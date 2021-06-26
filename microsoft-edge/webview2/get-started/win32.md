---
description: Guia de início com WebView2 para aplicativos Win32
title: Começar com WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Controller, controle de navegador, html de borda
ms.openlocfilehash: 2714f9a6cffea3cb7d53f9a4128d64920fd02dce
ms.sourcegitcommit: 7713eec634264b0c44b1bb426f5b466c44b4e005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2021
ms.locfileid: "11618383"
---
# <a name="get-started-with-webview2"></a><span data-ttu-id="08244-104">Começar com WebView2</span><span class="sxs-lookup"><span data-stu-id="08244-104">Get started with WebView2</span></span>  

<span data-ttu-id="08244-105">Neste artigo, você pode começar a criar seu primeiro aplicativo WebView2 e saber mais sobre os principais recursos do [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="08244-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="08244-106">Para obter mais informações sobre APIs webView2 individuais, navegue até [referência de API][Webview2ReferenceWin32].</span><span class="sxs-lookup"><span data-stu-id="08244-106">For more information about individual WebView2 APIs, navigate to [API reference][Webview2ReferenceWin32].</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="08244-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="08244-107">Prerequisites</span></span>  

<span data-ttu-id="08244-108">Certifique-se de instalar a lista de pré-requisitos a seguir antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="08244-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="08244-109">[WebView2 Runtime][Webview2Installer] ou qualquer canal Microsoft Edge [(Chromium)][MicrosoftedgeinsiderDownload] não estável instalado no sistema operacional com suporte \(atualmente Windows 10, Windows 8.1 e Windows 7\).</span><span class="sxs-lookup"><span data-stu-id="08244-109">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
*   <span data-ttu-id="08244-110">[Visual Studio][MicrosoftVisualstudioMain] 2015 ou posterior com suporte C++ instalado.</span><span class="sxs-lookup"><span data-stu-id="08244-110">[Visual Studio][MicrosoftVisualstudioMain] 2015 or later with C++ support installed.</span></span>  
    
## <a name="step-1---create-a-single-window-app"></a><span data-ttu-id="08244-111">Etapa 1 - Criar um aplicativo de janela única</span><span class="sxs-lookup"><span data-stu-id="08244-111">Step 1 - Create a single-window app</span></span>  

<span data-ttu-id="08244-112">Comece com um projeto de área de trabalho básico que contém uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="08244-112">Start with a basic desktop project that contains a single main window.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="08244-113">Para focalizar melhor o passo a passo, use o código de exemplo modificado do Passo a passo: Crie um aplicativo de área de trabalho Windows tradicional [(C++)][CppWindowsWalkthroughCreatingDesktopApplication] para seu aplicativo de exemplo.</span><span class="sxs-lookup"><span data-stu-id="08244-113">To better focus the walkthrough, use modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.</span></span>  <span data-ttu-id="08244-114">Para baixar o exemplo modificado e começar, navegue até [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span><span class="sxs-lookup"><span data-stu-id="08244-114">To download the modified sample and get started, navigate to [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span></span>  

1.  <span data-ttu-id="08244-115">Em Visual Studio, abra `WebView2GettingStarted.sln` .</span><span class="sxs-lookup"><span data-stu-id="08244-115">In Visual Studio, open `WebView2GettingStarted.sln`.</span></span>  
    <span data-ttu-id="08244-116">Se você usar uma versão mais antiga do Visual Studio, passe o mouse no projeto **WebView2GettingStarted,** abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="08244-116">If you use an older version of Visual Studio, hover on the **WebView2GettingStarted** project, open the contextual menu \(right-click\), and choose **Properties**.</span></span>  <span data-ttu-id="08244-117">Em **Propriedades**de Configuração Geral, modifique Windows Versão do SDK e Platform Toolset para usar o  >  \*\*\*\* SDK win10 e o \*\*\*\* Visual Studio ferramentas disponíveis para você. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="08244-117">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and Visual Studio toolset available to you.</span></span>  
    
:::image type="complex" source="../media/tool-version.png" alt-text="Versão da ferramenta" lightbox="../media/tool-version.png":::
   <span data-ttu-id="08244-119">Versão da ferramenta</span><span class="sxs-lookup"><span data-stu-id="08244-119">Tool version</span></span>  
:::image-end:::      

<span data-ttu-id="08244-120">Visual Studio pode exibir erros, pois seu projeto não tem o arquivo de header WebView2.</span><span class="sxs-lookup"><span data-stu-id="08244-120">Visual Studio may display errors, because your project is missing the WebView2 header file.</span></span>  <span data-ttu-id="08244-121">Os erros devem ser corrigidos após a [Etapa 2](#step-2---install-webview2-sdk).</span><span class="sxs-lookup"><span data-stu-id="08244-121">The errors should be fixed after [Step 2](#step-2---install-webview2-sdk).</span></span>  

## <a name="step-2---install-webview2-sdk"></a><span data-ttu-id="08244-122">Etapa 2 - Instalar o SDK WebView2</span><span class="sxs-lookup"><span data-stu-id="08244-122">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="08244-123">Adicione o SDK WebView2 ao projeto.</span><span class="sxs-lookup"><span data-stu-id="08244-123">Add the WebView2 SDK into the project.</span></span>  <span data-ttu-id="08244-124">Use NuGet para instalar o SDK win32.</span><span class="sxs-lookup"><span data-stu-id="08244-124">Use NuGet to install the Win32 SDK.</span></span>  

1.  <span data-ttu-id="08244-125">Passe o mouse no projeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Gerenciar NuGet Pacotes**.</span><span class="sxs-lookup"><span data-stu-id="08244-125">Hover on the project, open the contextual menu \(right-click\), and choose **Manage NuGet Packages**.</span></span>  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Gerenciar pacotes NuGet" lightbox="../media/manage-nuget-packages.png":::
       <span data-ttu-id="08244-127">Gerenciar pacotes NuGet</span><span class="sxs-lookup"><span data-stu-id="08244-127">Manage NuGet packages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="08244-128">Instale a biblioteca Windows implementação.</span><span class="sxs-lookup"><span data-stu-id="08244-128">Install the Windows Implementation Library.</span></span>  
    1.  <span data-ttu-id="08244-129">Na barra de pesquisa, digite `Microsoft.Windows.ImplementationLibrary` > escolha **Microsoft.Windows. ImplementationLibrary**.</span><span class="sxs-lookup"><span data-stu-id="08244-129">In the search bar, type `Microsoft.Windows.ImplementationLibrary` > choose **Microsoft.Windows.ImplementationLibrary**.</span></span>  
    1.  <span data-ttu-id="08244-130">Na janela do lado direito, escolha **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="08244-130">In the right-hand side window, choose **Install**.</span></span>  <span data-ttu-id="08244-131">NuGet baixa a biblioteca para seu computador.</span><span class="sxs-lookup"><span data-stu-id="08244-131">NuGet downloads the library to your machine.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="08244-132">A [Windows biblioteca de][GithubMicrosoftWilMain] implementação e Windows de modelos [C++][CppCxWrlTemplateLibraryVS2019] do Tempo de Execução são opcionais e facilitam o trabalho com COM para o exemplo.</span><span class="sxs-lookup"><span data-stu-id="08244-132">The [Windows Implementation Library][GithubMicrosoftWilMain] and [Windows Runtime C++ Template Library][CppCxWrlTemplateLibraryVS2019] are optional and make working with COM easier for the example.</span></span>  
        
        :::image type="complex" source="../media/wil.png" alt-text="Windows Biblioteca de Implementação" lightbox="../media/wil.png":::
           <span data-ttu-id="08244-134">Windows Biblioteca de Implementação</span><span class="sxs-lookup"><span data-stu-id="08244-134">Windows Implementation Library</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="08244-135">Instale o SDK WebView2.</span><span class="sxs-lookup"><span data-stu-id="08244-135">Install the WebView2 SDK.</span></span>  
    1.  <span data-ttu-id="08244-136">Na barra de pesquisa, digite `Microsoft.Web.WebView2` > escolha **Microsoft.Web.WebView2**.</span><span class="sxs-lookup"><span data-stu-id="08244-136">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
    1.  <span data-ttu-id="08244-137">Na janela do lado direito, escolha **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="08244-137">In the right-hand side window, choose **Install**.</span></span>  <span data-ttu-id="08244-138">NuGet baixa o SDK em seu computador.</span><span class="sxs-lookup"><span data-stu-id="08244-138">NuGet downloads the SDK to your machine.</span></span>  
        
        :::image type="complex" source="../media/nuget.png" alt-text="NuGet Gerenciador de Pacotes" lightbox="../media/nuget.png":::
           <span data-ttu-id="08244-140">NuGet Gerenciador de Pacotes</span><span class="sxs-lookup"><span data-stu-id="08244-140">NuGet Package Manager</span></span>
        :::image-end:::  
        
1.  <span data-ttu-id="08244-141">Adicione o header WebView2 ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="08244-141">Add WebView2 header to your project.</span></span>  
    
    :::row:::
       :::column span="1":::
          <span data-ttu-id="08244-142">No arquivo, copie o trecho de código a seguir e `HelloWebView.cpp` o colará após a última `#include` linha.</span><span class="sxs-lookup"><span data-stu-id="08244-142">In the `HelloWebView.cpp` file, copy the following code snippet and paste it after the last `#include` line.</span></span>  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          <span data-ttu-id="08244-143">A seção include deve ser semelhante ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="08244-143">The include section should look similar to the following code snippet.</span></span>  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
<span data-ttu-id="08244-144">Pronto para usar e criar na API WebView2.</span><span class="sxs-lookup"><span data-stu-id="08244-144">Ready to use and build against the WebView2 API.</span></span>  

### <a name="build-your-empty-sample-app"></a><span data-ttu-id="08244-145">Criar seu aplicativo de exemplo vazio</span><span class="sxs-lookup"><span data-stu-id="08244-145">Build your empty sample app</span></span>  

<span data-ttu-id="08244-146">Para criar e executar o aplicativo de exemplo, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="08244-146">To build and run the sample app, select `F5`.</span></span>  <span data-ttu-id="08244-147">Seu aplicativo exibe uma janela vazia.</span><span class="sxs-lookup"><span data-stu-id="08244-147">Your app displays an empty window.</span></span>  

:::image type="complex" source="../media/empty-app.png" alt-text="Aplicativo vazio" lightbox="../media/empty-app.png":::
   <span data-ttu-id="08244-149">Aplicativo vazio</span><span class="sxs-lookup"><span data-stu-id="08244-149">Empty app</span></span>  
:::image-end:::    

## <a name="step-3---create-a-single-webview-within-the-parent-window"></a><span data-ttu-id="08244-150">Etapa 3 - Criar um único WebView dentro da janela pai</span><span class="sxs-lookup"><span data-stu-id="08244-150">Step 3 - Create a single WebView within the parent window</span></span>  

<span data-ttu-id="08244-151">Adicione um WebView à janela principal.</span><span class="sxs-lookup"><span data-stu-id="08244-151">Add a WebView to the main window.</span></span>  

<span data-ttu-id="08244-152">Use o método para configurar o ambiente e localizar o navegador `CreateCoreWebView2Environment` Microsoft Edge \(Chromium\) que está visando o controle.</span><span class="sxs-lookup"><span data-stu-id="08244-152">Use the `CreateCoreWebView2Environment` method to set up the environment and locate the Microsoft Edge \(Chromium\) browser powering the control.</span></span>  <span data-ttu-id="08244-153">Você também pode usar o método se quiser especificar o local do navegador, a pasta do usuário, os sinalizadores do navegador e assim por diante, em vez de `CreateCoreWebView2EnvironmentWithOptions` usar a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="08244-153">You may also use the `CreateCoreWebView2EnvironmentWithOptions` method if you want to specify browser location, user folder, browser flags, and so on, instead of using the default setting.</span></span>  <span data-ttu-id="08244-154">Após a conclusão do método, execute o método dentro do retorno de chamada e execute o método `CreateCoreWebView2Environment` `ICoreWebView2Environment::CreateCoreWebView2Controller` para obter o `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` `ICoreWebView2Controller::get_CoreWebView2` WebView associado.</span><span class="sxs-lookup"><span data-stu-id="08244-154">Upon the completion of the `CreateCoreWebView2Environment` method, run the `ICoreWebView2Environment::CreateCoreWebView2Controller` method inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and run the `ICoreWebView2Controller::get_CoreWebView2` method to get the associated WebView.</span></span>  

<span data-ttu-id="08244-155">No retorno de chamada, de definir mais algumas configurações, resize o WebView para obter 100% da janela pai e navegue até Bing.</span><span class="sxs-lookup"><span data-stu-id="08244-155">In the callback, set a few more settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>  

<span data-ttu-id="08244-156">Copie o seguinte trecho de código e colar depois `HelloWebView.cpp` do comentário e antes do `// <-- WebView2 sample code starts here -->` `// <-- WebView2 sample code ends here -->` comentário.</span><span class="sxs-lookup"><span data-stu-id="08244-156">Copy the following code snippet and paste into `HelloWebView.cpp` after the `// <-- WebView2 sample code starts here -->` comment and before the `// <-- WebView2 sample code ends here -->` comment.</span></span>  

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

### <a name="build-your-bing-sample-app"></a><span data-ttu-id="08244-157">Criar seu Bing de exemplo</span><span class="sxs-lookup"><span data-stu-id="08244-157">Build your Bing sample app</span></span>  

<span data-ttu-id="08244-158">Para criar e executar o aplicativo, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="08244-158">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="08244-159">Agora você tem uma janela WebView exibindo a Bing página.</span><span class="sxs-lookup"><span data-stu-id="08244-159">Now you have a WebView window displaying the Bing page.</span></span>  

:::image type="complex" source="../media/bing-window.png" alt-text="Bing janela" lightbox="../media/bing-window.png":::
   <span data-ttu-id="08244-161">Bing janela</span><span class="sxs-lookup"><span data-stu-id="08244-161">Bing window</span></span>  
:::image-end:::    

## <a name="step-4---navigation-events"></a><span data-ttu-id="08244-162">Etapa 4 - Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="08244-162">Step 4 - Navigation events</span></span>  

<span data-ttu-id="08244-163">A equipe do WebView já cobriu a navegação para a URL usando o `ICoreWebView2::Navigate` método na última etapa.</span><span class="sxs-lookup"><span data-stu-id="08244-163">The WebView team already covered navigating to URL using the `ICoreWebView2::Navigate` method in the last step.</span></span>  <span data-ttu-id="08244-164">Durante a navegação, o WebView dispara uma sequência de eventos aos quais o host pode ouvir.</span><span class="sxs-lookup"><span data-stu-id="08244-164">During navigation, WebView fires a sequence of events to which the host may listen.</span></span>  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   
    
<span data-ttu-id="08244-165">Para obter mais informações, navegue até [Eventos de navegação][Webview2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="08244-165">For more information, navigate to [Navigation events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegação" lightbox="../media/navigation-events.png":::
   <span data-ttu-id="08244-167">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="08244-167">Navigation events</span></span>  
:::image-end:::    

<span data-ttu-id="08244-168">Em casos de erro, um ou mais dos seguintes eventos podem ocorrer, dependendo se a navegação é continuada para uma página da Web de erro.</span><span class="sxs-lookup"><span data-stu-id="08244-168">In error cases, one or more of the following events may occur depending on whether the navigation is continued to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`
    
> [!NOTE]
> <span data-ttu-id="08244-169">Se ocorrer um redirecionamento HTTP, haverá vários `NavigationStarting` eventos em uma linha.</span><span class="sxs-lookup"><span data-stu-id="08244-169">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="08244-170">Como exemplo de uso dos eventos, registre um manipulador para o `NavigationStarting` evento para cancelar qualquer solicitação que não seja https.</span><span class="sxs-lookup"><span data-stu-id="08244-170">As an example of using the events, register a handler for the `NavigationStarting` event to cancel any non-https requests.</span></span>  <span data-ttu-id="08244-171">Copie o seguinte trecho de código e colar em `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="08244-171">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="08244-172">Agora, o aplicativo não navega para sites que não são https.</span><span class="sxs-lookup"><span data-stu-id="08244-172">Now the app does not navigate to any non-https sites.</span></span>  <span data-ttu-id="08244-173">Você pode usar mecanismo semelhante para realizar outras tarefas, como restringir a navegação em seu próprio domínio.</span><span class="sxs-lookup"><span data-stu-id="08244-173">You may use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>  

## <a name="step-5---scripting"></a><span data-ttu-id="08244-174">Etapa 5 - Scripting</span><span class="sxs-lookup"><span data-stu-id="08244-174">Step 5 - Scripting</span></span>  

<span data-ttu-id="08244-175">Você pode usar aplicativos host para injetar código JavaScript em controles WebView2 no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="08244-175">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="08244-176">Você pode tarefa webView para executar JavaScript arbitrário ou adicionar scripts de inicialização.</span><span class="sxs-lookup"><span data-stu-id="08244-176">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="08244-177">O JavaScript injetado se aplica a todos os novos documentos de nível superior e a todos os quadros filho até que o JavaScript seja removido.</span><span class="sxs-lookup"><span data-stu-id="08244-177">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="08244-178">O JavaScript injetado é executado com tempo específico.</span><span class="sxs-lookup"><span data-stu-id="08244-178">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="08244-179">Execute-o após a criação do objeto global.</span><span class="sxs-lookup"><span data-stu-id="08244-179">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="08244-180">Execute-o antes que qualquer outro script incluído no documento HTML seja executado.</span><span class="sxs-lookup"><span data-stu-id="08244-180">Run it before any other script included in the HTML document is run.</span></span>  
    
<span data-ttu-id="08244-181">Copie o seguinte trecho de código e colar em `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="08244-181">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="08244-182">Agora, o WebView sempre congelará o `Object` objeto e retornará o documento de página uma vez.</span><span class="sxs-lookup"><span data-stu-id="08244-182">Now, WebView should always freeze the `Object` object and returns the page document once.</span></span>  

> [!NOTE] 
> <span data-ttu-id="08244-183">As APIs de injeção de script \(e algumas outras APIs webView2\) são assíncronas, você deve usar retornos de chamada se o código for necessário ser executado em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="08244-183">The script injection APIs \(and some other WebView2 APIs\) are asynchronous, you should use callbacks if code is must be run in a specific order.</span></span>  

## <a name="step-6---communication-between-host-and-web-content"></a><span data-ttu-id="08244-184">Etapa 6 - Comunicação entre conteúdo do host e da Web</span><span class="sxs-lookup"><span data-stu-id="08244-184">Step 6 - Communication between host and web content</span></span>  

<span data-ttu-id="08244-185">O host e o conteúdo da Web também podem se comunicar uns com os outros por meio do `postMessage` método.</span><span class="sxs-lookup"><span data-stu-id="08244-185">The host and the web content may also communicate with each other through the `postMessage` method.</span></span>  <span data-ttu-id="08244-186">O conteúdo da Web em execução em um WebView pode postar no host por meio do método e a mensagem é manipulada por qualquer manipulador de eventos `window.chrome.webview.postMessage` `ICoreWebView2WebMessageReceivedEventHandler` registrado no host.</span><span class="sxs-lookup"><span data-stu-id="08244-186">The web content running within a WebView may post to the host through the `window.chrome.webview.postMessage` method, and the message is handled by any registered the `ICoreWebView2WebMessageReceivedEventHandler` event handler on the host.</span></span>  <span data-ttu-id="08244-187">Da mesma forma, o host pode enviar mensagens ao conteúdo da Web por meio ou método, que é `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` capturado por manipuladores adicionados do `window.chrome.webview.addEventListener` ouvinte.</span><span class="sxs-lookup"><span data-stu-id="08244-187">Likewise, the host may message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON` method, which is caught by handlers added from `window.chrome.webview.addEventListener` listener.</span></span>  <span data-ttu-id="08244-188">O mecanismo de comunicação permite que o conteúdo da Web use recursos nativos passando mensagens para solicitar que o host execute APIs nativas.</span><span class="sxs-lookup"><span data-stu-id="08244-188">The communication mechanism allows the web content to use native capabilities by passing messages to ask the host to run native APIs.</span></span>  

<span data-ttu-id="08244-189">Como exemplo para entender o mecanismo, as etapas a seguir ocorrem quando você tenta saída da URL do documento no WebView.</span><span class="sxs-lookup"><span data-stu-id="08244-189">As an example to understand the mechanism, the following steps occur when you try to output the document URL in WebView.</span></span>  

1.  <span data-ttu-id="08244-190">O host registra um manipulador para retornar a mensagem recebida de volta ao conteúdo da Web</span><span class="sxs-lookup"><span data-stu-id="08244-190">The host registers a handler to return received message back to the web content</span></span>  
1.  <span data-ttu-id="08244-191">O host injeta um script no conteúdo da Web que registra um manipulador para imprimir mensagem do host</span><span class="sxs-lookup"><span data-stu-id="08244-191">The host injects a script to the web content that registers a handler to print message from the host</span></span>  
1.  <span data-ttu-id="08244-192">O host injeta um script no conteúdo da Web que posta a URL para o host</span><span class="sxs-lookup"><span data-stu-id="08244-192">The host injects a script to the web content that posts the URL to the host</span></span>  
1.  <span data-ttu-id="08244-193">O manipulador do host é acionado e retorna a mensagem \(a URL\) para o conteúdo da Web</span><span class="sxs-lookup"><span data-stu-id="08244-193">The handler of the host is triggered and returns the message \(the URL\) to the web content</span></span>  
1.  <span data-ttu-id="08244-194">O manipulador do conteúdo da Web é acionado e imprime a mensagem do host \(a URL\)</span><span class="sxs-lookup"><span data-stu-id="08244-194">The handler of the web content is triggered and prints message from the host \(the URL\)</span></span>  
    
<span data-ttu-id="08244-195">Copie o seguinte trecho de código e colar em `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="08244-195">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

### <a name="build-your-display-url-sample-app"></a><span data-ttu-id="08244-196">Criar seu aplicativo de exemplo de URL de exibição</span><span class="sxs-lookup"><span data-stu-id="08244-196">Build your display URL sample app</span></span>  

<span data-ttu-id="08244-197">Para criar e executar o aplicativo, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="08244-197">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="08244-198">A URL aparece em uma janela pop-up antes de navegar para uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="08244-198">The URL appears in a pop-up window before navigating to a webpage.</span></span>  

:::image type="complex" source="../media/show-url.png" alt-text="Url de exibição" lightbox="../media/show-url.png":::
   <span data-ttu-id="08244-200">Url de exibição</span><span class="sxs-lookup"><span data-stu-id="08244-200">Display url</span></span>  
:::image-end:::    

<span data-ttu-id="08244-201">Parabéns, você criou seu primeiro aplicativo WebView2.</span><span class="sxs-lookup"><span data-stu-id="08244-201">Congratulations, you built your first WebView2 app.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="08244-202">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="08244-202">Next steps</span></span>  

<span data-ttu-id="08244-203">Para obter funcionalidades adicionais do WebView2 que não são abordadas neste artigo, revise os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="08244-203">For additional WebView2 functionality that isn't covered in this article, review the following resources.</span></span>  

*   <span data-ttu-id="08244-204">Para saber mais sobre como criar aplicativos WebView2, navegue até Práticas recomendadas de desenvolvimento [webView2.][WV2BestPractices]</span><span class="sxs-lookup"><span data-stu-id="08244-204">To learn more about building WebView2 applications, navigate to [WebView2 development best practices][WV2BestPractices].</span></span>  
*   <span data-ttu-id="08244-205">Para um exemplo abrangente de recursos WebView2, navegue até [WebView2 API Sample][GithubMicrosoftedgeWebview2samplesApisample].</span><span class="sxs-lookup"><span data-stu-id="08244-205">For a comprehensive example of WebView2 capabilities, navigate to [WebView2 API Sample][GithubMicrosoftedgeWebview2samplesApisample].</span></span>  
*   <span data-ttu-id="08244-206">Para um aplicativo de exemplo criado usando WebView2, navegue até [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span><span class="sxs-lookup"><span data-stu-id="08244-206">For a sample app built using WebView2, navigate to [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span></span>  
*   <span data-ttu-id="08244-207">Para obter informações detalhadas sobre a API WebView2, navegue até [referência de API][Webview2ReferenceWin32].</span><span class="sxs-lookup"><span data-stu-id="08244-207">For detailed information about the WebView2 API, navigate to [API reference][Webview2ReferenceWin32].</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="08244-208">Entrar em contato com a equipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="08244-208">Getting in touch with the Microsoft Edge WebView team</span></span>  

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
