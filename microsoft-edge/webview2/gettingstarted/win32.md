---
description: Guia de introdução ao WebView2 para aplicativos Win32
title: Introdução ao WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 20d830e2c8b95213b223da46f9afd9f69a137946
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120379"
---
# <span data-ttu-id="a1f6c-104">Introdução ao WebView2</span><span class="sxs-lookup"><span data-stu-id="a1f6c-104">Getting started with WebView2</span></span>  

<span data-ttu-id="a1f6c-105">O conteúdo a seguir orienta você pelas funcionalidades comumente usadas do [WebView2][Webview2Index] e fornece um ponto de partida para criar seu primeiro aplicativo WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-105">The following content walks you through the commonly used functionalities of [WebView2][Webview2Index] and provides a starting point for creating your first WebView2 app.</span></span>  <span data-ttu-id="a1f6c-106">Para obter mais informações sobre APIs individuais do WebView2, consulte [referência de API][Webview2ReferenceWin32].</span><span class="sxs-lookup"><span data-stu-id="a1f6c-106">For more information about individual WebView2 APIs, see [API reference][Webview2ReferenceWin32].</span></span>  

## <span data-ttu-id="a1f6c-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a1f6c-107">Prerequisites</span></span>  

*   <span data-ttu-id="a1f6c-108">[WebView2 Runtime][Webview2Installer] ou qualquer [canal não estável do Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado em um sistema operacional com suporte \ (atualmente o Windows 10, o Windows 8,1 e o Windows 7 \).</span><span class="sxs-lookup"><span data-stu-id="a1f6c-108">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a1f6c-109">A equipe WebView recomenda usar o canal Canárias e a versão mínima necessária é 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-109">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="a1f6c-110">[Visual Studio][MicrosoftVisualstudioMain] 2015 ou posterior com suporte a C++ instalado.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-110">[Visual Studio][MicrosoftVisualstudioMain] 2015 or later with C++ support installed.</span></span>  

## <span data-ttu-id="a1f6c-111">Etapa 1-criar um aplicativo Win32 de janela única</span><span class="sxs-lookup"><span data-stu-id="a1f6c-111">Step 1 - Create a single-window win32 app</span></span>  

<span data-ttu-id="a1f6c-112">Comece com um projeto básico de área de trabalho que contenha uma única janela principal.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-112">Start with a basic desktop project that contains a single main window.</span></span>  <span data-ttu-id="a1f6c-113">Para melhor focalizar o guia passo a passo, você está usando código de exemplo modificado do [passo-a-passo: criar um aplicativo de área de trabalho tradicional do Windows (C++)][CppWindowsWalkthroughCreatingDesktopApplication] para o aplicativo de exemplo.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-113">To better focus the walkthrough, you are using modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.</span></span>  <span data-ttu-id="a1f6c-114">Para baixar a amostra modificada e começar, navegue até [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span><span class="sxs-lookup"><span data-stu-id="a1f6c-114">To download the modified sample and get started, navigate to [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span></span>  

<span data-ttu-id="a1f6c-115">No Visual Studio, abra `WebView2GettingStarted.sln` .</span><span class="sxs-lookup"><span data-stu-id="a1f6c-115">In Visual Studio, open `WebView2GettingStarted.sln`.</span></span>  <span data-ttu-id="a1f6c-116">Se você estiver usando uma versão mais antiga do Visual Studio, passe o mouse sobre o projeto **WebView2GettingStarted** , abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-116">If you are using an older version of Visual Studio, hover on the **WebView2GettingStarted** project, open the contextual menu \(right-click\), and select **Properties**.</span></span>  <span data-ttu-id="a1f6c-117">Em **Propriedades de configuração**  >  **geral**, modifique o conjunto de **ferramentas** do **SDK do Windows** e a plataforma para usar o SDK do Win10 e o conjunto de ferramentas do Visual Studio \ (vs Toolset \) disponíveis para você.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-117">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and Visual Studio toolset \(VS toolset\) available to you.</span></span>  

:::image type="complex" source="../media/tool-version.png" alt-text="Versão da ferramenta" lightbox="../media/tool-version.png":::
   <span data-ttu-id="a1f6c-119">Versão da ferramenta</span><span class="sxs-lookup"><span data-stu-id="a1f6c-119">Tool version</span></span>  
:::image-end:::  

<span data-ttu-id="a1f6c-120">O Visual Studio pode mostrar alguns erros devido ao arquivo de cabeçalho WebView2 ausente, que deve ficar ausente após a conclusão da etapa 2.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-120">Visual Studio may show some errors because of the missing WebView2 header file, which should go away after Step 2 is completed.</span></span>  

## <span data-ttu-id="a1f6c-121">Etapa 2-instalar o SDK do WebView2</span><span class="sxs-lookup"><span data-stu-id="a1f6c-121">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="a1f6c-122">Adicione o SDK WebView2 ao projeto.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-122">Add the WebView2 SDK into the project.</span></span>  <span data-ttu-id="a1f6c-123">Você pode instalar o SDK do Win32 usando o NuGet.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-123">You may install the Win32 SDK using NuGet.</span></span>  

1.  <span data-ttu-id="a1f6c-124">Passe o cursor do mouse sobre o projeto, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **gerenciar pacotes NuGet**.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-124">Hover on the project, open the contextual menu \(right-click\), and select **Manage NuGet Packages**.</span></span>  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Versão da ferramenta" lightbox="../media/manage-nuget-packages.png":::
       <span data-ttu-id="a1f6c-126">Gerenciar pacotes NuGet</span><span class="sxs-lookup"><span data-stu-id="a1f6c-126">Manage NuGet packages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a1f6c-127">Instale a biblioteca de implementação do Windows.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-127">Install the Windows Implementation Library.</span></span>  
    1.  <span data-ttu-id="a1f6c-128">Digite `Microsoft.Windows.ImplementationLibrary` na barra de pesquisa, selecione **Microsoft. Windows. ImplementationLibrary** nos resultados e selecione **instalar** na janela do lado direito.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-128">Enter `Microsoft.Windows.ImplementationLibrary` in the search bar, select **Microsoft.Windows.ImplementationLibrary** from the results, and select **Install** in the right-hand side window.</span></span>  <span data-ttu-id="a1f6c-129">O NuGet baixa o SDK para seu computador.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-129">NuGet downloads the SDK to your machine.</span></span>  
        
        > [!NOTE] 
        > <span data-ttu-id="a1f6c-130">A [biblioteca de implementação do Windows][GithubMicrosoftWilMain] e a [biblioteca de modelos do Windows Runtime C++][CppCxWrlTemplateLibraryVS2019] são opcionais e foram adicionadas para facilitar o trabalho com com mais facilidade para o exemplo.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-130">The [Windows Implementation Library][GithubMicrosoftWilMain] and [Windows Runtime C++ Template Library][CppCxWrlTemplateLibraryVS2019] are optional and were added to make working with COM easier for the example.</span></span>  
        
        :::image type="complex" source="../media/wil.png" alt-text="Versão da ferramenta" lightbox="../media/wil.png":::
           <span data-ttu-id="a1f6c-132">Biblioteca de implementação do Windows</span><span class="sxs-lookup"><span data-stu-id="a1f6c-132">Windows Implementation Library</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="a1f6c-133">Instale o SDK do WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-133">Install the WebView2 SDK.</span></span>  
    1.  <span data-ttu-id="a1f6c-134">Digite `Microsoft.Web.WebView2` na barra de pesquisa, selecione **Microsoft. Web. WebView2** nos resultados e selecione **instalar** na janela do lado direito.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-134">Enter `Microsoft.Web.WebView2` in the search bar, select **Microsoft.Web.WebView2** from the results, and select **Install** in the right-hand side window.</span></span>  <span data-ttu-id="a1f6c-135">O NuGet baixa o SDK para seu computador.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-135">NuGet downloads the SDK to your machine.</span></span>  
        
        :::image type="complex" source="../media/nuget.png" alt-text="Versão da ferramenta" lightbox="../media/nuget.png":::
           <span data-ttu-id="a1f6c-137">Gerenciador de pacotes NuGet</span><span class="sxs-lookup"><span data-stu-id="a1f6c-137">Nuget Package Manager</span></span>
        :::image-end:::  
        
1.  <span data-ttu-id="a1f6c-138">Adicione o cabeçalho WebView2 ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-138">Add WebView2 header to your project.</span></span>  
    :::row:::
       :::column span="1":::
          <span data-ttu-id="a1f6c-139">Abrir `HelloWebView.cpp` , copie o trecho de código a seguir e cole em `HelloWebView.cpp` após a última `#include` linha.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-139">Open `HelloWebView.cpp`, copy the following code snippet and paste into `HelloWebView.cpp` after last `#include` line.</span></span>  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          <span data-ttu-id="a1f6c-140">A seção include deve ser semelhante ao trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-140">The include section should look similar to the following code snippet.</span></span>  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
<span data-ttu-id="a1f6c-141">Você está pronto para usar e compilar a API WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-141">You are all set to use and build against the WebView2 API.</span></span>  

### <span data-ttu-id="a1f6c-142">Criar seu aplicativo de exemplo vazio</span><span class="sxs-lookup"><span data-stu-id="a1f6c-142">Build your empty sample app</span></span>  

<span data-ttu-id="a1f6c-143">Selecione `F5` para compilar e executar o aplicativo de exemplo.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-143">Select `F5` to build and run the sample app.</span></span>  <span data-ttu-id="a1f6c-144">Será exibido um aplicativo exibindo uma janela vazia.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-144">An app displaying an empty window appears.</span></span>  

:::image type="complex" source="../media/empty-app.png" alt-text="Versão da ferramenta" lightbox="../media/empty-app.png":::
   <span data-ttu-id="a1f6c-146">Aplicativo vazio</span><span class="sxs-lookup"><span data-stu-id="a1f6c-146">Empty app</span></span>  
:::image-end:::  

## <span data-ttu-id="a1f6c-147">Etapa 3-criar uma única WebView dentro da janela pai</span><span class="sxs-lookup"><span data-stu-id="a1f6c-147">Step 3 - Create a single WebView within the parent window</span></span>  

<span data-ttu-id="a1f6c-148">Adicione um WebView à janela principal.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-148">Add a WebView to the main window.</span></span>  <span data-ttu-id="a1f6c-149">Use o `CreateCoreWebView2Environment` método para configurar o ambiente e localizar o navegador Microsoft Edge \ (Chromium \) que o controla.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-149">Use the `CreateCoreWebView2Environment` method to set up the environment and locate the Microsoft Edge \(Chromium\) browser powering the control.</span></span>  <span data-ttu-id="a1f6c-150">Você também pode usar o `CreateCoreWebView2EnvironmentWithOptions` método se quiser especificar o local do navegador, a pasta do usuário, os sinalizadores do navegador e assim por diante, em vez de usar a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-150">You may also use the `CreateCoreWebView2EnvironmentWithOptions` method if you want to specify browser location, user folder, browser flags, and so on, instead of using the default setting.</span></span>  <span data-ttu-id="a1f6c-151">Após a conclusão do `CreateCoreWebView2Environment` método, você poderá executar o `ICoreWebView2Environment::CreateCoreWebView2Controller` método dentro do `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` retorno de chamada e executar o `ICoreWebView2Controller::get_CoreWebView2` método para obter o WebView associado.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-151">Upon the completion of the `CreateCoreWebView2Environment` method, you are able to run the `ICoreWebView2Environment::CreateCoreWebView2Controller` method inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and run the `ICoreWebView2Controller::get_CoreWebView2` method to get the associated WebView.</span></span>  

<span data-ttu-id="a1f6c-152">No retorno de chamada, defina algumas configurações adicionais, redimensione a WebView para fazer 100% da janela pai e navegue até Bing.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-152">In the callback, set a few additional settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>  

<span data-ttu-id="a1f6c-153">Copie o trecho de código a seguir e cole em `HelloWebView.cpp` após a `// <-- WebView2 sample code starts here -->` anotação e antes da `// <-- WebView2 sample code ends here -->` anotação.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-153">Copy the following code snippet and paste into `HelloWebView.cpp` after the `// <-- WebView2 sample code starts here -->` note and before the `// <-- WebView2 sample code ends here -->` note.</span></span>  

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

### <span data-ttu-id="a1f6c-154">Criar seu aplicativo de exemplo do Bing</span><span class="sxs-lookup"><span data-stu-id="a1f6c-154">Build your Bing sample app</span></span>  

<span data-ttu-id="a1f6c-155">Selecione `F5` para compilar e executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-155">Select `F5` to build and run the app.</span></span>  <span data-ttu-id="a1f6c-156">Agora você tem uma janela do WebView que exibe a página do Bing.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-156">Now you have a WebView window displaying the Bing page.</span></span>  

:::image type="complex" source="../media/bing-window.png" alt-text="Versão da ferramenta" lightbox="../media/bing-window.png":::
   <span data-ttu-id="a1f6c-158">Janela do Bing</span><span class="sxs-lookup"><span data-stu-id="a1f6c-158">Bing window</span></span>  
:::image-end:::  

## <span data-ttu-id="a1f6c-159">Etapa 4-eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="a1f6c-159">Step 4 - Navigation events</span></span>  

<span data-ttu-id="a1f6c-160">A equipe da WebView já abordou navegar para a URL usando o `ICoreWebView2::Navigate` método na última etapa.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-160">The WebView team already covered navigating to URL using the `ICoreWebView2::Navigate` method in the last step.</span></span>  <span data-ttu-id="a1f6c-161">Durante a navegação, o WebView aciona uma sequência de eventos que o host pode ouvir.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-161">During navigation, WebView fires a sequence of events to which the host may listen.</span></span>  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

<span data-ttu-id="a1f6c-162">Para obter mais informações, navegue até [eventos de navegação][Webview2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="a1f6c-162">For more information, navigate to [Navigation events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Versão da ferramenta" lightbox="../media/navigation-events.png":::
   <span data-ttu-id="a1f6c-164">Eventos de navegação</span><span class="sxs-lookup"><span data-stu-id="a1f6c-164">Navigation events</span></span>  
:::image-end:::  

<span data-ttu-id="a1f6c-165">Em casos de erro, um ou mais dos seguintes eventos podem ocorrer dependendo se a navegação é continuada para uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-165">In error cases, one or more of the following events may occur depending on whether the navigation is continued to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

<span data-ttu-id="a1f6c-166">Se ocorrer um redirecionamento HTTP, há vários `NavigationStarting` eventos em uma linha.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-166">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="a1f6c-167">Como um exemplo de como usar os eventos, registre um manipulador para o `NavigationStarting` evento para cancelar quaisquer solicitações que não sejam HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-167">As an example of using the events, register a handler for the `NavigationStarting` event to cancel any non-https requests.</span></span>  <span data-ttu-id="a1f6c-168">Copie o trecho de código a seguir e cole em `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="a1f6c-168">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="a1f6c-169">Agora o aplicativo não está navegando para sites não HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-169">Now the app is not navigating to any non-https sites.</span></span>  <span data-ttu-id="a1f6c-170">Você pode usar um mecanismo semelhante para realizar outras tarefas, como restringir a navegação para dentro do seu próprio domínio.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-170">You may use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>  

## <span data-ttu-id="a1f6c-171">Etapa 5-scripting</span><span class="sxs-lookup"><span data-stu-id="a1f6c-171">Step 5 - Scripting</span></span>  

<span data-ttu-id="a1f6c-172">O aplicativo de hospedagem também pode injetar JavaScript em WebView.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-172">The hosting app may also inject JavaScript into WebView.</span></span>  <span data-ttu-id="a1f6c-173">Você pode executar uma tarefa de WebView para executar JavaScript arbitrário ou adicionar scripts de inicialização.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-173">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="a1f6c-174">Scripts de inicialização adicionados se aplicam a todas as futuras navegação de documento de nível superior e de quadro filho até serem removidas.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-174">Added initialization scripts apply to all future top-level document and child frame navigation until removed.</span></span>  <span data-ttu-id="a1f6c-175">Os scripts de inicialização são executados após a criação do objeto global e antes da execução de qualquer outro script incluído no documento HTML.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-175">The initialization scripts run after creating the global object and before running any other script included by the HTML document.</span></span>  

<span data-ttu-id="a1f6c-176">Copie o trecho de código a seguir e cole em `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="a1f6c-176">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="a1f6c-177">Agora, o WebView deve sempre congelar o `Object` objeto e retornar o documento de página uma vez.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-177">Now, WebView should always freeze the `Object` object and returns the page document once.</span></span>  

> [!NOTE] 
> <span data-ttu-id="a1f6c-178">As APIs de injeção de script \ (e outras APIs WebView2 \) são assíncronas, você deve usar retornos de chamada se o código for deve ser executado em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-178">The script injection APIs \(and some other WebView2 APIs\) are asynchronous, you should use callbacks if code is must be run in a specific order.</span></span>  

## <span data-ttu-id="a1f6c-179">Etapa 6 – comunicação entre o conteúdo do host e da Web</span><span class="sxs-lookup"><span data-stu-id="a1f6c-179">Step 6 - Communication between host and web content</span></span>  

<span data-ttu-id="a1f6c-180">O host e o conteúdo da Web também podem se comunicar uns com os outros por meio do `postMessage` método.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-180">The host and the web content may also communicate with each other through the `postMessage` method.</span></span>  <span data-ttu-id="a1f6c-181">O conteúdo da Web em execução em um WebView pode postar no host por meio do `window.chrome.webview.postMessage` método, e a mensagem é manipulada por qualquer registro registrado no `ICoreWebView2WebMessageReceivedEventHandler` manipulador de eventos do host.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-181">The web content running within a WebView may post to the host through the `window.chrome.webview.postMessage` method, and the message is handled by any registered the `ICoreWebView2WebMessageReceivedEventHandler` event handler on the host.</span></span>  <span data-ttu-id="a1f6c-182">Da mesma forma, o host pode enviar uma mensagem ao conteúdo da Web por meio `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` do ou método, que é detectado por manipuladores adicionados pelo `window.chrome.webview.addEventListener` ouvinte.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-182">Likewise, the host may message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON` method, which is caught by handlers added from `window.chrome.webview.addEventListener` listener.</span></span>  <span data-ttu-id="a1f6c-183">O mecanismo de comunicação permite que o conteúdo da Web use recursos nativos, passando mensagens para solicitar que o host execute APIs nativas.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-183">The communication mechanism allows the web content to use native capabilities by passing messages to ask the host to run native APIs.</span></span>  

<span data-ttu-id="a1f6c-184">Como exemplo para entender o mecanismo, as seguintes etapas ocorrem quando você tenta imprimir a URL do documento no WebView.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-184">As an example to understand the mechanism, the following steps occur when you try printing out the document URL in WebView.</span></span>  

1.  <span data-ttu-id="a1f6c-185">O host registra um manipulador para retornar a mensagem recebida de volta para o conteúdo da Web</span><span class="sxs-lookup"><span data-stu-id="a1f6c-185">The host registers a handler to return received message back to the web content</span></span>  
1.  <span data-ttu-id="a1f6c-186">O host injeta um script para o conteúdo da Web que registra um manipulador para imprimir mensagens do host</span><span class="sxs-lookup"><span data-stu-id="a1f6c-186">The host injects a script to the web content that registers a handler to print message from the host</span></span>  
1.  <span data-ttu-id="a1f6c-187">O host injeta um script para o conteúdo da Web que envia a URL para o host</span><span class="sxs-lookup"><span data-stu-id="a1f6c-187">The host injects a script to the web content that posts the URL to the host</span></span>  
1.  <span data-ttu-id="a1f6c-188">O manipulador do host é disparado e retorna a mensagem \ (a URL \) ao conteúdo da Web</span><span class="sxs-lookup"><span data-stu-id="a1f6c-188">The handler of the host is triggered and returns the message \(the URL\) to the web content</span></span>  
1.  <span data-ttu-id="a1f6c-189">O manipulador do conteúdo da Web é disparado e imprime a mensagem do host \ (a URL \)</span><span class="sxs-lookup"><span data-stu-id="a1f6c-189">The handler of the web content is triggered and prints message from the host \(the URL\)</span></span>  

<span data-ttu-id="a1f6c-190">Copie o trecho de código a seguir e cole em `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="a1f6c-190">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>    

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

### <span data-ttu-id="a1f6c-191">Compilar o aplicativo de exemplo Mostrar URL</span><span class="sxs-lookup"><span data-stu-id="a1f6c-191">Build your show URL sample app</span></span>  

<span data-ttu-id="a1f6c-192">Selecione `F5` para compilar e executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-192">Select `F5` to build and run the app.</span></span>  <span data-ttu-id="a1f6c-193">A URL é exibida em uma janela pop-up antes de navegar para uma página.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-193">The URL appears in a pop-up window before navigating to a page.</span></span>  

:::image type="complex" source="../media/show-url.png" alt-text="Versão da ferramenta" lightbox="../media/show-url.png":::
   <span data-ttu-id="a1f6c-195">Mostrar URL</span><span class="sxs-lookup"><span data-stu-id="a1f6c-195">Show url</span></span>  
:::image-end:::  

<span data-ttu-id="a1f6c-196">Parabéns, você acabou de criar seu primeiro aplicativo WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-196">Congratulations, you just built your first WebView2 app.</span></span>  

## <span data-ttu-id="a1f6c-197">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="a1f6c-197">Next steps</span></span>  

<span data-ttu-id="a1f6c-198">Muitas das funcionalidades WebView2 que não estão incluídas nesta página, a seção a seguir forneceu recursos adicionais.</span><span class="sxs-lookup"><span data-stu-id="a1f6c-198">Many of the WebView2 functionalities that are not covered on this page, the following section provided additional resources.</span></span>  

### <span data-ttu-id="a1f6c-199">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a1f6c-199">See also</span></span>  

*   <span data-ttu-id="a1f6c-200">Para obter um exemplo abrangente de recursos do WebView2, navegue até o [exemplo de API WebView2][GithubMicrosoftedgeWebview2samplesApisample].</span><span class="sxs-lookup"><span data-stu-id="a1f6c-200">For a comprehensive example of WebView2 capabilities, navigate to [WebView2 API Sample][GithubMicrosoftedgeWebview2samplesApisample].</span></span>  
*   <span data-ttu-id="a1f6c-201">Para obter um aplicativo de exemplo criado usando WebView2, navegue até [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span><span class="sxs-lookup"><span data-stu-id="a1f6c-201">For a sample application built using WebView2, navigate to [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span></span>  
*   <span data-ttu-id="a1f6c-202">Para obter informações detalhadas sobre a API WebView2, navegue até [Referência API][Webview2ReferenceWin32].</span><span class="sxs-lookup"><span data-stu-id="a1f6c-202">For detailed information about the WebView2 API, navigate to [API reference][Webview2ReferenceWin32].</span></span>  

## <span data-ttu-id="a1f6c-203">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="a1f6c-203">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2Index]: ../index.md "Introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  
[Webview2ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Referência de C++ do WebView2 Win32 | Documentos da Microsoft"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegação | Documentos da Microsoft"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019&preserve-view=true "Biblioteca de modelos C++ do Windows Runtime (WRL) | Documentos da Microsoft"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019&preserve-view=true "Passo a passo: criar um aplicativo de área de trabalho tradicional do Windows (C++) | Documentos da Microsoft"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser-MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "Exemplo de API WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "Exemplos de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Bibliotecas de implementação do Windows (OUVIRÁ)-Microsoft/ouvirá | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar canais do Microsoft Edge Insider"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador do WebView2"  
