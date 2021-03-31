---
description: Saiba como executar JavaScript no Console.
title: Começar a executar JavaScript no Console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c1d6c393b6278f4622cf80576ccc8f9c70bdb6b5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398816"
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

# <a name="get-started-with-running-javascript-in-the-console"></a><span data-ttu-id="1d684-104">Começar a executar JavaScript no Console</span><span class="sxs-lookup"><span data-stu-id="1d684-104">Get started with running JavaScript in the Console</span></span>  

<span data-ttu-id="1d684-105">Este tutorial interativo mostra como executar o JavaScript no  Console do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="1d684-105">This interactive tutorial shows you how to run JavaScript in the Microsoft Edge DevTools **Console**.</span></span>  <span data-ttu-id="1d684-106">Para obter mais informações sobre como registrar mensagens no **Console,** navegue até [Começar a registrar mensagens][DevToolsConsoleLoggingMessages].</span><span class="sxs-lookup"><span data-stu-id="1d684-106">For more information about how to log messages to the **Console**, navigate to [Get Started With Logging Messages][DevToolsConsoleLoggingMessages].</span></span>  <span data-ttu-id="1d684-107">Para obter mais informações sobre como pausar o código JavaScript e percorrer uma linha por vez, navegue até Começar a [depurar JavaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="1d684-107">For more information about how to pause JavaScript code and step through it one line at a time, navigate to [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="O Console" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   <span data-ttu-id="1d684-109">O **Console**</span><span class="sxs-lookup"><span data-stu-id="1d684-109">The **Console**</span></span>  
:::image-end:::  

## <a name="overview"></a><span data-ttu-id="1d684-110">Visão geral</span><span class="sxs-lookup"><span data-stu-id="1d684-110">Overview</span></span>  

<span data-ttu-id="1d684-111">O **Console** é um [REPL][WikiReadEvalPrintLoop], que significa Leitura, Avaliação, Impressão e Loop.</span><span class="sxs-lookup"><span data-stu-id="1d684-111">The **Console** is a [REPL][WikiReadEvalPrintLoop], which stands for Read, Evaluate, Print, and Loop.</span></span>  <span data-ttu-id="1d684-112">Ele lê o JavaScript que você digita nele, avalia seu código, imprime o resultado de sua expressão [e,][2alityExpressionsVersusStatements]em seguida, faz um loop de volta para a primeira etapa.</span><span class="sxs-lookup"><span data-stu-id="1d684-112">It reads the JavaScript that you type into it, evaluates your code, prints out the result of your [expression][2alityExpressionsVersusStatements], and then loops back to the first step.</span></span>  

## <a name="set-up-devtools"></a><span data-ttu-id="1d684-113">Configurar o DevTools</span><span class="sxs-lookup"><span data-stu-id="1d684-113">Set up DevTools</span></span>  

<span data-ttu-id="1d684-114">Este tutorial foi projetado para você abrir a demonstração e experimentar todos os fluxos de trabalho por conta própria.</span><span class="sxs-lookup"><span data-stu-id="1d684-114">This tutorial is designed for you to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="1d684-115">Quando você acompanha fisicamente, é mais provável que você se lembre mais tarde dos fluxos de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1d684-115">When you physically follow along, you are more likely to remember the workflows later.</span></span>

1.  <span data-ttu-id="1d684-116">Selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\) para abrir o **Console**.</span><span class="sxs-lookup"><span data-stu-id="1d684-116">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open the **Console**.</span></span>  
1.  <span data-ttu-id="1d684-117">Segure `Control` \(Windows, Linux\) ou `Command` \(macOS\) e escolha **Console Javascript Example** para abrir em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="1d684-117">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Javascript Example** to open in a new window.</span></span>  
    
    *   [<span data-ttu-id="1d684-118">Exemplo de Javascript do Console</span><span class="sxs-lookup"><span data-stu-id="1d684-118">Console Javascript Example</span></span>][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="A página Exemplo javascript do console à esquerda e o DevTools à direita" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       <span data-ttu-id="1d684-120">A página Exemplo javascript do console à esquerda e o DevTools à direita</span><span class="sxs-lookup"><span data-stu-id="1d684-120">The Console JavaScript Example page on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
## <a name="view-and-change-the-javascript-or-dom-of-the-page"></a><span data-ttu-id="1d684-121">Exibir e alterar o JavaScript ou DOM da página</span><span class="sxs-lookup"><span data-stu-id="1d684-121">View and change the JavaScript or DOM of the page</span></span>  

<span data-ttu-id="1d684-122">Ao criar ou depurar uma página, geralmente é útil executar instruções no **Console** para alterar a aparência ou a aparência da página.</span><span class="sxs-lookup"><span data-stu-id="1d684-122">When building or debugging a page, it is often useful to run statements in the **Console** in order to change how the page looks or runs.</span></span>  
    
1.  <span data-ttu-id="1d684-123">Observe o texto no botão.</span><span class="sxs-lookup"><span data-stu-id="1d684-123">Notice the text in the button.</span></span>  
1.  <span data-ttu-id="1d684-124">Digite `document.getElementById('hello').textContent = 'Hello, Console!'` o Console **e** selecione para avaliar `Enter` a expressão.</span><span class="sxs-lookup"><span data-stu-id="1d684-124">Type `document.getElementById('hello').textContent = 'Hello, Console!'` in the **Console** and then select `Enter` to evaluate the expression.</span></span>  <span data-ttu-id="1d684-125">Observe como o texto dentro do botão muda.</span><span class="sxs-lookup"><span data-stu-id="1d684-125">Notice how the text inside the button changes.</span></span>  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Como o Console fica depois de avaliar a expressão" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       <span data-ttu-id="1d684-127">Como o **Console fica** depois de avaliar a expressão</span><span class="sxs-lookup"><span data-stu-id="1d684-127">How the **Console** looks after evaluating the expression</span></span>  
    :::image-end:::  
    
    `"Hello, Console!"`<span data-ttu-id="1d684-128">, é exibido abaixo do código avaliado.</span><span class="sxs-lookup"><span data-stu-id="1d684-128">, is displayed below the code that you evaluated.</span></span>  <span data-ttu-id="1d684-129">Lembre-se das 4 etapas do REPL: leitura, avaliação, impressão, loop.</span><span class="sxs-lookup"><span data-stu-id="1d684-129">Remember the 4 steps of REPL: read, evaluate, print, loop.</span></span>  <span data-ttu-id="1d684-130">Depois de avaliar seu código, uma REPL imprime o resultado da expressão.</span><span class="sxs-lookup"><span data-stu-id="1d684-130">After evaluating your code, a REPL prints the result of the expression.</span></span>  <span data-ttu-id="1d684-131">Portanto, `"Hello, Console!"` deve ser o resultado da avaliação `document.getElementById('hello').textContent = 'Hello, Console!'` .</span><span class="sxs-lookup"><span data-stu-id="1d684-131">So `"Hello, Console!"` must be the result of evaluating `document.getElementById('hello').textContent = 'Hello, Console!'`.</span></span>  
    
## <a name="run-arbitrary-javascript-that-is-not-related-to-the-page"></a><span data-ttu-id="1d684-132">Executar JavaScript arbitrário que não está relacionado à página</span><span class="sxs-lookup"><span data-stu-id="1d684-132">Run arbitrary JavaScript that is not related to the page</span></span>  

<span data-ttu-id="1d684-133">Às vezes, você só quer um playground de código onde você pode testar algum código ou experimentar novos recursos JavaScript com os quais não está familiarizado.</span><span class="sxs-lookup"><span data-stu-id="1d684-133">Sometimes, you just want a code playground where you are able to test some code, or try out new JavaScript features you are not familiar with.</span></span>  <span data-ttu-id="1d684-134">O **Console** é um lugar perfeito para esses tipos de experimentos.</span><span class="sxs-lookup"><span data-stu-id="1d684-134">The **Console** is a perfect place for these kinds of experiments.</span></span>  

1.  <span data-ttu-id="1d684-135">Digite `5 + 15` o Console e selecione para avaliar a `Enter` expressão.</span><span class="sxs-lookup"><span data-stu-id="1d684-135">Type `5 + 15` in the Console and select `Enter` to evaluate the expression.</span></span> <span data-ttu-id="1d684-136">O Console imprime o resultado da expressão abaixo do código.</span><span class="sxs-lookup"><span data-stu-id="1d684-136">The Console prints out the result of the expression below your code.</span></span>  <span data-ttu-id="1d684-137">Na figura a seguir, seu **Console** deve exibir o resultado após avaliar a expressão.</span><span class="sxs-lookup"><span data-stu-id="1d684-137">In the following figure, your **Console** should display the result after evaluating the expression.</span></span>  

1.  <span data-ttu-id="1d684-138">Digite o código a seguir no **Console**.</span><span class="sxs-lookup"><span data-stu-id="1d684-138">Type the following code into the **Console**.</span></span>  <span data-ttu-id="1d684-139">Tente digitá-lo, de caractere por caractere, em vez de copiá-lo.</span><span class="sxs-lookup"><span data-stu-id="1d684-139">Try typing it out, character-by-character, rather than copy-pasting it.</span></span>  
    
    ```javascript
    function add(a, b=20)
    ```  
    
    <span data-ttu-id="1d684-140">Se você não estiver familiarizado com a `b=20` sintaxe, navegue para [definir valores padrão para argumentos de função][Esma6DefaultParameterValues].</span><span class="sxs-lookup"><span data-stu-id="1d684-140">If you are unfamiliar with the `b=20` syntax, navigate to [define default values for function arguments][Esma6DefaultParameterValues].</span></span>  
    
1.  <span data-ttu-id="1d684-141">Agora, execute a função que você acabou de definir.</span><span class="sxs-lookup"><span data-stu-id="1d684-141">Now, run the function that you just defined.</span></span>  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="O Console é exibido após avaliar as expressões no trecho de código" lightbox="../media/console-javascript-example-console-playground.msft.png":::
             <span data-ttu-id="1d684-143">O **Console** é exibido após avaliar as expressões no trecho de código</span><span class="sxs-lookup"><span data-stu-id="1d684-143">The **Console** displays after evaluating the expressions in the code snippet</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` <span data-ttu-id="1d684-144">avalia porque `45` quando a função é chamada sem um segundo `add` argumento, o padrão é `b` `20` .</span><span class="sxs-lookup"><span data-stu-id="1d684-144">evaluates to `45` because when the `add` function is called without a second argument, `b` defaults to `20`.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="1d684-145">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="1d684-145">Next steps</span></span>  

<!--To explore more features related to running JavaScript in the **Console**, navigate to [Run JavaScript][DevToolsConsoleReference].  -->  

<!--todo: add console reference (run javascript) section when available  -->  

<span data-ttu-id="1d684-146">O DevTools permite pausar um script no meio da execução.</span><span class="sxs-lookup"><span data-stu-id="1d684-146">DevTools lets you pause a script in the middle of running.</span></span>  <span data-ttu-id="1d684-147">Enquanto você está pausado, você pode usar o **Console** para exibir e alterar o ou da `window` página nesse momento no `DOM` tempo.</span><span class="sxs-lookup"><span data-stu-id="1d684-147">While you are paused, you may use the **Console** to view and change the `window` or `DOM` of the page at that moment in time.</span></span>  <span data-ttu-id="1d684-148">O fluxo de trabalho faz com que um fluxo de trabalho de depuração poderoso.</span><span class="sxs-lookup"><span data-stu-id="1d684-148">The workflow makes for a powerful debugging workflow.</span></span>  <span data-ttu-id="1d684-149">Para obter um tutorial interativo, navegue até [Introdução à Depuração de JavaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="1d684-149">For an interactive tutorial, navigate to [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

<span data-ttu-id="1d684-150">O **Console** também tem um conjunto de funções de conveniência que facilitam a interação com uma página.</span><span class="sxs-lookup"><span data-stu-id="1d684-150">The **Console** also has a set of convenience functions that make it easier to interact with a page.</span></span>  <span data-ttu-id="1d684-151">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1d684-151">For example:</span></span>  

*   <span data-ttu-id="1d684-152">Em vez de digitar `document.querySelector()` para selecionar um elemento, digite `$()` .</span><span class="sxs-lookup"><span data-stu-id="1d684-152">Rather than typing `document.querySelector()` to select an element, type `$()`.</span></span>  <span data-ttu-id="1d684-153">Essa sintaxe é inspirada por jQuery, mas não é realmente jQuery.</span><span class="sxs-lookup"><span data-stu-id="1d684-153">This syntax is inspired by jQuery, but it is not actually jQuery.</span></span>  <span data-ttu-id="1d684-154">É apenas um alias para `document.querySelector()` .</span><span class="sxs-lookup"><span data-stu-id="1d684-154">It is just an alias for `document.querySelector()`.</span></span>  
*   `debug(function)` <span data-ttu-id="1d684-155">define efetivamente um ponto de interrupção na primeira linha dessa função.</span><span class="sxs-lookup"><span data-stu-id="1d684-155">effectively sets a breakpoint on the first line of that function.</span></span>  
*   `keys(object)` <span data-ttu-id="1d684-156">retorna uma matriz que contém as chaves do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="1d684-156">returns an array containing the keys of the specified object.</span></span>  

<span data-ttu-id="1d684-157">Para obter mais informações sobre as funções de conveniência, navegue até [Console Utilities API Reference][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="1d684-157">For more information about the convenience functions, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="1d684-158">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1d684-158">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Começar a registrar mensagens no console | Microsoft Docs"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Console reference | Microsoft Docs"  
[DevToolsConsoleUtilities]: ./utilities.md "Referência da API de Utilitários de Console | Microsoft Docs"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Começar a depurar JavaScript no Microsoft Edge DevTools | Microsoft Docs"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Expressões versus instruções em JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Valores de parâmetro padrão - Tratamento de parâmetros estendidos - ECMAScript 6 — Novos recursos: visão geral & comparação"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Exemplo javascript de console | Glitch"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Loop de leitura-eval-print - Wikipédia"  

> [!NOTE]
> <span data-ttu-id="1d684-167">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1d684-167">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1d684-168">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/javascript) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="1d684-168">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/javascript) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1d684-170">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1d684-170">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
