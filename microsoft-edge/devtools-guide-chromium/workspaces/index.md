---
description: Saiba como salvar as alterações feitas no DevTools no disco.
title: Editar arquivos com espaços de trabalho
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 17f9ced15dbacd62c9ffe40e4af889925a8155fb
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399243"
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

# <a name="edit-files-with-workspaces"></a><span data-ttu-id="c7984-104">Editar arquivos com espaços de trabalho</span><span class="sxs-lookup"><span data-stu-id="c7984-104">Edit files with Workspaces</span></span>  

> [!NOTE]
> <span data-ttu-id="c7984-105">O objetivo deste tutorial é fornecer prática na configuração e no uso de Espaços de Trabalho, para que você possa usar Espaços de Trabalho em seus próprios projetos.</span><span class="sxs-lookup"><span data-stu-id="c7984-105">The goal of this tutorial is to provide hands-on practice in setting up and using Workspaces, so that you are able to use Workspaces in your own projects.</span></span>  <span data-ttu-id="c7984-106">Você é capaz de salvar as alterações no código-fonte, em seu computador local, que você fez no DevTools depois de habilitar Espaços de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="c7984-106">You are able to save the changes to the source code, on your local computer, that you made within DevTools after you enable Workspaces.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="c7984-107">**Pré-requisitos**: Antes de começar este tutorial, você deve saber como executar as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="c7984-107">**Prerequisites**: Before beginning this tutorial, you should know how to perform the following actions.</span></span>  
> 
> *   [<span data-ttu-id="c7984-108">Usar html, CSS e JavaScript para criar uma página da Web</span><span class="sxs-lookup"><span data-stu-id="c7984-108">Use html, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="c7984-109">Usar o DevTools para fazer alterações básicas no CSS</span><span class="sxs-lookup"><span data-stu-id="c7984-109">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="c7984-110">Executar um servidor Web HTTP local</span><span class="sxs-lookup"><span data-stu-id="c7984-110">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <a name="overview"></a><span data-ttu-id="c7984-111">Visão geral</span><span class="sxs-lookup"><span data-stu-id="c7984-111">Overview</span></span>  

<span data-ttu-id="c7984-112">Os espaços de trabalho permitem salvar uma alteração que você faz no Devtools em uma cópia local do mesmo arquivo em seu computador.</span><span class="sxs-lookup"><span data-stu-id="c7984-112">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="c7984-113">Para este tutorial, você deve ter as seguintes configurações em seu computador.</span><span class="sxs-lookup"><span data-stu-id="c7984-113">For this tutorial, you should have the following settings on your machine.</span></span>  

*   <span data-ttu-id="c7984-114">Você tem o código-fonte do seu site na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c7984-114">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="c7984-115">Você está executando um servidor Web local no diretório de código-fonte, para que o site seja acessível em `localhost:8080` .</span><span class="sxs-lookup"><span data-stu-id="c7984-115">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="c7984-116">Você abriu `localhost:8080` no Microsoft Edge e está usando o DevTools para alterar o CSS do site.</span><span class="sxs-lookup"><span data-stu-id="c7984-116">You opened `localhost:8080` in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="c7984-117">Com espaços de trabalho habilitados, as alterações CSS feitas no DevTools são salvas no código-fonte da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c7984-117">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <a name="limitations"></a><span data-ttu-id="c7984-118">Limitações</span><span class="sxs-lookup"><span data-stu-id="c7984-118">Limitations</span></span>  

<span data-ttu-id="c7984-119">Se você estiver usando uma estrutura moderna, provavelmente transformará seu código-fonte de um formato fácil de manter em um formato otimizado para ser executado o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="c7984-119">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  

<span data-ttu-id="c7984-120">Os espaços de trabalho geralmente são capazes de mapear o código otimizado de volta para o código-fonte original com a ajuda de mapas [de origem.][TreehouseBlogSourceMaps]</span><span class="sxs-lookup"><span data-stu-id="c7984-120">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="c7984-121">Mas há uma grande variação entre as estruturas sobre como cada um usa mapas de origem.</span><span class="sxs-lookup"><span data-stu-id="c7984-121">But there is a lot of variation between frameworks over how each uses source maps.</span></span>  <span data-ttu-id="c7984-122">Os Devtools simplesmente suportam todas as variações.</span><span class="sxs-lookup"><span data-stu-id="c7984-122">Devtools simply does support all of the variations.</span></span>  

<span data-ttu-id="c7984-123">Os espaços de trabalho são conhecidos por não funcionarem com a estrutura a seguir.</span><span class="sxs-lookup"><span data-stu-id="c7984-123">Workspaces is known to not work with the following framework.</span></span>  

*   <span data-ttu-id="c7984-124">Criar Aplicativo React</span><span class="sxs-lookup"><span data-stu-id="c7984-124">Create React App</span></span>  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <a name="related-feature-local-overrides"></a><span data-ttu-id="c7984-125">Recurso relacionado: substituições locais</span><span class="sxs-lookup"><span data-stu-id="c7984-125">Related feature: Local overrides</span></span>  

<span data-ttu-id="c7984-126">**Substituições Locais** é outro recurso DevTools semelhante a Workspaces.</span><span class="sxs-lookup"><span data-stu-id="c7984-126">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="c7984-127">Use Substituições Locais quando quiser experimentar alterações em uma página da Web e você precisa exibir as alterações em cargas de página da Web, mas não se importa em mapear suas alterações no código-fonte da página da Web.</span><span class="sxs-lookup"><span data-stu-id="c7984-127">Use Local Overrides when you want to experiment with changes to a webpage, and you need to display the changes across webpage loads, but you do not care about mapping your changes to the source code of the webpage.</span></span>  

<!--Todo: add section when content is ready  -->  

## <a name="step-1-set-up"></a><span data-ttu-id="c7984-128">Etapa 1: Configurar</span><span class="sxs-lookup"><span data-stu-id="c7984-128">Step 1: Set up</span></span>  

<span data-ttu-id="c7984-129">Conclua as seguintes ações, para obter experiência prática com Espaços de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="c7984-129">Complete the following actions, to get hands-on experience with Workspaces.</span></span>  

### <a name="set-up-the-demo"></a><span data-ttu-id="c7984-130">Configurar a demonstração</span><span class="sxs-lookup"><span data-stu-id="c7984-130">Set up the demo</span></span>  

1.  <span data-ttu-id="c7984-131">[Abra a demonstração][GlitchWorkspacesDemo].</span><span class="sxs-lookup"><span data-stu-id="c7984-131">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Um projeto Glitch" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       <span data-ttu-id="c7984-133">Um projeto Glitch</span><span class="sxs-lookup"><span data-stu-id="c7984-133">A Glitch project</span></span>  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Choose **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="c7984-134">Crie um `app` diretório em sua área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c7984-134">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="c7984-135">Salve cópias dos arquivos do `workspaces-demo` diretório para o `app` diretório.</span><span class="sxs-lookup"><span data-stu-id="c7984-135">Save copies of the files from the `workspaces-demo` directory to the `app` directory.</span></span>  <span data-ttu-id="c7984-136">Para o restante do tutorial, o diretório é chamado de `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="c7984-136">For the rest of the tutorial, the directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="c7984-137">Inicie um servidor Web local em `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="c7984-137">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="c7984-138">Abaixo está um código de exemplo para iniciar `SimpleHTTPServer` , mas você pode usar qualquer servidor que preferir.</span><span class="sxs-lookup"><span data-stu-id="c7984-138">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
    :::row:::
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m SimpleHTTPServer # Python 2
          ```  
       :::column-end:::  
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m http.server # Python 3
          ```  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="c7984-139">Abra uma guia no Microsoft Edge e navegue até a versão hospedada localmente do site.</span><span class="sxs-lookup"><span data-stu-id="c7984-139">Open a tab in Microsoft Edge and navigate to locally-hosted version of the site.</span></span>  <span data-ttu-id="c7984-140">Você deve ser capaz de acessá-lo usando uma URL como `localhost:8080` ou `http://0.0.0.0:8080` .</span><span class="sxs-lookup"><span data-stu-id="c7984-140">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="c7984-141">O número [exato da porta][WikiPortURLs] pode ser diferente.</span><span class="sxs-lookup"><span data-stu-id="c7984-141">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="A demonstração" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       <span data-ttu-id="c7984-143">A demonstração</span><span class="sxs-lookup"><span data-stu-id="c7984-143">The demo</span></span>  
    :::image-end:::  
    
### <a name="set-up-devtools"></a><span data-ttu-id="c7984-144">Configurar o DevTools</span><span class="sxs-lookup"><span data-stu-id="c7984-144">Set up DevTools</span></span>  

1.  <span data-ttu-id="c7984-145">Selecione `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\) para abrir o **painel console** do DevTools.</span><span class="sxs-lookup"><span data-stu-id="c7984-145">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="O painel Console" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       <span data-ttu-id="c7984-147">O **painel Console**</span><span class="sxs-lookup"><span data-stu-id="c7984-147">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c7984-148">Escolha a **ferramenta Fontes.**</span><span class="sxs-lookup"><span data-stu-id="c7984-148">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="c7984-149">Escolha o **painel Sistema de** Arquivos.</span><span class="sxs-lookup"><span data-stu-id="c7984-149">Choose the **Filesystem** panel.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="O painel Filesystem" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       <span data-ttu-id="c7984-151">O **painel Filesystem**</span><span class="sxs-lookup"><span data-stu-id="c7984-151">The **Filesystem** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c7984-152">Escolha **Adicionar pasta ao espaço de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="c7984-152">Choose **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="c7984-153">Digite `~/Desktop/app`.</span><span class="sxs-lookup"><span data-stu-id="c7984-153">Type `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="c7984-154">Escolha **Permitir** para dar permissão ao DevTools para ler e gravar no diretório.</span><span class="sxs-lookup"><span data-stu-id="c7984-154">Choose **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="c7984-155">No painel **Sistema de** Arquivos, agora há um ponto verde ao lado de , `index.html` e `script.js` `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="c7984-155">In the **Filesystem** panel, there is now a green dot next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="c7984-156">Esses pontos verdes significam que o DevTools estabeleceu um mapeamento entre os recursos de rede da página e os arquivos em `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="c7984-156">These green dots mean that DevTools has established a mapping between the network resources of the page, and the files in `~/Desktop/app`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="O painel Sistema de Arquivos agora mostra um mapeamento entre os arquivos locais e os de rede" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       <span data-ttu-id="c7984-158">O **painel Sistema de** Arquivos agora mostra um mapeamento entre os arquivos locais e os de rede</span><span class="sxs-lookup"><span data-stu-id="c7984-158">The **Filesystem** panel now shows a mapping between the local files and the network ones</span></span>  
    :::image-end:::  
    
## <a name="step-2-save-a-css-change-to-disk"></a><span data-ttu-id="c7984-159">Etapa 2: Salvar uma alteração CSS no disco</span><span class="sxs-lookup"><span data-stu-id="c7984-159">Step 2: Save a CSS change to disk</span></span>  

1.  <span data-ttu-id="c7984-160">Abra `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="c7984-160">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c7984-161">A `color` propriedade de elementos é definida como `h1` `fuchsia` .</span><span class="sxs-lookup"><span data-stu-id="c7984-161">The `color` property of `h1` elements is set to `fuchsia`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Exibir styles.css em um editor de texto" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       <span data-ttu-id="c7984-163">Exibir `styles.css` em um editor de texto</span><span class="sxs-lookup"><span data-stu-id="c7984-163">View `styles.css` in a text editor</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c7984-164">Escolha a **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="c7984-164">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="c7984-165">Altere o valor `color` da propriedade do elemento para sua cor `<h1>` favorita.</span><span class="sxs-lookup"><span data-stu-id="c7984-165">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="c7984-166">Lembre-se de que você precisa escolher o elemento na Árvore DOM para exibir as regras CSS aplicadas a `<h1>` ele no painel **Estilos.** </span><span class="sxs-lookup"><span data-stu-id="c7984-166">Remember that you need to choose the `<h1>` element in the **DOM Tree** in order to display the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="c7984-167">O ponto verde ao lado `styles.css:1` significa que qualquer alteração que você fizer será mapeada para `~/Desktop/app/styles.css` .</span><span class="sxs-lookup"><span data-stu-id="c7984-167">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="O indicador verde que o arquivo está vinculado" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       <span data-ttu-id="c7984-169">O indicador verde que o arquivo está vinculado</span><span class="sxs-lookup"><span data-stu-id="c7984-169">The green indicator that the file is linked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c7984-170">Abra `styles.css` em um editor de texto novamente.</span><span class="sxs-lookup"><span data-stu-id="c7984-170">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="c7984-171">A `color` propriedade agora está definida como sua cor favorita.</span><span class="sxs-lookup"><span data-stu-id="c7984-171">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="c7984-172">Atualize a página.</span><span class="sxs-lookup"><span data-stu-id="c7984-172">Refresh the page.</span></span>  <span data-ttu-id="c7984-173">A cor do `<h1>` elemento ainda está definida como sua cor favorita.</span><span class="sxs-lookup"><span data-stu-id="c7984-173">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="c7984-174">A alteração permanece em uma atualização, porque quando você fez a alteração DevTools salvou a alteração no disco.</span><span class="sxs-lookup"><span data-stu-id="c7984-174">The change remains across a refresh, because when you made the change DevTools saved the change to disk.</span></span>  <span data-ttu-id="c7984-175">E, quando você atualizeu a página, seu servidor local atendeu a cópia modificada do arquivo do disco.</span><span class="sxs-lookup"><span data-stu-id="c7984-175">And then, when you refreshed the page, your local server served the modified copy of the file from disk.</span></span>  
    
## <a name="step-3-save-an-html-change-to-disk"></a><span data-ttu-id="c7984-176">Etapa 3: Salvar uma alteração HTML no disco</span><span class="sxs-lookup"><span data-stu-id="c7984-176">Step 3: Save an HTML change to disk</span></span>  

### <a name="change-html-from-the-elements-panel"></a><span data-ttu-id="c7984-177">Alterar HTML do Painel de Elementos</span><span class="sxs-lookup"><span data-stu-id="c7984-177">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="c7984-178">Você pode fazer alterações no html do Painel de Elementos, mas suas alterações na árvore DOM não são salvas no disco e só efetivam a sessão atual do navegador.</span><span class="sxs-lookup"><span data-stu-id="c7984-178">You may make changes to the html from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  

<span data-ttu-id="c7984-179">A árvore DOM não é html.</span><span class="sxs-lookup"><span data-stu-id="c7984-179">The DOM tree is not html.</span></span>  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tool.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Attempt to change html from the DOM Tree of the Elements panel" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempt to change html from the DOM Tree of the **Elements** tool  
    :::image-end:::  
    
1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Refresh the page.  The page reverts to the original title.  
    
#### Optional: Why it is not working  

> [!NOTE]
> This section describes why the workflow from [Try changing html from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that are displayed on the **Elements** tool represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches html over the network, parses the html, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the webpage displayed for users may be very different from the html that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** tool should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->  

### <a name="change-html-from-the-sources-panel"></a><span data-ttu-id="c7984-180">Alterar HTML do painel Fontes</span><span class="sxs-lookup"><span data-stu-id="c7984-180">Change HTML from the Sources panel</span></span>  

<span data-ttu-id="c7984-181">Se você quiser salvar uma alteração no html da página, faça isso usando o **painel Fontes.**</span><span class="sxs-lookup"><span data-stu-id="c7984-181">If you want to save a change to the html of the page, do it using the **Sources** panel.</span></span>  

1.  <span data-ttu-id="c7984-182">Escolha a **ferramenta Fontes.**</span><span class="sxs-lookup"><span data-stu-id="c7984-182">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="c7984-183">Escolha o **painel** Página.</span><span class="sxs-lookup"><span data-stu-id="c7984-183">Choose the **Page** panel.</span></span>  
1.  <span data-ttu-id="c7984-184">Escolha **(índice)**.</span><span class="sxs-lookup"><span data-stu-id="c7984-184">Choose **(index)**.</span></span>  <span data-ttu-id="c7984-185">O HTML da página é aberto.</span><span class="sxs-lookup"><span data-stu-id="c7984-185">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="c7984-186">Substitua `<h1>Workspaces Demo</h1>` por `<h1>I ❤️  Cake</h1>` .</span><span class="sxs-lookup"><span data-stu-id="c7984-186">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="c7984-187">Revise a figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="c7984-187">Review the following figure.</span></span>  
1.  <span data-ttu-id="c7984-188">Selecione `Control` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\) para salvar a alteração.</span><span class="sxs-lookup"><span data-stu-id="c7984-188">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="c7984-189">Atualize a página.</span><span class="sxs-lookup"><span data-stu-id="c7984-189">Refresh the page.</span></span>  <span data-ttu-id="c7984-190">O `<h1>` elemento ainda está exibindo o novo texto.</span><span class="sxs-lookup"><span data-stu-id="c7984-190">The `<h1>` element is still displaying the new text.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Alterar HTML do painel Fontes" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       <span data-ttu-id="c7984-192">Alterar HTML do painel **Fontes**</span><span class="sxs-lookup"><span data-stu-id="c7984-192">Change HTML from the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c7984-193">Abra `~/Desktop/app/index.html` .</span><span class="sxs-lookup"><span data-stu-id="c7984-193">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="c7984-194">O `<h1>` elemento contém o novo texto.</span><span class="sxs-lookup"><span data-stu-id="c7984-194">The `<h1>` element contains the new text.</span></span>  
    
## <a name="step-4-save-a-javascript-change-to-disk"></a><span data-ttu-id="c7984-195">Etapa 4: Salvar uma alteração do JavaScript no disco</span><span class="sxs-lookup"><span data-stu-id="c7984-195">Step 4: Save a JavaScript change to disk</span></span>  

<span data-ttu-id="c7984-196">O **painel Fontes** também é o local para fazer alterações no JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c7984-196">The **Sources** panel is also the place to make changes to JavaScript.</span></span>  <span data-ttu-id="c7984-197">Mas, às vezes, você precisa acessar outros painéis, como a ferramenta **Elements** ou o **painel console,** enquanto faz alterações em seu site.</span><span class="sxs-lookup"><span data-stu-id="c7984-197">But sometimes you need to access other panels, such as the **Elements** tool or the **Console** panel, while making changes to your site.</span></span>  <span data-ttu-id="c7984-198">Há uma maneira de abrir o painel **Fontes** junto com outros painéis.</span><span class="sxs-lookup"><span data-stu-id="c7984-198">There is a way to have the **Sources** panel open alongside other panels.</span></span>  

1.  <span data-ttu-id="c7984-199">Escolha a **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="c7984-199">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="c7984-200">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="c7984-200">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="c7984-201">O **Menu de Comando** é aberto.</span><span class="sxs-lookup"><span data-stu-id="c7984-201">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="c7984-202">Digite `QS` , escolha Mostrar Fonte **Rápida**.</span><span class="sxs-lookup"><span data-stu-id="c7984-202">Type `QS`, then choose **Show Quick Source**.</span></span>  <span data-ttu-id="c7984-203">Na parte inferior da janela DevTools, agora há um **painel De origem** rápida.</span><span class="sxs-lookup"><span data-stu-id="c7984-203">At the bottom of your DevTools window there is now a **Quick Source** panel.</span></span>  <span data-ttu-id="c7984-204">O painel está exibindo o conteúdo de , que é o `index.html` último arquivo editado no painel **Fontes.**</span><span class="sxs-lookup"><span data-stu-id="c7984-204">The panel is displaying the contents of `index.html`, which is the last file you edited in the **Sources** panel.</span></span>  <span data-ttu-id="c7984-205">O **painel Fonte Rápida** fornece o editor do painel **Fontes,** para que você possa editar arquivos enquanto outros painéis são abertos.</span><span class="sxs-lookup"><span data-stu-id="c7984-205">The **Quick Source** panel gives you the editor from the **Sources** panel, so that you are able to edit files while having other panels open.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Abra o painel De origem rápida usando o Menu de Comando" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       <span data-ttu-id="c7984-207">Abra o **painel De origem** rápida usando **o Menu de Comando**</span><span class="sxs-lookup"><span data-stu-id="c7984-207">Open the **Quick Source** panel using **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c7984-208">Selecione `Control` + `P` \(Windows, Linux\) `Command` + `P` ou \(macOS\) para abrir a **caixa de diálogo Abrir Arquivo.**</span><span class="sxs-lookup"><span data-stu-id="c7984-208">Select `Control`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="c7984-209">Revise a figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="c7984-209">Review the following figure.</span></span>  
1.  <span data-ttu-id="c7984-210">Digite `script` , escolha **aplicativo/script.js**.</span><span class="sxs-lookup"><span data-stu-id="c7984-210">Type `script`, then choose **app/script.js**.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Abra script.js usando a caixa de diálogo Abrir Arquivo" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       <span data-ttu-id="c7984-212">Abrir `script.js` usando a caixa de diálogo Abrir **Arquivo**</span><span class="sxs-lookup"><span data-stu-id="c7984-212">Open `script.js` using the **Open File** dialog</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="c7984-213">O `Save Changes To Disk With Workspaces` link na demonstração é estilizado regularmente.</span><span class="sxs-lookup"><span data-stu-id="c7984-213">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="c7984-214">Adicione o código a seguir à parte inferior  da script.jsusando o **painel Fonte** Rápida.</span><span class="sxs-lookup"><span data-stu-id="c7984-214">Add the following code to the bottom of **script.js** using the **Quick Source** panel.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="c7984-215">Selecione `Control` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\) para salvar a alteração.</span><span class="sxs-lookup"><span data-stu-id="c7984-215">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="c7984-216">Atualize a página.</span><span class="sxs-lookup"><span data-stu-id="c7984-216">Refresh the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c7984-217">O link na página agora está itálico.</span><span class="sxs-lookup"><span data-stu-id="c7984-217">The link on the page is now italicized.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="O link na página agora está itálico" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       <span data-ttu-id="c7984-219">O link na página agora está itálico</span><span class="sxs-lookup"><span data-stu-id="c7984-219">The link on the page is now italicized</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="c7984-220">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="c7984-220">Next steps</span></span>  

<span data-ttu-id="c7984-221">Use o que você aprendeu neste tutorial para configurar espaços de trabalho em seu próprio projeto.</span><span class="sxs-lookup"><span data-stu-id="c7984-221">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c7984-222">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c7984-222">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md "Começar a exibir e alterar o CSS | Microsoft Docs"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Arquivos de demonstração de espaços de trabalho | Glitch"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Conteúdo - CSS: Folhas de estilo em cascata | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Como começar com o web | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Executando um servidor HTTP local simples | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introdução ao DOM - APIs da Web | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Introdução aos mapas de origem | Treehouse Blog"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Porta \(rede do computador\) - Wikipédia"  

> [!NOTE]
> <span data-ttu-id="c7984-231">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c7984-231">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c7984-232">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="c7984-232">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c7984-234">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c7984-234">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
