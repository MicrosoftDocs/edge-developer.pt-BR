---
description: Saiba como avaliar o desempenho do tempo de execução Microsoft Edge DevTools.
title: Começar a analisar o desempenho do Tempo de Execução
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f40f23c4ac9fcc0bb0186ddb96956f691890c0c0
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564270"
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
# <a name="get-started-with-analyzing-runtime-performance"></a>Começar a analisar o desempenho do Tempo de Execução  

> [!NOTE]
> Para saber como fazer suas páginas carregarem mais rapidamente, navegue até [Otimizar a Velocidade do Site.][DevtoolsSpeedGetStarted]  

O desempenho do tempo de execução é o desempenho da sua página durante a execução, em vez de carregar.  O artigo do tutorial a seguir ensina como usar o painel Microsoft Edge Desempenho do DevTools para analisar o desempenho do tempo de execução.  Em termos do modelo **RAIL,** as habilidades que você aprender neste tutorial são úteis para analisar as fases resposta, animação e ociosidade da sua página.  

<!--todo: add rail link when section is ready -->  

## <a name="get-started"></a>Introdução  

No tutorial a seguir, você abre o DevTools em uma página ao vivo e usa o painel Desempenho para encontrar um a gargalo de desempenho na página. ****  

1.  Abra Microsoft Edge no **modo InPrivate**.  O Modo InPrivate garante que Microsoft Edge seja executado em um estado limpo.  Por exemplo, se você tiver muitas extensões instaladas, as extensões poderão criar ruído em suas medidas de desempenho.  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  Carregue a página a seguir na janela InPrivate.  A página é a demonstração que você vai perfilar.  A página mostra um monte de pequenos ícones movendo para cima e para baixo.  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  Selecione `Control` + `Shift` + `I` \(Windows, Linux\) `Command` + `Option` + `I` ou \(macOS\) para abrir o DevTools.  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="A demonstração à esquerda e o DevTools à direita" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       A demonstração à esquerda e o DevTools à direita  
    :::image-end:::  
    
    > [!NOTE]
    > Para o restante dos números, o DevTools é desfazido para uma janela [separada][DevtoolsCustomizePlacement] para se concentrar melhor no conteúdo.  
    
### <a name="simulate-a-mobile-cpu"></a>Simular uma CPU móvel  

Os dispositivos móveis têm muito menos energia da CPU do que desktops e laptops.  Sempre que você perfilar uma página, use a Throttling da CPU para simular o desempenho da sua página em dispositivos móveis.  

1.  No DevTools, escolha a **ferramenta Performance.**  
1.  Certifique-se de escolher a caixa de seleção ao lado **de Capturas de Tela**.  
1.  Escolha **Capturar Configurações** \( Capture Configurações ![ ](../media/capture-settings-icon.msft.png) \).  O DevTools revela configurações relacionadas à forma como captura métricas de desempenho.  
1.  Para **CPU,** escolha **4x de lentidão**.  O DevTools acelera sua CPU para que ela seja 4 vezes mais lenta do que o normal.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="Aceleração da CPU" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       Aceleração da CPU  
    :::image-end:::  
    
    > [!NOTE]
    > Ao testar outras páginas; se você quiser garantir que cada página funcione bem em dispositivos móveis de baixo nível, de definir a velocidade da CPU como **6x de lentidão**.  A demonstração não funciona bem com a lentidão de 6x, portanto, ela usa apenas 4x de lentidão para fins instrucionais.  
    
### <a name="set-up-the-demo"></a>Configurar a demonstração  

É difícil criar uma demonstração de desempenho de tempo de execução que funcione de forma consistente para todos os leitores do site.  A seção a seguir permite personalizar a demonstração para garantir que sua experiência seja relativamente consistente com as capturas de tela e as descrições, independentemente da configuração específica.

1.  Escolha o **botão Adicionar 10** até que os ícones azuis se movam visivelmente mais lentos do que antes.  Em um computador high-end, você pode escolher isso cerca de 20 vezes.  
1.  Escolha **Otimizar**.  Os ícones azuis devem ser mais rápidos e suaves.  
    
    > [!NOTE]
    > Para exibir melhor uma diferença entre as versões otimizadas e não otimizadas, escolha o botão **Subtrair 10** algumas vezes e tente novamente.  
    > Se você adicionar muitos ícones azuis, poderá aumentar a CPU e, em seguida, não observar uma grande diferença nos resultados das duas versões.  
    
1.  Escolha **Não Otimizar**.  Os ícones azuis são mais lentos e com mais lentidão novamente.  
    
### <a name="record-runtime-performance"></a>Registrar o desempenho do tempo de execução  

Quando você correu a versão otimizada da página, os ícones azuis são mais rápidos.  Por que isso?  Ambas as versões devem mover os ícones da mesma quantidade de espaço no mesmo período de tempo.  Leve uma gravação no painel Desempenho para saber como detectar o a gargalo de desempenho na versão não otimizada.  

1.  Em DevTools, escolha **Gravar** \( ![ Record ](../media/record-icon.msft.png) \).  O DevTools captura métricas de desempenho à medida que a página é executado.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Perfil da página" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       Perfil da página  
    :::image-end:::  
    
1.  Aguarde alguns segundos.  
1.  Escolha **Parar**.  O DevTools interrompe a gravação, processa os dados e exibe os resultados no painel Desempenho.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Os resultados do perfil" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       Os resultados do perfil  
    :::image-end:::  
    
Uau, isso é uma quantidade avassaladora de dados.  não se preocupe, em breve o processo faz mais sentido.  

## <a name="analyze-the-results"></a>Analisar os resultados  

Depois de registrar o desempenho da página, mede a qualidade do desempenho da página e encontre as causas.  

### <a name="analyze-frames-per-second"></a>Analisar quadros por segundo  

A métrica principal para medir o desempenho de qualquer animação são quadros por segundo \(FPS\).  Os usuários ficam felizes quando as animações são executados em 60 FPS.  

1.  Revise o **gráfico FPS.**  Sempre que uma barra vermelha é exibida acima **do FPS**, isso significa que a taxa de quadros caiu tão baixo que provavelmente está prejudicando a experiência do usuário.  Em geral, quanto maior for a barra verde, maior será o FPS.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="O gráfico FPS" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       O **gráfico FPS**  
    :::image-end:::  
    
1.  Abaixo do **gráfico FPS,** o **gráfico de CPU** é exibido.  As cores no **gráfico da CPU** correspondem às cores no painel **Resumo,** na parte inferior do painel Desempenho.  O fato de que o **gráfico da CPU** está cheio de cores significa que a CPU foi maxed para fora durante a gravação.  Sempre que a CPU tiver um tempo máximo máximo por longos períodos, é um indicador de que você deve encontrar maneiras de fazer menos trabalho.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="O gráfico da CPU e o painel Resumo" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       O **gráfico da CPU** e o painel **Resumo**  
    :::image-end:::  
    
1.  Passe o mouse nos **gráficos FPS,** **CPU**ou **NET.**  DevTools mostra uma captura de tela da página nesse ponto no tempo.  Mova o mouse para a esquerda e para a direita para repetir a gravação.  A ação é referenciada como limpeza e é útil para analisar manualmente a progressão das animações.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Exibir uma captura de tela da página em torno da marca de 2500ms da gravação" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       Exibir uma captura de tela da página em torno da marca de 2500ms da gravação  
    :::image-end:::  
    
1.  Na seção **Quadros,** passe o mouse em um dos quadrados verdes.  DevTools mostra o FPS para esse quadro específico.  Cada quadro provavelmente está bem abaixo do destino de 60 FPS.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Passar o mouse em um quadro" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       Passar o mouse em um quadro  
    :::image-end:::  
    
Obviamente, a exibição indica que a página da Web não está com bom desempenho.  Mas, em cenários reais, pode não ser tão claro, portanto, ter todas as ferramentas para fazer medições é útil.  

#### <a name="bonus-open-the-fps-meter"></a>Bônus: Abra o medidor FPS  

Outra ferramenta útil é o medidor FPS, que fornece estimativas em tempo real para FPS à medida que a página é executado.  

1.  Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\) para abrir o **Menu de Comando**.  
1.  Comece a digitar `Rendering` no Menu de Comando **e** escolha **Mostrar Renderização**.  
1.  Na ferramenta **Renderização,** a turn on **FPS Meter**.  Uma nova sobreposição aparece na parte superior direita do seu viewport.  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="O medidor FPS" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       O **medidor FPS**  
        :::image-end:::  
    
1.  Desligue o **Medidor de FPS e** selecione para fechar a ferramenta `Escape` **Rendering.**  Você não está usando **o Medidor FPS** neste tutorial.  
    
### <a name="find-the-bottleneck"></a>Encontre o a gargalo  

Depois de medir e verificar se a animação não está bem, a próxima etapa é responder à pergunta "por quê?".  

1.  Quando nenhum evento é escolhido, o painel **Resumo** mostra uma divisão de atividades.  A página passou a maior parte do tempo renderização.  Como o desempenho é a arte de fazer menos trabalho, seu objetivo é reduzir o tempo gasto fazendo trabalho de renderização.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="O painel Resumo" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       O **painel Resumo**  
    :::image-end:::  
    
1.  Expanda **a seção** Principal.  DevTools mostra um gráfico de chama de atividade no thread principal, com o tempo.  O eixo x representa a gravação, com o passar do tempo.  Cada barra representa um evento.  Uma barra mais ampla significa que o evento demorou mais.  O eixo y representa a pilha de chamada.  Quando os eventos são empilhados uns sobre os outros, isso significa que os eventos superiores causaram os eventos inferiores.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="A seção Principal" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       A **seção** Principal  
    :::image-end:::  
    
1.  Há muitos dados na gravação.  Para ampliar em um único evento; escolha, segure e arraste o cursor sobre a Visão Geral **,** que é a seção que inclui os gráficos **FPS,** **CPU**e **NET.**  A **seção Principal** e **o** painel Resumo exibem apenas informações para a parte escolhida da gravação.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Ampliar em um evento" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       Ampliar em um evento  
    :::image-end:::  
    
    > [!NOTE]
    > Outra maneira de ampliar, focalizar a **seção Principal,** escolher o plano de fundo ou um evento e `W` selecionar , , ou `A` `S` `D` .  
    
    1.  Concentre-se no triângulo vermelho no canto superior direito do **evento Animation Frame Fired.**  Sempre que um triângulo vermelho é exibido, é um aviso de que pode haver um problema relacionado ao evento.  
    
    > [!NOTE]
    > O **evento Animation Frame Fired** ocorre sempre que um retorno de chamada [requestAnimationFrame()][MDNWebRequestAnimationFrame] é executado.  
    
1.  Escolha o **evento Animation Frame Fired.**  O **painel** Resumo agora mostra informações sobre esse evento.  Observe o link **Revelação.**  Depois de escolher, DevTools realça o evento que iniciou o **evento Animation Frame Fired.**  Além disso, concentre-se **no linkapp.js:95.**  Depois de escolher, a linha relevante no código-fonte será exibida.
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Mais informações sobre o evento Animation Frame Fired" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       Mais informações sobre o evento **Animation Frame Fired**  
    :::image-end:::  
    
    > [!NOTE]
    > Depois de escolher um evento, use as teclas de seta para selecionar os eventos ao lado dele.  
    
1.  No evento **app.update,** há um monte de eventos roxos.  Se cada evento roxo era mais amplo, parece que cada um deles pode ter um triângulo vermelho nele.  
1.  Escolha um dos eventos **layout roxo.**  O DevTools fornece mais informações sobre o evento no painel **Resumo.**  Na verdade, há um aviso sobre refluxos forçados \(outra palavra para layout\).  
    
1.  No painel **Resumo,** escolha o link **app.js:71** em **Layout Forçado.**  DevTools leva você para a linha de código que força o layout.  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="A linha de código que causou o layout forçado" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       A linha de código que causou o layout forçado  
    :::image-end:::  
    
    > [!NOTE]
    > O problema com o código é que, em cada quadro de animação, ele altera o estilo de cada ícone e consulta a posição de cada ícone na página.  Como os estilos foram alterados, o navegador não sabe se cada posição de ícone foi alterada, portanto, ele precisa reposicioná-lo para calcular a nova posição.  <!--  > To learn more, navigate to [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts].  -->
    
<!-- todo: add layouts section when available -->

Isso foi muito para aprender.  Agora você tem uma base sólida no fluxo de trabalho básico para analisar o desempenho do tempo de execução.  Muito bom trabalho.  

### <a name="bonus-analyze-the-optimized-version"></a>Bônus: Analisar a versão otimizada  

Usando os fluxos de trabalho e as ferramentas que você acabou de aprender, escolha **Otimizar** na demonstração para ativar o código otimizado, fazer outra gravação de desempenho e analisar os resultados.  Da taxa de quadros aprimorada até a redução de eventos no gráfico de chama na seção **Principal,** a versão otimizada do aplicativo faz muito menos trabalho, resultando em melhor desempenho.  

> [!NOTE]
> Mesmo a versão otimizada não é ótima, pois manipula a `top` propriedade de cada ícone.  Uma abordagem melhor é manter as propriedades que afetam apenas a composição.  <!--  > For more information, navigate to [Use transform and opacity changes for animations][RenderingCompositor].  -->  

<!--todo: add rendering section when available -->

## <a name="next-steps"></a>Próximas etapas

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
To learn more, navigate to [Measure Performance With The RAIL Model][RAIL].  -->  

Para ficar mais confortável com a **ferramenta Performance,** a prática torna perfeito.  Tente perfilar suas páginas e analisar os resultados.  Se você tiver alguma dúvida sobre seus resultados, use o ícone Enviar **Comentários,** selecione `Alt` + `Shift` + `I` \(Windows, Linux\), selecione `Option` + `Shift` + `I` \(macOS\) ou tweet a equipe [DevTools][TwitterEdgeDevtools].  Inclua capturas de tela ou links para páginas reprodutíveis, se possível.  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="O ícone **Feedback** no Microsoft Edge DevTools" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   O **ícone Enviar Comentários** no Microsoft Edge DevTools  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

Por fim, há muitas maneiras de melhorar o desempenho do tempo de execução.  Este artigo se concentrou em um a gargalo de animação específico para dar a você um tour focado pelo painel Desempenho, mas é apenas um dos muitos gargalos que você pode encontrar.  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Alterar Microsoft Edge posicionamento do DevTools (Desfazer, Encaixar na Parte Inferior, Doca para a Esquerda)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Otimizar a velocidade do site com Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools - Postar um tweet | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window.requestAnimationFrame\(\) | MDN"  

<!--[InPrivate]: https://support.microsoft.com/help/4026200/microsoft-edge-browse-inprivate "Browse InPrivate in Microsoft Edge"  -->

<!--[FrameAnatomy]: https://aerotwist.com/blog/the-anatomy-of-a-frame  -->  

<!--[RAIL]: /web/fundamentals/performance/rail  -->  
<!--[RenderingAvoidSynchronousLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing#avoid_forced_synchronous_layouts  -->  
<!--[RenderingAvoidThrashing]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing  -->  
<!--[RenderingCompositor]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count#use_transform_and_opacity_changes_for_animations  -->  
<!--[RenderingDebounceInputs]: /web/fundamentals/performance/rendering/debounce-your-input-handlers  -->
<!--[RenderingManageLayers]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count  -->  
<!--[RenderingOptimizeJS]: /web/fundamentals/performance/rendering/optimize-javascript-execution  -->  
<!--[RenderingPerformance]: /web/fundamentals/performance/rendering  -->  
<!--[RenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations  -->  
<!--[RenderingSimplifyPaint]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas  -->  

<!--[StackOverflowAlphabetBrowserDevtools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser - Stack Overflow"  -->  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
