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
# <span data-ttu-id="2b2c3-104">Introdução aos emuladores Remote Debugging Surface Duo</span><span class="sxs-lookup"><span data-stu-id="2b2c3-104">Get Started with Remote Debugging Surface Duo emulators</span></span>  

<span data-ttu-id="2b2c3-105">Neste artigo, você percorre o processo de depuração remota do conteúdo da Web no [aplicativo Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] em um emulador [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] de uma instância da área de trabalho do [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="2b2c3-105">In this article, you walk through the process of remotely debugging your web content in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on a [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] emulator from a desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="2b2c3-106">Para obter informações sobre a depuração em um dispositivo Surface Duo, siga nosso guia para [dispositivos Android de depuração remota][DevtoolsRemoteDebuggingMain].</span><span class="sxs-lookup"><span data-stu-id="2b2c3-106">For information on debugging on a Surface Duo device, follow our guide for [remote debugging Android devices][DevtoolsRemoteDebuggingMain].</span></span>  

## <span data-ttu-id="2b2c3-107">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="2b2c3-107">Before you Begin</span></span>

<span data-ttu-id="2b2c3-108">Instale o [SDK do Surface Duo][MicrosoftDownload100847] antes de executar o [emulador Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="2b2c3-108">Install the [Surface Duo SDK][MicrosoftDownload100847] before running the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="2b2c3-109">Para obter mais informações, consulte [obter o SDK Surface Duo][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="2b2c3-109">For more information, see [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <span data-ttu-id="2b2c3-110">Etapa 1: Navegue até edge://inspect</span><span class="sxs-lookup"><span data-stu-id="2b2c3-110">Step 1: Navigate to edge://inspect</span></span>  

<span data-ttu-id="2b2c3-111">Abra uma instância da área de trabalho do [Microsoft Edge][MicrosoftEdge]e navegue até `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="2b2c3-111">Open a desktop instance of [Microsoft Edge][MicrosoftEdge], and navigate to `edge://inspect`.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="A página edge://inspect no Microsoft Edge na área de trabalho" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   <span data-ttu-id="2b2c3-113">A `edge://inspect` página no Microsoft Edge na área de trabalho</span><span class="sxs-lookup"><span data-stu-id="2b2c3-113">The `edge://inspect` page in Microsoft Edge on the desktop</span></span>  
:::image-end:::

> [!NOTE]
> <span data-ttu-id="2b2c3-114">Se a `edge://inspect` página não reconhecer o [emulador Surface Duo][DualScreenAndroidUseEmulator], reinicie o emulador.</span><span class="sxs-lookup"><span data-stu-id="2b2c3-114">If the `edge://inspect` page does not recognize the [Surface Duo emulator][DualScreenAndroidUseEmulator], restart the emulator.</span></span>  

## <span data-ttu-id="2b2c3-115">Etapa 2: iniciar o emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="2b2c3-115">Step 2: Launch the Surface Duo emulator</span></span>  

<span data-ttu-id="2b2c3-116">Inicie o [emulador Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="2b2c3-116">Launch the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="2b2c3-117">Observe que o emulador exibe duas telas diferentes em execução no emulador.</span><span class="sxs-lookup"><span data-stu-id="2b2c3-117">Notice that the emulator displays 2 different screens running on the emulator.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="O emulador Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   <span data-ttu-id="2b2c3-119">O emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="2b2c3-119">The Surface Duo emulator</span></span>  
:::image-end:::  

## <span data-ttu-id="2b2c3-120">Etapa 3: carregar o conteúdo da Web no Microsoft Edge no emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="2b2c3-120">Step 3: Load your web content in Microsoft Edge on the Surface Duo emulator</span></span>  

<span data-ttu-id="2b2c3-121">Em qualquer uma das telas, passe o dedo sobre a bandeja de favoritos do [emulador Surface Duo][DualScreenAndroidUseEmulator] para exibir a gaveta de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2b2c3-121">On either screen, swipe up on the Favorites Tray of the [Surface Duo emulator][DualScreenAndroidUseEmulator] to display the Apps Drawer.</span></span>  <span data-ttu-id="2b2c3-122">Escolha **borda** para iniciar o [aplicativo Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx].</span><span class="sxs-lookup"><span data-stu-id="2b2c3-122">Choose **Edge** to launch the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="O aplicativo Microsoft Edge no emulador Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   <span data-ttu-id="2b2c3-124">O aplicativo Microsoft Edge no emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="2b2c3-124">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="2b2c3-125">Navegue até o site ou o aplicativo que você deseja depurar no [aplicativo Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx].</span><span class="sxs-lookup"><span data-stu-id="2b2c3-125">Navigate to the website or app that you want to debug in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

## <span data-ttu-id="2b2c3-126">Etapa 4: depurar o conteúdo da Web pelo emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="2b2c3-126">Step 4: Debug your web content from the Surface Duo emulator</span></span>  

<span data-ttu-id="2b2c3-127">Volte para a instância da área de trabalho do [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="2b2c3-127">Switch back to the desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="2b2c3-128">A `edge://inspect` página agora mostra o **SurfaceDuoEmulator** com uma lista das guias abertas ou [PWAs][ProgressiveWebAppsIndex] que estão em execução no [emulador Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="2b2c3-128">The `edge://inspect` page now shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][ProgressiveWebAppsIndex] that are running on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="A página edge://inspect exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador" lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   <span data-ttu-id="2b2c3-130">A `edge://inspect` página exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador</span><span class="sxs-lookup"><span data-stu-id="2b2c3-130">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="2b2c3-131">Se você não vir **SurfaceDuoEmulator** na `edge://inspect` página, tente abrir ou fechar as guias no [aplicativo Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] no [emulador Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="2b2c3-131">If you do not see **SurfaceDuoEmulator** on the `edge://inspect` page, try opening or closing tabs in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on the [Surface Duo Emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="2b2c3-132">Para obter etapas adicionais de solução de problemas, consulte a [seção solução de problemas para dispositivos Android][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].</span><span class="sxs-lookup"><span data-stu-id="2b2c3-132">For additional troubleshooting steps, see the [troubleshooting section for Android devices][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].</span></span>  

<span data-ttu-id="2b2c3-133">Na lista de guias abertas em execução no emulador, escolha **inspecionar** na guia em que o conteúdo da Web deve ser depurado.</span><span class="sxs-lookup"><span data-stu-id="2b2c3-133">From the list of open tabs running on the emulator, choose **inspect** on the tab that has the web content to be debugged.</span></span>  <span data-ttu-id="2b2c3-134">O [Microsoft Edge devtools][DevtoolsIndex] será aberto em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="2b2c3-134">The [Microsoft Edge DevTools][DevtoolsIndex] will open in a new window.</span></span>  <span data-ttu-id="2b2c3-135">Escolha **alternar screencast** \ ( ![ alternar screencast ][ImageToggleScreencastIcon] \) para exibir o conteúdo da Web do seu [emulador Surface Duo][DualScreenAndroidUseEmulator] na janela do devtools.</span><span class="sxs-lookup"><span data-stu-id="2b2c3-135">Choose **Toggle Screencast** \(![Toggle Screencast][ImageToggleScreencastIcon]\) to view the web content from your [Surface Duo emulator][DualScreenAndroidUseEmulator] in the DevTools window.</span></span>  <span data-ttu-id="2b2c3-136">Agora você pode usar o Microsoft Edge DevTools para depurar o conteúdo da Web no [emulador Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="2b2c3-136">You are now able to use the Microsoft Edge DevTools to debug your web content on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Usar o Microsoft Edge DevTools para depurar o Bing no aplicativo Microsoft Edge no emulador Surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   <span data-ttu-id="2b2c3-138">Usar o Microsoft Edge DevTools para depurar o Bing no aplicativo Microsoft Edge no emulador Surface Duo</span><span class="sxs-lookup"><span data-stu-id="2b2c3-138">Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="2b2c3-139">Se você ocupar o [aplicativo Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] entre as duas telas no emulador, o screencast refletirá o novo tamanho do aplicativo, mas não a dobradiça.</span><span class="sxs-lookup"><span data-stu-id="2b2c3-139">If you span the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] across both screens in the emulator, the screencast will reflect the new size of the app but not the hinge.</span></span>  <span data-ttu-id="2b2c3-140">Para entender como a dobradiça impacta o layout do seu conteúdo da Web, use o [emulador Surface Duo][DualScreenAndroidUseEmulator] em vez do screencast.</span><span class="sxs-lookup"><span data-stu-id="2b2c3-140">To understand how the hinge impacts the layout of your web content, use the [Surface Duo emulator][DualScreenAndroidUseEmulator] instead of the screencast.</span></span>  

## <span data-ttu-id="2b2c3-141">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="2b2c3-141">Additional Resources</span></span>  

<span data-ttu-id="2b2c3-142">A Web é uma ótima plataforma para a nova classe de dobrável e dispositivos de tela dupla porque você pode escrever seu HTML, CSS e JavaScript uma vez e ter uma ótima aparência em dispositivos com tela única, tela dupla e dobrável.</span><span class="sxs-lookup"><span data-stu-id="2b2c3-142">The web is a great platform for the new class of foldable and dual-screen devices because you can write your HTML, CSS, and JavaScript once and have it look great across single-screen, dual-screen, and foldable devices.</span></span>  <span data-ttu-id="2b2c3-143">Para obter mais informações, consulte estes recursos adicionais para começar a criar conteúdo da Web para esses novos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2b2c3-143">For more information, see these additional resources to get started building web content for these new devices.</span></span>  

*   [<span data-ttu-id="2b2c3-144">Documentação para criar aplicativos em dispositivos de tela dupla</span><span class="sxs-lookup"><span data-stu-id="2b2c3-144">Documentation for creating apps on dual-screen devices</span></span>][DualScreenIndex]  
*   [<span data-ttu-id="2b2c3-145">O explicativo da plataforma Web Microsoft Edge para novas APIs para criar experiências na Web no dobrável e em dispositivos de tela dupla</span><span class="sxs-lookup"><span data-stu-id="2b2c3-145">The Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices</span></span>][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [<span data-ttu-id="2b2c3-146">Gravação da sessão de dia do desenvolvedor do Microsoft 365: como criar experiências de tela dupla para sites e aplicativos Web</span><span class="sxs-lookup"><span data-stu-id="2b2c3-146">Recording of Microsoft 365 Developer Day session: How to build dual-screen experiences for websites and web apps</span></span>][YoutubeDxrzwsqxpvc]  

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
