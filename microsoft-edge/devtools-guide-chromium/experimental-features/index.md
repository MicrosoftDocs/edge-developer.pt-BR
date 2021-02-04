---
description: Os recursos experimentais mais recentes no Microsoft Edge DevTools
title: Recursos experimentais
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas f12, devtools, experimento
ms.openlocfilehash: 018364d4debc1791685a028c337f61f85865ef6b
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313034"
---
# <span data-ttu-id="9785f-104">Recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="9785f-104">Experimental features</span></span>  

<span data-ttu-id="9785f-105">O Microsoft Edge DevTools fornece acesso a recursos experimentais que ainda estão em desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="9785f-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="9785f-106">Você pode testar e [fornecer comentários antes](#providing-feedback-on-experimental-features) de cada recurso ser lançado.</span><span class="sxs-lookup"><span data-stu-id="9785f-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="9785f-107">Embora os recursos experimentais estão disponíveis em todos os canais do Microsoft Edge, você pode obter os recursos experimentais mais recentes usando o canal Canary do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9785f-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="9785f-108">Ativar recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="9785f-108">Turn on experimental features</span></span>  

<span data-ttu-id="9785f-109">Para ativar \(ou desativar\) recursos experimentais no Microsoft Edge, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9785f-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="9785f-110">[Abra o DevTools.][DevtoolsOpenMain]</span><span class="sxs-lookup"><span data-stu-id="9785f-110">[Open DevTools][DevtoolsOpenMain].</span></span>  
    *   <span data-ttu-id="9785f-111">Selecione `Control` + `Shift` + `I` \(Windows, Linux\) ou `Command` + `Option` + `I` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="9785f-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="9785f-112">Para obter mais informações, navegue até atalhos de teclado do [Microsoft Edge DevTools.][DevToolsShortcuts]</span><span class="sxs-lookup"><span data-stu-id="9785f-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="9785f-113">Abra o [painel Configurações.][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="9785f-113">Open the [Settings][DevToolsCustomizeIndexSettings] pane.</span></span>  
    *   <span data-ttu-id="9785f-114">Selecione `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="9785f-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="9785f-115">Para obter mais informações, navegue até atalhos de teclado do [Microsoft Edge DevTools.][DevToolsShortcuts]</span><span class="sxs-lookup"><span data-stu-id="9785f-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="9785f-116">No lado esquerdo do painel **Configurações,** escolha a **seção** Experimentos.</span><span class="sxs-lookup"><span data-stu-id="9785f-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="A página Experimentos em Configurações" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="9785f-118">A **página Experimentos** em **Configurações**</span><span class="sxs-lookup"><span data-stu-id="9785f-118">The **Experiments** page in **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9785f-119">Na página **Experimentos,** role pela lista de todos os recursos experimentais disponíveis e marque a caixa de seleção ao lado de cada recurso que você deseja testar.</span><span class="sxs-lookup"><span data-stu-id="9785f-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="9785f-120">Feche e reabra o Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="9785f-121">Os recursos experimentais estão sendo constantemente atualizados e podem causar problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="9785f-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="9785f-122">Para desativar um recurso experimental, abra a página **Experimentos** e limpe a caixa de seleção do recurso experimental que você deseja desativar.</span><span class="sxs-lookup"><span data-stu-id="9785f-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="9785f-123">Recursos experimentais realçados</span><span class="sxs-lookup"><span data-stu-id="9785f-123">Highlighted experimental features</span></span>  

<span data-ttu-id="9785f-124">As seções a seguir descrevem os novos recursos experimentais disponíveis no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9785f-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="9785f-125">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="9785f-125">Experimental feature</span></span> | <span data-ttu-id="9785f-126">Versão do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9785f-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="9785f-127">Habilitar webhint</span><span class="sxs-lookup"><span data-stu-id="9785f-127">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="9785f-128">85 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9785f-128">85 or later</span></span> |  
| [<span data-ttu-id="9785f-129">Habilitar o Console de Rede</span><span class="sxs-lookup"><span data-stu-id="9785f-129">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="9785f-130">85 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9785f-130">85 or later</span></span> |  
| [<span data-ttu-id="9785f-131">Visualizador da Ordem de Origem</span><span class="sxs-lookup"><span data-stu-id="9785f-131">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="9785f-132">86 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9785f-132">86 or later</span></span> |  
| [<span data-ttu-id="9785f-133">Habilitar o editor de atalho do teclado</span><span class="sxs-lookup"><span data-stu-id="9785f-133">Enable keyboard shortcut editor</span></span>](#enable-keyboard-shortcut-editor) | <span data-ttu-id="9785f-134">87 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9785f-134">87 or later</span></span> |  
| [<span data-ttu-id="9785f-135">Habilitar camadas compostas no modo de exibição 3D</span><span class="sxs-lookup"><span data-stu-id="9785f-135">Enable Composited Layers in 3D View</span></span>](#enable-composited-layers-in-3d-view) | <span data-ttu-id="9785f-136">87 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9785f-136">87 or later</span></span> |  
| [<span data-ttu-id="9785f-137">Habilitar a nova ferramenta Editor de Fontes no painel Estilos</span><span class="sxs-lookup"><span data-stu-id="9785f-137">Enable new Font Editor tool within the Styles pane</span></span>](#) | <span data-ttu-id="9785f-138">89 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9785f-138">89 or later</span></span> |  
| [<span data-ttu-id="9785f-139">Habilitar novos recursos de depuração do CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="9785f-139">Enable new CSS Flexbox debugging features</span></span>](#enable-new-css-flexbox-debugging-features) | <span data-ttu-id="9785f-140">89 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9785f-140">89 or later</span></span> |  
| [<span data-ttu-id="9785f-141">Habilitar + menus de guia de botão para abrir mais ferramentas</span><span class="sxs-lookup"><span data-stu-id="9785f-141">Enable + button tab menus to open more tools</span></span>](#enable--button-tab-menus-to-open-more-tools) | <span data-ttu-id="9785f-142">89 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9785f-142">89 or later</span></span> |  
| [<span data-ttu-id="9785f-143">Habilitar guia Bem-vindo</span><span class="sxs-lookup"><span data-stu-id="9785f-143">Enable Welcome tab</span></span>](#enable-welcome-tool) | <span data-ttu-id="9785f-144">89 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9785f-144">89 or later</span></span> |  

### <span data-ttu-id="9785f-145">Habilitar novos recursos de depuração de grade CSS</span><span class="sxs-lookup"><span data-stu-id="9785f-145">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="9785f-146">Esse recurso experimental fornece várias novas visualizações para ajudá-lo a depurar layouts de grade CSS.</span><span class="sxs-lookup"><span data-stu-id="9785f-146">This experimental feature provides a number of new visualizations to help you debug CSS grid layouts.</span></span>  <span data-ttu-id="9785f-147">Para visualizar os recursos experimentais mais recentes, [habilita este experimento](#turn-on-experimental-features) e recarregue o DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-147">To preview the latest experimental features, [enable this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  <span data-ttu-id="9785f-148">Esse experimento está por padrão no Microsoft Edge versão 87 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9785f-148">This experiment is on by default in Microsoft Edge version 87 or later.</span></span>  

#### <span data-ttu-id="9785f-149">Exibindo sobreposições de grade em foco com a ferramenta Inspect</span><span class="sxs-lookup"><span data-stu-id="9785f-149">Viewing on-hover grid overlays with the Inspect tool</span></span>  

<span data-ttu-id="9785f-150">A **ferramenta Inspect** fornece uma maneira rápida de identificar e visualizar layouts de grade CSS em um site ao passar o mouse sobre eles.</span><span class="sxs-lookup"><span data-stu-id="9785f-150">The **Inspect** tool provides a quick way to identify and visualize CSS Grid layouts in a website by hovering over them with the mouse.</span></span>  <span data-ttu-id="9785f-151">Escolha o **ícone Inspecionar** \( ![ Inspecionar ](../media/inspect-icon.msft.png) \) no canto superior esquerdo do DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-151">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="9785f-152">Em seguida, passe o mouse sobre um elemento Grid no site que você está depurando.</span><span class="sxs-lookup"><span data-stu-id="9785f-152">Then, hover over a Grid element on the website you are debugging.</span></span>  <span data-ttu-id="9785f-153">Os contornos são exibidos ao redor da grade, e o sombreamento indica a localização das lacunas de grade, se presente.</span><span class="sxs-lookup"><span data-stu-id="9785f-153">Outlines are displayed around the grid, and shading indicates the location of grid gaps if present.</span></span>  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Exibindo grades com a ferramenta Inspect" lightbox="../media/grid-inspect.msft.png":::
   <span data-ttu-id="9785f-155">Exibindo grades com a **ferramenta Inspect**</span><span class="sxs-lookup"><span data-stu-id="9785f-155">Viewing grids with the **Inspect** tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="9785f-156">Exibindo sobreposições de grade persistente</span><span class="sxs-lookup"><span data-stu-id="9785f-156">Viewing persistent grid overlays</span></span>  

<span data-ttu-id="9785f-157">No Microsoft Edge versão 86 ou posterior, o recurso de grade CSS experimental também oferece a opção de habilitar sobreposições de grade persistentes.</span><span class="sxs-lookup"><span data-stu-id="9785f-157">In Microsoft Edge version 86 or later, the experimental CSS grid feature also offers the option to enable persistent Grid overlays.</span></span>  <span data-ttu-id="9785f-158">As sobreposições persistentes oferecem vários benefícios.</span><span class="sxs-lookup"><span data-stu-id="9785f-158">The persistent overlays provide several benefits.</span></span>  

*   <span data-ttu-id="9785f-159">As sobreposições persistentes permanecem visíveis na página à medida que você rola, move o mouse e usa outros recursos do DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-159">The persistent overlays remain visible on the page as you scroll, move your mouse, and use other features of the DevTools.</span></span>  
*   <span data-ttu-id="9785f-160">Várias sobreposições persistentes podem ser habilitadas ao mesmo tempo, permitindo que você revise vários layouts de grade ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="9785f-160">Multiple persistent overlays can be enabled at the same time, allowing you to review several grid layouts at once.</span></span>  
*   <span data-ttu-id="9785f-161">As sobreposições persistentes oferecem muitas opções de configuração, como ocultar ou mostrar nomes na área de grade, lacunas de grade, tamanhos de controle e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9785f-161">Persistent overlays offer many configuration options, such as hiding or showing names in the grid area, grid gaps, track sizes, and so on.</span></span>  
    
<span data-ttu-id="9785f-162">As duas maneiras de alternar uma sobreposição de grade persistente.</span><span class="sxs-lookup"><span data-stu-id="9785f-162">The two ways to toggle a persistent grid overlay.</span></span>  

*   <span data-ttu-id="9785f-163">Escolha o **ícone de** oval Grade ao lado de qualquer elemento Grid mostrado na árvore DOM da **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="9785f-163">Choose the **Grid** oval icon next to any Grid element shown in the DOM tree of the **Elements** tool.</span></span>  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Ícone de oval de grade na ferramenta Elementos" lightbox="../media/grid-adorner.msft.png":::
       <span data-ttu-id="9785f-165">Ícone de oval de grade na **ferramenta Elementos**</span><span class="sxs-lookup"><span data-stu-id="9785f-165">Grid oval icon in **Elements** tool</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="9785f-166">Abra o novo **painel layout** localizado na ferramenta Elementos e escolha a caixa de seleção ao lado de cada elemento grid que você deseja realçar.</span><span class="sxs-lookup"><span data-stu-id="9785f-166">Open the new **Layout** panel located in the Elements tool, and choose the checkbox next to each Grid element you want to highlight.</span></span>  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Painel de layout no DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       <span data-ttu-id="9785f-168">**Painel** de layout no DevTools</span><span class="sxs-lookup"><span data-stu-id="9785f-168">**Layout** panel in DevTools</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="9785f-169">Configurando sobreposições persistentes</span><span class="sxs-lookup"><span data-stu-id="9785f-169">Configuring persistent overlays</span></span>  

<span data-ttu-id="9785f-170">No Microsoft Edge versão 86 ou posterior, o \*\*\*\* novo painel \*\*\*\* **de Layout** está localizado na ferramenta Elementos junto com as guias Estilos **e** Calculados.</span><span class="sxs-lookup"><span data-stu-id="9785f-170">In Microsoft Edge version 86 or later, the new **Layout** panel is located in the **Elements** tool alongside the **Styles** and **Computed** tabs.</span></span>  <span data-ttu-id="9785f-171">O **painel layout** superfícies opções de configuração para sobreposições persistentes.</span><span class="sxs-lookup"><span data-stu-id="9785f-171">The **Layout** panel surfaces configuration options for persistent overlays.</span></span>  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Recurso de depuração de grade CSS" lightbox="../media/experiments-grid.msft.png":::
   <span data-ttu-id="9785f-173">Recurso de depuração de grade CSS</span><span class="sxs-lookup"><span data-stu-id="9785f-173">CSS grid debugging feature</span></span>  
:::image-end:::  

### <span data-ttu-id="9785f-174">Habilitar o suporte para mover guias entre painéis</span><span class="sxs-lookup"><span data-stu-id="9785f-174">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="9785f-175">Normalmente, ferramentas como **Elementos** **e** Rede só podem abrir no painel principal localizado na parte superior do DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-175">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="9785f-176">Ferramentas como **Exibição 3D** e Problemas que normalmente só abrem no painel **Gaveta** que está localizado na parte inferior do DevTools. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9785f-176">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="9785f-177">Depois de escolher o experimento, você pode mover ferramentas entre os painéis superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="9785f-177">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="9785f-178">Para mover uma ferramenta, passe o mouse sobre a guia, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Mover** para cima ou Mover para **baixo.**</span><span class="sxs-lookup"><span data-stu-id="9785f-178">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="9785f-179">Esse experimento permite que você personalize o layout do DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-179">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="9785f-180">Para exibir ou ocultar o painel **Gaveta,** selecione `Escape` .</span><span class="sxs-lookup"><span data-stu-id="9785f-180">To display or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Movendo guias entre painéis" lightbox="../media/experiments-move-panels.msft.png":::
   <span data-ttu-id="9785f-182">Movendo guias entre painéis</span><span class="sxs-lookup"><span data-stu-id="9785f-182">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9785f-183">Habilitar webhint</span><span class="sxs-lookup"><span data-stu-id="9785f-183">Enable webhint</span></span>  

<span data-ttu-id="9785f-184">[webhint é][WebhintMain] uma ferramenta de código aberto que fornece comentários em tempo real para sites e páginas da Web locais.</span><span class="sxs-lookup"><span data-stu-id="9785f-184">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="9785f-185">O tipo de comentário fornecido pela [webhint][WebhintMain].</span><span class="sxs-lookup"><span data-stu-id="9785f-185">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="9785f-186">acessibilidade</span><span class="sxs-lookup"><span data-stu-id="9785f-186">accessibility</span></span>  
*   <span data-ttu-id="9785f-187">compatibilidade entre navegadores</span><span class="sxs-lookup"><span data-stu-id="9785f-187">cross-browser compatibility</span></span>  
*   <span data-ttu-id="9785f-188">segurança</span><span class="sxs-lookup"><span data-stu-id="9785f-188">security</span></span>  
*   <span data-ttu-id="9785f-189">desempenho</span><span class="sxs-lookup"><span data-stu-id="9785f-189">performance</span></span>  
*   <span data-ttu-id="9785f-190">Aplicativos Web progressivos (PWAs)</span><span class="sxs-lookup"><span data-stu-id="9785f-190">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="9785f-191">outros problemas comuns de desenvolvimento na Web</span><span class="sxs-lookup"><span data-stu-id="9785f-191">other common web development issues</span></span>  
    
<span data-ttu-id="9785f-192">O [experimento webhint][WebhintMain] exibe os comentários de webhint [no][DevtoolsIssues] painel Problemas.</span><span class="sxs-lookup"><span data-stu-id="9785f-192">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="9785f-193">Escolha um problema para exibir a documentação da solução e uma lista dos recursos afetados em seu site.</span><span class="sxs-lookup"><span data-stu-id="9785f-193">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="9785f-194">Escolha um link de recurso para abrir \*\*\*\* o painel **Rede** **,** Fontes ou Elementos relevantes no DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-194">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="webhint feedback in the Issues panel" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="9785f-196">webhint feedback in the **Issues** panel</span><span class="sxs-lookup"><span data-stu-id="9785f-196">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9785f-197">Habilitar o Console de Rede</span><span class="sxs-lookup"><span data-stu-id="9785f-197">Enable Network Console</span></span>  

<span data-ttu-id="9785f-198">**Console de** rede é o título de trabalho de um experimento para fazer solicitações de rede sintética sobre HTTP.</span><span class="sxs-lookup"><span data-stu-id="9785f-198">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="9785f-199">Você pode usar o experimento **de Console de Rede** para enviar solicitações de API Web.</span><span class="sxs-lookup"><span data-stu-id="9785f-199">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="9785f-200">Depois de ativar o experimento, reinicie o DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-200">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="9785f-201">Para usar o **Console de Rede,** conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9785f-201">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="9785f-202">Abra o **painel** Rede.</span><span class="sxs-lookup"><span data-stu-id="9785f-202">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="9785f-203">Encontre a solicitação de rede que você deseja alterar e reendá-la.</span><span class="sxs-lookup"><span data-stu-id="9785f-203">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="9785f-204">Abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Editar e Repetir.**</span><span class="sxs-lookup"><span data-stu-id="9785f-204">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="9785f-205">Quando o **Console de Rede** for aberto, edite as informações de solicitação de rede.</span><span class="sxs-lookup"><span data-stu-id="9785f-205">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="9785f-206">Choose **Send**.</span><span class="sxs-lookup"><span data-stu-id="9785f-206">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Console de Rede na gaveta do Console" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="9785f-208">**Console de Rede** na gaveta **do Console**</span><span class="sxs-lookup"><span data-stu-id="9785f-208">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9785f-209">Visualizador da Ordem de Origem</span><span class="sxs-lookup"><span data-stu-id="9785f-209">Source Order Viewer</span></span>  

<span data-ttu-id="9785f-210">**O Visualizador de Ordem de** Origem é um experimento que exibe a ordem dos elementos na fonte da página da Web.</span><span class="sxs-lookup"><span data-stu-id="9785f-210">**Source Order Viewer** is an experiment that displays the order of elements in the webpage source.</span></span>  <span data-ttu-id="9785f-211">A ordem de exibição na tela pode ser diferente da ordem da origem, o que confunda os usuários do leitor de tela e do teclado.</span><span class="sxs-lookup"><span data-stu-id="9785f-211">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="9785f-212">Use o **experimento do Visualizador de Ordem** de Origem para encontrar as diferenças entre a ordem de exibição na tela e a ordem da fonte.</span><span class="sxs-lookup"><span data-stu-id="9785f-212">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="9785f-213">Depois de ativar o experimento, reinicie o DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-213">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="9785f-214">Para usar **o Visualizador de Ordem de Origem,** conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9785f-214">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="9785f-215">Abra a **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="9785f-215">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="9785f-216">Abra o **painel Acessibilidade** no painel de gaveta \(inferior\).</span><span class="sxs-lookup"><span data-stu-id="9785f-216">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="9785f-217">Na seção **Visualizador da Ordem de** Origem, escolha a caixa de seleção Mostrar Ordem de **Origem.**</span><span class="sxs-lookup"><span data-stu-id="9785f-217">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="9785f-218">Realça qualquer elemento HTML para exibir uma sobreposição à ordem na origem da página da Web.</span><span class="sxs-lookup"><span data-stu-id="9785f-218">Highlight any HTML element to display an overlay that the order in the webpage source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Visualizador da Ordem de Origem no painel Acessibilidade" lightbox="../media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="9785f-220">**Visualizador da Ordem de** Origem **no painel** Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="9785f-220">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <span data-ttu-id="9785f-221">Habilitar o editor de atalho do teclado</span><span class="sxs-lookup"><span data-stu-id="9785f-221">Enable keyboard shortcut editor</span></span>

<span data-ttu-id="9785f-222">Com o experimento de editor de **atalhos** habilitar teclado ativado, você pode personalizar atalhos de teclado para qualquer ação no DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-222">With the **Enable keyboard shortcut editor** experiment turned on, you may customize keyboard shortcuts for any action in the DevTools.</span></span>  <span data-ttu-id="9785f-223">Para personalizar o atalho do teclado para uma ação específica, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9785f-223">To customize the keyboard shortcut for a specific action, complete the following steps.</span></span>  

1.  <span data-ttu-id="9785f-224">[Abra o DevTools.][DevtoolsOpenMain]</span><span class="sxs-lookup"><span data-stu-id="9785f-224">[Open DevTools][DevtoolsOpenMain].</span></span>  
1.  <span data-ttu-id="9785f-225">Configurações [abertas.][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="9785f-225">Open [Settings][DevToolsCustomizeIndexSettings].</span></span>  
    *   <span data-ttu-id="9785f-226">Selecione `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="9785f-226">Select `Shift`+`?`.</span></span>  
1.  <span data-ttu-id="9785f-227">Navegue até a **página Atalhos.**</span><span class="sxs-lookup"><span data-stu-id="9785f-227">Navigate to the **Shortcuts** page.</span></span>  
1.  <span data-ttu-id="9785f-228">Escolha a ação que você deseja personalizar.</span><span class="sxs-lookup"><span data-stu-id="9785f-228">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="9785f-229">Escolha o **ícone** Editar \( ![ EditKeyboardShortcut ](../media/edit-keyboard-shortcut-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="9785f-229">Choose the **Edit** \(![EditKeyboardShortcut](../media/edit-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Choose the action to customize from the Shortcuts page in Settings" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       <span data-ttu-id="9785f-231">Choose the action to customize from the **Shortcuts** page in [Settings][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="9785f-231">Choose the action to customize from the **Shortcuts** page in [Settings][DevToolsCustomizeIndexSettings]</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9785f-232">No teclado, selecione as teclas para vincular à ação.</span><span class="sxs-lookup"><span data-stu-id="9785f-232">On the keyboard, select the keys to bind to the action.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Selecione as teclas a atribuir à ação" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="9785f-234">Selecione as teclas a atribuir à ação</span><span class="sxs-lookup"><span data-stu-id="9785f-234">Select the keys to assign to the action</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9785f-235">Para salvar o novo atalho de teclado, escolha a marca de seleção \(</span><span class="sxs-lookup"><span data-stu-id="9785f-235">To save your new keyboard shortcut, choose the checkmark \(</span></span>![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)<span data-ttu-id="9785f-237">\) ícone.</span><span class="sxs-lookup"><span data-stu-id="9785f-237">\) icon.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Escolha o ícone de marca de seleção para salvar o novo atalho de teclado" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="9785f-239">Escolha o ícone de marca de seleção para salvar o novo atalho de teclado</span><span class="sxs-lookup"><span data-stu-id="9785f-239">Choose the checkmark icon to save your new keyboard shortcut</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9785f-240">Selecione seu novo atalho de teclado para disparar a ação no DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-240">Select your new keyboard shortcut to trigger the action in the DevTools.</span></span>  
    
<span data-ttu-id="9785f-241">Na página **Atalhos,** o ícone Atalho de Teclado **Personalizado** \( ![ CustomKeyboardShortcut \) exibe ](../media/custom-keyboard-shortcut-icon.msft.png) atalhos de teclado personalizados.</span><span class="sxs-lookup"><span data-stu-id="9785f-241">On the **Shortcuts** page, the **Custom Keyboard Shortcut** \(![CustomKeyboardShortcut](../media/custom-keyboard-shortcut-icon.msft.png)\) icon displays keyboard shortcuts you customized.</span></span>  <span data-ttu-id="9785f-242">Para redefinir todos os atalhos, escolha **Restaurar atalhos padrão.**</span><span class="sxs-lookup"><span data-stu-id="9785f-242">To reset all shortcuts, choose **Restore default shortcuts**.</span></span>  

<span data-ttu-id="9785f-243">Para descartar suas alterações enquanto edita os atalhos de teclado para uma ação, escolha o ícone X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="9785f-243">To discard your changes while you edit the keyboard shortcuts for an action, choose the X \(![XKeyboardShortcut](../media/discard-changes-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="9785f-244">Para remover atalhos de uma ação específica, escolha o ícone Excluir atalho **\(** ![ DeleteKeyboardShortcut ](../media/delete-keyboard-shortcut-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="9785f-244">To remove shortcuts for a specific action, choose the **Delete shortcut** \(![DeleteKeyboardShortcut](../media/delete-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="9785f-245">Para adicionar vários atalhos para uma ação, escolha **Adicionar um atalho.**</span><span class="sxs-lookup"><span data-stu-id="9785f-245">To add multiple shortcuts for an action, choose **Add a shortcut**.</span></span>  

> [!NOTE]
> <span data-ttu-id="9785f-246">Se um atalho de teclado estiver atribuído a outra ação no momento, talvez você não o salve para uma nova ação.</span><span class="sxs-lookup"><span data-stu-id="9785f-246">If a keyboard shortcut is currently assigned to another action, you may not save it for a new action.</span></span>  <span data-ttu-id="9785f-247">Primeiro você deve excluir o atalho do teclado para a ação anterior e, em seguida, adicioná-lo à nova ação.</span><span class="sxs-lookup"><span data-stu-id="9785f-247">You must first delete the keyboard shortcut for the previous action and then add it to the new action.</span></span>  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <span data-ttu-id="9785f-248">Habilitar camadas compostas no modo de exibição 3D</span><span class="sxs-lookup"><span data-stu-id="9785f-248">Enable Composited Layers in 3D View</span></span>  

<span data-ttu-id="9785f-249">Agora você pode visualizar Camadas junto com índices z e o Modelo de Objeto do Documento \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="9785f-249">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="9785f-250">Esse recurso ajuda você a depurar sem alternar contextos com a mesma frequência.</span><span class="sxs-lookup"><span data-stu-id="9785f-250">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="9785f-251">Você identificou que a redução da alternação de contexto era um ponto de problema importante.</span><span class="sxs-lookup"><span data-stu-id="9785f-251">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="9785f-252">Nem sempre é claro como o código que você escreve afeta seu aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="9785f-252">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="9785f-253">Para uma experiência de depuração visual abrangente, o Modo de exibição 3D e as camadas compostas agora são combinados.</span><span class="sxs-lookup"><span data-stu-id="9785f-253">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  

<span data-ttu-id="9785f-254">Depois de ativar o experimento, reinicie o DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-254">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="9785f-255">Para usar **camadas compostas,** conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9785f-255">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="9785f-256">Na gaveta, escolha a ferramenta **Exibição 3D.**</span><span class="sxs-lookup"><span data-stu-id="9785f-256">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="9785f-257">Abra o **painel Camadas Compostas.**</span><span class="sxs-lookup"><span data-stu-id="9785f-257">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="9785f-258">Todas as camadas pintadas do aplicativo são exibidas.</span><span class="sxs-lookup"><span data-stu-id="9785f-258">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="9785f-259">Experimente esse recurso com seus próprios aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="9785f-259">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Painel de Camadas compostas" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="9785f-261">Painel de **Camadas Compostas**</span><span class="sxs-lookup"><span data-stu-id="9785f-261">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <span data-ttu-id="9785f-262">Habilitar a nova ferramenta Editor de Fontes no painel Estilos</span><span class="sxs-lookup"><span data-stu-id="9785f-262">Enable new Font Editor tool within the Styles pane</span></span>  

<span data-ttu-id="9785f-263">Agora você pode usar o novo Editor de [Fonte visual][DevtoolsInspectStylesEditFonts] para editar fontes.</span><span class="sxs-lookup"><span data-stu-id="9785f-263">You may now use the new visual [Font Editor][DevtoolsInspectStylesEditFonts] to edit fonts.</span></span>  <span data-ttu-id="9785f-264">Use-o para definir fontes e características de fonte.</span><span class="sxs-lookup"><span data-stu-id="9785f-264">Use it define fonts and font characteristics.</span></span>  <span data-ttu-id="9785f-265">O **Editor de Fonte visual** ajuda você a concluir as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="9785f-265">The visual **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="9785f-266">Alternar entre unidades para propriedades de fonte diferentes</span><span class="sxs-lookup"><span data-stu-id="9785f-266">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="9785f-267">Alternar entre palavras-chave para propriedades de fonte diferentes</span><span class="sxs-lookup"><span data-stu-id="9785f-267">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="9785f-268">Converter unidades</span><span class="sxs-lookup"><span data-stu-id="9785f-268">Convert units</span></span>  
*   <span data-ttu-id="9785f-269">Gerar código CSS preciso</span><span class="sxs-lookup"><span data-stu-id="9785f-269">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="9785f-270">Depois de ativar o experimento, reinicie o DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-270">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="9785f-271">Para usar o novo Editor de **Fontes visual,** conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9785f-271">To use the new visual **Font Editor**, complete the following steps.</span></span>  

1.  <span data-ttu-id="9785f-272">Abra a **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="9785f-272">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="9785f-273">Abra o **painel** Estilos.</span><span class="sxs-lookup"><span data-stu-id="9785f-273">Open the **Styles** pane.</span></span>  
1.  <span data-ttu-id="9785f-274">Escolha o **ícone do Editor de** Fontes.</span><span class="sxs-lookup"><span data-stu-id="9785f-274">Choose the **Font Editor** icon.</span></span>  
    
<span data-ttu-id="9785f-275">For more information about the new visual **Font Editor**, navigate to Edit CSS font styles [and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="9785f-275">For more information about the new visual **Font Editor**, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="O painel editor de fonte visual está realçada" lightbox="../media/font-editor-open.msft.png":::
   <span data-ttu-id="9785f-277">O painel **editor de** fonte visual está realçada</span><span class="sxs-lookup"><span data-stu-id="9785f-277">The visual **Font Editor** pane is highlighted</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <span data-ttu-id="9785f-278">Habilitar novos recursos de depuração do CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="9785f-278">Enable new CSS Flexbox debugging features</span></span>  

<span data-ttu-id="9785f-279">Esse recurso experimental fornece muitas visualizações novas para ajudá-lo a depurar layouts do CSS Flexbox.</span><span class="sxs-lookup"><span data-stu-id="9785f-279">This experimental feature provides many new visualizations to help you debug CSS Flexbox layouts.</span></span>  <span data-ttu-id="9785f-280">Para visualizar os recursos experimentais mais recentes, [a ligue esse experimento](#turn-on-experimental-features) e recarregue o DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-280">To preview the latest experimental features, [turn on this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  

#### <span data-ttu-id="9785f-281">Exibir sobreposições persistentes em layouts do Flexbox com a ferramenta Inspect</span><span class="sxs-lookup"><span data-stu-id="9785f-281">Display persistent overlays on Flexbox layouts with the Inspect tool</span></span>  

<span data-ttu-id="9785f-282">A **ferramenta Inspect** fornece uma maneira rápida de identificar e visualizar layouts do CSS Flexbox em um site, passe o mouse sobre eles.</span><span class="sxs-lookup"><span data-stu-id="9785f-282">The **Inspect** tool provides a quick way to identify and visualize CSS Flexbox layouts in a website by hovering on them with the mouse.</span></span>  <span data-ttu-id="9785f-283">Escolha o **ícone Inspecionar** \( ![ Inspecionar ](../media/inspect-icon.msft.png) \) no canto superior esquerdo do DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-283">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="9785f-284">Em seguida, durante a depuração do site, passe o mouse sobre um contêiner flexível para exibir contornos ao redor do contêiner flexível.</span><span class="sxs-lookup"><span data-stu-id="9785f-284">Then, while debugging the website, hover on a flex container to display outlines around the flex container.</span></span>  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Exibir contêineres do Flexbox com a ferramenta Inspect" lightbox="../media/flexbox-hover.msft.png":::
   <span data-ttu-id="9785f-286">Exibir contêineres do Flexbox com a **ferramenta Inspect**</span><span class="sxs-lookup"><span data-stu-id="9785f-286">Display Flexbox containers with the **Inspect** tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="9785f-287">Exibir sobreposições persistentes em layouts do Flexbox</span><span class="sxs-lookup"><span data-stu-id="9785f-287">Display persistent overlays on Flexbox layouts</span></span>  

<span data-ttu-id="9785f-288">No Microsoft Edge versão 89 ou posterior, o recurso experimental Css Flexbox também oferece a opção de ativar sobreposições persistentes em layouts do Flexbox.</span><span class="sxs-lookup"><span data-stu-id="9785f-288">In Microsoft Edge version 89 or later, the experimental CSS Flexbox feature also offers the option to turn on persistent overlays on Flexbox layouts.</span></span>  <span data-ttu-id="9785f-289">As sobreposições persistentes oferecem os seguintes benefícios.</span><span class="sxs-lookup"><span data-stu-id="9785f-289">Persistent overlays provide the following benefits.</span></span>  

*   <span data-ttu-id="9785f-290">As sobreposições persistentes permanecem visíveis na página da Web à medida que você rola, move o mouse e usa outros recursos do DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-290">Persistent overlays remain visible on the webpage as you scroll, move your mouse, and use other features of the DevTools.</span></span>
*   <span data-ttu-id="9785f-291">Várias sobreposições persistentes podem ser usadas ao mesmo tempo, para permitir que você revise vários layouts do Flexbox ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="9785f-291">Multiple persistent overlays may be used at the same time, to allow you to review several Flexbox layouts at once.</span></span>  
*   <span data-ttu-id="9785f-292">Sobreposições persistentes oferecem opções de configuração de cor.</span><span class="sxs-lookup"><span data-stu-id="9785f-292">Persistent overlays offer color configuration options.</span></span>  
    
<span data-ttu-id="9785f-293">Para alternar sobreposições persistentes no layout do Flexbox, use uma das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="9785f-293">To toggle persistent overlays on Flexbox layout, use one of following actions.</span></span>  

*   <span data-ttu-id="9785f-294">Escolha o ícone de oval **Flexbox** ao lado de qualquer contêiner flexbox exibido na árvore DOM da **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="9785f-294">Choose the **Flexbox** oval icon next to any Flexbox container displayed in the DOM tree of the **Elements** tool.</span></span>  
*   <span data-ttu-id="9785f-295">Abra o novo **painel layout** localizado na ferramenta **Elementos** e escolha a caixa de seleção ao lado de cada contêiner do Flexbox que você deseja realçar.</span><span class="sxs-lookup"><span data-stu-id="9785f-295">Open the new **Layout** panel located in the **Elements** tool, and choose the checkbox next to each Flexbox container you want to highlight.</span></span>  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Ícones flexíveis e painel layout no DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   <span data-ttu-id="9785f-297">Ícones flexíveis e **painel layout** no DevTools</span><span class="sxs-lookup"><span data-stu-id="9785f-297">Flex icons and **Layout** panel in DevTools</span></span>  
:::image-end:::  

#### <span data-ttu-id="9785f-298">Configurar sobreposições persistentes</span><span class="sxs-lookup"><span data-stu-id="9785f-298">Configure persistent overlays</span></span>  

<span data-ttu-id="9785f-299">Para configurar opções para sobreposições persistentes para grades CSS ou layouts do Flexbox, use o **painel** Layout.</span><span class="sxs-lookup"><span data-stu-id="9785f-299">To configure options for persistent overlays for CSS grids or Flexbox layouts, use the **Layout** pane.</span></span>  <span data-ttu-id="9785f-300">O **painel Layout** está localizado na ferramenta **Elementos** ao lado dos painéis **Estilos** **e** Calculados.</span><span class="sxs-lookup"><span data-stu-id="9785f-300">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span></span>  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Painel de layout" lightbox="../media/flexbox-layout.msft.png":::
   <span data-ttu-id="9785f-302">Painel de layout</span><span class="sxs-lookup"><span data-stu-id="9785f-302">Layout panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <span data-ttu-id="9785f-303">Habilitar + menus de guia de botão para abrir mais ferramentas</span><span class="sxs-lookup"><span data-stu-id="9785f-303">Enable + button tab menus to open more tools</span></span>  

<span data-ttu-id="9785f-304">Agora você pode abrir mais ferramentas usando o novo ícone Mais **Ferramentas** \( `+` \).</span><span class="sxs-lookup"><span data-stu-id="9785f-304">You may now open more tools using the new **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="9785f-305">Depois de ativar os **menus** da guia do botão Habilitar + para abrir mais ferramentas experimentar e recarregar o DevTools, um sinal de mais \( \) é exibido à direita do grupo de guias na parte superior do `+` DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-305">After you turn on the **Enable + button tab menus to open more tools** experiment and reload DevTools, a plus sign \(`+`\) displays to the right of the tab group at the top of the DevTools.</span></span>  <span data-ttu-id="9785f-306">Para exibir uma lista de outras ferramentas que você pode adicionar à barra de guias, escolha o novo ícone Mais **Ferramentas** \( `+` \).</span><span class="sxs-lookup"><span data-stu-id="9785f-306">To display a list of other tools that you may add to the tab bar, choose the new **More Tools** \(`+`\) icon.</span></span>  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Mais Ferramentas no painel superior" lightbox="../media/experiments-more-tools-button.msft.png":::
   <span data-ttu-id="9785f-308">**Mais Ferramentas** no painel superior</span><span class="sxs-lookup"><span data-stu-id="9785f-308">**More Tools** in the top pane</span></span>
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <span data-ttu-id="9785f-309">Habilitar a ferramenta de boas-vindas</span><span class="sxs-lookup"><span data-stu-id="9785f-309">Enable Welcome tool</span></span>

<span data-ttu-id="9785f-310">Esse experimento substitui a **ferramenta Novidades pela** nova ferramenta de **boas-vindas.**</span><span class="sxs-lookup"><span data-stu-id="9785f-310">This experiment replaces the **What's New** tool with the new **Welcome** tool.</span></span>  <span data-ttu-id="9785f-311">Ele exibe um design atualizado para o conteúdo a seguir.</span><span class="sxs-lookup"><span data-stu-id="9785f-311">It displays a refreshed design for the following content.</span></span>  

*   <span data-ttu-id="9785f-312">Links para documentos de desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="9785f-312">Links to developer docs</span></span>  
*   <span data-ttu-id="9785f-313">os recursos mais recentes</span><span class="sxs-lookup"><span data-stu-id="9785f-313">the latest features</span></span>  
*   <span data-ttu-id="9785f-314">notas de versão</span><span class="sxs-lookup"><span data-stu-id="9785f-314">release notes</span></span>  
*   <span data-ttu-id="9785f-315">Opção para entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9785f-315">Option to contact the Microsoft Edge DevTools team</span></span>  
    
<span data-ttu-id="9785f-316">A **ferramenta de boas-vindas** é aberta automaticamente após cada atualização do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9785f-316">The **Welcome** tool opens automatically after each update to Microsoft Edge.</span></span>  <span data-ttu-id="9785f-317">Para impedir a exibição da ferramenta **de** boas-vindas \*\*\*\* após cada atualização, des marque a caixa de seleção ao lado da guia Abrir após cada atualização sob o título da ferramenta **de** boas-vindas.</span><span class="sxs-lookup"><span data-stu-id="9785f-317">To prevent the display of the **Welcome** tool after each update, clear the checkbox next to **Open tab after each update** under the **Welcome** tool title.</span></span>  

<span data-ttu-id="9785f-318">Se você preferir a ferramenta **Novidades** original, navegue até [Experimentos][DevtoolsCustomizeIndexSettings]de Configurações e remova a caixa de seleção ao lado da guia  >  \*\*\*\* **Habilitar Boas-vindas.**</span><span class="sxs-lookup"><span data-stu-id="9785f-318">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Ferramenta de boas-vindas" lightbox="../media/experiments-welcome.msft.png":::
   <span data-ttu-id="9785f-320">**Ferramenta de boas-vindas**</span><span class="sxs-lookup"><span data-stu-id="9785f-320">**Welcome** tool</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <span data-ttu-id="9785f-321">Recursos experimentais anteriores</span><span class="sxs-lookup"><span data-stu-id="9785f-321">Previous experimental features</span></span>  

*   <span data-ttu-id="9785f-322">[O Modo de Exibição 3D][Devtools3dViewIndex] agora está disponível e ligado por padrão no Microsoft Edge versão 83 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9785f-322">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="9785f-323">[Ativar o suporte para mover guias][DevtoolsMoveTabs] entre painéis agora está disponível e ligado por padrão no Microsoft Edge versão 85 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9785f-323">[Turn on support to move tabs between panels][DevtoolsMoveTabs] is now available and turned on by default in Microsoft Edge version 85 or later.</span></span>  
*   <span data-ttu-id="9785f-324">[Personalizar atalhos de][DevtoolsCustomKeyboardShortcuts] teclado agora está disponível e ligado por padrão no Microsoft Edge versão 86 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9785f-324">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  
*   <span data-ttu-id="9785f-325">[Emulação: o modo de tela][DevtoolsDeviceModeDualScreenAndFoldables] dupla de suporte agora está disponível e ligado por padrão no Microsoft Edge versão 89 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9785f-325">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="9785f-326">[Ativar novos recursos de depuração][DevtoolsCssGrid] de grade CSS agora está disponível e ligado por padrão no Microsoft Edge versão 89 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9785f-326">[Turn on new CSS grid debugging features][DevtoolsCssGrid] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
    
## <span data-ttu-id="9785f-327">Fornecer comentários sobre recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="9785f-327">Providing feedback on experimental features</span></span>  

<span data-ttu-id="9785f-328">Para fornecer comentários sobre experimentos do Microsoft Edge DevTools ou qualquer outra coisa relacionada ao DevTools.</span><span class="sxs-lookup"><span data-stu-id="9785f-328">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="9785f-329">Envie seus comentários usando o **ícone Enviar Comentários** no DevTools</span><span class="sxs-lookup"><span data-stu-id="9785f-329">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="9785f-330">Tweet à [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="9785f-330">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="O ícone Enviar Comentários no Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="9785f-332">O **ícone Enviar Comentários** no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9785f-332">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Modo de exibição 3D | Microsoft Docs"  
[DevtoolsCssGrid]: ../css/grid.md "Inspecionar grade CSS no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsMoveTabs]: ../customize/index.md "Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Editar estilos e configurações de fonte CSS no painel Estilos no DevTools | Microsoft Docs"  
[DevtoolsIssues]: ../issues/index.md "Localizar e corrigir problemas com a ferramenta Issues do DevTools do Microsoft Edge | Microsoft Docs"  
[DevToolsShortcuts]: ../shortcuts/index.md "Atalhos de teclado do Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Personalizar atalhos de teclado no microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsOpenMain]: ../open/index.md "Abra o Microsoft Edge DevTools | Microsoft Docs"  

[DualScreenWebIndex]: /dual-screen/web/index "Experiências da Web de tela dupla | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obter o emulador surface Duo | Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Como trabalhar com a sam - Introdução a dispositivos de tela dupla | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Usar o emulador Surface Duo | Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Recurso de abrangeção de tela de mídia CSS para detecção de tela dupla | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "A API JavaScript getWindowSegments para dispositivos de tela dupla | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clientes de Área de Trabalho Remota | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "| Samsung"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emular dispositivos de tela dupla e dobrável no Microsoft Edge DevTools | Microsoft Docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
