---
description: Use a instrumentação alocação na linha do tempo para encontrar objetos que não estão sendo coletados corretamente e continuar a reter memória.
title: Como usar a instrumentação de alocação na linha do tempo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: a02249840256b1e5a2469a253d765eb888527662
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564081"
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
# <a name="how-to-use-allocation-instrumentation-on-timeline"></a><span data-ttu-id="91954-104">Como usar a instrumentação de alocação na linha do tempo</span><span class="sxs-lookup"><span data-stu-id="91954-104">How to use Allocation instrumentation on Timeline</span></span>  

<span data-ttu-id="91954-105">Use **a instrumentação alocação na** linha do tempo para encontrar objetos que não estão sendo coletados corretamente e continuar a reter memória.</span><span class="sxs-lookup"><span data-stu-id="91954-105">Use **Allocation instrumentation on timeline** to find objects that are not being properly garbage collected, and continue to retain memory.</span></span>  

## <a name="how-allocation-instrumentation-on-timeline-works"></a><span data-ttu-id="91954-106">Como funciona a instrumentação de alocação na linha do tempo</span><span class="sxs-lookup"><span data-stu-id="91954-106">How Allocation instrumentation on timeline works</span></span>  

<span data-ttu-id="91954-107">**A instrumentação de alocação na** linha do tempo combina as informações detalhadas do instantâneo do **profiler** de pilha com a atualização incremental e o controle do **painel Desempenho.**</span><span class="sxs-lookup"><span data-stu-id="91954-107">**Allocation instrumentation on timeline** combines the detailed snapshot information of the **heap profiler** with the incremental updating and tracking of the **Performance** panel.</span></span>  <span data-ttu-id="91954-108">Da mesma forma, controlar a alocação de heap para objetos envolve iniciar uma gravação, executar uma sequência de ações e interromper a gravação para análise.</span><span class="sxs-lookup"><span data-stu-id="91954-108">Similarly, tracking heap allocation for objects involves starting a recording, performing a sequence of actions, and stopping the recording for analysis.</span></span>  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

<span data-ttu-id="91954-109">**A instrumentação de** alocação na linha do tempo leva instantâneos de pilha periodicamente ao longo da gravação \(com a mesma frequência que a cada 50 ms\) e um instantâneo final no final da gravação.</span><span class="sxs-lookup"><span data-stu-id="91954-109">**Allocation instrumentation on timeline** takes heap snapshots periodically throughout the recording \(as frequently as every 50 ms\) and one final snapshot at the end of the recording.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Instrumentação de alocação na linha do tempo" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **<span data-ttu-id="91954-111">Instrumentação de alocação na linha do tempo</span><span class="sxs-lookup"><span data-stu-id="91954-111">Allocation instrumentation on timeline</span></span>**  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="91954-112">O número após o é uma ID de objeto que persiste entre `@` os vários instantâneos tirados durante a sessão de gravação.</span><span class="sxs-lookup"><span data-stu-id="91954-112">The number after the `@` is an object ID that persists across the multiple snapshots taken during the recording session.</span></span>  <span data-ttu-id="91954-113">A ID do objeto persistente permite uma comparação precisa entre estados de heap.</span><span class="sxs-lookup"><span data-stu-id="91954-113">The persistent object ID enables precise comparison between heap states.</span></span>  <span data-ttu-id="91954-114">Os objetos são movidos durante coletas de lixo, portanto, exibir o endereço de um objeto não faz sentido.</span><span class="sxs-lookup"><span data-stu-id="91954-114">Objects are moved during garbage collections, so displaying the address of an object makes no sense.</span></span>  

## <a name="enable-allocation-instrumentation-on-timeline"></a><span data-ttu-id="91954-115">Habilitar instrumentação de alocação na linha do tempo</span><span class="sxs-lookup"><span data-stu-id="91954-115">Enable Allocation Instrumentation on Timeline</span></span>  

<span data-ttu-id="91954-116">Conclua as seguintes ações para começar a usar **instrumentação de alocação na linha do tempo**.</span><span class="sxs-lookup"><span data-stu-id="91954-116">Complete the following actions to begin using **Allocation instrumentation on timeline**.</span></span>  

1.  <span data-ttu-id="91954-117">[Abra o DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="91954-117">[Open the DevTools][DevtoolsOpenIndex].</span></span>  
1.  <span data-ttu-id="91954-118">Abra o **painel Memória,** selecione o **botão de opção Instrumentação de Alocação na linha do tempo.**</span><span class="sxs-lookup"><span data-stu-id="91954-118">Open the **Memory** panel, select the **Allocation instrumentation on timeline** radio button.</span></span>  
1.  <span data-ttu-id="91954-119">Start recording.</span><span class="sxs-lookup"><span data-stu-id="91954-119">Start recording.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Profiler de alocações de pilha de registro" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       <span data-ttu-id="91954-121">Profiler de alocações de pilha de registro</span><span class="sxs-lookup"><span data-stu-id="91954-121">Record heap allocations profiler</span></span>  
    :::image-end:::  
    
## <a name="read-a-heap-allocation-timeline"></a><span data-ttu-id="91954-122">Ler uma linha do tempo de alocação de pilha</span><span class="sxs-lookup"><span data-stu-id="91954-122">Read a heap allocation timeline</span></span>  

<span data-ttu-id="91954-123">A linha do tempo de alocação de pilha mostra onde os objetos estão sendo criados e identifica o caminho de retenção.</span><span class="sxs-lookup"><span data-stu-id="91954-123">The heap allocation timeline shows where objects are being created and identifies the retaining path.</span></span>  <span data-ttu-id="91954-124">Na figura a seguir, as barras na parte superior indicam quando novos objetos são encontrados na pilha.</span><span class="sxs-lookup"><span data-stu-id="91954-124">In the following figure, the bars at the top indicate when new objects are found in the heap.</span></span>  

<span data-ttu-id="91954-125">A altura de cada barra corresponde ao tamanho dos objetos alocados recentemente, e a cor das barras indica se esses objetos ainda estão ou não no instantâneo de pilha final.</span><span class="sxs-lookup"><span data-stu-id="91954-125">The height of each bar corresponds to the size of the recently allocated objects, and the color of the bars indicate whether or not those objects are still live in the final heap snapshot.</span></span>  <span data-ttu-id="91954-126">Barras azuis indicam objetos que ainda estão ao vivo no final da linha do tempo, barras cinza indicam objetos que foram alocados durante a linha do tempo, mas desde então foram coletados lixo.</span><span class="sxs-lookup"><span data-stu-id="91954-126">Blue bars indicate objects that are still live at the end of the timeline, Gray bars indicate objects that were allocated during the timeline, but have since been garbage collected.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Instrumentação de alocação no instantâneo da linha do tempo" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   <span data-ttu-id="91954-128">**Instrumentação de alocação no instantâneo da linha do tempo**</span><span class="sxs-lookup"><span data-stu-id="91954-128">**Allocation instrumentation on timeline** snapshot</span></span>  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple choose actions  -->  

<span data-ttu-id="91954-129">Você pode usar os controles deslizantes na linha do tempo acima para ampliar esse instantâneo específico e revisar os objetos que foram alocados recentemente nesse ponto:</span><span class="sxs-lookup"><span data-stu-id="91954-129">You are able to use the sliders in the timeline above to zoom into that particular snapshot and review the objects that were recently allocated at that point:</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Ampliar o instantâneo" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   <span data-ttu-id="91954-131">Ampliar o instantâneo</span><span class="sxs-lookup"><span data-stu-id="91954-131">Zoom into snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="91954-132">Escolher um objeto específico na pilha mostra a árvore de retenção na parte inferior do instantâneo de pilha.</span><span class="sxs-lookup"><span data-stu-id="91954-132">Choosing on a specific object in the heap shows the retaining tree in the bottom portion of the heap snapshot.</span></span>  <span data-ttu-id="91954-133">Examinar o caminho de retenção para o objeto deve dar informações suficientes para entender por que o objeto não foi coletado e você deve fazer as alterações de código necessárias para remover a referência desnecessária.</span><span class="sxs-lookup"><span data-stu-id="91954-133">Examining the retaining path to the object should give you enough information to understand why the object was not collected, and you should make the necessary code changes to remove the unnecessary reference.</span></span>  

## <a name="view-memory-allocation-by-function"></a><span data-ttu-id="91954-134">Exibir alocação de memória por função</span><span class="sxs-lookup"><span data-stu-id="91954-134">View memory allocation by function</span></span>  

<span data-ttu-id="91954-135">Você pode exibir a alocação de memória pela função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="91954-135">You are able to view memory allocation by JavaScript function.</span></span>  <span data-ttu-id="91954-136">Para obter mais informações, navegue até [Investigar alocação de memória por função][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].</span><span class="sxs-lookup"><span data-stu-id="91954-136">For more information, navigate to [Investigate memory allocation by function][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="91954-137">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="91954-137">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open/index.md "Abra Microsoft Edge (Chromium) DevTools | Microsoft Docs"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Investigar a alocação de memória por função - Corrigir problemas de memória | Microsoft Docs"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Baixar um Microsoft Edge Channel"  

> [!NOTE]
> <span data-ttu-id="91954-141">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="91954-141">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="91954-142">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) e é de autoria de [Meggin Kearney][MegginKearney] \(Technical Writer\).</span><span class="sxs-lookup"><span data-stu-id="91954-142">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="91954-144">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="91954-144">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
