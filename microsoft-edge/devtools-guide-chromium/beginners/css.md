---
description: Introdução css
title: 'DevTools para iniciantes: Começar com CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools
ms.openlocfilehash: 6f34cfa8610848505c8aa795c4fab16e5d2a98ed
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564641"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="devtools-for-beginners-get-started-with-css"></a><span data-ttu-id="1f852-104">DevTools para iniciantes: Começar com CSS</span><span class="sxs-lookup"><span data-stu-id="1f852-104">DevTools for beginners: Get started with CSS</span></span>  

<span data-ttu-id="1f852-105">Neste tutorial, você aprenderá a usar CSS para estilo de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="1f852-105">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="1f852-106">Você também aprenderá a usar o Microsoft Edge DevTools para experimentar alterações CSS.</span><span class="sxs-lookup"><span data-stu-id="1f852-106">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="1f852-107">O artigo a seguir é o segundo tutorial de uma série de tutoriais que ensina as noções básicas de desenvolvimento da Web e Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="1f852-107">The following article is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="1f852-108">Você ganha experiência prática criando seu próprio site.</span><span class="sxs-lookup"><span data-stu-id="1f852-108">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="1f852-109">Não é preciso concluir o primeiro tutorial antes de seguir o segundo.</span><span class="sxs-lookup"><span data-stu-id="1f852-109">You do not have to complete the first tutorial before following the second.</span></span>  <span data-ttu-id="1f852-110">[Configurar seu código](#set-up-your-code) mostra como configurar.</span><span class="sxs-lookup"><span data-stu-id="1f852-110">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="1f852-111">Este tutorial foi projetado para iniciantes absolutos e se concentra nos fundamentos do desenvolvimento da Web e noções **básicas** de como usar o DevTools para experimentar CSS.</span><span class="sxs-lookup"><span data-stu-id="1f852-111">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="1f852-112">Se você quiser um tutorial que se concentre apenas no DevTools, navegue até Introdução [exibindo e alterando CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="1f852-112">If you want a tutorial that only focuses on DevTools, navigate to [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="1f852-113">No início do tutorial, seu site deve ter a aparência da figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f852-113">At the beginning of the tutorial, your site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Qual é a aparência do seu site no momento" lightbox="../media/beginners-css-intro1.msft.png":::
   <span data-ttu-id="1f852-115">Qual é a aparência do seu site no momento</span><span class="sxs-lookup"><span data-stu-id="1f852-115">What your site currently looks like</span></span>  
:::image-end:::  

<span data-ttu-id="1f852-116">Depois de concluir o tutorial, o site deve ter a aparência da figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f852-116">After you complete the tutorial, you site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Como seu site deve ser no final do tutorial" lightbox="../media/beginners-css-intro2.msft.png":::
   <span data-ttu-id="1f852-118">Como seu site deve ser no final do tutorial</span><span class="sxs-lookup"><span data-stu-id="1f852-118">What your site should look like at the end of the tutorial</span></span>  
:::image-end:::  

## <a name="goals"></a><span data-ttu-id="1f852-119">Metas</span><span class="sxs-lookup"><span data-stu-id="1f852-119">Goals</span></span>  

<span data-ttu-id="1f852-120">Siga este tutorial para entender melhor os seguintes conceitos e tarefas.</span><span class="sxs-lookup"><span data-stu-id="1f852-120">Follow this tutorial to better understand the following concepts and tasks.</span></span>  

*   <span data-ttu-id="1f852-121">Como usar CSS para estilar uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="1f852-121">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="1f852-122">Como usar Microsoft Edge DevTools para experimentar CSS.</span><span class="sxs-lookup"><span data-stu-id="1f852-122">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="1f852-123">A diferença entre estruturas CSS e CSS.</span><span class="sxs-lookup"><span data-stu-id="1f852-123">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="1f852-124">Você está criando um site real.</span><span class="sxs-lookup"><span data-stu-id="1f852-124">You are building a real website.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="1f852-125">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="1f852-125">Prerequisites</span></span>  

<span data-ttu-id="1f852-126">Antes de tentar este tutorial, conclua os seguintes pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="1f852-126">Before attempting this tutorial, complete the following prerequisites.</span></span>  

*   <span data-ttu-id="1f852-127">Conclua [Introdução com HTML][DevtoolsBeginnersHtml] e o DOM ou certifique-se de que você tenha um entendimento sobre HTML e o DOM semelhantes ao que é ministrado nesse tutorial.</span><span class="sxs-lookup"><span data-stu-id="1f852-127">Complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what is taught in that tutorial.</span></span>  
*   <span data-ttu-id="1f852-128">Baixe o [Microsoft Edge][MicrosoftEdgeInsider] da Web.</span><span class="sxs-lookup"><span data-stu-id="1f852-128">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="1f852-129">O tutorial a seguir usa um conjunto de ferramentas de desenvolvimento da Web, chamada Microsoft Edge DevTools, que são criadas em Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1f852-129">The following tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <a name="set-up-your-code"></a><span data-ttu-id="1f852-130">Configurar seu código</span><span class="sxs-lookup"><span data-stu-id="1f852-130">Set up your code</span></span>  

<span data-ttu-id="1f852-131">Para criar seu site, você deve primeiro concluir as seguintes ações para configurar seu código.</span><span class="sxs-lookup"><span data-stu-id="1f852-131">To create your site, you must first complete the following actions to set up your code.</span></span>  

> [!NOTE]
> <span data-ttu-id="1f852-132">Se você já concluiu o primeiro tutorial da série, pule para a próxima seção.</span><span class="sxs-lookup"><span data-stu-id="1f852-132">If you have already completed the first tutorial in the series, skip to the next section.</span></span>  <span data-ttu-id="1f852-133">Continue usando seu código do último tutorial, Introdução [html e dom][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="1f852-133">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  

1.  <span data-ttu-id="1f852-134">Abra o [código-fonte][GlitchCookedAmphibianIndex].</span><span class="sxs-lookup"><span data-stu-id="1f852-134">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="1f852-135">A guia em foco do navegador é referenciada como a **guia de edição**.</span><span class="sxs-lookup"><span data-stu-id="1f852-135">The in-focus tab of your browser is referenced as the **editing tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="A guia edição" lightbox="../media/beginners-css-setup1.msft.png":::
       <span data-ttu-id="1f852-137">A **guia edição**</span><span class="sxs-lookup"><span data-stu-id="1f852-137">The **editing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-138">Escolha **cooked-amphibian**.</span><span class="sxs-lookup"><span data-stu-id="1f852-138">Choose **cooked-amphibian**.</span></span>  <span data-ttu-id="1f852-139">Um menu é aberto.</span><span class="sxs-lookup"><span data-stu-id="1f852-139">A menu pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="O menu Project opções" lightbox="../media/beginners-css-setup2.msft.png":::
       <span data-ttu-id="1f852-141">O menu Project opções</span><span class="sxs-lookup"><span data-stu-id="1f852-141">The Project Options menu</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="1f852-142">Escolha **Mesclar Project**.</span><span class="sxs-lookup"><span data-stu-id="1f852-142">Choose **Remix Project**.</span></span>  <span data-ttu-id="1f852-143">A falha cria uma cópia do projeto que você pode editar.</span><span class="sxs-lookup"><span data-stu-id="1f852-143">Glitch creates a copy of the project that you are able to edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="1f852-144">A falha gera um nome aleatório para o novo projeto.</span><span class="sxs-lookup"><span data-stu-id="1f852-144">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="1f852-145">Escolha **Mostrar** e escolher **Em uma nova janela**.</span><span class="sxs-lookup"><span data-stu-id="1f852-145">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="1f852-146">Outra guia é aberta com uma exibição ao vivo do seu site.</span><span class="sxs-lookup"><span data-stu-id="1f852-146">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="1f852-147">A guia em foco do navegador é referenciada como a **guia ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="1f852-147">The in-focus tab of your browser is referenced as the **live tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="A guia ao vivo" lightbox="../media/beginners-css-setup3.msft.png":::
       <span data-ttu-id="1f852-149">A **guia ao vivo**</span><span class="sxs-lookup"><span data-stu-id="1f852-149">The **live tab**</span></span>  
    :::image-end:::  

## <a name="understand-css"></a><span data-ttu-id="1f852-150">Entender CSS</span><span class="sxs-lookup"><span data-stu-id="1f852-150">Understand CSS</span></span>  

<span data-ttu-id="1f852-151">**CSS** é uma linguagem de computador que determina o layout e o estilo de páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="1f852-151">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="1f852-152">A figura a seguir é um parágrafo com uma borda.</span><span class="sxs-lookup"><span data-stu-id="1f852-152">The following figure is a paragraph with a border.</span></span>  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="O texto foi estilado com CSS" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   <span data-ttu-id="1f852-154">O texto foi estilado com CSS</span><span class="sxs-lookup"><span data-stu-id="1f852-154">The text has been styled with CSS</span></span>  
:::image-end:::  

<span data-ttu-id="1f852-155">O trecho de código a seguir é o código HTML e CSS usado para criar o parágrafo na figura anterior.</span><span class="sxs-lookup"><span data-stu-id="1f852-155">The following code snippet is the HTML and CSS code used to create the paragraph in the previous figure.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="1f852-156">provavelmente parece novo para você.</span><span class="sxs-lookup"><span data-stu-id="1f852-156">probably looks new to you.</span></span>  <span data-ttu-id="1f852-157">O restante deve parecer familiar.</span><span class="sxs-lookup"><span data-stu-id="1f852-157">The rest should look familiar.</span></span>  <span data-ttu-id="1f852-158">Caso não, [conclua Introdução html e o DOM][DevtoolsBeginnersHtml] antes de tentar as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f852-158">If not, complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] before attempting the following sections.</span></span>  

## <a name="add-inline-styles"></a><span data-ttu-id="1f852-159">Adicionar estilos em linha</span><span class="sxs-lookup"><span data-stu-id="1f852-159">Add inline styles</span></span>  

<span data-ttu-id="1f852-160">Conclua as seguintes ações para usar **estilos em linha** para aplicar estilos a um único elemento.</span><span class="sxs-lookup"><span data-stu-id="1f852-160">Complete the following actions to use **inline styles** to apply styles to a single element.</span></span>  

1.  <span data-ttu-id="1f852-161">Volte para a guia edição e abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="1f852-161">Go back to the editing tab and open `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       <span data-ttu-id="1f852-163">Abra `index.html` na guia edição</span><span class="sxs-lookup"><span data-stu-id="1f852-163">Open `index.html` in the editing tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-164">Adicione `style="background-color: aliceblue;"` ao `<nav>` seu .</span><span class="sxs-lookup"><span data-stu-id="1f852-164">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="1f852-165">No bloco de código abaixo, a quarta linha de código é a que você precisa alterar.</span><span class="sxs-lookup"><span data-stu-id="1f852-165">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="1f852-166">O restante está apenas lá, portanto, você pode garantir que você está colocando o novo código no lugar certo.</span><span class="sxs-lookup"><span data-stu-id="1f852-166">The rest is just there, so you are able to ensure that you are putting the new code in the right place.</span></span>  
    
    ```html
    <header>
        <p>Welcome to my site!</p>
    </header>
    <nav style="background-color: aliceblue;">
        <ul>
            <li><a href="/">Home</a></li>
            ...
        ...
    ...
    ```  
    
1.  <span data-ttu-id="1f852-167">Para exibir as alterações, navegue até a **guia ao vivo**.  O plano de fundo `<nav>` da seção agora está azul.</span><span class="sxs-lookup"><span data-stu-id="1f852-167">To display the changes, navigate to the **live tab**.  The background of the `<nav>` section is now blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="A cor do plano de fundo por trás dos links Home e Contact agora é azul" lightbox="../media/beginners-css-inline2.msft.png":::
       <span data-ttu-id="1f852-169">A cor do plano de fundo por trás dos links **Home** e **Contact** agora é azul</span><span class="sxs-lookup"><span data-stu-id="1f852-169">The background color behind the **Home** and **Contact** links is now blue</span></span>  
    :::image-end:::  
    
## <a name="re-use-styles-on-a-single-page-with-internal-stylesheets"></a><span data-ttu-id="1f852-170">Rea uso de estilos em uma única página com folhas de estilos internas</span><span class="sxs-lookup"><span data-stu-id="1f852-170">Re-use styles on a single page with internal stylesheets</span></span>  

<span data-ttu-id="1f852-171">Em um trecho de código anterior, um estilo em linha aplicava um estilo a uma única `<p>` marca.</span><span class="sxs-lookup"><span data-stu-id="1f852-171">In a previous code snippet, an inline style applied a style to a single `<p>` tag.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="1f852-172">E se você quiser que todos os `<p>` elementos em sua página da Web sejam estilados da mesma maneira?</span><span class="sxs-lookup"><span data-stu-id="1f852-172">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="1f852-173">Você precisa copiar e colar o código em cada marca `<p>` única em seu site.</span><span class="sxs-lookup"><span data-stu-id="1f852-173">You have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="1f852-174">Isso é muito tempo e esforço.</span><span class="sxs-lookup"><span data-stu-id="1f852-174">That is a lot of time and effort.</span></span>  <span data-ttu-id="1f852-175">E, se você precisar fazer uma edição, terá que alterar cada marca novamente.</span><span class="sxs-lookup"><span data-stu-id="1f852-175">And, if you needed to make an edit, you have to change every tag again.</span></span>  <span data-ttu-id="1f852-176">Conclua as seguintes ações para usar **uma folha de** estilos Interna para gravar o CSS uma vez para que ela se aplique a vários elementos.</span><span class="sxs-lookup"><span data-stu-id="1f852-176">Complete the following actions to use an **Internal stylesheet** to write your CSS once so that it applies to multiple elements.</span></span>  

1.  <span data-ttu-id="1f852-177">Na guia ao vivo, escolha **Contato** para navegar até a página de contato.</span><span class="sxs-lookup"><span data-stu-id="1f852-177">In the live tab, choose **Contact** to navigate to the contact page.</span></span>  <span data-ttu-id="1f852-178">Observe a fonte de **Home** e **Contact**.</span><span class="sxs-lookup"><span data-stu-id="1f852-178">Notice the font of **Home** and **Contact**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="A página Contato" lightbox="../media/beginners-css-internal1.msft.png":::
       <span data-ttu-id="1f852-180">A página Contato</span><span class="sxs-lookup"><span data-stu-id="1f852-180">The Contact page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-181">Na **guia editor,** abra `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="1f852-181">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="1f852-182">Adicione o código a seguir a `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="1f852-182">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="1f852-183">Lembre-se de que as linhas que começam `<style>` com e terminam `</style>` com são o que você precisa adicionar.</span><span class="sxs-lookup"><span data-stu-id="1f852-183">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="1f852-184">O outro código está apenas lá para que você saiba onde colocar o novo código.</span><span class="sxs-lookup"><span data-stu-id="1f852-184">The other code is just there so you know where to put the new code.</span></span>  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <style>
                li a {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        </head>
        ...
    ...
    ```  
    
1.  <span data-ttu-id="1f852-185">Volte para a **guia ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="1f852-185">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="1f852-186">Escolha **Contato** para voltar à página de contato.</span><span class="sxs-lookup"><span data-stu-id="1f852-186">Choose **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="1f852-187">A fonte de **Home** e **Contact** foi alterada.</span><span class="sxs-lookup"><span data-stu-id="1f852-187">The font of **Home** and **Contact** has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="A fonte dos links Home e Contact foi alterada" lightbox="../media/beginners-css-internal2.msft.png":::
       <span data-ttu-id="1f852-189">A fonte dos links **Home** e **Contact** foi alterada</span><span class="sxs-lookup"><span data-stu-id="1f852-189">The font of the **Home** and **Contact** links has changed</span></span>  
    :::image-end:::  
    
### <a name="understand-internal-stylesheets"></a><span data-ttu-id="1f852-190">Compreender folhas de estilos internas</span><span class="sxs-lookup"><span data-stu-id="1f852-190">Understand internal stylesheets</span></span>  

<span data-ttu-id="1f852-191">As folhas de estilos internas aplicam estilos usando **seletores**.</span><span class="sxs-lookup"><span data-stu-id="1f852-191">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="1f852-192">Seletores são padrões que podem se aplicar a um ou mais elementos HTML.</span><span class="sxs-lookup"><span data-stu-id="1f852-192">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="1f852-193">O trecho de código anterior adicionou o seguinte estilo.</span><span class="sxs-lookup"><span data-stu-id="1f852-193">The previous code snippet added the following style.</span></span>  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` <span data-ttu-id="1f852-194">é um seletor que se converte em "qualquer `<li>` elemento que contenha um `<a>` elemento".</span><span class="sxs-lookup"><span data-stu-id="1f852-194">is a selector that translates to "any `<li>` element that contains an `<a>` element".</span></span>  <span data-ttu-id="1f852-195">O navegador altera a fonte dos links **Home** e **Contact** porque cada um dos grupos de marca corresponder ao padrão.</span><span class="sxs-lookup"><span data-stu-id="1f852-195">The browser changes the font of the **Home** and **Contact** links because each of the tag groups match the pattern.</span></span>  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="1f852-196">é uma **declaração**.</span><span class="sxs-lookup"><span data-stu-id="1f852-196">is a **declaration**.</span></span>  <span data-ttu-id="1f852-197">Uma declaração é feita de duas partes a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f852-197">A declaration is made of following two parts.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="1f852-198">property</span><span class="sxs-lookup"><span data-stu-id="1f852-198">property</span></span>**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="1f852-199">A propriedade descreve uma maneira geral de você poder alterar o estilo do elemento.</span><span class="sxs-lookup"><span data-stu-id="1f852-199">The property describes a general way that you are able to change the style of the element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="1f852-200">value</span><span class="sxs-lookup"><span data-stu-id="1f852-200">value</span></span>**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="1f852-201">O valor descreve exatamente como o estilo do elemento deve mudar.</span><span class="sxs-lookup"><span data-stu-id="1f852-201">The value describes exactly how the style of the element should change.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="1f852-202">Por exemplo, `font-family: 'Courier New', Courier, serif` fornece ao navegador a seguinte instrução: "Definir a fonte de elementos que corresponderem ao padrão como `li a` `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="1f852-202">For example, `font-family: 'Courier New', Courier, serif` gives the browser the following instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="1f852-203">Se essa fonte não estiver disponível, use `Courier` .</span><span class="sxs-lookup"><span data-stu-id="1f852-203">If that font is not available, use `Courier`.</span></span>  <span data-ttu-id="1f852-204">Se isso não estiver disponível, use `serif` ."</span><span class="sxs-lookup"><span data-stu-id="1f852-204">If that is not available, use `serif`."</span></span>  

### <a name="add-multiple-selectors-to-a-ruleset"></a><span data-ttu-id="1f852-205">Adicionar vários seletores a um ruleset</span><span class="sxs-lookup"><span data-stu-id="1f852-205">Add multiple selectors to a ruleset</span></span>  

<span data-ttu-id="1f852-206">Um bloco de código CSS como o trecho de código a seguir é chamado de **ruleset**.</span><span class="sxs-lookup"><span data-stu-id="1f852-206">A block of CSS code like the following code snippet is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="1f852-207">Conclua as seguintes ações para usar vírgulas para adicionar vários seletores a um ruleset.</span><span class="sxs-lookup"><span data-stu-id="1f852-207">Complete the following actions to use commas to add multiple selectors to a ruleset.</span></span>  

1.  <span data-ttu-id="1f852-208">Na **guia editor,** abra `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="1f852-208">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="1f852-209">Após `li a` o tipo `, h1` .</span><span class="sxs-lookup"><span data-stu-id="1f852-209">After `li a` type `, h1`.</span></span>  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    <span data-ttu-id="1f852-210">O trecho de código anterior informa ao navegador os elementos de estilo da mesma maneira que ele estilos `<h1>` os elementos que corresponderem ao padrão `li a` .</span><span class="sxs-lookup"><span data-stu-id="1f852-210">The previous code snippet tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="1f852-211">Navegue até **a guia ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="1f852-211">Navigate to the **live tab**.</span></span>  
1.  <span data-ttu-id="1f852-212">Escolha o link **Contato** para voltar à página de contato.</span><span class="sxs-lookup"><span data-stu-id="1f852-212">Choose the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="1f852-213">Agora, **entre em contato comigo!**</span><span class="sxs-lookup"><span data-stu-id="1f852-213">Now, **Contact Me!**</span></span> <span data-ttu-id="1f852-214">tem a mesma fonte dos links de navegação.</span><span class="sxs-lookup"><span data-stu-id="1f852-214">has the same font as the navigation links.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="O texto Fale comigo!  agora tem a mesma fonte que os links Home e Contact" lightbox="../media/beginners-css-multiple1.msft.png":::
       <span data-ttu-id="1f852-217">O texto **Fale comigo!**</span><span class="sxs-lookup"><span data-stu-id="1f852-217">The text **Contact Me!**</span></span> <span data-ttu-id="1f852-218">agora tem a mesma fonte que os links **Home** e **Contact**</span><span class="sxs-lookup"><span data-stu-id="1f852-218">now has the same font as the **Home** and **Contact** links</span></span>  
    :::image-end:::  
    
## <a name="experiment-with-devtools"></a><span data-ttu-id="1f852-219">Experimento com DevTools</span><span class="sxs-lookup"><span data-stu-id="1f852-219">Experiment with DevTools</span></span>  

<span data-ttu-id="1f852-220">À medida que você continua sua jornada para se tornar um especialista em desenvolvimento da Web, você pode descobrir que CSS é complicado.</span><span class="sxs-lookup"><span data-stu-id="1f852-220">As you continue your journey to become an expert in web development, you may find that CSS is tricky.</span></span>  <span data-ttu-id="1f852-221">Você pode escrever alguns CSS e esperar que ele seja exibido de uma maneira, mas o navegador faz algo completamente diferente.</span><span class="sxs-lookup"><span data-stu-id="1f852-221">You may write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="1f852-222">Microsoft Edge O DevTools facilita o experimento com alterações e exibe imediatamente como as alterações afetam a página.</span><span class="sxs-lookup"><span data-stu-id="1f852-222">Microsoft Edge DevTools makes it easy to experiment with changes and immediately display how the changes affect the page.</span></span>  

### <a name="add-a-declaration-to-an-existing-rulest-in-devtools"></a><span data-ttu-id="1f852-223">Adicionar uma declaração a um rulest existente no DevTools</span><span class="sxs-lookup"><span data-stu-id="1f852-223">Add a declaration to an existing rulest in DevTools</span></span>  

<span data-ttu-id="1f852-224">Conclua as seguintes ações para iterar no estilo de um elemento existente, adicione uma declaração a um ruleset existente.</span><span class="sxs-lookup"><span data-stu-id="1f852-224">Complete the following actions to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  

1.  <span data-ttu-id="1f852-225">Passe o **mouse** no link Home, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="1f852-225">Hover on the **Home** link, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Inspecionar o link Home" lightbox="../media/beginners-css-add1.msft.png":::
       <span data-ttu-id="1f852-227">Inspecionar o link Home</span><span class="sxs-lookup"><span data-stu-id="1f852-227">Inspect the Home link</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="1f852-228">O DevTools abre junto com sua página.</span><span class="sxs-lookup"><span data-stu-id="1f852-228">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="1f852-229">O código que representa o link Home é `<a href="/">Home</a>` realçado em azul na Árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="1f852-229">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="1f852-230">O trecho de código e a visualização devem estar familiarizados Introdução [html e dom][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="1f852-230">The code snippet and preview should be familiar from [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="1f852-231">Na figura a seguir, a declaração à qual você adicionou anteriormente é exibida na `font-family: 'Courier New', Courier, serif` guia Estilos abaixo da árvore `contact.html` DOM. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="1f852-231">In the following figure, the `font-family: 'Courier New', Courier, serif` declaration that you previously added to `contact.html` is displayed in the **Styles** tab below the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="A guia Estilos está abaixo da árvore DOM" lightbox="../media/beginners-css-add2.msft.png":::
             <span data-ttu-id="1f852-233">A **guia Estilos** está abaixo da árvore DOM</span><span class="sxs-lookup"><span data-stu-id="1f852-233">The **Styles** tab is below the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="1f852-234">Se sua janela DevTools for ampla, a guia Estilos será à direita da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="1f852-234">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="A guia Estilos fica à direita da árvore DOM" lightbox="../media/beginners-css-add3.msft.png":::
             <span data-ttu-id="1f852-236">A **guia Estilos** fica à direita da árvore DOM</span><span class="sxs-lookup"><span data-stu-id="1f852-236">The **Styles** tab is to the right of the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="1f852-237">Escolha a linha vazia abaixo `font-family: 'Courier New', Courier, Serif` para adicionar uma nova declaração.</span><span class="sxs-lookup"><span data-stu-id="1f852-237">Choose the empty line below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Adicionar uma nova declaração" lightbox="../media/beginners-css-add4.msft.png":::
       <span data-ttu-id="1f852-239">Adicionar uma nova declaração</span><span class="sxs-lookup"><span data-stu-id="1f852-239">Add a new declaration</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-240">Digite `color` e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="1f852-240">Type `color` and select `Enter`.</span></span>  <span data-ttu-id="1f852-241">A interface do usuário de preenchimento automático sugere opções conforme você digita.</span><span class="sxs-lookup"><span data-stu-id="1f852-241">The autocomplete UI suggests options as you type.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Cor do tipo" lightbox="../media/beginners-css-add5.msft.png":::
       <span data-ttu-id="1f852-243">Tipo</span><span class="sxs-lookup"><span data-stu-id="1f852-243">Type</span></span> `color`  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-244">Digite `magenta` e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="1f852-244">Type `magenta` and select `Enter`.</span></span>  <span data-ttu-id="1f852-245">Todo o texto na página de contato agora é magenta.</span><span class="sxs-lookup"><span data-stu-id="1f852-245">All of the text on the contact page is now magenta.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Digite magenta" lightbox="../media/beginners-css-add6.msft.png":::
       <span data-ttu-id="1f852-247">Tipo</span><span class="sxs-lookup"><span data-stu-id="1f852-247">Type</span></span> `magenta`  
    :::image-end:::  
    
### <a name="edit-a-declaration-in-devtools"></a><span data-ttu-id="1f852-248">Editar uma declaração no DevTools</span><span class="sxs-lookup"><span data-stu-id="1f852-248">Edit a declaration in DevTools</span></span>  

<span data-ttu-id="1f852-249">Conclua as seguintes ações para editar declarações existentes no DevTools.</span><span class="sxs-lookup"><span data-stu-id="1f852-249">Complete the following actions to edit existing declarations in DevTools.</span></span>  

1.  <span data-ttu-id="1f852-250">Escolha o quadrado magenta ao lado de `magenta` .</span><span class="sxs-lookup"><span data-stu-id="1f852-250">Choose the magenta square next to `magenta`.</span></span>  <span data-ttu-id="1f852-251">Um se picker de cores aparece.</span><span class="sxs-lookup"><span data-stu-id="1f852-251">A color picker pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="O Se picker de cores" lightbox="../media/beginners-css-edit1.msft.png":::
       <span data-ttu-id="1f852-253">O Se picker de cores</span><span class="sxs-lookup"><span data-stu-id="1f852-253">The Color Picker</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-254">Use o se picker de cores para alterar o texto da fonte para uma cor que você gosta.</span><span class="sxs-lookup"><span data-stu-id="1f852-254">Use the color picker to change the font text to a color that you like.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Altere a cor da fonte para roxo com o Selador de Cores" lightbox="../media/beginners-css-edit2.msft.png":::
       <span data-ttu-id="1f852-256">Altere a cor da fonte para roxo com o Selador de Cores</span><span class="sxs-lookup"><span data-stu-id="1f852-256">Change the font color to purple with the Color Picker</span></span>  
    :::image-end:::  
    
### <a name="add-a-new-ruleset-in-devtools"></a><span data-ttu-id="1f852-257">Adicionar um novo conjunto de regras no DevTools</span><span class="sxs-lookup"><span data-stu-id="1f852-257">Add a new ruleset in DevTools</span></span>  

<span data-ttu-id="1f852-258">Conclua as seguintes ações para adicionar novos rulesets no DevTools.</span><span class="sxs-lookup"><span data-stu-id="1f852-258">Complete the following actions to add new rulesets in DevTools.</span></span>  

1.  <span data-ttu-id="1f852-259">Escolha **Nova Regra de Estilo** \( Nova Regra de Estilo ![ ](../media/new-style-rule-icon.msft.png) \) que está ao lado de **.cls**.</span><span class="sxs-lookup"><span data-stu-id="1f852-259">Choose **New Style Rule** \(![New Style Rule](../media/new-style-rule-icon.msft.png)\) which is next to **.cls**.</span></span>  <span data-ttu-id="1f852-260">Um ruleset vazio é exibido `a` como seletor.</span><span class="sxs-lookup"><span data-stu-id="1f852-260">An empty ruleset appears with `a` as the selector.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Adicionar uma nova regra" lightbox="../media/beginners-css-rule1.msft.png":::
       <span data-ttu-id="1f852-262">Adicionar uma nova regra</span><span class="sxs-lookup"><span data-stu-id="1f852-262">Add a new rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-263">Substitua `a` por `a:hover` .</span><span class="sxs-lookup"><span data-stu-id="1f852-263">Replace `a` with `a:hover`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Substituir um por um:hover" lightbox="../media/beginners-css-rule2.msft.png":::
       <span data-ttu-id="1f852-265">Substituir `a` por</span><span class="sxs-lookup"><span data-stu-id="1f852-265">Replace `a` with</span></span> `a:hover`  
    :::image-end:::  
    
    `:hover` <span data-ttu-id="1f852-266">é uma **pseudo-classe**.</span><span class="sxs-lookup"><span data-stu-id="1f852-266">is a **pseudo-class**.</span></span>  <span data-ttu-id="1f852-267">Use pseudo classes para elementos de estilo que podem inserir estados especiais.</span><span class="sxs-lookup"><span data-stu-id="1f852-267">Use pseudo-classes for style elements that may enter special states.</span></span>  <span data-ttu-id="1f852-268">Por exemplo, o `a:hover` estilo só entra em vigor quando você está pairando sobre um `<a>` elemento.</span><span class="sxs-lookup"><span data-stu-id="1f852-268">For example, the `a:hover` style only takes effect when you are hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="1f852-269">Escolha entre os colchetes para adicionar uma nova declaração.</span><span class="sxs-lookup"><span data-stu-id="1f852-269">Choose between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="1f852-270">Digite `background-color` o nome da declaração e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="1f852-270">Type `background-color` for the declaration name and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Digite background-color" lightbox="../media/beginners-css-rule3.msft.png":::
       <span data-ttu-id="1f852-272">Tipo</span><span class="sxs-lookup"><span data-stu-id="1f852-272">Type</span></span> `background-color`  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-273">Digite `green` o valor da declaração e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="1f852-273">Type `green` for the declaration value and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Digite verde" lightbox="../media/beginners-css-rule4.msft.png":::
       <span data-ttu-id="1f852-275">Tipo</span><span class="sxs-lookup"><span data-stu-id="1f852-275">Type</span></span> `green`  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-276">Passe o mouse sobre o link **Página** 1.</span><span class="sxs-lookup"><span data-stu-id="1f852-276">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="1f852-277">O plano de fundo do link fica verde.</span><span class="sxs-lookup"><span data-stu-id="1f852-277">The background of the link turns green.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Passe o mouse no link Home para revelar seu plano de fundo verde" lightbox="../media/beginners-css-rule5.msft.png":::
       <span data-ttu-id="1f852-279">Passe o mouse no link Home para revelar seu plano de fundo verde</span><span class="sxs-lookup"><span data-stu-id="1f852-279">Hover on the Home link to reveal its green background</span></span>  
    :::image-end:::  
    
## <a name="re-use-styles-across-pages-with-external-stylesheets"></a><span data-ttu-id="1f852-280">Rea uso de estilos em páginas com folhas de estilos externas</span><span class="sxs-lookup"><span data-stu-id="1f852-280">Re-use styles across pages with external stylesheets</span></span>  

<span data-ttu-id="1f852-281">Em uma etapa anterior, você adicionou o seguinte trecho de código como uma folha de estilos interna a `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="1f852-281">In a previous step, you added the following code snippet as an internal stylesheet to `contact.html`.</span></span>  

```html
...
    ...
        ...
        <style>
            li a, h1 {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

<span data-ttu-id="1f852-282">E se você quiser ter `index.html` o mesmo estilo?</span><span class="sxs-lookup"><span data-stu-id="1f852-282">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="1f852-283">E se você tivesse um grande número de páginas para as quais você queria aplicar seus estilos?</span><span class="sxs-lookup"><span data-stu-id="1f852-283">What if you had a large number of pages to which you wanted to apply your styles?</span></span>  <span data-ttu-id="1f852-284">Você precisa copiar e colar a folha de estilos interna em cada página da Web única em seu site.</span><span class="sxs-lookup"><span data-stu-id="1f852-284">You have to copy and paste the internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="1f852-285">Conclua as seguintes ações para adicionar uma **folha de** estilos externa para permitir que você escreva seu CSS uma vez e aplicá-lo a várias páginas.</span><span class="sxs-lookup"><span data-stu-id="1f852-285">Complete the following actions to add an **External stylesheet** to allow you to write your CSS once and apply it to multiple pages.</span></span>  

1.  <span data-ttu-id="1f852-286">Primeiro, atualize a guia ao vivo para remover as alterações feitas no DevTools.</span><span class="sxs-lookup"><span data-stu-id="1f852-286">First, refresh the live tab to remove the changes that you made in DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" Depois de atualizar a página, as alterações feitas no DevTools se foram" lightbox="../media/beginners-css-external1.msft.png":::
        <span data-ttu-id="1f852-288">Depois de atualizar a página, as alterações feitas no DevTools se foram</span><span class="sxs-lookup"><span data-stu-id="1f852-288">After you refresh the page, the changes that were made in DevTools are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-289">Volte para a **guia editor e** abra `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="1f852-289">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       <span data-ttu-id="1f852-291">contact.html</span><span class="sxs-lookup"><span data-stu-id="1f852-291">contact.html</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-292">Exclua tudo `<style>` entre e , incluindo e `</style>` `<style>` `</style>` .</span><span class="sxs-lookup"><span data-stu-id="1f852-292">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="A marca de estilo foi removida" lightbox="../media/beginners-css-external3.msft.png":::
       <span data-ttu-id="1f852-294">A marca de estilo foi removida</span><span class="sxs-lookup"><span data-stu-id="1f852-294">The style tag has been removed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-295">Abra `index.html` e remova da `style="background-color: aliceblue;"` `<nav>` marca.</span><span class="sxs-lookup"><span data-stu-id="1f852-295">Open `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="1f852-296">Agora você removeu todo o CSS adicionado anteriormente ao seu site.</span><span class="sxs-lookup"><span data-stu-id="1f852-296">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="O estilo em linha foi removido do elemento nav" lightbox="../media/beginners-css-external4.msft.png":::
       <span data-ttu-id="1f852-298">O estilo em linha foi removido do elemento nav</span><span class="sxs-lookup"><span data-stu-id="1f852-298">The inline style has been removed from the nav element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-299">Escolha **Novo Arquivo**.</span><span class="sxs-lookup"><span data-stu-id="1f852-299">Choose **New File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="A nova caixa de diálogo de arquivo" lightbox="../media/beginners-css-external5.msft.png":::
       <span data-ttu-id="1f852-301">A nova caixa de diálogo de arquivo</span><span class="sxs-lookup"><span data-stu-id="1f852-301">The new file dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-302">Substitua `cool-file.js` e escolha Adicionar `style.css` **Arquivo**.</span><span class="sxs-lookup"><span data-stu-id="1f852-302">Replace `cool-file.js` with `style.css` and choose **Add File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Tipo style.css" lightbox="../media/beginners-css-external6.msft.png":::
       <span data-ttu-id="1f852-304">Tipo</span><span class="sxs-lookup"><span data-stu-id="1f852-304">Type</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-305">Adicione o seguinte trecho de código ao seu `style.css` arquivo.</span><span class="sxs-lookup"><span data-stu-id="1f852-305">Add the following code snippet to your `style.css` file.</span></span>  
    
    ```css
    li a, h1 {
      font-family: 'Courier New', Courier, Serif;
    }
    a:hover {
      background-color: green;
    }
    nav {
      background-color: aliceblue;
    }
    ```  
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Adicionar código a style.css" lightbox="../media/beginners-css-external7.msft.png":::
       <span data-ttu-id="1f852-307">Adicionar código ao</span><span class="sxs-lookup"><span data-stu-id="1f852-307">Add code to</span></span> `style.css`  
    :::image-end:::  
    
    <span data-ttu-id="1f852-308">Verifique se você criou uma folha de estilos externa.</span><span class="sxs-lookup"><span data-stu-id="1f852-308">Ensure that you have created an external stylesheet.</span></span> <span data-ttu-id="1f852-309">Seu HTML não está ciente de que ele existe.</span><span class="sxs-lookup"><span data-stu-id="1f852-309">Your HTML is not aware that it exists.</span></span>  
    
1.  <span data-ttu-id="1f852-310">Abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="1f852-310">Open `index.html`.</span></span>  
1.  <span data-ttu-id="1f852-311">Adicione `<link rel="stylesheet" href="style.css">` ao HTML.</span><span class="sxs-lookup"><span data-stu-id="1f852-311">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Link para style.css" lightbox="../media/beginners-css-external8.msft.png":::
       <span data-ttu-id="1f852-313">Link para</span><span class="sxs-lookup"><span data-stu-id="1f852-313">Link to</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-314">Abra o `contact.html` arquivo e adicione o link lá.</span><span class="sxs-lookup"><span data-stu-id="1f852-314">Open the `contact.html` file and add the link there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Link para style.css em contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       <span data-ttu-id="1f852-316">Link para `style.css` em</span><span class="sxs-lookup"><span data-stu-id="1f852-316">Link to `style.css` in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-317">Navegue até **a guia ao vivo**.  A home page agora tem a mesma fonte da última seção e uma seção de navegação azul.</span><span class="sxs-lookup"><span data-stu-id="1f852-317">Navigate to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="A home page" lightbox="../media/beginners-css-external10.msft.png":::
       <span data-ttu-id="1f852-319">A home page</span><span class="sxs-lookup"><span data-stu-id="1f852-319">The home page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-320">Escolha o link **Contato** para navegar até a página de contato.</span><span class="sxs-lookup"><span data-stu-id="1f852-320">Choose the **Contact** link to navigate to the contact page.</span></span>  <span data-ttu-id="1f852-321">A página de contato tem a mesma formatação da home page.</span><span class="sxs-lookup"><span data-stu-id="1f852-321">The contact page has the same formatting as the home page.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="A página de contato" lightbox="../media/beginners-css-external11.msft.png":::
       <span data-ttu-id="1f852-323">A página de contato</span><span class="sxs-lookup"><span data-stu-id="1f852-323">The contact page</span></span>  
    :::image-end:::  
    
## <a name="use-a-css-framework"></a><span data-ttu-id="1f852-324">Usar uma estrutura CSS</span><span class="sxs-lookup"><span data-stu-id="1f852-324">Use a CSS framework</span></span>  

<span data-ttu-id="1f852-325">**Estruturas CSS** são coleções de estilos criadas por outros desenvolvedores que facilitam a criação de sites atraentes.</span><span class="sxs-lookup"><span data-stu-id="1f852-325">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="1f852-326">Em vez de definir estilos por conta própria, uma estrutura fornece uma coleção de estilos que você pode usar em seus elementos de página.</span><span class="sxs-lookup"><span data-stu-id="1f852-326">Instead of defining styles yourself, a framework provides you a collection of styles that you are able to use on your page elements.</span></span>  

1.  <span data-ttu-id="1f852-327">Copie o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="1f852-327">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="1f852-328">Abra a guia edição e colar o código em `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="1f852-328">Open the editing tab and paste the code into `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Link para a estrutura em contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       <span data-ttu-id="1f852-330">Link para a estrutura em</span><span class="sxs-lookup"><span data-stu-id="1f852-330">Link to the framework in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-331">Abra o `index.html` arquivo e adicione o código lá.</span><span class="sxs-lookup"><span data-stu-id="1f852-331">Open the `index.html` file and add the code there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Link para a estrutura em index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       <span data-ttu-id="1f852-333">Link para a estrutura em</span><span class="sxs-lookup"><span data-stu-id="1f852-333">Link to the framework in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-334">Volte para a guia ao vivo para exibir suas alterações.</span><span class="sxs-lookup"><span data-stu-id="1f852-334">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="1f852-335">Embora a cor de plano de fundo do elemento e a fonte dos elementos e sejam as mesmas, a `<nav>` fonte dos outros elementos foi `<li>` `<a>` alterada.</span><span class="sxs-lookup"><span data-stu-id="1f852-335">While the background color of the `<nav>` element and the font of the `<li>` and `<a>` elements are the same, the font of the other elements has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Parte da fonte na home page foi alterada devido à estrutura" lightbox="../media/beginners-css-framework3.msft.png":::
       <span data-ttu-id="1f852-337">Parte da fonte na home page foi alterada devido à estrutura</span><span class="sxs-lookup"><span data-stu-id="1f852-337">Some of the font on the home page changed because of the framework</span></span>  
    :::image-end:::  
    
### <a name="use-a-class"></a><span data-ttu-id="1f852-338">Usar uma classe</span><span class="sxs-lookup"><span data-stu-id="1f852-338">Use a class</span></span>  

<span data-ttu-id="1f852-339">Na última seção, você adicionou Bootstrap às páginas da Web, que alterou as fontes de alguns dos elementos em seu site.</span><span class="sxs-lookup"><span data-stu-id="1f852-339">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="1f852-340">As estruturas CSS ajudam você a fazer alterações importantes em sua página com muito pouco código.</span><span class="sxs-lookup"><span data-stu-id="1f852-340">CSS frameworks help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="1f852-341">Conclua as seguintes ações para alterar o seu header.</span><span class="sxs-lookup"><span data-stu-id="1f852-341">Complete the following actions to change your header.</span></span>  

1.  <span data-ttu-id="1f852-342">Copie o seguinte trecho de código.</span><span class="sxs-lookup"><span data-stu-id="1f852-342">Copy the following code snippet.</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="1f852-343">Adicione o trecho de código anterior à `<header>` sua marca em `index.html` .</span><span class="sxs-lookup"><span data-stu-id="1f852-343">Add the previous code snippet to your `<header>` tag in `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Adicionar classes em index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       <span data-ttu-id="1f852-345">Adicionar classes em</span><span class="sxs-lookup"><span data-stu-id="1f852-345">Add classes in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-346">Adicione o código à `<header>` sua marca em `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="1f852-346">Add the code to your `<header>` tag in `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Adicionar classes em contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       <span data-ttu-id="1f852-348">Adicionar classes em</span><span class="sxs-lookup"><span data-stu-id="1f852-348">Add classes in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-349">Exibir suas alterações na guia ao vivo.  Há uma caixa grande e cinza ao redor do seu header.</span><span class="sxs-lookup"><span data-stu-id="1f852-349">View your changes in the live tab.  There is a big, grey box around your header.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="O header agora tem uma caixa grande e cinza ao seu redor" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       <span data-ttu-id="1f852-351">O header agora tem uma caixa grande e cinza ao seu redor</span><span class="sxs-lookup"><span data-stu-id="1f852-351">The header now has a big, grey box around it</span></span>  
    :::image-end:::  
    
### <a name="understand-classes"></a><span data-ttu-id="1f852-352">Compreender classes</span><span class="sxs-lookup"><span data-stu-id="1f852-352">Understand classes</span></span>  

<span data-ttu-id="1f852-353">Classes permitem atribuir coleções de estilos a elementos arbitrários.</span><span class="sxs-lookup"><span data-stu-id="1f852-353">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="1f852-354">Use o seguinte trecho de código para aplicar vários estilos ao elemento depois de `<header>` definir o atributo como `class` `jumbotron` .</span><span class="sxs-lookup"><span data-stu-id="1f852-354">Use the following code snippet to apply several styles to the `<header>` element after you set the `class` attribute to `jumbotron`.</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="1f852-355">Uma vantagem de uma classe é que ela permite que você aplique estilos a qualquer elemento que você deseja.</span><span class="sxs-lookup"><span data-stu-id="1f852-355">One advantage of a class is that it lets you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="1f852-356">Por exemplo, suponha que você queira definir a cor de plano de fundo de alguns `<p>` elementos como roxo, mas não todos os `<p>` elementos.</span><span class="sxs-lookup"><span data-stu-id="1f852-356">For example, suppose you want to set the background color of some `<p>` elements to purple, but not all `<p>` elements.</span></span>  <span data-ttu-id="1f852-357">Use o seguinte trecho de código para definir o estilo em uma classe.</span><span class="sxs-lookup"><span data-stu-id="1f852-357">Use the following code snippet to define the style in a class.</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="1f852-358">Em seguida, aplique a classe apenas aos `<p>` elementos que você deseja estilo.</span><span class="sxs-lookup"><span data-stu-id="1f852-358">Next, apply the class to only the `<p>` elements that you want to style.</span></span>  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### <a name="align-elements"></a><span data-ttu-id="1f852-359">Alinhar elementos</span><span class="sxs-lookup"><span data-stu-id="1f852-359">Align elements</span></span>  

<span data-ttu-id="1f852-360">Conclua as seguintes ações para inicializar e forneça classes para elementos de alinhamento.</span><span class="sxs-lookup"><span data-stu-id="1f852-360">Complete the following actions to bootstrap and provide classes for aligning elements.</span></span>  

1.  <span data-ttu-id="1f852-361">Volte para a guia editor e abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="1f852-361">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="1f852-362">Adicione `class="container-fluid"` à `<body>` sua marca.</span><span class="sxs-lookup"><span data-stu-id="1f852-362">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Adicionar a classe de fluido de contêiner" lightbox="../media/beginners-css-align1.msft.png":::
       <span data-ttu-id="1f852-364">Adicionar a `container-fluid` classe</span><span class="sxs-lookup"><span data-stu-id="1f852-364">Add the `container-fluid` class</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-365">Wrap your `<nav>` and `<main>` elements in `<div class="row">` .</span><span class="sxs-lookup"><span data-stu-id="1f852-365">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="1f852-366">Certifique-se de `</div>` colocar depois para fechar `</main>` corretamente a nova marca.</span><span class="sxs-lookup"><span data-stu-id="1f852-366">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Adicionar uma linha" lightbox="../media/beginners-css-align2.msft.png":::
       <span data-ttu-id="1f852-368">Adicionar uma linha</span><span class="sxs-lookup"><span data-stu-id="1f852-368">Add a row</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-369">Adicione `class="col-3"` à sua marca e à sua `<nav>` `class="col-9"` `<main>` marca.</span><span class="sxs-lookup"><span data-stu-id="1f852-369">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Adicionar as classes col-3 e col-9" lightbox="../media/beginners-css-align3.msft.png":::
       <span data-ttu-id="1f852-371">Adicionar as `col-3` classes e `col-9`</span><span class="sxs-lookup"><span data-stu-id="1f852-371">Add the `col-3` and `col-9` classes</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1f852-372">Exibir suas alterações na guia ao vivo.</span><span class="sxs-lookup"><span data-stu-id="1f852-372">View your changes in the live tab.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="O conteúdo de nav agora está à esquerda do conteúdo principal" lightbox="../media/beginners-css-align4.msft.png":::
       <span data-ttu-id="1f852-374">O conteúdo de nav agora está à esquerda do conteúdo principal</span><span class="sxs-lookup"><span data-stu-id="1f852-374">The nav content is now to the left of the main content</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="1f852-375">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="1f852-375">Next steps</span></span>  

<span data-ttu-id="1f852-376">Parabéns, você terminou.</span><span class="sxs-lookup"><span data-stu-id="1f852-376">Congratulations, you are done.</span></span>  

*   <span data-ttu-id="1f852-377">A melhor maneira de melhorar o desenvolvimento da Web é criar mais sites.</span><span class="sxs-lookup"><span data-stu-id="1f852-377">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="1f852-378">Não se preocupe com quebra de material.</span><span class="sxs-lookup"><span data-stu-id="1f852-378">Do not worry about breaking stuff.</span></span>  <span data-ttu-id="1f852-379">Divirta-se e aprenda o máximo possível ao longo do caminho.</span><span class="sxs-lookup"><span data-stu-id="1f852-379">Just have fun and learn as much as possible along the way.</span></span>  
*   <span data-ttu-id="1f852-380">Para saber mais sobre o estilo de páginas da Web, navegue até [Introdução ao CSS][MDNCssFirstSteps].</span><span class="sxs-lookup"><span data-stu-id="1f852-380">To learn more about styling web pages, navigate to [Introduction to CSS][MDNCssFirstSteps].</span></span>  
*   <span data-ttu-id="1f852-381">Para saber mais sobre como usar o DevTools para experimentar o CSS de uma página, navegue até Introdução [exibição e alteração css][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="1f852-381">To learn more about how to use DevTools to experiment with the CSS of a page, navigate to [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="1f852-382">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1f852-382">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools para Iniciantes: Introdução html e o dom | Microsoft Docs"  
[DevtoolsCssIndex]: ../css/index.md "Introdução Com exibição e alteração de css | Microsoft Docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html - cooked-amphibian | Glitch"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "As primeiras etapas do CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="1f852-388">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1f852-388">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1f852-389">A página original foi encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/beginners/css) e foi criada por [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="1f852-389">The original page was found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and was authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1f852-391">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1f852-391">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
