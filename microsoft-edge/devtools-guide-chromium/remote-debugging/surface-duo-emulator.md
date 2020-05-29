---
title: Introdução aos emuladores Remote Debugging Surface Duo
author: zoherghadyali
ms.author: zoghadya
ms.date: 04/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, depuração remota, Android, Surface Duo
ms.openlocfilehash: af6fa6433b0bc6bba0599e6e9a805235504caadd
ms.sourcegitcommit: 966bfc60040acc794b6ee20eb2084bc8264a4852
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2020
ms.locfileid: "10621499"
---
# Introdução aos emuladores Remote Debugging Surface Duo

Neste artigo, você percorre o processo de depuração remota do conteúdo da Web no [aplicativo Microsoft Edge][AndroidEdge] em um emulador [Surface Duo][SurfaceDuo] de uma instância da área de trabalho do [Microsoft Edge][DesktopEdge]. Para obter informações sobre a depuração em um dispositivo Surface Duo, siga nosso guia para [dispositivos Android de depuração remota][RemoteDebuggingAndroid].

## Antes de começar

Instale o [SDK do Surface Duo][DuoSdk] antes de executar o [emulador Surface Duo][DuoEmulator]. Para obter mais informações, consulte [obter o SDK Surface Duo][DuoSdkdocs].

## Etapa 1: Navegue até edge://inspect

Abra uma instância da área de trabalho do [Microsoft Edge][DesktopEdge]e navegue até `edge://inspect` .

> ##### Figura 1  
> A `edge://inspect` página no Microsoft Edge na área ![ de trabalho a página Edge://inspect no Microsoft Edge na área de trabalho][ImageEdgeInspect]

> [!NOTE]
> Se a `edge://inspect` página não reconhecer o [emulador Surface Duo][DuoEmulator], reinicie o emulador.

## Etapa 2: iniciar o emulador Surface Duo

Inicie o [emulador Surface Duo][DuoEmulator]. Observe que o emulador exibe duas telas diferentes em execução no emulador.

> ##### Figura 2
> Emulador Surface Duo ![ o emulador Surface Duo][ImageDuoEmulator]  

## Etapa 3: carregar o conteúdo da Web no Microsoft Edge no emulador Surface Duo

Em qualquer uma das telas, passe o dedo sobre a bandeja de favoritos do [emulador Surface Duo][DuoEmulator] para exibir a gaveta de aplicativos. Escolha **borda** para iniciar o [aplicativo Microsoft Edge][AndroidEdge].

> ##### Figura 3
> O aplicativo Microsoft Edge no emulador Surface Duo ![ do aplicativo Microsoft Edge no emulador Surface Duo][ImageDuoEmulatorEdge]  

Navegue até o site ou o aplicativo que você deseja depurar no [aplicativo Microsoft Edge][AndroidEdge].

## Etapa 4: depurar o conteúdo da Web pelo emulador Surface Duo 

Volte para a instância da área de trabalho do [Microsoft Edge][DesktopEdge]. A `edge://inspect` página agora mostra o **SurfaceDuoEmulator** com uma lista das guias abertas ou [PWAs][PwaDocs] que estão em execução no [emulador Surface Duo][DuoEmulator].

> ##### Figura 4
> A `edge://inspect` página exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador ![ a página Edge://inspect exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador][ImageEdgeInspectTargets]  

> [!NOTE]
> Se você não vir **SurfaceDuoEmulator** na `edge://inspect` página, tente abrir ou fechar as guias no [aplicativo Microsoft Edge][AndroidEdge] no [emulador Surface Duo][DuoEmulator]. Para obter etapas adicionais de solução de problemas, consulte a [seção solução de problemas para dispositivos Android][TroubleshootingAndroid].

Na lista de guias abertas em execução no emulador, escolha **inspecionar** na guia em que o conteúdo da Web deve ser depurado. O [Microsoft Edge devtools][DevToolsDocs] será aberto em uma nova janela. Escolha **alternar screencast** ![ alternar screencast ][ImageToggleScreencastIcon] para ver o conteúdo da Web do seu [emulador Surface Duo][DuoEmulator] na janela do devtools. Agora você pode usar o Microsoft Edge DevTools para depurar o conteúdo da Web no [emulador Surface Duo][DuoEmulator].

> ##### Figura 5
> Usando o Microsoft Edge DevTools para depurar o Bing no aplicativo Microsoft Edge no emulador Surface Duo ![ usando o Microsoft Edge devtools para depurar o Bing no aplicativo Microsoft Edge no emulador Surface Duo][ImageDevTools]  

> [!NOTE]
> Se você ocupar o [aplicativo Microsoft Edge][AndroidEdge] entre as duas telas no emulador, o screencast refletirá o novo tamanho do aplicativo, mas não a dobradiça. Para entender como a dobradiça impacta o layout do seu conteúdo da Web, use o [emulador Surface Duo][DuoEmulator] em vez do screencast.

## Recursos adicionais

A Web é uma ótima plataforma para a nova classe de dobrável e dispositivos de tela dupla porque você pode escrever seu HTML, CSS e JavaScript uma vez e ter uma ótima aparência em dispositivos com tela única, tela dupla e dobrável. Para obter mais informações, consulte estes recursos adicionais para começar a criar conteúdo da Web para esses novos dispositivos.

- [Documentação para criar aplicativos em dispositivos de tela dupla][DualScreenDocs]
- [O explicativo da plataforma Web Microsoft Edge para novas APIs para criar experiências na Web no dobrável e em dispositivos de tela dupla][WebPlatformExplainer]
- [Gravação da sessão de dia do desenvolvedor do Microsoft 365: como criar experiências de tela dupla para sites e aplicativos Web][DeveloperDay]

<!-- image links -->  
[ImageEdgeInspect]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-inspect-page.msft.png "Figura 1: a página edge://inspect no Microsoft Edge na área de trabalho"
[ImageDuoEmulator]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-emulator.msft.png "Figura 2: emulador Surface Duo"
[ImageDuoEmulatorEdge]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-emulator-edge.msft.png "Figura 3: o aplicativo Microsoft Edge no emulador Surface Duo"
[ImageEdgeInspectTargets]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png "Figura 4: a página edge://inspect exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador"
[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png
[ImageDevTools]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-devtools.msft.png "Figura 5: usar o Microsoft Edge DevTools para depurar o Bing no aplicativo Microsoft Edge no emulador Surface Duo"

<!-- links -->  
[RemoteDebuggingAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Introdução à depuração remota de dispositivos Android"
[PwaDocs]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicativos Web progressivos no Windows"
[DevToolsDocs]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"
[TroubleshootingAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index#troubleshooting-devtools-is-not-detecting-the-android-device "Solução de problemas: o DevTools não está detectando o dispositivo Android"

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Aplicativo Android do Microsoft Edge"
[SurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Apresentando o Surface Duo"
[DesktopEdge]: https://www.microsoft.com/edge/ "Apresentando o novo Microsoft Edge"
[DuoEmulator]: https://docs.microsoft.com/dual-screen/android/use-emulator "Usar o emulador Surface DUo"
[DuoSdk]: https://www.microsoft.com/download/details.aspx?id=100847 "Lançamento do SDK Surface Duo Preview"
[DuoSdkDocs]: https://docs.microsoft.com/dual-screen/android/get-duo-sdk "Obter o SDK do Surface Duo"
[DualScreenDocs]: https://docs.microsoft.com/dual-screen/ "Criar aplicativos para dispositivos com tela dupla"
[WebPlatformExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitivas de plataforma Web para experiências otimizadas em dispositivos dobrável"
[DeveloperDay]: https://youtu.be/DXrZWsqXPVc "Como criar experiências de tela dupla para o site e os aplicativos Web"
