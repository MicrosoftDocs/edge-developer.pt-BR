---
description: Uma introdução à ferramenta Console dentro das ferramentas Microsoft Edge Desenvolvedor.
title: Usar o Console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 3f2f8c01a9bc9c4f40158f0959ba5b60e03bfb80
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483171"
---
# <a name="use-the-console"></a><span data-ttu-id="3fd82-104">Usar o Console</span><span class="sxs-lookup"><span data-stu-id="3fd82-104">Use the Console</span></span>  

<span data-ttu-id="3fd82-105">A **ferramenta Console** do DevTools ajuda você com várias tarefas.</span><span class="sxs-lookup"><span data-stu-id="3fd82-105">The **Console** tool of the DevTools helps you with several tasks.</span></span>  <span data-ttu-id="3fd82-106">A lista a seguir inclui algumas das tarefas.</span><span class="sxs-lookup"><span data-stu-id="3fd82-106">The following list includes some of the tasks.</span></span>  

*   <span data-ttu-id="3fd82-107">Descubra por que algo não está funcionando no projeto atual e [rastreia problemas.][DevtoolsConsoleConsoleDebugJavascript]</span><span class="sxs-lookup"><span data-stu-id="3fd82-107">Find out why something isn't working in the current project and [track down problems][DevtoolsConsoleConsoleDebugJavascript].</span></span>  
*   <span data-ttu-id="3fd82-108">[Obter informações sobre o projeto Web][DevtoolsConsoleConsoleFilters] no navegador como mensagens de log.</span><span class="sxs-lookup"><span data-stu-id="3fd82-108">[Get information about the web project][DevtoolsConsoleConsoleFilters] in the browser as log messages.</span></span>  
*   <span data-ttu-id="3fd82-109">[Informações de][DevtoolsConsoleConsoleLog] log em scripts para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="3fd82-109">[Log information][DevtoolsConsoleConsoleLog] in scripts for debugging purposes.</span></span>  
*   <span data-ttu-id="3fd82-110">[Experimente expressões JavaScript ao][DevtoolsConsoleConsoleJavascript] vivo em um [ambiente REPL.][WikiReadEvalPrintLoop]</span><span class="sxs-lookup"><span data-stu-id="3fd82-110">[Try JavaScript expressions][DevtoolsConsoleConsoleJavascript] live in a [REPL][WikiReadEvalPrintLoop] environment.</span></span>  
*   <span data-ttu-id="3fd82-111">[Interaja com o projeto web no navegador usando][DevtoolsConsoleConsoleDomInteraction] JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3fd82-111">[Interact with the web project in the browser][DevtoolsConsoleConsoleDomInteraction] using JavaScript.</span></span>  
    
<span data-ttu-id="3fd82-112">O **Console** é uma ótima ferramenta de companhia a ser usada com outras ferramentas.</span><span class="sxs-lookup"><span data-stu-id="3fd82-112">The **Console** is a great companion tool to use with others tools.</span></span>  <span data-ttu-id="3fd82-113">O **Console** fornece uma maneira poderosa de executar scripts, inspecionar e manipular a página da Web atual usando JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3fd82-113">The **Console** provides a powerful way to script functionality, inspect, and manipulate the current webpage using JavaScript.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-main.msft.png" alt-text="A ferramenta Console aberta no painel superior" lightbox="../media/console-intro-console-main.msft.png":::
         <span data-ttu-id="3fd82-115">A **ferramenta Console** aberta no painel superior</span><span class="sxs-lookup"><span data-stu-id="3fd82-115">The **Console** tool open in the upper panel</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-panel.msft.png" alt-text="Console no painel inferior com a ferramenta Elements aberta acima dele" lightbox="../media/console-intro-console-panel.msft.png":::
         <span data-ttu-id="3fd82-117">**Console** no painel inferior com a **ferramenta Elements** aberta acima dele</span><span class="sxs-lookup"><span data-stu-id="3fd82-117">**Console** in the lower panel with the **Elements** tool open above it</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="3fd82-118">A maneira mais rápida de abrir diretamente o **Console** é selecionar `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="3fd82-118">The fastest way to directly open the **Console** is to select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

## <a name="error-reports-and-console"></a><span data-ttu-id="3fd82-119">Relatórios de erro e Console</span><span class="sxs-lookup"><span data-stu-id="3fd82-119">Error reports and Console</span></span>  

<span data-ttu-id="3fd82-120">**Console** é o local padrão em que os erros de conectividade e JavaScript são relatados.</span><span class="sxs-lookup"><span data-stu-id="3fd82-120">**Console** is the default place where JavaScript and connectivity errors are reported.</span></span>  <span data-ttu-id="3fd82-121">Se ocorrer algum erro, um botão será exibido ao lado do ícone Configurações **no** DevTools que fornece o número de erros e avisos.</span><span class="sxs-lookup"><span data-stu-id="3fd82-121">If any errors occur, a button displays next to the **Settings** icon in DevTools that provides the number of errors and warnings.</span></span>  <span data-ttu-id="3fd82-122">Escolha-o para abrir **o Console** e exibir o problema.</span><span class="sxs-lookup"><span data-stu-id="3fd82-122">Choose it to open the **Console** and display the problem.</span></span>  <span data-ttu-id="3fd82-123">Para obter mais informações, navegue até [Depurar erros relatados no Console][DevtoolsConsoleConsoleDebugJavascript].</span><span class="sxs-lookup"><span data-stu-id="3fd82-123">For more information, navigate to [Debug errors reported in Console][DevtoolsConsoleConsoleDebugJavascript].</span></span>  

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="O DevTools fornece informações detalhadas sobre o erro no Console" lightbox="../media/console-debug-displays-error.msft.png":::
   <span data-ttu-id="3fd82-125">O DevTools fornece informações detalhadas sobre o erro no **Console**</span><span class="sxs-lookup"><span data-stu-id="3fd82-125">DevTools gives detailed information about the error in the **Console**</span></span>  
:::image-end:::  

## <a name="inspect-and-filter-information-on-the-current-webpage"></a><span data-ttu-id="3fd82-126">Inspecionar e filtrar informações na página da Web atual</span><span class="sxs-lookup"><span data-stu-id="3fd82-126">Inspect and filter information on the current webpage</span></span>  

<span data-ttu-id="3fd82-127">Ao abrir o DevTools em uma página da Web, você provavelmente exibirá um dilúvio de informações registradas no **Console**.</span><span class="sxs-lookup"><span data-stu-id="3fd82-127">When you open the DevTools on a webpage, you're likely to display a deluge of information logged to the **Console**.</span></span>  <span data-ttu-id="3fd82-128">A quantidade de informações se torna um problema quando você precisa identificar informações importantes.</span><span class="sxs-lookup"><span data-stu-id="3fd82-128">The amount of information becomes a problem when you need to identify important information.</span></span>  <span data-ttu-id="3fd82-129">Para exibir as informações importantes que precisam de ação, use a [ferramenta Problemas][DevtoolsIssuesIndex] no DevTools.</span><span class="sxs-lookup"><span data-stu-id="3fd82-129">To view the important information that needs action, use the [Issues][DevtoolsIssuesIndex] tool in DevTools.</span></span>  <span data-ttu-id="3fd82-130">Grande parte do ruído permanece, e é por isso que é uma boa ideia saber sobre as opções automatizadas de [log][DevtoolsConsoleConsoleFilters] e filtro no **Console**.</span><span class="sxs-lookup"><span data-stu-id="3fd82-130">Much of the noise remains, which is why it's a good idea to know about the [automated log and filter options][DevtoolsConsoleConsoleFilters] in the **Console**.</span></span>  

:::image type="complex" source="../media/console-intro-noise.msft.png" alt-text="DevTools com um Console cheio de mensagens" lightbox="../media/console-intro-noise.msft.png":::
   <span data-ttu-id="3fd82-132">DevTools com um **Console** cheio de mensagens</span><span class="sxs-lookup"><span data-stu-id="3fd82-132">DevTools with a **Console** full of messages</span></span>  
:::image-end:::  

## <a name="log-information-to-display-in-the-console"></a><span data-ttu-id="3fd82-133">Informações de log a ser exibidas no Console</span><span class="sxs-lookup"><span data-stu-id="3fd82-133">Log information to display in the Console</span></span>  

<span data-ttu-id="3fd82-134">O caso de uso mais popular para **o Console** é registrar informações de seus scripts usando o método ou outros `console.log()` métodos semelhantes.</span><span class="sxs-lookup"><span data-stu-id="3fd82-134">The most popular use case for the **Console** is logging information from your scripts using the `console.log()` method or other similar methods.</span></span>  <span data-ttu-id="3fd82-135">Para experimentar, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="3fd82-135">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="3fd82-136">Para abrir **Console,** selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="3fd82-136">To open **Console**, select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
1.  <span data-ttu-id="3fd82-137">Navegue [até Console de exemplos de mensagens: log, informações,][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]erro e aviso , ou copie e execute o seguinte trecho de código no **Console**.</span><span class="sxs-lookup"><span data-stu-id="3fd82-137">Navigate to [Console messages examples: log, info, error and warn][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml], or copy and run the following code snippet in the **Console**.</span></span>  
    
    ```javascript
    console.log('This is a log message');
    console.info('This is some information'); 
    console.error('This is an error');
    console.warn('This is a warning');
    console.log(document.body.getBoundingClientRect());
    console.table(document.body.getBoundingClientRect());
    let technologies = ["HTML", "CSS", "SVG", "ECMAScript"];
    console.groupCollapsed('Technolgies');
    technologies.forEach(tech => {console.info(tech);})
    console.groupEnd('Technolgies');
    ```  
    
1.  <span data-ttu-id="3fd82-138">O **Console** exibe os resultados.</span><span class="sxs-lookup"><span data-stu-id="3fd82-138">The **Console** displays the results.</span></span>  
    
    :::image type="complex" source="../media/console-intro-logging.msft.png" alt-text="Console cheio de mensagens causadas pelo código de demonstração" lightbox="../media/console-intro-logging.msft.png":::
       <span data-ttu-id="3fd82-140">**Console** cheio de mensagens causadas pelo código de demonstração</span><span class="sxs-lookup"><span data-stu-id="3fd82-140">**Console** full of messages caused by demo code</span></span>  
    :::image-end:::  
    
<span data-ttu-id="3fd82-141">Muitos métodos úteis estão disponíveis quando você trabalha com o **Console**.</span><span class="sxs-lookup"><span data-stu-id="3fd82-141">Many useful methods are available when you work with the **Console**.</span></span>  <span data-ttu-id="3fd82-142">Para obter mais informações, navegue até [Registrar mensagens na ferramenta Console.][DevtoolsConsoleConsoleLog]</span><span class="sxs-lookup"><span data-stu-id="3fd82-142">For more information, navigate to [Log messages in the Console tool][DevtoolsConsoleConsoleLog].</span></span>  

## <a name="try-your-javascript-live-in-the-console"></a><span data-ttu-id="3fd82-143">Experimente seu JavaScript ao vivo no Console</span><span class="sxs-lookup"><span data-stu-id="3fd82-143">Try your JavaScript live in the Console</span></span>  

<span data-ttu-id="3fd82-144">O **Console** não é apenas um local para registrar informações.</span><span class="sxs-lookup"><span data-stu-id="3fd82-144">The **Console** isn't only a place to log information.</span></span>  <span data-ttu-id="3fd82-145">O **Console** é um [ambiente REPL.][WikiReadEvalPrintLoop]</span><span class="sxs-lookup"><span data-stu-id="3fd82-145">The **Console** is a [REPL][WikiReadEvalPrintLoop] environment.</span></span>  <span data-ttu-id="3fd82-146">Quando você escreve qualquer JavaScript no **Console**, o código é executado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="3fd82-146">When you write any JavaScript in the **Console**, the code runs immediately.</span></span>  <span data-ttu-id="3fd82-147">Você pode achar útil testar alguns novos recursos JavaScript ou fazer alguns cálculos rápidos.</span><span class="sxs-lookup"><span data-stu-id="3fd82-147">You may find it useful to test some new JavaScript features or to do some quick calculations.</span></span>  <span data-ttu-id="3fd82-148">Além disso, você pode obter todos os recursos esperados de um ambiente de edição moderno, como autocompleção, realce de sintaxe e histórico.</span><span class="sxs-lookup"><span data-stu-id="3fd82-148">Also, you get all of the features you expect from a modern editing environment, such as autocompletion, syntax highlighting, and history.</span></span>  <span data-ttu-id="3fd82-149">Para experimentar, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="3fd82-149">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="3fd82-150">Navegue até **o Console**.</span><span class="sxs-lookup"><span data-stu-id="3fd82-150">Navigate to the **Console**.</span></span>  
1.  <span data-ttu-id="3fd82-151">Digite `2 + 2`.</span><span class="sxs-lookup"><span data-stu-id="3fd82-151">Type `2 + 2`.</span></span>  
    
<span data-ttu-id="3fd82-152">O **Console** exibe o resultado `4` na linha a seguir.</span><span class="sxs-lookup"><span data-stu-id="3fd82-152">The **Console** displays the result `4` on the following line.</span></span>  <span data-ttu-id="3fd82-153">Esse **recurso de avaliação** do Eager é útil para depurar e verificar se você não está cometendo erros em seu código.</span><span class="sxs-lookup"><span data-stu-id="3fd82-153">This **Eager evaluation** feature is useful to debug and verify that you aren't making mistakes in your code.</span></span>  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="O Console exibe o resultado de 2 + 2 ao vivo à medida que você digita" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   <span data-ttu-id="3fd82-155">O **Console** exibe o resultado de `2 + 2` vida ao digitá-lo</span><span class="sxs-lookup"><span data-stu-id="3fd82-155">The **Console** displays the result of `2 + 2` live as you type it</span></span>  
:::image-end:::  

<span data-ttu-id="3fd82-156">Para executar a expressão JavaScript no **Console** e, opcionalmente, exibir um resultado, selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3fd82-156">To run the JavaScript expression in the **Console** and optionally display a result, select `Enter`.</span></span>  <span data-ttu-id="3fd82-157">Em seguida, você pode escrever o próximo código JavaScript a ser executado no **Console**.</span><span class="sxs-lookup"><span data-stu-id="3fd82-157">Then, you may write the next JavaScript code to run in the **Console**.</span></span>  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Executar várias linhas de código JavaScript em sucessão" lightbox="../media/console-javascript-several-expressions.msft.png":::
   <span data-ttu-id="3fd82-159">Executar várias linhas de código JavaScript em sucessão</span><span class="sxs-lookup"><span data-stu-id="3fd82-159">Run several lines of JavaScript code in succession</span></span>  
:::image-end:::  

<span data-ttu-id="3fd82-160">Por padrão, você executar código JavaScript em uma única linha.</span><span class="sxs-lookup"><span data-stu-id="3fd82-160">By default, you run JavaScript code on a single line.</span></span>  <span data-ttu-id="3fd82-161">Para executar uma linha, digite o JavaScript e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3fd82-161">To run a line, type your JavaScript and then select `Enter`.</span></span>  <span data-ttu-id="3fd82-162">Para trabalhar com a limitação de linha única, selecione em `Shift` + `Enter` vez de `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3fd82-162">To work around the single-line limitation, select `Shift`+`Enter` instead of `Enter`.</span></span>  <span data-ttu-id="3fd82-163">Semelhante a outras experiências de linha de comando, para acessar seus comandos JavaScript anteriores, selecione `Arrow-Up` .</span><span class="sxs-lookup"><span data-stu-id="3fd82-163">Similar to other command-line experiences, to access your previous JavaScript commands, select `Arrow-Up`.</span></span>  <span data-ttu-id="3fd82-164">O recurso de comcompleção automática do **Console** é uma ótima maneira de aprender sobre métodos desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="3fd82-164">The autocompletion feature of the **Console** is a great way to learn about unfamiliar methods.</span></span>  <span data-ttu-id="3fd82-165">Para experimentar, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="3fd82-165">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="3fd82-166">Abra o **Console**.</span><span class="sxs-lookup"><span data-stu-id="3fd82-166">Open the **Console**.</span></span>  
1.  <span data-ttu-id="3fd82-167">Digite `doc`.</span><span class="sxs-lookup"><span data-stu-id="3fd82-167">Type `doc`.</span></span>  
1.  <span data-ttu-id="3fd82-168">Escolha `document` no menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="3fd82-168">Choose `document` from the dropdown menu.</span></span>  
1.  <span data-ttu-id="3fd82-169">Selecione a `tab` chave para escolher.</span><span class="sxs-lookup"><span data-stu-id="3fd82-169">Select the `tab` key to choose it.</span></span>  
1.  <span data-ttu-id="3fd82-170">Digite `.bo`.</span><span class="sxs-lookup"><span data-stu-id="3fd82-170">Type `.bo`.</span></span>  
1.  <span data-ttu-id="3fd82-171">Selecione `tab` para obter `document.body` .</span><span class="sxs-lookup"><span data-stu-id="3fd82-171">Select `tab` to get `document.body`.</span></span>  
1.  <span data-ttu-id="3fd82-172">Digite outro para exibir a lista completa de propriedades e métodos disponíveis no corpo `.` da página da Web atual.</span><span class="sxs-lookup"><span data-stu-id="3fd82-172">Type another `.` to display the complete list of properties and methods available on the body of the current webpage.</span></span>  
    
<span data-ttu-id="3fd82-173">Para obter mais informações sobre todas as maneiras de trabalhar com **Console,** navegue até [Console como um ambiente JavaScript.][DevtoolsConsoleConsoleJavascript]</span><span class="sxs-lookup"><span data-stu-id="3fd82-173">For more information about all the ways to work with **Console**, navigate to [Console as a JavaScript environment][DevtoolsConsoleConsoleJavascript].</span></span>  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Console autocompletion of JavaScript expressions" lightbox="../media/console-javascript-autocomplete.msft.png":::
   <span data-ttu-id="3fd82-175">**Console** autocompletion of JavaScript expressions</span><span class="sxs-lookup"><span data-stu-id="3fd82-175">**Console** autocompletion of JavaScript expressions</span></span>  
:::image-end:::  

## <a name="interact-with-the-current-webpage-in-the-browser"></a><span data-ttu-id="3fd82-176">Interagir com a página da Web atual no navegador</span><span class="sxs-lookup"><span data-stu-id="3fd82-176">Interact with the current webpage in the browser</span></span>  

<span data-ttu-id="3fd82-177">O **Console** tem acesso ao [objeto Window][MdnDocsWebApiWindow] do navegador.</span><span class="sxs-lookup"><span data-stu-id="3fd82-177">The **Console** has access to the [Window][MdnDocsWebApiWindow] object of the browser.</span></span>  <span data-ttu-id="3fd82-178">Você pode escrever scripts que interagem com a página da Web atual.</span><span class="sxs-lookup"><span data-stu-id="3fd82-178">You may write scripts that interact with the current webpage.</span></span>  <span data-ttu-id="3fd82-179">Para experimentar, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="3fd82-179">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="3fd82-180">Abra o **Console**.</span><span class="sxs-lookup"><span data-stu-id="3fd82-180">Open the **Console**.</span></span>  
1.  <span data-ttu-id="3fd82-181">Copie e colar o seguinte trecho de código.</span><span class="sxs-lookup"><span data-stu-id="3fd82-181">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    document.querySelector('h1').innerHTML
    ```  
    
:::image type="complex" source="../media/console-intro-reading-DOM.msft.png" alt-text="Copiar o conteúdo de título superior (h1) do DOM e exibir no Console" lightbox="../media/console-intro-reading-DOM.msft.png":::
   <span data-ttu-id="3fd82-183">Copie o conteúdo de título superior \( `h1` \) do DOM e exibido no **Console**</span><span class="sxs-lookup"><span data-stu-id="3fd82-183">Copy the top heading \(`h1`\) content from the DOM and display in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="3fd82-184">Em vez de apenas ler da página da Web, você também pode alterá-la.</span><span class="sxs-lookup"><span data-stu-id="3fd82-184">Instead of only reading from the webpage, you may also change it.</span></span>  <span data-ttu-id="3fd82-185">Para experimentar, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="3fd82-185">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="3fd82-186">Abra o **Console**.</span><span class="sxs-lookup"><span data-stu-id="3fd82-186">Open the **Console**.</span></span>  
1.  <span data-ttu-id="3fd82-187">Copie e colar o seguinte trecho de código.</span><span class="sxs-lookup"><span data-stu-id="3fd82-187">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    document.querySelector('h1').innerHTML = 'Rocking the Console';
    ```  
    
:::image type="complex" source="../media/console-intro-wrtiting-DOM.msft.png" alt-text="Gravar texto no DOM no Console" lightbox="../media/console-intro-wrtiting-DOM.msft.png":::
   <span data-ttu-id="3fd82-189">Gravar texto no DOM no **Console**</span><span class="sxs-lookup"><span data-stu-id="3fd82-189">Write text to the DOM in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="3fd82-190">Você alterou o título principal da página da Web para **"Balançando o Console".**</span><span class="sxs-lookup"><span data-stu-id="3fd82-190">You changed the main heading of the webpage to **Rocking the Console**.</span></span>  <span data-ttu-id="3fd82-191">Os **métodos Utilitário** de Console facilitam o acesso e manipulação da página da Web atual.</span><span class="sxs-lookup"><span data-stu-id="3fd82-191">The **Console Utility** methods make it easy to access and manipulate the current webpage.</span></span>  <span data-ttu-id="3fd82-192">Para obter mais informações, navegue até [Console Utilities API reference][DevtoolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="3fd82-192">For more information, navigate to [Console Utilities API reference][DevtoolsConsoleUtilities].</span></span>  <span data-ttu-id="3fd82-193">Por exemplo, para adicionar uma borda verde em torno de todos os links na página da Web atual, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="3fd82-193">For example, to add a green border around all the links in the current webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="3fd82-194">Abra o **Console**.</span><span class="sxs-lookup"><span data-stu-id="3fd82-194">Open the **Console**.</span></span>  
1.  <span data-ttu-id="3fd82-195">Copie e colar o seguinte trecho de código.</span><span class="sxs-lookup"><span data-stu-id="3fd82-195">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    $$('a').forEach(a => a.style.border='1px solid lime');
    ```  
    

:::image type="complex" source="../media/console-intro-changing-styles.msft.png" alt-text="Manipular uma seleção de elementos usando o Console" lightbox="../media/console-intro-changing-styles.msft.png":::
    <span data-ttu-id="3fd82-197">Manipular uma seleção de elementos usando o **Console**</span><span class="sxs-lookup"><span data-stu-id="3fd82-197">Manipulate a selection of elements using the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="3fd82-198">Para obter mais informações sobre como trabalhar com o DOM, navegue até [Usar o Console para interagir com o DOM][DevtoolsConsoleConsoleDomInteraction].</span><span class="sxs-lookup"><span data-stu-id="3fd82-198">For more information about working with the DOM, navigate to [Use the Console to interact with the DOM][DevtoolsConsoleConsoleDomInteraction].</span></span>  

## <a name="learn-more-about-console"></a><span data-ttu-id="3fd82-199">Saiba mais sobre Console</span><span class="sxs-lookup"><span data-stu-id="3fd82-199">Learn more about Console</span></span>  

<span data-ttu-id="3fd82-200">Para obter mais informações sobre **o Console,** navegue até [Referência de Console,][DevtoolsConsoleReference]Referência da [API de Utilitários][DevtoolsConsoleUtilities]de Console e [Referência da API do Console.][DevtoolsConsoleApi]</span><span class="sxs-lookup"><span data-stu-id="3fd82-200">For more information about the **Console**, navigate to [Console reference][DevtoolsConsoleReference], [Console Utilities API reference][DevtoolsConsoleUtilities], and [Console API reference][DevtoolsConsoleApi].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="3fd82-201">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3fd82-201">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Referência da API de console | Microsoft Docs"  
[DevtoolsConsoleConsoleDebugJavascript]: ./console-debug-javascript.md "Erros de depuração relatados no Console | Microsoft Docs"  
[DevtoolsConsoleConsoleDomInteraction]: ./console-dom-interaction.md "Use o Console para interagir com o dom | Microsoft Docs" 
[DevtoolsConsoleConsoleFilters]: ./console-filters.md "Filtrar mensagens de console | Microsoft Docs"  
[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Console como um ambiente JavaScript | Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Registrar mensagens na ferramenta Console | Microsoft Docs"  
[DevtoolsConsoleReference]: ./reference.md "Console reference | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Referência da API de Utilitários de Console | Microsoft Docs"  

[DevtoolsIssuesIndex]: ../issues/index.md "Localizar e corrigir problemas com a ferramenta Issues do DevTools do Microsoft Edge | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-demo.html "Exemplos de mensagens de console: log, informações, erro e aviso | GitHub"  

[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Janela | MDN"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Loop de leitura-eval-print | Wikipédia"  
