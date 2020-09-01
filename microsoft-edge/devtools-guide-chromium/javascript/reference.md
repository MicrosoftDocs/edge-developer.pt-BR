---
title: Referências de Depuração de JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 26f7272534e0834e0fb302a40b7f0ebfc817c88e
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982072"
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







# <span data-ttu-id="dcc37-103">Referência de depuração JavaScript</span><span class="sxs-lookup"><span data-stu-id="dcc37-103">JavaScript debugging reference</span></span>   



<span data-ttu-id="dcc37-104">Descubra os novos fluxos de trabalho de depuração com esta referência abrangente de recursos de depuração do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="dcc37-104">Discover new debugging workflows with this comprehensive reference of Microsoft Edge DevTools debugging features.</span></span>  

<span data-ttu-id="dcc37-105">Consulte [introdução à depuração de JavaScript no Microsoft Edge devtools][DevToolsJavascriptGetStarted] para aprender as noções básicas de depuração.</span><span class="sxs-lookup"><span data-stu-id="dcc37-105">See [Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted] to learn the basics of debugging.</span></span>  

## <span data-ttu-id="dcc37-106">Pausar código com pontos de interrupção</span><span class="sxs-lookup"><span data-stu-id="dcc37-106">Pause code with breakpoints</span></span>   

<span data-ttu-id="dcc37-107">Defina um ponto de interrupção para que você possa pausar seu código no meio do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="dcc37-107">Set a breakpoint so that you are able to pause your code in the middle of the runtime.</span></span>  

<span data-ttu-id="dcc37-108">Consulte [Pausar um código com pontos de interrupção][DevToolsJavascriptBreakpoints] para saber como definir pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="dcc37-108">See [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints] to learn how to set breakpoints.</span></span>  

[DevToolsJavascriptBreakpoints]: breakpoints.md "Como pausar um código com pontos de interrupção no Microsoft Edge DevTools"  

## <span data-ttu-id="dcc37-110">Depurar o código</span><span class="sxs-lookup"><span data-stu-id="dcc37-110">Step through code</span></span>   

<span data-ttu-id="dcc37-111">Depois que o seu código for pausado, percorra-o, uma linha por vez, investigando o fluxo de controle e os valores de propriedade ao longo do caminho.</span><span class="sxs-lookup"><span data-stu-id="dcc37-111">Once your code is paused, step through it, one line at a time, investigating control flow and property values along the way.</span></span>  

### <span data-ttu-id="dcc37-112">Etapa sobre linha de código</span><span class="sxs-lookup"><span data-stu-id="dcc37-112">Step over line of code</span></span>   

<span data-ttu-id="dcc37-113">Quando pausado em uma linha de código contendo uma função que não é relevante para o problema que você está Depurando, clique no ícone de **etapa sobre** \ ( ![ etapa sobre ][ImageStepOverIcon] \) para executar a função sem fazer a depuração.</span><span class="sxs-lookup"><span data-stu-id="dcc37-113">When paused on a line of code containing a function that is not relevant to the problem you are debugging, click on the **Step over** \(![Step over][ImageStepOverIcon]\) icon to run the function without stepping into it.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Selecione passar sobre" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   <span data-ttu-id="dcc37-115">Selecione **passar sobre**</span><span class="sxs-lookup"><span data-stu-id="dcc37-115">Select **Step over**</span></span>  
:::image-end:::  

<span data-ttu-id="dcc37-116">Por exemplo, suponha que você esteja Depurando o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="dcc37-116">For example, suppose you are debugging the following code:</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name); // D
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name; // C
}
```  

<span data-ttu-id="dcc37-117">Você está pausado `A` .</span><span class="sxs-lookup"><span data-stu-id="dcc37-117">You are paused on `A`.</span></span>  <span data-ttu-id="dcc37-118">Pressionando a **etapa**, o devtools executa todo o código na função que você está Depurando, que é `B` e `C` .</span><span class="sxs-lookup"><span data-stu-id="dcc37-118">By pressing **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="dcc37-119">DevTools, em seguida, faz uma pausa `D` .</span><span class="sxs-lookup"><span data-stu-id="dcc37-119">DevTools then pauses on `D`.</span></span>  

### <span data-ttu-id="dcc37-120">Etapa na linha de código</span><span class="sxs-lookup"><span data-stu-id="dcc37-120">Step into line of code</span></span>   

<span data-ttu-id="dcc37-121">Quando pausado em uma linha de código contendo uma chamada de função relacionada ao problema que você está Depurando, clique no ícone **etapa** no \ ( ![ etapa para ][ImageStepIntoIcon] \) para investigar essa função ainda mais.</span><span class="sxs-lookup"><span data-stu-id="dcc37-121">When paused on a line of code containing a function call that is related to the problem you are debugging, click on the **Step into** \(![Step into][ImageStepIntoIcon]\) icon to investigate that function further.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Selecione Step Into" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   <span data-ttu-id="dcc37-123">Selecione **Step Into**</span><span class="sxs-lookup"><span data-stu-id="dcc37-123">Select **Step into**</span></span>  
:::image-end:::  

<span data-ttu-id="dcc37-124">Por exemplo, suponha que você esteja Depurando o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="dcc37-124">For example, suppose you are debugging the following code:</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name);
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name;
}
```  

<span data-ttu-id="dcc37-125">Você está pausado `A` .</span><span class="sxs-lookup"><span data-stu-id="dcc37-125">You are paused on `A`.</span></span>  <span data-ttu-id="dcc37-126">Ao pressionar **Step Into**, o devtools executa essa linha de código e, em seguida, pausa em `B` .</span><span class="sxs-lookup"><span data-stu-id="dcc37-126">By pressing **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <span data-ttu-id="dcc37-127">Etapa da linha de código</span><span class="sxs-lookup"><span data-stu-id="dcc37-127">Step out of line of code</span></span>   

<span data-ttu-id="dcc37-128">Quando pausado dentro de uma função que não está relacionada ao problema que você está Depurando, clique no ícone de **sair da etapa** \ ( ![ depurar ][ImageStepOutIcon] \) para executar o restante do código da função.</span><span class="sxs-lookup"><span data-stu-id="dcc37-128">When paused inside of a function that is not related to the problem you are debugging, click on the **Step out** \(![Step out][ImageStepOutIcon]\) icon to run the rest of the code of the function.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Selecione passar fora" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   <span data-ttu-id="dcc37-130">Selecione **passar fora**</span><span class="sxs-lookup"><span data-stu-id="dcc37-130">Select **Step out**</span></span>  
:::image-end:::  

<span data-ttu-id="dcc37-131">Por exemplo, suponha que você esteja Depurando o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="dcc37-131">For example, suppose you are debugging the following code snippet.</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName();
    updateName(name); // C
}
function getName() {
    var name = app.first + ' ' + app.last; // A
    return name; // B
}
```  

<span data-ttu-id="dcc37-132">Você está pausado `A` .</span><span class="sxs-lookup"><span data-stu-id="dcc37-132">You are paused on `A`.</span></span>  <span data-ttu-id="dcc37-133">Ao pressionar a **etapa**, o devtools executa o restante do código `getName()` , que está apenas `B` neste exemplo e, em seguida, pausa em `C` .</span><span class="sxs-lookup"><span data-stu-id="dcc37-133">By pressing **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <span data-ttu-id="dcc37-134">Executar todo o código em uma linha específica</span><span class="sxs-lookup"><span data-stu-id="dcc37-134">Run all code up to a specific line</span></span>   

<span data-ttu-id="dcc37-135">Durante a depuração de uma função longa, pode haver muitos códigos que não estão relacionados ao problema que você está depurando.</span><span class="sxs-lookup"><span data-stu-id="dcc37-135">When debugging a long function, there may be a lot of code that is not related to the problem you are debugging.</span></span>  

<span data-ttu-id="dcc37-136">Você pode optar por percorrer todas as linhas, mas isso é entediante.</span><span class="sxs-lookup"><span data-stu-id="dcc37-136">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="dcc37-137">Você pode optar por definir um ponto de interrupção de linha de código na linha na qual está interessado e clicar no ícone **retomar** a execução do script \ ( ![ retomar execução do script ][ImageResumeScriptExecutionIcon] \), mas há uma maneira mais rápida.</span><span class="sxs-lookup"><span data-stu-id="dcc37-137">You may choose to set a line-of-code breakpoint on the line in which you are interested and then click on the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) icon, but there is a faster way.</span></span>  

<span data-ttu-id="dcc37-138">Clique com o botão direito do mouse na linha de código na qual você está interessado e selecione **continuar até aqui**.</span><span class="sxs-lookup"><span data-stu-id="dcc37-138">Right-click the line of code in which you are interested, and select **Continue to here**.</span></span>  <span data-ttu-id="dcc37-139">O DevTools executa todo o código até esse ponto e, em seguida, faz uma pausa nessa linha.</span><span class="sxs-lookup"><span data-stu-id="dcc37-139">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Selecione continuar até aqui" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   <span data-ttu-id="dcc37-141">Selecione **continuar até aqui**</span><span class="sxs-lookup"><span data-stu-id="dcc37-141">Select **Continue to here**</span></span>  
:::image-end:::  

### <span data-ttu-id="dcc37-142">Reinicie a função superior da pilha de chamadas</span><span class="sxs-lookup"><span data-stu-id="dcc37-142">Restart the top function of the call stack</span></span>   

<span data-ttu-id="dcc37-143">Enquanto pausado em uma linha de código, clique com o botão direito do mouse em qualquer lugar no painel de **pilha de chamadas** e selecione **reiniciar quadro** para pausar na primeira linha da função superior na pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="dcc37-143">While paused on a line of code, right-click anywhere in the **Call Stack** pane and select **Restart Frame** to pause on the first line of the top function in your call stack.</span></span>  <span data-ttu-id="dcc37-144">A função Top é a última função que foi executada.</span><span class="sxs-lookup"><span data-stu-id="dcc37-144">The top function is the last function that was run.</span></span>  

<span data-ttu-id="dcc37-145">Por exemplo, suponha que você esteja percorrendo o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="dcc37-145">For example, suppose you are stepping through the following code snippet.</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="dcc37-146">Você está pausado `A` .</span><span class="sxs-lookup"><span data-stu-id="dcc37-146">You are paused on `A`.</span></span>  <span data-ttu-id="dcc37-147">Depois de clicar em **reiniciar quadro**, você deve pausar `B` , sem precisar definir um ponto de interrupção ou pressionar **retomar a execução do script**.</span><span class="sxs-lookup"><span data-stu-id="dcc37-147">After clicking **Restart Frame**, you should be paused on `B`, without ever setting a breakpoint or pressing **Resume script execution**.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Selecione reiniciar quadro" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   <span data-ttu-id="dcc37-149">Selecione **reiniciar quadro**</span><span class="sxs-lookup"><span data-stu-id="dcc37-149">Select **Restart Frame**</span></span>  
:::image-end:::  

### <span data-ttu-id="dcc37-150">Retomar o tempo de execução do script</span><span class="sxs-lookup"><span data-stu-id="dcc37-150">Resume script runtime</span></span>   

<span data-ttu-id="dcc37-151">Para continuar o tempo de execução após uma pausa do seu script, clique no ícone **retomar execução do script** \ ( ![ continuar execução do script ][ImageResumeScriptExecutionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="dcc37-151">To continue the runtime after a pause of your script, click on the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) icon.</span></span>  <span data-ttu-id="dcc37-152">DevTools executa o script até o próximo ponto de interrupção, se houver.</span><span class="sxs-lookup"><span data-stu-id="dcc37-152">DevTools runs the script up until the next breakpoint, if any.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Selecione continuar execução do script" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   <span data-ttu-id="dcc37-154">Selecione **continuar execução do script**</span><span class="sxs-lookup"><span data-stu-id="dcc37-154">Select **Resume script execution**</span></span>  
:::image-end:::  

#### <span data-ttu-id="dcc37-155">Forçar tempo de execução de script</span><span class="sxs-lookup"><span data-stu-id="dcc37-155">Force script runtime</span></span>   

<span data-ttu-id="dcc37-156">Para ignorar todos os pontos de interrupção e forçar o reinício do script, clique e mantenha pressionado o ícone continuar execução do **script** \ (retomar execução do script ![ ][ImageResumeScriptExecutionIcon] \) e selecione **forçar execução do script** \ (forçar execução de script ![ ][ImageForceScriptExecutionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="dcc37-156">To ignore all breakpoints and force your script to resume running, click and hold the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) icon and then select **Force script execution** \(![Force script execution][ImageForceScriptExecutionIcon]\).</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Selecione forçar execução de script" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   <span data-ttu-id="dcc37-158">Selecione **forçar execução de script**</span><span class="sxs-lookup"><span data-stu-id="dcc37-158">Select **Force script execution**</span></span>  
:::image-end:::  

### <span data-ttu-id="dcc37-159">Alterar o contexto do thread</span><span class="sxs-lookup"><span data-stu-id="dcc37-159">Change thread context</span></span>   

<span data-ttu-id="dcc37-160">Ao trabalhar com trabalhadores da Web ou funcionários do serviço, clique em um contexto listado no painel **threads** para alternar para esse contexto.</span><span class="sxs-lookup"><span data-stu-id="dcc37-160">When working with web workers or service workers, click on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="dcc37-161">O ícone de seta azul representa qual contexto está selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="dcc37-161">The blue arrow icon represents which context is currently selected.</span></span>  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="O painel threads" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   <span data-ttu-id="dcc37-163">O painel **threads**</span><span class="sxs-lookup"><span data-stu-id="dcc37-163">The **Threads** pane</span></span>  
:::image-end:::  

<span data-ttu-id="dcc37-164">Por exemplo, suponha que você está pausado em um ponto de interrupção no script principal e no seu roteiro de trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="dcc37-164">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="dcc37-165">Você deseja exibir as propriedades locais e globais do contexto do trabalho do serviço, mas o painel **fontes** está mostrando o contexto do script principal.</span><span class="sxs-lookup"><span data-stu-id="dcc37-165">You want to view the local and global properties for the service worker context, but the **Sources** panel is showing the main script context.</span></span>  <span data-ttu-id="dcc37-166">Ao clicar na entrada do serviço de trabalho no painel **threads** , você deve ser capaz de alternar para esse contexto.</span><span class="sxs-lookup"><span data-stu-id="dcc37-166">By clicking on the service worker entry in the **Threads** pane, you should be able to switch to that context.</span></span>  

## <span data-ttu-id="dcc37-167">Exibir e editar propriedades locais, de fechamento e globais</span><span class="sxs-lookup"><span data-stu-id="dcc37-167">View and edit local, closure, and global properties</span></span>   

<span data-ttu-id="dcc37-168">Enquanto pausado em uma linha de código, use o painel **escopo** para exibir e editar os valores de propriedades e variáveis nos escopos local, fechamento e global.</span><span class="sxs-lookup"><span data-stu-id="dcc37-168">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="dcc37-169">Clique duas vezes em um valor de propriedade para alterá-lo.</span><span class="sxs-lookup"><span data-stu-id="dcc37-169">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="dcc37-170">As propriedades não enumeráveis ficam acinzentadas.</span><span class="sxs-lookup"><span data-stu-id="dcc37-170">Non-enumerable properties are greyed out.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="O painel escopo" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   <span data-ttu-id="dcc37-172">O painel **escopo**</span><span class="sxs-lookup"><span data-stu-id="dcc37-172">The **Scope** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="dcc37-173">Exibir a pilha de chamadas atual</span><span class="sxs-lookup"><span data-stu-id="dcc37-173">View the current call stack</span></span>   

<span data-ttu-id="dcc37-174">Enquanto pausado em uma linha de código, use o painel de **pilha de chamadas** para ver a pilha de chamadas que você recebeu para este ponto.</span><span class="sxs-lookup"><span data-stu-id="dcc37-174">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="dcc37-175">Clique em uma entrada para saltar para a linha de código em que essa função foi chamada.</span><span class="sxs-lookup"><span data-stu-id="dcc37-175">Click on an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="dcc37-176">O ícone de seta azul representa qual função DevTools está realçando no momento.</span><span class="sxs-lookup"><span data-stu-id="dcc37-176">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="O painel pilha de chamadas" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   <span data-ttu-id="dcc37-178">O painel **pilha de chamadas**</span><span class="sxs-lookup"><span data-stu-id="dcc37-178">The **Call Stack** pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="dcc37-179">Quando não pausa em uma linha de código, o painel **pilha de chamadas** está vazio.</span><span class="sxs-lookup"><span data-stu-id="dcc37-179">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <span data-ttu-id="dcc37-180">Copiar rastreamento de pilha</span><span class="sxs-lookup"><span data-stu-id="dcc37-180">Copy stack trace</span></span>   

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="dcc37-181">Clique com o botão direito do mouse em qualquer lugar no painel de **pilha de chamadas** e selecione **copiar rastreamento de pilha** para copiar a pilha de chamadas atual para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="dcc37-181">Right-click anywhere in the **Call Stack** pane and select **Copy stack trace** to copy the current call stack to the clipboard.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Selecionar o rastreamento de pilha de cópia" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   <span data-ttu-id="dcc37-183">Selecionar o **rastreamento de pilha de cópia**</span><span class="sxs-lookup"><span data-stu-id="dcc37-183">Select **Copy Stack Trace**</span></span>  
:::image-end:::  

<span data-ttu-id="dcc37-184">Veja a seguir um exemplo da saída:</span><span class="sxs-lookup"><span data-stu-id="dcc37-184">Below is an example of the output:</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## <span data-ttu-id="dcc37-185">Ignorar um script ou um padrão de scripts</span><span class="sxs-lookup"><span data-stu-id="dcc37-185">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="dcc37-186">Marque um script como código da biblioteca quando quiser ignorar esse script durante a depuração.</span><span class="sxs-lookup"><span data-stu-id="dcc37-186">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="dcc37-187">Quando marcado como código de biblioteca, um script fica obscurecido no painel de **pilha de chamadas** , e você nunca percorre as funções do script quando percorre o código.</span><span class="sxs-lookup"><span data-stu-id="dcc37-187">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="dcc37-188">Por exemplo, suponha que você esteja percorrendo o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="dcc37-188">For example, suppose you are stepping through the following code snippet.</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` <span data-ttu-id="dcc37-189">é uma biblioteca de terceiros em que você confia.</span><span class="sxs-lookup"><span data-stu-id="dcc37-189">is a third-party library that you trust.</span></span>  <span data-ttu-id="dcc37-190">Se você tiver certeza de que o problema que está depurando não está relacionado à biblioteca de terceiros, faça sentido marcar o script como código de **biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="dcc37-190">If you are confident that the problem you are debugging is not related to the third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

### <span data-ttu-id="dcc37-191">Marcar um script como código da biblioteca no painel do editor</span><span class="sxs-lookup"><span data-stu-id="dcc37-191">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="dcc37-192">Para marcar um script como **código de biblioteca** no painel do **Editor** :</span><span class="sxs-lookup"><span data-stu-id="dcc37-192">To mark a script as **Library code** from the **Editor** pane:</span></span>  

1.  <span data-ttu-id="dcc37-193">Abra o arquivo.</span><span class="sxs-lookup"><span data-stu-id="dcc37-193">Open the file.</span></span>  
1.  <span data-ttu-id="dcc37-194">Clique com o botão direito do mouse em qualquer lugar.</span><span class="sxs-lookup"><span data-stu-id="dcc37-194">Right-click anywhere.</span></span>  
1.  <span data-ttu-id="dcc37-195">Selecione **Marcar como código da biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="dcc37-195">Select **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Marcando um script como código de biblioteca no painel do editor" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       <span data-ttu-id="dcc37-197">Marcando um script como **código de biblioteca** no painel do **Editor**</span><span class="sxs-lookup"><span data-stu-id="dcc37-197">Marking a script as **Library code** from the **Editor** pane</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="dcc37-198">Marcar um script como código da biblioteca no painel pilha de chamadas</span><span class="sxs-lookup"><span data-stu-id="dcc37-198">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="dcc37-199">Para marcar um script como **código de biblioteca** no painel **pilha de chamadas** :</span><span class="sxs-lookup"><span data-stu-id="dcc37-199">To mark a script as **Library code** from the **Call Stack** pane:</span></span>  

1.  <span data-ttu-id="dcc37-200">Clique com o botão direito do mouse em uma função do script.</span><span class="sxs-lookup"><span data-stu-id="dcc37-200">Right-click on a function from the script.</span></span>  
1.  <span data-ttu-id="dcc37-201">Selecione **Marcar como código da biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="dcc37-201">Select **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Marcando um script como código da biblioteca no painel pilha de chamadas" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       <span data-ttu-id="dcc37-203">Marcando um script como **código da biblioteca** no painel pilha de **chamadas**</span><span class="sxs-lookup"><span data-stu-id="dcc37-203">Marking a script as **Library code** from the **Call Stack** pane</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="dcc37-204">Marcar um script como código de biblioteca em configurações</span><span class="sxs-lookup"><span data-stu-id="dcc37-204">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="dcc37-205">Para marcar um único script ou um padrão de scripts em configurações:</span><span class="sxs-lookup"><span data-stu-id="dcc37-205">To mark a single script or pattern of scripts from Settings:</span></span>  

1.  <span data-ttu-id="dcc37-206">Abrir [as configurações][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="dcc37-206">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="dcc37-207">Vá para a guia **código da biblioteca** .</span><span class="sxs-lookup"><span data-stu-id="dcc37-207">Go to the **Library code** tab.</span></span>  
1.  <span data-ttu-id="dcc37-208">Clique em **Adicionar padrão**.</span><span class="sxs-lookup"><span data-stu-id="dcc37-208">Click **Add pattern**.</span></span>  
1.  <span data-ttu-id="dcc37-209">Digite o nome do script ou um padrão de Regex de nomes de script para marcar como **código de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="dcc37-209">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="dcc37-210">Clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="dcc37-210">Click **Add**.</span></span>  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Marcando um script como código de biblioteca em configurações" lightbox="../media/javascript-framework-library-code.msft.png":::
       <span data-ttu-id="dcc37-212">Marcando um script como **código de biblioteca** em **configurações**</span><span class="sxs-lookup"><span data-stu-id="dcc37-212">Marking a script as **Library code** from **Settings**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="dcc37-213">Executar trechos de código de depuração de qualquer página</span><span class="sxs-lookup"><span data-stu-id="dcc37-213">Run snippets of debug code from any page</span></span>   

<span data-ttu-id="dcc37-214">Se você estiver executando o mesmo código de depuração no console repetidamente, considere os trechos de código.</span><span class="sxs-lookup"><span data-stu-id="dcc37-214">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="dcc37-215">Trechos de código são scripts de tempo de execução que você cria, armazena e executa dentro do DevTools.</span><span class="sxs-lookup"><span data-stu-id="dcc37-215">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="dcc37-216">Consulte [executar trechos de código em qualquer página][DevToolsJavascriptSnippets] para saber mais.</span><span class="sxs-lookup"><span data-stu-id="dcc37-216">See [Run Snippets of Code From Any Page][DevToolsJavascriptSnippets] to learn more.</span></span>  

## <span data-ttu-id="dcc37-217">Assista aos valores de expressões JavaScript personalizadas</span><span class="sxs-lookup"><span data-stu-id="dcc37-217">Watch the values of custom JavaScript expressions</span></span>   

<span data-ttu-id="dcc37-218">Use o painel de **inspeção** para ver os valores de expressões personalizadas.</span><span class="sxs-lookup"><span data-stu-id="dcc37-218">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="dcc37-219">Você pode assistir a uma expressão JavaScript válida.</span><span class="sxs-lookup"><span data-stu-id="dcc37-219">You may watch any valid JavaScript expression.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="O painel de inspeção" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   <span data-ttu-id="dcc37-221">O painel de **inspeção**</span><span class="sxs-lookup"><span data-stu-id="dcc37-221">The **Watch** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="dcc37-222">Clique no ícone **Adicionar expressão** \ ( ![ Adicionar expressão ][ImageAddExpressionIcon] \) para criar uma nova expressão de inspeção.</span><span class="sxs-lookup"><span data-stu-id="dcc37-222">Click on the **Add Expression** \(![Add Expression][ImageAddExpressionIcon]\) icon to create a new watch expression.</span></span>  
*   <span data-ttu-id="dcc37-223">Clique no ícone **Atualizar** \ ( ![ Atualizar ][ImageRefreshIcon] \) para atualizar os valores de todas as expressões existentes.</span><span class="sxs-lookup"><span data-stu-id="dcc37-223">Click on the **Refresh** \(![Refresh][ImageRefreshIcon]\) icon to refresh the values of all existing expressions.</span></span>  <span data-ttu-id="dcc37-224">Valores são atualizados automaticamente durante a depuração do código.</span><span class="sxs-lookup"><span data-stu-id="dcc37-224">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="dcc37-225">Passe o mouse sobre uma expressão e clique no ícone **excluir expressão** \ ( ![ excluir expressão ][ImageDeleteExpressionIcon] \) para excluí-la.</span><span class="sxs-lookup"><span data-stu-id="dcc37-225">Hover over an expression and click on the **Delete Expression** \(![Delete Expression][ImageDeleteExpressionIcon]\) icon to delete it.</span></span>  
    
## <span data-ttu-id="dcc37-226">Torne um arquivo do minified legível</span><span class="sxs-lookup"><span data-stu-id="dcc37-226">Make a minified file readable</span></span>   

<span data-ttu-id="dcc37-227">Clique no ícone **formato** \ ( ![ formato ][ImageFormatIcon] \) para fazer com que um arquivo do minified seja legível pelo homem.</span><span class="sxs-lookup"><span data-stu-id="dcc37-227">Click on the **Format** \(![Format][ImageFormatIcon]\) icon to make a minified file human-readable.</span></span>  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="O botão Formatar" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   <span data-ttu-id="dcc37-229">O botão **Formatar**</span><span class="sxs-lookup"><span data-stu-id="dcc37-229">The **Format** button</span></span>  
:::image-end:::  

## <span data-ttu-id="dcc37-230">Editar um script</span><span class="sxs-lookup"><span data-stu-id="dcc37-230">Edit a script</span></span>   

<span data-ttu-id="dcc37-231">Ao corrigir um bug, você muitas vezes deseja testar algumas alterações no código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dcc37-231">When fixing a bug, you often want to test out some changes to your JavaScript code.</span></span>  <span data-ttu-id="dcc37-232">Você não precisa fazer as alterações em um editor externo ou IDE e, em seguida, recarregar a página.</span><span class="sxs-lookup"><span data-stu-id="dcc37-232">You do not need to make the changes in an external editor or IDE and then reload the page.</span></span>  <span data-ttu-id="dcc37-233">Você pode editar o script no DevTools.</span><span class="sxs-lookup"><span data-stu-id="dcc37-233">You may edit your script in DevTools.</span></span>  

<span data-ttu-id="dcc37-234">Para editar um script:</span><span class="sxs-lookup"><span data-stu-id="dcc37-234">To edit a script:</span></span>  

1.  <span data-ttu-id="dcc37-235">Abra o arquivo no painel **Editor** do painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="dcc37-235">Open the file in the **Editor** pane of the **Sources** panel.</span></span>  
1.  <span data-ttu-id="dcc37-236">Faça suas alterações no painel do **Editor** .</span><span class="sxs-lookup"><span data-stu-id="dcc37-236">Make your changes in the **Editor** pane.</span></span>  
1.  <span data-ttu-id="dcc37-237">Pressione `Ctrl` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) para salvar.</span><span class="sxs-lookup"><span data-stu-id="dcc37-237">Press `Ctrl`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="dcc37-238">O DevTools patches de todo o arquivo JS para o mecanismo JavaScript do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dcc37-238">DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Painel do editor" lightbox="../media/javascript-sources-html-minified.msft.png":::
       <span data-ttu-id="dcc37-240">Painel do **Editor**</span><span class="sxs-lookup"><span data-stu-id="dcc37-240">The **Editor** pane</span></span>  
    :::image-end:::  
     
## <span data-ttu-id="dcc37-241">Desabilitar o JavaScript</span><span class="sxs-lookup"><span data-stu-id="dcc37-241">Disable JavaScript</span></span>   

<span data-ttu-id="dcc37-242">Consulte [desabilitar JavaScript com o Microsoft Edge devtools][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="dcc37-242">See [Disable JavaScript with Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageStepOverIcon]: ../media/step-over-icon.msft.png  
[ImageStepIntoIcon]: ../media/step-into-icon.msft.png  
[ImageStepOutIcon]: ../media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: ../media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: ../media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: ../media/add-expression-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: ../media/delete-expression-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  

<!-- links -->  

[DevToolsJavascriptDisable]: ./disable.md "Desabilitar JavaScript com o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsJavascriptGetStarted]: ./index.md "Introdução à depuração JavaScript no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsJavascriptSnippets]: ./snippets.md "Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsCustomize]: ../customize/index.md "Personalizar o Microsoft Edge DevTools | Documentos da Microsoft"  

> [!NOTE]
> <span data-ttu-id="dcc37-247">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="dcc37-247">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dcc37-248">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="dcc37-248">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="dcc37-250">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dcc37-250">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
