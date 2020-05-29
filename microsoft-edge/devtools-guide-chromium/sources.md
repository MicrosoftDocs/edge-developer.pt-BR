---
title: Visão geral do painel fontes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: c61d1bda030ce729b0b217b95a9143508d1f51f8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601905"
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
   limitations under the License. -->






# <span data-ttu-id="9d92d-103">Visão geral do painel fontes</span><span class="sxs-lookup"><span data-stu-id="9d92d-103">Sources Panel Overview</span></span> 



<span data-ttu-id="9d92d-104">Use o painel **fontes** do Microsoft Edge devtools para:</span><span class="sxs-lookup"><span data-stu-id="9d92d-104">Use the Microsoft Edge DevTools **Sources** panel to:</span></span>

*   <span data-ttu-id="9d92d-105">[Exibir arquivos](#view-files).</span><span class="sxs-lookup"><span data-stu-id="9d92d-105">[View files](#view-files).</span></span>  
*   <span data-ttu-id="9d92d-106">[Editar CSS e JavaScript](#edit-css-and-javascript).</span><span class="sxs-lookup"><span data-stu-id="9d92d-106">[Edit CSS and JavaScript](#edit-css-and-javascript).</span></span>  
*   <span data-ttu-id="9d92d-107">[Crie e salve **trechos de código** JavaScript](#create-save-and-run-snippets), que você pode executar em qualquer página.</span><span class="sxs-lookup"><span data-stu-id="9d92d-107">[Create and save **Snippets** of JavaScript](#create-save-and-run-snippets), which you may run on any page.</span></span>  <span data-ttu-id="9d92d-108">Os **trechos de código** são semelhantes a bookmarklets.</span><span class="sxs-lookup"><span data-stu-id="9d92d-108">**Snippets** are similar to bookmarklets.</span></span>  
*   <span data-ttu-id="9d92d-109">[Depurar JavaScript](#debug-javascript).</span><span class="sxs-lookup"><span data-stu-id="9d92d-109">[Debug JavaScript](#debug-javascript).</span></span>  
*   <span data-ttu-id="9d92d-110">[Configure um espaço de trabalho](#set-up-a-workspace)para que as alterações feitas no devtools sejam salvas no código do seu sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9d92d-110">[Set up a Workspace](#set-up-a-workspace), so that changes you make in DevTools get saved to the code on your file system.</span></span>  

## <span data-ttu-id="9d92d-111">Exibir arquivos</span><span class="sxs-lookup"><span data-stu-id="9d92d-111">View files</span></span> 

<span data-ttu-id="9d92d-112">Use o painel de **página** para exibir todos os recursos que a página carregou.</span><span class="sxs-lookup"><span data-stu-id="9d92d-112">Use the **Page** pane to view all of the resources that the page has loaded.</span></span>

> ##### <span data-ttu-id="9d92d-113">Figura 1</span><span class="sxs-lookup"><span data-stu-id="9d92d-113">Figure 1</span></span>  
> <span data-ttu-id="9d92d-114">Painel de **página**</span><span class="sxs-lookup"><span data-stu-id="9d92d-114">The **Page** pane</span></span>  
> ![Figura 1: o painel da página][ImageSourcesPagePane]  

<span data-ttu-id="9d92d-116">Como o painel da **página** está organizado:</span><span class="sxs-lookup"><span data-stu-id="9d92d-116">How the **Page** pane is organized:</span></span>  
*   <span data-ttu-id="9d92d-117">O nível superior, como `top` na [**Figura 1**](#figure-1), representa um [quadro HTML][W3CHtml4Frames].</span><span class="sxs-lookup"><span data-stu-id="9d92d-117">The top-level, such as `top` in [**Figure 1**](#figure-1), represents an [HTML frame][W3CHtml4Frames].</span></span>  <span data-ttu-id="9d92d-118">Localizar `top` em cada página que você visita.</span><span class="sxs-lookup"><span data-stu-id="9d92d-118">Find `top` on every page that you visit.</span></span> `top` <span data-ttu-id="9d92d-119">representa o quadro do documento principal.</span><span class="sxs-lookup"><span data-stu-id="9d92d-119">represents the main document frame.</span></span>  
*   <span data-ttu-id="9d92d-120">O segundo nível, como `docs.microsoft.com` na [**Figura 1**](#figure-1), representa uma [origem][HtmlstandardOrigin].</span><span class="sxs-lookup"><span data-stu-id="9d92d-120">The second-level, such as `docs.microsoft.com` in [**Figure 1**](#figure-1), represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="9d92d-121">O terceiro nível, o quarto nível e assim por diante, representam diretórios e recursos que foram carregados dessa origem.</span><span class="sxs-lookup"><span data-stu-id="9d92d-121">The third-level, fourth-level, and so on, represent directories and resources that were loaded from that origin.</span></span>  <span data-ttu-id="9d92d-122">Por exemplo, na [**Figura 1**](#figure-1) , o caminho completo do recurso `devtools-guide-chromium` é</span><span class="sxs-lookup"><span data-stu-id="9d92d-122">For example, in [**Figure 1**](#figure-1) the full path to the resource `devtools-guide-chromium` is</span></span> `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  

<span data-ttu-id="9d92d-123">Clique em um arquivo no painel da **página** para exibir o conteúdo no painel do **Editor** .</span><span class="sxs-lookup"><span data-stu-id="9d92d-123">Click a file in the **Page** pane to view the contents in the **Editor** pane.</span></span>  <span data-ttu-id="9d92d-124">Você pode ver qualquer tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="9d92d-124">You may view any type of file.</span></span> <span data-ttu-id="9d92d-125">Para imagens, você vê uma visualização da imagem.</span><span class="sxs-lookup"><span data-stu-id="9d92d-125">For images, you see a preview of the image.</span></span>  

> ##### <span data-ttu-id="9d92d-126">Figura 2</span><span class="sxs-lookup"><span data-stu-id="9d92d-126">Figure 2</span></span>  
> <span data-ttu-id="9d92d-127">Exibir o conteúdo do `a4d10f71.index-docs.js` painel do **Editor**</span><span class="sxs-lookup"><span data-stu-id="9d92d-127">Viewing the contents of `a4d10f71.index-docs.js` in the **Editor** pane</span></span>  
> ![Figura 2.][ImageSourcesEditorPane]  

## <span data-ttu-id="9d92d-130">Editar CSS e JavaScript</span><span class="sxs-lookup"><span data-stu-id="9d92d-130">Edit CSS and JavaScript</span></span> 

<span data-ttu-id="9d92d-131">Use o painel **Editor** para editar CSS e JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9d92d-131">Use the **Editor** pane to edit CSS and JavaScript.</span></span>  <span data-ttu-id="9d92d-132">O DevTools atualiza a página para executar seu novo código.</span><span class="sxs-lookup"><span data-stu-id="9d92d-132">DevTools updates the page to run your new code.</span></span> <span data-ttu-id="9d92d-133">Por exemplo, se você editar um arquivo CSS, adicione a regra de estilo abaixo:</span><span class="sxs-lookup"><span data-stu-id="9d92d-133">For example, if you edit a CSS file by adding the style rule below:</span></span>

```css
.metadata.page-metadata {
    color: red;
}
```

<span data-ttu-id="9d92d-134">Você verá que a alteração entrará em vigor imediatamente.</span><span class="sxs-lookup"><span data-stu-id="9d92d-134">You should see that change take effect immediately.</span></span>

> ##### <span data-ttu-id="9d92d-135">Figura 3</span><span class="sxs-lookup"><span data-stu-id="9d92d-135">Figure 3</span></span>  
> <span data-ttu-id="9d92d-136">Editando CSS no painel do **Editor** para alterar a cor do texto do subtítulo para vermelho</span><span class="sxs-lookup"><span data-stu-id="9d92d-136">Editing CSS in the **Editor** pane to change the text color of the subtitle to red</span></span>  
> ![Figura 3.][ImageEditCSS]  

<span data-ttu-id="9d92d-139">As alterações de CSS entram em vigor imediatamente, não é necessário salvar.</span><span class="sxs-lookup"><span data-stu-id="9d92d-139">CSS changes take effect immediately, no save needed.</span></span> <span data-ttu-id="9d92d-140">Para que as alterações de JavaScript sejam efetivadas, pressione `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="9d92d-140">For JavaScript changes to take effect, press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\).</span></span> <span data-ttu-id="9d92d-141">O DevTools não executa novamente um script, portanto, as únicas alterações de JavaScript que entram em vigor são aquelas que você faz dentro de funções.</span><span class="sxs-lookup"><span data-stu-id="9d92d-141">DevTools does not re-run a script, so the only JavaScript changes that take effect are those that you make inside of functions.</span></span>  <span data-ttu-id="9d92d-142">Por exemplo, na [**Figura 4**](#figure-4) , observe como não `console.log('A')` funciona, enquanto `console.log('B')` o faz.</span><span class="sxs-lookup"><span data-stu-id="9d92d-142">For example, in [**Figure 4**](#figure-4) note how `console.log('A')` does not run, whereas `console.log('B')` does.</span></span> <span data-ttu-id="9d92d-143">Se o DevTools reexecutar o script inteiro depois de fazer a alteração, o texto `A` teria sido registrado no **console**.</span><span class="sxs-lookup"><span data-stu-id="9d92d-143">If DevTools re-ran the entire script after making the change, then the text `A` would have been logged to the **Console**.</span></span>  

> ##### <span data-ttu-id="9d92d-144">Figura 4</span><span class="sxs-lookup"><span data-stu-id="9d92d-144">Figure 4</span></span>  
> <span data-ttu-id="9d92d-145">Edição de JavaScript no painel do **Editor**</span><span class="sxs-lookup"><span data-stu-id="9d92d-145">Editing JavaScript in the **Editor** pane</span></span>  
> ![Figura 4.][ImageEditJS]  

<span data-ttu-id="9d92d-148">DevTools apagará as alterações de CSS e JavaScript quando você recarregar a página.</span><span class="sxs-lookup"><span data-stu-id="9d92d-148">DevTools erases your CSS and JavaScript changes when you reload the page.</span></span> <span data-ttu-id="9d92d-149">Consulte [configurar um espaço de trabalho](#set-up-a-workspace) para saber como salvar as alterações no seu sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9d92d-149">See [Set up a Workspace](#set-up-a-workspace) to learn how to save the changes to your file system.</span></span>  

## <span data-ttu-id="9d92d-150">Criar, salvar e executar Snippets</span><span class="sxs-lookup"><span data-stu-id="9d92d-150">Create, save, and run Snippets</span></span> 

<span data-ttu-id="9d92d-151">Trechos de código são scripts que você pode executar em qualquer página.</span><span class="sxs-lookup"><span data-stu-id="9d92d-151">Snippets are scripts which you may run on any page.</span></span> <span data-ttu-id="9d92d-152">Imagine que você digite repetidamente o código a seguir no **console**para inserir a biblioteca jQuery em uma página, para que você possa executar comandos do jQuery a partir do **console**:</span><span class="sxs-lookup"><span data-stu-id="9d92d-152">Imagine that you repeatedly type out the following code in the **Console**, in order to insert the jQuery library into a page, so that you may run jQuery commands from the **Console**:</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="9d92d-153">Em vez disso, você pode salvar esse código em um **snippet** e executá-lo com alguns cliques de botão, sempre que precisar.</span><span class="sxs-lookup"><span data-stu-id="9d92d-153">Instead, you may save this code in a **Snippet** and run it with a couple of button clicks, any time you need it.</span></span>  <span data-ttu-id="9d92d-154">DevTools salva o **trecho** em seu sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9d92d-154">DevTools saves the **Snippet** to your file system.</span></span>  

> ##### <span data-ttu-id="9d92d-155">Figura 5</span><span class="sxs-lookup"><span data-stu-id="9d92d-155">Figure 5</span></span>  
> <span data-ttu-id="9d92d-156">Um **trecho** que insere a biblioteca jQuery em uma página</span><span class="sxs-lookup"><span data-stu-id="9d92d-156">A **Snippet** that inserts the jQuery library into a page</span></span>  
> ![Figura 5.][ImageSnippet]  

<span data-ttu-id="9d92d-159">Para executar um **snippet**:</span><span class="sxs-lookup"><span data-stu-id="9d92d-159">To run a **Snippet**:</span></span>

*   <span data-ttu-id="9d92d-160">Abra o arquivo usando o painel **Snippets** e clique em **executar** ![ o botão executar ][ImageRunIcon] .</span><span class="sxs-lookup"><span data-stu-id="9d92d-160">Open the file via the **Snippets** pane, and click **Run** ![The Run button][ImageRunIcon].</span></span>  
*   <span data-ttu-id="9d92d-161">Abra o **[menu de comando][DevtoolsGuideChromiumCommandMenuIndex]**, exclua o `>` caractere, digite `!` , digite o nome do seu **snippet**e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="9d92d-161">Open the **[Command Menu][DevtoolsGuideChromiumCommandMenuIndex]**, delete the `>` character, type `!`, type the name of your **Snippet**, then press `Enter`.</span></span>  

<span data-ttu-id="9d92d-162">Consulte [executar trechos de código em qualquer página][DevtoolsGuideChromiumJavascriptSnippets] para saber mais.</span><span class="sxs-lookup"><span data-stu-id="9d92d-162">See [Run Snippets Of Code From Any Page][DevtoolsGuideChromiumJavascriptSnippets] to learn more.</span></span>


## <span data-ttu-id="9d92d-163">Depurar JavaScript</span><span class="sxs-lookup"><span data-stu-id="9d92d-163">Debug JavaScript</span></span> 

<span data-ttu-id="9d92d-164">Em vez de usar `console.log()` para inferir onde o JavaScript está errado, considere usar as ferramentas de depuração do Microsoft Edge devtools, em vez disso.</span><span class="sxs-lookup"><span data-stu-id="9d92d-164">Rather than using `console.log()` to infer where your JavaScript is going wrong, consider using the Microsoft Edge DevTools debugging tools, instead.</span></span> <span data-ttu-id="9d92d-165">A ideia geral é definir um ponto de interrupção, que é uma interrupção intencional em seu código e, em seguida, percorrer o tempo de execução do seu código, uma linha por vez.</span><span class="sxs-lookup"><span data-stu-id="9d92d-165">The general idea is to set a breakpoint, which is an intentional stopping place in your code, and then step through the runtime of your code, one line at a time.</span></span> <span data-ttu-id="9d92d-166">Ao percorrer o código, você pode visualizar e alterar os valores de todas as propriedades e variáveis definidas atualmente, executar JavaScript no **console**e muito mais.</span><span class="sxs-lookup"><span data-stu-id="9d92d-166">As you step through the code, you may view and change the values of all currently-defined properties and variables, run JavaScript in the **Console**, and more.</span></span>

<span data-ttu-id="9d92d-167">Consulte [introdução à depuração de JavaScript][DevtoolsGuideChromiumJavascriptIndex] para aprender as noções básicas de depuração no devtools.</span><span class="sxs-lookup"><span data-stu-id="9d92d-167">See [Get Started With Debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] to learn the basics of debugging in DevTools.</span></span>

> ##### <span data-ttu-id="9d92d-168">Figura 6</span><span class="sxs-lookup"><span data-stu-id="9d92d-168">Figure 6</span></span>  
> <span data-ttu-id="9d92d-169">Depuração de JavaScript</span><span class="sxs-lookup"><span data-stu-id="9d92d-169">Debugging JavaScript</span></span>  
> ![Figura 6.][ImageDebugging]  

## <span data-ttu-id="9d92d-172">Configurar um espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="9d92d-172">Set up a Workspace</span></span> 

<span data-ttu-id="9d92d-173">Por padrão, quando você edita um arquivo no painel **fontes** , essas alterações são perdidas quando você recarrega a página.</span><span class="sxs-lookup"><span data-stu-id="9d92d-173">By default, when you edit a file in the **Sources** panel, those changes are lost when you reload the page.</span></span>  <span data-ttu-id="9d92d-174">Os **espaços de trabalho** permitem salvar as alterações feitas no devtools em seu sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="9d92d-174">**Workspaces** enable you to save the changes that you make in DevTools to your file system.</span></span>  <span data-ttu-id="9d92d-175">Basicamente, isso permite que você use DevTools como seu editor de código.</span><span class="sxs-lookup"><span data-stu-id="9d92d-175">Essentially, this lets you use DevTools as your code editor.</span></span>

<span data-ttu-id="9d92d-176">Veja [Editar arquivos com espaços de trabalho][DevtoolsGuideChromiumWorkspacesIndex] para começar.</span><span class="sxs-lookup"><span data-stu-id="9d92d-176">See [Edit Files With Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to get started.</span></span>

 



<!-- image links -->  

[ImageRunIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSourcesPagePane]: /microsoft-edge/devtools-guide-chromium/media/sources-page-pane.msft.png "Figura 1: o painel da página"  
[ImageSourcesEditorPane]: /microsoft-edge/devtools-guide-chromium/media/sources-editor-pane.msft.png "Figura 2: exibindo o conteúdo de a4d10f71. index-docs. js no painel do editor"  
[ImageEditCSS]: /microsoft-edge/devtools-guide-chromium/media/edit-css.msft.png "Figura 3: editando CSS no painel do editor para alterar a cor do texto do subtítulo para vermelho"  
[ImageEditJS]: /microsoft-edge/devtools-guide-chromium/media/edit-js.msft.png "Figura 4: edição de JavaScript no painel do editor"  
[ImageSnippet]: /microsoft-edge/devtools-guide-chromium/media/snippet.msft.png "Figura 5: um snippet que insere a biblioteca jQuery em uma página"  
[ImageDebugging]: /microsoft-edge/devtools-guide-chromium/media/debugging.msft.png "Figura 6: depuração de JavaScript"  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando do Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptIndex]: /microsoft-edge/devtools-guide-chromium/javascript/index "Introdução à depuração de JavaScript no Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptSnippets]: /microsoft-edge/devtools-guide-chromium/javascript/snippets "Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools"  
[DevtoolsGuideChromiumWorkspacesIndex]: /microsoft-edge/devtools-guide-chromium/workspaces/index "Editar arquivos com espaços de trabalho"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origem-padrão HTML"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Quadros | W3C"  

> [!NOTE]
> <span data-ttu-id="9d92d-189">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="9d92d-189">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9d92d-190">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/sources) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="9d92d-190">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9d92d-192">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9d92d-192">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
