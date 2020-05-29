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
# <span data-ttu-id="295ca-104">Introdução ao WebView2 (Developer Preview)</span><span class="sxs-lookup"><span data-stu-id="295ca-104">Getting Started with WebView2 (developer preview)</span></span>

<span data-ttu-id="295ca-105">Este guia passo a passo passa pelas funcionalidades comumente usadas de [WebView2 (Developer Preview)](https://aka.ms/webview) e obtém você para começar a criar seu primeiro aplicativo WebView2.</span><span class="sxs-lookup"><span data-stu-id="295ca-105">This walkthrough goes over the commonly used functionalities of [WebView2 (developer preview)](https://aka.ms/webview) and gets you started on creating your first WebView2 app.</span></span> <span data-ttu-id="295ca-106">Acesse a [referência de API](../reference/win32/0-9-488-reference-webview2.md) para saber mais sobre APIs individuais.</span><span class="sxs-lookup"><span data-stu-id="295ca-106">Visit [API reference](../reference/win32/0-9-488-reference-webview2.md) to learn more about individual APIs.</span></span>  

## <span data-ttu-id="295ca-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="295ca-107">Prerequisites</span></span>

* <span data-ttu-id="295ca-108">[Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download/) instalado no sistema operacional compatível (atualmente Windows 10, Windows 8,1 e Windows 7).</span><span class="sxs-lookup"><span data-stu-id="295ca-108">[Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download/) installed on supported OS (currently Windows 10, Windows 8.1, and Windows 7).</span></span> <span data-ttu-id="295ca-109">**Recomendamos usar o canal Canárias e a versão mínima necessária é 82.0.488.0**.</span><span class="sxs-lookup"><span data-stu-id="295ca-109">**We recommend using the Canary channel and the minimum required version is 82.0.488.0**.</span></span>
* <span data-ttu-id="295ca-110">[Visual Studio](https://visualstudio.microsoft.com/) 2015 ou posterior com suporte a C++ instalado.</span><span class="sxs-lookup"><span data-stu-id="295ca-110">[Visual Studio](https://visualstudio.microsoft.com/) 2015 or later with C++ support installed.</span></span>

## <span data-ttu-id="295ca-111">Etapa 1-criar um aplicativo Win32 de janela única</span><span class="sxs-lookup"><span data-stu-id="295ca-111">Step 1 - Create a single window win32 app</span></span>

<span data-ttu-id="295ca-112">Vamos começar com um projeto de área de trabalho básico contendo uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="295ca-112">We will start with a basic desktop project containing a single main window.</span></span> <span data-ttu-id="295ca-113">Como este não é o foco principal deste guia passo a passo, usaremos o código de exemplo modificado do [passo-a-passo: criar um aplicativo de área de trabalho tradicional do Windows (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="295ca-113">As this is not the main focus of this walkthrough, we will simply use modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span></span> <span data-ttu-id="295ca-114">[Baixe](https://aka.ms/HelloWebView) a amostra modificada para começar.</span><span class="sxs-lookup"><span data-stu-id="295ca-114">[Download](https://aka.ms/HelloWebView) the modified sample to get started.</span></span>

<span data-ttu-id="295ca-115">Abra **WebView2GettingStarted. sln** no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="295ca-115">Open **WebView2GettingStarted.sln** in Visual Studio.</span></span> <span data-ttu-id="295ca-116">Se você estiver usando uma versão mais antiga do Visual Studio, clique com o botão direito do mouse no projeto **WebView2GettingStarted** e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="295ca-116">If you are using an older version of Visual Studio, right click on the **WebView2GettingStarted** project and click **Properties**.</span></span> <span data-ttu-id="295ca-117">Em **Propriedades de configuração**  >  **geral**, modifique o conjunto de **ferramentas** de versão e plataforma do **SDK do Windows** para usar o SDK do Win10 e o conjunto de ferramentas do vs disponíveis para você.</span><span class="sxs-lookup"><span data-stu-id="295ca-117">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and VS toolset available to you.</span></span>

![ferramenta-versão](../media/tool-version.png)

<span data-ttu-id="295ca-119">O Visual Studio pode mostrar alguns erros devido ao arquivo de cabeçalho WebView2 ausente, o que deve ficar indisponível quando a etapa 2 for concluída.</span><span class="sxs-lookup"><span data-stu-id="295ca-119">Visual Studio may show some errors due to missing WebView2 header file, which should go away once Step 2 is completed.</span></span>

## <span data-ttu-id="295ca-120">Etapa 2-instalar o SDK do WebView2</span><span class="sxs-lookup"><span data-stu-id="295ca-120">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="295ca-121">Agora, vamos adicionar o SDK WebView2 ao projeto.</span><span class="sxs-lookup"><span data-stu-id="295ca-121">Now let's add the WebView2 SDK into the project.</span></span> <span data-ttu-id="295ca-122">Para a visualização do desenvolvedor, você pode instalar o SDK do Win32 via NuGet.</span><span class="sxs-lookup"><span data-stu-id="295ca-122">For the developer preview, you can install the Win32 SDK via Nuget.</span></span>

1. <span data-ttu-id="295ca-123">Clique com o botão direito do mouse no projeto e clique em **gerenciar pacotes NuGet**.</span><span class="sxs-lookup"><span data-stu-id="295ca-123">Right click the project and click **Manage Nuget Packages**.</span></span>

    ![Manage-NuGet-Packages](../media/manage-nuget-packages.png)

2. <span data-ttu-id="295ca-125">Digite **Microsoft. Windows. ImplementationLibrary** na barra de pesquisa, clique em **Microsoft. Windows. ImplementationLibrary** nos resultados e clique em **instalar** na janela do lado direito e instale o SDK mais recente.</span><span class="sxs-lookup"><span data-stu-id="295ca-125">Enter **Microsoft.Windows.ImplementationLibrary** in the search bar, click **Microsoft.Windows.ImplementationLibrary** from the results, and click **Install** inthe right hand side window and install the latest SDK.</span></span> <span data-ttu-id="295ca-126">O NuGet baixará o SDK para seu computador.</span><span class="sxs-lookup"><span data-stu-id="295ca-126">Nuget will download the SDK to your machine.</span></span> <span data-ttu-id="295ca-127">Embora possamos usar a [biblioteca de implementação do Windows](https://github.com/Microsoft/wil) e a biblioteca de [modelos C++ do Windows Runtime](/cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019) para facilitar o trabalho com com mais facilidade neste guia passo a passo, eles são completamente opcionais.</span><span class="sxs-lookup"><span data-stu-id="295ca-127">While we use [Windows Implementation Library](https://github.com/Microsoft/wil) and [Windows Runtime C++ Template Library](/cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019) to make working with COM easier in this walkthrough, they are completely optional.</span></span>

    ![ouvirá](../media/wil.png)

3. <span data-ttu-id="295ca-129">Digite **Microsoft. Web. WebView2** na barra de pesquisa, clique em **Microsoft. Web. WebView2** nos resultados e clique em **instalar** na janela do lado direito e instale o SDK mais recente.</span><span class="sxs-lookup"><span data-stu-id="295ca-129">Enter **Microsoft.Web.WebView2** in the search bar, click **Microsoft.Web.WebView2** from the results, and click **Install** in the right hand side window and install the latest SDK.</span></span> <span data-ttu-id="295ca-130">O NuGet baixará o SDK para seu computador.</span><span class="sxs-lookup"><span data-stu-id="295ca-130">Nuget will download the SDK to your machine.</span></span>

    ![NuGet](../media/nuget.png)

4. <span data-ttu-id="295ca-132">Inclua o cabeçalho WebView2.</span><span class="sxs-lookup"><span data-stu-id="295ca-132">Include the WebView2 header.</span></span> <span data-ttu-id="295ca-133">Em **HelloWebView. cpp**, adicione `#include "WebView2.h"` abaixo das linhas de `#include` s.</span><span class="sxs-lookup"><span data-stu-id="295ca-133">In **HelloWebView.cpp**, add `#include "WebView2.h"` below the lines of `#include`s.</span></span>

    ```cpp
    ...
    #include <wrl.h>
    #include <wil/com.h>
    // include WebView2 header
    #include "WebView2.h"
    ```

<span data-ttu-id="295ca-134">Você está pronto para usar e compilar a API WebView2.</span><span class="sxs-lookup"><span data-stu-id="295ca-134">You are all set to use and build against the WebView2 API.</span></span> <span data-ttu-id="295ca-135">Pressione F5 para compilar e executar o aplicativo de exemplo.</span><span class="sxs-lookup"><span data-stu-id="295ca-135">Press F5 to build and run the sample app.</span></span> <span data-ttu-id="295ca-136">Você deve ver um aplicativo exibindo uma janela vazia.</span><span class="sxs-lookup"><span data-stu-id="295ca-136">You should see an app displaying an empty window.</span></span>

![aplicativo vazio](../media/empty-app.png)

## <span data-ttu-id="295ca-138">Etapa 3-criar uma única WebView dentro da janela pai</span><span class="sxs-lookup"><span data-stu-id="295ca-138">Step 3 - Create a single WebView within the parent window</span></span>

<span data-ttu-id="295ca-139">Agora, vamos adicionar um WebView à janela principal.</span><span class="sxs-lookup"><span data-stu-id="295ca-139">Now let's add a WebView to the main window.</span></span> <span data-ttu-id="295ca-140">Usaremos `CreateCoreWebView2Environment` para configurar o ambiente e localizar o navegador Microsoft Edge (Chromium) que o controla.</span><span class="sxs-lookup"><span data-stu-id="295ca-140">We'll use `CreateCoreWebView2Environment` to set up the environment and locate the Microsoft Edge (Chromium) browser powering the control.</span></span> <span data-ttu-id="295ca-141">Você também pode usar `CreateCoreWebView2EnvironmentWithOptions` se quiser especificar a localização do navegador, a pasta do usuário, os sinalizadores do navegador, etc., em vez de usar a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="295ca-141">You can also use `CreateCoreWebView2EnvironmentWithOptions` if you want to specify browser location, user folder, browser flags, etc., instead of using the default setting.</span></span> <span data-ttu-id="295ca-142">Após a conclusão do `CreateCoreWebView2Environment` , você poderá ligar `ICoreWebView2Environment::CreateCoreWebView2Controller` dentro do `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` retorno de chamada e chamar `ICoreWebView2Controller::get_CoreWebView2` para obter o WebView associado.</span><span class="sxs-lookup"><span data-stu-id="295ca-142">Upon the completion of `CreateCoreWebView2Environment`, you'll be able to call `ICoreWebView2Environment::CreateCoreWebView2Controller` inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and call `ICoreWebView2Controller::get_CoreWebView2` to get the associated WebView.</span></span>

<span data-ttu-id="295ca-143">No retorno de chamada, também vamos definir algumas configurações, redimensionar a WebView para fazer 100% da janela pai e navegar até o Bing.</span><span class="sxs-lookup"><span data-stu-id="295ca-143">In the callback, let's also set a few settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>

<span data-ttu-id="295ca-144">Copie o código a seguir para **HelloWebView. cpp** entre `// <-- WebView2 sample code starts here -->` e `// <-- WebView2 sample code ends here -->` .</span><span class="sxs-lookup"><span data-stu-id="295ca-144">Copy the following code to **HelloWebView.cpp** between `// <-- WebView2 sample code starts here -->` and `// <-- WebView2 sample code ends here -->`.</span></span>

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

<span data-ttu-id="295ca-145">Pressione F5 para compilar e executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="295ca-145">Press F5 to build and run the app.</span></span> <span data-ttu-id="295ca-146">Agora você tem uma janela do WebView que exibe o Bing.</span><span class="sxs-lookup"><span data-stu-id="295ca-146">Now you have a WebView window displaying Bing.</span></span>

![Bing-janela](../media/bing-window.png)

## <span data-ttu-id="295ca-148">Etapa 4-eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="295ca-148">Step 4 - Navigation events</span></span>

<span data-ttu-id="295ca-149">Já abordamos navegar para a URL usando `ICoreWebView2::Navigate` na última etapa.</span><span class="sxs-lookup"><span data-stu-id="295ca-149">We already covered navigating to URL using `ICoreWebView2::Navigate` in the last step.</span></span> <span data-ttu-id="295ca-150">Durante a navegação, o WebView aciona uma sequência de eventos que o host pode ouvir- `NavigationStarting` , `SourceChanged` ,, `ContentLoading` `HistoryChanged` e `NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="295ca-150">During navigation, WebView fires a sequence of events that the host can listen to - `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span> <span data-ttu-id="295ca-151">Clique [aqui](../reference/win32/0-9-488/ICoreWebView2.md#navigation-events) para saber mais.</span><span class="sxs-lookup"><span data-stu-id="295ca-151">Click [here](../reference/win32/0-9-488/ICoreWebView2.md#navigation-events) to learn more.</span></span>

![navegação-eventos](../media/navigation-events.png)

<span data-ttu-id="295ca-153">Em casos de erro, pode ou não ser `SourceChanged` , `ContentLoading` ou `HistoryChanged` evento (s), dependendo se a navegação é continuada para uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="295ca-153">In error cases there may or may not be `SourceChanged`, `ContentLoading`, or `HistoryChanged` event(s) depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="295ca-154">No caso de um redirecionamento HTTP, haverá vários `NavigationStarting` eventos em uma linha.</span><span class="sxs-lookup"><span data-stu-id="295ca-154">In case of an HTTP redirect, there will be multiple `NavigationStarting` events in a row.</span></span>

<span data-ttu-id="295ca-155">Como um exemplo de utilização desses eventos, vamos registrar um manipulador para `NavigationStarting` cancelar quaisquer solicitações que não sejam HTTPS.</span><span class="sxs-lookup"><span data-stu-id="295ca-155">As an example of utilizing those events, let's register a handler for `NavigationStarting` to cancel any non-https requests.</span></span> <span data-ttu-id="295ca-156">Copie o código a seguir para **HelloWebView. cpp** abaixo `// Step 4 - Navigation events` .</span><span class="sxs-lookup"><span data-stu-id="295ca-156">Copy the following code to **HelloWebView.cpp** below `// Step 4 - Navigation events`.</span></span>

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

<span data-ttu-id="295ca-157">Agora o aplicativo não irá navegar para sites não HTTPS.</span><span class="sxs-lookup"><span data-stu-id="295ca-157">Now the app will not navigate to any non-https sites.</span></span> <span data-ttu-id="295ca-158">Você pode usar um mecanismo semelhante para realizar outras tarefas, como restringir a navegação para dentro do seu próprio domínio.</span><span class="sxs-lookup"><span data-stu-id="295ca-158">You can use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>

## <span data-ttu-id="295ca-159">Etapa 5-scripting</span><span class="sxs-lookup"><span data-stu-id="295ca-159">Step 5 - Scripting</span></span>

<span data-ttu-id="295ca-160">O aplicativo de hospedagem também pode injetar JavaScript no WebView.</span><span class="sxs-lookup"><span data-stu-id="295ca-160">The hosting app can also inject JavaScript into WebView.</span></span> <span data-ttu-id="295ca-161">Você pode executar uma tarefa WebView para executar JavaScript arbitrário ou adicionar scripts de inicialização.</span><span class="sxs-lookup"><span data-stu-id="295ca-161">You can task WebView to execute arbitrary JavaScript or add initialization scripts.</span></span> <span data-ttu-id="295ca-162">Os scripts de inicialização adicionados se aplicam a todas as futuras opções de navegação de documentos de nível superior e de quadro filho até serem removidas e executadas após a criação do objeto global e antes de qualquer outro script incluído no documento HTML ser executado.</span><span class="sxs-lookup"><span data-stu-id="295ca-162">Added initialization scripts apply to all future top level document and child frame navigation until removed, and run after the global object has been created and before any other script included by the HTML document is executed.</span></span>

<span data-ttu-id="295ca-163">Copie o seguinte código abaixo `// Step 5 - Scripting` .</span><span class="sxs-lookup"><span data-stu-id="295ca-163">Copy the following code below `// Step 5 - Scripting`.</span></span>

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

<span data-ttu-id="295ca-164">Agora, o WebView sempre congelará o objeto objeto e retornará o documento de página uma vez.</span><span class="sxs-lookup"><span data-stu-id="295ca-164">Now WebView will always freeze the Object object and return the page document once.</span></span>

**<span data-ttu-id="295ca-165">Observe que essas APIs de injeção de script (e algumas outras APIs do WebView2) são assíncronas, você deve usar retornos de chamada se o código deve ser executado em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="295ca-165">Note that these script injection APIs (and some other WebView2 APIs) are asynchronous, you should use callbacks if code is to be executed in a particular order.</span></span>**

## <span data-ttu-id="295ca-166">Etapa 6 – comunicação entre o conteúdo do host e da Web</span><span class="sxs-lookup"><span data-stu-id="295ca-166">Step 6 - Communication between host and web content</span></span>

<span data-ttu-id="295ca-167">O host e o conteúdo da Web também podem se comunicar uns com os outros `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="295ca-167">The host and the web content can also communicate with each other through `postMessage`.</span></span> <span data-ttu-id="295ca-168">O conteúdo da Web executado em uma WebView pode postar no host por meio da `window.chrome.webview.postMessage` mensagem, e a mensagem seria manipulada por qualquer pessoa registrada `ICoreWebView2WebMessageReceivedEventHandler` no host.</span><span class="sxs-lookup"><span data-stu-id="295ca-168">The web content running within a WebView can post to the host through `window.chrome.webview.postMessage`, and the message would be handled by any registered `ICoreWebView2WebMessageReceivedEventHandler` on the host.</span></span> <span data-ttu-id="295ca-169">Da mesma forma, o host pode enviar o conteúdo da Web por meio `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` de ou, que seria detectado por manipuladores adicionados `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="295ca-169">Likewise, the host can message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON`, which would be caught by handlers added from `window.chrome.webview.addEventListener`.</span></span> <span data-ttu-id="295ca-170">O mecanismo de comunicação permite que o conteúdo da Web use recursos nativos, passando mensagens para solicitar que o host chame APIs nativas.</span><span class="sxs-lookup"><span data-stu-id="295ca-170">The communication mechanism allows the web content to utilize native capabilities by passing messages to ask the host to call native APIs.</span></span>

<span data-ttu-id="295ca-171">Como exemplo para entender o mecanismo, vamos tentar imprimir a URL do documento no WebView com um pouco de detour,</span><span class="sxs-lookup"><span data-stu-id="295ca-171">As an example to understand the mechanism, let's try printing out the document URL in WebView with a little detour,</span></span>

1. <span data-ttu-id="295ca-172">o host registra um manipulador para retornar a mensagem recebida de volta para o conteúdo da Web</span><span class="sxs-lookup"><span data-stu-id="295ca-172">the host registers a handler to return received message back to the web content</span></span>
2. <span data-ttu-id="295ca-173">o host injeta um script para o conteúdo da Web que registra um manipulador para imprimir mensagens do host</span><span class="sxs-lookup"><span data-stu-id="295ca-173">the host injects a script to the web content that registers a handler to print message from the host</span></span>
3. <span data-ttu-id="295ca-174">o host injeta um script para o conteúdo da Web que envia a URL para o host</span><span class="sxs-lookup"><span data-stu-id="295ca-174">the host injects a script to the web content that posts the URL to the host</span></span>
4. <span data-ttu-id="295ca-175">o manipulador do host é acionado e retorna a mensagem (a URL) ao conteúdo da Web</span><span class="sxs-lookup"><span data-stu-id="295ca-175">the host's handler is triggered and returns the message (the URL) to the web content</span></span>
5. <span data-ttu-id="295ca-176">o manipulador do conteúdo da Web é disparado e imprime a mensagem do host (a URL)</span><span class="sxs-lookup"><span data-stu-id="295ca-176">the web content's handler is triggered and prints the host's message (the URL)</span></span>

<span data-ttu-id="295ca-177">Copie o seguinte código abaixo `// Step 6 - Communication between host and web content` ,</span><span class="sxs-lookup"><span data-stu-id="295ca-177">Copy the following code below `// Step 6 - Communication between host and web content`,</span></span>

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

<span data-ttu-id="295ca-178">Pressione F5 para compilar e executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="295ca-178">Press F5 to build and run the app.</span></span> <span data-ttu-id="295ca-179">Agora, ele mostrará URLs antes de navegar para páginas.</span><span class="sxs-lookup"><span data-stu-id="295ca-179">It will now show URLs before navigating to pages.</span></span>

![show-URL](../media/show-url.png)

<span data-ttu-id="295ca-181">Parabéns, você acabou de criar seu primeiro aplicativo WebView2!</span><span class="sxs-lookup"><span data-stu-id="295ca-181">Congratulations, you've just built your first WebView2 app!</span></span>

## <span data-ttu-id="295ca-182">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="295ca-182">Next Steps</span></span>

<span data-ttu-id="295ca-183">Há muitas funcionalidades WebView2s que não são abordadas neste guia passo a passo.</span><span class="sxs-lookup"><span data-stu-id="295ca-183">There are plenty of WebView2 functionalities that are not covered in this walkthrough.</span></span>

<span data-ttu-id="295ca-184">Para saber mais:</span><span class="sxs-lookup"><span data-stu-id="295ca-184">To learn more:</span></span>

* <span data-ttu-id="295ca-185">WebView2-out [API Sample](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample) para obter um exemplo abrangente de recursos do WebView2's.</span><span class="sxs-lookup"><span data-stu-id="295ca-185">Checkout [WebView2 API Sample](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample) for a comprehensive example of WebView2's capabilities.</span></span>
* <span data-ttu-id="295ca-186">Fazer check-out [WebView2Browser](https://github.com/MicrosoftEdge/WebView2Browser) um aplicativo criado usando o WebView2.</span><span class="sxs-lookup"><span data-stu-id="295ca-186">Checkout [WebView2Browser](https://github.com/MicrosoftEdge/WebView2Browser) an application built using WebView2.</span></span>
* <span data-ttu-id="295ca-187">Explore a [referência de API](../reference/win32/0-9-488-reference-webview2.md) para obter informações detalhadas sobre nossa API.</span><span class="sxs-lookup"><span data-stu-id="295ca-187">Please explore [API reference](../reference/win32/0-9-488-reference-webview2.md) for detailed information about our API.</span></span>  

## <span data-ttu-id="295ca-188">Entrar em contato com a equipe do WebView2</span><span class="sxs-lookup"><span data-stu-id="295ca-188">Getting in touch with the WebView2 team</span></span>  

<span data-ttu-id="295ca-189">Ajude-nos a criar uma experiência WebView2 mais rica compartilhando seus comentários!</span><span class="sxs-lookup"><span data-stu-id="295ca-189">Help us build a richer WebView2 experience by sharing your feedback!</span></span> <span data-ttu-id="295ca-190">Acesse nosso [repositório de comentários](https://aka.ms/webviewfeedback) para enviar solicitações de recursos ou relatórios de erros ou Pesquisar problemas conhecidos.</span><span class="sxs-lookup"><span data-stu-id="295ca-190">Visit our [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports or search for known issues.</span></span>
