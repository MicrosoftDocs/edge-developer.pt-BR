---
description: Saiba como usar o Microsoft Edge e o DevTools para encontrar problemas de memória que afetam o desempenho da página, incluindo vazamentos de memória, excesso de memória e coletas de lixo frequentes.
title: Corrigir problemas de memória
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: ef820353f81eb3fd791433e9c53434dff3b10a60
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992775"
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

# Corrigir problemas de memória  

Saiba como usar o Microsoft Edge e o DevTools para encontrar problemas de memória que afetam o desempenho da página, incluindo vazamentos de memória, excesso de memória e coletas de lixo frequentes.  

### Resumo  

*   Verifique a quantidade de memória que sua página usa no momento com o Gerenciador de tarefas do navegador Microsoft Edge.  
*   Visualize o uso da memória ao longo do tempo com o painel **memória** .  
*   Identificar árvores de DOM desanexadas \ (uma causa comum de vazamentos de memória \) com o **instantâneo de heap**.  
*   Descubra quando está sendo atribuída uma nova memória no seu heap JavaScript \ (JS! heap \) com a **Instrumentação de distribuição na linha do tempo**.  

## Visão geral  

No espírito do modelo de desempenho do **trilho** , o foco de seus esforços de desempenho deve ser seus usuários.  

<!--todo: add RAIL section when available  -->  

Os problemas de memória são importantes porque costumam ser percebêveis pelos usuários.  Os usuários podem perceber problemas de memória das seguintes maneiras:  

*   **O desempenho de uma página é piormente pior ao longo do tempo**.  Isso possivelmente é um sintoma de perda de memória.  Um vazamento de memória é quando um bug na página faz com que a página use cada vez mais e mais memória ao longo do tempo.  
*   **O desempenho de uma página é consistentemente ruim**.  Isso possivelmente é um sintoma de excesso de memória.  O excesso de memória é quando uma página usa mais memória do que o necessário para a velocidade de página ideal.  
*   **O desempenho de uma página é atrasado ou parece pausar com frequência**.  Isso possivelmente é um sintoma de coletas de lixo frequentes.  Coleta de lixo é quando o navegador recupera memória.  O navegador decide quando isso acontece.  Durante as coletas, todos os scripts em execução são pausados.  Portanto, se o navegador estiver coletando um lote, o tempo de execução de script será pausado muito.  

### Inflação da memória: quanto custa "muito grande"?  

É fácil definir um vazamento de memória.  Se um site estiver usando um número cada vez maior de memória, você terá um vazamento.  Mas o excesso de memória é um pouco mais difícil de fixar.  O que é qualificado como "usando muita memória"?  

Não há números rígidos aqui, porque diferentes dispositivos e navegadores têm recursos diferentes.  A mesma página que é executada tranqüilamente em um smartphone high-end pode falhar em um smartphone low-end.  

A chave aqui é usar o modelo de trilho e enfocar seus usuários.  Descubra quais dispositivos são populares com seus usuários e teste sua página nesses dispositivos.  Se a experiência for ruim consistentemente, a página pode estar excedendo os recursos de memória desses dispositivos.  

## Monitorar o uso da memória em tempo real com o Gerenciador de tarefas do navegador Microsoft Edge  

Use o Gerenciador de tarefas do navegador Microsoft Edge como ponto de partida para a investigação do problema de memória.  O Gerenciador de tarefas do navegador Microsoft Edge é um monitor em tempo real que informa a quantidade de memória que uma página está usando no momento.  

1.  Pressione `Shift` + `Esc` ou vá para o menu principal do Microsoft Edge e selecione **mais ferramentas**  >  **Gerenciador de tarefas do navegador** para abrir o Gerenciador de tarefas do navegador Microsoft Edge.  
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Abrir o Gerenciador de tarefas do navegador Microsoft Edge" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       Figura 1: abrindo o Gerenciador de tarefas do navegador Microsoft Edge  
    :::image-end:::  
    
1.  Passe o cursor do mouse sobre o cabeçalho da tabela do Gerenciador de tarefas do navegador Microsoft Edge, abra o menu contextual \ (clique com o botão direito do mouse \) e ative a **memória JavaScript**.  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Habilitar a memória JavaScript" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       Figura 2: habilitar a memória JavaScript  
    :::image-end:::  
    
Essas duas colunas mostram itens diferentes sobre como a sua página está usando a memória.  

*   A coluna **memória** representa a memória nativa.  Os nós DOM são armazenados na memória nativa.  Se esse valor estiver aumentando, os nós DOM serão criados.  
*   A coluna **memória JavaScript** representa o heap do js.  Esta coluna contém dois valores.  O valor no qual você está interessado é o número Live \ (o número entre parênteses \).  O número Live representa a quantidade de memória que os objetos acessíveis na sua página estão usando.  Se esse número estiver aumentando, os novos objetos serão criados ou os objetos existentes estão crescendo.  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## Visualize vazamentos de memória com o painel desempenho  

Você também pode usar o painel desempenho como outro ponto de partida na investigação.  O painel desempenho ajuda você a visualizar o uso da memória de uma página ao longo do tempo.  

1.  Abra o painel **desempenho** no devtools.  
1.  Habilitar a caixa de seleção **memória** .  
1.  [Fazer uma gravação][DevtoolsEvaluatePerformanceReferenceRecord].  

> [!TIP]
> É uma boa prática começar e encerrar sua gravação com uma coleta de lixo forçada.  Selecione o botão coletar coleta de lixo da força de **lixo** ![ ][ImageForceGarbageCollectionIcon] durante a gravação para forçar a coleta de lixo.  

Para demonstrar gravações de memória, considere o código abaixo:  

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

Toda vez que o botão referenciado no código for pressionado, os `div` nós do 10000 serão acrescentados ao corpo do documento, e uma cadeia de caracteres de 1 milhão `x` será colocada na `x` matriz.  Executar o exemplo de código anterior produz uma gravação no painel **desempenho** , como a figura a seguir.  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Crescimento simples" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   Figura 3: crescimento simples  
:::image-end:::  

Primeiro, uma explicação sobre a interface do usuário.  O gráfico de **heap** no painel de **visão geral** \ (abaixo de **net**\) representa o heap do js.  Abaixo do painel **visão geral** está o painel **contador** .  Aqui você pode ver o uso da memória dividido por JS do JS \ (mesmo que o gráfico de **heap** no painel de **visão geral** \), documentos, nós dom, ouvintes e memória GPU.  Desabilitar uma caixa de seleção oculta-a do gráfico.  

Agora, uma análise do código em comparação com a imagem anterior.  Se você observar o contador de nós \ (o gráfico verde \), poderá ver que ele corresponderá perfeitamente com o código.  A contagem de nós aumenta em etapas discretas.  Você pode presumir que cada aumento na contagem de nós é uma chamada para `grow()` .  O gráfico de heap do JS \ (o gráfico azul \) não é tão simples.  Em manter as práticas recomendadas, o primeiro DIP é, na verdade, uma coleta de lixo forçada \ (obtida pressionando-se o botão coletar coleta de lixo da  **coleta** de lixo ![ ][ImageForceGarbageCollectionIcon] \).  À medida que a gravação progride, você pode ver que o tamanho de heap do JS é pico.  Isso é natural e esperado: o código JavaScript está criando os nós DOM em cada botão pressione e fazendo muito trabalho quando cria a cadeia de caracteres de 1 milhão caracteres.  A chave importante aqui é o fato de que o recurso heap do JS termina mais alto do que começou \ (o "começo" aqui está a ponto após a coleta de lixo forçada \).  No mundo real, se você viu esse padrão de tamanho de pilha ou tamanho de nó aumentado, pode ser possível definir um vazamento de memória.  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## Descobrir vazamentos de memória de árvore DOM desanexada com instantâneos de heap  

Um nó DOM é apenas lixo coletado quando não há referências para o nó da árvore DOM ou do código JavaScript em execução na página.  Um nó é considerado como "desconectado" quando é removido da árvore DOM, mas alguns JavaScript ainda fazem referência a ele.  Os nós DOM desanexados são uma causa comum de vazamentos de memória.  Esta seção ensina a usar os profilers de heap no DevTools para identificar nós desanexados.  

Aqui está um exemplo simples de nós DOM desanexados.  

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

Selecionar o botão referenciado no código cria um `ul` nó com dez `li` filhos.  Os nós são referenciados pelo código, mas não existem na árvore DOM, portanto, cada um é desconectado.  

Os instantâneos de pilha são uma maneira de identificar nós desanexados.  Como o nome indica, os instantâneos de heap mostram como a memória é distribuída entre os objetos JS e os nós DOM da página no momento do instantâneo.  

Para criar um instantâneo, abra o DevTools e vá para o painel **memória** , selecione o botão de opção **instantâneo de heap** e, em seguida, pressione o botão **criar instantâneo** .  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Criar instantâneo de heap" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   Figura 4: criar um instantâneo de heap  
:::image-end:::  

O instantâneo pode levar algum tempo para processar e carregar.  Após concluir, selecione-o no painel esquerdo \ (chamado de **instantâneos de heap**\).  

Digite `Detached` a caixa de texto **filtro de classe** para pesquisar árvores dom desanexadas.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Filtragem de nós desconectados" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   Figura 5: filtragem para nós desanexados  
:::image-end:::  

Expanda o carats para investigar uma árvore desanexada.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Investigando a árvore desanexada" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   Figura 6: investigando a árvore desanexada  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

Selecione um nó para investigar ainda mais.  No painel **objetos** , você pode ver mais informações sobre o código que o está fazendo referência a ele.  Por exemplo, na figura a seguir, você pode ver que a `detachedNodes` variável está fazendo referência ao nó.  Para corrigir esse vazamento de memória específico, você deve estudar o código que usa a `detachedUNode` variável e garantir que a referência ao nó seja removida quando não for mais necessária.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Investigando um nó" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   Figura 7: investigando um nó  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## Identificar vazamentos de memória de heap do JS com a instrumentação de alocação na linha do tempo  

A **Instrumentação de alocação na linha do tempo** é outra ferramenta que pode ajudá-lo a rastrear vazamentos de memória no heap do js.  

Demonstre a **Instrumentação de distribuição na linha do tempo**  usando o código a seguir.  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

Toda vez que o botão referenciado no código é enviado, uma cadeia de caracteres de 1 milhão caracteres é adicionada à `x` matriz.  

Para gravar uma instrumentação de alocação na linha do tempo, abra o DevTools, vá para o painel **memória** , selecione o botão de opção **Instrumentação de alocação no cronograma** , pressione o botão **Iniciar** , execute a ação que você acha que está causando o vazamento de memória e, em seguida, pressione o botão **parar gravação do perfil de heap** ![ parar gravação ][ImageStopRecordingIcon] quando terminar.  

Durante a gravação, observe se as barras azuis aparecem na instrumentação de alocação na linha do tempo, como na figura a seguir.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Novas alocações" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   Figura 8: novas atribuições  
:::image-end:::  

Essas barras azuis representam novas alocações de memória.  Essas novas atribuições de memória são seus candidatos para vazamentos de memória.  Você pode aplicar zoom em uma barra para filtrar o painel do **Construtor** para mostrar somente os objetos que foram atribuídos durante o período especificado.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Linha do tempo de alocação ampliada" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   Figura 9: linha do tempo de alocação ampliada  
:::image-end:::  

Expanda o objeto e selecione o valor para exibir mais detalhes no painel **objeto** .  Por exemplo, na figura a seguir, ao exibir os detalhes do objeto que foi recém atribuído, você deve ser capaz de ver que ele foi atribuído à `x` variável no `Window` escopo.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Detalhes do objeto" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   Figura 10: detalhes do objeto  
:::image-end:::  

## Investigar a alocação de memória por função  

Use o tipo de perfil de **amostragem de alocação** para exibir a alocação de memória por função de JavaScript.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Amostragem de alocação de registros" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   Figura 11: amostra de alocação de registros  
:::image-end:::  

1.  Selecione o botão de opção de **amostragem de alocação** .  Se houver um trabalhador na página, você poderá selecioná-lo como o destino do profiling usando o menu suspenso ao lado do botão **Iniciar** .  
1.  Pressione o botão **Iniciar** .  
1.  Execute as ações na página que você deseja investigar.  
1.  Pressione o botão **parar** quando terminar todas as ações.  

DevTools mostra uma divisão da alocação de memória por função.  O modo de exibição padrão é **pesado (abaixo)**, que exibe as funções que alocavam mais memória na parte superior.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Amostragem de alocação" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   Figura 12: amostra de alocação  
:::image-end:::  

## Coletas frequentes de lixo  

Se a página parecer pausar com frequência, você poderá ter problemas com a coleta de lixo.  

Você pode usar o Gerenciador de tarefas do navegador Microsoft Edge ou as gravações de memória de desempenho para identificar a coleta de lixo frequente.  No Gerenciador de tarefas do navegador Microsoft Edge, a **memória** em elevação e queda frequente ou valores de **memória JavaScript** representam coleta de lixo frequente.  Em gravações de desempenho, alterações frequentes \ (em elevação e queda \) na pilha do JS ou nos gráficos de contagem de nós indicam a coleta de lixo frequente.  

Depois de identificar o problema, você poderá usar uma **Instrumentação de alocação na gravação da linha do tempo** para descobrir onde a memória está sendo alocada e quais funções estão causando as atribuições.  

<!-- image links -->  

[ImageForceGarbageCollectionIcon]: ../media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: ../media/stop-recording-icon.msft.png  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Desempenho do registro-referência da análise de desempenho"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
