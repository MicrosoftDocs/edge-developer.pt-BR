---
description: Os usuários esperam páginas interativas e suaves.  Cada estágio no pipeline de pixels representa uma oportunidade de introduzir jank.  Saiba mais sobre ferramentas e estratégias para identificar e corrigir problemas comuns que retardam o desempenho do tempo de execução.
title: Analisar o desempenho do tempo de execução
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 646db5b2e88e33b109e5eb3ae01a296bf3a4fb46
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397997"
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

# <a name="analyze-runtime-performance"></a><span data-ttu-id="16ad7-106">Analisar o desempenho do tempo de execução</span><span class="sxs-lookup"><span data-stu-id="16ad7-106">Analyze runtime performance</span></span>  

<span data-ttu-id="16ad7-107">Os usuários esperam páginas interativas e suaves.</span><span class="sxs-lookup"><span data-stu-id="16ad7-107">Users expects interactive and smooth pages.</span></span>  <span data-ttu-id="16ad7-108">Cada estágio no pipeline de pixels representa uma oportunidade de introduzir jank.</span><span class="sxs-lookup"><span data-stu-id="16ad7-108">Each stage in the pixel pipeline represents an opportunity to introduce jank.</span></span>  <span data-ttu-id="16ad7-109">Saiba mais sobre ferramentas e estratégias para identificar e corrigir problemas comuns que retardam o desempenho do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="16ad7-109">Learn about tools and strategies to identify and fix common problems that slow down runtime performance.</span></span>  

### <a name="summary"></a><span data-ttu-id="16ad7-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="16ad7-110">Summary</span></span>  

*   <span data-ttu-id="16ad7-111">Não escreva JavaScript que força o navegador a recalcular o layout.</span><span class="sxs-lookup"><span data-stu-id="16ad7-111">Do not write JavaScript that forces the browser to recalculate layout.</span></span>  <span data-ttu-id="16ad7-112">Separe funções de leitura e gravação e execute leituras primeiro.</span><span class="sxs-lookup"><span data-stu-id="16ad7-112">Separate read and write functions, and perform reads first.</span></span>  
*   <span data-ttu-id="16ad7-113">Não complique demais seu CSS.</span><span class="sxs-lookup"><span data-stu-id="16ad7-113">Do not over-complicate your CSS.</span></span>  <span data-ttu-id="16ad7-114">Use menos CSS e mantenha seus seletores CSS simples.</span><span class="sxs-lookup"><span data-stu-id="16ad7-114">Use less CSS and keep your CSS selectors simple.</span></span>  
*   <span data-ttu-id="16ad7-115">Evite o layout o máximo possível.</span><span class="sxs-lookup"><span data-stu-id="16ad7-115">Avoid layout as much as possible.</span></span>  <span data-ttu-id="16ad7-116">Escolha CSS que não aciona o layout.</span><span class="sxs-lookup"><span data-stu-id="16ad7-116">Choose CSS that does not trigger layout at all.</span></span>  
*   <span data-ttu-id="16ad7-117">A pintura pode levar mais tempo do que qualquer outra atividade de renderização.</span><span class="sxs-lookup"><span data-stu-id="16ad7-117">Painting may take up more time than any other rendering activity.</span></span>  <span data-ttu-id="16ad7-118">Cuidado com os gargalos de tinta.</span><span class="sxs-lookup"><span data-stu-id="16ad7-118">Watch out for paint bottlenecks.</span></span>  
    
## <a name="javascript"></a><span data-ttu-id="16ad7-119">JavaScript</span><span class="sxs-lookup"><span data-stu-id="16ad7-119">JavaScript</span></span>  

<span data-ttu-id="16ad7-120">Cálculos JavaScript, especialmente aqueles que disparam alterações visuais extensas, podem atrasar o desempenho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16ad7-120">JavaScript calculations, especially ones that trigger extensive visual changes, may stall application performance.</span></span>  <span data-ttu-id="16ad7-121">Não deixe que o JavaScript em tempo hábil ou de longa duração interfira nas interações do usuário.</span><span class="sxs-lookup"><span data-stu-id="16ad7-121">Do not let badly-timed or long-running JavaScript interfere with user interactions.</span></span>  

### <a name="javascript-tools"></a><span data-ttu-id="16ad7-122">JavaScript: Ferramentas</span><span class="sxs-lookup"><span data-stu-id="16ad7-122">JavaScript: Tools</span></span>  

<span data-ttu-id="16ad7-123">Pegue uma gravação na ferramenta **Performance** e procure eventos suspeitosamente `Evaluate Script` longos.</span><span class="sxs-lookup"><span data-stu-id="16ad7-123">Take a recording in the **Performance** tool and look for suspiciously long `Evaluate Script` events.</span></span>  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

<span data-ttu-id="16ad7-124">f você observar um pouco de jank em seu JavaScript, talvez seja necessário levar sua análise para o próximo nível e coletar um perfil de CPU JavaScript.</span><span class="sxs-lookup"><span data-stu-id="16ad7-124">f you noticing quite a bit of jank in your JavaScript, you may need to take your analysis to the next level and collect a JavaScript CPU profile.</span></span>  <span data-ttu-id="16ad7-125">Os perfis de CPU mostram onde o tempo de execução é gasto dentro das funções da sua página.</span><span class="sxs-lookup"><span data-stu-id="16ad7-125">CPU profiles show where runtime is spent within the functions of your page.</span></span>  <span data-ttu-id="16ad7-126">Saiba como criar perfis de CPU no [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span><span class="sxs-lookup"><span data-stu-id="16ad7-126">Learn how to create CPU profiles in [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span></span>

### <a name="javascript-problems"></a><span data-ttu-id="16ad7-127">JavaScript: Problemas</span><span class="sxs-lookup"><span data-stu-id="16ad7-127">JavaScript: Problems</span></span>  

<span data-ttu-id="16ad7-128">A tabela a seguir descreve alguns problemas comuns do JavaScript e possíveis soluções.</span><span class="sxs-lookup"><span data-stu-id="16ad7-128">The following table describes some common JavaScript problems and potential solutions.</span></span>  

| <span data-ttu-id="16ad7-129">Problema</span><span class="sxs-lookup"><span data-stu-id="16ad7-129">Problem</span></span> | <span data-ttu-id="16ad7-130">Exemplo</span><span class="sxs-lookup"><span data-stu-id="16ad7-130">Example</span></span> | <span data-ttu-id="16ad7-131">Solução</span><span class="sxs-lookup"><span data-stu-id="16ad7-131">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16ad7-132">Manipuladores de entrada caros que afetam a resposta ou animação.</span><span class="sxs-lookup"><span data-stu-id="16ad7-132">Expensive input handlers affecting response or animation.</span></span>  | <span data-ttu-id="16ad7-133">Toque, rolagem de paralaxaxas.</span><span class="sxs-lookup"><span data-stu-id="16ad7-133">Touch, parallax scrolling.</span></span>  | <span data-ttu-id="16ad7-134">Deixe o navegador manipular toque e rolagem ou vincular o ouvinte o mais tarde possível.</span><span class="sxs-lookup"><span data-stu-id="16ad7-134">Let the browser handle touch and scrolls, or bind the listener as late as possible.</span></span>  <span data-ttu-id="16ad7-135">Navegue até [Manipuladores de Entrada Caros na][WebPerformanceCalendarRuntimeChecklist]lista de verificação de desempenho do tempo de execução de Paulo Lewis.</span><span class="sxs-lookup"><span data-stu-id="16ad7-135">Navigate to [Expensive Input Handlers in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  
| <span data-ttu-id="16ad7-136">JavaScript com tempo ruim afetando a resposta, animação, carga.</span><span class="sxs-lookup"><span data-stu-id="16ad7-136">Badly-timed JavaScript affecting response, animation, load.</span></span>  | <span data-ttu-id="16ad7-137">O usuário rola logo após o carregamento da página, setTimeout /setInterval.</span><span class="sxs-lookup"><span data-stu-id="16ad7-137">User scrolls right after page load, setTimeout / setInterval.</span></span>  | <span data-ttu-id="16ad7-138">Otimizar o tempo de execução do JavaScript: usar `requestAnimationFrame` , propagar a manipulação dom sobre quadros, usar [Web Workers][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="16ad7-138">Optimize JavaScript runtime: use `requestAnimationFrame`, spread DOM manipulation over frames, use [Web Workers][MDNUsingWebWorkers].</span></span>  |  
| <span data-ttu-id="16ad7-139">JavaScript de execução longa afetando a resposta.</span><span class="sxs-lookup"><span data-stu-id="16ad7-139">Long-running JavaScript affecting response.</span></span>  | <span data-ttu-id="16ad7-140">O [evento DOMContentLoaded][MDNUsingWebWorkers] para quando está cheio de trabalho JS.</span><span class="sxs-lookup"><span data-stu-id="16ad7-140">The [DOMContentLoaded event][MDNUsingWebWorkers] stalls as it is swamped with JS work.</span></span>  | <span data-ttu-id="16ad7-141">Mover trabalho computacional puro para [Web Workers][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="16ad7-141">Move pure computational work to [Web Workers][MDNUsingWebWorkers].</span></span>  <span data-ttu-id="16ad7-142">Se você precisar de acesso DOM, use `requestAnimationFrame` .</span><span class="sxs-lookup"><span data-stu-id="16ad7-142">If you need DOM access, use `requestAnimationFrame`.</span></span>  <!--Navigate to [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| <span data-ttu-id="16ad7-143">Scripts de lixo y que afetam a resposta ou animação.</span><span class="sxs-lookup"><span data-stu-id="16ad7-143">Garbage-y scripts affecting response or animation.</span></span>  | <span data-ttu-id="16ad7-144">A coleta de lixo pode acontecer em qualquer lugar.</span><span class="sxs-lookup"><span data-stu-id="16ad7-144">Garbage collection may happen anywhere.</span></span>  | <span data-ttu-id="16ad7-145">Escreva menos scripts de lixo y.</span><span class="sxs-lookup"><span data-stu-id="16ad7-145">Write less garbage-y scripts.</span></span>  <span data-ttu-id="16ad7-146">Navegue [até Coleta de Lixo em Animação na][WebPerformanceCalendarRuntimeChecklist]lista de verificação de desempenho do tempo de execução de Paulo Lewis.</span><span class="sxs-lookup"><span data-stu-id="16ad7-146">Navigate to [Garbage Collection in Animation in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <a name="style"></a><span data-ttu-id="16ad7-147">Estilo</span><span class="sxs-lookup"><span data-stu-id="16ad7-147">Style</span></span>  

<span data-ttu-id="16ad7-148">As alterações de estilo são caras, especialmente se essas alterações afetarem mais de um elemento no DOM.</span><span class="sxs-lookup"><span data-stu-id="16ad7-148">Style changes are costly, especially if those changes affect more than one element in the DOM.</span></span>  <span data-ttu-id="16ad7-149">Sempre que você aplica estilos a um elemento, o navegador descobre o impacto em todos os elementos relacionados, recalcula o layout e repaints.</span><span class="sxs-lookup"><span data-stu-id="16ad7-149">Any time you apply styles to an element, the browser figures out the impact on all related elements, recalculates the layout, and repaints.</span></span>  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <a name="style-tools"></a><span data-ttu-id="16ad7-150">Estilo: Ferramentas</span><span class="sxs-lookup"><span data-stu-id="16ad7-150">Style: Tools</span></span>  

<span data-ttu-id="16ad7-151">Fazer uma gravação na **ferramenta Performance.**</span><span class="sxs-lookup"><span data-stu-id="16ad7-151">Take a recording in the **Performance** tool.</span></span>  <span data-ttu-id="16ad7-152">Verifique a gravação de eventos `Recalculate Style` grandes \(exibido em roxo\).</span><span class="sxs-lookup"><span data-stu-id="16ad7-152">Check the recording for large `Recalculate Style` events \(displayed in purple\).</span></span>  

<!--todo: add Recording section when available  -->  

<span data-ttu-id="16ad7-153">Escolha um `Recalculate Style` evento para exibir mais informações sobre ele no painel **Detalhes.**</span><span class="sxs-lookup"><span data-stu-id="16ad7-153">Choose a `Recalculate Style` event to view more information about it in the **Details** pane.</span></span>  <span data-ttu-id="16ad7-154">Se as alterações de estilo estão demorando muito, isso é um sucesso de desempenho.</span><span class="sxs-lookup"><span data-stu-id="16ad7-154">If the style changes are taking a long time, that is a performance hit.</span></span>  <span data-ttu-id="16ad7-155">Se os cálculos de estilo estão afetando um grande número de elementos, essa é outra área com espaço para aprimoramento.</span><span class="sxs-lookup"><span data-stu-id="16ad7-155">If the style calculations are affecting a large number of elements, that is another area with room for improvement.</span></span>  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Estilo de recálcula longo" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="16ad7-157">Estilo de recálcula longo</span><span class="sxs-lookup"><span data-stu-id="16ad7-157">Long recalculate style</span></span>  
:::image-end:::  

<span data-ttu-id="16ad7-158">Para reduzir o impacto dos `Recalculate Style` eventos:</span><span class="sxs-lookup"><span data-stu-id="16ad7-158">To reduce the impact of `Recalculate Style` events:</span></span>  

*   <span data-ttu-id="16ad7-159">Use os [Gatilhos CSS para][CssTriggers] saber quais propriedades CSS disparam layout, tinta e composição.</span><span class="sxs-lookup"><span data-stu-id="16ad7-159">Use the [CSS Triggers][CssTriggers] to learn which CSS properties trigger layout, paint, and composite.</span></span>  <span data-ttu-id="16ad7-160">Essas propriedades têm o pior impacto no desempenho da renderização.</span><span class="sxs-lookup"><span data-stu-id="16ad7-160">These properties have the worst impact on rendering performance.</span></span>  
*   <span data-ttu-id="16ad7-161">Alternar para propriedades que tenham menos impacto.</span><span class="sxs-lookup"><span data-stu-id="16ad7-161">Switch to properties that have less impact.</span></span>  <!--For more guidance, navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <a name="style-problems"></a><span data-ttu-id="16ad7-162">Estilo: Problemas</span><span class="sxs-lookup"><span data-stu-id="16ad7-162">Style: Problems</span></span>  

<span data-ttu-id="16ad7-163">A tabela a seguir descreve alguns problemas de estilo comuns e possíveis soluções.</span><span class="sxs-lookup"><span data-stu-id="16ad7-163">The following table describes some common style problems and potential solutions.</span></span>  

| <span data-ttu-id="16ad7-164">Problema</span><span class="sxs-lookup"><span data-stu-id="16ad7-164">Problem</span></span> | <span data-ttu-id="16ad7-165">Exemplo</span><span class="sxs-lookup"><span data-stu-id="16ad7-165">Example</span></span> | <span data-ttu-id="16ad7-166">Solução</span><span class="sxs-lookup"><span data-stu-id="16ad7-166">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16ad7-167">Cálculos de estilo caros que afetam a resposta ou a animação.</span><span class="sxs-lookup"><span data-stu-id="16ad7-167">Expensive style calculations affecting response or animation.</span></span>  | <span data-ttu-id="16ad7-168">Qualquer propriedade CSS que altera a geometria de um elemento, como a largura, altura ou posição; o navegador verifica todos os outros elementos e recalcula o layout.</span><span class="sxs-lookup"><span data-stu-id="16ad7-168">Any CSS property that changes the geometry of an element, like the width, height, or position; the browser checks all other elements and recalculates the layout.</span></span>  | <span data-ttu-id="16ad7-169">Evitar CSS que dispara layouts</span><span class="sxs-lookup"><span data-stu-id="16ad7-169">Avoid CSS that triggers layouts</span></span> |  
| <span data-ttu-id="16ad7-170">Seletores complexos que afetam a resposta ou a animação.</span><span class="sxs-lookup"><span data-stu-id="16ad7-170">Complex selectors affecting response or animation.</span></span>  | <span data-ttu-id="16ad7-171">Os seletores aninhados forçam o navegador a saber tudo sobre todos os outros elementos, incluindo pais e filhos.</span><span class="sxs-lookup"><span data-stu-id="16ad7-171">Nested selectors force the browser to know everything about all the other elements, including parents and children.</span></span>  | <span data-ttu-id="16ad7-172">Fazer referência a um elemento em seu CSS com apenas uma classe.</span><span class="sxs-lookup"><span data-stu-id="16ad7-172">Reference an element in your CSS with just a class.</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <a name="layout"></a><span data-ttu-id="16ad7-173">Layout</span><span class="sxs-lookup"><span data-stu-id="16ad7-173">Layout</span></span>  

<span data-ttu-id="16ad7-174">Layout (ou refluxo no Firefox) é o processo pelo qual o navegador calcula as posições e tamanhos de todos os elementos em uma página.</span><span class="sxs-lookup"><span data-stu-id="16ad7-174">Layout (or reflow in Firefox) is the process by which the browser calculates the positions and sizes of all the elements on a page.</span></span>  <span data-ttu-id="16ad7-175">O modelo de layout da Web significa que um elemento pode afetar outros; por exemplo, a largura do elemento normalmente afeta as larguras de todos os elementos filho e assim por diante, todo o caminho para cima e para baixo `<body>` da árvore.</span><span class="sxs-lookup"><span data-stu-id="16ad7-175">The layout model of the web means that one element may affect others; for example, the width of the `<body>` element typically affects the widths of any child elements, and so on, all the way up and down the tree.</span></span>  <span data-ttu-id="16ad7-176">O processo pode estar bastante envolvido para o navegador.</span><span class="sxs-lookup"><span data-stu-id="16ad7-176">The process may be quite involved for the browser.</span></span>  

<span data-ttu-id="16ad7-177">Como regra geral, se você solicitar um valor geométrico de volta do DOM antes que um quadro seja concluído, você se encontrará com "layouts síncronos forçados", o que pode ser um grande arrojo de desempenho se repetido com frequência ou executado para uma árvore DOM grande.</span><span class="sxs-lookup"><span data-stu-id="16ad7-177">As a general rule of thumb, if you ask for a geometric value back from the DOM before a frame is complete, you are going to find yourself with "forced synchronous layouts", which may be a big performance bottleneck if repeated frequently or performed for a large DOM tree.</span></span>  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <a name="layout-tools"></a><span data-ttu-id="16ad7-178">Layout: Ferramentas</span><span class="sxs-lookup"><span data-stu-id="16ad7-178">Layout: Tools</span></span>  

<span data-ttu-id="16ad7-179">O **painel** Desempenho identifica quando uma página causa layouts síncronos forçados.</span><span class="sxs-lookup"><span data-stu-id="16ad7-179">The **Performance** pane identifies when a page causes forced synchronous layouts.</span></span>  <span data-ttu-id="16ad7-180">Esses `Layout` eventos são marcados com barras vermelhas.</span><span class="sxs-lookup"><span data-stu-id="16ad7-180">These `Layout` events are marked with red bars.</span></span>  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Layout síncrono forçado" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="16ad7-182">Layout síncrono forçado</span><span class="sxs-lookup"><span data-stu-id="16ad7-182">Forced synchronous layout</span></span>  
:::image-end:::  

<span data-ttu-id="16ad7-183">"Quebra de layout" é uma repetição das condições de layout síncronas forçadas.</span><span class="sxs-lookup"><span data-stu-id="16ad7-183">"Layout thrashing" is a repetition of forced synchronous layout conditions.</span></span>  <span data-ttu-id="16ad7-184">Isso ocorre quando JavaScript grava e lê do DOM repetidamente, o que força o navegador a recalcular o layout repetidamente.</span><span class="sxs-lookup"><span data-stu-id="16ad7-184">This occurs when JavaScript writes and reads from the DOM repeatedly, which forces the browser to recalculate the layout over and over.</span></span>  <span data-ttu-id="16ad7-185">Para identificar a quebra de layout, procure um padrão de vários avisos de layout síncrono forçados.</span><span class="sxs-lookup"><span data-stu-id="16ad7-185">To identify layout thrashing, look for a pattern of multiple forced synchronous layout warnings.</span></span>  <span data-ttu-id="16ad7-186">Revise a figura anterior.</span><span class="sxs-lookup"><span data-stu-id="16ad7-186">Review the previous figure.</span></span>  

### <a name="layout-problems"></a><span data-ttu-id="16ad7-187">Layout: Problemas</span><span class="sxs-lookup"><span data-stu-id="16ad7-187">Layout: Problems</span></span>  

<span data-ttu-id="16ad7-188">A tabela a seguir descreve alguns problemas comuns de layout e possíveis soluções.</span><span class="sxs-lookup"><span data-stu-id="16ad7-188">The following table describes some common layout problems and potential solutions.</span></span>  

| <span data-ttu-id="16ad7-189">Problema</span><span class="sxs-lookup"><span data-stu-id="16ad7-189">Problem</span></span> | <span data-ttu-id="16ad7-190">Exemplo</span><span class="sxs-lookup"><span data-stu-id="16ad7-190">Example</span></span> | <span data-ttu-id="16ad7-191">Solução</span><span class="sxs-lookup"><span data-stu-id="16ad7-191">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16ad7-192">Layout síncrono forçado afetando a resposta ou animação.</span><span class="sxs-lookup"><span data-stu-id="16ad7-192">Forced synchronous layout affecting response or animation.</span></span>  | <span data-ttu-id="16ad7-193">Forçando o navegador a executar o layout anteriormente no pipeline de pixels, resultando em etapas repetidas no processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="16ad7-193">Forcing the browser to perform layout earlier in the pixel pipeline, resulting in repeating steps in the rendering process.</span></span>  | <span data-ttu-id="16ad7-194">Em lotes, seu estilo lê primeiro e, em seguida, grava todas as gravações.</span><span class="sxs-lookup"><span data-stu-id="16ad7-194">Batch your style reads first, then do any writes.</span></span>  <!--Navigate to [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| <span data-ttu-id="16ad7-195">A reação de layout afetando a resposta ou a animação.</span><span class="sxs-lookup"><span data-stu-id="16ad7-195">Layout thrashing affecting response or animation.</span></span>  | <span data-ttu-id="16ad7-196">Um loop que coloca o navegador em um ciclo de leitura-gravação-leitura-gravação, forçando o navegador a recalcular o layout uma e outra vez.</span><span class="sxs-lookup"><span data-stu-id="16ad7-196">A loop that puts the browser into a read-write-read-write cycle, forcing the browser to recalculate layout over and over again.</span></span>  | <span data-ttu-id="16ad7-197">Operações de leitura em lote automaticamente usando [a biblioteca do FastDom.][GitHubWilsonpageFastdom]</span><span class="sxs-lookup"><span data-stu-id="16ad7-197">Automatically batch read-write operations using [FastDom library][GitHubWilsonpageFastdom].</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <a name="paint-and-composite"></a><span data-ttu-id="16ad7-198">Tinta e composição</span><span class="sxs-lookup"><span data-stu-id="16ad7-198">Paint and composite</span></span>  

<span data-ttu-id="16ad7-199">Paint é o processo de preenchimento de pixels.</span><span class="sxs-lookup"><span data-stu-id="16ad7-199">Paint is the process of filling in pixels.</span></span>  <span data-ttu-id="16ad7-200">Geralmente, é a parte mais cara do processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="16ad7-200">It is often the most costly part of the rendering process.</span></span>  <span data-ttu-id="16ad7-201">Se você reparou que sua página não está funcionando como projetada de alguma forma, é provável que você tenha problemas de tinta.</span><span class="sxs-lookup"><span data-stu-id="16ad7-201">If you noticed that your page is not working as designed in any way, it is likely that you have paint problems.</span></span>  

<span data-ttu-id="16ad7-202">A composição é onde as partes pintadas da página são colocadas juntas para exibição na tela.</span><span class="sxs-lookup"><span data-stu-id="16ad7-202">Compositing is where the painted parts of the page are put together for displaying on screen.</span></span>  <span data-ttu-id="16ad7-203">Na maioria das vezes, se você se ater a propriedades somente compositor e evitar a tinta completamente, você deve observar uma melhoria importante no desempenho, mas você precisa ter cuidado com as contagens excessivas de camadas.</span><span class="sxs-lookup"><span data-stu-id="16ad7-203">For the most part, if you stick to compositor-only properties and avoid paint altogether, you should notice a major improvement in performance, but you need to watch out for excessive layer counts.</span></span>  <!--Navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <a name="paint-and-composite-tools"></a><span data-ttu-id="16ad7-204">Tinta e composição: Ferramentas</span><span class="sxs-lookup"><span data-stu-id="16ad7-204">Paint and composite: Tools</span></span>  

<span data-ttu-id="16ad7-205">Quer saber quanto tempo a pintura leva ou com que frequência a pintura ocorre?</span><span class="sxs-lookup"><span data-stu-id="16ad7-205">Want to know how long painting takes or how often painting occurs?</span></span>  <span data-ttu-id="16ad7-206">Verifique a [configuração Habilitar instrumentação de][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] tinta avançada no painel **Desempenho** e, em seguida, fazer uma gravação.</span><span class="sxs-lookup"><span data-stu-id="16ad7-206">Check the [Enable advanced paint instrumentation][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] setting in the **Performance** panel and then take a recording.</span></span>  <span data-ttu-id="16ad7-207">Se a maior parte do tempo de renderização for gasto pintando, você terá problemas de tinta.</span><span class="sxs-lookup"><span data-stu-id="16ad7-207">If most of your rendering time is spent painting, you have paint problems.</span></span>  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <a name="paint-and-composite-problems"></a><span data-ttu-id="16ad7-208">Tinta e composição: Problemas</span><span class="sxs-lookup"><span data-stu-id="16ad7-208">Paint and composite: Problems</span></span>  

<span data-ttu-id="16ad7-209">A tabela a seguir descreve alguns problemas comuns de tinta e composição e possíveis soluções.</span><span class="sxs-lookup"><span data-stu-id="16ad7-209">The following table describes some common paint and composite problems and potential solutions.</span></span>  

| <span data-ttu-id="16ad7-210">Problema</span><span class="sxs-lookup"><span data-stu-id="16ad7-210">Problem</span></span> | <span data-ttu-id="16ad7-211">Exemplo</span><span class="sxs-lookup"><span data-stu-id="16ad7-211">Example</span></span> | <span data-ttu-id="16ad7-212">Solução</span><span class="sxs-lookup"><span data-stu-id="16ad7-212">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="16ad7-213">Tempestades de tinta que afetam a resposta ou animação.</span><span class="sxs-lookup"><span data-stu-id="16ad7-213">Paint storms affecting response or animation.</span></span>  | <span data-ttu-id="16ad7-214">Áreas de tinta grande ou tintas caras que afetam a resposta ou animação.</span><span class="sxs-lookup"><span data-stu-id="16ad7-214">Big paint areas or expensive paints affecting response or animation.</span></span>  | <span data-ttu-id="16ad7-215">Evite tinta, promova elementos que estão se movendo para sua própria camada, use transformes e opacidade.</span><span class="sxs-lookup"><span data-stu-id="16ad7-215">Avoid paint, promote elements that are moving to their own layer, use transforms and opacity.</span></span>  <!--Navigate to [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| <span data-ttu-id="16ad7-216">Explosões de camada que afetam animações.</span><span class="sxs-lookup"><span data-stu-id="16ad7-216">Layer explosions affecting animations.</span></span>  | <span data-ttu-id="16ad7-217">A superpromoção de muitos elementos com afeta muito o desempenho `translateZ(0)` da animação.</span><span class="sxs-lookup"><span data-stu-id="16ad7-217">Overpromotion of too many elements with `translateZ(0)` greatly affects animation performance.</span></span>  | <span data-ttu-id="16ad7-218">Promova para camadas com moderação e somente quando você sabe que ele oferece melhorias tangíveis.</span><span class="sxs-lookup"><span data-stu-id="16ad7-218">Promote to layers sparingly, and only when you know it offers tangible improvements.</span></span>  <!--Navigate to [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="16ad7-219">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="16ad7-219">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Acelerar o tempo de execução do JavaScript | Microsoft Docs"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#turn-on-advanced-paint-instrumentation "Ativar instrumentação de tinta avançada - Referência de análise de desempenho | Microsoft Docs"

<!--[DevtoolsRenderingToolsForcedSynchronousLayouts]: ./rendering-tools/forced-synchronous-layouts.md "Diagnose Forced Synchronous Layouts | Microsoft Docs"  -->  

<!-- The Timeline Tool page is deprecated  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfileJavascript]: ../evaluate-performance/timeline-tool#profile-javascript "Profile JavaScript - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfilePainting]: ../evaluate-performance/timeline-tool#profile-painting "Profile painting - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRecording]: ../evaluate-performance/timeline-tool#make-a-recording "Make a recording - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRenderingSettings]: ../evaluate-performance/timeline-tool#rendering-settings "Rendering settings - How to Use the Timeline Tool | Microsoft Docs"  -->  

<!--[WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing "Avoid Large, Complex Layouts, and Layout Thrashing"  -->  
<!--[WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime]: /web/fundamentals/performance/rendering/optimize-javascript-execution "Optimize JavaScript Runtime"  -->  
<!--[WebFundamentalsPerformanceRenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations "Reduce the Scope and Complexity of Style Calculations"  -->  
<!--[WebFundamentalsPerformanceRenderingSimplifyPaintComplexity]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas "Simplify Paint Complexity and Reduce Paint Areas"  -->  
<!--[WebFundamentalsPerformanceRenderingCompositorOnlyProperties]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count "Stick to Compositor-Only Properties and Manage Layer Count"  -->  

[CssTriggers]: https://csstriggers.com "Gatilhos CSS"  

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Usando web workers | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Lista de verificação de desempenho do tempo de execução - Calendário de desempenho da Web"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> <span data-ttu-id="16ad7-226">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="16ad7-226">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="16ad7-227">A página original [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) é encontrada aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) e [Meggin Kearney][MegginKearney] \(Tech Writer\).</span><span class="sxs-lookup"><span data-stu-id="16ad7-227">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="16ad7-229">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="16ad7-229">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
