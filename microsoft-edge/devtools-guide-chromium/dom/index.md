---
title: Começar a exibir e alterar o DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 6d41b072a8bd19ae728cc02b43eb2f843d91b332
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991208"
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





# <span data-ttu-id="99731-103">Começar a exibir e alterar o DOM</span><span class="sxs-lookup"><span data-stu-id="99731-103">Get started with viewing and changing the DOM</span></span>   



<span data-ttu-id="99731-104">Preencha esses tutoriais interativos para aprender as noções básicas de como Visualizar e alterar o DOM de uma página usando o Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="99731-104">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="99731-105">Este tutorial pressupõe que você saiba a diferença entre o DOM e o HTML.</span><span class="sxs-lookup"><span data-stu-id="99731-105">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="99731-106">Consulte [Apêndice: HTML versus o dom](#appendix-html-versus-the-dom) para obter uma explicação.</span><span class="sxs-lookup"><span data-stu-id="99731-106">See [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <span data-ttu-id="99731-107">Exemplos abertos do DOM</span><span class="sxs-lookup"><span data-stu-id="99731-107">Open DOM examples</span></span>  

1.  <span data-ttu-id="99731-108">Segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e clique em **exemplos de Dom** para abrir em uma nova guia.</span><span class="sxs-lookup"><span data-stu-id="99731-108">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="99731-109">Exemplos de DOM</span><span class="sxs-lookup"><span data-stu-id="99731-109">DOM Examples</span></span>][GlitchDomExamples]  
    
## <span data-ttu-id="99731-110">Exibir nós DOM</span><span class="sxs-lookup"><span data-stu-id="99731-110">View DOM nodes</span></span>   

<span data-ttu-id="99731-111">A árvore DOM do painel elementos é onde você faz todas as atividades relacionadas ao DOM no DevTools.</span><span class="sxs-lookup"><span data-stu-id="99731-111">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <span data-ttu-id="99731-112">Inspecionar um nó</span><span class="sxs-lookup"><span data-stu-id="99731-112">Inspect a node</span></span>   

<span data-ttu-id="99731-113">Quando você está interessado em um nó DOM específico, **inspecionar** é uma maneira rápida de abrir o devtools e investigar esse nó.</span><span class="sxs-lookup"><span data-stu-id="99731-113">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="99731-114">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="99731-114">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="99731-115">Em **inspecionar um nó**, clique com o botão direito do mouse em **Michelangelo** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="99731-115">Under **Inspect a Node**, right-click **Michelangelo** and select **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Inspecionar um nó" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       <span data-ttu-id="99731-117">Inspecionar um nó</span><span class="sxs-lookup"><span data-stu-id="99731-117">Inspect a node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="99731-118">O painel **elementos** do devtools é aberto.</span><span class="sxs-lookup"><span data-stu-id="99731-118">The **Elements** panel of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="99731-119">é realçado na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="99731-119">is highlighted in the **DOM Tree**.</span></span>  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Realce o nó Michelangelo" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           <span data-ttu-id="99731-121">Realce o `Michelangelo` nó</span><span class="sxs-lookup"><span data-stu-id="99731-121">Highlight the `Michelangelo` node</span></span>  
        :::image-end:::  
        
        1.  <span data-ttu-id="99731-122">Clique no ícone **inspecionar** \ ( ![ inspecionar ][ImageInspectIcon] \) no canto superior esquerdo do devtools.</span><span class="sxs-lookup"><span data-stu-id="99731-122">Click the **Inspect** \(![Inspect][ImageInspectIcon]\) icon in the top-left corner of DevTools.</span></span>  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="O ícone inspecionar" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               <span data-ttu-id="99731-124">O ícone **inspecionar**</span><span class="sxs-lookup"><span data-stu-id="99731-124">The **Inspect** icon</span></span>  
            :::image-end:::  
            
1.  <span data-ttu-id="99731-125">Em **inspecionar um nó**, clique no texto de **Tóquio** .</span><span class="sxs-lookup"><span data-stu-id="99731-125">Under **Inspect a Node**, click the **Tokyo** text.</span></span>  <span data-ttu-id="99731-126">Agora `<li>Tokyo</li>` está realçado na árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="99731-126">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="99731-127">Inspecionar um nó também é a primeira etapa em direção à exibição e alteração dos estilos de um nó.</span><span class="sxs-lookup"><span data-stu-id="99731-127">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="99731-128">Confira [introdução à exibição e à alteração da CSS][DevToolsCssGetStarted].</span><span class="sxs-lookup"><span data-stu-id="99731-128">See [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <span data-ttu-id="99731-129">Navegar pela árvore DOM com um teclado</span><span class="sxs-lookup"><span data-stu-id="99731-129">Navigate the DOM Tree with a keyboard</span></span>   

<span data-ttu-id="99731-130">Depois de selecionar um nó na árvore DOM, você poderá navegar pela árvore DOM com o teclado.</span><span class="sxs-lookup"><span data-stu-id="99731-130">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="99731-131">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="99731-131">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="99731-132">Em **navegar pela árvore DOM com um teclado**, clique com o botão direito do mouse em **Ringo** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="99731-132">Under **Navigate the DOM Tree with a Keyboard**, right-click **Ringo** and select **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="99731-133">está selecionado na árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="99731-133">is selected in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Inspecione o nó Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       <span data-ttu-id="99731-135">Inspecionar o `Ringo` nó</span><span class="sxs-lookup"><span data-stu-id="99731-135">Inspect the `Ringo` node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="99731-136">Pressione a `Up` tecla de direção 2 vezes.</span><span class="sxs-lookup"><span data-stu-id="99731-136">Press the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="99731-137"> está selecionada.</span><span class="sxs-lookup"><span data-stu-id="99731-137">is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Inspecionar o nó UL" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           <span data-ttu-id="99731-139">Inspecionar o `ul` nó</span><span class="sxs-lookup"><span data-stu-id="99731-139">Inspect the `ul` node</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="99731-140">Pressione a `Left` tecla de direção.</span><span class="sxs-lookup"><span data-stu-id="99731-140">Press the `Left` arrow key.</span></span>  <span data-ttu-id="99731-141">A `<ul>` lista é recolhida.</span><span class="sxs-lookup"><span data-stu-id="99731-141">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="99731-142">Pressione a `Left` tecla de direção novamente.</span><span class="sxs-lookup"><span data-stu-id="99731-142">Press the `Left` arrow key again.</span></span>  <span data-ttu-id="99731-143">O pai do `<ul>` nó está selecionado.</span><span class="sxs-lookup"><span data-stu-id="99731-143">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="99731-144">Nesse caso, é o `<div>` com ID `navigate-the-dom-tree-with-a-keyboard-1` .</span><span class="sxs-lookup"><span data-stu-id="99731-144">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="99731-145">Pressione a `Down` tecla de direção 2 vezes para selecionar novamente a `<ul>` lista que você acabou de recolhido.</span><span class="sxs-lookup"><span data-stu-id="99731-145">Press the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="99731-146">Ele deve ser assim:</span><span class="sxs-lookup"><span data-stu-id="99731-146">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="99731-147">Pressione a `Right` tecla de direção.</span><span class="sxs-lookup"><span data-stu-id="99731-147">Press the `Right` arrow key.</span></span>  <span data-ttu-id="99731-148">A lista é expandida.</span><span class="sxs-lookup"><span data-stu-id="99731-148">The list expands.</span></span>  

### <span data-ttu-id="99731-149">Rolar para o modo de exibição</span><span class="sxs-lookup"><span data-stu-id="99731-149">Scroll into view</span></span>   

<span data-ttu-id="99731-150">Ao exibir a árvore DOM, você pode estar interessado em um nó DOM que não está no visor no momento.</span><span class="sxs-lookup"><span data-stu-id="99731-150">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="99731-151">Por exemplo, suponha que você tenha rolagem para a parte inferior da página e esteja interessado no `<h1>` nó na parte superior da página.</span><span class="sxs-lookup"><span data-stu-id="99731-151">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="99731-152">**Acessar o modo de exibição** permite reposicionar rapidamente o visor para que você possa ver o nó.</span><span class="sxs-lookup"><span data-stu-id="99731-152">**Scroll into view** lets you quickly reposition the viewport so that you are able to see the node.</span></span>  

1.  <span data-ttu-id="99731-153">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="99731-153">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="99731-154">Em **rolar para a exibição**, clique com o botão direito do mouse em **Magritte** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="99731-154">Under **Scroll into View**, right-click **Magritte** and select **Inspect**.</span></span>  
1.  <span data-ttu-id="99731-155">Role até a parte inferior da página de exemplos do DOM.</span><span class="sxs-lookup"><span data-stu-id="99731-155">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="99731-156">O `<li>Magritte</li>` nó ainda deve ser selecionado na sua árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="99731-156">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="99731-157">Caso contrário, volte para rolar para o [modo de exibição](#scroll-into-view) e recomeçar.</span><span class="sxs-lookup"><span data-stu-id="99731-157">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="99731-158">Clique com o botão direito do mouse no `<li>Magritte</li>` nó e selecione **rolar para o modo de exibição**.</span><span class="sxs-lookup"><span data-stu-id="99731-158">Right-click the `<li>Magritte</li>` node and select **Scroll into view**.</span></span>  <span data-ttu-id="99731-159">O visor rola novamente para que você possa ver o nó **Magritte** .</span><span class="sxs-lookup"><span data-stu-id="99731-159">Your viewport scrolls back up so that you may see the **Magritte** node.</span></span>  <span data-ttu-id="99731-160">Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não conseguir ver a opção **rolar para a exibição** .</span><span class="sxs-lookup"><span data-stu-id="99731-160">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.</span></span>
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Rolar para o modo de exibição" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **<span data-ttu-id="99731-162">Rolar para o modo de exibição</span><span class="sxs-lookup"><span data-stu-id="99731-162">Scroll into view</span></span>**  
    :::image-end:::  

### <span data-ttu-id="99731-163">Pesquisar nós</span><span class="sxs-lookup"><span data-stu-id="99731-163">Search for nodes</span></span>   

<span data-ttu-id="99731-164">Você pode pesquisar a árvore DOM por cadeia de caracteres, seletor de CSS ou seletor XPath.</span><span class="sxs-lookup"><span data-stu-id="99731-164">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="99731-165">Focalize o cursor no painel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="99731-165">Focus your cursor on the **Elements** panel.</span></span>  
1.  <span data-ttu-id="99731-166">Pressione `Control` + `F` \ (Windows \) ou `Command` + `F` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="99731-166">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="99731-167">A barra de pesquisa é aberta na parte inferior da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="99731-167">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="99731-168">Digite `The Moon is a Harsh Mistress`.</span><span class="sxs-lookup"><span data-stu-id="99731-168">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="99731-169">A última sentença é realçada na árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="99731-169">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Realçar a consulta na barra de pesquisa" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       <span data-ttu-id="99731-171">Realçar a consulta na barra de pesquisa</span><span class="sxs-lookup"><span data-stu-id="99731-171">Highlight the query in the Search bar</span></span>  
    :::image-end:::  
    
<span data-ttu-id="99731-172">Conforme mencionado acima, a barra de pesquisa também oferece suporte a seletores CSS e XPath.</span><span class="sxs-lookup"><span data-stu-id="99731-172">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <span data-ttu-id="99731-173">Editar o DOM</span><span class="sxs-lookup"><span data-stu-id="99731-173">Edit the DOM</span></span>   

<span data-ttu-id="99731-174">Você pode editar o DOM instantaneamente e ver como essas alterações afetam a página.</span><span class="sxs-lookup"><span data-stu-id="99731-174">You may edit the DOM on the fly and see how those changes affect the page.</span></span>  

### <span data-ttu-id="99731-175">Editar conteúdo</span><span class="sxs-lookup"><span data-stu-id="99731-175">Edit content</span></span>   

<span data-ttu-id="99731-176">Para editar o conteúdo de um nó, clique duas vezes no conteúdo na árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="99731-176">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="99731-177">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="99731-177">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="99731-178">Em **editar conteúdo**, clique com o botão direito do mouse em **Michelle** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="99731-178">Under **Edit Content**, right-click **Michelle** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="99731-179">Na árvore DOM, clique duas vezes `Michelle` .</span><span class="sxs-lookup"><span data-stu-id="99731-179">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="99731-180">Em outras palavras, clique duas vezes no texto entre `<li>` e `</li>` .</span><span class="sxs-lookup"><span data-stu-id="99731-180">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="99731-181">O texto é realçado para indicar que está selecionado.</span><span class="sxs-lookup"><span data-stu-id="99731-181">The text is highlighted to indicate that it is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Editar o texto" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           <span data-ttu-id="99731-183">Editar o texto</span><span class="sxs-lookup"><span data-stu-id="99731-183">Edit the text</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="99731-184">Excluir `Michelle` , digite `Leela` e, em seguida, pressione `Enter` para confirmar a alteração.</span><span class="sxs-lookup"><span data-stu-id="99731-184">Delete `Michelle`, type `Leela`, then press `Enter` to confirm the change.</span></span>  <span data-ttu-id="99731-185">O texto no DOM muda de **Michelle** para **Leela**.</span><span class="sxs-lookup"><span data-stu-id="99731-185">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <span data-ttu-id="99731-186">Editar atributos</span><span class="sxs-lookup"><span data-stu-id="99731-186">Edit attributes</span></span>   

<span data-ttu-id="99731-187">Para editar atributos, clique duas vezes no nome ou no valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="99731-187">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="99731-188">Siga as instruções para saber como adicionar atributos a um nó.</span><span class="sxs-lookup"><span data-stu-id="99731-188">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="99731-189">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="99731-189">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="99731-190">Em **Editar atributos**, clique com o botão direito do mouse em **Howard** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="99731-190">Under **Edit Attributes**, right-click **Howard** and select **Inspect**.</span></span>  
1.  <span data-ttu-id="99731-191">Clique duas vezes `<li>` .</span><span class="sxs-lookup"><span data-stu-id="99731-191">Double-click `<li>`.</span></span>  <span data-ttu-id="99731-192">O texto é realçado para indicar que o nó está selecionado.</span><span class="sxs-lookup"><span data-stu-id="99731-192">The text is highlighted to indicate that the node is selected.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Editar o nó" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       <span data-ttu-id="99731-194">Editar o nó</span><span class="sxs-lookup"><span data-stu-id="99731-194">Edit the node</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="99731-195">Pressione a `Right` tecla de seta, adicione um espaço, digite `style="background-color:gold"` e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="99731-195">Press the `Right` arrow key, add a space, type `style="background-color:gold"`, and then press `Enter`.</span></span>  <span data-ttu-id="99731-196">A cor da tela de fundo do nó muda para ouro.</span><span class="sxs-lookup"><span data-stu-id="99731-196">The background color of the node changes to gold.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Adicionar um atributo Style ao nó" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       <span data-ttu-id="99731-198">Adicionar um `style` atributo ao nó</span><span class="sxs-lookup"><span data-stu-id="99731-198">Add a `style` attribute to the node</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="99731-199">Editar tipo de nó</span><span class="sxs-lookup"><span data-stu-id="99731-199">Edit node type</span></span>   

<span data-ttu-id="99731-200">Para editar o tipo de um nó, clique duas vezes no tipo e, em seguida, digite o novo tipo.</span><span class="sxs-lookup"><span data-stu-id="99731-200">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="99731-201">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="99731-201">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="99731-202">Em **Editar tipo de nó**, clique com o botão direito do mouse em **Hank** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="99731-202">Under **Edit Node Type**, right-click **Hank** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="99731-203">Clique duas vezes `<li>` .</span><span class="sxs-lookup"><span data-stu-id="99731-203">Double-click `<li>`.</span></span>  <span data-ttu-id="99731-204">O texto `li` é realçado.</span><span class="sxs-lookup"><span data-stu-id="99731-204">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="99731-205">Excluir `li` , digite `button` e, em seguida, pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="99731-205">Delete `li`, type `button`, then press `Enter`.</span></span>  <span data-ttu-id="99731-206">O `<li>` nó muda para um `<button>` nó.</span><span class="sxs-lookup"><span data-stu-id="99731-206">The `<li>` node changes to a `<button>` node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Alterar o botão do tipo de nó" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           <span data-ttu-id="99731-208">Alterar o tipo de nó para</span><span class="sxs-lookup"><span data-stu-id="99731-208">Change the node type to</span></span> `button`  
        :::image-end:::  
        
### <span data-ttu-id="99731-209">Reordenar nós DOM</span><span class="sxs-lookup"><span data-stu-id="99731-209">Reorder DOM nodes</span></span>   

<span data-ttu-id="99731-210">Arraste os nós para reorganizá-los.</span><span class="sxs-lookup"><span data-stu-id="99731-210">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="99731-211">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="99731-211">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="99731-212">Em **Reordenar nós dom**, clique com o botão direito do mouse em **Elvis Presley** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="99731-212">Under **Reorder DOM Nodes**, right-click **Elvis Presley** and select **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="99731-213">É o último item na lista.</span><span class="sxs-lookup"><span data-stu-id="99731-213">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="99731-214">Na árvore DOM, arraste `<li>Elvis Presley</li>` para a parte superior da lista.</span><span class="sxs-lookup"><span data-stu-id="99731-214">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Arraste o nó para a parte superior da lista" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           <span data-ttu-id="99731-216">Arraste o nó para a parte superior da lista</span><span class="sxs-lookup"><span data-stu-id="99731-216">Drag the node to the top of the list</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="99731-217">Forçar estado</span><span class="sxs-lookup"><span data-stu-id="99731-217">Force state</span></span>   

<span data-ttu-id="99731-218">Você pode forçar os nós a permanecer nos Estados, incluindo `:active` ,,, `:hover` `:focus` `:visited` e `:focus-within` .</span><span class="sxs-lookup"><span data-stu-id="99731-218">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="99731-219">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="99731-219">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="99731-220">Em **forçar estado**, passe o mouse sobre **o Lord dos voa**.</span><span class="sxs-lookup"><span data-stu-id="99731-220">Under **Force state**, hover over **The Lord of the Flies**.</span></span>  <span data-ttu-id="99731-221">A cor do plano de fundo se torna laranja.</span><span class="sxs-lookup"><span data-stu-id="99731-221">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="99731-222">Clique com o botão direito do mouse **no Lord dos voas** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="99731-222">Right-click **The Lord of the Flies** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="99731-223">Clique com o botão direito do mouse `<li class="demo--hover">The Lord of the Flies</li>` e selecione **forçar estado**  >  **: focalizar**.</span><span class="sxs-lookup"><span data-stu-id="99731-223">Right-click `<li class="demo--hover">The Lord of the Flies</li>` and select **Force State** > **:hover**.</span></span>  <span data-ttu-id="99731-224">Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não vir essa opção.</span><span class="sxs-lookup"><span data-stu-id="99731-224">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  <span data-ttu-id="99731-225">A cor do plano de fundo permanece laranja, mesmo que você não esteja efetivamente passando o mouse sobre o nó.</span><span class="sxs-lookup"><span data-stu-id="99731-225">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <span data-ttu-id="99731-226">Ocultar um nó</span><span class="sxs-lookup"><span data-stu-id="99731-226">Hide a node</span></span>   

<span data-ttu-id="99731-227">Pressione `H` para ocultar um nó.</span><span class="sxs-lookup"><span data-stu-id="99731-227">Press `H` to hide a node.</span></span>  

1.  <span data-ttu-id="99731-228">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="99731-228">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="99731-229">Em **ocultar um nó**, clique com o botão direito **do mouse no meu destino de estrelas** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="99731-229">Under **Hide a node**, right-click **The Stars My Destination** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="99731-230">Pressione a `H` tecla.</span><span class="sxs-lookup"><span data-stu-id="99731-230">Press the `H` key.</span></span>  <span data-ttu-id="99731-231">O nó está oculto.</span><span class="sxs-lookup"><span data-stu-id="99731-231">The node is hidden.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Qual é a aparência do nó na árvore DOM após ele estar oculto" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           <span data-ttu-id="99731-233">Qual é a aparência do nó na árvore DOM após ele estar oculto</span><span class="sxs-lookup"><span data-stu-id="99731-233">What the node looks like in the DOM Tree after it is hidden</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="99731-234">Pressione a `H` tecla novamente.</span><span class="sxs-lookup"><span data-stu-id="99731-234">Press the `H` key again.</span></span>  <span data-ttu-id="99731-235">O nó é mostrado novamente.</span><span class="sxs-lookup"><span data-stu-id="99731-235">The node is shown again.</span></span>  

### <span data-ttu-id="99731-236">Excluir um nó</span><span class="sxs-lookup"><span data-stu-id="99731-236">Delete a node</span></span>   

<span data-ttu-id="99731-237">Pressione `Delete` para excluir um nó.</span><span class="sxs-lookup"><span data-stu-id="99731-237">Press `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="99731-238">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="99731-238">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="99731-239">Em **excluir um nó**, clique com o botão direito do mouse em **base** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="99731-239">Under **Delete a Node**, right-click **Foundation** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="99731-240">Pressione a `Delete` tecla.</span><span class="sxs-lookup"><span data-stu-id="99731-240">Press the `Delete` key.</span></span>  <span data-ttu-id="99731-241">O nó é excluído.</span><span class="sxs-lookup"><span data-stu-id="99731-241">The node is deleted.</span></span>  
    1.  <span data-ttu-id="99731-242">Pressione `Control` + `Z` \ (Windows \) ou `Command` + `Z` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="99731-242">Press `Control`+`Z` \(Windows\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="99731-243">A última ação é desfeita e o nó é exibido novamente.</span><span class="sxs-lookup"><span data-stu-id="99731-243">The last action is undone and the node reappears.</span></span>  

## <span data-ttu-id="99731-244">Acessar nós no console</span><span class="sxs-lookup"><span data-stu-id="99731-244">Access nodes in the Console</span></span>   

<span data-ttu-id="99731-245">O DevTools fornece alguns atalhos para acessar nós DOM do console ou obter referências de JavaScript a cada um.</span><span class="sxs-lookup"><span data-stu-id="99731-245">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <span data-ttu-id="99731-246">Fazer referência ao nó atualmente selecionado com o $0</span><span class="sxs-lookup"><span data-stu-id="99731-246">Reference the currently-selected node with $0</span></span>   

<span data-ttu-id="99731-247">Quando você inspeciona um nó, o `== $0` texto ao lado do nó significa que você pode fazer referência a esse nó no console com a variável `$0` .</span><span class="sxs-lookup"><span data-stu-id="99731-247">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="99731-248">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="99731-248">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="99731-249">Em **referenciar o nó selecionado no momento com o $0**, clique com o botão direito do mouse **na mão esquerda da escuridão** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="99731-249">Under **Reference the currently-selected node with $0**, right-click **The Left Hand of Darkness** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="99731-250">Pressione a `Escape` tecla para abrir a gaveta do console.</span><span class="sxs-lookup"><span data-stu-id="99731-250">Press the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="99731-251">Digite `$0` e pressione a `Enter` tecla.</span><span class="sxs-lookup"><span data-stu-id="99731-251">Type `$0` and press the `Enter` key.</span></span>  <span data-ttu-id="99731-252">O resultado da expressão mostra que `$0` é avaliado como `<li>The Left Hand of Darkness</li>` .</span><span class="sxs-lookup"><span data-stu-id="99731-252">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="O resultado da primeira expressão $0 no console" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            <span data-ttu-id="99731-254">O resultado da primeira `$0` expressão no **console**</span><span class="sxs-lookup"><span data-stu-id="99731-254">The result of the first `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="99731-255">Passe o mouse sobre o resultado.</span><span class="sxs-lookup"><span data-stu-id="99731-255">Hover over the result.</span></span>  <span data-ttu-id="99731-256">O nó é realçado no visor.</span><span class="sxs-lookup"><span data-stu-id="99731-256">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="99731-257">Clique `<li>Dune</li>` na árvore DOM, digite `$0` novamente no console e pressione `Enter` novamente.</span><span class="sxs-lookup"><span data-stu-id="99731-257">Click `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then press `Enter` again.</span></span>  <span data-ttu-id="99731-258">Agora, `$0` é avaliada como `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="99731-258">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="O resultado da segunda expressão $0 no console" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           <span data-ttu-id="99731-260">O resultado da segunda `$0` expressão no **console**</span><span class="sxs-lookup"><span data-stu-id="99731-260">The result of the second `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="99731-261">Armazenar como variável global</span><span class="sxs-lookup"><span data-stu-id="99731-261">Store as global variable</span></span>   

<span data-ttu-id="99731-262">Se você precisar consultar novamente um nó muitas vezes, armazene-o como uma variável global.</span><span class="sxs-lookup"><span data-stu-id="99731-262">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="99731-263">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="99731-263">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="99731-264">Em **armazenar como variável global**, clique com o botão direito **do mouse na grande suspensão** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="99731-264">Under **Store as global variable**, right-click **The Big Sleep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="99731-265">Clique com o botão direito do mouse `<li>The Big Sleep</li>` na árvore DOM e selecione **armazenar como variável global**.</span><span class="sxs-lookup"><span data-stu-id="99731-265">Right-click `<li>The Big Sleep</li>` in the DOM Tree and select **Store as global variable**.</span></span>  <span data-ttu-id="99731-266">Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não vir essa opção.</span><span class="sxs-lookup"><span data-stu-id="99731-266">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  
    1.  <span data-ttu-id="99731-267">Digite `temp1` o console e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="99731-267">Type `temp1` in the Console and then press `Enter`.</span></span>  <span data-ttu-id="99731-268">O resultado da expressão mostra que a variável é avaliada como o nó.</span><span class="sxs-lookup"><span data-stu-id="99731-268">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="O resultado da expressão temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           <span data-ttu-id="99731-270">O resultado da `temp1` expressão</span><span class="sxs-lookup"><span data-stu-id="99731-270">The result of the `temp1` expression</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="99731-271">Copiar caminho do JS</span><span class="sxs-lookup"><span data-stu-id="99731-271">Copy JS path</span></span>   

<span data-ttu-id="99731-272">Copie o caminho JavaScript para um nó quando precisar referenciá-lo em um teste automatizado.</span><span class="sxs-lookup"><span data-stu-id="99731-272">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="99731-273">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="99731-273">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="99731-274">Em **copiar o caminho do js**, clique com o botão direito **do mouse na Karamazov da Brothers** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="99731-274">Under **Copy JS path**, right-click **The Brothers Karamazov** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="99731-275">Clique com o botão direito do mouse `<li>The Brothers Karamazov</li>` na árvore DOM e selecione **copiar**o  >  **caminho do js**.</span><span class="sxs-lookup"><span data-stu-id="99731-275">Right-click `<li>The Brothers Karamazov</li>` in the DOM Tree and select **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="99731-276">Uma `document.querySelector()` expressão que é resolvida para o nó foi copiada para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="99731-276">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="99731-277">Pressione `Control` + `V` \ (Windows \) ou `Command` + `V` \ (MacOS \) para colar a expressão no console.</span><span class="sxs-lookup"><span data-stu-id="99731-277">Press `Control`+`V` \(Windows\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="99731-278">Pressione `Enter` para avaliar a expressão.</span><span class="sxs-lookup"><span data-stu-id="99731-278">Press `Enter` to evaluate the expression.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="O resultado da expressão de caminho do JS de cópia" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           <span data-ttu-id="99731-280">O resultado da expressão de **caminho do js de cópia**</span><span class="sxs-lookup"><span data-stu-id="99731-280">The result of the **Copy JS Path** expression</span></span>  
        :::image-end:::  
        
## <span data-ttu-id="99731-281">Interromper alterações de DOM</span><span class="sxs-lookup"><span data-stu-id="99731-281">Break on DOM changes</span></span>   

<span data-ttu-id="99731-282">O DevTools permite pausar o JavaScript de uma página quando o JavaScript modifica o DOM.</span><span class="sxs-lookup"><span data-stu-id="99731-282">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <span data-ttu-id="99731-283">Interromper alterações de atributo</span><span class="sxs-lookup"><span data-stu-id="99731-283">Break on attribute modifications</span></span>   

<span data-ttu-id="99731-284">Use pontos de interrupção de modificação de atributo quando você quiser pausar o JavaScript que faz com que qualquer atributo de um nó seja alterado.</span><span class="sxs-lookup"><span data-stu-id="99731-284">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="99731-285">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="99731-285">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="99731-286">Em **interromper as modificações de atributo**, clique com o botão direito do mouse em **sauerkraut** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="99731-286">Under **Break on attribute modifications**, right-click **Sauerkraut** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="99731-287">Na árvore DOM, clique com o botão direito do mouse `<li id="target">Sauerkraut</li>` e selecione **interromper nas**  >  **modificações de atributo**.</span><span class="sxs-lookup"><span data-stu-id="99731-287">In the DOM Tree, right-click `<li id="target">Sauerkraut</li>` and select **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="99731-288">Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não conseguir ver esta opção.</span><span class="sxs-lookup"><span data-stu-id="99731-288">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Interromper alterações de atributo" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **<span data-ttu-id="99731-290">Interromper alterações de atributo</span><span class="sxs-lookup"><span data-stu-id="99731-290">Break on attribute modifications</span></span>**  
        :::image-end:::  
        
    1.  <span data-ttu-id="99731-291">Na próxima etapa, você será instruído a clicar em um botão que Pause o código da página.</span><span class="sxs-lookup"><span data-stu-id="99731-291">In the next step you are going to be instructed to click a button that pauses the code of the page.</span></span>  <span data-ttu-id="99731-292">Depois que a página for pausada, você não poderá mais rolar a página.</span><span class="sxs-lookup"><span data-stu-id="99731-292">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="99731-293">Você deve clicar em **retomar script** \ ( ![ continuar script ][ImageResumeScriptIcon] \) para que a página seja rolável novamente.</span><span class="sxs-lookup"><span data-stu-id="99731-293">You must click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\) in order to make the page scrollable again.</span></span>
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Onde continuar a execução do script" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           <span data-ttu-id="99731-295">Onde continuar a execução do script</span><span class="sxs-lookup"><span data-stu-id="99731-295">Where to resume script running</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="99731-296">Clique no botão **definir plano de fundo** acima.</span><span class="sxs-lookup"><span data-stu-id="99731-296">Click the **Set Background** button above.</span></span>  <span data-ttu-id="99731-297">Isso define o `style` atributo do nó para `background-color:thistle` .</span><span class="sxs-lookup"><span data-stu-id="99731-297">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="99731-298">DevTools pausará a página e realçará o código que fez com que o atributo fosse alterado.</span><span class="sxs-lookup"><span data-stu-id="99731-298">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="99731-299">Clique em **retomar script** \ ( ![ continuar script ][ImageResumeScriptIcon] \), conforme mencionado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="99731-299">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\), as mentioned earlier.</span></span>  
    
### <span data-ttu-id="99731-300">Interromper a remoção do nó</span><span class="sxs-lookup"><span data-stu-id="99731-300">Break on node removal</span></span>   

<span data-ttu-id="99731-301">Se você quiser pausar quando um nó específico for removido, use pontos de interrupção de remoção de nó.</span><span class="sxs-lookup"><span data-stu-id="99731-301">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="99731-302">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="99731-302">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="99731-303">Em **interromper a remoção do nó**, clique com o botão direito do mouse em **Neuromancer** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="99731-303">Under **Break on Node Removal**, right-click **Neuromancer** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="99731-304">Na árvore DOM, clique com o botão direito do mouse `<li id="target">Neuromancer</li>` e selecione **interromper na**  >  **remoção do nó**.</span><span class="sxs-lookup"><span data-stu-id="99731-304">In the DOM Tree, right-click `<li id="target">Neuromancer</li>` and select **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="99731-305">Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não conseguir ver esta opção.</span><span class="sxs-lookup"><span data-stu-id="99731-305">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="99731-306">Clique no botão **excluir** acima.</span><span class="sxs-lookup"><span data-stu-id="99731-306">Click the **Delete** button above.</span></span>  <span data-ttu-id="99731-307">DevTools pausará a página e realçará o código que fez com que o nó fosse removido.</span><span class="sxs-lookup"><span data-stu-id="99731-307">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="99731-308">Clique em **retomar script** \ ( ![ retomar script ][ImageResumeScriptIcon] \).</span><span class="sxs-lookup"><span data-stu-id="99731-308">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
### <span data-ttu-id="99731-309">Interromper modificações de subárvore</span><span class="sxs-lookup"><span data-stu-id="99731-309">Break on subtree modifications</span></span>   

<span data-ttu-id="99731-310">Depois que você colocar um ponto de interrupção de modificação de subárvore em um nó, o DevTools pausará a página quando qualquer um dos descendentes do nó for adicionado ou removido.</span><span class="sxs-lookup"><span data-stu-id="99731-310">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="99731-311">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="99731-311">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="99731-312">Em **interromper modificações de subárvore**, clique com o botão direito do mouse em **um incêndio na profundidade** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="99731-312">Under **Break on Subtree Modifications**, right-click **A Fire Upon The Deep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="99731-313">Na árvore DOM, clique com o botão direito do mouse `<ul id="target">` , que é o nó acima `<li>A Fire Upon the Deep</li>` e selecione **interromper**  >  **alterações de subárvore**.</span><span class="sxs-lookup"><span data-stu-id="99731-313">In the DOM Tree, right-click `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, and select **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="99731-314">Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não conseguir ver esta opção.</span><span class="sxs-lookup"><span data-stu-id="99731-314">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="99731-315">Clique em **Adicionar filho**.</span><span class="sxs-lookup"><span data-stu-id="99731-315">Click **Add Child**.</span></span>  <span data-ttu-id="99731-316">O código é pausado porque um `<li>` nó foi adicionado à lista.</span><span class="sxs-lookup"><span data-stu-id="99731-316">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="99731-317">Clique em **retomar script** \ ( ![ retomar script ][ImageResumeScriptIcon] \).</span><span class="sxs-lookup"><span data-stu-id="99731-317">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
## <span data-ttu-id="99731-318">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="99731-318">Next steps</span></span>   

<span data-ttu-id="99731-319">Isso abrange a maioria dos recursos relacionados ao DOM no DevTools.</span><span class="sxs-lookup"><span data-stu-id="99731-319">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="99731-320">Você pode descobrir o restante deles clicando com o botão direito do mouse nos nós na árvore DOM e experimentando as outras opções que não foram abordadas neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="99731-320">You are able to discover the rest of them by right-clicking nodes in the DOM Tree and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="99731-321">Consulte também [atalhos de teclado do painel elementos][DevToolsShortcutsElements].</span><span class="sxs-lookup"><span data-stu-id="99731-321">See also [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="99731-322">Confira a [Home Page do Microsoft Edge devtools][MicrosoftEdgeDevTools] para descobrir tudo o que você pode fazer com o devtools.</span><span class="sxs-lookup"><span data-stu-id="99731-322">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--See [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  



## <span data-ttu-id="99731-323">Apêndice: HTML versus DOM</span><span class="sxs-lookup"><span data-stu-id="99731-323">Appendix: HTML versus the DOM</span></span>   

<span data-ttu-id="99731-324">A seção a seguir explica rapidamente a diferença entre HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="99731-324">The following section quickly explains the difference between HTML and the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="99731-325">Quando você usa um navegador da Web para solicitar uma página, o servidor retorna HTML como o trecho de código a seguir</span><span class="sxs-lookup"><span data-stu-id="99731-325">When you use a web browser to request a page, the server returns HTML like the following code snippet</span></span>  

      ```html
      <!doctype html>
      <html>
          <head>
              <title>Hello, world!</title>
          </head>
          <body>
              <h1>Hello, world!</h1>
              <p>This is a hypertext document on the World Wide Web.</p>
              <script src="/script.js" async></script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="99731-326">O navegador analisa o HTML e cria uma árvore de objetos como a lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="99731-326">The browser parses the HTML and creates a tree of objects like the following list.</span></span>  
      
      ```dom
      html
          head
              title
          body
              h1
              p
              script
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="99731-327">Essa árvore de objetos, ou nós, que representa o conteúdo da página é chamada de DOM.</span><span class="sxs-lookup"><span data-stu-id="99731-327">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="99731-328">No momento, ele tem a mesma aparência do HTML, mas suponha que o script referenciado na parte inferior do HTML executa o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="99731-328">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs the following code snippet.</span></span>  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="99731-329">Esse código remove o `h1` nó e adiciona outro `p` nó ao dom.</span><span class="sxs-lookup"><span data-stu-id="99731-329">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="99731-330">O DOM completo agora exibe a lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="99731-330">The complete DOM now displays the following list.</span></span>  
      
      ```dom
      html
          head
              title
          body
              p
              script
              p
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="99731-331">O HTML da página agora é diferente do DOM.</span><span class="sxs-lookup"><span data-stu-id="99731-331">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="99731-332">Em outras palavras, HTML representa o conteúdo inicial da página, e o DOM representa o conteúdo da página atual.</span><span class="sxs-lookup"><span data-stu-id="99731-332">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="99731-333">Quando o JavaScript adiciona, remove ou edita nós, o DOM se torna diferente do HTML.</span><span class="sxs-lookup"><span data-stu-id="99731-333">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="99731-334">Consulte [introdução ao dom][MDNIntroductionToDOM] para saber mais.</span><span class="sxs-lookup"><span data-stu-id="99731-334">See [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view   

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and select **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    > ##### Figure 19  
    > Scroll into view  
    > :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
   Scroll into view  
:::image-end:::  
    -->  

## <span data-ttu-id="99731-335">Apêndice: opções ausentes</span><span class="sxs-lookup"><span data-stu-id="99731-335">Appendix: Missing options</span></span>   

<span data-ttu-id="99731-336">Muitas das instruções neste tutorial instruem você a clicar com o botão direito do mouse em um nó na árvore DOM e selecionar uma opção no menu de contexto exibido.</span><span class="sxs-lookup"><span data-stu-id="99731-336">Many of the instructions in this tutorial instruct you to right-click a node in the DOM Tree and then select an option from the context menu that pops up.</span></span>  <span data-ttu-id="99731-337">Se você não vir a opção especificado no menu de contexto, tente clicar com o botão direito do mouse sobre o texto do nó.</span><span class="sxs-lookup"><span data-stu-id="99731-337">If you do not see the specified option in the context menu, try right-clicking away from the node text.</span></span>  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Onde clicar se você não estiver vendo todas as opções" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   <span data-ttu-id="99731-339">Onde clicar se você não estiver vendo todas as opções</span><span class="sxs-lookup"><span data-stu-id="99731-339">Where to click if you are not seeing all the options</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: ../media/resume-script-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge \ (Chromium \) | Documentos da Microsoft"  
[DevToolsCssGetStarted]: ../css/index.md "Introdução ao visualizar e alterar CSS | Documentos da Microsoft"  
[DevToolsShortcutsElements]: ../shortcuts.md#elements-panel-keyboard-shortcuts "Atalhos de teclado do painel elementos-atalhos de teclado do Microsoft Edge DevTools | Documentos da Microsoft"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Exemplo de DOM do Microsoft Edge (Chromium) DevTools | Problema"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introdução ao DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="99731-345">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="99731-345">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="99731-346">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/dom/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="99731-346">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="99731-348">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="99731-348">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
