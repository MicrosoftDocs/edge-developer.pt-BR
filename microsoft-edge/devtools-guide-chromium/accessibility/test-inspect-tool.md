---
description: Use a ferramenta Inspecionar para detectar problemas de acessibilidade pairando sobre a página da Web.
title: Use a ferramenta Inspecionar para detectar problemas de acessibilidade passando o mouse sobre a página da Web
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c95116d38e5b0bda88af43ef8bfde4204b8cb372
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597174"
---
# <a name="use-the-inspect-tool-to-detect-accessibility-issues-by-hovering-over-the-webpage"></a><span data-ttu-id="2d785-104">Use a ferramenta Inspecionar para detectar problemas de acessibilidade passando o mouse sobre a página da Web</span><span class="sxs-lookup"><span data-stu-id="2d785-104">Use the Inspect tool to detect accessibility issues by hovering over the webpage</span></span>

<span data-ttu-id="2d785-105">A **ferramenta Inspecionar** exibe informações sobre elementos individuais à medida que você passar o mouse sobre a página da Web renderizada, incluindo informações de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="2d785-105">The **Inspect** tool displays information about individual elements as you hover over the rendered webpage, including accessibility information.</span></span>
<span data-ttu-id="2d785-106">Por outro lado, **a ferramenta Issues** relata automaticamente problemas para toda a página da Web.</span><span class="sxs-lookup"><span data-stu-id="2d785-106">In contrast, the **Issues** tool automatically reports issues for the entire webpage.</span></span>

<span data-ttu-id="2d785-107">O **botão Inspecionar** ferramenta \( Inspect ![ ](../media/inspect-icon.msft.png) \) está no canto superior esquerdo do DevTools.</span><span class="sxs-lookup"><span data-stu-id="2d785-107">The **Inspect** tool button \(![Inspect](../media/inspect-icon.msft.png)\) is in the upper-left corner of DevTools.</span></span>  <span data-ttu-id="2d785-108">Quando você seleciona o **botão Inspecionar** ferramenta, o botão fica azul, indicando que a **ferramenta Inspecionar** está ativa.</span><span class="sxs-lookup"><span data-stu-id="2d785-108">When you select the **Inspect** tool button, the button turns blue, indicating that the **Inspect** tool is active.</span></span>

<span data-ttu-id="2d785-109">Quando a **ferramenta Inspect** está ativa, passar o mouse sobre qualquer elemento na página da Web renderizada exibe a **sobreposição Inspecionar.**</span><span class="sxs-lookup"><span data-stu-id="2d785-109">When the **Inspect** tool is active, hovering over any element on the rendered webpage displays the **Inspect** overlay.</span></span> <span data-ttu-id="2d785-110">Essa sobreposição exibe informações gerais e informações de acessibilidade sobre esse elemento.</span><span class="sxs-lookup"><span data-stu-id="2d785-110">This overlay displays general information and accessibility information about that element.</span></span>  <span data-ttu-id="2d785-111">A **seção Acessibilidade** da sobreposição **Inspecionar** exibe informações sobre contraste de cor de texto, texto do leitor de tela e suporte ao teclado.</span><span class="sxs-lookup"><span data-stu-id="2d785-111">The **Accessibility** section of the **Inspect** overlay displays information about text-color contrast, screen reader text, and keyboard support.</span></span>

:::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="A ferramenta Inspecionar, mostrando a área do elemento como uma sobreposição multicolor, e mostrando os detalhes do elemento como uma grande sobreposição de informações" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
    <span data-ttu-id="2d785-113">A **ferramenta Inspecionar,** mostrando a área do elemento como uma sobreposição multicolor, e mostrando os detalhes do elemento como uma grande sobreposição de informações</span><span class="sxs-lookup"><span data-stu-id="2d785-113">The **Inspect** tool, showing the element's area as a multicolor overlay, and showing the element's details as a large information overlay</span></span>
:::image-end:::


## <a name="check-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support"></a><span data-ttu-id="2d785-114">Verifique elementos individuais para contraste de texto, texto do leitor de tela e suporte ao teclado</span><span class="sxs-lookup"><span data-stu-id="2d785-114">Check individual elements for text contrast, screen reader text, and keyboard support</span></span>

<!-- Inspect tool: Accessibility section of overlay -->

1.  <span data-ttu-id="2d785-115">Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="2d785-115">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="2d785-116">Selecione o **botão Inspecionar** \( Inspecionar \) no canto superior esquerdo do DevTools para que o ícone seja ![ ](../media/inspect-icon.msft.png) realçado (azul).</span><span class="sxs-lookup"><span data-stu-id="2d785-116">Select the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

    :::image type="complex" source="../media/a11y-testing-basics-inspector.msft.png" alt-text="Para ativar a ferramenta Inspecionar, selecione o botão Inspecionar" lightbox="../media/a11y-testing-basics-inspector.msft.png":::
        <span data-ttu-id="2d785-118">Para ativar a ferramenta **Inspecionar,** selecione o **botão Inspecionar**</span><span class="sxs-lookup"><span data-stu-id="2d785-118">To turn on the **Inspect** tool, select the **Inspect** button</span></span>
    :::image-end:::

1.  <span data-ttu-id="2d785-119">Passe o mouse sobre qualquer elemento na página da Web de demonstração renderizada.</span><span class="sxs-lookup"><span data-stu-id="2d785-119">Hover over any element in the rendered demo webpage.</span></span>  <span data-ttu-id="2d785-120">A **ferramenta Inspecionar** mostra uma sobreposição de informações abaixo do elemento na página da Web renderizada.</span><span class="sxs-lookup"><span data-stu-id="2d785-120">The **Inspect** tool shows an information overlay below the element within the rendered webpage.</span></span>

    :::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="A ferramenta Inspecionar, mostrando o layout do elemento como uma sobreposição multicolor, e mostrando os detalhes do elemento como uma grande sobreposição de informações" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
        <span data-ttu-id="2d785-122">A **ferramenta Inspecionar,** mostrando o layout do elemento como uma sobreposição multicolor, e mostrando os detalhes do elemento como uma grande sobreposição de informações</span><span class="sxs-lookup"><span data-stu-id="2d785-122">The **Inspect** tool, showing the element's layout as a multicolor overlay, and showing the element's details as a large information overlay</span></span>
    :::image-end:::

<span data-ttu-id="2d785-123">A parte inferior da sobreposição **Inspecionar** tem uma seção **Accessibility** que contém as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="2d785-123">The bottom part of the **Inspect** overlay has an **Accessibility** section that contains the following information:</span></span>

*   <span data-ttu-id="2d785-124">**Contraste** define se um elemento pode ser compreendido por pessoas com baixa visão.</span><span class="sxs-lookup"><span data-stu-id="2d785-124">**Contrast** defines whether an element can be understood by people with low vision.</span></span>  <span data-ttu-id="2d785-125">A [taxa de][W3CContrastRatio] contraste, conforme definido pelas Diretrizes do [WCAG,][WCAG] indica se há contraste suficiente (um ícone de marca de verificação verde) ou não suficiente (um ícone de ponto de exclamação laranja).</span><span class="sxs-lookup"><span data-stu-id="2d785-125">The [contrast ratio][W3CContrastRatio] as defined by the [WCAG Guidelines][WCAG] indicates whether there is enough contrast (a green check mark icon) or not enough (an orange exclamation-point icon).</span></span>

*   <span data-ttu-id="2d785-126">**Nome** e **função** são quais tecnologias assistivas, como leitores de tela, relatarão sobre o elemento.</span><span class="sxs-lookup"><span data-stu-id="2d785-126">**Name** and **Role** are what assistive technology such as screen readers will report about the element.</span></span>
    *   <span data-ttu-id="2d785-127">O **Nome** é o conteúdo de texto de um `a` elemento.</span><span class="sxs-lookup"><span data-stu-id="2d785-127">The **Name** is the text content of an `a` element.</span></span>  <span data-ttu-id="2d785-128">Para o elemento `<a href="/">About Us</a>` , **o nome** mostrado na ferramenta Inspecionar é "Sobre nós".</span><span class="sxs-lookup"><span data-stu-id="2d785-128">For the element `<a href="/">About Us</a>`, the **Name** shown in the Inspect tool is "About Us".</span></span>
    *   <span data-ttu-id="2d785-129">A **função** do elemento.</span><span class="sxs-lookup"><span data-stu-id="2d785-129">The **Role** of the element.</span></span>  <span data-ttu-id="2d785-130">Geralmente, esse é o nome do elemento, como `article` `img` , , ou `link` `heading` .</span><span class="sxs-lookup"><span data-stu-id="2d785-130">This is usually the element name, such as `article`, `img` , `link`, or `heading`.</span></span>  <span data-ttu-id="2d785-131">Os `div` elementos e são chamados de `span` `generic` .</span><span class="sxs-lookup"><span data-stu-id="2d785-131">The `div` and `span` elements are referred to as `generic`.</span></span>

*   <span data-ttu-id="2d785-132">**O foco no teclado** indica se os usuários podem alcançar o elemento independentemente do dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="2d785-132">**Keyboard-focusable** indicates whether users can reach the element regardless of input device.</span></span>
    *   <span data-ttu-id="2d785-133">Um ícone de marca de verificação verde indica que o elemento é focalizado no teclado.</span><span class="sxs-lookup"><span data-stu-id="2d785-133">A green check mark icon indicates that the element is keyboard-focusable.</span></span>
    *   <span data-ttu-id="2d785-134">Um círculo cinza com linha diagonal indica que o elemento não é focalizado no teclado.</span><span class="sxs-lookup"><span data-stu-id="2d785-134">A gray circle with diagonal line indicates that the element isn't keyboard-focusable.</span></span>


## <a name="additional-information-in-the-inspect-overlay"></a><span data-ttu-id="2d785-135">Informações adicionais na sobreposição Inspecionar</span><span class="sxs-lookup"><span data-stu-id="2d785-135">Additional information in the Inspect overlay</span></span>

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

<span data-ttu-id="2d785-136">A parte superior da sobreposição **Inspecionar,** que está acima da seção **Acessibilidade,** lista os seguintes detalhes do elemento.</span><span class="sxs-lookup"><span data-stu-id="2d785-136">The top part of the **Inspect** overlay, which is above the **Accessibility** section, lists the following details of the element.</span></span>

*   <span data-ttu-id="2d785-137">Tipo de layout.</span><span class="sxs-lookup"><span data-stu-id="2d785-137">Layout type.</span></span> <span data-ttu-id="2d785-138">Se o elemento estiver posicionado usando uma caixa de flexão ou grade, um ícone \(</span><span class="sxs-lookup"><span data-stu-id="2d785-138">If the element is positioned using a flexbox or grid, an icon \(</span></span>![Ícone de layout de grade](../media/grid-icon.msft.png)<span data-ttu-id="2d785-140">\) é exibido.</span><span class="sxs-lookup"><span data-stu-id="2d785-140">\) is displayed.</span></span>
*   <span data-ttu-id="2d785-141">Nome do elemento, como `h1` , `h2` ou `div` .</span><span class="sxs-lookup"><span data-stu-id="2d785-141">Name of the element, such as `h1`, `h2`, or `div`.</span></span>
*   <span data-ttu-id="2d785-142">As dimensões do elemento em pixels.</span><span class="sxs-lookup"><span data-stu-id="2d785-142">The dimensions of the element in pixels.</span></span>
*   <span data-ttu-id="2d785-143">A cor como uma amostra de cores (ou um quadrado pequeno e colorido) e como uma cadeia de caracteres (como `#336699` ).</span><span class="sxs-lookup"><span data-stu-id="2d785-143">The color as a color swatch (or a small, colored square) and as a string (such as `#336699`).</span></span>
*   <span data-ttu-id="2d785-144">Informações de fonte, como famílias de tamanho e fonte.</span><span class="sxs-lookup"><span data-stu-id="2d785-144">Font information, such as size and font families.</span></span>
*   <span data-ttu-id="2d785-145">Margem e preenchimento em pixels.</span><span class="sxs-lookup"><span data-stu-id="2d785-145">Margin and padding in pixels.</span></span>


## <a name="identify-nested-regions-using-color-highlighting"></a><span data-ttu-id="2d785-146">Identificar regiões aninhadas usando realçamento de cores</span><span class="sxs-lookup"><span data-stu-id="2d785-146">Identify nested regions using color highlighting</span></span> 

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

<span data-ttu-id="2d785-147">Além da sobreposição de informações, a ferramenta **Inspect** também fornece coloração de região semelhante ao passar o mouse na árvore DOM na ferramenta **Elements.**</span><span class="sxs-lookup"><span data-stu-id="2d785-147">In addition to the information overlay, the **Inspect** tool also provides region-coloring that's similar to hovering in the DOM tree in the **Elements** tool.</span></span>

1.  <span data-ttu-id="2d785-148">Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="2d785-148">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="2d785-149">Selecione o **botão Inspecionar** \( Inspecionar ícone da ferramenta \) no canto superior esquerdo do DevTools, para que o botão seja ![ ](../media/inspect-icon.msft.png) realçado (azul).</span><span class="sxs-lookup"><span data-stu-id="2d785-149">Select the **Inspect** button \(![Inspect tool icon](../media/inspect-icon.msft.png)\) in the top-left corner of DevTools, so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="2d785-150">Passe o mouse sobre diferentes partes da página da web de demonstração renderizada.</span><span class="sxs-lookup"><span data-stu-id="2d785-150">Hover over different parts of the rendered demo webpage.</span></span>  <span data-ttu-id="2d785-151">Cada elemento na página da Web agora é exibido com uma sobreposição multicolor.</span><span class="sxs-lookup"><span data-stu-id="2d785-151">Each element in the webpage now displays with a multicolor overlay.</span></span> <span data-ttu-id="2d785-152">Essa sobreposição multicolor pode exibir regiões aninhadas dentro de um elemento.</span><span class="sxs-lookup"><span data-stu-id="2d785-152">This multicolor overlay can display nested regions inside of an element.</span></span> <span data-ttu-id="2d785-153">Por exemplo, passe o mouse sobre a margem esquerda de **Gatos**.</span><span class="sxs-lookup"><span data-stu-id="2d785-153">For example, hover over the left margin of **Cats**.</span></span>  <span data-ttu-id="2d785-154">A **ferramenta Inspect** realça várias partes retangulares da seção **Gatos** com cores diferentes, mostrando o layout que resulta das definições de flexbox CSS em sua página da Web.</span><span class="sxs-lookup"><span data-stu-id="2d785-154">The **Inspect** tool highlights several rectangular portions of the **Cats** section with different colors, showing the layout that results from the CSS flexbox definitions on your webpage.</span></span>

:::image type="complex" source="../media/inspect-tool-flexbox-overlay.msft.png" alt-text="Sobreposição de flexbox multicolor e sobreposição de informações ao usar a ferramenta Inspecionar" lightbox="../media/inspect-tool-flexbox-overlay.msft.png":::
    <span data-ttu-id="2d785-156">Sobreposição de flexbox multicolor e sobreposição de informações ao usar a **ferramenta Inspecionar**</span><span class="sxs-lookup"><span data-stu-id="2d785-156">Multicolor flexbox overlay and information overlay when using the **Inspect** tool</span></span>
:::image-end:::

<span data-ttu-id="2d785-157">Para configurar a sobreposição de grade ou sobreposição de área flexível, na **ferramenta Elementos,** selecione a **guia Layout.**  Para obter mais informações, navegue até [Inspecionar Grade CSS](..\css\grid.md).</span><span class="sxs-lookup"><span data-stu-id="2d785-157">To configure the grid overlay or flexbox overlay, in the **Elements** tool, select the **Layout** tab.  For more information, navigate to [Inspect CSS Grid](..\css\grid.md).</span></span>


## <a name="use-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css"></a><span data-ttu-id="2d785-158">Use a ferramenta Inspecionar para passar o mouse sobre a página da Web para realçar o DOM e CSS</span><span class="sxs-lookup"><span data-stu-id="2d785-158">Use the Inspect tool to hover over the webpage to highlight the DOM and CSS</span></span>

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

1.  <span data-ttu-id="2d785-159">Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="2d785-159">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="2d785-160">Selecione o **botão Inspecionar** \( a ferramenta Inspecionar \) no canto superior esquerdo do DevTools, para que o botão seja ![ ](../media/inspect-icon.msft.png) realçado (azul).</span><span class="sxs-lookup"><span data-stu-id="2d785-160">Select the **Inspect** button \(![the Inspect tool](../media/inspect-icon.msft.png)\) in the top-left corner of DevTools, so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="2d785-161">Selecione a **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="2d785-161">Select the **Elements** tool.</span></span>

1.  <span data-ttu-id="2d785-162">Com a **ferramenta Inspecionar** ativa, passe o mouse sobre diferentes partes da página da Web renderizada.</span><span class="sxs-lookup"><span data-stu-id="2d785-162">With the **Inspect** tool active, hover over different parts of the rendered webpage.</span></span>  <span data-ttu-id="2d785-163">Na ferramenta **Elementos,** a árvore DOM HTML se expande automaticamente para mostrar informações sobre o elemento sobre o que você passar o mouse.</span><span class="sxs-lookup"><span data-stu-id="2d785-163">In the **Elements** tool, the HTML DOM tree automatically expands to show information about the element you hover over.</span></span>  <span data-ttu-id="2d785-164">O foco não faz com que o painel **Estilos** seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="2d785-164">Hovering doesn't cause the **Styles** pane to update.</span></span>

1.  <span data-ttu-id="2d785-165">Agora selecione qualquer elemento na página da Web renderizada.</span><span class="sxs-lookup"><span data-stu-id="2d785-165">Now select any element within the rendered webpage.</span></span>  <span data-ttu-id="2d785-166">A **ferramenta Elements** abre e exibe automaticamente o HTML do elemento na árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="2d785-166">The **Elements** tool automatically opens and displays the HTML of the element in the DOM tree.</span></span> <span data-ttu-id="2d785-167">A ferramenta também exibe o CSS aplicado no elemento no painel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="2d785-167">The tool also displays the applied CSS on the element in the **Styles** pane.</span></span>  <span data-ttu-id="2d785-168">Selecionar um elemento na página da Web renderizada desliga a **ferramenta Inspecionar.**</span><span class="sxs-lookup"><span data-stu-id="2d785-168">Selecting an element on the rendered webpage turns off the **Inspect** tool.</span></span>

:::image type="complex" source="../media/a11y-testing-basics-inspector-selected-element.msft.png" alt-text="Detalhes sobre o elemento selecionado são exibidos na ferramenta Elements" lightbox="../media/a11y-testing-basics-inspector-selected-element.msft.png":::
    <span data-ttu-id="2d785-170">Detalhes sobre o elemento selecionado são exibidos na **ferramenta Elements**</span><span class="sxs-lookup"><span data-stu-id="2d785-170">Details about the selected element are displayed in the **Elements** tool</span></span>
:::image-end:::

<span data-ttu-id="2d785-171">Depois de selecionar um elemento na página \*\*\*\* renderizada, você pode usar a \*\*\*\* guia Acessibilidade (perto da guia **Estilos)** para exibir a Árvore de Acessibilidade e usar o Visualizador de Ordem de **Origem**.</span><span class="sxs-lookup"><span data-stu-id="2d785-171">After selecting an element in the rendered page, you could then use the **Accessibility** tab (near the **Styles** tab) to view the **Accessibility Tree** and use the **Source Order Viewer**.</span></span>


## <a name="see-also"></a><span data-ttu-id="2d785-172">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2d785-172">See also</span></span>

*  [<span data-ttu-id="2d785-173">Inspecionar um nó</span><span class="sxs-lookup"><span data-stu-id="2d785-173">Inspect a node</span></span>](../dom/index.md#inspect-a-node)
*  [<span data-ttu-id="2d785-174">Verifique o contraste de cor de texto no estado padrão usando a ferramenta Inspecionar</span><span class="sxs-lookup"><span data-stu-id="2d785-174">Check text-color contrast in the default state using the Inspect tool</span></span>](test-inspect-text-contrast.md)
*  [<span data-ttu-id="2d785-175">Visão geral dos testes de acessibilidade usando o DevTools</span><span class="sxs-lookup"><span data-stu-id="2d785-175">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2d785-176">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2d785-176">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
[W3CContrastRatio]: https://www.w3.org/TR/WCAG21/#dfn-contrast-ratio "taxa de contraste | W3C"
[WCAG]: https://www.w3.org/TR/WCAG21/ "Diretrizes de acessibilidade de conteúdo da Web | W3C"
