---
description: Recursos de depuração de grade CSS, solicitações de Edição e Repetição com o Console de Rede e muito mais.
title: Novidades no DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 5bd013fae617e9759aa91949acccf936d85f7160
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514358"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-85"></a>Novidades no DevTools (Microsoft Edge 85)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Comunicados da equipe do Microsoft Edge DevTools  

As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools.  Confira os comunicados para experimentar novos recursos no DevTools, no Microsoft Visual Studio Code e muito mais.  Para ficar atualizado sobre todos os recursos mais recentes e maiores em suas ferramentas de desenvolvedor, baixe os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] e siga a equipe do Microsoft [Edge DevTools no Twitter][EdgeDevToolsTwitterAccount].  

### <a name="css-grid-debugging-features"></a>Recursos de depuração de grade CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

A equipe do Microsoft Edge DevTools está colaborando com a equipe do Chrome DevTools e com a comunidade do Chromium para adicionar novos recursos de depuração de grade CSS ao DevTools.  Agora você pode exibir números de linha de grade, lacunas de grade e linhas de grade estendidas como uma sobreposição na página.  Além disso, mais melhorias nas ferramentas de grade estão chegando em breve.  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Recursos de depuração de grade CSS" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   Recursos de depuração de grade CSS
:::image-end:::  

> [!NOTE]
> Para habilitar o experimento, navegue até Ativar recursos [experimentais][DevtoolsExperimentalFeaturesTurnOn] e selecione a caixa de seleção ao lado de Habilitar novos recursos **de depuração de GRADE CSS.**  
> 
> Para experimentar o experimento com um exemplo, navegue até [CSS Grid planner example][CodepenRachelweilYzwBzKM].  

Problema do Chromium [#1047356][CR1047356]  

### <a name="edit-and-replay-requests-with-the-network-console"></a>Editar e repetir solicitações com o Console de Rede  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

Agora você pode usar **Editar e Repetir** solicitações no Log de [Rede][DevtoolsNetworkIndexLogActivity] usando o Console **de Rede.**  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Editar e repetir uma solicitação no NetworkLog com o Console de Rede" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   Editar e repetir uma solicitação no [NetworkLog][DevtoolsNetworkIndexLogActivity] com o **Console de Rede**  
:::image-end:::  

Um novo painel, o **Console de Rede** é aberto na Gaveta de [DevTools][DevtoolsCustomizeIndexDrawer] e preenche automaticamente com informações para a solicitação HTTP.  Para exibir a resposta retornada do servidor, edite a solicitação \(se necessário\) e selecione **Enviar**.  

Você também pode usar o **Console de Rede** para criar e enviar solicitações HTTP diretamente do DevTools.  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="O painel Console de Rede" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   O **painel Console de** Rede  
:::image-end:::  

> [!TIP]
> Para exibir **o Console de Rede** no painel principal \(top\) em vez da Gaveta de [DevTools,][DevtoolsCustomizeIndexDrawer]navegue até mover ferramentas [entre painéis](#move-tools-between-panels).  

> [!NOTE]
> Para habilitar o experimento, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOn] e escolha a caixa de seleção ao lado de **Habilitar Console de Rede**.  
> 
> Abra o [Log de Rede,][DevtoolsNetworkIndexLogActivity]abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Editar e Repetir**.  

Problema do Chromium [#1093687][CR1093687]  

### <a name="service-worker-respondwith-events-in-the-timing-tab"></a>O trabalhador do serviço respondeCom eventos na guia Timing  

A **guia** Timing da **ferramenta Rede** agora inclui eventos de trabalho de `respondWith` serviço.  O evento do trabalhador do serviço mostra a duração do tempo imediatamente antes do manipulador de eventos do trabalhador do serviço começar a ser executado até o momento em que a promessa do `respondWith` `fetch` manipulador é `respondWith` `fetch` resolvida.  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="O evento respondWith service worker na guia Timing do painel Rede" lightbox="../../media/2020/06/timing-tab.msft.png":::
   O `respondWith` evento do trabalhador do serviço na guia **Timing** da **ferramenta Rede**  
:::image-end:::  

Expanda **Resposta recebida** para exibir informações adicionais `fetch` da `CacheStorageCacheName` resposta, como , e `serviceWorkerResponseSource` `ResponseTime` .  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Expanda Resposta recebida para exibir informações adicionais da resposta de busca" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   Expanda **Resposta recebida** para exibir informações adicionais da `fetch` resposta  
:::image-end:::  

Problema do Chromium [#1066579][CR1066579]  

### <a name="webhint-feedback-in-the-issues-panel"></a>comentários webhint no painel Problemas  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

[webhint][WebhintMain] é uma ferramenta de código aberto que fornece comentários em tempo real sobre acessibilidade, compatibilidade entre navegadores, segurança, desempenho, PWAs e outros problemas comuns de desenvolvimento da Web de sites.  Para revisar os comentários da webhint no painel [Problemas.][DevtoolsIssues]  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="comentários webhint no painel Problemas" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   comentários webhint no painel Problemas  
:::image-end:::  

> [!NOTE]
> Para habilitar o experimento, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOn] e escolha a caixa de seleção ao lado de **Habilitar webhint**.  
> 
> Abra o [painel Problemas][DevtoolsIssues] para exibir comentários da webhint.  

Problema do Chromium [#1070378][CR1070378]  

### <a name="move-tools-between-panels"></a>Mover ferramentas entre painéis  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

Normalmente, ferramentas como **Elementos** e **Rede** só podem ser abertas no painel principal \(top\) do DevTools.  Da mesma forma, ferramentas como Exibição **3D** e **Problemas** só podem ser abertas no painel de gaveta \(bottom\) do DevTools.  Agora você pode personalizar o layout do DevTools movendo ferramentas entre os painéis superior e inferior.  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Mover ferramentas entre painéis" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   Mover ferramentas entre painéis  
:::image-end:::  

> [!NOTE]
> Para habilitar o experimento, navegue até Ativar recursos [experimentais][DevtoolsExperimentalFeaturesTurnOn] e escolha a caixa de seleção ao lado de Habilitar suporte para mover **guias entre painéis**.  

Problema do Chromium [#897944][CR897944]  

### <a name="improved-initiator-tooltip-in-the-network-panel"></a>Dica de ferramenta iniciador aprimorada no painel Rede  

No Microsoft Edge 83 e 84, dicas de ferramenta para a coluna Iniciador, que mostra a causa da solicitação de recurso, no [Log][DevtoolsNetworkIndexLogActivity] de Rede exibido com uma barra de rolagem horizontal.  Você só foi capaz de exibir a pilha de chamada que iniciou a solicitação rolando horizontalmente na dica de ferramenta.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="A dica de ferramenta Iniciador no Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   A dica de ferramenta Iniciador no Microsoft Edge 84  
:::image-end:::  

A partir do Microsoft Edge 85, agora você pode exibir a pilha de chamada iniciador na dica de ferramenta sem rolar horizontalmente.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="A dica de ferramenta Iniciador no Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   A dica de ferramenta Iniciador no Microsoft Edge 85
:::image-end:::  

Problema do Chromium [#1069404][CR1069404]  

## <a name="announcements-from-the-chromium-project"></a>Anúncios do projeto Chromium  

As seções a seguir anunciam recursos adicionais disponíveis no Microsoft Edge 85 que contribuíram para o projeto Chromium de código aberto.  

### <a name="style-editing-for-css-in-js-frameworks"></a>Edição de estilo para estruturas CSS-in-JS  

O **painel Estilos** agora tem melhor suporte para edição de estilos que foram criados com as APIs CSS Object Model [(CSSOM).][CsswgDraftsCssom]  Muitas estruturas e bibliotecas CSS-in-JS usam as APIs CSSOM sob o hood para construir estilos.  

Agora você pode editar estilos adicionados em JavaScript usando [Folhas de Estilo Construíveis.][WicgConstructStylesheet]  Folhas de estilo construíveis são uma nova maneira de criar e distribuir estilos reutilizáveis ao usar [o Shadow DOM.][MdnShadowDom]  

Por exemplo, os `h1` estilos adicionados `CSSStyleSheet` com \(APIs CSSOM\) não eram editáveis anteriormente.  Os estilos agora podem ser editáveis no **painel Estilos.**  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Alterar a propriedade em segundo plano dos estilos h1 adicionados com CSSStyleSheet do rosa para o lightblue" lightbox="../../media/2020/06/css-in-js.msft.png":::
   Alterar a `background` propriedade dos `h1` estilos adicionados de para `CSSStyleSheet` `pink` `lightblue` .
:::image-end:::  

Experimente esse recurso com um [exemplo que usa CSS-in-JS][CodepenZoherghadyaliAbdgrpz].

Problema do Chromium [#946975][CR946975]  

### <a name="lighthouse-6-in-the-lighthouse-panel"></a>Farol 6 no painel do Farol  

O **painel do Farol** agora está executando o Farol 6.  Para uma lista completa de todas as alterações, navegue até [v6.0.0 notas de versão][GithubGoogleChromeLighthouse600].  

O Farol 6.0 apresenta três novas métricas ao relatório: Maior Tinta Contentful \(LCP\), Turno cumulativo de layout \(CLS\) e Tempo total de bloqueio \(TBT\).  

A fórmula de pontuação de desempenho também foi repesada para refletir melhor a experiência de carregamento do usuário.  

Problema do Chromium [#772558][CR772558]  

#### <a name="first-meaningful-paint-deprecation"></a>Primeira preteração de Tinta Significativa  

First Meaningful Paint \(FMP\) é preterido no Lighthouse 6.0.  O FMP também foi removido do painel **Desempenho.**  **Maior Tinta Contentful** é a substituição recomendada para FMP.  <!--For an explanation of why it was deprecated, navigate to [First Meaningful Paint][WebDevFirstMeaningfulPaint].  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

Problema do Chromium [#1096008][CR1096008]  

### <a name="support-for-new-javascript-features"></a>Suporte para novos recursos JavaScript  

O DevTools agora tem melhor suporte para alguns dos recursos de idioma JavaScript mais recentes.  

:::row:::
   :::column span="1":::
      [Autocompleção de][V8DevOptionalChaining] sintaxe de encadeamento opcional  
   :::column-end:::
   :::column span="2":::
      A conclusão automática da propriedade no **Console** agora dá suporte à sintaxe de encadeamento opcional, por exemplo, agora funciona  `name?.` além de e `name.` `name[` .  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Realce de sintaxe para [campos privados][V8DevClassFieldsPrivate]  
   :::column-end:::
   :::column span="2":::
      os campos de classe privada agora estão com realce de sintaxe corretamente e muito impressos no **painel Fontes.**  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Realce de sintaxe para [operador de coalescing nullish][V8DevNullishCoalescing]
   :::column-end:::
   :::column span="2":::
      O DevTools agora imprime corretamente o operador de coalescing nulo no **painel Fontes.**  
   :::column-end:::
:::row-end:::  

Problemas de cromo [#1073903,][CR1073903] [#1083214,][CR1083214] [#1083797][CR1083797]  

### <a name="new-app-shortcut-warnings-in-the-manifest-pane"></a>Novos avisos de atalho de aplicativo no painel Manifesto  

**Atalhos de aplicativo ajudam** os usuários a iniciar rapidamente tarefas comuns ou recomendadas em um aplicativo Web.  

<!--todo: add App shortcuts when section is live  -->  

O **painel** Manifesto agora mostra avisos para as seguintes condições.  

* Os ícones de atalho do aplicativo são menores que 96 x 96 pixels  
* Os ícones de atalho do aplicativo e os ícones de manifesto não são quadrados \(já que os ícones são ignorados\)  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Avisos de atalho de aplicativo" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   Avisos de atalho de aplicativo  
:::image-end:::  

Problema do Chromium [#955497][CR955497]  

### <a name="consistent-display-of-the-computed-pane"></a>Exibição consistente do painel Computed  

O **painel computado** na ferramenta **Elementos** agora é exibido consistentemente como um painel em todos os tamanhos do visor.  **Anteriormente, o** painel computado mesclava dentro do painel **Estilos** quando a largura do viewport DevTools era estreita.  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="O painel computado é exibido consistentemente como um painel separado, mesmo quando o DevTools é estreito" lightbox="../../media/2020/06/computed-pane.msft.png":::
   O **painel computado** é exibido consistentemente como um painel separado, mesmo quando o DevTools é estreito.
:::image-end:::  

Problema do Chromium [#1073899][CR1073899]  

### <a name="bytecode-offsets-for-webassembly-files"></a>Deslocamentos de bytecode para arquivos WebAssembly  

O DevTools agora usa deslocamentos de bytecode para exibir números de linha de desmontagem de Wasm.  
Os números de linha fazem com que seja mais claro que você está olhando para dados binários e é mais consistente com a forma como os locais de referência do tempo de execução wasm.  

Problema do Chromium [#1071432][CR1071432]  

### <a name="line-wise-copy-and-cut-in-sources-panel"></a>Cópia e corte em linha no Painel de Fontes  

Ao executar a cópia ou o corte sem seleção no [editor][DevtoolsSourcesEditCssJavascript]do painel Fontes, o DevTools copia ou corta a linha atual de conteúdo.  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Com o cursor no final da Linha 5, copiando toda a linha do pen.js no DevTools e colar no Visual Studio Code" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   Com o cursor no final da Linha 5, copiando toda ** a ** linha dopen.jsno DevTools e colar no [código Visual Studio][VisualStudioCode].
:::image-end:::  

Problema do Chromium [#800028][CR800028]

### <a name="console-settings-updates"></a>Atualizações de Configurações de Console  

#### <a name="ungroup-same-console-messages"></a>Desagrupar as mesmas mensagens de console  

A **alternância de** grupo semelhante em Configurações de Console agora se aplica a mensagens duplicadas.  Anteriormente, ele só se aplicava a mensagens semelhantes.  

Por exemplo, anteriormente, o DevTools não desagrupou as `hello` mensagens, mesmo que **Group similar** seja desmarcado.  Agora, as `hello` mensagens estão desagrupadas.  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Quando Group similar é desmarcado, as mensagens hello são desagrupadas" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   Quando **Group similar** é desmarcado, as mensagens são `hello` desagrupadas
:::image-end:::  

Experimente esse recurso com um exemplo [que envia mensagens duplicadas para o Console][CodepenZoherghadyaliZyrjgdJ].  

Problema do Chromium [#1082963][CR1082963]  

### <a name="persisting-selected-context-only-settings"></a>Persistindo apenas configurações de contexto selecionado  

As **configurações de contexto selecionadas** somente nas Configurações do Console agora são persistentes.  Anteriormente, as configurações eram redefinidas sempre que você fechava e reabria o DevTools.  A alteração torna o comportamento de configuração consistente com outras opções de Configurações do Console.  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Configuração somente de contexto selecionado" lightbox="../../media/2020/06/selected-context.msft.png":::
   **Configuração somente de contexto** selecionado  
:::image-end:::  

Problema do Chromium [#1055875][CR1055875]  

### <a name="performance-panel-updates"></a>Atualizações do painel de desempenho  

#### <a name="javascript-compilation-cache-information-in-performance-tool"></a>Informações de cache de compilação JavaScript na **ferramenta Performance**  

[As informações de cache de compilação javaScript][V8DevCodeCaching] agora são sempre exibidas no painel **Resumo** da **ferramenta Performance.**  Anteriormente, o DevTools não mostrava nada relacionado ao cache de código se o cache de código não tivesse acontecido.  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Informações de cache de compilação javaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   Informações de cache de compilação javaScript  
:::image-end:::  

Problema do Chromium [#912581][CR912581]  

#### <a name="navigation-timing-alignment-in-the-performance-panel"></a>Alinhamento do tempo de navegação no painel Desempenho  

O **painel** Desempenho usado para mostrar horários nas réguas com base em quando a gravação foi iniciada.  O tempo agora foi alterado para gravações em que o usuário navega, onde o DevTools agora mostra tempos de régua em relação à navegação.  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Alinhar o tempo de navegação na ferramenta Performance" lightbox="../../media/2020/06/nav-timing.msft.png":::
   Alinhar o tempo de navegação na **ferramenta Performance**  
:::image-end:::  

Os tempos `DOMContentLoaded` para , First Paint, First Contentful Paint e Largest Contentful Paint eventos são atualizados para serem relativos ao início da navegação, o que significa que o tempo corresponde aos horários relatados por `PerformanceObserver` .  

Problema do Chromium [#974550][CR974550]  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a>Novos ícones para pontos de interrupção, pontos de interrupção condicional e logpoints  

O **painel Fontes** tem novos designs para pontos de interrupção, pontos de interrupção condicionais e pontos de log.  Os pontos de interrupção são representados por um círculo vermelho, assim [como Visual Studio Código][VisualStudioCode] e [Visual Studio][VisualStudio].  Os ícones são adicionados para diferenciar pontos de interrupção condicionais e logpoints.  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Pontos de interrupção" lightbox="../../media/2020/06/breakpoints.msft.png":::
   Pontos de interrupção  
:::image-end:::  

Problema do Chromium [#1041830][CR1041830]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows ou macOS, considere usar os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Como entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Executar comandos com o menu de comando Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Gaveta - Personalizar o Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Ativar recursos experimentais - Recursos experimentais | Microsoft Docs"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Localizar e corrigir problemas com a ferramenta Issues do DevTools do Microsoft Edge | Microsoft Docs"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Editar CSS e JavaScript - Visão geral do painel de fontes | Microsoft Docs"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Atividade de rede de log - Inspecionar atividade de rede no Microsoft Edge DevTools | Microsoft Docs"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Edição de estilo para estruturas CSS-in-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Enviar mensagens duplicadas para o console | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Exemplo de planejador de grade CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros do Chromium"  

[CR772558]: https://crbug.com/772558 "DevTools: atualizar para a versão mais recente do | Bugs do Chromium"  
[CR800028]: https://crbug.com/800028 "Atalho de linha duplicado no editor de Ferramentas de Desenvolvedor não funcionando após a atualização do Chrome | Bugs do Chromium"  
[CR912581]: https://crbug.com/912581 "Expor quais scripts foram armazenados em cache pelo V8 no DevTools/about:tracing | Bugs do Chromium"  
[CR946975]: https://crbug.com/946975 "Barra lateral estilos de DevTools não funciona com folhas de estilo construídas | Bugs do Chromium"  
[CR955497]: https://crbug.com/955497 "Menu Atalho de ícone de aplicativo para PWAs | Bugs do Chromium"  
[CR974550]: https://crbug.com/974550 "Incompatibilidade métrica entre o painel Perf e performanceObserver | Bugs do Chromium"  
[CR1041830]: https://crbug.com/1041830 "Melhorar as cores para pontos de interrupção | Bugs do Chromium"  
[CR1055875]: https://crbug.com/1055875 "O valor da configuração de console somente de contexto selecionado não persiste após o fechamento e a reabertura das Ferramentas de Desenvolvedor | Bugs do Chromium"  
[CR1066579]: https://crbug.com/1066579 "DevTools: Mostrar Linha do Tempo de Busca do ServiceWorkers por solicitação no painel DevTools | Bugs do Chromium"  
[CR1071432]: https://crbug.com/1071432 "Experiência de Desenvolvedor Do Wasm Basic | Bugs do Chromium"  
[CR1073899]: https://crbug.com/1073899 "A guia Estilo Calculado desaparece no modo responsivo | Bugs do Chromium"  
[CR1073903]: https://crbug.com/1073903 "DevTools: Realce de sintaxe não funciona com campos privados | Bugs do Chromium"  
[CR1082963]: https://crbug.com/1082963 "Não é possível desabilitar o comportamento de mensagens semelhantes do grupo do console | Bugs do Chromium"  
[CR1083214]: https://crbug.com/1083214 "Acorn não dá suporte a encadeamento opcional | Bugs do Chromium"  
[CR1083797]: https://crbug.com/1083797 "Impressão bastante interrompida para a | Bugs do Chromium"  
[CR1096008]: https://crbug.com/1096008 "Remover O FMP | Bugs do Chromium"  
[CR1047356]: https://crbug.com/1047356 "Css Grid/Flexbox/Table tooling | Bugs do Chromium"  
[CR1093687]: https://crbug.com/1093687 "Criar ferramenta para criar e repetir solicitações de rede sintéticas | Bugs do Chromium"  
[CR1070378]: https://crbug.com/1070378 "Integrar webhint ao DevTools | Bugs do Chromium"  
[CR1069404]: https://crbug.com/1069404 "Os pop-ups de widget [Ferramentas de Dev] são muito estreitos | Bugs do Chromium"  
[CR897944]: https://crbug.com/897944 "Painéis de devtool arrastáveis | Bugs do Chromium"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v6.0.0 - GoogleChrome/| GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Novo problema - MicrosoftDocs/desenvolvedor de borda"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Usando o DOM de sombra | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Canais de Visualização do Microsoft Edge"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"
[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio Code"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Modelo de Objeto CSS (CSSOM) | Rascunhos do Editor do Grupo de Trabalho CSS do W3C"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Postar um Tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "conta @EdgeDevTools do Twitter"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Campos de classe privada - Campos de classe pública e privada | V8. Dev"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Cache de código para desenvolvedores JavaScript | V8. Dev"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Coalescing nullish | V8. Dev"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Encadeamento opcional | V8. Dev"  

[WebhintMain]: https://webhint.io "webhint"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Objetos Stylesheet construíveis | Web Incubator CG"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "A Web Que Queremos"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developer.chrome.com/blog/new-in-devtools-85) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
