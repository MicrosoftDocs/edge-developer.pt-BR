---
description: Exiba e edite arquivos, crie Snippets, depure o JavaScript e configure os espaços de trabalho no painel fontes do Microsoft Edge DevTools.
title: Visão geral do Painel Fontes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 029693ba27665a556446f4349c1517c53ff39b02
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993538"
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







# <span data-ttu-id="bf21b-104">Visão geral do painel fontes</span><span class="sxs-lookup"><span data-stu-id="bf21b-104">Sources panel overview</span></span> 



<span data-ttu-id="bf21b-105">Use o painel **fontes** devtools do Microsoft Edge para executar as ações de folowing.</span><span class="sxs-lookup"><span data-stu-id="bf21b-105">Use the Microsoft Edge DevTools **Sources** panel to perform the folowing actions.</span></span>  

*   <span data-ttu-id="bf21b-106">[Exibir arquivos](#view-files).</span><span class="sxs-lookup"><span data-stu-id="bf21b-106">[View files](#view-files).</span></span>  
*   <span data-ttu-id="bf21b-107">[Editar CSS e JavaScript](#edit-css-and-javascript).</span><span class="sxs-lookup"><span data-stu-id="bf21b-107">[Edit CSS and JavaScript](#edit-css-and-javascript).</span></span>  
*   <span data-ttu-id="bf21b-108">[Crie e salve **trechos de código** JavaScript](#create-save-and-run-snippets), que você pode executar em qualquer página.</span><span class="sxs-lookup"><span data-stu-id="bf21b-108">[Create and save **Snippets** of JavaScript](#create-save-and-run-snippets), which you may run on any page.</span></span>  <span data-ttu-id="bf21b-109">Os **trechos de código** são semelhantes a bookmarklets.</span><span class="sxs-lookup"><span data-stu-id="bf21b-109">**Snippets** are similar to bookmarklets.</span></span>  
*   <span data-ttu-id="bf21b-110">[Depurar JavaScript](#debug-javascript).</span><span class="sxs-lookup"><span data-stu-id="bf21b-110">[Debug JavaScript](#debug-javascript).</span></span>  
*   <span data-ttu-id="bf21b-111">[Configure um espaço de trabalho](#set-up-a-workspace)para que as alterações feitas no devtools sejam salvas no código do seu sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="bf21b-111">[Set up a Workspace](#set-up-a-workspace), so that changes you make in DevTools get saved to the code on your file system.</span></span>  
    
## <span data-ttu-id="bf21b-112">Exibir arquivos</span><span class="sxs-lookup"><span data-stu-id="bf21b-112">View files</span></span> 

<span data-ttu-id="bf21b-113">Use o painel de **página** para exibir todos os recursos que a página carregou.</span><span class="sxs-lookup"><span data-stu-id="bf21b-113">Use the **Page** pane to view all of the resources that the page has loaded.</span></span>

:::image type="complex" source="./media/sources-page-pane.msft.png" alt-text="Painel de página" lightbox="./media/sources-page-pane.msft.png":::
   <span data-ttu-id="bf21b-115">Painel de **página**</span><span class="sxs-lookup"><span data-stu-id="bf21b-115">The **Page** pane</span></span>  
:::image-end:::  

<span data-ttu-id="bf21b-116">Como o painel da **página** está organizado:</span><span class="sxs-lookup"><span data-stu-id="bf21b-116">How the **Page** pane is organized:</span></span>  
*   <span data-ttu-id="bf21b-117">O nível superior, como `top` na figura anterior, representa um [quadro HTML][W3CHtml4Frames].</span><span class="sxs-lookup"><span data-stu-id="bf21b-117">The top-level, such as `top` in the previous figure, represents an [HTML frame][W3CHtml4Frames].</span></span>  <span data-ttu-id="bf21b-118">Localizar `top` em cada página que você visita.</span><span class="sxs-lookup"><span data-stu-id="bf21b-118">Find `top` on every page that you visit.</span></span>  `top` <span data-ttu-id="bf21b-119">representa o quadro do documento principal.</span><span class="sxs-lookup"><span data-stu-id="bf21b-119">represents the main document frame.</span></span>  
*   <span data-ttu-id="bf21b-120">O segundo nível, como `docs.microsoft.com` na figura anterior, representa uma [origem][HtmlstandardOrigin].</span><span class="sxs-lookup"><span data-stu-id="bf21b-120">The second-level, such as `docs.microsoft.com` in the previous figure, represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="bf21b-121">O terceiro nível, o quarto nível e assim por diante, representam diretórios e recursos que foram carregados dessa origem.</span><span class="sxs-lookup"><span data-stu-id="bf21b-121">The third-level, fourth-level, and so on, represent directories and resources that were loaded from that origin.</span></span>  <span data-ttu-id="bf21b-122">Por exemplo, na figura anterior, o caminho completo do recurso `devtools-guide-chromium` é</span><span class="sxs-lookup"><span data-stu-id="bf21b-122">For example, in the previous figure the full path to the resource `devtools-guide-chromium` is</span></span> `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
<span data-ttu-id="bf21b-123">Clique em um arquivo no painel da **página** para exibir o conteúdo no painel do **Editor** .</span><span class="sxs-lookup"><span data-stu-id="bf21b-123">Click a file in the **Page** pane to view the contents in the **Editor** pane.</span></span>  <span data-ttu-id="bf21b-124">Você pode ver qualquer tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="bf21b-124">You may view any type of file.</span></span>  <span data-ttu-id="bf21b-125">Para imagens, você vê uma visualização da imagem.</span><span class="sxs-lookup"><span data-stu-id="bf21b-125">For images, you see a preview of the image.</span></span>  

:::image type="complex" source="./media/sources-editor-pane.msft.png" alt-text="Exibir o conteúdo de a4d10f71.index-docs.js no painel do editor" lightbox="./media/sources-editor-pane.msft.png":::
   <span data-ttu-id="bf21b-127">Exibir o conteúdo do `a4d10f71.index-docs.js` painel do **Editor**</span><span class="sxs-lookup"><span data-stu-id="bf21b-127">View the contents of `a4d10f71.index-docs.js` in the **Editor** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="bf21b-128">Editar CSS e JavaScript</span><span class="sxs-lookup"><span data-stu-id="bf21b-128">Edit CSS and JavaScript</span></span> 

<span data-ttu-id="bf21b-129">Use o painel **Editor** para editar CSS e JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bf21b-129">Use the **Editor** pane to edit CSS and JavaScript.</span></span>  <span data-ttu-id="bf21b-130">O DevTools atualiza a página para executar seu novo código.</span><span class="sxs-lookup"><span data-stu-id="bf21b-130">DevTools updates the page to run your new code.</span></span>  <span data-ttu-id="bf21b-131">Por exemplo, se você editar um arquivo CSS, adicione a regra de estilo abaixo:</span><span class="sxs-lookup"><span data-stu-id="bf21b-131">For example, if you edit a CSS file by adding the style rule below:</span></span>

```css
.metadata.page-metadata {
    color: red;
}
```

<span data-ttu-id="bf21b-132">Você verá que a alteração entrará em vigor imediatamente.</span><span class="sxs-lookup"><span data-stu-id="bf21b-132">You should see that change take effect immediately.</span></span>

:::image type="complex" source="./media/edit-css.msft.png" alt-text="Editar CSS no painel do editor para alterar a cor do texto do subtítulo para vermelho" lightbox="./media/edit-css.msft.png":::
   <span data-ttu-id="bf21b-134">Editar CSS no painel do **Editor** para alterar a cor do texto do subtítulo para vermelho</span><span class="sxs-lookup"><span data-stu-id="bf21b-134">Edit CSS in the **Editor** pane to change the text color of the subtitle to red</span></span>  
:::image-end:::  

<span data-ttu-id="bf21b-135">As alterações de CSS entram em vigor imediatamente, não é necessário salvar.</span><span class="sxs-lookup"><span data-stu-id="bf21b-135">CSS changes take effect immediately, no save needed.</span></span>  <span data-ttu-id="bf21b-136">Para que as alterações de JavaScript sejam efetivadas, pressione `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="bf21b-136">For JavaScript changes to take effect, press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\).</span></span>  <span data-ttu-id="bf21b-137">O DevTools não executa novamente um script, portanto, as únicas alterações de JavaScript que entram em vigor são aquelas que você faz dentro de funções.</span><span class="sxs-lookup"><span data-stu-id="bf21b-137">DevTools does not re-run a script, so the only JavaScript changes that take effect are those that you make inside of functions.</span></span>  <span data-ttu-id="bf21b-138">Por exemplo, na figura a seguir, observe como não `console.log('A')` é executado, enquanto `console.log('B')` o faz.</span><span class="sxs-lookup"><span data-stu-id="bf21b-138">For example, in the following figure, notice how `console.log('A')` does not run, whereas `console.log('B')` does.</span></span>  <span data-ttu-id="bf21b-139">Se o DevTools reexecutar o script inteiro depois de fazer a alteração, o texto `A` teria sido registrado no **console**.</span><span class="sxs-lookup"><span data-stu-id="bf21b-139">If DevTools re-runs the entire script after making the change, then the text `A` would have been logged to the **Console**.</span></span>  

:::image type="complex" source="./media/edit-js.msft.png" alt-text="Edição de JavaScript no painel do editor" lightbox="./media/edit-js.msft.png":::
   <span data-ttu-id="bf21b-141">Edição de JavaScript no painel do **Editor**</span><span class="sxs-lookup"><span data-stu-id="bf21b-141">Editing JavaScript in the **Editor** pane</span></span>  
:::image-end:::  

<span data-ttu-id="bf21b-142">DevTools apagará as alterações de CSS e JavaScript quando você recarregar a página.</span><span class="sxs-lookup"><span data-stu-id="bf21b-142">DevTools erases your CSS and JavaScript changes when you reload the page.</span></span>  <span data-ttu-id="bf21b-143">Consulte [configurar um espaço de trabalho](#set-up-a-workspace) para saber como salvar as alterações no seu sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="bf21b-143">See [Set up a Workspace](#set-up-a-workspace) to learn how to save the changes to your file system.</span></span>  

## <span data-ttu-id="bf21b-144">Criar, salvar e executar Snippets</span><span class="sxs-lookup"><span data-stu-id="bf21b-144">Create, save, and run Snippets</span></span> 

<span data-ttu-id="bf21b-145">Trechos de código são scripts que você pode executar em qualquer página.</span><span class="sxs-lookup"><span data-stu-id="bf21b-145">Snippets are scripts which you may run on any page.</span></span>  <span data-ttu-id="bf21b-146">Imagine que você digite repetidamente o código a seguir no **console**para inserir a biblioteca jQuery em uma página, para que você possa executar comandos do jQuery a partir do **console**:</span><span class="sxs-lookup"><span data-stu-id="bf21b-146">Imagine that you repeatedly type out the following code in the **Console**, in order to insert the jQuery library into a page, so that you may run jQuery commands from the **Console**:</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="bf21b-147">Em vez disso, você pode salvar esse código em um **snippet** e executá-lo com alguns cliques de botão, sempre que precisar.</span><span class="sxs-lookup"><span data-stu-id="bf21b-147">Instead, you may save this code in a **Snippet** and run it with a couple of button clicks, any time you need it.</span></span>  <span data-ttu-id="bf21b-148">DevTools salva o **trecho** em seu sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="bf21b-148">DevTools saves the **Snippet** to your file system.</span></span>  

:::image type="complex" source="./media/snippet.msft.png" alt-text="Um trecho que insere a biblioteca jQuery em uma página" lightbox="./media/snippet.msft.png":::
   <span data-ttu-id="bf21b-150">Um **trecho** que insere a biblioteca jQuery em uma página</span><span class="sxs-lookup"><span data-stu-id="bf21b-150">A **Snippet** that inserts the jQuery library into a page</span></span>  
:::image-end:::  

<span data-ttu-id="bf21b-151">Para executar um **snippet**:</span><span class="sxs-lookup"><span data-stu-id="bf21b-151">To run a **Snippet**:</span></span>

*   <span data-ttu-id="bf21b-152">Abra o arquivo usando o painel **Snippets** e clique em **executar** \ ( ![ o botão Executar \ ][ImageRunIcon] ).</span><span class="sxs-lookup"><span data-stu-id="bf21b-152">Open the file using the **Snippets** pane, and click **Run** \(![The Run button][ImageRunIcon]\).</span></span>  
*   <span data-ttu-id="bf21b-153">Abra o **[menu de comando][DevtoolsGuideChromiumCommandMenuIndex]**, exclua o `>` caractere, digite `!` , digite o nome do seu **snippet**e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="bf21b-153">Open the **[Command Menu][DevtoolsGuideChromiumCommandMenuIndex]**, delete the `>` character, type `!`, type the name of your **Snippet**, then press `Enter`.</span></span>  
    
<span data-ttu-id="bf21b-154">Consulte [executar trechos de código em qualquer página][DevtoolsGuideChromiumJavascriptSnippets] para saber mais.</span><span class="sxs-lookup"><span data-stu-id="bf21b-154">See [Run Snippets Of Code From Any Page][DevtoolsGuideChromiumJavascriptSnippets] to learn more.</span></span>

## <span data-ttu-id="bf21b-155">Depurar JavaScript</span><span class="sxs-lookup"><span data-stu-id="bf21b-155">Debug JavaScript</span></span> 

<span data-ttu-id="bf21b-156">Em vez de usar `console.log()` para inferir onde o JavaScript está errado, considere usar as ferramentas de depuração do Microsoft Edge devtools, em vez disso.</span><span class="sxs-lookup"><span data-stu-id="bf21b-156">Rather than using `console.log()` to infer where your JavaScript is going wrong, consider using the Microsoft Edge DevTools debugging tools, instead.</span></span>  <span data-ttu-id="bf21b-157">A ideia geral é definir um ponto de interrupção, que é uma interrupção intencional em seu código e, em seguida, percorrer o tempo de execução do seu código, uma linha por vez.</span><span class="sxs-lookup"><span data-stu-id="bf21b-157">The general idea is to set a breakpoint, which is an intentional stopping place in your code, and then step through the runtime of your code, one line at a time.</span></span>  <span data-ttu-id="bf21b-158">Ao percorrer o código, você pode visualizar e alterar os valores de todas as propriedades e variáveis definidas atualmente, executar JavaScript no **console**e muito mais.</span><span class="sxs-lookup"><span data-stu-id="bf21b-158">As you step through the code, you may view and change the values of all currently-defined properties and variables, run JavaScript in the **Console**, and more.</span></span>

<span data-ttu-id="bf21b-159">Consulte [introdução à depuração de JavaScript][DevtoolsGuideChromiumJavascriptIndex] para aprender as noções básicas de depuração no devtools.</span><span class="sxs-lookup"><span data-stu-id="bf21b-159">See [Get Started With Debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] to learn the basics of debugging in DevTools.</span></span>

:::image type="complex" source="./media/debugging.msft.png" alt-text="Depurar JavaScript" lightbox="./media/debugging.msft.png":::
   <span data-ttu-id="bf21b-161">Depurar JavaScript</span><span class="sxs-lookup"><span data-stu-id="bf21b-161">Debug JavaScript</span></span>  
:::image-end:::  

## <span data-ttu-id="bf21b-162">Configurar um espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="bf21b-162">Set up a Workspace</span></span> 

<span data-ttu-id="bf21b-163">Por padrão, quando você edita um arquivo no painel **fontes** , essas alterações são perdidas quando você recarrega a página.</span><span class="sxs-lookup"><span data-stu-id="bf21b-163">By default, when you edit a file in the **Sources** panel, those changes are lost when you reload the page.</span></span>  <span data-ttu-id="bf21b-164">Os **espaços de trabalho** permitem salvar as alterações feitas no devtools em seu sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="bf21b-164">**Workspaces** enable you to save the changes that you make in DevTools to your file system.</span></span>  <span data-ttu-id="bf21b-165">Basicamente, DevTools pode ser usado como editor de código.</span><span class="sxs-lookup"><span data-stu-id="bf21b-165">Essentially, DevTools is able to be used as your code editor.</span></span>

<span data-ttu-id="bf21b-166">Veja [Editar arquivos com espaços de trabalho][DevtoolsGuideChromiumWorkspacesIndex] para começar.</span><span class="sxs-lookup"><span data-stu-id="bf21b-166">See [Edit Files With Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to get started.</span></span>

<!--  
 


-->  

<!-- image links -->  

[ImageRunIcon]: ./media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ./command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptIndex]: ./javascript/index.md "Introdução à depuração de JavaScript no Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptSnippets]: ./javascript/snippets.md "Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools"  
[DevtoolsGuideChromiumWorkspacesIndex]: ./workspaces/index.md "Editar arquivos com espaços de trabalho"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origem-padrão HTML"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Quadros | W3C"  

> [!NOTE]
> <span data-ttu-id="bf21b-173">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="bf21b-173">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="bf21b-174">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/sources) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="bf21b-174">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="bf21b-176">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bf21b-176">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
