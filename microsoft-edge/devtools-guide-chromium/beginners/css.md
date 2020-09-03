---
description: Introdução ao CSS
title: 'DevTools para iniciantes: introdução ao CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: fe87b4f840c6d9dde3cdf6455700161ea8d8d31e
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993300"
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

# <span data-ttu-id="ccc87-104">DevTools para iniciantes: introdução ao CSS</span><span class="sxs-lookup"><span data-stu-id="ccc87-104">DevTools for beginners: Get started with CSS</span></span>  

<span data-ttu-id="ccc87-105">Neste tutorial, você aprenderá a usar CSS para estilizar uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="ccc87-105">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="ccc87-106">Você também aprenderá a usar o Microsoft Edge DevTools para experimentar alterações de CSS.</span><span class="sxs-lookup"><span data-stu-id="ccc87-106">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="ccc87-107">O artigo a seguir é o segundo tutorial em uma série de tutoriais que ensina a você noções básicas sobre o desenvolvimento da Web e o Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="ccc87-107">The following article is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="ccc87-108">Na verdade, você ganha experiência prática ao criar seu próprio website.</span><span class="sxs-lookup"><span data-stu-id="ccc87-108">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="ccc87-109">Você não precisa concluir o primeiro tutorial antes de seguir o segundo.</span><span class="sxs-lookup"><span data-stu-id="ccc87-109">You do not have to complete the first tutorial before following the second.</span></span>  <span data-ttu-id="ccc87-110">[Configurar seu código](#set-up-your-code) mostra como fazer a configuração.</span><span class="sxs-lookup"><span data-stu-id="ccc87-110">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="ccc87-111">Este tutorial foi projetado para principiantes absolutos e se concentra nos **fundamentos do desenvolvimento na Web** e nas noções básicas de como usar o devtools para experimentar com CSS.</span><span class="sxs-lookup"><span data-stu-id="ccc87-111">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="ccc87-112">Se você quiser um tutorial que só se concentre no DevTools, confira [introdução e alterar CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="ccc87-112">If you want a tutorial that only focuses on DevTools, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="ccc87-113">No início do tutorial, o seu site deve ter a aparência da figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="ccc87-113">At the beginning of the tutorial, your site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-intro1.msft.png":::
   <span data-ttu-id="ccc87-115">Qual é a aparência de seu site</span><span class="sxs-lookup"><span data-stu-id="ccc87-115">What your site currently looks like</span></span>  
:::image-end:::  

<span data-ttu-id="ccc87-116">Depois de concluir o tutorial, o site deve ter a aparência da figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="ccc87-116">After you complete the tutorial, you site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Qual deve ser a aparência de seu site no final do tutorial" lightbox="../media/beginners-css-intro2.msft.png":::
   <span data-ttu-id="ccc87-118">Qual deve ser a aparência de seu site no final do tutorial</span><span class="sxs-lookup"><span data-stu-id="ccc87-118">What your site should look like at the end of the tutorial</span></span>  
:::image-end:::  

## <span data-ttu-id="ccc87-119">Goal</span><span class="sxs-lookup"><span data-stu-id="ccc87-119">Goals</span></span>  

<span data-ttu-id="ccc87-120">Siga este tutorial para compreender melhor os conceitos e tarefas a seguir.</span><span class="sxs-lookup"><span data-stu-id="ccc87-120">Follow this tutorial to better understand the following concepts and tasks.</span></span>  

*   <span data-ttu-id="ccc87-121">Como usar CSS para estilizar uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="ccc87-121">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="ccc87-122">Como usar o Microsoft Edge DevTools para experimentar com CSS.</span><span class="sxs-lookup"><span data-stu-id="ccc87-122">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="ccc87-123">A diferença entre estruturas CSS e CSS.</span><span class="sxs-lookup"><span data-stu-id="ccc87-123">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="ccc87-124">Você está criando um site real.</span><span class="sxs-lookup"><span data-stu-id="ccc87-124">You are building a real website.</span></span>  

## <span data-ttu-id="ccc87-125">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="ccc87-125">Prerequisites</span></span>  

<span data-ttu-id="ccc87-126">Antes de tentar este tutorial, complete os pré-requisitos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ccc87-126">Before attempting this tutorial, complete the following prerequisites.</span></span>  

*   <span data-ttu-id="ccc87-127">Conclua [a introdução ao HTML e ao dom][DevtoolsBeginnersHtml] ou certifique-se de ter uma compreensão do HTML e do dom semelhante ao que é ensinado nesse tutorial.</span><span class="sxs-lookup"><span data-stu-id="ccc87-127">Complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what is taught in that tutorial.</span></span>  
*   <span data-ttu-id="ccc87-128">Baixar o navegador da Web [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="ccc87-128">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="ccc87-129">O tutorial a seguir usa um conjunto de ferramentas de desenvolvimento da Web, chamado de Microsoft Edge DevTools, incorporado ao Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ccc87-129">The following tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="ccc87-130">Configurar seu código</span><span class="sxs-lookup"><span data-stu-id="ccc87-130">Set up your code</span></span>  

<span data-ttu-id="ccc87-131">Para criar seu site, primeiro você deve concluir as seguintes ações para configurar o código.</span><span class="sxs-lookup"><span data-stu-id="ccc87-131">To create your site, you must first complete the following actions to set up your code.</span></span>  

> [!NOTE]
> <span data-ttu-id="ccc87-132">Se você já concluiu o primeiro tutorial da série, pule para a próxima seção.</span><span class="sxs-lookup"><span data-stu-id="ccc87-132">If you have already completed the first tutorial in the series, skip to the next section.</span></span>  <span data-ttu-id="ccc87-133">Continue usando o código do último tutorial, [introdução ao HTML e ao dom][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="ccc87-133">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  

1.  <span data-ttu-id="ccc87-134">Abra o [código-fonte][GlitchCookedAmphibianIndex].</span><span class="sxs-lookup"><span data-stu-id="ccc87-134">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="ccc87-135">A guia in-Focus do seu navegador é referenciada como a **guia edição**.</span><span class="sxs-lookup"><span data-stu-id="ccc87-135">The in-focus tab of your browser is referenced as the **editing tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="A guia edição" lightbox="../media/beginners-css-setup1.msft.png":::
       <span data-ttu-id="ccc87-137">A guia **edição**</span><span class="sxs-lookup"><span data-stu-id="ccc87-137">The **editing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-138">Escolha **cozinhá-Amphibian**.</span><span class="sxs-lookup"><span data-stu-id="ccc87-138">Choose **cooked-amphibian**.</span></span>  <span data-ttu-id="ccc87-139">Um menu é exibido.</span><span class="sxs-lookup"><span data-stu-id="ccc87-139">A menu pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="O menu opções do Project" lightbox="../media/beginners-css-setup2.msft.png":::
       <span data-ttu-id="ccc87-141">O menu opções do Project</span><span class="sxs-lookup"><span data-stu-id="ccc87-141">The Project Options menu</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="ccc87-142">Escolha **projeto remix**.</span><span class="sxs-lookup"><span data-stu-id="ccc87-142">Choose **Remix Project**.</span></span>  <span data-ttu-id="ccc87-143">Falha cria uma cópia do projeto que você pode editar.</span><span class="sxs-lookup"><span data-stu-id="ccc87-143">Glitch creates a copy of the project that you are able to edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="ccc87-144">A falha gera um nome aleatório para o novo projeto.</span><span class="sxs-lookup"><span data-stu-id="ccc87-144">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="ccc87-145">Escolha **Mostrar** e selecione **em uma nova janela**.</span><span class="sxs-lookup"><span data-stu-id="ccc87-145">Choose **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="ccc87-146">Outra guia abre com uma visualização dinâmica do seu site.</span><span class="sxs-lookup"><span data-stu-id="ccc87-146">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="ccc87-147">A guia em foco do seu navegador é referenciada como a **guia ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="ccc87-147">The in-focus tab of your browser is referenced as the **live tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="A guia ao vivo" lightbox="../media/beginners-css-setup3.msft.png":::
       <span data-ttu-id="ccc87-149">A **guia ao vivo**</span><span class="sxs-lookup"><span data-stu-id="ccc87-149">The **live tab**</span></span>  
    :::image-end:::  

## <span data-ttu-id="ccc87-150">Entender CSS</span><span class="sxs-lookup"><span data-stu-id="ccc87-150">Understand CSS</span></span>  

<span data-ttu-id="ccc87-151">**CSS** é um idioma de computador que determina o layout e o estilo de páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="ccc87-151">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="ccc87-152">A figura a seguir é um parágrafo com uma borda.</span><span class="sxs-lookup"><span data-stu-id="ccc87-152">The following figure is a paragraph with a border.</span></span>  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="O texto foi estilizado com CSS" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   <span data-ttu-id="ccc87-154">O texto foi estilizado com CSS</span><span class="sxs-lookup"><span data-stu-id="ccc87-154">The text has been styled with CSS</span></span>  
:::image-end:::  

<span data-ttu-id="ccc87-155">O trecho de código a seguir é o código HTML e CSS usado para criar o parágrafo na figura anterior.</span><span class="sxs-lookup"><span data-stu-id="ccc87-155">The following code snippet is the HTML and CSS code used to create the paragraph in the previous figure.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="ccc87-156">Provavelmente parece novidade para você.</span><span class="sxs-lookup"><span data-stu-id="ccc87-156">probably looks new to you.</span></span>  <span data-ttu-id="ccc87-157">O restante deve parecer familiar.</span><span class="sxs-lookup"><span data-stu-id="ccc87-157">The rest should look familiar.</span></span>  <span data-ttu-id="ccc87-158">Caso contrário, conclua a [introdução com HTML e o dom][DevtoolsBeginnersHtml] antes de tentar as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="ccc87-158">If not, complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] before attempting the following sections.</span></span>  

## <span data-ttu-id="ccc87-159">Adicionar estilos em linha</span><span class="sxs-lookup"><span data-stu-id="ccc87-159">Add inline styles</span></span>  

<span data-ttu-id="ccc87-160">Conclua as ações a seguir para usar **estilos embutidos** para aplicar estilos a um único elemento.</span><span class="sxs-lookup"><span data-stu-id="ccc87-160">Complete the following actions to use **inline styles** to apply styles to a single element.</span></span>  

1.  <span data-ttu-id="ccc87-161">Volte para a guia edição e abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-161">Go back to the editing tab and open `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       <span data-ttu-id="ccc87-163">Abrir `index.html` na guia edição</span><span class="sxs-lookup"><span data-stu-id="ccc87-163">Open `index.html` in the editing tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-164">Adicionar `style="background-color: aliceblue;"` à sua `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-164">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="ccc87-165">No bloco de código abaixo, a quarta linha de código é aquela que você precisa alterar.</span><span class="sxs-lookup"><span data-stu-id="ccc87-165">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="ccc87-166">O restante está apenas lá, portanto, você pode garantir que está colocando o novo código no lugar certo.</span><span class="sxs-lookup"><span data-stu-id="ccc87-166">The rest is just there, so you are able to ensure that you are putting the new code in the right place.</span></span>  
    
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
    
1.  <span data-ttu-id="ccc87-167">Vá para a **guia ao vivo** para ver as alterações!</span><span class="sxs-lookup"><span data-stu-id="ccc87-167">Go to the **live tab** to see the changes!</span></span>  <span data-ttu-id="ccc87-168">O plano de fundo da `<nav>` seção agora está em azul.</span><span class="sxs-lookup"><span data-stu-id="ccc87-168">The background of the `<nav>` section is now blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="A cor do plano de fundo por trás da página inicial e dos links de contatos agora está azul" lightbox="../media/beginners-css-inline2.msft.png":::
       <span data-ttu-id="ccc87-170">A cor do plano de fundo por trás da **página inicial** e dos links de **contatos** agora está azul</span><span class="sxs-lookup"><span data-stu-id="ccc87-170">The background color behind the **Home** and **Contact** links is now blue</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ccc87-171">Reutilizar estilos em uma única página com folhas de estilos internas</span><span class="sxs-lookup"><span data-stu-id="ccc87-171">Re-use styles on a single page with internal stylesheets</span></span>  

<span data-ttu-id="ccc87-172">Em um trecho de código anterior, um estilo embutido aplicou um estilo a uma única `<p>` marca.</span><span class="sxs-lookup"><span data-stu-id="ccc87-172">In a previous code snippet, an inline style applied a style to a single `<p>` tag.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="ccc87-173">E se você quiser que todos os `<p>` elementos na sua página da Web tenham o estilo da mesma maneira?</span><span class="sxs-lookup"><span data-stu-id="ccc87-173">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="ccc87-174">Você precisaria copiar e colar o código em cada marca única `<p>` do seu site.</span><span class="sxs-lookup"><span data-stu-id="ccc87-174">You would have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="ccc87-175">Isso é muito tempo e esforço.</span><span class="sxs-lookup"><span data-stu-id="ccc87-175">That is a lot of time and effort.</span></span>  <span data-ttu-id="ccc87-176">E, se precisar fazer uma edição, você precisaria alterar todas as marcas novamente.</span><span class="sxs-lookup"><span data-stu-id="ccc87-176">And, if you needed to make an edit, you would have to change every tag again.</span></span>  <span data-ttu-id="ccc87-177">Conclua as ações a seguir para usar uma **folha de estilos interna** para escrever seu CSS uma vez para que ele se aplique a vários elementos.</span><span class="sxs-lookup"><span data-stu-id="ccc87-177">Complete the following actions to use an **Internal stylesheet** to write your CSS once so that it applies to multiple elements.</span></span>  

1.  <span data-ttu-id="ccc87-178">Na guia ao vivo, escolha **contato** para acessar a página do contato.</span><span class="sxs-lookup"><span data-stu-id="ccc87-178">In the live tab, choose **Contact** to go to the contact page.</span></span>  <span data-ttu-id="ccc87-179">Observe a fonte de **casa** e do **contato**.</span><span class="sxs-lookup"><span data-stu-id="ccc87-179">Notice the font of **Home** and **Contact**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="Página de contato" lightbox="../media/beginners-css-internal1.msft.png":::
       <span data-ttu-id="ccc87-181">Página de contato</span><span class="sxs-lookup"><span data-stu-id="ccc87-181">The Contact page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-182">Na **guia Editor**, vá para `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-182">In the **editor tab**, go to `contact.html`.</span></span>  
1.  <span data-ttu-id="ccc87-183">Adicione o código a seguir a `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-183">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="ccc87-184">Lembre-se de que as linhas começando com `<style>` e terminando `</style>` são o que você precisa adicionar.</span><span class="sxs-lookup"><span data-stu-id="ccc87-184">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="ccc87-185">O outro código está aqui para que você saiba onde colocar o novo código.</span><span class="sxs-lookup"><span data-stu-id="ccc87-185">The other code is just there so you know where to put the new code.</span></span>  
    
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
    
1.  <span data-ttu-id="ccc87-186">Volte para a **guia ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="ccc87-186">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="ccc87-187">Escolha **contato** para voltar para a página de contato.</span><span class="sxs-lookup"><span data-stu-id="ccc87-187">Choose **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="ccc87-188">A fonte de **casa** e o **contato** foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="ccc87-188">The font of **Home** and **Contact** has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="A fonte dos links de página inicial e contato foi alterada" lightbox="../media/beginners-css-internal2.msft.png":::
       <span data-ttu-id="ccc87-190">A fonte dos links de **página inicial** e **contato** foi alterada</span><span class="sxs-lookup"><span data-stu-id="ccc87-190">The font of the **Home** and **Contact** links has changed</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="ccc87-191">Entender as folhas de estilos internas</span><span class="sxs-lookup"><span data-stu-id="ccc87-191">Understand internal stylesheets</span></span>  

<span data-ttu-id="ccc87-192">As folhas de estilos internas aplicam estilos usando **seletores**.</span><span class="sxs-lookup"><span data-stu-id="ccc87-192">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="ccc87-193">Os seletores são padrões que podem ser aplicados a um ou mais elementos HTML.</span><span class="sxs-lookup"><span data-stu-id="ccc87-193">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="ccc87-194">O trecho de código anterior adicionou o estilo a seguir.</span><span class="sxs-lookup"><span data-stu-id="ccc87-194">The previous code snippet added the following style.</span></span>  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` <span data-ttu-id="ccc87-195">é um seletor que traduz para "qualquer `<li>` elemento que contém um `<a>` elemento".</span><span class="sxs-lookup"><span data-stu-id="ccc87-195">is a selector that translates to "any `<li>` element that contains an `<a>` element".</span></span>  <span data-ttu-id="ccc87-196">O navegador altera a fonte dos links de **página inicial** e de **contato** porque cada um dos grupos de marcas corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="ccc87-196">The browser changes the font of the **Home** and **Contact** links because each of the tag groups match the pattern.</span></span>  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="ccc87-197">é uma **declaração**.</span><span class="sxs-lookup"><span data-stu-id="ccc87-197">is a **declaration**.</span></span>  <span data-ttu-id="ccc87-198">Uma declaração é feita das duas partes A seguir.</span><span class="sxs-lookup"><span data-stu-id="ccc87-198">A declaration is made of following two parts.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="ccc87-199">folha</span><span class="sxs-lookup"><span data-stu-id="ccc87-199">property</span></span>**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="ccc87-200">A propriedade descreve uma maneira geral pela qual você pode alterar o estilo do elemento.</span><span class="sxs-lookup"><span data-stu-id="ccc87-200">The property describes a general way that you are able to change the style of the element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="ccc87-201">value</span><span class="sxs-lookup"><span data-stu-id="ccc87-201">value</span></span>**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="ccc87-202">O valor descreve exatamente como o estilo do elemento deve mudar.</span><span class="sxs-lookup"><span data-stu-id="ccc87-202">The value describes exactly how the style of the element should change.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="ccc87-203">Por exemplo, `font-family: 'Courier New', Courier, serif` o navegador dá a seguinte instrução: "definir a fonte dos elementos que correspondem ao padrão `li a` `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-203">For example, `font-family: 'Courier New', Courier, serif` gives the browser the following instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="ccc87-204">Se essa fonte não estiver disponível, use `Courier` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-204">If that font is not available, use `Courier`.</span></span>  <span data-ttu-id="ccc87-205">Se isso não estiver disponível, use `serif` ".</span><span class="sxs-lookup"><span data-stu-id="ccc87-205">If that is not available, use `serif`."</span></span>  

### <span data-ttu-id="ccc87-206">Adicionar vários seletores a um RuleSet</span><span class="sxs-lookup"><span data-stu-id="ccc87-206">Add multiple selectors to a ruleset</span></span>  

<span data-ttu-id="ccc87-207">Um bloco de código CSS, como o que você vê abaixo, é chamado de **RuleSet**.</span><span class="sxs-lookup"><span data-stu-id="ccc87-207">A block of CSS code like what you see below is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="ccc87-208">Conclua as seguintes ações para usar vírgulas para adicionar vários seletores a um RuleSet.</span><span class="sxs-lookup"><span data-stu-id="ccc87-208">Complete the following actions to use commas to add multiple selectors to a ruleset.</span></span>  

1.  <span data-ttu-id="ccc87-209">Na **guia Editor**, abra `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-209">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="ccc87-210">Após o `li a` tipo `, h1` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-210">After `li a` type `, h1`.</span></span>  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    <span data-ttu-id="ccc87-211">O trecho de código anterior informa ao navegador para `<h1>` elementos de estilo da mesma maneira que ele estiliza elementos que correspondem ao padrão `li a` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-211">The previous code snippet tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="ccc87-212">Ir para a **guia ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="ccc87-212">Go to the **live tab**.</span></span>  
1.  <span data-ttu-id="ccc87-213">Escolha o link do **contato** para voltar para a página de contato.</span><span class="sxs-lookup"><span data-stu-id="ccc87-213">Choose the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="ccc87-214">Agora, **entre em contato comigo!**</span><span class="sxs-lookup"><span data-stu-id="ccc87-214">Now, **Contact Me!**</span></span> <span data-ttu-id="ccc87-215">tem a mesma fonte dos links de navegação.</span><span class="sxs-lookup"><span data-stu-id="ccc87-215">has the same font as the navigation links.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="O texto fale comigo!  Agora tem a mesma fonte dos links de página inicial e de contato" lightbox="../media/beginners-css-multiple1.msft.png":::
       <span data-ttu-id="ccc87-218">O texto **fale comigo!**</span><span class="sxs-lookup"><span data-stu-id="ccc87-218">The text **Contact Me!**</span></span> <span data-ttu-id="ccc87-219">Agora tem a mesma fonte dos links de **página inicial** e de **contato**</span><span class="sxs-lookup"><span data-stu-id="ccc87-219">now has the same font as the **Home** and **Contact** links</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ccc87-220">Experimente com o DevTools</span><span class="sxs-lookup"><span data-stu-id="ccc87-220">Experiment with DevTools</span></span>  

<span data-ttu-id="ccc87-221">Ao continuar a viagem para se tornar um especialista no desenvolvimento na Web, você pode descobrir que o CSS é complicado.</span><span class="sxs-lookup"><span data-stu-id="ccc87-221">As you continue your journey to become an expert in web development, you may find that CSS is tricky.</span></span>  <span data-ttu-id="ccc87-222">Você pode escrever um CSS e esperar que ele exiba uma maneira, mas o navegador faz algo completamente diferente.</span><span class="sxs-lookup"><span data-stu-id="ccc87-222">You may write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="ccc87-223">O Microsoft Edge DevTools torna mais fácil experimentar as alterações e ver imediatamente como as alterações afetam a página.</span><span class="sxs-lookup"><span data-stu-id="ccc87-223">Microsoft Edge DevTools makes it easy to experiment with changes and immediately see how the changes affect the page.</span></span>  

### <span data-ttu-id="ccc87-224">Adicionar uma declaração a um rulet existente no DevTools</span><span class="sxs-lookup"><span data-stu-id="ccc87-224">Add a declaration to an existing rulest in DevTools</span></span>  

<span data-ttu-id="ccc87-225">Conclua as ações a seguir para iterar no estilo de um elemento existente, adicionar uma declaração a um RuleSet existente.</span><span class="sxs-lookup"><span data-stu-id="ccc87-225">Complete the following actions to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  

1.  <span data-ttu-id="ccc87-226">Passe o mouse sobre o link **início** , abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="ccc87-226">Hover on the **Home** link, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Inspecionar o link home" lightbox="../media/beginners-css-add1.msft.png":::
       <span data-ttu-id="ccc87-228">Inspecionar o link home</span><span class="sxs-lookup"><span data-stu-id="ccc87-228">Inspect the Home link</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="ccc87-229">O DevTools é aberto juntamente com sua página.</span><span class="sxs-lookup"><span data-stu-id="ccc87-229">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="ccc87-230">O código que representa o link início `<a href="/">Home</a>` é em azul realçado na árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="ccc87-230">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="ccc87-231">O trecho de código e a visualização devem estar familiarizados [com o introdução ao HTML e ao dom][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="ccc87-231">The code snippet and preview should be familiar from [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="ccc87-232">Na figura a seguir, a `font-family: 'Courier New', Courier, serif` declaração que você adicionou anteriormente `contact.html` é vista na guia **estilos** abaixo da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="ccc87-232">In the following figure, the `font-family: 'Courier New', Courier, serif` declaration that you previously added to `contact.html` is seen in the **Styles** tab below the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="A guia estilos está abaixo da árvore DOM" lightbox="../media/beginners-css-add2.msft.png":::
             <span data-ttu-id="ccc87-234">A guia **estilos** está abaixo da árvore DOM</span><span class="sxs-lookup"><span data-stu-id="ccc87-234">The **Styles** tab is below the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="ccc87-235">Se a janela do DevTools for ampla, a guia estilos estará à direita da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="ccc87-235">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="A guia estilos está à direita da árvore DOM" lightbox="../media/beginners-css-add3.msft.png":::
             <span data-ttu-id="ccc87-237">A guia **estilos** está à direita da árvore DOM</span><span class="sxs-lookup"><span data-stu-id="ccc87-237">The **Styles** tab is to the right of the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="ccc87-238">Escolha a linha vazia abaixo `font-family: 'Courier New', Courier, Serif` para adicionar uma nova declaração.</span><span class="sxs-lookup"><span data-stu-id="ccc87-238">Choose the empty line below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Adicionar uma nova declaração" lightbox="../media/beginners-css-add4.msft.png":::
       <span data-ttu-id="ccc87-240">Adicionar uma nova declaração</span><span class="sxs-lookup"><span data-stu-id="ccc87-240">Add a new declaration</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-241">Digite `color` e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-241">Type `color` and select `Enter`.</span></span>  <span data-ttu-id="ccc87-242">A interface do usuário de AutoCompletar sugere opções à medida que você digita.</span><span class="sxs-lookup"><span data-stu-id="ccc87-242">The autocomplete UI suggests options as you type.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Cor do tipo" lightbox="../media/beginners-css-add5.msft.png":::
       <span data-ttu-id="ccc87-244">Tipo</span><span class="sxs-lookup"><span data-stu-id="ccc87-244">Type</span></span> `color`  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-245">Digite `magenta` e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-245">Type `magenta` and select `Enter`.</span></span>  <span data-ttu-id="ccc87-246">Todo o texto na página de contato agora é magenta.</span><span class="sxs-lookup"><span data-stu-id="ccc87-246">All of the text on the contact page is now magenta.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Digite magenta" lightbox="../media/beginners-css-add6.msft.png":::
       <span data-ttu-id="ccc87-248">Tipo</span><span class="sxs-lookup"><span data-stu-id="ccc87-248">Type</span></span> `magenta`  
    :::image-end:::  
    
### <span data-ttu-id="ccc87-249">Editar uma declaração no DevTools</span><span class="sxs-lookup"><span data-stu-id="ccc87-249">Edit a declaration in DevTools</span></span>  

<span data-ttu-id="ccc87-250">Conclua as seguintes ações para editar as declarações existentes no DevTools.</span><span class="sxs-lookup"><span data-stu-id="ccc87-250">Complete the following actions to edit existing declarations in DevTools.</span></span>  

1.  <span data-ttu-id="ccc87-251">Escolha o quadrado magenta ao lado de `magenta` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-251">Choose the magenta square next to `magenta`.</span></span>  <span data-ttu-id="ccc87-252">Um seletor de cores aparece.</span><span class="sxs-lookup"><span data-stu-id="ccc87-252">A color picker pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="O seletor de cores" lightbox="../media/beginners-css-edit1.msft.png":::
       <span data-ttu-id="ccc87-254">O seletor de cores</span><span class="sxs-lookup"><span data-stu-id="ccc87-254">The Color Picker</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-255">Use o seletor de cores para alterar o texto da fonte para uma cor que você quiser.</span><span class="sxs-lookup"><span data-stu-id="ccc87-255">Use the color picker to change the font text to a color that you like.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Alterar a cor da fonte para roxo com o seletor de cores" lightbox="../media/beginners-css-edit2.msft.png":::
       <span data-ttu-id="ccc87-257">Alterar a cor da fonte para roxo com o seletor de cores</span><span class="sxs-lookup"><span data-stu-id="ccc87-257">Change the font color to purple with the Color Picker</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="ccc87-258">Adicionar um novo RuleSet no DevTools</span><span class="sxs-lookup"><span data-stu-id="ccc87-258">Add a new ruleset in DevTools</span></span>  

<span data-ttu-id="ccc87-259">Conclua as seguintes ações para adicionar novos RuleSets ao DevTools.</span><span class="sxs-lookup"><span data-stu-id="ccc87-259">Complete the following actions to add new rulesets in DevTools.</span></span>  

1.  <span data-ttu-id="ccc87-260">Escolha **novo regra de estilo** \ ( ![ nova regra ][ImageNewStyleRuleIcon] de estilo \) que é ao lado de **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="ccc87-260">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) which is next to **.cls**.</span></span>  <span data-ttu-id="ccc87-261">Um RuleSet vazio aparece `a` como o seletor.</span><span class="sxs-lookup"><span data-stu-id="ccc87-261">An empty ruleset appears with `a` as the selector.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Adicionar uma nova regra" lightbox="../media/beginners-css-rule1.msft.png":::
       <span data-ttu-id="ccc87-263">Adicionar uma nova regra</span><span class="sxs-lookup"><span data-stu-id="ccc87-263">Add a new rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-264">Substituir `a` por `a:hover` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-264">Replace `a` with `a:hover`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Substituir por a:hover" lightbox="../media/beginners-css-rule2.msft.png":::
       <span data-ttu-id="ccc87-266">Substituir `a` por</span><span class="sxs-lookup"><span data-stu-id="ccc87-266">Replace `a` with</span></span> `a:hover`  
    :::image-end:::  
    
    `:hover` <span data-ttu-id="ccc87-267">é uma **pseudo-classe**.</span><span class="sxs-lookup"><span data-stu-id="ccc87-267">is a **pseudo-class**.</span></span>  <span data-ttu-id="ccc87-268">Use pseudovariáveis para elementos de estilo que podem inserir Estados especiais.</span><span class="sxs-lookup"><span data-stu-id="ccc87-268">Use pseudo-classes for style elements that may enter special states.</span></span>  <span data-ttu-id="ccc87-269">Por exemplo, o `a:hover` estilo somente tem efeito quando você estiver passando o mouse sobre um `<a>` elemento.</span><span class="sxs-lookup"><span data-stu-id="ccc87-269">For example, the `a:hover` style only takes effect when you are hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="ccc87-270">Escolha entre os colchetes para adicionar uma nova declaração.</span><span class="sxs-lookup"><span data-stu-id="ccc87-270">Choose between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="ccc87-271">Digite `background-color` o nome da declaração e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-271">Type `background-color` for the declaration name and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Digite a cor da tela de fundo" lightbox="../media/beginners-css-rule3.msft.png":::
       <span data-ttu-id="ccc87-273">Tipo</span><span class="sxs-lookup"><span data-stu-id="ccc87-273">Type</span></span> `background-color`  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-274">Digite `green` o valor da declaração e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-274">Type `green` for the declaration value and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Digite verde" lightbox="../media/beginners-css-rule4.msft.png":::
       <span data-ttu-id="ccc87-276">Tipo</span><span class="sxs-lookup"><span data-stu-id="ccc87-276">Type</span></span> `green`  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-277">Passe o mouse sobre o link **início** .</span><span class="sxs-lookup"><span data-stu-id="ccc87-277">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="ccc87-278">O plano de fundo do link fica verde.</span><span class="sxs-lookup"><span data-stu-id="ccc87-278">The background of the link turns green.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Passe o mouse sobre o link home para revelar o plano de fundo verde" lightbox="../media/beginners-css-rule5.msft.png":::
       <span data-ttu-id="ccc87-280">Passe o mouse sobre o link home para revelar o plano de fundo verde</span><span class="sxs-lookup"><span data-stu-id="ccc87-280">Hover over the Home link to reveal its green background</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ccc87-281">Reutilizar estilos em páginas com folhas de estilo externas</span><span class="sxs-lookup"><span data-stu-id="ccc87-281">Re-use styles across pages with external stylesheets</span></span>  

<span data-ttu-id="ccc87-282">Em uma etapa anterior, você adicionou o trecho de código a seguir como uma folha de estilos interna `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-282">In a previous step, you added the following code snippet as an internal stylesheet to `contact.html`.</span></span>  

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

<span data-ttu-id="ccc87-283">E se você quisesse estilizar `index.html` da mesma maneira?</span><span class="sxs-lookup"><span data-stu-id="ccc87-283">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="ccc87-284">E se você tivesse um grande número de páginas para as quais você deseja aplicar seus estilos?</span><span class="sxs-lookup"><span data-stu-id="ccc87-284">What if you had a large number of pages to which you wanted to apply your styles?</span></span>  <span data-ttu-id="ccc87-285">Você precisaria copiar e colar a folha de estilos interna em cada página da Web em seu site.</span><span class="sxs-lookup"><span data-stu-id="ccc87-285">You would have to copy and paste the internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="ccc87-286">Conclua as ações a seguir para adicionar uma **folha de estilos externa** para permitir que você escreva sua CSS uma vez e a aplique em várias páginas.</span><span class="sxs-lookup"><span data-stu-id="ccc87-286">Complete the following actions to add an **External stylesheet** to allow you to write your CSS once and apply it to multiple pages.</span></span>  

1.  <span data-ttu-id="ccc87-287">Primeiro, recarregue a guia ao vivo para remover as alterações feitas no DevTools.</span><span class="sxs-lookup"><span data-stu-id="ccc87-287">First, reload the live tab to remove the changes that you made in DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" Depois de atualizar a página, as alterações que foram feitas no DevTools são perdidas" lightbox="../media/beginners-css-external1.msft.png":::
        <span data-ttu-id="ccc87-289">Depois de atualizar a página, as alterações que foram feitas no DevTools são perdidas</span><span class="sxs-lookup"><span data-stu-id="ccc87-289">After you refresh the page, the changes that were made in DevTools are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-290">Volte para a **guia Editor** e abra `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-290">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       <span data-ttu-id="ccc87-292">contact.html</span><span class="sxs-lookup"><span data-stu-id="ccc87-292">contact.html</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-293">Exclua tudo entre `<style>` e `</style>` , incluindo `<style>` e `</style>` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-293">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="A marca de estilo foi removida" lightbox="../media/beginners-css-external3.msft.png":::
       <span data-ttu-id="ccc87-295">A marca de estilo foi removida</span><span class="sxs-lookup"><span data-stu-id="ccc87-295">The style tag has been removed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-296">Vá para `index.html` e remova `style="background-color: aliceblue;"` da `<nav>` marca.</span><span class="sxs-lookup"><span data-stu-id="ccc87-296">Go to `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="ccc87-297">Você já removeu toda a CSS que você adicionou anteriormente ao seu site.</span><span class="sxs-lookup"><span data-stu-id="ccc87-297">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="O estilo embutido foi removido do elemento NAV" lightbox="../media/beginners-css-external4.msft.png":::
       <span data-ttu-id="ccc87-299">O estilo embutido foi removido do elemento NAV</span><span class="sxs-lookup"><span data-stu-id="ccc87-299">The inline style has been removed from the nav element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-300">Escolha **novo arquivo**.</span><span class="sxs-lookup"><span data-stu-id="ccc87-300">Choose **New File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="A caixa de diálogo novo arquivo" lightbox="../media/beginners-css-external5.msft.png":::
       <span data-ttu-id="ccc87-302">A caixa de diálogo novo arquivo</span><span class="sxs-lookup"><span data-stu-id="ccc87-302">The new file dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-303">Substituir `cool-file.js` por `style.css` e escolha **Adicionar arquivo**.</span><span class="sxs-lookup"><span data-stu-id="ccc87-303">Replace `cool-file.js` with `style.css` and choose **Add File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Estilo de tipo. css" lightbox="../media/beginners-css-external6.msft.png":::
       <span data-ttu-id="ccc87-305">Tipo</span><span class="sxs-lookup"><span data-stu-id="ccc87-305">Type</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-306">Adicione o trecho de código a seguir ao seu `style.css` arquivo.</span><span class="sxs-lookup"><span data-stu-id="ccc87-306">Add the following code snippet to your `style.css` file.</span></span>  
    
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
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Adicionar código ao Style. css" lightbox="../media/beginners-css-external7.msft.png":::
       <span data-ttu-id="ccc87-308">Adicionar código a</span><span class="sxs-lookup"><span data-stu-id="ccc87-308">Add code to</span></span> `style.css`  
    :::image-end:::  
    
    <span data-ttu-id="ccc87-309">Certifique-se de que você criou uma folha de estilos externa.</span><span class="sxs-lookup"><span data-stu-id="ccc87-309">Ensure that you have created an external stylesheet.</span></span> <span data-ttu-id="ccc87-310">O HTML não está ciente de que ele existe.</span><span class="sxs-lookup"><span data-stu-id="ccc87-310">Your HTML is not aware that it exists.</span></span>  
    
1.  <span data-ttu-id="ccc87-311">Abrir `index.html` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-311">Open `index.html`.</span></span>  
1.  <span data-ttu-id="ccc87-312">Adicione `<link rel="stylesheet" href="style.css">` ao seu HTML.</span><span class="sxs-lookup"><span data-stu-id="ccc87-312">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Link para estilo. css" lightbox="../media/beginners-css-external8.msft.png":::
       <span data-ttu-id="ccc87-314">Link para</span><span class="sxs-lookup"><span data-stu-id="ccc87-314">Link to</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-315">Abra o `contact.html` arquivo e adicione o link ali.</span><span class="sxs-lookup"><span data-stu-id="ccc87-315">Open the `contact.html` file and add the link there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Link para estilo. CSS em contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       <span data-ttu-id="ccc87-317">Link para `style.css` em</span><span class="sxs-lookup"><span data-stu-id="ccc87-317">Link to `style.css` in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-318">Ir para a **guia ao vivo**.  A Home Page agora tem a mesma fonte da última seção e uma seção azul de navegação.</span><span class="sxs-lookup"><span data-stu-id="ccc87-318">Go to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="A Home Page" lightbox="../media/beginners-css-external10.msft.png":::
       <span data-ttu-id="ccc87-320">A Home Page</span><span class="sxs-lookup"><span data-stu-id="ccc87-320">The home page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-321">Escolha o link do **contato** para acessar a página do contato.</span><span class="sxs-lookup"><span data-stu-id="ccc87-321">Choose the **Contact** link to go to the contact page.</span></span>  <span data-ttu-id="ccc87-322">A página de contato tem a mesma formatação que a Home Page.</span><span class="sxs-lookup"><span data-stu-id="ccc87-322">The contact page has the same formatting as the home page.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="Página de contato" lightbox="../media/beginners-css-external11.msft.png":::
       <span data-ttu-id="ccc87-324">Página de contato</span><span class="sxs-lookup"><span data-stu-id="ccc87-324">The contact page</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ccc87-325">Usar uma estrutura CSS</span><span class="sxs-lookup"><span data-stu-id="ccc87-325">Use a CSS framework</span></span>  

<span data-ttu-id="ccc87-326">**Estruturas CSS** são coleções de estilos criados por outros desenvolvedores que facilitam a criação de sites atraentes.</span><span class="sxs-lookup"><span data-stu-id="ccc87-326">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="ccc87-327">Em vez de definir estilos por conta própria, uma estrutura fornece um conjunto de estilos que você pode usar em seus elementos de página.</span><span class="sxs-lookup"><span data-stu-id="ccc87-327">Instead of defining styles yourself, a framework provides you a collection of styles that you are able to use on your page elements.</span></span>  

1.  <span data-ttu-id="ccc87-328">Copie o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="ccc87-328">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="ccc87-329">Vá para a guia edição e cole o código em `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-329">Go to the editing tab and paste the code into `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Link para a estrutura em contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       <span data-ttu-id="ccc87-331">Link para a estrutura em</span><span class="sxs-lookup"><span data-stu-id="ccc87-331">Link to the framework in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-332">Abra o `index.html` arquivo e adicione o código.</span><span class="sxs-lookup"><span data-stu-id="ccc87-332">Open the `index.html` file and add the code there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Link para a estrutura em index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       <span data-ttu-id="ccc87-334">Link para a estrutura em</span><span class="sxs-lookup"><span data-stu-id="ccc87-334">Link to the framework in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-335">Volte para a guia ao vivo para ver suas alterações.</span><span class="sxs-lookup"><span data-stu-id="ccc87-335">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="ccc87-336">Enquanto a cor da tela de fundo do `<nav>` elemento e a fonte `<li>` dos `<a>` elementos e são iguais, a fonte dos outros elementos mudava.</span><span class="sxs-lookup"><span data-stu-id="ccc87-336">While the background color of the `<nav>` element and the font of the `<li>` and `<a>` elements are the same, the font of the other elements has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Parte da fonte na página inicial foi alterada por causa da estrutura" lightbox="../media/beginners-css-framework3.msft.png":::
       <span data-ttu-id="ccc87-338">Parte da fonte na página inicial foi alterada por causa da estrutura</span><span class="sxs-lookup"><span data-stu-id="ccc87-338">Some of the font on the home page changed because of the framework</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="ccc87-339">Usar uma classe</span><span class="sxs-lookup"><span data-stu-id="ccc87-339">Use a class</span></span>  

<span data-ttu-id="ccc87-340">Na última seção, você adicionou a inicialização às páginas da Web, o que altera as fontes de alguns dos elementos do seu site.</span><span class="sxs-lookup"><span data-stu-id="ccc87-340">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="ccc87-341">As estruturas CSS ajudam você a fazer alterações importantes na sua página com um pouco de código.</span><span class="sxs-lookup"><span data-stu-id="ccc87-341">CSS frameworks help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="ccc87-342">Conclua as ações a seguir para alterar o cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="ccc87-342">Complete the following actions to change your header.</span></span>  

1.  <span data-ttu-id="ccc87-343">Copie o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="ccc87-343">Copy the following code snippet.</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="ccc87-344">Adicione o trecho de código anterior à sua `<header>` marca `index.html` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-344">Add the previous code snippet to your `<header>` tag in `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Adicionar classes no index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       <span data-ttu-id="ccc87-346">Adicionar classes em</span><span class="sxs-lookup"><span data-stu-id="ccc87-346">Add classes in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-347">Adicione o código à sua `<header>` marca `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-347">Add the code to your `<header>` tag in `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Adicionar classes no contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       <span data-ttu-id="ccc87-349">Adicionar classes em</span><span class="sxs-lookup"><span data-stu-id="ccc87-349">Add classes in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-350">Exiba suas alterações na guia ao vivo.  Há uma grande caixa cinza em torno do seu cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="ccc87-350">View your changes in the live tab.  There is a big, grey box around your header.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="Agora o cabeçalho tem uma grande caixa cinza ao seu lado" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       <span data-ttu-id="ccc87-352">Agora o cabeçalho tem uma grande caixa cinza ao seu lado</span><span class="sxs-lookup"><span data-stu-id="ccc87-352">The header now has a big, grey box around it</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="ccc87-353">Compreender classes</span><span class="sxs-lookup"><span data-stu-id="ccc87-353">Understand classes</span></span>  

<span data-ttu-id="ccc87-354">As classes permitem atribuir coleções de estilos a elementos arbitrários.</span><span class="sxs-lookup"><span data-stu-id="ccc87-354">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="ccc87-355">Use o trecho de código a seguir para aplicar vários estilos ao `<header>` elemento depois de definir o `class` atributo para `jumbotron` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-355">Use the following code snippet to apply several styles to the `<header>` element after you set the `class` attribute to `jumbotron`.</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="ccc87-356">Uma vantagem de uma classe é permitir que você aplique estilos a qualquer elemento desejado.</span><span class="sxs-lookup"><span data-stu-id="ccc87-356">One advantage of a class is that it lets you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="ccc87-357">Por exemplo, suponha que você queira definir a cor da tela de fundo de alguns `<p>` elementos como roxo, mas não todos os `<p>` elementos.</span><span class="sxs-lookup"><span data-stu-id="ccc87-357">For example, suppose you want to set the background color of some `<p>` elements to purple, but not all `<p>` elements.</span></span>  <span data-ttu-id="ccc87-358">Use o trecho de código a seguir para definir o estilo em uma classe.</span><span class="sxs-lookup"><span data-stu-id="ccc87-358">Use the following code snippet to define the style in a class.</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="ccc87-359">Em seguida, aplique a classe somente aos `<p>` elementos que você deseja aplicar o estilo.</span><span class="sxs-lookup"><span data-stu-id="ccc87-359">Next, apply the class to only the `<p>` elements that you want to style.</span></span>  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### <span data-ttu-id="ccc87-360">Alinhar elementos</span><span class="sxs-lookup"><span data-stu-id="ccc87-360">Align elements</span></span>  

<span data-ttu-id="ccc87-361">Conclua as ações a seguir para inicializar e fornecer classes para alinhar elementos.</span><span class="sxs-lookup"><span data-stu-id="ccc87-361">Complete the following actions to bootstrap and provide classes for aligning elements.</span></span>  

1.  <span data-ttu-id="ccc87-362">Volte para a guia Editor e abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-362">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="ccc87-363">Adicionar `class="container-fluid"` à sua `<body>` marca.</span><span class="sxs-lookup"><span data-stu-id="ccc87-363">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Adicionar a classe container-fluido" lightbox="../media/beginners-css-align1.msft.png":::
       <span data-ttu-id="ccc87-365">Adicionar a `container-fluid` classe</span><span class="sxs-lookup"><span data-stu-id="ccc87-365">Add the `container-fluid` class</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-366">Envolver seus `<nav>` `<main>` elementos e em `<div class="row">` .</span><span class="sxs-lookup"><span data-stu-id="ccc87-366">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="ccc87-367">Certifique-se de colocar `</div>` após para `</main>` fechar corretamente a nova marca.</span><span class="sxs-lookup"><span data-stu-id="ccc87-367">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Adicionar uma linha" lightbox="../media/beginners-css-align2.msft.png":::
       <span data-ttu-id="ccc87-369">Adicionar uma linha</span><span class="sxs-lookup"><span data-stu-id="ccc87-369">Add a row</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-370">Adicione `class="col-3"` à sua `<nav>` marca e `class="col-9"` à sua `<main>` marca.</span><span class="sxs-lookup"><span data-stu-id="ccc87-370">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Adicionar as classes Col-3 e col-9" lightbox="../media/beginners-css-align3.msft.png":::
       <span data-ttu-id="ccc87-372">Adicionar as `col-3` `col-9` classes e</span><span class="sxs-lookup"><span data-stu-id="ccc87-372">Add the `col-3` and `col-9` classes</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ccc87-373">Exiba suas alterações na guia ao vivo.</span><span class="sxs-lookup"><span data-stu-id="ccc87-373">View your changes in the live tab.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="O conteúdo de NAV agora está à esquerda do conteúdo principal" lightbox="../media/beginners-css-align4.msft.png":::
       <span data-ttu-id="ccc87-375">O conteúdo de NAV agora está à esquerda do conteúdo principal</span><span class="sxs-lookup"><span data-stu-id="ccc87-375">The nav content is now to the left of the main content</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ccc87-376">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="ccc87-376">Next steps</span></span>  

<span data-ttu-id="ccc87-377">Parabéns! você concluiu.</span><span class="sxs-lookup"><span data-stu-id="ccc87-377">Congratulations, you are done.</span></span>  

*   <span data-ttu-id="ccc87-378">A melhor maneira de ficar melhor no desenvolvimento na Web é criar mais sites.</span><span class="sxs-lookup"><span data-stu-id="ccc87-378">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="ccc87-379">Não se preocupe com as coisas quebradas.</span><span class="sxs-lookup"><span data-stu-id="ccc87-379">Do not worry about breaking stuff.</span></span>  <span data-ttu-id="ccc87-380">Só Divirta-se e saiba o máximo possível ao longo do caminho.</span><span class="sxs-lookup"><span data-stu-id="ccc87-380">Just have fun and learn as much as possible along the way.</span></span>  
*   <span data-ttu-id="ccc87-381">Para saber mais sobre o estilo de páginas da Web, consulte [introdução ao CSS][MDNCssFirstSteps].</span><span class="sxs-lookup"><span data-stu-id="ccc87-381">To learn more about styling web pages, see [Introduction to CSS][MDNCssFirstSteps].</span></span>  
*   <span data-ttu-id="ccc87-382">Para saber mais sobre como usar o DevTools para experimentar a CSS de uma página, confira [introdução ao modo de exibição e alteração de CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="ccc87-382">To learn more about how to use DevTools to experiment with the CSS of a page, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<!--- image links --->  

[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools para iniciantes: introdução ao HTML e ao DOM | Documentos da Microsoft"  
[DevtoolsCssIndex]: ../css/index.md "Introdução ao visualizar e alterar CSS | Documentos da Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-cozinhá-Amphibian | Problema"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Primeiras etapas da CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="ccc87-388">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="ccc87-388">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ccc87-389">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/beginners/css) e é criada pela [Katherine Jackson][KatherineJackson] \ (redatora técnica, Chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="ccc87-389">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ccc87-391">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ccc87-391">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
