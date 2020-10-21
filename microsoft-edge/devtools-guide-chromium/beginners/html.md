---
description: Comece a usar HTML e o DOM
title: 'DevTools para iniciantes: introdução ao HTML e ao DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: f17b68845ef746fa2612cdf4d02cc7e1003baabb
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125297"
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

# <span data-ttu-id="b990f-104">DevTools para iniciantes: introdução ao HTML e ao DOM</span><span class="sxs-lookup"><span data-stu-id="b990f-104">DevTools for beginners: Get started with HTML and the DOM</span></span>  

<span data-ttu-id="b990f-105">Esta é a primeira em uma série de tutoriais que ensinam noções básicas sobre o desenvolvimento na Web.</span><span class="sxs-lookup"><span data-stu-id="b990f-105">This is the first in a series of tutorials that teach you the basics of web development.</span></span>  <span data-ttu-id="b990f-106">Você também aprenderá sobre um conjunto de ferramentas de desenvolvedor da Web, chamado Microsoft Edge DevTools, que podem aumentar sua produtividade.</span><span class="sxs-lookup"><span data-stu-id="b990f-106">You will also learn about a set of web developer tools called Microsoft Edge DevTools that can increase your productivity.</span></span>  

<span data-ttu-id="b990f-107">Neste tutorial específico, você aprenderá sobre HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="b990f-107">In this particular tutorial, you learn about HTML and the DOM.</span></span>  <span data-ttu-id="b990f-108">O HTML é uma das principais tecnologias de desenvolvimento na Web.</span><span class="sxs-lookup"><span data-stu-id="b990f-108">HTML is one of the core technologies of web development.</span></span>  <span data-ttu-id="b990f-109">É o idioma que controla a estrutura e o conteúdo das páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="b990f-109">It is the language that controls the structure and content of webpages.</span></span>  <span data-ttu-id="b990f-110">O DOM também está relacionado à estrutura e ao conteúdo de páginas da Web, mas você aprenderá mais sobre isso mais tarde.</span><span class="sxs-lookup"><span data-stu-id="b990f-110">The DOM is also related to the structure and content of webpages, but you'll learn more about that later.</span></span>  

## <span data-ttu-id="b990f-111">Goal</span><span class="sxs-lookup"><span data-stu-id="b990f-111">Goals</span></span>  

<span data-ttu-id="b990f-112">Você aprenderá a desenvolver na Web Criando seu próprio website.</span><span class="sxs-lookup"><span data-stu-id="b990f-112">You are going to learn web development by actually building your own website.</span></span>  <span data-ttu-id="b990f-113">Quando você concluir todos os tutoriais da série *devtools para iniciantes* , o seu site final será exibido na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="b990f-113">By the time you complete all of the tutorials in the *DevTools for Beginners* series, your finished site will look like in the following figure.</span></span>  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-finished.msft.png":::
   <span data-ttu-id="b990f-115">O site concluído</span><span class="sxs-lookup"><span data-stu-id="b990f-115">The finished site</span></span>  
:::image-end:::  

<span data-ttu-id="b990f-116">No final deste tutorial, você compreenderá:</span><span class="sxs-lookup"><span data-stu-id="b990f-116">By the end of this tutorial, you will understand:</span></span>  

*   <span data-ttu-id="b990f-117">Como o HTML e o DOM criam o conteúdo que você vê nas páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="b990f-117">How HTML and the DOM create the content that you see on webpages.</span></span>  
*   <span data-ttu-id="b990f-118">Como o Microsoft Edge DevTools pode ajudá-lo a experimentar alterações em HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="b990f-118">How Microsoft Edge DevTools can help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="b990f-119">A diferença entre HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="b990f-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="b990f-120">Você também terá um site real!</span><span class="sxs-lookup"><span data-stu-id="b990f-120">You'll also have a real website!</span></span>  <span data-ttu-id="b990f-121">Você pode usar este site para hospedar seu currículo ou blog.</span><span class="sxs-lookup"><span data-stu-id="b990f-121">You can use this site to host your resume or blog.</span></span>  

## <span data-ttu-id="b990f-122">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="b990f-122">Prerequisites</span></span>  

<span data-ttu-id="b990f-123">Antes de tentar este tutorial, complete os seguintes pré-requisitos:</span><span class="sxs-lookup"><span data-stu-id="b990f-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="b990f-124">Se você não estiver familiarizado com HTML, leia [introdução ao HTML][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="b990f-124">If you are unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="b990f-125">Baixar o navegador da Web [Microsoft Edge][MicrosoftEdgeInsider] .</span><span class="sxs-lookup"><span data-stu-id="b990f-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="b990f-126">Este tutorial usa um conjunto de ferramentas de desenvolvimento da Web, chamado de Microsoft Edge DevTools, incorporado ao Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b990f-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <span data-ttu-id="b990f-127">Configurar seu código</span><span class="sxs-lookup"><span data-stu-id="b990f-127">Set up your code</span></span>  

<span data-ttu-id="b990f-128">Você vai compilar seu site em um editor de código online chamado falha.</span><span class="sxs-lookup"><span data-stu-id="b990f-128">You are going to build your site in an online code editor called Glitch.</span></span>  

1.  <span data-ttu-id="b990f-129">Abra o [código-fonte][GlitchAlluringShockIndex].</span><span class="sxs-lookup"><span data-stu-id="b990f-129">Open the [source code][GlitchAlluringShockIndex].</span></span>  <span data-ttu-id="b990f-130">Esta guia será chamada de **guia Editor** ao longo deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="b990f-130">This tab will be called the **editor tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-setup1.msft.png":::
       <span data-ttu-id="b990f-132">A guia Editor</span><span class="sxs-lookup"><span data-stu-id="b990f-132">The editor tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b990f-133">Escolha **alluring-choque**.</span><span class="sxs-lookup"><span data-stu-id="b990f-133">Choose **alluring-shock**.</span></span>  <span data-ttu-id="b990f-134">O menu opções do projeto é aberto no canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="b990f-134">The Project Options menu opens in the top-left corner.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-setup2.msft.png":::
       <span data-ttu-id="b990f-136">O menu opções do Project</span><span class="sxs-lookup"><span data-stu-id="b990f-136">The Project Options menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b990f-137">Escolha **projeto remix**.</span><span class="sxs-lookup"><span data-stu-id="b990f-137">Choose **Remix Project**.</span></span>  <span data-ttu-id="b990f-138">Falha cria uma cópia do projeto que você pode editar e gera aleatoriamente um novo nome para o projeto.</span><span class="sxs-lookup"><span data-stu-id="b990f-138">Glitch creates a copy of the project that you can edit and randomly generates a new name for the project.</span></span>  <span data-ttu-id="b990f-139">O conteúdo é o mesmo que antes.</span><span class="sxs-lookup"><span data-stu-id="b990f-139">The content is the same as before.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-setup3.msft.png":::
       <span data-ttu-id="b990f-141">O projeto remisturado</span><span class="sxs-lookup"><span data-stu-id="b990f-141">The remixed project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b990f-142">Se você planeja concluir o próximo tutorial desta série, escolha **entrar** e entrar para entrar com uma falha com sua conta do GitHub ou do Facebook.</span><span class="sxs-lookup"><span data-stu-id="b990f-142">If you plan on completing the next tutorial in this series, choose **Sign In** and sign in to Glitch with your GitHub or Facebook account.</span></span>  <span data-ttu-id="b990f-143">Se você não se conectar, perderá a capacidade de editar esse projeto depois de fechar a guia Editar.</span><span class="sxs-lookup"><span data-stu-id="b990f-143">If you don't sign in you will lose the ability to edit this project once you close the editing tab.</span></span>  
1.  <span data-ttu-id="b990f-144">Escolha **Mostrar** e escolha **em uma nova janela**.</span><span class="sxs-lookup"><span data-stu-id="b990f-144">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="b990f-145">Uma nova guia é aberta, mostrando a página ao vivo.</span><span class="sxs-lookup"><span data-stu-id="b990f-145">A new tab opens, showing you the live page.</span></span>  <span data-ttu-id="b990f-146">Esta guia será chamada de **guia ao vivo** durante este tutorial.</span><span class="sxs-lookup"><span data-stu-id="b990f-146">This tab will be called the **live tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-setup4.msft.png":::
       <span data-ttu-id="b990f-148">A guia ao vivo</span><span class="sxs-lookup"><span data-stu-id="b990f-148">The live tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b990f-149">Adicionar conteúdo</span><span class="sxs-lookup"><span data-stu-id="b990f-149">Add content</span></span>  

<span data-ttu-id="b990f-150">Seu site está muito vazio.</span><span class="sxs-lookup"><span data-stu-id="b990f-150">Your site is pretty empty.</span></span>  <span data-ttu-id="b990f-151">Siga as etapas abaixo para adicionar conteúdo a ele!</span><span class="sxs-lookup"><span data-stu-id="b990f-151">Follow the steps below to add some content to it!</span></span>  

1.  <span data-ttu-id="b990f-152">Na **guia Editor**, substituir `<!-- You're "About Me" will go here.  -->` por `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="b990f-152">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-add1.msft.png":::
             <span data-ttu-id="b990f-154">O novo código é realçado na guia Editor</span><span class="sxs-lookup"><span data-stu-id="b990f-154">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="b990f-155">Exiba suas alterações na **guia ao vivo**.  O texto `About Me` está visível na página.</span><span class="sxs-lookup"><span data-stu-id="b990f-155">View your changes in the **live tab**.  The text `About Me` is visible on the page.</span></span>  <span data-ttu-id="b990f-156">É maior do que o restante do texto, porque o `<h1>` elemento representa um título de seção.</span><span class="sxs-lookup"><span data-stu-id="b990f-156">It's larger than the rest of the text, because the `<h1>` element represents a section heading.</span></span>  <span data-ttu-id="b990f-157">O navegador da Web automaticamente dimensiona títulos em tamanhos de fonte maiores.</span><span class="sxs-lookup"><span data-stu-id="b990f-157">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-add2.msft.png":::
       <span data-ttu-id="b990f-159">O novo título fica visível na guia ao vivo</span><span class="sxs-lookup"><span data-stu-id="b990f-159">The new heading is visible in the live tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b990f-160">De volta à **guia Editor**, insira `<p>I am learning HTML.  Recent accomplishments:</p>` na linha abaixo de onde você acabou de colocar `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="b990f-160">Back in the **editor tab**, insert `<p>I am learning HTML.  Recent accomplishments:</p>` on the line below where you just put `<h1>About Me</h1>`.</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-add3.msft.png":::
             <span data-ttu-id="b990f-162">O código atualizado é realçado na guia Editor</span><span class="sxs-lookup"><span data-stu-id="b990f-162">The updated code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="b990f-163">Exiba sua alteração na **guia ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="b990f-163">View your change in the **live tab**.</span></span>  
1.  <span data-ttu-id="b990f-164">De volta à **guia Editor**, adicione uma lista das suas conquistas:</span><span class="sxs-lookup"><span data-stu-id="b990f-164">Back in the **editor tab**, add a list of your accomplishments:</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-add4.msft.png":::
             <span data-ttu-id="b990f-166">O código atualizado também é realçado na guia Editor</span><span class="sxs-lookup"><span data-stu-id="b990f-166">The updated code is also highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="b990f-167">Novamente, volte para a **guia ao vivo** para garantir que o novo conteúdo seja exibido corretamente.</span><span class="sxs-lookup"><span data-stu-id="b990f-167">Again, go back to the **live tab** to make sure that the new content is displaying correctly.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-add5.msft.png":::
       <span data-ttu-id="b990f-169">A nova lista fica visível na guia ao vivo</span><span class="sxs-lookup"><span data-stu-id="b990f-169">The new list is visible in the live tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b990f-170">Experimentar alterações de conteúdo no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b990f-170">Experiment with content changes in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="b990f-171">Se você estivesse desenvolvendo uma página grande com grande parte do HTML, pode imaginar que pode ser um pouco cansativo para voltar e avançar entre a guia Editor e a guia ao vivo centenas de vezes para ver suas alterações, especialmente se você não tiver certeza sobre o que deve ser colocado na página.</span><span class="sxs-lookup"><span data-stu-id="b990f-171">If you were developing a big page with a lot of HTML, you can imagine that it might be somewhat tedious to go back-and-forth between the editor tab and the live tab hundreds of times in order to see your changes, especially if you weren't sure what exactly to put on the page.</span></span>  <span data-ttu-id="b990f-172">O Microsoft Edge DevTools pode ajudá-lo a experimentar alterações de conteúdo sem precisar sair da guia ao vivo.</span><span class="sxs-lookup"><span data-stu-id="b990f-172">Microsoft Edge DevTools can help you experiment with content changes without ever leaving the live tab.</span></span>  

### <span data-ttu-id="b990f-173">Saiba a diferença entre HTML e DOM</span><span class="sxs-lookup"><span data-stu-id="b990f-173">Learn the difference between HTML and the DOM</span></span>  

<span data-ttu-id="b990f-174">Antes de começar a editar seu conteúdo do Microsoft Edge DevTools, é útil compreender a diferença entre HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="b990f-174">Before you start editing your content from Microsoft Edge DevTools, it's helpful to understand the difference between HTML and the DOM.</span></span>  <span data-ttu-id="b990f-175">A melhor maneira de aprender é por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b990f-175">The best way to learn is by example:</span></span>  

1.  <span data-ttu-id="b990f-176">Ir para a **guia ao vivo**.  Na parte inferior da página, você vê o texto `A new element!?!` .</span><span class="sxs-lookup"><span data-stu-id="b990f-176">Go to the **live tab**.  At the bottom of your page you see the text `A new element!?!`.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-dom1.msft.png":::
       <span data-ttu-id="b990f-179">Na parte inferior da página, o novo elemento texto um novo!?!</span><span class="sxs-lookup"><span data-stu-id="b990f-179">At the bottom of the page the text A new element!?!</span></span> <span data-ttu-id="b990f-180">pode ser vista</span><span class="sxs-lookup"><span data-stu-id="b990f-180">can be seen</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b990f-181">Volte para a **guia Editor** e tente localizar esse texto `index.html` .</span><span class="sxs-lookup"><span data-stu-id="b990f-181">Go back to the **editor tab** and try to find this text in `index.html`.</span></span>  <span data-ttu-id="b990f-182">Não está lá!</span><span class="sxs-lookup"><span data-stu-id="b990f-182">It's not there!</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-dom2.msft.png":::
       <span data-ttu-id="b990f-185">O texto mistério `A new element!?!` não está disponível em qualquer lugar do</span><span class="sxs-lookup"><span data-stu-id="b990f-185">The mystery text `A new element!?!` is nowhere to be found in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="b990f-186">Volte para a **guia ao vivo**, clique com o botão direito do mouse `A new element!?!` e escolha **inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="b990f-186">Go back to the **live tab**, right-click `A new element!?!`, and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-dom3.msft.png":::
       <span data-ttu-id="b990f-188">Inspecionar texto</span><span class="sxs-lookup"><span data-stu-id="b990f-188">Inspecting some text</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="b990f-189">O DevTools é aberto juntamente com sua página.</span><span class="sxs-lookup"><span data-stu-id="b990f-189">DevTools opens up alongside your page.</span></span>  `<div>A new element!?!</div>` <span data-ttu-id="b990f-190">é realçado azul.</span><span class="sxs-lookup"><span data-stu-id="b990f-190">is highlighted blue.</span></span>  <span data-ttu-id="b990f-191">Embora essa estrutura em DevTools se pareça com o HTML, ela é na verdade a **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="b990f-191">Although this structure in DevTools looks like your HTML, it is actually the **DOM Tree**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-dom4.msft.png":::
       <span data-ttu-id="b990f-193">O DevTools está aberto junto com a página</span><span class="sxs-lookup"><span data-stu-id="b990f-193">DevTools is open alongside the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b990f-194">Quando a página é carregada, o navegador leva o HTML para criar o conteúdo *inicial* da página.</span><span class="sxs-lookup"><span data-stu-id="b990f-194">When your page loads, the browser takes your HTML to create the *initial* content of the page.</span></span>  <span data-ttu-id="b990f-195">O DOM representa o conteúdo *atual* da página, que pode mudar ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="b990f-195">The DOM represents the *current* content of the page, which can change over time.</span></span>  <span data-ttu-id="b990f-196">O `<div>A new element!?!</div>` conteúdo misterioso é adicionado à sua página devido à `<script src="new.js"></script>` marca na parte inferior da sua HTML.</span><span class="sxs-lookup"><span data-stu-id="b990f-196">The mysterious `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span>  <span data-ttu-id="b990f-197">Essa marca faz com que algum código JavaScript seja executado.</span><span class="sxs-lookup"><span data-stu-id="b990f-197">This tag causes some JavaScript code to run.</span></span>  <span data-ttu-id="b990f-198">Você aprenderá mais sobre JavaScript em um tutorial posterior, mas, por ora, pense nisso como uma linguagem de programação que pode alterar o conteúdo da sua página.</span><span class="sxs-lookup"><span data-stu-id="b990f-198">You'll learn more about JavaScript in a later tutorial, but for now think of it as a programming language that can change the content of your page.</span></span>  <span data-ttu-id="b990f-199">Nesse caso específico, o código JavaScript adiciona `<div>A new element!?!</div>` à sua página.</span><span class="sxs-lookup"><span data-stu-id="b990f-199">In this particular case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span>  <span data-ttu-id="b990f-200">É por isso que esse texto mistério fica visível na sua página ao vivo, mas não no HTML.</span><span class="sxs-lookup"><span data-stu-id="b990f-200">That is why this mystery text is visible on your live page, but not in your HTML.</span></span>  

### <span data-ttu-id="b990f-201">Editar o DOM</span><span class="sxs-lookup"><span data-stu-id="b990f-201">Edit the DOM</span></span>  

<span data-ttu-id="b990f-202">Se você quiser experimentar rapidamente as alterações de conteúdo sem precisar sair da guia ao vivo, tente DevTools.</span><span class="sxs-lookup"><span data-stu-id="b990f-202">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="b990f-203">No DevTools, clique com o botão direito do mouse `Your site!` e escolha **Editar como HTML**.</span><span class="sxs-lookup"><span data-stu-id="b990f-203">In DevTools, right-click `Your site!` and choose **Edit as HTML**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-edit1.msft.png":::
       <span data-ttu-id="b990f-205">Editando o nó como HTML</span><span class="sxs-lookup"><span data-stu-id="b990f-205">Editing the node as HTML</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b990f-206">Substituir `<p>Your site!</p>` pelo código abaixo.</span><span class="sxs-lookup"><span data-stu-id="b990f-206">Replace `<p>Your site!</p>` with the code below.</span></span>  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-edit2.msft.png":::
             <span data-ttu-id="b990f-208">Atualizando o nó como HTML</span><span class="sxs-lookup"><span data-stu-id="b990f-208">Updating the node as HTML</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="b990f-209">Selecione `Control` + `Enter` \ (Windows, Linux \) ou `Command` + `Enter` \ (MacOS \) para salvar suas alterações ou clique fora da caixa.</span><span class="sxs-lookup"><span data-stu-id="b990f-209">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save your changes, or click outside of the box.</span></span>  <span data-ttu-id="b990f-210">Suas alterações aparecem automaticamente na exibição ao vivo da página.</span><span class="sxs-lookup"><span data-stu-id="b990f-210">Your changes automatically show up in the live view of your page.</span></span>  <span data-ttu-id="b990f-211">O texto foi `Your site!` substituído pelo novo conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b990f-211">The text `Your site!` has been replaced with the new content.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-edit3.msft.png":::
       <span data-ttu-id="b990f-213">O novo conteúdo aparece imediatamente na página</span><span class="sxs-lookup"><span data-stu-id="b990f-213">The new content shows up immediately on the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b990f-214">Esse fluxo de trabalho é bom para experimentar alterações de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b990f-214">This workflow is only good for experimenting with content changes.</span></span>  <span data-ttu-id="b990f-215">Se você recarregar a página ou fechar a guia, suas alterações serão feitas para sempre.</span><span class="sxs-lookup"><span data-stu-id="b990f-215">If you reload the page or close the tab, your changes will be gone forever.</span></span>  <span data-ttu-id="b990f-216">Se você estiver usando este fluxo de trabalho e quiser salvar suas alterações, será necessário copiar manualmente essas alterações para o HTML.</span><span class="sxs-lookup"><span data-stu-id="b990f-216">If you're using this workflow and you want to save your changes, you need to manually copy those changes over to your HTML.</span></span>  <span data-ttu-id="b990f-217">As próximas seções mostram algumas outras maneiras de alterar o conteúdo da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="b990f-217">The next couple of sections show you some more ways that you can change content from the DOM Tree.</span></span>  

## <span data-ttu-id="b990f-218">Reordenar nós</span><span class="sxs-lookup"><span data-stu-id="b990f-218">Reorder nodes</span></span>  

<span data-ttu-id="b990f-219">Você também pode alterar a ordem dos nós DOM.</span><span class="sxs-lookup"><span data-stu-id="b990f-219">You can also change the order of DOM nodes.</span></span>  <span data-ttu-id="b990f-220">Por exemplo, em sua página da Web, o menu de navegação fica próximo à parte inferior.</span><span class="sxs-lookup"><span data-stu-id="b990f-220">For example, on your web page the navigation menu is near the bottom.</span></span>  <span data-ttu-id="b990f-221">Para movê-la para a parte superior:</span><span class="sxs-lookup"><span data-stu-id="b990f-221">To move it to the top:</span></span>  

1.  <span data-ttu-id="b990f-222">Localize o `<nav>` nó na **árvore DOM** do devtools.</span><span class="sxs-lookup"><span data-stu-id="b990f-222">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-reorder1.msft.png":::
       <span data-ttu-id="b990f-224">O nó de navegação é em azul realçado no DevTools</span><span class="sxs-lookup"><span data-stu-id="b990f-224">The nav node is highlighted blue in DevTools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b990f-225">Arraste o `<nav>` nó para a parte superior, para que seja o primeiro filho abaixo do `<body>` nó.</span><span class="sxs-lookup"><span data-stu-id="b990f-225">Drag the `<nav>` node to the top, so that it's the first child below the `<body>` node.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-reorder2.msft.png":::
             <span data-ttu-id="b990f-227">Arrastando o nó de navegação para a parte superior</span><span class="sxs-lookup"><span data-stu-id="b990f-227">Dragging the nav node to the top</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="b990f-228">O `<nav>` nó agora está sendo exibido na parte superior da página.</span><span class="sxs-lookup"><span data-stu-id="b990f-228">The `<nav>` node is now displaying at the top of your page.</span></span>  
          
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-reorder3.msft.png":::
             <span data-ttu-id="b990f-230">O nó de navegação está na parte superior da página</span><span class="sxs-lookup"><span data-stu-id="b990f-230">The nav node is at the top of the page</span></span>  
          :::image-end:::  
       :::column-end:::
   :::row-end:::  
    
### <span data-ttu-id="b990f-231">Excluir um nó</span><span class="sxs-lookup"><span data-stu-id="b990f-231">Delete a node</span></span>  

<span data-ttu-id="b990f-232">Você também pode remover nós da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="b990f-232">You can also remove nodes from the DOM Tree.</span></span>  

1.  <span data-ttu-id="b990f-233">Na **árvore DOM**, clique em `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="b990f-233">In the **DOM Tree**, click `<div>A new element!?!</div>`.</span></span>  <span data-ttu-id="b990f-234">DevTools realça o nó em azul.</span><span class="sxs-lookup"><span data-stu-id="b990f-234">DevTools highlights the node blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-delete1.msft.png":::
       <span data-ttu-id="b990f-236">Selecionando o nó a ser excluído</span><span class="sxs-lookup"><span data-stu-id="b990f-236">Selecting the node to be deleted</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b990f-237">Pressione a `Delete` tecla no teclado.</span><span class="sxs-lookup"><span data-stu-id="b990f-237">Press the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="b990f-238">O `<div>A new element!?!</div>` nó é removido da sua árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="b990f-238">The `<div>A new element!?!</div>` node is removed from your DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-delete2.msft.png":::
       <span data-ttu-id="b990f-240">O nó foi excluído</span><span class="sxs-lookup"><span data-stu-id="b990f-240">The node has been deleted</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b990f-241">Copiar as alterações</span><span class="sxs-lookup"><span data-stu-id="b990f-241">Copy your changes</span></span>  

<span data-ttu-id="b990f-242">Você está quase pronto.</span><span class="sxs-lookup"><span data-stu-id="b990f-242">You're almost done.</span></span>  <span data-ttu-id="b990f-243">Você fez algumas alterações na sua página no DevTools, mas elas ainda não foram salvas em seu código-fonte.</span><span class="sxs-lookup"><span data-stu-id="b990f-243">You've made a few changes to your page in DevTools, but they're not yet saved to your source code.</span></span>  

1.  <span data-ttu-id="b990f-244">Atualize a **guia ao vivo**.  As alterações feitas na árvore DOM desaparecem.</span><span class="sxs-lookup"><span data-stu-id="b990f-244">Refresh your **live tab**.  The changes that you made in the DOM Tree disappear.</span></span>  <span data-ttu-id="b990f-245">Em particular, o texto `Your site!` retorna à parte superior da página, e o texto `A new element!?!` retorna para a parte inferior.</span><span class="sxs-lookup"><span data-stu-id="b990f-245">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-copy1.msft.png":::
       <span data-ttu-id="b990f-247">As alterações feitas desapareceram</span><span class="sxs-lookup"><span data-stu-id="b990f-247">The changes that you've made are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b990f-248">Copie o código abaixo.</span><span class="sxs-lookup"><span data-stu-id="b990f-248">Copy the code below.</span></span>  
    
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
    
1.  <span data-ttu-id="b990f-249">Volte para a **guia Editor** e substitua o conteúdo do seu `index.html` arquivo pelo código que você acabou de copiar.</span><span class="sxs-lookup"><span data-stu-id="b990f-249">Go back to the **editor tab** and replace the contents of your `index.html` file with the code that you just copied.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-copy2.msft.png":::
       <span data-ttu-id="b990f-251">Qual `index.html` deve ser a aparência de seu arquivo</span><span class="sxs-lookup"><span data-stu-id="b990f-251">How your `index.html` file should look</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="b990f-252">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="b990f-252">Next steps</span></span>  

*   <span data-ttu-id="b990f-253">Conclua o próximo tutorial desta série, comece a [usar o CSS][DevToolsBeginnersCss]para aprender a estilizar sua página e experimentar alterações de estilo no Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="b990f-253">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="b990f-254">Leia [introdução ao dom][MDNIntroductionDom] para saber mais sobre o dom.</span><span class="sxs-lookup"><span data-stu-id="b990f-254">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="b990f-255">Dê uma olhada em um curso como [introdução ao desenvolvimento na Web][CourseraIntroductionToWebDevelopment] para obter uma experiência de desenvolvimento da Web mais prática.</span><span class="sxs-lookup"><span data-stu-id="b990f-255">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] to get more hands-on web development experience.</span></span>  

## <span data-ttu-id="b990f-256">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b990f-256">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools para iniciantes: introdução ao CSS | Documentos da Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Introdução ao desenvolvimento na Web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html-alluring-choques | Problema"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Introdução ao HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introdução ao DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="b990f-263">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="b990f-263">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b990f-264">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/beginners/html) e é criada pela [Katherine Jackson][KatherineJackson] \ (redatora técnica, Chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="b990f-264">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and is authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b990f-266">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b990f-266">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
