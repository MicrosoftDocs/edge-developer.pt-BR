---
title: Introdução à depuração de JavaScript no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 204d3033b65f82c6160a0d2c41a15d8eb62b4530
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982827"
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







# <span data-ttu-id="4de8a-103">Introdução à depuração de JavaScript no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4de8a-103">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>   



<span data-ttu-id="4de8a-104">Este tutorial ensina o fluxo de trabalho básico para a depuração de qualquer problema de JavaScript no DevTools.</span><span class="sxs-lookup"><span data-stu-id="4de8a-104">This tutorial teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <span data-ttu-id="4de8a-105">Etapa 1: reproduzir o bug</span><span class="sxs-lookup"><span data-stu-id="4de8a-105">Step 1: Reproduce the bug</span></span>   

<span data-ttu-id="4de8a-106">Encontrar uma série de ações que reproduzem um bug consistentemente é sempre a primeira etapa da depuração.</span><span class="sxs-lookup"><span data-stu-id="4de8a-106">Finding a series of actions that consistently reproduces a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="4de8a-107">Clique em **abrir demonstração**.</span><span class="sxs-lookup"><span data-stu-id="4de8a-107">Click **Open Demo**.</span></span>  <span data-ttu-id="4de8a-108">Segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e abra a demonstração em uma nova guia.</span><span class="sxs-lookup"><span data-stu-id="4de8a-108">Hold `Control` \(Windows\) or `Command` \(macOS\) and open the demo in a new tab.</span></span>  
    
    [<span data-ttu-id="4de8a-109">Abrir demonstração</span><span class="sxs-lookup"><span data-stu-id="4de8a-109">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="4de8a-110">Digite `5` na caixa de texto **número 1** .</span><span class="sxs-lookup"><span data-stu-id="4de8a-110">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="4de8a-111">Digite `1` na caixa de texto **número 2** .</span><span class="sxs-lookup"><span data-stu-id="4de8a-111">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="4de8a-112">Clique em **Adicionar número 1 e número 2**.</span><span class="sxs-lookup"><span data-stu-id="4de8a-112">Click **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="4de8a-113">A etiqueta abaixo do botão diz `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="4de8a-113">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="4de8a-114">O resultado deve ser `6` .</span><span class="sxs-lookup"><span data-stu-id="4de8a-114">The result should be `6`.</span></span>  <span data-ttu-id="4de8a-115">Esse é o bug que você vai corrigir.</span><span class="sxs-lookup"><span data-stu-id="4de8a-115">This is the bug you are going to fix.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="O resultado de 5 + 1 é 51, mas deve ser 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       <span data-ttu-id="4de8a-117">O resultado de `5 + 1` é `51` , mas deve ser</span><span class="sxs-lookup"><span data-stu-id="4de8a-117">The result of `5 + 1` is `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <span data-ttu-id="4de8a-118">Etapa 2: Familiarize-se com a interface do usuário do painel fontes</span><span class="sxs-lookup"><span data-stu-id="4de8a-118">Step 2: Get familiar with the Sources panel UI</span></span>   

<span data-ttu-id="4de8a-119">O DevTools oferece muitas ferramentas diferentes para tarefas diferentes, como a alteração de CSS, o profiling do desempenho da carga da página e o monitoramento de solicitações de rede.</span><span class="sxs-lookup"><span data-stu-id="4de8a-119">DevTools provides a lot of different tools for different tasks, such as changing CSS, profiling page load performance, and monitoring network requests.</span></span>  <span data-ttu-id="4de8a-120">O painel **fontes** é onde você depura o JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4de8a-120">The **Sources** panel is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="4de8a-121">Para abrir o devtools, pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="4de8a-121">Open DevTools by pressing `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) .</span></span>  <span data-ttu-id="4de8a-122">Esse atalho abre o painel do **console** .</span><span class="sxs-lookup"><span data-stu-id="4de8a-122">This shortcut opens the **Console** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Painel do console" lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="4de8a-124">Painel do **console**</span><span class="sxs-lookup"><span data-stu-id="4de8a-124">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4de8a-125">Clique na guia **fontes** .</span><span class="sxs-lookup"><span data-stu-id="4de8a-125">Click the **Sources** tab.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="O painel fontes" lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="4de8a-127">O painel **fontes**</span><span class="sxs-lookup"><span data-stu-id="4de8a-127">The **Sources** panel</span></span>  
    :::image-end:::  
    
<span data-ttu-id="4de8a-128">A interface do usuário do painel **fontes** tem 3 partes.</span><span class="sxs-lookup"><span data-stu-id="4de8a-128">The **Sources** panel UI has 3 parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="As 3 partes da interface do usuário do painel fontes" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="4de8a-130">As 3 partes da interface do usuário do painel **fontes**</span><span class="sxs-lookup"><span data-stu-id="4de8a-130">The 3 parts of the **Sources** panel UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="4de8a-131">O painel do **navegador de arquivos** \ (seção 1 na figura anterior \).</span><span class="sxs-lookup"><span data-stu-id="4de8a-131">The **File Navigator** pane \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="4de8a-132">Cada arquivo que as solicitações de página está listado aqui.</span><span class="sxs-lookup"><span data-stu-id="4de8a-132">Every file that the page requests is listed here.</span></span>  
1.  <span data-ttu-id="4de8a-133">O painel **Editor de código** \ (seção 2 na figura anterior \).</span><span class="sxs-lookup"><span data-stu-id="4de8a-133">The **Code Editor** pane \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="4de8a-134">Depois de selecionar um arquivo no painel do **navegador de arquivos** , o conteúdo desse arquivo é exibido aqui.</span><span class="sxs-lookup"><span data-stu-id="4de8a-134">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="4de8a-135">O painel de **depuração JavaScript** \ (seção 3 na figura anterior \).</span><span class="sxs-lookup"><span data-stu-id="4de8a-135">The **JavaScript Debugging** pane \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="4de8a-136">Várias ferramentas para inspecionar o JavaScript para a página.</span><span class="sxs-lookup"><span data-stu-id="4de8a-136">Various tools for inspecting the JavaScript for the page.</span></span>  <span data-ttu-id="4de8a-137">Se a janela do DevTools for ampla, esse painel será exibido à direita do painel do **Editor de código** .</span><span class="sxs-lookup"><span data-stu-id="4de8a-137">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  
    
## <span data-ttu-id="4de8a-138">Etapa 3: pausar o código com um ponto de interrupção</span><span class="sxs-lookup"><span data-stu-id="4de8a-138">Step 3: Pause the code with a breakpoint</span></span>   

<span data-ttu-id="4de8a-139">Um método comum para depurar um problema como este é inserir muitas `console.log()` instruções no código, para inspecionar valores conforme o script é executado.</span><span class="sxs-lookup"><span data-stu-id="4de8a-139">A common method for debugging a problem like this is to insert a lot of `console.log()` statements into the code, in order to inspect values as the script runs.</span></span>  <span data-ttu-id="4de8a-140">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="4de8a-140">For example:</span></span>  

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

<span data-ttu-id="4de8a-141">O `console.log()` método pode executar o trabalho, mas os **pontos de interrupção** são capazes de fazer uma realização mais rápida.</span><span class="sxs-lookup"><span data-stu-id="4de8a-141">The `console.log()` method may get the job done, but **breakpoints** are able to get it done faster.</span></span>  <span data-ttu-id="4de8a-142">Um ponto de interrupção permite pausar seu código no meio do tempo de execução e examinar todos os valores nesse momento.</span><span class="sxs-lookup"><span data-stu-id="4de8a-142">A breakpoint lets you pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="4de8a-143">Os pontos de interrupção têm algumas vantagens sobre o `console.log()` método:</span><span class="sxs-lookup"><span data-stu-id="4de8a-143">Breakpoints have a few advantages over the `console.log()` method:</span></span>  

*   <span data-ttu-id="4de8a-144">Com o `console.log()` , você precisa abrir manualmente o código-fonte, encontrar o código relevante, inserir as `console.log()` instruções e, em seguida, recarregar a página para ver as mensagens no console.</span><span class="sxs-lookup"><span data-stu-id="4de8a-144">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then reload the page in order to see the messages in the Console.</span></span>  <span data-ttu-id="4de8a-145">Com pontos de interrupção, você pode pausar no código relevante sem mesmo saber como o código está estruturado.</span><span class="sxs-lookup"><span data-stu-id="4de8a-145">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="4de8a-146">Em suas `console.log()` instruções, você precisa especificar explicitamente cada valor que você deseja inspecionar.</span><span class="sxs-lookup"><span data-stu-id="4de8a-146">In your `console.log()` statements you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="4de8a-147">Com pontos de interrupção, o DevTools mostra os valores de todas as variáveis nesse momento.</span><span class="sxs-lookup"><span data-stu-id="4de8a-147">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="4de8a-148">Às vezes, há variáveis que afetam seu código que você ainda não conhece.</span><span class="sxs-lookup"><span data-stu-id="4de8a-148">Sometimes there are variables affecting your code that you are not even aware of.</span></span>  

<span data-ttu-id="4de8a-149">Em resumo, os pontos de interrupção podem ajudá-lo a encontrar e corrigir bugs mais rápido do que o `console.log()` método.</span><span class="sxs-lookup"><span data-stu-id="4de8a-149">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="4de8a-150">Se você retomar uma etapa e pensar sobre como o aplicativo funciona, você poderá fazer uma estimativa de que a soma incorreta ( `5 + 1 = 51` ) é calculada no `click` ouvinte de eventos associado ao botão **Adicionar número 1 e número 2** .</span><span class="sxs-lookup"><span data-stu-id="4de8a-150">If you take a step back and think about how the app works, you are able to make an educated guess that the incorrect sum (`5 + 1 = 51`) gets computed in the `click` event listener that is associated to the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="4de8a-151">Portanto, você provavelmente desejará pausar o código no momento em que o `click` ouvinte for executado.</span><span class="sxs-lookup"><span data-stu-id="4de8a-151">Therefore, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="4de8a-152">Os **pontos de interrupção do ouvinte de eventos** permitem que você faça exatamente isso:</span><span class="sxs-lookup"><span data-stu-id="4de8a-152">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="4de8a-153">No painel **depuração de JavaScript** , clique em **pontos de interrupção de ouvinte de eventos** para expandir a seção.</span><span class="sxs-lookup"><span data-stu-id="4de8a-153">In the **JavaScript Debugging** pane, click **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="4de8a-154">O DevTools revela uma lista de categorias de eventos expansíveis, como **animação** e **área de transferência**.</span><span class="sxs-lookup"><span data-stu-id="4de8a-154">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="4de8a-155">Ao lado da categoria de evento **do mouse** , clique em **expandir** \ ( ![ expandir ícone ][ImageExpandIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4de8a-155">Next to the **Mouse** event category, click **Expand** \(![Expand icon][ImageExpandIcon]\).</span></span>  <span data-ttu-id="4de8a-156">O DevTools revela uma lista de eventos de mouse, como **clique** e **MouseDown**.</span><span class="sxs-lookup"><span data-stu-id="4de8a-156">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="4de8a-157">Cada evento tem uma caixa de seleção ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="4de8a-157">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="4de8a-158">Marque a caixa de seleção **clique** .</span><span class="sxs-lookup"><span data-stu-id="4de8a-158">Check the **click** checkbox.</span></span>  <span data-ttu-id="4de8a-159">O DevTools agora está configurado para pausar automaticamente quando *um* `click` ouvinte de evento é executado.</span><span class="sxs-lookup"><span data-stu-id="4de8a-159">DevTools is now set up to automatically pause when *any* `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="A caixa de seleção clicar está habilitada" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="4de8a-161">A caixa de seleção **clicar** está habilitada</span><span class="sxs-lookup"><span data-stu-id="4de8a-161">The **click** checkbox is enabled</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4de8a-162">De volta à demonstração, clique em **Adicionar número 1 e número 2** novamente.</span><span class="sxs-lookup"><span data-stu-id="4de8a-162">Back on the demo, click **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="4de8a-163">DevTools pausará a demonstração e realçará uma linha de código no painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="4de8a-163">DevTools pauses the demo and highlights a line of code in the **Sources** panel.</span></span>  <span data-ttu-id="4de8a-164">DevTools deve pausar na linha 16 `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="4de8a-164">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="4de8a-165">Se você pausar em uma linha de código diferente, pressione **retomar a execução do script** \ ( ![ retome a execução ][ImageResumeIcon] do script \) até que você pause na linha correta.</span><span class="sxs-lookup"><span data-stu-id="4de8a-165">If you pause on a different line of code, press **Resume Script Execution** \(![Resume Script Execution][ImageResumeIcon]\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="4de8a-166">Se você pausar em uma linha diferente, você tem uma extensão de navegador que registra um `click` ouvinte de eventos em cada página que você visita.</span><span class="sxs-lookup"><span data-stu-id="4de8a-166">If you paused on a different line, you have a browser extension that registers a `click` event listener on every page that you visit.</span></span>  <span data-ttu-id="4de8a-167">Você foi pausado no `click` ouvinte da extensão.</span><span class="sxs-lookup"><span data-stu-id="4de8a-167">You were paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="4de8a-168">Se você usar o modo InPrivate para **navegar em particular**, o que desabilita todas as extensões, poderá ver que você pausará na linha de código desejada a cada vez.</span><span class="sxs-lookup"><span data-stu-id="4de8a-168">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="4de8a-169">Os **pontos de interrupção do ouvinte de eventos** são apenas um dos muitos tipos de pontos de interrupção disponíveis no devtools.</span><span class="sxs-lookup"><span data-stu-id="4de8a-169">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="4de8a-170">Vale a pena memorizar todos os diferentes tipos, porque cada tipo acaba ajudando a depurar diferentes cenários o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="4de8a-170">It is worth memorizing all the different types, because each type ultimately helps you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <span data-ttu-id="4de8a-171">Etapa 4: percorrer o código</span><span class="sxs-lookup"><span data-stu-id="4de8a-171">Step 4: Step through the code</span></span>   

<span data-ttu-id="4de8a-172">Uma causa comum de erros é quando um script é executado na ordem errada.</span><span class="sxs-lookup"><span data-stu-id="4de8a-172">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="4de8a-173">Percorrer o código permite percorrer o tempo de execução do seu código, uma linha por vez e descobrir exatamente onde ele está sendo executado em uma ordem diferente do esperado.</span><span class="sxs-lookup"><span data-stu-id="4de8a-173">Stepping through your code enables you to walk through the runtime of your code, one line at a time, and figure out exactly where it is running in a different order than you expected.</span></span>  <span data-ttu-id="4de8a-174">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="4de8a-174">Try it now:</span></span>  

1.  <span data-ttu-id="4de8a-175">Clique em **passar sobre a próxima chamada de função** \ ( ![ passo pela próxima chamada de função ][ImageOverIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4de8a-175">Click **Step over next function call** \(![Step over next function call][ImageOverIcon]\).</span></span>  <span data-ttu-id="4de8a-176">O DevTools executa o código a seguir sem passar a ele.</span><span class="sxs-lookup"><span data-stu-id="4de8a-176">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="4de8a-177">DevTools ignora algumas linhas de código.</span><span class="sxs-lookup"><span data-stu-id="4de8a-177">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="4de8a-178">Isso ocorre porque é `inputsAreEmpty()` avaliado como falso; portanto, o bloco de código da `if` instrução não é executado.</span><span class="sxs-lookup"><span data-stu-id="4de8a-178">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="4de8a-179">No painel **fontes** do devtools, clique em **passar para a próxima chamada de função** \ ( ![ passar para a próxima chamada ][ImageIntoIcon] de função \) para percorrer o tempo de execução da `updateLabel()` função, uma linha por vez.</span><span class="sxs-lookup"><span data-stu-id="4de8a-179">On the **Sources** panel of DevTools, click **Step into next function call** \(![Step into next function call][ImageIntoIcon]\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="4de8a-180">Essa é a ideia básica de percorrer o código.</span><span class="sxs-lookup"><span data-stu-id="4de8a-180">That is the basic idea of stepping through code.</span></span>  <span data-ttu-id="4de8a-181">Se você examinar o código em `get-started.js` , verá que o bug está provavelmente em algum lugar na `updateLabel()` função.</span><span class="sxs-lookup"><span data-stu-id="4de8a-181">If you look at the code in `get-started.js`, you see that the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="4de8a-182">Em vez de percorrer cada linha de código, você pode usar outro tipo de ponto de interrupção para pausar o código mais próximo ao local provável do bug.</span><span class="sxs-lookup"><span data-stu-id="4de8a-182">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <span data-ttu-id="4de8a-183">Etapa 5: definir um ponto de interrupção de linha do código</span><span class="sxs-lookup"><span data-stu-id="4de8a-183">Step 5: Set a line-of-code breakpoint</span></span>   

<span data-ttu-id="4de8a-184">Os pontos de interrupção de linha de código são o tipo mais comum de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="4de8a-184">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="4de8a-185">Quando você obtém a linha específica de código em que deseja pausar, use um ponto de interrupção de linha de código:</span><span class="sxs-lookup"><span data-stu-id="4de8a-185">When you get the specific line of code that you want to pause on, use a line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="4de8a-186">Examine a última linha de código em `updateLabel()` :</span><span class="sxs-lookup"><span data-stu-id="4de8a-186">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="4de8a-187">À esquerda do código, você vê o número da linha dessa linha em particular de código, que é **33**.</span><span class="sxs-lookup"><span data-stu-id="4de8a-187">To the left of the code you see the line number of this particular line of code, which is **33**.</span></span>  <span data-ttu-id="4de8a-188">Clique em **33**.</span><span class="sxs-lookup"><span data-stu-id="4de8a-188">Click on **33**.</span></span>  <span data-ttu-id="4de8a-189">DevTools coloca um ícone vermelho à esquerda do **33**.</span><span class="sxs-lookup"><span data-stu-id="4de8a-189">DevTools puts a red icon to the left of **33**.</span></span>  <span data-ttu-id="4de8a-190">Isso significa que há um ponto de interrupção de linha de código nesta linha.</span><span class="sxs-lookup"><span data-stu-id="4de8a-190">This means that there is a line-of-code breakpoint on this line.</span></span>  <span data-ttu-id="4de8a-191">O DevTools agora sempre pausa antes da execução desta linha de código.</span><span class="sxs-lookup"><span data-stu-id="4de8a-191">DevTools now always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="4de8a-192">Clique em **retomar execução do script** \ ( ![ continuar execução do script ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4de8a-192">Click **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  <span data-ttu-id="4de8a-193">O script continuará em execução até chegar à linha 33.</span><span class="sxs-lookup"><span data-stu-id="4de8a-193">The script continues running until it reaches line 33.</span></span>  <span data-ttu-id="4de8a-194">Nas linhas 30, 31 e 32, DevTools imprime os valores de `addend1` , `addend2` e `sum` à direita do ponto-e-vírgula em cada linha.</span><span class="sxs-lookup"><span data-stu-id="4de8a-194">On lines 30, 31, and 32, DevTools prints out the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="O DevTools pausa no ponto de interrupção de linha do código na linha 32" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="4de8a-196">O DevTools pausa no ponto de interrupção de linha do código na linha 32</span><span class="sxs-lookup"><span data-stu-id="4de8a-196">DevTools pauses on the line-of-code breakpoint on line 32</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4de8a-197">Etapa 6: verificar valores de variáveis</span><span class="sxs-lookup"><span data-stu-id="4de8a-197">Step 6: Check variable values</span></span>   

<span data-ttu-id="4de8a-198">Os valores de `addend1` , `addend2` e `sum` parecem suspeitos.</span><span class="sxs-lookup"><span data-stu-id="4de8a-198">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="4de8a-199">Elas são quebradas entre aspas, o que significa que elas são cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4de8a-199">They are wrapped in quotes, which means that they are strings.</span></span>  <span data-ttu-id="4de8a-200">Trata-se de uma boa hipótese para explicar a causa do bug.</span><span class="sxs-lookup"><span data-stu-id="4de8a-200">This is a good hypothesis for the explaining the cause of the bug.</span></span>  <span data-ttu-id="4de8a-201">Agora é hora de obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="4de8a-201">Now it is time to gather more information.</span></span>  <span data-ttu-id="4de8a-202">O DevTools fornece muitas ferramentas para examinar valores variáveis.</span><span class="sxs-lookup"><span data-stu-id="4de8a-202">DevTools provides a lot of tools for examining variable values.</span></span>  

### <span data-ttu-id="4de8a-203">Método 1: o painel escopo</span><span class="sxs-lookup"><span data-stu-id="4de8a-203">Method 1: The Scope pane</span></span>   

<span data-ttu-id="4de8a-204">Quando você pausa em uma linha de código, o painel **escopo** mostra quais variáveis locais e globais estão definidas no momento, juntamente com o valor de cada variável.</span><span class="sxs-lookup"><span data-stu-id="4de8a-204">When you pause on a line of code, the **Scope** pane shows you what local and global variables are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="4de8a-205">Ele também mostra as variáveis de fechamento, quando aplicável.</span><span class="sxs-lookup"><span data-stu-id="4de8a-205">It also shows closure variables, when applicable.</span></span>  <span data-ttu-id="4de8a-206">Clique duas vezes em um valor de variável para editá-lo.</span><span class="sxs-lookup"><span data-stu-id="4de8a-206">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="4de8a-207">Quando você não estiver pausado em uma linha de código, o painel **escopo** estará vazio.</span><span class="sxs-lookup"><span data-stu-id="4de8a-207">When you are not paused on a line of code, the **Scope** pane is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="O painel escopo" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="4de8a-209">O painel **escopo**</span><span class="sxs-lookup"><span data-stu-id="4de8a-209">The **Scope** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="4de8a-210">Método 2: expressões de inspeção</span><span class="sxs-lookup"><span data-stu-id="4de8a-210">Method 2: Watch Expressions</span></span>   

<span data-ttu-id="4de8a-211">A guia **inspecionar expressões** permite monitorar os valores de variáveis ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="4de8a-211">The **Watch Expressions** tab lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="4de8a-212">Como o nome indica, as expressões de inspeção não são apenas limitadas a variáveis.</span><span class="sxs-lookup"><span data-stu-id="4de8a-212">As the name implies, Watch Expressions are not just limited to variables.</span></span>  <span data-ttu-id="4de8a-213">Você pode armazenar qualquer expressão JavaScript válida em uma expressão de inspeção.</span><span class="sxs-lookup"><span data-stu-id="4de8a-213">You are able to store any valid JavaScript expression in a Watch Expression.</span></span>  <span data-ttu-id="4de8a-214">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="4de8a-214">Try it now:</span></span>  

1.  <span data-ttu-id="4de8a-215">Clique na guia **assistir** .</span><span class="sxs-lookup"><span data-stu-id="4de8a-215">Click the **Watch** tab.</span></span>  
1.  <span data-ttu-id="4de8a-216">Clique em **Adicionar expressão** \ ( ![ Adicionar expressão ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4de8a-216">Click **Add Expression** \(![Add Expression][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="4de8a-217">Digite `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="4de8a-217">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="4de8a-218">Pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4de8a-218">Press `Enter`.</span></span>  <span data-ttu-id="4de8a-219">DevTools mostra `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="4de8a-219">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="4de8a-220">O valor à direita dos dois pontos é o resultado da sua expressão de inspeção.</span><span class="sxs-lookup"><span data-stu-id="4de8a-220">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="4de8a-221">No painel da expressão de inspeção \ (inferior-direita \) na figura a seguir, a `typeof sum` expressão de inspeção é exibida.</span><span class="sxs-lookup"><span data-stu-id="4de8a-221">In the Watch Expression pane \(bottom-right\) in in the following figure, the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="4de8a-222">Se a janela do DevTools for grande, o painel da expressão de inspeção estará no lado direito acima do painel **pontos de interrupção do ouvinte de eventos** .</span><span class="sxs-lookup"><span data-stu-id="4de8a-222">If your DevTools window is large, the Watch Expression pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="O painel da expressão de inspeção" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="4de8a-224">O painel da **expressão de inspeção**</span><span class="sxs-lookup"><span data-stu-id="4de8a-224">The **Watch Expression** pane</span></span>  
:::image-end:::  

<span data-ttu-id="4de8a-225">Como suspeito, `sum` está sendo avaliado como uma cadeia de caracteres quando deve ser um número.</span><span class="sxs-lookup"><span data-stu-id="4de8a-225">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="4de8a-226">Agora você confirmou que essa é a causa do bug.</span><span class="sxs-lookup"><span data-stu-id="4de8a-226">You have now confirmed that this is the cause of the bug.</span></span>  

### <span data-ttu-id="4de8a-227">Método 3: o console</span><span class="sxs-lookup"><span data-stu-id="4de8a-227">Method 3: The Console</span></span>   

<span data-ttu-id="4de8a-228">Além de exibir `console.log()` mensagens, você também pode usar o console para avaliar instruções JavaScript arbitrárias.</span><span class="sxs-lookup"><span data-stu-id="4de8a-228">In addition to viewing `console.log()` messages, you may also use the Console to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="4de8a-229">Em termos de depuração, você pode usar o console para testar possíveis correções de bugs.</span><span class="sxs-lookup"><span data-stu-id="4de8a-229">In terms of debugging, you may use the Console to test out potential fixes for bugs.</span></span>  <span data-ttu-id="4de8a-230">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="4de8a-230">Try it now:</span></span>  

1.  <span data-ttu-id="4de8a-231">Se você não tiver a gaveta do console aberta, pressione `Escape` para abri-la.</span><span class="sxs-lookup"><span data-stu-id="4de8a-231">If you do not have the Console drawer open, press `Escape` to open it.</span></span>  <span data-ttu-id="4de8a-232">Ele é aberto na parte inferior da janela do DevTools.</span><span class="sxs-lookup"><span data-stu-id="4de8a-232">It opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="4de8a-233">No console, digite `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="4de8a-233">In the Console, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="4de8a-234">Essa instrução funciona porque você está pausado em uma linha de código onde `addend1` e `addend2` está em escopo.</span><span class="sxs-lookup"><span data-stu-id="4de8a-234">This statement works because you are paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="4de8a-235">Pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4de8a-235">Press `Enter`.</span></span>  <span data-ttu-id="4de8a-236">O DevTools avalia a instrução e imprime `6` , que é o resultado que você espera que a demonstração produza.</span><span class="sxs-lookup"><span data-stu-id="4de8a-236">DevTools evaluates the statement and prints out `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="A gaveta do console, depois de avaliar parseInt (addend1) + parseInt (addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="4de8a-238">A gaveta do **console** , após a avaliação</span><span class="sxs-lookup"><span data-stu-id="4de8a-238">The **Console** drawer, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <span data-ttu-id="4de8a-239">Etapa 7: aplicar uma correção</span><span class="sxs-lookup"><span data-stu-id="4de8a-239">Step 7: Apply a fix</span></span>   

<span data-ttu-id="4de8a-240">Se você encontrar uma correção para o bug, experimente sua correção editando o código e executando a demonstração novamente.</span><span class="sxs-lookup"><span data-stu-id="4de8a-240">If you find a fix for the bug, try out your fix by editing the code and re-running the demo.</span></span>  <span data-ttu-id="4de8a-241">Você não precisa sair do DevTools para aplicar a correção.</span><span class="sxs-lookup"><span data-stu-id="4de8a-241">You do not need to leave DevTools to apply the fix.</span></span>  <span data-ttu-id="4de8a-242">Você pode editar o código JavaScript diretamente na interface do usuário do DevTools.</span><span class="sxs-lookup"><span data-stu-id="4de8a-242">You are able to edit JavaScript code directly within the DevTools UI.</span></span>  <span data-ttu-id="4de8a-243">Experimente agora:</span><span class="sxs-lookup"><span data-stu-id="4de8a-243">Try it now:</span></span>  

1.  <span data-ttu-id="4de8a-244">Clique em **retomar execução do script** \ ( ![ continuar execução do script ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4de8a-244">Click **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  
1.  <span data-ttu-id="4de8a-245">No **Editor de código**, substitua line 32, `var sum = addend1 + addend2` por `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="4de8a-245">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="4de8a-246">Pressione `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) para salvar a alteração.</span><span class="sxs-lookup"><span data-stu-id="4de8a-246">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="4de8a-247">Clique em **desativar pontos de interrupção** \ ( ![ desativar pontos de interrupção ][ImageDeactivateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4de8a-247">Click **Deactivate breakpoints** \(![Deactivate breakpoints][ImageDeactivateIcon]\).</span></span>  <span data-ttu-id="4de8a-248">Ele muda de azul para indicar que está ativo.</span><span class="sxs-lookup"><span data-stu-id="4de8a-248">It changes blue to indicate that it is active.</span></span>  <span data-ttu-id="4de8a-249">Enquanto isso é definido, DevTools ignora os pontos de interrupção que você definiu.</span><span class="sxs-lookup"><span data-stu-id="4de8a-249">While this is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="4de8a-250">Experimente a demonstração com valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="4de8a-250">Try out the demo with different values.</span></span>  <span data-ttu-id="4de8a-251">A demonstração agora é calculada corretamente.</span><span class="sxs-lookup"><span data-stu-id="4de8a-251">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="4de8a-252">Este fluxo de trabalho aplica-se apenas a uma correção do código que está sendo executado no navegador.</span><span class="sxs-lookup"><span data-stu-id="4de8a-252">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="4de8a-253">Ele não corrige o código para todos os usuários que acessam sua página.</span><span class="sxs-lookup"><span data-stu-id="4de8a-253">It does not fix the code for all users that visit your page.</span></span>  <span data-ttu-id="4de8a-254">Para fazer isso, você precisa corrigir o código que está em seus servidores.</span><span class="sxs-lookup"><span data-stu-id="4de8a-254">To do that, you need to fix the code that is on your servers.</span></span>  

## <span data-ttu-id="4de8a-255">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="4de8a-255">Next steps</span></span>   

<span data-ttu-id="4de8a-256">Parabéns!</span><span class="sxs-lookup"><span data-stu-id="4de8a-256">Congratulations!</span></span>  <span data-ttu-id="4de8a-257">Agora você sabe como aproveitar ao máximo o Microsoft Edge DevTools ao Depurar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4de8a-257">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="4de8a-258">As ferramentas e os métodos aprendidos neste tutorial podem economizar inúmeras horas.</span><span class="sxs-lookup"><span data-stu-id="4de8a-258">The tools and methods you learned in this tutorial may save you countless hours.</span></span>  

<span data-ttu-id="4de8a-259">Este tutorial mostrou apenas duas maneiras de definir pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="4de8a-259">This tutorial only showed you two ways to set breakpoints.</span></span>  <span data-ttu-id="4de8a-260">O DevTools oferece muitas outras maneiras, incluindo as configurações a seguir.</span><span class="sxs-lookup"><span data-stu-id="4de8a-260">DevTools offers many other ways including the following settings.</span></span>  

*   <span data-ttu-id="4de8a-261">Pontos de interrupção condicionais que são disparados quando a condição que você fornece é verdadeira.</span><span class="sxs-lookup"><span data-stu-id="4de8a-261">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="4de8a-262">Pontos de interrupção em exceções detectadas ou não capturadas.</span><span class="sxs-lookup"><span data-stu-id="4de8a-262">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="4de8a-263">XHR pontos de interrupção que são disparados quando a URL solicitada correspondem a uma Subcadeia fornecida.</span><span class="sxs-lookup"><span data-stu-id="4de8a-263">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="4de8a-264">Para obter mais informações sobre quando e como usar cada tipo, vá para [pausar o código com pontos de interrupção][DevtoolsJavscriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="4de8a-264">For more information about when and how to use each type, go to [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="4de8a-265">Há alguns controles de revisão de código que não foram explicados neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="4de8a-265">There are a couple of code stepping controls that were not explained in this tutorial.</span></span>  <span data-ttu-id="4de8a-266">Para obter mais informações, vá para a [linha passo a passo de código][DevtoolsJavascriptReferenceStepThroughCode].</span><span class="sxs-lookup"><span data-stu-id="4de8a-266">For more information, go to [Step over line of code][DevtoolsJavascriptReferenceStepThroughCode].</span></span>  

<!--  
 


-->  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Como pausar um código com pontos de interrupção no Microsoft Edge DevTools | Documentos da Microsoft"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Depurar o código-referência de depuração de JavaScript | Documentos da Microsoft"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Abrir demonstração | Problema"  

> [!NOTE]
> <span data-ttu-id="4de8a-270">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="4de8a-270">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4de8a-271">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="4de8a-271">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4de8a-273">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4de8a-273">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
