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
# <a name="get-started-with-remote-debugging-surface-duo-emulators"></a><span data-ttu-id="e3fbb-104">Começar a depurar remotamente os emuladores do Surface Duo</span><span class="sxs-lookup"><span data-stu-id="e3fbb-104">Get started with remote debugging Surface Duo emulators</span></span>  

<span data-ttu-id="e3fbb-105">Neste artigo, você passa pelo processo de depuração remota do conteúdo da Web no [aplicativo Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] em um emulador do Surface [Duo][MicrosoftSurfaceDevicesSurfaceDuo] de uma instância da área de trabalho do [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="e3fbb-105">In this article, you walk through the process of remotely debugging your web content in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on a [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] emulator from a desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="e3fbb-106">Para obter informações sobre a depuração em um dispositivo Surface Duo, siga nosso guia para [depuração][DevtoolsRemoteDebuggingMain]remota de dispositivos Android .</span><span class="sxs-lookup"><span data-stu-id="e3fbb-106">For information on debugging on a Surface Duo device, follow our guide for [remote debugging Android devices][DevtoolsRemoteDebuggingMain].</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="e3fbb-107">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="e3fbb-107">Before you begin</span></span>

<span data-ttu-id="e3fbb-108">Instale o [SDK do Surface Duo][MicrosoftDownload100847] antes de executar o [emulador do Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="e3fbb-108">Install the [Surface Duo SDK][MicrosoftDownload100847] before running the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="e3fbb-109">Para obter mais informações, navegue [até Obter o SDK do Surface Duo][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="e3fbb-109">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <a name="step-1-navigate-to-edgeinspect"></a><span data-ttu-id="e3fbb-110">Etapa 1: Navegue até edge://inspect</span><span class="sxs-lookup"><span data-stu-id="e3fbb-110">Step 1: Navigate to edge://inspect</span></span>  

<span data-ttu-id="e3fbb-111">Abra uma instância da área de trabalho [do Microsoft Edge][MicrosoftEdge]e navegue até `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="e3fbb-111">Open a desktop instance of [Microsoft Edge][MicrosoftEdge], and navigate to `edge://inspect`.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="A edge://inspect no Microsoft Edge na área de trabalho" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   <span data-ttu-id="e3fbb-113">A `edge://inspect` página no Microsoft Edge na área de trabalho</span><span class="sxs-lookup"><span data-stu-id="e3fbb-113">The `edge://inspect` page in Microsoft Edge on the desktop</span></span>  
:::image-end:::

> [!NOTE]
> <span data-ttu-id="e3fbb-114">Se a `edge://inspect` página não reconhecer o [emulador do Surface Duo,][DualScreenAndroidUseEmulator]reinicie o emulador.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-114">If the `edge://inspect` page does not recognize the [Surface Duo emulator][DualScreenAndroidUseEmulator], restart the emulator.</span></span>  

## <a name="step-2-launch-the-surface-duo-emulator"></a><span data-ttu-id="e3fbb-115">Etapa 2: Iniciar o emulador do Surface Duo</span><span class="sxs-lookup"><span data-stu-id="e3fbb-115">Step 2: Launch the Surface Duo emulator</span></span>  

<span data-ttu-id="e3fbb-116">Iniciar o [emulador do Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="e3fbb-116">Launch the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="e3fbb-117">Observe que o emulador exibe duas telas diferentes em execução no emulador.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-117">Notice that the emulator displays 2 different screens running on the emulator.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="O emulador do Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   <span data-ttu-id="e3fbb-119">O emulador do Surface Duo</span><span class="sxs-lookup"><span data-stu-id="e3fbb-119">The Surface Duo emulator</span></span>  
:::image-end:::  

## <a name="step-3-load-your-web-content-in-microsoft-edge-on-the-surface-duo-emulator"></a><span data-ttu-id="e3fbb-120">Etapa 3: carregar o conteúdo da Web no Microsoft Edge no emulador do Surface Duo</span><span class="sxs-lookup"><span data-stu-id="e3fbb-120">Step 3: Load your web content in Microsoft Edge on the Surface Duo emulator</span></span>  

<span data-ttu-id="e3fbb-121">Em uma das telas, passe o dedo para cima na Bandeja de Favoritos do [emulador do Surface Duo][DualScreenAndroidUseEmulator] para exibir a Gaveta de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-121">On either screen, swipe up on the Favorites Tray of the [Surface Duo emulator][DualScreenAndroidUseEmulator] to display the Apps Drawer.</span></span>  <span data-ttu-id="e3fbb-122">Escolha **Borda para** iniciar o aplicativo Microsoft [Edge][GooglePlayStoreAppsComMicrosoftEmmx].</span><span class="sxs-lookup"><span data-stu-id="e3fbb-122">Choose **Edge** to launch the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="O aplicativo Microsoft Edge no emulador do Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   <span data-ttu-id="e3fbb-124">O aplicativo Microsoft Edge no emulador do Surface Duo</span><span class="sxs-lookup"><span data-stu-id="e3fbb-124">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="e3fbb-125">Navegue até o site ou aplicativo que você deseja depurar no [aplicativo do Microsoft Edge.][GooglePlayStoreAppsComMicrosoftEmmx]</span><span class="sxs-lookup"><span data-stu-id="e3fbb-125">Navigate to the website or app that you want to debug in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

## <a name="step-4-debug-your-web-content-from-the-surface-duo-emulator"></a><span data-ttu-id="e3fbb-126">Etapa 4: Depurar o conteúdo da Web do emulador do Surface Duo</span><span class="sxs-lookup"><span data-stu-id="e3fbb-126">Step 4: Debug your web content from the Surface Duo emulator</span></span>  

<span data-ttu-id="e3fbb-127">Alternar de volta para a instância da área de trabalho [do Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="e3fbb-127">Switch back to the desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="e3fbb-128">A `edge://inspect` página agora mostra o **SurfaceDuoEmulator** com uma lista das guias abertas ou [PWAs][ProgressiveWebAppsIndex] que estão sendo executados no [emulador surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="e3fbb-128">The `edge://inspect` page now shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][ProgressiveWebAppsIndex] that are running on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="A edge://inspect exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador" lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   <span data-ttu-id="e3fbb-130">A `edge://inspect` página exibe uma lista das guias abertas no aplicativo Microsoft Edge em execução no emulador</span><span class="sxs-lookup"><span data-stu-id="e3fbb-130">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="e3fbb-131">Se **SurfaceDuoEmulator** não for exibido na página, tente abrir ou fechar guias no aplicativo Microsoft Edge no `edge://inspect` [Emulador surface Duo][DualScreenAndroidUseEmulator]. [][GooglePlayStoreAppsComMicrosoftEmmx]</span><span class="sxs-lookup"><span data-stu-id="e3fbb-131">If **SurfaceDuoEmulator** is not displayed on the `edge://inspect` page, try opening or closing tabs in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on the [Surface Duo Emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="e3fbb-132">Para obter etapas adicionais de solução de problemas, navegue até a seção [solução de problemas para dispositivos Android.][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]</span><span class="sxs-lookup"><span data-stu-id="e3fbb-132">For additional troubleshooting steps, navigate to [troubleshooting section for Android devices][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].</span></span>  

<span data-ttu-id="e3fbb-133">Na lista de guias abertas em execução  no emulador, escolha inspecionar na guia que tem o conteúdo da Web a ser depurado.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-133">From the list of open tabs running on the emulator, choose **inspect** on the tab that has the web content to be debugged.</span></span>  <span data-ttu-id="e3fbb-134">O [Microsoft Edge DevTools][DevtoolsIndex] será aberto em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-134">The [Microsoft Edge DevTools][DevtoolsIndex] will open in a new window.</span></span>  <span data-ttu-id="e3fbb-135">Escolha **Toggle Screencast** \( Toggle Screencast \) para exibir o conteúdo da Web a partir do ![ ](../media/toggle-screencast-icon.msft.png) [emulador do Surface Duo][DualScreenAndroidUseEmulator] na janela DevTools.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-135">Choose **Toggle Screencast** \(![Toggle Screencast](../media/toggle-screencast-icon.msft.png)\) to view the web content from your [Surface Duo emulator][DualScreenAndroidUseEmulator] in the DevTools window.</span></span>  <span data-ttu-id="e3fbb-136">Agora você pode usar o Microsoft Edge DevTools para depurar o conteúdo da Web no [emulador do Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="e3fbb-136">You are now able to use the Microsoft Edge DevTools to debug your web content on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Usando o Microsoft Edge DevTools para depurar o Bing no aplicativo do Microsoft Edge no emulador do Surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   <span data-ttu-id="e3fbb-138">Usando o Microsoft Edge DevTools para depurar o Bing no aplicativo do Microsoft Edge no emulador do Surface Duo</span><span class="sxs-lookup"><span data-stu-id="e3fbb-138">Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="e3fbb-139">Se você abranger o [aplicativo Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] em ambas as telas no emulador, o screencast refletirá o novo tamanho do aplicativo, mas não a dobradiça.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-139">If you span the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] across both screens in the emulator, the screencast will reflect the new size of the app but not the hinge.</span></span>  <span data-ttu-id="e3fbb-140">Para entender como a dobradiça afeta o layout do conteúdo da Web, use o [emulador do Surface Duo][DualScreenAndroidUseEmulator] em vez do screencast.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-140">To understand how the hinge impacts the layout of your web content, use the [Surface Duo emulator][DualScreenAndroidUseEmulator] instead of the screencast.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="e3fbb-141">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="e3fbb-141">Additional Resources</span></span>  

<span data-ttu-id="e3fbb-142">A Web é uma ótima plataforma para a nova classe de dispositivos de tela dupla e dobrável porque você pode gravar seu HTML, CSS e JavaScript uma vez e ter uma ótima aparência em dispositivos de tela única, de tela dupla e dobrável.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-142">The web is a great platform for the new class of foldable and dual-screen devices because you may write your HTML, CSS, and JavaScript once and have it look great across single-screen, dual-screen, and foldable devices.</span></span>  <span data-ttu-id="e3fbb-143">Para obter mais informações, navegue até os seguintes recursos adicionais para começar a criar conteúdo da Web para esses novos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e3fbb-143">For more information, navigate to the following additional resources to get started building web content for these new devices.</span></span>  

*   [<span data-ttu-id="e3fbb-144">Documentação para criar aplicativos em dispositivos de tela dupla</span><span class="sxs-lookup"><span data-stu-id="e3fbb-144">Documentation for creating apps on dual-screen devices</span></span>][DualScreenIndex]  
*   [<span data-ttu-id="e3fbb-145">O explicador da plataforma Web do Microsoft Edge para novas APIs para criar experiências da Web em dispositivos dobráveis e de tela dupla</span><span class="sxs-lookup"><span data-stu-id="e3fbb-145">The Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices</span></span>][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [<span data-ttu-id="e3fbb-146">Gravação da sessão do Dia do Desenvolvedor do Microsoft 365: como criar experiências de tela dupla para sites e aplicativos Web</span><span class="sxs-lookup"><span data-stu-id="e3fbb-146">Recording of Microsoft 365 Developer Day session: How to build dual-screen experiences for websites and web apps</span></span>][YoutubeDxrzwsqxpvc]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="e3fbb-147">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e3fbb-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[ProgressiveWebAppsIndex]: ../../progressive-web-apps-chromium/index.md "Aplicativos Web Progressivos no Windows | Microsoft Docs"  
[DevtoolsRemoteDebuggingMain]: ./index.md "Começar com a depuração remota de dispositivos Android | Microsoft Docs"  
[DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]: ./index.md#troubleshooting-devtools-is-not-detecting-the-android-device "Solução de problemas: o DevTools não está detectando o dispositivo Android - Começar com a depuração remota de dispositivos Android | Microsoft Docs"  

[DualScreenIndex]: /dual-screen/index "Criar aplicativos para dispositivos de tela | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Use o emulador Surface DUo | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obter o SDK do Surface Duo | Microsoft Docs"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Apresentando o novo Microsoft Edge"  
[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "O novo Surface Duo | Microsoft Surface"  
[MicrosoftDownload100847]: https://www.microsoft.com/download/details.aspx?id=100847 "Baixar o Surface Duo SDK Preview Release | Centro de Download da Microsoft"  

[GooglePlayStoreAppsComMicrosoftEmmx]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge: navegador da Web | GooglePlay"  

[GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitivas da plataforma Web para experiências iluminadas em dispositivos dobráveis - MicrosoftEdge/MSEdgeExplainers | GitHub"  

[YoutubeDxrzwsqxpvc]: https://youtu.be/DXrZWsqXPVc "Como criar experiências de tela dupla para o site e aplicativos web | YouTube"  
