---
description: Guia de introdução ao WebView2 para aplicativos Win32
title: Introdução ao WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 906ddbea08440aaa0f1fd7e32550c3b1790ba8a1
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119098"
---
# Introdução ao WebView2 (Developer Preview)  

O conteúdo a seguir orienta você pelas funcionalidades comumente usadas da [WebView2 (Developer Preview)][Webview2Index] e fornece um ponto de partida para criar seu primeiro aplicativo WebView2.  Para obter mais informações sobre APIs individuais do WebView2, consulte [referência de API][Webview2ReferenceWin32].  

## Pré-requisitos  

*   [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado em um sistema operacional com suporte \ (atualmente o Windows 10, o Windows 8,1 e o Windows 7 \).  
    
    > [!NOTE]
    > A equipe WebView recomenda usar o canal Canárias e a versão mínima necessária é 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2015 ou posterior com suporte a C++ instalado.  

## Etapa 1-criar um aplicativo Win32 de janela única  

Comece com um projeto de área de trabalho básico contendo uma única janela principal.  Para melhor focalizar o guia passo a passo, você está usando código de exemplo modificado do [passo-a-passo: criar um aplicativo de área de trabalho tradicional do Windows (C++)][CppWindowsWalkthroughCreatingDesktopApplication] para o aplicativo de exemplo.  Para baixar o exemplo modificado e começar, consulte [exemplos de WebView2][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].  

No Visual Studio, abra `WebView2GettingStarted.sln` .  Se você estiver usando uma versão mais antiga do Visual Studio, passe o mouse sobre o projeto **WebView2GettingStarted** , abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **Propriedades**.  Em **Propriedades de configuração**  >  **geral**, modifique o conjunto de **ferramentas** do **SDK do Windows** e a plataforma para usar o SDK do Win10 e o conjunto de ferramentas do Visual Studio \ (vs Toolset \) disponíveis para você.  

:::image type="complex" source="../media/tool-version.png" alt-text="Versão da ferramenta":::
   Versão da ferramenta  
:::image-end:::  

O Visual Studio pode mostrar alguns erros devido ao arquivo de cabeçalho WebView2 ausente, que deve ficar ausente após a conclusão da etapa 2.  

## Etapa 2-instalar o SDK do WebView2  

Adicione o SDK WebView2 ao projeto.  Para a visualização do desenvolvedor, você pode instalar o SDK do Win32 usando o NuGet.  

1.  Passe o cursor do mouse sobre o projeto, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **gerenciar pacotes NuGet**.  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Versão da ferramenta":::
       Gerenciar pacotes NuGet  
    :::image-end:::  
    
1.  Instale a biblioteca de implementação do Windows.  
    1.  Digite `Microsoft.Windows.ImplementationLibrary` na barra de pesquisa, selecione **Microsoft. Windows. ImplementationLibrary** nos resultados e selecione **instalar** na janela do lado direito.  O NuGet baixa o SDK para seu computador.  
        
        > [!NOTE] 
        > A [biblioteca de implementação do Windows][GithubMicrosoftWilMain] e a [biblioteca de modelos do Windows Runtime C++][CppCxWrlTemplateLibraryVS2019] são opcionais e foram adicionadas para facilitar o trabalho com com mais facilidade para o exemplo.  
        
        :::image type="complex" source="../media/wil.png" alt-text="Versão da ferramenta":::
           Biblioteca de implementação do Windows  
        :::image-end:::  
        
1.  Instale o SDK do WebView2.  
    1.  Digite `Microsoft.Web.WebView2` na barra de pesquisa, selecione **Microsoft. Web. WebView2** nos resultados e selecione **instalar** na janela do lado direito.  O NuGet baixa o SDK para seu computador.  
        
        :::image type="complex" source="../media/nuget.png" alt-text="Versão da ferramenta":::
           Gerenciador de pacotes NuGet
        :::image-end:::  
        
1.  Adicione o cabeçalho WebView2 ao seu projeto.  
    :::row:::
       :::column span="1":::
          Abrir `HelloWebView.cpp` , copie o trecho de código a seguir e cole em `HelloWebView.cpp` após a última `#include` linha.  
          
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
    
Você está pronto para usar e compilar a API WebView2.  

### Criar seu aplicativo de exemplo vazio  

Pressione `F5` para compilar e executar o aplicativo de exemplo.  Você deve ver um aplicativo exibindo uma janela vazia.  

:::image type="complex" source="../media/empty-app.png" alt-text="Versão da ferramenta":::
   Aplicativo vazio  
:::image-end:::  

## Etapa 3-criar uma única WebView dentro da janela pai  

Adicione um WebView à janela principal.  Use o `CreateCoreWebView2Environment` método para configurar o ambiente e localizar o navegador Microsoft Edge \ (Chromium \) que o controla.  Você também pode usar o `CreateCoreWebView2EnvironmentWithOptions` método se quiser especificar o local do navegador, a pasta do usuário, os sinalizadores do navegador e assim por diante, em vez de usar a configuração padrão.  Após a conclusão do `CreateCoreWebView2Environment` método, você poderá executar o `ICoreWebView2Environment::CreateCoreWebView2Controller` método dentro do `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` retorno de chamada e executar o `ICoreWebView2Controller::get_CoreWebView2` método para obter o WebView associado.  

No retorno de chamada, defina algumas configurações adicionais, redimensione a WebView para fazer 100% da janela pai e navegue até Bing.  

Copie o trecho de código a seguir e cole em `HelloWebView.cpp` após a `// <-- WebView2 sample code starts here -->` anotação e antes da `// <-- WebView2 sample code ends here -->` anotação.  

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


### Criar seu aplicativo de exemplo do Bing  

Pressione `F5` para compilar e executar o aplicativo.  Agora você tem uma janela do WebView que exibe a página do Bing.  

:::image type="complex" source="../media/bing-window.png" alt-text="Versão da ferramenta":::
   Janela do Bing  
:::image-end:::  

## Etapa 4-eventos de navegação  

A equipe da WebView já abordou navegar para a URL usando o `ICoreWebView2::Navigate` método na última etapa.  Durante a navegação, o WebView aciona uma sequência de eventos que o host pode ouvir.  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

Para obter mais informações, consulte [eventos de navegação][Webview2ConceptsNavigationEvents].  

:::image type="complex" source="../media/navigation-events.png" alt-text="Versão da ferramenta":::
   Eventos de navegação  
:::image-end:::  

Em casos de erro, um ou mais dos seguintes eventos podem ocorrer dependendo se a navegação é continuada para uma página de erro.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

No caso de um redirecionamento HTTP, há vários `NavigationStarting` eventos em uma linha.  

Como um exemplo de utilização dos eventos, registre um manipulador para o `NavigationStarting` evento para cancelar quaisquer solicitações que não sejam HTTPS.  Copie o trecho de código a seguir e cole em `HelloWebView.cpp` .  

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

Agora o aplicativo não está navegando para sites não HTTPS.  Você pode usar um mecanismo semelhante para realizar outras tarefas, como restringir a navegação para dentro do seu próprio domínio.  

## Etapa 5-scripting  

O aplicativo de hospedagem também pode injetar JavaScript em WebView.  Você pode executar uma tarefa de WebView para executar JavaScript arbitrário ou adicionar scripts de inicialização.  Os scripts de inicialização adicionados se aplicam a todas as futuras opções de navegação de documentos de nível superior e de quadro filho até serem removidas e executadas após a criação do objeto global e antes de qualquer outro script incluído no documento HTML ser executado.  

Copie o trecho de código a seguir e cole em `HelloWebView.cpp` .  

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

Agora, o WebView sempre deve congelar o `Object` objeto e retornar o documento de página uma vez.  

> [!NOTE] 
> As APIs de injeção de script \ (e outras APIs WebView2 \) são assíncronas, você deve usar retornos de chamada se o código for deve ser executado em uma ordem específica.  

## Etapa 6 – comunicação entre o conteúdo do host e da Web  

O host e o conteúdo da Web também podem se comunicar uns com os outros por meio do `postMessage` método.  O conteúdo da Web em execução em um WebView pode postar no host por meio do `window.chrome.webview.postMessage` método, e a mensagem é manipulada por qualquer registro registrado no `ICoreWebView2WebMessageReceivedEventHandler` manipulador de eventos do host.  Da mesma forma, o host pode enviar uma mensagem ao conteúdo da Web por meio `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` do ou método, que é detectado por manipuladores adicionados pelo `window.chrome.webview.addEventListener` ouvinte.  O mecanismo de comunicação permite que o conteúdo da Web use recursos nativos, passando mensagens para solicitar que o host chame APIs nativas.  

Como exemplo para entender o mecanismo, as seguintes etapas ocorrem quando você tenta imprimir a URL do documento no WebView.  

1.  O host registra um manipulador para retornar a mensagem recebida de volta para o conteúdo da Web  
1.  O host injeta um script para o conteúdo da Web que registra um manipulador para imprimir mensagens do host  
1.  O host injeta um script para o conteúdo da Web que envia a URL para o host  
1.  O manipulador do host é disparado e retorna a mensagem \ (a URL \) ao conteúdo da Web  
1.  O manipulador do conteúdo da Web é disparado e imprime a mensagem do host \ (a URL \)  

Copie o trecho de código a seguir e cole em `HelloWebView.cpp` .    

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

### Compilar o aplicativo de exemplo Mostrar URL  

Pressione `F5` para compilar e executar o aplicativo.  Você deve ver a URL em uma janela pop-up antes de navegar para uma página.  

:::image type="complex" source="../media/show-url.png" alt-text="Versão da ferramenta"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019&preserve-view=true "Biblioteca de modelos C++ do Windows Runtime (WRL) | Documentos da Microsoft"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019&preserve-view=true "Passo a passo: criar um aplicativo de área de trabalho tradicional do Windows (C++) | Documentos da Microsoft"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser-MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "Exemplo de API WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "Exemplos de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Bibliotecas de implementação do Windows (OUVIRÁ)-Microsoft/ouvirá | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar canais do Microsoft Edge Insider"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  
