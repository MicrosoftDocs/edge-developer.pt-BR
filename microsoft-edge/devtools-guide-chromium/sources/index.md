---
description: Exibir e editar arquivos, criar trechos de código, depurar JavaScript e configurar Espaços de Trabalho no painel Fontes do Microsoft Edge DevTools.
title: Visão geral do painel fontes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 4677bf82d3506a4b8d6336ded7ab557b794fd3df
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397759"
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

# <a name="sources-panel-overview"></a><span data-ttu-id="58f08-104">Visão geral do painel fontes</span><span class="sxs-lookup"><span data-stu-id="58f08-104">Sources panel overview</span></span>  

<span data-ttu-id="58f08-105">Use o painel Fontes \*\*\*\* do Microsoft Edge DevTools para executar as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="58f08-105">Use the Microsoft Edge DevTools **Sources** panel to perform the following actions.</span></span>  

*   <span data-ttu-id="58f08-106">[Exibir arquivos](#display-files).</span><span class="sxs-lookup"><span data-stu-id="58f08-106">[Display files](#display-files).</span></span>  
*   <span data-ttu-id="58f08-107">[Edite CSS e JavaScript](#edit-css-and-javascript).</span><span class="sxs-lookup"><span data-stu-id="58f08-107">[Edit CSS and JavaScript](#edit-css-and-javascript).</span></span>  
*   <span data-ttu-id="58f08-108">[Crie e salve **trechos de** JavaScript](#create-save-and-run-snippets), que você pode executar em qualquer página da Web.</span><span class="sxs-lookup"><span data-stu-id="58f08-108">[Create and save **Snippets** of JavaScript](#create-save-and-run-snippets), which you may run on any webpage.</span></span>  <span data-ttu-id="58f08-109">**Trechos de código** são semelhantes aos indicadores.</span><span class="sxs-lookup"><span data-stu-id="58f08-109">**Snippets** are similar to bookmarklets.</span></span>  
*   <span data-ttu-id="58f08-110">[Depurar JavaScript](#debug-javascript).</span><span class="sxs-lookup"><span data-stu-id="58f08-110">[Debug JavaScript](#debug-javascript).</span></span>  
*   <span data-ttu-id="58f08-111">[Configurar um Espaço de Trabalho](#set-up-a-workspace), para que as alterações feitas no DevTools são salvas no código em seu sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="58f08-111">[Set up a Workspace](#set-up-a-workspace), so that changes you make in DevTools get saved to the code on your file system.</span></span>  
    
## <a name="display-files"></a><span data-ttu-id="58f08-112">Exibir arquivos</span><span class="sxs-lookup"><span data-stu-id="58f08-112">Display files</span></span>  

<span data-ttu-id="58f08-113">Use o **painel Página;** para exibir todos os recursos que a página carregou.</span><span class="sxs-lookup"><span data-stu-id="58f08-113">Use the **Page** panel; to display all of the resources that the page has loaded.</span></span>

:::image type="complex" source="../media/sources-page-pane.msft.png" alt-text="O painel Página" lightbox="../media/sources-page-pane.msft.png":::
   <span data-ttu-id="58f08-115">O **painel Página**</span><span class="sxs-lookup"><span data-stu-id="58f08-115">The **Page** panel</span></span>  
:::image-end:::  

<span data-ttu-id="58f08-116">Como o **painel** Página é organizado:</span><span class="sxs-lookup"><span data-stu-id="58f08-116">How the **Page** pane is organized:</span></span>  
*   <span data-ttu-id="58f08-117">O nível superior, como `top` na figura anterior, representa um [quadro HTML][W3CHtml4Frames].</span><span class="sxs-lookup"><span data-stu-id="58f08-117">The top-level, such as `top` in the previous figure, represents an [HTML frame][W3CHtml4Frames].</span></span>  <span data-ttu-id="58f08-118">Encontre `top` em todas as páginas que você visitar.</span><span class="sxs-lookup"><span data-stu-id="58f08-118">Find `top` on every page that you visit.</span></span>  `top` <span data-ttu-id="58f08-119">representa o quadro principal do documento.</span><span class="sxs-lookup"><span data-stu-id="58f08-119">represents the main document frame.</span></span>  
*   <span data-ttu-id="58f08-120">O segundo nível, como `docs.microsoft.com` na figura anterior, representa uma [origem][HtmlstandardOrigin].</span><span class="sxs-lookup"><span data-stu-id="58f08-120">The second-level, such as `docs.microsoft.com` in the previous figure, represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="58f08-121">O terceiro nível, quarto nível e assim por diante, representam diretórios e recursos carregados a partir dessa origem.</span><span class="sxs-lookup"><span data-stu-id="58f08-121">The third-level, fourth-level, and so on, represent directories and resources that were loaded from that origin.</span></span>  <span data-ttu-id="58f08-122">Por exemplo, na figura anterior, o caminho completo para o `devtools-guide-chromium` recurso é</span><span class="sxs-lookup"><span data-stu-id="58f08-122">For example, in the previous figure the full path to the resource `devtools-guide-chromium` is</span></span> `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
<span data-ttu-id="58f08-123">Escolha um arquivo no painel **Página** para exibir o conteúdo no **painel Editor.**</span><span class="sxs-lookup"><span data-stu-id="58f08-123">Choose a file in the **Page** panel to display the contents in the **Editor** pane.</span></span>  <span data-ttu-id="58f08-124">Você pode exibir qualquer tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="58f08-124">You may display any type of file.</span></span>  <span data-ttu-id="58f08-125">Para imagens, uma visualização da imagem é exibida.</span><span class="sxs-lookup"><span data-stu-id="58f08-125">For images, a preview of the image is displayed.</span></span>  

:::image type="complex" source="../media/sources-editor-pane.msft.png" alt-text="Exibir o conteúdo de a4d10f71.index-docs.js no painel Editor" lightbox="../media/sources-editor-pane.msft.png":::
   <span data-ttu-id="58f08-127">Exibir o conteúdo `a4d10f71.index-docs.js` do painel **Editor**</span><span class="sxs-lookup"><span data-stu-id="58f08-127">Display the contents of `a4d10f71.index-docs.js` in the **Editor** panel</span></span>  
:::image-end:::  

## <a name="edit-css-and-javascript"></a><span data-ttu-id="58f08-128">Editar CSS e JavaScript</span><span class="sxs-lookup"><span data-stu-id="58f08-128">Edit CSS and JavaScript</span></span>  

<span data-ttu-id="58f08-129">Use o **painel Editor** para editar CSS e JavaScript.</span><span class="sxs-lookup"><span data-stu-id="58f08-129">Use the **Editor** pane to edit CSS and JavaScript.</span></span>  <span data-ttu-id="58f08-130">O DevTools atualiza a página para executar seu novo código.</span><span class="sxs-lookup"><span data-stu-id="58f08-130">DevTools updates the page to run your new code.</span></span>  <span data-ttu-id="58f08-131">Por exemplo, se você editar um arquivo CSS adicionando a regra de estilo abaixo:</span><span class="sxs-lookup"><span data-stu-id="58f08-131">For example, if you edit a CSS file by adding the style rule below:</span></span>

```css
.metadata.page-metadata {
    color: red;
}
```

<span data-ttu-id="58f08-132">Essa alteração deve ter efeito imediato.</span><span class="sxs-lookup"><span data-stu-id="58f08-132">That change should take effect immediately.</span></span>

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Editar CSS no painel Editor para alterar a cor do texto do subtítulo para vermelho" lightbox="../media/edit-css.msft.png":::
   <span data-ttu-id="58f08-134">Editar CSS no **painel Editor** para alterar a cor do texto do subtítulo para vermelho</span><span class="sxs-lookup"><span data-stu-id="58f08-134">Edit CSS in the **Editor** pane to change the text color of the subtitle to red</span></span>  
:::image-end:::  

<span data-ttu-id="58f08-135">As alterações css têm efeito imediato, sem a necessidade de salvar.</span><span class="sxs-lookup"><span data-stu-id="58f08-135">CSS changes take effect immediately, no save needed.</span></span>  <span data-ttu-id="58f08-136">Para que as alterações do JavaScript entre em vigor, selecione `Control` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="58f08-136">For JavaScript changes to take effect, select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\).</span></span>  <span data-ttu-id="58f08-137">DevTools não executará um script de novo, portanto, as únicas alterações javaScript que entrarão em vigor são aquelas que você faz dentro das funções.</span><span class="sxs-lookup"><span data-stu-id="58f08-137">DevTools does not re-run a script, so the only JavaScript changes that take effect are those that you make inside of functions.</span></span>  <span data-ttu-id="58f08-138">Por exemplo, na figura a seguir, observe como `console.log('A')` não é executado, enquanto `console.log('B')` o faz.</span><span class="sxs-lookup"><span data-stu-id="58f08-138">For example, in the following figure, notice how `console.log('A')` does not run, whereas `console.log('B')` does.</span></span>  <span data-ttu-id="58f08-139">Se o DevTools re-executa todo o script depois de fazer a alteração, o texto é `A` registrado no **Console**.</span><span class="sxs-lookup"><span data-stu-id="58f08-139">If DevTools re-runs the entire script after making the change, then the text `A` is logged to the **Console**.</span></span>  

:::image type="complex" source="../media/edit-js.msft.png" alt-text="Editando JavaScript no painel Editor" lightbox="../media/edit-js.msft.png":::
   <span data-ttu-id="58f08-141">Editando JavaScript no **painel Editor**</span><span class="sxs-lookup"><span data-stu-id="58f08-141">Editing JavaScript in the **Editor** panel</span></span>  
:::image-end:::  

<span data-ttu-id="58f08-142">O DevTools apaga as alterações CSS e JavaScript quando você atualize a página.</span><span class="sxs-lookup"><span data-stu-id="58f08-142">DevTools erases your CSS and JavaScript changes when you refresh the page.</span></span>  <span data-ttu-id="58f08-143">Navegue [até Configurar um Espaço de Trabalho](#set-up-a-workspace) para saber como salvar as alterações no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="58f08-143">Navigate to [Set up a Workspace](#set-up-a-workspace) to learn how to save the changes to your file system.</span></span>  

## <a name="create-save-and-run-snippets"></a><span data-ttu-id="58f08-144">Criar, salvar e executar trechos de código</span><span class="sxs-lookup"><span data-stu-id="58f08-144">Create, save, and run Snippets</span></span>  

<span data-ttu-id="58f08-145">Trechos de código são scripts que você pode executar em qualquer página.</span><span class="sxs-lookup"><span data-stu-id="58f08-145">Snippets are scripts which you may run on any page.</span></span>  <span data-ttu-id="58f08-146">Imagine que você digite repetidamente o código a seguir no **Console**, para inserir a biblioteca jQuery em uma página, para que você possa executar comandos jQuery do **Console**.</span><span class="sxs-lookup"><span data-stu-id="58f08-146">Imagine that you repeatedly type out the following code in the **Console**, in order to insert the jQuery library into a page, so that you may run jQuery commands from the **Console**.</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="58f08-147">Em vez disso, você pode salvar esse código em **um trecho** de código e execute-o com alguns cliques de botão, sempre que precisar dele.</span><span class="sxs-lookup"><span data-stu-id="58f08-147">Instead, you may save this code in a **Snippet** and run it with a couple of button clicks, any time you need it.</span></span>  <span data-ttu-id="58f08-148">O DevTools salva **o trecho em** seu sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="58f08-148">DevTools saves the **Snippet** to your file system.</span></span>  

:::image type="complex" source="../media/snippet.msft.png" alt-text="Um trecho que insere a biblioteca jQuery em uma página" lightbox="../media/snippet.msft.png":::
   <span data-ttu-id="58f08-150">Um **trecho que** insere a biblioteca jQuery em uma página</span><span class="sxs-lookup"><span data-stu-id="58f08-150">A **Snippet** that inserts the jQuery library into a page</span></span>  
:::image-end:::  

<span data-ttu-id="58f08-151">Para executar um **trecho de código:**</span><span class="sxs-lookup"><span data-stu-id="58f08-151">To run a **Snippet**:</span></span>

*   <span data-ttu-id="58f08-152">Abra o arquivo usando o painel **Trechos** de Código e escolha **Executar** \( ![ O botão Executar ][ImageRunIcon] \).</span><span class="sxs-lookup"><span data-stu-id="58f08-152">Open the file using the **Snippets** panel, and choose **Run** \(![The Run button][ImageRunIcon]\).</span></span>  
*   <span data-ttu-id="58f08-153">Abra o [Menu de Comando,][DevtoolsGuideChromiumCommandMenuIndex]exclua o caractere, digite , digite o nome do trecho de código e `>` `!` selecione \*\*\*\* `Enter` .</span><span class="sxs-lookup"><span data-stu-id="58f08-153">Open the [Command Menu][DevtoolsGuideChromiumCommandMenuIndex], delete the `>` character, type `!`, type the name of your **Snippet**, and then select `Enter`.</span></span>  
    
<span data-ttu-id="58f08-154">Navegue [até Executar trechos de código de qualquer página][DevtoolsGuideChromiumJavascriptSnippets] para saber mais.</span><span class="sxs-lookup"><span data-stu-id="58f08-154">Navigate to [Run Snippets Of Code From Any Page][DevtoolsGuideChromiumJavascriptSnippets] to learn more.</span></span>

## <a name="debug-javascript"></a><span data-ttu-id="58f08-155">Depurar JavaScript</span><span class="sxs-lookup"><span data-stu-id="58f08-155">Debug JavaScript</span></span>  

<span data-ttu-id="58f08-156">Em vez de usar para inferir onde o JavaScript está indo mal, considere usar as ferramentas `console.log()` de depuração do Microsoft Edge DevTools, em vez disso.</span><span class="sxs-lookup"><span data-stu-id="58f08-156">Rather than using `console.log()` to infer where your JavaScript is going wrong, consider using the Microsoft Edge DevTools debugging tools, instead.</span></span>  <span data-ttu-id="58f08-157">A ideia geral é definir um ponto de interrupção, que é um local de interrupção intencional em seu código e, em seguida, passar pelo tempo de execução do código, uma linha por vez.</span><span class="sxs-lookup"><span data-stu-id="58f08-157">The general idea is to set a breakpoint, which is an intentional stopping place in your code, and then step through the runtime of your code, one line at a time.</span></span>  <span data-ttu-id="58f08-158">Conforme você passa pelo código, você pode exibir e alterar os valores de todas as propriedades e variáveis definidas no momento, executar JavaScript no **Console**e muito mais.</span><span class="sxs-lookup"><span data-stu-id="58f08-158">As you step through the code, you may display and change the values of all currently-defined properties and variables, run JavaScript in the **Console**, and more.</span></span>

<span data-ttu-id="58f08-159">Navegue [até Começar a Depurar JavaScript][DevtoolsGuideChromiumJavascriptIndex] para aprender os conceitos básicos de depuração no DevTools.</span><span class="sxs-lookup"><span data-stu-id="58f08-159">Navigate to [Get Started With Debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] to learn the basics of debugging in DevTools.</span></span>

:::image type="complex" source="../media/debugging.msft.png" alt-text="Depurar JavaScript" lightbox="../media/debugging.msft.png":::
   <span data-ttu-id="58f08-161">Depurar JavaScript</span><span class="sxs-lookup"><span data-stu-id="58f08-161">Debug JavaScript</span></span>  
:::image-end:::  

## <a name="set-up-a-workspace"></a><span data-ttu-id="58f08-162">Configurar um Espaço de Trabalho</span><span class="sxs-lookup"><span data-stu-id="58f08-162">Set up a Workspace</span></span>  

<span data-ttu-id="58f08-163">Por padrão, quando você edita um arquivo na ferramenta **Fontes,** essas alterações são perdidas quando você atualize a página.</span><span class="sxs-lookup"><span data-stu-id="58f08-163">By default, when you edit a file in the **Sources** tool, those changes are lost when you refresh the page.</span></span>  <span data-ttu-id="58f08-164">**Os espaços de** trabalho permitem que você salve as alterações feitas no DevTools em seu sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="58f08-164">**Workspaces** enable you to save the changes that you make in DevTools to your file system.</span></span>  <span data-ttu-id="58f08-165">Essencialmente, o DevTools é capaz de ser usado como seu editor de código.</span><span class="sxs-lookup"><span data-stu-id="58f08-165">Essentially, DevTools is able to be used as your code editor.</span></span>

<span data-ttu-id="58f08-166">Navegue [até Editar Arquivos com Espaços de Trabalho][DevtoolsGuideChromiumWorkspacesIndex] para começar.</span><span class="sxs-lookup"><span data-stu-id="58f08-166">Navigate to [Edit Files With Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to get started.</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="58f08-167">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="58f08-167">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRunIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ../command-menu/index.md "Execute comandos com o menu de comando Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Começar a depurar JavaScript no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Execute trechos de código do JavaScript em qualquer página com o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Editar arquivos com espaços de trabalho | Microsoft Docs"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origem | HTML Standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Quadros | W3C"  

> [!NOTE]
> <span data-ttu-id="58f08-174">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="58f08-174">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="58f08-175">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/sources) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="58f08-175">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="58f08-177">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="58f08-177">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
