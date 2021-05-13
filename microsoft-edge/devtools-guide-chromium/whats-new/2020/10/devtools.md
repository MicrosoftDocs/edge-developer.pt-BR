---
description: Novas ferramentas de depuração de Grade CSS, ferramenta Webauthn, ferramentas movêveis e painel de barra lateral computada.
title: Novidades no DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c7859631327fc031909cd25736fddb8cff3cff45
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564893"
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
# <a name="whats-new-in-devtools-microsoft-edge-87"></a><span data-ttu-id="6d652-104">Novidades no DevTools (Microsoft Edge 87)</span><span class="sxs-lookup"><span data-stu-id="6d652-104">What's New In DevTools (Microsoft Edge 87)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="improving-devtools-localization"></a><span data-ttu-id="6d652-105">Melhorando a localização do DevTools</span><span class="sxs-lookup"><span data-stu-id="6d652-105">Improving DevTools localization</span></span>  

<span data-ttu-id="6d652-106">Para atender às suas necessidades de conversão, a equipe Microsoft Edge DevTools está focada em melhorar a qualidade da tradução.</span><span class="sxs-lookup"><span data-stu-id="6d652-106">To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.</span></span>  <span data-ttu-id="6d652-107">A partir da Microsoft Edge versão 87, várias cadeias de caracteres e termos são bloqueados e não mudam mesmo quando o restante do DevTools é exibido em outros idiomas.</span><span class="sxs-lookup"><span data-stu-id="6d652-107">Starting in Microsoft Edge version 87, several strings and terms are locked and do not change even when the rest of the DevTools are displayed in other languages.</span></span>  <span data-ttu-id="6d652-108">A lista de cadeias de caracteres e termos afetados inclui o seguinte.</span><span class="sxs-lookup"><span data-stu-id="6d652-108">The list of affected strings and terms include the following.</span></span>  

*   <span data-ttu-id="6d652-109">As cadeias de caracteres na **ferramenta Doleiro.**</span><span class="sxs-lookup"><span data-stu-id="6d652-109">The strings in the **Lighthouse** tool.</span></span>  
*   <span data-ttu-id="6d652-110">O termo `service worker` .</span><span class="sxs-lookup"><span data-stu-id="6d652-110">The term `service worker`.</span></span>  
*   <span data-ttu-id="6d652-111">Alguns dos **filtros da ferramenta** Network, como , , e `URL` `XHR` `JS` `CSS` .</span><span class="sxs-lookup"><span data-stu-id="6d652-111">Some of the **Network** tool filters such as `URL`, `XHR`, `JS`, and `CSS`.</span></span>  
*   <span data-ttu-id="6d652-112">A API de Utilitários de Console de [US$ 0.][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]</span><span class="sxs-lookup"><span data-stu-id="6d652-112">The [$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject] Console Utilities API.</span></span>  
    
<span data-ttu-id="6d652-113">[$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject] agora está disponível no [Console para][DevtoolsConsoleIndex] usuários em versões localizadas do DevTools.</span><span class="sxs-lookup"><span data-stu-id="6d652-113">[$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject] is now available in the [Console][DevtoolsConsoleIndex] for users on localized versions of the DevTools.</span></span>   <span data-ttu-id="6d652-114">Obrigado à comunidade global de desenvolvedores por ajudar a melhorar a localização do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="6d652-114">Thank you to the global developer community for helping improve localization of the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="6d652-115">Continue a [enviar comentários sobre a qualidade da localização](#getting-in-touch-with-microsoft-edge-devtools-team) para melhorar o suporte para o DevTools em todas as localidades.</span><span class="sxs-lookup"><span data-stu-id="6d652-115">Continue to [send feedback on localization quality](#getting-in-touch-with-microsoft-edge-devtools-team) to improve support for DevTools in all locales.</span></span>  <span data-ttu-id="6d652-116">Para revisar as atualizações em tempo real sobre esse recurso no Chromium de código aberto, navegue até Problema [#1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="6d652-116">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1136655][CR1136655].</span></span>  


:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Ferramenta de rede com filtros não localizados" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   <span data-ttu-id="6d652-118">**Painel** de rede com filtros não localizados</span><span class="sxs-lookup"><span data-stu-id="6d652-118">**Network** pane with non-localized filters</span></span>  
:::image-end:::  

## <a name="move-tools-between-top-and-bottom-panels"></a><span data-ttu-id="6d652-119">Mover ferramentas entre painéis superior e inferior</span><span class="sxs-lookup"><span data-stu-id="6d652-119">Move tools between top and bottom panels</span></span>  

<span data-ttu-id="6d652-120">O DevTools agora dá suporte à movimentação de ferramentas entre os painéis superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="6d652-120">DevTools now supports moving tools between the top and bottom panels.</span></span>  <span data-ttu-id="6d652-121">Personalize seu DevTools e melhore sua produtividade exibindo qualquer combinação de duas ferramentas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="6d652-121">Customize your DevTools and improve your productivity by viewing any combination of two tools at the same time.</span></span>  <span data-ttu-id="6d652-122">Por exemplo, ex view the **Elements** and the **Sources** tools at the same time \(by moving the **Sources** tool to the bottom\).</span><span class="sxs-lookup"><span data-stu-id="6d652-122">For example, view the **Elements** and the **Sources** tools at the same time \(by moving the **Sources** tool to the bottom\).</span></span>  <span data-ttu-id="6d652-123">Para revisar o histórico desse recurso no Chromium de código aberto, navegue até Problema [#1075732][CR1075732].</span><span class="sxs-lookup"><span data-stu-id="6d652-123">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1075732][CR1075732].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="6d652-124">Para mover qualquer ferramenta superior para a parte inferior, passe o mouse em uma guia, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Mover para baixo**.</span><span class="sxs-lookup"><span data-stu-id="6d652-124">To move any top tool to the bottom, hover on a tab, open the contextual menu \(right-click\), and choose **Move to bottom**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Mover para baixo" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         <span data-ttu-id="6d652-126">Mover para baixo</span><span class="sxs-lookup"><span data-stu-id="6d652-126">Move to bottom</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="6d652-127">Para mover qualquer ferramenta inferior para a parte superior, passe o mouse em uma guia, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Mover para cima**.</span><span class="sxs-lookup"><span data-stu-id="6d652-127">To move any bottom tool to the top, hover on a tab, open the contextual menu \(right-click\), and choose **Move to top**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Mover para cima" lightbox="../../media/2020/10/move-to-top.msft.png":::
         <span data-ttu-id="6d652-129">Mover para cima</span><span class="sxs-lookup"><span data-stu-id="6d652-129">Move to top</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <a name="save-and-export-using-the-network-console"></a><span data-ttu-id="6d652-130">Salvar e exportar usando o Console de Rede</span><span class="sxs-lookup"><span data-stu-id="6d652-130">Save and export using the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="6d652-132">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="6d652-132">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="6d652-133">A **ferramenta Console de** Rede agora melhorou a compatibilidade com os esquemas [Postman v2.1][PostmanSchemaJsonCollectionv210Index] e [OpenAPI v2.][SwaggerSpecificationV2]</span><span class="sxs-lookup"><span data-stu-id="6d652-133">The **Network Console** tool now has improved compatibility with the [Postman v2.1][PostmanSchemaJsonCollectionv210Index] and [OpenAPI v2][SwaggerSpecificationV2] schemas.</span></span>  <span data-ttu-id="6d652-134">Para habilitar o experimento, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **Habilitar Console de Rede**.</span><span class="sxs-lookup"><span data-stu-id="6d652-134">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Network Console**.</span></span>  <span data-ttu-id="6d652-135">Para obter mais informações sobre o Console de **Rede,** navegue até [Habilitar o recurso Experimental do Console de Rede][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span><span class="sxs-lookup"><span data-stu-id="6d652-135">For more information about the **Network Console**, navigate to [Enable Network Console Experimental feature][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span></span>  <span data-ttu-id="6d652-136">Este experimento agora dá suporte às seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="6d652-136">This experiment now supports the following actions.</span></span>  

*   <span data-ttu-id="6d652-137">Salvar e exportar Coleções e Ambientes.</span><span class="sxs-lookup"><span data-stu-id="6d652-137">Save and export Collections and Environments.</span></span>  
*   <span data-ttu-id="6d652-138">Editar e exportar conjuntos de variáveis de ambiente na **ferramenta Console de** Rede.</span><span class="sxs-lookup"><span data-stu-id="6d652-138">Edit and export sets of environment variables within the **Network Console** tool.</span></span>  
    
<span data-ttu-id="6d652-139">Para revisar as atualizações em tempo real sobre esse recurso no Chromium de código aberto, navegue até Problema [#1093687][CR1093687].</span><span class="sxs-lookup"><span data-stu-id="6d652-139">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1093687][CR1093687].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Digite o nome do novo ambiente" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         <span data-ttu-id="6d652-141">Digite o nome do novo ambiente</span><span class="sxs-lookup"><span data-stu-id="6d652-141">Enter name for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Escolher formato para o novo ambiente" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         <span data-ttu-id="6d652-143">Escolher formato para o novo ambiente</span><span class="sxs-lookup"><span data-stu-id="6d652-143">Choose format for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-grid-tooling"></a><span data-ttu-id="6d652-144">Ferramentas de Grade CSS aprimoradas</span><span class="sxs-lookup"><span data-stu-id="6d652-144">Improved CSS Grid tooling</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="6d652-146">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="6d652-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="6d652-147">O Microsoft Edge DevTools agora oferece suporte aos seguintes recursos para inspecionar, exibir e depurar suas grades CSS.</span><span class="sxs-lookup"><span data-stu-id="6d652-147">The Microsoft Edge DevTools now support the following features for inspecting, viewing, and debugging your CSS grids.</span></span>  

*   <span data-ttu-id="6d652-148">Exibe uma sobreposição de grade simplificada usando a ferramenta **Inspecionar** ou obter informações mais detalhadas com sobreposições persistentes.</span><span class="sxs-lookup"><span data-stu-id="6d652-148">Display a simplified grid overlay using the **Inspect** tool, or get more detailed information with persistent overlays.</span></span>  
*   <span data-ttu-id="6d652-149">Para habilitar sobreposições de grade persistentes, escolha o ícone de grade ao lado de um elemento contêiner de grade na ferramenta **Elementos** ou escolha a grade na **ferramenta Layout.**</span><span class="sxs-lookup"><span data-stu-id="6d652-149">To enable persistent grid overlays, choose the grid icon next to a grid container element in the **Elements** tool or choose the grid in the **Layout** tool.</span></span>  
*   <span data-ttu-id="6d652-150">Você pode habilitar sobreposições persistentes para várias grades.</span><span class="sxs-lookup"><span data-stu-id="6d652-150">You may enable persistent overlays for multiple grids.</span></span>  
*   <span data-ttu-id="6d652-151">A nova **ferramenta Layout** permite alternar facilmente sobreposições de grade e configurar a aparência e o conteúdo para cada um.</span><span class="sxs-lookup"><span data-stu-id="6d652-151">The new **Layout** tool allows you to easily toggle grid overlays and configure the appearance and the content for each.</span></span>  
    
<span data-ttu-id="6d652-152">Os recursos são aados por padrão.</span><span class="sxs-lookup"><span data-stu-id="6d652-152">The features are turned on by default.</span></span>  <span data-ttu-id="6d652-153">Para obter mais informações sobre os recursos, navegue até [grades CSS][DevtoolsCssGrid].</span><span class="sxs-lookup"><span data-stu-id="6d652-153">For more information about the features, navigate to [CSS grids][DevtoolsCssGrid].</span></span>  <span data-ttu-id="6d652-154">Para revisar o histórico desse recurso no Chromium de código aberto, navegue até Problema [#1047356][CR1047356].</span><span class="sxs-lookup"><span data-stu-id="6d652-154">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1047356][CR1047356].</span></span>  <span data-ttu-id="6d652-155">Além disso, Microsoft Edge equipe do DevTools está colaborando com a equipe do Chrome DevTools e Chromium comunidade para adicionar novos recursos de ferramentas de flexbox ao DevTools.</span><span class="sxs-lookup"><span data-stu-id="6d652-155">Additionally, the Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new flexbox tooling features to DevTools.</span></span>  <span data-ttu-id="6d652-156">Para atualizações sobre ferramentas de flexbox no projeto Chromium de código aberto, navegue até Problema [#1136394][CR1136394].</span><span class="sxs-lookup"><span data-stu-id="6d652-156">For updates on flexbox tooling in the Chromium open-source project, navigate to Issue [#1136394][CR1136394].</span></span>  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Ferramenta de layout com grades" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   <span data-ttu-id="6d652-158">**Ferramenta de layout** com grades</span><span class="sxs-lookup"><span data-stu-id="6d652-158">**Layout** tool with grids</span></span>  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a><span data-ttu-id="6d652-159">Personalize os atalhos do teclado em Configurações</span><span class="sxs-lookup"><span data-stu-id="6d652-159">Customize keyboard shortcuts in Settings</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="6d652-161">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="6d652-161">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="6d652-162">Agora você pode personalizar o atalho do teclado para qualquer ação no DevTools.</span><span class="sxs-lookup"><span data-stu-id="6d652-162">You are now able to customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="6d652-163">Desde Microsoft Edge versão 84, você pode \*\*\*\* escolher entre as predefinições Visual Studio Code **e DevTools (padrão)** para [atalhos de teclado.][DevtoolsCustomizeShortcuts]</span><span class="sxs-lookup"><span data-stu-id="6d652-163">Since Microsoft Edge version 84, you are able to choose between **Visual Studio Code** and **DevTools (default)** presets for [keyboard shortcuts][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="6d652-164">A partir Microsoft Edge versão 87, você pode ativar o experimento Habilitar o **editor** de atalhos de teclado para personalizar ainda mais os [atalhos de teclado.][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]</span><span class="sxs-lookup"><span data-stu-id="6d652-164">Starting in Microsoft Edge version 87, you may turn on the **Enable keyboard shortcut editor** experiment to further [customize keyboard shortcuts][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools].</span></span>  

<span data-ttu-id="6d652-165">Para habilitar o experimento, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de Habilitar o editor de atalho do **teclado.**</span><span class="sxs-lookup"><span data-stu-id="6d652-165">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="6d652-166">Para obter mais informações sobre como personalizar e editar atalhos, navegue até Editar atalhos de teclado para qualquer ação no [DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools].</span><span class="sxs-lookup"><span data-stu-id="6d652-166">For more information about customizing and editing shortcuts, navigate to [Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools].</span></span>  <span data-ttu-id="6d652-167">Para revisar as atualizações em tempo real sobre esse recurso no Chromium de código aberto, navegue até Problema [#174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="6d652-167">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Atalho personalizado para pausar um script" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   <span data-ttu-id="6d652-169">Atalho personalizado para pausar um script</span><span class="sxs-lookup"><span data-stu-id="6d652-169">Custom shortcut for pausing a script</span></span>  
:::image-end:::  

## <a name="introducing-the-microsoft-edge-tools-for-visual-studio-code-extension"></a><span data-ttu-id="6d652-170">Apresentando o Microsoft Edge ferramentas para Visual Studio Code extensão</span><span class="sxs-lookup"><span data-stu-id="6d652-170">Introducing the Microsoft Edge Tools for Visual Studio Code extension</span></span>  

<span data-ttu-id="6d652-171">Os **elementos para Visual Studio Code** e **Rede** para Visual Studio Code extensões agora são mesclados nas novas ferramentas de desenvolvedor Microsoft Edge para Visual Studio Code [extensão.][VisualStudioCodeMarketplaceMsEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="6d652-171">The **Elements for Visual Studio Code** and **Network for Visual Studio Code** extensions are now merged into the new [Microsoft Edge Developer Tools for Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] extension.</span></span>  <span data-ttu-id="6d652-172">Use o Microsoft Edge DevTools para as seguintes atividades sem sair Microsoft Visual Studio Código.</span><span class="sxs-lookup"><span data-stu-id="6d652-172">Use the Microsoft Edge DevTools for the following activities without leaving Microsoft Visual Studio Code.</span></span>  

*   <span data-ttu-id="6d652-173">Depurar o DOM</span><span class="sxs-lookup"><span data-stu-id="6d652-173">Debug the DOM</span></span>  
*   <span data-ttu-id="6d652-174">Editar CSS</span><span class="sxs-lookup"><span data-stu-id="6d652-174">Edit CSS</span></span>  
*   <span data-ttu-id="6d652-175">Inspecionar tráfego de rede</span><span class="sxs-lookup"><span data-stu-id="6d652-175">Inspect network traffic</span></span>  

<span data-ttu-id="6d652-176">Com a extensão, Microsoft Edge, conecte-se a uma instância existente do navegador ou use um navegador sem cabeça diretamente do seu editor.</span><span class="sxs-lookup"><span data-stu-id="6d652-176">With the extension, launch Microsoft Edge, connect to an existing instance of the browser, or use a headless browser directly from your editor.</span></span>  <span data-ttu-id="6d652-177">Para começar a contribuir e [arquivar][GithubMicrosoftVscodeEdgeDevtools] problemas com seus comentários sobre essa extensão, navegue até o Microsoft Edge ferramentas de desenvolvedor para Visual Studio Code de GitHub.</span><span class="sxs-lookup"><span data-stu-id="6d652-177">To start contributing and filing issues with your feedback about this extension, navigate to the [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repo on GitHub.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Usando a extensão na captura de tela do modo de navegador completo" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         <span data-ttu-id="6d652-179">Usando a extensão na captura de tela do modo de navegador completo</span><span class="sxs-lookup"><span data-stu-id="6d652-179">Using the extension in full browser mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Usando a extensão na captura de tela do modo sem cabeça" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         <span data-ttu-id="6d652-181">Usando a extensão na captura de tela do modo sem cabeça</span><span class="sxs-lookup"><span data-stu-id="6d652-181">Using the extension in headless mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="6d652-182">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="6d652-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-webauthn-tool"></a><span data-ttu-id="6d652-183">Nova ferramenta WebAuthn</span><span class="sxs-lookup"><span data-stu-id="6d652-183">New WebAuthn tool</span></span>  

<span data-ttu-id="6d652-184">Em versões anteriores do Microsoft Edge, não havia suporte para depuração webAuthn nativa.</span><span class="sxs-lookup"><span data-stu-id="6d652-184">In earlier versions of Microsoft Edge, there was no native WebAuthn debugging support.</span></span>  <span data-ttu-id="6d652-185">Você precisava de autenticadores físicos para testar seu aplicativo Web com a [API de Autenticação da Web.][GithubW3cWebauthn]</span><span class="sxs-lookup"><span data-stu-id="6d652-185">You needed physical authenticators to test your web application with the [Web Authentication API][GithubW3cWebauthn].</span></span>  <span data-ttu-id="6d652-186">Com a nova **ferramenta WebAuthn,** você pode fazer as seguintes ações sem o uso de autenticadores físicos.</span><span class="sxs-lookup"><span data-stu-id="6d652-186">With the new **WebAuthn** tool, you are able to do the following actions without the use of any physical authenticators.</span></span>

*   <span data-ttu-id="6d652-187">Emular autenticadores</span><span class="sxs-lookup"><span data-stu-id="6d652-187">Emulate authenticators</span></span>
*   <span data-ttu-id="6d652-188">Personalizar atributos de autenticadores</span><span class="sxs-lookup"><span data-stu-id="6d652-188">Customize attributes of authenticators</span></span>
*   <span data-ttu-id="6d652-189">Inspecionar estados de autenticadores</span><span class="sxs-lookup"><span data-stu-id="6d652-189">Inspect states of authenticators</span></span>
    
<span data-ttu-id="6d652-190">Para obter mais informações sobre o recurso **WebAuthn,** navegue até [Emular autenticadores e depurar WebAuthn no Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span><span class="sxs-lookup"><span data-stu-id="6d652-190">For more information about the **WebAuthn** feature, navigate to [Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span></span>  

<span data-ttu-id="6d652-191">Você pode emular autenticadores e depurar a API de Autenticação da [Web][GithubW3cWebauthn] com a nova ferramenta [WebAuthn][DevtoolsWebauthnIndex].</span><span class="sxs-lookup"><span data-stu-id="6d652-191">You are able to emulate authenticators and debug the [Web Authentication API][GithubW3cWebauthn] with the new [WebAuthn][DevtoolsWebauthnIndex] tool.</span></span>  <span data-ttu-id="6d652-192">Para abrir a **ferramenta WebAuthn,** escolha o ícone Personalizar e controlar **DevTools** \( \) > `...` Mais **ferramentas**  >  **WebAuthn**.</span><span class="sxs-lookup"><span data-stu-id="6d652-192">To open the **WebAuthn** tool, choose **the Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  <span data-ttu-id="6d652-193">Para revisar as atualizações em tempo real sobre esse recurso no Chromium de código aberto, navegue até Problema [#1034663][CR1034663].</span><span class="sxs-lookup"><span data-stu-id="6d652-193">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1034663][CR1034663].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Abra a ferramenta WebAuthn" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         <span data-ttu-id="6d652-195">Abra a **ferramenta WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="6d652-195">Open the **WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Ferramenta WebAuthn" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         <span data-ttu-id="6d652-197">**Ferramenta WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="6d652-197">**WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="elements-tool-updates"></a><span data-ttu-id="6d652-198">Atualizações da ferramenta Elementos</span><span class="sxs-lookup"><span data-stu-id="6d652-198">Elements tool updates</span></span>  

#### <a name="view-the-computed-sidebar-pane-in-the-styles-pane"></a><span data-ttu-id="6d652-199">Exibir o painel da barra lateral Computada no painel Estilos</span><span class="sxs-lookup"><span data-stu-id="6d652-199">View the Computed sidebar pane in the Styles pane</span></span>  

<span data-ttu-id="6d652-200">Alterne o **painel Computed** no painel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="6d652-200">Toggle the **Computed** pane in the **Styles** pane.</span></span>  <span data-ttu-id="6d652-201">O **painel Computado** no painel **Estilos** é recolhido por padrão.</span><span class="sxs-lookup"><span data-stu-id="6d652-201">The **Computed** pane in the **Styles** pane is collapsed by default.</span></span>  <span data-ttu-id="6d652-202">Para alternar, escolha o botão.</span><span class="sxs-lookup"><span data-stu-id="6d652-202">To toggle it, choose the button.</span></span>  <span data-ttu-id="6d652-203">Para revisar as atualizações em tempo real sobre esse recurso no projeto Chromium de código aberto, navegue até Problema [#1073899][CR1073899].</span><span class="sxs-lookup"><span data-stu-id="6d652-203">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1073899][CR1073899].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Abra o painel da barra lateral Computada" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         <span data-ttu-id="6d652-205">Abra o **painel da barra lateral** Computada</span><span class="sxs-lookup"><span data-stu-id="6d652-205">Open the **Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Painel de barras laterais calculado" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         <span data-ttu-id="6d652-207">**Painel de barras laterais** calculado</span><span class="sxs-lookup"><span data-stu-id="6d652-207">**Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="grouping-css-properties-in-the-computed-panel"></a><span data-ttu-id="6d652-208">Agrupando propriedades CSS no painel Computado</span><span class="sxs-lookup"><span data-stu-id="6d652-208">Grouping CSS properties in the Computed panel</span></span>  

<span data-ttu-id="6d652-209">Para exibir o CSS aplicado com menos rolagem, agrupar as propriedades CSS por categorias no painel **Computed.**</span><span class="sxs-lookup"><span data-stu-id="6d652-209">To view your applied CSS with less scrolling, group the CSS properties by categories in the **Computed** pane.</span></span>  <span data-ttu-id="6d652-210">Você também pode se concentrar seletivamente em um conjunto de propriedades relacionadas enquanto inspeciona seu CSS.</span><span class="sxs-lookup"><span data-stu-id="6d652-210">You may also selectively focus on a set of related properties while you inspect your CSS.</span></span>  <span data-ttu-id="6d652-211">Na ferramenta **Elementos,** escolha um elemento.</span><span class="sxs-lookup"><span data-stu-id="6d652-211">From the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="6d652-212">Para agrupar \(ou desagrupar\) as propriedades CSS, alterne a **caixa de** seleção Grupo.</span><span class="sxs-lookup"><span data-stu-id="6d652-212">To group \(or ungroup\) the CSS properties, toggle the **Group** checkbox.</span></span>  <span data-ttu-id="6d652-213">Para revisar as atualizações em tempo real sobre esse recurso no projeto Chromium de código aberto, navegue até Problemas [#1096230,][CR1096230] [#1084673][CR1084673]e [#1106251][CR1106251].</span><span class="sxs-lookup"><span data-stu-id="6d652-213">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1096230][CR1096230], [#1084673][CR1084673], and [#1106251][CR1106251].</span></span>  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Agrupando propriedades CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   <span data-ttu-id="6d652-215">Agrupando propriedades CSS</span><span class="sxs-lookup"><span data-stu-id="6d652-215">Grouping CSS properties</span></span>  
:::image-end:::  

### <a name="lighthouse-64-in-the-lighthouse-tool"></a><span data-ttu-id="6d652-216">Farol 6.4 na ferramenta Doleiro</span><span class="sxs-lookup"><span data-stu-id="6d652-216">Lighthouse 6.4 in the Lighthouse tool</span></span>  

<span data-ttu-id="6d652-217">A **ferramenta Doleiro** agora está executando o Farol 6.4.</span><span class="sxs-lookup"><span data-stu-id="6d652-217">The **Lighthouse** tool is now running Lighthouse 6.4.</span></span>  <span data-ttu-id="6d652-218">Para uma lista completa de alterações, navegue até as notas [de versão do Farol.][GithubGoogleChromeLighthouseReleasesV641]</span><span class="sxs-lookup"><span data-stu-id="6d652-218">For a full list of changes, navigate to the [Lighthouse release notes][GithubGoogleChromeLighthouseReleasesV641].</span></span>  <span data-ttu-id="6d652-219">Para analisar as atualizações em tempo real sobre esse recurso no Chromium de código aberto, navegue até Problema [#772558][CR772558].</span><span class="sxs-lookup"><span data-stu-id="6d652-219">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#772558][CR772558].</span></span>  

### <a name="performancemark-events-in-the-timings-section"></a><span data-ttu-id="6d652-220">eventos performance.mark() na seção Timings</span><span class="sxs-lookup"><span data-stu-id="6d652-220">performance.mark() events in the Timings section</span></span>  

<span data-ttu-id="6d652-221">A **seção Timings** de uma gravação na ferramenta [Performance][DevtoolsEvaluatePerformanceReference] agora marca `performance.mark()` eventos.</span><span class="sxs-lookup"><span data-stu-id="6d652-221">The **Timings section** of a recording in the [Performance][DevtoolsEvaluatePerformanceReference] tool now marks `performance.mark()` events.</span></span>  <span data-ttu-id="6d652-222">Para experimentar esse recurso e medir o desempenho do código JavaScript, adicione `performance.mark()` eventos ao seu código.</span><span class="sxs-lookup"><span data-stu-id="6d652-222">To try this feature and measure the performance of your JavaScript code, add `performance.mark()` events to your code.</span></span>  <span data-ttu-id="6d652-223">Por exemplo, o trecho de código a seguir adiciona marcadores antes e depois de um loop que itera de 0 a `for` 1000 usando incrementos de 7.</span><span class="sxs-lookup"><span data-stu-id="6d652-223">For example, the following code snippet adds markers before and after a `for` loop that iterates from 0 to 1000 using increments of 7.</span></span>  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

<span data-ttu-id="6d652-224">Em seguida, abra [a ferramenta Performance][DevtoolsEvaluatePerformanceReference] e navegue até a seção **Timings** para gravar seu código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6d652-224">Then, open the [Performance][DevtoolsEvaluatePerformanceReference] tool and navigate to the **Timings section** to record your JavaScript code.</span></span>  <span data-ttu-id="6d652-225">Os `performance.mark()` eventos adicionados agora são exibidos na gravação.</span><span class="sxs-lookup"><span data-stu-id="6d652-225">The `performance.mark()` events you added are now displayed in the recording.</span></span>  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Eventos Performance.mark" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` <span data-ttu-id="6d652-227">events</span><span class="sxs-lookup"><span data-stu-id="6d652-227">events</span></span>  
:::image-end:::  

### <a name="new-resource-type-and-url-filters-in-the-network-tool"></a><span data-ttu-id="6d652-228">Novos filtros de url e tipo de recurso na ferramenta Rede</span><span class="sxs-lookup"><span data-stu-id="6d652-228">New resource-type and url filters in the Network tool</span></span>  

<span data-ttu-id="6d652-229">Use as novas `resource-type` e `url` palavras-chave na ferramenta **Rede** para filtrar solicitações de rede.</span><span class="sxs-lookup"><span data-stu-id="6d652-229">Use the new `resource-type` and `url` keywords in the **Network** tool to filter network requests.</span></span>  <span data-ttu-id="6d652-230">Por exemplo, use `resource-type:image` para se concentrar nas solicitações de rede que são imagens.</span><span class="sxs-lookup"><span data-stu-id="6d652-230">For example, use `resource-type:image` to focus on the network requests that are images.</span></span>  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="filtro de tipo de recurso" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   <span data-ttu-id="6d652-232">filtro de tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="6d652-232">resource-type filter</span></span>  
:::image-end:::  

<span data-ttu-id="6d652-233">Para descobrir palavras-chave mais especiais, como e , navegue até `resource-type` `url` [filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties].</span><span class="sxs-lookup"><span data-stu-id="6d652-233">To discover more special keywords such as `resource-type` and `url`, navigate to [filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties].</span></span>  <span data-ttu-id="6d652-234">Para analisar as atualizações em tempo real sobre esse recurso no projeto Chromium de código aberto, navegue até Problemas [#1121141][CR1121141] e [#1104188][CR1104188].</span><span class="sxs-lookup"><span data-stu-id="6d652-234">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1121141][CR1121141] and [#1104188][CR1104188].</span></span>  

### <a name="frame-details-view-updates"></a><span data-ttu-id="6d652-235">Atualizações da exibição de detalhes do quadro</span><span class="sxs-lookup"><span data-stu-id="6d652-235">Frame details view updates</span></span>  

#### <a name="display-coep-and-coop-reporting-to-endpoint"></a><span data-ttu-id="6d652-236">Exibir relatórios de COEP e COOP para o ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="6d652-236">Display COEP and COOP reporting to endpoint</span></span>  

<span data-ttu-id="6d652-237">Exibir o ponto de extremidade Política de Embedder entre Origens \(COEP\) e Política de Abertura entre Origens \(COOP\) na seção Isolamento de Segurança `reporting to` **&.**</span><span class="sxs-lookup"><span data-stu-id="6d652-237">View the Cross-Origin Embedder Policy \(COEP\) and Cross-Origin Opener Policy \(COOP\) `reporting to` endpoint under the **Security & Isolation** section.</span></span>  <span data-ttu-id="6d652-238">A [API de][MdnReportingApi] Relatório define , um novo cabeçalho HTTP, que oferece uma maneira de especificar os pontos de extremidade do servidor para o navegador enviar `Report-To` avisos e erros.</span><span class="sxs-lookup"><span data-stu-id="6d652-238">The [Reporting API][MdnReportingApi] defines `Report-To`, a new HTTP header, that gives you a way to specify the server endpoints for the browser to send warnings and errors.</span></span>  <span data-ttu-id="6d652-239">Para analisar as atualizações em tempo real sobre esse recurso no Chromium de código aberto, navegue até Problema [#1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="6d652-239">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="O relatório para o ponto de extremidade" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   <span data-ttu-id="6d652-241">O `reporting to` ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="6d652-241">The `reporting to` endpoint</span></span>  
:::image-end:::  

#### <a name="display-coep-and-coop-report-only-mode"></a><span data-ttu-id="6d652-242">Exibir o modo somente relatório COEP e COOP</span><span class="sxs-lookup"><span data-stu-id="6d652-242">Display COEP and COOP report-only mode</span></span>  

<span data-ttu-id="6d652-243">DevTools agora exibe o `report-only` rótulo para COEP e COOP que estão definidos como `report-only` modo.</span><span class="sxs-lookup"><span data-stu-id="6d652-243">DevTools now display the `report-only` label for COEP and COOP that are set to `report-only` mode.</span></span>  <span data-ttu-id="6d652-244">Para analisar as atualizações em tempo real sobre esse recurso no Chromium de código aberto, navegue até Problema [#1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="6d652-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="O rótulo de modo somente relatório" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   <span data-ttu-id="6d652-246">O `report-only` rótulo de modo</span><span class="sxs-lookup"><span data-stu-id="6d652-246">The `report-only` mode label</span></span>  
:::image-end:::  

### <a name="view-and-fix-color-contrast-issues-in-the-css-overview-tool"></a><span data-ttu-id="6d652-247">Exibir e corrigir problemas de contraste de cor na ferramenta Visão Geral css</span><span class="sxs-lookup"><span data-stu-id="6d652-247">View and fix color contrast issues in the CSS Overview tool</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="6d652-249">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="6d652-249">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="6d652-250">A **ferramenta Visão geral** css agora exibe uma lista de elementos em sua página que têm problemas de contraste de cor.</span><span class="sxs-lookup"><span data-stu-id="6d652-250">The **CSS Overview** tool now displays a list of elements on your page that have color contrast issues.</span></span>  <span data-ttu-id="6d652-251">A página de demonstração a seguir tem um exemplo de um problema de contraste de cor.</span><span class="sxs-lookup"><span data-stu-id="6d652-251">The following demo page has an example of a color contrast issue.</span></span>  

[<span data-ttu-id="6d652-252">Demonstração de cores acessíveis de visão geral css</span><span class="sxs-lookup"><span data-stu-id="6d652-252">CSS Overview Accessible Colors Demo</span></span>][GlitchCssOverviewAccessibleColorsDemo]  

<span data-ttu-id="6d652-253">Para habilitar esse experimento, **em Configurações**  >  **Experimentos,** escolha a caixa de seleção Visão geral **css.**</span><span class="sxs-lookup"><span data-stu-id="6d652-253">To enable this experiment, under **Settings** > **Experiments**, choose the **CSS Overview** checkbox.</span></span>  <span data-ttu-id="6d652-254">Para exibir uma lista de elementos que têm um problema de contraste de cor, em Problemas **de contraste,** escolha **Texto**.</span><span class="sxs-lookup"><span data-stu-id="6d652-254">To view a list of elements that have a color contrast issue, on **Contrast issues**, choose **Text**.</span></span>  <span data-ttu-id="6d652-255">Para abrir o elemento na ferramenta **Elementos,** escolha um elemento na lista.</span><span class="sxs-lookup"><span data-stu-id="6d652-255">To open the element in the **Elements** tool, choose an element in the list.</span></span>  <span data-ttu-id="6d652-256">Para ajudar a corrigir problemas de contraste, o Microsoft Edge DevTools [fornece automaticamente sugestões de cores][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span><span class="sxs-lookup"><span data-stu-id="6d652-256">To help fix contrast issues, the Microsoft Edge DevTools [automatically provide color suggestions][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span></span>  <span data-ttu-id="6d652-257">Para revisar as atualizações em tempo real sobre esse recurso no projeto Chromium de código aberto, navegue até Problema [#1120316][CR1120316].</span><span class="sxs-lookup"><span data-stu-id="6d652-257">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1120316][CR1120316].</span></span>  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Problemas de contraste de cor baixa" lightbox="../../media/2020/10/css-overview.msft.png":::
   <span data-ttu-id="6d652-259">Problemas de contraste de cor baixa</span><span class="sxs-lookup"><span data-stu-id="6d652-259">Low color contrast issues</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="6d652-260">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6d652-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="6d652-261">Se você estiver no Windows ou macOS, considere usar os canais [Microsoft Edge de][MicrosoftEdgePreviewChannels] visualização como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="6d652-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="6d652-262">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="6d652-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="6d652-263">Como entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6d652-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsTool]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Deprecation do painel Propriedades na ferramenta Elementos - Novidades no DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Recursos de depuração de grade CSS - Novidades no DevTools (Microsoft Edge 85) | Microsoft Docs"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Sugestão de cores acessíveis no painel Estilos - Novidades no DevTools (Microsoft Edge 86) | Microsoft Docs"  

[DevtoolsConsoleIndex]: ../../../console/index.md "Use o console | Microsoft Docs"  
[DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]:  ../../../console/utilities.md#recently-chosen-element-or-javascript-object "Elemento ou objeto JavaScript escolhido recentemente - Referência da API de Utilitários de Console | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personalize os atalhos do teclado no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../../../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Editar atalhos de teclado para qualquer ação no devTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReference]: ../../../evaluate-performance/reference.md "Referência de análise de desempenho | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: ../../../experimental-features/index.md#emulation-support-dual-screen-mode "Emulação: suporte ao modo de tela dupla - Recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: ../../../experimental-features.md#enable-experimental-apis "Habilitar APIs experimentais - Recursos experimentais | Microsoft Docs"  
<!--  [DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: ../../../experimental-features/index.md#enable-keyboard-shortcut-editor "Enable keyboard shortcut editor - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: .. /.. /.. /experimental-features/index.md#enable-new-css-grid-debugging-features "Emulation: Support dual screen mode - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: .. /.. /.. /experimental-features/index.md#enable-network-console "Enable Network Console - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: .. /.. /.. /experimental-features/index.md#enable-source-order-viewer "Enable Source Order Viewer - Experimental features | Microsoft Docs&quot; [DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: .. /.. /.. /experimental-features/index.md#testing-on-foldable-and-dual-screen-devices &quot;Testing on foldable and dual-screen devices - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: .. /.. /.. /experimental-features/index.md#turn-on-experimental-features "Ativar recursos experimentais - Recursos experimentais | Microsoft Docs"  
[DevtoolsConsoleApiTable]: .. /.. /.. /console/api.md#table "table - Console API reference | Microsoft Docs"  
[DevtoolsCoverageIndex]: .. /.. /.. /coverage/index.md "Encontre código JavaScript e CSS nãousado com a guia Cobertura em Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssGrid]: .. /.. /.. /css/grid.md "Inspecionar grade CSS | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: .. /.. /.. /customize/index.md#drawer "Drawer - Personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: .. /.. /.. /customize/index.md#settings "Configurações - Personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: .. /.. /.. /evaluate-performance/reference.md#analyze-rendering-performance-with-the-rendering-tab "Analisar o desempenho da renderização com a guia Renderização - Referência de Análise de Desempenho | Microsoft Docs"  
[DevtoolsMediaIndex]: .. /.. /.. /media/index.md "Exibir e depurar informações de jogadores de mídia | Microsoft Docs"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: .. /.. /.. /network/reference.md#filter-requests-by-properties "Filter requests by properties - Network Analysis reference | Microsoft Docs"  
[DevtoolsWebauthnIndex]: .. /.. /.. /webauthn/index.md "Emular autenticadores e depurar WebAuthn no Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de visualização do Microsoft Edge"  

[VisualStudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Ferramentas para Visual Studio Code | Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros do Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: Permitir personalizar atalhos de teclado/vinculações de teclas | Chromium bugs"
[CR772558]: https://crbug.com/772558 "DevTools: atualizar para a versão mais recente do | Chromium bugs"  
[CR1034663]: https://crbug.com/1034663 "Criar um front-end para a API de Teste webAuthn | Chromium bugs"  
[CR1047356]: https://crbug.com/1047356 "Css Grid/Flexbox/Table tooling | Chromium bugs"  
[CR1051466]: https://crbug.com/1051466 "Suporte à depuração DE COOP/COEP no DevTools | Chromium bugs"  
[CR1073899]: https://crbug.com/1073899 "A guia Estilo Calculado desaparece no modo responsivo | Chromium bugs"  
[CR1075732]: https://crbug.com/1075732 "Personalização de DevTools - Guias móveis | Chromium bugs"  
[CR1084673]: https://crbug.com/1084673 "DevTools: melhore a maneira como apresentamos propriedades personalizadas CSS ((aka). Variáveis CSS) e seus valores | Chromium bugs"  
[CR1093687]: https://crbug.com/1093687 "Criar ferramenta para criar e repetir solicitações de rede sintéticas | Chromium bugs"  
[CR1096230]: https://crbug.com/1096230 "Propriedades CSS de grupo por categorias no painel Estilos Calculados | Chromium bugs"  
[CR1104188]: https://crbug.com/1104188 "A pesquisa da ferramenta de rede não encontra resultados ao pesquisar por url completa | Chromium bugs"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: melhorar a guia Estilos Calculados | Chromium bugs"  
[CR1120316]: https://crbug.com/1120316 "Realça o contraste ruim em Css Overview > Colors | Chromium Bugs"  
[CR1121141]: https://crbug.com/1121141 "Permitir a filtragem por tipo de recurso no log de rede | Chromium bugs"  
[CR1121312]: https://crbug.com/1121312 "Configurações deve ser removido do menu Mais Ferramentas | Chromium bugs"  
[CR1136394]: https://crbug.com/1136394 "Ferramentas do Flexbox | Chromium Bugs"  
[CR1136655]: https://crbug.com/1136655 "Devtools: Localização V2 | Chromium bugs"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "Relatórios de API | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v6.4.1 - GoogleChrome/| GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticação da Web | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Olá! | Glitch"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Formato da coleção Postman v2.1.0 | Postman"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "Especificação do OpenAPI | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> <span data-ttu-id="6d652-316">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6d652-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6d652-317">A página original é encontrada [aqui](https://developer.chrome.com/blog/new-in-devtools-87) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="6d652-317">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-87) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6d652-319">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6d652-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
