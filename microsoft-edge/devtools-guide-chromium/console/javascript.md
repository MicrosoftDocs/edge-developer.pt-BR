---
description: Saiba como executar JavaScript no console.
title: Começar a executar o JavaScript no console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: d31bcfbdf728e656c9a6fff882f939f8c24cd897
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993118"
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







# <span data-ttu-id="f9a61-104">Começar a executar o JavaScript no console</span><span class="sxs-lookup"><span data-stu-id="f9a61-104">Get Started With Running JavaScript In The Console</span></span>   



<span data-ttu-id="f9a61-105">Este tutorial interativo mostra como executar JavaScript no **console**devtools do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f9a61-105">This interactive tutorial shows you how to run JavaScript in the Microsoft Edge DevTools **Console**.</span></span>  <span data-ttu-id="f9a61-106">Para obter mais informações sobre como registrar mensagens no **console**, consulte [introdução ao registro de mensagens][DevToolsConsoleLoggingMessages].</span><span class="sxs-lookup"><span data-stu-id="f9a61-106">For more information about how to log messages to the **Console**, see [Get Started With Logging Messages][DevToolsConsoleLoggingMessages].</span></span>  <span data-ttu-id="f9a61-107">Para obter mais informações sobre como pausar o código JavaScript e passar por ele uma linha por vez, consulte [introdução à depuração de JavaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="f9a61-107">For more information about how to pause JavaScript code and step through it one line at a time, see [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="O console" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   <span data-ttu-id="f9a61-109">O **console**</span><span class="sxs-lookup"><span data-stu-id="f9a61-109">The **Console**</span></span>  
:::image-end:::  

## <span data-ttu-id="f9a61-110">Visão geral</span><span class="sxs-lookup"><span data-stu-id="f9a61-110">Overview</span></span>   

<span data-ttu-id="f9a61-111">O **console** é [repl][WikiReadEvalPrintLoop], que significa ler, avaliar, imprimir e fazer loop.</span><span class="sxs-lookup"><span data-stu-id="f9a61-111">The **Console** is a [REPL][WikiReadEvalPrintLoop], which stands for Read, Evaluate, Print, and Loop.</span></span>  <span data-ttu-id="f9a61-112">Ele lê o JavaScript que você digita, avalia seu código, imprime o resultado da sua [expressão][2alityExpressionsVersusStatements]e, em seguida, volta para a primeira etapa.</span><span class="sxs-lookup"><span data-stu-id="f9a61-112">It reads the JavaScript that you type into it, evaluates your code, prints out the result of your [expression][2alityExpressionsVersusStatements], and then loops back to the first step.</span></span>  

## <span data-ttu-id="f9a61-113">Configurar o DevTools</span><span class="sxs-lookup"><span data-stu-id="f9a61-113">Set up DevTools</span></span>   

<span data-ttu-id="f9a61-114">Este tutorial foi projetado para você abrir a demonstração e experimentar todos os fluxos de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f9a61-114">This tutorial is designed for you to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="f9a61-115">Ao acompanhar fisicamente, é mais provável que você se lembre dos fluxos de trabalho mais tarde.</span><span class="sxs-lookup"><span data-stu-id="f9a61-115">When you physically follow along, you are more likely to remember the workflows later.</span></span>

1.  <span data-ttu-id="f9a61-116">Pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) para abrir o **console**.</span><span class="sxs-lookup"><span data-stu-id="f9a61-116">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console**.</span></span>  
1.  <span data-ttu-id="f9a61-117">Segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e clique em **exemplo de JavaScript do console** para abrir em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="f9a61-117">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **Console Javascript Example** to open in a new window.</span></span>  
    
    *   [<span data-ttu-id="f9a61-118">Exemplo de JavaScript do console</span><span class="sxs-lookup"><span data-stu-id="f9a61-118">Console Javascript Example</span></span>][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="A página de exemplo de JavaScript do console à esquerda e DevTools à direita" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       <span data-ttu-id="f9a61-120">A página de exemplo de JavaScript do console à esquerda e DevTools à direita</span><span class="sxs-lookup"><span data-stu-id="f9a61-120">The Console JavaScript Example page on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f9a61-121">Exibir e alterar o JavaScript ou o DOM da página</span><span class="sxs-lookup"><span data-stu-id="f9a61-121">View and change the JavaScript or DOM of the page</span></span>   

<span data-ttu-id="f9a61-122">Ao criar ou depurar uma página, geralmente é útil executar instruções no **console** para alterar a aparência ou a execução da página.</span><span class="sxs-lookup"><span data-stu-id="f9a61-122">When building or debugging a page, it is often useful to run statements in the **Console** in order to change how the page looks or runs.</span></span>  
    
1.  <span data-ttu-id="f9a61-123">Observe o texto no botão.</span><span class="sxs-lookup"><span data-stu-id="f9a61-123">Notice the text in the button.</span></span>  
1.  <span data-ttu-id="f9a61-124">Digite `document.getElementById('hello').textContent = 'Hello, Console!'` o **console** e, em seguida, pressione `Enter` para avaliar a expressão.</span><span class="sxs-lookup"><span data-stu-id="f9a61-124">Type `document.getElementById('hello').textContent = 'Hello, Console!'` in the **Console** and then press `Enter` to evaluate the expression.</span></span>  <span data-ttu-id="f9a61-125">Observe como o texto dentro do botão muda.</span><span class="sxs-lookup"><span data-stu-id="f9a61-125">Notice how the text inside the button changes.</span></span>  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Como o console se parece após avaliar a expressão" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       <span data-ttu-id="f9a61-127">Como o **console** se parece após avaliar a expressão</span><span class="sxs-lookup"><span data-stu-id="f9a61-127">How the **Console** looks after evaluating the expression</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="f9a61-128">Abaixo do código que você avaliou para ver `"Hello, Console!"` .</span><span class="sxs-lookup"><span data-stu-id="f9a61-128">Below the code that you evaluated you see `"Hello, Console!"`.</span></span>  <span data-ttu-id="f9a61-129">Lembre-se das 4 etapas de REPL: ler, avaliar, imprimir, repetir.</span><span class="sxs-lookup"><span data-stu-id="f9a61-129">Recall the 4 steps of REPL: read, evaluate, print, loop.</span></span>  <span data-ttu-id="f9a61-130">Depois de avaliar seu código, um REPL imprime o resultado da expressão.</span><span class="sxs-lookup"><span data-stu-id="f9a61-130">After evaluating your code, a REPL prints the result of the expression.</span></span>  <span data-ttu-id="f9a61-131">Portanto, `"Hello, Console!"` deve ser o resultado da avaliação `document.getElementById('hello').textContent = 'Hello, Console!'` .</span><span class="sxs-lookup"><span data-stu-id="f9a61-131">So `"Hello, Console!"` must be the result of evaluating `document.getElementById('hello').textContent = 'Hello, Console!'`.</span></span>  
    
## <span data-ttu-id="f9a61-132">Executar JavaScript arbitrário que não está relacionado à página</span><span class="sxs-lookup"><span data-stu-id="f9a61-132">Run arbitrary JavaScript that is not related to the page</span></span>   

<span data-ttu-id="f9a61-133">Às vezes, você só quer um código playground onde você pode testar algum código ou experimentar novos recursos JavaScript com os quais não está familiarizado.</span><span class="sxs-lookup"><span data-stu-id="f9a61-133">Sometimes, you just want a code playground where you are able to test some code, or try out new JavaScript features you are not familiar with.</span></span>  <span data-ttu-id="f9a61-134">O console é um lugar perfeito para estes tipos de experimentos.</span><span class="sxs-lookup"><span data-stu-id="f9a61-134">The Console is a perfect place for these kinds of experiments.</span></span>  

1.  <span data-ttu-id="f9a61-135">Digite `5 + 15` o console e pressione `Enter` para avaliar a expressão.</span><span class="sxs-lookup"><span data-stu-id="f9a61-135">Type `5 + 15` in the Console and press `Enter` to evaluate the expression.</span></span> <span data-ttu-id="f9a61-136">O console imprime o resultado da expressão abaixo do código.</span><span class="sxs-lookup"><span data-stu-id="f9a61-136">The Console prints out the result of the expression below your code.</span></span>  <span data-ttu-id="f9a61-137">Na figura a seguir, o seu **console** deve exibir o resultado após avaliar a expressão.</span><span class="sxs-lookup"><span data-stu-id="f9a61-137">In the following figure, your **Console** should display the result after evaluating the expression.</span></span>  

1.  <span data-ttu-id="f9a61-138">Digite o código a seguir no **console**.</span><span class="sxs-lookup"><span data-stu-id="f9a61-138">Type the following code into the **Console**.</span></span>  <span data-ttu-id="f9a61-139">Tente digitá-lo, caractere por caractere, em vez de copiar-colar.</span><span class="sxs-lookup"><span data-stu-id="f9a61-139">Try typing it out, character-by-character, rather than copy-pasting it.</span></span>  
    
    ```javascript
    function add(a, b=20) { return a + b; }
    ```  
    
    <span data-ttu-id="f9a61-140">Se você não estiver familiarizado com a `b=20` sintaxe, consulte [definir valores padrão para argumentos de função][Esma6DefaultParameterValues].</span><span class="sxs-lookup"><span data-stu-id="f9a61-140">If you are unfamiliar with the `b=20` syntax, see [define default values for function arguments][Esma6DefaultParameterValues].</span></span>  
    
1.  <span data-ttu-id="f9a61-141">Agora, execute a função que você acabou de definir.</span><span class="sxs-lookup"><span data-stu-id="f9a61-141">Now, run the function that you just defined.</span></span>  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="O console é exibido após avaliar as expressões no trecho de código" lightbox="../media/console-javascript-example-console-playground.msft.png":::
             <span data-ttu-id="f9a61-143">O **console** é exibido após avaliar as expressões no trecho de código</span><span class="sxs-lookup"><span data-stu-id="f9a61-143">The **Console** displays after evaluating the expressions in the code snippet</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` <span data-ttu-id="f9a61-144">é avaliado `45` porque quando a `add` função é chamada sem um segundo argumento, o `b` padrão é `20` .</span><span class="sxs-lookup"><span data-stu-id="f9a61-144">evaluates to `45` because when the `add` function is called without a second argument, `b` defaults to `20`.</span></span>  

## <span data-ttu-id="f9a61-145">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="f9a61-145">Next steps</span></span>   

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

<span data-ttu-id="f9a61-146">DevTools permite pausar um script no meio da execução.</span><span class="sxs-lookup"><span data-stu-id="f9a61-146">DevTools lets you pause a script in the middle of running.</span></span>  <span data-ttu-id="f9a61-147">Durante a pausa, você pode usar o **console** para exibir e alterar a `window` ou `DOM` da página nesse momento.</span><span class="sxs-lookup"><span data-stu-id="f9a61-147">While you are paused, you may use the **Console** to view and change the `window` or `DOM` of the page at that moment in time.</span></span>  <span data-ttu-id="f9a61-148">O fluxo de trabalho torna um fluxo de trabalho avançado de depuração.</span><span class="sxs-lookup"><span data-stu-id="f9a61-148">The workflow makes for a powerful debugging workflow.</span></span>  <span data-ttu-id="f9a61-149">Para obter um tutorial interativo, consulte [introdução à depuração de JavaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="f9a61-149">For an interactive tutorial, see [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

<span data-ttu-id="f9a61-150">O **console** também tem um conjunto de funções de conveniência que facilita a interação com uma página.</span><span class="sxs-lookup"><span data-stu-id="f9a61-150">The **Console** also has a set of convenience functions that make it easier to interact with a page.</span></span>  <span data-ttu-id="f9a61-151">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f9a61-151">For example:</span></span>  

*   <span data-ttu-id="f9a61-152">Em vez de digitar `document.querySelector()` para selecionar um elemento, digite `$()` .</span><span class="sxs-lookup"><span data-stu-id="f9a61-152">Rather than typing `document.querySelector()` to select an element, type `$()`.</span></span>  <span data-ttu-id="f9a61-153">Essa sintaxe é inspirada pelo jQuery, mas não é realmente jQuery.</span><span class="sxs-lookup"><span data-stu-id="f9a61-153">This syntax is inspired by jQuery, but it is not actually jQuery.</span></span>  <span data-ttu-id="f9a61-154">É apenas um alias para `document.querySelector()` .</span><span class="sxs-lookup"><span data-stu-id="f9a61-154">It is just an alias for `document.querySelector()`.</span></span>  
*   `debug(function)` <span data-ttu-id="f9a61-155">define efetivamente um ponto de interrupção na primeira linha dessa função.</span><span class="sxs-lookup"><span data-stu-id="f9a61-155">effectively sets a breakpoint on the first line of that function.</span></span>  
*   `keys(object)` <span data-ttu-id="f9a61-156">Retorna uma matriz que contém as chaves do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="f9a61-156">returns an array containing the keys of the specified object.</span></span>  

<!--See [Console Utilities API Reference][DevToolsConsoleUtilities] to explore all the convenience functions.  -->  

<!--todo: add console utilities api reference section when available  -->  

 



<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Introdução ao registro de mensagens no console | Documentos da Microsoft"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Referência do console | Documentos da Microsoft"  
[DevToolsConsoleUtilities]: ./utilities.md "Referência de API de utilitários de console | Documentos da Microsoft"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Introdução à depuração de JavaScript no Microsoft Edge DevTools"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Expressões versus instruções em JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Valores de parâmetro padrão-manipulação de parâmetro estendido-ECMAScript 6 – novos recursos: visão geral & comparação"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Exemplo de JavaScript do console | Problema"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Leitura – eval – loop de impressão-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="f9a61-165">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="f9a61-165">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f9a61-166">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/javascript) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="f9a61-166">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/javascript) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f9a61-168">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f9a61-168">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
