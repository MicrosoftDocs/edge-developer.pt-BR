---
description: Os principais usos do console do Microsoft Edge DevTools são as mensagens registradas e a execução de JavaScript.
title: Visão geral do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 32272c3f76f715566ced66d11346985dc95dd290
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125262"
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

# <span data-ttu-id="1e237-104">Visão geral do console</span><span class="sxs-lookup"><span data-stu-id="1e237-104">Console Overview</span></span>  

  

<span data-ttu-id="1e237-105">Esta página explica como o console do Microsoft Edge DevTools torna mais fácil o desenvolvimento de páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="1e237-105">This page explains how the Microsoft Edge DevTools Console makes it easier to develop web pages.</span></span>  <span data-ttu-id="1e237-106">O console tem dois usos principais: [Exibir mensagens registradas](#viewing-logged-messages) e [executar JavaScript](#running-javascript).</span><span class="sxs-lookup"><span data-stu-id="1e237-106">The Console has 2 main uses: [viewing logged messages](#viewing-logged-messages) and [running JavaScript](#running-javascript).</span></span>  

## <span data-ttu-id="1e237-107">Exibir mensagens registradas</span><span class="sxs-lookup"><span data-stu-id="1e237-107">Viewing logged messages</span></span>  

<span data-ttu-id="1e237-108">Os desenvolvedores da Web geralmente registram mensagens no console para verificar se o JavaScript está funcionando conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="1e237-108">Web developers often log messages to the Console to make sure that their JavaScript is working as expected.</span></span>  <span data-ttu-id="1e237-109">Para registrar uma mensagem, insira uma expressão como `console.log('Hello, Console!')` em seu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1e237-109">To log a message, you insert an expression like `console.log('Hello, Console!')` into your JavaScript.</span></span>  <span data-ttu-id="1e237-110">Quando o navegador executa o JavaScript e vê uma expressão como essa, ele registra a mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="1e237-110">When the browser runs your JavaScript and sees an expression like that, it logs the message to the Console.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1e237-111">O HTML e JavaScript da página.</span><span class="sxs-lookup"><span data-stu-id="1e237-111">The HTML and JavaScript for the page.</span></span>  
      
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
      <span data-ttu-id="1e237-112">Na figura a seguir, o **console** exibe os resultados de carregar a página e esperar 3 segundos.</span><span class="sxs-lookup"><span data-stu-id="1e237-112">In the following figure, the **Console** displays the results of loading the page and waiting 3 seconds.</span></span>  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="Painel do console" lightbox="../media/console-console-demo.msft.png":::
         <span data-ttu-id="1e237-114">Painel do **console**</span><span class="sxs-lookup"><span data-stu-id="1e237-114">The **Console** panel</span></span>  
      :::image-end:::  
      
      <span data-ttu-id="1e237-115">Tente determinar quais linhas de código fizeram o navegador registrar as mensagens.</span><span class="sxs-lookup"><span data-stu-id="1e237-115">Try to determine which lines of code caused the browser to log the messages.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="1e237-116">Os desenvolvedores da Web registram mensagens pelos seguintes dois motivos gerais.</span><span class="sxs-lookup"><span data-stu-id="1e237-116">Web developers log messages for the following 2 general reasons.</span></span>  

*   <span data-ttu-id="1e237-117">Verificar se o código está em execução na ordem correta.</span><span class="sxs-lookup"><span data-stu-id="1e237-117">Making sure that code is running in the right order.</span></span>  
*   <span data-ttu-id="1e237-118">Inspecionar os valores de variáveis em um determinado momento no tempo.</span><span class="sxs-lookup"><span data-stu-id="1e237-118">Inspecting the values of variables at a certain moment in time.</span></span>  

<span data-ttu-id="1e237-119">Consulte [introdução ao registro de mensagens][DevtoolsConsoleLoggingMessages] para obter experiência prática com o registro em log.</span><span class="sxs-lookup"><span data-stu-id="1e237-119">See [Get Started With Logging Messages][DevtoolsConsoleLoggingMessages] to get hands-on experience with logging.</span></span>  <span data-ttu-id="1e237-120">Consulte a [referência de API do console][DevToolsConsoleAPI] para procurar a lista completa de `console` métodos.</span><span class="sxs-lookup"><span data-stu-id="1e237-120">See the [Console API Reference][DevToolsConsoleAPI] to browse the full list of `console` methods.</span></span>  <span data-ttu-id="1e237-121">A principal diferença entre os métodos é como os dados que estão sendo registrados são exibidos.</span><span class="sxs-lookup"><span data-stu-id="1e237-121">The main difference between the methods is how the data being logged is displayed.</span></span>  

## <span data-ttu-id="1e237-122">Executando JavaScript</span><span class="sxs-lookup"><span data-stu-id="1e237-122">Running JavaScript</span></span>  

<span data-ttu-id="1e237-123">O **console** também é um [repl][WikiREPLoop].</span><span class="sxs-lookup"><span data-stu-id="1e237-123">The **Console** is also a [REPL][WikiREPLoop].</span></span>  <span data-ttu-id="1e237-124">Você pode executar JavaScript no **console** para interagir com a página que está sendo inspecionada.</span><span class="sxs-lookup"><span data-stu-id="1e237-124">You may run JavaScript in the **Console** to interact with the page being inspected.</span></span>   

:::row:::
   :::column span="":::
      <span data-ttu-id="1e237-125">Na figura a seguir, o **console** é mostrado ao lado da home page do devtools.</span><span class="sxs-lookup"><span data-stu-id="1e237-125">In the following figure, the **Console** is shown next to the DevTools homepage.</span></span>  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="Painel do console" lightbox="../media/devtools-console-empty.msft.png":::
         <span data-ttu-id="1e237-127">O painel do **console** ao lado da home page do devtools</span><span class="sxs-lookup"><span data-stu-id="1e237-127">The **Console** panel next to the DevTools homepage</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1e237-128">Na figura a seguir, a mesma página é mostrada após usar o **console** para alterar o título superior da página.</span><span class="sxs-lookup"><span data-stu-id="1e237-128">In the following figure, the same page is shown after using the **Console** to change the top heading of the page.</span></span>
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Painel do console" lightbox="../media/devtools-console-h1-changed.msft.png":::
         <span data-ttu-id="1e237-130">Usar o **console** para alterar o título superior da página</span><span class="sxs-lookup"><span data-stu-id="1e237-130">Use the **Console** to change the top heading of the page</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="1e237-131">A modificação da página no **console** é possível porque o **console** tem acesso completo à [janela][MDNWindow] da página.</span><span class="sxs-lookup"><span data-stu-id="1e237-131">Modifying the page from the **Console** is possible because the **Console** has full access to the [window][MDNWindow] of the page.</span></span>  <span data-ttu-id="1e237-132">O DevTools tem algumas funções de conveniência que facilitam a inspeção de uma página.</span><span class="sxs-lookup"><span data-stu-id="1e237-132">DevTools has a few convenience functions that make it easier to inspect a page.</span></span>  <span data-ttu-id="1e237-133">Por exemplo, suponha que o JavaScript contenha uma função chamada `hideModal` .</span><span class="sxs-lookup"><span data-stu-id="1e237-133">For example, suppose that your JavaScript contains a function called `hideModal`.</span></span>  <span data-ttu-id="1e237-134">Executar `debug(hideModal)` pausa o código na primeira linha da `hideModal` próxima vez que você executá-lo.</span><span class="sxs-lookup"><span data-stu-id="1e237-134">Running `debug(hideModal)` pauses your code on the first line of `hideModal` the next time that you run it.</span></span>  <span data-ttu-id="1e237-135">Para obter mais informações sobre a lista completa de funções de utilitário, navegue até a [referência da API de utilitários do console][DevtoolsConsoleUtilitiesDebug].</span><span class="sxs-lookup"><span data-stu-id="1e237-135">For more information about the full list of utility functions, navigate to [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug].</span></span>  

<span data-ttu-id="1e237-136">Quando você executa JavaScript, você não precisa interagir com a página.</span><span class="sxs-lookup"><span data-stu-id="1e237-136">When you run JavaScript you do not have to interact with the page.</span></span>  <span data-ttu-id="1e237-137">Você pode usar o **console** para experimentar um novo código não relacionado à página.</span><span class="sxs-lookup"><span data-stu-id="1e237-137">You may use the **Console** to try out new code unrelated to the page.</span></span>  <span data-ttu-id="1e237-138">Por exemplo, suponha que você tenha aprendido apenas sobre o método interno de mapas de matrizes JavaScript [()][MDNMap] e queira experimentá-lo.</span><span class="sxs-lookup"><span data-stu-id="1e237-138">For example, suppose you just learned about the built-in JavaScript Array [map()][MDNMap] method, and you want to experiment with it.</span></span>  
<span data-ttu-id="1e237-139">O **console** é um bom lugar para experimentar a função.</span><span class="sxs-lookup"><span data-stu-id="1e237-139">The **Console** is a good place to try out the function.</span></span>  

<span data-ttu-id="1e237-140">Para obter mais experiência prática com a execução de JavaScript no **console**, navegue até [introdução à execução do JavaScript][DevtoolsConsoleRunningJavascript].</span><span class="sxs-lookup"><span data-stu-id="1e237-140">For more hands-on experience with running JavaScript in the **Console**, navigate to [Get Started With Running JavaScript][DevtoolsConsoleRunningJavascript].</span></span>  

## <span data-ttu-id="1e237-141">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1e237-141">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleAPI]: ./api.md "Referência de API de console | Documentos da Microsoft"  
[DevtoolsConsoleLoggingMessages]: ./log.md "Introdução ao registro de mensagens no console | Documentos da Microsoft"  
[DevtoolsConsoleRunningJavascript]: ./javascript.md "Comece a executar o JavaScript no console | Documentos da Microsoft"  
[DevtoolsConsoleUtilitiesDebug]: ./utilities.md#debug "Referência de API de utilitários de console de depuração | Documentos da Microsoft"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array. prototype. Map () | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Janela | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Leitura – eval – loop de impressão-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="1e237-149">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="1e237-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1e237-150">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="1e237-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1e237-152">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1e237-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
