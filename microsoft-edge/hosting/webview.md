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
# <span data-ttu-id="67061-104">WebView (EdgeHTML) para aplicativos do Windows 10</span><span class="sxs-lookup"><span data-stu-id="67061-104">WebView (EdgeHTML) for Windows 10 apps</span></span>  

[!INCLUDE [deprecation-note](./includes/deprecation-note.md)]  

<span data-ttu-id="67061-105">O controle WebView (EdgeHTML) permite que você hospede conteúdo da Web em seu aplicativo do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="67061-105">The WebView (EdgeHTML) control enables you to host web content in your Windows 10 app.</span></span>  

<span data-ttu-id="67061-106">Você pode usá-lo como um elemento XAML (para aplicativos da [plataforma universal do Windows (UWP)](/uwp/api/Windows.UI.Xaml.Controls.WebView) e [aplicativos do Windows Forms e da área de trabalho do WPF](/windows/communitytoolkit/controls/wpf-winforms/webview)) ou um elemento HTML (x-MS-WebView)/Dom Object para aplicativos do Windows 10 baseados em JavaScript, conforme descrito aqui.</span><span class="sxs-lookup"><span data-stu-id="67061-106">You can use it as a XAML element (for [Universal Windows Platform (UWP) apps](/uwp/api/Windows.UI.Xaml.Controls.WebView) and [Windows Forms and WPF desktop applications](/windows/communitytoolkit/controls/wpf-winforms/webview)), or an HTML element (x-ms-webview)/DOM object (MSHTMLWebViewElement) for JavaScript-based Windows 10 apps, as described here.</span></span>  

|  |  |  
|:--- |:--- |  
| [**<span data-ttu-id="67061-107">Eventos</span><span class="sxs-lookup"><span data-stu-id="67061-107">Events</span></span>**](#events) | <span data-ttu-id="67061-108">[departingFocus](#departingfocus), [MSWebViewContainsFullScreenElementChanged](#mswebviewcontainsfullscreenelementchanged), [MSWebViewContentLoading](#mswebviewcontentloading), [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded), [MSWebViewFrameContentLoading](#mswebviewframecontentloading), [MSWebViewFrameDOMContentLoaded](#mswebviewframedomcontentloaded), [MSWebViewFrameNavigationCompleted](#mswebviewframenavigationcompleted), [MSWebViewFrameNavigationStarting](#mswebviewframenavigationstarting), [MSWebViewLongRunningScriptDetected](#mswebviewlongrunningscriptdetected), [MSWebViewNavigationCompleted](#mswebviewnavigationcompleted), [MSWebViewNavigationStarting](#mswebviewnavigationstarting), [MSWebViewNewWindowRequested](#mswebviewnewwindowrequested), [MSWebViewPermissionRequested](#mswebviewpermissionrequested), [MSWebViewProcessExited](#mswebviewprocessexited), [MSWebViewWebResourceRequested](#mswebviewwebresourcerequested), [MSWebViewScriptNotify](#mswebviewscriptnotify), [MSWebViewUnsafeContentWarningDisplaying](#mswebviewunsafecontentwarningdisplaying), [MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsupportedurischemeidentified), [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified)</span><span class="sxs-lookup"><span data-stu-id="67061-108">[departingFocus](#departingfocus), [MSWebViewContainsFullScreenElementChanged](#mswebviewcontainsfullscreenelementchanged), [MSWebViewContentLoading](#mswebviewcontentloading), [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded), [MSWebViewFrameContentLoading](#mswebviewframecontentloading), [MSWebViewFrameDOMContentLoaded](#mswebviewframedomcontentloaded), [MSWebViewFrameNavigationCompleted](#mswebviewframenavigationcompleted), [MSWebViewFrameNavigationStarting](#mswebviewframenavigationstarting), [MSWebViewLongRunningScriptDetected](#mswebviewlongrunningscriptdetected), [MSWebViewNavigationCompleted](#mswebviewnavigationcompleted), [MSWebViewNavigationStarting](#mswebviewnavigationstarting), [MSWebViewNewWindowRequested](#mswebviewnewwindowrequested), [MSWebViewPermissionRequested](#mswebviewpermissionrequested), [MSWebViewProcessExited](#mswebviewprocessexited), [MSWebViewWebResourceRequested](#mswebviewwebresourcerequested), [MSWebViewScriptNotify](#mswebviewscriptnotify), [MSWebViewUnsafeContentWarningDisplaying](#mswebviewunsafecontentwarningdisplaying), [MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsupportedurischemeidentified), [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified)</span></span> |  
| [**<span data-ttu-id="67061-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="67061-109">Methods</span></span>**](#methods) | <span data-ttu-id="67061-110">[addWebAllowedObject](#addweballowedobject), [buildlocalStreamUri](#buildlocalstreamuri), [capturePreviewToBlobAsync](#capturepreviewtoblobasync), [captureSelectedContentToDataPackageAsync](#captureselectedcontenttodatapackageasync), [invokeScriptAsync](#invokescriptasync), [getDeferredPermissionRequests](#getdeferredpermissionrequests), [getDeferredPermissionRequestById](#getdeferredpermissionrequestbyid), [goBack](#goback), [goForward](#goforward), [navegar](#navigate), [navigateFocus](#navigatefocus), [navigateTolocalStreamUri](#navigatetolocalstreamuri), [navigateToString](#navigatetostring), [navigateWithHttpRequestMessage](#navigatewithhttprequestmessage), [Atualizar](#refresh), [parar](#stop)</span><span class="sxs-lookup"><span data-stu-id="67061-110">[addWebAllowedObject](#addweballowedobject), [buildlocalStreamUri](#buildlocalstreamuri), [capturePreviewToBlobAsync](#capturepreviewtoblobasync), [captureSelectedContentToDataPackageAsync](#captureselectedcontenttodatapackageasync), [invokeScriptAsync](#invokescriptasync), [getDeferredPermissionRequests](#getdeferredpermissionrequests), [getDeferredPermissionRequestById](#getdeferredpermissionrequestbyid), [goBack](#goback), [goForward](#goforward), [navigate](#navigate), [navigateFocus](#navigatefocus), [navigateTolocalStreamUri](#navigatetolocalstreamuri), [navigateToString](#navigatetostring), [navigateWithHttpRequestMessage](#navigatewithhttprequestmessage), [refresh](#refresh), [stop](#stop)</span></span> |  
| [**<span data-ttu-id="67061-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="67061-111">Properties</span></span>**](#properties) | <span data-ttu-id="67061-112">[CanGoBack](#cangoback), [canGoForward](#cangoforward), [containsFullScreenElement](#containsfullscreenelement), [DocumentTitle](#documenttitle), [Height](#height), [process](#process), [Settings](#settings), [src](#src), [Width](#width)</span><span class="sxs-lookup"><span data-stu-id="67061-112">[canGoBack](#cangoback), [canGoForward](#cangoforward), [containsFullScreenElement](#containsfullscreenelement), [documentTitle](#documenttitle), [height](#height), [process](#process), [settings](#settings), [src](#src), [width](#width)</span></span> |  

## <span data-ttu-id="67061-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67061-113">Syntax</span></span>  

```javascript
// Feature detect for webview support
if (MSHTMLWebViewElement) {
    let wv = document.createElement('x-ms-webview'); // Use CSS to set width, height and other styles
    wv.navigate("https://www.example.com");
    document.body.appendChild(wv);
}
```  

## <span data-ttu-id="67061-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="67061-114">Remarks</span></span>  

### <span data-ttu-id="67061-115">WebView versus iframe</span><span class="sxs-lookup"><span data-stu-id="67061-115">WebView versus iframe</span></span>  

<span data-ttu-id="67061-116">Como um elemento HTML [iframe](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) padrão, você pode usar o WebView para carregar páginas remotas por http e páginas locais (*MS-Appx-Web:///*) do pacote do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67061-116">Like a standard HTML [iframe](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) element, you can use WebView to load remote pages over HTTP and local pages (*ms-appx-web:///*) from your app package.</span></span>  <span data-ttu-id="67061-117">No entanto, o WebView também pode:</span><span class="sxs-lookup"><span data-stu-id="67061-117">However, the WebView can also:</span></span>  

*   <span data-ttu-id="67061-118">Carregar páginas e recursos de suas pastas [ApplicationData](/uwp/api/Windows.Storage.ApplicationData) (locais, móveis, Temp) (*MS-AppData:///*) e [fluxos de memória](/microsoft-edge/hosting/webview#buildlocalstreamuri) (*MS-local-Stream:///*)</span><span class="sxs-lookup"><span data-stu-id="67061-118">Load pages and resources from your [ApplicationData](/uwp/api/Windows.Storage.ApplicationData) (local, roaming, temp) folders (*ms-appdata:///*) and [in-memory streams](/microsoft-edge/hosting/webview#buildlocalstreamuri) (*ms-local-stream:///*)</span></span>  
*   <span data-ttu-id="67061-119">Fornecer controles semelhantes a navegadores: para [voltar](#goback) e [Avançar](#goforward) no histórico de navegação, e [parando](#stop) ou [atualizando](#refresh) a página atual.</span><span class="sxs-lookup"><span data-stu-id="67061-119">Provide browser-like controls: for going [back](#goback) and [forward](#goforward) in navigation history, and [stopping](#stop) or [refreshing](#refresh) the current page.</span></span>  
*   <span data-ttu-id="67061-120">[Capture capturas de tela do conteúdo da Web](#capturepreviewtoblobasync) tornando mais fácil implementar o contrato de [compartilhamento](/windows/uwp/app-to-app/share-data) de aplicativos do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="67061-120">[Capture screenshots of web content](#capturepreviewtoblobasync) making it easy to implement the Windows 10 app [Share](/windows/uwp/app-to-app/share-data) contract.</span></span>  
*   <span data-ttu-id="67061-121">Permita que o código JavaScript em execução em um WebView aumente eventos personalizados ([MSWebViewScriptNotify](#mswebviewscriptnotify)) para o aplicativo e permita que o aplicativo execute JavaScript dentro do WebView ([invokeScriptAsync](#invokescriptasync)).</span><span class="sxs-lookup"><span data-stu-id="67061-121">Allow JavaScript code running within a webview to raise custom events ([MSWebViewScriptNotify](#mswebviewscriptnotify)) to your app, and allow your app to run JavaScript within the webview ([invokeScriptAsync](#invokescriptasync)).</span></span>  
*   <span data-ttu-id="67061-122">Forneça eventos de conteúdo do WebView finos.</span><span class="sxs-lookup"><span data-stu-id="67061-122">Provide you with fine-tuned webview content events:</span></span>  
    
    | <span data-ttu-id="67061-123">Evento DOM do WebView</span><span class="sxs-lookup"><span data-stu-id="67061-123">WebView DOM event</span></span> | <span data-ttu-id="67061-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="67061-124">Description</span></span> |  
    |:--- |:--- |  
    | [<span data-ttu-id="67061-125">MSWebViewNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="67061-125">MSWebViewNavigationStarting</span></span>](#mswebviewnavigationstarting) | <span data-ttu-id="67061-126">Indica que o WebView está começando a navegar.</span><span class="sxs-lookup"><span data-stu-id="67061-126">Indicates the WebView is starting to navigate.</span></span>  |  
    | [<span data-ttu-id="67061-127">MSWebViewContentLoading</span><span class="sxs-lookup"><span data-stu-id="67061-127">MSWebViewContentLoading</span></span>](#mswebviewcontentloading) | <span data-ttu-id="67061-128">O conteúdo HTML é baixado e está sendo carregado no controle.</span><span class="sxs-lookup"><span data-stu-id="67061-128">The HTML content is downloaded and is being loaded into the control.</span></span>  |  
    | [<span data-ttu-id="67061-129">MSWebViewDOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="67061-129">MSWebViewDOMContentLoaded</span></span>](#mswebviewdomcontentloaded) | <span data-ttu-id="67061-130">Indica que os principais elementos DOM terminaram de carregar.</span><span class="sxs-lookup"><span data-stu-id="67061-130">Indicates that the main DOM elements have finished loading.</span></span>  |  
    | [<span data-ttu-id="67061-131">MSWebViewNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="67061-131">MSWebViewNavigationCompleted</span></span>](#mswebviewnavigationcompleted) | <span data-ttu-id="67061-132">Indica a conclusão da navegação e todos os elementos de mídia são renderizados.</span><span class="sxs-lookup"><span data-stu-id="67061-132">Indicates the navigation is complete, and all media elements are rendered.</span></span>  |  
    | [<span data-ttu-id="67061-133">MSWebViewUnviewableContentIdentified</span><span class="sxs-lookup"><span data-stu-id="67061-133">MSWebViewUnviewableContentIdentified</span></span>](#mswebviewunviewablecontentidentified) | <span data-ttu-id="67061-134">O WebView encontrou o conteúdo não era HTML.</span><span class="sxs-lookup"><span data-stu-id="67061-134">The WebView found the content was not HTML.</span></span>  |  
    | [<span data-ttu-id="67061-135">UnsafeContentWarningDisplaying</span><span class="sxs-lookup"><span data-stu-id="67061-135">UnsafeContentWarningDisplaying</span></span>](#mswebviewunsafecontentwarningdisplaying) | <span data-ttu-id="67061-136">O WebView mostra uma página de aviso para o conteúdo que foi relatado como não seguro pelo *Filtro SmartScreen*do Windows.</span><span class="sxs-lookup"><span data-stu-id="67061-136">The WebView shows a warning page for content that was reported as unsafe by Windows *SmartScreen Filter*.</span></span>  |  
    
    <span data-ttu-id="67061-137">... incluindo [eventos](#events) correspondentes para conteúdo iframe carregado em um WebView (como [MSWebView**frame**NavigationStarting](#mswebviewframenavigationstarting) e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="67061-137">...including corresponding [events](#events) for iframe content loaded within a WebView (such as [MSWebView**Frame**NavigationStarting](#mswebviewframenavigationstarting) and so on).</span></span> 

### <span data-ttu-id="67061-138">Impressão</span><span class="sxs-lookup"><span data-stu-id="67061-138">Printing</span></span>  

<span data-ttu-id="67061-139">Quando um aplicativo do Windows que usa JavaScript é impresso, as `<x-ms-webview>` marcas são transformadas em `<iframe>` marcas antes da impressão.</span><span class="sxs-lookup"><span data-stu-id="67061-139">When a Windows app using JavaScript is printed, the `<x-ms-webview>` tags are transformed into `<iframe>` tags before printing.</span></span>  <span data-ttu-id="67061-140">Além da diferença normal entre exibir na tela e renderizado para impressão, estilos CSS aplicados a `<iframe>` elementos são, então, aplicáveis à `<iframe>` transformada de `<x-ms-webview>` .</span><span class="sxs-lookup"><span data-stu-id="67061-140">Besides the normal difference between displaying on screen and rendered for print, CSS styles applied to `<iframe>` elements are then applicable to the `<iframe>` transformed from `<x-ms-webview>`.</span></span>  

### <span data-ttu-id="67061-141">Trabalhadores do serviço</span><span class="sxs-lookup"><span data-stu-id="67061-141">Service workers</span></span>  

<span data-ttu-id="67061-142">Começando com a [atualização do Windows 10 de outubro de 2018](/windows/uwp/whats-new/windows-10-build-17763) (EdgeHTML 18), [os funcionários de serviço são compatíveis com o controle WebView](/microsoft-edge/dev-guide#service-workers) (além do navegador Microsoft Edge e aplicativos do Windows 10 com JavaScript).</span><span class="sxs-lookup"><span data-stu-id="67061-142">Starting with the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) (EdgeHTML 18), [service workers are supported in the WebView control](/microsoft-edge/dev-guide#service-workers) (in addition to the Microsoft Edge browser and Windows 10 apps with JavaScript).</span></span>  

<span data-ttu-id="67061-143">as arquiteturas de aplicativos x64 exigem pacotes neutros (qualquer CPU) ou x64, pois os operadores de serviço não são compatíveis com processos WoW64.</span><span class="sxs-lookup"><span data-stu-id="67061-143">x64 app architectures require Neutral (Any CPU) or x64 packages, as service workers are not supported in WoW64 processes.</span></span>  <span data-ttu-id="67061-144">(Para conservar espaço em disco, a versão WoW das DLLs necessárias não está incluída nativamente no Windows.)</span><span class="sxs-lookup"><span data-stu-id="67061-144">(To conserve disk space, the WoW version of the required DLLs are not natively included in Windows.)</span></span>  

### <span data-ttu-id="67061-145">Modelo de threading e confiabilidade</span><span class="sxs-lookup"><span data-stu-id="67061-145">Threading model and reliability</span></span>  

<span data-ttu-id="67061-146">A criação de uma WebView via `document.createElement("x-ms-webview")` ou via `<x-ms-webview>` marcação cria uma WebView em um novo thread exclusivo no processo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67061-146">Creating a WebView via `document.createElement("x-ms-webview")` or via `<x-ms-webview>` markup creates a WebView on a new unique thread in the app's process.</span></span>  <span data-ttu-id="67061-147">Executar em um novo thread exclusivo significa que o script de execução longa de um WebView não pode travar o aplicativo ou outros modos de exibição da Web.</span><span class="sxs-lookup"><span data-stu-id="67061-147">Running on a new unique thread means that long running script from one WebView is unable to hang the app or other WebViews.</span></span>  <span data-ttu-id="67061-148">Criar uma WebView por meio do `new MSWebView()` construtor cria uma WebView em um processo da WebView separado.</span><span class="sxs-lookup"><span data-stu-id="67061-148">Creating a WebView via the `new MSWebView()` constructor creates a WebView in a separate WebView process.</span></span>  <span data-ttu-id="67061-149">Executar em um processo exclusivo significa que, além da proteção de um script de execução longa, o aplicativo também é protegido do conteúdo da Web que falha no processo da WebView.</span><span class="sxs-lookup"><span data-stu-id="67061-149">Running in a unique process means that in addition to protection from long running script, the app is also protected from web content that crashes the WebView process.</span></span>  <span data-ttu-id="67061-150">Criar uma WebView pelo [`MSWebViewProcess.createWebViewAsync`](./webview/MSWebViewProcess.md#createwebviewasync) método também cria uma WebView em um processo separado, mas permite que o chamador controle mais sobre configurações de processo e agrupamentos de Webviews em processos WebView.</span><span class="sxs-lookup"><span data-stu-id="67061-150">Creating a WebView via the [`MSWebViewProcess.createWebViewAsync`](./webview/MSWebViewProcess.md#createwebviewasync) method also creates a WebView in a separate process but allows the caller more control over process settings and grouping WebViews in WebView processes.</span></span>  <span data-ttu-id="67061-151">Consulte `MSWebViewProcess` para mais informações.</span><span class="sxs-lookup"><span data-stu-id="67061-151">See `MSWebViewProcess` for more information.</span></span>  

### <span data-ttu-id="67061-152">Acesso à API do WinRT</span><span class="sxs-lookup"><span data-stu-id="67061-152">WinRT API access</span></span>  

<span data-ttu-id="67061-153">Um aplicativo UWP pode permitir que documentos HTML dentro de webviews tenham acesso a APIs do WinRT.</span><span class="sxs-lookup"><span data-stu-id="67061-153">A UWP app may allow HTML documents inside WebViews to have access to WinRT APIs.</span></span>  <span data-ttu-id="67061-154">Isso ocorre por meio do atributo WindowsRuntimeAccess dos elementos filho da regra do elemento ApplicationContentUriRules do AppxManifest.xml do aplicativo UWP.</span><span class="sxs-lookup"><span data-stu-id="67061-154">This is via the WindowsRuntimeAccess attribute of the Rule child elements of the ApplicationContentUriRules element of the AppxManifest.xml of the UWP app.</span></span>  <span data-ttu-id="67061-155">Defina WindowsRuntimeAccess como ' all' e documentos HTML com URIs correspondentes poderão usar o WinRT.</span><span class="sxs-lookup"><span data-stu-id="67061-155">Set WindowsRuntimeAccess to 'all' and HTML documents with matching URIs will be allowed to use WinRT.</span></span>  <span data-ttu-id="67061-156">Isso é o mesmo que fornecer acesso ao WinRT para conteúdo HTML em aplicativos UWP JavaScript, portanto, consulte [chamar APIs do winrt a partir do seu PWA](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#call-winrt-apis-from-your-pwa) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="67061-156">This is the same as providing WinRT access to HTML content in JavaScript UWP apps so see [Call WinRT APIs from your PWA](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#call-winrt-apis-from-your-pwa) for more information.</span></span>  

<span data-ttu-id="67061-157">APIs do WinRT relacionadas à interface do usuário podem não funcionar quando chamadas de um WebView executando em seu próprio thread, mas podem funcionar quando são chamadas de um WebView em execução em um processo do WebView separado.</span><span class="sxs-lookup"><span data-stu-id="67061-157">UI related WinRT APIs may not work when called from a WebView running on its own thread but may work when called from a WebView running in a separate WebView process.</span></span>  <span data-ttu-id="67061-158">Ao usar um WebView em seu próprio thread exclusivo, esse thread não é o thread de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67061-158">When using a WebView on its own unique thread, that thread is not the app's view thread.</span></span>  <span data-ttu-id="67061-159">Algumas APIs do WinRT relacionadas à interface do usuário precisam ser chamadas do thread de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67061-159">Some UI related WinRT APIs require to be called from the app's view thread.</span></span>  <span data-ttu-id="67061-160">Os webviews criados em um processo da WebView separado são executados em um thread de exibição e, portanto, não devem ter as mesmas restrições da execução do WebView em seu próprio thread exclusivo.</span><span class="sxs-lookup"><span data-stu-id="67061-160">WebViews created in a separate WebView process do run on a view thread and so should not face the same restrictions as WebView's running on their own unique thread.</span></span>  <span data-ttu-id="67061-161">Se você tiver problemas com APIs do WinRT relacionadas à interface do usuário em uma WebView, verifique se está usando uma WebView em seu próprio processo WebView, conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="67061-161">If you have trouble with UI related WinRT APIs in a WebView ensure that you're using a WebView in its own WebView process as described above.</span></span>  

### <span data-ttu-id="67061-162">Limitações de armazenamento do AppCache</span><span class="sxs-lookup"><span data-stu-id="67061-162">AppCache storage limitations</span></span>  

<span data-ttu-id="67061-163">Os aplicativos que usam o suporte a JavaScript da API de cache do aplicativo (ou AppCache), conforme definido na [especificação do HTML5](https://go.microsoft.com/fwlink/p/?LinkId=228542), para criar aplicativos Web offline devem observar as limitações de armazenamento disponíveis.</span><span class="sxs-lookup"><span data-stu-id="67061-163">Applications using JavaScript support of the Application Cache API (or AppCache), as defined in the [HTML5 specification](https://go.microsoft.com/fwlink/p/?LinkId=228542), to create offline web applications must observe available storage limitations.</span></span>  <span data-ttu-id="67061-164">Isso é especialmente verdadeiro em dispositivos com espaço limitado de memória.</span><span class="sxs-lookup"><span data-stu-id="67061-164">This is especially true in devices with limited memory space.</span></span>  <span data-ttu-id="67061-165">Os limites práticos do tamanho do AppCache são sempre uma função do espaço de armazenamento em disco disponível.</span><span class="sxs-lookup"><span data-stu-id="67061-165">The practical limits on the size of the AppCache are always a function of available disk storage space.</span></span>  <span data-ttu-id="67061-166">As diretrizes gerais são mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="67061-166">The general guidelines are shown below.</span></span>  

| <span data-ttu-id="67061-167">Tamanho do volume</span><span class="sxs-lookup"><span data-stu-id="67061-167">Volume size</span></span> |<span data-ttu-id="67061-168">AppCache por domínio</span><span class="sxs-lookup"><span data-stu-id="67061-168">AppCache per domain</span></span> | <span data-ttu-id="67061-169">AppCache por usuário</span><span class="sxs-lookup"><span data-stu-id="67061-169">AppCache per user</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="67061-170">Até 4 GB</span><span class="sxs-lookup"><span data-stu-id="67061-170">Up to 4GB</span></span> | <span data-ttu-id="67061-171">10MB</span><span class="sxs-lookup"><span data-stu-id="67061-171">10MB</span></span> | <span data-ttu-id="67061-172">50 MB</span><span class="sxs-lookup"><span data-stu-id="67061-172">50MB</span></span> |  
| <span data-ttu-id="67061-173">4 GB para 16 GB</span><span class="sxs-lookup"><span data-stu-id="67061-173">4GB to 16GB</span></span> | <span data-ttu-id="67061-174">50 MB</span><span class="sxs-lookup"><span data-stu-id="67061-174">50MB</span></span> | <span data-ttu-id="67061-175">500MB</span><span class="sxs-lookup"><span data-stu-id="67061-175">500MB</span></span> |  
| <span data-ttu-id="67061-176">de 16 GB a 32 GB</span><span class="sxs-lookup"><span data-stu-id="67061-176">16GB to 32 GB</span></span> | <span data-ttu-id="67061-177">50 MB</span><span class="sxs-lookup"><span data-stu-id="67061-177">50MB</span></span> | <span data-ttu-id="67061-178">1 GB</span><span class="sxs-lookup"><span data-stu-id="67061-178">1GB</span></span> |  

<span data-ttu-id="67061-179">Todos os aplicativos do Windows10 devem usar o mesmo modelo de cota AppCache, portanto, a limitação de armazenamento em disco disponível se aplica aos aplicativos de área de trabalho e de telefone.</span><span class="sxs-lookup"><span data-stu-id="67061-179">All Windows10 apps are intended to use the same AppCache quota model, so the available disk storage limitation applies to both desktop and phone apps.</span></span>  <span data-ttu-id="67061-180">O limite do é também um difícil depois das páginas carregadas dentro do **WebView** , consumindo 1 GB de espaço *AppCache* ; solicitações para armazenamento adicional do *AppCache* acima desse limite serão negadas.</span><span class="sxs-lookup"><span data-stu-id="67061-180">The is also a hard limit after pages loaded inside **WebView** together have consumed 1 GB of *AppCache* space; requests for additional *AppCache* storage above this limit will be denied.</span></span>  

<span data-ttu-id="67061-181">Para obter mais informações, consulte o [exemplo de controle HTML WebView](https://go.microsoft.com/fwlink/p/?linkid=309825) e o JSBrowser a documentação do [controle WebView](https://github.com/MicrosoftEdge/JSBrowser#harnessing-the-webview-control) .</span><span class="sxs-lookup"><span data-stu-id="67061-181">For more information, see the [HTML WebView control sample](https://go.microsoft.com/fwlink/p/?linkid=309825) and the JSBrowser's [Harnessing the WebView control](https://github.com/MicrosoftEdge/JSBrowser#harnessing-the-webview-control) documentation.</span></span>  

## <span data-ttu-id="67061-182">Eventos</span><span class="sxs-lookup"><span data-stu-id="67061-182">Events</span></span>  

### <span data-ttu-id="67061-183">departingFocus</span><span class="sxs-lookup"><span data-stu-id="67061-183">departingFocus</span></span>  

<span data-ttu-id="67061-184">Indica a deaplicação de foco do **WebView** no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67061-184">Indicates focus departing from the **webview** into the app.</span></span>  <span data-ttu-id="67061-185">Acionado quando a janela de chamadas do documento de nível superior da WebView. departFocus.</span><span class="sxs-lookup"><span data-stu-id="67061-185">Fires when the webview's top level document calls window.departFocus.</span></span>  <span data-ttu-id="67061-186">Os args FocusNavigationEvent no evento departingFocus correspondem aos parâmetros fornecidos para departFocus, exceto os parâmetros de origem são convertidos do espaço de coordenadas de document's da WebView para o espaço de coordenadas do documento do host de WebView.</span><span class="sxs-lookup"><span data-stu-id="67061-186">The FocusNavigationEvent args in the departingFocus event match the parameters provided to departFocus except the origin parameters are translated from the webview's document's coordinate space to the coordinate space of the webview host document.</span></span>  <span data-ttu-id="67061-187">Consulte o método WebView. navigateFocus e o evento navigatingFocus de janela correspondente para transferir o foco do host para o WebView.</span><span class="sxs-lookup"><span data-stu-id="67061-187">See the webview.navigateFocus method and corresponding window navigatingFocus event for transferring focus from host to webview.</span></span>  <span data-ttu-id="67061-188">Consulte a [biblioteca de navegação de direção do TVJS](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) para obter um exemplo de implementação de navegação de foco via teclado ou gamepad que manipula esse evento.</span><span class="sxs-lookup"><span data-stu-id="67061-188">See the [TVJS's Direction Navigation library](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) for an example of an implementation of focus navigation via keyboard or gamepad that handles this event.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("departingFocus", handler);
webview.removeEventListener("departingFocus", handler);
```  

#### <span data-ttu-id="67061-189">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-189">Event Information</span></span>  

|            |      |  
|:--- |:--- |  
| **<span data-ttu-id="67061-190">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-190">Interface</span></span>** | [<span data-ttu-id="67061-191">FocusNavigationEvent</span><span class="sxs-lookup"><span data-stu-id="67061-191">FocusNavigationEvent</span></span>](./webview/FocusNavigationEvent.md) |  
| **<span data-ttu-id="67061-192">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-192">Synchronous</span></span>** | <span data-ttu-id="67061-193">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-193">Yes</span></span> |   
| **<span data-ttu-id="67061-194">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-194">Bubbles</span></span>** | <span data-ttu-id="67061-195">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-195">Yes</span></span> |  
| **<span data-ttu-id="67061-196">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-196">Cancelable</span></span>** | <span data-ttu-id="67061-197">Não</span><span class="sxs-lookup"><span data-stu-id="67061-197">No</span></span> |  

### <span data-ttu-id="67061-198">MSWebViewContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="67061-198">MSWebViewContainsFullScreenElementChanged</span></span>  

<span data-ttu-id="67061-199">Ocorre quando o status muda ou não **no momento se** contém um elemento de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="67061-199">Occurs when the status changes of whether or not the **webview** currently contains a full screen element.</span></span>  <span data-ttu-id="67061-200">Use a propriedade containsFullScreenElement para o valor atual.</span><span class="sxs-lookup"><span data-stu-id="67061-200">Use the containsFullScreenElement property to the current value.</span></span>  <span data-ttu-id="67061-201">Aqui, o elemento de tela inteira refere-se à noção de [APIs do dom](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) de tela inteira por meio das funções dom Element. requestFullScreen e Document. exitFullScreen.</span><span class="sxs-lookup"><span data-stu-id="67061-201">Full screen element here refers to the [Fullscreen DOM APIs](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) notion of a full screen element via the element.requestFullScreen and document.exitFullScreen DOM functions.</span></span>  

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

#### <span data-ttu-id="67061-202">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-202">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-203">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-203">Interface</span></span>** | **<span data-ttu-id="67061-204">Evento</span><span class="sxs-lookup"><span data-stu-id="67061-204">Event</span></span>** |  
| **<span data-ttu-id="67061-205">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-205">Synchronous</span></span>** | <span data-ttu-id="67061-206">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-206">Yes</span></span> |  
| **<span data-ttu-id="67061-207">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-207">Bubbles</span></span>** | <span data-ttu-id="67061-208">Não</span><span class="sxs-lookup"><span data-stu-id="67061-208">No</span></span> |   
| **<span data-ttu-id="67061-209">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-209">Cancelable</span></span>** | <span data-ttu-id="67061-210">Não</span><span class="sxs-lookup"><span data-stu-id="67061-210">No</span></span> |  

### <span data-ttu-id="67061-211">MSWebViewContentLoading</span><span class="sxs-lookup"><span data-stu-id="67061-211">MSWebViewContentLoading</span></span>  

<span data-ttu-id="67061-212">Indica que o conteúdo HTML é baixado e está sendo carregado no controle.</span><span class="sxs-lookup"><span data-stu-id="67061-212">Indicates that the HTML content is downloaded and is being loaded into the control.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewContentLoading", handler);
webview.removeEventListener("MSWebViewContentLoading", handler);
```  

#### <span data-ttu-id="67061-213">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-213">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-214">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-214">Interface</span></span>** | [<span data-ttu-id="67061-215">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="67061-215">NavigationEvent</span></span>](./webview/NavigationEvent.md) |  
| **<span data-ttu-id="67061-216">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-216">Synchronous</span></span>** | <span data-ttu-id="67061-217">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-217">Yes</span></span>  |  
| **<span data-ttu-id="67061-218">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-218">Bubbles</span></span>** | <span data-ttu-id="67061-219">Não</span><span class="sxs-lookup"><span data-stu-id="67061-219">No</span></span> |   
| **<span data-ttu-id="67061-220">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-220">Cancelable</span></span>** | <span data-ttu-id="67061-221">Não</span><span class="sxs-lookup"><span data-stu-id="67061-221">No</span></span> |  

### <span data-ttu-id="67061-222">MSWebViewDOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="67061-222">MSWebViewDOMContentLoaded</span></span>  

<span data-ttu-id="67061-223">Indica que os principais elementos DOM terminaram de carregar.</span><span class="sxs-lookup"><span data-stu-id="67061-223">Indicates that the main DOM elements have finished loading.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewDOMContentLoaded", handler);
```  

#### <span data-ttu-id="67061-224">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-224">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-225">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-225">Interface</span></span>** | [<span data-ttu-id="67061-226">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="67061-226">NavigationEvent</span></span>](./webview/NavigationEvent.md) |  
| **<span data-ttu-id="67061-227">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-227">Synchronous</span></span>** |<span data-ttu-id="67061-228">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-228">Yes</span></span> |  
| **<span data-ttu-id="67061-229">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-229">Bubbles</span></span>** | <span data-ttu-id="67061-230">Não</span><span class="sxs-lookup"><span data-stu-id="67061-230">No</span></span> |  
| **<span data-ttu-id="67061-231">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-231">Cancelable</span></span>** | <span data-ttu-id="67061-232">Não</span><span class="sxs-lookup"><span data-stu-id="67061-232">No</span></span> |   

### <span data-ttu-id="67061-233">MSWebViewFrameContentLoading</span><span class="sxs-lookup"><span data-stu-id="67061-233">MSWebViewFrameContentLoading</span></span>  

<span data-ttu-id="67061-234">Indica que o conteúdo HTML foi baixado e está sendo carregado no `<iframe>` controle.</span><span class="sxs-lookup"><span data-stu-id="67061-234">Indicates that the HTML content downloaded and is being loaded into the `<iframe>` control.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameContentLoading", handler);
webview.removeEventListener("MSWebViewFrameContentLoading", handler);
```  

#### <span data-ttu-id="67061-235">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-235">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-236">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-236">Interface</span></span>** | [<span data-ttu-id="67061-237">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="67061-237">NavigationEvent</span></span>](./webview/NavigationEvent.md) |  
| **<span data-ttu-id="67061-238">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-238">Synchronous</span></span>** | <span data-ttu-id="67061-239">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-239">Yes</span></span> |  
| **<span data-ttu-id="67061-240">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-240">Bubbles</span></span>** | <span data-ttu-id="67061-241">Não</span><span class="sxs-lookup"><span data-stu-id="67061-241">No</span></span> |  
| **<span data-ttu-id="67061-242">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-242">Cancelable</span></span>** | <span data-ttu-id="67061-243">Não</span><span class="sxs-lookup"><span data-stu-id="67061-243">No</span></span> |   

### <span data-ttu-id="67061-244">MSWebViewFrameDOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="67061-244">MSWebViewFrameDOMContentLoaded</span></span>  

<span data-ttu-id="67061-245">Indica que os principais elementos DOM terminaram de carregar no `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="67061-245">Indicates that the main DOM elements have finished loading in the `<iframe>`.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewFrameDOMContentLoaded", handler);
```  

#### <span data-ttu-id="67061-246">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-246">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-247">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-247">Interface</span></span>** | [<span data-ttu-id="67061-248">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="67061-248">NavigationEvent</span></span>](./webview/NavigationEvent.md) |  
| **<span data-ttu-id="67061-249">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-249">Synchronous</span></span>** | <span data-ttu-id="67061-250">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-250">Yes</span></span> |  
| **<span data-ttu-id="67061-251">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-251">Bubbles</span></span>** | <span data-ttu-id="67061-252">Não</span><span class="sxs-lookup"><span data-stu-id="67061-252">No</span></span> |   
| **<span data-ttu-id="67061-253">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-253">Cancelable</span></span>** | <span data-ttu-id="67061-254">Não</span><span class="sxs-lookup"><span data-stu-id="67061-254">No</span></span> |  

### <span data-ttu-id="67061-255">MSWebViewFrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="67061-255">MSWebViewFrameNavigationCompleted</span></span>  

<span data-ttu-id="67061-256">Indica a conclusão da navegação, e todos os elementos de mídia são renderizados no `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="67061-256">Indicates the navigation is complete, and all media elements are rendered in the `<iframe>`.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationCompleted", handler);
webview.removeEventListener("MSWebViewFrameNavigationCompleted", handler);
```  

#### <span data-ttu-id="67061-257">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-257">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-258">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-258">Interface</span></span>** | [<span data-ttu-id="67061-259">NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="67061-259">NavigationCompletedEvent</span></span>](./webview/NavigationCompletedEvent.md) |  
| **<span data-ttu-id="67061-260">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-260">Synchronous</span></span>** | <span data-ttu-id="67061-261">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-261">Yes</span></span> |  
| **<span data-ttu-id="67061-262">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-262">Bubbles</span></span>** | <span data-ttu-id="67061-263">Não</span><span class="sxs-lookup"><span data-stu-id="67061-263">No</span></span> |   
| **<span data-ttu-id="67061-264">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-264">Cancelable</span></span>** | <span data-ttu-id="67061-265">Não</span><span class="sxs-lookup"><span data-stu-id="67061-265">No</span></span> |  

### <span data-ttu-id="67061-266">MSWebViewFrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="67061-266">MSWebViewFrameNavigationStarting</span></span>  

<span data-ttu-id="67061-267">Indica `<iframe>` que a em um **WebView** está começando a navegar.</span><span class="sxs-lookup"><span data-stu-id="67061-267">Indicates a `<iframe>` within a **webview** is starting to navigate.</span></span>  <span data-ttu-id="67061-268">Isso é acionado antes da obtenção de recursos da rede para a navegação.</span><span class="sxs-lookup"><span data-stu-id="67061-268">This is fired before obtaining any resources from the network for the navigation.</span></span>  <span data-ttu-id="67061-269">A navegação não é iniciada até que todos os manipuladores de eventos MSWebViewFrameNavigationStarting sejam concluídos.</span><span class="sxs-lookup"><span data-stu-id="67061-269">The navigation is not started until all MSWebViewFrameNavigationStarting event handlers complete.</span></span>  <span data-ttu-id="67061-270">Esse evento é cancelável pela chamada `eventArgs.preventDefault()` .</span><span class="sxs-lookup"><span data-stu-id="67061-270">This event is cancellable via calling `eventArgs.preventDefault()`.</span></span>  <span data-ttu-id="67061-271">Se for cancelado, o WebView não executará a navegação.</span><span class="sxs-lookup"><span data-stu-id="67061-271">If cancelled, the WebView will not perform the navigation.</span></span>  

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

#### <span data-ttu-id="67061-272">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-272">Event Information</span></span>  

|  |  |
|:--- |:--- |  
| **<span data-ttu-id="67061-273">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-273">Interface</span></span>** | [<span data-ttu-id="67061-274">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="67061-274">NavigationEvent</span></span>](./webview/NavigationEvent.md) |  
| **<span data-ttu-id="67061-275">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-275">Synchronous</span></span>** | <span data-ttu-id="67061-276">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-276">Yes</span></span> |  
| **<span data-ttu-id="67061-277">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-277">Bubbles</span></span>** |<span data-ttu-id="67061-278">Não</span><span class="sxs-lookup"><span data-stu-id="67061-278">No</span></span> |   
| **<span data-ttu-id="67061-279">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-279">Cancelable</span></span>** | <span data-ttu-id="67061-280">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-280">Yes</span></span> |  

### <span data-ttu-id="67061-281">MSWebViewLongRunningScriptDetected</span><span class="sxs-lookup"><span data-stu-id="67061-281">MSWebViewLongRunningScriptDetected</span></span>  

<span data-ttu-id="67061-282">Ocorre periodicamente durante a execução ininterrupta do script no **WebView**, permitindo que você pare o script.</span><span class="sxs-lookup"><span data-stu-id="67061-282">Occurs periodically during uninterrupted script execution in the **webview**, letting you halt the script.</span></span>  

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

#### <span data-ttu-id="67061-283">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-283">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-284">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-284">Interface</span></span>** | [<span data-ttu-id="67061-285">LongRunningScriptDetectedEvent</span><span class="sxs-lookup"><span data-stu-id="67061-285">LongRunningScriptDetectedEvent</span></span>](./webview/LongRunningScriptDetectedEvent.md) |  
| **<span data-ttu-id="67061-286">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-286">Synchronous</span></span>** | <span data-ttu-id="67061-287">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-287">Yes</span></span> |  
| **<span data-ttu-id="67061-288">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-288">Bubbles</span></span>** | <span data-ttu-id="67061-289">Não</span><span class="sxs-lookup"><span data-stu-id="67061-289">No</span></span> |  
| **<span data-ttu-id="67061-290">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-290">Cancelable</span></span>** | <span data-ttu-id="67061-291">Não</span><span class="sxs-lookup"><span data-stu-id="67061-291">No</span></span> |  

### <span data-ttu-id="67061-292">MSWebViewNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="67061-292">MSWebViewNavigationCompleted</span></span>  

<span data-ttu-id="67061-293">Indica a conclusão da navegação, e todos os elementos de mídia são renderizados ou ocorreu um erro de navegação.</span><span class="sxs-lookup"><span data-stu-id="67061-293">Indicates the navigation is complete, and all media elements are rendered or there was a navigation error.</span></span>  <span data-ttu-id="67061-294">Verifique a Propriedade IsSuccess do Event args para saber se a navegação foi bem-sucedida e a propriedade webErrorStatus para obter detalhes sobre o erro de navegação.</span><span class="sxs-lookup"><span data-stu-id="67061-294">Check the event args isSuccess property to tell if the navigation was successful and the webErrorStatus property for details on the navigation error.</span></span>  <span data-ttu-id="67061-295">Erros de navegação podem ocorrer antes de obter qualquer conteúdo da rede por exemplo se o nome do host de um URI não resolver, caso contrário, o evento MSWebViewNavigationStarted será acionado seguido pelo evento MSWebViewNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="67061-295">Navigation errors can occur before obtaining any content from the network for instance if the hostname of a URI does not resolve in which case the MSWebViewNavigationStarted event will fire followed by the MSWebViewNavigationCompleted event.</span></span>  <span data-ttu-id="67061-296">Erros de navegação também podem ocorrer após receber uma página de erro de um servidor Web, por exemplo, uma página do 404 de um servidor HTTP, nesse caso, todos os eventos de navegação serão acionados, MSWebViewNavigationStarting, MSWebViewContentLoading, MSWebViewDOMContentLoaded e MSWebViewNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="67061-296">Navigation errors may also occur after receiving an error page from a web server, for instance a 404 page from an HTTP server in which case all navigation events will fire, MSWebViewNavigationStarting, MSWebViewContentLoading, MSWebViewDOMContentLoaded, and then MSWebViewNavigationCompleted.</span></span>  <span data-ttu-id="67061-297">Para fornecer uma página de erro de navegação do aplicativo para casos em que o servidor Web não forneceu uma página de erro, você precisará verificar se o MSWebViewContentLoading não foi disparado para uma navegação inexistente que indica que não há uma página de erro do servidor fornecida.</span><span class="sxs-lookup"><span data-stu-id="67061-297">To provide an app navigation error page for cases where the web server hasn't provided an error page, you'll need to check if MSWebViewContentLoading hasn't fired for a failed navigation which indicates there is no server provided error page.</span></span>  

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

#### <span data-ttu-id="67061-298">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-298">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-299">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-299">Interface</span></span>** | [<span data-ttu-id="67061-300">NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="67061-300">NavigationCompletedEvent</span></span>](./webview/NavigationCompletedEvent.md) |  
| **<span data-ttu-id="67061-301">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-301">Synchronous</span></span>** | <span data-ttu-id="67061-302">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-302">Yes</span></span> |  
| **<span data-ttu-id="67061-303">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-303">Bubbles</span></span>** | <span data-ttu-id="67061-304">Não</span><span class="sxs-lookup"><span data-stu-id="67061-304">No</span></span> |   
| **<span data-ttu-id="67061-305">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-305">Cancelable</span></span>** | <span data-ttu-id="67061-306">Não</span><span class="sxs-lookup"><span data-stu-id="67061-306">No</span></span> |  

### <span data-ttu-id="67061-307">MSWebViewNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="67061-307">MSWebViewNavigationStarting</span></span>  

<span data-ttu-id="67061-308">Indica que o **WebView** está começando a navegar.</span><span class="sxs-lookup"><span data-stu-id="67061-308">Indicates the **webview** is starting to navigate.</span></span>  <span data-ttu-id="67061-309">Isso é acionado antes da obtenção de recursos da rede para a navegação.</span><span class="sxs-lookup"><span data-stu-id="67061-309">This is fired before obtaining any resources from the network for the navigation.</span></span>  <span data-ttu-id="67061-310">A navegação não é iniciada até que todos os manipuladores de eventos MSWebViewNavigationStarting sejam concluídos.</span><span class="sxs-lookup"><span data-stu-id="67061-310">The navigation is not started until all MSWebViewNavigationStarting event handlers complete.</span></span>  <span data-ttu-id="67061-311">Esse evento é cancelável pela chamada `eventArgs.preventDefault()` .</span><span class="sxs-lookup"><span data-stu-id="67061-311">This event is cancellable via calling `eventArgs.preventDefault()`.</span></span>  <span data-ttu-id="67061-312">Se for cancelado, o WebView não executará a navegação.</span><span class="sxs-lookup"><span data-stu-id="67061-312">If cancelled, the WebView will not perform the navigation.</span></span>  

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

#### <span data-ttu-id="67061-313">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-313">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-314">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-314">Interface</span></span>** | [<span data-ttu-id="67061-315">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="67061-315">NavigationEvent</span></span>](./webview/NavigationEvent.md) |  
| **<span data-ttu-id="67061-316">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-316">Synchronous</span></span>** | <span data-ttu-id="67061-317">Não</span><span class="sxs-lookup"><span data-stu-id="67061-317">No</span></span> |  
| **<span data-ttu-id="67061-318">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-318">Bubbles</span></span>** | <span data-ttu-id="67061-319">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-319">Yes</span></span> |   
| **<span data-ttu-id="67061-320">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-320">Cancelable</span></span>** | <span data-ttu-id="67061-321">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-321">Yes</span></span> |  

### <span data-ttu-id="67061-322">MSWebViewNewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="67061-322">MSWebViewNewWindowRequested</span></span>  

<span data-ttu-id="67061-323">Gerado quando o conteúdo no **WebView** está tentando abrir uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="67061-323">Raised when content in **webview** is trying to open a new window.</span></span>  <span data-ttu-id="67061-324">Se o evento não for cancelado, o WebView iniciará o URI da nova solicitação de janela no navegador padrão do usuário.</span><span class="sxs-lookup"><span data-stu-id="67061-324">If the event isn't cancelled the webview will launch the URI of the new window request in the user's default browser.</span></span>  

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

#### <span data-ttu-id="67061-325">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-325">Event Information</span></span>  

|  |  |  
|:---|:--- |  
| **<span data-ttu-id="67061-326">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-326">Interface</span></span>** | [<span data-ttu-id="67061-327">NavigationEventWithReferrer</span><span class="sxs-lookup"><span data-stu-id="67061-327">NavigationEventWithReferrer</span></span>](./webview/NavigationEventWithReferrer.md) |  
| **<span data-ttu-id="67061-328">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-328">Synchronous</span></span>** | <span data-ttu-id="67061-329">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-329">Yes</span></span> |  
| **<span data-ttu-id="67061-330">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-330">Bubbles</span></span>** | <span data-ttu-id="67061-331">Não</span><span class="sxs-lookup"><span data-stu-id="67061-331">No</span></span> |  
| **<span data-ttu-id="67061-332">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-332">Cancelable</span></span>** | <span data-ttu-id="67061-333">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-333">Yes</span></span> |  

### <span data-ttu-id="67061-334">MSWebViewPermissionRequested</span><span class="sxs-lookup"><span data-stu-id="67061-334">MSWebViewPermissionRequested</span></span>  

<span data-ttu-id="67061-335">Indica que o conteúdo na **WebView** está tentando acessar a funcionalidade (como geolocalização ou acesso de bloqueio de ponteiro) que normalmente exige permissões de usuário final.</span><span class="sxs-lookup"><span data-stu-id="67061-335">Indicates that content in the **webview**  is trying to access functionality (such as geolocation, or pointer lock access) that normally requires end-user permissions.</span></span>  <span data-ttu-id="67061-336">Se nenhum manipulador de eventos estiver registrado ou se o manipulador de eventos não chamar eventArgs. permissionRequest. Allow (), Defer () ou Deny (), por padrão, a solicitação de permissão será negada.</span><span class="sxs-lookup"><span data-stu-id="67061-336">If no event handler is registered or if the event handler doesn't call eventArgs.permissionRequest.allow(), defer(), or deny(), then by default the permission request will be denied.</span></span>  <span data-ttu-id="67061-337">Se você precisar decidir se a permissão é permitida ou negada de forma assíncrona, por exemplo, se você precisar solicitar o usuário, use eventArgs. permissionRequest. Defer ().</span><span class="sxs-lookup"><span data-stu-id="67061-337">If you need to decide if permission is allowed or denied asynchronously for instance if you need to prompt the user, use eventArgs.permissionRequest.defer().</span></span>  <span data-ttu-id="67061-338">A solicitação de permissão será adiada até você usar WebView. getDeferredPermissionRequestById ou WebView. getDeferredPermissionRequests e chamar Allow () ou Deny () no DeferredPermissionRequest com o valor de ID correspondente.</span><span class="sxs-lookup"><span data-stu-id="67061-338">The permission request will be deferred until you use webview.getDeferredPermissionRequestById or webview.getDeferredPermissionRequests and call allow() or deny() on the DeferredPermissionRequest with the corresponding id value.</span></span>  

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

#### <span data-ttu-id="67061-339">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-339">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-340">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-340">Interface</span></span>** | [<span data-ttu-id="67061-341">PermissionRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="67061-341">PermissionRequestedEvent</span></span>](./webview/PermissionRequestedEvent.md) |  
| **<span data-ttu-id="67061-342">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-342">Synchronous</span></span>** | <span data-ttu-id="67061-343">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-343">Yes</span></span> |  
| **<span data-ttu-id="67061-344">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-344">Bubbles</span></span>** | <span data-ttu-id="67061-345">Não</span><span class="sxs-lookup"><span data-stu-id="67061-345">No</span></span> |   
| **<span data-ttu-id="67061-346">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-346">Cancelable</span></span>** | <span data-ttu-id="67061-347">Não</span><span class="sxs-lookup"><span data-stu-id="67061-347">No</span></span> |  

### <span data-ttu-id="67061-348">MSWebViewProcessExited</span><span class="sxs-lookup"><span data-stu-id="67061-348">MSWebViewProcessExited</span></span>  

<span data-ttu-id="67061-349">Indica que o processo de componente da **WebView** travou.</span><span class="sxs-lookup"><span data-stu-id="67061-349">Indicates that the **webview** component process crashsed.</span></span>  <span data-ttu-id="67061-350">Isso só é relevante para um WebView fora do processo.</span><span class="sxs-lookup"><span data-stu-id="67061-350">This is only relevant for an out-of-process WebView.</span></span>  <span data-ttu-id="67061-351">Consulte a seção de comentários sobre como criar uma WebView fora do processo, em oposição a uma WebView em processo.</span><span class="sxs-lookup"><span data-stu-id="67061-351">See the Remarks section for how to create an out-of-process WebView as opposed to an in-process WebView.</span></span>  <span data-ttu-id="67061-352">Depois que esse evento é acionado, o WebView correspondente é colocado em um estado de falha.</span><span class="sxs-lookup"><span data-stu-id="67061-352">After this event fires, the corresponding WebView is put into a crashed state.</span></span>  <span data-ttu-id="67061-353">Chamar a maioria dos métodos específicos do WebView ou acessar a maioria das propriedades específicas do WebView em uma WebView travada gerará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="67061-353">Calling most WebView specific methods or accessing most WebView specific properties on a crashed WebView will throw an exception.</span></span>  <span data-ttu-id="67061-354">Para recuperar esse evento, remova o WebView travado do DOM e substitua-o por um novo WebView.</span><span class="sxs-lookup"><span data-stu-id="67061-354">To recover from this event, remove the crashed WebView from the DOM and replace it with a new WebView.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewProcessExited", handler);
webview.removeEventListener("MSWebViewProcessExited", handler);
```  

#### <span data-ttu-id="67061-355">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-355">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-356">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-356">Interface</span></span>** | **<span data-ttu-id="67061-357">Evento</span><span class="sxs-lookup"><span data-stu-id="67061-357">Event</span></span>** |  
| **<span data-ttu-id="67061-358">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-358">Synchronous</span></span>** | <span data-ttu-id="67061-359">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-359">Yes</span></span> |  
| **<span data-ttu-id="67061-360">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-360">Bubbles</span></span>** | <span data-ttu-id="67061-361">Não</span><span class="sxs-lookup"><span data-stu-id="67061-361">No</span></span> |   
| **<span data-ttu-id="67061-362">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-362">Cancelable</span></span>** | <span data-ttu-id="67061-363">Não</span><span class="sxs-lookup"><span data-stu-id="67061-363">No</span></span> |  

### <span data-ttu-id="67061-364">MSWebViewWebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="67061-364">MSWebViewWebResourceRequested</span></span>  

<span data-ttu-id="67061-365">Gerado quando uma página dentro do elemento **WebView** solicita um recurso.</span><span class="sxs-lookup"><span data-stu-id="67061-365">Raised when a page inside the **webview** element requests a resource.</span></span>  

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

#### <span data-ttu-id="67061-366">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-366">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-367">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-367">Interface</span></span>** | [<span data-ttu-id="67061-368">WebResourceRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="67061-368">WebResourceRequestedEvent</span></span>](./webview/WebResourceRequestedEvent.md) |  
| **<span data-ttu-id="67061-369">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-369">Synchronous</span></span>** | <span data-ttu-id="67061-370">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-370">Yes</span></span> |  
| **<span data-ttu-id="67061-371">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-371">Bubbles</span></span>** | <span data-ttu-id="67061-372">Não</span><span class="sxs-lookup"><span data-stu-id="67061-372">No</span></span> |   
| **<span data-ttu-id="67061-373">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-373">Cancelable</span></span>** | <span data-ttu-id="67061-374">Não</span><span class="sxs-lookup"><span data-stu-id="67061-374">No</span></span> |  


### <span data-ttu-id="67061-375">MSWebViewScriptNotify</span><span class="sxs-lookup"><span data-stu-id="67061-375">MSWebViewScriptNotify</span></span>  

<span data-ttu-id="67061-376">Gerado quando uma página dentro do elemento **WebView** chama o método **Window. external. Notify** .</span><span class="sxs-lookup"><span data-stu-id="67061-376">Raised when a page inside the **webview** element calls the **window.external.notify** method.</span></span>  <span data-ttu-id="67061-377">O método window. external. Notify só está disponível para documentos com URIs que correspondam às regras no ApplicationContentUriRules de manifest's do aplicativo ou que tenha sido programaticamente permitido por meio da configuração de WebView. Settings. isScriptNotifyAllowed para true.</span><span class="sxs-lookup"><span data-stu-id="67061-377">The window.external.notify method is only available to documents with URIs that match rules in the app's manifest's ApplicationContentUriRules or that has been programatically allowed via setting webview.settings.isScriptNotifyAllowed to true.</span></span>  <span data-ttu-id="67061-378">Além disso, Window. external. Notify só está disponível para o documento de nível superior da WebView.</span><span class="sxs-lookup"><span data-stu-id="67061-378">Additionally window.external.notify is only available to the webview's top level document.</span></span>  

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

#### <span data-ttu-id="67061-379">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-379">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-380">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-380">Interface</span></span>** | [<span data-ttu-id="67061-381">ScriptNotifyEvent</span><span class="sxs-lookup"><span data-stu-id="67061-381">ScriptNotifyEvent</span></span>](./webview/ScriptNotifyEvent.md) |  
| **<span data-ttu-id="67061-382">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-382">Synchronous</span></span>** | <span data-ttu-id="67061-383">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-383">Yes</span></span> |  
| **<span data-ttu-id="67061-384">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-384">Bubbles</span></span>** | <span data-ttu-id="67061-385">Não</span><span class="sxs-lookup"><span data-stu-id="67061-385">No</span></span> |  
| **<span data-ttu-id="67061-386">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-386">Cancelable</span></span>** | <span data-ttu-id="67061-387">Não</span><span class="sxs-lookup"><span data-stu-id="67061-387">No</span></span> |  

### <span data-ttu-id="67061-388">MSWebViewUnsafeContentWarningDisplaying</span><span class="sxs-lookup"><span data-stu-id="67061-388">MSWebViewUnsafeContentWarningDisplaying</span></span>  

<span data-ttu-id="67061-389">Ocorre quando o **WebView** mostra uma página de aviso para o conteúdo que foi relatado como não seguro pelo filtro do SmartScreen.</span><span class="sxs-lookup"><span data-stu-id="67061-389">Occurs when the **webview** shows a warning page for content that was reported as unsafe by SmartScreen Filter.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
webview.removeEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
```  

#### <span data-ttu-id="67061-390">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-390">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-391">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-391">Interface</span></span>** | **<span data-ttu-id="67061-392">Evento</span><span class="sxs-lookup"><span data-stu-id="67061-392">Event</span></span>** |  
| **<span data-ttu-id="67061-393">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-393">Synchronous</span></span>** |<span data-ttu-id="67061-394">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-394">Yes</span></span> |  
| **<span data-ttu-id="67061-395">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-395">Bubbles</span></span>** |<span data-ttu-id="67061-396">Não</span><span class="sxs-lookup"><span data-stu-id="67061-396">No</span></span> |   
| **<span data-ttu-id="67061-397">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-397">Cancelable</span></span>** |<span data-ttu-id="67061-398">Não</span><span class="sxs-lookup"><span data-stu-id="67061-398">No</span></span> |  

### <span data-ttu-id="67061-399">MSWebViewUnsupportedUriSchemeIdentified</span><span class="sxs-lookup"><span data-stu-id="67061-399">MSWebViewUnsupportedUriSchemeIdentified</span></span>  

<span data-ttu-id="67061-400">Gerado quando há navegação para um URI (Uniform Resource Identifier) que o **WebView** não suporta.</span><span class="sxs-lookup"><span data-stu-id="67061-400">Raised when there is navigation to an Uniform Resource Identifier (URI) that the **webview** does not support.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
webview.removeEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
```  

#### <span data-ttu-id="67061-401">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-401">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-402">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-402">Interface</span></span>** | [<span data-ttu-id="67061-403">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="67061-403">NavigationEvent</span></span>](./webview/NavigationEvent.md) |  
| **<span data-ttu-id="67061-404">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-404">Synchronous</span></span>** | <span data-ttu-id="67061-405">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-405">Yes</span></span> |  
| **<span data-ttu-id="67061-406">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-406">Bubbles</span></span>** | <span data-ttu-id="67061-407">Não</span><span class="sxs-lookup"><span data-stu-id="67061-407">No</span></span> |  
| **<span data-ttu-id="67061-408">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-408">Cancelable</span></span>** | <span data-ttu-id="67061-409">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-409">Yes</span></span> |  

### <span data-ttu-id="67061-410">MSWebViewUnviewableContentIdentified</span><span class="sxs-lookup"><span data-stu-id="67061-410">MSWebViewUnviewableContentIdentified</span></span>  

<span data-ttu-id="67061-411">Gerado quando o **WebView** tenta navegar para conteúdo da Web com um tipo de conteúdo sem suporte.</span><span class="sxs-lookup"><span data-stu-id="67061-411">Raised when the **webview** attempts to navigate to web content with an unsupported content type.</span></span>  <span data-ttu-id="67061-412">Por exemplo, os PDFs atualmente não são compatíveis com a WebView e as navegações para documentos PDF não navegam e, em vez disso, geram esse evento.</span><span class="sxs-lookup"><span data-stu-id="67061-412">For example, PDFs are currently not supported by webview and navigations to PDF documents will not navigate and instead raise this event.</span></span>  

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

#### <span data-ttu-id="67061-413">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="67061-413">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-414">Interface</span><span class="sxs-lookup"><span data-stu-id="67061-414">Interface</span></span>** | [<span data-ttu-id="67061-415">UnviewableContentIdentifiedEvent</span><span class="sxs-lookup"><span data-stu-id="67061-415">UnviewableContentIdentifiedEvent</span></span>](./webview/UnviewableContentIdentifiedEvent.md) |  
| **<span data-ttu-id="67061-416">Síncrono</span><span class="sxs-lookup"><span data-stu-id="67061-416">Synchronous</span></span>** | <span data-ttu-id="67061-417">Sim</span><span class="sxs-lookup"><span data-stu-id="67061-417">Yes</span></span> |  
| **<span data-ttu-id="67061-418">Bolhas</span><span class="sxs-lookup"><span data-stu-id="67061-418">Bubbles</span></span>** | <span data-ttu-id="67061-419">Não</span><span class="sxs-lookup"><span data-stu-id="67061-419">No</span></span> |   
| **<span data-ttu-id="67061-420">Cela</span><span class="sxs-lookup"><span data-stu-id="67061-420">Cancelable</span></span>** | <span data-ttu-id="67061-421">Não</span><span class="sxs-lookup"><span data-stu-id="67061-421">No</span></span> |  

## <span data-ttu-id="67061-422">Métodos</span><span class="sxs-lookup"><span data-stu-id="67061-422">Methods</span></span>  

### <span data-ttu-id="67061-423">addWebAllowedObject</span><span class="sxs-lookup"><span data-stu-id="67061-423">addWebAllowedObject</span></span>  

<span data-ttu-id="67061-424">Adiciona um objeto do Windows Runtime nativo como um parâmetro global para o documento de nível superior dentro de um **WebView**.</span><span class="sxs-lookup"><span data-stu-id="67061-424">Adds a native Windows Runtime object as a global parameter to the top-level document inside of a **webview**.</span></span>  

<span data-ttu-id="67061-425">O objeto não é injetado no documento atual, mas sim o próximo documento de nível superior ao qual a WebView navega.</span><span class="sxs-lookup"><span data-stu-id="67061-425">The object is not injected into the current document, but rather the next top-level document to which the webview navigates.</span></span>  <span data-ttu-id="67061-426">O objeto é injetado antes que qualquer script do documento HTML seja executado para que você possa confiar no objeto no script global do seu documento.</span><span class="sxs-lookup"><span data-stu-id="67061-426">The object is injected before any script from the HTML document runs so you can rely on the object in your document's global script.</span></span>  

<span data-ttu-id="67061-427">Você deve usar addWebAllowedObject tanto durante um evento MSWebViewNavigationStarting ou antes de chamar explicitamente um método Navigate.</span><span class="sxs-lookup"><span data-stu-id="67061-427">You should use addWebAllowedObject either during an MSWebViewNavigationStarting event or before explicitly calling a navigate method.</span></span>  <span data-ttu-id="67061-428">Nesses casos, o objeto é injetado no documento da navegação correspondente.</span><span class="sxs-lookup"><span data-stu-id="67061-428">In these cases the object is injected into the document of the corresponding navigation.</span></span>  <span data-ttu-id="67061-429">Chamando-o em outro contexto, você não tem uma maneira de ter certeza de que documento vai injetar o objeto.</span><span class="sxs-lookup"><span data-stu-id="67061-429">Calling it in some other context, you don't have a way to be certain into what document you'll inject your object.</span></span>  

<span data-ttu-id="67061-430">Chamar addWebAllowedObject várias vezes em uma linha injetará vários objetos no documento.</span><span class="sxs-lookup"><span data-stu-id="67061-430">Calling addWebAllowedObject multiple times in a row will inject multiple objects into the document.</span></span>  <span data-ttu-id="67061-431">Se você chamá-lo antes de uma chamada de navegação explícita e, em seguida, novamente durante o evento MSWebViewNavigationStarting correspondente, as duas chamadas serão bem-sucedidas e você terá vários objetos injetados.</span><span class="sxs-lookup"><span data-stu-id="67061-431">If you call it both before an explicit navigate call and then again during the corresponding MSWebViewNavigationStarting event, both calls will succeed and you'll have multiple objects injected.</span></span>  <span data-ttu-id="67061-432">Se você chamar várias vezes com o mesmo parâmetro Name, a última chamada WINS e as chamadas anteriores com esse nome serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="67061-432">If you call multiple times with the same name parameter, the last call wins and the previous calls with that name are ignored.</span></span>  

<span data-ttu-id="67061-433">Se uma navegação falha ou é redirecionada, as chamadas addWebAllowedObject para essa navegação são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="67061-433">If a navigate fails or is redirected, the addWebAllowedObject calls for that navigation are ignored.</span></span>  <span data-ttu-id="67061-434">Se desejar manipular redirecionamentos, você pode assinar a inspeção de eventos MSWebViewNavigationStarting para redirecionar e chamar addWebAllowedObject novamente de acordo com qualquer critério apropriado para o seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67061-434">If you want to handle redirects you can subscribe to the MSWebViewNavigationStarting event watch for redirects and call addWebAllowedObject again according to whatever criteria is appropriate for your application.</span></span>  <span data-ttu-id="67061-435">Da mesma forma, quando um documento é acessado por todos os objetos injetados por meio do addWebAllowedObject para que o documento não seja transferido para o próximo documento, você precisará chamar explicitamente addWebAllowedObject se quiser que eles continuem.</span><span class="sxs-lookup"><span data-stu-id="67061-435">Similarly, once a document navigates away any objects injected via addWebAllowedObject for that document will not carry over to the next document and you'll need to explicitly call addWebAllowedObject if you want them to carry over.</span></span>  

<span data-ttu-id="67061-436">Se você chamar addWebAllowedObject para um documento que ainda não tem acesso ao WinRT, ou se tiver [acesso do AllowForWebOnly via ApplicationContentUriRules](/uwp/schemas/appxpackage/uapmanifestschema/element-uap-rule) , o objeto só será injetado se o objeto tiver o atributo Windows. Foundation. Metadata. AllowForWeb Metadata.</span><span class="sxs-lookup"><span data-stu-id="67061-436">If you call addWebAllowedObject for a document that has no WinRT access otherwise, or if it has [AllowForWebOnly access via ApplicationContentUriRules](/uwp/schemas/appxpackage/uapmanifestschema/element-uap-rule) then the object will only be injected if the object has the Windows.Foundation.Metadata.AllowForWeb metadata attribute.</span></span>  <span data-ttu-id="67061-437">Caso contrário, a injeção falhará e um erro será relatado ao console do desenvolvedor do JavaScript.</span><span class="sxs-lookup"><span data-stu-id="67061-437">Otherwise injection will fail and an error will be reported to the JavaScript developer console.</span></span>  <span data-ttu-id="67061-438">Se chamado em um documento com acesso completo ao WinRT, o objeto será injetado independentemente do atributo AllowForWeb.</span><span class="sxs-lookup"><span data-stu-id="67061-438">If called on a document that has full WinRT access, then the object will be injected regardless of the AllowForWeb attribute.</span></span>  

<span data-ttu-id="67061-439">Além disso, o objeto deve implementar a interface IAgileObject.</span><span class="sxs-lookup"><span data-stu-id="67061-439">Additionally, the object must implement the IAgileObject interface.</span></span>  <span data-ttu-id="67061-440">Isso ocorre porque os elementos XAML e HTML da WebView executados em seus threads de exibição do aplicativo do ASTA e o thread JavaScript da WebView são um thread ASTA diferente e queremos incentivar os desenvolvedores de aplicativos a garantir que o objeto possa ser executado no thread JavaScript sem bloquear o thread de exibição do aplicativo, se possível.</span><span class="sxs-lookup"><span data-stu-id="67061-440">This is because the XAML and HTML webview elements run on their app's ASTA view threads and the WebView's JavaScript thread is a different ASTA thread and we want to encourage app developers to ensure their object can run on the JavaScript thread without blocking the app view thread if possible.</span></span>  

<span data-ttu-id="67061-441">O parâmetro Name deve ser um nome de propriedade JavaScript válido, caso contrário, a chamada falhará silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="67061-441">The name parameter must be a valid JavaScript property name otherwise the call will fail silently.</span></span>  <span data-ttu-id="67061-442">Se o nome for de uma propriedade que já existe no objeto global, essa propriedade será sobrescrita se a propriedade for configurável.</span><span class="sxs-lookup"><span data-stu-id="67061-442">If the name is of a property that already exists on the global object then that property is overwritten if the property is configurable.</span></span>  <span data-ttu-id="67061-443">As propriedades não configuráveis no objeto global não são sobrescritas e a chamada addWebAllowedObject falha silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="67061-443">Non-configurable properties on the global object are not overwritten and the addWebAllowedObject call fails silently.</span></span>  <span data-ttu-id="67061-444">As propriedades de JavaScript criadas via addWebAllowedObject são graváveis, configuráveis e enumeráveis.</span><span class="sxs-lookup"><span data-stu-id="67061-444">JavaScript properties created via addWebAllowedObject are writable, configurable, and enumerable.</span></span>  

```javascript
let name = "exampleProperty";
webview.addWebAllowedObject(name, applicationObject);
webview.navigate("https://example.com/"); // applicationObject will be available as window.exampleProperty on https://example.com
```  

#### <span data-ttu-id="67061-445">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67061-445">Parameters</span></span>  

*<span data-ttu-id="67061-446">name</span><span class="sxs-lookup"><span data-stu-id="67061-446">name</span></span>*  

*   <span data-ttu-id="67061-447">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67061-447">Type: **String**</span></span>  
*   <span data-ttu-id="67061-448">O nome do objeto que será exposto ao documento no **WebView**.</span><span class="sxs-lookup"><span data-stu-id="67061-448">The name of the object to expose to the document in the **webview**.</span></span>  

*<span data-ttu-id="67061-449">applicationObject</span><span class="sxs-lookup"><span data-stu-id="67061-449">applicationObject</span></span>*  

*   <span data-ttu-id="67061-450">Tipo: **objeto**</span><span class="sxs-lookup"><span data-stu-id="67061-450">Type: **Object**</span></span>  
*   <span data-ttu-id="67061-451">O objeto a ser exposto ao documento no **WebView**.</span><span class="sxs-lookup"><span data-stu-id="67061-451">The object to expose to the document in the **webview**.</span></span>  

#### <span data-ttu-id="67061-452">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67061-452">Return value</span></span>  

<span data-ttu-id="67061-453">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="67061-453">This method does not return a value.</span></span>  

#### <span data-ttu-id="67061-454">Recursos e requisitos adicionais</span><span class="sxs-lookup"><span data-stu-id="67061-454">Additional features and requirements</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-455">Mínimo de cliente com suporte</span><span class="sxs-lookup"><span data-stu-id="67061-455">Minimum supported client</span></span>** | <span data-ttu-id="67061-456">Windows10 (somente aplicativos da Windows Store)</span><span class="sxs-lookup"><span data-stu-id="67061-456">Windows10 (Windows Store apps only)</span></span> |    
| **<span data-ttu-id="67061-457">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67061-457">Minimum supported server</span></span>** | <span data-ttu-id="67061-458">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="67061-458">None supported</span></span> |   
| **<span data-ttu-id="67061-459">Número mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67061-459">Minimum supported phone</span></span>** | <span data-ttu-id="67061-460">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="67061-460">None supported</span></span> |  

### <span data-ttu-id="67061-461">buildLocalStreamUri</span><span class="sxs-lookup"><span data-stu-id="67061-461">buildLocalStreamUri</span></span>  

<span data-ttu-id="67061-462">Cria um URI que você pode passar para [navigateToLocalStreamUri](#methods).</span><span class="sxs-lookup"><span data-stu-id="67061-462">Creates a URI that you can pass to [navigateToLocalStreamUri](#methods).</span></span>  

```javascript
var string = webview.buildLocalStreamUri(contentIdentifier, relativePath);
```  

#### <span data-ttu-id="67061-463">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67061-463">Parameters</span></span>  

*<span data-ttu-id="67061-464">contentIdentifier</span><span class="sxs-lookup"><span data-stu-id="67061-464">contentIdentifier</span></span>*  

*   <span data-ttu-id="67061-465">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67061-465">Type: **String**</span></span>  
*   <span data-ttu-id="67061-466">Um identificador exclusivo para o conteúdo ao qual o URI faz referência.</span><span class="sxs-lookup"><span data-stu-id="67061-466">A unique identifier for the content the URI is referencing.</span></span>  <span data-ttu-id="67061-467">Isso define a raiz do URI.</span><span class="sxs-lookup"><span data-stu-id="67061-467">This defines the root of the URI.</span></span>  

*<span data-ttu-id="67061-468">relativePath</span><span class="sxs-lookup"><span data-stu-id="67061-468">relativePath</span></span>*  

*  <span data-ttu-id="67061-469">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67061-469">Type: **String**</span></span>  
*  <span data-ttu-id="67061-470">O caminho do recurso, relativo à raiz.</span><span class="sxs-lookup"><span data-stu-id="67061-470">The path to the resource, relative to the root.</span></span>  

#### <span data-ttu-id="67061-471">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67061-471">Return value</span></span>  

<span data-ttu-id="67061-472">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67061-472">Type: **String**</span></span>  

<span data-ttu-id="67061-473">O URI criado combinando e normalizando o *contentIdentifier* e o *RelativePath*.</span><span class="sxs-lookup"><span data-stu-id="67061-473">The URI created by combining and normalizing the *contentIdentifier* and *relativePath*.</span></span>  

#### <span data-ttu-id="67061-474">Exemplo</span><span class="sxs-lookup"><span data-stu-id="67061-474">Example</span></span>  

<span data-ttu-id="67061-475">O exemplo a seguir ilustra um caso de uso típico.</span><span class="sxs-lookup"><span data-stu-id="67061-475">The following example illustrates a typical use case.</span></span>  

```javascript
var webview = document.createElement("x-ms-webview"); //Instantiate the webview element
var localStreamUri = webview.buildLocalStreamUri(contentIdentifier, relativePath); //Create URI to pass to navigateToLocalStreamUri method
webview.navigateToLocalStreamUri(localStreamUri, streamResolver); //Load the local web content 
```  

### <span data-ttu-id="67061-476">capturePreviewToBlobAsync</span><span class="sxs-lookup"><span data-stu-id="67061-476">capturePreviewToBlobAsync</span></span>  

<span data-ttu-id="67061-477">Cria uma imagem do [elemento WebView](./webview.md) atual e a escreve no elemento Image especificado.</span><span class="sxs-lookup"><span data-stu-id="67061-477">Creates an image of the current [webview element](./webview.md) and write it to the specified image element.</span></span>  

```javascript
var capturePreviewToBlobAsync = webview.capturePreviewToBlobAsync();
```  

#### <span data-ttu-id="67061-478">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67061-478">Parameters</span></span>  

<span data-ttu-id="67061-479">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="67061-479">This method has no parameters.</span></span>  

#### <span data-ttu-id="67061-480">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67061-480">Return value</span></span>  

<span data-ttu-id="67061-481">Tipo: **MSWebViewAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="67061-481">Type: **MSWebViewAsyncOperation**</span></span>  

<span data-ttu-id="67061-482">Um objeto **MSWebViewAsyncOperation** que, quando concluído, fornece um objeto **blob** que contém a imagem.</span><span class="sxs-lookup"><span data-stu-id="67061-482">An **MSWebViewAsyncOperation** object that, when it completes, provides a **Blob** object that contains the image.</span></span>  <span data-ttu-id="67061-483">Ao usar **capturePreviewToBlobAsync**, você precisa definir manipuladores de êxito e erros após definir a operação.</span><span class="sxs-lookup"><span data-stu-id="67061-483">When using **capturePreviewToBlobAsync**, you need to define success and error handlers after defining the operation.</span></span>  <span data-ttu-id="67061-484">Após a aplicação dos manipuladores de eventos, chame o método Start no objeto [MSWebViewAsyncOperation](./webview/MSWebViewAsyncOperation.md) para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="67061-484">After applying the event handlers, call the start method on the [MSWebViewAsyncOperation](./webview/MSWebViewAsyncOperation.md) object to execute the operation.</span></span>  

### <span data-ttu-id="67061-485">captureSelectedContentToDataPackageAsync</span><span class="sxs-lookup"><span data-stu-id="67061-485">captureSelectedContentToDataPackageAsync</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="67061-486">Esse método foi preterido e tem um problema conhecido.</span><span class="sxs-lookup"><span data-stu-id="67061-486">This method has been deprecated and has a known issue.</span></span>  <span data-ttu-id="67061-487">Evite usar esse método em seu código de produção.</span><span class="sxs-lookup"><span data-stu-id="67061-487">Avoid using this method in your production code.</span></span>  

<span data-ttu-id="67061-488">Assincronamente Obtém um [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) que contém o conteúdo selecionado no **WebView**.</span><span class="sxs-lookup"><span data-stu-id="67061-488">Asynchronously gets a [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) that contains the selected content within the **webview**.</span></span>  

```javascript
var msWebViewAsyncOperation = webview.captureSelectedContentToDataPackageAsync();
```  

#### <span data-ttu-id="67061-489">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67061-489">Parameters</span></span>  

<span data-ttu-id="67061-490">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="67061-490">This method has no parameters.</span></span>  

#### <span data-ttu-id="67061-491">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67061-491">Return value</span></span>  

<span data-ttu-id="67061-492">Tipo: **MSWebViewAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="67061-492">Type: **MSWebViewAsyncOperation**</span></span>  

<span data-ttu-id="67061-493">Um objeto **MSWebViewAsyncOperation** que, quando concluído, fornece um objeto [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) que contém a imagem.</span><span class="sxs-lookup"><span data-stu-id="67061-493">An **MSWebViewAsyncOperation** object that, when it completes, provides a [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) object that contains the image.</span></span>  <span data-ttu-id="67061-494">Ao usar **captureSelectedContentToDataPackageAsync**, você precisa definir manipuladores de êxito e erros após definir a operação.</span><span class="sxs-lookup"><span data-stu-id="67061-494">When using **captureSelectedContentToDataPackageAsync**, you need to define success and error handlers after defining the operation.</span></span>  <span data-ttu-id="67061-495">Após a aplicação dos manipuladores de eventos, chame o método Start no objeto MSWebViewAsyncOperation para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="67061-495">After applying the event handlers, call the start method on the MSWebViewAsyncOperation object to execute the operation.</span></span>  

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

### <span data-ttu-id="67061-496">invokeScriptAsync</span><span class="sxs-lookup"><span data-stu-id="67061-496">invokeScriptAsync</span></span>  

<span data-ttu-id="67061-497">Como uma ação assíncrona, executa a função de script especificada do HTML atualmente carregado, com argumentos específicos.</span><span class="sxs-lookup"><span data-stu-id="67061-497">As an asynchronous action, executes the specified script function from the currently loaded HTML, with specific arguments.</span></span>  

```javascript
webview.invokeScriptAsync(functionName, ...args)
```  

#### <span data-ttu-id="67061-498">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67061-498">Parameters</span></span>  

**<span data-ttu-id="67061-499">função FunctionName</span><span class="sxs-lookup"><span data-stu-id="67061-499">functionName</span></span>**  

*   <span data-ttu-id="67061-500">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67061-500">Type: **String**</span></span>  
*   <span data-ttu-id="67061-501">O nome da função a ser invocada.</span><span class="sxs-lookup"><span data-stu-id="67061-501">The name of the function to invoke.</span></span>  <span data-ttu-id="67061-502">Esse é um nome de propriedade no objeto da janela global do documento de nível superior da WebView.</span><span class="sxs-lookup"><span data-stu-id="67061-502">This is a property name on the global window object of the WebView's top level document.</span></span>  <span data-ttu-id="67061-503">Pode ser uma função global interna, como eval ou Open, ou pode ser uma função definida pelo script no objeto da janela global.</span><span class="sxs-lookup"><span data-stu-id="67061-503">This can be a built-in global function like eval or open, or it can be a script defined function on the global window object.</span></span>  <span data-ttu-id="67061-504">Somente funções no documento de nível superior do WebView podem ser invocadas.</span><span class="sxs-lookup"><span data-stu-id="67061-504">Only functions in the top level document of the WebView may be invoked.</span></span>  

**<span data-ttu-id="67061-505">args</span><span class="sxs-lookup"><span data-stu-id="67061-505">args</span></span>**  

*   <span data-ttu-id="67061-506">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67061-506">Type: **String**</span></span>  
*   <span data-ttu-id="67061-507">Parâmetros de cadeia de caracteres opcionais para passar para a função invocada.</span><span class="sxs-lookup"><span data-stu-id="67061-507">Optional string parameters to pass to the invoked function.</span></span>  <span data-ttu-id="67061-508">Após FunctionName, os parâmetros adicionais para invokeScriptAsync são cadeias de caracteres transferidas para a função invocada.</span><span class="sxs-lookup"><span data-stu-id="67061-508">After functionName, any additional parameters to invokeScriptAsync are strings passed to the invoked function.</span></span>  

#### <span data-ttu-id="67061-509">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67061-509">Return value</span></span>  

<span data-ttu-id="67061-510">Tipo: **MSWebViewAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="67061-510">Type: **MSWebViewAsyncOperation**</span></span>  

<span data-ttu-id="67061-511">Ao usar **invokeScriptAsync**, você precisa definir manipuladores de êxito e erros após definir a operação.</span><span class="sxs-lookup"><span data-stu-id="67061-511">When using **invokeScriptAsync**, you need to define success and error handlers after defining the operation.</span></span>  <span data-ttu-id="67061-512">Após a aplicação dos manipuladores de eventos, chame **MSWebViewAsyncOperation. Start** para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="67061-512">After applying the event handlers, call **MSWebViewAsyncOperation.start** to execute the operation.</span></span>  <span data-ttu-id="67061-513">Se o evento complete MSWebViewAsyncOperation for acionado, a propriedade Result do MSWebViewAsyncOperation será o valor de retorno da cadeia de caracteres para invocar a função.</span><span class="sxs-lookup"><span data-stu-id="67061-513">If the MSWebViewAsyncOperation's complete event fires then the MSWebViewAsyncOperation's result property is the string return value from invoking the function.</span></span>  <span data-ttu-id="67061-514">Usar o valor de retorno da função invocada permite que o conteúdo da WebView faça a comunicação de modo síncrono para o host da WebView.</span><span class="sxs-lookup"><span data-stu-id="67061-514">Using the invoked function's return value allows for the WebView content to communication synchronously back to the WebView host.</span></span>  <span data-ttu-id="67061-515">Para fazer com que o conteúdo da WebView se comunique de forma assíncrona ao host da WebView, consulte o evento MSWebViewScriptNotify.</span><span class="sxs-lookup"><span data-stu-id="67061-515">To instead have the WebView content communicate asynchronously back to the WebView host see the MSWebViewScriptNotify event.</span></span>  <span data-ttu-id="67061-516">Se a função invocada lançar uma exceção não tratada, o evento de erro do MSWebViewAsyncOperation será acionado.</span><span class="sxs-lookup"><span data-stu-id="67061-516">If the function invoked throws an unhandled exception then the MSWebViewAsyncOperation's error event will fire.</span></span>  

```javascript
const functionName = "eval";
const args = ["'Current URL: ' + document.location.href"];

const asyncOp = webview.invokeScriptAsync(functionName, ...args);

asyncOp.onerror = () => console.error("Error: " + asyncOp.error);
asyncOp.oncomplete = () => console.log("Result: " + asyncOp.result); // Logs 'Current URL: about:blank'
asyncOp.start();
```  

### <span data-ttu-id="67061-517">getDeferredPermissionRequests</span><span class="sxs-lookup"><span data-stu-id="67061-517">getDeferredPermissionRequests</span></span>  

<span data-ttu-id="67061-518">Retorna uma lista de solicitações de permissão adiadas emitidas pelo conteúdo no controle **WebView** .</span><span class="sxs-lookup"><span data-stu-id="67061-518">Returns a list of deferred permission requests issued by content in the **webview** control.</span></span>  

```javascript
var sequence<PermissionRequest> = x-ms-webview.getDeferredPermissionRequests();
```  

#### <span data-ttu-id="67061-519">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67061-519">Parameters</span></span>  

<span data-ttu-id="67061-520">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="67061-520">This method has no parameters.</span></span>  

#### <span data-ttu-id="67061-521">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67061-521">Return value</span></span>  

<span data-ttu-id="67061-522">Tipo: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span><span class="sxs-lookup"><span data-stu-id="67061-522">Type: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span></span>  

<span data-ttu-id="67061-523">A solicitação de permissão adiada especificada.</span><span class="sxs-lookup"><span data-stu-id="67061-523">The specified deferred permission request.</span></span>  

#### <span data-ttu-id="67061-524">Recursos e requisitos adicionais</span><span class="sxs-lookup"><span data-stu-id="67061-524">Additional features and requirements</span></span>  

|  | |  
|:--- |:--- |  
| **<span data-ttu-id="67061-525">Mínimo de cliente com suporte</span><span class="sxs-lookup"><span data-stu-id="67061-525">Minimum supported client</span></span>** | <span data-ttu-id="67061-526">Windows10 (somente aplicativos da Windows Store)</span><span class="sxs-lookup"><span data-stu-id="67061-526">Windows10 (Windows Store apps only)</span></span> |  
| **<span data-ttu-id="67061-527">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67061-527">Minimum supported server</span></span>** | <span data-ttu-id="67061-528">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="67061-528">None supported</span></span> |  
| **<span data-ttu-id="67061-529">Número mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67061-529">Minimum supported phone</span></span>** | <span data-ttu-id="67061-530">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="67061-530">None supported</span></span> |  


### <span data-ttu-id="67061-531">getDeferredPermissionRequestById</span><span class="sxs-lookup"><span data-stu-id="67061-531">getDeferredPermissionRequestById</span></span>  

<span data-ttu-id="67061-532">Retorna a solicitação de permissão adiada especificada.</span><span class="sxs-lookup"><span data-stu-id="67061-532">Returns the specified deferred permission request.</span></span>  

```javascript
var deferredPermissionRequest = x-ms-webview.getDeferredPermissionRequestById(id);
```  

#### <span data-ttu-id="67061-533">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67061-533">Parameters</span></span>  

*<span data-ttu-id="67061-534">id</span><span class="sxs-lookup"><span data-stu-id="67061-534">id</span></span>*  

*   <span data-ttu-id="67061-535">Tipo: **unsigned long**</span><span class="sxs-lookup"><span data-stu-id="67061-535">Type: **unsigned long**</span></span>  
*   <span data-ttu-id="67061-536">A ID da solicitação de permissão adiada que você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="67061-536">The ID of the deferred permission request you wish to get.</span></span>  

#### <span data-ttu-id="67061-537">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67061-537">Return value</span></span>  

<span data-ttu-id="67061-538">Tipo: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span><span class="sxs-lookup"><span data-stu-id="67061-538">Type: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span></span>  

<span data-ttu-id="67061-539">A solicitação de permissão adiada especificada.</span><span class="sxs-lookup"><span data-stu-id="67061-539">The specified deferred permission request.</span></span>  

#### <span data-ttu-id="67061-540">Recursos e requisitos adicionais</span><span class="sxs-lookup"><span data-stu-id="67061-540">Additional features and requirements</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="67061-541">Mínimo de cliente com suporte</span><span class="sxs-lookup"><span data-stu-id="67061-541">Minimum supported client</span></span>** | <span data-ttu-id="67061-542">Windows10 (somente aplicativos da Windows Store)</span><span class="sxs-lookup"><span data-stu-id="67061-542">Windows10 (Windows Store apps only)</span></span> |  
| **<span data-ttu-id="67061-543">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67061-543">Minimum supported server</span></span>** | <span data-ttu-id="67061-544">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="67061-544">None supported</span></span> |  
| **<span data-ttu-id="67061-545">Número mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67061-545">Minimum supported phone</span></span>** | <span data-ttu-id="67061-546">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="67061-546">None supported</span></span> |  

### <span data-ttu-id="67061-547">goBack</span><span class="sxs-lookup"><span data-stu-id="67061-547">goBack</span></span>  

<span data-ttu-id="67061-548">Navega o **WebView** para a página anterior no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="67061-548">Navigates the **webview** to the previous page in the navigation history.</span></span>  

```javascript
webview.goBack();
```  

#### <span data-ttu-id="67061-549">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67061-549">Parameters</span></span>  

<span data-ttu-id="67061-550">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="67061-550">This method has no parameters.</span></span>  

#### <span data-ttu-id="67061-551">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67061-551">Return value</span></span>  

<span data-ttu-id="67061-552">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="67061-552">This method does not return a value.</span></span>  

### <span data-ttu-id="67061-553">goForward</span><span class="sxs-lookup"><span data-stu-id="67061-553">goForward</span></span>  

<span data-ttu-id="67061-554">Navega o **WebView** para a próxima página no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="67061-554">Navigates the **webview** to the next page in the navigation history.</span></span>  

```javascript
webview.goForward();
```  

#### <span data-ttu-id="67061-555">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67061-555">Parameters</span></span>  

<span data-ttu-id="67061-556">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="67061-556">This method has no parameters.</span></span>  

#### <span data-ttu-id="67061-557">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67061-557">Return value</span></span>  

<span data-ttu-id="67061-558">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="67061-558">This method does not return a value.</span></span>  

### <span data-ttu-id="67061-559">navegar</span><span class="sxs-lookup"><span data-stu-id="67061-559">navigate</span></span>  

<span data-ttu-id="67061-560">Carrega o conteúdo HTML no URI (Uniform Resource Identifier) especificado.</span><span class="sxs-lookup"><span data-stu-id="67061-560">Loads the HTML content at the specified Uniform Resource Identifier (URI).</span></span>  

```javascript
webview.navigate(uri);
```  

#### <span data-ttu-id="67061-561">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67061-561">Parameters</span></span>  

**<span data-ttu-id="67061-562">uri</span><span class="sxs-lookup"><span data-stu-id="67061-562">uri</span></span>**  

*   <span data-ttu-id="67061-563">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67061-563">Type: **String**</span></span>  
*   <span data-ttu-id="67061-564">O URI a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="67061-564">The URI to load.</span></span>  

#### <span data-ttu-id="67061-565">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67061-565">Return value</span></span>  

<span data-ttu-id="67061-566">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="67061-566">This method does not return a value.</span></span>  

### <span data-ttu-id="67061-567">navigateFocus</span><span class="sxs-lookup"><span data-stu-id="67061-567">navigateFocus</span></span>  

<span data-ttu-id="67061-568">Navega no foco para o **WebView**.</span><span class="sxs-lookup"><span data-stu-id="67061-568">Navigates focus onto the **webview**.</span></span>  <span data-ttu-id="67061-569">Dispara o evento window's navigatingfocus do documento de nível superior da WebView.</span><span class="sxs-lookup"><span data-stu-id="67061-569">Fires the webview's top level document's window's navigatingfocus event.</span></span>  <span data-ttu-id="67061-570">Os args FocusNavigationEvent usados no evento navigatingfocus correspondem aos parâmetros fornecidos para navigateFocus, exceto os parâmetros de origem são convertidos do espaço de coordenadas do documento host para o espaço de coordenadas do documento de nível superior da WebView.</span><span class="sxs-lookup"><span data-stu-id="67061-570">The FocusNavigationEvent args used in the navigatingfocus event match the parameters provided to navigateFocus except the origin parameters are translated from the host document's coordinate space to the coordinate space of the webview's top level document.</span></span>  <span data-ttu-id="67061-571">Consulte o evento WebView departingFocus e o método window. departFocus correspondente para transferir o foco do WebView para o host.</span><span class="sxs-lookup"><span data-stu-id="67061-571">See the webview departingFocus event and corresponding window.departFocus method for transferring focus from the webview to the host.</span></span>  <span data-ttu-id="67061-572">Consulte a [biblioteca de navegação de direção do TVJS](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) para obter um exemplo de implementação de navegação de foco via teclado ou gamepad que usa esse método.</span><span class="sxs-lookup"><span data-stu-id="67061-572">See the [TVJS's Direction Navigation library](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) for an example of an implementation of focus navigation via keyboard or gamepad that uses this method.</span></span>  

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

#### <span data-ttu-id="67061-573">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67061-573">Parameters</span></span>  

*<span data-ttu-id="67061-574">navigationReason</span><span class="sxs-lookup"><span data-stu-id="67061-574">navigationReason</span></span>*  

*   <span data-ttu-id="67061-575">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67061-575">Type: **String**</span></span>  
*   <span data-ttu-id="67061-576">O motivo da navegação.</span><span class="sxs-lookup"><span data-stu-id="67061-576">The reason for the navigation.</span></span>  <span data-ttu-id="67061-577">O valor deve ser "Left", "up", "Right" ou "Down".</span><span class="sxs-lookup"><span data-stu-id="67061-577">The value should be either "left", "up", "right", or "down".</span></span>  <span data-ttu-id="67061-578">É a direção em que o foco está se afastando do elemento atualmente focalizado.</span><span class="sxs-lookup"><span data-stu-id="67061-578">It is the direction in which focus is moving away from the currently focused element.</span></span>  

*<span data-ttu-id="67061-579">Origin</span><span class="sxs-lookup"><span data-stu-id="67061-579">origin</span></span>*  

*   <span data-ttu-id="67061-580">Tipo: **objeto**</span><span class="sxs-lookup"><span data-stu-id="67061-580">Type: **Object**</span></span>  
*   <span data-ttu-id="67061-581">A origem da navegação.</span><span class="sxs-lookup"><span data-stu-id="67061-581">The origin of the navigation.</span></span>  <span data-ttu-id="67061-582">Este é um objeto JavaScript com propriedades "originLeft", "originTop", "originWidth" e "originHeight".</span><span class="sxs-lookup"><span data-stu-id="67061-582">This is a JavaScript object with properties "originLeft", "originTop", "originWidth", and "originHeight".</span></span>  <span data-ttu-id="67061-583">Esses valores devem descrever a posição e o tamanho do elemento focalizado no momento, longe do qual o foco está sendo movido.</span><span class="sxs-lookup"><span data-stu-id="67061-583">These values should describe the position and size of the currently focused element away from which focus is moving.</span></span>  

#### <span data-ttu-id="67061-584">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67061-584">Return value</span></span>  

<span data-ttu-id="67061-585">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="67061-585">This method does not return a value.</span></span>  

### <span data-ttu-id="67061-586">navigateToLocalStreamUri</span><span class="sxs-lookup"><span data-stu-id="67061-586">navigateToLocalStreamUri</span></span>  

<span data-ttu-id="67061-587">Carrega o conteúdo da Web local no URI especificado usando um [**UriToStreamResolver**](/uwp/api/windows.web.iuritostreamresolver.uritostreamasync).</span><span class="sxs-lookup"><span data-stu-id="67061-587">Loads local web content at the specified URI using a [**UriToStreamResolver**](/uwp/api/windows.web.iuritostreamresolver.uritostreamasync).</span></span>  

```javascript
webview.navigateToLocalStreamUri(source, streamResolver); 
```  

#### <span data-ttu-id="67061-588">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67061-588">Parameters</span></span>  

*<span data-ttu-id="67061-589">bibliográfica</span><span class="sxs-lookup"><span data-stu-id="67061-589">source</span></span>*  

*   <span data-ttu-id="67061-590">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67061-590">Type: **String**</span></span>  
*   <span data-ttu-id="67061-591">Um URI MS-local-Stream que identifica o conteúdo HTML local a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="67061-591">An ms-local-stream URI identifying the local HTML content to load.</span></span>  <span data-ttu-id="67061-592">Crie esta cadeia de caracteres usando [**buildLocalStreamUri**](/uwp/api/windows.web.ui.iwebviewcontrol.buildlocalstreamuri).</span><span class="sxs-lookup"><span data-stu-id="67061-592">Create this string using [**buildLocalStreamUri**](/uwp/api/windows.web.ui.iwebviewcontrol.buildlocalstreamuri).</span></span>  

*<span data-ttu-id="67061-593">streamResolver</span><span class="sxs-lookup"><span data-stu-id="67061-593">streamResolver</span></span>*  

*   <span data-ttu-id="67061-594">Tipo: qualquer</span><span class="sxs-lookup"><span data-stu-id="67061-594">Type: any</span></span>  
*   <span data-ttu-id="67061-595">Um resolvedor que converte o URI em um fluxo para carregar.</span><span class="sxs-lookup"><span data-stu-id="67061-595">A resolver that converts the URI into a stream to load.</span></span>  

#### <span data-ttu-id="67061-596">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67061-596">Return value</span></span>  

<span data-ttu-id="67061-597">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="67061-597">This method does not return a value.</span></span>  

### <span data-ttu-id="67061-598">navigateToString</span><span class="sxs-lookup"><span data-stu-id="67061-598">navigateToString</span></span>  

<span data-ttu-id="67061-599">Carrega o conteúdo HTML especificado como um novo documento.</span><span class="sxs-lookup"><span data-stu-id="67061-599">Loads the specified HTML content as a new document.</span></span>  

```javascript
webview.navigateToString(contents);
```  

#### <span data-ttu-id="67061-600">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67061-600">Parameters</span></span>  

*<span data-ttu-id="67061-601">conteúdos</span><span class="sxs-lookup"><span data-stu-id="67061-601">contents</span></span>*  

*   <span data-ttu-id="67061-602">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67061-602">Type: **String**</span></span>  
*   <span data-ttu-id="67061-603">O conteúdo HTML a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="67061-603">The HTML content to display.</span></span>  

#### <span data-ttu-id="67061-604">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67061-604">Return value</span></span>  

<span data-ttu-id="67061-605">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="67061-605">This method does not return a value.</span></span>  

### <span data-ttu-id="67061-606">navigateWithHttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="67061-606">navigateWithHttpRequestMessage</span></span>  

<span data-ttu-id="67061-607">Navega o WebView para um URI (Uniform Resource Identifier) com uma solicitação POST e cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="67061-607">Navigates the webview to a Uniform Resource Identifier (URI) with a POST request and HTTP headers.</span></span>  

```javascript
webview.navigateWithHttpRequestMessage(requestMessage);
```  

#### <span data-ttu-id="67061-608">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67061-608">Parameters</span></span>  

*<span data-ttu-id="67061-609">requestMessage</span><span class="sxs-lookup"><span data-stu-id="67061-609">requestMessage</span></span>*  

*   <span data-ttu-id="67061-610">Tipo: **HttpRequestMessage**</span><span class="sxs-lookup"><span data-stu-id="67061-610">Type: **HttpRequestMessage**</span></span>  
*   <span data-ttu-id="67061-611">Os detalhes da solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="67061-611">The details of the HTTP request.</span></span>  

#### <span data-ttu-id="67061-612">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67061-612">Return value</span></span>  

<span data-ttu-id="67061-613">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="67061-613">This method does not return a value.</span></span>  

#### <span data-ttu-id="67061-614">Comentários</span><span class="sxs-lookup"><span data-stu-id="67061-614">Remarks</span></span>  

> [!WARNING]
> <span data-ttu-id="67061-615">Se você adicionar mais cabeçalhos a essa solicitação, como credenciais de autenticação, lembre-se de que esses cabeçalhos também serão incluídos em quaisquer solicitações filho subsequentes.</span><span class="sxs-lookup"><span data-stu-id="67061-615">If you add additional headers to this request, such as authentication credentials, remember that those headers will also be included with any subsequent child requests.</span></span>  <span data-ttu-id="67061-616">Tenha cuidado para evitar a divulgação acidental de informações confidenciais ou pessoais.</span><span class="sxs-lookup"><span data-stu-id="67061-616">Use caution to prevent accidental disclosure of confidential or personal information.</span></span>  

### <span data-ttu-id="67061-617">Atualize</span><span class="sxs-lookup"><span data-stu-id="67061-617">refresh</span></span>  

<span data-ttu-id="67061-618">Recarrega o conteúdo atual no **WebView**.</span><span class="sxs-lookup"><span data-stu-id="67061-618">Reloads the current content in the **webview**.</span></span>  

```javascript
webview.refresh();
```  

#### <span data-ttu-id="67061-619">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67061-619">Parameters</span></span>  

<span data-ttu-id="67061-620">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="67061-620">This method has no parameters.</span></span>  

#### <span data-ttu-id="67061-621">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67061-621">Return value</span></span>  

<span data-ttu-id="67061-622">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="67061-622">This method does not return a value.</span></span>  

### <span data-ttu-id="67061-623">stop</span><span class="sxs-lookup"><span data-stu-id="67061-623">stop</span></span>  

<span data-ttu-id="67061-624">Interrompe a navegação ou download atual da **WebView** .</span><span class="sxs-lookup"><span data-stu-id="67061-624">Halts the current **webview** navigation or download.</span></span>  

```javascript
webview.stop();
```  

#### <span data-ttu-id="67061-625">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67061-625">Parameters</span></span>  

<span data-ttu-id="67061-626">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="67061-626">This method has no parameters.</span></span>  

#### <span data-ttu-id="67061-627">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67061-627">Return value</span></span>  

<span data-ttu-id="67061-628">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="67061-628">This method does not return a value.</span></span>  

## <span data-ttu-id="67061-629">Propriedades</span><span class="sxs-lookup"><span data-stu-id="67061-629">Properties</span></span>  

### <span data-ttu-id="67061-630">canGoBack</span><span class="sxs-lookup"><span data-stu-id="67061-630">canGoBack</span></span>  

<span data-ttu-id="67061-631">Obtém um valor que indica se a **WebView** pode navegar para trás.</span><span class="sxs-lookup"><span data-stu-id="67061-631">Gets a value that indicates whether the **webview** can navigate backward.</span></span>  

<span data-ttu-id="67061-632">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="67061-632">This property is read-only.</span></span>  

```javascript
var canGoBack = webview.canGoBack;
```  

#### <span data-ttu-id="67061-633">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="67061-633">Property value</span></span>  

<span data-ttu-id="67061-634">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="67061-634">Type: **Boolean**</span></span>  

<span data-ttu-id="67061-635">**Verdadeiro** se a **WebView** puder navegar para trás; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="67061-635">**True** if the **webview** can navigate backward; otherwise, **false**.</span></span>  

### <span data-ttu-id="67061-636">canGoForward</span><span class="sxs-lookup"><span data-stu-id="67061-636">canGoForward</span></span>  

<span data-ttu-id="67061-637">Obtém um valor que indica se a **WebView** pode navegar para frente.</span><span class="sxs-lookup"><span data-stu-id="67061-637">Gets a value that indicates whether the **webview** can navigate forward.</span></span>  

<span data-ttu-id="67061-638">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="67061-638">This property is read-only.</span></span>  

```javascript
var canGoForward = webview.canGoForward;
```  

#### <span data-ttu-id="67061-639">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="67061-639">Property value</span></span>  

<span data-ttu-id="67061-640">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="67061-640">Type: **Boolean**</span></span>  

<span data-ttu-id="67061-641">**Verdadeiro** se a **WebView** puder navegar para frente; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="67061-641">**True** if the **webview** can navigate forward; otherwise, **false**.</span></span>  

### <span data-ttu-id="67061-642">containsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="67061-642">containsFullScreenElement</span></span>  

<span data-ttu-id="67061-643">Obtém um valor que indica se a **WebView** contém um elemento compatível com tela inteira.</span><span class="sxs-lookup"><span data-stu-id="67061-643">Gets a value that indicates whether the **webview** contains an element that supports full screen.</span></span>  <span data-ttu-id="67061-644">Consulte o evento MSWebViewContainsFullScreenElementChanged para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="67061-644">See the MSWebViewContainsFullScreenElementChanged event for more info.</span></span>  

<span data-ttu-id="67061-645">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="67061-645">This property is read-only.</span></span>  

```javascript
var containsFullScreenElement = webview.containsFullScreenElement;
```  

#### <span data-ttu-id="67061-646">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="67061-646">Property value</span></span>  

<span data-ttu-id="67061-647">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="67061-647">Type: **Boolean**</span></span>  

<span data-ttu-id="67061-648">**Verdadeiro** se a **WebView** contiver um elemento compatível com tela inteira; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="67061-648">**True** if the **webview** contains an element that supports full screen; otherwise, **false**.</span></span>  

### <span data-ttu-id="67061-649">documentTitle</span><span class="sxs-lookup"><span data-stu-id="67061-649">documentTitle</span></span>  

<span data-ttu-id="67061-650">Obtém o título da página atualmente exibida no **WebView**.</span><span class="sxs-lookup"><span data-stu-id="67061-650">Gets the title of the page currently displayed in the **webview**.</span></span>  

<span data-ttu-id="67061-651">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="67061-651">This property is read-only.</span></span>  

```javascript
var documentTitle = webview.documentTitle;
```  

#### <span data-ttu-id="67061-652">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="67061-652">Property value</span></span>  

<span data-ttu-id="67061-653">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67061-653">Type: **String**</span></span>  

<span data-ttu-id="67061-654">O título da página.</span><span class="sxs-lookup"><span data-stu-id="67061-654">The page title.</span></span>  

### <span data-ttu-id="67061-655">height</span><span class="sxs-lookup"><span data-stu-id="67061-655">height</span></span>  

<span data-ttu-id="67061-656">Obtém ou define a altura do **WebView**.</span><span class="sxs-lookup"><span data-stu-id="67061-656">Gets or sets the height of the **webview**.</span></span>  

```javascript
var height = webview.height;
webview.height = height;
```  

#### <span data-ttu-id="67061-657">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="67061-657">Property value</span></span>  

<span data-ttu-id="67061-658">Tipo: **número**</span><span class="sxs-lookup"><span data-stu-id="67061-658">Type: **Number**</span></span>  

<span data-ttu-id="67061-659">A altura do **WebView**.</span><span class="sxs-lookup"><span data-stu-id="67061-659">The height of the **webview**.</span></span>  

### <span data-ttu-id="67061-660">processo</span><span class="sxs-lookup"><span data-stu-id="67061-660">process</span></span>  

<span data-ttu-id="67061-661">Obtém o processo **WebView** .</span><span class="sxs-lookup"><span data-stu-id="67061-661">Gets the **webview** process.</span></span>  

<span data-ttu-id="67061-662">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="67061-662">This property is read-only.</span></span>  

```javascript
var process = webview.process;
webview.process = process;
```  

#### <span data-ttu-id="67061-663">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="67061-663">Property value</span></span>  

<span data-ttu-id="67061-664">Tipo: [MSWebViewProcess](./webview/MSWebViewProcess.md)</span><span class="sxs-lookup"><span data-stu-id="67061-664">Type: [MSWebViewProcess](./webview/MSWebViewProcess.md)</span></span>  

### <span data-ttu-id="67061-665">settings</span><span class="sxs-lookup"><span data-stu-id="67061-665">settings</span></span>  

<span data-ttu-id="67061-666">Obtém um objeto [MSWebViewSettings](./webview/MSWebViewSettings.md) que contém propriedades para habilitar ou desabilitar recursos do **WebView** .</span><span class="sxs-lookup"><span data-stu-id="67061-666">Gets a [MSWebViewSettings](./webview/MSWebViewSettings.md) object that contains properties to enable or disable **webview** features.</span></span>  

<span data-ttu-id="67061-667">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="67061-667">This property is read-only.</span></span>  

```javascript
var settings = webview.settings;
webview.settings = settings;
```  

#### <span data-ttu-id="67061-668">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="67061-668">Property value</span></span>  

<span data-ttu-id="67061-669">Tipo: [MSWebViewSettings](./webview/MSWebViewSettings.md)</span><span class="sxs-lookup"><span data-stu-id="67061-669">Type: [MSWebViewSettings](./webview/MSWebViewSettings.md)</span></span>  

<span data-ttu-id="67061-670">Um objeto [MSWebViewSettings](./webview/MSWebViewSettings.md) que contém propriedades para habilitar ou desabilitar recursos do **WebView** .</span><span class="sxs-lookup"><span data-stu-id="67061-670">A [MSWebViewSettings](./webview/MSWebViewSettings.md) object that contains properties to enable or disable **webview** features.</span></span>  

### <span data-ttu-id="67061-671">src</span><span class="sxs-lookup"><span data-stu-id="67061-671">src</span></span>  

<span data-ttu-id="67061-672">Obtém ou define a fonte URI (Uniform Resource Identifier) do conteúdo HTML a ser exibido no controle de **WebView** .</span><span class="sxs-lookup"><span data-stu-id="67061-672">Gets or sets the Uniform Resource Identifier (URI) source of the HTML content to display in the **webview** control.</span></span>  

```javascript
var src = webview.src;
webview.src = src;
```  

#### <span data-ttu-id="67061-673">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="67061-673">Property value</span></span>  

<span data-ttu-id="67061-674">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67061-674">Type: **String**</span></span>  

<span data-ttu-id="67061-675">A origem do URI do conteúdo HTML a ser exibido no controle **WebView** .</span><span class="sxs-lookup"><span data-stu-id="67061-675">The URI source of the HTML content to display in the **webview** control.</span></span>  

### <span data-ttu-id="67061-676">width</span><span class="sxs-lookup"><span data-stu-id="67061-676">width</span></span>  

<span data-ttu-id="67061-677">Obtém ou define a largura do **WebView**.</span><span class="sxs-lookup"><span data-stu-id="67061-677">Gets or sets the width of the **webview**.</span></span>  

```javascript
var width = webview.width;
webview.width = width;
```  

#### <span data-ttu-id="67061-678">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="67061-678">Property value</span></span>  

<span data-ttu-id="67061-679">Tipo: **número**</span><span class="sxs-lookup"><span data-stu-id="67061-679">Type: **Number**</span></span>  

<span data-ttu-id="67061-680">A largura do **WebView**.</span><span class="sxs-lookup"><span data-stu-id="67061-680">The width of the **webview**.</span></span>  
