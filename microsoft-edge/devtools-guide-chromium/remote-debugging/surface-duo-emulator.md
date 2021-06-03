---
description: Começar com emuladores do Surface Duo de Depuração Remota.
title: Começar com emuladores do Surface Duo de Depuração Remota
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, depuração remota, android, surface duo
ms.openlocfilehash: 49b16f3c920735b34d44455bae437442cac3bf6e
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461238"
---
# <a name="get-started-with-remote-debugging-surface-duo-emulators"></a>Começar a depurar remotamente os emuladores do Surface Duo  

Neste artigo, você passa pelo processo de depuração remota do conteúdo da Web no aplicativo [Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] em um emulador [do Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] de uma instância da área de trabalho [Microsoft Edge][MicrosoftEdge].  Para obter informações sobre a depuração em um dispositivo Surface Duo, siga nosso guia para [depuração][DevtoolsRemoteDebuggingMain]remota de dispositivos Android .  

## <a name="before-you-begin"></a>Antes de começar

Instale o [SDK do Surface Duo][MicrosoftDownload100847] antes de executar o [emulador do Surface Duo.][DualScreenAndroidUseEmulator]  Para obter mais informações, navegue [até Obter o SDK do Surface Duo][DualScreenAndroidGetDuoSdk].  

## <a name="step-1-navigate-to-edgeinspect"></a>Etapa 1: Navegue até edge://inspect  

Abra uma instância da área de [trabalho Microsoft Edge][MicrosoftEdge]e navegue até `edge://inspect` .  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="A edge://inspect no Microsoft Edge na área de trabalho" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   A `edge://inspect` página em Microsoft Edge na área de trabalho  
:::image-end:::

> [!NOTE]
> Se a `edge://inspect` página não reconhecer o [emulador do Surface Duo,][DualScreenAndroidUseEmulator]reinicie o emulador.  

## <a name="step-2-launch-the-surface-duo-emulator"></a>Etapa 2: Iniciar o emulador do Surface Duo  

Iniciar o [emulador do Surface Duo.][DualScreenAndroidUseEmulator]  Observe que o emulador exibe duas telas diferentes em execução no emulador.  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="O emulador do Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   O emulador do Surface Duo  
:::image-end:::  

## <a name="step-3-load-your-web-content-in-microsoft-edge-on-the-surface-duo-emulator"></a>Etapa 3: carregar o conteúdo da Web Microsoft Edge no emulador do Surface Duo  

Em uma das telas, passe o dedo para cima na Bandeja de Favoritos do [emulador do Surface Duo][DualScreenAndroidUseEmulator] para exibir a Gaveta de Aplicativos.  Escolha **Borda para** iniciar o Microsoft Edge [app][GooglePlayStoreAppsComMicrosoftEmmx].  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="O Microsoft Edge no emulador do Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   O Microsoft Edge no emulador do Surface Duo  
:::image-end:::  

Navegue até o site ou aplicativo que você deseja depurar no Microsoft Edge [app][GooglePlayStoreAppsComMicrosoftEmmx].  

## <a name="step-4-debug-your-web-content-from-the-surface-duo-emulator"></a>Etapa 4: Depurar o conteúdo da Web do emulador do Surface Duo  

Alternar de volta para a instância da área de [trabalho Microsoft Edge][MicrosoftEdge].  A `edge://inspect` página agora mostra o **SurfaceDuoEmulator** com uma lista das guias abertas ou [PWAs][ProgressiveWebAppsIndex] que estão sendo executados no [emulador surface Duo][DualScreenAndroidUseEmulator].  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="A edge://inspect exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador" lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   A página exibe uma lista das guias abertas no aplicativo Microsoft Edge `edge://inspect` em execução no emulador  
:::image-end:::  

> [!NOTE]
> Se **SurfaceDuoEmulator** não for exibido na página, tente abrir ou fechar guias no aplicativo Microsoft Edge no `edge://inspect` [Emulador surface Duo][DualScreenAndroidUseEmulator]. [][GooglePlayStoreAppsComMicrosoftEmmx]  Para obter etapas adicionais de solução de problemas, navegue até a seção [solução de problemas para dispositivos Android.][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]  

Na lista de guias abertas em execução **** no emulador, escolha inspecionar na guia que tem o conteúdo da Web a ser depurado.  O [Microsoft Edge DevTools][DevtoolsIndex] será aberto em uma nova janela.  Escolha **Toggle Screencast** \( Toggle Screencast \) para exibir o conteúdo da Web a partir do ![ ](../media/toggle-screencast-icon.msft.png) [emulador do Surface Duo][DualScreenAndroidUseEmulator] na janela DevTools.  Agora você pode usar o Microsoft Edge DevTools para depurar o conteúdo da Web no [emulador do Surface Duo.][DualScreenAndroidUseEmulator]  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Usando o Microsoft Edge DevTools para depurar Bing no aplicativo Microsoft Edge no emulador do Surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   Usando o Microsoft Edge DevTools para depurar Bing no aplicativo Microsoft Edge no emulador do Surface Duo  
:::image-end:::  

> [!NOTE]
> Se você abranger o [aplicativo Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] em ambas as telas no emulador, o screencast refletirá o novo tamanho do aplicativo, mas não a dobradiça.  Para entender como a dobradiça afeta o layout do conteúdo da Web, use o [emulador do Surface Duo][DualScreenAndroidUseEmulator] em vez do screencast.  

## <a name="additional-resources"></a>Recursos adicionais  

A Web é uma ótima plataforma para a nova classe de dispositivos de tela dupla e dobrável porque você pode gravar seu HTML, CSS e JavaScript uma vez e ter uma ótima aparência em dispositivos de tela única, de tela dupla e dobrável.  Para obter mais informações, navegue até os seguintes recursos adicionais para começar a criar conteúdo da Web para esses novos dispositivos.  

*   [Documentação para criar aplicativos em dispositivos de tela dupla][DualScreenIndex]  
*   [O Microsoft Edge explicador da plataforma Web para novas APIs para criar experiências da Web em dispositivos dobráveis e de tela dupla][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [Gravação da Microsoft 365 dia do desenvolvedor: como criar experiências de tela dupla para sites e aplicativos Web][YoutubeDxrzwsqxpvc]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) ferramentas de desenvolvedor | Microsoft Docs"  
[ProgressiveWebAppsIndex]: ../../progressive-web-apps-chromium/index.md "Aplicativos Web progressivos Windows | Microsoft Docs"  
[DevtoolsRemoteDebuggingMain]: ./index.md "Começar com a depuração remota de dispositivos Android | Microsoft Docs"  
[DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]: ./index.md#troubleshooting-devtools-is-not-detecting-the-android-device "Solução de problemas: o DevTools não está detectando o dispositivo Android - Começar com a depuração remota de dispositivos Android | Microsoft Docs"  

[DualScreenIndex]: /dual-screen/index "Criar aplicativos para dispositivos de tela | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Use o emulador Surface DUo | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obter o SDK do Surface Duo | Microsoft Docs"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Apresentando o novo Microsoft Edge"  
[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "O novo Surface Duo | Microsoft Surface"  
[MicrosoftDownload100847]: https://www.microsoft.com/download/details.aspx?id=100847 "Baixar o Surface Duo SDK Preview Release | Centro de Download da Microsoft"  

[GooglePlayStoreAppsComMicrosoftEmmx]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge: Navegador da Web | GooglePlay"  

[GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitivas da plataforma Web para experiências iluminadas em dispositivos dobráveis - MicrosoftEdge/MSEdgeExplainers | GitHub"  

[YoutubeDxrzwsqxpvc]: https://youtu.be/DXrZWsqXPVc "Como criar experiências de tela dupla para o site e aplicativos web | YouTube"  
