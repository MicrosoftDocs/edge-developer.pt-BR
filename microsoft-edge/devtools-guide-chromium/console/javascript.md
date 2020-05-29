---
title: Começar a executar o JavaScript no console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 724d0e3c7c8439551538383e68a5fc4465eade94
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601723"
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







# <span data-ttu-id="d5d05-103">Começar a executar o JavaScript no console</span><span class="sxs-lookup"><span data-stu-id="d5d05-103">Get Started With Running JavaScript In The Console</span></span>   



<span data-ttu-id="d5d05-104">Este tutorial interativo mostra como executar JavaScript no console DevTools do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d5d05-104">This interactive tutorial shows you how to run JavaScript in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="d5d05-105">Consulte [introdução às mensagens de registro][DevToolsConsoleLoggingMessages] em log para saber como registrar mensagens no console.</span><span class="sxs-lookup"><span data-stu-id="d5d05-105">See [Get Started With Logging Messages][DevToolsConsoleLoggingMessages] to learn how to log messages to the Console.</span></span>  <span data-ttu-id="d5d05-106">Consulte [introdução à depuração de JavaScript][DevToolsJavascriptIndex] para saber como pausar o código JavaScript e passar por ele uma linha por vez.</span><span class="sxs-lookup"><span data-stu-id="d5d05-106">See [Get Started With Debugging JavaScript][DevToolsJavascriptIndex] to learn how to pause JavaScript code and step through it one line at a time.</span></span>  

> ##### <span data-ttu-id="d5d05-107">Figura 1</span><span class="sxs-lookup"><span data-stu-id="d5d05-107">Figure 1</span></span>  
> <span data-ttu-id="d5d05-108">O **console**</span><span class="sxs-lookup"><span data-stu-id="d5d05-108">The **Console**</span></span>  
> ![O console][ImageConsole]  

## <span data-ttu-id="d5d05-110">Visão geral</span><span class="sxs-lookup"><span data-stu-id="d5d05-110">Overview</span></span>   

<span data-ttu-id="d5d05-111">O **console** é [repl][WikiReadEvalPrintLoop], que significa ler, avaliar, imprimir e fazer loop.</span><span class="sxs-lookup"><span data-stu-id="d5d05-111">The **Console** is a [REPL][WikiReadEvalPrintLoop], which stands for Read, Evaluate, Print, and Loop.</span></span>  <span data-ttu-id="d5d05-112">Ele lê o JavaScript que você digita, avalia seu código, imprime o resultado da sua [expressão][2alityExpressionsVersusStatements]e, em seguida, volta para a primeira etapa.</span><span class="sxs-lookup"><span data-stu-id="d5d05-112">It reads the JavaScript that you type into it, evaluates your code, prints out the result of your [expression][2alityExpressionsVersusStatements], and then loops back to the first step.</span></span>  

## <span data-ttu-id="d5d05-113">Configurar o DevTools</span><span class="sxs-lookup"><span data-stu-id="d5d05-113">Set up DevTools</span></span>   

<span data-ttu-id="d5d05-114">Este tutorial foi projetado para você abrir a demonstração e experimentar todos os fluxos de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d5d05-114">This tutorial is designed for you to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="d5d05-115">Ao acompanhar fisicamente, é mais provável que você se lembre dos fluxos de trabalho mais tarde.</span><span class="sxs-lookup"><span data-stu-id="d5d05-115">When you physically follow along, you are more likely to remember the workflows later.</span></span>

1.  <span data-ttu-id="d5d05-116">Pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) para abrir o **console**.</span><span class="sxs-lookup"><span data-stu-id="d5d05-116">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console**.</span></span>  
1.  <span data-ttu-id="d5d05-117">Segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e clique em **exemplo de JavaScript do console** para abrir em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="d5d05-117">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **Console Javascript Example** to open in a new window.</span></span>  
    
    [<span data-ttu-id="d5d05-118">Exemplo de JavaScript do console</span><span class="sxs-lookup"><span data-stu-id="d5d05-118">Console Javascript Example</span></span>][GlitchConsoleJavascriptExample]  
    
    > ##### <span data-ttu-id="d5d05-119">Figura 2</span><span class="sxs-lookup"><span data-stu-id="d5d05-119">Figure 2</span></span>  
    > <span data-ttu-id="d5d05-120">A página de exemplo de JavaScript do console à esquerda e DevTools à direita</span><span class="sxs-lookup"><span data-stu-id="d5d05-120">The Console JavaScript Example page on the left, and DevTools on the right</span></span>  
    > ![A página de exemplo de JavaScript do console à esquerda e DevTools à direita][ImageTutorialDevToolsJs]  

## <span data-ttu-id="d5d05-122">Exibir e alterar o JavaScript ou o DOM da página</span><span class="sxs-lookup"><span data-stu-id="d5d05-122">View and change the JavaScript or DOM of the page</span></span>   

<span data-ttu-id="d5d05-123">Ao criar ou depurar uma página, geralmente é útil executar instruções no **console** para alterar a aparência ou a execução da página.</span><span class="sxs-lookup"><span data-stu-id="d5d05-123">When building or debugging a page, it is often useful to run statements in the **Console** in order to change how the page looks or runs.</span></span>  
    
1.  <span data-ttu-id="d5d05-124">Observe o texto no botão.</span><span class="sxs-lookup"><span data-stu-id="d5d05-124">Notice the text in the button.</span></span>  
1.  <span data-ttu-id="d5d05-125">Digite `document.getElementById('hello').textContent = 'Hello, Console!'` o **console** e, em seguida, pressione `Enter` para avaliar a expressão.</span><span class="sxs-lookup"><span data-stu-id="d5d05-125">Type `document.getElementById('hello').textContent = 'Hello, Console!'` in the **Console** and then press `Enter` to evaluate the expression.</span></span>  <span data-ttu-id="d5d05-126">Observe como o texto dentro do botão muda.</span><span class="sxs-lookup"><span data-stu-id="d5d05-126">Notice how the text inside the button changes.</span></span>  
    
    > ##### <span data-ttu-id="d5d05-127">Figura 3</span><span class="sxs-lookup"><span data-stu-id="d5d05-127">Figure 3</span></span>  
    > <span data-ttu-id="d5d05-128">Como o console se parece após avaliar a expressão</span><span class="sxs-lookup"><span data-stu-id="d5d05-128">How the Console looks after evaluating the expression</span></span>  
    > ![Como o console se parece após avaliar a expressão][ImageConsoleAfterEvaluating]  
    
    <span data-ttu-id="d5d05-130">Abaixo do código que você avaliou para ver `"Hello, Console!"` .</span><span class="sxs-lookup"><span data-stu-id="d5d05-130">Below the code that you evaluated you see `"Hello, Console!"`.</span></span>  <span data-ttu-id="d5d05-131">Lembre-se das 4 etapas de REPL: ler, avaliar, imprimir, repetir.</span><span class="sxs-lookup"><span data-stu-id="d5d05-131">Recall the 4 steps of REPL: read, evaluate, print, loop.</span></span>  <span data-ttu-id="d5d05-132">Depois de avaliar seu código, um REPL imprime o resultado da expressão.</span><span class="sxs-lookup"><span data-stu-id="d5d05-132">After evaluating your code, a REPL prints the result of the expression.</span></span>  <span data-ttu-id="d5d05-133">Portanto, `"Hello, Console!"` deve ser o resultado da avaliação `document.getElementById('hello').textContent = 'Hello, Console!'` .</span><span class="sxs-lookup"><span data-stu-id="d5d05-133">So `"Hello, Console!"` must be the result of evaluating `document.getElementById('hello').textContent = 'Hello, Console!'`.</span></span>  
    
## <span data-ttu-id="d5d05-134">Executar JavaScript arbitrário que não está relacionado à página</span><span class="sxs-lookup"><span data-stu-id="d5d05-134">Run arbitrary JavaScript that is not related to the page</span></span>   

<span data-ttu-id="d5d05-135">Às vezes, você só quer um código playground onde você pode testar algum código ou experimentar novos recursos JavaScript com os quais não está familiarizado.</span><span class="sxs-lookup"><span data-stu-id="d5d05-135">Sometimes, you just want a code playground where you are able to test some code, or try out new JavaScript features you are not familiar with.</span></span>  <span data-ttu-id="d5d05-136">O console é um lugar perfeito para estes tipos de experimentos.</span><span class="sxs-lookup"><span data-stu-id="d5d05-136">The Console is a perfect place for these kinds of experiments.</span></span>  

1.  <span data-ttu-id="d5d05-137">Digite `5 + 15` o console e pressione `Enter` para avaliar a expressão.</span><span class="sxs-lookup"><span data-stu-id="d5d05-137">Type `5 + 15` in the Console and press `Enter` to evaluate the expression.</span></span> <span data-ttu-id="d5d05-138">O console imprime o resultado da expressão abaixo do código.</span><span class="sxs-lookup"><span data-stu-id="d5d05-138">The Console prints out the result of the expression below your code.</span></span>  <span data-ttu-id="d5d05-139">A **Figura 4** abaixo mostra como deve ser a aparência do seu console depois da avaliação dessa expressão.</span><span class="sxs-lookup"><span data-stu-id="d5d05-139">**Figure 4** below shows how your Console should look after evaluating this expression.</span></span>  

1.  <span data-ttu-id="d5d05-140">Digite o código a seguir no **console**.</span><span class="sxs-lookup"><span data-stu-id="d5d05-140">Type the following code into the **Console**.</span></span>  <span data-ttu-id="d5d05-141">Tente digitá-lo, caractere por caractere, em vez de copiar-colar.</span><span class="sxs-lookup"><span data-stu-id="d5d05-141">Try typing it out, character-by-character, rather than copy-pasting it.</span></span>  
    
    ```javascript
    function add(a, b=20) {
        return a + b;
    }
    ```  
    
    <span data-ttu-id="d5d05-142">Consulte [definir valores padrão para argumentos de função][Esma6DefaultParameterValues] se você não estiver familiarizado com a `b=20` sintaxe.</span><span class="sxs-lookup"><span data-stu-id="d5d05-142">See [define default values for function arguments][Esma6DefaultParameterValues] if you are unfamiliar with the `b=20` syntax.</span></span>  
    
1.  <span data-ttu-id="d5d05-143">Agora, chame a função que você acabou de definir.</span><span class="sxs-lookup"><span data-stu-id="d5d05-143">Now, call the function that you just defined.</span></span>  
    
    ```javascript
    add(25);
    ```  
    
    > ##### <span data-ttu-id="d5d05-144">Figura 4</span><span class="sxs-lookup"><span data-stu-id="d5d05-144">Figure 4</span></span>  
    > <span data-ttu-id="d5d05-145">Como o console se parece após avaliar as expressões acima</span><span class="sxs-lookup"><span data-stu-id="d5d05-145">How the Console looks after evaluating the expressions above</span></span>  
    > ![Como o console se parece após avaliar as expressões acima][ImagePlayground]  
    
    `add(25)` <span data-ttu-id="d5d05-147">é avaliado `45` porque quando a `add` função é chamada sem um segundo argumento, o `b` padrão é `20` .</span><span class="sxs-lookup"><span data-stu-id="d5d05-147">evaluates to `45` because when the `add` function is called without a second argument, `b` defaults to `20`.</span></span>  

## <span data-ttu-id="d5d05-148">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="d5d05-148">Next steps</span></span>   

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

<span data-ttu-id="d5d05-149">DevTools permite pausar um script no meio da execução.</span><span class="sxs-lookup"><span data-stu-id="d5d05-149">DevTools lets you pause a script in the middle of running.</span></span>  <span data-ttu-id="d5d05-150">Durante a pausa, você pode usar o **console** para exibir e alterar a `window` ou `DOM` da página nesse momento.</span><span class="sxs-lookup"><span data-stu-id="d5d05-150">While you are paused, you may use the **Console** to view and change the `window` or `DOM` of the page at that moment in time.</span></span>  <span data-ttu-id="d5d05-151">Isso torna um fluxo de trabalho de depuração avançado.</span><span class="sxs-lookup"><span data-stu-id="d5d05-151">This makes for a powerful debugging workflow.</span></span>  <span data-ttu-id="d5d05-152">Consulte [introdução à depuração de JavaScript][DevToolsJavascriptIndex] para um tutorial interativo.</span><span class="sxs-lookup"><span data-stu-id="d5d05-152">See [Get Started With Debugging JavaScript][DevToolsJavascriptIndex] for an interactive tutorial.</span></span>  

<span data-ttu-id="d5d05-153">O **console** também tem um conjunto de funções de conveniência que facilita a interação com uma página.</span><span class="sxs-lookup"><span data-stu-id="d5d05-153">The **Console** also has a set of convenience functions that make it easier to interact with a page.</span></span>  <span data-ttu-id="d5d05-154">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d5d05-154">For example:</span></span>  

*   <span data-ttu-id="d5d05-155">Em vez de digitar `document.querySelector()` para selecionar um elemento, digite `$()` .</span><span class="sxs-lookup"><span data-stu-id="d5d05-155">Rather than typing `document.querySelector()` to select an element, type `$()`.</span></span>  <span data-ttu-id="d5d05-156">Essa sintaxe é inspirada pelo jQuery, mas não é realmente jQuery.</span><span class="sxs-lookup"><span data-stu-id="d5d05-156">This syntax is inspired by jQuery, but it is not actually jQuery.</span></span>  <span data-ttu-id="d5d05-157">É apenas um alias para `document.querySelector()` .</span><span class="sxs-lookup"><span data-stu-id="d5d05-157">It is just an alias for `document.querySelector()`.</span></span>  
*   `debug(function)` <span data-ttu-id="d5d05-158">define efetivamente um ponto de interrupção na primeira linha dessa função.</span><span class="sxs-lookup"><span data-stu-id="d5d05-158">effectively sets a breakpoint on the first line of that function.</span></span>  
*   `keys(object)` <span data-ttu-id="d5d05-159">Retorna uma matriz que contém as chaves do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="d5d05-159">returns an array containing the keys of the specified object.</span></span>  

<!--See [Console Utilities API Reference][DevToolsConsoleUtilities] to explore all the convenience functions.  -->  

<!--todo: add console utilities api reference section when available  -->  

 



<!-- image links -->  

[ImageConsole]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-playground.msft.png "Figura 1: o console"  
[ImageTutorialDevToolsJs]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-empty.msft.png "Figura 2: a página de exemplo de JavaScript do console à esquerda e DevTools à direita"  
[ImageConsoleAfterEvaluating]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-change-button-text.msft.png "Figura 3: aparência do console após a avaliação da expressão"  
[ImagePlayground]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-playground.msft.png "Figura 4: a aparência do console após a avaliação das expressões acima"  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: /microsoft-edge/devtools-guide-chromium/console/log "Introdução ao registro de mensagens no console"  
[DevToolsConsoleReference]: /microsoft-edge/devtools-guide-chromium/console/reference#run-javascript "Referência do console"  
[DevToolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium//console/utilities "Referência de API de utilitários de console"  

[DevToolsJavascriptIndex]: /microsoft-edge/devtools-guide-chromium/javascript/index "Introdução à depuração de JavaScript no Microsoft Edge DevTools"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Expressões versus instruções em JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Valores de parâmetro padrão-manipulação de parâmetro estendido-ECMAScript 6 – novos recursos: visão geral & comparação"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Exemplo de JavaScript do console | Problema"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Leitura – eval – loop de impressão-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="d5d05-172">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="d5d05-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d5d05-173">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/javascript) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="d5d05-173">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/javascript) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d5d05-175">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d5d05-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
