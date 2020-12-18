---
description: Saiba como registrar mensagens no console.
title: Introdução ao registro de mensagens no console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 2f91f1847bf5469e8106edc21553172fc06db9ee
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231108"
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

# <span data-ttu-id="af213-104">Introdução ao registro de mensagens no console</span><span class="sxs-lookup"><span data-stu-id="af213-104">Get Started With Logging Messages In The Console</span></span>  

<span data-ttu-id="af213-105">Este tutorial interativo mostra como registrar e filtrar mensagens no console do [Microsoft Edge devtools][MicrosoftEdgeDevTools] .</span><span class="sxs-lookup"><span data-stu-id="af213-105">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Mensagens no console" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   <span data-ttu-id="af213-107">Mensagens no **console**</span><span class="sxs-lookup"><span data-stu-id="af213-107">Messages in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="af213-108">Este tutorial deve ser concluído em ordem.</span><span class="sxs-lookup"><span data-stu-id="af213-108">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="af213-109">Ele pressupõe que você compreenda os conceitos básicos do desenvolvimento na Web, por exemplo, como usar JavaScript para adicionar interatividade a uma página.</span><span class="sxs-lookup"><span data-stu-id="af213-109">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <span data-ttu-id="af213-110">Configurar a demonstração e a DevTools</span><span class="sxs-lookup"><span data-stu-id="af213-110">Set up the demo and DevTools</span></span>  

<span data-ttu-id="af213-111">Este tutorial foi projetado para que você possa abrir a demonstração e experimentar todos os fluxos de trabalho.</span><span class="sxs-lookup"><span data-stu-id="af213-111">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="af213-112">Ao acompanhar fisicamente, é mais provável que você se lembre dos fluxos de trabalho mais tarde.</span><span class="sxs-lookup"><span data-stu-id="af213-112">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="af213-113">Segure `Control` \ (Windows, Linux \) ou `Command` \ (MacOS \) e escolha **exemplos de log do console** para abrir em uma nova guia.</span><span class="sxs-lookup"><span data-stu-id="af213-113">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="af213-114">Exemplos de log do console</span><span class="sxs-lookup"><span data-stu-id="af213-114">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  <span data-ttu-id="af213-115">Focalize a demonstração e selecione `Control` + `Shift` + `J` \ (Windows, Linux \) ou `Command` + `Option` + `J` \ (MacOS \) para abrir o devtools.</span><span class="sxs-lookup"><span data-stu-id="af213-115">Focus the demo and then select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="af213-116">Por padrão, o DevTools é aberto à direita da demonstração.</span><span class="sxs-lookup"><span data-stu-id="af213-116">By default DevTools opens to the right of the demo.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="O DevTools é aberto à direita da demonstração" lightbox="../media/console-example-devtools-right-console.msft.png":::
             <span data-ttu-id="af213-118">O DevTools é aberto à direita da demonstração</span><span class="sxs-lookup"><span data-stu-id="af213-118">DevTools opens to the right of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="af213-119">[Encaixe devtools na parte inferior da janela][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="af213-119">[Dock DevTools to the bottom of the window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools encaixado na parte inferior da demonstração" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             <span data-ttu-id="af213-121">DevTools encaixado na parte inferior da demonstração</span><span class="sxs-lookup"><span data-stu-id="af213-121">DevTools docked to the bottom of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="af213-122">[Desencaixe o devtools em uma janela separada][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="af213-122">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Navegador em uma janela separada" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             <span data-ttu-id="af213-124">Navegador em uma janela separada</span><span class="sxs-lookup"><span data-stu-id="af213-124">Browser in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="af213-125">[Desencaixe o devtools em uma janela separada][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="af213-125">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools desencaixado em uma janela separada" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             <span data-ttu-id="af213-127">DevTools desencaixado em uma janela separada</span><span class="sxs-lookup"><span data-stu-id="af213-127">DevTools undocked in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="af213-128">Exibir mensagens registradas do JavaScript</span><span class="sxs-lookup"><span data-stu-id="af213-128">View messages logged from JavaScript</span></span>  

<span data-ttu-id="af213-129">A maioria das mensagens que são exibidas no **console** vêm dos desenvolvedores da Web que escreveram o JavaScript da página.</span><span class="sxs-lookup"><span data-stu-id="af213-129">Most messages that are displayed in the **Console** come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="af213-130">O objetivo desta seção é apresentar a você os diferentes tipos de mensagem que você provavelmente vai analisar no **console**e explicar como você pode registrar cada tipo de mensagem por conta própria em seu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="af213-130">The goal of this section is to introduce you to the different message types that you are likely to review in the **Console**, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="af213-131">Escolha o botão **informações de log** na demonstração.</span><span class="sxs-lookup"><span data-stu-id="af213-131">Choose the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="af213-132">é registrado no console.</span><span class="sxs-lookup"><span data-stu-id="af213-132">gets logged to the Console.</span></span>
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="O console depois de escolher informações de log" lightbox="../media/console-log-info.msft.png":::
       <span data-ttu-id="af213-134">O **console** depois de escolher **informações de log**</span><span class="sxs-lookup"><span data-stu-id="af213-134">The **Console** after you choose **Log Info**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="af213-135">Ao lado da `Hello, Console!` mensagem no console, escolha **log.js:2**.</span><span class="sxs-lookup"><span data-stu-id="af213-135">Next to the `Hello, Console!` message in the Console choose **log.js:2**.</span></span>  <span data-ttu-id="af213-136">O painel fontes é aberto e realça a linha de código que fez com que a mensagem seja registrada no console.</span><span class="sxs-lookup"><span data-stu-id="af213-136">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="af213-137">A mensagem foi registrada quando o JavaScript da página foi executado `console.log('Hello, Console!')` .</span><span class="sxs-lookup"><span data-stu-id="af213-137">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="O DevTools abre o painel fontes depois que você escolhe log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       <span data-ttu-id="af213-139">O DevTools abre o painel **fontes** depois que você escolhe</span><span class="sxs-lookup"><span data-stu-id="af213-139">DevTools opens the **Sources** panel after you choose</span></span> `log.js:2`  
    :::image-end:::  
    
1.  <span data-ttu-id="af213-140">Navegue de volta para o **console** usando qualquer um dos fluxos de trabalho a seguir:</span><span class="sxs-lookup"><span data-stu-id="af213-140">Navigate back to the **Console** using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="af213-141">Escolha a guia **console** .</span><span class="sxs-lookup"><span data-stu-id="af213-141">Choose the **Console** tab.</span></span>  
    *   <span data-ttu-id="af213-142">Selecione `Control` + `[` \ (Windows, Linux \) ou `Command` + `[` \ (MacOS \) até que o painel do **console** esteja em foco.</span><span class="sxs-lookup"><span data-stu-id="af213-142">Select `Control`+`[` \(Windows, Linux\) or `Command`+`[` \(macOS\) until the **Console** panel is in focus.</span></span>  
    *   <span data-ttu-id="af213-143">[Abra o menu de comando][DevToolsCommandMenu], digite `Console` , escolha o comando **Mostrar painel do console** e, em seguida, selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="af213-143">[Open the Command Menu][DevToolsCommandMenu], type `Console`, choose the **Show Console Panel** command, and then select `Enter`.</span></span>  
    
1.  <span data-ttu-id="af213-144">Escolha o botão **aviso de log** na demonstração.</span><span class="sxs-lookup"><span data-stu-id="af213-144">Choose the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="af213-145">é registrado no **console**.</span><span class="sxs-lookup"><span data-stu-id="af213-145">gets logged to the **Console**.</span></span>  <span data-ttu-id="af213-146">As mensagens formatadas assim são avisos.</span><span class="sxs-lookup"><span data-stu-id="af213-146">Messages formatted like this are warnings.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="O console depois de escolher aviso de log" lightbox="../media/console-log-warning.msft.png":::
       <span data-ttu-id="af213-148">O **console** depois de escolher **aviso de log**</span><span class="sxs-lookup"><span data-stu-id="af213-148">The **Console** after you choose **Log Warning**</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="af213-149">Se você quiser exibir o código que causou a conexão de uma mensagem, escolha em um script \ (como `log.js:12` \) para exibir o código que causou a formatação da mensagem.</span><span class="sxs-lookup"><span data-stu-id="af213-149">If you want to display the code that caused a message to get logged a certain way, choose on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="af213-150">Escolha o ícone **expandir** \ ( ![ expandir ][ImageExpandIcon] \) na frente de `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="af213-150">Choose the **Expand** \(![Expand][ImageExpandIcon]\) icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="af213-151">DevTools mostra o [rastreamento de pilha][WikiStackTrace] que leva para a chamada.</span><span class="sxs-lookup"><span data-stu-id="af213-151">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Um rastreamento de pilha" lightbox="../media/console-log-warning-expanded.msft.png":::
       <span data-ttu-id="af213-153">Um rastreamento de pilha</span><span class="sxs-lookup"><span data-stu-id="af213-153">A stack trace</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="af213-154">O rastreamento de pilha informa que uma função nomeada `logWarning` é executada, que, por sua vez, executa uma função nomeada `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="af213-154">The stack trace is telling you that a function named `logWarning` is run, which in turn runs a function named `quoteDante`.</span></span>  <span data-ttu-id="af213-155">Em outras palavras, a solicitação que aconteceu primeiro está na parte inferior do rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="af213-155">In other words, the request that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="af213-156">Você pode criar um log de rastreamentos de pilha a qualquer momento executando `console.trace()` .</span><span class="sxs-lookup"><span data-stu-id="af213-156">You may log stack traces at any time by running `console.trace()`.</span></span>  

1.  <span data-ttu-id="af213-157">Escolha um **erro de log**.</span><span class="sxs-lookup"><span data-stu-id="af213-157">Choose **Log Error**.</span></span>  <span data-ttu-id="af213-158">A seguinte mensagem de erro é registrada:</span><span class="sxs-lookup"><span data-stu-id="af213-158">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Uma mensagem de erro" lightbox="../media/console-log-error.msft.png":::
       <span data-ttu-id="af213-160">Uma mensagem de erro</span><span class="sxs-lookup"><span data-stu-id="af213-160">An error message</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="af213-161">Escolha **tabela de log**.</span><span class="sxs-lookup"><span data-stu-id="af213-161">Choose **Log Table**.</span></span>  <span data-ttu-id="af213-162">Uma tabela sobre artistas famosos é registrada no **console**.</span><span class="sxs-lookup"><span data-stu-id="af213-162">A table about famous artists gets logged to the **Console**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="af213-163">A `birthday` coluna é apenas preenchida para uma linha.</span><span class="sxs-lookup"><span data-stu-id="af213-163">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="af213-164">Revise o código para determinar por que se trata.</span><span class="sxs-lookup"><span data-stu-id="af213-164">Review the code to determine why that is.</span></span>
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Uma tabela no console" lightbox="../media/console-log-table.msft.png":::
       <span data-ttu-id="af213-166">Uma tabela no **console**</span><span class="sxs-lookup"><span data-stu-id="af213-166">A table in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="af213-167">Escolha **grupo de log**.</span><span class="sxs-lookup"><span data-stu-id="af213-167">Choose **Log Group**.</span></span>  <span data-ttu-id="af213-168">Os nomes das 4 tartarugas famosas são agrupados sob a `Adolescent Irradiated Espionage Tortoises` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="af213-168">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Um grupo de mensagens no console" lightbox="../media/console-log-group.msft.png":::
       <span data-ttu-id="af213-170">Um grupo de mensagens no **console**</span><span class="sxs-lookup"><span data-stu-id="af213-170">A group of messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="af213-171">Escolha **log personalizado**.</span><span class="sxs-lookup"><span data-stu-id="af213-171">Choose **Log Custom**.</span></span>  <span data-ttu-id="af213-172">Uma mensagem com uma borda vermelha e plano de fundo azul é registrada no console.</span><span class="sxs-lookup"><span data-stu-id="af213-172">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Uma mensagem com formatação personalizada no console" lightbox="../media/console-log-custom.msft.png":::
       <span data-ttu-id="af213-174">Uma mensagem com formatação personalizada no **console**</span><span class="sxs-lookup"><span data-stu-id="af213-174">A message with custom formatting in the **Console**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="af213-175">A idéia principal aqui é que, quando você quiser registrar mensagens no console a partir de seu JavaScript, use um dos `console` métodos.</span><span class="sxs-lookup"><span data-stu-id="af213-175">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="af213-176">Cada método formata mensagens de maneira diferente.</span><span class="sxs-lookup"><span data-stu-id="af213-176">Each method formats messages differently.</span></span>  

<span data-ttu-id="af213-177">Há ainda mais métodos do que o que foi demonstrado nesta seção.</span><span class="sxs-lookup"><span data-stu-id="af213-177">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="af213-178">Este tutorial mostra como explorar o restante dos métodos.</span><span class="sxs-lookup"><span data-stu-id="af213-178">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <span data-ttu-id="af213-179">Exibir mensagens registradas pelo navegador</span><span class="sxs-lookup"><span data-stu-id="af213-179">View messages logged by the browser</span></span>  

<span data-ttu-id="af213-180">O navegador também registra mensagens no console.</span><span class="sxs-lookup"><span data-stu-id="af213-180">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="af213-181">Isso geralmente acontece quando há um problema com a página.</span><span class="sxs-lookup"><span data-stu-id="af213-181">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="af213-182">Escolha **causa 404**.</span><span class="sxs-lookup"><span data-stu-id="af213-182">Choose **Cause 404**.</span></span>  <span data-ttu-id="af213-183">O navegador registra um código de status HTTP do `404` erro de rede porque o JavaScript da página tentou buscar um arquivo que não existe.</span><span class="sxs-lookup"><span data-stu-id="af213-183">The browser logs an HTTP status code of `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Um erro do 404 no console" lightbox="../media/console-cause-404.msft.png":::
       <span data-ttu-id="af213-185">Um `404` erro no **console**</span><span class="sxs-lookup"><span data-stu-id="af213-185">A `404` error in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="af213-186">Escolher a **causa do erro**.</span><span class="sxs-lookup"><span data-stu-id="af213-186">Choose **Cause Error**.</span></span>  <span data-ttu-id="af213-187">O navegador registra uma não capturada `TypeError` porque o JavaScript está tentando atualizar um nó DOM que não existe.</span><span class="sxs-lookup"><span data-stu-id="af213-187">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="Um TypeError no console" lightbox="../media/console-cause-error.msft.png":::
       <span data-ttu-id="af213-189">A `TypeError` no **console**</span><span class="sxs-lookup"><span data-stu-id="af213-189">A `TypeError` in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="af213-190">Escolha a lista suspensa **níveis de log** e ative a opção **detalhado** se estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="af213-190">Choose the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="af213-191">Saiba mais sobre a filtragem na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="af213-191">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="af213-192">Você precisa fazer isso para certificar-se de que a próxima mensagem que você registrar está visível.</span><span class="sxs-lookup"><span data-stu-id="af213-192">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="af213-193">Se o menu suspenso níveis padrão estiver desabilitado, talvez seja necessário fechar a barra lateral do **console** .</span><span class="sxs-lookup"><span data-stu-id="af213-193">If the Default Levels dropdown is disabled, you may need to close the **Console** Sidebar.</span></span>  <span data-ttu-id="af213-194">Filtre por fonte de mensagem abaixo para obter mais informações sobre a barra lateral do **console** .</span><span class="sxs-lookup"><span data-stu-id="af213-194">Filter by Message Source below for more information about the **Console** Sidebar.</span></span>
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Habilitando o nível de log detalhado" lightbox="../media/console-cause-error-log-levels.msft.png":::
       <span data-ttu-id="af213-196">Habilitando o nível de log detalhado</span><span class="sxs-lookup"><span data-stu-id="af213-196">Enabling the Verbose log level</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="af213-197">Escolha **causa violação**.</span><span class="sxs-lookup"><span data-stu-id="af213-197">Choose **Cause Violation**.</span></span>  <span data-ttu-id="af213-198">A página deixa de responder por alguns segundos e, em seguida, o navegador registra a mensagem no `[Violation] 'click' handler took 3000ms` console.</span><span class="sxs-lookup"><span data-stu-id="af213-198">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="af213-199">A duração exata pode variar.</span><span class="sxs-lookup"><span data-stu-id="af213-199">The exact duration may vary.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Uma violação no console" lightbox="../media/console-cause-violation.msft.png":::
       <span data-ttu-id="af213-201">Uma violação no **console**</span><span class="sxs-lookup"><span data-stu-id="af213-201">A violation in the **Console**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="af213-202">Filtrar mensagens</span><span class="sxs-lookup"><span data-stu-id="af213-202">Filter messages</span></span>  

<span data-ttu-id="af213-203">Em algumas páginas da Web que você revisar o **console** são inundados com mensagens.</span><span class="sxs-lookup"><span data-stu-id="af213-203">On some webpages you review the **Console** get flooded with messages.</span></span>  <span data-ttu-id="af213-204">O DevTools oferece várias maneiras diferentes de filtrar mensagens que não são relevantes para a tarefa em questão.</span><span class="sxs-lookup"><span data-stu-id="af213-204">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <span data-ttu-id="af213-205">Filtrar por nível de log</span><span class="sxs-lookup"><span data-stu-id="af213-205">Filter by log level</span></span>  

<span data-ttu-id="af213-206">Cada `console` método é atribuído a um nível de gravidade: `Verbose` ,, `Info` `Warning` ou `Error` .</span><span class="sxs-lookup"><span data-stu-id="af213-206">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="af213-207">Por exemplo, `console.log()` é uma `Info` mensagem de nível um, enquanto `console.error()` é uma `Error` mensagem de nível um.</span><span class="sxs-lookup"><span data-stu-id="af213-207">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="af213-208">Escolha o menu suspenso **níveis de log** e desabilite os **erros**.</span><span class="sxs-lookup"><span data-stu-id="af213-208">Choose the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="af213-209">Um nível fica desabilitado quando não há mais uma marca de opção ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="af213-209">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="af213-210">As `Error` mensagens de nível desaparecerão.</span><span class="sxs-lookup"><span data-stu-id="af213-210">The `Error`-level messages disappear.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Desabilitar mensagens no nível de erro no console" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       <span data-ttu-id="af213-212">Desabilitar mensagens no nível de erro no **console**</span><span class="sxs-lookup"><span data-stu-id="af213-212">Disable Error-level messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="af213-213">Escolha a lista suspensa de **níveis de log** novamente e habilite novamente os **erros**.</span><span class="sxs-lookup"><span data-stu-id="af213-213">Choose the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="af213-214">As `Error` mensagens de nível reexibida.</span><span class="sxs-lookup"><span data-stu-id="af213-214">The `Error`-level messages reappear.</span></span>  

### <span data-ttu-id="af213-215">Filtrar por texto</span><span class="sxs-lookup"><span data-stu-id="af213-215">Filter by text</span></span>  

<span data-ttu-id="af213-216">Quando quiser exibir apenas as mensagens que incluem uma cadeia de caracteres exata, digite essa cadeia de caracteres na caixa de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="af213-216">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="af213-217">Digite `Dave` na caixa de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="af213-217">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="af213-218">Todas as mensagens que não incluem a cadeia de caracteres `Dave` estão ocultas.</span><span class="sxs-lookup"><span data-stu-id="af213-218">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="af213-219">Você também pode revisar o `Adolescent Irradiated Espionage Tortoises` rótulo.</span><span class="sxs-lookup"><span data-stu-id="af213-219">You may also review the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="af213-220">Isso é um bug.</span><span class="sxs-lookup"><span data-stu-id="af213-220">That is a bug.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Filtrar qualquer mensagem que não inclua Dave" lightbox="../media/console-all-messages-text-filter.msft.png":::
       <span data-ttu-id="af213-222">Filtrar qualquer mensagem que não inclua</span><span class="sxs-lookup"><span data-stu-id="af213-222">Filter out any message that does not include</span></span> `Dave`  
    :::image-end:::  
    
1.  <span data-ttu-id="af213-223">Excluir `Dave` na caixa de texto **Filtrar** .</span><span class="sxs-lookup"><span data-stu-id="af213-223">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="af213-224">Todas as mensagens reaparecem.</span><span class="sxs-lookup"><span data-stu-id="af213-224">All the messages reappear.</span></span>  

### <span data-ttu-id="af213-225">Filtrar por expressão regular</span><span class="sxs-lookup"><span data-stu-id="af213-225">Filter by regular expression</span></span>  

<span data-ttu-id="af213-226">Quando você quiser mostrar todas as mensagens que incluem um padrão de texto, em vez de uma cadeia de caracteres específica, use uma [expressão regular][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="af213-226">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="af213-227">Digite `/^[AH]/` na caixa de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="af213-227">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="af213-228">Digite esse padrão no [regexr][|::ref1::|Main] para obter uma explicação do que ele está fazendo.</span><span class="sxs-lookup"><span data-stu-id="af213-228">Type this pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Filtragem de qualquer mensagem que não corresponda a um padrão" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       <span data-ttu-id="af213-230">Filtragem de qualquer mensagem que não corresponda ao padrão</span><span class="sxs-lookup"><span data-stu-id="af213-230">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    :::image-end:::  
    
1.  <span data-ttu-id="af213-231">Excluir `/^[AH]/` na caixa de texto **Filtrar** .</span><span class="sxs-lookup"><span data-stu-id="af213-231">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="af213-232">Todas as mensagens ficarão visíveis novamente.</span><span class="sxs-lookup"><span data-stu-id="af213-232">All messages are visible again.</span></span>  

### <span data-ttu-id="af213-233">Filtrar por fonte de mensagem</span><span class="sxs-lookup"><span data-stu-id="af213-233">Filter by message source</span></span>  

<span data-ttu-id="af213-234">Quando quiser exibir apenas as mensagens que vieram de determinada URL, use a **barra lateral**.</span><span class="sxs-lookup"><span data-stu-id="af213-234">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="af213-235">Escolha **Mostrar barra lateral do console** \ ( ![ Mostrar barra lateral do console ][ImageShowConsoleSidebarIcon] \).</span><span class="sxs-lookup"><span data-stu-id="af213-235">Choose **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\).</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="A barra lateral" lightbox="../media/console-sidebar-all-messages.msft.png":::
       <span data-ttu-id="af213-237">A barra lateral</span><span class="sxs-lookup"><span data-stu-id="af213-237">The Sidebar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="af213-238">Escolha o ícone **expandir** \ ( ![ expandir ][ImageExpandIcon] \) ao lado do número de mensagens.</span><span class="sxs-lookup"><span data-stu-id="af213-238">Choose the **Expand** \(![Expand][ImageExpandIcon]\) icon next to the number of messages.</span></span>  <span data-ttu-id="af213-239">Na figura a seguir, o número de mensagens é indicado como **13 mensagens**.</span><span class="sxs-lookup"><span data-stu-id="af213-239">In the following figure, the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="af213-240">A **barra lateral** mostra uma lista de URLs que fizeram o registro das mensagens.</span><span class="sxs-lookup"><span data-stu-id="af213-240">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="af213-241">Por exemplo, `log.js` causou 11 mensagens.</span><span class="sxs-lookup"><span data-stu-id="af213-241">For example, `log.js` caused 11 messages.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Exibindo a fonte de mensagens na barra lateral" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       <span data-ttu-id="af213-243">Exibindo a fonte de mensagens na barra lateral</span><span class="sxs-lookup"><span data-stu-id="af213-243">Viewing the source of messages in the Sidebar</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="af213-244">Filtrar por mensagens de usuário</span><span class="sxs-lookup"><span data-stu-id="af213-244">Filter by user messages</span></span>  

<span data-ttu-id="af213-245">Antes, quando você escolhe **informações de log**, um script chamado para `console.log('Hello, Console!')` registrar a mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="af213-245">Earlier, when you choose **Log Info**, a script named `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="af213-246">Mensagens registradas do JavaScript, como **as mensagens de usuário**são nomeadas.</span><span class="sxs-lookup"><span data-stu-id="af213-246">Messages logged from JavaScript like this are named **user messages**.</span></span>  <span data-ttu-id="af213-247">Por outro lado, quando você escolhe **causa 404**, o navegador registra uma `Error` mensagem em nível informando que o recurso solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="af213-247">In contrast, when you choose **Cause 404**, the browser logs an `Error`-level message stating that the requested resource could not be found.</span></span>  <span data-ttu-id="af213-248">Mensagens como essa são consideradas **mensagens do navegador**.</span><span class="sxs-lookup"><span data-stu-id="af213-248">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="af213-249">Use a **barra lateral** para filtrar mensagens do navegador e mostrar apenas mensagens de usuário.</span><span class="sxs-lookup"><span data-stu-id="af213-249">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="af213-250">Escolha **nove mensagens de usuário**.</span><span class="sxs-lookup"><span data-stu-id="af213-250">Choose **9 User Messages**.</span></span>  <span data-ttu-id="af213-251">As mensagens do navegador estão ocultas.</span><span class="sxs-lookup"><span data-stu-id="af213-251">The browser messages are hidden.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Filtrando mensagens do navegador" lightbox="../media/console-sidebar-user-messages.msft.png":::
       <span data-ttu-id="af213-253">Filtrando mensagens do navegador</span><span class="sxs-lookup"><span data-stu-id="af213-253">Filtering out browser messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="af213-254">Escolha **13 mensagens** para mostrar todas as mensagens novamente.</span><span class="sxs-lookup"><span data-stu-id="af213-254">Choose **13 Messages** to show all messages again.</span></span>  

## <span data-ttu-id="af213-255">Usar o console juntamente com qualquer outro painel</span><span class="sxs-lookup"><span data-stu-id="af213-255">Use the Console alongside any other panel</span></span>  

<span data-ttu-id="af213-256">E se você estiver editando estilos, mas precisar verificar rapidamente o log do console para algo?</span><span class="sxs-lookup"><span data-stu-id="af213-256">What if you are editing styles, but you need to quickly check the Console log for something?</span></span>  <span data-ttu-id="af213-257">Use a gaveta.</span><span class="sxs-lookup"><span data-stu-id="af213-257">Use the Drawer.</span></span>  

1.  <span data-ttu-id="af213-258">Escolha a guia **elementos** .</span><span class="sxs-lookup"><span data-stu-id="af213-258">Choose the **Elements** tab.</span></span>  
1.  <span data-ttu-id="af213-259">Selecione `Escape` .</span><span class="sxs-lookup"><span data-stu-id="af213-259">Select `Escape`.</span></span>  <span data-ttu-id="af213-260">A guia **console** da **gaveta** será aberta.</span><span class="sxs-lookup"><span data-stu-id="af213-260">The **Console** tab of the **Drawer** opens.</span></span>  <span data-ttu-id="af213-261">Ele tem todos os recursos do painel do console que você estava usando em todo este tutorial.</span><span class="sxs-lookup"><span data-stu-id="af213-261">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="A guia Console na gaveta" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         <span data-ttu-id="af213-263">A guia **console** na **gaveta**</span><span class="sxs-lookup"><span data-stu-id="af213-263">The **Console** tab in the **Drawer**</span></span>  
    :::image-end:::  
    
<!--## Next steps  -->

<!--
*   Navigate to [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   Navigate to [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   Navigate to [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

## <span data-ttu-id="af213-264">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="af213-264">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge \ (Chromium \) | Documentos da Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Alterar o posicionamento do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsConsoleApi]: ./api.md "Referência de API de console | Documentos da Microsoft"  
[DevToolsConsoleReference]: ./reference.md "Referência do console | Documentos da Microsoft"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Introdução ao registro de mensagens | Problema"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expressões regulares | MDN"  

[RegExrMain]: https://regexr.com "RegEx"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Rastreamento de pilha-Wikipédia"  
> [!NOTE]
> <span data-ttu-id="af213-274">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="af213-274">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="af213-275">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/log) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="af213-275">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="af213-277">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="af213-277">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
