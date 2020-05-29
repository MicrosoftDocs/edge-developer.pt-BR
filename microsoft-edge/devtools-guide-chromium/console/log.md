---
title: Introdução ao registro de mensagens no console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: d3dbec41bc1e53b5e9001551c796e5a495dd331e
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601730"
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





# <span data-ttu-id="85685-103">Introdução ao registro de mensagens no console</span><span class="sxs-lookup"><span data-stu-id="85685-103">Get Started With Logging Messages In The Console</span></span>   



<span data-ttu-id="85685-104">Este tutorial interativo mostra como registrar e filtrar mensagens no console do [Microsoft Edge devtools][MicrosoftEdgeDevTools] .</span><span class="sxs-lookup"><span data-stu-id="85685-104">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

> ##### <span data-ttu-id="85685-105">Figura 1</span><span class="sxs-lookup"><span data-stu-id="85685-105">Figure 1</span></span>  
> <span data-ttu-id="85685-106">Mensagens no console</span><span class="sxs-lookup"><span data-stu-id="85685-106">Messages in the Console</span></span>  
> ![Mensagens no console][ImageLogExample]  

<span data-ttu-id="85685-108">Este tutorial deve ser concluído em ordem.</span><span class="sxs-lookup"><span data-stu-id="85685-108">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="85685-109">Ele pressupõe que você compreenda os conceitos básicos do desenvolvimento na Web, por exemplo, como usar JavaScript para adicionar interatividade a uma página.</span><span class="sxs-lookup"><span data-stu-id="85685-109">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <span data-ttu-id="85685-110">Configurar a demonstração e a DevTools</span><span class="sxs-lookup"><span data-stu-id="85685-110">Set up the demo and DevTools</span></span>   

<span data-ttu-id="85685-111">Este tutorial foi projetado para que você possa abrir a demonstração e experimentar todos os fluxos de trabalho.</span><span class="sxs-lookup"><span data-stu-id="85685-111">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="85685-112">Ao acompanhar fisicamente, é mais provável que você se lembre dos fluxos de trabalho mais tarde.</span><span class="sxs-lookup"><span data-stu-id="85685-112">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="85685-113">Segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e clique em **exemplos de log do console** para abrir em uma nova guia.</span><span class="sxs-lookup"><span data-stu-id="85685-113">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="85685-114">Exemplos de log do console</span><span class="sxs-lookup"><span data-stu-id="85685-114">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!-- > [!TIP]
    > Move the demo to a separate window.  
    > 
    > > ##### old Figure 2  
    > > The tutorial on the left, and the demo on the right  
    > > ![The tutorial on the left, and the demo on the right][ImageLogSetUp1]  -->
    
1.  <span data-ttu-id="85685-115">Focalize a demonstração e, em seguida, pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) para abrir o devtools.</span><span class="sxs-lookup"><span data-stu-id="85685-115">Focus the demo and then press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="85685-116">Por padrão, o DevTools é aberto à direita da demonstração.</span><span class="sxs-lookup"><span data-stu-id="85685-116">By default DevTools opens to the right of the demo.</span></span>  
    
    > ##### <span data-ttu-id="85685-117">Figura 2</span><span class="sxs-lookup"><span data-stu-id="85685-117">Figure 2</span></span>  
    > <span data-ttu-id="85685-118">O DevTools é aberto à direita da demonstração</span><span class="sxs-lookup"><span data-stu-id="85685-118">DevTools opens to the right of the demo</span></span>  
    > <span data-ttu-id="85685-119">! [O DevTools abre à direita da demonstração] [ImageDevToolsRight]</span><span class="sxs-lookup"><span data-stu-id="85685-119">![DevTools opens to the right of the demo][ImageDevToolsRight]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="85685-120">[Encaixe devtools na parte inferior da janela ou desencaixe-a em uma janela separada][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="85685-120">[Dock DevTools to the bottom of the window or undock it into a separate window][DevToolsCustomizePlacement].</span></span>  
    
    > ##### <span data-ttu-id="85685-121">Figura 3</span><span class="sxs-lookup"><span data-stu-id="85685-121">Figure 3</span></span>  
    > <span data-ttu-id="85685-122">DevTools encaixado na parte inferior da demonstração</span><span class="sxs-lookup"><span data-stu-id="85685-122">DevTools docked to the bottom of the demo</span></span>  
    > <span data-ttu-id="85685-123">! [DevTools encaixado na parte inferior da demonstração] [ImageDevToolsBottom]</span><span class="sxs-lookup"><span data-stu-id="85685-123">![DevTools docked to the bottom of the demo][ImageDevToolsBottom]</span></span>  
    
    > ##### <span data-ttu-id="85685-124">Figura 4</span><span class="sxs-lookup"><span data-stu-id="85685-124">Figure 4</span></span>  
    > <span data-ttu-id="85685-125">Navegador em uma janela separada</span><span class="sxs-lookup"><span data-stu-id="85685-125">Browser in a separate window</span></span>  
    > <span data-ttu-id="85685-126">! [Navegador em uma janela separada] [ImageDevToolsSeparateBrowse]</span><span class="sxs-lookup"><span data-stu-id="85685-126">![Browser in a separate window][ImageDevToolsSeparateBrowse]</span></span>  
    
    > ##### <span data-ttu-id="85685-127">Figura 5</span><span class="sxs-lookup"><span data-stu-id="85685-127">Figure 5</span></span>  
    > <span data-ttu-id="85685-128">DevTools desencaixado em uma janela separada</span><span class="sxs-lookup"><span data-stu-id="85685-128">DevTools undocked in a separate window</span></span>  
    > <span data-ttu-id="85685-129">! [DevTools desencaixado em uma janela separada] [ImageDevToolsSeparateDevTools]</span><span class="sxs-lookup"><span data-stu-id="85685-129">![DevTools undocked in a separate window][ImageDevToolsSeparateDevTools]</span></span>  
    
## <span data-ttu-id="85685-130">Exibir mensagens registradas do JavaScript</span><span class="sxs-lookup"><span data-stu-id="85685-130">View messages logged from JavaScript</span></span>   

<span data-ttu-id="85685-131">A maioria das mensagens que você vê no console vem dos desenvolvedores da Web que escreveram o JavaScript da página.</span><span class="sxs-lookup"><span data-stu-id="85685-131">Most messages that you see in the Console come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="85685-132">O objetivo desta seção é apresentar a você os diferentes tipos de mensagem que provavelmente você verá no console e explicar como você pode registrar cada tipo de mensagem a partir de seu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="85685-132">The goal of this section is to introduce you to the different message types that you are likely to see in the Console, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="85685-133">Clique no botão **informações de log** na demonstração.</span><span class="sxs-lookup"><span data-stu-id="85685-133">Click the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="85685-134">é registrado no console.</span><span class="sxs-lookup"><span data-stu-id="85685-134">gets logged to the Console.</span></span>
    
    > ##### <span data-ttu-id="85685-135">Figura 6</span><span class="sxs-lookup"><span data-stu-id="85685-135">Figure 6</span></span>  
    > <span data-ttu-id="85685-136">O console depois de clicar em **informações de log**</span><span class="sxs-lookup"><span data-stu-id="85685-136">The Console after clicking **Log Info**</span></span>  
    > <span data-ttu-id="85685-137">! [O console após clicar em informações do log] [ImageLogInfo]</span><span class="sxs-lookup"><span data-stu-id="85685-137">![The Console after clicking Log Info][ImageLogInfo]</span></span>  
    
1.  <span data-ttu-id="85685-138">Ao lado da `Hello, Console!` mensagem no console, clique em **log. js: 2**.</span><span class="sxs-lookup"><span data-stu-id="85685-138">Next to the `Hello, Console!` message in the Console click **log.js:2**.</span></span>  <span data-ttu-id="85685-139">O painel fontes é aberto e realça a linha de código que fez com que a mensagem seja registrada no console.</span><span class="sxs-lookup"><span data-stu-id="85685-139">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="85685-140">A mensagem foi registrada quando o JavaScript da página foi executado `console.log('Hello, Console!')` .</span><span class="sxs-lookup"><span data-stu-id="85685-140">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    > ##### <span data-ttu-id="85685-141">Figura 7</span><span class="sxs-lookup"><span data-stu-id="85685-141">Figure 7</span></span>  
    > <span data-ttu-id="85685-142">O DevTools abre o painel fontes depois que você clica em **log. js: 2**</span><span class="sxs-lookup"><span data-stu-id="85685-142">DevTools opens the Sources panel after you click **log.js:2**</span></span>  
    > <span data-ttu-id="85685-143">! [DevTools abre o painel fontes depois que você clica em log. js: 2] [ImageSourceLog]</span><span class="sxs-lookup"><span data-stu-id="85685-143">![DevTools opens the Sources panel after you click log.js:2][ImageSourceLog]</span></span>  
    
1.  <span data-ttu-id="85685-144">Navegue de volta para o console usando qualquer um dos fluxos de trabalho a seguir:</span><span class="sxs-lookup"><span data-stu-id="85685-144">Navigate back to the Console using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="85685-145">Clique na guia **console** .</span><span class="sxs-lookup"><span data-stu-id="85685-145">Click the **Console** tab.</span></span>  
    *   <span data-ttu-id="85685-146">Pressione `Control` + `[` \ (Windows \) ou `Command` + `[` \ (MacOS \) até que o painel do console esteja em foco.</span><span class="sxs-lookup"><span data-stu-id="85685-146">Press `Control`+`[` \(Windows\) or `Command`+`[` \(macOS\) until the Console panel is in focus.</span></span>  
    *   <span data-ttu-id="85685-147">[Abra o menu de comando][DevToolsCommandMenu], comece `Console` a digitar, selecione o comando **Mostrar painel do console** e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="85685-147">[Open the Command Menu][DevToolsCommandMenu], start typing `Console`, select the **Show Console Panel** command, and then press `Enter`.</span></span>  
    
1.  <span data-ttu-id="85685-148">Clique no botão **aviso de log** na demonstração.</span><span class="sxs-lookup"><span data-stu-id="85685-148">Click the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="85685-149">é registrado no console.</span><span class="sxs-lookup"><span data-stu-id="85685-149">gets logged to the Console.</span></span>  <span data-ttu-id="85685-150">As mensagens formatadas assim são avisos.</span><span class="sxs-lookup"><span data-stu-id="85685-150">Messages formatted like this are warnings.</span></span>  
    
    > ##### <span data-ttu-id="85685-151">Figura 8</span><span class="sxs-lookup"><span data-stu-id="85685-151">Figure 8</span></span>  
    > <span data-ttu-id="85685-152">O console após clicar em **aviso de log**</span><span class="sxs-lookup"><span data-stu-id="85685-152">The Console after clicking **Log Warning**</span></span>  
    > <span data-ttu-id="85685-153">! [O console após clicar em aviso de log] [ImageConsoleLogWarning]</span><span class="sxs-lookup"><span data-stu-id="85685-153">![The Console after clicking Log Warning][ImageConsoleLogWarning]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="85685-154">Se você quiser ver o código que causou a conexão de uma mensagem, clique em um script \ (como `log.js:12` \) para exibir o código que causou a formatação da mensagem.</span><span class="sxs-lookup"><span data-stu-id="85685-154">If you want to see the code that caused a message to get logged a certain way, click on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="85685-155">Clique no ícone **expandir** ![ expansão ][ImageExpandIcon] na frente da `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="85685-155">Click the **Expand** ![Expand][ImageExpandIcon] icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="85685-156">DevTools mostra o [rastreamento de pilha][WikiStackTrace] que leva para a chamada.</span><span class="sxs-lookup"><span data-stu-id="85685-156">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    > ##### <span data-ttu-id="85685-157">Figura 9</span><span class="sxs-lookup"><span data-stu-id="85685-157">Figure 9</span></span>  
    > <span data-ttu-id="85685-158">Um rastreamento de pilha</span><span class="sxs-lookup"><span data-stu-id="85685-158">A stack trace</span></span>  
    > <span data-ttu-id="85685-159">! [Um rastreamento de pilha] [ImageStackTrace]</span><span class="sxs-lookup"><span data-stu-id="85685-159">![A stack trace][ImageStackTrace]</span></span>  
    
    <span data-ttu-id="85685-160">O rastreamento de pilha informa que uma função nomeada `logWarning` foi chamada, que, por sua vez, chamou uma função nomeada `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="85685-160">The stack trace is telling you that a function named `logWarning` was called, which in turn called a function named `quoteDante`.</span></span>  <span data-ttu-id="85685-161">Em outras palavras, a chamada que aconteceu primeiro está na parte inferior do rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="85685-161">In other words, the call that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="85685-162">Você pode fazer o log de rastreamentos de pilha a qualquer momento chamando `console.trace()` .</span><span class="sxs-lookup"><span data-stu-id="85685-162">You may log stack traces at any time by calling `console.trace()`.</span></span>  

1.  <span data-ttu-id="85685-163">Clique em **log Error**.</span><span class="sxs-lookup"><span data-stu-id="85685-163">Click **Log Error**.</span></span>  <span data-ttu-id="85685-164">A seguinte mensagem de erro é registrada:</span><span class="sxs-lookup"><span data-stu-id="85685-164">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    > ##### <span data-ttu-id="85685-165">Figura 10</span><span class="sxs-lookup"><span data-stu-id="85685-165">Figure 10</span></span>  
    > <span data-ttu-id="85685-166">Uma mensagem de erro</span><span class="sxs-lookup"><span data-stu-id="85685-166">An error message</span></span>  
    > <span data-ttu-id="85685-167">! [Uma mensagem de erro] [ImageLogError]</span><span class="sxs-lookup"><span data-stu-id="85685-167">![An error message][ImageLogError]</span></span>  
    
1.  <span data-ttu-id="85685-168">Clique em **tabela de log**.</span><span class="sxs-lookup"><span data-stu-id="85685-168">Click **Log Table**.</span></span>  <span data-ttu-id="85685-169">Uma tabela sobre artistas famosos é registrada no console.</span><span class="sxs-lookup"><span data-stu-id="85685-169">A table about famous artists gets logged to the Console.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="85685-170">A `birthday` coluna é apenas preenchida para uma linha.</span><span class="sxs-lookup"><span data-stu-id="85685-170">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="85685-171">Verifique o código para descobrir o motivo.</span><span class="sxs-lookup"><span data-stu-id="85685-171">Check the code to figure out why that is.</span></span>
    
    > ##### <span data-ttu-id="85685-172">Figura 11</span><span class="sxs-lookup"><span data-stu-id="85685-172">Figure 11</span></span>  
    > <span data-ttu-id="85685-173">Uma tabela no console</span><span class="sxs-lookup"><span data-stu-id="85685-173">A table in the Console</span></span>  
    > <span data-ttu-id="85685-174">! [Uma tabela no console] [ImageConsoleTable]</span><span class="sxs-lookup"><span data-stu-id="85685-174">![A table in the Console][ImageConsoleTable]</span></span>  
    
1.  <span data-ttu-id="85685-175">Clique em **grupo de log**.</span><span class="sxs-lookup"><span data-stu-id="85685-175">Click **Log Group**.</span></span>  <span data-ttu-id="85685-176">Os nomes das 4 tartarugas famosas são agrupados sob a `Adolescent Irradiated Espionage Tortoises` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="85685-176">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    > ##### <span data-ttu-id="85685-177">Figura 12</span><span class="sxs-lookup"><span data-stu-id="85685-177">Figure 12</span></span>  
    > <span data-ttu-id="85685-178">Um grupo de mensagens no console</span><span class="sxs-lookup"><span data-stu-id="85685-178">A group of messages in the Console</span></span>  
    > <span data-ttu-id="85685-179">! [Um grupo de mensagens no console] [ImageConsoleLogGroup]</span><span class="sxs-lookup"><span data-stu-id="85685-179">![A group of messages in the Console][ImageConsoleLogGroup]</span></span>  
    
1.  <span data-ttu-id="85685-180">Clique em **log personalizado**.</span><span class="sxs-lookup"><span data-stu-id="85685-180">Click **Log Custom**.</span></span>  <span data-ttu-id="85685-181">Uma mensagem com uma borda vermelha e plano de fundo azul é registrada no console.</span><span class="sxs-lookup"><span data-stu-id="85685-181">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    > ##### <span data-ttu-id="85685-182">Figura 13</span><span class="sxs-lookup"><span data-stu-id="85685-182">Figure 13</span></span>  
    > <span data-ttu-id="85685-183">Uma mensagem com formatação personalizada no console</span><span class="sxs-lookup"><span data-stu-id="85685-183">A message with custom formatting in the Console</span></span>  
    > <span data-ttu-id="85685-184">! [Uma mensagem com formatação personalizada no console] [ImageConsoleLogCustomFormatting]</span><span class="sxs-lookup"><span data-stu-id="85685-184">![A message with custom formatting in the Console][ImageConsoleLogCustomFormatting]</span></span>  
    
<span data-ttu-id="85685-185">A idéia principal aqui é que, quando você quiser registrar mensagens no console a partir de seu JavaScript, use um dos `console` métodos.</span><span class="sxs-lookup"><span data-stu-id="85685-185">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="85685-186">Cada método formata mensagens de maneira diferente.</span><span class="sxs-lookup"><span data-stu-id="85685-186">Each method formats messages differently.</span></span>  

<span data-ttu-id="85685-187">Há ainda mais métodos do que o que foi demonstrado nesta seção.</span><span class="sxs-lookup"><span data-stu-id="85685-187">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="85685-188">Este tutorial mostra como explorar o restante dos métodos.</span><span class="sxs-lookup"><span data-stu-id="85685-188">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <span data-ttu-id="85685-189">Exibir mensagens registradas pelo navegador</span><span class="sxs-lookup"><span data-stu-id="85685-189">View messages logged by the browser</span></span>   

<span data-ttu-id="85685-190">O navegador também registra mensagens no console.</span><span class="sxs-lookup"><span data-stu-id="85685-190">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="85685-191">Isso geralmente acontece quando há um problema com a página.</span><span class="sxs-lookup"><span data-stu-id="85685-191">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="85685-192">Clique em **causa 404**.</span><span class="sxs-lookup"><span data-stu-id="85685-192">Click **Cause 404**.</span></span>  <span data-ttu-id="85685-193">O navegador registra um `404` erro de rede porque o JavaScript da página tentou buscar um arquivo que não existe.</span><span class="sxs-lookup"><span data-stu-id="85685-193">The browser logs a `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    > ##### <span data-ttu-id="85685-194">Figura 14</span><span class="sxs-lookup"><span data-stu-id="85685-194">Figure 14</span></span>  
    > <span data-ttu-id="85685-195">Um erro do 404 no console</span><span class="sxs-lookup"><span data-stu-id="85685-195">A 404 error in the Console</span></span>  
    > <span data-ttu-id="85685-196">! [Um erro 404 no console] [ImageConsoleLogError]</span><span class="sxs-lookup"><span data-stu-id="85685-196">![A 404 error in the Console][ImageConsoleLogError]</span></span>  
    
1.  <span data-ttu-id="85685-197">Clique em **causa erro**.</span><span class="sxs-lookup"><span data-stu-id="85685-197">Click **Cause Error**.</span></span>  <span data-ttu-id="85685-198">O navegador registra uma não capturada `TypeError` porque o JavaScript está tentando atualizar um nó DOM que não existe.</span><span class="sxs-lookup"><span data-stu-id="85685-198">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    > ##### <span data-ttu-id="85685-199">Figura 15</span><span class="sxs-lookup"><span data-stu-id="85685-199">Figure 15</span></span>  
    > <span data-ttu-id="85685-200">Um TypeError no console</span><span class="sxs-lookup"><span data-stu-id="85685-200">A TypeError in the Console</span></span>  
    > <span data-ttu-id="85685-201">! [Um TypeError no console] [ImageConsoleLogTypeError]</span><span class="sxs-lookup"><span data-stu-id="85685-201">![A TypeError in the Console][ImageConsoleLogTypeError]</span></span>  
    
1.  <span data-ttu-id="85685-202">Clique na lista suspensa **níveis de log** e habilite a opção **detalhado** se estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="85685-202">Click the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="85685-203">Saiba mais sobre a filtragem na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="85685-203">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="85685-204">Você precisa fazer isso para certificar-se de que a próxima mensagem que você registrar está visível.</span><span class="sxs-lookup"><span data-stu-id="85685-204">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > ##### <span data-ttu-id="85685-205">Figura 16</span><span class="sxs-lookup"><span data-stu-id="85685-205">Figure 16</span></span>  
    > <span data-ttu-id="85685-206">Habilitando o nível de log **detalhado**</span><span class="sxs-lookup"><span data-stu-id="85685-206">Enabling the **Verbose** log level</span></span>  
    > <span data-ttu-id="85685-207">! [Habilitando o nível de log detalhado] [ImageVerboseLogLevel]</span><span class="sxs-lookup"><span data-stu-id="85685-207">![Enabling the Verbose log level][ImageVerboseLogLevel]</span></span>  
    
1.  <span data-ttu-id="85685-208">Clique em **causa violação**.</span><span class="sxs-lookup"><span data-stu-id="85685-208">Click **Cause Violation**.</span></span>  <span data-ttu-id="85685-209">A página deixa de responder por alguns segundos e, em seguida, o navegador registra a mensagem no `[Violation] 'click' handler took 3000ms` console.</span><span class="sxs-lookup"><span data-stu-id="85685-209">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="85685-210">A duração exata pode variar.</span><span class="sxs-lookup"><span data-stu-id="85685-210">The exact duration may vary.</span></span>  
    
    > ##### <span data-ttu-id="85685-211">Figura 17</span><span class="sxs-lookup"><span data-stu-id="85685-211">Figure 17</span></span>  
    > <span data-ttu-id="85685-212">Uma violação no console</span><span class="sxs-lookup"><span data-stu-id="85685-212">A violation in the Console</span></span>  
    > <span data-ttu-id="85685-213">! [Uma violação no console] [ImageConsoleLogViolation]</span><span class="sxs-lookup"><span data-stu-id="85685-213">![A violation in the Console][ImageConsoleLogViolation]</span></span>  
    
## <span data-ttu-id="85685-214">Filtrar mensagens</span><span class="sxs-lookup"><span data-stu-id="85685-214">Filter messages</span></span>   

<span data-ttu-id="85685-215">Em algumas páginas, o console fica inundado com mensagens.</span><span class="sxs-lookup"><span data-stu-id="85685-215">On some pages you see the Console get flooded with messages.</span></span>  <span data-ttu-id="85685-216">O DevTools oferece várias maneiras diferentes de filtrar mensagens que não são relevantes para a tarefa em questão.</span><span class="sxs-lookup"><span data-stu-id="85685-216">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <span data-ttu-id="85685-217">Filtrar por nível de log</span><span class="sxs-lookup"><span data-stu-id="85685-217">Filter by log level</span></span>   

<span data-ttu-id="85685-218">Cada `console` método é atribuído a um nível de gravidade: `Verbose` ,, `Info` `Warning` ou `Error` .</span><span class="sxs-lookup"><span data-stu-id="85685-218">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="85685-219">Por exemplo, `console.log()` é uma `Info` mensagem de nível um, enquanto `console.error()` é uma `Error` mensagem de nível um.</span><span class="sxs-lookup"><span data-stu-id="85685-219">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="85685-220">Clique na lista suspensa **níveis de log** e desabilite os **erros**.</span><span class="sxs-lookup"><span data-stu-id="85685-220">Click the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="85685-221">Um nível fica desabilitado quando não há mais uma marca de opção ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="85685-221">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="85685-222">As `Error` mensagens de nível desaparecerão.</span><span class="sxs-lookup"><span data-stu-id="85685-222">The `Error`-level messages disappear.</span></span>  
    
    > ##### <span data-ttu-id="85685-223">Figura 18</span><span class="sxs-lookup"><span data-stu-id="85685-223">Figure 18</span></span>  
    > <span data-ttu-id="85685-224">Desativando `Error` mensagens de nível no console</span><span class="sxs-lookup"><span data-stu-id="85685-224">Disabling `Error`-level messages in the Console</span></span>  
    > <span data-ttu-id="85685-225">! [Desativando mensagens de nível de erro no console] [ImageConsoleDisablingLogError]</span><span class="sxs-lookup"><span data-stu-id="85685-225">![Disabling Error-level messages in the Console][ImageConsoleDisablingLogError]</span></span>  
    
1.  <span data-ttu-id="85685-226">Clique novamente na lista suspensa **níveis de log** e ative novamente os **erros**.</span><span class="sxs-lookup"><span data-stu-id="85685-226">Click the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="85685-227">As `Error` mensagens de nível reexibida.</span><span class="sxs-lookup"><span data-stu-id="85685-227">The `Error`-level messages reappear.</span></span>  

### <span data-ttu-id="85685-228">Filtrar por texto</span><span class="sxs-lookup"><span data-stu-id="85685-228">Filter by text</span></span>   

<span data-ttu-id="85685-229">Quando quiser exibir apenas as mensagens que incluem uma cadeia de caracteres exata, digite essa cadeia de caracteres na caixa de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="85685-229">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="85685-230">Digite `Dave` na caixa de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="85685-230">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="85685-231">Todas as mensagens que não incluem a cadeia de caracteres `Dave` estão ocultas.</span><span class="sxs-lookup"><span data-stu-id="85685-231">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="85685-232">Você também pode ver o `Adolescent Irradiated Espionage Tortoises` rótulo.</span><span class="sxs-lookup"><span data-stu-id="85685-232">You might also see the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="85685-233">Isso é um bug.</span><span class="sxs-lookup"><span data-stu-id="85685-233">That is a bug.</span></span>  
    
    > ##### <span data-ttu-id="85685-234">Figura 19</span><span class="sxs-lookup"><span data-stu-id="85685-234">Figure 19</span></span>  
    > <span data-ttu-id="85685-235">Filtragem de qualquer mensagem que não inclua</span><span class="sxs-lookup"><span data-stu-id="85685-235">Filtering out any message that does not include</span></span> `Dave`  
    > <span data-ttu-id="85685-236">! [Filtragem de qualquer mensagem que não inclua Dave] [ImageLogTextFiltering]</span><span class="sxs-lookup"><span data-stu-id="85685-236">![Filtering out any message that does not include Dave][ImageLogTextFiltering]</span></span>  
    
1.  <span data-ttu-id="85685-237">Excluir `Dave` na caixa de texto **Filtrar** .</span><span class="sxs-lookup"><span data-stu-id="85685-237">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="85685-238">Todas as mensagens reaparecem.</span><span class="sxs-lookup"><span data-stu-id="85685-238">All the messages reappear.</span></span>  

### <span data-ttu-id="85685-239">Filtrar por expressão regular</span><span class="sxs-lookup"><span data-stu-id="85685-239">Filter by regular expression</span></span>   

<span data-ttu-id="85685-240">Quando você quiser mostrar todas as mensagens que incluem um padrão de texto, em vez de uma cadeia de caracteres específica, use uma [expressão regular][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="85685-240">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="85685-241">Digite `/^[AH]/` na caixa de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="85685-241">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="85685-242">Digite esse padrão no [regexr][|::ref1::|Main] para obter uma explicação do que ele está fazendo.</span><span class="sxs-lookup"><span data-stu-id="85685-242">Type this pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    > ##### <span data-ttu-id="85685-243">Figura 20</span><span class="sxs-lookup"><span data-stu-id="85685-243">Figure 20</span></span>  
    > <span data-ttu-id="85685-244">Filtragem de qualquer mensagem que não corresponda ao padrão</span><span class="sxs-lookup"><span data-stu-id="85685-244">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    > <span data-ttu-id="85685-245">! [Filtrar qualquer mensagem que não corresponda a um padrão] [ImageLogRegExFiltering]</span><span class="sxs-lookup"><span data-stu-id="85685-245">![Filtering out any message that does not match a pattern][ImageLogRegExFiltering]</span></span>  
    
1.  <span data-ttu-id="85685-246">Excluir `/^[AH]/` na caixa de texto **Filtrar** .</span><span class="sxs-lookup"><span data-stu-id="85685-246">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="85685-247">Todas as mensagens ficarão visíveis novamente.</span><span class="sxs-lookup"><span data-stu-id="85685-247">All messages are visible again.</span></span>  

### <span data-ttu-id="85685-248">Filtrar por fonte de mensagem</span><span class="sxs-lookup"><span data-stu-id="85685-248">Filter by message source</span></span>   

<span data-ttu-id="85685-249">Quando quiser exibir apenas as mensagens que vieram de determinada URL, use a **barra lateral**.</span><span class="sxs-lookup"><span data-stu-id="85685-249">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="85685-250">Clique em **Mostrar barra lateral do console** ![ Mostrar barra lateral do console ][ImageShowConsoleSidebarIcon] .</span><span class="sxs-lookup"><span data-stu-id="85685-250">Click **Show Console Sidebar** ![Show Console Sidebar][ImageShowConsoleSidebarIcon].</span></span>  
    
    > ##### <span data-ttu-id="85685-251">Figura 21</span><span class="sxs-lookup"><span data-stu-id="85685-251">Figure 21</span></span>  
    > <span data-ttu-id="85685-252">A barra lateral</span><span class="sxs-lookup"><span data-stu-id="85685-252">The Sidebar</span></span>  
    > <span data-ttu-id="85685-253">! [A barra lateral] [ImageConsoleSidebar]</span><span class="sxs-lookup"><span data-stu-id="85685-253">![The Sidebar][ImageConsoleSidebar]</span></span>  
    
1.  <span data-ttu-id="85685-254">Clique no ícone **expandir** ![ expansão ][ImageExpandIcon] ao lado do número de mensagens.</span><span class="sxs-lookup"><span data-stu-id="85685-254">Click the **Expand** ![Expand][ImageExpandIcon] icon next to the number of messages.</span></span>  <span data-ttu-id="85685-255">Na [Figura 21](#figure-21), o número de mensagens é indicado como **13 mensagens**.</span><span class="sxs-lookup"><span data-stu-id="85685-255">In [Figure 21](#figure-21), the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="85685-256">A **barra lateral** mostra uma lista de URLs que fizeram o registro das mensagens.</span><span class="sxs-lookup"><span data-stu-id="85685-256">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="85685-257">Por exemplo, `log.js` causou 11 mensagens.</span><span class="sxs-lookup"><span data-stu-id="85685-257">For example, `log.js` caused 11 messages.</span></span>  
    
    > ##### <span data-ttu-id="85685-258">Figura 22</span><span class="sxs-lookup"><span data-stu-id="85685-258">Figure 22</span></span>  
    > <span data-ttu-id="85685-259">Exibindo a fonte de mensagens na barra lateral</span><span class="sxs-lookup"><span data-stu-id="85685-259">Viewing the source of messages in the Sidebar</span></span>  
    > <span data-ttu-id="85685-260">! [Exibindo a fonte de mensagens na barra lateral] [ImageConsoleSidebarLogSource]</span><span class="sxs-lookup"><span data-stu-id="85685-260">![Viewing the source of messages in the Sidebar][ImageConsoleSidebarLogSource]</span></span>  
    
### <span data-ttu-id="85685-261">Filtrar por mensagens de usuário</span><span class="sxs-lookup"><span data-stu-id="85685-261">Filter by user messages</span></span>   

<span data-ttu-id="85685-262">Antes, quando você clicou em **registrar informações**, um script chamado para `console.log('Hello, Console!')` registrar a mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="85685-262">Earlier, when you clicked **Log Info**, a script called `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="85685-263">As mensagens registradas do JavaScript como essa são chamadas de **mensagens de usuário**.</span><span class="sxs-lookup"><span data-stu-id="85685-263">Messages logged from JavaScript like this are called **user messages**.</span></span>  <span data-ttu-id="85685-264">Por outro lado, quando você clicou em **causa 404**, o navegador registrou uma `Error` mensagem de nível informando que o recurso solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="85685-264">In contrast, when you clicked **Cause 404**, the browser logged an `Error`-level message stating that the requested resource could not be found.</span></span>  <span data-ttu-id="85685-265">Mensagens como essa são consideradas **mensagens do navegador**.</span><span class="sxs-lookup"><span data-stu-id="85685-265">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="85685-266">Use a **barra lateral** para filtrar mensagens do navegador e mostrar apenas mensagens de usuário.</span><span class="sxs-lookup"><span data-stu-id="85685-266">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="85685-267">Clique em **9 mensagens de usuário**.</span><span class="sxs-lookup"><span data-stu-id="85685-267">Click **9 User Messages**.</span></span>  <span data-ttu-id="85685-268">As mensagens do navegador estão ocultas.</span><span class="sxs-lookup"><span data-stu-id="85685-268">The browser messages are hidden.</span></span>  
    
    > ##### <span data-ttu-id="85685-269">Figura 23</span><span class="sxs-lookup"><span data-stu-id="85685-269">Figure 23</span></span>  
    > <span data-ttu-id="85685-270">Filtrando mensagens do navegador</span><span class="sxs-lookup"><span data-stu-id="85685-270">Filtering out browser messages</span></span>  
    > <span data-ttu-id="85685-271">! [Filtrando mensagens do navegador] [ImageConsoleLogBrowserFiltering]</span><span class="sxs-lookup"><span data-stu-id="85685-271">![Filtering out browser messages][ImageConsoleLogBrowserFiltering]</span></span>  
    
1.  <span data-ttu-id="85685-272">Clique em **13 mensagens** para mostrar todas as mensagens novamente.</span><span class="sxs-lookup"><span data-stu-id="85685-272">Click **13 Messages** to show all messages again.</span></span>  

## <span data-ttu-id="85685-273">Usar o console juntamente com qualquer outro painel</span><span class="sxs-lookup"><span data-stu-id="85685-273">Use the Console alongside any other panel</span></span>   

<span data-ttu-id="85685-274">E se você estiver editando estilos, mas precisar verificar rapidamente o log do console para algo?</span><span class="sxs-lookup"><span data-stu-id="85685-274">What if you are editing styles, but you need to quickly check the Console log for something?</span></span> <span data-ttu-id="85685-275">Use a gaveta.</span><span class="sxs-lookup"><span data-stu-id="85685-275">Use the Drawer.</span></span>  

1.  <span data-ttu-id="85685-276">Clique na guia **elementos** .</span><span class="sxs-lookup"><span data-stu-id="85685-276">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="85685-277">Pressione `Escape` .</span><span class="sxs-lookup"><span data-stu-id="85685-277">Press `Escape`.</span></span>  <span data-ttu-id="85685-278">A guia Console da **gaveta** será aberta.</span><span class="sxs-lookup"><span data-stu-id="85685-278">The Console tab of the **Drawer** opens.</span></span>  <span data-ttu-id="85685-279">Ele tem todos os recursos do painel do console que você estava usando em todo este tutorial.</span><span class="sxs-lookup"><span data-stu-id="85685-279">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    > ##### <span data-ttu-id="85685-280">Figura 24</span><span class="sxs-lookup"><span data-stu-id="85685-280">Figure 24</span></span>  
    > <span data-ttu-id="85685-281">A guia Console na gaveta</span><span class="sxs-lookup"><span data-stu-id="85685-281">The Console tab in the Drawer</span></span>  
    > <span data-ttu-id="85685-282">! [A guia Console na gaveta] [ImageDrawerConsole]</span><span class="sxs-lookup"><span data-stu-id="85685-282">![The Console tab in the Drawer][ImageDrawerConsole]</span></span>  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

 



<!-- image links -->  

[ImageExpandIcon]: /microsoft-edge/devtools-guide-chromium/media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageLogExample]: /microsoft-edge/devtools-guide-chromium/media/console-ars-technica-console-onload.msft.png "Figura 1: mensagens no console"  
<!--[ImageLogSetUp1]: /microsoft-edge/devtools-guide-chromium/media/log-set-up-1.msft.png "old Figure 2: The tutorial on the left, and the demo on the right"  -->  
[ImageDevToolsRight]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-example-devtools-Right-console.msft.png "Figura 2: DevTools abre à direita da demonstração"  
[ImageDevToolsBottom]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-example-devtools-Bottom-console.msft.png "Figura 3: DevTools encaixado na parte inferior da demonstração"  
[ImageDevToolsSeparateBrowse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-example-devtools-separate-console-Browse.msft.png "Figura 4: navegador em uma janela separada"  
[ImageDevToolsSeparateDevTools]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-example-devtools-separate-console-devtools.msft.png "Figura 5: DevTools desencaixado em uma janela separada"  
[ImageLogInfo]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-info.msft.png "Figura 6: o console após clicar em informações do log"  
[ImageSourceLog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-sources-logjs.msft.png "Figura 7: DevTools abre o painel fontes depois que você clica em log. js: 2"  
[ImageConsoleLogWarning]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-Warning.msft.png "Figura 8: o console após clicar em aviso do log"  
[ImageStackTrace]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-Warning-Expanded.msft.png "Figura 9: um rastreamento de pilha"  
[ImageLogError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-Error.msft.png "Figura 10: uma mensagem de erro"  
[ImageConsoleTable]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-Table.msft.png "Figura 11: uma tabela no console"  
[ImageConsoleLogGroup]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-Group.msft.png "Figura 12: um grupo de mensagens no console"  
[ImageConsoleLogCustomFormatting]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-Custom.msft.png "Figura 13: uma mensagem com formatação personalizada no console"  
[ImageConsoleLogError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-cause-404.msft.png "Figura 14: um erro 404 no console"  
[ImageConsoleLogTypeError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-cause-Error.msft.png "Figura 15: uma TypeError no console"  
[ImageVerboseLogLevel]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-cause-error-log-Levels.msft.png "Figura 16: Habilitando o nível de log detalhado"  
[ImageConsoleLogViolation]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-cause-Violation.msft.png "figura 17: uma violação no console"  
[ImageConsoleDisablingLogError]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-cause-Violation-log-Levels.msft.png "Figura 18: Desativando mensagens de nível de erro no console"  
[ImageLogTextFiltering]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-All-Messages-Text-Filter.msft.png "Figura 19: filtrando qualquer mensagem que não inclua Dave"  
[ImageLogRegExFiltering]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-All-Messages-Regex-Filter.msft.png "Figura 20: filtrando qualquer mensagem que não corresponda a um padrão"  
[ImageConsoleSidebar]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Sidebar-All-Messages.msft.png "figura 21: a barra lateral"  
[ImageConsoleSidebarLogSource]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Sidebar-Expanded-All-Messages.msft.png "Figura 22: exibindo a fonte de mensagens na barra lateral"  
[ImageConsoleLogBrowserFiltering]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Sidebar-User-messages.msft.png "Figura 23: filtrando mensagens do navegador"  
[ImageDrawerConsole]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Elements-Drawer-console-Sidebar-All-Messages.msft.png "Figura 24: a guia Console na gaveta"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge \ (Chromium \)"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando do Microsoft Edge DevTools"  
[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Alterar o posicionamento do Microsoft Edge DevTools (desencaixar, encaixar na parte inferior, encaixar à esquerda)"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Referência de API do console"  
[DevToolsConsoleReference]: /microsoft-edge/devtools-guide-chromium/console/reference "Referência do console"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Introdução ao registro de mensagens | Problema"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expressões regulares | MDN"  

[RegExrMain]: https://regexr.com "RegEx"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Rastreamento de pilha-Wikipédia"  


> [!NOTE]
> <span data-ttu-id="85685-316">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="85685-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="85685-317">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/log) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="85685-317">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="85685-319">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="85685-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
