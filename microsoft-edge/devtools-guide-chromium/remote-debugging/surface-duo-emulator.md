---
description: Introdução aos emuladores Remote Debugging Surface Duo.
title: Introdução aos emuladores Remote Debugging Surface Duo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, depuração remota, Android, Surface Duo
ms.openlocfilehash: f44c85c468de3bdd7727695e3f33269584966231
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230623"
---
# Introdução aos emuladores Remote Debugging Surface Duo  

Neste artigo, você percorre o processo de depuração remota do conteúdo da Web no [aplicativo Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] em um emulador [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] de uma instância da área de trabalho do [Microsoft Edge][MicrosoftEdge].  Para obter informações sobre a depuração em um dispositivo Surface Duo, siga nosso guia para [dispositivos Android de depuração remota][DevtoolsRemoteDebuggingMain].  

## Antes de começar

Instale o [SDK do Surface Duo][MicrosoftDownload100847] antes de executar o [emulador Surface Duo][DualScreenAndroidUseEmulator].  Para obter mais informações, consulte [obter o SDK Surface Duo][DualScreenAndroidGetDuoSdk].  

## Etapa 1: Navegue até edge://inspect  

Abra uma instância da área de trabalho do [Microsoft Edge][MicrosoftEdge]e navegue até `edge://inspect` .  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="A página edge://inspect no Microsoft Edge na área de trabalho" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   A `edge://inspect` página no Microsoft Edge na área de trabalho  
:::image-end:::

> [!NOTE]
> Se a `edge://inspect` página não reconhecer o [emulador Surface Duo][DualScreenAndroidUseEmulator], reinicie o emulador.  

## Etapa 2: iniciar o emulador Surface Duo  

Inicie o [emulador Surface Duo][DualScreenAndroidUseEmulator].  Observe que o emulador exibe duas telas diferentes em execução no emulador.  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="O emulador Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   O emulador Surface Duo  
:::image-end:::  

## Etapa 3: carregar o conteúdo da Web no Microsoft Edge no emulador Surface Duo  

Em qualquer uma das telas, passe o dedo sobre a bandeja de favoritos do [emulador Surface Duo][DualScreenAndroidUseEmulator] para exibir a gaveta de aplicativos.  Escolha **borda** para iniciar o [aplicativo Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx].  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="O aplicativo Microsoft Edge no emulador Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   O aplicativo Microsoft Edge no emulador Surface Duo  
:::image-end:::  

Navegue até o site ou o aplicativo que você deseja depurar no [aplicativo Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx].  

## Etapa 4: depurar o conteúdo da Web pelo emulador Surface Duo  

Volte para a instância da área de trabalho do [Microsoft Edge][MicrosoftEdge].  A `edge://inspect` página agora mostra o **SurfaceDuoEmulator** com uma lista das guias abertas ou [PWAs][ProgressiveWebAppsIndex] que estão em execução no [emulador Surface Duo][DualScreenAndroidUseEmulator].  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="A página edge://inspect exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador" lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   A `edge://inspect` página exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador  
:::image-end:::  

> [!NOTE]
> Se você não vir **SurfaceDuoEmulator** na `edge://inspect` página, tente abrir ou fechar as guias no [aplicativo Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] no [emulador Surface Duo][DualScreenAndroidUseEmulator].  Para obter etapas adicionais de solução de problemas, consulte a [seção solução de problemas para dispositivos Android][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].  

Na lista de guias abertas em execução no emulador, escolha **inspecionar** na guia em que o conteúdo da Web deve ser depurado.  O [Microsoft Edge devtools][DevtoolsIndex] será aberto em uma nova janela.  Escolha **alternar screencast** \ ( ![ alternar screencast ][ImageToggleScreencastIcon] \) para exibir o conteúdo da Web do seu [emulador Surface Duo][DualScreenAndroidUseEmulator] na janela do devtools.  Agora você pode usar o Microsoft Edge DevTools para depurar o conteúdo da Web no [emulador Surface Duo][DualScreenAndroidUseEmulator].  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Usar o Microsoft Edge DevTools para depurar o Bing no aplicativo Microsoft Edge no emulador Surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   Usar o Microsoft Edge DevTools para depurar o Bing no aplicativo Microsoft Edge no emulador Surface Duo  
:::image-end:::  

> [!NOTE]
> Se você ocupar o [aplicativo Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] entre as duas telas no emulador, o screencast refletirá o novo tamanho do aplicativo, mas não a dobradiça.  Para entender como a dobradiça impacta o layout do seu conteúdo da Web, use o [emulador Surface Duo][DualScreenAndroidUseEmulator] em vez do screencast.  

## Recursos adicionais  

A Web é uma ótima plataforma para a nova classe de dobrável e dispositivos de tela dupla porque você pode escrever seu HTML, CSS e JavaScript uma vez e ter uma ótima aparência em dispositivos com tela única, tela dupla e dobrável.  Para obter mais informações, consulte estes recursos adicionais para começar a criar conteúdo da Web para esses novos dispositivos.  

*   [Documentação para criar aplicativos em dispositivos de tela dupla][DualScreenIndex]  
*   [O explicativo da plataforma Web Microsoft Edge para novas APIs para criar experiências na Web no dobrável e em dispositivos de tela dupla][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [Gravação da sessão de dia do desenvolvedor do Microsoft 365: como criar experiências de tela dupla para sites e aplicativos Web][YoutubeDxrzwsqxpvc]  

<!-- image links -->  

[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[ProgressiveWebAppsIndex]: ../../progressive-web-apps-chromium/index.md "Aplicativos Web progressivos no Windows | Documentos da Microsoft"  
[DevtoolsRemoteDebuggingMain]: ./index.md "Introdução à depuração remota de dispositivos Android | Documentos da Microsoft"  
[DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]: ./index.md#troubleshooting-devtools-is-not-detecting-the-android-device "Solução de problemas: o DevTools não está detectando o dispositivo Android-introdução aos dispositivos Android de depuração remota | Documentos da Microsoft"  

[DualScreenIndex]: /dual-screen/index "Criar aplicativos para dispositivos de tela dupla | Documentos da Microsoft"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Use o emulador Surface DUo | Documentos da Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtenha o SDK Surface Duo | Documentos da Microsoft"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Apresentando o novo Microsoft Edge"  
[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "O novo Surface Duo | Microsoft Surface"  
[MicrosoftDownload100847]: https://www.microsoft.com/download/details.aspx?id=100847 "Baixe a versão prévia do SDK do Surface Duo | Centro de download da Microsoft"  

[GooglePlayStoreAppsComMicrosoftEmmx]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge: navegador da Web | GooglePlay"  

[GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitivas de plataforma Web para experiências otimizadas em dobrável dispositivos-MicrosoftEdge/MSEdgeExplainers | GitHub"  

[YoutubeDxrzwsqxpvc]: https://youtu.be/DXrZWsqXPVc "Como criar experiências de tela dupla para o site e os aplicativos Web | YouTube"  
