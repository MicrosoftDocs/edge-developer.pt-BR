---
description: Exibir e editar arquivos, criar Snippets, Depurar JavaScript e configurar espaços de trabalho no painel fontes do Microsoft Edge DevTools.
title: Visão geral do painel fontes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: b90f927670146c004a335256ace28203219442eb
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231392"
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

# <span data-ttu-id="8862d-104">Visão geral do painel fontes</span><span class="sxs-lookup"><span data-stu-id="8862d-104">Sources panel overview</span></span>  

<span data-ttu-id="8862d-105">Use o painel **fontes** devtools do Microsoft Edge para executar as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="8862d-105">Use the Microsoft Edge DevTools **Sources** panel to perform the following actions.</span></span>  

*   <span data-ttu-id="8862d-106">[Exibir arquivos](#display-files).</span><span class="sxs-lookup"><span data-stu-id="8862d-106">[Display files](#display-files).</span></span>  
*   <span data-ttu-id="8862d-107">[Editar CSS e JavaScript](#edit-css-and-javascript).</span><span class="sxs-lookup"><span data-stu-id="8862d-107">[Edit CSS and JavaScript](#edit-css-and-javascript).</span></span>  
*   <span data-ttu-id="8862d-108">[Crie e salve **trechos de código** JavaScript](#create-save-and-run-snippets), que você pode executar em qualquer página da Web.</span><span class="sxs-lookup"><span data-stu-id="8862d-108">[Create and save **Snippets** of JavaScript](#create-save-and-run-snippets), which you may run on any webpage.</span></span>  <span data-ttu-id="8862d-109">Os **trechos de código** são semelhantes a bookmarklets.</span><span class="sxs-lookup"><span data-stu-id="8862d-109">**Snippets** are similar to bookmarklets.</span></span>  
*   <span data-ttu-id="8862d-110">[Depurar JavaScript](#debug-javascript).</span><span class="sxs-lookup"><span data-stu-id="8862d-110">[Debug JavaScript](#debug-javascript).</span></span>  
*   <span data-ttu-id="8862d-111">[Configure um espaço de trabalho](#set-up-a-workspace)para que as alterações feitas no devtools sejam salvas no código do seu sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8862d-111">[Set up a Workspace](#set-up-a-workspace), so that changes you make in DevTools get saved to the code on your file system.</span></span>  
    
## <span data-ttu-id="8862d-112">Exibir arquivos</span><span class="sxs-lookup"><span data-stu-id="8862d-112">Display files</span></span>  

<span data-ttu-id="8862d-113">Use o painel de **página** para exibir todos os recursos que a página carregou.</span><span class="sxs-lookup"><span data-stu-id="8862d-113">Use the **Page** pane to display all of the resources that the page has loaded.</span></span>

:::image type="complex" source="../media/sources-page-pane.msft.png" alt-text="Painel de página" lightbox="../media/sources-page-pane.msft.png":::
   <span data-ttu-id="8862d-115">Painel de **página**</span><span class="sxs-lookup"><span data-stu-id="8862d-115">The **Page** pane</span></span>  
:::image-end:::  

<span data-ttu-id="8862d-116">Como o painel da **página** está organizado:</span><span class="sxs-lookup"><span data-stu-id="8862d-116">How the **Page** pane is organized:</span></span>  
*   <span data-ttu-id="8862d-117">O nível superior, como `top` na figura anterior, representa um [quadro HTML][W3CHtml4Frames].</span><span class="sxs-lookup"><span data-stu-id="8862d-117">The top-level, such as `top` in the previous figure, represents an [HTML frame][W3CHtml4Frames].</span></span>  <span data-ttu-id="8862d-118">Localizar `top` em cada página que você visita.</span><span class="sxs-lookup"><span data-stu-id="8862d-118">Find `top` on every page that you visit.</span></span>  `top` <span data-ttu-id="8862d-119">representa o quadro do documento principal.</span><span class="sxs-lookup"><span data-stu-id="8862d-119">represents the main document frame.</span></span>  
*   <span data-ttu-id="8862d-120">O segundo nível, como `docs.microsoft.com` na figura anterior, representa uma [origem][HtmlstandardOrigin].</span><span class="sxs-lookup"><span data-stu-id="8862d-120">The second-level, such as `docs.microsoft.com` in the previous figure, represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="8862d-121">O terceiro nível, o quarto nível e assim por diante, representam diretórios e recursos que foram carregados dessa origem.</span><span class="sxs-lookup"><span data-stu-id="8862d-121">The third-level, fourth-level, and so on, represent directories and resources that were loaded from that origin.</span></span>  <span data-ttu-id="8862d-122">Por exemplo, na figura anterior, o caminho completo do recurso `devtools-guide-chromium` é</span><span class="sxs-lookup"><span data-stu-id="8862d-122">For example, in the previous figure the full path to the resource `devtools-guide-chromium` is</span></span> `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
<span data-ttu-id="8862d-123">Escolha um arquivo no painel de **página** para exibir o conteúdo no painel do **Editor** .</span><span class="sxs-lookup"><span data-stu-id="8862d-123">Choose a file in the **Page** pane to display the contents in the **Editor** pane.</span></span>  <span data-ttu-id="8862d-124">Você pode exibir qualquer tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8862d-124">You may display any type of file.</span></span>  <span data-ttu-id="8862d-125">Para imagens, uma visualização da imagem é exibida.</span><span class="sxs-lookup"><span data-stu-id="8862d-125">For images, a preview of the image is displayed.</span></span>  

:::image type="complex" source="../media/sources-editor-pane.msft.png" alt-text="Exibir o conteúdo de a4d10f71.index-docs.js no painel do editor" lightbox="../media/sources-editor-pane.msft.png":::
   <span data-ttu-id="8862d-127">Exibir o conteúdo do `a4d10f71.index-docs.js` painel do **Editor**</span><span class="sxs-lookup"><span data-stu-id="8862d-127">Display the contents of `a4d10f71.index-docs.js` in the **Editor** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="8862d-128">Editar CSS e JavaScript</span><span class="sxs-lookup"><span data-stu-id="8862d-128">Edit CSS and JavaScript</span></span>  

<span data-ttu-id="8862d-129">Use o painel **Editor** para editar CSS e JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8862d-129">Use the **Editor** pane to edit CSS and JavaScript.</span></span>  <span data-ttu-id="8862d-130">O DevTools atualiza a página para executar seu novo código.</span><span class="sxs-lookup"><span data-stu-id="8862d-130">DevTools updates the page to run your new code.</span></span>  <span data-ttu-id="8862d-131">Por exemplo, se você editar um arquivo CSS, adicione a regra de estilo abaixo:</span><span class="sxs-lookup"><span data-stu-id="8862d-131">For example, if you edit a CSS file by adding the style rule below:</span></span>

```css
.metadata.page-metadata {
    color: red;
}
```

<span data-ttu-id="8862d-132">Essa alteração deve entrar em vigor imediatamente.</span><span class="sxs-lookup"><span data-stu-id="8862d-132">That change should take effect immediately.</span></span>

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Editar CSS no painel do editor para alterar a cor do texto do subtítulo para vermelho" lightbox="../media/edit-css.msft.png":::
   <span data-ttu-id="8862d-134">Editar CSS no painel do **Editor** para alterar a cor do texto do subtítulo para vermelho</span><span class="sxs-lookup"><span data-stu-id="8862d-134">Edit CSS in the **Editor** pane to change the text color of the subtitle to red</span></span>  
:::image-end:::  

<span data-ttu-id="8862d-135">As alterações de CSS entram em vigor imediatamente, não é necessário salvar.</span><span class="sxs-lookup"><span data-stu-id="8862d-135">CSS changes take effect immediately, no save needed.</span></span>  <span data-ttu-id="8862d-136">Para que as alterações de JavaScript entrem em vigor, selecione `Control` + `S` \ (Windows, Linux \) ou `Command` + `S` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="8862d-136">For JavaScript changes to take effect, select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\).</span></span>  <span data-ttu-id="8862d-137">O DevTools não executa novamente um script, portanto, as únicas alterações de JavaScript que entram em vigor são aquelas que você faz dentro de funções.</span><span class="sxs-lookup"><span data-stu-id="8862d-137">DevTools does not re-run a script, so the only JavaScript changes that take effect are those that you make inside of functions.</span></span>  <span data-ttu-id="8862d-138">Por exemplo, na figura a seguir, observe como não `console.log('A')` é executado, enquanto `console.log('B')` o faz.</span><span class="sxs-lookup"><span data-stu-id="8862d-138">For example, in the following figure, notice how `console.log('A')` does not run, whereas `console.log('B')` does.</span></span>  <span data-ttu-id="8862d-139">Se o DevTools reexecutar o script inteiro depois de fazer a alteração, o texto `A` teria sido registrado no **console**.</span><span class="sxs-lookup"><span data-stu-id="8862d-139">If DevTools re-runs the entire script after making the change, then the text `A` would have been logged to the **Console**.</span></span>  

:::image type="complex" source="../media/edit-js.msft.png" alt-text="Edição de JavaScript no painel do editor" lightbox="../media/edit-js.msft.png":::
   <span data-ttu-id="8862d-141">Edição de JavaScript no painel do **Editor**</span><span class="sxs-lookup"><span data-stu-id="8862d-141">Editing JavaScript in the **Editor** pane</span></span>  
:::image-end:::  

<span data-ttu-id="8862d-142">DevTools apagará as alterações de CSS e JavaScript quando você recarregar a página.</span><span class="sxs-lookup"><span data-stu-id="8862d-142">DevTools erases your CSS and JavaScript changes when you reload the page.</span></span>  <span data-ttu-id="8862d-143">Navegue para [configurar um espaço de trabalho](#set-up-a-workspace) para aprender a salvar as alterações no seu sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8862d-143">Navigate to [Set up a Workspace](#set-up-a-workspace) to learn how to save the changes to your file system.</span></span>  

## <span data-ttu-id="8862d-144">Criar, salvar e executar Snippets</span><span class="sxs-lookup"><span data-stu-id="8862d-144">Create, save, and run Snippets</span></span>  

<span data-ttu-id="8862d-145">Trechos de código são scripts que você pode executar em qualquer página.</span><span class="sxs-lookup"><span data-stu-id="8862d-145">Snippets are scripts which you may run on any page.</span></span>  <span data-ttu-id="8862d-146">Imagine que você digite repetidamente o código a seguir no **console**para inserir a biblioteca jQuery em uma página, para que você possa executar comandos jQuery a partir do **console**.</span><span class="sxs-lookup"><span data-stu-id="8862d-146">Imagine that you repeatedly type out the following code in the **Console**, in order to insert the jQuery library into a page, so that you may run jQuery commands from the **Console**.</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="8862d-147">Em vez disso, você pode salvar esse código em um **snippet** e executá-lo com alguns cliques de botão, sempre que precisar.</span><span class="sxs-lookup"><span data-stu-id="8862d-147">Instead, you may save this code in a **Snippet** and run it with a couple of button clicks, any time you need it.</span></span>  <span data-ttu-id="8862d-148">DevTools salva o **trecho** em seu sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8862d-148">DevTools saves the **Snippet** to your file system.</span></span>  

:::image type="complex" source="../media/snippet.msft.png" alt-text="Um trecho que insere a biblioteca jQuery em uma página" lightbox="../media/snippet.msft.png":::
   <span data-ttu-id="8862d-150">Um **trecho** que insere a biblioteca jQuery em uma página</span><span class="sxs-lookup"><span data-stu-id="8862d-150">A **Snippet** that inserts the jQuery library into a page</span></span>  
:::image-end:::  

<span data-ttu-id="8862d-151">Para executar um **snippet**:</span><span class="sxs-lookup"><span data-stu-id="8862d-151">To run a **Snippet**:</span></span>

*   <span data-ttu-id="8862d-152">Abra o arquivo usando o painel **Snippets** e escolha **executar** \ ( ![ o botão executar ][ImageRunIcon] \).</span><span class="sxs-lookup"><span data-stu-id="8862d-152">Open the file using the **Snippets** pane, and choose **Run** \(![The Run button][ImageRunIcon]\).</span></span>  
*   <span data-ttu-id="8862d-153">Abra o [menu de comando][DevtoolsGuideChromiumCommandMenuIndex], exclua o `>` caractere, digite `!` , digite o nome do seu **snippet**e, em seguida, selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="8862d-153">Open the [Command Menu][DevtoolsGuideChromiumCommandMenuIndex], delete the `>` character, type `!`, type the name of your **Snippet**, and then select `Enter`.</span></span>  
    
<span data-ttu-id="8862d-154">Navegue até [executar trechos de código de qualquer página][DevtoolsGuideChromiumJavascriptSnippets] para saber mais.</span><span class="sxs-lookup"><span data-stu-id="8862d-154">Navigate to [Run Snippets Of Code From Any Page][DevtoolsGuideChromiumJavascriptSnippets] to learn more.</span></span>

## <span data-ttu-id="8862d-155">Depurar JavaScript</span><span class="sxs-lookup"><span data-stu-id="8862d-155">Debug JavaScript</span></span>  

<span data-ttu-id="8862d-156">Em vez de usar `console.log()` para inferir onde o JavaScript está errado, considere usar as ferramentas de depuração do Microsoft Edge devtools, em vez disso.</span><span class="sxs-lookup"><span data-stu-id="8862d-156">Rather than using `console.log()` to infer where your JavaScript is going wrong, consider using the Microsoft Edge DevTools debugging tools, instead.</span></span>  <span data-ttu-id="8862d-157">A ideia geral é definir um ponto de interrupção, que é uma interrupção intencional em seu código e, em seguida, percorrer o tempo de execução do seu código, uma linha por vez.</span><span class="sxs-lookup"><span data-stu-id="8862d-157">The general idea is to set a breakpoint, which is an intentional stopping place in your code, and then step through the runtime of your code, one line at a time.</span></span>  <span data-ttu-id="8862d-158">Ao percorrer o código, você pode exibir e alterar os valores de todas as propriedades e variáveis definidas atualmente, executar JavaScript no **console**e muito mais.</span><span class="sxs-lookup"><span data-stu-id="8862d-158">As you step through the code, you may display and change the values of all currently-defined properties and variables, run JavaScript in the **Console**, and more.</span></span>

<span data-ttu-id="8862d-159">Navegue até [introdução à depuração de JavaScript][DevtoolsGuideChromiumJavascriptIndex] para aprender as noções básicas de depuração no devtools.</span><span class="sxs-lookup"><span data-stu-id="8862d-159">Navigate to [Get Started With Debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] to learn the basics of debugging in DevTools.</span></span>

:::image type="complex" source="../media/debugging.msft.png" alt-text="Depurar JavaScript" lightbox="../media/debugging.msft.png":::
   <span data-ttu-id="8862d-161">Depurar JavaScript</span><span class="sxs-lookup"><span data-stu-id="8862d-161">Debug JavaScript</span></span>  
:::image-end:::  

## <span data-ttu-id="8862d-162">Configurar um espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="8862d-162">Set up a Workspace</span></span>  

<span data-ttu-id="8862d-163">Por padrão, quando você edita um arquivo na ferramenta **fontes** , essas alterações são perdidas quando você recarrega a página.</span><span class="sxs-lookup"><span data-stu-id="8862d-163">By default, when you edit a file in the **Sources** tool, those changes are lost when you reload the page.</span></span>  <span data-ttu-id="8862d-164">Os **espaços de trabalho** permitem salvar as alterações feitas no devtools em seu sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8862d-164">**Workspaces** enable you to save the changes that you make in DevTools to your file system.</span></span>  <span data-ttu-id="8862d-165">Basicamente, DevTools pode ser usado como editor de código.</span><span class="sxs-lookup"><span data-stu-id="8862d-165">Essentially, DevTools is able to be used as your code editor.</span></span>

<span data-ttu-id="8862d-166">Navegue para [Editar arquivos com espaços de trabalho][DevtoolsGuideChromiumWorkspacesIndex] para começar.</span><span class="sxs-lookup"><span data-stu-id="8862d-166">Navigate to [Edit Files With Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to get started.</span></span>

## <span data-ttu-id="8862d-167">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8862d-167">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRunIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ../command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Introdução à depuração JavaScript no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Editar arquivos com espaços de trabalho | Documentos da Microsoft"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origem | HTML padrão"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Quadros | W3C"  

> [!NOTE]
> <span data-ttu-id="8862d-174">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8862d-174">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8862d-175">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/sources) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="8862d-175">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8862d-177">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8862d-177">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
