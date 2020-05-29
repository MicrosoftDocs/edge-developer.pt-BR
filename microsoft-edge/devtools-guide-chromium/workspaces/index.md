---
title: Editar arquivos com espaços de trabalho
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 612e85b8b00a78a40e53ac5c33d187fdae174024
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601843"
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







# <span data-ttu-id="e3167-103">Editar arquivos com espaços de trabalho</span><span class="sxs-lookup"><span data-stu-id="e3167-103">Edit Files With Workspaces</span></span>   



> [!NOTE]
> <span data-ttu-id="e3167-104">O objetivo deste tutorial é fornecer uma prática prática para configurar e usar espaços de trabalho, para que você possa usar os espaços de trabalho em seus próprios projetos.</span><span class="sxs-lookup"><span data-stu-id="e3167-104">The goal of this tutorial is to provide hands-on practice in setting up and using Workspaces, so that you are able to use Workspaces in your own projects.</span></span>  <span data-ttu-id="e3167-105">Você pode salvar as alterações no código-fonte em seu computador local, que você fez no DevTools depois de habilitar os espaços de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e3167-105">You are able to save the changes to the source code, on your local computer, that you made within DevTools after you enable Workspaces.</span></span>  

> [!CAUTION]
> <span data-ttu-id="e3167-106">**Pré-requisitos**: antes de iniciar este tutorial, você deve saber como:</span><span class="sxs-lookup"><span data-stu-id="e3167-106">**Prerequisites**: Before beginning this tutorial, you should know how to:</span></span>  
> *   [<span data-ttu-id="e3167-107">Usar HTML, CSS e JavaScript para criar uma página da Web</span><span class="sxs-lookup"><span data-stu-id="e3167-107">Use HTML, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="e3167-108">Usar o DevTools para fazer alterações básicas em CSS</span><span class="sxs-lookup"><span data-stu-id="e3167-108">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="e3167-109">Executar um servidor Web HTTP local</span><span class="sxs-lookup"><span data-stu-id="e3167-109">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <span data-ttu-id="e3167-110">Visão geral</span><span class="sxs-lookup"><span data-stu-id="e3167-110">Overview</span></span>   

<span data-ttu-id="e3167-111">Os espaços de trabalho permitem salvar uma alteração feita no devtools em uma cópia local do mesmo arquivo em seu computador.</span><span class="sxs-lookup"><span data-stu-id="e3167-111">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="e3167-112">Por exemplo, suponha que:</span><span class="sxs-lookup"><span data-stu-id="e3167-112">For example, suppose:</span></span>  

*   <span data-ttu-id="e3167-113">Você tem o código-fonte do seu site na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e3167-113">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="e3167-114">Você está executando um servidor Web local do diretório de código-fonte, para que o site possa ser acessado em `localhost:8080` .</span><span class="sxs-lookup"><span data-stu-id="e3167-114">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="e3167-115">Você abriu `localhost:8080` no Microsoft Edge e está usando o devtools para alterar a CSS do site.</span><span class="sxs-lookup"><span data-stu-id="e3167-115">You opened `localhost:8080`  in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="e3167-116">Com os espaços de trabalho habilitados, as alterações de CSS feitas em DevTools são salvas no código-fonte na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e3167-116">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <span data-ttu-id="e3167-117">Limitações</span><span class="sxs-lookup"><span data-stu-id="e3167-117">Limitations</span></span>   

<span data-ttu-id="e3167-118">Se você estiver usando uma estrutura moderna, ele provavelmente transforma o código-fonte de um formato fácil de manter em um formato otimizado para ser executado o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="e3167-118">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  
<span data-ttu-id="e3167-119">Em geral, os espaços de trabalho são capazes de mapear o código otimizado de volta ao código-fonte original com a ajuda dos [mapas de origem][TreehouseBlogSourceMaps].</span><span class="sxs-lookup"><span data-stu-id="e3167-119">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="e3167-120">Mas há uma grande quantidade de variações entre estruturas sobre como elas usam mapas de origem.</span><span class="sxs-lookup"><span data-stu-id="e3167-120">But there is a lot of variation between frameworks over how they use source maps.</span></span>  <span data-ttu-id="e3167-121">Devtools simplesmente dá suporte a todas as variações.</span><span class="sxs-lookup"><span data-stu-id="e3167-121">Devtools simply does support all the variations.</span></span>  

<span data-ttu-id="e3167-122">Não se sabe que os espaços de trabalho não funcionam com esses frameworks:</span><span class="sxs-lookup"><span data-stu-id="e3167-122">Workspaces is known to not work with these frameworks:</span></span>  

*   <span data-ttu-id="e3167-123">Criar aplicativo reagir</span><span class="sxs-lookup"><span data-stu-id="e3167-123">Create React App</span></span>  

<!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

## <span data-ttu-id="e3167-124">Recurso relacionado: substituições locais</span><span class="sxs-lookup"><span data-stu-id="e3167-124">Related feature: Local Overrides</span></span>   

<span data-ttu-id="e3167-125">**Substituições locais** é outro recurso de devtools semelhante a espaços de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e3167-125">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="e3167-126">Use substituições locais quando você deseja experimentar alterações em uma página, e você precisa ver essas alterações nas cargas da página, mas não importa o mapeamento das alterações para o código-fonte da página.</span><span class="sxs-lookup"><span data-stu-id="e3167-126">Use Local Overrides when you want to experiment with changes to a page, and you need to see those changes across page loads, but you do not care about mapping your changes to the source code of the page.</span></span>  

<!--Todo: add section when content is ready  -->  

## <span data-ttu-id="e3167-127">Etapa 1: configurar</span><span class="sxs-lookup"><span data-stu-id="e3167-127">Step 1: Setup</span></span>   

<span data-ttu-id="e3167-128">Preencha este tutorial para obter experiência prática com espaços de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e3167-128">Complete this tutorial to get hands-on experience with Workspaces.</span></span>  

### <span data-ttu-id="e3167-129">Configurar a demonstração</span><span class="sxs-lookup"><span data-stu-id="e3167-129">Set up the demo</span></span>   

1.  <span data-ttu-id="e3167-130">[Abra a demonstração][GlitchWorkspacesDemo].</span><span class="sxs-lookup"><span data-stu-id="e3167-130">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    > ##### <span data-ttu-id="e3167-131">Figura 1</span><span class="sxs-lookup"><span data-stu-id="e3167-131">Figure 1</span></span>  
    > <span data-ttu-id="e3167-132">Um projeto de falha em ![ um projeto de falha][ImageGlitchProject]</span><span class="sxs-lookup"><span data-stu-id="e3167-132">A Glitch project ![A Glitch project][ImageGlitchProject]</span></span>  
    
    <!--1.  Click the project name.  -->
    <!--1.  Select **Advanced Options** > **Download Project**.  
    
    > ##### Figure 2  
    > The Download Project button  
    > ![The Download Project button][ImageDownloadProjectButton]  
    -->
    <!--1.  Close the tab.  -->
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial this directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="e3167-133">Crie um `app` diretório na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e3167-133">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="e3167-134">Salvar cópias dos arquivos no `workspaces-demo` diretório.</span><span class="sxs-lookup"><span data-stu-id="e3167-134">Save copies of the files in the `workspaces-demo` directory.</span></span>  <span data-ttu-id="e3167-135">Para o restante deste tutorial, este diretório é conhecido como `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="e3167-135">For the rest of this tutorial this directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="e3167-136">Inicie um servidor Web local `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="e3167-136">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="e3167-137">Veja a seguir um exemplo de código para inicialização `SimpleHTTPServer` , mas você pode usar qualquer servidor de sua preferência.</span><span class="sxs-lookup"><span data-stu-id="e3167-137">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
    ```bash
    cd ~/Desktop/app
    python -m SimpleHTTPServer # Python 2
    ```  
    
    ```bash
    cd ~/Desktop/app
    python -m http.server # Python 3
    ```  
    
1.  <span data-ttu-id="e3167-138">Abra uma guia no Microsoft Edge e vá para a versão hospedada localmente do site.</span><span class="sxs-lookup"><span data-stu-id="e3167-138">Open a tab in Microsoft Edge and go to locally-hosted version of the site.</span></span>  <span data-ttu-id="e3167-139">Você deve ser capaz de acessá-lo usando uma URL como `localhost:8080` ou `http://0.0.0.0:8080` .</span><span class="sxs-lookup"><span data-stu-id="e3167-139">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="e3167-140">O [número de porta][WikiPortURLs] exato pode ser diferente.</span><span class="sxs-lookup"><span data-stu-id="e3167-140">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    > ##### <span data-ttu-id="e3167-141">Figura 2</span><span class="sxs-lookup"><span data-stu-id="e3167-141">Figure 2</span></span>  
    > <span data-ttu-id="e3167-142">A demonstração</span><span class="sxs-lookup"><span data-stu-id="e3167-142">The demo</span></span>  
    > <span data-ttu-id="e3167-143">! [A demonstração] [ImageDemo]</span><span class="sxs-lookup"><span data-stu-id="e3167-143">![The demo][ImageDemo]</span></span>  

### <span data-ttu-id="e3167-144">Configurar o DevTools</span><span class="sxs-lookup"><span data-stu-id="e3167-144">Set up DevTools</span></span>   

1.  <span data-ttu-id="e3167-145">Pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) para abrir o painel do **console** do devtools.</span><span class="sxs-lookup"><span data-stu-id="e3167-145">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    > ##### <span data-ttu-id="e3167-146">Figura 3</span><span class="sxs-lookup"><span data-stu-id="e3167-146">Figure 3</span></span>  
    > <span data-ttu-id="e3167-147">Painel do **console**</span><span class="sxs-lookup"><span data-stu-id="e3167-147">The **Console** panel</span></span>  
    > <span data-ttu-id="e3167-148">! [O painel do console] [ImageConsolePanel]</span><span class="sxs-lookup"><span data-stu-id="e3167-148">![The Console panel][ImageConsolePanel]</span></span>  

1.  <span data-ttu-id="e3167-149">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="e3167-149">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="e3167-150">Clique na guia **FileSystem** .</span><span class="sxs-lookup"><span data-stu-id="e3167-150">Click the **Filesystem** tab.</span></span>  
    
    > ##### <span data-ttu-id="e3167-151">Figura 4</span><span class="sxs-lookup"><span data-stu-id="e3167-151">Figure 4</span></span>  
    > <span data-ttu-id="e3167-152">A guia **sistema de arquivos**</span><span class="sxs-lookup"><span data-stu-id="e3167-152">The **Filesystem** tab</span></span>  
    > <span data-ttu-id="e3167-153">! [Guia sistema de arquivos] [ImageFilesystem]</span><span class="sxs-lookup"><span data-stu-id="e3167-153">![The Filesystem tab][ImageFilesystem]</span></span>  

1.  <span data-ttu-id="e3167-154">Clique em **Adicionar pasta ao espaço de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="e3167-154">Click **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="e3167-155">Selecione `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="e3167-155">Select `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="e3167-156">Clique em **permitir** para conceder ao devtools permissão para ler e gravar no diretório.</span><span class="sxs-lookup"><span data-stu-id="e3167-156">Click **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="e3167-157">Na guia **sistema de sistema** , agora há um ponto verde ao lado de `index.html` , `script.js` e `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="e3167-157">In the **Filesystem** tab, there is now a green dot next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="e3167-158">Esses pontos verdes significam que o DevTools estabeleceu um mapeamento entre os recursos de rede da página e os arquivos `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="e3167-158">These green dots mean that DevTools has established a mapping between the network resources of the page, and the files in `~/Desktop/app`.</span></span>  
    
    > ##### <span data-ttu-id="e3167-159">Figura 5</span><span class="sxs-lookup"><span data-stu-id="e3167-159">Figure 5</span></span>  
    > <span data-ttu-id="e3167-160">A guia **sistema de arquivos** agora mostra um mapeamento entre os arquivos locais e os de rede</span><span class="sxs-lookup"><span data-stu-id="e3167-160">The **Filesystem** tab now shows a mapping between the local files and the network ones</span></span>  
    > <span data-ttu-id="e3167-161">! [A guia sistema de arquivos agora mostra um mapeamento entre os arquivos locais e os de rede] [ImageMapping]</span><span class="sxs-lookup"><span data-stu-id="e3167-161">![The Filesystem tab now shows a mapping between the local files and the network ones][ImageMapping]</span></span>  

## <span data-ttu-id="e3167-162">Etapa 2: salvar uma alteração de CSS em disco</span><span class="sxs-lookup"><span data-stu-id="e3167-162">Step 2: Save a CSS change to disk</span></span>   

1.  <span data-ttu-id="e3167-163">Abrir `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="e3167-163">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    ><span data-ttu-id="e3167-164">A `color` propriedade dos `h1` elementos é definida como `fuchsia` .</span><span class="sxs-lookup"><span data-stu-id="e3167-164">The `color` property of `h1` elements is set to `fuchsia`.</span></span>
    
    > ##### <span data-ttu-id="e3167-165">Figura 6</span><span class="sxs-lookup"><span data-stu-id="e3167-165">Figure 6</span></span>  
    > <span data-ttu-id="e3167-166">Exibir `styles.css` em um editor de texto</span><span class="sxs-lookup"><span data-stu-id="e3167-166">Viewing `styles.css` in a text editor</span></span>  
    > <span data-ttu-id="e3167-167">! [Exibindo estilos. CSS em um editor de texto] [ImageStylesFuchsia]</span><span class="sxs-lookup"><span data-stu-id="e3167-167">![Viewing styles.css in a text editor][ImageStylesFuchsia]</span></span>  


1.  <span data-ttu-id="e3167-168">Clique na guia **elementos** .</span><span class="sxs-lookup"><span data-stu-id="e3167-168">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="e3167-169">Altere o valor da `color` Propriedade do `<h1>` elemento para sua cor favorita.</span><span class="sxs-lookup"><span data-stu-id="e3167-169">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="e3167-170">Lembre-se de que você precisa clicar no `<h1>` elemento na **árvore DOM** para ver as regras CSS aplicadas a ele no painel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="e3167-170">Remember that you need to click the `<h1>` element in the **DOM Tree** in order to see the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="e3167-171">O ponto verde ao lado de `styles.css:1` significa que qualquer alteração feita está mapeada `~/Desktop/app/styles.css` .</span><span class="sxs-lookup"><span data-stu-id="e3167-171">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    > ##### <span data-ttu-id="e3167-172">Figura 7</span><span class="sxs-lookup"><span data-stu-id="e3167-172">Figure 7</span></span>  
    > <span data-ttu-id="e3167-173">O indicador verde para o qual o arquivo está vinculado</span><span class="sxs-lookup"><span data-stu-id="e3167-173">The green indicator that the file is linked</span></span>  
    > <span data-ttu-id="e3167-174">! [O indicador verde no qual o arquivo está vinculado] [ImageStylesGreen]</span><span class="sxs-lookup"><span data-stu-id="e3167-174">![The green indicator that the file is linked][ImageStylesGreen]</span></span>  

1.  <span data-ttu-id="e3167-175">Abra `styles.css` em um editor de texto novamente.</span><span class="sxs-lookup"><span data-stu-id="e3167-175">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="e3167-176">A `color` Propriedade agora está definida como sua cor favorita.</span><span class="sxs-lookup"><span data-stu-id="e3167-176">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="e3167-177">Recarregar a página.</span><span class="sxs-lookup"><span data-stu-id="e3167-177">Reload the page.</span></span>  <span data-ttu-id="e3167-178">A cor do `<h1>` elemento ainda está definida para sua cor favorita.</span><span class="sxs-lookup"><span data-stu-id="e3167-178">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="e3167-179">Isso funciona porque quando você fez a alteração, o DevTools salvou a alteração em disco.</span><span class="sxs-lookup"><span data-stu-id="e3167-179">This works because when you made the change, DevTools saved the change to disk.</span></span>  <span data-ttu-id="e3167-180">Depois, quando você recarregar a página, o servidor local atuou na cópia modificada do disco.</span><span class="sxs-lookup"><span data-stu-id="e3167-180">And then, when you reloaded the page, your local server served the modified copy of the file from disk.</span></span>  

## <span data-ttu-id="e3167-181">Etapa 3: salvar uma alteração de HTML em disco</span><span class="sxs-lookup"><span data-stu-id="e3167-181">Step 3: Save an HTML change to disk</span></span>   

### <span data-ttu-id="e3167-182">Alterar o HTML do painel elementos</span><span class="sxs-lookup"><span data-stu-id="e3167-182">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="e3167-183">Você pode fazer alterações no HTML a partir do painel de elementos, mas as alterações na árvore DOM não são salvas em disco e só afetam a sessão atual do navegador.</span><span class="sxs-lookup"><span data-stu-id="e3167-183">You may make changes to the HTML from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  
<span data-ttu-id="e3167-184">A árvore DOM não é HTML.</span><span class="sxs-lookup"><span data-stu-id="e3167-184">The DOM tree is not HTML.</span></span>  

<!--### Try changing HTML from the Elements panel   

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Click the **Elements** tab.  
1.  Double click the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    > ##### Old Figure 9  
    > Attempting to change HTML from the **DOM Tree** of the **Elements** panel  
    > ![Attempting to change HTML from the DOM Tree of the Elements panel][ImageElementsCake]  

1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Reload the page.  The page reverts to its original title.  

#### Optional: Why it is not working   

> [!NOTE]
> This section describes why the workflow from [Try changing HTML from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that you see on the **Elements** panel represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches HTML over the network, parses the HTML, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the page that users see may be very different from the HTML that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** panel should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->
### <span data-ttu-id="e3167-185">Alterar o HTML no painel fontes</span><span class="sxs-lookup"><span data-stu-id="e3167-185">Change HTML from the Sources panel</span></span>   

<span data-ttu-id="e3167-186">Se você quiser salvar uma alteração no HTML da página, use o painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="e3167-186">If you want to save a change to the HTML of the page, do it using the **Sources** panel.</span></span>  

1.  <span data-ttu-id="e3167-187">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="e3167-187">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="e3167-188">Clique na guia **página** .</span><span class="sxs-lookup"><span data-stu-id="e3167-188">Click the **Page** tab.</span></span>  
1.  <span data-ttu-id="e3167-189">Clique em **(índice)**.</span><span class="sxs-lookup"><span data-stu-id="e3167-189">Click **(index)**.</span></span>  <span data-ttu-id="e3167-190">O HTML da página é aberto.</span><span class="sxs-lookup"><span data-stu-id="e3167-190">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="e3167-191">Substituir `<h1>Workspaces Demo</h1>` por `<h1>I ❤️  Cake</h1>` .</span><span class="sxs-lookup"><span data-stu-id="e3167-191">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="e3167-192">Veja a [Figura 8](#figure-8).</span><span class="sxs-lookup"><span data-stu-id="e3167-192">See [Figure 8](#figure-8).</span></span>  
1.  <span data-ttu-id="e3167-193">Pressione `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) para salvar a alteração.</span><span class="sxs-lookup"><span data-stu-id="e3167-193">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="e3167-194">Recarregar a página.</span><span class="sxs-lookup"><span data-stu-id="e3167-194">Reload the page.</span></span>  <span data-ttu-id="e3167-195">O `<h1>` elemento ainda está exibindo o novo texto.</span><span class="sxs-lookup"><span data-stu-id="e3167-195">The `<h1>` element is still displaying the new text.</span></span>  
    
    > ##### <span data-ttu-id="e3167-196">Figura 8</span><span class="sxs-lookup"><span data-stu-id="e3167-196">Figure 8</span></span>  
    > <span data-ttu-id="e3167-197">A linha 12 foi definida como</span><span class="sxs-lookup"><span data-stu-id="e3167-197">Line 12 has been set to</span></span> `I ❤️  Cake`  
    > <span data-ttu-id="e3167-198">! [Alterando HTML no painel fontes] [ImageSourcesCakeHTML]</span><span class="sxs-lookup"><span data-stu-id="e3167-198">![Changing HTML from the Sources panel][ImageSourcesCakeHTML]</span></span>  

1.  <span data-ttu-id="e3167-199">Abrir `~/Desktop/app/index.html` .</span><span class="sxs-lookup"><span data-stu-id="e3167-199">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="e3167-200">O `<h1>` elemento contém o novo texto.</span><span class="sxs-lookup"><span data-stu-id="e3167-200">The `<h1>` element contains the new text.</span></span>  

## <span data-ttu-id="e3167-201">Etapa 4: salvar uma alteração de JavaScript em disco</span><span class="sxs-lookup"><span data-stu-id="e3167-201">Step 4: Save a JavaScript change to disk</span></span>   

<span data-ttu-id="e3167-202">O painel **fontes** também é o local para fazer alterações em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e3167-202">The **Sources** panel is also the place to make changes to JavaScript.</span></span>  <span data-ttu-id="e3167-203">Mas, às vezes, você precisa acessar outros painéis, como o painel **elementos** ou o painel do **console** , ao fazer alterações em seu site.</span><span class="sxs-lookup"><span data-stu-id="e3167-203">But sometimes you need to access other panels, such as the **Elements** panel or the **Console** panel, while making changes to your site.</span></span>  <span data-ttu-id="e3167-204">Há uma maneira de ter o painel **fontes** aberto junto com outros painéis.</span><span class="sxs-lookup"><span data-stu-id="e3167-204">There is a way to have the **Sources** panel open alongside other panels.</span></span>  

1.  <span data-ttu-id="e3167-205">Clique na guia **elementos** .</span><span class="sxs-lookup"><span data-stu-id="e3167-205">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="e3167-206">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="e3167-206">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="e3167-207">O **menu de comando** é aberto.</span><span class="sxs-lookup"><span data-stu-id="e3167-207">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="e3167-208">Digite `QS` e selecione **Mostrar fonte rápida**.</span><span class="sxs-lookup"><span data-stu-id="e3167-208">Type `QS`, then select **Show Quick Source**.</span></span>  <span data-ttu-id="e3167-209">Na parte inferior da janela do DevTools, agora há uma guia **fonte rápida** .  A guia exibe o conteúdo de `index.html` , que é o último arquivo editado no painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="e3167-209">At the bottom of your DevTools window there is now a **Quick Source** tab.  The tab is displaying the contents of `index.html`, which is the last file you edited in the **Sources** panel.</span></span>  <span data-ttu-id="e3167-210">A guia **fonte rápida** oferece o editor do painel **fontes** , para que você possa editar arquivos enquanto tiver outros painéis abertos.</span><span class="sxs-lookup"><span data-stu-id="e3167-210">The **Quick Source** tab gives you the editor from the **Sources** panel, so that you are able to edit files while having other panels open.</span></span>  
    
    > ##### <span data-ttu-id="e3167-211">Figura 9</span><span class="sxs-lookup"><span data-stu-id="e3167-211">Figure 9</span></span>  
    > <span data-ttu-id="e3167-212">Abrir a guia **fonte rápida** usando o **menu de comandos**</span><span class="sxs-lookup"><span data-stu-id="e3167-212">Opening the **Quick Source** tab using the **Command Menu**</span></span>  
    > <span data-ttu-id="e3167-213">! [Abrindo a guia fonte rápida usando o menu de comando] [ImageCommandMenuQuickSource]</span><span class="sxs-lookup"><span data-stu-id="e3167-213">![Opening the Quick Source tab using Command Menu][ImageCommandMenuQuickSource]</span></span>  

1.  <span data-ttu-id="e3167-214">Pressione `Control` + `P` \ (Windows \) ou `Command` + `P` \ (MacOS \) para abrir a caixa de diálogo **Abrir arquivo** .</span><span class="sxs-lookup"><span data-stu-id="e3167-214">Press `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="e3167-215">Veja a [Figura 10](#figure-10).</span><span class="sxs-lookup"><span data-stu-id="e3167-215">See [Figure 10](#figure-10).</span></span>  
1.  <span data-ttu-id="e3167-216">Digite `script` e, em seguida, selecione **app/script. js**.</span><span class="sxs-lookup"><span data-stu-id="e3167-216">Type `script`, then select **app/script.js**.</span></span>  
    
    > ##### <span data-ttu-id="e3167-217">Figura 10</span><span class="sxs-lookup"><span data-stu-id="e3167-217">Figure 10</span></span>  
    > <span data-ttu-id="e3167-218">Abrindo `script.js` usando a caixa de diálogo **Abrir arquivo**</span><span class="sxs-lookup"><span data-stu-id="e3167-218">Opening `script.js` using the **Open File** dialog</span></span>  
    > <span data-ttu-id="e3167-219">! [Abrindo script. js usando a caixa de diálogo abrir arquivo] [ImageOpenFileDialog]</span><span class="sxs-lookup"><span data-stu-id="e3167-219">![Opening script.js using the Open File dialog][ImageOpenFileDialog]</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e3167-220">O `Save Changes To Disk With Workspaces` link na demonstração tem o estilo regular.</span><span class="sxs-lookup"><span data-stu-id="e3167-220">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="e3167-221">Adicione o código a seguir na parte inferior do **script. js** usando a guia **fonte rápida** .</span><span class="sxs-lookup"><span data-stu-id="e3167-221">Add the following code to the bottom of **script.js** using the **Quick Source** tab.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="e3167-222">Pressione `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) para salvar a alteração.</span><span class="sxs-lookup"><span data-stu-id="e3167-222">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="e3167-223">Recarregar a página.</span><span class="sxs-lookup"><span data-stu-id="e3167-223">Reload the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e3167-224">O link na página agora está em itálico.</span><span class="sxs-lookup"><span data-stu-id="e3167-224">The link on the page is now italic.</span></span>
    
    > ##### <span data-ttu-id="e3167-225">Figura 11</span><span class="sxs-lookup"><span data-stu-id="e3167-225">Figure 11</span></span>  
    > <span data-ttu-id="e3167-226">O link na página agora está em itálico</span><span class="sxs-lookup"><span data-stu-id="e3167-226">The link on the page is now italic</span></span>  
    > <span data-ttu-id="e3167-227">! [O link na página agora está em itálico] [ImageScriptItalic]</span><span class="sxs-lookup"><span data-stu-id="e3167-227">![The link on the page is now italic][ImageScriptItalic]</span></span>  

## <span data-ttu-id="e3167-228">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="e3167-228">Next steps</span></span>   

<span data-ttu-id="e3167-229">Use o que você aprendeu neste tutorial para configurar espaços de trabalho em seu próprio projeto.</span><span class="sxs-lookup"><span data-stu-id="e3167-229">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->

 <!--  -->



<!-- 
If you have more feedback on these topics or anything else, please use any of the channels below:
*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  
-->

<!-- image links -->  

[ImageGlitchProject]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-workspaces-demo-source.msft.png "Figura 1: um projeto de falha com um nome gerado aleatoriamente"  
<!--[ImageDownloadProjectButton]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-advanced-options-download-project.msft.png "old Figure 2: The Download Project button"  -->  
[ImageDemo]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo.msft.png "Figura 2: a demonstração"  
[ImageConsolePanel]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-console.msft.png "Figura 3: o painel do console"  
[ImageFilesystem]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-sources-FileSystem.msft.png "Figura 4: a guia Filesystem"  
[ImageMapping]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-sources-FileSystem-Folder.msft.png "Figura 5: a guia Filesystem agora mostra um mapeamento entre os arquivos locais e os de rede"  
[ImageStylesFuchsia]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-sources-FileSystem-CSS.msft.png "Figura 6: exibindo estilos. CSS em um editor de texto"  
[ImageStylesGreen]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-Elements-Styles-CSS.msft.png "Figura 7: o indicador verde no qual o arquivo está vinculado"  
[ImageSourcesCakeHTML]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-sources-Page-H1.msft.png "Figura 8: alterando o HTML no painel fontes"  
<!--[ImageElementsCake]: /microsoft-edge/devtools-guide-chromium/media/workspaces-workspaces-demo-change-h1.msft.png "Old Figure 9: Attempting to change HTML from the DOM Tree of the Elements panel"  -->  
[ImageCommandMenuQuickSource]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-Search-show-Quick-Source.msft.png "Figura 9: abrindo a guia fonte rápida usando o menu de comando"  
[ImageOpenFileDialog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-Search-script.msft.png "Figura 10: abrindo script. js usando a caixa de diálogo abrir arquivo"  
[ImageScriptItalic]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-Elements-Styles-Quick-Source-script.msft.png "Figura 11: o link na página agora está em itálico"  

<!-- links -->  

[DevToolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Introdução à exibição e alteração de CSS"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Arquivos de demonstração de espaços de trabalho | Problema"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Conteúdo-CSS: folhas de estilos em cascata | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Introdução à Web | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Executar um servidor HTTP local simples | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introdução a APIs do DOM-Web | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Uma introdução aos mapas de origem | Blog Treehouse"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Porta \ (rede de computador \)-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="e3167-249">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="e3167-249">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e3167-250">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e3167-250">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e3167-252">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e3167-252">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
