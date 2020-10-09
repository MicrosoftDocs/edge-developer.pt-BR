---
description: Corresponder os atalhos de teclado ao código do Visual Studio, emular Surface Duo e Samsung Galaxy fold, melhorias na sobreposição de grade CSS e muito mais.
title: O que há de novo no DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 74fb4e276547d9f653a5bcbdcab9c4406d09a81a
ms.sourcegitcommit: 912609aa49864e3363aaa3b245ff2aa4bec3fc3e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104858"
---
# O que há de novo no DevTools (Microsoft Edge 86)  

## Anúncios da equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### Corresponder os atalhos de teclado no DevTools ao código do Visual Studio  

No Microsoft Edge 86, você pode corresponder a atalhos de teclado no DevTools para seus atalhos no [código do Visual Studio][VisualStudioCode]. 

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   Corresponder os atalhos de teclado no código do DevTools para o Visual Studio  
:::image-end:::  

Para ativar esse recurso, navegue até [Personalizar atalhos de teclado no Microsoft Edge devtools][DevtoolsCustomizeShortcuts].  

Por exemplo, o atalho de teclado para pausar ou continuar a execução de um script no [código do Visual Studio][VisualStudioCodeShortcutsKeyboardWindows] é `F5` .  Com a predefinição **devtools (padrão)** , o mesmo atalho no devtools é `F8` , mas quando você escolhe a predefinição de **código do Visual Studio** , esse atalho também é `F5` .  

Chromium problema [#174309][CR174309]  

### Emular Surface Duo e dobra para Samsung Galaxy  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio":::
   Recurso experimental  
:::image-end:::  

Agora você pode testar a aparência do seu site ou aplicativo em dois novos dispositivos:  [Surface Duo][MicrosoftSurfaceDevicesDuo] e [dobra da Samsung Galaxy][SamsungMobileGalaxyFold] no Microsoft Edge.  

Para ajudar a aprimorar seu site ou aplicativo para os dispositivos de tela dupla e dobrável, use os recursos a seguir ao [emular o dispositivo][DevtoolsDeviceModeIndex].  

*   [Distribuição][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], que é quando seu site \ (ou app \) aparece em ambas as telas.
*   [Renderizar a fenda][DualScreenIntroductionHowWorkSeam], que é o espaço entre as duas telas.
*   [Habilitar APIs experimentais da Web Platform][DevtoolsExperimentalFeaturesEnableExperimentalApis] para acessar o novo [recurso de distribuição de tela de mídia CSS e a API de][DualScreenWebCssMediaSpanning] [getWindowSegments JavaScript][DualScreenWebJavascriptGetwindowsegments].  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   Emulação de dispositivo para Surface Duo  
:::image-end:::  

Para ativar esse recurso experimental, navegue até [ativar os recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **emulação: suporte para o modo de tela dupla**.  

Para obter mais informações sobre esse experimento, navegue até [emulação: suporte para o modo de tela dupla][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].  

Problema do Chromium: [#1054281][CR1054281]  

### Melhorias na sobreposição de grade CSS e novos recursos de grade experimental  

Obrigado pelo feedback positivo sobre as sobreposições de grade de CSS aprimoradas.  As sobreposições de grade de CSS agora são habilitadas por padrão e não exigem que você ative um experimento.  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   Sobreposição de grade CSS para o `article` elemento  
:::image-end:::  

> [!NOTE]
> Para obter mais informações sobre sobreposições de grade, acesse [recursos de depuração de grade CSS][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].  

A equipe do Microsoft Edge DevTools e a equipe DevTools do Chrome colaboram com recursos adicionais.  Os novos recursos incluem várias sobreposições persistentes e configuráveis a partir de um novo painel de **layout** no painel **elementos** .  

Para ativar esse recurso experimental, navegue até [ativar os recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **habilitar novos recursos de depuração de grade CSS (opções de configuração disponíveis no painel da barra lateral layout nos elementos após a reinicialização)**.  

Para obter mais informações sobre esse experimento, navegue para [habilitar os novos recursos de depuração de grade CSS][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].  

Problema do Chromium: [#1047356][CR1047356]  

### A tabela copiada do console preserva a formatação  

No Microsoft Edge 85 ou anterior, a formatação de uma cópia `console.table` foi perdida.  Se você copiou a saída da API do console de [tabela][DevtoolsConsoleApiTable] e a colou, somente o texto da tabela foi mantido.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` Saída da API do console no Microsoft Edge 85 ou anterior  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` Saída da API do console do Microsoft Edge 85 ou anterior colada no código do Visual Studio  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

No Microsoft Edge 86 ou posterior, quando você copia uma tabela do **console**, a formatação agora é preservada.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` Saída da API do console no Microsoft Edge 86 ou posterior  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` Saída da API do console do Microsoft Edge 86 ou posterior colada no código do Visual Studio  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Problema do Chromium: [#1115011] [CR1115011]  

### Visualizador de pedido de origem para facilitar o teste de acessibilidade  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio":::
   Recurso experimental  
:::image-end:::  

O novo auxiliar de acessibilidade exibe a ordem dos elementos na fonte.  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   Ativar **Mostrar ordem de origem**  
:::image-end:::  

Esse recurso torna mais fácil testar a maneira como o leitor de tela e os usuários de teclado experimentam seu site ou aplicativo.  Os leitores de tela e a navegação de teclado dependem do conteúdo sendo colocado em uma ordem específica no código-fonte do seu site ou aplicativo, para que ele corresponda à página renderizada.  O Visualizador de ordem de origem exibe possíveis diferenças em ordem entre a página renderizada e o código-fonte.  

Para ativar esse recurso experimental, navegue até [ativar os recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **habilitar Visualizador de ordem de origem**.  

Para obter mais informações sobre esse experimento, navegue até [habilitar o Visualizador de ordem de origem][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].  

Problema do Chromium: [#1094406][CR1094406]  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### Ferramenta realçar todos os resultados da pesquisa na ferramenta elementos  

No Microsoft Edge 84 e no 85, o primeiro resultado da pesquisa no painel **elementos** não realce.  Os resultados da pesquisa restantes foram realçados corretamente.  

Obrigado por enviar seus comentários e ajudar a melhorar o Chromium.  Seu comentário sobre o problema não coberto [#1103316][CR1103316] no projeto Chromium de código-fonte aberto.  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   Primeiro resultado da pesquisa realçada no painel de **elementos** no Microsoft Edge 84 ou posterior  
:::image-end:::  

O problema agora está corrigido em todas as versões do Microsoft Edge.  

Problema do Chromium: [#1103316][CR1103316]  

## Anúncios do projeto Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Novo painel de mídia  

O DevTools agora exibe as informações do media players no painel [mídia][DevtoolsMediaPanelIndex] .  

Para abrir o novo painel **mídia** , conclua a etapa a seguir.  

1.  Escolha **Personalizar e controle devtools** \ ( `...` \) > **mais ferramentas**de  >  **mídia**.  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/media-panel.msft.png":::
       Novo painel de **mídia**  
    :::image-end:::  

Antes do novo painel de **mídia** no devtools, as informações de log e depuração sobre players de vídeo estavam localizadas na configuração **jogadores recentes** .  Para abrir a configuração do **reprodutor recentes** , vá para `edge://media-internals` e escolha a guia **players** .  

Exiba conteúdo ao vivo e inspecione possíveis problemas mais rapidamente, incluindo os exemplos a seguir.  

*   Por que os quadros são soltos?  
*   Por que o JavaScript está interagindo com o jogador de forma inesperada?  

### Capturar capturas de tela do nó usando o menu de contexto do painel elementos  

Agora você pode capturar capturas de tela do nó usando o menu de contexto no painel de **elementos** .  

Por exemplo, para fazer uma captura de tela do Sumário, passe o mouse sobre o elemento, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **capturar captura de tela do nó**.  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   Capturar capturas de tela do nó  
:::image-end:::  

Problema do Chromium: [#1100253][CR1100253]  

### Problemas de atualizações da ferramenta  

A barra de aviso de problemas no painel do **console** agora é substituída por uma mensagem normal.  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   Problemas na mensagem do console  
:::image-end:::  

Problemas com cookies de terceiros agora estão ocultos por padrão na ferramenta **problemas** .  Habilite a caixa de seleção **incluir problemas de cookies** de terceiros para exibir os problemas.  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   caixa de seleção problemas com cookies de terceiros  
:::image-end:::  

Problemas do Chromium: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]  

### Emular fontes locais ausentes  

Abra a [ferramenta de renderização][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] e use o novo recurso **desabilitar fontes locais** para emular `local()` fontes ausentes nas `@font-face` regras.  

Por exemplo, quando a `Rubik` fonte é instalada em seu dispositivo e a `@font-face src` regra a usa como `local()` fonte, o Microsoft Edge usa o arquivo de fonte local do seu dispositivo.  

Quando **desativar fontes locais** estiver habilitado, o devtools ignorará as `local()` fontes e buscará cada uma da rede.  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/disable-font.msft.png":::
   Emular fontes locais ausentes  
:::image-end:::  

Se você usar duas cópias diferentes da mesma fonte durante o desenvolvimento, como os exemplos a seguir.  

*   Uma fonte local para suas ferramentas de design.  
*   Uma fonte da Web para seu código.  

Use **desabilitar fontes locais** para facilitar a realização das tarefas a seguir.  

*   Depuração e medição do desempenho e da otimização do carregamento de fontes da Web.  
*   Verifique a precisão das suas `@font-face` regras CSS.  
*   Descubra as diferenças entre as versões locais instaladas em seu dispositivo e uma fonte da Web.  

Problema do Chromium: [#384968][CR384968]  

### Emular usuários inativos  

A [API de detecção ociosa][WebDevIdleDetection] permite que os desenvolvedores detectem usuários inativos e reajam a alterações de estado ocioso.  Agora você pode usar DevTools para emular alterações de estado ocioso na ferramenta **sensores** para o estado do usuário e o estado da tela em vez de aguardar o estado real de ociosidade mudar.  Você pode abrir a ferramenta de **sensores** da [gaveta][DevtoolsCustomizeIndexDrawer].  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   Emular usuários inativos  
:::image-end:::  

Problema do Chromium: [#1090802][CR1090802]  

### Emular preferência-dados reduzidos  

> [!NOTE]
> No Microsoft Edge 86, para habilitar esse recurso, vá para `edge://flags#enable-experimental-web-platform-features` e ative o sinalizador de **recursos da plataforma da Web experimental** .  A opção emulação só será exibida se o sinalizador estiver habilitado.  

A consulta [preferencial – mídia de dados reduzida][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] detecta as preferências de conteúdo do usuário para reduzir os dados.  Se selecionado, o usuário receberá um conteúdo de página alternativo que usa menos dados.  

Agora você pode usar o DevTools para emular a `prefers-reduced-data` consulta de mídia.  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   Emular preferência-dados reduzidos  
:::image-end:::  

Problema do Chromium: [#1096068][CR1096068]  

### Suporte para novos recursos de JavaScript  

O DevTools agora tem o melhor suporte dos recursos da linguagem JavaScript a seguir.  

| Recurso de linguagem JavaScript | Detalhes |  
|:--- |:--- |  
| [Operadores lógicos de atribuição][V8FeaturesLogicalAssignment] | O DevTools agora oferece suporte à atribuição lógica com os novos `&&=` `||=` operadores e `??=` operadores nos painéis **console** e **fontes** .  |  
| [Separadores numéricos][V8FeaturesNumericSeparators] de impressão bonita | Agora, o DevTools agora realmente imprime os separadores numéricos no painel **fontes** .  |  

Problemas do Chromium: [1086817][CR1086817], [1080569][CR1080569]  

### Lighthouse 6,2 no painel Lighthouse  

O painel **Lighthouse** agora está em execução Lighthouse 6,2.  Para obter uma lista completa de alterações, acesse as [notas de versão do Lighthouse][GithubGooglechromeLighthouseV620].  

Problema do Chromium: [#772558][CR772558]  

### Substituição de outras origens listadas no painel de trabalhadores do serviço  

O DevTools agora fornece um link do painel **funcionários do serviço** \ (painel do**aplicativo** > painel de trabalho do **serviço** \) para exibir a lista completa de trabalhadores de serviço de outras origens.  Para acessar a lista sem abrir o DevTools, vá para `edge://service-worker-internals/?devtools` .  

DevTools anteriormente exibir uma lista aninhada sob o painel do **aplicativo** > painel de **trabalhadores do serviço** .  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   Link para outras origens  
:::image-end:::  

Problema do Chromium: [#807440][CR807440]  

### Mostrar Resumo da cobertura para itens filtrados  

O DevTools agora recalcula e exibe um resumo das informações de cobertura dinamicamente.  A exibição dinâmica é disparada quando os filtros são aplicados na ferramenta [cobertura][DevtoolsCoverageIndex] .  Antes que a ferramenta **cobertura** sempre tenha exibido um resumo de todas as informações de cobertura.  

No primeiro dos números a seguir, o resumo é exibido inicialmente `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` e, na segunda das figuras abaixo, o resumo é exibido `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` após a aplicação da filtragem CSS.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         Resumo da cobertura  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         Resumo da cobertura para itens filtrados  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Problema do Chromium: [#1061385][CR1090802]  

### Novo modo de exibição de detalhes do quadro no painel do aplicativo  

O DevTools agora mostra um modo de exibição detalhado para cada quadro.  Para acessá-lo, escolha um quadro no menu **quadros** no painel do **aplicativo** .  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/frame-details.msft.png":::
   Novo modo de exibição detalhado para um quadro no painel de **aplicativos**  
:::image-end:::  

Problema do Chromium: [#1093247][CR1093247]  

#### Detalhes do quadro para janelas abertas  

Abrir janelas e janelas pop-up agora são exibidos na árvore de quadros também.  O modo de exibição detalhado do Windows aberto inclui informações de segurança adicionais.  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/window-opener.msft.png":::
   Modo de exibição detalhado de novo quadro para janelas abertas  
:::image-end:::  

Problema do Chromium: [#1107766] [CR1107766]  

#### Informações de segurança e isolamento  

Contexto seguro, [Cross-Origin-incorporáer-Policy (COEP)][WebDevCoopCoep]e [Cross-Origin-Opener-Policy (Coop)][WebDevCoopCoep] agora são exibidos nos detalhes do quadro.  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/coep-coop.msft.png":::
   Informações de segurança e isolamento  
:::image-end:::  

No futuro, a equipe do Microsoft Edge DevTools e a equipe DevTools do Chrome estão planejando adicionar mais informações de segurança aos detalhes do quadro.  

Problema do Chromium: [#1051466][CR1051466]  

### Atualizações de elementos e painel de rede  

#### Sugestão de cor acessível no painel estilos  

O DevTools agora fornece sugestões de cor para texto de contraste de cor baixa.  

No exemplo abaixo, `h1` há texto de baixo contraste.  Para corrigi-lo, abra o seletor de cores da `color` propriedade no painel **estilos** .  Após expandir a seção de **taxa de contraste** , o devtools fornece sugestões de cores AA e AAA.  Selecione a cor sugerida para aplicar a cor.  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   O seletor de cores sugere sugestões de cores AA e AAA  
:::image-end:::  

Problema do Chromium: [#1093227][CR1093227]  

#### Reaplicar painel Propriedades no painel elementos  

O painel **Propriedades** está de volta.  Ele foi [preterido no Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].  A equipe do Microsoft Edge DevTools e a equipe DevTools do Chrome são melhorias de planejamento para inspecionar Propriedades de elementos.  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/properties-pane.msft.png":::
   Painel **Propriedades** no painel **elementos**  
:::image-end:::  

Problema do Chromium:  <!--  [#1105205][CR1105205],  -->  [#1116085] [CR1116085]  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### Preenchimento automático de fontes personalizadas no painel estilos  

As faces de fonte importadas agora são adicionadas à lista de preenchimento automático de CSS ao editar a `font-family` propriedade no painel **estilos** .  

Por exemplo, se `monospace` for uma fonte personalizada instalada no computador local, ela será exibida na lista de conclusão da CSS. Em versões anteriores do Microsoft Edge, a fonte não era exibida.

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   Autopreencher fontes personalizadas  
:::image-end:::  

Problema do Chromium: [#1106221] [CR1106221]  

#### Exibir consistentemente o tipo de recurso no painel de rede  

O DevTools agora exibe o mesmo tipo de recurso que a solicitação de rede original e acrescenta `/ Redirect` ao valor de coluna de **tipo** quando o redirecionamento \ (código de status HTTP 302 \) acontece.  

Anteriormente, DevTools alterou o tipo para `Other` às vezes.  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/network-redirect.msft.png":::
   Exibir tipo de recurso de redirecionamento  
:::image-end:::  

Problema do Chromium: [#997694][CR997694]  

#### Limpar botões nos painéis de elementos e de rede  

As seguintes caixas de texto agora têm botões **claros** .  

*   As caixas de texto filtro no painel **estilos** e painel de **rede** .  
*   A caixa de texto de pesquisa DOM no painel de **elementos** .  

Escolha o botão **limpar** para remover qualquer texto reemitido.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         Botões limpar nos painéis de **elementos**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         Limpar botões nos painéis de **rede**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Problema do Chromium: [#1067184][CR1067184]  

## Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## Como entrar em contato com o Microsoft Edge DevTools equipe  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Ícone de configurações do DevTools"  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Substituição do painel Propriedades no painel elementos – novidades do DevTools (Microsoft Edge 84) | Documentos da Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Recursos de depuração de grade CSS-novidades do DevTools (Microsoft Edge 85) | Documentos da Microsoft"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móveis no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalizar atalhos de teclado no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Habilitar APIs experimentais-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulação: suporta o modo de tela dupla-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Habilitar o Visualizador de ordem de origem-recursos experimentais | Documentos da Microsoft"
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: https://review.docs.microsoft.com/microsoft-edge/devtools-guide-chromium/experimental-features?branch=user/zoghadya/dual-screen-experiment#emulation-support-dual-screen-mode "Emulação: suporta o modo de tela dupla-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Testes em dispositivos dobrável e de tela dupla-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Ativar recursos experimentais-recursos experimentais | Documentos da Microsoft"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "tabela-referência da API do console | Documentos da Microsoft"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Localizar código JavaScript e CSS não usados com a guia cobertura no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Gaveta-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analisar o desempenho de renderização com a guia renderização-referência de análise de desempenho | Documentos da Microsoft"  
[DevtoolsMediaPanelIndex]: /microsoft-edge/devtools-guide-chromium/media-panel/index "Exibir e depurar informações do media players | Documentos da Microsoft"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Como trabalhar com a fenda-introdução a dispositivos de tela dupla | Documentos da Microsoft"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Tela de mídia CSS – recurso de abrangência para detecção de tela dupla | Documentos da Microsoft"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "A API JavaScript getWindowSegments para dispositivos de tela dupla | Documentos da Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de visualização do Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Código do Visual Studio "  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Atalhos de teclado de código do Visual Studio para Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "O novo Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools conta do Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros de Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: permite personalizar atalhos de teclado/associações de teclas | Erros de Chromium"
[CR384968]: https://crbug.com/384968 "Opção para ignorar fontes locais () | Erros de Chromium"  
[CR772558]: https://crbug.com/772558 "DevTools: Atualize para a versão mais recente do Lighthouse | Erros de Chromium"  
[CR807440]: https://crbug.com/807440 "O Chrome trava com um grande número de SWs | Erros de Chromium"  
[CR997694]: https://crbug.com/997694 "As solicitações XHR com o status do 302 não são mostradas no filtro \ "XHR \" no painel de rede | Erros de Chromium"  
[CR1047356]: https://crbug.com/1047356 "Ferramentas de grade/flexbox/tabela CSS"  
[CR1051466]: https://crbug.com/1051466 "Suporta a depuração COOP/COEP no DevTools | Erros de Chromium"  
[CR1054281]: https://crbug.com/1054281 "Solicitação de recurso: o DevTools deve emular dobrável e dispositivos de tela dupla | Erros de Chromium"  
[CR1067184]: https://crbug.com/1067184 "Solicitação de recurso: botão Limpar filtro em elementos de & de rede-> entradas de filtro de estilo | Erros de Chromium"  
[CR1068116]: https://crbug.com/1068116 "Painel de problemas de envio de ☂ | Erros de Chromium"  
[CR1080569]: https://crbug.com/1080569 "o Acorn não dá suporte a operadores de atribuição lógica | Erros de Chromium"  
[CR1080589]: https://crbug.com/1080589 "Classificar problemas por terceiros/de terceiros | Erros de Chromium"  
[CR1086817]: https://crbug.com/1086817 "Acorn não dá suporte a separadores numéricos | Erros de Chromium"  
[CR1090802]: https://crbug.com/1090802 "Simular alterações de estado ocioso da API de detecção ociosa | Erros de Chromium"  
[CR1093227]: https://crbug.com/1093227 "DevTools: sugerir cor acessível mais próxima | Erros de Chromium"  
[CR1093247]: https://crbug.com/1093247 "Exibir informações sobre quadros no painel de aplicativos | Erros de Chromium"  
[CR1094406]: https://crbug.com/1094406 "Os desenvolvedores querem um visualizador de pedido de origem por AT https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: suporte à emulação do recurso de mídia de dados de preferência-reduzido | Erros de Chromium"  
[CR1096481]: https://crbug.com/1096481 "Posicionamento da faixa de problemas | Erros de Chromium"  
[CR1100253]: https://crbug.com/1100253 "Adicionar atalho do nó de captura de tela no menu de contexto de elemento | Erros de Chromium"  
[CR1103316]: https://crbug.com/1103316 "A pesquisa de elementos não resolveNode (realçar texto, etc.) no primeiro resultado da pesquisa | Erros de Chromium"  
[CR1103854]: https://crbug.com/1103854 "Do-ofuscador X – cliente-valores de dados nas ferramentas de desenvolvedor | Erros de Chromium"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: https://crbug.com/1106221 "adicionar fontes importadas à AutoPreenchimento da família de fontes no painel estilos | Erros de Chromium "  
[CR1107766]: https://crbug.com/1107766 "exibir informações sobre quadros gerados por ' Window. Open () ' na árvore de quadros | Erros de Chromium "  
[CR1115011]: https://crbug.com/1115011 "ao copiar uma tabela do console, a estrutura da tabela não é preservada | Erros de Chromium "  
[CR1116085]: https://crbug.com/1116085 "retorne o Inspetor de propriedades do devtools | Erros de Chromium "  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "preferíveis-reduzido-dados-consultas de mídia nível 5 | Rascunhos do editor de grupo de trabalho W3C CSS"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v 6.2.0-GoogleChrome/Lighthouse | GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Buffers de protocolo | Desenvolvedores do Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy dobre | Samsung US"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Atribuição lógica | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Separadores numéricos | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Como criar seu site \ "entre origens isoladas \" usando COOP e COEP | Web. dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Detectar usuários inativos com a API de detecção de ociosidade | Web. dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Evitar animações não compostas | Web. dev"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/08/devtools/index) e é criada por [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome devtools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
