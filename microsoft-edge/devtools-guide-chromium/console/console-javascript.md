---
description: Uma introdução ao uso da ferramenta Console dentro das Ferramentas de Desenvolvedor do Microsoft Edge como um ambiente JavaScript.
title: O Console como um ambiente JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, JavaScript, desenvolvimento da Web, ferramentas f12, devtools
ms.openlocfilehash: f75ac6d728c9a69542b2f58df85248759267f76d
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483288"
---
# <a name="the-console-as-a-javascript-environment"></a><span data-ttu-id="9b588-104">O Console como um ambiente JavaScript</span><span class="sxs-lookup"><span data-stu-id="9b588-104">The Console as a JavaScript environment</span></span>  

<span data-ttu-id="9b588-105">A **ferramenta Console** dentro do navegador DevTools é um ambiente [REPL.][WikiReadEvalPrintLoop]</span><span class="sxs-lookup"><span data-stu-id="9b588-105">The **Console** tool inside the browser DevTools is a [REPL][WikiReadEvalPrintLoop] environment.</span></span>  <span data-ttu-id="9b588-106">Isso significa que você pode gravar qualquer JavaScript no **Console** que seja executado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="9b588-106">It means that you may write any JavaScript in the **Console** that runs immediately.</span></span>

<span data-ttu-id="9b588-107">Para experimentar, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="9b588-107">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="9b588-108">Abra o **Console**.</span><span class="sxs-lookup"><span data-stu-id="9b588-108">Open the **Console**.</span></span>  
    *   <span data-ttu-id="9b588-109">Selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="9b588-109">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
1.  <span data-ttu-id="9b588-110">Digite `2 + 2`.</span><span class="sxs-lookup"><span data-stu-id="9b588-110">Type `2 + 2`.</span></span>  <span data-ttu-id="9b588-111">O **Console** já exibe o resultado `4` na próxima linha enquanto você o digita.</span><span class="sxs-lookup"><span data-stu-id="9b588-111">The **Console** already displays the result `4` on the next line while you type it.</span></span>  <span data-ttu-id="9b588-112">O `Eager evaluation` recurso ajuda você a escrever JavaScript válido.</span><span class="sxs-lookup"><span data-stu-id="9b588-112">The `Eager evaluation` feature helps you write valid JavaScript.</span></span>  <span data-ttu-id="9b588-113">Ele exibe o resultado enquanto você digita se ele está errado ou se existe um resultado válido.</span><span class="sxs-lookup"><span data-stu-id="9b588-113">It displays the result while you type whether it's wrong or if a valid result exists.</span></span>  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="Console exibe o resultado de 2 + 2 ao vivo à medida que você digita" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   <span data-ttu-id="9b588-115">**Console** exibe o resultado de `2 + 2` vida ao digitá-lo</span><span class="sxs-lookup"><span data-stu-id="9b588-115">**Console** displays the result of `2 + 2` live as you type it</span></span>  
:::image-end:::  

<span data-ttu-id="9b588-116">Se você selecionar , o Console executará o comando JavaScript, lhe dará o resultado e permitirá que `Enter` você escreva o próximo comando. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9b588-116">If you select `Enter`, the **Console** runs the JavaScript command, gives you the result, and allows you to write the next command.</span></span>  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Executar várias expressões JavaScript em sucessão" lightbox="../media/console-javascript-several-expressions.msft.png":::
   <span data-ttu-id="9b588-118">Executar várias expressões JavaScript em sucessão</span><span class="sxs-lookup"><span data-stu-id="9b588-118">Run several JavaScript expressions in succession</span></span>  
:::image-end:::  

## <a name="autocompletion-to-write-complex-expressions"></a><span data-ttu-id="9b588-119">Autocompleção para gravar expressões complexas</span><span class="sxs-lookup"><span data-stu-id="9b588-119">Autocompletion to write complex expressions</span></span>

<span data-ttu-id="9b588-120">O último exemplo pode parecer assustador, mas o **Console** ajuda você a escrever JavaScript complexo usando um excelente recurso de autocompleção.</span><span class="sxs-lookup"><span data-stu-id="9b588-120">The last example may seem scary, but the **Console** helps you write complex JavaScript using an excellent autocompletion feature.</span></span>  <span data-ttu-id="9b588-121">Esse recurso é uma ótima maneira de aprender sobre métodos que você não sabia antes.</span><span class="sxs-lookup"><span data-stu-id="9b588-121">This feature is a great way to learn about methods you didn't know before.</span></span>  

<span data-ttu-id="9b588-122">Para experimentar, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="9b588-122">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="9b588-123">Digite `doc`.</span><span class="sxs-lookup"><span data-stu-id="9b588-123">Type `doc`.</span></span>  
1.  <span data-ttu-id="9b588-124">Escolha `document` no menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="9b588-124">Choose `document` from the dropdown menu.</span></span>  
1.  <span data-ttu-id="9b588-125">Selecione a `tab` chave para escolher.</span><span class="sxs-lookup"><span data-stu-id="9b588-125">Select the `tab` key to choose it.</span></span>  
1.  <span data-ttu-id="9b588-126">Digite `.bo`.</span><span class="sxs-lookup"><span data-stu-id="9b588-126">Type `.bo`.</span></span>  
1.  <span data-ttu-id="9b588-127">Selecione `tab` para obter `document.body` .</span><span class="sxs-lookup"><span data-stu-id="9b588-127">Select `tab` to get `document.body`.</span></span>  
1.  <span data-ttu-id="9b588-128">Digite outro para obter uma lista grande de possíveis propriedades e métodos disponíveis no corpo `.` da página da Web atual.</span><span class="sxs-lookup"><span data-stu-id="9b588-128">Type another `.` to get a large list of possible properties and methods available on the body of the current webpage.</span></span>  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Console autocompletion of JavaScript expressions" lightbox="../media/console-javascript-autocomplete.msft.png":::
   <span data-ttu-id="9b588-130">**Console** autocompletion of JavaScript expressions</span><span class="sxs-lookup"><span data-stu-id="9b588-130">**Console** autocompletion of JavaScript expressions</span></span>  
:::image-end:::  

## <a name="console-history"></a><span data-ttu-id="9b588-131">Histórico do console</span><span class="sxs-lookup"><span data-stu-id="9b588-131">Console history</span></span>

<span data-ttu-id="9b588-132">Assim como em muitas outras experiências de linha de comando, você também tem um histórico de comandos.</span><span class="sxs-lookup"><span data-stu-id="9b588-132">As with many other command-line experiences, you also have a history of commands.</span></span>  <span data-ttu-id="9b588-133">Selecione `Arrow Up` para exibir os comandos inseridos antes.</span><span class="sxs-lookup"><span data-stu-id="9b588-133">Select `Arrow Up` to display the commands you entered before.</span></span>  <span data-ttu-id="9b588-134">A comcompleção automática também mantém um histórico dos comandos digitados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9b588-134">Autocompletion also keeps a history of the commands you previously typed.</span></span>  <span data-ttu-id="9b588-135">Você pode digitar as primeiras letras de comandos anteriores e suas opções anteriores exibidas em uma caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="9b588-135">You may type the first few letters of earlier commands and your previous choices display in a textbox.</span></span>  

<span data-ttu-id="9b588-136">Além disso, **o Console** também oferece alguns métodos [utilitários que][DevtoolsConsoleUtilities] facilitam sua vida.</span><span class="sxs-lookup"><span data-stu-id="9b588-136">Also, the **Console** also offers quite a few [utility methods][DevtoolsConsoleUtilities] that make your life easier.</span></span>  <span data-ttu-id="9b588-137">Por exemplo, `$_` sempre contém o resultado da última expressão que você publicou no **Console**.</span><span class="sxs-lookup"><span data-stu-id="9b588-137">For example, `$_` always contains the result of the last expression you ran in the **Console**.</span></span>

:::image type="complex" source="../media/console-javascript-console-history.msft.png" alt-text="A expressão $_ no Console sempre contém o último resultado" lightbox="../media/console-javascript-console-history.msft.png":::
    <span data-ttu-id="9b588-139">A `$_` expressão no **Console** sempre contém o último resultado</span><span class="sxs-lookup"><span data-stu-id="9b588-139">The `$_` expression in the **Console** always contains the last result</span></span>  
:::image-end:::  

## <a name="multiline-edits"></a><span data-ttu-id="9b588-140">Edições de várias linhas</span><span class="sxs-lookup"><span data-stu-id="9b588-140">Multiline edits</span></span>

<span data-ttu-id="9b588-141">Por padrão, o **Console** fornece apenas uma linha para gravar sua expressão JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9b588-141">By default, the **Console** only gives you one line to write your JavaScript expression.</span></span>  <span data-ttu-id="9b588-142">O código é executado quando você seleciona `Enter` .</span><span class="sxs-lookup"><span data-stu-id="9b588-142">You code runs when you select `Enter`.</span></span> <span data-ttu-id="9b588-143">A limitação de uma linha pode frustrar você.</span><span class="sxs-lookup"><span data-stu-id="9b588-143">The one line limitation may frustrate you.</span></span>  <span data-ttu-id="9b588-144">Para trabalhar em torno da limitação de uma linha, selecione `Shift` + `Enter` em vez de `Enter` .</span><span class="sxs-lookup"><span data-stu-id="9b588-144">To work around the one line limitation, select `Shift`+`Enter` instead of `Enter`.</span></span>  <span data-ttu-id="9b588-145">No exemplo a seguir, o valor exibido é o resultado de todas as linhas em ordem.</span><span class="sxs-lookup"><span data-stu-id="9b588-145">In the following example, the value displayed is the result of all the lines run in order.</span></span>  

:::image type="complex" source="../media/console-javascript-multiline.msft.png" alt-text="Selecione Shift+Enter para gravar várias linhas de JavaScript e o valor resultante é executado em ordem" lightbox="../media/console-javascript-multiline.msft.png":::
   <span data-ttu-id="9b588-147">Selecione `Shift` + `Enter` para gravar várias linhas de JavaScript e o valor resultante é executado em ordem</span><span class="sxs-lookup"><span data-stu-id="9b588-147">Select `Shift`+`Enter` to write several lines of JavaScript and the resulting value is run in order</span></span>  
:::image-end:::  

<span data-ttu-id="9b588-148">Se você iniciar uma instrução multiline no **Console**, ela será automaticamente reconhecida e recuada.</span><span class="sxs-lookup"><span data-stu-id="9b588-148">If you start a multiline statement in the **Console**, it gets automatically recognized and indented.</span></span>  <span data-ttu-id="9b588-149">Por exemplo, se você iniciar uma instrução block com uma chaveta.</span><span class="sxs-lookup"><span data-stu-id="9b588-149">For example, if you start a block statement with a curly brace.</span></span>  

:::image type="complex" source="../media/console-javascript-automatic-lineindent.msft.png" alt-text="Console já reconhece expressões multi-linha usando chaves e recuos cada uma para você" lightbox="../media/console-javascript-automatic-lineindent.msft.png":::
    <span data-ttu-id="9b588-151">**Console** já reconhece expressões multi-linha usando chaves e recuos cada uma para você</span><span class="sxs-lookup"><span data-stu-id="9b588-151">**Console** already recognizes multiline expressions using curly braces and indents each for you</span></span>  
:::image-end:::  

## <a name="network-requests-using-top-level-await"></a><span data-ttu-id="9b588-152">Solicitações de rede usando o aguardado de nível superior()</span><span class="sxs-lookup"><span data-stu-id="9b588-152">Network requests using top-level await()</span></span>  

<span data-ttu-id="9b588-153">Além de seus próprios scripts, **o Console** oferece suporte a espera de nível superior para executar JavaScript assíncrono arbitrário nele. [][GithubTc39ProposalTopLevelAwait]</span><span class="sxs-lookup"><span data-stu-id="9b588-153">Other than in your own scripts, **Console** supports [top level await][GithubTc39ProposalTopLevelAwait] to run arbitrary asynchronous JavaScript in it.</span></span>  <span data-ttu-id="9b588-154">Por exemplo, use a `fetch` API sem envolver a `await` instrução com uma função assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9b588-154">For example, use the `fetch` API without wrapping the `await` statement with an async function.</span></span>  

<span data-ttu-id="9b588-155">Para obter os últimos 50 problemas arquivados nas Ferramentas de Desenvolvedor do Microsoft Edge para Visual Studio repositório [do GitHub][GithubMicrosoftVscodeEdgeDevtools] de Código, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="9b588-155">To get the last 50 issues filed on the [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] GitHub repo, complete the following actions.</span></span>  

1.  <span data-ttu-id="9b588-156">Abra o **Console**.</span><span class="sxs-lookup"><span data-stu-id="9b588-156">Open the **Console**.</span></span>  
1.  <span data-ttu-id="9b588-157">Copie e colar o trecho de código a seguir para obter um objeto que contém 10 entradas.</span><span class="sxs-lookup"><span data-stu-id="9b588-157">Copy and paste the following code snippet to get an object that contains 10 entries.</span></span>  
    
    ```javascript
    await ( await fetch(
    'https://api.github.com/repos/microsoft/vscode-edge-devtools/issues?state=all&per_page=50&page=1'
    )).json();
    ```  
    
:::image type="complex" source="../media/console-javascript-top-level-await.msft.png" alt-text="Console exibe o resultado de uma solicitação de busca assíncrona de nível superior" lightbox="../media/console-javascript-top-level-await.msft.png":::
    <span data-ttu-id="9b588-159">**Console** exibe o resultado de uma solicitação assíncrona de nível `fetch` superior</span><span class="sxs-lookup"><span data-stu-id="9b588-159">**Console** displays the result of a top-level async `fetch` request</span></span>  
:::image-end:::  

<span data-ttu-id="9b588-160">As 10 entradas são difíceis de reconhecer, pois muitas informações são exibidas.</span><span class="sxs-lookup"><span data-stu-id="9b588-160">The 10 entries are hard to recognize, since a lot of information is displayed.</span></span>  <span data-ttu-id="9b588-161">Felizmente, você pode usar o método log para receber apenas as informações nas quais `console.table()` você está interessado.</span><span class="sxs-lookup"><span data-stu-id="9b588-161">Luckily enough, you may use the `console.table()` log method to only receive the information in which you're interested.</span></span>  

:::image type="complex" source="../media/console-javascript-filtered-with-table.msft.png" alt-text="Exibir o último resultado em um formato acessível por humanos usando console.table" lightbox="../media/console-javascript-filtered-with-table.msft.png":::
    <span data-ttu-id="9b588-163">Exibir o último resultado em um formato acessível usando</span><span class="sxs-lookup"><span data-stu-id="9b588-163">Display the last result in a human readable format using</span></span> `console.table`  
:::image-end:::  

<span data-ttu-id="9b588-164">Para reutilizar os dados retornados de uma expressão, você pode usar o método `copy()` utilitário do **Console**.</span><span class="sxs-lookup"><span data-stu-id="9b588-164">To reuse the data returned from an expression, you may use the `copy()` utility method of the **Console**.</span></span>  <span data-ttu-id="9b588-165">O trecho de código a seguir envia a solicitação e copia os dados da resposta à área de transferência.</span><span class="sxs-lookup"><span data-stu-id="9b588-165">The following code snippet sends the request and copies the data from the response to the clipboard.</span></span>  

```javascript
copy(await (await fetch(
'https://api.github.com/repos/microsoft/vscode-edge-devtools/issues?state=all&per_page=50&page=1'
)).json())
```  

<span data-ttu-id="9b588-166">Use o **Console** como uma ótima maneira de praticar a funcionalidade JavaScript e fazer alguns cálculos rápidos.</span><span class="sxs-lookup"><span data-stu-id="9b588-166">Use the **Console** as a great way to practice JavaScript functionality and to do some quick calculations.</span></span>  <span data-ttu-id="9b588-167">A potência real é o fato de que você tem acesso ao [objeto window.][MdnDocsWebApiWindow]</span><span class="sxs-lookup"><span data-stu-id="9b588-167">The real power is the fact that you have access to the [window][MdnDocsWebApiWindow] object.</span></span>  <span data-ttu-id="9b588-168">Você pode [interagir com o DOM no Console.][DevtoolsConsoleConsoleDomInteraction]</span><span class="sxs-lookup"><span data-stu-id="9b588-168">You may [interact with the DOM in Console][DevtoolsConsoleConsoleDomInteraction].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="9b588-169">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9b588-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleDomInteraction]: ./console-dom-interaction.md "Use o Console para interagir com o dom | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Referência da API de Utilitários de Console | Microsoft Docs"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubTc39ProposalTopLevelAwait]: https://github.com/tc39/proposal-top-level-await "Proposta do ECMAScript: Espera de nível superior - tc39/proposal-top-level-await | GitHub"

[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Janela | MDN"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Loop de leitura-eval-print | Wikipédia"  
