---
description: Suporte de depuração para CSS Flexbox, tela de alerta de desempenho na página da Web, atualizações de ferramenta de problemas e muito mais
title: O que há de novo no DevTools (Microsoft Edge 90)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.localizationpriority: high
ms.openlocfilehash: a6682043166909bf75a875b72058cc9839c5b43b
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564844"
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
# <a name="whats-new-in-devtools-microsoft-edge-90"></a>O que há de novo no DevTools (Microsoft Edge 90)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="group-tools-together-in-focus-mode"></a>Ferramentas de grupo juntas no Modo de Foco  

<!-- Title: Grouping the tools in Focus Mode  -->  
<!-- Subtitle: Organize your favorite tools into groups with the new Focus Mode UI.  -->  

O Modo de Foco é uma interface experimental que permite agrupar diferentes ferramentas com base em seus próprios cenários de depuração.  A nova **Barra de Atividades** exibida à esquerda inclui grupos de ferramentas predefinidos, como **Layout** e **Depuração**.  Para personalizar cada grupo de ferramentas, feche as ferramentas com o ícone **Fechar** \(`X`\) ou adicione novas ferramentas com o ícone **Mais ferramentas** \(`+`\).  

Para ativar o experimento, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] e escolha as caixas de seleção ao lado de **Modo de foco e Dicas de ferramentas do DevTools** e **Habilitar os menus da guia do botão + para abrir mais ferramentas**.  Para obter mais informações sobre este recurso ou para comentar com perguntas e ideias, navegue até [DevTools: Interface do usuário Modo de Foco][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode.msft.png" alt-text="Exibir a Barra de Atividades" lightbox="../../media/2021/02/focus-mode.msft.png":::
   Exibir a **Barra de Atividades**  
:::image-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a>Saiba mais sobre o DevTools com dicas de ferramentas informativas  

<!-- Title: DevTools Tooltips  -->  
<!-- Subtitle: Learn more about how to use DevTools with informative DevTools tooltips.  -->  

O recurso de Dicas de Ferramentas do DevTools ajuda você a aprender sobre todas as diferentes ferramentas e painéis.  Escolha o ícone Ajuda \(`?`\) na parte inferior da **Barra de Atividades** para alternar as dicas de ferramentas no DevTools.  Quando as dicas de ferramentas estiverem habilitadas, passe o mouse sobre cada região delineada do DevTools para saber mais sobre como usar a ferramenta.  Para ativar o experimento, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] e escolha as caixas de seleção ao lado de **Modo de foco e Dicas de ferramentas do DevTools** e **Habilitar os menus da guia do botão + para abrir mais ferramentas**.  Para obter mais informações sobre este recurso ou para comentar com perguntas e ideias, navegue até [DevTools: Interface do usuário Modo de Foco][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode-and-tooltips-help.msft.png" alt-text="Escolha o ícone de Ajuda (?) Na Barra de Atividades para exibir as dicas de ferramentas" lightbox="../../media/2021/02/focus-mode-and-tooltips-help.msft.png":::
   Escolha o ícone Ajuda \(`?`\) na **Barra de Atividades** para exibir dicas de ferramenta  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a>Personalize os atalhos do teclado em Configurações  

<!-- Title: Change keyboard shortcuts in Settings  -->  
<!-- TODO:  Rachel's feedback is about the fact that this experimental feature is turned on by default, may have separate section in What's New for experimental features)  -->  
<!-- Subtitle: Make DevTools work better for you by creating new keyboard shortcuts for any action in the DevTools.  -->  

Agora você pode personalizar o atalho de teclado para qualquer ação no DevTools.  Para editar um atalho de teclado, execute as seguintes ações.  

1.  Abra o DevTools e escolha **Atalhos** > **de Configurações**.  
1.  Escolha a ação que você deseja personalizar.  
1.  Escolha Editar \(![Editar o ícone de Atalho de Teclado](../../media/2021/02/edit-keyboard-shortcut-icon.msft.png)\) ícone.  
1.  Selecione as teclas que você deseja vincular à ação.  
1.  Escolha a marca de seleção \(![Ícone de Atalho de Teclado marca de seleção](../../media/2021/02/checkmark-keyboard-shortcut-icon.msft.png)\) ícone.  
    
Para obter mais informações sobre como personalizar e editar atalhos, navegue até [Personalizar atalhos de teclado no Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].  Para revisar as atualizações em tempo real desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [174309][CR174309].  

:::image type="complex" source="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png" alt-text="Personalize os atalhos de teclado nas Configurações do DevTools em Atalhos com um atalho no modo de edição" lightbox="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png":::
   Personalize os atalhos de teclado nas [Configurações do DevTools][DevtoolsCustomizeIndexSettings] em Atalhos com um atalho no modo de edição  
:::image-end:::  

## <a name="microsoft-edge-devtools-for-visual-studio-code-extension-update-114"></a>Atualização 1.1.4 da extensão do Microsoft Edge DevTools para o Visual Studio Code  

<!-- Title: Edge Devtools for Visual Studio code extension update 1.1.4  -->  
<!-- Subtitle: Latest changes including a favicon is displayed next to each of the instances and console messages from the browser are displayed in the console of Visual Studio Code.  -->  

O [Microsoft Edge Developer Tools para o Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extensão 1.1.4 para o Microsoft Visual Studio Code agora exibe um favicon próximo a cada uma das instâncias do DevTools.  As mensagens do console do Microsoft Edge agora são exibidas no **Console do DevTools** em **Saída** do Microsoft Visual Studio Code.  O Microsoft Visual Studio Code atualiza as extensões automaticamente.  Para atualizar manualmente para a versão 1.1.4, navegue até [Atualizar uma extensão manualmente][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].  Você pode registrar problemas e contribuir para a extensão no repositório do GitHub [vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools].  

:::row:::
   :::column span="":::
      A figura a seguir exibe as mensagens de uma página da Web de exemplo registrada na ferramenta **Console** no Microsoft Edge.  
   :::column-end:::
   :::column span="":::
      A figura a seguir exibe as mesmas mensagens da página da Web de exemplo registrada no **Console do DevTools** em **Saída** do Microsoft Visual Studio Code.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png" alt-text="Exibir uma mensagem no Console do Microsoft Edge DevTools" lightbox="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png":::
         Exibir uma mensagem no Console do Microsoft Edge DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png" alt-text="Exibir a mesma mensagem no Console do DevTools em Saída do Microsoft Visual Studio Code" lightbox="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png":::
         Exibir a mesma mensagem no Console do DevTools em Saída do Microsoft Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-flexbox-editing-with-visual-flexbox-editor-and-multiple-overlays"></a>Edição com CSS flexbox aprimorada com editor visual flexbox e múltiplas sobreposições  

<!-- Title: Try different CSS flexbox layouts with the visual flexbox editor  -->  
<!-- Subtitle: In the Styles pane, choose the icon that appears next to display: flex to try different layout properties for flex containers.  -->  

O DevTools agora possui ferramentas de depuração do CSS flexbox dedicadas.  Se o `display: flex` ou `display: inline-flex` estilo CSS for aplicado a um elemento HTML, um `flex` ícone será exibido próximo a esse elemento na ferramenta **Elementos**.  Para exibir \(ou ocultar\) uma sobreposição flexível na página da Web, escolha o ícone`flex`.  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até os Problemas [1166710][CR1166710] e [1175699][CR1175699].  

:::row:::
   :::column span="":::
      Para abrir o editor do**Flexbox**, navegue até o painel **Estilos** e escolha o novo ícone ao lado do `display: flex` ou `display: inline-flex` estilo.  O editor do **Flexbox** fornece uma maneira rápida de editar as propriedades do flexbox.  
   :::column-end:::
   :::column span="":::
      Além disso, a seção do **Flexbox** no painel **Layout** exibe todos os elementos do flexbox na página da Web.  Você pode alternar a sobreposição de cada elemento.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-styles-display-flex-window.msft.png" alt-text="Ferramentas de depuração do CSS flexbox" lightbox="../../media/2021/02/elements-styles-display-flex-window.msft.png":::
         Ferramentas de depuração do CSS flexbox  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png" alt-text="Seção do Flexbox no painel Layout" lightbox="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png":::
         Seção do **Flexbox** no painel **Layout**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="keyboard-navigation-improvements-for-network-requests"></a>Melhorias na navegação do teclado para solicitações de rede  

<!-- Title: Navigate the request initiator chain in the Network tool with the keyboard  -->  
<!-- Subtitle: The Initiator pane may now be expanded or collapsed with the arrow keys.  -->  

Anteriormente, você não conseguia expandir ou recolher a cadeia de solicitações usando as teclas de direção do teclado no painel **Iniciador**, ao contrário do DOM na ferramenta **Elementos**.  Quando uma solicitação de rede é selecionada na ferramenta **Rede**, o painel **Iniciador** exibe a cadeia de solicitações que iniciou a solicitação atualmente selecionada.  

No Microsoft Edge versão 90, você pode expandir ou recolher a cadeia de solicitações usando as teclas de direção no teclado no painel **Iniciador**.  A solicitação de rede focada na rede também está agora em destaque.  Para saber mais sobre os iniciadores na ferramenta **Rede**, navegue até [Exibir iniciadores e dependências][DevtoolsNetworkReferenceDisplayInitiatorsDependencies].  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até os Problemas [1158276][CR1158276] e [1160637][CR1160637].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain.msft.png" alt-text="Escolha uma solicitação de Rede e escolha o painel Iniciador" lightbox="../../media/2021/02/network-request-initiator-chain.msft.png":::
         Escolha uma solicitação de Rede e escolha o painel **Iniciador**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png" alt-text="Expanda ou recolha a solicitação de cadeia de iniciador e siga a linha destacada" lightbox="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png":::
         Expanda ou recolha a solicitação de cadeia de iniciador e siga a linha destacada  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="filtering-in-the-console-is-more-consistent"></a>A filtragem no Console é mais consistente  

<!-- Title: Console improvements make filtering more consistent  -->  
<!-- Subtitle: The Log Levels dropdown is more clearly disabled when using filters in the Console sidebar.  -->  

Enquanto você filtra com a [Barra Lateral do Console][DevtoolsConsoleReferenceOpenConsoleSidebar], os filtros na lista suspensa [Níveis de Registro][DevtoolsConsoleReferenceFilterByLogLevel] não estão disponíveis.  Anteriormente, a lista suspensa **Níveis de Registro** era destacada quando você passava o mouse sobre ela, mesmo quando um filtro da **Barra Lateral do Console** era escolhido.  No Microsoft Edge versão 90, a lista suspensa **Níveis de Registro** não é mais realçada quando você passa o mouse sobre ela enquanto um filtro da **Barra Lateral do Console** é escolhido.  Para saber mais sobre a filtragem no **Console**, navegue até [Filtrar Mensagens][DevtoolsConsoleReferenceFilterMessages].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-old.msft.png" alt-text="Anteriormente, se você abrisse a barra lateral do Console e passasse o mouse sobre os níveis Padrão, ele ficava realçado" lightbox="../../media/2021/02/console-sidebar-default-levels-old.msft.png":::
         Anteriormente, se você abrisse a **barra lateral do Console** e passasse o mouse sobre os **níveis Padrão**, ele ficava realçado  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-new.msft.png" alt-text="A partir do Microsoft Edge 90, se você escolhesse a barra lateral do Console e passasse o mouse sobre os níveis padrão, ele não será realçada" lightbox="../../media/2021/02/console-sidebar-default-levels-new.msft.png":::
         A partir do Microsoft Edge 90, se você escolhesse a **barra lateral do Console** e passasse o mouse sobre os **níveis padrão**, ele não será realçada  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a>Anúncios do projeto Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="the-console-now-escapes-double-quote-characters"></a>O console agora escapa de caracteres de aspas duplas  

Anteriormente, o **Console** não produzia caracteres de aspas duplas \(`"`\) válidos em strings do JavaScript.  A partir do Microsoft Edge versão 90, o **Console** gera strings do JavaScript usando caracteres de aspas duplas escapadas \ (`"`\).  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [1178530][CR1178530].  

:::image type="complex" source="../../media/2021/02/console-string-formatted-double-quotes.msft.png" alt-text="O Console gera strings do JavaScript usando caracteres de aspas duplas escapadas (&#0022;)" lightbox="../../media/2021/02/console-string-formatted-double-quotes.msft.png":::
   O **Console** gera strings do JavaScript usando caracteres de aspas duplas escapadas \(`"`\)  
:::image-end:::  

### <a name="emulate-the-css-color-gamut-media-feature"></a>Emular a gama de cores do recurso de mídia do CSS  

A consulta de mídia de [gama de cores][ChromestatusFeature5354410980933632] emula a faixa aproximada de cores suportada pelo navegador e o dispositivo que você está testando.  A lista suspensa em **Emular a gama de cores do recurso de mídia do CSS** contém espaços de cores que o DevTools pode emular.  Por exemplo, para acionar uma `color-gamut: p3` consulta de mídia, escolha **gama de cores: p3** no menu suspenso.  

Para emular a gama de cores do recurso de mídia do CSS, conclua as seguintes ações.  

1.  Abra o [Menu de Comando][DevtoolsCommandMenuIndex].  
1.  Digite `Rendering`.  
1.  Execute o comando **Mostrar Renderização**.  
1.  Navegue até **Emular a gama de cores do recurso de mídia do CSS** e escolha uma opção.  

Para saber mais sobre o recurso `color-gamut`, navegue até [Qualidade de Exibição de Cores: O recurso de 'gama de cores'][CsswgDraftsMediaqueries4ColorGamut].  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [1073887][CR1073887].  

:::image type="complex" source="../../media/2021/02/rendering-css-color-gamut.msft.png" alt-text="Emular a gama de cores do recurso de mídia do CSS" lightbox="../../media/2021/02/rendering-css-color-gamut.msft.png":::
   Emular a gama de cores do recurso de mídia do CSS  
:::image-end:::  

### <a name="improved-progressive-web-apps-tooling"></a>Ferramentas de Aplicativos Web progressivos  

#### <a name="pwa-installability-warning-in-the-console"></a>Aviso de instalabilidade do PWA no Console  

O **Console** agora exibe uma mensagem de aviso de instalação dos [Aplicativos Web Progressivos (PWA)][ProgressiveWebAppsIndex] mais detalhada com um link para [Aprimoramento da detecção de suporte offline do Aplicativo Web Progressivo][ChromeDeveloperBlogImprovedPwaOfflineDetection].  

:::image type="complex" source="../../media/2021/02/console-pwa-installability.msft.png" alt-text="Aviso de instalabilidade do PWA na ferramenta Console" lightbox="../../media/2021/02/console-pwa-installability.msft.png":::
   Aviso de instalabilidade do PWA na ferramenta **Console**  
:::image-end:::  

#### <a name="pwa-description-length-warning-in-the-manifest-pane"></a>Aviso de comprimento da descrição do PWA no painel Manifesto

O painel **Manifesto** agora exibe uma mensagem de aviso se a descrição do manifesto exceder 324 caracteres.  

:::image type="complex" source="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png" alt-text="Aviso de truncamento da descrição do PWA" lightbox="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png":::
   Aviso de truncamento da descrição do PWA  
:::image-end:::  

Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até os Problemas [965802][CR965802], [1146450][CR1146450] e [1169689][CR1169689].  

### <a name="new-remote-address-space-column-in-the-network-tool"></a>Nova coluna Espaço de Endereço Remoto na ferramenta Rede  

<!-- does not work in canary 90.0.813.0 -->  
A nova coluna **Espaço de Endereço Remoto** exibe o espaço de endereço do IP da rede de cada recurso da rede.  Para exibir a nova coluna Espaço de Endereço Remoto, conclua as seguintes ações.  

1.  Navegue até a ferramenta **Rede**.  
1.  Na tabela Solicitações, passe o mouse sobre a linha do cabeçalho e abra o menu contextual \(clique com o botão direito\).  Para saber como adicionar ou remover colunas da tabela Solicitações, navegue até [Adicionar ou remover colunas][DevtoolsNetworkReferenceAddRemoveColumns].  
1.  Escolha **Espaço de Endereço Remoto**.  
    
A tabela Solicitações agora exibe uma nova coluna com o cabeçalho denominado**Espaço de Endereço Remoto**.  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [1128885][CR1128885].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png" alt-text="No menu contextual, escolha Espaço de Endereço Remoto" lightbox="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png":::
         No menu contextual, escolha o **Espaço de Endereço Remoto**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-remote-address-space.msft.png" alt-text="A tabela Solicitações agora exibe a coluna Espaço de Endereço Remoto" lightbox="../../media/2021/02/network-requests-remote-address-space.msft.png":::
         A tabela Solicitações agora exibe a coluna **Espaço de Endereço Remoto** :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-allowed-and-disallowed-features-in-the-frame-details-view"></a>Exibir recursos permitidos e não permitidos na visualização de detalhes do Quadro  

A exibição de detalhes do Quadro agora exibe uma lista de recursos permitidos e não permitidos do navegador controlados pela [Política de Permissões][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer].  A Política de Permissões é uma API de plataforma Web que permite \(ou bloqueia\) o uso de recursos do navegador de uma página da Web em um quadro individual ou em iframes que ela incorpora.  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [1158827][CR1158827].  

:::image type="complex" source="../../media/2021/02/application-frames-permissions-policy.msft.png" alt-text="Recursos permitidos e não permitidos com base na Política de Permissão" lightbox="../../media/2021/02/application-frames-permissions-policy.msft.png":::
   Recursos permitidos e não permitidos com base na Política de Permissão  
:::image-end:::  

### <a name="new-sameparty-column-in-the-cookies-pane"></a>Nova coluna SameParty no painel Cookies  

O painel **Cookies** na ferramenta **Aplicativo** agora exibe o atributo `SameParty` para cada cookie.  O atributo `SameParty` é um novo atributo booleano para indicar se um cookie está incluído em solicitações para origens dos mesmos [Conjuntos de Primeira Parte][GithubPrivacycgFirstPartySets].  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [1161427][CR1161427].  

:::image type="complex" source="../../media/2021/02/application-storage-cookies-sameparty.msft.png" alt-text="Coluna SameParty no painel Cookies" lightbox="../../media/2021/02/application-storage-cookies-sameparty.msft.png":::
   Coluna **SameParty** no painel **Cookies**  
:::image-end:::  

### <a name="fndisplayname-property-in-the-console-tool-is-now-deprecated"></a>A propriedade fn.displayName na ferramenta Console agora está obsoleta  

Anteriormente, a `fn.displayName` propriedade permitia controlar os nomes de depuração das funções a serem exibidas em `error.stack`e nos rastreamentos de pilha do DevTools.  A partir do Microsoft Edge versão 90, a propriedade `fn.displayName` foi descontinuada e substituída pela propriedade `fn.name`.  Use o método padrão `Object.defineProperty` para definir a propriedade `fn.name`.  Para saber mais sobre `fn.name`, navegue até [Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [1177685][CR1177685].  

:::image type="complex" source="../../media/2021/02/console-display-name-name.msft.png" alt-text="Um exemplo da propriedade fn.name para controlar os nomes de depuração para funções" lightbox="../../media/2021/02/console-display-name-name.msft.png":::
   Um exemplo da propriedade `fn.name` para controlar os nomes de depuração para funções  
:::image-end:::  

### <a name="full-accessibility-tree-view-in-the-elements-tool"></a>Exibição em árvore de acessibilidade completa na ferramenta Elementos  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Este experimento fornece uma **exibição em árvore de acessibilidade completa** na ferramenta **Elementos**.  O painel [Acessibilidade][DevtoolsAccessibilityReferenceAccessibilityPanel] fornece uma visualização em árvore de acessibilidade parcial que exibe a cadeia ancestral direta do nó raiz ao nó inspecionado.  
Depois de ativar esse experimento e recarregar o DevTools, escolha um dos seguintes botões para alternar a exibição na ferramenta Elementos para todos os elementos na página da Web.  

*   Para exibir em árvore de acessibilidade completa, escolha **Alternar para o modo de exibição em Árvore de Acessibilidade**.  
*   Para exibir a exibição da árvore DOM, escolha **Alternar para exibição da árvore DOM**.  
    
Para ativar o experimento, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **Ativar visualização em árvore de acessibilidade completa no painel Elementos**.  Para examinar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até o Problema [887173][CR887173].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png" alt-text="Exibir o modo de exibição árvore DOM" lightbox="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png":::
         Exibir o **modo de exibição DOM**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png" alt-text="Exibir o modo de exibição em árvore de acessibilidade completa" lightbox="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png":::
         Exibir o modo de exibição em **Árvore de Acessibilidade Completa**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Baixar os canais de visualização do Microsoft Edge  

Se você está no Windows, Linux ou macOS, considere usar os [Microsoft Edge Preview Channels][MicrosoftEdgePreviewChannels] como o seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Como entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsAccessibilityReferenceAccessibilityPanel]: ../../../accessibility/reference.md#the-accessibility-panel "O painel de Acessibilidade - referência de acessibilidade | Microsoft Docs"  
[DevtoolsCommandMenuIndex]: ../../../command-menu/index.md "Executar comandos com o Menu de Comandos do Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterByLogLevel]: ../../../console/reference.md#filter-by-log-level "Filtrar por nível de registro - referência do console | Microsoft Docs"  
[DevtoolsConsoleReferenceFilterMessages]: ../../../console/reference.md#filter-messages "Filtrar mensagens - Referência do Console | Microsoft Docs"  
[DevtoolsConsoleReferenceOpenConsoleSidebar]: ../../../console/reference.md#open-the-console-sidebar "Abra a Barra Lateral do Console - referência do Console | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personalize os atalhos do teclado no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexEnablePlusButtonTabMenusToOpenMoreTools]: ../../../experimental-features/index.md#enable--button-tab-menus-to-open-more-tools "Ative os menus da guia do botão + para abrir mais ferramentas - Recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../../../experimental-features/index.md#turn-on-experimental-features "Ativar recursos experimentais - Recursos experimentais | Microsoft Docs"  
[DevtoolsNetworkReferenceAddRemoveColumns]: ../../../network/reference.md#add-or-remove-columns "Adicionar ou remover colunas - Referência de Análise de Rede | Microsoft Docs"  
[DevtoolsNetworkReferenceDisplayInitiatorsDependencies]: ../../../network/reference.md#display-initiators-and-dependencies "Exibir iniciadores e dependências - Referência de Análise de Rede | Microsoft Docs"  

[ProgressiveWebAppsIndex]: ../../../../progressive-web-apps-chromium/index.md "Visão geral progressiva dos Aplicativos Web no Windows | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de Visualização do Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Atualizar uma extensão manualmente - Marketplace da Extensão | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Ferramentas do Microsoft Edge para o Visual Studio Code | Visual Studio Marketplace"  

[ChromeDeveloperBlogImprovedPwaOfflineDetection]: https://developer.chrome.com/blog/improved-pwa-offline-detection "Melhorar a detecção de suporte offline do Aplicativo Web Progressivo | Desenvolvedores do Chrome"  

[ChromestatusFeature5354410980933632]: https://www.chromestatus.com/feature/5354410980933632 "consulta de mídia de gama de cores | Status da Plataforma Chrome"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs do Chromium"  
[CR174309]: https://crbug.com/174309 "Problema 174309: DevTools: permitir a personalização de atalhos de teclado/associações de chave | Bugs do Chromium"  
[CR887173]: https://crbug.com/887173 "Problema 887173: DevTools: Inspeção da Árvore de Acessibilidade Completa | Bugs do Chromium"  
[CR965802]: https://crbug.com/965802 "Problema 965802: Implementar a detecção de recursos offline mais precisa do trabalho de serviço | Bugs do Chromium"  
[CR1073887]: https://crbug.com/1073887 "Problema 1073887: DevTools: @media (Gama de cores: ...) emulação de espaço de cores | Bugs do Chromium"  
[CR1128885]: https://crbug.com/1128885 "Problema 1128885: Suporte do DevTools para CORS-RFC1918 | Bugs do Chromium"  
[CR1146450]: https://crbug.com/1146450 "Problema 1146450: [Android] Implementar instalações de folha inferior | Bugs do Chromium"  
[CR1158276]: https://crbug.com/1158276 "Problema 1158276: Não é possível expandir/contrair o painel 'Solicitação de cadeia de iniciador' usando as teclas de direção na seção 'Rede' do DevTools | Bugs do Chromium"  
[CR1158827]: https://crbug.com/1158827 "Problema 1158827: [Política de Permissões] Implementar suporte do devtool para políticas de permissões | Bugs do Chromium"  
[CR1160637]: https://crbug.com/1160637 "Problema 1160637: O Foco em 'Solicitação de cadeia de iniciador' é visto incompleto na seção 'Rede' da janela 'Dev Tools' | Bugs de cromo"  
[CR1161427]: https://crbug.com/1161427 "Problema 1161427: &#9730; suporte à depuração de atributo de cookie SameParty no DevTools | Bugs do Chromium"  
[CR1166710]: https://crbug.com/1166710 "Problema 1166710: Ativar o experimento de ferramentas do flexbox por padrão | Bugs do Chromium"  
[CR1169689]: https://crbug.com/1169689 "Problema 1169689: A folha inferior de instalação do PWA não deve apresentar categorias | Bugs do Chromium"  
[CR1175699]: https://crbug.com/1175699 "Problema 1175699: Editor do Flexbox | Bugs do Chromium"  
[CR1177685]: https://crbug.com/1177685 "Problema 1177685: Remover o suporte não-padronizado fn.displayName | Bugs do Chromium"  
[CR1178530]: https://crbug.com/1178530 "Problema 1178530: O console não evita aspas duplas ao imprimir as cadeias de caracteres | Bugs do Chromium"  

[CsswgDraftsMediaqueries4ColorGamut]: https://drafts.csswg.org/mediaqueries-4#color-gamut "Qualidade de Exibição de Cores: O recurso de 'gama de cores' | Rascunhos do Editor do Grupo de Trabalho do CSS"  

[GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DevTools/FocusMode/explainer.md "DevTools: Interface do Usuário do Modo de Foco - MicrosoftEdge/MSEdgeExplainers | GitHub"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubPrivacycgFirstPartySets]: https://github.com/privacycg/first-party-sets "Conjuntos de Primeira Parte | GitHub"  

[GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Explicação da Política de Permissões | GitHub"  

[MdnJavascriptReferenceGlobalObjectsFunctionName]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/name "Function.name | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developer.chrome.com/blog/new-in-devtools-90) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
