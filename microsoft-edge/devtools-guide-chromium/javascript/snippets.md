---
title: Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: aa9f7e96c7e379c1fe537ffba730e08990e0c20a
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581814"
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





# <span data-ttu-id="ce4d6-103">Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ce4d6-103">Run Snippets Of JavaScript On Any Page With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="ce4d6-104">Se você estiver executando o mesmo código no [console][DevtoolsConsoleIndex] repetidamente, considere salvar o código como um trecho de código em vez disso.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-104">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="ce4d6-105">Trechos de código são scripts que você cria no [painel **fontes** ][DevToolsSourcesPanel].</span><span class="sxs-lookup"><span data-stu-id="ce4d6-105">Snippets are scripts that you author in the [**Sources** panel][DevToolsSourcesPanel].</span></span>  <span data-ttu-id="ce4d6-106">Eles têm acesso ao contexto JavaScript da página, e você pode executá-los em qualquer página.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-106">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="ce4d6-107">Os snippets são uma alternativa para [bookmarklets][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="ce4d6-107">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="ce4d6-108">O Firefox DevTools tem um recurso semelhante a Snippets chamado [bloco de rascunho][MDNScratchpad].</span><span class="sxs-lookup"><span data-stu-id="ce4d6-108">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="ce4d6-109">Por exemplo, a [**Figura 1**](#figure-1) mostra a home page do devtools à esquerda e parte do código-fonte do trecho à direita.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-109">For example, [**Figure 1**](#figure-1) shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

> ##### <span data-ttu-id="ce4d6-110">Figura 1</span><span class="sxs-lookup"><span data-stu-id="ce4d6-110">Figure 1</span></span>  
> <span data-ttu-id="ce4d6-111">Qual a aparência da página antes de executar o trecho</span><span class="sxs-lookup"><span data-stu-id="ce4d6-111">How the page looks before running the Snippet</span></span>  
> ![Qual a aparência da página antes de executar o trecho][ImageSnippetSplitScreen]  

<span data-ttu-id="ce4d6-113">O código-fonte do trecho da [**Figura 1**](#figure-1):</span><span class="sxs-lookup"><span data-stu-id="ce4d6-113">The Snippet source code from [**Figure 1**](#figure-1):</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="ce4d6-114">A [**Figura 2**](#figure-2) mostra como a página é exibida após a execução do trecho de código.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-114">[**Figure 2**](#figure-2) shows how the page looks after running the Snippet.</span></span>  <span data-ttu-id="ce4d6-115">A **gaveta do console** é exibida para exibir a `Hello, Snippets!` mensagem que o trecho registra e o conteúdo da página muda completamente.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-115">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

> ##### <span data-ttu-id="ce4d6-116">Figura 2</span><span class="sxs-lookup"><span data-stu-id="ce4d6-116">Figure 2</span></span>  
> <span data-ttu-id="ce4d6-117">Qual a aparência da página depois de executar o trecho</span><span class="sxs-lookup"><span data-stu-id="ce4d6-117">How the page looks after running the Snippet</span></span>  
> ![Qual a aparência da página depois de executar o trecho][ImageSnippetSplitScreenAfter]  

## <span data-ttu-id="ce4d6-119">Abrir o painel Snippets</span><span class="sxs-lookup"><span data-stu-id="ce4d6-119">Open the Snippets pane</span></span>   

<span data-ttu-id="ce4d6-120">O painel **Snippets** lista seus trechos de código.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-120">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="ce4d6-121">Quando você quiser editar um trecho de código, será necessário abri-lo no painel **Snippets** .</span><span class="sxs-lookup"><span data-stu-id="ce4d6-121">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

> ##### <span data-ttu-id="ce4d6-122">Figura 3</span><span class="sxs-lookup"><span data-stu-id="ce4d6-122">Figure 3</span></span>  
> <span data-ttu-id="ce4d6-123">O painel **Snippets**</span><span class="sxs-lookup"><span data-stu-id="ce4d6-123">The **Snippets** pane</span></span>  
> ![O painel Snippets][ImageSnippetsPane]  

### <span data-ttu-id="ce4d6-125">Abrir o painel Snippets com um mouse</span><span class="sxs-lookup"><span data-stu-id="ce4d6-125">Open the Snippets pane with a mouse</span></span>   

1.  <span data-ttu-id="ce4d6-126">Clique na guia **fontes** para abrir o painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="ce4d6-126">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="ce4d6-127">O painel de **página** geralmente abre por padrão.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-127">The **Page** pane usually opens by default.</span></span>  

    > ##### <span data-ttu-id="ce4d6-128">Figura 4</span><span class="sxs-lookup"><span data-stu-id="ce4d6-128">Figure 4</span></span>  
    > <span data-ttu-id="ce4d6-129">O painel **fontes** com o painel da **página** aberto à esquerda</span><span class="sxs-lookup"><span data-stu-id="ce4d6-129">The **Sources** panel with the **Page** pane open on the left</span></span>  
    > ![O painel fontes com o painel da página aberto à esquerda][ImageSourcesPageEmpty]  

1.  <span data-ttu-id="ce4d6-131">Clique na guia **Snippets** para abrir o painel **Snippets** .</span><span class="sxs-lookup"><span data-stu-id="ce4d6-131">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="ce4d6-132">Talvez seja necessário clicar em **mais** guias ![ ][ImageMoreTabsIcon] para acessar a opção **Snippets** .</span><span class="sxs-lookup"><span data-stu-id="ce4d6-132">You might need to click **More Tabs** ![More Tabs][ImageMoreTabsIcon] in order to access the **Snippets** option.</span></span>  

### <span data-ttu-id="ce4d6-133">Abrir o painel Snippets com o menu de comandos</span><span class="sxs-lookup"><span data-stu-id="ce4d6-133">Open the Snippets pane with the Command Menu</span></span>   

1.  <span data-ttu-id="ce4d6-134">Focalize o cursor em algum lugar dentro da DevTools.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-134">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="ce4d6-135">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comandos.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-135">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="ce4d6-136">Comece a digitar `Snippets` , selecione **Mostrar Snippets**e pressione `Enter` para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-136">Start typing `Snippets`, select **Show Snippets**, and then press `Enter` to run the command.</span></span>  

    > ##### <span data-ttu-id="ce4d6-137">Figura 5</span><span class="sxs-lookup"><span data-stu-id="ce4d6-137">Figure 5</span></span>  
    > <span data-ttu-id="ce4d6-138">O comando **Mostrar Snippets**</span><span class="sxs-lookup"><span data-stu-id="ce4d6-138">The **Show Snippets** command</span></span>  
    > ![O comando Mostrar Snippets][ImageShowSnippetsSearch]  

## <span data-ttu-id="ce4d6-140">Criar Snippets</span><span class="sxs-lookup"><span data-stu-id="ce4d6-140">Create Snippets</span></span>   

### <span data-ttu-id="ce4d6-141">Criar um snippet por meio do painel fontes</span><span class="sxs-lookup"><span data-stu-id="ce4d6-141">Create a Snippet through the Sources panel</span></span>   

1.  <span data-ttu-id="ce4d6-142">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="ce4d6-142">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="ce4d6-143">Clique em **novo snippet**.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-143">Click **New snippet**.</span></span>  
1.  <span data-ttu-id="ce4d6-144">Digite um nome para o seu snippet e pressione `Enter` para salvar.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-144">Enter a name for your Snippet then press `Enter` to save.</span></span>  

    > ##### <span data-ttu-id="ce4d6-145">Figura 6</span><span class="sxs-lookup"><span data-stu-id="ce4d6-145">Figure 6</span></span>  
    > <span data-ttu-id="ce4d6-146">Nomear um snippet</span><span class="sxs-lookup"><span data-stu-id="ce4d6-146">Naming a Snippet</span></span>  
    > ![Nomear um snippet][ImageSnippetName]  

### <span data-ttu-id="ce4d6-148">Criar um snippet por meio do menu de comando</span><span class="sxs-lookup"><span data-stu-id="ce4d6-148">Create a Snippet through the Command Menu</span></span>   

1.  <span data-ttu-id="ce4d6-149">Focalize o cursor em algum lugar dentro da DevTools.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-149">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="ce4d6-150">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comandos.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-150">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="ce4d6-151">Comece a digitar `Snippet` , selecione **criar novo snippet**e pressione `Enter` para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-151">Start typing `Snippet`, select **Create new snippet**, then press `Enter` to run the command.</span></span>  

    > ##### <span data-ttu-id="ce4d6-152">Figura 7</span><span class="sxs-lookup"><span data-stu-id="ce4d6-152">Figure 7</span></span>  
    > <span data-ttu-id="ce4d6-153">O comando para criar um novo snippet</span><span class="sxs-lookup"><span data-stu-id="ce4d6-153">The command for creating a new Snippet</span></span>  
    > ![O comando para criar um novo snippet][ImageCreateSnippetSearch]  

<span data-ttu-id="ce4d6-155">Consulte [renomear trechos](#rename-snippets) se quiser dar um nome personalizado ao novo Snippet.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-155">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="ce4d6-156">Editar trechos</span><span class="sxs-lookup"><span data-stu-id="ce4d6-156">Edit Snippets</span></span>   

1.  <span data-ttu-id="ce4d6-157">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="ce4d6-157">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="ce4d6-158">No painel **Snippets** , clique no nome do trecho que você deseja editar para abri-lo no **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-158">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  

    > ##### <span data-ttu-id="ce4d6-159">Figura 8</span><span class="sxs-lookup"><span data-stu-id="ce4d6-159">Figure 8</span></span>  
    > <span data-ttu-id="ce4d6-160">Editor de código</span><span class="sxs-lookup"><span data-stu-id="ce4d6-160">The Code Editor</span></span>  
    > ![Editor de código][ImageSnippetEditor]  

1.  <span data-ttu-id="ce4d6-162">Use o **Editor de código** para adicionar JavaScript ao seu snippet.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-162">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="ce4d6-163">Quando um asterisco aparece ao lado do nome de seu snippet, significa que você tem código não salvo.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-163">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="ce4d6-164">Pressione `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) para salvar.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-164">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  

    > ##### <span data-ttu-id="ce4d6-165">Figura 9</span><span class="sxs-lookup"><span data-stu-id="ce4d6-165">Figure 9</span></span>  
    > <span data-ttu-id="ce4d6-166">Um asterisco ao lado do nome do snippet, que indica o código não salvo</span><span class="sxs-lookup"><span data-stu-id="ce4d6-166">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    > ![Um asterisco ao lado do nome do snippet, que indica o código não salvo][ImageUnsavedSnippet]  

## <span data-ttu-id="ce4d6-168">Executar Snippets</span><span class="sxs-lookup"><span data-stu-id="ce4d6-168">Run Snippets</span></span>   

### <span data-ttu-id="ce4d6-169">Executar um snippet do painel fontes</span><span class="sxs-lookup"><span data-stu-id="ce4d6-169">Run a Snippet from the Sources panel</span></span>   

1.  <span data-ttu-id="ce4d6-170">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="ce4d6-170">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="ce4d6-171">Clique no nome do trecho que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-171">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="ce4d6-172">O trecho é aberto no **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-172">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="ce4d6-173">Clique em **executar** ![ trecho ][ImageRunSnippetIcon] de código de execução, ou pressione `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="ce4d6-173">Click **Run Snippet** ![Run Snippet][ImageRunSnippetIcon], or press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\).</span></span>  

### <span data-ttu-id="ce4d6-174">Executar um snippet com o menu de comando</span><span class="sxs-lookup"><span data-stu-id="ce4d6-174">Run a Snippet with the Command Menu</span></span>   

1.  <span data-ttu-id="ce4d6-175">Focalize o cursor em algum lugar dentro da DevTools.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-175">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="ce4d6-176">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comandos.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-176">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="ce4d6-177">Exclua o `>` caractere e digite o `!` caractere seguido do nome do trecho que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-177">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  

    > ##### <span data-ttu-id="ce4d6-178">Figura 10</span><span class="sxs-lookup"><span data-stu-id="ce4d6-178">Figure 10</span></span>  
    > <span data-ttu-id="ce4d6-179">Executar um snippet no menu de comando</span><span class="sxs-lookup"><span data-stu-id="ce4d6-179">Running a Snippet from the Command Menu</span></span>  
    > ![Executar um snippet no menu de comando][ImageRunSnippetCommand]  

1.  <span data-ttu-id="ce4d6-181">Pressione `Enter` para executar o trecho de código.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-181">Press `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="ce4d6-182">Renomear trechos</span><span class="sxs-lookup"><span data-stu-id="ce4d6-182">Rename Snippets</span></span>   

1.  <span data-ttu-id="ce4d6-183">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="ce4d6-183">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="ce4d6-184">Clique com o botão direito do mouse no nome do snippet e selecione **renomear**.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-184">Right-click the Snippet name and select **Rename**.</span></span>  

## <span data-ttu-id="ce4d6-185">Excluir Snippets</span><span class="sxs-lookup"><span data-stu-id="ce4d6-185">Delete Snippets</span></span>   

1.  <span data-ttu-id="ce4d6-186">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="ce4d6-186">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="ce4d6-187">Clique com o botão direito do mouse no nome do snippet e selecione **remover**.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-187">Right-click the Snippet name and select **Remove**.</span></span>  

 



<!-- image links -->  

[ImageMoreTabsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSnippetSplitScreen]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen.msft.png "Figura 1: qual a aparência da página antes de executar o trecho"  
[ImageSnippetSplitScreenAfter]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen-after.msft.png "Figura 2: como a página é exibida após a execução do snippet"  
[ImageSnippetsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-pane.msft.png "Figura 3: o painel Snippets"  
[ImageSourcesPageEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-pane.msft.png "Figura 4: painel fontes com o painel da página aberto à esquerda"  
[ImageShowSnippetsSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-show-snippets.msft.png "Figura 5: o comando Mostrar Snippets"  
[ImageSnippetName]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-naming.msft.png "Figura 6: nomeando um trecho"  
[ImageCreateSnippetSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-create-new-snippet.msft.png "Figura 7: o comando para criar um novo snippet"  
[ImageSnippetEditor]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-saved.msft.png "Figura 8: editor de código"  
[ImageUnsavedSnippet]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-unsaved.msft.png "Figura 9: um asterisco ao lado do nome do snippet, que indica o código não salvo"  
[ImageRunSnippetCommand]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-run-command.msft.png "Figura 10: executando um snippet no menu de comando"  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Visão geral do console"  
[DevToolsSourcesPanel]: ../sources.md "Visão geral do painel fontes"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloco de rascunho | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="ce4d6-202">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="ce4d6-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ce4d6-203">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="ce4d6-203">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ce4d6-205">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ce4d6-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
