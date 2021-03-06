---
description: Saiba como usar o Microsoft Edge e o DevTools para encontrar problemas de memória que afetam o desempenho da página, incluindo vazamentos de memória, inchação de memória e coletas de lixo frequentes.
title: Corrigir problemas de memória
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: afaea8ca561bd975490d9153cda40877786a0f08
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397829"
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

# <a name="fix-memory-problems"></a><span data-ttu-id="518bf-104">Corrigir problemas de memória</span><span class="sxs-lookup"><span data-stu-id="518bf-104">Fix memory problems</span></span>  

<span data-ttu-id="518bf-105">Saiba como usar o Microsoft Edge e o DevTools para encontrar problemas de memória que afetam o desempenho da página, incluindo vazamentos de memória, inchação de memória e coletas de lixo frequentes.</span><span class="sxs-lookup"><span data-stu-id="518bf-105">Learn how to use Microsoft Edge and DevTools to find memory issues that affect page performance, including memory leaks, memory bloat, and frequent garbage collections.</span></span>  

### <a name="summary"></a><span data-ttu-id="518bf-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="518bf-106">Summary</span></span>  

*   <span data-ttu-id="518bf-107">Descubra quanta memória sua página está usando no momento com o Gerenciador de Tarefas do Navegador do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="518bf-107">Find out how much memory your page is currently using with the Microsoft Edge Browser Task Manager.</span></span>  
*   <span data-ttu-id="518bf-108">Visualize o uso de memória ao longo do tempo com o **painel Memória.**</span><span class="sxs-lookup"><span data-stu-id="518bf-108">Visualize memory usage over time with the **Memory** panel.</span></span>  
*   <span data-ttu-id="518bf-109">Identificar árvores DOM desvinculadas \(uma causa comum de vazamentos de memória\) com **o instantâneo heap**.</span><span class="sxs-lookup"><span data-stu-id="518bf-109">Identify detached DOM trees \(a common cause of memory leaks\) with **Heap snapshot**.</span></span>  
*   <span data-ttu-id="518bf-110">Descubra quando a nova memória está sendo alocada em sua pilha JavaScript \(pilha JS\) com **instrumentação de**Alocação na linha do tempo .</span><span class="sxs-lookup"><span data-stu-id="518bf-110">Find out when new memory is being allocated in your JavaScript heap \(JS heap\) with **Allocation instrumentation on timeline**.</span></span>  

## <a name="overview"></a><span data-ttu-id="518bf-111">Visão geral</span><span class="sxs-lookup"><span data-stu-id="518bf-111">Overview</span></span>  

<span data-ttu-id="518bf-112">No espírito do modelo de desempenho **rail,** o foco de seus esforços de desempenho deve ser seus usuários.</span><span class="sxs-lookup"><span data-stu-id="518bf-112">In the spirit of the **RAIL** performance model, the focus of your performance efforts should be your users.</span></span>  

<!--todo: add RAIL section when available  -->  

<span data-ttu-id="518bf-113">Problemas de memória são importantes porque eles geralmente são compreensíveis pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="518bf-113">Memory issues are important because they are often perceivable by users.</span></span>  <span data-ttu-id="518bf-114">Os usuários podem perceber problemas de memória das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="518bf-114">Users may perceive memory issues in the following ways:</span></span>  

*   <span data-ttu-id="518bf-115">**O desempenho de uma página piora progressivamente ao longo do tempo.**</span><span class="sxs-lookup"><span data-stu-id="518bf-115">**The performance of a page gets progressively worse over time**.</span></span>  <span data-ttu-id="518bf-116">Isso é possivelmente um sintoma de um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="518bf-116">This is possibly a symptom of a memory leak.</span></span>  <span data-ttu-id="518bf-117">Um vazamento de memória é quando um bug na página faz com que a página use progressivamente mais e mais memória ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="518bf-117">A memory leak is when a bug in the page causes the page to progressively use more and more memory over time.</span></span>  
*   <span data-ttu-id="518bf-118">**O desempenho de uma página é consistentemente ruim.**</span><span class="sxs-lookup"><span data-stu-id="518bf-118">**The performance of a page is consistently bad**.</span></span>  <span data-ttu-id="518bf-119">Isso é possivelmente um sintoma de inchação de memória.</span><span class="sxs-lookup"><span data-stu-id="518bf-119">This is possibly a symptom of memory bloat.</span></span>  <span data-ttu-id="518bf-120">O inchação da memória é quando uma página usa mais memória do que o necessário para a velocidade ideal da página.</span><span class="sxs-lookup"><span data-stu-id="518bf-120">Memory bloat is when a page uses more memory than is necessary for optimal page speed.</span></span>  
*   <span data-ttu-id="518bf-121">**O desempenho de uma página é atrasado ou parece pausar com frequência.**</span><span class="sxs-lookup"><span data-stu-id="518bf-121">**The performance of a page is delayed or appears to pause frequently**.</span></span>  <span data-ttu-id="518bf-122">Isso é possivelmente um sintoma de coletas de lixo frequentes.</span><span class="sxs-lookup"><span data-stu-id="518bf-122">This is possibly a symptom of frequent garbage collections.</span></span>  <span data-ttu-id="518bf-123">Coleta de lixo é quando o navegador recupera memória.</span><span class="sxs-lookup"><span data-stu-id="518bf-123">Garbage collection is when the browser reclaims memory.</span></span>  <span data-ttu-id="518bf-124">O navegador decide quando isso acontece.</span><span class="sxs-lookup"><span data-stu-id="518bf-124">The browser decides when this happens.</span></span>  <span data-ttu-id="518bf-125">Durante as coleções, todo o script em execução é pausado.</span><span class="sxs-lookup"><span data-stu-id="518bf-125">During collections, all script running is paused.</span></span>  <span data-ttu-id="518bf-126">Portanto, se o navegador estiver coletando muito lixo, o tempo de execução do script será bastante pausado.</span><span class="sxs-lookup"><span data-stu-id="518bf-126">So if the browser is garbage collecting a lot, script runtime is going to get paused a lot.</span></span>  

### <a name="memory-bloat-how-much-is-too-much"></a><span data-ttu-id="518bf-127">Inchação da memória: quanto é "muito"?</span><span class="sxs-lookup"><span data-stu-id="518bf-127">Memory bloat: how much is "too much"?</span></span>  

<span data-ttu-id="518bf-128">Um vazamento de memória é fácil de definir.</span><span class="sxs-lookup"><span data-stu-id="518bf-128">A memory leak is easy to define.</span></span>  <span data-ttu-id="518bf-129">Se um site estiver usando progressivamente mais e mais memória, você terá um vazamento.</span><span class="sxs-lookup"><span data-stu-id="518bf-129">If a site is progressively using more and more memory, then you have a leak.</span></span>  <span data-ttu-id="518bf-130">Mas o inchar da memória é um pouco mais difícil de fixar.</span><span class="sxs-lookup"><span data-stu-id="518bf-130">But memory bloat is a bit harder to pin down.</span></span>  <span data-ttu-id="518bf-131">O que se qualifica como "usar muita memória"?</span><span class="sxs-lookup"><span data-stu-id="518bf-131">What qualifies as "using too much memory"?</span></span>  

<span data-ttu-id="518bf-132">Não há números rígidos aqui, porque diferentes dispositivos e navegadores têm recursos diferentes.</span><span class="sxs-lookup"><span data-stu-id="518bf-132">There are no hard numbers here, because different devices and browsers have different capabilities.</span></span>  <span data-ttu-id="518bf-133">A mesma página que é executado sem problemas em um smartphone high-end pode falhar em um smartphone low-end.</span><span class="sxs-lookup"><span data-stu-id="518bf-133">The same page that runs smoothly on a high-end smartphone may crash on a low-end smartphone.</span></span>  

<span data-ttu-id="518bf-134">A chave aqui é usar o modelo RAIL e se concentrar em seus usuários.</span><span class="sxs-lookup"><span data-stu-id="518bf-134">The key here is to use the RAIL model and focus on your users.</span></span>  <span data-ttu-id="518bf-135">Descubra quais dispositivos são populares com seus usuários e teste sua página nesses dispositivos.</span><span class="sxs-lookup"><span data-stu-id="518bf-135">Find out what devices are popular with your users, and then test out your page on those devices.</span></span>  <span data-ttu-id="518bf-136">Se a experiência for consistentemente ruim, a página pode estar excedendo os recursos de memória desses dispositivos.</span><span class="sxs-lookup"><span data-stu-id="518bf-136">If the experience is consistently bad, the page may be exceeding the memory capabilities of those devices.</span></span>  

## <a name="monitor-memory-use-in-realtime-with-the-microsoft-edge-browser-task-manager"></a><span data-ttu-id="518bf-137">Monitorar o uso de memória em tempo real com o Gerenciador de Tarefas do Navegador do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="518bf-137">Monitor memory use in realtime with the Microsoft Edge Browser Task Manager</span></span>  

<span data-ttu-id="518bf-138">Use o Gerenciador de Tarefas do Navegador do Microsoft Edge como ponto de partida para a investigação de problemas de memória.</span><span class="sxs-lookup"><span data-stu-id="518bf-138">Use the Microsoft Edge Browser Task Manager as a starting point to your memory issue investigation.</span></span>  <span data-ttu-id="518bf-139">O Gerenciador de Tarefas do Navegador do Microsoft Edge é um monitor em tempo real que informa a memória que uma página está usando no momento.</span><span class="sxs-lookup"><span data-stu-id="518bf-139">The Microsoft Edge Browser Task Manager is a realtime monitor that tells you how much memory a page is currently using.</span></span>  

1.  <span data-ttu-id="518bf-140">Selecione `Shift` + `Esc` ou navegue até o menu principal do Microsoft Edge \*\*\*\* e escolha Mais ferramentas  >  **Gerenciador** de Tarefas do Navegador para abrir o Gerenciador de Tarefas do Navegador do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="518bf-140">Select `Shift`+`Esc` or navigate to the Microsoft Edge main menu and choose **More tools** > **Browser Task Manager** to open the Microsoft Edge Browser Task Manager.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Abrindo o Gerenciador de Tarefas do Navegador do Microsoft Edge" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       <span data-ttu-id="518bf-142">Figura 1: Abrindo o Gerenciador de Tarefas do Navegador do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="518bf-142">Figure 1:  Opening the Microsoft Edge Browser Task Manager</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="518bf-143">Passe o mouse no header da tabela do Gerenciador de Tarefas do Navegador do Microsoft Edge, abra o menu contextual \(clique com o botão direito do mouse\) e habilite a memória **JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="518bf-143">Hover on the table header of the Microsoft Edge Browser Task Manager, open the contextual menu \(right-click\), and enable **JavaScript memory**.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Habilitar memória JavaScript" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       <span data-ttu-id="518bf-145">Figura 2: Habilitar memória JavaScript</span><span class="sxs-lookup"><span data-stu-id="518bf-145">Figure 2:  Enable JavaScript memory</span></span>  
    :::image-end:::  
    
<span data-ttu-id="518bf-146">Essas duas colunas contam coisas diferentes sobre como sua página está usando memória.</span><span class="sxs-lookup"><span data-stu-id="518bf-146">These two columns tell you different things about how your page is using memory.</span></span>  

*   <span data-ttu-id="518bf-147">A **coluna Memória** representa a memória nativa.</span><span class="sxs-lookup"><span data-stu-id="518bf-147">The **Memory** column represents native memory.</span></span>  <span data-ttu-id="518bf-148">Nós DOM são armazenados na memória nativa.</span><span class="sxs-lookup"><span data-stu-id="518bf-148">DOM nodes are stored in native memory.</span></span>  <span data-ttu-id="518bf-149">Se esse valor estiver aumentando, nós DOM serão criados.</span><span class="sxs-lookup"><span data-stu-id="518bf-149">If this value is increasing, DOM nodes are getting created.</span></span>  
*   <span data-ttu-id="518bf-150">A **coluna Memória JavaScript** representa a pilha JS.</span><span class="sxs-lookup"><span data-stu-id="518bf-150">The **JavaScript Memory** column represents the JS heap.</span></span>  <span data-ttu-id="518bf-151">Esta coluna contém dois valores.</span><span class="sxs-lookup"><span data-stu-id="518bf-151">This column contains two values.</span></span>  <span data-ttu-id="518bf-152">O valor em que você está interessado é o número ao vivo \(o número entre parênteses\).</span><span class="sxs-lookup"><span data-stu-id="518bf-152">The value you are interested in is the live number \(the number in parentheses\).</span></span>  <span data-ttu-id="518bf-153">O número ao vivo representa a quantidade de memória que os objetos acessíveis em sua página estão usando.</span><span class="sxs-lookup"><span data-stu-id="518bf-153">The live number represents how much memory the reachable objects on your page are using.</span></span>  <span data-ttu-id="518bf-154">Se esse número estiver aumentando, novos objetos estão sendo criados ou os objetos existentes estão crescendo.</span><span class="sxs-lookup"><span data-stu-id="518bf-154">If this number is increasing, either new objects are being created, or the existing objects are growing.</span></span>  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <a name="visualize-memory-leaks-with-performance-panel"></a><span data-ttu-id="518bf-155">Visualizar vazamentos de memória com painel desempenho</span><span class="sxs-lookup"><span data-stu-id="518bf-155">Visualize memory leaks with Performance panel</span></span>  

<span data-ttu-id="518bf-156">Você também pode usar o painel Desempenho como outro ponto de partida em sua investigação.</span><span class="sxs-lookup"><span data-stu-id="518bf-156">You may also use the Performance panel as another starting point in your investigation.</span></span>  <span data-ttu-id="518bf-157">O painel Desempenho ajuda você a visualizar o uso de memória de uma página ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="518bf-157">The Performance panel helps you visualize the memory use of a page over time.</span></span>  

1.  <span data-ttu-id="518bf-158">Abra o **painel Desempenho** no DevTools.</span><span class="sxs-lookup"><span data-stu-id="518bf-158">Open the **Performance** panel on DevTools.</span></span>  
1.  <span data-ttu-id="518bf-159">Habilita **a caixa de** seleção Memória.</span><span class="sxs-lookup"><span data-stu-id="518bf-159">Enable the **Memory** checkbox.</span></span>  
1.  <span data-ttu-id="518bf-160">[Faça uma gravação][DevtoolsEvaluatePerformanceReferenceRecord].</span><span class="sxs-lookup"><span data-stu-id="518bf-160">[Make a recording][DevtoolsEvaluatePerformanceReferenceRecord].</span></span>  

> [!TIP]
> <span data-ttu-id="518bf-161">É uma boa prática iniciar e encerrar sua gravação com uma coleta de lixo forçada.</span><span class="sxs-lookup"><span data-stu-id="518bf-161">It is a good practice to start and end your recording with a forced garbage collection.</span></span>  <span data-ttu-id="518bf-162">Para forçar a coleta de lixo, escolha o botão **coletar** lixo ![ force coleta de lixo durante a ][ImageForceGarbageCollectionIcon] gravação.</span><span class="sxs-lookup"><span data-stu-id="518bf-162">To force garbage collection, choose the **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button while recording.</span></span>  

<span data-ttu-id="518bf-163">Para demonstrar gravações de memória, considere o código abaixo:</span><span class="sxs-lookup"><span data-stu-id="518bf-163">To demonstrate memory recordings, consider the code below:</span></span>  

```javascript
var x = [];
function grow() {
    for (var i = 0; i < 10000; i++) {
        document.body.appendChild(document.createElement('div'));
    }
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="518bf-164">Sempre que o botão referenciado no código é escolhido, dez mil nós são anexados ao corpo do documento e uma cadeia de caracteres de um milhão de caracteres é empurrada para a `div` `x` `x` matriz.</span><span class="sxs-lookup"><span data-stu-id="518bf-164">Every time that the button referenced in the code is chosen, ten thousand `div` nodes are appended to the document body, and a string of one million `x` characters is pushed onto the `x` array.</span></span>  <span data-ttu-id="518bf-165">Executar o exemplo de código anterior produz uma gravação no painel **Desempenho** como a figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="518bf-165">Running the previous code sample produces a recording in the **Performance** panel like the following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Crescimento simples" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   <span data-ttu-id="518bf-167">Figura 3: Crescimento simples</span><span class="sxs-lookup"><span data-stu-id="518bf-167">Figure 3:  Simple growth</span></span>  
:::image-end:::  

<span data-ttu-id="518bf-168">Primeiro, uma explicação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="518bf-168">First, an explanation of the user interface.</span></span>  <span data-ttu-id="518bf-169">O **gráfico HEAP** no painel **Visão** geral \(abaixo de **NET**\) representa a pilha JS.</span><span class="sxs-lookup"><span data-stu-id="518bf-169">The **HEAP** graph in the **Overview** pane \(below **NET**\) represents the JS heap.</span></span>  <span data-ttu-id="518bf-170">Abaixo do **painel Visão** geral está o **painel Contador.**</span><span class="sxs-lookup"><span data-stu-id="518bf-170">Below the **Overview** pane is the **Counter** pane.</span></span>  <span data-ttu-id="518bf-171">O uso da memória é dividido pela pilha JS \(mesmo que o gráfico **HEAP** no **painel** Visão geral\), documentos, nós DOM, ouvintes e memória GPU.</span><span class="sxs-lookup"><span data-stu-id="518bf-171">The memory usage is broken down by JS heap \(same as **HEAP** graph in the **Overview** pane\), documents, DOM nodes, listeners, and GPU memory.</span></span>  <span data-ttu-id="518bf-172">Desativar uma caixa de seleção para escondê-la do gráfico.</span><span class="sxs-lookup"><span data-stu-id="518bf-172">Turn off a checkbox to hide it from the graph.</span></span>  

<span data-ttu-id="518bf-173">Agora, uma análise do código em comparação com a figura anterior.</span><span class="sxs-lookup"><span data-stu-id="518bf-173">Now, an analysis of the code compared with the previous figure.</span></span>  <span data-ttu-id="518bf-174">Se você revisar o contador de nó \(o gráfico verde\), ele corresponde limpo ao código.</span><span class="sxs-lookup"><span data-stu-id="518bf-174">If you review the node counter \(the green graph\), it matches up cleanly with the code.</span></span>  <span data-ttu-id="518bf-175">A contagem de nós aumenta em etapas discretas.</span><span class="sxs-lookup"><span data-stu-id="518bf-175">The node count increases in discrete steps.</span></span>  <span data-ttu-id="518bf-176">Você pode presumir que cada aumento na contagem de nós é uma chamada para `grow()` .</span><span class="sxs-lookup"><span data-stu-id="518bf-176">You may presume that each increase in the node count is a call to `grow()`.</span></span>  <span data-ttu-id="518bf-177">O gráfico de pilha JS \(o gráfico azul\) não é tão simples.</span><span class="sxs-lookup"><span data-stu-id="518bf-177">The JS heap graph \(the blue graph\) is not as straightforward.</span></span>  <span data-ttu-id="518bf-178">De acordo com as práticas recomendadas, o primeiro dip \*\*\*\* é, na verdade, um conjunto de lixo forçado \(escolha o botão coletar coleta de lixo ![ ][ImageForceGarbageCollectionIcon] forçado\).</span><span class="sxs-lookup"><span data-stu-id="518bf-178">In keeping with best practices, the first dip is actually a forced garbage collection \(choose the  **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button\).</span></span>  <span data-ttu-id="518bf-179">À medida que a gravação progride, os picos de tamanho da pilha JS são exibidos.</span><span class="sxs-lookup"><span data-stu-id="518bf-179">As the recording progresses, the JS heap size spikes are displayed.</span></span>  <span data-ttu-id="518bf-180">Isso é natural e esperado: o código JavaScript está criando os nós DOM em cada botão que você escolher e fazendo muito trabalho quando cria a cadeia de caracteres de um milhão de caracteres.</span><span class="sxs-lookup"><span data-stu-id="518bf-180">This is natural and expected:  the JavaScript code is creating the DOM nodes on every button you choose and doing a lot of work when it creates the string of one million characters.</span></span>  <span data-ttu-id="518bf-181">O principal aqui é o fato de que a pilha JS termina mais alto do que começou \(o "início" aqui sendo o ponto após a coleta de lixo forçada\).</span><span class="sxs-lookup"><span data-stu-id="518bf-181">The key thing here is the fact that the JS heap ends higher than it began \(the "beginning" here being the point after the forced garbage collection\).</span></span>  <span data-ttu-id="518bf-182">No mundo real, se você viu esse padrão de aumento do tamanho da pilha JS ou tamanho do nó, ele pode definir potencialmente um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="518bf-182">In the real world, if you saw this pattern of increasing JS heap size or node size, it may potentially define a memory leak.</span></span>  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <a name="discover-detached-dom-tree-memory-leaks-with-heap-snapshots"></a><span data-ttu-id="518bf-183">Descobrir vazamentos de memória de árvore DOM desvinculados com Instantâneos de Pilha</span><span class="sxs-lookup"><span data-stu-id="518bf-183">Discover detached DOM tree memory leaks with Heap Snapshots</span></span>  

<span data-ttu-id="518bf-184">Um nó DOM é apenas lixo coletado quando não há referências ao nó da árvore DOM ou do código JavaScript em execução na página.</span><span class="sxs-lookup"><span data-stu-id="518bf-184">A DOM node is only garbage collected when there are no references to the node from either the DOM tree or JavaScript code running on the page.</span></span>  <span data-ttu-id="518bf-185">Um nó é dito como "desvinculado" quando é removido da árvore DOM, mas alguns JavaScript ainda a referenciam.</span><span class="sxs-lookup"><span data-stu-id="518bf-185">A node is said to be "detached" when it is removed from the DOM tree but some JavaScript still references it.</span></span>  <span data-ttu-id="518bf-186">Nós DOM desvinculados são uma causa comum de vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="518bf-186">Detached DOM nodes are a common cause of memory leaks.</span></span>  <span data-ttu-id="518bf-187">Esta seção ensina como usar os perfis de pilha no DevTools para identificar nós desvinculados.</span><span class="sxs-lookup"><span data-stu-id="518bf-187">This section teaches you how to use the heap profilers in DevTools to identify detached nodes.</span></span>  

<span data-ttu-id="518bf-188">Aqui está um exemplo simples de nós DOM desvinculados.</span><span class="sxs-lookup"><span data-stu-id="518bf-188">Here is a simple example of detached DOM nodes.</span></span>  

```javascript
var detachedTree;

function create() {
    var ul = document.createElement('ul');
    for (var i = 0; i < 10; i++) {
        var li = document.createElement('li');
        ul.appendChild(li);
    }
    detachedTree = ul;
}
document.getElementById('create').addEventListener('click', create);
```  

<span data-ttu-id="518bf-189">Escolher o botão referenciado no código cria um `ul` nó com dez `li` filhos.</span><span class="sxs-lookup"><span data-stu-id="518bf-189">Choosing the button referenced in the code creates a `ul` node with ten `li` children.</span></span>  <span data-ttu-id="518bf-190">Os nós são referenciados pelo código, mas não existem na árvore DOM, portanto, cada um é desvinculado.</span><span class="sxs-lookup"><span data-stu-id="518bf-190">The nodes are referenced by the code but do not exist in the DOM tree, so each is detached.</span></span>  

<span data-ttu-id="518bf-191">Instantâneos de pilha são uma maneira de identificar nós desvinculados.</span><span class="sxs-lookup"><span data-stu-id="518bf-191">Heap snapshots are one way to identify detached nodes.</span></span>  <span data-ttu-id="518bf-192">Como o nome sugere, os instantâneos de pilha mostram como a memória é distribuída entre os objetos JS e nós DOM para sua página no momento do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="518bf-192">As the name implies, heap snapshots show you how memory is distributed among the JS objects and DOM nodes for your page at the point of time of the snapshot.</span></span>  

<span data-ttu-id="518bf-193">Para criar um instantâneo, abra DevTools e navegue até o painel Memória, escolha o botão de > **de** instantâneo de pilha. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="518bf-193">To create a snapshot, open DevTools and navigate to the **Memory** panel, choose the **Heap snapshot** radio button > **Take snapshot** button.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Fazer instantâneo de pilha" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   <span data-ttu-id="518bf-195">Figura 4: Fazer instantâneo de pilha</span><span class="sxs-lookup"><span data-stu-id="518bf-195">Figure 4:  Take heap snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="518bf-196">O instantâneo pode levar algum tempo para processar e carregar.</span><span class="sxs-lookup"><span data-stu-id="518bf-196">The snapshot may take some time to process and load.</span></span>  <span data-ttu-id="518bf-197">Depois que terminar, selecione-o no painel à esquerda \(denominado **HEAP SNAPSHOTS**\).</span><span class="sxs-lookup"><span data-stu-id="518bf-197">After it is finished, select it from the left-hand panel \(named **HEAP SNAPSHOTS**\).</span></span>  

<span data-ttu-id="518bf-198">Digite `Detached` na caixa de texto **Filtro** de classe para pesquisar árvores DOM desvinculadas.</span><span class="sxs-lookup"><span data-stu-id="518bf-198">Type `Detached` in the **Class filter** textbox to search for detached DOM trees.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Filtragem para nós desvinculados" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   <span data-ttu-id="518bf-200">Figura 5: Filtragem para nós desvinculados</span><span class="sxs-lookup"><span data-stu-id="518bf-200">Figure 5:  Filtering for detached nodes</span></span>  
:::image-end:::  

<span data-ttu-id="518bf-201">Expanda os quilates para investigar uma árvore desvinculada.</span><span class="sxs-lookup"><span data-stu-id="518bf-201">Expand the carats to investigate a detached tree.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Investigando árvore desvinculada" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   <span data-ttu-id="518bf-203">Figura 6: Investigando árvore desvinculada</span><span class="sxs-lookup"><span data-stu-id="518bf-203">Figure 6:  Investigating detached tree</span></span>  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

<span data-ttu-id="518bf-204">Escolha um nó para investigar ainda mais.</span><span class="sxs-lookup"><span data-stu-id="518bf-204">Choose a node to investigate it further.</span></span>  <span data-ttu-id="518bf-205">No painel **Objetos,** você pode revisar mais informações sobre o código que está fazendo referência a ele.</span><span class="sxs-lookup"><span data-stu-id="518bf-205">In the **Objects** pane, you may review more information about the code that is referencing it.</span></span>  <span data-ttu-id="518bf-206">Por exemplo, na figura a seguir, a `detachedNodes` variável está fazendo referência ao nó.</span><span class="sxs-lookup"><span data-stu-id="518bf-206">For example, in the following figure, the `detachedNodes` variable is referencing the node.</span></span>  <span data-ttu-id="518bf-207">Para corrigir o vazamento de memória específico, você deve estudar o código que usa a variável e garantir que a referência ao nó seja removida quando ela `detachedUNode` não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="518bf-207">To fix the particular memory leak, you should study the code that uses the `detachedUNode` variable and ensure that the reference to the node is removed when it is no longer needed.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Investigando um nó" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   <span data-ttu-id="518bf-209">Figura 7: Investigando um nó</span><span class="sxs-lookup"><span data-stu-id="518bf-209">Figure 7:  Investigating a node</span></span>  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <a name="identify-js-heap-memory-leaks-with-allocation-instrumentation-on-timeline"></a><span data-ttu-id="518bf-210">Identificar vazamentos de memória de pilha JS com instrumentação de alocação na linha do tempo</span><span class="sxs-lookup"><span data-stu-id="518bf-210">Identify JS heap memory leaks with Allocation instrumentation on timeline</span></span>  

<span data-ttu-id="518bf-211">**A instrumentação de alocação na** linha do tempo é outra ferramenta que pode ajudá-lo a rastrear vazamentos de memória na pilha JS.</span><span class="sxs-lookup"><span data-stu-id="518bf-211">**Allocation instrumentation on timeline** is another tool that may help you track down memory leaks in your JS heap.</span></span>  

<span data-ttu-id="518bf-212">Demonstrar **instrumentação de alocação na linha do tempo**  usando o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="518bf-212">Demonstrate **Allocation instrumentation on timeline**  using the following code.</span></span>  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="518bf-213">Sempre que o botão referenciado no código é pressionado, uma cadeia de caracteres de um milhão de caracteres é adicionada à `x` matriz.</span><span class="sxs-lookup"><span data-stu-id="518bf-213">Every time that the button referenced in the code is pushed, a string of one million characters is added to the `x` array.</span></span>  

<span data-ttu-id="518bf-214">Para registrar uma instrumentação de Alocação na linha \*\*\*\* do tempo, abra DevTools, navegue \*\*\*\* até o painel Memória, escolha a **instrumentação** alocação \*\*\*\* no botão de rádio linha do tempo, escolha o botão Iniciar, execute a ação que você suspeita que está causando o vazamento de memória e escolha o botão Parar a gravação de perfil de pilha de gravação parar de gravar quando ![ ][ImageStopRecordingIcon] terminar.</span><span class="sxs-lookup"><span data-stu-id="518bf-214">To record an Allocation instrumentation on timeline, open DevTools, navigate to the **Memory** panel, choose the **Allocation instrumentation on timeline** radio button, choose the **Start** button, perform the action that you suspect is causing the memory leak, and then choose the **Stop recording heap profile** ![stop recording][ImageStopRecordingIcon] button when you are done.</span></span>  

<span data-ttu-id="518bf-215">À medida que você estiver gravando, observe se alguma barra azul aparecer na instrumentação Alocação na linha do tempo, como na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="518bf-215">As you are recording, notice if any blue bars show up on the Allocation instrumentation on timeline, like in the following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Novas alocações" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   <span data-ttu-id="518bf-217">Figura 8: Novas alocações</span><span class="sxs-lookup"><span data-stu-id="518bf-217">Figure 8:  New allocations</span></span>  
:::image-end:::  

<span data-ttu-id="518bf-218">Essas barras azuis representam novas alocações de memória.</span><span class="sxs-lookup"><span data-stu-id="518bf-218">Those blue bars represent new memory allocations.</span></span>  <span data-ttu-id="518bf-219">Essas novas alocações de memória são seus candidatos a vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="518bf-219">Those new memory allocations are your candidates for memory leaks.</span></span>  <span data-ttu-id="518bf-220">Você pode ampliar uma barra para filtrar o **painel** construtor para mostrar somente objetos que foram alocados durante o período especificado.</span><span class="sxs-lookup"><span data-stu-id="518bf-220">You are able to zoom on a bar to filter the **Constructor** pane to only show objects that were allocated during the specified timeframe.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Linha do tempo de alocação ampliada" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   <span data-ttu-id="518bf-222">Figura 9: Linha do tempo de alocação ampliada</span><span class="sxs-lookup"><span data-stu-id="518bf-222">Figure 9:  Zoomed allocation timeline</span></span>  
:::image-end:::  

<span data-ttu-id="518bf-223">Expanda o objeto e selecione o valor para exibir mais detalhes no **painel Objeto.**</span><span class="sxs-lookup"><span data-stu-id="518bf-223">Expand the object and select the value to view more details in the **Object** pane.</span></span>  <span data-ttu-id="518bf-224">Por exemplo, na figura a seguir, nos detalhes do objeto recém-alocado indica que ele foi alocado à variável `x` no `Window` escopo.</span><span class="sxs-lookup"><span data-stu-id="518bf-224">For example, in the following figure, in the details of the newly allocated object indicates that it was allocated to the `x` variable in the `Window` scope.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Detalhes do objeto" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   <span data-ttu-id="518bf-226">Figura 10: Detalhes do objeto</span><span class="sxs-lookup"><span data-stu-id="518bf-226">Figure 10:  Object details</span></span>  
:::image-end:::  

## <a name="investigate-memory-allocation-by-function"></a><span data-ttu-id="518bf-227">Investigar a alocação de memória por função</span><span class="sxs-lookup"><span data-stu-id="518bf-227">Investigate memory allocation by function</span></span>  

<span data-ttu-id="518bf-228">Use o **tipo de perfil de amostragem** de alocação para exibir a alocação de memória pela função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="518bf-228">Use the **Allocation sampling** profiling type to view memory allocation by JavaScript function.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Amostragem de Alocação de Registros" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   <span data-ttu-id="518bf-230">Figura 11: Amostragem de Alocação de Registros</span><span class="sxs-lookup"><span data-stu-id="518bf-230">Figure 11:  Record Allocation sampling</span></span>  
:::image-end:::  

1.  <span data-ttu-id="518bf-231">Escolha o **botão de rádio de amostragem** de alocação.</span><span class="sxs-lookup"><span data-stu-id="518bf-231">Choose the **Allocation sampling** radio button.</span></span>  <span data-ttu-id="518bf-232">Se houver um trabalhador na página, você poderá selecionar isso como o destino da criação de perfil usando o menu suspenso ao lado do **botão Iniciar.**</span><span class="sxs-lookup"><span data-stu-id="518bf-232">If there is a worker on the page, you are able to select that as the profiling target using the dropdown menu next to the **Start** button.</span></span>  
1.  <span data-ttu-id="518bf-233">Escolha o **botão Iniciar.**</span><span class="sxs-lookup"><span data-stu-id="518bf-233">Choose the **Start** button.</span></span>  
1.  <span data-ttu-id="518bf-234">Conclua as ações na página da Web que você deseja investigar.</span><span class="sxs-lookup"><span data-stu-id="518bf-234">Complete the actions on the webpage which you want to investigate.</span></span>  
1.  <span data-ttu-id="518bf-235">Escolha o **botão Parar** quando tiver concluído todas as suas ações.</span><span class="sxs-lookup"><span data-stu-id="518bf-235">Choose the **Stop** button when you have finished all of your actions.</span></span>  

<span data-ttu-id="518bf-236">DevTools mostra uma divisão da alocação de memória por função.</span><span class="sxs-lookup"><span data-stu-id="518bf-236">DevTools shows you a breakdown of memory allocation by function.</span></span>  <span data-ttu-id="518bf-237">O modo de exibição padrão **é Heavy (Bottom Up)**, que exibe as funções que alocaram a maior parte da memória na parte superior.</span><span class="sxs-lookup"><span data-stu-id="518bf-237">The default view is **Heavy (Bottom Up)**, which displays the functions that allocated the most memory at the top.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Amostragem de alocação" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   <span data-ttu-id="518bf-239">Figura 12: Amostragem de alocação</span><span class="sxs-lookup"><span data-stu-id="518bf-239">Figure 12:  Allocation sampling</span></span>  
:::image-end:::  

## <a name="spot-frequent-garbage-collections"></a><span data-ttu-id="518bf-240">Coletas de lixo frequentes no local</span><span class="sxs-lookup"><span data-stu-id="518bf-240">Spot frequent garbage collections</span></span>  

<span data-ttu-id="518bf-241">Se sua página parece pausar com frequência, talvez você tenha problemas de coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="518bf-241">If your page appears to pause frequently, then you may have garbage collection issues.</span></span>  

<span data-ttu-id="518bf-242">Você pode usar o Gerenciador de Tarefas do Navegador do Microsoft Edge ou gravações de memória de desempenho para detectar coleta de lixo frequente.</span><span class="sxs-lookup"><span data-stu-id="518bf-242">You are able to use either the Microsoft Edge Browser Task Manager or Performance memory recordings to spot frequent garbage collection.</span></span>  <span data-ttu-id="518bf-243">No Gerenciador de Tarefas do Navegador do Microsoft Edge, os valores de **Memória** ou Memória **JavaScript** frequentemente crescentes e em queda representam coleta de lixo frequente.</span><span class="sxs-lookup"><span data-stu-id="518bf-243">In the Microsoft Edge Browser Task Manager, frequently rising and falling **Memory** or **JavaScript Memory** values represent frequent garbage collection.</span></span>  <span data-ttu-id="518bf-244">Em Gravações de desempenho, as alterações frequentes \(crescente e em queda\) para a pilha JS ou gráficos de contagem de nós indicam coleta de lixo frequente.</span><span class="sxs-lookup"><span data-stu-id="518bf-244">In Performance recordings, frequent changes \(rising and falling\) to the JS heap or node count graphs indicate frequent garbage collection.</span></span>  

<span data-ttu-id="518bf-245">Depois de identificar o problema, você poderá usar uma **instrumentação de** Alocação no registro de linha do tempo para descobrir onde a memória está sendo alocada e quais funções estão causando as alocações.</span><span class="sxs-lookup"><span data-stu-id="518bf-245">After you have identified the problem, you are able to use an **Allocation instrumentation on timeline** recording to find out where memory is being allocated and which functions are causing the allocations.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="518bf-246">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="518bf-246">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageForceGarbageCollectionIcon]: ../media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: ../media/stop-recording-icon.msft.png  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Desempenho do registro - Referência de Análise de Desempenho"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> <span data-ttu-id="518bf-248">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="518bf-248">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="518bf-249">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="518bf-249">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="518bf-251">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="518bf-251">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
