---
description: Use a ferramenta Sources para exibir, modificar e depurar JavaScript retornado pelo servidor e inspecionar os recursos que comem a página da Web atual.  Para usar a ferramenta Sources como um ambiente de desenvolvimento, adicione arquivos de origem a um Workspace.
title: Visão geral da ferramenta Fontes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/20/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 6ba6a7615c2d9e2b70975af01edeeb3e10db8e59
ms.sourcegitcommit: 31741a0c331816642ceafd20680bd3206c87c7bf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "11579740"
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
# <a name="sources-tool-overview"></a><span data-ttu-id="c4e7a-105">Visão geral da ferramenta Fontes</span><span class="sxs-lookup"><span data-stu-id="c4e7a-105">Sources tool overview</span></span>  

<span data-ttu-id="c4e7a-106">Use a **ferramenta Sources** para exibir, modificar e depurar código JavaScript front-end e inspecionar os recursos que comem a página da Web atual.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-106">Use the **Sources** tool to view, modify, and debug front-end JavaScript code, and to inspect the resources that make up the current webpage.</span></span>  <span data-ttu-id="c4e7a-107">A **ferramenta Sources** tem três painéis:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-107">The **Sources** tool has three panes:</span></span>  

| <span data-ttu-id="c4e7a-108">Painel</span><span class="sxs-lookup"><span data-stu-id="c4e7a-108">Pane</span></span> | <span data-ttu-id="c4e7a-109">Ações</span><span class="sxs-lookup"><span data-stu-id="c4e7a-109">Actions</span></span> |
|---|---|
| <span data-ttu-id="c4e7a-110">**Painel navegador**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-110">**Navigator** pane</span></span> | <span data-ttu-id="c4e7a-111">Navegue entre os recursos retornados do servidor para construir a página da Web atual.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-111">Navigate among the resources that are returned from the server to construct the current webpage.</span></span>  <span data-ttu-id="c4e7a-112">Selecione arquivos, imagens e outros recursos e veja seus caminhos.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-112">Select files, images, and other resources, and view their paths.</span></span>  <span data-ttu-id="c4e7a-113">Opcionalmente, configurar um Espaço de Trabalho local para salvar alterações diretamente nos arquivos de origem.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-113">Optionally, set up a local Workspace to save changes directly to source files.</span></span> |
| <span data-ttu-id="c4e7a-114">**Painel editor**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-114">**Editor** pane</span></span> | <span data-ttu-id="c4e7a-115">Exibir JavaScript, HTML, CSS e outros arquivos retornados do servidor.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-115">View JavaScript, HTML, CSS, and other files that are returned from the server.</span></span>  <span data-ttu-id="c4e7a-116">Faça edições experimentais em JavaScript ou CSS.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-116">Make experimental edits to JavaScript or CSS.</span></span>  <span data-ttu-id="c4e7a-117">Suas alterações serão preservadas até que você atualize a página ou seja preservada após a atualização da página se você salvar em um arquivo local com Espaços de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-117">Your changes are preserved until you refresh the page, or are preserved after page refresh if you save to a local file with Workspaces.</span></span> <span data-ttu-id="c4e7a-118">Ao usar Espaços de Trabalho ou Substituições, você também pode editar arquivos HTML.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-118">When you use Workspaces or Overrides, you can edit HTML files as well.</span></span> |
| <span data-ttu-id="c4e7a-119">**Painel de depurador**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-119">**Debugger** pane</span></span> | <span data-ttu-id="c4e7a-120">Use o Depurador JavaScript para definir pontos de interrupção, pausar a execução do JavaScript e passar pelo código, incluindo todas as edições feitas, enquanto observa quaisquer expressões JavaScript que você especificar.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-120">Use the JavaScript Debugger to set breakpoints, pause running JavaScript, and step through the code, including any edits you have made, while watching any JavaScript expressions you specify.</span></span>  <span data-ttu-id="c4e7a-121">Assista e altere manualmente os valores das variáveis que estão no escopo da linha de código atual.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-121">Watch and manually change the values of variables that are in-scope for the current line of code.</span></span> |

<span data-ttu-id="c4e7a-122">A figura a seguir mostra o painel **Navegador** realçado com uma caixa vermelha no canto superior esquerdo do DevTools, o painel **Editor** realçado na parte superior direita e o painel **Depurador** realçado na parte inferior.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-122">The following figure shows the **Navigator** pane highlighted with a red box in the upper left corner of DevTools, the **Editor** pane highlighted in the upper right, and the **Debugger** pane highlighted on the bottom.</span></span>  <span data-ttu-id="c4e7a-123">No lado esquerdo, está a parte principal da janela do navegador, mostrando a página da Web renderizada acinzenada porque o depurador é pausado em um ponto de interrupção:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-123">On the far left side is the main part of the browser window, showing the rendered webpage grayed-out because the debugger is paused on a breakpoint:</span></span>

:::image type="complex" source="../media/sources-panes-narrow-layout.msft.png" alt-text="Os painéis da ferramenta Sources, em layout estreito" lightbox="../media/sources-panes-narrow-layout.msft.png":::
   <span data-ttu-id="c4e7a-125">Os painéis da ferramenta Sources, em layout estreito</span><span class="sxs-lookup"><span data-stu-id="c4e7a-125">The panes of the Sources tool, in narrow layout</span></span>  
:::image-end:::  

<span data-ttu-id="c4e7a-126">Quando o DevTools é largo, o painel **Depurador** é colocado à direita e inclui **Escopo** e **Assistir**:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-126">When DevTools is wide, the **Debugger** pane is placed on the right, and includes **Scope** and **Watch**:</span></span>  

:::image type="complex" source="../media/sources-panes-wide-layout.msft.png" alt-text="Navegar, exibir, editar e depurar JavaScript retornado pelo servidor" lightbox="../media/sources-panes-wide-layout.msft.png":::
   <span data-ttu-id="c4e7a-128">Navegar, exibir, editar e depurar JavaScript retornado pelo servidor</span><span class="sxs-lookup"><span data-stu-id="c4e7a-128">Navigate, view, edit, and debug JavaScript returned by the server</span></span>  
:::image-end:::  

<span data-ttu-id="c4e7a-129">Para maximizar o tamanho da ferramenta Sources, desfaça DevTools em uma janela separada e, opcionalmente, mova a janela DevTools para um monitor separado.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-129">To maximize the size of the Sources tool, undock DevTools into a separate window, and optionally move the DevTools window to a separate monitor.</span></span>  <span data-ttu-id="c4e7a-130">Consulte [Alterar Microsoft Edge posicionamento do DevTools (Desfazer, Encaixar para baixo, Doca para a esquerda)][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-130">See [Change Microsoft Edge DevTools placement (Undock, Dock to bottom, Dock to left)][DevToolsCustomizePlacement].</span></span>

<span data-ttu-id="c4e7a-131">Para carregar a página da Web de demonstração de depuração mostrada acima, consulte A abordagem básica para usar um [depurador](#the-basic-approach-to-using-a-debugger), abaixo.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-131">To load the debugging demo webpage that's shown above, see [The basic approach to using a debugger](#the-basic-approach-to-using-a-debugger), below.</span></span>

## <a name="using-the-navigator-pane-to-select-files"></a><span data-ttu-id="c4e7a-132">Usando o painel Navegador para selecionar arquivos</span><span class="sxs-lookup"><span data-stu-id="c4e7a-132">Using the Navigator pane to select files</span></span>

<span data-ttu-id="c4e7a-133">Use o **painel Navegador** (à esquerda) para navegar entre os recursos retornados do servidor para construir a página da Web atual.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-133">Use the **Navigator** pane (on the left) to navigate among the resources that are returned from the server to construct the current webpage.</span></span>  <span data-ttu-id="c4e7a-134">Selecione arquivos, imagens e outros recursos e veja seus caminhos.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-134">Select files, images, and other resources, and view their paths.</span></span>  

:::image type="complex" source="../media/navigator-pane.msft.png" alt-text="O painel Navegador" lightbox="../media/navigator-pane.msft.png":::
   <span data-ttu-id="c4e7a-136">O **painel Navegador**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-136">The **Navigator** pane</span></span>
:::image-end:::  

<span data-ttu-id="c4e7a-137">Para acessar quaisquer guias ocultas do painel Navegador, selecione ![ Mais guias ( Mais ](../media/more-tabs-icon.msft.png) **guias**).</span><span class="sxs-lookup"><span data-stu-id="c4e7a-137">To access any hidden tabs of the Navigator pane, select ![More tabs](../media/more-tabs-icon.msft.png) (**More tabs**).</span></span>

<span data-ttu-id="c4e7a-138">As subseções a seguir abrangem o painel Navegador:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-138">The following subsections cover the Navigator pane:</span></span>
*   [<span data-ttu-id="c4e7a-139">Usando a guia Página para explorar recursos que constroem a página da Web atual</span><span class="sxs-lookup"><span data-stu-id="c4e7a-139">Using the Page tab to explore resources that construct the current webpage</span></span>](#using-the-page-tab-to-explore-resources-that-construct-the-current-webpage)
*   [<span data-ttu-id="c4e7a-140">Usando a guia Sistema de Arquivos para definir um Espaço de Trabalho local</span><span class="sxs-lookup"><span data-stu-id="c4e7a-140">Using the Filesystem tab to define a local Workspace</span></span>](#using-the-filesystem-tab-to-define-a-local-workspace)
*   [<span data-ttu-id="c4e7a-141">Usando a guia Substituições para substituir arquivos de servidor com arquivos locais</span><span class="sxs-lookup"><span data-stu-id="c4e7a-141">Using the Overrides tab to override server files with local files</span></span>](#using-the-overrides-tab-to-override-server-files-with-local-files)
*   [<span data-ttu-id="c4e7a-142">Usando a guia Scripts de conteúdo para Microsoft Edge extensões</span><span class="sxs-lookup"><span data-stu-id="c4e7a-142">Using the Content scripts tab for Microsoft Edge extensions</span></span>](#using-the-content-scripts-tab-for-microsoft-edge-extensions)
*   [<span data-ttu-id="c4e7a-143">Usando a guia Trechos de Código para executar trechos de código JavaScript em qualquer página</span><span class="sxs-lookup"><span data-stu-id="c4e7a-143">Using the Snippets tab to run JavaScript code snippets on any page</span></span>](#using-the-snippets-tab-to-run-javascript-code-snippets-on-any-webpage)
*   [<span data-ttu-id="c4e7a-144">Usando o Menu de Comando para abrir arquivos</span><span class="sxs-lookup"><span data-stu-id="c4e7a-144">Using the Command Menu to open files</span></span>](#using-the-command-menu-to-open-files)

### <a name="using-the-page-tab-to-explore-resources-that-construct-the-current-webpage"></a><span data-ttu-id="c4e7a-145">Usando a guia Página para explorar recursos que constroem a página da Web atual</span><span class="sxs-lookup"><span data-stu-id="c4e7a-145">Using the Page tab to explore resources that construct the current webpage</span></span>

<span data-ttu-id="c4e7a-146">Use a **guia Página** do painel **Navegador** para explorar o sistema de arquivos retornado do servidor para construir a página da Web atual.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-146">Use the **Page** tab of the **Navigator** pane to explore the file system that's returned from the server to construct the current webpage.</span></span>  <span data-ttu-id="c4e7a-147">Selecione um arquivo JavaScript para exibi-lo, editá-lo e depurá-lo.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-147">Select a JavaScript file to view, edit, and debug it.</span></span>  <span data-ttu-id="c4e7a-148">A **guia Página** lista todos os recursos carregados pela página.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-148">The **Page** tab lists all of the resources that the page has loaded.</span></span>

:::image type="complex" source="../media/sources-page-tab.msft.png" alt-text="A guia Página no painel Navegador da ferramenta Sources" lightbox="../media/sources-page-tab.msft.png":::
   <span data-ttu-id="c4e7a-150">A **guia Página** no painel **Navegador** da ferramenta **Sources**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-150">The **Page** tab in the **Navigator** pane of the **Sources** tool</span></span>
:::image-end:::  

<span data-ttu-id="c4e7a-151">Para exibir um arquivo no painel **Editor,** selecione um arquivo **na** guia Página.  Para uma imagem, uma visualização da imagem é exibida.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-151">To display a file in the **Editor** pane, select a file in the **Page** tab.  For an image, a preview of the image is displayed.</span></span>  

<span data-ttu-id="c4e7a-152">Para exibir a URL ou o caminho de um recurso, passe o mouse sobre o recurso.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-152">To display the URL or path for a resource, hover over the resource.</span></span>

<span data-ttu-id="c4e7a-153">Para carregar um arquivo em uma nova guia do navegador ou para exibir outras ações, clique com o botão direito do mouse no nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-153">To load a file into a new tab of the browser, or to display other actions, right-click on the file name.</span></span>
   
#### <a name="icons-in-the-page-tab"></a><span data-ttu-id="c4e7a-154">Ícones na guia Página</span><span class="sxs-lookup"><span data-stu-id="c4e7a-154">Icons in the Page tab</span></span>

<span data-ttu-id="c4e7a-155">A **guia Página** usa os seguintes ícones:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-155">The **Page** tab uses the following icons:</span></span>
*   <span data-ttu-id="c4e7a-156">O **ícone** da janela, juntamente com o rótulo `top` , representa o quadro principal do documento, que é um [quadro HTML][W3CHtml4Frames].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-156">The **window** icon, along with the label `top`, represents the main document frame, which is an [HTML frame][W3CHtml4Frames].</span></span>  
*   <span data-ttu-id="c4e7a-157">O **ícone de** nuvem representa uma [origem][HtmlstandardOrigin].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-157">The **cloud** icon represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="c4e7a-158">O **ícone de** pasta representa um diretório.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-158">The **folder** icon represents a directory.</span></span>
*   <span data-ttu-id="c4e7a-159">O **ícone** da página representa um recurso.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-159">The **page** icon represents a resource.</span></span>  
    
#### <a name="group-files-by-folder-or-as-a-flat-list"></a><span data-ttu-id="c4e7a-160">Arquivos de grupo por pasta ou como uma lista simples</span><span class="sxs-lookup"><span data-stu-id="c4e7a-160">Group files by folder or as a flat list</span></span>

<span data-ttu-id="c4e7a-161">A **guia Página** exibe arquivos ou recursos agrupados por servidor e diretório ou como uma lista simples.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-161">The **Page** tab displays files or resources grouped by server and directory, or as a flat list.</span></span>

<span data-ttu-id="c4e7a-162">Para alterar como os recursos são agrupados:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-162">To change how resources are grouped:</span></span>

1.  <span data-ttu-id="c4e7a-163">Ao lado das guias no painel Navegador (à esquerda), selecione **o botão ...** ( Mais**opções**).</span><span class="sxs-lookup"><span data-stu-id="c4e7a-163">Next to the tabs on the Navigator pane (on the left), select the **...** (**More options**) button.</span></span>  <span data-ttu-id="c4e7a-164">Um menu é exibido.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-164">A menu appears.</span></span>
1.  <span data-ttu-id="c4e7a-165">Selecione ou deslele **a opção Grupo por** pasta.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-165">Select or clear the **Group by folder** option.</span></span>  

### <a name="using-the-filesystem-tab-to-define-a-local-workspace"></a><span data-ttu-id="c4e7a-166">Usando a guia Sistema de Arquivos para definir um Espaço de Trabalho local</span><span class="sxs-lookup"><span data-stu-id="c4e7a-166">Using the Filesystem tab to define a local Workspace</span></span>

<span data-ttu-id="c4e7a-167">Use a guia **Sistema** de Arquivos do painel **Navegador** para adicionar arquivos a um Espaço de Trabalho, para que as alterações feitas no DevTools são salvas no sistema de arquivos local.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-167">Use the **Filesystem** tab of the **Navigator** pane to add files to a Workspace, so that changes you make in DevTools get saved to your local file system.</span></span>

<span data-ttu-id="c4e7a-168">Um arquivo que está em um Espaço de Trabalho é indicado por um ponto verde ao lado do nome do arquivo, em todo o DevTools.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-168">A file that's in a Workspace is indicated by a green dot next to the file name, throughout DevTools.</span></span> 

:::image type="complex" source="../media/sources-filesystem-tab.msft.png" alt-text="A guia Sistema de Arquivos, para um Espaço de Trabalho" lightbox="../media/sources-filesystem-tab.msft.png":::
   <span data-ttu-id="c4e7a-170">A **guia Sistema de** Arquivos, para um Espaço de Trabalho</span><span class="sxs-lookup"><span data-stu-id="c4e7a-170">The **Filesystem** tab, for a Workspace</span></span>
:::image-end:::  

<span data-ttu-id="c4e7a-171">Por padrão, quando você edita um arquivo na ferramenta **Fontes,** suas alterações são descartadas quando você atualize a página da Web.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-171">By default, when you edit a file in the **Sources** tool, your changes are discarded when you refresh the webpage.</span></span>  <span data-ttu-id="c4e7a-172">A **ferramenta Sources** funciona com uma cópia dos recursos front-end retornados pelo servidor Web.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-172">The **Sources** tool works with a copy of the front-end resources that are returned by the web server.</span></span>  <span data-ttu-id="c4e7a-173">Quando você modifica esses arquivos front-end retornados pelo servidor, as alterações não persistem, pois você não alterou os arquivos de origem.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-173">When you modify these front-end files that are returned by the server, the changes don't persist, because you didn't change the source files.</span></span>  <span data-ttu-id="c4e7a-174">Você também precisa aplicar suas edições no código-fonte real e, em seguida, implantar no servidor.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-174">You need to also apply your edits in your actual source code, and then re-deploy to the server.</span></span>

<span data-ttu-id="c4e7a-175">Por outro lado, quando você usa um Workspace, as alterações feitas no código front-end são preservadas quando você atualize a página da Web.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-175">In contrast, when you use a Workspace, changes that you make to your front-end code are preserved when you refresh the webpage.</span></span>  <span data-ttu-id="c4e7a-176">Com um Workspace, quando você edita o código front-end retornado pelo servidor, a ferramenta Sources também aplica suas edições ao código-fonte local.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-176">With a Workspace, when you edit the front-end code that's returned by the server, the Sources tool also applies your edits to your local source code.</span></span>  <span data-ttu-id="c4e7a-177">Em seguida, para que outros usuários vejam suas alterações, você só precisa reimplantar seus arquivos de origem alterados para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-177">Then for other users to see your changes, you only need to redeploy your changed source files to the server.</span></span>

<span data-ttu-id="c4e7a-178">Os espaços de trabalho funcionam bem quando o código JavaScript retornado pelo servidor é o mesmo que o código-fonte JavaScript local.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-178">Workspaces work well when the JavaScript code that's returned by the server is the same as your local JavaScript source code.</span></span>  <span data-ttu-id="c4e7a-179">Os espaços de trabalho não funcionam tão bem quando seu fluxo de trabalho envolve transformações em seu código-fonte, como a minificação ou a [compilação TypeScript.][TypescriptlangMain]</span><span class="sxs-lookup"><span data-stu-id="c4e7a-179">Workspaces don't work as well when your workflow involves transformations on your source code, such as minification or [TypeScript][TypescriptlangMain] compilation.</span></span>  

<span data-ttu-id="c4e7a-180">Para obter mais informações, consulte o tutorial [Editar arquivos com espaços de trabalho][DevtoolsGuideChromiumWorkspacesIndex].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-180">For more information, see the tutorial [Edit files with Workspaces][DevtoolsGuideChromiumWorkspacesIndex].</span></span>

### <a name="using-the-overrides-tab-to-override-server-files-with-local-files"></a><span data-ttu-id="c4e7a-181">Usando a guia Substituições para substituir arquivos de servidor com arquivos locais</span><span class="sxs-lookup"><span data-stu-id="c4e7a-181">Using the Overrides tab to override server files with local files</span></span>

<span data-ttu-id="c4e7a-182">Use a **guia Substituições** do painel **Navegador** para substituir ativos de página (como imagens) por arquivos de uma pasta local.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-182">Use the **Overrides** tab of the **Navigator** pane to override page assets (such as images) with files from a local folder.</span></span>

<span data-ttu-id="c4e7a-183">Os itens nesta guia substituem o que o servidor envia para o navegador, mesmo depois que o servidor envia os ativos.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-183">Items in this tab override what the server sends to the browser, even after the server has sent the assets.</span></span>  

:::image type="complex" source="../media/overrides-tab.msft.png" alt-text="A guia Substituições do painel Navegador" lightbox="../media/overrides-tab.msft.png":::
   <span data-ttu-id="c4e7a-185">A **guia Substituições** do painel **Navegador**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-185">The **Overrides** tab of the **Navigator** pane</span></span>
:::image-end:::  

<span data-ttu-id="c4e7a-186">O **recurso Substituições** é semelhante a Workspaces.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-186">The **Overrides** feature is similar to Workspaces.</span></span>  <span data-ttu-id="c4e7a-187">Use Substituições quando quiser experimentar alterações em uma página da Web e você precisa manter as alterações depois de atualizar a página da Web, mas não se importa em mapear suas alterações no código-fonte da página da Web.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-187">Use Overrides when you want to experiment with changes to a webpage, and you need to keep the changes after you refresh the webpage, but you don't care about mapping your changes to the source code of the webpage.</span></span>  

<span data-ttu-id="c4e7a-188">Um arquivo que substitui um arquivo retornado pelo servidor é indicado por um ponto roxo ao lado do nome do arquivo, em todo o DevTools.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-188">A file that overrides a file that is returned by the server is indicated by a purple dot next to the file name, throughout DevTools.</span></span>

#### <a name="see-also"></a><span data-ttu-id="c4e7a-189">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c4e7a-189">See also</span></span>

*   [<span data-ttu-id="c4e7a-190">Substituir recursos de página da Web com cópias locais usando Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c4e7a-190">Override webpage resources with local copies using Microsoft Edge DevTools</span></span>][DevtoolsJavascriptOverrides]

*   [<span data-ttu-id="c4e7a-191">Mapear código pré-processador para código-fonte</span><span class="sxs-lookup"><span data-stu-id="c4e7a-191">Map preprocessed code to source code</span></span>][DevToolsJavaScriptSourceMaps]

### <a name="using-the-content-scripts-tab-for-microsoft-edge-extensions"></a><span data-ttu-id="c4e7a-192">Usando a guia Scripts de conteúdo para Microsoft Edge extensões</span><span class="sxs-lookup"><span data-stu-id="c4e7a-192">Using the Content scripts tab for Microsoft Edge extensions</span></span>

<span data-ttu-id="c4e7a-193">Use a **guia Scripts de** conteúdo do painel **Navegador** para exibir quaisquer scripts de conteúdo carregados por uma extensão Microsoft Edge que você instalou.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-193">Use the **Content scripts** tab of the **Navigator** pane to view any content scripts that were loaded by a Microsoft Edge extension that you installed.</span></span> 

:::image type="complex" source="../media/content-scripts-tab.msft.png" alt-text="A guia Scripts de conteúdo do painel Navegador" lightbox="../media/content-scripts-tab.msft.png":::
   <span data-ttu-id="c4e7a-195">A **guia Scripts de** conteúdo do painel **Navegador**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-195">The **Content scripts** tab of the **Navigator** pane</span></span>
:::image-end:::  

<span data-ttu-id="c4e7a-196">Quando o depurador entra no código que você não reconhece, talvez você queira marcar esse código como código biblioteca, para evitar entrar nesse código.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-196">When the debugger steps into code that you don't recognize, you might want to mark that code as Library code, to avoid stepping into that code.</span></span>  <span data-ttu-id="c4e7a-197">Consulte [Marcar scripts de conteúdo como código biblioteca][DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-197">See [Mark content scripts as Library code][DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode].</span></span>

#### <a name="see-also"></a><span data-ttu-id="c4e7a-198">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c4e7a-198">See also</span></span>

*   [<span data-ttu-id="c4e7a-199">Scripts de conteúdo</span><span class="sxs-lookup"><span data-stu-id="c4e7a-199">Content scripts</span></span>][MDNContentScripts]
*   [<span data-ttu-id="c4e7a-200">Criar um tutorial para extensão Parte 2</span><span class="sxs-lookup"><span data-stu-id="c4e7a-200">Create an extension tutorial Part 2</span></span>][ExtensionsChromiumGetstartPart2ContentScripts]

### <a name="using-the-snippets-tab-to-run-javascript-code-snippets-on-any-webpage"></a><span data-ttu-id="c4e7a-201">Usando a guia Trechos de Código para executar trechos de código JavaScript em qualquer página da Web</span><span class="sxs-lookup"><span data-stu-id="c4e7a-201">Using the Snippets tab to run JavaScript code snippets on any webpage</span></span>

<span data-ttu-id="c4e7a-202">Use a **guia Trechos** de Código do painel **Navegador** para criar e salvar trechos de código JavaScript, para que você possa executar facilmente esses trechos em qualquer página da Web.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-202">Use the **Snippets** tab of the **Navigator** pane to create and save JavaScript code snippets, so that you can easily run these snippets on any webpage.</span></span>

:::image type="complex" source="../media/snippet.msft.png" alt-text="Um trecho que insere a biblioteca jQuery em uma página da Web" lightbox="../media/snippet.msft.png":::
   <span data-ttu-id="c4e7a-204">Um trecho que insere a biblioteca jQuery em uma página da Web</span><span class="sxs-lookup"><span data-stu-id="c4e7a-204">A Snippet that inserts the jQuery library into a webpage</span></span>  
:::image-end:::  

<span data-ttu-id="c4e7a-205">Por exemplo, suponha que você insira com frequência o seguinte código no **Console**, para inserir a biblioteca jQuery em uma página para que você possa executar comandos jQuery no **Console**:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-205">For example, suppose you frequently enter the following code in the **Console**, to insert the jQuery library into a page so that you can run jQuery commands from the **Console**:</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="c4e7a-206">Em vez disso, você pode salvar esse código em **um trecho de código** e, em seguida, execute-o facilmente sempre que precisar.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-206">Instead, you can save this code in a **Snippet** and then easily run it whenever you need to.</span></span>  <span data-ttu-id="c4e7a-207">Quando você seleciona `Ctrl` + `S` \(Windows/Linux\) ou `Command` + `S` \(macOS\), o DevTools \*\*\*\* salva o trecho em seu sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-207">When you select `Ctrl`+`S` \(Windows/Linux\) or `Command`+`S` \(macOS\), DevTools saves the **Snippet** to your file system.</span></span>  

<span data-ttu-id="c4e7a-208">Há várias maneiras de executar um trecho de código:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-208">There are multiple ways to run a Snippet:</span></span>
*   <span data-ttu-id="c4e7a-209">No painel **Navegador,** selecione a guia **Trechos** de Código e selecione o arquivo de trechos para abri-lo.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-209">In the **Navigator** pane, select the **Snippets** tab, and then select the snippets file to open it.</span></span>  <span data-ttu-id="c4e7a-210">Em seguida, na parte inferior do painel Editor, selecione **Executar** \( ![ O botão Executar ](../media/run-snippet-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="c4e7a-210">Then at the bottom of the Editor pane, select **Run** \(![The Run button](../media/run-snippet-icon.msft.png)\).</span></span>  
*   <span data-ttu-id="c4e7a-211">Quando DevTools tiver foco, selecione `Ctrl` + `P` \(Windows/Linux\) ou `Command` + `P` [][DevToolsCommandMenuIndex]\(macOS\) `!` para abrir o Menu de Comando e digite .</span><span class="sxs-lookup"><span data-stu-id="c4e7a-211">When DevTools has focus, select `Ctrl`+`P` \(Windows/Linux\) or `Command`+`P` \(macOS\) to open the [Command Menu][DevToolsCommandMenuIndex], and then type `!`.</span></span> 

<span data-ttu-id="c4e7a-212">Trechos de código são semelhantes aos indicadores.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-212">Snippets are similar to bookmarklets.</span></span>

#### <a name="see-also"></a><span data-ttu-id="c4e7a-213">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c4e7a-213">See also</span></span>

*   [<span data-ttu-id="c4e7a-214">Executar trechos de código do JavaScript em qualquer página da Web com Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c4e7a-214">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>][DevtoolsGuideChromiumJavascriptSnippets]

### <a name="using-the-command-menu-to-open-files"></a><span data-ttu-id="c4e7a-215">Usando o Menu de Comando para abrir arquivos</span><span class="sxs-lookup"><span data-stu-id="c4e7a-215">Using the Command Menu to open files</span></span>

<span data-ttu-id="c4e7a-216">Para abrir um arquivo, além de usar o painel **Navegador** na ferramenta **Fontes,** você pode usar o Menu de Comando de qualquer lugar no DevTools.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-216">To open a file, in addition to using the **Navigator** pane within the **Sources** tool, you can use the Command Menu from anywhere within DevTools.</span></span>

*   <span data-ttu-id="c4e7a-217">Em qualquer lugar no DevTools, selecione `Ctrl` + `P` em Windows/Linux `Command` + `P` ou no macOS.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-217">From anywhere in DevTools, select `Ctrl`+`P` on Windows/Linux or `Command`+`P` on macOS.</span></span>  <span data-ttu-id="c4e7a-218">O Menu de Comando é exibido e lista todos os recursos que estão nas guias do painel **Navegador** da **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-218">The Command Menu appears, and lists all the resources that are in the tabs of the **Navigator** pane of the **Sources** tool.</span></span>  
*   <span data-ttu-id="c4e7a-219">Ou, ao lado das guias do painel **Navegador** na ferramenta **Fontes,** selecione o **botão ...** (**Mais**opções ) e selecione **Abrir Arquivo**.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-219">Or, next to the tabs of the **Navigator** pane in the **Sources** tool, select the **...** (**More options**) button, and then select **Open File**.</span></span>  

<span data-ttu-id="c4e7a-220">Para exibir e escolher de uma lista de todos os arquivos .js, digite `.js` .</span><span class="sxs-lookup"><span data-stu-id="c4e7a-220">To display and pick from a list of all .js files, type `.js`.</span></span>

:::image type="complex" source="../media/sources-command-menu-to-open-file.msft.png" alt-text="Abrir um arquivo usando o Menu de Comando" lightbox="../media/sources-command-menu-to-open-file.msft.png":::
   <span data-ttu-id="c4e7a-222">Abrir um arquivo usando o Menu de Comando</span><span class="sxs-lookup"><span data-stu-id="c4e7a-222">Opening a file by using the Command Menu</span></span>
:::image-end:::

<span data-ttu-id="c4e7a-223">Se você digitar `?` , o Menu de Comando mostrará vários comandos, incluindo **... Abrir arquivo**.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-223">If you type `?`, the Command Menu shows several commands, including **... Open file**.</span></span>  <span data-ttu-id="c4e7a-224">Se você selecionar `Backspace` para limpar o Menu de Comando, uma lista de arquivos será mostrada.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-224">If you select `Backspace` to clear the Command Menu, a list of files is shown.</span></span>

<span data-ttu-id="c4e7a-225">Para obter mais informações, [consulte Executar comandos com o menu de comando Microsoft Edge DevTools][DevToolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-225">For more information, see [Run commands with the Microsoft Edge DevTools Command Menu][DevToolsCommandMenuIndex].</span></span>

## <a name="using-the-editor-pane-to-view-or-edit-files"></a><span data-ttu-id="c4e7a-226">Usando o painel Editor para exibir ou editar arquivos</span><span class="sxs-lookup"><span data-stu-id="c4e7a-226">Using the Editor pane to view or edit files</span></span>

<span data-ttu-id="c4e7a-227">Use o **painel Editor** para exibir os arquivos front-end retornados do servidor para compor a página da Web atual, incluindo JavaScript, HTML, CSS e arquivos de imagem.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-227">Use the **Editor** pane to view the front-end files that are returned from the server to compose the current webpage, including JavaScript, HTML, CSS, and image files.</span></span>  <span data-ttu-id="c4e7a-228">Quando você edita os arquivos front-end no **painel Editor,** o DevTools atualiza a página da Web para executar o código modificado.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-228">When you edit the front-end files in the **Editor** pane, DevTools updates the webpage to run the modified code.</span></span>  

:::image type="complex" source="../media/editor-pane.msft.png" alt-text="O painel Editor na ferramenta Fontes" lightbox="../media/editor-pane.msft.png":::
   <span data-ttu-id="c4e7a-230">O **painel Editor** na ferramenta **Fontes**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-230">The **Editor** pane in the **Sources** tool</span></span>  
:::image-end:::

<span data-ttu-id="c4e7a-231">O **painel Editor** tem o seguinte nível de suporte para vários tipos de arquivo:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-231">The **Editor** pane has the following level of support for various file types:</span></span>

| <span data-ttu-id="c4e7a-232">Tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="c4e7a-232">File Type</span></span> | <span data-ttu-id="c4e7a-233">Ações com suporte</span><span class="sxs-lookup"><span data-stu-id="c4e7a-233">Supported Actions</span></span> |
|---|---|
| <span data-ttu-id="c4e7a-234">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c4e7a-234">JavaScript</span></span> | <span data-ttu-id="c4e7a-235">Exibir, editar e depurar.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-235">View, edit, and debug.</span></span> |
| <span data-ttu-id="c4e7a-236">CSS</span><span class="sxs-lookup"><span data-stu-id="c4e7a-236">CSS</span></span> | <span data-ttu-id="c4e7a-237">Exibir e editar.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-237">View and edit.</span></span> |
| <span data-ttu-id="c4e7a-238">HTML</span><span class="sxs-lookup"><span data-stu-id="c4e7a-238">HTML</span></span> | <span data-ttu-id="c4e7a-239">Exibir e editar.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-239">View and edit.</span></span> |
| <span data-ttu-id="c4e7a-240">Images</span><span class="sxs-lookup"><span data-stu-id="c4e7a-240">Images</span></span> | <span data-ttu-id="c4e7a-241">Exibir.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-241">View.</span></span> |

<span data-ttu-id="c4e7a-242">Por padrão, as edições são descartadas quando você atualize a página da Web.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-242">By default, edits are discarded when you refresh the webpage.</span></span>  <span data-ttu-id="c4e7a-243">Para obter informações sobre como salvar as alterações no sistema de arquivos, consulte [Using the Filesystem tab to define a local Workspace](#using-the-filesystem-tab-to-define-a-local-workspace), above.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-243">For information about how to save the changes to your file system, see [Using the Filesystem tab to define a local Workspace](#using-the-filesystem-tab-to-define-a-local-workspace), above.</span></span>

<span data-ttu-id="c4e7a-244">As subseções a seguir abrangem o painel Editor:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-244">The following subsections cover the Editor pane:</span></span>
*   [<span data-ttu-id="c4e7a-245">Editando um arquivo JavaScript</span><span class="sxs-lookup"><span data-stu-id="c4e7a-245">Editing a JavaScript file</span></span>](#editing-a-javascript-file)
*   [<span data-ttu-id="c4e7a-246">Reformatar um arquivo JavaScript minificado com impressão bastante impressa</span><span class="sxs-lookup"><span data-stu-id="c4e7a-246">Reformatting a minified JavaScript file with pretty-print</span></span>](#reformatting-a-minified-javascript-file-with-pretty-print)
*   [<span data-ttu-id="c4e7a-247">Mapeamento de código minificado para seu código-fonte para mostrar código acessível</span><span class="sxs-lookup"><span data-stu-id="c4e7a-247">Mapping minified code to your source code to show readable code</span></span>](#mapping-minified-code-to-your-source-code-to-show-readable-code)
*   [<span data-ttu-id="c4e7a-248">Transformações do código-fonte para o código front-end compilado</span><span class="sxs-lookup"><span data-stu-id="c4e7a-248">Transformations from source code to compiled front-end code</span></span>](#transformations-from-source-code-to-compiled-front-end-code)
*   [<span data-ttu-id="c4e7a-249">Editando um arquivo CSS</span><span class="sxs-lookup"><span data-stu-id="c4e7a-249">Editing a CSS file</span></span>](#editing-a-css-file)
*   [<span data-ttu-id="c4e7a-250">Editar um arquivo HTML</span><span class="sxs-lookup"><span data-stu-id="c4e7a-250">Editing an HTML file</span></span>](#editing-an-html-file)
*   [<span data-ttu-id="c4e7a-251">Indo para um número de linha ou função</span><span class="sxs-lookup"><span data-stu-id="c4e7a-251">Going to a line number or function</span></span>](#going-to-a-line-number-or-function)
*   [<span data-ttu-id="c4e7a-252">Exibindo arquivos de origem ao usar uma ferramenta diferente</span><span class="sxs-lookup"><span data-stu-id="c4e7a-252">Displaying source files when using a different tool</span></span>](#displaying-source-files-when-using-a-different-tool)

### <a name="editing-a-javascript-file"></a><span data-ttu-id="c4e7a-253">Editando um arquivo JavaScript</span><span class="sxs-lookup"><span data-stu-id="c4e7a-253">Editing a JavaScript file</span></span>

<span data-ttu-id="c4e7a-254">Para editar um arquivo JavaScript no DevTools, use o **painel Editor,** na **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-254">To edit a JavaScript file in DevTools, use the **Editor** pane, within the **Sources** tool.</span></span>

:::image type="complex" source="../media/editing-js-in-editor-pane.msft.png" alt-text="Editando JavaScript no painel Editor" lightbox="../media/editing-js-in-editor-pane.msft.png":::
   <span data-ttu-id="c4e7a-256">Editando JavaScript no **painel Editor**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-256">Editing JavaScript in the **Editor** pane</span></span>  
:::image-end:::

<span data-ttu-id="c4e7a-257">Para carregar um arquivo no painel Editor, use a guia **Página** no painel **Navegador** (à esquerda).</span><span class="sxs-lookup"><span data-stu-id="c4e7a-257">To load a file into the Editor pane, use the **Page** tab in the **Navigator** pane (on the left).</span></span>  <span data-ttu-id="c4e7a-258">Ou use o **Menu de**Comando , da seguinte forma: no canto superior direito do DevTools, selecione Personalizar e controlar **DevTools** \( \) e selecione `...` Abrir **Arquivo**.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-258">Or use the **Command Menu**, as follows: in the upper right of DevTools, select **Customize and control DevTools** \(`...`\) and then select **Open File**.</span></span>

#### <a name="save-and-undo"></a><span data-ttu-id="c4e7a-259">Salvar e Desfazer</span><span class="sxs-lookup"><span data-stu-id="c4e7a-259">Save and Undo</span></span>

<span data-ttu-id="c4e7a-260">Para que as alterações do JavaScript entre em vigor, selecione `Ctrl` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="c4e7a-260">For JavaScript changes to take effect, select `Ctrl`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\).</span></span>  

<span data-ttu-id="c4e7a-261">Se você alterar um arquivo, um asterisco será exibido ao lado do nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-261">If you change a file, an asterisk appears next to the file name.</span></span>
*   <span data-ttu-id="c4e7a-262">Para salvar alterações, selecione `Ctrl` + `S` em Windows/Linux `Command` + `S` ou no macOS.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-262">To save changes, select `Ctrl`+`S` on Windows/Linux or `Command`+`S` on macOS.</span></span>
*   <span data-ttu-id="c4e7a-263">Para desfazer uma alteração, selecione `Ctrl` + `Z` em Windows/Linux ou `Command` + `Z` no macOS.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-263">To undo a change, select `Ctrl`+`Z` on Windows/Linux or `Command`+`Z` on macOS.</span></span>

<span data-ttu-id="c4e7a-264">Por padrão, suas edições são descartadas quando você atualize a página da Web.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-264">By default, your edits are discarded when you refresh the webpage.</span></span>  <span data-ttu-id="c4e7a-265">Para obter mais informações sobre como salvar as alterações no sistema de arquivos local, consulte [Edit files with Workspaces][DevtoolsGuideChromiumWorkspacesIndex].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-265">For more information about how to save the changes in your local file system, see [Edit files with Workspaces][DevtoolsGuideChromiumWorkspacesIndex].</span></span>

#### <a name="find-and-replace"></a><span data-ttu-id="c4e7a-266">Encontrar e substituir</span><span class="sxs-lookup"><span data-stu-id="c4e7a-266">Find and Replace</span></span>

<span data-ttu-id="c4e7a-267">Para encontrar texto no arquivo atual, selecione o painel **Editor** para dar foco a ele e selecione em `Ctrl` + `F` Windows/Linux ou `Command` + `F` no macOS.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-267">To find text in the current file, select the **Editor** pane to give it focus, and then select `Ctrl`+`F` on Windows/Linux, or `Command`+`F` on macOS.</span></span>  

:::image type="complex" source="../media/find-replace.msft.png" alt-text="Encontrar e substituir, no painel Editor da ferramenta Fontes" lightbox="../media/find-replace.msft.png":::
   <span data-ttu-id="c4e7a-269">**Encontrar** e **substituir**, no **painel Editor** da **ferramenta Sources**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-269">**Find** and **Replace**, in the **Editor** pane of the **Sources** tool</span></span>
:::image-end:::

<span data-ttu-id="c4e7a-270">Para encontrar e substituir texto, selecione o botão **Substituir** (**A-\>B**) à esquerda da caixa **de** texto Encontrar.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-270">To find and replace text, select the **Replace** (**A-\>B**) button to the left of the **Find** textbox.</span></span> <span data-ttu-id="c4e7a-271">O **botão Substituir** (**A-\>B**) é exibido ao exibir um arquivo editável.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-271">The **Replace** (**A-\>B**) button appears when viewing an editable file.</span></span>

#### <a name="showing-the-changes-you-made"></a><span data-ttu-id="c4e7a-272">Mostrando as alterações feitas</span><span class="sxs-lookup"><span data-stu-id="c4e7a-272">Showing the changes you made</span></span>

<span data-ttu-id="c4e7a-273">Para revisar as alterações feitas em um arquivo, clique com o botão direito do mouse no painel **Editor** e selecione **Modificações Locais.**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-273">To review the changes you made to a file, right-click in the **Editor** pane and then select **Local Modifications**.</span></span>

<span data-ttu-id="c4e7a-274">A **Gaveta** é aberta na parte inferior do DevTools, mostrando suas alterações na **guia Alterações.**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-274">The **Drawer** opens at the bottom of DevTools, showing your changes within the **Changes** tab.</span></span>

:::image type="complex" source="../media/local-modifications.msft.png" alt-text="Mostrando modificações locais, na guia Alterações da Gaveta" lightbox="../media/local-modifications.msft.png":::
   <span data-ttu-id="c4e7a-276">Mostrando **modificações locais**, na guia **Alterações** da **Gaveta**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-276">Showing **Local Modifications**, in the **Changes** tab of the **Drawer**</span></span>
:::image-end:::

#### <a name="changes-inside-a-function-take-effect"></a><span data-ttu-id="c4e7a-277">Alterações dentro de uma função entrarão em vigor</span><span class="sxs-lookup"><span data-stu-id="c4e7a-277">Changes inside a function take effect</span></span>

<span data-ttu-id="c4e7a-278">O DevTools não executará um script de novo, portanto, as únicas alterações do JavaScript que têm efeito são as alterações feitas em funções.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-278">DevTools doesn't re-run a script, so the only JavaScript changes that take effect are changes that you make within functions.</span></span>  <span data-ttu-id="c4e7a-279">Por exemplo, na figura a seguir, adicionamos o seguinte código ao JavaScript retornado pelo servidor:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-279">For example, in the following figure, we added the following code to the JavaScript that is returned by the server:</span></span>  
*   <span data-ttu-id="c4e7a-280">Adicionamos a instrução `console.log('A')` fora de qualquer função.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-280">We added the statement `console.log('A')` outside of any function.</span></span>  
*   <span data-ttu-id="c4e7a-281">Adicionamos a instrução `console.log('B')` dentro de uma `onClick` função.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-281">We added the statement `console.log('B')` inside an `onClick` function.</span></span>  
<span data-ttu-id="c4e7a-282">Salvamos as alterações, os números inseridos no formulário e selecionamos o botão de formulário para enviar o formulário.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-282">We then saved the changes, entered numbers into the form, and then selected the form button to send the form.</span></span>  

<span data-ttu-id="c4e7a-283">Depois de enviar o formulário, , que está no escopo global, não é executado, mas , dentro de uma função, é executado, saída `console.log('A')` `console.log('B')` para o `onClick` `B` Console:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-283">After submitting the form, `console.log('A')`, which is at global scope, doesn't run, but `console.log('B')`, inside an `onClick` function, does run, outputting `B` to the Console:</span></span>

:::image type="complex" source="../media/edit-js.msft.png" alt-text="JavaScript de escopo global não é executado de acordo com o escopo global" lightbox="../media/edit-js.msft.png":::
   <span data-ttu-id="c4e7a-285">JavaScript de escopo global não é executado de acordo com o escopo global</span><span class="sxs-lookup"><span data-stu-id="c4e7a-285">Global-scope JavaScript is not re-run</span></span>  
:::image-end:::

### <a name="reformatting-a-minified-javascript-file-with-pretty-print"></a><span data-ttu-id="c4e7a-286">Reformatar um arquivo JavaScript minificado com impressão bastante impressa</span><span class="sxs-lookup"><span data-stu-id="c4e7a-286">Reformatting a minified JavaScript file with pretty-print</span></span>

<span data-ttu-id="c4e7a-287">Para usar a impressão bastante impressa para reformatar um \*\*\*\* arquivo para torná-lo acessível, selecione o botão De impressão bonito \( Format \), que é mostrado como chaves, na parte inferior do ![ painel ](../media/format-icon.msft.png) Editor.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-287">To use pretty-print to reformat a file to make it readable, select the **Pretty print** button \(![Format](../media/format-icon.msft.png)\), which is shown as braces, at the bottom of the Editor pane.</span></span>  <span data-ttu-id="c4e7a-288">Ou, se um **botão Pretty-print** aparecer na parte superior do painel Editor, você poderá selecionar esse botão.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-288">Or, if a **Pretty-print** button appears at the top of the Editor pane, you can select that button.</span></span>

:::image type="complex" source="../media/minified.msft.png" alt-text="O botão de impressão Pretty" lightbox="../media/minified.msft.png":::
   <span data-ttu-id="c4e7a-290">O **botão de impressão** Pretty</span><span class="sxs-lookup"><span data-stu-id="c4e7a-290">The **Pretty print** button</span></span>  
:::image-end:::  

<span data-ttu-id="c4e7a-291">O arquivo reformatado aparece em uma nova guia, com `:formatted` anexado ao nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-291">The reformatted file appears in a new tab, with `:formatted` appended to the file name.</span></span>  <span data-ttu-id="c4e7a-292">O código reformatado é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-292">The reformatted code is read-only.</span></span>  

:::image type="complex" source="../media/pretty-printed.msft.png" alt-text="Um arquivo JavaScript bastante impresso (reformatado)" lightbox="../media/pretty-printed.msft.png":::
   <span data-ttu-id="c4e7a-294">Um arquivo JavaScript bastante impresso (reformatado)</span><span class="sxs-lookup"><span data-stu-id="c4e7a-294">A pretty-printed (reformatted) JavaScript file</span></span>  
:::image-end:::  

<span data-ttu-id="c4e7a-295">Para fazer o arquivo reformatado rolar para o código selecionado no arquivo minificado:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-295">To make the reformatted file scroll to the code that you select in the minified file:</span></span> 
1.   <span data-ttu-id="c4e7a-296">Se a guia arquivo reformatado estiver aberta, feche-a.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-296">If the reformatted file tab is open, close it.</span></span>  
1.   <span data-ttu-id="c4e7a-297">Selecione algum código no arquivo minificado no painel Editor.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-297">Select some code in the minified file in the Editor pane.</span></span>
1.   <span data-ttu-id="c4e7a-298">Selecione o **botão De impressão** bonito.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-298">Select the **Pretty print** button.</span></span>
<span data-ttu-id="c4e7a-299">O código formatado aparece em uma nova guia, rolada para o código selecionado.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-299">The formatted code appears in a new tab, scrolled to the code that you selected.</span></span>

<span data-ttu-id="c4e7a-300">Para obter mais informações, [consulte Reformat a minified JavaScript file with pretty-print][DevToolsJavaScriptReferenceReformat].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-300">For more information, see [Reformat a minified JavaScript file with pretty-print][DevToolsJavaScriptReferenceReformat].</span></span>  

### <a name="mapping-minified-code-to-your-source-code-to-show-readable-code"></a><span data-ttu-id="c4e7a-301">Mapeamento de código minificado para seu código-fonte para mostrar código acessível</span><span class="sxs-lookup"><span data-stu-id="c4e7a-301">Mapping minified code to your source code to show readable code</span></span>

<span data-ttu-id="c4e7a-302">Mapas de origem de pré-processadores fazem com que o DevTools carregue seus arquivos de origem JavaScript originais, além de seus arquivos JavaScript minificados e transformados que são retornados pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-302">Source maps from preprocessors cause DevTools to load your original JavaScript source files in addition to your minified, transformed JavaScript files that are returned by the server.</span></span>  <span data-ttu-id="c4e7a-303">Em seguida, você exibirá seus arquivos de origem originais enquanto definir pontos de interrupção e passar o código.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-303">You then view your original source files while you set breakpoints and step through code.</span></span>  <span data-ttu-id="c4e7a-304">Enquanto isso, Microsoft Edge está executando seu código minificado.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-304">Meanwhile, Microsoft Edge is actually running your minified code.</span></span>  

<span data-ttu-id="c4e7a-305">No painel **Editor,** se você clicar com o botão direito do mouse em um arquivo JavaScript e, em seguida, selecionar Adicionar mapa de origem **,** uma caixa pop-up será exibida, com uma caixa de texto **URL** de mapa de origem e um **botão Adicionar.**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-305">In the **Editor** pane, if you right-click a JavaScript file and then select **Add source map**, a popup box appears, with a **Source map URL** textbox and an **Add** button.</span></span>

<span data-ttu-id="c4e7a-306">A abordagem de mapeamento de origem mantém seu código front-end acessível e depurável mesmo depois de combiná-lo, minificá-lo ou compilá-lo.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-306">The source-mapping approach keeps your front-end code human-readable and debuggable even after you combine, minify, or compile it.</span></span>
<span data-ttu-id="c4e7a-307">Para obter mais informações, consulte [Map preprocessado code to source code][DevToolsJavaScriptSourceMaps].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-307">For more information, see [Map preprocessed code to source code][DevToolsJavaScriptSourceMaps].</span></span>

### <a name="transformations-from-source-code-to-compiled-front-end-code"></a><span data-ttu-id="c4e7a-308">Transformações do código-fonte para o código front-end compilado</span><span class="sxs-lookup"><span data-stu-id="c4e7a-308">Transformations from source code to compiled front-end code</span></span>

<span data-ttu-id="c4e7a-309">Se você usar uma estrutura que transforme seus arquivos JavaScript, como React, sua fonte local JavaScript pode ser diferente do JavaScript front-end retornado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-309">If you use a framework that transforms your JavaScript files, such as React, your local source JavaScript might be different than the front-end JavaScript that's returned by the server.</span></span>  <span data-ttu-id="c4e7a-310">Não há suporte para espaços de trabalho nesse cenário, mas há suporte para mapeamento de código-fonte nesse cenário.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-310">Workspaces aren't supported in this scenario, but source code mapping is supported in this scenario.</span></span>  

<span data-ttu-id="c4e7a-311">Em um ambiente de desenvolvimento, seu servidor pode incluir seus mapas de origem e seus arquivos originais `.ts` `.jsx` ou React.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-311">In a development environment, your server might include your source maps and your original `.ts` or `.jsx` files for React.</span></span>  <span data-ttu-id="c4e7a-312">A **ferramenta Sources** exibe esses arquivos, mas não permite que você edite esses arquivos.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-312">The **Sources** tool displays these files, but doesn't allow you to edit these files.</span></span>  <span data-ttu-id="c4e7a-313">Quando você definir pontos de interrupção e usar o depurador, o DevTools exibe seus arquivos originais ou, na verdade, passo a passo pela versão minificada de seus `.ts` `.jsx` arquivos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-313">When you set breakpoints and use the debugger, DevTools displays your original `.ts` or `.jsx` files, but actually steps-through the minified version of your JavaScript files.</span></span>

<span data-ttu-id="c4e7a-314">Nesse cenário, a **ferramenta Sources** é útil para inspecionar e examinar o JavaScript de front-end transformado que é retornado do servidor.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-314">In this scenario, the **Sources** tool is useful for inspecting and stepping-through the transformed, front-end JavaScript that's returned from the server.</span></span>  <span data-ttu-id="c4e7a-315">Use o depurador para definir expressões de Watch e use o Console para inserir expressões JavaScript para manipular dados que estão no escopo.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-315">Use the debugger to define Watch expressions, and use the Console to enter JavaScript expressions to manipulate data that's in-scope.</span></span>

### <a name="editing-a-css-file"></a><span data-ttu-id="c4e7a-316">Editando um arquivo CSS</span><span class="sxs-lookup"><span data-stu-id="c4e7a-316">Editing a CSS file</span></span>

<span data-ttu-id="c4e7a-317">Há duas maneiras de editar CSS no DevTools:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-317">There are two ways to edit CSS in DevTools:</span></span>
*   <span data-ttu-id="c4e7a-318">Na ferramenta **Elementos,** você trabalha com uma configuração CSS por vez, por meio de controles de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-318">In the **Elements** tool, you work with one CSS setting at a time, through user interface controls.</span></span>  <span data-ttu-id="c4e7a-319">Essa abordagem é recomendada na maioria dos casos.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-319">This approach is recommended in most cases.</span></span>  <span data-ttu-id="c4e7a-320">Para obter mais informações, [consulte Edit CSS font styles and settings in the Styles pane][DevToolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-320">For more information, see [Edit CSS font styles and settings in the Styles pane][DevToolsInspectStylesEditFonts].</span></span>
*   <span data-ttu-id="c4e7a-321">Na ferramenta **Fontes,** você usa um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-321">In the **Sources** tool, you use a text editor.</span></span>

<span data-ttu-id="c4e7a-322">A ferramenta Sources dá suporte à edição direta de um arquivo CSS.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-322">The Sources tool supports directly editing a CSS file.</span></span>  <span data-ttu-id="c4e7a-323">Por exemplo, se você editar o arquivo CSS do tutorial Editar arquivos com [espaços][DevtoolsGuideChromiumWorkspacesIndex] de trabalho para corresponder à regra de estilo abaixo, o elemento no canto superior esquerdo da página da Web renderizada muda `H1` para verde:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-323">For example, if you edit the CSS file from the tutorial [Edit files with Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to match the style rule below, the `H1` element in the upper left of the rendered webpage changes to green:</span></span>

```css
h1 {
  color: green;
}  
```

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Editar CSS no painel Editor para alterar a cor do texto do título H1 para verde" lightbox="../media/edit-css.msft.png":::
   <span data-ttu-id="c4e7a-325">Editar CSS no **painel Editor** para alterar a cor do texto do título `H1` para verde</span><span class="sxs-lookup"><span data-stu-id="c4e7a-325">Edit CSS in the **Editor** pane to change the text color of the `H1` heading to green</span></span>  
:::image-end:::  

<span data-ttu-id="c4e7a-326">As alterações CSS vigoram imediatamente; você não precisa salvar manualmente as alterações.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-326">CSS changes take effect immediately; you don't need to manually save the changes.</span></span>

#### <a name="see-also"></a><span data-ttu-id="c4e7a-327">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c4e7a-327">See also</span></span>

*   [<span data-ttu-id="c4e7a-328">Editar estilos de fonte CSS e configurações no painel Estilos</span><span class="sxs-lookup"><span data-stu-id="c4e7a-328">Edit CSS font styles and settings in the Styles pane</span></span>][DevToolsInspectStylesEditFonts]

*   <span data-ttu-id="c4e7a-329">[DevTools para iniciantes: Introdução ao CSS][DevToolsBeginnersCss] - tutorial</span><span class="sxs-lookup"><span data-stu-id="c4e7a-329">[DevTools for beginners: Get started with CSS][DevToolsBeginnersCss] - tutorial</span></span>

### <a name="editing-an-html-file"></a><span data-ttu-id="c4e7a-330">Editar um arquivo HTML</span><span class="sxs-lookup"><span data-stu-id="c4e7a-330">Editing an HTML file</span></span>

<span data-ttu-id="c4e7a-331">Há duas maneiras de editar HTML no DevTools:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-331">There are two ways to edit HTML in DevTools:</span></span>  
*   <span data-ttu-id="c4e7a-332">Na ferramenta **Elementos,** você trabalha com um elemento HTML por vez, por meio de controles de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-332">In the **Elements** tool, you work with one HTML element at a time, through user interface controls.</span></span>  
*   <span data-ttu-id="c4e7a-333">Na ferramenta **Fontes,** você usa um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-333">In the **Sources** tool, you use a text editor.</span></span>  

:::image type="complex" source="../media/sources-html-editor.msft.png" alt-text="O editor HTML da ferramenta Sources" lightbox="../media/sources-html-editor.msft.png":::
   <span data-ttu-id="c4e7a-335">O editor HTML da **ferramenta Sources**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-335">The HTML editor of the **Sources** tool</span></span>
:::image-end:::  

<span data-ttu-id="c4e7a-336">Ao contrário de um arquivo JavaScript ou CSS, um arquivo HTML retornado pelo servidor Web não pode ser editado diretamente na ferramenta Sources.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-336">Unlike a JavaScript or CSS file, an HTML file that is returned by the web server cannot be directly edited in the Sources tool.</span></span>  <span data-ttu-id="c4e7a-337">Para editar um arquivo HTML usando o Editor da ferramenta Fontes, o arquivo HTML deve estar em um Espaço de Trabalho ou na guia **Substituições.**  Consulte estas subseções do artigo atual:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-337">To edit an HTML file using the Editor of the Sources tool, the HTML file must be in a Workspace or on the **Overrides** tab.  See these subsections of the current article:</span></span>
*   [<span data-ttu-id="c4e7a-338">Usando a guia Sistema de Arquivos para definir um Espaço de Trabalho local</span><span class="sxs-lookup"><span data-stu-id="c4e7a-338">Using the Filesystem tab to define a local Workspace</span></span>](#using-the-filesystem-tab-to-define-a-local-workspace)
*   [<span data-ttu-id="c4e7a-339">Usando a guia Substituições para substituir arquivos de servidor com arquivos locais</span><span class="sxs-lookup"><span data-stu-id="c4e7a-339">Using the Overrides tab to override server files with local files</span></span>](#using-the-overrides-tab-to-override-server-files-with-local-files)
    
<span data-ttu-id="c4e7a-340">Para salvar alterações, selecione `Ctrl` + `S` em Windows/Linux `Command` + `S` ou no macOS.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-340">To save changes, select `Ctrl`+`S` on Windows/Linux or `Command`+`S` on macOS.</span></span>  <span data-ttu-id="c4e7a-341">Um arquivo editado é marcado por um asterisco.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-341">An edited file is marked by an asterisk.</span></span>  

<span data-ttu-id="c4e7a-342">Para encontrar texto, selecione `Ctrl` + `F` em Windows/Linux ou `Command` + `F` no macOS.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-342">To find text, select `Ctrl`+`F` on Windows/Linux or `Command`+`F` on macOS.</span></span>

<span data-ttu-id="c4e7a-343">Para desfazer uma edição, selecione `Ctrl` + `Z` em Windows/Linux `Command` + `Z` ou no macOS.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-343">To undo an edit, select `Ctrl`+`Z` on Windows/Linux or `Command`+`Z` on macOS.</span></span>

<span data-ttu-id="c4e7a-344">Para exibir outros comandos durante a edição de um arquivo HTML, no painel Editor, clique com o botão direito do mouse no arquivo HTML.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-344">To view other commands while editing an HTML file, in the Editor pane, right-click the HTML file.</span></span>

<span data-ttu-id="c4e7a-345">Você também pode editar HTML usando um editor HTML, em vez de DevTools.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-345">You can also edit HTML by using an HTML editor, rather than DevTools.</span></span>  <span data-ttu-id="c4e7a-346">Por exemplo, o artigo [DevTools para iniciantes:][DevToolsBeginnersHtml] Começar com HTML e o DOM usa um site que habilita a edição HTML na página da Web.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-346">For example, the article [DevTools for beginners: Get started with HTML and the DOM][DevToolsBeginnersHtml] uses a website that enables HTML editing within the webpage.</span></span>

### <a name="going-to-a-line-number-or-function"></a><span data-ttu-id="c4e7a-347">Indo para um número de linha ou função</span><span class="sxs-lookup"><span data-stu-id="c4e7a-347">Going to a line number or function</span></span>

<span data-ttu-id="c4e7a-348">Para ir para um número de linha ou símbolo (como um nome de função) no arquivo que está aberto no painel Editor, você pode usar o Menu de Comando, em vez de rolar pelo arquivo.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-348">To go to a line number or symbol (such as a function name) in the file which is open in the Editor pane, you can use the Command Menu, rather than scrolling through the file.</span></span>

1.   <span data-ttu-id="c4e7a-349">No painel **Navegador,** selecione as releitos (...) (**Mais opções**) e selecione Abrir **Arquivo**.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-349">In the **Navigator** pane, select the ellipses (...) (**More options**), and then select **Open File**.</span></span>  <span data-ttu-id="c4e7a-350">O Menu de Comando é exibido.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-350">The Command Menu appears.</span></span>  
1.   <span data-ttu-id="c4e7a-351">Digite um dos seguintes caracteres:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-351">Type one of the following characters:</span></span>  

| <span data-ttu-id="c4e7a-352">Character</span><span class="sxs-lookup"><span data-stu-id="c4e7a-352">Character</span></span> | <span data-ttu-id="c4e7a-353">Nome do comando</span><span class="sxs-lookup"><span data-stu-id="c4e7a-353">Command name</span></span> | <span data-ttu-id="c4e7a-354">Finalidade</span><span class="sxs-lookup"><span data-stu-id="c4e7a-354">Purpose</span></span> |
|---|---|---|
| <span data-ttu-id="c4e7a-355">\:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-355">\:</span></span> | **<span data-ttu-id="c4e7a-356">Ir para a linha</span><span class="sxs-lookup"><span data-stu-id="c4e7a-356">Go to line</span></span>** | <span data-ttu-id="c4e7a-357">Vá para um número de linha.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-357">Go to a line number.</span></span> |
| \@ | **<span data-ttu-id="c4e7a-358">Ir para o símbolo</span><span class="sxs-lookup"><span data-stu-id="c4e7a-358">Go to symbol</span></span>** | <span data-ttu-id="c4e7a-359">Vá para uma função.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-359">Go to a function.</span></span>  <span data-ttu-id="c4e7a-360">Quando você digita , o Menu de Comando lista as funções encontradas no arquivo JavaScript que está `@` aberto no painel Editor.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-360">When you type `@`, the Command Menu lists the functions that are found in the JavaScript file which is open in the Editor pane.</span></span> |
   
<span data-ttu-id="c4e7a-361">Para obter mais informações, [consulte Executar comandos com o menu de comando Microsoft Edge DevTools][DevToolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-361">For more information, see [Run commands with the Microsoft Edge DevTools Command Menu][DevToolsCommandMenuIndex].</span></span>

### <a name="displaying-source-files-when-using-a-different-tool"></a><span data-ttu-id="c4e7a-362">Exibindo arquivos de origem ao usar uma ferramenta diferente</span><span class="sxs-lookup"><span data-stu-id="c4e7a-362">Displaying source files when using a different tool</span></span>

<span data-ttu-id="c4e7a-363">O principal local para exibir arquivos de origem no DevTools está na **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-363">The main place to view source files in the DevTools is within the **Sources** tool.</span></span>  <span data-ttu-id="c4e7a-364">Mas, às vezes, você precisa acessar outras ferramentas, como **Elementos** ou **Console**, durante a exibição ou edição de seus arquivos de origem.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-364">But sometimes you need to access other tools, such as **Elements** or **Console**, while viewing or editing your source files.</span></span>  <span data-ttu-id="c4e7a-365">Use a **ferramenta Fontes Rápidas** na [Gaveta][DevtoolsCustomizeIndexDrawer].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-365">Use the **Quick Sources** tool in the [Drawer][DevtoolsCustomizeIndexDrawer].</span></span>

1.  <span data-ttu-id="c4e7a-366">Selecione uma ferramenta diferente da **ferramenta Sources,** como a **ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-366">Select a tool other than the **Sources** tool, such as the **Elements** tool.</span></span>  
1.  <span data-ttu-id="c4e7a-367">Selecione `Ctrl` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="c4e7a-367">Select `Ctrl`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="c4e7a-368">O Menu de Comando é aberto.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-368">The Command Menu opens.</span></span>  
1.  <span data-ttu-id="c4e7a-369">Digite `Quick Source` e selecione Mostrar Fonte **Rápida**.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-369">Type `Quick Source`, and then select **Show Quick Source**.</span></span>  <span data-ttu-id="c4e7a-370">Na parte inferior da janela DevTools, a Gaveta é exibida, com o **painel De origem** rápida selecionado.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-370">At the bottom of the DevTools window, the Drawer appears, with the **Quick Source** panel selected.</span></span>  <span data-ttu-id="c4e7a-371">O **painel Fonte Rápida** contém o último arquivo editado na ferramenta **Fontes,** dentro de uma versão compacta do editor de código DevTools.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-371">The **Quick Source** panel contains the last file you edited in the **Sources** tool, within a compact version of the DevTools code editor.</span></span>  
1.  <span data-ttu-id="c4e7a-372">Selecione `Ctrl` + `P` \(Windows, Linux\) `Command` + `P` ou \(macOS\) para abrir a **caixa de diálogo Abrir Arquivo.**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-372">Select `Ctrl`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  

## <a name="using-the-debugger-pane-to-debug-javascript-code"></a><span data-ttu-id="c4e7a-373">Usando o painel Depurador para depurar código JavaScript</span><span class="sxs-lookup"><span data-stu-id="c4e7a-373">Using the Debugger pane to debug JavaScript code</span></span>

<span data-ttu-id="c4e7a-374">Use o depurador JavaScript para passar pelo código JavaScript retornado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-374">Use the JavaScript debugger to step through the JavaScript code that's returned by the server.</span></span> <span data-ttu-id="c4e7a-375">O depurador inclui o painel **Depurador,** juntamente com pontos de interrupção que você definir em linhas de código no **painel Editor.**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-375">The debugger includes the **Debugger** pane, along with breakpoints that you set on lines of code in the **Editor** pane.</span></span>

<span data-ttu-id="c4e7a-376">Com o depurador, você passa pelo código enquanto observa as expressões JavaScript especificadas.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-376">With the debugger, you step through the code, while watching any JavaScript expressions you specify.</span></span>  <span data-ttu-id="c4e7a-377">Assista e altere manualmente os valores de variável e mostre automaticamente quais variáveis estão no escopo da instrução atual.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-377">Watch and manually change variable values, and automatically show which variables are in-scope for the current statement.</span></span>

:::image type="complex" source="../media/sources-paused-breakpoint-highlight-debug-pane.msft.png" alt-text="O painel Depurador da ferramenta Sources  " lightbox="../media/sources-paused-breakpoint-highlight-debug-pane.msft.png":::
   <span data-ttu-id="c4e7a-379">O **painel Depurador** da **ferramenta Sources**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-379">The **Debugger** pane of the **Sources** tool</span></span>  
:::image-end:::  

<span data-ttu-id="c4e7a-380">O depurador dá suporte a ações padrão de depuração, como:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-380">The debugger supports standard debugging actions, such as:</span></span>  
*   <span data-ttu-id="c4e7a-381">Definindo pontos de interrupção, para pausar código.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-381">Setting breakpoints, to pause code.</span></span>
*   <span data-ttu-id="c4e7a-382">Passando pelo código.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-382">Stepping through code.</span></span>
*   <span data-ttu-id="c4e7a-383">Exibindo e editando propriedades e variáveis.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-383">Viewing and editing properties and variables.</span></span>
*   <span data-ttu-id="c4e7a-384">Observando os valores das expressões JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-384">Watching the values of JavaScript expressions.</span></span>
*   <span data-ttu-id="c4e7a-385">Exibindo a pilha de chamadas (a sequência de chamadas de função até o momento).</span><span class="sxs-lookup"><span data-stu-id="c4e7a-385">Viewing the call stack (the sequence of function calls so far).</span></span>

<span data-ttu-id="c4e7a-386">O depurador no DevTools foi projetado para parecer, parecer e trabalhar como o [depurador][CodeVisualStudioComDocsEditorDebugging] no Visual Studio Code e o [depurador em Visual Studio][DMCVisualStudioDebuggerNavigatingThroughCodeWithTheDebugger].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-386">The debugger in DevTools is designed to look, feel, and work like [the debugger in Visual Studio Code][CodeVisualStudioComDocsEditorDebugging] and [the debugger in Visual Studio][DMCVisualStudioDebuggerNavigatingThroughCodeWithTheDebugger].</span></span>

<span data-ttu-id="c4e7a-387">As subseções a seguir abrangem a depuração:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-387">The following subsections cover debugging:</span></span>
*   [<span data-ttu-id="c4e7a-388">A abordagem básica para usar um depurador</span><span class="sxs-lookup"><span data-stu-id="c4e7a-388">The basic approach to using a debugger</span></span>](#the-basic-approach-to-using-a-debugger)
*   [<span data-ttu-id="c4e7a-389">Vantagens do Watch and Scope do depurador sobre console.log</span><span class="sxs-lookup"><span data-stu-id="c4e7a-389">Advantages of the debugger's Watch and Scope over console.log</span></span>](#advantages-of-the-debuggers-watch-and-scope-over-consolelog)
*   [<span data-ttu-id="c4e7a-390">Depurar do Visual Studio Code diretamente</span><span class="sxs-lookup"><span data-stu-id="c4e7a-390">Debug from Visual Studio Code directly</span></span>](#debug-from-visual-studio-code-directly)
*   [<span data-ttu-id="c4e7a-391">Artigos sobre depuração</span><span class="sxs-lookup"><span data-stu-id="c4e7a-391">Articles about debugging</span></span>](#articles-about-debugging)

### <a name="the-basic-approach-to-using-a-debugger"></a><span data-ttu-id="c4e7a-392">A abordagem básica para usar um depurador</span><span class="sxs-lookup"><span data-stu-id="c4e7a-392">The basic approach to using a debugger</span></span>

<span data-ttu-id="c4e7a-393">Para solucionar problemas de código JavaScript, você pode inserir `console.log()` instruções no **painel Editor.**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-393">To troubleshoot JavaScript code, you can insert `console.log()` statements in the **Editor** pane.</span></span>  <span data-ttu-id="c4e7a-394">Outra abordagem mais poderosa é usar o depurador de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-394">Another, more powerful approach is to use the debugger of Microsoft Edge DevTools.</span></span>  <span data-ttu-id="c4e7a-395">O uso de um depurador pode ser mais simples do que , depois que você estiver familiarizado com a `console.log()` abordagem do depurador.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-395">Using a debugger can actually be simpler than `console.log()`, once you're familiar with the debugger approach.</span></span>

<span data-ttu-id="c4e7a-396">Para usar um depurador em uma página da Web, você normalmente definirá um ponto de interrupção e enviará um formulário da página da Web, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-396">To use a debugger on a webpage, you typically set a breakpoint and then send a form from the webpage, as follows:</span></span>

1.  <span data-ttu-id="c4e7a-397">Abra a página da Web em uma nova guia do navegador.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-397">Open the webpage in a new tab of the browser.</span></span>  <span data-ttu-id="c4e7a-398">Por exemplo, abra essa página da Web de formulário em uma nova guia: [Demonstração: Introdução Depuração javaScript com Microsoft Edge (Chromium) DevTools][DevtoolsGlitchMeDebugJsGetStarted].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-398">For example, open this form webpage in a new tab: [Demo: Get Started Debugging JavaScript with Microsoft Edge (Chromium) DevTools][DevtoolsGlitchMeDebugJsGetStarted].</span></span>

1.  <span data-ttu-id="c4e7a-399">Selecione `F12` para abrir a janela **DevTools** e selecione a **guia Fontes.**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-399">Select `F12` to open the **DevTools** window, and then select the **Sources** tab.</span></span>

1.  <span data-ttu-id="c4e7a-400">No painel **Navegador** (à esquerda), selecione a guia **Página** e selecione o arquivo JavaScript, como `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="c4e7a-400">In the **Navigator** pane (on the left), select the **Page** tab, and then select the JavaScript file, such as `get-started.js`.</span></span>

1.  <span data-ttu-id="c4e7a-401">No painel **Editor,** selecione um número de linha perto de uma linha de código suspeita para definir um ponto de interrupção nessa linha.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-401">In the **Editor** pane, select a line number near a suspect line of code, to set a breakpoint on that line.</span></span>  <span data-ttu-id="c4e7a-402">Na figura abaixo, um ponto de interrupção é definido na linha `var sum = addend1 + addend2;` .</span><span class="sxs-lookup"><span data-stu-id="c4e7a-402">In the figure below, a breakpoint is set on the line `var sum = addend1 + addend2;`.</span></span>

1.  <span data-ttu-id="c4e7a-403">Na página da Web, insira valores e envie o formulário.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-403">In the webpage, enter values and submit the form.</span></span>  <span data-ttu-id="c4e7a-404">Por exemplo, insira números, como e , em seguida, selecione o `5` botão Adicionar Número `1` **1 e Número 2**.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-404">For example, enter numbers, such as `5` and `1`, then select the button **Add Number 1 and Number 2**.</span></span>  

    <span data-ttu-id="c4e7a-405">O depurador executa o código JavaScript e pausa no ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-405">The debugger runs the JavaScript code and then pauses at the breakpoint.</span></span>  <span data-ttu-id="c4e7a-406">O depurador agora está no modo Pausado, para que você possa inspecionar os valores das propriedades que estão no escopo e passar pelo código.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-406">The debugger is now in Paused mode, so you can inspect the values of the properties that are in-scope, and step through the code.</span></span>

    :::image type="complex" source="../media/sources-paused-breakpoint-highlights.msft.png" alt-text="Inserindo o modo pausado do depurador" lightbox="../media/sources-paused-breakpoint-highlights.msft.png":::
        <span data-ttu-id="c4e7a-408">Inserindo o modo pausado do depurador</span><span class="sxs-lookup"><span data-stu-id="c4e7a-408">Entering Paused mode of the debugger</span></span>  
    :::image-end:::  

    <span data-ttu-id="c4e7a-409">Na figura acima, adicionamos as expressões watch e , e pisou `sum` duas linhas além do ponto de `typeof sum` interrupção.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-409">In the above figure, we added the Watch expressions `sum` and `typeof sum`, and stepped two lines past the breakpoint.</span></span>

1.  <span data-ttu-id="c4e7a-410">Examine os valores no painel **Escopo,** que mostra todas as variáveis ou propriedades que estão no escopo do ponto de interrupção atual e seus valores.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-410">Examine the values in the **Scope** pane, which shows all variables or properties that are in-scope for the current breakpoint, and their values.</span></span>  <span data-ttu-id="c4e7a-411">Ou adicione expressões no painel **de** relógio.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-411">Or, add expressions in the **Watch** pane.</span></span>  <span data-ttu-id="c4e7a-412">Essas expressões são as mesmas expressões que você escreveria em uma `console.log` instrução para depurar seu código.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-412">These expressions are the same expressions that you would write within a `console.log` statement to debug your code.</span></span>  <span data-ttu-id="c4e7a-413">Para executar comandos JavaScript para manipular dados no contexto atual, use **o Console**.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-413">To run JavaScript commands to manipulate data in the current context, use the **Console**.</span></span>  <span data-ttu-id="c4e7a-414">Para abrir o console, selecione `Esc` .</span><span class="sxs-lookup"><span data-stu-id="c4e7a-414">To open the console, select `Esc`.</span></span>  

1.  <span data-ttu-id="c4e7a-415">Passo a passo pelo código usando os controles na parte superior do painel **Depurador,** como **Etapa** ( `F9` ).</span><span class="sxs-lookup"><span data-stu-id="c4e7a-415">Step through the code by using the controls at the top of the **Debugger** pane, such as **Step** (`F9`).</span></span>

#### <a name="see-also"></a><span data-ttu-id="c4e7a-416">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c4e7a-416">See also</span></span>

*   <span data-ttu-id="c4e7a-417">[Introdução à depuração][DevtoolsGuideChromiumJavascriptIndex] do JavaScript - um tutorial usando uma página da Web existente e simples que contém alguns controles de formulário.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-417">[Get started with debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] - a tutorial using an existing, simple webpage that contains a few form controls.</span></span>

### <a name="advantages-of-the-debuggers-watch-and-scope-over-consolelog"></a><span data-ttu-id="c4e7a-418">Vantagens do Depurador\'s Watch and Scope sobre console\.log</span><span class="sxs-lookup"><span data-stu-id="c4e7a-418">Advantages of the debugger\'s Watch and Scope over console\.log</span></span>

<span data-ttu-id="c4e7a-419">Essas três abordagens são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-419">These three approaches are equivalent:</span></span>

*   <span data-ttu-id="c4e7a-420">Adicionando temporariamente `console.log(sum)` as instruções e no `console.log(typeof sum)` código, onde está no `sum` escopo.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-420">Temporarily adding the statements `console.log(sum)` and `console.log(typeof sum)` in the code, where `sum` is in-scope.</span></span>
*   <span data-ttu-id="c4e7a-421">Emitando as instruções e no painel Console do `sum` `console.log(typeof sum)` \*\*\*\* DevTools, quando o depurador é pausado onde `sum` está no escopo.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-421">Issuing the statements `sum` and `console.log(typeof sum)` in the **Console** pane of the DevTools, when the debugger is paused where `sum` is in-scope.</span></span>
*   <span data-ttu-id="c4e7a-422">Definindo **as expressões** do `sum` Relógio e no painel `typeof sum` **Depurador.**</span><span class="sxs-lookup"><span data-stu-id="c4e7a-422">Setting the **Watch** expressions `sum` and `typeof sum` in the **Debugger** pane.</span></span>

<span data-ttu-id="c4e7a-423">Quando a variável está no escopo, e seu valor é mostrado automaticamente na seção Escopo do `sum` `sum` painel **Depurador,** \*\*\*\* e também são sobreposição no painel Editor onde é `sum` calculado.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-423">When the variable `sum` is in-scope, `sum` and its value are automatically shown in the **Scope** section of the **Debugger** pane, and are also overlaid in the Editor pane where `sum` is calculated.</span></span>  <span data-ttu-id="c4e7a-424">Portanto, você provavelmente não precisaria definir uma expressão watch para `sum` .</span><span class="sxs-lookup"><span data-stu-id="c4e7a-424">So you probably wouldn't need to define a Watch expression for `sum`.</span></span>

<span data-ttu-id="c4e7a-425">O depurador oferece uma exibição mais rica e flexível e um ambiente do que uma `console.log` instrução.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-425">The debugger gives a richer, more flexible display and environment than a `console.log` statement.</span></span>  <span data-ttu-id="c4e7a-426">Por exemplo, no depurador, conforme você passa pelo código, você pode exibir e alterar os valores de todas as propriedades e variáveis definidas no momento.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-426">For example, in the debugger, as you step through the code, you can display and change the values of all currently defined properties and variables.</span></span>  <span data-ttu-id="c4e7a-427">Você também pode emitir instruções JavaScript no **Console**, como para alterar valores em uma matriz que está no escopo.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-427">You can also issue JavaScript statements in the **Console**, such as to change values in an array that's in-scope.</span></span>  <span data-ttu-id="c4e7a-428">(Para exibir o Console, selecione **Esc**.)</span><span class="sxs-lookup"><span data-stu-id="c4e7a-428">(To display the Console, select **Esc**.)</span></span>

<span data-ttu-id="c4e7a-429">As expressões Breakpoints e Watch são preservadas quando você atualize a página da Web.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-429">Breakpoints and Watch expressions are preserved when you refresh the webpage.</span></span>

### <a name="debug-from-visual-studio-code-directly"></a><span data-ttu-id="c4e7a-430">Depurar do Visual Studio Code diretamente</span><span class="sxs-lookup"><span data-stu-id="c4e7a-430">Debug from Visual Studio Code directly</span></span>

<span data-ttu-id="c4e7a-431">Para usar o depurador mais completo do Visual Studio Code em vez do depurador DevTools, use o Microsoft Edge Ferramentas para extensão **VS Code** para Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-431">To use the more full-featured debugger of Visual Studio Code instead of the DevTools debugger, use the **Microsoft Edge Tools for VS Code** extension for Visual Studio Code.</span></span>

:::image type="complex" source="../media/microsoft-edge-tools-for-vs-code-extension.msft.png" alt-text="As Microsoft Edge ferramentas para VS Code de Visual Studio Code" lightbox="../media/microsoft-edge-tools-for-vs-code-extension.msft.png":::
   <span data-ttu-id="c4e7a-433">O **Microsoft Edge ferramentas para VS Code** de Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="c4e7a-433">The **Microsoft Edge Tools for VS Code** extension for Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="c4e7a-434">Essa extensão fornece acesso \*\*\*\* às ferramentas **Elementos** e Rede do Microsoft Edge DevTools, de dentro Microsoft Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-434">This extension provides access to the **Elements** and **Network** tools of Microsoft Edge DevTools, from within Microsoft Visual Studio Code.</span></span>  

<span data-ttu-id="c4e7a-435">Para obter mais informações, [consulte Visual Studio Code visão][DevToolsVSCodeIndex] geral e a página GitHub Readme, Microsoft Edge Ferramentas de Desenvolvedor para [Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-435">For more information, see [Visual Studio Code overview][DevToolsVSCodeIndex] and the GitHub Readme page, [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools].</span></span>

### <a name="articles-about-debugging"></a><span data-ttu-id="c4e7a-436">Artigos sobre depuração</span><span class="sxs-lookup"><span data-stu-id="c4e7a-436">Articles about debugging</span></span>

<span data-ttu-id="c4e7a-437">Os artigos a seguir abrangem o painel **de depurador** e pontos de interrupção:</span><span class="sxs-lookup"><span data-stu-id="c4e7a-437">The following articles cover the **Debugger** pane and breakpoints:</span></span>

*   <span data-ttu-id="c4e7a-438">[Introdução à depuração de JavaScript no Microsoft Edge DevTools][DevtoolsGuideChromiumJavascriptIndex] - Um tutorial (com capturas de tela), usando um projeto existente e simples.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-438">[Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsGuideChromiumJavascriptIndex] - A tutorial (with screen captures), using an existing, simple project.</span></span>

*   <span data-ttu-id="c4e7a-439">Use os recursos [de depurador][DevToolsJavaScriptReference] - Como usar o depurador para definir pontos de interrupção, passar pelo código, exibir e modificar valores variáveis, assistir expressões JavaScript e exibir a pilha de chamada.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-439">[Use the debugger features][DevToolsJavaScriptReference] - How to use the debugger to set breakpoints, step through code, view and modify variable values, watch JavaScript expressions, and view the call stack.</span></span>

*   <span data-ttu-id="c4e7a-440">[Pause seu código com pontos de][DevToolsJavaScriptBreakpoints] interrupção - Como definir pontos de interrupção básicos e especializados no depurador.</span><span class="sxs-lookup"><span data-stu-id="c4e7a-440">[Pause your code with breakpoints][DevToolsJavaScriptBreakpoints] - How to set basic and specialized breakpoints in the debugger.</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c4e7a-441">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c4e7a-441">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsBeginnersCss]: ../beginners/css.md "DevTools para iniciantes: Começar a trabalhar em CSS | Microsoft Docs"
[DevToolsBeginnersHtml]: ../beginners/html.md "DevTools para iniciantes: começar com HTML e o dom | Microsoft Docs"
[DevToolsCommandMenuIndex]: ../command-menu/index.md "Executar comandos com o Menu de Comandos do Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: ../customize/index.md#drawer "Gaveta - Personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Alterar Microsoft Edge posicionamento do DevTools (Desfazer, Doca para baixo, Doca para a esquerda) | Microsoft Docs"
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Começar a depurar JavaScript no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Execute trechos de código do JavaScript em qualquer página da Web com Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Editar arquivos com espaços de trabalho | Microsoft Docs"  
[DevToolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Editar estilos de fonte CSS e configurações no painel Estilos | Microsoft Docs"
[DevToolsJavaScriptBreakpoints]: ../javascript/breakpoints.md "Pause seu código com pontos de interrupção | Microsoft Docs"
[DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode]: ../javascript/guides/mark-content-scripts-library-code.md "Marcar scripts de conteúdo como código biblioteca | Microsoft Docs"
[DevtoolsJavascriptOverrides]: ../javascript/overrides.md "Substituir recursos de página da Web por cópias locais usando Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavaScriptReference]: ../javascript/reference.md "Use os recursos de depurador | Microsoft Docs"
[DevToolsJavaScriptReferenceReformat]: ../javascript/reference.md#reformat-a-minified-javascript-file-with-pretty-print "Reformata um arquivo JavaScript minificado com impressão bastante impressa - Use os recursos de depurador | Microsoft Docs"
[DevToolsJavaScriptSourceMaps]: ../javascript/source-maps.md "Mapear código pré-processador para código-fonte | Microsoft Docs"
[DevToolsVSCodeIndex]: ../../visual-studio-code/index.md "Visual Studio Code visão geral | Microsoft Docs"
[ExtensionsChromiumGetstartPart2ContentScripts]: ../../extensions-chromium/getting-started/part2-content-scripts.md "Criar um tutorial de extensão Parte 2 | Microsoft Docs"
<!-- external: -->
[CodeVisualStudioComDocsEditorDebugging]: https://code.visualstudio.com/docs/editor/debugging "Depuração - Visual Studio Code | Microsoft Docs"
[DMCVisualStudioDebuggerNavigatingThroughCodeWithTheDebugger]: /visualstudio/debugger/navigating-through-code-with-the-debugger "Navegue pelo código com o Visual Studio depurador | Microsoft Docs"
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "Microsoft Edge Ferramentas de desenvolvedor para Visual Studio Code | GitHub"
[DevtoolsGlitchMeDebugJsGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Demonstração: Introdução Depuração javaScript com Microsoft Edge (Chromium) DevTools | Microsoft Docs"
[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origem | HTML Standard"  
[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Quadros | W3C"  
[MDNContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Scripts de conteúdo | MDN"  
[TypescriptlangMain]: https://www.typescriptlang.org "TypeScript"

> [!NOTE]
> <span data-ttu-id="c4e7a-467">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-467">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c4e7a-468">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/sources) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="c4e7a-468">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c4e7a-470">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c4e7a-470">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
