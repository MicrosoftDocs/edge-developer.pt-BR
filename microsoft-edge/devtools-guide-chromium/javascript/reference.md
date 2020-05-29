---
title: Referência de depuração JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 1d361bb39523e9b039500f46da54e60b82adbda6
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581737"
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







# <span data-ttu-id="2d024-103">Referência de depuração JavaScript</span><span class="sxs-lookup"><span data-stu-id="2d024-103">JavaScript Debugging Reference</span></span>   



<span data-ttu-id="2d024-104">Descubra os novos fluxos de trabalho de depuração com esta referência abrangente de recursos de depuração do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="2d024-104">Discover new debugging workflows with this comprehensive reference of Microsoft Edge DevTools debugging features.</span></span>  

<span data-ttu-id="2d024-105">Consulte [introdução à depuração de JavaScript no Microsoft Edge devtools][DevToolsJavascriptGetStarted] para aprender as noções básicas de depuração.</span><span class="sxs-lookup"><span data-stu-id="2d024-105">See [Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted] to learn the basics of debugging.</span></span>  

## <span data-ttu-id="2d024-106">Pausar código com pontos de interrupção</span><span class="sxs-lookup"><span data-stu-id="2d024-106">Pause code with breakpoints</span></span>   

<span data-ttu-id="2d024-107">Defina um ponto de interrupção para que você possa pausar seu código no meio do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="2d024-107">Set a breakpoint so that you are able to pause your code in the middle of the runtime.</span></span>  

<span data-ttu-id="2d024-108">Consulte [Pausar um código com pontos de interrupção][DevToolsJavascriptBreakpoints] para saber como definir pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="2d024-108">See [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints] to learn how to set breakpoints.</span></span>  

[DevToolsJavascriptBreakpoints]: breakpoints.md "Como pausar um código com pontos de interrupção no Microsoft Edge DevTools"  

## <span data-ttu-id="2d024-110">Depurar o código</span><span class="sxs-lookup"><span data-stu-id="2d024-110">Step through code</span></span>   

<span data-ttu-id="2d024-111">Depois que o seu código for pausado, percorra-o, uma linha por vez, investigando o fluxo de controle e os valores de propriedade ao longo do caminho.</span><span class="sxs-lookup"><span data-stu-id="2d024-111">Once your code is paused, step through it, one line at a time, investigating control flow and property values along the way.</span></span>  

### <span data-ttu-id="2d024-112">Etapa sobre linha de código</span><span class="sxs-lookup"><span data-stu-id="2d024-112">Step over line of code</span></span>   

<span data-ttu-id="2d024-113">Quando pausado em uma linha de código contendo uma função que não é relevante para o problema que você está Depurando, clique no ícone de **etapa sobre** a etapa sobre ![ ][ImageStepOverIcon] para executar a função sem fazer a depuração.</span><span class="sxs-lookup"><span data-stu-id="2d024-113">When paused on a line of code containing a function that is not relevant to the problem you are debugging, click on the **Step over** ![Step over][ImageStepOverIcon] icon to run the function without stepping into it.</span></span>  

> ##### <span data-ttu-id="2d024-114">Figura 1</span><span class="sxs-lookup"><span data-stu-id="2d024-114">Figure 1</span></span>  
> <span data-ttu-id="2d024-115">Selecionando o passar **sobre**</span><span class="sxs-lookup"><span data-stu-id="2d024-115">Selecting **Step over**</span></span>  
> ![Selecionando o passar sobre][ImageSelectingStepOver]  

<span data-ttu-id="2d024-117">Por exemplo, suponha que você esteja Depurando o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="2d024-117">For example, suppose you are debugging the following code:</span></span>  

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

<span data-ttu-id="2d024-118">Você está pausado `A` .</span><span class="sxs-lookup"><span data-stu-id="2d024-118">You are paused on `A`.</span></span>  <span data-ttu-id="2d024-119">Pressionando a **etapa**, o devtools executa todo o código na função que você está Depurando, que é `B` e `C` .</span><span class="sxs-lookup"><span data-stu-id="2d024-119">By pressing **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="2d024-120">DevTools, em seguida, faz uma pausa `D` .</span><span class="sxs-lookup"><span data-stu-id="2d024-120">DevTools then pauses on `D`.</span></span>  

### <span data-ttu-id="2d024-121">Etapa na linha de código</span><span class="sxs-lookup"><span data-stu-id="2d024-121">Step into line of code</span></span>   

<span data-ttu-id="2d024-122">Quando pausado em uma linha de código contendo uma chamada de função relacionada ao problema que você está Depurando, clique no ícone **Step Into** ![ Step Into ][ImageStepIntoIcon] para investigar mais a função.</span><span class="sxs-lookup"><span data-stu-id="2d024-122">When paused on a line of code containing a function call that is related to the problem you are debugging, click on the **Step into** ![Step into][ImageStepIntoIcon] icon to investigate that function further.</span></span>  

> ##### <span data-ttu-id="2d024-123">Figura 2</span><span class="sxs-lookup"><span data-stu-id="2d024-123">Figure 2</span></span>  
> <span data-ttu-id="2d024-124">Selecionando **a etapa em**</span><span class="sxs-lookup"><span data-stu-id="2d024-124">Selecting **Step into**</span></span>  
> ![Selecionando a etapa em][ImageSelectingStepInto]  

<span data-ttu-id="2d024-126">Por exemplo, suponha que você esteja Depurando o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="2d024-126">For example, suppose you are debugging the following code:</span></span>  

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

<span data-ttu-id="2d024-127">Você está pausado `A` .</span><span class="sxs-lookup"><span data-stu-id="2d024-127">You are paused on `A`.</span></span>  <span data-ttu-id="2d024-128">Ao pressionar **Step Into**, o devtools executa essa linha de código e, em seguida, pausa em `B` .</span><span class="sxs-lookup"><span data-stu-id="2d024-128">By pressing **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <span data-ttu-id="2d024-129">Etapa da linha de código</span><span class="sxs-lookup"><span data-stu-id="2d024-129">Step out of line of code</span></span>   

<span data-ttu-id="2d024-130">Quando pausado dentro de uma função que não está relacionada ao problema que você está Depurando, clique no ícone de Step **out** Step Out ![ ][ImageStepOutIcon] para executar o restante do código da função.</span><span class="sxs-lookup"><span data-stu-id="2d024-130">When paused inside of a function that is not related to the problem you are debugging, click on the **Step out** ![Step out][ImageStepOutIcon] icon to run the rest of the code of the function.</span></span>  

> ##### <span data-ttu-id="2d024-131">Figura 3</span><span class="sxs-lookup"><span data-stu-id="2d024-131">Figure 3</span></span>  
> <span data-ttu-id="2d024-132">Selecionando o **Step Out**</span><span class="sxs-lookup"><span data-stu-id="2d024-132">Selecting **Step out**</span></span>  
> ![Selecionando o Step Out][ImageSelectingStepOut]  

<span data-ttu-id="2d024-134">Por exemplo, suponha que você esteja Depurando o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="2d024-134">For example, suppose you are debugging the following code:</span></span>  

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

<span data-ttu-id="2d024-135">Você está pausado `A` .</span><span class="sxs-lookup"><span data-stu-id="2d024-135">You are paused on `A`.</span></span>  <span data-ttu-id="2d024-136">Ao pressionar a **etapa**, o devtools executa o restante do código `getName()` , que está apenas `B` neste exemplo e, em seguida, pausa em `C` .</span><span class="sxs-lookup"><span data-stu-id="2d024-136">By pressing **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <span data-ttu-id="2d024-137">Executar todo o código em uma linha específica</span><span class="sxs-lookup"><span data-stu-id="2d024-137">Run all code up to a specific line</span></span>   

<span data-ttu-id="2d024-138">Durante a depuração de uma função longa, pode haver muitos códigos que não estão relacionados ao problema que você está depurando.</span><span class="sxs-lookup"><span data-stu-id="2d024-138">When debugging a long function, there may be a lot of code that is not related to the problem you are debugging.</span></span>  

<span data-ttu-id="2d024-139">Você pode optar por percorrer todas as linhas, mas isso é entediante.</span><span class="sxs-lookup"><span data-stu-id="2d024-139">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="2d024-140">Você pode optar por definir um ponto de interrupção de linha de código na linha em que você está interessado e clicar no ícone **retomar** a ![ execução do script de retomada de script ][ImageResumeScriptExecutionIcon] , mas há uma maneira mais rápida.</span><span class="sxs-lookup"><span data-stu-id="2d024-140">You may choose to set a line-of-code breakpoint on the line in which you are interested and then click on the **Resume Script Execution** ![Resume Script Execution][ImageResumeScriptExecutionIcon] icon, but there is a faster way.</span></span>  

<span data-ttu-id="2d024-141">Clique com o botão direito do mouse na linha de código na qual você está interessado e selecione **continuar até aqui**.</span><span class="sxs-lookup"><span data-stu-id="2d024-141">Right-click the line of code in which you are interested, and select **Continue to here**.</span></span>  <span data-ttu-id="2d024-142">O DevTools executa todo o código até esse ponto e, em seguida, faz uma pausa nessa linha.</span><span class="sxs-lookup"><span data-stu-id="2d024-142">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

> ##### <span data-ttu-id="2d024-143">Figura 4</span><span class="sxs-lookup"><span data-stu-id="2d024-143">Figure 4</span></span>  
> <span data-ttu-id="2d024-144">Selecione **continuar até aqui**</span><span class="sxs-lookup"><span data-stu-id="2d024-144">Selecting **Continue to here**</span></span>  
> ![Selecione continuar até aqui][ImageSelectingContinueToHere]  

### <span data-ttu-id="2d024-146">Reinicie a função superior da pilha de chamadas</span><span class="sxs-lookup"><span data-stu-id="2d024-146">Restart the top function of the call stack</span></span>   

<span data-ttu-id="2d024-147">Enquanto pausado em uma linha de código, clique com o botão direito do mouse em qualquer lugar no painel de **pilha de chamadas** e selecione **reiniciar quadro** para pausar na primeira linha da função superior na pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="2d024-147">While paused on a line of code, right-click anywhere in the **Call Stack** pane and select **Restart Frame** to pause on the first line of the top function in your call stack.</span></span>  <span data-ttu-id="2d024-148">A função Top é a última função que foi chamada.</span><span class="sxs-lookup"><span data-stu-id="2d024-148">The top function is the last function that was called.</span></span>  

<span data-ttu-id="2d024-149">Por exemplo, suponha que você esteja percorrendo o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="2d024-149">For example, suppose you are stepping through the following code:</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="2d024-150">Você está pausado `A` .</span><span class="sxs-lookup"><span data-stu-id="2d024-150">You are paused on `A`.</span></span>  <span data-ttu-id="2d024-151">Depois de clicar em **reiniciar quadro**, você deve pausar `B` , sem precisar definir um ponto de interrupção ou pressionar **retomar a execução do script**.</span><span class="sxs-lookup"><span data-stu-id="2d024-151">After clicking **Restart Frame**, you should be paused on `B`, without ever setting a breakpoint or pressing **Resume script execution**.</span></span>  

> ##### <span data-ttu-id="2d024-152">Figura 5</span><span class="sxs-lookup"><span data-stu-id="2d024-152">Figure 5</span></span>  
> <span data-ttu-id="2d024-153">Selecionar **reiniciar quadro**</span><span class="sxs-lookup"><span data-stu-id="2d024-153">Selecting **Restart Frame**</span></span>  
> ![Selecionar reiniciar quadro][ImageSelectingRestartFrame]  

### <span data-ttu-id="2d024-155">Retomar o tempo de execução do script</span><span class="sxs-lookup"><span data-stu-id="2d024-155">Resume script runtime</span></span>   

<span data-ttu-id="2d024-156">Para continuar o tempo de execução após uma pausa do seu script, clique no ícone de execução **retomar** ![ script de retomada de execução de script ][ImageResumeScriptExecutionIcon] .</span><span class="sxs-lookup"><span data-stu-id="2d024-156">To continue the runtime after a pause of your script, click on the **Resume Script Execution** ![Resume Script Execution][ImageResumeScriptExecutionIcon] icon.</span></span>  <span data-ttu-id="2d024-157">DevTools executa o script até o próximo ponto de interrupção, se houver.</span><span class="sxs-lookup"><span data-stu-id="2d024-157">DevTools runs the script up until the next breakpoint, if any.</span></span>  

> ##### <span data-ttu-id="2d024-158">Figura 6</span><span class="sxs-lookup"><span data-stu-id="2d024-158">Figure 6</span></span>  
> <span data-ttu-id="2d024-159">Selecionando **continuar execução do script**</span><span class="sxs-lookup"><span data-stu-id="2d024-159">Selecting **Resume script execution**</span></span>  
> ![Selecionando continuar execução do script][ImageSelectingResumeScriptExecution]  

#### <span data-ttu-id="2d024-161">Forçar tempo de execução de script</span><span class="sxs-lookup"><span data-stu-id="2d024-161">Force script runtime</span></span>   

<span data-ttu-id="2d024-162">Para ignorar todos os pontos de interrupção e forçar o reinício do script, clique e mantenha pressionado o ícone de execução do script de retomada da **execução** do script ![ ][ImageResumeScriptExecutionIcon] e, em seguida, selecione **forçar** execução do script ![ Force ][ImageForceScriptExecutionIcon] .</span><span class="sxs-lookup"><span data-stu-id="2d024-162">To ignore all breakpoints and force your script to resume running, click and hold the **Resume Script Execution** ![Resume Script Execution][ImageResumeScriptExecutionIcon] icon and then select **Force script execution** ![Force script execution][ImageForceScriptExecutionIcon].</span></span>  

> ##### <span data-ttu-id="2d024-163">Figura 7</span><span class="sxs-lookup"><span data-stu-id="2d024-163">Figure 7</span></span>  
> <span data-ttu-id="2d024-164">Selecionar **forçar execução de script**</span><span class="sxs-lookup"><span data-stu-id="2d024-164">Selecting **Force script execution**</span></span>  
> ![Selecionar forçar execução de script][ImageSelectingForceScriptExecution]  

### <span data-ttu-id="2d024-166">Alterar o contexto do thread</span><span class="sxs-lookup"><span data-stu-id="2d024-166">Change thread context</span></span>   

<span data-ttu-id="2d024-167">Ao trabalhar com trabalhadores da Web ou funcionários do serviço, clique em um contexto listado no painel **threads** para alternar para esse contexto.</span><span class="sxs-lookup"><span data-stu-id="2d024-167">When working with web workers or service workers, click on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="2d024-168">O ícone de seta azul representa qual contexto está selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="2d024-168">The blue arrow icon represents which context is currently selected.</span></span>  

> ##### <span data-ttu-id="2d024-169">Figura 8</span><span class="sxs-lookup"><span data-stu-id="2d024-169">Figure 8</span></span>  
> <span data-ttu-id="2d024-170">O painel **threads**</span><span class="sxs-lookup"><span data-stu-id="2d024-170">The **Threads** pane</span></span>  
> ![O painel threads][ImageThreadsPane]  

<span data-ttu-id="2d024-172">Por exemplo, suponha que você está pausado em um ponto de interrupção no script principal e no seu roteiro de trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="2d024-172">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="2d024-173">Você deseja exibir as propriedades locais e globais do contexto do trabalho do serviço, mas o painel **fontes** está mostrando o contexto do script principal.</span><span class="sxs-lookup"><span data-stu-id="2d024-173">You want to view the local and global properties for the service worker context, but the **Sources** panel is showing the main script context.</span></span>  <span data-ttu-id="2d024-174">Ao clicar na entrada do serviço de trabalho no painel **threads** , você deve ser capaz de alternar para esse contexto.</span><span class="sxs-lookup"><span data-stu-id="2d024-174">By clicking on the service worker entry in the **Threads** pane, you should be able to switch to that context.</span></span>  

## <span data-ttu-id="2d024-175">Exibir e editar propriedades locais, de fechamento e globais</span><span class="sxs-lookup"><span data-stu-id="2d024-175">View and edit local, closure, and global properties</span></span>   

<span data-ttu-id="2d024-176">Enquanto pausado em uma linha de código, use o painel **escopo** para exibir e editar os valores de propriedades e variáveis nos escopos local, fechamento e global.</span><span class="sxs-lookup"><span data-stu-id="2d024-176">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="2d024-177">Clique duas vezes em um valor de propriedade para alterá-lo.</span><span class="sxs-lookup"><span data-stu-id="2d024-177">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="2d024-178">As propriedades não enumeráveis ficam acinzentadas.</span><span class="sxs-lookup"><span data-stu-id="2d024-178">Non-enumerable properties are greyed out.</span></span>  

> ##### <span data-ttu-id="2d024-179">Figura 9</span><span class="sxs-lookup"><span data-stu-id="2d024-179">Figure 9</span></span>  
> <span data-ttu-id="2d024-180">O painel **escopo**</span><span class="sxs-lookup"><span data-stu-id="2d024-180">The **Scope** pane</span></span>  
> ![O painel escopo][ImageScopePane]  

## <span data-ttu-id="2d024-182">Exibir a pilha de chamadas atual</span><span class="sxs-lookup"><span data-stu-id="2d024-182">View the current call stack</span></span>   

<span data-ttu-id="2d024-183">Enquanto pausado em uma linha de código, use o painel de **pilha de chamadas** para ver a pilha de chamadas que você recebeu para este ponto.</span><span class="sxs-lookup"><span data-stu-id="2d024-183">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="2d024-184">Clique em uma entrada para saltar para a linha de código em que essa função foi chamada.</span><span class="sxs-lookup"><span data-stu-id="2d024-184">Click on an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="2d024-185">O ícone de seta azul representa qual função DevTools está realçando no momento.</span><span class="sxs-lookup"><span data-stu-id="2d024-185">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

> ##### <span data-ttu-id="2d024-186">Figura 10</span><span class="sxs-lookup"><span data-stu-id="2d024-186">Figure 10</span></span>  
> <span data-ttu-id="2d024-187">O painel **pilha de chamadas**</span><span class="sxs-lookup"><span data-stu-id="2d024-187">The **Call Stack** pane</span></span>  
> ![O painel pilha de chamadas][ImageCallStackPane]  

> [!NOTE]
> <span data-ttu-id="2d024-189">Quando não pausa em uma linha de código, o painel **pilha de chamadas** está vazio.</span><span class="sxs-lookup"><span data-stu-id="2d024-189">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <span data-ttu-id="2d024-190">Copiar rastreamento de pilha</span><span class="sxs-lookup"><span data-stu-id="2d024-190">Copy stack trace</span></span>   

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="2d024-191">Clique com o botão direito do mouse em qualquer lugar no painel de **pilha de chamadas** e selecione **copiar rastreamento de pilha** para copiar a pilha de chamadas atual para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="2d024-191">Right-click anywhere in the **Call Stack** pane and select **Copy stack trace** to copy the current call stack to the clipboard.</span></span>  

> ##### <span data-ttu-id="2d024-192">Figura 11</span><span class="sxs-lookup"><span data-stu-id="2d024-192">Figure 11</span></span>  
> <span data-ttu-id="2d024-193">Selecionar o **rastreamento de pilha de cópia**</span><span class="sxs-lookup"><span data-stu-id="2d024-193">Selecting **Copy Stack Trace**</span></span>  
> ![Selecionar o rastreamento de pilha de cópia][ImageSelectingCopyStackTrace]  

<span data-ttu-id="2d024-195">Veja a seguir um exemplo da saída:</span><span class="sxs-lookup"><span data-stu-id="2d024-195">Below is an example of the output:</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## <span data-ttu-id="2d024-196">Ignorar um script ou um padrão de scripts</span><span class="sxs-lookup"><span data-stu-id="2d024-196">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="2d024-197">Marque um script como código da biblioteca quando quiser ignorar esse script durante a depuração.</span><span class="sxs-lookup"><span data-stu-id="2d024-197">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="2d024-198">Quando marcado como código de biblioteca, um script fica obscurecido no painel de **pilha de chamadas** , e você nunca percorre as funções do script quando percorre o código.</span><span class="sxs-lookup"><span data-stu-id="2d024-198">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="2d024-199">Por exemplo, suponha que você esteja passando por esse código:</span><span class="sxs-lookup"><span data-stu-id="2d024-199">For example, suppose you are stepping through this code:</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` <span data-ttu-id="2d024-200">é uma biblioteca de terceiros em que você confia.</span><span class="sxs-lookup"><span data-stu-id="2d024-200">is a third-party library that you trust.</span></span>  <span data-ttu-id="2d024-201">Se você tiver certeza de que o problema que está depurando não está relacionado à biblioteca de terceiros, faça sentido marcar o script como código de **biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="2d024-201">If you are confident that the problem you are debugging is not related to the third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

### <span data-ttu-id="2d024-202">Marcar um script como código da biblioteca no painel do editor</span><span class="sxs-lookup"><span data-stu-id="2d024-202">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="2d024-203">Para marcar um script como **código de biblioteca** no painel do **Editor** :</span><span class="sxs-lookup"><span data-stu-id="2d024-203">To mark a script as **Library code** from the **Editor** pane:</span></span>  

1.  <span data-ttu-id="2d024-204">Abra o arquivo.</span><span class="sxs-lookup"><span data-stu-id="2d024-204">Open the file.</span></span>  
1.  <span data-ttu-id="2d024-205">Clique com o botão direito do mouse em qualquer lugar.</span><span class="sxs-lookup"><span data-stu-id="2d024-205">Right-click anywhere.</span></span>  
1.  <span data-ttu-id="2d024-206">Selecione **Marcar como código da biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="2d024-206">Select **Mark as Library code**.</span></span>  

> ##### <span data-ttu-id="2d024-207">Figura 12</span><span class="sxs-lookup"><span data-stu-id="2d024-207">Figure 12</span></span>  
> <span data-ttu-id="2d024-208">Marcando um script como **código de biblioteca** no painel do **Editor**</span><span class="sxs-lookup"><span data-stu-id="2d024-208">Marking a script as **Library code** from the **Editor** pane</span></span>  
> ![Marcando um script como código de biblioteca no painel do editor][ImageMarkEditorPane]  

### <span data-ttu-id="2d024-210">Marcar um script como código da biblioteca no painel pilha de chamadas</span><span class="sxs-lookup"><span data-stu-id="2d024-210">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="2d024-211">Para marcar um script como **código de biblioteca** no painel **pilha de chamadas** :</span><span class="sxs-lookup"><span data-stu-id="2d024-211">To mark a script as **Library code** from the **Call Stack** pane:</span></span>  

1.  <span data-ttu-id="2d024-212">Clique com o botão direito do mouse em uma função do script.</span><span class="sxs-lookup"><span data-stu-id="2d024-212">Right-click on a function from the script.</span></span>  
1.  <span data-ttu-id="2d024-213">Selecione **Marcar como código da biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="2d024-213">Select **Mark as Library code**.</span></span>  

> ##### <span data-ttu-id="2d024-214">Figura 13</span><span class="sxs-lookup"><span data-stu-id="2d024-214">Figure 13</span></span>  
> <span data-ttu-id="2d024-215">Marcando um script como **código da biblioteca** no painel pilha de **chamadas**</span><span class="sxs-lookup"><span data-stu-id="2d024-215">Marking a script as **Library code** from the **Call Stack** pane</span></span>  
> ![Marcando um script como código da biblioteca no painel pilha de chamadas][ImageMarkCallStackPane]  

### <span data-ttu-id="2d024-217">Marcar um script como código de biblioteca em configurações</span><span class="sxs-lookup"><span data-stu-id="2d024-217">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="2d024-218">Para marcar um único script ou um padrão de scripts em configurações:</span><span class="sxs-lookup"><span data-stu-id="2d024-218">To mark a single script or pattern of scripts from Settings:</span></span>  

1.  <span data-ttu-id="2d024-219">Abrir [as configurações][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="2d024-219">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="2d024-220">Vá para a guia **código da biblioteca** .</span><span class="sxs-lookup"><span data-stu-id="2d024-220">Go to the **Library code** tab.</span></span>  
1.  <span data-ttu-id="2d024-221">Clique em **Adicionar padrão**.</span><span class="sxs-lookup"><span data-stu-id="2d024-221">Click **Add pattern**.</span></span>  
1.  <span data-ttu-id="2d024-222">Digite o nome do script ou um padrão de Regex de nomes de script para marcar como **código de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="2d024-222">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="2d024-223">Clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="2d024-223">Click **Add**.</span></span>  

> ##### <span data-ttu-id="2d024-224">Figura 14</span><span class="sxs-lookup"><span data-stu-id="2d024-224">Figure 14</span></span>  
> <span data-ttu-id="2d024-225">Marcando um script como **código de biblioteca** em configurações</span><span class="sxs-lookup"><span data-stu-id="2d024-225">Marking a script as **Library code** from Settings</span></span>  
> ![Marcando um script como código de biblioteca em configurações][ImageMarkScriptSettings]  

## <span data-ttu-id="2d024-227">Executar trechos de código de depuração de qualquer página</span><span class="sxs-lookup"><span data-stu-id="2d024-227">Run snippets of debug code from any page</span></span>   

<span data-ttu-id="2d024-228">Se você estiver executando o mesmo código de depuração no console repetidamente, considere os trechos de código.</span><span class="sxs-lookup"><span data-stu-id="2d024-228">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="2d024-229">Trechos de código são scripts de tempo de execução que você cria, armazena e executa dentro do DevTools.</span><span class="sxs-lookup"><span data-stu-id="2d024-229">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="2d024-230">Consulte [executar trechos de código em qualquer página][DevToolsJavascriptSnippets] para saber mais.</span><span class="sxs-lookup"><span data-stu-id="2d024-230">See [Run Snippets of Code From Any Page][DevToolsJavascriptSnippets] to learn more.</span></span>  

## <span data-ttu-id="2d024-231">Assista aos valores de expressões JavaScript personalizadas</span><span class="sxs-lookup"><span data-stu-id="2d024-231">Watch the values of custom JavaScript expressions</span></span>   

<span data-ttu-id="2d024-232">Use o painel de **inspeção** para ver os valores de expressões personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2d024-232">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="2d024-233">Você pode assistir a uma expressão JavaScript válida.</span><span class="sxs-lookup"><span data-stu-id="2d024-233">You may watch any valid JavaScript expression.</span></span>  

> ##### <span data-ttu-id="2d024-234">Figura 15</span><span class="sxs-lookup"><span data-stu-id="2d024-234">Figure 15</span></span>  
> <span data-ttu-id="2d024-235">O painel de **inspeção**</span><span class="sxs-lookup"><span data-stu-id="2d024-235">The **Watch** pane</span></span>  
> ![O painel de inspeção][ImageWatchPane]  

*   <span data-ttu-id="2d024-237">Clique no ícone **Adicionar expressão** ![ Adicionar expressão ][ImageAddExpressionIcon] para criar uma nova expressão de inspeção.</span><span class="sxs-lookup"><span data-stu-id="2d024-237">Click on the **Add Expression** ![Add Expression][ImageAddExpressionIcon] icon to create a new watch expression.</span></span>  
*   <span data-ttu-id="2d024-238">Clique no ícone **Atualizar** ![ atualização ][ImageRefreshIcon] para atualizar os valores de todas as expressões existentes.</span><span class="sxs-lookup"><span data-stu-id="2d024-238">Click on the **Refresh** ![Refresh][ImageRefreshIcon] icon to refresh the values of all existing expressions.</span></span>  <span data-ttu-id="2d024-239">Valores são atualizados automaticamente durante a depuração do código.</span><span class="sxs-lookup"><span data-stu-id="2d024-239">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="2d024-240">Passe o mouse sobre uma expressão e clique no ícone **excluir** expressão de ![ exclusão de expressão ][ImageDeleteExpressionIcon] para excluí-la.</span><span class="sxs-lookup"><span data-stu-id="2d024-240">Hover over an expression and click on the **Delete Expression** ![Delete Expression][ImageDeleteExpressionIcon] icon to delete it.</span></span>  

## <span data-ttu-id="2d024-241">Torne um arquivo do minified legível</span><span class="sxs-lookup"><span data-stu-id="2d024-241">Make a minified file readable</span></span>   

<span data-ttu-id="2d024-242">Clique no ícone formato de **formato** ![ ][ImageFormatIcon] para fazer com que um arquivo do minified seja legível pelo homem.</span><span class="sxs-lookup"><span data-stu-id="2d024-242">Click on the **Format** ![Format][ImageFormatIcon] icon to make a minified file human-readable.</span></span>  

> ##### <span data-ttu-id="2d024-243">Figura 16</span><span class="sxs-lookup"><span data-stu-id="2d024-243">Figure 16</span></span>  
> <span data-ttu-id="2d024-244">O botão **Formatar**</span><span class="sxs-lookup"><span data-stu-id="2d024-244">The **Format** button</span></span>  
> ![O botão Formatar][ImageFormat]  

## <span data-ttu-id="2d024-246">Editar um script</span><span class="sxs-lookup"><span data-stu-id="2d024-246">Edit a script</span></span>   

<span data-ttu-id="2d024-247">Ao corrigir um bug, você muitas vezes deseja testar algumas alterações no código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2d024-247">When fixing a bug, you often want to test out some changes to your JavaScript code.</span></span>  <span data-ttu-id="2d024-248">Você não precisa fazer as alterações em um editor externo ou IDE e, em seguida, recarregar a página.</span><span class="sxs-lookup"><span data-stu-id="2d024-248">You do not need to make the changes in an external editor or IDE and then reload the page.</span></span>  <span data-ttu-id="2d024-249">Você pode editar o script no DevTools.</span><span class="sxs-lookup"><span data-stu-id="2d024-249">You may edit your script in DevTools.</span></span>  

<span data-ttu-id="2d024-250">Para editar um script:</span><span class="sxs-lookup"><span data-stu-id="2d024-250">To edit a script:</span></span>  

1.  <span data-ttu-id="2d024-251">Abra o arquivo no painel **Editor** do painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="2d024-251">Open the file in the **Editor** pane of the **Sources** panel.</span></span>  
1.  <span data-ttu-id="2d024-252">Faça suas alterações no painel do **Editor** .</span><span class="sxs-lookup"><span data-stu-id="2d024-252">Make your changes in the **Editor** pane.</span></span>  
1.  <span data-ttu-id="2d024-253">Pressione `Ctrl` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) para salvar.</span><span class="sxs-lookup"><span data-stu-id="2d024-253">Press `Ctrl`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="2d024-254">O DevTools patches de todo o arquivo JS para o mecanismo JavaScript do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2d024-254">DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.</span></span>  

> ##### <span data-ttu-id="2d024-255">Figura 17</span><span class="sxs-lookup"><span data-stu-id="2d024-255">Figure 17</span></span>  
> <span data-ttu-id="2d024-256">Painel do **Editor**</span><span class="sxs-lookup"><span data-stu-id="2d024-256">The **Editor** pane</span></span>  
> ![Painel do editor][ImageEditorPane]  

## <span data-ttu-id="2d024-258">Desabilitar JavaScript</span><span class="sxs-lookup"><span data-stu-id="2d024-258">Disable JavaScript</span></span>   

<span data-ttu-id="2d024-259">Consulte [desabilitar JavaScript com o Microsoft Edge devtools][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="2d024-259">See [Disable JavaScript With Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageStepOverIcon]: /microsoft-edge/devtools-guide-chromium/media/step-over-icon.msft.png  
[ImageStepIntoIcon]: /microsoft-edge/devtools-guide-chromium/media/step-into-icon.msft.png  
[ImageStepOutIcon]: /microsoft-edge/devtools-guide-chromium/media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: /microsoft-edge/devtools-guide-chromium/media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/add-expression-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-expression-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  

[ImageSelectingStepOver]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-over-next-function-call.msft.png "Figura 1: selecionando a etapa sobre"  
[ImageSelectingStepInto]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-into-next-function-call.msft.png "Figura 2: selecionando Step in"  
[ImageSelectingStepOut]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-out-of-current-function.msft.png "Figura 3: selecionando o Step Out"  
[ImageSelectingContinueToHere]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-continue-to-here.msft.png "Figura 4: selecionar continuar até aqui"  
[ImageSelectingRestartFrame]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-restart-frame.msft.png "Figura 5: selecionando reiniciar quadro"  
[ImageSelectingResumeScriptExecution]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-resume-script-runtime.msft.png "Figura 6: selecionando retomar execução do script"  
[ImageSelectingForceScriptExecution]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-force-script-runtime.msft.png "Figura 7: seleção forçar execução de script"  
[ImageThreadsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-main-min-js-threads.msft.png "Figura 8: o painel threads"  
[ImageScopePane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-scope.msft.png "Figura 9: o painel escopo"  
[ImageCallStackPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png "Figura 10: o painel de pilha de chamadas"  
[ImageSelectingCopyStackTrace]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png "Figura 11: selecionando o rastreamento de pilha de cópia"  
[ImageMarkEditorPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png "Figura 12: marcando um script como código da biblioteca no painel do editor"  
[ImageMarkCallStackPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png "Figura 13: marcando um script como código de biblioteca a partir do painel de pilha de chamadas"  
[ImageMarkScriptSettings]: /microsoft-edge/devtools-guide-chromium/media/javascript-framework-library-code.msft.png "Figura 14: marcando um script como código de biblioteca de configurações"  
[ImageWatchPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-watch.msft.png "Figura 15: o painel de inspeção"  
[ImageFormat]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-html-non-minified.msft.png "Figura 16: o botão Formatar"  
[ImageEditorPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-html-minified.msft.png "Figura 17: painel do editor"  

<!-- links -->  

[DevToolsJavascriptDisable]: disable.md "Desabilitar JavaScript com o Microsoft Edge DevTools"  
[DevToolsJavascriptGetStarted]: index.md "Introdução à depuração de JavaScript no Microsoft Edge DevTools"  
[DevToolsJavascriptSnippets]: snippets.md "Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools"  

[DevToolsCustomize]: ../customize/index.md "Personalizar o Microsoft Edge DevTools"  

> [!NOTE]
> <span data-ttu-id="2d024-281">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="2d024-281">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2d024-282">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="2d024-282">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2d024-284">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2d024-284">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
