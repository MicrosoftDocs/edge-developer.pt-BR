---
description: Saiba como avaliar o desempenho do tempo de execução no Microsoft Edge DevTools.
title: Comece a analisar o desempenho do tempo de execução
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 65351f3846ed76ef8a27dbff2cfb08c497282d15
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992943"
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

# Comece a analisar o desempenho do tempo de execução  

> [!NOTE]
> Para saber como fazer as páginas serem carregadas mais rapidamente, consulte [otimizar a velocidade do site][DevtoolsSpeedGetStarted].  

O desempenho do tempo de execução é a forma como a sua página é executada, em oposição ao carregamento.  O artigo do tutorial a seguir ensina a usar o painel de desempenho do Microsoft Edge DevTools para analisar o desempenho do tempo de execução.  Em termos do modelo de **trilho** , as habilidades que você aprende neste tutorial são úteis para analisar a resposta, a animação e as fases ociosas da página.  

<!--todo: add rail link when section is ready -->  

## Introdução  

No tutorial a seguir, abra o DevTools em uma página dinâmica e use o painel **desempenho** para localizar um afunilamento de desempenho na página.  

1.  Abrir o Microsoft Edge no **modo InPrivate**.  O modo InPrivate garante que o Microsoft Edge seja executado em um estado limpo.  Por exemplo, se você tiver muitas extensões instaladas, as extensões poderão criar ruído em medidas de desempenho.  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  Carregue a página a seguir na sua janela InPrivate.  A página é a demonstração na qual você vai criar o perfil.  A página mostra um monte de ícones pequenos em movimento para cima e para baixo.  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  Selecione `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \) para abrir o devtools.  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="A demonstração à esquerda e DevTools à direita" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       A demonstração à esquerda e DevTools à direita  
    :::image-end:::  
    
    > [!NOTE]
    > Para o restante dos números, o DevTools está [desencaixado em uma janela separada][DevtoolsCustomizePlacement] para se concentrar melhor no conteúdo.  
    
### Simular uma CPU móvel  

Dispositivos móveis têm muito menos energia de CPU do que desktops e notebooks.  Sempre que você criar o perfil de uma página, use a limitação de CPU para simular como a sua página é realizada em dispositivos móveis.  

1.  No DevTools, escolha a guia **desempenho** .  
1.  Verifique se a caixa de seleção **capturas de tela** está habilitada.  
1.  Escolha **configurações de captura** \ (! [ Configurações de captura] [ImageCaptureSettingsIcon] \).  DevTools revela configurações relacionadas à maneira como ele captura métricas de desempenho.  
1.  Para **CPU**, selecione **4x lentidão**.  O DevTools acelera a CPU para que seja 4 vezes mais lento do que o normal.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="Acelerador de CPU" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       Acelerador de CPU  
    :::image-end:::  
    
    > [!NOTE]
    > Ao testar outras páginas; Se você quiser garantir que cada página funcione bem em dispositivos móveis low-end, defina a limitação de CPU para **6x a lentidão**.  A demonstração não funciona bem com o 6X de lentidão, portanto, ele simplesmente usa 4 vezes a lentidão para fins de instrução.  
    
### Configurar a demonstração  

É difícil criar uma demonstração de desempenho do tempo de execução que funcione consistentemente para todos os leitores do site.  A seção a seguir permite que você personalize a demonstração para garantir que sua experiência seja relativamente consistente com as capturas de tela e as descrições, independentemente de sua configuração específica.

1.  Escolha o botão **Adicionar 10** até que os ícones azuis sejam movidos visivelmente mais devagar do que antes.  Em um computador high-end, você pode escolher cerca de 20 vezes.  
1.  Escolha **otimizar**.  Os ícones azuis devem se mover de forma mais rápida e mais suave.  
    
    > [!NOTE]
    > Para exibir melhor uma diferença entre as versões otimizadas e não otimizadas, escolha algumas vezes o botão **subtrair 10** e tente novamente.  
    > Se você adicionar muitos ícones azuis, poderá terminar a CPU e, em seguida, poderá não observar uma diferença importante nos resultados das duas versões.  
    
1.  Escolha não **otimizar**.  Os ícones azuis se movem mais lentos e com mais lentidão.  
    
### Desempenho do registro em tempo de execução  

Quando você executou a versão otimizada da página, os ícones azuis são movidos mais rapidamente.  Por quê?  Ambas as versões devem mover os ícones da mesma quantidade de espaço na mesma quantidade de tempo.  Faça uma gravação no painel desempenho para aprender a detectar o afunilamento de desempenho na versão desotimizada.  

1.  No DevTools, escolha **gravar** \ (! [ Record] [ImageRecordIcon] \).  DevTools captura métricas de desempenho à medida que a página é executada.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Criar perfil da página" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       Criar perfil da página  
    :::image-end:::  
    
1.  Aguarde alguns segundos.  
1.  Escolha **parar**.  DevTools interrompe a gravação, processa os dados e, em seguida, exibe os resultados no painel desempenho.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Os resultados do perfil" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       Os resultados do perfil  
    :::image-end:::  
    
Wow, que é um volume impressionante de dados.  Não se preocupe, logo, o processo faz mais sentido.  

## Analisar os resultados  

Depois de registrar o desempenho da página, avalie a qualidade do desempenho da página e encontre as causas.  

### Analisar quadros por segundo  

A principal métrica para medir o desempenho de qualquer animação é a de quadros por segundo \ (FPS \).  Os usuários ficam satisfeitos quando animações são executadas em 60 FPS.  

1.  Examine o gráfico de **FPS** .  Sempre que você vir uma barra vermelha acima de **FPS**, significa que a taxa de quadros ficou tão baixa que provavelmente está prejudicando a experiência do usuário.  Em geral, quanto maior a barra verde, mais alta a FPS.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="O gráfico de FPS" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       O gráfico de **FPS**  
    :::image-end:::  
    
1.  Abaixo do gráfico de **FPS** , você vê o gráfico **da CPU** .  As cores do gráfico de **CPU** correspondem às cores na guia **Resumo** , na parte inferior do painel desempenho.  O fato de que o gráfico de **CPU** está cheio de cores significa que a CPU foi maximizada durante a gravação.  Sempre que você vê a CPU esgotada durante longos períodos, é uma indicação para encontrar formas de fazer menos trabalho.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="A guia Resumo e gráfico da CPU" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       A guia **Resumo** e gráfico **da CPU**  
    :::image-end:::  
    
1.  Passe o mouse sobre os gráficos de **FPS**, **CPU**ou **rede** .  DevTools mostra uma captura de tela da página nesse momento.  Mova o mouse para a esquerda e para a direita para reproduzir a gravação.  A ação é referenciada como scrubbing, e é útil para analisar manualmente a progressão de animações.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Exibir uma captura de tela da página ao lado da marca 2500ms da gravação" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       Exibir uma captura de tela da página ao lado da marca 2500ms da gravação  
    :::image-end:::  
    
1.  Na seção **quadros** , passe o mouse sobre um dos quadrados verdes.  DevTools mostra as FPS para esse quadro específico.  Cada quadro provavelmente está logo abaixo do destino de 60 FPS.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Passe o mouse sobre um quadro" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       Passe o mouse sobre um quadro  
    :::image-end:::  
    
É claro que você verá que a página não está funcionando bem.  Mas, em situações reais, talvez não seja tão claro que ter todas as ferramentas para fazer as medições se torne útil.  

#### Bônus: abrir o medidor de FPS  

Outra ferramenta prática é o medidor de FPS, que fornece estimativas em tempo real para FPS quando a página é executada.  

1.  Selecione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comandos**.  
1.  Comece `Rendering` a digitar no **menu de comando** e selecione **Mostrar renderização**.  
1.  Na guia **renderização** , ative o **medidor de FPS**.  Uma nova sobreposição aparece no canto superior direito do seu visor.  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="O medidor de FPS" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       O **medidor de FPS**  
        :::image-end:::  
    
1.  Desabilite o **medidor de FPS** e selecione `Escape` para fechar a guia **renderização** .  Você não está usando o **metro de FPS** neste tutorial.  
    
### Localizar o afunilamento  

Depois de medir e verificar se a animação não está funcionando bem, a próxima etapa é responder a pergunta "por quê?".  

1.  Quando nenhum evento é selecionado, a guia **Resumo** mostra uma análise da atividade.  A página gastou na maioria do processamento de tempo.  Como o desempenho é a arte de fazer menos trabalho, seu objetivo é reduzir a quantidade de tempo gasto com o trabalho de renderização.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="A guia Resumo" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       A guia **Resumo**  
    :::image-end:::  
    
1.  Expanda a seção **principal** .  DevTools mostra um gráfico de chama de atividade no thread principal ao longo do tempo.  O eixo x representa a gravação ao longo do tempo.  Cada barra representa um evento.  Uma barra mais ampla significa que o evento demorou mais.  O eixo y representa a pilha de chamadas.  Quando você vê eventos empilhados uns sobre os outros, isso significa que os eventos superiores causaram os eventos inferiores.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="A seção principal" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       A seção **principal**  
    :::image-end:::  
    
1.  Há muitos dados na gravação.  Para ampliar um único evento; escolha, segure e arrastou o cursor sobre a **visão geral**, que é a seção que inclui os gráficos de **FPS**, **CPU**e **net** .  A seção **principal** e a guia **Resumo** exibem apenas informações para a parte selecionada da gravação.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Ampliar um evento" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       Ampliar um evento  
    :::image-end:::  
    
    > [!NOTE]
    > Outra maneira de aplicar zoom, focalizar a seção **principal** , escolher o plano de fundo ou um evento e selecionar `W` , `A` , `S` ou `D` .  
    
    1.  Foco no triângulo vermelho no canto superior direito do evento de **quadro de animação acionado** .  Sempre que você vir um triângulo vermelho, é um aviso de que pode haver um problema relacionado ao evento.  
    
    > [!NOTE]
    > O **quadro de animação acionado** pelo evento ocorre sempre que um [ `requestAnimationFrame()` retorno de chamada][MDNWebRequestAnimationFrame] é executado.  
    
1.  Escolha o evento **Framed de animação acionado** .  A guia **Resumo** agora mostra informações sobre esse evento.  Observe o link **revelar** .  Depois de escolher, DevTools para destacar o evento que iniciou o evento **Framed de animação** .  Além disso, concentre-se no link **app.js:95** .  Depois de escolher, a linha relevante no código-fonte será exibida.
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Mais informações sobre o evento Framed de animação acionado" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       Mais informações sobre o evento **Framed de animação acionado**  
    :::image-end:::  
    
    > [!NOTE]
    > Depois de selecionar um evento, use as teclas de direção para selecionar os eventos ao lado dele.  
    
1.  No evento **app. Update** , há vários eventos roxos.  Se cada evento roxo foi mais largo, parece que cada um deles pode ter um triângulo vermelho sobre ele.  
1.  Escolha um dos eventos de **layout** roxo.  O DevTools fornece mais informações sobre o evento na guia **Resumo** .  De fato, há um aviso sobre refluxos forçados \ (outra palavra para layout \).  
    
1.  Na guia **Resumo** , escolha o link **app.js:71** em **layout forçado**.  DevTools leva você até a linha de código que forçou o layout.  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="A linha de código que causou o layout forçado" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       A linha de código que causou o layout forçado  
    :::image-end:::  
    
    > [!NOTE]
    > O problema com o código é que, em cada quadro de animação, ele altera o estilo de cada ícone e, em seguida, consulta a posição de cada ícone na página.  Como os estilos foram alterados, o navegador não sabe se cada posição de ícone foi alterada, portanto, é preciso refazer o layout do ícone para calcular a nova posição.  <!--  > See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->
    
<!-- todo: add layouts section when available -->

Foi muito útil aprender.  Agora você tem uma base sólida no fluxo de trabalho básico para analisar o desempenho do tempo de execução.  Muito bom trabalho.  

### Bônus: analisar a versão otimizada  

Usando os fluxos de trabalho e as ferramentas que você acabou de aprender, escolha **otimizar** na demonstração para habilitar o código otimizado, faça outra gravação de desempenho e, em seguida, analise os resultados.  Na taxa de quadros aprimorada para a redução de eventos no gráfico de chama na seção **principal** , você pode ver que a versão otimizada do aplicativo faz muito menos trabalho, resultando em melhor desempenho.  

> [!NOTE]
> Até mesmo a versão otimizada não é ótima, porque ela manipula a `top` propriedade de cada ícone.  Uma abordagem melhor é aderir às propriedades que afetam somente a composição.  <!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## Próximas etapas

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

Para se familiarizar com o painel de desempenho, a prática torna-se perfeita.  Tente fazer a criação de perfil de suas páginas e analisar os resultados.  Se tiver alguma dúvida sobre seus resultados, use o ícone **enviar comentários** , selecione `Alt` + `Shift` + `I` \ (Windows \), selecione `Option` + `Shift` + `I` \ (MacOS \) ou [tweet The devtools Team][TwitterEdgeDevtools].  Inclua capturas de tela ou links para páginas reproduzíveis, se possível.  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="O ícone * * feedback * * na Microsoft Edge DevTools" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   O ícone **enviar comentários** no Microsoft Edge devtools  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

Por último, há muitas maneiras de melhorar o desempenho do tempo de execução.  Este artigo se concentrou em um afunilamento de animação específico para dar a você um tour focalizado pelo painel desempenho, mas é apenas um dos muitos afunilamentos que você pode encontrar.  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Alterar o posicionamento do Microsoft Edge DevTools (desencaixar, encaixar na parte inferior, encaixar à esquerda)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Otimizar a velocidade do site com o Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools-postar um tweet | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window. requestAnimationFrame \ (\) | MDN"  

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
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
