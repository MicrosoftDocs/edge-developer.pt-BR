---
description: Saiba como depurar controles WebView2.
title: Depurando WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 386bc237257be0ade8c48bc1c737b0151a882719
ms.sourcegitcommit: 5bdffe91a6594f77eeffa4e864fda90a02784771
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659676"
---
# <span data-ttu-id="42d71-104">Como depurar ao desenvolver com controles WebView2</span><span class="sxs-lookup"><span data-stu-id="42d71-104">How to Debug when developing with WebView2 controls</span></span>  

<span data-ttu-id="42d71-105">O objetivo do controle WebView2 do Microsoft Edge é combinar o melhor dos recursos de desenvolvimento de aplicativos Web e nativo e ferramentas de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="42d71-105">The goal of the Microsoft Edge WebView2 control is combining the best of both the web and native application development features and developer tools.</span></span>  <span data-ttu-id="42d71-106">Este artigo descreve as diferentes ferramentas a serem usadas ao desenvolver com controles WebView2.</span><span class="sxs-lookup"><span data-stu-id="42d71-106">This article outlines the different tools to use when developing with WebView2 controls.</span></span>  

## <span data-ttu-id="42d71-107">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="42d71-107">Microsoft Edge DevTools</span></span>  

<span data-ttu-id="42d71-108">Use as [ferramentas de desenvolvedor do Microsoft Edge (Chromium)](/microsoft-edge/devtools-guide-chromium) para depurar o conteúdo da Web exibido em controles WebView2, da mesma forma que faria se estivesse usando o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="42d71-108">Use [Microsoft Edge (Chromium) Developer Tools](/microsoft-edge/devtools-guide-chromium) to debug web content displayed in WebView2 controls, in the same way that you would if you were using Microsoft Edge.</span></span>  <span data-ttu-id="42d71-109">Para abrir o DevTools, defina o foco na janela do WebView e use qualquer uma das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="42d71-109">To open the DevTools, set focus on the WebView window and then use any of the following options.</span></span>  
*   <span data-ttu-id="42d71-110">Selecione `F12` .</span><span class="sxs-lookup"><span data-stu-id="42d71-110">Select `F12`.</span></span>  
*   <span data-ttu-id="42d71-111">Selecione `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="42d71-111">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="42d71-112">Abra o menu de contexto \ (clique com o botão direito do mouse \) > selecionar `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="42d71-112">Open the context menu \(right-click\) > select `Inspect`.</span></span>  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools":::
   <span data-ttu-id="42d71-114">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="42d71-114">Microsoft Edge DevTools</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="42d71-115">Quando você depura o aplicativo no Visual Studio com o depurador nativo anexado, a seleção `F12` pode disparar o depurador nativo em vez de ferramentas de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="42d71-115">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="42d71-116">Use `Ctrl` + `Shift` + `I` ou use o menu de contexto \ (clique com o botão direito do mouse \) para evitar essa situação.</span><span class="sxs-lookup"><span data-stu-id="42d71-116">Use `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid this situation.</span></span>  

## <span data-ttu-id="42d71-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="42d71-117">Visual Studio</span></span>  

<span data-ttu-id="42d71-118">Use o depurador de script do Visual Studio 2019 versão 16,4 Preview 2 ou posterior para depurar seu script no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="42d71-118">Use the script debugger in Visual Studio 2019 version 16.4 Preview 2 or later to debug your script in Visual Studio.</span></span>  <span data-ttu-id="42d71-119">Verifique se o componente de **diagnóstico JavaScript** em **desenvolvimento de área de trabalho com carga de trabalho C++** está instalado.</span><span class="sxs-lookup"><span data-stu-id="42d71-119">Verify the **JavaScript diagnostics** component in **Desktop development with C++** workload is installed.</span></span>  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Diagnóstico do JavaScript do Visual Studio":::
   <span data-ttu-id="42d71-121">Diagnóstico do JavaScript do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="42d71-121">Visual Studio JavaScript diagnostics</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="42d71-122">Para habilitar a depuração de script do WebView2, abra o menu de contexto \ (clique com o botão direito do mouse \) em seu projeto > selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="42d71-122">To enable WebView2 script debugging, open the context menu \(right-click\) on your project > select **Properties**.</span></span>  <span data-ttu-id="42d71-123">Em **Propriedades de configuração**, selecione **depuração**.</span><span class="sxs-lookup"><span data-stu-id="42d71-123">On **Configuration Properties**, select **Debugging**.</span></span>  <span data-ttu-id="42d71-124">Na propriedade **tipo de depurador** , escolha **JavaScript (WebView2)** na lista de opções.</span><span class="sxs-lookup"><span data-stu-id="42d71-124">On the **Debugger Type** property, choose **JavaScript (WebView2)** from the list of options.</span></span> 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Depurador do JavaScript do Visual Studio":::
   <span data-ttu-id="42d71-126">Depurador do JavaScript do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="42d71-126">Visual Studio JavaScript Debugger</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

## <span data-ttu-id="42d71-127">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="42d71-127">Visual Studio Code</span></span>  

<span data-ttu-id="42d71-128">Você pode usar o código do Visual Studio para depurar scripts executados em controles WebView2.</span><span class="sxs-lookup"><span data-stu-id="42d71-128">You may use Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <span data-ttu-id="42d71-129">Para obter mais informações, consulte [aplicativos do Microsoft Edge (Chromium) WebView](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).</span><span class="sxs-lookup"><span data-stu-id="42d71-129">For more information, see [Microsoft Edge (Chromium) WebView Applications](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).</span></span>  

<!--todo:  add See also heading  -->  

## <span data-ttu-id="42d71-130">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="42d71-130">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="42d71-131">Ajude a criar uma experiência de WebView2 mais rica compartilhando seus comentários.</span><span class="sxs-lookup"><span data-stu-id="42d71-131">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="42d71-132">Acesse o [repositório de comentários](https://aka.ms/webviewfeedback) para enviar solicitações de recursos ou relatórios de erros.</span><span class="sxs-lookup"><span data-stu-id="42d71-132">Visit the [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports.</span></span>  
