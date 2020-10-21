---
description: Os trechos de código são pequenos scripts que você pode criar e executar no painel fontes do Microsoft Edge DevTools.  Você pode acessá-los e executá-los em qualquer página.  Quando você executa um trecho, ele é executado do contexto da página atualmente aberta.
title: Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: e353da76a5c354d834b69708c8a8c9e8dbdf9934
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124737"
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

# <span data-ttu-id="02567-106">Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="02567-106">Run snippets of JavaScript on any page with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="02567-107">Se você estiver executando o mesmo código no [console][DevtoolsConsoleIndex] repetidamente, considere salvar o código como um trecho de código em vez disso.</span><span class="sxs-lookup"><span data-stu-id="02567-107">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="02567-108">Trechos de código são scripts que você cria no painel [fontes][DevToolsSourcesPanel] .</span><span class="sxs-lookup"><span data-stu-id="02567-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesPanel] panel.</span></span>  <span data-ttu-id="02567-109">Eles têm acesso ao contexto JavaScript da página, e você pode executá-los em qualquer página.</span><span class="sxs-lookup"><span data-stu-id="02567-109">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="02567-110">Os snippets são uma alternativa para [bookmarklets][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="02567-110">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="02567-111">O Firefox DevTools tem um recurso semelhante a Snippets chamado [bloco de rascunho][MDNScratchpad].</span><span class="sxs-lookup"><span data-stu-id="02567-111">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="02567-112">Por exemplo, na figura a seguir mostra a home page do DevTools à esquerda e algum código de origem do trecho à direita.</span><span class="sxs-lookup"><span data-stu-id="02567-112">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   <span data-ttu-id="02567-114">Qual a aparência da página antes de executar o trecho</span><span class="sxs-lookup"><span data-stu-id="02567-114">How the page looks before running the Snippet</span></span>  
:::image-end:::  

<span data-ttu-id="02567-115">O código-fonte do trecho da figura anterior.</span><span class="sxs-lookup"><span data-stu-id="02567-115">The Snippet source code from the previous figure.</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="02567-116">Na figura a seguir, a página aparece depois de executar o trecho de código.</span><span class="sxs-lookup"><span data-stu-id="02567-116">In the following figure, the page appears after running the Snippet.</span></span>  <span data-ttu-id="02567-117">A **gaveta do console** é exibida para exibir a `Hello, Snippets!` mensagem que o trecho registra e o conteúdo da página muda completamente.</span><span class="sxs-lookup"><span data-stu-id="02567-117">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="02567-119">Qual a aparência da página depois de executar o trecho</span><span class="sxs-lookup"><span data-stu-id="02567-119">How the page looks after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="02567-120">Abrir o painel Snippets</span><span class="sxs-lookup"><span data-stu-id="02567-120">Open the Snippets pane</span></span>  

<span data-ttu-id="02567-121">O painel **Snippets** lista seus trechos de código.</span><span class="sxs-lookup"><span data-stu-id="02567-121">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="02567-122">Quando você quiser editar um trecho de código, será necessário abri-lo no painel **Snippets** .</span><span class="sxs-lookup"><span data-stu-id="02567-122">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="02567-124">O painel **Snippets**</span><span class="sxs-lookup"><span data-stu-id="02567-124">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="02567-125">Abrir o painel Snippets com um mouse</span><span class="sxs-lookup"><span data-stu-id="02567-125">Open the Snippets pane with a mouse</span></span>  

1.  <span data-ttu-id="02567-126">Clique na guia **fontes** para abrir o painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="02567-126">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="02567-127">O painel de **página** geralmente abre por padrão.</span><span class="sxs-lookup"><span data-stu-id="02567-127">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="02567-129">O painel **fontes** com o painel da **página** aberto à esquerda</span><span class="sxs-lookup"><span data-stu-id="02567-129">The **Sources** panel with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="02567-130">Clique na guia **Snippets** para abrir o painel **Snippets** .</span><span class="sxs-lookup"><span data-stu-id="02567-130">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="02567-131">Talvez seja necessário escolher **mais guias** \ ( ![ mais guias ][ImageMoreTabsIcon] \) para acessar a opção **Snippets** .</span><span class="sxs-lookup"><span data-stu-id="02567-131">You might need to choose **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) in order to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="02567-132">Abrir o painel Snippets com o menu de comandos</span><span class="sxs-lookup"><span data-stu-id="02567-132">Open the Snippets pane with the Command Menu</span></span>  

1.  <span data-ttu-id="02567-133">Focalize o cursor em algum lugar dentro da DevTools.</span><span class="sxs-lookup"><span data-stu-id="02567-133">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="02567-134">Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando.</span><span class="sxs-lookup"><span data-stu-id="02567-134">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="02567-135">Comece a digitar `Snippets` , escolha **Mostrar Snippets**e, em seguida, selecione `Enter` para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="02567-135">Start typing `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="02567-137">O comando **Mostrar Snippets**</span><span class="sxs-lookup"><span data-stu-id="02567-137">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="02567-138">Criar Snippets</span><span class="sxs-lookup"><span data-stu-id="02567-138">Create Snippets</span></span>  

### <span data-ttu-id="02567-139">Criar um snippet por meio do painel fontes</span><span class="sxs-lookup"><span data-stu-id="02567-139">Create a Snippet through the Sources panel</span></span>  

1.  <span data-ttu-id="02567-140">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="02567-140">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="02567-141">Escolha **novo snippet**.</span><span class="sxs-lookup"><span data-stu-id="02567-141">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="02567-142">Digite um nome para o seu snippet e, em seguida, selecione `Enter` salvar.</span><span class="sxs-lookup"><span data-stu-id="02567-142">Enter a name for your Snippet then select `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="02567-144">Nomear um snippet</span><span class="sxs-lookup"><span data-stu-id="02567-144">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="02567-145">Criar um snippet por meio do menu de comando</span><span class="sxs-lookup"><span data-stu-id="02567-145">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="02567-146">Focalize o cursor em algum lugar dentro da DevTools.</span><span class="sxs-lookup"><span data-stu-id="02567-146">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="02567-147">Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando.</span><span class="sxs-lookup"><span data-stu-id="02567-147">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="02567-148">Comece a digitar `Snippet` , escolha **criar novo snippet**e, em seguida, selecione `Enter` para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="02567-148">Start typing `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="02567-150">O comando para criar um novo snippet</span><span class="sxs-lookup"><span data-stu-id="02567-150">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="02567-151">Consulte [renomear trechos](#rename-snippets) se quiser dar um nome personalizado ao novo Snippet.</span><span class="sxs-lookup"><span data-stu-id="02567-151">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="02567-152">Editar trechos</span><span class="sxs-lookup"><span data-stu-id="02567-152">Edit Snippets</span></span>  

1.  <span data-ttu-id="02567-153">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="02567-153">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="02567-154">No painel **Snippets** , clique no nome do trecho que você deseja editar para abri-lo no **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="02567-154">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="02567-156">**Editor de código**</span><span class="sxs-lookup"><span data-stu-id="02567-156">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="02567-157">Use o **Editor de código** para adicionar JavaScript ao seu snippet.</span><span class="sxs-lookup"><span data-stu-id="02567-157">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="02567-158">Quando um asterisco aparece ao lado do nome de seu snippet, significa que você tem código não salvo.</span><span class="sxs-lookup"><span data-stu-id="02567-158">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="02567-159">Selecione `Control` + `S` \ (Windows, Linux \) ou `Command` + `S` \ (MacOS \) para salvar.</span><span class="sxs-lookup"><span data-stu-id="02567-159">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="02567-161">Um asterisco ao lado do nome do snippet, que indica o código não salvo</span><span class="sxs-lookup"><span data-stu-id="02567-161">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="02567-162">Executar Snippets</span><span class="sxs-lookup"><span data-stu-id="02567-162">Run Snippets</span></span>  

### <span data-ttu-id="02567-163">Executar um snippet do painel fontes</span><span class="sxs-lookup"><span data-stu-id="02567-163">Run a Snippet from the Sources panel</span></span>  

1.  <span data-ttu-id="02567-164">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="02567-164">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="02567-165">Clique no nome do trecho que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="02567-165">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="02567-166">O trecho é aberto no **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="02567-166">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="02567-167">Escolha **executar snippet** \ ( ![ executar snippet ][ImageRunSnippetIcon] \) ou selecionar `Control` + `Enter` \ (Windows, Linux \) ou `Command` + `Enter` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="02567-167">Choose **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="02567-168">Executar um snippet com o menu de comando</span><span class="sxs-lookup"><span data-stu-id="02567-168">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="02567-169">Focalize o cursor em algum lugar dentro da DevTools.</span><span class="sxs-lookup"><span data-stu-id="02567-169">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="02567-170">Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando.</span><span class="sxs-lookup"><span data-stu-id="02567-170">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="02567-171">Exclua o `>` caractere e digite o `!` caractere seguido do nome do trecho que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="02567-171">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Qual a aparência da página antes de executar o trecho" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="02567-173">Executar um snippet no **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="02567-173">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="02567-174">Selecione `Enter` para executar o trecho de código.</span><span class="sxs-lookup"><span data-stu-id="02567-174">Select `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="02567-175">Renomear trechos</span><span class="sxs-lookup"><span data-stu-id="02567-175">Rename Snippets</span></span>  

1.  <span data-ttu-id="02567-176">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="02567-176">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="02567-177">Clique com o botão direito do mouse no nome do snippet e escolha **renomear**.</span><span class="sxs-lookup"><span data-stu-id="02567-177">Right-click the Snippet name and choose **Rename**.</span></span>  
    
## <span data-ttu-id="02567-178">Excluir Snippets</span><span class="sxs-lookup"><span data-stu-id="02567-178">Delete Snippets</span></span>  

1.  <span data-ttu-id="02567-179">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="02567-179">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="02567-180">Clique com o botão direito do mouse no nome do snippet e escolha **remover**.</span><span class="sxs-lookup"><span data-stu-id="02567-180">Right-click the Snippet name and choose **Remove**.</span></span>  
    
## <span data-ttu-id="02567-181">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="02567-181">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Visão geral do console | Documentos da Microsoft"  
[DevToolsSourcesPanel]: ../sources.md "Visão geral do painel fontes | Documentos da Microsoft"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloco de rascunho | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="02567-186">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="02567-186">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="02567-187">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="02567-187">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="02567-189">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="02567-189">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
