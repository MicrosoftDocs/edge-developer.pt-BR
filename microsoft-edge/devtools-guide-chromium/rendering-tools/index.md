---
description: Os usuários esperam páginas interativas e suaves.  Cada estágio no pipeline de pixels representa uma oportunidade de introduzir jank.  Saiba mais sobre ferramentas e estratégias para identificar e corrigir problemas comuns que retardam o desempenho do tempo de execução.
title: Analisar o desempenho do tempo de execução
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 646db5b2e88e33b109e5eb3ae01a296bf3a4fb46
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397997"
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
   limitations under the License.  -->

# <a name="analyze-runtime-performance"></a>Analisar o desempenho do tempo de execução  

Os usuários esperam páginas interativas e suaves.  Cada estágio no pipeline de pixels representa uma oportunidade de introduzir jank.  Saiba mais sobre ferramentas e estratégias para identificar e corrigir problemas comuns que retardam o desempenho do tempo de execução.  

### <a name="summary"></a>Resumo  

*   Não escreva JavaScript que força o navegador a recalcular o layout.  Separe funções de leitura e gravação e execute leituras primeiro.  
*   Não complique demais seu CSS.  Use menos CSS e mantenha seus seletores CSS simples.  
*   Evite o layout o máximo possível.  Escolha CSS que não aciona o layout.  
*   A pintura pode levar mais tempo do que qualquer outra atividade de renderização.  Cuidado com os gargalos de tinta.  
    
## <a name="javascript"></a>JavaScript  

Cálculos JavaScript, especialmente aqueles que disparam alterações visuais extensas, podem atrasar o desempenho do aplicativo.  Não deixe que o JavaScript em tempo hábil ou de longa duração interfira nas interações do usuário.  

### <a name="javascript-tools"></a>JavaScript: Ferramentas  

Pegue uma gravação na ferramenta **Performance** e procure eventos suspeitosamente `Evaluate Script` longos.  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

f você observar um pouco de jank em seu JavaScript, talvez seja necessário levar sua análise para o próximo nível e coletar um perfil de CPU JavaScript.  Os perfis de CPU mostram onde o tempo de execução é gasto dentro das funções da sua página.  Saiba como criar perfis de CPU no [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].

### <a name="javascript-problems"></a>JavaScript: Problemas  

A tabela a seguir descreve alguns problemas comuns do JavaScript e possíveis soluções.  

| Problema | Exemplo | Solução |  
|:--- |:--- |:--- |  
| Manipuladores de entrada caros que afetam a resposta ou animação.  | Toque, rolagem de paralaxaxas.  | Deixe o navegador manipular toque e rolagem ou vincular o ouvinte o mais tarde possível.  Navegue até [Manipuladores de Entrada Caros na][WebPerformanceCalendarRuntimeChecklist]lista de verificação de desempenho do tempo de execução de Paulo Lewis.  |  
| JavaScript com tempo ruim afetando a resposta, animação, carga.  | O usuário rola logo após o carregamento da página, setTimeout /setInterval.  | Otimizar o tempo de execução do JavaScript: usar `requestAnimationFrame` , propagar a manipulação dom sobre quadros, usar [Web Workers][MDNUsingWebWorkers].  |  
| JavaScript de execução longa afetando a resposta.  | O [evento DOMContentLoaded][MDNUsingWebWorkers] para quando está cheio de trabalho JS.  | Mover trabalho computacional puro para [Web Workers][MDNUsingWebWorkers].  Se você precisar de acesso DOM, use `requestAnimationFrame` .  <!--Navigate to [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| Scripts de lixo y que afetam a resposta ou animação.  | A coleta de lixo pode acontecer em qualquer lugar.  | Escreva menos scripts de lixo y.  Navegue [até Coleta de Lixo em Animação na][WebPerformanceCalendarRuntimeChecklist]lista de verificação de desempenho do tempo de execução de Paulo Lewis.  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <a name="style"></a>Estilo  

As alterações de estilo são caras, especialmente se essas alterações afetarem mais de um elemento no DOM.  Sempre que você aplica estilos a um elemento, o navegador descobre o impacto em todos os elementos relacionados, recalcula o layout e repaints.  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <a name="style-tools"></a>Estilo: Ferramentas  

Fazer uma gravação na **ferramenta Performance.**  Verifique a gravação de eventos `Recalculate Style` grandes \(exibido em roxo\).  

<!--todo: add Recording section when available  -->  

Escolha um `Recalculate Style` evento para exibir mais informações sobre ele no painel **Detalhes.**  Se as alterações de estilo estão demorando muito, isso é um sucesso de desempenho.  Se os cálculos de estilo estão afetando um grande número de elementos, essa é outra área com espaço para aprimoramento.  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Estilo de recálcula longo" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   Estilo de recálcula longo  
:::image-end:::  

Para reduzir o impacto dos `Recalculate Style` eventos:  

*   Use os [Gatilhos CSS para][CssTriggers] saber quais propriedades CSS disparam layout, tinta e composição.  Essas propriedades têm o pior impacto no desempenho da renderização.  
*   Alternar para propriedades que tenham menos impacto.  <!--For more guidance, navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <a name="style-problems"></a>Estilo: Problemas  

A tabela a seguir descreve alguns problemas de estilo comuns e possíveis soluções.  

| Problema | Exemplo | Solução |  
|:--- |:--- |:--- |  
| Cálculos de estilo caros que afetam a resposta ou a animação.  | Qualquer propriedade CSS que altera a geometria de um elemento, como a largura, altura ou posição; o navegador verifica todos os outros elementos e recalcula o layout.  | Evitar CSS que dispara layouts |  
| Seletores complexos que afetam a resposta ou a animação.  | Os seletores aninhados forçam o navegador a saber tudo sobre todos os outros elementos, incluindo pais e filhos.  | Fazer referência a um elemento em seu CSS com apenas uma classe.  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <a name="layout"></a>Layout  

Layout (ou refluxo no Firefox) é o processo pelo qual o navegador calcula as posições e tamanhos de todos os elementos em uma página.  O modelo de layout da Web significa que um elemento pode afetar outros; por exemplo, a largura do elemento normalmente afeta as larguras de todos os elementos filho e assim por diante, todo o caminho para cima e para baixo `<body>` da árvore.  O processo pode estar bastante envolvido para o navegador.  

Como regra geral, se você solicitar um valor geométrico de volta do DOM antes que um quadro seja concluído, você se encontrará com "layouts síncronos forçados", o que pode ser um grande arrojo de desempenho se repetido com frequência ou executado para uma árvore DOM grande.  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <a name="layout-tools"></a>Layout: Ferramentas  

O **painel** Desempenho identifica quando uma página causa layouts síncronos forçados.  Esses `Layout` eventos são marcados com barras vermelhas.  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Layout síncrono forçado" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   Layout síncrono forçado  
:::image-end:::  

"Quebra de layout" é uma repetição das condições de layout síncronas forçadas.  Isso ocorre quando JavaScript grava e lê do DOM repetidamente, o que força o navegador a recalcular o layout repetidamente.  Para identificar a quebra de layout, procure um padrão de vários avisos de layout síncrono forçados.  Revise a figura anterior.  

### <a name="layout-problems"></a>Layout: Problemas  

A tabela a seguir descreve alguns problemas comuns de layout e possíveis soluções.  

| Problema | Exemplo | Solução |  
|:--- |:--- |:--- |  
| Layout síncrono forçado afetando a resposta ou animação.  | Forçando o navegador a executar o layout anteriormente no pipeline de pixels, resultando em etapas repetidas no processo de renderização.  | Em lotes, seu estilo lê primeiro e, em seguida, grava todas as gravações.  <!--Navigate to [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| A reação de layout afetando a resposta ou a animação.  | Um loop que coloca o navegador em um ciclo de leitura-gravação-leitura-gravação, forçando o navegador a recalcular o layout uma e outra vez.  | Operações de leitura em lote automaticamente usando [a biblioteca do FastDom.][GitHubWilsonpageFastdom]  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <a name="paint-and-composite"></a>Tinta e composição  

Paint é o processo de preenchimento de pixels.  Geralmente, é a parte mais cara do processo de renderização.  Se você reparou que sua página não está funcionando como projetada de alguma forma, é provável que você tenha problemas de tinta.  

A composição é onde as partes pintadas da página são colocadas juntas para exibição na tela.  Na maioria das vezes, se você se ater a propriedades somente compositor e evitar a tinta completamente, você deve observar uma melhoria importante no desempenho, mas você precisa ter cuidado com as contagens excessivas de camadas.  <!--Navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <a name="paint-and-composite-tools"></a>Tinta e composição: Ferramentas  

Quer saber quanto tempo a pintura leva ou com que frequência a pintura ocorre?  Verifique a [configuração Habilitar instrumentação de][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] tinta avançada no painel **Desempenho** e, em seguida, fazer uma gravação.  Se a maior parte do tempo de renderização for gasto pintando, você terá problemas de tinta.  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <a name="paint-and-composite-problems"></a>Tinta e composição: Problemas  

A tabela a seguir descreve alguns problemas comuns de tinta e composição e possíveis soluções.  

| Problema | Exemplo | Solução |  
|:--- |:--- |:--- |  
| Tempestades de tinta que afetam a resposta ou animação.  | Áreas de tinta grande ou tintas caras que afetam a resposta ou animação.  | Evite tinta, promova elementos que estão se movendo para sua própria camada, use transformes e opacidade.  <!--Navigate to [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| Explosões de camada que afetam animações.  | A superpromoção de muitos elementos com afeta muito o desempenho `translateZ(0)` da animação.  | Promova para camadas com moderação e somente quando você sabe que ele oferece melhorias tangíveis.  <!--Navigate to [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Acelerar o tempo de execução do JavaScript | Microsoft Docs"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#turn-on-advanced-paint-instrumentation "Ativar instrumentação de tinta avançada - Referência de análise de desempenho | Microsoft Docs"

<!--[DevtoolsRenderingToolsForcedSynchronousLayouts]: ./rendering-tools/forced-synchronous-layouts.md "Diagnose Forced Synchronous Layouts | Microsoft Docs"  -->  

<!-- The Timeline Tool page is deprecated  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfileJavascript]: ../evaluate-performance/timeline-tool#profile-javascript "Profile JavaScript - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfilePainting]: ../evaluate-performance/timeline-tool#profile-painting "Profile painting - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRecording]: ../evaluate-performance/timeline-tool#make-a-recording "Make a recording - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRenderingSettings]: ../evaluate-performance/timeline-tool#rendering-settings "Rendering settings - How to Use the Timeline Tool | Microsoft Docs"  -->  

<!--[WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing "Avoid Large, Complex Layouts, and Layout Thrashing"  -->  
<!--[WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime]: /web/fundamentals/performance/rendering/optimize-javascript-execution "Optimize JavaScript Runtime"  -->  
<!--[WebFundamentalsPerformanceRenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations "Reduce the Scope and Complexity of Style Calculations"  -->  
<!--[WebFundamentalsPerformanceRenderingSimplifyPaintComplexity]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas "Simplify Paint Complexity and Reduce Paint Areas"  -->  
<!--[WebFundamentalsPerformanceRenderingCompositorOnlyProperties]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count "Stick to Compositor-Only Properties and Manage Layer Count"  -->  

[CssTriggers]: https://csstriggers.com "Gatilhos CSS"  

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Usando web workers | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Lista de verificação de desempenho do tempo de execução - Calendário de desempenho da Web"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) é encontrada aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) e [Meggin Kearney][MegginKearney] \(Tech Writer\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
