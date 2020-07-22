---
description: Saiba como depurar controles WebView2.
title: Depurando WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 232104abc360cfa660d567ffb66535213fcb3ae0
ms.sourcegitcommit: a82aa5fc1ada35cd8274490fbff3c0a850785835
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/21/2020
ms.locfileid: "10888574"
---
# <span data-ttu-id="e8874-104">Como depurar com WebView2</span><span class="sxs-lookup"><span data-stu-id="e8874-104">How to Debug with WebView2</span></span>  

<span data-ttu-id="e8874-105">O objetivo do controle WebView2 do Microsoft Edge é combinar o melhor dos recursos de desenvolvimento de aplicativos Web e nativo e ferramentas de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="e8874-105">The goal of the Microsoft Edge WebView2 control is combining the best of both the web and native application development features and developer tools.</span></span>  <span data-ttu-id="e8874-106">A página a seguir descreve as diferentes ferramentas a serem usadas ao desenvolver com controles WebView2.</span><span class="sxs-lookup"><span data-stu-id="e8874-106">The following page outlines the different tools to use when developing with WebView2 controls.</span></span>  

## <span data-ttu-id="e8874-107">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e8874-107">Microsoft Edge DevTools</span></span>  

<span data-ttu-id="e8874-108">Use as [ferramentas de desenvolvedor do Microsoft Edge (Chromium)][DevtoolsMain] para depurar o conteúdo da Web exibido em controles WebView2, da mesma forma que faria se estivesse usando o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e8874-108">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsMain] to debug web content displayed in WebView2 controls, in the same way that you would if you were using Microsoft Edge.</span></span>  <span data-ttu-id="e8874-109">Para abrir o DevTools, defina o foco na janela do WebView e use qualquer uma das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="e8874-109">To open the DevTools, set focus on the WebView window and then use any of the following actions.</span></span>  

*   <span data-ttu-id="e8874-110">Selecione `F12` .</span><span class="sxs-lookup"><span data-stu-id="e8874-110">Select `F12`.</span></span>  
*   <span data-ttu-id="e8874-111">Selecione `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="e8874-111">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="e8874-112">Abra o menu de contexto \ (clique com o botão direito do mouse \) e selecione `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="e8874-112">Open the context menu \(right-click\) and select `Inspect`.</span></span>  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools" lightbox="../media/f12.png":::
   <span data-ttu-id="e8874-114">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e8874-114">Microsoft Edge DevTools</span></span>  
:::image-end:::  

> [!IMPORTANT]
> <span data-ttu-id="e8874-115">Quando você depura o aplicativo no Visual Studio com o depurador nativo anexado, a seleção `F12` pode disparar o depurador nativo em vez de ferramentas de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="e8874-115">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="e8874-116">Use `Ctrl` + `Shift` + `I` ou use o menu de contexto \ (clique com o botão direito do mouse \) para evitar a situação.</span><span class="sxs-lookup"><span data-stu-id="e8874-116">Use `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

## <span data-ttu-id="e8874-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e8874-117">Visual Studio</span></span>  

<span data-ttu-id="e8874-118">Você pode usar o Visual Studio para desenvolver o código do aplicativo e depurar scripts ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="e8874-118">You may use Visual Studio to develop application code and debug scripts at the same time.</span></span>  

<span data-ttu-id="e8874-119">Tenha o seguinte em mente.</span><span class="sxs-lookup"><span data-stu-id="e8874-119">Keep the following things in mind.</span></span>  

*   <span data-ttu-id="e8874-120">O Visual Studio só oferece suporte a scripts de depuração quando o aplicativo é iniciado no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e8874-120">Visual Studio only supports debugging scripts when the app is launched from within Visual Studio.</span></span>  <span data-ttu-id="e8874-121">\ (Não há suporte para anexar um processo em execução para depuração. \)</span><span class="sxs-lookup"><span data-stu-id="e8874-121">\(Attaching a running process for debugging is not supported.\)</span></span>  
*   <span data-ttu-id="e8874-122">Não há suporte para o cenário de depuração de webviews direcionado.</span><span class="sxs-lookup"><span data-stu-id="e8874-122">The targeted WebView debugging scenario is not supported.</span></span>  

<span data-ttu-id="e8874-123">Use o depurador de script do Visual Studio 2019 versão 16,4 Preview 2 ou posterior para depurar seu script no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e8874-123">Use the script debugger in Visual Studio 2019 version 16.4 Preview 2 or later to debug your script in Visual Studio.</span></span>  

<span data-ttu-id="e8874-124">Configurar o depurador.</span><span class="sxs-lookup"><span data-stu-id="e8874-124">Set up the debugger.</span></span>  

*   <span data-ttu-id="e8874-125">Verifique se o componente de **diagnóstico JavaScript** em **desenvolvimento de área de trabalho com carga de trabalho C++** está instalado.</span><span class="sxs-lookup"><span data-stu-id="e8874-125">Verify the **JavaScript diagnostics** component in **Desktop development with C++** workload is installed.</span></span>  
    
    1.  <span data-ttu-id="e8874-126">Navegue até **aplicativos &** configurações de recursos no Windows.</span><span class="sxs-lookup"><span data-stu-id="e8874-126">Navigate to **Apps & features** settings in Windows.</span></span>  <span data-ttu-id="e8874-127">Pesquise por ele usando a barra de tarefas do Windows.</span><span class="sxs-lookup"><span data-stu-id="e8874-127">Search for it using the Windows task bar.</span></span>  
    1.  <span data-ttu-id="e8874-128">Escolha **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="e8874-128">Choose **Modify**.</span></span>  
    1.  <span data-ttu-id="e8874-129">Verifique se as caixas de seleção **diagnóstico** e **desenvolvimento da área de trabalho do JavaScript em C++** estão marcadas.</span><span class="sxs-lookup"><span data-stu-id="e8874-129">Verify the **Javascript diagnostics** and **Desktop Development in C++** checkboxes are selected.</span></span>  
        
        :::image type="complex" source="../media/appsandfeatures.png" alt-text="Aplicativos e recursos" lightbox="../media/appsandfeatures.png":::
           <span data-ttu-id="e8874-131">Aplicativos e recursos</span><span class="sxs-lookup"><span data-stu-id="e8874-131">Apps & Features</span></span>  
        :::image-end:::  
        
*   <span data-ttu-id="e8874-132">Habilite a depuração de script WebView2.</span><span class="sxs-lookup"><span data-stu-id="e8874-132">Enable WebView2 script debugging.</span></span>  
    1.  <span data-ttu-id="e8874-133">Passe o mouse no seu projeto, abra o menu de contexto \ (clique com o botão direito do mouse \) e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="e8874-133">Hover on your project, open the context menu \(right-click\), and select **Properties**.</span></span>  
    1.  <span data-ttu-id="e8874-134">Em **Propriedades de configuração**, selecione **depuração**.</span><span class="sxs-lookup"><span data-stu-id="e8874-134">On **Configuration Properties**, select **Debugging**.</span></span>  
    1.  <span data-ttu-id="e8874-135">Na propriedade **tipo de depurador** , procure a lista de opções e selecione **JavaScript (WebView2)**.</span><span class="sxs-lookup"><span data-stu-id="e8874-135">On the **Debugger Type** property, search the the list of options, and select **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="../media/enbjs.png" alt-text="Depurador do JavaScript do Visual Studio" lightbox="../media/enbjs.png":::
           <span data-ttu-id="e8874-137">Depurador do JavaScript do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e8874-137">Visual Studio JavaScript Debugger</span></span>  
        :::image-end:::  
        
<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="e8874-138">Você está configurado e pronto para depurar.</span><span class="sxs-lookup"><span data-stu-id="e8874-138">You are all set up and ready to debug.</span></span>  

<span data-ttu-id="e8874-139">Para depurar, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="e8874-139">To Debug, complete the following actions.</span></span>  

1.  <span data-ttu-id="e8874-140">Definir pontos de interrupção</span><span class="sxs-lookup"><span data-stu-id="e8874-140">Set Breakpoints</span></span>  
    *   <span data-ttu-id="e8874-141">Abra o arquivo de script e defina o ponto de interrupção onde você deseja.</span><span class="sxs-lookup"><span data-stu-id="e8874-141">Open the script file and set the breakpoint where you want it.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="e8874-142">O adaptador de depuração JS/TS não faz o mapeamento de caminho de origem.</span><span class="sxs-lookup"><span data-stu-id="e8874-142">The JS/TS debug adapter does not do source path mapping.</span></span><span data-ttu-id="e8874-143">Você deve abrir exatamente o mesmo caminho associado à sua WebView2.</span><span class="sxs-lookup"><span data-stu-id="e8874-143">  You must open the exact same path associated with your WebView2.</span></span>  
        
1.  <span data-ttu-id="e8874-144">Executar código</span><span class="sxs-lookup"><span data-stu-id="e8874-144">Run Code</span></span>  
    *   <span data-ttu-id="e8874-145">Selecione seu tipo de compilação e ambiente de tempo de execução apropriados e inicie o depurador local do Windows.</span><span class="sxs-lookup"><span data-stu-id="e8874-145">Select your appropriate build flavor and runtime environment and then start the local windows debugger.</span></span>  
1.  <span data-ttu-id="e8874-146">Exibir console de depuração</span><span class="sxs-lookup"><span data-stu-id="e8874-146">View Debug Console</span></span>  
    *   <span data-ttu-id="e8874-147">Seu aplicativo é executado e o depurador se conecta após a criação do primeiro webview2.</span><span class="sxs-lookup"><span data-stu-id="e8874-147">You application runs and the debugger connects after the first webview2 is created.</span></span><span data-ttu-id="e8874-148">Qualquer saída de depuração pendente será exibida.</span><span class="sxs-lookup"><span data-stu-id="e8874-148">  Any pending debug output is displayed.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="e8874-149">Esse método de depuração está atualmente restrito a aplicativos Win32 e suplementos do Office.</span><span class="sxs-lookup"><span data-stu-id="e8874-149">This method of debugging is currently restricted to Win32 applications and Office add-ins.</span></span>  
        
## <span data-ttu-id="e8874-150">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="e8874-150">Visual Studio Code</span></span>  

<span data-ttu-id="e8874-151">Você pode usar o código do Visual Studio para depurar scripts executados em controles WebView2.</span><span class="sxs-lookup"><span data-stu-id="e8874-151">You may use Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <span data-ttu-id="e8874-152">Para obter mais informações, consulte [aplicativos do Microsoft Edge (Chromium) WebView][GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications].</span><span class="sxs-lookup"><span data-stu-id="e8874-152">For more information, see [Microsoft Edge (Chromium) WebView Applications][GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications].</span></span>  

<!--todo:  add See also heading  -->  

## <span data-ttu-id="e8874-153">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="e8874-153">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="e8874-154">Ajude a criar uma experiência de WebView2 mais rica compartilhando seus comentários.</span><span class="sxs-lookup"><span data-stu-id="e8874-154">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="e8874-155">Acesse o [repositório de comentários][GithubMicrosoftedgeWebviewfeedback] para enviar solicitações de recursos ou relatórios de erros.</span><span class="sxs-lookup"><span data-stu-id="e8874-155">Visit the [feedback repo][GithubMicrosoftedgeWebviewfeedback] to submit feature requests or bug reports.</span></span>  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chromium) aplicativos WebView-VS-depurador de código-depurador para Microsoft Edge | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
