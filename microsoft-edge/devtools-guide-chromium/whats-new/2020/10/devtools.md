---
description: Novas ferramentas de depuração de Grade CSS, ferramenta Webauthn, ferramentas moveizáveis e painel da barra lateral Computada.
title: Novidades no DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/26/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 88e6678880172a7a494bcf73c74874aeb70c24b9
ms.sourcegitcommit: e737277744dd25a7585c113eef22a2aa4d4c167f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "11325956"
---
# Novidades no DevTools (Microsoft Edge 87)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## Melhorar a localização do DevTools  

Para atender às suas necessidades de tradução, a equipe do Microsoft Edge DevTools se concentra em melhorar a qualidade da tradução.  A partir da versão 87 do Microsoft Edge, várias cadeias de caracteres e termos são bloqueados e não mudam mesmo quando o restante do DevTools é exibido em outros idiomas.  A lista de cadeias de caracteres e termos afetados inclui o seguinte.  

*   As cadeias de caracteres na **ferramenta Desdoo.**  
*   O termo `service worker` .  
*   Alguns dos **filtros da** ferramenta de `URL` rede, como , e `XHR` `JS` `CSS` .  
*   A API de Utilitários de Console [$0.][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]  
    
[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] agora está disponível no [Console](/microsoft-edge/devtools-guide-chromium/console/index.md) para usuários em versões localizadas do DevTools.   Obrigado à comunidade global de desenvolvedores por ajudar a melhorar a localização do Microsoft Edge DevTools.  Continue a [enviar comentários sobre a qualidade de localização](#getting-in-touch-with-microsoft-edge-devtools-team) para melhorar o suporte para o DevTools em todas as localidades.  Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até Problema [#1136655][CR1136655].  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Ferramenta de rede com filtros não localizados" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   **Painel** de rede com filtros não localizados  
:::image-end:::  

## Mover ferramentas entre os painéis superior e inferior  

O DevTools agora dá suporte à movimentação de ferramentas entre os painéis superior e inferior.  Personalize o DevTools e melhore sua produtividade exibindo qualquer combinação de duas ferramentas ao mesmo tempo.  Por exemplo, ex view the **Elements** and the **Sources** tools at the same time \(by moving the **Sources** tool to the bottom\).  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [#1075732][CR1075732].  

:::row:::
   :::column span="":::
      Para mover qualquer ferramenta superior para a parte inferior, passe o mouse sobre uma guia, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Mover para **baixo.**  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Mover para baixo" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         Mover para baixo  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Para mover qualquer ferramenta inferior para a parte superior, passe o mouse sobre uma guia, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Mover para cima.**  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Mover para o topo" lightbox="../../media/2020/10/move-to-top.msft.png":::
         Mover para o topo  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## Salvar e exportar usando o Console de Rede  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

A **ferramenta Console de** Rede agora melhorou a compatibilidade com os esquemas [Postman v2.1][PostmanSchemaJsonCollectionv210Index] e [OpenAPI v2.][SwaggerSpecificationV2]  Para habilitar o experimento, navegue até Ativar [recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **Habilitar Console de Rede.**  Para obter mais informações sobre o **Console de Rede,** navegue até [Habilitar o recurso Experimental do Console de Rede.][DevtoolsExperimentalFeaturesEnableNetworkConsole]  Esse experimento agora dá suporte às ações a seguir.  

*   Salvar e exportar coleções e ambientes.  
*   Edite e exporte conjuntos de variáveis de ambiente na ferramenta **Console de** Rede.  
    
Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até [Problema #1093687][CR1093687].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Insira o nome do novo ambiente" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         Insira o nome do novo ambiente  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Escolher formato para o novo ambiente" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         Escolher formato para o novo ambiente  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Ferramentas de grade CSS aprimoradas  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

O Microsoft Edge DevTools agora oferece suporte aos seguintes recursos para inspecionar, exibir e depurar suas grades CSS.  

*   Exibir uma sobreposição de grade simplificada usando a ferramenta **Inspect** ou obter informações mais detalhadas com sobreposições persistentes.  
*   Para habilitar sobreposições de grade persistentes, escolha o ícone de grade ao lado de um elemento de contêiner de grade na ferramenta **Elementos** ou escolha a grade na ferramenta **Layout.**  
*   Você pode habilitar sobreposições persistentes para várias grades.  
*   A nova **ferramenta Layout** permite que você alterne facilmente sobreposições de grade e configure a aparência e o conteúdo de cada uma delas.  
    
Os recursos estão ligado por padrão.  Para obter mais informações sobre os recursos, navegue até [grades CSS.][DevtoolsCssGrid]  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [#1047356][CR1047356].  Além disso, a equipe do Microsoft Edge DevTools está colaborando com a equipe do Chrome DevTools e a comunidade do Chromium para adicionar novos recursos de ferramentas do Flexbox ao DevTools.  Para atualizações sobre ferramentas de flexbox no projeto de software livre do Chromium, navegue até [Problema #1136394][CR1136394].  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Ferramenta de layout com grades" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   **Ferramenta de layout** com grades  
:::image-end:::  

## Personalizar atalhos de teclado em Configurações  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

Agora você pode personalizar o atalho do teclado para qualquer ação no DevTools.  Desde a versão 84 do Microsoft Edge, você pode escolher entre predefinições do **Visual Studio Code** e do **DevTools (padrão)** para [atalhos de teclado.][DevtoolsCustomizeShortcuts]  A partir da versão 87 do Microsoft Edge, você pode ativar o experimento de editor de atalhos de teclado **Habilitar** para personalizar ainda mais [os atalhos de teclado.][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]  

Para habilitar o experimento, navegue até Ativar recursos [experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **Habilitar o editor de atalho do teclado.**  Para obter mais informações sobre como personalizar e editar atalhos, acesse o [recurso experimental do editor de atalhos de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até Problema [#174309][CR174309].  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Atalho personalizado para pausar um script" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   Atalho personalizado para pausar um script  
:::image-end:::  

## Apresentando a extensão do Microsoft Edge Tools for Visual Studio Code  

Os **elementos para o Visual Studio Code** e a rede para **extensões do Visual Studio Code** agora são mesclados na nova extensão Microsoft Edge Developer Tools para Visual Studio [Code.][VisualStudioCodeMarketplaceMsEdgedevtools]  Use o Microsoft Edge DevTools para as seguintes atividades sem sair do Visual Studio Code.  

*   Depurar o DOM  
*   Editar CSS  
*   Inspecionar o tráfego de rede  

Com a extensão, launch Microsoft Edge, connect to an existing instance of the browser, or use a headless browser directly from your editor.  Para começar a contribuir e registrar problemas com seus comentários sobre essa extensão, navegue até o repositório microsoft [Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] no GitHub.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Usando a extensão no modo de navegador completo captura de tela" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         Usando a extensão no modo de navegador completo captura de tela  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Using the extension in headless mode screenshot" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         Using the extension in headless mode screenshot  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Anúncios do projeto Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Nova ferramenta WebAuthn  

Em versões anteriores do Microsoft Edge, não havia suporte nativo de depuração WebAuthn.  Você precisava de autenticadores físicos para testar seu aplicativo Web com a [API de Autenticação da Web.][GithubW3cWebauthn]  Com a nova **ferramenta WebAuthn,** você pode fazer as seguintes ações sem o uso de autenticadores físicos.

*   Emular autenticadores
*   Personalizar atributos de autenticadores
*   Inspecionar estados de autenticadores
    
Para obter mais informações sobre o recurso **WebAuthn,** navegue até [Emular autenticadores e depurar WebAuthn no Microsoft Edge DevTools][DevtoolsWebauthnIndex].  

Você pode emular autenticadores e depurar a API de Autenticação da [Web][GithubW3cWebauthn] com a nova [ferramenta WebAuthn.][DevtoolsWebauthnIndex]  Para abrir a **ferramenta WebAuthn,** escolha o ícone Personalizar e controlar **o DevTools** \( \) > `...` Mais **ferramentas**  >  **WebAuthn**.  Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até Problema [#1034663][CR1034663].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Abra a ferramenta WebAuthn" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         Abra a **ferramenta WebAuthn**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Ferramenta WebAuthn" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         **Ferramenta WebAuthn**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Atualizações da ferramenta Elementos  

#### Exibir o painel barra lateral Computado no painel Estilos  

Alterne o **painel Computed** no **painel** Estilos.  O **painel Computed** no painel **Estilos** é recolhido por padrão.  Para alternar, escolha o botão.  Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até [Problema #1073899][CR1073899].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Abrir o painel barra lateral Computado" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         Abrir o **painel barra lateral** Computado  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Painel da barra lateral computado" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         **Painel da barra lateral** computado  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### Agrupar propriedades CSS no painel computado  

Para exibir o CSS aplicado com menos rolagem, a agrupar as propriedades CSS por categorias no **painel** Computed.  Você também pode se concentrar seletivamente em um conjunto de propriedades relacionadas enquanto inspeciona seu CSS.  Na ferramenta **Elementos,** escolha um elemento.  Para agrupar \(ou desagrupar\) as propriedades CSS, alterne a **caixa de seleção** Grupo.  Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até Problemas [#1096230][CR1096230], [#1084673][CR1084673]e [#1106251][CR1106251].  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Agrupar propriedades CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   Agrupar propriedades CSS  
:::image-end:::  

### 6.4 da Ferramenta Desdoo  

A **ferramenta Desdois** agora está executando o 6.4 do 6.4.  Para uma lista completa de alterações, navegue até as notas de [versão do Filme.][GithubGoogleChromeLighthouseReleasesV641]  Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até Problema [#772558][CR772558].  

### eventos performance.mark() na seção Timings  

A **seção Timings de** uma gravação na ferramenta [Desempenho][DevtoolsGuideChromiumEvaluatePerformanceReference] agora marca `performance.mark()` eventos.  Para testar esse recurso e medir o desempenho do código JavaScript, adicione `performance.mark()` eventos ao seu código.  Por exemplo, o trecho de código a seguir adiciona marcadores antes e depois de um loop que itera de 0 a `for` 1000 usando incrementos de 7.  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

Em seguida, abra [a ferramenta Desempenho][DevtoolsGuideChromiumEvaluatePerformanceReference] e navegue até a seção **Timings** para registrar seu código JavaScript.  Os `performance.mark()` eventos adicionados agora são exibidos na gravação.  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Eventos Performance.mark" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` events  
:::image-end:::  

### Novos filtros de URL e tipo de recurso na ferramenta Rede  

Use o novo e `resource-type` as `url` palavras-chave na ferramenta **Rede** para filtrar solicitações de rede.  Por exemplo, use `resource-type:image` para se concentrar nas solicitações de rede que são imagens.  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="filtro de tipo de recurso" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   filtro de tipo de recurso  
:::image-end:::  

Para descobrir mais palavras-chave especiais, como `resource-type` `url` e, navegue até [filtrar solicitações por propriedades.][DevtoolsNetworkReferenceFilterRequestsProperties]  Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até Problemas [#1121141][CR1121141] e [#1104188][CR1104188].  

### Atualizações da exibição de detalhes do quadro  

#### Exibir relatórios COEP e COD para o ponto de extremidade  

Exibir o ponto de extremidade Política de Inserção entre Origens \(COEP\) e Política de Abertura entre Origens \(ÂMBITO\) na seção Isolamento de `reporting to` **& Segurança.**  A [API de Relatórios][MdnReportingApi] define , um novo cabeçalho HTTP, que oferece uma maneira de especificar os pontos de extremidade do servidor para o navegador enviar `Report-To` avisos e erros.  Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até Problema [#1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="O relatório para o ponto de extremidade" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   O `reporting to` ponto de extremidade  
:::image-end:::  

#### Exibir o modo somente relatório COEP e COD  

O DevTools agora exibe `report-only` o rótulo para COEP e COD que estão definidos para `report-only` o modo.  Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até Problema [#1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="O rótulo do modo somente relatório" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   O `report-only` rótulo do modo  
:::image-end:::  

### Exibir e corrigir problemas de contraste de cor na ferramenta de Visão Geral do CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

A **ferramenta De visão** geral do CSS agora exibe uma lista de elementos em sua página que têm problemas de contraste de cor.  A página de demonstração a seguir tem um exemplo de um problema de contraste de cor.  

[Demonstração de cores acessíveis da visão geral do CSS][GlitchCssOverviewAccessibleColorsDemo]  

Para habilitar **** esse experimento, em  >  **Experimentos de Configurações,** escolha a caixa de seleção Visão Geral do **CSS.**  Para exibir uma lista de elementos que têm um problema de contraste de cor, **em**questões de contraste, escolha **Texto**.  Para abrir o elemento na ferramenta **Elementos,** escolha um elemento na lista.  Para ajudar a corrigir problemas de contraste, o Microsoft Edge DevTools [fornece sugestões de cor automaticamente.][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]  Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até [Problema #1120316][CR1120316].  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Problemas de baixo contraste de cor" lightbox="../../media/2020/10/css-overview.msft.png":::
   Problemas de baixo contraste de cor  
:::image-end:::  

## Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows ou no macOS, considere usar os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## Como entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Preterição do painel Propriedades na ferramenta Elementos - Novidades no DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Recursos de depuração de grade CSS - Novidades no DevTools (Microsoft Edge 85) | Microsoft Docs"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Sugestão de cores acessíveis no painel Estilos - Novidades no DevTools (Microsoft Edge 86) | Microsoft Docs"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Elemento selecionado recentemente ou objeto JavaScript - referência de API de utilitários de console | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalizar atalhos de teclado no microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Referência de análise de | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Emulação: Suporte ao modo de tela dupla - recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Habilitar APIs experimentais - recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Habilitar o editor de atalhos de teclado - recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulação: Suporte ao modo de tela dupla - recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Habilitar o Console de Rede - recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Habilitar o Visualizador de Ordem de Origem - Recursos experimentais | Microsoft Docs"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Teste em dispositivos de tela dupla e dobráveis - recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Ativar recursos experimentais - recursos experimentais | Microsoft Docs"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "tabela - Referência da API do Console | Microsoft Docs"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Encontre código CSS e JavaScript não em uso com a guia Cobertura no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Inspecionar grade CSS | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Gaveta - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analisar o desempenho de renderização com a guia Renderização - Performance Analysis Reference | Microsoft Docs"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Exibir e depurar informações de media players | Microsoft Docs"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Filter requests by properties - Network Analysis reference | Microsoft Docs"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Emular autenticadores e depurar WebAuthn no Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de Visualização do Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros do Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: permitir personalizar atalhos de teclado/vinculações de teclas | Bugs do Chromium"
[CR772558]: https://crbug.com/772558 "DevTools: atualização para a versão mais recente do | Bugs do Chromium"  
[CR1034663]: https://crbug.com/1034663 "Criar um front-end para a API de teste do WebAuthn | Bugs do Chromium"  
[CR1047356]: https://crbug.com/1047356 "Css Grid/Flexbox/Table tooling | Bugs do Chromium"  
[CR1051466]: https://crbug.com/1051466 "Suporte à depuração DEM/COEP no DevTools | Bugs do Chromium"  
[CR1073899]: https://crbug.com/1073899 "A guia Estilo Calculado desaparece no modo responsivo | Bugs do Chromium"  
[CR1075732]: https://crbug.com/1075732 "Personalização do DevTools - guias removíveis | Bugs do Chromium"  
[CR1084673]: https://crbug.com/1084673 "DevTools: melhorar a maneira como apresentamos propriedades personalizadas css (também conhecidas). Variáveis CSS) e seus valores | Bugs do Chromium"  
[CR1093687]: https://crbug.com/1093687 "Criar uma ferramenta para criar e repetir solicitações de rede sintéticas | Bugs do Chromium"  
[CR1096230]: https://crbug.com/1096230 "Agrupar propriedades CSS por categorias no painel Estilos Calculados | Bugs do Chromium"  
[CR1104188]: https://crbug.com/1104188 "A pesquisa da ferramenta de rede não encontra resultados ao pesquisar por URL completa | Bugs do Chromium"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: melhorar a guia Estilos Calculados | Bugs do Chromium"  
[CR1120316]: https://crbug.com/1120316 "Realça o contraste ruim em Visão geral de CSS > cores | Chromium Bugs"  
[CR1121141]: https://crbug.com/1121141 "Permitir a filtragem por tipo de recurso no log de rede | Bugs do Chromium"  
[CR1121312]: https://crbug.com/1121312 "As configurações devem ser removidas do menu Mais Ferramentas | Bugs do Chromium"  
[CR1136394]: https://crbug.com/1136394 "Ferramentas do Flexbox | Chromium Bugs"  
[CR1136655]: https://crbug.com/1136655 "Devtools: localização V2 | Bugs do Chromium"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "Relatório api | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v6.4.1 - GoogleChrome/| GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticação da Web | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Olá! | Falha"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Formato da coleção Postman v2.1.0 | Postman"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "Especificação OpenAPI | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/10/devtools/index) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
