---
description: Saiba como depurar controles WebView2.
title: Depurando WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/22/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: ad6f334e5796d2f22146f2853ae1ef1d854e329c
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894316"
---
# <span data-ttu-id="369c2-104">Como depurar com WebView2</span><span class="sxs-lookup"><span data-stu-id="369c2-104">How to Debug with WebView2</span></span>  

<span data-ttu-id="369c2-105">O objetivo do controle WebView2 do Microsoft Edge é combinar o melhor dos recursos de desenvolvimento de aplicativos Web e nativo e ferramentas de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="369c2-105">The goal of the Microsoft Edge WebView2 control is combining the best of both the web and native application development features and developer tools.</span></span>  <span data-ttu-id="369c2-106">A página a seguir descreve as diferentes ferramentas a serem usadas ao desenvolver com controles WebView2.</span><span class="sxs-lookup"><span data-stu-id="369c2-106">The following page outlines the different tools to use when developing with WebView2 controls.</span></span>  

## <span data-ttu-id="369c2-107">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="369c2-107">Microsoft Edge DevTools</span></span>  

<span data-ttu-id="369c2-108">Use as [ferramentas de desenvolvedor do Microsoft Edge (Chromium)][DevtoolsGuideChromiumMain] para depurar o conteúdo da Web exibido em controles WebView2, da mesma forma que você usa o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="369c2-108">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you use Microsoft Edge.</span></span>  <span data-ttu-id="369c2-109">Para abrir o DevTools, defina o foco na janela do WebView e use qualquer uma das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="369c2-109">To open the DevTools, set focus on the WebView window and then use any of the following actions.</span></span>  
*   <span data-ttu-id="369c2-110">Selecione `F12` .</span><span class="sxs-lookup"><span data-stu-id="369c2-110">Select `F12`.</span></span>  
*   <span data-ttu-id="369c2-111">Selecione `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="369c2-111">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="369c2-112">Abra o menu de contexto \ (clique com o botão direito do mouse \) > selecionar `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="369c2-112">Open the context menu \(right-click\) > select `Inspect`.</span></span>  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools" lightbox="../media/f12.png":::
   <span data-ttu-id="369c2-114">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="369c2-114">Microsoft Edge DevTools</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="369c2-115">Quando você depura o aplicativo no Visual Studio com o depurador nativo anexado, o pressionamento `F12` pode disparar o depurador nativo em vez de ferramentas de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="369c2-115">When you debug your application in Visual Studio with the native debugger attached, pressing `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="369c2-116">Pressione `Ctrl` + `Shift` + `I` ou use o menu de contexto \ (clique com o botão direito do mouse \) para evitar a situação.</span><span class="sxs-lookup"><span data-stu-id="369c2-116">Press `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

> [!NOTE]
> <span data-ttu-id="369c2-117">Você pode usar o `--auto-open-devtools-for-tabs` argumento da linha de comando para abrir uma nova janela do devtools ao criar pela primeira vez um WebView.</span><span class="sxs-lookup"><span data-stu-id="369c2-117">You may use the `--auto-open-devtools-for-tabs` command-line argument to open a new DevTools window when you first create a WebView.</span></span>  <!--See `CreateCoreWebView2Controller` documentation for how to provide additional command-line arguments to the browser process.  See `LoaderOverride` registry key to examine different builds of WebView2 without modifying your application in the `CreateCoreWebView2Controller` documentation.  -->  

## <span data-ttu-id="369c2-118">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="369c2-118">Visual Studio</span></span>  

<span data-ttu-id="369c2-119">Use o depurador de script do Visual Studio 2019 versão 16,4 Preview 2 ou posterior para depurar seu script no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="369c2-119">Use the script debugger in Visual Studio 2019 version 16.4 Preview 2 or later to debug your script in Visual Studio.</span></span>  <span data-ttu-id="369c2-120">Verifique se o componente de **diagnóstico JavaScript** em **desenvolvimento de área de trabalho com carga de trabalho C++** está instalado.</span><span class="sxs-lookup"><span data-stu-id="369c2-120">Verify the **JavaScript diagnostics** component in **Desktop development with C++** workload is installed.</span></span>  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Diagnóstico do JavaScript do Visual Studio":::
   <span data-ttu-id="369c2-122">Diagnóstico do JavaScript do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="369c2-122">Visual Studio JavaScript diagnostics</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="369c2-123">Para habilitar a depuração de script do WebView2, abra o menu de contexto \ (clique com o botão direito do mouse \) em seu projeto > selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="369c2-123">To enable WebView2 script debugging, open the context menu \(right-click\) on your project > select **Properties**.</span></span>  

*   <span data-ttu-id="369c2-124">Em **Propriedades de configuração**, selecione **depuração**.</span><span class="sxs-lookup"><span data-stu-id="369c2-124">On **Configuration Properties**, select **Debugging**.</span></span>  
*   <span data-ttu-id="369c2-125">Na propriedade **tipo de depurador** , selecione **JavaScript (WebView2)** na lista de opções.</span><span class="sxs-lookup"><span data-stu-id="369c2-125">On the **Debugger Type** property, select **JavaScript (WebView2)** from the list of options.</span></span> 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Depurador do JavaScript do Visual Studio":::
   <span data-ttu-id="369c2-127">Depurador do JavaScript do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="369c2-127">Visual Studio JavaScript Debugger</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="369c2-128">Você está configurado e pronto para depurar.</span><span class="sxs-lookup"><span data-stu-id="369c2-128">You are all set up and ready to debug.</span></span>  

<span data-ttu-id="369c2-129">Para depurar, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="369c2-129">To Debug, complete the following actions.</span></span>  

1.  <span data-ttu-id="369c2-130">Definir pontos de interrupção</span><span class="sxs-lookup"><span data-stu-id="369c2-130">Set Breakpoints</span></span>  
    *   <span data-ttu-id="369c2-131">Abra o arquivo de script e defina o ponto de interrupção onde você deseja.</span><span class="sxs-lookup"><span data-stu-id="369c2-131">Open the script file and set the breakpoint where you want it.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="369c2-132">O adaptador de depuração JS/TS não faz o mapeamento de caminho de origem.</span><span class="sxs-lookup"><span data-stu-id="369c2-132">The JS/TS debug adapter does not do source path mapping.</span></span><span data-ttu-id="369c2-133">Você deve abrir exatamente o mesmo caminho associado à sua WebView2.</span><span class="sxs-lookup"><span data-stu-id="369c2-133">  You must open the exact same path associated with your WebView2.</span></span>  
        
1.  <span data-ttu-id="369c2-134">Executar código</span><span class="sxs-lookup"><span data-stu-id="369c2-134">Run Code</span></span>  
    *   <span data-ttu-id="369c2-135">Selecione seu tipo de compilação e ambiente de tempo de execução apropriados e inicie o depurador local do Windows.</span><span class="sxs-lookup"><span data-stu-id="369c2-135">Select your appropriate build flavor and runtime environment and then start the local windows debugger.</span></span>  
1.  <span data-ttu-id="369c2-136">Exibir console de depuração</span><span class="sxs-lookup"><span data-stu-id="369c2-136">View Debug Console</span></span>  
    *   <span data-ttu-id="369c2-137">Seu aplicativo é executado e o depurador se conecta após a criação do primeiro webview2.</span><span class="sxs-lookup"><span data-stu-id="369c2-137">You application runs and the debugger connects after the first webview2 is created.</span></span><span data-ttu-id="369c2-138">Qualquer saída de depuração pendente será exibida.</span><span class="sxs-lookup"><span data-stu-id="369c2-138">  Any pending debug output is displayed.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="369c2-139">Esse método de depuração está atualmente restrito a aplicativos Win32 e suplementos do Office.</span><span class="sxs-lookup"><span data-stu-id="369c2-139">This method of debugging is currently restricted to Win32 applications and Office add-ins.</span></span>  
        
## <span data-ttu-id="369c2-140">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="369c2-140">Visual Studio Code</span></span>  

<span data-ttu-id="369c2-141">Você pode usar o código do Visual Studio para depurar scripts executados em controles WebView2.</span><span class="sxs-lookup"><span data-stu-id="369c2-141">You may use Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <span data-ttu-id="369c2-142">Para obter mais informações, consulte [aplicativos do Microsoft Edge (Chromium) WebView][GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications].</span><span class="sxs-lookup"><span data-stu-id="369c2-142">For more information, see [Microsoft Edge (Chromium) WebView Applications][GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications].</span></span>  

<!--todo:  add See also heading  -->  

## <span data-ttu-id="369c2-143">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="369c2-143">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="369c2-144">Ajude a criar uma experiência de WebView2 mais rica compartilhando seus comentários.</span><span class="sxs-lookup"><span data-stu-id="369c2-144">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="369c2-145">Acesse o [repositório de comentários][GithubMicrosoftedgeWebviewfeedbackMain] para enviar solicitações de recursos ou relatórios de erros.</span><span class="sxs-lookup"><span data-stu-id="369c2-145">Visit the [feedback repo][GithubMicrosoftedgeWebviewfeedbackMain] to submit feature requests or bug reports.</span></span>  

<!--## Debugging  

Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`. You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView. See CreateCoreWebView2Controller documentation for how to provide additional command line arguments to the browser process. Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Controller documentation.  -->  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chromium) aplicativos WebView-VS Code-Debugger para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
