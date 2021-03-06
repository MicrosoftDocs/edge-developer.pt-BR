---
description: Descubra novos fluxos de trabalho de depuração nesta referência abrangente dos recursos de depuração do Microsoft Edge DevTools.
title: Referências de depuração de JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 09a2d61269b2fe3a23a57ce58eb1c89b12a7639c
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398473"
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

# <a name="javascript-debugging-reference"></a><span data-ttu-id="25649-104">Referências de depuração de JavaScript</span><span class="sxs-lookup"><span data-stu-id="25649-104">JavaScript debugging reference</span></span>  

<span data-ttu-id="25649-105">Descubra novos fluxos de trabalho de depuração com a seguinte referência abrangente dos recursos de depuração do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="25649-105">Discover new debugging workflows with the following comprehensive reference of Microsoft Edge DevTools debugging features.</span></span>  

<span data-ttu-id="25649-106">Para saber as noções básicas de depuração, navegue até Começar a [depurar JavaScript no Microsoft Edge DevTools][DevToolsJavascriptGetStarted].</span><span class="sxs-lookup"><span data-stu-id="25649-106">To learn the basics of debugging, navigate to [Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted].</span></span>  

## <a name="pause-code-with-breakpoints"></a><span data-ttu-id="25649-107">Pausar código com pontos de interrupção</span><span class="sxs-lookup"><span data-stu-id="25649-107">Pause code with breakpoints</span></span>  

<span data-ttu-id="25649-108">De definir um ponto de interrupção para que você possa pausar seu código no meio do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="25649-108">Set a breakpoint so that you are able to pause your code in the middle of the runtime.</span></span>  

<span data-ttu-id="25649-109">Para saber como definir pontos de interrupção, navegue até [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="25649-109">To learn how to set breakpoints, navigate to [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <a name="step-through-code"></a><span data-ttu-id="25649-110">Passo a passo código</span><span class="sxs-lookup"><span data-stu-id="25649-110">Step through code</span></span>  

<span data-ttu-id="25649-111">Depois que seu código for pausado, passo a passo por ele, uma linha por vez, investigando o fluxo de controle e os valores de propriedade ao longo do caminho.</span><span class="sxs-lookup"><span data-stu-id="25649-111">Once your code is paused, step through it, one line at a time, investigating control flow and property values along the way.</span></span>  

### <a name="step-over-line-of-code"></a><span data-ttu-id="25649-112">Passo a passo sobre a linha de código</span><span class="sxs-lookup"><span data-stu-id="25649-112">Step over line of code</span></span>  

<span data-ttu-id="25649-113">Quando pausado em uma linha de código que contém uma função que não é relevante para o problema que você está depurando, escolha o botão **Passo** a passo \( Passo a passo \) para executar a função sem entrar ![ ][ImageStepOverIcon] nele.</span><span class="sxs-lookup"><span data-stu-id="25649-113">When paused on a line of code containing a function that is not relevant to the problem you are debugging, choose the **Step over** \(![Step over][ImageStepOverIcon]\) button to run the function without stepping into it.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Escolha Passo a passo" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   <span data-ttu-id="25649-115">Escolha **Passo a passo**</span><span class="sxs-lookup"><span data-stu-id="25649-115">Choose **Step over**</span></span>  
:::image-end:::  

<span data-ttu-id="25649-116">Por exemplo, suponha que você está depurando o seguinte trecho de código.</span><span class="sxs-lookup"><span data-stu-id="25649-116">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="25649-117">Você está pausado em `A` .</span><span class="sxs-lookup"><span data-stu-id="25649-117">You are paused on `A`.</span></span>  <span data-ttu-id="25649-118">Depois de escolher **Passo a Passo,** o DevTools executa todo o código na função que você está passando, que é `B` e `C` .</span><span class="sxs-lookup"><span data-stu-id="25649-118">After you choose **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="25649-119">Em seguida, o DevTools pausa `D` em .</span><span class="sxs-lookup"><span data-stu-id="25649-119">DevTools then pauses on `D`.</span></span>  

### <a name="step-into-line-of-code"></a><span data-ttu-id="25649-120">Entrar na linha de código</span><span class="sxs-lookup"><span data-stu-id="25649-120">Step into line of code</span></span>  

<span data-ttu-id="25649-121">Quando pausado em uma linha de código que contém uma chamada de função relacionada ao problema que você está depurando, escolha o botão **Entrar** em \( Entrar em \) para investigar ainda mais essa ![ ][ImageStepIntoIcon] função.</span><span class="sxs-lookup"><span data-stu-id="25649-121">When paused on a line of code containing a function call that is related to the problem you are debugging, choose the **Step into** \(![Step into][ImageStepIntoIcon]\) button to investigate that function further.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Escolha Entrar" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   <span data-ttu-id="25649-123">Escolha **Entrar**</span><span class="sxs-lookup"><span data-stu-id="25649-123">Choose **Step into**</span></span>  
:::image-end:::  

<span data-ttu-id="25649-124">Por exemplo, suponha que você está depurando o seguinte trecho de código.</span><span class="sxs-lookup"><span data-stu-id="25649-124">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="25649-125">Você está pausado em `A` .</span><span class="sxs-lookup"><span data-stu-id="25649-125">You are paused on `A`.</span></span>  <span data-ttu-id="25649-126">Depois de escolher **Entrar,** o DevTools executa essa linha de código e pausa em `B` .</span><span class="sxs-lookup"><span data-stu-id="25649-126">After you choose **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <a name="step-out-of-line-of-code"></a><span data-ttu-id="25649-127">Sair da linha de código</span><span class="sxs-lookup"><span data-stu-id="25649-127">Step out of line of code</span></span>  

<span data-ttu-id="25649-128">Quando pausado dentro de uma função que não está relacionada ao problema que você está depurando, escolha o botão **Sair** \( Sair \) para executar o restante do código da ![ ][ImageStepOutIcon] função.</span><span class="sxs-lookup"><span data-stu-id="25649-128">When paused inside of a function that is not related to the problem you are debugging, choose the **Step out** \(![Step out][ImageStepOutIcon]\) button to run the rest of the code of the function.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Escolha Sair" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   <span data-ttu-id="25649-130">Escolha **Sair**</span><span class="sxs-lookup"><span data-stu-id="25649-130">Choose **Step out**</span></span>  
:::image-end:::  

<span data-ttu-id="25649-131">Por exemplo, suponha que você está depurando o seguinte trecho de código.</span><span class="sxs-lookup"><span data-stu-id="25649-131">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="25649-132">Você está pausado em `A` .</span><span class="sxs-lookup"><span data-stu-id="25649-132">You are paused on `A`.</span></span>  <span data-ttu-id="25649-133">Depois de escolher **Sair,** o DevTools executa o restante do código em , que está apenas neste exemplo e, em `getName()` `B` seguida, pausa em `C` .</span><span class="sxs-lookup"><span data-stu-id="25649-133">After you choose **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <a name="run-all-code-up-to-a-specific-line"></a><span data-ttu-id="25649-134">Executar todo o código até uma linha específica</span><span class="sxs-lookup"><span data-stu-id="25649-134">Run all code up to a specific line</span></span>  

<span data-ttu-id="25649-135">Ao depurar uma função longa, pode haver muito código que não está relacionado ao problema que você está depurando.</span><span class="sxs-lookup"><span data-stu-id="25649-135">When debugging a long function, there may be a lot of code that is not related to the problem you are debugging.</span></span>  

<span data-ttu-id="25649-136">Você pode optar por passar por todas as linhas, mas isso é entediante.</span><span class="sxs-lookup"><span data-stu-id="25649-136">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="25649-137">Você pode optar por definir um ponto de interrupção de linha de código na linha na qual você está interessado e, em seguida, escolher o botão Retomar Execução de **Script** \( Retomar Execução de Script \) mas há uma maneira mais ![ ][ImageResumeScriptExecutionIcon] rápida.</span><span class="sxs-lookup"><span data-stu-id="25649-137">You may choose to set a line-of-code breakpoint on the line in which you are interested and then choose the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button, but there is a faster way.</span></span>  

<span data-ttu-id="25649-138">Passe o mouse na linha de código na qual você está **interessado,** abra o menu contextual \(clique com o botão direito do mouse\) e escolha Continuar até aqui .</span><span class="sxs-lookup"><span data-stu-id="25649-138">Hover on the line of code in which you are interested, open the contextual menu \(right-click\), and choose **Continue to here**.</span></span>  <span data-ttu-id="25649-139">O DevTools executa todo o código até esse ponto e pausa nessa linha.</span><span class="sxs-lookup"><span data-stu-id="25649-139">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Escolha Continuar até aqui" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   <span data-ttu-id="25649-141">Escolha **Continuar até aqui**</span><span class="sxs-lookup"><span data-stu-id="25649-141">Choose **Continue to here**</span></span>  
:::image-end:::  

### <a name="restart-the-top-function-of-the-call-stack"></a><span data-ttu-id="25649-142">Reinicie a função superior da pilha de chamada</span><span class="sxs-lookup"><span data-stu-id="25649-142">Restart the top function of the call stack</span></span>  

<span data-ttu-id="25649-143">Para pausar na primeira linha da função superior na pilha de chamada, enquanto estiver pausado em uma linha de código, passe o mouse em qualquer lugar no painel **Pilha** de Chamada, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Reiniciar Quadro**.</span><span class="sxs-lookup"><span data-stu-id="25649-143">To pause on the first line of the top function in your call stack, while paused on a line of code, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Restart Frame**.</span></span>  <span data-ttu-id="25649-144">A função superior é a última função que foi executado.</span><span class="sxs-lookup"><span data-stu-id="25649-144">The top function is the last function that was run.</span></span>  

<span data-ttu-id="25649-145">O trecho de código a seguir é um exemplo para você fazer o passo a passo.</span><span class="sxs-lookup"><span data-stu-id="25649-145">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="25649-146">Você está pausado em `A` .</span><span class="sxs-lookup"><span data-stu-id="25649-146">You are paused on `A`.</span></span>  <span data-ttu-id="25649-147">Depois de **escolher Reiniciar Quadro**, você deve ser pausado em , sem nunca definir um ponto de interrupção ou escolher Retomar execução de `B` **script**.</span><span class="sxs-lookup"><span data-stu-id="25649-147">After choosing **Restart Frame**, you should be paused on `B`, without ever setting a breakpoint or choosing **Resume script execution**.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Escolha Reiniciar Quadro" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   <span data-ttu-id="25649-149">Escolha **Reiniciar Quadro**</span><span class="sxs-lookup"><span data-stu-id="25649-149">Choose **Restart Frame**</span></span>  
:::image-end:::  

### <a name="resume-script-runtime"></a><span data-ttu-id="25649-150">Retomar o tempo de execução do script</span><span class="sxs-lookup"><span data-stu-id="25649-150">Resume script runtime</span></span>  

<span data-ttu-id="25649-151">Para continuar o tempo de execução após uma pausa do seu script, escolha o botão Retomar Execução de **Script** \( ![ Retomar Execução de Script ][ImageResumeScriptExecutionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="25649-151">To continue the runtime after a pause of your script, choose the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button.</span></span>  <span data-ttu-id="25649-152">O DevTools executa o script até o próximo ponto de interrupção, se for o caso.</span><span class="sxs-lookup"><span data-stu-id="25649-152">DevTools runs the script up until the next breakpoint, if any.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Escolha Retomar execução de script" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   <span data-ttu-id="25649-154">Escolha **Retomar execução de script**</span><span class="sxs-lookup"><span data-stu-id="25649-154">Choose **Resume script execution**</span></span>  
:::image-end:::  

#### <a name="force-script-runtime"></a><span data-ttu-id="25649-155">Forçar o tempo de execução do script</span><span class="sxs-lookup"><span data-stu-id="25649-155">Force script runtime</span></span>  

<span data-ttu-id="25649-156">Para ignorar todos os pontos de interrupção e forçar seu script a continuar em execução, escolha e segure o botão Retomar Execução de Script **\(** Retomar Execução de Script \) e escolha o botão Forçar execução de script \( Forçar execução ![ de script ][ImageResumeScriptExecutionIcon] \*\*\*\* ![ ][ImageForceScriptExecutionIcon] \) .</span><span class="sxs-lookup"><span data-stu-id="25649-156">To ignore all breakpoints and force your script to resume running, choose and hold the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button and then choose the **Force script execution** \(![Force script execution][ImageForceScriptExecutionIcon]\) button.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Escolha Forçar execução de script" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   <span data-ttu-id="25649-158">Escolha **Forçar execução de script**</span><span class="sxs-lookup"><span data-stu-id="25649-158">Choose **Force script execution**</span></span>  
:::image-end:::  

### <a name="change-thread-context"></a><span data-ttu-id="25649-159">Alterar contexto de thread</span><span class="sxs-lookup"><span data-stu-id="25649-159">Change thread context</span></span>  

<span data-ttu-id="25649-160">Ao trabalhar com funcionários da Web ou funcionários de serviços, escolha um contexto listado no **painel Threads** para alternar para esse contexto.</span><span class="sxs-lookup"><span data-stu-id="25649-160">When working with web workers or service workers, choose on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="25649-161">O ícone de seta azul representa qual contexto está selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="25649-161">The blue arrow icon represents which context is currently selected.</span></span>  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="O painel Threads" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   <span data-ttu-id="25649-163">O **painel Threads**</span><span class="sxs-lookup"><span data-stu-id="25649-163">The **Threads** pane</span></span>  
:::image-end:::  

<span data-ttu-id="25649-164">Por exemplo, suponha que você tenha pausado em um ponto de interrupção no script principal e no script de trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="25649-164">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="25649-165">Você deseja exibir as propriedades locais e globais para o contexto de trabalho do serviço, mas o painel **Fontes** está mostrando o contexto principal do script.</span><span class="sxs-lookup"><span data-stu-id="25649-165">You want to view the local and global properties for the service worker context, but the **Sources** panel is showing the main script context.</span></span>  <span data-ttu-id="25649-166">Ao escolher a entrada do trabalhador do serviço no **painel Threads,** você deve ser capaz de alternar para esse contexto.</span><span class="sxs-lookup"><span data-stu-id="25649-166">By choosing on the service worker entry in the **Threads** pane, you should be able to switch to that context.</span></span>  

## <a name="view-and-edit-local-closure-and-global-properties"></a><span data-ttu-id="25649-167">Exibir e editar propriedades locais, de fechamento e globais</span><span class="sxs-lookup"><span data-stu-id="25649-167">View and edit local, closure, and global properties</span></span>  

<span data-ttu-id="25649-168">Enquanto estiver pausado em uma linha de código, use o painel **Escopo** para exibir e editar os valores de propriedades e variáveis nos escopos local, fechamento e global.</span><span class="sxs-lookup"><span data-stu-id="25649-168">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="25649-169">Clique duas vezes em um valor de propriedade para alterá-lo.</span><span class="sxs-lookup"><span data-stu-id="25649-169">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="25649-170">Propriedades não enumeradas estão acinzenadas.</span><span class="sxs-lookup"><span data-stu-id="25649-170">Non-enumerable properties are greyed out.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="O painel Escopo" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   <span data-ttu-id="25649-172">O **painel Escopo**</span><span class="sxs-lookup"><span data-stu-id="25649-172">The **Scope** pane</span></span>  
:::image-end:::  

## <a name="view-the-current-call-stack"></a><span data-ttu-id="25649-173">Exibir a pilha de chamada atual</span><span class="sxs-lookup"><span data-stu-id="25649-173">View the current call stack</span></span>  

<span data-ttu-id="25649-174">Enquanto estiver pausado em uma linha de código, use o painel **Pilha** de Chamada para exibir a pilha de chamada que o fez chegar a esse ponto.</span><span class="sxs-lookup"><span data-stu-id="25649-174">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="25649-175">Escolha uma entrada para ir para a linha de código onde essa função foi chamada.</span><span class="sxs-lookup"><span data-stu-id="25649-175">Choose an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="25649-176">O ícone de seta azul representa qual função DevTools está realçando no momento.</span><span class="sxs-lookup"><span data-stu-id="25649-176">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="O painel Pilha de Chamada" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   <span data-ttu-id="25649-178">O **painel Pilha de** Chamada</span><span class="sxs-lookup"><span data-stu-id="25649-178">The **Call Stack** pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="25649-179">Quando não pausado em uma linha de código, o painel **Pilha de** Chamada fica vazio.</span><span class="sxs-lookup"><span data-stu-id="25649-179">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <a name="copy-stack-trace"></a><span data-ttu-id="25649-180">Copiar rastreamento de pilha</span><span class="sxs-lookup"><span data-stu-id="25649-180">Copy stack trace</span></span>  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="25649-181">para copiar a pilha de chamada atual para \*\*\*\* a área de transferência, passe o mouse em qualquer lugar no painel Pilha de Chamada, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Copiar rastreamento **de**pilha .</span><span class="sxs-lookup"><span data-stu-id="25649-181">to copy the current call stack to the clipboard, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Copy stack trace**.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Escolha Copiar Rastreamento de Pilha" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   <span data-ttu-id="25649-183">Escolha **Copiar Rastreamento de Pilha**</span><span class="sxs-lookup"><span data-stu-id="25649-183">Choose **Copy Stack Trace**</span></span>  
:::image-end:::  

<span data-ttu-id="25649-184">O trecho de código a seguir é um exemplo da saída.</span><span class="sxs-lookup"><span data-stu-id="25649-184">The following code snippet is an example of the output.</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onChoose (get-started.js:15)
```  

## <a name="ignore-a-script-or-pattern-of-scripts"></a><span data-ttu-id="25649-185">Ignorar um script ou um padrão de scripts</span><span class="sxs-lookup"><span data-stu-id="25649-185">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="25649-186">Marque um script como código de biblioteca quando quiser ignorar esse script durante a depuração.</span><span class="sxs-lookup"><span data-stu-id="25649-186">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="25649-187">Quando marcado como código biblioteca, um \*\*\*\* script é obscurecido no painel Pilha de Chamada e você nunca entra nas funções do script quando passa pelo código.</span><span class="sxs-lookup"><span data-stu-id="25649-187">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="25649-188">O trecho de código a seguir é um exemplo para você fazer o passo a passo.</span><span class="sxs-lookup"><span data-stu-id="25649-188">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` <span data-ttu-id="25649-189">é uma biblioteca de terceiros em que você confia.</span><span class="sxs-lookup"><span data-stu-id="25649-189">is a third-party library that you trust.</span></span>  <span data-ttu-id="25649-190">Se você estiver confiante de que o problema que você está depurando não está relacionado à biblioteca de terceiros, então faz sentido marcar o script como código **biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="25649-190">If you are confident that the problem you are debugging is not related to the third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

### <a name="mark-a-script-as-library-code-from-the-editor-pane"></a><span data-ttu-id="25649-191">Marcar um script como código biblioteca do painel Editor</span><span class="sxs-lookup"><span data-stu-id="25649-191">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="25649-192">Conclua as seguintes ações para marcar um script como **código biblioteca** no **painel Editor.**</span><span class="sxs-lookup"><span data-stu-id="25649-192">Complete the following actions to mark a script as **Library code** from the **Editor** pane.</span></span>  

1.  <span data-ttu-id="25649-193">Abra o arquivo.</span><span class="sxs-lookup"><span data-stu-id="25649-193">Open the file.</span></span>  
1.  <span data-ttu-id="25649-194">Passe o mouse em qualquer lugar e abra o menu contextual \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="25649-194">Hover anywhere and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="25649-195">Escolha **Marcar como código da biblioteca.**</span><span class="sxs-lookup"><span data-stu-id="25649-195">Choose **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Marcar um script como código biblioteca do painel Editor" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       <span data-ttu-id="25649-197">Marcar um script como **código biblioteca** do **painel Editor**</span><span class="sxs-lookup"><span data-stu-id="25649-197">Mark a script as **Library code** from the **Editor** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-the-call-stack-pane"></a><span data-ttu-id="25649-198">Marcar um script como código biblioteca do painel Pilha de Chamada</span><span class="sxs-lookup"><span data-stu-id="25649-198">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="25649-199">Conclua as seguintes ações para marcar um script como **código biblioteca** do painel **Pilha de** Chamada.</span><span class="sxs-lookup"><span data-stu-id="25649-199">Complete the following actions to mark a script as **Library code** from the **Call Stack** pane.</span></span>  

1.  <span data-ttu-id="25649-200">Passe o mouse em uma função do script e abra o menu contextual \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="25649-200">Hover on a function from the script and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="25649-201">Escolha **Marcar como código da biblioteca.**</span><span class="sxs-lookup"><span data-stu-id="25649-201">Choose **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Marcar um script como código biblioteca do painel Pilha de Chamada" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       <span data-ttu-id="25649-203">Marcar um script como **código biblioteca do** painel Pilha **de** Chamada</span><span class="sxs-lookup"><span data-stu-id="25649-203">Mark a script as **Library code** from the **Call Stack** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-settings"></a><span data-ttu-id="25649-204">Marcar um script como código de biblioteca a partir de Configurações</span><span class="sxs-lookup"><span data-stu-id="25649-204">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="25649-205">Conclua as seguintes ações para marcar um único script ou padrão de scripts de **Configurações**.</span><span class="sxs-lookup"><span data-stu-id="25649-205">Complete the following actions to mark a single script or pattern of scripts from **Settings**.</span></span>  

1.  <span data-ttu-id="25649-206">Configurações [abertas][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="25649-206">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="25649-207">Navegue até **a configuração de código biblioteca.**</span><span class="sxs-lookup"><span data-stu-id="25649-207">Navigate to the **Library code** setting.</span></span>  
1.  <span data-ttu-id="25649-208">Escolha **Adicionar padrão**.</span><span class="sxs-lookup"><span data-stu-id="25649-208">Choose **Add pattern**.</span></span>  
1.  <span data-ttu-id="25649-209">Insira o nome do script ou um padrão regex de nomes de script para marcar como **código biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="25649-209">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="25649-210">Escolha **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="25649-210">Choose **Add**.</span></span>  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Marcar um script como código de biblioteca a partir de Configurações" lightbox="../media/javascript-framework-library-code.msft.png":::
       <span data-ttu-id="25649-212">Marcar um script como **código de biblioteca** a partir de **Configurações**</span><span class="sxs-lookup"><span data-stu-id="25649-212">Mark a script as **Library code** from **Settings**</span></span>  
    :::image-end:::  
    
## <a name="run-snippets-of-debug-code-from-any-page"></a><span data-ttu-id="25649-213">Executar trechos de código de depuração de qualquer página</span><span class="sxs-lookup"><span data-stu-id="25649-213">Run snippets of debug code from any page</span></span>  

<span data-ttu-id="25649-214">Se você estiver executando o mesmo código de depuração no Console uma e outra vez, considere Trechos.</span><span class="sxs-lookup"><span data-stu-id="25649-214">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="25649-215">Trechos de código são scripts de tempo de execução que você pode escrever, armazenar e executar no DevTools.</span><span class="sxs-lookup"><span data-stu-id="25649-215">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="25649-216">Para saber mais, navegue [até Executar trechos de código em qualquer página.][DevToolsJavascriptSnippets]</span><span class="sxs-lookup"><span data-stu-id="25649-216">To learn more, navigate to [Run Snippets of Code From Any Page][DevToolsJavascriptSnippets].</span></span>  

## <a name="watch-the-values-of-custom-javascript-expressions"></a><span data-ttu-id="25649-217">Assista aos valores de expressões JavaScript personalizadas</span><span class="sxs-lookup"><span data-stu-id="25649-217">Watch the values of custom JavaScript expressions</span></span>  

<span data-ttu-id="25649-218">Use o **painel** de relógio para observar os valores de expressões personalizadas.</span><span class="sxs-lookup"><span data-stu-id="25649-218">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="25649-219">Você pode assistir a qualquer expressão JavaScript válida.</span><span class="sxs-lookup"><span data-stu-id="25649-219">You may watch any valid JavaScript expression.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="O painel de relógio" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   <span data-ttu-id="25649-221">O **painel** de relógio</span><span class="sxs-lookup"><span data-stu-id="25649-221">The **Watch** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="25649-222">Escolha o **botão Adicionar Expressão** \( Adicionar Expressão ![ ][ImageAddExpressionIcon] \) para criar uma nova expressão de relógio.</span><span class="sxs-lookup"><span data-stu-id="25649-222">Choose the **Add Expression** \(![Add Expression][ImageAddExpressionIcon]\) button to create a new watch expression.</span></span>  
*   <span data-ttu-id="25649-223">Escolha o **botão Atualizar** \( ![ Atualizar ][ImageRefreshIcon] \) para atualizar os valores de todas as expressões existentes.</span><span class="sxs-lookup"><span data-stu-id="25649-223">Choose the **Refresh** \(![Refresh][ImageRefreshIcon]\) button to refresh the values of all existing expressions.</span></span>  <span data-ttu-id="25649-224">Os valores são atualizados automaticamente ao passar pelo código.</span><span class="sxs-lookup"><span data-stu-id="25649-224">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="25649-225">Passe o mouse em uma expressão e escolha o botão **Excluir Expressão** \( Excluir ![ Expressão ][ImageDeleteExpressionIcon] \) para excluí-la.</span><span class="sxs-lookup"><span data-stu-id="25649-225">Hover on an expression and choose the **Delete Expression** \(![Delete Expression][ImageDeleteExpressionIcon]\) button to delete it.</span></span>  

## <a name="make-a-minified-file-readable"></a><span data-ttu-id="25649-226">Tornar um arquivo minificado acessível</span><span class="sxs-lookup"><span data-stu-id="25649-226">Make a minified file readable</span></span>  

<span data-ttu-id="25649-227">Escolha o **botão Formatar** \( ![ Formatar ][ImageFormatIcon] \) para tornar um arquivo minificado acessível.</span><span class="sxs-lookup"><span data-stu-id="25649-227">Choose the **Format** \(![Format][ImageFormatIcon]\) button to make a minified file human-readable.</span></span>  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="O botão Formatar" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   <span data-ttu-id="25649-229">O **botão Formatar**</span><span class="sxs-lookup"><span data-stu-id="25649-229">The **Format** button</span></span>  
:::image-end:::  

## <a name="edit-a-script"></a><span data-ttu-id="25649-230">Editar um script</span><span class="sxs-lookup"><span data-stu-id="25649-230">Edit a script</span></span>  

<span data-ttu-id="25649-231">Ao corrigir um bug, muitas vezes você deseja testar algumas alterações no código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="25649-231">When fixing a bug, you often want to test out some changes to your JavaScript code.</span></span>  <span data-ttu-id="25649-232">Você não precisa fazer as alterações em um editor externo ou IDE e atualizar a página.</span><span class="sxs-lookup"><span data-stu-id="25649-232">You do not need to make the changes in an external editor or IDE and then refresh the page.</span></span>  <span data-ttu-id="25649-233">Você pode editar seu script no DevTools.</span><span class="sxs-lookup"><span data-stu-id="25649-233">You may edit your script in DevTools.</span></span>  

<span data-ttu-id="25649-234">Conclua as seguintes ações para editar um script.</span><span class="sxs-lookup"><span data-stu-id="25649-234">Complete the following actions to edit a script.</span></span>  

1.  <span data-ttu-id="25649-235">Abra o arquivo no **painel Editor** do painel **Fontes.**</span><span class="sxs-lookup"><span data-stu-id="25649-235">Open the file in the **Editor** pane of the **Sources** panel.</span></span>  
1.  <span data-ttu-id="25649-236">Faça suas alterações no **painel Editor.**</span><span class="sxs-lookup"><span data-stu-id="25649-236">Make your changes in the **Editor** pane.</span></span>  
1.  <span data-ttu-id="25649-237">Selecione `Ctrl` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\) para salvar.</span><span class="sxs-lookup"><span data-stu-id="25649-237">Select `Ctrl`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="25649-238">O DevTools remenda todo o arquivo JS no mecanismo JavaScript do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="25649-238">DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="O painel Editor" lightbox="../media/javascript-sources-html-minified.msft.png":::
       <span data-ttu-id="25649-240">O **painel Editor**</span><span class="sxs-lookup"><span data-stu-id="25649-240">The **Editor** pane</span></span>  
    :::image-end:::  
     
## <a name="disable-javascript"></a><span data-ttu-id="25649-241">Desabilitar o JavaScript</span><span class="sxs-lookup"><span data-stu-id="25649-241">Disable JavaScript</span></span>  

<span data-ttu-id="25649-242">Navegue [até Desabilitar JavaScript com o Microsoft Edge DevTools][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="25649-242">Navigate to [Disable JavaScript with Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="25649-243">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="25649-243">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

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

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Como pausar seu código com pontos de interrupção no Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptDisable]: ./disable.md "Desabilitar JavaScript com o Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptGetStarted]: ./index.md "Começar a depurar JavaScript no Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptSnippets]: ./snippets.md "Execute trechos de código do JavaScript em qualquer página com o Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomize]: ../customize/index.md "Personalizar o Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="25649-249">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="25649-249">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="25649-250">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="25649-250">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="25649-252">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="25649-252">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
