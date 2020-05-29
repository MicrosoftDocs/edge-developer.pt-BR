---
title: Visão geral do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 6062afb929a5d763c095d4915a2960993bc5ab4c
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601779"
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





# <span data-ttu-id="43e00-103">Visão geral do console</span><span class="sxs-lookup"><span data-stu-id="43e00-103">Console Overview</span></span>   

  

<span data-ttu-id="43e00-104">Esta página explica como o console do Microsoft Edge DevTools torna mais fácil o desenvolvimento de páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="43e00-104">This page explains how the Microsoft Edge DevTools Console makes it easier to develop web pages.</span></span>  <span data-ttu-id="43e00-105">O console tem dois usos principais: [Exibir mensagens registradas](#viewing-logged-messages) e [executar JavaScript](#running-javascript).</span><span class="sxs-lookup"><span data-stu-id="43e00-105">The Console has 2 main uses: [viewing logged messages](#viewing-logged-messages) and [running JavaScript](#running-javascript).</span></span>  

## <span data-ttu-id="43e00-106">Exibir mensagens registradas</span><span class="sxs-lookup"><span data-stu-id="43e00-106">Viewing logged messages</span></span>   

<span data-ttu-id="43e00-107">Os desenvolvedores da Web geralmente registram mensagens no console para verificar se o JavaScript está funcionando conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="43e00-107">Web developers often log messages to the Console to make sure that their JavaScript is working as expected.</span></span>  <span data-ttu-id="43e00-108">Para registrar uma mensagem, insira uma expressão como `console.log('Hello, Console!')` em seu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="43e00-108">To log a message, you insert an expression like `console.log('Hello, Console!')` into your JavaScript.</span></span>  <span data-ttu-id="43e00-109">Quando o navegador executa o JavaScript e vê uma expressão como essa, ele registra a mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="43e00-109">When the browser runs your JavaScript and sees an expression like that, it logs the message to the Console.</span></span>  <span data-ttu-id="43e00-110">Por exemplo, suponha que você esteja escrevendo o HTML e JavaScript para uma página:</span><span class="sxs-lookup"><span data-stu-id="43e00-110">For example, suppose that you are writing the HTML and JavaScript for a page:</span></span>  

```html
<!doctype html>
<html>
  <head>
    <title>Console Demo</title>
  </head>
  <body>
    <h1>Hello, World!</h1>
    <script>
      console.log('Loading!');
      const h1 = document.querySelector('h1');
      console.log(h1.textContent);
      console.assert(document.querySelector('h2'), 'h2 not found!');
      const artists = [
        {
          first: 'René',
          last: 'Magritte'
        },
        {
          first: 'Chaim',
          last: 'Soutine'
        },
        {
          first: 'Henri',
          last: 'Matisse'
        }
      ];
      console.table(artists);
      setTimeout(() => {
        h1.textContent = 'Hello, Console!';
        console.log(h1.textContent);
      }, 3000);
    </script>
  </body>
</html>
```  

<span data-ttu-id="43e00-111">A [Figura 1](#figure-1) mostra como é a aparência do console depois de carregar a página e esperar 3 segundos.</span><span class="sxs-lookup"><span data-stu-id="43e00-111">[Figure 1](#figure-1) shows what the Console looks like after loading the page and waiting 3 seconds.</span></span>  <span data-ttu-id="43e00-112">Tente descobrir quais linhas de código fizeram o navegador registrar as mensagens.</span><span class="sxs-lookup"><span data-stu-id="43e00-112">Try to figure out which lines of code caused the browser to log the messages.</span></span>  

> ##### <span data-ttu-id="43e00-113">Figura 1</span><span class="sxs-lookup"><span data-stu-id="43e00-113">Figure 1</span></span>  
> <span data-ttu-id="43e00-114">Painel do console</span><span class="sxs-lookup"><span data-stu-id="43e00-114">The Console panel</span></span>  
> ![Painel do console][ImageConsole]  

<span data-ttu-id="43e00-116">Os desenvolvedores da Web registram mensagens por dois motivos gerais:</span><span class="sxs-lookup"><span data-stu-id="43e00-116">Web developers log messages for 2 general reasons:</span></span>  

*   <span data-ttu-id="43e00-117">Verificar se o código está em execução na ordem correta.</span><span class="sxs-lookup"><span data-stu-id="43e00-117">Making sure that code is running in the right order.</span></span>  
*   <span data-ttu-id="43e00-118">Inspecionar os valores de variáveis em um determinado momento no tempo.</span><span class="sxs-lookup"><span data-stu-id="43e00-118">Inspecting the values of variables at a certain moment in time.</span></span>  

<span data-ttu-id="43e00-119">Consulte [introdução ao registro de mensagens][DevtoolsConsoleLoggingMessages] para obter experiência prática com o registro em log.</span><span class="sxs-lookup"><span data-stu-id="43e00-119">See [Get Started With Logging Messages][DevtoolsConsoleLoggingMessages] to get hands-on experience with logging.</span></span>  <span data-ttu-id="43e00-120">Consulte a [referência de API do console][DevToolsConsoleAPI] para procurar a lista completa de `console` métodos.</span><span class="sxs-lookup"><span data-stu-id="43e00-120">See the [Console API Reference][DevToolsConsoleAPI] to browse the full list of `console` methods.</span></span>  <span data-ttu-id="43e00-121">A principal diferença entre os métodos é como os dados que estão sendo registrados são exibidos.</span><span class="sxs-lookup"><span data-stu-id="43e00-121">The main difference between the methods is how the data being logged is displayed.</span></span>  

## <span data-ttu-id="43e00-122">Executando JavaScript</span><span class="sxs-lookup"><span data-stu-id="43e00-122">Running JavaScript</span></span>   

<span data-ttu-id="43e00-123">O console também é um [repl][WikiREPLoop].</span><span class="sxs-lookup"><span data-stu-id="43e00-123">The Console is also a [REPL][WikiREPLoop].</span></span>  <span data-ttu-id="43e00-124">Você pode executar JavaScript no console para interagir com a página que está sendo inspecionada.</span><span class="sxs-lookup"><span data-stu-id="43e00-124">You may run JavaScript in the Console to interact with the page being inspected.</span></span>  <span data-ttu-id="43e00-125">Por exemplo, a [Figura 2](#figure-2) mostra o console ao lado da home page do devtools, e a [Figura 3](#figure-3) mostra essa mesma página depois de usar o console para alterar o título superior da página.</span><span class="sxs-lookup"><span data-stu-id="43e00-125">For example, [Figure 2](#figure-2) shows the Console next to the DevTools homepage, and [Figure 3](#figure-3) shows that same page after using the Console to change the top heading of the page.</span></span>  

> ##### <span data-ttu-id="43e00-126">Figura 2</span><span class="sxs-lookup"><span data-stu-id="43e00-126">Figure 2</span></span>  
> <span data-ttu-id="43e00-127">O painel do console ao lado da home page do DevTools</span><span class="sxs-lookup"><span data-stu-id="43e00-127">The Console panel next to the DevTools homepage</span></span>  
> ![O painel do console ao lado da home page do DevTools][ImageConsoleOverview]  

> ##### <span data-ttu-id="43e00-129">Figura 3</span><span class="sxs-lookup"><span data-stu-id="43e00-129">Figure 3</span></span>  
> <span data-ttu-id="43e00-130">Usar o console para alterar o título superior da página</span><span class="sxs-lookup"><span data-stu-id="43e00-130">Using the Console to change the top heading of the page</span></span>  
> ![Usar o console para alterar o título superior da página][ImageConsoleChangeTitle]  

<span data-ttu-id="43e00-132">A modificação da página no console é possível porque o console tem acesso completo à [janela][MDNWindow] da página.</span><span class="sxs-lookup"><span data-stu-id="43e00-132">Modifying the page from the Console is possible because the Console has full access to the [window][MDNWindow] of the page.</span></span>  <span data-ttu-id="43e00-133">O DevTools tem algumas funções de conveniência que facilitam a inspeção de uma página.</span><span class="sxs-lookup"><span data-stu-id="43e00-133">DevTools has a few convenience functions that make it easier to inspect a page.</span></span>  <span data-ttu-id="43e00-134">Por exemplo, suponha que o JavaScript contenha uma função chamada `hideModal` .</span><span class="sxs-lookup"><span data-stu-id="43e00-134">For example, suppose that your JavaScript contains a function called `hideModal`.</span></span>  <span data-ttu-id="43e00-135">Executar `debug(hideModal)` pausa o código na primeira linha da `hideModal` próxima vez que você executá-lo.</span><span class="sxs-lookup"><span data-stu-id="43e00-135">Running `debug(hideModal)` pauses your code on the first line of `hideModal` the next time that you run it.</span></span>  <span data-ttu-id="43e00-136">Consulte [referência da API de utilitários de console][DevtoolsConsoleUtilitiesDebug] para ver a lista completa de funções de utilitário.</span><span class="sxs-lookup"><span data-stu-id="43e00-136">See [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug] to see the full list of utility functions.</span></span>  

<span data-ttu-id="43e00-137">Quando você executa JavaScript, você não precisa interagir com a página.</span><span class="sxs-lookup"><span data-stu-id="43e00-137">When you run JavaScript you do not have to interact with the page.</span></span>  <span data-ttu-id="43e00-138">Você pode usar o console para experimentar um novo código não relacionado à página.</span><span class="sxs-lookup"><span data-stu-id="43e00-138">You may use the Console to try out new code unrelated to the page.</span></span>  <span data-ttu-id="43e00-139">Por exemplo, suponha que você tenha aprendido apenas sobre o método interno de mapas de matrizes JavaScript [()][MDNMap] e queira experimentá-lo.</span><span class="sxs-lookup"><span data-stu-id="43e00-139">For example, suppose you just learned about the built-in JavaScript Array [map()][MDNMap] method, and you want to experiment with it.</span></span>  
<span data-ttu-id="43e00-140">O **console** é um bom lugar para experimentar a função.</span><span class="sxs-lookup"><span data-stu-id="43e00-140">The **Console** is a good place to try out the function.</span></span>  

<span data-ttu-id="43e00-141">Consulte [introdução à execução de JavaScript][ImageConsoleChangeTitle] para obter experiência prática com a execução de JavaScript no console.</span><span class="sxs-lookup"><span data-stu-id="43e00-141">See [Get Started With Running JavaScript][ImageConsoleChangeTitle] to get hands-on experience with running JavaScript in the Console.</span></span>  

   

  

<!-- image links -->  

[ImageConsole]: /microsoft-edge/devtools-guide-chromium/media/console-console-demo.msft.png "Figura 1: painel do console"  
[ImageConsoleChangeTitle]: /microsoft-edge/devtools-guide-chromium/media/devtools-console-h1-changed.msft.png "Figura 3: usar o console para alterar o título superior da página"  
[ImageConsoleOverview]: /microsoft-edge/devtools-guide-chromium/media/devtools-console-empty.msft.png "Figura 2: painel do console ao lado da home page do DevTools"  

<!-- links -->  

[DevToolsConsoleAPI]: /microsoft-edge/devtools-guide-chromium/console/api "Referência de API do console"  
[DevtoolsConsoleLoggingMessages]: /microsoft-edge/devtools-guide-chromium/console/log "Introdução ao registro de mensagens no console"  
[DevtoolsConsoleRunningJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Começar a executar o JavaScript no console"  
[DevtoolsConsoleUtilitiesDebug]: /microsoft-edge/devtools-guide-chromium/console/utilities#debug "Referência de API de utilitários de console de depuração"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array. prototype. Map () | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Janela | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Leitura – eval – loop de impressão-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="43e00-152">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="43e00-152">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="43e00-153">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="43e00-153">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="43e00-155">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="43e00-155">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
