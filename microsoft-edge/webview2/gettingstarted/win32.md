---
description: Guia de iniciação com WebView2 para aplicativos Win32
title: Getting started with WebView2 for Win32 apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Controller, controle de navegador, html de borda
ms.openlocfilehash: 19bc0c5600ebd072ad9a6aa61d2a965e999865ce
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306156"
---
# <span data-ttu-id="affd1-104">Getting started with WebView2</span><span class="sxs-lookup"><span data-stu-id="affd1-104">Getting started with WebView2</span></span>  

<span data-ttu-id="affd1-105">Neste artigo, aprenda a criar seu primeiro aplicativo WebView2 e saiba mais sobre os principais recursos do [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="affd1-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="affd1-106">Para obter mais informações sobre APIs WebView2 individuais, navegue até a [referência de API.][Webview2ReferenceWin32]</span><span class="sxs-lookup"><span data-stu-id="affd1-106">For more information about individual WebView2 APIs, navigate to [API reference][Webview2ReferenceWin32].</span></span>  

## <span data-ttu-id="affd1-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="affd1-107">Prerequisites</span></span>  

<span data-ttu-id="affd1-108">Certifique-se de instalar a seguinte lista de pré-requisitos antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="affd1-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="affd1-109">[WebView2 Runtime][Webview2Installer] ou qualquer canal não estável do [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado no sistema operacional suportado \(atualmente Windows 10, Windows 8.1 e Windows 7\).</span><span class="sxs-lookup"><span data-stu-id="affd1-109">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="affd1-110">A equipe WebView recomenda usar o canal Canary e a versão mínima necessária é 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="affd1-110">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="affd1-111">[Visual Studio][MicrosoftVisualstudioMain] 2015 ou posterior com suporte a C++ instalado.</span><span class="sxs-lookup"><span data-stu-id="affd1-111">[Visual Studio][MicrosoftVisualstudioMain] 2015 or later with C++ support installed.</span></span>  
    
## <span data-ttu-id="affd1-112">Etapa 1: criar um aplicativo de janela única</span><span class="sxs-lookup"><span data-stu-id="affd1-112">Step 1 - Create a single-window app</span></span>  

<span data-ttu-id="affd1-113">Comece com um projeto de área de trabalho básico que contenha uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="affd1-113">Start with a basic desktop project that contains a single main window.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="affd1-114">Para focalizar melhor o passo a passo, use o código de exemplo modificado do Passo a passo: crie um aplicativo tradicional da Área de Trabalho do [Windows (C++)][CppWindowsWalkthroughCreatingDesktopApplication] para seu aplicativo de exemplo.</span><span class="sxs-lookup"><span data-stu-id="affd1-114">To better focus the walkthrough, use modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.</span></span>  <span data-ttu-id="affd1-115">Para baixar o exemplo modificado e começar, navegue até [WebView2 Amostras][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span><span class="sxs-lookup"><span data-stu-id="affd1-115">To download the modified sample and get started, navigate to [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span></span>  

1.  <span data-ttu-id="affd1-116">No Visual Studio, `WebView2GettingStarted.sln` abra.</span><span class="sxs-lookup"><span data-stu-id="affd1-116">In Visual Studio, open `WebView2GettingStarted.sln`.</span></span>  
    <span data-ttu-id="affd1-117">Se você usar uma versão mais antiga do Visual Studio, passe o mouse sobre o projeto **WebView2GettingStarted,** abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="affd1-117">If you use an older version of Visual Studio, hover on the **WebView2GettingStarted** project, open the contextual menu \(right-click\), and choose **Properties**.</span></span>  <span data-ttu-id="affd1-118">Em **Propriedades de**Configuração Geral, modifique a Versão do SDK do Windows e o platform Toolset para usar o SDK do Win10 e o toolset do Visual Studio disponíveis  >  \*\*\*\* para você. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="affd1-118">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and Visual Studio toolset available to you.</span></span>  

:::image type="complex" source="../media/tool-version.png" alt-text="Versão da ferramenta" lightbox="../media/tool-version.png":::
   <span data-ttu-id="affd1-120">Versão da ferramenta</span><span class="sxs-lookup"><span data-stu-id="affd1-120">Tool version</span></span>  
:::image-end:::  

<span data-ttu-id="affd1-121">O Visual Studio pode exibir erros, pois o seu projeto não tem o arquivo de header WebView2.</span><span class="sxs-lookup"><span data-stu-id="affd1-121">Visual Studio may display errors, because your project is missing the WebView2 header file.</span></span>  <span data-ttu-id="affd1-122">Os erros devem ser corrigidos após a [Etapa 2.](#step-2---install-webview2-sdk)</span><span class="sxs-lookup"><span data-stu-id="affd1-122">The errors should be fixed after [Step 2](#step-2---install-webview2-sdk).</span></span>  

## <span data-ttu-id="affd1-123">Etapa 2 - Instalar o SDK webView2</span><span class="sxs-lookup"><span data-stu-id="affd1-123">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="affd1-124">Adicione o SDK webView2 ao projeto.</span><span class="sxs-lookup"><span data-stu-id="affd1-124">Add the WebView2 SDK into the project.</span></span>  <span data-ttu-id="affd1-125">Use o NuGet para instalar o SDK do Win32.</span><span class="sxs-lookup"><span data-stu-id="affd1-125">Use NuGet to install the Win32 SDK.</span></span>  

1.  <span data-ttu-id="affd1-126">Passe o mouse sobre o projeto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Gerenciar Pacotes NuGet.**</span><span class="sxs-lookup"><span data-stu-id="affd1-126">Hover on the project, open the contextual menu \(right-click\), and choose **Manage NuGet Packages**.</span></span>  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Gerenciar pacotes NuGet" lightbox="../media/manage-nuget-packages.png":::
       <span data-ttu-id="affd1-128">Gerenciar pacotes NuGet</span><span class="sxs-lookup"><span data-stu-id="affd1-128">Manage NuGet packages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="affd1-129">Instale a Biblioteca de Implementação do Windows.</span><span class="sxs-lookup"><span data-stu-id="affd1-129">Install the Windows Implementation Library.</span></span>  
    1.  <span data-ttu-id="affd1-130">Na barra de pesquisa, digite > `Microsoft.Windows.ImplementationLibrary` escolha **Microsoft.Windows.ImplementationLibrary**.</span><span class="sxs-lookup"><span data-stu-id="affd1-130">In the search bar, type `Microsoft.Windows.ImplementationLibrary` > choose **Microsoft.Windows.ImplementationLibrary**.</span></span>  
    1.  <span data-ttu-id="affd1-131">Na janela do lado direito, escolha **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="affd1-131">In the right-hand side window, choose **Install**.</span></span>  <span data-ttu-id="affd1-132">O NuGet baixa a biblioteca para o computador.</span><span class="sxs-lookup"><span data-stu-id="affd1-132">NuGet downloads the library to your machine.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="affd1-133">A [Biblioteca de Implementação do Windows][GithubMicrosoftWilMain] e a Biblioteca de Modelos [C++][CppCxWrlTemplateLibraryVS2019] do Windows Runtime são opcionais e facilitam o trabalho com COM para o exemplo.</span><span class="sxs-lookup"><span data-stu-id="affd1-133">The [Windows Implementation Library][GithubMicrosoftWilMain] and [Windows Runtime C++ Template Library][CppCxWrlTemplateLibraryVS2019] are optional and make working with COM easier for the example.</span></span>  
        
        :::image type="complex" source="../media/wil.png" alt-text="Biblioteca de Implementação do Windows" lightbox="../media/wil.png":::
           <span data-ttu-id="affd1-135">Biblioteca de Implementação do Windows</span><span class="sxs-lookup"><span data-stu-id="affd1-135">Windows Implementation Library</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="affd1-136">Instale o SDK webView2.</span><span class="sxs-lookup"><span data-stu-id="affd1-136">Install the WebView2 SDK.</span></span>  
    1.  <span data-ttu-id="affd1-137">Na barra de pesquisa, digite > `Microsoft.Web.WebView2` escolha **Microsoft.Web.WebView2**.</span><span class="sxs-lookup"><span data-stu-id="affd1-137">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
    1.  <span data-ttu-id="affd1-138">Na janela do lado direito, escolha **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="affd1-138">In the right-hand side window, choose **Install**.</span></span>  <span data-ttu-id="affd1-139">O NuGet baixa o SDK em seu computador.</span><span class="sxs-lookup"><span data-stu-id="affd1-139">NuGet downloads the SDK to your machine.</span></span>  
        
        :::image type="complex" source="../media/nuget.png" alt-text="Gerenciador de Pacotes NuGet" lightbox="../media/nuget.png":::
           <span data-ttu-id="affd1-141">Gerenciador de Pacotes NuGet</span><span class="sxs-lookup"><span data-stu-id="affd1-141">NuGet Package Manager</span></span>
        :::image-end:::  
        
1.  <span data-ttu-id="affd1-142">Adicione o header WebView2 ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="affd1-142">Add WebView2 header to your project.</span></span>  
    :::row:::
       :::column span="1":::
          <span data-ttu-id="affd1-143">No `HelloWebView.cpp` arquivo, copie o trecho de código a seguir e o copie após a última `#include` linha.</span><span class="sxs-lookup"><span data-stu-id="affd1-143">In the `HelloWebView.cpp` file, copy the following code snippet and paste it after the last `#include` line.</span></span>  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          <span data-ttu-id="affd1-144">A seção include deve ser semelhante ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="affd1-144">The include section should look similar to the following code snippet.</span></span>  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
<span data-ttu-id="affd1-145">Pronto para usar e criar com base na API WebView2.</span><span class="sxs-lookup"><span data-stu-id="affd1-145">Ready to use and build against the WebView2 API.</span></span>  

### <span data-ttu-id="affd1-146">Criar seu aplicativo de exemplo vazio</span><span class="sxs-lookup"><span data-stu-id="affd1-146">Build your empty sample app</span></span>  

<span data-ttu-id="affd1-147">Para criar e executar o aplicativo de exemplo, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="affd1-147">To build and run the sample app, select `F5`.</span></span>  <span data-ttu-id="affd1-148">Seu aplicativo exibe uma janela vazia.</span><span class="sxs-lookup"><span data-stu-id="affd1-148">Your app displays an empty window.</span></span>  

:::image type="complex" source="../media/empty-app.png" alt-text="Aplicativo vazio" lightbox="../media/empty-app.png":::
   <span data-ttu-id="affd1-150">Aplicativo vazio</span><span class="sxs-lookup"><span data-stu-id="affd1-150">Empty app</span></span>  
:::image-end:::  

## <span data-ttu-id="affd1-151">Etapa 3 : Criar um único WebView dentro da janela pai</span><span class="sxs-lookup"><span data-stu-id="affd1-151">Step 3 - Create a single WebView within the parent window</span></span>  

<span data-ttu-id="affd1-152">Adicione um WebView à janela principal.</span><span class="sxs-lookup"><span data-stu-id="affd1-152">Add a WebView to the main window.</span></span>  

 <span data-ttu-id="affd1-153">Use o método para configurar o ambiente e localizar o navegador `CreateCoreWebView2Environment` Microsoft Edge \(Chromium\) a partir do controle.</span><span class="sxs-lookup"><span data-stu-id="affd1-153">Use the `CreateCoreWebView2Environment` method to set up the environment and locate the Microsoft Edge \(Chromium\) browser powering the control.</span></span>  <span data-ttu-id="affd1-154">Você também pode usar o método se quiser especificar o local do navegador, a pasta do usuário, os sinalizadores do navegador e assim por diante, em vez de usar `CreateCoreWebView2EnvironmentWithOptions` a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="affd1-154">You may also use the `CreateCoreWebView2EnvironmentWithOptions` method if you want to specify browser location, user folder, browser flags, and so on, instead of using the default setting.</span></span>  <span data-ttu-id="affd1-155">Após a conclusão do método, execute o método dentro do retorno de chamada e execute o método `CreateCoreWebView2Environment` `ICoreWebView2Environment::CreateCoreWebView2Controller` para obter o `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` `ICoreWebView2Controller::get_CoreWebView2` WebView associado.</span><span class="sxs-lookup"><span data-stu-id="affd1-155">Upon the completion of the `CreateCoreWebView2Environment` method, run the `ICoreWebView2Environment::CreateCoreWebView2Controller` method inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and run the `ICoreWebView2Controller::get_CoreWebView2` method to get the associated WebView.</span></span>  

<span data-ttu-id="affd1-156">No retorno de chamada, de definir mais algumas configurações, reize o WebView para que ele pegue 100% da janela pai e navegue até o Bing.</span><span class="sxs-lookup"><span data-stu-id="affd1-156">In the callback, set a few more settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>  

<span data-ttu-id="affd1-157">Copie o trecho de código a seguir e copie-o `HelloWebView.cpp` depois do comentário e antes do `// <-- WebView2 sample code starts here -->` `// <-- WebView2 sample code ends here -->` comentário.</span><span class="sxs-lookup"><span data-stu-id="affd1-157">Copy the following code snippet and paste into `HelloWebView.cpp` after the `// <-- WebView2 sample code starts here -->` comment and before the `// <-- WebView2 sample code ends here -->` comment.</span></span>  

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

### <span data-ttu-id="affd1-158">Criar seu aplicativo de exemplo do Bing</span><span class="sxs-lookup"><span data-stu-id="affd1-158">Build your Bing sample app</span></span>  

<span data-ttu-id="affd1-159">Para criar e executar o aplicativo, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="affd1-159">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="affd1-160">Agora você tem uma janela WebView exibindo a página do Bing.</span><span class="sxs-lookup"><span data-stu-id="affd1-160">Now you have a WebView window displaying the Bing page.</span></span>  

:::image type="complex" source="../media/bing-window.png" alt-text="Janela do Bing" lightbox="../media/bing-window.png":::
   <span data-ttu-id="affd1-162">Janela do Bing</span><span class="sxs-lookup"><span data-stu-id="affd1-162">Bing window</span></span>  
:::image-end:::  

## <span data-ttu-id="affd1-163">Etapa 4 - Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="affd1-163">Step 4 - Navigation events</span></span>  

<span data-ttu-id="affd1-164">A equipe WebView já abrangeu a navegação para a URL usando `ICoreWebView2::Navigate` o método na última etapa.</span><span class="sxs-lookup"><span data-stu-id="affd1-164">The WebView team already covered navigating to URL using the `ICoreWebView2::Navigate` method in the last step.</span></span>  <span data-ttu-id="affd1-165">Durante a navegação, o WebView dispara uma sequência de eventos aos quais o host pode escutar.</span><span class="sxs-lookup"><span data-stu-id="affd1-165">During navigation, WebView fires a sequence of events to which the host may listen.</span></span>  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

<span data-ttu-id="affd1-166">Para obter mais informações, navegue até [eventos de navegação.][Webview2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="affd1-166">For more information, navigate to [Navigation events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegação" lightbox="../media/navigation-events.png":::
   <span data-ttu-id="affd1-168">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="affd1-168">Navigation events</span></span>  
:::image-end:::  

<span data-ttu-id="affd1-169">Em casos de erro, um ou mais dos eventos a seguir podem ocorrer dependendo se a navegação continua para uma página da Web de erro.</span><span class="sxs-lookup"><span data-stu-id="affd1-169">In error cases, one or more of the following events may occur depending on whether the navigation is continued to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

> [!NOTE]
> <span data-ttu-id="affd1-170">Se ocorrer um redirecionamento HTTP, haverá vários `NavigationStarting` eventos em uma linha.</span><span class="sxs-lookup"><span data-stu-id="affd1-170">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="affd1-171">Como exemplo de uso dos eventos, registre um manipulador para o `NavigationStarting` evento para cancelar qualquer solicitação não https.</span><span class="sxs-lookup"><span data-stu-id="affd1-171">As an example of using the events, register a handler for the `NavigationStarting` event to cancel any non-https requests.</span></span>  <span data-ttu-id="affd1-172">Copie o trecho de código a seguir e `HelloWebView.cpp` copie-o.</span><span class="sxs-lookup"><span data-stu-id="affd1-172">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="affd1-173">Agora, o aplicativo não navega para nenhum site não https.</span><span class="sxs-lookup"><span data-stu-id="affd1-173">Now the app does not navigate to any non-https sites.</span></span>  <span data-ttu-id="affd1-174">Você pode usar um mecanismo semelhante para realizar outras tarefas, como restringir a navegação dentro de seu próprio domínio.</span><span class="sxs-lookup"><span data-stu-id="affd1-174">You may use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>  

## <span data-ttu-id="affd1-175">Etapa 5 - Scripts</span><span class="sxs-lookup"><span data-stu-id="affd1-175">Step 5 - Scripting</span></span>  

<span data-ttu-id="affd1-176">Você pode usar aplicativos host para inserir código JavaScript em controles WebView2 no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="affd1-176">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="affd1-177">Você pode tarefa WebView para executar JavaScript arbitrário ou adicionar scripts de inicialização.</span><span class="sxs-lookup"><span data-stu-id="affd1-177">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="affd1-178">O JavaScript injetado se aplica a todos os novos documentos de nível superior e a todos os quadros filho até que o JavaScript seja removido.</span><span class="sxs-lookup"><span data-stu-id="affd1-178">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="affd1-179">O JavaScript injetado é executado com tempo específico.</span><span class="sxs-lookup"><span data-stu-id="affd1-179">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="affd1-180">Execute-o após a criação do objeto global.</span><span class="sxs-lookup"><span data-stu-id="affd1-180">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="affd1-181">Execute-o antes que qualquer outro script incluído no documento HTML seja executado.</span><span class="sxs-lookup"><span data-stu-id="affd1-181">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="affd1-182">Copie o trecho de código a seguir e `HelloWebView.cpp` copie-o.</span><span class="sxs-lookup"><span data-stu-id="affd1-182">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="affd1-183">Agora, o WebView sempre deve congelar o `Object` objeto e retornar o documento da página uma vez.</span><span class="sxs-lookup"><span data-stu-id="affd1-183">Now, WebView should always freeze the `Object` object and returns the page document once.</span></span>  

> [!NOTE] 
> <span data-ttu-id="affd1-184">As APIs de injeção de script \(e algumas outras APIs WebView2\) são assíncronas, você deve usar retornos de chamada se o código deve ser executado em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="affd1-184">The script injection APIs \(and some other WebView2 APIs\) are asynchronous, you should use callbacks if code is must be run in a specific order.</span></span>  

## <span data-ttu-id="affd1-185">Etapa 6- Comunicação entre o conteúdo do host e da Web</span><span class="sxs-lookup"><span data-stu-id="affd1-185">Step 6 - Communication between host and web content</span></span>  

<span data-ttu-id="affd1-186">O host e o conteúdo da Web também podem se comunicar uns com os outros por meio do `postMessage` método.</span><span class="sxs-lookup"><span data-stu-id="affd1-186">The host and the web content may also communicate with each other through the `postMessage` method.</span></span>  <span data-ttu-id="affd1-187">O conteúdo da Web em execução em um WebView pode postar no host por meio do método, e a mensagem é manipulada por qualquer manipulador de eventos `window.chrome.webview.postMessage` `ICoreWebView2WebMessageReceivedEventHandler` registrado no host.</span><span class="sxs-lookup"><span data-stu-id="affd1-187">The web content running within a WebView may post to the host through the `window.chrome.webview.postMessage` method, and the message is handled by any registered the `ICoreWebView2WebMessageReceivedEventHandler` event handler on the host.</span></span>  <span data-ttu-id="affd1-188">Da mesma forma, o host pode enviar mensagens ao conteúdo da Web por meio ou método, que é capturado por `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` manipuladores adicionados do `window.chrome.webview.addEventListener` ouvinte.</span><span class="sxs-lookup"><span data-stu-id="affd1-188">Likewise, the host may message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON` method, which is caught by handlers added from `window.chrome.webview.addEventListener` listener.</span></span>  <span data-ttu-id="affd1-189">O mecanismo de comunicação permite que o conteúdo da Web use recursos nativos passando mensagens para solicitar que o host execute APIs nativas.</span><span class="sxs-lookup"><span data-stu-id="affd1-189">The communication mechanism allows the web content to use native capabilities by passing messages to ask the host to run native APIs.</span></span>  

<span data-ttu-id="affd1-190">Como exemplo para entender o mecanismo, as etapas a seguir ocorrem quando você tenta a saída da URL do documento no WebView.</span><span class="sxs-lookup"><span data-stu-id="affd1-190">As an example to understand the mechanism, the following steps occur when you try to output the document URL in WebView.</span></span>  

1.  <span data-ttu-id="affd1-191">O host registra um manipulador para retornar a mensagem recebida de volta para o conteúdo da Web</span><span class="sxs-lookup"><span data-stu-id="affd1-191">The host registers a handler to return received message back to the web content</span></span>  
1.  <span data-ttu-id="affd1-192">O host injeta um script no conteúdo da Web que registra um manipulador para imprimir a mensagem do host</span><span class="sxs-lookup"><span data-stu-id="affd1-192">The host injects a script to the web content that registers a handler to print message from the host</span></span>  
1.  <span data-ttu-id="affd1-193">O host injeta um script no conteúdo da Web que posta a URL para o host</span><span class="sxs-lookup"><span data-stu-id="affd1-193">The host injects a script to the web content that posts the URL to the host</span></span>  
1.  <span data-ttu-id="affd1-194">O manipulador do host é disparado e retorna a mensagem \(a URL\) para o conteúdo da Web</span><span class="sxs-lookup"><span data-stu-id="affd1-194">The handler of the host is triggered and returns the message \(the URL\) to the web content</span></span>  
1.  <span data-ttu-id="affd1-195">O manipulador do conteúdo da Web é disparado e imprime a mensagem do host \(a URL\)</span><span class="sxs-lookup"><span data-stu-id="affd1-195">The handler of the web content is triggered and prints message from the host \(the URL\)</span></span>  

<span data-ttu-id="affd1-196">Copie o trecho de código a seguir e `HelloWebView.cpp` copie-o.</span><span class="sxs-lookup"><span data-stu-id="affd1-196">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

### <span data-ttu-id="affd1-197">Criar seu aplicativo de exemplo de URL de exibição</span><span class="sxs-lookup"><span data-stu-id="affd1-197">Build your display URL sample app</span></span>  

<span data-ttu-id="affd1-198">Para criar e executar o aplicativo, selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="affd1-198">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="affd1-199">A URL aparece em uma janela pop-up antes de navegar para uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="affd1-199">The URL appears in a pop-up window before navigating to a webpage.</span></span>  

:::image type="complex" source="../media/show-url.png" alt-text="Url de exibição" lightbox="../media/show-url.png":::
   <span data-ttu-id="affd1-201">Url de exibição</span><span class="sxs-lookup"><span data-stu-id="affd1-201">Display url</span></span>  
:::image-end:::  

<span data-ttu-id="affd1-202">Parabéns, você criou seu primeiro aplicativo WebView2.</span><span class="sxs-lookup"><span data-stu-id="affd1-202">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="affd1-203">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="affd1-203">Next steps</span></span>  

<span data-ttu-id="affd1-204">Muitas das funcionalidades WebView2 não são abordadas neste artigo, a seção a seguir fornece mais recursos.</span><span class="sxs-lookup"><span data-stu-id="affd1-204">Many of the WebView2 functionalities are not covered on this article, the following section provides more resources.</span></span>  

### <span data-ttu-id="affd1-205">Ver também</span><span class="sxs-lookup"><span data-stu-id="affd1-205">See also</span></span>  

*   <span data-ttu-id="affd1-206">Para um exemplo abrangente de recursos WebView2, navegue até [WebView2 API Sample][GithubMicrosoftedgeWebview2samplesApisample].</span><span class="sxs-lookup"><span data-stu-id="affd1-206">For a comprehensive example of WebView2 capabilities, navigate to [WebView2 API Sample][GithubMicrosoftedgeWebview2samplesApisample].</span></span>  
*   <span data-ttu-id="affd1-207">Para um aplicativo de exemplo criado usando WebView2, navegue até [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span><span class="sxs-lookup"><span data-stu-id="affd1-207">For a sample app built using WebView2, navigate to [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span></span>  
*   <span data-ttu-id="affd1-208">Para obter informações detalhadas sobre a API WebView2, navegue até a [referência de API.][Webview2ReferenceWin32]</span><span class="sxs-lookup"><span data-stu-id="affd1-208">For detailed information about the WebView2 API, navigate to [API reference][Webview2ReferenceWin32].</span></span>  

## <span data-ttu-id="affd1-209">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="affd1-209">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2 | Desenvolvedor do Microsoft Edge"  

[Webview2ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "WebView2 Win32 C++ Reference | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegação | Microsoft Docs"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019&preserve-view=true "Biblioteca de Modelos C++ do Windows Runtime (WRL) | Microsoft Docs"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019&preserve-view=true "Passo a passo: criar um aplicativo tradicional da Área de Trabalho do Windows (C++) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser - MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback - MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "Exemplo de API WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Bibliotecas de Implementação do Windows (WIL) - microsoft/wil | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador WebView2"  
