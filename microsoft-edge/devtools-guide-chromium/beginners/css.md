---
title: 'DevTools para iniciantes: introdução ao CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: fba049a20a7b5f981130b4d9e60c37b07dc7e092
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882734"
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

# <span data-ttu-id="2c2ed-103">DevTools para iniciantes: introdução ao CSS</span><span class="sxs-lookup"><span data-stu-id="2c2ed-103">DevTools for beginners: Get started with CSS</span></span>   

<span data-ttu-id="2c2ed-104">Neste tutorial, você aprenderá a usar CSS para estilizar uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-104">In this tutorial, you learn how to use CSS to style a web page.</span></span>  <span data-ttu-id="2c2ed-105">Você também aprenderá a usar o Microsoft Edge DevTools para experimentar alterações de CSS.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-105">You also learn how to use Microsoft Edge DevTools to experiment with CSS changes.</span></span>  

<span data-ttu-id="2c2ed-106">Este é o segundo tutorial em uma série de tutoriais que ensina noções básicas de desenvolvimento da Web e do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-106">This is the second tutorial in a series of tutorials that teaches you the basics of web development and Microsoft Edge DevTools.</span></span>  <span data-ttu-id="2c2ed-107">Na verdade, você ganha experiência prática ao criar seu próprio website.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-107">You gain hands-on experience by actually building your own website.</span></span>  <span data-ttu-id="2c2ed-108">Você não precisa concluir o primeiro tutorial antes de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-108">You don't have to complete the first tutorial before doing this one.</span></span>  <span data-ttu-id="2c2ed-109">Você pode começar aqui.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-109">You can start here.</span></span>  <span data-ttu-id="2c2ed-110">[Configurar seu código](#set-up-your-code) mostra como fazer a configuração.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-110">[Set up your code](#set-up-your-code) shows you how to get set up.</span></span>  

> [!NOTE]
> <span data-ttu-id="2c2ed-111">Este tutorial foi projetado para principiantes absolutos e se concentra nos **fundamentos do desenvolvimento na Web** e nas noções básicas de como usar o devtools para experimentar com CSS.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-111">This tutorial is designed for absolute beginners and focuses on both the **fundamentals of web development** and the basics of using DevTools to experiment with CSS.</span></span>  <span data-ttu-id="2c2ed-112">Se você quiser um tutorial que só se concentre no DevTools, confira [introdução e alterar CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="2c2ed-112">If you want a tutorial that only focuses on DevTools, see [Get Started with Viewing and Changing CSS][DevtoolsCssIndex].</span></span>  

<span data-ttu-id="2c2ed-113">No momento, o seu site tem a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-113">Currently your site looks like this:</span></span>  

> ##### <span data-ttu-id="2c2ed-114">Figura 1</span><span class="sxs-lookup"><span data-stu-id="2c2ed-114">Figure 1</span></span>  
> <span data-ttu-id="2c2ed-115">Qual é a aparência de seu site</span><span class="sxs-lookup"><span data-stu-id="2c2ed-115">What your site currently looks like</span></span>  
> ![Qual é a aparência de seu site][ImageCssIntro1]  

<span data-ttu-id="2c2ed-117">Depois de concluir o tutorial, ele terá a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-117">After completing the tutorial, it will look like this:</span></span>  

> ##### <span data-ttu-id="2c2ed-118">Figura 2</span><span class="sxs-lookup"><span data-stu-id="2c2ed-118">Figure 2</span></span>  
> <span data-ttu-id="2c2ed-119">Qual será a aparência do seu site no final do tutorial</span><span class="sxs-lookup"><span data-stu-id="2c2ed-119">What your site will look like at the end of the tutorial</span></span>  
> ![Qual será a aparência do seu site no final do tutorial][ImageCssIntro2]  

## <span data-ttu-id="2c2ed-121">Goal</span><span class="sxs-lookup"><span data-stu-id="2c2ed-121">Goals</span></span>   

<span data-ttu-id="2c2ed-122">No final deste tutorial, você compreenderá:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-122">By the end of this tutorial, you will understand:</span></span>  

*   <span data-ttu-id="2c2ed-123">Como usar CSS para estilizar uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-123">How to use CSS to style a web page.</span></span>  
*   <span data-ttu-id="2c2ed-124">Como usar o Microsoft Edge DevTools para experimentar com CSS.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-124">How to use Microsoft Edge DevTools to experiment with CSS.</span></span>  
*   <span data-ttu-id="2c2ed-125">A diferença entre estruturas CSS e CSS.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-125">The difference between CSS and CSS frameworks.</span></span>  

<span data-ttu-id="2c2ed-126">Você também terá um site real!</span><span class="sxs-lookup"><span data-stu-id="2c2ed-126">You'll also have a real website!</span></span>  

## <span data-ttu-id="2c2ed-127">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="2c2ed-127">Prerequisites</span></span>   

<span data-ttu-id="2c2ed-128">Antes de tentar este tutorial, complete os seguintes pré-requisitos:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-128">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="2c2ed-129">Conclua [a introdução ao HTML e ao dom][DevToolsBeginnersHtml] ou certifique-se de que você tenha uma compreensão do HTML e do dom semelhante ao ensinado nesse tutorial.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-129">Complete [Get Started with HTML and the DOM][DevToolsBeginnersHtml] or make sure that you have an understanding of HTML and the DOM similar to what's taught in that tutorial.</span></span>  
*   <span data-ttu-id="2c2ed-130">Baixar o navegador da Web [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-130">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="2c2ed-131">Este tutorial usa um conjunto de ferramentas de desenvolvimento da Web, chamado de Microsoft Edge DevTools, incorporado ao Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-131">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="2c2ed-132">Configurar seu código</span><span class="sxs-lookup"><span data-stu-id="2c2ed-132">Set up your code</span></span>   

<span data-ttu-id="2c2ed-133">Para começar a criar seu site, você precisa configurar seu código:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-133">In order to start creating your site, you need to set up your code:</span></span>  

1.  **<span data-ttu-id="2c2ed-134">Se você já concluiu o primeiro tutorial desta série, pule esta seção!</span><span class="sxs-lookup"><span data-stu-id="2c2ed-134">If you have already completed the first tutorial in this series, skip this section!</span></span>  <span data-ttu-id="2c2ed-135">Continue usando o código do último tutorial, [introdução ao HTML e ao dom][DevToolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="2c2ed-135">Continue using your code from the last tutorial, [Get Started with HTML and the DOM][DevToolsBeginnersHtml].</span></span>**  
1.  <span data-ttu-id="2c2ed-136">Abra o [código-fonte][GlitchCookedAmphibianIndex].</span><span class="sxs-lookup"><span data-stu-id="2c2ed-136">Open the [source code][GlitchCookedAmphibianIndex].</span></span>  <span data-ttu-id="2c2ed-137">Esta guia do seu navegador será chamada de **guia edição**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-137">This tab of your browser will be called the **editing tab**.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-138">Figura 3</span><span class="sxs-lookup"><span data-stu-id="2c2ed-138">Figure 3</span></span>  
    > <span data-ttu-id="2c2ed-139">A guia edição</span><span class="sxs-lookup"><span data-stu-id="2c2ed-139">The editing tab</span></span>  
    > ![A guia edição][ImageCssSetup1]  
    
1.  <span data-ttu-id="2c2ed-141">Clique em **cozinhá-Amphibian**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-141">Click **cooked-amphibian**.</span></span>  <span data-ttu-id="2c2ed-142">Um menu é exibido.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-142">A menu pops up.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-143">Figura 4</span><span class="sxs-lookup"><span data-stu-id="2c2ed-143">Figure 4</span></span>  
    > <span data-ttu-id="2c2ed-144">O menu opções do Project</span><span class="sxs-lookup"><span data-stu-id="2c2ed-144">The Project Options menu</span></span>  
    > ![O menu opções do Project][ImageCssSetup2]  

1.  <span data-ttu-id="2c2ed-146">Clique em **remix projeto**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-146">Click **Remix Project**.</span></span>  <span data-ttu-id="2c2ed-147">Falha cria uma cópia do projeto que você pode editar.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-147">Glitch creates a copy of the project that you can edit.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="2c2ed-148">A falha gera um nome aleatório para o novo projeto.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-148">Glitch generates a random name for the new project.</span></span>  
    
1.  <span data-ttu-id="2c2ed-149">Clique em **Mostrar** e selecione **em uma nova janela**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-149">Click **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="2c2ed-150">Outra guia abre com uma visualização dinâmica do seu site.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-150">Another tab opens with a live view of your site.</span></span>  <span data-ttu-id="2c2ed-151">Esta guia do seu navegador será chamada de **guia ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-151">This tab of your browser will be called the **live tab**.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-152">Figura 5</span><span class="sxs-lookup"><span data-stu-id="2c2ed-152">Figure 5</span></span>  
    > <span data-ttu-id="2c2ed-153">A guia ao vivo</span><span class="sxs-lookup"><span data-stu-id="2c2ed-153">The live tab</span></span>  
    > ![A guia ao vivo][ImageCssSetup3]  

## <span data-ttu-id="2c2ed-155">Entender CSS</span><span class="sxs-lookup"><span data-stu-id="2c2ed-155">Understand CSS</span></span>   

<span data-ttu-id="2c2ed-156">**CSS** é um idioma de computador que determina o layout e o estilo de páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-156">**CSS** is a computer language that determines the layout and styling of web pages.</span></span>  <span data-ttu-id="2c2ed-157">Por exemplo, aqui está um parágrafo com uma borda:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-157">For example, here is a paragraph with a border:</span></span>  

> ##### <span data-ttu-id="2c2ed-158">Figura 6</span><span class="sxs-lookup"><span data-stu-id="2c2ed-158">Figure 6</span></span>  
> <span data-ttu-id="2c2ed-159">Isso foi estilizado com CSS</span><span class="sxs-lookup"><span data-stu-id="2c2ed-159">This has been styled with CSS</span></span>  
> ![Isso foi estilizado com CSS][ImageCssStyled]  

<span data-ttu-id="2c2ed-161">Aqui está o código HTML e CSS usado para criar esse parágrafo:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-161">Here is the HTML and CSS code used to create that paragraph:</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` <span data-ttu-id="2c2ed-162">Provavelmente parece novidade para você.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-162">probably looks new to you.</span></span>  <span data-ttu-id="2c2ed-163">O restante deve parecer familiar.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-163">The rest should look familiar.</span></span>  <span data-ttu-id="2c2ed-164">Caso contrário, conclua [a introdução com HTML e o dom antes de][DevToolsBeginnersHtml] tentar este tutorial.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-164">If not, complete [Get Started with HTML and the DOM][DevToolsBeginnersHtml] before attempting this tutorial.</span></span>  

## <span data-ttu-id="2c2ed-165">Adicionar estilos em linha</span><span class="sxs-lookup"><span data-stu-id="2c2ed-165">Add inline styles</span></span>   

<span data-ttu-id="2c2ed-166">Use **estilos embutidos** quando você quiser aplicar estilos a um único elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-166">Use **inline styles** when you want to apply styles to a single element.</span></span>  <span data-ttu-id="2c2ed-167">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-167">Try it now:</span></span>  

1.  <span data-ttu-id="2c2ed-168">Volte para a guia edição e abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-168">Go back to the editing tab and open `index.html`.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-169">Figura 7</span><span class="sxs-lookup"><span data-stu-id="2c2ed-169">Figure 7</span></span>  
    > `index.html`  
    > ![index.html][ImageCssInline1]  

1.  <span data-ttu-id="2c2ed-171">Adicionar `style="background-color: aliceblue;"` à sua `<nav>` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-171">Add `style="background-color: aliceblue;"` to your `<nav>`.</span></span>  <span data-ttu-id="2c2ed-172">No bloco de código abaixo, a quarta linha de código é aquela que você precisa alterar.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-172">In the code block below, the fourth line of code is the one you need to change.</span></span>  <span data-ttu-id="2c2ed-173">O restante está aqui para que você possa ter certeza de que está colocando o novo código no lugar certo.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-173">The rest is just there so you can be sure that you're putting the new code in the right place.</span></span>  
    
    ```html
    ...
        ...
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav style="background-color: aliceblue;">
                <ul>
                    <li><a href="/">Home</a></li>
                    ...
                ...
            ...
        ...
    ...
    ```  

1.  <span data-ttu-id="2c2ed-174">Vá para a **guia ao vivo** para ver as alterações!</span><span class="sxs-lookup"><span data-stu-id="2c2ed-174">Go to the **live tab** to see the changes!</span></span>  <span data-ttu-id="2c2ed-175">O plano de fundo da `<nav>` seção agora está em azul.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-175">The background of the `<nav>` section is now blue.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-176">Figura 8</span><span class="sxs-lookup"><span data-stu-id="2c2ed-176">Figure 8</span></span>  
    > <span data-ttu-id="2c2ed-177">A cor do plano de fundo por trás da página inicial e dos links de contatos agora está azul</span><span class="sxs-lookup"><span data-stu-id="2c2ed-177">The background color behind the Home and Contact links is now blue</span></span>  
    > ![A cor do plano de fundo por trás da página inicial e dos links de contatos agora está azul][ImageCssInline2]  

## <span data-ttu-id="2c2ed-179">Reutilizar estilos em uma única página com folhas de estilos internas</span><span class="sxs-lookup"><span data-stu-id="2c2ed-179">Re-use styles on a single page with internal stylesheets</span></span>   

<span data-ttu-id="2c2ed-180">Anteriormente, você viu um estilo embutido que aplicou um estilo a uma única `<p>` marca como esta:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-180">Earlier, you saw an inline style that applied a style to a single `<p>` tag like this:</span></span>  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

<span data-ttu-id="2c2ed-181">E se você quiser que todos os `<p>` elementos na sua página da Web tenham o estilo da mesma maneira?</span><span class="sxs-lookup"><span data-stu-id="2c2ed-181">What if you wanted all of the `<p>` elements on your webpage to be styled the same way?</span></span>  <span data-ttu-id="2c2ed-182">Você precisaria copiar e colar o código em cada marca única `<p>` do seu site.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-182">You'd have to copy and paste the code into every single `<p>` tag on your site.</span></span>  <span data-ttu-id="2c2ed-183">Isso é muito tempo e esforço.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-183">That's a lot of time and effort.</span></span>  <span data-ttu-id="2c2ed-184">E, se precisar fazer uma edição, você terá que alterar todas as marcas novamente.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-184">And, if you needed to make an edit, you'd have to change every tag again.</span></span>  <span data-ttu-id="2c2ed-185">As **folhas de estilos internas** permitem que você escreva seu CSS uma vez para que ele se aplique a vários elementos.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-185">**Internal stylesheets** allow you to write your CSS once so that it applies to multiple elements.</span></span>  <span data-ttu-id="2c2ed-186">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-186">Try it now:</span></span>  

1.  <span data-ttu-id="2c2ed-187">Na guia ao vivo, clique em **contato** para acessar a página do contato.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-187">In the live tab, click **Contact** to go to the contact page.</span></span>  <span data-ttu-id="2c2ed-188">Observe a fonte de **casa** e do **contato**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-188">Notice the font of **Home** and **Contact**.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-189">Figura 9</span><span class="sxs-lookup"><span data-stu-id="2c2ed-189">Figure 9</span></span>  
    > <span data-ttu-id="2c2ed-190">Página de contato</span><span class="sxs-lookup"><span data-stu-id="2c2ed-190">The Contact page</span></span>  
    > ![Página de contato][ImageCssInternal1]  

1.  <span data-ttu-id="2c2ed-192">Na **guia Editor**, vá para `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-192">In the **editor tab**, go to `contact.html`.</span></span>  
1.  <span data-ttu-id="2c2ed-193">Adicione o código a seguir a `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-193">Add the following code to `contact.html`.</span></span>  <span data-ttu-id="2c2ed-194">Lembre-se de que as linhas começando com `<style>` e terminando `</style>` são o que você precisa adicionar.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-194">Remember, the lines starting with `<style>` and ending with `</style>` are what you need to add.</span></span>  <span data-ttu-id="2c2ed-195">O outro código está aqui para que você saiba onde colocar o novo código.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-195">The other code is just there so you know where to put the new code.</span></span>  
    
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
    
1.  <span data-ttu-id="2c2ed-196">Volte para a **guia ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-196">Go back to the **live tab**.</span></span>  
1.  <span data-ttu-id="2c2ed-197">Clique em **contato** para voltar para a página de contato.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-197">Click **Contact** to go back to the contact page.</span></span>  <span data-ttu-id="2c2ed-198">A fonte de **casa** e o **contato** foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-198">The font of **Home** and **Contact** has changed.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-199">Figura 10</span><span class="sxs-lookup"><span data-stu-id="2c2ed-199">Figure 10</span></span>  
    > <span data-ttu-id="2c2ed-200">A fonte dos links de página inicial e contato foi alterada</span><span class="sxs-lookup"><span data-stu-id="2c2ed-200">The font of the Home and Contact links has changed</span></span>  
    > ![A fonte dos links de página inicial e contato foi alterada][ImageCssInternal2]  
    
### <span data-ttu-id="2c2ed-202">Entender as folhas de estilos internas</span><span class="sxs-lookup"><span data-stu-id="2c2ed-202">Understand internal stylesheets</span></span>   

<span data-ttu-id="2c2ed-203">As folhas de estilos internas aplicam estilos usando **seletores**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-203">Internal stylesheets apply styles using **selectors**.</span></span>  <span data-ttu-id="2c2ed-204">Os seletores são padrões que podem ser aplicados a um ou mais elementos HTML.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-204">Selectors are patterns that may apply to one or more HTML elements.</span></span>  <span data-ttu-id="2c2ed-205">Por exemplo, no código anterior:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-205">For example, in the previous code:</span></span>  

```html
...
    ...
        ...
        <style>
            li a {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

`li a` <span data-ttu-id="2c2ed-206">é um seletor que traduz para "qualquer `<li>` um que contenha um `<a>` ".</span><span class="sxs-lookup"><span data-stu-id="2c2ed-206">is a selector that translates to "any `<li>` that contains an `<a>`".</span></span>  <span data-ttu-id="2c2ed-207">O navegador altera a fonte dos links de **página inicial** e de **contato** porque eles correspondem a esse padrão.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-207">The browser changes the font of the **Home** and **Contact** links because they match this pattern.</span></span>  

```html
...
    ...
        ...
            ...
                <li><a href="/">Home</a></li>
                <li><a href="/contact.html">Contact</a></li>
                ...
            ...
        ...
    ...
...
```  

`font-family: 'Courier New', Courier, serif` <span data-ttu-id="2c2ed-208">é uma **declaração**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-208">is a **declaration**.</span></span>  <span data-ttu-id="2c2ed-209">Uma declaração é feita de duas partes: uma **Propriedade** e um **valor**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-209">A declaration is made of two parts: a **property** and a **value**.</span></span>  `font-family` <span data-ttu-id="2c2ed-210">é a propriedade e `'Courier New', Courier, serif` é o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-210">is the property, and `'Courier New', Courier, serif` is the value of that property.</span></span>  <span data-ttu-id="2c2ed-211">A propriedade descreve uma maneira geral de que você pode alterar o estilo do elemento, e o valor indica exatamente que ele deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-211">The property describes a general way that you can change the element's style, and the value says how exactly it should change.</span></span>  <span data-ttu-id="2c2ed-212">Por exemplo, `font-family: 'Courier New', Courier, serif` o navegador oferece esta instrução: "definir a fonte dos elementos que correspondem ao padrão `li a` `'Courier New'` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-212">For example, `font-family: 'Courier New', Courier, serif` gives the browser this instruction:  "Set the font of elements that match the pattern `li a` to `'Courier New'`.</span></span>  <span data-ttu-id="2c2ed-213">Se essa fonte não estiver disponível, use `Courier` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-213">If that font isn't available, use `Courier`.</span></span>  <span data-ttu-id="2c2ed-214">Se isso não estiver disponível, use `serif` ".</span><span class="sxs-lookup"><span data-stu-id="2c2ed-214">If that isn't available, use `serif`."</span></span>  

### <span data-ttu-id="2c2ed-215">Adicionar vários seletores a um RuleSet</span><span class="sxs-lookup"><span data-stu-id="2c2ed-215">Add multiple selectors to a ruleset</span></span>   

<span data-ttu-id="2c2ed-216">Um bloco de código CSS, como o que você vê abaixo, é chamado de **RuleSet**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-216">A block of CSS code like what you see below is called a **ruleset**.</span></span>  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

<span data-ttu-id="2c2ed-217">Use vírgulas para adicionar vários seletores a um RuleSet.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-217">Use commas to add multiple selectors to a ruleset.</span></span>  <span data-ttu-id="2c2ed-218">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-218">Try it now:</span></span>  

1.  <span data-ttu-id="2c2ed-219">Na **guia Editor**, abra `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-219">In the **editor tab**, open `contact.html`.</span></span>  
1.  <span data-ttu-id="2c2ed-220">Após o `li a` tipo `, h1` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-220">After `li a` type `, h1`.</span></span>  

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

    <span data-ttu-id="2c2ed-221">Isso informa ao navegador para `<h1>` elementos de estilo da mesma maneira que ele estiliza elementos que correspondem ao padrão `li a` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-221">This tells the browser to style `<h1>` elements the same way that it styles elements that match the pattern `li a`.</span></span>  
    
1.  <span data-ttu-id="2c2ed-222">Ir para a **guia ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-222">Go to the **live tab**.</span></span>  
1.  <span data-ttu-id="2c2ed-223">Clique no link do **contato** para voltar para a página de contato.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-223">Click the **Contact** link to go back to the contact page.</span></span>  <span data-ttu-id="2c2ed-224">Agora, **entre em contato comigo!**</span><span class="sxs-lookup"><span data-stu-id="2c2ed-224">Now, **Contact Me!**</span></span> <span data-ttu-id="2c2ed-225">tem a mesma fonte dos links de navegação.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-225">has the same font as the navigation links.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-226">Figura 11</span><span class="sxs-lookup"><span data-stu-id="2c2ed-226">Figure 11</span></span>  
    > <span data-ttu-id="2c2ed-227">O texto ' Fale comigo! '</span><span class="sxs-lookup"><span data-stu-id="2c2ed-227">The text 'Contact Me!'</span></span> <span data-ttu-id="2c2ed-228">Agora tem a mesma fonte dos links de página inicial e de contato</span><span class="sxs-lookup"><span data-stu-id="2c2ed-228">now has the same font as the Home and Contact links</span></span>  
    > ![O texto fale comigo!][ImageCssMultiple1]  

## <span data-ttu-id="2c2ed-231">Experimente com o DevTools</span><span class="sxs-lookup"><span data-stu-id="2c2ed-231">Experiment with DevTools</span></span>   

<span data-ttu-id="2c2ed-232">Ao continuar a viagem para o desenvolvimento mestre na Web, você descobrirá que a CSS pode ser difícil.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-232">As you continue your journey to master web development, you'll find that CSS can be tricky.</span></span>  <span data-ttu-id="2c2ed-233">Você escreverá algumas CSS e esperará que elas sejam exibidas de uma maneira, mas o navegador faz algo completamente diferente.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-233">You'll write some CSS and expect it to display one way, but the browser does something completely different.</span></span>  <span data-ttu-id="2c2ed-234">O Microsoft Edge DevTools torna mais fácil experimentar as alterações e ver imediatamente como essas alterações afetam a página.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-234">Microsoft Edge DevTools makes it easy to experiment with changes and immediately see how those changes affect the page.</span></span>  

### <span data-ttu-id="2c2ed-235">Adicionar uma declaração a um rulet existente no DevTools</span><span class="sxs-lookup"><span data-stu-id="2c2ed-235">Add a declaration to an existing rulest in DevTools</span></span>   

<span data-ttu-id="2c2ed-236">Quando você quiser iterar no estilo de um elemento existente, adicione uma declaração a um RuleSet existente.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-236">When you want to iterate on the style of an existing element, add a declaration to an existing ruleset.</span></span>  <span data-ttu-id="2c2ed-237">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-237">Try it now:</span></span>  

1.  <span data-ttu-id="2c2ed-238">Clique com o botão direito do mouse no link **início** e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-238">Right-click the **Home** link and select **Inspect**.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-239">Figura 12</span><span class="sxs-lookup"><span data-stu-id="2c2ed-239">Figure 12</span></span>  
    > <span data-ttu-id="2c2ed-240">Inspecionar o link home</span><span class="sxs-lookup"><span data-stu-id="2c2ed-240">Inspecting the Home link</span></span>  
    > ![Inspecionar o link home][ImageCssAdd1]  
    
    <span data-ttu-id="2c2ed-242">O DevTools é aberto juntamente com sua página.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-242">DevTools opens up alongside your page.</span></span>  <span data-ttu-id="2c2ed-243">O código que representa o link início `<a href="/">Home</a>` é em azul realçado na árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-243">The code that represents the Home link, `<a href="/">Home</a>` is highlighted blue in the DOM Tree.</span></span>  <span data-ttu-id="2c2ed-244">Isso deve ser familiar em introdução [ao HTML e ao dom][DevToolsBeginnersHtml].</span><span class="sxs-lookup"><span data-stu-id="2c2ed-244">This should be familiar from [Get Started with HTML and the DOM][DevToolsBeginnersHtml].</span></span>  <span data-ttu-id="2c2ed-245">Na guia **estilos** abaixo da árvore DOM, você pode ver a `font-family: 'Courier New', Courier, serif` declaração que você adicionou ao `contact.html` anterior.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-245">In the **Styles** tab below the DOM Tree you can see the `font-family: 'Courier New', Courier, serif` declaration that you added to `contact.html` earlier.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-246">Figura 13</span><span class="sxs-lookup"><span data-stu-id="2c2ed-246">Figure 13</span></span>  
    > <span data-ttu-id="2c2ed-247">A guia estilos está abaixo da árvore DOM</span><span class="sxs-lookup"><span data-stu-id="2c2ed-247">The Styles tab is below the DOM Tree</span></span>  
    > ![A guia estilos está abaixo da árvore DOM][ImageCssAdd2]  
    
    <span data-ttu-id="2c2ed-249">Se a janela do DevTools for ampla, a guia estilos estará à direita da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-249">If your DevTools window is wide, the Styles tab is to the right of the DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-250">Figura 14</span><span class="sxs-lookup"><span data-stu-id="2c2ed-250">Figure 14</span></span>  
    > <span data-ttu-id="2c2ed-251">A guia estilos está à direita da árvore DOM</span><span class="sxs-lookup"><span data-stu-id="2c2ed-251">The Styles tab is to the right of the DOM Tree</span></span>  
    > ![A guia estilos está à direita da árvore DOM][ImageCssAdd3]  
    
1.  <span data-ttu-id="2c2ed-253">Clique no espaço em branco abaixo `font-family: 'Courier New', Courier, Serif` para adicionar uma nova declaração.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-253">Click the whitespace below `font-family: 'Courier New', Courier, Serif` to add a new declaration.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-254">Figura 15</span><span class="sxs-lookup"><span data-stu-id="2c2ed-254">Figure 15</span></span>  
    > <span data-ttu-id="2c2ed-255">Adicionando uma nova declaração</span><span class="sxs-lookup"><span data-stu-id="2c2ed-255">Adding a new declaration</span></span>  
    > ![Adicionando uma nova declaração][ImageCssAdd4]  
    
1.  <span data-ttu-id="2c2ed-257">Digite `color` e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-257">Type `color` and then press `Enter`.</span></span>  <span data-ttu-id="2c2ed-258">A interface do usuário de AutoCompletar sugere opções à medida que você digita.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-258">The autocomplete UI suggests options as you type.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-259">Figura 16</span><span class="sxs-lookup"><span data-stu-id="2c2ed-259">Figure 16</span></span>  
    > <span data-ttu-id="2c2ed-260">Digitação</span><span class="sxs-lookup"><span data-stu-id="2c2ed-260">Typing</span></span> `color`  
    > ![Digitando cor][ImageCssAdd5]  

1.  <span data-ttu-id="2c2ed-262">Digite `magenta` e, em seguida, pressione `Enter` novamente.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-262">Type `magenta` and then press `Enter` again.</span></span>  <span data-ttu-id="2c2ed-263">Todo o texto na página de contato agora é magenta.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-263">All of the text on the contact page is now magenta.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-264">Figura 17</span><span class="sxs-lookup"><span data-stu-id="2c2ed-264">Figure 17</span></span>  
    > <span data-ttu-id="2c2ed-265">Digitação</span><span class="sxs-lookup"><span data-stu-id="2c2ed-265">Typing</span></span> `magenta`  
    > ![Digitando magenta][ImageCssAdd6]  
    
### <span data-ttu-id="2c2ed-267">Editar uma declaração no DevTools</span><span class="sxs-lookup"><span data-stu-id="2c2ed-267">Edit a declaration in DevTools</span></span>   

<span data-ttu-id="2c2ed-268">Você também pode editar declarações existentes no DevTools.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-268">You can also edit existing declarations in DevTools.</span></span>  <span data-ttu-id="2c2ed-269">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-269">Try it now:</span></span>  

1.  <span data-ttu-id="2c2ed-270">Clique no quadrado magenta ao lado de `magenta` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-270">Click the magenta square next to `magenta`.</span></span>  <span data-ttu-id="2c2ed-271">Um seletor de cores aparece.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-271">A color picker pops up.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-272">Figura 18</span><span class="sxs-lookup"><span data-stu-id="2c2ed-272">Figure 18</span></span>  
    > <span data-ttu-id="2c2ed-273">O seletor de cores</span><span class="sxs-lookup"><span data-stu-id="2c2ed-273">The Color Picker</span></span>  
    > ![O seletor de cores][ImageCssEdit1]  
    
1.  <span data-ttu-id="2c2ed-275">Use o seletor de cores para alterar o texto da fonte para uma cor que você quiser.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-275">Use the color picker to change the font text to a color that you like.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-276">Figura 19</span><span class="sxs-lookup"><span data-stu-id="2c2ed-276">Figure 19</span></span>  
    > <span data-ttu-id="2c2ed-277">Alterando a cor da fonte para roxo com o seletor de cores</span><span class="sxs-lookup"><span data-stu-id="2c2ed-277">Changing the font color to purple with the Color Picker</span></span>  
    > ![Alterando a cor da fonte para roxo com o seletor de cores][ImageCssEdit2]  

### <span data-ttu-id="2c2ed-279">Adicionar um novo RuleSet no DevTools</span><span class="sxs-lookup"><span data-stu-id="2c2ed-279">Add a new ruleset in DevTools</span></span>   

<span data-ttu-id="2c2ed-280">Você também pode adicionar novos RuleSets ao DevTools.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-280">You can also add new rulesets in DevTools.</span></span>  <span data-ttu-id="2c2ed-281">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-281">Try it now:</span></span>  

1.  <span data-ttu-id="2c2ed-282">Clique em nova regra de **estilo** ![ nova regra ][ImageNewStyleRuleIcon] de estilo que está ao lado de **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-282">Click **New Style Rule** ![New Style Rule][ImageNewStyleRuleIcon] which is next to **.cls**.</span></span>  <span data-ttu-id="2c2ed-283">Um RuleSet vazio aparece `a` como o seletor.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-283">An empty ruleset appears with `a` as the selector.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-284">Figura 20</span><span class="sxs-lookup"><span data-stu-id="2c2ed-284">Figure 20</span></span>  
    > <span data-ttu-id="2c2ed-285">Adicionando uma nova regra</span><span class="sxs-lookup"><span data-stu-id="2c2ed-285">Adding a new rule</span></span>  
    > ![Adicionando uma nova regra][ImageCssRule1]  
    
1.  <span data-ttu-id="2c2ed-287">Substituir `a` por `a:hover` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-287">Replace `a` with `a:hover`.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-288">Figura 21</span><span class="sxs-lookup"><span data-stu-id="2c2ed-288">Figure 21</span></span>  
    > <span data-ttu-id="2c2ed-289">Substituindo `a` por</span><span class="sxs-lookup"><span data-stu-id="2c2ed-289">Replacing `a` with</span></span> `a:hover`  
    > ![Substituindo a com a:hover][ImageCssRule2]  
    
    `:hover` <span data-ttu-id="2c2ed-291">é uma **pseudo-classe**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-291">is a **pseudo-class**.</span></span>  <span data-ttu-id="2c2ed-292">Use pseudovariáveis para elementos de estilo quando eles inserem Estados especiais.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-292">Use pseudo-classes to style elements when they enter special states.</span></span>  <span data-ttu-id="2c2ed-293">Por exemplo, o `a:hover` estilo somente tem efeito quando você estiver passando o mouse sobre um `<a>` elemento.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-293">For example, the `a:hover` style only takes effect when you're hovering over an `<a>` element.</span></span>  
    
1.  <span data-ttu-id="2c2ed-294">Clique entre os colchetes para adicionar uma nova declaração.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-294">Click between the brackets to add a new declaration.</span></span>  
1.  <span data-ttu-id="2c2ed-295">Digite `background-color` o nome da declaração e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-295">Type `background-color` for the declaration name and then press `Enter`.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-296">Figura 22</span><span class="sxs-lookup"><span data-stu-id="2c2ed-296">Figure 22</span></span>  
    > <span data-ttu-id="2c2ed-297">Digitação</span><span class="sxs-lookup"><span data-stu-id="2c2ed-297">Typing</span></span> `background-color`  
    > ![Digitando a cor da tela de fundo][ImageCssRule3]  
    
1.  <span data-ttu-id="2c2ed-299">Digite `green` o valor da declaração e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-299">Type `green` for the declaration value and then press `Enter`.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-300">Figura 23</span><span class="sxs-lookup"><span data-stu-id="2c2ed-300">Figure 23</span></span>  
    > <span data-ttu-id="2c2ed-301">Digitação</span><span class="sxs-lookup"><span data-stu-id="2c2ed-301">Typing</span></span> `green`  
    > ![Digitando verde][ImageCssRule4]  
    
1.  <span data-ttu-id="2c2ed-303">Passe o mouse sobre o link **início** .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-303">Hover your mouse over the **Home** link.</span></span>  <span data-ttu-id="2c2ed-304">O plano de fundo do link fica verde.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-304">The background of the link turns green.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-305">Figura 24</span><span class="sxs-lookup"><span data-stu-id="2c2ed-305">Figure 24</span></span>  
    > <span data-ttu-id="2c2ed-306">Passando o mouse sobre o link home para revelar seu plano de fundo verde</span><span class="sxs-lookup"><span data-stu-id="2c2ed-306">Hovering over the Home link to reveal its green background</span></span>  
    > ![Passando o mouse sobre o link home para revelar seu plano de fundo verde][ImageCssRule5]  
    
## <span data-ttu-id="2c2ed-308">Reutilizar estilos em páginas com folhas de estilo externas</span><span class="sxs-lookup"><span data-stu-id="2c2ed-308">Re-use styles across pages with external stylesheets</span></span>   

<span data-ttu-id="2c2ed-309">Antes de você ter adicionado esta folha de estilos interna a `contact.html` :</span><span class="sxs-lookup"><span data-stu-id="2c2ed-309">Earlier you added this internal stylesheet to `contact.html`:</span></span>  

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

<span data-ttu-id="2c2ed-310">E se você quisesse estilizar `index.html` da mesma maneira?</span><span class="sxs-lookup"><span data-stu-id="2c2ed-310">What if you wanted to style `index.html` the same way?</span></span>  <span data-ttu-id="2c2ed-311">E se você tiver *milhares* de páginas e quiser aplicar esses estilos a todas elas?</span><span class="sxs-lookup"><span data-stu-id="2c2ed-311">What if you had a *thousand* pages and you wanted to apply these styles to all of them?</span></span>  <span data-ttu-id="2c2ed-312">Você precisaria copiar e colar esta folha de estilos interna em cada página da Web em seu site.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-312">You'd have to copy and paste this internal stylesheet into every single web page on your site.</span></span>  <span data-ttu-id="2c2ed-313">As **folhas de estilo externas** permitem que você escreva a CSS uma vez, aplica-a a várias páginas.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-313">**External stylesheets** allow you to write your CSS once yet apply it to multiple pages.</span></span>  <span data-ttu-id="2c2ed-314">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-314">Try it now:</span></span>  

1.  <span data-ttu-id="2c2ed-315">Primeiro, recarregue a guia ao vivo para remover as alterações feitas no DevTools.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-315">First, reload the live tab to remove the changes that you made in DevTools.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-316">Figura 25</span><span class="sxs-lookup"><span data-stu-id="2c2ed-316">Figure 25</span></span>  
    >  <span data-ttu-id="2c2ed-317">Depois de recarregar a página, as alterações feitas no DevTools são perdidas</span><span class="sxs-lookup"><span data-stu-id="2c2ed-317">After reloading the page the changes that were made in DevTools are gone</span></span>  
    > ![ <span data-ttu-id="2c2ed-318">Depois de recarregar a página, as alterações feitas no DevTools são perdidas</span><span class="sxs-lookup"><span data-stu-id="2c2ed-318">After reloading the page the changes that were made in DevTools are gone</span></span>][ImageCssExternal01]  
    
1.  <span data-ttu-id="2c2ed-319">Volte para a **guia Editor** e abra `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-319">Go back to the **editor tab** and open `contact.html`.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-320">Figura 26</span><span class="sxs-lookup"><span data-stu-id="2c2ed-320">Figure 26</span></span>  
    > `contact.html`  
    > ![contact.html][ImageCssExternal02]  
    
1.  <span data-ttu-id="2c2ed-322">Exclua tudo entre `<style>` e `</style>` , incluindo `<style>` e `</style>` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-322">Delete everything between `<style>` and `</style>`, including `<style>` and `</style>`.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-323">Figura 27</span><span class="sxs-lookup"><span data-stu-id="2c2ed-323">Figure 27</span></span>  
    > <span data-ttu-id="2c2ed-324">A marca de estilo foi removida</span><span class="sxs-lookup"><span data-stu-id="2c2ed-324">The style tag has been removed</span></span>  
    > ![A marca de estilo foi removida][ImageCssExternal03]  
    
1.  <span data-ttu-id="2c2ed-326">Vá para `index.html` e remova `style="background-color: aliceblue;"` da `<nav>` marca.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-326">Go to `index.html` and remove `style="background-color: aliceblue;"` from the `<nav>` tag.</span></span>  <span data-ttu-id="2c2ed-327">Você já removeu toda a CSS que você adicionou anteriormente ao seu site.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-327">You have now removed all of the CSS that you previously added to your site.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-328">Figura 28</span><span class="sxs-lookup"><span data-stu-id="2c2ed-328">Figure 28</span></span>  
    > <span data-ttu-id="2c2ed-329">O estilo embutido foi removido do elemento NAV</span><span class="sxs-lookup"><span data-stu-id="2c2ed-329">The inline style has been removed from the nav element</span></span>  
    > ![O estilo embutido foi removido do elemento NAV][ImageCssExternal04]  

1.  <span data-ttu-id="2c2ed-331">Clique em **novo arquivo**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-331">Click **New File**.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-332">Figura 29</span><span class="sxs-lookup"><span data-stu-id="2c2ed-332">Figure 29</span></span>  
    > <span data-ttu-id="2c2ed-333">A caixa de diálogo novo arquivo</span><span class="sxs-lookup"><span data-stu-id="2c2ed-333">The new file dialog</span></span>  
    > ![A caixa de diálogo novo arquivo][ImageCssExternal05]  
    
1.  <span data-ttu-id="2c2ed-335">Substituir `cool-file.js` por `style.css` e, em seguida, clique em **Adicionar arquivo**.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-335">Replace `cool-file.js` with `style.css` and then click **Add File**.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-336">Figura 30</span><span class="sxs-lookup"><span data-stu-id="2c2ed-336">Figure 30</span></span>  
    > <span data-ttu-id="2c2ed-337">Digitação</span><span class="sxs-lookup"><span data-stu-id="2c2ed-337">Typing</span></span> `style.css`  
    > ![Digitando Style. css][ImageCssExternal06]  
    
1.  <span data-ttu-id="2c2ed-339">Cole este código em `style.css` :</span><span class="sxs-lookup"><span data-stu-id="2c2ed-339">Paste this code into `style.css`:</span></span>  
    
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
    
    > ##### <span data-ttu-id="2c2ed-340">Figura 31</span><span class="sxs-lookup"><span data-stu-id="2c2ed-340">Figure 31</span></span>  
    > <span data-ttu-id="2c2ed-341">Adicionando código a</span><span class="sxs-lookup"><span data-stu-id="2c2ed-341">Adding code to</span></span> `style.css`  
    > ![Adicionando código ao Style. css][ImageCssExternal07]  
    
    <span data-ttu-id="2c2ed-343">Nesse ponto, você criou uma folha de estilos externa, mas o HTML não sabe que ela existe, ainda.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-343">At this point, you have created an external stylesheet, but your HTML doesn't know that it exists, yet.</span></span>  
    
1.  <span data-ttu-id="2c2ed-344">Abrir `index.html` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-344">Open `index.html`.</span></span>  
1.  <span data-ttu-id="2c2ed-345">Adicione `<link rel="stylesheet" href="style.css">` ao seu HTML.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-345">Add `<link rel="stylesheet" href="style.css">` to your HTML.</span></span>  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <link rel="stylesheet" href="style.css">
        </head>
        ...
    ...
    ```  

    > ##### <span data-ttu-id="2c2ed-346">Figura 32</span><span class="sxs-lookup"><span data-stu-id="2c2ed-346">Figure 32</span></span>  
    > <span data-ttu-id="2c2ed-347">Vinculando a</span><span class="sxs-lookup"><span data-stu-id="2c2ed-347">Linking to</span></span> `style.css`  
    > ![Vinculando a Style. css][ImageCssExternal08]  

1.  <span data-ttu-id="2c2ed-349">Acesse `contact.html` e adicione o link lá também.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-349">Go to `contact.html` and add the link there, too.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-350">Figura 33</span><span class="sxs-lookup"><span data-stu-id="2c2ed-350">Figure 33</span></span>  
    > <span data-ttu-id="2c2ed-351">Vinculando a `style.css` em</span><span class="sxs-lookup"><span data-stu-id="2c2ed-351">Linking to `style.css` in</span></span> `contact.html`  
    > ![Vinculando a Style. CSS em contact.html][ImageCssExternal09]  

1.  <span data-ttu-id="2c2ed-353">Ir para a **guia ao vivo**.  A Home Page agora tem a mesma fonte da última seção e uma seção azul de navegação.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-353">Go to the **live tab**.  The home page now has the same font from the last section and a blue navigation section.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-354">Figura 34</span><span class="sxs-lookup"><span data-stu-id="2c2ed-354">Figure 34</span></span>  
    > <span data-ttu-id="2c2ed-355">A Home Page</span><span class="sxs-lookup"><span data-stu-id="2c2ed-355">The home page</span></span>  
    > ![A Home Page][ImageCssExternal10]  
    
1.  <span data-ttu-id="2c2ed-357">Clique no link do **contato** para acessar a página do contato.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-357">Click the **Contact** link to go to the contact page.</span></span>  <span data-ttu-id="2c2ed-358">A página de contato tem a mesma formatação que a Home Page.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-358">The contact page has the same formatting as the home page.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-359">Figura 35</span><span class="sxs-lookup"><span data-stu-id="2c2ed-359">Figure 35</span></span>  
    > <span data-ttu-id="2c2ed-360">Página de contato</span><span class="sxs-lookup"><span data-stu-id="2c2ed-360">The contact page</span></span>  
    > ![Página de contato][ImageCssExternal11]  
    
## <span data-ttu-id="2c2ed-362">Usar uma estrutura CSS</span><span class="sxs-lookup"><span data-stu-id="2c2ed-362">Use a CSS framework</span></span>   

<span data-ttu-id="2c2ed-363">**Estruturas CSS** são coleções de estilos criados por outros desenvolvedores que facilitam a criação de sites atraentes.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-363">**CSS frameworks** are collections of styles built by other developers that make it easier to create attractive web sites.</span></span>  <span data-ttu-id="2c2ed-364">Em vez de definir estilos por conta própria, uma estrutura oferece um conjunto de estilos que você pode usar em seus elementos de página.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-364">Instead of defining styles yourself, a framework gives you a collection of styles that you can use on your page elements.</span></span>  

1.  <span data-ttu-id="2c2ed-365">Copie o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-365">Copy the following code:</span></span>  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  <span data-ttu-id="2c2ed-366">Vá para a guia edição e cole o código em `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-366">Go to the editing tab and paste the code into `contact.html`.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-367">Figura 36</span><span class="sxs-lookup"><span data-stu-id="2c2ed-367">Figure 36</span></span>  
    > <span data-ttu-id="2c2ed-368">Vinculando à estrutura em</span><span class="sxs-lookup"><span data-stu-id="2c2ed-368">Linking to the framework in</span></span> `contact.html`  
    > ![Vinculando à estrutura no contact.html][ImageCssFramework1]  
    
1.  <span data-ttu-id="2c2ed-370">Cole o código em `index.html` , também.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-370">Paste the code into `index.html`, as well.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-371">Figura 37</span><span class="sxs-lookup"><span data-stu-id="2c2ed-371">Figure 37</span></span>  
    > <span data-ttu-id="2c2ed-372">Vinculando à estrutura em</span><span class="sxs-lookup"><span data-stu-id="2c2ed-372">Linking to the framework in</span></span> `index.html`  
    > ![Vinculando à estrutura no index.html][ImageCssFramework2]  
    
1.  <span data-ttu-id="2c2ed-374">Volte para a guia ao vivo para ver suas alterações.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-374">Go back to the live tab to view your changes.</span></span>  <span data-ttu-id="2c2ed-375">Enquanto a cor do plano de fundo da `<nav>` fonte e da fonte dos `li a` elementos são iguais, a fonte dos outros elementos mudava.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-375">While the background color of the `<nav>` and the font of the `li a` elements are the same, the font of the other elements has changed.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-376">Figura 38</span><span class="sxs-lookup"><span data-stu-id="2c2ed-376">Figure 38</span></span>  
    > <span data-ttu-id="2c2ed-377">Algumas fontes na Home Page foram alteradas devido à estrutura</span><span class="sxs-lookup"><span data-stu-id="2c2ed-377">Some of the font on the home page has changed because of the framework</span></span>  
    > ![Algumas fontes na Home Page foram alteradas devido à estrutura][ImageCssFramework3]  

### <span data-ttu-id="2c2ed-379">Usar uma classe</span><span class="sxs-lookup"><span data-stu-id="2c2ed-379">Use a class</span></span>   

<span data-ttu-id="2c2ed-380">Na última seção, você adicionou a inicialização às páginas da Web, o que altera as fontes de alguns dos elementos do seu site.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-380">In the last section, you added Bootstrap to your web pages, which changed the fonts of some of the elements on your site.</span></span>  <span data-ttu-id="2c2ed-381">As estruturas CSS podem ajudá-lo a fazer alterações importantes na sua página com um pouco de código.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-381">CSS frameworks can help you make major changes to your page with very little code.</span></span>  <span data-ttu-id="2c2ed-382">Experimente agora alterando seu cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-382">Try it now by changing your header:</span></span>  

1.  <span data-ttu-id="2c2ed-383">Copie este código:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-383">Copy this code:</span></span>  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  <span data-ttu-id="2c2ed-384">Adicione este código à sua `<header>` marca `index.html` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-384">Add this code to your `<header>` tag in `index.html`.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-385">Figura 39</span><span class="sxs-lookup"><span data-stu-id="2c2ed-385">Figure 39</span></span>  
    > <span data-ttu-id="2c2ed-386">Adicionando classes em</span><span class="sxs-lookup"><span data-stu-id="2c2ed-386">Adding classes in</span></span> `index.html`  
    > ![Adicionando classes no index.html][ImageCssJumbotron1]  
    
1.  <span data-ttu-id="2c2ed-388">Adicione também o código à sua `<header>` marca `contact.html` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-388">Add the code to your `<header>` tag in `contact.html`, too.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-389">Figura 40</span><span class="sxs-lookup"><span data-stu-id="2c2ed-389">Figure 40</span></span>  
    > <span data-ttu-id="2c2ed-390">Adicionando classes em</span><span class="sxs-lookup"><span data-stu-id="2c2ed-390">Adding classes in</span></span> `contact.html`  
    > ![Adicionando classes no contact.html][ImageCssJumbotron2]  
    
1.  <span data-ttu-id="2c2ed-392">Exiba suas alterações na guia ao vivo.  Há uma grande caixa cinza em torno do seu cabeçalho agora.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-392">View your changes in the live tab.  There's a big, grey box around your header now.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-393">Figura 41</span><span class="sxs-lookup"><span data-stu-id="2c2ed-393">Figure 41</span></span>  
    > <span data-ttu-id="2c2ed-394">Agora o cabeçalho tem uma grande caixa cinza ao seu lado</span><span class="sxs-lookup"><span data-stu-id="2c2ed-394">The header now has a big, grey box around it</span></span>  
    > ![Agora o cabeçalho tem uma grande caixa cinza ao seu lado][ImageCssJumbotron3]  
    
### <span data-ttu-id="2c2ed-396">Compreender classes</span><span class="sxs-lookup"><span data-stu-id="2c2ed-396">Understand classes</span></span>   

<span data-ttu-id="2c2ed-397">As classes permitem atribuir coleções de estilos a elementos arbitrários.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-397">Classes let you assign collections of styles to arbitrary elements.</span></span>  <span data-ttu-id="2c2ed-398">Por exemplo, configurar o `class` atributo das `<header>` marcas para `jumbotron` aplicar os seguintes estilos a elas:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-398">For example, setting the `class` attribute of the `<header>` tags to `jumbotron` applied the following styles to them:</span></span>  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

<span data-ttu-id="2c2ed-399">Uma vantagem das classes é que elas permitem aplicar estilos a qualquer elemento desejado.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-399">One advantage of classes is that they let you apply styles to whatever elements you want.</span></span>  <span data-ttu-id="2c2ed-400">Por exemplo, suponha que você queira definir a cor da tela de fundo de *alguns* `<p>` elementos como roxo, mas não *todos* eles.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-400">For example, suppose you want to set the background color of *some* `<p>` elements to purple, but not *all* of them.</span></span>  <span data-ttu-id="2c2ed-401">Você pode definir o estilo em uma classe:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-401">You could define the style in a class:</span></span>  

```css
.custom-background {
  background-color: purple;
}
```  

<span data-ttu-id="2c2ed-402">E, em seguida, aplicar a classe somente aos `<p>` elementos que você deseja estilizar:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-402">And then apply the class to only the `<p>` elements that you want to style:</span></span>  

```html
...
    ...
        ...
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        ...
    ...
...
```  

### <span data-ttu-id="2c2ed-403">Alinhar elementos</span><span class="sxs-lookup"><span data-stu-id="2c2ed-403">Align elements</span></span>   

<span data-ttu-id="2c2ed-404">Bootstrap também fornece classes para alinhar elementos.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-404">Bootstrap also provides classes for aligning elements.</span></span>  <span data-ttu-id="2c2ed-405">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="2c2ed-405">Try it now:</span></span>  

1.  <span data-ttu-id="2c2ed-406">Volte para a guia Editor e abra `index.html` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-406">Go back to the editor tab and open `index.html`.</span></span>  
1.  <span data-ttu-id="2c2ed-407">Adicionar `class="container-fluid"` à sua `<body>` marca.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-407">Add `class="container-fluid"` to your `<body>` tag.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-408">Figura 42</span><span class="sxs-lookup"><span data-stu-id="2c2ed-408">Figure 42</span></span>  
    > <span data-ttu-id="2c2ed-409">Adicionar a `container-fluid` classe</span><span class="sxs-lookup"><span data-stu-id="2c2ed-409">Adding the `container-fluid` class</span></span>  
    > ![Adicionando a classe container-fluido][ImageCssAlign1]  

1.  <span data-ttu-id="2c2ed-411">Envolver seus `<nav>` `<main>` elementos e em `<div class="row">` .</span><span class="sxs-lookup"><span data-stu-id="2c2ed-411">Wrap your `<nav>` and `<main>` elements in `<div class="row">`.</span></span>  <span data-ttu-id="2c2ed-412">Certifique-se de colocar `</div>` após para `</main>` fechar corretamente a nova marca.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-412">Make sure to put `</div>` after `</main>` in order to properly close the new tag.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-413">Figura 43</span><span class="sxs-lookup"><span data-stu-id="2c2ed-413">Figure 43</span></span>  
    > <span data-ttu-id="2c2ed-414">Adicionar uma linha</span><span class="sxs-lookup"><span data-stu-id="2c2ed-414">Adding a row</span></span>  
    > ![Adicionar uma linha][ImageCssAlign2]  
    
1.  <span data-ttu-id="2c2ed-416">Adicione `class="col-3"` à sua `<nav>` marca e `class="col-9"` à sua `<main>` marca.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-416">Add `class="col-3"` to your `<nav>` tag and `class="col-9"` to your `<main>` tag.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-417">Figura 44</span><span class="sxs-lookup"><span data-stu-id="2c2ed-417">Figure 44</span></span>  
    > <span data-ttu-id="2c2ed-418">Adicionando as `col-3` `col-9` classes e</span><span class="sxs-lookup"><span data-stu-id="2c2ed-418">Adding the `col-3` and `col-9` classes</span></span>  
    > ![Adicionando as classes Col-3 e col-9][ImageCssAlign3]  
    
1.  <span data-ttu-id="2c2ed-420">Exiba suas alterações na guia ao vivo.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-420">View your changes in the live tab.</span></span>  
    
    > ##### <span data-ttu-id="2c2ed-421">Figura 45</span><span class="sxs-lookup"><span data-stu-id="2c2ed-421">Figure 45</span></span>  
    > <span data-ttu-id="2c2ed-422">O conteúdo de NAV agora está à esquerda do conteúdo principal</span><span class="sxs-lookup"><span data-stu-id="2c2ed-422">The nav content is now to the left of the main content</span></span>  
    > ![O conteúdo de NAV agora está à esquerda do conteúdo principal][ImageCssAlign4]  
    
## <span data-ttu-id="2c2ed-424">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="2c2ed-424">Next steps</span></span>   

<span data-ttu-id="2c2ed-425">Parabéns!</span><span class="sxs-lookup"><span data-stu-id="2c2ed-425">Congratulations!</span></span>  <span data-ttu-id="2c2ed-426">Concluído!</span><span class="sxs-lookup"><span data-stu-id="2c2ed-426">You're done!</span></span>  

*   <span data-ttu-id="2c2ed-427">A melhor maneira de ficar melhor no desenvolvimento na Web é criar mais sites.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-427">The best way to get better at web development is to build more sites.</span></span>  <span data-ttu-id="2c2ed-428">Não se preocupe em quebrar itens.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-428">Don't worry about breaking stuff.</span></span>  <span data-ttu-id="2c2ed-429">Só Divirta-se e saiba o quanto puder ao longo do caminho.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-429">Just have fun and learn as much as you can along the way.</span></span>  
*   <span data-ttu-id="2c2ed-430">Consulte [a introdução à CSS][MDNCssFirstSteps] para saber mais sobre o estilo de páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-430">Check out [Introduction to CSS][MDNCssFirstSteps] to learn lots more about styling web pages.</span></span>  
*   <span data-ttu-id="2c2ed-431">Trabalhe com o tutorial de introdução ao [Exibir e alterar][DevtoolsCssIndex] o tutorial em CSS para saber mais sobre como você pode usar o devtools para experimentar a CSS de uma página.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-431">Work through our [Get Started with Viewing and Changing CSS][DevtoolsCssIndex] tutorial to learn more about how you can use DevTools to experiment with a page's CSS.</span></span>  

<!--- image links --->  

[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  

[ImageCssIntro1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro1.msft.png "Figura 1: o que o site tem atualmente"  
[ImageCssIntro2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro2.msft.png "Figura 2: qual será a aparência do seu site no final do tutorial"  
[ImageCssSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup1.msft.png "Figura 3: a guia edição"  
[ImageCssSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup2.msft.png "Figura 4: o menu de opções do Project"  
[ImageCssSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup3.msft.png "Figura 5: a guia ao vivo"  
[ImageCssStyled]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-red_paragraph.msft.png "Figura 6: foi estilizado com CSS"  
[ImageCssInline1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline1.msft.png "Figura 7: index.html"  
[ImageCssInline2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline2.msft.png "Figura 8: a cor da tela de fundo por trás dos links para casa e contatos agora está azul"  
[ImageCssInternal1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal1.msft.png "Figura 9: página de contato"  
[ImageCssInternal2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal2.msft.png "Figura 10: a fonte dos links de página inicial e de contato foi alterada"  
[ImageCssMultiple1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-multiple1.msft.png "Figura 11: o texto "entrar em contato!" agora tem a mesma fonte dos links de página inicial e de contato"  
[ImageCssAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add1.msft.png "Figura 12: inspecionar o link home"  
[ImageCssAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add2.msft.png "Figura 13: a guia estilos está abaixo da árvore DOM"  
[ImageCssAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add3.msft.png "Figura 14: a guia estilos está à direita da árvore DOM"  
[ImageCssAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add4.msft.png "Figura 15: adicionando uma nova declaração"
[ImageCssAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add5.msft.png "Figura 16: digitando cor"  
[ImageCssAdd6]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add6.msft.png "Figura 17: digitação de magenta"  
[ImageCssEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit1.msft.png "Figura 18: o seletor de cores"  
[ImageCssEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit2.msft.png "Figura 19: alterando a cor da fonte para roxo com o seletor de cores"  
[ImageCssRule1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule1.msft.png "Figura 20: adicionando uma nova regra"  
[ImageCssRule2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule2.msft.png "Figura 21: substituindo a com a:hover"  
[ImageCssRule3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule3.msft.png "Figura 22: digitando a cor da tela de fundo"  
[ImageCssRule4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule4.msft.png "Figura 23: digitando verde"  
[ImageCssRule5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule5.msft.png "Figura 24: passando o mouse sobre o link home para revelar o plano de fundo verde"  
[ImageCssExternal01]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external1.msft.png "Figura 25: depois de recarregar a página, as alterações feitas no DevTools são perdidas"  
[ImageCssExternal02]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external2.msft.png "Figura 26: contact.html"  
[ImageCssExternal03]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external3.msft.png "Figura 27: a marca de estilo foi removida"  
[ImageCssExternal04]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external4.msft.png "Figura 28: o estilo embutido foi removido do elemento NAV"  
[ImageCssExternal05]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external5.msft.png "Figura 29: a caixa de diálogo novo arquivo"  
[ImageCssExternal06]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external6.msft.png "Figura 30: digitando Style. css"  
[ImageCssExternal07]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external7.msft.png "Figura 31: adicionando código ao estilo. css"  
[ImageCssExternal08]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external8.msft.png "Figura 32: vinculando ao estilo. css"  
[ImageCssExternal09]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external9.msft.png "Figura 33: vinculando ao estilo. CSS em contact.html"  
[ImageCssExternal10]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external10.msft.png "Figura 34: a Home Page"  
[ImageCssExternal11]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external11.msft.png "Figura 35: a página de contato"  
[ImageCssFramework1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework1.msft.png "Figura 36: vinculando à estrutura no contact.html"  
[ImageCssFramework2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework2.msft.png "Figura 37: vinculando à estrutura no index.html"  
[ImageCssFramework3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework3.msft.png "Figura 38: parte da fonte da página inicial foi alterada devido à estrutura"  
[ImageCssJumbotron1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron1.msft.png "Figura 39: adicionando classes no index.html"  
[ImageCssJumbotron2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron2.msft.png "Figura 40: adicionando classes no contact.html"  
[ImageCssJumbotron3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron3.msft.png "Figura 41: o cabeçalho agora tem uma grande caixa cinza ao seu lado"  
[ImageCssAlign1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align1.msft.png "Figura 42: adicionando a classe container-fluido"  
[ImageCssAlign2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align2.msft.png "Figura 43: adicionando uma linha"  
[ImageCssAlign3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align3.msft.png "Figura 44: adicionando as classes Col-3 e col-9"  
[ImageCssAlign4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align4.msft.png "Figura 45: o conteúdo de NAV agora está à esquerda do conteúdo principal"  

<!--- links  --->  

[DevToolsBeginnersHtml]: html.md "DevTools para iniciantes: introdução ao HTML e ao DOM"  
[DevtoolsCssIndex]: ../css/index.md "Introdução à exibição e alteração de CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-cozinhá-Amphibian | Problema"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Primeiras etapas da CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="2c2ed-482">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="2c2ed-482">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2c2ed-483">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/beginners/css) e é criada pela [Katherine Jackson][KatherineJackson] \ (redatora técnica, Chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="2c2ed-483">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/css) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2c2ed-485">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2c2ed-485">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
