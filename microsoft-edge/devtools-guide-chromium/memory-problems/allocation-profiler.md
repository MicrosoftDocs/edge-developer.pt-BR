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





# Como usar a instrumentação de alocação na linha do tempo  



Use a **Instrumentação de alocação na linha do tempo** para localizar objetos que não estão sendo coletados corretamente e continue a reter a memória.  

## Como a instrumentação de alocação na linha do tempo funciona  

A **Instrumentação de alocação na linha do tempo** combina as informações detalhadas do instantâneo do **gerador de perfil de heap** com a atualização e o rastreamento incremental do painel **desempenho** .  Da mesma forma, rastrear a alocação de heap para objetos envolve iniciar uma gravação, executar uma sequência de ações e interromper a gravação para análise.  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

A **Instrumentação de alocação na linha do tempo** tem instantâneos de pilha periodicamente em toda a gravação \ (com frequência a cada 50 ms! \) e um instantâneo final no final da gravação.  

> ##### Figura 1  
> **Instrumentação de alocação na linha do tempo**  
> ![Instrumentação de alocação na linha do tempo][ImageObjectTracker]  

> [!NOTE]
> O número após o `@` é uma ID de objeto persiste nos vários instantâneos feitos durante a sessão de gravação.  A ID do objeto persistente permite uma comparação precisa entre os Estados de heap.  Os objetos são movidos durante coletas de lixo, portanto, a exibição do endereço de um objeto não faz sentido.  

## Habilitar a instrumentação de alocação na linha do tempo  

Siga estas etapas para começar a usar a **Instrumentação de alocação na linha do tempo**.  

1.  [Abra o devtools][DevtoolsOpenIndex].  
1.  Abrir o painel **memória** , selecione o botão de opção **Instrumentação de alocação no cronograma** .  
1.  Start recording.  

> ##### Figura 2  
> Registrar alocações de atribuições de heap  
> ![Registrar alocações de atribuições de heap][ImageRecordHeap]  

## Ler uma linha do tempo de alocação de heap  

A linha do tempo de alocação de heap mostra onde os objetos estão sendo criados e identifica o caminho de retenção.  Na [Figura 3](#figure-3), as barras na parte superior indicam quando novos objetos são encontrados na pilha.  

A altura de cada barra corresponde ao tamanho dos objetos alocados recentemente, e a cor das barras indica se esses objetos ainda estão ativos no instantâneo de heap final.  As barras azuis indicam objetos que ainda estão ao final da linha do tempo, as barras cinza indicam os objetos que foram atribuídos durante a linha do tempo, mas desde que foram coletadas pelo Garbage Collector.  

> ##### Figura 3  
> **Instrumentação de alocação no instantâneo da linha do tempo**  
> ![Instrumentação de alocação no instantâneo da linha do tempo][ImageCollected]  

<!--In [Figure 4](#figure-4), an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple click actions  -->  

Você pode usar os controles deslizantes na linha do tempo acima para ampliar o instantâneo em particular e ver os objetos que foram alocados recentemente nesse ponto:  

> ##### Figura 4  
> Ampliar o instantâneo  
> ![Ampliar o instantâneo][ImageSliders]  

Clicar em um objeto específico na heap mostra a árvore de retenção na parte inferior do instantâneo de heap.  Examinar o caminho de retenção para o objeto deve fornecer a você informações suficientes para entender por que o objeto não foi coletado, e você deve fazer as alterações de código necessárias para remover a referência desnecessária.  

## Exibir a alocação de memória por função   

Você pode visualizar a alocação de memória por meio da função JavaScript.  Consulte [investigar a alocação de memória por função][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction] para obter mais informações.  

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
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) e é criada por [Meggin Kearney][MegginKearney] \ (redator técnico \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
