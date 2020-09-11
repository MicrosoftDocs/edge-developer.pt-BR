---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2
ms.openlocfilehash: ca31ddd3536350d3b3bdd02b445b4c47589f7dba
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011108"
---
# classe 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

O WebView2 permite que você hospede conteúdo da Web usando a tecnologia de navegador da Web mais recente do Edge.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[BrowserProcessId](#browserprocessid) | A ID do processo do navegador que hospeda o WebView.
[CanGoBack](#cangoback) | Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação.
[CanGoForward](#cangoforward) | Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação.
[ContainsFullScreenElement](#containsfullscreenelement) | Indica se a WebView contém um elemento HTML de tela inteira.
[ContainsFullScreenElementChanged](#containsfullscreenelementchanged) | Notifica quando a propriedade ContainsFullScreenElement muda.
[ContentLoading](#contentloading) | ContentLoading é acionado antes que qualquer conteúdo seja carregado, incluindo scripts adicionados com AddScriptToExecuteOnDocumentCreated ContentLoading não será acionado se ocorrer uma mesma navegação de página (por exemplo, por meio de navegações de fragmento ou de histórico. pushstate).
[DocumentTitle](#documenttitle) | O título do documento atual de nível superior.
[DocumentTitleChanged](#documenttitlechanged) | O evento é acionado quando a propriedade DocumentTitle da WebView muda e pode ser acionada antes ou depois do evento NavigationCompleted.
[FrameNavigationCompleted](#framenavigationcompleted) | O evento FrameNavigationCompleted é acionado quando um quadro filho é completamente carregado (Body. OnLoad foi acionado) ou o carregamento parou com o erro.
[FrameNavigationStarting](#framenavigationstarting) | FrameNavigationStarting é acionado quando um quadro filho na WebView solicita permissão para navegar para um URI diferente.
[Historychanged](#historychanged) | Cobrançaalterar Ouça a alteração do histórico de navegação do documento de nível superior.
[NavigationCompleted](#navigationcompleted) | O evento NavigationCompleted é acionado quando o WebView foi completamente carregado (Body. OnLoad foi acionado) ou o carregamento parou com o erro.
[NavigationStarting](#navigationstarting) | NavigationStarting é acionado quando o quadro principal do WebView está solicitando permissão para navegar para um URI diferente.
[NewWindowRequested](#newwindowrequested) | Acionado quando o conteúdo dentro do WebView solicitado para abrir uma nova janela, por exemplo, por meio de Window. Open.
[PermissionRequested](#permissionrequested) | Acionado quando o conteúdo de uma WebView solicita permissão para acessar alguns recursos privilegiados.
[ProcessFailed](#processfailed) | Acionado quando um processo da WebView termina inesperadamente ou não responde.
[ScriptDialogOpening](#scriptdialogopening) | O evento é acionado quando uma caixa de diálogo JavaScript (alerta, confirmação ou prompt) aparecerá para o WebView.
[Configurações](#settings) | O objeto CoreWebView2Settings contém várias configurações modificáveis para a execução
[Origem](#source) | O URI do documento de nível superior atual.
[SourceChanged](#sourcechanged) | SourceChanged é acionado quando a propriedade Source muda.
[WebMessageReceived](#webmessagereceived) | Esse evento é acionado quando a configuração IsWebMessageEnabled é definida e o documento de nível superior das chamadas WebView `window.chrome.webview.postMessage` .
[WebResourceRequested](#webresourcerequested) | Acionado quando o WebView está executando uma solicitação HTTP para uma URL correspondente e um filtro de contexto de recurso que foi adicionado com o AddWebResourceRequestedFilter.
[WebResourceResponseReceived](#webresourceresponsereceived) | O evento WebResourceResponseReceived é acionado depois que a WebView recebeu e processou a resposta de uma solicitação WebResource.
[WindowCloseRequested](#windowcloserequested) | Dispara quando o conteúdo dentro do WebView solicitado para fechar a janela, como After Window. Close, é chamado.
[AddHostObjectToScript](#addhostobjecttoscript) | Adicione o objeto de host fornecido ao script em execução no WebView com o nome especificado.
[AddScriptToExecuteOnDocumentCreatedAsync](#addscripttoexecuteondocumentcreatedasync) | Adicione o JavaScript fornecido a uma lista de scripts que devem ser executados após a criação do objeto global, mas antes de o documento HTML ter sido analisado e antes de qualquer outro script incluído no documento HTML ser executado.
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | Adiciona um URI e um filtro de contexto de recurso ao evento WebResourceRequested.
[CallDevToolsProtocolMethodAsync](#calldevtoolsprotocolmethodasync) | Chame um método DevToolsProtocol assíncrono.
[CapturePreviewAsync](#capturepreviewasync) | Capture uma imagem do que o WebView está exibindo.
[ExecuteScriptAsync](#executescriptasync) | Execute o código JavaScript do parâmetro JavaScript no documento de nível superior atual renderizado no WebView.
[GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver) | Obtenha um receptor de evento de protocolo DevTools que permite que você se inscreva em um evento de protocolo DevTools.
[GoBack](#goback) | Navega o WebView para a página anterior no histórico de navegação.
[GoForward](#goforward) | Navega o WebView para a próxima página no histórico de navegação.
[Navegar](#navigate) | Fazer uma navegação do documento de nível superior para o URI especificado.
[NavigateToString](#navigatetostring) | Inicia uma navegação para htmlContent como código-fonte HTML de um novo documento.
[OpenDevToolsWindow](#opendevtoolswindow) | Abre a janela do DevTools para o documento atual no WebView.
[PostWebMessageAsJson](#postwebmessageasjson) | Postar a WebMessage especificada no documento de nível superior neste WebView.
[PostWebMessageAsString](#postwebmessageasstring) | Isso é um auxiliar para postar uma mensagem que é uma cadeia de caracteres simples em vez de uma representação JSON de cadeia de caracteres de um objeto JavaScript.
[Recarregar](#reload) | Recarregar a página atual.
[RemoveHostObjectFromScript](#removehostobjectfromscript) | Remova o objeto host especificado pelo nome para que ele não fique mais acessível a partir do código JavaScript na WebView.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Remova o JavaScript correspondente adicionado via AddScriptToExecuteOnDocumentCreated com a ID de script especificada.
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | Remove um filtro WebResource correspondente que foi adicionado anteriormente ao evento WebResourceRequested.
[Parar](#stop) | Interrompa todas as navegações e buscas de recursos pendentes.

## Parte

#### BrowserProcessId 

A ID do processo do navegador que hospeda o WebView.

> Public uint [BrowserProcessId](#browserprocessid)

#### CanGoBack 

Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação.

> bool público [CanGoBack](#cangoback)

O evento Historychanged será acionado se CanGoBack alterar Value.

#### CanGoForward 

Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação.

> Public bool [CanGoForward](#cangoforward)

O evento Historychanged será acionado se CanGoForward alterar Value.

#### ContainsFullScreenElement 

Indica se a WebView contém um elemento HTML de tela inteira.

> Public bool [ContainsFullScreenElement](#containsfullscreenelement)

#### ContainsFullScreenElementChanged 

Notifica quando a propriedade ContainsFullScreenElement muda.

> objeto<-EventHandler de evento público > [ContainsFullScreenElementChanged](#containsfullscreenelementchanged)

Isso significa que um elemento HTML dentro do WebView está entrando em tela inteira no tamanho do WebView ou sai do fullscreen. Esse evento é útil quando, por exemplo, um elemento de vídeo solicita a tela inteira. O ouvinte de ContainsFullScreenElementChanged pode então redimensionar a WebView em resposta.

#### ContentLoading 

ContentLoading é acionado antes que qualquer conteúdo seja carregado, incluindo scripts adicionados com AddScriptToExecuteOnDocumentCreated ContentLoading não será acionado se ocorrer uma mesma navegação de página (por exemplo, por meio de navegações de fragmento ou de histórico. pushstate).

> < do evento público EventHandler [CoreWebView2ContentLoadingEventArgs](microsoft-web-webview2-core-corewebview2contentloadingeventargs.md)  >  [ContentLoading](#contentloading)

Isso segue os eventos NavigationStarting e SourceChanged e precede os eventos Historychanged e NavigationCompleted.

#### DocumentTitle 

O título do documento atual de nível superior.

> Cadeia de caracteres pública [DocumentTitle](#documenttitle)

Se o documento não tiver um título explícito ou estiver vazio, um padrão que pode ou não corresponder ao URI do documento será usado.

#### DocumentTitleChanged 

O evento é acionado quando a propriedade DocumentTitle da WebView muda e pode ser acionada antes ou depois do evento NavigationCompleted.

> objeto<-EventHandler de evento público > [DocumentTitleChanged](#documenttitlechanged)

#### FrameNavigationCompleted 

O evento FrameNavigationCompleted é acionado quando um quadro filho é completamente carregado (Body. OnLoad foi acionado) ou o carregamento parou com o erro.

> < do evento público EventHandler [CoreWebView2NavigationCompletedEventArgs](microsoft-web-webview2-core-corewebview2navigationcompletedeventargs.md)  >  [FrameNavigationCompleted](#framenavigationcompleted)

#### FrameNavigationStarting 

FrameNavigationStarting é acionado quando um quadro filho na WebView solicita permissão para navegar para um URI diferente.

> < do evento público EventHandler [CoreWebView2NavigationStartingEventArgs](microsoft-web-webview2-core-corewebview2navigationstartingeventargs.md)  >  [FrameNavigationStarting](#framenavigationstarting)

Isso também será acionado para redirecionamentos.

#### Historychanged 

Cobrançaalterar Ouça a alteração do histórico de navegação do documento de nível superior.

> objeto<-EventHandler de evento público > [historychanged](#historychanged)

Use Cobrançaalterar para verificar se o valor CanGoBack/CanGoForward foi alterado. Historychanged também é acionado para usar o GoBack/GoForward. Historychanged é acionado após SourceChanged e ContentLoading. Adicione um manipulador de eventos para o evento Historychanged.

#### NavigationCompleted 

O evento NavigationCompleted é acionado quando o WebView foi completamente carregado (Body. OnLoad foi acionado) ou o carregamento parou com o erro.

> < do evento público EventHandler [CoreWebView2NavigationCompletedEventArgs](microsoft-web-webview2-core-corewebview2navigationcompletedeventargs.md)  >  [NavigationCompleted](#navigationcompleted)

#### NavigationStarting 

NavigationStarting é acionado quando o quadro principal do WebView está solicitando permissão para navegar para um URI diferente.

> < do evento público EventHandler [CoreWebView2NavigationStartingEventArgs](microsoft-web-webview2-core-corewebview2navigationstartingeventargs.md)  >  [NavigationStarting](#navigationstarting)

Isso também será acionado para redirecionamentos.

#### NewWindowRequested 

Acionado quando o conteúdo dentro do WebView solicitado para abrir uma nova janela, por exemplo, por meio de Window. Open.

> < do evento público EventHandler [CoreWebView2NewWindowRequestedEventArgs](microsoft-web-webview2-core-corewebview2newwindowrequestedeventargs.md)  >  [NewWindowRequested](#newwindowrequested)

O aplicativo pode passar um WebView de destino que será considerado a janela aberta.

#### PermissionRequested 

Acionado quando o conteúdo de uma WebView solicita permissão para acessar alguns recursos privilegiados.

> < do evento público EventHandler [CoreWebView2PermissionRequestedEventArgs](microsoft-web-webview2-core-corewebview2permissionrequestedeventargs.md)  >  [PermissionRequested](#permissionrequested)

#### ProcessFailed 

Acionado quando um processo da WebView termina inesperadamente ou não responde.

> < do evento público EventHandler [CoreWebView2ProcessFailedEventArgs](microsoft-web-webview2-core-corewebview2processfailedeventargs.md)  >  [ProcessFailed](#processfailed)

#### ScriptDialogOpening 

O evento é acionado quando uma caixa de diálogo JavaScript (alerta, confirmação ou prompt) aparecerá para o WebView.

> < do evento público EventHandler [CoreWebView2ScriptDialogOpeningEventArgs](microsoft-web-webview2-core-corewebview2scriptdialogopeningeventargs.md)  >  [ScriptDialogOpening](#scriptdialogopening)

Esse evento só será acionado se a propriedade CoreWebView2Settings. AreDefaultScriptDialogsEnabled estiver definida como false. O evento ScriptDialogOpening pode ser usado para suprimir caixas de diálogo ou substituir caixas de diálogo padrão por caixas de diálogo personalizadas.

#### Configurações 

O objeto CoreWebView2Settings contém várias configurações modificáveis para a execução

> [configurações](#settings) de [CoreWebView2Settings](microsoft-web-webview2-core-corewebview2settings.md) público

#### Origem 

O URI do documento de nível superior atual.

> [fonte](#source) de cadeia de caracteres pública

Esse valor potencialmente muda como parte do acionamento do evento SourceChanged para alguns casos, como navegar para diferentes navegação de site ou de fragmento. Ele permanecerá o mesmo para outros tipos de navegação, como recarregamentos de página ou historystate com a mesma URL que a página atual.

#### SourceChanged 

SourceChanged é acionado quando a propriedade Source muda.

> evento público EventHandler< [CoreWebView2SourceChangedEventArgs](microsoft-web-webview2-core-corewebview2sourcechangedeventargs.md)  >  [SourceChanged](#sourcechanged)

SourceChanged é acionado para navegar para um site ou navegação de fragmento diferente. Ele não será acionado para outros tipos de navegação, como recarregamentos de página ou historystate com a mesma URL que a página atual. SourceChanged é acionado antes de ContentLoading para navegação para um novo documento. Adicione um manipulador de eventos para o evento SourceChanged.

#### WebMessageReceived 

Esse evento é acionado quando a configuração IsWebMessageEnabled é definida e o documento de nível superior das chamadas WebView `window.chrome.webview.postMessage` .

> < do evento público EventHandler [CoreWebView2WebMessageReceivedEventArgs](microsoft-web-webview2-core-corewebview2webmessagereceivedeventargs.md)  >  [WebMessageReceived](#webmessagereceived)

A função CreateMessage é `void postMessage(object)` onde o objeto é qualquer objeto compatível com a conversão JSON. Quando a "CreateMessage" é chamado, o conjunto de CoreWebView2WebMessageReceivedEventHandler é invocado com o parâmetro de objeto da createmessagestring convertido em uma cadeia de caracteres JSON.

#### WebResourceRequested 

Acionado quando o WebView está executando uma solicitação HTTP para uma URL correspondente e um filtro de contexto de recurso que foi adicionado com o AddWebResourceRequestedFilter.

> < do evento público EventHandler [CoreWebView2WebResourceRequestedEventArgs](microsoft-web-webview2-core-corewebview2webresourcerequestedeventargs.md)  >  [WebResourceRequested](#webresourcerequested)

Pelo menos um filtro deve ser adicionado para que o evento seja acionado.

#### WebResourceResponseReceived 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

O evento WebResourceResponseReceived é acionado depois que a WebView recebeu e processou a resposta de uma solicitação WebResource.

> < do evento público EventHandler [CoreWebView2WebResourceResponseReceivedEventArgs](microsoft-web-webview2-core-corewebview2webresourceresponsereceivedeventargs.md)  >  [WebResourceResponseReceived](#webresourceresponsereceived)

Os args de evento incluem o WebResourceRequest como enviado pelo fio e WebResourceResponse recebidos, incluindo outros cabeçalhos adicionais adicionados pela pilha de rede que não foram incluídos como parte do evento WebResourceRequested associado, como cabeçalhos de autenticação.

#### WindowCloseRequested 

Dispara quando o conteúdo dentro do WebView solicitado para fechar a janela, como After Window. Close, é chamado.

> objeto<-EventHandler de evento público > [WindowCloseRequested](#windowcloserequested)

O aplicativo deve fechar a janela da WebView e do aplicativo relacionado se isso fizer sentido com o aplicativo.

#### AddHostObjectToScript 

Adicione o objeto de host fornecido ao script em execução no WebView com o nome especificado.

> public void [AddHostObjectToScript](#addhostobjecttoscript)(nome da cadeia de caracteres, rawObject do objeto)

Os objetos host são expostos como proxies do objeto host via `window.chrome.webview.hostObjects.{name}` . Os proxies do objeto host são promessas e serão resolvidos para um objeto que representa o objeto host. O código JavaScript na WebView poderá acessar o appObject da seguinte forma e, em seguida, acessar atributos e métodos de appObject: 
```
let app_object = await window.chrome.webview.hostObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```
 Observe que, enquanto tipos simples, IDispatch e matriz são compatíveis, IUnknown Generic, VT_DECIMAL ou Variant VT_RECORD não é suportada. Objetos JavaScript remotos como funções de retorno de chamada são representados como uma variante VT_DISPATCH com o objeto que implementa IDispatch. O método de retorno de chamada JavaScript pode ser invocado usando DISPID_VALUE para o DISPID. Há suporte para matrizes aninhadas até uma profundidade de 3. Matrizes de tipos de referência não são suportadas. VT_EMPTY e VT_NULL são mapeados para JavaScript como nulo. Em JavaScript nulo e indefinido são mapeados para VT_EMPTY.

Além disso, todos os objetos de host são expostos como `window.chrome.webview.hostObjects.sync.{name}` . Aqui, os objetos do host são expostos como proxies síncronos do objeto de host. Elas não são promessas e chamadas para funções ou acesso à propriedade o bloqueio síncrono de script em execução, aguardando a comunicação de processo cruzado para o código do host ser executado. Portanto, isso pode resultar em problemas de confiabilidade e é recomendável que você use a API assíncrona baseada em promessa `window.chrome.webview.hostObjects.{name}` descrita acima.

Proxies síncronos de objeto de host síncrono e proxies de objeto de host assíncrono podem proxy para o mesmo objeto host. As alterações remotas feitas por um proxy serão refletidas em qualquer outro proxy do mesmo objeto host se os outros proxies e síncronos ou assíncronos.

Embora o JavaScript seja bloqueado em uma chamada síncrona para o código nativo, esse código nativo não pode retornar a chamada para JavaScript. As tentativas de fazer isso falharão com o HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).

Os proxies do objeto de host são objetos de proxy JavaScript que interceptam todas as chamadas de propriedade, conjunto de propriedades e método. Propriedades ou métodos que fazem parte da função ou do protótipo do objeto são executados localmente. Além disso, qualquer propriedade ou método na matriz `chrome.webview.hostObjects.options.forceLocalProperties` também será executado localmente. Isso assume como padrão os métodos opcionais que têm significado em JavaScript como `toJSON` e `Symbol.toPrimitive` . Você pode adicionar mais à matriz, conforme necessário.

Há um método `chrome.webview.hostObjects.cleanupSome` que melhor irá melhorar os proxies do objeto do host de coleta de lixo.

Os proxies de objetos host também têm os seguintes métodos que são executados localmente:

* applyHostFunction, gethostproperty, sethostproperty: realize uma invocação de método, uma propriedade get ou um conjunto de propriedades no objeto host. Você pode usá-los para forçar explicitamente um método ou uma propriedade para execução remota se houver um método ou uma propriedade local conflitante. Por exemplo, ele `proxy.toString()` executará o método ToString local no objeto proxy. Mas `proxy.applyHostFunction('toString')` é executado `toString` no objeto de proxy do host em vez disso.

* getlocalproperty, setlocalproperty: executar propriedade get ou Property definido localmente. Você pode usar esses métodos para forçar a obtenção ou configuração de uma propriedade no próprio proxy do objeto host, em vez de no objeto host que ele representa. Por exemplo, receberá `proxy.unknownProperty` a propriedade nomeada `unknownProperty` do objeto host com proxy. Mas receberá `proxy.getLocalProperty('unknownProperty')` o valor da propriedade `unknownProperty` no próprio objeto proxy.

* sincronização: proxies de objeto de host assíncronos expõem um método Sync que retorna uma promessa para um proxy de objeto de host síncrono para o mesmo objeto host. Por exemplo, `chrome.webview.hostObjects.sample.methodCall()` retorna um proxy de objeto de host assíncrono. Você pode usar o `sync` método para obter um proxy de objeto de host síncrono em vez disso: `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`

* Async: proxies de objeto de host síncronos expõem um método Async que bloqueia e retorna um proxy de objeto de host assíncrono para o mesmo objeto host. Por exemplo, `chrome.webview.hostObjects.sync.sample.methodCall()` retorna um proxy de objeto de host síncrono. Chamar o `async` método nesse bloco e, em seguida, retorna um proxy de objeto de host assíncrono para o mesmo objeto host: `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`

* em seguida: proxies de objetos de host assíncronos têm um método Where. Isso permite que eles sejam awaitable. `then` retornará uma promessa que será resolvida com uma representação do objeto host. Se o proxy representar um literal JavaScript, uma cópia dele será retornada localmente. Se o proxy representar uma função, um proxy não awaitable será retornado. Se o proxy representar um objeto JavaScript com uma mistura de propriedades literais e propriedades de função, a cópia do objeto será retornada com algumas propriedades como proxies de objeto host.

Todas as outras invocações de método e Propriedade (além dos métodos de proxy de objeto remoto acima, lista de forceLocalProperties e propriedades em protótipos de objeto e função) são executadas remotamente. Proxies de objetos de host assíncronos retornam uma promessa que representa a conclusão assíncrona da invocação remota do método ou a obtenção da propriedade. A promessa é resolvida após a conclusão das operações remotas e as promessas são resolvidas para o valor resultante da operação. Os proxies de objeto de host síncrono funcionam da mesma forma, mas bloqueiam a execução de JavaScript e aguardam a conclusão da operação remota.

A configuração de uma propriedade em um proxy de objeto de host assíncrono funciona de forma ligeiramente diferente. O conjunto retorna imediatamente e o valor de retorno é o valor que será definido. Isso é uma exigência do objeto proxy JavaScript. Se você precisar esperar assincronamente o conjunto de propriedades para concluir, use o método sethostproperty que retorna uma promessa conforme descrito acima. Propriedade de conjunto de propriedades de objeto síncrono bloqueia sincronamente, até que a propriedade seja definida.

#### AddScriptToExecuteOnDocumentCreatedAsync 

Adicione o JavaScript fornecido a uma lista de scripts que devem ser executados após a criação do objeto global, mas antes de o documento HTML ter sido analisado e antes de qualquer outro script incluído no documento HTML ser executado.

> Cadeia de caracteres de< de tarefas assíncronas pública > [AddScriptToExecuteOnDocumentCreatedAsync](#addscripttoexecuteondocumentcreatedasync)(cadeia de caracteres JavaScript)

##### Devolver
Retorna uma ID de script que pode ser passada ao chamar [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated). 

O script injetado se aplicará a todas as futuras navegações de documento de nível superior e quadro filho até que sejam removidas com o RemoveScriptToExecuteOnDocumentCreated. Isso é aplicado de forma assíncrona e você deve aguardar até que o manipulador de conclusão seja executado antes de poder ter certeza de que o script está pronto para ser executado em navegações futuras.

Observe que, se um documento HTML tiver uma área restrita de algum tipo via propriedades de [área restrita](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) ou o [cabeçalho HTTP de política de segurança de conteúdo](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , isso afetará o script ser executado aqui. Portanto, por exemplo, se a palavra-chave ' allow-janelarestritas ' não estiver definida, as chamadas para a `alert` função serão ignoradas.

#### AddWebResourceRequestedFilter 

Adiciona um URI e um filtro de contexto de recurso ao evento WebResourceRequested.

> public void [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(URI da cadeia de caracteres, CoreWebView2WebResourceContext ResourceContext)

O parâmetro URI pode ser uma cadeia de caracteres curinga (' ': zero ou mais, '? ': exatamente um). nullptr é equivalente a L "". Consulte Enumeração CoreWebView2WebResourceContext para obter descrição dos filtros de contexto de recurso.

#### CallDevToolsProtocolMethodAsync 

Chame um método DevToolsProtocol assíncrono.

> Tarefa assíncrona pública< cadeia de caracteres > [CallDevToolsProtocolMethodAsync](#calldevtoolsprotocolmethodasync)(cadeia de caracteres MethodName, Cadeia de caracteres parametersAsJson)

##### Devolver
Uma cadeia de caracteres JSON que representa o objeto de retorno do método. 

Consulte o [Visualizador de protocolo devtools](https://aka.ms/DevToolsProtocolDocs) para obter uma lista e a descrição dos métodos disponíveis. O parâmetro methodName é o nome completo do método no formato `{domain}.{method}` . O parâmetro parametersAsJson é uma cadeia de caracteres JSON formatada que contém os parâmetros para o método correspondente. O método Invoke do manipulador será chamado quando o método for concluído de forma assíncrona. Invoke será chamado com o objeto Return do método como uma cadeia de caracteres JSON.

#### CapturePreviewAsync 

Capture uma imagem do que o WebView está exibindo.

> [CapturePreviewAsync](#capturepreviewasync)de tarefas assíncronas públicas (CoreWebView2CapturePreviewImageFormat ImageFormat, ImageStream de fluxo)

Especifique o formato da imagem com o parâmetro imageFormat. Os dados binários da imagem resultante são gravados no parâmetro imageStream fornecido. Quando o CapturePreview termina de gravar no fluxo, o método Invoke no parâmetro do manipulador fornecido é chamado.

#### ExecuteScriptAsync 

Execute o código JavaScript do parâmetro JavaScript no documento de nível superior atual renderizado no WebView.

> Cadeia de caracteres de< de tarefas assíncronas pública > [ExecuteScriptAsync](#executescriptasync)(cadeia de caracteres JavaScript)

##### Devolver
Retorna uma cadeia de caracteres codificada JSON que representa o resultado da execução do JavaScript fornecido. 

Esse método executa o JavaScript fornecido de forma assíncrona e retornará o resultado do JavaScript fornecido. Se o resultado do JavaScript fornecido for `undefined` , contiver um ciclo de referência ou não puder ser codificado em JSON, a cadeia de caracteres ' NULL ' será retornada. Se uma função chamada no JavaScript fornecido não tiver valor de retorno explícito, `undefined` será retornada. Se o JavaScript fornecido lança uma exceção não tratada, ' NULL ' é retornado. Se esse método for chamado após um evento NavigationStarting, o JavaScript fornecido será executado no novo documento quando ele for carregado, ao mesmo tempo em que ContentLoading é disparado. O ExecuteScriptAsync funcionará mesmo se IsScriptEnabled estiver definido como `FALSE` .

#### GetDevToolsProtocolEventReceiver 

Obtenha um receptor de evento de protocolo DevTools que permite que você se inscreva em um evento de protocolo DevTools.

> Public CoreWebView2DevToolsProtocolEventReceiver [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(cadeia de eventos de cadeia de caracteres)

Consulte o [Visualizador de protocolo devtools](https://aka.ms/DevToolsProtocolDocs) para obter uma lista e a descrição dos métodos disponíveis. O parâmetro methodName é o nome completo do método no formato `{domain}.{method}` . O parâmetro parametersAsJson é uma cadeia de caracteres JSON formatada que contém os parâmetros para o método correspondente. O método Invoke do manipulador será chamado quando o método for concluído de forma assíncrona. Invoke será chamado com o objeto Return do método como uma cadeia de caracteres JSON.

#### GoBack 

Navega o WebView para a página anterior no histórico de navegação.

> public void [(](#goback)) public void

#### GoForward 

Navega o WebView para a próxima página no histórico de navegação.

> public void [GoForward](#goforward)()

#### Navegar 

Fazer uma navegação do documento de nível superior para o URI especificado.

> [navegação](#navigate)void pública (URI da cadeia de caracteres)

Consulte os eventos de navegação para obter mais informações. Observe que isso iniciará uma navegação e o evento NavigationStarting correspondente será acionado algum tempo após a conclusão dessa chamada de navegação.

#### NavigateToString 

Inicia uma navegação para htmlContent como código-fonte HTML de um novo documento.

> public void [NavigateToString](#navigatetostring)(cadeia de caracteres htmlContent)

O parâmetro htmlContent não pode ter mais de 2 MB de caracteres. A origem da nova página será: em branco.

#### OpenDevToolsWindow 

Abre a janela do DevTools para o documento atual no WebView.

> public void [OpenDevToolsWindow](#opendevtoolswindow)()

Não faz nada se for chamado quando a janela do DevTools já estiver aberta.

#### PostWebMessageAsJson 

Postar a WebMessage especificada no documento de nível superior neste WebView.

> public void [PostWebMessageAsJson](#postwebmessageasjson)(cadeia de caracteres webMessageAsJson)

O evento Message da janela do documento de nível superior. Chrome. WebView será acionado. O JavaScript nesse documento pode assinar e cancelar a assinatura do evento por meio do seguinte:

```
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

Os argumentos do evento é uma instância de `MessageEvent` . A configuração CoreWebView2Settings. IsWebMessageEnabled deve ser true ou esse método irá falhar com E_INVALIDARG. A propriedade data do ARG do evento é o parâmetro da cadeia de caracteres WebMessage analisado como uma cadeia de caracteres JSON em um objeto JavaScript. A propriedade de origem do ARG do evento é uma referência ao `window.chrome.webview` objeto. Consulte SetWebMessageReceivedEventHandler para obter informações sobre como enviar mensagens do documento HTML no WebView para o host. Esta mensagem é enviada de forma assíncrona. Se ocorrer uma navegação antes que a mensagem seja postada na página, a mensagem não será enviada.

#### PostWebMessageAsString 

Isso é um auxiliar para postar uma mensagem que é uma cadeia de caracteres simples em vez de uma representação JSON de cadeia de caracteres de um objeto JavaScript.

> public void [PostWebMessageAsString](#postwebmessageasstring)(cadeia de caracteres webMessageAsString)

Isso se comporta exatamente da mesma maneira que PostWebMessageAsJson, mas a `window.chrome.webview` propriedade data do ARG (evento de mensagem) será uma cadeia de caracteres com o mesmo valor de webMessageAsString. Use isso em vez de PostWebMessageAsJson se você quiser se comunicar por cadeias de caracteres simples em vez de objetos JSON.

#### Recarregar 

Recarregar a página atual.

> recarregamento [Reload](#reload)nulo público ()

Isso é semelhante a navegar para o URI do documento de nível superior atual, incluindo todos os eventos de navegação que estão sendo acionados e como respeitar as entradas no cache HTTP. Mas o histórico de back/forward não será modificado.

#### RemoveHostObjectFromScript 

Remova o objeto host especificado pelo nome para que ele não fique mais acessível a partir do código JavaScript na WebView.

> public void [RemoveHostObjectFromScript](#removehostobjectfromscript)(nome da cadeia de caracteres)

Embora novas tentativas de acesso sejam negadas, se o objeto já for obtido por código JavaScript na WebView, o código JavaScript continuará a ter acesso a esse objeto. Chamar este método para um nome que já foi removido ou nunca adicionado falhará.

#### RemoveScriptToExecuteOnDocumentCreated 

Remova o JavaScript correspondente adicionado via AddScriptToExecuteOnDocumentCreated com a ID de script especificada.

> public void [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(ID da cadeia de caracteres)

#### RemoveWebResourceRequestedFilter 

Remove um filtro WebResource correspondente que foi adicionado anteriormente ao evento WebResourceRequested.

> public void [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(URI da cadeia de caracteres, [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) ResourceContext)

Se o mesmo filtro tiver sido adicionado várias vezes, será preciso removê-lo quantas vezes forem adicionadas para que a remoção seja efetiva. Retorna E_INVALIDARG para um filtro que nunca foi adicionado.

#### Parar 

Interrompa todas as navegações e buscas de recursos pendentes.

> [Stop](#stop)void Public ()

Não interrompe scripts.

