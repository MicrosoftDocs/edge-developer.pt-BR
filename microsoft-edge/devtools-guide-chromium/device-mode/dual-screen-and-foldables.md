---
description: Use dispositivos virtuais no Microsoft Edge para aprimorar seu site para dispositivos de tela dupla e dobrável.
title: Emular dispositivos de tela dupla e dobrável no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, emulação, dispositivo, simulação, celular, tela dupla, dobrável, Surface Duo, Samsung Fold
ms.openlocfilehash: bc91c0b7c917d82f169dc7d47e047a587d505353
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313110"
---
# Emular dispositivos de tela dupla e dobrável no Microsoft Edge DevTools  

No Microsoft Edge versão 89 ou posterior, você pode emular os seguintes dispositivos de tela dupla e dobrável.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Samsung Galaxy Fold][SamsungMobileGalaxyFold]  
    
Emular os dispositivos e alternar entre as seguintes posturas.  

*   Postura de tela única ou dobrada  
*   Postura de tela dupla ou desdobrada  
    
Ative [AS APIs](#turn-on-experimental-apis) experimentais da Plataforma Web e use o recurso de tela de mídia [CSS][DualScreenDocsCssMedia] e a [API getWindowSegments][DualScreenDocsJSAPI] do JavaScript para aprimorar seu site \(ou aplicativo\) para dispositivos de tela dupla e dobrável.  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Emular o Surface Duo no Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   Emular o Surface Duo no Microsoft Edge  
:::image-end:::  

## Ativar APIs experimentais  

Para usar o [recurso de abrangeção][DualScreenDocsCssMedia] de tela de mídia CSS e [JavaScript getWindowSegments API][DualScreenDocsJSAPI], ative o sinalizador no Microsoft `Experimental Web Platform features` Edge.  Conclua as etapas a seguir.  

1.  Navegue até `edge://flags` .  
1.  In the **Search flags** textbox, enter `Experimental Web Platform features` , choose the Experimental Web Platform **features** flag, and change **Disabled** to **Enabled**.  
1.  Reinicie o Microsoft Edge.  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Ativar o sinalizador de recursos da Plataforma Web Experimental" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   Ativar o sinalizador de **recursos da Plataforma Web Experimental**  
:::image-end:::  

> [!NOTE]
> Se você estiver usando consultas de mídia [CSS][DualScreenDocsCssMedia] ou a API de Enumeração do Segmento do [Windows JavaScript][DualScreenDocsJSAPI] para aprimorar seu site ou aplicativo para [o Surface Duo,][SurfaceDevicesDuo]você também deve ativar o sinalizador de recursos da Plataforma **Web Experimental** no aplicativo Android [Microsoft Edge][GooglePlayMicrosoftEdge] em seu dispositivo [Surface Duo.][SurfaceDevicesDuo]  
> 
> Se o sinalizador de recursos da Plataforma **Web Experimental** estiver ligado no [Microsoft Edge][MicrosoftEdge] para área de trabalho e estiver desligado no aplicativo Android [Microsoft Edge,][GooglePlayMicrosoftEdge]o comportamento do seu site ou aplicativo no emulador Surface Duo na área de trabalho do Microsoft Edge não corresponderá ao aplicativo [Android Microsoft Edge][GooglePlayMicrosoftEdge] no [Surface Duo.][SurfaceDevicesDuo]  Certifique-se de que os sinalizadores corresponderem ao Microsoft Edge do Android e da área de trabalho para usar com êxito o emulador Surface Duo na área [de trabalho do Microsoft Edge.][MicrosoftEdge]  

## Testar em dispositivos de tela dupla e dobrável  

Quando você emular o [Surface Duo][SurfaceDevicesDuo] em uma postura de tela dupla no Microsoft Edge, a seam \(o espaço entre as duas telas\) é desenhada sobre seu site ou aplicativo.  

A exibição emulada corresponde à maneira como seu site \(ou app\) renderiza no aplicativo Android do [Microsoft Edge][GooglePlayMicrosoftEdge] durante a execução no [Surface Duo.][SurfaceDevicesDuo]  Talvez seja preciso atualizar seu site \(ou aplicativo\) para ser exibido melhor ao longo da análise.  Para obter mais informações sobre como adaptar seu site \(ou aplicativo\) à navegação, navegue até Como trabalhar [com aam][DualScreenIntroductionHowWorkSeam].  

A [Barra de Ferramentas de][DevtoolsDeviceModeIndexSimulateMobileViewport] Dispositivo tem recursos adicionais para ajudá-lo a testar seu site ou aplicativo em várias posturas e orientações.  Choose **Rotate** \( ![ Rotate ](../media/rotate-dark-icon.msft.png) \) to rotate the viewport to landscape orientation. Combine o recurso com **Span** \( Span \) para alternar entre tela única ou dobrada e posturas de tela dupla ou ![ ](../media/span-dark-icon.msft.png) desdobradas.  Juntos, os recursos permitem que você teste seu site ou aplicativo em todas as quatro posturas e orientações possíveis.  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matriz de posturas e orientações para dispositivos de tela dupla e dobrável" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Matriz de posturas e orientações para dispositivos de tela dupla e dobrável  
:::image-end:::  

O **ícone da Plataforma Web Experimental** \( ![ ExperimentalApis \) exibe o estado do sinalizador de recursos da Plataforma ](../media/experimental-apis-dark-icon.msft.png) Web **Experimental.**  Se o sinalizador estiver ligado, o ícone será realçado.  Se o sinalizador estiver desligado, o ícone não será realçado.  Para ativar \(ou desativar\) o sinalizador, escolha o ícone ou navegue até e `edge://flags` alterne o sinalizador.  

> [!NOTE]
> A seguir está uma lista de problemas conhecidos atuais.  
> 
> *   Quando você usa um cliente de Área de Trabalho Remota da [Microsoft][RemoteDesktopClientDocs] para se conectar a um computador remoto e emular o [Surface Duo][SurfaceDevicesDuo] ou [Samsung Duoy Fold,][SamsungMobileGalaxyFold]o ponteiro pode treme ou treme.  Se você tiver o problema, [envie comentários.](#getting-in-touch-with-the-microsoft-edge-devtools-team)  

## Recursos adicionais  

Aqui estão recursos adicionais que podem ajudá-lo a aprimorar seu site \(ou aplicativo\) para dispositivos de tela dupla.  

*   Para obter mais informações sobre o desenvolvimento da Web em dispositivos de tela dupla, navegue até [experiências da Web de tela dupla.][DualScreenWebIndex]  
*   Instale o [emulador Surface Duo.][DualScreenAndroidUseEmulator]  O emulador Surface Duo é diferente do emulador no Microsoft Edge, executa o Android e se integra ao [Android Studio.][AndroidDeveloperStudio]  Para obter mais informações, [navegue até Obter o SDK do Surface Duo.][DualScreenAndroidGetDuoSdk]  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Microsoft Edge"  

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
