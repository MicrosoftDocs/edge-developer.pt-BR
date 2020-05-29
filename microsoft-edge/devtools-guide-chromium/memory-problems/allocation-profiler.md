---
title: Como usar a instrumentação de alocação na linha do tempo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: ab7a270e1d599e254aaaf4515b6898cb1d9782fc
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611731"
---
<!-- Copyright Meggin Kearney 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->





# <span data-ttu-id="177c2-103">Como usar a instrumentação de alocação na linha do tempo</span><span class="sxs-lookup"><span data-stu-id="177c2-103">How to Use Allocation Instrumentation on Timeline</span></span>  



<span data-ttu-id="177c2-104">Use a **Instrumentação de alocação na linha do tempo** para localizar objetos que não estão sendo coletados corretamente e continue a reter a memória.</span><span class="sxs-lookup"><span data-stu-id="177c2-104">Use **Allocation instrumentation on timeline** to find objects that are not being properly garbage collected, and continue to retain memory.</span></span>  

## <span data-ttu-id="177c2-105">Como a instrumentação de alocação na linha do tempo funciona</span><span class="sxs-lookup"><span data-stu-id="177c2-105">How Allocation instrumentation on timeline works</span></span>  

<span data-ttu-id="177c2-106">A **Instrumentação de alocação na linha do tempo** combina as informações detalhadas do instantâneo do **gerador de perfil de heap** com a atualização e o rastreamento incremental do painel **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="177c2-106">**Allocation instrumentation on timeline** combines the detailed snapshot information of the **heap profiler** with the incremental updating and tracking of the **Performance** panel.</span></span>  <span data-ttu-id="177c2-107">Da mesma forma, rastrear a alocação de heap para objetos envolve iniciar uma gravação, executar uma sequência de ações e interromper a gravação para análise.</span><span class="sxs-lookup"><span data-stu-id="177c2-107">Similarly, tracking heap allocation for objects involves starting a recording, performing a sequence of actions, and stopping the recording for analysis.</span></span>  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

<span data-ttu-id="177c2-108">A **Instrumentação de alocação na linha do tempo** tem instantâneos de pilha periodicamente em toda a gravação \ (com frequência a cada 50 ms! \) e um instantâneo final no final da gravação.</span><span class="sxs-lookup"><span data-stu-id="177c2-108">**Allocation instrumentation on timeline** takes heap snapshots periodically throughout the recording \(as frequently as every 50 ms!\) and one final snapshot at the end of the recording.</span></span>  

> ##### <span data-ttu-id="177c2-109">Figura 1</span><span class="sxs-lookup"><span data-stu-id="177c2-109">Figure 1</span></span>  
> **<span data-ttu-id="177c2-110">Instrumentação de alocação na linha do tempo</span><span class="sxs-lookup"><span data-stu-id="177c2-110">Allocation instrumentation on timeline</span></span>**  
> ![Instrumentação de alocação na linha do tempo][ImageObjectTracker]  

> [!NOTE]
> <span data-ttu-id="177c2-112">O número após o `@` é uma ID de objeto persiste nos vários instantâneos feitos durante a sessão de gravação.</span><span class="sxs-lookup"><span data-stu-id="177c2-112">The number after the `@` is an object ID that persists across the multiple snapshots taken during the recording session.</span></span>  <span data-ttu-id="177c2-113">A ID do objeto persistente permite uma comparação precisa entre os Estados de heap.</span><span class="sxs-lookup"><span data-stu-id="177c2-113">The persistent object ID enables precise comparison between heap states.</span></span>  <span data-ttu-id="177c2-114">Os objetos são movidos durante coletas de lixo, portanto, a exibição do endereço de um objeto não faz sentido.</span><span class="sxs-lookup"><span data-stu-id="177c2-114">Objects are moved during garbage collections, so displaying the address of an object makes no sense.</span></span>  

## <span data-ttu-id="177c2-115">Habilitar a instrumentação de alocação na linha do tempo</span><span class="sxs-lookup"><span data-stu-id="177c2-115">Enable Allocation Instrumentation on Timeline</span></span>  

<span data-ttu-id="177c2-116">Siga estas etapas para começar a usar a **Instrumentação de alocação na linha do tempo**.</span><span class="sxs-lookup"><span data-stu-id="177c2-116">Follow these steps to begin using **Allocation instrumentation on timeline**.</span></span>  

1.  <span data-ttu-id="177c2-117">[Abra o devtools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="177c2-117">[Open the DevTools][DevtoolsOpenIndex].</span></span>  
1.  <span data-ttu-id="177c2-118">Abrir o painel **memória** , selecione o botão de opção **Instrumentação de alocação no cronograma** .</span><span class="sxs-lookup"><span data-stu-id="177c2-118">Open the **Memory** panel, select the **Allocation instrumentation on timeline** radio button.</span></span>  
1.  <span data-ttu-id="177c2-119">Start recording.</span><span class="sxs-lookup"><span data-stu-id="177c2-119">Start recording.</span></span>  

> ##### <span data-ttu-id="177c2-120">Figura 2</span><span class="sxs-lookup"><span data-stu-id="177c2-120">Figure 2</span></span>  
> <span data-ttu-id="177c2-121">Registrar alocações de atribuições de heap</span><span class="sxs-lookup"><span data-stu-id="177c2-121">Record heap allocations profiler</span></span>  
> ![Registrar alocações de atribuições de heap][ImageRecordHeap]  

## <span data-ttu-id="177c2-123">Ler uma linha do tempo de alocação de heap</span><span class="sxs-lookup"><span data-stu-id="177c2-123">Read a heap allocation timeline</span></span>  

<span data-ttu-id="177c2-124">A linha do tempo de alocação de heap mostra onde os objetos estão sendo criados e identifica o caminho de retenção.</span><span class="sxs-lookup"><span data-stu-id="177c2-124">The heap allocation timeline shows where objects are being created and identifies the retaining path.</span></span>  <span data-ttu-id="177c2-125">Na [Figura 3](#figure-3), as barras na parte superior indicam quando novos objetos são encontrados na pilha.</span><span class="sxs-lookup"><span data-stu-id="177c2-125">In [Figure 3](#figure-3), the bars at the top indicate when new objects are found in the heap.</span></span>  

<span data-ttu-id="177c2-126">A altura de cada barra corresponde ao tamanho dos objetos alocados recentemente, e a cor das barras indica se esses objetos ainda estão ativos no instantâneo de heap final.</span><span class="sxs-lookup"><span data-stu-id="177c2-126">The height of each bar corresponds to the size of the recently allocated objects, and the color of the bars indicate whether or not those objects are still live in the final heap snapshot.</span></span>  <span data-ttu-id="177c2-127">As barras azuis indicam objetos que ainda estão ao final da linha do tempo, as barras cinza indicam os objetos que foram atribuídos durante a linha do tempo, mas desde que foram coletadas pelo Garbage Collector.</span><span class="sxs-lookup"><span data-stu-id="177c2-127">Blue bars indicate objects that are still live at the end of the timeline, Gray bars indicate objects that were allocated during the timeline, but have since been garbage collected.</span></span>  

> ##### <span data-ttu-id="177c2-128">Figura 3</span><span class="sxs-lookup"><span data-stu-id="177c2-128">Figure 3</span></span>  
> <span data-ttu-id="177c2-129">**Instrumentação de alocação no instantâneo da linha do tempo**</span><span class="sxs-lookup"><span data-stu-id="177c2-129">**Allocation instrumentation on timeline** snapshot</span></span>  
> ![Instrumentação de alocação no instantâneo da linha do tempo][ImageCollected]  

<!--In [Figure 4](#figure-4), an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple click actions  -->  

<span data-ttu-id="177c2-131">Você pode usar os controles deslizantes na linha do tempo acima para ampliar o instantâneo em particular e ver os objetos que foram alocados recentemente nesse ponto:</span><span class="sxs-lookup"><span data-stu-id="177c2-131">You are able to use the sliders in the timeline above to zoom into that particular snapshot and see the objects that were recently allocated at that point:</span></span>  

> ##### <span data-ttu-id="177c2-132">Figura 4</span><span class="sxs-lookup"><span data-stu-id="177c2-132">Figure 4</span></span>  
> <span data-ttu-id="177c2-133">Ampliar o instantâneo</span><span class="sxs-lookup"><span data-stu-id="177c2-133">Zoom into snapshot</span></span>  
> ![Ampliar o instantâneo][ImageSliders]  

<span data-ttu-id="177c2-135">Clicar em um objeto específico na heap mostra a árvore de retenção na parte inferior do instantâneo de heap.</span><span class="sxs-lookup"><span data-stu-id="177c2-135">Clicking on a specific object in the heap shows the retaining tree in the bottom portion of the heap snapshot.</span></span>  <span data-ttu-id="177c2-136">Examinar o caminho de retenção para o objeto deve fornecer a você informações suficientes para entender por que o objeto não foi coletado, e você deve fazer as alterações de código necessárias para remover a referência desnecessária.</span><span class="sxs-lookup"><span data-stu-id="177c2-136">Examining the retaining path to the object should give you enough information to understand why the object was not collected, and you should make the necessary code changes to remove the unnecessary reference.</span></span>  

## <span data-ttu-id="177c2-137">Exibir a alocação de memória por função</span><span class="sxs-lookup"><span data-stu-id="177c2-137">View memory allocation by function</span></span>   

<span data-ttu-id="177c2-138">Você pode visualizar a alocação de memória por meio da função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="177c2-138">You are able to view memory allocation by JavaScript function.</span></span>  <span data-ttu-id="177c2-139">Consulte [investigar a alocação de memória por função][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction] para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="177c2-139">See [Investigate memory allocation by function][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction] for more information.</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageObjectTracker]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png "Figura 1: Instrumentação de distribuição na linha do tempo"  
[ImageRecordHeap]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png "Figura 2: registrar o gerador de perfil de alocações de heap"  
[ImageCollected]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-timelines-snapshot.msft.png "Figura 3: Instrumentação de alocação no instantâneo da linha do tempo"  
[ImageSliders]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png "Figura 4: ampliar o instantâneo"  

<!-- links -->  

[DevToolsOpenIndex]: /microsoft-edge/devtools-guide-chromium/open "Abrir o Microsoft Edge (Chromium) DevTools"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: /microsoft-edge/devtools-guide-chromium/memory-problems/index#investigate-memory-allocation-by-function "Investigar a alocação de memória por função-corrigir problemas de memória"  

<!--[HeapProfiler]: ../profile/memory-problems/heap-snapshots ""  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Baixar um canal do Microsoft Edge"  

> [!NOTE]
> <span data-ttu-id="177c2-147">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="177c2-147">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="177c2-148">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) e é criada por [Meggin Kearney][MegginKearney] \ (redator técnico \).</span><span class="sxs-lookup"><span data-stu-id="177c2-148">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="177c2-150">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="177c2-150">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
