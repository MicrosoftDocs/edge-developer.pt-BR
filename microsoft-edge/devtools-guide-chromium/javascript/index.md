---
description: Saiba como usar o Microsoft Edge DevTools para encontrar e corrigir bugs do JavaScript.
title: Começar a depurar JavaScript no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: b036fc87149d13446ab1bc05afc8fc8631d27c8d
ms.sourcegitcommit: e737277744dd25a7585c113eef22a2aa4d4c167f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "11325942"
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
# <span data-ttu-id="aa69c-104">Começar a depurar JavaScript no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="aa69c-104">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="aa69c-105">Este artigo ensina o fluxo de trabalho básico para depurar qualquer problema do JavaScript no DevTools.</span><span class="sxs-lookup"><span data-stu-id="aa69c-105">This article teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <span data-ttu-id="aa69c-106">Etapa 1: Reproduzir o bug</span><span class="sxs-lookup"><span data-stu-id="aa69c-106">Step 1: Reproduce the bug</span></span>  

<span data-ttu-id="aa69c-107">Encontrar uma série de ações que reproduzem consistentemente um bug é sempre a primeira etapa para a depuração.</span><span class="sxs-lookup"><span data-stu-id="aa69c-107">Finding a series of actions that consistently reproduce a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="aa69c-108">Escolha **Abrir Demonstração.**</span><span class="sxs-lookup"><span data-stu-id="aa69c-108">Choose **Open Demo**.</span></span>  <span data-ttu-id="aa69c-109">Segure `Control` \(Windows, Linux\) ou `Command` \(macOS\) e abra a demonstração em uma nova guia do navegador.</span><span class="sxs-lookup"><span data-stu-id="aa69c-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and open the demo in a new browser tab.</span></span>  
    
    [<span data-ttu-id="aa69c-110">Open Demo</span><span class="sxs-lookup"><span data-stu-id="aa69c-110">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="aa69c-111">Digite `5` a caixa de texto Número **1.**</span><span class="sxs-lookup"><span data-stu-id="aa69c-111">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="aa69c-112">Digite `1` a caixa de texto Número **2.**</span><span class="sxs-lookup"><span data-stu-id="aa69c-112">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="aa69c-113">Escolha **Adicionar Número 1 e Número 2.**</span><span class="sxs-lookup"><span data-stu-id="aa69c-113">Choose **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="aa69c-114">O rótulo abaixo do botão diz `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="aa69c-114">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="aa69c-115">O resultado deve ser `6` .</span><span class="sxs-lookup"><span data-stu-id="aa69c-115">The result should be `6`.</span></span>  <span data-ttu-id="aa69c-116">Em seguida, corrige o erro de adição que é o bug.</span><span class="sxs-lookup"><span data-stu-id="aa69c-116">Next, fix the addition error that is the bug.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 resulta em 51, mas deve ser 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` <span data-ttu-id="aa69c-118">resultados `51` em, mas deve ser</span><span class="sxs-lookup"><span data-stu-id="aa69c-118">results in `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <span data-ttu-id="aa69c-119">Etapa 2: familiarizar-se com a interface do usuário do painel fontes</span><span class="sxs-lookup"><span data-stu-id="aa69c-119">Step 2: Get familiar with the Sources panel UI</span></span>  

<span data-ttu-id="aa69c-120">O DevTools fornece várias ferramentas diferentes para tarefas diferentes.</span><span class="sxs-lookup"><span data-stu-id="aa69c-120">DevTools provides many different tools for different tasks.</span></span>  <span data-ttu-id="aa69c-121">Tarefas diferentes incluem alterar CSS, criação de perfil de desempenho de carga de página e monitoramento de solicitações de rede.</span><span class="sxs-lookup"><span data-stu-id="aa69c-121">Different tasks include changing CSS, profiling page-load performance, and monitoring network requests.</span></span>  <span data-ttu-id="aa69c-122">O **painel Fontes** é onde você depura JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aa69c-122">The **Sources** panel is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="aa69c-123">Abra o DevTools `Control` + `Shift` + `J` pressionando \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="aa69c-123">Open DevTools by pressing `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="aa69c-124">Esse atalho abre o **painel do** Console.</span><span class="sxs-lookup"><span data-stu-id="aa69c-124">This shortcut opens the **Console** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="O painel do Console" lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="aa69c-126">A **ferramenta Console**</span><span class="sxs-lookup"><span data-stu-id="aa69c-126">The **Console** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa69c-127">Escolha a **ferramenta** Fontes.</span><span class="sxs-lookup"><span data-stu-id="aa69c-127">Choose the **Sources** tool.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="O painel Fontes" lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="aa69c-129">O **painel Fontes**</span><span class="sxs-lookup"><span data-stu-id="aa69c-129">The **Sources** panel</span></span>  
    :::image-end:::  
    
<span data-ttu-id="aa69c-130">A **interface do** usuário do painel Fontes tem três partes.</span><span class="sxs-lookup"><span data-stu-id="aa69c-130">The **Sources** panel UI has three parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="As 3 partes da interface do usuário do painel Fontes" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="aa69c-132">As 3 partes da interface **do usuário do painel** Fontes</span><span class="sxs-lookup"><span data-stu-id="aa69c-132">The 3 parts of the **Sources** panel UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="aa69c-133">O **painel Navegador** de Arquivos \(Seção 1 na figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="aa69c-133">The **File Navigator** pane \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="aa69c-134">Todos os arquivos que a página da Web solicita estão listados aqui.</span><span class="sxs-lookup"><span data-stu-id="aa69c-134">Every file that the webpage requests is listed here.</span></span>  
1.  <span data-ttu-id="aa69c-135">O **painel Editor** de Código \(Seção 2 na figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="aa69c-135">The **Code Editor** pane \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="aa69c-136">Depois de selecionar um arquivo no painel **Navegador** de Arquivos, o conteúdo desse arquivo será exibido aqui.</span><span class="sxs-lookup"><span data-stu-id="aa69c-136">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="aa69c-137">O **painel Depuração** de JavaScript \(Seção 3 na figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="aa69c-137">The **JavaScript Debugging** pane \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="aa69c-138">Várias ferramentas para inspecionar o JavaScript para a página da Web.</span><span class="sxs-lookup"><span data-stu-id="aa69c-138">Various tools for inspecting the JavaScript for the webpage.</span></span>  <span data-ttu-id="aa69c-139">Se a janela DevTools for larga, esse painel será exibido à direita do painel **Editor de** Código.</span><span class="sxs-lookup"><span data-stu-id="aa69c-139">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  
    
## <span data-ttu-id="aa69c-140">Etapa 3: Pausar o código com um ponto de interrupção</span><span class="sxs-lookup"><span data-stu-id="aa69c-140">Step 3: Pause the code with a breakpoint</span></span>  

<span data-ttu-id="aa69c-141">Um método comum para depurar esse tipo de problema é inserir várias instruções no código e inspecionar valores à medida que `console.log()` o script é executado.</span><span class="sxs-lookup"><span data-stu-id="aa69c-141">A common method for debugging this type of problem is to insert several `console.log()` statements into the code and then to inspect values as the script runs.</span></span>  <span data-ttu-id="aa69c-142">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="aa69c-142">For example:</span></span>  

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

<span data-ttu-id="aa69c-143">O método pode fazer o trabalho, mas pontos de interrupção `console.log()` o fazer mais rapidamente. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="aa69c-143">The `console.log()` method may get the job done, but **breakpoints** get it done faster.</span></span>  <span data-ttu-id="aa69c-144">Um ponto de interrupção permite pausar seu código no meio do tempo de execução e examinar todos os valores nesse momento.</span><span class="sxs-lookup"><span data-stu-id="aa69c-144">A breakpoint lets you pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="aa69c-145">Pontos de interrupção têm algumas vantagens em relação ao `console.log()` método:</span><span class="sxs-lookup"><span data-stu-id="aa69c-145">Breakpoints have a few advantages over the `console.log()` method:</span></span>  

*   <span data-ttu-id="aa69c-146">With `console.log()` , you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.</span><span class="sxs-lookup"><span data-stu-id="aa69c-146">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.</span></span>  <span data-ttu-id="aa69c-147">Com pontos de interrupção, você pode pausar o código relevante sem saber como o código está estruturado.</span><span class="sxs-lookup"><span data-stu-id="aa69c-147">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="aa69c-148">Em suas `console.log()` instruções, você precisa especificar explicitamente cada valor que deseja inspecionar.</span><span class="sxs-lookup"><span data-stu-id="aa69c-148">In your `console.log()` statements, you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="aa69c-149">Com pontos de interrupção, o DevTools mostra os valores de todas as variáveis nesse momento.</span><span class="sxs-lookup"><span data-stu-id="aa69c-149">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="aa69c-150">Às vezes, as variáveis que afetam seu código são ocultas e ofuscados.</span><span class="sxs-lookup"><span data-stu-id="aa69c-150">Sometimes variables that affect your code are hidden and obfuscated.</span></span>  
    
<span data-ttu-id="aa69c-151">Em resumo, pontos de interrupção podem ajudá-lo a encontrar e corrigir bugs mais rapidamente do que o `console.log()` método.</span><span class="sxs-lookup"><span data-stu-id="aa69c-151">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="aa69c-152">Se voltar e pensar em como o aplicativo funciona, você pode fazer uma suposição instrucionada de que a soma incorreta \( \) é calculada no ouvinte de eventos associado ao botão Adicionar Número 1 e Número `5 + 1 = 51` `click` **2.**</span><span class="sxs-lookup"><span data-stu-id="aa69c-152">If you step back and think about how the app works, you may make an educated guess that the incorrect sum \(`5 + 1 = 51`\) is computed in the `click` event listener associated with the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="aa69c-153">Portanto, você provavelmente deseja pausar o código no horário em que o `click` ouvinte é executado.</span><span class="sxs-lookup"><span data-stu-id="aa69c-153">So, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="aa69c-154">**Os Pontos de Interrupção do Ouvinte de** Eventos permitem que você faça exatamente isso:</span><span class="sxs-lookup"><span data-stu-id="aa69c-154">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="aa69c-155">No painel **Depuração de JavaScript,** escolha Pontos de Interrupção do Ouvinte **de** Eventos para expandir a seção.</span><span class="sxs-lookup"><span data-stu-id="aa69c-155">In the **JavaScript Debugging** pane, choose **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="aa69c-156">O DevTools revela uma lista de categorias de eventos expansíveis, como **Animação e** **Área de Transferência.**</span><span class="sxs-lookup"><span data-stu-id="aa69c-156">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="aa69c-157">Ao lado da categoria de evento **Mouse,** escolha **Expandir** \( ![ ícone Expandir ][ImageExpandIcon] \).</span><span class="sxs-lookup"><span data-stu-id="aa69c-157">Next to the **Mouse** event category, choose **Expand** \(![Expand icon][ImageExpandIcon]\).</span></span>  <span data-ttu-id="aa69c-158">O DevTools revela uma lista de eventos do mouse, como **clique** e **mouse para baixo.**</span><span class="sxs-lookup"><span data-stu-id="aa69c-158">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="aa69c-159">Cada evento tem uma caixa de seleção ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="aa69c-159">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="aa69c-160">Escolha a caixa de seleção ao lado de **clicar.**</span><span class="sxs-lookup"><span data-stu-id="aa69c-160">Choose the checkbox next to **click**.</span></span>  <span data-ttu-id="aa69c-161">O DevTools agora está definido para pausar automaticamente quando qualquer `click` ouvinte de eventos for executado.</span><span class="sxs-lookup"><span data-stu-id="aa69c-161">DevTools is now set up to automatically pause when any `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Escolha a caixa de seleção ao lado de clicar" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="aa69c-163">Escolha a caixa de seleção ao lado de **clicar**</span><span class="sxs-lookup"><span data-stu-id="aa69c-163">Choose the checkbox next to **click**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="aa69c-164">Novamente na demonstração, escolha **Adicionar Número 1 e Número 2** novamente.</span><span class="sxs-lookup"><span data-stu-id="aa69c-164">Back on the demo, choose **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="aa69c-165">O DevTools pausa a demonstração e realça uma linha de código no **painel** Fontes.</span><span class="sxs-lookup"><span data-stu-id="aa69c-165">DevTools pauses the demo and highlights a line of code in the **Sources** panel.</span></span>  <span data-ttu-id="aa69c-166">DevTools deve pausar na linha 16 em `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="aa69c-166">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="aa69c-167">Se você pausar em uma linha de código diferente, pressione **Resume Script Execution** \( Resume Script Execution ![ ][ImageResumeIcon] \) até pausar na linha correta.</span><span class="sxs-lookup"><span data-stu-id="aa69c-167">If you pause on a different line of code, press **Resume Script Execution** \(![Resume Script Execution][ImageResumeIcon]\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="aa69c-168">Se você tiver pausado em uma linha diferente, terá uma extensão de navegador que registra um ouvinte de eventos em cada página `click` da Web visitada.</span><span class="sxs-lookup"><span data-stu-id="aa69c-168">If you paused on a different line, you have a browser extension that registers a `click` event listener on every webpage that you visit.</span></span>  <span data-ttu-id="aa69c-169">Você foi pausado no `click` ouvinte da extensão.</span><span class="sxs-lookup"><span data-stu-id="aa69c-169">You were paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="aa69c-170">Se você usar o Modo \*\*\*\* InPrivate para navegar em particular, o que desabilita todas as extensões, você poderá ver que pausa na linha de código desejada sempre.</span><span class="sxs-lookup"><span data-stu-id="aa69c-170">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="aa69c-171">**Os Pontos de Interrupção do** Ouvinte de Eventos são apenas um dos vários tipos de pontos de interrupção disponíveis no DevTools.</span><span class="sxs-lookup"><span data-stu-id="aa69c-171">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="aa69c-172">Memorize todos os tipos diferentes para ajudá-lo a depurar cenários diferentes o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="aa69c-172">Memorize all the different types to help you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <span data-ttu-id="aa69c-173">Etapa 4: Passar pelo código</span><span class="sxs-lookup"><span data-stu-id="aa69c-173">Step 4: Step through the code</span></span>  

<span data-ttu-id="aa69c-174">Uma causa comum de bugs é quando um script é executado na ordem errada.</span><span class="sxs-lookup"><span data-stu-id="aa69c-174">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="aa69c-175">Passar pelo código permite que você ande pelo tempo de execução do seu código.</span><span class="sxs-lookup"><span data-stu-id="aa69c-175">Stepping through your code allows you to walk through the runtime of your code.</span></span>  <span data-ttu-id="aa69c-176">Você passa por uma linha por vez para ajudá-lo a descobrir exatamente onde seu código está sendo executado em uma ordem diferente do esperado.</span><span class="sxs-lookup"><span data-stu-id="aa69c-176">You walk through one line at a time to help you figure out exactly where your code is running in a different order than you expect.</span></span>  <span data-ttu-id="aa69c-177">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="aa69c-177">Try it now:</span></span>  

1.  <span data-ttu-id="aa69c-178">Choose **Step over next function call** \( Step over next function call ![ ][ImageOverIcon] \).</span><span class="sxs-lookup"><span data-stu-id="aa69c-178">Choose **Step over next function call** \(![Step over next function call][ImageOverIcon]\).</span></span>  <span data-ttu-id="aa69c-179">O DevTools executa o código a seguir sem entrar nele.</span><span class="sxs-lookup"><span data-stu-id="aa69c-179">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="aa69c-180">O DevTools ignora algumas linhas de código.</span><span class="sxs-lookup"><span data-stu-id="aa69c-180">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="aa69c-181">Isso porque é `inputsAreEmpty()` avaliada como false, portanto, o bloco de código para a `if` instrução não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa69c-181">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="aa69c-182">No painel **Fontes** do DevTools, escolha Step **into next function call** \( Step into next function call \) para passar pelo tempo de execução da função, uma linha ![ por ][ImageIntoIcon] `updateLabel()` vez.</span><span class="sxs-lookup"><span data-stu-id="aa69c-182">On the **Sources** panel of DevTools, choose **Step into next function call** \(![Step into next function call][ImageIntoIcon]\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="aa69c-183">Revisar uma linha por vez é a ideia básica de passar pelo código.</span><span class="sxs-lookup"><span data-stu-id="aa69c-183">Reviewing one line at a time is the basic idea of stepping through code.</span></span>  <span data-ttu-id="aa69c-184">Se você olhar para o `get-started.js` código, verá que o bug provavelmente está em algum lugar na `updateLabel()` função.</span><span class="sxs-lookup"><span data-stu-id="aa69c-184">If you look at the code in `get-started.js`, you see that the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="aa69c-185">Em vez de passar por cada linha de código, você pode usar outro tipo de ponto de interrupção para pausar o código mais próximo da localização provável do bug.</span><span class="sxs-lookup"><span data-stu-id="aa69c-185">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <span data-ttu-id="aa69c-186">Etapa 5: Definir um ponto de interrupção de linha de código</span><span class="sxs-lookup"><span data-stu-id="aa69c-186">Step 5: Set a line-of-code breakpoint</span></span>  

<span data-ttu-id="aa69c-187">Os pontos de interrupção de linha de código são o tipo mais comum de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="aa69c-187">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="aa69c-188">Quando você chegar à linha de código específica que deseja pausar, use um ponto de interrupção de linha de código.</span><span class="sxs-lookup"><span data-stu-id="aa69c-188">When you get to the specific line of code you want to pause, use a line-of-code breakpoint.</span></span>  

1.  <span data-ttu-id="aa69c-189">Veja a última linha de código `updateLabel()` em:</span><span class="sxs-lookup"><span data-stu-id="aa69c-189">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="aa69c-190">À esquerda, o número dessa linha específica de código é exibido como **34**.</span><span class="sxs-lookup"><span data-stu-id="aa69c-190">On the left, the number of this particular line of code is displayed as **34**.</span></span>  <span data-ttu-id="aa69c-191">Escolha a **linha 34.**</span><span class="sxs-lookup"><span data-stu-id="aa69c-191">Choose line **34**.</span></span>  <span data-ttu-id="aa69c-192">O DevTools coloca um ícone vermelho à esquerda de **34**.</span><span class="sxs-lookup"><span data-stu-id="aa69c-192">DevTools puts a red icon to the left of **34**.</span></span>  <span data-ttu-id="aa69c-193">O ícone vermelho indica que um ponto de interrupção de linha de código está nessa linha.</span><span class="sxs-lookup"><span data-stu-id="aa69c-193">The red icon indicates that a line-of-code breakpoint is on this line.</span></span>  <span data-ttu-id="aa69c-194">O DevTools sempre pausa antes que essa linha de código seja executado.</span><span class="sxs-lookup"><span data-stu-id="aa69c-194">DevTools always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="aa69c-195">Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="aa69c-195">Choose **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  <span data-ttu-id="aa69c-196">O script continua em execução até atingir a linha 33.</span><span class="sxs-lookup"><span data-stu-id="aa69c-196">The script continues running until it reaches line 33.</span></span>  <span data-ttu-id="aa69c-197">Nas linhas 31, 32 e 33, o DevTools imprime os valores de , e à direita dos pontos e vírgulas em `addend1` `addend2` cada `sum` linha.</span><span class="sxs-lookup"><span data-stu-id="aa69c-197">On lines 31, 32, and 33, DevTools prints the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="O DevTools pausa no ponto de interrupção de linha de código na linha 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="aa69c-199">O DevTools pausa no ponto de interrupção de linha de código na linha 34</span><span class="sxs-lookup"><span data-stu-id="aa69c-199">DevTools pauses on the line-of-code breakpoint on line 34</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="aa69c-200">Etapa 6: Verificar valores variáveis</span><span class="sxs-lookup"><span data-stu-id="aa69c-200">Step 6: Check variable values</span></span>  

<span data-ttu-id="aa69c-201">Os valores `addend1` de , e parecem `addend2` `sum` suspeitos.</span><span class="sxs-lookup"><span data-stu-id="aa69c-201">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="aa69c-202">Os valores são entre aspas.</span><span class="sxs-lookup"><span data-stu-id="aa69c-202">The values are wrapped in quotes.</span></span>  <span data-ttu-id="aa69c-203">As aspas significam que o valor é uma cadeia de caracteres, o que é uma boa hipótese para explicar a causa do bug.</span><span class="sxs-lookup"><span data-stu-id="aa69c-203">The quotations mean that the value is a string, which is a good hypothesis to explain the cause of the bug.</span></span>  <span data-ttu-id="aa69c-204">Reúna mais informações sobre a situação.</span><span class="sxs-lookup"><span data-stu-id="aa69c-204">Gather more information about the situation.</span></span>  <span data-ttu-id="aa69c-205">O DevTools fornece muitas ferramentas para examinar valores variáveis.</span><span class="sxs-lookup"><span data-stu-id="aa69c-205">DevTools provides many tools for examining variable values.</span></span>  

### <span data-ttu-id="aa69c-206">Método 1: O painel Escopo</span><span class="sxs-lookup"><span data-stu-id="aa69c-206">Method 1: The Scope pane</span></span>  

<span data-ttu-id="aa69c-207">Se você pausar em uma \*\*\*\* linha de código, o painel Escopo exibirá as variáveis locais e globais definidas no momento, juntamente com o valor de cada variável.</span><span class="sxs-lookup"><span data-stu-id="aa69c-207">If you pause on a line of code, the **Scope** pane displays the local and global variables that are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="aa69c-208">Ele também exibe variáveis de fechamento, conforme aplicável.</span><span class="sxs-lookup"><span data-stu-id="aa69c-208">It also displays closure variables, as applicable.</span></span>  <span data-ttu-id="aa69c-209">Clique duas vezes em um valor variável para editá-lo.</span><span class="sxs-lookup"><span data-stu-id="aa69c-209">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="aa69c-210">Se você não pausar em uma linha de código, **o** painel Escopo será vazio.</span><span class="sxs-lookup"><span data-stu-id="aa69c-210">If you don't pause on a line of code, the **Scope** pane is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="O painel Escopo" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="aa69c-212">O **painel** Escopo</span><span class="sxs-lookup"><span data-stu-id="aa69c-212">The **Scope** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="aa69c-213">Método 2: Expressões de relógio</span><span class="sxs-lookup"><span data-stu-id="aa69c-213">Method 2: Watch Expressions</span></span>  

<span data-ttu-id="aa69c-214">O **painel Expressões** de Relógio permite monitorar os valores das variáveis ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="aa69c-214">The **Watch Expressions** pane lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="aa69c-215">Como o nome sugere, **as expressões de relógio** não são limitadas a variáveis.</span><span class="sxs-lookup"><span data-stu-id="aa69c-215">As the name implies, **Watch Expressions** aren't limited to variables.</span></span>  <span data-ttu-id="aa69c-216">Você pode armazenar qualquer expressão JavaScript válida em uma **expressão de relógio.**</span><span class="sxs-lookup"><span data-stu-id="aa69c-216">You may store any valid JavaScript expression in a **Watch Expression**.</span></span>  <span data-ttu-id="aa69c-217">Experimente agora.</span><span class="sxs-lookup"><span data-stu-id="aa69c-217">Try it now.</span></span>  

1.  <span data-ttu-id="aa69c-218">Escolha o **painel** de relógio.</span><span class="sxs-lookup"><span data-stu-id="aa69c-218">Choose the **Watch** pane.</span></span>  
1.  <span data-ttu-id="aa69c-219">Escolha **Adicionar expressão** \( Adicionar expressão ![ ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="aa69c-219">Choose **Add Expression** \(![Add Expression][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="aa69c-220">Digite `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="aa69c-220">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="aa69c-221">Selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="aa69c-221">Select `Enter`.</span></span>  <span data-ttu-id="aa69c-222">O DevTools mostra `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="aa69c-222">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="aa69c-223">O valor à direita dos dois-pontos é o resultado de sua expressão de relógio.</span><span class="sxs-lookup"><span data-stu-id="aa69c-223">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="aa69c-224">No painel **expressão** de relógio \(inferior direito\) na figura a seguir, a expressão `typeof sum` de relógio é exibida.</span><span class="sxs-lookup"><span data-stu-id="aa69c-224">In the **Watch Expression** pane \(bottom-right\) in the following figure, the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="aa69c-225">Se a janela DevTools for grande, o painel **DevTools** fica à direita acima do painel Pontos de Interrupção do Ouvinte **de** Eventos.</span><span class="sxs-lookup"><span data-stu-id="aa69c-225">If your DevTools window is large, the **Watch Expression** pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="O painel Expressão de Relógio" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="aa69c-227">O **painel Expressão** de Relógio</span><span class="sxs-lookup"><span data-stu-id="aa69c-227">The **Watch Expression** pane</span></span>  
:::image-end:::  

<span data-ttu-id="aa69c-228">Como suspeito, `sum` está sendo avaliado como uma cadeia de caracteres, quando deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="aa69c-228">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="aa69c-229">Você agora confirma que o tipo de valor é a causa do bug.</span><span class="sxs-lookup"><span data-stu-id="aa69c-229">You now confirmed value type is the cause of the bug.</span></span>  

### <span data-ttu-id="aa69c-230">Método 3: O console</span><span class="sxs-lookup"><span data-stu-id="aa69c-230">Method 3: The Console</span></span>  

<span data-ttu-id="aa69c-231">O **Console** permite exibir mensagens e você também pode usá-lo para avaliar `console.log()` instruções JavaScript arbitrárias.</span><span class="sxs-lookup"><span data-stu-id="aa69c-231">The **Console** allows you to view `console.log()` messages and you may also use it to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="aa69c-232">Para depuração, você pode usar o **Console** para testar possíveis correções de bugs.</span><span class="sxs-lookup"><span data-stu-id="aa69c-232">For debugging, you may use the **Console** to test potential fixes for bugs.</span></span>  <span data-ttu-id="aa69c-233">Experimente agora.</span><span class="sxs-lookup"><span data-stu-id="aa69c-233">Try it now.</span></span>  

1.  <span data-ttu-id="aa69c-234">Se a **gaveta do Console** estiver fechada, selecione para `Escape` abri-la.</span><span class="sxs-lookup"><span data-stu-id="aa69c-234">If the **Console** drawer is closed, select `Escape` to open it.</span></span>  <span data-ttu-id="aa69c-235">A **gaveta console** é aberta no painel inferior da janela DevTools.</span><span class="sxs-lookup"><span data-stu-id="aa69c-235">The **Console** drawer opens in the lower panel of the DevTools window.</span></span>  
1.  <span data-ttu-id="aa69c-236">No **Console,** digite `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="aa69c-236">In the **Console**, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="aa69c-237">A instrução em que a ferramenta está pausada em uma linha de código onde `addend1` `addend2` está no escopo.</span><span class="sxs-lookup"><span data-stu-id="aa69c-237">The statement the tool is paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="aa69c-238">Selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="aa69c-238">Select `Enter`.</span></span>  <span data-ttu-id="aa69c-239">DevTools avalia a instrução e imprime `6` , que é o resultado que você espera que a demonstração produza.</span><span class="sxs-lookup"><span data-stu-id="aa69c-239">DevTools evaluates the statement and prints `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="A gaveta console, depois de avaliar parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="aa69c-241">A **gaveta console,** depois de avaliar</span><span class="sxs-lookup"><span data-stu-id="aa69c-241">The **Console** drawer, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <span data-ttu-id="aa69c-242">Etapa 7: Aplicar uma correção</span><span class="sxs-lookup"><span data-stu-id="aa69c-242">Step 7: Apply a fix</span></span>  

<span data-ttu-id="aa69c-243">Se você encontrar uma correção para o bug, experimente a correção editando o código e reruindo a demonstração.</span><span class="sxs-lookup"><span data-stu-id="aa69c-243">If you find a fix for the bug, try out your fix by editing the code and rerunning the demo.</span></span>  <span data-ttu-id="aa69c-244">Você pode editar o código JavaScript diretamente na interface do usuário do DevTools e aplicar a correção.</span><span class="sxs-lookup"><span data-stu-id="aa69c-244">You may edit JavaScript code directly within the DevTools UI and apply the fix.</span></span>  <span data-ttu-id="aa69c-245">Experimente agora.</span><span class="sxs-lookup"><span data-stu-id="aa69c-245">Try it now.</span></span>  

1.  <span data-ttu-id="aa69c-246">Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="aa69c-246">Choose **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  
1.  <span data-ttu-id="aa69c-247">No **Editor de Código,** substitua a linha 32, `var sum = addend1 + addend2` por `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="aa69c-247">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="aa69c-248">Selecione `Control` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\) para salvar a alteração.</span><span class="sxs-lookup"><span data-stu-id="aa69c-248">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="aa69c-249">Choose **Deactivate breakpoints** \( ![ Deactivate breakpoints ][ImageDeactivateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="aa69c-249">Choose **Deactivate breakpoints** \(![Deactivate breakpoints][ImageDeactivateIcon]\).</span></span>  <span data-ttu-id="aa69c-250">Ele muda azul para indicar que a opção está ativa.</span><span class="sxs-lookup"><span data-stu-id="aa69c-250">It changes blue to indicate the option is active.</span></span>  <span data-ttu-id="aa69c-251">Enquanto **desativa pontos de interrupção definidos,** o DevTools ignora todos os pontos de interrupção que você definir.</span><span class="sxs-lookup"><span data-stu-id="aa69c-251">While **Deactivate breakpoints** is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="aa69c-252">Experimente a demonstração com valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="aa69c-252">Try out the demo with different values.</span></span>  <span data-ttu-id="aa69c-253">A demonstração agora calcula corretamente.</span><span class="sxs-lookup"><span data-stu-id="aa69c-253">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="aa69c-254">Esse fluxo de trabalho aplica apenas uma correção ao código que está sendo executado no navegador.</span><span class="sxs-lookup"><span data-stu-id="aa69c-254">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="aa69c-255">Ele não corrige o código para todos os usuários que visitam sua página da Web.</span><span class="sxs-lookup"><span data-stu-id="aa69c-255">It does not fix the code for all users that visit your webpage.</span></span>  <span data-ttu-id="aa69c-256">Para fazer isso, você precisa corrigir o código que está em seus servidores.</span><span class="sxs-lookup"><span data-stu-id="aa69c-256">To do that, you need to fix the code that is on your servers.</span></span>  

## <span data-ttu-id="aa69c-257">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="aa69c-257">Next steps</span></span>  

<span data-ttu-id="aa69c-258">Parabéns!</span><span class="sxs-lookup"><span data-stu-id="aa69c-258">Congratulations!</span></span>  <span data-ttu-id="aa69c-259">Agora você sabe como fazer o máximo do Microsoft Edge DevTools ao depurar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aa69c-259">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="aa69c-260">As ferramentas e os métodos que você aprendeu neste artigo podem poupar-lhe inúmeras horas.</span><span class="sxs-lookup"><span data-stu-id="aa69c-260">The tools and methods you learned in this article may save you countless hours.</span></span>  

<span data-ttu-id="aa69c-261">Este artigo ensinava apenas duas maneiras de definir pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="aa69c-261">This article only taught you two ways to set breakpoints.</span></span>  <span data-ttu-id="aa69c-262">O DevTools oferece muitas outras maneiras, incluindo as configurações a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa69c-262">DevTools offers many other ways including the following settings.</span></span>  

*   <span data-ttu-id="aa69c-263">Pontos de interrupção condicionais que só são disparados quando a condição que você fornece é verdadeira.</span><span class="sxs-lookup"><span data-stu-id="aa69c-263">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="aa69c-264">Pontos de interrupção em exceções capturadas ou não capturadas.</span><span class="sxs-lookup"><span data-stu-id="aa69c-264">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="aa69c-265">Pontos de interrupção XHR que são disparados quando a URL solicitada corresponde a uma substring que você fornece.</span><span class="sxs-lookup"><span data-stu-id="aa69c-265">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="aa69c-266">Para obter mais informações sobre quando e como usar cada tipo, navegue até [Pausar seu código com pontos de interrupção.][DevtoolsJavscriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="aa69c-266">For more information about when and how to use each type, navigate to [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="aa69c-267">Alguns controles de passo a passo de código não são explicados neste artigo.</span><span class="sxs-lookup"><span data-stu-id="aa69c-267">A couple of code stepping controls aren't explained in this article.</span></span>  <span data-ttu-id="aa69c-268">Para obter mais informações, [navegue até a linha de código Step over.][DevtoolsJavascriptReferenceStepThroughCode]</span><span class="sxs-lookup"><span data-stu-id="aa69c-268">For more information, navigate to [Step over line of code][DevtoolsJavascriptReferenceStepThroughCode].</span></span>  

## <span data-ttu-id="aa69c-269">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="aa69c-269">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Abrir demonstração | Falha"  

> [!NOTE]
> <span data-ttu-id="aa69c-273">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aa69c-273">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="aa69c-274">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Meio\).</span><span class="sxs-lookup"><span data-stu-id="aa69c-274">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="aa69c-276">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aa69c-276">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
