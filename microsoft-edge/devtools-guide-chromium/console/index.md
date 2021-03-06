---
description: Os principais usos do Console do Microsoft Edge DevTools são registrar mensagens e executar JavaScript.
title: Visão geral do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 496caa4d304d9511d4b1c341846f377899ba4597
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399117"
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

# <a name="console-overview"></a><span data-ttu-id="e2be0-104">Visão geral do console</span><span class="sxs-lookup"><span data-stu-id="e2be0-104">Console overview</span></span>  

  

<span data-ttu-id="e2be0-105">Esta página explica como o Console do Microsoft Edge DevTools facilita o desenvolvimento de páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="e2be0-105">This page explains how the Microsoft Edge DevTools Console makes it easier to develop web pages.</span></span>  <span data-ttu-id="e2be0-106">O **Console** tem 2 usos principais: [exibição de mensagens registradas e](#viewing-logged-messages) execução de [JavaScript](#running-javascript).</span><span class="sxs-lookup"><span data-stu-id="e2be0-106">The **Console** has 2 main uses: [viewing logged messages](#viewing-logged-messages) and [running JavaScript](#running-javascript).</span></span>  

## <a name="viewing-logged-messages"></a><span data-ttu-id="e2be0-107">Exibindo mensagens registradas</span><span class="sxs-lookup"><span data-stu-id="e2be0-107">Viewing logged messages</span></span>  

<span data-ttu-id="e2be0-108">Os desenvolvedores da Web geralmente registram mensagens no Console para garantir que o JavaScript deles está funcionando conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="e2be0-108">Web developers often log messages to the Console to make sure that their JavaScript is working as expected.</span></span>  <span data-ttu-id="e2be0-109">Para registrar uma mensagem, insira uma expressão como `console.log('Hello, Console!')` em seu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e2be0-109">To log a message, you insert an expression like `console.log('Hello, Console!')` into your JavaScript.</span></span>  <span data-ttu-id="e2be0-110">Quando o navegador executa o JavaScript e processa uma expressão como essa, o navegador registra a mensagem no **Console**.</span><span class="sxs-lookup"><span data-stu-id="e2be0-110">When the browser runs your JavaScript and processes an expression like it, the browser logs the message to the **Console**.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e2be0-111">O HTML e JavaScript para a página.</span><span class="sxs-lookup"><span data-stu-id="e2be0-111">The HTML and JavaScript for the page.</span></span>  
      
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
                      { first: 'René', last: 'Magritte' },
                      { first: 'Chaim', last: 'Soutine' },
                        
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
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="e2be0-112">Na figura a seguir, o **Console** exibe os resultados de carregar a página e aguardar 3 segundos.</span><span class="sxs-lookup"><span data-stu-id="e2be0-112">In the following figure, the **Console** displays the results of loading the page and waiting 3 seconds.</span></span>  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="O painel Console" lightbox="../media/console-console-demo.msft.png":::
         <span data-ttu-id="e2be0-114">A **ferramenta Console**</span><span class="sxs-lookup"><span data-stu-id="e2be0-114">The **Console** tool</span></span>  
      :::image-end:::  
      
      <span data-ttu-id="e2be0-115">Tente determinar quais linhas de código fizeram com que o navegador registrava as mensagens.</span><span class="sxs-lookup"><span data-stu-id="e2be0-115">Try to determine which lines of code caused the browser to log the messages.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e2be0-116">Os desenvolvedores da Web registram mensagens pelos dois motivos gerais a seguir.</span><span class="sxs-lookup"><span data-stu-id="e2be0-116">Web developers log messages for the following 2 general reasons.</span></span>  

*   <span data-ttu-id="e2be0-117">Certifique-se de que o código está sendo executado na ordem certa.</span><span class="sxs-lookup"><span data-stu-id="e2be0-117">Making sure that code is running in the right order.</span></span>  
*   <span data-ttu-id="e2be0-118">Inspecionando os valores das variáveis em um determinado momento no tempo.</span><span class="sxs-lookup"><span data-stu-id="e2be0-118">Inspecting the values of variables at a certain moment in time.</span></span>  

<span data-ttu-id="e2be0-119">Para obter a experiência prática com o registro em log, navegue até [Começar a registrar mensagens][DevtoolsConsoleLoggingMessages].</span><span class="sxs-lookup"><span data-stu-id="e2be0-119">To get hands-on experience with logging, navigate to [Get Started With Logging Messages][DevtoolsConsoleLoggingMessages].</span></span>  <span data-ttu-id="e2be0-120">Para procurar a lista completa `console` de métodos, navegue até a [Referência da API do Console.][DevToolsConsoleAPI]</span><span class="sxs-lookup"><span data-stu-id="e2be0-120">To browse the full list of `console` methods, navigate to the [Console API Reference][DevToolsConsoleAPI].</span></span>  <span data-ttu-id="e2be0-121">A principal diferença entre os métodos é como os dados que estão sendo registrados são exibidos.</span><span class="sxs-lookup"><span data-stu-id="e2be0-121">The main difference between the methods is how the data being logged is displayed.</span></span>  

## <a name="running-javascript"></a><span data-ttu-id="e2be0-122">Executando JavaScript</span><span class="sxs-lookup"><span data-stu-id="e2be0-122">Running JavaScript</span></span>  

<span data-ttu-id="e2be0-123">O **Console** também é [um REPL][WikiREPLoop].</span><span class="sxs-lookup"><span data-stu-id="e2be0-123">The **Console** is also a [REPL][WikiREPLoop].</span></span>  <span data-ttu-id="e2be0-124">Você pode executar JavaScript no **Console para** interagir com a página que está sendo inspecionada.</span><span class="sxs-lookup"><span data-stu-id="e2be0-124">You may run JavaScript in the **Console** to interact with the page being inspected.</span></span>   

:::row:::
   :::column span="":::
      <span data-ttu-id="e2be0-125">Na figura a seguir, **o Console** é mostrado ao lado da homepage DevTools.</span><span class="sxs-lookup"><span data-stu-id="e2be0-125">In the following figure, the **Console** is shown next to the DevTools homepage.</span></span>  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="A ferramenta Console ao lado da página inicial do DevTools" lightbox="../media/devtools-console-empty.msft.png":::
         <span data-ttu-id="e2be0-127">A **ferramenta Console** ao lado da página inicial do DevTools</span><span class="sxs-lookup"><span data-stu-id="e2be0-127">The **Console** tool next to the DevTools homepage</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="e2be0-128">Na figura a seguir, a mesma página é mostrada depois de usar o **Console** para alterar o título superior da página.</span><span class="sxs-lookup"><span data-stu-id="e2be0-128">In the following figure, the same page is shown after using the **Console** to change the top heading of the page.</span></span>
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Use o Console para alterar o título superior da página" lightbox="../media/devtools-console-h1-changed.msft.png":::
         <span data-ttu-id="e2be0-130">Use o **Console** para alterar o título superior da página</span><span class="sxs-lookup"><span data-stu-id="e2be0-130">Use the **Console** to change the top heading of the page</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="e2be0-131">Modificar a página do **Console** é possível porque o **Console** tem acesso total à [janela][MDNWindow] da página.</span><span class="sxs-lookup"><span data-stu-id="e2be0-131">Modifying the page from the **Console** is possible because the **Console** has full access to the [window][MDNWindow] of the page.</span></span>  <span data-ttu-id="e2be0-132">O DevTools tem algumas funções de conveniência que facilitam a inspeção de uma página.</span><span class="sxs-lookup"><span data-stu-id="e2be0-132">DevTools has a few convenience functions that make it easier to inspect a page.</span></span>  <span data-ttu-id="e2be0-133">Por exemplo, suponha que seu JavaScript contenha uma função chamada `hideModal` .</span><span class="sxs-lookup"><span data-stu-id="e2be0-133">For example, suppose that your JavaScript contains a function called `hideModal`.</span></span>  <span data-ttu-id="e2be0-134">A `debug(hideModal)` execução pausa seu código na primeira linha da próxima vez que você o `hideModal` executa.</span><span class="sxs-lookup"><span data-stu-id="e2be0-134">Running `debug(hideModal)` pauses your code on the first line of `hideModal` the next time that you run it.</span></span>  <span data-ttu-id="e2be0-135">Para obter mais informações sobre a lista completa de funções de utilitário, navegue até Referência da [API de Utilitários de Console.][DevtoolsConsoleUtilitiesDebug]</span><span class="sxs-lookup"><span data-stu-id="e2be0-135">For more information about the full list of utility functions, navigate to [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug].</span></span>  

<span data-ttu-id="e2be0-136">Ao executar o JavaScript, você não precisa interagir com a página.</span><span class="sxs-lookup"><span data-stu-id="e2be0-136">When you run JavaScript you do not have to interact with the page.</span></span>  <span data-ttu-id="e2be0-137">Você pode usar o **Console** para experimentar um novo código não relacionado à página.</span><span class="sxs-lookup"><span data-stu-id="e2be0-137">You may use the **Console** to try out new code unrelated to the page.</span></span>  <span data-ttu-id="e2be0-138">Por exemplo, suponha que você acabou de aprender sobre o método JavaScript Array [map()][MDNMap] integrado e deseja experimentar com ele.</span><span class="sxs-lookup"><span data-stu-id="e2be0-138">For example, suppose you just learned about the built-in JavaScript Array [map()][MDNMap] method, and you want to experiment with it.</span></span>  
<span data-ttu-id="e2be0-139">O **Console** é um bom lugar para experimentar a função.</span><span class="sxs-lookup"><span data-stu-id="e2be0-139">The **Console** is a good place to try out the function.</span></span>  

<span data-ttu-id="e2be0-140">Para obter mais experiência prática com a execução de JavaScript no **Console,** navegue até [Começar a executar JavaScript][DevtoolsConsoleRunningJavascript].</span><span class="sxs-lookup"><span data-stu-id="e2be0-140">For more hands-on experience with running JavaScript in the **Console**, navigate to [Get Started With Running JavaScript][DevtoolsConsoleRunningJavascript].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="e2be0-141">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e2be0-141">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleAPI]: ./api.md "Referência da API de console | Microsoft Docs"  
[DevtoolsConsoleLoggingMessages]: ./log.md "Começar a registrar mensagens no console | Microsoft Docs"  
[DevtoolsConsoleRunningJavascript]: ./javascript.md "Começar a executar JavaScript no console | Microsoft Docs"  
[DevtoolsConsoleUtilitiesDebug]: ./utilities.md#debug "depuração - Referência da API de Utilitários de Console | Microsoft Docs"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array.prototype.map() | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Janela | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Loop de leitura-eval-print - Wikipédia"  

> [!NOTE]
> <span data-ttu-id="e2be0-149">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e2be0-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e2be0-150">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="e2be0-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e2be0-152">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e2be0-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
