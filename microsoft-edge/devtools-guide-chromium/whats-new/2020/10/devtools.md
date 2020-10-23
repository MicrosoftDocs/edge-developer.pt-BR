---
description: Nova ferramentas de depuração de grade CSS, ferramenta webauthn, ferramentas móveis e painel da barra lateral calculada.
title: O que há de novo no DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 0e4b1972918797d69e2068236f6d1336c54cc858
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/23/2020
ms.locfileid: "11133915"
---
# O que há de novo no DevTools (Microsoft Edge 87)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## Melhorando a localização do DevTools  

Para atender às suas necessidades de tradução, a equipe do Microsoft Edge DevTools tem o foco em melhorar a qualidade da tradução.  A partir do Microsoft Edge versão 87, várias cadeias de caracteres e termos são bloqueados e não são alterados mesmo quando o restante da DevTools são exibidos em outros idiomas.  A lista de cadeias de caracteres e termos afetados inclui o seguinte.  

*   As cadeias de caracteres na ferramenta **Lighthouse** .  
*   O termo `service worker` .  
*   Alguns filtros da ferramenta de **rede** , como `URL` , `XHR` , `JS` e `CSS` .  
*   API de utilitários de console do [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] .  
    
o [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] agora está disponível no [console](/microsoft-edge/devtools-guide-chromium/console/index.md) para usuários em versões localizadas do devtools.   Obrigado à comunidade de desenvolvedores globais para ajudar a melhorar a localização do Microsoft Edge DevTools.  Continue a [enviar comentários sobre a qualidade de localização](#getting-in-touch-with-microsoft-edge-devtools-team) para melhorar o suporte para devtools em todas as localidades.  Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#1136655][CR1136655].  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   Painel de **rede** com filtros não traduzidos  
:::image-end:::  

## Mover ferramentas entre os painéis superior e inferior  

O DevTools agora oferece suporte a ferramentas de movimentação entre os painéis superior e inferior.  Personalize sua DevTools e melhore a produtividade ao exibir qualquer combinação de duas ferramentas ao mesmo tempo.  Por exemplo, exiba os **elementos** e as ferramentas de **fontes** ao mesmo tempo \ (movendo a ferramenta **fontes** para a parte inferior \).  Para revisar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até Issue [#1075732][CR1075732].  

:::row:::
   :::column span="":::
      Para mover qualquer ferramenta de cima para baixo, passe o mouse sobre uma guia, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **mover para baixo**.  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         Mover para o fim  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Para mover qualquer ferramenta de cima para baixo, passe o mouse sobre uma guia, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **mover para o início**.  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/move-to-top.msft.png":::
         Mover para o início  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## Salvar e exportar usando o console de rede  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos":::
   Recurso experimental  
:::image-end:::  

A ferramenta de **console de rede** agora aumentou a compatibilidade com os esquemas do [postmaster v 2.1][PostmanSchemaJsonCollectionv210Index] e do [openapi v2][SwaggerSpecificationV2] .  Para habilitar o experimento, navegue até [ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **habilitar console de rede**.  Para obter mais informações sobre o **console de rede**, navegue até habilitar o [recurso experimental do console de rede][DevtoolsExperimentalFeaturesEnableNetworkConsole].  Este experimento agora dá suporte às ações a seguir.  

*   Salvar e exportar coletas e ambientes.  
*   Editar e exportar conjuntos de variáveis de ambiente dentro da ferramenta **console de rede** .  
    
Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#1093687][CR1093687].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         Digite o nome do novo ambiente  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         Escolher formato para o novo ambiente  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Ferramentas de grade CSS aprimoradas  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos":::
   Recurso experimental  
:::image-end:::  

O Microsoft Edge DevTools agora oferece suporte aos recursos a seguir para inspecionar, exibir e depurar suas grades CSS.  

*   Exiba uma sobreposição de grade simplificada usando a ferramenta **inspecionar** ou obter informações mais detalhadas com sobreposições persistentes.  
*   Para habilitar sobreposições de grade persistente, escolha o ícone de grade ao lado de um elemento de contêiner de grade na ferramenta **elementos** ou escolha a grade na ferramenta de **layout** .  
*   Você pode habilitar sobreposições persistentes para várias grades.  
*   A nova ferramenta de **layout** permite que você alterne facilmente sobreposições de grade e configure a aparência e o conteúdo de cada um.  
    
Os recursos estão ativados por padrão.  Para obter mais informações sobre os recursos, navegue até [grades CSS][DevtoolsCssGrid].  Para revisar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até Issue [#1047356][CR1047356].  Além disso, a equipe do Microsoft Edge DevTools está colaborando com a equipe do Chrome DevTools e com a Comunidade da Chromium para adicionar novos recursos de ferramenta de flexbox ao DevTools.  Para obter atualizações sobre a ferramenta flexbox no projeto de fonte aberta do Chromium, navegue até o Issue [#1136394][CR1136394].  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   Ferramenta de **layout** com grades  
:::image-end:::  

## Personalizar atalhos de teclado em configurações  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos":::
   Recurso experimental  
:::image-end:::  

Agora você pode personalizar o atalho de teclado para qualquer ação no DevTools.  Desde a versão 84 do Microsoft Edge, você pode escolher entre o **código do Visual Studio** e predefinições **devtools (padrão)** para [atalhos de teclado][DevtoolsCustomizeShortcuts].  A partir da versão 87 do Microsoft Edge, você pode ativar o **Editor de atalhos de teclado** de teste para personalizar ainda mais os atalhos de [teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  

Para habilitar o experimento, navegue até [ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **habilitar o editor de atalhos de teclado**.  Para obter mais informações sobre como personalizar e editar atalhos, acesse o [recurso experimental do editor de atalhos de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#174309][CR174309].  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   Atalho personalizado para pausar um script  
:::image-end:::  

## Apresentando a extensão de código do Microsoft Edge Tools para Visual Studio  

Os **elementos de código** e rede do Visual Studio **para extensões de código do Visual Studio** agora são mesclados nas novas [ferramentas de desenvolvedor do Microsoft Edge para extensão de código do Visual Studio][VisualStudioCodeMarketplaceMsEdgedevtools] .  Use o Microsoft Edge DevTools para as seguintes atividades sem sair do código do Visual Studio.  

*   Depurar o DOM  
*   Editar CSS  
*   Inspecionar o tráfego de rede  

Com a extensão, inicie o Microsoft Edge, conecte-se a uma instância existente do navegador ou use um navegador sem cabeça diretamente do seu editor.  Para começar a colaborar e arquivar problemas com seus comentários sobre essa extensão, navegue até as [ferramentas de desenvolvedor do Microsoft Edge para repositório de código do Visual Studio][GithubMicrosoftVscodeEdgeDevtools] no github.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         Usar a extensão na captura de tela do modo de navegador completo  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         Usar a extensão na captura de tela de modo sem periféricos  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Anúncios do projeto Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Nova ferramenta webauthn  

Em versões anteriores do Microsoft Edge, não havia nenhum suporte nativo à depuração webauthn.  Você precisou de autenticadores físicos para testar seu aplicativo Web com a [API de autenticação da Web][GithubW3cWebauthn].  Com a nova ferramenta **Webauthn** , você poderá executar as seguintes ações sem o uso de autenticadores físicos.

*   Emular autenticadores
*   Personalizar atributos de autenticadores
*   Inspecionar Estados de autenticadores
    
Para obter mais informações sobre o recurso **Webauthn** , navegue para [emular autenticadores e depurar webauthn no Microsoft Edge devtools][DevtoolsWebauthnIndex].  

Você pode emular autenticadores e depurar a API de [autenticação da Web][GithubW3cWebauthn] com a nova ferramenta [webauthn][DevtoolsWebauthnIndex] .  Para abrir a ferramenta **webauthn** , escolha **o ícone Personalizar e controlar devtools** \ ( `...` \) > **mais ferramentas**  >  **webauthn**.  Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#1034663][CR1034663].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         Abrir a ferramenta **Webauthn**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         Ferramenta **Webauthn**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Atualizações da ferramenta de elementos  

#### Exibir o painel da barra lateral calculada no painel estilos  

Alternar o painel **calculado** no painel **estilos** .  O painel **calculado** no painel **estilos** é recolhido por padrão.  Para ativá-la, escolha o botão.  Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#1073899][CR1073899].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         Abrir o painel da **barra lateral calculada**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         Painel da **barra lateral calculada**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### Agrupando Propriedades CSS no painel calculado  

Para exibir a CSS aplicada com menos rolagem, agrupe as propriedades CSS por categorias no painel **calculado** .  Você também pode se concentrar seletivamente em um conjunto de propriedades relacionadas enquanto inspeciona seu CSS.  Na ferramenta **elementos** , escolha um elemento.  Para agrupar \ (ou desagrupar \) as propriedades CSS, alterne a caixa de seleção do **grupo** .  Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até problemas [#1096230][CR1096230], [#1084673][CR1084673]e [#1106251][CR1106251].  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   Agrupando Propriedades CSS  
:::image-end:::  

### Lighthouse 6,4 na ferramenta Lighthouse  

A ferramenta **Lighthouse** agora está em execução Lighthouse 6,4.  Para obter uma lista completa de alterações, acesse as [notas de versão do Lighthouse][GithubGoogleChromeLighthouseReleasesV641].  Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#772558][CR772558].  

### eventos performance. Mark () na seção timings  

A **seção intervalos** de uma gravação na ferramenta [desempenho][DevtoolsGuideChromiumEvaluatePerformanceReference] agora marca os `performance.mark()` eventos.  Para experimentar esse recurso e medir o desempenho do seu código JavaScript, adicione `performance.mark()` eventos ao seu código.  Por exemplo, o trecho de código a seguir adiciona marcadores antes e depois de um `for` loop que itera de 0 a 1000 usando incrementos de 7.  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

Em seguida, abra a ferramenta [desempenho][DevtoolsGuideChromiumEvaluatePerformanceReference] e navegue até a **seção intervalos** para gravar o código JavaScript.  Os `performance.mark()` eventos que você adicionou são agora exibidos na gravação.  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` MouseUp  
:::image-end:::  

### Novos filtros de tipo de recurso e URL na ferramenta rede  

Use as `resource-type` `url` palavras-chave novo e na ferramenta **rede** para filtrar solicitações de rede.  Por exemplo, use `resource-type:image` para se concentrar nas solicitações de rede que são imagens.  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   filtro do tipo recurso  
:::image-end:::  

Para descobrir mais palavras-chave especiais, como `resource-type` e `url` , navegue até [Filtrar solicitações por Propriedades][DevtoolsNetworkReferenceFilterRequestsProperties].  Para revisar as atualizações em tempo real sobre esse recurso no projeto de fonte aberta do Chromium, navegue até problemas [#1121141][CR1121141] e [#1104188][CR1104188].  

### Atualizações da exibição de detalhes do quadro  

#### Exibir relatórios do COEP e COOP para o ponto de extremidade  

Veja o ponto de extremidade da política incorporada de várias origens \ (COEP \) e interoriginal Opener Policy \ (COOP \) `reporting to` na seção **isolamento de segurança &** .  A [API de relatório][MdnReportingApi] define `Report-To` um novo cabeçalho HTTP, que oferece uma maneira de especificar os pontos de extremidade do servidor para que o navegador envie avisos e erros.  Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   O `reporting to` ponto de extremidade  
:::image-end:::  

#### Exibir COEP e COOP modo somente de relatório  

O DevTools agora exibe o `report-only` rótulo para COEP e Coop que estão definidos como `report-only` Mode.  Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   O `report-only` rótulo Mode  
:::image-end:::  

### Exibir e corrigir problemas de contraste de cor na ferramenta de visão geral CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos":::
   Recurso experimental  
:::image-end:::  

A ferramenta de **visão geral CSS** agora exibe uma lista de elementos em sua página com problemas de contraste de cor.  A seguinte página de demonstração tem um exemplo de um problema de contraste de cor.  

[Visão geral da CSS demonstração de cores acessíveis][GlitchCssOverviewAccessibleColorsDemo]  

Para habilitar esse experimento, em **configurações**  >  **experimentos**, escolha a caixa de seleção **visão geral da CSS** .  Para exibir uma lista de elementos que têm um problema de contraste de cor, em **problemas de contraste**, escolha **texto**.  Para abrir o elemento na ferramenta **elementos** , escolha um elemento na lista.  Para ajudar a corrigir problemas de contraste, o Microsoft Edge DevTools [fornecer sugestões de cores automaticamente][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].  Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#1120316][CR1120316].  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/css-overview.msft.png":::
   Problemas de contraste de cor baixo  
:::image-end:::  

## Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## Como entrar em contato com o Microsoft Edge DevTools equipe  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Substituição do painel Propriedades na ferramenta elementos – novidades do DevTools (Microsoft Edge 84) | Documentos da Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Recursos de depuração de grade CSS-novidades do DevTools (Microsoft Edge 85) | Documentos da Microsoft"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Sugestão de cor acessível no painel estilos – novidades do DevTools (Microsoft Edge 86) | Documentos da Microsoft"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móveis no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Elemento JavaScript ou elemento JavaScript selecionado recentemente-referência de API de utilitários de console | Documentos da Microsoft"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalizar atalhos de teclado no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Referência de análise de desempenho | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Emulação: suporta o modo de tela dupla-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Habilitar APIs experimentais-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Habilitar o editor de atalhos de teclado-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulação: suporta o modo de tela dupla-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Habilitar o console de rede-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Habilitar o Visualizador de ordem de origem-recursos experimentais | Documentos da Microsoft"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Testes em dispositivos dobrável e de tela dupla-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Ativar recursos experimentais-recursos experimentais | Documentos da Microsoft"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "tabela-referência da API do console | Documentos da Microsoft"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Localizar código JavaScript e CSS não usados com a guia cobertura no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Inspecionar grade CSS | Documentos da Microsoft"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Gaveta-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analisar o desempenho de renderização com a guia renderização-referência de análise de desempenho | Documentos da Microsoft"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Exibir e depurar informações do media players | Documentos da Microsoft"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Filtrar solicitações por Propriedades-referência de análise de rede | Documentos da Microsoft"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Emular autenticadores e depurar webauthn no Microsoft Edge DevTools | Documentos da Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de visualização do Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Código do Visual Studio"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Ferramentas do Microsoft Edge para o código do Visual Studio | Código do Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros de Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: permite personalizar atalhos de teclado/associações de teclas | Erros de Chromium"
[CR772558]: https://crbug.com/772558 "DevTools: Atualize para a versão mais recente do Lighthouse | Erros de Chromium"  
[CR1034663]: https://crbug.com/1034663 "Crie um front-end para a API de teste webauthn | Erros de Chromium"  
[CR1047356]: https://crbug.com/1047356 "Ferramentas de grade/flexbox/tabela CSS | Erros de Chromium"  
[CR1051466]: https://crbug.com/1051466 "Suporta a depuração COOP/COEP no DevTools | Erros de Chromium"  
[CR1073899]: https://crbug.com/1073899 "Guia estilo calculado desaparece no modo responsivo | Erros de Chromium"  
[CR1075732]: https://crbug.com/1075732 "Personalização DevTools-guias móveis | Erros de Chromium"  
[CR1084673]: https://crbug.com/1084673 "DevTools: aprimore a maneira como apresentamos as propriedades personalizadas CSS (também conhecidos). Variáveis CSS) e seus valores | Erros de Chromium"  
[CR1093687]: https://crbug.com/1093687 "Crie uma ferramenta para criar e reproduzir solicitações de rede sintéticas | Erros de Chromium"  
[CR1096230]: https://crbug.com/1096230 "Agrupar Propriedades CSS por categorias no painel estilos calculados | Erros de Chromium"  
[CR1104188]: https://crbug.com/1104188 "A pesquisa da ferramenta de rede não localiza resultados ao procurar por URL completa | Erros de Chromium"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: a guia melhorar estilos calculados | Erros de Chromium"  
[CR1120316]: https://crbug.com/1120316 "Realçar contraste incorreto na visão geral da CSS > cores | Erros de Chromium"  
[CR1121141]: https://crbug.com/1121141 "Permitir filtragem por tipo de recurso no log de rede | Erros de Chromium"  
[CR1121312]: https://crbug.com/1121312 "As configurações devem ser removidas do menu mais ferramentas | Erros de Chromium"  
[CR1136394]: https://crbug.com/1136394 "Ferramenta de flexbox | Erros de Chromium"  
[CR1136655]: https://crbug.com/1136655 "Devtools: localização v2 | Erros de Chromium"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "API de relatórios | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v 6.4.1-GoogleChrome/Lighthouse | GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticação da Web | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Olá! | Problema"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Formato da coleção do postmaster v 2.1.0 | Postmaster"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "Especificação do OpenAPI | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/10/devtools/index) e é criada por [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome devtools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
