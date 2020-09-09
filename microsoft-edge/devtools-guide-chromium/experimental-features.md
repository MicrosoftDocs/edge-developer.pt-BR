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
# <span data-ttu-id="9aa92-104">Recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="9aa92-104">Experimental features</span></span>  

<span data-ttu-id="9aa92-105">O Microsoft Edge DevTools fornece acesso a recursos experimentais que ainda estão em desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="9aa92-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="9aa92-106">Você pode testar e p[fornecer comentários](#providing-feedback-on-experimental-features) antes que cada recurso seja lançado.</span><span class="sxs-lookup"><span data-stu-id="9aa92-106">You may test and p[provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="9aa92-107">Embora os recursos experimentais estejam disponíveis em todos os canais do Microsoft Edge, você pode obter os recursos experimentais mais recentes usando o Microsoft Edge Canárias Channel.</span><span class="sxs-lookup"><span data-stu-id="9aa92-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="9aa92-108">Ativar os recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="9aa92-108">Turn on experimental features</span></span>  

<span data-ttu-id="9aa92-109">Use as etapas a seguir para ativar \ (ou desligado \) recursos experimentais no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9aa92-109">Use the following steps to turn on \(or off\) experimental features in Microsoft Edge.</span></span>  

1.  <span data-ttu-id="9aa92-110">[Abra o devtools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="9aa92-110">[Open DevTools][DevtoolsOpen].</span></span>  
     *   <span data-ttu-id="9aa92-111">Selecione `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="9aa92-111">Select `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="9aa92-112">Para obter mais informações, consulte [atalhos de teclado do Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="9aa92-112">For more information, see [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="9aa92-113">Abra o painel [configurações][DevToolsCustomizeSettings] .</span><span class="sxs-lookup"><span data-stu-id="9aa92-113">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="9aa92-114">Selecione `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="9aa92-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="9aa92-115">Para obter mais informações, navegue até [atalhos de teclado do Microsoft Edge devtools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="9aa92-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="9aa92-116">No lado esquerdo do painel **configurações** , escolha a seção **experimentos** .</span><span class="sxs-lookup"><span data-stu-id="9aa92-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.msft.png" alt-text="Lista de experimentos nas configurações do DevTools" lightbox="./media/experiments-devtools.msft.png":::
       <span data-ttu-id="9aa92-118">Lista de experimentos nas configurações do DevTools</span><span class="sxs-lookup"><span data-stu-id="9aa92-118">List of experiments in DevTools Settings</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9aa92-119">Na página **experimentos** , percorra a lista de todos os recursos experimentais disponíveis e escolha a caixa de seleção ao lado de cada recurso que você deseja testar.</span><span class="sxs-lookup"><span data-stu-id="9aa92-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="9aa92-120">Feche e abra novamente o Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="9aa92-120">Close and reopen Microsoft Edge DevTools.</span></span>  

> [!NOTE]
> <span data-ttu-id="9aa92-121">Os recursos experimentais são atualizados constantemente e podem causar problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="9aa92-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="9aa92-122">Para desativar um recurso experimental, abra a página **experimentos** e desmarque a caixa de seleção do recurso experimental que você deseja desativar.</span><span class="sxs-lookup"><span data-stu-id="9aa92-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="9aa92-123">Recursos experimentais realçados</span><span class="sxs-lookup"><span data-stu-id="9aa92-123">Highlighted experimental features</span></span>  

<span data-ttu-id="9aa92-124">As seções a seguir descrevem os novos recursos experimentais que estão disponíveis no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9aa92-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="9aa92-125">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="9aa92-125">Experimental feature</span></span> | <span data-ttu-id="9aa92-126">Microsoft Edge versão</span><span class="sxs-lookup"><span data-stu-id="9aa92-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="9aa92-127">Habilitar a guia Configurações de atalhos de teclado personalizados</span><span class="sxs-lookup"><span data-stu-id="9aa92-127">Enable custom keyboard shortcuts settings tab</span></span>](#enable-custom-keyboard-shortcuts-settings-tab) | <span data-ttu-id="9aa92-128">84 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9aa92-128">84 or later</span></span> |
| [<span data-ttu-id="9aa92-129">Emulação: suporta o modo de tela dupla</span><span class="sxs-lookup"><span data-stu-id="9aa92-129">Emulation: Support dual screen mode</span></span>](#emulation-support-dual-screen-mode) | <span data-ttu-id="9aa92-130">84 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9aa92-130">84 or later</span></span> |  
| [<span data-ttu-id="9aa92-131">Habilitar novos recursos de depuração de grade CSS</span><span class="sxs-lookup"><span data-stu-id="9aa92-131">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="9aa92-132">85 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9aa92-132">85 or later</span></span> |  
| [<span data-ttu-id="9aa92-133">Habilitar o suporte para mover as guias entre painéis</span><span class="sxs-lookup"><span data-stu-id="9aa92-133">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="9aa92-134">85 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9aa92-134">85 or later</span></span> |  
| [<span data-ttu-id="9aa92-135">Habilitar webhint</span><span class="sxs-lookup"><span data-stu-id="9aa92-135">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="9aa92-136">85 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9aa92-136">85 or later</span></span> |  
| [<span data-ttu-id="9aa92-137">Habilitar console de rede</span><span class="sxs-lookup"><span data-stu-id="9aa92-137">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="9aa92-138">85 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9aa92-138">85 or later</span></span> |  
| [<span data-ttu-id="9aa92-139">Habilitar o Visualizador de ordem de origem</span><span class="sxs-lookup"><span data-stu-id="9aa92-139">Enable Source Order Viewer</span></span>](#enable-source-order-viewer) | <span data-ttu-id="9aa92-140">86 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9aa92-140">86 or later</span></span> |  

### <span data-ttu-id="9aa92-141">Habilitar a guia Configurações de atalhos de teclado personalizados</span><span class="sxs-lookup"><span data-stu-id="9aa92-141">Enable custom keyboard shortcuts settings tab</span></span>  

<span data-ttu-id="9aa92-142">Fornece uma nova página **atalhos** nas [configurações do devtools][DevToolsCustomizeSettings] para corresponder os atalhos de [teclado][DevToolsShortcuts] no código do devtools ao [Microsoft Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="9aa92-142">Provides a new **Shortcuts** page in [DevTools Settings][DevToolsCustomizeSettings] to match [keyboard shortcuts][DevToolsShortcuts] in the DevTools to [Microsoft Visual Studio Code][VisualstudioCode].</span></span>  

<span data-ttu-id="9aa92-143">Depois de habilitar o experimento, abra [as configurações do devtools][DevToolsCustomizeSettings] novamente usando selecionar `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="9aa92-143">After you enable the experiment, open [DevTools Settings][DevToolsCustomizeSettings] again using select `Shift`+`?`.</span></span>  <span data-ttu-id="9aa92-144">Navegue até a página novos **atalhos** .</span><span class="sxs-lookup"><span data-stu-id="9aa92-144">Navigate to the new **Shortcuts** page.</span></span>  <span data-ttu-id="9aa92-145">Selecione **devtools (padrão)** na lista suspensa **coincidir os atalhos de predefinir** e selecione **código do Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="9aa92-145">Select **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="9aa92-146">Os atalhos de teclado no DevTools agora correspondem aos atalhos para ações equivalentes no código do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9aa92-146">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in Visual Studio Code.</span></span>  

:::image type="complex" source="./media/experiments-keyboard-shortcut.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="./media/experiments-keyboard-shortcut.msft.png":::
   <span data-ttu-id="9aa92-148">Corresponder os atalhos de teclado no código do DevTools para o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9aa92-148">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="9aa92-149">Por exemplo, no Windows, o atalho de teclado para pausar ou continuar a execução de um script no [código do Visual Studio][VisualstudioCodeShortcutsKeyboardWindows] é `F5` .</span><span class="sxs-lookup"><span data-stu-id="9aa92-149">For example, on Windows the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualstudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="9aa92-150">Com a predefinição **devtools (padrão)** , o mesmo atalho no devtools é `F8` .</span><span class="sxs-lookup"><span data-stu-id="9aa92-150">With the **DevTools (Default)** preset, the same shortcut in the DevTools is `F8`.</span></span>  <span data-ttu-id="9aa92-151">Com a predefinição de **código do Visual Studio** , o atalho também é `F5` .</span><span class="sxs-lookup"><span data-stu-id="9aa92-151">With the **Visual Studio Code** preset, the shortcut is also `F5`.</span></span>  

### <span data-ttu-id="9aa92-152">Emulação: suporta o modo de tela dupla</span><span class="sxs-lookup"><span data-stu-id="9aa92-152">Emulation: Support dual screen mode</span></span>  

<span data-ttu-id="9aa92-153">Fornece recursos adicionais para emular dois novos dispositivos de tela dupla e de dobrável no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9aa92-153">Provides additional features for emulating two new dual-screen and foldable devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="9aa92-154">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="9aa92-154">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="9aa92-155">Dobra Samsung Galaxy</span><span class="sxs-lookup"><span data-stu-id="9aa92-155">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  

<span data-ttu-id="9aa92-156">EMule os dispositivos e alterne entre as seguintes condições.</span><span class="sxs-lookup"><span data-stu-id="9aa92-156">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="9aa92-157">postura de tela única ou dobrada</span><span class="sxs-lookup"><span data-stu-id="9aa92-157">single-screen or folded posture</span></span>  
*   <span data-ttu-id="9aa92-158">postura de tela dupla ou não dobrada</span><span class="sxs-lookup"><span data-stu-id="9aa92-158">dual-screen or unfolded posture</span></span>  

<span data-ttu-id="9aa92-159">Use o recurso [habilitar APIs experimentales](#enable-experimental-apis) para aprimorar seu site \ (ou app \) para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9aa92-159">Use the [enable experimental APIs](#enable-experimental-apis) to enhance your website \(or app\) for a device.</span></span>  <span data-ttu-id="9aa92-160">Você também pode usar as [consultas de mídia CSS e a API de enumeração de segmento do Windows JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].</span><span class="sxs-lookup"><span data-stu-id="9aa92-160">You may also use the [CSS media queries and the JavaScript Windows Segment Enumeration API][GitHubMicrosoftedgeMsedgeexplainerFoldables].</span></span>  

<!-- This image was taken in Chromium Canary since we don't yet have an Edge Canary that has Stan's changes -->  

:::image type="complex" source="./media/experiments-dual-screen-emulation.msft.png" alt-text="Emular superfície Duo no Microsoft Edge" lightbox="./media/experiments-dual-screen-emulation.msft.png":::  
   <span data-ttu-id="9aa92-162">Emular superfície Duo no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9aa92-162">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

#### <span data-ttu-id="9aa92-163">Habilitar APIs experimentais</span><span class="sxs-lookup"><span data-stu-id="9aa92-163">Enable experimental APIs</span></span>  

<span data-ttu-id="9aa92-164">Para [habilitar esse experimento](#turn-on-experimental-features) no Microsoft Edge devtools, siga as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9aa92-164">To [enable this experiment](#turn-on-experimental-features) in the Microsoft Edge DevTools, complete the following steps.</span></span>  

1.  <span data-ttu-id="9aa92-165">Navegue até `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="9aa92-165">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="9aa92-166">Na caixa de texto de **sinalizadores de pesquisa** , digite `Experimental Web Platform features` , escolha o sinalizador de **recursos da plataforma da Web experimental** e alterar **desabilitado** como **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="9aa92-166">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="9aa92-167">Reinicie o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9aa92-167">Restart Microsoft Edge.</span></span>  

<span data-ttu-id="9aa92-168">Para aprimorar seu site ou aplicativo para dispositivos com tela dupla e dobrável, navegue até [consultas de mídia CSS e a API de enumeração de segmento do Windows JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].</span><span class="sxs-lookup"><span data-stu-id="9aa92-168">To enhance your website or app for dual-screen and foldable devices, navigate to [CSS media queries and the JavaScript Windows Segment Enumeration API][GitHubMicrosoftedgeMsedgeexplainerFoldables].</span></span>

<span data-ttu-id="9aa92-169">[Ative este experimento](#turn-on-experimental-features) no Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="9aa92-169">[Turn on this experiment](#turn-on-experimental-features) in the Microsoft Edge DevTools.</span></span>  

1.  <span data-ttu-id="9aa92-170">Abra uma nova guia no Microsoft Edge e navegue até `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="9aa92-170">Open a new tab in Microsoft Edge and navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="9aa92-171">Na caixa de texto de **sinalizadores de pesquisa** , insira `Experimental Web Platform features` , escolha **recursos da plataforma da Web experimental**e alterar **desabilitado** como **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="9aa92-171">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose **Experimental Web Platform features**, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="9aa92-172">Reinicie o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9aa92-172">Restart Microsoft Edge.</span></span>  

<span data-ttu-id="9aa92-173">Para obter mais informações sobre como aprimorar seu site \ (ou app \) para dispositivos de tela dupla e dobrável, navegue até [consultas de mídia CSS e API de enumeração de segmento do Windows JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].</span><span class="sxs-lookup"><span data-stu-id="9aa92-173">For more information about enhancing your website \(or app\) for dual-screen and foldable devices, navigate to [CSS media queries and the JavaScript Windows Segment Enumeration API][GitHubMicrosoftedgeMsedgeexplainerFoldables].</span></span>  

:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Habilitar o sinalizador de recursos da plataforma da Web experimental" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="9aa92-175">Habilitar o sinalizador de recursos da plataforma da Web experimental</span><span class="sxs-lookup"><span data-stu-id="9aa92-175">Enable the Experimental Web Platform features flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="9aa92-176">Se você estiver usando [consultas de mídia CSS ou a API de enumeração de segmento do Windows JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables] para aprimorar seu site ou aplicativo para o [Surface Duo][SurfaceDevicesDuo], também deverá habilitar o sinalizador de **recursos da plataforma da Web experimental** no [aplicativo Android do Microsoft Edge][GooglePlayMicrosoftEdge] em seu dispositivo [Surface Duo][SurfaceDevicesDuo] .</span><span class="sxs-lookup"><span data-stu-id="9aa92-176">If you are using [CSS media queries or the JavaScript Windows Segment Enumeration API][GitHubMicrosoftedgeMsedgeexplainerFoldables] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also enable the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>
> 
> <span data-ttu-id="9aa92-177">Se o sinalizador de **recursos da plataforma da Web experimental** estiver habilitado no [Microsoft Edge da área de trabalho][MicrosoftEdge] e desabilitado no [aplicativo Android do Microsoft Edge][GooglePlayMicrosoftEdge], o comportamento do seu site ou aplicativo no emulador Surface Duo no Microsoft Edge da área de trabalho não será compatível com o [aplicativo Microsoft Edge do Android][GooglePlayMicrosoftEdge] no [Surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="9aa92-177">If the **Experimental Web Platform features** flag is enabled in [desktop Microsoft Edge][MicrosoftEdge] and disabled in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge will not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="9aa92-178">Certifique-se de que os sinalizadores sejam compatíveis com o Android e o Microsoft Edge da área de trabalho para usar com êxito o emulador Surface Duo no [Microsoft Edge da área de trabalho][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="9aa92-178">Ensure that the flags are matching across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

#### <span data-ttu-id="9aa92-179">Testando em dispositivos dobrável e de tela dupla</span><span class="sxs-lookup"><span data-stu-id="9aa92-179">Testing on foldable and dual-screen devices</span></span>  

<span data-ttu-id="9aa92-180">Quando você emula o [Surface Duo][SurfaceDevicesDuo] em uma postura de tela dupla no Microsoft Edge, a **fenda** é desenhada sobre seu site ou aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9aa92-180">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the **seam** is drawn over your website or app.</span></span>  

> [!NOTE]
> <span data-ttu-id="9aa92-181">A **fenda** é o espaço entre as duas telas.</span><span class="sxs-lookup"><span data-stu-id="9aa92-181">The **seam** is the space between the two screens.</span></span>  

<span data-ttu-id="9aa92-182">A exibição emulada do seu site \ (ou app \) é uma representação correta.</span><span class="sxs-lookup"><span data-stu-id="9aa92-182">The emulated display for your website \(or app\) is a correct representation.</span></span>  <span data-ttu-id="9aa92-183">Ele corresponde à exibição no [aplicativo Android do Microsoft Edge][GooglePlayMicrosoftEdge] no [Surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="9aa92-183">It matches the display in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="9aa92-184">Atualize o conteúdo para exibi-lo melhor ao longo da **fenda**.</span><span class="sxs-lookup"><span data-stu-id="9aa92-184">Update the content to display better along the **seam**.</span></span>  <span data-ttu-id="9aa92-185">Para obter mais informações sobre como adaptar seu site \ (ou app \) à **fenda**, navegue até [como trabalhar com a fenda][DualScreenIntroductionHowWorkSeam] na documentação do Surface Duo.</span><span class="sxs-lookup"><span data-stu-id="9aa92-185">For more information about adapting your website \(or app\) to the **seam**, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam] in the Surface Duo documentation.</span></span>  

<span data-ttu-id="9aa92-186">A [barra de ferramentas do dispositivo][DevtoolsDeviceModeIndexSimulateMobileViewport] tem recursos adicionais para ajudá-lo a testar seu site ou aplicativo em várias posturas e orientações.</span><span class="sxs-lookup"><span data-stu-id="9aa92-186">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="9aa92-187">Escolha **girar** \ ( ![ girar ][ImageRotateIcon] \) para girar o visor para a orientação paisagem.</span><span class="sxs-lookup"><span data-stu-id="9aa92-187">Choose **Rotate** \(![Rotate][ImageRotateIcon]\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="9aa92-188">Combine o recurso com **span** \ ( ![ span ][ImageSpanIcon] \) para alternar entre as posturas de tela única ou dobrada e de tela dupla ou sem dobra.</span><span class="sxs-lookup"><span data-stu-id="9aa92-188">Combine the feature with **Span** \(![Span][ImageSpanIcon]\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="9aa92-189">Juntos, os recursos permitem testar o seu site ou aplicativo em todas as quatro posturas e orientações possíveis.</span><span class="sxs-lookup"><span data-stu-id="9aa92-189">Together, the features enable testing your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matriz de posturas e orientações para dispositivos com tela dupla e dobrável" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="9aa92-191">Matriz de posturas e orientações para dispositivos com tela dupla e dobrável</span><span class="sxs-lookup"><span data-stu-id="9aa92-191">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="9aa92-192">O ícone de **recursos da plataforma da Web experimental** \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \) exibe o estado do sinalizador de **recursos da plataforma da Web experimental** .</span><span class="sxs-lookup"><span data-stu-id="9aa92-192">The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="9aa92-193">Se o sinalizador estiver ativado, o ícone será realçado.</span><span class="sxs-lookup"><span data-stu-id="9aa92-193">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="9aa92-194">Se o sinalizador estiver desativado, o ícone não será realçado.</span><span class="sxs-lookup"><span data-stu-id="9aa92-194">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="9aa92-195">Para ativar \ (ou desligar \) o sinalizador, escolha o ícone ou navegue até `edge://flags` o sinalizador e alterne-o.</span><span class="sxs-lookup"><span data-stu-id="9aa92-195">To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.</span></span>  

#### <span data-ttu-id="9aa92-196">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="9aa92-196">Additional resources</span></span>  
*   <span data-ttu-id="9aa92-197">Para obter mais informações sobre o desenvolvimento, navegue até [experiências na Web de tela dupla][DualScreenWebIndex].</span><span class="sxs-lookup"><span data-stu-id="9aa92-197">For more information about developing, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="9aa92-198">Instale o emulador Surface Duo].</span><span class="sxs-lookup"><span data-stu-id="9aa92-198">Install the Surface Duo emulator].</span></span>  <span data-ttu-id="9aa92-199">Ele é diferente do emulador no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9aa92-199">It is different from the emulator in Microsoft Edge.</span></span>  <span data-ttu-id="9aa92-200">Ele emula o Surface duo que executa o Android e integra-se ao [Android Studio][AndroidDeveloperStudio].</span><span class="sxs-lookup"><span data-stu-id="9aa92-200">It emulates the Surface Duo running Android and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="9aa92-201">Para obter mais informações, navegue para [obter o SDK Surface Duo][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="9aa92-201">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

### <span data-ttu-id="9aa92-202">Habilitar novos recursos de depuração de grade CSS</span><span class="sxs-lookup"><span data-stu-id="9aa92-202">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="9aa92-203">Aprimora as visualizações na página quando você depura sites que têm layouts de grade CSS.</span><span class="sxs-lookup"><span data-stu-id="9aa92-203">Improves on-page visualizations when you debug websites that have CSS grid layouts.</span></span>  <span data-ttu-id="9aa92-204">Você pode personalizar ainda mais as sobreposições nas configurações do DevTools.</span><span class="sxs-lookup"><span data-stu-id="9aa92-204">You may further customize the overlays in DevTools Settings.</span></span>  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="Recurso de depuração de grade CSS" lightbox="./media/experiments-grid.msft.png":::
   <span data-ttu-id="9aa92-206">Recurso de depuração de grade CSS</span><span class="sxs-lookup"><span data-stu-id="9aa92-206">CSS grid debugging feature</span></span>  
:::image-end:::  

<span data-ttu-id="9aa92-207">Para visualizar os recursos experimentais mais recentes, conclua as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="9aa92-207">To preview the latest experimental features, complete the following actions.</span></span>  

1.  <span data-ttu-id="9aa92-208">Na seção **experimentos** , escolha a caixa de seleção **habilitar novos recursos de depuração de grade CSS (opções de configuração disponíveis no painel de barra lateral de layout nos elementos após a reinicialização)** .</span><span class="sxs-lookup"><span data-stu-id="9aa92-208">In the **Experiments** section, choose the **Enable new CSS Grid debugging features (configuration options available in Layout sidebar pane in Elements after restart)** checkbox.</span></span>  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9aa92-209">Habilitar o suporte para mover as guias entre painéis</span><span class="sxs-lookup"><span data-stu-id="9aa92-209">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="9aa92-210">Normalmente, ferramentas como **elementos** e **rede** só podem abrir no painel principal localizado na parte superior da devtools.</span><span class="sxs-lookup"><span data-stu-id="9aa92-210">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="9aa92-211">Ferramentas como **modo de exibição 3D** e **problemas** que normalmente são abertos apenas no painel de **gaveta** localizado na parte inferior da devtools.</span><span class="sxs-lookup"><span data-stu-id="9aa92-211">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="9aa92-212">Depois de escolher o experimento, você poderá mover ferramentas entre os painéis superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="9aa92-212">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="9aa92-213">Para mover uma ferramenta, passe o mouse sobre a guia, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **mover para o início** ou **mover para o fim**.</span><span class="sxs-lookup"><span data-stu-id="9aa92-213">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="9aa92-214">Este experimento permite que você personalize o layout do DevTools.</span><span class="sxs-lookup"><span data-stu-id="9aa92-214">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="9aa92-215">Para mostrar ou ocultar o painel de **gavetas** , selecione `Escape` .</span><span class="sxs-lookup"><span data-stu-id="9aa92-215">To show or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Mover guias entre painéis" lightbox="./media/experiments-move-panels.msft.png":::
   <span data-ttu-id="9aa92-217">Mover guias entre painéis</span><span class="sxs-lookup"><span data-stu-id="9aa92-217">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9aa92-218">Habilitar webhint</span><span class="sxs-lookup"><span data-stu-id="9aa92-218">Enable webhint</span></span>  

<span data-ttu-id="9aa92-219">[webhint][WebhintMain] é uma ferramenta de código-fonte aberto que fornece comentários em tempo real para sites e páginas da Web locais.</span><span class="sxs-lookup"><span data-stu-id="9aa92-219">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local web pages.</span></span>  <span data-ttu-id="9aa92-220">O tipo de comentário fornecido pela [webhint][WebhintMain].</span><span class="sxs-lookup"><span data-stu-id="9aa92-220">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="9aa92-221">acessibilidade</span><span class="sxs-lookup"><span data-stu-id="9aa92-221">accessibility</span></span>  
*   <span data-ttu-id="9aa92-222">compatibilidade entre navegadores</span><span class="sxs-lookup"><span data-stu-id="9aa92-222">cross-browser compatibility</span></span>  
*   <span data-ttu-id="9aa92-223">segurança</span><span class="sxs-lookup"><span data-stu-id="9aa92-223">security</span></span>  
*   <span data-ttu-id="9aa92-224">execução</span><span class="sxs-lookup"><span data-stu-id="9aa92-224">performance</span></span>  
*   <span data-ttu-id="9aa92-225">PWAs</span><span class="sxs-lookup"><span data-stu-id="9aa92-225">PWAs</span></span>  
*   <span data-ttu-id="9aa92-226">outros problemas comuns de desenvolvimento na Web</span><span class="sxs-lookup"><span data-stu-id="9aa92-226">other common web development issues</span></span>  

<span data-ttu-id="9aa92-227">O experimento do [webhint][WebhintMain] exibe os comentários do webhint no painel [problemas][DevtoolsIssues] .</span><span class="sxs-lookup"><span data-stu-id="9aa92-227">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="9aa92-228">Selecione um problema para exibir a documentação da solução e uma lista dos recursos afetados em seu site.</span><span class="sxs-lookup"><span data-stu-id="9aa92-228">Select an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="9aa92-229">Selecione um link de recurso para abrir o painel de **rede**, **fontes**ou **elementos** relevantes no devtools.</span><span class="sxs-lookup"><span data-stu-id="9aa92-229">Select a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="Comentários da webhint no painel problemas" lightbox="./media/experiments-webhint.msft.png":::
   <span data-ttu-id="9aa92-231">Comentários da webhint no painel **problemas**</span><span class="sxs-lookup"><span data-stu-id="9aa92-231">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9aa92-232">Habilitar console de rede</span><span class="sxs-lookup"><span data-stu-id="9aa92-232">Enable Network Console</span></span>  

<span data-ttu-id="9aa92-233">**Console de rede** é o título de trabalho de um experimento para fazer solicitações de rede sintéticas por http.</span><span class="sxs-lookup"><span data-stu-id="9aa92-233">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="9aa92-234">Você pode usar o experimento do **console de rede** para enviar solicitações de API da Web.</span><span class="sxs-lookup"><span data-stu-id="9aa92-234">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="9aa92-235">Depois de habilitar o experimento, certifique-se de reiniciar o DevTools.</span><span class="sxs-lookup"><span data-stu-id="9aa92-235">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="9aa92-236">Para usar o **console de rede**, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9aa92-236">To use the **Network Console**, use the following steps.</span></span>    

1.  <span data-ttu-id="9aa92-237">Abra o painel **rede** .</span><span class="sxs-lookup"><span data-stu-id="9aa92-237">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="9aa92-238">Localize a solicitação de rede que você deseja alterar e envie novamente.</span><span class="sxs-lookup"><span data-stu-id="9aa92-238">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="9aa92-239">Abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **Editar e reproduzir**.</span><span class="sxs-lookup"><span data-stu-id="9aa92-239">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="9aa92-240">Quando o **console de rede** for aberto, edite as informações de solicitação de rede.</span><span class="sxs-lookup"><span data-stu-id="9aa92-240">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="9aa92-241">Selecione **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="9aa92-241">Select **Send**.</span></span>  

:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Console de rede na gaveta do console" lightbox="./media/network-network-console.msft.png":::
   <span data-ttu-id="9aa92-243">**Console de rede** na gaveta do **console**</span><span class="sxs-lookup"><span data-stu-id="9aa92-243">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="9aa92-244">Habilitar o Visualizador de ordem de origem</span><span class="sxs-lookup"><span data-stu-id="9aa92-244">Enable Source Order Viewer</span></span>  

<span data-ttu-id="9aa92-245">O **Visualizador de ordem de origem** é um experimento que exibe a ordem dos elementos na fonte da página.</span><span class="sxs-lookup"><span data-stu-id="9aa92-245">**Source Order Viewer** is an experiment that displays the order of elements in the page source.</span></span>  <span data-ttu-id="9aa92-246">A ordem de exibição na tela pode ser diferente da ordem da fonte, que confundi o leitor de tela e os usuários de teclado.</span><span class="sxs-lookup"><span data-stu-id="9aa92-246">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="9aa92-247">Use o **Visualizador de pedido de origem** para encontrar as diferenças entre ordem de exibição na tela e a ordem da fonte.</span><span class="sxs-lookup"><span data-stu-id="9aa92-247">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="9aa92-248">Depois de habilitar o experimento, certifique-se de reiniciar o DevTools.</span><span class="sxs-lookup"><span data-stu-id="9aa92-248">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="9aa92-249">Para usar o Visualizador de ordem de origem:</span><span class="sxs-lookup"><span data-stu-id="9aa92-249">To use Source Order Viewer:</span></span>  

1.  <span data-ttu-id="9aa92-250">Abrir o painel de **elementos** .</span><span class="sxs-lookup"><span data-stu-id="9aa92-250">Open the **Elements** pane.</span></span>  
1.  <span data-ttu-id="9aa92-251">Abra o painel **acessibilidade** no painel gaveta \ (inferior \).</span><span class="sxs-lookup"><span data-stu-id="9aa92-251">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="9aa92-252">Na seção **Visualizador de ordem de origem** , marque a caixa de seleção **Mostrar ordem de origem** .</span><span class="sxs-lookup"><span data-stu-id="9aa92-252">Under the **Source Order Viewer** section, select the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="9aa92-253">Realce qualquer elemento HTML para exibir uma sobreposição que a ordem na fonte da página.</span><span class="sxs-lookup"><span data-stu-id="9aa92-253">Highlight any HTML element to display an overlay that the order in the page source.</span></span>  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Visualizador de ordem de origem no painel Acessibilidade" lightbox="./media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="9aa92-255">**Visualizador de ordem de origem** no painel **acessibilidade**</span><span class="sxs-lookup"><span data-stu-id="9aa92-255">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## <span data-ttu-id="9aa92-256">Recursos experimentais anteriores</span><span class="sxs-lookup"><span data-stu-id="9aa92-256">Previous experimental features</span></span>  

*   <span data-ttu-id="9aa92-257">o [modo de exibição 3D][Devtools3dViewIndex] agora está disponível e ativado por padrão no Microsoft Edge versão 83 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9aa92-257">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  

## <span data-ttu-id="9aa92-258">Fornecer comentários sobre os recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="9aa92-258">Providing feedback on experimental features</span></span>  

<span data-ttu-id="9aa92-259">Para fornecer comentários sobre o Microsoft Edge DevTools experimentos ou qualquer outro item relacionado ao DevTools.</span><span class="sxs-lookup"><span data-stu-id="9aa92-259">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="9aa92-260">Envie seus comentários usando o ícone **enviar comentários** no devtools</span><span class="sxs-lookup"><span data-stu-id="9aa92-260">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="9aa92-261">Tweet em [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="9aa92-261">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="O ícone enviar comentários no Microsoft Edge DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="9aa92-263">O ícone **enviar comentários** no Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="9aa92-263">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
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
