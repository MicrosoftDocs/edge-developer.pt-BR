---
description: Trechos de código são scripts pequenos que você pode escrever e executar na ferramenta Sources do Microsoft Edge DevTools.  Você pode acessar e executar recursos de qualquer página da Web.  Quando você executa um trecho, ele é executado a partir do contexto da página da Web aberta no momento.
title: Executar trechos de código do JavaScript em qualquer página da Web com Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 4a84e959f652320f40a501a26e9ba763c7348b33
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564109"
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
# <a name="run-snippets-of-javascript-on-any-webpage-with-microsoft-edge-devtools"></a><span data-ttu-id="bca9f-106">Executar trechos de código do JavaScript em qualquer página da Web com Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bca9f-106">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="bca9f-107">Se você estiver executando o mesmo código no [Console][DevtoolsConsoleIndex] repetidamente, considere salvar o código como um trecho.</span><span class="sxs-lookup"><span data-stu-id="bca9f-107">If you are running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="bca9f-108">Trechos de código são scripts que você escreveu na [ferramenta Fontes.][DevToolsSourcesTool]</span><span class="sxs-lookup"><span data-stu-id="bca9f-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesTool] tool.</span></span>  <span data-ttu-id="bca9f-109">Trechos de código têm acesso ao contexto JavaScript da página da Web e você pode executar trechos em qualquer página da Web.</span><span class="sxs-lookup"><span data-stu-id="bca9f-109">Snippets have access to the JavaScript context of the webpage, and you may run snippets on any webpage.</span></span>  <span data-ttu-id="bca9f-110">As configurações de segurança da maioria das páginas da Web bloqueiam o carregamento de outros scripts em Trechos de Código.</span><span class="sxs-lookup"><span data-stu-id="bca9f-110">The security settings of most webpages block from loading other scripts in Snippets.</span></span>  <span data-ttu-id="bca9f-111">Por esse motivo, você deve incluir todo o código em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="bca9f-111">For that reason, you must include all your code in one file.</span></span>  

<span data-ttu-id="bca9f-112">Trechos de código são [][WikiBookmarklet] uma alternativa aos indicadores com a diferença de que trechos de código são executados apenas no DevTools e não se limitam ao tamanho permitido de uma URL.</span><span class="sxs-lookup"><span data-stu-id="bca9f-112">Snippets are an alternative to [bookmarklets][WikiBookmarklet] with the difference that Snippets only run in DevTools and are not limited to the allowed length of a URL.</span></span>  

<span data-ttu-id="bca9f-113">Usar trechos de código é uma excelente maneira de alterar algumas coisas em uma página da Web de terceiros.</span><span class="sxs-lookup"><span data-stu-id="bca9f-113">Using Snippets is an excellent way to change a few things in a third-party webpage.</span></span>  <span data-ttu-id="bca9f-114">As alterações de código em Trechos de Código são adicionadas à página da Web atual e são executados no mesmo contexto.</span><span class="sxs-lookup"><span data-stu-id="bca9f-114">Code changes in Snippets are added to the current webpage and run in the same context.</span></span>  <span data-ttu-id="bca9f-115">Para obter mais informações sobre como alterar o código existente de uma página da Web, navegue até [Substituições][DevtoolsJavascriptOverrides].</span><span class="sxs-lookup"><span data-stu-id="bca9f-115">For more information about changing the existing code of a webpage, navigate to [Overrides][DevtoolsJavascriptOverrides].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="bca9f-116">Por exemplo, na figura a seguir mostra a homepage DevTools à esquerda e algum código-fonte trecho à direita.</span><span class="sxs-lookup"><span data-stu-id="bca9f-116">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="O antes de executar o trecho" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         <span data-ttu-id="bca9f-118">A página da Web antes de executar o trecho de código</span><span class="sxs-lookup"><span data-stu-id="bca9f-118">The webpage before running the Snippet</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="bca9f-119">O código-fonte trecho da página da Web antes de executar o trecho.</span><span class="sxs-lookup"><span data-stu-id="bca9f-119">The Snippet source code from the webpage before running the Snippet.</span></span>  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

<span data-ttu-id="bca9f-120">Na figura a seguir, a página da Web é exibida após a execução do trecho de código.</span><span class="sxs-lookup"><span data-stu-id="bca9f-120">In the following figure, the webpage appears after running the Snippet.</span></span>  <span data-ttu-id="bca9f-121">A **Gaveta de Console** é exibida para exibir a mensagem que o trecho de código registra e o conteúdo da página da Web muda `Hello, Snippets!` completamente.</span><span class="sxs-lookup"><span data-stu-id="bca9f-121">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the webpage changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="A página da Web após a execução do trecho de código" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="bca9f-123">A página da Web após a execução do trecho de código</span><span class="sxs-lookup"><span data-stu-id="bca9f-123">The webpage after running the Snippet</span></span>  
:::image-end:::  

## <a name="open-the-snippets-tab"></a><span data-ttu-id="bca9f-124">Abra a guia Trechos de Código</span><span class="sxs-lookup"><span data-stu-id="bca9f-124">Open the Snippets tab</span></span>  

<span data-ttu-id="bca9f-125">A **guia Trechos de** Código, no painel **Navegador** à esquerda, lista seus trechos.</span><span class="sxs-lookup"><span data-stu-id="bca9f-125">The **Snippets** tab, in the **Navigator** pane on the left, lists your Snippets.</span></span>  <span data-ttu-id="bca9f-126">Quando você deseja editar um trecho, você precisa abri-lo na guia **Trechos.**</span><span class="sxs-lookup"><span data-stu-id="bca9f-126">When you want to edit a Snippet, you need to open it from the **Snippets** tab.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="A guia Trechos de Código" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="bca9f-128">A **guia Trechos de** Código</span><span class="sxs-lookup"><span data-stu-id="bca9f-128">The **Snippets** tab</span></span>  
:::image-end:::  

### <a name="open-the-snippets-tab-with-a-mouse"></a><span data-ttu-id="bca9f-129">Abra a guia Trechos de Código com um mouse</span><span class="sxs-lookup"><span data-stu-id="bca9f-129">Open the Snippets tab with a mouse</span></span>  

1.  <span data-ttu-id="bca9f-130">Escolha a **guia Fontes.**  A **ferramenta Sources** é exibida.</span><span class="sxs-lookup"><span data-stu-id="bca9f-130">Choose the **Sources** tab.  The **Sources** tool appears.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="A ferramenta Fontes com a guia Página aberta à esquerda" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="bca9f-132">A **ferramenta Fontes** com a guia **Página** aberta à esquerda</span><span class="sxs-lookup"><span data-stu-id="bca9f-132">The **Sources** tool with the **Page** tab open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bca9f-133">No painel **Navegador** (à esquerda), escolha a **guia Trechos.**  Para acessar a **opção Trechos** de Código, talvez seja necessário escolher **Mais guias** \( Mais ![ guias ](../media/more-tabs-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="bca9f-133">In the **Navigator** pane (on the left), choose the **Snippets** tab.  To access the **Snippets** option, you may need to choose **More tabs** \(![More tabs](../media/more-tabs-icon.msft.png)\).</span></span>  
    
### <a name="open-the-snippets-tab-with-the-command-menu"></a><span data-ttu-id="bca9f-134">Abra a guia Trechos de Código com o Menu de Comando</span><span class="sxs-lookup"><span data-stu-id="bca9f-134">Open the Snippets tab with the Command Menu</span></span>  

1.  <span data-ttu-id="bca9f-135">Selecione qualquer coisa no DevTools, para que o DevTools tenha foco.</span><span class="sxs-lookup"><span data-stu-id="bca9f-135">Select anything in DevTools, so that DevTools has focus.</span></span>  
1.  <span data-ttu-id="bca9f-136">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o Menu de Comando.</span><span class="sxs-lookup"><span data-stu-id="bca9f-136">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="bca9f-137">Digite `Snippets` , escolha Mostrar **Trechos de**Código e, em seguida, selecione para executar o `Enter` comando.</span><span class="sxs-lookup"><span data-stu-id="bca9f-137">Type `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="O comando Mostrar Trechos de Código" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="bca9f-139">O **comando Mostrar Trechos de** Código</span><span class="sxs-lookup"><span data-stu-id="bca9f-139">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <a name="create-snippets"></a><span data-ttu-id="bca9f-140">Criar trechos de código</span><span class="sxs-lookup"><span data-stu-id="bca9f-140">Create Snippets</span></span>  

### <a name="create-a-snippet-through-the-sources-tool"></a><span data-ttu-id="bca9f-141">Criar um trecho de código por meio da ferramenta Sources</span><span class="sxs-lookup"><span data-stu-id="bca9f-141">Create a Snippet through the Sources tool</span></span>  

1.  <span data-ttu-id="bca9f-142">[Abra a guia Trechos de Código](#open-the-snippets-tab).</span><span class="sxs-lookup"><span data-stu-id="bca9f-142">[Open the Snippets tab](#open-the-snippets-tab).</span></span>  
1.  <span data-ttu-id="bca9f-143">Escolha **Novo trecho**de código .</span><span class="sxs-lookup"><span data-stu-id="bca9f-143">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="bca9f-144">Insira um nome para o trecho de código e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="bca9f-144">Enter a name for your Snippet, and then select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Nomear um trecho" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="bca9f-146">Nomear um trecho</span><span class="sxs-lookup"><span data-stu-id="bca9f-146">Name a Snippet</span></span>  
    :::image-end:::  
    
### <a name="create-a-snippet-through-the-command-menu"></a><span data-ttu-id="bca9f-147">Criar um trecho de código por meio do Menu de Comando</span><span class="sxs-lookup"><span data-stu-id="bca9f-147">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="bca9f-148">Concentre seu cursor em algum lugar no DevTools.</span><span class="sxs-lookup"><span data-stu-id="bca9f-148">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="bca9f-149">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o Menu de Comando.</span><span class="sxs-lookup"><span data-stu-id="bca9f-149">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="bca9f-150">Digite `Snippet` , escolha Criar novo trecho de **código**e, em seguida, selecione para executar `Enter` o comando.</span><span class="sxs-lookup"><span data-stu-id="bca9f-150">Type `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="O comando para criar um novo trecho" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="bca9f-152">O comando para criar um novo trecho</span><span class="sxs-lookup"><span data-stu-id="bca9f-152">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="bca9f-153">Para renomear seu novo trecho de código com um nome personalizado, navegue até [Renomear Trechos de Código](#rename-snippets).</span><span class="sxs-lookup"><span data-stu-id="bca9f-153">To rename your new Snippet with a custom name, navigate to [Rename Snippets](#rename-snippets).</span></span>  

## <a name="edit-snippets"></a><span data-ttu-id="bca9f-154">Editar trechos</span><span class="sxs-lookup"><span data-stu-id="bca9f-154">Edit Snippets</span></span>  

1.  <span data-ttu-id="bca9f-155">[Abra a guia Trechos de Código](#open-the-snippets-tab).</span><span class="sxs-lookup"><span data-stu-id="bca9f-155">[Open the Snippets tab](#open-the-snippets-tab).</span></span>  
1.  <span data-ttu-id="bca9f-156">Na guia **Trechos** de Código, escolha o nome do trecho que você deseja editar.</span><span class="sxs-lookup"><span data-stu-id="bca9f-156">In the **Snippets** tab, choose the name of the Snippet that you want to edit.</span></span>  <span data-ttu-id="bca9f-157">Ele é aberto no **Editor de Código.**</span><span class="sxs-lookup"><span data-stu-id="bca9f-157">It opens in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="O Editor de Código" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="bca9f-159">O **Editor de Código**</span><span class="sxs-lookup"><span data-stu-id="bca9f-159">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bca9f-160">Use o **Editor de Código** para adicionar JavaScript ao seu trecho de código.</span><span class="sxs-lookup"><span data-stu-id="bca9f-160">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="bca9f-161">Quando um asterisco é exibido ao lado do nome do trecho de código, significa que você tem código não saved.</span><span class="sxs-lookup"><span data-stu-id="bca9f-161">When an asterisk appears next to the name of your Snippet, it means you have unsaved code.</span></span>  <span data-ttu-id="bca9f-162">Selecione `Control` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\) para salvar.</span><span class="sxs-lookup"><span data-stu-id="bca9f-162">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Um asterisco ao lado do nome trecho indica código não saved" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="bca9f-164">Um asterisco ao lado do nome trecho indica código não saved</span><span class="sxs-lookup"><span data-stu-id="bca9f-164">An asterisk next to the Snippet name indicates unsaved code</span></span>  
    :::image-end:::  
    
## <a name="run-snippets"></a><span data-ttu-id="bca9f-165">Executar trechos de código</span><span class="sxs-lookup"><span data-stu-id="bca9f-165">Run Snippets</span></span>  

### <a name="run-a-snippet-from-the-sources-tool"></a><span data-ttu-id="bca9f-166">Executar um trecho da ferramenta Sources</span><span class="sxs-lookup"><span data-stu-id="bca9f-166">Run a Snippet from the Sources tool</span></span>  

1.  <span data-ttu-id="bca9f-167">[Abra a guia Trechos de Código](#open-the-snippets-tab).</span><span class="sxs-lookup"><span data-stu-id="bca9f-167">[Open the Snippets tab](#open-the-snippets-tab).</span></span>  
1.  <span data-ttu-id="bca9f-168">Escolha o nome do trecho que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="bca9f-168">Choose the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="bca9f-169">O trecho é aberto no **Editor de Código.**</span><span class="sxs-lookup"><span data-stu-id="bca9f-169">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="bca9f-170">Escolha **Executar trecho de código** \( Executar trecho ![ ](../media/run-snippet-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="bca9f-170">Choose **Run snippet** \(![Run Snippet](../media/run-snippet-icon.msft.png)\).</span></span>
    
### <a name="run-a-snippet-with-the-command-menu"></a><span data-ttu-id="bca9f-171">Executar um trecho com o Menu de Comando</span><span class="sxs-lookup"><span data-stu-id="bca9f-171">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="bca9f-172">Concentre seu cursor em algum lugar no DevTools.</span><span class="sxs-lookup"><span data-stu-id="bca9f-172">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="bca9f-173">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o Menu de Comando.</span><span class="sxs-lookup"><span data-stu-id="bca9f-173">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="bca9f-174">Exclua o caractere e digite o caractere seguido pelo nome do `>` trecho que você deseja `!` executar.</span><span class="sxs-lookup"><span data-stu-id="bca9f-174">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Executando um trecho do Menu de Comando" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="bca9f-176">Executando um trecho do **Menu de Comando**</span><span class="sxs-lookup"><span data-stu-id="bca9f-176">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bca9f-177">Selecione `Enter` para executar o trecho.</span><span class="sxs-lookup"><span data-stu-id="bca9f-177">Select `Enter` to run the Snippet.</span></span>  

## <a name="rename-snippets"></a><span data-ttu-id="bca9f-178">Renomear trechos</span><span class="sxs-lookup"><span data-stu-id="bca9f-178">Rename Snippets</span></span>  

1.  <span data-ttu-id="bca9f-179">[Abra a guia Trechos de Código](#open-the-snippets-tab).</span><span class="sxs-lookup"><span data-stu-id="bca9f-179">[Open the Snippets tab](#open-the-snippets-tab).</span></span>  
1.  <span data-ttu-id="bca9f-180">Passe o mouse no nome do trecho, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Renomear**.</span><span class="sxs-lookup"><span data-stu-id="bca9f-180">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Rename**.</span></span>  
    
## <a name="delete-snippets"></a><span data-ttu-id="bca9f-181">Excluir trechos de código</span><span class="sxs-lookup"><span data-stu-id="bca9f-181">Delete Snippets</span></span>  

1.  <span data-ttu-id="bca9f-182">[Abra a guia Trechos de Código](#open-the-snippets-tab).</span><span class="sxs-lookup"><span data-stu-id="bca9f-182">[Open the Snippets tab](#open-the-snippets-tab).</span></span>  
1.  <span data-ttu-id="bca9f-183">Passe o mouse no nome do trecho, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Remover**.</span><span class="sxs-lookup"><span data-stu-id="bca9f-183">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Remove**.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="bca9f-184">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bca9f-184">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Visão geral do console | Microsoft Docs"  
[DevToolsSourcesTool]: ../sources/index.md "Visão geral da ferramenta Sources | Microsoft Docs"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Substitui | Microsoft Docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Scratchpad | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Wikipédia"  

> [!NOTE]
> <span data-ttu-id="bca9f-190">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bca9f-190">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="bca9f-191">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="bca9f-191">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="bca9f-193">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bca9f-193">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
