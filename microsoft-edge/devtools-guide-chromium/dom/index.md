---
description: Como exibir nós, pesquisar nós, editar nós, fazer referência a nós no Console, pausar alterações no nó e muito mais.
title: Começar a exibir e alterar o DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: e4c08fb2fd5f360f037502c04edabaabb873ba16
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439237"
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

# <a name="get-started-with-viewing-and-changing-the-dom"></a><span data-ttu-id="9a468-104">Começar a exibir e alterar o DOM</span><span class="sxs-lookup"><span data-stu-id="9a468-104">Get started with viewing and changing the DOM</span></span>  

<span data-ttu-id="9a468-105">Conclua estes tutoriais interativos para aprender os conceitos básicos de exibição e alteração do DOM de uma página usando o Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="9a468-105">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="9a468-106">Este tutorial supõe que você sabe a diferença entre DOM e HTML.</span><span class="sxs-lookup"><span data-stu-id="9a468-106">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="9a468-107">Navegue [até Apêndice: HTML versus DOM](#appendix-html-versus-the-dom) para uma explicação.</span><span class="sxs-lookup"><span data-stu-id="9a468-107">Navigate to [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <a name="open-dom-examples"></a><span data-ttu-id="9a468-108">Abrir exemplos dom</span><span class="sxs-lookup"><span data-stu-id="9a468-108">Open DOM examples</span></span>  

1.  <span data-ttu-id="9a468-109">Segure `Control` \(Windows, Linux\) ou `Command` \(macOS\) e escolha **Exemplos dom** para abrir em uma nova guia.</span><span class="sxs-lookup"><span data-stu-id="9a468-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="9a468-110">Exemplos dom</span><span class="sxs-lookup"><span data-stu-id="9a468-110">DOM Examples</span></span>][GlitchDomExamples]  
    
## <a name="view-dom-nodes"></a><span data-ttu-id="9a468-111">Exibir nós DOM</span><span class="sxs-lookup"><span data-stu-id="9a468-111">View DOM nodes</span></span>  

<span data-ttu-id="9a468-112">A Árvore DOM do painel Elementos é onde você faz todas as atividades relacionadas ao DOM no DevTools.</span><span class="sxs-lookup"><span data-stu-id="9a468-112">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <a name="inspect-a-node"></a><span data-ttu-id="9a468-113">Inspecionar um nó</span><span class="sxs-lookup"><span data-stu-id="9a468-113">Inspect a node</span></span>  

<span data-ttu-id="9a468-114">Quando você estiver interessado em um nó DOM específico, **Inspecionar** é uma maneira rápida de abrir o DevTools e investigar esse nó.</span><span class="sxs-lookup"><span data-stu-id="9a468-114">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="9a468-115">[Abra exemplos dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="9a468-115">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9a468-116">Em **Inspecionar um Nó,** escolha Com a direita **o Próprio Ângelo** e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="9a468-116">Under **Inspect a Node**, right-choose **Michelangelo** and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Inspecionar um nó" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       <span data-ttu-id="9a468-118">Inspecionar um nó</span><span class="sxs-lookup"><span data-stu-id="9a468-118">Inspect a node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="9a468-119">A **ferramenta Elements** do DevTools é aberta.</span><span class="sxs-lookup"><span data-stu-id="9a468-119">The **Elements** tool of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="9a468-120">é realçada na árvore **DOM**.</span><span class="sxs-lookup"><span data-stu-id="9a468-120">is highlighted in the **DOM Tree**.</span></span>  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Realça o nó Delângelo" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           <span data-ttu-id="9a468-122">Realça o `Michelangelo` nó</span><span class="sxs-lookup"><span data-stu-id="9a468-122">Highlight the `Michelangelo` node</span></span>  
        :::image-end:::  
        
        1.  <span data-ttu-id="9a468-123">Escolha o **ícone Inspecionar** \( ![ Inspecionar ](../media/inspect-icon.msft.png) \) no canto superior esquerdo do DevTools.</span><span class="sxs-lookup"><span data-stu-id="9a468-123">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="O ícone Inspecionar" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               <span data-ttu-id="9a468-125">O **ícone Inspecionar**</span><span class="sxs-lookup"><span data-stu-id="9a468-125">The **Inspect** icon</span></span>  
            :::image-end:::  
            
1.  <span data-ttu-id="9a468-126">Em **Inspecionar um Nó,** escolha o **texto de** Tokyo.</span><span class="sxs-lookup"><span data-stu-id="9a468-126">Under **Inspect a Node**, choose the **Tokyo** text.</span></span>  <span data-ttu-id="9a468-127">Agora, `<li>Tokyo</li>` é realçado na árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="9a468-127">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="9a468-128">Inspecionar um nó também é a primeira etapa para exibir e alterar os estilos de um nó.</span><span class="sxs-lookup"><span data-stu-id="9a468-128">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="9a468-129">Navegue [até Começar a exibir e alterar CSS][DevToolsCssGetStarted].</span><span class="sxs-lookup"><span data-stu-id="9a468-129">Navigate to [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <a name="navigate-the-dom-tree-with-a-keyboard"></a><span data-ttu-id="9a468-130">Navegue pela Árvore DOM com um teclado</span><span class="sxs-lookup"><span data-stu-id="9a468-130">Navigate the DOM Tree with a keyboard</span></span>  

<span data-ttu-id="9a468-131">Depois de selecionar um nó na Árvore DOM, você poderá navegar na Árvore DOM com o teclado.</span><span class="sxs-lookup"><span data-stu-id="9a468-131">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="9a468-132">[Abra exemplos dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="9a468-132">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9a468-133">Em **Navegar na Árvore DOM com um Teclado,** escolha **Ringo** com a direita e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="9a468-133">Under **Navigate the DOM Tree with a Keyboard**, right-choose **Ringo** and choose **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="9a468-134">está selecionado na Árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="9a468-134">is selected in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Inspecionar o nó Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       <span data-ttu-id="9a468-136">Inspecionar o `Ringo` nó</span><span class="sxs-lookup"><span data-stu-id="9a468-136">Inspect the `Ringo` node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="9a468-137">Selecione a `Up` tecla de seta duas vezes.</span><span class="sxs-lookup"><span data-stu-id="9a468-137">Select the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="9a468-138"> está selecionada.</span><span class="sxs-lookup"><span data-stu-id="9a468-138">is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Inspecionar o nó ul" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           <span data-ttu-id="9a468-140">Inspecionar o `ul` nó</span><span class="sxs-lookup"><span data-stu-id="9a468-140">Inspect the `ul` node</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="9a468-141">Selecione a `Left` tecla de seta.</span><span class="sxs-lookup"><span data-stu-id="9a468-141">Select the `Left` arrow key.</span></span>  <span data-ttu-id="9a468-142">A `<ul>` lista colapsa.</span><span class="sxs-lookup"><span data-stu-id="9a468-142">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="9a468-143">Selecione a `Left` tecla de seta novamente.</span><span class="sxs-lookup"><span data-stu-id="9a468-143">Select the `Left` arrow key again.</span></span>  <span data-ttu-id="9a468-144">O pai do `<ul>` nó está selecionado.</span><span class="sxs-lookup"><span data-stu-id="9a468-144">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="9a468-145">Nesse caso, é o `<div>` com a ID `navigate-the-dom-tree-with-a-keyboard-1` .</span><span class="sxs-lookup"><span data-stu-id="9a468-145">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="9a468-146">Selecione a tecla de seta 2 vezes para que você tenha selecionado a `Down` lista que você acabou de `<ul>` recolhido.</span><span class="sxs-lookup"><span data-stu-id="9a468-146">Select the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="9a468-147">Ele deve ser assim:</span><span class="sxs-lookup"><span data-stu-id="9a468-147">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="9a468-148">Selecione a `Right` tecla de seta.</span><span class="sxs-lookup"><span data-stu-id="9a468-148">Select the `Right` arrow key.</span></span>  <span data-ttu-id="9a468-149">A lista se expande.</span><span class="sxs-lookup"><span data-stu-id="9a468-149">The list expands.</span></span>  

### <a name="scroll-into-view"></a><span data-ttu-id="9a468-150">Rolar para a exibição</span><span class="sxs-lookup"><span data-stu-id="9a468-150">Scroll into view</span></span>  

<span data-ttu-id="9a468-151">Ao exibir a Árvore DOM, você pode se interessar por um nó DOM que não esteja no viewport no momento.</span><span class="sxs-lookup"><span data-stu-id="9a468-151">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="9a468-152">Por exemplo, suponha que você tenha rolado até a parte inferior da página e esteja interessado no nó na `<h1>` parte superior da página.</span><span class="sxs-lookup"><span data-stu-id="9a468-152">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="9a468-153">**Rolar para o modo** de exibição permite que você reposicionar rapidamente o modo de exibição para que você possa revisar o nó.</span><span class="sxs-lookup"><span data-stu-id="9a468-153">**Scroll into view** lets you quickly reposition the viewport so that you are able to review the node.</span></span>  

1.  <span data-ttu-id="9a468-154">[Abra exemplos dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="9a468-154">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9a468-155">Em **Rolar para Exibir**, escolha **Magritte à** direita e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="9a468-155">Under **Scroll into View**, right-choose **Magritte** and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="9a468-156">Role até a parte inferior da página Exemplos dom.</span><span class="sxs-lookup"><span data-stu-id="9a468-156">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="9a468-157">O `<li>Magritte</li>` nó ainda deve ser selecionado em sua Árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="9a468-157">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="9a468-158">Caso não seja, volte para [Rolar para a exibição](#scroll-into-view) e comece de novo.</span><span class="sxs-lookup"><span data-stu-id="9a468-158">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="9a468-159">Passe o mouse `<li>Magritte</li>` no nó, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Rolar para exibição**.</span><span class="sxs-lookup"><span data-stu-id="9a468-159">Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.</span></span>  <span data-ttu-id="9a468-160">Seu modo de exibição rola de volta para cima para que você possa revisar o nó **Magritte.**</span><span class="sxs-lookup"><span data-stu-id="9a468-160">Your viewport scrolls back up so that you may review the **Magritte** node.</span></span>  <span data-ttu-id="9a468-161">Navegue [até Apêndice: Opções ausentes](#appendix-missing-options) se você não for capaz de revisar a opção **Rolar para exibição.**</span><span class="sxs-lookup"><span data-stu-id="9a468-161">Navigate to [Appendix: Missing options](#appendix-missing-options) if you are not able to review the **Scroll into view** option.</span></span>
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Rolar para a exibição" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **<span data-ttu-id="9a468-163">Rolar para a exibição</span><span class="sxs-lookup"><span data-stu-id="9a468-163">Scroll into view</span></span>**  
    :::image-end:::  

### <a name="search-for-nodes"></a><span data-ttu-id="9a468-164">Pesquisar nós</span><span class="sxs-lookup"><span data-stu-id="9a468-164">Search for nodes</span></span>  

<span data-ttu-id="9a468-165">Você pode pesquisar a Árvore DOM por cadeia de caracteres, seletor CSS ou seletor XPath.</span><span class="sxs-lookup"><span data-stu-id="9a468-165">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="9a468-166">Concentre o cursor na **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="9a468-166">Focus your cursor on the **Elements** tool.</span></span>  
1.  <span data-ttu-id="9a468-167">Selecione `Control` + `F` \(Windows, Linux\) `Command` + `F` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="9a468-167">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="9a468-168">A barra de pesquisa é aberta na parte inferior da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="9a468-168">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="9a468-169">Digite `The Moon is a Harsh Mistress`.</span><span class="sxs-lookup"><span data-stu-id="9a468-169">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="9a468-170">A última frase é realçada na Árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="9a468-170">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Realça a consulta na barra de pesquisa" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       <span data-ttu-id="9a468-172">Realça a consulta na barra de pesquisa</span><span class="sxs-lookup"><span data-stu-id="9a468-172">Highlight the query in the Search bar</span></span>  
    :::image-end:::  
    
<span data-ttu-id="9a468-173">Como mencionado acima, a barra de pesquisa também dá suporte a seletores CSS e XPath.</span><span class="sxs-lookup"><span data-stu-id="9a468-173">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <a name="edit-the-dom"></a><span data-ttu-id="9a468-174">Editar o DOM</span><span class="sxs-lookup"><span data-stu-id="9a468-174">Edit the DOM</span></span>  

<span data-ttu-id="9a468-175">Você pode editar o DOM em tempo real e analisar como as alterações afetam a página.</span><span class="sxs-lookup"><span data-stu-id="9a468-175">You may edit the DOM on the fly and review how the changes affect the page.</span></span>  

### <a name="edit-content"></a><span data-ttu-id="9a468-176">Editar conteúdo</span><span class="sxs-lookup"><span data-stu-id="9a468-176">Edit content</span></span>  

<span data-ttu-id="9a468-177">Para editar o conteúdo de um nó, clique duas vezes no conteúdo na Árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="9a468-177">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="9a468-178">[Abra exemplos dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="9a468-178">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9a468-179">Em **Editar Conteúdo,** escolha **Michelle** com o direito e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="9a468-179">Under **Edit Content**, right-choose **Michelle** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9a468-180">Na Árvore DOM, clique duas vezes `Michelle` em .</span><span class="sxs-lookup"><span data-stu-id="9a468-180">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="9a468-181">Em outras palavras, clique duas vezes no texto `<li>` entre `</li>` e .</span><span class="sxs-lookup"><span data-stu-id="9a468-181">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="9a468-182">O texto é realçado para indicar que ele está selecionado.</span><span class="sxs-lookup"><span data-stu-id="9a468-182">The text is highlighted to indicate that it is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Editar o texto" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           <span data-ttu-id="9a468-184">Editar o texto</span><span class="sxs-lookup"><span data-stu-id="9a468-184">Edit the text</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="9a468-185">`Michelle`Exclua , digite e selecione para confirmar a `Leela` `Enter` alteração.</span><span class="sxs-lookup"><span data-stu-id="9a468-185">Delete `Michelle`, type `Leela`, then select `Enter` to confirm the change.</span></span>  <span data-ttu-id="9a468-186">O texto no DOM muda de **Michelle** para **Leela**.</span><span class="sxs-lookup"><span data-stu-id="9a468-186">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <a name="edit-attributes"></a><span data-ttu-id="9a468-187">Editar atributos</span><span class="sxs-lookup"><span data-stu-id="9a468-187">Edit attributes</span></span>  

<span data-ttu-id="9a468-188">Para editar atributos, clique duas vezes no nome ou no valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="9a468-188">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="9a468-189">Siga as instruções para saber como adicionar atributos a um nó.</span><span class="sxs-lookup"><span data-stu-id="9a468-189">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="9a468-190">[Abra exemplos dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="9a468-190">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9a468-191">Em **Editar Atributos,** escolha Com o direito **Descaro e** escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="9a468-191">Under **Edit Attributes**, right-choose **Howard** and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="9a468-192">Clique duas vezes `<li>` em .</span><span class="sxs-lookup"><span data-stu-id="9a468-192">Double-click `<li>`.</span></span>  <span data-ttu-id="9a468-193">O texto é realçado para indicar que o nó está selecionado.</span><span class="sxs-lookup"><span data-stu-id="9a468-193">The text is highlighted to indicate that the node is selected.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Editar o nó" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       <span data-ttu-id="9a468-195">Editar o nó</span><span class="sxs-lookup"><span data-stu-id="9a468-195">Edit the node</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9a468-196">Selecione a `Right` tecla de seta, adicione um espaço, digite `style="background-color:gold"` e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="9a468-196">Select the `Right` arrow key, add a space, type `style="background-color:gold"`, and then select `Enter`.</span></span>  <span data-ttu-id="9a468-197">A cor de plano de fundo do nó muda para ouro.</span><span class="sxs-lookup"><span data-stu-id="9a468-197">The background color of the node changes to gold.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Adicionar um atributo de estilo ao nó" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       <span data-ttu-id="9a468-199">Adicionar um `style` atributo ao nó</span><span class="sxs-lookup"><span data-stu-id="9a468-199">Add a `style` attribute to the node</span></span>  
    :::image-end:::  
    
### <a name="edit-node-type"></a><span data-ttu-id="9a468-200">Editar tipo de nó</span><span class="sxs-lookup"><span data-stu-id="9a468-200">Edit node type</span></span>  

<span data-ttu-id="9a468-201">Para editar o tipo de nó, clique duas vezes no tipo e digite o novo tipo.</span><span class="sxs-lookup"><span data-stu-id="9a468-201">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="9a468-202">[Abra exemplos dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="9a468-202">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9a468-203">Em **Editar Tipo de Nó,** escolha à direita o **Hank** e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="9a468-203">Under **Edit Node Type**, right-choose **Hank** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9a468-204">Clique duas vezes `<li>` em .</span><span class="sxs-lookup"><span data-stu-id="9a468-204">Double-click `<li>`.</span></span>  <span data-ttu-id="9a468-205">O texto `li` é realçado.</span><span class="sxs-lookup"><span data-stu-id="9a468-205">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="9a468-206">Excluir `li` , `button` digitar, em seguida, selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="9a468-206">Delete `li`, type `button`, then select `Enter`.</span></span>  <span data-ttu-id="9a468-207">O `<li>` nó muda para um `<button>` nó.</span><span class="sxs-lookup"><span data-stu-id="9a468-207">The `<li>` node changes to a `<button>` node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Alterar o tipo de nó para botão" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           <span data-ttu-id="9a468-209">Alterar o tipo de nó para</span><span class="sxs-lookup"><span data-stu-id="9a468-209">Change the node type to</span></span> `button`  
        :::image-end:::  
        
### <a name="reorder-dom-nodes"></a><span data-ttu-id="9a468-210">Reordenar nós DOM</span><span class="sxs-lookup"><span data-stu-id="9a468-210">Reorder DOM nodes</span></span>  

<span data-ttu-id="9a468-211">Arraste nós para reordená-los.</span><span class="sxs-lookup"><span data-stu-id="9a468-211">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="9a468-212">[Abra exemplos dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="9a468-212">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9a468-213">Em **Reorder DOM Nodes**, escolha Com o direito **o nome de Elvis Presley** e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="9a468-213">Under **Reorder DOM Nodes**, right-choose **Elvis Presley** and choose **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="9a468-214">É o último item da lista.</span><span class="sxs-lookup"><span data-stu-id="9a468-214">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="9a468-215">Na Árvore DOM, arraste `<li>Elvis Presley</li>` até a parte superior da lista.</span><span class="sxs-lookup"><span data-stu-id="9a468-215">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Arraste o nó para a parte superior da lista" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           <span data-ttu-id="9a468-217">Arraste o nó para a parte superior da lista</span><span class="sxs-lookup"><span data-stu-id="9a468-217">Drag the node to the top of the list</span></span>  
        :::image-end:::  
        
### <a name="force-state"></a><span data-ttu-id="9a468-218">Estado de força</span><span class="sxs-lookup"><span data-stu-id="9a468-218">Force state</span></span>  

<span data-ttu-id="9a468-219">Você pode forçar nós a permanecerem em estados, incluindo `:active` , , , e `:hover` `:focus` `:visited` `:focus-within` .</span><span class="sxs-lookup"><span data-stu-id="9a468-219">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="9a468-220">[Abra exemplos dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="9a468-220">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9a468-221">Em **Estado de Força**, passe o mouse sobre O Senhor das **Moscas.**</span><span class="sxs-lookup"><span data-stu-id="9a468-221">Under **Force state**, hover on **The Lord of the Flies**.</span></span>  <span data-ttu-id="9a468-222">A cor do plano de fundo se torna laranja.</span><span class="sxs-lookup"><span data-stu-id="9a468-222">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="9a468-223">Passe o **mouse em O Senhor das Moscas**, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="9a468-223">Hover on **The Lord of the Flies**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9a468-224">Passe o mouse sobre , abra o menu contextual \(clique com o botão `<li class="demo--hover">The Lord of the Flies</li>` direito do mouse\) e escolha **Force State**  >  **:hover**.</span><span class="sxs-lookup"><span data-stu-id="9a468-224">Hover on `<li class="demo--hover">The Lord of the Flies</li>`, open the contextual menu \(right-click\), and choose **Force State** > **:hover**.</span></span>  <span data-ttu-id="9a468-225">Navegue [até Apêndice: Opções ausentes](#appendix-missing-options) se a opção não for exibida.</span><span class="sxs-lookup"><span data-stu-id="9a468-225">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  <span data-ttu-id="9a468-226">A cor do plano de fundo permanece laranja, mesmo que você não seja realmente pairando sobre o nó.</span><span class="sxs-lookup"><span data-stu-id="9a468-226">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <a name="hide-a-node"></a><span data-ttu-id="9a468-227">Ocultar um nó</span><span class="sxs-lookup"><span data-stu-id="9a468-227">Hide a node</span></span>  

<span data-ttu-id="9a468-228">Selecione `H` para ocultar um nó.</span><span class="sxs-lookup"><span data-stu-id="9a468-228">Select `H` to hide a node.</span></span>  

1.  <span data-ttu-id="9a468-229">[Abra exemplos dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="9a468-229">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9a468-230">Em **Ocultar um nó**, escolha Com a direita As Estrelas Meu **Destino** e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="9a468-230">Under **Hide a node**, right-choose **The Stars My Destination** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9a468-231">Selecione a `H` tecla.</span><span class="sxs-lookup"><span data-stu-id="9a468-231">Select the `H` key.</span></span>  <span data-ttu-id="9a468-232">O nó está oculto.</span><span class="sxs-lookup"><span data-stu-id="9a468-232">The node is hidden.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Como o nó se parece na árvore DOM depois que ele está oculto" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           <span data-ttu-id="9a468-234">Como o nó se parece na árvore DOM depois que ele está oculto</span><span class="sxs-lookup"><span data-stu-id="9a468-234">What the node looks like in the DOM Tree after it is hidden</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="9a468-235">Selecione a `H` tecla novamente.</span><span class="sxs-lookup"><span data-stu-id="9a468-235">Select the `H` key again.</span></span>  <span data-ttu-id="9a468-236">O nó é mostrado novamente.</span><span class="sxs-lookup"><span data-stu-id="9a468-236">The node is shown again.</span></span>  

### <a name="delete-a-node"></a><span data-ttu-id="9a468-237">Excluir um nó</span><span class="sxs-lookup"><span data-stu-id="9a468-237">Delete a node</span></span>  

<span data-ttu-id="9a468-238">Selecione `Delete` para excluir um nó.</span><span class="sxs-lookup"><span data-stu-id="9a468-238">Select `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="9a468-239">[Abra exemplos dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="9a468-239">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9a468-240">Em **Excluir um Nó,** escolha à direita **Foundation** e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="9a468-240">Under **Delete a Node**, right-choose **Foundation** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9a468-241">Selecione a `Delete` tecla.</span><span class="sxs-lookup"><span data-stu-id="9a468-241">Select the `Delete` key.</span></span>  <span data-ttu-id="9a468-242">O nó é excluído.</span><span class="sxs-lookup"><span data-stu-id="9a468-242">The node is deleted.</span></span>  
    1.  <span data-ttu-id="9a468-243">Selecione `Control` + `Z` \(Windows, Linux\) `Command` + `Z` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="9a468-243">Select `Control`+`Z` \(Windows, Linux\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="9a468-244">A última ação é desfeita e o nó reaparece.</span><span class="sxs-lookup"><span data-stu-id="9a468-244">The last action is undone and the node reappears.</span></span>  

## <a name="access-nodes-in-the-console"></a><span data-ttu-id="9a468-245">Acessar nós no Console</span><span class="sxs-lookup"><span data-stu-id="9a468-245">Access nodes in the Console</span></span>  

<span data-ttu-id="9a468-246">O DevTools fornece alguns atalhos para acessar nós DOM do Console ou obter referências javaScript para cada um deles.</span><span class="sxs-lookup"><span data-stu-id="9a468-246">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <a name="reference-the-currently-selected-node-with-0"></a><span data-ttu-id="9a468-247">Fazer referência ao nó selecionado no momento com $0</span><span class="sxs-lookup"><span data-stu-id="9a468-247">Reference the currently-selected node with $0</span></span>  

<span data-ttu-id="9a468-248">Quando você inspeciona um nó, o texto ao lado do nó significa que você pode fazer referência a esse nó no `== $0` Console com a variável `$0` .</span><span class="sxs-lookup"><span data-stu-id="9a468-248">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="9a468-249">[Abra exemplos dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="9a468-249">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9a468-250">Em Referência, o nó selecionado no momento com **$0**, escolha à direita **A Mão** Esquerda da Escuridão e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="9a468-250">Under **Reference the currently-selected node with $0**, right-choose **The Left Hand of Darkness** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9a468-251">Selecione a `Escape` chave para abrir a Gaveta do Console.</span><span class="sxs-lookup"><span data-stu-id="9a468-251">Select the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="9a468-252">Digite `$0` e selecione a `Enter` tecla.</span><span class="sxs-lookup"><span data-stu-id="9a468-252">Type `$0` and select the `Enter` key.</span></span>  <span data-ttu-id="9a468-253">O resultado da expressão mostra que `$0` avalia `<li>The Left Hand of Darkness</li>` como .</span><span class="sxs-lookup"><span data-stu-id="9a468-253">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="O resultado da primeira expressão $0 no Console" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            <span data-ttu-id="9a468-255">O resultado da primeira `$0` expressão no **Console**</span><span class="sxs-lookup"><span data-stu-id="9a468-255">The result of the first `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="9a468-256">Passe o mouse no resultado.</span><span class="sxs-lookup"><span data-stu-id="9a468-256">Hover on the result.</span></span>  <span data-ttu-id="9a468-257">O nó é realçado no viewport.</span><span class="sxs-lookup"><span data-stu-id="9a468-257">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="9a468-258">Escolha `<li>Dune</li>` na Árvore DOM, digite o Console novamente `$0` e selecione `Enter` novamente.</span><span class="sxs-lookup"><span data-stu-id="9a468-258">Choose `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then select `Enter` again.</span></span>  <span data-ttu-id="9a468-259">Agora, `$0` avalia como `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="9a468-259">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="O resultado da segunda expressão $0 no Console" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           <span data-ttu-id="9a468-261">O resultado da segunda `$0` expressão no **Console**</span><span class="sxs-lookup"><span data-stu-id="9a468-261">The result of the second `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
### <a name="store-as-global-variable"></a><span data-ttu-id="9a468-262">Armazenar como variável global</span><span class="sxs-lookup"><span data-stu-id="9a468-262">Store as global variable</span></span>  

<span data-ttu-id="9a468-263">Se você precisar fazer referência a um nó muitas vezes, armazene-o como uma variável global.</span><span class="sxs-lookup"><span data-stu-id="9a468-263">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="9a468-264">[Abra exemplos dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="9a468-264">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9a468-265">Em **Store como variável global,** passe o mouse em **O Grande Sono,** abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="9a468-265">Under **Store as global variable**, hover on **The Big Sleep**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9a468-266">Passe o `<li>The Big Sleep</li>` mouse na Árvore DOM, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Store como variável global**.</span><span class="sxs-lookup"><span data-stu-id="9a468-266">Hover on `<li>The Big Sleep</li>` in the DOM Tree, open the contextual menu \(right-click\), and choose **Store as global variable**.</span></span>  <span data-ttu-id="9a468-267">Navegue [até Apêndice: Opções ausentes](#appendix-missing-options) se a opção não for exibida.</span><span class="sxs-lookup"><span data-stu-id="9a468-267">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="9a468-268">Digite `temp1` o Console e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="9a468-268">Type `temp1` in the Console and then select `Enter`.</span></span>  <span data-ttu-id="9a468-269">O resultado da expressão mostra que a variável é avaliada para o nó.</span><span class="sxs-lookup"><span data-stu-id="9a468-269">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="O resultado da expressão temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           <span data-ttu-id="9a468-271">O resultado da `temp1` expressão</span><span class="sxs-lookup"><span data-stu-id="9a468-271">The result of the `temp1` expression</span></span>  
        :::image-end:::  
        
### <a name="copy-js-path"></a><span data-ttu-id="9a468-272">Copiar caminho JS</span><span class="sxs-lookup"><span data-stu-id="9a468-272">Copy JS path</span></span>  

<span data-ttu-id="9a468-273">Copie o caminho JavaScript para um nó quando precisar fazer referência a ele em um teste automatizado.</span><span class="sxs-lookup"><span data-stu-id="9a468-273">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="9a468-274">[Abra exemplos dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="9a468-274">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9a468-275">Em **Copiar caminho JS,** passe o mouse em **Os Irmãos Karamazov**, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="9a468-275">Under **Copy JS path**, hover on **The Brothers Karamazov**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9a468-276">Passe o mouse na Árvore DOM, abra o menu contextual \(clique com o botão direito do `<li>The Brothers Karamazov</li>` mouse\) e escolha **Copiar Copiar**  >  **Caminho JS**.</span><span class="sxs-lookup"><span data-stu-id="9a468-276">Hover on `<li>The Brothers Karamazov</li>` in the DOM Tree, open the contextual menu \(right-click\), and choose **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="9a468-277">Uma `document.querySelector()` expressão que resolve o nó foi copiada para sua área de transferência.</span><span class="sxs-lookup"><span data-stu-id="9a468-277">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="9a468-278">Selecione `Control` + `V` \(Windows, Linux\) ou `Command` + `V` \(macOS\) para colar a expressão no Console.</span><span class="sxs-lookup"><span data-stu-id="9a468-278">Select `Control`+`V` \(Windows, Linux\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="9a468-279">Selecione `Enter` para avaliar a expressão.</span><span class="sxs-lookup"><span data-stu-id="9a468-279">Select `Enter` to evaluate the expression.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="O resultado da expressão Copiar Caminho JS" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           <span data-ttu-id="9a468-281">O resultado da expressão **Copiar Caminho JS**</span><span class="sxs-lookup"><span data-stu-id="9a468-281">The result of the **Copy JS Path** expression</span></span>  
        :::image-end:::  
        
## <a name="break-on-dom-changes"></a><span data-ttu-id="9a468-282">Quebra nas alterações dom</span><span class="sxs-lookup"><span data-stu-id="9a468-282">Break on DOM changes</span></span>  

<span data-ttu-id="9a468-283">O DevTools permite pausar o JavaScript de uma página quando o JavaScript modifica o DOM.</span><span class="sxs-lookup"><span data-stu-id="9a468-283">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <a name="break-on-attribute-modifications"></a><span data-ttu-id="9a468-284">Quebra de modificações de atributo</span><span class="sxs-lookup"><span data-stu-id="9a468-284">Break on attribute modifications</span></span>  

<span data-ttu-id="9a468-285">Use pontos de interrupção de modificação de atributo quando quiser pausar o JavaScript que faz com que qualquer atributo de um nó seja modificado.</span><span class="sxs-lookup"><span data-stu-id="9a468-285">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="9a468-286">[Abra exemplos dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="9a468-286">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9a468-287">Em **Modificações de atributo Break on**, escolha **Sauerkraut** com a direita e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="9a468-287">Under **Break on attribute modifications**, right-choose **Sauerkraut** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9a468-288">Na Árvore DOM, passe o mouse sobre , abra o menu contextual \(clique com o botão direito do `<li id="target">Sauerkraut</li>` mouse\) e escolha **Quebrar Modificações**  >  **de Atributo**.</span><span class="sxs-lookup"><span data-stu-id="9a468-288">In the DOM Tree, hover on `<li id="target">Sauerkraut</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="9a468-289">Navegue [até Apêndice: Opções ausentes](#appendix-missing-options) se a opção não for exibida.</span><span class="sxs-lookup"><span data-stu-id="9a468-289">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Quebra de modificações de atributo" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **<span data-ttu-id="9a468-291">Quebra de modificações de atributo</span><span class="sxs-lookup"><span data-stu-id="9a468-291">Break on attribute modifications</span></span>**  
        :::image-end:::  
        
    1.  <span data-ttu-id="9a468-292">Na próxima etapa, você será instruído a escolher um botão que pausa o código da página.</span><span class="sxs-lookup"><span data-stu-id="9a468-292">In the next step you are going to be instructed to choose a button that pauses the code of the page.</span></span>  <span data-ttu-id="9a468-293">Depois que a página for pausada, você não poderá mais rolar a página.</span><span class="sxs-lookup"><span data-stu-id="9a468-293">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="9a468-294">Você deve escolher **Resume Script** \( Resume ![ Script ](../media/resume-script-icon.msft.png) \) para tornar a página rolável novamente.</span><span class="sxs-lookup"><span data-stu-id="9a468-294">You must choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\) in order to make the page scrollable again.</span></span>
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Onde retomar a execução do script" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           <span data-ttu-id="9a468-296">Onde retomar a execução do script</span><span class="sxs-lookup"><span data-stu-id="9a468-296">Where to resume script running</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="9a468-297">Escolha o **botão Definir Plano de** Fundo acima.</span><span class="sxs-lookup"><span data-stu-id="9a468-297">Choose the **Set Background** button above.</span></span>  <span data-ttu-id="9a468-298">Isso define o `style` atributo do nó como `background-color:thistle` .</span><span class="sxs-lookup"><span data-stu-id="9a468-298">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="9a468-299">O DevTools pausa a página e realça o código que causou a alteração do atributo.</span><span class="sxs-lookup"><span data-stu-id="9a468-299">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="9a468-300">Escolha **Retomar Script** \( Resume Script ![ ](../media/resume-script-icon.msft.png) \), conforme mencionado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9a468-300">Choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\), as mentioned earlier.</span></span>  
    
### <a name="break-on-node-removal"></a><span data-ttu-id="9a468-301">Quebra na remoção do nó</span><span class="sxs-lookup"><span data-stu-id="9a468-301">Break on node removal</span></span>  

<span data-ttu-id="9a468-302">Se você quiser pausar quando um nó específico for removido, use pontos de interrupção de remoção de nó.</span><span class="sxs-lookup"><span data-stu-id="9a468-302">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="9a468-303">[Abra exemplos dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="9a468-303">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9a468-304">Em **Quebra na Remoção de Nó**, escolha Com o direito o **Neuromancer** e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="9a468-304">Under **Break on Node Removal**, right-choose **Neuromancer** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9a468-305">Na Árvore DOM, passe o mouse sobre , abra o menu contextual \(clique com o botão direito `<li id="target">Neuromancer</li>` do mouse\) e escolha Break **On**  >  **Node Removal**.</span><span class="sxs-lookup"><span data-stu-id="9a468-305">In the DOM Tree, hover on `<li id="target">Neuromancer</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="9a468-306">Navegue [até Apêndice: Opções ausentes](#appendix-missing-options) se a opção não for exibida.</span><span class="sxs-lookup"><span data-stu-id="9a468-306">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="9a468-307">Escolha o **botão Excluir** acima.</span><span class="sxs-lookup"><span data-stu-id="9a468-307">Choose the **Delete** button above.</span></span>  <span data-ttu-id="9a468-308">O DevTools pausa a página e realça o código que fez com que o nó fosse removido.</span><span class="sxs-lookup"><span data-stu-id="9a468-308">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="9a468-309">Escolha **Retomar Script** \( Resume Script ![ ](../media/resume-script-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="9a468-309">Choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\).</span></span>  
    
### <a name="break-on-subtree-modifications"></a><span data-ttu-id="9a468-310">Quebra em modificações de subárvore</span><span class="sxs-lookup"><span data-stu-id="9a468-310">Break on subtree modifications</span></span>  

<span data-ttu-id="9a468-311">Depois de colocar um ponto de interrupção de modificação de subárvore em um nó, o DevTools pausa a página quando qualquer um dos descendentes do nó é adicionado ou removido.</span><span class="sxs-lookup"><span data-stu-id="9a468-311">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="9a468-312">[Abra exemplos dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="9a468-312">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9a468-313">Em **Break on Subtree Modifications**, right-choose **A Fire Upon The Deep** e choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="9a468-313">Under **Break on Subtree Modifications**, right-choose **A Fire Upon The Deep** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9a468-314">Na Árvore DOM, passe o mouse sobre , que é o nó acima, abra o menu contextual \(clique com o botão direito do mouse\) e escolha `<ul id="target">` `<li>A Fire Upon the Deep</li>` Quebrar **modificações**  >  **de subárvore**.</span><span class="sxs-lookup"><span data-stu-id="9a468-314">In the DOM Tree, hover on `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="9a468-315">Se a opção não for exibida, navegue até [Apêndice: Opções ausentes](#appendix-missing-options).</span><span class="sxs-lookup"><span data-stu-id="9a468-315">If the option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).</span></span>  
    1.  <span data-ttu-id="9a468-316">Escolha **Adicionar Filho**.</span><span class="sxs-lookup"><span data-stu-id="9a468-316">Choose **Add Child**.</span></span>  <span data-ttu-id="9a468-317">O código pausa porque um `<li>` nó foi adicionado à lista.</span><span class="sxs-lookup"><span data-stu-id="9a468-317">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="9a468-318">Escolha **Retomar Script** \( Resume Script ![ ](../media/resume-script-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="9a468-318">Choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\).</span></span>  
    
## <a name="next-steps"></a><span data-ttu-id="9a468-319">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="9a468-319">Next steps</span></span>  

<span data-ttu-id="9a468-320">Isso abrange a maioria dos recursos relacionados ao DOM no DevTools.</span><span class="sxs-lookup"><span data-stu-id="9a468-320">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="9a468-321">Você pode descobrir o restante dos recursos, pairando em nós na Árvore DOM, abrindo o menu contextual \(clique com o botão direito do mouse\) e experimentando as outras opções que não foram abordadas neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="9a468-321">You are able to discover the rest of the features by hovering on nodes in the DOM Tree, opening the contextual menu \(right-click\), and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="9a468-322">Navegue até atalhos de teclado [do painel Elementos.][DevToolsShortcutsElements]</span><span class="sxs-lookup"><span data-stu-id="9a468-322">Navigate to [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="9a468-323">Confira a página [inicial do Microsoft Edge DevTools][MicrosoftEdgeDevTools] para descobrir tudo o que você pode fazer com o DevTools.</span><span class="sxs-lookup"><span data-stu-id="9a468-323">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--Navigate to [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## <a name="appendix-html-versus-the-dom"></a><span data-ttu-id="9a468-324">Apêndice: HTML versus DOM</span><span class="sxs-lookup"><span data-stu-id="9a468-324">Appendix: HTML versus the DOM</span></span>  

<span data-ttu-id="9a468-325">A seção a seguir explica rapidamente a diferença entre HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="9a468-325">The following section quickly explains the difference between HTML and the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9a468-326">Quando você usa um navegador da Web para solicitar uma página, o servidor retorna HTML como o trecho de código a seguir</span><span class="sxs-lookup"><span data-stu-id="9a468-326">When you use a web browser to request a page, the server returns HTML like the following code snippet</span></span>  

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
      <span data-ttu-id="9a468-327">O navegador analisará o HTML e criará uma árvore de objetos como a lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a468-327">The browser parses the HTML and creates a tree of objects like the following list.</span></span>  
      
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

<span data-ttu-id="9a468-328">Essa árvore de objetos, ou nós, que representa o conteúdo da página é chamada de DOM.</span><span class="sxs-lookup"><span data-stu-id="9a468-328">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9a468-329">No momento, ele tem a mesma aparência do HTML, mas suponha que o script referenciado na parte inferior do HTML executa o seguinte trecho de código.</span><span class="sxs-lookup"><span data-stu-id="9a468-329">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs the following code snippet.</span></span>  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="9a468-330">Esse código remove o `h1` nó e adiciona outro nó ao `p` DOM.</span><span class="sxs-lookup"><span data-stu-id="9a468-330">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="9a468-331">O DOM completo agora exibe a lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a468-331">The complete DOM now displays the following list.</span></span>  
      
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

<span data-ttu-id="9a468-332">O HTML da página agora é diferente do DOM.</span><span class="sxs-lookup"><span data-stu-id="9a468-332">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="9a468-333">Em outras palavras, HTML representa o conteúdo inicial da página e o DOM representa o conteúdo da página atual.</span><span class="sxs-lookup"><span data-stu-id="9a468-333">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="9a468-334">Quando JavaScript adiciona, remove ou edita nós, o DOM se torna diferente do HTML.</span><span class="sxs-lookup"><span data-stu-id="9a468-334">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="9a468-335">Navegue [até Introdução ao DOM][MDNIntroductionToDOM] para saber mais.</span><span class="sxs-lookup"><span data-stu-id="9a468-335">Navigate to [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.  Your viewport scrolls back up so that the **Magritte** node is displayed.  If you the **Scroll into view** option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## <a name="appendix-missing-options"></a><span data-ttu-id="9a468-336">Apêndice: Opções ausentes</span><span class="sxs-lookup"><span data-stu-id="9a468-336">Appendix: Missing options</span></span>  

<span data-ttu-id="9a468-337">Muitas das instruções neste tutorial instruim você a passar o mouse em um nó na Árvore DOM, abra o menu contextual \(clique com o botão direito do mouse\) e escolha uma opção no menu de contexto que aparece.</span><span class="sxs-lookup"><span data-stu-id="9a468-337">Many of the instructions in this tutorial instruct you to hover on a node in the DOM Tree, open the contextual menu \(right-click\), and then choose an option from the context menu that pops up.</span></span>  <span data-ttu-id="9a468-338">Se a opção especificada no menu de contexto não for exibida, tente passar o mouse para longe do texto do nó e abrir o menu contextual \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="9a468-338">If the specified option in the context menu is not displayed, try hovering away from the node text and opening the contextual menu \(right-click\).</span></span>  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Onde escolher se todas as opções não são exibidas" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   <span data-ttu-id="9a468-340">Onde escolher se todas as opções não são exibidas</span><span class="sxs-lookup"><span data-stu-id="9a468-340">Where to choose if all of the options are not displayed</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="9a468-341">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9a468-341">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge \(Chromium\) | Microsoft Docs"  
[DevToolsCssGetStarted]: ../css/index.md "Começar a exibir e alterar o css | Microsoft Docs"  
[DevToolsShortcutsElements]: ../shortcuts/index.md#elements-tool-keyboard-shortcuts "Atalhos de teclado de ferramentas de elementos - Atalhos de teclado do Microsoft Edge DevTools | Microsoft Docs"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Exemplo do Microsoft Edge (Chromium) DevTools DOM | Glitch"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introdução ao dom | MDN"  

> [!NOTE]
> <span data-ttu-id="9a468-347">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9a468-347">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9a468-348">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/dom/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="9a468-348">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9a468-350">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9a468-350">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
