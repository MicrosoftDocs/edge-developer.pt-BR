---
description: Introdução html e o DOM
title: 'DevTools para iniciantes: Começar com HTML e o DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools
ms.openlocfilehash: d2893021f5e19ffb714215b27edadba08c8d6f71
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564564"
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
# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a><span data-ttu-id="92b7a-104">DevTools para iniciantes: Começar com HTML e o DOM</span><span class="sxs-lookup"><span data-stu-id="92b7a-104">DevTools for beginners: Get started with HTML and the DOM</span></span>  

<span data-ttu-id="92b7a-105">Este é o primeiro de uma série de tutoriais que lhe ensinarão as noções básicas de desenvolvimento da Web.</span><span class="sxs-lookup"><span data-stu-id="92b7a-105">This is the first in a series of tutorials that teach you the basics of web development.</span></span>  <span data-ttu-id="92b7a-106">Saiba mais sobre um conjunto de ferramentas de desenvolvedor da Web, chamada Microsoft Edge DevTools, que pode aumentar sua produtividade.</span><span class="sxs-lookup"><span data-stu-id="92b7a-106">Learn about a set of web developer tools, named Microsoft Edge DevTools, that may increase your productivity.</span></span>  

<span data-ttu-id="92b7a-107">Neste tutorial específico, você aprenderá sobre HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="92b7a-107">In this particular tutorial, you learn about HTML and the DOM.</span></span>  <span data-ttu-id="92b7a-108">HTML é uma das principais tecnologias de desenvolvimento da Web.</span><span class="sxs-lookup"><span data-stu-id="92b7a-108">HTML is one of the core technologies of web development.</span></span>  <span data-ttu-id="92b7a-109">É o idioma que controla a estrutura e o conteúdo das páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="92b7a-109">It is the language that controls the structure and content of webpages.</span></span>  <span data-ttu-id="92b7a-110">O DOM também está relacionado à estrutura e ao conteúdo das páginas da Web, saiba mais sobre isso mais tarde.</span><span class="sxs-lookup"><span data-stu-id="92b7a-110">The DOM is also related to the structure and content of webpages, learn more about that later.</span></span>  

## <a name="goals"></a><span data-ttu-id="92b7a-111">Metas</span><span class="sxs-lookup"><span data-stu-id="92b7a-111">Goals</span></span>  

<span data-ttu-id="92b7a-112">Você aprenderá o desenvolvimento da Web criando seu próprio site.</span><span class="sxs-lookup"><span data-stu-id="92b7a-112">You are going to learn web development by actually building your own website.</span></span>  <span data-ttu-id="92b7a-113">Quando você concluir todos os tutoriais na série **DevTools para Iniciantes,** o site concluído poderá ter a aparência da figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="92b7a-113">By the time you complete all of the tutorials in the **DevTools for Beginners** series, your finished site may look like the following figure.</span></span>  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-finished.msft.png":::
   <span data-ttu-id="92b7a-115">O site concluído</span><span class="sxs-lookup"><span data-stu-id="92b7a-115">The finished site</span></span>  
:::image-end:::  

<span data-ttu-id="92b7a-116">No final deste tutorial, você deve entender os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="92b7a-116">By the end of this tutorial, you should understand the following topics.</span></span>  

*   <span data-ttu-id="92b7a-117">Como o HTML e o DOM criam o conteúdo exibido em páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="92b7a-117">How HTML and the DOM create the content that are displayed on webpages.</span></span>  
*   <span data-ttu-id="92b7a-118">Como Microsoft Edge o DevTools pode ajudá-lo a experimentar alterações em HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="92b7a-118">How Microsoft Edge DevTools may help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="92b7a-119">A diferença entre HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="92b7a-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="92b7a-120">Você também tem um site real.</span><span class="sxs-lookup"><span data-stu-id="92b7a-120">You also have a real website.</span></span>  <span data-ttu-id="92b7a-121">Você pode usar o site para hospedar seu currículo ou blog.</span><span class="sxs-lookup"><span data-stu-id="92b7a-121">You may use the site to host your resume or blog.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="92b7a-122">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="92b7a-122">Prerequisites</span></span>  

<span data-ttu-id="92b7a-123">Antes de tentar este tutorial, conclua os seguintes pré-requisitos:</span><span class="sxs-lookup"><span data-stu-id="92b7a-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="92b7a-124">Se você não estiver familiarizado com HTML, leia [Getting Started with HTML][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="92b7a-124">If you are unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="92b7a-125">Baixe o [Microsoft Edge][MicrosoftEdgeInsider] da Web.</span><span class="sxs-lookup"><span data-stu-id="92b7a-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="92b7a-126">Este tutorial usa um conjunto de ferramentas de desenvolvimento da Web, chamada Microsoft Edge DevTools, que são Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="92b7a-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <a name="set-up-your-code"></a><span data-ttu-id="92b7a-127">Configurar seu código</span><span class="sxs-lookup"><span data-stu-id="92b7a-127">Set up your code</span></span>  

<span data-ttu-id="92b7a-128">Você vai criar seu site em um editor de código online chamado Glitch.</span><span class="sxs-lookup"><span data-stu-id="92b7a-128">You are going to build your site in an online code editor called Glitch.</span></span>  

1.  <span data-ttu-id="92b7a-129">Abra o [código-fonte][GlitchAlluringShockIndex].</span><span class="sxs-lookup"><span data-stu-id="92b7a-129">Open the [source code][GlitchAlluringShockIndex].</span></span>  <span data-ttu-id="92b7a-130">Essa guia é chamada de **guia editor ao** longo deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="92b7a-130">This tab is called the **editor tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="A guia editor" lightbox="../media/beginners-html-setup1.msft.png":::
       <span data-ttu-id="92b7a-132">A guia editor</span><span class="sxs-lookup"><span data-stu-id="92b7a-132">The editor tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92b7a-133">Escolha **alluring-shock**.</span><span class="sxs-lookup"><span data-stu-id="92b7a-133">Choose **alluring-shock**.</span></span>  <span data-ttu-id="92b7a-134">O Project menu Opções é aberto no canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="92b7a-134">The Project Options menu opens in the top-left corner.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="O menu Project opções" lightbox="../media/beginners-html-setup2.msft.png":::
       <span data-ttu-id="92b7a-136">O menu Project opções</span><span class="sxs-lookup"><span data-stu-id="92b7a-136">The Project Options menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92b7a-137">Escolha **Mesclar Project**.</span><span class="sxs-lookup"><span data-stu-id="92b7a-137">Choose **Remix Project**.</span></span>  <span data-ttu-id="92b7a-138">A falha cria uma cópia do projeto que você pode editar e gera aleatoriamente um novo nome para o projeto.</span><span class="sxs-lookup"><span data-stu-id="92b7a-138">Glitch creates a copy of the project that you may edit and randomly generates a new name for the project.</span></span>  <span data-ttu-id="92b7a-139">O conteúdo é o mesmo de antes.</span><span class="sxs-lookup"><span data-stu-id="92b7a-139">The content is the same as before.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="O projeto remixado" lightbox="../media/beginners-html-setup3.msft.png":::
       <span data-ttu-id="92b7a-141">O projeto remixado</span><span class="sxs-lookup"><span data-stu-id="92b7a-141">The remixed project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92b7a-142">Se você planeja concluir o próximo tutorial \*\*\*\* desta série, escolha Entrar e entrar em Glitch com sua GitHub ou conta do Facebook.</span><span class="sxs-lookup"><span data-stu-id="92b7a-142">If you plan on completing the next tutorial in this series, choose **Sign In** and sign into Glitch with your GitHub or Facebook account.</span></span>  <span data-ttu-id="92b7a-143">Se você optar por não entrar em sua conta, perderá a capacidade de editar o projeto depois de fechar a guia de edição.</span><span class="sxs-lookup"><span data-stu-id="92b7a-143">If you choose to not sign into your account, you lose the ability to edit the project after you close the editing tab.</span></span>  
1.  <span data-ttu-id="92b7a-144">Escolha **Mostrar** e escolher **Em uma nova janela**.</span><span class="sxs-lookup"><span data-stu-id="92b7a-144">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="92b7a-145">Uma nova guia é aberta, mostrando a página ao vivo.</span><span class="sxs-lookup"><span data-stu-id="92b7a-145">A new tab opens, showing you the live page.</span></span>  <span data-ttu-id="92b7a-146">Essa guia é chamada de **guia ao vivo ao** longo deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="92b7a-146">This tab is called the **live tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="A guia ao vivo" lightbox="../media/beginners-html-setup4.msft.png":::
       <span data-ttu-id="92b7a-148">A guia ao vivo</span><span class="sxs-lookup"><span data-stu-id="92b7a-148">The live tab</span></span>  
    :::image-end:::  
    
## <a name="add-content"></a><span data-ttu-id="92b7a-149">Adicionar conteúdo</span><span class="sxs-lookup"><span data-stu-id="92b7a-149">Add content</span></span>  

<span data-ttu-id="92b7a-150">Seu site está muito vazio.</span><span class="sxs-lookup"><span data-stu-id="92b7a-150">Your site is pretty empty.</span></span>  <span data-ttu-id="92b7a-151">Siga as etapas abaixo para adicionar algum conteúdo a ele.</span><span class="sxs-lookup"><span data-stu-id="92b7a-151">Follow the steps below to add some content to it.</span></span>  

1.  <span data-ttu-id="92b7a-152">Na guia **editor,** substitua `<!-- You're "About Me" will go here.  -->` por `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="92b7a-152">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="O novo código é realçado na guia editor" lightbox="../media/beginners-html-add1.msft.png":::
             <span data-ttu-id="92b7a-154">O novo código é realçado na guia editor</span><span class="sxs-lookup"><span data-stu-id="92b7a-154">The new code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="92b7a-155">Exibir suas alterações na **guia ao vivo**.  O texto `About Me` está visível na página.</span><span class="sxs-lookup"><span data-stu-id="92b7a-155">View your changes in the **live tab**.  The text `About Me` is visible on the page.</span></span>  <span data-ttu-id="92b7a-156">O texto maior do que o texto ao redor, porque `<h1>` o elemento representa um título de seção.</span><span class="sxs-lookup"><span data-stu-id="92b7a-156">The text larger than the surrounding text, because the `<h1>` element represents a section heading.</span></span>  <span data-ttu-id="92b7a-157">O navegador da Web automaticamente estilos de títulos em tamanhos de fonte maiores.</span><span class="sxs-lookup"><span data-stu-id="92b7a-157">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="O novo título está visível na guia ao vivo" lightbox="../media/beginners-html-add2.msft.png":::
       <span data-ttu-id="92b7a-159">O novo título está visível na guia ao vivo</span><span class="sxs-lookup"><span data-stu-id="92b7a-159">The new heading is visible in the live tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92b7a-160">De volta à **guia editor**, insira na linha abaixo onde você acabou de `<p>I am learning HTML.  Recent accomplishments:</p>` colocar `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="92b7a-160">Back in the **editor tab**, insert `<p>I am learning HTML.  Recent accomplishments:</p>` on the line below where you just put `<h1>About Me</h1>`.</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="O código atualizado é realçado na guia editor" lightbox="../media/beginners-html-add3.msft.png":::
             <span data-ttu-id="92b7a-162">O código atualizado é realçado na guia editor</span><span class="sxs-lookup"><span data-stu-id="92b7a-162">The updated code is highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="92b7a-163">Exibir sua alteração na **guia ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="92b7a-163">View your change in the **live tab**.</span></span>  
1.  <span data-ttu-id="92b7a-164">De volta à **guia editor**, adicione uma lista de suas conquistas:</span><span class="sxs-lookup"><span data-stu-id="92b7a-164">Back in the **editor tab**, add a list of your accomplishments:</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="O código atualizado também é realçado na guia editor" lightbox="../media/beginners-html-add4.msft.png":::
             <span data-ttu-id="92b7a-166">O código atualizado também é realçado na guia editor</span><span class="sxs-lookup"><span data-stu-id="92b7a-166">The updated code is also highlighted in the editor tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="92b7a-167">Novamente, volte para a **guia ao** vivo para garantir que o novo conteúdo seja exibido corretamente.</span><span class="sxs-lookup"><span data-stu-id="92b7a-167">Again, go back to the **live tab** to make sure that the new content is displaying correctly.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="A nova lista está visível na guia ao vivo" lightbox="../media/beginners-html-add5.msft.png":::
       <span data-ttu-id="92b7a-169">A nova lista está visível na guia ao vivo</span><span class="sxs-lookup"><span data-stu-id="92b7a-169">The new list is visible in the live tab</span></span>  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a><span data-ttu-id="92b7a-170">Experimente alterações de conteúdo no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="92b7a-170">Experiment with content changes in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="92b7a-171">Se você estava desenvolvendo uma página grande com muito HTML, é um pouco tedioso ir e voltar entre a guia editor e a guia ao vivo centenas de vezes para exibir suas alterações, especialmente se você não tiver certeza do que exatamente colocar na página.</span><span class="sxs-lookup"><span data-stu-id="92b7a-171">If you were developing a big page with a lot of HTML, it is somewhat tedious to go back-and-forth between the editor tab and the live tab hundreds of times in order to display your changes, especially if you are unsure what exactly to put on the page.</span></span>  <span data-ttu-id="92b7a-172">Microsoft Edge O DevTools ajuda você a experimentar alterações de conteúdo sem sair da **guia ao vivo.**</span><span class="sxs-lookup"><span data-stu-id="92b7a-172">Microsoft Edge DevTools helps you experiment with content changes without ever leaving the **live tab**.</span></span>  

### <a name="learn-the-difference-between-html-and-the-dom"></a><span data-ttu-id="92b7a-173">Saiba a diferença entre HTML e DOM</span><span class="sxs-lookup"><span data-stu-id="92b7a-173">Learn the difference between HTML and the DOM</span></span>  

<span data-ttu-id="92b7a-174">Antes de começar a editar seu conteúdo Microsoft Edge DevTools, você deve entender a diferença entre HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="92b7a-174">Before you start editing your content from Microsoft Edge DevTools, you should understand the difference between HTML and the DOM.</span></span>  <span data-ttu-id="92b7a-175">A melhor maneira de aprender é por exemplo:</span><span class="sxs-lookup"><span data-stu-id="92b7a-175">The best way to learn is by example:</span></span>  

1.  <span data-ttu-id="92b7a-176">Navegue até **a guia ao vivo**.  Na parte inferior da página, o `A new element!?!` texto é exibido.</span><span class="sxs-lookup"><span data-stu-id="92b7a-176">Navigate to the **live tab**.  At the bottom of your page, the text `A new element!?!` is displayed.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="Na parte inferior da página, o texto Um novo elemento!?! é exibido" lightbox="../media/beginners-html-dom1.msft.png":::
       <span data-ttu-id="92b7a-179">Na parte inferior da página, o `A new element!?!` texto é exibido</span><span class="sxs-lookup"><span data-stu-id="92b7a-179">At the bottom of the page the text `A new element!?!` is displayed</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92b7a-180">Volte para a **guia editor** e tente encontrar o texto em `index.html` .</span><span class="sxs-lookup"><span data-stu-id="92b7a-180">Go back to the **editor tab** and try to find the text in `index.html`.</span></span>  <span data-ttu-id="92b7a-181">O texto não está lá.</span><span class="sxs-lookup"><span data-stu-id="92b7a-181">The text is not there.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="O texto de mistério Um novo elemento!?! não está em nenhum lugar para ser encontrado index.html" lightbox="../media/beginners-html-dom2.msft.png":::
       <span data-ttu-id="92b7a-184">O texto de `A new element!?!` mistério não é encontrado em nenhum lugar</span><span class="sxs-lookup"><span data-stu-id="92b7a-184">The mystery text `A new element!?!` is nowhere to be found in</span></span> `index.html`  
    :::image-end:::  
    
1.  <span data-ttu-id="92b7a-185">Volte para a guia **ao**vivo, passe o mouse sobre , abra o menu contextual \(clique com o botão direito do `A new element!?!` mouse\) e escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="92b7a-185">Go back to the **live tab**, hover on `A new element!?!`, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="Inspecionando algum texto" lightbox="../media/beginners-html-dom3.msft.png":::
       <span data-ttu-id="92b7a-187">Inspecionando algum texto</span><span class="sxs-lookup"><span data-stu-id="92b7a-187">Inspecting some text</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="92b7a-188">O DevTools abre junto com sua página.</span><span class="sxs-lookup"><span data-stu-id="92b7a-188">DevTools opens up alongside your page.</span></span>  `<div>A new element!?!</div>` <span data-ttu-id="92b7a-189">é realçada em azul.</span><span class="sxs-lookup"><span data-stu-id="92b7a-189">is highlighted blue.</span></span>  <span data-ttu-id="92b7a-190">Embora essa estrutura no DevTools se pareça com seu HTML, na verdade é a **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="92b7a-190">Although this structure in DevTools looks like your HTML, it is actually the **DOM Tree**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="O DevTools está aberto juntamente com a página" lightbox="../media/beginners-html-dom4.msft.png":::
       <span data-ttu-id="92b7a-192">O DevTools está aberto juntamente com a página</span><span class="sxs-lookup"><span data-stu-id="92b7a-192">DevTools is open alongside the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="92b7a-193">Quando sua página é carregada, o navegador pega seu HTML para criar o *conteúdo inicial* da página.</span><span class="sxs-lookup"><span data-stu-id="92b7a-193">When your page loads, the browser takes your HTML to create the *initial* content of the page.</span></span>  <span data-ttu-id="92b7a-194">O DOM representa *o conteúdo* atual da página, que pode mudar ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="92b7a-194">The DOM represents the *current* content of the page, which may change over time.</span></span>  <span data-ttu-id="92b7a-195">O conteúdo `<div>A new element!?!</div>` misterioso é adicionado à sua página devido à marca na parte inferior do `<script src="new.js"></script>` HTML.</span><span class="sxs-lookup"><span data-stu-id="92b7a-195">The mysterious `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span>  <span data-ttu-id="92b7a-196">Essa marca faz com que algum código JavaScript seja executado.</span><span class="sxs-lookup"><span data-stu-id="92b7a-196">This tag causes some JavaScript code to run.</span></span>  <span data-ttu-id="92b7a-197">Saiba mais sobre JavaScript em um tutorial posterior, mas, por enquanto, pense nele como uma linguagem de programação que pode alterar o conteúdo da sua página.</span><span class="sxs-lookup"><span data-stu-id="92b7a-197">Learn more about JavaScript in a later tutorial, but for now think of it as a programming language that may change the content of your page.</span></span>  <span data-ttu-id="92b7a-198">Nesse caso específico, o código JavaScript adiciona `<div>A new element!?!</div>` à sua página.</span><span class="sxs-lookup"><span data-stu-id="92b7a-198">In this particular case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span>  <span data-ttu-id="92b7a-199">É por isso que esse texto de mistério é visível em sua página ao vivo, mas não em seu HTML.</span><span class="sxs-lookup"><span data-stu-id="92b7a-199">That is why this mystery text is visible on your live page, but not in your HTML.</span></span>  

### <a name="edit-the-dom"></a><span data-ttu-id="92b7a-200">Editar o DOM</span><span class="sxs-lookup"><span data-stu-id="92b7a-200">Edit the DOM</span></span>  

<span data-ttu-id="92b7a-201">Se você quiser experimentar rapidamente as alterações de conteúdo sem sair da guia ao vivo, experimente DevTools.</span><span class="sxs-lookup"><span data-stu-id="92b7a-201">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="92b7a-202">Em DevTools, passe o mouse sobre , abra o menu contextual \(clique com o botão direito do `Your site!` mouse\) e escolha Editar como **HTML**.</span><span class="sxs-lookup"><span data-stu-id="92b7a-202">In DevTools, hover on `Your site!`, open the contextual menu \(right-click\), and choose **Edit as HTML**.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="Editar o nó como HTML" lightbox="../media/beginners-html-edit1.msft.png":::
       <span data-ttu-id="92b7a-204">Editar o nó como HTML</span><span class="sxs-lookup"><span data-stu-id="92b7a-204">Editing the node as HTML</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92b7a-205">Substitua `<p>Your site!</p>` pelo código abaixo.</span><span class="sxs-lookup"><span data-stu-id="92b7a-205">Replace `<p>Your site!</p>` with the code below.</span></span>  
    
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
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="Atualizando o nó como HTML" lightbox="../media/beginners-html-edit2.msft.png":::
             <span data-ttu-id="92b7a-207">Atualizando o nó como HTML</span><span class="sxs-lookup"><span data-stu-id="92b7a-207">Updating the node as HTML</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="92b7a-208">Selecione `Control` + `Enter` \(Windows, Linux\) ou `Command` + `Enter` \(macOS\) para salvar suas alterações ou escolher fora da caixa.</span><span class="sxs-lookup"><span data-stu-id="92b7a-208">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save your changes, or choose outside of the box.</span></span>  <span data-ttu-id="92b7a-209">Suas alterações aparecem automaticamente na exibição ao vivo da página.</span><span class="sxs-lookup"><span data-stu-id="92b7a-209">Your changes automatically show up in the live view of your page.</span></span>  <span data-ttu-id="92b7a-210">O texto `Your site!` foi substituído pelo novo conteúdo.</span><span class="sxs-lookup"><span data-stu-id="92b7a-210">The text `Your site!` has been replaced with the new content.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="O novo conteúdo aparece imediatamente na página" lightbox="../media/beginners-html-edit3.msft.png":::
       <span data-ttu-id="92b7a-212">O novo conteúdo aparece imediatamente na página</span><span class="sxs-lookup"><span data-stu-id="92b7a-212">The new content shows up immediately on the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="92b7a-213">Esse fluxo de trabalho só é bom para experimentar alterações de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="92b7a-213">This workflow is only good for experimenting with content changes.</span></span>  <span data-ttu-id="92b7a-214">Se você atualizar a página ou fechar a guia, suas alterações se foram para sempre.</span><span class="sxs-lookup"><span data-stu-id="92b7a-214">If you refresh the page or close the tab, your changes are gone forever.</span></span>  <span data-ttu-id="92b7a-215">Se você estiver usando esse fluxo de trabalho e quiser salvar suas alterações, será necessário copiar manualmente essas alterações para seu HTML.</span><span class="sxs-lookup"><span data-stu-id="92b7a-215">If you're using this workflow and you want to save your changes, you need to manually copy those changes over to your HTML.</span></span>  <span data-ttu-id="92b7a-216">As próximas seções mostram mais algumas maneiras de alterar o conteúdo da Árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="92b7a-216">The next couple of sections show you some more ways that you may change content from the DOM Tree.</span></span>  

## <a name="reorder-nodes"></a><span data-ttu-id="92b7a-217">Nós de reordenar</span><span class="sxs-lookup"><span data-stu-id="92b7a-217">Reorder nodes</span></span>  

<span data-ttu-id="92b7a-218">Você também pode alterar a ordem dos nós DOM.</span><span class="sxs-lookup"><span data-stu-id="92b7a-218">You may also change the order of DOM nodes.</span></span>  <span data-ttu-id="92b7a-219">Por exemplo, em sua página da Web, o menu de navegação está próximo à parte inferior.</span><span class="sxs-lookup"><span data-stu-id="92b7a-219">For example, on your web page the navigation menu is near the bottom.</span></span>  <span data-ttu-id="92b7a-220">Para movê-lo para a parte superior:</span><span class="sxs-lookup"><span data-stu-id="92b7a-220">To move it to the top:</span></span>  

1.  <span data-ttu-id="92b7a-221">Encontre o `<nav>` nó na Árvore **DOM** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="92b7a-221">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="O nó de nav é realçado em azul no DevTools" lightbox="../media/beginners-html-reorder1.msft.png":::
       <span data-ttu-id="92b7a-223">O nó de nav é realçado em azul no DevTools</span><span class="sxs-lookup"><span data-stu-id="92b7a-223">The nav node is highlighted blue in DevTools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92b7a-224">Arraste o `<nav>` nó até a parte superior, para que o nó seja o primeiro filho do `<body>` nó.</span><span class="sxs-lookup"><span data-stu-id="92b7a-224">Drag the `<nav>` node to the top, so that the node is the first child of the `<body>` node.</span></span>  
    
    :::row:::
       :::column span="":::
          &nbsp;  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="92b7a-225">O `<nav>` nó agora está sendo exibido na parte superior da página.</span><span class="sxs-lookup"><span data-stu-id="92b7a-225">The `<nav>` node is now displaying at the top of your page.</span></span>  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="Arrastando o nó de nav para a parte superior" lightbox="../media/beginners-html-reorder2.msft.png":::
             <span data-ttu-id="92b7a-227">Arrastando o nó de nav para a parte superior</span><span class="sxs-lookup"><span data-stu-id="92b7a-227">Dragging the nav node to the top</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="O nó de nav está na parte superior da página" lightbox="../media/beginners-html-reorder3.msft.png":::
             <span data-ttu-id="92b7a-229">O nó de nav está na parte superior da página</span><span class="sxs-lookup"><span data-stu-id="92b7a-229">The nav node is at the top of the page</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
### <a name="delete-a-node"></a><span data-ttu-id="92b7a-230">Excluir um nó</span><span class="sxs-lookup"><span data-stu-id="92b7a-230">Delete a node</span></span>  

<span data-ttu-id="92b7a-231">Você também pode remover nós da Árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="92b7a-231">You may also remove nodes from the DOM Tree.</span></span>  

1.  <span data-ttu-id="92b7a-232">Na Árvore **DOM,** escolha `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="92b7a-232">In the **DOM Tree**, choose `<div>A new element!?!</div>`.</span></span>  <span data-ttu-id="92b7a-233">DevTools realça o nó azul.</span><span class="sxs-lookup"><span data-stu-id="92b7a-233">DevTools highlights the node blue.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="Escolha o nó a ser excluído" lightbox="../media/beginners-html-delete1.msft.png":::
       <span data-ttu-id="92b7a-235">Escolha o nó a ser excluído</span><span class="sxs-lookup"><span data-stu-id="92b7a-235">Choose the node to be deleted</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92b7a-236">Selecione a `Delete` tecla no teclado.</span><span class="sxs-lookup"><span data-stu-id="92b7a-236">Select the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="92b7a-237">O `<div>A new element!?!</div>` nó é removido da árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="92b7a-237">The `<div>A new element!?!</div>` node is removed from your DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="O nó foi excluído" lightbox="../media/beginners-html-delete2.msft.png":::
       <span data-ttu-id="92b7a-239">O nó foi excluído</span><span class="sxs-lookup"><span data-stu-id="92b7a-239">The node has been deleted</span></span>  
    :::image-end:::  
    
## <a name="copy-your-changes"></a><span data-ttu-id="92b7a-240">Copiar suas alterações</span><span class="sxs-lookup"><span data-stu-id="92b7a-240">Copy your changes</span></span>  

<span data-ttu-id="92b7a-241">Você está quase terminando.</span><span class="sxs-lookup"><span data-stu-id="92b7a-241">You're almost done.</span></span>  <span data-ttu-id="92b7a-242">Você fez algumas alterações em sua página no DevTools, mas elas ainda não foram salvas no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="92b7a-242">You've made a few changes to your page in DevTools, but they're not yet saved to your source code.</span></span>  

1.  <span data-ttu-id="92b7a-243">Atualize sua **guia ao vivo**.  As alterações feitas na Árvore DOM desaparecem.</span><span class="sxs-lookup"><span data-stu-id="92b7a-243">Refresh your **live tab**.  The changes that you made in the DOM Tree disappear.</span></span>  <span data-ttu-id="92b7a-244">Em particular, o texto `Your site!` retorna para a parte superior da página e o texto retorna para a parte `A new element!?!` inferior.</span><span class="sxs-lookup"><span data-stu-id="92b7a-244">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="As alterações que você fez foram embora" lightbox="../media/beginners-html-copy1.msft.png":::
       <span data-ttu-id="92b7a-246">As alterações que você fez foram embora</span><span class="sxs-lookup"><span data-stu-id="92b7a-246">The changes that you've made are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="92b7a-247">Copie o código abaixo.</span><span class="sxs-lookup"><span data-stu-id="92b7a-247">Copy the code below.</span></span>  
    
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
    
1.  <span data-ttu-id="92b7a-248">Volte para a **guia editor e** substitua o conteúdo do arquivo pelo código que você `index.html` copiou.</span><span class="sxs-lookup"><span data-stu-id="92b7a-248">Go back to the **editor tab** and replace the contents of your `index.html` file with the code that you just copied.</span></span>  
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="Como seu arquivo index.html deve ficar" lightbox="../media/beginners-html-copy2.msft.png":::
       <span data-ttu-id="92b7a-250">Como seu `index.html` arquivo deve ser</span><span class="sxs-lookup"><span data-stu-id="92b7a-250">How your `index.html` file should look</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="92b7a-251">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="92b7a-251">Next steps</span></span>  

*   <span data-ttu-id="92b7a-252">Conclua o próximo tutorial desta série, Introdução [css][DevToolsBeginnersCss], para saber como estilo sua página e experimentar alterações de estilo no Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="92b7a-252">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="92b7a-253">Leia [Introdução ao DOM][MDNIntroductionDom] para saber mais sobre o DOM.</span><span class="sxs-lookup"><span data-stu-id="92b7a-253">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="92b7a-254">Confira um curso como Introdução ao [Desenvolvimento da Web][CourseraIntroductionToWebDevelopment] para obter mais experiência de desenvolvimento da Web prática.</span><span class="sxs-lookup"><span data-stu-id="92b7a-254">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] to get more hands-on web development experience.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="92b7a-255">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="92b7a-255">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools para iniciantes: Introdução com css | Microsoft Docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Introdução ao desenvolvimento da Web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html - | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Iniciando com o html | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introdução ao dom | MDN"  

> [!NOTE]
> <span data-ttu-id="92b7a-262">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="92b7a-262">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="92b7a-263">A página original foi encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/beginners/html) e foi criada por [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="92b7a-263">The original page was found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and was authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="92b7a-265">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="92b7a-265">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
