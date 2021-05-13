---
description: Saiba como salvar as alterações feitas no DevTools no disco.
title: Editar arquivos com o Workspaces
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 640bb80e01f776c763af053cf8354ce90cf52e93
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564662"
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
# <a name="edit-files-with-workspaces"></a><span data-ttu-id="77bd0-104">Editar arquivos com o Workspaces</span><span class="sxs-lookup"><span data-stu-id="77bd0-104">Edit files with Workspaces</span></span>  

<span data-ttu-id="77bd0-105">Este tutorial fornece prática na configuração e no uso de um Espaço de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="77bd0-105">This tutorial provides hands-on practice in setting up and using a Workspace.</span></span>  <span data-ttu-id="77bd0-106">Depois de adicionar arquivos a um Espaço de Trabalho, as alterações feitas no código-fonte no DevTools são salvas no computador local e são preservadas após a atualização da página da Web.</span><span class="sxs-lookup"><span data-stu-id="77bd0-106">After you add files to a Workspace, the changes that you make in your source code within DevTools are saved on your local computer, and are preserved after you refresh the webpage.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="77bd0-107">**Pré-requisitos**: Antes de começar este tutorial, você deve saber como executar as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="77bd0-107">**Prerequisites**: Before beginning this tutorial, you should know how to perform the following actions.</span></span>  
> 
> *   [<span data-ttu-id="77bd0-108">Usar html, CSS e JavaScript para criar uma página da Web</span><span class="sxs-lookup"><span data-stu-id="77bd0-108">Use html, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="77bd0-109">Usar o DevTools para fazer alterações básicas no CSS</span><span class="sxs-lookup"><span data-stu-id="77bd0-109">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="77bd0-110">Executar um servidor Web HTTP local</span><span class="sxs-lookup"><span data-stu-id="77bd0-110">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <a name="overview"></a><span data-ttu-id="77bd0-111">Visão geral</span><span class="sxs-lookup"><span data-stu-id="77bd0-111">Overview</span></span>  

<span data-ttu-id="77bd0-112">Os espaços de trabalho permitem salvar uma alteração que você faz no Devtools em uma cópia local do mesmo arquivo em seu computador.</span><span class="sxs-lookup"><span data-stu-id="77bd0-112">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="77bd0-113">Para este tutorial, você deve ter as seguintes configurações em seu computador.</span><span class="sxs-lookup"><span data-stu-id="77bd0-113">For this tutorial, you should have the following settings on your machine.</span></span>  

*   <span data-ttu-id="77bd0-114">Você tem o código-fonte do seu site na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="77bd0-114">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="77bd0-115">Você está executando um servidor Web local no diretório de código-fonte, para que o site seja acessível em `localhost:8080` .</span><span class="sxs-lookup"><span data-stu-id="77bd0-115">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="77bd0-116">Você abriu `localhost:8080` no Microsoft Edge e está usando o DevTools para alterar o CSS do site.</span><span class="sxs-lookup"><span data-stu-id="77bd0-116">You opened `localhost:8080` in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="77bd0-117">Com espaços de trabalho habilitados, as alterações CSS feitas no DevTools são salvas no código-fonte da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="77bd0-117">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <a name="limitations"></a><span data-ttu-id="77bd0-118">Limitações</span><span class="sxs-lookup"><span data-stu-id="77bd0-118">Limitations</span></span>  

<span data-ttu-id="77bd0-119">Se você estiver usando uma estrutura moderna, provavelmente transformará seu código-fonte de um formato fácil de manter em um formato otimizado para ser executado o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="77bd0-119">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  

<span data-ttu-id="77bd0-120">Os espaços de trabalho geralmente são capazes de mapear o código otimizado de volta para o código-fonte original com a ajuda de mapas [de origem.][TreehouseBlogSourceMaps]</span><span class="sxs-lookup"><span data-stu-id="77bd0-120">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="77bd0-121">Mas há uma grande variação entre estruturas sobre como cada estrutura usa mapas de origem.</span><span class="sxs-lookup"><span data-stu-id="77bd0-121">But there is a lot of variation between frameworks over how each framework uses source maps.</span></span>  <span data-ttu-id="77bd0-122">Os Devtools não suportam todas as variações.</span><span class="sxs-lookup"><span data-stu-id="77bd0-122">Devtools doesn't support all of the variations.</span></span>  

<span data-ttu-id="77bd0-123">Os espaços de trabalho são conhecidos por não funcionarem com a estrutura a seguir.</span><span class="sxs-lookup"><span data-stu-id="77bd0-123">Workspaces is known to not work with the following framework.</span></span>  

*   <span data-ttu-id="77bd0-124">Criar React App</span><span class="sxs-lookup"><span data-stu-id="77bd0-124">Create React App</span></span>  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <a name="related-feature-local-overrides"></a><span data-ttu-id="77bd0-125">Recurso relacionado: substituições locais</span><span class="sxs-lookup"><span data-stu-id="77bd0-125">Related feature: Local overrides</span></span>  

<span data-ttu-id="77bd0-126">**Substituições Locais** é outro recurso DevTools semelhante a Workspaces.</span><span class="sxs-lookup"><span data-stu-id="77bd0-126">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="77bd0-127">Use Substituições Locais quando quiser experimentar alterações em uma página da Web e você precisa exibir as alterações em cargas de página da Web, mas não se importa em mapear suas alterações no código-fonte da página da Web.</span><span class="sxs-lookup"><span data-stu-id="77bd0-127">Use Local Overrides when you want to experiment with changes to a webpage, and you need to display the changes across webpage loads, but you do not care about mapping your changes to the source code of the webpage.</span></span>  

<!--Todo: add section when content is ready  -->  

## <a name="step-1-set-up"></a><span data-ttu-id="77bd0-128">Etapa 1: Configurar</span><span class="sxs-lookup"><span data-stu-id="77bd0-128">Step 1: Set up</span></span>  

<span data-ttu-id="77bd0-129">Conclua as seguintes ações, para obter experiência prática com Espaços de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="77bd0-129">Complete the following actions, to get hands-on experience with Workspaces.</span></span>  

### <a name="set-up-the-demo"></a><span data-ttu-id="77bd0-130">Configurar a demonstração</span><span class="sxs-lookup"><span data-stu-id="77bd0-130">Set up the demo</span></span>  

1.  <span data-ttu-id="77bd0-131">[Abra a demonstração][GlitchWorkspacesDemo].</span><span class="sxs-lookup"><span data-stu-id="77bd0-131">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Um projeto Glitch" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       <span data-ttu-id="77bd0-133">Um projeto Glitch</span><span class="sxs-lookup"><span data-stu-id="77bd0-133">A Glitch project</span></span>  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Choose **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="77bd0-134">Crie um `app` diretório em sua área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="77bd0-134">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="77bd0-135">Salve cópias dos arquivos do `workspaces-demo` diretório para o `app` diretório.</span><span class="sxs-lookup"><span data-stu-id="77bd0-135">Save copies of the files from the `workspaces-demo` directory to the `app` directory.</span></span>  <span data-ttu-id="77bd0-136">Para o restante do tutorial, o diretório é chamado de `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="77bd0-136">For the rest of the tutorial, the directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="77bd0-137">Inicie um servidor Web local em `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="77bd0-137">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="77bd0-138">Abaixo está um código de exemplo para iniciar `SimpleHTTPServer` , mas você pode usar qualquer servidor que preferir.</span><span class="sxs-lookup"><span data-stu-id="77bd0-138">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
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
    
1.  <span data-ttu-id="77bd0-139">Abra uma guia no Microsoft Edge e navegue até a versão hospedada localmente do site.</span><span class="sxs-lookup"><span data-stu-id="77bd0-139">Open a tab in Microsoft Edge and navigate to locally-hosted version of the site.</span></span>  <span data-ttu-id="77bd0-140">Você deve ser capaz de acessá-lo usando uma URL como `localhost:8080` ou `http://0.0.0.0:8080` .</span><span class="sxs-lookup"><span data-stu-id="77bd0-140">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="77bd0-141">O número [exato da porta][WikiPortURLs] pode ser diferente.</span><span class="sxs-lookup"><span data-stu-id="77bd0-141">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="A demonstração" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       <span data-ttu-id="77bd0-143">A demonstração</span><span class="sxs-lookup"><span data-stu-id="77bd0-143">The demo</span></span>  
    :::image-end:::  
    
### <a name="set-up-devtools"></a><span data-ttu-id="77bd0-144">Configurar o DevTools</span><span class="sxs-lookup"><span data-stu-id="77bd0-144">Set up DevTools</span></span>  

1.  <span data-ttu-id="77bd0-145">Selecione `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\) para abrir o **painel console** do DevTools.</span><span class="sxs-lookup"><span data-stu-id="77bd0-145">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="O painel Console" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       <span data-ttu-id="77bd0-147">O **painel Console**</span><span class="sxs-lookup"><span data-stu-id="77bd0-147">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="77bd0-148">Navegue até a **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="77bd0-148">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="77bd0-149">No painel **Navegador** (à esquerda), escolha a **guia Sistema de** Arquivos.</span><span class="sxs-lookup"><span data-stu-id="77bd0-149">In the **Navigator** pane (on the left), choose the **Filesystem** tab.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="A guia Sistema de Arquivos" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       <span data-ttu-id="77bd0-151">A **guia Sistema de** Arquivos</span><span class="sxs-lookup"><span data-stu-id="77bd0-151">The **Filesystem** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="77bd0-152">Escolha **Adicionar pasta ao espaço de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="77bd0-152">Choose **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="77bd0-153">Digite `~/Desktop/app`.</span><span class="sxs-lookup"><span data-stu-id="77bd0-153">Type `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="77bd0-154">Escolha **Permitir** para dar permissão ao DevTools para ler e gravar no diretório.</span><span class="sxs-lookup"><span data-stu-id="77bd0-154">Choose **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="77bd0-155">Na guia **Sistema de** Arquivos, um ponto verde agora aparece ao lado de , `index.html` e `script.js` `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="77bd0-155">In the **Filesystem** tab, a green dot now appears next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="77bd0-156">Um ponto verde indica que o DevTools estabeleceu um mapeamento entre um recurso de rede da página e o arquivo em `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="77bd0-156">A green dot indicates that DevTools has established a mapping between a network resource of the page, and the file in `~/Desktop/app`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="A guia Sistema de Arquivos agora indica um mapeamento entre os arquivos locais e os de rede" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       <span data-ttu-id="77bd0-158">A **guia Sistema de** Arquivos agora indica um mapeamento entre os arquivos locais e os de rede</span><span class="sxs-lookup"><span data-stu-id="77bd0-158">The **Filesystem** tab now indicates a mapping between the local files and the network ones</span></span>  
    :::image-end:::  
    
## <a name="step-2-save-a-css-change-to-disk"></a><span data-ttu-id="77bd0-159">Etapa 2: Salvar uma alteração CSS no disco</span><span class="sxs-lookup"><span data-stu-id="77bd0-159">Step 2: Save a CSS change to disk</span></span>  

1.  <span data-ttu-id="77bd0-160">Abra `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="77bd0-160">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="77bd0-161">A `color` propriedade de elementos é definida como `h1` `fuchsia` .</span><span class="sxs-lookup"><span data-stu-id="77bd0-161">The `color` property of `h1` elements is set to `fuchsia`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Exibir styles.css em um editor de texto" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       <span data-ttu-id="77bd0-163">Exibir `styles.css` em um editor de texto</span><span class="sxs-lookup"><span data-stu-id="77bd0-163">View `styles.css` in a text editor</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="77bd0-164">Escolha a **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="77bd0-164">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="77bd0-165">Altere o valor `color` da propriedade do elemento para sua cor `<h1>` favorita.</span><span class="sxs-lookup"><span data-stu-id="77bd0-165">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="77bd0-166">Lembre-se de que você precisa escolher o elemento na Árvore DOM para exibir as regras CSS aplicadas a `<h1>` ele no painel **Estilos.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="77bd0-166">Remember that you need to choose the `<h1>` element in the **DOM Tree** in order to display the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="77bd0-167">O ponto verde ao lado `styles.css:1` significa que qualquer alteração que você fizer será mapeada para `~/Desktop/app/styles.css` .</span><span class="sxs-lookup"><span data-stu-id="77bd0-167">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="O indicador verde que o arquivo está vinculado" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       <span data-ttu-id="77bd0-169">O indicador verde que o arquivo está vinculado</span><span class="sxs-lookup"><span data-stu-id="77bd0-169">The green indicator that the file is linked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="77bd0-170">Abra `styles.css` em um editor de texto novamente.</span><span class="sxs-lookup"><span data-stu-id="77bd0-170">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="77bd0-171">A `color` propriedade agora está definida como sua cor favorita.</span><span class="sxs-lookup"><span data-stu-id="77bd0-171">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="77bd0-172">Atualize a página.</span><span class="sxs-lookup"><span data-stu-id="77bd0-172">Refresh the page.</span></span>  <span data-ttu-id="77bd0-173">A cor do `<h1>` elemento ainda está definida como sua cor favorita.</span><span class="sxs-lookup"><span data-stu-id="77bd0-173">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="77bd0-174">A alteração permanece em uma atualização, porque quando você fez a alteração DevTools salvou a alteração no disco.</span><span class="sxs-lookup"><span data-stu-id="77bd0-174">The change remains across a refresh, because when you made the change DevTools saved the change to disk.</span></span>  <span data-ttu-id="77bd0-175">E, quando você atualizeu a página, seu servidor local atendeu a cópia modificada do arquivo do disco.</span><span class="sxs-lookup"><span data-stu-id="77bd0-175">And then, when you refreshed the page, your local server served the modified copy of the file from disk.</span></span>  
    
## <a name="step-3-save-an-html-change-to-disk"></a><span data-ttu-id="77bd0-176">Etapa 3: Salvar uma alteração HTML no disco</span><span class="sxs-lookup"><span data-stu-id="77bd0-176">Step 3: Save an HTML change to disk</span></span>  

### <a name="change-html-from-the-elements-panel"></a><span data-ttu-id="77bd0-177">Alterar HTML do Painel de Elementos</span><span class="sxs-lookup"><span data-stu-id="77bd0-177">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="77bd0-178">Você pode fazer alterações no html do Painel de Elementos, mas suas alterações na árvore DOM não são salvas no disco e só efetivam a sessão atual do navegador.</span><span class="sxs-lookup"><span data-stu-id="77bd0-178">You may make changes to the html from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  

<span data-ttu-id="77bd0-179">A árvore DOM não é html.</span><span class="sxs-lookup"><span data-stu-id="77bd0-179">The DOM tree is not html.</span></span>  

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

### <a name="change-html-from-the-sources-tool"></a><span data-ttu-id="77bd0-180">Alterar HTML da ferramenta Sources</span><span class="sxs-lookup"><span data-stu-id="77bd0-180">Change HTML from the Sources tool</span></span>  

<span data-ttu-id="77bd0-181">Se você quiser salvar uma alteração no HTML da página da Web, use a **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="77bd0-181">If you want to save a change to the HTML of the webpage, use the **Sources** tool.</span></span>  

1.  <span data-ttu-id="77bd0-182">Navegue até a **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="77bd0-182">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="77bd0-183">No painel **Navegador** (à esquerda), escolha a **guia** Página.</span><span class="sxs-lookup"><span data-stu-id="77bd0-183">In the **Navigator** pane (on the left), choose the **Page** tab.</span></span>  
1.  <span data-ttu-id="77bd0-184">Escolha **(índice)**.</span><span class="sxs-lookup"><span data-stu-id="77bd0-184">Choose **(index)**.</span></span>  <span data-ttu-id="77bd0-185">O HTML da página é aberto.</span><span class="sxs-lookup"><span data-stu-id="77bd0-185">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="77bd0-186">Substitua `<h1>Workspaces Demo</h1>` por `<h1>I ❤️  Cake</h1>` .</span><span class="sxs-lookup"><span data-stu-id="77bd0-186">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="77bd0-187">Revise a figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="77bd0-187">Review the following figure.</span></span>  
1.  <span data-ttu-id="77bd0-188">Selecione `Control` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\) para salvar a alteração.</span><span class="sxs-lookup"><span data-stu-id="77bd0-188">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="77bd0-189">Atualize a página.</span><span class="sxs-lookup"><span data-stu-id="77bd0-189">Refresh the page.</span></span>  <span data-ttu-id="77bd0-190">O `<h1>` elemento continua a exibir o novo texto após a atualização da página.</span><span class="sxs-lookup"><span data-stu-id="77bd0-190">The `<h1>` element continues to display the new text after the page is refreshed.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Alterar HTML da ferramenta Sources" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       <span data-ttu-id="77bd0-192">Alterar HTML da ferramenta **Sources**</span><span class="sxs-lookup"><span data-stu-id="77bd0-192">Change HTML from the **Sources** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="77bd0-193">Abra `~/Desktop/app/index.html` .</span><span class="sxs-lookup"><span data-stu-id="77bd0-193">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="77bd0-194">O `<h1>` elemento contém o novo texto.</span><span class="sxs-lookup"><span data-stu-id="77bd0-194">The `<h1>` element contains the new text.</span></span>  
    
## <a name="step-4-save-a-javascript-change-to-disk"></a><span data-ttu-id="77bd0-195">Etapa 4: Salvar uma alteração do JavaScript no disco</span><span class="sxs-lookup"><span data-stu-id="77bd0-195">Step 4: Save a JavaScript change to disk</span></span>  

<span data-ttu-id="77bd0-196">O principal local para usar o editor de código do DevTools é a **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="77bd0-196">The main place to use the code editor of DevTools is the **Sources** tool.</span></span>  <span data-ttu-id="77bd0-197">Mas, às vezes, você precisa acessar outras ferramentas, como a **ferramenta Elements** ou o **painel console,** durante a edição de arquivos.</span><span class="sxs-lookup"><span data-stu-id="77bd0-197">But sometimes you need to access other tools, such as the **Elements** tool or the **Console** panel, while editing files.</span></span>  <span data-ttu-id="77bd0-198">A **ferramenta De origem** Rápida fornece apenas o editor da ferramenta **Fontes,** enquanto qualquer ferramenta está aberta.</span><span class="sxs-lookup"><span data-stu-id="77bd0-198">The **Quick Source** tool gives you just the editor from the **Sources** tool, while any tool is open.</span></span>  

<span data-ttu-id="77bd0-199">Para abrir o editor de código do DevTools juntamente com outras ferramentas, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="77bd0-199">To open the DevTools code editor alongside other tools, do the following:</span></span>  

1.  <span data-ttu-id="77bd0-200">Navegue até **a ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="77bd0-200">Navigate to the **Elements** tool.</span></span>  
1.  <span data-ttu-id="77bd0-201">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="77bd0-201">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="77bd0-202">O **Menu de Comando** é aberto.</span><span class="sxs-lookup"><span data-stu-id="77bd0-202">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="77bd0-203">Digite `Quick Source` e escolha Mostrar Fonte **Rápida**.</span><span class="sxs-lookup"><span data-stu-id="77bd0-203">Type `Quick Source`, and then choose **Show Quick Source**.</span></span>  <span data-ttu-id="77bd0-204">Na parte inferior da janela DevTools, a ferramenta **Fonte** Rápida é exibida, exibindo o conteúdo de , que é o último arquivo editado na `index.html` ferramenta **Fontes.**</span><span class="sxs-lookup"><span data-stu-id="77bd0-204">At the bottom of the DevTools window, the **Quick Source** tool appears, displaying the contents of `index.html`, which is the last file you edited in the **Sources** tool.</span></span>    
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Abra a ferramenta Fonte Rápida usando o Menu de Comando" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       <span data-ttu-id="77bd0-206">Abra a **ferramenta Fonte** Rápida usando o Menu **de Comando**</span><span class="sxs-lookup"><span data-stu-id="77bd0-206">Open the **Quick Source** tool by using the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="77bd0-207">Selecione `Control` + `P` \(Windows, Linux\) `Command` + `P` ou \(macOS\) para abrir a **caixa de diálogo Abrir Arquivo.**</span><span class="sxs-lookup"><span data-stu-id="77bd0-207">Select `Control`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="77bd0-208">Revise a figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="77bd0-208">Review the following figure.</span></span>  
1.  <span data-ttu-id="77bd0-209">Digite `script` , escolha **aplicativo/script.js**.</span><span class="sxs-lookup"><span data-stu-id="77bd0-209">Type `script`, then choose **app/script.js**.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Abra script.js usando a caixa de diálogo Abrir Arquivo" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       <span data-ttu-id="77bd0-211">Abrir `script.js` usando a caixa de diálogo Abrir **Arquivo**</span><span class="sxs-lookup"><span data-stu-id="77bd0-211">Open `script.js` using the **Open File** dialog</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="77bd0-212">O `Save Changes To Disk With Workspaces` link na demonstração é estilizado regularmente.</span><span class="sxs-lookup"><span data-stu-id="77bd0-212">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="77bd0-213">Adicione o código a seguir à parte inferior \*\* do \*\*script.jsusando a ferramenta **De origem** rápida.</span><span class="sxs-lookup"><span data-stu-id="77bd0-213">Add the following code to the bottom of **script.js** using the **Quick Source** tool.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="77bd0-214">Selecione `Control` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\) para salvar a alteração.</span><span class="sxs-lookup"><span data-stu-id="77bd0-214">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="77bd0-215">Atualize a página.</span><span class="sxs-lookup"><span data-stu-id="77bd0-215">Refresh the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="77bd0-216">O link na página agora está itálico.</span><span class="sxs-lookup"><span data-stu-id="77bd0-216">The link on the page is now italicized.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="O link na página agora está itálico" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       <span data-ttu-id="77bd0-218">O link na página agora está itálico</span><span class="sxs-lookup"><span data-stu-id="77bd0-218">The link on the page is now italicized</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="77bd0-219">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="77bd0-219">Next steps</span></span>  

<span data-ttu-id="77bd0-220">Use o que você aprendeu neste tutorial para configurar espaços de trabalho em seu próprio projeto.</span><span class="sxs-lookup"><span data-stu-id="77bd0-220">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="77bd0-221">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="77bd0-221">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Uma introdução ao código-fonte Mapas | Treehouse Blog"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Porta \(rede do computador\) - Wikipédia"  

> [!NOTE]
> <span data-ttu-id="77bd0-230">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="77bd0-230">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="77bd0-231">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="77bd0-231">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="77bd0-233">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="77bd0-233">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
