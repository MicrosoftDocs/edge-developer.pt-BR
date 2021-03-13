---
description: Suporte de depuração para CSS Flexbox, exibição de heads-up de desempenho na página da Web, problemas de atualizações da ferramenta e muito mais
title: Novidades no DevTools (Microsoft Edge 90)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 4222bcf7284b69269691ec9fb78094e5efb95793
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408431"
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
# <a name="whats-new-in-devtools-microsoft-edge-90"></a>Novidades no DevTools (Microsoft Edge 90)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="group-tools-together-in-focus-mode"></a>Ferramentas de grupo juntas no Modo de Foco  

<!-- Title: Grouping the tools in Focus Mode  -->  
<!-- Subtitle: Organize your favorite tools into groups with the new Focus Mode UI.  -->  

O Modo de Foco é uma interface experimental que permite agrupar diferentes ferramentas com base em seus próprios cenários de depuração.  A nova **Barra de Atividades** exibida à esquerda inclui grupos de ferramentas predefinidos, como **Layout** e **Depuração.**  Para personalizar cada grupo de ferramentas, feche as ferramentas com o ícone **Fechar** \( \) ou adicione novas ferramentas com o ícone `X` Mais **ferramentas** \( `+` \).  

Para ativar o experimento, [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] navegue até Ativar recursos experimentais e escolha as caixas de seleção ao lado de Focus Mode e **DevTools Tooltips** e **Habilitar + menus**de guia de botão para abrir mais ferramentas .  Para obter mais informações sobre esse recurso ou para comentar com perguntas e ideias, navegue até [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode.msft.png" alt-text="Exibir a Barra de Atividades" lightbox="../../media/2021/02/focus-mode.msft.png":::
   Exibir a **Barra de Atividades**  
:::image-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a>Saiba mais sobre o DevTools com dicas de ferramentas informativas  

<!-- Title: DevTools Tooltips  -->  
<!-- Subtitle: Learn more about how to use DevTools with informative DevTools tooltips.  -->  

O recurso Dicas de Ferramentas do DevTools ajuda você a aprender sobre todas as diferentes ferramentas e painéis.  Escolha o ícone Ajuda \( \) na parte inferior da Barra de Atividades para alternar dicas de `?` ferramenta no **** DevTools.  Quando as dicas de ferramenta estão ativados, passe o mouse sobre cada região descrita do DevTools para saber mais sobre como usar a ferramenta.  Para ativar o experimento, [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] navegue até Ativar recursos experimentais e escolha as caixas de seleção ao lado de Focus Mode e **DevTools Tooltips** e **Habilitar + menus**de guia de botão para abrir mais ferramentas .  Para obter mais informações sobre esse recurso ou para comentar com perguntas e ideias, navegue até [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode-and-tooltips-help.msft.png" alt-text="Escolha o ícone ajuda (?) na Barra de Atividades para exibir dicas de ferramentas" lightbox="../../media/2021/02/focus-mode-and-tooltips-help.msft.png":::
   Escolha o ícone Ajuda \( `?` \) na **Barra de Atividades** para exibir dicas de ferramenta  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a>Personalizar atalhos de teclado em Configurações  

<!-- Title: Change keyboard shortcuts in Settings  -->  
<!-- TODO:  Rachel's feedback is about the fact that this experimental feature is turned on by default, may have separate section in What's New for experimental features)  -->  
<!-- Subtitle: Make DevTools work better for you by creating new keyboard shortcuts for any action in the DevTools.  -->  

Agora você pode personalizar o atalho do teclado para qualquer ação no DevTools.  Para editar um atalho de teclado, conclua as seguintes ações.  

1.  Abra o DevTools e escolha **Atalhos**  >  **de Configurações.**  
1.  Escolha a ação que você deseja personalizar.  
1.  Escolha Editar \(![Editar ícone de atalho do teclado](../../media/2021/02/edit-keyboard-shortcut-icon.msft.png)\) ícone.  
1.  Selecione as chaves que você deseja vincular à ação.  
1.  Escolha a marca de seleção \(![Ícone de Atalho de Teclado de Marca de Verificação](../../media/2021/02/checkmark-keyboard-shortcut-icon.msft.png)\) ícone.  
    
Para obter mais informações sobre como personalizar e editar atalhos, navegue até Personalizar atalhos de teclado [no Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].  Para revisar atualizações em tempo real sobre esse recurso no projeto de código aberto do Chromium, navegue até o Problema [174309][CR174309].  

:::image type="complex" source="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png" alt-text="Personalizar atalhos de teclado nas Configurações de DevTools em Atalhos com um atalho no modo de edição" lightbox="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png":::
   Personalizar atalhos de teclado nas [Configurações de DevTools][DevtoolsCustomizeIndexSettings] em Atalhos com um atalho no modo de edição  
:::image-end:::  

## <a name="microsoft-edge-devtools-for-visual-studio-code-extension-update-114"></a>Microsoft Edge DevTools para Visual Studio atualização de extensão de código 1.1.4  

<!-- Title: Edge Devtools for Visual Studio code extension update 1.1.4  -->  
<!-- Subtitle: Latest changes including a favicon is displayed next to each of the instances and console messages from the browser are displayed in the console of Visual Studio Code.  -->  

O [Microsoft Edge Developer Tools for Visual Studio Code extension][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] version 1.1.4 for Microsoft Visual Studio Code agora exibe um favicon ao lado de cada uma das instâncias do DevTools.  As mensagens de console do Microsoft Edge agora são exibidas no **Console de DevTools** em **Saída** do Microsoft Visual Studio Code.  O Microsoft Visual Studio Code atualiza as extensões automaticamente.  Para atualizar manualmente para a versão 1.1.4, navegue até [Atualizar uma extensão manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  Você pode registrar problemas e contribuir para a extensão no repositório [do GitHub vscode-edge-devtools.][GithubMicrosoftVscodeEdgeDevtools]  

:::row:::
   :::column span="":::
      A figura a seguir exibe mensagens de uma página da Web de exemplo registrada na **ferramenta Console** no Microsoft Edge.  
   :::column-end:::
   :::column span="":::
      A figura a seguir exibe as mesmas mensagens da página da Web de exemplo registrada no **Console de DevTools** em **Saída** do Microsoft Visual Studio Code.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png" alt-text="Exibir uma mensagem no Console no Microsoft Edge DevTools" lightbox="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png":::
         Exibir uma mensagem no Console no Microsoft Edge DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png" alt-text="Exibir a mesma mensagem no Console de DevTools em Saída do Microsoft Visual Studio Code" lightbox="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png":::
         Exibir a mesma mensagem no Console de DevTools em Saída do Microsoft Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-flexbox-editing-with-visual-flexbox-editor-and-multiple-overlays"></a>Edição de flexbox CSS aprimorada com editor de flexbox visual e várias sobreposições  

<!-- Title: Try different CSS flexbox layouts with the visual flexbox editor  -->  
<!-- Subtitle: In the Styles pane, choose the icon that appears next to display: flex to try different layout properties for flex containers.  -->  

O DevTools agora tem ferramentas de depuração de área de flexbox CSS dedicadas.  Se o estilo ou CSS for aplicado a um elemento HTML, um ícone será exibido ao lado desse `display: flex` `display: inline-flex` elemento na ferramenta `flex` **Elements.**  Para exibir \(ou ocultar\) uma sobreposição flexível na página da Web, escolha o `flex` ícone.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problemas [1166710][CR1166710] e [1175699][CR1175699].  

:::row:::
   :::column span="":::
      Para abrir o editor **do Flexbox,** navegue até o painel **Estilos** e escolha o novo ícone ao lado `display: flex` do ou `display: inline-flex` estilo.  O **editor do Flexbox** fornece uma maneira rápida de editar as propriedades do flexbox.  
   :::column-end:::
   :::column span="":::
      Além disso, a **seção Flexbox** no **painel Layout** exibe todos os elementos de flexbox na página da Web.  Você pode alternar a sobreposição de cada elemento.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-styles-display-flex-window.msft.png" alt-text="Ferramentas de depuração de flexbox CSS" lightbox="../../media/2021/02/elements-styles-display-flex-window.msft.png":::
         Ferramentas de depuração de flexbox CSS  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png" alt-text="Seção Flexbox no painel Layout" lightbox="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png":::
         **Seção Flexbox** no **painel Layout**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="keyboard-navigation-improvements-for-network-requests"></a>Melhorias de navegação de teclado para solicitações de rede  

<!-- Title: Navigate the request initiator chain in the Network tool with the keyboard  -->  
<!-- Subtitle: The Initiator pane may now be expanded or collapsed with the arrow keys.  -->  

Anteriormente, você não era capaz de expandir ou fechar a cadeia **** de solicitações usando as teclas de seta no teclado no painel Iniciador, ao contrário do DOM na **ferramenta Elements.**  Quando uma solicitação de **** rede é selecionada na ferramenta Rede, o painel **Iniciador** exibe a cadeia de solicitações que iniciou a solicitação selecionada no momento.  

No Microsoft Edge versão 90, você pode expandir ou fechar a cadeia de solicitações usando as teclas de seta no teclado no painel **Iniciador.**  A solicitação de rede focada na cadeia também agora está realçada.  Para saber mais sobre iniciadores na ferramenta **Rede,** navegue até [Exibir iniciadores e dependências.][DevtoolsNetworkReferenceDisplayInitiatorsDependencies]  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problemas [1158276][CR1158276] e [1160637][CR1160637].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain.msft.png" alt-text="Escolha uma solicitação de rede e escolha o painel Iniciador" lightbox="../../media/2021/02/network-request-initiator-chain.msft.png":::
         Escolha uma solicitação de rede e escolha o painel **Iniciador**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png" alt-text="Expanda ou colapse a cadeia de iniciador de solicitação e siga a linha realçada" lightbox="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png":::
         Expanda ou colapse a cadeia de iniciador de solicitação e siga a linha realçada  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="filtering-in-the-console-is-more-consistent"></a>A filtragem no Console é mais consistente  

<!-- Title: Console improvements make filtering more consistent  -->  
<!-- Subtitle: The Log Levels dropdown is more clearly disabled when using filters in the Console sidebar.  -->  

Enquanto você filtra com a Barra Lateral do [Console,][DevtoolsConsoleReferenceOpenConsoleSidebar]os filtros na lista suspenso Níveis de [Log][DevtoolsConsoleReferenceFilterByLogLevel] não estão disponíveis.  Anteriormente, o **menu suspenso Níveis** de Log realçava quando você pairava sobre ele, mesmo enquanto um filtro da Barra Lateral do **Console** era escolhido.  No Microsoft Edge versão 90, o menu suspenso Níveis de **Log** não é mais realçado quando você passar o mouse nele enquanto um filtro da **Barra Lateral** do Console é escolhido.  Para saber mais sobre a filtragem no **Console,** navegue até [Filtrar Mensagens][DevtoolsConsoleReferenceFilterMessages].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-old.msft.png" alt-text="Anteriormente, se você abrir a barra lateral do Console e passar o mouse nos níveis padrão, ela foi realçada" lightbox="../../media/2021/02/console-sidebar-default-levels-old.msft.png":::
         Anteriormente, se você abrir a **barra lateral do Console** e passar o mouse nos níveis **padrão,** ela foi realçada  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-new.msft.png" alt-text="A partir do Microsoft Edge 90, se você escolher a barra lateral do Console e passar o mouse nos níveis padrão, ela não será realçada" lightbox="../../media/2021/02/console-sidebar-default-levels-new.msft.png":::
         A partir do Microsoft Edge 90, se você escolher a **barra lateral do Console** e passar o mouse nos níveis padrão, ela não será realçada ****  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a>Anúncios do projeto Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="the-console-now-escapes-double-quote-characters"></a>O Console agora escapou de caracteres de aspas duplas  

Anteriormente, **o Console** não tinha caracteres válidos de aspas duplas \( `"` \) em cadeias de caracteres JavaScript.  A partir da versão 90 do Microsoft Edge, o **Console** saída cadeias de caracteres JavaScript usando caracteres de aspas duplas \( `"` \).  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1178530][CR1178530].  

:::image type="complex" source="../../media/2021/02/console-string-formatted-double-quotes.msft.png" alt-text="O Console saídas cadeias de caracteres JavaScript usando caracteres de aspas duplas de escape (&#0022;)" lightbox="../../media/2021/02/console-string-formatted-double-quotes.msft.png":::
   O **Console saídas** cadeias de caracteres JavaScript usando caracteres de aspas duplas \( `"` \)  
:::image-end:::  

### <a name="emulate-the-css-color-gamut-media-feature"></a>Emular o recurso de mídia css color-gamut  

A [consulta de][ChromestatusFeature5354410980933632] mídia de gama de cores emula o intervalo aproximado de cores com suporte do navegador e do dispositivo que você está testando.  O menu suspenso em Emular o recurso de **mídia CSS color-gamut** contém espaços de cores que o DevTools pode emular.  Por exemplo, para disparar uma `color-gamut: p3` consulta de mídia, escolha **color-gamut: p3** no menu suspenso.  

Para emular o recurso de mídia css color-gamut, conclua as seguintes ações.  

1.  Abra o [Menu de Comando][DevtoolsCommandMenuIndex].  
1.  Digite `Rendering`.  
1.  Execute o **comando Mostrar Renderização.**  
1.  Navegue **até Emular color-gamut** do recurso de mídia CSS e escolha uma opção.  

Para saber mais sobre o `color-gamut` recurso, navegue até [Color Display Quality: the 'color-gamut' feature][CsswgDraftsMediaqueries4ColorGamut].  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1073887][CR1073887].  

:::image type="complex" source="../../media/2021/02/rendering-css-color-gamut.msft.png" alt-text="Emular o recurso de mídia css color-gamut" lightbox="../../media/2021/02/rendering-css-color-gamut.msft.png":::
   Emular o recurso de mídia css color-gamut  
:::image-end:::  

### <a name="improved-progressive-web-apps-tooling"></a>Ferramenta progressiva aprimorada de Aplicativos Web  

#### <a name="pwa-installability-warning-in-the-console"></a>Aviso de capacidade de instalação do PWA no Console  

O **Console** agora exibe uma mensagem de aviso de capacidade de instalação do [PWA (Progressive Web Apps)][ProgressiveWebAppsIndex] mais detalhada com um link para Melhorar a detecção de suporte [offline do Progressive Web App.][ChromeDeveloperBlogImprovedPwaOfflineDetection]  

:::image type="complex" source="../../media/2021/02/console-pwa-installability.msft.png" alt-text="Aviso de capacidade de instalação do PWA na ferramenta Console" lightbox="../../media/2021/02/console-pwa-installability.msft.png":::
   Aviso de capacidade de instalação do PWA na **ferramenta Console**  
:::image-end:::  

#### <a name="pwa-description-length-warning-in-the-manifest-pane"></a>Aviso de comprimento da descrição do PWA no painel Manifesto

O **painel** Manifesto agora exibirá uma mensagem de aviso se a descrição do manifesto exceder 324 caracteres.  

:::image type="complex" source="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png" alt-text="Aviso de truncado de descrição do PWA" lightbox="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png":::
   Aviso de truncado de descrição do PWA  
:::image-end:::  

Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problemas [965802][CR965802], [1146450][CR1146450]e [1169689][CR1169689].  

### <a name="new-remote-address-space-column-in-the-network-tool"></a>Nova coluna Espaço de Endereço Remoto na ferramenta Rede  

<!-- does not work in canary 90.0.813.0 -->  
A nova **coluna Espaço de Endereço Remoto** exibe o espaço de endereço IP de rede de cada recurso de rede.  Para exibir a nova coluna Espaço de Endereço Remoto, conclua as seguintes ações.  

1.  Navegue até **a ferramenta Rede.**  
1.  Na tabela Solicitações, passe o mouse na linha do header e abra o menu contextual \(clique com o botão direito do mouse\).  Para saber como adicionar ou remover colunas da tabela Solicitações, navegue até [Adicionar ou remover colunas][DevtoolsNetworkReferenceAddRemoveColumns].  
1.  Escolha **Espaço de Endereço Remoto**.  
    
A tabela Solicitações agora exibe uma nova coluna com o header chamado **Espaço de Endereço Remoto**.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1128885][CR1128885].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png" alt-text="No menu contextual, escolha Espaço de Endereço Remoto" lightbox="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png":::
         No menu contextual, escolha o **Espaço de Endereço Remoto**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-remote-address-space.msft.png" alt-text="A tabela Solicitações agora exibe a coluna Espaço de Endereço Remoto" lightbox="../../media/2021/02/network-requests-remote-address-space.msft.png":::
         A tabela Solicitações agora exibe a coluna **Espaço de Endereço** Remoto :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-allowed-and-disallowed-features-in-the-frame-details-view"></a>Exibir recursos permitidos e não permitidos na exibição De detalhes do quadro  

A exibição de detalhes do Quadro agora exibe uma lista de recursos permitidos e não permitidos do navegador [controlados][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]pela Política de Permissões .  Política de Permissões é uma API de plataforma da Web que permite \(ou bloqueia\) uma página da Web o uso de recursos do navegador em um quadro individual ou em iframes que ele incorpora.  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1158827][CR1158827].  

:::image type="complex" source="../../media/2021/02/application-frames-permissions-policy.msft.png" alt-text="Recursos permitidos e não permitidos com base na Política de Permissão" lightbox="../../media/2021/02/application-frames-permissions-policy.msft.png":::
   Recursos permitidos e não permitidos com base na Política de Permissão  
:::image-end:::  

### <a name="new-sameparty-column-in-the-cookies-pane"></a>Nova coluna SameParty no painel Cookies  

O **painel Cookies** na ferramenta **Application** agora exibe o atributo para `SameParty` cada cookie.  O `SameParty` atributo é um novo atributo booliano para indicar se um cookie está incluído em solicitações para origens dos mesmos Conjuntos de Primeira [Parte][GithubPrivacycgFirstPartySets].  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1161427][CR1161427].  

:::image type="complex" source="../../media/2021/02/application-storage-cookies-sameparty.msft.png" alt-text="Coluna SameParty no painel Cookies" lightbox="../../media/2021/02/application-storage-cookies-sameparty.msft.png":::
   **Coluna SameParty** no painel **Cookies**  
:::image-end:::  

### <a name="fndisplayname-property-in-the-console-tool-is-now-deprecated"></a>A propriedade fn.displayName na ferramenta Console agora está preterida  

Anteriormente, a propriedade permitia controlar nomes de depuração para funções que eram exibidas em e em Rastreamentos de `fn.displayName` `error.stack` pilha do DevTools.  A partir da versão 90 do Microsoft Edge, a propriedade agora é preterida e substituída `fn.displayName` pela `fn.name` propriedade.  Use o método `Object.defineProperty` padrão para definir a `fn.name` propriedade.  Para saber mais `fn.name` sobre , navegue [até Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [1177685][CR1177685].  

:::image type="complex" source="../../media/2021/02/console-display-name-name.msft.png" alt-text="Um exemplo da propriedade fn.name para controlar nomes de depuração para funções" lightbox="../../media/2021/02/console-display-name-name.msft.png":::
   Um exemplo da propriedade `fn.name` para controlar nomes de depuração para funções  
:::image-end:::  

### <a name="full-accessibility-tree-view-in-the-elements-tool"></a>Exibição de árvore de acessibilidade completa na ferramenta Elements  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Este experimento fornece uma **exibição completa de árvore de** acessibilidade na ferramenta **Elements.**  O [painel Acessibilidade][DevtoolsAccessibilityReferenceTheAccessibilityPane] fornece uma exibição parcial de árvore de acessibilidade, que exibe a cadeia ancestral direta do nó raiz para o nó inspecionado.  
Depois de ativar esse experimento e recarregar o DevTools, escolha um dos seguintes botões para alternar a exibição na ferramenta Elementos para todos os elementos na página da Web.  

*   Para exibir a exibição de árvore de acessibilidade completa, escolha a **exibição Alternar**para Árvore de Acessibilidade.  
*   Para exibir a exibição de árvore DOM, escolha a **exibição Alternar para Árvore DOM**.  
    
Para ativar o experimento, [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] navegue até Ativar recursos experimentais e escolha a caixa de seleção ao lado de Habilitar o modo de exibição de árvore de acessibilidade total no **painel Elementos.**  Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até o Problema [887173][CR887173].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png" alt-text="Exibir o exibição de árvore DOM" lightbox="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png":::
         Exibir o **exibição DOM**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png" alt-text="Exibir a exibição de árvore de acessibilidade completa" lightbox="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png":::
         Exibir o **exibição árvore de acessibilidade total**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows, Linux ou macOS, considere usar os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Como entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsAccessibilityReferenceTheAccessibilityPane]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#the-accessibility-pane "Painel Acessibilidade - Referência de acessibilidade | Microsoft Docs"  
[DevtoolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Execute comandos com o menu de comando Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterByLogLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrar por nível de log - referência de console | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterMessages]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-messages "Filtrar mensagens - Console Reference | Microsoft Docs"  
[DevtoolsConsoleReferenceOpenConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/console/reference#open-the-console-sidebar "Abra a barra lateral do console - referência do console | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalizar atalhos de teclado no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexEnablePlusButtonTabMenusToOpenMoreTools]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#enable--button-tab-menus-to-open-more-tools "Habilitar + menus de guia de botão para abrir mais ferramentas - Recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#turn-on-experimental-features "Ativar recursos experimentais - Recursos experimentais | Microsoft Docs"  
[DevtoolsNetworkReferenceAddRemoveColumns]: /microsoft-edge/devtools-guide-chromium/network/reference#add-or-remove-columns "Adicionar ou remover colunas - Referência de Análise de Rede | Microsoft Docs"  
[DevtoolsNetworkReferenceDisplayInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#display-initiators-and-dependencies "Exibir iniciadores e dependências - Referência de Análise de Rede | Microsoft Docs"  

[ProgressiveWebAppsIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Visão geral progressiva dos Aplicativos Web no Windows | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de visualização do Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Atualizar uma extensão manualmente - Extensão do Marketplace | Visual Studio Código"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio Marketplace"  

[ChromeDeveloperBlogImprovedPwaOfflineDetection]: https://developer.chrome.com/blog/improved-pwa-offline-detection "Melhorar a detecção de suporte offline do Aplicativo Web Progressivo | Desenvolvedores do Chrome"  

[ChromestatusFeature5354410980933632]: https://www.chromestatus.com/feature/5354410980933632 "color-gamut media query | Status da plataforma Chrome"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs do Chromium"  
[CR174309]: https://crbug.com/174309 "Problema 174309: DevTools: permitir a personalização de atalhos de teclado/associações de chave | Erros de Chromium"  
[CR887173]: https://crbug.com/887173 "Problema 887173: DevTools: Inspeção completa de árvore de acessibilidade | Bugs do Chromium"  
[CR965802]: https://crbug.com/965802 "Problema 965802: Implemente a detecção de recursos offline mais precisa do trabalhador do serviço | Bugs do Chromium"  
[CR1073887]: https://crbug.com/1073887 "Problema 1073887: DevTools: @media (color-gamut: ...) colorspace | Bugs do Chromium"  
[CR1128885]: https://crbug.com/1128885 "Problema 1128885: Suporte a DevTools para CORS-RFC1918 | Bugs do Chromium"  
[CR1146450]: https://crbug.com/1146450 "Problema 1146450: [Android] Implementar instalação de planilha inferior | Bugs do Chromium"  
[CR1158276]: https://crbug.com/1158276 "Problema 1158276: Não é possível expandir/contrair o painel 'Solicitar cadeia de iniciadores' usando teclas de seta na seção 'Rede' do DevTools | Bugs do Chromium"  
[CR1158827]: https://crbug.com/1158827 "Problema 1158827: [Política de Permissões] Implementar o suporte ao devtool para políticas de permissões | Bugs do Chromium"  
[CR1160637]: https://crbug.com/1160637 "Problema 1160637: o foco em 'Cadeia de iniciadores de solicitação' é visto incompleto na seção 'Rede' da janela 'Ferramentas de Dev' | Bugs de cromo"  
[CR1161427]: https://crbug.com/1161427 "Problema 1161427: &#9730; suporte à depuração de atributo de cookie SameParty no DevTools | Bugs do Chromium"  
[CR1166710]: https://crbug.com/1166710 "Problema 1166710: ativar o experimento de ferramentas de flexbox por padrão | Bugs do Chromium"  
[CR1169689]: https://crbug.com/1169689 "Problema 1169689: a planilha inferior de instalação do PWA não deve apresentar categorias | Bugs do Chromium"  
[CR1175699]: https://crbug.com/1175699 "Problema 1175699: editor do Flexbox | Bugs do Chromium"  
[CR1177685]: https://crbug.com/1177685 "Problema 1177685: Remover suporte não padrão fn.displayName | Bugs do Chromium"  
[CR1178530]: https://crbug.com/1178530 "Problema 1178530: Console não escapa de doublequotes ao imprimir cadeias de caracteres | Bugs do Chromium"  

[CsswgDraftsMediaqueries4ColorGamut]: https://drafts.csswg.org/mediaqueries-4#color-gamut "Qualidade de exibição de cor: o recurso "color-gamut" | Rascunhos do Editor do Grupo de Trabalho CSS"  

[GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DevTools/FocusMode/explainer.md "DevTools: Interface do Usuário do Modo de Foco - MicrosoftEdge/MSEdgeExplainers | GitHub"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubPrivacycgFirstPartySets]: https://github.com/privacycg/first-party-sets "Conjuntos de primeira | GitHub"  

[GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Explicador de Política de Permissões | GitHub"  

[MdnJavascriptReferenceGlobalObjectsFunctionName]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/name "Function.name | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/updates/2021/02/devtools/index) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
