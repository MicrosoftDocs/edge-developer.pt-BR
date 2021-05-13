---
description: Use dispositivos virtuais em Microsoft Edge para aprimorar seu site para dispositivos de tela dupla e dobráveis.
title: Emular dispositivos de tela dupla e dobráveis Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, emulação, dispositivo, simulação, celular, tela dupla, dobrável, Surface Duo, Samsung Galaxy Fold
ms.openlocfilehash: c3bd3296afa86d9d2c90c164bc3e9088bc043c3c
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564340"
---
# <a name="emulate-dual-screen-and-foldable-devices-in-microsoft-edge-devtools"></a>Emular dispositivos de tela dupla e dobráveis Microsoft Edge DevTools  

Na Microsoft Edge versão 89 ou posterior, você pode emular os seguintes dispositivos de tela dupla e dobrável.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Samsung Galaxy Fold][SamsungMobileGalaxyFold]  
    
Emular os dispositivos e alternar entre as seguintes posturas.  

*   Postura de tela única ou dobrada  
*   Postura de tela dupla ou desdobre  
    
Ative AS [APIs](#turn-on-experimental-apis) experimentais da Plataforma Web e use o recurso de abrangência de tela de mídia [CSS][DualScreenDocsCssMedia] e a [API getWindowSegments javaScript getWindowSegments][DualScreenDocsJSAPI] para aprimorar seu site \(ou app\) para dispositivos de tela dupla e dobráveis.  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Emular o Surface Duo no Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   Emular o Surface Duo no Microsoft Edge  
:::image-end:::  

## <a name="turn-on-experimental-apis"></a>Ativar APIs experimentais  

Para usar o [recurso de][DualScreenDocsCssMedia] abrangência de tela de mídia CSS e a [API javaScript getWindowSegments][DualScreenDocsJSAPI], ative o `Experimental Web Platform features` sinalizador em Microsoft Edge.  Conclua as etapas a seguir.  

1.  Navegue até `edge://flags`.  
1.  Na caixa **de texto Sinalizadores** de Pesquisa, digite , escolha o sinalizador de recursos da Plataforma Web Experimental e `Experimental Web Platform features` altere **Desabilitado** para **Habilitado.** ****  
1.  Reinicie o Microsoft Edge.  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Ativar o sinalizador de recursos da Plataforma Web Experimental" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   Ativar o sinalizador de recursos **da Plataforma Web** Experimental  
:::image-end:::  

> [!NOTE]
> Se você estiver usando consultas de mídia [CSS][DualScreenDocsCssMedia] ou a API de Enumeração de Segmentos do [JavaScript Windows para][DualScreenDocsJSAPI] aprimorar seu site ou aplicativo para o Surface [Duo,][SurfaceDevicesDuo]você também deve ativar o sinalizador de recursos da Plataforma **Web Experimental** no aplicativo Microsoft Edge [Android][GooglePlayMicrosoftEdge] em seu dispositivo [Surface Duo.][SurfaceDevicesDuo]  
> 
> Se o sinalizador de recursos da Plataforma **Web** Experimental estiver ligado na área de trabalho [Microsoft Edge][MicrosoftEdge] e desligado no aplicativo [android Microsoft Edge][GooglePlayMicrosoftEdge], o comportamento do seu site ou aplicativo no emulador do Surface Duo na área de trabalho Microsoft Edge não corresponderá ao aplicativo [android Microsoft Edge][GooglePlayMicrosoftEdge] no [Surface Duo.][SurfaceDevicesDuo]  Certifique-se de que os sinalizadores se matchem entre o Android e a área de trabalho Microsoft Edge usar com êxito o emulador surface Duo em área de [trabalho Microsoft Edge][MicrosoftEdge].  

## <a name="test-on-foldable-and-dual-screen-devices"></a>Teste em dispositivos dobráveis e de tela dupla  

Quando você emular o [Surface Duo][SurfaceDevicesDuo] em uma postura de tela dupla no Microsoft Edge, a seam \(o espaço entre as duas telas\) é desenhada sobre seu site ou aplicativo.  

A exibição emulada corresponde à maneira como seu site \(ou app\) renderiza no aplicativo [Microsoft Edge Android][GooglePlayMicrosoftEdge] durante a execução no [Surface Duo][SurfaceDevicesDuo].  Talvez seja preciso atualizar seu site \(ou app\) para exibir melhor ao longo da emenda.  Para obter mais informações sobre como adaptar seu site \(ou app\) à emenda, navegue até [Como trabalhar com a emenda][DualScreenIntroductionHowWorkSeam].  

A [Barra de Ferramentas de Dispositivo][DevtoolsDeviceModeIndexSimulateMobileViewport] tem recursos adicionais para ajudá-lo a testar seu site ou aplicativo em várias posturas e orientações.  Escolha **Girar** \( ![ Girar ](../media/rotate-dark-icon.msft.png) \) para girar o viewport para a orientação paisagem. Combine o recurso com **Span** \( Span \) para alternar entre as posturas de tela única ou dobrada e de tela dupla ![ ou ](../media/span-dark-icon.msft.png) desdobreada.  Juntos, os recursos permitem que você teste seu site ou aplicativo em todas as quatro posturas e orientações possíveis.  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matriz de posturas e orientações para dispositivos de tela dupla e dobráveis" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Matriz de posturas e orientações para dispositivos de tela dupla e dobráveis  
:::image-end:::  

O **ícone da Plataforma Web** Experimental \( ExperimentalApis \) exibe o estado do sinalizador de recursos da ![ Plataforma Web ](../media/experimental-apis-dark-icon.msft.png) **Experimental.**  Se o sinalizador estiver ligado, o ícone será realçado.  Se o sinalizador estiver desligado, o ícone não será realçado.  Para ativar \(ou desativar\) o sinalizador, escolha o ícone ou navegue até `edge://flags` e alterne o sinalizador.  

> [!NOTE]
> Veja a seguir uma lista de problemas conhecidos atuais.  
> 
> *   Quando você usa um [cliente Área de Trabalho Remota da Microsoft][RemoteDesktopClientDocs] para se conectar a um computador remoto e emular o [Surface Duo][SurfaceDevicesDuo] ou [o Samsung Galaxy Fold][SamsungMobileGalaxyFold], o ponteiro pode tremular ou gaguejar.  Se você executar o problema, [envie comentários](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

## <a name="additional-resources"></a>Recursos adicionais  

Aqui estão recursos adicionais que podem ajudá-lo a aprimorar seu site \(ou app\) para dispositivos de tela dupla.  

*   Para obter mais informações sobre o desenvolvimento da Web em dispositivos de tela dupla, navegue até [Experiências da Web de tela dupla.][DualScreenWebIndex]  
*   Instale o [emulador do Surface Duo.][DualScreenAndroidUseEmulator]  O emulador do Surface Duo é diferente do emulador no Microsoft Edge, executa o Android e se integra ao [Android Studio][AndroidDeveloperStudio].  Para obter mais informações, navegue [até Obter o SDK do Surface Duo][DualScreenAndroidGetDuoSdk].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móveis com o modo de dispositivo Microsoft Edge DevTools | Microsoft Edge"  

[DualScreenWebIndex]: /dual-screen/web/index "Experiências da Web de tela dupla | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obter o emulador do Surface Duo | Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Como trabalhar com a junção – Introdução aos dispositivos de duas telas | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Use o emulador do Surface Duo | Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Recurso de abrangência de tela de mídia CSS para detecção de dualidade de tela | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "A API JavaScript getWindowSegments para dispositivos de duas telas | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clientes de Área de Trabalho Remota | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/global/galaxy/galaxy-fold "Dobra de | Samsung"  
