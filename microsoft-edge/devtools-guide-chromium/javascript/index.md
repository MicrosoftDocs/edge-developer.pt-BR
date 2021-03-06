---
description: Saiba como usar o Microsoft Edge DevTools para encontrar e corrigir bugs javaScript.
title: Começar a depurar JavaScript no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: e146c6708f097b1ea8dc82f08be58f5aa5e52d1f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398438"
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
# <a name="get-started-with-debugging-javascript-in-microsoft-edge-devtools"></a><span data-ttu-id="b60c4-104">Começar a depurar JavaScript no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b60c4-104">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="b60c4-105">Este artigo ensina o fluxo de trabalho básico para depurar qualquer problema javascript no DevTools.</span><span class="sxs-lookup"><span data-stu-id="b60c4-105">This article teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <a name="step-1-reproduce-the-bug"></a><span data-ttu-id="b60c4-106">Etapa 1: Reproduzir o bug</span><span class="sxs-lookup"><span data-stu-id="b60c4-106">Step 1: Reproduce the bug</span></span>  

<span data-ttu-id="b60c4-107">Encontrar uma série de ações que reproduzam consistentemente um bug é sempre a primeira etapa para a depuração.</span><span class="sxs-lookup"><span data-stu-id="b60c4-107">Finding a series of actions that consistently reproduce a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="b60c4-108">Escolha **Abrir Demonstração**.</span><span class="sxs-lookup"><span data-stu-id="b60c4-108">Choose **Open Demo**.</span></span>  <span data-ttu-id="b60c4-109">Segure `Control` \(Windows, Linux\) `Command` ou \(macOS\) e abra a demonstração em uma nova guia do navegador.</span><span class="sxs-lookup"><span data-stu-id="b60c4-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and open the demo in a new browser tab.</span></span>  
    
    [<span data-ttu-id="b60c4-110">Abrir Demonstração</span><span class="sxs-lookup"><span data-stu-id="b60c4-110">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="b60c4-111">Insira `5` na caixa de texto Número **1.**</span><span class="sxs-lookup"><span data-stu-id="b60c4-111">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="b60c4-112">Insira `1` na caixa de texto Número **2.**</span><span class="sxs-lookup"><span data-stu-id="b60c4-112">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="b60c4-113">Escolha **Adicionar Número 1 e Número 2**.</span><span class="sxs-lookup"><span data-stu-id="b60c4-113">Choose **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="b60c4-114">O rótulo abaixo do botão diz `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="b60c4-114">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="b60c4-115">O resultado deve ser `6` .</span><span class="sxs-lookup"><span data-stu-id="b60c4-115">The result should be `6`.</span></span>  <span data-ttu-id="b60c4-116">Em seguida, corrige o erro de adição que é o bug.</span><span class="sxs-lookup"><span data-stu-id="b60c4-116">Next, fix the addition error that is the bug.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 resulta em 51, mas deve ser 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` <span data-ttu-id="b60c4-118">resulta `51` em , mas deve ser</span><span class="sxs-lookup"><span data-stu-id="b60c4-118">results in `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <a name="step-2-get-familiar-with-the-sources-tool-ui"></a><span data-ttu-id="b60c4-119">Etapa 2: Familiarizar-se com a interface do usuário da ferramenta Sources</span><span class="sxs-lookup"><span data-stu-id="b60c4-119">Step 2: Get familiar with the Sources tool UI</span></span>  

<span data-ttu-id="b60c4-120">O DevTools fornece muitas ferramentas diferentes para tarefas diferentes.</span><span class="sxs-lookup"><span data-stu-id="b60c4-120">DevTools provides many different tools for different tasks.</span></span>  <span data-ttu-id="b60c4-121">Tarefas diferentes incluem alterar CSS, perfil de desempenho de carga de página e monitoramento de solicitações de rede.</span><span class="sxs-lookup"><span data-stu-id="b60c4-121">Different tasks include changing CSS, profiling page-load performance, and monitoring network requests.</span></span>  <span data-ttu-id="b60c4-122">A **ferramenta Sources** é onde você depura JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b60c4-122">The **Sources** tool is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="b60c4-123">Para abrir a **ferramenta Console** no DevTools, selecione `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="b60c4-123">To open the **Console** tool in DevTools, select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="A ferramenta Console" lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="b60c4-125">A **ferramenta Console**</span><span class="sxs-lookup"><span data-stu-id="b60c4-125">The **Console** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b60c4-126">Escolha a **ferramenta Fontes.**</span><span class="sxs-lookup"><span data-stu-id="b60c4-126">Choose the **Sources** tool.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="A ferramenta Sources" lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="b60c4-128">A **ferramenta Sources**</span><span class="sxs-lookup"><span data-stu-id="b60c4-128">The **Sources** tool</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b60c4-129">A **interface do usuário** da ferramenta Sources tem três partes.</span><span class="sxs-lookup"><span data-stu-id="b60c4-129">The **Sources** tool UI has three parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="As 3 partes da interface do usuário da ferramenta Sources" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="b60c4-131">As 3 partes da interface do **usuário da ferramenta Sources**</span><span class="sxs-lookup"><span data-stu-id="b60c4-131">The 3 parts of the **Sources** tool UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="b60c4-132">O **painel Navegador** de Arquivos \(Seção 1 na figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="b60c4-132">The **File Navigator** panel \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="b60c4-133">Todos os arquivos que a página da Web solicita estão listados aqui.</span><span class="sxs-lookup"><span data-stu-id="b60c4-133">Every file that the webpage requests is listed here.</span></span>  
1.  <span data-ttu-id="b60c4-134">O **painel Editor de** Código \(Seção 2 na figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="b60c4-134">The **Code Editor** panel \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="b60c4-135">Depois de selecionar um arquivo no painel **Navegador** de Arquivos, o conteúdo desse arquivo será exibido aqui.</span><span class="sxs-lookup"><span data-stu-id="b60c4-135">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="b60c4-136">O **painel Depuração** de JavaScript \(Seção 3 na figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="b60c4-136">The **JavaScript Debugging** panel \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="b60c4-137">Várias ferramentas para inspecionar o JavaScript para a página da Web.</span><span class="sxs-lookup"><span data-stu-id="b60c4-137">Various tools for inspecting the JavaScript for the webpage.</span></span>  <span data-ttu-id="b60c4-138">Se sua janela DevTools for ampla, esse painel será exibido à direita do painel **Editor de** Código.</span><span class="sxs-lookup"><span data-stu-id="b60c4-138">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  
    
## <a name="step-3-pause-the-code-with-a-breakpoint"></a><span data-ttu-id="b60c4-139">Etapa 3: Pausar o código com um ponto de interrupção</span><span class="sxs-lookup"><span data-stu-id="b60c4-139">Step 3: Pause the code with a breakpoint</span></span>  

<span data-ttu-id="b60c4-140">Um método comum para depurar esse tipo de problema é inserir várias instruções no código e inspecionar valores conforme `console.log()` o script é executado.</span><span class="sxs-lookup"><span data-stu-id="b60c4-140">A common method for debugging this type of problem is to insert several `console.log()` statements into the code and then to inspect values as the script runs.</span></span>  <span data-ttu-id="b60c4-141">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b60c4-141">For example:</span></span>  

```javascript
function updateLabel() {
    var addend1 = getNumber1();
    console.log('addend1:', addend1);
    var addend2 = getNumber2();
    console.log('addend2:', addend2);
    var sum = addend1 + addend2;
    console.log('sum:', sum);
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
}
```  

<span data-ttu-id="b60c4-142">O `console.log()` método pode fazer o trabalho, mas os pontos de **interrupção** o aceleram.</span><span class="sxs-lookup"><span data-stu-id="b60c4-142">The `console.log()` method may get the job done, but **breakpoints** get it done faster.</span></span>  <span data-ttu-id="b60c4-143">Um ponto de interrupção permite pausar seu código no meio do tempo de execução e examinar todos os valores nesse momento.</span><span class="sxs-lookup"><span data-stu-id="b60c4-143">A breakpoint allows you to pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="b60c4-144">Os pontos de interrupção têm as seguintes vantagens sobre o `console.log()` método.</span><span class="sxs-lookup"><span data-stu-id="b60c4-144">Breakpoints have the following advantages over the `console.log()` method.</span></span>  

*   <span data-ttu-id="b60c4-145">Com , você precisa abrir manualmente o código-fonte, encontrar o código relevante, inserir as instruções e atualizar a página da Web para exibir as mensagens `console.log()` `console.log()` no **Console**.</span><span class="sxs-lookup"><span data-stu-id="b60c4-145">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.</span></span>  <span data-ttu-id="b60c4-146">Com pontos de interrupção, você pode pausar o código relevante sem saber como o código é estruturado.</span><span class="sxs-lookup"><span data-stu-id="b60c4-146">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="b60c4-147">Em suas `console.log()` instruções, você precisa especificar explicitamente cada valor que deseja inspecionar.</span><span class="sxs-lookup"><span data-stu-id="b60c4-147">In your `console.log()` statements, you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="b60c4-148">Com pontos de interrupção, o DevTools mostra os valores de todas as variáveis nesse momento.</span><span class="sxs-lookup"><span data-stu-id="b60c4-148">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="b60c4-149">Às vezes, as variáveis que afetam seu código são ocultas e ofuscados.</span><span class="sxs-lookup"><span data-stu-id="b60c4-149">Sometimes variables that affect your code are hidden and obfuscated.</span></span>  
    
<span data-ttu-id="b60c4-150">Em resumo, pontos de interrupção podem ajudá-lo a encontrar e corrigir bugs mais rapidamente do que o `console.log()` método.</span><span class="sxs-lookup"><span data-stu-id="b60c4-150">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="b60c4-151">Se você voltar e pensar em como o aplicativo funciona, você pode fazer uma suposição educada de que a soma incorreta \( \) é calculada no ouvinte de eventos associado ao botão Adicionar Número 1 e Número `5 + 1 = 51` `click` **2.**</span><span class="sxs-lookup"><span data-stu-id="b60c4-151">If you step back and think about how the app works, you may make an educated guess that the incorrect sum \(`5 + 1 = 51`\) is computed in the `click` event listener associated with the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="b60c4-152">Portanto, você provavelmente deseja pausar o código na hora em que o `click` ouvinte é executado.</span><span class="sxs-lookup"><span data-stu-id="b60c4-152">So, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="b60c4-153">**Os Pontos de Interrupção do** Ouvinte de Eventos permitem que você faça exatamente isso:</span><span class="sxs-lookup"><span data-stu-id="b60c4-153">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="b60c4-154">No painel **Depuração de JavaScript,** escolha Pontos de Interrupção do Ouvinte **de** Eventos para expandir a seção.</span><span class="sxs-lookup"><span data-stu-id="b60c4-154">In the **JavaScript Debugging** pane, choose **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="b60c4-155">O DevTools revela uma lista de categorias de eventos expansíveis, como **Animação** e **Área de Transferência.**</span><span class="sxs-lookup"><span data-stu-id="b60c4-155">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="b60c4-156">Ao lado da categoria de evento **Mouse,** escolha **Expandir** \( ![ Expand icon ][ImageExpandIcon] \).</span><span class="sxs-lookup"><span data-stu-id="b60c4-156">Next to the **Mouse** event category, choose **Expand** \(![Expand icon][ImageExpandIcon]\).</span></span>  <span data-ttu-id="b60c4-157">O DevTools revela uma lista de eventos do mouse, como **clique** e **mouse para baixo.**</span><span class="sxs-lookup"><span data-stu-id="b60c4-157">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="b60c4-158">Cada evento tem uma caixa de seleção ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="b60c4-158">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="b60c4-159">Escolha a caixa de seleção ao lado de **clicar em**.</span><span class="sxs-lookup"><span data-stu-id="b60c4-159">Choose the checkbox next to **click**.</span></span>  <span data-ttu-id="b60c4-160">O DevTools agora está definido para pausar automaticamente quando qualquer `click` ouvinte de eventos for executado.</span><span class="sxs-lookup"><span data-stu-id="b60c4-160">DevTools is now set up to automatically pause when any `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Escolha a caixa de seleção ao lado de clicar" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="b60c4-162">Escolha a caixa de seleção ao lado de **clicar**</span><span class="sxs-lookup"><span data-stu-id="b60c4-162">Choose the checkbox next to **click**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b60c4-163">De volta à demonstração, escolha **Adicionar Número 1 e Número 2** novamente.</span><span class="sxs-lookup"><span data-stu-id="b60c4-163">Back on the demo, choose **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="b60c4-164">O DevTools pausa a demonstração e realça uma linha de código na **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="b60c4-164">DevTools pauses the demo and highlights a line of code in the **Sources** tool.</span></span>  <span data-ttu-id="b60c4-165">DevTools deve pausar na linha 16 em `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="b60c4-165">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="b60c4-166">Se você pausar em uma linha de código diferente, escolha Retomar Execução de **Script** \( Retomar Execução de Script \) até pausar ![ na linha ][ImageResumeIcon] correta.</span><span class="sxs-lookup"><span data-stu-id="b60c4-166">If you pause on a different line of code, choose **Resume Script Execution** \(![Resume Script Execution][ImageResumeIcon]\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="b60c4-167">Se você fez uma pausa em uma linha diferente, você tem uma extensão do navegador que registra um ouvinte de eventos em cada página da `click` Web que você visitar.</span><span class="sxs-lookup"><span data-stu-id="b60c4-167">If you paused on a different line, you have a browser extension that registers a `click` event listener on every webpage that you visit.</span></span>  <span data-ttu-id="b60c4-168">Você é pausado no `click` ouvinte da extensão.</span><span class="sxs-lookup"><span data-stu-id="b60c4-168">You are paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="b60c4-169">Se você usar o Modo InPrivate para navegar em particular **,** o que desabilita todas as extensões, você pode ver que você pausa na linha de código desejada sempre.</span><span class="sxs-lookup"><span data-stu-id="b60c4-169">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="b60c4-170">**Os Pontos de Interrupção do** Ouvinte de Eventos são apenas um dos vários tipos de pontos de interrupção disponíveis no DevTools.</span><span class="sxs-lookup"><span data-stu-id="b60c4-170">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="b60c4-171">Memorize todos os tipos diferentes para ajudá-lo a depurar cenários diferentes o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="b60c4-171">Memorize all the different types to help you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <a name="step-4-step-through-the-code"></a><span data-ttu-id="b60c4-172">Etapa 4: Passar pelo código</span><span class="sxs-lookup"><span data-stu-id="b60c4-172">Step 4: Step through the code</span></span>  

<span data-ttu-id="b60c4-173">Uma causa comum de bugs é quando um script é executado na ordem errada.</span><span class="sxs-lookup"><span data-stu-id="b60c4-173">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="b60c4-174">Passar pelo código permite que você ande pelo tempo de execução do código.</span><span class="sxs-lookup"><span data-stu-id="b60c4-174">Stepping through your code allows you to walk through the runtime of your code.</span></span>  <span data-ttu-id="b60c4-175">Você passa por uma linha de cada vez para ajudá-lo a descobrir exatamente onde seu código está sendo executado em uma ordem diferente do esperado.</span><span class="sxs-lookup"><span data-stu-id="b60c4-175">You walk through one line at a time to help you figure out exactly where your code is running in a different order than you expect.</span></span>  <span data-ttu-id="b60c4-176">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="b60c4-176">Try it now:</span></span>  

1.  <span data-ttu-id="b60c4-177">Escolha **Step over next function call** \( Step over next function call ![ ][ImageOverIcon] \).</span><span class="sxs-lookup"><span data-stu-id="b60c4-177">Choose **Step over next function call** \(![Step over next function call][ImageOverIcon]\).</span></span>  <span data-ttu-id="b60c4-178">O DevTools executa o código a seguir sem entrar nele.</span><span class="sxs-lookup"><span data-stu-id="b60c4-178">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="b60c4-179">O DevTools ignora algumas linhas de código.</span><span class="sxs-lookup"><span data-stu-id="b60c4-179">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="b60c4-180">Isso acontece porque `inputsAreEmpty()` é avaliada como false, para que o bloco de código da `if` instrução não seja executado.</span><span class="sxs-lookup"><span data-stu-id="b60c4-180">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="b60c4-181">Na ferramenta **Sources** do DevTools, escolha Etapa na próxima chamada de função **\(** Passo a passo na próxima chamada de função \) para passar pelo tempo de execução da função, uma linha por ![ ][ImageIntoIcon] `updateLabel()` vez.</span><span class="sxs-lookup"><span data-stu-id="b60c4-181">On the **Sources** tool of DevTools, choose **Step into next function call** \(![Step into next function call][ImageIntoIcon]\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="b60c4-182">Revisar uma linha de cada vez é a ideia básica de passar pelo código.</span><span class="sxs-lookup"><span data-stu-id="b60c4-182">Reviewing one line at a time is the basic idea of stepping through code.</span></span>  <span data-ttu-id="b60c4-183">Se você revisar o código em `get-started.js` , o bug provavelmente está em algum lugar na `updateLabel()` função.</span><span class="sxs-lookup"><span data-stu-id="b60c4-183">If you review the code in `get-started.js`, the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="b60c4-184">Em vez de passar por cada linha de código, você pode usar outro tipo de ponto de interrupção para pausar o código mais próximo do local provável do bug.</span><span class="sxs-lookup"><span data-stu-id="b60c4-184">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <a name="step-5-set-a-line-of-code-breakpoint"></a><span data-ttu-id="b60c4-185">Etapa 5: Definir um ponto de interrupção de linha de código</span><span class="sxs-lookup"><span data-stu-id="b60c4-185">Step 5: Set a line-of-code breakpoint</span></span>  

<span data-ttu-id="b60c4-186">Pontos de interrupção de linha de código são o tipo de ponto de interrupção mais comum.</span><span class="sxs-lookup"><span data-stu-id="b60c4-186">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="b60c4-187">Quando você chegar à linha de código específica que deseja pausar, use um ponto de interrupção de linha de código.</span><span class="sxs-lookup"><span data-stu-id="b60c4-187">When you get to the specific line of code you want to pause, use a line-of-code breakpoint.</span></span>  

1.  <span data-ttu-id="b60c4-188">Veja a última linha de código em `updateLabel()` :</span><span class="sxs-lookup"><span data-stu-id="b60c4-188">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="b60c4-189">À esquerda, o número dessa linha de código específica é exibido como **34**.</span><span class="sxs-lookup"><span data-stu-id="b60c4-189">On the left, the number of this particular line of code is displayed as **34**.</span></span>  <span data-ttu-id="b60c4-190">Escolha a **linha 34**.</span><span class="sxs-lookup"><span data-stu-id="b60c4-190">Choose line **34**.</span></span>  <span data-ttu-id="b60c4-191">DevTools exibe um ícone vermelho à esquerda de **34**.</span><span class="sxs-lookup"><span data-stu-id="b60c4-191">DevTools displays a red icon to the left of **34**.</span></span>  <span data-ttu-id="b60c4-192">O ícone vermelho indica que um ponto de interrupção de linha de código está nessa linha.</span><span class="sxs-lookup"><span data-stu-id="b60c4-192">The red icon indicates that a line-of-code breakpoint is on this line.</span></span>  <span data-ttu-id="b60c4-193">O DevTools sempre pausa antes que essa linha de código seja executado.</span><span class="sxs-lookup"><span data-stu-id="b60c4-193">DevTools always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="b60c4-194">Escolha **Retomar execução de script** \( Retomar execução de script ![ ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="b60c4-194">Choose **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  <span data-ttu-id="b60c4-195">O script continua a ser executado até atingir a linha 33.</span><span class="sxs-lookup"><span data-stu-id="b60c4-195">The script continues to run until it reaches line 33.</span></span>  <span data-ttu-id="b60c4-196">Nas linhas 31, 32 e 33, DevTools imprime os valores de , e à direita dos pontos e vírgulas em `addend1` `addend2` cada `sum` linha.</span><span class="sxs-lookup"><span data-stu-id="b60c4-196">On lines 31, 32, and 33, DevTools prints the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="O DevTools pausa o ponto de interrupção de linha de código na linha 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="b60c4-198">O DevTools pausa o ponto de interrupção de linha de código na linha 34</span><span class="sxs-lookup"><span data-stu-id="b60c4-198">DevTools pauses on the line-of-code breakpoint on line 34</span></span>  
    :::image-end:::  
    
## <a name="step-6-check-variable-values"></a><span data-ttu-id="b60c4-199">Etapa 6: Verificar valores de variável</span><span class="sxs-lookup"><span data-stu-id="b60c4-199">Step 6: Check variable values</span></span>  

<span data-ttu-id="b60c4-200">Os valores `addend1` de , e parecem `addend2` `sum` suspeitos.</span><span class="sxs-lookup"><span data-stu-id="b60c4-200">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="b60c4-201">Os valores são empacotados entre aspas.</span><span class="sxs-lookup"><span data-stu-id="b60c4-201">The values are wrapped in quotes.</span></span>  <span data-ttu-id="b60c4-202">As aspas significam que o valor é uma cadeia de caracteres, o que é uma boa hipótese para explicar a causa do bug.</span><span class="sxs-lookup"><span data-stu-id="b60c4-202">The quotations mean that the value is a string, which is a good hypothesis to explain the cause of the bug.</span></span>  <span data-ttu-id="b60c4-203">Reúna mais informações sobre a situação.</span><span class="sxs-lookup"><span data-stu-id="b60c4-203">Gather more information about the situation.</span></span>  <span data-ttu-id="b60c4-204">O DevTools fornece muitas ferramentas para examinar valores variáveis.</span><span class="sxs-lookup"><span data-stu-id="b60c4-204">DevTools provides many tools for examining variable values.</span></span>  

### <a name="method-1-the-scope-panel"></a><span data-ttu-id="b60c4-205">Método 1: o painel Escopo</span><span class="sxs-lookup"><span data-stu-id="b60c4-205">Method 1: The Scope panel</span></span>  

<span data-ttu-id="b60c4-206">Se você pausar em uma linha de código, o painel **Escopo** exibirá as variáveis locais e globais que estão definidas no momento, juntamente com o valor de cada variável.</span><span class="sxs-lookup"><span data-stu-id="b60c4-206">If you pause on a line of code, the **Scope** panel displays the local and global variables that are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="b60c4-207">Ele também exibe variáveis de fechamento, conforme aplicável.</span><span class="sxs-lookup"><span data-stu-id="b60c4-207">It also displays closure variables, as applicable.</span></span>  <span data-ttu-id="b60c4-208">Clique duas vezes em um valor variável para editá-lo.</span><span class="sxs-lookup"><span data-stu-id="b60c4-208">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="b60c4-209">Se você não pausar em uma linha de código, o painel **Escopo** será vazio.</span><span class="sxs-lookup"><span data-stu-id="b60c4-209">If you don't pause on a line of code, the **Scope** panel is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="O painel Escopo" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="b60c4-211">O **painel Escopo**</span><span class="sxs-lookup"><span data-stu-id="b60c4-211">The **Scope** pane</span></span>  
:::image-end:::  

### <a name="method-2-watch-expressions"></a><span data-ttu-id="b60c4-212">Método 2: Expressões de Assistir</span><span class="sxs-lookup"><span data-stu-id="b60c4-212">Method 2: Watch Expressions</span></span>  

<span data-ttu-id="b60c4-213">O **painel Expressões de** Assistir permite monitorar os valores das variáveis ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="b60c4-213">The **Watch Expressions** panel lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="b60c4-214">Como o nome sugere, **Expressões de** Relógio não estão limitadas a variáveis.</span><span class="sxs-lookup"><span data-stu-id="b60c4-214">As the name implies, **Watch Expressions** aren't limited to variables.</span></span>  <span data-ttu-id="b60c4-215">Você pode armazenar qualquer expressão JavaScript válida em uma **expressão watch**.</span><span class="sxs-lookup"><span data-stu-id="b60c4-215">You may store any valid JavaScript expression in a **Watch Expression**.</span></span>  <span data-ttu-id="b60c4-216">Experimente agora.</span><span class="sxs-lookup"><span data-stu-id="b60c4-216">Try it now.</span></span>  

1.  <span data-ttu-id="b60c4-217">Escolha o **painel** Assistir.</span><span class="sxs-lookup"><span data-stu-id="b60c4-217">Choose the **Watch** panel.</span></span>  
1.  <span data-ttu-id="b60c4-218">Escolha **Adicionar Expressão** \( Adicionar Expressão ![ ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="b60c4-218">Choose **Add Expression** \(![Add Expression][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="b60c4-219">Digite `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="b60c4-219">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="b60c4-220">Selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b60c4-220">Select `Enter`.</span></span>  <span data-ttu-id="b60c4-221">DevTools mostra `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="b60c4-221">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="b60c4-222">O valor à direita dos dois pontos é o resultado da expressão do relógio.</span><span class="sxs-lookup"><span data-stu-id="b60c4-222">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="b60c4-223">No painel **Expressão do** Relógio \(inferior à direita\) na figura a seguir, a Expressão do Relógio `typeof sum` é exibida.</span><span class="sxs-lookup"><span data-stu-id="b60c4-223">In the **Watch Expression** pane \(bottom-right\) in the following figure, the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="b60c4-224">Se sua janela DevTools for grande, o **painel** Expressão do Relógio fica à direita acima do painel Pontos de Interrupção do Ouvinte **de** Eventos.</span><span class="sxs-lookup"><span data-stu-id="b60c4-224">If your DevTools window is large, the **Watch Expression** pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="O painel Expressão do Relógio" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="b60c4-226">O **painel Expressão do** Relógio</span><span class="sxs-lookup"><span data-stu-id="b60c4-226">The **Watch Expression** panel</span></span>  
:::image-end:::  

<span data-ttu-id="b60c4-227">Como suspeita, `sum` está sendo avaliado como uma cadeia de caracteres, quando deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="b60c4-227">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="b60c4-228">O tipo de valor confirmado agora é a causa do bug.</span><span class="sxs-lookup"><span data-stu-id="b60c4-228">You now confirmed value type is the cause of the bug.</span></span>  

### <a name="method-3-the-console"></a><span data-ttu-id="b60c4-229">Método 3: o console</span><span class="sxs-lookup"><span data-stu-id="b60c4-229">Method 3: The Console</span></span>  

<span data-ttu-id="b60c4-230">O **Console** permite que você veja mensagens e você também pode `console.log()` usá-la para avaliar instruções JavaScript arbitrárias.</span><span class="sxs-lookup"><span data-stu-id="b60c4-230">The **Console** allows you to view `console.log()` messages and you may also use it to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="b60c4-231">Para depuração, você pode usar o **Console** para testar possíveis correções para bugs.</span><span class="sxs-lookup"><span data-stu-id="b60c4-231">For debugging, you may use the **Console** to test potential fixes for bugs.</span></span>  <span data-ttu-id="b60c4-232">Experimente agora.</span><span class="sxs-lookup"><span data-stu-id="b60c4-232">Try it now.</span></span>  

1.  <span data-ttu-id="b60c4-233">Se a **ferramenta Console** estiver fechada, selecione `Escape` abri-la.</span><span class="sxs-lookup"><span data-stu-id="b60c4-233">If the **Console** tool is closed, select `Escape` to open it.</span></span>  <span data-ttu-id="b60c4-234">A **ferramenta Console** é aberta no painel inferior da janela DevTools.</span><span class="sxs-lookup"><span data-stu-id="b60c4-234">The **Console** tool opens in the lower panel of the DevTools window.</span></span>  
1.  <span data-ttu-id="b60c4-235">No **Console,** digite `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="b60c4-235">In the **Console**, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="b60c4-236">A instrução da ferramenta é pausada em uma linha de código onde `addend1` e `addend2` estão no escopo.</span><span class="sxs-lookup"><span data-stu-id="b60c4-236">The statement the tool is paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="b60c4-237">Selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b60c4-237">Select `Enter`.</span></span>  <span data-ttu-id="b60c4-238">DevTools avalia a instrução e as impressões , que `6` é o resultado que você espera que a demonstração produza.</span><span class="sxs-lookup"><span data-stu-id="b60c4-238">DevTools evaluates the statement and prints `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="A ferramenta Console, após avaliar parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="b60c4-240">A **ferramenta Console,** após a avaliação</span><span class="sxs-lookup"><span data-stu-id="b60c4-240">The **Console** tool, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <a name="step-7-apply-a-fix"></a><span data-ttu-id="b60c4-241">Etapa 7: Aplicar uma correção</span><span class="sxs-lookup"><span data-stu-id="b60c4-241">Step 7: Apply a fix</span></span>  

<span data-ttu-id="b60c4-242">Se você encontrar uma correção para o bug, experimente a correção editando o código e rerurindo a demonstração.</span><span class="sxs-lookup"><span data-stu-id="b60c4-242">If you find a fix for the bug, try out your fix by editing the code and rerunning the demo.</span></span>  <span data-ttu-id="b60c4-243">Você pode editar o código JavaScript diretamente na interface do usuário do DevTools e aplicar a correção.</span><span class="sxs-lookup"><span data-stu-id="b60c4-243">You may edit JavaScript code directly within the DevTools UI and apply the fix.</span></span>  <span data-ttu-id="b60c4-244">Experimente agora.</span><span class="sxs-lookup"><span data-stu-id="b60c4-244">Try it now.</span></span>  

1.  <span data-ttu-id="b60c4-245">Escolha **Retomar execução de script** \( Retomar execução de script ![ ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="b60c4-245">Choose **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  
1.  <span data-ttu-id="b60c4-246">No Editor **de Código,** substitua a linha 32, `var sum = addend1 + addend2` , por `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="b60c4-246">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="b60c4-247">Selecione `Control` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\) para salvar sua alteração.</span><span class="sxs-lookup"><span data-stu-id="b60c4-247">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="b60c4-248">Escolha **Desativar pontos de interrupção** \( Desativar pontos de ![ interrupção ][ImageDeactivateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="b60c4-248">Choose **Deactivate breakpoints** \(![Deactivate breakpoints][ImageDeactivateIcon]\).</span></span>  <span data-ttu-id="b60c4-249">Ele muda em azul para indicar que a opção está ativa.</span><span class="sxs-lookup"><span data-stu-id="b60c4-249">It changes blue to indicate the option is active.</span></span>  <span data-ttu-id="b60c4-250">Embora os pontos de interrupção de desativação **estão definidos,** o DevTools ignora todos os pontos de interrupção que você definir.</span><span class="sxs-lookup"><span data-stu-id="b60c4-250">While **Deactivate breakpoints** is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="b60c4-251">Experimente a demonstração com valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="b60c4-251">Try out the demo with different values.</span></span>  <span data-ttu-id="b60c4-252">A demonstração agora calcula corretamente.</span><span class="sxs-lookup"><span data-stu-id="b60c4-252">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="b60c4-253">Esse fluxo de trabalho aplica apenas uma correção ao código que está sendo executado no navegador.</span><span class="sxs-lookup"><span data-stu-id="b60c4-253">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="b60c4-254">Ele não corrige o código para todos os usuários que visitam sua página da Web.</span><span class="sxs-lookup"><span data-stu-id="b60c4-254">It does not fix the code for all users that visit your webpage.</span></span>  <span data-ttu-id="b60c4-255">Para fazer isso, você precisa corrigir o código que está em seus servidores.</span><span class="sxs-lookup"><span data-stu-id="b60c4-255">To do that, you need to fix the code that is on your servers.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="b60c4-256">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="b60c4-256">Next steps</span></span>  

<span data-ttu-id="b60c4-257">Parabéns!</span><span class="sxs-lookup"><span data-stu-id="b60c4-257">Congratulations!</span></span>  <span data-ttu-id="b60c4-258">Agora você sabe como usar o Microsoft Edge DevTools ao depurar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b60c4-258">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="b60c4-259">As ferramentas e os métodos que você aprendeu neste artigo podem salvar inúmeras horas.</span><span class="sxs-lookup"><span data-stu-id="b60c4-259">The tools and methods you learned in this article may save you countless hours.</span></span>  

<span data-ttu-id="b60c4-260">Este artigo ensinava apenas duas maneiras de definir pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="b60c4-260">This article only taught you two ways to set breakpoints.</span></span>  <span data-ttu-id="b60c4-261">O DevTools oferece muitas outras maneiras, incluindo as configurações a seguir.</span><span class="sxs-lookup"><span data-stu-id="b60c4-261">DevTools offers many other ways including the following settings.</span></span>  

*   <span data-ttu-id="b60c4-262">Pontos de interrupção condicionais que são disparados somente quando a condição que você fornece é verdadeira.</span><span class="sxs-lookup"><span data-stu-id="b60c4-262">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="b60c4-263">Pontos de interrupção em exceções capturadas ou não capturadas.</span><span class="sxs-lookup"><span data-stu-id="b60c4-263">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="b60c4-264">Pontos de interrupção XHR disparados quando a URL solicitada corresponde a uma subdstring que você fornece.</span><span class="sxs-lookup"><span data-stu-id="b60c4-264">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="b60c4-265">Para obter mais informações sobre quando e como usar cada tipo, navegue até [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="b60c4-265">For more information about when and how to use each type, navigate to [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="b60c4-266">Alguns controles de revisão de código não são explicados neste artigo.</span><span class="sxs-lookup"><span data-stu-id="b60c4-266">A couple of code stepping controls aren't explained in this article.</span></span>  <span data-ttu-id="b60c4-267">Para obter mais informações, navegue [até Passo sobre a linha de código][DevtoolsJavascriptReferenceStepThroughCode].</span><span class="sxs-lookup"><span data-stu-id="b60c4-267">For more information, navigate to [Step over line of code][DevtoolsJavascriptReferenceStepThroughCode].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="b60c4-268">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b60c4-268">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Como pausar seu código com pontos de interrupção no Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Código passo a passo - referência de depuração do JavaScript | Microsoft Docs"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Open Demo | Glitch"  

> [!NOTE]
> <span data-ttu-id="b60c4-272">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b60c4-272">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b60c4-273">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="b60c4-273">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b60c4-275">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b60c4-275">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
