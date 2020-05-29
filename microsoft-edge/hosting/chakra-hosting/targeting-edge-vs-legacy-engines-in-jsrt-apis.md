---
description: 'Saiba como direcionar os diferentes mecanismos JavaScript do Windows 10. '
title: Direcionando mecanismos do Microsoft Edge versus Legacy em APIs do JsRT | Documentos da Microsoft
ms.custom: ''
ms.date: 03/05/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: cbc7df6c-0bc9-48f5-b9ad-b9ed31c42f92
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ed0dc8c67b8189a7433d52185aa995997edb70a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560984"
---
# Direcionando mecanismos do Microsoft Edge versus Legacy em APIs do JsRT

O Windows 10 dá suporte a dois mecanismos JavaScript diferentes:

-   O antigo mecanismo de Chakra (também chamado de *mecanismo herdado* ou jscript9. dll abaixo) que acompanha e suporta o Internet Explorer 11. Esse mecanismo está congelado no tempo e permanecerá fundamentalmente inalterado do lançamento do Win 8.1/IE11.  
  
-   O novo mecanismo Chakra (também chamado de *Edge Engine* ou Chakra. dll abaixo) que acompanha e dá suporte ao novo navegador no Windows 10, Microsoft Edge. Este mecanismo será atualizado continuamente e dará suporte a um mecanismo de [borda](https://blogs.msdn.com/b/ie/archive/2014/11/11/living-on-the-edge-our-next-step-in-interoperability.aspx) "vivo". Um mecanismo dinâmico da Microsoft Edge sugere que, ao contrário do mecanismo herdado, o mecanismo Microsoft Edge não transportasse qualquer tipo de funcionalidade de script de controle de versão para aceitar.  
  
 Ao criar um aplicativo usando a API de Hospedagem de tempo de execução (JsRT) do JavaScript, você pode optar por direcionar o mecanismo herdado ou o Microsoft Edge.  
  
-   Se você precisar enfatizar a compatibilidade com versões anteriores de seus aplicativos existentes, destinar-se ao mecanismo herdado.  
  
-   Se você quiser que seu aplicativo seja encaminhado procurando e dê suporte a novos recursos JavaScript conforme eles são lançados (por exemplo, ECMAScript 6), destinam-se ao mecanismo Microsoft Edge.  
  
 Este tópico inclui detalhes que descrevem como direcionar os diferentes mecanismos.  
  
## Destinar-se à sua versão preferida  
 Ao criar um aplicativo, você pode selecionar a versão do JsRT que suporta o mecanismo Microsoft Edge ou o mecanismo herdado. Você pode escolher a versão do JsRT com base nas diretrizes acima. Para acomodar essas distinções, as seguintes alterações foram feitas em `JsCreateRuntime` , `JsCreateContext` e `JsStartDebugging` .  
  
 Para `JsCreateRuntime` :  
  
-   Ao direcionar o mecanismo herdado, o `JsRuntimeVersionEdge` valor de enumeração é preterido, e uma mensagem vai sugerir usar o `JsRuntimeVersionInternetExplorer11` valor em vez disso.  
  
-   Ao direcionar o mecanismo do Microsoft Edge, o parâmetro version é omitido da `JsCreateRuntime` função.  
  
    ```cpp  
    JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
    ```  
  
 Para `JsCreateContext` e `JsStartDebugging` :  
  
-   Ao direcionar o mecanismo herdado, a `IDebugApplication` interface é usada para fornecer seus próprios métodos de depuração não remotos. Para fins de depuração, `JsCreateContext` e `JsStartDebugging` as funções são executadas `IDebugApplication` como parâmetro.  
  
-   Ao direcionar o mecanismo do Microsoft Edge, a `IDebugApplication` interface é preterida. O mecanismo Chakra permite a funcionalidade de depuração nativa e de script com depurador do Visual Studio sem exigir uma implementação de `IDebugApplication` do usuário. A interface não é mais um parâmetro para `JsCreateContext` e `JsStartDebugging` como resultado.  
  
 As assinaturas para as APIs anteriores no mecanismo herdado são as seguintes:  
  
```cpp  
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsRuntimeVersion version, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
  
JsErrorCode JsCreateContext(JsRuntimeHandle runtime, IDebugApplication *debugApplication, JsContextRef *newContext);  
  
JsErrorCode JsStartDebugging(IDebugApplication *debugApplication);  
```  
  
 As assinaturas para as APIs anteriores no mecanismo Microsoft Edge são as seguintes:  
  
```cpp  
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
  
JsErrorCode JsCreateContext(JsRuntimeHandle runtime, JsContextRef *newContext);  
  
JsErrorCode JsStartDebugging();  
```  
  
## Compilar para a sua versão preferida usando o Visual C++  
 Ao usar o Visual C++, importe a API JsRT incluindo o cabeçalho JsRT. h e certifique-se de que JsRT. lib esteja incluído na sua lista de arquivos de entrada do vinculador:  
  
```cpp  
#include <jsrt.h>  
```  
  
 ![Adicionando jsrt. lib como um arquivo de entrada do vinculador](../chakra-hosting/media/js-chakra.png "JS_Chakra_")  
  
 Se quiser direcionar os binários do mecanismo Microsoft Edge, você precisa definir a macro `USE_EDGEMODE_JSRT` antes de incluir jsrt. h e, em vez de vincular a jsrt. lib, você deve vincular o chakrart. lib:  
  
```cpp  
#define USE_EDGEMODE_JSRT  
#include <jsrt.h>  
```  
  
 ![Adicionando chakrart. lib como um arquivo de entrada do vinculador](../chakra-hosting/media/js-chakra-hosting.png "JS_Chakra_Hosting_")  
  
 Se você estiver começando com um novo aplicativo, agora você está pronto para começar a escrever código com a API JsRT.  
  
## Compilar para a sua versão preferida usando o .NET  
 Se você estiver usando .NET e P/Invoke, será necessário alterar suas declarações API de JsRT [DllImport] para importar Chakra. dll em vez de jscript9. dll. Além disso, altere a definição de `JsCreateRuntime` para remover o `JsRuntimeVersion` parâmetro e a definição de `JsCreateContext` e `JsStartDebugging` para remover o `IDebugApplication` parâmetro.  
  
 Para o mecanismo herdado, use o código a seguir.  
  
```c#  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsCreateRuntime(  
    JsRuntimeAttributes attributes,  
    JsRuntimeVersion version,  
    JsThreadServiceCallback callback,  
    out JsRuntimeSafeHandle runtime  
);  
  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsCreateContext(  
    JsRuntimeSafeHandle runtime,  
    IDebugApplication debugApplication,  
    out JsContextRef newContext  
);   
  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsStartDebugging(  
    IDebugApplication debugApplication,  
);  
```  
  
 Para o mecanismo Microsoft Edge, use o código a seguir.  
  
```c#  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsCreateRuntime(  
    JsRuntimeAttributes attributes,  
    JsThreadServiceCallback callback,  
    out JsRuntimeSafeHandle runtime  
);  
  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsCreateContext(  
    JsRuntimeSafeHandle runtime,  
    out JsContextRef newContext  
);   
  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsStartDebugging();  
```  
  
> [!CAUTION]
>  Se você estiver fazendo o marshaling manual do ponteiro da função (como via LoadLibrary/GetProcAddress), é fundamental que você não misture as declarações do método ou desbalanceia a pilha, o que resultará em um comportamento imprevisível, como causar falha no aplicativo. O mesmo problema ocorrerá se você executar uma pesquisa global e substituir de instâncias de jscript9. dll no código de importação, porque perderá o `version` parâmetro sendo eliminado.  
  
## Resumo  
 No Windows 10, as APIs de hospedagem do tempo de execução do JavaScript estão sendo divididas em duas. Essas APIs agora dão suporte a um mecanismo "vivo" do Microsoft Edge, cujos recursos de idioma serão alinhados com o mecanismo "vivo" do Microsoft Edge no Microsoft Edge. Você pode aproveitar esses recursos da área de trabalho ou aplicativos da loja para criar maneiras novas e incríveis de estender o aplicativo e aproveitar habilidades modernas da Web em sua base de códigos existente. No entanto, como há diferenças sutis entre as versões anteriores, você deve estar ciente dos seguintes pontos ao direcionar a borda ou o mecanismo herdado.  
  
-   Seu aplicativo pode dar suporte a apenas uma versão do JsRT por processo.  
  
     Por exemplo, você não pode criar um tempo de execução do Microsoft Edge Engine e, em seguida, um tempo de execução do mecanismo herdado e esperar que eles sejam executados corretamente no mesmo processo. Isso não tem suporte e pode resultar em um comportamento não documentado, como falha ao carregar a segunda DLL.  
  
-   Ao direcionar o mecanismo do Microsoft Edge, seu aplicativo pode adquirir inesperadamente novos recursos quando a plataforma subjacente é atualizada automaticamente.  
  
     Por exemplo, o modo do Internet Explorer 11 do tempo de execução herdado dá suporte a declarações de variáveis de escopo de bloco, como `let` e `const` . Se o comportamento de controle automático do mecanismo de borda da Microsoft Edge era o padrão anteriormente, o código que funcionou no modo do Internet Explorer 10, que não tinha regras de escopo de bloco, pode ter começado a falhar quando a plataforma tiver sido atualizada automaticamente. Isso deve ser uma consideração ao escolher qual modelo de tempo de execução usar. Enquanto acreditamos que você deve direcionar o mecanismo Microsoft Edge sempre que possível, você deve ter cuidado em usar estruturas de código JavaScript que podem se tornar inválidas no futuro.  
  
-   O JsRT para a Windows Store só oferece suporte ao mecanismo Microsoft Edge (Chakra. dll). Os aplicativos que tentam se vincular a qualquer API do JsRT no jscript9. dll falham na certificação.  
  
-   É essencial que você não confunda a declaração de `JsCreateRuntime` , `JsCreateContext` e `JsStartDebugging` entre jscript9. dll e Chakra. dll, pois isso resultará em imbalancear a pilha.  
  
     Ao usar C e C++, você receberá um erro de vinculador se tentar usar a declaração errada, desde que não esteja fazendo algo como fazer chamadas `LoadLibrary` e, em seguida, `GetProcAddress` . Os desenvolvedores do .NET podem não encontrar esse problema com facilidade, portanto, clique duas vezes no seu código ao usar esse recurso.  
  
## Consulte também  
 [Hospedagem do tempo de execução JavaScript](../javascript-runtime-hosting.md)
 