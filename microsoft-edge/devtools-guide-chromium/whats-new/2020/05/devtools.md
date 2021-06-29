---
description: Use o DevTools Windows modo de alto contraste, match keyboard shortcuts in the DevTools to Visual Studio Code, and more.
title: Novidades no DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: fabfa21abedb02bc83ec2bedbe3662f0d81c1bf9
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624805"
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
# <a name="whats-new-in-devtools-microsoft-edge-84"></a>Novidades no DevTools (Microsoft Edge 84)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Comunicados da equipe Microsoft Edge DevTools  

As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe Microsoft Edge DevTools.  Confira os comunicados para experimentar novos recursos no DevTools, Microsoft Visual Studio Extensões de Código e muito mais.  Para ficar atualizado sobre todos os recursos mais recentes e maiores em suas ferramentas de desenvolvedor, baixe os canais Microsoft Edge [de][MicrosoftEdgePreviewChannels] visualização e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].  

### <a name="use-the-devtools-in-windows-high-contrast-mode"></a>Use o DevTools Windows modo de alto contraste

Os Microsoft Edge DevTools agora são exibidos no modo de alto contraste quando Windows está no modo de alto contraste.  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="O Microsoft Edge DevTools no modo de alto contraste" lightbox="../../media/2020/05/high-contrast.msft.png":::
   O Microsoft Edge DevTools no modo de alto contraste  
:::image-end:::  

[Siga as instruções para ativar o modo de alto contraste em Windows][MicrosoftSupportWindows10HighContrastMode].  Para abrir o DevTools no Microsoft Edge, selecione `F12` ou `Ctrl` + `Shift` + `I` .  Os DevTools são exibidos no modo de alto contraste.  

> [!NOTE]
> O Microsoft Edge DevTools atualmente suporta o modo de alto contraste no Windows, mas não no macOS.  

Chromium problema [#1048378][CR1048378]  

### <a name="match-keyboard-shortcuts-in-the-devtools-to-visual-studio-code"></a>Corresponder atalhos de teclado no DevTools para Visual Studio Code  

Com seus [comentários](#getting-in-touch-with-microsoft-edge-devtools-team) e o Chromium de problemas [públicos,][CRIssuesList]a equipe Microsoft Edge DevTools aprendeu que você queria a capacidade de personalizar atalhos de teclado no DevTools.  No Microsoft Edge 84, agora você pode combinar atalhos de teclado no DevTools para Visual Studio Code , que é apenas um dos recursos em que [a][VisualStudioCodeMain]equipe está trabalhando para personalização de atalho.  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Corresponder atalhos de teclado no DevTools para Visual Studio Code" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   O Microsoft Edge DevTools no modo de alto contraste  
:::image-end:::  

Para experimentar o experimento, abra DevTools Configurações selecionando ou escolhendo o ícone Devtools Configurações ícone no canto superior direito do `?` ![ ](../../../media/settings-icon.msft.png) DevTools.  Navegue até **a seção Experimentos** e verifique **Habilitar configurações de atalhos de teclado personalizadas (requer recarga)**.  Agora recarregue o DevTools, abra Configurações novamente e navegue até **a seção Atalhos.**  

Escolha **DevTools (Padrão)** no menu suspenso Corresponder **atalhos** e selecione **Visual Studio Code**.  Os atalhos de teclado no DevTools agora corresponderão aos atalhos para ações equivalentes em Visual Studio Code.  

Por exemplo, o atalho do teclado para pausar ou continuar executando um script [em][VisualStudioCodeShortcuts] Visual Studio Code é `F5` .  Com a **predefinição DevTools (Padrão),** esse mesmo atalho no DevTools é, mas com a Visual Studio Code predefinida, esse atalho agora `F8` também é **** `F5` .  

O recurso está disponível no Microsoft Edge 84 como um experimento, portanto, compartilhe seus [comentários](#getting-in-touch-with-microsoft-edge-devtools-team) com a equipe!  

Chromium problema [#174309][CR174309]  

### <a name="remote-debug-surface-duo-emulators"></a>Emuladores do Surface Duo de depuração remota  

Agora você pode depurar remotamente o conteúdo da Web em execução no [emulador do Surface Duo][DualScreensAndroidEmulator] usando a potência total do [Microsoft Edge DevTools][DevtoolsIndex].  

Com o [emulador do Surface Duo,][DualScreensAndroidEmulator]você pode testar como o conteúdo da Web é renderizável em uma nova classe de dispositivos de tela dupla e dobrável.  O emulador executa o sistema operacional Android e fornece o [aplicativo Microsoft Edge Android][AndroidEdge].  Carregue o conteúdo da Web no [aplicativo Microsoft Edge e][AndroidEdge] depure-o com o Microsoft Edge [DevTools][DevtoolsIndex].  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="O Microsoft Edge aplicativo em execução no emulador do Surface Duo" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   O Microsoft Edge no emulador do Surface Duo  
:::image-end:::  

A página em uma instância da área de trabalho de Microsoft Edge mostra o `edge://inspect` **SurfaceDuoEmulator** com uma lista das guias abertas ou [PWAs][PwaIndex] que estão sendo executados no [emulador do Surface Duo.][DualScreensAndroidEmulator] [][DesktopEdge]  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="A edge://inspect exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   A página exibe uma lista das guias abertas no aplicativo Microsoft Edge `edge://inspect` em execução no emulador
:::image-end:::  

Escolha **inspecionar** a guia ou PWA que você deseja depurar para abrir o [Microsoft Edge DevTools][DevtoolsIndex].  Siga o guia passo a passo para depurar remotamente o conteúdo [da Web no emulador do Surface Duo.][DevtoolsRemoteDebugDuoEmulator]  

### <a name="resize-the-devtools-drawer-more-easily"></a>Resize a gaveta DevTools com mais facilidade  

No Microsoft Edge 83 ou anterior, você só foi capaz de ressarixar a [Gaveta de Devtools][DevtoolsDrawer] pairando na barra de ferramentas da Gaveta.  A Gaveta se comportava de forma diferente dos outros controles de ressarção para painéis no DevTools, onde você passar o mouse na borda do painel para ressilá-lo.  Escolha a imagem a seguir para exibir como o ressamento da Gaveta funcionou na versão 83 ou anterior do Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Resizing the DevTools Drawer in Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   Resizing the DevTools Drawer in Microsoft Edge 83
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

A partir Microsoft Edge 84, agora você pode ressarcionar a Gaveta pairando sobre a borda da Gaveta.  Essa alteração alinha o comportamento resizing the DevTools Drawer com a maneira como você resize outros painéis no DevTools.  Escolha a imagem a seguir para exibir o resizing em ação Microsoft Edge 84.  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Resizing the DevTools Drawer in Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   Resizing the DevTools Drawer in Microsoft Edge 84
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

Chromium problema [#1076112][CR1076112]  

### <a name="screencasting-navigation-buttons-display-focus"></a>Botões de navegação de screencasting exibem o foco  

Ao depurar remotamente um dispositivo [Android,][DevtoolsRemoteDebugAndroid]um dispositivo [Windows 10][DevtoolsRemoteDebugWindows]ou [um emulador do Surface Duo,][DevtoolsRemoteDebugDuoEmulator]você é capaz de alternar a tela com o ícone Deggle Screencast no canto superior esquerdo do ![ ](../../../media/toggle-screencast-icon.msft.png) DevTools.  Com a screencasting habilitada, você pode navegar na guia Microsoft Edge no dispositivo remoto da janela DevTools.  No Microsoft Edge 84, esses botões de navegação agora também estão acessíveis ao teclado.  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Selecione Shift+Tab na barra de URL em tela mostra o foco no botão Atualizar" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   Selecionar na barra de URL em `Shift` + `Tab` tela mostra o foco no **botão Atualizar**
:::image-end:::  

Chromium problema [#1081486][CR1081486]  

### <a name="network-panel-details-pane-is-now-accessible"></a>Painel Detalhes do painel de rede agora está acessível  

No Microsoft Edge 84, o [painel Detalhes][DevtoolsNetworkDetails] **** na ferramenta Rede agora se concentra ao abri-lo para um recurso no Log [de Rede.][DevtoolsNetworkLog]  Essa alteração permite que os leitores de tela leiam e interajam com o conteúdo do painel **Detalhes.**  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="O painel Detalhes no painel Rede tem foco quando aberto" lightbox="../../media/2020/05/network-details.msft.png":::
   O **painel Detalhes** na ferramenta **Rede** tem foco quando aberto
:::image-end:::  

Chromium problema [#963183][CR963183]  

## <a name="announcements-from-the-chromium-project"></a>Anúncios do projeto Chromium  

As seções a seguir anunciam recursos adicionais disponíveis no Microsoft Edge 84 que foram contribuídos para o projeto de Chromium de código aberto.  

### <a name="fix-site-issues-with-the-new-issues-tool-in-the-devtools-drawer"></a>Corrigir problemas de site com a nova ferramenta Problemas na Gaveta de DevTools

A nova **ferramenta Issues** na DevTools Drawer foi criada para ajudar a reduzir a fatiga de notificação e a desordem do **Console.**  Atualmente, o **Console** é o local central para desenvolvedores de site, bibliotecas, estruturas e Microsoft Edge registrar mensagens, avisos e erros.  A **ferramenta Issues** agrega avisos do navegador de forma estruturada, agregada e a ação, links para recursos afetados no Microsoft Edge DevTools e fornece orientações sobre como corrigir os problemas.  Com o passar do tempo, mais e mais avisos são Microsoft Edge na ferramenta **Problemas,** em vez do **Console,** o que deve ajudar a reduzir a desordem no **Console**.  

Para começar, navegue até [Encontrar e corrigir problemas usando a ferramenta Problemas][DevtoolsIssuesIndex].  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="A ferramenta Problemas na Gaveta de DevTools" lightbox="../../media/2020/05/issues.msft.png":::
   A **ferramenta Problemas** na Gaveta de DevTools  
:::image-end:::  

Chromium problema [#1068116][CR1068116]  

### <a name="view-accessibility-information-in-the-inspect-mode-tooltip"></a>Exibir informações de acessibilidade na dica de ferramenta Inspecionar Modo  

A **dica de ferramenta Modo** de Inspeção agora indica se o elemento tem um nome e função acessíveis e é focalizado no [teclado][WebhintHintsAxeKeyboard]. [][WebhintHintsAxeNameRoleValue]  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="A dica de ferramenta Inspecionar Modo com informações de acessibilidade" lightbox="../../media/2020/05/a11y.msft.png":::
  A **dica de ferramenta Inspecionar Modo** com informações de acessibilidade  
:::image-end:::  

Chromium problema [#1040025][CR1040025]  

### <a name="performance-panel-updates"></a>Atualizações do painel de desempenho  

#### <a name="view-total-blocking-time-information-in-the-footer"></a>Exibir informações de Tempo de Bloqueio Total no rodapé  

Depois de gravar seu desempenho de carga, o **painel Desempenho** agora mostra informações de Tempo de Bloqueio Total \(TBT\) no rodapé.  O TBT é uma métrica de desempenho de carga que ajuda a quantificar quanto tempo uma página leva para se tornar usável.  Ele mede basicamente por quanto tempo uma página parece ser usável \(porque o conteúdo é renderizado na tela\); mas não é realmente usável, porque JavaScript está bloqueando o thread principal e, portanto, a página não responde à entrada do usuário.  O TBT é a principal métrica para se aproximar do Primeiro Atraso de Entrada.  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

Para obter informações de Tempo de Bloqueio Total, não use o **fluxo** de trabalho de ícone da página Atualizar Página de Atualização ![ para registrar o desempenho da carga da ](../../../media/refresh-page-icon.msft.png) página.  

Em vez disso, **selecione Record** Record icon ![ , recarrege manualmente a página, aguarde a página ser carregada e, ](../../../media/record-icon.msft.png) em seguida, pare a gravação.  

Se `Total Blocking Time: Unavailable` for exibido, Microsoft Edge DevTools não obterá as informações necessárias dos dados de criação de perfil internos no Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Total de informações de Tempo de Bloqueio no rodapé de uma gravação de painel de desempenho" lightbox="../../media/2020/05/tbt.msft.png":::
   Total de informações de Tempo de Bloqueio no rodapé de uma **gravação de painel** de desempenho  
:::image-end:::  

Chromium problema [#1054381][CR1054381]  

#### <a name="layout-shift-events-in-the-new-experience-section"></a>Eventos de Layout Shift na nova seção Experiência  

A nova **seção Experiência** do **painel Desempenho** ajuda você a detectar turnos de layout.  A Mudança cumulativa de Layout \(CLS\) é uma métrica que ajuda você a quantificar a instabilidade visual indesejada.

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

Escolha o **evento Layout Shift** para exibir os detalhes da mudança de layout no painel **Resumo.**  Passe o mouse nos **campos Movido de e** Movido **para** visualizar onde ocorreu a mudança de layout.  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Os detalhes de uma mudança de layout" lightbox="../../media/2020/05/cls.msft.png":::
   Os detalhes de uma mudança de layout  
:::image-end:::  

### <a name="more-accurate-promise-terminology-in-the-console"></a>Terminologia de promessa mais precisa no Console  

Ao registrar um `Promise` , o console **forneceu** o valor `PromiseStatus` incorretamente definido como `resolved` .  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Um exemplo do Console usando a terminologia resolvida antiga" lightbox="../../media/2020/05/resolved.msft.png":::
   Um exemplo do **Console** usando a `resolved` terminologia antiga  
:::image-end:::  

O **Console** agora usa o termo `fulfilled` , que se alinha à `Promise` especificação.  Para obter mais informações sobre a `Promise` especificação, navegue até [Estados e Destinos em GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Um exemplo do Console usando a nova terminologia cumprida" lightbox="../../media/2020/05/fulfilled.msft.png":::
  Um exemplo do **Console usando** a `fulfilled` nova terminologia  
:::image-end:::  

V8 issue [#6751][CRV86751]  

### <a name="styles-pane-updates"></a>Atualizações do painel estilos  

#### <a name="support-for-the-revert-keyword"></a>Suporte para a palavra-chave de reverter  

A interface do usuário de preenchimento automático do painel **Estilos** agora detecta a palavra-chave [CSS][MDNRevert] revertida, que reverte o valor em cascata de uma propriedade para o valor anterior aplicado ao estilo do elemento.  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Definindo o valor de uma propriedade a ser revertida" lightbox="../../media/2020/05/revert.msft.png":::
  Definindo o valor de uma propriedade a ser revertida  
:::image-end:::  

Chromium problema [#1075437][CR1075437]  

#### <a name="image-previews"></a>Visualizações de imagem  

Passe o mouse em um valor no painel Estilos para `background-image` exibir uma visualização da imagem em uma dica de ferramenta. ****  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Passar o mouse sobre um valor de imagem em segundo plano" lightbox="../../media/2020/05/image-preview.msft.png":::
  Passar o mouse sobre um `background-image` valor  
:::image-end:::  

Chromium problema [#1040019][CR1040019]  

#### <a name="color-picker-now-uses-space-separated-functional-color-notation"></a>O Selador de Cores agora usa notação de cor funcional separada por espaço  

[O Módulo de Cor CSS Nível 4][CSSWGDraftsColor4Changes3] especifica que as funções de cor, como , devem dar suporte a `rgb()` argumentos separados por espaço.  Por exemplo, `rgb(0, 0, 0)` é equivalente a `rbg(0 0 0)`.  

Quando você escolhe [][DevtoolsCssReferenceColorPicker] cores com o Seletor de Cores ou alterna entre representações de cores no painel **Estilos** segurando e selecionando o valor, a sintaxe de argumento separada por espaço é `Shift` `background-color` exibida.  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Usando argumentos separados por espaço no painel Estilos" lightbox="../../media/2020/05/color.msft.png":::
  Usando argumentos separados por espaço no painel **Estilos**  
:::image-end:::  

Você também deve exibir a sintaxe no painel **Computed** e na dica de ferramenta **Inspecionar Modo.**  

Microsoft Edge DevTools está usando a nova sintaxe porque os recursos CSS futuros, como [color()][CSSWGDraftsColor4Property] não suportam a sintaxe de argumento preterida separada por vírgulas.  

A sintaxe de argumento separada por espaço tem suporte na maioria dos navegadores por um tempo.  Para obter mais informações, navegue até [Posso usar: Notações][CaniuseMDNSpaceSeparatedFunctionalColorNotations] de cores funcionais separadas por espaço?  

Chromium problema [#1072952][CR1072952]  

### <a name="deprecation-of-the-properties-pane-in-the-elements-panel"></a>Deprecation do painel Propriedades no painel Elementos  

O **painel Propriedades** na ferramenta **Elements** é preterido.  Em `console.dir($0)` vez **disso, execute no Console.**  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="O painel Propriedades preterida" lightbox="../../media/2020/05/properties.msft.png":::
   O painel Propriedades **** preterida  
:::image-end:::  

#### <a name="references"></a>Referências  

*   [console.dir()][DevtoolsConsoleApiDir]  
*   [$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]  

### <a name="app-shortcuts-support-in-the-manifest-pane"></a>Suporte a atalhos de aplicativo no painel Manifesto  

Atalhos de aplicativo ajudam os usuários a iniciar rapidamente tarefas comuns ou recomendadas em um aplicativo Web.  O menu atalhos do aplicativo é mostrado apenas para Aplicativos [Web][PwaIndex] Progressivos instalados na área de trabalho ou dispositivo móvel do usuário.  

<!--For more information, navigate to [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Atalhos de aplicativo no painel Manifesto" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  Atalhos de aplicativo no painel **Manifesto**  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Baixar os canais de visualização do Microsoft Edge  

Se você estiver no Windows ou macOS, considere usar os canais [Microsoft Edge de][MicrosoftEdgePreviewChannels] visualização como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Entrar em contato com a Microsoft Edge Devtools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

<!--[DevtoolsWhatsNew201901Inspect]: ../../../whats-new/2019/01/devtools.md#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[DevtoolsConsoleApiDir]: ../../../console/api.md#dir "dir - Console API Reference | Microsoft Docs"  
[DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]: ../../../console/utilities.md#recently-chosen-element-or-javascript-object "Elemento escolhido recentemente ou objeto JavaScript - Referência da API de Utilitários de Console | Microsoft Docs"  
[DevtoolsCssReferenceColorPicker]: ../../../css/reference.md#change-colors-with-the-color-picker "Alterar cores com o Seletor de Cores - Referência CSS | Microsoft Docs"  
[DevtoolsDrawer]: ../../../customize/index.md#drawer "Gaveta - Personalizar visão geral | Microsoft Docs"  
[DevtoolsIndex]: ../../../index.md "Microsoft Edge (Chromium) ferramentas de desenvolvedor | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../../../issues/index.md "Encontrar e corrigir problemas com a guia Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkDetails]: ../../../network/index.md#inspect-the-details-of-the-resource "Inspecione os detalhes do recurso | Microsoft Docs"  
[DevtoolsNetworkLog]: ../../../network/index.md#log-network-activity "Log network activity | Microsoft Docs"  
[DevtoolsRemoteDebugAndroid]: ../../../remote-debugging/index.md "Introdução com dispositivos Android de depuração remota | Microsoft Docs"  
[DevtoolsRemoteDebugDuoEmulator]: ../../../remote-debugging/surface-duo-emulator.md "Introdução com emuladores do Surface Duo de Depuração Remota | Microsoft Docs"  
[DevtoolsRemoteDebugWindows]: ../../../remote-debugging/windows.md "Introdução com a Depuração Remota Windows 10 Dispositivos | Microsoft Docs"  

[PwaIndex]: ../../../../progressive-web-apps-chromium/index.md "Aplicativos Web progressivos no Windows | Microsoft Docs"  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Use o emulador do Surface Duo | Microsoft Docs"

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge Aplicativo Android"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Notações de cores funcionais separadas por espaço - MDN | Posso usar"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros do Chromium"

[CR174309]: https://crbug.com/174309 "DevTools: Permitir personalizar atalhos de teclado/vinculações de teclas | Chromium bugs"  
[CR963183]: https://crbug.com/963183 "DevTools não são compatíveis com wcag | Chromium bugs"  
[CR1040019]: https://crbug.com/1040019 "DevTools: visualizar facilmente imagens e imagens de plano de fundo no painel Estilos | Chromium bugs"  
[CR1040025]: https://crbug.com/1040025 "DevTools: mostrar informações básicas do a11y no elemento | Chromium bugs"  
[CR1048378]: https://crbug.com/1048378 "Suporte à interface do usuário do DevTools para o modo de alto contraste | Chromium bugs"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Chromium bugs"  
[CR1068116]: https://crbug.com/1068116 "Painel de problemas de | Chromium bugs"  
[CR1072952]: https://crbug.com/1072952 "DevTools: o seletor de cores deve produzir uma sintaxe de cor CSS moderna | Chromium bugs"  
[CR1075437]: https://crbug.com/1075437 "DevTools: adicione suporte para a palavra-chave/valor css 'reverter' | Chromium bugs"  
[CR1076112]: https://crbug.com/1076112 "Personalização de devtools - resizer de gaveta"  
[CR1081486]: https://crbug.com/1081486 "Foco do teclado não visível para botões de navegação no modo screencast | Chromium bugs"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus deve ser 'cumprido', não 'resolvido' | Bugs de V8"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Alterações de Cores 3 - Css Color Module Level 4 | Rascunhos do Editor do Grupo de Trabalho CSS do W3C"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. Cor de primeiro plano: a &quot;cor&quot; - Css Color Module Level 4 | Rascunhos do Editor do Grupo de Trabalho CSS do W3C"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Apresentando o novo Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Estados e Destinos - domenic/promises-unwrapping | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "reverter | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Compatibilidade do navegador | MDN"  

[VisualStudioCodeMain]: https://code.visualstudio.com/ "Visual Studio Code"  
[VisualStudioCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio Code Atalhos de teclado para Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: teclado | WebHint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: Name Role Value | WebHint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Ativar ou desativar o modo de alto contraste Windows | Windows suporte"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Postar um Tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools conta do Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Novo problema - MicrosoftDocs/desenvolvedor de borda"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Microsoft Edge Canais de visualização"  
[TheWebWeWantMain]: https://aka.ms/webwewant "A Web Que Queremos"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developer.chrome.com/blog/new-in-devtools-84) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
