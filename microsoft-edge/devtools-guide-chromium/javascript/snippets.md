---
description: Os trechos de código são pequenos scripts que você pode criar e executar no painel fontes do Microsoft Edge DevTools.  Você pode acessá-los e executá-los em qualquer página.  Quando você executa um trecho, ele é executado do contexto da página atualmente aberta.
title: Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 5f6284179aacb471116a2d732507b010c37ef235
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993384"
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





# <span data-ttu-id="e4b39-106">Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e4b39-106">Run snippets of JavaScript on any page with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="e4b39-107">Se você estiver executando o mesmo código no [console][DevtoolsConsoleIndex] repetidamente, considere salvar o código como um trecho de código em vez disso.</span><span class="sxs-lookup"><span data-stu-id="e4b39-107">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="e4b39-108">Trechos de código são scripts que você cria no painel [fontes][DevToolsSourcesPanel] .</span><span class="sxs-lookup"><span data-stu-id="e4b39-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesPanel] panel.</span></span>  <span data-ttu-id="e4b39-109">Eles têm acesso ao contexto JavaScript da página, e você pode executá-los em qualquer página.</span><span class="sxs-lookup"><span data-stu-id="e4b39-109">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="e4b39-110">Os snippets são uma alternativa para [bookmarklets][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="e4b39-110">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="e4b39-111">O Firefox DevTools tem um recurso semelhante a Snippets chamado [bloco de rascunho][MDNScratchpad].</span><span class="sxs-lookup"><span data-stu-id="e4b39-111">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="e4b39-112">Por exemplo, na figura a seguir mostra a home page do DevTools à esquerda e algum código de origem do trecho à direita.</span><span class="sxs-lookup"><span data-stu-id="e4b39-112">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   <span data-ttu-id="e4b39-114">Qual a aparência da página antes de executar o trecho</span><span class="sxs-lookup"><span data-stu-id="e4b39-114">How the page looks before running the Snippet</span></span>  
:::image-end:::  

<span data-ttu-id="e4b39-115">O código-fonte do trecho da figura anterior.</span><span class="sxs-lookup"><span data-stu-id="e4b39-115">The Snippet source code from the previous figure.</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="e4b39-116">Na figura a seguir, a página aparece depois de executar o trecho de código.</span><span class="sxs-lookup"><span data-stu-id="e4b39-116">In the following figure, the page appears after running the Snippet.</span></span>  <span data-ttu-id="e4b39-117">A **gaveta do console** é exibida para exibir a `Hello, Snippets!` mensagem que o trecho registra e o conteúdo da página muda completamente.</span><span class="sxs-lookup"><span data-stu-id="e4b39-117">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Qual a aparência da página depois de executar o trecho" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="e4b39-119">Qual a aparência da página depois de executar o trecho</span><span class="sxs-lookup"><span data-stu-id="e4b39-119">How the page looks after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="e4b39-120">Abrir o painel Snippets</span><span class="sxs-lookup"><span data-stu-id="e4b39-120">Open the Snippets pane</span></span>   

<span data-ttu-id="e4b39-121">O painel **Snippets** lista seus trechos de código.</span><span class="sxs-lookup"><span data-stu-id="e4b39-121">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="e4b39-122">Quando você quiser editar um trecho de código, será necessário abri-lo no painel **Snippets** .</span><span class="sxs-lookup"><span data-stu-id="e4b39-122">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="O painel Snippets" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="e4b39-124">O painel **Snippets**</span><span class="sxs-lookup"><span data-stu-id="e4b39-124">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="e4b39-125">Abrir o painel Snippets com um mouse</span><span class="sxs-lookup"><span data-stu-id="e4b39-125">Open the Snippets pane with a mouse</span></span>   

1.  <span data-ttu-id="e4b39-126">Clique na guia **fontes** para abrir o painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="e4b39-126">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="e4b39-127">O painel de **página** geralmente abre por padrão.</span><span class="sxs-lookup"><span data-stu-id="e4b39-127">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="O painel fontes com o painel da página aberto à esquerda" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="e4b39-129">O painel **fontes** com o painel da **página** aberto à esquerda</span><span class="sxs-lookup"><span data-stu-id="e4b39-129">The **Sources** panel with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e4b39-130">Clique na guia **Snippets** para abrir o painel **Snippets** .</span><span class="sxs-lookup"><span data-stu-id="e4b39-130">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="e4b39-131">Talvez seja necessário clicar em **mais guias** \ ( ![ mais guias ][ImageMoreTabsIcon] \) para acessar a opção **Snippets** .</span><span class="sxs-lookup"><span data-stu-id="e4b39-131">You might need to click **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) in order to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="e4b39-132">Abrir o painel Snippets com o menu de comandos</span><span class="sxs-lookup"><span data-stu-id="e4b39-132">Open the Snippets pane with the Command Menu</span></span>   

1.  <span data-ttu-id="e4b39-133">Focalize o cursor em algum lugar dentro da DevTools.</span><span class="sxs-lookup"><span data-stu-id="e4b39-133">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="e4b39-134">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comandos.</span><span class="sxs-lookup"><span data-stu-id="e4b39-134">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="e4b39-135">Comece a digitar `Snippets` , selecione **Mostrar Snippets**e pressione `Enter` para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="e4b39-135">Start typing `Snippets`, select **Show Snippets**, and then press `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="O comando Mostrar Snippets" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="e4b39-137">O comando **Mostrar Snippets**</span><span class="sxs-lookup"><span data-stu-id="e4b39-137">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e4b39-138">Criar Snippets</span><span class="sxs-lookup"><span data-stu-id="e4b39-138">Create Snippets</span></span>   

### <span data-ttu-id="e4b39-139">Criar um snippet por meio do painel fontes</span><span class="sxs-lookup"><span data-stu-id="e4b39-139">Create a Snippet through the Sources panel</span></span>   

1.  <span data-ttu-id="e4b39-140">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="e4b39-140">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="e4b39-141">Clique em **novo snippet**.</span><span class="sxs-lookup"><span data-stu-id="e4b39-141">Click **New snippet**.</span></span>  
1.  <span data-ttu-id="e4b39-142">Digite um nome para o seu snippet e pressione `Enter` para salvar.</span><span class="sxs-lookup"><span data-stu-id="e4b39-142">Enter a name for your Snippet then press `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Nomear um snippet" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="e4b39-144">Nomear um snippet</span><span class="sxs-lookup"><span data-stu-id="e4b39-144">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e4b39-145">Criar um snippet por meio do menu de comando</span><span class="sxs-lookup"><span data-stu-id="e4b39-145">Create a Snippet through the Command Menu</span></span>   

1.  <span data-ttu-id="e4b39-146">Focalize o cursor em algum lugar dentro da DevTools.</span><span class="sxs-lookup"><span data-stu-id="e4b39-146">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="e4b39-147">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comandos.</span><span class="sxs-lookup"><span data-stu-id="e4b39-147">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="e4b39-148">Comece a digitar `Snippet` , selecione **criar novo snippet**e pressione `Enter` para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="e4b39-148">Start typing `Snippet`, select **Create new snippet**, then press `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="O comando para criar um novo snippet" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="e4b39-150">O comando para criar um novo snippet</span><span class="sxs-lookup"><span data-stu-id="e4b39-150">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="e4b39-151">Consulte [renomear trechos](#rename-snippets) se quiser dar um nome personalizado ao novo Snippet.</span><span class="sxs-lookup"><span data-stu-id="e4b39-151">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="e4b39-152">Editar trechos</span><span class="sxs-lookup"><span data-stu-id="e4b39-152">Edit Snippets</span></span>   

1.  <span data-ttu-id="e4b39-153">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="e4b39-153">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="e4b39-154">No painel **Snippets** , clique no nome do trecho que você deseja editar para abri-lo no **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="e4b39-154">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Editor de código" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="e4b39-156">**Editor de código**</span><span class="sxs-lookup"><span data-stu-id="e4b39-156">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e4b39-157">Use o **Editor de código** para adicionar JavaScript ao seu snippet.</span><span class="sxs-lookup"><span data-stu-id="e4b39-157">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="e4b39-158">Quando um asterisco aparece ao lado do nome de seu snippet, significa que você tem código não salvo.</span><span class="sxs-lookup"><span data-stu-id="e4b39-158">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="e4b39-159">Pressione `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) para salvar.</span><span class="sxs-lookup"><span data-stu-id="e4b39-159">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Um asterisco ao lado do nome do snippet, que indica o código não salvo" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="e4b39-161">Um asterisco ao lado do nome do snippet, que indica o código não salvo</span><span class="sxs-lookup"><span data-stu-id="e4b39-161">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e4b39-162">Executar Snippets</span><span class="sxs-lookup"><span data-stu-id="e4b39-162">Run Snippets</span></span>   

### <span data-ttu-id="e4b39-163">Executar um snippet do painel fontes</span><span class="sxs-lookup"><span data-stu-id="e4b39-163">Run a Snippet from the Sources panel</span></span>   

1.  <span data-ttu-id="e4b39-164">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="e4b39-164">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="e4b39-165">Clique no nome do trecho que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="e4b39-165">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="e4b39-166">O trecho é aberto no **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="e4b39-166">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="e4b39-167">Clique em **executar snippet** \ ( ![ executar snippet ][ImageRunSnippetIcon] \) ou pressione `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="e4b39-167">Click **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="e4b39-168">Executar um snippet com o menu de comando</span><span class="sxs-lookup"><span data-stu-id="e4b39-168">Run a Snippet with the Command Menu</span></span>   

1.  <span data-ttu-id="e4b39-169">Focalize o cursor em algum lugar dentro da DevTools.</span><span class="sxs-lookup"><span data-stu-id="e4b39-169">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="e4b39-170">Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comandos.</span><span class="sxs-lookup"><span data-stu-id="e4b39-170">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="e4b39-171">Exclua o `>` caractere e digite o `!` caractere seguido do nome do trecho que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="e4b39-171">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Executar um snippet no menu de comando" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="e4b39-173">Executar um snippet no **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="e4b39-173">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e4b39-174">Pressione `Enter` para executar o trecho de código.</span><span class="sxs-lookup"><span data-stu-id="e4b39-174">Press `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="e4b39-175">Renomear trechos</span><span class="sxs-lookup"><span data-stu-id="e4b39-175">Rename Snippets</span></span>   

1.  <span data-ttu-id="e4b39-176">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="e4b39-176">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="e4b39-177">Clique com o botão direito do mouse no nome do snippet e selecione **renomear**.</span><span class="sxs-lookup"><span data-stu-id="e4b39-177">Right-click the Snippet name and select **Rename**.</span></span>  
    
## <span data-ttu-id="e4b39-178">Excluir Snippets</span><span class="sxs-lookup"><span data-stu-id="e4b39-178">Delete Snippets</span></span>   

1.  <span data-ttu-id="e4b39-179">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="e4b39-179">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="e4b39-180">Clique com o botão direito do mouse no nome do snippet e selecione **remover**.</span><span class="sxs-lookup"><span data-stu-id="e4b39-180">Right-click the Snippet name and select **Remove**.</span></span>  
    
<!--  
 


-->  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Visão geral do console | Documentos da Microsoft"  
[DevToolsSourcesPanel]: ../sources.md "Visão geral do painel fontes | Documentos da Microsoft"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloco de rascunho | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="e4b39-185">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="e4b39-185">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e4b39-186">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e4b39-186">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e4b39-188">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e4b39-188">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
