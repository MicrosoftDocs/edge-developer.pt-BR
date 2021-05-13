---
description: Saiba como usar o Microsoft Edge DevTools para encontrar e corrigir bugs JavaScript.
title: Começar a depurar JavaScript no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 90a979cebcb74a118cb1d8ce88d48c7ac64c7a6d
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564088"
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
# <a name="get-started-with-debugging-javascript-in-microsoft-edge-devtools"></a><span data-ttu-id="3f568-104">Começar a depurar JavaScript no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3f568-104">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="3f568-105">Este artigo ensina o fluxo de trabalho básico para depurar qualquer problema javascript no DevTools.</span><span class="sxs-lookup"><span data-stu-id="3f568-105">This article teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <a name="step-1-reproduce-the-bug"></a><span data-ttu-id="3f568-106">Etapa 1: Reproduzir o bug</span><span class="sxs-lookup"><span data-stu-id="3f568-106">Step 1: Reproduce the bug</span></span>  

<span data-ttu-id="3f568-107">Encontrar uma série de ações que reproduzam consistentemente um bug é sempre a primeira etapa para a depuração.</span><span class="sxs-lookup"><span data-stu-id="3f568-107">Finding a series of actions that consistently reproduce a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="3f568-108">Escolha o seguinte link **Abrir Demonstração** e abra a página da Web em uma nova guia.  Para abrir a demonstração em uma nova guia, selecione e segure `Ctrl` \(Windows, Linux\) `Command` ou \(macOS\) e escolha **Abrir Demonstração**.</span><span class="sxs-lookup"><span data-stu-id="3f568-108">Choose the following **Open Demo** link and open the webpage in a new tab.  To open the demo in a new tab, select and hold `Ctrl` \(Windows, Linux\) or `Command` \(macOS\), and then choose **Open Demo**.</span></span>  
    
    [<span data-ttu-id="3f568-109">Abrir Demonstração</span><span class="sxs-lookup"><span data-stu-id="3f568-109">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="3f568-110">Insira `5` na caixa de texto Número **1.**</span><span class="sxs-lookup"><span data-stu-id="3f568-110">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="3f568-111">Insira `1` na caixa de texto Número **2.**</span><span class="sxs-lookup"><span data-stu-id="3f568-111">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="3f568-112">Escolha **Adicionar Número 1 e Número 2**.</span><span class="sxs-lookup"><span data-stu-id="3f568-112">Choose **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="3f568-113">O rótulo abaixo do botão diz `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="3f568-113">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="3f568-114">O resultado deve ser `6` .</span><span class="sxs-lookup"><span data-stu-id="3f568-114">The result should be `6`.</span></span>  <span data-ttu-id="3f568-115">Em seguida, corrige o erro de adição que é o bug.</span><span class="sxs-lookup"><span data-stu-id="3f568-115">Next, fix the addition error that is the bug.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 resulta em 51, mas deve ser 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` <span data-ttu-id="3f568-117">resulta `51` em , mas deve ser</span><span class="sxs-lookup"><span data-stu-id="3f568-117">results in `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <a name="step-2-get-familiar-with-the-sources-tool-ui"></a><span data-ttu-id="3f568-118">Etapa 2: Familiarizar-se com a interface do usuário da ferramenta Sources</span><span class="sxs-lookup"><span data-stu-id="3f568-118">Step 2: Get familiar with the Sources tool UI</span></span>  

<span data-ttu-id="3f568-119">O DevTools fornece muitas ferramentas diferentes para tarefas diferentes.</span><span class="sxs-lookup"><span data-stu-id="3f568-119">DevTools provides many different tools for different tasks.</span></span>  <span data-ttu-id="3f568-120">Tarefas diferentes incluem alterar CSS, perfil de desempenho de carga de página e monitoramento de solicitações de rede.</span><span class="sxs-lookup"><span data-stu-id="3f568-120">Different tasks include changing CSS, profiling page-load performance, and monitoring network requests.</span></span>  <span data-ttu-id="3f568-121">A **ferramenta Sources** é onde você depura JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3f568-121">The **Sources** tool is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="3f568-122">Para abrir a **ferramenta Console** no DevTools, selecione `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="3f568-122">To open the **Console** tool in DevTools, select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="A ferramenta Console" lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="3f568-124">A **ferramenta Console**</span><span class="sxs-lookup"><span data-stu-id="3f568-124">The **Console** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3f568-125">Escolha a **ferramenta Fontes.**</span><span class="sxs-lookup"><span data-stu-id="3f568-125">Choose the **Sources** tool.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="A ferramenta Sources" lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="3f568-127">A **ferramenta Sources**</span><span class="sxs-lookup"><span data-stu-id="3f568-127">The **Sources** tool</span></span>  
    :::image-end:::  
    
<span data-ttu-id="3f568-128">A **interface do usuário** da ferramenta Sources tem três partes.</span><span class="sxs-lookup"><span data-stu-id="3f568-128">The **Sources** tool UI has three parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="As 3 partes da interface do usuário da ferramenta Sources" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="3f568-130">As 3 partes da interface do **usuário da ferramenta Sources**</span><span class="sxs-lookup"><span data-stu-id="3f568-130">The 3 parts of the **Sources** tool UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="3f568-131">O **painel** Navegador \(Seção 1 na figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="3f568-131">The **Navigator** pane \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="3f568-132">Todos os arquivos que a página da Web solicita estão listados aqui.</span><span class="sxs-lookup"><span data-stu-id="3f568-132">Every file that the webpage requests is listed here.</span></span>  
1.  <span data-ttu-id="3f568-133">O **painel** Editor \(Seção 2 na figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="3f568-133">The **Editor** pane \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="3f568-134">Depois de escolher um arquivo no painel **Navegador,** esse painel exibe o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3f568-134">After you choose a file in the **Navigator** pane, this pane displays the contents of the file.</span></span>  
1.  <span data-ttu-id="3f568-135">O **painel Depurador** \(Seção 3 na figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="3f568-135">The **Debugger** pane \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="3f568-136">Este painel fornece ferramentas para inspecionar o JavaScript para a página da Web.</span><span class="sxs-lookup"><span data-stu-id="3f568-136">This pane provides tools for inspecting the JavaScript for the webpage.</span></span>  <span data-ttu-id="3f568-137">Se sua janela DevTools for ampla, esse painel será exibido à direita do **painel Editor.**</span><span class="sxs-lookup"><span data-stu-id="3f568-137">If your DevTools window is wide, this pane is displayed to the right of the **Editor** pane.</span></span>  
    
## <a name="step-3-pause-the-code-with-a-breakpoint"></a><span data-ttu-id="3f568-138">Etapa 3: Pausar o código com um ponto de interrupção</span><span class="sxs-lookup"><span data-stu-id="3f568-138">Step 3: Pause the code with a breakpoint</span></span>  

<span data-ttu-id="3f568-139">Um método comum para depurar esse tipo de problema é inserir várias instruções no código e inspecionar valores conforme `console.log()` o script é executado.</span><span class="sxs-lookup"><span data-stu-id="3f568-139">A common method for debugging this type of problem is to insert several `console.log()` statements into the code and then to inspect values as the script runs.</span></span>  <span data-ttu-id="3f568-140">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="3f568-140">For example:</span></span>  

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

<span data-ttu-id="3f568-141">O `console.log()` método pode fazer o trabalho, mas os pontos de **interrupção** o aceleram.</span><span class="sxs-lookup"><span data-stu-id="3f568-141">The `console.log()` method may get the job done, but **breakpoints** get it done faster.</span></span>  <span data-ttu-id="3f568-142">Um ponto de interrupção permite pausar seu código no meio do tempo de execução e examinar todos os valores nesse momento.</span><span class="sxs-lookup"><span data-stu-id="3f568-142">A breakpoint allows you to pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="3f568-143">Os pontos de interrupção têm as seguintes vantagens sobre o `console.log()` método.</span><span class="sxs-lookup"><span data-stu-id="3f568-143">Breakpoints have the following advantages over the `console.log()` method.</span></span>  

*   <span data-ttu-id="3f568-144">Com , você precisa abrir manualmente o código-fonte, encontrar o código relevante, inserir as instruções e atualizar a página da Web para exibir as mensagens `console.log()` `console.log()` no **Console**.</span><span class="sxs-lookup"><span data-stu-id="3f568-144">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.</span></span>  <span data-ttu-id="3f568-145">Com pontos de interrupção, você pode pausar o código relevante sem saber como o código é estruturado.</span><span class="sxs-lookup"><span data-stu-id="3f568-145">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="3f568-146">Em suas `console.log()` instruções, você precisa especificar explicitamente cada valor que deseja inspecionar.</span><span class="sxs-lookup"><span data-stu-id="3f568-146">In your `console.log()` statements, you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="3f568-147">Com pontos de interrupção, o DevTools mostra os valores de todas as variáveis nesse momento.</span><span class="sxs-lookup"><span data-stu-id="3f568-147">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="3f568-148">Às vezes, as variáveis que afetam seu código são ocultas e ofuscados.</span><span class="sxs-lookup"><span data-stu-id="3f568-148">Sometimes variables that affect your code are hidden and obfuscated.</span></span>  
    
<span data-ttu-id="3f568-149">Em resumo, pontos de interrupção podem ajudá-lo a encontrar e corrigir bugs mais rapidamente do que o `console.log()` método.</span><span class="sxs-lookup"><span data-stu-id="3f568-149">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="3f568-150">Se você voltar e pensar em como o aplicativo funciona, você pode fazer uma suposição educada de que a soma incorreta \( \) é calculada no ouvinte de eventos associado ao botão Adicionar Número 1 e Número `5 + 1 = 51` `click` **2.**</span><span class="sxs-lookup"><span data-stu-id="3f568-150">If you step back and think about how the app works, you may make an educated guess that the incorrect sum \(`5 + 1 = 51`\) is computed in the `click` event listener associated with the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="3f568-151">Portanto, você provavelmente deseja pausar o código na hora em que o `click` ouvinte é executado.</span><span class="sxs-lookup"><span data-stu-id="3f568-151">So, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="3f568-152">**Os Pontos de Interrupção do** Ouvinte de Eventos permitem que você faça exatamente isso:</span><span class="sxs-lookup"><span data-stu-id="3f568-152">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="3f568-153">No painel **Depurador,** escolha Pontos de Interrupção **do Ouvinte de** Eventos para expandir a seção.</span><span class="sxs-lookup"><span data-stu-id="3f568-153">In the **Debugger** pane, choose **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="3f568-154">O DevTools revela uma lista de categorias de eventos expansíveis, como **Animação** e **Área de Transferência.**</span><span class="sxs-lookup"><span data-stu-id="3f568-154">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="3f568-155">Ao lado da categoria de evento **Mouse,** escolha **Expandir** \( ![ Expand icon ](../media/expand-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="3f568-155">Next to the **Mouse** event category, choose **Expand** \(![Expand icon](../media/expand-icon.msft.png)\).</span></span>  <span data-ttu-id="3f568-156">O DevTools revela uma lista de eventos do mouse, como **clique** e **mouse para baixo.**</span><span class="sxs-lookup"><span data-stu-id="3f568-156">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="3f568-157">Cada evento tem uma caixa de seleção ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="3f568-157">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="3f568-158">Escolha a caixa de seleção ao lado de **clicar em**.</span><span class="sxs-lookup"><span data-stu-id="3f568-158">Choose the checkbox next to **click**.</span></span>  <span data-ttu-id="3f568-159">O DevTools agora está definido para pausar automaticamente quando qualquer `click` ouvinte de eventos for executado.</span><span class="sxs-lookup"><span data-stu-id="3f568-159">DevTools is now set up to automatically pause when any `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Escolha a caixa de seleção ao lado de clicar" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="3f568-161">Escolha a caixa de seleção ao lado de **clicar**</span><span class="sxs-lookup"><span data-stu-id="3f568-161">Choose the checkbox next to **click**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3f568-162">De volta à demonstração, escolha **Adicionar Número 1 e Número 2** novamente.</span><span class="sxs-lookup"><span data-stu-id="3f568-162">Back on the demo, choose **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="3f568-163">O DevTools pausa a demonstração e realça uma linha de código na **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="3f568-163">DevTools pauses the demo and highlights a line of code in the **Sources** tool.</span></span>  <span data-ttu-id="3f568-164">DevTools deve pausar na linha 16 em `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="3f568-164">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="3f568-165">Se você pausar em uma linha de código diferente, escolha Retomar Execução de **Script** \( Retomar Execução de Script \) até pausar ![ na linha ](../media/resume-script-run-icon.msft.png) correta.</span><span class="sxs-lookup"><span data-stu-id="3f568-165">If you pause on a different line of code, choose **Resume Script Execution** \(![Resume Script Execution](../media/resume-script-run-icon.msft.png)\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="3f568-166">Se você fez uma pausa em uma linha diferente, você tem uma extensão do navegador que registra um ouvinte de eventos em cada página da `click` Web que você visitar.</span><span class="sxs-lookup"><span data-stu-id="3f568-166">If you paused on a different line, you have a browser extension that registers a `click` event listener on every webpage that you visit.</span></span>  <span data-ttu-id="3f568-167">Você é pausado no `click` ouvinte da extensão.</span><span class="sxs-lookup"><span data-stu-id="3f568-167">You are paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="3f568-168">Se você usar o Modo InPrivate para navegar em particular **,** o que desabilita todas as extensões, você pode ver que você pausa na linha de código desejada sempre.</span><span class="sxs-lookup"><span data-stu-id="3f568-168">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="3f568-169">**Os Pontos de Interrupção do** Ouvinte de Eventos são apenas um dos vários tipos de pontos de interrupção disponíveis no DevTools.</span><span class="sxs-lookup"><span data-stu-id="3f568-169">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="3f568-170">Memorize todos os tipos diferentes para ajudá-lo a depurar cenários diferentes o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="3f568-170">Memorize all the different types to help you debug different scenarios as quickly as possible.</span></span>  <!--  To learn when and how to use each type, navigate to [Pause your code with breakpoints][JSBreakpoints].  -->  

## <a name="step-4-step-through-the-code"></a><span data-ttu-id="3f568-171">Etapa 4: Passar pelo código</span><span class="sxs-lookup"><span data-stu-id="3f568-171">Step 4: Step through the code</span></span>  

<span data-ttu-id="3f568-172">Uma causa comum de bugs é quando um script é executado na ordem errada.</span><span class="sxs-lookup"><span data-stu-id="3f568-172">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="3f568-173">Passar pelo código permite que você ande pelo tempo de execução do código.</span><span class="sxs-lookup"><span data-stu-id="3f568-173">Stepping through your code allows you to walk through the runtime of your code.</span></span>  <span data-ttu-id="3f568-174">Você passa por uma linha de cada vez para ajudá-lo a descobrir exatamente onde seu código está sendo executado em uma ordem diferente do esperado.</span><span class="sxs-lookup"><span data-stu-id="3f568-174">You walk through one line at a time to help you figure out exactly where your code is running in a different order than you expect.</span></span>  <span data-ttu-id="3f568-175">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="3f568-175">Try it now:</span></span>  

1.  <span data-ttu-id="3f568-176">Escolha **Step over next function call** \( Step over next function call ![ ](../media/step-over-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="3f568-176">Choose **Step over next function call** \(![Step over next function call](../media/step-over-icon.msft.png)\).</span></span>  <span data-ttu-id="3f568-177">O DevTools executa o código a seguir sem entrar nele.</span><span class="sxs-lookup"><span data-stu-id="3f568-177">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="3f568-178">O DevTools ignora algumas linhas de código.</span><span class="sxs-lookup"><span data-stu-id="3f568-178">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="3f568-179">Isso acontece porque `inputsAreEmpty()` é avaliada como false, para que o bloco de código da `if` instrução não seja executado.</span><span class="sxs-lookup"><span data-stu-id="3f568-179">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="3f568-180">Na ferramenta **Sources** do DevTools, escolha Etapa na próxima chamada de função **\(** Passo a passo na próxima chamada de função \) para passar pelo tempo de execução da função, uma linha por ![ ](../media/step-into-icon.msft.png) `updateLabel()` vez.</span><span class="sxs-lookup"><span data-stu-id="3f568-180">On the **Sources** tool of DevTools, choose **Step into next function call** \(![Step into next function call](../media/step-into-icon.msft.png)\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="3f568-181">Revisar uma linha de cada vez é a ideia básica de passar pelo código.</span><span class="sxs-lookup"><span data-stu-id="3f568-181">Reviewing one line at a time is the basic idea of stepping through code.</span></span>  <span data-ttu-id="3f568-182">Se você revisar o código em `get-started.js` , o bug provavelmente está em algum lugar na `updateLabel()` função.</span><span class="sxs-lookup"><span data-stu-id="3f568-182">If you review the code in `get-started.js`, the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="3f568-183">Em vez de passar por cada linha de código, você pode usar outro tipo de ponto de interrupção para pausar o código mais próximo do local provável do bug.</span><span class="sxs-lookup"><span data-stu-id="3f568-183">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <a name="step-5-set-a-line-of-code-breakpoint"></a><span data-ttu-id="3f568-184">Etapa 5: Definir um ponto de interrupção de linha de código</span><span class="sxs-lookup"><span data-stu-id="3f568-184">Step 5: Set a line-of-code breakpoint</span></span>  

<span data-ttu-id="3f568-185">Pontos de interrupção de linha de código são o tipo de ponto de interrupção mais comum.</span><span class="sxs-lookup"><span data-stu-id="3f568-185">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="3f568-186">Quando você chegar à linha de código específica que deseja pausar, use um ponto de interrupção de linha de código.</span><span class="sxs-lookup"><span data-stu-id="3f568-186">When you get to the specific line of code you want to pause, use a line-of-code breakpoint.</span></span>  

1.  <span data-ttu-id="3f568-187">Veja a última linha de código em `updateLabel()` :</span><span class="sxs-lookup"><span data-stu-id="3f568-187">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="3f568-188">À esquerda, o número dessa linha de código específica é exibido como **34**.</span><span class="sxs-lookup"><span data-stu-id="3f568-188">On the left, the number of this particular line of code is displayed as **34**.</span></span>  <span data-ttu-id="3f568-189">Escolha a **linha 34**.</span><span class="sxs-lookup"><span data-stu-id="3f568-189">Choose line **34**.</span></span>  <span data-ttu-id="3f568-190">DevTools exibe um ícone vermelho à esquerda de **34**.</span><span class="sxs-lookup"><span data-stu-id="3f568-190">DevTools displays a red icon to the left of **34**.</span></span>  <span data-ttu-id="3f568-191">O ícone vermelho indica que um ponto de interrupção de linha de código está nessa linha.</span><span class="sxs-lookup"><span data-stu-id="3f568-191">The red icon indicates that a line-of-code breakpoint is on this line.</span></span>  <span data-ttu-id="3f568-192">O DevTools sempre pausa antes que essa linha de código seja executado.</span><span class="sxs-lookup"><span data-stu-id="3f568-192">DevTools always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="3f568-193">Escolha **Retomar execução de script** \( Retomar execução de script ![ ](../media/resume-script-run-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="3f568-193">Choose **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\).</span></span>  <span data-ttu-id="3f568-194">O script continua a ser executado até atingir a linha 33.</span><span class="sxs-lookup"><span data-stu-id="3f568-194">The script continues to run until it reaches line 33.</span></span>  <span data-ttu-id="3f568-195">Nas linhas 31, 32 e 33, DevTools imprime os valores de , e à direita dos pontos e vírgulas em `addend1` `addend2` cada `sum` linha.</span><span class="sxs-lookup"><span data-stu-id="3f568-195">On lines 31, 32, and 33, DevTools prints the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="O DevTools pausa o ponto de interrupção de linha de código na linha 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="3f568-197">O DevTools pausa o ponto de interrupção de linha de código na linha 34</span><span class="sxs-lookup"><span data-stu-id="3f568-197">DevTools pauses on the line-of-code breakpoint on line 34</span></span>  
    :::image-end:::  
    
## <a name="step-6-check-variable-values"></a><span data-ttu-id="3f568-198">Etapa 6: Verificar valores de variável</span><span class="sxs-lookup"><span data-stu-id="3f568-198">Step 6: Check variable values</span></span>  

<span data-ttu-id="3f568-199">Os valores `addend1` de , e parecem `addend2` `sum` suspeitos.</span><span class="sxs-lookup"><span data-stu-id="3f568-199">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="3f568-200">Os valores são empacotados entre aspas.</span><span class="sxs-lookup"><span data-stu-id="3f568-200">The values are wrapped in quotes.</span></span>  <span data-ttu-id="3f568-201">As aspas significam que o valor é uma cadeia de caracteres, o que é uma boa hipótese para explicar a causa do bug.</span><span class="sxs-lookup"><span data-stu-id="3f568-201">The quotations mean that the value is a string, which is a good hypothesis to explain the cause of the bug.</span></span>  <span data-ttu-id="3f568-202">Reúna mais informações sobre a situação.</span><span class="sxs-lookup"><span data-stu-id="3f568-202">Gather more information about the situation.</span></span>  <span data-ttu-id="3f568-203">O DevTools fornece muitas ferramentas para examinar valores variáveis.</span><span class="sxs-lookup"><span data-stu-id="3f568-203">DevTools provides many tools for examining variable values.</span></span>  

### <a name="method-1-the-scope-pane"></a><span data-ttu-id="3f568-204">Método 1: o painel Escopo</span><span class="sxs-lookup"><span data-stu-id="3f568-204">Method 1: The Scope pane</span></span>  

<span data-ttu-id="3f568-205">Se você pausar em uma linha de código, o painel **Escopo** exibirá as variáveis locais e globais que estão definidas no momento, juntamente com o valor de cada variável.</span><span class="sxs-lookup"><span data-stu-id="3f568-205">If you pause on a line of code, the **Scope** pane displays the local and global variables that are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="3f568-206">Ele também exibe variáveis de fechamento, conforme aplicável.</span><span class="sxs-lookup"><span data-stu-id="3f568-206">It also displays closure variables, as applicable.</span></span>  <span data-ttu-id="3f568-207">Clique duas vezes em um valor variável para editá-lo.</span><span class="sxs-lookup"><span data-stu-id="3f568-207">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="3f568-208">Se você não pausar em uma linha de código, o painel **Escopo** fica vazio.</span><span class="sxs-lookup"><span data-stu-id="3f568-208">If you don't pause on a line of code, the **Scope** pane is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="O painel Escopo" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="3f568-210">O **painel Escopo**</span><span class="sxs-lookup"><span data-stu-id="3f568-210">The **Scope** pane</span></span>  
:::image-end:::  

### <a name="method-2-watch-expressions"></a><span data-ttu-id="3f568-211">Método 2: Expressões de Assistir</span><span class="sxs-lookup"><span data-stu-id="3f568-211">Method 2: Watch Expressions</span></span>  

<span data-ttu-id="3f568-212">O **painel** de relógio permite que você monitore os valores de variáveis (como `sum` ) ou expressões (como `typeof sum` ).</span><span class="sxs-lookup"><span data-stu-id="3f568-212">The **Watch** pane allows you to monitor the values of variables (such as `sum`) or expressions (such as `typeof sum`).</span></span>  <span data-ttu-id="3f568-213">Você pode armazenar qualquer expressão JavaScript válida em uma Expressão de Relógio.</span><span class="sxs-lookup"><span data-stu-id="3f568-213">You may store any valid JavaScript expression in a Watch Expression.</span></span>  

1.  <span data-ttu-id="3f568-214">Escolha o **painel** Assistir.</span><span class="sxs-lookup"><span data-stu-id="3f568-214">Choose the **Watch** pane.</span></span>  
1.  <span data-ttu-id="3f568-215">Escolha **Adicionar expressão de relógio** \( Adicionar expressão de relógio ![ ](../media/add-expression-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="3f568-215">Choose **Add watch expression** \(![Add watch expression](../media/add-expression-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="3f568-216">Digite `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="3f568-216">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="3f568-217">Selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3f568-217">Select `Enter`.</span></span>  <span data-ttu-id="3f568-218">DevTools exibe `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="3f568-218">DevTools displays `typeof sum: "string"`.</span></span>  <span data-ttu-id="3f568-219">O valor à direita dos dois pontos é o resultado da expressão do relógio.</span><span class="sxs-lookup"><span data-stu-id="3f568-219">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="3f568-220">Na figura a seguir, a `typeof sum` Expressão \*\*\*\* do Relógio é exibida no painel De exibição.</span><span class="sxs-lookup"><span data-stu-id="3f568-220">In the following figure, the `typeof sum` Watch Expression is displayed in the **Watch** pane.</span></span>  <span data-ttu-id="3f568-221">Se sua janela DevTools for ampla, o **painel** Depurador será exibido no painel **Depurador,** que será exibido à direita.</span><span class="sxs-lookup"><span data-stu-id="3f568-221">If your DevTools window is wide, the **Watch** pane is displayed within the **Debugger** pane, which then appears on the right.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="O painel de relógio" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="3f568-223">O **painel** de relógio</span><span class="sxs-lookup"><span data-stu-id="3f568-223">The **Watch** pane</span></span>  
:::image-end:::  

<span data-ttu-id="3f568-224">Como suspeita, `sum` está sendo avaliado como uma cadeia de caracteres, quando deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="3f568-224">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="3f568-225">O tipo de valor confirmado agora é a causa do bug.</span><span class="sxs-lookup"><span data-stu-id="3f568-225">You now confirmed value type is the cause of the bug.</span></span>  

### <a name="method-3-the-console"></a><span data-ttu-id="3f568-226">Método 3: o console</span><span class="sxs-lookup"><span data-stu-id="3f568-226">Method 3: The Console</span></span>  

<span data-ttu-id="3f568-227">O **Console** permite que você veja a `console.log()` saída.</span><span class="sxs-lookup"><span data-stu-id="3f568-227">The **Console** allows you to view `console.log()` output.</span></span>  <span data-ttu-id="3f568-228">Você também pode usar o **Console para** avaliar instruções JavaScript arbitrárias enquanto o depurador é pausado em uma instrução de código.</span><span class="sxs-lookup"><span data-stu-id="3f568-228">You can also use the **Console** to evaluate arbitrary JavaScript statements while the debugger is paused at a code statement.</span></span>  <span data-ttu-id="3f568-229">Para depuração, você pode usar o **Console** para testar possíveis correções para bugs.</span><span class="sxs-lookup"><span data-stu-id="3f568-229">For debugging, you can use the **Console** to test potential fixes for bugs.</span></span>

1.  <span data-ttu-id="3f568-230">Se a **ferramenta Console** estiver fechada, selecione `Esc` abri-la.</span><span class="sxs-lookup"><span data-stu-id="3f568-230">If the **Console** tool is closed, select `Esc` to open it.</span></span>  <span data-ttu-id="3f568-231">A **ferramenta Console** é aberta no painel inferior da janela DevTools.</span><span class="sxs-lookup"><span data-stu-id="3f568-231">The **Console** tool opens in the lower pane of the DevTools window.</span></span>  
1.  <span data-ttu-id="3f568-232">No **Console,** digite `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="3f568-232">In the **Console**, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="3f568-233">A instrução da ferramenta é pausada em uma linha de código onde `addend1` e `addend2` estão no escopo.</span><span class="sxs-lookup"><span data-stu-id="3f568-233">The statement the tool is paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="3f568-234">Selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3f568-234">Select `Enter`.</span></span>  <span data-ttu-id="3f568-235">DevTools avalia a instrução e as impressões , que `6` é o resultado que você espera que a demonstração produza.</span><span class="sxs-lookup"><span data-stu-id="3f568-235">DevTools evaluates the statement and prints `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="A ferramenta Console, após avaliar parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="3f568-237">A **ferramenta Console,** após a avaliação</span><span class="sxs-lookup"><span data-stu-id="3f568-237">The **Console** tool, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <a name="step-7-apply-a-fix"></a><span data-ttu-id="3f568-238">Etapa 7: Aplicar uma correção</span><span class="sxs-lookup"><span data-stu-id="3f568-238">Step 7: Apply a fix</span></span>  

<span data-ttu-id="3f568-239">Identificamos uma possível correção para o bug.</span><span class="sxs-lookup"><span data-stu-id="3f568-239">We've identified a possible fix for the bug.</span></span>  <span data-ttu-id="3f568-240">Em seguida, edite o código JavaScript diretamente na interface do usuário do DevTools e, em seguida, executar a demonstração para testar a correção, da seguinte forma.</span><span class="sxs-lookup"><span data-stu-id="3f568-240">Next, edit the JavaScript code directly within the DevTools UI and then rerun the demo to test the fix, as follows.</span></span>

1.  <span data-ttu-id="3f568-241">Escolha **Retomar execução de script** \( Retomar execução de script ![ ](../media/resume-script-run-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="3f568-241">Choose **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="3f568-242">No painel **Editor,** substitua a linha `var sum = addend1 + addend2` por `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="3f568-242">In the **Editor** pane, replace the line `var sum = addend1 + addend2` with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="3f568-243">Selecione `Control` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\) para salvar a alteração.</span><span class="sxs-lookup"><span data-stu-id="3f568-243">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="3f568-244">Escolha **Desativar pontos de interrupção** \( Desativar pontos de ![ interrupção ](../media/deactivate-breakpoints-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="3f568-244">Choose **Deactivate breakpoints** \(![Deactivate breakpoints](../media/deactivate-breakpoints-button-icon.msft.png)\).</span></span>  <span data-ttu-id="3f568-245">Ele muda em azul para indicar que a opção está ativa.</span><span class="sxs-lookup"><span data-stu-id="3f568-245">It changes blue to indicate the option is active.</span></span>  <span data-ttu-id="3f568-246">Embora os pontos de interrupção de desativação **estão definidos,** o DevTools ignora todos os pontos de interrupção que você definir.</span><span class="sxs-lookup"><span data-stu-id="3f568-246">While **Deactivate breakpoints** is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="3f568-247">Experimente a demonstração com valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="3f568-247">Try out the demo with different values.</span></span>  <span data-ttu-id="3f568-248">A demonstração agora calcula corretamente.</span><span class="sxs-lookup"><span data-stu-id="3f568-248">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="3f568-249">Esse fluxo de trabalho aplica apenas uma correção a uma cópia local do código enviado do servidor.</span><span class="sxs-lookup"><span data-stu-id="3f568-249">This workflow only applies a fix to a local copy of the code sent from the server.</span></span>  <span data-ttu-id="3f568-250">Ao depurar seu projeto, depois de identificar a correção, você ainda precisa aplicar essa correção ao código no servidor, como editando seu código-fonte local e implantando seu código fixo no servidor.</span><span class="sxs-lookup"><span data-stu-id="3f568-250">When debugging your project, after you identify the fix, you still need to apply that fix to the code on the server, such as by editing your local source code and then re-deploying your fixed code to the server.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3f568-251">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="3f568-251">Next steps</span></span>  

<span data-ttu-id="3f568-252">Parabéns!</span><span class="sxs-lookup"><span data-stu-id="3f568-252">Congratulations!</span></span>  <span data-ttu-id="3f568-253">Agora você sabe como usar ao máximo Microsoft Edge DevTools ao depurar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3f568-253">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="3f568-254">As ferramentas e os métodos que você aprendeu neste artigo podem salvar inúmeras horas.</span><span class="sxs-lookup"><span data-stu-id="3f568-254">The tools and methods you learned in this article may save you countless hours.</span></span>  

<span data-ttu-id="3f568-255">Este artigo mostrou duas maneiras de definir pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="3f568-255">This article showed two ways to set breakpoints.</span></span>  <span data-ttu-id="3f568-256">O DevTools também fornece maneiras de definir pontos de interrupção para pausar seu código quando determinadas condições são atendidas, como:</span><span class="sxs-lookup"><span data-stu-id="3f568-256">DevTools also provides ways to set breakpoints to pause your code when certain conditions are met, such as:</span></span>

*   <span data-ttu-id="3f568-257">Pontos de interrupção condicionais que são disparados somente quando a condição que você fornece é verdadeira.</span><span class="sxs-lookup"><span data-stu-id="3f568-257">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="3f568-258">Pontos de interrupção em exceções capturadas ou não capturadas.</span><span class="sxs-lookup"><span data-stu-id="3f568-258">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="3f568-259">Pontos de interrupção XHR disparados quando a URL solicitada corresponde a uma subdstring que você fornece.</span><span class="sxs-lookup"><span data-stu-id="3f568-259">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="3f568-260">Para obter mais informações sobre quando e como usar cada tipo, navegue até [Pause your code with breakpoints][DevToolsJavscriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="3f568-260">For more information about when and how to use each type, navigate to [Pause your code with breakpoints][DevToolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="3f568-261">Alguns controles de revisão de código não são explicados neste artigo.</span><span class="sxs-lookup"><span data-stu-id="3f568-261">A couple of code stepping controls aren't explained in this article.</span></span>  <span data-ttu-id="3f568-262">Para obter mais informações, navegue até [Passo sobre a][DevToolsJavascriptReferenceStepThroughCode] linha de código no artigo "Usar os recursos do depurador".</span><span class="sxs-lookup"><span data-stu-id="3f568-262">For more information, navigate to [Step over line of code][DevToolsJavascriptReferenceStepThroughCode] in the "Use the debugger features" article.</span></span>

### <a name="see-also"></a><span data-ttu-id="3f568-263">Ver também</span><span class="sxs-lookup"><span data-stu-id="3f568-263">See also</span></span>

*   <span data-ttu-id="3f568-264">[Use os recursos de depurador][DevToolsJavascriptReference] - Usando a interface do usuário do depurador na ferramenta Sources.</span><span class="sxs-lookup"><span data-stu-id="3f568-264">[Use the debugger features][DevToolsJavascriptReference] - Using the UI of the debugger in the Sources tool.</span></span>
*   <span data-ttu-id="3f568-265">[Visão geral da ferramenta Sources][DevToolsSourcesIndex] - Apresenta o depurador JavaScript e o editor de código.</span><span class="sxs-lookup"><span data-stu-id="3f568-265">[Sources tool overview][DevToolsSourcesIndex] - Introduces the JavaScript debugger and code editor.</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="3f568-266">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3f568-266">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptReference]: ./reference.md "Use os recursos de depurador | Microsoft Docs"  
[DevToolsSourcesIndex]: ../sources/index.md "Visão geral da ferramenta Sources | Microsoft Docs"  
[DevToolsJavscriptBreakpoints]: ./breakpoints.md "Como pausar seu código com pontos de interrupção Microsoft Edge DevTools | Microsoft Docs"
[DevToolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Código passo a passo - Use os recursos de depurador | Microsoft Docs"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Open Demo | Glitch"  

> [!NOTE]
> <span data-ttu-id="3f568-272">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3f568-272">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3f568-273">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="3f568-273">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3f568-275">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3f568-275">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
