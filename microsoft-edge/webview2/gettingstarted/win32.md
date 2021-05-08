---
description: Guia de início com WebView2 para aplicativos Win32
title: Iniciando o WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Controller, controle de navegador, html de borda
ms.openlocfilehash: 47f24b160797ce0ab7a7cb6a656c4f6b4e5696ac
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536321"
---
# <a name="getting-started-with-webview2"></a>Como começar com o WebView2  

Neste artigo, você pode começar a criar seu primeiro aplicativo WebView2 e saber mais sobre os principais recursos do [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Para obter mais informações sobre APIs webView2 individuais, navegue até [referência de API][Webview2ReferenceWin32].  

## <a name="prerequisites"></a>Pré-requisitos  

Certifique-se de instalar a lista de pré-requisitos a seguir antes de prosseguir.  

*   [WebView2 Runtime][Webview2Installer] ou qualquer canal Microsoft Edge [(Chromium)][MicrosoftedgeinsiderDownload] não estável instalado no sistema operacional com suporte \(atualmente Windows 10, Windows 8.1 e Windows 7\).  
    
    > [!NOTE]
    > A equipe webView recomenda o uso do canal Canary e a versão mínima necessária é 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2015 ou posterior com suporte C++ instalado.  
    
## <a name="step-1---create-a-single-window-app"></a>Etapa 1 - Criar um aplicativo de janela única  

Comece com um projeto de área de trabalho básico que contém uma única janela principal.  

> [!IMPORTANT]
> Para focalizar melhor o passo a passo, use o código de exemplo modificado do Passo a passo: Crie um aplicativo de área de trabalho Windows tradicional [(C++)][CppWindowsWalkthroughCreatingDesktopApplication] para seu aplicativo de exemplo.  Para baixar o exemplo modificado e começar, navegue até [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].  

1.  Em Visual Studio, abra `WebView2GettingStarted.sln` .  
    Se você usar uma versão mais antiga do Visual Studio, passe o mouse no projeto **WebView2GettingStarted,** abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Propriedades**.  Em **Propriedades**de Configuração Geral, modifique Windows Versão do SDK e Platform Toolset para usar o  >  **** SDK win10 e o **** Visual Studio ferramentas disponíveis para você. ****  

:::image type="complex" source="../media/tool-version.png" alt-text="Versão da ferramenta" lightbox="../media/tool-version.png":::
   Versão da ferramenta  
:::image-end:::  

Visual Studio pode exibir erros, pois seu projeto não tem o arquivo de header WebView2.  Os erros devem ser corrigidos após a [Etapa 2](#step-2---install-webview2-sdk).  

## <a name="step-2---install-webview2-sdk"></a>Etapa 2 - Instalar o SDK WebView2  

Adicione o SDK WebView2 ao projeto.  Use NuGet para instalar o SDK win32.  

1.  Passe o mouse no projeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Gerenciar NuGet Pacotes**.  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Gerenciar pacotes NuGet" lightbox="../media/manage-nuget-packages.png":::
       Gerenciar pacotes NuGet  
    :::image-end:::  
    
1.  Instale a biblioteca Windows implementação.  
    1.  Na barra de pesquisa, digite `Microsoft.Windows.ImplementationLibrary` > escolha **Microsoft.Windows. ImplementationLibrary**.  
    1.  Na janela do lado direito, escolha **Instalar**.  NuGet baixa a biblioteca para seu computador.  
        
        > [!NOTE]
        > A [Windows biblioteca de][GithubMicrosoftWilMain] implementação e Windows de modelos [C++][CppCxWrlTemplateLibraryVS2019] do Tempo de Execução são opcionais e facilitam o trabalho com COM para o exemplo.  
        
        :::image type="complex" source="../media/wil.png" alt-text="Windows Biblioteca de Implementação" lightbox="../media/wil.png":::
           Windows Biblioteca de Implementação  
        :::image-end:::  
        
1.  Instale o SDK WebView2.  
    1.  Na barra de pesquisa, digite `Microsoft.Web.WebView2` > escolha **Microsoft.Web.WebView2**.  
    1.  Na janela do lado direito, escolha **Instalar**.  NuGet baixa o SDK em seu computador.  
        
        :::image type="complex" source="../media/nuget.png" alt-text="NuGet Gerenciador de Pacotes" lightbox="../media/nuget.png":::
           NuGet Gerenciador de Pacotes
        :::image-end:::  
        
1.  Adicione o header WebView2 ao seu projeto.  
    :::row:::
       :::column span="1":::
          No arquivo, copie o trecho de código a seguir e `HelloWebView.cpp` o colará após a última `#include` linha.  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          A seção include deve ser semelhante ao trecho de código a seguir.  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
Pronto para usar e criar na API WebView2.  

### <a name="build-your-empty-sample-app"></a>Criar seu aplicativo de exemplo vazio  

Para criar e executar o aplicativo de exemplo, selecione `F5` .  Seu aplicativo exibe uma janela vazia.  

:::image type="complex" source="../media/empty-app.png" alt-text="Aplicativo vazio" lightbox="../media/empty-app.png":::
   Aplicativo vazio  
:::image-end:::  

## <a name="step-3---create-a-single-webview-within-the-parent-window"></a>Etapa 3 - Criar um único WebView dentro da janela pai  

Adicione um WebView à janela principal.  

 Use o método para configurar o ambiente e localizar o navegador `CreateCoreWebView2Environment` Microsoft Edge \(Chromium\) que está visando o controle.  Você também pode usar o método se quiser especificar o local do navegador, a pasta do usuário, os sinalizadores do navegador e assim por diante, em vez de `CreateCoreWebView2EnvironmentWithOptions` usar a configuração padrão.  Após a conclusão do método, execute o método dentro do retorno de chamada e execute o método `CreateCoreWebView2Environment` `ICoreWebView2Environment::CreateCoreWebView2Controller` para obter o `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` `ICoreWebView2Controller::get_CoreWebView2` WebView associado.  

No retorno de chamada, de definir mais algumas configurações, resize o WebView para obter 100% da janela pai e navegue até Bing.  

Copie o seguinte trecho de código e colar depois `HelloWebView.cpp` do comentário e antes do `// <-- WebView2 sample code starts here -->` `// <-- WebView2 sample code ends here -->` comentário.  

```cpp
// Step 3 - Create a single WebView within the parent window
// Locate the browser and set up the environment for WebView
CreateCoreWebView2EnvironmentWithOptions(nullptr, nullptr, nullptr,
    Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
        [hWnd](HRESULT result, ICoreWebView2Environment* env) -> HRESULT {
        
            // Create a CoreWebView2Controller and get the associated CoreWebView2 whose parent is the main window hWnd
            env->CreateCoreWebView2Controller(hWnd, Callback<ICoreWebView2CreateCoreWebView2ControllerCompletedHandler>(
                [hWnd](HRESULT result, ICoreWebView2Controller* controller) -> HRESULT {
                if (controller != nullptr) {
                    webviewController = controller;
                    webviewController->get_CoreWebView2(&webviewWindow);
                }
                
                // Add a few settings for the webview
                // The demo step is redundant since the values are the default settings
                ICoreWebView2Settings* Settings;
                webviewWindow->get_Settings(&Settings);
                Settings->put_IsScriptEnabled(TRUE);
                Settings->put_AreDefaultScriptDialogsEnabled(TRUE);
                Settings->put_IsWebMessageEnabled(TRUE);
                
                // Resize WebView to fit the bounds of the parent window
                RECT bounds;
                GetClientRect(hWnd, &bounds);
                webviewController->put_Bounds(bounds);
                
                // Schedule an async task to navigate to Bing
                webviewWindow->Navigate(L"https://www.bing.com/");
                
                // Step 4 - Navigation events
                
                // Step 5 - Scripting
                
                // Step 6 - Communication between host and web content
                
                return S_OK;
            }).Get());
        return S_OK;
    }).Get());
```  

### <a name="build-your-bing-sample-app"></a>Criar seu Bing de exemplo  

Para criar e executar o aplicativo, selecione `F5` .  Agora você tem uma janela WebView exibindo a Bing página.  

:::image type="complex" source="../media/bing-window.png" alt-text="Bing janela" lightbox="../media/bing-window.png":::
   Bing janela  
:::image-end:::  

## <a name="step-4---navigation-events"></a>Etapa 4 - Eventos de navegação  

A equipe do WebView já cobriu a navegação para a URL usando o `ICoreWebView2::Navigate` método na última etapa.  Durante a navegação, o WebView dispara uma sequência de eventos aos quais o host pode ouvir.  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

Para obter mais informações, navegue até [Eventos de navegação][Webview2ConceptsNavigationEvents].  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegação" lightbox="../media/navigation-events.png":::
   Eventos de navegação  
:::image-end:::  

Em casos de erro, um ou mais dos seguintes eventos podem ocorrer, dependendo se a navegação é continuada para uma página da Web de erro.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

> [!NOTE]
> Se ocorrer um redirecionamento HTTP, haverá vários `NavigationStarting` eventos em uma linha.  

Como exemplo de uso dos eventos, registre um manipulador para o `NavigationStarting` evento para cancelar qualquer solicitação que não seja https.  Copie o seguinte trecho de código e colar em `HelloWebView.cpp` .  

```cpp
// register an ICoreWebView2NavigationStartingEventHandler to cancel any non-https navigation
EventRegistrationToken token;
webviewWindow->add_NavigationStarting(Callback<ICoreWebView2NavigationStartingEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2NavigationStartingEventArgs * args) -> HRESULT {
        PWSTR uri;
        args->get_Uri(&uri);
        std::wstring source(uri);
        if (source.substr(0, 5) != L"https") {
            args->put_Cancel(true);
        }
        CoTaskMemFree(uri);
        return S_OK;
    }).Get(), &token);
```  

Agora, o aplicativo não navega para sites que não são https.  Você pode usar mecanismo semelhante para realizar outras tarefas, como restringir a navegação em seu próprio domínio.  

## <a name="step-5---scripting"></a>Etapa 5 - Scripting  

Você pode usar aplicativos host para injetar código JavaScript em controles WebView2 no tempo de execução.  Você pode tarefa webView para executar JavaScript arbitrário ou adicionar scripts de inicialização.  O JavaScript injetado se aplica a todos os novos documentos de nível superior e a todos os quadros filho até que o JavaScript seja removido.  O JavaScript injetado é executado com tempo específico.  

*   Execute-o após a criação do objeto global.  
*   Execute-o antes que qualquer outro script incluído no documento HTML seja executado.  

Copie o seguinte trecho de código e colar em `HelloWebView.cpp` .  

```cpp
// Schedule an async task to add initialization script that freezes the Object object
webviewWindow->AddScriptToExecuteOnDocumentCreated(L"Object.freeze(Object);", nullptr);
// Schedule an async task to get the document URL
webviewWindow->ExecuteScript(L"window.document.URL;", Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
    [](HRESULT errorCode, LPCWSTR resultObjectAsJson) -> HRESULT {
        LPCWSTR URL = resultObjectAsJson;
        //doSomethingWithURL(URL);
        return S_OK;
    }).Get());
```  

Agora, o WebView sempre congelará o `Object` objeto e retornará o documento de página uma vez.  

> [!NOTE] 
> As APIs de injeção de script \(e algumas outras APIs webView2\) são assíncronas, você deve usar retornos de chamada se o código for necessário ser executado em uma ordem específica.  

## <a name="step-6---communication-between-host-and-web-content"></a>Etapa 6 - Comunicação entre conteúdo do host e da Web  

O host e o conteúdo da Web também podem se comunicar uns com os outros por meio do `postMessage` método.  O conteúdo da Web em execução em um WebView pode postar no host por meio do método e a mensagem é manipulada por qualquer manipulador de eventos `window.chrome.webview.postMessage` `ICoreWebView2WebMessageReceivedEventHandler` registrado no host.  Da mesma forma, o host pode enviar mensagens ao conteúdo da Web por meio ou método, que é `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` capturado por manipuladores adicionados do `window.chrome.webview.addEventListener` ouvinte.  O mecanismo de comunicação permite que o conteúdo da Web use recursos nativos passando mensagens para solicitar que o host execute APIs nativas.  

Como exemplo para entender o mecanismo, as etapas a seguir ocorrem quando você tenta saída da URL do documento no WebView.  

1.  O host registra um manipulador para retornar a mensagem recebida de volta ao conteúdo da Web  
1.  O host injeta um script no conteúdo da Web que registra um manipulador para imprimir mensagem do host  
1.  O host injeta um script no conteúdo da Web que posta a URL para o host  
1.  O manipulador do host é acionado e retorna a mensagem \(a URL\) para o conteúdo da Web  
1.  O manipulador do conteúdo da Web é acionado e imprime a mensagem do host \(a URL\)  

Copie o seguinte trecho de código e colar em `HelloWebView.cpp` .  

```cpp
// Set an event handler for the host to return received message back to the web content
webviewWindow->add_WebMessageReceived(Callback<ICoreWebView2WebMessageReceivedEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2WebMessageReceivedEventArgs * args) -> HRESULT {
        PWSTR message;
        args->TryGetWebMessageAsString(&message);
        // processMessage(&message);
        webview->PostWebMessageAsString(message);
        CoTaskMemFree(message);
        return S_OK;
    }).Get(), &token);

// Schedule an async task to add initialization script that
// 1) Add an listener to print message from the host
// 2) Post document URL to the host
webviewWindow->AddScriptToExecuteOnDocumentCreated(
    L"window.chrome.webview.addEventListener(\'message\', event => alert(event.data));" \
    L"window.chrome.webview.postMessage(window.document.URL);",
nullptr);
```  

### <a name="build-your-display-url-sample-app"></a>Criar seu aplicativo de exemplo de URL de exibição  

Para criar e executar o aplicativo, selecione `F5` .  A URL aparece em uma janela pop-up antes de navegar para uma página da Web.  

:::image type="complex" source="../media/show-url.png" alt-text="Url de exibição" lightbox="../media/show-url.png":::
   Url de exibição  
:::image-end:::  

Parabéns, você criou seu primeiro aplicativo WebView2.  

## <a name="next-steps"></a>Próximas etapas  

Para obter funcionalidades adicionais do WebView2 que não são abordadas neste artigo, revise os recursos a seguir.  

*   Para saber mais sobre como criar aplicativos WebView2, navegue até Práticas recomendadas de desenvolvimento [webView2.][WV2BestPractices]  
*   Para um exemplo abrangente de recursos WebView2, navegue até [WebView2 API Sample][GithubMicrosoftedgeWebview2samplesApisample].  
*   Para um aplicativo de exemplo criado usando WebView2, navegue até [WebView2Browser][GithubMicrosoftedgeWebview2browser].  
*   Para obter informações detalhadas sobre a API WebView2, navegue até [referência de API][Webview2ReferenceWin32].  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrar em contato com a equipe Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WV2BestPractices]: ../concepts/developer-guide.md "Práticas recomendadas de desenvolvimento do WebView2 | Microsoft Docs"  
[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 | Microsoft Edge Desenvolvedor"  

[Webview2ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "WebView2 Win32 C++ Reference | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegação | Microsoft Docs"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019&preserve-view=true "Windows Biblioteca de Modelos C++ do Tempo de Execução (WRL) | Microsoft Docs"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019&preserve-view=true "Passo a passo: criar um aplicativo de Windows desktop (C++) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser - MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentários do WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "Exemplo de API WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Windows Bibliotecas de Implementação (WIL) - microsoft/wil | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador WebView2"  
