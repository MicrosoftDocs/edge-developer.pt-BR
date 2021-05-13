---
description: Match keyboard shortcuts to Visual Studio Code, emular Surface Duo e Samsung Galaxy Fold, melhorias de sobreposição de grade CSS e muito mais.
title: Novidades no DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: ec2219e9ebdd5d79c61bcaa813f7784246b1f5d0
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564942"
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
# <a name="whats-new-in-devtools-microsoft-edge-86"></a>Novidades no DevTools (Microsoft Edge 86)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Comunicados da equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### <a name="match-keyboard-shortcuts-in-devtools-to-visual-studio-code"></a>Corresponder atalhos de teclado no DevTools para Visual Studio Code  

No Microsoft Edge 86, você pode corresponder atalhos de teclado no DevTools aos atalhos [em Microsoft Visual Studio Código][VisualStudioCodeMain].  

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Corresponder atalhos de teclado no DevTools para Visual Studio Code" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   Corresponder atalhos de teclado no DevTools para Visual Studio Code  
:::image-end:::  

Para ativar esse recurso, navegue até [Personalizar atalhos de teclado no Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].  

Por exemplo, o atalho do teclado para pausar ou continuar executando um script [em][VisualStudioCodeShortcutsKeyboardWindows] Visual Studio Code é `F5` .  Com a **predefinição DevTools (Padrão),** esse mesmo atalho no DevTools é , mas quando você escolhe o Visual Studio Code predefinido, esse atalho agora `F8` também é **** `F5` .  

Chromium problema [#174309][CR174309]  

### <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a>Emular o Surface Duo e o Samsung Galaxy Fold  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

Agora você pode testar a aparência do seu site ou aplicativo em dois novos dispositivos: [Surface Duo][MicrosoftSurfaceDevicesDuo] e [Samsung Galaxy Fold][SamsungMobileGalaxyFold] no Microsoft Edge.  

Para ajudar a aprimorar seu site ou aplicativo para dispositivos de tela dupla e dobráveis, use os seguintes recursos ao [emular o dispositivo][DevtoolsDeviceModeIndex].  

*   [Abrangência][DevtoolsDeviceModeDualScreenAndFoldables], que é quando seu site \(ou app\) aparece em ambas as telas.
*   [Renderização da junção][DualScreenIntroductionHowWorkSeam], que é o espaço entre as duas telas.
*   Habilitando APIs experimentais da Plataforma Web para acessar o novo recurso de abrangência de tela de mídia [CSS][DualScreenWebCssMediaSpanning] e [JavaScript getWindowSegments API][DualScreenWebJavascriptGetwindowsegments].  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Emulação de dispositivo para Surface Duo" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   Emulação de dispositivo para Surface Duo  
:::image-end:::  

Para ativar esse recurso experimental, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **Emulação:** Suporte ao modo de tela dupla .  

Para obter mais informações sobre esse recurso, navegue até Emular dispositivos de tela dupla e [dobráveis Microsoft Edge DevTools][DevtoolsDeviceModeDualScreenAndFoldables].  

Chromium problema: [#1054281][CR1054281]  

### <a name="css-grid-overlay-improvements-and-new-experimental-grid-features"></a>Melhorias de sobreposição de grade CSS e novos recursos de grade experimentais  

Obrigado pelos comentários positivos sobre as sobreposições de grade CSS aprimoradas.  As sobreposições de grade CSS agora estão habilitadas por padrão e não exigem que você ative um experimento.  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Sobreposição de grade CSS para elemento article" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   Sobreposição de grade CSS para `article` elemento  
:::image-end:::  

> [!NOTE]
> Para obter mais informações sobre sobreposições de grade, navegue até [recursos de depuração de][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]grade CSS.  

A Microsoft Edge de DevTools e a equipe do Chrome DevTools colaboram em recursos adicionais.  Os novos recursos incluem várias sobreposições persistentes e configuráveis de um novo **painel layout** na **ferramenta Elements.**  

Para ativar esse recurso experimental, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de Habilitar novos recursos **de depuração**de Grade CSS (opções de configuração disponíveis no painel da barra lateral layout em Elementos após a reinicialização) .  

Para obter mais informações sobre esse recurso, navegue até [Inspect CSS Grid in Microsoft Edge DevTools][DevtoolsCssGrid].  

Chromium problema: [#1047356][CR1047356]  

### <a name="table-copied-from-the-console-preserves-formatting"></a>Tabela copiada do Console preserva a formatação  

No Microsoft Edge 85 ou anterior, a formatação de uma copiada `console.table` foi perdida.  Se você copiou a saída [da][DevtoolsConsoleApiTable] API de Console da tabela e a colou, apenas o texto da tabela foi mantido.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="saída da API de console de tabela Microsoft Edge 85 ou anterior" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` Saída da API de console em Microsoft Edge 85 ou anterior  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="saída da API de console de tabela Microsoft Edge 85 ou anteriormente Visual Studio Code" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` Saída da API de console Microsoft Edge 85 ou anteriormente Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

No Microsoft Edge 86 ou posterior, quando você copia uma tabela do **Console**, a formatação agora é preservada.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="saída da API de console de tabela Microsoft Edge 86 ou posterior" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` Saída da API de console Microsoft Edge 86 ou posterior  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="saída da API de console de tabela Microsoft Edge 86 ou posteriores em Visual Studio Code" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` Saída da API de console Microsoft Edge 86 ou posteriormente passada para Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Chromium problema: [#1115011][CR1115011]  

### <a name="source-order-viewer-for-easier-accessibility-testing"></a>Visualizador de Ordem de Origem para testes de acessibilidade mais fáceis  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

O novo auxiliar de acessibilidade exibe a ordem dos elementos na origem.  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Ativar Mostrar ordem de origem" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   Ativar **Mostrar ordem de origem**  
:::image-end:::  

Esse recurso facilita o teste da maneira como os usuários de teclado e leitor de tela experimentam seu site ou aplicativo.  Leitores de tela e navegação por teclado dependem do conteúdo que está sendo colocado em uma ordem específica no código-fonte do seu site ou aplicativo, para que ele corresponde à página renderizada.  O Visualizador de Ordem de Origem exibe possíveis diferenças na ordem entre a página renderizada e o código-fonte.  

Para ativar esse recurso experimental, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **Habilitar o Visualizador**de Ordem de Origem.  

Para obter mais informações sobre esse experimento, navegue até [Visualizador de Ordem de Origem][DevtoolsExperimentalFeaturesSourceOrderViewer].  

Chromium problema: [#1094406][CR1094406]  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Microsoft Edge DevTools in Traditional Chinese" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Microsoft Edge DevTools in Japanese" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### <a name="highlight-all-search-results-in-elements-tool"></a>Realça todos os resultados da pesquisa na ferramenta Elements  

Em Microsoft Edge 84 e 85, o primeiro resultado de pesquisa na **ferramenta Elements** não foi realçado.  Os resultados restantes da pesquisa foram realçados corretamente.  

Obrigado por enviar seus comentários e ajudar a melhorar Chromium.  Seus comentários descobriram Problemas [#1103316][CR1103316] no projeto de Chromium de código aberto.  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Primeiro resultado de pesquisa realçado no painel Elementos no Microsoft Edge 84 ou posterior" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   Primeiro resultado de pesquisa realçado na **ferramenta Elements** no Microsoft Edge 84 ou posterior  
:::image-end:::  

O problema agora está corrigido em todas as versões Microsoft Edge.  

Chromium problema: [#1103316][CR1103316]  

## <a name="announcements-from-the-chromium-project"></a>Anúncios do projeto Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-media-tool"></a>Nova ferramenta de mídia  

O DevTools agora exibe informações de media players na ferramenta [Media][DevtoolsMediaPanelIndex].  

Para abrir a nova **ferramenta Mídia,** conclua a etapa a seguir.  

1.  Escolha **Personalizar e controlar DevTools** \( `...` \) > Mais **ferramentas**  >  **Mídia**.  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Nova ferramenta de mídia" lightbox="../../media/2020/08/media-panel.msft.png":::
       Nova **ferramenta de** mídia  
    :::image-end:::  

Antes da nova **ferramenta de mídia** no DevTools, as informações de registro em log e depuração sobre jogadores de vídeo estava localizada na configuração **Jogadores** Recentes.  Para abrir a **configuração Jogadores Recentes,** navegue até `edge://media-internals` e escolha a ferramenta **Players.**  

Exibir conteúdo ao vivo e inspecionar possíveis problemas mais rapidamente, incluindo os exemplos a seguir.  

*   Por que os quadros são descartados?  
*   Por que JavaScript está interagindo com o jogador de forma inesperada?  

### <a name="capture-node-screenshots-using-the-elements-tool-context-menu"></a>Capturar capturas de tela do nó usando o menu de contexto da ferramenta Elements  

Agora você pode capturar capturas de tela do nó usando o menu de contexto na **ferramenta Elements.**  

Por exemplo, para fazer uma captura de tela do conteúdo, passe o mouse no elemento, abra o menu contextual \(clique com o botão direito do mouse\) e selecione Captura captura de tela do **nó**.  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Capturar capturas de tela do nó" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   Capturar capturas de tela do nó  
:::image-end:::  

Chromium problema: [#1100253][CR1100253]  

### <a name="issues-tool-updates"></a>Problemas de atualizações da ferramenta  

A barra de aviso Problemas na **ferramenta Console** agora é substituída por uma mensagem regular.  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Problemas na mensagem do console" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   Problemas na mensagem do console  
:::image-end:::  

Os problemas de cookie de terceiros agora estão ocultos por padrão na **ferramenta Problemas.**  Habilita a nova caixa de seleção Incluir **problemas de cookie** de terceiros para exibir os problemas.  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="caixa de seleção de problemas de cookie de terceiros" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   caixa de seleção de problemas de cookie de terceiros  
:::image-end:::  

Chromium problemas: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]  

### <a name="emulate-missing-local-fonts"></a>Emular fontes locais ausentes  

Abra a [ferramenta Rendering][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] e use o novo recurso Desabilitar fontes locais para emular fontes **ausentes** `local()` em `@font-face` regras.  

Por exemplo, quando a fonte é instalada em seu dispositivo e a regra a usa como fonte, Microsoft Edge usa o arquivo de fonte `Rubik` `@font-face src` local do seu `local()` dispositivo.  

Quando **Desabilitar fontes locais** estiver habilitada, o DevTools ignorará as fontes e `local()` buscará cada uma da rede.  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Emular fontes locais ausentes" lightbox="../../media/2020/08/disable-font.msft.png":::
   Emular fontes locais ausentes  
:::image-end:::  

Se você usar duas cópias diferentes da mesma fonte durante o desenvolvimento, como os exemplos a seguir.  

*   Uma fonte local para suas ferramentas de design.  
*   Uma fonte da Web para seu código.  

Use **Desabilitar fontes locais** para facilitar a conclusão das seguintes tarefas.  

*   Depurar e medir o desempenho de carregamento e a otimização de fontes da Web.  
*   Verifique a precisão de suas regras `@font-face` CSS.  
*   Descubra as diferenças entre as versões locais instaladas em seu dispositivo e uma fonte da Web.  

Chromium problema: [#384968][CR384968]  

### <a name="emulate-inactive-users"></a>Emular usuários inativos  

A [API de Detecção Ociosa][WebDevIdleDetection] permite que os desenvolvedores detectem usuários inativos e reajam em alterações de estado ocioso.  Agora você pode usar o DevTools para emular alterações de estado ocioso na ferramenta **Sensores** para o estado do usuário e o estado da tela, em vez de aguardar a alteração do estado ocioso real.  Você pode abrir a **ferramenta Sensores** da [Gaveta][DevtoolsCustomizeIndexDrawer].  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Emular usuários inativos" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   Emular usuários inativos  
:::image-end:::  

Chromium problema: [#1090802][CR1090802]  

### <a name="emulate-prefers-reduced-data"></a>Emular prefere dados reduzidos  

> [!NOTE]
> No Microsoft Edge 86, para habilitar esse recurso, navegue até e ative o sinalizador de recursos da `edge://flags#enable-experimental-web-platform-features` **Plataforma Web Experimental.**  A opção de emulação só será exibida se o sinalizador estiver habilitado.  

A [consulta de mídia prefers-reduced-data][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] detecta as preferências de conteúdo do usuário para dados reduzidos.  Se selecionado, o usuário recebe conteúdo de página alternativo que usa menos dados.  

Agora você pode usar o DevTools para emular a `prefers-reduced-data` consulta de mídia.  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Emular prefere dados reduzidos" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   Emular prefere dados reduzidos  
:::image-end:::  

Chromium problema: [#1096068][CR1096068]  

### <a name="support-for-new-javascript-features"></a>Suporte para novos recursos JavaScript  

O DevTools agora tem melhor suporte para os seguintes recursos de idioma JavaScript.  

| Recurso de idioma JavaScript | Detalhes |  
|:--- |:--- |  
| [Operadores de atribuição lógica][V8FeaturesLogicalAssignment] | O DevTools agora dá suporte à atribuição lógica com os novos operadores , e nas `&&=` ferramentas Console `||=` e `??=` **Sources.** ****  |  
| Separadores [numéricos][V8FeaturesNumericSeparators] de impressão bastante impressa | O DevTools agora imprime corretamente os separadores numéricos na **ferramenta Sources.**  |  

Chromium problemas: [1086817][CR1086817], [1080569][CR1080569]  

### <a name="lighthouse-62-in-the-lighthouse-panel"></a>Farol 6.2 no painel do Farol  

A **ferramenta Doleiro** agora está executando o Farol 6.2.  Para uma lista completa de alterações, navegue até as notas [de versão do Farol.][GithubGooglechromeLighthouseV620]  

Chromium problema: [#772558][CR772558]  

### <a name="deprecation-of-other-origins-listing-in-the-service-workers-pane"></a>Deprecation of other origins listing in the Service Workers pane  

O DevTools agora fornece **** um link do painel Funcionários do Serviço**\(** Ferramenta de aplicativo > **Painel** de Funcionários do Serviço\) para exibir a lista completa de funcionários do serviço de outras origens.  Para acessar a lista sem abrir o DevTools, navegue até `edge://service-worker-internals/?devtools` .  

Anteriormente, o DevTools exibia uma lista aninhada no **painel Ferramenta aplicativo** > **Funcionários do** Serviço.  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Link para outras origens" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   Link para outras origens  
:::image-end:::  

Chromium problema: [#807440][CR807440]  

### <a name="show-coverage-summary-for-filtered-items"></a>Mostrar resumo de cobertura para itens filtrados  

Agora, o DevTools recalculará e exibirá um resumo das informações de cobertura dinamicamente.  A exibição dinâmica é disparada quando os filtros são aplicados na [ferramenta Cobertura.][DevtoolsCoverageIndex]  Antes que **a ferramenta Coverage** sempre exibia um resumo de todas as informações de cobertura.  

Na primeira das figuras a seguir, o resumo é exibido inicialmente e, na segunda das figuras a seguir, o resumo é exibido depois que a filtragem `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` CSS é aplicada.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Resumo de cobertura" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         Resumo de cobertura  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Resumo de cobertura para itens filtrados" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         Resumo de cobertura para itens filtrados  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Chromium problema: [#1061385][CR1090802]  

### <a name="new-frame-details-view-in-application-panel"></a>Nova exibição de detalhes do quadro no painel Aplicativo  

O DevTools agora mostra uma exibição detalhada para cada quadro.  Para acessá-lo, escolha um quadro no menu **Quadros** na **ferramenta Aplicativo.**  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Nova exibição detalhada para um quadro no painel Aplicativo" lightbox="../../media/2020/08/frame-details.msft.png":::
   Nova exibição detalhada para um quadro na **ferramenta Application**  
:::image-end:::  

Chromium problema: [#1093247][CR1093247]  

#### <a name="frame-details-for-opened-windows"></a>Detalhes do quadro para janelas abertas  

Abra janelas e janelas pop-up agora exibidas sob a árvore de quadros também.  A exibição detalhada das janelas abertas inclui informações adicionais de segurança.  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Novo quadro de exibição detalhado para janelas abertas" lightbox="../../media/2020/08/window-opener.msft.png":::
   Novo quadro de exibição detalhado para janelas abertas  
:::image-end:::  

Chromium problema: [#1107766][CR1107766]  

#### <a name="security-and-isolation-information"></a>Informações de segurança e isolamento  

Contexto seguro, [CoEP (Cross-Origin-Embedder-Policy)][WebDevCoopCoep]e [CROSS-Origin-Opener-Policy (COOP)][WebDevCoopCoep] agora são exibidos nos detalhes do quadro.  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Informações de segurança e isolamento" lightbox="../../media/2020/08/coep-coop.msft.png":::
   Informações de segurança e isolamento  
:::image-end:::  

No futuro, a equipe Microsoft Edge DevTools e a equipe do Chrome DevTools planejam adicionar mais informações de segurança aos detalhes do quadro.  

Chromium problema: [#1051466][CR1051466]  

### <a name="elements-and-network-panel-updates"></a>Elementos e atualizações de painel de rede  

#### <a name="accessible-color-suggestion-in-the-styles-pane"></a>Sugestão de cor acessível no painel Estilos  

O DevTools agora fornece sugestões de cores para texto de contraste de cor baixo.  

No exemplo abaixo, `h1` tem texto de baixo contraste.  Para corrigi-lo, abra o selador de cores `color` da propriedade no painel **Estilos.**  Depois de expandir a seção **Taxa de contraste,** o DevTools fornece sugestões de cores AA e AAA.  Escolha a cor sugerida para aplicar a cor.  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="O se picker de cores sugere sugestões de cores AA e AAA" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   O se picker de cores sugere sugestões de cores AA e AAA  
:::image-end:::  

Chromium problema: [#1093227][CR1093227]  

#### <a name="reinstate-properties-pane-in-the-elements-panel"></a>Reinstalar o painel Propriedades no painel Elementos  

O **painel Propriedades** está de volta.  Foi [preterido no Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].  A Microsoft Edge de DevTools e a equipe do Chrome DevTools estão planejando melhorias para inspecionar propriedades de elementos.  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Painel Propriedades no painel Elementos" lightbox="../../media/2020/08/properties-pane.msft.png":::
   **Painel Propriedades** na **ferramenta Elementos**  
:::image-end:::  

Chromium problema:  <!--  [#1105205][CR1105205],  -->  [#1116085] [CR1116085]  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Human-readable `X-Client-Data` header values" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### <a name="autocomplete-custom-fonts-in-the-styles-pane"></a>Preenchimento automático de fontes personalizadas no painel Estilos  

Os rostos de fonte importados agora são adicionados à lista de autocompleção CSS ao editar a propriedade `font-family` no painel **Estilos.**  

Por exemplo, se for uma fonte personalizada instalada no `monospace` computador local, ela será exibida na lista de conclusão css.  Nas versões anteriores Microsoft Edge, a fonte não era exibida.

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Preenchimento automático de fontes personalizadas" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   Preenchimento automático de fontes personalizadas  
:::image-end:::  

Chromium problema: [#1106221][CR1106221]  

#### <a name="consistently-display-resource-type-in-network-panel"></a>Exibir consistentemente o tipo de recurso no painel Rede  

O DevTools agora exibe consistentemente o mesmo tipo de recurso que a solicitação de rede original e anexa ao valor de coluna Type quando o `/ Redirect` redirecionamento \(código de status HTTP 302\) acontece. ****  

Anteriormente, o DevTools alterou o tipo para às `Other` vezes.  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Exibir tipo de recurso de redirecionamento" lightbox="../../media/2020/08/network-redirect.msft.png":::
   Exibir tipo de recurso de redirecionamento  
:::image-end:::  

Chromium problema: [#997694][CR997694]  

#### <a name="clear-buttons-in-the-elements-and-network-tools"></a>Limpar botões nas ferramentas Elementos e Rede  

As caixas de texto a seguir agora têm **botões Clear.**  

*   As caixas de texto do filtro no painel **Estilos** e **na ferramenta** Rede.  
*   A caixa de texto de pesquisa DOM na **ferramenta Elementos.**  

Escolha o **botão Limpar** para remover qualquer texto de entrada.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Limpar botões nos painéis Elementos" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         Limpar botões nas ferramentas **Elements**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Limpar botões nos painéis rede" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         Limpar botões nas ferramentas  **de** rede  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Chromium problema: [#1067184][CR1067184]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows ou macOS, considere usar os canais [Microsoft Edge de][MicrosoftEdgePreviewChannels] visualização como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Como entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Deprecation do painel Propriedades no painel Elementos - Novidades no DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Recursos de depuração de grade CSS - Novidades no DevTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsConsoleApiTable]: ../../../console/api.md#table "table - Console API reference | Microsoft Docs"  
[DevtoolsCoverageIndex]: ../../../coverage/index.md "Encontre o JavaScript e o código CSS não Microsoft Edge código CSS não Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssGrid]: ../../../css/grid.md "Inspecionar Grade CSS no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: ../../../customize/index.md#drawer "Gaveta - Personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personalize os atalhos do teclado no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../../../device-mode/dual-screen-and-foldables.md "Emular dispositivos de tela dupla e dobráveis Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: ../../../evaluate-performance/reference.md#analyze-rendering-performance-with-the-rendering-tool "Analisar o desempenho da renderização com a ferramenta Rendering - Performance Analysis Reference | Microsoft Docs"  
<!--  [DevtoolsExperimentalFeaturesEnableExperimentalApis]: ../../../experimental-features/index.md#enable-experimental-apis "Enable experimental APIs - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: .. /.. /.. /experimental-features/index.md#emulation-support-dual-screen-mode "Emulation: Support dual screen mode - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesSourceOrderViewer]: .. /.. /.. /experimental-features/index.md#source-order-viewer "Source Order Viewer - Recursos experimentais | Microsoft Docs"
<!--  [DevtoolsExperimentalFeaturesTestOnFoldableDualScreenDevices]: ../../../experimental-features/index.md#test-on-foldable-and-dual-screen-devices "Test on foldable and dual-screen devices - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: .. /.. /.. /experimental-features/index.md#turn-on-experimental-features "Ativar recursos experimentais - Recursos experimentais | Microsoft Docs"  
[DevtoolsMediaPanelIndex]: .. /.. /.. /media-panel/index.md "Exibir e depurar informações de jogadores de mídia | Microsoft Docs"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Como trabalhar com a junção – Introdução aos dispositivos de duas telas | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Recurso de abrangência de tela de mídia CSS para detecção de dualidade de tela | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "A API JavaScript getWindowSegments para dispositivos de duas telas | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de visualização do Microsoft Edge"  

[VisualStudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio Code Atalhos de teclado para Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "O novo Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "conta @EdgeDevTools do Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros do Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: Permitir personalizar atalhos de teclado/vinculações de teclas | Chromium bugs"
[CR384968]: https://crbug.com/384968 "Opção para ignorar fontes locais() | Chromium bugs"  
[CR772558]: https://crbug.com/772558 "DevTools: atualizar para a versão mais recente do | Chromium bugs"  
[CR807440]: https://crbug.com/807440 "O Chrome bloqueia com um grande número de SWs | Chromium bugs"  
[CR997694]: https://crbug.com/997694 "As solicitações XHR com status 302 não são mostradas no filtro \"xhr\" no painel de rede | Chromium bugs"  
[CR1047356]: https://crbug.com/1047356 "Css Grid/Flexbox/Table tooling | Chromium bugs"  
[CR1051466]: https://crbug.com/1051466 "Suporte à depuração DE COOP/COEP no DevTools | Chromium bugs"  
[CR1054281]: https://crbug.com/1054281 "Solicitação de Recurso: DevTools deve emular dispositivos dobráveis e de tela dupla | Chromium bugs"  
[CR1067184]: https://crbug.com/1067184 "Solicitação de Recurso: limpar o botão de filtro em Elementos & Rede -> Entradas de Filtro de Estilo | Chromium bugs"  
[CR1068116]: https://crbug.com/1068116 "☂ Painel de problemas de | Chromium bugs"  
[CR1080569]: https://crbug.com/1080569 "Acorn não dá suporte a operadores de atribuição lógica | Chromium bugs"  
[CR1080589]: https://crbug.com/1080589 "Classificar problemas por terceiros/usuários de terceiros | Chromium bugs"  
[CR1086817]: https://crbug.com/1086817 "Acorn não dá suporte a separadores numéricos | Chromium bugs"  
[CR1090802]: https://crbug.com/1090802 "Simular alterações de estado ocioso da API de Detecção Ociosa | Chromium bugs"  
[CR1093227]: https://crbug.com/1093227 "DevTools: sugerir cores acessíveis mais próximas | Chromium bugs"  
[CR1093247]: https://crbug.com/1093247 "Exibir informações sobre quadros no painel de aplicativos | Chromium bugs"  
[CR1094406]: https://crbug.com/1094406 "Os desenvolvedores querem um visualizador de ordem de origem para AT https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: suporte à emulação do recurso de mídia prefers-reduced-data | Chromium bugs"  
[CR1096481]: https://crbug.com/1096481 "Problemas de posicionamento de faixa | Chromium bugs"  
[CR1100253]: https://crbug.com/1100253 "Adicionar atalho de nó de captura de tela no menu de contexto elemento | Chromium bugs"  
[CR1103316]: https://crbug.com/1103316 "A pesquisa de elementos não resolveNode (texto de realçada, etc) no primeiro resultado da pesquisa | Chromium bugs"  
[CR1103854]: https://crbug.com/1103854 "Desobfusar valores X-Client-Data em Ferramentas de Desenvolvedor | Chromium bugs"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: "Adicionar fontes importadas à autocompleção da família de fontes no painel https://crbug.com/1106221 Estilos | Chromium bugs"  
[CR1107766]: "Exibir informações sobre quadros gerados por https://crbug.com/1107766 'window.open()' na árvore de quadros | Chromium bugs"  
[CR1115011]: "Ao copiar uma tabela do console, a estrutura da tabela não é https://crbug.com/1115011 preservada | Chromium bugs"  
[CR1116085]: "Por favor, traga de volta o inspetor de propriedades https://crbug.com/1116085 de DevTools | Chromium bugs"  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "prefers-reduced-data - Media Queries Level 5 | Rascunhos do Editor do Grupo de Trabalho CSS do W3C"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v6.2.0 - GoogleChrome/| GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Buffers de protocolo | Desenvolvedores do Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung US"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Atribuição lógica | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Separadores numéricos | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Tornar seu site \"isolado entre origens\" usando o COOP e o COEP | web.dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Detectar usuários inativos com a API de Detecção Ociosa | web.dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Evite animações não compostas | web.dev"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developer.chrome.com/blog/new-in-devtools-86) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
