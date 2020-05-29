---
title: Comece a analisar o desempenho do tempo de execução
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: bff2d2fb0ff8424303289183ca8c5935ef477381
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611738"
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
> Consulte [otimizar a velocidade do site][DevtoolsSpeedGetStarted] para aprender a fazer com que suas páginas sejam carregadas mais rapidamente.  

O desempenho do tempo de execução é a forma como a sua página é executada, em oposição ao carregamento.  Este tutorial ensina a usar o painel de desempenho do Microsoft Edge DevTools para analisar o desempenho do tempo de execução.  Em termos do modelo de **trilho** , as habilidades que você aprende neste tutorial são úteis para analisar a resposta, a animação e as fases ociosas da página.  

<!--todo: add rail link when section is ready -->  

## Introdução   

Neste tutorial, você abre o DevTools em uma página dinâmica e usa o painel desempenho para localizar um afunilamento de desempenho na página.  

1.  Abrir o Microsoft Edge no **modo InPrivate**.  O modo InPrivate garante que o Microsoft Edge seja executado em um estado limpo.  Por exemplo, se você tiver muitas extensões instaladas, essas extensões poderão criar ruído em medidas de desempenho.  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  Carregue a página a seguir na sua janela InPrivate.  Esta é a demonstração na qual você pretende fazer o perfil.  A página mostra um monte de ícones pequenos em movimento para cima e para baixo.  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/jank/
    ```  
    
1.  Pressione `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \) para abrir o devtools.  
    
    > ###### Figura 1  
    > A demonstração à esquerda e DevTools à direita  
    > ![A demonstração à esquerda e DevTools à direita][ImageGetStarted]  
    
    > [!NOTE]
    > Para o restante das capturas de tela, o DevTools é [desencaixado em uma janela separada][DevtoolsCustomizePlacement] para que você possa ver o conteúdo melhor.  
    
### Simular uma CPU móvel  

Dispositivos móveis têm muito menos energia de CPU do que desktops e notebooks.  Sempre que você criar o perfil de uma página, use a limitação de CPU para simular como a sua página é realizada em dispositivos móveis.  

1.  No DevTools, clique na guia **desempenho** .  
1.  Verifique se a caixa de seleção **capturas de tela** está habilitada.  
1.  Clique em capturar configurações de captura de **configurações** ![ ][ImageCaptureSettingsIcon] .  DevTools revela configurações relacionadas à maneira como ele captura métricas de desempenho.  
1.  Para **CPU**, selecione **4x lentidão**.  O DevTools acelera a CPU para que seja 4 vezes mais lento do que o normal.  
    
    > ###### Figura 2  
    > Aceleração da CPU  
    > ![Aceleração da CPU][ImageCPUThrottling]  
    
    > [!NOTE]
    > Ao testar outras páginas, se você quiser garantir que elas funcionem bem em dispositivos móveis low-end, defina a limitação de CPU para **6x a lentidão**.  Esta demonstração não funciona bem com 6X de lentidão, portanto, ele simplesmente usa 4 vezes de lentidão para fins de instrução.  
    
### Configurar a demonstração  

É difícil criar uma demonstração de desempenho do tempo de execução que funcione consistentemente para todos os leitores deste site.  Esta seção permite que você personalize a demonstração para garantir que sua experiência seja relativamente consistente com as capturas de tela e descrições que você vê neste tutorial, independentemente de sua configuração específica.

1.  Continue clicando em **Adicionar 10** até que os ícones azuis se movimentem visivelmente mais devagar do que antes.  Em um computador high-end, pode demorar cerca de 20 cliques.  
1.  Clique em **otimizar**.  Os ícones azuis devem se mover de forma mais rápida e mais suave.  

    > [!NOTE]
    > Se você não vir uma diferença perceptível entre as versões otimizadas e não otimizadas, tente clicar em **subtrair 10** algumas vezes e tentar novamente.  
    > Se você adicionar muitos ícones azuis, terá apenas a versão máxima da CPU e não verá uma diferença importante nos resultados das duas versões (em inglês).  

1.  Clique em **desfazer**.  Os ícones azuis se movem mais lentos e com mais Jank.  

### Desempenho do registro em tempo de execução   

Quando você executou a versão otimizada da página, os ícones azuis são movidos mais rapidamente.  
Por quê?  Ambas as versões devem mover os ícones da mesma quantidade de espaço na mesma quantidade de tempo.  Faça uma gravação no painel desempenho para aprender a detectar o afunilamento de desempenho na versão desotimizada.  

1.  No DevTools, clique em **gravar** ![ registro ][ImageRecordIcon] .  
    DevTools captura métricas de desempenho à medida que a página é executada.  
    
    > ###### Figura 3 
    > Criando o perfil da página  
    > ![Criando o perfil da página][ImagePageProfiling]  
    
1.  Aguarde alguns segundos.  
1.  Clique em **parar**.  DevTools interrompe a gravação, processa os dados e, em seguida, exibe os resultados no painel desempenho.  
    
    > ###### Figura 4  
    > Os resultados do perfil  
    > ![Os resultados do perfil][ImageProfileResults]  

Wow, que é um volume impressionante de dados.  Não se preocupe, tudo fará mais sentido em breve.  

## Analisar os resultados   

Depois de registrar o desempenho da página, você pode medir o desempenho da página e encontrar as causas possíveis e encontrar as causas mais lentas.  

### Analisar quadros por segundo  

A principal métrica para medir o desempenho de qualquer animação é a de quadros por segundo \ (FPS \).  Os usuários ficam satisfeitos quando animações são executadas em 60 FPS.  

1.  Examine o gráfico de **FPS** .  Sempre que você vir uma barra vermelha acima de **FPS**, significa que a taxa de quadros ficou tão baixa que provavelmente está prejudicando a experiência do usuário.  Em geral, quanto maior a barra verde, mais alta a FPS.  
    
    > ###### Figura 5  
    > O gráfico de FPS  
    > ![O gráfico de FPS][ImageFPSChart]  

1.  Abaixo do gráfico de **FPS** , você vê o gráfico **da CPU** .  As cores do gráfico de **CPU** correspondem às cores na guia **Resumo** , na parte inferior do painel desempenho.  O fato de que o gráfico de **CPU** está cheio de cores significa que a CPU foi maximizada durante a gravação.  Sempre que você vê a CPU esgotada durante longos períodos, é uma indicação para encontrar formas de fazer menos trabalho.  
    
    > ###### Figura 6  
    > A guia Resumo e gráfico da CPU  
    > ![A guia Resumo e gráfico da CPU][ImageCPUSummary]  

1.  Passe o mouse sobre os gráficos de **FPS**, **CPU**ou **rede** .  DevTools mostra uma captura de tela da página nesse momento.  Mova o mouse para a esquerda e para a direita para reproduzir a gravação.  Isso é chamado de depuração, e é útil para analisar manualmente a progressão de animações.  
    
    > ###### Figura 7  
    > Exibir uma captura de tela da página ao lado da marca 2500ms da gravação  
    > ![Exibir uma captura de tela da página ao lado da marca 2500ms da gravação][ImageViewingScreenshot]  

1.  Na seção **quadros** , passe o mouse sobre um dos quadrados verdes.  DevTools mostra as FPS para esse quadro específico.  Cada quadro provavelmente está logo abaixo do destino de 60 FPS.  
    
    > ###### Figura 8  
    > Passar o mouse sobre um quadro  
    > ![Passar o mouse sobre um quadro][ImageFrameHover]  

Claro que, com esta demonstração, é muito óbvio que a página não está funcionando bem.  Mas, em situações reais, talvez não seja tão claro que ter todas essas ferramentas para fazer com que as medições se tornem úteis.  

#### Bônus: abrir o medidor de FPS  

Outra ferramenta prática é o medidor de FPS, que fornece estimativas em tempo real para FPS quando a página é executada.  

1.  Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comandos.  
1.  Comece `Rendering` a digitar no menu de comando e selecione **Mostrar renderização**.  
1.  Na guia **renderização** , ative o **medidor de FPS**.  Uma nova sobreposição aparece no canto superior direito do seu visor.  
    
    > ###### Figura 9  
    > O medidor de FPS  
    > ![O medidor de FPS][ImageFPSMeter]  

1.  Desative o **medidor de FPS** e pressione `Escape` para fechar a guia **renderização** .  Você não o usará neste tutorial.  

### Localizar o afunilamento  

Agora que você já mediu e verificou que a animação não está funcionando bem, a próxima pergunta a ser respondida é: por quê?  

1.  Observe a guia Resumo.  Quando nenhum evento é selecionado, essa guia mostra uma análise da atividade.  A página gastou na maior parte da renderização de tempo.  Como o desempenho é a arte de fazer menos trabalho, seu objetivo é reduzir a quantidade de tempo gasto com o trabalho de renderização.  
    
    > ###### Figura 10  
    > A guia Resumo  
    > ![A guia Resumo][ImageSummaryTab]  

1.  Expanda a seção **principal** .  DevTools mostra um gráfico de chama de atividade no thread principal ao longo do tempo.  O eixo x representa a gravação ao longo do tempo.  Cada barra representa um evento.  Uma barra mais ampla significa que o evento demorou mais.  O eixo y representa a pilha de chamadas.  Quando você vê eventos empilhados uns sobre os outros, isso significa que os eventos superiores causaram os eventos inferiores.  
    
    > ##### Figura 11  
    > A seção principal  
    > ![A seção principal][ImageMainSection]  

1.  Há muitos dados na gravação.  Amplie um único evento clicando, mantendo e arrastando o mouse sobre a **visão geral**, que inclui a seção que inclui os gráficos de **FPS**, **CPU**e **net** .  A seção **principal** e a guia **Resumo** exibem apenas informações para a parte selecionada da gravação.  
    
    > ###### Figura 12  
    > Ampliado em um único evento  
    > ![Ampliado em um evento][ImageZoomedAnimation]  
    
    > [!NOTE]
    > Outra maneira de ampliar é focalizar a seção **principal** clicando em seu plano de fundo ou selecionando um evento e, em seguida, pressione as `W` teclas,, `A` `S` e `D` .  
    
    1.  Observe o triângulo vermelho no canto superior direito do evento do **quadro de animação acionado** .  Sempre que você vir um triângulo vermelho, é um aviso de que pode haver um problema relacionado a esse evento.  
    
    > [!NOTE]
    > O **quadro de animação acionado** pelo evento ocorre sempre que um [ `requestAnimationFrame()` retorno de chamada][MDNWebRequestAnimationFrame] é executado.  
    
1.  Clique no evento **frame de animação acionado** .  A guia **Resumo** agora mostra informações sobre esse evento.  Observe o link **revelar** .  Clicar em isso faz com que o DevTools realce o evento que iniciou o evento **Framed de animação** .  Observe também o link **app. js: 95** .  Clicar nelas vai para a linha relevante no código-fonte.
    
    > ##### Figura 13  
    > Mais informações sobre o evento Framed de animação acionado  
    > ![Mais informações sobre o evento Framed de animação acionado][ImageAnimationFrameFired]  
    
    > [!NOTE]
    > Depois de selecionar um evento, use as teclas de direção para selecionar os eventos ao lado dele.  

1.  No evento **app. Update** , há vários eventos roxos.  Se fosse mais largo, parece que cada um deles pode ter um triângulo vermelho.  Clique em um dos eventos de **layout** roxo agora.  O DevTools fornece mais informações sobre o evento na guia **Resumo** .  De fato, há um aviso sobre refluxos forçados \ (outra palavra para layout \).  

1.  Na guia **Resumo** , clique no **aplicativo App. js: 71** um link em **layout forçado**.  DevTools leva você até a linha de código que forçou o layout.  
    
    > ##### Figura 14  
    > A linha de código que causou o layout forçado  
    > ![A linha de código que causou o layout forçado][ImageForcedLayoutSRC]  
    
    > [!NOTE]
    > O problema com esse código é que, em cada quadro de animação, ele altera o estilo de cada ícone e, em seguida, consulta a posição de cada ícone na página.  Como os estilos foram alterados, o navegador não sabe se cada posição de ícone foi alterada, portanto, é preciso refazer o layout do ícone para calcular sua posição.  <!--  See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->

<!-- todo: add layouts section when available -->

Phew!  Isso foi muito demorado, mas agora você tem uma base sólida no fluxo de trabalho básico para analisar o desempenho do tempo de execução.  Muito bom trabalho.  

### Bônus: analisar a versão otimizada  

Usando os fluxos de trabalho e as ferramentas que você acabou de aprender, clique em **otimizar** na demonstração para habilitar o código otimizado, faça outra gravação de desempenho e, em seguida, analise os resultados.  Na taxa de quadros aprimorada para a redução de eventos no gráfico de chama na seção **principal** , você pode ver que a versão otimizada do aplicativo faz muito menos trabalho, resultando em melhor desempenho.  

> [!NOTE]
> Mesmo essa versão "otimizada" não é tão ótima, porque ela ainda manipula a `top` propriedade de cada ícone.  Uma abordagem melhor é aderir às propriedades que afetam somente a composição.  
<!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## Próximas etapas

<!--The foundation for understanding performance is the RAIL model.  This model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

Para se familiarizar com o painel de desempenho, a prática torna-se perfeita.  Tente fazer a criação de perfil de suas próprias páginas e analisar os resultados.  Se tiver alguma dúvida sobre seus resultados, use o ícone de **comentários** , pressione `Alt`  +  `Shift`  +  `I` no Windows ( `Option`  +  `Shift`  +  `I` no MacOS) ou [tweet em nós][TwitterEdgeDevtools].  Inclua capturas de tela ou links para páginas reproduzíveis, se possível.

> ##### Figura 15
> O ícone de **comentários** no Microsoft Edge devtools  
> ![O ícone * * feedback * * na Microsoft Edge DevTools][ImageFeedbackIcon]

<!-- To really master runtime performance, you've got to learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

Por último, há muitas maneiras de melhorar o desempenho do tempo de execução.  Este tutorial se concentrou em um afunilamento de animação específico para dar a você um tour focalizado pelo painel desempenho, mas é apenas um dos muitos afunilamentos que você pode encontrar.  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  

[ImageGetStarted]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-get-started-side-by-side.msft.png "Figura 1: a demonstração à esquerda e DevTools à direita"  
[ImageCPUThrottling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings.msft.png "Figura 2: limitação da CPU"  
[ImagePageProfiling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-profiling.msft.png "Figura 3: criando o perfil da página"  
[ImageProfileResults]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-results.msft.png "Figura 4: resultados do perfil"  
[ImageFPSChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-chart.msft.png "Figura 5: o gráfico de FPS"  
[ImageCPUSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-cpu-chart.msft.png "Figura 6: a guia Resumo e gráfico da CPU, organizada em azul"  
[ImageViewingScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshot-hover.msft.png "Figura 7: exibindo uma captura de tela da página ao lado da marca 2500ms da gravação"  
[ImageFrameHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frame-hover.msft.png "Figura 8: passando o mouse sobre um quadro"  
[ImageFPSMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-fps-meter-overlay.msft.png "Figura 9: o medidor de FPS"  
[ImageSummaryTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-tab.msft.png "Figura 10: a guia Resumo"  
[ImageMainSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main.msft.png "Figura 11: seção principal"  
[ImageZoomedAnimation]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Figura 12: ampliada em um único quadro de animação evento acionado"  
[ImageAnimationFrameFired]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-animation-frame-fired.msft.png "Figura 13: mais informações sobre o evento Framed de animação acionado"  
[ImageForcedLayoutSRC]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-sources-app-update.msft.png "Figura 14: a linha de código que causou o layout forçado"  
[ImageFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-feedback-icon.msft.png "Figura 15: o ícone * * feedback * * na Microsoft Edge DevTools"

<!-- links -->

[DevtoolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Alterar o posicionamento do Microsoft Edge DevTools (desencaixar, encaixar na parte inferior, encaixar à esquerda)"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Otimizar a velocidade do site com o Microsoft Edge DevTools"  

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
