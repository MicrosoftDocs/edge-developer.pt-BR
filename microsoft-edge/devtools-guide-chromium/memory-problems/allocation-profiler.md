---
description: Use a instrumentação alocação na linha do tempo para encontrar objetos que não estão sendo coletados corretamente e continuar a reter memória.
title: Como usar a instrumentação de alocação na linha do tempo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 374b7f0ad80b8975319b2b0ec5cecf42ce4bde82
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397815"
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

# <a name="how-to-use-allocation-instrumentation-on-timeline"></a>Como usar a instrumentação de alocação na linha do tempo  

Use **a instrumentação alocação na** linha do tempo para encontrar objetos que não estão sendo coletados corretamente e continuar a reter memória.  

## <a name="how-allocation-instrumentation-on-timeline-works"></a>Como funciona a instrumentação de alocação na linha do tempo  

**A instrumentação de alocação na** linha do tempo combina as informações detalhadas do instantâneo do **profiler** de pilha com a atualização incremental e o controle do **painel Desempenho.**  Da mesma forma, controlar a alocação de heap para objetos envolve iniciar uma gravação, executar uma sequência de ações e interromper a gravação para análise.  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

**A instrumentação de** alocação na linha do tempo leva instantâneos de pilha periodicamente ao longo da gravação \(com a mesma frequência que a cada 50 ms\) e um instantâneo final no final da gravação.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Instrumentação de alocação na linha do tempo" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **Instrumentação de alocação na linha do tempo**  
:::image-end:::  

> [!NOTE]
> O número após o é uma ID de objeto que persiste entre `@` os vários instantâneos tirados durante a sessão de gravação.  A ID do objeto persistente permite uma comparação precisa entre estados de heap.  Os objetos são movidos durante coletas de lixo, portanto, exibir o endereço de um objeto não faz sentido.  

## <a name="enable-allocation-instrumentation-on-timeline"></a>Habilitar instrumentação de alocação na linha do tempo  

Conclua as seguintes ações para começar a usar **instrumentação de alocação na linha do tempo**.  

1.  [Abra o DevTools][DevtoolsOpenIndex].  
1.  Abra o **painel Memória,** selecione o **botão de opção Instrumentação de Alocação na linha do tempo.**  
1.  Start recording.  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Profiler de alocações de pilha de registro" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       Profiler de alocações de pilha de registro  
    :::image-end:::  
    
## <a name="read-a-heap-allocation-timeline"></a>Ler uma linha do tempo de alocação de pilha  

A linha do tempo de alocação de pilha mostra onde os objetos estão sendo criados e identifica o caminho de retenção.  Na figura a seguir, as barras na parte superior indicam quando novos objetos são encontrados na pilha.  

A altura de cada barra corresponde ao tamanho dos objetos alocados recentemente, e a cor das barras indica se esses objetos ainda estão ou não no instantâneo de pilha final.  Barras azuis indicam objetos que ainda estão ao vivo no final da linha do tempo, barras cinza indicam objetos que foram alocados durante a linha do tempo, mas desde então foram coletados lixo.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Instrumentação de alocação no instantâneo da linha do tempo" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   **Instrumentação de alocação no instantâneo da linha do tempo**  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple choose actions  -->  

Você pode usar os controles deslizantes na linha do tempo acima para ampliar esse instantâneo específico e revisar os objetos que foram alocados recentemente nesse ponto:  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Ampliar o instantâneo" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   Ampliar o instantâneo  
:::image-end:::  

Escolher um objeto específico na pilha mostra a árvore de retenção na parte inferior do instantâneo de pilha.  Examinar o caminho de retenção para o objeto deve dar informações suficientes para entender por que o objeto não foi coletado e você deve fazer as alterações de código necessárias para remover a referência desnecessária.  

## <a name="view-memory-allocation-by-function"></a>Exibir alocação de memória por função  

Você pode exibir a alocação de memória pela função JavaScript.  Para obter mais informações, navegue até [Investigar alocação de memória por função][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open/index.md "Abra o Microsoft Edge (Chromium) DevTools | Microsoft Docs"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Investigar a alocação de memória por função - Corrigir problemas de memória | Microsoft Docs"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Baixar um Canal do Microsoft Edge"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) e é de autoria de [Meggin Kearney][MegginKearney] \(Technical Writer\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
