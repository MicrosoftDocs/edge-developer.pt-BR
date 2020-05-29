---
title: O que há de novo no DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: f07639d3c5cd246704f3d489c0e59714a938f13d
ms.sourcegitcommit: a5392ab44133d742c0e1fa500ad9a872989b7c3f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684737"
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

# O que há de novo no DevTools (Microsoft Edge 84)  

## Anúncios da equipe do Microsoft Edge DevTools  

As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools! Dê uma olhada neles para experimentar os novos recursos do DevTools, as extensões de código do VS e muito mais.  Para ficar atualizado sobre todos os recursos mais recentes e mais recentes em suas ferramentas de desenvolvedor, baixe os [canais de visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].  

### Usar o DevTools no modo de alto contraste do Windows

O Microsoft Edge DevTools agora é exibido no modo de alto contraste quando o Windows está no modo de alto contraste.  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="O Microsoft Edge DevTools no modo de alto contraste" lightbox="../../media/2020/05/high-contrast.msft.png":::
   O Microsoft Edge DevTools no modo de alto contraste  
:::image-end:::  

[Siga as instruções para ativar o modo de alto contraste no Windows][MicrosoftSupportWindows10HighContrastMode].  Abra o DevTools no Microsoft Edge pressionando `F12` ou `Ctrl` + `Shift` + `I` .  O DevTools é exibido no modo de alto contraste.  

> [!NOTE]
> O Microsoft Edge DevTools atualmente é compatível com o modo de alto contraste no Windows, mas não no macOS. 

Chromium problema [#1048378][CR1048378]  

### Corresponder os atalhos de teclado no DevTools código do VS  

Do seu [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) e do [controlador de problemas Chromium público][CRIssuesList], a equipe do Microsoft Edge devtools aprendeu que você queria a capacidade de personalizar atalhos de teclado no devtools.  No Microsoft Edge 84, agora é possível fazer a correspondência entre os atalhos de teclado no [código][VSCode]do devtools, que é apenas um dos recursos nos quais a equipe está trabalhando para a personalização de atalhos.  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Corresponder os atalhos de teclado no DevTools código do VS" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   O Microsoft Edge DevTools no modo de alto contraste  
:::image-end:::  

Para experimentar o experimento, abra as configurações do DevTools pressionando `?` ou selecionando o ícone de ![ configurações do devtools ][ImageSettingsIcon] no canto superior direito da devtools.  Navegue até a seção **experimentos** e marque **habilitar a guia Configurações de atalhos de teclado personalizados (requer recarregamento)**.  Agora, recarregue o DevTools, abra as configurações novamente e navegue até a seção **atalhos** .  

Selecione **devtools (padrão)** na lista suspensa **coincidir os atalhos de predefinir** e selecione **código do Visual Studio**.  Os atalhos de teclado no DevTools agora correspondem aos atalhos para ações equivalentes no código VS.  

Por exemplo, o atalho de teclado para pausar ou continuar a execução de um script em um [código vs][VSCodeShortcuts] é `F5` .  Com a predefinição **devtools (padrão)** , o mesmo atalho no devtools está, `F8` mas com a predefinição de **código do Visual Studio** , esse atalho também é `F5` .  

No momento, o recurso está disponível no Microsoft Edge 84 como um experimento, portanto Compartilhe seus [comentários](#getting-in-touch-with-microsoft-edge-devtools-team) com a equipe!  

Chromium problema [#174309][CR174309]  

### Emuladores Remote Debug Surface Duo  

Agora você pode depurar remotamente o conteúdo da Web em execução no [emulador Surface Duo][DualScreensAndroidEmulator] usando toda a capacidade do [Microsoft Edge devtools][DevToolsChromiumGuide].  

Com o [emulador Surface Duo][DualScreensAndroidEmulator], você pode testar como o conteúdo da Web é renderizado em uma nova classe de dispositivos dobrável e de tela dupla.  O emulador executa o sistema operacional Android e fornece o [aplicativo Android do Microsoft Edge][AndroidEdge].  Carregue o conteúdo da Web no [aplicativo Microsoft Edge][AndroidEdge] e depure-o com o [Microsoft Edge devtools][DevToolsChromiumGuide].  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="O aplicativo Microsoft Edge em execução no emulador Surface Duo" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   O aplicativo Microsoft Edge no emulador Surface Duo  
:::image-end:::  

A `edge://inspect` página em uma instância da área de trabalho do [Microsoft Edge][DesktopEdge] mostra o **SurfaceDuoEmulator** com uma lista das guias abertas ou [PWAs][PwaIndex] que estão em execução no [emulador Surface Duo][DualScreensAndroidEmulator].  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="A página edge://inspect exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   A `edge://inspect` página exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador
:::image-end:::  

Selecionar **inspecionar** para a guia ou PWA que você deseja depurar abre o [Microsoft Edge devtools][DevToolsChromiumGuide].  [Siga o guia passo a passo para depurar remotamente o conteúdo da Web no emulador Surface Duo][DevToolsRemoteDebugDuoEmulator].  

### Redimensionar a gaveta DevTools mais facilmente  

No Microsoft Edge 83 ou anterior, você foi capaz de redimensionar a [gaveta devtools][DevToolsDrawer] passando dentro da barra de ferramentas da gaveta.  A gaveta se comportada de maneira diferente dos outros controles de redimensionamento para painéis no DevTools onde você passa o mouse sobre a borda do painel para redimensioná-lo.  Selecione a imagem a seguir para ver como o redimensionamento da gaveta trabalhou na versão 83 ou anterior do Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Redimensionando a gaveta DevTools no Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   Redimensionando a gaveta DevTools no Microsoft Edge 83
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

Começando com o Microsoft Edge 84, agora você pode redimensionar a gaveta passando o mouse sobre a borda da gaveta.  Essa alteração alinha o comportamento redimensionando a gaveta DevTools com a maneira como você redimensiona outros painéis no DevTools.  Selecione a imagem a seguir para ver o redimensionamento em ação no Microsoft Edge 84.  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Redimensionando a gaveta DevTools no Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   Redimensionando a gaveta DevTools no Microsoft Edge 84
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

Chromium problema [#1076112][CR1076112]  

### Botões de navegação de screencasts exibem o foco  

Ao depurar remotamente um [dispositivo Android][DevToolsRemoteDebugAndroid], um [dispositivo com o Windows 10][DevToolsRemoteDebugWindows]ou um [emulador Surface Duo][DevToolsRemoteDebugDuoEmulator], você pode alternar o screencast com o ![ ícone alternar screencast ][ImageScreencastingIcon] no canto superior esquerdo da devtools.  Com o screencast habilitado, você poderá navegar na guia no Microsoft Edge no dispositivo remoto na janela do DevTools.  No Microsoft Edge 84, esses botões de navegação agora também são acessíveis pelo teclado.  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Pressionar Shift + Tab na barra de URL do screencast mostra o foco no botão atualizar" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   Pressione `Shift` + `Tab` a barra de URL com o screencast para mostrar o foco no botão **Atualizar**
:::image-end:::  

Chromium problema [#1081486][CR1081486]  

### O painel de detalhes do painel de rede tem foco  

No Microsoft Edge 84, o [painel de detalhes][DevToolsNetworkDetails] no painel de **rede** agora tem foco quando você o abre para um recurso no [log de rede][DevToolsNetworkLog].  Essa alteração permite que os leitores de tela leiam e interajam com o conteúdo do painel de **detalhes** .  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="O painel de detalhes no painel rede tem o foco quando aberto" lightbox="../../media/2020/05/network-details.msft.png":::
   O painel de **detalhes** no painel **rede** tem o foco quando aberto
:::image-end:::  

Chromium problema [#963183][CR963183]  

## Anúncios do projeto Chromium  

As seções a seguir anunciarão recursos adicionais disponíveis no Microsoft Edge 84 que contribuíram para o projeto de código-fonte aberto Chromium.  

### Corrigir problemas de site com a nova ferramenta problemas na gaveta do DevTools

A nova ferramenta de **problemas** na gaveta devtools foi criada para ajudar a reduzir o cansativo de notificação e o email secundário do **console**.  Atualmente, o **console** é o local central para desenvolvedores de site, bibliotecas, estruturas e Microsoft Edge para registrar mensagens, avisos e erros.  A ferramenta **problemas** agrega avisos do navegador em uma maneira estruturada, agregada e acionável, links para recursos afetados no Microsoft Edge devtools e fornece orientação sobre como corrigir os problemas.  Ao longo do tempo, você deve ver mais e mais avisos no Microsoft Edge faceamento na ferramenta **problemas** em vez de no **console**, o que pode ajudar a reduzir o email secundário no **console**.  

Para começar, confira [Localizar e corrigir problemas com a ferramenta problemas do Microsoft Edge devtools][DevtoolsIssuesIndex].  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="A ferramenta problemas na gaveta DevTools" lightbox="../../media/2020/05/issues.msft.png":::
   A ferramenta **problemas** na gaveta devtools  
:::image-end:::  

Chromium problema [#1068116][CR1068116]  

### Exibir informações de acessibilidade na dica de ferramenta do modo de inspeção  

A dica de ferramenta do **modo de inspeção** agora indica se o elemento tem um [nome e função][WebhintHintsAxeNameRoleValue] acessível e se é [focado no teclado][WebhintHintsAxeKeyboard].  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Dica de ferramenta do modo de inspeção com informações de acessibilidade" lightbox="../../media/2020/05/a11y.msft.png":::
  Dica de ferramenta do **modo de inspeção** com informações de acessibilidade  
:::image-end:::  

Chromium problema [#1040025][CR1040025]  

### Atualizações do painel de desempenho  

#### Exibir informações de tempo de bloqueio total no rodapé  

Depois de gravar o desempenho da carga, o painel **desempenho** agora mostra as informações do tempo de bloqueio total \ (TBT \) no rodapé.  TBT é uma métrica de desempenho de carga que ajuda a quantificar o tempo que uma página leva para ser utilizável.  Isso essencialmente mede o tempo em que uma página parece ser utilizável \ (porque o conteúdo é renderizado na tela \); Mas não é utilizável realmente porque o JavaScript está bloqueando o thread principal e, portanto, a página não responde à entrada do usuário.  TBT é a métrica principal para approximating do primeiro atraso de entrada.  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

Para obter informações sobre o tempo total de bloqueio, não use o fluxo de trabalho **Atualizar** ![ ícone da página ][ImageRefreshPageIcon] de atualização de página para gravar o desempenho da carga da página.  

Em vez disso **, selecione** ![ o ícone registro ][ImageRecordIcon] de registro, recarregue manualmente a página, aguarde até que a página seja carregada e, em seguida, pare a gravação.  

Se você vir `Total Blocking Time: Unavailable` , o Microsoft Edge devtools não obteve as informações necessárias dos dados internos de criação de perfil no Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Total de informações de tempo de bloqueio no rodapé de uma gravação de painel de desempenho" lightbox="../../media/2020/05/tbt.msft.png":::
   Total de informações de tempo de bloqueio no rodapé de uma gravação de painel de **desempenho**  
:::image-end:::  

Chromium problema [#1054381][CR1054381]  

#### Eventos Shift de layout na seção nova experiência  

A seção **experiência** nova do painel **desempenho** ajuda você a detectar turnos de layout.  O deslocamento de layout cumulativo \ (CLS \) é uma métrica que ajuda você a quantificar a instabilidade Visual indesejada.

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

Selecione o evento de **deslocamento de layout** para ver os detalhes do deslocamento de layout no painel **Resumo** .  Passe o mouse sobre os campos **movido de** e **movido para** para visualizar onde a mudança de layout ocorreu.  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Os detalhes de uma mudança de layout" lightbox="../../media/2020/05/cls.msft.png":::
   Os detalhes de uma mudança de layout  
:::image-end:::  

### Terminologia Promise mais precisa no console  

Ao registrar um `Promise` , o valor de **console** fornecido incorretamente é `PromiseStatus` definido como `resolved` .  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Um exemplo do console usando a antiga terminologia resolvida" lightbox="../../media/2020/05/resolved.msft.png":::
   Um exemplo do **console** que usa a antiga `resolved` terminologia  
:::image-end:::  

O **console** agora usa o termo `fulfilled` , que se alinha com a `Promise` especificação.  Para obter mais informações sobre a `Promise` especificação, consulte [Estados e Fates no GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Um exemplo do console usando a nova terminologia atendida" lightbox="../../media/2020/05/fulfilled.msft.png":::
  Um exemplo do **console** usando a nova `fulfilled` terminologia  
:::image-end:::  

V8 problema [#6751][CRV86751]  

### Atualizações do painel de estilos  

#### Suporte para a palavra-chave REVERT  

A interface do usuário de autocompletar do painel **estilos** agora detecta a palavra-chave CSS [REVERT][MDNRevert] , que reverte o valor em cascata de uma propriedade para o valor anterior aplicado ao estilo do elemento.  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Definir o valor de uma propriedade para reverter" lightbox="../../media/2020/05/revert.msft.png":::
  Definir o valor de uma propriedade para reverter  
:::image-end:::  

Chromium problema [#1075437][CR1075437]  

#### Visualizações de imagens  

Passe o mouse sobre um `background-image` valor no painel **estilos** para ver uma visualização da imagem em uma dica de ferramenta.  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Passando o cursor do mouse sobre um valor de imagem de tela de fundo" lightbox="../../media/2020/05/image-preview.msft.png":::
  Passar o mouse sobre um `background-image` valor  
:::image-end:::  

Chromium problema [#1040019][CR1040019]  

#### Agora, o seletor de cores usa a notação de cores funcional separada por espaços  

[Módulo de cores CSS nível 4][CSSWGDraftsColor4Changes3] especifica que as funções de cor, como, por exemplo `rgb()` , devem dar suporte a argumentos separados por espaço.  Por exemplo, `rgb(0, 0, 0)` é equivalente a `rbg(0 0 0)`.  

Ao escolher as cores com o [seletor de cores][DevtoolsCssReferenceColorPicker] ou alternar entre as representações de cores no painel **estilos** , mantendo `Shift` e selecionando o `background-color` valor, você verá a sintaxe do argumento separado por espaços.  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Usando argumentos separados por espaço no painel estilos" lightbox="../../media/2020/05/color.msft.png":::
  Usando argumentos separados por espaço no painel **estilos**  
:::image-end:::  

Você também deve ver a sintaxe no painel **calculado** e a dica de ferramenta do **modo de inspeção** .  

O Microsoft Edge DevTools está usando a nova sintaxe porque recursos CSS futuros, como [Color ()][CSSWGDraftsColor4Property] , não são compatíveis com a sintaxe do argumento separado por vírgulas substituídas por vírgula.  

A sintaxe do argumento separado por espaços tem suporte na maioria dos navegadores há algum tempo.  Para obter mais informações, consulte [posso usar: notações de cores funcionais separadas por espaços?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]  

Chromium problema [#1072952][CR1072952]  

### Substituição do painel Propriedades no painel elementos  

O painel **Propriedades** no painel **elementos** é preterido.  `console.dir($0)`Em vez disso, execute no **console** .  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="O painel Propriedades preteridas" lightbox="../../media/2020/05/properties.msft.png":::
   O painel **Propriedades** preteridas  
:::image-end:::  

#### Referências  

*   [console. dir ()][DevtoolsConsoleApiDir]  
*   [$0][DevtoolsConsoleUtilitiesDom]  

### Suporte a atalhos do aplicativo no painel manifesto  

Os atalhos do aplicativo ajudam os usuários a iniciar rapidamente tarefas comuns ou recomendadas em um aplicativo Web.  O menu de atalhos do aplicativo é mostrado somente para [aplicativos Web progressivos][PwaIndex] que são instalados na área de trabalho do usuário ou no dispositivo móvel.  

<!--For more information, see [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Atalhos do aplicativo no painel manifesto" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  Atalhos do aplicativo no painel **manifesto**  
:::image-end:::  

## Baixar os canais de visualização do Microsoft Edge   

Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.  Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.  

## Como entrar em contato com o Microsoft Edge devtools equipe  

  

Para discutir os novos recursos e alterações no post ou em qualquer outro item relacionado ao DevTools:  

*   Envie seus comentários usando o ícone de **comentários** no devtools  
*   Tweet em [@EdgeDevTools][PostTweetEdgeDevTools]  
*   Enviar uma sugestão para [a Web que][TheWebWeWant] queremos  
*   Erros de arquivo nesta página no repositório [Edge-Developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue]  

:::image type="complex" source="../../media/2020/05/feedback-icon.msft.png" alt-text="O ícone de comentários no Microsoft Edge DevTools" lightbox="../../media/2020/05/feedback-icon.msft.png":::
  O ícone de **comentários** no Microsoft Edge devtools  
:::image-end:::  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Ícone de configurações do DevTools"
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/images/toggle-screencast-icon.msft.png "Ícone de DevTools de botão de alternância"
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png "Ícone de página de atualização do painel desempenho do DevTools"
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png "Ícone de registro do painel desempenho do DevTools"

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Use o emulador Surface Duo | Documentos da Microsoft"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "Dir-referência de API do console | Documentos da Microsoft"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Elemento JavaScript ou elemento JavaScript selecionado recentemente-referência de API de utilitários de console | Documentos da Microsoft"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Alterar as cores com o seletor de cores – referência de CSS | Documentos da Microsoft"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Gaveta-personalizar visão geral | Documentos da Microsoft"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Localizar e corrigir problemas com a guia problemas do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Introdução à depuração remota de dispositivos Android | Documentos da Microsoft"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Introdução aos emuladores Remote Debugging Surface Duo | Documentos da Microsoft"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Introdução à depuração remota de dispositivos Windows 10 | Documentos da Microsoft"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Inspecione os detalhes do recurso | Documentos da Microsoft"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Registrar atividades da rede | Documentos da Microsoft"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicativos Web progressivos no Windows | Documentos da Microsoft"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Aplicativo Android do Microsoft Edge"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Notações de cores funcionais separadas por espaços-MDN | Posso usar"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros de Chromium"

[CR174309]: https://crbug.com/174309 "DevTools: permite personalizar atalhos de teclado/associações de teclas | Erros de Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools não são compatíveis com a WCAG | Erros de Chromium"  
[CR1040019]: https://crbug.com/1040019 "DevTools: visualize facilmente imagens de plano de fundo e imagens no painel estilos | Erros de Chromium"  
[CR1040025]: https://crbug.com/1040025 "DevTools: show Basic A11y info in Element popover | Erros de Chromium"  
[CR1048378]: https://crbug.com/1048378 "Suporte de interface do usuário DevTools para modo de alto contraste | Erros de Chromium"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Erros de Chromium"  
[CR1068116]: https://crbug.com/1068116 "Painel de envio de problemas | Erros de Chromium"  
[CR1072952]: https://crbug.com/1072952 "DevTools: o seletor de cores deve produzir uma sintaxe de cor CSS moderna | Erros de Chromium"  
[CR1075437]: https://crbug.com/1075437 "DevTools: adicionar suporte para a palavra-chave/valor da CSS ' rever ' | Erros de Chromium"  
[CR1076112]: https://crbug.com/1076112 "Personalização de devtools-redimensionador de gaveta"  
[CR1081486]: https://crbug.com/1081486 "O foco do teclado não está visível para botões de navegação no modo screencast | Erros de Chromium"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus deve ser ' cumprido ', não ' resolvido ' | Erros de V8"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Alterações de cores 3-módulo de cor CSS nível 4 | Rascunhos do editor de grupo de trabalho W3C CSS"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. cor do primeiro plano: ' cor '-nível 4 do módulo colorido CSS | Rascunhos do editor de grupo de trabalho W3C CSS"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Apresentando o novo Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Estados e Fates-Domenic/promessas-desempacotamento | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "reverter | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Compatibilidade com o navegador | MDN"  

[VSCode]: https://code.visualstudio.com/ "Código do Visual Studio"  
[VSCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Atalhos de teclado de código do Visual Studio para Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: teclado | Webhint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: nome função valor | Webhint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Ativar ou desativar o modo de alto contraste no Windows | Suporte do Windows"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Postar um tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools conta do Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Novo problema-MicrosoftDocs/Edge-Developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canais de visualização do Microsoft Edge"  
[TheWebWeWant]: https://aka.ms/webwewant "A Web que queremos"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/05/devtools/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
