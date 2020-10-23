---
description: Os recursos experimentais mais recentes do Microsoft Edge DevTools
title: Recursos experimentais
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/21/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools, experimento
ms.openlocfilehash: b620388df309109e28ab8b9c010dfd448ca906f7
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/23/2020
ms.locfileid: "11133828"
---
# Recursos experimentais  

O Microsoft Edge DevTools fornece acesso a recursos experimentais que ainda estão em desenvolvimento.  Você pode testar e [fornecer comentários](#providing-feedback-on-experimental-features) antes que cada recurso seja lançado.  

Embora os recursos experimentais estejam disponíveis em todos os canais do Microsoft Edge, você pode obter os recursos experimentais mais recentes usando o Microsoft Edge Canárias Channel.  

## Ativar os recursos experimentais  

Para ativar \ (ou desligar \) recursos experimentais no Microsoft Edge, use as etapas a seguir.  

1.  [Abra o devtools][DevtoolsOpen].  
     *   Selecione `Control` + `Shift` + `I` \ (Windows, Linux \) ou `Command` + `Option` + `I` \ (MacOS \).  Para obter mais informações, navegue até [atalhos de teclado do Microsoft Edge devtools][DevToolsShortcuts].  
1.  Abra o painel [configurações][DevToolsCustomizeSettings] .  
    *   Selecione `Shift` + `?` .  Para obter mais informações, navegue até [atalhos de teclado do Microsoft Edge devtools][DevToolsShortcuts].  
1.  No lado esquerdo do painel **configurações** , escolha a seção **experimentos** .  
    
    :::image type="complex" source="./media/experiments-devtools.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/experiments-devtools.msft.png":::
       Lista de experimentos nas **configurações** do devtools  
    :::image-end:::  
    
1.  Na página **experimentos** , percorra a lista de todos os recursos experimentais disponíveis e escolha a caixa de seleção ao lado de cada recurso que você deseja testar.  
1.  Feche e abra novamente o Microsoft Edge DevTools.  

> [!NOTE]
> Os recursos experimentais são atualizados constantemente e podem causar problemas de desempenho.  Para desativar um recurso experimental, abra a página **experimentos** e desmarque a caixa de seleção do recurso experimental que você deseja desativar.  

## Recursos experimentais realçados  

As seções a seguir descrevem os novos recursos experimentais que estão disponíveis no Microsoft Edge.  

| Recurso experimental | Microsoft Edge versão |  
|:--- |:--- |  
| [Emulação: suporta o modo de tela dupla](#emulation-support-dual-screen-mode) | 84 ou posterior |  
| [Habilitar novos recursos de depuração de grade CSS](#enable-new-css-grid-debugging-features) | 85 ou posterior |  
| [Habilitar o suporte para mover as guias entre painéis](#enable-support-to-move-tabs-between-panels) | 85 ou posterior |  
| [Habilitar webhint](#enable-webhint) | 85 ou posterior |  
| [Habilitar console de rede](#enable-network-console) | 85 ou posterior |  
| [Visualizador de ordem de origem](#source-order-viewer) | 86 ou posterior |  
| [Habilitar o editor de atalhos de teclado](#enable-keyboard-shortcut-editor) | 87 ou posterior |  

### Emulação: suporta o modo de tela dupla  

Fornece recursos adicionais para emular dois novos dispositivos de tela dupla e de dobrável no Microsoft Edge.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Dobra Samsung Galaxy][SamsungMobileGalaxyFold]  

EMule os dispositivos e alterne entre as seguintes condições.  

*   postura de tela única ou dobrada  
*   postura de tela dupla ou não dobrada  
    
[Habilite APIs experimentais da Web Platform](#enable-experimental-apis) e use o [recurso de distribuição de tela de mídia CSS][DualScreenDocsCssMedia] e a [API JavaScript getWindowSegments][DualScreenDocsJSAPI] para aprimorar seu site \ (ou app \) para dispositivos de tela dupla e dobrável.  

:::image type="complex" source="./media/experiments-surface-duo-emulation.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/experiments-surface-duo-emulation.msft.png":::  
   Emular superfície Duo no Microsoft Edge  
:::image-end:::  

#### Habilitar APIs experimentais  

Para usar o [recurso de distribuição de tela de mídia CSS][DualScreenDocsCssMedia] e a [API de getWindowSegments JavaScript][DualScreenDocsJSAPI], ative o `Experimental Web Platform features` sinalizador no Microsoft Edge.  Conclua as etapas a seguir.  

1.  Navegue até `edge://flags` .  
1.  Na caixa de texto de **sinalizadores de pesquisa** , digite `Experimental Web Platform features` , escolha o sinalizador de **recursos da plataforma da Web experimental** e alterar **desabilitado** como **habilitado**.  
1.  Reinicie o Microsoft Edge.  

:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   Habilitar o sinalizador de recursos da plataforma da Web experimental  
:::image-end:::  

> [!NOTE]
> Se você estiver usando [consultas de mídia CSS][DualScreenDocsCssMedia] ou a [API de enumeração de segmento do Windows JavaScript][DualScreenDocsJSAPI] para aprimorar seu site ou aplicativo para o [Surface Duo][SurfaceDevicesDuo], também deverá habilitar o sinalizador de **recursos da plataforma da Web experimental** no [aplicativo Android do Microsoft Edge][GooglePlayMicrosoftEdge] em seu dispositivo [Surface Duo][SurfaceDevicesDuo] .  
> 
> Se o sinalizador de **recursos da plataforma da Web experimental** estiver habilitado no [Microsoft Edge da área de trabalho][MicrosoftEdge] e desabilitado no [aplicativo Android do Microsoft Edge][GooglePlayMicrosoftEdge], o comportamento do seu site ou aplicativo no emulador Surface Duo no Microsoft Edge da área de trabalho não corresponde ao [aplicativo Android do Microsoft Edge][GooglePlayMicrosoftEdge] no [Surface Duo][SurfaceDevicesDuo].  Certifique-se de que os sinalizadores sejam compatíveis com o Android e o Microsoft Edge da área de trabalho para usar com êxito o emulador Surface Duo no [Microsoft Edge da área de trabalho][MicrosoftEdge].  

#### Testando em dispositivos dobrável e de tela dupla  

Quando você emula o [Surface Duo][SurfaceDevicesDuo] em uma postura de tela dupla no Microsoft Edge, a fenda \ (o espaço entre as duas telas \) é desenhada em seu site ou aplicativo.  

A exibição emulada corresponde à maneira como seu site \ (ou app \) renderiza no [aplicativo Android do Microsoft Edge][GooglePlayMicrosoftEdge] em execução em [Surface Duo][SurfaceDevicesDuo].  Pode ser necessário atualizar seu website \ (ou app \) para ser exibido melhor ao longo da fenda.  Para obter mais informações sobre como adaptar seu site \ (ou app \) à fenda, navegue até [como trabalhar com a fenda][DualScreenIntroductionHowWorkSeam].  

A [barra de ferramentas do dispositivo][DevtoolsDeviceModeIndexSimulateMobileViewport] tem recursos adicionais para ajudá-lo a testar seu site ou aplicativo em várias posturas e orientações.  Escolha **girar** \ ( ![ girar ][ImageRotateIcon] \) para girar o visor para a orientação paisagem. Combine o recurso com **span** \ ( ![ span ][ImageSpanIcon] \) para alternar entre as posturas de tela única ou dobrada e de tela dupla ou sem dobra.  Juntos, os recursos permitem testar o seu site ou aplicativo em todas as quatro posturas e orientações possíveis.  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Matriz de posturas e orientações para dispositivos com tela dupla e dobrável  
:::image-end:::  

O ícone de **recursos da plataforma da Web experimental** \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \) exibe o estado do sinalizador de **recursos da plataforma da Web experimental** .  Se o sinalizador estiver ativado, o ícone será realçado.  Se o sinalizador estiver desativado, o ícone não será realçado.  Para ativar \ (ou desligar \) o sinalizador, navegue até `edge://flags` e alterne o sinalizador.  

<!-- Commenting out until the icon issue is fixed in Edge Canary
The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.  If the flag is turned on, the icon is highlighted.  If the flag is turned off, the icon is not highlighted.  To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.   -->  

Aqui estão recursos adicionais que podem ajudá-lo a aprimorar seu website \ (ou app \) para dispositivos de tela dupla.  

*   Para obter mais informações sobre o desenvolvimento da Web em dispositivos de tela dupla, acesse [experiências na Web de tela dupla][DualScreenWebIndex].  
*   Instale o [emulador Surface Duo][DualScreenAndroidUseEmulator].  Ele é diferente do emulador no Microsoft Edge, emula o Surface Duo executando Android e integra-se ao [Android Studio][AndroidDeveloperStudio].  Para obter mais informações, navegue para [obter o SDK Surface Duo][DualScreenAndroidGetDuoSdk].  

> [!NOTE]
> Veja a seguir uma lista de problemas conhecidos atuais.  
> 
> *   Ao usar um [cliente de área de trabalho remota da Microsoft][RemoteDesktopClientDocs] para se conectar a um computador remoto e emular o [Surface Duo][SurfaceDevicesDuo] ou a [dobra do Galaxy Galaxy][SamsungMobileGalaxyFold], o ponteiro pode se trave.  Se você tiver problemas, [envie comentários](#providing-feedback-on-experimental-features).  

### Habilitar novos recursos de depuração de grade CSS  

Este recurso experimental fornece uma série de novas visualizações para ajudar você a depurar layouts de grade CSS.  Para visualizar os recursos experimentais mais recentes, [habilite este experimento](#turn-on-experimental-features) e recarregue o devtools.  Este experimento está ativado por padrão no Microsoft Edge versão 87 ou posterior.  

#### Exibir sobreposições de grade de foco com a ferramenta inspecionar  

A ferramenta **inspecionar** fornece uma maneira rápida de identificar e Visualizar layouts de grade CSS em um site passando o mouse sobre eles.  Escolha o ícone **inspecionar** \ ( ![ inspecionar ](./media/inspect-icon.msft.png) \) no canto superior esquerdo do devtools.  Em seguida, passe o mouse sobre um elemento de grade no site que você está depurando.  As estruturas de tópicos são exibidas ao lado da grade, e o sombreamento indica o local das lacunas da grade, se houver.  

:::image type="complex" source="./media/grid-inspect.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/grid-inspect.msft.png":::
   Visualização de grades com a ferramenta inspecionar  
:::image-end:::  

#### Exibindo sobreposições de grade persistente  

No Microsoft Edge versão 86 ou posterior, o recurso experimental da CSS da CSS também oferece a opção de habilitar sobreposições de grade persistente.  As sobreposições persistentes fornecem vários benefícios.  

*   As sobreposições persistentes permanecem visíveis na página enquanto você rola, move o mouse e usa outros recursos do DevTools.  
*   Várias sobreposições persistentes podem ser habilitadas ao mesmo tempo, permitindo que você reveja vários layouts de grade ao mesmo tempo.  
*   Sobreposições persistentes oferecem muitas opções de configuração, como ocultar ou mostrar nomes na área de grade, lacunas de grade, tamanhos de faixa e assim por diante.  

As duas maneiras de alternar uma sobreposição de grade persistente.  

*   Escolha o ícone de elipse de **grade** ao lado de qualquer elemento de grade mostrado na árvore dom da ferramenta de **elementos** .  
    
    :::image type="complex" source="./media/grid-adorner.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/grid-adorner.msft.png":::
       Ícone de elipse de grade na ferramenta **elementos**  
    :::image-end:::  
    
*   Abra o painel novo **layout** localizado na ferramenta elementos e escolha a caixa de seleção ao lado de cada elemento de grade que você deseja realçar.  
    
    :::image type="complex" source="./media/grid-layout-zoom.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/grid-layout-zoom.msft.png":::
       Painel de **layout** no devtools  
    :::image-end:::  
    
#### Configurando sobreposições persistentes  

No Microsoft Edge versão 86 ou posterior, o novo painel de **layout** está localizado na ferramenta **elementos** juntamente com as guias **estilos** e **calculadas** .  O painel de **layout** superfícies as opções de configuração para sobreposições persistentes.  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/experiments-grid.msft.png":::
   Recurso de depuração de grade CSS  
:::image-end:::  

### Habilitar o suporte para mover as guias entre painéis  

Normalmente, ferramentas como **elementos** e **rede** só podem abrir no painel principal localizado na parte superior da devtools.  Ferramentas como **modo de exibição 3D** e **problemas** que normalmente são abertos apenas no painel de **gaveta** localizado na parte inferior da devtools.  Depois de escolher o experimento, você poderá mover ferramentas entre os painéis superior e inferior.  Para mover uma ferramenta, passe o mouse sobre a guia, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **mover para o início** ou **mover para o fim**.   Este experimento permite que você personalize o layout do DevTools.  Para mostrar ou ocultar o painel de **gavetas** , selecione `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/experiments-move-panels.msft.png":::
   Mover guias entre painéis  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar webhint  

[webhint][WebhintMain] é uma ferramenta de código-fonte aberto que fornece comentários em tempo real para sites e páginas da Web locais.  O tipo de comentário fornecido pela [webhint][WebhintMain].  

*   acessibilidade  
*   compatibilidade entre navegadores  
*   segurança  
*   execução  
*   PWAs  
*   outros problemas comuns de desenvolvimento na Web  

O experimento do [webhint][WebhintMain] exibe os comentários do webhint no painel [problemas][DevtoolsIssues] .  Escolha um problema para exibir a documentação da solução e uma lista dos recursos afetados em seu site.  Escolha um link de recurso para abrir o painel de **rede**, **fontes**ou **elementos** relevantes no devtools.  

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/experiments-webhint.msft.png":::
   Comentários da webhint no painel **problemas**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar console de rede  

**Console de rede** é o título de trabalho de um experimento para fazer solicitações de rede sintéticas por http.  Você pode usar o experimento do **console de rede** para enviar solicitações de API da Web.  

Depois de habilitar o experimento, certifique-se de reiniciar o DevTools.  Para usar o **console de rede**, use as etapas a seguir.  

1.  Abra o painel **rede** .  
1.  Localize a solicitação de rede que você deseja alterar e envie novamente.  
1.  Abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **Editar e reproduzir**.  
1.  Quando o **console de rede** for aberto, edite as informações de solicitação de rede.  
1.  Escolha **Enviar**.  

:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/network-network-console.msft.png":::
   **Console de rede** na gaveta do **console**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Visualizador de ordem de origem  

O **Visualizador de ordem de origem** é um experimento que exibe a ordem dos elementos na fonte da página.  A ordem de exibição na tela pode ser diferente da ordem da fonte, que confundi o leitor de tela e os usuários de teclado.  Use o **Visualizador de pedido de origem** para encontrar as diferenças entre ordem de exibição na tela e a ordem da fonte.  

Depois de habilitar o experimento, certifique-se de reiniciar o DevTools.  Para usar o **Visualizador de ordem de origem**, use as etapas a seguir.  

1.  Abrir o painel de **elementos** .  
1.  Abra o painel **acessibilidade** no painel gaveta \ (inferior \).  
1.  Na seção **Visualizador de ordem de origem** , escolha a caixa de seleção **Mostrar ordem de origem** .  
1.  Realce qualquer elemento HTML para exibir uma sobreposição que a ordem na fonte da página.  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/experiments-source-order-viewer.msft.png":::
   **Visualizador de ordem de origem** no painel **acessibilidade**  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Habilitar o editor de atalhos de teclado

Com o **Editor de atalhos de teclado** ativado o experimento, agora você pode personalizar os atalhos de teclado para qualquer ação no devtools.  Para personalizar o atalho de teclado para uma ação específica, conclua as etapas a seguir.  

1.  [Abra o devtools][DevtoolsOpenMain].  
1.  Abrir [as configurações][DevToolsCustomizeSettings].
    *   Selecione `Shift` + `?` .  
1.  Navegue até a página **atalhos** .  
1.  Escolha a ação que você deseja personalizar.  
1.  Escolha o ícone **Editar** \ ( ![ EditKeyboardShortcut ][ImageEditKeyboardShortcutIcon] \).  
    
    :::image type="complex" source="./media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       Escolha a ação que deseja personalizar na página **atalhos** em [configurações][DevToolsCustomizeSettings]
    :::image-end:::  
    
1.  No teclado, selecione as teclas que você deseja associar à ação.
    
    :::image type="complex" source="./media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Selecione as teclas que você deseja atribuir à ação
    :::image-end:::  
    
1.  Para salvar seu novo atalho de teclado, escolha a marca de seleção \ (![CheckmarkKeyboardShortcut][ImageCheckmarkKeyboardShortcutIcon]\) ícone.
    
    :::image type="complex" source="./media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Escolher o ícone de marca de seleção para salvar o novo atalho de teclado
    :::image-end:::  
    
1.  Selecione o novo atalho de teclado para disparar a ação no DevTools.  
    
Na página **atalhos** , o ícone de **atalho de teclado personalizado** \ ( ![ CustomKeyboardShortcut ][ImageCustomKeyboardShortcutIcon] \) exibe os atalhos de teclado que você personalizou.  Para redefinir todos os atalhos, escolha **restaurar atalhos padrão**.  

Quando você estiver editando os atalhos de teclado para uma ação, para descartar suas alterações, escolha o ícone X \ ( ![ XKeyboardShortcut ][ImageXKeyboardShortcutIcon] \).  Para remover atalhos de uma ação específica, escolha o ícone **excluir atalho** \ ( ![ DeleteKeyboardShortcut ][ImageDeleteKeyboardShortcutIcon] \).  Para adicionar vários atalhos para uma ação, escolha **Adicionar um atalho**.

> [!NOTE]
> Se um atalho de teclado estiver atribuído atualmente a outra ação, você não poderá salvá-lo para uma nova ação.  Você deve primeiro excluir o atalho de teclado para a ação anterior e, em seguida, adicioná-lo à nova ação.  

## Recursos experimentais anteriores  

*   o [modo de exibição 3D][Devtools3dViewIndex] agora está disponível e ativado por padrão no Microsoft Edge versão 83 ou posterior.  
*   [Personalizar atalhos de teclado][DevtoolsCustomKeyboardShortcuts] agora está disponível e ativado por padrão no Microsoft Edge versão 86 ou posterior.  

## Fornecer comentários sobre os recursos experimentais  

Para fornecer comentários sobre o Microsoft Edge DevTools experimentos ou qualquer outro item relacionado ao DevTools.  

*   Envie seus comentários usando o ícone **enviar comentários** no devtools  
*   Tweet em [@EdgeDevTools][TwitterEdgedevtools]  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   O ícone **enviar comentários** no Microsoft Edge devtools  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  
-->  

<!-- image links -->  

[ImageRotateIcon]: ./media/rotate-dark-icon.msft.png  
[ImageSpanIcon]: ./media/span-dark-icon.msft.png  
[ImageExperimentalApisIcon]: ./media/experimental-apis-dark-icon.msft.png  
[ImageEditKeyboardShortcutIcon]: ./media/edit-keyboard-shortcut-icon.msft.png  
[ImageCheckmarkKeyboardShortcutIcon]: ./media/checkmark-keyboard-shortcut-icon.msft.png  
[ImageCustomKeyboardShortcutIcon]: ./media/custom-keyboard-shortcut-icon.msft.png  
[ImageDeleteKeyboardShortcutIcon]: ./media/delete-keyboard-shortcut-icon.msft.png  
[ImageXKeyboardShortcutIcon]: ./media/discard-changes-keyboard-shortcut-icon.msft.png  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Modo de exibição 3D | Documentos da Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Configurações-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ./device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsIssues]: ./issues/index.md "Localizar e corrigir problemas com a ferramenta problemas do DevTools Microsoft Edge | Documentos da Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Atalhos de teclado do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsOpen]: ./open.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsCustomKeyboardShortcuts]: ./customize/shortcuts.md "Personalizar atalhos de teclado no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsOpenMain]: ./open.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  

[DualScreenWebIndex]: /dual-screen/web/index "Experiências na Web de tela dupla | Documentos da Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obter o emulador Surface Duo | Documentos da Microsoft"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Como trabalhar com a fenda-introdução a dispositivos de tela dupla | Documentos da Microsoft"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Use o emulador Surface Duo | Documentos da Microsoft"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Tela de mídia CSS – recurso de abrangência para detecção de tela dupla | Documentos da Microsoft"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "A API JavaScript getWindowSegments para dispositivos de tela dupla | Documentos da Microsoft"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clientes de área de trabalho remota | Documentos da Microsoft"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Galaxy dobre | Samsung"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
