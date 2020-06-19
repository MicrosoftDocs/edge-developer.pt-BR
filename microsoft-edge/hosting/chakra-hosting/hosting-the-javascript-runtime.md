---
description: Use o mecanismo JavaScript Chakra baseado em padrões para adicionar recursos de script ao seu aplicativo do Windows.
title: Hospedando o Runtime do JavaScript
ms.date: 06/18/2020
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: 30ec744e-57cc-4ef5-8fe1-d2c27b946548
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
ms.openlocfilehash: 043f7ecd174515ce407d2fc0c2bbe796fa2750a5
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752245"
---
# Hospedando o tempo de execução JavaScript  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

As APIs do tempo de execução do JavaScript (JsRT) fornecem uma maneira para aplicativos da área de trabalho, da Windows Store e do servidor em execução no sistema operacional Windows para adicionar recursos de script ao aplicativo usando o mecanismo JavaScript Chakra baseado em padrões, que também é usado pelo Microsoft Edge e pelo Internet Explorer. Essas APIs estão disponíveis no Windows 10 e em qualquer versão do sistema operacional Windows que tenha o Internet Explorer versão 11,0 instalado no computador. Para obter mais informações, consulte [referência (JavaScript Runtime)](../chakra-hosting/reference-javascript-runtime.md). Para obter informações sobre como usar o JsRT em aplicativos da Windows Store, consulte [JsRT e a plataforma universal do Windows](#Windows).  

> [!NOTE]
> Esta documentação pressupõe uma familiaridade de trabalho geral com a linguagem JavaScript.  

## Conceitos  

Entender como hospedar o mecanismo JavaScript usando as APIs JsRT depende de dois conceitos chave: runtimes e contextos de execução.  

Um *tempo de execução* representa um ambiente de execução JavaScript completo. Cada tempo de execução que é criado tem seu próprio heap de coleta de lixo isolado e, por padrão, seu próprio thread de compilador just-in-time (JIT) e o coletor de lixo (GC). Um *contexto de execução* representa um ambiente JavaScript que tem seu próprio objeto global JavaScript distinto de todos os outros contextos de execução. Um tempo de execução pode conter vários contextos de execução e, nesses casos, todos os contextos de execução compartilham o compilador JIT e o thread GC associado ao Runtime.  

Os tempos de execução representam um único thread de execução. Somente um tempo de execução pode estar ativo em um thread específico de cada vez, e um tempo de execução só pode estar ativo em um thread de cada vez. Os tempos de execução são alugados threads, portanto, um tempo de execução que não está ativo no momento em um thread (ou seja, não está executando qualquer código JavaScript ou respondendo a chamadas do host) pode ser usado em qualquer thread que ainda não tenha um tempo de execução ativo.  

Os contextos de execução estão ligados a um tempo de execução específico e executar o código dentro desse tempo de execução. Ao contrário dos tempos de execução, vários contextos de execução podem ficar ativos em um thread ao mesmo tempo. Para que um host possa fazer uma chamada em um contexto de execução, esse contexto de execução pode retornar a chamada para o host, e o host pode fazer uma chamada em um contexto de execução diferente.  

![Vários contextos de execução](../chakra-hosting/media/js-chakra-hosting.png "JS_Chakra_Hosting")  

Na prática, a menos que um host precise executar o código em ambientes separados, um único contexto de execução pode ser usado. Da mesma forma, a menos que um host precise executar várias partes de código simultaneamente, um único tempo de execução é suficiente.  

## Gerenciamento de memória  

JavaScript é uma linguagem coletada pelo Garbage Collector e, portanto, há várias considerações que devem ser mantidas em mente ao trabalhar com APIs do JsRT a partir de outro idioma.  

A principal consideração é que o coletor de lixo JavaScript só pode ver referências a valores em dois locais: o heap do tempo de execução e a pilha. Portanto, uma referência a um valor de JavaScript armazenado dentro de outro valor JavaScript ou em uma variável local na pilha será sempre vista pelo coletor de lixo. Mas as referências armazenadas em outros locais, como heaps gerenciadas pelo host ou sistema, não serão vistas pelo coletor de lixo e podem resultar em uma coleção prematuro de valores que ainda estão em uso pelo host.  

> [!IMPORTANT]
> Alguns compiladores de idiomas (como o compilador do Visual Studio C++) otimizarão as variáveis locais sempre que possível. Deve-se ter cuidado para garantir que as variáveis locais que fazem referência a valores JavaScript estejam na pilha se esperarem manter esses valores ativos.  

Se uma referência a um valor de JavaScript for armazenada em um local não visível para o coletor de lixo, o host deve adicionar e remover manualmente referências usando as APIs JsRT.  

## Manipulação de exceções  

Quando ocorre uma exceção JavaScript durante a execução do script, o tempo de execução contido é colocado em um estado de exceção. Durante um estado de exceção, nenhum código pode ser executado e todas as chamadas de API falharão com o código de erro `JsErrorInExceptionState` até que o host recupere e limpe a exceção usando a `JsGetAndClearException` API. Se o host retornar de um retorno de chamada JavaScript sem limpar o tempo de execução de um estado de exceção, a exceção JavaScript será lançada novamente assim que o controle passar de volta para o mecanismo JavaScript. Isso também permite que os retornos de chamada do host "acionem" uma exceção JavaScript definindo o tempo de execução em um estado de exceção e, em seguida, retornando de um retorno de chamada do host.  

Um host não tem permissão para permitir que suas próprias exceções internas sejam propagadas em um retorno de chamada do host – qualquer método de retorno de chamada deve detectar todas as exceções de host antes de retornar o controle ao Runtime.  

## Uso de recursos de tempo de execução  

As APIs do JsRT expõem uma série de como monitorar e modificar o modo em que os tempos de execução usam recursos. Eles geralmente dividem-se nas seguintes categorias:  

*   **Uso de thread**. Por padrão, cada tempo de execução criará um thread de compilador JIT dedicado e um thread GC dedicado que servirá de acordo com o tempo de execução. Se um tempo de execução for criado com o `JsRuntimeAttributeDisableBackgroundWork` sinalizador, o trabalho JIT e GC será executado no próprio thread do tempo de execução, em vez de threads de segundo plano separados para cada um deles. Um host também pode fornecer um retorno de chamada de serviço de thread para a `JsCreateRuntime` chamada, o que permitirá que o host agende o JIT e o GC funcione de maneira adequada.
*   **Uso de memória**. Há várias maneiras de monitorar e modificar o uso da memória de um tempo de execução. Se o tempo de execução estiver em execução por muito tempo, o host poderá especificar o `JsRuntimeAttributeEnableIdleProcessing` sinalizador ao criar o tempo de execução e, em seguida, chamar `JsIdle` quando o host estiver em um estado ocioso. Isso permite que o mecanismo adie alguns trabalhos de limpeza e escrituração de memória até o tempo ocioso.  
    
    O host pode monitorar as coletas de lixo chamando `JsSetRuntimeBeforeCollectCallback` . Ele também pode monitorar as atribuições feitas pelo heap chamando `JsSetRuntimeMemoryAllocationCallback` . Observe que essa API não chama novamente todas as atribuições de JavaScript, apenas quando a pilha do tempo de execução precisa de mais espaço do qual atribuir. O retorno de chamada de alocação de memória tem permissão para recusar a solicitação, que acionará uma coleta de lixo e, se não houver memória disponível, um erro de falta de memória no tempo de execução.  
    
    O host também pode chamar `JsSetRuntimeMemoryLimit` para definir um limite para a quantidade de memória que um tempo de execução pode usar. Quando um tempo de execução atinge um limite, ele aciona uma coleta de lixo e, se não houver memória disponível, um erro de falta de memória será lançado pelo tempo de execução.  
    
*   **Interrupções e avaliações de script**. O host pode chamar `JsDisableRuntimeExecution` para terminar a execução dentro de um tempo de execução. Esta chamada pode ser feita a qualquer momento e a partir de qualquer thread. Como a terminação de script depende de atingir pontos de proteção inseridos no código, um script não pode terminar no momento exato, mas fará isso logo em seguida. Por padrão, os pontos de proteção de término são colocados no código gerado de modo conservador e podem não cobrir todas as situações, como um loop infinito. A criação do tempo de execução com o `JsRuntimeAttributeAllowScriptInterrupt` sinalizador faz com que o tempo de execução insira verificações adicionais de loops infinitos, muitas vezes pelo custo de uma pequena sobrecarga de desempenho.  
    
    Se um host quiser impedir a geração de código nativo pelo compilador JIT, ele poderá especificar o `JsRuntimeAttributeDisableNativeCodeGeneration` sinalizador. Um host também pode impedir que os scripts executem scripts dinamicamente especificando o `JsRuntimeAttributeDisableEval` sinalizador.  
    
## Depuração e criação de perfil  

As APIs do JsRT dão suporte à depuração e ao profiling por meio da tecnologia de script ativo.  

A partir do Windows 10, o mecanismo de JavaScript Chakra dá suporte ao mecanismo do Internet Explorer (MSHTML) herdado e ao novo mecanismo Microsoft Edge (EdgeHTML), e você pode direcionar no JsRT (consulte [direcionando o Microsoft Edge versus mecanismos herdados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md) para obter detalhes). A depuração de um script no Visual Studio funciona de forma diferente entre o mecanismo herdado e o mecanismo do Microsoft Edge. Com o mecanismo herdado, o host precisa fornecer um ponteiro de [interface IDebugApplication](/scripting/winscript/reference/idebugapplication-interface) , que pode ser obtido de uma instância de [interface IProcessDebugManager](/scripting/winscript/reference/iprocessdebugmanager-interface) . Com o mecanismo Microsoft Edge, `IDebugApplication` está obsoleto, e o mecanismo Chakra permite recursos de depuração nativa e de script por meio do depurador do Visual Studio sem exigir uma implementação do `IDebugApplication` usuário.  

Para criar scripts em um debuggable de contexto de execução, o mecanismo de Chakra precisa alternar para usar métodos de execução de código menos eficientes. Assim, o código debuggable geralmente é executado de forma mais lenta do que o código não debuggable. Como resultado, com o mecanismo herdado, um host pode optar por iniciar a depuração em um contexto de execução desde o início fornecendo o `IDebugApplication` ponteiro para cima `JsCreateContext` , ou pode aguardar até que a depuração seja necessária e, em seguida, chamar `JsStartDebugging` . Com o mecanismo Microsoft Edge, você `JsCreateContext` não obtém mais um `IDebugApplication` parâmetro e, como resultado, o script é debuggable somente após `JsStartDebugging` ser chamado. Durante a depuração usando o Visual Studio, a opção do depurador "script" deve estar habilitada.  

O código JavaScript em um contexto de execução pode ser profiledo de uma das duas maneiras. A linha de comando do Visual Studio Profiler (vsperf.exe) pode ser usada no Windows 8,1 e em versões posteriores com a opção/js para produzir um relatório direcionado ao código JavaScript executado no aplicativo. Ou o host pode chamar diretamente `JsStartProfiling` e `JsStopProfiling` fornecer um retorno de chamada para fazer o próprio profiling. O host também pode examinar o estado da pilha coletada pelo Garbage ao chamar `JsEnumerateHeap` . A criação de perfil no JsRT funciona da mesma maneira entre o mecanismo herdado e o Microsoft Edge Engine. No entanto, as APIs de criação de perfil do JsRT ( `JsStartProfiling` , `JsStopProfiling` ,, `JsEnumerateHeap` e `JsIsEnumeratingHeap` ) não estão disponíveis para aplicativos universais do Windows.  

<a name="Windows"></a>   

## JsRT e a plataforma universal do Windows  

Você pode usar APIs JsRT para adicionar recursos de script a um aplicativo universal do Windows. Um aplicativo universal do Windows que usa as APIs JsRT precisará direcionar as APIs do Microsoft Edge JSRT, que, por sua vez, direcionam o mecanismo Chakra do Edge. Para obter mais informações, consulte [direcionar mecanismos do Microsoft Edge versus Legacy](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md). A API JsRT completa está disponível para aplicativos universais do Windows, exceto para a criação de perfil e suporte à enumeração de heap ( `JsStartProfiling` ,, `JsStopProfiling` `JsEnumerateHeap` e `JsIsEnumeratingHeap` não são suportados).  

O JsRT também permite que os scripts acessem nativamente todas as [APIs da plataforma universal do Windows (UWP)](https://msdn.microsoft.com/library/windows/apps/br211377.aspx) depois de expor o namespace da API por meio da API do Microsoft Edge JsRT `JsProjectWinRTNamespace` . Embora os aplicativos universais do Windows não exijam configuração, além da projeção de namespaces necessários, em um aplicativo do Windows clássico (Win32), um mecanismo de bombeamento delegado inicializado COM deve ser habilitado `JsSetProjectionEnqueueCallback` para habilitar eventos e APIs assíncronas. O exemplo de Win32 a seguir usa APIs UWP assíncronas para criar um cliente http para obter conteúdo de um URI:  

```cpp
typedef struct _jsCall {
    JsProjectionCallback jsCallback;
    JsProjectionCallbackContext jsContext;
    HANDLE event;
} jsCall;

// Set up delegated pumping mechanism; not necessary in UWP applications.
jsCall outstandingCall = {};
CoInitializeEx(nullptr, COINIT_MULTITHREADED);
JsSetProjectionEnqueueCallback([](JsProjectionCallback jsCallback,
JsProjectionCallbackContext jsContext, void *callbackState) {
    jsCall* call = (jsCall*)callbackState;
    call->jsCallback = jsCallback;
    call->jsContext = jsContext;
    SetEvent(call->event);
    },
&outstandingCall);
HANDLE event = CreateEventEx(NULL, NULL, CREATE_EVENT_MANUAL_RESET, EVENT_ALL_ACCESS);
outstandingCall.event = event;

// Project necessary namespaces.
JsProjectWinRTNamespace(L"Windows.Foundation");
JsProjectWinRTNamespace(L"Windows.Web");

// Get content from an Uri.
JsRunScript(L"var uri = new Windows.Foundation.Uri(\"http://somedatasource.com\"); " \
    L"var httpClient = new Windows.Web.Http.HttpClient();" \
    L"httpClient.getStringAsync(uri).done(function (content) { " \
    L"    // do something with the string content " \
    L"}, onError); " \
    L"function onError(reason) { " \
    L"    // error handling " \
    L"}",
    currentSourceContext, L"", &result);

// Wait for async call to come in and then execute; not necessary in UWP applications.
WaitForSingleObjectEx(outstandingCall.event, 10000, FALSE) == WAIT_OBJECT_0;
outstandingCall.jsCallback(outstandingCall.jsContext);
```  

## Consulte também  

*   [Aplicativo de exemplo do tempo de execução JavaScript](https://go.microsoft.com/fwlink/p/?LinkID=306674&clcid=0x409)   
*   [Referência (Runtime do JavaScript)](../chakra-hosting/reference-javascript-runtime.md)   
*   [Hospedagem de Runtime no JavaScript](../javascript-runtime-hosting.md)  
