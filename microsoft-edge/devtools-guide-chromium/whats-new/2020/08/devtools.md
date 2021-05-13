---
description: Match keyboard shortcuts to Visual Studio Code, emular Surface Duo e Samsung Galaxy Fold, melhorias de sobreposição de grade CSS e muito mais.
title: Novidades no DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: ec2219e9ebdd5d79c61bcaa813f7784246b1f5d0
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564942"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-86"></a><span data-ttu-id="af07e-104">Novidades no DevTools (Microsoft Edge 86)</span><span class="sxs-lookup"><span data-stu-id="af07e-104">What's New In DevTools (Microsoft Edge 86)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="af07e-105">Comunicados da equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="af07e-105">Announcements from the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### <a name="match-keyboard-shortcuts-in-devtools-to-visual-studio-code"></a><span data-ttu-id="af07e-106">Corresponder atalhos de teclado no DevTools para Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="af07e-106">Match keyboard shortcuts in DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="af07e-107">No Microsoft Edge 86, você pode corresponder atalhos de teclado no DevTools aos atalhos [em Microsoft Visual Studio Código][VisualStudioCodeMain].</span><span class="sxs-lookup"><span data-stu-id="af07e-107">In Microsoft Edge 86, you may match keyboard shortcuts in the DevTools to your shortcuts in [Microsoft Visual Studio Code][VisualStudioCodeMain].</span></span>  

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Corresponder atalhos de teclado no DevTools para Visual Studio Code" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   <span data-ttu-id="af07e-109">Corresponder atalhos de teclado no DevTools para Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="af07e-109">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-110">Para ativar esse recurso, navegue até [Personalizar atalhos de teclado no Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="af07e-110">To activate this feature, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  

<span data-ttu-id="af07e-111">Por exemplo, o atalho do teclado para pausar ou continuar executando um script [em][VisualStudioCodeShortcutsKeyboardWindows] Visual Studio Code é `F5` .</span><span class="sxs-lookup"><span data-stu-id="af07e-111">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="af07e-112">Com a **predefinição DevTools (Padrão),** esse mesmo atalho no DevTools é , mas quando você escolhe o Visual Studio Code predefinido, esse atalho agora `F8` também é \*\*\*\* `F5` .</span><span class="sxs-lookup"><span data-stu-id="af07e-112">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8`, but when you choose the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="af07e-113">Chromium problema [#174309][CR174309]</span><span class="sxs-lookup"><span data-stu-id="af07e-113">Chromium issue [#174309][CR174309]</span></span>  

### <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a><span data-ttu-id="af07e-114">Emular o Surface Duo e o Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="af07e-114">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="af07e-116">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="af07e-116">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-117">Agora você pode testar a aparência do seu site ou aplicativo em dois novos dispositivos: [Surface Duo][MicrosoftSurfaceDevicesDuo] e [Samsung Galaxy Fold][SamsungMobileGalaxyFold] no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="af07e-117">You are now able to test the look and feel of your website or app on two new devices:  [Surface Duo][MicrosoftSurfaceDevicesDuo] and [Samsung Galaxy Fold][SamsungMobileGalaxyFold] in Microsoft Edge.</span></span>  

<span data-ttu-id="af07e-118">Para ajudar a aprimorar seu site ou aplicativo para dispositivos de tela dupla e dobráveis, use os seguintes recursos ao [emular o dispositivo][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="af07e-118">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="af07e-119">[Abrangência][DevtoolsDeviceModeDualScreenAndFoldables], que é quando seu site \(ou app\) aparece em ambas as telas.</span><span class="sxs-lookup"><span data-stu-id="af07e-119">[Spanning][DevtoolsDeviceModeDualScreenAndFoldables], which is when your website \(or app\) appears across both screens.</span></span>
*   <span data-ttu-id="af07e-120">[Renderização da junção][DualScreenIntroductionHowWorkSeam], que é o espaço entre as duas telas.</span><span class="sxs-lookup"><span data-stu-id="af07e-120">[Rendering the seam][DualScreenIntroductionHowWorkSeam], which is the space between the two screens.</span></span>
*   <span data-ttu-id="af07e-121">Habilitando APIs experimentais da Plataforma Web para acessar o novo recurso de abrangência de tela de mídia [CSS][DualScreenWebCssMediaSpanning] e [JavaScript getWindowSegments API][DualScreenWebJavascriptGetwindowsegments].</span><span class="sxs-lookup"><span data-stu-id="af07e-121">Enabling experimental Web Platform APIs to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [JavaScript getWindowSegments API][DualScreenWebJavascriptGetwindowsegments].</span></span>  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Emulação de dispositivo para Surface Duo" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   <span data-ttu-id="af07e-123">Emulação de dispositivo para Surface Duo</span><span class="sxs-lookup"><span data-stu-id="af07e-123">Device emulation for Surface Duo</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-124">Para ativar esse recurso experimental, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **Emulação:** Suporte ao modo de tela dupla .</span><span class="sxs-lookup"><span data-stu-id="af07e-124">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Emulation: Support dual screen mode**.</span></span>  

<span data-ttu-id="af07e-125">Para obter mais informações sobre esse recurso, navegue até Emular dispositivos de tela dupla e [dobráveis Microsoft Edge DevTools][DevtoolsDeviceModeDualScreenAndFoldables].</span><span class="sxs-lookup"><span data-stu-id="af07e-125">For more information about this feature, navigate to [Emulate dual-screen and foldable devices in Microsoft Edge DevTools][DevtoolsDeviceModeDualScreenAndFoldables].</span></span>  

<span data-ttu-id="af07e-126">Chromium problema: [#1054281][CR1054281]</span><span class="sxs-lookup"><span data-stu-id="af07e-126">Chromium issue: [#1054281][CR1054281]</span></span>  

### <a name="css-grid-overlay-improvements-and-new-experimental-grid-features"></a><span data-ttu-id="af07e-127">Melhorias de sobreposição de grade CSS e novos recursos de grade experimentais</span><span class="sxs-lookup"><span data-stu-id="af07e-127">CSS grid overlay improvements and new experimental grid features</span></span>  

<span data-ttu-id="af07e-128">Obrigado pelos comentários positivos sobre as sobreposições de grade CSS aprimoradas.</span><span class="sxs-lookup"><span data-stu-id="af07e-128">Thank you for the positive feedback about the improved CSS grid overlays.</span></span>  <span data-ttu-id="af07e-129">As sobreposições de grade CSS agora estão habilitadas por padrão e não exigem que você ative um experimento.</span><span class="sxs-lookup"><span data-stu-id="af07e-129">The CSS grid overlays are now enabled by default and do not require you to turn on an experiment.</span></span>  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Sobreposição de grade CSS para elemento article" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   <span data-ttu-id="af07e-131">Sobreposição de grade CSS para `article` elemento</span><span class="sxs-lookup"><span data-stu-id="af07e-131">CSS grid overlay for `article` element</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="af07e-132">Para obter mais informações sobre sobreposições de grade, navegue até [recursos de depuração de][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]grade CSS.</span><span class="sxs-lookup"><span data-stu-id="af07e-132">For more information about grid overlays, navigate to [CSS grid debugging features][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="af07e-133">A Microsoft Edge de DevTools e a equipe do Chrome DevTools colaboram em recursos adicionais.</span><span class="sxs-lookup"><span data-stu-id="af07e-133">The Microsoft Edge DevTools team and the Chrome DevTools team collaborate on additional features.</span></span>  <span data-ttu-id="af07e-134">Os novos recursos incluem várias sobreposições persistentes e configuráveis de um novo **painel layout** na **ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="af07e-134">The new features include multiple overlays that are persistent and configurable from a new **Layout** pane on the **Elements** tool.</span></span>  

<span data-ttu-id="af07e-135">Para ativar esse recurso experimental, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de Habilitar novos recursos **de depuração**de Grade CSS (opções de configuração disponíveis no painel da barra lateral layout em Elementos após a reinicialização) .</span><span class="sxs-lookup"><span data-stu-id="af07e-135">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable new CSS Grid debugging features (configuration options available in Layout sidebar pane in Elements after restart)**.</span></span>  

<span data-ttu-id="af07e-136">Para obter mais informações sobre esse recurso, navegue até [Inspect CSS Grid in Microsoft Edge DevTools][DevtoolsCssGrid].</span><span class="sxs-lookup"><span data-stu-id="af07e-136">For more information about this feature, navigate to [Inspect CSS Grid in Microsoft Edge DevTools][DevtoolsCssGrid].</span></span>  

<span data-ttu-id="af07e-137">Chromium problema: [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="af07e-137">Chromium issue: [#1047356][CR1047356]</span></span>  

### <a name="table-copied-from-the-console-preserves-formatting"></a><span data-ttu-id="af07e-138">Tabela copiada do Console preserva a formatação</span><span class="sxs-lookup"><span data-stu-id="af07e-138">Table copied from the Console preserves formatting</span></span>  

<span data-ttu-id="af07e-139">No Microsoft Edge 85 ou anterior, a formatação de uma copiada `console.table` foi perdida.</span><span class="sxs-lookup"><span data-stu-id="af07e-139">In Microsoft Edge 85 or earlier, the formatting of a copied `console.table` was lost.</span></span>  <span data-ttu-id="af07e-140">Se você copiou a saída [da][DevtoolsConsoleApiTable] API de Console da tabela e a colou, apenas o texto da tabela foi mantido.</span><span class="sxs-lookup"><span data-stu-id="af07e-140">If you copied the output from the [table][DevtoolsConsoleApiTable] Console API, and pasted it, only the text of the table was kept.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="saída da API de console de tabela Microsoft Edge 85 ou anterior" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` <span data-ttu-id="af07e-142">Saída da API de console em Microsoft Edge 85 ou anterior</span><span class="sxs-lookup"><span data-stu-id="af07e-142">Console API output in Microsoft Edge 85 or earlier</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="saída da API de console de tabela Microsoft Edge 85 ou anteriormente Visual Studio Code" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="af07e-144">Saída da API de console Microsoft Edge 85 ou anteriormente Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="af07e-144">Console API output from Microsoft Edge 85 or earlier pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="af07e-145">No Microsoft Edge 86 ou posterior, quando você copia uma tabela do **Console**, a formatação agora é preservada.</span><span class="sxs-lookup"><span data-stu-id="af07e-145">In Microsoft Edge 86 or later, when you copy a table from the **Console**, the formatting is now preserved.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="saída da API de console de tabela Microsoft Edge 86 ou posterior" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` <span data-ttu-id="af07e-147">Saída da API de console Microsoft Edge 86 ou posterior</span><span class="sxs-lookup"><span data-stu-id="af07e-147">Console API output in Microsoft Edge 86 or later</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="saída da API de console de tabela Microsoft Edge 86 ou posteriores em Visual Studio Code" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="af07e-149">Saída da API de console Microsoft Edge 86 ou posteriormente passada para Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="af07e-149">Console API output from Microsoft Edge 86 or later pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="af07e-150">Chromium problema: [#1115011][CR1115011]</span><span class="sxs-lookup"><span data-stu-id="af07e-150">Chromium issue: [#1115011][CR1115011]</span></span>  

### <a name="source-order-viewer-for-easier-accessibility-testing"></a><span data-ttu-id="af07e-151">Visualizador de Ordem de Origem para testes de acessibilidade mais fáceis</span><span class="sxs-lookup"><span data-stu-id="af07e-151">Source Order Viewer for easier accessibility testing</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="af07e-153">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="af07e-153">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-154">O novo auxiliar de acessibilidade exibe a ordem dos elementos na origem.</span><span class="sxs-lookup"><span data-stu-id="af07e-154">The new accessibility helper displays the order of elements in the source.</span></span>  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Ativar Mostrar ordem de origem" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   <span data-ttu-id="af07e-156">Ativar **Mostrar ordem de origem**</span><span class="sxs-lookup"><span data-stu-id="af07e-156">Activate **Show source order**</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-157">Esse recurso facilita o teste da maneira como os usuários de teclado e leitor de tela experimentam seu site ou aplicativo.</span><span class="sxs-lookup"><span data-stu-id="af07e-157">This feature makes it easier to test the way screen reader and keyboard users experience your website or app.</span></span>  <span data-ttu-id="af07e-158">Leitores de tela e navegação por teclado dependem do conteúdo que está sendo colocado em uma ordem específica no código-fonte do seu site ou aplicativo, para que ele corresponde à página renderizada.</span><span class="sxs-lookup"><span data-stu-id="af07e-158">Screen readers and keyboard navigation depend on content being placed in a particular order in the source code of your website or app, so that it matches the rendered page.</span></span>  <span data-ttu-id="af07e-159">O Visualizador de Ordem de Origem exibe possíveis diferenças na ordem entre a página renderizada e o código-fonte.</span><span class="sxs-lookup"><span data-stu-id="af07e-159">The Source Order Viewer displays potential differences in order between the rendered page and the source code.</span></span>  

<span data-ttu-id="af07e-160">Para ativar esse recurso experimental, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **Habilitar o Visualizador**de Ordem de Origem.</span><span class="sxs-lookup"><span data-stu-id="af07e-160">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Source Order Viewer**.</span></span>  

<span data-ttu-id="af07e-161">Para obter mais informações sobre esse experimento, navegue até [Visualizador de Ordem de Origem][DevtoolsExperimentalFeaturesSourceOrderViewer].</span><span class="sxs-lookup"><span data-stu-id="af07e-161">For more information about this experiment, navigate to [Source Order Viewer][DevtoolsExperimentalFeaturesSourceOrderViewer].</span></span>  

<span data-ttu-id="af07e-162">Chromium problema: [#1094406][CR1094406]</span><span class="sxs-lookup"><span data-stu-id="af07e-162">Chromium issue: [#1094406][CR1094406]</span></span>  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Microsoft Edge DevTools in Traditional Chinese" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Microsoft Edge DevTools in Japanese" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### <a name="highlight-all-search-results-in-elements-tool"></a><span data-ttu-id="af07e-163">Realça todos os resultados da pesquisa na ferramenta Elements</span><span class="sxs-lookup"><span data-stu-id="af07e-163">Highlight all search results in Elements tool</span></span>  

<span data-ttu-id="af07e-164">Em Microsoft Edge 84 e 85, o primeiro resultado de pesquisa na **ferramenta Elements** não foi realçado.</span><span class="sxs-lookup"><span data-stu-id="af07e-164">In Microsoft Edge 84 and 85, the first search result in the **Elements** tool did not highlight.</span></span>  <span data-ttu-id="af07e-165">Os resultados restantes da pesquisa foram realçados corretamente.</span><span class="sxs-lookup"><span data-stu-id="af07e-165">The remaining search results were highlighted correctly.</span></span>  

<span data-ttu-id="af07e-166">Obrigado por enviar seus comentários e ajudar a melhorar Chromium.</span><span class="sxs-lookup"><span data-stu-id="af07e-166">Thank you for sending your feedback and helping improve Chromium.</span></span>  <span data-ttu-id="af07e-167">Seus comentários descobriram Problemas [#1103316][CR1103316] no projeto de Chromium de código aberto.</span><span class="sxs-lookup"><span data-stu-id="af07e-167">Your feedback uncovered Issue [#1103316][CR1103316] in the open-source Chromium project.</span></span>  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Primeiro resultado de pesquisa realçado no painel Elementos no Microsoft Edge 84 ou posterior" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   <span data-ttu-id="af07e-169">Primeiro resultado de pesquisa realçado na **ferramenta Elements** no Microsoft Edge 84 ou posterior</span><span class="sxs-lookup"><span data-stu-id="af07e-169">Highlighted first search result on **Elements** tool in Microsoft Edge 84 or later</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-170">O problema agora está corrigido em todas as versões Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="af07e-170">The issue is now fixed in all versions of Microsoft Edge.</span></span>  

<span data-ttu-id="af07e-171">Chromium problema: [#1103316][CR1103316]</span><span class="sxs-lookup"><span data-stu-id="af07e-171">Chromium issue: [#1103316][CR1103316]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="af07e-172">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="af07e-172">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-media-tool"></a><span data-ttu-id="af07e-173">Nova ferramenta de mídia</span><span class="sxs-lookup"><span data-stu-id="af07e-173">New Media tool</span></span>  

<span data-ttu-id="af07e-174">O DevTools agora exibe informações de media players na ferramenta [Media][DevtoolsMediaPanelIndex].</span><span class="sxs-lookup"><span data-stu-id="af07e-174">DevTools now displays media players information in the [Media][DevtoolsMediaPanelIndex] tool.</span></span>  

<span data-ttu-id="af07e-175">Para abrir a nova **ferramenta Mídia,** conclua a etapa a seguir.</span><span class="sxs-lookup"><span data-stu-id="af07e-175">To open the new **Media** tool, complete the following step.</span></span>  

1.  <span data-ttu-id="af07e-176">Escolha **Personalizar e controlar DevTools** \( `...` \) > Mais **ferramentas**  >  **Mídia**.</span><span class="sxs-lookup"><span data-stu-id="af07e-176">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Nova ferramenta de mídia" lightbox="../../media/2020/08/media-panel.msft.png":::
       <span data-ttu-id="af07e-178">Nova **ferramenta de** mídia</span><span class="sxs-lookup"><span data-stu-id="af07e-178">New **Media** tool</span></span>  
    :::image-end:::  

<span data-ttu-id="af07e-179">Antes da nova **ferramenta de mídia** no DevTools, as informações de registro em log e depuração sobre jogadores de vídeo estava localizada na configuração **Jogadores** Recentes.</span><span class="sxs-lookup"><span data-stu-id="af07e-179">Before the new **Media** tool in DevTools, the logging and debug information about video players was located under the **Recent Players** setting.</span></span>  <span data-ttu-id="af07e-180">Para abrir a **configuração Jogadores Recentes,** navegue até `edge://media-internals` e escolha a ferramenta **Players.**</span><span class="sxs-lookup"><span data-stu-id="af07e-180">To open the **Recent Players** setting, navigate to `edge://media-internals` and choose the **Players** tool.</span></span>  

<span data-ttu-id="af07e-181">Exibir conteúdo ao vivo e inspecionar possíveis problemas mais rapidamente, incluindo os exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="af07e-181">View live content and inspect potential issues more quickly, including the following examples.</span></span>  

*   <span data-ttu-id="af07e-182">Por que os quadros são descartados?</span><span class="sxs-lookup"><span data-stu-id="af07e-182">Why frames are dropped?</span></span>  
*   <span data-ttu-id="af07e-183">Por que JavaScript está interagindo com o jogador de forma inesperada?</span><span class="sxs-lookup"><span data-stu-id="af07e-183">Why JavaScript is interacting with the player in an unexpected way?</span></span>  

### <a name="capture-node-screenshots-using-the-elements-tool-context-menu"></a><span data-ttu-id="af07e-184">Capturar capturas de tela do nó usando o menu de contexto da ferramenta Elements</span><span class="sxs-lookup"><span data-stu-id="af07e-184">Capture node screenshots using the Elements tool context menu</span></span>  

<span data-ttu-id="af07e-185">Agora você pode capturar capturas de tela do nó usando o menu de contexto na **ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="af07e-185">You may now capture node screenshots using the context menu in the **Elements** tool.</span></span>  

<span data-ttu-id="af07e-186">Por exemplo, para fazer uma captura de tela do conteúdo, passe o mouse no elemento, abra o menu contextual \(clique com o botão direito do mouse\) e selecione Captura captura de tela do **nó**.</span><span class="sxs-lookup"><span data-stu-id="af07e-186">For example, to take a screenshot of the table of contents, hover on the element, open the contextual menu \(right-click\), and select **Capture node screenshot**.</span></span>  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Capturar capturas de tela do nó" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   <span data-ttu-id="af07e-188">Capturar capturas de tela do nó</span><span class="sxs-lookup"><span data-stu-id="af07e-188">Capture node screenshots</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-189">Chromium problema: [#1100253][CR1100253]</span><span class="sxs-lookup"><span data-stu-id="af07e-189">Chromium issue: [#1100253][CR1100253]</span></span>  

### <a name="issues-tool-updates"></a><span data-ttu-id="af07e-190">Problemas de atualizações da ferramenta</span><span class="sxs-lookup"><span data-stu-id="af07e-190">Issues tool updates</span></span>  

<span data-ttu-id="af07e-191">A barra de aviso Problemas na **ferramenta Console** agora é substituída por uma mensagem regular.</span><span class="sxs-lookup"><span data-stu-id="af07e-191">The Issues warning bar on the **Console** tool is now replaced with a regular message.</span></span>  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Problemas na mensagem do console" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   <span data-ttu-id="af07e-193">Problemas na mensagem do console</span><span class="sxs-lookup"><span data-stu-id="af07e-193">Issues in console message</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-194">Os problemas de cookie de terceiros agora estão ocultos por padrão na **ferramenta Problemas.**</span><span class="sxs-lookup"><span data-stu-id="af07e-194">Third-party cookie issues are now hidden by default in the **Issues** tool.</span></span>  <span data-ttu-id="af07e-195">Habilita a nova caixa de seleção Incluir **problemas de cookie** de terceiros para exibir os problemas.</span><span class="sxs-lookup"><span data-stu-id="af07e-195">Enable the new **Include third-party cookie issues** checkbox to view the issues.</span></span>  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="caixa de seleção de problemas de cookie de terceiros" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   <span data-ttu-id="af07e-197">caixa de seleção de problemas de cookie de terceiros</span><span class="sxs-lookup"><span data-stu-id="af07e-197">third-party cookie issues checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-198">Chromium problemas: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span><span class="sxs-lookup"><span data-stu-id="af07e-198">Chromium issues: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span></span>  

### <a name="emulate-missing-local-fonts"></a><span data-ttu-id="af07e-199">Emular fontes locais ausentes</span><span class="sxs-lookup"><span data-stu-id="af07e-199">Emulate missing local fonts</span></span>  

<span data-ttu-id="af07e-200">Abra a [ferramenta Rendering][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] e use o novo recurso Desabilitar fontes locais para emular fontes **ausentes** `local()` em `@font-face` regras.</span><span class="sxs-lookup"><span data-stu-id="af07e-200">Open the [Rendering tool][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] and use the new **Disable local fonts** feature to emulate missing `local()` sources in `@font-face` rules.</span></span>  

<span data-ttu-id="af07e-201">Por exemplo, quando a fonte é instalada em seu dispositivo e a regra a usa como fonte, Microsoft Edge usa o arquivo de fonte `Rubik` `@font-face src` local do seu `local()` dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af07e-201">For example, when the `Rubik` font is installed on your device and the `@font-face src` rule uses it as a `local()` font, Microsoft Edge uses the local font file from your device.</span></span>  

<span data-ttu-id="af07e-202">Quando **Desabilitar fontes locais** estiver habilitada, o DevTools ignorará as fontes e `local()` buscará cada uma da rede.</span><span class="sxs-lookup"><span data-stu-id="af07e-202">When **Disable local fonts** is enabled, DevTools ignores the `local()` fonts and fetches each from the network.</span></span>  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Emular fontes locais ausentes" lightbox="../../media/2020/08/disable-font.msft.png":::
   <span data-ttu-id="af07e-204">Emular fontes locais ausentes</span><span class="sxs-lookup"><span data-stu-id="af07e-204">Emulate missing local fonts</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-205">Se você usar duas cópias diferentes da mesma fonte durante o desenvolvimento, como os exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="af07e-205">If you use two different copies of the same font during development, such as the following examples.</span></span>  

*   <span data-ttu-id="af07e-206">Uma fonte local para suas ferramentas de design.</span><span class="sxs-lookup"><span data-stu-id="af07e-206">A local font for your design tools.</span></span>  
*   <span data-ttu-id="af07e-207">Uma fonte da Web para seu código.</span><span class="sxs-lookup"><span data-stu-id="af07e-207">A web font for your code.</span></span>  

<span data-ttu-id="af07e-208">Use **Desabilitar fontes locais** para facilitar a conclusão das seguintes tarefas.</span><span class="sxs-lookup"><span data-stu-id="af07e-208">Use **Disable local fonts** to make it easier for you to complete the following tasks.</span></span>  

*   <span data-ttu-id="af07e-209">Depurar e medir o desempenho de carregamento e a otimização de fontes da Web.</span><span class="sxs-lookup"><span data-stu-id="af07e-209">Debug and measure loading performance and optimization of web fonts.</span></span>  
*   <span data-ttu-id="af07e-210">Verifique a precisão de suas regras `@font-face` CSS.</span><span class="sxs-lookup"><span data-stu-id="af07e-210">Verify accuracy of your CSS `@font-face` rules.</span></span>  
*   <span data-ttu-id="af07e-211">Descubra as diferenças entre as versões locais instaladas em seu dispositivo e uma fonte da Web.</span><span class="sxs-lookup"><span data-stu-id="af07e-211">Discover differences between local versions installed on your device and a web font.</span></span>  

<span data-ttu-id="af07e-212">Chromium problema: [#384968][CR384968]</span><span class="sxs-lookup"><span data-stu-id="af07e-212">Chromium issue: [#384968][CR384968]</span></span>  

### <a name="emulate-inactive-users"></a><span data-ttu-id="af07e-213">Emular usuários inativos</span><span class="sxs-lookup"><span data-stu-id="af07e-213">Emulate inactive users</span></span>  

<span data-ttu-id="af07e-214">A [API de Detecção Ociosa][WebDevIdleDetection] permite que os desenvolvedores detectem usuários inativos e reajam em alterações de estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="af07e-214">The [Idle Detection API][WebDevIdleDetection] allows developers to detect inactive users and react on idle state changes.</span></span>  <span data-ttu-id="af07e-215">Agora você pode usar o DevTools para emular alterações de estado ocioso na ferramenta **Sensores** para o estado do usuário e o estado da tela, em vez de aguardar a alteração do estado ocioso real.</span><span class="sxs-lookup"><span data-stu-id="af07e-215">You are now able to use DevTools to emulate idle state changes in the **Sensors** tool for both the user state and the screen state instead of waiting for the actual idle state to change.</span></span>  <span data-ttu-id="af07e-216">Você pode abrir a **ferramenta Sensores** da [Gaveta][DevtoolsCustomizeIndexDrawer].</span><span class="sxs-lookup"><span data-stu-id="af07e-216">You may open the **Sensors** tool from the [Drawer][DevtoolsCustomizeIndexDrawer].</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Emular usuários inativos" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   <span data-ttu-id="af07e-218">Emular usuários inativos</span><span class="sxs-lookup"><span data-stu-id="af07e-218">Emulate inactive users</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-219">Chromium problema: [#1090802][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="af07e-219">Chromium issue: [#1090802][CR1090802]</span></span>  

### <a name="emulate-prefers-reduced-data"></a><span data-ttu-id="af07e-220">Emular prefere dados reduzidos</span><span class="sxs-lookup"><span data-stu-id="af07e-220">Emulate prefers-reduced-data</span></span>  

> [!NOTE]
> <span data-ttu-id="af07e-221">No Microsoft Edge 86, para habilitar esse recurso, navegue até e ative o sinalizador de recursos da `edge://flags#enable-experimental-web-platform-features` **Plataforma Web Experimental.**</span><span class="sxs-lookup"><span data-stu-id="af07e-221">In Microsoft Edge 86, to enable this feature, navigate to `edge://flags#enable-experimental-web-platform-features` and turn on the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="af07e-222">A opção de emulação só será exibida se o sinalizador estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="af07e-222">The emulation option is only displayed if the flag is enabled.</span></span>  

<span data-ttu-id="af07e-223">A [consulta de mídia prefers-reduced-data][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] detecta as preferências de conteúdo do usuário para dados reduzidos.</span><span class="sxs-lookup"><span data-stu-id="af07e-223">The [prefers-reduced-data][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] media query detects user content preferences for reduced data.</span></span>  <span data-ttu-id="af07e-224">Se selecionado, o usuário recebe conteúdo de página alternativo que usa menos dados.</span><span class="sxs-lookup"><span data-stu-id="af07e-224">If selected, the user receives alternate page content that uses less data.</span></span>  

<span data-ttu-id="af07e-225">Agora você pode usar o DevTools para emular a `prefers-reduced-data` consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="af07e-225">You may now use DevTools to emulate the `prefers-reduced-data` media query.</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Emular prefere dados reduzidos" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   <span data-ttu-id="af07e-227">Emular prefere dados reduzidos</span><span class="sxs-lookup"><span data-stu-id="af07e-227">Emulate prefers-reduced-data</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-228">Chromium problema: [#1096068][CR1096068]</span><span class="sxs-lookup"><span data-stu-id="af07e-228">Chromium issue: [#1096068][CR1096068]</span></span>  

### <a name="support-for-new-javascript-features"></a><span data-ttu-id="af07e-229">Suporte para novos recursos JavaScript</span><span class="sxs-lookup"><span data-stu-id="af07e-229">Support for new JavaScript features</span></span>  

<span data-ttu-id="af07e-230">O DevTools agora tem melhor suporte para os seguintes recursos de idioma JavaScript.</span><span class="sxs-lookup"><span data-stu-id="af07e-230">DevTools now have better supported the following JavaScript language features.</span></span>  

| <span data-ttu-id="af07e-231">Recurso de idioma JavaScript</span><span class="sxs-lookup"><span data-stu-id="af07e-231">JavaScript language feature</span></span> | <span data-ttu-id="af07e-232">Detalhes</span><span class="sxs-lookup"><span data-stu-id="af07e-232">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="af07e-233">Operadores de atribuição lógica</span><span class="sxs-lookup"><span data-stu-id="af07e-233">Logical assignment operators</span></span>][V8FeaturesLogicalAssignment] | <span data-ttu-id="af07e-234">O DevTools agora dá suporte à atribuição lógica com os novos operadores , e nas `&&=` ferramentas Console `||=` e `??=` **Sources.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="af07e-234">DevTools now supports logical assignment with the new `&&=`, `||=`, and `??=` operators in the **Console** and **Sources** tools.</span></span>  |  
| <span data-ttu-id="af07e-235">Separadores [numéricos][V8FeaturesNumericSeparators] de impressão bastante impressa</span><span class="sxs-lookup"><span data-stu-id="af07e-235">Pretty-print [numeric separators][V8FeaturesNumericSeparators]</span></span> | <span data-ttu-id="af07e-236">O DevTools agora imprime corretamente os separadores numéricos na **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="af07e-236">DevTools now properly pretty-prints the numeric separators in the **Sources** tool.</span></span>  |  

<span data-ttu-id="af07e-237">Chromium problemas: [1086817][CR1086817], [1080569][CR1080569]</span><span class="sxs-lookup"><span data-stu-id="af07e-237">Chromium issues: [1086817][CR1086817], [1080569][CR1080569]</span></span>  

### <a name="lighthouse-62-in-the-lighthouse-panel"></a><span data-ttu-id="af07e-238">Farol 6.2 no painel do Farol</span><span class="sxs-lookup"><span data-stu-id="af07e-238">Lighthouse 6.2 in the Lighthouse panel</span></span>  

<span data-ttu-id="af07e-239">A **ferramenta Doleiro** agora está executando o Farol 6.2.</span><span class="sxs-lookup"><span data-stu-id="af07e-239">The **Lighthouse** tool is now running Lighthouse 6.2.</span></span>  <span data-ttu-id="af07e-240">Para uma lista completa de alterações, navegue até as notas [de versão do Farol.][GithubGooglechromeLighthouseV620]</span><span class="sxs-lookup"><span data-stu-id="af07e-240">For a full list of changes, navigate to the [Lighthouse release notes][GithubGooglechromeLighthouseV620].</span></span>  

<span data-ttu-id="af07e-241">Chromium problema: [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="af07e-241">Chromium issue: [#772558][CR772558]</span></span>  

### <a name="deprecation-of-other-origins-listing-in-the-service-workers-pane"></a><span data-ttu-id="af07e-242">Deprecation of other origins listing in the Service Workers pane</span><span class="sxs-lookup"><span data-stu-id="af07e-242">Deprecation of other origins listing in the Service Workers pane</span></span>  

<span data-ttu-id="af07e-243">O DevTools agora fornece \*\*\*\* um link do painel Funcionários do Serviço**\(** Ferramenta de aplicativo > **Painel** de Funcionários do Serviço\) para exibir a lista completa de funcionários do serviço de outras origens.</span><span class="sxs-lookup"><span data-stu-id="af07e-243">DevTools now provides a link from the **Service workers** pane \(**Application** tool > **Service workers** pane\) to view the full list of service workers from other origins.</span></span>  <span data-ttu-id="af07e-244">Para acessar a lista sem abrir o DevTools, navegue até `edge://service-worker-internals/?devtools` .</span><span class="sxs-lookup"><span data-stu-id="af07e-244">To access the list without opening the DevTools, navigate to `edge://service-worker-internals/?devtools`.</span></span>  

<span data-ttu-id="af07e-245">Anteriormente, o DevTools exibia uma lista aninhada no **painel Ferramenta aplicativo** > **Funcionários do** Serviço.</span><span class="sxs-lookup"><span data-stu-id="af07e-245">Previously DevTools displayed a list nested under the **Application** tool > **Service workers** pane.</span></span>  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Link para outras origens" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   <span data-ttu-id="af07e-247">Link para outras origens</span><span class="sxs-lookup"><span data-stu-id="af07e-247">Link to other origins</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-248">Chromium problema: [#807440][CR807440]</span><span class="sxs-lookup"><span data-stu-id="af07e-248">Chromium issue: [#807440][CR807440]</span></span>  

### <a name="show-coverage-summary-for-filtered-items"></a><span data-ttu-id="af07e-249">Mostrar resumo de cobertura para itens filtrados</span><span class="sxs-lookup"><span data-stu-id="af07e-249">Show coverage summary for filtered items</span></span>  

<span data-ttu-id="af07e-250">Agora, o DevTools recalculará e exibirá um resumo das informações de cobertura dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="af07e-250">DevTools now recalculate and display a summary of coverage information dynamically.</span></span>  <span data-ttu-id="af07e-251">A exibição dinâmica é disparada quando os filtros são aplicados na [ferramenta Cobertura.][DevtoolsCoverageIndex]</span><span class="sxs-lookup"><span data-stu-id="af07e-251">The dynamic display is triggered when filters are applied in the [Coverage][DevtoolsCoverageIndex] tool.</span></span>  <span data-ttu-id="af07e-252">Antes que **a ferramenta Coverage** sempre exibia um resumo de todas as informações de cobertura.</span><span class="sxs-lookup"><span data-stu-id="af07e-252">Before the **Coverage** tool always displayed a summary of all coverage information.</span></span>  

<span data-ttu-id="af07e-253">Na primeira das figuras a seguir, o resumo é exibido inicialmente e, na segunda das figuras a seguir, o resumo é exibido depois que a filtragem `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` CSS é aplicada.</span><span class="sxs-lookup"><span data-stu-id="af07e-253">In the first of the following figures, the summary initially displays `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` and in the second of the following figures, the summary displays `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` after CSS filtering is applied.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Resumo de cobertura" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         <span data-ttu-id="af07e-255">Resumo de cobertura</span><span class="sxs-lookup"><span data-stu-id="af07e-255">Coverage summary</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Resumo de cobertura para itens filtrados" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         <span data-ttu-id="af07e-257">Resumo de cobertura para itens filtrados</span><span class="sxs-lookup"><span data-stu-id="af07e-257">Coverage summary for filtered items</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="af07e-258">Chromium problema: [#1061385][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="af07e-258">Chromium issue: [#1061385][CR1090802]</span></span>  

### <a name="new-frame-details-view-in-application-panel"></a><span data-ttu-id="af07e-259">Nova exibição de detalhes do quadro no painel Aplicativo</span><span class="sxs-lookup"><span data-stu-id="af07e-259">New frame details view in Application panel</span></span>  

<span data-ttu-id="af07e-260">O DevTools agora mostra uma exibição detalhada para cada quadro.</span><span class="sxs-lookup"><span data-stu-id="af07e-260">DevTools now show a detailed view for each frame.</span></span>  <span data-ttu-id="af07e-261">Para acessá-lo, escolha um quadro no menu **Quadros** na **ferramenta Aplicativo.**</span><span class="sxs-lookup"><span data-stu-id="af07e-261">To access it, choose a frame under the **Frames** menu in the **Application** tool.</span></span>  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Nova exibição detalhada para um quadro no painel Aplicativo" lightbox="../../media/2020/08/frame-details.msft.png":::
   <span data-ttu-id="af07e-263">Nova exibição detalhada para um quadro na **ferramenta Application**</span><span class="sxs-lookup"><span data-stu-id="af07e-263">New detailed view for a frame in **Application** tool</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-264">Chromium problema: [#1093247][CR1093247]</span><span class="sxs-lookup"><span data-stu-id="af07e-264">Chromium issue: [#1093247][CR1093247]</span></span>  

#### <a name="frame-details-for-opened-windows"></a><span data-ttu-id="af07e-265">Detalhes do quadro para janelas abertas</span><span class="sxs-lookup"><span data-stu-id="af07e-265">Frame details for opened windows</span></span>  

<span data-ttu-id="af07e-266">Abra janelas e janelas pop-up agora exibidas sob a árvore de quadros também.</span><span class="sxs-lookup"><span data-stu-id="af07e-266">Open windows and pop-up windows now display under the frame tree as well.</span></span>  <span data-ttu-id="af07e-267">A exibição detalhada das janelas abertas inclui informações adicionais de segurança.</span><span class="sxs-lookup"><span data-stu-id="af07e-267">The detailed view of the opened windows includes additional security information.</span></span>  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Novo quadro de exibição detalhado para janelas abertas" lightbox="../../media/2020/08/window-opener.msft.png":::
   <span data-ttu-id="af07e-269">Novo quadro de exibição detalhado para janelas abertas</span><span class="sxs-lookup"><span data-stu-id="af07e-269">New frame detailed view for opened windows</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-270">Chromium problema: [#1107766][CR1107766]</span><span class="sxs-lookup"><span data-stu-id="af07e-270">Chromium issue: [#1107766][CR1107766]</span></span>  

#### <a name="security-and-isolation-information"></a><span data-ttu-id="af07e-271">Informações de segurança e isolamento</span><span class="sxs-lookup"><span data-stu-id="af07e-271">Security and isolation information</span></span>  

<span data-ttu-id="af07e-272">Contexto seguro, [CoEP (Cross-Origin-Embedder-Policy)][WebDevCoopCoep]e [CROSS-Origin-Opener-Policy (COOP)][WebDevCoopCoep] agora são exibidos nos detalhes do quadro.</span><span class="sxs-lookup"><span data-stu-id="af07e-272">Secure context, [Cross-Origin-Embedder-Policy (COEP)][WebDevCoopCoep], and [Cross-Origin-Opener-Policy (COOP)][WebDevCoopCoep] are now displayed in the frame details.</span></span>  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Informações de segurança e isolamento" lightbox="../../media/2020/08/coep-coop.msft.png":::
   <span data-ttu-id="af07e-274">Informações de segurança e isolamento</span><span class="sxs-lookup"><span data-stu-id="af07e-274">Security and isolation information</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-275">No futuro, a equipe Microsoft Edge DevTools e a equipe do Chrome DevTools planejam adicionar mais informações de segurança aos detalhes do quadro.</span><span class="sxs-lookup"><span data-stu-id="af07e-275">In the future, the Microsoft Edge DevTools team and the Chrome DevTools team are planning to add more security information to the frame details.</span></span>  

<span data-ttu-id="af07e-276">Chromium problema: [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="af07e-276">Chromium issue: [#1051466][CR1051466]</span></span>  

### <a name="elements-and-network-panel-updates"></a><span data-ttu-id="af07e-277">Elementos e atualizações de painel de rede</span><span class="sxs-lookup"><span data-stu-id="af07e-277">Elements and Network panel updates</span></span>  

#### <a name="accessible-color-suggestion-in-the-styles-pane"></a><span data-ttu-id="af07e-278">Sugestão de cor acessível no painel Estilos</span><span class="sxs-lookup"><span data-stu-id="af07e-278">Accessible color suggestion in the Styles pane</span></span>  

<span data-ttu-id="af07e-279">O DevTools agora fornece sugestões de cores para texto de contraste de cor baixo.</span><span class="sxs-lookup"><span data-stu-id="af07e-279">DevTools now provides color suggestions for low color contrast text.</span></span>  

<span data-ttu-id="af07e-280">No exemplo abaixo, `h1` tem texto de baixo contraste.</span><span class="sxs-lookup"><span data-stu-id="af07e-280">In the example below, `h1` has low contrast text.</span></span>  <span data-ttu-id="af07e-281">Para corrigi-lo, abra o selador de cores `color` da propriedade no painel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="af07e-281">To fix it, open the color picker of the `color` property in the **Styles** pane.</span></span>  <span data-ttu-id="af07e-282">Depois de expandir a seção **Taxa de contraste,** o DevTools fornece sugestões de cores AA e AAA.</span><span class="sxs-lookup"><span data-stu-id="af07e-282">After you expand the **Contrast ratio** section, DevTools provides AA and AAA color suggestions.</span></span>  <span data-ttu-id="af07e-283">Escolha a cor sugerida para aplicar a cor.</span><span class="sxs-lookup"><span data-stu-id="af07e-283">Choose the suggested color to apply the color.</span></span>  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="O se picker de cores sugere sugestões de cores AA e AAA" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   <span data-ttu-id="af07e-285">O se picker de cores sugere sugestões de cores AA e AAA</span><span class="sxs-lookup"><span data-stu-id="af07e-285">Color picker suggests AA and AAA color suggestions</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-286">Chromium problema: [#1093227][CR1093227]</span><span class="sxs-lookup"><span data-stu-id="af07e-286">Chromium issue: [#1093227][CR1093227]</span></span>  

#### <a name="reinstate-properties-pane-in-the-elements-panel"></a><span data-ttu-id="af07e-287">Reinstalar o painel Propriedades no painel Elementos</span><span class="sxs-lookup"><span data-stu-id="af07e-287">Reinstate Properties pane in the Elements panel</span></span>  

<span data-ttu-id="af07e-288">O **painel Propriedades** está de volta.</span><span class="sxs-lookup"><span data-stu-id="af07e-288">The **Properties** pane is back.</span></span>  <span data-ttu-id="af07e-289">Foi [preterido no Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span><span class="sxs-lookup"><span data-stu-id="af07e-289">It was [deprecated in Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span></span>  <span data-ttu-id="af07e-290">A Microsoft Edge de DevTools e a equipe do Chrome DevTools estão planejando melhorias para inspecionar propriedades de elementos.</span><span class="sxs-lookup"><span data-stu-id="af07e-290">The Microsoft Edge DevTools team and the Chrome DevTools team are planning improvements for inspecting properties of elements.</span></span>  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Painel Propriedades no painel Elementos" lightbox="../../media/2020/08/properties-pane.msft.png":::
   <span data-ttu-id="af07e-292">**Painel Propriedades** na **ferramenta Elementos**</span><span class="sxs-lookup"><span data-stu-id="af07e-292">**Properties** pane in the **Elements** tool</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-293">Chromium problema:</span><span class="sxs-lookup"><span data-stu-id="af07e-293">Chromium issue:</span></span>  <!--  [#1105205][CR1105205],  -->  <span data-ttu-id="af07e-294">[#1116085] [CR1116085]</span><span class="sxs-lookup"><span data-stu-id="af07e-294">[#1116085][CR1116085]</span></span>  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Human-readable `X-Client-Data` header values" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### <a name="autocomplete-custom-fonts-in-the-styles-pane"></a><span data-ttu-id="af07e-295">Preenchimento automático de fontes personalizadas no painel Estilos</span><span class="sxs-lookup"><span data-stu-id="af07e-295">Autocomplete custom fonts in the Styles pane</span></span>  

<span data-ttu-id="af07e-296">Os rostos de fonte importados agora são adicionados à lista de autocompleção CSS ao editar a propriedade `font-family` no painel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="af07e-296">Imported font faces are now added to the list of CSS autocompletion when editing the `font-family` property in the **Styles** pane.</span></span>  

<span data-ttu-id="af07e-297">Por exemplo, se for uma fonte personalizada instalada no `monospace` computador local, ela será exibida na lista de conclusão css.</span><span class="sxs-lookup"><span data-stu-id="af07e-297">For example, if `monospace` is a custom font installed on the local machine, it displays in the CSS completion list.</span></span>  <span data-ttu-id="af07e-298">Nas versões anteriores Microsoft Edge, a fonte não era exibida.</span><span class="sxs-lookup"><span data-stu-id="af07e-298">In previous versions of Microsoft Edge, the font was not displayed.</span></span>

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Preenchimento automático de fontes personalizadas" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   <span data-ttu-id="af07e-300">Preenchimento automático de fontes personalizadas</span><span class="sxs-lookup"><span data-stu-id="af07e-300">Autocomplete custom fonts</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-301">Chromium problema: [#1106221][CR1106221]</span><span class="sxs-lookup"><span data-stu-id="af07e-301">Chromium issue: [#1106221][CR1106221]</span></span>  

#### <a name="consistently-display-resource-type-in-network-panel"></a><span data-ttu-id="af07e-302">Exibir consistentemente o tipo de recurso no painel Rede</span><span class="sxs-lookup"><span data-stu-id="af07e-302">Consistently display resource type in Network panel</span></span>  

<span data-ttu-id="af07e-303">O DevTools agora exibe consistentemente o mesmo tipo de recurso que a solicitação de rede original e anexa ao valor de coluna Type quando o `/ Redirect` redirecionamento \(código de status HTTP 302\) acontece. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="af07e-303">DevTools now consistently display the same resource type as the original network request and appends `/ Redirect` to the **Type** column value when redirection \(HTTP status code 302\) happens.</span></span>  

<span data-ttu-id="af07e-304">Anteriormente, o DevTools alterou o tipo para às `Other` vezes.</span><span class="sxs-lookup"><span data-stu-id="af07e-304">Previously DevTools changed the type to `Other` sometimes.</span></span>  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Exibir tipo de recurso de redirecionamento" lightbox="../../media/2020/08/network-redirect.msft.png":::
   <span data-ttu-id="af07e-306">Exibir tipo de recurso de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="af07e-306">Display redirect resource type</span></span>  
:::image-end:::  

<span data-ttu-id="af07e-307">Chromium problema: [#997694][CR997694]</span><span class="sxs-lookup"><span data-stu-id="af07e-307">Chromium issue: [#997694][CR997694]</span></span>  

#### <a name="clear-buttons-in-the-elements-and-network-tools"></a><span data-ttu-id="af07e-308">Limpar botões nas ferramentas Elementos e Rede</span><span class="sxs-lookup"><span data-stu-id="af07e-308">Clear buttons in the Elements and Network tools</span></span>  

<span data-ttu-id="af07e-309">As caixas de texto a seguir agora têm **botões Clear.**</span><span class="sxs-lookup"><span data-stu-id="af07e-309">The following text boxes now have **Clear** buttons.</span></span>  

*   <span data-ttu-id="af07e-310">As caixas de texto do filtro no painel **Estilos** e **na ferramenta** Rede.</span><span class="sxs-lookup"><span data-stu-id="af07e-310">The filter text boxes in the **Styles** pane and **Network** tool.</span></span>  
*   <span data-ttu-id="af07e-311">A caixa de texto de pesquisa DOM na **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="af07e-311">The DOM search text box in the **Elements** tool.</span></span>  

<span data-ttu-id="af07e-312">Escolha o **botão Limpar** para remover qualquer texto de entrada.</span><span class="sxs-lookup"><span data-stu-id="af07e-312">Choose the **Clear** button to remove any inputted text.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Limpar botões nos painéis Elementos" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         <span data-ttu-id="af07e-314">Limpar botões nas ferramentas **Elements**</span><span class="sxs-lookup"><span data-stu-id="af07e-314">Clear buttons in the **Elements** tools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Limpar botões nos painéis rede" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         <span data-ttu-id="af07e-316">Limpar botões nas ferramentas  **de** rede</span><span class="sxs-lookup"><span data-stu-id="af07e-316">Clear buttons in the  **Network** tools</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="af07e-317">Chromium problema: [#1067184][CR1067184]</span><span class="sxs-lookup"><span data-stu-id="af07e-317">Chromium issue: [#1067184][CR1067184]</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="af07e-318">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="af07e-318">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="af07e-319">Se você estiver no Windows ou macOS, considere usar os canais [Microsoft Edge de][MicrosoftEdgePreviewChannels] visualização como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="af07e-319">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="af07e-320">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="af07e-320">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="af07e-321">Como entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="af07e-321">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Deprecation do painel Propriedades no painel Elementos - Novidades no DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Recursos de depuração de grade CSS - Novidades no DevTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsConsoleApiTable]: ../../../console/api.md#table "table - Console API reference | Microsoft Docs"  
[DevtoolsCoverageIndex]: ../../../coverage/index.md "Encontre o JavaScript e o código CSS não Microsoft Edge código CSS não Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssGrid]: ../../../css/grid.md "Inspecionar Grade CSS no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: ../../../customize/index.md#drawer "Gaveta - Personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personalize os atalhos do teclado no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../../../device-mode/dual-screen-and-foldables.md "Emular dispositivos de tela dupla e dobráveis Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: ../../../evaluate-performance/reference.md#analyze-rendering-performance-with-the-rendering-tool "Analisar o desempenho da renderização com a ferramenta Rendering - Performance Analysis Reference | Microsoft Docs"  
<!--  [DevtoolsExperimentalFeaturesEnableExperimentalApis]: ../../../experimental-features/index.md#enable-experimental-apis "Enable experimental APIs - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: .. /.. /.. /experimental-features/index.md#emulation-support-dual-screen-mode "Emulation: Support dual screen mode - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesSourceOrderViewer]: .. /.. /.. /experimental-features/index.md#source-order-viewer "Source Order Viewer - Recursos experimentais | Microsoft Docs"
<!--  [DevtoolsExperimentalFeaturesTestOnFoldableDualScreenDevices]: ../../../experimental-features/index.md#test-on-foldable-and-dual-screen-devices "Test on foldable and dual-screen devices - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: .. /.. /.. /experimental-features/index.md#turn-on-experimental-features "Ativar recursos experimentais - Recursos experimentais | Microsoft Docs"  
[DevtoolsMediaPanelIndex]: .. /.. /.. /media-panel/index.md "Exibir e depurar informações de jogadores de mídia | Microsoft Docs"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Como trabalhar com a junção – Introdução aos dispositivos de duas telas | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Recurso de abrangência de tela de mídia CSS para detecção de dualidade de tela | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "A API JavaScript getWindowSegments para dispositivos de duas telas | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de visualização do Microsoft Edge"  

[VisualStudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio Code Atalhos de teclado para Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "O novo Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "conta @EdgeDevTools do Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros do Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: Permitir personalizar atalhos de teclado/vinculações de teclas | Chromium bugs"
[CR384968]: https://crbug.com/384968 "Opção para ignorar fontes locais() | Chromium bugs"  
[CR772558]: https://crbug.com/772558 "DevTools: atualizar para a versão mais recente do | Chromium bugs"  
[CR807440]: https://crbug.com/807440 "O Chrome bloqueia com um grande número de SWs | Chromium bugs"  
[CR997694]: https://crbug.com/997694 "As solicitações XHR com status 302 não são mostradas no filtro \"xhr\" no painel de rede | Chromium bugs"  
[CR1047356]: https://crbug.com/1047356 "Css Grid/Flexbox/Table tooling | Chromium bugs"  
[CR1051466]: https://crbug.com/1051466 "Suporte à depuração DE COOP/COEP no DevTools | Chromium bugs"  
[CR1054281]: https://crbug.com/1054281 "Solicitação de Recurso: DevTools deve emular dispositivos dobráveis e de tela dupla | Chromium bugs"  
[CR1067184]: https://crbug.com/1067184 "Solicitação de Recurso: limpar o botão de filtro em Elementos & Rede -> Entradas de Filtro de Estilo | Chromium bugs"  
[CR1068116]: https://crbug.com/1068116 "☂ Painel de problemas de | Chromium bugs"  
[CR1080569]: https://crbug.com/1080569 "Acorn não dá suporte a operadores de atribuição lógica | Chromium bugs"  
[CR1080589]: https://crbug.com/1080589 "Classificar problemas por terceiros/usuários de terceiros | Chromium bugs"  
[CR1086817]: https://crbug.com/1086817 "Acorn não dá suporte a separadores numéricos | Chromium bugs"  
[CR1090802]: https://crbug.com/1090802 "Simular alterações de estado ocioso da API de Detecção Ociosa | Chromium bugs"  
[CR1093227]: https://crbug.com/1093227 "DevTools: sugerir cores acessíveis mais próximas | Chromium bugs"  
[CR1093247]: https://crbug.com/1093247 "Exibir informações sobre quadros no painel de aplicativos | Chromium bugs"  
[CR1094406]: https://crbug.com/1094406 "Os desenvolvedores querem um visualizador de ordem de origem para AT https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: suporte à emulação do recurso de mídia prefers-reduced-data | Chromium bugs"  
[CR1096481]: https://crbug.com/1096481 "Problemas de posicionamento de faixa | Chromium bugs"  
[CR1100253]: https://crbug.com/1100253 "Adicionar atalho de nó de captura de tela no menu de contexto elemento | Chromium bugs"  
[CR1103316]: https://crbug.com/1103316 "A pesquisa de elementos não resolveNode (texto de realçada, etc) no primeiro resultado da pesquisa | Chromium bugs"  
[CR1103854]: https://crbug.com/1103854 "Desobfusar valores X-Client-Data em Ferramentas de Desenvolvedor | Chromium bugs"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: "Adicionar fontes importadas à autocompleção da família de fontes no painel https://crbug.com/1106221 Estilos | Chromium bugs"  
[CR1107766]: "Exibir informações sobre quadros gerados por https://crbug.com/1107766 'window.open()' na árvore de quadros | Chromium bugs"  
[CR1115011]: "Ao copiar uma tabela do console, a estrutura da tabela não é https://crbug.com/1115011 preservada | Chromium bugs"  
[CR1116085]: "Por favor, traga de volta o inspetor de propriedades https://crbug.com/1116085 de DevTools | Chromium bugs"  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "prefers-reduced-data - Media Queries Level 5 | Rascunhos do Editor do Grupo de Trabalho CSS do W3C"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v6.2.0 - GoogleChrome/| GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Buffers de protocolo | Desenvolvedores do Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung US"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Atribuição lógica | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Separadores numéricos | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Tornar seu site \"isolado entre origens\" usando o COOP e o COEP | web.dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Detectar usuários inativos com a API de Detecção Ociosa | web.dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Evite animações não compostas | web.dev"  

> [!NOTE]
> <span data-ttu-id="af07e-380">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="af07e-380">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="af07e-381">A página original é encontrada [aqui](https://developer.chrome.com/blog/new-in-devtools-86) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="af07e-381">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-86) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="af07e-383">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="af07e-383">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
