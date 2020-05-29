---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle Microsoft Edge WebView 2
title: Microsoft Edge WebView 2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 0ab152e52b5e5d89cf493ff525ce53d9ab174e6d
ms.sourcegitcommit: 799fe63d961a37ada455bb36ef3ef0d8076e70bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2020
ms.locfileid: "10685677"
---
# Introdução ao WebView2 (Developer Preview)

Este guia passo a passo passa pelas funcionalidades comumente usadas de [WebView2 (Developer Preview)](https://aka.ms/webview) e obtém você para começar a criar seu primeiro aplicativo WebView2. Acesse a [referência de API](../reference/win32/0-9-488-reference-webview2.md) para saber mais sobre APIs individuais.  

## Pré-requisitos

* [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download/) instalado no sistema operacional compatível (atualmente Windows 10, Windows 8,1 e Windows 7). **Recomendamos usar o canal Canárias e a versão mínima necessária é 82.0.488.0**.
* [Visual Studio](https://visualstudio.microsoft.com/) 2015 ou posterior com suporte a C++ instalado.

## Etapa 1-criar um aplicativo Win32 de janela única

Vamos começar com um projeto de área de trabalho básico contendo uma única janela principal. Como este não é o foco principal deste guia passo a passo, usaremos o código de exemplo modificado do [passo-a-passo: criar um aplicativo de área de trabalho tradicional do Windows (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019). [Baixe](https://aka.ms/HelloWebView) a amostra modificada para começar.

Abra **WebView2GettingStarted. sln** no Visual Studio. Se você estiver usando uma versão mais antiga do Visual Studio, clique com o botão direito do mouse no projeto **WebView2GettingStarted** e clique em **Propriedades**. Em **Propriedades de configuração**  >  **geral**, modifique o conjunto de **ferramentas** de versão e plataforma do **SDK do Windows** para usar o SDK do Win10 e o conjunto de ferramentas do vs disponíveis para você.

![ferramenta-versão](../media/tool-version.png)

O Visual Studio pode mostrar alguns erros devido ao arquivo de cabeçalho WebView2 ausente, o que deve ficar indisponível quando a etapa 2 for concluída.

## Etapa 2-instalar o SDK do WebView2

Agora, vamos adicionar o SDK WebView2 ao projeto. Para a visualização do desenvolvedor, você pode instalar o SDK do Win32 via NuGet.

1. Clique com o botão direito do mouse no projeto e clique em **gerenciar pacotes NuGet**.

    ![Manage-NuGet-Packages](../media/manage-nuget-packages.png)

2. Digite **Microsoft. Windows. ImplementationLibrary** na barra de pesquisa, clique em **Microsoft. Windows. ImplementationLibrary** nos resultados e clique em **instalar** na janela do lado direito e instale o SDK mais recente. O NuGet baixará o SDK para seu computador. Embora possamos usar a [biblioteca de implementação do Windows](https://github.com/Microsoft/wil) e a biblioteca de [modelos C++ do Windows Runtime](/cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019) para facilitar o trabalho com com mais facilidade neste guia passo a passo, eles são completamente opcionais.

    ![ouvirá](../media/wil.png)

3. Digite **Microsoft. Web. WebView2** na barra de pesquisa, clique em **Microsoft. Web. WebView2** nos resultados e clique em **instalar** na janela do lado direito e instale o SDK mais recente. O NuGet baixará o SDK para seu computador.

    ![NuGet](../media/nuget.png)

4. Inclua o cabeçalho WebView2. Em **HelloWebView. cpp**, adicione `#include "WebView2.h"` abaixo das linhas de `#include` s.

    ```cpp
    ...
    #include <wrl.h>
    #include <wil/com.h>
    // include WebView2 header
    #include "WebView2.h"
    ```

Você está pronto para usar e compilar a API WebView2. Pressione F5 para compilar e executar o aplicativo de exemplo. Você deve ver um aplicativo exibindo uma janela vazia.

![aplicativo vazio](../media/empty-app.png)

## Etapa 3-criar uma única WebView dentro da janela pai

Agora, vamos adicionar um WebView à janela principal. Usaremos `CreateCoreWebView2Environment` para configurar o ambiente e localizar o navegador Microsoft Edge (Chromium) que o controla. Você também pode usar `CreateCoreWebView2EnvironmentWithOptions` se quiser especificar a localização do navegador, a pasta do usuário, os sinalizadores do navegador, etc., em vez de usar a configuração padrão. Após a conclusão do `CreateCoreWebView2Environment` , você poderá ligar `ICoreWebView2Environment::CreateCoreWebView2Controller` dentro do `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` retorno de chamada e chamar `ICoreWebView2Controller::get_CoreWebView2` para obter o WebView associado.

No retorno de chamada, também vamos definir algumas configurações, redimensionar a WebView para fazer 100% da janela pai e navegar até o Bing.

Copie o código a seguir para **HelloWebView. cpp** entre `// <-- WebView2 sample code starts here -->` e `// <-- WebView2 sample code ends here -->` .

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
                // this is a redundant demo step as they are the default settings values
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

Pressione F5 para compilar e executar o aplicativo. Agora você tem uma janela do WebView que exibe o Bing.

![Bing-janela](../media/bing-window.png)

## Etapa 4-eventos de navegação

Já abordamos navegar para a URL usando `ICoreWebView2::Navigate` na última etapa. Durante a navegação, o WebView aciona uma sequência de eventos que o host pode ouvir- `NavigationStarting` , `SourceChanged` ,, `ContentLoading` `HistoryChanged` e `NavigationCompleted` . Clique [aqui](../reference/win32/0-9-488/ICoreWebView2.md#navigation-events) para saber mais.

![navegação-eventos](../media/navigation-events.png)

Em casos de erro, pode ou não ser `SourceChanged` , `ContentLoading` ou `HistoryChanged` evento (s), dependendo se a navegação é continuada para uma página de erro. No caso de um redirecionamento HTTP, haverá vários `NavigationStarting` eventos em uma linha.

Como um exemplo de utilização desses eventos, vamos registrar um manipulador para `NavigationStarting` cancelar quaisquer solicitações que não sejam HTTPS. Copie o código a seguir para **HelloWebView. cpp** abaixo `// Step 4 - Navigation events` .

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

Agora o aplicativo não irá navegar para sites não HTTPS. Você pode usar um mecanismo semelhante para realizar outras tarefas, como restringir a navegação para dentro do seu próprio domínio.

## Etapa 5-scripting

O aplicativo de hospedagem também pode injetar JavaScript no WebView. Você pode executar uma tarefa WebView para executar JavaScript arbitrário ou adicionar scripts de inicialização. Os scripts de inicialização adicionados se aplicam a todas as futuras opções de navegação de documentos de nível superior e de quadro filho até serem removidas e executadas após a criação do objeto global e antes de qualquer outro script incluído no documento HTML ser executado.

Copie o seguinte código abaixo `// Step 5 - Scripting` .

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

Agora, o WebView sempre congelará o objeto objeto e retornará o documento de página uma vez.

**Observe que essas APIs de injeção de script (e algumas outras APIs do WebView2) são assíncronas, você deve usar retornos de chamada se o código deve ser executado em uma ordem específica.**

## Etapa 6 – comunicação entre o conteúdo do host e da Web

O host e o conteúdo da Web também podem se comunicar uns com os outros `postMessage` . O conteúdo da Web executado em uma WebView pode postar no host por meio da `window.chrome.webview.postMessage` mensagem, e a mensagem seria manipulada por qualquer pessoa registrada `ICoreWebView2WebMessageReceivedEventHandler` no host. Da mesma forma, o host pode enviar o conteúdo da Web por meio `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` de ou, que seria detectado por manipuladores adicionados `window.chrome.webview.addEventListener` . O mecanismo de comunicação permite que o conteúdo da Web use recursos nativos, passando mensagens para solicitar que o host chame APIs nativas.

Como exemplo para entender o mecanismo, vamos tentar imprimir a URL do documento no WebView com um pouco de detour,

1. o host registra um manipulador para retornar a mensagem recebida de volta para o conteúdo da Web
2. o host injeta um script para o conteúdo da Web que registra um manipulador para imprimir mensagens do host
3. o host injeta um script para o conteúdo da Web que envia a URL para o host
4. o manipulador do host é acionado e retorna a mensagem (a URL) ao conteúdo da Web
5. o manipulador do conteúdo da Web é disparado e imprime a mensagem do host (a URL)

Copie o seguinte código abaixo `// Step 6 - Communication between host and web content` ,

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

Pressione F5 para compilar e executar o aplicativo. Agora, ele mostrará URLs antes de navegar para páginas.

![show-URL](../media/show-url.png)

Parabéns, você acabou de criar seu primeiro aplicativo WebView2!

## Próximas etapas

Há muitas funcionalidades WebView2s que não são abordadas neste guia passo a passo.

Para saber mais:

* WebView2-out [API Sample](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample) para obter um exemplo abrangente de recursos do WebView2's.
* Fazer check-out [WebView2Browser](https://github.com/MicrosoftEdge/WebView2Browser) um aplicativo criado usando o WebView2.
* Explore a [referência de API](../reference/win32/0-9-488-reference-webview2.md) para obter informações detalhadas sobre nossa API.  

## Entrar em contato com a equipe do WebView2  

Ajude-nos a criar uma experiência WebView2 mais rica compartilhando seus comentários! Acesse nosso [repositório de comentários](https://aka.ms/webviewfeedback) para enviar solicitações de recursos ou relatórios de erros ou Pesquisar problemas conhecidos.
