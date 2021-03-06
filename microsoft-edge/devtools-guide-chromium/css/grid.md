---
description: Saiba como usar o Microsoft Edge DevTools para exibir e alterar o CSS de uma página CSS.
title: Inspecionar Grade CSS no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 5e4b20690eac3a692f6428f391def102a4f78ecb
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398767"
---
# <a name="inspect-css-grid"></a><span data-ttu-id="9056c-104">Inspecionar Grade CSS</span><span class="sxs-lookup"><span data-stu-id="9056c-104">Inspect CSS Grid</span></span>  

<span data-ttu-id="9056c-105">Este artigo orienta você a identificar grades CSS em um site e depurar problemas de layout de grade usando sobreposições de grade personalizáveis.</span><span class="sxs-lookup"><span data-stu-id="9056c-105">This article walks you through identifying CSS grids on a website and debugging grid layout issues using customizable grid overlays.</span></span>  

<span data-ttu-id="9056c-106">Os exemplos usados nos números deste artigo são tirados das páginas da Web a seguir.</span><span class="sxs-lookup"><span data-stu-id="9056c-106">The examples used in the figures in this article are taken from the following webpages.</span></span>  

*   [<span data-ttu-id="9056c-107">Caixa de frutas</span><span class="sxs-lookup"><span data-stu-id="9056c-107">Fruit box</span></span>][JecFyiDemoCssGridFruit]  
*   [<span data-ttu-id="9056c-108">Caixa de lanchinho</span><span class="sxs-lookup"><span data-stu-id="9056c-108">Snack box</span></span>][JecFyiDemoCssGridSnack]  

## <a name="before-you-begin"></a><span data-ttu-id="9056c-109">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="9056c-109">Before you begin</span></span>  

<span data-ttu-id="9056c-110">CSS Grid é um paradigma de layout poderoso para a Web.</span><span class="sxs-lookup"><span data-stu-id="9056c-110">CSS Grid is a powerful layout paradigm for the web.</span></span>  <span data-ttu-id="9056c-111">Um ótimo lugar para começar a aprender sobre CSS Grid e os muitos recursos é o [guia layout de grade css][MdnCssGridLayout] no MDN.</span><span class="sxs-lookup"><span data-stu-id="9056c-111">A great place to get started learning about CSS Grid and the many features is the [CSS Grid Layout guide][MdnCssGridLayout] on MDN.</span></span>  

## <a name="discover-css-grids"></a><span data-ttu-id="9056c-112">Descobrir grades CSS</span><span class="sxs-lookup"><span data-stu-id="9056c-112">Discover CSS grids</span></span>  

<span data-ttu-id="9056c-113">Quando um elemento HTML em sua página tem ou aplicado a ele, um selo é exibido ao lado dele `display: grid` `display: inline-grid` no painel `grid` [Elementos.][DevtoolsGuideChromiumOpen]</span><span class="sxs-lookup"><span data-stu-id="9056c-113">When an HTML element on your page has `display: grid` or `display: inline-grid` applied to it, a `grid` badge is displayed next to it in the [Elements][DevtoolsGuideChromiumOpen] panel.</span></span>  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Descobrir grade" lightbox="../media/grid-discover-grid.msft.png":::
   <span data-ttu-id="9056c-115">Descobrir grade</span><span class="sxs-lookup"><span data-stu-id="9056c-115">Discover grid</span></span>  
:::image-end:::  

<span data-ttu-id="9056c-116">Escolha o selo para alternar a exibição de uma sobreposição de grade na página.</span><span class="sxs-lookup"><span data-stu-id="9056c-116">Choose the badge to toggle the display of a grid overlay on the page.</span></span>  <span data-ttu-id="9056c-117">A sobreposição aparece sobre o elemento, definida como uma grade para exibir a posição das linhas e faixas de grade:</span><span class="sxs-lookup"><span data-stu-id="9056c-117">The overlay appears over the element, laid out like a grid to display the position of the grid lines and tracks:</span></span>  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Selo de grade de alternância" lightbox="../media/grid-highlight-grid.msft.png":::
   <span data-ttu-id="9056c-119">Selo de grade de alternância</span><span class="sxs-lookup"><span data-stu-id="9056c-119">Toggle grid badge</span></span>  
:::image-end:::  

<span data-ttu-id="9056c-120">Abra o **painel Layout.**</span><span class="sxs-lookup"><span data-stu-id="9056c-120">Open the **Layout** pane.</span></span>  <span data-ttu-id="9056c-121">Quando as grades são incluídas em uma página, o **painel Layout** inclui uma seção **Grid** contendo várias opções para exibir as grades.</span><span class="sxs-lookup"><span data-stu-id="9056c-121">When grids are included on a page, the **Layout** pane includes a **Grid** section containing a number of options for viewing the grids.</span></span>  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Painel de layout" lightbox="../media/grid-layout-pane.msft.png":::
   <span data-ttu-id="9056c-123">**Painel** de layout</span><span class="sxs-lookup"><span data-stu-id="9056c-123">**Layout** pane</span></span>  
:::image-end:::  

<span data-ttu-id="9056c-124">A **seção Grade** no painel **Layout** contém as duas subseções a seguir.</span><span class="sxs-lookup"><span data-stu-id="9056c-124">The **Grid** section in the **Layout** pane contains the following 2 sub-sections.</span></span>  

*   <span data-ttu-id="9056c-125">Configurações de exibição de sobreposição</span><span class="sxs-lookup"><span data-stu-id="9056c-125">Overlay display settings</span></span>  
*   <span data-ttu-id="9056c-126">Sobreposições de grade</span><span class="sxs-lookup"><span data-stu-id="9056c-126">Grid overlays</span></span>  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## <a name="overlay-display-settings"></a><span data-ttu-id="9056c-127">Configurações de exibição de sobreposição</span><span class="sxs-lookup"><span data-stu-id="9056c-127">Overlay display settings</span></span>  

<span data-ttu-id="9056c-128">As **configurações de exibição sobreposição** consistem em duas partes a seguir.</span><span class="sxs-lookup"><span data-stu-id="9056c-128">The **Overlay display settings** consists of following 2 parts.</span></span>  

*   <span data-ttu-id="9056c-129">Escolha uma das opções a seguir no menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="9056c-129">Choose one of the following options from the dropdown menu.</span></span>  
    
    | <span data-ttu-id="9056c-130">Opção De linha</span><span class="sxs-lookup"><span data-stu-id="9056c-130">Line option</span></span> | <span data-ttu-id="9056c-131">Detalhes</span><span class="sxs-lookup"><span data-stu-id="9056c-131">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="9056c-132">Ocultar rótulos de linha</span><span class="sxs-lookup"><span data-stu-id="9056c-132">Hide line labels</span></span>** | <span data-ttu-id="9056c-133">Ocultar os rótulos das linhas para cada sobreposição de grade.</span><span class="sxs-lookup"><span data-stu-id="9056c-133">Hide the labels of the lines for each grid overlay.</span></span> |  
    | **<span data-ttu-id="9056c-134">Mostrar números de linha</span><span class="sxs-lookup"><span data-stu-id="9056c-134">Show line numbers</span></span>** | <span data-ttu-id="9056c-135">Exibir os números das linhas para cada sobreposição de grade \(selecionado por padrão\).</span><span class="sxs-lookup"><span data-stu-id="9056c-135">Display the numbers of the lines for each grid overlay \(selected by default\).</span></span> |  
    | **<span data-ttu-id="9056c-136">Mostrar nomes de linha</span><span class="sxs-lookup"><span data-stu-id="9056c-136">Show line names</span></span>** | <span data-ttu-id="9056c-137">Exibe os nomes das linhas para cada sobreposição de grade quando os nomes são fornecidos.</span><span class="sxs-lookup"><span data-stu-id="9056c-137">Display the names of the lines for each grid overlay when names are provided.</span></span> |  
    
*  <span data-ttu-id="9056c-138">Escolha a caixa de seleção ao lado das seguintes opções.</span><span class="sxs-lookup"><span data-stu-id="9056c-138">Choose the checkbox next the following options.</span></span>  
    
    | <span data-ttu-id="9056c-139">Opção</span><span class="sxs-lookup"><span data-stu-id="9056c-139">Option</span></span> | <span data-ttu-id="9056c-140">Detalhes</span><span class="sxs-lookup"><span data-stu-id="9056c-140">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="9056c-141">Mostrar tamanhos de faixa</span><span class="sxs-lookup"><span data-stu-id="9056c-141">Show track sizes</span></span>**  | <span data-ttu-id="9056c-142">Exibe \(ou ocultar\) os tamanhos das faixas.</span><span class="sxs-lookup"><span data-stu-id="9056c-142">Display \(or hide\) the sizes of the tracks.</span></span> |  
    | **<span data-ttu-id="9056c-143">Mostrar nomes de área</span><span class="sxs-lookup"><span data-stu-id="9056c-143">Show area names</span></span>** | <span data-ttu-id="9056c-144">Exibir \(ou ocultar\) os nomes da área, quando os nomes são fornecidos.</span><span class="sxs-lookup"><span data-stu-id="9056c-144">Display \(or hide\) the names of the area, when names are provided.</span></span> |  
    | **<span data-ttu-id="9056c-145">Estender linhas de grade</span><span class="sxs-lookup"><span data-stu-id="9056c-145">Extend grid lines</span></span>** | <span data-ttu-id="9056c-146">Exibe \(ou oculta\) as extensões das dimensões de grade ao longo de cada eixo.</span><span class="sxs-lookup"><span data-stu-id="9056c-146">Displays \(or hides\) the extensions of the grid dimensions along each axis.</span></span>  <span data-ttu-id="9056c-147">Por padrão, as linhas de grade só são mostradas dentro do elemento com `display: grid` ou `display: inline-grid` css definido nele.</span><span class="sxs-lookup"><span data-stu-id="9056c-147">By default, grid lines are only shown inside the element with `display: grid` or `display: inline-grid` CSS set on it.</span></span> |  
    
<span data-ttu-id="9056c-148">As seções a seguir fornecem detalhes para cada uma das configurações de **exibição sobreposição.**</span><span class="sxs-lookup"><span data-stu-id="9056c-148">The following sections provide details for each of the **Overlay display settings**.</span></span>  

### <a name="show-line-numbers"></a><span data-ttu-id="9056c-149">Mostrar números de linha</span><span class="sxs-lookup"><span data-stu-id="9056c-149">Show line numbers</span></span>  

<span data-ttu-id="9056c-150">Por padrão, os números de linha positivos e negativos são exibidos na sobreposição de grade.</span><span class="sxs-lookup"><span data-stu-id="9056c-150">By default, the positive and negative line numbers are displayed on the grid overlay.</span></span>  

<span data-ttu-id="9056c-151">Para obter mais informações sobre números negativos na sobreposição de grade, navegue até [Posicionamento baseado em linha com CSS Grid][MdnLineBasedPlacementCssGrid].</span><span class="sxs-lookup"><span data-stu-id="9056c-151">For more information about negative numbers in the grid overlay, navigate to [Line-based placement with CSS Grid][MdnLineBasedPlacementCssGrid].</span></span>  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Exibir números de linha" lightbox="../media/grid-show-line-numbers.msft.png":::
   <span data-ttu-id="9056c-153">Exibir números de linha</span><span class="sxs-lookup"><span data-stu-id="9056c-153">Display line numbers</span></span>  
:::image-end:::  

### <a name="hide-line-labels"></a><span data-ttu-id="9056c-154">Ocultar rótulos de linha</span><span class="sxs-lookup"><span data-stu-id="9056c-154">Hide line labels</span></span>  

<span data-ttu-id="9056c-155">Escolha **Ocultar rótulos de linha** para ocultar os números de linha.</span><span class="sxs-lookup"><span data-stu-id="9056c-155">Choose **Hide line labels** to hide the line numbers.</span></span>  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Ocultar rótulos de linha" lightbox="../media/grid-hide-line-labels.msft.png":::
   <span data-ttu-id="9056c-157">Ocultar rótulos de linha</span><span class="sxs-lookup"><span data-stu-id="9056c-157">Hide line labels</span></span>  
:::image-end:::  

### <a name="show-line-names"></a><span data-ttu-id="9056c-158">Mostrar nomes de linha</span><span class="sxs-lookup"><span data-stu-id="9056c-158">Show line names</span></span>  

<span data-ttu-id="9056c-159">Para obter mais informações sobre nomes de linha na sobreposição de grade, navegue até [Layout usando linhas de grade nomeadas][MdnLayoutUsingNamedGridLines].</span><span class="sxs-lookup"><span data-stu-id="9056c-159">For more information about line names in the grid overlay, navigate to [Layout using named grid lines][MdnLayoutUsingNamedGridLines].</span></span>  

<span data-ttu-id="9056c-160">Escolha **Mostrar nomes de linha** para exibir os nomes de linha em vez de números.</span><span class="sxs-lookup"><span data-stu-id="9056c-160">Choose **Show line names** to view the line names instead of numbers.</span></span>  <span data-ttu-id="9056c-161">No exemplo, 4 linhas têm nomes: `left` , `middle1` , e `middle2` `right` .</span><span class="sxs-lookup"><span data-stu-id="9056c-161">In the example, 4 lines have names: `left`, `middle1`, `middle2`, and `right`.</span></span>  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Mostrar nomes de linha" lightbox="../media/grid-show-line-names.msft.png":::
   **<span data-ttu-id="9056c-163">Mostrar nomes de linha</span><span class="sxs-lookup"><span data-stu-id="9056c-163">Show line names</span></span>**  
:::image-end:::  

### <a name="show-track-sizes"></a><span data-ttu-id="9056c-164">Mostrar tamanhos de faixa</span><span class="sxs-lookup"><span data-stu-id="9056c-164">Show track sizes</span></span>  

<span data-ttu-id="9056c-165">Habilita a caixa de seleção Mostrar **tamanhos** de faixa para exibir os tamanhos de faixa da grade.</span><span class="sxs-lookup"><span data-stu-id="9056c-165">Enable the **Show track sizes** checkbox to view the track sizes of the grid.</span></span>  

<span data-ttu-id="9056c-166">DevTools exibe `[authored size]` e em cada rótulo de `[computed size]` linha.</span><span class="sxs-lookup"><span data-stu-id="9056c-166">DevTools displays `[authored size]` and `[computed size]` in each line label.</span></span>  

| <span data-ttu-id="9056c-167">Size</span><span class="sxs-lookup"><span data-stu-id="9056c-167">Size</span></span> | <span data-ttu-id="9056c-168">Detalhes</span><span class="sxs-lookup"><span data-stu-id="9056c-168">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="9056c-169">tamanho de autoria</span><span class="sxs-lookup"><span data-stu-id="9056c-169">authored size</span></span>** | <span data-ttu-id="9056c-170">O tamanho definido na folha de estilos \(omitido se não definido\).</span><span class="sxs-lookup"><span data-stu-id="9056c-170">The size defined in stylesheet \(omitted if not defined\).</span></span> |  
| **<span data-ttu-id="9056c-171">tamanho calculado</span><span class="sxs-lookup"><span data-stu-id="9056c-171">computed size</span></span>** | <span data-ttu-id="9056c-172">O tamanho real na tela.</span><span class="sxs-lookup"><span data-stu-id="9056c-172">The actual size on screen.</span></span> |  

<span data-ttu-id="9056c-173">Na demonstração, os `snack-box` tamanhos das colunas são definidos no `grid-template-columns:1fr 2fr;` CSS.</span><span class="sxs-lookup"><span data-stu-id="9056c-173">In the demo, the `snack-box` column sizes are defined in the `grid-template-columns:1fr 2fr;` CSS.</span></span>  <span data-ttu-id="9056c-174">Portanto, os rótulos de linha de coluna exibem tamanhos de autoria e computação.</span><span class="sxs-lookup"><span data-stu-id="9056c-174">Therefore, the column line labels display both authored and computed sizes.</span></span>  

| <span data-ttu-id="9056c-175">Tamanho da faixa</span><span class="sxs-lookup"><span data-stu-id="9056c-175">Track size</span></span> | <span data-ttu-id="9056c-176">Tamanho de autoria</span><span class="sxs-lookup"><span data-stu-id="9056c-176">Authored size</span></span> | <span data-ttu-id="9056c-177">Tamanho calculado</span><span class="sxs-lookup"><span data-stu-id="9056c-177">Computed size</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="9056c-178">**1fr** &#x2022; **96,66px**</span><span class="sxs-lookup"><span data-stu-id="9056c-178">**1fr** &#x2022; **96.66px**</span></span> | <span data-ttu-id="9056c-179">1fr</span><span class="sxs-lookup"><span data-stu-id="9056c-179">1fr</span></span> | <span data-ttu-id="9056c-180">96,66px</span><span class="sxs-lookup"><span data-stu-id="9056c-180">96.66px</span></span> |  
| <span data-ttu-id="9056c-181">**2fr** &#x2022; **193,32px**</span><span class="sxs-lookup"><span data-stu-id="9056c-181">**2fr** &#x2022; **193.32px**</span></span> | <span data-ttu-id="9056c-182">2fr</span><span class="sxs-lookup"><span data-stu-id="9056c-182">2fr</span></span> | <span data-ttu-id="9056c-183">193,32px</span><span class="sxs-lookup"><span data-stu-id="9056c-183">193.32px</span></span> |  

<span data-ttu-id="9056c-184">Os rótulos de linha de linha exibem apenas tamanhos calculados, já que não há tamanhos de linha definidos na folha de estilos.</span><span class="sxs-lookup"><span data-stu-id="9056c-184">The row line labels display only computed sizes, since there are no row sizes defined in the stylesheet.</span></span>  

| <span data-ttu-id="9056c-185">Tamanho da faixa</span><span class="sxs-lookup"><span data-stu-id="9056c-185">Track size</span></span> | <span data-ttu-id="9056c-186">Tamanho de autoria</span><span class="sxs-lookup"><span data-stu-id="9056c-186">Authored size</span></span> | <span data-ttu-id="9056c-187">Tamanho calculado</span><span class="sxs-lookup"><span data-stu-id="9056c-187">Computed size</span></span> |  
|:--- |:--- |:--- |  
| **<span data-ttu-id="9056c-188">80px</span><span class="sxs-lookup"><span data-stu-id="9056c-188">80px</span></span>** | &nbsp;| <span data-ttu-id="9056c-189">80px</span><span class="sxs-lookup"><span data-stu-id="9056c-189">80px</span></span> |  
| **<span data-ttu-id="9056c-190">80px</span><span class="sxs-lookup"><span data-stu-id="9056c-190">80px</span></span>** | &nbsp;| <span data-ttu-id="9056c-191">80px</span><span class="sxs-lookup"><span data-stu-id="9056c-191">80px</span></span> |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Mostrar tamanhos de faixa" lightbox="../media/grid-show-track-sizes.msft.png":::
   **<span data-ttu-id="9056c-193">Mostrar tamanhos de faixa</span><span class="sxs-lookup"><span data-stu-id="9056c-193">Show track sizes</span></span>**  
:::image-end:::  

### <a name="show-area-names"></a><span data-ttu-id="9056c-194">Mostrar nomes de área</span><span class="sxs-lookup"><span data-stu-id="9056c-194">Show area names</span></span>  

<span data-ttu-id="9056c-195">Para exibir os nomes de área, habilita a caixa de seleção **Mostrar nomes de** área.</span><span class="sxs-lookup"><span data-stu-id="9056c-195">To view the area names, enable the **Show area names** checkbox.</span></span>  <span data-ttu-id="9056c-196">No exemplo, há 3 áreas na grade: **superior**, **inferior1** e **inferior2**.</span><span class="sxs-lookup"><span data-stu-id="9056c-196">In the example, there are 3 areas in the grid: **top**, **bottom1** and **bottom2**.</span></span>  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Mostrar nomes de área" lightbox="../media/grid-show-area-names.msft.png":::
   **<span data-ttu-id="9056c-198">Mostrar nomes de área</span><span class="sxs-lookup"><span data-stu-id="9056c-198">Show area names</span></span>**  
:::image-end:::  

### <a name="extend-grid-lines"></a><span data-ttu-id="9056c-199">Estender linhas de grade</span><span class="sxs-lookup"><span data-stu-id="9056c-199">Extend grid lines</span></span>  

<span data-ttu-id="9056c-200">Habilita **a caixa** de seleção Estender linhas de grade para estender as linhas de grade até a borda do viewport ao longo de cada eixo.</span><span class="sxs-lookup"><span data-stu-id="9056c-200">Enable the **Extend grid lines** checkbox to extend the grid lines to the edge of the viewport along each axis.</span></span>  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Estender linhas de grade" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **<span data-ttu-id="9056c-202">Estender linhas de grade</span><span class="sxs-lookup"><span data-stu-id="9056c-202">Extend grid lines</span></span>**  
:::image-end:::  

## <a name="grid-overlays"></a><span data-ttu-id="9056c-203">Sobreposições de grade</span><span class="sxs-lookup"><span data-stu-id="9056c-203">Grid overlays</span></span>  

<span data-ttu-id="9056c-204">A **seção Sobreposições de** grade contém uma lista de grades presentes na página, cada uma com uma caixa de seleção, juntamente com várias opções.</span><span class="sxs-lookup"><span data-stu-id="9056c-204">The **Grid overlays** section contains a list of grids that are present on the page, each with a checkbox, along with various options.</span></span>  

### <a name="enable-overlay-views-of-multiple-grids"></a><span data-ttu-id="9056c-205">Habilitar exibições de sobreposição de várias grades</span><span class="sxs-lookup"><span data-stu-id="9056c-205">Enable overlay views of multiple grids</span></span>  

<span data-ttu-id="9056c-206">Para exibir a grade de sobreposição para várias grades, escolha a caixa de seleção ao lado de cada nome da grade.</span><span class="sxs-lookup"><span data-stu-id="9056c-206">To display the overlay grid for multiple grids, choose the checkbox next to each name of the grid.</span></span>  <span data-ttu-id="9056c-207">No exemplo, há duas sobreposições de grade habilitadas que são representadas com cores diferentes.</span><span class="sxs-lookup"><span data-stu-id="9056c-207">In the example, there are 2 grid overlays enabled that are each represented with different colors.</span></span>  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Habilitar exibições de sobreposição de várias grades" lightbox="../media/grid-grid-overlays.msft.png":::
   <span data-ttu-id="9056c-209">Habilitar exibições de sobreposição de várias grades</span><span class="sxs-lookup"><span data-stu-id="9056c-209">Enable overlay views of multiple grids</span></span>  
:::image-end:::  

### <a name="customize-the-grid-overlay-color"></a><span data-ttu-id="9056c-210">Personalizar a cor da sobreposição de grade</span><span class="sxs-lookup"><span data-stu-id="9056c-210">Customize the grid overlay color</span></span>  

<span data-ttu-id="9056c-211">Para abrir o selador de cores e personalizar a cor da sobreposição de grade, escolha a caixa ao lado do nome da sobreposição de grade.</span><span class="sxs-lookup"><span data-stu-id="9056c-211">To open the color picker and customize the grid overlay color, choose the box next to the name of the grid overlay.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Personalizar a cor da sobreposição de grade" lightbox="../media/grid-grid-overlays-color.msft.png":::
   <span data-ttu-id="9056c-213">Personalizar a cor da sobreposição de grade</span><span class="sxs-lookup"><span data-stu-id="9056c-213">Customize the grid overlay color</span></span>  
:::image-end:::  

### <a name="highlight-the-grid"></a><span data-ttu-id="9056c-214">Realça a grade</span><span class="sxs-lookup"><span data-stu-id="9056c-214">Highlight the grid</span></span>  

<span data-ttu-id="9056c-215">Para realçar o elemento HTML na ferramenta **Elementos** e rolar até ele na página da Web, escolha o elemento **Mostrar** no painel Elementos \( Elemento Mostrar no ícone do painel Elementos ![ ][ImageShowElementInElementsPanelIcon] \) ícone.</span><span class="sxs-lookup"><span data-stu-id="9056c-215">To highlight the HTML element in the **Elements** tool and scroll to it on the webpage, choose the **Show element in the Elements panel** \(![Show element in the Elements panel icon][ImageShowElementInElementsPanelIcon]\) icon.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Realça a grade" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   <span data-ttu-id="9056c-217">Realça a grade</span><span class="sxs-lookup"><span data-stu-id="9056c-217">Highlight the grid</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="9056c-218">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9056c-218">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageShowElementInElementsPanelIcon]: ../media/show-element-in-element-panel-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Abra o Microsoft Edge DevTools | Microsoft Docs"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "Grade CSS | jec.fyi"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "Grade CSS | jec.fyi"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Layout de Grade CSS | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Layout usando linhas de grade nomeadas | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Posicionamento baseado em linha com grade CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="9056c-225">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9056c-225">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9056c-226">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/css/grid) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="9056c-226">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/grid) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9056c-228">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9056c-228">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
