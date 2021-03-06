---
description: Saiba como registrar mensagens no Console.
title: Começar a registrar mensagens no Console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: e2ea1a8327dd2a591e067b69198c4509b2abcb2d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399166"
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

# <a name="get-started-with-logging-messages-in-the-console"></a><span data-ttu-id="922bd-104">Começar a registrar mensagens no Console</span><span class="sxs-lookup"><span data-stu-id="922bd-104">Get started with logging messages in the Console</span></span>  

<span data-ttu-id="922bd-105">Este tutorial interativo mostra como registrar e filtrar mensagens no [console do Microsoft Edge DevTools.][MicrosoftEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="922bd-105">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Mensagens no Console" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   <span data-ttu-id="922bd-107">Mensagens no **Console**</span><span class="sxs-lookup"><span data-stu-id="922bd-107">Messages in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="922bd-108">Este tutorial destina-se a ser concluído em ordem.</span><span class="sxs-lookup"><span data-stu-id="922bd-108">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="922bd-109">Ele supõe que você entenda os fundamentos do desenvolvimento da Web, como como usar JavaScript para adicionar interatividade a uma página.</span><span class="sxs-lookup"><span data-stu-id="922bd-109">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <a name="set-up-the-demo-and-devtools"></a><span data-ttu-id="922bd-110">Configurar a demonstração e o DevTools</span><span class="sxs-lookup"><span data-stu-id="922bd-110">Set up the demo and DevTools</span></span>  

<span data-ttu-id="922bd-111">Este tutorial foi projetado para que você possa abrir a demonstração e experimentar todos os fluxos de trabalho por conta própria.</span><span class="sxs-lookup"><span data-stu-id="922bd-111">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="922bd-112">Quando você acompanha fisicamente, é mais provável que você se lembre mais tarde dos fluxos de trabalho.</span><span class="sxs-lookup"><span data-stu-id="922bd-112">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="922bd-113">Segure `Control` \(Windows, Linux\) ou `Command` \(macOS\) e escolha **Exemplos** de Log de Console para abrir em uma nova guia.</span><span class="sxs-lookup"><span data-stu-id="922bd-113">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="922bd-114">Exemplos de log de console</span><span class="sxs-lookup"><span data-stu-id="922bd-114">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  <span data-ttu-id="922bd-115">Concentre a demonstração e selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\) para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="922bd-115">Focus the demo and then select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="922bd-116">Por padrão, o DevTools é aberto à direita da demonstração.</span><span class="sxs-lookup"><span data-stu-id="922bd-116">By default DevTools opens to the right of the demo.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="DevTools abre à direita da demonstração" lightbox="../media/console-example-devtools-right-console.msft.png":::
             <span data-ttu-id="922bd-118">DevTools abre à direita da demonstração</span><span class="sxs-lookup"><span data-stu-id="922bd-118">DevTools opens to the right of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="922bd-119">[Dock DevTools na parte inferior da janela][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="922bd-119">[Dock DevTools to the bottom of the window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools encaixado na parte inferior da demonstração" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             <span data-ttu-id="922bd-121">DevTools encaixado na parte inferior da demonstração</span><span class="sxs-lookup"><span data-stu-id="922bd-121">DevTools docked to the bottom of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="922bd-122">[Desfazer DevTools em uma janela separada.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="922bd-122">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Navegador em uma janela separada" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             <span data-ttu-id="922bd-124">Navegador em uma janela separada</span><span class="sxs-lookup"><span data-stu-id="922bd-124">Browser in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="922bd-125">[Desfazer DevTools em uma janela separada.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="922bd-125">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools desfazida em uma janela separada" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             <span data-ttu-id="922bd-127">DevTools desfazida em uma janela separada</span><span class="sxs-lookup"><span data-stu-id="922bd-127">DevTools undocked in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="view-messages-logged-from-javascript"></a><span data-ttu-id="922bd-128">Exibir mensagens registradas no JavaScript</span><span class="sxs-lookup"><span data-stu-id="922bd-128">View messages logged from JavaScript</span></span>  

<span data-ttu-id="922bd-129">A maioria das mensagens exibidas no **Console vem** dos desenvolvedores da Web que escreveram o JavaScript da página.</span><span class="sxs-lookup"><span data-stu-id="922bd-129">Most messages that are displayed in the **Console** come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="922bd-130">O objetivo desta seção é apresentar os diferentes tipos de mensagem que você provavelmente revisará no **Console**e explicar como você pode registrar cada tipo de mensagem por conta própria do seu próprio JavaScript.</span><span class="sxs-lookup"><span data-stu-id="922bd-130">The goal of this section is to introduce you to the different message types that you are likely to review in the **Console**, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="922bd-131">Escolha o **botão Informações de** Log na demonstração.</span><span class="sxs-lookup"><span data-stu-id="922bd-131">Choose the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="922bd-132">é registrado no Console.</span><span class="sxs-lookup"><span data-stu-id="922bd-132">gets logged to the Console.</span></span>
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="O Console depois de escolher Informações de Log" lightbox="../media/console-log-info.msft.png":::
       <span data-ttu-id="922bd-134">O **Console depois** de escolher Informações de **Log**</span><span class="sxs-lookup"><span data-stu-id="922bd-134">The **Console** after you choose **Log Info**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="922bd-135">Ao lado da `Hello, Console!` mensagem no Console, escolha **log.js:2**.</span><span class="sxs-lookup"><span data-stu-id="922bd-135">Next to the `Hello, Console!` message in the Console choose **log.js:2**.</span></span>  <span data-ttu-id="922bd-136">O painel Fontes abre e realça a linha de código que fez com que a mensagem seja registrada no Console.</span><span class="sxs-lookup"><span data-stu-id="922bd-136">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="922bd-137">A mensagem foi registrada quando o JavaScript da página foi executar `console.log('Hello, Console!')` .</span><span class="sxs-lookup"><span data-stu-id="922bd-137">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="O DevTools abre a ferramenta Sources depois que você log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       <span data-ttu-id="922bd-139">O DevTools abre a **ferramenta Sources** depois de escolher</span><span class="sxs-lookup"><span data-stu-id="922bd-139">DevTools opens the **Sources** tool after you choose</span></span> `log.js:2`  
    :::image-end:::  
    
1.  <span data-ttu-id="922bd-140">Navegue até **o Console** usando qualquer um dos seguintes fluxos de trabalho:</span><span class="sxs-lookup"><span data-stu-id="922bd-140">Navigate back to the **Console** using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="922bd-141">Escolha a **ferramenta Console.**</span><span class="sxs-lookup"><span data-stu-id="922bd-141">Choose the **Console** tool.</span></span>  
    *   <span data-ttu-id="922bd-142">Selecione `Control` + `[` \(Windows, Linux\) ou `Command` + `[` \(macOS\) até que a **ferramenta Console** está em foco.</span><span class="sxs-lookup"><span data-stu-id="922bd-142">Select `Control`+`[` \(Windows, Linux\) or `Command`+`[` \(macOS\) until the **Console** tool is in focus.</span></span>  
    *   <span data-ttu-id="922bd-143">[Abra o Menu de Comando][DevToolsCommandMenu], digite , escolha o comando Mostrar Painel de `Console` **Console** e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="922bd-143">[Open the Command Menu][DevToolsCommandMenu], type `Console`, choose the **Show Console Panel** command, and then select `Enter`.</span></span>  
    
1.  <span data-ttu-id="922bd-144">Escolha o **botão Aviso de** Log na demonstração.</span><span class="sxs-lookup"><span data-stu-id="922bd-144">Choose the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="922bd-145">é registrado no **Console**.</span><span class="sxs-lookup"><span data-stu-id="922bd-145">gets logged to the **Console**.</span></span>  <span data-ttu-id="922bd-146">Mensagens formatadas assim são avisos.</span><span class="sxs-lookup"><span data-stu-id="922bd-146">Messages formatted like this are warnings.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="O Console depois de escolher Aviso de Log" lightbox="../media/console-log-warning.msft.png":::
       <span data-ttu-id="922bd-148">O **Console depois** de escolher Aviso de **Log**</span><span class="sxs-lookup"><span data-stu-id="922bd-148">The **Console** after you choose **Log Warning**</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="922bd-149">Se você quiser exibir o código que fez com que uma mensagem fosse registrada de uma determinada maneira, escolha em um script \(como \) para exibir o código que fez com que a mensagem fosse `log.js:12` formatada.</span><span class="sxs-lookup"><span data-stu-id="922bd-149">If you want to display the code that caused a message to get logged a certain way, choose on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="922bd-150">Escolha o **ícone Expandir** \( ![ Expand ][ImageExpandIcon] \) na frente de `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="922bd-150">Choose the **Expand** \(![Expand][ImageExpandIcon]\) icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="922bd-151">DevTools mostra o [rastreamento de][WikiStackTrace] pilha que antecede a chamada.</span><span class="sxs-lookup"><span data-stu-id="922bd-151">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Um rastreamento de pilha" lightbox="../media/console-log-warning-expanded.msft.png":::
       <span data-ttu-id="922bd-153">Um rastreamento de pilha</span><span class="sxs-lookup"><span data-stu-id="922bd-153">A stack trace</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="922bd-154">O rastreamento de pilha está dizendo que uma função chamada é executado, que, por sua `logWarning` vez, executa uma função chamada `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="922bd-154">The stack trace is telling you that a function named `logWarning` is run, which in turn runs a function named `quoteDante`.</span></span>  <span data-ttu-id="922bd-155">Em outras palavras, a solicitação que aconteceu primeiro está na parte inferior do rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="922bd-155">In other words, the request that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="922bd-156">Você pode registrar rastreamentos de pilha a qualquer momento executando `console.trace()` .</span><span class="sxs-lookup"><span data-stu-id="922bd-156">You may log stack traces at any time by running `console.trace()`.</span></span>  

1.  <span data-ttu-id="922bd-157">Escolha **Erro de Log**.</span><span class="sxs-lookup"><span data-stu-id="922bd-157">Choose **Log Error**.</span></span>  <span data-ttu-id="922bd-158">A seguinte mensagem de erro é registrada:</span><span class="sxs-lookup"><span data-stu-id="922bd-158">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Uma mensagem de erro" lightbox="../media/console-log-error.msft.png":::
       <span data-ttu-id="922bd-160">Uma mensagem de erro</span><span class="sxs-lookup"><span data-stu-id="922bd-160">An error message</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="922bd-161">Escolha **Tabela de Log**.</span><span class="sxs-lookup"><span data-stu-id="922bd-161">Choose **Log Table**.</span></span>  <span data-ttu-id="922bd-162">Uma tabela sobre os artistas famoso é registrada no **Console**.</span><span class="sxs-lookup"><span data-stu-id="922bd-162">A table about famous artists gets logged to the **Console**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="922bd-163">A `birthday` coluna só é preenchida por uma linha.</span><span class="sxs-lookup"><span data-stu-id="922bd-163">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="922bd-164">Revise o código para determinar por que isso é.</span><span class="sxs-lookup"><span data-stu-id="922bd-164">Review the code to determine why that is.</span></span>
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Uma tabela no Console" lightbox="../media/console-log-table.msft.png":::
       <span data-ttu-id="922bd-166">Uma tabela no **Console**</span><span class="sxs-lookup"><span data-stu-id="922bd-166">A table in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="922bd-167">Escolha **Grupo de Log**.</span><span class="sxs-lookup"><span data-stu-id="922bd-167">Choose **Log Group**.</span></span>  <span data-ttu-id="922bd-168">Os nomes de 4 tartarugas que combatem crimes são agrupados sob o `Adolescent Irradiated Espionage Tortoises` rótulo.</span><span class="sxs-lookup"><span data-stu-id="922bd-168">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Um grupo de mensagens no Console" lightbox="../media/console-log-group.msft.png":::
       <span data-ttu-id="922bd-170">Um grupo de mensagens no **Console**</span><span class="sxs-lookup"><span data-stu-id="922bd-170">A group of messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="922bd-171">Escolha **Log Personalizado**.</span><span class="sxs-lookup"><span data-stu-id="922bd-171">Choose **Log Custom**.</span></span>  <span data-ttu-id="922bd-172">Uma mensagem com borda vermelha e plano de fundo azul é registrada no Console.</span><span class="sxs-lookup"><span data-stu-id="922bd-172">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Uma mensagem com formatação personalizada no Console" lightbox="../media/console-log-custom.msft.png":::
       <span data-ttu-id="922bd-174">Uma mensagem com formatação personalizada no **Console**</span><span class="sxs-lookup"><span data-stu-id="922bd-174">A message with custom formatting in the **Console**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="922bd-175">A ideia principal aqui é que, quando você deseja registrar mensagens no Console do JavaScript, use um dos `console` métodos.</span><span class="sxs-lookup"><span data-stu-id="922bd-175">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="922bd-176">Cada método formatará mensagens de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="922bd-176">Each method formats messages differently.</span></span>  

<span data-ttu-id="922bd-177">Há ainda mais métodos do que o que foi demonstrado nesta seção.</span><span class="sxs-lookup"><span data-stu-id="922bd-177">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="922bd-178">Este tutorial mostra como explorar o restante dos métodos.</span><span class="sxs-lookup"><span data-stu-id="922bd-178">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <a name="view-messages-logged-by-the-browser"></a><span data-ttu-id="922bd-179">Exibir mensagens registradas pelo navegador</span><span class="sxs-lookup"><span data-stu-id="922bd-179">View messages logged by the browser</span></span>  

<span data-ttu-id="922bd-180">O navegador registra mensagens no Console também.</span><span class="sxs-lookup"><span data-stu-id="922bd-180">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="922bd-181">Isso geralmente acontece quando há um problema com a página.</span><span class="sxs-lookup"><span data-stu-id="922bd-181">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="922bd-182">Escolha **Causa 404**.</span><span class="sxs-lookup"><span data-stu-id="922bd-182">Choose **Cause 404**.</span></span>  <span data-ttu-id="922bd-183">O navegador registra um código de status HTTP de erro de rede porque o JavaScript da página tentou buscar um `404` arquivo que não existe.</span><span class="sxs-lookup"><span data-stu-id="922bd-183">The browser logs an HTTP status code of `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Um erro 404 no Console" lightbox="../media/console-cause-404.msft.png":::
       <span data-ttu-id="922bd-185">Um `404` erro no **Console**</span><span class="sxs-lookup"><span data-stu-id="922bd-185">A `404` error in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="922bd-186">Escolha **Causar Erro**.</span><span class="sxs-lookup"><span data-stu-id="922bd-186">Choose **Cause Error**.</span></span>  <span data-ttu-id="922bd-187">O navegador registra um arquivo não detectado porque o JavaScript está tentando atualizar um nó `TypeError` DOM que não existe.</span><span class="sxs-lookup"><span data-stu-id="922bd-187">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="Um TypeError no Console" lightbox="../media/console-cause-error.msft.png":::
       <span data-ttu-id="922bd-189">A `TypeError` no **Console**</span><span class="sxs-lookup"><span data-stu-id="922bd-189">A `TypeError` in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="922bd-190">Escolha o **menu suspenso Níveis de** Log e habilita a opção **Verbose** se estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="922bd-190">Choose the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="922bd-191">Saiba mais sobre filtragem na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="922bd-191">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="922bd-192">Você precisa fazer isso para garantir que a próxima mensagem que você registrar está visível.</span><span class="sxs-lookup"><span data-stu-id="922bd-192">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="922bd-193">Se a lista de menus padrão Níveis estiver desabilitada, talvez seja necessário fechar **a** Barra Lateral do Console.</span><span class="sxs-lookup"><span data-stu-id="922bd-193">If the Default Levels dropdown is disabled, you may need to close the **Console** Sidebar.</span></span>  <span data-ttu-id="922bd-194">Filtrar por Fonte de Mensagem abaixo para obter mais informações sobre a Barra Lateral **do** Console.</span><span class="sxs-lookup"><span data-stu-id="922bd-194">Filter by Message Source below for more information about the **Console** Sidebar.</span></span>
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Habilitando o nível de log Detalhado" lightbox="../media/console-cause-error-log-levels.msft.png":::
       <span data-ttu-id="922bd-196">Habilitando o nível de log Detalhado</span><span class="sxs-lookup"><span data-stu-id="922bd-196">Enabling the Verbose log level</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="922bd-197">Escolha **Violação de Causa**.</span><span class="sxs-lookup"><span data-stu-id="922bd-197">Choose **Cause Violation**.</span></span>  <span data-ttu-id="922bd-198">A página fica sem resposta por alguns segundos e, em seguida, o navegador registra a mensagem `[Violation] 'click' handler took 3000ms` no Console.</span><span class="sxs-lookup"><span data-stu-id="922bd-198">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="922bd-199">A duração exata pode variar.</span><span class="sxs-lookup"><span data-stu-id="922bd-199">The exact duration may vary.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Uma violação no Console" lightbox="../media/console-cause-violation.msft.png":::
       <span data-ttu-id="922bd-201">Uma violação no **Console**</span><span class="sxs-lookup"><span data-stu-id="922bd-201">A violation in the **Console**</span></span>  
    :::image-end:::  
    
## <a name="filter-messages"></a><span data-ttu-id="922bd-202">Filtrar mensagens</span><span class="sxs-lookup"><span data-stu-id="922bd-202">Filter messages</span></span>  

<span data-ttu-id="922bd-203">Em algumas páginas da Web, você revisa **o Console** e é inundado de mensagens.</span><span class="sxs-lookup"><span data-stu-id="922bd-203">On some webpages you review the **Console** get flooded with messages.</span></span>  <span data-ttu-id="922bd-204">O DevTools fornece muitas maneiras diferentes de filtrar mensagens que não são relevantes para a tarefa em questão.</span><span class="sxs-lookup"><span data-stu-id="922bd-204">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <a name="filter-by-log-level"></a><span data-ttu-id="922bd-205">Filtrar por nível de log</span><span class="sxs-lookup"><span data-stu-id="922bd-205">Filter by log level</span></span>  

<span data-ttu-id="922bd-206">Cada `console` método recebe um nível de severidade: , , ou `Verbose` `Info` `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="922bd-206">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="922bd-207">Por exemplo, `console.log()` é uma mensagem de `Info` nível, enquanto é uma mensagem `console.error()` de `Error` nível.</span><span class="sxs-lookup"><span data-stu-id="922bd-207">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="922bd-208">Escolha o **menu suspenso Níveis de** Log e desabilite **Erros**.</span><span class="sxs-lookup"><span data-stu-id="922bd-208">Choose the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="922bd-209">Um nível é desabilitado quando não há mais uma marca de seleção ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="922bd-209">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="922bd-210">As `Error` mensagens de nível desaparecem.</span><span class="sxs-lookup"><span data-stu-id="922bd-210">The `Error`-level messages disappear.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Desabilitar mensagens de nível de erro no Console" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       <span data-ttu-id="922bd-212">Desabilitar mensagens de nível de erro no **Console**</span><span class="sxs-lookup"><span data-stu-id="922bd-212">Disable Error-level messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="922bd-213">Escolha o **menu suspenso Níveis de** Log novamente e reabilitar **Erros**.</span><span class="sxs-lookup"><span data-stu-id="922bd-213">Choose the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="922bd-214">As `Error` mensagens de nível reaparecem.</span><span class="sxs-lookup"><span data-stu-id="922bd-214">The `Error`-level messages reappear.</span></span>  

### <a name="filter-by-text"></a><span data-ttu-id="922bd-215">Filtrar por texto</span><span class="sxs-lookup"><span data-stu-id="922bd-215">Filter by text</span></span>  

<span data-ttu-id="922bd-216">Quando você deseja exibir apenas mensagens que incluem uma cadeia de caracteres exata, digite essa cadeia de caracteres na **caixa de texto Filtrar.**</span><span class="sxs-lookup"><span data-stu-id="922bd-216">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="922bd-217">Digite `Dave` na caixa de **texto** Filtrar.</span><span class="sxs-lookup"><span data-stu-id="922bd-217">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="922bd-218">Todas as mensagens que não incluem a cadeia de `Dave` caracteres estão ocultas.</span><span class="sxs-lookup"><span data-stu-id="922bd-218">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="922bd-219">Você também pode revisar o `Adolescent Irradiated Espionage Tortoises` rótulo.</span><span class="sxs-lookup"><span data-stu-id="922bd-219">You may also review the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="922bd-220">Isso é um bug.</span><span class="sxs-lookup"><span data-stu-id="922bd-220">That is a bug.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Filtrar qualquer mensagem que não inclua Dave" lightbox="../media/console-all-messages-text-filter.msft.png":::
       <span data-ttu-id="922bd-222">Filtrar qualquer mensagem que não inclua</span><span class="sxs-lookup"><span data-stu-id="922bd-222">Filter out any message that does not include</span></span> `Dave`  
    :::image-end:::  
    
1.  <span data-ttu-id="922bd-223">Excluir `Dave` da caixa de **texto** Filtro.</span><span class="sxs-lookup"><span data-stu-id="922bd-223">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="922bd-224">Todas as mensagens reaparecem.</span><span class="sxs-lookup"><span data-stu-id="922bd-224">All the messages reappear.</span></span>  

### <a name="filter-by-regular-expression"></a><span data-ttu-id="922bd-225">Filtrar por expressão regular</span><span class="sxs-lookup"><span data-stu-id="922bd-225">Filter by regular expression</span></span>  

<span data-ttu-id="922bd-226">Quando você quiser mostrar todas as mensagens que incluem um padrão de texto, em vez de uma cadeia de caracteres específica, use uma [expressão regular][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="922bd-226">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="922bd-227">Digite `/^[AH]/` na caixa de **texto** Filtrar.</span><span class="sxs-lookup"><span data-stu-id="922bd-227">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="922bd-228">Digite o padrão em [RegExr][|::ref1::|Main] para uma explicação do que ele está fazendo.</span><span class="sxs-lookup"><span data-stu-id="922bd-228">Type the pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Filtrando qualquer mensagem que não corresponder a um padrão" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       <span data-ttu-id="922bd-230">Filtrando qualquer mensagem que não corresponder ao padrão</span><span class="sxs-lookup"><span data-stu-id="922bd-230">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    :::image-end:::  
    
1.  <span data-ttu-id="922bd-231">Excluir `/^[AH]/` da caixa de **texto** Filtro.</span><span class="sxs-lookup"><span data-stu-id="922bd-231">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="922bd-232">Todas as mensagens estão visíveis novamente.</span><span class="sxs-lookup"><span data-stu-id="922bd-232">All messages are visible again.</span></span>  

### <a name="filter-by-message-source"></a><span data-ttu-id="922bd-233">Filtrar por fonte de mensagem</span><span class="sxs-lookup"><span data-stu-id="922bd-233">Filter by message source</span></span>  

<span data-ttu-id="922bd-234">Quando você quiser exibir apenas as mensagens que vieram de uma determinada URL, use a **barra lateral**.</span><span class="sxs-lookup"><span data-stu-id="922bd-234">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="922bd-235">Escolha **Mostrar Barra Lateral do Console** \( Mostrar Barra Lateral do Console ![ ][ImageShowConsoleSidebarIcon] \).</span><span class="sxs-lookup"><span data-stu-id="922bd-235">Choose **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\).</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="A barra lateral" lightbox="../media/console-sidebar-all-messages.msft.png":::
       <span data-ttu-id="922bd-237">A barra lateral</span><span class="sxs-lookup"><span data-stu-id="922bd-237">The Sidebar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="922bd-238">Escolha o **ícone Expandir** \( ![ Expand ][ImageExpandIcon] \) ao lado do número de mensagens.</span><span class="sxs-lookup"><span data-stu-id="922bd-238">Choose the **Expand** \(![Expand][ImageExpandIcon]\) icon next to the number of messages.</span></span>  <span data-ttu-id="922bd-239">Na figura a seguir, o número de mensagens é indicado como **13 Mensagens**.</span><span class="sxs-lookup"><span data-stu-id="922bd-239">In the following figure, the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="922bd-240">A **barra lateral** mostra uma lista de URLs que causaram o registro de mensagens.</span><span class="sxs-lookup"><span data-stu-id="922bd-240">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="922bd-241">Por exemplo, `log.js` causou 11 mensagens.</span><span class="sxs-lookup"><span data-stu-id="922bd-241">For example, `log.js` caused 11 messages.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Exibindo a origem das mensagens na barra lateral" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       <span data-ttu-id="922bd-243">Exibindo a origem das mensagens na barra lateral</span><span class="sxs-lookup"><span data-stu-id="922bd-243">Viewing the source of messages in the Sidebar</span></span>  
    :::image-end:::  
    
### <a name="filter-by-user-messages"></a><span data-ttu-id="922bd-244">Filtrar por mensagens de usuário</span><span class="sxs-lookup"><span data-stu-id="922bd-244">Filter by user messages</span></span>  

<span data-ttu-id="922bd-245">Anteriormente, quando você escolhe **Informações de Log**, um script chamado para registrar a mensagem no `console.log('Hello, Console!')` Console.</span><span class="sxs-lookup"><span data-stu-id="922bd-245">Earlier, when you choose **Log Info**, a script named `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="922bd-246">As mensagens registradas no JavaScript como esta são chamadas **de mensagens de usuário**.</span><span class="sxs-lookup"><span data-stu-id="922bd-246">Messages logged from JavaScript like this are named **user messages**.</span></span>  <span data-ttu-id="922bd-247">Por outro lado, quando você escolhe **Causa 404**, o navegador registra uma mensagem de nível informando que o recurso `Error` solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="922bd-247">In contrast, when you choose **Cause 404**, the browser logs an `Error`-level message stating that the requested resource is not found.</span></span>  <span data-ttu-id="922bd-248">Mensagens como essa são consideradas **mensagens do navegador**.</span><span class="sxs-lookup"><span data-stu-id="922bd-248">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="922bd-249">Use a **Barra lateral para** filtrar as mensagens do navegador e mostrar apenas mensagens do usuário.</span><span class="sxs-lookup"><span data-stu-id="922bd-249">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="922bd-250">Escolha **9 Mensagens de Usuário**.</span><span class="sxs-lookup"><span data-stu-id="922bd-250">Choose **9 User Messages**.</span></span>  <span data-ttu-id="922bd-251">As mensagens do navegador estão ocultas.</span><span class="sxs-lookup"><span data-stu-id="922bd-251">The browser messages are hidden.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Filtrando mensagens do navegador" lightbox="../media/console-sidebar-user-messages.msft.png":::
       <span data-ttu-id="922bd-253">Filtrando mensagens do navegador</span><span class="sxs-lookup"><span data-stu-id="922bd-253">Filtering out browser messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="922bd-254">Escolha **13 Mensagens para** mostrar todas as mensagens novamente.</span><span class="sxs-lookup"><span data-stu-id="922bd-254">Choose **13 Messages** to show all messages again.</span></span>  

## <a name="use-the-console-alongside-any-other-tools"></a><span data-ttu-id="922bd-255">Use o Console juntamente com qualquer outra ferramenta</span><span class="sxs-lookup"><span data-stu-id="922bd-255">Use the Console alongside any other tools</span></span>  

<span data-ttu-id="922bd-256">Se você estiver editando estilos, mas precisar verificar rapidamente o log do Console para algo, Use a Gaveta.</span><span class="sxs-lookup"><span data-stu-id="922bd-256">If you are editing styles, but you need to quickly check the Console log for something, Use the Drawer.</span></span>  

1.  <span data-ttu-id="922bd-257">Escolha a **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="922bd-257">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="922bd-258">Selecione `Escape` .</span><span class="sxs-lookup"><span data-stu-id="922bd-258">Select `Escape`.</span></span>  <span data-ttu-id="922bd-259">A **ferramenta Console** na **Gaveta** é aberta.</span><span class="sxs-lookup"><span data-stu-id="922bd-259">The **Console** tool in the **Drawer** opens.</span></span>  <span data-ttu-id="922bd-260">Ele tem todos os recursos do painel console que você tem usado durante este tutorial.</span><span class="sxs-lookup"><span data-stu-id="922bd-260">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="A ferramenta Console na Gaveta" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         <span data-ttu-id="922bd-262">A **ferramenta Console** na **Gaveta**</span><span class="sxs-lookup"><span data-stu-id="922bd-262">The **Console** tool in the **Drawer**</span></span>  
    :::image-end:::  
    
## <a name="see-also"></a><span data-ttu-id="922bd-263">Veja também</span><span class="sxs-lookup"><span data-stu-id="922bd-263">See also</span></span>  

*   <span data-ttu-id="922bd-264">Para explorar mais recursos e fluxos de trabalho relacionados à interface do usuário do **Console,** navegue até [Referência do Console][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="922bd-264">To explore more features and workflows related to the **Console** UI,navigate to [Console Reference][DevToolsConsoleApi].</span></span>  
*   <span data-ttu-id="922bd-265">Para saber mais sobre todos os métodos demonstrados em Exibir mensagens registradas no JavaScript e explorar os outros métodos não abordados neste artigo, navegue até Referência da `console` API de [](#view-messages-logged-from-javascript) `console` [Console.][DevToolsConsoleReference]</span><span class="sxs-lookup"><span data-stu-id="922bd-265">To learn more about all of the `console` methods demonstrated in [View messages logged from JavaScript](#view-messages-logged-from-javascript) and explore the other `console` methods not covered in this article, navigate to [Console API Reference][DevToolsConsoleReference].</span></span>  
<!--*   Navigate to [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  
     
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="922bd-266">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="922bd-266">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge \(Chromium\) | Microsoft Docs"  
[DevToolsCommandMenu]: ../command-menu/index.md "Execute comandos com o menu DevTools Command do Microsoft Edge | Microsoft Docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Alterar o posicionamento do Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsConsoleApi]: ./api.md "Referência da API de console | Microsoft Docs"  
[DevToolsConsoleReference]: ./reference.md "Console reference | Microsoft Docs"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Começar a registrar mensagens em log | Glitch"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expressões regulares | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Rastreamento de pilha - Wikipédia"  
> [!NOTE]
> <span data-ttu-id="922bd-276">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="922bd-276">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="922bd-277">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/log) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="922bd-277">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="922bd-279">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="922bd-279">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
