---
description: Saiba como usar o Protocolo Chrome DevTools em seus aplicativos WebView2 usando o pacote NuGet do Microsoft Edge WebView2 Chromium DevTools Protocol
title: Usar o Protocolo Chrome DevTools no WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Chrome DevTools Protocol
ms.openlocfilehash: 86846ee195406f78d5fd7c369f375ed1e359101a
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461196"
---
# <a name="use-chromium-devtools-protocol-in-webview2"></a>Usar o Protocolo Chromium DevTools no WebView2  

O [Protocolo Chromium DevTools][GitHubChromedevtoolsDevtoolsProtocol] fornece APIs para instrumentar, inspecionar, depurar e perfis de navegadores baseados em Chromium.  O Protocolo Chromium DevTools é a base do Microsoft Edge \(Chromium\) DevTools.  Use o Protocolo Chromium DevTools para recursos que não são implementados na plataforma WebView2.  Para obter mais informações sobre a funcionalidade Chromium DevTools Protocol, navegue até [Chromium DevTools Protocol][GitHubChromedevtoolsDevtoolsProtocol].  

> [!CAUTION]
> A equipe do Microsoft Edge WebView2 não mantém ou dá suporte ao Protocolo Chromium DevTools.  O Protocolo Chromium DevTools é mantido pelo projeto Chromium de código aberto.  
> 
> Para enviar suas sugestões para os recursos futuros da plataforma WebView2, navegue até [WebView Feedback][GithubMicrosoftedgeWebview2feedback] e envie um problema.  

Para usar a API de Protocolo Chromium DevTools no WebView2, use uma das seguintes ações.  

*   Instale e use o [pacote NuGet do Microsoft.Web.WebView2.DevToolsProtocolExtension (Visualização)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] \(.NET\).  
*   Execute um dos seguintes métodos.  
    *   .NET:  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]  
    *   Win32 C/C++:  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]  
    
## <a name="use-devtoolsprotocolhelper-preview"></a>Usar DevToolsProtocolHelper (Visualização)

> [!NOTE]
> O [pacote NuGet Microsoft.Web.WebView2.DevToolsProtocolExtension][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] está atualmente em visualização técnica.  Durante a visualização, evite usar o pacote em aplicativos de produção.

[Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] é um pacote NuGet criado pela equipe webView2 que fornece fácil acesso aos recursos do Protocolo Chromium DevTools.  Os exemplos a seguir descrevem como usar a funcionalidade de localização geográfica no Protocolo Chromium DevTools em seu controle WebView2.  Você pode seguir um padrão semelhante para usar outros recursos do Chromium DevTools Protocol.  

## <a name="step-1-create-a-webpage-to-find-your-geolocation"></a>Etapa 1: Criar uma página da Web para encontrar sua localização geográfica  

Para criar um `HTML file` para encontrar sua localização geográfica, conclua seguindo as ações.  

1.  Abra Visual Studio Código \(ou um IDE de sua escolha\).  
1.  Crie um novo `.html` arquivo.  
1.  Copie e colar o seguinte trecho de código no novo `.html` arquivo.  
    
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
    
1.  Salve o `.html` arquivo com o nome do arquivo `geolocation.html` .  
1.  Abra o Microsoft Edge.  
1.  Abra o arquivo `geolocation.html`.  
1.  Para exibir suas coordenadas de latitude e longitude, escolha o **botão Exibir Local.**  Para verificar e comparar sua localização geográfica, copie e colar suas coordenadas em [https://www.bing.com/maps][BingMaps] .  
    
    :::image type="complex" source="./media/geolocater-browser.png" alt-text="Exibir as coordenadas de localização geográfica do usuário no Microsoft Edge" lightbox="./media/geolocater-browser.png":::
       Exibir as coordenadas de localização geográfica do usuário no Microsoft Edge  
    :::image-end:::  
    
## <a name="step-2-display-geolocationhtml-in-a-webview2"></a>Etapa 2: Exibir geolocation.html em um WebView2  

1.  Para criar um aplicativo WebView2, use um dos seguintes guias de início ou exemplos de WebView2.  
    *   [Como começar com o WebView2 no Windows Forms][Webview2GettingstartedWinforms]  
    *   [Como começar com WebView2 no WPF][Webview2GettingstartedWpf]  
    *   [Exemplos de WebView2][GithubMicrosoftedgeWebview2samples]  
        
1.  Definir a navegação inicial do controle WebView2 como `geolocation.html` .  
    
    ```csharp
    webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    ```  
    
1.  Verifique se o arquivo é exibido no aplicativo de controle `geolocation.html` WebView2.  
    
    :::image type="complex" source="./media/initial-geolocate.png" alt-text="Exibir o arquivo geolocater.html em seu aplicativo de controle WebView2" lightbox="./media/initial-geolocate.png":::
       Exibir o `geolocation.html` arquivo no aplicativo de controle WebView2  
    :::image-end:::  
    
## <a name="step-3-install-the-devtoolsprotocolhelper-nuget-package"></a>Etapa 3: Instalar o pacote NuGet DevToolsProtocolHelper  

Use NuGet para baixar `Microsoft.Web.WebView2.DevToolsProtocolExtension` .  Para instalar o pacote, conclua as seguintes ações.  

1.  Escolha **Gerenciar**  >  **Pacotes NuGet do Projeto**  >  **Procurar**.  
1.  Digite `Microsoft.Web.WebView2.DevToolsProtocolExtension` e escolha **Microsoft.Web.WebView2.DevToolsProtocolExtension**  >  **Install**.   
    
:::image type="complex" source="./media/cdpnuget.png" alt-text="Certifique-se de que o Microsoft.Web.WebView2.DevToolsProtocolExtension seja exibido no Visual Studio NuGet Gerenciador de Pacotes" lightbox="./media/cdpnuget.png":::
   Verifique **se o Microsoft.Web.WebView2.DevToolsProtocolExtension** é exibido no Visual Studio NuGet Gerenciador de Pacotes  
:::image-end:::  

## <a name="step-4-use-devtools-protocol-helper"></a>Etapa 4: Usar o Auxiliar de Protocolo DevTools  

1.  Adicione o `DevToolsProtocolExtension` namespace ao seu projeto.  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    using Microsoft.Web.WebView2.Core.DevToolsProtocolExtension;
    ```  
    
1.  Insinue `DevToolsProtocolHelper` o objeto e navegue até `geolocation.html` .  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        DevToolsProtocolHelper helper = webView.CoreWebView2.GetDevToolsProtocolHelper(); 
        
        webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    }
    ```  
    
1.  Execute o [método setGeoLocationOverrideAsync.][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]  Para obter mais informações, navegue [até setGeolocationOverride][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride].  
    
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
    
1.  Execute seu aplicativo.  
1.  Para exibir as coordenadas de Paris, França, escolha o **botão Exibir Local.**  
    
    :::image type="complex" source="./media/finallocation-cdp.png" alt-text="Exibir o arquivo .html em um controle WebView2 com as coordenadas de Paris" lightbox="./media/finallocation-cdp.png":::
       Exibir o `.html` arquivo em um controle WebView2 com as coordenadas para Paris  
    :::image-end:::  
    
## <a name="file-a-chromium-devtools-protocol-bug"></a>Arquivar um bug do Protocolo Chromium DevTools  

A equipe WebView2 não possui o Protocolo Chromium DevTools.  

> [!IMPORTANT]
> Comentários diretos e bugs para o repo Chromium Issues.  

Para arquivar um bug ou problema do Protocolo Chromium DevTools, conclua as seguintes ações.  

1.  Arquivar um [relatório de bugs.][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform]  
1.  Navegue [até WebView Feedback][GithubMicrosoftedgeWebview2feedback] e abra um novo problema.  
    
## <a name="see-also"></a>Consulte também  

*   [Exemplos de WebView2][GithubMicrosoftedgeWebview2samples]  
    
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

[NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension]: https://www.nuget.org/packages/Microsoft.Web.WebView2.DevToolsProtocolExtension "Microsoft.Web.WebView2.DevToolsProtocolExtension | Galeria de QA NuGet"  
