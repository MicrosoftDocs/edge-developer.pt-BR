---
description: Novas ferramentas de depuração de Grade CSS, ferramenta Webauthn, ferramentas moveizáveis e painel da barra lateral Computada.
title: Novidades no DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/26/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 88e6678880172a7a494bcf73c74874aeb70c24b9
ms.sourcegitcommit: e737277744dd25a7585c113eef22a2aa4d4c167f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "11325956"
---
# <span data-ttu-id="b91e5-104">Novidades no DevTools (Microsoft Edge 87)</span><span class="sxs-lookup"><span data-stu-id="b91e5-104">What's New In DevTools (Microsoft Edge 87)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="b91e5-105">Melhorar a localização do DevTools</span><span class="sxs-lookup"><span data-stu-id="b91e5-105">Improving DevTools localization</span></span>  

<span data-ttu-id="b91e5-106">Para atender às suas necessidades de tradução, a equipe do Microsoft Edge DevTools se concentra em melhorar a qualidade da tradução.</span><span class="sxs-lookup"><span data-stu-id="b91e5-106">To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.</span></span>  <span data-ttu-id="b91e5-107">A partir da versão 87 do Microsoft Edge, várias cadeias de caracteres e termos são bloqueados e não mudam mesmo quando o restante do DevTools é exibido em outros idiomas.</span><span class="sxs-lookup"><span data-stu-id="b91e5-107">Starting in Microsoft Edge version 87, several strings and terms are locked and do not change even when the rest of the DevTools are displayed in other languages.</span></span>  <span data-ttu-id="b91e5-108">A lista de cadeias de caracteres e termos afetados inclui o seguinte.</span><span class="sxs-lookup"><span data-stu-id="b91e5-108">The list of affected strings and terms include the following.</span></span>  

*   <span data-ttu-id="b91e5-109">As cadeias de caracteres na **ferramenta Desdoo.**</span><span class="sxs-lookup"><span data-stu-id="b91e5-109">The strings in the **Lighthouse** tool.</span></span>  
*   <span data-ttu-id="b91e5-110">O termo `service worker` .</span><span class="sxs-lookup"><span data-stu-id="b91e5-110">The term `service worker`.</span></span>  
*   <span data-ttu-id="b91e5-111">Alguns dos **filtros da** ferramenta de `URL` rede, como , e `XHR` `JS` `CSS` .</span><span class="sxs-lookup"><span data-stu-id="b91e5-111">Some of the **Network** tool filters such as `URL`, `XHR`, `JS`, and `CSS`.</span></span>  
*   <span data-ttu-id="b91e5-112">A API de Utilitários de Console [$0.][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]</span><span class="sxs-lookup"><span data-stu-id="b91e5-112">The [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] Console Utilities API.</span></span>  
    
<span data-ttu-id="b91e5-113">[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] agora está disponível no [Console](/microsoft-edge/devtools-guide-chromium/console/index.md) para usuários em versões localizadas do DevTools.</span><span class="sxs-lookup"><span data-stu-id="b91e5-113">[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] is now available in the [Console](/microsoft-edge/devtools-guide-chromium/console/index.md) for users on localized versions of the DevTools.</span></span>   <span data-ttu-id="b91e5-114">Obrigado à comunidade global de desenvolvedores por ajudar a melhorar a localização do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="b91e5-114">Thank you to the global developer community for helping improve localization of the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="b91e5-115">Continue a [enviar comentários sobre a qualidade de localização](#getting-in-touch-with-microsoft-edge-devtools-team) para melhorar o suporte para o DevTools em todas as localidades.</span><span class="sxs-lookup"><span data-stu-id="b91e5-115">Continue to [send feedback on localization quality](#getting-in-touch-with-microsoft-edge-devtools-team) to improve support for DevTools in all locales.</span></span>  <span data-ttu-id="b91e5-116">Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até Problema [#1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="b91e5-116">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Ferramenta de rede com filtros não localizados" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   <span data-ttu-id="b91e5-118">**Painel** de rede com filtros não localizados</span><span class="sxs-lookup"><span data-stu-id="b91e5-118">**Network** pane with non-localized filters</span></span>  
:::image-end:::  

## <span data-ttu-id="b91e5-119">Mover ferramentas entre os painéis superior e inferior</span><span class="sxs-lookup"><span data-stu-id="b91e5-119">Move tools between top and bottom panels</span></span>  

<span data-ttu-id="b91e5-120">O DevTools agora dá suporte à movimentação de ferramentas entre os painéis superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="b91e5-120">DevTools now supports moving tools between the top and bottom panels.</span></span>  <span data-ttu-id="b91e5-121">Personalize o DevTools e melhore sua produtividade exibindo qualquer combinação de duas ferramentas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="b91e5-121">Customize your DevTools and improve your productivity by viewing any combination of two tools at the same time.</span></span>  <span data-ttu-id="b91e5-122">Por exemplo, ex view the **Elements** and the **Sources** tools at the same time \(by moving the **Sources** tool to the bottom\).</span><span class="sxs-lookup"><span data-stu-id="b91e5-122">For example, view the **Elements** and the **Sources** tools at the same time \(by moving the **Sources** tool to the bottom\).</span></span>  <span data-ttu-id="b91e5-123">Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [#1075732][CR1075732].</span><span class="sxs-lookup"><span data-stu-id="b91e5-123">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1075732][CR1075732].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b91e5-124">Para mover qualquer ferramenta superior para a parte inferior, passe o mouse sobre uma guia, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Mover para **baixo.**</span><span class="sxs-lookup"><span data-stu-id="b91e5-124">To move any top tool to the bottom, hover on a tab, open the contextual menu \(right-click\), and choose **Move to bottom**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Mover para baixo" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         <span data-ttu-id="b91e5-126">Mover para baixo</span><span class="sxs-lookup"><span data-stu-id="b91e5-126">Move to bottom</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="b91e5-127">Para mover qualquer ferramenta inferior para a parte superior, passe o mouse sobre uma guia, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Mover para cima.**</span><span class="sxs-lookup"><span data-stu-id="b91e5-127">To move any bottom tool to the top, hover on a tab, open the contextual menu \(right-click\), and choose **Move to top**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Mover para o topo" lightbox="../../media/2020/10/move-to-top.msft.png":::
         <span data-ttu-id="b91e5-129">Mover para o topo</span><span class="sxs-lookup"><span data-stu-id="b91e5-129">Move to top</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <span data-ttu-id="b91e5-130">Salvar e exportar usando o Console de Rede</span><span class="sxs-lookup"><span data-stu-id="b91e5-130">Save and export using the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="b91e5-132">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="b91e5-132">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="b91e5-133">A **ferramenta Console de** Rede agora melhorou a compatibilidade com os esquemas [Postman v2.1][PostmanSchemaJsonCollectionv210Index] e [OpenAPI v2.][SwaggerSpecificationV2]</span><span class="sxs-lookup"><span data-stu-id="b91e5-133">The **Network Console** tool now has improved compatibility with the [Postman v2.1][PostmanSchemaJsonCollectionv210Index] and [OpenAPI v2][SwaggerSpecificationV2] schemas.</span></span>  <span data-ttu-id="b91e5-134">Para habilitar o experimento, navegue até Ativar [recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **Habilitar Console de Rede.**</span><span class="sxs-lookup"><span data-stu-id="b91e5-134">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Network Console**.</span></span>  <span data-ttu-id="b91e5-135">Para obter mais informações sobre o **Console de Rede,** navegue até [Habilitar o recurso Experimental do Console de Rede.][DevtoolsExperimentalFeaturesEnableNetworkConsole]</span><span class="sxs-lookup"><span data-stu-id="b91e5-135">For more information about the **Network Console**, navigate to [Enable Network Console Experimental feature][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span></span>  <span data-ttu-id="b91e5-136">Esse experimento agora dá suporte às ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="b91e5-136">This experiment now supports the following actions.</span></span>  

*   <span data-ttu-id="b91e5-137">Salvar e exportar coleções e ambientes.</span><span class="sxs-lookup"><span data-stu-id="b91e5-137">Save and export Collections and Environments.</span></span>  
*   <span data-ttu-id="b91e5-138">Edite e exporte conjuntos de variáveis de ambiente na ferramenta **Console de** Rede.</span><span class="sxs-lookup"><span data-stu-id="b91e5-138">Edit and export sets of environment variables within the **Network Console** tool.</span></span>  
    
<span data-ttu-id="b91e5-139">Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até [Problema #1093687][CR1093687].</span><span class="sxs-lookup"><span data-stu-id="b91e5-139">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1093687][CR1093687].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Insira o nome do novo ambiente" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         <span data-ttu-id="b91e5-141">Insira o nome do novo ambiente</span><span class="sxs-lookup"><span data-stu-id="b91e5-141">Enter name for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Escolher formato para o novo ambiente" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         <span data-ttu-id="b91e5-143">Escolher formato para o novo ambiente</span><span class="sxs-lookup"><span data-stu-id="b91e5-143">Choose format for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="b91e5-144">Ferramentas de grade CSS aprimoradas</span><span class="sxs-lookup"><span data-stu-id="b91e5-144">Improved CSS Grid tooling</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="b91e5-146">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="b91e5-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="b91e5-147">O Microsoft Edge DevTools agora oferece suporte aos seguintes recursos para inspecionar, exibir e depurar suas grades CSS.</span><span class="sxs-lookup"><span data-stu-id="b91e5-147">The Microsoft Edge DevTools now support the following features for inspecting, viewing, and debugging your CSS grids.</span></span>  

*   <span data-ttu-id="b91e5-148">Exibir uma sobreposição de grade simplificada usando a ferramenta **Inspect** ou obter informações mais detalhadas com sobreposições persistentes.</span><span class="sxs-lookup"><span data-stu-id="b91e5-148">Display a simplified grid overlay using the **Inspect** tool, or get more detailed information with persistent overlays.</span></span>  
*   <span data-ttu-id="b91e5-149">Para habilitar sobreposições de grade persistentes, escolha o ícone de grade ao lado de um elemento de contêiner de grade na ferramenta **Elementos** ou escolha a grade na ferramenta **Layout.**</span><span class="sxs-lookup"><span data-stu-id="b91e5-149">To enable persistent grid overlays, choose the grid icon next to a grid container element in the **Elements** tool or choose the grid in the **Layout** tool.</span></span>  
*   <span data-ttu-id="b91e5-150">Você pode habilitar sobreposições persistentes para várias grades.</span><span class="sxs-lookup"><span data-stu-id="b91e5-150">You may enable persistent overlays for multiple grids.</span></span>  
*   <span data-ttu-id="b91e5-151">A nova **ferramenta Layout** permite que você alterne facilmente sobreposições de grade e configure a aparência e o conteúdo de cada uma delas.</span><span class="sxs-lookup"><span data-stu-id="b91e5-151">The new **Layout** tool allows you to easily toggle grid overlays and configure the appearance and the content for each.</span></span>  
    
<span data-ttu-id="b91e5-152">Os recursos estão ligado por padrão.</span><span class="sxs-lookup"><span data-stu-id="b91e5-152">The features are turned on by default.</span></span>  <span data-ttu-id="b91e5-153">Para obter mais informações sobre os recursos, navegue até [grades CSS.][DevtoolsCssGrid]</span><span class="sxs-lookup"><span data-stu-id="b91e5-153">For more information about the features, navigate to [CSS grids][DevtoolsCssGrid].</span></span>  <span data-ttu-id="b91e5-154">Para revisar o histórico desse recurso no projeto de código aberto do Chromium, navegue até Problema [#1047356][CR1047356].</span><span class="sxs-lookup"><span data-stu-id="b91e5-154">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1047356][CR1047356].</span></span>  <span data-ttu-id="b91e5-155">Além disso, a equipe do Microsoft Edge DevTools está colaborando com a equipe do Chrome DevTools e a comunidade do Chromium para adicionar novos recursos de ferramentas do Flexbox ao DevTools.</span><span class="sxs-lookup"><span data-stu-id="b91e5-155">Additionally, the Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new flexbox tooling features to DevTools.</span></span>  <span data-ttu-id="b91e5-156">Para atualizações sobre ferramentas de flexbox no projeto de software livre do Chromium, navegue até [Problema #1136394][CR1136394].</span><span class="sxs-lookup"><span data-stu-id="b91e5-156">For updates on flexbox tooling in the Chromium open-source project, navigate to Issue [#1136394][CR1136394].</span></span>  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Ferramenta de layout com grades" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   <span data-ttu-id="b91e5-158">**Ferramenta de layout** com grades</span><span class="sxs-lookup"><span data-stu-id="b91e5-158">**Layout** tool with grids</span></span>  
:::image-end:::  

## <span data-ttu-id="b91e5-159">Personalizar atalhos de teclado em Configurações</span><span class="sxs-lookup"><span data-stu-id="b91e5-159">Customize keyboard shortcuts in Settings</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="b91e5-161">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="b91e5-161">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="b91e5-162">Agora você pode personalizar o atalho do teclado para qualquer ação no DevTools.</span><span class="sxs-lookup"><span data-stu-id="b91e5-162">You are now able to customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="b91e5-163">Desde a versão 84 do Microsoft Edge, você pode escolher entre predefinições do **Visual Studio Code** e do **DevTools (padrão)** para [atalhos de teclado.][DevtoolsCustomizeShortcuts]</span><span class="sxs-lookup"><span data-stu-id="b91e5-163">Since Microsoft Edge version 84, you are able to choose between **Visual Studio Code** and **DevTools (default)** presets for [keyboard shortcuts][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="b91e5-164">A partir da versão 87 do Microsoft Edge, você pode ativar o experimento de editor de atalhos de teclado **Habilitar** para personalizar ainda mais [os atalhos de teclado.][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]</span><span class="sxs-lookup"><span data-stu-id="b91e5-164">Starting in Microsoft Edge version 87, you may turn on the **Enable keyboard shortcut editor** experiment to further [customize keyboard shortcuts][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="b91e5-165">Para habilitar o experimento, navegue até Ativar recursos [experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **Habilitar o editor de atalho do teclado.**</span><span class="sxs-lookup"><span data-stu-id="b91e5-165">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="b91e5-166">Para obter mais informações sobre como personalizar e editar atalhos, acesse o [recurso experimental do editor de atalhos de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="b91e5-166">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  <span data-ttu-id="b91e5-167">Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até Problema [#174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="b91e5-167">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Atalho personalizado para pausar um script" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   <span data-ttu-id="b91e5-169">Atalho personalizado para pausar um script</span><span class="sxs-lookup"><span data-stu-id="b91e5-169">Custom shortcut for pausing a script</span></span>  
:::image-end:::  

## <span data-ttu-id="b91e5-170">Apresentando a extensão do Microsoft Edge Tools for Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b91e5-170">Introducing the Microsoft Edge Tools for Visual Studio Code extension</span></span>  

<span data-ttu-id="b91e5-171">Os **elementos para o Visual Studio Code** e a rede para **extensões do Visual Studio Code** agora são mesclados na nova extensão Microsoft Edge Developer Tools para Visual Studio [Code.][VisualStudioCodeMarketplaceMsEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="b91e5-171">The **Elements for Visual Studio Code** and **Network for Visual Studio Code** extensions are now merged into the new [Microsoft Edge Developer Tools for Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] extension.</span></span>  <span data-ttu-id="b91e5-172">Use o Microsoft Edge DevTools para as seguintes atividades sem sair do Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="b91e5-172">Use the Microsoft Edge DevTools for the following activities without leaving Visual Studio Code.</span></span>  

*   <span data-ttu-id="b91e5-173">Depurar o DOM</span><span class="sxs-lookup"><span data-stu-id="b91e5-173">Debug the DOM</span></span>  
*   <span data-ttu-id="b91e5-174">Editar CSS</span><span class="sxs-lookup"><span data-stu-id="b91e5-174">Edit CSS</span></span>  
*   <span data-ttu-id="b91e5-175">Inspecionar o tráfego de rede</span><span class="sxs-lookup"><span data-stu-id="b91e5-175">Inspect network traffic</span></span>  

<span data-ttu-id="b91e5-176">Com a extensão, launch Microsoft Edge, connect to an existing instance of the browser, or use a headless browser directly from your editor.</span><span class="sxs-lookup"><span data-stu-id="b91e5-176">With the extension, launch Microsoft Edge, connect to an existing instance of the browser, or use a headless browser directly from your editor.</span></span>  <span data-ttu-id="b91e5-177">Para começar a contribuir e registrar problemas com seus comentários sobre essa extensão, navegue até o repositório microsoft [Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] no GitHub.</span><span class="sxs-lookup"><span data-stu-id="b91e5-177">To start contributing and filing issues with your feedback about this extension, navigate to the [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repo on GitHub.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Usando a extensão no modo de navegador completo captura de tela" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         <span data-ttu-id="b91e5-179">Usando a extensão no modo de navegador completo captura de tela</span><span class="sxs-lookup"><span data-stu-id="b91e5-179">Using the extension in full browser mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Using the extension in headless mode screenshot" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         <span data-ttu-id="b91e5-181">Using the extension in headless mode screenshot</span><span class="sxs-lookup"><span data-stu-id="b91e5-181">Using the extension in headless mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="b91e5-182">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="b91e5-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="b91e5-183">Nova ferramenta WebAuthn</span><span class="sxs-lookup"><span data-stu-id="b91e5-183">New WebAuthn tool</span></span>  

<span data-ttu-id="b91e5-184">Em versões anteriores do Microsoft Edge, não havia suporte nativo de depuração WebAuthn.</span><span class="sxs-lookup"><span data-stu-id="b91e5-184">In earlier versions of Microsoft Edge, there was no native WebAuthn debugging support.</span></span>  <span data-ttu-id="b91e5-185">Você precisava de autenticadores físicos para testar seu aplicativo Web com a [API de Autenticação da Web.][GithubW3cWebauthn]</span><span class="sxs-lookup"><span data-stu-id="b91e5-185">You needed physical authenticators to test your web application with the [Web Authentication API][GithubW3cWebauthn].</span></span>  <span data-ttu-id="b91e5-186">Com a nova **ferramenta WebAuthn,** você pode fazer as seguintes ações sem o uso de autenticadores físicos.</span><span class="sxs-lookup"><span data-stu-id="b91e5-186">With the new **WebAuthn** tool, you are able to do the following actions without the use of any physical authenticators.</span></span>

*   <span data-ttu-id="b91e5-187">Emular autenticadores</span><span class="sxs-lookup"><span data-stu-id="b91e5-187">Emulate authenticators</span></span>
*   <span data-ttu-id="b91e5-188">Personalizar atributos de autenticadores</span><span class="sxs-lookup"><span data-stu-id="b91e5-188">Customize attributes of authenticators</span></span>
*   <span data-ttu-id="b91e5-189">Inspecionar estados de autenticadores</span><span class="sxs-lookup"><span data-stu-id="b91e5-189">Inspect states of authenticators</span></span>
    
<span data-ttu-id="b91e5-190">Para obter mais informações sobre o recurso **WebAuthn,** navegue até [Emular autenticadores e depurar WebAuthn no Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span><span class="sxs-lookup"><span data-stu-id="b91e5-190">For more information about the **WebAuthn** feature, navigate to [Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span></span>  

<span data-ttu-id="b91e5-191">Você pode emular autenticadores e depurar a API de Autenticação da [Web][GithubW3cWebauthn] com a nova [ferramenta WebAuthn.][DevtoolsWebauthnIndex]</span><span class="sxs-lookup"><span data-stu-id="b91e5-191">You are able to emulate authenticators and debug the [Web Authentication API][GithubW3cWebauthn] with the new [WebAuthn][DevtoolsWebauthnIndex] tool.</span></span>  <span data-ttu-id="b91e5-192">Para abrir a **ferramenta WebAuthn,** escolha o ícone Personalizar e controlar **o DevTools** \( \) > `...` Mais **ferramentas**  >  **WebAuthn**.</span><span class="sxs-lookup"><span data-stu-id="b91e5-192">To open the **WebAuthn** tool, choose **the Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  <span data-ttu-id="b91e5-193">Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até Problema [#1034663][CR1034663].</span><span class="sxs-lookup"><span data-stu-id="b91e5-193">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1034663][CR1034663].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Abra a ferramenta WebAuthn" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         <span data-ttu-id="b91e5-195">Abra a **ferramenta WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="b91e5-195">Open the **WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Ferramenta WebAuthn" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         <span data-ttu-id="b91e5-197">**Ferramenta WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="b91e5-197">**WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b91e5-198">Atualizações da ferramenta Elementos</span><span class="sxs-lookup"><span data-stu-id="b91e5-198">Elements tool updates</span></span>  

#### <span data-ttu-id="b91e5-199">Exibir o painel barra lateral Computado no painel Estilos</span><span class="sxs-lookup"><span data-stu-id="b91e5-199">View the Computed sidebar pane in the Styles pane</span></span>  

<span data-ttu-id="b91e5-200">Alterne o **painel Computed** no **painel** Estilos.</span><span class="sxs-lookup"><span data-stu-id="b91e5-200">Toggle the **Computed** pane in the **Styles** pane.</span></span>  <span data-ttu-id="b91e5-201">O **painel Computed** no painel **Estilos** é recolhido por padrão.</span><span class="sxs-lookup"><span data-stu-id="b91e5-201">The **Computed** pane in the **Styles** pane is collapsed by default.</span></span>  <span data-ttu-id="b91e5-202">Para alternar, escolha o botão.</span><span class="sxs-lookup"><span data-stu-id="b91e5-202">To toggle it, choose the button.</span></span>  <span data-ttu-id="b91e5-203">Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até [Problema #1073899][CR1073899].</span><span class="sxs-lookup"><span data-stu-id="b91e5-203">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1073899][CR1073899].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Abrir o painel barra lateral Computado" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         <span data-ttu-id="b91e5-205">Abrir o **painel barra lateral** Computado</span><span class="sxs-lookup"><span data-stu-id="b91e5-205">Open the **Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Painel da barra lateral computado" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         <span data-ttu-id="b91e5-207">**Painel da barra lateral** computado</span><span class="sxs-lookup"><span data-stu-id="b91e5-207">**Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="b91e5-208">Agrupar propriedades CSS no painel computado</span><span class="sxs-lookup"><span data-stu-id="b91e5-208">Grouping CSS properties in the Computed panel</span></span>  

<span data-ttu-id="b91e5-209">Para exibir o CSS aplicado com menos rolagem, a agrupar as propriedades CSS por categorias no **painel** Computed.</span><span class="sxs-lookup"><span data-stu-id="b91e5-209">To view your applied CSS with less scrolling, group the CSS properties by categories in the **Computed** pane.</span></span>  <span data-ttu-id="b91e5-210">Você também pode se concentrar seletivamente em um conjunto de propriedades relacionadas enquanto inspeciona seu CSS.</span><span class="sxs-lookup"><span data-stu-id="b91e5-210">You may also selectively focus on a set of related properties while you inspect your CSS.</span></span>  <span data-ttu-id="b91e5-211">Na ferramenta **Elementos,** escolha um elemento.</span><span class="sxs-lookup"><span data-stu-id="b91e5-211">From the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="b91e5-212">Para agrupar \(ou desagrupar\) as propriedades CSS, alterne a **caixa de seleção** Grupo.</span><span class="sxs-lookup"><span data-stu-id="b91e5-212">To group \(or ungroup\) the CSS properties, toggle the **Group** checkbox.</span></span>  <span data-ttu-id="b91e5-213">Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até Problemas [#1096230][CR1096230], [#1084673][CR1084673]e [#1106251][CR1106251].</span><span class="sxs-lookup"><span data-stu-id="b91e5-213">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1096230][CR1096230], [#1084673][CR1084673], and [#1106251][CR1106251].</span></span>  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Agrupar propriedades CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   <span data-ttu-id="b91e5-215">Agrupar propriedades CSS</span><span class="sxs-lookup"><span data-stu-id="b91e5-215">Grouping CSS properties</span></span>  
:::image-end:::  

### <span data-ttu-id="b91e5-216">6.4 da Ferramenta Desdoo</span><span class="sxs-lookup"><span data-stu-id="b91e5-216">Lighthouse 6.4 in the Lighthouse tool</span></span>  

<span data-ttu-id="b91e5-217">A **ferramenta Desdois** agora está executando o 6.4 do 6.4.</span><span class="sxs-lookup"><span data-stu-id="b91e5-217">The **Lighthouse** tool is now running Lighthouse 6.4.</span></span>  <span data-ttu-id="b91e5-218">Para uma lista completa de alterações, navegue até as notas de [versão do Filme.][GithubGoogleChromeLighthouseReleasesV641]</span><span class="sxs-lookup"><span data-stu-id="b91e5-218">For a full list of changes, navigate to the [Lighthouse release notes][GithubGoogleChromeLighthouseReleasesV641].</span></span>  <span data-ttu-id="b91e5-219">Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até Problema [#772558][CR772558].</span><span class="sxs-lookup"><span data-stu-id="b91e5-219">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#772558][CR772558].</span></span>  

### <span data-ttu-id="b91e5-220">eventos performance.mark() na seção Timings</span><span class="sxs-lookup"><span data-stu-id="b91e5-220">performance.mark() events in the Timings section</span></span>  

<span data-ttu-id="b91e5-221">A **seção Timings de** uma gravação na ferramenta [Desempenho][DevtoolsGuideChromiumEvaluatePerformanceReference] agora marca `performance.mark()` eventos.</span><span class="sxs-lookup"><span data-stu-id="b91e5-221">The **Timings section** of a recording in the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool now marks `performance.mark()` events.</span></span>  <span data-ttu-id="b91e5-222">Para testar esse recurso e medir o desempenho do código JavaScript, adicione `performance.mark()` eventos ao seu código.</span><span class="sxs-lookup"><span data-stu-id="b91e5-222">To try this feature and measure the performance of your JavaScript code, add `performance.mark()` events to your code.</span></span>  <span data-ttu-id="b91e5-223">Por exemplo, o trecho de código a seguir adiciona marcadores antes e depois de um loop que itera de 0 a `for` 1000 usando incrementos de 7.</span><span class="sxs-lookup"><span data-stu-id="b91e5-223">For example, the following code snippet adds markers before and after a `for` loop that iterates from 0 to 1000 using increments of 7.</span></span>  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

<span data-ttu-id="b91e5-224">Em seguida, abra [a ferramenta Desempenho][DevtoolsGuideChromiumEvaluatePerformanceReference] e navegue até a seção **Timings** para registrar seu código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b91e5-224">Then, open the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool and navigate to the **Timings section** to record your JavaScript code.</span></span>  <span data-ttu-id="b91e5-225">Os `performance.mark()` eventos adicionados agora são exibidos na gravação.</span><span class="sxs-lookup"><span data-stu-id="b91e5-225">The `performance.mark()` events you added are now displayed in the recording.</span></span>  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Eventos Performance.mark" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` <span data-ttu-id="b91e5-227">events</span><span class="sxs-lookup"><span data-stu-id="b91e5-227">events</span></span>  
:::image-end:::  

### <span data-ttu-id="b91e5-228">Novos filtros de URL e tipo de recurso na ferramenta Rede</span><span class="sxs-lookup"><span data-stu-id="b91e5-228">New resource-type and url filters in the Network tool</span></span>  

<span data-ttu-id="b91e5-229">Use o novo e `resource-type` as `url` palavras-chave na ferramenta **Rede** para filtrar solicitações de rede.</span><span class="sxs-lookup"><span data-stu-id="b91e5-229">Use the new `resource-type` and `url` keywords in the **Network** tool to filter network requests.</span></span>  <span data-ttu-id="b91e5-230">Por exemplo, use `resource-type:image` para se concentrar nas solicitações de rede que são imagens.</span><span class="sxs-lookup"><span data-stu-id="b91e5-230">For example, use `resource-type:image` to focus on the network requests that are images.</span></span>  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="filtro de tipo de recurso" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   <span data-ttu-id="b91e5-232">filtro de tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="b91e5-232">resource-type filter</span></span>  
:::image-end:::  

<span data-ttu-id="b91e5-233">Para descobrir mais palavras-chave especiais, como `resource-type` `url` e, navegue até [filtrar solicitações por propriedades.][DevtoolsNetworkReferenceFilterRequestsProperties]</span><span class="sxs-lookup"><span data-stu-id="b91e5-233">To discover more special keywords such as `resource-type` and `url`, navigate to [filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties].</span></span>  <span data-ttu-id="b91e5-234">Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até Problemas [#1121141][CR1121141] e [#1104188][CR1104188].</span><span class="sxs-lookup"><span data-stu-id="b91e5-234">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1121141][CR1121141] and [#1104188][CR1104188].</span></span>  

### <span data-ttu-id="b91e5-235">Atualizações da exibição de detalhes do quadro</span><span class="sxs-lookup"><span data-stu-id="b91e5-235">Frame details view updates</span></span>  

#### <span data-ttu-id="b91e5-236">Exibir relatórios COEP e COD para o ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="b91e5-236">Display COEP and COOP reporting to endpoint</span></span>  

<span data-ttu-id="b91e5-237">Exibir o ponto de extremidade Política de Inserção entre Origens \(COEP\) e Política de Abertura entre Origens \(ÂMBITO\) na seção Isolamento de `reporting to` **& Segurança.**</span><span class="sxs-lookup"><span data-stu-id="b91e5-237">View the Cross-Origin Embedder Policy \(COEP\) and Cross-Origin Opener Policy \(COOP\) `reporting to` endpoint under the **Security & Isolation** section.</span></span>  <span data-ttu-id="b91e5-238">A [API de Relatórios][MdnReportingApi] define , um novo cabeçalho HTTP, que oferece uma maneira de especificar os pontos de extremidade do servidor para o navegador enviar `Report-To` avisos e erros.</span><span class="sxs-lookup"><span data-stu-id="b91e5-238">The [Reporting API][MdnReportingApi] defines `Report-To`, a new HTTP header, that gives you a way to specify the server endpoints for the browser to send warnings and errors.</span></span>  <span data-ttu-id="b91e5-239">Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até Problema [#1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="b91e5-239">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="O relatório para o ponto de extremidade" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   <span data-ttu-id="b91e5-241">O `reporting to` ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="b91e5-241">The `reporting to` endpoint</span></span>  
:::image-end:::  

#### <span data-ttu-id="b91e5-242">Exibir o modo somente relatório COEP e COD</span><span class="sxs-lookup"><span data-stu-id="b91e5-242">Display COEP and COOP report-only mode</span></span>  

<span data-ttu-id="b91e5-243">O DevTools agora exibe `report-only` o rótulo para COEP e COD que estão definidos para `report-only` o modo.</span><span class="sxs-lookup"><span data-stu-id="b91e5-243">DevTools now display the `report-only` label for COEP and COOP that are set to `report-only` mode.</span></span>  <span data-ttu-id="b91e5-244">Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até Problema [#1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="b91e5-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="O rótulo do modo somente relatório" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   <span data-ttu-id="b91e5-246">O `report-only` rótulo do modo</span><span class="sxs-lookup"><span data-stu-id="b91e5-246">The `report-only` mode label</span></span>  
:::image-end:::  

### <span data-ttu-id="b91e5-247">Exibir e corrigir problemas de contraste de cor na ferramenta de Visão Geral do CSS</span><span class="sxs-lookup"><span data-stu-id="b91e5-247">View and fix color contrast issues in the CSS Overview tool</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="b91e5-249">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="b91e5-249">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="b91e5-250">A **ferramenta De visão** geral do CSS agora exibe uma lista de elementos em sua página que têm problemas de contraste de cor.</span><span class="sxs-lookup"><span data-stu-id="b91e5-250">The **CSS Overview** tool now displays a list of elements on your page that have color contrast issues.</span></span>  <span data-ttu-id="b91e5-251">A página de demonstração a seguir tem um exemplo de um problema de contraste de cor.</span><span class="sxs-lookup"><span data-stu-id="b91e5-251">The following demo page has an example of a color contrast issue.</span></span>  

[<span data-ttu-id="b91e5-252">Demonstração de cores acessíveis da visão geral do CSS</span><span class="sxs-lookup"><span data-stu-id="b91e5-252">CSS Overview Accessible Colors Demo</span></span>][GlitchCssOverviewAccessibleColorsDemo]  

<span data-ttu-id="b91e5-253">Para habilitar \*\*\*\* esse experimento, em  >  **Experimentos de Configurações,** escolha a caixa de seleção Visão Geral do **CSS.**</span><span class="sxs-lookup"><span data-stu-id="b91e5-253">To enable this experiment, under **Settings** > **Experiments**, choose the **CSS Overview** checkbox.</span></span>  <span data-ttu-id="b91e5-254">Para exibir uma lista de elementos que têm um problema de contraste de cor, **em**questões de contraste, escolha **Texto**.</span><span class="sxs-lookup"><span data-stu-id="b91e5-254">To view a list of elements that have a color contrast issue, on **Contrast issues**, choose **Text**.</span></span>  <span data-ttu-id="b91e5-255">Para abrir o elemento na ferramenta **Elementos,** escolha um elemento na lista.</span><span class="sxs-lookup"><span data-stu-id="b91e5-255">To open the element in the **Elements** tool, choose an element in the list.</span></span>  <span data-ttu-id="b91e5-256">Para ajudar a corrigir problemas de contraste, o Microsoft Edge DevTools [fornece sugestões de cor automaticamente.][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]</span><span class="sxs-lookup"><span data-stu-id="b91e5-256">To help fix contrast issues, the Microsoft Edge DevTools [automatically provide color suggestions][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span></span>  <span data-ttu-id="b91e5-257">Para revisar as atualizações em tempo real sobre esse recurso no projeto de software livre do Chromium, navegue até [Problema #1120316][CR1120316].</span><span class="sxs-lookup"><span data-stu-id="b91e5-257">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1120316][CR1120316].</span></span>  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Problemas de baixo contraste de cor" lightbox="../../media/2020/10/css-overview.msft.png":::
   <span data-ttu-id="b91e5-259">Problemas de baixo contraste de cor</span><span class="sxs-lookup"><span data-stu-id="b91e5-259">Low color contrast issues</span></span>  
:::image-end:::  

## <span data-ttu-id="b91e5-260">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b91e5-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="b91e5-261">Se você estiver no Windows ou no macOS, considere usar os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="b91e5-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="b91e5-262">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="b91e5-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="b91e5-263">Como entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b91e5-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Preterição do painel Propriedades na ferramenta Elementos - Novidades no DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Recursos de depuração de grade CSS - Novidades no DevTools (Microsoft Edge 85) | Microsoft Docs"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Sugestão de cores acessíveis no painel Estilos - Novidades no DevTools (Microsoft Edge 86) | Microsoft Docs"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Elemento selecionado recentemente ou objeto JavaScript - referência de API de utilitários de console | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalizar atalhos de teclado no microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Referência de análise de | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Emulação: Suporte ao modo de tela dupla - recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Habilitar APIs experimentais - recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Habilitar o editor de atalhos de teclado - recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulação: Suporte ao modo de tela dupla - recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Habilitar o Console de Rede - recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Habilitar o Visualizador de Ordem de Origem - Recursos experimentais | Microsoft Docs"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Teste em dispositivos de tela dupla e dobráveis - recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Ativar recursos experimentais - recursos experimentais | Microsoft Docs"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "tabela - Referência da API do Console | Microsoft Docs"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Encontre código CSS e JavaScript não em uso com a guia Cobertura no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Inspecionar grade CSS | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Gaveta - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analisar o desempenho de renderização com a guia Renderização - Performance Analysis Reference | Microsoft Docs"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Exibir e depurar informações de media players | Microsoft Docs"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Filter requests by properties - Network Analysis reference | Microsoft Docs"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Emular autenticadores e depurar WebAuthn no Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de Visualização do Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros do Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: permitir personalizar atalhos de teclado/vinculações de teclas | Bugs do Chromium"
[CR772558]: https://crbug.com/772558 "DevTools: atualização para a versão mais recente do | Bugs do Chromium"  
[CR1034663]: https://crbug.com/1034663 "Criar um front-end para a API de teste do WebAuthn | Bugs do Chromium"  
[CR1047356]: https://crbug.com/1047356 "Css Grid/Flexbox/Table tooling | Bugs do Chromium"  
[CR1051466]: https://crbug.com/1051466 "Suporte à depuração DEM/COEP no DevTools | Bugs do Chromium"  
[CR1073899]: https://crbug.com/1073899 "A guia Estilo Calculado desaparece no modo responsivo | Bugs do Chromium"  
[CR1075732]: https://crbug.com/1075732 "Personalização do DevTools - guias removíveis | Bugs do Chromium"  
[CR1084673]: https://crbug.com/1084673 "DevTools: melhorar a maneira como apresentamos propriedades personalizadas css (também conhecidas). Variáveis CSS) e seus valores | Bugs do Chromium"  
[CR1093687]: https://crbug.com/1093687 "Criar uma ferramenta para criar e repetir solicitações de rede sintéticas | Bugs do Chromium"  
[CR1096230]: https://crbug.com/1096230 "Agrupar propriedades CSS por categorias no painel Estilos Calculados | Bugs do Chromium"  
[CR1104188]: https://crbug.com/1104188 "A pesquisa da ferramenta de rede não encontra resultados ao pesquisar por URL completa | Bugs do Chromium"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: melhorar a guia Estilos Calculados | Bugs do Chromium"  
[CR1120316]: https://crbug.com/1120316 "Realça o contraste ruim em Visão geral de CSS > cores | Chromium Bugs"  
[CR1121141]: https://crbug.com/1121141 "Permitir a filtragem por tipo de recurso no log de rede | Bugs do Chromium"  
[CR1121312]: https://crbug.com/1121312 "As configurações devem ser removidas do menu Mais Ferramentas | Bugs do Chromium"  
[CR1136394]: https://crbug.com/1136394 "Ferramentas do Flexbox | Chromium Bugs"  
[CR1136655]: https://crbug.com/1136655 "Devtools: localização V2 | Bugs do Chromium"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "Relatório api | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v6.4.1 - GoogleChrome/| GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticação da Web | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Olá! | Falha"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Formato da coleção Postman v2.1.0 | Postman"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "Especificação OpenAPI | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> <span data-ttu-id="b91e5-316">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b91e5-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b91e5-317">A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/10/devtools/index) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="b91e5-317">The original page is found [here](https://developers.google.com/web/updates/2020/10/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b91e5-319">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b91e5-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
