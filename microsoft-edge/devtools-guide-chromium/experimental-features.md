---
description: Os recursos experimentais mais recentes do Microsoft Edge DevTools
title: Recursos experimentais
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools, experimento
ms.openlocfilehash: c78e9aa5e0b4d808dd67d607a954b185ddcf54e7
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "11003983"
---
# Recursos experimentais  

O Microsoft Edge DevTools fornece acesso a recursos experimentais que ainda estão em desenvolvimento.  Você pode testar e p[fornecer comentários](#providing-feedback-on-experimental-features) antes que cada recurso seja lançado.  

Embora os recursos experimentais estejam disponíveis em todos os canais do Microsoft Edge, você pode obter os recursos experimentais mais recentes usando o Microsoft Edge Canárias Channel.  

## Ativar os recursos experimentais  

Use as etapas a seguir para ativar \ (ou desligado \) recursos experimentais no Microsoft Edge.  

1.  [Abra o devtools][DevtoolsOpen].  
     *   Selecione `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).  Para obter mais informações, consulte [atalhos de teclado do Microsoft Edge devtools][DevToolsShortcuts].  
1.  Abra o painel [configurações][DevToolsCustomizeSettings] .  
    *   Selecione `Shift` + `?` .  Para obter mais informações, navegue até [atalhos de teclado do Microsoft Edge devtools][DevToolsShortcuts].  
1.  No lado esquerdo do painel **configurações** , escolha a seção **experimentos** .  
    
    :::image type="complex" source="./media/experiments-devtools.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/experiments-devtools.msft.png":::
       Lista de experimentos nas configurações do DevTools  
    :::image-end:::  
    
1.  Na página **experimentos** , percorra a lista de todos os recursos experimentais disponíveis e escolha a caixa de seleção ao lado de cada recurso que você deseja testar.  
1.  Feche e abra novamente o Microsoft Edge DevTools.  

> [!NOTE]
> Os recursos experimentais são atualizados constantemente e podem causar problemas de desempenho.  Para desativar um recurso experimental, abra a página **experimentos** e desmarque a caixa de seleção do recurso experimental que você deseja desativar.  

## Recursos experimentais realçados  

As seções a seguir descrevem os novos recursos experimentais que estão disponíveis no Microsoft Edge.  

| Recurso experimental | Microsoft Edge versão |  
|:--- |:--- |  
| [Habilitar a guia Configurações de atalhos de teclado personalizados](#enable-custom-keyboard-shortcuts-settings-tab) | 84 ou posterior |
| [Emulação: suporta o modo de tela dupla](#emulation-support-dual-screen-mode) | 84 ou posterior |  
| [Habilitar novos recursos de depuração de grade CSS](#enable-new-css-grid-debugging-features) | 85 ou posterior |  
| [Habilitar o suporte para mover as guias entre painéis](#enable-support-to-move-tabs-between-panels) | 85 ou posterior |  
| [Habilitar webhint](#enable-webhint) | 85 ou posterior |  
| [Habilitar console de rede](#enable-network-console) | 85 ou posterior |  
| [Habilitar o Visualizador de ordem de origem](#enable-source-order-viewer) | 86 ou posterior |  

### Habilitar a guia Configurações de atalhos de teclado personalizados  

Fornece uma nova página **atalhos** nas [configurações do devtools][DevToolsCustomizeSettings] para corresponder os atalhos de [teclado][DevToolsShortcuts] no código do devtools ao [Microsoft Visual Studio][VisualstudioCode].  

Depois de habilitar o experimento, abra [as configurações do devtools][DevToolsCustomizeSettings] novamente usando selecionar `Shift` + `?` .  Navegue até a página novos **atalhos** .  Selecione **devtools (padrão)** na lista suspensa **coincidir os atalhos de predefinir** e selecione **código do Visual Studio**.  Os atalhos de teclado no DevTools agora correspondem aos atalhos para ações equivalentes no código do Visual Studio.  

:::image type="complex" source="./media/experiments-keyboard-shortcut.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="./media/experiments-keyboard-shortcut.msft.png":::
   Corresponder os atalhos de teclado no código do DevTools para o Visual Studio  
:::image-end:::  

Por exemplo, no Windows, o atalho de teclado para pausar ou continuar a execução de um script no [código do Visual Studio][VisualstudioCodeShortcutsKeyboardWindows] é `F5` .  Com a predefinição **devtools (padrão)** , o mesmo atalho no devtools é `F8` .  Com a predefinição de **código do Visual Studio** , o atalho também é `F5` .  

### Emulação: suporta o modo de tela dupla  

Fornece recursos adicionais para emular dois novos dispositivos de tela dupla e de dobrável no Microsoft Edge.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Dobra Samsung Galaxy][SamsungMobileGalaxyFold]  

EMule os dispositivos e alterne entre as seguintes condições.  

*   postura de tela única ou dobrada  
*   postura de tela dupla ou não dobrada  

Use o recurso [habilitar APIs experimentales](#enable-experimental-apis) para aprimorar seu site \ (ou app \) para um dispositivo.  Você também pode usar as [consultas de mídia CSS e a API de enumeração de segmento do Windows JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].  

<!-- This image was taken in Chromium Canary since we don't yet have an Edge Canary that has Stan's changes -->  

:::image type="complex" source="./media/experiments-dual-screen-emulation.msft.png" alt-text="Emular superfície Duo no Microsoft Edge" lightbox="./media/experiments-dual-screen-emulation.msft.png":::  
   Emular superfície Duo no Microsoft Edge  
:::image-end:::  

#### Habilitar APIs experimentais  

Para [habilitar esse experimento](#turn-on-experimental-features) no Microsoft Edge devtools, siga as etapas a seguir.  

1.  Navegue até `edge://flags` .  
1.  Na caixa de texto de **sinalizadores de pesquisa** , digite `Experimental Web Platform features` , escolha o sinalizador de **recursos da plataforma da Web experimental** e alterar **desabilitado** como **habilitado**.  
1.  Reinicie o Microsoft Edge.  

Para aprimorar seu site ou aplicativo para dispositivos com tela dupla e dobrável, navegue até [consultas de mídia CSS e a API de enumeração de segmento do Windows JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].

[Ative este experimento](#turn-on-experimental-features) no Microsoft Edge devtools.  

1.  Abra uma nova guia no Microsoft Edge e navegue até `edge://flags` .  
1.  Na caixa de texto de **sinalizadores de pesquisa** , insira `Experimental Web Platform features` , escolha **recursos da plataforma da Web experimental**e alterar **desabilitado** como **habilitado**.  
1.  Reinicie o Microsoft Edge.  

Para obter mais informações sobre como aprimorar seu site \ (ou app \) para dispositivos de tela dupla e dobrável, navegue até [consultas de mídia CSS e API de enumeração de segmento do Windows JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].  

:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Habilitar o sinalizador de recursos da plataforma da Web experimental" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   Habilitar o sinalizador de recursos da plataforma da Web experimental  
:::image-end:::  

> [!NOTE]
> Se você estiver usando [consultas de mídia CSS ou a API de enumeração de segmento do Windows JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables] para aprimorar seu site ou aplicativo para o [Surface Duo][SurfaceDevicesDuo], também deverá habilitar o sinalizador de **recursos da plataforma da Web experimental** no [aplicativo Android do Microsoft Edge][GooglePlayMicrosoftEdge] em seu dispositivo [Surface Duo][SurfaceDevicesDuo] .
> 
> Se o sinalizador de **recursos da plataforma da Web experimental** estiver habilitado no [Microsoft Edge da área de trabalho][MicrosoftEdge] e desabilitado no [aplicativo Android do Microsoft Edge][GooglePlayMicrosoftEdge], o comportamento do seu site ou aplicativo no emulador Surface Duo no Microsoft Edge da área de trabalho não será compatível com o [aplicativo Microsoft Edge do Android][GooglePlayMicrosoftEdge] no [Surface Duo][SurfaceDevicesDuo].  Certifique-se de que os sinalizadores sejam compatíveis com o Android e o Microsoft Edge da área de trabalho para usar com êxito o emulador Surface Duo no [Microsoft Edge da área de trabalho][MicrosoftEdge].  

#### Testando em dispositivos dobrável e de tela dupla  

Quando você emula o [Surface Duo][SurfaceDevicesDuo] em uma postura de tela dupla no Microsoft Edge, a **fenda** é desenhada sobre seu site ou aplicativo.  

> [!NOTE]
> A **fenda** é o espaço entre as duas telas.  

A exibição emulada do seu site \ (ou app \) é uma representação correta.  Ele corresponde à exibição no [aplicativo Android do Microsoft Edge][GooglePlayMicrosoftEdge] no [Surface Duo][SurfaceDevicesDuo].  Atualize o conteúdo para exibi-lo melhor ao longo da **fenda**.  Para obter mais informações sobre como adaptar seu site \ (ou app \) à **fenda**, navegue até [como trabalhar com a fenda][DualScreenIntroductionHowWorkSeam] na documentação do Surface Duo.  

A [barra de ferramentas do dispositivo][DevtoolsDeviceModeIndexSimulateMobileViewport] tem recursos adicionais para ajudá-lo a testar seu site ou aplicativo em várias posturas e orientações.  Escolha **girar** \ ( ![ girar ][ImageRotateIcon] \) para girar o visor para a orientação paisagem. Combine o recurso com **span** \ ( ![ span ][ImageSpanIcon] \) para alternar entre as posturas de tela única ou dobrada e de tela dupla ou sem dobra.  Juntos, os recursos permitem testar o seu site ou aplicativo em todas as quatro posturas e orientações possíveis.  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matriz de posturas e orientações para dispositivos com tela dupla e dobrável" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Matriz de posturas e orientações para dispositivos com tela dupla e dobrável  
:::image-end:::  

O ícone de **recursos da plataforma da Web experimental** \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \) exibe o estado do sinalizador de **recursos da plataforma da Web experimental** .  Se o sinalizador estiver ativado, o ícone será realçado.  Se o sinalizador estiver desativado, o ícone não será realçado.  Para ativar \ (ou desligar \) o sinalizador, escolha o ícone ou navegue até `edge://flags` o sinalizador e alterne-o.  

#### Recursos adicionais  
*   Para obter mais informações sobre o desenvolvimento, navegue até [experiências na Web de tela dupla][DualScreenWebIndex].  
*   Instale o emulador Surface Duo].  Ele é diferente do emulador no Microsoft Edge.  Ele emula o Surface duo que executa o Android e integra-se ao [Android Studio][AndroidDeveloperStudio].  Para obter mais informações, navegue para [obter o SDK Surface Duo][DualScreenAndroidGetDuoSdk].  

### Habilitar novos recursos de depuração de grade CSS  

Aprimora as visualizações na página quando você depura sites que têm layouts de grade CSS.  Você pode personalizar ainda mais as sobreposições nas configurações do DevTools.  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="Recurso de depuração de grade CSS" lightbox="./media/experiments-grid.msft.png":::
   Recurso de depuração de grade CSS  
:::image-end:::  

Para visualizar os recursos experimentais mais recentes, conclua as ações a seguir.  

1.  Na seção **experimentos** , escolha a caixa de seleção **habilitar novos recursos de depuração de grade CSS (opções de configuração disponíveis no painel de barra lateral de layout nos elementos após a reinicialização)** .  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar o suporte para mover as guias entre painéis  

Normalmente, ferramentas como **elementos** e **rede** só podem abrir no painel principal localizado na parte superior da devtools.  Ferramentas como **modo de exibição 3D** e **problemas** que normalmente são abertos apenas no painel de **gaveta** localizado na parte inferior da devtools.  Depois de escolher o experimento, você poderá mover ferramentas entre os painéis superior e inferior.  Para mover uma ferramenta, passe o mouse sobre a guia, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **mover para o início** ou **mover para o fim**.   Este experimento permite que você personalize o layout do DevTools.  Para mostrar ou ocultar o painel de **gavetas** , selecione `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Mover guias entre painéis" lightbox="./media/experiments-move-panels.msft.png":::
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

O experimento do [webhint][WebhintMain] exibe os comentários do webhint no painel [problemas][DevtoolsIssues] .  Selecione um problema para exibir a documentação da solução e uma lista dos recursos afetados em seu site.  Selecione um link de recurso para abrir o painel de **rede**, **fontes**ou **elementos** relevantes no devtools.  

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="Comentários da webhint no painel problemas" lightbox="./media/experiments-webhint.msft.png":::
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
1.  Selecione **Enviar**.  

:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Console de rede na gaveta do console" lightbox="./media/network-network-console.msft.png":::
   **Console de rede** na gaveta do **console**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar o Visualizador de ordem de origem  

O **Visualizador de ordem de origem** é um experimento que exibe a ordem dos elementos na fonte da página.  A ordem de exibição na tela pode ser diferente da ordem da fonte, que confundi o leitor de tela e os usuários de teclado.  Use o **Visualizador de pedido de origem** para encontrar as diferenças entre ordem de exibição na tela e a ordem da fonte.  

Depois de habilitar o experimento, certifique-se de reiniciar o DevTools.  Para usar o Visualizador de ordem de origem:  

1.  Abrir o painel de **elementos** .  
1.  Abra o painel **acessibilidade** no painel gaveta \ (inferior \).  
1.  Na seção **Visualizador de ordem de origem** , marque a caixa de seleção **Mostrar ordem de origem** .  
1.  Realce qualquer elemento HTML para exibir uma sobreposição que a ordem na fonte da página.  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Visualizador de ordem de origem no painel Acessibilidade" lightbox="./media/experiments-source-order-viewer.msft.png":::
   **Visualizador de ordem de origem** no painel **acessibilidade**  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## Recursos experimentais anteriores  

*   o [modo de exibição 3D][Devtools3dViewIndex] agora está disponível e ativado por padrão no Microsoft Edge versão 83 ou posterior.  

## Fornecer comentários sobre os recursos experimentais  

Para fornecer comentários sobre o Microsoft Edge DevTools experimentos ou qualquer outro item relacionado ao DevTools.  

*   Envie seus comentários usando o ícone **enviar comentários** no devtools  
*   Tweet em [@EdgeDevTools][TwitterEdgedevtools]  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="O ícone enviar comentários no Microsoft Edge DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
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

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Modo de exibição 3D | Documentos da Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Configurações-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ./device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsIssues]: ./issues/index.md "Localizar e corrigir problemas com a ferramenta problemas do DevTools Microsoft Edge | Documentos da Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Atalhos de teclado do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsOpen]: ./open.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  

[DualScreenWebIndex]: /dual-screen/web/index "Experiências na Web de tela dupla | Documentos da Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obter o emulador Surface Duo | Documentos da Microsoft"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Como trabalhar com a fenda-introdução a dispositivos de tela dupla | Documentos da Microsoft"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[VisualstudioCode]: https://code.visualstudio.com "Código do Microsoft Visual Studio"  
[VisualstudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Atalhos de teclado de código do Visual Studio para Windows | Código do Microsoft Visual Studio"  

[GitHubMicrosoftedgeMsedgeexplainerFoldables]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitivas de plataforma Web para experiências otimizadas em dispositivos dobrável | GitHub"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Galaxy dobre | Samsung"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
