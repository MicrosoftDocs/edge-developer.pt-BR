---
title: Analisar o desempenho do tempo de execução
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 0fc576703a9760a3306e74da3521f93bf2d5d9cd
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986175"
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

# Analisar o desempenho do tempo de execução 

Os usuários esperam páginas interativas e suaves.  Cada estágio no pipeline de pixel representa uma oportunidade de introduzir o Jank.  Saiba mais sobre ferramentas e estratégias para identificar e corrigir problemas comuns que desaceleram o desempenho do tempo de execução.  

### Resumo  

*   Não escreva JavaScript que força o navegador a recalcular o layout.  Separar funções de leitura e gravação e fazer leituras primeiro.  
*   Não se complica ao CSS.  Use menos CSS e mantenha seus seletores CSS simples.  
*   Evite o máximo de layout possível.  Escolha CSS que não dispare o layout.  
*   Pintar pode levar mais tempo do que qualquer outra atividade de renderização.  Cuidado com os afunilamentos de tinta.  
    
## JavaScript  

Cálculos de JavaScript, especialmente aqueles que disparam alterações visuais abrangentes, podem paralisar o desempenho do aplicativo.  Não deixe que JavaScript com tempo incorreto ou com execução demorada interfira nas interações do usuário.  

### JavaScript: ferramentas  

Faça uma gravação no painel **desempenho** e procure eventos suspeitosmente longos `Evaluate Script` .  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

para notar um pouco de Jank em seu JavaScript, talvez seja necessário levar a análise para o próximo nível e coletar um perfil de CPU em JavaScript.  Os perfis de CPU mostram onde o tempo de execução é gasto dentro das funções da página.  Saiba como criar perfis de CPU [para acelerar o tempo de execução do JavaScript][DevtoolsRenderingToolsJavascriptRuntime].

### JavaScript: problemas  

A tabela a seguir descreve alguns problemas comuns de JavaScript e possíveis soluções:  

| Problema | Exemplo | Solução |  
|:--- |:--- |:--- |  
| Manipuladores de entrada caros que afetam a resposta ou a animação.  | Toque paralaxe rolagem.  | Permita que o navegador manipule o toque e rola ou associe o ouvinte o mais tarde possível.  Veja [manipuladores de entrada caros na lista de verificação de desempenho de tempo de execução de Paul Lewis][WebPerformanceCalendarRuntimeChecklist].  |  
| O JavaScript com tempo incorreto afeta a resposta, a animação e a carga.  | O usuário rola para a direita após a carga da página, setTimeout/setInterval.  | Otimizar o tempo de execução do JavaScript: usar `requestAnimationFrame` , divulgar a manipulação dom sobre quadros, usar [funcionários da Web][MDNUsingWebWorkers].  |  
| O JavaScript de execução demorada afeta a resposta.  | O [evento DOMContentLoaded][MDNUsingWebWorkers] é interrompido, pois sobrecarregado com o JS funciona.  | Mover o trabalho de computação puro para [funcionários da Web][MDNUsingWebWorkers].  Se precisar de acesso ao DOM, use `requestAnimationFrame` .  <!--See also [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| Scripts de lixo-y que afetam a resposta ou a animação.  | A coleta de lixo pode ocorrer em qualquer lugar.  | Escreva menos scripts de lixo y.  Consulte [coleta de lixo em animação na lista de verificação de desempenho de tempo de execução de Paul Lewis][WebPerformanceCalendarRuntimeChecklist].  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## Estilo  

As alterações de estilo são caras, especialmente se essas alterações afetarem mais de um elemento no DOM.  Sempre que você aplicar estilos a um elemento, o navegador descobre o impacto sobre todos os elementos relacionados, recalcula o layout e redesenha.  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### Estilo: ferramentas  

Faça uma gravação no painel **desempenho** .  Verifique a gravação de `Recalculate Style` eventos grandes \ (exibidos em roxo \).  

<!--todo: add Recording section when available  -->  

Clique em um `Recalculate Style` evento para ver mais informações sobre ele no painel **detalhes** .  Se as alterações de estilo estiverem demorando muito, isso representa um impacto no desempenho.  Se os cálculos de estilo estiverem afetando um grande número de elementos, essa é outra área com espaço para melhorias.  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Estilo de recálculo longo" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   Estilo de recálculo longo  
:::image-end:::  

Para reduzir o impacto de `Recalculate Style` eventos:  

*   Use os [gatilhos CSS][CssTriggers] para saber quais propriedades CSS disparam o layout, o Paint e o composto.  Essas propriedades têm o pior impacto no desempenho da renderização.  
*   Alternar para propriedades que têm menos impacto.  <!--See [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties] for more guidance.  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### Estilo: problemas  

A tabela a seguir descreve alguns problemas comuns de estilo e soluções em potencial:  

| Problema | Exemplo | Solução |  
|:--- |:--- |:--- |  
| Cálculos de estilo caros que afetam a resposta ou a animação.  | Qualquer propriedade CSS que altera a geometria de um elemento, como a largura, a altura ou a posição; o navegador verifica todos os outros elementos e recalcula o layout.  | Evitar CSS que dispara layouts |  
| Seletores complexos que afetam a resposta ou a animação.  | Seletores aninhados forçam o navegador a saber tudo sobre todos os outros elementos, incluindo pais e filhos.  | Faça referência a um elemento em seu CSS com apenas uma classe.  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## Layout  

O layout (ou refluxo no Firefox) é o processo pelo qual o navegador calcula as posições e os tamanhos de todos os elementos em uma página.  O modelo de layout da Web significa que um elemento pode afetar outras pessoas; por exemplo, a largura do `<body>` elemento geralmente afeta as larguras de qualquer elemento filho, e assim por diante, até a árvore.  O processo pode estar bastante envolvido para o navegador.  

Como regra geral, se você solicitar um valor geométrico de volta do DOM antes da conclusão de um quadro, você se encontrará com "layouts síncronos forçados", que podem ser um grande afunilamento de desempenho se repetidos frequentemente ou executados para uma árvore DOM grande.  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### Layout: ferramentas  

O painel **desempenho** identifica quando uma página faz com que os layouts síncronos sejam forçados.  Esses `Layout` eventos são marcados com barras vermelhas.  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Layout síncrono forçado" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   Layout síncrono forçado  
:::image-end:::  

"Layout thrashing" é uma repetição de condições de layout síncrono forçado.  Isso ocorre quando o JavaScript grava e lê do DOM repetidamente, o que força o navegador a recalcular o layout de uma vez.  Para identificar a thrashing de layout, procure por um padrão de vários avisos de layout síncrono forçado.  Veja a imagem anterior.  

### Layout: problemas  

A tabela a seguir descreve alguns problemas comuns de layout e soluções possíveis:  

| Problema | Exemplo | Solução |  
|:--- |:--- |:--- |  
| Layout síncrono forçado que afeta a resposta ou a animação.  | Forçar o navegador a executar o layout anteriormente no pipeline de pixel, resultando em etapas repetidas do processo de renderização.  | Lote o seu estilo lê primeiro e, em seguida, faça gravações.  <!--See also [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| Layout thrashing afetar a resposta ou a animação.  | Um loop que coloca o navegador em um ciclo de leitura-gravação-leitura-gravação, forçando o navegador a recalcular o layout repetidas vezes.  | Operações de leitura/gravação em lotes automaticamente usando a [biblioteca do FastDom][GitHubWilsonpageFastdom].  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## Pintura e composição  

O Paint é o processo de preenchimento em pixels.  Geralmente, é a parte mais dispendiosa do processo de renderização.  Se você observou que sua página está Janky de alguma maneira, é provável que você tenha problemas de pintura.  

Composição é onde as partes pintadas da página são colocadas juntas para exibição na tela.  Para a maioria das propriedades, se você se conectar a somente propriedades do compositor e evitar o Paint, verá uma grande melhoria no desempenho, mas você precisará tomar cuidado com contagens de camadas excessivas.  <!--See also [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### Pintura e composição: ferramentas  

Quer saber quanto tempo de pintura leva ou com que frequência ocorre a pintura?  Marque a configuração [habilitar a instrumentação avançada de pintura][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] no painel **desempenho** e, em seguida, faça uma gravação.  Se a maior parte do seu tempo de renderização for gasta na pintura, você tem problemas de pintura.  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### Pintura e composição: problemas  

A tabela a seguir descreve alguns problemas comuns de pintura e composição e possíveis soluções:  

| Problema | Exemplo | Solução |  
|:--- |:--- |:--- |  
| As tempestades de pintura afetam a resposta ou a animação.  | Grandes áreas de pintura ou pinturas caras que afetam a resposta ou a animação.  | Evite pintar, promover elementos que estão se movendo para sua própria camada, use transformações e opacidade.  <!--See [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| Explosões de camada que afetam animações.  | A promoção de elementos demais com o `translateZ(0)` desempenho da animação é bastante afetado.  | Promover a camadas com moderação e apenas quando você souber que ela oferece melhorias concretas.  <!--See [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## Entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Acelerar o tempo de execução de JavaScript | Documentos da Microsoft"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#enable-advanced-paint-instrumentation "Habilitar a instrumentação avançada de pintura – referência de análise de desempenho | Documentos da Microsoft"

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

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Usar o Web Works | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Lista de verificação de desempenho do tempo de execução-calendário de desempenho da Web"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \) e [Meggin Kearney][MegginKearney] \ (Tech Writer \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
