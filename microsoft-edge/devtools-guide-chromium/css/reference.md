---
title: Referência BITS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 4f0370b83d8c939476a1ed378dbdf750101c9527
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843961"
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







# <span data-ttu-id="5c910-103">Referência BITS</span><span class="sxs-lookup"><span data-stu-id="5c910-103">CSS Reference</span></span>   



<span data-ttu-id="5c910-104">Descubra novos fluxos de trabalho nesta referência abrangente do Microsoft Edge DevTools recursos relacionados à exibição e alteração da CSS.</span><span class="sxs-lookup"><span data-stu-id="5c910-104">Discover new workflows in this comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="5c910-105">Confira [introdução e alterar CSS][DevToolsCSSGetStarted] para aprender as noções básicas.</span><span class="sxs-lookup"><span data-stu-id="5c910-105">See [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted] to learn the basics.</span></span>  

## <span data-ttu-id="5c910-106">Selecionar um elemento</span><span class="sxs-lookup"><span data-stu-id="5c910-106">Select an element</span></span>   

<span data-ttu-id="5c910-107">O painel **elementos** do devtools permite que você visualize ou altere a CSS de um elemento de cada vez.</span><span class="sxs-lookup"><span data-stu-id="5c910-107">The **Elements** panel of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="5c910-108">O elemento selecionado é realçado na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="5c910-108">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="5c910-109">Os estilos do elemento são mostrados no painel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="5c910-109">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="5c910-110">Consulte [Exibir o CSS de um elemento][DevToolsCSSGetStartedTutorial] para um tutorial.</span><span class="sxs-lookup"><span data-stu-id="5c910-110">See [View the CSS for an element][DevToolsCSSGetStartedTutorial] for a tutorial.</span></span>  

> [!NOTE]
> <span data-ttu-id="5c910-111">Na [Figura 1](#figure-1), o `h1` elemento que está realçado na **árvore DOM** é o elemento selecionado.</span><span class="sxs-lookup"><span data-stu-id="5c910-111">In [Figure 1](#figure-1), the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="5c910-112">À direita, os estilos do elemento são mostrados no painel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="5c910-112">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="5c910-113">À esquerda, o elemento é realçado na viewport, mas só porque o mouse está passando no momento sobre ele na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="5c910-113">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

> ##### <span data-ttu-id="5c910-114">Figura 1</span><span class="sxs-lookup"><span data-stu-id="5c910-114">Figure 1</span></span>  
> <span data-ttu-id="5c910-115">Um exemplo de um elemento selecionado</span><span class="sxs-lookup"><span data-stu-id="5c910-115">An example of a selected element</span></span>  
> ![Um exemplo de um elemento selecionado][ImageSelectedElement]  

<span data-ttu-id="5c910-117">Há muitas maneiras de selecionar um elemento:</span><span class="sxs-lookup"><span data-stu-id="5c910-117">There are many ways to select an element:</span></span>  

*   <span data-ttu-id="5c910-118">No seu visor, clique com o botão direito do mouse no elemento e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="5c910-118">In your viewport, right-click the element and select **Inspect**.</span></span>  
*   <span data-ttu-id="5c910-119">No devtools, clique em **selecionar um elemento** , ![ Selecione um elemento ][ImageSelectAnElementIcon] ou pressione `Control` + `Shift` + `C` \ (Windows \) ou `Command` + `Shift` + `C` \ (MacOS \) e, em seguida, clique no elemento no visor.</span><span class="sxs-lookup"><span data-stu-id="5c910-119">In DevTools, click **Select an element** ![Select an element][ImageSelectAnElementIcon] or press `Control`+`Shift`+`C` \(Windows\) or `Command`+`Shift`+`C` \(macOS\), and then click the element in the viewport.</span></span>  
*   <span data-ttu-id="5c910-120">No DevTools, clique no elemento na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="5c910-120">In DevTools, click the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="5c910-121">No DevTools, execute uma consulta como `document.querySelector('p')` no **console**, clique com o botão direito do mouse no resultado e selecione **revelar no painel de elementos**.</span><span class="sxs-lookup"><span data-stu-id="5c910-121">In DevTools, run a query like `document.querySelector('p')` in the **Console**, right-click the result, and then select **Reveal in Elements panel**.</span></span>  

## <span data-ttu-id="5c910-122">Exibir CSS</span><span class="sxs-lookup"><span data-stu-id="5c910-122">View CSS</span></span>   

### <span data-ttu-id="5c910-123">Exibir a folha de estilos externa na qual uma regra está definida</span><span class="sxs-lookup"><span data-stu-id="5c910-123">View the external stylesheet where a rule is defined</span></span>   

<span data-ttu-id="5c910-124">No painel **estilos** , clique no link ao lado de uma regra CSS para abrir a folha de estilos externa que define a regra.</span><span class="sxs-lookup"><span data-stu-id="5c910-124">In the **Styles** pane, click the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  

<span data-ttu-id="5c910-125">Se a folha de estilos for minified, consulte [torne um arquivo do minified legível][DevToolsJavascriptReferenceFormat].</span><span class="sxs-lookup"><span data-stu-id="5c910-125">If the stylesheet is minified, see [Make a minified file readable][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="5c910-126">Na [Figura 2](#figure-2), clicar `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` leva você até a linha 2 de `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , onde a `.content h1:first-of-type` regra CSS é definida.</span><span class="sxs-lookup"><span data-stu-id="5c910-126">In [Figure 2](#figure-2), clicking `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` takes you to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

> ##### <span data-ttu-id="5c910-127">Figura 2</span><span class="sxs-lookup"><span data-stu-id="5c910-127">Figure 2</span></span>  
> <span data-ttu-id="5c910-128">Exibir a folha de estilos onde uma regra está definida</span><span class="sxs-lookup"><span data-stu-id="5c910-128">Viewing the stylesheet where a rule is defined</span></span>  
> ![Exibir a folha de estilos onde uma regra está definida][ImageViewRuleStylesheet]  

### <span data-ttu-id="5c910-130">Exibir apenas a CSS que é realmente aplicada a um elemento</span><span class="sxs-lookup"><span data-stu-id="5c910-130">View only the CSS that is actually applied to an element</span></span>   

<span data-ttu-id="5c910-131">A guia **estilos** mostra todas as regras que se aplicam a um elemento, incluindo declarações que foram substituídas.</span><span class="sxs-lookup"><span data-stu-id="5c910-131">The **Styles** tab shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="5c910-132">Quando você não está interessado em declarações substituídas, use a guia **calculada** para exibir apenas a CSS que está realmente sendo aplicada a um elemento.</span><span class="sxs-lookup"><span data-stu-id="5c910-132">When you are not interested in overridden declarations, use the **Computed** tab to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="5c910-133">[Selecione um elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5c910-133">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5c910-134">Vá para a guia **calculada** no painel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="5c910-134">Go to the **Computed** tab in the **Elements** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="5c910-135">Em uma ampla janela do DevTools, a guia **calculada** não existe.</span><span class="sxs-lookup"><span data-stu-id="5c910-135">On a wide DevTools window, the **Computed** tab does not exist.</span></span>  <span data-ttu-id="5c910-136">O conteúdo da guia **calculada** é mostrado na guia **estilos** .</span><span class="sxs-lookup"><span data-stu-id="5c910-136">The contents of the **Computed** tab are shown on the **Styles** tab.</span></span>  

<span data-ttu-id="5c910-137">As propriedades herdadas são opacas.</span><span class="sxs-lookup"><span data-stu-id="5c910-137">Inherited properties are opaque.</span></span>  <span data-ttu-id="5c910-138">Marque a caixa de seleção **Mostrar tudo** para ver todos os valores herdados.</span><span class="sxs-lookup"><span data-stu-id="5c910-138">Check the **Show All** checkbox to see all inherited values.</span></span>  

> [!NOTE]
> <span data-ttu-id="5c910-139">Na [Figura 3](#figure-3), a guia **calculada** mostra as propriedades CSS aplicadas ao elemento atualmente selecionado `h1` .</span><span class="sxs-lookup"><span data-stu-id="5c910-139">In [Figure 3](#figure-3), the **Computed** tab shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

> ##### <span data-ttu-id="5c910-140">Figura 3</span><span class="sxs-lookup"><span data-stu-id="5c910-140">Figure 3</span></span>  
> <span data-ttu-id="5c910-141">A guia **calculada**</span><span class="sxs-lookup"><span data-stu-id="5c910-141">The **Computed** tab</span></span>  
> ![A guia calculada][ImageComputedTab]  

### <span data-ttu-id="5c910-143">Exibir as propriedades CSS em ordem alfabética</span><span class="sxs-lookup"><span data-stu-id="5c910-143">View CSS properties in alphabetical order</span></span>   

<span data-ttu-id="5c910-144">Use a guia **calculada** .  Consulte [exibir apenas a CSS que é realmente aplicada a um elemento](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="5c910-144">Use the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="5c910-145">Exibir Propriedades CSS herdadas</span><span class="sxs-lookup"><span data-stu-id="5c910-145">View inherited CSS properties</span></span>   

<span data-ttu-id="5c910-146">Marque a caixa de seleção **Mostrar tudo** na guia **calculada** .  Consulte [exibir apenas a CSS que é realmente aplicada a um elemento](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="5c910-146">Check the **Show All** checkbox in the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="5c910-147">Exibir o modelo de caixa para um elemento</span><span class="sxs-lookup"><span data-stu-id="5c910-147">View the box model for an element</span></span>   

<span data-ttu-id="5c910-148">Para exibir [o modelo de caixa][MDNBoxModel] de um elemento, acesse a guia **estilos** .  Se a janela do DevTools for restrita, o diagrama de **modelo de caixa** estará na parte inferior da guia.</span><span class="sxs-lookup"><span data-stu-id="5c910-148">To view [the box model][MDNBoxModel] of an element, go to the **Styles** tab.  If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the tab.</span></span>  

<span data-ttu-id="5c910-149">Para alterar um valor, clique duas vezes nele.</span><span class="sxs-lookup"><span data-stu-id="5c910-149">To change a value, double-click on it.</span></span>  

> [!NOTE]
> <span data-ttu-id="5c910-150">Na [Figura 4](#figure-4), o diagrama de **modelo de caixa** na guia **estilos** mostra o modelo de caixa do elemento atualmente selecionado `h1` .</span><span class="sxs-lookup"><span data-stu-id="5c910-150">In [Figure 4](#figure-4), the **Box Model** diagram in the **Styles** tab shows the box model for the currently selected `h1` element.</span></span>  

> ##### <span data-ttu-id="5c910-151">Figura 4</span><span class="sxs-lookup"><span data-stu-id="5c910-151">Figure 4</span></span>  
> <span data-ttu-id="5c910-152">O diagrama de **modelo de caixa**</span><span class="sxs-lookup"><span data-stu-id="5c910-152">The **Box Model** diagram</span></span>  
> ![O diagrama de modelo de caixa][ImageBoxModel]  

### <span data-ttu-id="5c910-154">Pesquisar e filtrar a CSS de um elemento</span><span class="sxs-lookup"><span data-stu-id="5c910-154">Search and filter the CSS of an element</span></span>   

<span data-ttu-id="5c910-155">Use a caixa de texto **Filtrar** nas guias **estilos** e **calculados** para pesquisar valores ou propriedades CSS específicas.</span><span class="sxs-lookup"><span data-stu-id="5c910-155">Use the **Filter** text box on the **Styles** and **Computed** tabs to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="5c910-156">Para pesquisar também as propriedades herdadas na guia **calculada** , marque a caixa de seleção **Mostrar tudo** .</span><span class="sxs-lookup"><span data-stu-id="5c910-156">To also search inherited properties in the **Computed** tab, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="5c910-157">Na [Figura 5](#figure-5), a guia **estilos** é filtrada para mostrar apenas as regras que incluem a consulta de pesquisa `color` .</span><span class="sxs-lookup"><span data-stu-id="5c910-157">In [Figure 5](#figure-5), the **Styles** tab is filtered to only show rules that include the search query `color`.</span></span>  

> ##### <span data-ttu-id="5c910-158">Figura 5</span><span class="sxs-lookup"><span data-stu-id="5c910-158">Figure 5</span></span>  
> <span data-ttu-id="5c910-159">Filtrando a guia **estilos**</span><span class="sxs-lookup"><span data-stu-id="5c910-159">Filtering the **Styles** tab</span></span>  
> ![Filtrando a guia estilos][ImageStylesFilter]  

> [!NOTE]
> <span data-ttu-id="5c910-161">Na [Figura 6](#figure-6), a guia **calculada** é filtrada para mostrar somente declarações que incluam a consulta de pesquisa `100%` .</span><span class="sxs-lookup"><span data-stu-id="5c910-161">In [Figure 6](#figure-6), the **Computed** tab is filtered to only show declarations that include the search query `100%`.</span></span>  

> ##### <span data-ttu-id="5c910-162">Figura 6</span><span class="sxs-lookup"><span data-stu-id="5c910-162">Figure 6</span></span>  
> <span data-ttu-id="5c910-163">Filtrando a guia **calculada**</span><span class="sxs-lookup"><span data-stu-id="5c910-163">Filtering the **Computed** tab</span></span>  
> ![Filtrando a guia calculada][ImageComputerFilter]  

### <span data-ttu-id="5c910-165">Alternar uma pseudo-classe</span><span class="sxs-lookup"><span data-stu-id="5c910-165">Toggle a pseudo-class</span></span>   

<span data-ttu-id="5c910-166">Para alternar entre uma pseudoclasse, como `:active` , `:focus` `:hover` ou `:visited` :</span><span class="sxs-lookup"><span data-stu-id="5c910-166">To toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`:</span></span>  

1.  <span data-ttu-id="5c910-167">[Selecione um elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5c910-167">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5c910-168">No painel **elementos** , vá para a guia **estilos** .</span><span class="sxs-lookup"><span data-stu-id="5c910-168">On the **Elements** panel, go to the **Styles** tab.</span></span>  
1.  <span data-ttu-id="5c910-169">Clique em **: Hov**.</span><span class="sxs-lookup"><span data-stu-id="5c910-169">Click **:hov**.</span></span>  
1.  <span data-ttu-id="5c910-170">Verifique a pseudo-classe que você deseja habilitar.</span><span class="sxs-lookup"><span data-stu-id="5c910-170">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="5c910-171">Na [Figura 7](#figure-7), alterne a `:hover` pseudo-classe.</span><span class="sxs-lookup"><span data-stu-id="5c910-171">In [Figure 7](#figure-7), toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="5c910-172">Na viewport, verifique se a `background-color: cornflowerblue` declaração está sendo aplicada ao elemento, mesmo que o elemento não esteja realmente sendo focalizado.</span><span class="sxs-lookup"><span data-stu-id="5c910-172">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

> ##### <span data-ttu-id="5c910-173">Figura 7</span><span class="sxs-lookup"><span data-stu-id="5c910-173">Figure 7</span></span>  
> <span data-ttu-id="5c910-174">Como alternar a `:hover` pseudo-classe</span><span class="sxs-lookup"><span data-stu-id="5c910-174">Toggling the `:hover` pseudo-class</span></span>  
> ![Alternando o: hover pseudo-classe][ImagePseudoClass]  

<span data-ttu-id="5c910-176">Consulte [Adicionar um pseudo-estado a uma classe][DevToolsCSSGetStartedAddPseudoState] para um tutorial interativo.</span><span class="sxs-lookup"><span data-stu-id="5c910-176">See [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState] for an interactive tutorial.</span></span> 

### <span data-ttu-id="5c910-177">Exibir uma página no modo de impressão</span><span class="sxs-lookup"><span data-stu-id="5c910-177">View a page in print mode</span></span>   

<span data-ttu-id="5c910-178">Para exibir uma página no modo de impressão:</span><span class="sxs-lookup"><span data-stu-id="5c910-178">To view a page in print mode:</span></span>  
1.  <span data-ttu-id="5c910-179">[Abrir o menu de comandos][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="5c910-179">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="5c910-180">Comece a digitar `Rendering` e selecione `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="5c910-180">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="5c910-181">Para a lista suspensa **emular mídia CSS** , selecione **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="5c910-181">For the **Emulate CSS Media** dropdown, select **print**.</span></span>  

### <span data-ttu-id="5c910-182">Exibir CSS usado e não usado com a guia cobertura</span><span class="sxs-lookup"><span data-stu-id="5c910-182">View used and unused CSS with the Coverage tab</span></span>   

<span data-ttu-id="5c910-183">A guia cobertura mostra a CSS que uma página realmente usa.</span><span class="sxs-lookup"><span data-stu-id="5c910-183">The Coverage tab shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="5c910-184">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) enquanto o devtools estiver em foco para abrir o menu de comando.</span><span class="sxs-lookup"><span data-stu-id="5c910-184">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to open the Command Menu.</span></span>  
1.  <span data-ttu-id="5c910-185">Comece a digitar `coverage` e selecione **Mostrar cobertura**.</span><span class="sxs-lookup"><span data-stu-id="5c910-185">Start typing `coverage` and select **Show Coverage**.</span></span>  <span data-ttu-id="5c910-186">A guia cobertura é exibida.</span><span class="sxs-lookup"><span data-stu-id="5c910-186">The Coverage tab appears.</span></span>  
    
    > ##### <span data-ttu-id="5c910-187">Figura 8</span><span class="sxs-lookup"><span data-stu-id="5c910-187">Figure 8</span></span>  
    > <span data-ttu-id="5c910-188">Abrindo a guia cobertura no menu comando</span><span class="sxs-lookup"><span data-stu-id="5c910-188">Opening the Coverage tab from the Command Menu</span></span>  
    > ![Abrindo a guia cobertura no menu comando][ImageCommandMenu]  
    
    > ##### <span data-ttu-id="5c910-190">Figura 9</span><span class="sxs-lookup"><span data-stu-id="5c910-190">Figure 9</span></span>  
    > <span data-ttu-id="5c910-191">A guia cobertura</span><span class="sxs-lookup"><span data-stu-id="5c910-191">The Coverage tab</span></span>  
    > ![A guia cobertura][ImageCoverageEmpty]  
    
1.  <span data-ttu-id="5c910-193">Clique em **Iniciar cobertura de instrumentação e atualize a cobertura de** ![ Instrumentação de início de página e atualize a página ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="5c910-193">Click **Start instrumenting coverage and refresh the page** ![Start instrumenting coverage and refresh the page][ImageRefreshIcon].</span></span>  <span data-ttu-id="5c910-194">A página é atualizada e a guia cobertura fornece uma visão geral de quanto o CSS \ (e JavaScript \) é usado em cada arquivo que o navegador carrega.</span><span class="sxs-lookup"><span data-stu-id="5c910-194">The page refreshes and the Coverage tab provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="5c910-195">Verde representa a CSS usada.</span><span class="sxs-lookup"><span data-stu-id="5c910-195">Green represents used CSS.</span></span>  <span data-ttu-id="5c910-196">Vermelho representa a CSS não usada.</span><span class="sxs-lookup"><span data-stu-id="5c910-196">Red represents unused CSS.</span></span>  
    
    > ##### <span data-ttu-id="5c910-197">Figura 10</span><span class="sxs-lookup"><span data-stu-id="5c910-197">Figure 10</span></span>  
    > <span data-ttu-id="5c910-198">Uma visão geral do quanto CSS (e JavaScript) é usado e não usado</span><span class="sxs-lookup"><span data-stu-id="5c910-198">An overview of how much CSS (and JavaScript) is used and unused</span></span>  
    > ![Uma visão geral do quanto CSS (e JavaScript) é usado e não usado][ImageCoverageOverview]  

1.  <span data-ttu-id="5c910-200">Clique em um arquivo CSS para ver uma divisão linha por linha de qual CSS ele usa.</span><span class="sxs-lookup"><span data-stu-id="5c910-200">Click a CSS file to see a line-by-line breakdown of what CSS it uses.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5c910-201">Na [Figura 11](#figure-11), as linhas 145 a 147 e 149 a 151 não `b66bc881.site-ltr.css` são usadas, enquanto as linhas 163 para 166 são usadas.</span><span class="sxs-lookup"><span data-stu-id="5c910-201">In [Figure 11](#figure-11), lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    > ##### <span data-ttu-id="5c910-202">Figura 11</span><span class="sxs-lookup"><span data-stu-id="5c910-202">Figure 11</span></span>  
    > <span data-ttu-id="5c910-203">Uma divisão linha por linha do CSS usado e não usado</span><span class="sxs-lookup"><span data-stu-id="5c910-203">A line-by-line breakdown of used and unused CSS</span></span>  
    > ![Uma divisão linha por linha do CSS usado e não usado][ImageCoverageDetail]  
    
### <span data-ttu-id="5c910-205">Modo de visualização de impressão forçado</span><span class="sxs-lookup"><span data-stu-id="5c910-205">Force print preview mode</span></span>   

<span data-ttu-id="5c910-206">Consulte [forçar devtools no modo de visualização de impressão][DevToolsCssPrintPreview].</span><span class="sxs-lookup"><span data-stu-id="5c910-206">See [Force DevTools Into Print Preview Mode][DevToolsCssPrintPreview].</span></span>  

## <span data-ttu-id="5c910-207">Alterar CSS</span><span class="sxs-lookup"><span data-stu-id="5c910-207">Change CSS</span></span>   

<!-- todo s/CSS declaration/declaration/ -->  

### <span data-ttu-id="5c910-208">Adicionar uma declaração CSS a um elemento</span><span class="sxs-lookup"><span data-stu-id="5c910-208">Add a CSS declaration to an element</span></span>   

<span data-ttu-id="5c910-209">Como a ordem das declarações afeta a forma como um elemento é estilizado, você pode adicionar declarações de maneiras diferentes:</span><span class="sxs-lookup"><span data-stu-id="5c910-209">Since the order of declarations affects how an element is styled, you may add declarations in different ways:</span></span>  

*   <span data-ttu-id="5c910-210">[Adicione uma declaração embutida](#add-an-inline-declaration).</span><span class="sxs-lookup"><span data-stu-id="5c910-210">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="5c910-211">Equivalente a adicionar um `style` atributo ao HTML de um elemento.</span><span class="sxs-lookup"><span data-stu-id="5c910-211">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="5c910-212">[Adicione uma declaração a uma regra de estilo](#add-a-declaration-to-a-style-rule).</span><span class="sxs-lookup"><span data-stu-id="5c910-212">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="5c910-213">Que fluxo de trabalho você deve usar?</span><span class="sxs-lookup"><span data-stu-id="5c910-213">What workflow should you use?</span></span>** <span data-ttu-id="5c910-214">Para a maioria dos cenários, você provavelmente deseja usar o fluxo de trabalho da declaração embutida.</span><span class="sxs-lookup"><span data-stu-id="5c910-214">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="5c910-215">As declarações embutidas têm uma prioridade mais alta do que as externas, portanto, o fluxo de trabalho embutido garante que as alterações entrem em vigor no elemento como você esperaria.</span><span class="sxs-lookup"><span data-stu-id="5c910-215">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in the element as you would expect.</span></span>  <span data-ttu-id="5c910-216">Consulte [tipos de seletores][MDNSelectorTypes] para obter mais informações sobre a específica.</span><span class="sxs-lookup"><span data-stu-id="5c910-216">See [Selector Types][MDNSelectorTypes] for more on specificity.</span></span>  

<span data-ttu-id="5c910-217">Se você estiver Depurando qualquer estilo do elemento e precisar testar especificamente o que acontece quando uma declaração é definida em locais diferentes, use o outro fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5c910-217">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <span data-ttu-id="5c910-218">Adicionar uma declaração embutida</span><span class="sxs-lookup"><span data-stu-id="5c910-218">Add an inline declaration</span></span>   

<span data-ttu-id="5c910-219">Para adicionar uma declaração embutida:</span><span class="sxs-lookup"><span data-stu-id="5c910-219">To add an inline declaration:</span></span>  

1.  <span data-ttu-id="5c910-220">[Selecione um elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5c910-220">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5c910-221">No painel **estilos** , clique entre os colchetes da seção **elemento. Style** .</span><span class="sxs-lookup"><span data-stu-id="5c910-221">In the **Styles** pane, click between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="5c910-222">O cursor se concentra, permitindo que você insira texto.</span><span class="sxs-lookup"><span data-stu-id="5c910-222">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="5c910-223">Insira um nome de propriedade e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5c910-223">Enter a property name and press `Enter`.</span></span>  
1.  <span data-ttu-id="5c910-224">Insira um valor válido para essa propriedade e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5c910-224">Enter a valid value for that property and press `Enter`.</span></span>  <span data-ttu-id="5c910-225">Na **árvore DOM**, verifique se um `style` atributo foi adicionado ao elemento.</span><span class="sxs-lookup"><span data-stu-id="5c910-225">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="5c910-226">Na [Figura 12](#figure-12), as `margin-top` Propriedades e foram `background-color` aplicadas ao elemento selecionado.</span><span class="sxs-lookup"><span data-stu-id="5c910-226">In [Figure 12](#figure-12), the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="5c910-227">Na **árvore DOM** , verifique se as declarações são refletidas no `style` atributo para um elemento.</span><span class="sxs-lookup"><span data-stu-id="5c910-227">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

> ##### <span data-ttu-id="5c910-228">Figura 12</span><span class="sxs-lookup"><span data-stu-id="5c910-228">Figure 12</span></span>  
> <span data-ttu-id="5c910-229">Adicionando declarações embutidas</span><span class="sxs-lookup"><span data-stu-id="5c910-229">Adding inline declarations</span></span>  
> ![Adicionando declarações embutidas][ImageInlineDeclarations]  

#### <span data-ttu-id="5c910-231">Adicionar uma declaração a uma regra de estilo</span><span class="sxs-lookup"><span data-stu-id="5c910-231">Add a declaration to a style rule</span></span>   

<span data-ttu-id="5c910-232">Para adicionar uma declaração a uma regra de estilo existente:</span><span class="sxs-lookup"><span data-stu-id="5c910-232">To add a declaration to an existing style rule:</span></span>  

1.  <span data-ttu-id="5c910-233">[Selecione um elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5c910-233">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5c910-234">No painel **estilos** , clique entre os colchetes da regra de estilo à qual você deseja adicionar a declaração.</span><span class="sxs-lookup"><span data-stu-id="5c910-234">In the **Styles** pane, click between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="5c910-235">O cursor se concentra, permitindo que você insira texto.</span><span class="sxs-lookup"><span data-stu-id="5c910-235">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="5c910-236">Insira um nome de propriedade e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5c910-236">Enter a property name and press `Enter`.</span></span>  
1.  <span data-ttu-id="5c910-237">Insira um valor válido para essa propriedade e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5c910-237">Enter a valid value for that property and press `Enter`.</span></span>  

> ##### <span data-ttu-id="5c910-238">Figura 13</span><span class="sxs-lookup"><span data-stu-id="5c910-238">Figure 13</span></span>  
> <span data-ttu-id="5c910-239">Adicionando a `border-bottom-style:groove` declaração a uma regra de estilo</span><span class="sxs-lookup"><span data-stu-id="5c910-239">Adding the `border-bottom-style:groove` declaration to a style rule</span></span>  
> ![Adicionando uma declaração a uma regra de estilo][ImageAddDeclarationExistingRule]  

### <span data-ttu-id="5c910-241">Alterar um nome ou valor de declaração</span><span class="sxs-lookup"><span data-stu-id="5c910-241">Change a declaration name or value</span></span>   

<span data-ttu-id="5c910-242">Clique duas vezes no nome ou valor de uma declaração para alterá-la.</span><span class="sxs-lookup"><span data-stu-id="5c910-242">Double-click the name or value of a declaration to change it.</span></span>  <span data-ttu-id="5c910-243">Consulte [alterar valores de declaração com atalhos de teclado](#change-declaration-values-with-keyboard-shortcuts) para atalhos para incrementar ou decrementar rapidamente um valor por `0.1` ,, `1` `10` ou `100` unidades.</span><span class="sxs-lookup"><span data-stu-id="5c910-243">See [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts) for shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units.</span></span>  

> ##### <span data-ttu-id="5c910-244">Figura 14</span><span class="sxs-lookup"><span data-stu-id="5c910-244">Figure 14</span></span>  
> <span data-ttu-id="5c910-245">Alterar o valor da</span><span class="sxs-lookup"><span data-stu-id="5c910-245">Changing the value of the</span></span> `border-bottom-style`  
> ![Alterar o valor de uma declaração][ImageAddDeclarationExistingRule2]  

### <span data-ttu-id="5c910-247">Alterar valores de declaração com atalhos de teclado</span><span class="sxs-lookup"><span data-stu-id="5c910-247">Change declaration values with keyboard shortcuts</span></span>   

<span data-ttu-id="5c910-248">Durante a edição do valor de uma declaração, você pode usar os seguintes atalhos de teclado para incrementar o valor por um valor fixo:</span><span class="sxs-lookup"><span data-stu-id="5c910-248">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a fixed amount:</span></span>  

*   <span data-ttu-id="5c910-249">Pressione `Alt` + `Up` \ (Windows \) ou `Option` + `Up` \ (MacOS \) para incrementar `0.1` .</span><span class="sxs-lookup"><span data-stu-id="5c910-249">Press `Alt`+`Up` \(Windows\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="5c910-250">Pressione `Up` para alterar o valor por `1` , ou `0.1` se o valor atual estiver entre `-1` e `1` .</span><span class="sxs-lookup"><span data-stu-id="5c910-250">Press `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="5c910-251">Pressione `Shift` + `Up` para incrementar `10` .</span><span class="sxs-lookup"><span data-stu-id="5c910-251">Press `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="5c910-252">Pressione `Shift` + `Page Up` \ (Windows \) ou `Shift` + `Command` + `Up` \ (MacOS \) para incrementar o valor por `100` .</span><span class="sxs-lookup"><span data-stu-id="5c910-252">Press `Shift`+`Page Up` \(Windows\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="5c910-253">O decréscimo também funciona.</span><span class="sxs-lookup"><span data-stu-id="5c910-253">Decrementing also works.</span></span>  <span data-ttu-id="5c910-254">Basta substituir cada ocorrência de `Up` mencionado acima por `Down` .</span><span class="sxs-lookup"><span data-stu-id="5c910-254">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <span data-ttu-id="5c910-255">Adicionar uma classe a um elemento</span><span class="sxs-lookup"><span data-stu-id="5c910-255">Add a class to an element</span></span>   

<span data-ttu-id="5c910-256">Para adicionar uma classe a um elemento:</span><span class="sxs-lookup"><span data-stu-id="5c910-256">To add a class to an element:</span></span>  

1.  <span data-ttu-id="5c910-257">[Selecione o elemento](#select-an-element) na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="5c910-257">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="5c910-258">Clique em **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="5c910-258">Click **.cls**.</span></span>  
1.  <span data-ttu-id="5c910-259">Digite o nome da classe na caixa de texto **Adicionar nova classe** .</span><span class="sxs-lookup"><span data-stu-id="5c910-259">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="5c910-260">Pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5c910-260">Press `Enter`.</span></span>  

> ##### <span data-ttu-id="5c910-261">Figura 15</span><span class="sxs-lookup"><span data-stu-id="5c910-261">Figure 15</span></span>  
> <span data-ttu-id="5c910-262">O painel **classes de elemento**</span><span class="sxs-lookup"><span data-stu-id="5c910-262">The **Element Classes** pane</span></span>  
> ![O painel classes de elemento][ImageElementClasses]  

### <span data-ttu-id="5c910-264">Alternar uma classe</span><span class="sxs-lookup"><span data-stu-id="5c910-264">Toggle a class</span></span>   

<span data-ttu-id="5c910-265">Para habilitar ou desabilitar uma classe em um elemento:</span><span class="sxs-lookup"><span data-stu-id="5c910-265">To enable or disable a class on an element:</span></span>  

1.  <span data-ttu-id="5c910-266">[Selecione o elemento](#select-an-element) na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="5c910-266">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="5c910-267">Abrir o painel **classes de elementos** .</span><span class="sxs-lookup"><span data-stu-id="5c910-267">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="5c910-268">Consulte [Adicionar uma classe a um elemento](#add-a-class-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="5c910-268">See [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="5c910-269">Abaixo da caixa de texto **Adicionar nova classe** estão todas as classes que estão sendo aplicadas a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="5c910-269">Below the **Add New Class** text box are all of the classes that are being applied to this element.</span></span>  
1.  <span data-ttu-id="5c910-270">Alternar a caixa de seleção ao lado da classe que você deseja habilitar ou desabilitar.</span><span class="sxs-lookup"><span data-stu-id="5c910-270">Toggle the checkbox next to the class that you want to enable or disable.</span></span>  

### <span data-ttu-id="5c910-271">Adicionar uma regra de estilo</span><span class="sxs-lookup"><span data-stu-id="5c910-271">Add a style rule</span></span>   

<span data-ttu-id="5c910-272">Para adicionar uma nova regra de estilo:</span><span class="sxs-lookup"><span data-stu-id="5c910-272">To add a new style rule:</span></span>  

1.  <span data-ttu-id="5c910-273">[Selecione um elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5c910-273">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5c910-274">Clique em nova regra de **estilo** ![ nova regra de estilo ][ImageNewStyleRuleIcon] .</span><span class="sxs-lookup"><span data-stu-id="5c910-274">Click **New Style Rule** ![New Style Rule][ImageNewStyleRuleIcon].</span></span>  <span data-ttu-id="5c910-275">DevTools insere uma nova regra abaixo da regra **elemento. Style** .</span><span class="sxs-lookup"><span data-stu-id="5c910-275">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="5c910-276">Na [Figura 16](#figure-16), devtools adiciona a `h1.devsite-page-title` regra de estilo depois de clicar em **nova regra de estilo**.</span><span class="sxs-lookup"><span data-stu-id="5c910-276">In [Figure 16](#figure-16), DevTools adds the `h1.devsite-page-title` style rule after clicking **New Style Rule**.</span></span>  

> ##### <span data-ttu-id="5c910-277">Figura 16</span><span class="sxs-lookup"><span data-stu-id="5c910-277">Figure 16</span></span>  
> <span data-ttu-id="5c910-278">Adicionando uma nova regra de estilo</span><span class="sxs-lookup"><span data-stu-id="5c910-278">Adding a new style rule</span></span>  
> ![Adicionando uma nova regra de estilo][ImageStyleRule]  

#### <span data-ttu-id="5c910-280">Escolha em qual folha de estilos você deseja adicionar uma regra</span><span class="sxs-lookup"><span data-stu-id="5c910-280">Choose which stylesheet to add a rule to</span></span>   

<span data-ttu-id="5c910-281">Ao [Adicionar uma nova regra de estilo](#add-a-style-rule), clique e **mantenha nova regra de estilo** ![ nova regra ][ImageNewStyleRuleIcon] de estilo para escolher em qual folha de estilos adicionar a regra de estilo.</span><span class="sxs-lookup"><span data-stu-id="5c910-281">When [adding a new style rule](#add-a-style-rule), click and hold **New Style Rule** ![New Style Rule][ImageNewStyleRuleIcon] to choose which stylesheet to add the style rule to.</span></span>  

> ##### <span data-ttu-id="5c910-282">Figura 17</span><span class="sxs-lookup"><span data-stu-id="5c910-282">Figure 17</span></span>  
> <span data-ttu-id="5c910-283">Escolhendo uma folha de estilos</span><span class="sxs-lookup"><span data-stu-id="5c910-283">Choosing a stylesheet</span></span>  
> ![Escolhendo uma folha de estilos][ImageChooseStylesheet]  

#### <span data-ttu-id="5c910-285">Adicionar uma regra de estilo a um local específico</span><span class="sxs-lookup"><span data-stu-id="5c910-285">Add a style rule to a specific location</span></span>   

<span data-ttu-id="5c910-286">Para adicionar uma regra de estilo a um local específico na guia **estilos** :</span><span class="sxs-lookup"><span data-stu-id="5c910-286">To add a style rule to a specific location in the **Styles** tab:</span></span>  

1.  <span data-ttu-id="5c910-287">Passe o mouse sobre a regra de estilo que está diretamente acima de onde você deseja adicionar sua nova regra de estilo.</span><span class="sxs-lookup"><span data-stu-id="5c910-287">Hover over the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="5c910-288">[Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5c910-288">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5c910-289">Clique em **Inserir regra de estilo abaixo** ![ Inserir regra de estilo abaixo ][ImageNewStyleRuleIcon] .</span><span class="sxs-lookup"><span data-stu-id="5c910-289">Click **Insert Style Rule Below** ![Insert Style Rule Below][ImageNewStyleRuleIcon].</span></span>  

> ##### <span data-ttu-id="5c910-290">Figura 18</span><span class="sxs-lookup"><span data-stu-id="5c910-290">Figure 18</span></span>  
> **<span data-ttu-id="5c910-291">Inserir regra de estilo abaixo</span><span class="sxs-lookup"><span data-stu-id="5c910-291">Insert Style Rule Below</span></span>**  
> ![Inserir regra de estilo abaixo][ImageInsertStyleRuleBelow]  

### <span data-ttu-id="5c910-293">Revelar a barra de ferramentas mais ações</span><span class="sxs-lookup"><span data-stu-id="5c910-293">Reveal the More Actions toolbar</span></span>   

<span data-ttu-id="5c910-294">A barra de ferramentas **mais ações** permite que você:</span><span class="sxs-lookup"><span data-stu-id="5c910-294">The **More Actions** toolbar lets you:</span></span>  

*   <span data-ttu-id="5c910-295">Insira uma regra de estilo diretamente abaixo da que você está focalizado.</span><span class="sxs-lookup"><span data-stu-id="5c910-295">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="5c910-296">Adicione uma `background-color` `color` declaração,, `box-shadow` ou `text-shadow` para a regra de estilo na qual você está focalizado.</span><span class="sxs-lookup"><span data-stu-id="5c910-296">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="5c910-297">Para revelar a barra de ferramentas **mais ações** :</span><span class="sxs-lookup"><span data-stu-id="5c910-297">To reveal the **More Actions** toolbar:</span></span>  

1.  <span data-ttu-id="5c910-298">Na guia **estilos** , passe o mouse sobre uma regra de estilo.</span><span class="sxs-lookup"><span data-stu-id="5c910-298">In the **Styles** tab, hover over a style rule.</span></span>  <span data-ttu-id="5c910-299">**Mais ações** `...` é revelado no canto inferior direito da seção de regra de estilo.</span><span class="sxs-lookup"><span data-stu-id="5c910-299">**More Actions** `...` is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5c910-300">Na [Figura 19](#figure-19), passe o mouse sobre a `.header-holder.has-default-focus` regra de estilo e **mais ações** são reveladas no canto inferior direito da seção de regra de estilo.</span><span class="sxs-lookup"><span data-stu-id="5c910-300">In [Figure 19](#figure-19), hover over the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    > ##### <span data-ttu-id="5c910-301">Figura 19</span><span class="sxs-lookup"><span data-stu-id="5c910-301">Figure 19</span></span>  
    > <span data-ttu-id="5c910-302">Revelando **mais ações**</span><span class="sxs-lookup"><span data-stu-id="5c910-302">Revealing **More Actions**</span></span>  
    > ![Revelando mais ações][ImageRevealMore]  
    
1.  <span data-ttu-id="5c910-304">Passe o mouse sobre **mais ações** `...` para revelar as ações mencionadas acima.</span><span class="sxs-lookup"><span data-stu-id="5c910-304">Hover over **More Actions** `...` to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5c910-305">A ação **Inserir regra de estilo abaixo** é revelada depois de passar o mouse sobre **mais ações**.</span><span class="sxs-lookup"><span data-stu-id="5c910-305">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    > ##### <span data-ttu-id="5c910-306">Figura 20</span><span class="sxs-lookup"><span data-stu-id="5c910-306">Figure 20</span></span>  
    > <span data-ttu-id="5c910-307">A barra de ferramentas **mais ações**</span><span class="sxs-lookup"><span data-stu-id="5c910-307">The **More Actions** toolbar</span></span>  
    > ![A barra de ferramentas mais ações][ImageInsertStyleRuleBelow2]  
    
### <span data-ttu-id="5c910-309">Alternar uma declaração</span><span class="sxs-lookup"><span data-stu-id="5c910-309">Toggle a declaration</span></span>   

<span data-ttu-id="5c910-310">Para ativar ou desativar uma única declaração:</span><span class="sxs-lookup"><span data-stu-id="5c910-310">To toggle a single declaration on or off:</span></span>  

1.  <span data-ttu-id="5c910-311">[Selecione um elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5c910-311">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5c910-312">No painel **estilos** , passe o mouse sobre a regra que define a declaração.</span><span class="sxs-lookup"><span data-stu-id="5c910-312">In the **Styles** pane, hover over the rule that defines the declaration.</span></span>  <span data-ttu-id="5c910-313">As caixas de seleção aparecem ao lado de cada declaração.</span><span class="sxs-lookup"><span data-stu-id="5c910-313">Checkboxes appear next to each declaration.</span></span>  
1.  <span data-ttu-id="5c910-314">Marque ou desmarque a caixa de seleção ao lado da declaração.</span><span class="sxs-lookup"><span data-stu-id="5c910-314">Check or uncheck the checkbox next to the declaration.</span></span>  <span data-ttu-id="5c910-315">Quando você desmarca uma declaração, o DevTools a risca para indicar que não está mais ativo.</span><span class="sxs-lookup"><span data-stu-id="5c910-315">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="5c910-316">Na [Figura 21](#figure-21), a `margin-top` Propriedade do elemento selecionado no momento foi desativada.</span><span class="sxs-lookup"><span data-stu-id="5c910-316">In [Figure 21](#figure-21), the `margin-top` property for the currently selected element has been toggled off.</span></span>  

> ##### <span data-ttu-id="5c910-317">Figura 21</span><span class="sxs-lookup"><span data-stu-id="5c910-317">Figure 21</span></span>  
> <span data-ttu-id="5c910-318">Como alternar uma declaração</span><span class="sxs-lookup"><span data-stu-id="5c910-318">Toggling a declaration</span></span>  
> ![Como alternar uma declaração][ImageToggleDeclaration]  

### <span data-ttu-id="5c910-320">Adicionar uma declaração de cor de plano de fundo</span><span class="sxs-lookup"><span data-stu-id="5c910-320">Add a background-color declaration</span></span>   

<span data-ttu-id="5c910-321">Para adicionar uma `background-color` declaração a um elemento:</span><span class="sxs-lookup"><span data-stu-id="5c910-321">To add a `background-color` declaration to an element:</span></span>  

1.  <span data-ttu-id="5c910-322">Passe o mouse sobre a regra de estilo à qual você deseja adicionar a `background-color` declaração.</span><span class="sxs-lookup"><span data-stu-id="5c910-322">Hover over the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="5c910-323">[Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5c910-323">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5c910-324">Clique em **adicionar cor de plano de fundo** ![ adicionar cor de plano de fundo ][ImageAddBackgroundColorIcon] .</span><span class="sxs-lookup"><span data-stu-id="5c910-324">Click **Add Background Color** ![Add Background Color][ImageAddBackgroundColorIcon].</span></span>  

> ##### <span data-ttu-id="5c910-325">Figura 22</span><span class="sxs-lookup"><span data-stu-id="5c910-325">Figure 22</span></span>  
> **<span data-ttu-id="5c910-326">Adicionar cor de plano de fundo</span><span class="sxs-lookup"><span data-stu-id="5c910-326">Add Background Color</span></span>**  
> ![Adicionar cor de plano de fundo][ImageAddBackgroundColor]  

### <span data-ttu-id="5c910-328">Adicionar uma declaração de cor</span><span class="sxs-lookup"><span data-stu-id="5c910-328">Add a color declaration</span></span>   

<span data-ttu-id="5c910-329">Para adicionar uma `color` declaração a um elemento:</span><span class="sxs-lookup"><span data-stu-id="5c910-329">To add a `color` declaration to an element:</span></span>  

1.  <span data-ttu-id="5c910-330">Passe o mouse sobre a regra de estilo à qual você deseja adicionar a `color` declaração.</span><span class="sxs-lookup"><span data-stu-id="5c910-330">Hover over the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="5c910-331">[Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5c910-331">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5c910-332">Clique em **adicionar cor** ![ adicionar cor ][ImageAddColorIcon] .</span><span class="sxs-lookup"><span data-stu-id="5c910-332">Click **Add Color** ![Add Color][ImageAddColorIcon].</span></span>  

> ##### <span data-ttu-id="5c910-333">Figura 23</span><span class="sxs-lookup"><span data-stu-id="5c910-333">Figure 23</span></span>  
> **<span data-ttu-id="5c910-334">Adicionar cor</span><span class="sxs-lookup"><span data-stu-id="5c910-334">Add Color</span></span>**  
> ![Adicionar cor][ImageAddColor]  

### <span data-ttu-id="5c910-336">Adicionar uma declaração de caixa-sombra</span><span class="sxs-lookup"><span data-stu-id="5c910-336">Add a box-shadow declaration</span></span>   

<span data-ttu-id="5c910-337">Para adicionar uma `box-shadow` declaração a um elemento:</span><span class="sxs-lookup"><span data-stu-id="5c910-337">To add a `box-shadow` declaration to an element:</span></span>  

1.  <span data-ttu-id="5c910-338">Passe o mouse sobre a regra de estilo à qual você deseja adicionar a `box-shadow` declaração.</span><span class="sxs-lookup"><span data-stu-id="5c910-338">Hover over the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="5c910-339">[Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5c910-339">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5c910-340">Clique em **Adicionar caixa** ![ Adicionar à caixa Adicionar sombra ][ImageAddBoxShadowIcon] .</span><span class="sxs-lookup"><span data-stu-id="5c910-340">Click **Add Box Shadow** ![Add Box Shadow][ImageAddBoxShadowIcon].</span></span>  

> ##### <span data-ttu-id="5c910-341">Figura 24</span><span class="sxs-lookup"><span data-stu-id="5c910-341">Figure 24</span></span>  
> **<span data-ttu-id="5c910-342">Adicionar sombra à caixa</span><span class="sxs-lookup"><span data-stu-id="5c910-342">Add Box Shadow</span></span>**  
> ![Adicionar sombra à caixa][ImageAddBoxShadow]  

### <span data-ttu-id="5c910-344">Adicionar uma declaração de sombra de texto</span><span class="sxs-lookup"><span data-stu-id="5c910-344">Add a text-shadow declaration</span></span>   

<span data-ttu-id="5c910-345">Para adicionar uma `text-shadow` declaração a um elemento:</span><span class="sxs-lookup"><span data-stu-id="5c910-345">To add a `text-shadow` declaration to an element:</span></span>  

1.  <span data-ttu-id="5c910-346">Passe o mouse sobre a regra de estilo à qual você deseja adicionar a `text-shadow` declaração.</span><span class="sxs-lookup"><span data-stu-id="5c910-346">Hover over the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="5c910-347">[Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5c910-347">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5c910-348">Clique em **Adicionar sombra de texto** ![ Adicionar sombra de texto ][ImageAddTextShadowIcon] .</span><span class="sxs-lookup"><span data-stu-id="5c910-348">Click **Add Text Shadow** ![Add Text Shadow][ImageAddTextShadowIcon].</span></span>  

> ##### <span data-ttu-id="5c910-349">Figura 25</span><span class="sxs-lookup"><span data-stu-id="5c910-349">Figure 25</span></span>  
> **<span data-ttu-id="5c910-350">Adicionar sombra de texto</span><span class="sxs-lookup"><span data-stu-id="5c910-350">Add Text Shadow</span></span>**  
> ![Adicionar sombra de texto][ImageAddTextShadow]  

### <span data-ttu-id="5c910-352">Alterar as cores com o seletor de cores</span><span class="sxs-lookup"><span data-stu-id="5c910-352">Change colors with the Color Picker</span></span>   

<span data-ttu-id="5c910-353">O **seletor de cores** fornece uma GUI para alteração `color` e `background-color` declarações.</span><span class="sxs-lookup"><span data-stu-id="5c910-353">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="5c910-354">Para abrir o **seletor de cores**:</span><span class="sxs-lookup"><span data-stu-id="5c910-354">To open the **Color Picker**:</span></span>  

1.  <span data-ttu-id="5c910-355">[Selecione um elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5c910-355">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5c910-356">Na guia **estilos** , localize a `color` declaração, `background-color` ou semelhante, que você deseja alterar.</span><span class="sxs-lookup"><span data-stu-id="5c910-356">In the **Styles** tab, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="5c910-357">À esquerda do `color` `background-color` valor, ou semelhante, há um quadrado pequeno que é uma visualização da cor.</span><span class="sxs-lookup"><span data-stu-id="5c910-357">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5c910-358">Na [Figura 26](#figure-26), o pequeno quadrado à esquerda de `rgba(0, 0, 0, 0.7)` é uma visualização da cor.</span><span class="sxs-lookup"><span data-stu-id="5c910-358">In [Figure 26](#figure-26), the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    > ##### <span data-ttu-id="5c910-359">Figura 26</span><span class="sxs-lookup"><span data-stu-id="5c910-359">Figure 26</span></span>  
    > <span data-ttu-id="5c910-360">Visualização de cores</span><span class="sxs-lookup"><span data-stu-id="5c910-360">Color preview</span></span>  
    > ![Visualização de cores][ImageColorPreview]  
    
1.  <span data-ttu-id="5c910-362">Clique na visualização para abrir o **seletor de cores**.</span><span class="sxs-lookup"><span data-stu-id="5c910-362">Click the preview to open the **Color Picker**.</span></span>  
    
    > ##### <span data-ttu-id="5c910-363">Figura 27</span><span class="sxs-lookup"><span data-stu-id="5c910-363">Figure 27</span></span>  
    > <span data-ttu-id="5c910-364">O **seletor de cores**</span><span class="sxs-lookup"><span data-stu-id="5c910-364">The **Color Picker**</span></span>  
    > ![O seletor de cores][ImageColorPicker]  
    
<span data-ttu-id="5c910-366">Aqui está uma descrição de cada um dos elementos de interface do usuário do **seletor de cores**:</span><span class="sxs-lookup"><span data-stu-id="5c910-366">Here is a description of each of the UI elements of the **Color Picker**:</span></span>  

> ##### <span data-ttu-id="5c910-367">Figura 28</span><span class="sxs-lookup"><span data-stu-id="5c910-367">Figure 28</span></span>  
> <span data-ttu-id="5c910-368">O seletor de cores, anotado</span><span class="sxs-lookup"><span data-stu-id="5c910-368">The Color Picker, annotated</span></span>  
> ![O seletor de cores, anotado][ImageColorPickerAnnotated]  

1.  <span data-ttu-id="5c910-370">**Sombras**.</span><span class="sxs-lookup"><span data-stu-id="5c910-370">**Shades**.</span></span>  
1.  <span data-ttu-id="5c910-371">**Conta-gotas**.</span><span class="sxs-lookup"><span data-stu-id="5c910-371">**Eyedropper**.</span></span>  <span data-ttu-id="5c910-372">Consulte [obter uma amostra de uma cor na página com o conta-gotas](#sample-a-color-off-the-page-with-the-eyedropper).</span><span class="sxs-lookup"><span data-stu-id="5c910-372">See [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
1.  <span data-ttu-id="5c910-373">**Copiar para a área de transferência**.</span><span class="sxs-lookup"><span data-stu-id="5c910-373">**Copy To Clipboard**.</span></span>  <span data-ttu-id="5c910-374">Copie o **valor de exibição** para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="5c910-374">Copy the **Display Value** to your clipboard.</span></span>  
1.  <span data-ttu-id="5c910-375">**Valor de exibição**.</span><span class="sxs-lookup"><span data-stu-id="5c910-375">**Display Value**.</span></span>  <span data-ttu-id="5c910-376">A representação RGBA, HSLA ou hexa da cor.</span><span class="sxs-lookup"><span data-stu-id="5c910-376">The RGBA, HSLA, or Hex representation of the color.</span></span>  
1.  <span data-ttu-id="5c910-377">**Paleta de cores**.</span><span class="sxs-lookup"><span data-stu-id="5c910-377">**Color Palette**.</span></span>  <span data-ttu-id="5c910-378">Clique em um desses quadrados para alterar a cor para esse quadrado.</span><span class="sxs-lookup"><span data-stu-id="5c910-378">Click one of these squares to change the color to that square.</span></span>  
1.  <span data-ttu-id="5c910-379">**Matiz**.</span><span class="sxs-lookup"><span data-stu-id="5c910-379">**Hue**.</span></span>  
1.  <span data-ttu-id="5c910-380">**Opacidade**.</span><span class="sxs-lookup"><span data-stu-id="5c910-380">**Opacity**.</span></span>  
1.  <span data-ttu-id="5c910-381">**Seletor de valor de exibição**.</span><span class="sxs-lookup"><span data-stu-id="5c910-381">**Display Value Switcher**.</span></span>  <span data-ttu-id="5c910-382">Alternar entre as representações de RGBA, HSLA e HexA da cor atual.</span><span class="sxs-lookup"><span data-stu-id="5c910-382">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
1.  <span data-ttu-id="5c910-383">**Interruptor de paleta de cores**.</span><span class="sxs-lookup"><span data-stu-id="5c910-383">**Color Palette Switcher**.</span></span>  <span data-ttu-id="5c910-384">Alternar entre a [paleta de design de material][MaterialDesignColorSystem], uma paleta personalizada ou uma paleta de cores de página.</span><span class="sxs-lookup"><span data-stu-id="5c910-384">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="5c910-385">O DevTools gera a paleta de cores da página com base nas cores encontradas nas suas folhas de estilos.</span><span class="sxs-lookup"><span data-stu-id="5c910-385">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  

#### <span data-ttu-id="5c910-386">Exemplo de uma cor para fora da página com o conta-gotas</span><span class="sxs-lookup"><span data-stu-id="5c910-386">Sample a color off the page with the Eyedropper</span></span>   

<span data-ttu-id="5c910-387">Quando você abre o **seletor de cores**, o conta-gotas do **conta** -gotas ![ ][ImageEyedropperIcon] está ativado por padrão.</span><span class="sxs-lookup"><span data-stu-id="5c910-387">When you open the **Color Picker**, the **Eyedropper** ![Eyedropper][ImageEyedropperIcon] is on by default.</span></span>  <span data-ttu-id="5c910-388">Para alterar a cor selecionada para outra cor na página:</span><span class="sxs-lookup"><span data-stu-id="5c910-388">To change the selected color to some other color on the page:</span></span>  

1.  <span data-ttu-id="5c910-389">Passe o mouse sobre a cor de destino no visor.</span><span class="sxs-lookup"><span data-stu-id="5c910-389">Hover over the target color in the viewport.</span></span>  
1.  <span data-ttu-id="5c910-390">Clique em para confirmar.</span><span class="sxs-lookup"><span data-stu-id="5c910-390">Click to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5c910-391">Na [Figura 29](#figure-29), o **seletor de cores** mostra um valor de cor atual de `rgba(0,0,0,0.7)` , que é próximo a preto.</span><span class="sxs-lookup"><span data-stu-id="5c910-391">In [Figure 29](#figure-29), the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="5c910-392">Essa cor deve mudar para o preto que está realçado no visor quando o preto foi clicado.</span><span class="sxs-lookup"><span data-stu-id="5c910-392">This color should change to the black that is currently highlighted in the viewport once the black was clicked.</span></span>  
    
    > ##### <span data-ttu-id="5c910-393">Figura 29</span><span class="sxs-lookup"><span data-stu-id="5c910-393">Figure 29</span></span>  
    > <span data-ttu-id="5c910-394">Usar o conta-gotas</span><span class="sxs-lookup"><span data-stu-id="5c910-394">Using the Eyedropper</span></span>  
    > ![Usar o conta-gotas][ImageUsingEyedropper]  
    
 



<!-- image links -->  

[ImageAddBackgroundColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: /microsoft-edge/devtools-guide-chromium/media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-an-element-icon.msft.png  

[ImageSelectedElement]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1.msft.png "Figura 1: um exemplo de um elemento selecionado"  
[ImageViewRuleStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-highlight.msft.png "Figura 2: exibir a folha de estilos na qual uma regra está definida"  
[ImageComputedTab]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-h1.msft.png "Figura 3: a guia calculada"  
[ImageBoxModel]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-2.msft.png "Figura 4: o diagrama de modelo de caixa"  
[ImageStylesFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-color.msft.png "Figura 5: filtrando a guia estilos"  
[ImageComputerFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-filter-100.msft.png "Figura 6: filtrando a guia calculada"  
[ImagePseudoClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-hov-hover.msft.png "Figura 7: alternando o: hover pseudo-classe"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-coverage.msft.png "Figura 8: abrindo a guia cobertura no menu de comando"  
[ImageCoverageEmpty]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-empty.msft.png "Figura 9: a guia cobertura"  
[ImageCoverageOverview]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-run.msft.png "Figura 10: uma visão geral do quanto CSS (e JavaScript) é usado e não usado"  
[ImageCoverageDetail]: /microsoft-edge/devtools-guide-chromium/media/css-sources-css-coverage.msft.png "Figura 11: divisão linha por linha de CSS usada e não usada"  
[ImageInlineDeclarations]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-margin-top-background-color.msft.png "Figura 12: adicionando declarações embutidas"  
[ImageAddDeclarationExistingRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style.msft.png "Figura 13: adicionando uma declaração a uma regra de estilo"  
[ImageAddDeclarationExistingRule2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style-dropdown.msft.png "Figura 14: alterando o valor de uma declaração"  
[ImageElementClasses]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-classes.msft.png "Figura 15: painel classes de elemento"  
[ImageStyleRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new.msft.png "Figura 16: adicionando uma nova regra de estilo"  
[ImageChooseStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new-select-exisiting.msft.png "Figura 17: escolhendo uma folha de estilos"  
[ImageInsertStyleRuleBelow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-insert-style-rule-below.msft.png "Figura 18: inserir regra de estilo abaixo"  
[ImageRevealMore]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-new-rule-styles.msft.png "Figura 19: revelando mais ações"  
[ImageInsertStyleRuleBelow2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png "Figura 20: a barra de ferramentas mais ações"  
[ImageToggleDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-deactivated.msft.png "Figura 21: alternando uma declaração"  
[ImageAddBackgroundColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-background-color.msft.png "Figura 22: adicionar cor de plano de fundo"  
[ImageAddColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-color.msft.png "Figura 23: adicionar cor"  
[ImageAddBoxShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-box-shadow.msft.png "Figura 24: Adicionar sombra à caixa"  
[ImageAddTextShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-text-shadow.msft.png "Figura 25: Adicionar sombra de texto"  
[ImageColorPreview]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-overlay-color-box.msft.png "Figura 26: visualização de cores"  
[ImageColorPicker]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker.msft.png "Figura 27: o seletor de cores"  
[ImageColorPickerAnnotated]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker-annotated.msft.png "Figura 28: o seletor de cores, anotado"  
[ImageUsingEyedropper]: /microsoft-edge/devtools-guide-chromium/media/css-color-picker-eye-dropper.msft.png "Figura 29: usando o conta-gotas"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando do Microsoft Edge DevTools"  
[DevToolsCSSGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Introdução à exibição e alteração de CSS"  
[DevToolsCSSGetStartedAddPseudoState]: /microsoft-edge/devtools-guide-chromium/css/index#add-a-pseudostate-to-a-class "Adicionar um PseudoState a uma classe-introdução ao exibir e alterar CSS"  
[DevToolsCSSGetStartedTutorial]: /microsoft-edge/devtools-guide-chromium/css/index#view-the-css-for-an-element "Exibir o CSS para um elemento-introdução à exibição e alteração de CSS"  
[DevToolsCssPrintPreview]: /microsoft-edge/devtools-guide-chromium/css/print-preview "Forçar o Microsoft Edge DevTools no modo de visualização de impressão (tipo de mídia de impressão CSS)"  
[DevToolsJavascriptReferenceFormat]: /microsoft-edge/devtools-guide-chromium/javascript/reference#make-a-minified-file-readable "Torne um arquivo minified legível – referência de depuração de JavaScript"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "O sistema de cores-design do material"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "O modelo de caixa | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Tipos de seletor-específico | MDN"  

> [!NOTE]
> <span data-ttu-id="5c910-434">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="5c910-434">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5c910-435">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/css/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5c910-435">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5c910-437">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5c910-437">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
