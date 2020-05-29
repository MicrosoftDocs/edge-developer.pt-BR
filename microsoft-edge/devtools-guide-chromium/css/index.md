---
title: Introdução à exibição e alteração de CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 85fceaa44b0143a82ca8f66ef8c63e1a9275dcd8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601814"
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





# <span data-ttu-id="1af5c-103">Introdução à exibição e alteração de CSS</span><span class="sxs-lookup"><span data-stu-id="1af5c-103">Get Started With Viewing And Changing CSS</span></span>   



<span data-ttu-id="1af5c-104">Preencha esses tutoriais interativos para aprender as noções básicas de exibição e alteração do CSS para uma página usando o Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="1af5c-104">Complete these interactive tutorials to learn the basics of viewing and changing the CSS for a page using Microsoft Edge DevTools.</span></span>  

## <span data-ttu-id="1af5c-105">Exemplos de CSS abertos</span><span class="sxs-lookup"><span data-stu-id="1af5c-105">Open CSS Examples</span></span>  

1.  <span data-ttu-id="1af5c-106">Segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e clique em **exemplos CSS** para abrir em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="1af5c-106">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **CSS Examples** to open in a new window.</span></span>  
    
    [<span data-ttu-id="1af5c-107">Exemplos de CSS</span><span class="sxs-lookup"><span data-stu-id="1af5c-107">CSS Examples</span></span>][GlitchDevToolsCssExamples]  

> [!NOTE]
> <span data-ttu-id="1af5c-108">Se você quiser [encaixar a janela do devtools][DevToolsCustomizePlacement] à direita do seu visor \ (exibido na [Figura 1](#figure-1)\), clique em **Personalizar e controlar o devtools** `...` .</span><span class="sxs-lookup"><span data-stu-id="1af5c-108">If you want to [dock your DevTools window][DevToolsCustomizePlacement] to the right of your viewport \(displayed in [Figure 1](#figure-1)\), click **Customize and control DevTools** `...`.</span></span>  <span data-ttu-id="1af5c-109">No menu suspenso **Personalizar e controlar devtools** , na seção do lado do **encaixe** , selecione **encaixar à direita**.</span><span class="sxs-lookup"><span data-stu-id="1af5c-109">On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, select **Dock to right**.</span></span>  
    
## <span data-ttu-id="1af5c-110">Exibir o CSS de um elemento</span><span class="sxs-lookup"><span data-stu-id="1af5c-110">View the CSS for an element</span></span>   

1.  <span data-ttu-id="1af5c-111">[Exemplos de CSS abertos](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="1af5c-111">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="1af5c-112">Clique com o botão direito do mouse no `Inspect Me!` texto e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="1af5c-112">Right-click the `Inspect Me!` text and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="1af5c-113">No DevTools, no painel **elementos** , na guia **árvore DOM** , o `Inspect Me!` elemento é realçado.</span><span class="sxs-lookup"><span data-stu-id="1af5c-113">In DevTools, on the **Elements** panel, in the **DOM Tree** tab, the `Inspect Me!` element is highlighted.</span></span>  
        
        > ##### <span data-ttu-id="1af5c-114">Figura 1</span><span class="sxs-lookup"><span data-stu-id="1af5c-114">Figure 1</span></span>  
        > <span data-ttu-id="1af5c-115">O elemento inspecionado é realçado na **árvore DOM**</span><span class="sxs-lookup"><span data-stu-id="1af5c-115">The inspected element is highlighted in the **DOM Tree**</span></span>  
        > ![O elemento inspecionado é realçado na árvore DOM][ImageInspect]  
        
    1.  <span data-ttu-id="1af5c-117">No `Inspect Me!` elemento, localize o valor do `data-message` atributo e copie-o.</span><span class="sxs-lookup"><span data-stu-id="1af5c-117">In the `Inspect Me!` element, find the value of the `data-message` attribute and copy it.</span></span>  
1.  <span data-ttu-id="1af5c-118">Na página, no **valor de `data-message` :** TextBox, insira o valor.</span><span class="sxs-lookup"><span data-stu-id="1af5c-118">On the page, in the **Value of `data-message`:** textbox, enter the value.</span></span>  
1.  <span data-ttu-id="1af5c-119">Clique com o botão direito do mouse no `Inspect Me!` texto e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="1af5c-119">Right-click the `Inspect Me!` text and select **Inspect**.</span></span>  
    
    1.  <span data-ttu-id="1af5c-120">No DevTools, no painel **elementos** , selecione a guia **estilos** .</span><span class="sxs-lookup"><span data-stu-id="1af5c-120">In DevTools, on the **Elements** panel, select the **Styles** tab.</span></span>  
    1.  <span data-ttu-id="1af5c-121">Na guia **estilos** , o `Inspect Me!` elemento é realçado.</span><span class="sxs-lookup"><span data-stu-id="1af5c-121">In the **Styles** tab, the `Inspect Me!` element is highlighted.</span></span>  
    1.  <span data-ttu-id="1af5c-122">No `Inspect Me!` elemento, localize a `aloha` regra de classe.</span><span class="sxs-lookup"><span data-stu-id="1af5c-122">In the `Inspect Me!` element, find the `aloha` class rule.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="1af5c-123">Você vê esta regra porque ela está sendo aplicada ao `Inspect Me!` elemento.</span><span class="sxs-lookup"><span data-stu-id="1af5c-123">You see this rule because it is being applied to the `Inspect Me!` element.</span></span>  
        
    1.  <span data-ttu-id="1af5c-124">Na `aloha` classe, localize o valor para o `padding` estilo e copie-o.</span><span class="sxs-lookup"><span data-stu-id="1af5c-124">In the `aloha` class, find the value for the `padding` style and copy it.</span></span>  
        
        > ##### <span data-ttu-id="1af5c-125">Figura 2</span><span class="sxs-lookup"><span data-stu-id="1af5c-125">Figure 2</span></span>  
        > <span data-ttu-id="1af5c-126">As classes CSS aplicadas ao elemento selecionado, como `aloha` , são exibidas na guia **estilos**</span><span class="sxs-lookup"><span data-stu-id="1af5c-126">CSS classes being applied to the selected element, such as `aloha`, are displayed in the **Styles** tab</span></span>  
        > ![As classes CSS aplicadas ao elemento inspecionado são realçadas na guia estilos][ImageAloha]  
        
1.  <span data-ttu-id="1af5c-128">Na página, no **valor de `padding` :** TextBox, insira o valor.</span><span class="sxs-lookup"><span data-stu-id="1af5c-128">On the page, in the **Value of `padding`:** textbox, enter the value.</span></span>  

## <span data-ttu-id="1af5c-129">Adicionar uma declaração CSS a um elemento</span><span class="sxs-lookup"><span data-stu-id="1af5c-129">Add a CSS declaration to an element</span></span>   

<span data-ttu-id="1af5c-130">Use a guia **estilos** quando desejar alterar ou adicionar declarações CSS a um elemento.</span><span class="sxs-lookup"><span data-stu-id="1af5c-130">Use the **Styles** tab when you want to change or add CSS declarations to an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="1af5c-131">Conclua a [exibição do CSS para um](#view-the-css-for-an-element) tutorial de elemento antes de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="1af5c-131">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="1af5c-132">[Exemplos de CSS abertos](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="1af5c-132">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="1af5c-133">Clique com o botão direito do mouse no `Add A Background Color To Me!` texto e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="1af5c-133">Right-click the `Add A Background Color To Me!` text and select **Inspect**.</span></span>  
1.  <span data-ttu-id="1af5c-134">Clique `element.style` próximo à parte superior da guia **estilos** .</span><span class="sxs-lookup"><span data-stu-id="1af5c-134">Click `element.style` near the top of the **Styles** tab.</span></span>  
1.  <span data-ttu-id="1af5c-135">Digite `background-color` e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="1af5c-135">Type `background-color` and press `Enter`.</span></span>  
1.  <span data-ttu-id="1af5c-136">Digite `honeydew` e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="1af5c-136">Type `honeydew` and press `Enter`.</span></span>  <span data-ttu-id="1af5c-137">Na **árvore DOM** , você verá que uma declaração de estilo embutido foi aplicada ao elemento.</span><span class="sxs-lookup"><span data-stu-id="1af5c-137">In the **DOM Tree** you should see that an inline style declaration was applied to the element.</span></span>  

> ##### <span data-ttu-id="1af5c-138">Figura 3</span><span class="sxs-lookup"><span data-stu-id="1af5c-138">Figure 3</span></span>  
> <span data-ttu-id="1af5c-139">A `background-color:honeydew` declaração foi aplicada ao elemento usando a `element.style` seção da guia **estilos**</span><span class="sxs-lookup"><span data-stu-id="1af5c-139">The `background-color:honeydew` declaration has been applied to the element using the `element.style` section of the **Styles** tab</span></span>  
> ![Adicionando uma declaração CSS ao elemento usando a guia estilos][ImageDeclaration]  

## <span data-ttu-id="1af5c-141">Adicionar uma classe CSS a um elemento</span><span class="sxs-lookup"><span data-stu-id="1af5c-141">Add a CSS class to an element</span></span>   

<span data-ttu-id="1af5c-142">Use a guia **estilos** para ver como um elemento se parece quando uma classe CSS é aplicada a ou removida de um elemento.</span><span class="sxs-lookup"><span data-stu-id="1af5c-142">Use the **Styles** tab to see how an element looks when a CSS class is applied to or removed from an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="1af5c-143">Conclua a [exibição do CSS para um](#view-the-css-for-an-element) tutorial de elemento antes de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="1af5c-143">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="1af5c-144">[Exemplos de CSS abertos](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="1af5c-144">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="1af5c-145">Clique com o botão direito do mouse no `Add A Class To Me!` elemento e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="1af5c-145">Right-click the `Add A Class To Me!` element and select **Inspect**.</span></span>  
1.  <span data-ttu-id="1af5c-146">Clique em **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="1af5c-146">Click **.cls**.</span></span>  <span data-ttu-id="1af5c-147">DevTools revela uma caixa de texto onde você pode adicionar classes ao elemento selecionado.</span><span class="sxs-lookup"><span data-stu-id="1af5c-147">DevTools reveals a text box where you may add classes to the selected element.</span></span>  
1.  <span data-ttu-id="1af5c-148">Digite `color_me` na caixa de texto **Adicionar nova classe** e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="1af5c-148">Type `color_me` in the **Add new class** text box and then press `Enter`.</span></span>  <span data-ttu-id="1af5c-149">Uma caixa de seleção é exibida abaixo da caixa de texto **Adicionar nova classe** , em que você pode ativar e desativar a classe.</span><span class="sxs-lookup"><span data-stu-id="1af5c-149">A checkbox appears below the **Add new class** text box, where you may toggle the class on and off.</span></span>  <span data-ttu-id="1af5c-150">Se o `Add A Class To Me!` elemento tiver outras classes aplicadas a ele, você também poderá alternar entre eles.</span><span class="sxs-lookup"><span data-stu-id="1af5c-150">If the `Add A Class To Me!` element has any other classes applied to it, you are also able to toggle each from here.</span></span>  

> ##### <span data-ttu-id="1af5c-151">Figura 4</span><span class="sxs-lookup"><span data-stu-id="1af5c-151">Figure 4</span></span>  
> <span data-ttu-id="1af5c-152">A `color_me` classe foi aplicada ao elemento usando a seção **. CLS** da guia **estilos**</span><span class="sxs-lookup"><span data-stu-id="1af5c-152">The `color_me` class has been applied to the element using the **.cls** section of the **Styles** tab</span></span>  
> ![Aplicando a classe color_me ao elemento][ImageApplyClass]  

## <span data-ttu-id="1af5c-154">Adicionar um PseudoState a uma classe</span><span class="sxs-lookup"><span data-stu-id="1af5c-154">Add a pseudostate to a class</span></span>   

<span data-ttu-id="1af5c-155">Use a guia **estilos** para aplicar permanentemente um PseudoState CSS a um elemento.</span><span class="sxs-lookup"><span data-stu-id="1af5c-155">Use the **Styles** tab to permanently apply a CSS pseudostate to an element.</span></span>  <span data-ttu-id="1af5c-156">DevTools dá suporte a `:active` ,, `:focus` `:hover` e `:visited` .</span><span class="sxs-lookup"><span data-stu-id="1af5c-156">DevTools supports `:active`, `:focus`, `:hover`, and `:visited`.</span></span>  

> [!NOTE]
> <span data-ttu-id="1af5c-157">Conclua a [exibição do CSS para um](#view-the-css-for-an-element) tutorial de elemento antes de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="1af5c-157">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="1af5c-158">[Exemplos de CSS abertos](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="1af5c-158">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="1af5c-159">Passe o mouse sobre o `Hover Over Me!` texto.</span><span class="sxs-lookup"><span data-stu-id="1af5c-159">Hover over the `Hover Over Me!` text.</span></span>  <span data-ttu-id="1af5c-160">A cor do plano de fundo muda.</span><span class="sxs-lookup"><span data-stu-id="1af5c-160">The background color changes.</span></span>  
1.  <span data-ttu-id="1af5c-161">Clique com o botão direito do mouse no `Hover Over Me!` texto e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="1af5c-161">Right-click the `Hover Over Me!` text and select **Inspect**.</span></span>  
1.  <span data-ttu-id="1af5c-162">Na guia **estilos** , clique em **: Hov**.</span><span class="sxs-lookup"><span data-stu-id="1af5c-162">In the **Styles** tab, click **:hov**.</span></span>  
1.  <span data-ttu-id="1af5c-163">Marque a caixa de seleção **: hover** .</span><span class="sxs-lookup"><span data-stu-id="1af5c-163">Check the **:hover** checkbox.</span></span>  <span data-ttu-id="1af5c-164">A cor do plano de fundo muda como antes, mesmo que você não esteja efetivamente passando o mouse sobre o elemento.</span><span class="sxs-lookup"><span data-stu-id="1af5c-164">The background color changes like before, even though you are not actually hovering over the element.</span></span>  

> ##### <span data-ttu-id="1af5c-165">Figura 5</span><span class="sxs-lookup"><span data-stu-id="1af5c-165">Figure 5</span></span>  
> <span data-ttu-id="1af5c-166">Alternando o `:hover` PseudoState em um elemento</span><span class="sxs-lookup"><span data-stu-id="1af5c-166">Toggling the `:hover` pseudostate on an element</span></span>  
> ![Alternando o PseudoState de foco em um elemento][ImageSetHover]  

## <span data-ttu-id="1af5c-168">Alterar as dimensões de um elemento</span><span class="sxs-lookup"><span data-stu-id="1af5c-168">Change the dimensions of an element</span></span>   

<span data-ttu-id="1af5c-169">Use o diagrama interativo do **modelo de caixa** na guia **estilos** para alterar a largura, a altura, o enchimento, a margem ou o comprimento da borda de um elemento.</span><span class="sxs-lookup"><span data-stu-id="1af5c-169">Use the **Box Model** interactive diagram in the **Styles** tab to change the width, height, padding, margin, or border length of an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="1af5c-170">Conclua a [exibição do CSS para um](#view-the-css-for-an-element) tutorial de elemento antes de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="1af5c-170">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="1af5c-171">[Exemplos de CSS abertos](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="1af5c-171">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="1af5c-172">Clique com o botão direito do mouse no `Change My Margin!` elemento e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="1af5c-172">Right-click the `Change My Margin!` element and select **Inspect**.</span></span>  
1.  <span data-ttu-id="1af5c-173">No diagrama de **modelo de caixa** na guia **estilos** , passe o mouse sobre o **preenchimento**.</span><span class="sxs-lookup"><span data-stu-id="1af5c-173">In the **Box Model** diagram in the **Styles** tab, hover over **padding**.</span></span>  <span data-ttu-id="1af5c-174">O preenchimento de um elemento é realçado no visor.</span><span class="sxs-lookup"><span data-stu-id="1af5c-174">The padding of an element is highlighted in the viewport.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="1af5c-175">Dependendo do tamanho da janela do DevTools, talvez seja necessário rolar até a parte inferior da guia **estilos** para ver o **modelo de caixa**.</span><span class="sxs-lookup"><span data-stu-id="1af5c-175">Depending on the size of your DevTools window, you may need to scroll to the bottom of the **Styles** tab to see the **Box Model**.</span></span>  

1.  <span data-ttu-id="1af5c-176">Clique duas vezes na margem esquerda no **modelo de caixa**, que atualmente tem um valor `-` que indica que o elemento não tem uma margem esquerda.</span><span class="sxs-lookup"><span data-stu-id="1af5c-176">Double-click the left margin in the **Box Model**, which currently has a value of `-` meaning that the element does not have a left-margin.</span></span>  
1.  <span data-ttu-id="1af5c-177">Digite `100px` e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="1af5c-177">Type `100px` and press `Enter`.</span></span>  <span data-ttu-id="1af5c-178">O **modelo de caixa** tem como padrão pixels, mas também aceita outros valores, como `25%` ou `10vw` .</span><span class="sxs-lookup"><span data-stu-id="1af5c-178">The **Box Model** defaults to pixels, but it also accepts other values, such as `25%`, or `10vw`.</span></span>  

> ##### <span data-ttu-id="1af5c-179">Figura 6</span><span class="sxs-lookup"><span data-stu-id="1af5c-179">Figure 6</span></span>  
> <span data-ttu-id="1af5c-180">Passando o cursor sobre o preenchimento do elemento</span><span class="sxs-lookup"><span data-stu-id="1af5c-180">Hovering over the padding of the element</span></span>  
> ![Passando o cursor sobre o preenchimento do elemento][ImageShowPadding]  

> ##### <span data-ttu-id="1af5c-182">Figura 7</span><span class="sxs-lookup"><span data-stu-id="1af5c-182">Figure 7</span></span>  
> <span data-ttu-id="1af5c-183">Alterar a margem esquerda do elemento</span><span class="sxs-lookup"><span data-stu-id="1af5c-183">Changing the left-margin of the element</span></span>  
> ![Alterar a margem esquerda do elemento][ImageChangeMargin]  

 



<!-- image links -->  

[ImageInspect]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me.msft.png "Figura 1: o elemento inspecionado é realçado na árvore DOM"  
[ImageAloha]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me-styles.msft.png "Figura 2: as classes CSS aplicadas ao elemento inspecionado são realçadas na guia estilos"  
[ImageDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-background-color-to-me-styles-p.msft.png "Figura 3: adicionando uma declaração CSS ao elemento usando a guia estilos"  
[ImageApplyClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-a-class-to-me-styles-cls.msft.png "Figura 4: aplicando a classe color_me ao elemento"  
[ImageSetHover]: /microsoft-edge/devtools-guide-chromium/media/css-elements-hover-over-me-styles-hov-hover.msft.png "Figura 5: alternando o pseudo-passe de hover em um elemento"  
[ImageShowPadding]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-padding.msft.png "Figura 6: passando o cursor sobre o preenchimento do elemento"  
[ImageChangeMargin]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-margin-edit.msft.png "Figura 7: alterando a margem esquerda do elemento"  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Alterar o posicionamento do Microsoft Edge DevTools (desencaixar, encaixar na parte inferior, encaixar à esquerda)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Exemplos de CSS-Microsoft Edge (Chromium) DevTools | Problema"  

> [!NOTE]
> <span data-ttu-id="1af5c-194">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="1af5c-194">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1af5c-195">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/css/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="1af5c-195">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1af5c-197">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1af5c-197">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
