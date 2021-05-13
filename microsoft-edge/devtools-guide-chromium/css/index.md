---
description: Saiba como usar Microsoft Edge DevTools para exibir e alterar o CSS de uma página.
title: Introdução à exibição e alteração do CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: bc629286530e709bef0e04a671f1a0e56eee48ea
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564445"
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
# <a name="get-started-with-viewing-and-changing-css"></a><span data-ttu-id="63b0e-104">Introdução à exibição e alteração do CSS</span><span class="sxs-lookup"><span data-stu-id="63b0e-104">Get started with viewing and changing CSS</span></span>  

<span data-ttu-id="63b0e-105">Conclua estes tutoriais interativos para aprender os conceitos básicos de exibição e alteração do CSS para uma página usando Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="63b0e-105">Complete these interactive tutorials to learn the basics of viewing and changing the CSS for a page using Microsoft Edge DevTools.</span></span>  

## <a name="open-css-examples"></a><span data-ttu-id="63b0e-106">Exemplos de CSS abertos</span><span class="sxs-lookup"><span data-stu-id="63b0e-106">Open CSS Examples</span></span>  

1.  <span data-ttu-id="63b0e-107">Segure `Control` \(Windows, Linux\) ou `Command` \(macOS\) e escolha **Exemplos CSS** para abrir em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="63b0e-107">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **CSS Examples** to open in a new window.</span></span>  
    
    [<span data-ttu-id="63b0e-108">Exemplos CSS</span><span class="sxs-lookup"><span data-stu-id="63b0e-108">CSS Examples</span></span>][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > <span data-ttu-id="63b0e-109">Se você quiser encaixar sua janela [DevTools][DevToolsCustomizePlacement] à direita do visor \(exibido na figura a seguir\), escolha Personalizar e controlar **DevTools** `...` .</span><span class="sxs-lookup"><span data-stu-id="63b0e-109">If you want to [dock your DevTools window][DevToolsCustomizePlacement] to the right of your viewport \(displayed in the following figure\), choose **Customize and control DevTools** `...`.</span></span>  <span data-ttu-id="63b0e-110">No menu **suspenso Personalizar e controlar DevTools,** na seção Lado **do** Encaixe, escolha **Doca para a direita**.</span><span class="sxs-lookup"><span data-stu-id="63b0e-110">On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, choose **Dock to right**.</span></span>  
    
## <a name="view-the-css-for-an-element"></a><span data-ttu-id="63b0e-111">Exibir o CSS para um elemento</span><span class="sxs-lookup"><span data-stu-id="63b0e-111">View the CSS for an element</span></span>  

1.  <span data-ttu-id="63b0e-112">[Abra exemplos css](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="63b0e-112">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="63b0e-113">Passe o mouse `Inspect Me!` no texto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="63b0e-113">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="63b0e-114">No DevTools, na **ferramenta Elementos,** no painel **Árvore DOM,** o `Inspect Me!` elemento é realçado.</span><span class="sxs-lookup"><span data-stu-id="63b0e-114">In DevTools, on the **Elements** tool, in the **DOM Tree** panel, the `Inspect Me!` element is highlighted.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="O elemento inspecionado é realçado na árvore DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           <span data-ttu-id="63b0e-116">O elemento inspecionado é realçado na árvore **DOM**</span><span class="sxs-lookup"><span data-stu-id="63b0e-116">The inspected element is highlighted in the **DOM Tree**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="63b0e-117">No `Inspect Me!` elemento, encontre o valor do `data-message` atributo e copie-o.</span><span class="sxs-lookup"><span data-stu-id="63b0e-117">In the `Inspect Me!` element, find the value of the `data-message` attribute and copy it.</span></span>  
1.  <span data-ttu-id="63b0e-118">Na página, na caixa **de texto Valor de `data-message` :** , insira o valor.</span><span class="sxs-lookup"><span data-stu-id="63b0e-118">On the page, in the **Value of `data-message`:** textbox, enter the value.</span></span>  
1.  <span data-ttu-id="63b0e-119">Passe o mouse `Inspect Me!` no texto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="63b0e-119">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="63b0e-120">No DevTools, na ferramenta **Elementos,** selecione o **painel Estilos.**</span><span class="sxs-lookup"><span data-stu-id="63b0e-120">In DevTools, on the **Elements** tool, select the **Styles** panel.</span></span>  
    1.  <span data-ttu-id="63b0e-121">No painel **Estilos,** o `Inspect Me!` elemento é realçado.</span><span class="sxs-lookup"><span data-stu-id="63b0e-121">In the **Styles** panel, the `Inspect Me!` element is highlighted.</span></span>  
    1.  <span data-ttu-id="63b0e-122">No `Inspect Me!` elemento, encontre a `aloha` regra de classe.</span><span class="sxs-lookup"><span data-stu-id="63b0e-122">In the `Inspect Me!` element, find the `aloha` class rule.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="63b0e-123">Essa regra é exibida porque está sendo aplicada ao `Inspect Me!` elemento.</span><span class="sxs-lookup"><span data-stu-id="63b0e-123">This rule is displayed, because it is being applied to the `Inspect Me!` element.</span></span>  
        
    1.  <span data-ttu-id="63b0e-124">Na `aloha` classe, encontre o valor do `padding` estilo e copie-o.</span><span class="sxs-lookup"><span data-stu-id="63b0e-124">In the `aloha` class, find the value for the `padding` style and copy it.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Classes CSS são aplicadas ao elemento inspecionado são realçadas no painel Estilos" lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           <span data-ttu-id="63b0e-126">Classes CSS são aplicadas ao elemento selecionado, como `aloha` , são exibidas no painel **Estilos**</span><span class="sxs-lookup"><span data-stu-id="63b0e-126">CSS classes is applied to the selected element, such as `aloha`, are displayed in the **Styles** panel</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="63b0e-127">Na página, na caixa **de texto Valor de `padding` :** , insira o valor.</span><span class="sxs-lookup"><span data-stu-id="63b0e-127">On the page, in the **Value of `padding`:** textbox, enter the value.</span></span>  

## <a name="add-a-css-declaration-to-an-element"></a><span data-ttu-id="63b0e-128">Adicionar uma declaração CSS a um elemento</span><span class="sxs-lookup"><span data-stu-id="63b0e-128">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="63b0e-129">Use o **painel Estilos** quando quiser alterar ou adicionar declarações CSS a um elemento.</span><span class="sxs-lookup"><span data-stu-id="63b0e-129">Use the **Styles** panel when you want to change or add CSS declarations to an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="63b0e-130">Conclua [o tutorial Exibir o CSS para um](#view-the-css-for-an-element) elemento antes de fazer este.</span><span class="sxs-lookup"><span data-stu-id="63b0e-130">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="63b0e-131">[Abra exemplos css](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="63b0e-131">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="63b0e-132">Passe o mouse `Add A Background Color To Me!` no texto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="63b0e-132">Hover on the `Add A Background Color To Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="63b0e-133">Escolha `element.style` perto da parte superior do painel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="63b0e-133">Choose `element.style` near the top of the **Styles** panel.</span></span>  
1.  <span data-ttu-id="63b0e-134">Digite `background-color` e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="63b0e-134">Type `background-color` and select `Enter`.</span></span>  
1.  <span data-ttu-id="63b0e-135">Digite `honeydew` e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="63b0e-135">Type `honeydew` and select `Enter`.</span></span>  <span data-ttu-id="63b0e-136">Na Árvore **DOM,** uma declaração de estilo em linha aplicada ao elemento é exibida.</span><span class="sxs-lookup"><span data-stu-id="63b0e-136">In the **DOM Tree**, an inline style declaration applied to the element is displayed.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Adicionar uma declaração CSS ao elemento usando o painel Estilos" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       <span data-ttu-id="63b0e-138">A `background-color:honeydew` declaração é aplicada ao elemento usando a seção do painel `element.style` **Estilos**</span><span class="sxs-lookup"><span data-stu-id="63b0e-138">The `background-color:honeydew` declaration is applied to the element using the `element.style` section of the **Styles** panel</span></span>  
    :::image-end:::  
    
## <a name="add-a-css-class-to-an-element"></a><span data-ttu-id="63b0e-139">Adicionar uma classe CSS a um elemento</span><span class="sxs-lookup"><span data-stu-id="63b0e-139">Add a CSS class to an element</span></span>  

<span data-ttu-id="63b0e-140">Para exibir a aparência de um elemento quando uma classe CSS é aplicada ou removida de um elemento, navegue até o **painel Estilos.**</span><span class="sxs-lookup"><span data-stu-id="63b0e-140">To display how an element looks when a CSS class is applied to or removed from an element, navigate to the **Styles** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="63b0e-141">Conclua [o tutorial Exibir o CSS para um](#view-the-css-for-an-element) elemento antes de fazer este.</span><span class="sxs-lookup"><span data-stu-id="63b0e-141">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="63b0e-142">[Abra exemplos css](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="63b0e-142">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="63b0e-143">Passe o mouse `Add A Class To Me!` no texto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="63b0e-143">Hover on the `Add A Class To Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="63b0e-144">Escolha **.cls**.</span><span class="sxs-lookup"><span data-stu-id="63b0e-144">Choose **.cls**.</span></span>  <span data-ttu-id="63b0e-145">DevTools revela uma caixa de texto onde você pode adicionar classes ao elemento selecionado.</span><span class="sxs-lookup"><span data-stu-id="63b0e-145">DevTools reveals a text box where you may add classes to the selected element.</span></span>  
1.  <span data-ttu-id="63b0e-146">Digite `color_me` a caixa de texto Adicionar **nova** classe e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="63b0e-146">Type `color_me` in the **Add new class** text box and then select `Enter`.</span></span>  <span data-ttu-id="63b0e-147">Uma caixa de seleção é exibida abaixo da caixa de texto **Adicionar nova** classe, onde você pode alternar a classe para cima e para baixo.</span><span class="sxs-lookup"><span data-stu-id="63b0e-147">A checkbox appears below the **Add new class** text box, where you may toggle the class on and off.</span></span>  <span data-ttu-id="63b0e-148">Se o elemento tiver outras classes aplicadas a ele, você também poderá `Add A Class To Me!` alternar cada uma delas daqui.</span><span class="sxs-lookup"><span data-stu-id="63b0e-148">If the `Add A Class To Me!` element has any other classes applied to it, you are also able to toggle each from here.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Aplicar a color_me ao elemento" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       <span data-ttu-id="63b0e-150">A `color_me` classe é aplicada ao elemento usando a seção **.cls** do painel **Estilos**</span><span class="sxs-lookup"><span data-stu-id="63b0e-150">The `color_me` class is applied to the element using the **.cls** section of the **Styles** panel</span></span>  
    :::image-end:::  
    
## <a name="add-a-pseudostate-to-a-class"></a><span data-ttu-id="63b0e-151">Adicionar um pseudostate a uma classe</span><span class="sxs-lookup"><span data-stu-id="63b0e-151">Add a pseudostate to a class</span></span>  

<span data-ttu-id="63b0e-152">Use o **painel Estilos** para aplicar permanentemente um pseudostate CSS a um elemento.</span><span class="sxs-lookup"><span data-stu-id="63b0e-152">Use the **Styles** panel to permanently apply a CSS pseudostate to an element.</span></span>  <span data-ttu-id="63b0e-153">O DevTools dá `:active` suporte a , e `:focus` `:hover` `:visited` .</span><span class="sxs-lookup"><span data-stu-id="63b0e-153">DevTools supports `:active`, `:focus`, `:hover`, and `:visited`.</span></span>  

> [!NOTE]
> <span data-ttu-id="63b0e-154">Conclua [o tutorial Exibir o CSS para um](#view-the-css-for-an-element) elemento antes de fazer este.</span><span class="sxs-lookup"><span data-stu-id="63b0e-154">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="63b0e-155">[Abra exemplos css](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="63b0e-155">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="63b0e-156">Passe o mouse no `Hover Over Me!` texto.</span><span class="sxs-lookup"><span data-stu-id="63b0e-156">Hover on the `Hover Over Me!` text.</span></span>  <span data-ttu-id="63b0e-157">A cor do plano de fundo muda.</span><span class="sxs-lookup"><span data-stu-id="63b0e-157">The background color changes.</span></span>  
1.  <span data-ttu-id="63b0e-158">Passe o mouse `Hover Over Me!` no texto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="63b0e-158">Hover on the `Hover Over Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="63b0e-159">No painel **Estilos,** escolha **:hov**.</span><span class="sxs-lookup"><span data-stu-id="63b0e-159">In the **Styles** panel, choose **:hov**.</span></span>  
1.  <span data-ttu-id="63b0e-160">Marque a **caixa de seleção :hover.**</span><span class="sxs-lookup"><span data-stu-id="63b0e-160">Check the **:hover** checkbox.</span></span>  <span data-ttu-id="63b0e-161">A cor do plano de fundo muda como antes, mesmo que você não está realmente pairando sobre o elemento.</span><span class="sxs-lookup"><span data-stu-id="63b0e-161">The background color changes like before, even though you are not actually hovering over the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Alternar o pseudostate de foco em um elemento" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       <span data-ttu-id="63b0e-163">Alternar o `:hover` pseudostate em um elemento</span><span class="sxs-lookup"><span data-stu-id="63b0e-163">Toggle the `:hover` pseudostate on an element</span></span>  
    :::image-end:::  
    
## <a name="change-the-dimensions-of-an-element"></a><span data-ttu-id="63b0e-164">Alterar as dimensões de um elemento</span><span class="sxs-lookup"><span data-stu-id="63b0e-164">Change the dimensions of an element</span></span>  

<span data-ttu-id="63b0e-165">Use o **diagrama interativo Modelo** de Caixa no painel **Estilos** para alterar a largura, altura, preenchimento, margem ou comprimento da borda de um elemento.</span><span class="sxs-lookup"><span data-stu-id="63b0e-165">Use the **Box Model** interactive diagram in the **Styles** panel to change the width, height, padding, margin, or border length of an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="63b0e-166">Conclua [o tutorial Exibir o CSS para um](#view-the-css-for-an-element) elemento antes de fazer este.</span><span class="sxs-lookup"><span data-stu-id="63b0e-166">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="63b0e-167">[Abra exemplos css](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="63b0e-167">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="63b0e-168">Passe o mouse `Change My Margin!` no texto, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="63b0e-168">Hover on the `Change My Margin!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="63b0e-169">No diagrama **Modelo de** Caixa no painel **Estilos,** passe o mouse sobre **preenchimento**.</span><span class="sxs-lookup"><span data-stu-id="63b0e-169">In the **Box Model** diagram in the **Styles** panel, hover on **padding**.</span></span>  <span data-ttu-id="63b0e-170">O preenchimento de um elemento é realçado no viewport.</span><span class="sxs-lookup"><span data-stu-id="63b0e-170">The padding of an element is highlighted in the viewport.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="63b0e-171">Dependendo do tamanho da janela DevTools, talvez seja necessário rolar até a parte inferior do painel **Estilos** para exibir **o Modelo de Caixa**.</span><span class="sxs-lookup"><span data-stu-id="63b0e-171">Depending on the size of your DevTools window, you may need to scroll to the bottom of the **Styles** panel to display the **Box Model**.</span></span>  

1.  <span data-ttu-id="63b0e-172">Clique duas vezes na margem esquerda no **Modelo**de Caixa , que atualmente tem um valor de significado de que o elemento não `-` tem uma margem esquerda.</span><span class="sxs-lookup"><span data-stu-id="63b0e-172">Double-click the left margin in the **Box Model**, which currently has a value of `-` meaning that the element does not have a left-margin.</span></span>  
1.  <span data-ttu-id="63b0e-173">Digite `100px` e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="63b0e-173">Type `100px` and select `Enter`.</span></span>  <span data-ttu-id="63b0e-174">O **Modelo de Caixa** é padrão para pixels, mas também aceita outros valores, como , ou `25%` `10vw` .</span><span class="sxs-lookup"><span data-stu-id="63b0e-174">The **Box Model** defaults to pixels, but it also accepts other values, such as `25%`, or `10vw`.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Passe o mouse no preenchimento do elemento" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             <span data-ttu-id="63b0e-176">Passe o mouse no preenchimento do elemento</span><span class="sxs-lookup"><span data-stu-id="63b0e-176">Hover on the padding of the element</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Alterar a margem esquerda do elemento" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             <span data-ttu-id="63b0e-178">Alterar a margem esquerda do elemento</span><span class="sxs-lookup"><span data-stu-id="63b0e-178">Change the left-margin of the element</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="debugging-media-queries"></a><span data-ttu-id="63b0e-179">Depuração de consultas de mídia</span><span class="sxs-lookup"><span data-stu-id="63b0e-179">Debugging Media Queries</span></span>  

<span data-ttu-id="63b0e-180">[Consultas de mídia][MDNUsingMediaGueries] são uma maneira de fazer com que seu produto Web reaja às alterações nas configurações de cada usuário.</span><span class="sxs-lookup"><span data-stu-id="63b0e-180">[Media Queries][MDNUsingMediaGueries] are a way to make your web product react to changes in the configuration settings for each user.</span></span>  <span data-ttu-id="63b0e-181">O caso de uso mais significativo é fornecer ao seu produto um layout CSS diferente, dependendo das dimensões do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="63b0e-181">The most significant use case is to provide your product a different CSS layout depending on the dimensions of the viewport.</span></span>  <span data-ttu-id="63b0e-182">O uso de layouts separados permite um layout de uma coluna para dispositivos móveis e layouts de várias colunas quando há mais propriedades de tela disponíveis.</span><span class="sxs-lookup"><span data-stu-id="63b0e-182">Using separate layouts allows for a one-column layout for mobile devices and multi-column layouts when there is more screen estate available.</span></span>  

<span data-ttu-id="63b0e-183">Se você quiser depurar ou testar as Consultas de Mídia definidas em seu CSS, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="63b0e-183">If you want to debug or test the Media Queries you defined in your CSS, use the following steps.</span></span>  

1.  <span data-ttu-id="63b0e-184">Abra as ferramentas do desenvolvedor e selecione o ícone da barra de ferramentas do dispositivo **De** alternar segundo na parte superior esquerda ou selecione `Ctrl` + `Shift` + `M` \( `Cmd` + `Shift` + `M` no macOS\).</span><span class="sxs-lookup"><span data-stu-id="63b0e-184">Open the developer tools and select the **Toggle device toolbar** icon second on the top-left, or select `Ctrl`+`Shift`+`M` \(`Cmd`+`Shift`+`M` on macOS\).</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Abra a barra de ferramentas do dispositivo" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       <span data-ttu-id="63b0e-186">Abra a barra de ferramentas do dispositivo</span><span class="sxs-lookup"><span data-stu-id="63b0e-186">Open the device toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="63b0e-187">Com a barra de ferramentas do dispositivo aberta, selecione o menu na `...` parte superior direita e escolha Exibir Consultas de **Mídia**.</span><span class="sxs-lookup"><span data-stu-id="63b0e-187">With the device toolbar open, select the `...` menu on the top-right and choose **View Media Queries**.</span></span>  <span data-ttu-id="63b0e-188">As barras coloridas exibidas acima da página da Web representam as diferentes consultas de mídia.</span><span class="sxs-lookup"><span data-stu-id="63b0e-188">The colored bars displayed above the webpage represent the different media queries.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Mostrar consultas de mídia na barra de ferramentas do dispositivo" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       <span data-ttu-id="63b0e-190">Mostrar consultas de mídia na barra de ferramentas do dispositivo</span><span class="sxs-lookup"><span data-stu-id="63b0e-190">Show Media Queries in Device Toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="63b0e-191">Passe o mouse nos limites nas barras para exibir os valores das diferentes consultas de mídia.</span><span class="sxs-lookup"><span data-stu-id="63b0e-191">Hover on the boundaries in the bars to display the values of the different media queries.</span></span>  <span data-ttu-id="63b0e-192">Escolha cada um para reorganizar a página da Web para corresponder.</span><span class="sxs-lookup"><span data-stu-id="63b0e-192">Choose each to resize the web page to match.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Escolha Consulta de Mídia na barra de visualização" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       <span data-ttu-id="63b0e-194">Escolha Consulta de Mídia na barra de visualização</span><span class="sxs-lookup"><span data-stu-id="63b0e-194">Choose Media Query from preview bar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="63b0e-195">Para depurar consultas de mídia e abrir o arquivo CSS no editor; passe o mouse em qualquer um dos segmentos de barra, abra o menu contextual \(clique com o botão direito `Sources` do mouse\) e selecione `reveal in source code` .</span><span class="sxs-lookup"><span data-stu-id="63b0e-195">To debug media queries and open the CSS file in the `Sources` editor; hover on any of the bar segments, open the contextual menu \(right-click\), and select `reveal in source code`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Revelar consultas de mídia no Editor de Fontes" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       <span data-ttu-id="63b0e-197">Revelar consultas de mídia no Editor de Fontes</span><span class="sxs-lookup"><span data-stu-id="63b0e-197">Reveal Media Queries in Sources Editor</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="63b0e-198">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="63b0e-198">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Alterar Microsoft Edge posicionamento do DevTools (Desfazer, Encaixar na Parte Inferior, Doca para a Esquerda)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Exemplos css - Microsoft Edge (Chromium) DevTools | Glitch"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Usando consultas de mídia | MDN"  

> [!NOTE]
> <span data-ttu-id="63b0e-202">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="63b0e-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="63b0e-203">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/css/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="63b0e-203">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="63b0e-205">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="63b0e-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
