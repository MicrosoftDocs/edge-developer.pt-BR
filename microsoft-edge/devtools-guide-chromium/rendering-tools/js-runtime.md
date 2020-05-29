---
title: Acelerar o tempo de execução do JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 0e198be3e1cef53590a24bfaa2382746ced299ed
ms.sourcegitcommit: 0342d99bf8d3212068890bab0e1e960afa507c02
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611868"
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

> ##### Figura 1  
> Perfis de amostragem  
> ![Perfis de amostragem][ImageCpuProfile]  

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

Para alterar a ordem de classificação, selecione o menu suspenso ao lado do ícone função selecionada foco **da função** ![ selecionada ][ImageFocusIcon] e escolha uma das opções a seguir.

**Gráfico**.  Exibe um gráfico cronológico da gravação.  

> ##### Figura 2  
> Gráfico de chama  
> ![Gráfico de chama][ImageFlameChart]  

**Pesado \ (abaixo)**.  Lista as funções por meio do impacto no desempenho e permite que você examine os caminhos de chamadas para as funções.  Este é o modo de exibição padrão.  

> ##### Figura 3  
> Gráfico pesado  
> ![Gráfico pesado][ImageHeavyChart]  

**Árvore \ (acima para baixo \)**.  Mostra uma imagem geral da estrutura de chamadas, começando na parte superior da pilha de chamadas.  

> ##### Figura 4  
> Gráfico de árvore  
> ![Gráfico de árvore][ImageTreeChart]  

### Funções Exclude   

Para excluir uma função do seu perfil de amostragem, selecione-a para selecioná-la e, em seguida, **Selecione o ícone Excluir função** selecionada ![ excluir função selecionada ][ImageExcludeIcon] .  A função solicitante \ (pai \) da função excluída \ (filho \) é cobrada pela memória alocada atribuída à função excluída \ (filho \).  

Selecione o ícone **restaurar todas** as funções ![ restaurar todas as funções ][ImageRestoreIcon] para restaurar novamente todas as funções excluídas na gravação.  

## Exibir Perfil de amostra como gráfico   

O modo de exibição de gráfico fornece uma representação visual do perfil de amostragem ao longo do tempo.  

Depois de [gravar um perfil de amostragem](#record-a-sampling-profile), exiba a gravação como um gráfico de chama, [alterando a ordem de classificação](#change-sort-order) para **gráfico**.  

> ##### Figura 5  
> Modo de exibição de gráfico de chama  
> ![Modo de exibição de gráfico de chama][ImageFlameChartView]  

O gráfico de chama é dividido em duas partes.  

| | Parte | Descrição |  
| --- |:--- |:--- |  
| um | Visão geral | Uma exibição de olho de toda a gravação.  A altura das barras corresponde à profundidade da pilha de chamadas.  Portanto, quanto mais alta a barra, mais profunda a pilha de chamadas.  |  
| 2 | Pilha de chamadas | Esta é uma exibição detalhada das funções que foram chamadas durante a gravação.  O eixo horizontal é tempo e eixo vertical é a pilha de chamadas.  As pilhas são organizadas de cima para baixo.  Portanto, a função na parte superior acima dela e assim por diante.  |  

As funções são coloridas aleatoriamente.  Não há nenhuma correlação entre as cores usadas nos outros painéis.  No entanto, as funções são sempre coloridas iguais em chamadas para que você possa ver padrões em cada tempo de execução.  

> ##### Figura 6  
> Gráfico de chama com anotações  
> ![Gráfico de chama com anotações][ImageAnnotatedFlameChart]  

Uma pilha de chamadas alta não é necessariamente importante, apenas significa que muitas funções foram chamadas.  Mas uma barra larga significa que uma função demorou muito tempo para ser concluída.  Estes são candidatos para otimização.  

### Ampliar partes específicas da gravação   

Selecione, segure e arraste o mouse para a esquerda e para a direita na visão geral para ampliar partes específicas da pilha de chamadas.  Depois de aplicar zoom, a pilha de chamadas exibirá automaticamente a parte da gravação selecionada.  

> ##### Figura 7  
> Gráfico ampliado  
> ![Gráfico ampliado][ImageFlameChartZoomed]  

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

> ##### Figura 8  
> Exibir detalhes de funções no gráfico  
> ![Exibir detalhes de funções no gráfico][ImageFunctionsDetails]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageExcludeIcon]: /microsoft-edge/devtools-guide-chromium/media/exclude-icon.msft.png  
[ImageFocusIcon]: /microsoft-edge/devtools-guide-chromium/media/images/focus-icon.msft.png  
[ImageRestoreIcon]: /microsoft-edge/devtools-guide-chromium/media/images/restore-icon.msft.png  

[ImageCpuProfile]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png "Figura 1: perfis de amostragem"  
[ImageFlameChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png "Figura 2: gráfico de chama"  
[ImageHeavyChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png "Figura 3: gráfico pesado"  
[ImageTreeChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png "Figura 4: gráfico de árvore"  
[ImageFlameChartView]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png "Figura 5: modo de exibição de gráfico da chama"  
[ImageAnnotatedFlameChart]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png "Figura 6: gráfico de chama com anotações"  
[ImageFlameChartZoomed]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png "Figura 7: gráfico ampliado"  
[ImageFunctionsDetails]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png "Figura 8: Exibir detalhes de funções no gráfico"  

<!-- links -->  

[DevtoolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Referência de API de utilitários de console"  
[DevtoolsConsoleUtilitiesProfile]: /microsoft-edge/devtools-guide-chromium/console/utilities#profile "Referência da API de utilitários do console-perfil"  
[DevtoolsConsoleUtilitiesProfileEnd]: /microsoft-edge/devtools-guide-chromium/console/utilities#profileend "profileEnd-referência de API de utilitários de console"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools & Lighthouse \) e [Meggin Kearney][MegginKearney] \ (Tech Writer \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
