---
description: Os trechos de código são pequenos scripts que você pode criar e executar dentro da ferramenta fontes do Microsoft Edge DevTools.  Você pode acessar e executar recursos de qualquer página da Web.  Quando você executa um trecho, ele é executado do contexto da página da Web aberta no momento.
title: Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 3542243f7fa886865ced47d47991cd9b11001e2e
ms.sourcegitcommit: 9dcaf598f3930bcfab9f93ff63463beb98274de0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/30/2020
ms.locfileid: "11145117"
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

# <span data-ttu-id="9bfa9-106">Executar trechos de JavaScript em qualquer página da Web com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9bfa9-106">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="9bfa9-107">Se você estiver executando o mesmo código no [console][DevtoolsConsoleIndex] repetidamente, considere salvar o código como um trecho em vez disso.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-107">If you are running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="9bfa9-108">Trechos de código são scripts que você cria na ferramenta [fontes][DevToolsSourcesTool] .</span><span class="sxs-lookup"><span data-stu-id="9bfa9-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesTool] tool.</span></span>  <span data-ttu-id="9bfa9-109">Os snippets têm acesso ao contexto JavaScript da página da Web, e você pode executar Snippets em qualquer página da Web.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-109">Snippets have access to the JavaScript context of the webpage, and you may run snippets on any webpage.</span></span>  <span data-ttu-id="9bfa9-110">As configurações de segurança da maioria das páginas da Web bloqueiam o carregamento de outros scripts em Snippets.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-110">The security settings of most webpages block from loading other scripts in Snippets.</span></span>  <span data-ttu-id="9bfa9-111">Por esse motivo, você deve incluir todo o código em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-111">For that reason, you must include all your code in one file.</span></span>  

<span data-ttu-id="9bfa9-112">Os snippets são uma alternativa para [bookmarklets][WikiBookmarklet] com a diferença que os trechos de código são executados apenas em devtools e não se limitam ao comprimento permitido de uma URL.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-112">Snippets are an alternative to [bookmarklets][WikiBookmarklet] with the difference that Snippets only run in DevTools and are not limited to the allowed length of a URL.</span></span>  

<span data-ttu-id="9bfa9-113">Usar Snippets é uma maneira excelente de alterar algumas coisas em uma página da Web de terceiros.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-113">Using Snippets is an excellent way to change a few things in a third-party webpage.</span></span>  <span data-ttu-id="9bfa9-114">As alterações de código em Snippets são adicionadas à página da Web atual e são executadas no mesmo contexto.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-114">Code changes in Snippets are added to the current webpage and run in the same context.</span></span>  <span data-ttu-id="9bfa9-115">Para obter mais informações sobre como alterar o código existente de uma página da Web, navegue até [substituições][DevtoolsJavascriptOverrides].</span><span class="sxs-lookup"><span data-stu-id="9bfa9-115">For more information about changing the existing code of a webpage, navigate to [Overrides][DevtoolsJavascriptOverrides].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9bfa9-116">Por exemplo, na figura a seguir mostra a home page do DevTools à esquerda e algum código de origem do trecho à direita.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-116">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="O antes de executar o trecho de código" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         <span data-ttu-id="9bfa9-118">A página da Web antes de executar o trecho de código</span><span class="sxs-lookup"><span data-stu-id="9bfa9-118">The webpage before running the Snippet</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="9bfa9-119">O código-fonte do trecho da página da Web antes de executar o trecho de código.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-119">The Snippet source code from the webpage before running the Snippet.</span></span>  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

<span data-ttu-id="9bfa9-120">Na figura a seguir, a página da Web é exibida após a execução do trecho de código.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-120">In the following figure, the webpage appears after running the Snippet.</span></span>  <span data-ttu-id="9bfa9-121">A **gaveta do console** é exibida para exibir a `Hello, Snippets!` mensagem que o trecho registra e o conteúdo da página muda completamente.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-121">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the webpage changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="A página da Web após a execução do snippet" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="9bfa9-123">A página da Web após a execução do snippet</span><span class="sxs-lookup"><span data-stu-id="9bfa9-123">The webpage after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="9bfa9-124">Abrir o painel Snippets</span><span class="sxs-lookup"><span data-stu-id="9bfa9-124">Open the Snippets pane</span></span>  

<span data-ttu-id="9bfa9-125">O painel **Snippets** lista seus trechos de código.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-125">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="9bfa9-126">Quando você quiser editar um trecho de código, será necessário abri-lo no painel **Snippets** .</span><span class="sxs-lookup"><span data-stu-id="9bfa9-126">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="O painel Snippets" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="9bfa9-128">O painel **Snippets**</span><span class="sxs-lookup"><span data-stu-id="9bfa9-128">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="9bfa9-129">Abrir o painel Snippets com um mouse</span><span class="sxs-lookup"><span data-stu-id="9bfa9-129">Open the Snippets pane with a mouse</span></span>  

1.  <span data-ttu-id="9bfa9-130">Escolha a guia **fontes** para abrir a ferramenta **fontes** .</span><span class="sxs-lookup"><span data-stu-id="9bfa9-130">Choose the **Sources** tab to open the **Sources** tool.</span></span>  <span data-ttu-id="9bfa9-131">O painel de **página** geralmente abre por padrão.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-131">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="A ferramenta fontes com o painel da página aberto à esquerda" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="9bfa9-133">A ferramenta **fontes** com o painel da **página** aberto à esquerda</span><span class="sxs-lookup"><span data-stu-id="9bfa9-133">The **Sources** tool with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9bfa9-134">Escolha a guia **Snippets** para abrir o painel **Snippets** .</span><span class="sxs-lookup"><span data-stu-id="9bfa9-134">Choose the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="9bfa9-135">Talvez seja necessário escolher **mais guias** \ ( ![ mais guias ][ImageMoreTabsIcon] \) para acessar a opção **Snippets** .</span><span class="sxs-lookup"><span data-stu-id="9bfa9-135">You may need to choose **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="9bfa9-136">Abrir o painel Snippets com o menu de comandos</span><span class="sxs-lookup"><span data-stu-id="9bfa9-136">Open the Snippets pane with the Command Menu</span></span>  

1.  <span data-ttu-id="9bfa9-137">Focalize o cursor em algum lugar no DevTools.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-137">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="9bfa9-138">Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-138">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="9bfa9-139">Tipo `Snippets` , escolha **Mostrar Snippets**e, em seguida, selecione `Enter` para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-139">Type `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="O comando Mostrar Snippets" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="9bfa9-141">O comando **Mostrar Snippets**</span><span class="sxs-lookup"><span data-stu-id="9bfa9-141">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="9bfa9-142">Criar Snippets</span><span class="sxs-lookup"><span data-stu-id="9bfa9-142">Create Snippets</span></span>  

### <span data-ttu-id="9bfa9-143">Criar um snippet por meio do painel fontes</span><span class="sxs-lookup"><span data-stu-id="9bfa9-143">Create a Snippet through the Sources panel</span></span>  

1.  <span data-ttu-id="9bfa9-144">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="9bfa9-144">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="9bfa9-145">Escolha **novo snippet**.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-145">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="9bfa9-146">Digite um nome para o seu snippet e, em seguida, selecione `Enter` salvar.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-146">Enter a name for your Snippet then select `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Nomear um snippet" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="9bfa9-148">Nomear um snippet</span><span class="sxs-lookup"><span data-stu-id="9bfa9-148">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="9bfa9-149">Criar um snippet por meio do menu de comando</span><span class="sxs-lookup"><span data-stu-id="9bfa9-149">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="9bfa9-150">Focalize o cursor em algum lugar no DevTools.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-150">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="9bfa9-151">Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-151">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="9bfa9-152">Digite `Snippet` , escolha **criar novo snippet**e, em seguida, selecione `Enter` para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-152">Type `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="O comando para criar um novo snippet" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="9bfa9-154">O comando para criar um novo snippet</span><span class="sxs-lookup"><span data-stu-id="9bfa9-154">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="9bfa9-155">Para renomear o novo snippet com um nome personalizado, navegue até [renomear trechos](#rename-snippets).</span><span class="sxs-lookup"><span data-stu-id="9bfa9-155">To rename your new Snippet with a custom name, navigate to [Rename Snippets](#rename-snippets).</span></span>  

## <span data-ttu-id="9bfa9-156">Editar trechos</span><span class="sxs-lookup"><span data-stu-id="9bfa9-156">Edit Snippets</span></span>  

1.  <span data-ttu-id="9bfa9-157">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="9bfa9-157">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="9bfa9-158">No painel **Snippets** , escolha o nome do trecho que você deseja editar.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-158">In the **Snippets** pane, choose the name of the Snippet that you want to edit.</span></span>  <span data-ttu-id="9bfa9-159">Ele abre no **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-159">It opens in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Editor de código" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="9bfa9-161">**Editor de código**</span><span class="sxs-lookup"><span data-stu-id="9bfa9-161">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9bfa9-162">Use o **Editor de código** para adicionar JavaScript ao seu snippet.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-162">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="9bfa9-163">Quando um asterisco é exibido ao lado do nome do seu snippet, isso significa que você tem código não salvo.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-163">When an asterisk appears next to the name of your Snippet, it means you have unsaved code.</span></span>  <span data-ttu-id="9bfa9-164">Selecione `Control` + `S` \ (Windows, Linux \) ou `Command` + `S` \ (MacOS \) para salvar.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-164">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Um asterisco ao lado do nome do trecho indica o código não salvo" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="9bfa9-166">Um asterisco ao lado do nome do trecho indica o código não salvo</span><span class="sxs-lookup"><span data-stu-id="9bfa9-166">An asterisk next to the Snippet name indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="9bfa9-167">Executar Snippets</span><span class="sxs-lookup"><span data-stu-id="9bfa9-167">Run Snippets</span></span>  

### <span data-ttu-id="9bfa9-168">Executar um snippet do painel fontes</span><span class="sxs-lookup"><span data-stu-id="9bfa9-168">Run a Snippet from the Sources panel</span></span>  

1.  <span data-ttu-id="9bfa9-169">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="9bfa9-169">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="9bfa9-170">Escolha o nome do trecho que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-170">Choose the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="9bfa9-171">O trecho é aberto no **Editor de código**.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-171">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="9bfa9-172">Escolha **executar snippet** \ ( ![ executar snippet ][ImageRunSnippetIcon] \) ou selecionar `Control` + `Enter` \ (Windows, Linux \) ou `Command` + `Enter` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="9bfa9-172">Choose **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="9bfa9-173">Executar um snippet com o menu de comando</span><span class="sxs-lookup"><span data-stu-id="9bfa9-173">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="9bfa9-174">Focalize o cursor em algum lugar no DevTools.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-174">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="9bfa9-175">Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-175">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="9bfa9-176">Exclua o `>` caractere e digite o `!` caractere seguido do nome do trecho que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-176">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Executar um snippet no menu de comando" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="9bfa9-178">Executar um snippet no **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="9bfa9-178">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9bfa9-179">Selecione `Enter` para executar o trecho de código.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-179">Select `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="9bfa9-180">Renomear trechos</span><span class="sxs-lookup"><span data-stu-id="9bfa9-180">Rename Snippets</span></span>  

1.  <span data-ttu-id="9bfa9-181">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="9bfa9-181">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="9bfa9-182">Passe o cursor do mouse sobre o nome do snippet, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **renomear**.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-182">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Rename**.</span></span>  
    
## <span data-ttu-id="9bfa9-183">Excluir Snippets</span><span class="sxs-lookup"><span data-stu-id="9bfa9-183">Delete Snippets</span></span>  

1.  <span data-ttu-id="9bfa9-184">[Abrir o painel **Snippets** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="9bfa9-184">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="9bfa9-185">Passe o cursor do mouse sobre o nome do snippet, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **remover**.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-185">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Remove**.</span></span>  
    
## <span data-ttu-id="9bfa9-186">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9bfa9-186">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Visão geral do console | Documentos da Microsoft"  
[DevToolsSourcesTool]: ../sources.md "Visão geral da ferramenta fontes | Documentos da Microsoft"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Substituições | Documentos da Microsoft"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloco de rascunho | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Wikipédia"  

> [!NOTE]
> <span data-ttu-id="9bfa9-192">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="9bfa9-192">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9bfa9-193">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="9bfa9-193">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9bfa9-195">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9bfa9-195">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
