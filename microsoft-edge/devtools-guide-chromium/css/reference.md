---
description: Descubra novos fluxos de trabalho para exibir e alterar CSS no Microsoft Edge DevTools.
title: Referência BITS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: a4c8d5ed7f3cf84f20b4b73531f871e17921b186
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125220"
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

# <span data-ttu-id="291ed-104">Referência CSS</span><span class="sxs-lookup"><span data-stu-id="291ed-104">CSS reference</span></span>  

<span data-ttu-id="291ed-105">Descubra novos fluxos de trabalho na seguinte referência abrangente dos recursos do Microsoft Edge DevTools relacionados à exibição e alteração da CSS.</span><span class="sxs-lookup"><span data-stu-id="291ed-105">Discover new workflows in the following comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="291ed-106">Confira [introdução e alterar CSS][DevToolsCSSGetStarted] para aprender as noções básicas.</span><span class="sxs-lookup"><span data-stu-id="291ed-106">See [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted] to learn the basics.</span></span>  

## <span data-ttu-id="291ed-107">Selecionar um elemento</span><span class="sxs-lookup"><span data-stu-id="291ed-107">Select an element</span></span>  

<span data-ttu-id="291ed-108">O painel **elementos** do devtools permite que você visualize ou altere a CSS de um elemento de cada vez.</span><span class="sxs-lookup"><span data-stu-id="291ed-108">The **Elements** panel of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="291ed-109">O elemento selecionado é realçado na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="291ed-109">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="291ed-110">Os estilos do elemento são mostrados no painel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="291ed-110">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="291ed-111">Consulte [Exibir o CSS de um elemento][DevToolsCSSGetStartedTutorial] para um tutorial.</span><span class="sxs-lookup"><span data-stu-id="291ed-111">See [View the CSS for an element][DevToolsCSSGetStartedTutorial] for a tutorial.</span></span>  

> [!NOTE]
> <span data-ttu-id="291ed-112">Na figura a seguir, o `h1` elemento que está realçado na **árvore DOM** é o elemento selecionado.</span><span class="sxs-lookup"><span data-stu-id="291ed-112">In the following figure, the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="291ed-113">À direita, os estilos do elemento são mostrados no painel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="291ed-113">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="291ed-114">À esquerda, o elemento é realçado na viewport, mas só porque o mouse está passando no momento sobre ele na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="291ed-114">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-h1.msft.png":::
   <span data-ttu-id="291ed-116">Um exemplo de um elemento selecionado</span><span class="sxs-lookup"><span data-stu-id="291ed-116">An example of a selected element</span></span>  
:::image-end:::  

<span data-ttu-id="291ed-117">Use uma das ações a seguir para selecionar um elemento.</span><span class="sxs-lookup"><span data-stu-id="291ed-117">Use one the following actions to select an element.</span></span>  

*   <span data-ttu-id="291ed-118">No seu visor, passe o cursor do mouse sobre o elemento, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="291ed-118">In your viewport, hover on the element, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
*   <span data-ttu-id="291ed-119">No devtools, escolha **selecionar um elemento** \ ( ![ Selecione um elemento ][ImageSelectAnElementIcon] \) ou selecionar `Control` + `Shift` + `C` \ (Windows, Linux \) ou `Command` + `Shift` + `C` \ (MacOS \) e, em seguida, escolha o elemento no visor.</span><span class="sxs-lookup"><span data-stu-id="291ed-119">In DevTools, choose **Select an element** \(![Select an element][ImageSelectAnElementIcon]\) or select `Control`+`Shift`+`C` \(Windows, Linux\) or `Command`+`Shift`+`C` \(macOS\), and then choose the element in the viewport.</span></span>  
*   <span data-ttu-id="291ed-120">No DevTools, escolha o elemento na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="291ed-120">In DevTools, choose the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="291ed-121">No DevTools, execute uma consulta como `document.querySelector('p')` no **console**, passe o cursor do mouse sobre o resultado, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **revelar no painel de elementos**.</span><span class="sxs-lookup"><span data-stu-id="291ed-121">In DevTools, run a query like `document.querySelector('p')` in the **Console**, hover on the result, open the contextual menu \(right-click\), and choose **Reveal in Elements panel**.</span></span>  

## <span data-ttu-id="291ed-122">Exibir CSS</span><span class="sxs-lookup"><span data-stu-id="291ed-122">View CSS</span></span>  

### <span data-ttu-id="291ed-123">Exibir a folha de estilos externa na qual uma regra está definida</span><span class="sxs-lookup"><span data-stu-id="291ed-123">View the external stylesheet where a rule is defined</span></span>  

<span data-ttu-id="291ed-124">No painel **estilos** , escolha o link ao lado de uma regra CSS para abrir a folha de estilos externa que define a regra.</span><span class="sxs-lookup"><span data-stu-id="291ed-124">In the **Styles** pane, choose the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  

<span data-ttu-id="291ed-125">Se a folha de estilos for minified, navegue para [deixar um arquivo do minified legível][DevToolsJavascriptReferenceFormat].</span><span class="sxs-lookup"><span data-stu-id="291ed-125">If the stylesheet is minified, navigate to [Make a minified file readable][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="291ed-126">Na figura a seguir, depois de escolher `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` você será levado para a linha 2 de `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , onde a `.content h1:first-of-type` regra CSS é definida.</span><span class="sxs-lookup"><span data-stu-id="291ed-126">In the following figure, after you choose `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` you are taken to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  <span data-ttu-id="291ed-128">Exibir a folha de estilos onde uma regra está definida</span><span class="sxs-lookup"><span data-stu-id="291ed-128">Viewing the stylesheet where a rule is defined</span></span>  
:::image-end:::  

### <span data-ttu-id="291ed-129">Exibir apenas a CSS que é realmente aplicada a um elemento</span><span class="sxs-lookup"><span data-stu-id="291ed-129">View only the CSS that is actually applied to an element</span></span>  

<span data-ttu-id="291ed-130">A guia **estilos** mostra todas as regras que se aplicam a um elemento, incluindo declarações que foram substituídas.</span><span class="sxs-lookup"><span data-stu-id="291ed-130">The **Styles** tab shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="291ed-131">Quando você não está interessado em declarações substituídas, use a guia **calculada** para exibir apenas a CSS que está realmente sendo aplicada a um elemento.</span><span class="sxs-lookup"><span data-stu-id="291ed-131">When you are not interested in overridden declarations, use the **Computed** tab to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="291ed-132">[Selecione um elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="291ed-132">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="291ed-133">Vá para a guia **calculada** no painel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="291ed-133">Go to the **Computed** tab in the **Elements** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="291ed-134">Em uma ampla janela do DevTools, a guia **calculada** não existe.</span><span class="sxs-lookup"><span data-stu-id="291ed-134">On a wide DevTools window, the **Computed** tab does not exist.</span></span>  <span data-ttu-id="291ed-135">O conteúdo da guia **calculada** é mostrado na guia **estilos** .</span><span class="sxs-lookup"><span data-stu-id="291ed-135">The contents of the **Computed** tab are shown on the **Styles** tab.</span></span>  

<span data-ttu-id="291ed-136">As propriedades herdadas são opacas.</span><span class="sxs-lookup"><span data-stu-id="291ed-136">Inherited properties are opaque.</span></span>  <span data-ttu-id="291ed-137">Marque a caixa de seleção **Mostrar tudo** para ver todos os valores herdados.</span><span class="sxs-lookup"><span data-stu-id="291ed-137">Check the **Show All** checkbox to see all inherited values.</span></span>  

> [!NOTE]
> <span data-ttu-id="291ed-138">Na figura a seguir, a guia **calculada** mostra as propriedades CSS aplicadas ao elemento atualmente selecionado `h1` .</span><span class="sxs-lookup"><span data-stu-id="291ed-138">In the following figure, the **Computed** tab shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-computed-h1.msft.png":::
   <span data-ttu-id="291ed-140">A guia **calculada**</span><span class="sxs-lookup"><span data-stu-id="291ed-140">The **Computed** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="291ed-141">Exibir as propriedades CSS em ordem alfabética</span><span class="sxs-lookup"><span data-stu-id="291ed-141">View CSS properties in alphabetical order</span></span>  

<span data-ttu-id="291ed-142">Use a guia **calculada** .  Consulte [exibir apenas a CSS que é realmente aplicada a um elemento](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="291ed-142">Use the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="291ed-143">Exibir Propriedades CSS herdadas</span><span class="sxs-lookup"><span data-stu-id="291ed-143">View inherited CSS properties</span></span>  

<span data-ttu-id="291ed-144">Marque a caixa de seleção **Mostrar tudo** na guia **calculada** .  Consulte [exibir apenas a CSS que é realmente aplicada a um elemento](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="291ed-144">Check the **Show All** checkbox in the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="291ed-145">Exibir o modelo de caixa para um elemento</span><span class="sxs-lookup"><span data-stu-id="291ed-145">View the box model for an element</span></span>  

<span data-ttu-id="291ed-146">Para exibir [o modelo de caixa][MDNBoxModel] de um elemento, acesse a guia **estilos** .  Se a janela do DevTools for restrita, o diagrama de **modelo de caixa** estará na parte inferior da guia.</span><span class="sxs-lookup"><span data-stu-id="291ed-146">To view [the box model][MDNBoxModel] of an element, go to the **Styles** tab.  If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the tab.</span></span>  

<span data-ttu-id="291ed-147">Escolha e edite um valor para alterar um valor.</span><span class="sxs-lookup"><span data-stu-id="291ed-147">Choose and edit on a value to change a value.</span></span>  

> [!NOTE]
> <span data-ttu-id="291ed-148">Na figura a seguir, o diagrama de **modelo de caixa** na guia **estilos** mostra o modelo de caixa do elemento atualmente selecionado `h1` .</span><span class="sxs-lookup"><span data-stu-id="291ed-148">In the following figure, the **Box Model** diagram in the **Styles** tab shows the box model for the currently selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   <span data-ttu-id="291ed-150">O diagrama de **modelo de caixa**</span><span class="sxs-lookup"><span data-stu-id="291ed-150">The **Box Model** diagram</span></span>  
:::image-end:::  

### <span data-ttu-id="291ed-151">Pesquisar e filtrar a CSS de um elemento</span><span class="sxs-lookup"><span data-stu-id="291ed-151">Search and filter the CSS of an element</span></span>  

<span data-ttu-id="291ed-152">Use a caixa de texto **Filtrar** nas guias **estilos** e **calculados** para pesquisar valores ou propriedades CSS específicas.</span><span class="sxs-lookup"><span data-stu-id="291ed-152">Use the **Filter** text box on the **Styles** and **Computed** tabs to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="291ed-153">Para pesquisar também as propriedades herdadas na guia **calculada** , marque a caixa de seleção **Mostrar tudo** .</span><span class="sxs-lookup"><span data-stu-id="291ed-153">To also search inherited properties in the **Computed** tab, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="291ed-154">Na figura a seguir, a guia **estilos** é filtrada para mostrar apenas as regras que incluem a consulta de pesquisa `color` .</span><span class="sxs-lookup"><span data-stu-id="291ed-154">In the following figure, the **Styles** tab is filtered to only show rules that include the search query `color`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   <span data-ttu-id="291ed-156">Filtrar a guia **estilos**</span><span class="sxs-lookup"><span data-stu-id="291ed-156">Filter the **Styles** tab</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="291ed-157">Na figura a seguir, a guia **calculada** é filtrada para mostrar somente declarações que incluam a consulta de pesquisa `100%` .</span><span class="sxs-lookup"><span data-stu-id="291ed-157">In the following figure, the **Computed** tab is filtered to only show declarations that include the search query `100%`.</span></span>  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   <span data-ttu-id="291ed-159">Filtrar a guia **calculada**</span><span class="sxs-lookup"><span data-stu-id="291ed-159">Filter the **Computed** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="291ed-160">Alternar uma pseudo-classe</span><span class="sxs-lookup"><span data-stu-id="291ed-160">Toggle a pseudo-class</span></span>  

<span data-ttu-id="291ed-161">Conclua as ações a seguir para alternar uma pseudoclasse como `:active` , `:focus` , `:hover` ou `:visited` .</span><span class="sxs-lookup"><span data-stu-id="291ed-161">Complete the following actions to toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`.</span></span>  

1.  <span data-ttu-id="291ed-162">[Selecione um elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="291ed-162">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="291ed-163">No painel **elementos** , vá para a guia **estilos** .</span><span class="sxs-lookup"><span data-stu-id="291ed-163">On the **Elements** panel, go to the **Styles** tab.</span></span>  
1.  <span data-ttu-id="291ed-164">Escolha **: Hov**.</span><span class="sxs-lookup"><span data-stu-id="291ed-164">Choose **:hov**.</span></span>  
1.  <span data-ttu-id="291ed-165">Verifique a pseudo-classe que você deseja habilitar.</span><span class="sxs-lookup"><span data-stu-id="291ed-165">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="291ed-166">Na figura a seguir, alterne a `:hover` pseudo-classe.</span><span class="sxs-lookup"><span data-stu-id="291ed-166">In the following figure, toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="291ed-167">Na viewport, verifique se a `background-color: cornflowerblue` declaração está sendo aplicada ao elemento, mesmo que o elemento não esteja realmente sendo focalizado.</span><span class="sxs-lookup"><span data-stu-id="291ed-167">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   <span data-ttu-id="291ed-169">Alternar a `:hover` pseudo-classe</span><span class="sxs-lookup"><span data-stu-id="291ed-169">Toggle the `:hover` pseudo-class</span></span>  
:::image-end:::  

<span data-ttu-id="291ed-170">Para obter um tutorial interativo, navegue para [Adicionar um pseudo-estado a uma classe][DevToolsCSSGetStartedAddPseudoState].</span><span class="sxs-lookup"><span data-stu-id="291ed-170">For an interactive tutorial, navigate to [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState].</span></span>  

### <span data-ttu-id="291ed-171">Exibir uma página no modo de impressão</span><span class="sxs-lookup"><span data-stu-id="291ed-171">View a page in print mode</span></span>  

<span data-ttu-id="291ed-172">Conclua as ações a seguir para exibir uma página no modo de impressão.</span><span class="sxs-lookup"><span data-stu-id="291ed-172">Complete the following actions to view a page in print mode.</span></span>  

1.  <span data-ttu-id="291ed-173">[Abrir o menu de comandos][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="291ed-173">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="291ed-174">Comece a digitar `Rendering` e selecione `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="291ed-174">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="291ed-175">Para o menu suspenso **emular CSS Media** , escolha **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="291ed-175">For the **Emulate CSS Media** dropdown, choose **print**.</span></span>  

### <span data-ttu-id="291ed-176">Exibir CSS usado e não usado com a guia cobertura</span><span class="sxs-lookup"><span data-stu-id="291ed-176">View used and unused CSS with the Coverage tab</span></span>  

<span data-ttu-id="291ed-177">A guia cobertura mostra a CSS que uma página realmente usa.</span><span class="sxs-lookup"><span data-stu-id="291ed-177">The Coverage tab shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="291ed-178">Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) enquanto o devtools estiver em foco para [abrir o menu de comando][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="291ed-178">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to [open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="291ed-179">Comece a digitar `coverage` e escolha **Mostrar cobertura**.</span><span class="sxs-lookup"><span data-stu-id="291ed-179">Start typing `coverage` and choose **Show Coverage**.</span></span>  <span data-ttu-id="291ed-180">A guia cobertura é exibida.</span><span class="sxs-lookup"><span data-stu-id="291ed-180">The Coverage tab appears.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             <span data-ttu-id="291ed-182">Abrir a guia **cobertura** no **menu comando**</span><span class="sxs-lookup"><span data-stu-id="291ed-182">Open the **Coverage** tab from the **Command Menu**</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             <span data-ttu-id="291ed-184">A guia **cobertura**</span><span class="sxs-lookup"><span data-stu-id="291ed-184">The **Coverage** tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="291ed-185">Escolha **Iniciar cobertura de instrumentação e atualize a página** \ ( ![ Iniciar cobertura de instrumentação e atualizar a página ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="291ed-185">Choose **Start instrumenting coverage and refresh the page** \(![Start instrumenting coverage and refresh the page][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="291ed-186">A página é atualizada e a guia cobertura fornece uma visão geral de quanto o CSS \ (e JavaScript \) é usado em cada arquivo que o navegador carrega.</span><span class="sxs-lookup"><span data-stu-id="291ed-186">The page refreshes and the Coverage tab provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="291ed-187">Verde representa a CSS usada.</span><span class="sxs-lookup"><span data-stu-id="291ed-187">Green represents used CSS.</span></span>  <span data-ttu-id="291ed-188">Vermelho representa a CSS não usada.</span><span class="sxs-lookup"><span data-stu-id="291ed-188">Red represents unused CSS.</span></span>  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       <span data-ttu-id="291ed-190">Uma visão geral do quanto o CSS \ (e JavaScript \) é usado e não é usado</span><span class="sxs-lookup"><span data-stu-id="291ed-190">An overview of how much CSS \(and JavaScript\) is used and unused</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="291ed-191">Escolha um arquivo CSS para ver uma divisão linha por linha de qual CSS ele usa.</span><span class="sxs-lookup"><span data-stu-id="291ed-191">Choose a CSS file to see a line-by-line breakdown of what CSS it uses.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="291ed-192">Na figura a seguir, as linhas 145 a 147 e 149 a 151 de `b66bc881.site-ltr.css` não são usadas, enquanto as linhas 163 para 166 são usadas.</span><span class="sxs-lookup"><span data-stu-id="291ed-192">In the following figure, lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-sources-css-coverage.msft.png":::
       <span data-ttu-id="291ed-194">Uma divisão linha por linha do CSS usado e não usado</span><span class="sxs-lookup"><span data-stu-id="291ed-194">A line-by-line breakdown of used and unused CSS</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="291ed-195">Modo de visualização de impressão forçado</span><span class="sxs-lookup"><span data-stu-id="291ed-195">Force print preview mode</span></span>  

<span data-ttu-id="291ed-196">Consulte [forçar devtools no modo de visualização de impressão][DevToolsCssPrintPreview].</span><span class="sxs-lookup"><span data-stu-id="291ed-196">See [Force DevTools into Print Preview mode][DevToolsCssPrintPreview].</span></span>  

## <span data-ttu-id="291ed-197">Alterar CSS</span><span class="sxs-lookup"><span data-stu-id="291ed-197">Change CSS</span></span>  

<!-- todo s/CSS declaration/declaration/ -->  

### <span data-ttu-id="291ed-198">Adicionar uma declaração CSS a um elemento</span><span class="sxs-lookup"><span data-stu-id="291ed-198">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="291ed-199">A ordem das declarações afeta a forma como um elemento é estilizado, use a lista a seguir para ajudá-lo a adicionar declarações de maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="291ed-199">The order of declarations affects how an element is styled, use the following list to help you add declarations in different ways.</span></span>  

*   <span data-ttu-id="291ed-200">[Adicione uma declaração embutida](#add-an-inline-declaration).</span><span class="sxs-lookup"><span data-stu-id="291ed-200">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="291ed-201">Equivalente a adicionar um `style` atributo ao HTML de um elemento.</span><span class="sxs-lookup"><span data-stu-id="291ed-201">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="291ed-202">[Adicione uma declaração a uma regra de estilo](#add-a-declaration-to-a-style-rule).</span><span class="sxs-lookup"><span data-stu-id="291ed-202">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="291ed-203">Que fluxo de trabalho você deve usar?</span><span class="sxs-lookup"><span data-stu-id="291ed-203">What workflow should you use?</span></span>** <span data-ttu-id="291ed-204">Para a maioria dos cenários, você provavelmente deseja usar o fluxo de trabalho da declaração embutida.</span><span class="sxs-lookup"><span data-stu-id="291ed-204">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="291ed-205">As declarações embutidas têm uma prioridade mais alta do que as externas, portanto, o fluxo de trabalho embutido garante que as alterações entrem em vigor no elemento esperado.</span><span class="sxs-lookup"><span data-stu-id="291ed-205">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in your expected element.</span></span>  <span data-ttu-id="291ed-206">Para obter mais informações sobre a específicaidade, navegue até [tipos de seletor][MDNSelectorTypes].</span><span class="sxs-lookup"><span data-stu-id="291ed-206">For more information about specificity, navigate to [Selector Types][MDNSelectorTypes].</span></span>  

<span data-ttu-id="291ed-207">Se você estiver Depurando qualquer estilo do elemento e precisar testar especificamente o que acontece quando uma declaração é definida em locais diferentes, use o outro fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="291ed-207">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <span data-ttu-id="291ed-208">Adicionar uma declaração embutida</span><span class="sxs-lookup"><span data-stu-id="291ed-208">Add an inline declaration</span></span>  

<span data-ttu-id="291ed-209">Conclua as ações a seguir para adicionar uma declaração embutida.</span><span class="sxs-lookup"><span data-stu-id="291ed-209">Complete the following actions to add an inline declaration.</span></span>  

1.  <span data-ttu-id="291ed-210">[Selecione um elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="291ed-210">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="291ed-211">No painel **estilos** , escolha entre os colchetes da seção **elemento. Style** .</span><span class="sxs-lookup"><span data-stu-id="291ed-211">In the **Styles** pane, choose between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="291ed-212">O cursor se concentra, permitindo que você insira texto.</span><span class="sxs-lookup"><span data-stu-id="291ed-212">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="291ed-213">Insira um nome de propriedade e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="291ed-213">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="291ed-214">Insira um valor válido para essa propriedade e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="291ed-214">Enter a valid value for that property and select `Enter`.</span></span>  <span data-ttu-id="291ed-215">Na **árvore DOM**, verifique se um `style` atributo foi adicionado ao elemento.</span><span class="sxs-lookup"><span data-stu-id="291ed-215">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="291ed-216">Na figura a seguir, as `margin-top` Propriedades e foram `background-color` aplicadas ao elemento selecionado.</span><span class="sxs-lookup"><span data-stu-id="291ed-216">In the following figure, the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="291ed-217">Na **árvore DOM** , verifique se as declarações são refletidas no `style` atributo para um elemento.</span><span class="sxs-lookup"><span data-stu-id="291ed-217">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   <span data-ttu-id="291ed-219">Adicionar declarações embutidas</span><span class="sxs-lookup"><span data-stu-id="291ed-219">Add inline declarations</span></span>  
:::image-end:::  

#### <span data-ttu-id="291ed-220">Adicionar uma declaração a uma regra de estilo</span><span class="sxs-lookup"><span data-stu-id="291ed-220">Add a declaration to a style rule</span></span>  

<span data-ttu-id="291ed-221">Conclua as ações a seguir para adicionar uma declaração a uma regra de estilo existente.</span><span class="sxs-lookup"><span data-stu-id="291ed-221">Complete the following actions to add a declaration to an existing style rule.</span></span>  

1.  <span data-ttu-id="291ed-222">[Selecione um elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="291ed-222">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="291ed-223">No painel **estilos** , escolha entre os colchetes da regra de estilo à qual você deseja adicionar a declaração.</span><span class="sxs-lookup"><span data-stu-id="291ed-223">In the **Styles** pane, choose between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="291ed-224">O cursor se concentra, permitindo que você insira texto.</span><span class="sxs-lookup"><span data-stu-id="291ed-224">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="291ed-225">Insira um nome de propriedade e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="291ed-225">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="291ed-226">Insira um valor válido para essa propriedade e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="291ed-226">Enter a valid value for that property and select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   <span data-ttu-id="291ed-228">Adicionar a `border-bottom-style:groove` declaração a uma regra de estilo</span><span class="sxs-lookup"><span data-stu-id="291ed-228">Add the `border-bottom-style:groove` declaration to a style rule</span></span>  
:::image-end:::  

### <span data-ttu-id="291ed-229">Alterar um nome ou valor de declaração</span><span class="sxs-lookup"><span data-stu-id="291ed-229">Change a declaration name or value</span></span>  

<span data-ttu-id="291ed-230">Escolha e edite o nome ou o valor de uma declaração para alterá-la.</span><span class="sxs-lookup"><span data-stu-id="291ed-230">Choose and edit the name or value of a declaration to change it.</span></span>  <span data-ttu-id="291ed-231">Consulte [alterar valores de declaração com atalhos de teclado](#change-declaration-values-with-keyboard-shortcuts) para atalhos para incrementar ou decrementar rapidamente um valor por `0.1` ,, `1` `10` ou `100` unidades.</span><span class="sxs-lookup"><span data-stu-id="291ed-231">See [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts) for shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   <span data-ttu-id="291ed-233">Alterar o valor da `border-bottom-style` declaração</span><span class="sxs-lookup"><span data-stu-id="291ed-233">Change the value of the `border-bottom-style` declaration</span></span>  
:::image-end:::  

### <span data-ttu-id="291ed-234">Alterar valores de declaração com atalhos de teclado</span><span class="sxs-lookup"><span data-stu-id="291ed-234">Change declaration values with keyboard shortcuts</span></span>  

<span data-ttu-id="291ed-235">Durante a edição do valor de uma declaração, você pode usar os seguintes atalhos de teclado para incrementar o valor por uma quantia específica.</span><span class="sxs-lookup"><span data-stu-id="291ed-235">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a specific amount.</span></span>  

*   <span data-ttu-id="291ed-236">Selecione `Alt` + `Up` \ (Windows, Linux \) ou `Option` + `Up` \ (MacOS \) para aumentar o incremento `0.1` .</span><span class="sxs-lookup"><span data-stu-id="291ed-236">Select `Alt`+`Up` \(Windows, Linux\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="291ed-237">Selecione `Up` para alterar o valor por `1` , ou `0.1` se o valor atual estiver entre `-1` e `1` .</span><span class="sxs-lookup"><span data-stu-id="291ed-237">Select `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="291ed-238">Selecione `Shift` + `Up` para aumentar o incremento `10` .</span><span class="sxs-lookup"><span data-stu-id="291ed-238">Select `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="291ed-239">Selecione `Shift` + `Page Up` \ (Windows, Linux \) ou `Shift` + `Command` + `Up` \ (MacOS \) para incrementar o valor por `100` .</span><span class="sxs-lookup"><span data-stu-id="291ed-239">Select `Shift`+`Page Up` \(Windows, Linux\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="291ed-240">O decréscimo também funciona.</span><span class="sxs-lookup"><span data-stu-id="291ed-240">Decrementing also works.</span></span>  <span data-ttu-id="291ed-241">Basta substituir cada ocorrência de `Up` mencionado acima por `Down` .</span><span class="sxs-lookup"><span data-stu-id="291ed-241">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <span data-ttu-id="291ed-242">Adicionar uma classe a um elemento</span><span class="sxs-lookup"><span data-stu-id="291ed-242">Add a class to an element</span></span>  

<span data-ttu-id="291ed-243">Conclua as ações a seguir para adicionar uma classe a um elemento.</span><span class="sxs-lookup"><span data-stu-id="291ed-243">Complete the following actions to add a class to an element.</span></span>  

1.  <span data-ttu-id="291ed-244">[Selecione o elemento](#select-an-element) na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="291ed-244">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="291ed-245">Choose **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="291ed-245">Choose **.cls**.</span></span>  
1.  <span data-ttu-id="291ed-246">Digite o nome da classe na caixa de texto **Adicionar nova classe** .</span><span class="sxs-lookup"><span data-stu-id="291ed-246">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="291ed-247">Selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="291ed-247">Select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   <span data-ttu-id="291ed-249">O painel **classes de elemento**</span><span class="sxs-lookup"><span data-stu-id="291ed-249">The **Element Classes** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="291ed-250">Alternar uma classe</span><span class="sxs-lookup"><span data-stu-id="291ed-250">Toggle a class</span></span>  

<span data-ttu-id="291ed-251">Conclua as ações a seguir para habilitar ou desabilitar uma classe em um elemento.</span><span class="sxs-lookup"><span data-stu-id="291ed-251">Complete the following actions to enable or disable a class on an element.</span></span>  

1.  <span data-ttu-id="291ed-252">[Selecione o elemento](#select-an-element) na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="291ed-252">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="291ed-253">Abrir o painel **classes de elementos** .</span><span class="sxs-lookup"><span data-stu-id="291ed-253">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="291ed-254">Consulte [Adicionar uma classe a um elemento](#add-a-class-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="291ed-254">See [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="291ed-255">Abaixo da caixa de texto **Adicionar nova classe** estão todas as classes que estão sendo aplicadas ao elemento específico.</span><span class="sxs-lookup"><span data-stu-id="291ed-255">Below the **Add New Class** text box are all of the classes that are being applied to the specific element.</span></span>  
1.  <span data-ttu-id="291ed-256">Alternar a caixa de seleção ao lado da classe que você deseja habilitar ou desabilitar.</span><span class="sxs-lookup"><span data-stu-id="291ed-256">Toggle the checkbox next to the class that you want to enable or disable.</span></span>  

### <span data-ttu-id="291ed-257">Adicionar uma regra de estilo</span><span class="sxs-lookup"><span data-stu-id="291ed-257">Add a style rule</span></span>  

<span data-ttu-id="291ed-258">Conclua as ações a seguir para adicionar uma nova regra de estilo.</span><span class="sxs-lookup"><span data-stu-id="291ed-258">Complete the following actions to add a new style rule.</span></span>  

1.  <span data-ttu-id="291ed-259">[Selecione um elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="291ed-259">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="291ed-260">Escolha **novo regra de estilo** \ ( ![ novo regra de estilo ][ImageNewStyleRuleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="291ed-260">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\).</span></span>  <span data-ttu-id="291ed-261">DevTools insere uma nova regra abaixo da regra **elemento. Style** .</span><span class="sxs-lookup"><span data-stu-id="291ed-261">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="291ed-262">Na figura a seguir, o DevTools adiciona a `h1.devsite-page-title` regra de estilo depois que você escolhe **nova regra de estilo**.</span><span class="sxs-lookup"><span data-stu-id="291ed-262">In the following figure, DevTools adds the `h1.devsite-page-title` style rule after you choose **New Style Rule**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-style-new.msft.png":::
   <span data-ttu-id="291ed-264">Adicionar uma nova regra de estilo</span><span class="sxs-lookup"><span data-stu-id="291ed-264">Add a new style rule</span></span>  
:::image-end:::  

#### <span data-ttu-id="291ed-265">Escolha em qual folha de estilos você deseja adicionar uma regra</span><span class="sxs-lookup"><span data-stu-id="291ed-265">Choose which stylesheet to add a rule to</span></span>  

<span data-ttu-id="291ed-266">Ao [Adicionar uma nova regra de estilo](#add-a-style-rule), escolha e segure **nova regra de estilo** \ ( ![ nova regra de estilo ][ImageNewStyleRuleIcon] \) para escolher para qual folha de estilo adicionar a regra de estilo.</span><span class="sxs-lookup"><span data-stu-id="291ed-266">When [adding a new style rule](#add-a-style-rule), choose and hold **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) to choose which stylesheet to add the style rule to.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   <span data-ttu-id="291ed-268">Escolher uma folha de estilos</span><span class="sxs-lookup"><span data-stu-id="291ed-268">Choose a stylesheet</span></span>  
:::image-end:::  

#### <span data-ttu-id="291ed-269">Adicionar uma regra de estilo a um local específico</span><span class="sxs-lookup"><span data-stu-id="291ed-269">Add a style rule to a specific location</span></span>  

<span data-ttu-id="291ed-270">Conclua as ações a seguir para adicionar uma regra de estilo a um local específico na guia **estilos** .</span><span class="sxs-lookup"><span data-stu-id="291ed-270">Complete the following actions to add a style rule to a specific location in the **Styles** tab.</span></span>  

1.  <span data-ttu-id="291ed-271">Passe o mouse sobre a regra de estilo que está diretamente acima de onde você deseja adicionar sua nova regra de estilo.</span><span class="sxs-lookup"><span data-stu-id="291ed-271">Hover over the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="291ed-272">[Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="291ed-272">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="291ed-273">Escolha **Inserir regra de estilo abaixo** \ ( ![ Inserir regra de estilo abaixo do ícone ][ImageNewStyleRuleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="291ed-273">Choose **Insert Style Rule Below** \(![Insert Style Rule Below icon][ImageNewStyleRuleIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **<span data-ttu-id="291ed-275">Inserir regra de estilo abaixo</span><span class="sxs-lookup"><span data-stu-id="291ed-275">Insert Style Rule Below</span></span>**  
:::image-end:::  

### <span data-ttu-id="291ed-276">Revelar a barra de ferramentas mais ações</span><span class="sxs-lookup"><span data-stu-id="291ed-276">Reveal the More Actions toolbar</span></span>  

<span data-ttu-id="291ed-277">A barra de ferramentas **mais ações** permite executar as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="291ed-277">The **More Actions** toolbar lets you perform the following actions.</span></span>  

*   <span data-ttu-id="291ed-278">Insira uma regra de estilo diretamente abaixo da que você está focalizado.</span><span class="sxs-lookup"><span data-stu-id="291ed-278">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="291ed-279">Adicione uma `background-color` `color` declaração,, `box-shadow` ou `text-shadow` para a regra de estilo na qual você está focalizado.</span><span class="sxs-lookup"><span data-stu-id="291ed-279">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="291ed-280">Conclua as ações a seguir para revelar a barra de ferramentas **mais ações** .</span><span class="sxs-lookup"><span data-stu-id="291ed-280">Complete the following actions to reveal the **More Actions** toolbar.</span></span>  

1.  <span data-ttu-id="291ed-281">Na guia **estilos** , passe o mouse sobre uma regra de estilo.</span><span class="sxs-lookup"><span data-stu-id="291ed-281">In the **Styles** tab, hover over a style rule.</span></span>  <span data-ttu-id="291ed-282">**Mais ações** \ ( `...` \) são reveladas no canto inferior direito da seção de regra de estilo.</span><span class="sxs-lookup"><span data-stu-id="291ed-282">**More Actions** \(`...`\) is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="291ed-283">Na figura a seguir, passe o mouse sobre a `.header-holder.has-default-focus` regra de estilo e **mais ações** serão reveladas no canto inferior direito da seção de regra de estilo.</span><span class="sxs-lookup"><span data-stu-id="291ed-283">In the following figure, hover over the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       <span data-ttu-id="291ed-285">Revelar **mais ações** \ ( `...` \)</span><span class="sxs-lookup"><span data-stu-id="291ed-285">Reveal **More Actions** \(`...`\)</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="291ed-286">Passe o mouse sobre **mais ações** \ ( `...` \) para revelar as ações mencionadas acima.</span><span class="sxs-lookup"><span data-stu-id="291ed-286">Hover over **More Actions** \(`...`\) to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="291ed-287">A ação **Inserir regra de estilo abaixo** é revelada depois de passar o mouse sobre **mais ações**.</span><span class="sxs-lookup"><span data-stu-id="291ed-287">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       <span data-ttu-id="291ed-289">A barra de ferramentas **mais ações**</span><span class="sxs-lookup"><span data-stu-id="291ed-289">The **More Actions** toolbar</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="291ed-290">Alternar uma declaração</span><span class="sxs-lookup"><span data-stu-id="291ed-290">Toggle a declaration</span></span>  

<span data-ttu-id="291ed-291">Conclua as ações folllwoing para alternar uma única declaração em \ (ou off \).</span><span class="sxs-lookup"><span data-stu-id="291ed-291">Complete the folllwoing actions to toggle a single declaration on \(or off\).</span></span>  

1.  <span data-ttu-id="291ed-292">[Selecione um elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="291ed-292">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="291ed-293">No painel **estilos** , passe o mouse sobre a regra que define a declaração.</span><span class="sxs-lookup"><span data-stu-id="291ed-293">In the **Styles** pane, hover over the rule that defines the declaration.</span></span>  <span data-ttu-id="291ed-294">Uma caixa de seleção é exibida ao lado de cada declaração.</span><span class="sxs-lookup"><span data-stu-id="291ed-294">A checkbox appears next to each declaration.</span></span>  
1.  <span data-ttu-id="291ed-295">Marque \ (ou desmarque \) a caixa de seleção ao lado da declaração.</span><span class="sxs-lookup"><span data-stu-id="291ed-295">Check \(or uncheck\) the checkbox next to the declaration.</span></span>  <span data-ttu-id="291ed-296">Quando você desmarca uma declaração, o DevTools a risca para indicar que não está mais ativo.</span><span class="sxs-lookup"><span data-stu-id="291ed-296">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="291ed-297">Na figura a seguir, a `margin-top` Propriedade do elemento selecionado no momento foi desativada.</span><span class="sxs-lookup"><span data-stu-id="291ed-297">In the following figure, the `margin-top` property for the currently selected element has been toggled off.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   <span data-ttu-id="291ed-299">Alternar uma declaração</span><span class="sxs-lookup"><span data-stu-id="291ed-299">Toggle a declaration</span></span>  
:::image-end:::  

### <span data-ttu-id="291ed-300">Adicionar uma declaração de cor de plano de fundo</span><span class="sxs-lookup"><span data-stu-id="291ed-300">Add a background-color declaration</span></span>  

<span data-ttu-id="291ed-301">Conclua as ações a seguir para adicionar uma `background-color` declaração a um elemento.</span><span class="sxs-lookup"><span data-stu-id="291ed-301">Complete the following actions to add a `background-color` declaration to an element.</span></span>  

1.  <span data-ttu-id="291ed-302">Passe o mouse sobre a regra de estilo à qual você deseja adicionar a `background-color` declaração.</span><span class="sxs-lookup"><span data-stu-id="291ed-302">Hover over the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="291ed-303">[Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="291ed-303">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="291ed-304">Escolha **adicionar cor de plano de fundo** \ ( ![ ícone de cor da tela de fundo ][ImageAddBackgroundColorIcon] \).</span><span class="sxs-lookup"><span data-stu-id="291ed-304">Choose **Add Background Color** \(![Add Background Color icon][ImageAddBackgroundColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **<span data-ttu-id="291ed-306">Adicionar cor de plano de fundo</span><span class="sxs-lookup"><span data-stu-id="291ed-306">Add Background Color</span></span>**  
:::image-end:::  

### <span data-ttu-id="291ed-307">Adicionar uma declaração de cor</span><span class="sxs-lookup"><span data-stu-id="291ed-307">Add a color declaration</span></span>  

<span data-ttu-id="291ed-308">Conclua as ações a seguir para adicionar uma `color` declaração a um elemento.</span><span class="sxs-lookup"><span data-stu-id="291ed-308">Complete the following actions to add a `color` declaration to an element.</span></span>  

1.  <span data-ttu-id="291ed-309">Passe o mouse sobre a regra de estilo à qual você deseja adicionar a `color` declaração.</span><span class="sxs-lookup"><span data-stu-id="291ed-309">Hover over the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="291ed-310">[Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="291ed-310">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="291ed-311">Escolha **adicionar cor** \ ( ![ ícone Adicionar cor ][ImageAddColorIcon] \).</span><span class="sxs-lookup"><span data-stu-id="291ed-311">Choose **Add Color** \(![Add Color icon][ImageAddColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **<span data-ttu-id="291ed-313">Adicionar cor</span><span class="sxs-lookup"><span data-stu-id="291ed-313">Add Color</span></span>**  
:::image-end:::  

### <span data-ttu-id="291ed-314">Adicionar uma declaração de caixa-sombra</span><span class="sxs-lookup"><span data-stu-id="291ed-314">Add a box-shadow declaration</span></span>  

<span data-ttu-id="291ed-315">Conclua as ações a seguir para adicionar uma `box-shadow` declaração a um elemento.</span><span class="sxs-lookup"><span data-stu-id="291ed-315">Complete the follwoing actions to add a `box-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="291ed-316">Passe o mouse sobre a regra de estilo à qual você deseja adicionar a `box-shadow` declaração.</span><span class="sxs-lookup"><span data-stu-id="291ed-316">Hover over the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="291ed-317">[Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="291ed-317">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="291ed-318">Escolha **Adicionar sombra de caixa** \ ( ![ ícone de sombra Adicionar caixa ][ImageAddBoxShadowIcon] \).</span><span class="sxs-lookup"><span data-stu-id="291ed-318">Choose **Add Box Shadow** \(![Add Box Shadow icon][ImageAddBoxShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **<span data-ttu-id="291ed-320">Adicionar sombra à caixa</span><span class="sxs-lookup"><span data-stu-id="291ed-320">Add Box Shadow</span></span>**  
:::image-end:::  

### <span data-ttu-id="291ed-321">Adicionar uma declaração de sombra de texto</span><span class="sxs-lookup"><span data-stu-id="291ed-321">Add a text-shadow declaration</span></span>  

<span data-ttu-id="291ed-322">Conclua as ações a seguir para adicionar uma `text-shadow` declaração a um elemento.</span><span class="sxs-lookup"><span data-stu-id="291ed-322">Complete the following actions to add a `text-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="291ed-323">Passe o mouse sobre a regra de estilo à qual você deseja adicionar a `text-shadow` declaração.</span><span class="sxs-lookup"><span data-stu-id="291ed-323">Hover over the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="291ed-324">[Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="291ed-324">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="291ed-325">Escolha **Adicionar sombra de texto** \ ( ![ Adicionar ícone de sombra de texto ][ImageAddTextShadowIcon] \).</span><span class="sxs-lookup"><span data-stu-id="291ed-325">Choose **Add Text Shadow** \(![Add Text Shadow icon][ImageAddTextShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **<span data-ttu-id="291ed-327">Adicionar sombra de texto</span><span class="sxs-lookup"><span data-stu-id="291ed-327">Add Text Shadow</span></span>**  
:::image-end:::  

### <span data-ttu-id="291ed-328">Alterar as cores com o seletor de cores</span><span class="sxs-lookup"><span data-stu-id="291ed-328">Change colors with the Color Picker</span></span>  

<span data-ttu-id="291ed-329">O **seletor de cores** fornece uma GUI para alteração `color` e `background-color` declarações.</span><span class="sxs-lookup"><span data-stu-id="291ed-329">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="291ed-330">Conclua as seguintes ações para abrir o **seletor de cores**.</span><span class="sxs-lookup"><span data-stu-id="291ed-330">Complete the following actions to open the **Color Picker**.</span></span>  

1.  <span data-ttu-id="291ed-331">[Selecione um elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="291ed-331">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="291ed-332">Na guia **estilos** , localize a `color` declaração, `background-color` ou semelhante, que você deseja alterar.</span><span class="sxs-lookup"><span data-stu-id="291ed-332">In the **Styles** tab, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="291ed-333">À esquerda do `color` `background-color` valor, ou semelhante, há um quadrado pequeno que é uma visualização da cor.</span><span class="sxs-lookup"><span data-stu-id="291ed-333">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="291ed-334">Na figura a seguir, o pequeno quadrado à esquerda de `rgba(0, 0, 0, 0.7)` é uma visualização da cor.</span><span class="sxs-lookup"><span data-stu-id="291ed-334">In the following figure, the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       <span data-ttu-id="291ed-336">Visualização de cores</span><span class="sxs-lookup"><span data-stu-id="291ed-336">Color preview</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="291ed-337">Escolha a visualização para abrir o **seletor de cores**.</span><span class="sxs-lookup"><span data-stu-id="291ed-337">Choose the preview to open the **Color Picker**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       <span data-ttu-id="291ed-339">O **seletor de cores**</span><span class="sxs-lookup"><span data-stu-id="291ed-339">The **Color Picker**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="291ed-340">A figura a seguir e a lista descreve de cada um dos elementos da interface do usuário do **seletor de cores**.</span><span class="sxs-lookup"><span data-stu-id="291ed-340">The following figure and list descries of each of the UI elements of the **Color Picker**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   <span data-ttu-id="291ed-342">O **seletor de cores**, anotado</span><span class="sxs-lookup"><span data-stu-id="291ed-342">The **Color Picker**, annotated</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      <span data-ttu-id="291ed-343">um</span><span class="sxs-lookup"><span data-stu-id="291ed-343">1</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="291ed-344">Sombras</span><span class="sxs-lookup"><span data-stu-id="291ed-344">Shades</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="291ed-345">2</span><span class="sxs-lookup"><span data-stu-id="291ed-345">2</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="291ed-346">Ferramenta</span><span class="sxs-lookup"><span data-stu-id="291ed-346">Eyedropper</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="291ed-347">Para obter mais informações, navegue para obter [uma amostra de cor na página com o conta-gotas](#sample-a-color-off-the-page-with-the-eyedropper).</span><span class="sxs-lookup"><span data-stu-id="291ed-347">For more information, navigate to [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="291ed-348">3D</span><span class="sxs-lookup"><span data-stu-id="291ed-348">3</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="291ed-349">Copiar para área de transferência</span><span class="sxs-lookup"><span data-stu-id="291ed-349">Copy To Clipboard</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="291ed-350">Copie o **valor de exibição** para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="291ed-350">Copy the **Display Value** to your clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="291ed-351">4</span><span class="sxs-lookup"><span data-stu-id="291ed-351">4</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="291ed-352">Valor de exibição</span><span class="sxs-lookup"><span data-stu-id="291ed-352">Display Value</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="291ed-353">A representação RGBA, HSLA ou hexa da cor.</span><span class="sxs-lookup"><span data-stu-id="291ed-353">The RGBA, HSLA, or Hex representation of the color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="291ed-354">5</span><span class="sxs-lookup"><span data-stu-id="291ed-354">5</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="291ed-355">Paleta de cores</span><span class="sxs-lookup"><span data-stu-id="291ed-355">Color Palette</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="291ed-356">Escolha um dos quadrados para alterar a cor para esse quadrado.</span><span class="sxs-lookup"><span data-stu-id="291ed-356">Choose one of the squares to change the color to that square.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="291ed-357">5</span><span class="sxs-lookup"><span data-stu-id="291ed-357">6</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="291ed-358">Matiz</span><span class="sxs-lookup"><span data-stu-id="291ed-358">Hue</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="291ed-359">7</span><span class="sxs-lookup"><span data-stu-id="291ed-359">7</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="291ed-360">Opacidade</span><span class="sxs-lookup"><span data-stu-id="291ed-360">Opacity</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="291ed-361">08</span><span class="sxs-lookup"><span data-stu-id="291ed-361">8</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="291ed-362">Seletor de valor de exibição</span><span class="sxs-lookup"><span data-stu-id="291ed-362">Display Value Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="291ed-363">Alternar entre as representações de RGBA, HSLA e HexA da cor atual.</span><span class="sxs-lookup"><span data-stu-id="291ed-363">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="291ed-364">222</span><span class="sxs-lookup"><span data-stu-id="291ed-364">9</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="291ed-365">Seletor de paleta de cores</span><span class="sxs-lookup"><span data-stu-id="291ed-365">Color Palette Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="291ed-366">Alternar entre a [paleta de design de material][MaterialDesignColorSystem], uma paleta personalizada ou uma paleta de cores de página.</span><span class="sxs-lookup"><span data-stu-id="291ed-366">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="291ed-367">O DevTools gera a paleta de cores da página com base nas cores encontradas nas suas folhas de estilos.</span><span class="sxs-lookup"><span data-stu-id="291ed-367">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="291ed-368">Exemplo de uma cor para fora da página com o conta-gotas</span><span class="sxs-lookup"><span data-stu-id="291ed-368">Sample a color off the page with the Eyedropper</span></span>  

<span data-ttu-id="291ed-369">Quando você abre o **seletor de cores**, o **conta-gotas** \ ( ![ conta-gotas ][ImageEyedropperIcon] \) é ativado por padrão.</span><span class="sxs-lookup"><span data-stu-id="291ed-369">When you open the **Color Picker**, the **Eyedropper** \(![Eyedropper][ImageEyedropperIcon]\) is on by default.</span></span>  <span data-ttu-id="291ed-370">Conclua as ações a seguir para alterar a cor selecionada para outra cor na página.</span><span class="sxs-lookup"><span data-stu-id="291ed-370">Complete the following actions to change the selected color to some other color on the page.</span></span>  

1.  <span data-ttu-id="291ed-371">Passe o mouse sobre a cor de destino no visor.</span><span class="sxs-lookup"><span data-stu-id="291ed-371">Hover over the target color in the viewport.</span></span>  
1.  <span data-ttu-id="291ed-372">Escolha confirmar.</span><span class="sxs-lookup"><span data-stu-id="291ed-372">Choose to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="291ed-373">Na figura a seguir, o **seletor de cores** mostra um valor de cor atual de `rgba(0,0,0,0.7)` , que é próximo a preto.</span><span class="sxs-lookup"><span data-stu-id="291ed-373">In the following figure, the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="291ed-374">A cor específica deve mudar para a versão do preto que está realçada no visor depois que você a escolheu.</span><span class="sxs-lookup"><span data-stu-id="291ed-374">The specific color should change to the version of black that is currently highlighted in the viewport after you chose it.</span></span>  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       <span data-ttu-id="291ed-376">Usar o conta-gotas</span><span class="sxs-lookup"><span data-stu-id="291ed-376">Using the Eyedropper</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="291ed-377">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="291ed-377">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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

[DevToolsCommandMenu]: ../command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsCSSGetStarted]: ../css/index.md "Introdução ao visualizar e alterar CSS | Documentos da Microsoft"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Adicionar um PseudoState a uma classe-introdução ao visualizar e alterar CSS | Documentos da Microsoft"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Exibir o CSS de um elemento-introdução ao modo de exibição e alteração de CSS | Documentos da Microsoft"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Forçar o Microsoft Edge DevTools no modo de visualização de impressão (tipo de mídia de impressão CSS) | Documentos da Microsoft"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Torne um arquivo minified legível – referência de depuração de JavaScript | Documentos da Microsoft"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "O sistema de cores-design do material"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "O modelo de caixa | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Tipos de seletor-específico | MDN"  

> [!NOTE]
> <span data-ttu-id="291ed-387">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="291ed-387">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="291ed-388">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/css/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="291ed-388">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="291ed-390">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="291ed-390">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
