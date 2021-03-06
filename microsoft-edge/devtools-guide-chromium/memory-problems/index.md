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

# <a name="fix-memory-problems"></a>Corrigir problemas de memória  

Saiba como usar o Microsoft Edge e o DevTools para encontrar problemas de memória que afetam o desempenho da página, incluindo vazamentos de memória, inchação de memória e coletas de lixo frequentes.  

### <a name="summary"></a>Resumo  

*   Descubra quanta memória sua página está usando no momento com o Gerenciador de Tarefas do Navegador do Microsoft Edge.  
*   Visualize o uso de memória ao longo do tempo com o **painel Memória.**  
*   Identificar árvores DOM desvinculadas \(uma causa comum de vazamentos de memória\) com **o instantâneo heap**.  
*   Descubra quando a nova memória está sendo alocada em sua pilha JavaScript \(pilha JS\) com **instrumentação de**Alocação na linha do tempo .  

## <a name="overview"></a>Visão geral  

No espírito do modelo de desempenho **rail,** o foco de seus esforços de desempenho deve ser seus usuários.  

<!--todo: add RAIL section when available  -->  

Problemas de memória são importantes porque eles geralmente são compreensíveis pelos usuários.  Os usuários podem perceber problemas de memória das seguintes maneiras:  

*   **O desempenho de uma página piora progressivamente ao longo do tempo.**  Isso é possivelmente um sintoma de um vazamento de memória.  Um vazamento de memória é quando um bug na página faz com que a página use progressivamente mais e mais memória ao longo do tempo.  
*   **O desempenho de uma página é consistentemente ruim.**  Isso é possivelmente um sintoma de inchação de memória.  O inchação da memória é quando uma página usa mais memória do que o necessário para a velocidade ideal da página.  
*   **O desempenho de uma página é atrasado ou parece pausar com frequência.**  Isso é possivelmente um sintoma de coletas de lixo frequentes.  Coleta de lixo é quando o navegador recupera memória.  O navegador decide quando isso acontece.  Durante as coleções, todo o script em execução é pausado.  Portanto, se o navegador estiver coletando muito lixo, o tempo de execução do script será bastante pausado.  

### <a name="memory-bloat-how-much-is-too-much"></a>Inchação da memória: quanto é "muito"?  

Um vazamento de memória é fácil de definir.  Se um site estiver usando progressivamente mais e mais memória, você terá um vazamento.  Mas o inchar da memória é um pouco mais difícil de fixar.  O que se qualifica como "usar muita memória"?  

Não há números rígidos aqui, porque diferentes dispositivos e navegadores têm recursos diferentes.  A mesma página que é executado sem problemas em um smartphone high-end pode falhar em um smartphone low-end.  

A chave aqui é usar o modelo RAIL e se concentrar em seus usuários.  Descubra quais dispositivos são populares com seus usuários e teste sua página nesses dispositivos.  Se a experiência for consistentemente ruim, a página pode estar excedendo os recursos de memória desses dispositivos.  

## <a name="monitor-memory-use-in-realtime-with-the-microsoft-edge-browser-task-manager"></a>Monitorar o uso de memória em tempo real com o Gerenciador de Tarefas do Navegador do Microsoft Edge  

Use o Gerenciador de Tarefas do Navegador do Microsoft Edge como ponto de partida para a investigação de problemas de memória.  O Gerenciador de Tarefas do Navegador do Microsoft Edge é um monitor em tempo real que informa a memória que uma página está usando no momento.  

1.  Selecione `Shift` + `Esc` ou navegue até o menu principal do Microsoft Edge **** e escolha Mais ferramentas  >  **Gerenciador** de Tarefas do Navegador para abrir o Gerenciador de Tarefas do Navegador do Microsoft Edge.  
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Abrindo o Gerenciador de Tarefas do Navegador do Microsoft Edge" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       Figura 1: Abrindo o Gerenciador de Tarefas do Navegador do Microsoft Edge  
    :::image-end:::  
    
1.  Passe o mouse no header da tabela do Gerenciador de Tarefas do Navegador do Microsoft Edge, abra o menu contextual \(clique com o botão direito do mouse\) e habilite a memória **JavaScript.**  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Habilitar memória JavaScript" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       Figura 2: Habilitar memória JavaScript  
    :::image-end:::  
    
Essas duas colunas contam coisas diferentes sobre como sua página está usando memória.  

*   A **coluna Memória** representa a memória nativa.  Nós DOM são armazenados na memória nativa.  Se esse valor estiver aumentando, nós DOM serão criados.  
*   A **coluna Memória JavaScript** representa a pilha JS.  Esta coluna contém dois valores.  O valor em que você está interessado é o número ao vivo \(o número entre parênteses\).  O número ao vivo representa a quantidade de memória que os objetos acessíveis em sua página estão usando.  Se esse número estiver aumentando, novos objetos estão sendo criados ou os objetos existentes estão crescendo.  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <a name="visualize-memory-leaks-with-performance-panel"></a>Visualizar vazamentos de memória com painel desempenho  

Você também pode usar o painel Desempenho como outro ponto de partida em sua investigação.  O painel Desempenho ajuda você a visualizar o uso de memória de uma página ao longo do tempo.  

1.  Abra o **painel Desempenho** no DevTools.  
1.  Habilita **a caixa de** seleção Memória.  
1.  [Faça uma gravação][DevtoolsEvaluatePerformanceReferenceRecord].  

> [!TIP]
> É uma boa prática iniciar e encerrar sua gravação com uma coleta de lixo forçada.  Para forçar a coleta de lixo, escolha o botão **coletar** lixo ![ force coleta de lixo durante a ][ImageForceGarbageCollectionIcon] gravação.  

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

Sempre que o botão referenciado no código é escolhido, dez mil nós são anexados ao corpo do documento e uma cadeia de caracteres de um milhão de caracteres é empurrada para a `div` `x` `x` matriz.  Executar o exemplo de código anterior produz uma gravação no painel **Desempenho** como a figura a seguir.  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Crescimento simples" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   Figura 3: Crescimento simples  
:::image-end:::  

Primeiro, uma explicação da interface do usuário.  O **gráfico HEAP** no painel **Visão** geral \(abaixo de **NET**\) representa a pilha JS.  Abaixo do **painel Visão** geral está o **painel Contador.**  O uso da memória é dividido pela pilha JS \(mesmo que o gráfico **HEAP** no **painel** Visão geral\), documentos, nós DOM, ouvintes e memória GPU.  Desativar uma caixa de seleção para escondê-la do gráfico.  

Agora, uma análise do código em comparação com a figura anterior.  Se você revisar o contador de nó \(o gráfico verde\), ele corresponde limpo ao código.  A contagem de nós aumenta em etapas discretas.  Você pode presumir que cada aumento na contagem de nós é uma chamada para `grow()` .  O gráfico de pilha JS \(o gráfico azul\) não é tão simples.  De acordo com as práticas recomendadas, o primeiro dip **** é, na verdade, um conjunto de lixo forçado \(escolha o botão coletar coleta de lixo ![ ][ImageForceGarbageCollectionIcon] forçado\).  À medida que a gravação progride, os picos de tamanho da pilha JS são exibidos.  Isso é natural e esperado: o código JavaScript está criando os nós DOM em cada botão que você escolher e fazendo muito trabalho quando cria a cadeia de caracteres de um milhão de caracteres.  O principal aqui é o fato de que a pilha JS termina mais alto do que começou \(o "início" aqui sendo o ponto após a coleta de lixo forçada\).  No mundo real, se você viu esse padrão de aumento do tamanho da pilha JS ou tamanho do nó, ele pode definir potencialmente um vazamento de memória.  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <a name="discover-detached-dom-tree-memory-leaks-with-heap-snapshots"></a>Descobrir vazamentos de memória de árvore DOM desvinculados com Instantâneos de Pilha  

Um nó DOM é apenas lixo coletado quando não há referências ao nó da árvore DOM ou do código JavaScript em execução na página.  Um nó é dito como "desvinculado" quando é removido da árvore DOM, mas alguns JavaScript ainda a referenciam.  Nós DOM desvinculados são uma causa comum de vazamentos de memória.  Esta seção ensina como usar os perfis de pilha no DevTools para identificar nós desvinculados.  

Aqui está um exemplo simples de nós DOM desvinculados.  

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

Escolher o botão referenciado no código cria um `ul` nó com dez `li` filhos.  Os nós são referenciados pelo código, mas não existem na árvore DOM, portanto, cada um é desvinculado.  

Instantâneos de pilha são uma maneira de identificar nós desvinculados.  Como o nome sugere, os instantâneos de pilha mostram como a memória é distribuída entre os objetos JS e nós DOM para sua página no momento do instantâneo.  

Para criar um instantâneo, abra DevTools e navegue até o painel Memória, escolha o botão de > **de** instantâneo de pilha. **** ****  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Fazer instantâneo de pilha" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   Figura 4: Fazer instantâneo de pilha  
:::image-end:::  

O instantâneo pode levar algum tempo para processar e carregar.  Depois que terminar, selecione-o no painel à esquerda \(denominado **HEAP SNAPSHOTS**\).  

Digite `Detached` na caixa de texto **Filtro** de classe para pesquisar árvores DOM desvinculadas.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Filtragem para nós desvinculados" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   Figura 5: Filtragem para nós desvinculados  
:::image-end:::  

Expanda os quilates para investigar uma árvore desvinculada.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Investigando árvore desvinculada" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   Figura 6: Investigando árvore desvinculada  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

Escolha um nó para investigar ainda mais.  No painel **Objetos,** você pode revisar mais informações sobre o código que está fazendo referência a ele.  Por exemplo, na figura a seguir, a `detachedNodes` variável está fazendo referência ao nó.  Para corrigir o vazamento de memória específico, você deve estudar o código que usa a variável e garantir que a referência ao nó seja removida quando ela `detachedUNode` não for mais necessária.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Investigando um nó" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   Figura 7: Investigando um nó  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <a name="identify-js-heap-memory-leaks-with-allocation-instrumentation-on-timeline"></a>Identificar vazamentos de memória de pilha JS com instrumentação de alocação na linha do tempo  

**A instrumentação de alocação na** linha do tempo é outra ferramenta que pode ajudá-lo a rastrear vazamentos de memória na pilha JS.  

Demonstrar **instrumentação de alocação na linha do tempo**  usando o código a seguir.  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

Sempre que o botão referenciado no código é pressionado, uma cadeia de caracteres de um milhão de caracteres é adicionada à `x` matriz.  

Para registrar uma instrumentação de Alocação na linha **** do tempo, abra DevTools, navegue **** até o painel Memória, escolha a **instrumentação** alocação **** no botão de rádio linha do tempo, escolha o botão Iniciar, execute a ação que você suspeita que está causando o vazamento de memória e escolha o botão Parar a gravação de perfil de pilha de gravação parar de gravar quando ![ ][ImageStopRecordingIcon] terminar.  

À medida que você estiver gravando, observe se alguma barra azul aparecer na instrumentação Alocação na linha do tempo, como na figura a seguir.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Novas alocações" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   Figura 8: Novas alocações  
:::image-end:::  

Essas barras azuis representam novas alocações de memória.  Essas novas alocações de memória são seus candidatos a vazamentos de memória.  Você pode ampliar uma barra para filtrar o **painel** construtor para mostrar somente objetos que foram alocados durante o período especificado.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Linha do tempo de alocação ampliada" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   Figura 9: Linha do tempo de alocação ampliada  
:::image-end:::  

Expanda o objeto e selecione o valor para exibir mais detalhes no **painel Objeto.**  Por exemplo, na figura a seguir, nos detalhes do objeto recém-alocado indica que ele foi alocado à variável `x` no `Window` escopo.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Detalhes do objeto" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   Figura 10: Detalhes do objeto  
:::image-end:::  

## <a name="investigate-memory-allocation-by-function"></a>Investigar a alocação de memória por função  

Use o **tipo de perfil de amostragem** de alocação para exibir a alocação de memória pela função JavaScript.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Amostragem de Alocação de Registros" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   Figura 11: Amostragem de Alocação de Registros  
:::image-end:::  

1.  Escolha o **botão de rádio de amostragem** de alocação.  Se houver um trabalhador na página, você poderá selecionar isso como o destino da criação de perfil usando o menu suspenso ao lado do **botão Iniciar.**  
1.  Escolha o **botão Iniciar.**  
1.  Conclua as ações na página da Web que você deseja investigar.  
1.  Escolha o **botão Parar** quando tiver concluído todas as suas ações.  

DevTools mostra uma divisão da alocação de memória por função.  O modo de exibição padrão **é Heavy (Bottom Up)**, que exibe as funções que alocaram a maior parte da memória na parte superior.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Amostragem de alocação" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   Figura 12: Amostragem de alocação  
:::image-end:::  

## <a name="spot-frequent-garbage-collections"></a>Coletas de lixo frequentes no local  

Se sua página parece pausar com frequência, talvez você tenha problemas de coleta de lixo.  

Você pode usar o Gerenciador de Tarefas do Navegador do Microsoft Edge ou gravações de memória de desempenho para detectar coleta de lixo frequente.  No Gerenciador de Tarefas do Navegador do Microsoft Edge, os valores de **Memória** ou Memória **JavaScript** frequentemente crescentes e em queda representam coleta de lixo frequente.  Em Gravações de desempenho, as alterações frequentes \(crescente e em queda\) para a pilha JS ou gráficos de contagem de nós indicam coleta de lixo frequente.  

Depois de identificar o problema, você poderá usar uma **instrumentação de** Alocação no registro de linha do tempo para descobrir onde a memória está sendo alocada e quais funções estão causando as alocações.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

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
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
