---
description: Saiba como depurar controles WebView2.
title: Introdução à depuração de aplicativos WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/13/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: dcdeeadc2c25bcf50834176706b8d181f06f994a
ms.sourcegitcommit: 6c7ededf8677fd7add5e4060e92f9ec4cfdb6952
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "10927885"
---
# <span data-ttu-id="79a11-104">Introdução à depuração de aplicativos WebView2</span><span class="sxs-lookup"><span data-stu-id="79a11-104">Get started debugging WebView2 applications</span></span>  

<span data-ttu-id="79a11-105">O objetivo do controle WebView2 do Microsoft Edge é combinar o melhor dos recursos e ferramentas de desenvolvimento de aplicativo Web e nativo.</span><span class="sxs-lookup"><span data-stu-id="79a11-105">The goal of the Microsoft Edge WebView2 control is to combine the best of both the web and native application development features and tools.</span></span>  <span data-ttu-id="79a11-106">Ao desenvolver seu aplicativo WebView2, você deve depurar seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="79a11-106">When you develop your WebView2 application, you should debug your application.</span></span>  <span data-ttu-id="79a11-107">Este artigo descreve as diferentes ferramentas a serem usadas para depurar o código nativo e Web em seu aplicativo do WebView2.</span><span class="sxs-lookup"><span data-stu-id="79a11-107">This article outlines the different tools to use to debug both your web and native code in your WebView2 application.</span></span>  

## [<span data-ttu-id="79a11-108">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="79a11-108">Microsoft Edge DevTools</span></span>](#tab/devtools)  

<span data-ttu-id="79a11-109">Use as [ferramentas de desenvolvedor do Microsoft Edge (Chromium)][DevtoolsGuideChromiumMain] para depurar o conteúdo da Web exibido em controles WebView2, da mesma forma que você pode depurar para outra página da Web exibida no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="79a11-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you may debug for another webpage displayed in Microsoft Edge.</span></span>  <span data-ttu-id="79a11-110">Para abrir o DevTools, defina o foco no controle WebView e use uma das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="79a11-110">To open the DevTools, set focus on the WebView control and then use one of the following actions.</span></span>  

*   <span data-ttu-id="79a11-111">Selecione `F12` .</span><span class="sxs-lookup"><span data-stu-id="79a11-111">Select `F12`.</span></span>  
*   <span data-ttu-id="79a11-112">Selecione `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="79a11-112">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="79a11-113">Abra o menu de contexto \ (clique com o botão direito do mouse \) e escolha `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="79a11-113">Open the context menu \(right-click\) and choose `Inspect`.</span></span>  

<span data-ttu-id="79a11-114">Para obter mais informações, consulte [visão geral de devtools][DevtoolsGuideChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="79a11-114">For more information, see [DevTools overview][DevtoolsGuideChromiumMain].</span></span>  

:::image type="complex" source="./media/f12.png" alt-text="Depuração DevTools" lightbox="./media/f12.png":::
   <span data-ttu-id="79a11-116">Depuração DevTools</span><span class="sxs-lookup"><span data-stu-id="79a11-116">DevTools debugging</span></span>  
:::image-end:::  

## [<span data-ttu-id="79a11-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="79a11-117">Visual Studio</span></span>](#tab/visualstudio)  

<span data-ttu-id="79a11-118">O Visual Studio fornece várias ferramentas de depuração para o código nativo e Web em aplicativos do WebView2.</span><span class="sxs-lookup"><span data-stu-id="79a11-118">Visual Studio provides various debugging tools for web and native code in WebView2 applications.</span></span>  <span data-ttu-id="79a11-119">Na seção do Visual Studio, o foco principalmente é a depuração de controles WebView, mas os outros métodos de depuração no Visual Studio estão disponíveis normalmente.</span><span class="sxs-lookup"><span data-stu-id="79a11-119">In the Visual Studio section, the primarily focus is debugging WebView controls, however the other methods of debugging in Visual Studio are available as usual.</span></span>  <span data-ttu-id="79a11-120">Use o processo a seguir para depurar o código nativo e Web somente em aplicativos Win32 ou em suplementos do Office.</span><span class="sxs-lookup"><span data-stu-id="79a11-120">Use the following process to debug web and native code in Win32 applications or Office add-ins only.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="79a11-121">Quando você depura o aplicativo no Visual Studio com o depurador nativo anexado, a seleção `F12` pode disparar o depurador nativo em vez de ferramentas de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="79a11-121">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="79a11-122">Selecione `Ctrl` + `Shift` + `I` ou use o menu de contexto \ (clique com o botão direito do mouse \) para evitar a situação.</span><span class="sxs-lookup"><span data-stu-id="79a11-122">Select `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

<span data-ttu-id="79a11-123">Antes de começar, certifique-se de que os seguintes requisitos sejam atendidos.</span><span class="sxs-lookup"><span data-stu-id="79a11-123">Before you begin, ensure the following requirements are met.</span></span>  

*   <span data-ttu-id="79a11-124">Para depurar scripts, o aplicativo deve ser iniciado no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="79a11-124">To debug scripts, the app must be launched from within Visual Studio.</span></span>  
*   <span data-ttu-id="79a11-125">Não é possível anexar um depurador a um processo de WebView2 em execução.</span><span class="sxs-lookup"><span data-stu-id="79a11-125">You cannot attach a debugger to a running WebView2 process.</span></span>  
*   <span data-ttu-id="79a11-126">Instale o Visual Studio 2019 versão 16,4 Preview 2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="79a11-126">Install Visual Studio 2019 version 16.4 Preview 2 or later.</span></span>  

<span data-ttu-id="79a11-127">Instale e configure as ferramentas do depurador de scripts no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="79a11-127">Install and set up the script debugger tools in Visual Studio.</span></span>  

1.  <span data-ttu-id="79a11-128">Conclua as seguintes ações para instalar o componente de **diagnóstico JavaScript** no **desenvolvimento de área de trabalho com C++**.</span><span class="sxs-lookup"><span data-stu-id="79a11-128">Complete the following actions to install the **JavaScript diagnostics** component in **Desktop development with C++**.</span></span>  

    1. <span data-ttu-id="79a11-129">Na barra do Windows Explorer, digite `Visual Studio Installer` .</span><span class="sxs-lookup"><span data-stu-id="79a11-129">In the Windows Explorer bar, type `Visual Studio Installer`.</span></span>  
    1. <span data-ttu-id="79a11-130">Escolha **instalador do Visual Studio** para abri-lo.</span><span class="sxs-lookup"><span data-stu-id="79a11-130">Choose **Visual Studio Installer** to open it.</span></span>  
    1. <span data-ttu-id="79a11-131">No instalador do Visual Studio, na versão instalada, escolha o botão **mais** e, em seguida, escolha **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="79a11-131">In the Visual Studio Installer, on the installed version, choose the **More** button, and then choose **Modify**.</span></span>  
    1. <span data-ttu-id="79a11-132">No Visual Studio, em **cargas**de trabalho, escolha a configuração **desenvolvimento de área de trabalho em C++** .</span><span class="sxs-lookup"><span data-stu-id="79a11-132">In Visual Studio, under **Workloads**, choose the **Desktop Development in C++** setting.</span></span>  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Tela modificando cargas de trabalho do Visual Studio" lightbox="./media/workloads.png":::
            <span data-ttu-id="79a11-134">Tela modificando cargas de trabalho do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="79a11-134">Visual Studio Modifying Workloads Screen</span></span> :::image-end:::  
        
    1.  <span data-ttu-id="79a11-135">Escolha **componentes individuais**.</span><span class="sxs-lookup"><span data-stu-id="79a11-135">Choose **Individual components**.</span></span>  
    1.  <span data-ttu-id="79a11-136">Na caixa de pesquisa, digite `JavaScript diagnostics` .</span><span class="sxs-lookup"><span data-stu-id="79a11-136">In the search box, enter `JavaScript diagnostics`.</span></span>  
    1.  <span data-ttu-id="79a11-137">Escolha a configuração **diagnóstico de JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="79a11-137">Choose the **JavaScript diagnostics** setting.</span></span>  
    1.  <span data-ttu-id="79a11-138">Escolha **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="79a11-138">Choose **Modify**.</span></span> 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Visual Studio modificando a guia componentes individuais" lightbox="./media/indivcomp.png":::
           <span data-ttu-id="79a11-140">Visual Studio modificando a guia componentes individuais</span><span class="sxs-lookup"><span data-stu-id="79a11-140">Visual Studio Modifying Individual Components Tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="79a11-141">Habilite a depuração de script para aplicativos do WebView2.</span><span class="sxs-lookup"><span data-stu-id="79a11-141">Enable script debugging for WebView2 applications.</span></span>  
    1.  <span data-ttu-id="79a11-142">No projeto do WebView2, abra o menu de contexto \ (clique com o botão direito do mouse \) e escolha **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="79a11-142">In your WebView2 project, open the context menu \(right-click\), and choose **Properties**.</span></span>  
    1.  <span data-ttu-id="79a11-143">Em **Propriedades de configuração**, escolha **depuração**.</span><span class="sxs-lookup"><span data-stu-id="79a11-143">Under the **Configuration Properties**, choose **Debugging**.</span></span>  
    1.  <span data-ttu-id="79a11-144">Em **tipo de depurador**, escolha **JavaScript (WebView2)**.</span><span class="sxs-lookup"><span data-stu-id="79a11-144">Under the **Debugger Type**, choose **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Propriedade de configuração de depuração do Visual Studio" lightbox="./media/enbjs.png":::
           <span data-ttu-id="79a11-146">Propriedade de configuração de **depuração** do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="79a11-146">Visual Studio **Debugging** Configuration Property</span></span>  
        :::image-end:::  
        
<span data-ttu-id="79a11-147">Conclua as seguintes ações para depurar seu aplicativo WebView2.</span><span class="sxs-lookup"><span data-stu-id="79a11-147">Complete the following actions to debug your WebView2 application.</span></span>  

1.  <span data-ttu-id="79a11-148">Para definir um ponto de interrupção no código-fonte, passe o mouse à esquerda do número da linha e escolha definir um ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="79a11-148">To set a breakpoint in your source code, hover to the left of the line number, and choose to set a breakpoint.</span></span>  <span data-ttu-id="79a11-149">O adaptador de depuração JS/TS não executa o mapeamento de caminho de origem.</span><span class="sxs-lookup"><span data-stu-id="79a11-149">The JS/TS debug adapter does not perform source path mapping.</span></span>  <span data-ttu-id="79a11-150">Você deve abrir exatamente o mesmo caminho associado à sua WebView2.</span><span class="sxs-lookup"><span data-stu-id="79a11-150">You must open the exact same path associated with your WebView2.</span></span>  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Adicionar ponto de interrupção do Visual Studio" lightbox="./media/breakpoint.png"::: 
       <span data-ttu-id="79a11-152">Adicionar ponto de interrupção do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="79a11-152">Visual Studio add breakpoint</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="79a11-153">Para executar o depurador, escolha o tamanho do bit da plataforma e escolha o botão de reprodução verde ao lado de **depurador local do Windows**.</span><span class="sxs-lookup"><span data-stu-id="79a11-153">To run the debugger, choose the bit size of the platform, and then choose the green play button next to **Local Windows Debugger**.</span></span>  <span data-ttu-id="79a11-154">O aplicativo é executado e o depurador se conecta ao primeiro processo WebView2 criado.</span><span class="sxs-lookup"><span data-stu-id="79a11-154">The application runs and the debugger connects to the first WebView2 process that is created.</span></span>  
    
    :::image type="complex" source="./media/run.png" alt-text=" Depurador local do Windows do Visual Studio" lightbox="./media/run.png"::: 
       <span data-ttu-id="79a11-156">**Depurador local do Windows** do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="79a11-156">Visual Studio **Local Windows Debugger**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="79a11-157">No **console de depuração**, localize a saída do depurador.</span><span class="sxs-lookup"><span data-stu-id="79a11-157">In the **Debug Console**, find the output from the debugger.</span></span>  
    
    :::image type="complex" source="./media/console.png" alt-text=" Console de depuração do Visual Studio" lightbox="./media/console.png"::: 
       <span data-ttu-id="79a11-159">Console de **depuração** do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="79a11-159">Visual Studio **Debug Console**</span></span>  
    :::image-end:::  
    
* * *  

## <span data-ttu-id="79a11-160">Consulte também</span><span class="sxs-lookup"><span data-stu-id="79a11-160">See also</span></span>  

*   <span data-ttu-id="79a11-161">Para começar a usar o WebView2, confira [WebView2 guias de introdução][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="79a11-161">To get started using WebView2, see [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="79a11-162">Para obter um exemplo abrangente de recursos do WebView2, consulte o repositório do [WebView2Samples][GithubMicrosoftedgeWebview2samples] no github.</span><span class="sxs-lookup"><span data-stu-id="79a11-162">For a comprehensive example of WebView2 capabilities, see the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>
*   <span data-ttu-id="79a11-163">Para obter informações mais detalhadas sobre APIs do WebView2, consulte [referência de API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="79a11-163">For more detailed information about WebView2 APIs, see [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="79a11-164">Para obter mais informações sobre o WebView2, consulte [recursos do WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="79a11-164">For more information about WebView2, see [WebView2 Resources][Webview2MainNextSteps].</span></span>

## <span data-ttu-id="79a11-165">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="79a11-165">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  

[Webview2ReferenceDotnet09515MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-515/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "AdditionalBrowserArguments-0.9.515-a classe Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions | Documentos da Microsoft"  
[Webview2ReferenceWin3209538Webview2IdlParameters]: ../reference/win32/0-9-538/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-globais | Documentos da Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Referência de API do Microsoft Edge WebView2 | Documentos da Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Próximas etapas-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Ponto de partida-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Quais são as novidades? -Depurador JavaScript para código do Visual Studio-Microsoft/vscode-js-depuração | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicativos WebView do Microsoft Edge (Chromium)-depurador de código do Visual Studio para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
