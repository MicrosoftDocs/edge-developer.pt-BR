---
description: Descubra novos fluxos de trabalho de depuração nesta referência abrangente dos recursos de depuração do Microsoft Edge DevTools.
title: Usar os recursos de depurador
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 6fb90a70e0aac9f556fa9f5f02afee1fd5b4962e
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519601"
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

# <a name="use-the-debugger-features"></a><span data-ttu-id="684c9-104">Usar os recursos de depurador</span><span class="sxs-lookup"><span data-stu-id="684c9-104">Use the debugger features</span></span>

<span data-ttu-id="684c9-105">Este artigo aborda como usar o depurador no Microsoft Edge DevTools, incluindo como definir um ponto de interrupção de linha de código.</span><span class="sxs-lookup"><span data-stu-id="684c9-105">This article covers how to use the debugger in Microsoft Edge DevTools, including how to set a line-of-code breakpoint.</span></span>  <span data-ttu-id="684c9-106">Para definir outros tipos de pontos de interrupção, consulte [Pause your code with breakpoints][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="684c9-106">To set other types of breakpoints, see [Pause your code with breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

<span data-ttu-id="684c9-107">Para saber as noções básicas de depuração, navegue até Introdução à depuração do JavaScript no [Microsoft Edge DevTools,][DevToolsJavascriptGetStarted]que é um tutorial que usa uma página da Web baseada em formulário existente.</span><span class="sxs-lookup"><span data-stu-id="684c9-107">To learn the basics of debugging, navigate to [Get started with debugging JavaScript in Microsoft Edge DevTools][DevToolsJavascriptGetStarted], which is a tutorial that uses an existing, form-based webpage.</span></span>  <span data-ttu-id="684c9-108">O tutorial tem capturas de tela, para que você possa skim-lo.</span><span class="sxs-lookup"><span data-stu-id="684c9-108">The tutorial has screen captures, so you can skim it.</span></span>  <span data-ttu-id="684c9-109">Você pode experimentar facilmente os recursos de depurador usando a página da Web de demonstração.</span><span class="sxs-lookup"><span data-stu-id="684c9-109">You can easily try out the debugger features by using the demo webpage.</span></span>

## <a name="view-and-edit-javascript-code"></a><span data-ttu-id="684c9-110">Exibir e editar código JavaScript</span><span class="sxs-lookup"><span data-stu-id="684c9-110">View and edit JavaScript code</span></span>

<span data-ttu-id="684c9-111">Ao corrigir um bug, muitas vezes você deseja experimentar algumas alterações no código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="684c9-111">When fixing a bug, you often want to try out some changes to your JavaScript code.</span></span>  <span data-ttu-id="684c9-112">Não é necessário fazer as alterações em um editor externo ou no IDE, carregar o arquivo no servidor e atualizar a página. em vez disso, para testar alterações, você pode editar seu código JavaScript diretamente no DevTools e ver o resultado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="684c9-112">You don't need to make the changes in an external editor or IDE, re-upload the file to the server, and then refresh the page; instead, to test changes, you can edit your JavaScript code directly in DevTools and see the result immediately.</span></span>  

<span data-ttu-id="684c9-113">Para exibir e editar um arquivo JavaScript:</span><span class="sxs-lookup"><span data-stu-id="684c9-113">To view and edit a JavaScript file:</span></span>  

1.  <span data-ttu-id="684c9-114">Navegue até a **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="684c9-114">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="684c9-115">No painel **Navegador,** selecione seu arquivo, para abri-lo no **painel Editor.**</span><span class="sxs-lookup"><span data-stu-id="684c9-115">In the **Navigator** pane, select your file, to open it in the **Editor** pane.</span></span>
1.  <span data-ttu-id="684c9-116">No painel **Editor,** edite seu arquivo.</span><span class="sxs-lookup"><span data-stu-id="684c9-116">In the **Editor** pane, edit your file.</span></span>  
1.  <span data-ttu-id="684c9-117">Selecione `Ctrl` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\) para salvar.</span><span class="sxs-lookup"><span data-stu-id="684c9-117">Select `Ctrl`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="684c9-118">Em seguida, o DevTools carrega o arquivo JavaScript no mecanismo JavaScript do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="684c9-118">DevTools then loads the JavaScript file into the JavaScript engine of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="O painel Editor" lightbox="../media/javascript-sources-html-minified.msft.png":::
       <span data-ttu-id="684c9-120">O **painel Editor**</span><span class="sxs-lookup"><span data-stu-id="684c9-120">The **Editor** pane</span></span>  
    :::image-end:::  
     
## <a name="reformat-a-minified-javascript-file-with-pretty-print"></a><span data-ttu-id="684c9-121">Reformata um arquivo JavaScript minificado com impressão bastante impressa</span><span class="sxs-lookup"><span data-stu-id="684c9-121">Reformat a minified JavaScript file with pretty-print</span></span>

<span data-ttu-id="684c9-122">Para tornar um arquivo minificado acessível, escolha o botão **Formatar** \( Formatar \) na parte inferior ![ do painel ](../media/format-icon.msft.png) **Editor.**</span><span class="sxs-lookup"><span data-stu-id="684c9-122">To make a minified file human-readable, choose the **Format** \(![Format](../media/format-icon.msft.png)\) button at the bottom of the **Editor** pane.</span></span>

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="O botão Formatar" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   <span data-ttu-id="684c9-124">O **botão Formatar**</span><span class="sxs-lookup"><span data-stu-id="684c9-124">The **Format** button</span></span>  
:::image-end:::  

## <a name="set-a-breakpoint-to-pause-code"></a><span data-ttu-id="684c9-125">Definir um ponto de interrupção, para pausar código</span><span class="sxs-lookup"><span data-stu-id="684c9-125">Set a breakpoint, to pause code</span></span>

<span data-ttu-id="684c9-126">Para pausar seu código no meio do tempo de execução, de definir um ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="684c9-126">To pause your code in the middle of the runtime, set a breakpoint.</span></span>  <span data-ttu-id="684c9-127">O tipo de ponto de interrupção mais básico e conhecido é um ponto de interrupção de linha de código.</span><span class="sxs-lookup"><span data-stu-id="684c9-127">The most basic and well-known type of breakpoint is a line-of-code breakpoint.</span></span>

<span data-ttu-id="684c9-128">Use um ponto de interrupção de linha de código quando você conhecer a região exata do código que precisa investigar.</span><span class="sxs-lookup"><span data-stu-id="684c9-128">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="684c9-129">O DevTools sempre pausa na linha de código especificada, antes de ser executado.</span><span class="sxs-lookup"><span data-stu-id="684c9-129">DevTools always pauses at the specified line of code, before running it.</span></span>

<span data-ttu-id="684c9-130">Para definir um ponto de interrupção de linha de código:</span><span class="sxs-lookup"><span data-stu-id="684c9-130">To set a line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="684c9-131">Navegue até a **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="684c9-131">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="684c9-132">Abra o arquivo que contém a linha de código.</span><span class="sxs-lookup"><span data-stu-id="684c9-132">Open the file that contains the line of code.</span></span>  
1.  <span data-ttu-id="684c9-133">Selecione a área à esquerda do número de linha para a linha de código.</span><span class="sxs-lookup"><span data-stu-id="684c9-133">Select the area to the left of the line number for the line of code.</span></span>  <span data-ttu-id="684c9-134">Ou clique com o botão direito do mouse no número da linha e escolha **Adicionar ponto de interrupção**.</span><span class="sxs-lookup"><span data-stu-id="684c9-134">Or, right-click the line number and then choose **Add breakpoint**.</span></span>  <span data-ttu-id="684c9-135">Em seguida, um círculo vermelho aparece ao lado do número da linha, indicando um ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="684c9-135">A red circle then appears next to the line number, indicating a breakpoint.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Um ponto de interrupção de linha de código" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="684c9-137">Um ponto de interrupção de linha de código</span><span class="sxs-lookup"><span data-stu-id="684c9-137">A line-of-code breakpoint</span></span>  
    :::image-end:::  

<span data-ttu-id="684c9-138">Os pontos de interrupção de linha de código podem ser ineficientes para definir, especialmente se você não sabe exatamente onde procurar ou se sua base de código é grande.</span><span class="sxs-lookup"><span data-stu-id="684c9-138">Line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if your codebase is large.</span></span>  <span data-ttu-id="684c9-139">Para economizar tempo durante a depuração, saiba como e quando usar os outros tipos de pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="684c9-139">To save time when debugging, learn how and when to use the other types of breakpoints.</span></span>  <span data-ttu-id="684c9-140">Para obter mais informações, navegue até [Pause your code with breakpoints][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="684c9-140">For more information, navigate to [Pause your code with breakpoints][DevToolsJavascriptBreakpoints].</span></span>

## <a name="step-through-code"></a><span data-ttu-id="684c9-141">Passo a passo código</span><span class="sxs-lookup"><span data-stu-id="684c9-141">Step through code</span></span>  

<span data-ttu-id="684c9-142">Depois que seu código é pausado em um ponto de interrupção, passo pelo código, uma linha por vez, investigando o fluxo de controle e os valores de propriedade ao longo do caminho.</span><span class="sxs-lookup"><span data-stu-id="684c9-142">After your code is paused at a breakpoint, step through the code, one line at a time, investigating control flow and property values along the way.</span></span>  

### <a name="step-over-line-of-code"></a><span data-ttu-id="684c9-143">Passo a passo sobre a linha de código</span><span class="sxs-lookup"><span data-stu-id="684c9-143">Step over line of code</span></span>  

<span data-ttu-id="684c9-144">Quando pausado em uma linha de código que contém uma função que não é relevante para o problema que você está depurando, escolha o botão **Passo** a passo \( Passo a passo \) para executar a função sem entrar ![ ](../media/step-over-icon.msft.png) nele.</span><span class="sxs-lookup"><span data-stu-id="684c9-144">When paused on a line of code containing a function that isn't relevant to the problem you are debugging, choose the **Step over** \(![Step over](../media/step-over-icon.msft.png)\) button to run the function without stepping into it.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Escolha Passo a passo" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   <span data-ttu-id="684c9-146">Escolha **Passo a passo**</span><span class="sxs-lookup"><span data-stu-id="684c9-146">Choose **Step over**</span></span>  
:::image-end:::  

<span data-ttu-id="684c9-147">Por exemplo, suponha que você está depurando o seguinte trecho de código.</span><span class="sxs-lookup"><span data-stu-id="684c9-147">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="684c9-148">Você está pausado em `A` .</span><span class="sxs-lookup"><span data-stu-id="684c9-148">You are paused on `A`.</span></span>  <span data-ttu-id="684c9-149">Depois de escolher **Passo a Passo,** o DevTools executa todo o código na função que você está passando, que é `B` e `C` .</span><span class="sxs-lookup"><span data-stu-id="684c9-149">After you choose **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="684c9-150">Em seguida, o DevTools pausa `D` em .</span><span class="sxs-lookup"><span data-stu-id="684c9-150">DevTools then pauses on `D`.</span></span>  

### <a name="step-into-line-of-code"></a><span data-ttu-id="684c9-151">Entrar na linha de código</span><span class="sxs-lookup"><span data-stu-id="684c9-151">Step into line of code</span></span>  

<span data-ttu-id="684c9-152">Quando pausado em uma linha de código que contém uma chamada de função relacionada ao problema que você está depurando, escolha o botão **Entrar** em \( Entrar em \) para investigar ainda mais essa ![ ](../media/step-into-icon.msft.png) função.</span><span class="sxs-lookup"><span data-stu-id="684c9-152">When paused on a line of code containing a function call that is related to the problem you are debugging, choose the **Step into** \(![Step into](../media/step-into-icon.msft.png)\) button to investigate that function further.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Escolha Entrar" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   <span data-ttu-id="684c9-154">Escolha **Entrar**</span><span class="sxs-lookup"><span data-stu-id="684c9-154">Choose **Step into**</span></span>  
:::image-end:::  

<span data-ttu-id="684c9-155">Por exemplo, suponha que você está depurando o seguinte trecho de código.</span><span class="sxs-lookup"><span data-stu-id="684c9-155">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="684c9-156">Você está pausado em `A` .</span><span class="sxs-lookup"><span data-stu-id="684c9-156">You are paused on `A`.</span></span>  <span data-ttu-id="684c9-157">Depois de escolher **Entrar,** o DevTools executa essa linha de código e pausa em `B` .</span><span class="sxs-lookup"><span data-stu-id="684c9-157">After you choose **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <a name="step-out-of-line-of-code"></a><span data-ttu-id="684c9-158">Sair da linha de código</span><span class="sxs-lookup"><span data-stu-id="684c9-158">Step out of line of code</span></span>  

<span data-ttu-id="684c9-159">Quando pausado dentro de uma função que não está relacionada ao problema que você está depurando, escolha o botão **Sair** \( Sair \) para executar o restante do código da ![ ](../media/step-out-icon.msft.png) função.</span><span class="sxs-lookup"><span data-stu-id="684c9-159">When paused inside of a function that isn't related to the problem you are debugging, choose the **Step out** \(![Step out](../media/step-out-icon.msft.png)\) button to run the rest of the code of the function.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Escolha Sair" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   <span data-ttu-id="684c9-161">Escolha **Sair**</span><span class="sxs-lookup"><span data-stu-id="684c9-161">Choose **Step out**</span></span>  
:::image-end:::  

<span data-ttu-id="684c9-162">Por exemplo, suponha que você está depurando o seguinte trecho de código.</span><span class="sxs-lookup"><span data-stu-id="684c9-162">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="684c9-163">Você está pausado em `A` .</span><span class="sxs-lookup"><span data-stu-id="684c9-163">You are paused on `A`.</span></span>  <span data-ttu-id="684c9-164">Depois de escolher **Sair,** o DevTools executa o restante do código em , que está apenas neste exemplo e, em `getName()` `B` seguida, pausa em `C` .</span><span class="sxs-lookup"><span data-stu-id="684c9-164">After you choose **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <a name="run-all-code-up-to-a-specific-line"></a><span data-ttu-id="684c9-165">Executar todo o código até uma linha específica</span><span class="sxs-lookup"><span data-stu-id="684c9-165">Run all code up to a specific line</span></span>  

<span data-ttu-id="684c9-166">Ao depurar uma função longa, pode haver muito código que não está relacionado ao problema que você está depurando.</span><span class="sxs-lookup"><span data-stu-id="684c9-166">When debugging a long function, there may be a lot of code that isn't related to the problem you are debugging.</span></span>  

<span data-ttu-id="684c9-167">Você pode optar por passar por todas as linhas, mas isso é entediante.</span><span class="sxs-lookup"><span data-stu-id="684c9-167">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="684c9-168">Você pode optar por definir um ponto de interrupção de linha de código na linha na qual você está interessado e, em seguida, escolher o botão Retomar execução de **script** \( Retomar execução de script \) mas há uma maneira mais ![ ](../media/resume-script-run-icon.msft.png) rápida.</span><span class="sxs-lookup"><span data-stu-id="684c9-168">You may choose to set a line-of-code breakpoint on the line in which you are interested and then choose the **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\) button, but there is a faster way.</span></span>  

<span data-ttu-id="684c9-169">Passe o mouse na linha de código na qual você está **interessado,** abra o menu contextual \(clique com o botão direito do mouse\) e escolha Continuar até aqui .</span><span class="sxs-lookup"><span data-stu-id="684c9-169">Hover on the line of code in which you are interested, open the contextual menu \(right-click\), and choose **Continue to here**.</span></span>  <span data-ttu-id="684c9-170">O DevTools executa todo o código até esse ponto e pausa nessa linha.</span><span class="sxs-lookup"><span data-stu-id="684c9-170">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Escolha Continuar até aqui" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   <span data-ttu-id="684c9-172">Escolha **Continuar até aqui**</span><span class="sxs-lookup"><span data-stu-id="684c9-172">Choose **Continue to here**</span></span>  
:::image-end:::  

### <a name="restart-the-top-function-of-the-call-stack"></a><span data-ttu-id="684c9-173">Reinicie a função superior da pilha de chamada</span><span class="sxs-lookup"><span data-stu-id="684c9-173">Restart the top function of the call stack</span></span>  

<span data-ttu-id="684c9-174">Para pausar na primeira linha da função superior na pilha de chamada, enquanto pausada em uma linha de código, passe o mouse em qualquer lugar no painel **Pilha** de Chamada, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Reiniciar**quadro .</span><span class="sxs-lookup"><span data-stu-id="684c9-174">To pause on the first line of the top function in your call stack, while paused on a line of code, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Restart frame**.</span></span>  <span data-ttu-id="684c9-175">A função superior é a última função que foi executado.</span><span class="sxs-lookup"><span data-stu-id="684c9-175">The top function is the last function that was run.</span></span>  

<span data-ttu-id="684c9-176">O trecho de código a seguir é um exemplo para você fazer o passo a passo.</span><span class="sxs-lookup"><span data-stu-id="684c9-176">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="684c9-177">Você está pausado em `A` .</span><span class="sxs-lookup"><span data-stu-id="684c9-177">You are paused on `A`.</span></span>  <span data-ttu-id="684c9-178">Depois de **escolher Reiniciar quadro**, você deve ser pausado em , sem nunca definir um ponto de interrupção ou escolher Retomar execução de `B` **script**.</span><span class="sxs-lookup"><span data-stu-id="684c9-178">After choosing **Restart frame**, you should be paused on `B`, without ever setting a breakpoint or choosing **Resume script execution**.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Escolha Reiniciar quadro" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   <span data-ttu-id="684c9-180">Escolha **Reiniciar quadro**</span><span class="sxs-lookup"><span data-stu-id="684c9-180">Choose **Restart frame**</span></span>  
:::image-end:::  

### <a name="resume-script-runtime"></a><span data-ttu-id="684c9-181">Retomar o tempo de execução do script</span><span class="sxs-lookup"><span data-stu-id="684c9-181">Resume script runtime</span></span>  

<span data-ttu-id="684c9-182">Para continuar o tempo de execução após uma pausa do script, escolha o botão Retomar execução de **script** \( ![ Retomar execução de script ](../media/resume-script-run-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="684c9-182">To continue the runtime after a pause of your script, choose the **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\) button.</span></span>  <span data-ttu-id="684c9-183">O DevTools executa o script até o próximo ponto de interrupção, se for o caso.</span><span class="sxs-lookup"><span data-stu-id="684c9-183">DevTools runs the script up until the next breakpoint, if any.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Escolha Retomar execução de script" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   <span data-ttu-id="684c9-185">Escolha **Retomar execução de script**</span><span class="sxs-lookup"><span data-stu-id="684c9-185">Choose **Resume script execution**</span></span>  
:::image-end:::  

#### <a name="force-script-runtime"></a><span data-ttu-id="684c9-186">Forçar o tempo de execução do script</span><span class="sxs-lookup"><span data-stu-id="684c9-186">Force script runtime</span></span>  

<span data-ttu-id="684c9-187">Para ignorar todos os pontos de interrupção e forçar seu script a continuar a ser executado, escolha e segure o botão Retomar execução de script **\(** Retomar execução de script \) e escolha o botão Forçar execução de script \( Forçar execução ![ de script ](../media/resume-script-run-icon.msft.png) \*\*\*\* ![ ](../media/force-script-run-icon.msft.png) \) .</span><span class="sxs-lookup"><span data-stu-id="684c9-187">To ignore all breakpoints and force your script to continue to run, choose and hold the **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\) button and then choose the **Force script execution** \(![Force script execution](../media/force-script-run-icon.msft.png)\) button.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Escolha Forçar execução de script" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   <span data-ttu-id="684c9-189">Escolha **Forçar execução de script**</span><span class="sxs-lookup"><span data-stu-id="684c9-189">Choose **Force script execution**</span></span>  
:::image-end:::  

### <a name="change-thread-context"></a><span data-ttu-id="684c9-190">Alterar contexto de thread</span><span class="sxs-lookup"><span data-stu-id="684c9-190">Change thread context</span></span>  

<span data-ttu-id="684c9-191">Ao trabalhar com funcionários da Web ou funcionários de serviços, escolha um contexto listado no **painel Threads** para alternar para esse contexto.</span><span class="sxs-lookup"><span data-stu-id="684c9-191">When working with web workers or service workers, choose on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="684c9-192">O ícone de seta azul representa qual contexto está selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="684c9-192">The blue arrow icon represents which context is currently selected.</span></span>  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="O painel Threads" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   <span data-ttu-id="684c9-194">O **painel Threads**</span><span class="sxs-lookup"><span data-stu-id="684c9-194">The **Threads** pane</span></span>  
:::image-end:::  

<span data-ttu-id="684c9-195">Por exemplo, suponha que você tenha pausado em um ponto de interrupção no script principal e no script de trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="684c9-195">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="684c9-196">Você deseja exibir as propriedades locais e globais para o contexto de trabalho do serviço, mas a ferramenta **Sources** está mostrando o contexto de script principal.</span><span class="sxs-lookup"><span data-stu-id="684c9-196">You want to view the local and global properties for the service worker context, but the **Sources** tool is showing the main script context.</span></span>  <span data-ttu-id="684c9-197">Para alternar para o contexto de trabalho do serviço, no **painel Threads,** escolha a entrada do trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="684c9-197">To switch to the service worker context, in the **Threads** pane, choose the service worker entry.</span></span>  

## <a name="view-and-edit-properties-and-variables"></a><span data-ttu-id="684c9-198">Exibir e editar propriedades e variáveis</span><span class="sxs-lookup"><span data-stu-id="684c9-198">View and edit properties and variables</span></span>

<span data-ttu-id="684c9-199">Enquanto estiver pausado em uma linha de código, use o painel **Escopo** para exibir e editar os valores de propriedades e variáveis nos escopos local, fechamento e global.</span><span class="sxs-lookup"><span data-stu-id="684c9-199">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="684c9-200">Clique duas vezes em um valor de propriedade para alterá-lo.</span><span class="sxs-lookup"><span data-stu-id="684c9-200">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="684c9-201">Propriedades não enumeradas estão acinzenadas.</span><span class="sxs-lookup"><span data-stu-id="684c9-201">Non-enumerable properties are greyed out.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="O painel Escopo" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   <span data-ttu-id="684c9-203">O **painel Escopo**</span><span class="sxs-lookup"><span data-stu-id="684c9-203">The **Scope** pane</span></span>  
:::image-end:::  

## <a name="watch-the-values-of-javascript-expressions"></a><span data-ttu-id="684c9-204">Assista aos valores das expressões JavaScript</span><span class="sxs-lookup"><span data-stu-id="684c9-204">Watch the values of JavaScript expressions</span></span>  

<span data-ttu-id="684c9-205">Use o **painel** de relógio para observar os valores de expressões personalizadas.</span><span class="sxs-lookup"><span data-stu-id="684c9-205">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="684c9-206">Você pode assistir a qualquer expressão JavaScript válida.</span><span class="sxs-lookup"><span data-stu-id="684c9-206">You can watch any valid JavaScript expression.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="O painel de relógio" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   <span data-ttu-id="684c9-208">O **painel** de relógio</span><span class="sxs-lookup"><span data-stu-id="684c9-208">The **Watch** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="684c9-209">Para criar uma nova expressão de relógio, selecione o botão **Adicionar expressão de relógio** \( Adicionar expressão de relógio ![ ](../media/add-expression-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="684c9-209">To create a new watch expression, select the **Add watch expression** \(![Add watch expression](../media/add-expression-icon.msft.png)\) button.</span></span>  
*   <span data-ttu-id="684c9-210">Para atualizar os valores de todas as expressões existentes, selecione o botão **Atualizar** \( ![ Atualizar ](../media/refresh-icon.msft.png) \)</span><span class="sxs-lookup"><span data-stu-id="684c9-210">To refresh the values of all existing expressions, select the **Refresh** \(![Refresh](../media/refresh-icon.msft.png)\) button.</span></span>  <span data-ttu-id="684c9-211">Os valores são atualizados automaticamente ao passar pelo código.</span><span class="sxs-lookup"><span data-stu-id="684c9-211">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="684c9-212">Para excluir uma expressão de relógio, clique com o botão direito do mouse na expressão e selecione Excluir expressão de **relógio** \( ![ Excluir expressão de relógio ](../media/delete-expression-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="684c9-212">To delete a watch expression, right-click the expression and then select **Delete watch expression** \(![Delete watch expression](../media/delete-expression-icon.msft.png)\).</span></span>  

## <a name="view-the-call-stack"></a><span data-ttu-id="684c9-213">Exibir a pilha de chamada</span><span class="sxs-lookup"><span data-stu-id="684c9-213">View the call stack</span></span>  

<span data-ttu-id="684c9-214">Enquanto estiver pausado em uma linha de código, use o painel **Pilha** de Chamada para exibir a pilha de chamada que o fez chegar a esse ponto.</span><span class="sxs-lookup"><span data-stu-id="684c9-214">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="684c9-215">Escolha uma entrada para ir para a linha de código onde essa função foi chamada.</span><span class="sxs-lookup"><span data-stu-id="684c9-215">Choose an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="684c9-216">O ícone de seta azul representa qual função DevTools está realçando no momento.</span><span class="sxs-lookup"><span data-stu-id="684c9-216">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="O painel Pilha de Chamada" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   <span data-ttu-id="684c9-218">O **painel Pilha de** Chamada</span><span class="sxs-lookup"><span data-stu-id="684c9-218">The **Call Stack** pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="684c9-219">Quando não pausado em uma linha de código, o painel **Pilha de** Chamada fica vazio.</span><span class="sxs-lookup"><span data-stu-id="684c9-219">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <a name="copy-stack-trace"></a><span data-ttu-id="684c9-220">Copiar rastreamento de pilha</span><span class="sxs-lookup"><span data-stu-id="684c9-220">Copy stack trace</span></span>  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="684c9-221">Para copiar a pilha de chamada atual para \*\*\*\* a área de transferência, passe o mouse em qualquer lugar no painel Pilha de Chamada, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Copiar rastreamento **de**pilha .</span><span class="sxs-lookup"><span data-stu-id="684c9-221">To copy the current call stack to the clipboard, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Copy stack trace**.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Escolha Copiar Rastreamento de Pilha" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   <span data-ttu-id="684c9-223">Escolha **Copiar Rastreamento de Pilha**</span><span class="sxs-lookup"><span data-stu-id="684c9-223">Choose **Copy Stack Trace**</span></span>  
:::image-end:::  

<span data-ttu-id="684c9-224">O trecho de código a seguir é um exemplo da saída.</span><span class="sxs-lookup"><span data-stu-id="684c9-224">The following code snippet is an example of the output.</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onChoose (get-started.js:15)
```  

## <a name="ignore-a-script-or-pattern-of-scripts"></a><span data-ttu-id="684c9-225">Ignorar um script ou um padrão de scripts</span><span class="sxs-lookup"><span data-stu-id="684c9-225">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="684c9-226">Marque um script como código de biblioteca quando quiser ignorar esse script durante a depuração.</span><span class="sxs-lookup"><span data-stu-id="684c9-226">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="684c9-227">Quando marcado como código biblioteca, um \*\*\*\* script é obscurecido no painel Pilha de Chamada e você nunca entra nas funções do script quando passa pelo código.</span><span class="sxs-lookup"><span data-stu-id="684c9-227">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="684c9-228">Por exemplo, no trecho de código a seguir, a linha `A` usa , que é uma biblioteca de `lib` terceiros.</span><span class="sxs-lookup"><span data-stu-id="684c9-228">For example, in the following code snippet, line `A` uses `lib`, which is a third-party library.</span></span>  <span data-ttu-id="684c9-229">Se você estiver confiante de que o problema que você está depurando não está relacionado a essa biblioteca de terceiros, então faz sentido marcar o script como código **biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="684c9-229">If you are confident that the problem you are debugging is not related to that third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

### <a name="mark-a-script-as-library-code-from-the-editor-pane"></a><span data-ttu-id="684c9-230">Marcar um script como código biblioteca do painel Editor</span><span class="sxs-lookup"><span data-stu-id="684c9-230">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="684c9-231">Para marcar um script como **código biblioteca** do **painel Editor:**</span><span class="sxs-lookup"><span data-stu-id="684c9-231">To mark a script as **Library code** from the **Editor** pane:</span></span>  

1.  <span data-ttu-id="684c9-232">Abra o arquivo.</span><span class="sxs-lookup"><span data-stu-id="684c9-232">Open the file.</span></span>  
1.  <span data-ttu-id="684c9-233">Passe o mouse em qualquer lugar e abra o menu contextual \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="684c9-233">Hover anywhere and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="684c9-234">Escolha **Adicionar script para ignorar lista** (anteriormente mostrado como Marca como código da **biblioteca**).</span><span class="sxs-lookup"><span data-stu-id="684c9-234">Choose **Add script to ignore list** (previously shown as **Mark as Library code**).</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Marcar um script como código biblioteca do painel Editor" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       <span data-ttu-id="684c9-236">Marcar um script como **código biblioteca** do **painel Editor**</span><span class="sxs-lookup"><span data-stu-id="684c9-236">Mark a script as **Library code** from the **Editor** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-the-call-stack-pane"></a><span data-ttu-id="684c9-237">Marcar um script como código biblioteca do painel Pilha de Chamada</span><span class="sxs-lookup"><span data-stu-id="684c9-237">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="684c9-238">Para marcar um script como **código biblioteca do** painel Pilha **de** Chamada:</span><span class="sxs-lookup"><span data-stu-id="684c9-238">To mark a script as **Library code** from the **Call Stack** pane:</span></span>  

1.  <span data-ttu-id="684c9-239">Passe o mouse em uma função do script e abra o menu contextual \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="684c9-239">Hover on a function from the script and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="684c9-240">Escolha **Adicionar script para ignorar lista** (anteriormente mostrado como Marca como código da **biblioteca**).</span><span class="sxs-lookup"><span data-stu-id="684c9-240">Choose **Add script to ignore list** (previously shown as **Mark as Library code**).</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Marcar um script como código biblioteca do painel Pilha de Chamada" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       <span data-ttu-id="684c9-242">Marcar um script como **código biblioteca do** painel Pilha **de** Chamada</span><span class="sxs-lookup"><span data-stu-id="684c9-242">Mark a script as **Library code** from the **Call Stack** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-settings"></a><span data-ttu-id="684c9-243">Marcar um script como código de biblioteca a partir de Configurações</span><span class="sxs-lookup"><span data-stu-id="684c9-243">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="684c9-244">Para marcar um único script ou padrão de scripts de **Configurações**:</span><span class="sxs-lookup"><span data-stu-id="684c9-244">To mark a single script or pattern of scripts from **Settings**:</span></span>  

1.  <span data-ttu-id="684c9-245">Configurações [abertas][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="684c9-245">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="684c9-246">Navegue até **a configuração de código biblioteca.**</span><span class="sxs-lookup"><span data-stu-id="684c9-246">Navigate to the **Library code** setting.</span></span>  
1.  <span data-ttu-id="684c9-247">Escolha **Adicionar padrão**.</span><span class="sxs-lookup"><span data-stu-id="684c9-247">Choose **Add pattern**.</span></span>  
1.  <span data-ttu-id="684c9-248">Insira o nome do script ou um padrão regex de nomes de script para marcar como **código biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="684c9-248">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="684c9-249">Escolha **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="684c9-249">Choose **Add**.</span></span>  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Marcar um script como código de biblioteca a partir de Configurações" lightbox="../media/javascript-framework-library-code.msft.png":::
       <span data-ttu-id="684c9-251">Marcar um script como **código de biblioteca** a partir de **Configurações**</span><span class="sxs-lookup"><span data-stu-id="684c9-251">Mark a script as **Library code** from **Settings**</span></span>  
    :::image-end:::  
    
## <a name="run-snippets-of-debug-code-from-any-page"></a><span data-ttu-id="684c9-252">Executar trechos de código de depuração de qualquer página</span><span class="sxs-lookup"><span data-stu-id="684c9-252">Run snippets of debug code from any page</span></span>  

<span data-ttu-id="684c9-253">Se você estiver executando o mesmo código de depuração no Console uma e outra vez, considere Trechos.</span><span class="sxs-lookup"><span data-stu-id="684c9-253">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="684c9-254">Trechos de código são scripts de tempo de execução que você pode escrever, armazenar e executar no DevTools.</span><span class="sxs-lookup"><span data-stu-id="684c9-254">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="684c9-255">Consulte [Executar trechos de código javascript em qualquer página da Web][DevToolsJavascriptSnippets].</span><span class="sxs-lookup"><span data-stu-id="684c9-255">See [Run snippets of JavaScript on any webpage][DevToolsJavascriptSnippets].</span></span>  

## <a name="see-also"></a><span data-ttu-id="684c9-256">Ver também</span><span class="sxs-lookup"><span data-stu-id="684c9-256">See also</span></span>  

*   <span data-ttu-id="684c9-257">[Introdução à depuração de JavaScript no Microsoft Edge DevTools][DevToolsJavascriptGetStarted] - Um tutorial simples e curto usando código existente, com capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="684c9-257">[Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted] - A simple, short tutorial using existing code, with screen captures.</span></span>
*   <span data-ttu-id="684c9-258">[Visão geral da][DevToolsSourcesIndex] ferramenta Sources - A **ferramenta Sources** inclui o depurador e editor javaScript.</span><span class="sxs-lookup"><span data-stu-id="684c9-258">[Sources tool overview][DevToolsSourcesIndex] - The **Sources** tool includes the JavaScript debugger and editor.</span></span>
*   <span data-ttu-id="684c9-259">[Desabilitar JavaScript com o Microsoft Edge DevTools][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="684c9-259">[Disable JavaScript with Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="684c9-260">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="684c9-260">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Como pausar seu código com pontos de interrupção no Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptDisable]: ./disable.md "Desabilitar JavaScript com o Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptGetStarted]: ./index.md "Começar a depurar JavaScript no Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptSnippets]: ./snippets.md "Execute trechos de código do JavaScript em qualquer página com o Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsSourcesIndex]: ../sources/index.md "Visão geral da ferramenta Sources | Microsoft Docs"  
[DevToolsCustomize]: ../customize/index.md "Personalizar o Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="684c9-267">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="684c9-267">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="684c9-268">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="684c9-268">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="684c9-270">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="684c9-270">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
