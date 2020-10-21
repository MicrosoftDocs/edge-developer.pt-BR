---
description: Use a instrumentação de alocação na linha do tempo para localizar objetos que não estão sendo coletados corretamente e continue a reter a memória.
title: Como usar a instrumentação de alocação na linha do tempo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 1e76e3459128be5b659d790163ef62447dd97ae4
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125444"
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

A **Instrumentação de alocação na linha do tempo** tem instantâneos de pilha periodicamente em toda a gravação \ (com frequência a cada 50 ms \) e um instantâneo final no final da gravação.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Instrumentação de alocação na linha do tempo" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **Instrumentação de alocação na linha do tempo**  
:::image-end:::  

> [!NOTE]
> O número após o `@` é uma ID de objeto persiste nos vários instantâneos feitos durante a sessão de gravação.  A ID do objeto persistente permite uma comparação precisa entre os Estados de heap.  Os objetos são movidos durante coletas de lixo, portanto, a exibição do endereço de um objeto não faz sentido.  

## Habilitar a instrumentação de alocação na linha do tempo  

Conclua as seguintes ações para começar a usar a **Instrumentação de alocação na linha do tempo**.  

1.  [Abra o devtools][DevtoolsOpenIndex].  
1.  Abrir o painel **memória** , selecione o botão de opção **Instrumentação de alocação no cronograma** .  
1.  Start recording.  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Instrumentação de alocação na linha do tempo" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       Registrar alocações de atribuições de heap  
    :::image-end:::  
    
## Ler uma linha do tempo de alocação de heap  

A linha do tempo de alocação de heap mostra onde os objetos estão sendo criados e identifica o caminho de retenção.  Na figura a seguir, as barras na parte superior indicam quando novos objetos são encontrados na pilha.  

A altura de cada barra corresponde ao tamanho dos objetos alocados recentemente, e a cor das barras indica se esses objetos ainda estão ativos no instantâneo de heap final.  As barras azuis indicam objetos que ainda estão ao final da linha do tempo, as barras cinza indicam os objetos que foram atribuídos durante a linha do tempo, mas desde que foram coletadas pelo Garbage Collector.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Instrumentação de alocação na linha do tempo" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   **Instrumentação de alocação no instantâneo da linha do tempo**  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple click actions  -->  

Você pode usar os controles deslizantes na linha do tempo acima para ampliar o instantâneo em particular e revisar os objetos que foram alocados recentemente nesse ponto:  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Instrumentação de alocação na linha do tempo" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   Ampliar o instantâneo  
:::image-end:::  

Clicar em um objeto específico na heap mostra a árvore de retenção na parte inferior do instantâneo de heap.  Examinar o caminho de retenção para o objeto deve fornecer a você informações suficientes para entender por que o objeto não foi coletado, e você deve fazer as alterações de código necessárias para remover a referência desnecessária.  

## Exibir a alocação de memória por função  

Você pode visualizar a alocação de memória por meio da função JavaScript.  Para obter mais informações, navegue até [investigar a alocação de memória por função][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open.md "Abrir o Microsoft Edge (Chromium) DevTools | Documentos da Microsoft"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Investigar a alocação de memória por função-corrigir problemas de memória | Documentos da Microsoft"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
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
