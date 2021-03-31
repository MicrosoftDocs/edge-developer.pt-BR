---
description: Microsoft Edge (Chromium) e código do Visual Studio
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, código vs, código do Visual Studio, depurador, dica da Web
ms.openlocfilehash: 1aa5b66043e87ebb0f1b848dcd60e2553b378f36
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230688"
---
# <span data-ttu-id="268cb-104">Visão geral do código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="268cb-104">Visual Studio Code overview</span></span>  

<span data-ttu-id="268cb-105">O [código do Visual Studio][VisualStudioCodeDocs] é um editor de código-fonte leve, mas potente.</span><span class="sxs-lookup"><span data-stu-id="268cb-105">[Visual Studio Code][VisualStudioCodeDocs] is a lightweight, but powerful source code editor.</span></span>  <span data-ttu-id="268cb-106">O [código do Visual Studio][VisualStudioCodeDocs] está disponível para Windows, Linux e MacOS.</span><span class="sxs-lookup"><span data-stu-id="268cb-106">[Visual Studio Code][VisualStudioCodeDocs] is available for Windows, Linux, and macOS.</span></span>  <span data-ttu-id="268cb-107">Ele inclui suporte interno para JavaScript, TypeScript e Node.js, portanto é uma ótima ferramenta para desenvolvedores da Web antes de você personalizá-lo.</span><span class="sxs-lookup"><span data-stu-id="268cb-107">It includes built-in support for JavaScript, TypeScript, and Node.js, so it is a great tool for web developers before you customize it.</span></span>  <span data-ttu-id="268cb-108">Se você ainda não o estiver usando, baixe o [código do Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="268cb-108">If you are not using it yet, download [Visual Studio Code][VisualstudioCode].</span></span>  

## <span data-ttu-id="268cb-109">Extensões</span><span class="sxs-lookup"><span data-stu-id="268cb-109">Extensions</span></span>  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

<span data-ttu-id="268cb-110">Para adquirir qualquer uma das extensões realçadas abaixo, navegue até Extensões \(selecione `Ctrl` + `Shift` + `X` no Windows/Linux ou `Command` + `Shift` + `X` no MacOS \) no código do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="268cb-110">To acquire any of the extensions highlighted below, navigate to Extensions \(select `Ctrl`+`Shift`+`X` on Windows/Linux or `Command`+`Shift`+`X` on macOS\) in Visual Studio Code.</span></span>  

<span data-ttu-id="268cb-111">Pesquise o Marketplace para obter a extensão específica e escolha **instalar**.</span><span class="sxs-lookup"><span data-stu-id="268cb-111">Search the Marketplace for the specific extension and choose **Install**.</span></span>  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Instalar o depurador para extensão de código do Microsoft Edge Visual Studio" lightbox="./media/vscode-debugger-install.png":::
   <span data-ttu-id="268cb-113">Instalar o **depurador para extensão de código do Microsoft Edge** Visual Studio</span><span class="sxs-lookup"><span data-stu-id="268cb-113">Install the **Debugger for Microsoft Edge** Visual Studio Code extension</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Depurador para extensão de código do Microsoft Edge Visual Studio" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         <span data-ttu-id="268cb-115">**Depurador para Microsoft Edge** Extensão de código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="268cb-115">**Debugger for Microsoft Edge** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="268cb-116">Depurador para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="268cb-116">Debugger for Microsoft Edge</span></span>](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Extensão de código do Visual Studio de ferramentas do Microsoft Edge para Visual Studio" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         <span data-ttu-id="268cb-118">**Ferramentas do Microsoft Edge para o código do Visual Studio** Extensão de código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="268cb-118">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="268cb-119">Ferramentas do Microsoft Edge para o código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="268cb-119">Microsoft Edge Tools for Visual Studio Code</span></span>](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="extensão de código do webdica Visual Studio" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         <span data-ttu-id="268cb-121">**webhint** Extensão de código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="268cb-121">**webhint** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="268cb-122">Dica da web</span><span class="sxs-lookup"><span data-stu-id="268cb-122">webhint</span></span>](#webhint)  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="268cb-123">Depurador para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="268cb-123">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="268cb-124">Com o [depurador para extensão de código do Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio, depure o código JavaScript front-end linha por linha e veja as `console.log()` instruções diretamente do [código do Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="268cb-124">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line-by-line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode].</span></span>  
      
<span data-ttu-id="268cb-125">Usando a ferramenta depurador, você pode iniciar ou anexar tanto ao Microsoft Edge \(EdgeHTML \) quanto ao Microsoft Edge \(Chromium \).</span><span class="sxs-lookup"><span data-stu-id="268cb-125">Using the Debugger tool, you may launch or attach to both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="268cb-126">Para obter instruções passo a passo para depurar o Microsoft Edge do Visual Studio e configurações de exemplo `launch.json` , navegue até [depurador para extensão de código do Visual Studio do Microsoft Edge][VisualStudioCodeDebuggerEdge].</span><span class="sxs-lookup"><span data-stu-id="268cb-126">For a walkthrough of debugging Microsoft Edge from Visual Studio Code and sample `launch.json` configurations, navigate to [Debugger For Microsoft Edge Visual Studio Code Extension][VisualStudioCodeDebuggerEdge].</span></span>  <span data-ttu-id="268cb-127">Escolha a imagem a seguir para ver a extensão em ação.</span><span class="sxs-lookup"><span data-stu-id="268cb-127">Choose the following image to see the extension in action.</span></span>  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Depurador para extensão de código do Edge Visual Studio em ação" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="268cb-129">**Depurador para Microsoft Edge** Extensão de código do Visual Studio em ação</span><span class="sxs-lookup"><span data-stu-id="268cb-129">**Debugger for Microsoft Edge** Visual Studio Code extension in action</span></span>  
:::image-end:::  

## <span data-ttu-id="268cb-130">Ferramentas do Microsoft Edge para o código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="268cb-130">Microsoft Edge Tools for Visual Studio Code</span></span>

<span data-ttu-id="268cb-131">Com a extensão de código do Visual Studio de código do Visual Studio [Tools do Microsoft Edge][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] , use a ferramenta **elementos** do navegador Microsoft Edge dentro do código do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="268cb-131">With the [Microsoft Edge Tools for Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code extension, use the **Elements** tool of the Microsoft Edge browser within Visual Studio Code.</span></span>  <span data-ttu-id="268cb-132">Use-o para as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="268cb-132">Use it for the following actions.</span></span>  

*   <span data-ttu-id="268cb-133">Anexar a uma instância ou iniciar uma instância do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="268cb-133">Attach to an instance or launch an instance of Microsoft Edge.</span></span>  
*   <span data-ttu-id="268cb-134">Exiba a estrutura HTML do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="268cb-134">Display the runtime HTML structure.</span></span>  
*   <span data-ttu-id="268cb-135">Atualize o layout.</span><span class="sxs-lookup"><span data-stu-id="268cb-135">Update the layout.</span></span>  
*   <span data-ttu-id="268cb-136">Corrigir problemas de estilo.</span><span class="sxs-lookup"><span data-stu-id="268cb-136">Fix styling issues.</span></span>  
    
<span data-ttu-id="268cb-137">Para obter mais informações, acesse a [extensão de código do Visual Studio de código do Visual Studio para ferramentas do Microsoft Edge][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].</span><span class="sxs-lookup"><span data-stu-id="268cb-137">For more information, navigate to [Microsoft Edge Tools for Visual Studio Code Visual Studio Code extension][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].</span></span>  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Extensão de código do Visual Studio de ferramentas do Microsoft Edge para Visual Studio em ação" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   <span data-ttu-id="268cb-139">**Ferramentas do Microsoft Edge para o código do Visual Studio** Extensão de código do Visual Studio em ação</span><span class="sxs-lookup"><span data-stu-id="268cb-139">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension in action</span></span>  
:::image-end:::  

## <span data-ttu-id="268cb-140">Dica da web</span><span class="sxs-lookup"><span data-stu-id="268cb-140">webhint</span></span>  
      
<span data-ttu-id="268cb-141">Use [webhint][WebhintMain], uma ferramenta de refiapoção personalizável, para melhorar a funcionalidade do seu site a seguir.</span><span class="sxs-lookup"><span data-stu-id="268cb-141">Use [webhint][WebhintMain], a customizable linting tool, to improve the following functionality of your site.</span></span>  

*   <span data-ttu-id="268cb-142">Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="268cb-142">Accessibility</span></span>
*   <span data-ttu-id="268cb-143">Desempenho</span><span class="sxs-lookup"><span data-stu-id="268cb-143">Performance</span></span>
*   <span data-ttu-id="268cb-144">Compatibilidade entre navegadores</span><span class="sxs-lookup"><span data-stu-id="268cb-144">Cross-browser compatibility</span></span>
*   <span data-ttu-id="268cb-145">Compatibilidade com o PWA</span><span class="sxs-lookup"><span data-stu-id="268cb-145">PWA compatibility</span></span>
*   <span data-ttu-id="268cb-146">Segurança</span><span class="sxs-lookup"><span data-stu-id="268cb-146">Security</span></span>

<span data-ttu-id="268cb-147">Ele verifica o código em busca de práticas de codificação e erros comuns.</span><span class="sxs-lookup"><span data-stu-id="268cb-147">It checks your code for coding practices and common errors.</span></span> <span data-ttu-id="268cb-148">O projeto de código-fonte aberto da webdica, inicialmente desenvolvido pela equipe do Microsoft Edge, agora faz parte da [Fundação do OpenJS][OpenjsFoundation].</span><span class="sxs-lookup"><span data-stu-id="268cb-148">The webhint open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="268cb-149">A equipe do Microsoft Edge continua a contribuir para webhint junto com desenvolvedores da Web na Comunidade.</span><span class="sxs-lookup"><span data-stu-id="268cb-149">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Captura de tela da extensão de código do webdica Visual Studio" lightbox="./media/webhint-extension.png":::
   <span data-ttu-id="268cb-151">Captura de tela da extensão de código do **webdica** Visual Studio</span><span class="sxs-lookup"><span data-stu-id="268cb-151">Screenshot of **webhint** Visual Studio Code extension</span></span>  
:::image-end:::  
      
<span data-ttu-id="268cb-152">Identifique e corrija os problemas no seu site adicionando a [extensão webhint para o código do Visual Studio][VisualstudioMarketplaceWebhint].</span><span class="sxs-lookup"><span data-stu-id="268cb-152">Identify and fix problems in your website by adding the [webhint extension for Visual Studio Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="268cb-153">Dicas examine HTML, CSS, JavaScript, TypeScript e muito mais.</span><span class="sxs-lookup"><span data-stu-id="268cb-153">Hints examine HTML, CSS, JavaScript, TypeScript, and more.</span></span>  <span data-ttu-id="268cb-154">As dicas aparecem como sublinhados embutidos e são resumidas no painel **problemas** .</span><span class="sxs-lookup"><span data-stu-id="268cb-154">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  
      
<span data-ttu-id="268cb-155">Para obter mais informações, navegue até [como usar o webhint no código do Visual Studio][VisualStudioCodeWebhint].</span><span class="sxs-lookup"><span data-stu-id="268cb-155">For more information, navigate to [How to use webhint in Visual Studio Code][VisualStudioCodeWebhint].</span></span>  

<!--links -->  

[VisualStudioCodeDebuggerEdge]: ./debugger-for-edge.md "Depurador para extensão de código do Microsoft Edge Visual Studio | Documentos da Microsoft"  
[VisualStudioCodeMicrosoftEdgeDevtoolsExtension]: ./microsoft-edge-devtools-extension.md "Extensão de código do Microsoft Edge DevTools para Visual Studio | Documentos da Microsoft"  
[VisualStudioCodeWebhint]: ./webhint.md "Webhint Visual Studio extensão de código | Documentos da Microsoft"  

[VisualstudioCode]: https://code.visualstudio.com "Código do Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentação | Código do Visual Studio"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Ferramentas do Microsoft Edge para o código do Visual Studio | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "webhint"  
[OpenjsFoundation]:  https://openjsf.org "Base do OpenJS"  
