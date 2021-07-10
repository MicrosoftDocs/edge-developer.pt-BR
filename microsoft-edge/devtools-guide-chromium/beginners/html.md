---
description: Introdução html e o DOM
title: 'DevTools para iniciantes: Começar com HTML e o DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/01/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, devtools para iniciantes, HTML devtools para iniciantes, DOM devtools para iniciantes, tutorial html devtools, tutorial dom devtools, tutorial de modelo de objeto de documento devtools
ms.openlocfilehash: a049ec500e22f89db3ab1e966b55d89c2ad682fe
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643452"
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
# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a><span data-ttu-id="0a876-104">DevTools para iniciantes: Começar com HTML e o DOM</span><span class="sxs-lookup"><span data-stu-id="0a876-104">DevTools for beginners: Get started with HTML and the DOM</span></span>  

<span data-ttu-id="0a876-105">Este é o primeiro de uma série de tutoriais que lhe ensinarão as noções básicas de desenvolvimento da Web.</span><span class="sxs-lookup"><span data-stu-id="0a876-105">This is the first in a series of tutorials that teach you the basics of web development.</span></span> <span data-ttu-id="0a876-106">Saiba mais sobre um conjunto de ferramentas de desenvolvedor da Web, chamada Microsoft Edge DevTools, que pode aumentar sua produtividade.</span><span class="sxs-lookup"><span data-stu-id="0a876-106">Learn about a set of web developer tools, named Microsoft Edge DevTools, that may increase your productivity.</span></span>  

<span data-ttu-id="0a876-107">Este tutorial descreve HTML e o [Modelo de Objeto de Documento](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="0a876-107">This tutorial describes HTML and the [Document Object Model](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) \(DOM\).</span></span> <span data-ttu-id="0a876-108">HTML é uma das principais tecnologias de desenvolvimento da Web.</span><span class="sxs-lookup"><span data-stu-id="0a876-108">HTML is one of the core technologies of web development.</span></span> <span data-ttu-id="0a876-109">É o idioma que controla a estrutura e o conteúdo das páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="0a876-109">It is the language that controls the structure and content of webpages.</span></span> <span data-ttu-id="0a876-110">O DOM também está relacionado à estrutura e ao conteúdo das páginas da Web, que saberemos mais sobre mais tarde.</span><span class="sxs-lookup"><span data-stu-id="0a876-110">The DOM is also related to the structure and content of webpages, which we learn more about later.</span></span>

## <a name="goals"></a><span data-ttu-id="0a876-111">Metas</span><span class="sxs-lookup"><span data-stu-id="0a876-111">Goals</span></span>  

<span data-ttu-id="0a876-112">Você aprenderá o desenvolvimento da Web criando um site.</span><span class="sxs-lookup"><span data-stu-id="0a876-112">You're going to learn web development by building a website.</span></span>  <span data-ttu-id="0a876-113">Quando você concluir todos os tutoriais na série **DevTools para Iniciantes,** o site concluído poderá ter a aparência da figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a876-113">By the time you complete all of the tutorials in the **DevTools for Beginners** series, your finished site may look like the following figure.</span></span>  

:::image type="complex" source="media/beginners-html-finished.msft.png" alt-text="O site concluído" lightbox="media/beginners-html-finished.msft.png":::
   <span data-ttu-id="0a876-115">O site concluído</span><span class="sxs-lookup"><span data-stu-id="0a876-115">The finished site</span></span>  
:::image-end:::  

<span data-ttu-id="0a876-116">No final deste tutorial, você deve entender os seguintes conceitos.</span><span class="sxs-lookup"><span data-stu-id="0a876-116">By the end of this tutorial, you should understand the following concepts.</span></span>  

*   <span data-ttu-id="0a876-117">Como o HTML e o DOM criam o conteúdo exibido em páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="0a876-117">How HTML and the DOM create the content displayed on webpages.</span></span>  
*   <span data-ttu-id="0a876-118">Como Microsoft Edge o DevTools pode ajudá-lo a experimentar alterações em HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="0a876-118">How Microsoft Edge DevTools may help you experiment with HTML and DOM changes.</span></span>  
*   <span data-ttu-id="0a876-119">A diferença entre HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="0a876-119">The difference between HTML and the DOM.</span></span>  

<span data-ttu-id="0a876-120">Você também terá um site de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0a876-120">You will also have a working website.</span></span> <span data-ttu-id="0a876-121">Você pode usar o site para hospedar seu currículo ou blog.</span><span class="sxs-lookup"><span data-stu-id="0a876-121">You may use the site to host your resume or blog.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="0a876-122">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="0a876-122">Prerequisites</span></span>  

<span data-ttu-id="0a876-123">Antes de tentar este tutorial, conclua os seguintes pré-requisitos:</span><span class="sxs-lookup"><span data-stu-id="0a876-123">Before attempting this tutorial, complete the following prerequisites:</span></span>  

*   <span data-ttu-id="0a876-124">Se você não estiver familiarizado com HTML, leia [Getting Started with HTML][MDNGettingStartedHtml].</span><span class="sxs-lookup"><span data-stu-id="0a876-124">If you are unfamiliar with HTML, read [Getting Started with HTML][MDNGettingStartedHtml].</span></span>  
*   <span data-ttu-id="0a876-125">Baixe o [Microsoft Edge][MicrosoftEdgeInsider] da Web.</span><span class="sxs-lookup"><span data-stu-id="0a876-125">Download the [Microsoft Edge][MicrosoftEdgeInsider] web browser.</span></span>  <span data-ttu-id="0a876-126">Este tutorial usa um conjunto de ferramentas de desenvolvimento da Web, chamada Microsoft Edge DevTools, que são Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0a876-126">This tutorial uses a set of web development tools, called the Microsoft Edge DevTools, that are built into Microsoft Edge.</span></span>  

## <a name="set-up-your-code"></a><span data-ttu-id="0a876-127">Configurar seu código</span><span class="sxs-lookup"><span data-stu-id="0a876-127">Set up your code</span></span>  

<span data-ttu-id="0a876-128">Você vai criar um site no editor de código do Glitch online.</span><span class="sxs-lookup"><span data-stu-id="0a876-128">You are going to build a site in the Glitch online code editor.</span></span>  

1.  <span data-ttu-id="0a876-129">Abra o [código-fonte][GlitchAlluringShockIndex].</span><span class="sxs-lookup"><span data-stu-id="0a876-129">Open the [source code][GlitchAlluringShockIndex].</span></span> <span data-ttu-id="0a876-130">Essa guia é chamada de **guia editor ao** longo deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="0a876-130">This tab is called the **editor tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="media/beginners-html-setup1.msft.png" alt-text="A guia editor" lightbox="media/beginners-html-setup1.msft.png":::
       <span data-ttu-id="0a876-132">A guia editor</span><span class="sxs-lookup"><span data-stu-id="0a876-132">The editor tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0a876-133">Escolha **alluring-shock**.</span><span class="sxs-lookup"><span data-stu-id="0a876-133">Choose **alluring-shock**.</span></span> <span data-ttu-id="0a876-134">O **Project menu Opções** é aberto.</span><span class="sxs-lookup"><span data-stu-id="0a876-134">The **Project Options** menu opens.</span></span>  
    
    :::image type="complex" source="media/beginners-html-setup2.msft.png" alt-text="O menu Project opções" lightbox="media/beginners-html-setup2.msft.png":::
       <span data-ttu-id="0a876-136">O menu Project opções</span><span class="sxs-lookup"><span data-stu-id="0a876-136">The Project Options menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0a876-137">Escolha **Mesclar Project**.</span><span class="sxs-lookup"><span data-stu-id="0a876-137">Choose **Remix Project**.</span></span> <span data-ttu-id="0a876-138">A falha cria uma cópia do projeto que você pode editar e gera aleatoriamente um novo nome para o projeto.</span><span class="sxs-lookup"><span data-stu-id="0a876-138">Glitch creates a copy of the project that you may edit and randomly generates a new name for the project.</span></span> <span data-ttu-id="0a876-139">O conteúdo é o mesmo de antes.</span><span class="sxs-lookup"><span data-stu-id="0a876-139">The content is the same as before.</span></span>  
    
    :::image type="complex" source="media/beginners-html-setup3.msft.png" alt-text="O projeto remixado" lightbox="media/beginners-html-setup3.msft.png":::
       <span data-ttu-id="0a876-141">O projeto remixado</span><span class="sxs-lookup"><span data-stu-id="0a876-141">The remixed project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0a876-142">Se você planeja concluir o próximo tutorial \*\*\*\* desta série, escolha Entrar em Falha usando sua conta do Facebook, GitHub ou google; ou envie um link mágico para você mesmo.</span><span class="sxs-lookup"><span data-stu-id="0a876-142">If you plan to complete the next tutorial in this series, choose **Sign In** to Glitch using your Facebook, GitHub, or Google account; or email yourself a magic link.</span></span> <span data-ttu-id="0a876-143">Se você optar por não entrar em uma conta, não poderá editar o projeto depois de fechar a guia editor.</span><span class="sxs-lookup"><span data-stu-id="0a876-143">If you choose not to sign in to an account, you cannot edit the project after closing the editor tab.</span></span>

1.  <span data-ttu-id="0a876-144">Escolha **Mostrar**  \>  **em uma nova janela**.</span><span class="sxs-lookup"><span data-stu-id="0a876-144">Choose **Show** \> **In a New Window**.</span></span>  <span data-ttu-id="0a876-145">Uma nova guia é aberta, mostrando a página ao vivo.</span><span class="sxs-lookup"><span data-stu-id="0a876-145">A new tab opens, showing the live page.</span></span> <span data-ttu-id="0a876-146">Essa guia é chamada de **guia ao vivo ao** longo deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="0a876-146">This tab is called the **live tab** throughout this tutorial.</span></span>  
    
    :::image type="complex" source="media/beginners-html-setup4.msft.png" alt-text="A guia ao vivo" lightbox="media/beginners-html-setup4.msft.png":::
       <span data-ttu-id="0a876-148">A guia ao vivo</span><span class="sxs-lookup"><span data-stu-id="0a876-148">The live tab</span></span>  
    :::image-end:::  
    
## <a name="add-content"></a><span data-ttu-id="0a876-149">Adicionar conteúdo</span><span class="sxs-lookup"><span data-stu-id="0a876-149">Add content</span></span>  

<span data-ttu-id="0a876-150">Seu site precisa de mais informações.</span><span class="sxs-lookup"><span data-stu-id="0a876-150">Your site needs more information.</span></span> <span data-ttu-id="0a876-151">Conclua as etapas a seguir para adicionar algum conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0a876-151">Complete the following steps to add some content.</span></span>  

1. <span data-ttu-id="0a876-152">Na guia **editor,** substitua `<!-- You're "About Me" will go here.  -->` por `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="0a876-152">In the **editor tab**, replace `<!-- You're "About Me" will go here.  -->` with `<h1>About Me</h1>`.</span></span>  
    
    ```html
        ...
        <body>
            <p> Your site!</p>
                <main>
                    <h1>About Me</h1>
                </main>
        ...
    ```  
    
    :::image type="complex" source="media/beginners-html-add1.msft.png" alt-text="O novo código é realçado na guia editor" lightbox="media/beginners-html-add1.msft.png":::
        <span data-ttu-id="0a876-154">O novo código é realçado na guia editor</span><span class="sxs-lookup"><span data-stu-id="0a876-154">The new code is highlighted in the editor tab</span></span>  
    :::image-end:::  
    
1. <span data-ttu-id="0a876-155">Exibir suas alterações na **guia ao vivo**. O texto `About Me` está visível na página.</span><span class="sxs-lookup"><span data-stu-id="0a876-155">View your changes in the **live tab**. The text `About Me` is visible on the page.</span></span> <span data-ttu-id="0a876-156">O texto é maior do que o texto ao redor porque `<h1>` o elemento representa um Título 1.</span><span class="sxs-lookup"><span data-stu-id="0a876-156">The text is larger than the surrounding text because the `<h1>` element represents a Heading 1.</span></span>  <span data-ttu-id="0a876-157">O navegador da Web automaticamente estilos de títulos em tamanhos de fonte maiores.</span><span class="sxs-lookup"><span data-stu-id="0a876-157">Your web browser automatically styles headings in larger font sizes.</span></span>  
    
    :::image type="complex" source="media/beginners-html-add2.msft.png" alt-text="O novo título está visível na guia ao vivo" lightbox="media/beginners-html-add2.msft.png":::
       <span data-ttu-id="0a876-159">O novo título está visível na guia ao vivo</span><span class="sxs-lookup"><span data-stu-id="0a876-159">The new heading is visible in the live tab</span></span>  
    :::image-end:::  
    
1. <span data-ttu-id="0a876-160">De volta à **guia editor**, insira na linha `<p>I am learning web development. Recent accomplishments:</p>` abaixo  `<h1>About Me</h1>` .</span><span class="sxs-lookup"><span data-stu-id="0a876-160">Back in the **editor tab**, insert `<p>I am learning web development. Recent accomplishments:</p>` on the line below  `<h1>About Me</h1>`.</span></span>  
    
    ```html
    ...
        <body>
            <p> Your site!</p>
                <main>
                    <h1>About Me</h1>
                    <p>I am learning web development. Recent accomplishments:</p>
                </main>
    ...
    ```  

    :::image type="complex" source="media/beginners-html-add3.msft.png" alt-text="O código atualizado é realçado na guia editor" lightbox="media/beginners-html-add3.msft.png":::
        <span data-ttu-id="0a876-162">O código atualizado é realçado na guia editor</span><span class="sxs-lookup"><span data-stu-id="0a876-162">The updated code is highlighted in the editor tab</span></span>  
    :::image-end:::  
    
1. <span data-ttu-id="0a876-163">Exibir sua alteração na **guia ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="0a876-163">View your change in the **live tab**.</span></span>

1. <span data-ttu-id="0a876-164">De volta à **guia editor**, adicione uma lista de suas conquistas usando o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a876-164">Back in the **editor tab**, add a list of your accomplishments using the following code.</span></span>
    
    ```html
    ...
    <p>I am learning web development.  Recent accomplishments:</p>
        <ul>
            <li>Learned how to set up my code in Glitch.</li>
            <li>Added content to my HTML.</li>
            <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
            <li>TODO: Learn the difference between HTML and the DOM.</li>
        </ul>
    ...
    ```  

    :::image type="complex" source="media/beginners-html-add4.msft.png" alt-text="O código atualizado também é realçado na guia editor" lightbox="media/beginners-html-add4.msft.png":::
        <span data-ttu-id="0a876-166">O código atualizado também é realçado na guia editor</span><span class="sxs-lookup"><span data-stu-id="0a876-166">The updated code is also highlighted in the editor tab</span></span>  
    :::image-end:::  

1. <span data-ttu-id="0a876-167">Exibir a **guia ao vivo** para garantir que o novo conteúdo seja exibido corretamente.</span><span class="sxs-lookup"><span data-stu-id="0a876-167">View the **live tab** to make sure that the new content displays correctly.</span></span>  
    
    :::image type="complex" source="media/beginners-html-add5.msft.png" alt-text="A nova lista está visível na guia ao vivo" lightbox="media/beginners-html-add5.msft.png":::
       <span data-ttu-id="0a876-169">A nova lista está visível na guia ao vivo</span><span class="sxs-lookup"><span data-stu-id="0a876-169">The new list is visible in the live tab</span></span>  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a><span data-ttu-id="0a876-170">Experimente alterações de conteúdo no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0a876-170">Experiment with content changes in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="0a876-171">Se você estiver desenvolvendo uma página com muito HTML, torna-se tedioso ir e voltar entre a guia editor e a guia ao vivo para ver suas alterações.</span><span class="sxs-lookup"><span data-stu-id="0a876-171">If you are developing a page with a lot of HTML, it becomes tedious to go back-and-forth between the editor tab and the live tab to see your changes.</span></span> <span data-ttu-id="0a876-172">Microsoft Edge O DevTools ajuda você a experimentar alterações de conteúdo sem sair da **guia ao vivo.**</span><span class="sxs-lookup"><span data-stu-id="0a876-172">Microsoft Edge DevTools helps you experiment with content changes without ever leaving the **live tab**.</span></span>  

### <a name="learn-the-difference-between-html-and-the-dom"></a><span data-ttu-id="0a876-173">Saiba a diferença entre HTML e DOM</span><span class="sxs-lookup"><span data-stu-id="0a876-173">Learn the difference between HTML and the DOM</span></span>  

<span data-ttu-id="0a876-174">Antes de editar o conteúdo Microsoft Edge DevTools, vamos entender a diferença entre HTML e DOM.</span><span class="sxs-lookup"><span data-stu-id="0a876-174">Before editing content from Microsoft Edge DevTools, let's understand the difference between HTML and the DOM.</span></span> <span data-ttu-id="0a876-175">Prossiga com as etapas a seguir para aprender com um exemplo.</span><span class="sxs-lookup"><span data-stu-id="0a876-175">Proceed with the following steps to learn from an example.</span></span>

1. <span data-ttu-id="0a876-176">Navegue até **a guia ao vivo**. Na parte inferior da página, o `A new element!?!` texto é exibido.</span><span class="sxs-lookup"><span data-stu-id="0a876-176">Navigate to the **live tab**. At the bottom of your page, the text `A new element!?!` displays.</span></span>  

    <!--
        :::image type="complex" source="media/beginners-html-dom1.msft.png" alt-text="At the bottom of the page the text A new element!?! displays" lightbox="media/beginners-html-dom1.msft.png":::
        At the bottom of the page the text `A new element!?!` is displays  
        :::image-end:::
    -->
    
1. <span data-ttu-id="0a876-177">Abra a **guia editor** e tente encontrar o texto em `index.html` .</span><span class="sxs-lookup"><span data-stu-id="0a876-177">Open the **editor tab** and try to find the text in `index.html`.</span></span> <span data-ttu-id="0a876-178">O texto não é exibido neste exibição.</span><span class="sxs-lookup"><span data-stu-id="0a876-178">The text does not display in this view.</span></span>  

    <!--
        :::image type="complex" source="media/beginners-html-dom2.msft.png" alt-text="The mystery text A new element!?! is not found in index.html" lightbox="media/beginners-html-dom2.msft.png":::
        The mystery text `A new element!?!` is not found in `index.html`  
        :::image-end:::
    -->

1. <span data-ttu-id="0a876-179">Abra a **guia ao vivo**, passe o mouse sobre , abra o menu contextual (clique com o botão direito do mouse) e `A new element!?!` escolha **Inspecionar**.</span><span class="sxs-lookup"><span data-stu-id="0a876-179">Open the **live tab**, hover over `A new element!?!`, open the contextual menu (right-click) and then choose **Inspect**.</span></span>  
    
    :::image type="complex" source="media/beginners-html-dom3.msft.png" alt-text="Inspecionando algum texto" lightbox="media/beginners-html-dom3.msft.png":::
       <span data-ttu-id="0a876-181">Inspecionando algum texto</span><span class="sxs-lookup"><span data-stu-id="0a876-181">Inspecting some text</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="0a876-182">O DevTools abre junto com sua página.</span><span class="sxs-lookup"><span data-stu-id="0a876-182">DevTools opens up alongside your page.</span></span> `<div>A new element!?!</div>` <span data-ttu-id="0a876-183">é realçada.</span><span class="sxs-lookup"><span data-stu-id="0a876-183">is highlighted.</span></span> <span data-ttu-id="0a876-184">Embora essa estrutura no DevTools se pareça com HTML, é a **árvore DOM**.</span><span class="sxs-lookup"><span data-stu-id="0a876-184">Although this structure in DevTools looks like HTML, it is the **DOM Tree**.</span></span>  
    
    :::image type="complex" source="media/beginners-html-dom4.msft.png" alt-text="O DevTools está aberto juntamente com a página" lightbox="media/beginners-html-dom4.msft.png":::
       <span data-ttu-id="0a876-186">O DevTools está aberto juntamente com a página</span><span class="sxs-lookup"><span data-stu-id="0a876-186">DevTools is open alongside the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="0a876-187">Quando sua página é carregada, o navegador usa o HTML para criar o conteúdo inicial da página.</span><span class="sxs-lookup"><span data-stu-id="0a876-187">When your page loads, the browser uses the HTML to create the initial content of the page.</span></span> <span data-ttu-id="0a876-188">O DOM representa o conteúdo atual da página, que pode mudar ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="0a876-188">The DOM represents the current content of the page, which may change over time.</span></span> 

<span data-ttu-id="0a876-189">O `<div>A new element!?!</div>` conteúdo é adicionado à sua página devido à marca na parte inferior do `<script src="new.js"></script>` HTML.</span><span class="sxs-lookup"><span data-stu-id="0a876-189">The `<div>A new element!?!</div>` content is added to your page because of the `<script src="new.js"></script>` tag at the bottom of your HTML.</span></span> <span data-ttu-id="0a876-190">Essa marca faz com que algum código JavaScript seja executado.</span><span class="sxs-lookup"><span data-stu-id="0a876-190">This tag causes some JavaScript code to run.</span></span> <span data-ttu-id="0a876-191">Saiba mais sobre JavaScript em um [tutorial posterior.](../javascript/index.md)</span><span class="sxs-lookup"><span data-stu-id="0a876-191">Learn more about JavaScript in a [later tutorial](../javascript/index.md).</span></span>

<span data-ttu-id="0a876-192">Por enquanto, pense nele como uma linguagem de script que pode alterar o conteúdo da sua página.</span><span class="sxs-lookup"><span data-stu-id="0a876-192">For now, think of it as a scripting language that may change the content of your page.</span></span> <span data-ttu-id="0a876-193">Nesse caso, o código JavaScript adiciona `<div>A new element!?!</div>` à sua página.</span><span class="sxs-lookup"><span data-stu-id="0a876-193">In this case, JavaScript code adds `<div>A new element!?!</div>` to your page.</span></span> <span data-ttu-id="0a876-194">É por isso que esse texto é exibido na guia **ao** vivo, mas não no HTML.</span><span class="sxs-lookup"><span data-stu-id="0a876-194">That is why this text is displayed in the **live** tab, but not in the HTML.</span></span>  

### <a name="edit-the-dom"></a><span data-ttu-id="0a876-195">Editar o DOM</span><span class="sxs-lookup"><span data-stu-id="0a876-195">Edit the DOM</span></span>  

<span data-ttu-id="0a876-196">Se você quiser experimentar rapidamente as alterações de conteúdo sem sair da guia ao vivo, experimente DevTools.</span><span class="sxs-lookup"><span data-stu-id="0a876-196">If you want to quickly experiment with content changes without ever leaving the live tab, try DevTools.</span></span>  

1.  <span data-ttu-id="0a876-197">Em DevTools, passe o mouse sobre , abra o menu contextual (clique com o botão direito do mouse) e `Your site!` escolha Editar como **HTML**.</span><span class="sxs-lookup"><span data-stu-id="0a876-197">In DevTools, hover over `Your site!`, open the contextual menu (right-click) and choose **Edit as HTML**.</span></span>  
    
1.  <span data-ttu-id="0a876-198">Substitua `<p>Your site!</p>` pelo código a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a876-198">Replace `<p>Your site!</p>` with the following code.</span></span>  

```html
    ...
    <header>
        <p><b>Welcome to my site!</b></p>
        <button>Download my resume</button>
    </header>
    ...
```  

:::image type="complex" source="media/beginners-html-edit2.msft.png" alt-text="Atualizando o nó como HTML" lightbox="media/beginners-html-edit2.msft.png":::
    <span data-ttu-id="0a876-200">Atualizando o nó como HTML</span><span class="sxs-lookup"><span data-stu-id="0a876-200">Updating the node as HTML</span></span>  
<span data-ttu-id="0a876-201">::image-end:::</span><span class="sxs-lookup"><span data-stu-id="0a876-201">::image-end:::</span></span>  

1.  <span data-ttu-id="0a876-202">Selecione `Control` + `Enter` \(Windows, Linux\) `Command` + `Enter` ou \(macOS\) para salvar suas alterações ou selecione fora da caixa.</span><span class="sxs-lookup"><span data-stu-id="0a876-202">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save your changes, or select outside the box.</span></span> <span data-ttu-id="0a876-203">Suas alterações aparecem automaticamente na exibição ao vivo da página.</span><span class="sxs-lookup"><span data-stu-id="0a876-203">Your changes automatically show up in the live view of your page.</span></span> <span data-ttu-id="0a876-204">O texto `Your site!` foi substituído pelo novo conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0a876-204">The text `Your site!` has been replaced with the new content.</span></span>  
    
    :::image type="complex" source="media/beginners-html-edit3.msft.png" alt-text="O novo conteúdo aparece imediatamente na página" lightbox="media/beginners-html-edit3.msft.png":::
       <span data-ttu-id="0a876-206">O novo conteúdo aparece imediatamente na página</span><span class="sxs-lookup"><span data-stu-id="0a876-206">The new content shows up immediately on the page</span></span>  
    :::image-end:::  
    
<span data-ttu-id="0a876-207">Esse fluxo de trabalho só é adequado para experimentar alterações de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0a876-207">This workflow is only suitable for experimenting with content changes.</span></span> <span data-ttu-id="0a876-208">Se você atualizar a página ou fechar a guia, suas alterações serão perdidas.</span><span class="sxs-lookup"><span data-stu-id="0a876-208">If you refresh the page or close the tab, your changes are lost.</span></span> <span data-ttu-id="0a876-209">Se você quiser salvar suas alterações, copie manualmente o código para seu arquivo HTML.</span><span class="sxs-lookup"><span data-stu-id="0a876-209">If you want to save your changes, manually copy the code to your HTML file.</span></span> <span data-ttu-id="0a876-210">As próximas seções mostram mais algumas maneiras de alterar o conteúdo da Árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="0a876-210">The next couple of sections show you some more ways to change content from the DOM Tree.</span></span>  

## <a name="reorder-nodes"></a><span data-ttu-id="0a876-211">Nós de reordenar</span><span class="sxs-lookup"><span data-stu-id="0a876-211">Reorder nodes</span></span>

<span data-ttu-id="0a876-212">Você também pode alterar a ordem dos nós DOM.</span><span class="sxs-lookup"><span data-stu-id="0a876-212">You may also change the order of DOM nodes.</span></span> <span data-ttu-id="0a876-213">Por exemplo, em sua página da Web, o menu de navegação está próximo à parte inferior.</span><span class="sxs-lookup"><span data-stu-id="0a876-213">For example, on your web page the navigation menu is near the bottom.</span></span> <span data-ttu-id="0a876-214">Para movê-lo para a parte superior, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a876-214">To move it to the top, perform the following steps.</span></span>  

1.  <span data-ttu-id="0a876-215">Encontre o `<nav>` nó na Árvore **DOM** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="0a876-215">Find the `<nav>` node in the **DOM Tree** of DevTools.</span></span>  
    
    :::image type="complex" source="media/beginners-html-reorder1.msft.png" alt-text="O nó de nav é realçado no DevTools" lightbox="media/beginners-html-reorder1.msft.png":::
       <span data-ttu-id="0a876-217">O nó de nav é realçado no DevTools</span><span class="sxs-lookup"><span data-stu-id="0a876-217">The nav node is highlighted in DevTools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0a876-218">Arraste o `<nav>` nó até a parte superior, para que o nó seja o primeiro filho após o `<body>` nó.</span><span class="sxs-lookup"><span data-stu-id="0a876-218">Drag the `<nav>` node to the top, so that the node is the first child after the `<body>` node.</span></span>  
    
    :::image type="complex" source="media/beginners-html-reorder3.msft.png" alt-text="O nó de nav está na parte superior da página" lightbox="media/beginners-html-reorder3.msft.png":::
        <span data-ttu-id="0a876-220">O nó de nav está na parte superior da página</span><span class="sxs-lookup"><span data-stu-id="0a876-220">The nav node is at the top of the page</span></span>  
    :::image-end:::  
    
### <a name="delete-a-node"></a><span data-ttu-id="0a876-221">Excluir um nó</span><span class="sxs-lookup"><span data-stu-id="0a876-221">Delete a node</span></span>

<span data-ttu-id="0a876-222">Você também pode remover nós da Árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="0a876-222">You may also remove nodes from the DOM Tree.</span></span> <span data-ttu-id="0a876-223">Execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a876-223">Perform the following steps.</span></span>

1.  <span data-ttu-id="0a876-224">Na Árvore **DOM,** escolha `<div>A new element!?!</div>` .</span><span class="sxs-lookup"><span data-stu-id="0a876-224">In the **DOM Tree**, choose `<div>A new element!?!</div>`.</span></span> <span data-ttu-id="0a876-225">O DevTools realça o nó.</span><span class="sxs-lookup"><span data-stu-id="0a876-225">DevTools highlights the node.</span></span> 
    
1.  <span data-ttu-id="0a876-226">Selecione a `Delete` tecla no teclado.</span><span class="sxs-lookup"><span data-stu-id="0a876-226">Select the `Delete` key on your keyboard.</span></span>  <span data-ttu-id="0a876-227">O `<div>A new element!?!</div>` nó é removido da Árvore DOM.</span><span class="sxs-lookup"><span data-stu-id="0a876-227">The `<div>A new element!?!</div>` node is removed from the DOM Tree.</span></span>  
    
    :::image type="complex" source="media/beginners-html-delete2.msft.png" alt-text="O nó foi excluído" lightbox="media/beginners-html-delete2.msft.png":::
       <span data-ttu-id="0a876-229">O nó foi excluído</span><span class="sxs-lookup"><span data-stu-id="0a876-229">The node has been deleted</span></span>  
    :::image-end:::  
    
## <a name="copy-your-changes"></a><span data-ttu-id="0a876-230">Copiar suas alterações</span><span class="sxs-lookup"><span data-stu-id="0a876-230">Copy your changes</span></span>  

<span data-ttu-id="0a876-231">Você está quase terminando.</span><span class="sxs-lookup"><span data-stu-id="0a876-231">You're almost done.</span></span> <span data-ttu-id="0a876-232">Você fez algumas alterações na página no DevTools, mas elas não são salvas em seu código-fonte.</span><span class="sxs-lookup"><span data-stu-id="0a876-232">You made a few changes to the page in DevTools, but they're not saved to your source code.</span></span>  

1.  <span data-ttu-id="0a876-233">Atualize **a guia ao vivo**. As alterações feitas na Árvore DOM desaparecem.</span><span class="sxs-lookup"><span data-stu-id="0a876-233">Refresh the **live tab**. The changes that you made in the DOM Tree disappear.</span></span> <span data-ttu-id="0a876-234">Em particular, o texto `Your site!` retorna para a parte superior da página e o texto retorna para a parte `A new element!?!` inferior.</span><span class="sxs-lookup"><span data-stu-id="0a876-234">In particular, the text `Your site!` returns to the top of the page, and the text `A new element!?!` returns to the bottom.</span></span>  
    
    :::image type="complex" source="media/beginners-html-copy1.msft.png" alt-text="As alterações feitas foram embora" lightbox="media/beginners-html-copy1.msft.png":::
       <span data-ttu-id="0a876-236">As alterações feitas foram embora</span><span class="sxs-lookup"><span data-stu-id="0a876-236">The changes that you made are gone</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0a876-237">Copie o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a876-237">Copy the following code.</span></span>  
    
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
    
1.  <span data-ttu-id="0a876-238">Volte para a **guia editor e** substitua o conteúdo do arquivo pelo código que você `index.html` copiou.</span><span class="sxs-lookup"><span data-stu-id="0a876-238">Go back to the **editor tab** and replace the content of your `index.html` file with the code that you copied.</span></span>  
    
    :::image type="complex" source="media/beginners-html-copy2.msft.png" alt-text="Como seu arquivo index.html deve ficar" lightbox="media/beginners-html-copy2.msft.png":::
       <span data-ttu-id="0a876-240">Como seu `index.html` arquivo deve ser</span><span class="sxs-lookup"><span data-stu-id="0a876-240">How your `index.html` file should look</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="0a876-241">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="0a876-241">Next steps</span></span>  

*   <span data-ttu-id="0a876-242">Conclua o próximo tutorial desta série, Introdução [css][DevToolsBeginnersCss], para saber como estilo sua página e experimentar alterações de estilo no Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="0a876-242">Complete the next tutorial in this series, [Get Started with CSS][DevToolsBeginnersCss], to learn how to style your page and experiment with style changes in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="0a876-243">Leia [Introdução ao DOM][MDNIntroductionDom] para saber mais sobre o DOM.</span><span class="sxs-lookup"><span data-stu-id="0a876-243">Read [Introduction to the DOM][MDNIntroductionDom] to learn more about the DOM.</span></span>  
*   <span data-ttu-id="0a876-244">Confira um curso como Introdução ao [Desenvolvimento da Web][CourseraIntroductionToWebDevelopment] para obter mais experiência de desenvolvimento da Web prática.</span><span class="sxs-lookup"><span data-stu-id="0a876-244">Check out a course like [Introduction to Web Development][CourseraIntroductionToWebDevelopment] for more hands-on web development experience.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="0a876-245">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0a876-245">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools para iniciantes: Introdução com css | Microsoft Docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Introdução ao desenvolvimento da Web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html - | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Iniciando com o html | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introdução ao dom | MDN"  

> [!NOTE]
> <span data-ttu-id="0a876-252">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0a876-252">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0a876-253">A página original foi encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/beginners/html) e foi criada por [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="0a876-253">The original page was found [here](https://developers.google.com/web/tools/chrome-devtools/beginners/html) and was authored by [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0a876-255">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0a876-255">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
