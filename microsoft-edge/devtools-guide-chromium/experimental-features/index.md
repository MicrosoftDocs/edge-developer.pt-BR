---
description: Os recursos experimentais mais recentes do Microsoft Edge DevTools
title: Recursos experimentais
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools, experimento
ms.openlocfilehash: fbdeeb08599285a9cfa6edd467282cfbabbadd74
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231601"
---
# <span data-ttu-id="9d925-104">Recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="9d925-104">Experimental features</span></span>  

<span data-ttu-id="9d925-105">O Microsoft Edge DevTools fornece acesso a recursos experimentais que ainda estão em desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="9d925-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="9d925-106">Você pode testar e [fornecer comentários](#providing-feedback-on-experimental-features) antes que cada recurso seja lançado.</span><span class="sxs-lookup"><span data-stu-id="9d925-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="9d925-107">Embora os recursos experimentais estejam disponíveis em todos os canais do Microsoft Edge, você pode obter os recursos experimentais mais recentes usando o Microsoft Edge Canárias Channel.</span><span class="sxs-lookup"><span data-stu-id="9d925-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="9d925-108">Ativar os recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="9d925-108">Turn on experimental features</span></span>  

<span data-ttu-id="9d925-109">Para ativar \ (ou desligar \) recursos experimentais no Microsoft Edge, siga as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d925-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="9d925-110">[Abra o devtools][DevtoolsOpenMain].</span><span class="sxs-lookup"><span data-stu-id="9d925-110">[Open DevTools][DevtoolsOpenMain].</span></span>  
    *   <span data-ttu-id="9d925-111">Selecione `Control` + `Shift` + `I` \ (Windows, Linux \) ou `Command` + `Option` + `I` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="9d925-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="9d925-112">Para obter mais informações, navegue até [atalhos de teclado do Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="9d925-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="9d925-113">Abra o painel [configurações][DevToolsCustomizeSettings] .</span><span class="sxs-lookup"><span data-stu-id="9d925-113">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="9d925-114">Selecione `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="9d925-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="9d925-115">Para obter mais informações, navegue até [atalhos de teclado do Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="9d925-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="9d925-116">No lado esquerdo do painel **configurações** , escolha a seção **experimentos** .</span><span class="sxs-lookup"><span data-stu-id="9d925-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="9d925-118">Lista de experimentos nas **configurações** do devtools</span><span class="sxs-lookup"><span data-stu-id="9d925-118">List of experiments in DevTools **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9d925-119">Na página **experimentos** , percorra a lista de todos os recursos experimentais disponíveis e escolha a caixa de seleção ao lado de cada recurso que você deseja testar.</span><span class="sxs-lookup"><span data-stu-id="9d925-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="9d925-120">Feche e abra novamente o Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="9d925-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="9d925-121">Os recursos experimentais são atualizados constantemente e podem causar problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="9d925-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="9d925-122">Para desativar um recurso experimental, abra a página **experimentos** e desmarque a caixa de seleção do recurso experimental que você deseja desativar.</span><span class="sxs-lookup"><span data-stu-id="9d925-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="9d925-123">Recursos experimentais realçados</span><span class="sxs-lookup"><span data-stu-id="9d925-123">Highlighted experimental features</span></span>  

<span data-ttu-id="9d925-124">As seções a seguir descrevem os novos recursos experimentais que estão disponíveis no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9d925-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="9d925-125">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="9d925-125">Experimental feature</span></span> | <span data-ttu-id="9d925-126">Microsoft Edge versão</span><span class="sxs-lookup"><span data-stu-id="9d925-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="9d925-127">Emulação: suporta o modo de tela dupla</span><span class="sxs-lookup"><span data-stu-id="9d925-127">Emulation: Support dual screen mode</span></span>](#emulation-support-dual-screen-mode) | <span data-ttu-id="9d925-128">84 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9d925-128">84 or later</span></span> |  
| [<span data-ttu-id="9d925-129">Habilitar novos recursos de depuração de grade CSS</span><span class="sxs-lookup"><span data-stu-id="9d925-129">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="9d925-130">85 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9d925-130">85 or later</span></span> |  
| [<span data-ttu-id="9d925-131">Habilitar o suporte para mover as guias entre painéis</span><span class="sxs-lookup"><span data-stu-id="9d925-131">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="9d925-132">85 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9d925-132">85 or later</span></span> |  
| [<span data-ttu-id="9d925-133">Habilitar webhint</span><span class="sxs-lookup"><span data-stu-id="9d925-133">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="9d925-134">85 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9d925-134">85 or later</span></span> |  
| [<span data-ttu-id="9d925-135">Habilitar console de rede</span><span class="sxs-lookup"><span data-stu-id="9d925-135">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="9d925-136">85 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9d925-136">85 or later</span></span> |  
| [<span data-ttu-id="9d925-137">Visualizador de ordem de origem</span><span class="sxs-lookup"><span data-stu-id="9d925-137">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="9d925-138">86 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9d925-138">86 or later</span></span> |  
| [<span data-ttu-id="9d925-139">Habilitar o editor de atalhos de teclado</span><span class="sxs-lookup"><span data-stu-id="9d925-139">Enable keyboard shortcut editor</span></span>](#enable-keyboard-shortcut-editor) | <span data-ttu-id="9d925-140">87 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9d925-140">87 or later</span></span> |  
| [<span data-ttu-id="9d925-141">Ativar camadas compostas no modo de exibição 3D</span><span class="sxs-lookup"><span data-stu-id="9d925-141">Turn on Composited Layers in 3D View</span></span>](#turn-on-composited-layers-in-3d-view) | <span data-ttu-id="9d925-142">87 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9d925-142">87 or later</span></span> |  

### <span data-ttu-id="9d925-143">Emulação: suporta o modo de tela dupla</span><span class="sxs-lookup"><span data-stu-id="9d925-143">Emulation: Support dual screen mode</span></span>  

<span data-ttu-id="9d925-144">Fornece recursos adicionais para emular dois novos dispositivos de tela dupla e de dobrável no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9d925-144">Provides additional features for emulating two new dual-screen and foldable devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="9d925-145">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="9d925-145">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="9d925-146">Dobra Samsung Galaxy</span><span class="sxs-lookup"><span data-stu-id="9d925-146">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  
    
<span data-ttu-id="9d925-147">EMule os dispositivos e alterne entre as seguintes condições.</span><span class="sxs-lookup"><span data-stu-id="9d925-147">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="9d925-148">Postura de tela única ou dobrada</span><span class="sxs-lookup"><span data-stu-id="9d925-148">Single-screen or folded posture</span></span>  
*   <span data-ttu-id="9d925-149">Postura de tela dupla ou não dobrada</span><span class="sxs-lookup"><span data-stu-id="9d925-149">Dual-screen or unfolded posture</span></span>  
    
<span data-ttu-id="9d925-150">[Habilite APIs experimentais da Web Platform](#enable-experimental-apis) e use o [recurso de distribuição de tela de mídia CSS][DualScreenDocsCssMedia] e a [API JavaScript getWindowSegments][DualScreenDocsJSAPI] para aprimorar seu site \ (ou app \) para dispositivos de tela dupla e dobrável.</span><span class="sxs-lookup"><span data-stu-id="9d925-150">[Enable experimental Web Platform APIs](#enable-experimental-apis) and use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI] to enhance your website \(or app\) for dual-screen and foldable devices.</span></span>  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Emular superfície Duo no Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   <span data-ttu-id="9d925-152">Emular superfície Duo no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9d925-152">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

#### <span data-ttu-id="9d925-153">Habilitar APIs experimentais</span><span class="sxs-lookup"><span data-stu-id="9d925-153">Enable experimental APIs</span></span>  

<span data-ttu-id="9d925-154">Para usar o [recurso de distribuição de tela de mídia CSS][DualScreenDocsCssMedia] e a [API de getWindowSegments JavaScript][DualScreenDocsJSAPI], ative o `Experimental Web Platform features` sinalizador no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9d925-154">To use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI], turn on the `Experimental Web Platform features` flag in Microsoft Edge.</span></span>  <span data-ttu-id="9d925-155">Conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d925-155">Complete the following steps.</span></span>  

1.  <span data-ttu-id="9d925-156">Navegue até `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="9d925-156">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="9d925-157">Na caixa de texto de **sinalizadores de pesquisa** , digite `Experimental Web Platform features` , escolha o sinalizador de **recursos da plataforma da Web experimental** e alterar **desabilitado** como **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="9d925-157">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="9d925-158">Reinicie o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9d925-158">Restart Microsoft Edge.</span></span>  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Habilitar o sinalizador de recursos da plataforma da Web experimental" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="9d925-160">Habilitar o sinalizador de recursos da plataforma da Web experimental</span><span class="sxs-lookup"><span data-stu-id="9d925-160">Enable the Experimental Web Platform features flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="9d925-161">Se você estiver usando [consultas de mídia CSS][DualScreenDocsCssMedia] ou a [API de enumeração de segmento do Windows JavaScript][DualScreenDocsJSAPI] para aprimorar seu site ou aplicativo para o [Surface Duo][SurfaceDevicesDuo], também deverá habilitar o sinalizador de **recursos da plataforma da Web experimental** no [aplicativo Android do Microsoft Edge][GooglePlayMicrosoftEdge] em seu dispositivo [Surface Duo][SurfaceDevicesDuo] .</span><span class="sxs-lookup"><span data-stu-id="9d925-161">If you are using [CSS media queries][DualScreenDocsCssMedia] or the [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also enable the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>  
> 
> <span data-ttu-id="9d925-162">Se o sinalizador de **recursos da plataforma da Web experimental** estiver habilitado no [Microsoft Edge da área de trabalho][MicrosoftEdge] e desabilitado no [aplicativo Android do Microsoft Edge][GooglePlayMicrosoftEdge], o comportamento do seu site ou aplicativo no emulador Surface Duo no Microsoft Edge da área de trabalho não corresponde ao [aplicativo Android do Microsoft Edge][GooglePlayMicrosoftEdge] no [Surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="9d925-162">If the **Experimental Web Platform features** flag is enabled in [desktop Microsoft Edge][MicrosoftEdge] and disabled in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge does not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="9d925-163">Certifique-se de que os sinalizadores sejam compatíveis com o Android e o Microsoft Edge da área de trabalho para usar com êxito o emulador Surface Duo no [Microsoft Edge da área de trabalho][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="9d925-163">Ensure that the flags are matching across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

#### <span data-ttu-id="9d925-164">Testando em dispositivos dobrável e de tela dupla</span><span class="sxs-lookup"><span data-stu-id="9d925-164">Testing on foldable and dual-screen devices</span></span>  

<span data-ttu-id="9d925-165">Quando você emula o [Surface Duo][SurfaceDevicesDuo] em uma postura de tela dupla no Microsoft Edge, a fenda \ (o espaço entre as duas telas \) é desenhada em seu site ou aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9d925-165">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the seam \(the space between the two screens\) is drawn over your website or app.</span></span>  

<span data-ttu-id="9d925-166">A exibição emulada corresponde à maneira como seu site \ (ou app \) renderiza no [aplicativo Android do Microsoft Edge][GooglePlayMicrosoftEdge] em execução em [Surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="9d925-166">The emulated display matches the way your website \(or app\) renders in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] running on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="9d925-167">Pode ser necessário atualizar seu website \ (ou app \) para ser exibido melhor ao longo da fenda.</span><span class="sxs-lookup"><span data-stu-id="9d925-167">You may have to update your website \(or app\) to display better along the seam.</span></span>  <span data-ttu-id="9d925-168">Para obter mais informações sobre como adaptar seu site \ (ou app \) à fenda, navegue até [como trabalhar com a fenda][DualScreenIntroductionHowWorkSeam].</span><span class="sxs-lookup"><span data-stu-id="9d925-168">For more information about adapting your website \(or app\) to the seam, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam].</span></span>  

<span data-ttu-id="9d925-169">A [barra de ferramentas do dispositivo][DevtoolsDeviceModeIndexSimulateMobileViewport] tem recursos adicionais para ajudá-lo a testar seu site ou aplicativo em várias posturas e orientações.</span><span class="sxs-lookup"><span data-stu-id="9d925-169">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="9d925-170">Escolha **girar** \ ( ![ girar ][ImageRotateIcon] \) para girar o visor para a orientação paisagem.</span><span class="sxs-lookup"><span data-stu-id="9d925-170">Choose **Rotate** \(![Rotate][ImageRotateIcon]\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="9d925-171">Combine o recurso com **span** \ ( ![ span ][ImageSpanIcon] \) para alternar entre as posturas de tela única ou dobrada e de tela dupla ou sem dobra.</span><span class="sxs-lookup"><span data-stu-id="9d925-171">Combine the feature with **Span** \(![Span][ImageSpanIcon]\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="9d925-172">Juntos, os recursos permitem testar o seu site ou aplicativo em todas as quatro posturas e orientações possíveis.</span><span class="sxs-lookup"><span data-stu-id="9d925-172">Together, the features enable testing your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matriz de posturas e orientações para dispositivos com tela dupla e dobrável" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="9d925-174">Matriz de posturas e orientações para dispositivos com tela dupla e dobrável</span><span class="sxs-lookup"><span data-stu-id="9d925-174">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="9d925-175">O ícone de **recursos da plataforma da Web experimental** \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \) exibe o estado do sinalizador de **recursos da plataforma da Web experimental** .</span><span class="sxs-lookup"><span data-stu-id="9d925-175">The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="9d925-176">Se o sinalizador estiver ativado, o ícone será realçado.</span><span class="sxs-lookup"><span data-stu-id="9d925-176">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="9d925-177">Se o sinalizador estiver desativado, o ícone não será realçado.</span><span class="sxs-lookup"><span data-stu-id="9d925-177">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="9d925-178">Para ativar \ (ou desligar \) o sinalizador, navegue até `edge://flags` e alterne o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="9d925-178">To turn on \(or off\) the flag, navigate to `edge://flags` and toggle the flag.</span></span>  

<!-- Commenting out until the icon issue is fixed in Edge Canary
The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.  If the flag is turned on, the icon is highlighted.  If the flag is turned off, the icon is not highlighted.  To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.   -->  

<span data-ttu-id="9d925-179">Aqui estão recursos adicionais que podem ajudá-lo a aprimorar seu website \ (ou app \) para dispositivos de tela dupla.</span><span class="sxs-lookup"><span data-stu-id="9d925-179">Here are additional resources that may help you enhance your website \(or app\) for dual-screen devices.</span></span>  

*   <span data-ttu-id="9d925-180">Para obter mais informações sobre o desenvolvimento da Web em dispositivos de tela dupla, acesse [experiências na Web de tela dupla][DualScreenWebIndex].</span><span class="sxs-lookup"><span data-stu-id="9d925-180">For more information about web development on dual-screen devices, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="9d925-181">Instale o [emulador Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="9d925-181">Install the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="9d925-182">Ele é diferente do emulador no Microsoft Edge, emula o Surface Duo executando Android e integra-se ao [Android Studio][AndroidDeveloperStudio].</span><span class="sxs-lookup"><span data-stu-id="9d925-182">It is different from the emulator in Microsoft Edge, emulates the Surface Duo running Android, and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="9d925-183">Para obter mais informações, navegue para [obter o SDK Surface Duo][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="9d925-183">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  
    
> [!NOTE]
> <span data-ttu-id="9d925-184">Veja a seguir uma lista de problemas conhecidos atuais.</span><span class="sxs-lookup"><span data-stu-id="9d925-184">The following is a list of current known issues.</span></span>  
> 
> *   <span data-ttu-id="9d925-185">Ao usar um [cliente de área de trabalho remota da Microsoft][RemoteDesktopClientDocs] para se conectar a um computador remoto e emular o [Surface Duo][SurfaceDevicesDuo] ou a [dobra do Galaxy Galaxy][SamsungMobileGalaxyFold], o ponteiro pode se trave.</span><span class="sxs-lookup"><span data-stu-id="9d925-185">When using a [Microsoft Remote Desktop client][RemoteDesktopClientDocs] to connect to a remote PC and emulate the [Surface Duo][SurfaceDevicesDuo] or [Samsung Galaxy Fold][SamsungMobileGalaxyFold], the pointer may shake or stutter.</span></span>  <span data-ttu-id="9d925-186">Se você tiver problemas, [envie comentários](#providing-feedback-on-experimental-features).</span><span class="sxs-lookup"><span data-stu-id="9d925-186">If you run into the issue, [send feedback](#providing-feedback-on-experimental-features).</span></span>  

### <span data-ttu-id="9d925-187">Habilitar novos recursos de depuração de grade CSS</span><span class="sxs-lookup"><span data-stu-id="9d925-187">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="9d925-188">Este recurso experimental fornece uma série de novas visualizações para ajudar você a depurar layouts de grade CSS.</span><span class="sxs-lookup"><span data-stu-id="9d925-188">This experimental feature provides a number of new visualizations to help you debug CSS grid layouts.</span></span>  <span data-ttu-id="9d925-189">Para visualizar os recursos experimentais mais recentes, [habilite este experimento](#turn-on-experimental-features) e recarregue o devtools.</span><span class="sxs-lookup"><span data-stu-id="9d925-189">To preview the latest experimental features, [enable this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  <span data-ttu-id="9d925-190">Este experimento está ativado por padrão no Microsoft Edge versão 87 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9d925-190">This experiment is on by default in Microsoft Edge version 87 or later.</span></span>  

#### <span data-ttu-id="9d925-191">Exibir sobreposições de grade de foco com a ferramenta inspecionar</span><span class="sxs-lookup"><span data-stu-id="9d925-191">Viewing on-hover grid overlays with the Inspect tool</span></span>  

<span data-ttu-id="9d925-192">A ferramenta **inspecionar** fornece uma maneira rápida de identificar e Visualizar layouts de grade CSS em um site passando o mouse sobre eles.</span><span class="sxs-lookup"><span data-stu-id="9d925-192">The **Inspect** tool provides a quick way to identify and visualize CSS Grid layouts in a website by hovering over them with the mouse.</span></span>  <span data-ttu-id="9d925-193">Escolha o ícone **inspecionar** \ ( ![ inspecionar ][ImageInspectIcon] \) no canto superior esquerdo do devtools.</span><span class="sxs-lookup"><span data-stu-id="9d925-193">Choose the **Inspect** \(![Inspect][ImageInspectIcon]\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="9d925-194">Em seguida, passe o mouse sobre um elemento de grade no site que você está depurando.</span><span class="sxs-lookup"><span data-stu-id="9d925-194">Then, hover over a Grid element on the website you are debugging.</span></span>  <span data-ttu-id="9d925-195">As estruturas de tópicos são exibidas ao lado da grade, e o sombreamento indica o local das lacunas da grade, se houver.</span><span class="sxs-lookup"><span data-stu-id="9d925-195">Outlines are displayed around the grid, and shading indicates the location of grid gaps if present.</span></span>  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Visualização de grades com a ferramenta inspecionar" lightbox="../media/grid-inspect.msft.png":::
   <span data-ttu-id="9d925-197">Visualização de grades com a ferramenta **inspecionar**</span><span class="sxs-lookup"><span data-stu-id="9d925-197">Viewing grids with the **Inspect** tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="9d925-198">Exibindo sobreposições de grade persistente</span><span class="sxs-lookup"><span data-stu-id="9d925-198">Viewing persistent grid overlays</span></span>  

<span data-ttu-id="9d925-199">No Microsoft Edge versão 86 ou posterior, o recurso experimental da CSS da CSS também oferece a opção de habilitar sobreposições de grade persistente.</span><span class="sxs-lookup"><span data-stu-id="9d925-199">In Microsoft Edge version 86 or later, the experimental CSS grid feature also offers the option to enable persistent Grid overlays.</span></span>  <span data-ttu-id="9d925-200">As sobreposições persistentes fornecem vários benefícios.</span><span class="sxs-lookup"><span data-stu-id="9d925-200">The persistent overlays provide several benefits.</span></span>  

*   <span data-ttu-id="9d925-201">As sobreposições persistentes permanecem visíveis na página enquanto você rola, move o mouse e usa outros recursos do DevTools.</span><span class="sxs-lookup"><span data-stu-id="9d925-201">The persistent overlays remain visible on the page as you scroll, move your mouse, and use other features of the DevTools.</span></span>  
*   <span data-ttu-id="9d925-202">Várias sobreposições persistentes podem ser habilitadas ao mesmo tempo, permitindo que você reveja vários layouts de grade ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="9d925-202">Multiple persistent overlays can be enabled at the same time, allowing you to review several grid layouts at once.</span></span>  
*   <span data-ttu-id="9d925-203">Sobreposições persistentes oferecem muitas opções de configuração, como ocultar ou mostrar nomes na área de grade, lacunas de grade, tamanhos de faixa e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9d925-203">Persistent overlays offer many configuration options, such as hiding or showing names in the grid area, grid gaps, track sizes, and so on.</span></span>  
    
<span data-ttu-id="9d925-204">As duas maneiras de alternar uma sobreposição de grade persistente.</span><span class="sxs-lookup"><span data-stu-id="9d925-204">The two ways to toggle a persistent grid overlay.</span></span>  

*   <span data-ttu-id="9d925-205">Escolha o ícone de elipse de **grade** ao lado de qualquer elemento de grade mostrado na árvore dom da ferramenta de **elementos** .</span><span class="sxs-lookup"><span data-stu-id="9d925-205">Choose the **Grid** oval icon next to any Grid element shown in the DOM tree of the **Elements** tool.</span></span>  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Ícone de elipse de grade na ferramenta elementos" lightbox="../media/grid-adorner.msft.png":::
       <span data-ttu-id="9d925-207">Ícone de elipse de grade na ferramenta **elementos**</span><span class="sxs-lookup"><span data-stu-id="9d925-207">Grid oval icon in **Elements** tool</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="9d925-208">Abra o painel novo **layout** localizado na ferramenta elementos e escolha a caixa de seleção ao lado de cada elemento de grade que você deseja realçar.</span><span class="sxs-lookup"><span data-stu-id="9d925-208">Open the new **Layout** panel located in the Elements tool, and choose the checkbox next to each Grid element you want to highlight.</span></span>  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Painel de layout no DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       <span data-ttu-id="9d925-210">Painel de **layout** no devtools</span><span class="sxs-lookup"><span data-stu-id="9d925-210">**Layout** panel in DevTools</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="9d925-211">Configurando sobreposições persistentes</span><span class="sxs-lookup"><span data-stu-id="9d925-211">Configuring persistent overlays</span></span>  

<span data-ttu-id="9d925-212">No Microsoft Edge versão 86 ou posterior, o novo painel de **layout** está localizado na ferramenta **elementos** juntamente com as guias **estilos** e **calculadas** .</span><span class="sxs-lookup"><span data-stu-id="9d925-212">In Microsoft Edge version 86 or later, the new **Layout** panel is located in the **Elements** tool alongside the **Styles** and **Computed** tabs.</span></span>  <span data-ttu-id="9d925-213">O painel de **layout** superfícies as opções de configuração para sobreposições persistentes.</span><span class="sxs-lookup"><span data-stu-id="9d925-213">The **Layout** panel surfaces configuration options for persistent overlays.</span></span>  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Recurso de depuração de grade CSS" lightbox="../media/experiments-grid.msft.png":::
   <span data-ttu-id="9d925-215">Recurso de depuração de grade CSS</span><span class="sxs-lookup"><span data-stu-id="9d925-215">CSS grid debugging feature</span></span>  
:::image-end:::  

### <span data-ttu-id="9d925-216">Habilitar o suporte para mover as guias entre painéis</span><span class="sxs-lookup"><span data-stu-id="9d925-216">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="9d925-217">Normalmente, ferramentas como **elementos** e **rede** só podem abrir no painel principal localizado na parte superior da devtools.</span><span class="sxs-lookup"><span data-stu-id="9d925-217">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="9d925-218">Ferramentas como **modo de exibição 3D** e **problemas** que normalmente são abertos apenas no painel de **gaveta** localizado na parte inferior da devtools.</span><span class="sxs-lookup"><span data-stu-id="9d925-218">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="9d925-219">Depois de escolher o experimento, você poderá mover ferramentas entre os painéis superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="9d925-219">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="9d925-220">Para mover uma ferramenta, passe o mouse sobre a guia, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **mover para o início** ou **mover para o fim**.</span><span class="sxs-lookup"><span data-stu-id="9d925-220">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="9d925-221">Este experimento permite que você personalize o layout do DevTools.</span><span class="sxs-lookup"><span data-stu-id="9d925-221">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="9d925-222">Para mostrar ou ocultar o painel de **gavetas** , selecione `Escape` .</span><span class="sxs-lookup"><span data-stu-id="9d925-222">To show or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Mover guias entre painéis" lightbox="../media/experiments-move-panels.msft.png":::
   <span data-ttu-id="9d925-224">Mover guias entre painéis</span><span class="sxs-lookup"><span data-stu-id="9d925-224">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9d925-225">Habilitar webhint</span><span class="sxs-lookup"><span data-stu-id="9d925-225">Enable webhint</span></span>  

<span data-ttu-id="9d925-226">[webhint][WebhintMain] é uma ferramenta de código-fonte aberto que fornece comentários em tempo real para sites e páginas da Web locais.</span><span class="sxs-lookup"><span data-stu-id="9d925-226">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local web pages.</span></span>  <span data-ttu-id="9d925-227">O tipo de comentário fornecido pela [webhint][WebhintMain].</span><span class="sxs-lookup"><span data-stu-id="9d925-227">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="9d925-228">acessibilidade</span><span class="sxs-lookup"><span data-stu-id="9d925-228">accessibility</span></span>  
*   <span data-ttu-id="9d925-229">compatibilidade entre navegadores</span><span class="sxs-lookup"><span data-stu-id="9d925-229">cross-browser compatibility</span></span>  
*   <span data-ttu-id="9d925-230">segurança</span><span class="sxs-lookup"><span data-stu-id="9d925-230">security</span></span>  
*   <span data-ttu-id="9d925-231">execução</span><span class="sxs-lookup"><span data-stu-id="9d925-231">performance</span></span>  
*   <span data-ttu-id="9d925-232">Aplicativos Web progressivos (PWAs)</span><span class="sxs-lookup"><span data-stu-id="9d925-232">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="9d925-233">outros problemas comuns de desenvolvimento na Web</span><span class="sxs-lookup"><span data-stu-id="9d925-233">other common web development issues</span></span>  
    
<span data-ttu-id="9d925-234">O experimento do [webhint][WebhintMain] exibe os comentários do webhint no painel [problemas][DevtoolsIssues] .</span><span class="sxs-lookup"><span data-stu-id="9d925-234">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="9d925-235">Escolha um problema para exibir a documentação da solução e uma lista dos recursos afetados em seu site.</span><span class="sxs-lookup"><span data-stu-id="9d925-235">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="9d925-236">Escolha um link de recurso para abrir o painel de **rede**, **fontes**ou **elementos** relevantes no devtools.</span><span class="sxs-lookup"><span data-stu-id="9d925-236">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="Comentários da webhint no painel problemas" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="9d925-238">Comentários da webhint no painel **problemas**</span><span class="sxs-lookup"><span data-stu-id="9d925-238">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9d925-239">Habilitar console de rede</span><span class="sxs-lookup"><span data-stu-id="9d925-239">Enable Network Console</span></span>  

<span data-ttu-id="9d925-240">**Console de rede** é o título de trabalho de um experimento para fazer solicitações de rede sintéticas por http.</span><span class="sxs-lookup"><span data-stu-id="9d925-240">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="9d925-241">Você pode usar o experimento do **console de rede** para enviar solicitações de API da Web.</span><span class="sxs-lookup"><span data-stu-id="9d925-241">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="9d925-242">Depois de habilitar o experimento, certifique-se de reiniciar o DevTools.</span><span class="sxs-lookup"><span data-stu-id="9d925-242">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="9d925-243">Para usar o **console de rede**, siga as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d925-243">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="9d925-244">Abra o painel **rede** .</span><span class="sxs-lookup"><span data-stu-id="9d925-244">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="9d925-245">Localize a solicitação de rede que você deseja alterar e envie novamente.</span><span class="sxs-lookup"><span data-stu-id="9d925-245">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="9d925-246">Abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **Editar e reproduzir**.</span><span class="sxs-lookup"><span data-stu-id="9d925-246">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="9d925-247">Quando o **console de rede** for aberto, edite as informações de solicitação de rede.</span><span class="sxs-lookup"><span data-stu-id="9d925-247">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="9d925-248">Escolha **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="9d925-248">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Console de rede na gaveta do console" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="9d925-250">**Console de rede** na gaveta do **console**</span><span class="sxs-lookup"><span data-stu-id="9d925-250">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9d925-251">Visualizador de ordem de origem</span><span class="sxs-lookup"><span data-stu-id="9d925-251">Source Order Viewer</span></span>  

<span data-ttu-id="9d925-252">O **Visualizador de ordem de origem** é um experimento que exibe a ordem dos elementos na fonte da página.</span><span class="sxs-lookup"><span data-stu-id="9d925-252">**Source Order Viewer** is an experiment that displays the order of elements in the page source.</span></span>  <span data-ttu-id="9d925-253">A ordem de exibição na tela pode ser diferente da ordem da fonte, que confundi o leitor de tela e os usuários de teclado.</span><span class="sxs-lookup"><span data-stu-id="9d925-253">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="9d925-254">Use o **Visualizador de pedido de origem** para encontrar as diferenças entre ordem de exibição na tela e a ordem da fonte.</span><span class="sxs-lookup"><span data-stu-id="9d925-254">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="9d925-255">Depois de habilitar o experimento, certifique-se de reiniciar o DevTools.</span><span class="sxs-lookup"><span data-stu-id="9d925-255">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="9d925-256">Para usar o **Visualizador de ordem de origem**, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d925-256">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="9d925-257">Abrir o painel de **elementos** .</span><span class="sxs-lookup"><span data-stu-id="9d925-257">Open the **Elements** pane.</span></span>  
1.  <span data-ttu-id="9d925-258">Abra o painel **acessibilidade** no painel gaveta \ (inferior \).</span><span class="sxs-lookup"><span data-stu-id="9d925-258">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="9d925-259">Na seção **Visualizador de ordem de origem** , escolha a caixa de seleção **Mostrar ordem de origem** .</span><span class="sxs-lookup"><span data-stu-id="9d925-259">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="9d925-260">Realce qualquer elemento HTML para exibir uma sobreposição que a ordem na fonte da página.</span><span class="sxs-lookup"><span data-stu-id="9d925-260">Highlight any HTML element to display an overlay that the order in the page source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Visualizador de ordem de origem no painel Acessibilidade" lightbox="../media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="9d925-262">**Visualizador de ordem de origem** no painel **acessibilidade**</span><span class="sxs-lookup"><span data-stu-id="9d925-262">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <span data-ttu-id="9d925-263">Habilitar o editor de atalhos de teclado</span><span class="sxs-lookup"><span data-stu-id="9d925-263">Enable keyboard shortcut editor</span></span>

<span data-ttu-id="9d925-264">Com o **Editor de atalhos de teclado** ativado o experimento, agora você pode personalizar os atalhos de teclado para qualquer ação no devtools.</span><span class="sxs-lookup"><span data-stu-id="9d925-264">With the **Enable keyboard shortcut editor** experiment turned on, you are now able to customize keyboard shortcuts for any action in the DevTools.</span></span>  <span data-ttu-id="9d925-265">Para personalizar o atalho de teclado para uma ação específica, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d925-265">To customize the keyboard shortcut for a specific action, complete the following steps.</span></span>  

1.  <span data-ttu-id="9d925-266">[Abra o devtools][DevtoolsOpenMain].</span><span class="sxs-lookup"><span data-stu-id="9d925-266">[Open DevTools][DevtoolsOpenMain].</span></span>  
1.  <span data-ttu-id="9d925-267">Abrir [as configurações][DevToolsCustomizeSettings].</span><span class="sxs-lookup"><span data-stu-id="9d925-267">Open [Settings][DevToolsCustomizeSettings].</span></span>
    *   <span data-ttu-id="9d925-268">Selecione `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="9d925-268">Select `Shift`+`?`.</span></span>  
1.  <span data-ttu-id="9d925-269">Navegue até a página **atalhos** .</span><span class="sxs-lookup"><span data-stu-id="9d925-269">Navigate to the **Shortcuts** page.</span></span>  
1.  <span data-ttu-id="9d925-270">Escolha a ação que você deseja personalizar.</span><span class="sxs-lookup"><span data-stu-id="9d925-270">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="9d925-271">Escolha o ícone **Editar** \ ( ![ EditKeyboardShortcut ][ImageEditKeyboardShortcutIcon] \).</span><span class="sxs-lookup"><span data-stu-id="9d925-271">Choose the **Edit** \(![EditKeyboardShortcut][ImageEditKeyboardShortcutIcon]\) icon.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Escolha a ação que deseja personalizar na página atalhos em configurações" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       <span data-ttu-id="9d925-273">Escolha a ação que deseja personalizar na página **atalhos** em [configurações][DevToolsCustomizeSettings]</span><span class="sxs-lookup"><span data-stu-id="9d925-273">Choose the action to customize from the **Shortcuts** page in [Settings][DevToolsCustomizeSettings]</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="9d925-274">No teclado, selecione as teclas que você deseja associar à ação.</span><span class="sxs-lookup"><span data-stu-id="9d925-274">On the keyboard, select the keys you want to bind to the action.</span></span>
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Selecione as teclas que você deseja atribuir à ação" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="9d925-276">Selecione as teclas que você deseja atribuir à ação</span><span class="sxs-lookup"><span data-stu-id="9d925-276">Select the keys you want to assign to the action</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="9d925-277">Para salvar seu novo atalho de teclado, escolha a marca de seleção \ (</span><span class="sxs-lookup"><span data-stu-id="9d925-277">To save your new keyboard shortcut, choose the checkmark \(</span></span>![CheckmarkKeyboardShortcut][ImageCheckmarkKeyboardShortcutIcon]<span data-ttu-id="9d925-279">\) ícone.</span><span class="sxs-lookup"><span data-stu-id="9d925-279">\) icon.</span></span>
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Escolher o ícone de marca de seleção para salvar o novo atalho de teclado" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="9d925-281">Escolher o ícone de marca de seleção para salvar o novo atalho de teclado</span><span class="sxs-lookup"><span data-stu-id="9d925-281">Choose the checkmark icon to save your new keyboard shortcut</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="9d925-282">Selecione o novo atalho de teclado para disparar a ação no DevTools.</span><span class="sxs-lookup"><span data-stu-id="9d925-282">Select your new keyboard shortcut to trigger the action in the DevTools.</span></span>  
    
<span data-ttu-id="9d925-283">Na página **atalhos** , o ícone de **atalho de teclado personalizado** \ ( ![ CustomKeyboardShortcut ][ImageCustomKeyboardShortcutIcon] \) exibe os atalhos de teclado que você personalizou.</span><span class="sxs-lookup"><span data-stu-id="9d925-283">On the **Shortcuts** page, the **Custom Keyboard Shortcut** \(![CustomKeyboardShortcut][ImageCustomKeyboardShortcutIcon]\) icon displays keyboard shortcuts that you have customized.</span></span>  <span data-ttu-id="9d925-284">Para redefinir todos os atalhos, escolha **restaurar atalhos padrão**.</span><span class="sxs-lookup"><span data-stu-id="9d925-284">To reset all shortcuts, choose **Restore default shortcuts**.</span></span>  

<span data-ttu-id="9d925-285">Quando você estiver editando os atalhos de teclado para uma ação, para descartar suas alterações, escolha o ícone X \ ( ![ XKeyboardShortcut ][ImageXKeyboardShortcutIcon] \).</span><span class="sxs-lookup"><span data-stu-id="9d925-285">When you are editing the keyboard shortcuts for an action, to discard your changes, choose the X \(![XKeyboardShortcut][ImageXKeyboardShortcutIcon]\) icon.</span></span>  <span data-ttu-id="9d925-286">Para remover atalhos de uma ação específica, escolha o ícone **excluir atalho** \ ( ![ DeleteKeyboardShortcut ][ImageDeleteKeyboardShortcutIcon] \).</span><span class="sxs-lookup"><span data-stu-id="9d925-286">To remove shortcuts for a specific action, choose the **Delete shortcut** \(![DeleteKeyboardShortcut][ImageDeleteKeyboardShortcutIcon]\) icon.</span></span>  <span data-ttu-id="9d925-287">Para adicionar vários atalhos para uma ação, escolha **Adicionar um atalho**.</span><span class="sxs-lookup"><span data-stu-id="9d925-287">To add multiple shortcuts for an action, choose **Add a shortcut**.</span></span>

> [!NOTE]
> <span data-ttu-id="9d925-288">Se um atalho de teclado estiver atribuído atualmente a outra ação, você não poderá salvá-lo para uma nova ação.</span><span class="sxs-lookup"><span data-stu-id="9d925-288">If a keyboard shortcut is currently assigned to another action, you are not able to save it for a new action.</span></span>  <span data-ttu-id="9d925-289">Você deve primeiro excluir o atalho de teclado para a ação anterior e, em seguida, adicioná-lo à nova ação.</span><span class="sxs-lookup"><span data-stu-id="9d925-289">You must first delete the keyboard shortcut for the previous action and then add it to the new action.</span></span>  

<!--Available in Microsoft Edge version 87 and later.  -->

### <span data-ttu-id="9d925-290">Ativar camadas compostas no modo de exibição 3D</span><span class="sxs-lookup"><span data-stu-id="9d925-290">Turn on Composited Layers in 3D View</span></span>

<span data-ttu-id="9d925-291">Agora você pode visualizar camadas juntamente com os índices z e o modelo de objeto do documento \ (DOM \).</span><span class="sxs-lookup"><span data-stu-id="9d925-291">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="9d925-292">Esse recurso ajuda você a depurar sem mudar de contextos com frequência.</span><span class="sxs-lookup"><span data-stu-id="9d925-292">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="9d925-293">Você identificou que reduzir a alternância de contexto era um grande ponto problemático.</span><span class="sxs-lookup"><span data-stu-id="9d925-293">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="9d925-294">Nem sempre fica claro como o código que você escreve afeta o aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="9d925-294">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="9d925-295">Para uma experiência de depuração visual abrangente, o Modo de exibição 3D e as camadas compostas agora são combinados.</span><span class="sxs-lookup"><span data-stu-id="9d925-295">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  <span data-ttu-id="9d925-296">Depois de habilitar o experimento, certifique-se de reiniciar o DevTools.</span><span class="sxs-lookup"><span data-stu-id="9d925-296">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="9d925-297">Para usar **camadas compostas**, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d925-297">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="9d925-298">Na gaveta, escolha a ferramenta **modo de exibição 3D** .</span><span class="sxs-lookup"><span data-stu-id="9d925-298">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="9d925-299">Abrir o painel de **camadas compostas** .</span><span class="sxs-lookup"><span data-stu-id="9d925-299">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="9d925-300">Todas as camadas pintadas do aplicativo são exibidas.</span><span class="sxs-lookup"><span data-stu-id="9d925-300">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="9d925-301">Experimente este recurso com seus próprios aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="9d925-301">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Painel de Camadas compostas" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="9d925-303">Painel de **Camadas Compostas**</span><span class="sxs-lookup"><span data-stu-id="9d925-303">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

## <span data-ttu-id="9d925-304">Recursos experimentais anteriores</span><span class="sxs-lookup"><span data-stu-id="9d925-304">Previous experimental features</span></span>  

*   <span data-ttu-id="9d925-305">o [modo de exibição 3D][Devtools3dViewIndex] agora está disponível e ativado por padrão no Microsoft Edge versão 83 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9d925-305">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="9d925-306">[Personalizar atalhos de teclado][DevtoolsCustomKeyboardShortcuts] agora está disponível e ativado por padrão no Microsoft Edge versão 86 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9d925-306">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  

## <span data-ttu-id="9d925-307">Fornecer comentários sobre os recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="9d925-307">Providing feedback on experimental features</span></span>  

<span data-ttu-id="9d925-308">Para fornecer comentários sobre o Microsoft Edge DevTools experimentos ou qualquer outro item relacionado ao DevTools.</span><span class="sxs-lookup"><span data-stu-id="9d925-308">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="9d925-309">Envie seus comentários usando o ícone **enviar comentários** no devtools</span><span class="sxs-lookup"><span data-stu-id="9d925-309">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="9d925-310">Tweet em [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="9d925-310">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="O ícone enviar comentários no Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="9d925-312">O ícone **enviar comentários** no Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="9d925-312">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- image links -->  

[ImageCheckmarkKeyboardShortcutIcon]: ../media/checkmark-keyboard-shortcut-icon.msft.png  
[ImageCustomKeyboardShortcutIcon]: ../media/custom-keyboard-shortcut-icon.msft.png  
[ImageDeleteKeyboardShortcutIcon]: ../media/delete-keyboard-shortcut-icon.msft.png  
[ImageEditKeyboardShortcutIcon]: ../media/edit-keyboard-shortcut-icon.msft.png  
[ImageExperimentalApisIcon]: ../media/experimental-apis-dark-icon.msft.png  
[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  
[ImageSpanIcon]: ../media/span-dark-icon.msft.png  
[ImageXKeyboardShortcutIcon]: ../media/discard-changes-keyboard-shortcut-icon.msft.png  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Modo de exibição 3D | Microsoft Docs"  
[DevToolsCustomizeSettings]: ../customize/index.md#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsIssues]: ../issues/index.md "Localizar e corrigir problemas com a ferramenta Issues do DevTools do Microsoft Edge | Microsoft Docs"  
[DevToolsShortcuts]: ../shortcuts/index.md "Atalhos de teclado do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Personalizar atalhos de teclado no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsOpenMain]: ../open/index.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  

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
