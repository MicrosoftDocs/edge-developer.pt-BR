---
title: DevTools para iniciantes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 8695fe1b2c5d78bd074447acd26a1f01a5833b2d
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581584"
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

# <span data-ttu-id="8f65c-103">DevTools para iniciantes: introdução ao HTML e ao DOM</span><span class="sxs-lookup"><span data-stu-id="8f65c-103">DevTools for Beginners: Get Started with HTML and the DOM</span></span>   

<span data-ttu-id="8f65c-104">Esta é a primeira em uma série de tutoriais que ensinam noções básicas sobre o desenvolvimento na Web.</span><span class="sxs-lookup"><span data-stu-id="8f65c-104">This is the first in a series of tutorials that teach you the basics of web development.</span></span>  <span data-ttu-id="8f65c-105">Você também aprenderá sobre um conjunto de ferramentas de desenvolvedor da Web, chamado Microsoft Edge DevTools, que podem aumentar sua produtividade.</span><span class="sxs-lookup"><span data-stu-id="8f65c-105">You will also learn about a set of web developer tools called Microsoft Edge DevTools that can increase your productivity.</span></span>  

<span data-ttu-id="8f65c-106">Neste tutorial específico, você aprenderá sobre HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="8f65c-106">In this particular tutorial, you learn about HTML and the DOM.</span></span>  <span data-ttu-id="8f65c-107">O HTML é uma das principais tecnologias de desenvolvimento na Web.</span><span class="sxs-lookup"><span data-stu-id="8f65c-107">HTML is one of the core technologies of web development.</span></span>  <span data-ttu-id="8f65c-108">É o idioma que controla a estrutura e o conteúdo das páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="8f65c-108">It is the language that controls the structure and content of webpages.</span></span>  <span data-ttu-id="8f65c-109">O DOM também está relacionado à estrutura e ao conteúdo de páginas da Web, mas você aprenderá mais sobre isso mais tarde.</span><span class="sxs-lookup"><span data-stu-id="8f65c-109">The DOM is also related to the structure and content of webpages, but you'll learn more about that later.</span></span>  

## <span data-ttu-id="8f65c-110">Goal</span><span class="sxs-lookup"><span data-stu-id="8f65c-110">Goals</span></span>   

<span data-ttu-id="8f65c-111">Você aprenderá a desenvolver na Web Criando seu próprio website.</span><span class="sxs-lookup"><span data-stu-id="8f65c-111">You are going to learn web development by actually building your own website.</span></span>  <span data-ttu-id="8f65c-112">Quando você concluir todos os tutoriais da série *devtools para iniciantes* , o seu site final terá a aparência da **Figura 1**.</span><span class="sxs-lookup"><span data-stu-id="8f65c-112">By the time you complete all of the tutorials in the *DevTools for Beginners* series, your finished site will look like **Figure 1**.</span></span>  

> ##### <span data-ttu-id="8f65c-113">Figura 1</span><span class="sxs-lookup"><span data-stu-id="8f65c-113">Figure 1</span></span>  
> <span data-ttu-id="8f65c-114">O site concluído</span><span class="sxs-lookup"><span data-stu-id="8f65c-114">The finished site</span></span>  
> ![O site concluído][ImageHtmlFinished]  

<span data-ttu-id="8f65c-116">No final deste tutorial, você compreenderá:</span><span class="sxs-lookup"><span data-stu-id="8f65c-116">By the end of this tutorial, you will understand:</span></span>  

*   <span data-ttu-id="8f65c-117">Como o HTML e o DOM criam o conteúdo que você vê nas páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="8f65c-117">How HTML and the DOM create the content that you see on webpages.</span></span>  
*   <span data-ttu-id="8f65c-118">Como o Microsoft Edge DevTools pode ajudá-lo a experimentar alterações em HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="8f65c-118">How Microsoft Edge DevTools can help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="8f65c-119">A diferença entre HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="8f65c-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="8f65c-120">Você também terá um site real!</span><span class="sxs-lookup"><span data-stu-id="8f65c-120">You'll also have a real website!</span></span>  <span data-ttu-id="8f65c-121">Você pode usar este site para hospedar seu currículo ou blog.</span><span class="sxs-lookup"><span data-stu-id="8f65c-121">You can use this site to host your resume or blog.</span></span>  

## <span data-ttu-id="8f65c-122">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="8f65c-122">Prerequisites</span></span>   

<span data-ttu-id="8f65c-123">Antes de tentar este tutorial, complete os seguintes pré-requisitos:</span><span class="sxs-lookup"><span data-stu-id="8f65c-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="8f65c-124">Se você não estiver familiarizado com HTML, leia [introdução ao HTML][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="8f65c-124">If you're unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="8f65c-125">Baixar o navegador da Web [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="8f65c-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="8f65c-126">Este tutorial usa um conjunto de ferramentas de desenvolvimento da Web, chamado de Microsoft Edge DevTools, incorporado ao Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8f65c-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="8f65c-127">Configurar seu código</span><span class="sxs-lookup"><span data-stu-id="8f65c-127">Set up your code</span></span>   

<span data-ttu-id="8f65c-128">Você vai criar seu site em um editor de código online chamado falha.</span><span class="sxs-lookup"><span data-stu-id="8f65c-128">You're going to build your site in an online code editor called Glitch.</span></span>  

1.  <span data-ttu-id="8f65c-129">Abra o [código-fonte][GlitchAlluringShockIndex].</span><span class="sxs-lookup"><span data-stu-id="8f65c-129">Open the [source code][GlitchAlluringShockIndex].</span></span>  <span data-ttu-id="8f65c-130">Esta guia será chamada de **guia Editor** ao longo deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="8f65c-130">This tab will be called the **editor tab** throughout this tutorial.</span></span>  
    > ##### <span data-ttu-id="8f65c-131">Figura 2</span><span class="sxs-lookup"><span data-stu-id="8f65c-131">Figure 2</span></span>  
    > <span data-ttu-id="8f65c-132">A guia Editor</span><span class="sxs-lookup"><span data-stu-id="8f65c-132">The editor tab</span></span>  
    > ![A guia Editor][ImageHtmlSetup1]  

1.  <span data-ttu-id="8f65c-134">Clique em **alluring-choque**.</span><span class="sxs-lookup"><span data-stu-id="8f65c-134">Click **alluring-shock**.</span></span>  <span data-ttu-id="8f65c-135">O menu opções do projeto é aberto no canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="8f65c-135">The Project Options menu opens in the top-left corner.</span></span>  
    
    > #### <span data-ttu-id="8f65c-136">Figura 3</span><span class="sxs-lookup"><span data-stu-id="8f65c-136">Figure 3</span></span>  
    > <span data-ttu-id="8f65c-137">O menu opções do Project</span><span class="sxs-lookup"><span data-stu-id="8f65c-137">The Project Options menu</span></span>  
    > ![O menu opções do Project][ImageHtmlSetup2]  
    
1.  <span data-ttu-id="8f65c-139">Clique em **remix projeto**.</span><span class="sxs-lookup"><span data-stu-id="8f65c-139">Click **Remix Project**.</span></span>  <span data-ttu-id="8f65c-140">Falha cria uma cópia do projeto que você pode editar e gera aleatoriamente um novo nome para o projeto.</span><span class="sxs-lookup"><span data-stu-id="8f65c-140">Glitch creates a copy of the project that you can edit and randomly generates a new name for the project.</span></span>  <span data-ttu-id="8f65c-141">O conteúdo é o mesmo que antes.</span><span class="sxs-lookup"><span data-stu-id="8f65c-141">The content is the same as before.</span></span>  
    
    > ##### <span data-ttu-id="8f65c-142">Figura 4</span><span class="sxs-lookup"><span data-stu-id="8f65c-142">Figure 4</span></span>  
    > <span data-ttu-id="8f65c-143">O projeto remisturado</span><span class="sxs-lookup"><span data-stu-id="8f65c-143">The remixed project</span></span>  
    > ![O projeto remisturado][ImageHtmlSetup3]  
    
1.  <span data-ttu-id="8f65c-145">Se você planeja concluir o próximo tutorial desta série, clique em **entrar** e entre em falha com sua conta do GitHub ou do Facebook.</span><span class="sxs-lookup"><span data-stu-id="8f65c-145">If you plan on completing the next tutorial in this series, click **Sign In** and sign in to Glitch with your GitHub or Facebook account.</span></span>  <span data-ttu-id="8f65c-146">Se você não se conectar, perderá a capacidade de editar esse projeto depois de fechar a guia Editar.</span><span class="sxs-lookup"><span data-stu-id="8f65c-146">If you don't sign in you will lose the ability to edit this project once you close the editing tab.</span></span>  
1.  <span data-ttu-id="8f65c-147">Clique em **Mostrar** e selecione **em uma nova janela**.</span><span class="sxs-lookup"><span data-stu-id="8f65c-147">Click **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="8f65c-148">Uma nova guia é aberta, mostrando a página ao vivo.</span><span class="sxs-lookup"><span data-stu-id="8f65c-148">A new tab opens, showing you the live page.</span></span>  <span data-ttu-id="8f65c-149">Esta guia será chamada de **guia ao vivo** durante este tutorial.</span><span class="sxs-lookup"><span data-stu-id="8f65c-149">This tab will be called the **live tab** throughout this tutorial.</span></span>  
    
    > ##### <span data-ttu-id="8f65c-150">Figura 5</span><span class="sxs-lookup"><span data-stu-id="8f65c-150">Figure 5</span></span>  
    > <span data-ttu-id="8f65c-151">A guia ao vivo</span><span class="sxs-lookup"><span data-stu-id="8f65c-151">The live tab</span></span>  
    > ![A guia ao vivo][ImageHtmlSetup4]  
    
## <span data-ttu-id="8f65c-153">Adicionar conteúdo</span><span class="sxs-lookup"><span data-stu-id="8f65c-153">Add content</span></span>   

<span data-ttu-id="8f65c-154">Seu site está muito vazio.</span><span class="sxs-lookup"><span data-stu-id="8f65c-154">Your site is pretty empty.</span></span>  <span data-ttu-id="8f65c-155">Siga as etapas abaixo para adicionar conteúdo a ele!</span><span class="sxs-lookup"><span data-stu-id="8f65c-155">Follow the steps below to add some content to it!</span></span>  

1.  <span data-ttu-id="8f65c-156">Na **guia Editor**, substituir `<!-- You're "About Me" will go here.  -->` por `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="8f65c-156">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
            </main>
            ...
        ...
    ...
    ```  
    
    > ##### <span data-ttu-id="8f65c-157">Figura 6</span><span class="sxs-lookup"><span data-stu-id="8f65c-157">Figure 6</span></span>  
    > <span data-ttu-id="8f65c-158">O novo código é realçado na guia Editor</span><span class="sxs-lookup"><span data-stu-id="8f65c-158">The new code is highlighted in the editor tab</span></span>  
    > ![O novo código é realçado na guia Editor][ImageHtmlAdd1]  
    
1.  <span data-ttu-id="8f65c-160">Exiba suas alterações na **guia ao vivo**.  O texto `About Me` está visível na página.</span><span class="sxs-lookup"><span data-stu-id="8f65c-160">View your changes in the **live tab**.  The text `About Me` is visible on the page.</span></span>  <span data-ttu-id="8f65c-161">É maior do que o restante do texto, porque o `<h1>` elemento representa um título de seção.</span><span class="sxs-lookup"><span data-stu-id="8f65c-161">It's larger than the rest of the text, because the `<h1>` element represents a section heading.</span></span>  <span data-ttu-id="8f65c-162">O navegador da Web automaticamente dimensiona títulos em tamanhos de fonte maiores.</span><span class="sxs-lookup"><span data-stu-id="8f65c-162">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    > ##### <span data-ttu-id="8f65c-163">Figura 7</span><span class="sxs-lookup"><span data-stu-id="8f65c-163">Figure 7</span></span>  
    > <span data-ttu-id="8f65c-164">O novo título fica visível na guia ao vivo</span><span class="sxs-lookup"><span data-stu-id="8f65c-164">The new heading is visible in the live tab</span></span>  
    > ![O novo título fica visível na guia ao vivo][ImageHtmlAdd2]  
    
1.  <span data-ttu-id="8f65c-166">De volta à **guia Editor**, insira `<p>I am learning HTML.  Recent accomplishments:</p>` na linha abaixo de onde você acabou de colocar `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="8f65c-166">Back in the **editor tab**, insert `<p>I am learning HTML.  Recent accomplishments:</p>` on the line below where you just put `<h1>About Me</h1>`.</span></span>  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
            </main>
            ...
        ...
    ...
    ```  

    > ##### <span data-ttu-id="8f65c-167">Figura 8</span><span class="sxs-lookup"><span data-stu-id="8f65c-167">Figure 8</span></span>  
    > <span data-ttu-id="8f65c-168">O novo código é realçado na guia Editor</span><span class="sxs-lookup"><span data-stu-id="8f65c-168">The new code is highlighted in the editor tab</span></span>  
    > ![O novo código é realçado na guia Editor][ImageHtmlAdd3]  
    
1.  <span data-ttu-id="8f65c-170">Exiba sua alteração na **guia ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="8f65c-170">View your change in the **live tab**.</span></span>  
1.  <span data-ttu-id="8f65c-171">De volta à **guia Editor**, adicione uma lista das suas conquistas:</span><span class="sxs-lookup"><span data-stu-id="8f65c-171">Back in the **editor tab**, add a list of your accomplishments:</span></span>  
    
    ```html
    ...
        ...
            ...
            <p>I am learning web development.  Recent accomplishments:</p>
            <ul>
                <li>Learned how to set up my code in Glitch.</li>
                <li>Added content to my HTML.</li>
                <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
                <li>TODO: Learn the difference between HTML and the DOM.</li>
            </ul>
            ...
        ...
    ...
    ```  
    
    > ##### <span data-ttu-id="8f65c-172">Figura 9</span><span class="sxs-lookup"><span data-stu-id="8f65c-172">Figure 9</span></span>  
    > <span data-ttu-id="8f65c-173">O novo código é realçado na guia Editor</span><span class="sxs-lookup"><span data-stu-id="8f65c-173">The new code is highlighted in the editor tab</span></span>  
    > ![O novo código é realçado na guia Editor][ImageHtmlAdd4]  
    
1.  <span data-ttu-id="8f65c-175">Novamente, volte para a **guia ao vivo** para garantir que o novo conteúdo seja exibido corretamente.</span><span class="sxs-lookup"><span data-stu-id="8f65c-175">Again, go back to the **live tab** to make sure that the new content is displaying correctly.</span></span>  
    
    > ##### <span data-ttu-id="8f65c-176">Figura 10</span><span class="sxs-lookup"><span data-stu-id="8f65c-176">Figure 10</span></span>  
    > <span data-ttu-id="8f65c-177">A nova lista fica visível na guia ao vivo</span><span class="sxs-lookup"><span data-stu-id="8f65c-177">The new list is visible in the live tab</span></span>  
    > ![A nova lista fica visível na guia ao vivo][ImageHtmlAdd5]  
    
## <span data-ttu-id="8f65c-179">Experimentar alterações de conteúdo no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8f65c-179">Experiment with content changes in Microsoft Edge DevTools</span></span>   

<span data-ttu-id="8f65c-180">Se você estivesse desenvolvendo uma página grande com grande parte do HTML, pode imaginar que pode ser um pouco cansativo para voltar e avançar entre a guia Editor e a guia ao vivo centenas de vezes para ver suas alterações, especialmente se você não tiver certeza sobre o que deve ser colocado na página.</span><span class="sxs-lookup"><span data-stu-id="8f65c-180">If you were developing a big page with a lot of HTML, you can imagine that it might be somewhat tedious to go back-and-forth between the editor tab and the live tab hundreds of times in order to see your changes, especially if you weren't sure what exactly to put on the page.</span></span>  <span data-ttu-id="8f65c-181">O Microsoft Edge DevTools pode ajudá-lo a experimentar alterações de conteúdo sem precisar sair da guia ao vivo.</span><span class="sxs-lookup"><span data-stu-id="8f65c-181">Microsoft Edge DevTools can help you experiment with content changes without ever leaving the live tab.</span></span>  

### <span data-ttu-id="8f65c-182">Saiba a diferença entre HTML e DOM</span><span class="sxs-lookup"><span data-stu-id="8f65c-182">Learn the difference between HTML and the DOM</span></span>   

<span data-ttu-id="8f65c-183">Antes de começar a editar seu conteúdo do Microsoft Edge DevTools, é útil compreender a diferença entre HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="8f65c-183">Before you start editing your content from Microsoft Edge DevTools, it's helpful to understand the difference between HTML and the DOM.</span></span>  <span data-ttu-id="8f65c-184">A melhor maneira de aprender é por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8f65c-184">The best way to learn is by example:</span></span>  

1.  <span data-ttu-id="8f65c-185">Ir para a **guia ao vivo**.  Na parte inferior da página, você vê o texto `A new element!?!` .</span><span class="sxs-lookup"><span data-stu-id="8f65c-185">Go to the **live tab**.  At the bottom of your page you see the text `A new element!?!`.</span></span>  
    
    > ###### <span data-ttu-id="8f65c-186">Figura 11</span><span class="sxs-lookup"><span data-stu-id="8f65c-186">Figure 11</span></span>  
    > <span data-ttu-id="8f65c-187">Na parte inferior da página, o texto `A new element!?!` pode ser visto</span><span class="sxs-lookup"><span data-stu-id="8f65c-187">At the bottom of the page the text `A new element!?!` can be seen</span></span>  
    > ![Na parte inferior da página, o novo elemento texto um novo!?!][ImageHtmlDom1]  
    
1.  <span data-ttu-id="8f65c-190">Volte para a **guia Editor** e tente localizar esse texto `index.html` .</span><span class="sxs-lookup"><span data-stu-id="8f65c-190">Go back to the **editor tab** and try to find this text in `index.html`.</span></span>  <span data-ttu-id="8f65c-191">Não está lá!</span><span class="sxs-lookup"><span data-stu-id="8f65c-191">It's not there!</span></span>  
    
    > ##### <span data-ttu-id="8f65c-192">Figura 12</span><span class="sxs-lookup"><span data-stu-id="8f65c-192">Figure 12</span></span>  
    > <span data-ttu-id="8f65c-193">O texto mistério `A new element!?!` não está disponível em qualquer lugar do</span><span class="sxs-lookup"><span data-stu-id="8f65c-193">The mystery text `A new element!?!` is nowhere to be found in</span></span> `index.html`  
    > ![O texto mistério um novo elemento!?!][ImageHtmlDom2]  
    
1.  <span data-ttu-id="8f65c-196">Volte para a **guia ao vivo**, clique com o botão direito do mouse `A new element!?!` e selecione **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="8f65c-196">Go back to the **live tab**, right-click `A new element!?!`, and select **Inspect**.</span></span>  
    
    > ##### <span data-ttu-id="8f65c-197">Figura 13</span><span class="sxs-lookup"><span data-stu-id="8f65c-197">Figure 13</span></span>  
    > <span data-ttu-id="8f65c-198">Inspecionar texto</span><span class="sxs-lookup"><span data-stu-id="8f65c-198">Inspecting some text</span></span>  
    > ![Inspecionar texto][ImageHtmlDom3]  
    
    <span data-ttu-id="8f65c-200">O DevTools é aberto juntamente com sua página.</span><span class="sxs-lookup"><span data-stu-id="8f65c-200">DevTools opens up alongside your page.</span></span>  `<div>A new element!?!</div>` <span data-ttu-id="8f65c-201">é realçado azul.</span><span class="sxs-lookup"><span data-stu-id="8f65c-201">is highlighted blue.</span></span>  <span data-ttu-id="8f65c-202">Embora essa estrutura em DevTools se pareça com o HTML, ela é na verdade a **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="8f65c-202">Although this structure in DevTools looks like your HTML, it is actually the **DOM Tree**.</span></span>  
    
    > ##### <span data-ttu-id="8f65c-203">Figura 14</span><span class="sxs-lookup"><span data-stu-id="8f65c-203">Figure 14</span></span>  
    > <span data-ttu-id="8f65c-204">O DevTools está aberto junto com a página</span><span class="sxs-lookup"><span data-stu-id="8f65c-204">DevTools is open alongside the page</span></span>  
    > ![O DevTools está aberto junto com a página][ImageHtmlDom4]  
    
<span data-ttu-id="8f65c-206">Quando a página é carregada, o navegador leva o HTML para criar o conteúdo *inicial* da página.</span><span class="sxs-lookup"><span data-stu-id="8f65c-206">When your page loads, the browser takes your HTML to create the *initial* content of the page.</span></span>  <span data-ttu-id="8f65c-207">O DOM representa o conteúdo *atual* da página, que pode mudar ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="8f65c-207">The DOM represents the *current* content of the page, which can change over time.</span></span>  <span data-ttu-id="8f65c-208">O `<div>A new element!?!</div>` conteúdo misterioso é adicionado à sua página devido à `<script src="new.js"></script>` marca na parte inferior da sua HTML.</span><span class="sxs-lookup"><span data-stu-id="8f65c-208">The mysterious `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span>  <span data-ttu-id="8f65c-209">Essa marca faz com que algum código JavaScript seja executado.</span><span class="sxs-lookup"><span data-stu-id="8f65c-209">This tag causes some JavaScript code to run.</span></span>  <span data-ttu-id="8f65c-210">Você aprenderá mais sobre JavaScript em um tutorial posterior, mas, por ora, pense nisso como uma linguagem de programação que pode alterar o conteúdo da sua página.</span><span class="sxs-lookup"><span data-stu-id="8f65c-210">You'll learn more about JavaScript in a later tutorial, but for now think of it as a programming language that can change the content of your page.</span></span>  <span data-ttu-id="8f65c-211">Nesse caso específico, o código JavaScript adiciona `<div>A new element!?!</div>` à sua página.</span><span class="sxs-lookup"><span data-stu-id="8f65c-211">In this particular case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span>  <span data-ttu-id="8f65c-212">É por isso que esse texto mistério fica visível na sua página ao vivo, mas não no HTML.</span><span class="sxs-lookup"><span data-stu-id="8f65c-212">That is why this mystery text is visible on your live page, but not in your HTML.</span></span>  

### <span data-ttu-id="8f65c-213">Editar o DOM</span><span class="sxs-lookup"><span data-stu-id="8f65c-213">Edit the DOM</span></span>   

<span data-ttu-id="8f65c-214">Se você quiser experimentar rapidamente as alterações de conteúdo sem precisar sair da guia ao vivo, tente DevTools.</span><span class="sxs-lookup"><span data-stu-id="8f65c-214">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="8f65c-215">No DevTools, clique com o botão direito do mouse `Your site!` e selecione **Editar como HTML**.</span><span class="sxs-lookup"><span data-stu-id="8f65c-215">In DevTools, right-click `Your site!` and select **Edit as HTML**.</span></span>  

    > ##### <span data-ttu-id="8f65c-216">Figura 15</span><span class="sxs-lookup"><span data-stu-id="8f65c-216">Figure 15</span></span>  
    > <span data-ttu-id="8f65c-217">Editando o nó como HTML</span><span class="sxs-lookup"><span data-stu-id="8f65c-217">Editing the node as HTML</span></span>  
    > ![Editando o nó como HTML][ImageHtmlEdit1]  
    
1.  <span data-ttu-id="8f65c-219">Substituir `<p>Your site!</p>` pelo código abaixo.</span><span class="sxs-lookup"><span data-stu-id="8f65c-219">Replace `<p>Your site!</p>` with the code below.</span></span>  
    
    ```html
    ...
        ...
            ...
            <header>
                <p><b>Welcome to my site!</b></p>
                <button>Download my resume</button>
            </header>
            ...
        ...
    ...
    ```  
    
    > ##### <span data-ttu-id="8f65c-220">Figura 16</span><span class="sxs-lookup"><span data-stu-id="8f65c-220">Figure 16</span></span>  
    > <span data-ttu-id="8f65c-221">Editando o nó como HTML</span><span class="sxs-lookup"><span data-stu-id="8f65c-221">Editing the node as HTML</span></span>  
    > ![Editando o nó como HTML][ImageHtmlEdit2]  
    
1.  <span data-ttu-id="8f65c-223">Pressione `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) para salvar suas alterações ou clique fora da caixa.</span><span class="sxs-lookup"><span data-stu-id="8f65c-223">Press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save your changes, or click outside of the box.</span></span>  <span data-ttu-id="8f65c-224">Suas alterações aparecem automaticamente na exibição ao vivo da página.</span><span class="sxs-lookup"><span data-stu-id="8f65c-224">Your changes automatically show up in the live view of your page.</span></span>  <span data-ttu-id="8f65c-225">O texto foi `Your site!` substituído pelo novo conteúdo.</span><span class="sxs-lookup"><span data-stu-id="8f65c-225">The text `Your site!` has been replaced with the new content.</span></span>  
    
    > ##### <span data-ttu-id="8f65c-226">Figura 17</span><span class="sxs-lookup"><span data-stu-id="8f65c-226">Figure 17</span></span>  
    > <span data-ttu-id="8f65c-227">O novo conteúdo aparece imediatamente na página</span><span class="sxs-lookup"><span data-stu-id="8f65c-227">The new content shows up immediately on the page</span></span>  
    > ![O novo conteúdo aparece imediatamente na página][ImageHtmlEdit3]  
    
<span data-ttu-id="8f65c-229">Esse fluxo de trabalho é bom para experimentar alterações de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="8f65c-229">This workflow is only good for experimenting with content changes.</span></span>  <span data-ttu-id="8f65c-230">Se você recarregar a página ou fechar a guia, suas alterações serão feitas para sempre.</span><span class="sxs-lookup"><span data-stu-id="8f65c-230">If you reload the page or close the tab, your changes will be gone forever.</span></span>  <span data-ttu-id="8f65c-231">Se você estiver usando este fluxo de trabalho e quiser salvar suas alterações, será necessário copiar manualmente essas alterações para o HTML.</span><span class="sxs-lookup"><span data-stu-id="8f65c-231">If you're using this workflow and you want to save your changes, you need to manually copy those changes over to your HTML.</span></span>  <span data-ttu-id="8f65c-232">As próximas seções mostram algumas outras maneiras de alterar o conteúdo da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="8f65c-232">The next couple of sections show you some more ways that you can change content from the DOM Tree.</span></span>  

## <span data-ttu-id="8f65c-233">Reordenar nós</span><span class="sxs-lookup"><span data-stu-id="8f65c-233">Reorder nodes</span></span>   

<span data-ttu-id="8f65c-234">Você também pode alterar a ordem dos nós DOM.</span><span class="sxs-lookup"><span data-stu-id="8f65c-234">You can also change the order of DOM nodes.</span></span>  <span data-ttu-id="8f65c-235">Por exemplo, em sua página da Web, o menu de navegação fica próximo à parte inferior.</span><span class="sxs-lookup"><span data-stu-id="8f65c-235">For example, on your web page the navigation menu is near the bottom.</span></span>  <span data-ttu-id="8f65c-236">Para movê-la para a parte superior:</span><span class="sxs-lookup"><span data-stu-id="8f65c-236">To move it to the top:</span></span>  

1.  <span data-ttu-id="8f65c-237">Localize o `<nav>` nó na **árvore DOM** do devtools.</span><span class="sxs-lookup"><span data-stu-id="8f65c-237">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    > ##### <span data-ttu-id="8f65c-238">Figura 18</span><span class="sxs-lookup"><span data-stu-id="8f65c-238">Figure 18</span></span>  
    > <span data-ttu-id="8f65c-239">O nó de navegação é em azul realçado no DevTools</span><span class="sxs-lookup"><span data-stu-id="8f65c-239">The nav node is highlighted blue in DevTools</span></span>  
    > ![O nó de navegação é em azul realçado no DevTools][ImageHtmlReorder1]  
    
1.  <span data-ttu-id="8f65c-241">Arraste o `<nav>` nó para a parte superior, para que seja o primeiro filho abaixo do `<body>` nó.</span><span class="sxs-lookup"><span data-stu-id="8f65c-241">Drag the `<nav>` node to the top, so that it's the first child below the `<body>` node.</span></span>  
    > ##### <span data-ttu-id="8f65c-242">Figura 19</span><span class="sxs-lookup"><span data-stu-id="8f65c-242">Figure 19</span></span>  
    > <span data-ttu-id="8f65c-243">Arrastando o nó de navegação para a parte superior</span><span class="sxs-lookup"><span data-stu-id="8f65c-243">Dragging the nav node to the top</span></span>  
    > ![Arrastando o nó de navegação para a parte superior][ImageHtmlReorder2]  
    
    <span data-ttu-id="8f65c-245">O `<nav>` nó agora está sendo exibido na parte superior da página.</span><span class="sxs-lookup"><span data-stu-id="8f65c-245">The `<nav>` node is now displaying at the top of your page.</span></span>  
    
    > ##### <span data-ttu-id="8f65c-246">Figura 20</span><span class="sxs-lookup"><span data-stu-id="8f65c-246">Figure 20</span></span>  
    > <span data-ttu-id="8f65c-247">O nó de navegação está na parte superior da página</span><span class="sxs-lookup"><span data-stu-id="8f65c-247">The nav node is at the top of the page</span></span>  
    > ![O nó de navegação está na parte superior da página][ImageHtmlReorder3]  
    
### <span data-ttu-id="8f65c-249">Excluir um nó</span><span class="sxs-lookup"><span data-stu-id="8f65c-249">Delete a node</span></span>   

<span data-ttu-id="8f65c-250">Você também pode remover nós da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="8f65c-250">You can also remove nodes from the DOM Tree.</span></span>  

1.  <span data-ttu-id="8f65c-251">Na **árvore DOM**, clique em `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="8f65c-251">In the **DOM Tree**, click `<div>A new element!?!</div>`.</span></span>  <span data-ttu-id="8f65c-252">DevTools realça o nó em azul.</span><span class="sxs-lookup"><span data-stu-id="8f65c-252">DevTools highlights the node blue.</span></span>  
    
    > ##### <span data-ttu-id="8f65c-253">Figura 21</span><span class="sxs-lookup"><span data-stu-id="8f65c-253">Figure 21</span></span>  
    > <span data-ttu-id="8f65c-254">Selecionando o nó a ser excluído</span><span class="sxs-lookup"><span data-stu-id="8f65c-254">Selecting the node to be deleted</span></span>  
    > ![Selecionando o nó a ser excluído][ImageHtmlDelete1]  
    
1.  <span data-ttu-id="8f65c-256">Pressione a `Delete` tecla no teclado.</span><span class="sxs-lookup"><span data-stu-id="8f65c-256">Press the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="8f65c-257">O `<div>A new element!?!</div>` nó é removido da sua árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="8f65c-257">The `<div>A new element!?!</div>` node is removed from your DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="8f65c-258">Figura 22</span><span class="sxs-lookup"><span data-stu-id="8f65c-258">Figure 22</span></span>  
    > <span data-ttu-id="8f65c-259">O nó foi excluído</span><span class="sxs-lookup"><span data-stu-id="8f65c-259">The node has been deleted</span></span>  
    > ![O nó foi excluído][ImageHtmlDelete2]  
    
## <span data-ttu-id="8f65c-261">Copiar as alterações</span><span class="sxs-lookup"><span data-stu-id="8f65c-261">Copy your changes</span></span>   

<span data-ttu-id="8f65c-262">Você está quase pronto.</span><span class="sxs-lookup"><span data-stu-id="8f65c-262">You're almost done.</span></span>  <span data-ttu-id="8f65c-263">Você fez algumas alterações na sua página no DevTools, mas elas ainda não foram salvas em seu código-fonte.</span><span class="sxs-lookup"><span data-stu-id="8f65c-263">You've made a few changes to your page in DevTools, but they're not yet saved to your source code.</span></span>  

1.  <span data-ttu-id="8f65c-264">Atualize a **guia ao vivo**.  As alterações feitas na árvore DOM desaparecem.</span><span class="sxs-lookup"><span data-stu-id="8f65c-264">Refresh your **live tab**.  The changes that you made in the DOM Tree disappear.</span></span>  <span data-ttu-id="8f65c-265">Em particular, o texto `Your site!` retorna à parte superior da página, e o texto `A new element!?!` retorna para a parte inferior.</span><span class="sxs-lookup"><span data-stu-id="8f65c-265">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    > ##### <span data-ttu-id="8f65c-266">Figura 23</span><span class="sxs-lookup"><span data-stu-id="8f65c-266">Figure 23</span></span>  
    > <span data-ttu-id="8f65c-267">As alterações feitas desapareceram</span><span class="sxs-lookup"><span data-stu-id="8f65c-267">The changes that you've made are gone</span></span>  
    > ![As alterações feitas desapareceram][ImageHtmlCopy1]  

1.  <span data-ttu-id="8f65c-269">Copie o código abaixo.</span><span class="sxs-lookup"><span data-stu-id="8f65c-269">Copy the code below.</span></span>  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1">
        </head>
        <body>
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav>
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/contact.html">Contact</a></li>
                </ul>
            </nav>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
                <ul>
                    <li>Learned how to set up my code in Glitch.</li>
                    <li>Added content to my HTML.</li>
                    <li>Learned how to use Microsoft Edge DevTools to experiment with content changes.</li>
                    <li>Learned the difference between HTML and the DOM.</li>
                </ul>
            </main>
        </body>
    </html>
    ```  
      
1.  <span data-ttu-id="8f65c-270">Volte para a **guia Editor** e substitua o conteúdo do seu `index.html` arquivo pelo código que você acabou de copiar.</span><span class="sxs-lookup"><span data-stu-id="8f65c-270">Go back to the **editor tab** and replace the contents of your `index.html` file with the code that you just copied.</span></span>  
    
    > ##### <span data-ttu-id="8f65c-271">Figura 24</span><span class="sxs-lookup"><span data-stu-id="8f65c-271">Figure 24</span></span>  
    > <span data-ttu-id="8f65c-272">Qual `index.html` deve ser a aparência de seu arquivo</span><span class="sxs-lookup"><span data-stu-id="8f65c-272">How your `index.html` file should look</span></span>  
    > ![Como o arquivo index. html deve ser exibido][ImageHtmlCopy2]  
    
## <span data-ttu-id="8f65c-274">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="8f65c-274">Next steps</span></span>   

*   <span data-ttu-id="8f65c-275">Conclua o próximo tutorial desta série, comece a [usar o CSS][DevToolsBeginnersCss]para aprender a estilizar sua página e experimentar alterações de estilo no Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="8f65c-275">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="8f65c-276">Leia [introdução ao dom][MDNIntroductionDom] para saber mais sobre o dom.</span><span class="sxs-lookup"><span data-stu-id="8f65c-276">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="8f65c-277">Dê uma olhada em um curso como [introdução ao desenvolvimento na Web][CourseraIntroductionToWebDevelopment] para obter uma experiência de desenvolvimento da Web mais prática.</span><span class="sxs-lookup"><span data-stu-id="8f65c-277">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] to get more hands-on web development experience.</span></span>  

<!--- image links --->  

[ImageHtmlFinished]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-finished.msft.png "Figura 1: o site concluído"  
[ImageHtmlSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup1.msft.png "Figura 2: a guia Editor"  
[ImageHtmlSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup2.msft.png "Figura 3: o menu de opções do Project"  
[ImageHtmlSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup3.msft.png "Figura 4: o projeto misturado"  
[ImageHtmlSetup4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup4.msft.png "Figura 5: a guia ao vivo"  
[ImageHtmlAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add1.msft.png "Figura 6: o novo código está realçado na guia Editor"  
[ImageHtmlAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add2.msft.png "Figura 7: o novo título está visível na guia ao vivo"  
[ImageHtmlAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add3.msft.png "Figura 8: o novo código está realçado na guia Editor"  
[ImageHtmlAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add4.msft.png "Figura 9: o novo código está realçado na guia Editor"  
[ImageHtmlAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add5.msft.png "Figura 10: a nova lista é visível na guia ao vivo"  
[ImageHtmlDom1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom1.msft.png "Figura 11: na parte inferior da página o novo elemento texto um novo!?! pode ser vista"  
[ImageHtmlDom2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom2.msft.png "Figura 12: o texto mistério um novo elemento!?! está em qualquer lugar para ser localizado em index. html"  
[ImageHtmlDom3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom3.msft.png "Figura 13: inspecionar algum texto"  
[ImageHtmlDom4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom4.msft.png "Figura 14: o DevTools está aberto junto com a página"  
[ImageHtmlEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit1.msft.png "Figura 15: editando o nó como HTML"  
[ImageHtmlEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit2.msft.png "Figura 16: editando o nó como HTML"  
[ImageHtmlEdit3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit3.msft.png "Figura 17: o novo conteúdo aparece imediatamente na página"  
[ImageHtmlReorder1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder1.msft.png "Figura 18: o nó de navegação é em azul realçado no DevTools"  
[ImageHtmlReorder2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder2.msft.png "Figura 19: arrastando o nó de navegação até o início"  
[ImageHtmlReorder3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder3.msft.png "Figura 20: o nó de navegação está na parte superior da página"  
[ImageHtmlDelete1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete1.msft.png "Figura 21: selecionando o nó a ser excluído"  
[ImageHtmlDelete2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete2.msft.png "Figura 22: o nó foi excluído"  
[ImageHtmlCopy1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy1.msft.png "Figura 23: as alterações feitas desapareceram"  
[ImageHtmlCopy2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy2.msft.png "Figura 24: como será a aparência do arquivo index. html"  

<!--- links --->  

[DevToolsBeginnersCss]: /microsoft-edge/devtools-guide-chromium/beginners/css "DevTools para iniciantes: introdução ao CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Introdução ao desenvolvimento na Web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index. html-alluring-choque | Problema"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Introdução ao HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introdução ao DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="8f65c-308">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="8f65c-308">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8f65c-309">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/beginners/html) e é criada pela [Katherine Jackson][KatherineJackson] \ (redatora técnica, Chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="8f65c-309">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8f65c-311">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8f65c-311">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
