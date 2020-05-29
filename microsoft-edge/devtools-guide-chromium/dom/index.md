---
title: Começar a exibir e alterar o DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 4dee8b4e3ea927e72c0f98517f264b2c1d453013
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607444"
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





# <span data-ttu-id="519a7-103">Começar a exibir e alterar o DOM</span><span class="sxs-lookup"><span data-stu-id="519a7-103">Get Started With Viewing And Changing The DOM</span></span>   



<span data-ttu-id="519a7-104">Preencha esses tutoriais interativos para aprender as noções básicas de como Visualizar e alterar o DOM de uma página usando o Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="519a7-104">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="519a7-105">Este tutorial pressupõe que você saiba a diferença entre o DOM e o HTML.</span><span class="sxs-lookup"><span data-stu-id="519a7-105">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="519a7-106">Consulte [Apêndice: HTML versus o dom](#appendix-html-versus-the-dom) para obter uma explicação.</span><span class="sxs-lookup"><span data-stu-id="519a7-106">See [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <span data-ttu-id="519a7-107">Exemplos abertos do DOM</span><span class="sxs-lookup"><span data-stu-id="519a7-107">Open DOM Examples</span></span>  

1.  <span data-ttu-id="519a7-108">Segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e clique em **exemplos de Dom** para abrir em uma nova guia.</span><span class="sxs-lookup"><span data-stu-id="519a7-108">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="519a7-109">Exemplos de DOM</span><span class="sxs-lookup"><span data-stu-id="519a7-109">DOM Examples</span></span>][GlitchDomExamples]  
    
## <span data-ttu-id="519a7-110">Exibir nós DOM</span><span class="sxs-lookup"><span data-stu-id="519a7-110">View DOM nodes</span></span>   

<span data-ttu-id="519a7-111">A árvore DOM do painel elementos é onde você faz todas as atividades relacionadas ao DOM no DevTools.</span><span class="sxs-lookup"><span data-stu-id="519a7-111">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <span data-ttu-id="519a7-112">Inspecionar um nó</span><span class="sxs-lookup"><span data-stu-id="519a7-112">Inspect a node</span></span>   

<span data-ttu-id="519a7-113">Quando você está interessado em um nó DOM específico, **inspecionar** é uma maneira rápida de abrir o devtools e investigar esse nó.</span><span class="sxs-lookup"><span data-stu-id="519a7-113">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="519a7-114">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="519a7-114">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="519a7-115">Em **inspecionar um nó**, clique com o botão direito do mouse em **Michelangelo** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-115">Under **Inspect a Node**, right-click **Michelangelo** and select **Inspect**.</span></span>  
    
    > ##### <span data-ttu-id="519a7-116">Figura 1</span><span class="sxs-lookup"><span data-stu-id="519a7-116">Figure 1</span></span>  
    > <span data-ttu-id="519a7-117">Inspecionar um nó</span><span class="sxs-lookup"><span data-stu-id="519a7-117">Inspecting a node</span></span>  
    > ![Inspecionar um nó][ImageInspectingNode]  
    
    1.  <span data-ttu-id="519a7-119">O painel **elementos** do devtools é aberto.</span><span class="sxs-lookup"><span data-stu-id="519a7-119">The **Elements** panel of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="519a7-120">é realçado na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="519a7-120">is highlighted in the **DOM Tree**.</span></span>  
        
        > ##### <span data-ttu-id="519a7-121">Figura 2</span><span class="sxs-lookup"><span data-stu-id="519a7-121">Figure 2</span></span>  
        > <span data-ttu-id="519a7-122">Realçando o nó Michelangelo</span><span class="sxs-lookup"><span data-stu-id="519a7-122">Highlighting the Michelangelo node</span></span>  
        > ![Realçando o nó Michelangelo][ImageHighlightingMichelangeloNode]  
        
        1.  <span data-ttu-id="519a7-124">Clique no ícone **inspecionar** ![ inspeção ][ImageInspectIcon] no canto superior esquerdo do devtools.</span><span class="sxs-lookup"><span data-stu-id="519a7-124">Click the **Inspect** ![Inspect][ImageInspectIcon] icon in the top-left corner of DevTools.</span></span>  
            
            > ##### <span data-ttu-id="519a7-125">Figura 3</span><span class="sxs-lookup"><span data-stu-id="519a7-125">Figure 3</span></span>  
            > <span data-ttu-id="519a7-126">O ícone inspecionar</span><span class="sxs-lookup"><span data-stu-id="519a7-126">The Inspect icon</span></span>  
            > ![O ícone inspecionar][ImageInspect]  
            
1.  <span data-ttu-id="519a7-128">Em **inspecionar um nó**, clique no texto de **Tóquio** .</span><span class="sxs-lookup"><span data-stu-id="519a7-128">Under **Inspect a Node**, click the **Tokyo** text.</span></span>  <span data-ttu-id="519a7-129">Agora `<li>Tokyo</li>` está realçado na árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="519a7-129">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="519a7-130">Inspecionar um nó também é a primeira etapa em direção à exibição e alteração dos estilos de um nó.</span><span class="sxs-lookup"><span data-stu-id="519a7-130">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="519a7-131">Confira [introdução à exibição e à alteração da CSS][DevToolsCssGetStarted].</span><span class="sxs-lookup"><span data-stu-id="519a7-131">See [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <span data-ttu-id="519a7-132">Navegar pela árvore DOM com um teclado</span><span class="sxs-lookup"><span data-stu-id="519a7-132">Navigate the DOM Tree with a keyboard</span></span>   

<span data-ttu-id="519a7-133">Depois de selecionar um nó na árvore DOM, você poderá navegar pela árvore DOM com o teclado.</span><span class="sxs-lookup"><span data-stu-id="519a7-133">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="519a7-134">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="519a7-134">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="519a7-135">Em **navegar pela árvore DOM com um teclado**, clique com o botão direito do mouse em **Ringo** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-135">Under **Navigate the DOM Tree with a Keyboard**, right-click **Ringo** and select **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="519a7-136">está selecionado na árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="519a7-136">is selected in the DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="519a7-137">Figura 4</span><span class="sxs-lookup"><span data-stu-id="519a7-137">Figure 4</span></span>  
    > <span data-ttu-id="519a7-138">Inspecionar o nó Ringo</span><span class="sxs-lookup"><span data-stu-id="519a7-138">Inspecting the Ringo node</span></span>  
    > ![Inspecionar o nó Ringo][ImageInspectingRingoNode]  
    
    1.  <span data-ttu-id="519a7-140">Pressione a `Up` tecla de direção 2 vezes.</span><span class="sxs-lookup"><span data-stu-id="519a7-140">Press the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="519a7-141"> está selecionada.</span><span class="sxs-lookup"><span data-stu-id="519a7-141">is selected.</span></span>  
        
        > ##### <span data-ttu-id="519a7-142">Figura 5</span><span class="sxs-lookup"><span data-stu-id="519a7-142">Figure 5</span></span>  
        > <span data-ttu-id="519a7-143">Inspecionar o nó UL</span><span class="sxs-lookup"><span data-stu-id="519a7-143">Inspecting the ul node</span></span>  
        > ![Inspecionar o nó UL][ImageInspectingUlNode]  
        
    1.  <span data-ttu-id="519a7-145">Pressione a `Left` tecla de direção.</span><span class="sxs-lookup"><span data-stu-id="519a7-145">Press the `Left` arrow key.</span></span>  <span data-ttu-id="519a7-146">A `<ul>` lista é recolhida.</span><span class="sxs-lookup"><span data-stu-id="519a7-146">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="519a7-147">Pressione a `Left` tecla de direção novamente.</span><span class="sxs-lookup"><span data-stu-id="519a7-147">Press the `Left` arrow key again.</span></span>  <span data-ttu-id="519a7-148">O pai do `<ul>` nó está selecionado.</span><span class="sxs-lookup"><span data-stu-id="519a7-148">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="519a7-149">Nesse caso, é o `<div>` com ID `navigate-the-dom-tree-with-a-keyboard-1` .</span><span class="sxs-lookup"><span data-stu-id="519a7-149">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="519a7-150">Pressione a `Down` tecla de direção 2 vezes para selecionar novamente a `<ul>` lista que você acabou de recolhido.</span><span class="sxs-lookup"><span data-stu-id="519a7-150">Press the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="519a7-151">Ele deve ser assim:</span><span class="sxs-lookup"><span data-stu-id="519a7-151">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="519a7-152">Pressione a `Right` tecla de direção.</span><span class="sxs-lookup"><span data-stu-id="519a7-152">Press the `Right` arrow key.</span></span>  <span data-ttu-id="519a7-153">A lista é expandida.</span><span class="sxs-lookup"><span data-stu-id="519a7-153">The list expands.</span></span>  

### <span data-ttu-id="519a7-154">Rolar para o modo de exibição</span><span class="sxs-lookup"><span data-stu-id="519a7-154">Scroll into view</span></span>   

<span data-ttu-id="519a7-155">Ao exibir a árvore DOM, você pode estar interessado em um nó DOM que não está no visor no momento.</span><span class="sxs-lookup"><span data-stu-id="519a7-155">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="519a7-156">Por exemplo, suponha que você tenha rolagem para a parte inferior da página e esteja interessado no `<h1>` nó na parte superior da página.</span><span class="sxs-lookup"><span data-stu-id="519a7-156">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="519a7-157">**Acessar o modo de exibição** permite reposicionar rapidamente o visor para que você possa ver o nó.</span><span class="sxs-lookup"><span data-stu-id="519a7-157">**Scroll into view** lets you quickly reposition the viewport so that you are able to see the node.</span></span>  

1.  <span data-ttu-id="519a7-158">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="519a7-158">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="519a7-159">Em **rolar para a exibição**, clique com o botão direito do mouse em **Magritte** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-159">Under **Scroll into View**, right-click **Magritte** and select **Inspect**.</span></span>  
1.  <span data-ttu-id="519a7-160">Role até a parte inferior da página de exemplos do DOM.</span><span class="sxs-lookup"><span data-stu-id="519a7-160">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="519a7-161">O `<li>Magritte</li>` nó ainda deve ser selecionado na sua árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="519a7-161">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="519a7-162">Caso contrário, volte para rolar para o [modo de exibição](#scroll-into-view) e recomeçar.</span><span class="sxs-lookup"><span data-stu-id="519a7-162">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="519a7-163">Clique com o botão direito do mouse no `<li>Magritte</li>` nó e selecione **rolar para o modo de exibição**.</span><span class="sxs-lookup"><span data-stu-id="519a7-163">Right-click the `<li>Magritte</li>` node and select **Scroll into view**.</span></span>  <span data-ttu-id="519a7-164">O visor rola novamente para que você possa ver o nó **Magritte** .</span><span class="sxs-lookup"><span data-stu-id="519a7-164">Your viewport scrolls back up so that you may see the **Magritte** node.</span></span>  <span data-ttu-id="519a7-165">Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não conseguir ver a opção **rolar para a exibição** .</span><span class="sxs-lookup"><span data-stu-id="519a7-165">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.</span></span>
    
    > ##### <span data-ttu-id="519a7-166">Figura 6</span><span class="sxs-lookup"><span data-stu-id="519a7-166">Figure 6</span></span>  
    > <span data-ttu-id="519a7-167">Rolar para o modo de exibição</span><span class="sxs-lookup"><span data-stu-id="519a7-167">Scroll into view</span></span>  
    > ![Rolar para o modo de exibição][ImageScrollView]  

### <span data-ttu-id="519a7-169">Pesquisar nós</span><span class="sxs-lookup"><span data-stu-id="519a7-169">Search for nodes</span></span>   

<span data-ttu-id="519a7-170">Você pode pesquisar a árvore DOM por cadeia de caracteres, seletor de CSS ou seletor XPath.</span><span class="sxs-lookup"><span data-stu-id="519a7-170">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="519a7-171">Focalize o cursor no painel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="519a7-171">Focus your cursor on the **Elements** panel.</span></span>  
1.  <span data-ttu-id="519a7-172">Pressione `Control` + `F` \ (Windows \) ou `Command` + `F` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="519a7-172">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="519a7-173">A barra de pesquisa é aberta na parte inferior da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="519a7-173">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="519a7-174">Digite `The Moon is a Harsh Mistress`.</span><span class="sxs-lookup"><span data-stu-id="519a7-174">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="519a7-175">A última sentença é realçada na árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="519a7-175">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="519a7-176">Figura 7</span><span class="sxs-lookup"><span data-stu-id="519a7-176">Figure 7</span></span>  
    > <span data-ttu-id="519a7-177">Realçando a consulta na barra de pesquisa</span><span class="sxs-lookup"><span data-stu-id="519a7-177">Highlighting the query in the Search bar</span></span>  
    > ![Realçando a consulta na barra de pesquisa][ImageHighlightingQuerySearchBar]  
    
<span data-ttu-id="519a7-179">Conforme mencionado acima, a barra de pesquisa também oferece suporte a seletores CSS e XPath.</span><span class="sxs-lookup"><span data-stu-id="519a7-179">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <span data-ttu-id="519a7-180">Editar o DOM</span><span class="sxs-lookup"><span data-stu-id="519a7-180">Edit the DOM</span></span>   

<span data-ttu-id="519a7-181">Você pode editar o DOM instantaneamente e ver como essas alterações afetam a página.</span><span class="sxs-lookup"><span data-stu-id="519a7-181">You may edit the DOM on the fly and see how those changes affect the page.</span></span>  

### <span data-ttu-id="519a7-182">Editar conteúdo</span><span class="sxs-lookup"><span data-stu-id="519a7-182">Edit content</span></span>   

<span data-ttu-id="519a7-183">Para editar o conteúdo de um nó, clique duas vezes no conteúdo na árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="519a7-183">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="519a7-184">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="519a7-184">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="519a7-185">Em **editar conteúdo**, clique com o botão direito do mouse em **Michelle** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-185">Under **Edit Content**, right-click **Michelle** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="519a7-186">Na árvore DOM, clique duas vezes `Michelle` .</span><span class="sxs-lookup"><span data-stu-id="519a7-186">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="519a7-187">Em outras palavras, clique duas vezes no texto entre `<li>` e `</li>` .</span><span class="sxs-lookup"><span data-stu-id="519a7-187">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="519a7-188">O texto é realçado para indicar que está selecionado.</span><span class="sxs-lookup"><span data-stu-id="519a7-188">The text is highlighted to indicate that it is selected.</span></span>  
        
        > ##### <span data-ttu-id="519a7-189">Figura 8</span><span class="sxs-lookup"><span data-stu-id="519a7-189">Figure 8</span></span>  
        > <span data-ttu-id="519a7-190">Editando o texto</span><span class="sxs-lookup"><span data-stu-id="519a7-190">Editing the text</span></span>  
        > ![Editando o texto][ImageEditingText]  
        
    1.  <span data-ttu-id="519a7-192">Excluir `Michelle` , digite `Leela` e, em seguida, pressione `Enter` para confirmar a alteração.</span><span class="sxs-lookup"><span data-stu-id="519a7-192">Delete `Michelle`, type `Leela`, then press `Enter` to confirm the change.</span></span>  <span data-ttu-id="519a7-193">O texto no DOM muda de **Michelle** para **Leela**.</span><span class="sxs-lookup"><span data-stu-id="519a7-193">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <span data-ttu-id="519a7-194">Editar atributos</span><span class="sxs-lookup"><span data-stu-id="519a7-194">Edit attributes</span></span>   

<span data-ttu-id="519a7-195">Para editar atributos, clique duas vezes no nome ou no valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="519a7-195">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="519a7-196">Siga as instruções para saber como adicionar atributos a um nó.</span><span class="sxs-lookup"><span data-stu-id="519a7-196">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="519a7-197">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="519a7-197">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="519a7-198">Em **Editar atributos**, clique com o botão direito do mouse em **Howard** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-198">Under **Edit Attributes**, right-click **Howard** and select **Inspect**.</span></span>  

1.  <span data-ttu-id="519a7-199">Clique duas vezes `<li>` .</span><span class="sxs-lookup"><span data-stu-id="519a7-199">Double-click `<li>`.</span></span>  <span data-ttu-id="519a7-200">O texto é realçado para indicar que o nó está selecionado.</span><span class="sxs-lookup"><span data-stu-id="519a7-200">The text is highlighted to indicate that the node is selected.</span></span>  
    
    > ##### <span data-ttu-id="519a7-201">Figura 9</span><span class="sxs-lookup"><span data-stu-id="519a7-201">Figure 9</span></span>  
    > <span data-ttu-id="519a7-202">Editando o nó</span><span class="sxs-lookup"><span data-stu-id="519a7-202">Editing the node</span></span>  
    > ![Editando o nó][ImageEditingNode]  
    
1.  <span data-ttu-id="519a7-204">Pressione a `Right` tecla de seta, adicione um espaço, digite `style="background-color:gold"` e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="519a7-204">Press the `Right` arrow key, add a space, type `style="background-color:gold"`, and then press `Enter`.</span></span>  <span data-ttu-id="519a7-205">A cor da tela de fundo do nó muda para ouro.</span><span class="sxs-lookup"><span data-stu-id="519a7-205">The background color of the node changes to gold.</span></span>  
    
    > ##### <span data-ttu-id="519a7-206">Figura 10</span><span class="sxs-lookup"><span data-stu-id="519a7-206">Figure 10</span></span>  
    > <span data-ttu-id="519a7-207">Adicionando um atributo Style ao nó</span><span class="sxs-lookup"><span data-stu-id="519a7-207">Adding a style attribute to the node</span></span>  
    > ![Adicionando um atributo Style ao nó][ImageAddingStyleAttributeNode]  
    
### <span data-ttu-id="519a7-209">Editar tipo de nó</span><span class="sxs-lookup"><span data-stu-id="519a7-209">Edit node type</span></span>   

<span data-ttu-id="519a7-210">Para editar o tipo de um nó, clique duas vezes no tipo e, em seguida, digite o novo tipo.</span><span class="sxs-lookup"><span data-stu-id="519a7-210">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="519a7-211">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="519a7-211">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="519a7-212">Em **Editar tipo de nó**, clique com o botão direito do mouse em **Hank** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-212">Under **Edit Node Type**, right-click **Hank** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="519a7-213">Clique duas vezes `<li>` .</span><span class="sxs-lookup"><span data-stu-id="519a7-213">Double-click `<li>`.</span></span>  <span data-ttu-id="519a7-214">O texto `li` é realçado.</span><span class="sxs-lookup"><span data-stu-id="519a7-214">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="519a7-215">Excluir `li` , digite `button` e, em seguida, pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="519a7-215">Delete `li`, type `button`, then press `Enter`.</span></span>  <span data-ttu-id="519a7-216">O `<li>` nó muda para um `<button>` nó.</span><span class="sxs-lookup"><span data-stu-id="519a7-216">The `<li>` node changes to a `<button>` node.</span></span>  
        
        > ##### <span data-ttu-id="519a7-217">Figura 11</span><span class="sxs-lookup"><span data-stu-id="519a7-217">Figure 11</span></span>  
        > <span data-ttu-id="519a7-218">Alterar o botão do tipo de nó</span><span class="sxs-lookup"><span data-stu-id="519a7-218">Changing the node type to button</span></span>  
        > ![Alterar o botão do tipo de nó][ImageChangingNodeButton]  
        
### <span data-ttu-id="519a7-220">Reordenar nós DOM</span><span class="sxs-lookup"><span data-stu-id="519a7-220">Reorder DOM nodes</span></span>   

<span data-ttu-id="519a7-221">Arraste os nós para reorganizá-los.</span><span class="sxs-lookup"><span data-stu-id="519a7-221">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="519a7-222">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="519a7-222">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="519a7-223">Em **Reordenar nós dom**, clique com o botão direito do mouse em **Elvis Presley** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-223">Under **Reorder DOM Nodes**, right-click **Elvis Presley** and select **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="519a7-224">É o último item na lista.</span><span class="sxs-lookup"><span data-stu-id="519a7-224">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="519a7-225">Na árvore DOM, arraste `<li>Elvis Presley</li>` para a parte superior da lista.</span><span class="sxs-lookup"><span data-stu-id="519a7-225">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        > ##### <span data-ttu-id="519a7-226">Figura 12</span><span class="sxs-lookup"><span data-stu-id="519a7-226">Figure 12</span></span>  
        > <span data-ttu-id="519a7-227">Arrastando o nó para a parte superior da lista</span><span class="sxs-lookup"><span data-stu-id="519a7-227">Dragging the node to the top of the list</span></span>  
        > ![Arrastando o nó para a parte superior da lista][ImageDraggingNodeTopList]  
        
### <span data-ttu-id="519a7-229">Forçar estado</span><span class="sxs-lookup"><span data-stu-id="519a7-229">Force state</span></span>   

<span data-ttu-id="519a7-230">Você pode forçar os nós a permanecer nos Estados, incluindo `:active` ,,, `:hover` `:focus` `:visited` e `:focus-within` .</span><span class="sxs-lookup"><span data-stu-id="519a7-230">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="519a7-231">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="519a7-231">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="519a7-232">Em **forçar estado**, passe o mouse sobre **o Lord dos voa**.</span><span class="sxs-lookup"><span data-stu-id="519a7-232">Under **Force state**, hover over **The Lord of the Flies**.</span></span>  <span data-ttu-id="519a7-233">A cor do plano de fundo se torna laranja.</span><span class="sxs-lookup"><span data-stu-id="519a7-233">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="519a7-234">Clique com o botão direito do mouse **no Lord dos voas** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-234">Right-click **The Lord of the Flies** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="519a7-235">Clique com o botão direito do mouse `<li class="demo--hover">The Lord of the Flies</li>` e selecione **forçar estado**  >  **: focalizar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-235">Right-click `<li class="demo--hover">The Lord of the Flies</li>` and select **Force State** > **:hover**.</span></span>  <span data-ttu-id="519a7-236">Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não vir essa opção.</span><span class="sxs-lookup"><span data-stu-id="519a7-236">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  <span data-ttu-id="519a7-237">A cor do plano de fundo permanece laranja, mesmo que você não esteja efetivamente passando o mouse sobre o nó.</span><span class="sxs-lookup"><span data-stu-id="519a7-237">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <span data-ttu-id="519a7-238">Ocultar um nó</span><span class="sxs-lookup"><span data-stu-id="519a7-238">Hide a node</span></span>   

<span data-ttu-id="519a7-239">Pressione `H` para ocultar um nó.</span><span class="sxs-lookup"><span data-stu-id="519a7-239">Press `H` to hide a node.</span></span>  

1.  <span data-ttu-id="519a7-240">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="519a7-240">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="519a7-241">Em **ocultar um nó**, clique com o botão direito **do mouse no meu destino de estrelas** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-241">Under **Hide a node**, right-click **The Stars My Destination** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="519a7-242">Pressione a `H` tecla.</span><span class="sxs-lookup"><span data-stu-id="519a7-242">Press the `H` key.</span></span>  <span data-ttu-id="519a7-243">O nó está oculto.</span><span class="sxs-lookup"><span data-stu-id="519a7-243">The node is hidden.</span></span>  
        
        > ##### <span data-ttu-id="519a7-244">Figura 13</span><span class="sxs-lookup"><span data-stu-id="519a7-244">Figure 13</span></span>  
        > <span data-ttu-id="519a7-245">Qual é a aparência do nó na árvore DOM após ele estar oculto</span><span class="sxs-lookup"><span data-stu-id="519a7-245">What the node looks like in the DOM Tree after it is hidden</span></span>  
        > ![Qual é a aparência do nó na árvore DOM após ele estar oculto][ImageNodeDomTreeAfterHidden]  
        
    1.  <span data-ttu-id="519a7-247">Pressione a `H` tecla novamente.</span><span class="sxs-lookup"><span data-stu-id="519a7-247">Press the `H` key again.</span></span>  <span data-ttu-id="519a7-248">O nó é mostrado novamente.</span><span class="sxs-lookup"><span data-stu-id="519a7-248">The node is shown again.</span></span>  

### <span data-ttu-id="519a7-249">Excluir um nó</span><span class="sxs-lookup"><span data-stu-id="519a7-249">Delete a node</span></span>   

<span data-ttu-id="519a7-250">Pressione `Delete` para excluir um nó.</span><span class="sxs-lookup"><span data-stu-id="519a7-250">Press `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="519a7-251">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="519a7-251">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="519a7-252">Em **excluir um nó**, clique com o botão direito do mouse em **base** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-252">Under **Delete a Node**, right-click **Foundation** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="519a7-253">Pressione a `Delete` tecla.</span><span class="sxs-lookup"><span data-stu-id="519a7-253">Press the `Delete` key.</span></span>  <span data-ttu-id="519a7-254">O nó é excluído.</span><span class="sxs-lookup"><span data-stu-id="519a7-254">The node is deleted.</span></span>  
    1.  <span data-ttu-id="519a7-255">Pressione `Control` + `Z` \ (Windows \) ou `Command` + `Z` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="519a7-255">Press `Control`+`Z` \(Windows\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="519a7-256">A última ação é desfeita e o nó é exibido novamente.</span><span class="sxs-lookup"><span data-stu-id="519a7-256">The last action is undone and the node reappears.</span></span>  

## <span data-ttu-id="519a7-257">Acessar nós no console</span><span class="sxs-lookup"><span data-stu-id="519a7-257">Access nodes in the Console</span></span>   

<span data-ttu-id="519a7-258">O DevTools fornece alguns atalhos para acessar nós DOM do console ou obter referências de JavaScript a cada um.</span><span class="sxs-lookup"><span data-stu-id="519a7-258">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <span data-ttu-id="519a7-259">Fazer referência ao nó atualmente selecionado com o $0</span><span class="sxs-lookup"><span data-stu-id="519a7-259">Reference the currently-selected node with $0</span></span>   

<span data-ttu-id="519a7-260">Quando você inspeciona um nó, o `== $0` texto ao lado do nó significa que você pode fazer referência a esse nó no console com a variável `$0` .</span><span class="sxs-lookup"><span data-stu-id="519a7-260">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="519a7-261">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="519a7-261">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="519a7-262">Em **referenciar o nó selecionado no momento com o $0**, clique com o botão direito do mouse **na mão esquerda da escuridão** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-262">Under **Reference the currently-selected node with $0**, right-click **The Left Hand of Darkness** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="519a7-263">Pressione a `Escape` tecla para abrir a gaveta do console.</span><span class="sxs-lookup"><span data-stu-id="519a7-263">Press the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="519a7-264">Digite `$0` e pressione a `Enter` tecla.</span><span class="sxs-lookup"><span data-stu-id="519a7-264">Type `$0` and press the `Enter` key.</span></span>  <span data-ttu-id="519a7-265">O resultado da expressão mostra que `$0` é avaliado como `<li>The Left Hand of Darkness</li>` .</span><span class="sxs-lookup"><span data-stu-id="519a7-265">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        > ##### <span data-ttu-id="519a7-266">Figura 14</span><span class="sxs-lookup"><span data-stu-id="519a7-266">Figure 14</span></span>  
        > <span data-ttu-id="519a7-267">O resultado da primeira `$0` expressão no console</span><span class="sxs-lookup"><span data-stu-id="519a7-267">The result of the first `$0` expression in the Console</span></span>  
        > ![O resultado da primeira expressão $0 no console][ImageFirstConsole]  
        
    1.  <span data-ttu-id="519a7-269">Passe o mouse sobre o resultado.</span><span class="sxs-lookup"><span data-stu-id="519a7-269">Hover over the result.</span></span>  <span data-ttu-id="519a7-270">O nó é realçado no visor.</span><span class="sxs-lookup"><span data-stu-id="519a7-270">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="519a7-271">Clique `<li>Dune</li>` na árvore DOM, digite `$0` novamente no console e pressione `Enter` novamente.</span><span class="sxs-lookup"><span data-stu-id="519a7-271">Click `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then press `Enter` again.</span></span>  <span data-ttu-id="519a7-272">Agora, `$0` é avaliada como `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="519a7-272">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        > ##### <span data-ttu-id="519a7-273">Figura 15</span><span class="sxs-lookup"><span data-stu-id="519a7-273">Figure 15</span></span>  
        > <span data-ttu-id="519a7-274">O resultado da segunda `$0` expressão no console ![ o resultado da segunda expressão $0 no console][ImageSecondConsole]</span><span class="sxs-lookup"><span data-stu-id="519a7-274">The result of the second `$0` expression in the Console ![The result of the second $0 expression in the Console][ImageSecondConsole]</span></span>  
        
### <span data-ttu-id="519a7-275">Armazenar como variável global</span><span class="sxs-lookup"><span data-stu-id="519a7-275">Store as global variable</span></span>   

<span data-ttu-id="519a7-276">Se você precisar consultar novamente um nó muitas vezes, armazene-o como uma variável global.</span><span class="sxs-lookup"><span data-stu-id="519a7-276">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="519a7-277">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="519a7-277">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="519a7-278">Em **armazenar como variável global**, clique com o botão direito **do mouse na grande suspensão** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-278">Under **Store as global variable**, right-click **The Big Sleep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="519a7-279">Clique com o botão direito do mouse `<li>The Big Sleep</li>` na árvore DOM e selecione **armazenar como variável global**.</span><span class="sxs-lookup"><span data-stu-id="519a7-279">Right-click `<li>The Big Sleep</li>` in the DOM Tree and select **Store as global variable**.</span></span>  <span data-ttu-id="519a7-280">Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não vir essa opção.</span><span class="sxs-lookup"><span data-stu-id="519a7-280">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  
    1.  <span data-ttu-id="519a7-281">Digite `temp1` o console e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="519a7-281">Type `temp1` in the Console and then press `Enter`.</span></span>  <span data-ttu-id="519a7-282">O resultado da expressão mostra que a variável é avaliada como o nó.</span><span class="sxs-lookup"><span data-stu-id="519a7-282">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        > ##### <span data-ttu-id="519a7-283">Figura 16</span><span class="sxs-lookup"><span data-stu-id="519a7-283">Figure 16</span></span>  
        > <span data-ttu-id="519a7-284">O resultado da expressão temp1</span><span class="sxs-lookup"><span data-stu-id="519a7-284">The result of the temp1 expression</span></span>  
        > ![O resultado da expressão temp1][ImageResultTemp1]  
        
### <span data-ttu-id="519a7-286">Copiar caminho do JS</span><span class="sxs-lookup"><span data-stu-id="519a7-286">Copy JS path</span></span>   

<span data-ttu-id="519a7-287">Copie o caminho JavaScript para um nó quando precisar referenciá-lo em um teste automatizado.</span><span class="sxs-lookup"><span data-stu-id="519a7-287">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="519a7-288">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="519a7-288">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="519a7-289">Em **copiar o caminho do js**, clique com o botão direito **do mouse na Karamazov da Brothers** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-289">Under **Copy JS path**, right-click **The Brothers Karamazov** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="519a7-290">Clique com o botão direito do mouse `<li>The Brothers Karamazov</li>` na árvore DOM e selecione **copiar**o  >  **caminho do js**.</span><span class="sxs-lookup"><span data-stu-id="519a7-290">Right-click `<li>The Brothers Karamazov</li>` in the DOM Tree and select **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="519a7-291">Uma `document.querySelector()` expressão que é resolvida para o nó foi copiada para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="519a7-291">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="519a7-292">Pressione `Control` + `V` \ (Windows \) ou `Command` + `V` \ (MacOS \) para colar a expressão no console.</span><span class="sxs-lookup"><span data-stu-id="519a7-292">Press `Control`+`V` \(Windows\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="519a7-293">Pressione `Enter` para avaliar a expressão.</span><span class="sxs-lookup"><span data-stu-id="519a7-293">Press `Enter` to evaluate the expression.</span></span>
        
        > ##### <span data-ttu-id="519a7-294">Figura 17</span><span class="sxs-lookup"><span data-stu-id="519a7-294">Figure 17</span></span>  
        > <span data-ttu-id="519a7-295">O resultado da expressão de caminho do JS de cópia</span><span class="sxs-lookup"><span data-stu-id="519a7-295">The result of the Copy JS Path expression</span></span>  
        > ![O resultado da expressão de caminho do JS de cópia][ImageResultCopyJSPath]  
        
## <span data-ttu-id="519a7-297">Interromper alterações de DOM</span><span class="sxs-lookup"><span data-stu-id="519a7-297">Break on DOM changes</span></span>   

<span data-ttu-id="519a7-298">O DevTools permite pausar o JavaScript de uma página quando o JavaScript modifica o DOM.</span><span class="sxs-lookup"><span data-stu-id="519a7-298">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <span data-ttu-id="519a7-299">Interromper alterações de atributo</span><span class="sxs-lookup"><span data-stu-id="519a7-299">Break on attribute modifications</span></span>   

<span data-ttu-id="519a7-300">Use pontos de interrupção de modificação de atributo quando você quiser pausar o JavaScript que faz com que qualquer atributo de um nó seja alterado.</span><span class="sxs-lookup"><span data-stu-id="519a7-300">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="519a7-301">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="519a7-301">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="519a7-302">Em **interromper as modificações de atributo**, clique com o botão direito do mouse em **sauerkraut** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-302">Under **Break on attribute modifications**, right-click **Sauerkraut** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="519a7-303">Na árvore DOM, clique com o botão direito do mouse `<li id="target">Sauerkraut</li>` e selecione **interromper nas**  >  **modificações de atributo**.</span><span class="sxs-lookup"><span data-stu-id="519a7-303">In the DOM Tree, right-click `<li id="target">Sauerkraut</li>` and select **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="519a7-304">Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não conseguir ver esta opção.</span><span class="sxs-lookup"><span data-stu-id="519a7-304">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>
        
        > ##### <span data-ttu-id="519a7-305">Figura 18</span><span class="sxs-lookup"><span data-stu-id="519a7-305">Figure 18</span></span>  
        > <span data-ttu-id="519a7-306">Interromper alterações de atributo</span><span class="sxs-lookup"><span data-stu-id="519a7-306">Break on attribute modifications</span></span>  
        > ![Interromper alterações de atributo][ImageBreakAttributeModification]  
        
    1.  <span data-ttu-id="519a7-308">Na próxima etapa, você será instruído a clicar em um botão que Pause o código da página.</span><span class="sxs-lookup"><span data-stu-id="519a7-308">In the next step you are going to be instructed to click a button that pauses the code of the page.</span></span>  <span data-ttu-id="519a7-309">Depois que a página for pausada, você não poderá mais rolar a página.</span><span class="sxs-lookup"><span data-stu-id="519a7-309">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="519a7-310">Você deve clicar em **retomar** ![ script retomar script ][ImageResumeScriptIcon] para fazer com que a página seja rolável novamente.</span><span class="sxs-lookup"><span data-stu-id="519a7-310">You must click **Resume Script** ![Resume Script][ImageResumeScriptIcon] in order to make the page scrollable again.</span></span>
        
        > ##### <span data-ttu-id="519a7-311">Figura 19</span><span class="sxs-lookup"><span data-stu-id="519a7-311">Figure 19</span></span>  
        > <span data-ttu-id="519a7-312">Onde continuar a execução do script</span><span class="sxs-lookup"><span data-stu-id="519a7-312">Where to resume script running</span></span>  
        > ![Onde continuar a execução do script][ImageResumeScript]  
        
    1.  <span data-ttu-id="519a7-314">Clique no botão **definir plano de fundo** acima.</span><span class="sxs-lookup"><span data-stu-id="519a7-314">Click the **Set Background** button above.</span></span>  <span data-ttu-id="519a7-315">Isso define o `style` atributo do nó para `background-color:thistle` .</span><span class="sxs-lookup"><span data-stu-id="519a7-315">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="519a7-316">DevTools pausará a página e realçará o código que fez com que o atributo fosse alterado.</span><span class="sxs-lookup"><span data-stu-id="519a7-316">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="519a7-317">Clique em **retomar** ![ script da retomada de script ][ImageResumeScriptIcon] , conforme mencionado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="519a7-317">Click **Resume Script** ![Resume Script][ImageResumeScriptIcon], as mentioned earlier.</span></span>  
    
### <span data-ttu-id="519a7-318">Interromper a remoção do nó</span><span class="sxs-lookup"><span data-stu-id="519a7-318">Break on node removal</span></span>   

<span data-ttu-id="519a7-319">Se você quiser pausar quando um nó específico for removido, use pontos de interrupção de remoção de nó.</span><span class="sxs-lookup"><span data-stu-id="519a7-319">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="519a7-320">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="519a7-320">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="519a7-321">Em **interromper a remoção do nó**, clique com o botão direito do mouse em **Neuromancer** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-321">Under **Break on Node Removal**, right-click **Neuromancer** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="519a7-322">Na árvore DOM, clique com o botão direito do mouse `<li id="target">Neuromancer</li>` e selecione **interromper na**  >  **remoção do nó**.</span><span class="sxs-lookup"><span data-stu-id="519a7-322">In the DOM Tree, right-click `<li id="target">Neuromancer</li>` and select **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="519a7-323">Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não conseguir ver esta opção.</span><span class="sxs-lookup"><span data-stu-id="519a7-323">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="519a7-324">Clique no botão **excluir** acima.</span><span class="sxs-lookup"><span data-stu-id="519a7-324">Click the **Delete** button above.</span></span>  <span data-ttu-id="519a7-325">DevTools pausará a página e realçará o código que fez com que o nó fosse removido.</span><span class="sxs-lookup"><span data-stu-id="519a7-325">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="519a7-326">Clique em **retomar** ![ script da retomada de script ][ImageResumeScriptIcon] .</span><span class="sxs-lookup"><span data-stu-id="519a7-326">Click **Resume Script** ![Resume Script][ImageResumeScriptIcon].</span></span>  
    
### <span data-ttu-id="519a7-327">Interromper modificações de subárvore</span><span class="sxs-lookup"><span data-stu-id="519a7-327">Break on subtree modifications</span></span>   

<span data-ttu-id="519a7-328">Depois que você colocar um ponto de interrupção de modificação de subárvore em um nó, o DevTools pausará a página quando qualquer um dos descendentes do nó for adicionado ou removido.</span><span class="sxs-lookup"><span data-stu-id="519a7-328">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="519a7-329">[Exemplos abertos do dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="519a7-329">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="519a7-330">Em **interromper modificações de subárvore**, clique com o botão direito do mouse em **um incêndio na profundidade** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="519a7-330">Under **Break on Subtree Modifications**, right-click **A Fire Upon The Deep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="519a7-331">Na árvore DOM, clique com o botão direito do mouse `<ul id="target">` , que é o nó acima `<li>A Fire Upon the Deep</li>` e selecione **interromper**  >  **alterações de subárvore**.</span><span class="sxs-lookup"><span data-stu-id="519a7-331">In the DOM Tree, right-click `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, and select **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="519a7-332">Consulte [Apêndice: opções ausentes](#appendix-missing-options) se você não conseguir ver esta opção.</span><span class="sxs-lookup"><span data-stu-id="519a7-332">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="519a7-333">Clique em **Adicionar filho**.</span><span class="sxs-lookup"><span data-stu-id="519a7-333">Click **Add Child**.</span></span>  <span data-ttu-id="519a7-334">O código é pausado porque um `<li>` nó foi adicionado à lista.</span><span class="sxs-lookup"><span data-stu-id="519a7-334">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="519a7-335">Clique em **retomar** ![ script da retomada de script ][ImageResumeScriptIcon] .</span><span class="sxs-lookup"><span data-stu-id="519a7-335">Click **Resume Script** ![Resume Script][ImageResumeScriptIcon].</span></span>  
    
## <span data-ttu-id="519a7-336">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="519a7-336">Next steps</span></span>   

<span data-ttu-id="519a7-337">Isso abrange a maioria dos recursos relacionados ao DOM no DevTools.</span><span class="sxs-lookup"><span data-stu-id="519a7-337">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="519a7-338">Você pode descobrir o restante deles clicando com o botão direito do mouse nos nós na árvore DOM e experimentando as outras opções que não foram abordadas neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="519a7-338">You are able to discover the rest of them by right-clicking nodes in the DOM Tree and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="519a7-339">Consulte também [atalhos de teclado do painel elementos][DevToolsShortcutsElements].</span><span class="sxs-lookup"><span data-stu-id="519a7-339">See also [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="519a7-340">Confira a [Home Page do Microsoft Edge devtools][MicrosoftEdgeDevTools] para descobrir tudo o que você pode fazer com o devtools.</span><span class="sxs-lookup"><span data-stu-id="519a7-340">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--See [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  



## <span data-ttu-id="519a7-341">Apêndice: HTML versus DOM</span><span class="sxs-lookup"><span data-stu-id="519a7-341">Appendix: HTML versus the DOM</span></span>   

<span data-ttu-id="519a7-342">Esta seção explica rapidamente a diferença entre HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="519a7-342">This section quickly explains the difference between HTML and the DOM.</span></span>  

<span data-ttu-id="519a7-343">Quando você usa um navegador da Web para solicitar uma página, o servidor retorna HTML da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="519a7-343">When you use a web browser to request a page, the server returns HTML like this:</span></span>  

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

<span data-ttu-id="519a7-344">O navegador analisa o HTML e cria uma árvore de objetos como esta:</span><span class="sxs-lookup"><span data-stu-id="519a7-344">The browser parses the HTML and creates a tree of objects like this:</span></span>  

```dom
html
  head
    title
  body
    h1
    p
    script
```  

<span data-ttu-id="519a7-345">Essa árvore de objetos, ou nós, que representa o conteúdo da página é chamada de DOM.</span><span class="sxs-lookup"><span data-stu-id="519a7-345">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  <span data-ttu-id="519a7-346">No momento, ele tem a mesma aparência do HTML, mas suponha que o script referenciado na parte inferior do HTML executa este código:</span><span class="sxs-lookup"><span data-stu-id="519a7-346">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs this code:</span></span>  

```javascript
const h1 = document.querySelector('h1');
h1.parentElement.removeChild(h1);
const p = document.createElement('p');
p.textContent = 'Wildcard!';
document.body.appendChild(p);
```  

<span data-ttu-id="519a7-347">Esse código remove o `h1` nó e adiciona outro `p` nó ao dom.</span><span class="sxs-lookup"><span data-stu-id="519a7-347">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="519a7-348">Agora, o DOM completo tem a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="519a7-348">The complete DOM now looks like this:</span></span>  

```dom
html
  head
    title
  body
    p
    script
    p
```  

<span data-ttu-id="519a7-349">O HTML da página agora é diferente do DOM.</span><span class="sxs-lookup"><span data-stu-id="519a7-349">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="519a7-350">Em outras palavras, HTML representa o conteúdo inicial da página, e o DOM representa o conteúdo da página atual.</span><span class="sxs-lookup"><span data-stu-id="519a7-350">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="519a7-351">Quando o JavaScript adiciona, remove ou edita nós, o DOM se torna diferente do HTML.</span><span class="sxs-lookup"><span data-stu-id="519a7-351">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="519a7-352">Consulte [introdução ao dom][MDNIntroductionToDOM] para saber mais.</span><span class="sxs-lookup"><span data-stu-id="519a7-352">See [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view   

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and select **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    > ##### Figure 19  
    > Scroll into view  
    > ![Scroll into view][ImageScrollView]  
    -->  

## <span data-ttu-id="519a7-353">Apêndice: opções ausentes</span><span class="sxs-lookup"><span data-stu-id="519a7-353">Appendix: Missing options</span></span>   

<span data-ttu-id="519a7-354">Muitas das instruções neste tutorial instruem você a clicar com o botão direito do mouse em um nó na árvore DOM e selecionar uma opção no menu de contexto exibido.</span><span class="sxs-lookup"><span data-stu-id="519a7-354">Many of the instructions in this tutorial instruct you to right-click a node in the DOM Tree and then select an option from the context menu that pops up.</span></span>  <span data-ttu-id="519a7-355">Se você não vir a opção especificado no menu de contexto, tente clicar com o botão direito do mouse sobre o texto do nó.</span><span class="sxs-lookup"><span data-stu-id="519a7-355">If you do not see the specified option in the context menu, try right-clicking away from the node text.</span></span>  

> ##### <span data-ttu-id="519a7-356">Figura 20</span><span class="sxs-lookup"><span data-stu-id="519a7-356">Figure 20</span></span>  
> <span data-ttu-id="519a7-357">Onde clicar se você não estiver vendo todas as opções</span><span class="sxs-lookup"><span data-stu-id="519a7-357">Where to click if you are not seeing all the options</span></span>  
> ![Onde clicar se você não estiver vendo todas as opções][ImageNotSeeingAllOptions]  

<!-- image links -->  

[ImageInspectIcon]: /microsoft-edge/devtools-guide-chromium/media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-icon.msft.png  

[ImageInspectingNode]: /microsoft-edge/devtools-guide-chromium/media/dom-glitch-dom-examples-michelangelo-inspect.msft.png "Figura 1: inspecionando um nó"  
[ImageHighlightingMichelangeloNode]: /microsoft-edge/devtools-guide-chromium/media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png "Figura 2: realçando o nó Michelangelo"  
[ImageInspect]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-select-element-page-inspect.msft.png "Figura 3: o ícone inspecionar"  
[ImageInspectingRingoNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png "Figura 4: inspeção do nó Ringo"  
[ImageInspectingUlNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png "Figura 5: inspeção do nó UL"  
[ImageScrollView]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png "Figura 6: rolar para o modo de exibição"  
[ImageHighlightingQuerySearchBar]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-search-nodes-highlight.msft.png "Figura 7: realçando a consulta na barra de pesquisa"  
[ImageEditingText]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-content.msft.png "Figura 8: editando o texto"  
[ImageEditingNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-attributes-highlighted.msft.png "Figura 9: editando o nó"  
[ImageAddingStyleAttributeNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-attributes-inline-css.msft.png "Figura 10: adicionando um atributo Style ao nó"  
[ImageChangingNodeButton]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-node-type-button.msft.png "Figura 11: alterando o tipo de nó para o botão"  
[ImageDraggingNodeTopList]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-reorder-dom-nodes.msft.png "Figura 12: arrastando o nó para a parte superior da lista"  
[ImageNodeDomTreeAfterHidden]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-hide-a-node.msft.png "Figura 13: Qual é a aparência do nó na árvore DOM após ele estar oculto"  
[ImageFirstConsole]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png "Figura 14: o resultado da primeira expressão $0 no console"  
[ImageSecondConsole]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png "Figura 15: o resultado da segunda expressão do $0 no console"  
[ImageResultTemp1]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png "Figura 16: o resultado da expressão temp1"  
[ImageResultCopyJSPath]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png "Figura 17: o resultado da expressão de caminho do JS de cópia"  
[ImageBreakAttributeModification]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png "Figura 18: pausa nas modificações do atributo"  
[ImageResumeScript]: /microsoft-edge/devtools-guide-chromium/media/dom-break-attribute-modifications-sources-paused-on.msft.png "Figura 19: onde retomar o script em execução"  
[ImageNotSeeingAllOptions]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-right-click-right-side.msft.png "Figura 20: onde clicar se você não estiver vendo todas as opções"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge \ (Chromium \)"  
[DevToolsCssGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Introdução à exibição e alteração de CSS"  
[DevToolsShortcutsElements]: /microsoft-edge/devtools-guide-chromium/shortcuts#elements-panel-keyboard-shortcuts "Atalhos de teclado do painel elementos-atalhos de teclado do Microsoft Edge DevTools"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Exemplo de DOM do Microsoft Edge (Chromium) DevTools | Problema"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introdução ao DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="519a7-384">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="519a7-384">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="519a7-385">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/dom/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="519a7-385">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="519a7-387">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="519a7-387">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
