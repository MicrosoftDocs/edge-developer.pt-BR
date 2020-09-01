---
title: Introdução ao registro de mensagens no console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c2cf868e6daaf9dd45c7acc90a71c2154261b9c3
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982590"
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





# <span data-ttu-id="10e28-103">Introdução ao registro de mensagens no console</span><span class="sxs-lookup"><span data-stu-id="10e28-103">Get Started With Logging Messages In The Console</span></span>   



<span data-ttu-id="10e28-104">Este tutorial interativo mostra como registrar e filtrar mensagens no console do [Microsoft Edge devtools][MicrosoftEdgeDevTools] .</span><span class="sxs-lookup"><span data-stu-id="10e28-104">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Mensagens no console" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   <span data-ttu-id="10e28-106">Mensagens no **console**</span><span class="sxs-lookup"><span data-stu-id="10e28-106">Messages in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="10e28-107">Este tutorial deve ser concluído em ordem.</span><span class="sxs-lookup"><span data-stu-id="10e28-107">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="10e28-108">Ele pressupõe que você compreenda os conceitos básicos do desenvolvimento na Web, por exemplo, como usar JavaScript para adicionar interatividade a uma página.</span><span class="sxs-lookup"><span data-stu-id="10e28-108">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <span data-ttu-id="10e28-109">Configurar a demonstração e a DevTools</span><span class="sxs-lookup"><span data-stu-id="10e28-109">Set up the demo and DevTools</span></span>   

<span data-ttu-id="10e28-110">Este tutorial foi projetado para que você possa abrir a demonstração e experimentar todos os fluxos de trabalho.</span><span class="sxs-lookup"><span data-stu-id="10e28-110">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="10e28-111">Ao acompanhar fisicamente, é mais provável que você se lembre dos fluxos de trabalho mais tarde.</span><span class="sxs-lookup"><span data-stu-id="10e28-111">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="10e28-112">Segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e clique em **exemplos de log do console** para abrir em uma nova guia.</span><span class="sxs-lookup"><span data-stu-id="10e28-112">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="10e28-113">Exemplos de log do console</span><span class="sxs-lookup"><span data-stu-id="10e28-113">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  <span data-ttu-id="10e28-114">Focalize a demonstração e, em seguida, pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) para abrir o devtools.</span><span class="sxs-lookup"><span data-stu-id="10e28-114">Focus the demo and then press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="10e28-115">Por padrão, o DevTools é aberto à direita da demonstração.</span><span class="sxs-lookup"><span data-stu-id="10e28-115">By default DevTools opens to the right of the demo.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="O DevTools é aberto à direita da demonstração" lightbox="../media/console-example-devtools-right-console.msft.png":::
             <span data-ttu-id="10e28-117">O DevTools é aberto à direita da demonstração</span><span class="sxs-lookup"><span data-stu-id="10e28-117">DevTools opens to the right of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="10e28-118">[Encaixe devtools na parte inferior da janela][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="10e28-118">[Dock DevTools to the bottom of the window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools encaixado na parte inferior da demonstração" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             <span data-ttu-id="10e28-120">DevTools encaixado na parte inferior da demonstração</span><span class="sxs-lookup"><span data-stu-id="10e28-120">DevTools docked to the bottom of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="10e28-121">[Desencaixe o devtools em uma janela separada][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="10e28-121">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Navegador em uma janela separada" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             <span data-ttu-id="10e28-123">Navegador em uma janela separada</span><span class="sxs-lookup"><span data-stu-id="10e28-123">Browser in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="10e28-124">[Desencaixe o devtools em uma janela separada][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="10e28-124">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools desencaixado em uma janela separada" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             <span data-ttu-id="10e28-126">DevTools desencaixado em uma janela separada</span><span class="sxs-lookup"><span data-stu-id="10e28-126">DevTools undocked in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="10e28-127">Exibir mensagens registradas do JavaScript</span><span class="sxs-lookup"><span data-stu-id="10e28-127">View messages logged from JavaScript</span></span>   

<span data-ttu-id="10e28-128">A maioria das mensagens que você vê no console vem dos desenvolvedores da Web que escreveram o JavaScript da página.</span><span class="sxs-lookup"><span data-stu-id="10e28-128">Most messages that you see in the Console come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="10e28-129">O objetivo desta seção é apresentar a você os diferentes tipos de mensagem que provavelmente você verá no console e explicar como você pode registrar cada tipo de mensagem a partir de seu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="10e28-129">The goal of this section is to introduce you to the different message types that you are likely to see in the Console, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="10e28-130">Clique no botão **informações de log** na demonstração.</span><span class="sxs-lookup"><span data-stu-id="10e28-130">Click the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="10e28-131">é registrado no console.</span><span class="sxs-lookup"><span data-stu-id="10e28-131">gets logged to the Console.</span></span>
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="O console depois de clicar em informações de log" lightbox="../media/console-log-info.msft.png":::
       <span data-ttu-id="10e28-133">O **console** depois de clicar em **informações de log**</span><span class="sxs-lookup"><span data-stu-id="10e28-133">The **Console** after clicking **Log Info**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="10e28-134">Ao lado da `Hello, Console!` mensagem no console, clique em **log.js:2**.</span><span class="sxs-lookup"><span data-stu-id="10e28-134">Next to the `Hello, Console!` message in the Console click **log.js:2**.</span></span>  <span data-ttu-id="10e28-135">O painel fontes é aberto e realça a linha de código que fez com que a mensagem seja registrada no console.</span><span class="sxs-lookup"><span data-stu-id="10e28-135">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="10e28-136">A mensagem foi registrada quando o JavaScript da página foi executado `console.log('Hello, Console!')` .</span><span class="sxs-lookup"><span data-stu-id="10e28-136">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="O DevTools abre o painel fontes depois que você clica em log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       <span data-ttu-id="10e28-138">O DevTools abre o painel **fontes** depois que você clica em</span><span class="sxs-lookup"><span data-stu-id="10e28-138">DevTools opens the **Sources** panel after you click</span></span> `log.js:2`  
    :::image-end:::  
    
1.  <span data-ttu-id="10e28-139">Navegue de volta para o **console** usando qualquer um dos fluxos de trabalho a seguir:</span><span class="sxs-lookup"><span data-stu-id="10e28-139">Navigate back to the **Console** using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="10e28-140">Clique na guia **console** .</span><span class="sxs-lookup"><span data-stu-id="10e28-140">Click the **Console** tab.</span></span>  
    *   <span data-ttu-id="10e28-141">Pressione `Control` + `[` \ (Windows \) ou `Command` + `[` \ (MacOS \) até que o painel do console esteja em foco.</span><span class="sxs-lookup"><span data-stu-id="10e28-141">Press `Control`+`[` \(Windows\) or `Command`+`[` \(macOS\) until the Console panel is in focus.</span></span>  
    *   <span data-ttu-id="10e28-142">[Abra o menu de comando][DevToolsCommandMenu], comece `Console` a digitar, selecione o comando **Mostrar painel do console** e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="10e28-142">[Open the Command Menu][DevToolsCommandMenu], start typing `Console`, select the **Show Console Panel** command, and then press `Enter`.</span></span>  
    
1.  <span data-ttu-id="10e28-143">Clique no botão **aviso de log** na demonstração.</span><span class="sxs-lookup"><span data-stu-id="10e28-143">Click the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="10e28-144">é registrado no console.</span><span class="sxs-lookup"><span data-stu-id="10e28-144">gets logged to the Console.</span></span>  <span data-ttu-id="10e28-145">As mensagens formatadas assim são avisos.</span><span class="sxs-lookup"><span data-stu-id="10e28-145">Messages formatted like this are warnings.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="O console depois de clicar em registrar aviso" lightbox="../media/console-log-warning.msft.png":::
       <span data-ttu-id="10e28-147">O **console** depois de clicar em **registrar aviso**</span><span class="sxs-lookup"><span data-stu-id="10e28-147">The **Console** after you click **Log Warning**</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="10e28-148">Se você quiser ver o código que causou a conexão de uma mensagem, clique em um script \ (como `log.js:12` \) para exibir o código que causou a formatação da mensagem.</span><span class="sxs-lookup"><span data-stu-id="10e28-148">If you want to see the code that caused a message to get logged a certain way, click on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="10e28-149">Clique no ícone **expandir** \ ( ![ expandir ][ImageExpandIcon] \) em frente a `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="10e28-149">Click the **Expand** \(![Expand][ImageExpandIcon]\) icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="10e28-150">DevTools mostra o [rastreamento de pilha][WikiStackTrace] que leva para a chamada.</span><span class="sxs-lookup"><span data-stu-id="10e28-150">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Um rastreamento de pilha" lightbox="../media/console-log-warning-expanded.msft.png":::
       <span data-ttu-id="10e28-152">Um rastreamento de pilha</span><span class="sxs-lookup"><span data-stu-id="10e28-152">A stack trace</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="10e28-153">O rastreamento de pilha informa que uma função nomeada `logWarning` foi chamada, que, por sua vez, chamou uma função nomeada `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="10e28-153">The stack trace is telling you that a function named `logWarning` was called, which in turn called a function named `quoteDante`.</span></span>  <span data-ttu-id="10e28-154">Em outras palavras, a chamada que aconteceu primeiro está na parte inferior do rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="10e28-154">In other words, the call that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="10e28-155">Você pode fazer o log de rastreamentos de pilha a qualquer momento chamando `console.trace()` .</span><span class="sxs-lookup"><span data-stu-id="10e28-155">You may log stack traces at any time by calling `console.trace()`.</span></span>  

1.  <span data-ttu-id="10e28-156">Clique em **log Error**.</span><span class="sxs-lookup"><span data-stu-id="10e28-156">Click **Log Error**.</span></span>  <span data-ttu-id="10e28-157">A seguinte mensagem de erro é registrada:</span><span class="sxs-lookup"><span data-stu-id="10e28-157">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Uma mensagem de erro" lightbox="../media/console-log-error.msft.png":::
       <span data-ttu-id="10e28-159">Uma mensagem de erro</span><span class="sxs-lookup"><span data-stu-id="10e28-159">An error message</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="10e28-160">Clique em **tabela de log**.</span><span class="sxs-lookup"><span data-stu-id="10e28-160">Click **Log Table**.</span></span>  <span data-ttu-id="10e28-161">Uma tabela sobre artistas famosos é registrada no console.</span><span class="sxs-lookup"><span data-stu-id="10e28-161">A table about famous artists gets logged to the Console.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="10e28-162">A `birthday` coluna é apenas preenchida para uma linha.</span><span class="sxs-lookup"><span data-stu-id="10e28-162">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="10e28-163">Revise o código para determinar por que se trata.</span><span class="sxs-lookup"><span data-stu-id="10e28-163">Review the code to determine why that is.</span></span>
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Uma tabela no console" lightbox="../media/console-log-table.msft.png":::
       <span data-ttu-id="10e28-165">Uma tabela no **console**</span><span class="sxs-lookup"><span data-stu-id="10e28-165">A table in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="10e28-166">Clique em **grupo de log**.</span><span class="sxs-lookup"><span data-stu-id="10e28-166">Click **Log Group**.</span></span>  <span data-ttu-id="10e28-167">Os nomes das 4 tartarugas famosas são agrupados sob a `Adolescent Irradiated Espionage Tortoises` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="10e28-167">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Um grupo de mensagens no console" lightbox="../media/console-log-group.msft.png":::
       <span data-ttu-id="10e28-169">Um grupo de mensagens no **console**</span><span class="sxs-lookup"><span data-stu-id="10e28-169">A group of messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="10e28-170">Clique em **log personalizado**.</span><span class="sxs-lookup"><span data-stu-id="10e28-170">Click **Log Custom**.</span></span>  <span data-ttu-id="10e28-171">Uma mensagem com uma borda vermelha e plano de fundo azul é registrada no console.</span><span class="sxs-lookup"><span data-stu-id="10e28-171">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Uma mensagem com formatação personalizada no console" lightbox="../media/console-log-custom.msft.png":::
       <span data-ttu-id="10e28-173">Uma mensagem com formatação personalizada no **console**</span><span class="sxs-lookup"><span data-stu-id="10e28-173">A message with custom formatting in the **Console**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="10e28-174">A idéia principal aqui é que, quando você quiser registrar mensagens no console a partir de seu JavaScript, use um dos `console` métodos.</span><span class="sxs-lookup"><span data-stu-id="10e28-174">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="10e28-175">Cada método formata mensagens de maneira diferente.</span><span class="sxs-lookup"><span data-stu-id="10e28-175">Each method formats messages differently.</span></span>  

<span data-ttu-id="10e28-176">Há ainda mais métodos do que o que foi demonstrado nesta seção.</span><span class="sxs-lookup"><span data-stu-id="10e28-176">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="10e28-177">Este tutorial mostra como explorar o restante dos métodos.</span><span class="sxs-lookup"><span data-stu-id="10e28-177">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <span data-ttu-id="10e28-178">Exibir mensagens registradas pelo navegador</span><span class="sxs-lookup"><span data-stu-id="10e28-178">View messages logged by the browser</span></span>   

<span data-ttu-id="10e28-179">O navegador também registra mensagens no console.</span><span class="sxs-lookup"><span data-stu-id="10e28-179">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="10e28-180">Isso geralmente acontece quando há um problema com a página.</span><span class="sxs-lookup"><span data-stu-id="10e28-180">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="10e28-181">Clique em **causa 404**.</span><span class="sxs-lookup"><span data-stu-id="10e28-181">Click **Cause 404**.</span></span>  <span data-ttu-id="10e28-182">O navegador registra um código de status HTTP do `404` erro de rede porque o JavaScript da página tentou buscar um arquivo que não existe.</span><span class="sxs-lookup"><span data-stu-id="10e28-182">The browser logs an HTTP status code of `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Um erro do 404 no console" lightbox="../media/console-cause-404.msft.png":::
       <span data-ttu-id="10e28-184">Um `404` erro no **console**</span><span class="sxs-lookup"><span data-stu-id="10e28-184">A `404` error in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="10e28-185">Clique em **causa erro**.</span><span class="sxs-lookup"><span data-stu-id="10e28-185">Click **Cause Error**.</span></span>  <span data-ttu-id="10e28-186">O navegador registra uma não capturada `TypeError` porque o JavaScript está tentando atualizar um nó DOM que não existe.</span><span class="sxs-lookup"><span data-stu-id="10e28-186">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="Um TypeError no console" lightbox="../media/console-cause-error.msft.png":::
       <span data-ttu-id="10e28-188">A `TypeError` no **console**</span><span class="sxs-lookup"><span data-stu-id="10e28-188">A `TypeError` in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="10e28-189">Clique na lista suspensa **níveis de log** e habilite a opção **detalhado** se estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="10e28-189">Click the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="10e28-190">Saiba mais sobre a filtragem na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="10e28-190">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="10e28-191">Você precisa fazer isso para certificar-se de que a próxima mensagem que você registrar está visível.</span><span class="sxs-lookup"><span data-stu-id="10e28-191">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="10e28-192">Se o menu suspenso níveis padrão estiver desabilitado, talvez seja necessário fechar a barra lateral do **console** .</span><span class="sxs-lookup"><span data-stu-id="10e28-192">If the Default Levels dropdown is disabled, you may need to close the **Console** Sidebar.</span></span>  <span data-ttu-id="10e28-193">Filtre por fonte de mensagem abaixo para obter mais informações sobre a barra lateral do **console** .</span><span class="sxs-lookup"><span data-stu-id="10e28-193">Filter by Message Source below for more information about the **Console** Sidebar.</span></span>
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Habilitando o nível de log detalhado" lightbox="../media/console-cause-error-log-levels.msft.png":::
       <span data-ttu-id="10e28-195">Habilitando o nível de log detalhado</span><span class="sxs-lookup"><span data-stu-id="10e28-195">Enabling the Verbose log level</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="10e28-196">Clique em **causa violação**.</span><span class="sxs-lookup"><span data-stu-id="10e28-196">Click **Cause Violation**.</span></span>  <span data-ttu-id="10e28-197">A página deixa de responder por alguns segundos e, em seguida, o navegador registra a mensagem no `[Violation] 'click' handler took 3000ms` console.</span><span class="sxs-lookup"><span data-stu-id="10e28-197">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="10e28-198">A duração exata pode variar.</span><span class="sxs-lookup"><span data-stu-id="10e28-198">The exact duration may vary.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Uma violação no console" lightbox="../media/console-cause-violation.msft.png":::
       <span data-ttu-id="10e28-200">Uma violação no **console**</span><span class="sxs-lookup"><span data-stu-id="10e28-200">A violation in the **Console**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="10e28-201">Filtrar mensagens</span><span class="sxs-lookup"><span data-stu-id="10e28-201">Filter messages</span></span>   

<span data-ttu-id="10e28-202">Em algumas páginas, o console fica inundado com mensagens.</span><span class="sxs-lookup"><span data-stu-id="10e28-202">On some pages you see the Console get flooded with messages.</span></span>  <span data-ttu-id="10e28-203">O DevTools oferece várias maneiras diferentes de filtrar mensagens que não são relevantes para a tarefa em questão.</span><span class="sxs-lookup"><span data-stu-id="10e28-203">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <span data-ttu-id="10e28-204">Filtrar por nível de log</span><span class="sxs-lookup"><span data-stu-id="10e28-204">Filter by log level</span></span>   

<span data-ttu-id="10e28-205">Cada `console` método é atribuído a um nível de gravidade: `Verbose` ,, `Info` `Warning` ou `Error` .</span><span class="sxs-lookup"><span data-stu-id="10e28-205">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="10e28-206">Por exemplo, `console.log()` é uma `Info` mensagem de nível um, enquanto `console.error()` é uma `Error` mensagem de nível um.</span><span class="sxs-lookup"><span data-stu-id="10e28-206">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="10e28-207">Clique na lista suspensa **níveis de log** e desabilite os **erros**.</span><span class="sxs-lookup"><span data-stu-id="10e28-207">Click the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="10e28-208">Um nível fica desabilitado quando não há mais uma marca de opção ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="10e28-208">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="10e28-209">As `Error` mensagens de nível desaparecerão.</span><span class="sxs-lookup"><span data-stu-id="10e28-209">The `Error`-level messages disappear.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Desativando mensagens do nível de erro no console" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       <span data-ttu-id="10e28-211">Desativando mensagens do nível de erro no **console**</span><span class="sxs-lookup"><span data-stu-id="10e28-211">Disabling Error-level messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="10e28-212">Clique novamente na lista suspensa **níveis de log** e ative novamente os **erros**.</span><span class="sxs-lookup"><span data-stu-id="10e28-212">Click the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="10e28-213">As `Error` mensagens de nível reexibida.</span><span class="sxs-lookup"><span data-stu-id="10e28-213">The `Error`-level messages reappear.</span></span>  

### <span data-ttu-id="10e28-214">Filtrar por texto</span><span class="sxs-lookup"><span data-stu-id="10e28-214">Filter by text</span></span>   

<span data-ttu-id="10e28-215">Quando quiser exibir apenas as mensagens que incluem uma cadeia de caracteres exata, digite essa cadeia de caracteres na caixa de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="10e28-215">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="10e28-216">Digite `Dave` na caixa de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="10e28-216">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="10e28-217">Todas as mensagens que não incluem a cadeia de caracteres `Dave` estão ocultas.</span><span class="sxs-lookup"><span data-stu-id="10e28-217">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="10e28-218">Você também pode ver o `Adolescent Irradiated Espionage Tortoises` rótulo.</span><span class="sxs-lookup"><span data-stu-id="10e28-218">You might also see the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="10e28-219">Isso é um bug.</span><span class="sxs-lookup"><span data-stu-id="10e28-219">That is a bug.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Filtragem de qualquer mensagem que não inclua Dave" lightbox="../media/console-all-messages-text-filter.msft.png":::
       <span data-ttu-id="10e28-221">Filtragem de qualquer mensagem que não inclua</span><span class="sxs-lookup"><span data-stu-id="10e28-221">Filtering out any message that does not include</span></span> `Dave`  
    :::image-end:::  
    
1.  <span data-ttu-id="10e28-222">Excluir `Dave` na caixa de texto **Filtrar** .</span><span class="sxs-lookup"><span data-stu-id="10e28-222">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="10e28-223">Todas as mensagens reaparecem.</span><span class="sxs-lookup"><span data-stu-id="10e28-223">All the messages reappear.</span></span>  

### <span data-ttu-id="10e28-224">Filtrar por expressão regular</span><span class="sxs-lookup"><span data-stu-id="10e28-224">Filter by regular expression</span></span>   

<span data-ttu-id="10e28-225">Quando você quiser mostrar todas as mensagens que incluem um padrão de texto, em vez de uma cadeia de caracteres específica, use uma [expressão regular][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="10e28-225">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="10e28-226">Digite `/^[AH]/` na caixa de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="10e28-226">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="10e28-227">Digite esse padrão no [regexr][|::ref1::|Main] para obter uma explicação do que ele está fazendo.</span><span class="sxs-lookup"><span data-stu-id="10e28-227">Type this pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Filtragem de qualquer mensagem que não corresponda a um padrão" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       <span data-ttu-id="10e28-229">Filtragem de qualquer mensagem que não corresponda ao padrão</span><span class="sxs-lookup"><span data-stu-id="10e28-229">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    :::image-end:::  
    
1.  <span data-ttu-id="10e28-230">Excluir `/^[AH]/` na caixa de texto **Filtrar** .</span><span class="sxs-lookup"><span data-stu-id="10e28-230">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="10e28-231">Todas as mensagens ficarão visíveis novamente.</span><span class="sxs-lookup"><span data-stu-id="10e28-231">All messages are visible again.</span></span>  

### <span data-ttu-id="10e28-232">Filtrar por fonte de mensagem</span><span class="sxs-lookup"><span data-stu-id="10e28-232">Filter by message source</span></span>   

<span data-ttu-id="10e28-233">Quando quiser exibir apenas as mensagens que vieram de determinada URL, use a **barra lateral**.</span><span class="sxs-lookup"><span data-stu-id="10e28-233">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="10e28-234">Clique em **Mostrar barra lateral do console** \ ( ![ Mostrar barra lateral do console ][ImageShowConsoleSidebarIcon] \).</span><span class="sxs-lookup"><span data-stu-id="10e28-234">Click **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\).</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="A barra lateral" lightbox="../media/console-sidebar-all-messages.msft.png":::
       <span data-ttu-id="10e28-236">A barra lateral</span><span class="sxs-lookup"><span data-stu-id="10e28-236">The Sidebar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="10e28-237">Clique no ícone **expandir** \ ( ![ expandir ][ImageExpandIcon] \) ao lado do número de mensagens.</span><span class="sxs-lookup"><span data-stu-id="10e28-237">Click the **Expand** \(![Expand][ImageExpandIcon]\) icon next to the number of messages.</span></span>  <span data-ttu-id="10e28-238">Na figura a seguir, o número de mensagens é indicado como **13 mensagens**.</span><span class="sxs-lookup"><span data-stu-id="10e28-238">In the following figure, the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="10e28-239">A **barra lateral** mostra uma lista de URLs que fizeram o registro das mensagens.</span><span class="sxs-lookup"><span data-stu-id="10e28-239">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="10e28-240">Por exemplo, `log.js` causou 11 mensagens.</span><span class="sxs-lookup"><span data-stu-id="10e28-240">For example, `log.js` caused 11 messages.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Exibindo a fonte de mensagens na barra lateral" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       <span data-ttu-id="10e28-242">Exibindo a fonte de mensagens na barra lateral</span><span class="sxs-lookup"><span data-stu-id="10e28-242">Viewing the source of messages in the Sidebar</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="10e28-243">Filtrar por mensagens de usuário</span><span class="sxs-lookup"><span data-stu-id="10e28-243">Filter by user messages</span></span>   

<span data-ttu-id="10e28-244">Antes, quando você clicou em **registrar informações**, um script chamado para `console.log('Hello, Console!')` registrar a mensagem no console.</span><span class="sxs-lookup"><span data-stu-id="10e28-244">Earlier, when you clicked **Log Info**, a script called `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="10e28-245">As mensagens registradas do JavaScript como essa são chamadas de **mensagens de usuário**.</span><span class="sxs-lookup"><span data-stu-id="10e28-245">Messages logged from JavaScript like this are called **user messages**.</span></span>  <span data-ttu-id="10e28-246">Por outro lado, quando você clicou em **causa 404**, o navegador registrou uma `Error` mensagem de nível informando que o recurso solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="10e28-246">In contrast, when you clicked **Cause 404**, the browser logged an `Error`-level message stating that the requested resource could not be found.</span></span>  <span data-ttu-id="10e28-247">Mensagens como essa são consideradas **mensagens do navegador**.</span><span class="sxs-lookup"><span data-stu-id="10e28-247">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="10e28-248">Use a **barra lateral** para filtrar mensagens do navegador e mostrar apenas mensagens de usuário.</span><span class="sxs-lookup"><span data-stu-id="10e28-248">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="10e28-249">Clique em **9 mensagens de usuário**.</span><span class="sxs-lookup"><span data-stu-id="10e28-249">Click **9 User Messages**.</span></span>  <span data-ttu-id="10e28-250">As mensagens do navegador estão ocultas.</span><span class="sxs-lookup"><span data-stu-id="10e28-250">The browser messages are hidden.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Filtrando mensagens do navegador" lightbox="../media/console-sidebar-user-messages.msft.png":::
       <span data-ttu-id="10e28-252">Filtrando mensagens do navegador</span><span class="sxs-lookup"><span data-stu-id="10e28-252">Filtering out browser messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="10e28-253">Clique em **13 mensagens** para mostrar todas as mensagens novamente.</span><span class="sxs-lookup"><span data-stu-id="10e28-253">Click **13 Messages** to show all messages again.</span></span>  

## <span data-ttu-id="10e28-254">Usar o console juntamente com qualquer outro painel</span><span class="sxs-lookup"><span data-stu-id="10e28-254">Use the Console alongside any other panel</span></span>   

<span data-ttu-id="10e28-255">E se você estiver editando estilos, mas precisar verificar rapidamente o log do console para algo?</span><span class="sxs-lookup"><span data-stu-id="10e28-255">What if you are editing styles, but you need to quickly check the Console log for something?</span></span> <span data-ttu-id="10e28-256">Use a gaveta.</span><span class="sxs-lookup"><span data-stu-id="10e28-256">Use the Drawer.</span></span>  

1.  <span data-ttu-id="10e28-257">Clique na guia **elementos** .</span><span class="sxs-lookup"><span data-stu-id="10e28-257">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="10e28-258">Pressione `Escape` .</span><span class="sxs-lookup"><span data-stu-id="10e28-258">Press `Escape`.</span></span>  <span data-ttu-id="10e28-259">A guia Console da **gaveta** será aberta.</span><span class="sxs-lookup"><span data-stu-id="10e28-259">The Console tab of the **Drawer** opens.</span></span>  <span data-ttu-id="10e28-260">Ele tem todos os recursos do painel do console que você estava usando em todo este tutorial.</span><span class="sxs-lookup"><span data-stu-id="10e28-260">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="A guia Console na gaveta" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         <span data-ttu-id="10e28-262">A guia **console** na **gaveta**</span><span class="sxs-lookup"><span data-stu-id="10e28-262">The **Console** tab in the **Drawer**</span></span>  
    :::image-end:::  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

<!--
 


-->  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge \ (Chromium \) | Documentos da Microsoft"  
[DevToolsCommandMenu]: ../command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Alterar o posicionamento do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsConsoleApi]: ./api.md "Referência de API de console | Documentos da Microsoft"  
[DevToolsConsoleReference]: ./reference.md "Referência do console | Documentos da Microsoft"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Introdução ao registro de mensagens | Problema"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expressões regulares | MDN"  

[RegExrMain]: https://regexr.com "RegEx"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Rastreamento de pilha-Wikipédia"  


> [!NOTE]
> <span data-ttu-id="10e28-272">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="10e28-272">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="10e28-273">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/log) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="10e28-273">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="10e28-275">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="10e28-275">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
