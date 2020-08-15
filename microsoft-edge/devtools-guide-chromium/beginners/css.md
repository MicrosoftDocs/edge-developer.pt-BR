---
title: 'DevTools para iniciantes: introdução ao CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 6e005f4107764a13934f0c8f3b3cde0ab9bf98c2
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931546"
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

# <span data-ttu-id="28138-103">DevTools para iniciantes: introdução ao CSS</span><span class="sxs-lookup"><span data-stu-id="28138-103">DevTools for beginners: Get started with CSS</span></span>  

<span data-ttu-id="28138-104">Neste tutorial, você aprenderá a usar CSS para estilizar uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="28138-104">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="28138-105">Você também aprenderá a usar o Microsoft Edge DevTools para experimentar alterações de CSS.</span><span class="sxs-lookup"><span data-stu-id="28138-105">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="28138-106">O artigo a seguir é o segundo tutorial em uma série de tutoriais que ensina a você noções básicas sobre o desenvolvimento da Web e o Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="28138-106">The following article is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="28138-107">Na verdade, você ganha experiência prática ao criar seu próprio website.</span><span class="sxs-lookup"><span data-stu-id="28138-107">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="28138-108">Você não precisa concluir o primeiro tutorial antes de seguir o segundo.</span><span class="sxs-lookup"><span data-stu-id="28138-108">You do not have to complete the first tutorial before following the second.</span></span>  <span data-ttu-id="28138-109">[Configurar seu código](#set-up-your-code) mostra como fazer a configuração.</span><span class="sxs-lookup"><span data-stu-id="28138-109">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="28138-110">Este tutorial foi projetado para principiantes absolutos e se concentra nos **fundamentos do desenvolvimento na Web** e nas noções básicas de como usar o devtools para experimentar com CSS.</span><span class="sxs-lookup"><span data-stu-id="28138-110">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="28138-111">Se você quiser um tutorial que só se concentre no DevTools, confira [introdução e alterar CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="28138-111">If you want a tutorial that only focuses on DevTools, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="28138-112">No início do tutorial, o seu site deve ter a aparência da figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="28138-112">At the beginning of the tutorial, your site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Qual é a aparência de seu site" lightbox="../media/beginners-css-intro1.msft.png":::
   <span data-ttu-id="28138-114">Qual é a aparência de seu site</span><span class="sxs-lookup"><span data-stu-id="28138-114">What your site currently looks like</span></span>  
:::image-end:::  

<span data-ttu-id="28138-115">Depois de concluir o tutorial, o site deve ter a aparência da figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="28138-115">After you complete the tutorial, you site should look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Qual deve ser a aparência de seu site no final do tutorial" lightbox="../media/beginners-css-intro2.msft.png":::
   <span data-ttu-id="28138-117">Qual deve ser a aparência de seu site no final do tutorial</span><span class="sxs-lookup"><span data-stu-id="28138-117">What your site should look like at the end of the tutorial</span></span>  
:::image-end:::  

## <span data-ttu-id="28138-118">Goal</span><span class="sxs-lookup"><span data-stu-id="28138-118">Goals</span></span>  

<span data-ttu-id="28138-119">Siga este tutorial para compreender melhor os conceitos e tarefas a seguir.</span><span class="sxs-lookup"><span data-stu-id="28138-119">Follow this tutorial to better understand the following concepts and tasks.</span></span>  

*   <span data-ttu-id="28138-120">Como usar CSS para estilizar uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="28138-120">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="28138-121">Como usar o Microsoft Edge DevTools para experimentar com CSS.</span><span class="sxs-lookup"><span data-stu-id="28138-121">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="28138-122">A diferença entre estruturas CSS e CSS.</span><span class="sxs-lookup"><span data-stu-id="28138-122">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="28138-123">Você está criando um site real.</span><span class="sxs-lookup"><span data-stu-id="28138-123">You are building a real website.</span></span>  

## <span data-ttu-id="28138-124">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="28138-124">Prerequisites</span></span>  

<span data-ttu-id="28138-125">Antes de tentar este tutorial, complete os pré-requisitos a seguir.</span><span class="sxs-lookup"><span data-stu-id="28138-125">Before attempting this tutorial, complete the following prerequisites.</span></span>  

*   <span data-ttu-id="28138-126">Conclua [a introdução ao HTML e ao dom][DevtoolsBeginnersHtml] ou certifique-se de ter uma compreensão do HTML e do dom semelhante ao que é ensinado nesse tutorial.</span><span class="sxs-lookup"><span data-stu-id="28138-126">Complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what is taught in that tutorial.</span></span>  
*   <span data-ttu-id="28138-127">Baixar o navegador da Web [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="28138-127">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="28138-128">O tutorial a seguir usa um conjunto de ferramentas de desenvolvimento da Web, chamado de Microsoft Edge DevTools, incorporado ao Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="28138-128">The following tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="28138-129">Configurar seu código</span><span class="sxs-lookup"><span data-stu-id="28138-129">Set up your code</span></span>  

<span data-ttu-id="28138-130">Para criar seu site, primeiro você deve concluir as seguintes ações para configurar o código.</span><span class="sxs-lookup"><span data-stu-id="28138-130">To create your site, you must first complete the following actions to set up your code.</span></span>  

> [!NOTE]
> <span data-ttu-id="28138-131">Se você já concluiu o primeiro tutorial da série, pule para a próxima seção.</span><span class="sxs-lookup"><span data-stu-id="28138-131">If you have already completed the first tutorial in the series, skip to the next section.</span></span>  <span data-ttu-id="28138-132">Continue usando o código do último tutorial, [introdução ao HTML e ao dom][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="28138-132">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  

1.  <span data-ttu-id="28138-133">Abra o [código-fonte][GlitchCookedAmphibianIndex].</span><span class="sxs-lookup"><span data-stu-id="28138-133">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="28138-134">A guia in-Focus do seu navegador é referenciada como a **guia edição**.</span><span class="sxs-lookup"><span data-stu-id="28138-134">The in-focus tab of your browser is referenced as the **editing tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="A guia edição" lightbox="../media/beginners-css-setup1.msft.png":::
       <span data-ttu-id="28138-136">A guia **edição**</span><span class="sxs-lookup"><span data-stu-id="28138-136">The **editing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-137">Escolha **cozinhá-Amphibian**.</span><span class="sxs-lookup"><span data-stu-id="28138-137">Choose **cooked-amphibian**.</span></span>  <span data-ttu-id="28138-138">Um menu é exibido.</span><span class="sxs-lookup"><span data-stu-id="28138-138">A menu pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="O menu opções do Project" lightbox="../media/beginners-css-setup2.msft.png":::
       <span data-ttu-id="28138-140">O menu opções do Project</span><span class="sxs-lookup"><span data-stu-id="28138-140">The Project Options menu</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="28138-141">Escolha **projeto remix**.</span><span class="sxs-lookup"><span data-stu-id="28138-141">Choose **Remix Project**.</span></span>  <span data-ttu-id="28138-142">Falha cria uma cópia do projeto que você pode editar.</span><span class="sxs-lookup"><span data-stu-id="28138-142">Glitch creates a copy of the project that you are able to edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="28138-143">A falha gera um nome aleatório para o novo projeto.</span><span class="sxs-lookup"><span data-stu-id="28138-143">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="28138-144">Escolha **Mostrar** e selecione **em uma nova janela**.</span><span class="sxs-lookup"><span data-stu-id="28138-144">Choose **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="28138-145">Outra guia abre com uma visualização dinâmica do seu site.</span><span class="sxs-lookup"><span data-stu-id="28138-145">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="28138-146">A guia em foco do seu navegador é referenciada como a **guia ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="28138-146">The in-focus tab of your browser is referenced as the **live tab**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="A guia ao vivo" lightbox="../media/beginners-css-setup3.msft.png":::
       <span data-ttu-id="28138-148">A **guia ao vivo**</span><span class="sxs-lookup"><span data-stu-id="28138-148">The **live tab**</span></span>  
    :::image-end:::  

## <span data-ttu-id="28138-149">Entender CSS</span><span class="sxs-lookup"><span data-stu-id="28138-149">Understand CSS</span></span>  

<span data-ttu-id="28138-150">**CSS** é um idioma de computador que determina o layout e o estilo de páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="28138-150">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="28138-151">A figura a seguir é um parágrafo com uma borda.</span><span class="sxs-lookup"><span data-stu-id="28138-151">The following figure is a paragraph with a border.</span></span>  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="O texto foi estilizado com CSS" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   <span data-ttu-id="28138-153">O texto foi estilizado com CSS</span><span class="sxs-lookup"><span data-stu-id="28138-153">The text has been styled with CSS</span></span>  
:::image-end:::  

<span data-ttu-id="28138-154">O trecho de código a seguir é o código HTML e CSS usado para criar o parágrafo na figura anterior.</span><span class="sxs-lookup"><span data-stu-id="28138-154">The following code snippet is the HTML and CSS code used to create the paragraph in the previous figure.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="28138-155">Provavelmente parece novidade para você.</span><span class="sxs-lookup"><span data-stu-id="28138-155">probably looks new to you.</span></span>  <span data-ttu-id="28138-156">O restante deve parecer familiar.</span><span class="sxs-lookup"><span data-stu-id="28138-156">The rest should look familiar.</span></span>  <span data-ttu-id="28138-157">Caso contrário, conclua a [introdução com HTML e o dom][DevtoolsBeginnersHtml] antes de tentar as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="28138-157">If not, complete [Get Started with HTML and the DOM][DevtoolsBeginnersHtml] before attempting the following sections.</span></span>  

## <span data-ttu-id="28138-158">Adicionar estilos em linha</span><span class="sxs-lookup"><span data-stu-id="28138-158">Add inline styles</span></span>  

<span data-ttu-id="28138-159">Conclua as ações a seguir para usar **estilos embutidos** para aplicar estilos a um único elemento.</span><span class="sxs-lookup"><span data-stu-id="28138-159">Complete the following actions to use **inline styles** to apply styles to a single element.</span></span>  

1.  <span data-ttu-id="28138-160">Volte para a guia edição e abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="28138-160">Go back to the editing tab and open `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       <span data-ttu-id="28138-162">Abrir `index.html` na guia edição</span><span class="sxs-lookup"><span data-stu-id="28138-162">Open `index.html` in the editing tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-163">Adicionar `style="background-color: aliceblue;"` à sua `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="28138-163">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="28138-164">No bloco de código abaixo, a quarta linha de código é aquela que você precisa alterar.</span><span class="sxs-lookup"><span data-stu-id="28138-164">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="28138-165">O restante está apenas lá, portanto, você pode garantir que está colocando o novo código no lugar certo.</span><span class="sxs-lookup"><span data-stu-id="28138-165">The rest is just there, so you are able to ensure that you are putting the new code in the right place.</span></span>  
    
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
    
1.  <span data-ttu-id="28138-166">Vá para a **guia ao vivo** para ver as alterações!</span><span class="sxs-lookup"><span data-stu-id="28138-166">Go to the **live tab** to see the changes!</span></span>  <span data-ttu-id="28138-167">O plano de fundo da `<nav>` seção agora está em azul.</span><span class="sxs-lookup"><span data-stu-id="28138-167">The background of the `<nav>` section is now blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="A cor do plano de fundo por trás da página inicial e dos links de contatos agora está azul" lightbox="../media/beginners-css-inline2.msft.png":::
       <span data-ttu-id="28138-169">A cor do plano de fundo por trás da **página inicial** e dos links de **contatos** agora está azul</span><span class="sxs-lookup"><span data-stu-id="28138-169">The background color behind the **Home** and **Contact** links is now blue</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="28138-170">Reutilizar estilos em uma única página com folhas de estilos internas</span><span class="sxs-lookup"><span data-stu-id="28138-170">Re-use styles on a single page with internal stylesheets</span></span>  

<span data-ttu-id="28138-171">Em um trecho de código anterior, um estilo embutido aplicou um estilo a uma única `<p>` marca.</span><span class="sxs-lookup"><span data-stu-id="28138-171">In a previous code snippet, an inline style applied a style to a single `<p>` tag.</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="28138-172">E se você quiser que todos os `<p>` elementos na sua página da Web tenham o estilo da mesma maneira?</span><span class="sxs-lookup"><span data-stu-id="28138-172">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="28138-173">Você precisaria copiar e colar o código em cada marca única `<p>` do seu site.</span><span class="sxs-lookup"><span data-stu-id="28138-173">You would have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="28138-174">Isso é muito tempo e esforço.</span><span class="sxs-lookup"><span data-stu-id="28138-174">That is a lot of time and effort.</span></span>  <span data-ttu-id="28138-175">E, se precisar fazer uma edição, você precisaria alterar todas as marcas novamente.</span><span class="sxs-lookup"><span data-stu-id="28138-175">And, if you needed to make an edit, you would have to change every tag again.</span></span>  <span data-ttu-id="28138-176">Conclua as ações a seguir para usar uma **folha de estilos interna** para escrever seu CSS uma vez para que ele se aplique a vários elementos.</span><span class="sxs-lookup"><span data-stu-id="28138-176">Complete the following actions to use an **Internal stylesheet** to write your CSS once so that it applies to multiple elements.</span></span>  

1.  <span data-ttu-id="28138-177">Na guia ao vivo, escolha **contato** para acessar a página do contato.</span><span class="sxs-lookup"><span data-stu-id="28138-177">In the live tab, choose **Contact** to go to the contact page.</span></span>  <span data-ttu-id="28138-178">Observe a fonte de **casa** e do **contato**.</span><span class="sxs-lookup"><span data-stu-id="28138-178">Notice the font of **Home** and **Contact**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="Página de contato" lightbox="../media/beginners-css-internal1.msft.png":::
       <span data-ttu-id="28138-180">Página de contato</span><span class="sxs-lookup"><span data-stu-id="28138-180">The Contact page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-181">Na **guia Editor**, vá para `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="28138-181">In the **editor tab**, go to `contact.html`.</span></span>  
1.  <span data-ttu-id="28138-182">Adicione o código a seguir a `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="28138-182">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="28138-183">Lembre-se de que as linhas começando com `<style>` e terminando `</style>` são o que você precisa adicionar.</span><span class="sxs-lookup"><span data-stu-id="28138-183">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="28138-184">O outro código está aqui para que você saiba onde colocar o novo código.</span><span class="sxs-lookup"><span data-stu-id="28138-184">The other code is just there so you know where to put the new code.</span></span>  
    
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
    
1.  <span data-ttu-id="28138-185">Volte para a **guia ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="28138-185">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="28138-186">Escolha **contato** para voltar para a página de contato.</span><span class="sxs-lookup"><span data-stu-id="28138-186">Choose **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="28138-187">A fonte de **casa** e o **contato** foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="28138-187">The font of **Home** and **Contact** has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="A fonte dos links de página inicial e contato foi alterada" lightbox="../media/beginners-css-internal2.msft.png":::
       <span data-ttu-id="28138-189">A fonte dos links de **página inicial** e **contato** foi alterada</span><span class="sxs-lookup"><span data-stu-id="28138-189">The font of the **Home** and **Contact** links has changed</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="28138-190">Entender as folhas de estilos internas</span><span class="sxs-lookup"><span data-stu-id="28138-190">Understand internal stylesheets</span></span>  

<span data-ttu-id="28138-191">As folhas de estilos internas aplicam estilos usando **seletores**.</span><span class="sxs-lookup"><span data-stu-id="28138-191">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="28138-192">Os seletores são padrões que podem ser aplicados a um ou mais elementos HTML.</span><span class="sxs-lookup"><span data-stu-id="28138-192">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="28138-193">O trecho de código anterior adicionou o estilo a seguir.</span><span class="sxs-lookup"><span data-stu-id="28138-193">The previous code snippet added the following style.</span></span>  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` <span data-ttu-id="28138-194">é um seletor que traduz para "qualquer `<li>` elemento que contém um `<a>` elemento".</span><span class="sxs-lookup"><span data-stu-id="28138-194">is a selector that translates to "any `<li>` element that contains an `<a>` element".</span></span>  <span data-ttu-id="28138-195">O navegador altera a fonte dos links de **página inicial** e de **contato** porque cada um dos grupos de marcas corresponde ao padrão.</span><span class="sxs-lookup"><span data-stu-id="28138-195">The browser changes the font of the **Home** and **Contact** links because each of the tag groups match the pattern.</span></span>  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="28138-196">é uma **declaração**.</span><span class="sxs-lookup"><span data-stu-id="28138-196">is a **declaration**.</span></span>  <span data-ttu-id="28138-197">Uma declaração é feita das duas partes A seguir.</span><span class="sxs-lookup"><span data-stu-id="28138-197">A declaration is made of following two parts.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="28138-198">folha</span><span class="sxs-lookup"><span data-stu-id="28138-198">property</span></span>**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="28138-199">A propriedade descreve uma maneira geral pela qual você pode alterar o estilo do elemento.</span><span class="sxs-lookup"><span data-stu-id="28138-199">The property describes a general way that you are able to change the style of the element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="28138-200">value</span><span class="sxs-lookup"><span data-stu-id="28138-200">value</span></span>**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="28138-201">O valor descreve exatamente como o estilo do elemento deve mudar.</span><span class="sxs-lookup"><span data-stu-id="28138-201">The value describes exactly how the style of the element should change.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="28138-202">Por exemplo, `font-family: 'Courier New', Courier, serif` o navegador dá a seguinte instrução: "definir a fonte dos elementos que correspondem ao padrão `li a` `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="28138-202">For example, `font-family: 'Courier New', Courier, serif` gives the browser the following instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="28138-203">Se essa fonte não estiver disponível, use `Courier` .</span><span class="sxs-lookup"><span data-stu-id="28138-203">If that font is not available, use `Courier`.</span></span>  <span data-ttu-id="28138-204">Se isso não estiver disponível, use `serif` ".</span><span class="sxs-lookup"><span data-stu-id="28138-204">If that is not available, use `serif`."</span></span>  

### <span data-ttu-id="28138-205">Adicionar vários seletores a um RuleSet</span><span class="sxs-lookup"><span data-stu-id="28138-205">Add multiple selectors to a ruleset</span></span>  

<span data-ttu-id="28138-206">Um bloco de código CSS, como o que você vê abaixo, é chamado de **RuleSet**.</span><span class="sxs-lookup"><span data-stu-id="28138-206">A block of CSS code like what you see below is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="28138-207">Conclua as seguintes ações para usar vírgulas para adicionar vários seletores a um RuleSet.</span><span class="sxs-lookup"><span data-stu-id="28138-207">Complete the following actions to use commas to add multiple selectors to a ruleset.</span></span>  

1.  <span data-ttu-id="28138-208">Na **guia Editor**, abra `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="28138-208">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="28138-209">Após o `li a` tipo `, h1` .</span><span class="sxs-lookup"><span data-stu-id="28138-209">After `li a` type `, h1`.</span></span>  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    <span data-ttu-id="28138-210">O trecho de código anterior informa ao navegador para `<h1>` elementos de estilo da mesma maneira que ele estiliza elementos que correspondem ao padrão `li a` .</span><span class="sxs-lookup"><span data-stu-id="28138-210">The previous code snippet tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="28138-211">Ir para a **guia ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="28138-211">Go to the **live tab**.</span></span>  
1.  <span data-ttu-id="28138-212">Escolha o link do **contato** para voltar para a página de contato.</span><span class="sxs-lookup"><span data-stu-id="28138-212">Choose the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="28138-213">Agora, **entre em contato comigo!**</span><span class="sxs-lookup"><span data-stu-id="28138-213">Now, **Contact Me!**</span></span> <span data-ttu-id="28138-214">tem a mesma fonte dos links de navegação.</span><span class="sxs-lookup"><span data-stu-id="28138-214">has the same font as the navigation links.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="O texto fale comigo!  Agora tem a mesma fonte dos links de página inicial e de contato" lightbox="../media/beginners-css-multiple1.msft.png":::
       <span data-ttu-id="28138-217">O texto **fale comigo!**</span><span class="sxs-lookup"><span data-stu-id="28138-217">The text **Contact Me!**</span></span> <span data-ttu-id="28138-218">Agora tem a mesma fonte dos links de **página inicial** e de **contato**</span><span class="sxs-lookup"><span data-stu-id="28138-218">now has the same font as the **Home** and **Contact** links</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="28138-219">Experimente com o DevTools</span><span class="sxs-lookup"><span data-stu-id="28138-219">Experiment with DevTools</span></span>  

<span data-ttu-id="28138-220">Ao continuar a viagem para se tornar um especialista no desenvolvimento na Web, você pode descobrir que o CSS é complicado.</span><span class="sxs-lookup"><span data-stu-id="28138-220">As you continue your journey to become an expert in web development, you may find that CSS is tricky.</span></span>  <span data-ttu-id="28138-221">Você pode escrever um CSS e esperar que ele exiba uma maneira, mas o navegador faz algo completamente diferente.</span><span class="sxs-lookup"><span data-stu-id="28138-221">You may write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="28138-222">O Microsoft Edge DevTools torna mais fácil experimentar as alterações e ver imediatamente como as alterações afetam a página.</span><span class="sxs-lookup"><span data-stu-id="28138-222">Microsoft Edge DevTools makes it easy to experiment with changes and immediately see how the changes affect the page.</span></span>  

### <span data-ttu-id="28138-223">Adicionar uma declaração a um rulet existente no DevTools</span><span class="sxs-lookup"><span data-stu-id="28138-223">Add a declaration to an existing rulest in DevTools</span></span>  

<span data-ttu-id="28138-224">Conclua as ações a seguir para iterar no estilo de um elemento existente, adicionar uma declaração a um RuleSet existente.</span><span class="sxs-lookup"><span data-stu-id="28138-224">Complete the following actions to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  

1.  <span data-ttu-id="28138-225">Passe o mouse sobre o link **início** , abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="28138-225">Hover on the **Home** link, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Inspecionar o link home" lightbox="../media/beginners-css-add1.msft.png":::
       <span data-ttu-id="28138-227">Inspecionar o link home</span><span class="sxs-lookup"><span data-stu-id="28138-227">Inspect the Home link</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="28138-228">O DevTools é aberto juntamente com sua página.</span><span class="sxs-lookup"><span data-stu-id="28138-228">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="28138-229">O código que representa o link início `<a href="/">Home</a>` é em azul realçado na árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="28138-229">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="28138-230">O trecho de código e a visualização devem estar familiarizados [com o introdução ao HTML e ao dom][DevtoolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="28138-230">The code snippet and preview should be familiar from [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="28138-231">Na figura a seguir, a `font-family: 'Courier New', Courier, serif` declaração que você adicionou anteriormente `contact.html` é vista na guia **estilos** abaixo da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="28138-231">In the following figure, the `font-family: 'Courier New', Courier, serif` declaration that you previously added to `contact.html` is seen in the **Styles** tab below the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="A guia estilos está abaixo da árvore DOM" lightbox="../media/beginners-css-add2.msft.png":::
             <span data-ttu-id="28138-233">A guia **estilos** está abaixo da árvore DOM</span><span class="sxs-lookup"><span data-stu-id="28138-233">The **Styles** tab is below the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="28138-234">Se a janela do DevTools for ampla, a guia estilos estará à direita da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="28138-234">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="A guia estilos está à direita da árvore DOM" lightbox="../media/beginners-css-add3.msft.png":::
             <span data-ttu-id="28138-236">A guia **estilos** está à direita da árvore DOM</span><span class="sxs-lookup"><span data-stu-id="28138-236">The **Styles** tab is to the right of the DOM Tree</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="28138-237">Escolha a linha vazia abaixo `font-family: 'Courier New', Courier, Serif` para adicionar uma nova declaração.</span><span class="sxs-lookup"><span data-stu-id="28138-237">Choose the empty line below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Adicionar uma nova declaração" lightbox="../media/beginners-css-add4.msft.png":::
       <span data-ttu-id="28138-239">Adicionar uma nova declaração</span><span class="sxs-lookup"><span data-stu-id="28138-239">Add a new declaration</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-240">Digite `color` e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="28138-240">Type `color` and select `Enter`.</span></span>  <span data-ttu-id="28138-241">A interface do usuário de AutoCompletar sugere opções à medida que você digita.</span><span class="sxs-lookup"><span data-stu-id="28138-241">The autocomplete UI suggests options as you type.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Cor do tipo" lightbox="../media/beginners-css-add5.msft.png":::
       <span data-ttu-id="28138-243">Tipo</span><span class="sxs-lookup"><span data-stu-id="28138-243">Type</span></span> `color`  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-244">Digite `magenta` e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="28138-244">Type `magenta` and select `Enter`.</span></span>  <span data-ttu-id="28138-245">Todo o texto na página de contato agora é magenta.</span><span class="sxs-lookup"><span data-stu-id="28138-245">All of the text on the contact page is now magenta.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Digite magenta" lightbox="../media/beginners-css-add6.msft.png":::
       <span data-ttu-id="28138-247">Tipo</span><span class="sxs-lookup"><span data-stu-id="28138-247">Type</span></span> `magenta`  
    :::image-end:::  
    
### <span data-ttu-id="28138-248">Editar uma declaração no DevTools</span><span class="sxs-lookup"><span data-stu-id="28138-248">Edit a declaration in DevTools</span></span>  

<span data-ttu-id="28138-249">Conclua as seguintes ações para editar as declarações existentes no DevTools.</span><span class="sxs-lookup"><span data-stu-id="28138-249">Complete the following actions to edit existing declarations in DevTools.</span></span>  

1.  <span data-ttu-id="28138-250">Escolha o quadrado magenta ao lado de `magenta` .</span><span class="sxs-lookup"><span data-stu-id="28138-250">Choose the magenta square next to `magenta`.</span></span>  <span data-ttu-id="28138-251">Um seletor de cores aparece.</span><span class="sxs-lookup"><span data-stu-id="28138-251">A color picker pops up.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="O seletor de cores" lightbox="../media/beginners-css-edit1.msft.png":::
       <span data-ttu-id="28138-253">O seletor de cores</span><span class="sxs-lookup"><span data-stu-id="28138-253">The Color Picker</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-254">Use o seletor de cores para alterar o texto da fonte para uma cor que você quiser.</span><span class="sxs-lookup"><span data-stu-id="28138-254">Use the color picker to change the font text to a color that you like.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Alterar a cor da fonte para roxo com o seletor de cores" lightbox="../media/beginners-css-edit2.msft.png":::
       <span data-ttu-id="28138-256">Alterar a cor da fonte para roxo com o seletor de cores</span><span class="sxs-lookup"><span data-stu-id="28138-256">Change the font color to purple with the Color Picker</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="28138-257">Adicionar um novo RuleSet no DevTools</span><span class="sxs-lookup"><span data-stu-id="28138-257">Add a new ruleset in DevTools</span></span>  

<span data-ttu-id="28138-258">Conclua as seguintes ações para adicionar novos RuleSets ao DevTools.</span><span class="sxs-lookup"><span data-stu-id="28138-258">Complete the following actions to add new rulesets in DevTools.</span></span>  

1.  <span data-ttu-id="28138-259">Escolha **novo regra de estilo** \ ( ![ nova regra ][ImageNewStyleRuleIcon] de estilo \) que é ao lado de **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="28138-259">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) which is next to **.cls**.</span></span>  <span data-ttu-id="28138-260">Um RuleSet vazio aparece `a` como o seletor.</span><span class="sxs-lookup"><span data-stu-id="28138-260">An empty ruleset appears with `a` as the selector.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Adicionar uma nova regra" lightbox="../media/beginners-css-rule1.msft.png":::
       <span data-ttu-id="28138-262">Adicionar uma nova regra</span><span class="sxs-lookup"><span data-stu-id="28138-262">Add a new rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-263">Substituir `a` por `a:hover` .</span><span class="sxs-lookup"><span data-stu-id="28138-263">Replace `a` with `a:hover`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Substituir por a:hover" lightbox="../media/beginners-css-rule2.msft.png":::
       <span data-ttu-id="28138-265">Substituir `a` por</span><span class="sxs-lookup"><span data-stu-id="28138-265">Replace `a` with</span></span> `a:hover`  
    :::image-end:::  
    
    `:hover` <span data-ttu-id="28138-266">é uma **pseudo-classe**.</span><span class="sxs-lookup"><span data-stu-id="28138-266">is a **pseudo-class**.</span></span>  <span data-ttu-id="28138-267">Use pseudovariáveis para elementos de estilo que podem inserir Estados especiais.</span><span class="sxs-lookup"><span data-stu-id="28138-267">Use pseudo-classes for style elements that may enter special states.</span></span>  <span data-ttu-id="28138-268">Por exemplo, o `a:hover` estilo somente tem efeito quando você estiver passando o mouse sobre um `<a>` elemento.</span><span class="sxs-lookup"><span data-stu-id="28138-268">For example, the `a:hover` style only takes effect when you are hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="28138-269">Escolha entre os colchetes para adicionar uma nova declaração.</span><span class="sxs-lookup"><span data-stu-id="28138-269">Choose between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="28138-270">Digite `background-color` o nome da declaração e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="28138-270">Type `background-color` for the declaration name and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Digite a cor da tela de fundo" lightbox="../media/beginners-css-rule3.msft.png":::
       <span data-ttu-id="28138-272">Tipo</span><span class="sxs-lookup"><span data-stu-id="28138-272">Type</span></span> `background-color`  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-273">Digite `green` o valor da declaração e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="28138-273">Type `green` for the declaration value and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Digite verde" lightbox="../media/beginners-css-rule4.msft.png":::
       <span data-ttu-id="28138-275">Tipo</span><span class="sxs-lookup"><span data-stu-id="28138-275">Type</span></span> `green`  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-276">Passe o mouse sobre o link **início** .</span><span class="sxs-lookup"><span data-stu-id="28138-276">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="28138-277">O plano de fundo do link fica verde.</span><span class="sxs-lookup"><span data-stu-id="28138-277">The background of the link turns green.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Passe o mouse sobre o link home para revelar o plano de fundo verde" lightbox="../media/beginners-css-rule5.msft.png":::
       <span data-ttu-id="28138-279">Passe o mouse sobre o link home para revelar o plano de fundo verde</span><span class="sxs-lookup"><span data-stu-id="28138-279">Hover over the Home link to reveal its green background</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="28138-280">Reutilizar estilos em páginas com folhas de estilo externas</span><span class="sxs-lookup"><span data-stu-id="28138-280">Re-use styles across pages with external stylesheets</span></span>  

<span data-ttu-id="28138-281">Em uma etapa anterior, você adicionou o trecho de código a seguir como uma folha de estilos interna `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="28138-281">In a previous step, you added the following code snippet as an internal stylesheet to `contact.html`.</span></span>  

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

<span data-ttu-id="28138-282">E se você quisesse estilizar `index.html` da mesma maneira?</span><span class="sxs-lookup"><span data-stu-id="28138-282">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="28138-283">E se você tivesse um grande número de páginas para as quais você deseja aplicar seus estilos?</span><span class="sxs-lookup"><span data-stu-id="28138-283">What if you had a large number of pages to which you wanted to apply your styles?</span></span>  <span data-ttu-id="28138-284">Você precisaria copiar e colar a folha de estilos interna em cada página da Web em seu site.</span><span class="sxs-lookup"><span data-stu-id="28138-284">You would have to copy and paste the internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="28138-285">Conclua as ações a seguir para adicionar uma **folha de estilos externa** para permitir que você escreva sua CSS uma vez e a aplique em várias páginas.</span><span class="sxs-lookup"><span data-stu-id="28138-285">Complete the following actions to add an **External stylesheet** to allow you to write your CSS once and apply it to multiple pages.</span></span>  

1.  <span data-ttu-id="28138-286">Primeiro, recarregue a guia ao vivo para remover as alterações feitas no DevTools.</span><span class="sxs-lookup"><span data-stu-id="28138-286">First, reload the live tab to remove the changes that you made in DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" Depois de atualizar a página, as alterações que foram feitas no DevTools são perdidas" lightbox="../media/beginners-css-external1.msft.png":::
        <span data-ttu-id="28138-288">Depois de atualizar a página, as alterações que foram feitas no DevTools são perdidas</span><span class="sxs-lookup"><span data-stu-id="28138-288">After you refresh the page, the changes that were made in DevTools are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-289">Volte para a **guia Editor** e abra `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="28138-289">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       <span data-ttu-id="28138-291">contact.html</span><span class="sxs-lookup"><span data-stu-id="28138-291">contact.html</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-292">Exclua tudo entre `<style>` e `</style>` , incluindo `<style>` e `</style>` .</span><span class="sxs-lookup"><span data-stu-id="28138-292">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="A marca de estilo foi removida" lightbox="../media/beginners-css-external3.msft.png":::
       <span data-ttu-id="28138-294">A marca de estilo foi removida</span><span class="sxs-lookup"><span data-stu-id="28138-294">The style tag has been removed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-295">Vá para `index.html` e remova `style="background-color: aliceblue;"` da `<nav>` marca.</span><span class="sxs-lookup"><span data-stu-id="28138-295">Go to `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="28138-296">Você já removeu toda a CSS que você adicionou anteriormente ao seu site.</span><span class="sxs-lookup"><span data-stu-id="28138-296">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="O estilo embutido foi removido do elemento NAV" lightbox="../media/beginners-css-external4.msft.png":::
       <span data-ttu-id="28138-298">O estilo embutido foi removido do elemento NAV</span><span class="sxs-lookup"><span data-stu-id="28138-298">The inline style has been removed from the nav element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-299">Escolha **novo arquivo**.</span><span class="sxs-lookup"><span data-stu-id="28138-299">Choose **New File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="A caixa de diálogo novo arquivo" lightbox="../media/beginners-css-external5.msft.png":::
       <span data-ttu-id="28138-301">A caixa de diálogo novo arquivo</span><span class="sxs-lookup"><span data-stu-id="28138-301">The new file dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-302">Substituir `cool-file.js` por `style.css` e escolha **Adicionar arquivo**.</span><span class="sxs-lookup"><span data-stu-id="28138-302">Replace `cool-file.js` with `style.css` and choose **Add File**.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Estilo de tipo. css" lightbox="../media/beginners-css-external6.msft.png":::
       <span data-ttu-id="28138-304">Tipo</span><span class="sxs-lookup"><span data-stu-id="28138-304">Type</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-305">Adicione o trecho de código a seguir ao seu `style.css` arquivo.</span><span class="sxs-lookup"><span data-stu-id="28138-305">Add the following code snippet to your `style.css` file.</span></span>  
    
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
       <span data-ttu-id="28138-307">Adicionar código a</span><span class="sxs-lookup"><span data-stu-id="28138-307">Add code to</span></span> `style.css`  
    :::image-end:::  
    
    <span data-ttu-id="28138-308">Certifique-se de que você criou uma folha de estilos externa.</span><span class="sxs-lookup"><span data-stu-id="28138-308">Ensure that you have created an external stylesheet.</span></span> <span data-ttu-id="28138-309">O HTML não está ciente de que ele existe.</span><span class="sxs-lookup"><span data-stu-id="28138-309">Your HTML is not aware that it exists.</span></span>  
    
1.  <span data-ttu-id="28138-310">Abrir `index.html` .</span><span class="sxs-lookup"><span data-stu-id="28138-310">Open `index.html`.</span></span>  
1.  <span data-ttu-id="28138-311">Adicione `<link rel="stylesheet" href="style.css">` ao seu HTML.</span><span class="sxs-lookup"><span data-stu-id="28138-311">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Link para estilo. css" lightbox="../media/beginners-css-external8.msft.png":::
       <span data-ttu-id="28138-313">Link para</span><span class="sxs-lookup"><span data-stu-id="28138-313">Link to</span></span> `style.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-314">Abra o `contact.html` arquivo e adicione o link ali.</span><span class="sxs-lookup"><span data-stu-id="28138-314">Open the `contact.html` file and add the link there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Link para estilo. CSS em contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       <span data-ttu-id="28138-316">Link para `style.css` em</span><span class="sxs-lookup"><span data-stu-id="28138-316">Link to `style.css` in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-317">Ir para a **guia ao vivo**.  A Home Page agora tem a mesma fonte da última seção e uma seção azul de navegação.</span><span class="sxs-lookup"><span data-stu-id="28138-317">Go to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="A Home Page" lightbox="../media/beginners-css-external10.msft.png":::
       <span data-ttu-id="28138-319">A Home Page</span><span class="sxs-lookup"><span data-stu-id="28138-319">The home page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-320">Escolha o link do **contato** para acessar a página do contato.</span><span class="sxs-lookup"><span data-stu-id="28138-320">Choose the **Contact** link to go to the contact page.</span></span>  <span data-ttu-id="28138-321">A página de contato tem a mesma formatação que a Home Page.</span><span class="sxs-lookup"><span data-stu-id="28138-321">The contact page has the same formatting as the home page.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="Página de contato" lightbox="../media/beginners-css-external11.msft.png":::
       <span data-ttu-id="28138-323">Página de contato</span><span class="sxs-lookup"><span data-stu-id="28138-323">The contact page</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="28138-324">Usar uma estrutura CSS</span><span class="sxs-lookup"><span data-stu-id="28138-324">Use a CSS framework</span></span>  

<span data-ttu-id="28138-325">**Estruturas CSS** são coleções de estilos criados por outros desenvolvedores que facilitam a criação de sites atraentes.</span><span class="sxs-lookup"><span data-stu-id="28138-325">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="28138-326">Em vez de definir estilos por conta própria, uma estrutura fornece um conjunto de estilos que você pode usar em seus elementos de página.</span><span class="sxs-lookup"><span data-stu-id="28138-326">Instead of defining styles yourself, a framework provides you a collection of styles that you are able to use on your page elements.</span></span>  

1.  <span data-ttu-id="28138-327">Copie o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="28138-327">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="28138-328">Vá para a guia edição e cole o código em `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="28138-328">Go to the editing tab and paste the code into `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Link para a estrutura em contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       <span data-ttu-id="28138-330">Link para a estrutura em</span><span class="sxs-lookup"><span data-stu-id="28138-330">Link to the framework in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-331">Abra o `index.html` arquivo e adicione o código.</span><span class="sxs-lookup"><span data-stu-id="28138-331">Open the `index.html` file and add the code there.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Link para a estrutura em index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       <span data-ttu-id="28138-333">Link para a estrutura em</span><span class="sxs-lookup"><span data-stu-id="28138-333">Link to the framework in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-334">Volte para a guia ao vivo para ver suas alterações.</span><span class="sxs-lookup"><span data-stu-id="28138-334">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="28138-335">Enquanto a cor da tela de fundo do `<nav>` elemento e a fonte `<li>` dos `<a>` elementos e são iguais, a fonte dos outros elementos mudava.</span><span class="sxs-lookup"><span data-stu-id="28138-335">While the background color of the `<nav>` element and the font of the `<li>` and `<a>` elements are the same, the font of the other elements has changed.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Parte da fonte na página inicial foi alterada por causa da estrutura" lightbox="../media/beginners-css-framework3.msft.png":::
       <span data-ttu-id="28138-337">Parte da fonte na página inicial foi alterada por causa da estrutura</span><span class="sxs-lookup"><span data-stu-id="28138-337">Some of the font on the home page changed because of the framework</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="28138-338">Usar uma classe</span><span class="sxs-lookup"><span data-stu-id="28138-338">Use a class</span></span>  

<span data-ttu-id="28138-339">Na última seção, você adicionou a inicialização às páginas da Web, o que altera as fontes de alguns dos elementos do seu site.</span><span class="sxs-lookup"><span data-stu-id="28138-339">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="28138-340">As estruturas CSS ajudam você a fazer alterações importantes na sua página com um pouco de código.</span><span class="sxs-lookup"><span data-stu-id="28138-340">CSS frameworks help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="28138-341">Conclua as ações a seguir para alterar o cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="28138-341">Complete the following actions to change your header.</span></span>  

1.  <span data-ttu-id="28138-342">Copie o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="28138-342">Copy the following code snippet.</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="28138-343">Adicione o trecho de código anterior à sua `<header>` marca `index.html` .</span><span class="sxs-lookup"><span data-stu-id="28138-343">Add the previous code snippet to your `<header>` tag in `index.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Adicionar classes no index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       <span data-ttu-id="28138-345">Adicionar classes em</span><span class="sxs-lookup"><span data-stu-id="28138-345">Add classes in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-346">Adicione o código à sua `<header>` marca `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="28138-346">Add the code to your `<header>` tag in `contact.html`.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Adicionar classes no contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       <span data-ttu-id="28138-348">Adicionar classes em</span><span class="sxs-lookup"><span data-stu-id="28138-348">Add classes in</span></span> `contact.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-349">Exiba suas alterações na guia ao vivo.  Há uma grande caixa cinza em torno do seu cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="28138-349">View your changes in the live tab.  There is a big, grey box around your header.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="Agora o cabeçalho tem uma grande caixa cinza ao seu lado" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       <span data-ttu-id="28138-351">Agora o cabeçalho tem uma grande caixa cinza ao seu lado</span><span class="sxs-lookup"><span data-stu-id="28138-351">The header now has a big, grey box around it</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="28138-352">Compreender classes</span><span class="sxs-lookup"><span data-stu-id="28138-352">Understand classes</span></span>  

<span data-ttu-id="28138-353">As classes permitem atribuir coleções de estilos a elementos arbitrários.</span><span class="sxs-lookup"><span data-stu-id="28138-353">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="28138-354">Use o trecho de código a seguir para aplicar vários estilos ao `<header>` elemento depois de definir o `class` atributo para `jumbotron` .</span><span class="sxs-lookup"><span data-stu-id="28138-354">Use the following code snippet to apply several styles to the `<header>` element after you set the `class` attribute to `jumbotron`.</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="28138-355">Uma vantagem de uma classe é permitir que você aplique estilos a qualquer elemento desejado.</span><span class="sxs-lookup"><span data-stu-id="28138-355">One advantage of a class is that it lets you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="28138-356">Por exemplo, suponha que você queira definir a cor da tela de fundo de alguns `<p>` elementos como roxo, mas não todos os `<p>` elementos.</span><span class="sxs-lookup"><span data-stu-id="28138-356">For example, suppose you want to set the background color of some `<p>` elements to purple, but not all `<p>` elements.</span></span>  <span data-ttu-id="28138-357">Use o trecho de código a seguir para definir o estilo em uma classe.</span><span class="sxs-lookup"><span data-stu-id="28138-357">Use the following code snippet to define the style in a class.</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="28138-358">Em seguida, aplique a classe somente aos `<p>` elementos que você deseja aplicar o estilo.</span><span class="sxs-lookup"><span data-stu-id="28138-358">Next, apply the class to only the `<p>` elements that you want to style.</span></span>  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### <span data-ttu-id="28138-359">Alinhar elementos</span><span class="sxs-lookup"><span data-stu-id="28138-359">Align elements</span></span>  

<span data-ttu-id="28138-360">Conclua as ações a seguir para inicializar e fornecer classes para alinhar elementos.</span><span class="sxs-lookup"><span data-stu-id="28138-360">Complete the following actions to bootstrap and provide classes for aligning elements.</span></span>  

1.  <span data-ttu-id="28138-361">Volte para a guia Editor e abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="28138-361">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="28138-362">Adicionar `class="container-fluid"` à sua `<body>` marca.</span><span class="sxs-lookup"><span data-stu-id="28138-362">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Adicionar a classe container-fluido" lightbox="../media/beginners-css-align1.msft.png":::
       <span data-ttu-id="28138-364">Adicionar a `container-fluid` classe</span><span class="sxs-lookup"><span data-stu-id="28138-364">Add the `container-fluid` class</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-365">Envolver seus `<nav>` `<main>` elementos e em `<div class="row">` .</span><span class="sxs-lookup"><span data-stu-id="28138-365">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="28138-366">Certifique-se de colocar `</div>` após para `</main>` fechar corretamente a nova marca.</span><span class="sxs-lookup"><span data-stu-id="28138-366">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Adicionar uma linha" lightbox="../media/beginners-css-align2.msft.png":::
       <span data-ttu-id="28138-368">Adicionar uma linha</span><span class="sxs-lookup"><span data-stu-id="28138-368">Add a row</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-369">Adicione `class="col-3"` à sua `<nav>` marca e `class="col-9"` à sua `<main>` marca.</span><span class="sxs-lookup"><span data-stu-id="28138-369">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Adicionar as classes Col-3 e col-9" lightbox="../media/beginners-css-align3.msft.png":::
       <span data-ttu-id="28138-371">Adicionar as `col-3` `col-9` classes e</span><span class="sxs-lookup"><span data-stu-id="28138-371">Add the `col-3` and `col-9` classes</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28138-372">Exiba suas alterações na guia ao vivo.</span><span class="sxs-lookup"><span data-stu-id="28138-372">View your changes in the live tab.</span></span>  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="O conteúdo de NAV agora está à esquerda do conteúdo principal" lightbox="../media/beginners-css-align4.msft.png":::
       <span data-ttu-id="28138-374">O conteúdo de NAV agora está à esquerda do conteúdo principal</span><span class="sxs-lookup"><span data-stu-id="28138-374">The nav content is now to the left of the main content</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="28138-375">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="28138-375">Next steps</span></span>  

<span data-ttu-id="28138-376">Parabéns! você concluiu.</span><span class="sxs-lookup"><span data-stu-id="28138-376">Congratulations, you are done.</span></span>  

*   <span data-ttu-id="28138-377">A melhor maneira de ficar melhor no desenvolvimento na Web é criar mais sites.</span><span class="sxs-lookup"><span data-stu-id="28138-377">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="28138-378">Não se preocupe com as coisas quebradas.</span><span class="sxs-lookup"><span data-stu-id="28138-378">Do not worry about breaking stuff.</span></span>  <span data-ttu-id="28138-379">Só Divirta-se e saiba o máximo possível ao longo do caminho.</span><span class="sxs-lookup"><span data-stu-id="28138-379">Just have fun and learn as much as possible along the way.</span></span>  
*   <span data-ttu-id="28138-380">Para saber mais sobre o estilo de páginas da Web, consulte [introdução ao CSS][MDNCssFirstSteps].</span><span class="sxs-lookup"><span data-stu-id="28138-380">To learn more about styling web pages, see [Introduction to CSS][MDNCssFirstSteps].</span></span>  
*   <span data-ttu-id="28138-381">Para saber mais sobre como usar o DevTools para experimentar a CSS de uma página, confira [introdução ao modo de exibição e alteração de CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="28138-381">To learn more about how to use DevTools to experiment with the CSS of a page, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<!--- image links --->  

[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools para iniciantes: introdução ao HTML e ao DOM | Documentos da Microsoft"  
[DevtoolsCssIndex]: ../css/index.md "Introdução ao visualizar e alterar CSS | Documentos da Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-cozinhá-Amphibian | Problema"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Primeiras etapas da CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="28138-387">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="28138-387">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="28138-388">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/beginners/css) e é criada pela [Katherine Jackson][KatherineJackson] \ (redatora técnica, Chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="28138-388">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="28138-390">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="28138-390">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
