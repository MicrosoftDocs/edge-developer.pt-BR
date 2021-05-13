---
description: Novas ferramentas de depuração de Grade CSS, ferramenta Webauthn, ferramentas movêveis e painel de barra lateral computada.
title: Novidades no DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c7859631327fc031909cd25736fddb8cff3cff45
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564893"
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
# <a name="whats-new-in-devtools-microsoft-edge-87"></a>Novidades no DevTools (Microsoft Edge 87)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="improving-devtools-localization"></a>Melhorando a localização do DevTools  

Para atender às suas necessidades de conversão, a equipe Microsoft Edge DevTools está focada em melhorar a qualidade da tradução.  A partir da Microsoft Edge versão 87, várias cadeias de caracteres e termos são bloqueados e não mudam mesmo quando o restante do DevTools é exibido em outros idiomas.  A lista de cadeias de caracteres e termos afetados inclui o seguinte.  

*   As cadeias de caracteres na **ferramenta Doleiro.**  
*   O termo `service worker` .  
*   Alguns dos **filtros da ferramenta** Network, como , , e `URL` `XHR` `JS` `CSS` .  
*   A API de Utilitários de Console de [US$ 0.][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]  
    
[$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject] agora está disponível no [Console para][DevtoolsConsoleIndex] usuários em versões localizadas do DevTools.   Obrigado à comunidade global de desenvolvedores por ajudar a melhorar a localização do Microsoft Edge DevTools.  Continue a [enviar comentários sobre a qualidade da localização](#getting-in-touch-with-microsoft-edge-devtools-team) para melhorar o suporte para o DevTools em todas as localidades.  Para revisar as atualizações em tempo real sobre esse recurso no Chromium de código aberto, navegue até Problema [#1136655][CR1136655].  


:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Ferramenta de rede com filtros não localizados" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   **Painel** de rede com filtros não localizados  
:::image-end:::  

## <a name="move-tools-between-top-and-bottom-panels"></a>Mover ferramentas entre painéis superior e inferior  

O DevTools agora dá suporte à movimentação de ferramentas entre os painéis superior e inferior.  Personalize seu DevTools e melhore sua produtividade exibindo qualquer combinação de duas ferramentas ao mesmo tempo.  Por exemplo, ex view the **Elements** and the **Sources** tools at the same time \(by moving the **Sources** tool to the bottom\).  Para revisar o histórico desse recurso no Chromium de código aberto, navegue até Problema [#1075732][CR1075732].  

:::row:::
   :::column span="":::
      Para mover qualquer ferramenta superior para a parte inferior, passe o mouse em uma guia, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Mover para baixo**.  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Mover para baixo" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         Mover para baixo  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Para mover qualquer ferramenta inferior para a parte superior, passe o mouse em uma guia, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Mover para cima**.  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Mover para cima" lightbox="../../media/2020/10/move-to-top.msft.png":::
         Mover para cima  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <a name="save-and-export-using-the-network-console"></a>Salvar e exportar usando o Console de Rede  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

A **ferramenta Console de** Rede agora melhorou a compatibilidade com os esquemas [Postman v2.1][PostmanSchemaJsonCollectionv210Index] e [OpenAPI v2.][SwaggerSpecificationV2]  Para habilitar o experimento, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **Habilitar Console de Rede**.  Para obter mais informações sobre o Console de **Rede,** navegue até [Habilitar o recurso Experimental do Console de Rede][DevtoolsExperimentalFeaturesEnableNetworkConsole].  Este experimento agora dá suporte às seguintes ações.  

*   Salvar e exportar Coleções e Ambientes.  
*   Editar e exportar conjuntos de variáveis de ambiente na **ferramenta Console de** Rede.  
    
Para revisar as atualizações em tempo real sobre esse recurso no Chromium de código aberto, navegue até Problema [#1093687][CR1093687].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Digite o nome do novo ambiente" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         Digite o nome do novo ambiente  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Escolher formato para o novo ambiente" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         Escolher formato para o novo ambiente  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-grid-tooling"></a>Ferramentas de Grade CSS aprimoradas  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

O Microsoft Edge DevTools agora oferece suporte aos seguintes recursos para inspecionar, exibir e depurar suas grades CSS.  

*   Exibe uma sobreposição de grade simplificada usando a ferramenta **Inspecionar** ou obter informações mais detalhadas com sobreposições persistentes.  
*   Para habilitar sobreposições de grade persistentes, escolha o ícone de grade ao lado de um elemento contêiner de grade na ferramenta **Elementos** ou escolha a grade na **ferramenta Layout.**  
*   Você pode habilitar sobreposições persistentes para várias grades.  
*   A nova **ferramenta Layout** permite alternar facilmente sobreposições de grade e configurar a aparência e o conteúdo para cada um.  
    
Os recursos são aados por padrão.  Para obter mais informações sobre os recursos, navegue até [grades CSS][DevtoolsCssGrid].  Para revisar o histórico desse recurso no Chromium de código aberto, navegue até Problema [#1047356][CR1047356].  Além disso, Microsoft Edge equipe do DevTools está colaborando com a equipe do Chrome DevTools e Chromium comunidade para adicionar novos recursos de ferramentas de flexbox ao DevTools.  Para atualizações sobre ferramentas de flexbox no projeto Chromium de código aberto, navegue até Problema [#1136394][CR1136394].  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Ferramenta de layout com grades" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   **Ferramenta de layout** com grades  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a>Personalize os atalhos do teclado em Configurações  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

Agora você pode personalizar o atalho do teclado para qualquer ação no DevTools.  Desde Microsoft Edge versão 84, você pode **** escolher entre as predefinições Visual Studio Code **e DevTools (padrão)** para [atalhos de teclado.][DevtoolsCustomizeShortcuts]  A partir Microsoft Edge versão 87, você pode ativar o experimento Habilitar o **editor** de atalhos de teclado para personalizar ainda mais os [atalhos de teclado.][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]  

Para habilitar o experimento, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de Habilitar o editor de atalho do **teclado.**  Para obter mais informações sobre como personalizar e editar atalhos, navegue até Editar atalhos de teclado para qualquer ação no [DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools].  Para revisar as atualizações em tempo real sobre esse recurso no Chromium de código aberto, navegue até Problema [#174309][CR174309].  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Atalho personalizado para pausar um script" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   Atalho personalizado para pausar um script  
:::image-end:::  

## <a name="introducing-the-microsoft-edge-tools-for-visual-studio-code-extension"></a>Apresentando o Microsoft Edge ferramentas para Visual Studio Code extensão  

Os **elementos para Visual Studio Code** e **Rede** para Visual Studio Code extensões agora são mesclados nas novas ferramentas de desenvolvedor Microsoft Edge para Visual Studio Code [extensão.][VisualStudioCodeMarketplaceMsEdgedevtools]  Use o Microsoft Edge DevTools para as seguintes atividades sem sair Microsoft Visual Studio Código.  

*   Depurar o DOM  
*   Editar CSS  
*   Inspecionar tráfego de rede  

Com a extensão, Microsoft Edge, conecte-se a uma instância existente do navegador ou use um navegador sem cabeça diretamente do seu editor.  Para começar a contribuir e [arquivar][GithubMicrosoftVscodeEdgeDevtools] problemas com seus comentários sobre essa extensão, navegue até o Microsoft Edge ferramentas de desenvolvedor para Visual Studio Code de GitHub.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Usando a extensão na captura de tela do modo de navegador completo" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         Usando a extensão na captura de tela do modo de navegador completo  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Usando a extensão na captura de tela do modo sem cabeça" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         Usando a extensão na captura de tela do modo sem cabeça  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a>Anúncios do projeto Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-webauthn-tool"></a>Nova ferramenta WebAuthn  

Em versões anteriores do Microsoft Edge, não havia suporte para depuração webAuthn nativa.  Você precisava de autenticadores físicos para testar seu aplicativo Web com a [API de Autenticação da Web.][GithubW3cWebauthn]  Com a nova **ferramenta WebAuthn,** você pode fazer as seguintes ações sem o uso de autenticadores físicos.

*   Emular autenticadores
*   Personalizar atributos de autenticadores
*   Inspecionar estados de autenticadores
    
Para obter mais informações sobre o recurso **WebAuthn,** navegue até [Emular autenticadores e depurar WebAuthn no Microsoft Edge DevTools][DevtoolsWebauthnIndex].  

Você pode emular autenticadores e depurar a API de Autenticação da [Web][GithubW3cWebauthn] com a nova ferramenta [WebAuthn][DevtoolsWebauthnIndex].  Para abrir a **ferramenta WebAuthn,** escolha o ícone Personalizar e controlar **DevTools** \( \) > `...` Mais **ferramentas**  >  **WebAuthn**.  Para revisar as atualizações em tempo real sobre esse recurso no Chromium de código aberto, navegue até Problema [#1034663][CR1034663].  

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

### <a name="elements-tool-updates"></a>Atualizações da ferramenta Elementos  

#### <a name="view-the-computed-sidebar-pane-in-the-styles-pane"></a>Exibir o painel da barra lateral Computada no painel Estilos  

Alterne o **painel Computed** no painel **Estilos.**  O **painel Computado** no painel **Estilos** é recolhido por padrão.  Para alternar, escolha o botão.  Para revisar as atualizações em tempo real sobre esse recurso no projeto Chromium de código aberto, navegue até Problema [#1073899][CR1073899].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Abra o painel da barra lateral Computada" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         Abra o **painel da barra lateral** Computada  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Painel de barras laterais calculado" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         **Painel de barras laterais** calculado  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="grouping-css-properties-in-the-computed-panel"></a>Agrupando propriedades CSS no painel Computado  

Para exibir o CSS aplicado com menos rolagem, agrupar as propriedades CSS por categorias no painel **Computed.**  Você também pode se concentrar seletivamente em um conjunto de propriedades relacionadas enquanto inspeciona seu CSS.  Na ferramenta **Elementos,** escolha um elemento.  Para agrupar \(ou desagrupar\) as propriedades CSS, alterne a **caixa de** seleção Grupo.  Para revisar as atualizações em tempo real sobre esse recurso no projeto Chromium de código aberto, navegue até Problemas [#1096230,][CR1096230] [#1084673][CR1084673]e [#1106251][CR1106251].  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Agrupando propriedades CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   Agrupando propriedades CSS  
:::image-end:::  

### <a name="lighthouse-64-in-the-lighthouse-tool"></a>Farol 6.4 na ferramenta Doleiro  

A **ferramenta Doleiro** agora está executando o Farol 6.4.  Para uma lista completa de alterações, navegue até as notas [de versão do Farol.][GithubGoogleChromeLighthouseReleasesV641]  Para analisar as atualizações em tempo real sobre esse recurso no Chromium de código aberto, navegue até Problema [#772558][CR772558].  

### <a name="performancemark-events-in-the-timings-section"></a>eventos performance.mark() na seção Timings  

A **seção Timings** de uma gravação na ferramenta [Performance][DevtoolsEvaluatePerformanceReference] agora marca `performance.mark()` eventos.  Para experimentar esse recurso e medir o desempenho do código JavaScript, adicione `performance.mark()` eventos ao seu código.  Por exemplo, o trecho de código a seguir adiciona marcadores antes e depois de um loop que itera de 0 a `for` 1000 usando incrementos de 7.  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

Em seguida, abra [a ferramenta Performance][DevtoolsEvaluatePerformanceReference] e navegue até a seção **Timings** para gravar seu código JavaScript.  Os `performance.mark()` eventos adicionados agora são exibidos na gravação.  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Eventos Performance.mark" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` events  
:::image-end:::  

### <a name="new-resource-type-and-url-filters-in-the-network-tool"></a>Novos filtros de url e tipo de recurso na ferramenta Rede  

Use as novas `resource-type` e `url` palavras-chave na ferramenta **Rede** para filtrar solicitações de rede.  Por exemplo, use `resource-type:image` para se concentrar nas solicitações de rede que são imagens.  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="filtro de tipo de recurso" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   filtro de tipo de recurso  
:::image-end:::  

Para descobrir palavras-chave mais especiais, como e , navegue até `resource-type` `url` [filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties].  Para analisar as atualizações em tempo real sobre esse recurso no projeto Chromium de código aberto, navegue até Problemas [#1121141][CR1121141] e [#1104188][CR1104188].  

### <a name="frame-details-view-updates"></a>Atualizações da exibição de detalhes do quadro  

#### <a name="display-coep-and-coop-reporting-to-endpoint"></a>Exibir relatórios de COEP e COOP para o ponto de extremidade  

Exibir o ponto de extremidade Política de Embedder entre Origens \(COEP\) e Política de Abertura entre Origens \(COOP\) na seção Isolamento de Segurança `reporting to` **&.**  A [API de][MdnReportingApi] Relatório define , um novo cabeçalho HTTP, que oferece uma maneira de especificar os pontos de extremidade do servidor para o navegador enviar `Report-To` avisos e erros.  Para analisar as atualizações em tempo real sobre esse recurso no Chromium de código aberto, navegue até Problema [#1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="O relatório para o ponto de extremidade" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   O `reporting to` ponto de extremidade  
:::image-end:::  

#### <a name="display-coep-and-coop-report-only-mode"></a>Exibir o modo somente relatório COEP e COOP  

DevTools agora exibe o `report-only` rótulo para COEP e COOP que estão definidos como `report-only` modo.  Para analisar as atualizações em tempo real sobre esse recurso no Chromium de código aberto, navegue até Problema [#1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="O rótulo de modo somente relatório" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   O `report-only` rótulo de modo  
:::image-end:::  

### <a name="view-and-fix-color-contrast-issues-in-the-css-overview-tool"></a>Exibir e corrigir problemas de contraste de cor na ferramenta Visão Geral css  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   Recurso experimental  
:::image-end:::  

A **ferramenta Visão geral** css agora exibe uma lista de elementos em sua página que têm problemas de contraste de cor.  A página de demonstração a seguir tem um exemplo de um problema de contraste de cor.  

[Demonstração de cores acessíveis de visão geral css][GlitchCssOverviewAccessibleColorsDemo]  

Para habilitar esse experimento, **em Configurações**  >  **Experimentos,** escolha a caixa de seleção Visão geral **css.**  Para exibir uma lista de elementos que têm um problema de contraste de cor, em Problemas **de contraste,** escolha **Texto**.  Para abrir o elemento na ferramenta **Elementos,** escolha um elemento na lista.  Para ajudar a corrigir problemas de contraste, o Microsoft Edge DevTools [fornece automaticamente sugestões de cores][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].  Para revisar as atualizações em tempo real sobre esse recurso no projeto Chromium de código aberto, navegue até Problema [#1120316][CR1120316].  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Problemas de contraste de cor baixa" lightbox="../../media/2020/10/css-overview.msft.png":::
   Problemas de contraste de cor baixa  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows ou macOS, considere usar os canais [Microsoft Edge de][MicrosoftEdgePreviewChannels] visualização como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Como entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsTool]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Deprecation do painel Propriedades na ferramenta Elementos - Novidades no DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Recursos de depuração de grade CSS - Novidades no DevTools (Microsoft Edge 85) | Microsoft Docs"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Sugestão de cores acessíveis no painel Estilos - Novidades no DevTools (Microsoft Edge 86) | Microsoft Docs"  

[DevtoolsConsoleIndex]: ../../../console/index.md "Use o console | Microsoft Docs"  
[DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]:  ../../../console/utilities.md#recently-chosen-element-or-javascript-object "Elemento ou objeto JavaScript escolhido recentemente - Referência da API de Utilitários de Console | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personalize os atalhos do teclado no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../../../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Editar atalhos de teclado para qualquer ação no devTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReference]: ../../../evaluate-performance/reference.md "Referência de análise de desempenho | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: ../../../experimental-features/index.md#emulation-support-dual-screen-mode "Emulação: suporte ao modo de tela dupla - Recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: ../../../experimental-features.md#enable-experimental-apis "Habilitar APIs experimentais - Recursos experimentais | Microsoft Docs"  
<!--  [DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: ../../../experimental-features/index.md#enable-keyboard-shortcut-editor "Enable keyboard shortcut editor - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: .. /.. /.. /experimental-features/index.md#enable-new-css-grid-debugging-features "Emulation: Support dual screen mode - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: .. /.. /.. /experimental-features/index.md#enable-network-console "Enable Network Console - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: .. /.. /.. /experimental-features/index.md#enable-source-order-viewer "Enable Source Order Viewer - Experimental features | Microsoft Docs&quot; [DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: .. /.. /.. /experimental-features/index.md#testing-on-foldable-and-dual-screen-devices &quot;Testing on foldable and dual-screen devices - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: .. /.. /.. /experimental-features/index.md#turn-on-experimental-features "Ativar recursos experimentais - Recursos experimentais | Microsoft Docs"  
[DevtoolsConsoleApiTable]: .. /.. /.. /console/api.md#table "table - Console API reference | Microsoft Docs"  
[DevtoolsCoverageIndex]: .. /.. /.. /coverage/index.md "Encontre código JavaScript e CSS nãousado com a guia Cobertura em Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssGrid]: .. /.. /.. /css/grid.md "Inspecionar grade CSS | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: .. /.. /.. /customize/index.md#drawer "Drawer - Personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: .. /.. /.. /customize/index.md#settings "Configurações - Personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: .. /.. /.. /evaluate-performance/reference.md#analyze-rendering-performance-with-the-rendering-tab "Analisar o desempenho da renderização com a guia Renderização - Referência de Análise de Desempenho | Microsoft Docs"  
[DevtoolsMediaIndex]: .. /.. /.. /media/index.md "Exibir e depurar informações de jogadores de mídia | Microsoft Docs"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: .. /.. /.. /network/reference.md#filter-requests-by-properties "Filter requests by properties - Network Analysis reference | Microsoft Docs"  
[DevtoolsWebauthnIndex]: .. /.. /.. /webauthn/index.md "Emular autenticadores e depurar WebAuthn no Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de visualização do Microsoft Edge"  

[VisualStudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Ferramentas para Visual Studio Code | Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros do Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: Permitir personalizar atalhos de teclado/vinculações de teclas | Chromium bugs"
[CR772558]: https://crbug.com/772558 "DevTools: atualizar para a versão mais recente do | Chromium bugs"  
[CR1034663]: https://crbug.com/1034663 "Criar um front-end para a API de Teste webAuthn | Chromium bugs"  
[CR1047356]: https://crbug.com/1047356 "Css Grid/Flexbox/Table tooling | Chromium bugs"  
[CR1051466]: https://crbug.com/1051466 "Suporte à depuração DE COOP/COEP no DevTools | Chromium bugs"  
[CR1073899]: https://crbug.com/1073899 "A guia Estilo Calculado desaparece no modo responsivo | Chromium bugs"  
[CR1075732]: https://crbug.com/1075732 "Personalização de DevTools - Guias móveis | Chromium bugs"  
[CR1084673]: https://crbug.com/1084673 "DevTools: melhore a maneira como apresentamos propriedades personalizadas CSS ((aka). Variáveis CSS) e seus valores | Chromium bugs"  
[CR1093687]: https://crbug.com/1093687 "Criar ferramenta para criar e repetir solicitações de rede sintéticas | Chromium bugs"  
[CR1096230]: https://crbug.com/1096230 "Propriedades CSS de grupo por categorias no painel Estilos Calculados | Chromium bugs"  
[CR1104188]: https://crbug.com/1104188 "A pesquisa da ferramenta de rede não encontra resultados ao pesquisar por url completa | Chromium bugs"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: melhorar a guia Estilos Calculados | Chromium bugs"  
[CR1120316]: https://crbug.com/1120316 "Realça o contraste ruim em Css Overview > Colors | Chromium Bugs"  
[CR1121141]: https://crbug.com/1121141 "Permitir a filtragem por tipo de recurso no log de rede | Chromium bugs"  
[CR1121312]: https://crbug.com/1121312 "Configurações deve ser removido do menu Mais Ferramentas | Chromium bugs"  
[CR1136394]: https://crbug.com/1136394 "Ferramentas do Flexbox | Chromium Bugs"  
[CR1136655]: https://crbug.com/1136655 "Devtools: Localização V2 | Chromium bugs"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "Relatórios de API | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v6.4.1 - GoogleChrome/| GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticação da Web | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Olá! | Glitch"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Formato da coleção Postman v2.1.0 | Postman"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "Especificação do OpenAPI | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developer.chrome.com/blog/new-in-devtools-87) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
