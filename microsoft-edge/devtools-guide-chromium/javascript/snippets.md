---
description: Trechos de código são scripts pequenos que você pode escrever e executar na ferramenta Sources do Microsoft Edge DevTools.  Você pode acessar e executar recursos de qualquer página da Web.  Quando você executa um trecho, ele é executado a partir do contexto da página da Web aberta no momento.
title: Executar trechos de javascript em qualquer página com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 779c3dcec66b6b5df3e38abe9ee458bca7dc0c45
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439420"
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

# <a name="run-snippets-of-javascript-on-any-webpage-with-microsoft-edge-devtools"></a><span data-ttu-id="b5806-106">Executar trechos de código do JavaScript em qualquer página da Web com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b5806-106">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="b5806-107">Se você estiver executando o mesmo código no [Console][DevtoolsConsoleIndex] repetidamente, considere salvar o código como um trecho.</span><span class="sxs-lookup"><span data-stu-id="b5806-107">If you are running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="b5806-108">Trechos de código são scripts que você escreveu na [ferramenta Fontes.][DevToolsSourcesTool]</span><span class="sxs-lookup"><span data-stu-id="b5806-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesTool] tool.</span></span>  <span data-ttu-id="b5806-109">Trechos de código têm acesso ao contexto JavaScript da página da Web e você pode executar trechos em qualquer página da Web.</span><span class="sxs-lookup"><span data-stu-id="b5806-109">Snippets have access to the JavaScript context of the webpage, and you may run snippets on any webpage.</span></span>  <span data-ttu-id="b5806-110">As configurações de segurança da maioria das páginas da Web bloqueiam o carregamento de outros scripts em Trechos de Código.</span><span class="sxs-lookup"><span data-stu-id="b5806-110">The security settings of most webpages block from loading other scripts in Snippets.</span></span>  <span data-ttu-id="b5806-111">Por esse motivo, você deve incluir todo o código em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b5806-111">For that reason, you must include all your code in one file.</span></span>  

<span data-ttu-id="b5806-112">Trechos de código são [][WikiBookmarklet] uma alternativa aos indicadores com a diferença de que trechos de código são executados apenas no DevTools e não se limitam ao tamanho permitido de uma URL.</span><span class="sxs-lookup"><span data-stu-id="b5806-112">Snippets are an alternative to [bookmarklets][WikiBookmarklet] with the difference that Snippets only run in DevTools and are not limited to the allowed length of a URL.</span></span>  

<span data-ttu-id="b5806-113">Usar trechos de código é uma excelente maneira de alterar algumas coisas em uma página da Web de terceiros.</span><span class="sxs-lookup"><span data-stu-id="b5806-113">Using Snippets is an excellent way to change a few things in a third-party webpage.</span></span>  <span data-ttu-id="b5806-114">As alterações de código em Trechos de Código são adicionadas à página da Web atual e são executados no mesmo contexto.</span><span class="sxs-lookup"><span data-stu-id="b5806-114">Code changes in Snippets are added to the current webpage and run in the same context.</span></span>  <span data-ttu-id="b5806-115">Para obter mais informações sobre como alterar o código existente de uma página da Web, navegue até [Substituições][DevtoolsJavascriptOverrides].</span><span class="sxs-lookup"><span data-stu-id="b5806-115">For more information about changing the existing code of a webpage, navigate to [Overrides][DevtoolsJavascriptOverrides].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b5806-116">Por exemplo, na figura a seguir mostra a homepage DevTools à esquerda e algum código-fonte trecho à direita.</span><span class="sxs-lookup"><span data-stu-id="b5806-116">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="O antes de executar o trecho" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         <span data-ttu-id="b5806-118">A página da Web antes de executar o trecho de código</span><span class="sxs-lookup"><span data-stu-id="b5806-118">The webpage before running the Snippet</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="b5806-119">O código-fonte trecho da página da Web antes de executar o trecho.</span><span class="sxs-lookup"><span data-stu-id="b5806-119">The Snippet source code from the webpage before running the Snippet.</span></span>  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

<span data-ttu-id="b5806-120">Na figura a seguir, a página da Web é exibida após a execução do trecho de código.</span><span class="sxs-lookup"><span data-stu-id="b5806-120">In the following figure, the webpage appears after running the Snippet.</span></span>  <span data-ttu-id="b5806-121">A **Gaveta de Console** é exibida para exibir a mensagem que o trecho de código registra e o conteúdo da página da Web muda `Hello, Snippets!` completamente.</span><span class="sxs-lookup"><span data-stu-id="b5806-121">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the webpage changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="A página da Web após a execução do trecho de código" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="b5806-123">A página da Web após a execução do trecho de código</span><span class="sxs-lookup"><span data-stu-id="b5806-123">The webpage after running the Snippet</span></span>  
:::image-end:::  

## <a name="open-the-snippets-pane"></a><span data-ttu-id="b5806-124">Abra o painel Trechos de Código</span><span class="sxs-lookup"><span data-stu-id="b5806-124">Open the Snippets pane</span></span>  

<span data-ttu-id="b5806-125">O **painel Trechos de** Código lista seus trechos.</span><span class="sxs-lookup"><span data-stu-id="b5806-125">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="b5806-126">Quando você deseja editar um trecho, você precisa abri-lo do painel **Trechos** de Código.</span><span class="sxs-lookup"><span data-stu-id="b5806-126">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="O painel Trechos de Código" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="b5806-128">O **painel Trechos** de Código</span><span class="sxs-lookup"><span data-stu-id="b5806-128">The **Snippets** pane</span></span>  
:::image-end:::  

### <a name="open-the-snippets-pane-with-a-mouse"></a><span data-ttu-id="b5806-129">Abra o painel Trechos de Código com um mouse</span><span class="sxs-lookup"><span data-stu-id="b5806-129">Open the Snippets pane with a mouse</span></span>  

1.  <span data-ttu-id="b5806-130">Escolha a **guia Fontes** para abrir a **ferramenta Fontes.**</span><span class="sxs-lookup"><span data-stu-id="b5806-130">Choose the **Sources** tab to open the **Sources** tool.</span></span>  <span data-ttu-id="b5806-131">O **painel Página** geralmente é aberto por padrão.</span><span class="sxs-lookup"><span data-stu-id="b5806-131">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="A ferramenta Sources com o painel Página aberta à esquerda" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="b5806-133">A **ferramenta Sources** com o painel **Página** aberta à esquerda</span><span class="sxs-lookup"><span data-stu-id="b5806-133">The **Sources** tool with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b5806-134">Escolha a **guia Trechos de** Código para abrir o painel **Trechos** de Código.</span><span class="sxs-lookup"><span data-stu-id="b5806-134">Choose the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="b5806-135">Talvez seja necessário escolher **Mais Guias** \( Mais ![ Guias ](../media/more-tabs-icon.msft.png) \) para acessar a opção **Trechos** de Código.</span><span class="sxs-lookup"><span data-stu-id="b5806-135">You may need to choose **More Tabs** \(![More Tabs](../media/more-tabs-icon.msft.png)\) to access the **Snippets** option.</span></span>  
    
### <a name="open-the-snippets-pane-with-the-command-menu"></a><span data-ttu-id="b5806-136">Abra o painel Trechos de Código com o Menu de Comando</span><span class="sxs-lookup"><span data-stu-id="b5806-136">Open the Snippets pane with the Command Menu</span></span>  

1.  <span data-ttu-id="b5806-137">Concentre seu cursor em algum lugar no DevTools.</span><span class="sxs-lookup"><span data-stu-id="b5806-137">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="b5806-138">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o Menu de Comando.</span><span class="sxs-lookup"><span data-stu-id="b5806-138">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="b5806-139">Digite `Snippets` , escolha Mostrar **Trechos de**Código e, em seguida, selecione para executar o `Enter` comando.</span><span class="sxs-lookup"><span data-stu-id="b5806-139">Type `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="O comando Mostrar Trechos de Código" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="b5806-141">O **comando Mostrar Trechos de** Código</span><span class="sxs-lookup"><span data-stu-id="b5806-141">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <a name="create-snippets"></a><span data-ttu-id="b5806-142">Criar trechos de código</span><span class="sxs-lookup"><span data-stu-id="b5806-142">Create Snippets</span></span>  

### <a name="create-a-snippet-through-the-sources-panel"></a><span data-ttu-id="b5806-143">Criar um trecho por meio do painel Fontes</span><span class="sxs-lookup"><span data-stu-id="b5806-143">Create a Snippet through the Sources panel</span></span>  

1.  <span data-ttu-id="b5806-144">[Abra o **painel Trechos de** Código.](#open-the-snippets-pane)</span><span class="sxs-lookup"><span data-stu-id="b5806-144">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="b5806-145">Escolha **Novo trecho**de código .</span><span class="sxs-lookup"><span data-stu-id="b5806-145">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="b5806-146">Insira um nome para o trecho de código e selecione `Enter` salvar.</span><span class="sxs-lookup"><span data-stu-id="b5806-146">Enter a name for your Snippet then select `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Nomear um trecho" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="b5806-148">Nomear um trecho</span><span class="sxs-lookup"><span data-stu-id="b5806-148">Name a Snippet</span></span>  
    :::image-end:::  
    
### <a name="create-a-snippet-through-the-command-menu"></a><span data-ttu-id="b5806-149">Criar um trecho de código por meio do Menu de Comando</span><span class="sxs-lookup"><span data-stu-id="b5806-149">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="b5806-150">Concentre seu cursor em algum lugar no DevTools.</span><span class="sxs-lookup"><span data-stu-id="b5806-150">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="b5806-151">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o Menu de Comando.</span><span class="sxs-lookup"><span data-stu-id="b5806-151">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="b5806-152">Digite `Snippet` , escolha Criar novo trecho de **código**e, em seguida, selecione para executar `Enter` o comando.</span><span class="sxs-lookup"><span data-stu-id="b5806-152">Type `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="O comando para criar um novo trecho" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="b5806-154">O comando para criar um novo trecho</span><span class="sxs-lookup"><span data-stu-id="b5806-154">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b5806-155">Para renomear seu novo trecho de código com um nome personalizado, navegue até [Renomear Trechos de Código](#rename-snippets).</span><span class="sxs-lookup"><span data-stu-id="b5806-155">To rename your new Snippet with a custom name, navigate to [Rename Snippets](#rename-snippets).</span></span>  

## <a name="edit-snippets"></a><span data-ttu-id="b5806-156">Editar trechos</span><span class="sxs-lookup"><span data-stu-id="b5806-156">Edit Snippets</span></span>  

1.  <span data-ttu-id="b5806-157">[Abra o **painel Trechos de** Código.](#open-the-snippets-pane)</span><span class="sxs-lookup"><span data-stu-id="b5806-157">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="b5806-158">No painel **Trechos** de Código, escolha o nome do trecho que você deseja editar.</span><span class="sxs-lookup"><span data-stu-id="b5806-158">In the **Snippets** pane, choose the name of the Snippet that you want to edit.</span></span>  <span data-ttu-id="b5806-159">Ele é aberto no **Editor de Código.**</span><span class="sxs-lookup"><span data-stu-id="b5806-159">It opens in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="O Editor de Código" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="b5806-161">O **Editor de Código**</span><span class="sxs-lookup"><span data-stu-id="b5806-161">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b5806-162">Use o **Editor de Código** para adicionar JavaScript ao seu trecho de código.</span><span class="sxs-lookup"><span data-stu-id="b5806-162">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="b5806-163">Quando um asterisco é exibido ao lado do nome do trecho de código, significa que você tem código não saved.</span><span class="sxs-lookup"><span data-stu-id="b5806-163">When an asterisk appears next to the name of your Snippet, it means you have unsaved code.</span></span>  <span data-ttu-id="b5806-164">Selecione `Control` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\) para salvar.</span><span class="sxs-lookup"><span data-stu-id="b5806-164">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Um asterisco ao lado do nome trecho indica código não saved" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="b5806-166">Um asterisco ao lado do nome trecho indica código não saved</span><span class="sxs-lookup"><span data-stu-id="b5806-166">An asterisk next to the Snippet name indicates unsaved code</span></span>  
    :::image-end:::  
    
## <a name="run-snippets"></a><span data-ttu-id="b5806-167">Executar trechos de código</span><span class="sxs-lookup"><span data-stu-id="b5806-167">Run Snippets</span></span>  

### <a name="run-a-snippet-from-the-sources-panel"></a><span data-ttu-id="b5806-168">Executar um trecho do painel Fontes</span><span class="sxs-lookup"><span data-stu-id="b5806-168">Run a Snippet from the Sources panel</span></span>  

1.  <span data-ttu-id="b5806-169">[Abra o **painel Trechos de** Código.](#open-the-snippets-pane)</span><span class="sxs-lookup"><span data-stu-id="b5806-169">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="b5806-170">Escolha o nome do trecho que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="b5806-170">Choose the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="b5806-171">O trecho é aberto no **Editor de Código.**</span><span class="sxs-lookup"><span data-stu-id="b5806-171">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="b5806-172">Escolha **Executar Trecho de Código** \( Executar Trecho \) ou selecione ![ ](../media/run-snippet-icon.msft.png) `Control` + `Enter` \(Windows, Linux\) ou `Command` + `Enter` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="b5806-172">Choose **Run Snippet** \(![Run Snippet](../media/run-snippet-icon.msft.png)\), or select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <a name="run-a-snippet-with-the-command-menu"></a><span data-ttu-id="b5806-173">Executar um trecho com o Menu de Comando</span><span class="sxs-lookup"><span data-stu-id="b5806-173">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="b5806-174">Concentre seu cursor em algum lugar no DevTools.</span><span class="sxs-lookup"><span data-stu-id="b5806-174">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="b5806-175">Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o Menu de Comando.</span><span class="sxs-lookup"><span data-stu-id="b5806-175">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="b5806-176">Exclua o caractere e digite o caractere seguido pelo nome do `>` trecho que você deseja `!` executar.</span><span class="sxs-lookup"><span data-stu-id="b5806-176">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Executando um trecho do Menu de Comando" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="b5806-178">Executando um trecho do **Menu de Comando**</span><span class="sxs-lookup"><span data-stu-id="b5806-178">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b5806-179">Selecione `Enter` para executar o trecho.</span><span class="sxs-lookup"><span data-stu-id="b5806-179">Select `Enter` to run the Snippet.</span></span>  

## <a name="rename-snippets"></a><span data-ttu-id="b5806-180">Renomear trechos</span><span class="sxs-lookup"><span data-stu-id="b5806-180">Rename Snippets</span></span>  

1.  <span data-ttu-id="b5806-181">[Abra o **painel Trechos de** Código.](#open-the-snippets-pane)</span><span class="sxs-lookup"><span data-stu-id="b5806-181">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="b5806-182">Passe o mouse no nome do trecho, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Renomear**.</span><span class="sxs-lookup"><span data-stu-id="b5806-182">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Rename**.</span></span>  
    
## <a name="delete-snippets"></a><span data-ttu-id="b5806-183">Excluir trechos de código</span><span class="sxs-lookup"><span data-stu-id="b5806-183">Delete Snippets</span></span>  

1.  <span data-ttu-id="b5806-184">[Abra o **painel Trechos de** Código.](#open-the-snippets-pane)</span><span class="sxs-lookup"><span data-stu-id="b5806-184">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="b5806-185">Passe o mouse no nome do trecho, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Remover**.</span><span class="sxs-lookup"><span data-stu-id="b5806-185">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Remove**.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="b5806-186">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b5806-186">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Visão geral do console | Microsoft Docs"  
[DevToolsSourcesTool]: ../sources/index.md "Visão geral da ferramenta Sources | Microsoft Docs"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Substitui | Microsoft Docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Scratchpad | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Wikipédia"  

> [!NOTE]
> <span data-ttu-id="b5806-192">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b5806-192">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b5806-193">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="b5806-193">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b5806-195">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b5806-195">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
