---
title: Corrigir problemas de memória
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: b9e6e2af333257f0cbe0a4a354dcd1d7b862af9c
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751986"
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

# <span data-ttu-id="70c3b-103">Corrigir problemas de memória</span><span class="sxs-lookup"><span data-stu-id="70c3b-103">Fix Memory Problems</span></span>  

<span data-ttu-id="70c3b-104">Saiba como usar o Microsoft Edge e o DevTools para encontrar problemas de memória que afetam o desempenho da página, incluindo vazamentos de memória, excesso de memória e coletas de lixo frequentes.</span><span class="sxs-lookup"><span data-stu-id="70c3b-104">Learn how to use Microsoft Edge and DevTools to find memory issues that affect page performance, including memory leaks, memory bloat, and frequent garbage collections.</span></span>  

### <span data-ttu-id="70c3b-105">Resumo</span><span class="sxs-lookup"><span data-stu-id="70c3b-105">Summary</span></span>  

*   <span data-ttu-id="70c3b-106">Verifique a quantidade de memória que sua página usa no momento com o Gerenciador de tarefas do navegador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="70c3b-106">Find out how much memory your page is currently using with the Microsoft Edge Browser Task Manager.</span></span>  
*   <span data-ttu-id="70c3b-107">Visualize o uso da memória ao longo do tempo com o painel **memória** .</span><span class="sxs-lookup"><span data-stu-id="70c3b-107">Visualize memory usage over time with the **Memory** panel.</span></span>  
*   <span data-ttu-id="70c3b-108">Identificar árvores de DOM desanexadas \ (uma causa comum de vazamentos de memória \) com o **instantâneo de heap**.</span><span class="sxs-lookup"><span data-stu-id="70c3b-108">Identify detached DOM trees \(a common cause of memory leaks\) with **Heap snapshot**.</span></span>  
*   <span data-ttu-id="70c3b-109">Descubra quando está sendo atribuída uma nova memória no seu heap JavaScript \ (JS! heap \) com a **Instrumentação de distribuição na linha do tempo**.</span><span class="sxs-lookup"><span data-stu-id="70c3b-109">Find out when new memory is being allocated in your JavaScript heap \(JS heap\) with **Allocation instrumentation on timeline**.</span></span>  

## <span data-ttu-id="70c3b-110">Visão geral</span><span class="sxs-lookup"><span data-stu-id="70c3b-110">Overview</span></span>  

<span data-ttu-id="70c3b-111">No espírito do modelo de desempenho do **trilho** , o foco de seus esforços de desempenho deve ser seus usuários.</span><span class="sxs-lookup"><span data-stu-id="70c3b-111">In the spirit of the **RAIL** performance model, the focus of your performance efforts should be your users.</span></span>  

<!--todo: add RAIL section when available  -->  

<span data-ttu-id="70c3b-112">Os problemas de memória são importantes porque costumam ser percebêveis pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="70c3b-112">Memory issues are important because they are often perceivable by users.</span></span>  <span data-ttu-id="70c3b-113">Os usuários podem perceber problemas de memória das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="70c3b-113">Users may perceive memory issues in the following ways:</span></span>  

*   <span data-ttu-id="70c3b-114">**O desempenho de uma página é piormente pior ao longo do tempo**.</span><span class="sxs-lookup"><span data-stu-id="70c3b-114">**The performance of a page gets progressively worse over time**.</span></span>  <span data-ttu-id="70c3b-115">Isso possivelmente é um sintoma de perda de memória.</span><span class="sxs-lookup"><span data-stu-id="70c3b-115">This is possibly a symptom of a memory leak.</span></span>  <span data-ttu-id="70c3b-116">Um vazamento de memória é quando um bug na página faz com que a página use cada vez mais e mais memória ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="70c3b-116">A memory leak is when a bug in the page causes the page to progressively use more and more memory over time.</span></span>  
*   <span data-ttu-id="70c3b-117">**O desempenho de uma página é consistentemente ruim**.</span><span class="sxs-lookup"><span data-stu-id="70c3b-117">**The performance of a page is consistently bad**.</span></span>  <span data-ttu-id="70c3b-118">Isso possivelmente é um sintoma de excesso de memória.</span><span class="sxs-lookup"><span data-stu-id="70c3b-118">This is possibly a symptom of memory bloat.</span></span>  <span data-ttu-id="70c3b-119">O excesso de memória é quando uma página usa mais memória do que o necessário para a velocidade de página ideal.</span><span class="sxs-lookup"><span data-stu-id="70c3b-119">Memory bloat is when a page uses more memory than is necessary for optimal page speed.</span></span>  
*   <span data-ttu-id="70c3b-120">**O desempenho de uma página é atrasado ou parece pausar com frequência**.</span><span class="sxs-lookup"><span data-stu-id="70c3b-120">**The performance of a page is delayed or appears to pause frequently**.</span></span>  <span data-ttu-id="70c3b-121">Isso possivelmente é um sintoma de coletas de lixo frequentes.</span><span class="sxs-lookup"><span data-stu-id="70c3b-121">This is possibly a symptom of frequent garbage collections.</span></span>  <span data-ttu-id="70c3b-122">Coleta de lixo é quando o navegador recupera memória.</span><span class="sxs-lookup"><span data-stu-id="70c3b-122">Garbage collection is when the browser reclaims memory.</span></span>  <span data-ttu-id="70c3b-123">O navegador decide quando isso acontece.</span><span class="sxs-lookup"><span data-stu-id="70c3b-123">The browser decides when this happens.</span></span>  <span data-ttu-id="70c3b-124">Durante as coletas, todos os scripts em execução são pausados.</span><span class="sxs-lookup"><span data-stu-id="70c3b-124">During collections, all script running is paused.</span></span>  <span data-ttu-id="70c3b-125">Portanto, se o navegador estiver coletando um lote, o tempo de execução de script será pausado muito.</span><span class="sxs-lookup"><span data-stu-id="70c3b-125">So if the browser is garbage collecting a lot, script runtime is going to get paused a lot.</span></span>  

### <span data-ttu-id="70c3b-126">Inflação da memória: quanto custa "muito grande"?</span><span class="sxs-lookup"><span data-stu-id="70c3b-126">Memory bloat: how much is "too much"?</span></span>  

<span data-ttu-id="70c3b-127">É fácil definir um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="70c3b-127">A memory leak is easy to define.</span></span>  <span data-ttu-id="70c3b-128">Se um site estiver usando um número cada vez maior de memória, você terá um vazamento.</span><span class="sxs-lookup"><span data-stu-id="70c3b-128">If a site is progressively using more and more memory, then you have a leak.</span></span>  <span data-ttu-id="70c3b-129">Mas o excesso de memória é um pouco mais difícil de fixar.</span><span class="sxs-lookup"><span data-stu-id="70c3b-129">But memory bloat is a bit harder to pin down.</span></span>  <span data-ttu-id="70c3b-130">O que é qualificado como "usando muita memória"?</span><span class="sxs-lookup"><span data-stu-id="70c3b-130">What qualifies as "using too much memory"?</span></span>  

<span data-ttu-id="70c3b-131">Não há números rígidos aqui, porque diferentes dispositivos e navegadores têm recursos diferentes.</span><span class="sxs-lookup"><span data-stu-id="70c3b-131">There are no hard numbers here, because different devices and browsers have different capabilities.</span></span>  <span data-ttu-id="70c3b-132">A mesma página que é executada tranqüilamente em um smartphone high-end pode falhar em um smartphone low-end.</span><span class="sxs-lookup"><span data-stu-id="70c3b-132">The same page that runs smoothly on a high-end smartphone may crash on a low-end smartphone.</span></span>  

<span data-ttu-id="70c3b-133">A chave aqui é usar o modelo de trilho e enfocar seus usuários.</span><span class="sxs-lookup"><span data-stu-id="70c3b-133">The key here is to use the RAIL model and focus on your users.</span></span>  <span data-ttu-id="70c3b-134">Descubra quais dispositivos são populares com seus usuários e teste sua página nesses dispositivos.</span><span class="sxs-lookup"><span data-stu-id="70c3b-134">Find out what devices are popular with your users, and then test out your page on those devices.</span></span>  <span data-ttu-id="70c3b-135">Se a experiência for ruim consistentemente, a página pode estar excedendo os recursos de memória desses dispositivos.</span><span class="sxs-lookup"><span data-stu-id="70c3b-135">If the experience is consistently bad, the page may be exceeding the memory capabilities of those devices.</span></span>  

## <span data-ttu-id="70c3b-136">Monitorar o uso da memória em tempo real com o Gerenciador de tarefas do navegador Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="70c3b-136">Monitor memory use in realtime with the Microsoft Edge Browser Task Manager</span></span>  

<span data-ttu-id="70c3b-137">Use o Gerenciador de tarefas do navegador Microsoft Edge como ponto de partida para a investigação do problema de memória.</span><span class="sxs-lookup"><span data-stu-id="70c3b-137">Use the Microsoft Edge Browser Task Manager as a starting point to your memory issue investigation.</span></span>  <span data-ttu-id="70c3b-138">O Gerenciador de tarefas do navegador Microsoft Edge é um monitor em tempo real que informa a quantidade de memória que uma página está usando no momento.</span><span class="sxs-lookup"><span data-stu-id="70c3b-138">The Microsoft Edge Browser Task Manager is a realtime monitor that tells you how much memory a page is currently using.</span></span>  

1.  <span data-ttu-id="70c3b-139">Pressione `Shift` + `Esc` ou vá para o menu principal do Microsoft Edge e selecione **mais ferramentas**  >  **Gerenciador de tarefas do navegador** para abrir o Gerenciador de tarefas do navegador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="70c3b-139">Press `Shift`+`Esc` or go to the Microsoft Edge main menu and select **More tools** > **Browser Task Manager** to open the Microsoft Edge Browser Task Manager.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Abrir o Gerenciador de tarefas do navegador Microsoft Edge" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       <span data-ttu-id="70c3b-141">Figura 1: abrindo o Gerenciador de tarefas do navegador Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="70c3b-141">Figure 1:  Opening the Microsoft Edge Browser Task Manager</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="70c3b-142">Passe o cursor do mouse sobre o cabeçalho da tabela do Gerenciador de tarefas do navegador Microsoft Edge, abra o menu contextual \ (clique com o botão direito do mouse \) e ative a **memória JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="70c3b-142">Hover on the table header of the Microsoft Edge Browser Task Manager, open the contextual menu \(right-click\), and enable **JavaScript memory**.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Habilitar a memória JavaScript" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       <span data-ttu-id="70c3b-144">Figura 2: habilitar a memória JavaScript</span><span class="sxs-lookup"><span data-stu-id="70c3b-144">Figure 2:  Enable JavaScript memory</span></span>  
    :::image-end:::  
    
<span data-ttu-id="70c3b-145">Essas duas colunas mostram itens diferentes sobre como a sua página está usando a memória.</span><span class="sxs-lookup"><span data-stu-id="70c3b-145">These two columns tell you different things about how your page is using memory.</span></span>  

*   <span data-ttu-id="70c3b-146">A coluna **memória** representa a memória nativa.</span><span class="sxs-lookup"><span data-stu-id="70c3b-146">The **Memory** column represents native memory.</span></span>  <span data-ttu-id="70c3b-147">Os nós DOM são armazenados na memória nativa.</span><span class="sxs-lookup"><span data-stu-id="70c3b-147">DOM nodes are stored in native memory.</span></span>  <span data-ttu-id="70c3b-148">Se esse valor estiver aumentando, os nós DOM serão criados.</span><span class="sxs-lookup"><span data-stu-id="70c3b-148">If this value is increasing, DOM nodes are getting created.</span></span>  
*   <span data-ttu-id="70c3b-149">A coluna **memória JavaScript** representa o heap do js.</span><span class="sxs-lookup"><span data-stu-id="70c3b-149">The **JavaScript Memory** column represents the JS heap.</span></span>  <span data-ttu-id="70c3b-150">Esta coluna contém dois valores.</span><span class="sxs-lookup"><span data-stu-id="70c3b-150">This column contains two values.</span></span>  <span data-ttu-id="70c3b-151">O valor no qual você está interessado é o número Live \ (o número entre parênteses \).</span><span class="sxs-lookup"><span data-stu-id="70c3b-151">The value you are interested in is the live number \(the number in parentheses\).</span></span>  <span data-ttu-id="70c3b-152">O número Live representa a quantidade de memória que os objetos acessíveis na sua página estão usando.</span><span class="sxs-lookup"><span data-stu-id="70c3b-152">The live number represents how much memory the reachable objects on your page are using.</span></span>  <span data-ttu-id="70c3b-153">Se esse número estiver aumentando, os novos objetos serão criados ou os objetos existentes estão crescendo.</span><span class="sxs-lookup"><span data-stu-id="70c3b-153">If this number is increasing, either new objects are being created, or the existing objects are growing.</span></span>  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <span data-ttu-id="70c3b-154">Visualize vazamentos de memória com o painel desempenho</span><span class="sxs-lookup"><span data-stu-id="70c3b-154">Visualize memory leaks with Performance panel</span></span>  

<span data-ttu-id="70c3b-155">Você também pode usar o painel desempenho como outro ponto de partida na investigação.</span><span class="sxs-lookup"><span data-stu-id="70c3b-155">You may also use the Performance panel as another starting point in your investigation.</span></span>  <span data-ttu-id="70c3b-156">O painel desempenho ajuda você a visualizar o uso da memória de uma página ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="70c3b-156">The Performance panel helps you visualize the memory use of a page over time.</span></span>  

1.  <span data-ttu-id="70c3b-157">Abra o painel **desempenho** no devtools.</span><span class="sxs-lookup"><span data-stu-id="70c3b-157">Open the **Performance** panel on DevTools.</span></span>  
1.  <span data-ttu-id="70c3b-158">Habilitar a caixa de seleção **memória** .</span><span class="sxs-lookup"><span data-stu-id="70c3b-158">Enable the **Memory** checkbox.</span></span>  
1.  <span data-ttu-id="70c3b-159">[Fazer uma gravação][DevtoolsEvaluatePerformanceReferenceRecord].</span><span class="sxs-lookup"><span data-stu-id="70c3b-159">[Make a recording][DevtoolsEvaluatePerformanceReferenceRecord].</span></span>  

> [!TIP]
> <span data-ttu-id="70c3b-160">É uma boa prática começar e encerrar sua gravação com uma coleta de lixo forçada.</span><span class="sxs-lookup"><span data-stu-id="70c3b-160">It is a good practice to start and end your recording with a forced garbage collection.</span></span>  <span data-ttu-id="70c3b-161">Selecione o botão coletar coleta de lixo da força de **lixo** ![ ][ImageForceGarbageCollectionIcon] durante a gravação para forçar a coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="70c3b-161">Select the **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button while recording to force garbage collection.</span></span>  

<span data-ttu-id="70c3b-162">Para demonstrar gravações de memória, considere o código abaixo:</span><span class="sxs-lookup"><span data-stu-id="70c3b-162">To demonstrate memory recordings, consider the code below:</span></span>  

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

<span data-ttu-id="70c3b-163">Toda vez que o botão referenciado no código for pressionado, os `div` nós do 10000 serão acrescentados ao corpo do documento, e uma cadeia de caracteres de 1 milhão `x` será colocada na `x` matriz.</span><span class="sxs-lookup"><span data-stu-id="70c3b-163">Every time that the button referenced in the code is pressed, ten thousand `div` nodes are appended to the document body, and a string of one million `x` characters is pushed onto the `x` array.</span></span>  <span data-ttu-id="70c3b-164">Executar o exemplo de código anterior produz uma gravação no painel **desempenho** , como a figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="70c3b-164">Running the previous code sample produces a recording in the **Performance** panel like the following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Crescimento simples" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   <span data-ttu-id="70c3b-166">Figura 3: crescimento simples</span><span class="sxs-lookup"><span data-stu-id="70c3b-166">Figure 3:  Simple growth</span></span>  
:::image-end:::  

<span data-ttu-id="70c3b-167">Primeiro, uma explicação sobre a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="70c3b-167">First, an explanation of the user interface.</span></span>  <span data-ttu-id="70c3b-168">O gráfico de **heap** no painel de **visão geral** \ (abaixo de **net**\) representa o heap do js.</span><span class="sxs-lookup"><span data-stu-id="70c3b-168">The **HEAP** graph in the **Overview** pane \(below **NET**\) represents the JS heap.</span></span>  <span data-ttu-id="70c3b-169">Abaixo do painel **visão geral** está o painel **contador** .</span><span class="sxs-lookup"><span data-stu-id="70c3b-169">Below the **Overview** pane is the **Counter** pane.</span></span>  <span data-ttu-id="70c3b-170">Aqui você pode ver o uso da memória dividido por JS do JS \ (mesmo que o gráfico de **heap** no painel de **visão geral** \), documentos, nós dom, ouvintes e memória GPU.</span><span class="sxs-lookup"><span data-stu-id="70c3b-170">Here you are able to see memory usage broken down by JS heap \(same as **HEAP** graph in the **Overview** pane\), documents, DOM nodes, listeners, and GPU memory.</span></span>  <span data-ttu-id="70c3b-171">Desabilitar uma caixa de seleção oculta-a do gráfico.</span><span class="sxs-lookup"><span data-stu-id="70c3b-171">Disabling a checkbox hides it from the graph.</span></span>  

<span data-ttu-id="70c3b-172">Agora, uma análise do código em comparação com a imagem anterior.</span><span class="sxs-lookup"><span data-stu-id="70c3b-172">Now, an analysis of the code compared with the previous figure.</span></span>  <span data-ttu-id="70c3b-173">Se você observar o contador de nós \ (o gráfico verde \), poderá ver que ele corresponderá perfeitamente com o código.</span><span class="sxs-lookup"><span data-stu-id="70c3b-173">If you look at the node counter \(the green graph\) you are able to see that it matches up cleanly with the code.</span></span>  <span data-ttu-id="70c3b-174">A contagem de nós aumenta em etapas discretas.</span><span class="sxs-lookup"><span data-stu-id="70c3b-174">The node count increases in discrete steps.</span></span>  <span data-ttu-id="70c3b-175">Você pode presumir que cada aumento na contagem de nós é uma chamada para `grow()` .</span><span class="sxs-lookup"><span data-stu-id="70c3b-175">You may presume that each increase in the node count is a call to `grow()`.</span></span>  <span data-ttu-id="70c3b-176">O gráfico de heap do JS \ (o gráfico azul \) não é tão simples.</span><span class="sxs-lookup"><span data-stu-id="70c3b-176">The JS heap graph \(the blue graph\) is not as straightforward.</span></span>  <span data-ttu-id="70c3b-177">Em manter as práticas recomendadas, o primeiro DIP é, na verdade, uma coleta de lixo forçada \ (obtida pressionando-se o botão coletar coleta de lixo da **coleta** de lixo ![ ][ImageForceGarbageCollectionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="70c3b-177">In keeping with best practices, the first dip is actually a forced garbage collection \(achieved by pressing the  **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button\).</span></span>  <span data-ttu-id="70c3b-178">À medida que a gravação progride, você pode ver que o tamanho de heap do JS é pico.</span><span class="sxs-lookup"><span data-stu-id="70c3b-178">As the recording progresses you are able to see that the JS heap size spikes.</span></span>  <span data-ttu-id="70c3b-179">Isso é natural e esperado: o código JavaScript está criando os nós DOM em cada botão pressione e fazendo muito trabalho quando cria a cadeia de caracteres de 1 milhão caracteres.</span><span class="sxs-lookup"><span data-stu-id="70c3b-179">This is natural and expected:  the JavaScript code is creating the DOM nodes on every button press and doing a lot of work when it creates the string of one million characters.</span></span>  <span data-ttu-id="70c3b-180">A chave importante aqui é o fato de que o recurso heap do JS termina mais alto do que começou \ (o "começo" aqui está a ponto após a coleta de lixo forçada \).</span><span class="sxs-lookup"><span data-stu-id="70c3b-180">The key thing here is the fact that the JS heap ends higher than it began \(the "beginning" here being the point after the forced garbage collection\).</span></span>  <span data-ttu-id="70c3b-181">No mundo real, se você viu esse padrão de tamanho de pilha ou tamanho de nó aumentado, pode ser possível definir um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="70c3b-181">In the real world, if you saw this pattern of increasing JS heap size or node size, it may potentially define a memory leak.</span></span>  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <span data-ttu-id="70c3b-182">Descobrir vazamentos de memória de árvore DOM desanexada com instantâneos de heap</span><span class="sxs-lookup"><span data-stu-id="70c3b-182">Discover detached DOM tree memory leaks with Heap Snapshots</span></span>  

<span data-ttu-id="70c3b-183">Um nó DOM é apenas lixo coletado quando não há referências para o nó da árvore DOM ou do código JavaScript em execução na página.</span><span class="sxs-lookup"><span data-stu-id="70c3b-183">A DOM node is only garbage collected when there are no references to the node from either the DOM tree or JavaScript code running on the page.</span></span>  <span data-ttu-id="70c3b-184">Um nó é considerado como "desconectado" quando é removido da árvore DOM, mas alguns JavaScript ainda fazem referência a ele.</span><span class="sxs-lookup"><span data-stu-id="70c3b-184">A node is said to be "detached" when it is removed from the DOM tree but some JavaScript still references it.</span></span>  <span data-ttu-id="70c3b-185">Os nós DOM desanexados são uma causa comum de vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="70c3b-185">Detached DOM nodes are a common cause of memory leaks.</span></span>  <span data-ttu-id="70c3b-186">Esta seção ensina a usar os profilers de heap no DevTools para identificar nós desanexados.</span><span class="sxs-lookup"><span data-stu-id="70c3b-186">This section teaches you how to use the heap profilers in DevTools to identify detached nodes.</span></span>  

<span data-ttu-id="70c3b-187">Aqui está um exemplo simples de nós DOM desanexados.</span><span class="sxs-lookup"><span data-stu-id="70c3b-187">Here is a simple example of detached DOM nodes.</span></span>  

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

<span data-ttu-id="70c3b-188">Selecionar o botão referenciado no código cria um `ul` nó com dez `li` filhos.</span><span class="sxs-lookup"><span data-stu-id="70c3b-188">Selecting the button referenced in the code creates a `ul` node with ten `li` children.</span></span>  <span data-ttu-id="70c3b-189">Os nós são referenciados pelo código, mas não existem na árvore DOM, portanto, cada um é desconectado.</span><span class="sxs-lookup"><span data-stu-id="70c3b-189">The nodes are referenced by the code but do not exist in the DOM tree, so each is detached.</span></span>  

<span data-ttu-id="70c3b-190">Os instantâneos de pilha são uma maneira de identificar nós desanexados.</span><span class="sxs-lookup"><span data-stu-id="70c3b-190">Heap snapshots are one way to identify detached nodes.</span></span>  <span data-ttu-id="70c3b-191">Como o nome indica, os instantâneos de heap mostram como a memória é distribuída entre os objetos JS e os nós DOM da página no momento do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="70c3b-191">As the name implies, heap snapshots show you how memory is distributed among the JS objects and DOM nodes for your page at the point of time of the snapshot.</span></span>  

<span data-ttu-id="70c3b-192">Para criar um instantâneo, abra o DevTools e vá para o painel **memória** , selecione o botão de opção **instantâneo de heap** e, em seguida, pressione o botão **criar instantâneo** .</span><span class="sxs-lookup"><span data-stu-id="70c3b-192">To create a snapshot, open DevTools and go to the **Memory** panel, select the **Heap snapshot** radio button, and then press the **Take snapshot** button.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Criar instantâneo de heap" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   <span data-ttu-id="70c3b-194">Figura 4: criar um instantâneo de heap</span><span class="sxs-lookup"><span data-stu-id="70c3b-194">Figure 4:  Take heap snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="70c3b-195">O instantâneo pode levar algum tempo para processar e carregar.</span><span class="sxs-lookup"><span data-stu-id="70c3b-195">The snapshot may take some time to process and load.</span></span>  <span data-ttu-id="70c3b-196">Após concluir, selecione-o no painel esquerdo \ (chamado de **instantâneos de heap**\).</span><span class="sxs-lookup"><span data-stu-id="70c3b-196">After it is finished, select it from the left-hand panel \(named **HEAP SNAPSHOTS**\).</span></span>  

<span data-ttu-id="70c3b-197">Digite `Detached` a caixa de texto **filtro de classe** para pesquisar árvores dom desanexadas.</span><span class="sxs-lookup"><span data-stu-id="70c3b-197">Type `Detached` in the **Class filter** textbox to search for detached DOM trees.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Filtragem de nós desconectados" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   <span data-ttu-id="70c3b-199">Figura 5: filtragem para nós desanexados</span><span class="sxs-lookup"><span data-stu-id="70c3b-199">Figure 5:  Filtering for detached nodes</span></span>  
:::image-end:::  

<span data-ttu-id="70c3b-200">Expanda o carats para investigar uma árvore desanexada.</span><span class="sxs-lookup"><span data-stu-id="70c3b-200">Expand the carats to investigate a detached tree.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Investigando a árvore desanexada" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   <span data-ttu-id="70c3b-202">Figura 6: investigando a árvore desanexada</span><span class="sxs-lookup"><span data-stu-id="70c3b-202">Figure 6:  Investigating detached tree</span></span>  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

<span data-ttu-id="70c3b-203">Selecione um nó para investigar ainda mais.</span><span class="sxs-lookup"><span data-stu-id="70c3b-203">Select a node to investigate it further.</span></span>  <span data-ttu-id="70c3b-204">No painel **objetos** , você pode ver mais informações sobre o código que o está fazendo referência a ele.</span><span class="sxs-lookup"><span data-stu-id="70c3b-204">In the **Objects** pane you are able to see more information about the code that is referencing it.</span></span>  <span data-ttu-id="70c3b-205">Por exemplo, na figura a seguir, você pode ver que a `detachedNodes` variável está fazendo referência ao nó.</span><span class="sxs-lookup"><span data-stu-id="70c3b-205">For example, in the following figure you are able to see that the `detachedNodes` variable is referencing the node.</span></span>  <span data-ttu-id="70c3b-206">Para corrigir esse vazamento de memória específico, você deve estudar o código que usa a `detachedNodes` variável e garantir que a referência ao nó seja removida quando não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="70c3b-206">To fix this particular memory leak, you should study the code that uses the `detachedNodes` variable and ensure that the reference to the node is removed when it is no longer needed.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Investigando um nó" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   <span data-ttu-id="70c3b-208">Figura 7: investigando um nó</span><span class="sxs-lookup"><span data-stu-id="70c3b-208">Figure 7:  Investigating a node</span></span>  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <span data-ttu-id="70c3b-209">Identificar vazamentos de memória de heap do JS com a instrumentação de alocação na linha do tempo</span><span class="sxs-lookup"><span data-stu-id="70c3b-209">Identify JS heap memory leaks with Allocation instrumentation on timeline</span></span>  

<span data-ttu-id="70c3b-210">A **Instrumentação de alocação na linha do tempo** é outra ferramenta que pode ajudá-lo a rastrear vazamentos de memória no heap do js.</span><span class="sxs-lookup"><span data-stu-id="70c3b-210">**Allocation instrumentation on timeline** is another tool that may help you track down memory leaks in your JS heap.</span></span>  

<span data-ttu-id="70c3b-211">Demonstre a **Instrumentação de distribuição na linha do tempo** usando o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="70c3b-211">Demonstrate **Allocation instrumentation on timeline**  using the following code.</span></span>  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="70c3b-212">Toda vez que o botão referenciado no código é enviado, uma cadeia de caracteres de 1 milhão caracteres é adicionada à `x` matriz.</span><span class="sxs-lookup"><span data-stu-id="70c3b-212">Every time that the button referenced in the code is pushed, a string of one million characters is added to the `x` array.</span></span>  

<span data-ttu-id="70c3b-213">Para gravar uma instrumentação de alocação na linha do tempo, abra o DevTools, vá para o painel **memória** , selecione o botão de opção **Instrumentação de alocação no cronograma** , pressione o botão **Iniciar** , execute a ação que você acha que está causando o vazamento de memória e, em seguida, pressione o botão **parar gravação do perfil de heap** ![ parar gravação ][ImageStopRecordingIcon] quando terminar.</span><span class="sxs-lookup"><span data-stu-id="70c3b-213">To record an Allocation instrumentation on timeline, open DevTools, go to the **Memory** panel, select the **Allocation instrumentation on timeline** radio button, press the **Start** button, perform the action that you suspect is causing the memory leak, and then press the **Stop recording heap profile** ![stop recording][ImageStopRecordingIcon] button when you are done.</span></span>  

<span data-ttu-id="70c3b-214">Durante a gravação, observe se as barras azuis aparecem na instrumentação de alocação na linha do tempo, como na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="70c3b-214">As you are recording, notice if any blue bars show up on the Allocation instrumentation on timeline, like in the following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Novas alocações" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   <span data-ttu-id="70c3b-216">Figura 8: novas atribuições</span><span class="sxs-lookup"><span data-stu-id="70c3b-216">Figure 8:  New allocations</span></span>  
:::image-end:::  

<span data-ttu-id="70c3b-217">Essas barras azuis representam novas alocações de memória.</span><span class="sxs-lookup"><span data-stu-id="70c3b-217">Those blue bars represent new memory allocations.</span></span>  <span data-ttu-id="70c3b-218">Essas novas atribuições de memória são seus candidatos para vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="70c3b-218">Those new memory allocations are your candidates for memory leaks.</span></span>  <span data-ttu-id="70c3b-219">Você pode aplicar zoom em uma barra para filtrar o painel do **Construtor** para mostrar somente os objetos que foram atribuídos durante o período especificado.</span><span class="sxs-lookup"><span data-stu-id="70c3b-219">You are able to zoom on a bar to filter the **Constructor** pane to only show objects that were allocated during the specified timeframe.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Linha do tempo de alocação ampliada" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   <span data-ttu-id="70c3b-221">Figura 9: linha do tempo de alocação ampliada</span><span class="sxs-lookup"><span data-stu-id="70c3b-221">Figure 9:  Zoomed allocation timeline</span></span>  
:::image-end:::  

<span data-ttu-id="70c3b-222">Expanda o objeto e selecione o valor para exibir mais detalhes no painel **objeto** .</span><span class="sxs-lookup"><span data-stu-id="70c3b-222">Expand the object and select the value to view more details in the **Object** pane.</span></span>  <span data-ttu-id="70c3b-223">Por exemplo, na figura a seguir, ao exibir os detalhes do objeto que foi recém atribuído, você deve ser capaz de ver que ele foi atribuído à `x` variável no `Window` escopo.</span><span class="sxs-lookup"><span data-stu-id="70c3b-223">For example, in the following figure, by viewing the details of the object that was newly allocated, you should be able to see that it was allocated to the `x` variable in the `Window` scope.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Detalhes do objeto" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   <span data-ttu-id="70c3b-225">Figura 10: detalhes do objeto</span><span class="sxs-lookup"><span data-stu-id="70c3b-225">Figure 10:  Object details</span></span>  
:::image-end:::  

## <span data-ttu-id="70c3b-226">Investigar a alocação de memória por função</span><span class="sxs-lookup"><span data-stu-id="70c3b-226">Investigate memory allocation by function</span></span>  

<span data-ttu-id="70c3b-227">Use o tipo de perfil de **amostragem de alocação** para exibir a alocação de memória por função de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="70c3b-227">Use the **Allocation sampling** profiling type to view memory allocation by JavaScript function.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Amostragem de alocação de registros" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   <span data-ttu-id="70c3b-229">Figura 11: amostra de alocação de registros</span><span class="sxs-lookup"><span data-stu-id="70c3b-229">Figure 11:  Record Allocation sampling</span></span>  
:::image-end:::  

1.  <span data-ttu-id="70c3b-230">Selecione o botão de opção de **amostragem de alocação** .</span><span class="sxs-lookup"><span data-stu-id="70c3b-230">Select the **Allocation sampling** radio button.</span></span>  <span data-ttu-id="70c3b-231">Se houver um trabalhador na página, você poderá selecioná-lo como o destino do profiling usando o menu suspenso ao lado do botão **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="70c3b-231">If there is a worker on the page, you are able to select that as the profiling target using the dropdown menu next to the **Start** button.</span></span>  
1.  <span data-ttu-id="70c3b-232">Pressione o botão **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="70c3b-232">Press the **Start** button.</span></span>  
1.  <span data-ttu-id="70c3b-233">Execute as ações na página que você deseja investigar.</span><span class="sxs-lookup"><span data-stu-id="70c3b-233">Perform the actions on the page which you want to investigate.</span></span>  
1.  <span data-ttu-id="70c3b-234">Pressione o botão **parar** quando terminar todas as ações.</span><span class="sxs-lookup"><span data-stu-id="70c3b-234">Press the **Stop** button when you have finished all of your actions.</span></span>  

<span data-ttu-id="70c3b-235">DevTools mostra uma divisão da alocação de memória por função.</span><span class="sxs-lookup"><span data-stu-id="70c3b-235">DevTools shows you a breakdown of memory allocation by function.</span></span>  <span data-ttu-id="70c3b-236">O modo de exibição padrão é **pesado (abaixo)**, que exibe as funções que alocavam mais memória na parte superior.</span><span class="sxs-lookup"><span data-stu-id="70c3b-236">The default view is **Heavy (Bottom Up)**, which displays the functions that allocated the most memory at the top.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Amostragem de alocação" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   <span data-ttu-id="70c3b-238">Figura 12: amostra de alocação</span><span class="sxs-lookup"><span data-stu-id="70c3b-238">Figure 12:  Allocation sampling</span></span>  
:::image-end:::  

## <span data-ttu-id="70c3b-239">Coletas frequentes de lixo</span><span class="sxs-lookup"><span data-stu-id="70c3b-239">Spot frequent garbage collections</span></span>  

<span data-ttu-id="70c3b-240">Se a página parecer pausar com frequência, você poderá ter problemas com a coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="70c3b-240">If your page appears to pause frequently, then you may have garbage collection issues.</span></span>  

<span data-ttu-id="70c3b-241">Você pode usar o Gerenciador de tarefas do navegador Microsoft Edge ou as gravações de memória de desempenho para identificar a coleta de lixo frequente.</span><span class="sxs-lookup"><span data-stu-id="70c3b-241">You are able to use either the Microsoft Edge Browser Task Manager or Performance memory recordings to spot frequent garbage collection.</span></span>  <span data-ttu-id="70c3b-242">No Gerenciador de tarefas do navegador Microsoft Edge, a **memória** em elevação e queda frequente ou valores de **memória JavaScript** representam coleta de lixo frequente.</span><span class="sxs-lookup"><span data-stu-id="70c3b-242">In the Microsoft Edge Browser Task Manager, frequently rising and falling **Memory** or **JavaScript Memory** values represent frequent garbage collection.</span></span>  <span data-ttu-id="70c3b-243">Em gravações de desempenho, alterações frequentes \ (em elevação e queda \) na pilha do JS ou nos gráficos de contagem de nós indicam a coleta de lixo frequente.</span><span class="sxs-lookup"><span data-stu-id="70c3b-243">In Performance recordings, frequent changes \(rising and falling\) to the JS heap or node count graphs indicate frequent garbage collection.</span></span>  

<span data-ttu-id="70c3b-244">Depois de identificar o problema, você poderá usar uma **Instrumentação de alocação na gravação da linha do tempo** para descobrir onde a memória está sendo alocada e quais funções estão causando as atribuições.</span><span class="sxs-lookup"><span data-stu-id="70c3b-244">After you have identified the problem, you are able to use an **Allocation instrumentation on timeline** recording to find out where memory is being allocated and which functions are causing the allocations.</span></span>  

<!-- image links -->  

[ImageForceGarbageCollectionIcon]: ../media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: ../media/stop-recording-icon.msft.png  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Desempenho do registro-referência da análise de desempenho"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> <span data-ttu-id="70c3b-246">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="70c3b-246">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="70c3b-247">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="70c3b-247">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="70c3b-249">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="70c3b-249">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
