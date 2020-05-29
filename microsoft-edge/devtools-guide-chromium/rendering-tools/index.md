---
title: Analisar o desempenho do tempo de execução
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 7705428dba2ca368eb8f61b13bb96901756b081f
ms.sourcegitcommit: 0342d99bf8d3212068890bab0e1e960afa507c02
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611861"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="63f7c-103">Analisar o desempenho do tempo de execução</span><span class="sxs-lookup"><span data-stu-id="63f7c-103">Analyze Runtime Performance</span></span>   




<span data-ttu-id="63f7c-104">Os usuários esperam páginas interativas e suaves.</span><span class="sxs-lookup"><span data-stu-id="63f7c-104">Users expects interactive and smooth pages.</span></span>  <span data-ttu-id="63f7c-105">Cada estágio no pipeline de pixel representa uma oportunidade de introduzir o Jank.</span><span class="sxs-lookup"><span data-stu-id="63f7c-105">Each stage in the pixel pipeline represents an opportunity to introduce jank.</span></span>  <span data-ttu-id="63f7c-106">Saiba mais sobre ferramentas e estratégias para identificar e corrigir problemas comuns que desaceleram o desempenho do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="63f7c-106">Learn about tools and strategies to identify and fix common problems that slow down runtime performance.</span></span>  

### <span data-ttu-id="63f7c-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="63f7c-107">Summary</span></span>  

*   <span data-ttu-id="63f7c-108">Não escreva JavaScript que força o navegador a recalcular o layout.</span><span class="sxs-lookup"><span data-stu-id="63f7c-108">Do not write JavaScript that forces the browser to recalculate layout.</span></span>  <span data-ttu-id="63f7c-109">Separar funções de leitura e gravação e fazer leituras primeiro.</span><span class="sxs-lookup"><span data-stu-id="63f7c-109">Separate read and write functions, and perform reads first.</span></span>  
*   <span data-ttu-id="63f7c-110">Não se complica ao CSS.</span><span class="sxs-lookup"><span data-stu-id="63f7c-110">Do not over-complicate your CSS.</span></span>  <span data-ttu-id="63f7c-111">Use menos CSS e mantenha seus seletores CSS simples.</span><span class="sxs-lookup"><span data-stu-id="63f7c-111">Use less CSS and keep your CSS selectors simple.</span></span>  
*   <span data-ttu-id="63f7c-112">Evite o máximo de layout possível.</span><span class="sxs-lookup"><span data-stu-id="63f7c-112">Avoid layout as much as possible.</span></span>  <span data-ttu-id="63f7c-113">Escolha CSS que não dispare o layout.</span><span class="sxs-lookup"><span data-stu-id="63f7c-113">Choose CSS that does not trigger layout at all.</span></span>  
*   <span data-ttu-id="63f7c-114">Pintar pode levar mais tempo do que qualquer outra atividade de renderização.</span><span class="sxs-lookup"><span data-stu-id="63f7c-114">Painting may take up more time than any other rendering activity.</span></span>  <span data-ttu-id="63f7c-115">Cuidado com os afunilamentos de tinta.</span><span class="sxs-lookup"><span data-stu-id="63f7c-115">Watch out for paint bottlenecks.</span></span>  

## <span data-ttu-id="63f7c-116">JavaScript</span><span class="sxs-lookup"><span data-stu-id="63f7c-116">JavaScript</span></span>  

<span data-ttu-id="63f7c-117">Cálculos de JavaScript, especialmente aqueles que disparam alterações visuais abrangentes, podem paralisar o desempenho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="63f7c-117">JavaScript calculations, especially ones that trigger extensive visual changes, may stall application performance.</span></span>  <span data-ttu-id="63f7c-118">Não deixe que JavaScript com tempo incorreto ou com execução demorada interfira nas interações do usuário.</span><span class="sxs-lookup"><span data-stu-id="63f7c-118">Do not let badly-timed or long-running JavaScript interfere with user interactions.</span></span>  

### <span data-ttu-id="63f7c-119">JavaScript: ferramentas</span><span class="sxs-lookup"><span data-stu-id="63f7c-119">JavaScript: Tools</span></span>  

<span data-ttu-id="63f7c-120">Faça uma gravação no painel **desempenho** e procure eventos suspeitosmente longos `Evaluate Script` .</span><span class="sxs-lookup"><span data-stu-id="63f7c-120">Take a recording in the **Performance** panel and look for suspiciously long `Evaluate Script` events.</span></span>  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

<span data-ttu-id="63f7c-121">para notar um pouco de Jank em seu JavaScript, talvez seja necessário levar a análise para o próximo nível e coletar um perfil de CPU em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="63f7c-121">f you noticing quite a bit of jank in your JavaScript, you may need to take your analysis to the next level and collect a JavaScript CPU profile.</span></span>  <span data-ttu-id="63f7c-122">Os perfis de CPU mostram onde o tempo de execução é gasto dentro das funções da página.</span><span class="sxs-lookup"><span data-stu-id="63f7c-122">CPU profiles show where runtime is spent within the functions of your page.</span></span>  <span data-ttu-id="63f7c-123">Saiba como criar perfis de CPU [para acelerar o tempo de execução do JavaScript][DevtoolsRenderingToolsJavascriptRuntime].</span><span class="sxs-lookup"><span data-stu-id="63f7c-123">Learn how to create CPU profiles in [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span></span>

### <span data-ttu-id="63f7c-124">JavaScript: problemas</span><span class="sxs-lookup"><span data-stu-id="63f7c-124">JavaScript: Problems</span></span>  

<span data-ttu-id="63f7c-125">A tabela a seguir descreve alguns problemas comuns de JavaScript e possíveis soluções:</span><span class="sxs-lookup"><span data-stu-id="63f7c-125">The following table describes some common JavaScript problems and potential solutions:</span></span>  

| <span data-ttu-id="63f7c-126">Problema</span><span class="sxs-lookup"><span data-stu-id="63f7c-126">Problem</span></span> | <span data-ttu-id="63f7c-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="63f7c-127">Example</span></span> | <span data-ttu-id="63f7c-128">Solução</span><span class="sxs-lookup"><span data-stu-id="63f7c-128">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="63f7c-129">Manipuladores de entrada caros que afetam a resposta ou a animação.</span><span class="sxs-lookup"><span data-stu-id="63f7c-129">Expensive input handlers affecting response or animation.</span></span>  | <span data-ttu-id="63f7c-130">Toque paralaxe rolagem.</span><span class="sxs-lookup"><span data-stu-id="63f7c-130">Touch, parallax scrolling.</span></span>  | <span data-ttu-id="63f7c-131">Permita que o navegador manipule o toque e rola ou associe o ouvinte o mais tarde possível.</span><span class="sxs-lookup"><span data-stu-id="63f7c-131">Let the browser handle touch and scrolls, or bind the listener as late as possible.</span></span>  <span data-ttu-id="63f7c-132">Veja [manipuladores de entrada caros na lista de verificação de desempenho de tempo de execução de Paul Lewis][WebPerformanceCalendarRuntimeChecklist].</span><span class="sxs-lookup"><span data-stu-id="63f7c-132">See [Expensive Input Handlers in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  
| <span data-ttu-id="63f7c-133">O JavaScript com tempo incorreto afeta a resposta, a animação e a carga.</span><span class="sxs-lookup"><span data-stu-id="63f7c-133">Badly-timed JavaScript affecting response, animation, load.</span></span>  | <span data-ttu-id="63f7c-134">O usuário rola para a direita após a carga da página, setTimeout/setInterval.</span><span class="sxs-lookup"><span data-stu-id="63f7c-134">User scrolls right after page load, setTimeout / setInterval.</span></span>  | <span data-ttu-id="63f7c-135">Otimizar o tempo de execução do JavaScript: usar `requestAnimationFrame` , divulgar a manipulação dom sobre quadros, usar [funcionários da Web][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="63f7c-135">Optimize JavaScript runtime: use `requestAnimationFrame`, spread DOM manipulation over frames, use [Web Workers][MDNUsingWebWorkers].</span></span>  |  
| <span data-ttu-id="63f7c-136">O JavaScript de execução demorada afeta a resposta.</span><span class="sxs-lookup"><span data-stu-id="63f7c-136">Long-running JavaScript affecting response.</span></span>  | <span data-ttu-id="63f7c-137">O [evento DOMContentLoaded][MDNUsingWebWorkers] é interrompido, pois sobrecarregado com o JS funciona.</span><span class="sxs-lookup"><span data-stu-id="63f7c-137">The [DOMContentLoaded event][MDNUsingWebWorkers] stalls as it is swamped with JS work.</span></span>  | <span data-ttu-id="63f7c-138">Mover o trabalho de computação puro para [funcionários da Web][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="63f7c-138">Move pure computational work to [Web Workers][MDNUsingWebWorkers].</span></span>  <span data-ttu-id="63f7c-139">Se precisar de acesso ao DOM, use `requestAnimationFrame` .</span><span class="sxs-lookup"><span data-stu-id="63f7c-139">If you need DOM access, use `requestAnimationFrame`.</span></span>  <!--See also [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| <span data-ttu-id="63f7c-140">Scripts de lixo-y que afetam a resposta ou a animação.</span><span class="sxs-lookup"><span data-stu-id="63f7c-140">Garbage-y scripts affecting response or animation.</span></span>  | <span data-ttu-id="63f7c-141">A coleta de lixo pode ocorrer em qualquer lugar.</span><span class="sxs-lookup"><span data-stu-id="63f7c-141">Garbage collection may happen anywhere.</span></span>  | <span data-ttu-id="63f7c-142">Escreva menos scripts de lixo y.</span><span class="sxs-lookup"><span data-stu-id="63f7c-142">Write less garbage-y scripts.</span></span>  <span data-ttu-id="63f7c-143">Consulte [coleta de lixo em animação na lista de verificação de desempenho de tempo de execução de Paul Lewis][WebPerformanceCalendarRuntimeChecklist].</span><span class="sxs-lookup"><span data-stu-id="63f7c-143">See [Garbage Collection in Animation in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <span data-ttu-id="63f7c-144">Estilo</span><span class="sxs-lookup"><span data-stu-id="63f7c-144">Style</span></span>  

<span data-ttu-id="63f7c-145">As alterações de estilo são caras, especialmente se essas alterações afetarem mais de um elemento no DOM.</span><span class="sxs-lookup"><span data-stu-id="63f7c-145">Style changes are costly, especially if those changes affect more than one element in the DOM.</span></span>  <span data-ttu-id="63f7c-146">Sempre que você aplicar estilos a um elemento, o navegador descobre o impacto sobre todos os elementos relacionados, recalcula o layout e redesenha.</span><span class="sxs-lookup"><span data-stu-id="63f7c-146">Any time you apply styles to an element, the browser figures out the impact on all related elements, recalculates the layout, and repaints.</span></span>  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <span data-ttu-id="63f7c-147">Estilo: ferramentas</span><span class="sxs-lookup"><span data-stu-id="63f7c-147">Style: Tools</span></span>  

<span data-ttu-id="63f7c-148">Faça uma gravação no painel **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="63f7c-148">Take a recording in the **Performance** panel.</span></span>  <span data-ttu-id="63f7c-149">Verifique a gravação de `Recalculate Style` eventos grandes \ (exibidos em roxo \).</span><span class="sxs-lookup"><span data-stu-id="63f7c-149">Check the recording for large `Recalculate Style` events \(displayed in purple\).</span></span>  

<!--todo: add Recording section when available  -->  

<span data-ttu-id="63f7c-150">Clique em um `Recalculate Style` evento para ver mais informações sobre ele no painel **detalhes** .</span><span class="sxs-lookup"><span data-stu-id="63f7c-150">Click on a `Recalculate Style` event to view more information about it in the **Details** pane.</span></span>  <span data-ttu-id="63f7c-151">Se as alterações de estilo estiverem demorando muito, isso representa um impacto no desempenho.</span><span class="sxs-lookup"><span data-stu-id="63f7c-151">If the style changes are taking a long time, that is a performance hit.</span></span>  <span data-ttu-id="63f7c-152">Se os cálculos de estilo estiverem afetando um grande número de elementos, essa é outra área com espaço para melhorias.</span><span class="sxs-lookup"><span data-stu-id="63f7c-152">If the style calculations are affecting a large number of elements, that is another area with room for improvement.</span></span>  

> ##### <span data-ttu-id="63f7c-153">Figura 1</span><span class="sxs-lookup"><span data-stu-id="63f7c-153">Figure 1</span></span>  
> <span data-ttu-id="63f7c-154">Estilo de recálculo longo</span><span class="sxs-lookup"><span data-stu-id="63f7c-154">Long recalculate style</span></span>  
> ![Estilo de recálculo longo][ImageLongRecalculateStyle]

<span data-ttu-id="63f7c-156">Para reduzir o impacto de `Recalculate Style` eventos:</span><span class="sxs-lookup"><span data-stu-id="63f7c-156">To reduce the impact of `Recalculate Style` events:</span></span>  

*   <span data-ttu-id="63f7c-157">Use os [gatilhos CSS][CssTriggers] para saber quais propriedades CSS disparam o layout, o Paint e o composto.</span><span class="sxs-lookup"><span data-stu-id="63f7c-157">Use the [CSS Triggers][CssTriggers] to learn which CSS properties trigger layout, paint, and composite.</span></span>  <span data-ttu-id="63f7c-158">Essas propriedades têm o pior impacto no desempenho da renderização.</span><span class="sxs-lookup"><span data-stu-id="63f7c-158">These properties have the worst impact on rendering performance.</span></span>  
*   <span data-ttu-id="63f7c-159">Alternar para propriedades que têm menos impacto.</span><span class="sxs-lookup"><span data-stu-id="63f7c-159">Switch to properties that have less impact.</span></span>  <!--See [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties] for more guidance.  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <span data-ttu-id="63f7c-160">Estilo: problemas</span><span class="sxs-lookup"><span data-stu-id="63f7c-160">Style: Problems</span></span>  

<span data-ttu-id="63f7c-161">A tabela a seguir descreve alguns problemas comuns de estilo e soluções em potencial:</span><span class="sxs-lookup"><span data-stu-id="63f7c-161">The following table describes some common style problems and potential solutions:</span></span>  

| <span data-ttu-id="63f7c-162">Problema</span><span class="sxs-lookup"><span data-stu-id="63f7c-162">Problem</span></span> | <span data-ttu-id="63f7c-163">Exemplo</span><span class="sxs-lookup"><span data-stu-id="63f7c-163">Example</span></span> | <span data-ttu-id="63f7c-164">Solução</span><span class="sxs-lookup"><span data-stu-id="63f7c-164">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="63f7c-165">Cálculos de estilo caros que afetam a resposta ou a animação.</span><span class="sxs-lookup"><span data-stu-id="63f7c-165">Expensive style calculations affecting response or animation.</span></span>  | <span data-ttu-id="63f7c-166">Qualquer propriedade CSS que altera a geometria de um elemento, como a largura, a altura ou a posição; o navegador verifica todos os outros elementos e recalcula o layout.</span><span class="sxs-lookup"><span data-stu-id="63f7c-166">Any CSS property that changes the geometry of an element, like the width, height, or position; the browser checks all other elements and recalculates the layout.</span></span>  | <span data-ttu-id="63f7c-167">Evitar CSS que dispara layouts</span><span class="sxs-lookup"><span data-stu-id="63f7c-167">Avoid CSS that triggers layouts</span></span> |  
| <span data-ttu-id="63f7c-168">Seletores complexos que afetam a resposta ou a animação.</span><span class="sxs-lookup"><span data-stu-id="63f7c-168">Complex selectors affecting response or animation.</span></span>  | <span data-ttu-id="63f7c-169">Seletores aninhados forçam o navegador a saber tudo sobre todos os outros elementos, incluindo pais e filhos.</span><span class="sxs-lookup"><span data-stu-id="63f7c-169">Nested selectors force the browser to know everything about all the other elements, including parents and children.</span></span>  | <span data-ttu-id="63f7c-170">Faça referência a um elemento em seu CSS com apenas uma classe.</span><span class="sxs-lookup"><span data-stu-id="63f7c-170">Reference an element in your CSS with just a class.</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <span data-ttu-id="63f7c-171">Layout</span><span class="sxs-lookup"><span data-stu-id="63f7c-171">Layout</span></span>  

<span data-ttu-id="63f7c-172">O layout (ou refluxo no Firefox) é o processo pelo qual o navegador calcula as posições e os tamanhos de todos os elementos em uma página.</span><span class="sxs-lookup"><span data-stu-id="63f7c-172">Layout (or reflow in Firefox) is the process by which the browser calculates the positions and sizes of all the elements on a page.</span></span>  <span data-ttu-id="63f7c-173">O modelo de layout da Web significa que um elemento pode afetar outras pessoas; por exemplo, a largura do `<body>` elemento geralmente afeta as larguras de qualquer elemento filho, e assim por diante, até a árvore.</span><span class="sxs-lookup"><span data-stu-id="63f7c-173">The layout model of the web means that one element may affect others; for example, the width of the `<body>` element typically affects the widths of any child elements, and so on, all the way up and down the tree.</span></span>  <span data-ttu-id="63f7c-174">O processo pode estar bastante envolvido para o navegador.</span><span class="sxs-lookup"><span data-stu-id="63f7c-174">The process may be quite involved for the browser.</span></span>  

<span data-ttu-id="63f7c-175">Como regra geral, se você solicitar um valor geométrico de volta do DOM antes da conclusão de um quadro, você se encontrará com "layouts síncronos forçados", que podem ser um grande afunilamento de desempenho se repetidos frequentemente ou executados para uma árvore DOM grande.</span><span class="sxs-lookup"><span data-stu-id="63f7c-175">As a general rule of thumb, if you ask for a geometric value back from the DOM before a frame is complete, you are going to find yourself with "forced synchronous layouts", which may be a big performance bottleneck if repeated frequently or performed for a large DOM tree.</span></span>  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <span data-ttu-id="63f7c-176">Layout: ferramentas</span><span class="sxs-lookup"><span data-stu-id="63f7c-176">Layout: Tools</span></span>  

<span data-ttu-id="63f7c-177">O painel **desempenho** identifica quando uma página faz com que os layouts síncronos sejam forçados.</span><span class="sxs-lookup"><span data-stu-id="63f7c-177">The **Performance** pane identifies when a page causes forced synchronous layouts.</span></span>  <span data-ttu-id="63f7c-178">Esses `Layout` eventos são marcados com barras vermelhas.</span><span class="sxs-lookup"><span data-stu-id="63f7c-178">These `Layout` events are marked with red bars.</span></span>  

> ##### <span data-ttu-id="63f7c-179">Figura 2</span><span class="sxs-lookup"><span data-stu-id="63f7c-179">Figure 2</span></span>  
> <span data-ttu-id="63f7c-180">Layout síncrono forçado</span><span class="sxs-lookup"><span data-stu-id="63f7c-180">Forced synchronous layout</span></span>  
> ![Layout síncrono forçado][ImageForcedSynchronousLayout]  

<span data-ttu-id="63f7c-182">"Layout thrashing" é uma repetição de condições de layout síncrono forçado.</span><span class="sxs-lookup"><span data-stu-id="63f7c-182">"Layout thrashing" is a repetition of forced synchronous layout conditions.</span></span>  <span data-ttu-id="63f7c-183">Isso ocorre quando o JavaScript grava e lê do DOM repetidamente, o que força o navegador a recalcular o layout de uma vez.</span><span class="sxs-lookup"><span data-stu-id="63f7c-183">This occurs when JavaScript writes and reads from the DOM repeatedly, which forces the browser to recalculate the layout over and over.</span></span>  <span data-ttu-id="63f7c-184">Para identificar a thrashing de layout, procure por um padrão de vários avisos de layout síncrono forçado.</span><span class="sxs-lookup"><span data-stu-id="63f7c-184">To identify layout thrashing, look for a pattern of multiple forced synchronous layout warnings.</span></span>  <span data-ttu-id="63f7c-185">Veja a [Figura 2](#figure-2).</span><span class="sxs-lookup"><span data-stu-id="63f7c-185">See [Figure 2](#figure-2).</span></span>  

### <span data-ttu-id="63f7c-186">Layout: problemas</span><span class="sxs-lookup"><span data-stu-id="63f7c-186">Layout: Problems</span></span>  

<span data-ttu-id="63f7c-187">A tabela a seguir descreve alguns problemas comuns de layout e soluções possíveis:</span><span class="sxs-lookup"><span data-stu-id="63f7c-187">The following table describes some common layout problems and potential solutions:</span></span>  

| <span data-ttu-id="63f7c-188">Problema</span><span class="sxs-lookup"><span data-stu-id="63f7c-188">Problem</span></span> | <span data-ttu-id="63f7c-189">Exemplo</span><span class="sxs-lookup"><span data-stu-id="63f7c-189">Example</span></span> | <span data-ttu-id="63f7c-190">Solução</span><span class="sxs-lookup"><span data-stu-id="63f7c-190">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="63f7c-191">Layout síncrono forçado que afeta a resposta ou a animação.</span><span class="sxs-lookup"><span data-stu-id="63f7c-191">Forced synchronous layout affecting response or animation.</span></span>  | <span data-ttu-id="63f7c-192">Forçar o navegador a executar o layout anteriormente no pipeline de pixel, resultando em etapas repetidas do processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="63f7c-192">Forcing the browser to perform layout earlier in the pixel pipeline, resulting in repeating steps in the rendering process.</span></span>  | <span data-ttu-id="63f7c-193">Lote o seu estilo lê primeiro e, em seguida, faça gravações.</span><span class="sxs-lookup"><span data-stu-id="63f7c-193">Batch your style reads first, then do any writes.</span></span>  <!--See also [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| <span data-ttu-id="63f7c-194">Layout thrashing afetar a resposta ou a animação.</span><span class="sxs-lookup"><span data-stu-id="63f7c-194">Layout thrashing affecting response or animation.</span></span>  | <span data-ttu-id="63f7c-195">Um loop que coloca o navegador em um ciclo de leitura-gravação-leitura-gravação, forçando o navegador a recalcular o layout repetidas vezes.</span><span class="sxs-lookup"><span data-stu-id="63f7c-195">A loop that puts the browser into a read-write-read-write cycle, forcing the browser to recalculate layout over and over again.</span></span>  | <span data-ttu-id="63f7c-196">Operações de leitura/gravação em lotes automaticamente usando a [biblioteca do FastDom][GitHubWilsonpageFastdom].</span><span class="sxs-lookup"><span data-stu-id="63f7c-196">Automatically batch read-write operations using [FastDom library][GitHubWilsonpageFastdom].</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <span data-ttu-id="63f7c-197">Pintura e composição</span><span class="sxs-lookup"><span data-stu-id="63f7c-197">Paint and composite</span></span>  

<span data-ttu-id="63f7c-198">O Paint é o processo de preenchimento em pixels.</span><span class="sxs-lookup"><span data-stu-id="63f7c-198">Paint is the process of filling in pixels.</span></span>  <span data-ttu-id="63f7c-199">Geralmente, é a parte mais dispendiosa do processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="63f7c-199">It is often the most costly part of the rendering process.</span></span>  <span data-ttu-id="63f7c-200">Se você observou que sua página está Janky de alguma maneira, é provável que você tenha problemas de pintura.</span><span class="sxs-lookup"><span data-stu-id="63f7c-200">If you noticed that your page is janky in any way, it is likely that you have paint problems.</span></span>  

<span data-ttu-id="63f7c-201">Composição é onde as partes pintadas da página são colocadas juntas para exibição na tela.</span><span class="sxs-lookup"><span data-stu-id="63f7c-201">Compositing is where the painted parts of the page are put together for displaying on screen.</span></span>  <span data-ttu-id="63f7c-202">Para a maioria das propriedades, se você se conectar a somente propriedades do compositor e evitar o Paint, verá uma grande melhoria no desempenho, mas você precisará tomar cuidado com contagens de camadas excessivas.</span><span class="sxs-lookup"><span data-stu-id="63f7c-202">For the most part, if you stick to compositor-only properties and avoid paint altogether, you should see a major improvement in performance, but you need to watch out for excessive layer counts.</span></span>  <!--See also [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <span data-ttu-id="63f7c-203">Pintura e composição: ferramentas</span><span class="sxs-lookup"><span data-stu-id="63f7c-203">Paint and composite: Tools</span></span>  

<span data-ttu-id="63f7c-204">Quer saber quanto tempo de pintura leva ou com que frequência ocorre a pintura?</span><span class="sxs-lookup"><span data-stu-id="63f7c-204">Want to know how long painting takes or how often painting occurs?</span></span>  <span data-ttu-id="63f7c-205">Marque a configuração [habilitar a instrumentação avançada de pintura][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] no painel **desempenho** e, em seguida, faça uma gravação.</span><span class="sxs-lookup"><span data-stu-id="63f7c-205">Check the [Enable advanced paint instrumentation][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] setting in the **Performance** panel and then take a recording.</span></span>  <span data-ttu-id="63f7c-206">Se a maior parte do seu tempo de renderização for gasta na pintura, você tem problemas de pintura.</span><span class="sxs-lookup"><span data-stu-id="63f7c-206">If most of your rendering time is spent painting, you have paint problems.</span></span>  

<!--
> ##### Old Figure 3  
> Long paint times in timeline recording  
> ![Long paint times in timeline recording][ImageLongPaintTimes]  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <span data-ttu-id="63f7c-207">Pintura e composição: problemas</span><span class="sxs-lookup"><span data-stu-id="63f7c-207">Paint and composite: Problems</span></span>  

<span data-ttu-id="63f7c-208">A tabela a seguir descreve alguns problemas comuns de pintura e composição e possíveis soluções:</span><span class="sxs-lookup"><span data-stu-id="63f7c-208">The following table describes some common paint and composite problems and potential solutions:</span></span>  

| <span data-ttu-id="63f7c-209">Problema</span><span class="sxs-lookup"><span data-stu-id="63f7c-209">Problem</span></span> | <span data-ttu-id="63f7c-210">Exemplo</span><span class="sxs-lookup"><span data-stu-id="63f7c-210">Example</span></span> | <span data-ttu-id="63f7c-211">Solução</span><span class="sxs-lookup"><span data-stu-id="63f7c-211">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="63f7c-212">As tempestades de pintura afetam a resposta ou a animação.</span><span class="sxs-lookup"><span data-stu-id="63f7c-212">Paint storms affecting response or animation.</span></span>  | <span data-ttu-id="63f7c-213">Grandes áreas de pintura ou pinturas caras que afetam a resposta ou a animação.</span><span class="sxs-lookup"><span data-stu-id="63f7c-213">Big paint areas or expensive paints affecting response or animation.</span></span>  | <span data-ttu-id="63f7c-214">Evite pintar, promover elementos que estão se movendo para sua própria camada, use transformações e opacidade.</span><span class="sxs-lookup"><span data-stu-id="63f7c-214">Avoid paint, promote elements that are moving to their own layer, use transforms and opacity.</span></span>  <!--See [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| <span data-ttu-id="63f7c-215">Explosões de camada que afetam animações.</span><span class="sxs-lookup"><span data-stu-id="63f7c-215">Layer explosions affecting animations.</span></span>  | <span data-ttu-id="63f7c-216">A promoção de elementos demais com o `translateZ(0)` desempenho da animação é bastante afetado.</span><span class="sxs-lookup"><span data-stu-id="63f7c-216">Overpromotion of too many elements with `translateZ(0)` greatly affects animation performance.</span></span>  | <span data-ttu-id="63f7c-217">Promover a camadas com moderação e apenas quando você souber que ela oferece melhorias concretas.</span><span class="sxs-lookup"><span data-stu-id="63f7c-217">Promote to layers sparingly, and only when you know it offers tangible improvements.</span></span>  <!--See [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

<!--## Feedback   -->  



<!-- image links -->  

[ImageLongRecalculateStyle]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-performance-recalculate-style-summary.msft.png "Figura 1: estilo de recálculo longo"  
[ImageForcedSynchronousLayout]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-jank-performance-recalculate-style-summary.msft.png "Figura 2: layout síncrono forçado"  
<!--[ImageLongPaintTimes]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png "Old Figure 3: Long paint times in timeline recording"  -->  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Acelerar o tempo de execução do JavaScript"  

[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#enable-advanced-paint-instrumentation "Habilitar a instrumentação avançada de pintura-referência de análise de desempenho"

<!--[DevtoolsRenderingToolsForcedSynchronousLayouts]: /microsoft-edge/devtools-guide-chromium/rendering-tools/forced-synchronous-layouts "Diagnose Forced Synchronous Layouts"  -->  

<!-- The Timeline Tool page is deprecated  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfileJavascript]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/timeline-tool#profile-javascript "Profile JavaScript - How to Use the Timeline Tool"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfilePainting]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/timeline-tool#profile-painting "Profile painting - How to Use the Timeline Tool"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRecording]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/timeline-tool#make-a-recording "Make a recording - How to Use the Timeline Tool"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRenderingSettings]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/timeline-tool#rendering-settings "Rendering settings - How to Use the Timeline Tool"  -->  

<!--[WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing "Avoid Large, Complex Layouts, and Layout Thrashing"  -->  
<!--[WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime]: /web/fundamentals/performance/rendering/optimize-javascript-execution "Optimize JavaScript Runtime"  -->  
<!--[WebFundamentalsPerformanceRenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations "Reduce the Scope and Complexity of Style Calculations"  -->  
<!--[WebFundamentalsPerformanceRenderingSimplifyPaintComplexity]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas "Simplify Paint Complexity and Reduce Paint Areas"  -->  
<!--[WebFundamentalsPerformanceRenderingCompositorOnlyProperties]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count "Stick to Compositor-Only Properties and Manage Layer Count"  -->  

[CssTriggers]: https://csstriggers.com "Gatilhos CSS"  

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Usar o Web Works | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Lista de verificação de desempenho do tempo de execução-calendário de desempenho da Web"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> <span data-ttu-id="63f7c-226">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="63f7c-226">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="63f7c-227">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \) e [Meggin Kearney][MegginKearney] \ (Tech Writer \).</span><span class="sxs-lookup"><span data-stu-id="63f7c-227">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="63f7c-229">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="63f7c-229">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
