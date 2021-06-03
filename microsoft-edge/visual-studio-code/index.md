---
description: Microsoft Edge (Chromium) e Visual Studio Code
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, vs code, código do visual studio, depurador, webhint
ms.openlocfilehash: 1aa5b66043e87ebb0f1b848dcd60e2553b378f36
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230688"
---
# <span data-ttu-id="27b0d-104">Visão geral do Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="27b0d-104">Visual Studio Code overview</span></span>  

<span data-ttu-id="27b0d-105">[Visual Studio Code][VisualStudioCodeDocs] é um editor de código-fonte leve, mas poderoso.</span><span class="sxs-lookup"><span data-stu-id="27b0d-105">[Visual Studio Code][VisualStudioCodeDocs] is a lightweight, but powerful source code editor.</span></span>  <span data-ttu-id="27b0d-106">[Visual Studio Code][VisualStudioCodeDocs] está disponível para Windows, Linux e macOS.</span><span class="sxs-lookup"><span data-stu-id="27b0d-106">[Visual Studio Code][VisualStudioCodeDocs] is available for Windows, Linux, and macOS.</span></span>  <span data-ttu-id="27b0d-107">Ele inclui suporte integrado para JavaScript, TypeScript e Node.js, portanto, é uma ótima ferramenta para desenvolvedores da Web antes de personalizá-lo.</span><span class="sxs-lookup"><span data-stu-id="27b0d-107">It includes built-in support for JavaScript, TypeScript, and Node.js, so it is a great tool for web developers before you customize it.</span></span>  <span data-ttu-id="27b0d-108">Se você ainda não estiver usando, baixe [Visual Studio Code][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="27b0d-108">If you are not using it yet, download [Visual Studio Code][VisualstudioCode].</span></span>  

## <span data-ttu-id="27b0d-109">Extensões</span><span class="sxs-lookup"><span data-stu-id="27b0d-109">Extensions</span></span>  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

<span data-ttu-id="27b0d-110">Para adquirir qualquer uma das extensões realçadas abaixo, navegue até Extensões \(selecione em `Ctrl` + `Shift` + `X` Windows/Linux ou `Command` + `Shift` + `X` no macOS\) no Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="27b0d-110">To acquire any of the extensions highlighted below, navigate to Extensions \(select `Ctrl`+`Shift`+`X` on Windows/Linux or `Command`+`Shift`+`X` on macOS\) in Visual Studio Code.</span></span>  

<span data-ttu-id="27b0d-111">Pesquise o Marketplace para a extensão específica e escolha **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="27b0d-111">Search the Marketplace for the specific extension and choose **Install**.</span></span>  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Instalar o Depurador para Microsoft Edge Visual Studio Code extensão" lightbox="./media/vscode-debugger-install.png":::
   <span data-ttu-id="27b0d-113">Instalar o **Depurador para Microsoft Edge** Visual Studio Code extensão</span><span class="sxs-lookup"><span data-stu-id="27b0d-113">Install the **Debugger for Microsoft Edge** Visual Studio Code extension</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Depurador para Microsoft Edge Visual Studio Code extensão" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         <span data-ttu-id="27b0d-115">**Depurador para Microsoft Edge** Visual Studio Code extensão</span><span class="sxs-lookup"><span data-stu-id="27b0d-115">**Debugger for Microsoft Edge** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="27b0d-116">Depurador para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="27b0d-116">Debugger for Microsoft Edge</span></span>](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Microsoft Edge Ferramentas para Visual Studio Code Visual Studio Code extensão" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         <span data-ttu-id="27b0d-118">**Microsoft Edge Ferramentas para Visual Studio Code** Visual Studio Code extensão</span><span class="sxs-lookup"><span data-stu-id="27b0d-118">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="27b0d-119">Microsoft Edge Ferramentas para Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="27b0d-119">Microsoft Edge Tools for Visual Studio Code</span></span>](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="webhint Visual Studio Code extensão" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         <span data-ttu-id="27b0d-121">**webhint** Visual Studio Code extensão</span><span class="sxs-lookup"><span data-stu-id="27b0d-121">**webhint** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="27b0d-122">Dica da web</span><span class="sxs-lookup"><span data-stu-id="27b0d-122">webhint</span></span>](#webhint)  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="27b0d-123">Depurador para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="27b0d-123">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="27b0d-124">Com o [Depurador][VisualstudioMarketplaceDebuggerMicrosoftEdge] para Microsoft Edge Visual Studio Code, depure seu código javaScript front-end linha por linha e consulte instruções diretamente de `console.log()` [Visual Studio Code][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="27b0d-124">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line-by-line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode].</span></span>  
      
<span data-ttu-id="27b0d-125">Usando a ferramenta Depurador, você pode iniciar ou anexar Microsoft Edge \(EdgeHTML\) e Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="27b0d-125">Using the Debugger tool, you may launch or attach to both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="27b0d-126">Para um passo a passo de depuração Microsoft Edge de configurações Visual Studio Code exemplo e de exemplo, navegue até `launch.json` [Depurador para Microsoft Edge Visual Studio Code Extension][VisualStudioCodeDebuggerEdge].</span><span class="sxs-lookup"><span data-stu-id="27b0d-126">For a walkthrough of debugging Microsoft Edge from Visual Studio Code and sample `launch.json` configurations, navigate to [Debugger For Microsoft Edge Visual Studio Code Extension][VisualStudioCodeDebuggerEdge].</span></span>  <span data-ttu-id="27b0d-127">Escolha a imagem a seguir para ver a extensão em ação.</span><span class="sxs-lookup"><span data-stu-id="27b0d-127">Choose the following image to see the extension in action.</span></span>  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Depurador para extensão Visual Studio Code de Borda em ação" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="27b0d-129">**Depurador para Microsoft Edge** Visual Studio Code extensão em ação</span><span class="sxs-lookup"><span data-stu-id="27b0d-129">**Debugger for Microsoft Edge** Visual Studio Code extension in action</span></span>  
:::image-end:::  

## <span data-ttu-id="27b0d-130">Microsoft Edge Ferramentas para Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="27b0d-130">Microsoft Edge Tools for Visual Studio Code</span></span>

<span data-ttu-id="27b0d-131">Com a [Microsoft Edge ferramentas para Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code, use a ferramenta **Elements** do navegador Microsoft Edge no Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="27b0d-131">With the [Microsoft Edge Tools for Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code extension, use the **Elements** tool of the Microsoft Edge browser within Visual Studio Code.</span></span>  <span data-ttu-id="27b0d-132">Use-o para as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="27b0d-132">Use it for the following actions.</span></span>  

*   <span data-ttu-id="27b0d-133">Anexar a uma instância ou iniciar uma instância de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="27b0d-133">Attach to an instance or launch an instance of Microsoft Edge.</span></span>  
*   <span data-ttu-id="27b0d-134">Exibe a estrutura HTML do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="27b0d-134">Display the runtime HTML structure.</span></span>  
*   <span data-ttu-id="27b0d-135">Atualize o layout.</span><span class="sxs-lookup"><span data-stu-id="27b0d-135">Update the layout.</span></span>  
*   <span data-ttu-id="27b0d-136">Correção de problemas de estilo.</span><span class="sxs-lookup"><span data-stu-id="27b0d-136">Fix styling issues.</span></span>  
    
<span data-ttu-id="27b0d-137">Para obter mais informações, navegue [até Microsoft Edge Ferramentas para Visual Studio Code Visual Studio Code extensão][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].</span><span class="sxs-lookup"><span data-stu-id="27b0d-137">For more information, navigate to [Microsoft Edge Tools for Visual Studio Code Visual Studio Code extension][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].</span></span>  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Microsoft Edge Ferramentas para Visual Studio Code Visual Studio Code extensão em ação" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   <span data-ttu-id="27b0d-139">**Microsoft Edge Ferramentas para Visual Studio Code** Visual Studio Code em ação</span><span class="sxs-lookup"><span data-stu-id="27b0d-139">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension in action</span></span>  
:::image-end:::  

## <span data-ttu-id="27b0d-140">Dica da web</span><span class="sxs-lookup"><span data-stu-id="27b0d-140">webhint</span></span>  
      
<span data-ttu-id="27b0d-141">Use [webhint][WebhintMain], uma ferramenta de linting personalizável, para melhorar a funcionalidade a seguir do seu site.</span><span class="sxs-lookup"><span data-stu-id="27b0d-141">Use [webhint][WebhintMain], a customizable linting tool, to improve the following functionality of your site.</span></span>  

*   <span data-ttu-id="27b0d-142">Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="27b0d-142">Accessibility</span></span>
*   <span data-ttu-id="27b0d-143">Desempenho</span><span class="sxs-lookup"><span data-stu-id="27b0d-143">Performance</span></span>
*   <span data-ttu-id="27b0d-144">Compatibilidade entre navegadores</span><span class="sxs-lookup"><span data-stu-id="27b0d-144">Cross-browser compatibility</span></span>
*   <span data-ttu-id="27b0d-145">PWA compatibilidade</span><span class="sxs-lookup"><span data-stu-id="27b0d-145">PWA compatibility</span></span>
*   <span data-ttu-id="27b0d-146">Segurança</span><span class="sxs-lookup"><span data-stu-id="27b0d-146">Security</span></span>

<span data-ttu-id="27b0d-147">Ele verifica seu código em busca de práticas de codificação e erros comuns.</span><span class="sxs-lookup"><span data-stu-id="27b0d-147">It checks your code for coding practices and common errors.</span></span> <span data-ttu-id="27b0d-148">O projeto de código aberto webhint, inicialmente desenvolvido pela equipe Microsoft Edge, agora faz parte do [OpenJS Foundation][OpenjsFoundation].</span><span class="sxs-lookup"><span data-stu-id="27b0d-148">The webhint open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="27b0d-149">A Microsoft Edge equipe continua a contribuir para Webhint junto com os desenvolvedores da Web na comunidade.</span><span class="sxs-lookup"><span data-stu-id="27b0d-149">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Captura de tela da extensão Visual Studio Code webhint" lightbox="./media/webhint-extension.png":::
   <span data-ttu-id="27b0d-151">Captura de tela **da extensão Visual Studio Code webhint**</span><span class="sxs-lookup"><span data-stu-id="27b0d-151">Screenshot of **webhint** Visual Studio Code extension</span></span>  
:::image-end:::  
      
<span data-ttu-id="27b0d-152">Identifique e corrige problemas em seu site adicionando a [extensão webhint para Visual Studio Code][VisualstudioMarketplaceWebhint].</span><span class="sxs-lookup"><span data-stu-id="27b0d-152">Identify and fix problems in your website by adding the [webhint extension for Visual Studio Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="27b0d-153">As dicas examinam HTML, CSS, JavaScript, TypeScript e muito mais.</span><span class="sxs-lookup"><span data-stu-id="27b0d-153">Hints examine HTML, CSS, JavaScript, TypeScript, and more.</span></span>  <span data-ttu-id="27b0d-154">As dicas aparecem como sublinhados em linha e são resumidas no painel **Problemas.**</span><span class="sxs-lookup"><span data-stu-id="27b0d-154">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  
      
<span data-ttu-id="27b0d-155">Para obter mais informações, navegue [até Como usar webhint em Visual Studio Code][VisualStudioCodeWebhint].</span><span class="sxs-lookup"><span data-stu-id="27b0d-155">For more information, navigate to [How to use webhint in Visual Studio Code][VisualStudioCodeWebhint].</span></span>  

<!--links -->  

[VisualStudioCodeDebuggerEdge]: ./debugger-for-edge.md "Depurador para Microsoft Edge Visual Studio Code extensão | Microsoft Docs"  
[VisualStudioCodeMicrosoftEdgeDevtoolsExtension]: ./microsoft-edge-devtools-extension.md "Microsoft Edge DevTools para Visual Studio Code extensão | Microsoft Docs"  
[VisualStudioCodeWebhint]: ./webhint.md "Webhint Visual Studio Code Extension | Microsoft Docs"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentação | Visual Studio Code"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Ferramentas do Microsoft Edge para o Visual Studio Code | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "webhint"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  
