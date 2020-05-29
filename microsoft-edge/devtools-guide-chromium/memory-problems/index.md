---
title: Corrigir problemas de memória
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 738ef5fe682633f3100345c922ff12c3c27a7166
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611759"
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





# <span data-ttu-id="dd192-103">Corrigir problemas de memória</span><span class="sxs-lookup"><span data-stu-id="dd192-103">Fix Memory Problems</span></span>   



<span data-ttu-id="dd192-104">Saiba como usar o Microsoft Edge e o DevTools para encontrar problemas de memória que afetam o desempenho da página, incluindo vazamentos de memória, excesso de memória e coletas de lixo frequentes.</span><span class="sxs-lookup"><span data-stu-id="dd192-104">Learn how to use Microsoft Edge and DevTools to find memory issues that affect page performance, including memory leaks, memory bloat, and frequent garbage collections.</span></span>  

### <span data-ttu-id="dd192-105">Resumo</span><span class="sxs-lookup"><span data-stu-id="dd192-105">Summary</span></span>  

*   <span data-ttu-id="dd192-106">Verifique a quantidade de memória que sua página usa no momento com o Gerenciador de tarefas do navegador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dd192-106">Find out how much memory your page is currently using with the Microsoft Edge Browser Task Manager.</span></span>  
*   <span data-ttu-id="dd192-107">Visualize o uso da memória ao longo do tempo com o painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="dd192-107">Visualize memory usage over time with the **Memory** panel.</span></span>  
*   <span data-ttu-id="dd192-108">Identificar árvores de DOM desanexadas \ (uma causa comum de vazamentos de memória \) com o **instantâneo de heap**.</span><span class="sxs-lookup"><span data-stu-id="dd192-108">Identify detached DOM trees \(a common cause of memory leaks\) with **Heap snapshot**.</span></span>  
*   <span data-ttu-id="dd192-109">Descubra quando está sendo atribuída uma nova memória no seu heap JavaScript \ (JS! heap \) com a **Instrumentação de distribuição na linha do tempo**.</span><span class="sxs-lookup"><span data-stu-id="dd192-109">Find out when new memory is being allocated in your JavaScript heap \(JS heap\) with **Allocation instrumentation on timeline**.</span></span>  

## <span data-ttu-id="dd192-110">Visão geral</span><span class="sxs-lookup"><span data-stu-id="dd192-110">Overview</span></span>  

<span data-ttu-id="dd192-111">No espírito do modelo de desempenho do **trilho** , o foco de seus esforços de desempenho deve ser seus usuários.</span><span class="sxs-lookup"><span data-stu-id="dd192-111">In the spirit of the **RAIL** performance model, the focus of your performance efforts should be your users.</span></span>  

<!--todo: add RAIL section when available  -->  

<span data-ttu-id="dd192-112">Os problemas de memória são importantes porque costumam ser percebêveis pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="dd192-112">Memory issues are important because they are often perceivable by users.</span></span>  <span data-ttu-id="dd192-113">Os usuários podem perceber problemas de memória das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="dd192-113">Users may perceive memory issues in the following ways:</span></span>  

*   <span data-ttu-id="dd192-114">**O desempenho de uma página é piormente pior ao longo do tempo**.</span><span class="sxs-lookup"><span data-stu-id="dd192-114">**The performance of a page gets progressively worse over time**.</span></span>  <span data-ttu-id="dd192-115">Isso possivelmente é um sintoma de perda de memória.</span><span class="sxs-lookup"><span data-stu-id="dd192-115">This is possibly a symptom of a memory leak.</span></span>  <span data-ttu-id="dd192-116">Um vazamento de memória é quando um bug na página faz com que a página use cada vez mais e mais memória ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="dd192-116">A memory leak is when a bug in the page causes the page to progressively use more and more memory over time.</span></span>  
*   <span data-ttu-id="dd192-117">**O desempenho de uma página é consistentemente ruim**.</span><span class="sxs-lookup"><span data-stu-id="dd192-117">**The performance of a page is consistently bad**.</span></span>  <span data-ttu-id="dd192-118">Isso possivelmente é um sintoma de excesso de memória.</span><span class="sxs-lookup"><span data-stu-id="dd192-118">This is possibly a symptom of memory bloat.</span></span>  <span data-ttu-id="dd192-119">O excesso de memória é quando uma página usa mais memória do que o necessário para a velocidade de página ideal.</span><span class="sxs-lookup"><span data-stu-id="dd192-119">Memory bloat is when a page uses more memory than is necessary for optimal page speed.</span></span>  
*   <span data-ttu-id="dd192-120">**O desempenho de uma página é atrasado ou parece pausar com frequência**.</span><span class="sxs-lookup"><span data-stu-id="dd192-120">**The performance of a page is delayed or appears to pause frequently**.</span></span>  <span data-ttu-id="dd192-121">Isso possivelmente é um sintoma de coletas de lixo frequentes.</span><span class="sxs-lookup"><span data-stu-id="dd192-121">This is possibly a symptom of frequent garbage collections.</span></span>  <span data-ttu-id="dd192-122">Coleta de lixo é quando o navegador recupera memória.</span><span class="sxs-lookup"><span data-stu-id="dd192-122">Garbage collection is when the browser reclaims memory.</span></span>  <span data-ttu-id="dd192-123">O navegador decide quando isso acontece.</span><span class="sxs-lookup"><span data-stu-id="dd192-123">The browser decides when this happens.</span></span>  <span data-ttu-id="dd192-124">Durante as coletas, todos os scripts em execução são pausados.</span><span class="sxs-lookup"><span data-stu-id="dd192-124">During collections, all script running is paused.</span></span>  <span data-ttu-id="dd192-125">Portanto, se o navegador estiver coletando um lote, o tempo de execução de script será pausado muito.</span><span class="sxs-lookup"><span data-stu-id="dd192-125">So if the browser is garbage collecting a lot, script runtime is going to get paused a lot.</span></span>  

### <span data-ttu-id="dd192-126">Inflação da memória: quanto custa "muito grande"?</span><span class="sxs-lookup"><span data-stu-id="dd192-126">Memory bloat: how much is "too much"?</span></span>  

<span data-ttu-id="dd192-127">É fácil definir um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="dd192-127">A memory leak is easy to define.</span></span>  <span data-ttu-id="dd192-128">Se um site estiver usando um número cada vez maior de memória, você terá um vazamento.</span><span class="sxs-lookup"><span data-stu-id="dd192-128">If a site is progressively using more and more memory, then you have a leak.</span></span>  <span data-ttu-id="dd192-129">Mas o excesso de memória é um pouco mais difícil de fixar.</span><span class="sxs-lookup"><span data-stu-id="dd192-129">But memory bloat is a bit harder to pin down.</span></span>  <span data-ttu-id="dd192-130">O que é qualificado como "usando muita memória"?</span><span class="sxs-lookup"><span data-stu-id="dd192-130">What qualifies as "using too much memory"?</span></span>  

<span data-ttu-id="dd192-131">Não há números rígidos aqui, porque diferentes dispositivos e navegadores têm recursos diferentes.</span><span class="sxs-lookup"><span data-stu-id="dd192-131">There are no hard numbers here, because different devices and browsers have different capabilities.</span></span>  <span data-ttu-id="dd192-132">A mesma página que é executada tranqüilamente em um smartphone high-end pode falhar em um smartphone low-end.</span><span class="sxs-lookup"><span data-stu-id="dd192-132">The same page that runs smoothly on a high-end smartphone may crash on a low-end smartphone.</span></span>  

<span data-ttu-id="dd192-133">A chave aqui é usar o modelo de trilho e enfocar seus usuários.</span><span class="sxs-lookup"><span data-stu-id="dd192-133">The key here is to use the RAIL model and focus on your users.</span></span>  <span data-ttu-id="dd192-134">Descubra quais dispositivos são populares com seus usuários e teste sua página nesses dispositivos.</span><span class="sxs-lookup"><span data-stu-id="dd192-134">Find out what devices are popular with your users, and then test out your page on those devices.</span></span>  <span data-ttu-id="dd192-135">Se a experiência for ruim consistentemente, a página pode estar excedendo os recursos de memória desses dispositivos.</span><span class="sxs-lookup"><span data-stu-id="dd192-135">If the experience is consistently bad, the page may be exceeding the memory capabilities of those devices.</span></span>  

## <span data-ttu-id="dd192-136">Monitorar o uso da memória em tempo real com o Gerenciador de tarefas do navegador Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="dd192-136">Monitor memory use in realtime with the Microsoft Edge Browser Task Manager</span></span>  

<span data-ttu-id="dd192-137">Use o Gerenciador de tarefas do navegador Microsoft Edge como ponto de partida para a investigação do problema de memória.</span><span class="sxs-lookup"><span data-stu-id="dd192-137">Use the Microsoft Edge Browser Task Manager as a starting point to your memory issue investigation.</span></span>  <span data-ttu-id="dd192-138">O Gerenciador de tarefas do navegador Microsoft Edge é um monitor em tempo real que informa a quantidade de memória que uma página está usando no momento.</span><span class="sxs-lookup"><span data-stu-id="dd192-138">The Microsoft Edge Browser Task Manager is a realtime monitor that tells you how much memory a page is currently using.</span></span>  

1.  <span data-ttu-id="dd192-139">Pressione `Shift` + `Esc` ou vá para o menu principal do Microsoft Edge e selecione **mais ferramentas**  >  **Gerenciador de tarefas do navegador** para abrir o Gerenciador de tarefas do navegador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dd192-139">Press `Shift`+`Esc` or go to the Microsoft Edge main menu and select **More tools** > **Browser Task Manager** to open the Microsoft Edge Browser Task Manager.</span></span>  
    
    > ##### <span data-ttu-id="dd192-140">Figura 1</span><span class="sxs-lookup"><span data-stu-id="dd192-140">Figure 1</span></span>  
    > <span data-ttu-id="dd192-141">Abrir o Gerenciador de tarefas do navegador Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="dd192-141">Opening the Microsoft Edge Browser Task Manager</span></span>  
    > ![Abrir o Gerenciador de tarefas do navegador Microsoft Edge][ImageTaskManager]  
    
1.  <span data-ttu-id="dd192-143">Clique com o botão direito do mouse no cabeçalho da tabela do Gerenciador de tarefas do navegador Microsoft Edge e habilite a **memória JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="dd192-143">Right-click on the table header of the Microsoft Edge Browser Task Manager and enable **JavaScript memory**.</span></span>  
    
    > ##### <span data-ttu-id="dd192-144">Figura 2</span><span class="sxs-lookup"><span data-stu-id="dd192-144">Figure 2</span></span>  
    > <span data-ttu-id="dd192-145">Habilitar a memória JavaScript</span><span class="sxs-lookup"><span data-stu-id="dd192-145">Enable JavaScript memory</span></span>  
    > ![Habilitar a memória JavaScript][ImageJavascriptMemory]  
    
<span data-ttu-id="dd192-147">Essas duas colunas mostram itens diferentes sobre como a sua página está usando a memória:</span><span class="sxs-lookup"><span data-stu-id="dd192-147">These two columns tell you different things about how your page is using memory:</span></span>  

*   <span data-ttu-id="dd192-148">A coluna **memória** representa a memória nativa.</span><span class="sxs-lookup"><span data-stu-id="dd192-148">The **Memory** column represents native memory.</span></span>  <span data-ttu-id="dd192-149">Os nós DOM são armazenados na memória nativa.</span><span class="sxs-lookup"><span data-stu-id="dd192-149">DOM nodes are stored in native memory.</span></span>  <span data-ttu-id="dd192-150">Se esse valor estiver aumentando, os nós DOM serão criados.</span><span class="sxs-lookup"><span data-stu-id="dd192-150">If this value is increasing, DOM nodes are getting created.</span></span>  
*   <span data-ttu-id="dd192-151">A coluna **memória JavaScript** representa o heap do js.</span><span class="sxs-lookup"><span data-stu-id="dd192-151">The **JavaScript Memory** column represents the JS heap.</span></span>  <span data-ttu-id="dd192-152">Esta coluna contém dois valores.</span><span class="sxs-lookup"><span data-stu-id="dd192-152">This column contains two values.</span></span>  <span data-ttu-id="dd192-153">O valor no qual você está interessado é o número Live \ (o número entre parênteses \).</span><span class="sxs-lookup"><span data-stu-id="dd192-153">The value you are interested in is the live number \(the number in parentheses\).</span></span>  <span data-ttu-id="dd192-154">O número Live representa a quantidade de memória que os objetos acessíveis na sua página estão usando.</span><span class="sxs-lookup"><span data-stu-id="dd192-154">The live number represents how much memory the reachable objects on your page are using.</span></span>  <span data-ttu-id="dd192-155">Se esse número estiver aumentando, os novos objetos serão criados ou os objetos existentes estão crescendo.</span><span class="sxs-lookup"><span data-stu-id="dd192-155">If this number is increasing, either new objects are being created, or the existing objects are growing.</span></span>  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <span data-ttu-id="dd192-156">Visualize vazamentos de memória com o painel desempenho</span><span class="sxs-lookup"><span data-stu-id="dd192-156">Visualize memory leaks with Performance panel</span></span>  

<span data-ttu-id="dd192-157">Você também pode usar o painel desempenho como outro ponto de partida na investigação.</span><span class="sxs-lookup"><span data-stu-id="dd192-157">You may also use the Performance panel as another starting point in your investigation.</span></span>  <span data-ttu-id="dd192-158">O painel desempenho ajuda você a visualizar o uso da memória de uma página ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="dd192-158">The Performance panel helps you visualize the memory use of a page over time.</span></span>  

1.  <span data-ttu-id="dd192-159">Abra o painel **desempenho** no devtools.</span><span class="sxs-lookup"><span data-stu-id="dd192-159">Open the **Performance** panel on DevTools.</span></span>  
1.  <span data-ttu-id="dd192-160">Habilitar a caixa de seleção **memória** .</span><span class="sxs-lookup"><span data-stu-id="dd192-160">Enable the **Memory** checkbox.</span></span>  
1.  <span data-ttu-id="dd192-161">[Fazer uma gravação][DevtoolsEvaluatePerformanceReferenceRecord].</span><span class="sxs-lookup"><span data-stu-id="dd192-161">[Make a recording][DevtoolsEvaluatePerformanceReferenceRecord].</span></span>  

> [!TIP]
> <span data-ttu-id="dd192-162">É uma boa prática começar e encerrar sua gravação com uma coleta de lixo forçada.</span><span class="sxs-lookup"><span data-stu-id="dd192-162">It is a good practice to start and end your recording with a forced garbage collection.</span></span>  <span data-ttu-id="dd192-163">Clique no botão coletar coleta de lixo da força de **lixo** ![ ][ImageForceGarbageCollectionIcon] durante a gravação para forçar a coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="dd192-163">Click the **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button while recording to force garbage collection.</span></span>  

<span data-ttu-id="dd192-164">Para demonstrar gravações de memória, considere o código abaixo:</span><span class="sxs-lookup"><span data-stu-id="dd192-164">To demonstrate memory recordings, consider the code below:</span></span>  

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

<span data-ttu-id="dd192-165">Toda vez que o botão referenciado no código for pressionado, os `div` nós do 10000 serão acrescentados ao corpo do documento, e uma cadeia de caracteres de 1 milhão `x` será colocada na `x` matriz.</span><span class="sxs-lookup"><span data-stu-id="dd192-165">Every time that the button referenced in the code is pressed, ten thousand `div` nodes are appended to the document body, and a string of one million `x` characters is pushed onto the `x` array.</span></span>  <span data-ttu-id="dd192-166">Executar esse código produz uma gravação no painel **desempenho** , como a [Figura 3](#figure-3).</span><span class="sxs-lookup"><span data-stu-id="dd192-166">Running this code produces a recording in the **Performance** panel like [Figure 3](#figure-3).</span></span>  

> ##### <span data-ttu-id="dd192-167">Figura 3</span><span class="sxs-lookup"><span data-stu-id="dd192-167">Figure 3</span></span>  
> <span data-ttu-id="dd192-168">Crescimento simples</span><span class="sxs-lookup"><span data-stu-id="dd192-168">Simple growth</span></span>  
> ![Crescimento simples][ImageSimpleGrowth]  

<span data-ttu-id="dd192-170">Primeiro, uma explicação sobre a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="dd192-170">First, an explanation of the user interface.</span></span>  <span data-ttu-id="dd192-171">O gráfico de **heap** no painel de **visão geral** \ (abaixo de **net**\) representa o heap do js.</span><span class="sxs-lookup"><span data-stu-id="dd192-171">The **HEAP** graph in the **Overview** pane \(below **NET**\) represents the JS heap.</span></span>  <span data-ttu-id="dd192-172">Abaixo do painel **visão geral** está o painel **contador** .</span><span class="sxs-lookup"><span data-stu-id="dd192-172">Below the **Overview** pane is the **Counter** pane.</span></span>  <span data-ttu-id="dd192-173">Aqui você pode ver o uso da memória dividido por JS do JS \ (mesmo que o gráfico de **heap** no painel de **visão geral** \), documentos, nós dom, ouvintes e memória GPU.</span><span class="sxs-lookup"><span data-stu-id="dd192-173">Here you are able to see memory usage broken down by JS heap \(same as **HEAP** graph in the **Overview** pane\), documents, DOM nodes, listeners, and GPU memory.</span></span>  <span data-ttu-id="dd192-174">Desabilitar uma caixa de seleção oculta-a do gráfico.</span><span class="sxs-lookup"><span data-stu-id="dd192-174">Disabling a checkbox hides it from the graph.</span></span>  

<span data-ttu-id="dd192-175">Agora, uma análise do código em comparação com a [Figura 3](#figure-3).</span><span class="sxs-lookup"><span data-stu-id="dd192-175">Now, an analysis of the code compared with [Figure 3](#figure-3).</span></span>  <span data-ttu-id="dd192-176">Se você observar o contador de nós \ (o gráfico verde \), poderá ver que ele corresponderá perfeitamente com o código.</span><span class="sxs-lookup"><span data-stu-id="dd192-176">If you look at the node counter \(the green graph\) you are able to see that it matches up cleanly with the code.</span></span>  <span data-ttu-id="dd192-177">A contagem de nós aumenta em etapas discretas.</span><span class="sxs-lookup"><span data-stu-id="dd192-177">The node count increases in discrete steps.</span></span>  <span data-ttu-id="dd192-178">Você pode presumir que cada aumento na contagem de nós é uma chamada para `grow()` .</span><span class="sxs-lookup"><span data-stu-id="dd192-178">You may presume that each increase in the node count is a call to `grow()`.</span></span>  <span data-ttu-id="dd192-179">O gráfico de heap do JS \ (o gráfico azul \) não é tão simples.</span><span class="sxs-lookup"><span data-stu-id="dd192-179">The JS heap graph \(the blue graph\) is not as straightforward.</span></span>  <span data-ttu-id="dd192-180">Em manter as práticas recomendadas, o primeiro DIP é, na verdade, uma coleta de lixo forçada \ (obtida pressionando-se o botão coletar coleta de lixo da **coleta** de lixo ![ ][ImageForceGarbageCollectionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="dd192-180">In keeping with best practices, the first dip is actually a forced garbage collection \(achieved by pressing the  **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button\).</span></span>  <span data-ttu-id="dd192-181">À medida que a gravação progride, você pode ver que o tamanho de heap do JS é pico.</span><span class="sxs-lookup"><span data-stu-id="dd192-181">As the recording progresses you are able to see that the JS heap size spikes.</span></span>  <span data-ttu-id="dd192-182">Isso é natural e esperado: o código JavaScript está criando os nós DOM em cada botão clique e fazendo muito trabalho quando cria a cadeia de caracteres de 1 milhão caracteres.</span><span class="sxs-lookup"><span data-stu-id="dd192-182">This is natural and expected:  the JavaScript code is creating the DOM nodes on every button click and doing a lot of work when it creates the string of one million characters.</span></span>  <span data-ttu-id="dd192-183">A chave importante aqui é o fato de que o recurso heap do JS termina mais alto do que começou \ (o "começo" aqui está a ponto após a coleta de lixo forçada \).</span><span class="sxs-lookup"><span data-stu-id="dd192-183">The key thing here is the fact that the JS heap ends higher than it began \(the "beginning" here being the point after the forced garbage collection\).</span></span>  <span data-ttu-id="dd192-184">No mundo real, se você viu esse padrão de tamanho de pilha ou tamanho de nó aumentado, pode ser possível definir um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="dd192-184">In the real world, if you saw this pattern of increasing JS heap size or node size, it may potentially define a memory leak.</span></span>  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <span data-ttu-id="dd192-185">Descobrir vazamentos de memória de árvore DOM desanexada com instantâneos de heap</span><span class="sxs-lookup"><span data-stu-id="dd192-185">Discover detached DOM tree memory leaks with Heap Snapshots</span></span>  

<span data-ttu-id="dd192-186">Um nó DOM é apenas lixo coletado quando não há referências para o nó da árvore DOM ou do código JavaScript em execução na página.</span><span class="sxs-lookup"><span data-stu-id="dd192-186">A DOM node is only garbage collected when there are no references to the node from either the DOM tree or JavaScript code running on the page.</span></span>  <span data-ttu-id="dd192-187">Um nó é considerado como "desconectado" quando é removido da árvore DOM, mas alguns JavaScript ainda fazem referência a ele.</span><span class="sxs-lookup"><span data-stu-id="dd192-187">A node is said to be "detached" when it is removed from the DOM tree but some JavaScript still references it.</span></span>  <span data-ttu-id="dd192-188">Os nós DOM desanexados são uma causa comum de vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="dd192-188">Detached DOM nodes are a common cause of memory leaks.</span></span>  <span data-ttu-id="dd192-189">Esta seção ensina a usar os profilers de heap no DevTools para identificar nós desanexados.</span><span class="sxs-lookup"><span data-stu-id="dd192-189">This section teaches you how to use the heap profilers in DevTools to identify detached nodes.</span></span>  

<span data-ttu-id="dd192-190">Aqui está um exemplo simples de nós DOM desanexados.</span><span class="sxs-lookup"><span data-stu-id="dd192-190">Here is a simple example of detached DOM nodes.</span></span>  

```javascript
var detachedNodes;
function create() {
    var ul = document.createElement('ul');
    for (var i = 0; i < 10; i++) {
        var li = document.createElement('li');
        ul.appendChild(li);
    }
    detachedNodes = ul;
}
document.getElementById('create').addEventListener('click', create);
```  

<span data-ttu-id="dd192-191">Clicar no botão referenciado no código cria um `ul` nó com dez `li` filhos.</span><span class="sxs-lookup"><span data-stu-id="dd192-191">Clicking the button referenced in the code creates a `ul` node with ten `li` children.</span></span>  <span data-ttu-id="dd192-192">Esses nós são referenciados pelo código, mas não existem na árvore DOM, portanto, cada um é desconectado.</span><span class="sxs-lookup"><span data-stu-id="dd192-192">These nodes are referenced by the code but do not exist in the DOM tree, so each is detached.</span></span>  

<span data-ttu-id="dd192-193">Os instantâneos de pilha são uma maneira de identificar nós desanexados.</span><span class="sxs-lookup"><span data-stu-id="dd192-193">Heap snapshots are one way to identify detached nodes.</span></span>  <span data-ttu-id="dd192-194">Como o nome indica, os instantâneos de heap mostram como a memória é distribuída entre os objetos JS e os nós DOM da página no momento do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="dd192-194">As the name implies, heap snapshots show you how memory is distributed among the JS objects and DOM nodes for your page at the point of time of the snapshot.</span></span>  

<span data-ttu-id="dd192-195">Para criar um instantâneo, abra o DevTools e vá para o painel **memória** , selecione o botão de opção **instantâneo de heap** e, em seguida, pressione o botão **criar instantâneo** .</span><span class="sxs-lookup"><span data-stu-id="dd192-195">To create a snapshot, open DevTools and go to the **Memory** panel, select the **Heap snapshot** radio button, and then press the **Take snapshot** button.</span></span>  

> ##### <span data-ttu-id="dd192-196">Figura 4</span><span class="sxs-lookup"><span data-stu-id="dd192-196">Figure 4</span></span>  
> <span data-ttu-id="dd192-197">Criar instantâneo de heap</span><span class="sxs-lookup"><span data-stu-id="dd192-197">Take heap snapshot</span></span>  
> ![Criar instantâneo de heap][ImageTakeHeapSnapshot]  

<span data-ttu-id="dd192-199">O instantâneo pode levar algum tempo para processar e carregar.</span><span class="sxs-lookup"><span data-stu-id="dd192-199">The snapshot may take some time to process and load.</span></span>  <span data-ttu-id="dd192-200">Após concluir, selecione-o no painel esquerdo \ (chamado de **instantâneos de heap**\).</span><span class="sxs-lookup"><span data-stu-id="dd192-200">After it is finished, select it from the left-hand panel \(named **HEAP SNAPSHOTS**\).</span></span>  

<span data-ttu-id="dd192-201">Digite `Detached` a caixa de texto **filtro de classe** para pesquisar árvores dom desanexadas.</span><span class="sxs-lookup"><span data-stu-id="dd192-201">Type `Detached` in the **Class filter** textbox to search for detached DOM trees.</span></span>  

> ##### <span data-ttu-id="dd192-202">Figura 5</span><span class="sxs-lookup"><span data-stu-id="dd192-202">Figure 5</span></span>  
> <span data-ttu-id="dd192-203">Filtragem de nós desconectados</span><span class="sxs-lookup"><span data-stu-id="dd192-203">Filtering for detached nodes</span></span>  
> ![Filtragem de nós desconectados][ImageFilteringForDetachedNodes]  

<span data-ttu-id="dd192-205">Expanda o carats para investigar uma árvore desanexada.</span><span class="sxs-lookup"><span data-stu-id="dd192-205">Expand the carats to investigate a detached tree.</span></span>  

> ##### <span data-ttu-id="dd192-206">Figura 6</span><span class="sxs-lookup"><span data-stu-id="dd192-206">Figure 6</span></span>  
> <span data-ttu-id="dd192-207">Investigando a árvore desanexada</span><span class="sxs-lookup"><span data-stu-id="dd192-207">Investigating detached tree</span></span>  
> ![Investigando a árvore desanexada][ImageInvestigatingDetachedTree]  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

<span data-ttu-id="dd192-209">Clique em um nó para investigar ainda mais.</span><span class="sxs-lookup"><span data-stu-id="dd192-209">Click on a node to investigate it further.</span></span>  <span data-ttu-id="dd192-210">No painel **objetos** , você pode ver mais informações sobre o código que o está fazendo referência a ele.</span><span class="sxs-lookup"><span data-stu-id="dd192-210">In the **Objects** pane you are able to see more information about the code that is referencing it.</span></span>  <span data-ttu-id="dd192-211">Por exemplo, na [Figura 7](#figure-7) , você pode ver que a `detachedNodes` variável faz referência ao nó.</span><span class="sxs-lookup"><span data-stu-id="dd192-211">For example, in [Figure 7](#figure-7) you are able to see that the `detachedNodes` variable is referencing the node.</span></span>  <span data-ttu-id="dd192-212">Para corrigir esse vazamento de memória específico, você deve estudar o código que usa a `detachedUNode` variável e garantir que a referência ao nó seja removida quando não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="dd192-212">To fix this particular memory leak, you should study the code that uses the `detachedUNode` variable and ensure that the reference to the node is removed when it is no longer needed.</span></span>

> ##### <span data-ttu-id="dd192-213">Figura 7</span><span class="sxs-lookup"><span data-stu-id="dd192-213">Figure 7</span></span>  
> <span data-ttu-id="dd192-214">Investigando um nó</span><span class="sxs-lookup"><span data-stu-id="dd192-214">Investigating a node</span></span>  
> ![Investigando um nó][ImageInvestigatingNode]  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <span data-ttu-id="dd192-216">Identificar vazamentos de memória de heap do JS com a instrumentação de alocação na linha do tempo</span><span class="sxs-lookup"><span data-stu-id="dd192-216">Identify JS heap memory leaks with Allocation instrumentation on timeline</span></span>  

<span data-ttu-id="dd192-217">A **Instrumentação de alocação na linha do tempo** é outra ferramenta que pode ajudá-lo a rastrear vazamentos de memória no heap do js.</span><span class="sxs-lookup"><span data-stu-id="dd192-217">**Allocation instrumentation on timeline** is another tool that may help you track down memory leaks in your JS heap.</span></span>  

<span data-ttu-id="dd192-218">Demonstre a **Instrumentação de distribuição na linha do tempo** usando o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="dd192-218">Demonstrate **Allocation instrumentation on timeline**  using the following code.</span></span>  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="dd192-219">Toda vez que o botão referenciado no código é enviado, uma cadeia de caracteres de 1 milhão caracteres é adicionada à `x` matriz.</span><span class="sxs-lookup"><span data-stu-id="dd192-219">Every time that the button referenced in the code is pushed, a string of one million characters is added to the `x` array.</span></span>  

<span data-ttu-id="dd192-220">Para gravar uma instrumentação de alocação na linha do tempo, abra o DevTools, vá para o painel **memória** , selecione o botão de opção **Instrumentação de alocação no cronograma** , pressione o botão **Iniciar** , execute a ação que você acha que está causando o vazamento de memória e, em seguida, pressione o botão **parar gravação do perfil de heap** ![ parar gravação ][ImageStopRecordingIcon] quando terminar.</span><span class="sxs-lookup"><span data-stu-id="dd192-220">To record an Allocation instrumentation on timeline, open DevTools, go to the **Memory** panel, select the **Allocation instrumentation on timeline** radio button, press the **Start** button, perform the action that you suspect is causing the memory leak, and then press the **Stop recording heap profile** ![stop recording][ImageStopRecordingIcon] button when you are done.</span></span>  

<span data-ttu-id="dd192-221">Durante a gravação, observe se as barras azuis aparecem na instrumentação de alocação na linha do tempo, como na [Figura 8](#figure-8).</span><span class="sxs-lookup"><span data-stu-id="dd192-221">As you are recording, notice if any blue bars show up on the Allocation instrumentation on timeline, like in [Figure 8](#figure-8).</span></span>  

> ##### <span data-ttu-id="dd192-222">Figura 8</span><span class="sxs-lookup"><span data-stu-id="dd192-222">Figure 8</span></span>  
> <span data-ttu-id="dd192-223">Novas alocações</span><span class="sxs-lookup"><span data-stu-id="dd192-223">New allocations</span></span>  
> ![Novas alocações][ImageNewAllocations]  

<span data-ttu-id="dd192-225">Essas barras azuis representam novas alocações de memória.</span><span class="sxs-lookup"><span data-stu-id="dd192-225">Those blue bars represent new memory allocations.</span></span>  <span data-ttu-id="dd192-226">Essas novas atribuições de memória são seus candidatos para vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="dd192-226">Those new memory allocations are your candidates for memory leaks.</span></span>  <span data-ttu-id="dd192-227">Você pode aplicar zoom em uma barra para filtrar o painel do **Construtor** para mostrar somente os objetos que foram atribuídos durante o período especificado.</span><span class="sxs-lookup"><span data-stu-id="dd192-227">You are able to zoom on a bar to filter the **Constructor** pane to only show objects that were allocated during the specified timeframe.</span></span>  

> ##### <span data-ttu-id="dd192-228">Figura 9</span><span class="sxs-lookup"><span data-stu-id="dd192-228">Figure 9</span></span>  
> <span data-ttu-id="dd192-229">Linha do tempo de alocação ampliada</span><span class="sxs-lookup"><span data-stu-id="dd192-229">Zoomed allocation timeline</span></span>  
> ![Linha do tempo de alocação ampliada][ImageZoomedAllocationTimeline]  

<span data-ttu-id="dd192-231">Expanda o objeto e clique no valor para ver mais detalhes no painel **objeto** .</span><span class="sxs-lookup"><span data-stu-id="dd192-231">Expand the object and click on the value to view more details in the **Object** pane.</span></span>  <span data-ttu-id="dd192-232">Por exemplo, na [Figura 10](#figure-10), exibindo os detalhes do objeto que foi recém atribuído, você deve ser capaz de ver que ele foi atribuído à `x` variável no `Window` escopo.</span><span class="sxs-lookup"><span data-stu-id="dd192-232">For example, in [Figure 10](#figure-10), by viewing the details of the object that was newly allocated, you should be able to see that it was allocated to the `x` variable in the `Window` scope.</span></span>  

> ##### <span data-ttu-id="dd192-233">Figura 10</span><span class="sxs-lookup"><span data-stu-id="dd192-233">Figure 10</span></span> 
> <span data-ttu-id="dd192-234">Detalhes do objeto</span><span class="sxs-lookup"><span data-stu-id="dd192-234">Object details</span></span>  
> ![Detalhes do objeto][ImageObjectDetail]  

## <span data-ttu-id="dd192-236">Investigar a alocação de memória por função</span><span class="sxs-lookup"><span data-stu-id="dd192-236">Investigate memory allocation by function</span></span>   

<span data-ttu-id="dd192-237">Use o tipo de perfil de **amostragem de alocação** para exibir a alocação de memória por função de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dd192-237">Use the **Allocation sampling** profiling type to view memory allocation by JavaScript function.</span></span>  

> ##### <span data-ttu-id="dd192-238">Figura 11</span><span class="sxs-lookup"><span data-stu-id="dd192-238">Figure 11</span></span>  
> <span data-ttu-id="dd192-239">Amostragem de alocação de registros</span><span class="sxs-lookup"><span data-stu-id="dd192-239">Record Allocation sampling</span></span>  
> ![Amostragem de alocação de registros][ImageRecordAllocationSampling]  

1.  <span data-ttu-id="dd192-241">Selecione o botão de opção de **amostragem de alocação** .</span><span class="sxs-lookup"><span data-stu-id="dd192-241">Select the **Allocation sampling** radio button.</span></span>  <span data-ttu-id="dd192-242">Se houver um trabalhador na página, você poderá selecioná-lo como o destino do profiling usando o menu suspenso ao lado do botão **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="dd192-242">If there is a worker on the page, you are able to select that as the profiling target using the dropdown menu next to the **Start** button.</span></span>  
1.  <span data-ttu-id="dd192-243">Pressione o botão **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="dd192-243">Press the **Start** button.</span></span>  
1.  <span data-ttu-id="dd192-244">Execute as ações na página que você deseja investigar.</span><span class="sxs-lookup"><span data-stu-id="dd192-244">Perform the actions on the page which you want to investigate.</span></span>  
1.  <span data-ttu-id="dd192-245">Pressione o botão **parar** quando terminar todas as ações.</span><span class="sxs-lookup"><span data-stu-id="dd192-245">Press the **Stop** button when you have finished all of your actions.</span></span>  

<span data-ttu-id="dd192-246">DevTools mostra uma divisão da alocação de memória por função.</span><span class="sxs-lookup"><span data-stu-id="dd192-246">DevTools shows you a breakdown of memory allocation by function.</span></span>  <span data-ttu-id="dd192-247">O modo de exibição padrão é **pesado (abaixo)**, que exibe as funções que alocavam mais memória na parte superior.</span><span class="sxs-lookup"><span data-stu-id="dd192-247">The default view is **Heavy (Bottom Up)**, which displays the functions that allocated the most memory at the top.</span></span>  

> ##### <span data-ttu-id="dd192-248">Figura 12</span><span class="sxs-lookup"><span data-stu-id="dd192-248">Figure 12</span></span>  
> <span data-ttu-id="dd192-249">Amostragem de alocação</span><span class="sxs-lookup"><span data-stu-id="dd192-249">Allocation sampling</span></span>  
>![Amostragem de alocação][ImageAllocationSampling]  

## <span data-ttu-id="dd192-251">Coletas frequentes de lixo</span><span class="sxs-lookup"><span data-stu-id="dd192-251">Spot frequent garbage collections</span></span>  

<span data-ttu-id="dd192-252">Se a página parecer pausar com frequência, você poderá ter problemas com a coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="dd192-252">If your page appears to pause frequently, then you may have garbage collection issues.</span></span>  

<span data-ttu-id="dd192-253">Você pode usar o Gerenciador de tarefas do navegador Microsoft Edge ou as gravações de memória de desempenho para identificar a coleta de lixo frequente.</span><span class="sxs-lookup"><span data-stu-id="dd192-253">You are able to use either the Microsoft Edge Browser Task Manager or Performance memory recordings to spot frequent garbage collection.</span></span>  <span data-ttu-id="dd192-254">No Gerenciador de tarefas do navegador Microsoft Edge, a **memória** em elevação e queda frequente ou valores de **memória JavaScript** representam coleta de lixo frequente.</span><span class="sxs-lookup"><span data-stu-id="dd192-254">In the Microsoft Edge Browser Task Manager, frequently rising and falling **Memory** or **JavaScript Memory** values represent frequent garbage collection.</span></span>  <span data-ttu-id="dd192-255">Em gravações de desempenho, alterações frequentes (em elevação e queda) para os gráficos de contagem de nós ou heap do JS indicam coleta de lixo frequente.</span><span class="sxs-lookup"><span data-stu-id="dd192-255">In Performance recordings, frequent changes (rising and falling) to the JS heap or node count graphs indicate frequent garbage collection.</span></span>  

<span data-ttu-id="dd192-256">Depois de identificar o problema, você poderá usar uma **Instrumentação de alocação na gravação da linha do tempo** para descobrir onde a memória está sendo alocada e quais funções estão causando as atribuições.</span><span class="sxs-lookup"><span data-stu-id="dd192-256">After you have identified the problem, you are able to use an **Allocation instrumentation on timeline** recording to find out where memory is being allocated and which functions are causing the allocations.</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageForceGarbageCollectionIcon]: /microsoft-edge/devtools-guide-chromium/media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: /microsoft-edge/devtools-guide-chromium/media/stop-recording-icon.msft.png  

[ImageTaskManager]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png "Figura 1: abrindo o Gerenciador de tarefas do navegador Microsoft Edge"  
[ImageJavascriptMemory]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png "Figura 2: habilitar a memória JavaScript"  
[ImageSimpleGrowth]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-1-performance-memory.msft.png "Figura 3: crescimento simples"  
[ImageTakeHeapSnapshot]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png "Figura 4: criar um instantâneo de heap"  
[ImageFilteringForDetachedNodes]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png "Figura 5: filtragem para nós desanexados"  
[ImageInvestigatingDetachedTree]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png "Figura 6: investigando a árvore desanexada"  
[ImageInvestigatingNode]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png "Figura 7: investigando um nó"  
[ImageNewAllocations]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png "Figura 8: novas atribuições"  
[ImageZoomedAllocationTimeline]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png "Figura 9: linha do tempo de alocação ampliada"  
[ImageObjectDetail]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png "Figura 10: detalhes do objeto"  
[ImageRecordAllocationSampling]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png "Figura 11: amostra de alocação de registros"  
[ImageAllocationSampling]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png "Figura 12: amostra de alocação"  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Desempenho do registro-referência da análise de desempenho"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> <span data-ttu-id="dd192-270">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="dd192-270">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dd192-271">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="dd192-271">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="dd192-273">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dd192-273">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
