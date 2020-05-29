---
title: Navegar no Microsoft Edge DevTools com tecnologia assistencial
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 5de27e46d20957a1be79f72cf36074291566e6e5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560844"
---
<!-- Copyright Rob Dodson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="9433b-103">Navegar no Microsoft Edge DevTools com tecnologia assistencial</span><span class="sxs-lookup"><span data-stu-id="9433b-103">Navigate Microsoft Edge DevTools With Assistive Technology</span></span>   



<span data-ttu-id="9433b-104">Este guia tem como objetivo ajudar os usuários que dependem principalmente da tecnologia adaptativa, como leitores de tela, a usar o Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="9433b-104">This guide aims to help users who primarily rely on assistive technology like screen readers access and use Microsoft Edge DevTools.</span></span>  <span data-ttu-id="9433b-105">O Microsoft Edge DevTools é um pacote de ferramentas de desenvolvedor da Web integrado ao navegador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9433b-105">Microsoft Edge DevTools is a suite of web developer tools built into the Microsoft Edge browser.</span></span>  <!--See [Accessibility Reference][DevtoolsAccessibilityReference] if you are looking for DevTools features related to improving the accessibility of a web page.  -->

<!--todo: add edge devtools index section when available  -->  
<!--todo: add reference (Accessibility Reference) section when available  -->  

<span data-ttu-id="9433b-106">A acessibilidade do DevTools é um trabalho em andamento.</span><span class="sxs-lookup"><span data-stu-id="9433b-106">The accessibility of DevTools is a work-in-progress.</span></span>  <span data-ttu-id="9433b-107">Alguns painéis e guias funcionam melhor com a tecnologia assistencial do que outros.</span><span class="sxs-lookup"><span data-stu-id="9433b-107">Some panels and tabs work better with assistive technology than others.</span></span>  <span data-ttu-id="9433b-108">Este guia o orienta pelos painéis que são mais acessíveis e realça problemas específicos que você pode encontrar ao longo do caminho.</span><span class="sxs-lookup"><span data-stu-id="9433b-108">This guide walks you through the panels which are the most accessible and highlights specific issues you may encounter along the way.</span></span>  

## <span data-ttu-id="9433b-109">Visão geral</span><span class="sxs-lookup"><span data-stu-id="9433b-109">Overview</span></span>   

<span data-ttu-id="9433b-110">Antes de começar, é útil ter um modelo mental de como a interface do usuário do DevTools é estruturada.</span><span class="sxs-lookup"><span data-stu-id="9433b-110">Before starting, it helps to have a mental model of how the DevTools UI is structured.</span></span>  <span data-ttu-id="9433b-111">DevTools é dividido em uma série de painéis que são organizados em um [Aria `tablist` ][W3CWaiAriaTablist].</span><span class="sxs-lookup"><span data-stu-id="9433b-111">DevTools is divided into a series of panels which are organized into an [ARIA `tablist`][W3CWaiAriaTablist].</span></span>  

<span data-ttu-id="9433b-112">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="9433b-112">For example:</span></span>  

*   <span data-ttu-id="9433b-113">O painel **elementos** permite que você visualize e altere os nós dom ou [CSS] [DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="9433b-113">The **Elements** panel lets you view and change DOM nodes or [CSS][DevtoolsCssIndex].</span></span>  
*   <span data-ttu-id="9433b-114">O [painel do**console** ] [DevtoolsConsoleIndex] permite que você leia os logs de JavaScript e os objetos de edição ao vivo.</span><span class="sxs-lookup"><span data-stu-id="9433b-114">The [**Console** panel][DevtoolsConsoleIndex] lets you read JavaScript logs and live edit objects.</span></span>  

<!--todo:  add dom nodes (dom nodes) section when available  -->  

<span data-ttu-id="9433b-115">Na área de conteúdo de cada painel, há várias ferramentas diferentes, muitas vezes chamadas de guias ou painéis na documentação.</span><span class="sxs-lookup"><span data-stu-id="9433b-115">Within the content area of each panel, there are a number of different tools, often referred to as tabs or panes in the documentation.</span></span>  
<span data-ttu-id="9433b-116">Por exemplo, o painel **elementos** contém guias adicionais para inspecionar ouvintes de eventos, a árvore de acessibilidade e muito mais.</span><span class="sxs-lookup"><span data-stu-id="9433b-116">For instance, the **Elements** panel contains additional tabs to inspect event listeners, the accessibility tree, and much more.</span></span>  <span data-ttu-id="9433b-117">A distinção entre guias e painéis é um pouco arbitrária.</span><span class="sxs-lookup"><span data-stu-id="9433b-117">The distinction between tabs and panes is somewhat arbitrary.</span></span>  <span data-ttu-id="9433b-118">A única razão pela qual você pode ver um termo ou o outro é manter a consistência com o restante da documentação oficial do DevTools.</span><span class="sxs-lookup"><span data-stu-id="9433b-118">The only reason you may see one term or the other is to maintain consistency with the rest of the official DevTools documentation.</span></span>  

## <span data-ttu-id="9433b-119">Atalhos de teclado</span><span class="sxs-lookup"><span data-stu-id="9433b-119">Keyboard shortcuts</span></span>   

<span data-ttu-id="9433b-120">A [DevTools de atalhos de teclado do [] é um cheatsheet útil.</span><span class="sxs-lookup"><span data-stu-id="9433b-120">The [DevTools Keyboard Shortcuts reference][DevtoolsShortcuts] is a helpful cheatsheet.</span></span>  <span data-ttu-id="9433b-121">Certifique-se de marcá-lo e consultá-lo enquanto explora os diferentes painéis.</span><span class="sxs-lookup"><span data-stu-id="9433b-121">Be sure to bookmark it and refer back to it as you explore the different panels.</span></span>  

## <span data-ttu-id="9433b-122">Abrir o DevTools</span><span class="sxs-lookup"><span data-stu-id="9433b-122">Open DevTools</span></span>   

<span data-ttu-id="9433b-123">Para começar, leia [Open Microsoft Edge DevTools] [DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="9433b-123">To get started, read through [Open Microsoft Edge DevTools][DevtoolsOpen].</span></span>  <span data-ttu-id="9433b-124">Há várias maneiras de abrir o DevTools, por meio de atalhos de teclado ou itens de menu.</span><span class="sxs-lookup"><span data-stu-id="9433b-124">There are a number of ways to open DevTools, either through keyboard shortcuts or menu items.</span></span>  

## <span data-ttu-id="9433b-125">Navegar entre painéis</span><span class="sxs-lookup"><span data-stu-id="9433b-125">Navigate between panels</span></span>   

### <span data-ttu-id="9433b-126">Navegar por teclado</span><span class="sxs-lookup"><span data-stu-id="9433b-126">Navigate by keyboard</span></span>   

*   <span data-ttu-id="9433b-127">Com o devtools aberto, pressione `Control` + `]` \ (Windows \) ou `Command` + `]` \ (MacOS \) para concentrar o próximo painel.</span><span class="sxs-lookup"><span data-stu-id="9433b-127">With DevTools open, press `Control`+`]` \(Windows\) or `Command`+`]` \(macOS\) to focus the next panel.</span></span>  
*   <span data-ttu-id="9433b-128">Pressione `Control` + `[` \ (Windows \) ou `Command` + `[` \ (MacOS \) para concentrar o painel anterior.</span><span class="sxs-lookup"><span data-stu-id="9433b-128">Press `Control`+`[` \(Windows\) or `Command`+`[` \(macOS\) to focus the previous panel.</span></span>  
*   <span data-ttu-id="9433b-129">Também é possível usar `Shift` + `Tab` para mover o foco para o [Aria `tablist` ][W3CWaiAriaTablist] de um painel e usar as teclas de direção para alterar os painéis, embora ele possa ser mais rápido de usar os atalhos mencionados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9433b-129">It is also possible to use `Shift`+`Tab` to move focus into the [ARIA `tablist`][W3CWaiAriaTablist] of a panel and use the arrow keys to change panels, though it may be faster to use the previously mentioned shortcuts.</span></span>  

#### <span data-ttu-id="9433b-130">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="9433b-130">Known issues</span></span>   

*   <span data-ttu-id="9433b-131">Alguns painéis, como o **console** e os painéis de **desempenho** , podem mover o foco para a área de conteúdo assim que eles são ativados.</span><span class="sxs-lookup"><span data-stu-id="9433b-131">Some panels, such as the **Console** and **Performance** panels, may move focus into their content area as soon as they are activated.</span></span>  <span data-ttu-id="9433b-132">Isso pode dificultar a navegação pelas teclas de direção.</span><span class="sxs-lookup"><span data-stu-id="9433b-132">This may make navigating by arrow keys difficult.</span></span>  
*   <span data-ttu-id="9433b-133">O nome do painel selecionado é anunciado, mas só depois que ele lê o conteúdo focalizado no painel.</span><span class="sxs-lookup"><span data-stu-id="9433b-133">The name of the selected panel is announced, but only after it has read the focused content in the panel.</span></span>  <span data-ttu-id="9433b-134">Isso pode facilitar a perda.</span><span class="sxs-lookup"><span data-stu-id="9433b-134">This may make it very easy to miss.</span></span>  

### <span data-ttu-id="9433b-135">Navegar por menu de comando</span><span class="sxs-lookup"><span data-stu-id="9433b-135">Navigate by Command Menu</span></span>   

<span data-ttu-id="9433b-136">Para focalizar um painel específico, use o [**menu de comando**] [DevtoolsCommandMenuIndex]:</span><span class="sxs-lookup"><span data-stu-id="9433b-136">To focus a specific panel, use the [**Command Menu**][DevtoolsCommandMenuIndex]:</span></span>  

1.  <span data-ttu-id="9433b-137">Com o devtools aberto, pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comando**.</span><span class="sxs-lookup"><span data-stu-id="9433b-137">With DevTools open, press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    <span data-ttu-id="9433b-138">O **menu de comando** é um ComboBox AutoComplete de pesquisa difusa.</span><span class="sxs-lookup"><span data-stu-id="9433b-138">The **Command Menu** is a fuzzy search autocomplete combobox.</span></span>  
1.  <span data-ttu-id="9433b-139">Digite o nome do painel que você deseja abrir e use o `Down Arrow` no teclado para navegar até a opção correta.</span><span class="sxs-lookup"><span data-stu-id="9433b-139">Type the name of the panel you want to open, then use the `Down Arrow` on the keyboard to navigate to the correct option.</span></span>  
1.  <span data-ttu-id="9433b-140">Pressione `Enter` para executar um comando.</span><span class="sxs-lookup"><span data-stu-id="9433b-140">Press `Enter` to run a command.</span></span>  

<span data-ttu-id="9433b-141">Por exemplo, para abrir o painel **elementos** :</span><span class="sxs-lookup"><span data-stu-id="9433b-141">For example, to open the **Elements** panel:</span></span>  

1.  <span data-ttu-id="9433b-142">Abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="9433b-142">Open the **Command Menu**.</span></span>  
1.  <span data-ttu-id="9433b-143">Digite `E` então `L` .</span><span class="sxs-lookup"><span data-stu-id="9433b-143">Type `E` then `L`.</span></span>  <span data-ttu-id="9433b-144">O **painel > opção Mostrar elementos** está selecionado.</span><span class="sxs-lookup"><span data-stu-id="9433b-144">The **Panel > Show Elements** option is selected.</span></span>  
1.  <span data-ttu-id="9433b-145">Pressione `Enter` para executar o comando que abre o painel.</span><span class="sxs-lookup"><span data-stu-id="9433b-145">Press `Enter` to run the command that opens the panel.</span></span>  

<span data-ttu-id="9433b-146">Abrir um painel dessa maneira direciona o foco para o conteúdo do painel.</span><span class="sxs-lookup"><span data-stu-id="9433b-146">Opening a panel this way directs focus to the contents of the panel.</span></span>  <span data-ttu-id="9433b-147">No caso do painel **elementos** , o foco se move para a **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="9433b-147">In the case of the **Elements** panel, focus moves into the **DOM Tree**.</span></span>  

## <span data-ttu-id="9433b-148">Painel elementos</span><span class="sxs-lookup"><span data-stu-id="9433b-148">Elements panel</span></span>   

### <span data-ttu-id="9433b-149">Inspecionar um elemento na página</span><span class="sxs-lookup"><span data-stu-id="9433b-149">Inspect an element on the page</span></span>   

1.  <span data-ttu-id="9433b-150">Navegue até o elemento que você deseja inspecionar usando o cursor no leitor de tela.</span><span class="sxs-lookup"><span data-stu-id="9433b-150">Navigate to the element you want to inspect using the cursor in the screen reader.</span></span>  
1.  <span data-ttu-id="9433b-151">Simule um clique com o botão direito do mouse no elemento para abrir o menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="9433b-151">Simulate a right-mouse click on the element to open the context menu.</span></span>  
1.  <span data-ttu-id="9433b-152">Escolha a opção **inspecionar** .</span><span class="sxs-lookup"><span data-stu-id="9433b-152">Choose the **Inspect** option.</span></span>  <span data-ttu-id="9433b-153">Isso abre o painel de **elementos** e enfoca o elemento na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="9433b-153">This opens the **Elements** panel and focuses the element in the **DOM Tree**.</span></span>  

<!--todo:  add dom nodes (elements pane) section when available  -->  

<span data-ttu-id="9433b-154">A **árvore DOM** é disposta como um [Aria `tree` ][W3CWaiAriaTree].</span><span class="sxs-lookup"><span data-stu-id="9433b-154">The **DOM Tree** is laid out as an [ARIA `tree`][W3CWaiAriaTree].</span></span>  <!--See [Navigate the **DOM Tree** with a keyboard][DevtoolsDomIndexNavigateDomTreeKeyboard] for an example.  -->  

<!--todo: add dom index navigation tree section then available  -->

### <span data-ttu-id="9433b-155">Copiar o código de um elemento na árvore DOM</span><span class="sxs-lookup"><span data-stu-id="9433b-155">Copy the code for an element in the DOM Tree</span></span>   

1.  <span data-ttu-id="9433b-156">Com o foco em um nó na **árvore DOM**, abra o menu de contexto clique com o botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="9433b-156">With focus on a node in the **DOM Tree**, bring up the right-click context menu.</span></span>  
1.  <span data-ttu-id="9433b-157">Expanda a opção de **cópia** .</span><span class="sxs-lookup"><span data-stu-id="9433b-157">Expand the **Copy** option.</span></span>  
1.  <span data-ttu-id="9433b-158">Selecione **copiar OuterHtml**.</span><span class="sxs-lookup"><span data-stu-id="9433b-158">Select **Copy outerHTML**.</span></span>  

#### <span data-ttu-id="9433b-159">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="9433b-159">Known issues</span></span>   

*   <span data-ttu-id="9433b-160">**Copy OuterHtml** geralmente não seleciona o nó atual, em vez disso, seleciona o nó pai.</span><span class="sxs-lookup"><span data-stu-id="9433b-160">**Copy outerHTML** often does not select the current node but instead selects the parent node.</span></span>  <span data-ttu-id="9433b-161">No entanto, o conteúdo do elemento ainda deve estar na outerHTML copiada.</span><span class="sxs-lookup"><span data-stu-id="9433b-161">However, the contents of the element should still be in the copied outerHTML.</span></span>  

### <span data-ttu-id="9433b-162">Modificar os atributos de um elemento na árvore DOM</span><span class="sxs-lookup"><span data-stu-id="9433b-162">Modify the attributes of an element in the DOM Tree</span></span>   

*   <span data-ttu-id="9433b-163">Com o foco em um nó na **árvore DOM**, pressione `Enter` para torná-lo editável.</span><span class="sxs-lookup"><span data-stu-id="9433b-163">With focus on a node in the **DOM Tree**, press `Enter` to make it editable.</span></span>  
*   <span data-ttu-id="9433b-164">Pressione `Tab` para mover-se entre os valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="9433b-164">Press `Tab` to move between attribute values.</span></span>  <span data-ttu-id="9433b-165">Quando você ouvir "espaço", você está dentro de uma entrada de texto vazia e poderá digitar um novo valor de atributo.</span><span class="sxs-lookup"><span data-stu-id="9433b-165">When you hear "space" you are inside of an empty text input and are able to type a new attribute value.</span></span>  
*   <span data-ttu-id="9433b-166">Pressione `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) para aceitar a alteração e ouvir todo o conteúdo do elemento.</span><span class="sxs-lookup"><span data-stu-id="9433b-166">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to accept the change and hear the entire contents of the element.</span></span>  

#### <span data-ttu-id="9433b-167">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="9433b-167">Known issues</span></span>   

*   <span data-ttu-id="9433b-168">Ao digitar na entrada de texto, você não recebe nenhum comentário.</span><span class="sxs-lookup"><span data-stu-id="9433b-168">When you type into the text input you get no feedback.</span></span>  <span data-ttu-id="9433b-169">Se você cometer um digitador e usar as teclas de direção para explorar a entrada, também não receberá nenhum comentário.</span><span class="sxs-lookup"><span data-stu-id="9433b-169">If you make a typo and use the arrow keys to explore your input you also get no feedback.</span></span>  <span data-ttu-id="9433b-170">A maneira mais fácil de verificar seu trabalho é aceitar a alteração e, em seguida, escutar o elemento inteiro a ser anunciado.</span><span class="sxs-lookup"><span data-stu-id="9433b-170">The easiest way to check your work is to accept the change, then listen for the entire element to be announced.</span></span>  

### <span data-ttu-id="9433b-171">Editar o HTML de um elemento na árvore DOM</span><span class="sxs-lookup"><span data-stu-id="9433b-171">Edit the HTML of an element in the DOM Tree</span></span>   

*   <span data-ttu-id="9433b-172">Com o foco em um nó na **árvore DOM**, pressione `Enter` para torná-lo editável.</span><span class="sxs-lookup"><span data-stu-id="9433b-172">With focus on a node in the **DOM Tree**, press `Enter` to make it editable.</span></span>  
*   <span data-ttu-id="9433b-173">Pressione `Tab` para mover-se entre os valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="9433b-173">Press `Tab` to move between attribute values.</span></span>  <span data-ttu-id="9433b-174">Quando você ouvir o nome do elemento, por exemplo, "H2", você está dentro de uma entrada de texto e poderá alterar o tipo do elemento.</span><span class="sxs-lookup"><span data-stu-id="9433b-174">When you hear the name of the element, for instance, "h2", you are inside of a text input and may change the type of the element.</span></span>  
*   <span data-ttu-id="9433b-175">Pressione `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) para aceitar a alteração.</span><span class="sxs-lookup"><span data-stu-id="9433b-175">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to accept the change.</span></span>  

<span data-ttu-id="9433b-176">Por exemplo, digitar `h3` e pressionar `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) altera as marcas de início e término do elemento para `h3` .</span><span class="sxs-lookup"><span data-stu-id="9433b-176">For example, typing `h3` and pressing `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) changes the start and end tags of the element to `h3`.</span></span>  

## <span data-ttu-id="9433b-177">Guias do painel elementos</span><span class="sxs-lookup"><span data-stu-id="9433b-177">Elements panel tabs</span></span>   

<span data-ttu-id="9433b-178">O painel **elementos** contém guias adicionais para inspecionar itens como o CSS aplicado a um elemento ou o local relevante na árvore de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="9433b-178">The **Elements** panel contains additional tabs for inspecting things like the CSS applied to an element or the relevant place in the accessibility tree.</span></span>  

*   <span data-ttu-id="9433b-179">Com o foco em um nó na **árvore DOM**, pressione `Tab` até ouvir que o painel **estilos** está selecionado.</span><span class="sxs-lookup"><span data-stu-id="9433b-179">With focus on a node in the **DOM Tree**, press `Tab` until you hear that the **Styles** pane is selected.</span></span>  
*   <span data-ttu-id="9433b-180">Use a `Right Arrow` para explorar outras guias disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9433b-180">Use the `Right Arrow` to explore other available tabs.</span></span>  

<span data-ttu-id="9433b-181">A **árvore DOM** transforma elementos com `href` atributos em links que podem ser focados, portanto, talvez seja necessário pressionar `Tab` mais de uma vez para acessar o painel de **estilos** .</span><span class="sxs-lookup"><span data-stu-id="9433b-181">The **DOM Tree** turns elements with `href` attributes into focusable links, so you may need to press `Tab` more than once to reach the **Styles** pane.</span></span>  

### <span data-ttu-id="9433b-182">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="9433b-182">Known issues</span></span>   

<span data-ttu-id="9433b-183">As guias de **pontos de interrupção** e **Propriedades** do dom não são acessíveis pelo teclado.</span><span class="sxs-lookup"><span data-stu-id="9433b-183">The **DOM Breakpoints** and **Properties** tabs are not keyboard accessible.</span></span>  

### <span data-ttu-id="9433b-184">Painel estilos</span><span class="sxs-lookup"><span data-stu-id="9433b-184">Styles pane</span></span>   

<span data-ttu-id="9433b-185">No painel **estilos** , encontre controles para filtrar estilos, alternar entre Estados de elemento \ (como [`:active`][MDNActive] e [`:focus`][MDNFocus] \), alternar classes e adicionar novas classes.</span><span class="sxs-lookup"><span data-stu-id="9433b-185">In the **Styles** pane find controls for filtering styles, toggling element states \(such as [`:active`][MDNActive] and [`:focus`][MDNFocus]\), toggling classes, and adding new classes.</span></span>  <span data-ttu-id="9433b-186">Também existe uma ferramenta de inspeção de estilo eficiente para explorar e modificar os estilos atualmente aplicados ao elemento que está em foco na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="9433b-186">There is also a powerful style inspection tool to explore and modify styles currently applied to the element that is in focus in the **DOM Tree**.</span></span>  

<span data-ttu-id="9433b-187">O conceito de chave para entender o painel **estilos** é que ele só mostra os estilos do nó atualmente selecionado na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="9433b-187">The key concept to understand about the **Styles** pane is that it only shows styles for the currently-selected node in the **DOM Tree**.</span></span>  <span data-ttu-id="9433b-188">Por exemplo, suponha que você tenha concluído a inspeção dos estilos de um `<header>` nó e agora deseja examinar os estilos de um `<footer>` nó.</span><span class="sxs-lookup"><span data-stu-id="9433b-188">For example, suppose you are done inspecting the styles of a `<header>` node, and now you want to look at the styles for a `<footer>` node.</span></span>  <span data-ttu-id="9433b-189">Para fazer isso, primeiro você precisa selecionar o `<footer>` nó na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="9433b-189">To do that, you first need to select the `<footer>` node in the **DOM Tree**.</span></span>  <span data-ttu-id="9433b-190">Você pode achar mais rápido usar o fluxo de trabalho [inspecionar](#inspect-an-element-on-the-page) para inspecionar um nó que está na proximidade geral do `footer` nó \ (como um link dentro do rodapé \), que enfoca a **árvore DOM**e use o teclado para navegar até o nó exato no qual você está interessado.</span><span class="sxs-lookup"><span data-stu-id="9433b-190">You may find it faster to use the [Inspect](#inspect-an-element-on-the-page) workflow to inspect a node that is in the general vicinity of the `footer` node \(such as a link within the footer\), which focuses the **DOM Tree**, and then use your keyboard to navigate to the exact node in which you are interested.</span></span>  

#### <span data-ttu-id="9433b-191">Navegar pelo painel estilos</span><span class="sxs-lookup"><span data-stu-id="9433b-191">Navigate the Styles pane</span></span>   

<span data-ttu-id="9433b-192">Como todas as ferramentas de estilo se conectam de uma maneira ou de outra volta ao painel **estilos** , faz sentido dominar essa ferramenta primeiro.</span><span class="sxs-lookup"><span data-stu-id="9433b-192">Because all of the style tools connect in one way or another back to the **Styles** pane, it makes sense to master this tool first.</span></span>  

*   <span data-ttu-id="9433b-193">Com o foco no painel **estilos** , pressione `Tab` para mover o foco dentro e explore o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="9433b-193">With focus on the **Styles** pane, press `Tab` to move focus inside and explore the contents.</span></span>  
*   <span data-ttu-id="9433b-194">Pressione `Tab` até que o primeiro estilo se torne ativo.</span><span class="sxs-lookup"><span data-stu-id="9433b-194">Press `Tab` until the first style becomes active.</span></span>  <span data-ttu-id="9433b-195">Se você estiver usando um leitor de tela, este primeiro estilo será anunciado como "elemento. Style {} ".</span><span class="sxs-lookup"><span data-stu-id="9433b-195">If you are using a screen reader this first style is announced as "element.style {}".</span></span>  
*   <span data-ttu-id="9433b-196">Pressione `Down Arrow` para navegar pela lista de estilos em ordem de específica.</span><span class="sxs-lookup"><span data-stu-id="9433b-196">Press `Down Arrow` to navigate the list of styles in order of specificity.</span></span>  <span data-ttu-id="9433b-197">Um leitor de tela anuncia cada estilo que começa com o nome do arquivo CSS, o número da linha em que o estilo aparece e o nome do estilo.</span><span class="sxs-lookup"><span data-stu-id="9433b-197">A screen reader announces each style starting with the name of the CSS file, the line number on which the style appears, and the name of the style.</span></span>  <span data-ttu-id="9433b-198">Por exemplo: "Main. css: 233. card__img {} "</span><span class="sxs-lookup"><span data-stu-id="9433b-198">For example: "main.css:233 .card__img {}"</span></span>  
*   <span data-ttu-id="9433b-199">Pressione `Enter` para inspecionar um estilo em mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="9433b-199">Press `Enter` to inspect a style in more detail.</span></span>  <span data-ttu-id="9433b-200">O foco começa em uma versão editável do nome do estilo.</span><span class="sxs-lookup"><span data-stu-id="9433b-200">Focus begins on an editable version of the style name.</span></span>  
*   <span data-ttu-id="9433b-201">Pressione `Tab` para mover-se entre as versões editáveis de cada propriedade CSS e seus valores correspondentes.</span><span class="sxs-lookup"><span data-stu-id="9433b-201">Press `Tab` to move between editable versions of each CSS property and their corresponding values.</span></span>  <span data-ttu-id="9433b-202">No final de cada bloco de estilo está um campo de texto editável em branco que você pode usar para adicionar outras propriedades CSS.</span><span class="sxs-lookup"><span data-stu-id="9433b-202">At the end of each style block is a blank editable text field which you may use to add additional CSS properties.</span></span>  
*   <span data-ttu-id="9433b-203">Você pode continuar a pressionar `Tab` para percorrer a lista de estilos ou pressionar `Escape` para sair desse modo e voltar para navegar pelas teclas de direção.</span><span class="sxs-lookup"><span data-stu-id="9433b-203">You may continue to press `Tab` to move through the list of styles, or press `Escape` to exit this mode and go back to navigating by arrow keys.</span></span>  

<span data-ttu-id="9433b-204">Não deixe de ler a [referência do teclado do painel de estilos] [DevtoolsShortcutsStylesPaneKeyboard] para obter atalhos adicionais.</span><span class="sxs-lookup"><span data-stu-id="9433b-204">Be sure to read through the [Styles pane keyboard reference][DevtoolsShortcutsStylesPaneKeyboard] for additional shortcuts.</span></span>  

##### <span data-ttu-id="9433b-205">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="9433b-205">Known Issues</span></span>   

*   <span data-ttu-id="9433b-206">Se você usar o campo de texto de **filtro** editável, não será mais possível navegar na lista de estilos.</span><span class="sxs-lookup"><span data-stu-id="9433b-206">If you use the **Filter** editable text field, you are no longer be able to navigate the list of styles.</span></span>  

#### <span data-ttu-id="9433b-207">Alternar o estado do elemento</span><span class="sxs-lookup"><span data-stu-id="9433b-207">Toggle element state</span></span>   

<span data-ttu-id="9433b-208">Para alternar o estado de um elemento, como `:active` ou `:focus` :</span><span class="sxs-lookup"><span data-stu-id="9433b-208">To toggle the state of an element, such as `:active` or `:focus`:</span></span>  

1.  <span data-ttu-id="9433b-209">Navegue até o painel **estilos** e pressione `Tab` até o botão **alternar estado do elemento** ter foco.</span><span class="sxs-lookup"><span data-stu-id="9433b-209">Navigate to the **Styles** pane and press `Tab` until the **Toggle Element State** button has focus.</span></span>  
1.  <span data-ttu-id="9433b-210">Pressione `Enter` para expandir a coleção de Estados do elemento.</span><span class="sxs-lookup"><span data-stu-id="9433b-210">Press `Enter` to expand the collection of element states.</span></span>  <span data-ttu-id="9433b-211">Os Estados dos elementos são apresentados como um grupo de caixas de seleção.</span><span class="sxs-lookup"><span data-stu-id="9433b-211">The element states are presented as a group of checkboxes.</span></span>  
1.  <span data-ttu-id="9433b-212">Pressione `Tab` até o primeiro Estado, `:active` com foco.</span><span class="sxs-lookup"><span data-stu-id="9433b-212">Press `Tab` until the first state, `:active`, has focus.</span></span>  
1.  <span data-ttu-id="9433b-213">Pressione `Space` para habilitá-la.</span><span class="sxs-lookup"><span data-stu-id="9433b-213">Press `Space` to enable it.</span></span>  <span data-ttu-id="9433b-214">Se o elemento atualmente selecionado na árvore DOM tiver um `:active` estilo, ele será aplicado agora.</span><span class="sxs-lookup"><span data-stu-id="9433b-214">If the currently-selected element in the DOM Tree has an `:active` style, it is now applied.</span></span>  
1.  <span data-ttu-id="9433b-215">Continue pressionando `Tab` para explorar todos os Estados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9433b-215">Continue pressing `Tab` to explore all of the available states.</span></span>  

#### <span data-ttu-id="9433b-216">Adicionar uma classe existente</span><span class="sxs-lookup"><span data-stu-id="9433b-216">Add an existing class</span></span>   

<span data-ttu-id="9433b-217">Adjacente ao botão **alternar estado do elemento** é o botão **classes do elemento** .</span><span class="sxs-lookup"><span data-stu-id="9433b-217">Adjacent to the **Toggle Element State** button is the **Element Classes** button.</span></span>  <span data-ttu-id="9433b-218">Para mover o foco para ele, pressione `Tab` em seguida `Enter` .</span><span class="sxs-lookup"><span data-stu-id="9433b-218">Move focus to it by pressing `Tab` then `Enter`.</span></span>  <span data-ttu-id="9433b-219">O foco se move para um campo de edição de texto rotulado **Adicionar nova classe**.</span><span class="sxs-lookup"><span data-stu-id="9433b-219">Focus moves into an edit text field labeled **Add New Class**.</span></span>  

<span data-ttu-id="9433b-220">O botão **classes de elemento** é usado principalmente para adicionar classes existentes a um elemento.</span><span class="sxs-lookup"><span data-stu-id="9433b-220">The **Element Classes** button is primarily used for adding existing classes to an element.</span></span>  <span data-ttu-id="9433b-221">Por exemplo, se a sua folha de estilos contiver uma classe auxiliar chamada `.clearfix` você pode pressionar `.` dentro do campo de edição de texto para ver uma lista de sugestões de classes e usar o `Down Arrow` para localizar a `.clearfix` sugestão.</span><span class="sxs-lookup"><span data-stu-id="9433b-221">For example, if your stylesheet contained a helper class named `.clearfix` you may press `.` inside of the edit text field to see a suggestion list of classes and use the `Down Arrow` to find the `.clearfix` suggestion.</span></span>  <span data-ttu-id="9433b-222">Ou digite o nome da classe e pressione `Enter` para aplicá-la.</span><span class="sxs-lookup"><span data-stu-id="9433b-222">Or type the class name out yourself and press `Enter` to apply it.</span></span>  

#### <span data-ttu-id="9433b-223">Adicionar uma nova regra de estilo</span><span class="sxs-lookup"><span data-stu-id="9433b-223">Add a new style rule</span></span>   

<span data-ttu-id="9433b-224">Adjacente ao botão **classes de elemento** é o botão **nova regra de estilo** .</span><span class="sxs-lookup"><span data-stu-id="9433b-224">Adjacent to the **Element Classes** button is the **New Style Rule** button.</span></span>  <span data-ttu-id="9433b-225">Para mover o foco para ele, `Tab` pressione e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="9433b-225">Move focus to it by pressing `Tab` and press `Enter`.</span></span>  <span data-ttu-id="9433b-226">O foco se move para um campo de texto editável dentro do Inspetor de estilo.</span><span class="sxs-lookup"><span data-stu-id="9433b-226">Focus moves into an editable text field inside of the style inspector.</span></span>  <span data-ttu-id="9433b-227">O conteúdo de texto inicial do campo é o nome da marca do elemento selecionado na **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="9433b-227">The initial text content of the field is the tag name of the element that is selected in the **DOM Tree**.</span></span>  
<span data-ttu-id="9433b-228">Você pode digitar qualquer nome de classe desejado nesse campo e, em seguida, pressionar `Tab` para atribuir propriedades CSS a ele.</span><span class="sxs-lookup"><span data-stu-id="9433b-228">You may type any class name you want into this field and then press `Tab` to assign CSS properties to it.</span></span>  

### <span data-ttu-id="9433b-229">Guia calculada</span><span class="sxs-lookup"><span data-stu-id="9433b-229">Computed tab</span></span>   

<span data-ttu-id="9433b-230">Com o foco na guia **calculada** , pressione `Tab` para mover o foco dentro e explore o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="9433b-230">With focus on the **Computed** tab, press `Tab` to move focus inside and explore the contents.</span></span>  <span data-ttu-id="9433b-231">Na guia **calculada** há controles para explorar quais propriedades de CSS são realmente aplicadas a um elemento em ordem de poder específica.</span><span class="sxs-lookup"><span data-stu-id="9433b-231">Within the **Computed** tab there are controls for exploring which CSS properties are actually applied to an element in order of specificity.</span></span>  

<!--todo: add computed tab section when available  -->  

#### <span data-ttu-id="9433b-232">Explorar todos os estilos calculados</span><span class="sxs-lookup"><span data-stu-id="9433b-232">Explore all computed styles</span></span>   

<span data-ttu-id="9433b-233">Pressione `Tab` até chegar à coleção de estilos calculados.</span><span class="sxs-lookup"><span data-stu-id="9433b-233">Press `Tab` until you reach the collection of computed styles.</span></span>  <span data-ttu-id="9433b-234">Eles são apresentados como um [Aria `tree` ][W3CWaiAriaTree].</span><span class="sxs-lookup"><span data-stu-id="9433b-234">These are presented as an [ARIA `tree`][W3CWaiAriaTree].</span></span>  <span data-ttu-id="9433b-235">Expandir uma ListBox revela quais seletores de CSS estão aplicando o estilo calculado.</span><span class="sxs-lookup"><span data-stu-id="9433b-235">Expanding a listbox reveals which CSS selectors are applying the computed style.</span></span>  <span data-ttu-id="9433b-236">Esses seletores são organizados por uma específica.</span><span class="sxs-lookup"><span data-stu-id="9433b-236">These selectors are organized by specificity.</span></span>  <span data-ttu-id="9433b-237">Um leitor de tela anuncia o valor calculado, em que o seletor de CSS está atualmente em correspondência, o nome do arquivo da folha de estilos que contém o seletor e o número da linha do seletor.</span><span class="sxs-lookup"><span data-stu-id="9433b-237">A screen reader announces the computed value, which CSS selector is currently matching, the filename of the stylesheet that contains the selector, and the line number for the selector.</span></span>  

#### <span data-ttu-id="9433b-238">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="9433b-238">Known issues</span></span>   

*   <span data-ttu-id="9433b-239">Se você usar o campo texto do **filtro** , não será mais possível inspecionar os estilos.</span><span class="sxs-lookup"><span data-stu-id="9433b-239">If you use the **Filter** text field, you are no longer able to inspect styles.</span></span>  

### <span data-ttu-id="9433b-240">Guia ouvintes de eventos</span><span class="sxs-lookup"><span data-stu-id="9433b-240">Event listeners tab</span></span>   

<span data-ttu-id="9433b-241">No painel **elementos** , você pode inspecionar os ouvintes de eventos aplicados a um elemento usando a guia **ouvintes de eventos** .  Com o foco no painel **estilos** , pressione a `Right Arrow` para navegar até a guia **ouvintes de eventos** .</span><span class="sxs-lookup"><span data-stu-id="9433b-241">From within the **Elements** panel you may inspect the event listeners applied to an element using the **Event Listeners** tab.  With focus on the **Styles** pane, press the `Right Arrow` to navigate to the **Event Listeners** tab.</span></span>  

#### <span data-ttu-id="9433b-242">Explorar ouvintes de eventos</span><span class="sxs-lookup"><span data-stu-id="9433b-242">Explore event listeners</span></span>   

<span data-ttu-id="9433b-243">Ouvintes de eventos são apresentados como [Aria `tree` ][W3CWaiAriaTree].</span><span class="sxs-lookup"><span data-stu-id="9433b-243">Event listeners are presented as an [ARIA `tree`][W3CWaiAriaTree].</span></span>  <span data-ttu-id="9433b-244">Você pode usar as teclas de direção para navegar.</span><span class="sxs-lookup"><span data-stu-id="9433b-244">You may use the arrow keys to navigate them.</span></span>  <span data-ttu-id="9433b-245">Um leitor de tela anuncia o nome do objeto DOM ao qual o ouvinte de eventos está associado, bem como o nome do arquivo em que o ouvinte de evento é definido e o número da linha.</span><span class="sxs-lookup"><span data-stu-id="9433b-245">A screen reader announces the name of the DOM object that the event listener is attached to, as well as the file name where the event listener is defined and the line number.</span></span>  

### <span data-ttu-id="9433b-246">Painel de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="9433b-246">Accessibility pane</span></span>   

<span data-ttu-id="9433b-247">Com o foco no painel de **acessibilidade** , pressione `Tab` para mover o foco dentro e explore o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="9433b-247">With focus on the **Accessibility** pane, press `Tab` to move focus inside and explore the contents.</span></span>  <span data-ttu-id="9433b-248">No painel **acessibilidade** , há controles para explorar a árvore de acessibilidade, os atributos do Aria aplicados a um elemento e as propriedades de acessibilidade calculadas.</span><span class="sxs-lookup"><span data-stu-id="9433b-248">Within the **Accessibility** pane there are controls for exploring the accessibility tree, the ARIA attributes applied to an element, and the computed accessibility properties.</span></span>  

<!--todo: add reference (Accessibility pane) section when available  -->  

#### <span data-ttu-id="9433b-249">Árvore de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="9433b-249">Accessibility Tree</span></span>   

<span data-ttu-id="9433b-250">A **árvore de acessibilidade** é apresentada como [um `tree` Aria][W3CWaiAriaTree] em que cada `treeitem` um corresponde a um elemento no dom.</span><span class="sxs-lookup"><span data-stu-id="9433b-250">The **Accessibility Tree** is presented as an [ARIA `tree`][W3CWaiAriaTree] where each `treeitem` corresponds to an element in the DOM.</span></span>  <span data-ttu-id="9433b-251">A árvore anuncia a função calculada para o nó selecionado.</span><span class="sxs-lookup"><span data-stu-id="9433b-251">The tree announces the computed role for the selected node.</span></span>  <span data-ttu-id="9433b-252">Elementos genéricos como `div` e `span` são anunciados como "GenericContainer" na árvore.</span><span class="sxs-lookup"><span data-stu-id="9433b-252">Generic elements like `div` and `span` are announced as "GenericContainer" in the tree.</span></span>  <span data-ttu-id="9433b-253">Use as teclas de direção para percorrer a árvore e explorar as relações pai-filho.</span><span class="sxs-lookup"><span data-stu-id="9433b-253">Use the arrow keys to traverse the tree and explore parent-child relationships.</span></span>  

#### <span data-ttu-id="9433b-254">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="9433b-254">Known issues</span></span>   

*   <span data-ttu-id="9433b-255">O tipo de [Aria `tree` ][W3CWaiAriaTree] usado pelo painel de **acessibilidade** pode não estar exposto corretamente no Microsoft Edge para leitores de tela do MacOS, como o VoiceOver.</span><span class="sxs-lookup"><span data-stu-id="9433b-255">The type of [ARIA `tree`][W3CWaiAriaTree] used by the **Accessibility** pane may not be properly exposed in Microsoft Edge for macOS screen readers like VoiceOver.</span></span>  <span data-ttu-id="9433b-256">Assine o [problema do Chromium #868480][ChromiumIssues868480] ser informado sobre o progresso sobre esse problema.</span><span class="sxs-lookup"><span data-stu-id="9433b-256">Subscribe to [Chromium issue #868480][ChromiumIssues868480] to be informed about progress on this issue.</span></span>  
*   <span data-ttu-id="9433b-257">Cada um dos **atributos do Aria** e as seções de **Propriedades calculadas** são marcados [como `tree` Aria ][W3CWaiAriaTree], mas cada um não tem atualmente o gerenciamento de foco e não tem o teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="9433b-257">Each of the **ARIA Attributes** and **Computed Properties** sections are marked up as an [ARIA `tree`][W3CWaiAriaTree], but each does not currently have focus management and is not keyboard operable.</span></span>  

## <span data-ttu-id="9433b-258">Painel auditorias</span><span class="sxs-lookup"><span data-stu-id="9433b-258">Audits panel</span></span>   

<span data-ttu-id="9433b-259">O painel **auditorias** você deve executar uma série de testes em um site para verificar problemas comuns relacionados a desempenho, acessibilidade, SEO e várias outras categorias.</span><span class="sxs-lookup"><span data-stu-id="9433b-259">The **Audits** panel you should run a series of tests against a site to check for common issues related to performance, accessibility, SEO, and a number of other categories.</span></span>  

### <span data-ttu-id="9433b-260">Configurar e executar uma auditoria</span><span class="sxs-lookup"><span data-stu-id="9433b-260">Configure and run an audit</span></span>   

1.  <span data-ttu-id="9433b-261">Quando o painel **auditorias** é aberto pela primeira vez, o foco é colocado no botão **executar auditoria** no final do formulário.</span><span class="sxs-lookup"><span data-stu-id="9433b-261">When the **Audits** panel is first opened, focus is placed on the **Run Audit** button at the end of the form.</span></span>  <span data-ttu-id="9433b-262">Por padrão, o formulário é configurado para executar auditorias para cada categoria usando emulação de celular em uma conexão 3G simulada.</span><span class="sxs-lookup"><span data-stu-id="9433b-262">By default the form is configured to run audits for every category using mobile emulation on a simulated 3G connection.</span></span>  
1.  <span data-ttu-id="9433b-263">Use `Shift` + `Tab` ou navegue de volta no modo de navegação para alterar as configurações de auditoria.</span><span class="sxs-lookup"><span data-stu-id="9433b-263">Use `Shift`+`Tab` or navigate back in Browse mode to change the audit settings.</span></span>  
1.  <span data-ttu-id="9433b-264">Quando estiver pronto para executar a auditoria, navegue de volta para o botão **executar auditoria** e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="9433b-264">When you are ready to run the audit, navigate back to the **Run Audit** button and press `Enter`.</span></span>  
1.  <span data-ttu-id="9433b-265">O foco se move em uma janela modal com um botão **Cancelar** que permite que você saia da auditoria.</span><span class="sxs-lookup"><span data-stu-id="9433b-265">Focus moves into a modal window with a **Cancel** button which allows you to exit the audit.</span></span>  <span data-ttu-id="9433b-266">Você pode ouvir uma série de earcons à medida que a auditoria é executada e atualiza a página várias vezes.</span><span class="sxs-lookup"><span data-stu-id="9433b-266">You may hear a series of earcons as the audit runs and refreshes the page multiple times.</span></span>  

#### <span data-ttu-id="9433b-267">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="9433b-267">Known issues</span></span>   

*   <span data-ttu-id="9433b-268">As diferentes seções do formulário de configuração não estão atualmente marcadas com um `fieldset` elemento.</span><span class="sxs-lookup"><span data-stu-id="9433b-268">The different sections of the configuration form are not currently marked up with a `fieldset` element.</span></span>  <span data-ttu-id="9433b-269">Pode ser mais fácil navegar no modo de procura para descobrir quais controles estão associados a cada seção.</span><span class="sxs-lookup"><span data-stu-id="9433b-269">It may be easier to navigate them in Browse mode to figure out which controls are associated with each section.</span></span>  
*   <span data-ttu-id="9433b-270">Não há anúncio earcon ou região ao vivo quando a execução da auditoria termina.</span><span class="sxs-lookup"><span data-stu-id="9433b-270">There is no earcon or live region announcement when the audit is finished running.</span></span>  <span data-ttu-id="9433b-271">Geralmente, demora cerca de 30 segundos, após o qual você deve conseguir navegar até os resultados.</span><span class="sxs-lookup"><span data-stu-id="9433b-271">Generally it takes about 30 seconds, after which you should be able to navigate to the results.</span></span>  <span data-ttu-id="9433b-272">Usar o modo de procura pode ser a maneira mais fácil de alcançar os resultados.</span><span class="sxs-lookup"><span data-stu-id="9433b-272">Using Browse mode may be the easiest way to reach the results.</span></span>  

### <span data-ttu-id="9433b-273">Navegar no relatório de auditoria</span><span class="sxs-lookup"><span data-stu-id="9433b-273">Navigate the audit report</span></span>   

<span data-ttu-id="9433b-274">O relatório de auditoria é organizado em seções que correspondem a cada uma das categorias de auditoria.</span><span class="sxs-lookup"><span data-stu-id="9433b-274">The audit report is organized into sections that correspond with each of the audit categories.</span></span>  <span data-ttu-id="9433b-275">O relatório é aberto com uma lista de resultados para cada categoria.</span><span class="sxs-lookup"><span data-stu-id="9433b-275">The report opens with a list of scores for each category.</span></span>  <span data-ttu-id="9433b-276">Esses resultados também são links que podem ser usados para pular para as seções relevantes.</span><span class="sxs-lookup"><span data-stu-id="9433b-276">These scores are also links which are able to be used to skip to the relevant sections.</span></span>  <span data-ttu-id="9433b-277">Em cada seção `details` , há elementos expansíveis que contêm informações relacionadas a auditorias aprovadas ou falhas.</span><span class="sxs-lookup"><span data-stu-id="9433b-277">Within each section are expandable `details` elements, which contain information relating to passed or failed audits.</span></span>  <span data-ttu-id="9433b-278">Por padrão, somente as auditorias com falha são mostradas.</span><span class="sxs-lookup"><span data-stu-id="9433b-278">By default, only failing audits are shown.</span></span>  <span data-ttu-id="9433b-279">Cada seção termina com um `details` elemento final que contém todas as auditorias passadas.</span><span class="sxs-lookup"><span data-stu-id="9433b-279">Each section ends with a final `details` element which contains all of the passed audits.</span></span>  

<span data-ttu-id="9433b-280">Para executar uma nova auditoria, use `Shift` + `Tab` para sair do relatório e procure o botão **executar uma auditoria** .</span><span class="sxs-lookup"><span data-stu-id="9433b-280">To run a new audit, use `Shift`+`Tab` to exit the report and look for the **Perform An Audit** button.</span></span>  

## <span data-ttu-id="9433b-281">Privacidade Jurídica</span><span class="sxs-lookup"><span data-stu-id="9433b-281">Feedback</span></span>   

*   <span data-ttu-id="9433b-282">Envie relatórios de bug DevTools ou solicitações de recursos para [Chromium Issue Tracker][MonorailChromiumIssues].</span><span class="sxs-lookup"><span data-stu-id="9433b-282">Send DevTools bug reports or feature requests to [Chromium Issue Tracker][MonorailChromiumIssues].</span></span>  
*   <span data-ttu-id="9433b-283">Envie qualquer comentário relacionado a este documento para o [GitHub][GithubEdgeDeveloperNewIssue].</span><span class="sxs-lookup"><span data-stu-id="9433b-283">Send any feedback related to this document to [GitHub][GithubEdgeDeveloperNewIssue].</span></span>  

<!-- image links -->  

<!-- links -->  

<!--[DevtoolsAccessibilityReference]: reference.md "Accessibility Reference"  -->  
<!--[DevtoolsAccessibilityReferencePane]: reference.md#the-accessibility-pane "The Accessibility pane - Accessibility Reference"  -->  

<!--[MicrosoftEdgeDevtoolsIndex]: ../index.md "Microsoft Edge DevTools"  -->  
[DevtoolsCommandMenuIndex]: .. /Command-menu/index.MD "executar comandos com o menu de comando do Microsoft Edge DevTools"  
[DevtoolsConsoleIndex]: .. /console/index.MD "visão geral do console"  
[DevtoolsCssIndex]: .. /CSS/index.MD "comece a exibir e alterar CSS"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get Started With Viewing And Changing The DOM"  -->  
<!--[DevtoolsDomIndexNavigateDomTreeKeyboard]: ../dom/index.md#navigate-the-dom-tree-with-a-keyboard "Navigate the DOM Tree with a keyboard - Get Started With Viewing And Changing The DOM"  -->
[DevtoolsOpen]: .. /open.md "abrir o Microsoft Edge DevTools"  
[DevtoolsShortcuts]: .. /shortcuts.md "atalhos de teclado do Microsoft Edge DevTools"  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /Shortcuts.MD # estilos-painel-atalhos de teclado "atalhos de teclado do painel estilos-atalhos de teclado do Microsoft Edge DevTools"  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Problema 868480-expor árvores do ARIA como tabelas na acessibilidade do Mac"  
[GithubEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Docs%20Feedback%5D "Novo problema-MicrosoftDocs/Edge-Developer | GitHub"  
[MDNActive]: https://developer.mozilla.org/docs/Web/CSS/:active ": ativo | MDN"  
[MDNFocus]: https://developer.mozilla.org/docs/Web/CSS/:focus ": foco | MDN"  
[MonorailChromiumIssues]: https://crbug.com "Problemas-Chromium-monorail"  
[W3CWaiAriaTablist]: https://www.w3.org/TR/wai-aria-1.1/#tablist "tablist (função)-aplicativos da Internet sofisticados acessíveis (WAI-ARIA) 1,1 | W3C"  
[W3CWaiAriaTree]: https://www.w3.org/TR/wai-aria-1.1/#tree "Tree (função)-aplicativos sofisticados da Internet acessíveis (WAI-ARIA) 1,1 | W3C"  

> [!NOTE]
> <span data-ttu-id="9433b-297">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="9433b-297">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9433b-298">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) e é criada por [Rob Dodson][RobDodson] \ (colaborador, Google webfundamentals \).</span><span class="sxs-lookup"><span data-stu-id="9433b-298">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) and is authored by [Rob Dodson][RobDodson] \(Contributor, Google WebFundamentals\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9433b-300">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9433b-300">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[RobDodson]: https://developers.google.com/web/resources/contributors/robdodson  
