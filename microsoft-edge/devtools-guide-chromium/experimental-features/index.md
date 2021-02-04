---
description: Os recursos experimentais mais recentes no Microsoft Edge DevTools
title: Recursos experimentais
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas f12, devtools, experimento
ms.openlocfilehash: 018364d4debc1791685a028c337f61f85865ef6b
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313034"
---
# Recursos experimentais  

O Microsoft Edge DevTools fornece acesso a recursos experimentais que ainda estão em desenvolvimento.  Você pode testar e [fornecer comentários antes](#providing-feedback-on-experimental-features) de cada recurso ser lançado.  

Embora os recursos experimentais estão disponíveis em todos os canais do Microsoft Edge, você pode obter os recursos experimentais mais recentes usando o canal Canary do Microsoft Edge.  

## Ativar recursos experimentais  

Para ativar \(ou desativar\) recursos experimentais no Microsoft Edge, conclua as etapas a seguir.  

1.  [Abra o DevTools.][DevtoolsOpenMain]  
    *   Selecione `Control` + `Shift` + `I` \(Windows, Linux\) ou `Command` + `Option` + `I` \(macOS\).  Para obter mais informações, navegue até atalhos de teclado do [Microsoft Edge DevTools.][DevToolsShortcuts]  
1.  Abra o [painel Configurações.][DevToolsCustomizeIndexSettings]  
    *   Selecione `Shift` + `?` .  Para obter mais informações, navegue até atalhos de teclado do [Microsoft Edge DevTools.][DevToolsShortcuts]  
1.  No lado esquerdo do painel **Configurações,** escolha a **seção** Experimentos.  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="A página Experimentos em Configurações" lightbox="../media/experiments-devtools.msft.png":::
       A **página Experimentos** em **Configurações**  
    :::image-end:::  
    
1.  Na página **Experimentos,** role pela lista de todos os recursos experimentais disponíveis e marque a caixa de seleção ao lado de cada recurso que você deseja testar.  
1.  Feche e reabra o Microsoft Edge DevTools.  
    
> [!NOTE]
> Os recursos experimentais estão sendo constantemente atualizados e podem causar problemas de desempenho.  Para desativar um recurso experimental, abra a página **Experimentos** e limpe a caixa de seleção do recurso experimental que você deseja desativar.  

## Recursos experimentais realçados  

As seções a seguir descrevem os novos recursos experimentais disponíveis no Microsoft Edge.  

| Recurso experimental | Versão do Microsoft Edge |  
|:--- |:--- |  
| [Habilitar webhint](#enable-webhint) | 85 ou posterior |  
| [Habilitar o Console de Rede](#enable-network-console) | 85 ou posterior |  
| [Visualizador da Ordem de Origem](#source-order-viewer) | 86 ou posterior |  
| [Habilitar o editor de atalho do teclado](#enable-keyboard-shortcut-editor) | 87 ou posterior |  
| [Habilitar camadas compostas no modo de exibição 3D](#enable-composited-layers-in-3d-view) | 87 ou posterior |  
| [Habilitar a nova ferramenta Editor de Fontes no painel Estilos](#) | 89 ou posterior |  
| [Habilitar novos recursos de depuração do CSS Flexbox](#enable-new-css-flexbox-debugging-features) | 89 ou posterior |  
| [Habilitar + menus de guia de botão para abrir mais ferramentas](#enable--button-tab-menus-to-open-more-tools) | 89 ou posterior |  
| [Habilitar guia Bem-vindo](#enable-welcome-tool) | 89 ou posterior |  

### Habilitar novos recursos de depuração de grade CSS  

Esse recurso experimental fornece várias novas visualizações para ajudá-lo a depurar layouts de grade CSS.  Para visualizar os recursos experimentais mais recentes, [habilita este experimento](#turn-on-experimental-features) e recarregue o DevTools.  Esse experimento está por padrão no Microsoft Edge versão 87 ou posterior.  

#### Exibindo sobreposições de grade em foco com a ferramenta Inspect  

A **ferramenta Inspect** fornece uma maneira rápida de identificar e visualizar layouts de grade CSS em um site ao passar o mouse sobre eles.  Escolha o **ícone Inspecionar** \( ![ Inspecionar ](../media/inspect-icon.msft.png) \) no canto superior esquerdo do DevTools.  Em seguida, passe o mouse sobre um elemento Grid no site que você está depurando.  Os contornos são exibidos ao redor da grade, e o sombreamento indica a localização das lacunas de grade, se presente.  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Exibindo grades com a ferramenta Inspect" lightbox="../media/grid-inspect.msft.png":::
   Exibindo grades com a **ferramenta Inspect**  
:::image-end:::  

#### Exibindo sobreposições de grade persistente  

No Microsoft Edge versão 86 ou posterior, o recurso de grade CSS experimental também oferece a opção de habilitar sobreposições de grade persistentes.  As sobreposições persistentes oferecem vários benefícios.  

*   As sobreposições persistentes permanecem visíveis na página à medida que você rola, move o mouse e usa outros recursos do DevTools.  
*   Várias sobreposições persistentes podem ser habilitadas ao mesmo tempo, permitindo que você revise vários layouts de grade ao mesmo tempo.  
*   As sobreposições persistentes oferecem muitas opções de configuração, como ocultar ou mostrar nomes na área de grade, lacunas de grade, tamanhos de controle e assim por diante.  
    
As duas maneiras de alternar uma sobreposição de grade persistente.  

*   Escolha o **ícone de** oval Grade ao lado de qualquer elemento Grid mostrado na árvore DOM da **ferramenta Elementos.**  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Ícone de oval de grade na ferramenta Elementos" lightbox="../media/grid-adorner.msft.png":::
       Ícone de oval de grade na **ferramenta Elementos**  
    :::image-end:::  
    
*   Abra o novo **painel layout** localizado na ferramenta Elementos e escolha a caixa de seleção ao lado de cada elemento grid que você deseja realçar.  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Painel de layout no DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       **Painel** de layout no DevTools  
    :::image-end:::  
    
#### Configurando sobreposições persistentes  

No Microsoft Edge versão 86 ou posterior, o **** novo painel **** **de Layout** está localizado na ferramenta Elementos junto com as guias Estilos **e** Calculados.  O **painel layout** superfícies opções de configuração para sobreposições persistentes.  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Recurso de depuração de grade CSS" lightbox="../media/experiments-grid.msft.png":::
   Recurso de depuração de grade CSS  
:::image-end:::  

### Habilitar o suporte para mover guias entre painéis  

Normalmente, ferramentas como **Elementos** **e** Rede só podem abrir no painel principal localizado na parte superior do DevTools.  Ferramentas como **Exibição 3D** e Problemas que normalmente só abrem no painel **Gaveta** que está localizado na parte inferior do DevTools. ****  Depois de escolher o experimento, você pode mover ferramentas entre os painéis superior e inferior.  Para mover uma ferramenta, passe o mouse sobre a guia, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Mover** para cima ou Mover para **baixo.**   Esse experimento permite que você personalize o layout do DevTools.  Para exibir ou ocultar o painel **Gaveta,** selecione `Escape` .  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Movendo guias entre painéis" lightbox="../media/experiments-move-panels.msft.png":::
   Movendo guias entre painéis  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar webhint  

[webhint é][WebhintMain] uma ferramenta de código aberto que fornece comentários em tempo real para sites e páginas da Web locais.  O tipo de comentário fornecido pela [webhint][WebhintMain].  

*   acessibilidade  
*   compatibilidade entre navegadores  
*   segurança  
*   desempenho  
*   Aplicativos Web progressivos (PWAs)  
*   outros problemas comuns de desenvolvimento na Web  
    
O [experimento webhint][WebhintMain] exibe os comentários de webhint [no][DevtoolsIssues] painel Problemas.  Escolha um problema para exibir a documentação da solução e uma lista dos recursos afetados em seu site.  Escolha um link de recurso para abrir **** o painel **Rede** **,** Fontes ou Elementos relevantes no DevTools.  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="webhint feedback in the Issues panel" lightbox="../media/experiments-webhint.msft.png":::
   webhint feedback in the **Issues** panel  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar o Console de Rede  

**Console de** rede é o título de trabalho de um experimento para fazer solicitações de rede sintética sobre HTTP.  Você pode usar o experimento **de Console de Rede** para enviar solicitações de API Web.  

Depois de ativar o experimento, reinicie o DevTools.  Para usar o **Console de Rede,** conclua as etapas a seguir.  

1.  Abra o **painel** Rede.  
1.  Encontre a solicitação de rede que você deseja alterar e reendá-la.  
1.  Abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Editar e Repetir.**  
1.  Quando o **Console de Rede** for aberto, edite as informações de solicitação de rede.  
1.  Choose **Send**.  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Console de Rede na gaveta do Console" lightbox="../media/network-network-console.msft.png":::
   **Console de Rede** na gaveta **do Console**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Visualizador da Ordem de Origem  

**O Visualizador de Ordem de** Origem é um experimento que exibe a ordem dos elementos na fonte da página da Web.  A ordem de exibição na tela pode ser diferente da ordem da origem, o que confunda os usuários do leitor de tela e do teclado.  Use o **experimento do Visualizador de Ordem** de Origem para encontrar as diferenças entre a ordem de exibição na tela e a ordem da fonte.  

Depois de ativar o experimento, reinicie o DevTools.  Para usar **o Visualizador de Ordem de Origem,** conclua as etapas a seguir.  

1.  Abra a **ferramenta Elementos.**  
1.  Abra o **painel Acessibilidade** no painel de gaveta \(inferior\).  
1.  Na seção **Visualizador da Ordem de** Origem, escolha a caixa de seleção Mostrar Ordem de **Origem.**  
1.  Realça qualquer elemento HTML para exibir uma sobreposição à ordem na origem da página da Web.  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Visualizador da Ordem de Origem no painel Acessibilidade" lightbox="../media/experiments-source-order-viewer.msft.png":::
   **Visualizador da Ordem de** Origem **no painel** Acessibilidade  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Habilitar o editor de atalho do teclado

Com o experimento de editor de **atalhos** habilitar teclado ativado, você pode personalizar atalhos de teclado para qualquer ação no DevTools.  Para personalizar o atalho do teclado para uma ação específica, conclua as etapas a seguir.  

1.  [Abra o DevTools.][DevtoolsOpenMain]  
1.  Configurações [abertas.][DevToolsCustomizeIndexSettings]  
    *   Selecione `Shift` + `?` .  
1.  Navegue até a **página Atalhos.**  
1.  Escolha a ação que você deseja personalizar.  
1.  Escolha o **ícone** Editar \( ![ EditKeyboardShortcut ](../media/edit-keyboard-shortcut-icon.msft.png) \).  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Choose the action to customize from the Shortcuts page in Settings" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       Choose the action to customize from the **Shortcuts** page in [Settings][DevToolsCustomizeIndexSettings]  
    :::image-end:::  
    
1.  No teclado, selecione as teclas para vincular à ação.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Selecione as teclas a atribuir à ação" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Selecione as teclas a atribuir à ação  
    :::image-end:::  
    
1.  Para salvar o novo atalho de teclado, escolha a marca de seleção \(![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)\) ícone.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Escolha o ícone de marca de seleção para salvar o novo atalho de teclado" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Escolha o ícone de marca de seleção para salvar o novo atalho de teclado  
    :::image-end:::  
    
1.  Selecione seu novo atalho de teclado para disparar a ação no DevTools.  
    
Na página **Atalhos,** o ícone Atalho de Teclado **Personalizado** \( ![ CustomKeyboardShortcut \) exibe ](../media/custom-keyboard-shortcut-icon.msft.png) atalhos de teclado personalizados.  Para redefinir todos os atalhos, escolha **Restaurar atalhos padrão.**  

Para descartar suas alterações enquanto edita os atalhos de teclado para uma ação, escolha o ícone X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \).  Para remover atalhos de uma ação específica, escolha o ícone Excluir atalho **\(** ![ DeleteKeyboardShortcut ](../media/delete-keyboard-shortcut-icon.msft.png) \).  Para adicionar vários atalhos para uma ação, escolha **Adicionar um atalho.**  

> [!NOTE]
> Se um atalho de teclado estiver atribuído a outra ação no momento, talvez você não o salve para uma nova ação.  Primeiro você deve excluir o atalho do teclado para a ação anterior e, em seguida, adicioná-lo à nova ação.  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Habilitar camadas compostas no modo de exibição 3D  

Agora você pode visualizar Camadas junto com índices z e o Modelo de Objeto do Documento \(DOM\).  Esse recurso ajuda você a depurar sem alternar contextos com a mesma frequência.  Você identificou que a redução da alternação de contexto era um ponto de problema importante.  Nem sempre é claro como o código que você escreve afeta seu aplicativo Web.  Para uma experiência de depuração visual abrangente, o Modo de exibição 3D e as camadas compostas agora são combinados.  

Depois de ativar o experimento, reinicie o DevTools.  Para usar **camadas compostas,** conclua as etapas a seguir.  

1.  Na gaveta, escolha a ferramenta **Exibição 3D.**  
1.  Abra o **painel Camadas Compostas.**  
1.  Todas as camadas pintadas do aplicativo são exibidas.  Experimente esse recurso com seus próprios aplicativos Web.  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Painel de Camadas compostas" lightbox="../media/experiments-layers.msft.png":::
   Painel de **Camadas Compostas**  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Habilitar a nova ferramenta Editor de Fontes no painel Estilos  

Agora você pode usar o novo Editor de [Fonte visual][DevtoolsInspectStylesEditFonts] para editar fontes.  Use-o para definir fontes e características de fonte.  O **Editor de Fonte visual** ajuda você a concluir as seguintes ações.  

*   Alternar entre unidades para propriedades de fonte diferentes  
*   Alternar entre palavras-chave para propriedades de fonte diferentes  
*   Converter unidades  
*   Gerar código CSS preciso  
    
Depois de ativar o experimento, reinicie o DevTools.  Para usar o novo Editor de **Fontes visual,** conclua as etapas a seguir.  

1.  Abra a **ferramenta Elementos.**  
1.  Abra o **painel** Estilos.  
1.  Escolha o **ícone do Editor de** Fontes.  
    
For more information about the new visual **Font Editor**, navigate to Edit CSS font styles [and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="O painel editor de fonte visual está realçada" lightbox="../media/font-editor-open.msft.png":::
   O painel **editor de** fonte visual está realçada  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Habilitar novos recursos de depuração do CSS Flexbox  

Esse recurso experimental fornece muitas visualizações novas para ajudá-lo a depurar layouts do CSS Flexbox.  Para visualizar os recursos experimentais mais recentes, [a ligue esse experimento](#turn-on-experimental-features) e recarregue o DevTools.  

#### Exibir sobreposições persistentes em layouts do Flexbox com a ferramenta Inspect  

A **ferramenta Inspect** fornece uma maneira rápida de identificar e visualizar layouts do CSS Flexbox em um site, passe o mouse sobre eles.  Escolha o **ícone Inspecionar** \( ![ Inspecionar ](../media/inspect-icon.msft.png) \) no canto superior esquerdo do DevTools.  Em seguida, durante a depuração do site, passe o mouse sobre um contêiner flexível para exibir contornos ao redor do contêiner flexível.  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Exibir contêineres do Flexbox com a ferramenta Inspect" lightbox="../media/flexbox-hover.msft.png":::
   Exibir contêineres do Flexbox com a **ferramenta Inspect**  
:::image-end:::  

#### Exibir sobreposições persistentes em layouts do Flexbox  

No Microsoft Edge versão 89 ou posterior, o recurso experimental Css Flexbox também oferece a opção de ativar sobreposições persistentes em layouts do Flexbox.  As sobreposições persistentes oferecem os seguintes benefícios.  

*   As sobreposições persistentes permanecem visíveis na página da Web à medida que você rola, move o mouse e usa outros recursos do DevTools.
*   Várias sobreposições persistentes podem ser usadas ao mesmo tempo, para permitir que você revise vários layouts do Flexbox ao mesmo tempo.  
*   Sobreposições persistentes oferecem opções de configuração de cor.  
    
Para alternar sobreposições persistentes no layout do Flexbox, use uma das ações a seguir.  

*   Escolha o ícone de oval **Flexbox** ao lado de qualquer contêiner flexbox exibido na árvore DOM da **ferramenta Elementos.**  
*   Abra o novo **painel layout** localizado na ferramenta **Elementos** e escolha a caixa de seleção ao lado de cada contêiner do Flexbox que você deseja realçar.  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Ícones flexíveis e painel layout no DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   Ícones flexíveis e **painel layout** no DevTools  
:::image-end:::  

#### Configurar sobreposições persistentes  

Para configurar opções para sobreposições persistentes para grades CSS ou layouts do Flexbox, use o **painel** Layout.  O **painel Layout** está localizado na ferramenta **Elementos** ao lado dos painéis **Estilos** **e** Calculados.  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Painel de layout" lightbox="../media/flexbox-layout.msft.png":::
   Painel de layout  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Habilitar + menus de guia de botão para abrir mais ferramentas  

Agora você pode abrir mais ferramentas usando o novo ícone Mais **Ferramentas** \( `+` \).  Depois de ativar os **menus** da guia do botão Habilitar + para abrir mais ferramentas experimentar e recarregar o DevTools, um sinal de mais \( \) é exibido à direita do grupo de guias na parte superior do `+` DevTools.  Para exibir uma lista de outras ferramentas que você pode adicionar à barra de guias, escolha o novo ícone Mais **Ferramentas** \( `+` \).  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Mais Ferramentas no painel superior" lightbox="../media/experiments-more-tools-button.msft.png":::
   **Mais Ferramentas** no painel superior
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Habilitar a ferramenta de boas-vindas

Esse experimento substitui a **ferramenta Novidades pela** nova ferramenta de **boas-vindas.**  Ele exibe um design atualizado para o conteúdo a seguir.  

*   Links para documentos de desenvolvedor  
*   os recursos mais recentes  
*   notas de versão  
*   Opção para entrar em contato com a equipe do Microsoft Edge DevTools  
    
A **ferramenta de boas-vindas** é aberta automaticamente após cada atualização do Microsoft Edge.  Para impedir a exibição da ferramenta **de** boas-vindas **** após cada atualização, des marque a caixa de seleção ao lado da guia Abrir após cada atualização sob o título da ferramenta **de** boas-vindas.  

Se você preferir a ferramenta **Novidades** original, navegue até [Experimentos][DevtoolsCustomizeIndexSettings]de Configurações e remova a caixa de seleção ao lado da guia  >  **** **Habilitar Boas-vindas.**  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Ferramenta de boas-vindas" lightbox="../media/experiments-welcome.msft.png":::
   **Ferramenta de boas-vindas**  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## Recursos experimentais anteriores  

*   [O Modo de Exibição 3D][Devtools3dViewIndex] agora está disponível e ligado por padrão no Microsoft Edge versão 83 ou posterior.  
*   [Ativar o suporte para mover guias][DevtoolsMoveTabs] entre painéis agora está disponível e ligado por padrão no Microsoft Edge versão 85 ou posterior.  
*   [Personalizar atalhos de][DevtoolsCustomKeyboardShortcuts] teclado agora está disponível e ligado por padrão no Microsoft Edge versão 86 ou posterior.  
*   [Emulação: o modo de tela][DevtoolsDeviceModeDualScreenAndFoldables] dupla de suporte agora está disponível e ligado por padrão no Microsoft Edge versão 89 ou posterior.  
*   [Ativar novos recursos de depuração][DevtoolsCssGrid] de grade CSS agora está disponível e ligado por padrão no Microsoft Edge versão 89 ou posterior.  
    
## Fornecer comentários sobre recursos experimentais  

Para fornecer comentários sobre experimentos do Microsoft Edge DevTools ou qualquer outra coisa relacionada ao DevTools.  

*   Envie seus comentários usando o **ícone Enviar Comentários** no DevTools  
*   Tweet à [@EdgeDevTools][TwitterEdgedevtools]  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="O ícone Enviar Comentários no Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   O **ícone Enviar Comentários** no Microsoft Edge DevTools  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Modo de exibição 3D | Microsoft Docs"  
[DevtoolsCssGrid]: ../css/grid.md "Inspecionar grade CSS no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsMoveTabs]: ../customize/index.md "Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Editar estilos e configurações de fonte CSS no painel Estilos no DevTools | Microsoft Docs"  
[DevtoolsIssues]: ../issues/index.md "Localizar e corrigir problemas com a ferramenta Issues do DevTools do Microsoft Edge | Microsoft Docs"  
[DevToolsShortcuts]: ../shortcuts/index.md "Atalhos de teclado do Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Personalizar atalhos de teclado no microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsOpenMain]: ../open/index.md "Abra o Microsoft Edge DevTools | Microsoft Docs"  

[DualScreenWebIndex]: /dual-screen/web/index "Experiências da Web de tela dupla | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obter o emulador surface Duo | Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Como trabalhar com a sam - Introdução a dispositivos de tela dupla | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Usar o emulador Surface Duo | Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Recurso de abrangeção de tela de mídia CSS para detecção de tela dupla | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "A API JavaScript getWindowSegments para dispositivos de tela dupla | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clientes de Área de Trabalho Remota | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "| Samsung"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emular dispositivos de tela dupla e dobrável no Microsoft Edge DevTools | Microsoft Docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
