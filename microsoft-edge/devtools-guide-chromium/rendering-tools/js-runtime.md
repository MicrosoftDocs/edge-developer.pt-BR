---
description: Identifique funções caras usando o painel Memória do Microsoft Edge DevTools.
title: Acelerar o tempo de execução do JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 682001ae8d265b342e5d6e0725f9f8ac4e298cf8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397598"
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

# <a name="speed-up-javascript-runtime"></a>Acelerar o tempo de execução do JavaScript  

Identifique funções caras usando o **painel Memória.**  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Perfis de Exemplo" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Perfis de Exemplo  
:::image-end:::  

### <a name="summary"></a>Resumo  

*   Grave exatamente quais funções foram chamadas e quanta memória cada uma requer com a Amostragem de Alocação no **painel Memória.**  
*   Visualize seus perfis como um gráfico de chama.  
    
## <a name="record-a-sampling-profile"></a>Registrar um perfil de amostragem  

Se você observar jank em seu JavaScript, colete um Perfil de Amostragem.  Os Perfis de Amostragem mostram onde o tempo de execução é gasto em funções em sua página.  

1.  Navegue até **o painel Memória** do DevTools.  
1.  Escolha o **botão de rádio de amostragem** de alocação.  
1.  Escolha **Iniciar**.  
1.  Dependendo do que você está tentando analisar, você pode atualizar a página, interagir com a página ou apenas deixar a página ser executado.  
1.  Escolha o **botão Parar** quando terminar.  
    
> [!NOTE]
> Você também pode usar a [API Utilitários de Console][DevtoolsConsoleUtilities] para gravar e agrupar perfis da linha de comando.  

## <a name="view-sampling-profile"></a>Exibir Perfil de Amostragem  

Quando você terminar de gravar, o DevTools preencherá automaticamente o painel **Memória** em **PERFIS DE AMOSTRAGEM** com os dados da gravação.  

O modo de exibição padrão **é Heavy \(Bottom Up\)**.  Essa exibição permite que você revise quais funções tiveram mais impacto no desempenho e examine o caminho de solicitação para cada função.  

### <a name="change-sort-order"></a>Alterar ordem de classificação  

Para alterar a ordem de classificação, selecione o menu suspenso ao lado da função selecionada **de** foco \( ícone de função selecionada por foco \) e escolha uma ![ das opções a ][ImageFocusIcon] seguir.

**Gráfico**.  Exibe um gráfico cronologicamente da gravação.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Gráfico de chama" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Gráfico de chama  
:::image-end:::  

**Heavy \(Bottom Up\)**.  Lista funções por impacto no desempenho e permite examinar os caminhos de chamada para as funções.  Esse é o modo de exibição padrão.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Gráfico pesado" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Gráfico pesado  
:::image-end:::  

**Árvore \(Top Down\)**.  Mostra uma imagem geral da estrutura de chamada, começando na parte superior da pilha de chamada.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Gráfico de árvore" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   Gráfico de árvore  
:::image-end:::  

### <a name="exclude-functions"></a>Excluir funções  

Para excluir uma função do seu Perfil de Amostragem, selecione-a e selecione o botão **excluir** função selecionada \( excluir função ![ selecionada ][ImageExcludeIcon] \).  A função solicitante \(parent\) da função excluída \(child\) é carregada com a memória alocada atribuída à função excluída \(child\).  

Escolha o **botão restaurar todas as** funções \( restaure todas as funções \) para restaurar todas as funções excluídas de volta à ![ ][ImageRestoreIcon] gravação.  

## <a name="view-sampling-profile-as-chart"></a>Exibir Perfil de Amostragem como Gráfico  

A exibição Gráfico fornece uma representação visual do Perfil de Amostragem ao longo do tempo.  

Depois de [gravar um Perfil de Amostragem,](#record-a-sampling-profile)veja a gravação como um gráfico de chama alterando a ordem de [classificação](#change-sort-order) para **Chart**.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Exibição do gráfico de chama" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Exibição do gráfico de chama  
:::image-end:::  

O gráfico de chama é dividido em duas partes.  

| index | Parte | Descrição |  
| --- |:--- |:--- |  
| 1 | Visão geral | Um ponto de vista de visão de visão de toda a gravação.  A altura das barras corresponde à profundidade da pilha de chamada.  Assim, quanto maior for a barra, mais profunda será a pilha de chamada.  |  
| 2 | Pilha de chamada | Esta é uma visão detalhada das funções que foram chamadas durante a gravação.  O eixo horizontal é o tempo e o eixo vertical é a pilha de chamada.  As pilhas são organizadas de cima para baixo.  Assim, a função na parte superior chamou a uma abaixo dela e assim por diante.  |  

As funções são coloridas aleatoriamente.  Não há correlação com as cores usadas nos outros painéis.  No entanto, as funções são sempre coloridas da mesma forma em invocações para que você possa observar padrões em cada tempo de execução.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Gráfico de chama anotado" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   Gráfico de chama anotado  
:::image-end:::  

Uma pilha de chamadas altas não é necessariamente significativa, apenas significa que muitas funções foram chamadas.  Mas uma barra larga significa que uma função levou muito tempo para ser concluída.  São candidatos à otimização.  

### <a name="zoom-in-on-specific-parts-of-recording"></a>Ampliar partes específicas da gravação  

Escolha, segure e arraste o mouse para a esquerda e para a direita na visão geral para ampliar partes específicas da pilha de chamada.  Depois de ampliar, a pilha de chamada exibe automaticamente a parte da gravação selecionada.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Gráfico ampliado" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   Gráfico ampliado  
:::image-end:::  

### <a name="view-function-details"></a>Exibir detalhes da função  

Escolha uma função para exibir a definição no painel **Fontes.**  

Passe o mouse em uma função para exibir o nome e os dados de tempo.  As informações a seguir são fornecidas.  

| Detalhes | Descrição |  
|:--- |:--- |  
| **Name** | O nome da função.  |  
| **Tamanho próprio** | O tamanho da invocação atual da função, incluindo apenas as instruções na função.  |  
| **Tamanho total** | O tamanho da invocação atual dessa função e todas as funções que ela chamou.  |  
| **URL** | O local da definição da função na forma de onde é o nome do arquivo em que a função é definida e é o número `base.js:261` `base.js` de linha da `261` definição.  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Exibir detalhes das funções no gráfico" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   Exibir detalhes das funções no gráfico  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExcludeIcon]: ../media/exclude-icon.msft.png  
[ImageFocusIcon]: ../media/focus-icon.msft.png  
[ImageRestoreIcon]: ../media/restore-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Referência da API de utilitários de console | Microsoft Docs"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "profile - Referência da API de utilitários de console | Microsoft Docs"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd - Referência da API de utilitários de console | Microsoft Docs"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) é encontrada aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) e [Meggin Kearney][MegginKearney] \(Tech Writer\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
