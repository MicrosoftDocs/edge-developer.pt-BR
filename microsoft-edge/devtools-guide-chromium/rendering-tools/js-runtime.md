---
title: Acelerar o Tempo de Execução do JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 801de4beeec29010ef63b2bcda950b57d4e544f7
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986182"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->

# Acelerar o tempo de execução do JavaScript  

Identifique funções caras usando o painel **memória** .  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Perfis de exemplo" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Perfis de exemplo  
:::image-end:::  

### Resumo  

*   Registre exatamente quais funções foram chamadas e quantas memórias cada requer com a amostragem de alocação no painel **memória** .  
*   Visualize seus perfis como um gráfico de chama.  
    
## Gravar um perfil de amostra  

Se você observar o Jank em seu JavaScript, colete um perfil de amostragem.  Os perfis de amostragem mostram onde o tempo de execução é gasto em funções na sua página.  

1.  Vá para o painel **memória** do devtools.  
1.  Selecione o botão de opção de **amostragem de alocação** .  
1.  Selecione **Iniciar**.  
1.  Dependendo do que você está tentando analisar, você pode recarregar a página, interagir com a página ou simplesmente deixar a página ser executada.  
1.  Selecione o botão **parar** quando terminar.  
    
> [!NOTE]
> Você também pode usar a [API de utilitários de console][DevtoolsConsoleUtilities] para gravar e agrupar perfis a partir da linha de comando.  

## Ver Perfil de amostragem  

Quando terminar a gravação, o DevTools automaticamente preenche o painel **memória** em **perfis de amostragem** com os dados da sua gravação.  

O modo de exibição padrão é **Heavy \ (baixo para cima \)**.  Este modo de exibição permite que você veja quais funções tiveram mais impacto no desempenho e examine os caminhos de chamadas para essas funções.  

### Alterar a ordem de classificação  

Para alterar a ordem de classificação, selecione o menu suspenso ao lado do ícone **função de foco selecionado** \ ( ![ foco selecionado função ][ImageFocusIcon] \) e escolha uma das opções a seguir.

**Gráfico**.  Exibe um gráfico cronológico da gravação.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Gráfico de chama" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Gráfico de chama  
:::image-end:::  

**Pesado \ (abaixo)**.  Lista as funções por meio do impacto no desempenho e permite que você examine os caminhos de chamadas para as funções.  Este é o modo de exibição padrão.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Gráfico pesado" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Gráfico pesado  
:::image-end:::  

**Árvore \ (acima para baixo \)**.  Mostra uma imagem geral da estrutura de chamadas, começando na parte superior da pilha de chamadas.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Gráfico de árvore" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   Gráfico de árvore  
:::image-end:::  

### Funções Exclude  

Para excluir uma função do seu perfil de amostragem, selecione-a e, em seguida, selecione o botão **excluir função selecionada** \ ( ![ excluir função selecionada ][ImageExcludeIcon] \).  A função solicitante \ (pai \) da função excluída \ (filho \) é cobrada pela memória alocada atribuída à função excluída \ (filho \).  

Selecione o botão **restaurar todas as funções** \ ( ![ restaurar todas as funções ][ImageRestoreIcon] \) para restaurar novamente todas as funções excluídas na gravação.  

## Exibir Perfil de amostra como gráfico  

O modo de exibição de gráfico fornece uma representação visual do perfil de amostragem ao longo do tempo.  

Depois de [gravar um perfil de amostragem](#record-a-sampling-profile), exiba a gravação como um gráfico de chama, [alterando a ordem de classificação](#change-sort-order) para **gráfico**.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Modo de exibição de gráfico de chama" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Modo de exibição de gráfico de chama  
:::image-end:::  

O gráfico de chama é dividido em duas partes.  

| dedo | Parte | Descrição |  
| --- |:--- |:--- |  
| um | Visão geral | Uma exibição de olho de toda a gravação.  A altura das barras corresponde à profundidade da pilha de chamadas.  Portanto, quanto mais alta a barra, mais profunda a pilha de chamadas.  |  
| 2 | Pilha de chamadas | Esta é uma exibição detalhada das funções que foram chamadas durante a gravação.  O eixo horizontal é tempo e eixo vertical é a pilha de chamadas.  As pilhas são organizadas de cima para baixo.  Portanto, a função na parte superior acima dela e assim por diante.  |  

As funções são coloridas aleatoriamente.  Não há nenhuma correlação entre as cores usadas nos outros painéis.  No entanto, as funções são sempre coloridas iguais em chamadas para que você possa ver padrões em cada tempo de execução.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Gráfico de chama com anotações" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   Gráfico de chama com anotações  
:::image-end:::  

Uma pilha de chamadas alta não é necessariamente importante, apenas significa que muitas funções foram chamadas.  Mas uma barra larga significa que uma função demorou muito tempo para ser concluída.  Estes são candidatos para otimização.  

### Ampliar partes específicas da gravação  

Selecione, segure e arraste o mouse para a esquerda e para a direita na visão geral para ampliar partes específicas da pilha de chamadas.  Depois de aplicar zoom, a pilha de chamadas exibirá automaticamente a parte da gravação selecionada.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Gráfico ampliado" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   Gráfico ampliado  
:::image-end:::  

### Exibir detalhes da função  

Selecione uma função para exibir a definição no painel **fontes** .  

Passe o mouse sobre uma função para exibir o nome e os dados de tempo.  As informações a seguir são fornecidas.  

| Minuciosa | Descrição |  
|:--- |:--- |  
| **Name** | O nome da função.  |  
| **Tamanho próprio** | O tamanho da chamada atual da função, incluindo somente as instruções na função.  |  
| **Tamanho total** | O tamanho da invocação atual dessa função e de todas as funções chamadas.  |  
| **URL** | O local da definição da função na forma de `base.js:261` onde `base.js` está o nome do arquivo em que a função está definida e `261` é o número da linha da definição.  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Exibir detalhes de funções no gráfico" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   Exibir detalhes de funções no gráfico  
:::image-end:::  

## Entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExcludeIcon]: ../media/exclude-icon.msft.png  
[ImageFocusIcon]: ../media/focus-icon.msft.png  
[ImageRestoreIcon]: ../media/restore-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Referência de API de utilitários de console | Documentos da Microsoft"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "Perfil-referência API de utilitários de console | Documentos da Microsoft"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd-referência de API de utilitários de console | Documentos da Microsoft"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \) e [Meggin Kearney][MegginKearney] \ (Tech Writer \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
