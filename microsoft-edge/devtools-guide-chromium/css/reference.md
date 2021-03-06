---
description: Descubra novos fluxos de trabalho para exibição e alteração de CSS no Microsoft Edge DevTools.
title: Referência CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: a99cf46c4c0a6c6f14892268a30f8aab471e919d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399138"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="css-reference"></a><span data-ttu-id="4ec6e-104">Referência CSS</span><span class="sxs-lookup"><span data-stu-id="4ec6e-104">CSS reference</span></span>  

<span data-ttu-id="4ec6e-105">Descubra novos fluxos de trabalho na referência abrangente a seguir dos recursos do Microsoft Edge DevTools relacionados à exibição e alteração de CSS.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-105">Discover new workflows in the following comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="4ec6e-106">Para saber as noções básicas, navegue até [Começar a exibir e alterar CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="4ec6e-106">To learn the basics, navigate to [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted].</span></span>  

## <a name="choose-an-element"></a><span data-ttu-id="4ec6e-107">Escolher um elemento</span><span class="sxs-lookup"><span data-stu-id="4ec6e-107">Choose an element</span></span>  

<span data-ttu-id="4ec6e-108">A **ferramenta Elements** do DevTools permite exibir ou alterar o CSS de um elemento de cada vez.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-108">The **Elements** tool of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="4ec6e-109">O elemento selecionado é realçado na árvore **DOM**.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-109">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="4ec6e-110">Os estilos do elemento são mostrados no painel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-110">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="4ec6e-111">Para um tutorial, navegue até [Exibir o CSS para um elemento][DevToolsCSSGetStartedTutorial].</span><span class="sxs-lookup"><span data-stu-id="4ec6e-111">For a tutorial, navigate to [View the CSS for an element][DevToolsCSSGetStartedTutorial].</span></span>  

> [!NOTE]
> <span data-ttu-id="4ec6e-112">Na figura a seguir, o `h1` elemento realçado na Árvore **DOM** é o elemento selecionado.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-112">In the following figure, the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="4ec6e-113">À direita, os estilos do elemento são mostrados no painel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-113">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="4ec6e-114">À esquerda, o elemento é realçado no viewport, mas somente porque o mouse está atualmente pairando sobre ele na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-114">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-h1.msft.png":::
   <span data-ttu-id="4ec6e-116">Um exemplo de um elemento selecionado</span><span class="sxs-lookup"><span data-stu-id="4ec6e-116">An example of a selected element</span></span>  
:::image-end:::  

<span data-ttu-id="4ec6e-117">Use uma das seguintes ações para selecionar um elemento.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-117">Use one the following actions to select an element.</span></span>  

*   <span data-ttu-id="4ec6e-118">No seu viewport, passe o mouse no elemento, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-118">In your viewport, hover on the element, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
*   <span data-ttu-id="4ec6e-119">No DevTools, escolha **Selecionar** um elemento \( Selecione um elemento \) ou selecione ![ ][ImageSelectAnElementIcon] `Control` + `Shift` + `C` \(Windows, Linux\) `Command` + `Shift` + `C` ou \(macOS\) e escolha o elemento no viewport.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-119">In DevTools, choose **Select an element** \(![Select an element][ImageSelectAnElementIcon]\) or select `Control`+`Shift`+`C` \(Windows, Linux\) or `Command`+`Shift`+`C` \(macOS\), and then choose the element in the viewport.</span></span>  
*   <span data-ttu-id="4ec6e-120">Em DevTools, escolha o elemento na Árvore **DOM**.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-120">In DevTools, choose the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="4ec6e-121">No DevTools, execute uma consulta como no Console , passe o mouse no resultado, abra o menu contextual \(clique com o botão direito do mouse\) e escolha `document.querySelector('p')` Revelar em Elementos \*\*\*\* **painel**.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-121">In DevTools, run a query like `document.querySelector('p')` in the **Console**, hover on the result, open the contextual menu \(right-click\), and choose **Reveal in Elements panel**.</span></span>  

## <a name="view-css"></a><span data-ttu-id="4ec6e-122">Exibir CSS</span><span class="sxs-lookup"><span data-stu-id="4ec6e-122">View CSS</span></span>  

### <a name="view-the-external-stylesheet-where-a-rule-is-defined"></a><span data-ttu-id="4ec6e-123">Exibir a folha de estilos externa onde uma regra é definida</span><span class="sxs-lookup"><span data-stu-id="4ec6e-123">View the external stylesheet where a rule is defined</span></span>  

<span data-ttu-id="4ec6e-124">No painel **Estilos,** escolha o link ao lado de uma regra CSS para abrir a folha de estilos externa que define a regra.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-124">In the **Styles** pane, choose the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  

<span data-ttu-id="4ec6e-125">Se a folha de estilos for minificada, navegue até [Tornar um arquivo minificado acessível][DevToolsJavascriptReferenceFormat].</span><span class="sxs-lookup"><span data-stu-id="4ec6e-125">If the stylesheet is minified, navigate to [Make a minified file readable][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="4ec6e-126">Na figura a seguir, depois de escolher, você é levado para a `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` linha 2 `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` de , onde a regra CSS é `.content h1:first-of-type` definida.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-126">In the following figure, after you choose `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` you are taken to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Exibindo a folha de estilos em que uma regra é definida" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  <span data-ttu-id="4ec6e-128">Exibindo a folha de estilos em que uma regra é definida</span><span class="sxs-lookup"><span data-stu-id="4ec6e-128">Viewing the stylesheet where a rule is defined</span></span>  
:::image-end:::  

### <a name="view-only-the-css-that-is-actually-applied-to-an-element"></a><span data-ttu-id="4ec6e-129">Exibir apenas o CSS que é realmente aplicado a um elemento</span><span class="sxs-lookup"><span data-stu-id="4ec6e-129">View only the CSS that is actually applied to an element</span></span>  

<span data-ttu-id="4ec6e-130">O **painel Estilos** mostra todas as regras que se aplicam a um elemento, incluindo declarações que foram substituídos.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-130">The **Styles** panel shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="4ec6e-131">Quando você não estiver interessado em declarações substituidas, use o painel **Computed** para exibir apenas o CSS que está realmente sendo aplicado a um elemento.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-131">When you are not interested in overridden declarations, use the **Computed** panel to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="4ec6e-132">[Selecione um elemento](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-132">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="4ec6e-133">Navegue até **o painel Computed** na **ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-133">Navigate to the **Computed** panel in the **Elements** tool.</span></span>  

> [!NOTE]
> <span data-ttu-id="4ec6e-134">Em uma janela ampla do DevTools, o painel **Computed** não existe.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-134">On a wide DevTools window, the **Computed** panel does not exist.</span></span>  <span data-ttu-id="4ec6e-135">O conteúdo do painel **Computed** é mostrado no painel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-135">The contents of the **Computed** panel are shown on the **Styles** panel.</span></span>  

<span data-ttu-id="4ec6e-136">As propriedades herdadas são opacas.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-136">Inherited properties are opaque.</span></span>  <span data-ttu-id="4ec6e-137">Para exibir todos os valores herdados, selecione a **caixa de seleção Mostrar Tudo.**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-137">To display all inherited values, select the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="4ec6e-138">Na figura a seguir, o **painel Computed** mostra as propriedades CSS que estão sendo aplicadas ao elemento selecionado `h1` no momento.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-138">In the following figure, the **Computed** panel shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="O painel Computed" lightbox="../media/css-elements-computed-h1.msft.png":::
   <span data-ttu-id="4ec6e-140">O **painel Computed**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-140">The **Computed** panel</span></span>  
:::image-end:::  

### <a name="view-css-properties-in-alphabetical-order"></a><span data-ttu-id="4ec6e-141">Exibir propriedades CSS em ordem alfabética</span><span class="sxs-lookup"><span data-stu-id="4ec6e-141">View CSS properties in alphabetical order</span></span>  

<span data-ttu-id="4ec6e-142">Use o **painel Computed.**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-142">Use the **Computed** panel.</span></span>  <span data-ttu-id="4ec6e-143">Navegue [até Exibir somente o CSS que é realmente aplicado a um elemento](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-143">Navigate to [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <a name="view-inherited-css-properties"></a><span data-ttu-id="4ec6e-144">Exibir propriedades CSS herdadas</span><span class="sxs-lookup"><span data-stu-id="4ec6e-144">View inherited CSS properties</span></span>  

<span data-ttu-id="4ec6e-145">Marque a **caixa de seleção** Mostrar Tudo no painel **Computado.**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-145">Check the **Show All** checkbox in the **Computed** panel.</span></span>  <span data-ttu-id="4ec6e-146">Navegue [até Exibir somente o CSS que é realmente aplicado a um elemento](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-146">Navigate to [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <a name="view-the-box-model-for-an-element"></a><span data-ttu-id="4ec6e-147">Exibir o modelo de caixa de um elemento</span><span class="sxs-lookup"><span data-stu-id="4ec6e-147">View the box model for an element</span></span>  

<span data-ttu-id="4ec6e-148">Para exibir [o modelo de caixa][MDNBoxModel] de um elemento, navegue até o painel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-148">To view [the box model][MDNBoxModel] of an element, navigate to the **Styles** panel.</span></span>  <span data-ttu-id="4ec6e-149">Se sua janela DevTools for estreita, o diagrama **do Modelo** de Caixa será na parte inferior do painel.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-149">If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the panel.</span></span>  

<span data-ttu-id="4ec6e-150">Escolha e edite em um valor para alterar um valor.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-150">Choose and edit on a value to change a value.</span></span>  

> [!NOTE]
> <span data-ttu-id="4ec6e-151">Na figura a seguir, o diagrama **Modelo** de Caixa no painel **Estilos** mostra o modelo de caixa do elemento selecionado `h1` no momento.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-151">In the following figure, the **Box Model** diagram in the **Styles** panel shows the box model for the currently selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="O diagrama do modelo de caixa" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   <span data-ttu-id="4ec6e-153">O **diagrama do modelo de** caixa</span><span class="sxs-lookup"><span data-stu-id="4ec6e-153">The **Box Model** diagram</span></span>  
:::image-end:::  

### <a name="search-and-filter-the-css-of-an-element"></a><span data-ttu-id="4ec6e-154">Pesquisar e filtrar o CSS de um elemento</span><span class="sxs-lookup"><span data-stu-id="4ec6e-154">Search and filter the CSS of an element</span></span>  

<span data-ttu-id="4ec6e-155">Use a **caixa de** texto Filtrar nos **painéis Estilos** e **Computados** para pesquisar propriedades ou valores CSS específicos.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-155">Use the **Filter** text box on the **Styles** and **Computed** panels to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="4ec6e-156">Para também pesquisar propriedades herdadas no **painel Computed,** marque a caixa de seleção **Mostrar Tudo.**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-156">To also search inherited properties in the **Computed** panel, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="4ec6e-157">Na figura a seguir, o painel **Estilos** é filtrado para mostrar apenas regras que incluem a consulta de pesquisa `color` .</span><span class="sxs-lookup"><span data-stu-id="4ec6e-157">In the following figure, the **Styles** panel is filtered to only show rules that include the search query `color`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Filtrar o painel Estilos" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   <span data-ttu-id="4ec6e-159">Filtrar o **painel Estilos**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-159">Filter the **Styles** panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="4ec6e-160">Na figura a seguir, o **painel Computed** é filtrado para mostrar apenas declarações que incluem a consulta de pesquisa `100%` .</span><span class="sxs-lookup"><span data-stu-id="4ec6e-160">In the following figure, the **Computed** panel is filtered to only show declarations that include the search query `100%`.</span></span>  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Filtrar o painel Computed" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   <span data-ttu-id="4ec6e-162">Filtrar o **painel Computed**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-162">Filter the **Computed** panel</span></span>  
:::image-end:::  

### <a name="toggle-a-pseudo-class"></a><span data-ttu-id="4ec6e-163">Alternar uma pseudo-classe</span><span class="sxs-lookup"><span data-stu-id="4ec6e-163">Toggle a pseudo-class</span></span>  

<span data-ttu-id="4ec6e-164">Conclua as seguintes ações para alternar uma pseudo-classe `:active` como , , ou `:focus` `:hover` `:visited` .</span><span class="sxs-lookup"><span data-stu-id="4ec6e-164">Complete the following actions to toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`.</span></span>  

1.  <span data-ttu-id="4ec6e-165">[Selecione um elemento](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-165">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="4ec6e-166">Na ferramenta **Elementos,** navegue até o **painel Estilos.**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-166">On the **Elements** tool, navigate to the **Styles** panel.</span></span>  
1.  <span data-ttu-id="4ec6e-167">Escolha **:hov**.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-167">Choose **:hov**.</span></span>  
1.  <span data-ttu-id="4ec6e-168">Verifique a pseudo-classe que você deseja habilitar.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-168">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="4ec6e-169">Na figura a seguir, alterne a `:hover` pseudo-classe.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-169">In the following figure, toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="4ec6e-170">No viewport, verifique se a declaração está sendo aplicada ao elemento, mesmo que o elemento não está realmente sendo `background-color: cornflowerblue` pairado sobre.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-170">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Alternar a pseudo-classe :hover" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   <span data-ttu-id="4ec6e-172">Alternar a `:hover` pseudo-classe</span><span class="sxs-lookup"><span data-stu-id="4ec6e-172">Toggle the `:hover` pseudo-class</span></span>  
:::image-end:::  

<span data-ttu-id="4ec6e-173">Para um tutorial interativo, navegue até [Adicionar um pseudostate a uma classe][DevToolsCSSGetStartedAddPseudoState].</span><span class="sxs-lookup"><span data-stu-id="4ec6e-173">For an interactive tutorial, navigate to [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState].</span></span>  

### <a name="view-a-page-in-print-mode"></a><span data-ttu-id="4ec6e-174">Exibir uma página no modo de impressão</span><span class="sxs-lookup"><span data-stu-id="4ec6e-174">View a page in print mode</span></span>  

<span data-ttu-id="4ec6e-175">Conclua as seguintes ações para exibir uma página no modo de impressão.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-175">Complete the following actions to view a page in print mode.</span></span>  

1.  <span data-ttu-id="4ec6e-176">[Abra o Menu de Comando][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="4ec6e-176">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="4ec6e-177">Comece a digitar `Rendering` e selecione `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="4ec6e-177">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="4ec6e-178">Para o **menu suspenso Emular Mídia CSS,** escolha **imprimir**.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-178">For the **Emulate CSS Media** dropdown, choose **print**.</span></span>  

### <a name="view-used-and-unused-css-with-the-coverage-tool"></a><span data-ttu-id="4ec6e-179">Exibir CSS usado e não usado com a ferramenta Coverage</span><span class="sxs-lookup"><span data-stu-id="4ec6e-179">View used and unused CSS with the Coverage tool</span></span>  

<span data-ttu-id="4ec6e-180">A **ferramenta Coverage** mostra qual CSS uma página realmente usa.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-180">The **Coverage** tool shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="4ec6e-181">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) enquanto o [][DevToolsCommandMenu]DevTools está em foco para abrir o Menu de Comando .</span><span class="sxs-lookup"><span data-stu-id="4ec6e-181">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to [open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="4ec6e-182">Comece a digitar `coverage` e escolha Mostrar **Cobertura**.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-182">Start typing `coverage` and choose **Show Coverage**.</span></span>  <span data-ttu-id="4ec6e-183">A **ferramenta Coverage** é exibida.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-183">The **Coverage** tool appears.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Abrindo a ferramenta Cobertura no Menu de Comando" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             <span data-ttu-id="4ec6e-185">Abra a **ferramenta Cobertura** no Menu **de Comando**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-185">Open the **Coverage** tool from the **Command Menu**</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="A ferramenta Coverage" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             <span data-ttu-id="4ec6e-187">A **ferramenta Coverage**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-187">The **Coverage** tool</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="4ec6e-188">Escolha **Iniciar a cobertura de instrumentação e atualize a página** \( Inicie a cobertura de ![ instrumentação e atualize a ][ImageRefreshIcon] página \).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-188">Choose **Start instrumenting coverage and refresh the page** \(![Start instrumenting coverage and refresh the page][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="4ec6e-189">A página atualiza e a ferramenta **Coverage** fornece uma visão geral de quanto CSS \(e JavaScript\) é usado a partir de cada arquivo que o navegador carrega.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-189">The page refreshes and the **Coverage** tool provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="4ec6e-190">Verde representa CSS usado.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-190">Green represents used CSS.</span></span>  <span data-ttu-id="4ec6e-191">Vermelho representa CSS nãousado.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-191">Red represents unused CSS.</span></span>  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Uma visão geral de quanto CSS (e JavaScript) é usado e não usado" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       <span data-ttu-id="4ec6e-193">Uma visão geral de quanto CSS \(e JavaScript\) é usado e não usado</span><span class="sxs-lookup"><span data-stu-id="4ec6e-193">An overview of how much CSS \(and JavaScript\) is used and unused</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="4ec6e-194">Para exibir uma divisão linha a linha do que CSS é usado, escolha um arquivo CSS.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-194">To display a line-by-line breakdown of what CSS is used, choose a CSS file.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="4ec6e-195">Na figura a seguir, as linhas 145 a 147 e 149 a 151 de não são usadas, enquanto as linhas `b66bc881.site-ltr.css` 163 a 166 são usadas.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-195">In the following figure, lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Uma divisão linha a linha de CSS usada e não utilizada" lightbox="../media/css-sources-css-coverage.msft.png":::
       <span data-ttu-id="4ec6e-197">Uma divisão linha a linha de CSS usada e não utilizada</span><span class="sxs-lookup"><span data-stu-id="4ec6e-197">A line-by-line breakdown of used and unused CSS</span></span>  
    :::image-end:::  
    
### <a name="force-print-preview-mode"></a><span data-ttu-id="4ec6e-198">Forçar o modo de visualização de impressão</span><span class="sxs-lookup"><span data-stu-id="4ec6e-198">Force print preview mode</span></span>  

<span data-ttu-id="4ec6e-199">Navegue [até Forçar DevTools no modo Visualização de Impressão.][DevToolsCssPrintPreview]</span><span class="sxs-lookup"><span data-stu-id="4ec6e-199">Navigate to [Force DevTools into Print Preview mode][DevToolsCssPrintPreview].</span></span>  

## <a name="change-css"></a><span data-ttu-id="4ec6e-200">Alterar CSS</span><span class="sxs-lookup"><span data-stu-id="4ec6e-200">Change CSS</span></span>  

<!-- todo s/CSS declaration/declaration/ -->  

### <a name="add-a-css-declaration-to-an-element"></a><span data-ttu-id="4ec6e-201">Adicionar uma declaração CSS a um elemento</span><span class="sxs-lookup"><span data-stu-id="4ec6e-201">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="4ec6e-202">A ordem das declarações afeta a forma como um elemento é estilado, use a lista a seguir para ajudá-lo a adicionar declarações de maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-202">The order of declarations affects how an element is styled, use the following list to help you add declarations in different ways.</span></span>  

*   <span data-ttu-id="4ec6e-203">[Adicione uma declaração em linha](#add-an-inline-declaration).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-203">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="4ec6e-204">Equivalente a adicionar `style` um atributo ao HTML de um elemento.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-204">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="4ec6e-205">[Adicione uma declaração a uma regra de estilo.](#add-a-declaration-to-a-style-rule)</span><span class="sxs-lookup"><span data-stu-id="4ec6e-205">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="4ec6e-206">Qual fluxo de trabalho você deve usar?</span><span class="sxs-lookup"><span data-stu-id="4ec6e-206">What workflow should you use?</span></span>** <span data-ttu-id="4ec6e-207">Para a maioria dos cenários, você provavelmente deseja usar o fluxo de trabalho de declaração em linha.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-207">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="4ec6e-208">As declarações em linha têm maior especificidade do que as externas, portanto, o fluxo de trabalho em linha garante que as alterações tenham efeito no elemento esperado.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-208">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in your expected element.</span></span>  <span data-ttu-id="4ec6e-209">Para obter mais informações sobre a especificidade, navegue até [Tipos de Seletor][MDNSelectorTypes].</span><span class="sxs-lookup"><span data-stu-id="4ec6e-209">For more information about specificity, navigate to [Selector Types][MDNSelectorTypes].</span></span>  

<span data-ttu-id="4ec6e-210">Se você estiver depurando quaisquer estilos do elemento e precisar testar especificamente o que acontece quando uma declaração é definida em locais diferentes, use o outro fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-210">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <a name="add-an-inline-declaration"></a><span data-ttu-id="4ec6e-211">Adicionar uma declaração em linha</span><span class="sxs-lookup"><span data-stu-id="4ec6e-211">Add an inline declaration</span></span>  

<span data-ttu-id="4ec6e-212">Conclua as seguintes ações para adicionar uma declaração em linha.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-212">Complete the following actions to add an inline declaration.</span></span>  

1.  <span data-ttu-id="4ec6e-213">[Selecione um elemento](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-213">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="4ec6e-214">No painel **Estilos,** escolha entre os colchetes da **seção element.style.**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-214">In the **Styles** pane, choose between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="4ec6e-215">O cursor se concentra, permitindo que você insira texto.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-215">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="4ec6e-216">Insira um nome de propriedade e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4ec6e-216">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="4ec6e-217">Insira um valor válido para essa propriedade e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4ec6e-217">Enter a valid value for that property and select `Enter`.</span></span>  <span data-ttu-id="4ec6e-218">Na Árvore **DOM,** verifique se um `style` atributo foi adicionado ao elemento.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-218">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="4ec6e-219">Na figura a seguir, `margin-top` as propriedades e foram `background-color` aplicadas ao elemento selecionado.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-219">In the following figure, the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="4ec6e-220">Na Árvore **DOM,** verifique se as declarações são refletidas no `style` atributo de um elemento.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-220">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Adicionar declarações em linha" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   <span data-ttu-id="4ec6e-222">Adicionar declarações em linha</span><span class="sxs-lookup"><span data-stu-id="4ec6e-222">Add inline declarations</span></span>  
:::image-end:::  

#### <a name="add-a-declaration-to-a-style-rule"></a><span data-ttu-id="4ec6e-223">Adicionar uma declaração a uma regra de estilo</span><span class="sxs-lookup"><span data-stu-id="4ec6e-223">Add a declaration to a style rule</span></span>  

<span data-ttu-id="4ec6e-224">Conclua as seguintes ações para adicionar uma declaração a uma regra de estilo existente.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-224">Complete the following actions to add a declaration to an existing style rule.</span></span>  

1.  <span data-ttu-id="4ec6e-225">[Selecione um elemento](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-225">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="4ec6e-226">No painel **Estilos,** escolha entre os colchetes da regra de estilo à qual você deseja adicionar a declaração.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-226">In the **Styles** pane, choose between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="4ec6e-227">O cursor se concentra, permitindo que você insira texto.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-227">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="4ec6e-228">Insira um nome de propriedade e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4ec6e-228">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="4ec6e-229">Insira um valor válido para essa propriedade e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4ec6e-229">Enter a valid value for that property and select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Adicionar uma declaração a uma regra de estilo" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   <span data-ttu-id="4ec6e-231">Adicionar a `border-bottom-style:groove` declaração a uma regra de estilo</span><span class="sxs-lookup"><span data-stu-id="4ec6e-231">Add the `border-bottom-style:groove` declaration to a style rule</span></span>  
:::image-end:::  

### <a name="change-a-declaration-name-or-value"></a><span data-ttu-id="4ec6e-232">Alterar um nome ou valor de declaração</span><span class="sxs-lookup"><span data-stu-id="4ec6e-232">Change a declaration name or value</span></span>  

<span data-ttu-id="4ec6e-233">Escolha e edite o nome ou o valor de uma declaração para alterá-la.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-233">Choose and edit the name or value of a declaration to change it.</span></span>  <span data-ttu-id="4ec6e-234">Para atalhos para incrementar ou decrementar rapidamente um valor por , , ou unidades, navegue até Alterar valores de declaração `0.1` `1` com `10` `100` [atalhos de teclado](#change-declaration-values-with-keyboard-shortcuts).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-234">For shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units, navigate to [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts).</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Alterando o valor de uma declaração" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   <span data-ttu-id="4ec6e-236">Alterar o valor da `border-bottom-style` declaração</span><span class="sxs-lookup"><span data-stu-id="4ec6e-236">Change the value of the `border-bottom-style` declaration</span></span>  
:::image-end:::  

### <a name="change-declaration-values-with-keyboard-shortcuts"></a><span data-ttu-id="4ec6e-237">Alterar valores de declaração com atalhos de teclado</span><span class="sxs-lookup"><span data-stu-id="4ec6e-237">Change declaration values with keyboard shortcuts</span></span>  

<span data-ttu-id="4ec6e-238">Ao editar o valor de uma declaração, você pode usar os atalhos de teclado a seguir para incrementar o valor por uma quantidade específica.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-238">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a specific amount.</span></span>  

*   <span data-ttu-id="4ec6e-239">Selecione `Alt` + `Up` \(Windows, Linux\) `Option` + `Up` ou \(macOS\) para incrementar `0.1` por .</span><span class="sxs-lookup"><span data-stu-id="4ec6e-239">Select `Alt`+`Up` \(Windows, Linux\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="4ec6e-240">Selecione `Up` para alterar o valor por , ou se o valor atual estiver entre e `1` `0.1` `-1` `1` .</span><span class="sxs-lookup"><span data-stu-id="4ec6e-240">Select `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="4ec6e-241">Selecione `Shift` + `Up` para incrementar `10` por .</span><span class="sxs-lookup"><span data-stu-id="4ec6e-241">Select `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="4ec6e-242">Selecione `Shift` + `Page Up` \(Windows, Linux\) `Shift` + `Command` + `Up` ou \(macOS\) para incrementar o valor em `100` .</span><span class="sxs-lookup"><span data-stu-id="4ec6e-242">Select `Shift`+`Page Up` \(Windows, Linux\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="4ec6e-243">A decrementação também funciona.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-243">Decrementing also works.</span></span>  <span data-ttu-id="4ec6e-244">Basta substituir cada instância mencionada `Up` acima por `Down` .</span><span class="sxs-lookup"><span data-stu-id="4ec6e-244">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <a name="add-a-class-to-an-element"></a><span data-ttu-id="4ec6e-245">Adicionar uma classe a um elemento</span><span class="sxs-lookup"><span data-stu-id="4ec6e-245">Add a class to an element</span></span>  

<span data-ttu-id="4ec6e-246">Conclua as seguintes ações para adicionar uma classe a um elemento.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-246">Complete the following actions to add a class to an element.</span></span>  

1.  <span data-ttu-id="4ec6e-247">[Selecione o elemento](#choose-an-element) na Árvore **DOM**.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-247">[Select the element](#choose-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="4ec6e-248">Escolha **.cls**.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-248">Choose **.cls**.</span></span>  
1.  <span data-ttu-id="4ec6e-249">Insira o nome da classe na caixa **de texto Adicionar Nova** Classe.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-249">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="4ec6e-250">Selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4ec6e-250">Select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="O painel Classes de Elemento" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   <span data-ttu-id="4ec6e-252">O **painel Classes de** Elemento</span><span class="sxs-lookup"><span data-stu-id="4ec6e-252">The **Element Classes** pane</span></span>  
:::image-end:::  

### <a name="toggle-a-class"></a><span data-ttu-id="4ec6e-253">Alternar uma classe</span><span class="sxs-lookup"><span data-stu-id="4ec6e-253">Toggle a class</span></span>  

<span data-ttu-id="4ec6e-254">Conclua as seguintes ações para habilitar ou desabilitar uma classe em um elemento.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-254">Complete the following actions to enable or disable a class on an element.</span></span>  

1.  <span data-ttu-id="4ec6e-255">[Selecione o elemento](#choose-an-element) na Árvore **DOM**.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-255">[Select the element](#choose-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="4ec6e-256">Abra o **painel Classes de** Elemento.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-256">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="4ec6e-257">Navegue [até Adicionar uma classe a um elemento](#add-a-class-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-257">Navigate to [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="4ec6e-258">Abaixo da **caixa de texto** Adicionar Nova Classe estão todas as classes aplicadas ao elemento específico.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-258">Below the **Add New Class** text box are all of the classes applied to the specific element.</span></span>  
1.  <span data-ttu-id="4ec6e-259">Alterne a caixa de seleção ao lado da classe que você deseja ativar ou desativar.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-259">Toggle the checkbox next to the class that you want to turn on or off.</span></span>  

### <a name="add-a-style-rule"></a><span data-ttu-id="4ec6e-260">Adicionar uma regra de estilo</span><span class="sxs-lookup"><span data-stu-id="4ec6e-260">Add a style rule</span></span>  

<span data-ttu-id="4ec6e-261">Conclua as seguintes ações para adicionar uma nova regra de estilo.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-261">Complete the following actions to add a new style rule.</span></span>  

1.  <span data-ttu-id="4ec6e-262">[Selecione um elemento](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-262">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="4ec6e-263">Escolha **Nova Regra de Estilo** \( Nova Regra de Estilo ![ ][ImageNewStyleRuleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-263">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\).</span></span>  <span data-ttu-id="4ec6e-264">O DevTools insere uma nova regra abaixo da **regra element.style.**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-264">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="4ec6e-265">Na figura a seguir, DevTools adiciona a regra de estilo `h1.devsite-page-title` depois de escolher Nova Regra de **Estilo**.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-265">In the following figure, DevTools adds the `h1.devsite-page-title` style rule after you choose **New Style Rule**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Adicionar uma nova regra de estilo" lightbox="../media/css-elements-styles-style-new.msft.png":::
   <span data-ttu-id="4ec6e-267">Adicionar uma nova regra de estilo</span><span class="sxs-lookup"><span data-stu-id="4ec6e-267">Add a new style rule</span></span>  
:::image-end:::  

#### <a name="choose-which-stylesheet-to-add-a-rule-to"></a><span data-ttu-id="4ec6e-268">Escolha a qual folha de estilos adicionar uma regra</span><span class="sxs-lookup"><span data-stu-id="4ec6e-268">Choose which stylesheet to add a rule to</span></span>  

<span data-ttu-id="4ec6e-269">Ao [adicionar uma nova regra de](#add-a-style-rule)estilo, escolha e segure New Style **Rule** \( New Style Rule \) para escolher qual folha de estilos adicionar a regra ![ de ][ImageNewStyleRuleIcon] estilo.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-269">When [adding a new style rule](#add-a-style-rule), choose and hold **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) to choose which stylesheet to add the style rule to.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Escolha uma folha de estilos" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   <span data-ttu-id="4ec6e-271">Escolha uma folha de estilos</span><span class="sxs-lookup"><span data-stu-id="4ec6e-271">Choose a stylesheet</span></span>  
:::image-end:::  

#### <a name="add-a-style-rule-to-a-specific-location"></a><span data-ttu-id="4ec6e-272">Adicionar uma regra de estilo a um local específico</span><span class="sxs-lookup"><span data-stu-id="4ec6e-272">Add a style rule to a specific location</span></span>  

<span data-ttu-id="4ec6e-273">Conclua as seguintes ações para adicionar uma regra de estilo a um local específico no painel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-273">Complete the following actions to add a style rule to a specific location in the **Styles** panel.</span></span>  

1.  <span data-ttu-id="4ec6e-274">Passe o mouse na regra de estilo que está diretamente acima de onde você deseja adicionar sua nova regra de estilo.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-274">Hover on the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="4ec6e-275">[Revelar a **barra de ferramentas Mais Ações.** ](#reveal-the-more-actions-toolbar)</span><span class="sxs-lookup"><span data-stu-id="4ec6e-275">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="4ec6e-276">Escolha **Inserir Regra de Estilo abaixo** \( Inserir Regra de Estilo abaixo ícone ![ ][ImageNewStyleRuleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-276">Choose **Insert Style Rule Below** \(![Insert Style Rule Below icon][ImageNewStyleRuleIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Inserir regra de estilo abaixo" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **<span data-ttu-id="4ec6e-278">Inserir regra de estilo abaixo</span><span class="sxs-lookup"><span data-stu-id="4ec6e-278">Insert Style Rule Below</span></span>**  
:::image-end:::  

### <a name="reveal-the-more-actions-toolbar"></a><span data-ttu-id="4ec6e-279">Revelar a barra de ferramentas Mais Ações</span><span class="sxs-lookup"><span data-stu-id="4ec6e-279">Reveal the More Actions toolbar</span></span>  

<span data-ttu-id="4ec6e-280">A **barra de ferramentas** Mais Ações permite executar as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-280">The **More Actions** toolbar lets you perform the following actions.</span></span>  

*   <span data-ttu-id="4ec6e-281">Insira uma regra de estilo diretamente abaixo da que você está focado.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-281">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="4ec6e-282">Adicione uma `background-color` , , ou declaração à regra de estilo em que você está `color` `box-shadow` `text-shadow` focado.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-282">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="4ec6e-283">Conclua as seguintes ações para revelar a barra **de ferramentas Mais** Ações.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-283">Complete the following actions to reveal the **More Actions** toolbar.</span></span>  

1.  <span data-ttu-id="4ec6e-284">No painel **Estilos,** passe o mouse em uma regra de estilo.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-284">In the **Styles** panel, hover on a style rule.</span></span>  <span data-ttu-id="4ec6e-285">**Mais Ações** \( \) é revelado na parte inferior `...` direita da seção de regra de estilo.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-285">**More Actions** \(`...`\) is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="4ec6e-286">Na figura a seguir, passe o mouse na regra de estilo e Mais Ações será revelada no canto inferior direito `.header-holder.has-default-focus` da seção de regra de estilo. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4ec6e-286">In the following figure, hover on the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Revelar mais ações" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       <span data-ttu-id="4ec6e-288">Revelar **mais ações** \( `...` \)</span><span class="sxs-lookup"><span data-stu-id="4ec6e-288">Reveal **More Actions** \(`...`\)</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4ec6e-289">Passe o **mouse sobre Mais Ações** `...` \( \) para revelar as ações mencionadas acima.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-289">Hover on **More Actions** \(`...`\) to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="4ec6e-290">A **ação Inserir Regra de Estilo Abaixo** é revelada após passar o mouse sobre Mais **Ações**.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-290">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="A barra de ferramentas Mais Ações" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       <span data-ttu-id="4ec6e-292">A **barra de ferramentas Mais** Ações</span><span class="sxs-lookup"><span data-stu-id="4ec6e-292">The **More Actions** toolbar</span></span>  
    :::image-end:::  
    
### <a name="toggle-a-declaration"></a><span data-ttu-id="4ec6e-293">Alternar uma declaração</span><span class="sxs-lookup"><span data-stu-id="4ec6e-293">Toggle a declaration</span></span>  

<span data-ttu-id="4ec6e-294">Conclua as ações folllwoing para alternar uma única declaração em \(ou off\).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-294">Complete the folllwoing actions to toggle a single declaration on \(or off\).</span></span>  

1.  <span data-ttu-id="4ec6e-295">[Selecione um elemento](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-295">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="4ec6e-296">No painel **Estilos,** passe o mouse na regra que define a declaração.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-296">In the **Styles** pane, hover on the rule that defines the declaration.</span></span>  <span data-ttu-id="4ec6e-297">Uma caixa de seleção é exibida ao lado de cada declaração.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-297">A checkbox appears next to each declaration.</span></span>  
1.  <span data-ttu-id="4ec6e-298">Marque \(ou desmarcar\) a caixa de seleção ao lado da declaração.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-298">Check \(or uncheck\) the checkbox next to the declaration.</span></span>  <span data-ttu-id="4ec6e-299">Quando você desmarca uma declaração, o DevTools a cruza para indicar que ela não está mais ativa.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-299">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="4ec6e-300">Na figura a seguir, a propriedade do elemento selecionado no momento `margin-top` foi alternada.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-300">In the following figure, the `margin-top` property for the currently selected element has been toggled off.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Alternar uma declaração" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   <span data-ttu-id="4ec6e-302">Alternar uma declaração</span><span class="sxs-lookup"><span data-stu-id="4ec6e-302">Toggle a declaration</span></span>  
:::image-end:::  

### <a name="add-a-background-color-declaration"></a><span data-ttu-id="4ec6e-303">Adicionar uma declaração de cor de plano de fundo</span><span class="sxs-lookup"><span data-stu-id="4ec6e-303">Add a background-color declaration</span></span>  

<span data-ttu-id="4ec6e-304">Conclua as seguintes ações para adicionar `background-color` uma declaração a um elemento.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-304">Complete the following actions to add a `background-color` declaration to an element.</span></span>  

1.  <span data-ttu-id="4ec6e-305">Passe o mouse na regra de estilo à que você deseja `background-color` adicionar a declaração.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-305">Hover on the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="4ec6e-306">[Revelar a **barra de ferramentas Mais Ações.** ](#reveal-the-more-actions-toolbar)</span><span class="sxs-lookup"><span data-stu-id="4ec6e-306">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="4ec6e-307">Escolha **Adicionar Cor do Plano de** Fundo \( Adicionar ícone de cor de plano de fundo ![ ][ImageAddBackgroundColorIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-307">Choose **Add Background Color** \(![Add Background Color icon][ImageAddBackgroundColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Adicionar cor de plano de fundo" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **<span data-ttu-id="4ec6e-309">Adicionar cor de plano de fundo</span><span class="sxs-lookup"><span data-stu-id="4ec6e-309">Add Background Color</span></span>**  
:::image-end:::  

### <a name="add-a-color-declaration"></a><span data-ttu-id="4ec6e-310">Adicionar uma declaração de cor</span><span class="sxs-lookup"><span data-stu-id="4ec6e-310">Add a color declaration</span></span>  

<span data-ttu-id="4ec6e-311">Conclua as seguintes ações para adicionar `color` uma declaração a um elemento.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-311">Complete the following actions to add a `color` declaration to an element.</span></span>  

1.  <span data-ttu-id="4ec6e-312">Passe o mouse na regra de estilo à que você deseja `color` adicionar a declaração.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-312">Hover on the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="4ec6e-313">[Revelar a **barra de ferramentas Mais Ações.** ](#reveal-the-more-actions-toolbar)</span><span class="sxs-lookup"><span data-stu-id="4ec6e-313">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="4ec6e-314">Escolha **Adicionar Cor** \( Adicionar ícone de cor ![ ][ImageAddColorIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-314">Choose **Add Color** \(![Add Color icon][ImageAddColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Adicionar Cor" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **<span data-ttu-id="4ec6e-316">Adicionar Cor</span><span class="sxs-lookup"><span data-stu-id="4ec6e-316">Add Color</span></span>**  
:::image-end:::  

### <a name="add-a-box-shadow-declaration"></a><span data-ttu-id="4ec6e-317">Adicionar uma declaração de sombra de caixa</span><span class="sxs-lookup"><span data-stu-id="4ec6e-317">Add a box-shadow declaration</span></span>  

<span data-ttu-id="4ec6e-318">Conclua as seguintes ações para adicionar `box-shadow` uma declaração a um elemento.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-318">Complete the follwoing actions to add a `box-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="4ec6e-319">Passe o mouse na regra de estilo à que você deseja `box-shadow` adicionar a declaração.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-319">Hover on the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="4ec6e-320">[Revelar a **barra de ferramentas Mais Ações.** ](#reveal-the-more-actions-toolbar)</span><span class="sxs-lookup"><span data-stu-id="4ec6e-320">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="4ec6e-321">Escolha **Adicionar Sombra de Caixa** \( Adicionar ícone sombra de caixa ![ ][ImageAddBoxShadowIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-321">Choose **Add Box Shadow** \(![Add Box Shadow icon][ImageAddBoxShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Adicionar Sombra de Caixa" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **<span data-ttu-id="4ec6e-323">Adicionar Sombra de Caixa</span><span class="sxs-lookup"><span data-stu-id="4ec6e-323">Add Box Shadow</span></span>**  
:::image-end:::  

### <a name="add-a-text-shadow-declaration"></a><span data-ttu-id="4ec6e-324">Adicionar uma declaração de sombra de texto</span><span class="sxs-lookup"><span data-stu-id="4ec6e-324">Add a text-shadow declaration</span></span>  

<span data-ttu-id="4ec6e-325">Conclua as seguintes ações para adicionar `text-shadow` uma declaração a um elemento.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-325">Complete the following actions to add a `text-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="4ec6e-326">Passe o mouse na regra de estilo à que você deseja `text-shadow` adicionar a declaração.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-326">Hover on the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="4ec6e-327">[Revelar a **barra de ferramentas Mais Ações.** ](#reveal-the-more-actions-toolbar)</span><span class="sxs-lookup"><span data-stu-id="4ec6e-327">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="4ec6e-328">Escolha **Adicionar Sombra de Texto** \( Adicionar ícone sombra de texto ![ ][ImageAddTextShadowIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-328">Choose **Add Text Shadow** \(![Add Text Shadow icon][ImageAddTextShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Adicionar Sombra de Texto" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **<span data-ttu-id="4ec6e-330">Adicionar Sombra de Texto</span><span class="sxs-lookup"><span data-stu-id="4ec6e-330">Add Text Shadow</span></span>**  
:::image-end:::  

### <a name="change-colors-with-the-color-picker"></a><span data-ttu-id="4ec6e-331">Alterar cores com o Selador de Cores</span><span class="sxs-lookup"><span data-stu-id="4ec6e-331">Change colors with the Color Picker</span></span>  

<span data-ttu-id="4ec6e-332">O **Selador de** Cores fornece uma GUI para alterações `color` e `background-color` declarações.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-332">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="4ec6e-333">Conclua as seguintes ações para abrir o **Selador de Cores**.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-333">Complete the following actions to open the **Color Picker**.</span></span>  

1.  <span data-ttu-id="4ec6e-334">[Selecione um elemento](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-334">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="4ec6e-335">No painel **Estilos,** encontre `color` a declaração , ou semelhante que você deseja `background-color` alterar.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-335">In the **Styles** panel, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="4ec6e-336">À esquerda do valor , ou semelhante, há um pequeno `color` quadrado que é uma `background-color` visualização da cor.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-336">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="4ec6e-337">Na figura a seguir, o pequeno quadrado à esquerda `rgba(0, 0, 0, 0.7)` é uma visualização dessa cor.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-337">In the following figure, the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Visualização de cores" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       <span data-ttu-id="4ec6e-339">Visualização de cores</span><span class="sxs-lookup"><span data-stu-id="4ec6e-339">Color preview</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4ec6e-340">Escolha a visualização para abrir o **Selador de Cores**.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-340">Choose the preview to open the **Color Picker**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="O Se picker de cores" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       <span data-ttu-id="4ec6e-342">O **Se picker de cores**</span><span class="sxs-lookup"><span data-stu-id="4ec6e-342">The **Color Picker**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="4ec6e-343">A figura a seguir e os descries de lista de cada um dos elementos da interface do usuário do **Selador de Cores**.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-343">The following figure and list descries of each of the UI elements of the **Color Picker**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="O Seletor de Cores, anotado" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   <span data-ttu-id="4ec6e-345">O **Seletor de**Cores , anotado</span><span class="sxs-lookup"><span data-stu-id="4ec6e-345">The **Color Picker**, annotated</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      <span data-ttu-id="4ec6e-346">1</span><span class="sxs-lookup"><span data-stu-id="4ec6e-346">1</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="4ec6e-347">Sombreos</span><span class="sxs-lookup"><span data-stu-id="4ec6e-347">Shades</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="4ec6e-348">2</span><span class="sxs-lookup"><span data-stu-id="4ec6e-348">2</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="4ec6e-349">Conta-gotas</span><span class="sxs-lookup"><span data-stu-id="4ec6e-349">Eyedropper</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ec6e-350">Para obter mais informações, navegue até Amostra de uma cor da [página com o Conta-gotas](#sample-a-color-off-the-page-with-the-eyedropper).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-350">For more information, navigate to [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="4ec6e-351">3</span><span class="sxs-lookup"><span data-stu-id="4ec6e-351">3</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="4ec6e-352">Copiar para área de transferência</span><span class="sxs-lookup"><span data-stu-id="4ec6e-352">Copy To Clipboard</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ec6e-353">Copie o **Valor de Exibição** para sua área de transferência.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-353">Copy the **Display Value** to your clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="4ec6e-354">4</span><span class="sxs-lookup"><span data-stu-id="4ec6e-354">4</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="4ec6e-355">Valor de exibição</span><span class="sxs-lookup"><span data-stu-id="4ec6e-355">Display Value</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ec6e-356">A representação RGBA, HSLA ou Hex da cor.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-356">The RGBA, HSLA, or Hex representation of the color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="4ec6e-357">5</span><span class="sxs-lookup"><span data-stu-id="4ec6e-357">5</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="4ec6e-358">Paleta de Cores</span><span class="sxs-lookup"><span data-stu-id="4ec6e-358">Color Palette</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ec6e-359">Escolha um dos quadrados para alterar a cor para esse quadrado.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-359">Choose one of the squares to change the color to that square.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="4ec6e-360">6</span><span class="sxs-lookup"><span data-stu-id="4ec6e-360">6</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="4ec6e-361">Hue</span><span class="sxs-lookup"><span data-stu-id="4ec6e-361">Hue</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="4ec6e-362">7</span><span class="sxs-lookup"><span data-stu-id="4ec6e-362">7</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="4ec6e-363">Opacidade</span><span class="sxs-lookup"><span data-stu-id="4ec6e-363">Opacity</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="4ec6e-364">8</span><span class="sxs-lookup"><span data-stu-id="4ec6e-364">8</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="4ec6e-365">Alternador de valor de exibição</span><span class="sxs-lookup"><span data-stu-id="4ec6e-365">Display Value Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ec6e-366">Alterne entre as representações RGBA, HSLA e Hex da cor atual.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-366">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="4ec6e-367">9</span><span class="sxs-lookup"><span data-stu-id="4ec6e-367">9</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="4ec6e-368">Alternador de Paleta de Cores</span><span class="sxs-lookup"><span data-stu-id="4ec6e-368">Color Palette Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="4ec6e-369">Alterne entre a paleta [Design de Material,][MaterialDesignColorSystem]uma paleta personalizada ou uma paleta de cores de página.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-369">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="4ec6e-370">O DevTools gera a paleta de cores da página com base nas cores que ele encontra em suas folhas de estilo.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-370">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  
   :::column-end:::
:::row-end:::  

#### <a name="sample-a-color-off-the-page-with-the-eyedropper"></a><span data-ttu-id="4ec6e-371">Amostra de uma cor da página com o Conta-gotas</span><span class="sxs-lookup"><span data-stu-id="4ec6e-371">Sample a color off the page with the Eyedropper</span></span>  

<span data-ttu-id="4ec6e-372">Quando você abre o **Selador de**Cores, **o** Conta-gotas \( Conta-gotas ![ ][ImageEyedropperIcon] \) está em uso por padrão.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-372">When you open the **Color Picker**, the **Eyedropper** \(![Eyedropper][ImageEyedropperIcon]\) is on by default.</span></span>  <span data-ttu-id="4ec6e-373">Conclua as seguintes ações para alterar a cor selecionada para outra cor na página.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-373">Complete the following actions to change the selected color to some other color on the page.</span></span>  

1.  <span data-ttu-id="4ec6e-374">Passe o mouse sobre a cor de destino no viewport.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-374">Hover on the target color in the viewport.</span></span>  
1.  <span data-ttu-id="4ec6e-375">Escolha confirmar.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-375">Choose to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="4ec6e-376">Na figura a seguir, o **Selador** de Cores mostra um valor de cor atual `rgba(0,0,0,0.7)` de , que está próximo ao preto.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-376">In the following figure, the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="4ec6e-377">A cor específica deve mudar para a versão do preto que está realçada no viewport depois que você a escolheu.</span><span class="sxs-lookup"><span data-stu-id="4ec6e-377">The specific color should change to the version of black that is currently highlighted in the viewport after you chose it.</span></span>  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Usando o Conta-gotas" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       <span data-ttu-id="4ec6e-379">Usando o Conta-gotas</span><span class="sxs-lookup"><span data-stu-id="4ec6e-379">Using the Eyedropper</span></span>  
    :::image-end:::  
    
<!--todo:  add the section on the Angle clock section for What's New 88.  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4ec6e-380">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4ec6e-380">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddBackgroundColorIcon]: ../media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: ../media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: ../media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: ../media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: ../media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: ../media/select-an-element-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Executar comandos com o menu de comando Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCSSGetStarted]: ../css/index.md "Começar a exibir e alterar o css | Microsoft Docs"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Adicionar um pseudostate a uma classe - Começar a exibir e alterar o css | Microsoft Docs"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Exibir o CSS para um elemento - Começar a exibir e alterar o css | Microsoft Docs"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Forçar o Microsoft Edge DevTools no modo de visualização de impressão (tipo de mídia de impressão CSS) | Microsoft Docs"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Tornar um arquivo minificado acessível - Referência de Depuração de JavaScript | Microsoft Docs"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "O sistema de cores - Design de Material"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "O modelo de caixa | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Tipos de seletor - Especificidade | MDN"  

> [!NOTE]
> <span data-ttu-id="4ec6e-390">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4ec6e-390">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4ec6e-391">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/css/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="4ec6e-391">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4ec6e-393">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4ec6e-393">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  