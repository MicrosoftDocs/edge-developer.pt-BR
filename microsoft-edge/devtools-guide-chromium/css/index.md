---
title: Introdução à Visualização e Mudança da CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 346145a7deb9e8ac951ed0578a5060da72817463
ms.sourcegitcommit: a34858dd3260967ba9699842fa839c7a94775fe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/12/2020
ms.locfileid: "10710382"
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

# <span data-ttu-id="40d10-103">Introdução à Visualização e Mudança da CSS</span><span class="sxs-lookup"><span data-stu-id="40d10-103">Get Started With Viewing And Changing CSS</span></span>  

<span data-ttu-id="40d10-104">Preencha esses tutoriais interativos para aprender as noções básicas de exibição e alteração do CSS para uma página usando o Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="40d10-104">Complete these interactive tutorials to learn the basics of viewing and changing the CSS for a page using Microsoft Edge DevTools.</span></span>  

## <span data-ttu-id="40d10-105">Exemplos de CSS abertos</span><span class="sxs-lookup"><span data-stu-id="40d10-105">Open CSS Examples</span></span>  

1.  <span data-ttu-id="40d10-106">Segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e selecione **exemplos CSS** para abrir em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="40d10-106">Hold `Control` \(Windows\) or `Command` \(macOS\) and select **CSS Examples** to open in a new window.</span></span>  
    
    [<span data-ttu-id="40d10-107">Exemplos de CSS</span><span class="sxs-lookup"><span data-stu-id="40d10-107">CSS Examples</span></span>][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > <span data-ttu-id="40d10-108">Se você quiser [encaixar a janela do devtools][DevToolsCustomizePlacement] à direita do seu visor \ (exibido na figura a seguir), selecione **Personalizar e controlar o devtools** `...` .</span><span class="sxs-lookup"><span data-stu-id="40d10-108">If you want to [dock your DevTools window][DevToolsCustomizePlacement] to the right of your viewport \(displayed in the following figure\), select **Customize and control DevTools** `...`.</span></span>  <span data-ttu-id="40d10-109">No menu suspenso **Personalizar e controlar devtools** , na seção do lado do **encaixe** , selecione **encaixar à direita**.</span><span class="sxs-lookup"><span data-stu-id="40d10-109">On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, select **Dock to right**.</span></span>  
    
## <span data-ttu-id="40d10-110">Exibir o CSS de um elemento</span><span class="sxs-lookup"><span data-stu-id="40d10-110">View the CSS for an element</span></span>  

1.  <span data-ttu-id="40d10-111">[Exemplos de CSS abertos](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="40d10-111">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="40d10-112">Passe o cursor do mouse sobre o `Inspect Me!` texto, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="40d10-112">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="40d10-113">No DevTools, no painel **elementos** , na guia **árvore DOM** , o `Inspect Me!` elemento é realçado.</span><span class="sxs-lookup"><span data-stu-id="40d10-113">In DevTools, on the **Elements** panel, in the **DOM Tree** tab, the `Inspect Me!` element is highlighted.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="O elemento inspecionado é realçado na árvore DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           <span data-ttu-id="40d10-115">Figura 1: o elemento inspecionado é realçado na **árvore DOM**</span><span class="sxs-lookup"><span data-stu-id="40d10-115">Figure 1:  The inspected element is highlighted in the **DOM Tree**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="40d10-116">No `Inspect Me!` elemento, localize o valor do `data-message` atributo e copie-o.</span><span class="sxs-lookup"><span data-stu-id="40d10-116">In the `Inspect Me!` element, find the value of the `data-message` attribute and copy it.</span></span>  
1.  <span data-ttu-id="40d10-117">Na página, no **valor de `data-message` :** TextBox, insira o valor.</span><span class="sxs-lookup"><span data-stu-id="40d10-117">On the page, in the **Value of `data-message`:** textbox, enter the value.</span></span>  
1.  <span data-ttu-id="40d10-118">Passe o cursor do mouse sobre o `Inspect Me!` texto, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="40d10-118">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="40d10-119">No DevTools, no painel **elementos** , selecione a guia **estilos** .</span><span class="sxs-lookup"><span data-stu-id="40d10-119">In DevTools, on the **Elements** panel, select the **Styles** tab.</span></span>  
    1.  <span data-ttu-id="40d10-120">Na guia **estilos** , o `Inspect Me!` elemento é realçado.</span><span class="sxs-lookup"><span data-stu-id="40d10-120">In the **Styles** tab, the `Inspect Me!` element is highlighted.</span></span>  
    1.  <span data-ttu-id="40d10-121">No `Inspect Me!` elemento, localize a `aloha` regra de classe.</span><span class="sxs-lookup"><span data-stu-id="40d10-121">In the `Inspect Me!` element, find the `aloha` class rule.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="40d10-122">Você vê esta regra porque ela está sendo aplicada ao `Inspect Me!` elemento.</span><span class="sxs-lookup"><span data-stu-id="40d10-122">You see this rule because it is being applied to the `Inspect Me!` element.</span></span>  
        
    1.  <span data-ttu-id="40d10-123">Na `aloha` classe, localize o valor para o `padding` estilo e copie-o.</span><span class="sxs-lookup"><span data-stu-id="40d10-123">In the `aloha` class, find the value for the `padding` style and copy it.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="As classes CSS aplicadas ao elemento inspecionado são realçadas na guia estilos" lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           <span data-ttu-id="40d10-125">Figura 2: as classes CSS aplicadas ao elemento selecionado, como, por exemplo `aloha` , são exibidas na guia **estilos**</span><span class="sxs-lookup"><span data-stu-id="40d10-125">Figure 2:  CSS classes being applied to the selected element, such as `aloha`, are displayed in the **Styles** tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="40d10-126">Na página, no **valor de `padding` :** TextBox, insira o valor.</span><span class="sxs-lookup"><span data-stu-id="40d10-126">On the page, in the **Value of `padding`:** textbox, enter the value.</span></span>  

## <span data-ttu-id="40d10-127">Adicionar uma declaração CSS a um elemento</span><span class="sxs-lookup"><span data-stu-id="40d10-127">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="40d10-128">Use a guia **estilos** quando desejar alterar ou adicionar declarações CSS a um elemento.</span><span class="sxs-lookup"><span data-stu-id="40d10-128">Use the **Styles** tab when you want to change or add CSS declarations to an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="40d10-129">Conclua a [exibição do CSS para um](#view-the-css-for-an-element) tutorial de elemento antes de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="40d10-129">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="40d10-130">[Exemplos de CSS abertos](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="40d10-130">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="40d10-131">Passe o cursor do mouse sobre o `Add A Background Color To Me!` texto, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="40d10-131">Hover on the `Add A Background Color To Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="40d10-132">Selecione `element.style` próximo à parte superior da guia **estilos** .</span><span class="sxs-lookup"><span data-stu-id="40d10-132">Select `element.style` near the top of the **Styles** tab.</span></span>  
1.  <span data-ttu-id="40d10-133">Digite `background-color` e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="40d10-133">Type `background-color` and press `Enter`.</span></span>  
1.  <span data-ttu-id="40d10-134">Digite `honeydew` e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="40d10-134">Type `honeydew` and press `Enter`.</span></span>  <span data-ttu-id="40d10-135">Na **árvore DOM** , você verá que uma declaração de estilo embutido foi aplicada ao elemento.</span><span class="sxs-lookup"><span data-stu-id="40d10-135">In the **DOM Tree** you should see that an inline style declaration was applied to the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Adicionando uma declaração CSS ao elemento usando a guia estilos" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       <span data-ttu-id="40d10-137">Figura 3: a `background-color:honeydew` declaração foi aplicada ao elemento usando a `element.style` seção da guia **estilos**</span><span class="sxs-lookup"><span data-stu-id="40d10-137">Figure 3:  The `background-color:honeydew` declaration has been applied to the element using the `element.style` section of the **Styles** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="40d10-138">Adicionar uma classe CSS a um elemento</span><span class="sxs-lookup"><span data-stu-id="40d10-138">Add a CSS class to an element</span></span>  

<span data-ttu-id="40d10-139">Use a guia **estilos** para ver como um elemento se parece quando uma classe CSS é aplicada a ou removida de um elemento.</span><span class="sxs-lookup"><span data-stu-id="40d10-139">Use the **Styles** tab to see how an element looks when a CSS class is applied to or removed from an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="40d10-140">Conclua a [exibição do CSS para um](#view-the-css-for-an-element) tutorial de elemento antes de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="40d10-140">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="40d10-141">[Exemplos de CSS abertos](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="40d10-141">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="40d10-142">Passe o cursor do mouse sobre o `Add A Class To Me!` texto, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="40d10-142">Hover on the `Add A Class To Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="40d10-143">Select **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="40d10-143">Select **.cls**.</span></span>  <span data-ttu-id="40d10-144">DevTools revela uma caixa de texto onde você pode adicionar classes ao elemento selecionado.</span><span class="sxs-lookup"><span data-stu-id="40d10-144">DevTools reveals a text box where you may add classes to the selected element.</span></span>  
1.  <span data-ttu-id="40d10-145">Digite `color_me` na caixa de texto **Adicionar nova classe** e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="40d10-145">Type `color_me` in the **Add new class** text box and then press `Enter`.</span></span>  <span data-ttu-id="40d10-146">Uma caixa de seleção é exibida abaixo da caixa de texto **Adicionar nova classe** , em que você pode ativar e desativar a classe.</span><span class="sxs-lookup"><span data-stu-id="40d10-146">A checkbox appears below the **Add new class** text box, where you may toggle the class on and off.</span></span>  <span data-ttu-id="40d10-147">Se o `Add A Class To Me!` elemento tiver outras classes aplicadas a ele, você também poderá alternar entre eles.</span><span class="sxs-lookup"><span data-stu-id="40d10-147">If the `Add A Class To Me!` element has any other classes applied to it, you are also able to toggle each from here.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Aplicando a classe color_me ao elemento" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       <span data-ttu-id="40d10-149">Figura 4: a `color_me` classe foi aplicada ao elemento usando a seção **. CLS** da guia **estilos**</span><span class="sxs-lookup"><span data-stu-id="40d10-149">Figure 4:  The `color_me` class has been applied to the element using the **.cls** section of the **Styles** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="40d10-150">Adicionar um PseudoState a uma classe</span><span class="sxs-lookup"><span data-stu-id="40d10-150">Add a pseudostate to a class</span></span>  

<span data-ttu-id="40d10-151">Use a guia **estilos** para aplicar permanentemente um PseudoState CSS a um elemento.</span><span class="sxs-lookup"><span data-stu-id="40d10-151">Use the **Styles** tab to permanently apply a CSS pseudostate to an element.</span></span>  <span data-ttu-id="40d10-152">DevTools dá suporte a `:active` ,, `:focus` `:hover` e `:visited` .</span><span class="sxs-lookup"><span data-stu-id="40d10-152">DevTools supports `:active`, `:focus`, `:hover`, and `:visited`.</span></span>  

> [!NOTE]
> <span data-ttu-id="40d10-153">Conclua a [exibição do CSS para um](#view-the-css-for-an-element) tutorial de elemento antes de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="40d10-153">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="40d10-154">[Exemplos de CSS abertos](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="40d10-154">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="40d10-155">Passe o mouse sobre o `Hover Over Me!` texto.</span><span class="sxs-lookup"><span data-stu-id="40d10-155">Hover over the `Hover Over Me!` text.</span></span>  <span data-ttu-id="40d10-156">A cor do plano de fundo muda.</span><span class="sxs-lookup"><span data-stu-id="40d10-156">The background color changes.</span></span>  
1.  <span data-ttu-id="40d10-157">Passe o cursor do mouse sobre o `Hover Over Me!` texto, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="40d10-157">Hover on the `Hover Over Me!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="40d10-158">Na guia **estilos** , selecione **: Hov**.</span><span class="sxs-lookup"><span data-stu-id="40d10-158">In the **Styles** tab, select **:hov**.</span></span>  
1.  <span data-ttu-id="40d10-159">Marque a caixa de seleção **: hover** .</span><span class="sxs-lookup"><span data-stu-id="40d10-159">Check the **:hover** checkbox.</span></span>  <span data-ttu-id="40d10-160">A cor do plano de fundo muda como antes, mesmo que você não esteja efetivamente passando o mouse sobre o elemento.</span><span class="sxs-lookup"><span data-stu-id="40d10-160">The background color changes like before, even though you are not actually hovering over the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Alternando o PseudoState de foco em um elemento" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       <span data-ttu-id="40d10-162">Figura 5: alternando o `:hover` pseudo-estado em um elemento</span><span class="sxs-lookup"><span data-stu-id="40d10-162">Figure 5:  Toggling the `:hover` pseudostate on an element</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="40d10-163">Alterar as dimensões de um elemento</span><span class="sxs-lookup"><span data-stu-id="40d10-163">Change the dimensions of an element</span></span>  

<span data-ttu-id="40d10-164">Use o diagrama interativo do **modelo de caixa** na guia **estilos** para alterar a largura, a altura, o enchimento, a margem ou o comprimento da borda de um elemento.</span><span class="sxs-lookup"><span data-stu-id="40d10-164">Use the **Box Model** interactive diagram in the **Styles** tab to change the width, height, padding, margin, or border length of an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="40d10-165">Conclua a [exibição do CSS para um](#view-the-css-for-an-element) tutorial de elemento antes de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="40d10-165">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="40d10-166">[Exemplos de CSS abertos](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="40d10-166">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="40d10-167">Passe o cursor do mouse sobre o `Change My Margin!` texto, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="40d10-167">Hover on the `Change My Margin!` text, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
1.  <span data-ttu-id="40d10-168">No diagrama de **modelo de caixa** na guia **estilos** , passe o mouse sobre o **preenchimento**.</span><span class="sxs-lookup"><span data-stu-id="40d10-168">In the **Box Model** diagram in the **Styles** tab, hover over **padding**.</span></span>  <span data-ttu-id="40d10-169">O preenchimento de um elemento é realçado no visor.</span><span class="sxs-lookup"><span data-stu-id="40d10-169">The padding of an element is highlighted in the viewport.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="40d10-170">Dependendo do tamanho da janela do DevTools, talvez seja necessário rolar até a parte inferior da guia **estilos** para ver o **modelo de caixa**.</span><span class="sxs-lookup"><span data-stu-id="40d10-170">Depending on the size of your DevTools window, you may need to scroll to the bottom of the **Styles** tab to see the **Box Model**.</span></span>  

1.  <span data-ttu-id="40d10-171">Clique duas vezes na margem esquerda no **modelo de caixa**, que atualmente tem um valor `-` que indica que o elemento não tem uma margem esquerda.</span><span class="sxs-lookup"><span data-stu-id="40d10-171">Double-click the left margin in the **Box Model**, which currently has a value of `-` meaning that the element does not have a left-margin.</span></span>  
1.  <span data-ttu-id="40d10-172">Digite `100px` e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="40d10-172">Type `100px` and press `Enter`.</span></span>  <span data-ttu-id="40d10-173">O **modelo de caixa** tem como padrão pixels, mas também aceita outros valores, como `25%` ou `10vw` .</span><span class="sxs-lookup"><span data-stu-id="40d10-173">The **Box Model** defaults to pixels, but it also accepts other values, such as `25%`, or `10vw`.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Passando o cursor sobre o preenchimento do elemento" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             <span data-ttu-id="40d10-175">Figura 6: passando o cursor sobre o preenchimento do elemento</span><span class="sxs-lookup"><span data-stu-id="40d10-175">Figure 6:  Hovering over the padding of the element</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Alterar a margem esquerda do elemento" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             <span data-ttu-id="40d10-177">Figura 7: alterando a margem esquerda do elemento</span><span class="sxs-lookup"><span data-stu-id="40d10-177">Figure 7:  Changing the left-margin of the element</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="40d10-178">Depuração de consultas de mídia</span><span class="sxs-lookup"><span data-stu-id="40d10-178">Debugging Media Queries</span></span>  

<span data-ttu-id="40d10-179">As [consultas de mídia][MDNUsingMediaGueries] são uma maneira de fazer com que seu produto da Web reajam a alterações nas definições de configuração de cada usuário.</span><span class="sxs-lookup"><span data-stu-id="40d10-179">[Media Queries][MDNUsingMediaGueries] are a way to make your web product react to changes in the configuration settings for each user.</span></span>  <span data-ttu-id="40d10-180">O caso de uso mais significativo é fornecer ao seu produto um layout CSS diferente, dependendo das dimensões do visor.</span><span class="sxs-lookup"><span data-stu-id="40d10-180">The most significant use case is to provide your product a different CSS layout depending on the dimensions of the viewport.</span></span>  <span data-ttu-id="40d10-181">O uso de layouts separados permite um layout de uma coluna para dispositivos móveis e layouts de várias colunas quando há mais bens de tela disponíveis.</span><span class="sxs-lookup"><span data-stu-id="40d10-181">Using separate layouts allows for a one-column layout for mobile devices and multi-column layouts when there is more screen estate available.</span></span>  

<span data-ttu-id="40d10-182">Se você quiser depurar ou testar as consultas de mídia definidas em seu CSS, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="40d10-182">If you want to debug or test the Media Queries you defined in your CSS, use the following steps.</span></span>  

1.  <span data-ttu-id="40d10-183">Abra as ferramentas de desenvolvedor e selecione o ícone de **Ativar/desativar a barra de ferramentas do dispositivo** em segundo lugar no canto superior esquerdo ou pressione `Ctrl` + `Shift` + `M` \ ( `Cmd` + `Shift` + `M` no MacOS \).</span><span class="sxs-lookup"><span data-stu-id="40d10-183">Open the developer tools and select the **Toggle device toolbar** icon second on the top-left, or press `Ctrl`+`Shift`+`M` \(`Cmd`+`Shift`+`M` on macOS\).</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Abrir a barra de ferramentas do dispositivo" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       <span data-ttu-id="40d10-185">Figura 8: abrindo a barra de ferramentas do dispositivo</span><span class="sxs-lookup"><span data-stu-id="40d10-185">Figure 8:  Opening the device toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="40d10-186">Com a barra de ferramentas do dispositivo aberta, selecione o `...` menu no canto superior direito e selecione **Exibir consultas de mídia**.</span><span class="sxs-lookup"><span data-stu-id="40d10-186">With the device toolbar open, select the `...` menu on the top-right and select **View Media Queries**.</span></span>  <span data-ttu-id="40d10-187">Você deve ver barras coloridas acima da exibição da página que representa as diferentes consultas de mídia.</span><span class="sxs-lookup"><span data-stu-id="40d10-187">You should see colored bars above the display of the page that represent the different media queries.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Mostrando consultas de mídia na barra de ferramentas do dispositivo" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       <span data-ttu-id="40d10-189">Figura 9: mostrando consultas de mídia na barra de ferramentas do dispositivo</span><span class="sxs-lookup"><span data-stu-id="40d10-189">Figure 9:  Showing Media Queries in Device Toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="40d10-190">Passe o mouse sobre os limites nas barras para ver os valores das diferentes consultas de mídia.</span><span class="sxs-lookup"><span data-stu-id="40d10-190">Hover over the boundaries in the bars to see the values of the different media queries.</span></span> <span data-ttu-id="40d10-191">Selecione cada um para redimensionar a página da Web para corresponder.</span><span class="sxs-lookup"><span data-stu-id="40d10-191">Select each to resize the web page to match.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Selecionando consulta de mídia na barra de visualização" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       <span data-ttu-id="40d10-193">Figura 10: selecionando consulta de mídia na barra de visualização</span><span class="sxs-lookup"><span data-stu-id="40d10-193">Figure 10:  Selecting Media Query from preview bar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="40d10-194">Para depurar consultas de mídia e abrir o arquivo CSS no `Sources` editor; passe o mouse sobre qualquer um dos segmentos de barras, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione `reveal in source code` .</span><span class="sxs-lookup"><span data-stu-id="40d10-194">To debug media queries and open the CSS file in the `Sources` editor; hover on any of the bar segments, open the contextual menu \(right-click\), and select `reveal in source code`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Revelando consultas de mídia no editor de fontes" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       <span data-ttu-id="40d10-196">Figura 11: revelando consultas de mídia no editor de fontes</span><span class="sxs-lookup"><span data-stu-id="40d10-196">Figure 11:  Revealing Media Queries in Sources Editor</span></span>  
    :::image-end:::  
    
<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Alterar o posicionamento do Microsoft Edge DevTools (desencaixar, encaixar na parte inferior, encaixar à esquerda)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Exemplos de CSS-Microsoft Edge (Chromium) DevTools | Problema"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Usando consultas de mídia | MDN"  

> [!NOTE]
> <span data-ttu-id="40d10-200">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="40d10-200">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="40d10-201">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/css/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="40d10-201">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="40d10-203">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="40d10-203">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
