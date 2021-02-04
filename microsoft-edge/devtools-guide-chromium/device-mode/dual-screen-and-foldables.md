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
# <span data-ttu-id="bad76-104">Emular dispositivos de tela dupla e dobrável no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bad76-104">Emulate dual-screen and foldable devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="bad76-105">No Microsoft Edge versão 89 ou posterior, você pode emular os seguintes dispositivos de tela dupla e dobrável.</span><span class="sxs-lookup"><span data-stu-id="bad76-105">In Microsoft Edge version 89 or later, you may emulate the following dual-screen and foldable devices.</span></span>  

*   [<span data-ttu-id="bad76-106">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="bad76-106">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="bad76-107">Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="bad76-107">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  
    
<span data-ttu-id="bad76-108">Emular os dispositivos e alternar entre as seguintes posturas.</span><span class="sxs-lookup"><span data-stu-id="bad76-108">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="bad76-109">Postura de tela única ou dobrada</span><span class="sxs-lookup"><span data-stu-id="bad76-109">Single-screen or folded posture</span></span>  
*   <span data-ttu-id="bad76-110">Postura de tela dupla ou desdobrada</span><span class="sxs-lookup"><span data-stu-id="bad76-110">Dual-screen or unfolded posture</span></span>  
    
<span data-ttu-id="bad76-111">Ative [AS APIs](#turn-on-experimental-apis) experimentais da Plataforma Web e use o recurso de tela de mídia [CSS][DualScreenDocsCssMedia] e a [API getWindowSegments][DualScreenDocsJSAPI] do JavaScript para aprimorar seu site \(ou aplicativo\) para dispositivos de tela dupla e dobrável.</span><span class="sxs-lookup"><span data-stu-id="bad76-111">[Turn on experimental Web Platform APIs](#turn-on-experimental-apis) and use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI] to enhance your website \(or app\) for dual-screen and foldable devices.</span></span>  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Emular o Surface Duo no Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   <span data-ttu-id="bad76-113">Emular o Surface Duo no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bad76-113">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

## <span data-ttu-id="bad76-114">Ativar APIs experimentais</span><span class="sxs-lookup"><span data-stu-id="bad76-114">Turn on experimental APIs</span></span>  

<span data-ttu-id="bad76-115">Para usar o [recurso de abrangeção][DualScreenDocsCssMedia] de tela de mídia CSS e [JavaScript getWindowSegments API][DualScreenDocsJSAPI], ative o sinalizador no Microsoft `Experimental Web Platform features` Edge.</span><span class="sxs-lookup"><span data-stu-id="bad76-115">To use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI], turn on the `Experimental Web Platform features` flag in Microsoft Edge.</span></span>  <span data-ttu-id="bad76-116">Conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="bad76-116">Complete the following steps.</span></span>  

1.  <span data-ttu-id="bad76-117">Navegue até `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="bad76-117">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="bad76-118">In the **Search flags** textbox, enter `Experimental Web Platform features` , choose the Experimental Web Platform **features** flag, and change **Disabled** to **Enabled**.</span><span class="sxs-lookup"><span data-stu-id="bad76-118">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="bad76-119">Reinicie o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="bad76-119">Restart Microsoft Edge.</span></span>  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Ativar o sinalizador de recursos da Plataforma Web Experimental" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="bad76-121">Ativar o sinalizador de **recursos da Plataforma Web Experimental**</span><span class="sxs-lookup"><span data-stu-id="bad76-121">Turn on the **Experimental Web Platform features** flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="bad76-122">Se você estiver usando consultas de mídia [CSS][DualScreenDocsCssMedia] ou a API de Enumeração do Segmento do [Windows JavaScript][DualScreenDocsJSAPI] para aprimorar seu site ou aplicativo para [o Surface Duo,][SurfaceDevicesDuo]você também deve ativar o sinalizador de recursos da Plataforma **Web Experimental** no aplicativo Android [Microsoft Edge][GooglePlayMicrosoftEdge] em seu dispositivo [Surface Duo.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="bad76-122">If you are using [CSS media queries][DualScreenDocsCssMedia] or the [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also turn on the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>  
> 
> <span data-ttu-id="bad76-123">Se o sinalizador de recursos da Plataforma **Web Experimental** estiver ligado no [Microsoft Edge][MicrosoftEdge] para área de trabalho e estiver desligado no aplicativo Android [Microsoft Edge,][GooglePlayMicrosoftEdge]o comportamento do seu site ou aplicativo no emulador Surface Duo na área de trabalho do Microsoft Edge não corresponderá ao aplicativo [Android Microsoft Edge][GooglePlayMicrosoftEdge] no [Surface Duo.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="bad76-123">If the **Experimental Web Platform features** flag is turned on in [desktop Microsoft Edge][MicrosoftEdge] and turned off in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge does not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="bad76-124">Certifique-se de que os sinalizadores corresponderem ao Microsoft Edge do Android e da área de trabalho para usar com êxito o emulador Surface Duo na área [de trabalho do Microsoft Edge.][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="bad76-124">Ensure that the flags match across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

## <span data-ttu-id="bad76-125">Testar em dispositivos de tela dupla e dobrável</span><span class="sxs-lookup"><span data-stu-id="bad76-125">Test on foldable and dual-screen devices</span></span>  

<span data-ttu-id="bad76-126">Quando você emular o [Surface Duo][SurfaceDevicesDuo] em uma postura de tela dupla no Microsoft Edge, a seam \(o espaço entre as duas telas\) é desenhada sobre seu site ou aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bad76-126">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the seam \(the space between the two screens\) is drawn over your website or app.</span></span>  

<span data-ttu-id="bad76-127">A exibição emulada corresponde à maneira como seu site \(ou app\) renderiza no aplicativo Android do [Microsoft Edge][GooglePlayMicrosoftEdge] durante a execução no [Surface Duo.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="bad76-127">The emulated display matches the way your website \(or app\) renders in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] while running on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="bad76-128">Talvez seja preciso atualizar seu site \(ou aplicativo\) para ser exibido melhor ao longo da análise.</span><span class="sxs-lookup"><span data-stu-id="bad76-128">You may have to update your website \(or app\) to display better along the seam.</span></span>  <span data-ttu-id="bad76-129">Para obter mais informações sobre como adaptar seu site \(ou aplicativo\) à navegação, navegue até Como trabalhar [com aam][DualScreenIntroductionHowWorkSeam].</span><span class="sxs-lookup"><span data-stu-id="bad76-129">For more information about adapting your website \(or app\) to the seam, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam].</span></span>  

<span data-ttu-id="bad76-130">A [Barra de Ferramentas de][DevtoolsDeviceModeIndexSimulateMobileViewport] Dispositivo tem recursos adicionais para ajudá-lo a testar seu site ou aplicativo em várias posturas e orientações.</span><span class="sxs-lookup"><span data-stu-id="bad76-130">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="bad76-131">Choose **Rotate** \( ![ Rotate ](../media/rotate-dark-icon.msft.png) \) to rotate the viewport to landscape orientation.</span><span class="sxs-lookup"><span data-stu-id="bad76-131">Choose **Rotate** \(![Rotate](../media/rotate-dark-icon.msft.png)\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="bad76-132">Combine o recurso com **Span** \( Span \) para alternar entre tela única ou dobrada e posturas de tela dupla ou ![ ](../media/span-dark-icon.msft.png) desdobradas.</span><span class="sxs-lookup"><span data-stu-id="bad76-132">Combine the feature with **Span** \(![Span](../media/span-dark-icon.msft.png)\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="bad76-133">Juntos, os recursos permitem que você teste seu site ou aplicativo em todas as quatro posturas e orientações possíveis.</span><span class="sxs-lookup"><span data-stu-id="bad76-133">Together, the features allow you to test your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matriz de posturas e orientações para dispositivos de tela dupla e dobrável" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="bad76-135">Matriz de posturas e orientações para dispositivos de tela dupla e dobrável</span><span class="sxs-lookup"><span data-stu-id="bad76-135">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="bad76-136">O **ícone da Plataforma Web Experimental** \( ![ ExperimentalApis \) exibe o estado do sinalizador de recursos da Plataforma ](../media/experimental-apis-dark-icon.msft.png) Web **Experimental.**</span><span class="sxs-lookup"><span data-stu-id="bad76-136">The **Experimental Web Platform features** \(![ExperimentalApis](../media/experimental-apis-dark-icon.msft.png)\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="bad76-137">Se o sinalizador estiver ligado, o ícone será realçado.</span><span class="sxs-lookup"><span data-stu-id="bad76-137">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="bad76-138">Se o sinalizador estiver desligado, o ícone não será realçado.</span><span class="sxs-lookup"><span data-stu-id="bad76-138">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="bad76-139">Para ativar \(ou desativar\) o sinalizador, escolha o ícone ou navegue até e `edge://flags` alterne o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="bad76-139">To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.</span></span>  

> [!NOTE]
> <span data-ttu-id="bad76-140">A seguir está uma lista de problemas conhecidos atuais.</span><span class="sxs-lookup"><span data-stu-id="bad76-140">The following is a list of current known issues.</span></span>  
> 
> *   <span data-ttu-id="bad76-141">Quando você usa um cliente de Área de Trabalho Remota da [Microsoft][RemoteDesktopClientDocs] para se conectar a um computador remoto e emular o [Surface Duo][SurfaceDevicesDuo] ou [Samsung Duoy Fold,][SamsungMobileGalaxyFold]o ponteiro pode treme ou treme.</span><span class="sxs-lookup"><span data-stu-id="bad76-141">When you use a [Microsoft Remote Desktop client][RemoteDesktopClientDocs] to connect to a remote PC and emulate the [Surface Duo][SurfaceDevicesDuo] or [Samsung Galaxy Fold][SamsungMobileGalaxyFold], the pointer may shake or stutter.</span></span>  <span data-ttu-id="bad76-142">Se você tiver o problema, [envie comentários.](#getting-in-touch-with-the-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="bad76-142">If you run into the issue, [send feedback](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

## <span data-ttu-id="bad76-143">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="bad76-143">Additional Resources</span></span>  

<span data-ttu-id="bad76-144">Aqui estão recursos adicionais que podem ajudá-lo a aprimorar seu site \(ou aplicativo\) para dispositivos de tela dupla.</span><span class="sxs-lookup"><span data-stu-id="bad76-144">Here are additional resources that may help you enhance your website \(or app\) for dual-screen devices.</span></span>  

*   <span data-ttu-id="bad76-145">Para obter mais informações sobre o desenvolvimento da Web em dispositivos de tela dupla, navegue até [experiências da Web de tela dupla.][DualScreenWebIndex]</span><span class="sxs-lookup"><span data-stu-id="bad76-145">For more information about web development on dual-screen devices, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="bad76-146">Instale o [emulador Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="bad76-146">Install the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="bad76-147">O emulador Surface Duo é diferente do emulador no Microsoft Edge, executa o Android e se integra ao [Android Studio.][AndroidDeveloperStudio]</span><span class="sxs-lookup"><span data-stu-id="bad76-147">The Surface Duo emulator is different from the emulator in Microsoft Edge, runs Android, and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="bad76-148">Para obter mais informações, [navegue até Obter o SDK do Surface Duo.][DualScreenAndroidGetDuoSdk]</span><span class="sxs-lookup"><span data-stu-id="bad76-148">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <span data-ttu-id="bad76-149">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bad76-149">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
