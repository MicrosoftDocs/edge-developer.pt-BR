---
description: Saiba como usar o Protocolo Chrome DevTools em seus aplicativos WebView2 usando o pacote NuGet do Microsoft Edge WebView2 Chromium DevTools Protocol
title: Usar o Protocolo Chrome DevTools no WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/15/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Chrome DevTools Protocol
ms.openlocfilehash: 0f7a2dd4bb3b1621e854cd4c0c5410e64d3c03ff
ms.sourcegitcommit: 0ef5bb3933cde8a466f2931b824f07b4995cfe5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "11409301"
---
# <a name="use-chromium-devtools-protocol-in-webview2"></a><span data-ttu-id="9a7d1-104">Usar o Protocolo Chromium DevTools no WebView2</span><span class="sxs-lookup"><span data-stu-id="9a7d1-104">Use Chromium DevTools Protocol in WebView2</span></span>  

<span data-ttu-id="9a7d1-105">O [Protocolo Chromium DevTools][GitHubChromedevtoolsDevtoolsProtocol] fornece APIs para instrumentar, inspecionar, depurar e perfis de navegadores baseados em Chromium.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-105">The [Chromium DevTools Protocol][GitHubChromedevtoolsDevtoolsProtocol] provides APIs to instrument, inspect, debug, and profile Chromium-based browsers.</span></span>  <span data-ttu-id="9a7d1-106">O Protocolo Chromium DevTools é a base do Microsoft Edge \(Chromium\) DevTools.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-106">The Chromium DevTools Protocol is the foundation for the Microsoft Edge \(Chromium\) DevTools.</span></span>  <span data-ttu-id="9a7d1-107">Use o Protocolo Chromium DevTools para recursos que não são implementados na plataforma WebView2.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-107">Use the Chromium DevTools Protocol for features that aren't implemented in the WebView2 platform.</span></span>  <span data-ttu-id="9a7d1-108">Para obter mais informações sobre a funcionalidade Chromium DevTools Protocol, navegue até [Chromium DevTools Protocol][GitHubChromedevtoolsDevtoolsProtocol].</span><span class="sxs-lookup"><span data-stu-id="9a7d1-108">For more information about the Chromium DevTools Protocol functionality, navigate to [Chromium DevTools Protocol][GitHubChromedevtoolsDevtoolsProtocol].</span></span>  

> [!CAUTION]
> <span data-ttu-id="9a7d1-109">A equipe do Microsoft Edge WebView2 não mantém ou dá suporte ao Protocolo Chromium DevTools.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-109">The Microsoft Edge WebView2 team does not maintain or support the Chromium DevTools Protocol.</span></span>  <span data-ttu-id="9a7d1-110">O Protocolo Chromium DevTools é mantido pelo projeto Chromium de código aberto.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-110">The Chromium DevTools Protocol is maintained by the open source Chromium project.</span></span>  
> 
> <span data-ttu-id="9a7d1-111">Para enviar suas sugestões para os recursos futuros da plataforma WebView2, navegue até [WebView Feedback][GithubMicrosoftedgeWebview2feedback] e envie um problema.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-111">To send your suggestions for future WebView2 platform features, navigate to [WebView Feedback][GithubMicrosoftedgeWebview2feedback] and submit an issue.</span></span>  

<span data-ttu-id="9a7d1-112">Para usar a API de Protocolo Chromium DevTools no WebView2, use uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-112">To use the Chromium DevTools Protocol API in WebView2, use either of the following actions.</span></span>  

*   <span data-ttu-id="9a7d1-113">Instale e use o [pacote NuGet do Microsoft.Web.WebView2.DevToolsProtocolExtension (Visualização)][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] \(.NET\).</span><span class="sxs-lookup"><span data-stu-id="9a7d1-113">Install and use the [Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet package \(.NET\).</span></span>  
*   <span data-ttu-id="9a7d1-114">Execute um dos seguintes métodos.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-114">Run one of the following methods.</span></span>  
    *   <span data-ttu-id="9a7d1-115">.NET:  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]</span><span class="sxs-lookup"><span data-stu-id="9a7d1-115">.NET:  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]</span></span>  
    *   <span data-ttu-id="9a7d1-116">Win32 C/C++:  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]</span><span class="sxs-lookup"><span data-stu-id="9a7d1-116">Win32 C/C++:  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]</span></span>  
    
## <a name="use-devtoolsprotocolhelper-preview"></a><span data-ttu-id="9a7d1-117">Usar DevToolsProtocolHelper (Visualização)</span><span class="sxs-lookup"><span data-stu-id="9a7d1-117">Use DevToolsProtocolHelper (Preview)</span></span>

> [!NOTE]
> <span data-ttu-id="9a7d1-118">O [pacote NuGet Microsoft.Web.WebView2.DevToolsProtocolExtension][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] está atualmente em visualização técnica.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-118">The [Microsoft.Web.WebView2.DevToolsProtocolExtension][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet package is currently in technical preview.</span></span>  <span data-ttu-id="9a7d1-119">Durante a visualização, evite usar o pacote em aplicativos de produção.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-119">While in preview, refrain from using the package in production apps.</span></span>

<span data-ttu-id="9a7d1-120">[Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] é um pacote NuGet criado pela equipe webView2 que fornece fácil acesso aos recursos do Protocolo Chromium DevTools.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-120">[Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] is a NuGet package created by the WebView2 team that provides easy access to Chromium DevTools Protocol features.</span></span>  <span data-ttu-id="9a7d1-121">Os exemplos a seguir descrevem como usar a funcionalidade de localização geográfica no Protocolo Chromium DevTools em seu controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-121">The following examples describe how to use the geolocation functionality in Chromium DevTools Protocol in your WebView2 control.</span></span>  <span data-ttu-id="9a7d1-122">Você pode seguir um padrão semelhante para usar outros recursos do Chromium DevTools Protocol.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-122">You may follow a similar pattern to use other Chromium DevTools Protocol features.</span></span>  

## <a name="step-1-create-a-webpage-to-find-your-geolocation"></a><span data-ttu-id="9a7d1-123">Etapa 1: Criar uma página da Web para encontrar sua localização geográfica</span><span class="sxs-lookup"><span data-stu-id="9a7d1-123">Step 1: Create a webpage to find your geolocation</span></span>  

<span data-ttu-id="9a7d1-124">Para criar um `HTML file` para encontrar sua localização geográfica, conclua seguindo as ações.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-124">To create an `HTML file` to find your geolocation, complete following the actions.</span></span>  

1.  <span data-ttu-id="9a7d1-125">Abra Visual Studio Código \(ou um IDE de sua escolha\).</span><span class="sxs-lookup"><span data-stu-id="9a7d1-125">Open Visual Studio Code \(or an IDE of your choice\).</span></span>  
1.  <span data-ttu-id="9a7d1-126">Crie um novo `.html` arquivo.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-126">Create a new `.html` file.</span></span>  
1.  <span data-ttu-id="9a7d1-127">Copie e colar o seguinte trecho de código no novo `.html` arquivo.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-127">Copy and paste the following code snippet in your new `.html` file.</span></span>  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <title>Geolocation Finder</title>
    </head>
    <body>
        <button id="display">Display Location</button>
        <div id="message"></div>
    </body>
    
    <script>
        const btn = document.getElementById('display');
        // Find the user location.
        btn.addEventListener('click', function () {
            navigator.geolocation.getCurrentPosition(onSuccess, onError);
        });
        
        // Update message to display the latitude and longitude coordinates.
        function onSuccess(position) {
            const {latitude, longitude} = position.coords;
            message.textContent = `Your location: (${latitude},${longitude})`;
        }
        
        function onError() {
            message.textContent = `Operation Failed`;
        }
    </script>
    </html>
    ```  
    
1.  <span data-ttu-id="9a7d1-128">Salve o `.html` arquivo com o nome do arquivo `geolocation.html` .</span><span class="sxs-lookup"><span data-stu-id="9a7d1-128">Save the `.html` file with the filename `geolocation.html`.</span></span>  
1.  <span data-ttu-id="9a7d1-129">Abra o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-129">Open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="9a7d1-130">Abra o arquivo `geolocation.html`.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-130">Open the `geolocation.html` file.</span></span>  
1.  <span data-ttu-id="9a7d1-131">Para exibir suas coordenadas de latitude e longitude, escolha o **botão Exibir Local.**</span><span class="sxs-lookup"><span data-stu-id="9a7d1-131">To display your latitude and longitude coordinates, choose the **Display Location** button.</span></span>  <span data-ttu-id="9a7d1-132">Para verificar e comparar sua localização geográfica, copie e colar suas coordenadas em [https://www.bing.com/maps][BingMaps] .</span><span class="sxs-lookup"><span data-stu-id="9a7d1-132">To verify and compare your geolocation, copy and paste your coordinates in [https://www.bing.com/maps][BingMaps].</span></span>  
    
    :::image type="complex" source="./media/geolocater-browser.png" alt-text="Exibir as coordenadas de localização geográfica do usuário no Microsoft Edge" lightbox="./media/geolocater-browser.png":::
       <span data-ttu-id="9a7d1-134">Exibir as coordenadas de localização geográfica do usuário no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9a7d1-134">Display the geolocation coordinates of the user in Microsoft Edge</span></span>  
    :::image-end:::  
    
## <a name="step-2-display-geolocationhtml-in-a-webview2"></a><span data-ttu-id="9a7d1-135">Etapa 2: Exibir geolocation.html em um WebView2</span><span class="sxs-lookup"><span data-stu-id="9a7d1-135">Step 2: Display geolocation.html in a WebView2</span></span>  

1.  <span data-ttu-id="9a7d1-136">Para criar um aplicativo WebView2, use um dos seguintes guias de início ou exemplos de WebView2.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-136">To create a WebView2 app, use either of the following getting started guides or WebView2 samples.</span></span>  
    *   [<span data-ttu-id="9a7d1-137">Como começar com o WebView2 no Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9a7d1-137">Getting Started with WebView2 in Windows Forms</span></span>][Webview2GettingstartedWinforms]  
    *   [<span data-ttu-id="9a7d1-138">Como começar com WebView2 no WPF</span><span class="sxs-lookup"><span data-stu-id="9a7d1-138">Getting Started with WebView2 in WPF</span></span>][Webview2GettingstartedWpf]  
    *   [<span data-ttu-id="9a7d1-139">Exemplos de WebView2</span><span class="sxs-lookup"><span data-stu-id="9a7d1-139">WebView2 samples</span></span>][GithubMicrosoftedgeWebview2samples]  
        
1.  <span data-ttu-id="9a7d1-140">Definir a navegação inicial do controle WebView2 como `geolocation.html` .</span><span class="sxs-lookup"><span data-stu-id="9a7d1-140">Set the initial navigation of the WebView2 control to `geolocation.html`.</span></span>  
    
    ```csharp
    webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    ```  
    
1.  <span data-ttu-id="9a7d1-141">Verifique se o arquivo é exibido no aplicativo de controle `geolocation.html` WebView2.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-141">Ensure the `geolocation.html` file displays in your WebView2 control app.</span></span>  
    
    :::image type="complex" source="./media/initial-geolocate.png" alt-text="Exibir o arquivo geolocater.html em seu aplicativo de controle WebView2" lightbox="./media/initial-geolocate.png":::
       <span data-ttu-id="9a7d1-143">Exibir o `geolocation.html` arquivo no aplicativo de controle WebView2</span><span class="sxs-lookup"><span data-stu-id="9a7d1-143">Display the `geolocation.html` file in your WebView2 control app</span></span>  
    :::image-end:::  
    
## <a name="step-3-install-the-devtoolsprotocolhelper-nuget-package"></a><span data-ttu-id="9a7d1-144">Etapa 3: Instalar o pacote NuGet DevToolsProtocolHelper</span><span class="sxs-lookup"><span data-stu-id="9a7d1-144">Step 3: Install the DevToolsProtocolHelper NuGet package</span></span>  

<span data-ttu-id="9a7d1-145">Use NuGet para baixar `Microsoft.Web.WebView2.DevToolsProtocolExtension` .</span><span class="sxs-lookup"><span data-stu-id="9a7d1-145">Use NuGet to download `Microsoft.Web.WebView2.DevToolsProtocolExtension`.</span></span>  <span data-ttu-id="9a7d1-146">Para instalar o pacote, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-146">To install the package, complete the following actions.</span></span>  

1.  <span data-ttu-id="9a7d1-147">Escolha **Gerenciar**  >  **Pacotes NuGet do Projeto**  >  **Procurar**.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-147">Choose **Project** > **Manage NuGet Packages** > **Browse**.</span></span>  
1.  <span data-ttu-id="9a7d1-148">Digite `Microsoft.Web.WebView2.DevToolsProtocolExtension` e escolha **Microsoft.Web.WebView2.DevToolsProtocolExtension**  >  **Install**.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-148">Type `Microsoft.Web.WebView2.DevToolsProtocolExtension` and choose **Microsoft.Web.WebView2.DevToolsProtocolExtension** > **Install**.</span></span>   
    
:::image type="complex" source="./media/cdpnuget.png" alt-text="Certifique-se de que o Microsoft.Web.WebView2.DevToolsProtocolExtension seja exibido no Visual Studio NuGet Gerenciador de Pacotes" lightbox="./media/cdpnuget.png":::
   <span data-ttu-id="9a7d1-150">Verifique **se o Microsoft.Web.WebView2.DevToolsProtocolExtension** é exibido no Visual Studio NuGet Gerenciador de Pacotes</span><span class="sxs-lookup"><span data-stu-id="9a7d1-150">Ensure **Microsoft.Web.WebView2.DevToolsProtocolExtension** displays in the Visual Studio NuGet Package Manager</span></span>  
:::image-end:::  

## <a name="step-4-use-devtools-protocol-helper"></a><span data-ttu-id="9a7d1-151">Etapa 4: Usar o Auxiliar de Protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="9a7d1-151">Step 4: Use DevTools Protocol Helper</span></span>  

1.  <span data-ttu-id="9a7d1-152">Adicione o `DevToolsProtocolExtension` namespace ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-152">Add the `DevToolsProtocolExtension` namespace to your project.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    using Microsoft.Web.WebView2.Core.DevToolsProtocolExtension;
    ```  
    
1.  <span data-ttu-id="9a7d1-153">Insinue `DevToolsProtocolHelper` o objeto e navegue até `geolocation.html` .</span><span class="sxs-lookup"><span data-stu-id="9a7d1-153">Instantiate the `DevToolsProtocolHelper` object and navigate to `geolocation.html`.</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        DevToolsProtocolHelper helper = webView.CoreWebView2.GetDevToolsProtocolHelper(); 
        
        webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    }
    ```  
    
1.  <span data-ttu-id="9a7d1-154">Execute o [método setGeoLocationOverrideAsync.][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]</span><span class="sxs-lookup"><span data-stu-id="9a7d1-154">Run the [setGeoLocationOverrideAsync][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride] method.</span></span>  <span data-ttu-id="9a7d1-155">Para obter mais informações, navegue [até setGeolocationOverride][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride].</span><span class="sxs-lookup"><span data-stu-id="9a7d1-155">For more information, navigate to [setGeolocationOverride][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride].</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        DevToolsProtocolHelper helper = webview.CoreWebView2.GetDevToolsProtocolHelper();
        
        webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
        
        // Latitude and longitude for Paris, France.
        double latitude = 48.857024082572565;  
        double longitude = 2.3161581601457386;  
        double accuracy = 1;
        await helper.Emulation.setGeolocationOverrideAsync(latitude, longitude, accuracy);
        
    }
    ```  
    
1.  <span data-ttu-id="9a7d1-156">Execute seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-156">Run your app.</span></span>  
1.  <span data-ttu-id="9a7d1-157">Para exibir as coordenadas de Paris, França, escolha o **botão Exibir Local.**</span><span class="sxs-lookup"><span data-stu-id="9a7d1-157">To display the coordinates of Paris, France, choose the **Display Location** button.</span></span>  
    
    :::image type="complex" source="./media/finallocation-cdp.png" alt-text="Exibir o arquivo .html em um controle WebView2 com as coordenadas de Paris" lightbox="./media/finallocation-cdp.png":::
       <span data-ttu-id="9a7d1-159">Exibir o `.html` arquivo em um controle WebView2 com as coordenadas para Paris</span><span class="sxs-lookup"><span data-stu-id="9a7d1-159">Display the `.html` file in a WebView2 control with the coordinates for Paris</span></span>  
    :::image-end:::  
    
## <a name="file-a-chromium-devtools-protocol-bug"></a><span data-ttu-id="9a7d1-160">Arquivar um bug do Protocolo Chromium DevTools</span><span class="sxs-lookup"><span data-stu-id="9a7d1-160">File a Chromium DevTools Protocol bug</span></span>  

<span data-ttu-id="9a7d1-161">A equipe WebView2 não possui o Protocolo Chromium DevTools.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-161">The WebView2 team doesn't own the Chromium DevTools Protocol.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="9a7d1-162">Comentários diretos e bugs para o repo Chromium Issues.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-162">Direct feedback and bugs to the Chromium Issues repo.</span></span>  

<span data-ttu-id="9a7d1-163">Para arquivar um bug ou problema do Protocolo Chromium DevTools, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-163">To file a Chromium DevTools Protocol bug or issue, complete the following actions.</span></span>  

1.  <span data-ttu-id="9a7d1-164">Arquivar um [relatório de bugs.][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform]</span><span class="sxs-lookup"><span data-stu-id="9a7d1-164">File a [bug report][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform].</span></span>  
1.  <span data-ttu-id="9a7d1-165">Navegue [até WebView Feedback][GithubMicrosoftedgeWebview2feedback] e abra um novo problema.</span><span class="sxs-lookup"><span data-stu-id="9a7d1-165">Navigate to [WebView Feedback][GithubMicrosoftedgeWebview2feedback] and open a new issue.</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="9a7d1-166">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9a7d1-166">See also</span></span>  

*   [<span data-ttu-id="9a7d1-167">Exemplos de WebView2</span><span class="sxs-lookup"><span data-stu-id="9a7d1-167">WebView2 samples</span></span>][GithubMicrosoftedgeWebview2samples]  
    
 <!-- links -->  

[Webview2GettingstartedWinforms]: /microsoft-edge/webview2/gettingstarted/winforms "Como começar com o WebView2 no Windows Forms | Microsoft Docs"  
[Webview2GettingstartedWpf]: /microsoft-edge/webview2/gettingstarted/wpf "Como começar com WebView2 no WPF | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]: /dotnet/api/microsoft.web.webview2.core.corewebview2.getdevtoolsprotocoleventreceiver?view=webview2-dotnet-1.0.774.44&preserve-view=true "Método CoreWebView2.GetDevToolsProtocolEventReceiver(String) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString]: /dotnet/api/microsoft.web.webview2.core.corewebview2.calldevtoolsprotocolmethodasync?view=webview2-dotnet-1.0.774.44&preserve-view=true#Microsoft_Web_WebView2_Core_CoreWebView2_CallDevToolsProtocolMethodAsync_System_String_System_String_ "Método CoreWebView2.CallDevToolsProtocolMethodAsync(String, String) | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-1.0.774.44&preserve-view=true#calldevtoolsprotocolmethod "CallDevToolsProtocolMethod - interface ICoreWebView2 | Microsoft Docs"  
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-1.0.774.44&preserve-view=true "interface ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs"  

[BingMaps]: https://www.bing.com/maps "Bing Maps"  

[GitHubChromedevtoolsDevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Protocolo Chrome DevTools | GitHub"  
[GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]: https://chromedevtools.github.io/devtools-protocol/tot/Emulation/#method-setGeolocationOverride "Emulation.setGeolocationOverride - Protocolo Chrome DevTools | GitHub"  

[GithubMicrosoftedgeWebview2feedback]: https://github.com/MicrosoftEdge/WebView2Feedback "WebView Feedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 | GitHub"  

[ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform]: https://bugs.chromium.org/p/chromium/issues/entry?components=Platform%3EDevTools%3EPlatform "Relatório de bugs | Bugs de cromo"  

[NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension]: https://int.nugettest.org/packages/Microsoft.Web.WebView2.DevToolsProtocolExtension "Microsoft.Web.WebView2.DevToolsProtocolExtension | Galeria de QA NuGet"  