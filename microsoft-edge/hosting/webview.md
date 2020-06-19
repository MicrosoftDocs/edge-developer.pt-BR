---
description: Hospedar conteúdo da Web em seu aplicativo do Windows 10 com o controle WebView (EdgeHTML)
title: Microsoft Edge WebView para aplicativos do Windows 10
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: x-MS-WebView, MSHTMLWebViewElement, WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: aa9bef7bf214cf4f4ffdb4d68ad3a1a86ac2977b
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752203"
---
# WebView (EdgeHTML) para aplicativos do Windows 10  

[!INCLUDE [deprecation-note](./includes/deprecation-note.md)]  

O controle WebView (EdgeHTML) permite que você hospede conteúdo da Web em seu aplicativo do Windows 10.  

Você pode usá-lo como um elemento XAML (para aplicativos da [plataforma universal do Windows (UWP)](/uwp/api/Windows.UI.Xaml.Controls.WebView) e [aplicativos do Windows Forms e da área de trabalho do WPF](/windows/communitytoolkit/controls/wpf-winforms/webview)) ou um elemento HTML (x-MS-WebView)/Dom Object para aplicativos do Windows 10 baseados em JavaScript, conforme descrito aqui.  

|  |  |  
|:--- |:--- |  
| [**Eventos**](#events) | [departingFocus](#departingfocus), [MSWebViewContainsFullScreenElementChanged](#mswebviewcontainsfullscreenelementchanged), [MSWebViewContentLoading](#mswebviewcontentloading), [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded), [MSWebViewFrameContentLoading](#mswebviewframecontentloading), [MSWebViewFrameDOMContentLoaded](#mswebviewframedomcontentloaded), [MSWebViewFrameNavigationCompleted](#mswebviewframenavigationcompleted), [MSWebViewFrameNavigationStarting](#mswebviewframenavigationstarting), [MSWebViewLongRunningScriptDetected](#mswebviewlongrunningscriptdetected), [MSWebViewNavigationCompleted](#mswebviewnavigationcompleted), [MSWebViewNavigationStarting](#mswebviewnavigationstarting), [MSWebViewNewWindowRequested](#mswebviewnewwindowrequested), [MSWebViewPermissionRequested](#mswebviewpermissionrequested), [MSWebViewProcessExited](#mswebviewprocessexited), [MSWebViewWebResourceRequested](#mswebviewwebresourcerequested), [MSWebViewScriptNotify](#mswebviewscriptnotify), [MSWebViewUnsafeContentWarningDisplaying](#mswebviewunsafecontentwarningdisplaying), [MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsupportedurischemeidentified), [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified) |  
| [**Métodos**](#methods) | [addWebAllowedObject](#addweballowedobject), [buildlocalStreamUri](#buildlocalstreamuri), [capturePreviewToBlobAsync](#capturepreviewtoblobasync), [captureSelectedContentToDataPackageAsync](#captureselectedcontenttodatapackageasync), [invokeScriptAsync](#invokescriptasync), [getDeferredPermissionRequests](#getdeferredpermissionrequests), [getDeferredPermissionRequestById](#getdeferredpermissionrequestbyid), [goBack](#goback), [goForward](#goforward), [navegar](#navigate), [navigateFocus](#navigatefocus), [navigateTolocalStreamUri](#navigatetolocalstreamuri), [navigateToString](#navigatetostring), [navigateWithHttpRequestMessage](#navigatewithhttprequestmessage), [Atualizar](#refresh), [parar](#stop) |  
| [**Propriedades**](#properties) | [CanGoBack](#cangoback), [canGoForward](#cangoforward), [containsFullScreenElement](#containsfullscreenelement), [DocumentTitle](#documenttitle), [Height](#height), [process](#process), [Settings](#settings), [src](#src), [Width](#width) |  

## Sintaxe  

```javascript
// Feature detect for webview support
if (MSHTMLWebViewElement) {
    let wv = document.createElement('x-ms-webview'); // Use CSS to set width, height and other styles
    wv.navigate("https://www.example.com");
    document.body.appendChild(wv);
}
```  

## Comentários  

### WebView versus iframe  

Como um elemento HTML [iframe](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) padrão, você pode usar o WebView para carregar páginas remotas por http e páginas locais (*MS-Appx-Web:///*) do pacote do aplicativo.  No entanto, o WebView também pode:  

*   Carregar páginas e recursos de suas pastas [ApplicationData](/uwp/api/Windows.Storage.ApplicationData) (locais, móveis, Temp) (*MS-AppData:///*) e [fluxos de memória](/microsoft-edge/hosting/webview#buildlocalstreamuri) (*MS-local-Stream:///*)  
*   Fornecer controles semelhantes a navegadores: para [voltar](#goback) e [Avançar](#goforward) no histórico de navegação, e [parando](#stop) ou [atualizando](#refresh) a página atual.  
*   [Capture capturas de tela do conteúdo da Web](#capturepreviewtoblobasync) tornando mais fácil implementar o contrato de [compartilhamento](/windows/uwp/app-to-app/share-data) de aplicativos do Windows 10.  
*   Permita que o código JavaScript em execução em um WebView aumente eventos personalizados ([MSWebViewScriptNotify](#mswebviewscriptnotify)) para o aplicativo e permita que o aplicativo execute JavaScript dentro do WebView ([invokeScriptAsync](#invokescriptasync)).  
*   Forneça eventos de conteúdo do WebView finos.  
    
    | Evento DOM do WebView | Descrição |  
    |:--- |:--- |  
    | [MSWebViewNavigationStarting](#mswebviewnavigationstarting) | Indica que o WebView está começando a navegar.  |  
    | [MSWebViewContentLoading](#mswebviewcontentloading) | O conteúdo HTML é baixado e está sendo carregado no controle.  |  
    | [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded) | Indica que os principais elementos DOM terminaram de carregar.  |  
    | [MSWebViewNavigationCompleted](#mswebviewnavigationcompleted) | Indica a conclusão da navegação e todos os elementos de mídia são renderizados.  |  
    | [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified) | O WebView encontrou o conteúdo não era HTML.  |  
    | [UnsafeContentWarningDisplaying](#mswebviewunsafecontentwarningdisplaying) | O WebView mostra uma página de aviso para o conteúdo que foi relatado como não seguro pelo *Filtro SmartScreen*do Windows.  |  
    
    ... incluindo [eventos](#events) correspondentes para conteúdo iframe carregado em um WebView (como [MSWebView**frame**NavigationStarting](#mswebviewframenavigationstarting) e assim por diante). 

### Impressão  

Quando um aplicativo do Windows que usa JavaScript é impresso, as `<x-ms-webview>` marcas são transformadas em `<iframe>` marcas antes da impressão.  Além da diferença normal entre exibir na tela e renderizado para impressão, estilos CSS aplicados a `<iframe>` elementos são, então, aplicáveis à `<iframe>` transformada de `<x-ms-webview>` .  

### Trabalhadores do serviço  

Começando com a [atualização do Windows 10 de outubro de 2018](/windows/uwp/whats-new/windows-10-build-17763) (EdgeHTML 18), [os funcionários de serviço são compatíveis com o controle WebView](/microsoft-edge/dev-guide#service-workers) (além do navegador Microsoft Edge e aplicativos do Windows 10 com JavaScript).  

as arquiteturas de aplicativos x64 exigem pacotes neutros (qualquer CPU) ou x64, pois os operadores de serviço não são compatíveis com processos WoW64.  (Para conservar espaço em disco, a versão WoW das DLLs necessárias não está incluída nativamente no Windows.)  

### Modelo de threading e confiabilidade  

A criação de uma WebView via `document.createElement("x-ms-webview")` ou via `<x-ms-webview>` marcação cria uma WebView em um novo thread exclusivo no processo do aplicativo.  Executar em um novo thread exclusivo significa que o script de execução longa de um WebView não pode travar o aplicativo ou outros modos de exibição da Web.  Criar uma WebView por meio do `new MSWebView()` construtor cria uma WebView em um processo da WebView separado.  Executar em um processo exclusivo significa que, além da proteção de um script de execução longa, o aplicativo também é protegido do conteúdo da Web que falha no processo da WebView.  Criar uma WebView pelo [`MSWebViewProcess.createWebViewAsync`](./webview/MSWebViewProcess.md#createwebviewasync) método também cria uma WebView em um processo separado, mas permite que o chamador controle mais sobre configurações de processo e agrupamentos de Webviews em processos WebView.  Consulte `MSWebViewProcess` para mais informações.  

### Acesso à API do WinRT  

Um aplicativo UWP pode permitir que documentos HTML dentro de webviews tenham acesso a APIs do WinRT.  Isso ocorre por meio do atributo WindowsRuntimeAccess dos elementos filho da regra do elemento ApplicationContentUriRules do AppxManifest.xml do aplicativo UWP.  Defina WindowsRuntimeAccess como ' all' e documentos HTML com URIs correspondentes poderão usar o WinRT.  Isso é o mesmo que fornecer acesso ao WinRT para conteúdo HTML em aplicativos UWP JavaScript, portanto, consulte [chamar APIs do winrt a partir do seu PWA](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#call-winrt-apis-from-your-pwa) para obter mais informações.  

APIs do WinRT relacionadas à interface do usuário podem não funcionar quando chamadas de um WebView executando em seu próprio thread, mas podem funcionar quando são chamadas de um WebView em execução em um processo do WebView separado.  Ao usar um WebView em seu próprio thread exclusivo, esse thread não é o thread de exibição do aplicativo.  Algumas APIs do WinRT relacionadas à interface do usuário precisam ser chamadas do thread de exibição do aplicativo.  Os webviews criados em um processo da WebView separado são executados em um thread de exibição e, portanto, não devem ter as mesmas restrições da execução do WebView em seu próprio thread exclusivo.  Se você tiver problemas com APIs do WinRT relacionadas à interface do usuário em uma WebView, verifique se está usando uma WebView em seu próprio processo WebView, conforme descrito acima.  

### Limitações de armazenamento do AppCache  

Os aplicativos que usam o suporte a JavaScript da API de cache do aplicativo (ou AppCache), conforme definido na [especificação do HTML5](https://go.microsoft.com/fwlink/p/?LinkId=228542), para criar aplicativos Web offline devem observar as limitações de armazenamento disponíveis.  Isso é especialmente verdadeiro em dispositivos com espaço limitado de memória.  Os limites práticos do tamanho do AppCache são sempre uma função do espaço de armazenamento em disco disponível.  As diretrizes gerais são mostradas abaixo.  

| Tamanho do volume |AppCache por domínio | AppCache por usuário |  
|:--- |:--- |:--- |  
| Até 4 GB | 10MB | 50 MB |  
| 4 GB para 16 GB | 50 MB | 500MB |  
| de 16 GB a 32 GB | 50 MB | 1 GB |  

Todos os aplicativos do Windows10 devem usar o mesmo modelo de cota AppCache, portanto, a limitação de armazenamento em disco disponível se aplica aos aplicativos de área de trabalho e de telefone.  O limite do é também um difícil depois das páginas carregadas dentro do **WebView** , consumindo 1 GB de espaço *AppCache* ; solicitações para armazenamento adicional do *AppCache* acima desse limite serão negadas.  

Para obter mais informações, consulte o [exemplo de controle HTML WebView](https://go.microsoft.com/fwlink/p/?linkid=309825) e o JSBrowser a documentação do [controle WebView](https://github.com/MicrosoftEdge/JSBrowser#harnessing-the-webview-control) .  

## Eventos  

### departingFocus  

Indica a deaplicação de foco do **WebView** no aplicativo.  Acionado quando a janela de chamadas do documento de nível superior da WebView. departFocus.  Os args FocusNavigationEvent no evento departingFocus correspondem aos parâmetros fornecidos para departFocus, exceto os parâmetros de origem são convertidos do espaço de coordenadas de document's da WebView para o espaço de coordenadas do documento do host de WebView.  Consulte o método WebView. navigateFocus e o evento navigatingFocus de janela correspondente para transferir o foco do host para o WebView.  Consulte a [biblioteca de navegação de direção do TVJS](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) para obter um exemplo de implementação de navegação de foco via teclado ou gamepad que manipula esse evento.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("departingFocus", handler);
webview.removeEventListener("departingFocus", handler);
```  

#### Informações do evento  

|            |      |  
|:--- |:--- |  
| **Interface** | [FocusNavigationEvent](./webview/FocusNavigationEvent.md) |  
| **Síncrono** | Sim |   
| **Bolhas** | Sim |  
| **Cela** | Não |  

### MSWebViewContainsFullScreenElementChanged  

Ocorre quando o status muda ou não **no momento se** contém um elemento de tela inteira.  Use a propriedade containsFullScreenElement para o valor atual.  Aqui, o elemento de tela inteira refere-se à noção de [APIs do dom](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) de tela inteira por meio das funções dom Element. requestFullScreen e Document. exitFullScreen.  

```javascript
function containsFullScreenElementChangedHandler(eventInfo) {
    const applicationView = Windows.UI.ViewManagement.ApplicationView.getForCurrentView();
    if (webview.containsFullScreenElement) {
        webview.classList.add("fullscreen"); // Have the webview fill the app view
        applicationView.tryEnterFullScreenMode(); // Have the app view fill the screen
    }
    else {
        webview.classList.remove("fullscreen"); // Return webview to normal
        applicationView.exitFullScreenMode(); // Return app view to normal
    }
}

// addEventListener syntax
webview.addEventListener("MSWebViewContainsFullScreenElementChanged", containsFullScreenElementChangedHandler);
webview.removeEventListener("MSWebViewContainsFullScreenElementChanged", containsFullScreenElementChangedHandler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | **Evento** |  
| **Síncrono** | Sim |  
| **Bolhas** | Não |   
| **Cela** | Não |  

### MSWebViewContentLoading  

Indica que o conteúdo HTML é baixado e está sendo carregado no controle.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewContentLoading", handler);
webview.removeEventListener("MSWebViewContentLoading", handler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Síncrono** | Sim  |  
| **Bolhas** | Não |   
| **Cela** | Não |  

### MSWebViewDOMContentLoaded  

Indica que os principais elementos DOM terminaram de carregar.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewDOMContentLoaded", handler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Síncrono** |Sim |  
| **Bolhas** | Não |  
| **Cela** | Não |   

### MSWebViewFrameContentLoading  

Indica que o conteúdo HTML foi baixado e está sendo carregado no `<iframe>` controle.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameContentLoading", handler);
webview.removeEventListener("MSWebViewFrameContentLoading", handler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Síncrono** | Sim |  
| **Bolhas** | Não |  
| **Cela** | Não |   

### MSWebViewFrameDOMContentLoaded  

Indica que os principais elementos DOM terminaram de carregar no `<iframe>` .  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewFrameDOMContentLoaded", handler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Síncrono** | Sim |  
| **Bolhas** | Não |   
| **Cela** | Não |  

### MSWebViewFrameNavigationCompleted  

Indica a conclusão da navegação, e todos os elementos de mídia são renderizados no `<iframe>` .  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationCompleted", handler);
webview.removeEventListener("MSWebViewFrameNavigationCompleted", handler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | [NavigationCompletedEvent](./webview/NavigationCompletedEvent.md) |  
| **Síncrono** | Sim |  
| **Bolhas** | Não |   
| **Cela** | Não |  

### MSWebViewFrameNavigationStarting  

Indica `<iframe>` que a em um **WebView** está começando a navegar.  Isso é acionado antes da obtenção de recursos da rede para a navegação.  A navegação não é iniciada até que todos os manipuladores de eventos MSWebViewFrameNavigationStarting sejam concluídos.  Esse evento é cancelável pela chamada `eventArgs.preventDefault()` .  Se for cancelado, o WebView não executará a navegação.  

```javascript
function frameNavigationStartingHandler(navigationEventArgs) {
    // Cancel all navigations that don't meet some criteria.
    if (!navigationEventArgs.uri.startsWith("https://example.com/")) {
        navigationEventArgs.preventDefault();
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationStarting", frameNavigationStartingHandler);
webview.removeEventListener("MSWebViewFrameNavigationStarting", frameNavigationStartingHandler);
```  

#### Informações do evento  

|  |  |
|:--- |:--- |  
| **Interface** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Síncrono** | Sim |  
| **Bolhas** |Não |   
| **Cela** | Sim |  

### MSWebViewLongRunningScriptDetected  

Ocorre periodicamente durante a execução ininterrupta do script no **WebView**, permitindo que você pare o script.  

```javascript
function handler(eventInfo) {
    const stopPageScriptThreshold = 5 * 1000;
    if (eventInfo.executionTime > stopPageScriptThreshold) {
        eventInfo.stopPageScriptExecution = true; // Stop the long running script if it goes over our threshold
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewLongRunningScriptDetected", handler);
webview.removeEventListener("MSWebViewLongRunningScriptDetected", handler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | [LongRunningScriptDetectedEvent](./webview/LongRunningScriptDetectedEvent.md) |  
| **Síncrono** | Sim |  
| **Bolhas** | Não |  
| **Cela** | Não |  

### MSWebViewNavigationCompleted  

Indica a conclusão da navegação, e todos os elementos de mídia são renderizados ou ocorreu um erro de navegação.  Verifique a Propriedade IsSuccess do Event args para saber se a navegação foi bem-sucedida e a propriedade webErrorStatus para obter detalhes sobre o erro de navegação.  Erros de navegação podem ocorrer antes de obter qualquer conteúdo da rede por exemplo se o nome do host de um URI não resolver, caso contrário, o evento MSWebViewNavigationStarted será acionado seguido pelo evento MSWebViewNavigationCompleted.  Erros de navegação também podem ocorrer após receber uma página de erro de um servidor Web, por exemplo, uma página do 404 de um servidor HTTP, nesse caso, todos os eventos de navegação serão acionados, MSWebViewNavigationStarting, MSWebViewContentLoading, MSWebViewDOMContentLoaded e MSWebViewNavigationCompleted.  Para fornecer uma página de erro de navegação do aplicativo para casos em que o servidor Web não forneceu uma página de erro, você precisará verificar se o MSWebViewContentLoading não foi disparado para uma navegação inexistente que indica que não há uma página de erro do servidor fornecida.  

```javascript
let hasContent = false;
webview.addEventListener("MSWebViewNavigationStarting", () => { hasContent = false; });
webview.addEventListener("MSWebViewContentLoading", () => { hasContent = true; });

webview.addEventListener("MSWebViewNavigationCompleted", navigationCompletedEventArgs => {
    // Navigation failures may or may not come after getting an error page from the web server.
    // We keep track of the ContentLoading event with hasContent to tell if we have an error page from the server.
    // So we only navigate to our app error page when there's no server provided error page.
    if (!navigationCompletedEventArgs.isSuccess && !hasContent) {
        // Pass our failed URI and error details in the query and the error page script can read it as appropriate.
        webview.navigate("ms-appx-web:///appErrorPage.html?" + 
            "uri=" + encodeURIComponent(navigationCompletedEventArgs.uri) + "&" +
            "webErrorStatus=" + encodeURIComponent(navigationCompletedEventArgs.webErrorStatus));
    }
});
 
// addEventListener syntax
webview.addEventListener("MSWebViewNavigationCompleted", handler);
webview.removeEventListener("MSWebViewNavigationCompleted", handler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | [NavigationCompletedEvent](./webview/NavigationCompletedEvent.md) |  
| **Síncrono** | Sim |  
| **Bolhas** | Não |   
| **Cela** | Não |  

### MSWebViewNavigationStarting  

Indica que o **WebView** está começando a navegar.  Isso é acionado antes da obtenção de recursos da rede para a navegação.  A navegação não é iniciada até que todos os manipuladores de eventos MSWebViewNavigationStarting sejam concluídos.  Esse evento é cancelável pela chamada `eventArgs.preventDefault()` .  Se for cancelado, o WebView não executará a navegação.  

```javascript
function navigationStartingHandler(navigationEventArgs) {
    // Cancel all navigations that don't meet some criteria.
    if (!navigationEventArgs.uri.startsWith("https://example.com/")) {
        navigationEventArgs.preventDefault();
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewNavigationStarting", navigationStartingHandler);
webview.removeEventListener("MSWebViewNavigationStarting", navigationStartingHandler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Síncrono** | Não |  
| **Bolhas** | Sim |   
| **Cela** | Sim |  

### MSWebViewNewWindowRequested  

Gerado quando o conteúdo no **WebView** está tentando abrir uma nova janela.  Se o evento não for cancelado, o WebView iniciará o URI da nova solicitação de janela no navegador padrão do usuário.  

```javascript
function handler(eventInfo) {
    // Prevent the webview from opening URIs in the default browser.
    eventInfo.preventDefault();
    
    // Only allow https://example.com/ to open new windows.
    if (eventInfo.referer === "https://example.com/") {
        // Perform some custom handling of the URI.
        openUri(eventInfo.uri);
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewNewWindowRequested", handler);
webview.removeEventListener("MSWebViewNewWindowRequested", handler);
```  

#### Informações do evento  

|  |  |  
|:---|:--- |  
| **Interface** | [NavigationEventWithReferrer](./webview/NavigationEventWithReferrer.md) |  
| **Síncrono** | Sim |  
| **Bolhas** | Não |  
| **Cela** | Sim |  

### MSWebViewPermissionRequested  

Indica que o conteúdo na **WebView** está tentando acessar a funcionalidade (como geolocalização ou acesso de bloqueio de ponteiro) que normalmente exige permissões de usuário final.  Se nenhum manipulador de eventos estiver registrado ou se o manipulador de eventos não chamar eventArgs. permissionRequest. Allow (), Defer () ou Deny (), por padrão, a solicitação de permissão será negada.  Se você precisar decidir se a permissão é permitida ou negada de forma assíncrona, por exemplo, se você precisar solicitar o usuário, use eventArgs. permissionRequest. Defer ().  A solicitação de permissão será adiada até você usar WebView. getDeferredPermissionRequestById ou WebView. getDeferredPermissionRequests e chamar Allow () ou Deny () no DeferredPermissionRequest com o valor de ID correspondente.  

```javascript
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    switch (permissionRequest.type) {
        case "geolocation":
        case "media":
        case "pointerlock":
        case "webnotifications":
        case "screen":
        case "immersiveview":
            if (permissionRequest.uri.startsWith("https://www.example.com/")) {
                // Implicitly trust particular URI
                permissionRequest.allow();
            }
            else if (permissionRequest.uri.startsWith("https://")) {
                // Defer the request so we can ask the user to allow or deny the request
                permissionRequest.defer();
                // Later we'll need to use webview.getDeferredPermissionRequestById for this
                // request and call allow or deny.
                promptUserForDeferredPermissionRequest(
                    permissionRequest.id,
                    permissionRequest.uri,
                    permissionRequest.type);
            }
            else {
                // Implicitly deny non-https URIs
                permissionRequest.deny();
            }
            break;

        case "unlimitedIndexedDBQuota":
        default:
            permissionRequest.deny();
            break;
    }
});

// addEventListener syntax
webview.addEventListener("MSWebViewPermissionRequested", handler);
webview.removeEventListener("MSWebViewPermissionRequested", handler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | [PermissionRequestedEvent](./webview/PermissionRequestedEvent.md) |  
| **Síncrono** | Sim |  
| **Bolhas** | Não |   
| **Cela** | Não |  

### MSWebViewProcessExited  

Indica que o processo de componente da **WebView** travou.  Isso só é relevante para um WebView fora do processo.  Consulte a seção de comentários sobre como criar uma WebView fora do processo, em oposição a uma WebView em processo.  Depois que esse evento é acionado, o WebView correspondente é colocado em um estado de falha.  Chamar a maioria dos métodos específicos do WebView ou acessar a maioria das propriedades específicas do WebView em uma WebView travada gerará uma exceção.  Para recuperar esse evento, remova o WebView travado do DOM e substitua-o por um novo WebView.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewProcessExited", handler);
webview.removeEventListener("MSWebViewProcessExited", handler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | **Evento** |  
| **Síncrono** | Sim |  
| **Bolhas** | Não |   
| **Cela** | Não |  

### MSWebViewWebResourceRequested  

Gerado quando uma página dentro do elemento **WebView** solicita um recurso.  

```javascript
// A handler that completes synchronously with a custom HTTP response built from a string.
function handlerWithSyncString(webResourceRequestedEventArgs) {
    // Only provide custom HTTP responses for particular HTTP requests
    if (webResourceRequestedEventArgs.args.request.requestUri.absoluteUri === "https://www.bing.com/") {
        const Http = Windows.Web.Http;
        // Create the custom response using a string
        webResourceRequestedEventArgs.args.response = new Http.HttpResponseMessage(Http.HttpStatusCode.ok);
        webResourceRequestedEventArgs.args.response.content = new Http.HttpStringContent("<H1>Example</H1>");
    }
});

// A more complicated handler that completes asynchronously with a custom HTTP response built from a stream.
function handlerWithAsyncStream(webResourceRequestedEventArgs) {
    // Only provide custom HTTP responses for particular HTTP requests
    if (webResourceRequestedEventArgs.args.request.requestUri.absoluteUri === "https://www.bing.com/") {
        // Take a deferral on the WebResourceRequested event so that we can create the custom HTTP response asynchronously.
        const deferral = webResourceRequestedEventArgs.args.getDeferral();

        // Use fetch to get a Blob of the content of the URI
        fetch("ms-appx:///replacement.html").then(fetchResponse => {
            return fetchResponse.blob();
        }).then(fetchResponseBlob => {
            const Http = Windows.Web.Http;
            webResourceRequestedEventArgs.args.response = new Http.HttpResponseMessage(
                Http.HttpStatusCode.ok);

            // Use Blob.msDetachStream to convert the Blob to a Windows.Storage.Streams.IInputStream
            webResourceRequestedEventArgs.args.response.content = new Http.HttpStreamContent(
                fetchResponseBlob.msDetachStream());

        }).finally(() => {
            // Use a finally call to complete the deferral so even if there is an error we will unblock the event.
            deferral.complete();
        });
    }
});
 
// addEventListener syntax
webview.addEventListener("MSWebViewWebResourceRequested", handler);
webview.removeEventListener("MSWebViewWebResourceRequested", handler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | [WebResourceRequestedEvent](./webview/WebResourceRequestedEvent.md) |  
| **Síncrono** | Sim |  
| **Bolhas** | Não |   
| **Cela** | Não |  


### MSWebViewScriptNotify  

Gerado quando uma página dentro do elemento **WebView** chama o método **Window. external. Notify** .  O método window. external. Notify só está disponível para documentos com URIs que correspondam às regras no ApplicationContentUriRules de manifest's do aplicativo ou que tenha sido programaticamente permitido por meio da configuração de WebView. Settings. isScriptNotifyAllowed para true.  Além disso, Window. external. Notify só está disponível para o documento de nível superior da WebView.  

```javascript
webview.addEventListener("MSWebViewScriptNotify", eventInfo => {
    console.log("The URI " + eventInfo.callingUri + 
        " has sent notification " + eventInfo.value);
});

// Allow the next URI to which we navigate access to window.external.notify
webview.settings.isScriptNotifyAllowed = true;
webview.navigate("https://example.com/");

webview.addEventListener("MSWebViewNavigationCompleted", () => {
    // Inject script to the webview that will send a notification back.
    const asyncOp = webview.invokeScriptAsync("eval", "window.external.notify('example notification')");
    asyncOp.start();
});
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | [ScriptNotifyEvent](./webview/ScriptNotifyEvent.md) |  
| **Síncrono** | Sim |  
| **Bolhas** | Não |  
| **Cela** | Não |  

### MSWebViewUnsafeContentWarningDisplaying  

Ocorre quando o **WebView** mostra uma página de aviso para o conteúdo que foi relatado como não seguro pelo filtro do SmartScreen.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
webview.removeEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | **Evento** |  
| **Síncrono** |Sim |  
| **Bolhas** |Não |   
| **Cela** |Não |  

### MSWebViewUnsupportedUriSchemeIdentified  

Gerado quando há navegação para um URI (Uniform Resource Identifier) que o **WebView** não suporta.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
webview.removeEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Síncrono** | Sim |  
| **Bolhas** | Não |  
| **Cela** | Sim |  

### MSWebViewUnviewableContentIdentified  

Gerado quando o **WebView** tenta navegar para conteúdo da Web com um tipo de conteúdo sem suporte.  Por exemplo, os PDFs atualmente não são compatíveis com a WebView e as navegações para documentos PDF não navegam e, em vez disso, geram esse evento.  

```javascript
function handler(args) {
    if (args.mediaType === "application/pdf") {
        Windows.System.Launcher.launchUriAsync(new Windows.Foundation.Uri(args.uri));
    }
}

// addEventListener syntax
webview.addEventListener("MSWebViewUnviewableContentIdentified", handler);
webview.removeEventListener("MSWebViewUnviewableContentIdentified", handler);
```  

#### Informações do evento  

|  |  |  
|:--- |:--- |  
| **Interface** | [UnviewableContentIdentifiedEvent](./webview/UnviewableContentIdentifiedEvent.md) |  
| **Síncrono** | Sim |  
| **Bolhas** | Não |   
| **Cela** | Não |  

## Métodos  

### addWebAllowedObject  

Adiciona um objeto do Windows Runtime nativo como um parâmetro global para o documento de nível superior dentro de um **WebView**.  

O objeto não é injetado no documento atual, mas sim o próximo documento de nível superior ao qual a WebView navega.  O objeto é injetado antes que qualquer script do documento HTML seja executado para que você possa confiar no objeto no script global do seu documento.  

Você deve usar addWebAllowedObject tanto durante um evento MSWebViewNavigationStarting ou antes de chamar explicitamente um método Navigate.  Nesses casos, o objeto é injetado no documento da navegação correspondente.  Chamando-o em outro contexto, você não tem uma maneira de ter certeza de que documento vai injetar o objeto.  

Chamar addWebAllowedObject várias vezes em uma linha injetará vários objetos no documento.  Se você chamá-lo antes de uma chamada de navegação explícita e, em seguida, novamente durante o evento MSWebViewNavigationStarting correspondente, as duas chamadas serão bem-sucedidas e você terá vários objetos injetados.  Se você chamar várias vezes com o mesmo parâmetro Name, a última chamada WINS e as chamadas anteriores com esse nome serão ignoradas.  

Se uma navegação falha ou é redirecionada, as chamadas addWebAllowedObject para essa navegação são ignoradas.  Se desejar manipular redirecionamentos, você pode assinar a inspeção de eventos MSWebViewNavigationStarting para redirecionar e chamar addWebAllowedObject novamente de acordo com qualquer critério apropriado para o seu aplicativo.  Da mesma forma, quando um documento é acessado por todos os objetos injetados por meio do addWebAllowedObject para que o documento não seja transferido para o próximo documento, você precisará chamar explicitamente addWebAllowedObject se quiser que eles continuem.  

Se você chamar addWebAllowedObject para um documento que ainda não tem acesso ao WinRT, ou se tiver [acesso do AllowForWebOnly via ApplicationContentUriRules](/uwp/schemas/appxpackage/uapmanifestschema/element-uap-rule) , o objeto só será injetado se o objeto tiver o atributo Windows. Foundation. Metadata. AllowForWeb Metadata.  Caso contrário, a injeção falhará e um erro será relatado ao console do desenvolvedor do JavaScript.  Se chamado em um documento com acesso completo ao WinRT, o objeto será injetado independentemente do atributo AllowForWeb.  

Além disso, o objeto deve implementar a interface IAgileObject.  Isso ocorre porque os elementos XAML e HTML da WebView executados em seus threads de exibição do aplicativo do ASTA e o thread JavaScript da WebView são um thread ASTA diferente e queremos incentivar os desenvolvedores de aplicativos a garantir que o objeto possa ser executado no thread JavaScript sem bloquear o thread de exibição do aplicativo, se possível.  

O parâmetro Name deve ser um nome de propriedade JavaScript válido, caso contrário, a chamada falhará silenciosamente.  Se o nome for de uma propriedade que já existe no objeto global, essa propriedade será sobrescrita se a propriedade for configurável.  As propriedades não configuráveis no objeto global não são sobrescritas e a chamada addWebAllowedObject falha silenciosamente.  As propriedades de JavaScript criadas via addWebAllowedObject são graváveis, configuráveis e enumeráveis.  

```javascript
let name = "exampleProperty";
webview.addWebAllowedObject(name, applicationObject);
webview.navigate("https://example.com/"); // applicationObject will be available as window.exampleProperty on https://example.com
```  

#### Parâmetros  

*name*  

*   Tipo: **cadeia de caracteres**  
*   O nome do objeto que será exposto ao documento no **WebView**.  

*applicationObject*  

*   Tipo: **objeto**  
*   O objeto a ser exposto ao documento no **WebView**.  

#### Valor de retorno  

Esse método não retorna um valor.  

#### Recursos e requisitos adicionais  

|  |  |  
|:--- |:--- |  
| **Mínimo de cliente com suporte** | Windows10 (somente aplicativos da Windows Store) |    
| **Servidor mínimo com suporte** | Nenhum compatível |   
| **Número mínimo com suporte** | Nenhum compatível |  

### buildLocalStreamUri  

Cria um URI que você pode passar para [navigateToLocalStreamUri](#methods).  

```javascript
var string = webview.buildLocalStreamUri(contentIdentifier, relativePath);
```  

#### Parâmetros  

*contentIdentifier*  

*   Tipo: **cadeia de caracteres**  
*   Um identificador exclusivo para o conteúdo ao qual o URI faz referência.  Isso define a raiz do URI.  

*relativePath*  

*  Tipo: **cadeia de caracteres**  
*  O caminho do recurso, relativo à raiz.  

#### Valor de retorno  

Tipo: **cadeia de caracteres**  

O URI criado combinando e normalizando o *contentIdentifier* e o *RelativePath*.  

#### Exemplo  

O exemplo a seguir ilustra um caso de uso típico.  

```javascript
var webview = document.createElement("x-ms-webview"); //Instantiate the webview element
var localStreamUri = webview.buildLocalStreamUri(contentIdentifier, relativePath); //Create URI to pass to navigateToLocalStreamUri method
webview.navigateToLocalStreamUri(localStreamUri, streamResolver); //Load the local web content 
```  

### capturePreviewToBlobAsync  

Cria uma imagem do [elemento WebView](./webview.md) atual e a escreve no elemento Image especificado.  

```javascript
var capturePreviewToBlobAsync = webview.capturePreviewToBlobAsync();
```  

#### Parâmetros  

Esse método não tem parâmetros.  

#### Valor de retorno  

Tipo: **MSWebViewAsyncOperation**  

Um objeto **MSWebViewAsyncOperation** que, quando concluído, fornece um objeto **blob** que contém a imagem.  Ao usar **capturePreviewToBlobAsync**, você precisa definir manipuladores de êxito e erros após definir a operação.  Após a aplicação dos manipuladores de eventos, chame o método Start no objeto [MSWebViewAsyncOperation](./webview/MSWebViewAsyncOperation.md) para executar a operação.  

### captureSelectedContentToDataPackageAsync  

> [!IMPORTANT]
> Esse método foi preterido e tem um problema conhecido.  Evite usar esse método em seu código de produção.  

Assincronamente Obtém um [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) que contém o conteúdo selecionado no **WebView**.  

```javascript
var msWebViewAsyncOperation = webview.captureSelectedContentToDataPackageAsync();
```  

#### Parâmetros  

Esse método não tem parâmetros.  

#### Valor de retorno  

Tipo: **MSWebViewAsyncOperation**  

Um objeto **MSWebViewAsyncOperation** que, quando concluído, fornece um objeto [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) que contém a imagem.  Ao usar **captureSelectedContentToDataPackageAsync**, você precisa definir manipuladores de êxito e erros após definir a operação.  Após a aplicação dos manipuladores de eventos, chame o método Start no objeto MSWebViewAsyncOperation para executar a operação.  

```javascript
 var operation = webview.captureSelectedContentToDataPackageAsync();
    operation.oncomplete = function () {
        // operation.result is a package object that contains the selected data.
        var url = URL.createObjectURL(operation.result, { oneTimeOnly: true });
        // After converting the package to a URI, put it in an image element.
        document.getElementById('webviewPreview').src = url;
    };
    operation.start();
```  

### invokeScriptAsync  

Como uma ação assíncrona, executa a função de script especificada do HTML atualmente carregado, com argumentos específicos.  

```javascript
webview.invokeScriptAsync(functionName, ...args)
```  

#### Parâmetros  

**função FunctionName**  

*   Tipo: **cadeia de caracteres**  
*   O nome da função a ser invocada.  Esse é um nome de propriedade no objeto da janela global do documento de nível superior da WebView.  Pode ser uma função global interna, como eval ou Open, ou pode ser uma função definida pelo script no objeto da janela global.  Somente funções no documento de nível superior do WebView podem ser invocadas.  

**args**  

*   Tipo: **cadeia de caracteres**  
*   Parâmetros de cadeia de caracteres opcionais para passar para a função invocada.  Após FunctionName, os parâmetros adicionais para invokeScriptAsync são cadeias de caracteres transferidas para a função invocada.  

#### Valor de retorno  

Tipo: **MSWebViewAsyncOperation**  

Ao usar **invokeScriptAsync**, você precisa definir manipuladores de êxito e erros após definir a operação.  Após a aplicação dos manipuladores de eventos, chame **MSWebViewAsyncOperation. Start** para executar a operação.  Se o evento complete MSWebViewAsyncOperation for acionado, a propriedade Result do MSWebViewAsyncOperation será o valor de retorno da cadeia de caracteres para invocar a função.  Usar o valor de retorno da função invocada permite que o conteúdo da WebView faça a comunicação de modo síncrono para o host da WebView.  Para fazer com que o conteúdo da WebView se comunique de forma assíncrona ao host da WebView, consulte o evento MSWebViewScriptNotify.  Se a função invocada lançar uma exceção não tratada, o evento de erro do MSWebViewAsyncOperation será acionado.  

```javascript
const functionName = "eval";
const args = ["'Current URL: ' + document.location.href"];

const asyncOp = webview.invokeScriptAsync(functionName, ...args);

asyncOp.onerror = () => console.error("Error: " + asyncOp.error);
asyncOp.oncomplete = () => console.log("Result: " + asyncOp.result); // Logs 'Current URL: about:blank'
asyncOp.start();
```  

### getDeferredPermissionRequests  

Retorna uma lista de solicitações de permissão adiadas emitidas pelo conteúdo no controle **WebView** .  

```javascript
var sequence<PermissionRequest> = x-ms-webview.getDeferredPermissionRequests();
```  

#### Parâmetros  

Esse método não tem parâmetros.  

#### Valor de retorno  

Tipo: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)  

A solicitação de permissão adiada especificada.  

#### Recursos e requisitos adicionais  

|  | |  
|:--- |:--- |  
| **Mínimo de cliente com suporte** | Windows10 (somente aplicativos da Windows Store) |  
| **Servidor mínimo com suporte** | Nenhum compatível |  
| **Número mínimo com suporte** | Nenhum compatível |  


### getDeferredPermissionRequestById  

Retorna a solicitação de permissão adiada especificada.  

```javascript
var deferredPermissionRequest = x-ms-webview.getDeferredPermissionRequestById(id);
```  

#### Parâmetros  

*id*  

*   Tipo: **unsigned long**  
*   A ID da solicitação de permissão adiada que você deseja obter.  

#### Valor de retorno  

Tipo: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)  

A solicitação de permissão adiada especificada.  

#### Recursos e requisitos adicionais  

|  |  |  
|:--- |:--- |  
| **Mínimo de cliente com suporte** | Windows10 (somente aplicativos da Windows Store) |  
| **Servidor mínimo com suporte** | Nenhum compatível |  
| **Número mínimo com suporte** | Nenhum compatível |  

### goBack  

Navega o **WebView** para a página anterior no histórico de navegação.  

```javascript
webview.goBack();
```  

#### Parâmetros  

Esse método não tem parâmetros.  

#### Valor de retorno  

Esse método não retorna um valor.  

### goForward  

Navega o **WebView** para a próxima página no histórico de navegação.  

```javascript
webview.goForward();
```  

#### Parâmetros  

Esse método não tem parâmetros.  

#### Valor de retorno  

Esse método não retorna um valor.  

### navegar  

Carrega o conteúdo HTML no URI (Uniform Resource Identifier) especificado.  

```javascript
webview.navigate(uri);
```  

#### Parâmetros  

**uri**  

*   Tipo: **cadeia de caracteres**  
*   O URI a ser carregado.  

#### Valor de retorno  

Esse método não retorna um valor.  

### navigateFocus  

Navega no foco para o **WebView**.  Dispara o evento window's navigatingfocus do documento de nível superior da WebView.  Os args FocusNavigationEvent usados no evento navigatingfocus correspondem aos parâmetros fornecidos para navigateFocus, exceto os parâmetros de origem são convertidos do espaço de coordenadas do documento host para o espaço de coordenadas do documento de nível superior da WebView.  Consulte o evento WebView departingFocus e o método window. departFocus correspondente para transferir o foco do WebView para o host.  Consulte a [biblioteca de navegação de direção do TVJS](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) para obter um exemplo de implementação de navegação de foco via teclado ou gamepad que usa esse método.  

```javascript
const activeElementBounds = document.activeElement.getBoundingClientRect();
const origin = { 
    originLeft: activeElementBounds.left,
    originTop: activeElementBounds.top,
    originWidth: activeElementBounds.width,
    originHeight: activeElementBounds.height
};
webview.navigateFocus(navigationReason, origin);
```  

#### Parâmetros  

*navigationReason*  

*   Tipo: **cadeia de caracteres**  
*   O motivo da navegação.  O valor deve ser "Left", "up", "Right" ou "Down".  É a direção em que o foco está se afastando do elemento atualmente focalizado.  

*Origin*  

*   Tipo: **objeto**  
*   A origem da navegação.  Este é um objeto JavaScript com propriedades "originLeft", "originTop", "originWidth" e "originHeight".  Esses valores devem descrever a posição e o tamanho do elemento focalizado no momento, longe do qual o foco está sendo movido.  

#### Valor de retorno  

Esse método não retorna um valor.  

### navigateToLocalStreamUri  

Carrega o conteúdo da Web local no URI especificado usando um [**UriToStreamResolver**](/uwp/api/windows.web.iuritostreamresolver.uritostreamasync).  

```javascript
webview.navigateToLocalStreamUri(source, streamResolver); 
```  

#### Parâmetros  

*bibliográfica*  

*   Tipo: **cadeia de caracteres**  
*   Um URI MS-local-Stream que identifica o conteúdo HTML local a ser carregado.  Crie esta cadeia de caracteres usando [**buildLocalStreamUri**](/uwp/api/windows.web.ui.iwebviewcontrol.buildlocalstreamuri).  

*streamResolver*  

*   Tipo: qualquer  
*   Um resolvedor que converte o URI em um fluxo para carregar.  

#### Valor de retorno  

Esse método não retorna um valor.  

### navigateToString  

Carrega o conteúdo HTML especificado como um novo documento.  

```javascript
webview.navigateToString(contents);
```  

#### Parâmetros  

*conteúdos*  

*   Tipo: **cadeia de caracteres**  
*   O conteúdo HTML a ser exibido.  

#### Valor de retorno  

Esse método não retorna um valor.  

### navigateWithHttpRequestMessage  

Navega o WebView para um URI (Uniform Resource Identifier) com uma solicitação POST e cabeçalhos HTTP.  

```javascript
webview.navigateWithHttpRequestMessage(requestMessage);
```  

#### Parâmetros  

*requestMessage*  

*   Tipo: **HttpRequestMessage**  
*   Os detalhes da solicitação HTTP.  

#### Valor de retorno  

Esse método não retorna um valor.  

#### Comentários  

> [!WARNING]
> Se você adicionar mais cabeçalhos a essa solicitação, como credenciais de autenticação, lembre-se de que esses cabeçalhos também serão incluídos em quaisquer solicitações filho subsequentes.  Tenha cuidado para evitar a divulgação acidental de informações confidenciais ou pessoais.  

### Atualize  

Recarrega o conteúdo atual no **WebView**.  

```javascript
webview.refresh();
```  

#### Parâmetros  

Esse método não tem parâmetros.  

#### Valor de retorno  

Esse método não retorna um valor.  

### stop  

Interrompe a navegação ou download atual da **WebView** .  

```javascript
webview.stop();
```  

#### Parâmetros  

Esse método não tem parâmetros.  

#### Valor de retorno  

Esse método não retorna um valor.  

## Propriedades  

### canGoBack  

Obtém um valor que indica se a **WebView** pode navegar para trás.  

Essa propriedade é somente leitura.  

```javascript
var canGoBack = webview.canGoBack;
```  

#### Valor da propriedade  

Tipo: **booliano**  

**Verdadeiro** se a **WebView** puder navegar para trás; caso contrário, **false**.  

### canGoForward  

Obtém um valor que indica se a **WebView** pode navegar para frente.  

Essa propriedade é somente leitura.  

```javascript
var canGoForward = webview.canGoForward;
```  

#### Valor da propriedade  

Tipo: **booliano**  

**Verdadeiro** se a **WebView** puder navegar para frente; caso contrário, **false**.  

### containsFullScreenElement  

Obtém um valor que indica se a **WebView** contém um elemento compatível com tela inteira.  Consulte o evento MSWebViewContainsFullScreenElementChanged para obter mais informações.  

Essa propriedade é somente leitura.  

```javascript
var containsFullScreenElement = webview.containsFullScreenElement;
```  

#### Valor da propriedade  

Tipo: **booliano**  

**Verdadeiro** se a **WebView** contiver um elemento compatível com tela inteira; caso contrário, **false**.  

### documentTitle  

Obtém o título da página atualmente exibida no **WebView**.  

Essa propriedade é somente leitura.  

```javascript
var documentTitle = webview.documentTitle;
```  

#### Valor da propriedade  

Tipo: **cadeia de caracteres**  

O título da página.  

### height  

Obtém ou define a altura do **WebView**.  

```javascript
var height = webview.height;
webview.height = height;
```  

#### Valor da propriedade  

Tipo: **número**  

A altura do **WebView**.  

### processo  

Obtém o processo **WebView** .  

Essa propriedade é somente leitura.  

```javascript
var process = webview.process;
webview.process = process;
```  

#### Valor da propriedade  

Tipo: [MSWebViewProcess](./webview/MSWebViewProcess.md)  

### settings  

Obtém um objeto [MSWebViewSettings](./webview/MSWebViewSettings.md) que contém propriedades para habilitar ou desabilitar recursos do **WebView** .  

Essa propriedade é somente leitura.  

```javascript
var settings = webview.settings;
webview.settings = settings;
```  

#### Valor da propriedade  

Tipo: [MSWebViewSettings](./webview/MSWebViewSettings.md)  

Um objeto [MSWebViewSettings](./webview/MSWebViewSettings.md) que contém propriedades para habilitar ou desabilitar recursos do **WebView** .  

### src  

Obtém ou define a fonte URI (Uniform Resource Identifier) do conteúdo HTML a ser exibido no controle de **WebView** .  

```javascript
var src = webview.src;
webview.src = src;
```  

#### Valor da propriedade  

Tipo: **cadeia de caracteres**  

A origem do URI do conteúdo HTML a ser exibido no controle **WebView** .  

### width  

Obtém ou define a largura do **WebView**.  

```javascript
var width = webview.width;
webview.width = width;
```  

#### Valor da propriedade  

Tipo: **número**  

A largura do **WebView**.  
