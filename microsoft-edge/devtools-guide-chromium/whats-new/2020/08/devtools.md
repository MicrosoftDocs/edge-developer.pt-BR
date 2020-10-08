---
description: Corresponder os atalhos de teclado ao código do Visual Studio, emular Surface Duo e Samsung Galaxy fold, melhorias na sobreposição de grade CSS e muito mais.
title: O que há de novo no DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 943eca7e73385513b264feb74ec37c450d5c5a2f
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "11004068"
---
# <span data-ttu-id="a5b3f-104">O que há de novo no DevTools (Microsoft Edge 86)</span><span class="sxs-lookup"><span data-stu-id="a5b3f-104">What's New In DevTools (Microsoft Edge 86)</span></span>  

## <span data-ttu-id="a5b3f-105">Anúncios da equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a5b3f-105">Announcements from the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### <span data-ttu-id="a5b3f-106">Corresponder os atalhos de teclado no DevTools ao código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a5b3f-106">Match keyboard shortcuts in DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="a5b3f-107">No Microsoft Edge 86, você pode corresponder a atalhos de teclado no DevTools para seus atalhos no [código do Visual Studio][VisualStudioCode].</span><span class="sxs-lookup"><span data-stu-id="a5b3f-107">In Microsoft Edge 86, you may match keyboard shortcuts in the DevTools to your shortcuts in [Visual Studio Code][VisualStudioCode].</span></span> 

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   <span data-ttu-id="a5b3f-109">Corresponder os atalhos de teclado no código do DevTools para o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a5b3f-109">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-110">Para ativar esse recurso, navegue até [Personalizar atalhos de teclado no Microsoft Edge devtools][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="a5b3f-110">To activate this feature, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  

<span data-ttu-id="a5b3f-111">Por exemplo, o atalho de teclado para pausar ou continuar a execução de um script no [código do Visual Studio][VisualStudioCodeShortcutsKeyboardWindows] é `F5` .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-111">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="a5b3f-112">Com a predefinição **devtools (padrão)** , o mesmo atalho no devtools é `F8` , mas quando você escolhe a predefinição de **código do Visual Studio** , esse atalho também é `F5` .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-112">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8`, but when you choose the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="a5b3f-113">Chromium problema [#174309][CR174309]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-113">Chromium issue [#174309][CR174309]</span></span>  

### <span data-ttu-id="a5b3f-114">Emular Surface Duo e dobra para Samsung Galaxy</span><span class="sxs-lookup"><span data-stu-id="a5b3f-114">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio":::
   <span data-ttu-id="a5b3f-116">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="a5b3f-116">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-117">Agora você pode testar a aparência do seu site ou aplicativo em dois novos dispositivos:  [Surface Duo][MicrosoftSurfaceDevicesDuo] e [dobra da Samsung Galaxy][SamsungMobileGalaxyFold] no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-117">You are now able to test the look and feel of your website or app on two new devices:  [Surface Duo][MicrosoftSurfaceDevicesDuo] and [Samsung Galaxy Fold][SamsungMobileGalaxyFold] in Microsoft Edge.</span></span>  

<span data-ttu-id="a5b3f-118">Para ajudar a aprimorar seu site ou aplicativo para os dispositivos de tela dupla e dobrável, use os recursos a seguir ao [emular o dispositivo][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="a5b3f-118">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="a5b3f-119">[Distribuição][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], que é quando seu site \ (ou app \) aparece em ambas as telas.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-119">[Spanning][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], which is when your website \(or app\) appears across both screens.</span></span>
*   <span data-ttu-id="a5b3f-120">[Renderizar a fenda][DualScreenIntroductionHowWorkSeam], que é o espaço entre as duas telas.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-120">[Rendering the seam][DualScreenIntroductionHowWorkSeam], which is the space between the two screens.</span></span>
*   <span data-ttu-id="a5b3f-121">[Habilitar APIs experimentais da Web Platform][DevtoolsExperimentalFeaturesEnableExperimentalApis] para acessar o novo [recurso de distribuição de tela de mídia CSS e a API de][DualScreenWebCssMediaSpanning] [getWindowSegments JavaScript][DualScreenWebJavascriptGetwindowsegments].</span><span class="sxs-lookup"><span data-stu-id="a5b3f-121">[Enabling experimental Web Platform APIs][DevtoolsExperimentalFeaturesEnableExperimentalApis] to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [JavaScript getWindowSegments API][DualScreenWebJavascriptGetwindowsegments].</span></span>  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   <span data-ttu-id="a5b3f-123">Emulação de dispositivo para Surface Duo</span><span class="sxs-lookup"><span data-stu-id="a5b3f-123">Device emulation for Surface Duo</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-124">Para ativar esse recurso experimental, navegue até [ativar os recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **emulação: suporte para o modo de tela dupla**.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-124">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Emulation: Support dual screen mode**.</span></span>  

<span data-ttu-id="a5b3f-125">Para obter mais informações sobre esse experimento, navegue até [emulação: suporte para o modo de tela dupla][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].</span><span class="sxs-lookup"><span data-stu-id="a5b3f-125">For more information about this experiment, navigate to [Emulation: Support dual screen mode][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].</span></span>  

<span data-ttu-id="a5b3f-126">Problema do Chromium: [#1054281][CR1054281]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-126">Chromium issue: [#1054281][CR1054281]</span></span>  

### <span data-ttu-id="a5b3f-127">Melhorias na sobreposição de grade CSS e novos recursos de grade experimental</span><span class="sxs-lookup"><span data-stu-id="a5b3f-127">CSS grid overlay improvements and new experimental grid features</span></span>  

<span data-ttu-id="a5b3f-128">Obrigado pelo feedback positivo sobre as sobreposições de grade de CSS aprimoradas.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-128">Thank you for the positive feedback about the improved CSS grid overlays.</span></span>  <span data-ttu-id="a5b3f-129">As sobreposições de grade de CSS agora são habilitadas por padrão e não exigem que você ative um experimento.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-129">The CSS grid overlays are now enabled by default and do not require you to turn on an experiment.</span></span>  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   <span data-ttu-id="a5b3f-131">Sobreposição de grade CSS para o `article` elemento</span><span class="sxs-lookup"><span data-stu-id="a5b3f-131">CSS grid overlay for `article` element</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="a5b3f-132">Para obter mais informações sobre sobreposições de grade, acesse [recursos de depuração de grade CSS][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].</span><span class="sxs-lookup"><span data-stu-id="a5b3f-132">For more information about grid overlays, go to [CSS grid debugging features][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="a5b3f-133">A equipe do Microsoft Edge DevTools e a equipe DevTools do Chrome colaboram com recursos adicionais.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-133">The Microsoft Edge DevTools team and the Chrome DevTools team collaborate on additional features.</span></span>  <span data-ttu-id="a5b3f-134">Os novos recursos incluem várias sobreposições persistentes e configuráveis a partir de um novo painel de **layout** no painel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-134">The new features include multiple overlays that are persistent and configurable from a new **Layout** pane on the **Elements** panel.</span></span>  

<span data-ttu-id="a5b3f-135">Para ativar esse recurso experimental, navegue até [ativar os recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **habilitar novos recursos de depuração de grade CSS (opções de configuração disponíveis no painel da barra lateral layout nos elementos após a reinicialização)**.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-135">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable new CSS Grid debugging features (configuration options available in Layout sidebar pane in Elements after restart)**.</span></span>  

<span data-ttu-id="a5b3f-136">Para obter mais informações sobre esse experimento, navegue para [habilitar os novos recursos de depuração de grade CSS][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].</span><span class="sxs-lookup"><span data-stu-id="a5b3f-136">For more information about this experiment, navigate to [Enable new CSS grid debugging features][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="a5b3f-137">Problema do Chromium: [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-137">Chromium issue: [#1047356][CR1047356]</span></span>  

### <span data-ttu-id="a5b3f-138">A tabela copiada do console preserva a formatação</span><span class="sxs-lookup"><span data-stu-id="a5b3f-138">Table copied from the Console preserves formatting</span></span>  

<span data-ttu-id="a5b3f-139">No Microsoft Edge 85 ou anterior, a formatação de uma cópia `console.table` foi perdida.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-139">In Microsoft Edge 85 or earlier, the formatting of a copied `console.table` was lost.</span></span>  <span data-ttu-id="a5b3f-140">Se você copiou a saída da API do console de [tabela][DevtoolsConsoleApiTable] e a colou, somente o texto da tabela foi mantido.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-140">If you copied the output from the [table][DevtoolsConsoleApiTable] Console API, and pasted it, only the text of the table was kept.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` <span data-ttu-id="a5b3f-142">Saída da API do console no Microsoft Edge 85 ou anterior</span><span class="sxs-lookup"><span data-stu-id="a5b3f-142">Console API output in Microsoft Edge 85 or earlier</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="a5b3f-144">Saída da API do console do Microsoft Edge 85 ou anterior colada no código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a5b3f-144">Console API output from Microsoft Edge 85 or earlier pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="a5b3f-145">No Microsoft Edge 86 ou posterior, quando você copia uma tabela do **console**, a formatação agora é preservada.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-145">In Microsoft Edge 86 or later, when you copy a table from the **Console**, the formatting is now preserved.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` <span data-ttu-id="a5b3f-147">Saída da API do console no Microsoft Edge 86 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a5b3f-147">Console API output in Microsoft Edge 86 or later</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="a5b3f-149">Saída da API do console do Microsoft Edge 86 ou posterior colada no código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a5b3f-149">Console API output from Microsoft Edge 86 or later pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="a5b3f-150">Problema do Chromium: [#1115011] [CR1115011]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-150">Chromium issue: [#1115011][CR1115011]</span></span>  

### <span data-ttu-id="a5b3f-151">Visualizador de pedido de origem para facilitar o teste de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="a5b3f-151">Source Order Viewer for easier accessibility testing</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio":::
   <span data-ttu-id="a5b3f-153">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="a5b3f-153">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-154">O novo auxiliar de acessibilidade exibe a ordem dos elementos na fonte.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-154">The new accessibility helper displays the order of elements in the source.</span></span>  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   <span data-ttu-id="a5b3f-156">Ativar **Mostrar ordem de origem**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-156">Activate **Show source order**</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-157">Esse recurso torna mais fácil testar a maneira como o leitor de tela e os usuários de teclado experimentam seu site ou aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-157">This feature makes it easier to test the way screen reader and keyboard users experience your website or app.</span></span>  <span data-ttu-id="a5b3f-158">Os leitores de tela e a navegação de teclado dependem do conteúdo sendo colocado em uma ordem específica no código-fonte do seu site ou aplicativo, para que ele corresponda à página renderizada.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-158">Screen readers and keyboard navigation depend on content being placed in a particular order in the source code of your website or app, so that it matches the rendered page.</span></span>  <span data-ttu-id="a5b3f-159">O Visualizador de ordem de origem exibe possíveis diferenças em ordem entre a página renderizada e o código-fonte.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-159">The Source Order Viewer displays potential differences in order between the rendered page and the source code.</span></span>  

<span data-ttu-id="a5b3f-160">Para ativar esse recurso experimental, navegue até [ativar os recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **habilitar Visualizador de ordem de origem**.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-160">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Source Order Viewer**.</span></span>  

<span data-ttu-id="a5b3f-161">Para obter mais informações sobre esse experimento, navegue até [habilitar o Visualizador de ordem de origem][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].</span><span class="sxs-lookup"><span data-stu-id="a5b3f-161">For more information about this experiment, navigate to [Enable Source Order Viewer][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].</span></span>  

<span data-ttu-id="a5b3f-162">Problema do Chromium: [#1094406][CR1094406]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-162">Chromium issue: [#1094406][CR1094406]</span></span>  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### <span data-ttu-id="a5b3f-163">Ferramenta realçar todos os resultados da pesquisa na ferramenta elementos</span><span class="sxs-lookup"><span data-stu-id="a5b3f-163">Highlight all search results in Elements tool</span></span>  

<span data-ttu-id="a5b3f-164">No Microsoft Edge 84 e no 85, o primeiro resultado da pesquisa no painel **elementos** não realce.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-164">In Microsoft Edge 84 and 85, the first search result in the **Elements** panel did not highlight.</span></span>  <span data-ttu-id="a5b3f-165">Os resultados da pesquisa restantes foram realçados corretamente.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-165">The remaining search results were highlighted correctly.</span></span>  

<span data-ttu-id="a5b3f-166">Obrigado por enviar seus comentários e ajudar a melhorar o Chromium.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-166">Thank you for sending your feedback and helping improve Chromium.</span></span>  <span data-ttu-id="a5b3f-167">Seu comentário sobre o problema não coberto [#1103316][CR1103316] no projeto Chromium de código-fonte aberto.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-167">Your feedback uncovered Issue [#1103316][CR1103316] in the open-source Chromium project.</span></span>  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   <span data-ttu-id="a5b3f-169">Primeiro resultado da pesquisa realçada no painel de **elementos** no Microsoft Edge 84 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a5b3f-169">Highlighted first search result on **Elements** panel in Microsoft Edge 84 or later</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-170">O problema agora está corrigido em todas as versões do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-170">The issue is now fixed in all versions of Microsoft Edge.</span></span>  

<span data-ttu-id="a5b3f-171">Problema do Chromium: [#1103316][CR1103316]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-171">Chromium issue: [#1103316][CR1103316]</span></span>  

## <span data-ttu-id="a5b3f-172">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="a5b3f-172">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="a5b3f-173">Novo painel de mídia</span><span class="sxs-lookup"><span data-stu-id="a5b3f-173">New Media panel</span></span>  

<span data-ttu-id="a5b3f-174">O DevTools agora exibe as informações do media players no painel [mídia][DevtoolsMediaIndex] .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-174">DevTools now displays media players information in the [Media][DevtoolsMediaIndex] panel.</span></span>  

<span data-ttu-id="a5b3f-175">Para abrir o novo painel **mídia** , conclua a etapa a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-175">To open the new **Media** panel, complete the following step.</span></span>  

1.  <span data-ttu-id="a5b3f-176">Escolha **Personalizar e controle devtools** \ ( `...` \) > **mais ferramentas**de  >  **mídia**.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-176">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/media-panel.msft.png":::
       <span data-ttu-id="a5b3f-178">Novo painel de **mídia**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-178">New **Media** panel</span></span>  
    :::image-end:::  

<span data-ttu-id="a5b3f-179">Antes do novo painel de **mídia** no devtools, as informações de log e depuração sobre players de vídeo estavam localizadas na configuração **jogadores recentes** .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-179">Before the new **Media** panel in DevTools, the logging and debug information about video players was located under the **Recent Players** setting.</span></span>  <span data-ttu-id="a5b3f-180">Para abrir a configuração do **reprodutor recentes** , vá para `edge://media-internals` e escolha a guia **players** .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-180">To open the **Recent Players** setting, go to `edge://media-internals` and choose the **Players** tab.</span></span>  

<span data-ttu-id="a5b3f-181">Exiba conteúdo ao vivo e inspecione possíveis problemas mais rapidamente, incluindo os exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-181">View live content and inspect potential issues more quickly, including the following examples.</span></span>  

*   <span data-ttu-id="a5b3f-182">Por que os quadros são soltos?</span><span class="sxs-lookup"><span data-stu-id="a5b3f-182">Why frames are dropped?</span></span>  
*   <span data-ttu-id="a5b3f-183">Por que o JavaScript está interagindo com o jogador de forma inesperada?</span><span class="sxs-lookup"><span data-stu-id="a5b3f-183">Why JavaScript is interacting with the player in an unexpected way?</span></span>  

### <span data-ttu-id="a5b3f-184">Capturar capturas de tela do nó usando o menu de contexto do painel elementos</span><span class="sxs-lookup"><span data-stu-id="a5b3f-184">Capture node screenshots using the Elements panel context menu</span></span>  

<span data-ttu-id="a5b3f-185">Agora você pode capturar capturas de tela do nó usando o menu de contexto no painel de **elementos** .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-185">You may now capture node screenshots using the context menu in the **Elements** panel.</span></span>  

<span data-ttu-id="a5b3f-186">Por exemplo, para fazer uma captura de tela do Sumário, passe o mouse sobre o elemento, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **capturar captura de tela do nó**.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-186">For example, to take a screenshot of the table of contents, hover on the element, open the contextual menu \(right-click\), and select **Capture node screenshot**.</span></span>  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   <span data-ttu-id="a5b3f-188">Capturar capturas de tela do nó</span><span class="sxs-lookup"><span data-stu-id="a5b3f-188">Capture node screenshots</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-189">Problema do Chromium: [#1100253][CR1100253]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-189">Chromium issue: [#1100253][CR1100253]</span></span>  

### <span data-ttu-id="a5b3f-190">Problemas de atualizações da ferramenta</span><span class="sxs-lookup"><span data-stu-id="a5b3f-190">Issues tool updates</span></span>  

<span data-ttu-id="a5b3f-191">A barra de aviso de problemas no painel do **console** agora é substituída por uma mensagem normal.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-191">The Issues warning bar on the **Console** panel is now replaced with a regular message.</span></span>  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   <span data-ttu-id="a5b3f-193">Problemas na mensagem do console</span><span class="sxs-lookup"><span data-stu-id="a5b3f-193">Issues in console message</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-194">Problemas com cookies de terceiros agora estão ocultos por padrão na ferramenta **problemas** .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-194">Third-party cookie issues are now hidden by default in the **Issues** tool.</span></span>  <span data-ttu-id="a5b3f-195">Habilite a caixa de seleção **incluir problemas de cookies** de terceiros para exibir os problemas.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-195">Enable the new **Include third-party cookie issues** checkbox to view the issues.</span></span>  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   <span data-ttu-id="a5b3f-197">caixa de seleção problemas com cookies de terceiros</span><span class="sxs-lookup"><span data-stu-id="a5b3f-197">third-party cookie issues checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-198">Problemas do Chromium: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-198">Chromium issues: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span></span>  

### <span data-ttu-id="a5b3f-199">Emular fontes locais ausentes</span><span class="sxs-lookup"><span data-stu-id="a5b3f-199">Emulate missing local fonts</span></span>  

<span data-ttu-id="a5b3f-200">Abra a [ferramenta de renderização][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] e use o novo recurso **desabilitar fontes locais** para emular `local()` fontes ausentes nas `@font-face` regras.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-200">Open the [Rendering tool][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] and use the new **Disable local fonts** feature to emulate missing `local()` sources in `@font-face` rules.</span></span>  

<span data-ttu-id="a5b3f-201">Por exemplo, quando a `Rubik` fonte é instalada em seu dispositivo e a `@font-face src` regra a usa como `local()` fonte, o Microsoft Edge usa o arquivo de fonte local do seu dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-201">For example, when the `Rubik` font is installed on your device and the `@font-face src` rule uses it as a `local()` font, Microsoft Edge uses the local font file from your device.</span></span>  

<span data-ttu-id="a5b3f-202">Quando **desativar fontes locais** estiver habilitado, o devtools ignorará as `local()` fontes e buscará cada uma da rede.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-202">When **Disable local fonts** is enabled, DevTools ignores the `local()` fonts and fetches each from the network.</span></span>  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/disable-font.msft.png":::
   <span data-ttu-id="a5b3f-204">Emular fontes locais ausentes</span><span class="sxs-lookup"><span data-stu-id="a5b3f-204">Emulate missing local fonts</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-205">Se você usar duas cópias diferentes da mesma fonte durante o desenvolvimento, como os exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-205">If you use two different copies of the same font during development, such as the following examples.</span></span>  

*   <span data-ttu-id="a5b3f-206">Uma fonte local para suas ferramentas de design.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-206">A local font for your design tools.</span></span>  
*   <span data-ttu-id="a5b3f-207">Uma fonte da Web para seu código.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-207">A web font for your code.</span></span>  

<span data-ttu-id="a5b3f-208">Use **desabilitar fontes locais** para facilitar a realização das tarefas a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-208">Use **Disable local fonts** to make it easier for you to complete the following tasks.</span></span>  

*   <span data-ttu-id="a5b3f-209">Depuração e medição do desempenho e da otimização do carregamento de fontes da Web.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-209">Debug and measure loading performance and optimization of web fonts.</span></span>  
*   <span data-ttu-id="a5b3f-210">Verifique a precisão das suas `@font-face` regras CSS.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-210">Verify accuracy of your CSS `@font-face` rules.</span></span>  
*   <span data-ttu-id="a5b3f-211">Descubra as diferenças entre as versões locais instaladas em seu dispositivo e uma fonte da Web.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-211">Discover differences between local versions installed on your device and a web font.</span></span>  

<span data-ttu-id="a5b3f-212">Problema do Chromium: [#384968][CR384968]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-212">Chromium issue: [#384968][CR384968]</span></span>  

### <span data-ttu-id="a5b3f-213">Emular usuários inativos</span><span class="sxs-lookup"><span data-stu-id="a5b3f-213">Emulate inactive users</span></span>  

<span data-ttu-id="a5b3f-214">A [API de detecção ociosa][WebDevIdleDetection] permite que os desenvolvedores detectem usuários inativos e reajam a alterações de estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-214">The [Idle Detection API][WebDevIdleDetection] allows developers to detect inactive users and react on idle state changes.</span></span>  <span data-ttu-id="a5b3f-215">Agora você pode usar DevTools para emular alterações de estado ocioso na ferramenta **sensores** para o estado do usuário e o estado da tela em vez de aguardar o estado real de ociosidade mudar.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-215">You are now able to use DevTools to emulate idle state changes in the **Sensors** tool for both the user state and the screen state instead of waiting for the actual idle state to change.</span></span>  <span data-ttu-id="a5b3f-216">Você pode abrir a ferramenta de **sensores** da [gaveta][DevtoolsCustomizeIndexDrawer].</span><span class="sxs-lookup"><span data-stu-id="a5b3f-216">You may open the **Sensors** tool from the [Drawer][DevtoolsCustomizeIndexDrawer].</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   <span data-ttu-id="a5b3f-218">Emular usuários inativos</span><span class="sxs-lookup"><span data-stu-id="a5b3f-218">Emulate inactive users</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-219">Problema do Chromium: [#1090802][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-219">Chromium issue: [#1090802][CR1090802]</span></span>  

### <span data-ttu-id="a5b3f-220">Emular preferência-dados reduzidos</span><span class="sxs-lookup"><span data-stu-id="a5b3f-220">Emulate prefers-reduced-data</span></span>  

> [!NOTE]
> <span data-ttu-id="a5b3f-221">No Microsoft Edge 86, para habilitar esse recurso, vá para `edge://flags#enable-experimental-web-platform-features` e ative o sinalizador de **recursos da plataforma da Web experimental** .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-221">In Microsoft Edge 86, to enable this feature, go to `edge://flags#enable-experimental-web-platform-features` and turn on the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="a5b3f-222">A opção emulação só será exibida se o sinalizador estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-222">The emulation option is only displayed if the flag is enabled.</span></span>  

<span data-ttu-id="a5b3f-223">A consulta [preferencial – mídia de dados reduzida][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] detecta as preferências de conteúdo do usuário para reduzir os dados.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-223">The [prefers-reduced-data][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] media query detects user content preferences for reduced data.</span></span>  <span data-ttu-id="a5b3f-224">Se selecionado, o usuário receberá um conteúdo de página alternativo que usa menos dados.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-224">If selected, the user receives alternate page content that uses less data.</span></span>  

<span data-ttu-id="a5b3f-225">Agora você pode usar o DevTools para emular a `prefers-reduced-data` consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-225">You may now use DevTools to emulate the `prefers-reduced-data` media query.</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   <span data-ttu-id="a5b3f-227">Emular preferência-dados reduzidos</span><span class="sxs-lookup"><span data-stu-id="a5b3f-227">Emulate prefers-reduced-data</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-228">Problema do Chromium: [#1096068][CR1096068]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-228">Chromium issue: [#1096068][CR1096068]</span></span>  

### <span data-ttu-id="a5b3f-229">Suporte para novos recursos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="a5b3f-229">Support for new JavaScript features</span></span>  

<span data-ttu-id="a5b3f-230">O DevTools agora tem o melhor suporte dos recursos da linguagem JavaScript a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-230">DevTools now have better supported the following JavaScript language features.</span></span>  

| <span data-ttu-id="a5b3f-231">Recurso de linguagem JavaScript</span><span class="sxs-lookup"><span data-stu-id="a5b3f-231">JavaScript language feature</span></span> | <span data-ttu-id="a5b3f-232">Detalhes</span><span class="sxs-lookup"><span data-stu-id="a5b3f-232">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="a5b3f-233">Operadores lógicos de atribuição</span><span class="sxs-lookup"><span data-stu-id="a5b3f-233">Logical assignment operators</span></span>][V8FeaturesLogicalAssignment] | <span data-ttu-id="a5b3f-234">O DevTools agora oferece suporte à atribuição lógica com os novos `&&=` `||=` operadores e `??=` operadores nos painéis **console** e **fontes** .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-234">DevTools now supports logical assignment with the new `&&=`, `||=`, and `??=` operators in the **Console** and **Sources** panels.</span></span>  |  
| <span data-ttu-id="a5b3f-235">[Separadores numéricos][V8FeaturesNumericSeparators] de impressão bonita</span><span class="sxs-lookup"><span data-stu-id="a5b3f-235">Pretty-print [numeric separators][V8FeaturesNumericSeparators]</span></span> | <span data-ttu-id="a5b3f-236">Agora, o DevTools agora realmente imprime os separadores numéricos no painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-236">DevTools now properly pretty-prints the numeric separators in the **Sources** panel.</span></span>  |  

<span data-ttu-id="a5b3f-237">Problemas do Chromium: [1086817][CR1086817], [1080569][CR1080569]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-237">Chromium issues: [1086817][CR1086817], [1080569][CR1080569]</span></span>  

### <span data-ttu-id="a5b3f-238">Lighthouse 6,2 no painel Lighthouse</span><span class="sxs-lookup"><span data-stu-id="a5b3f-238">Lighthouse 6.2 in the Lighthouse panel</span></span>  

<span data-ttu-id="a5b3f-239">O painel **Lighthouse** agora está em execução Lighthouse 6,2.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-239">The **Lighthouse** panel is now running Lighthouse 6.2.</span></span>  <span data-ttu-id="a5b3f-240">Para obter uma lista completa de alterações, acesse as [notas de versão do Lighthouse][GithubGooglechromeLighthouseV620].</span><span class="sxs-lookup"><span data-stu-id="a5b3f-240">For a full list of changes, go to the [Lighthouse release notes][GithubGooglechromeLighthouseV620].</span></span>  

<span data-ttu-id="a5b3f-241">Problema do Chromium: [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-241">Chromium issue: [#772558][CR772558]</span></span>  

### <span data-ttu-id="a5b3f-242">Substituição de outras origens listadas no painel de trabalhadores do serviço</span><span class="sxs-lookup"><span data-stu-id="a5b3f-242">Deprecation of other origins listing in the Service Workers pane</span></span>  

<span data-ttu-id="a5b3f-243">O DevTools agora fornece um link do painel **funcionários do serviço** \ (painel do**aplicativo** > painel de trabalho do **serviço** \) para exibir a lista completa de trabalhadores de serviço de outras origens.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-243">DevTools now provides a link from the **Service workers** pane \(**Application** panel > **Service workers** pane\) to view the full list of service workers from other origins.</span></span>  <span data-ttu-id="a5b3f-244">Para acessar a lista sem abrir o DevTools, vá para `edge://service-worker-internals/?devtools` .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-244">To access the list without opening the DevTools, go to `edge://service-worker-internals/?devtools`.</span></span>  

<span data-ttu-id="a5b3f-245">DevTools anteriormente exibir uma lista aninhada sob o painel do **aplicativo** > painel de **trabalhadores do serviço** .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-245">Previously DevTools displayed a list nested under the **Application** panel > **Service workers** pane.</span></span>  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   <span data-ttu-id="a5b3f-247">Link para outras origens</span><span class="sxs-lookup"><span data-stu-id="a5b3f-247">Link to other origins</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-248">Problema do Chromium: [#807440][CR807440]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-248">Chromium issue: [#807440][CR807440]</span></span>  

### <span data-ttu-id="a5b3f-249">Mostrar Resumo da cobertura para itens filtrados</span><span class="sxs-lookup"><span data-stu-id="a5b3f-249">Show coverage summary for filtered items</span></span>  

<span data-ttu-id="a5b3f-250">O DevTools agora recalcula e exibe um resumo das informações de cobertura dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-250">DevTools now recalculate and display a summary of coverage information dynamically.</span></span>  <span data-ttu-id="a5b3f-251">A exibição dinâmica é disparada quando os filtros são aplicados na ferramenta [cobertura][DevtoolsCoverageIndex] .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-251">The dynamic display is triggered when filters are applied in the [Coverage][DevtoolsCoverageIndex] tool.</span></span>  <span data-ttu-id="a5b3f-252">Antes que a ferramenta **cobertura** sempre tenha exibido um resumo de todas as informações de cobertura.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-252">Before the **Coverage** tool always displayed a summary of all coverage information.</span></span>  

<span data-ttu-id="a5b3f-253">No primeiro dos números a seguir, o resumo é exibido inicialmente `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` e, na segunda das figuras abaixo, o resumo é exibido `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` após a aplicação da filtragem CSS.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-253">In the first of the following figures, the summary initially displays `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` and in the second of the following figures, the summary displays `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` after CSS filtering is applied.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         <span data-ttu-id="a5b3f-255">Resumo da cobertura</span><span class="sxs-lookup"><span data-stu-id="a5b3f-255">Coverage summary</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         <span data-ttu-id="a5b3f-257">Resumo da cobertura para itens filtrados</span><span class="sxs-lookup"><span data-stu-id="a5b3f-257">Coverage summary for filtered items</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="a5b3f-258">Problema do Chromium: [#1061385][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-258">Chromium issue: [#1061385][CR1090802]</span></span>  

### <span data-ttu-id="a5b3f-259">Novo modo de exibição de detalhes do quadro no painel do aplicativo</span><span class="sxs-lookup"><span data-stu-id="a5b3f-259">New frame details view in Application panel</span></span>  

<span data-ttu-id="a5b3f-260">O DevTools agora mostra um modo de exibição detalhado para cada quadro.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-260">DevTools now show a detailed view for each frame.</span></span>  <span data-ttu-id="a5b3f-261">Para acessá-lo, escolha um quadro no menu **quadros** no painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-261">To access it, choose a frame under the **Frames** menu in the **Application** panel.</span></span>  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/frame-details.msft.png":::
   <span data-ttu-id="a5b3f-263">Novo modo de exibição detalhado para um quadro no painel de **aplicativos**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-263">New detailed view for a frame in **Application** panel</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-264">Problema do Chromium: [#1093247][CR1093247]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-264">Chromium issue: [#1093247][CR1093247]</span></span>  

#### <span data-ttu-id="a5b3f-265">Detalhes do quadro para janelas abertas</span><span class="sxs-lookup"><span data-stu-id="a5b3f-265">Frame details for opened windows</span></span>  

<span data-ttu-id="a5b3f-266">Abrir janelas e janelas pop-up agora são exibidos na árvore de quadros também.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-266">Open windows and pop-up windows now display under the frame tree as well.</span></span>  <span data-ttu-id="a5b3f-267">O modo de exibição detalhado do Windows aberto inclui informações de segurança adicionais.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-267">The detailed view of the opened windows includes additional security information.</span></span>  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/window-opener.msft.png":::
   <span data-ttu-id="a5b3f-269">Modo de exibição detalhado de novo quadro para janelas abertas</span><span class="sxs-lookup"><span data-stu-id="a5b3f-269">New frame detailed view for opened windows</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-270">Problema do Chromium: [#1107766] [CR1107766]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-270">Chromium issue: [#1107766][CR1107766]</span></span>  

#### <span data-ttu-id="a5b3f-271">Informações de segurança e isolamento</span><span class="sxs-lookup"><span data-stu-id="a5b3f-271">Security and isolation information</span></span>  

<span data-ttu-id="a5b3f-272">Contexto seguro, [Cross-Origin-incorporáer-Policy (COEP)][WebDevCoopCoep]e [Cross-Origin-Opener-Policy (Coop)][WebDevCoopCoep] agora são exibidos nos detalhes do quadro.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-272">Secure context, [Cross-Origin-Embedder-Policy (COEP)][WebDevCoopCoep], and [Cross-Origin-Opener-Policy (COOP)][WebDevCoopCoep] are now displayed in the frame details.</span></span>  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/coep-coop.msft.png":::
   <span data-ttu-id="a5b3f-274">Informações de segurança e isolamento</span><span class="sxs-lookup"><span data-stu-id="a5b3f-274">Security and isolation information</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-275">No futuro, a equipe do Microsoft Edge DevTools e a equipe DevTools do Chrome estão planejando adicionar mais informações de segurança aos detalhes do quadro.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-275">In the future, the Microsoft Edge DevTools team and the Chrome DevTools team are planning to add more security information to the frame details.</span></span>  

<span data-ttu-id="a5b3f-276">Problema do Chromium: [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-276">Chromium issue: [#1051466][CR1051466]</span></span>  

### <span data-ttu-id="a5b3f-277">Atualizações de elementos e painel de rede</span><span class="sxs-lookup"><span data-stu-id="a5b3f-277">Elements and Network panel updates</span></span>  

#### <span data-ttu-id="a5b3f-278">Sugestão de cor acessível no painel estilos</span><span class="sxs-lookup"><span data-stu-id="a5b3f-278">Accessible color suggestion in the Styles pane</span></span>  

<span data-ttu-id="a5b3f-279">O DevTools agora fornece sugestões de cor para texto de contraste de cor baixa.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-279">DevTools now provides color suggestions for low color contrast text.</span></span>  

<span data-ttu-id="a5b3f-280">No exemplo abaixo, `h1` há texto de baixo contraste.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-280">In the example below, `h1` has low contrast text.</span></span>  <span data-ttu-id="a5b3f-281">Para corrigi-lo, abra o seletor de cores da `color` propriedade no painel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-281">To fix it, open the color picker of the `color` property in the **Styles** pane.</span></span>  <span data-ttu-id="a5b3f-282">Após expandir a seção de **taxa de contraste** , o devtools fornece sugestões de cores AA e AAA.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-282">After you expand the **Contrast ratio** section, DevTools provides AA and AAA color suggestions.</span></span>  <span data-ttu-id="a5b3f-283">Selecione a cor sugerida para aplicar a cor.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-283">Select the suggested color to apply the color.</span></span>  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   <span data-ttu-id="a5b3f-285">O seletor de cores sugere sugestões de cores AA e AAA</span><span class="sxs-lookup"><span data-stu-id="a5b3f-285">Color picker suggests AA and AAA color suggestions</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-286">Problema do Chromium: [#1093227][CR1093227]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-286">Chromium issue: [#1093227][CR1093227]</span></span>  

#### <span data-ttu-id="a5b3f-287">Reaplicar painel Propriedades no painel elementos</span><span class="sxs-lookup"><span data-stu-id="a5b3f-287">Reinstate Properties pane in the Elements panel</span></span>  

<span data-ttu-id="a5b3f-288">O painel **Propriedades** está de volta.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-288">The **Properties** pane is back.</span></span>  <span data-ttu-id="a5b3f-289">Ele foi [preterido no Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span><span class="sxs-lookup"><span data-stu-id="a5b3f-289">It was [deprecated in Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span></span>  <span data-ttu-id="a5b3f-290">A equipe do Microsoft Edge DevTools e a equipe DevTools do Chrome são melhorias de planejamento para inspecionar Propriedades de elementos.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-290">The Microsoft Edge DevTools team and the Chrome DevTools team are planning improvements for inspecting properties of elements.</span></span>  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/properties-pane.msft.png":::
   <span data-ttu-id="a5b3f-292">Painel **Propriedades** no painel **elementos**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-292">**Properties** pane in the **Elements** panel</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-293">Problema do Chromium:</span><span class="sxs-lookup"><span data-stu-id="a5b3f-293">Chromium issue:</span></span>  <!--  [#1105205][CR1105205],  -->  <span data-ttu-id="a5b3f-294">[#1116085] [CR1116085]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-294">[#1116085][CR1116085]</span></span>  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### <span data-ttu-id="a5b3f-295">Preenchimento automático de fontes personalizadas no painel estilos</span><span class="sxs-lookup"><span data-stu-id="a5b3f-295">Autocomplete custom fonts in the Styles pane</span></span>  

<span data-ttu-id="a5b3f-296">As faces de fonte importadas agora são adicionadas à lista de preenchimento automático de CSS ao editar a `font-family` propriedade no painel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-296">Imported font faces are now added to the list of CSS autocompletion when editing the `font-family` property in the **Styles** pane.</span></span>  

<span data-ttu-id="a5b3f-297">Por exemplo, se `monospace` for uma fonte personalizada instalada no computador local, ela será exibida na lista de conclusão da CSS.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-297">For example, if `monospace` is a custom font installed on the local machine, it's displayed in the CSS completion list.</span></span> <span data-ttu-id="a5b3f-298">Em versões anteriores do Microsoft Edge, a fonte não era exibida.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-298">In previous versions of Microsoft Edge, the font wasn't displayed.</span></span>

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   <span data-ttu-id="a5b3f-300">Autopreencher fontes personalizadas</span><span class="sxs-lookup"><span data-stu-id="a5b3f-300">Autocomplete custom fonts</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-301">Problema do Chromium: [#1106221] [CR1106221]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-301">Chromium issue: [#1106221][CR1106221]</span></span>  

#### <span data-ttu-id="a5b3f-302">Exibir consistentemente o tipo de recurso no painel de rede</span><span class="sxs-lookup"><span data-stu-id="a5b3f-302">Consistently display resource type in Network panel</span></span>  

<span data-ttu-id="a5b3f-303">O DevTools agora exibe o mesmo tipo de recurso que a solicitação de rede original e acrescenta `/ Redirect` ao valor de coluna de **tipo** quando o redirecionamento \ (código de status HTTP 302 \) acontece.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-303">DevTools now consistently display the same resource type as the original network request and appends `/ Redirect` to the **Type** column value when redirection \(HTTP status code 302\) happens.</span></span>  

<span data-ttu-id="a5b3f-304">Anteriormente, DevTools alterou o tipo para `Other` às vezes.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-304">Previously DevTools changed the type to `Other` sometimes.</span></span>  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/network-redirect.msft.png":::
   <span data-ttu-id="a5b3f-306">Exibir tipo de recurso de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="a5b3f-306">Display redirect resource type</span></span>  
:::image-end:::  

<span data-ttu-id="a5b3f-307">Problema do Chromium: [#997694][CR997694]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-307">Chromium issue: [#997694][CR997694]</span></span>  

#### <span data-ttu-id="a5b3f-308">Limpar botões nos painéis de elementos e de rede</span><span class="sxs-lookup"><span data-stu-id="a5b3f-308">Clear buttons in the Elements and Network panels</span></span>  

<span data-ttu-id="a5b3f-309">As seguintes caixas de texto agora têm botões **claros** .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-309">The following text boxes now have **Clear** buttons.</span></span>  

*   <span data-ttu-id="a5b3f-310">As caixas de texto filtro no painel **estilos** e painel de **rede** .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-310">The filter text boxes in the **Styles** pane and **Network** panel.</span></span>  
*   <span data-ttu-id="a5b3f-311">A caixa de texto de pesquisa DOM no painel de **elementos** .</span><span class="sxs-lookup"><span data-stu-id="a5b3f-311">The DOM search text box in the **Elements** panel.</span></span>  

<span data-ttu-id="a5b3f-312">Escolha o botão **limpar** para remover qualquer texto reemitido.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-312">Choose the **Clear** button to remove any inputted text.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         <span data-ttu-id="a5b3f-314">Botões limpar nos painéis de **elementos**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-314">Clear buttons in the **Elements** panels</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Corresponder os atalhos de teclado no código do DevTools para o Visual Studio" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         <span data-ttu-id="a5b3f-316">Limpar botões nos painéis de **rede**</span><span class="sxs-lookup"><span data-stu-id="a5b3f-316">Clear buttons in the  **Network** panels</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="a5b3f-317">Problema do Chromium: [#1067184][CR1067184]</span><span class="sxs-lookup"><span data-stu-id="a5b3f-317">Chromium issue: [#1067184][CR1067184]</span></span>  

## <span data-ttu-id="a5b3f-318">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a5b3f-318">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="a5b3f-319">Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-319">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="a5b3f-320">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-320">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="a5b3f-321">Como entrar em contato com o Microsoft Edge DevTools equipe</span><span class="sxs-lookup"><span data-stu-id="a5b3f-321">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Ícone de configurações do DevTools"  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Substituição do painel Propriedades no painel elementos – novidades do DevTools (Microsoft Edge 84) | Documentos da Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Recursos de depuração de grade CSS-novidades do DevTools (Microsoft Edge 85) | Documentos da Microsoft"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móveis no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalizar atalhos de teclado no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Habilitar APIs experimentais-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulação: suporta o modo de tela dupla-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Habilitar o Visualizador de ordem de origem-recursos experimentais | Documentos da Microsoft"
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: https://review.docs.microsoft.com/microsoft-edge/devtools-guide-chromium/experimental-features?branch=user/zoghadya/dual-screen-experiment#emulation-support-dual-screen-mode "Emulação: suporta o modo de tela dupla-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Testes em dispositivos dobrável e de tela dupla-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Ativar recursos experimentais-recursos experimentais | Documentos da Microsoft"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "tabela-referência da API do console | Documentos da Microsoft"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Localizar código JavaScript e CSS não usados com a guia cobertura no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Gaveta-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analisar o desempenho de renderização com a guia renderização-referência de análise de desempenho | Documentos da Microsoft"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Exibir e depurar informações do media players | Documentos da Microsoft"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Como trabalhar com a fenda-introdução a dispositivos de tela dupla | Documentos da Microsoft"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Tela de mídia CSS – recurso de abrangência para detecção de tela dupla | Documentos da Microsoft"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "A API JavaScript getWindowSegments para dispositivos de tela dupla | Documentos da Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de visualização do Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Código do Visual Studio "  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Atalhos de teclado de código do Visual Studio para Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "O novo Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools conta do Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros de Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: permite personalizar atalhos de teclado/associações de teclas | Erros de Chromium"
[CR384968]: https://crbug.com/384968 "Opção para ignorar fontes locais () | Erros de Chromium"  
[CR772558]: https://crbug.com/772558 "DevTools: Atualize para a versão mais recente do Lighthouse | Erros de Chromium"  
[CR807440]: https://crbug.com/807440 "O Chrome trava com um grande número de SWs | Erros de Chromium"  
[CR997694]: https://crbug.com/997694 "As solicitações XHR com o status do 302 não são mostradas no filtro \ "XHR \" no painel de rede | Erros de Chromium"  
[CR1047356]: https://crbug.com/1047356 "Ferramentas de grade/flexbox/tabela CSS"  
[CR1051466]: https://crbug.com/1051466 "Suporta a depuração COOP/COEP no DevTools | Erros de Chromium"  
[CR1054281]: https://crbug.com/1054281 "Solicitação de recurso: o DevTools deve emular dobrável e dispositivos de tela dupla | Erros de Chromium"  
[CR1067184]: https://crbug.com/1067184 "Solicitação de recurso: botão Limpar filtro em elementos de & de rede-> entradas de filtro de estilo | Erros de Chromium"  
[CR1068116]: https://crbug.com/1068116 "Painel de problemas de envio de ☂ | Erros de Chromium"  
[CR1080569]: https://crbug.com/1080569 "o Acorn não dá suporte a operadores de atribuição lógica | Erros de Chromium"  
[CR1080589]: https://crbug.com/1080589 "Classificar problemas por terceiros/de terceiros | Erros de Chromium"  
[CR1086817]: https://crbug.com/1086817 "Acorn não dá suporte a separadores numéricos | Erros de Chromium"  
[CR1090802]: https://crbug.com/1090802 "Simular alterações de estado ocioso da API de detecção ociosa | Erros de Chromium"  
[CR1093227]: https://crbug.com/1093227 "DevTools: sugerir cor acessível mais próxima | Erros de Chromium"  
[CR1093247]: https://crbug.com/1093247 "Exibir informações sobre quadros no painel de aplicativos | Erros de Chromium"  
[CR1094406]: https://crbug.com/1094406 "Os desenvolvedores querem um visualizador de pedido de origem por AT https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: suporte à emulação do recurso de mídia de dados de preferência-reduzido | Erros de Chromium"  
[CR1096481]: https://crbug.com/1096481 "Posicionamento da faixa de problemas | Erros de Chromium"  
[CR1100253]: https://crbug.com/1100253 "Adicionar atalho do nó de captura de tela no menu de contexto de elemento | Erros de Chromium"  
[CR1103316]: https://crbug.com/1103316 "A pesquisa de elementos não resolveNode (realçar texto, etc.) no primeiro resultado da pesquisa | Erros de Chromium"  
[CR1103854]: https://crbug.com/1103854 "Do-ofuscador X – cliente-valores de dados nas ferramentas de desenvolvedor | Erros de Chromium"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: https://crbug.com/1106221 "adicionar fontes importadas à AutoPreenchimento da família de fontes no painel estilos | Erros de Chromium "  
[CR1107766]: https://crbug.com/1107766 "exibir informações sobre quadros gerados por ' Window. Open () ' na árvore de quadros | Erros de Chromium "  
[CR1115011]: https://crbug.com/1115011 "ao copiar uma tabela do console, a estrutura da tabela não é preservada | Erros de Chromium "  
[CR1116085]: https://crbug.com/1116085 "retorne o Inspetor de propriedades do devtools | Erros de Chromium "  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "preferíveis-reduzido-dados-consultas de mídia nível 5 | Rascunhos do editor de grupo de trabalho W3C CSS"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v 6.2.0-GoogleChrome/Lighthouse | GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Buffers de protocolo | Desenvolvedores do Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy dobre | Samsung US"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Atribuição lógica | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Separadores numéricos | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Como criar seu site \ "entre origens isoladas \" usando COOP e COEP | Web. dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Detectar usuários inativos com a API de detecção de ociosidade | Web. dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Evitar animações não compostas | Web. dev"  

> [!NOTE]
> <span data-ttu-id="a5b3f-382">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="a5b3f-382">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a5b3f-383">A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/08/devtools/index) e é criada por [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="a5b3f-383">The original page is found [here](https://developers.google.com/web/updates/2020/08/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a5b3f-385">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a5b3f-385">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
