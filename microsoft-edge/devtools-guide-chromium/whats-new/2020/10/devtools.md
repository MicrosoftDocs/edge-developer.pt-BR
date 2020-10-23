---
description: Nova ferramentas de depuração de grade CSS, ferramenta webauthn, ferramentas móveis e painel da barra lateral calculada.
title: O que há de novo no DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 0e4b1972918797d69e2068236f6d1336c54cc858
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/23/2020
ms.locfileid: "11133915"
---
# <span data-ttu-id="544ac-104">O que há de novo no DevTools (Microsoft Edge 87)</span><span class="sxs-lookup"><span data-stu-id="544ac-104">What's New In DevTools (Microsoft Edge 87)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="544ac-105">Melhorando a localização do DevTools</span><span class="sxs-lookup"><span data-stu-id="544ac-105">Improving DevTools localization</span></span>  

<span data-ttu-id="544ac-106">Para atender às suas necessidades de tradução, a equipe do Microsoft Edge DevTools tem o foco em melhorar a qualidade da tradução.</span><span class="sxs-lookup"><span data-stu-id="544ac-106">To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.</span></span>  <span data-ttu-id="544ac-107">A partir do Microsoft Edge versão 87, várias cadeias de caracteres e termos são bloqueados e não são alterados mesmo quando o restante da DevTools são exibidos em outros idiomas.</span><span class="sxs-lookup"><span data-stu-id="544ac-107">Starting in Microsoft Edge version 87, several strings and terms are locked and do not change even when the rest of the DevTools are displayed in other languages.</span></span>  <span data-ttu-id="544ac-108">A lista de cadeias de caracteres e termos afetados inclui o seguinte.</span><span class="sxs-lookup"><span data-stu-id="544ac-108">The list of affected strings and terms include the following.</span></span>  

*   <span data-ttu-id="544ac-109">As cadeias de caracteres na ferramenta **Lighthouse** .</span><span class="sxs-lookup"><span data-stu-id="544ac-109">The strings in the **Lighthouse** tool.</span></span>  
*   <span data-ttu-id="544ac-110">O termo `service worker` .</span><span class="sxs-lookup"><span data-stu-id="544ac-110">The term `service worker`.</span></span>  
*   <span data-ttu-id="544ac-111">Alguns filtros da ferramenta de **rede** , como `URL` , `XHR` , `JS` e `CSS` .</span><span class="sxs-lookup"><span data-stu-id="544ac-111">Some of the **Network** tool filters such as `URL`, `XHR`, `JS`, and `CSS`.</span></span>  
*   <span data-ttu-id="544ac-112">API de utilitários de console do [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] .</span><span class="sxs-lookup"><span data-stu-id="544ac-112">The [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] Console Utilities API.</span></span>  
    
<span data-ttu-id="544ac-113">o [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] agora está disponível no [console](/microsoft-edge/devtools-guide-chromium/console/index.md) para usuários em versões localizadas do devtools.</span><span class="sxs-lookup"><span data-stu-id="544ac-113">[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] is now available in the [Console](/microsoft-edge/devtools-guide-chromium/console/index.md) for users on localized versions of the DevTools.</span></span>   <span data-ttu-id="544ac-114">Obrigado à comunidade de desenvolvedores globais para ajudar a melhorar a localização do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="544ac-114">Thank you to the global developer community for helping improve localization of the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="544ac-115">Continue a [enviar comentários sobre a qualidade de localização](#getting-in-touch-with-microsoft-edge-devtools-team) para melhorar o suporte para devtools em todas as localidades.</span><span class="sxs-lookup"><span data-stu-id="544ac-115">Continue to [send feedback on localization quality](#getting-in-touch-with-microsoft-edge-devtools-team) to improve support for DevTools in all locales.</span></span>  <span data-ttu-id="544ac-116">Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="544ac-116">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   <span data-ttu-id="544ac-118">Painel de **rede** com filtros não traduzidos</span><span class="sxs-lookup"><span data-stu-id="544ac-118">**Network** pane with non-localized filters</span></span>  
:::image-end:::  

## <span data-ttu-id="544ac-119">Mover ferramentas entre os painéis superior e inferior</span><span class="sxs-lookup"><span data-stu-id="544ac-119">Move tools between top and bottom panels</span></span>  

<span data-ttu-id="544ac-120">O DevTools agora oferece suporte a ferramentas de movimentação entre os painéis superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="544ac-120">DevTools now supports moving tools between the top and bottom panels.</span></span>  <span data-ttu-id="544ac-121">Personalize sua DevTools e melhore a produtividade ao exibir qualquer combinação de duas ferramentas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="544ac-121">Customize your DevTools and improve your productivity by viewing any combination of two tools at the same time.</span></span>  <span data-ttu-id="544ac-122">Por exemplo, exiba os **elementos** e as ferramentas de **fontes** ao mesmo tempo \ (movendo a ferramenta **fontes** para a parte inferior \).</span><span class="sxs-lookup"><span data-stu-id="544ac-122">For example, view the **Elements** and the **Sources** tools at the same time \(by moving the **Sources** tool to the bottom\).</span></span>  <span data-ttu-id="544ac-123">Para revisar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até Issue [#1075732][CR1075732].</span><span class="sxs-lookup"><span data-stu-id="544ac-123">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1075732][CR1075732].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="544ac-124">Para mover qualquer ferramenta de cima para baixo, passe o mouse sobre uma guia, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **mover para baixo**.</span><span class="sxs-lookup"><span data-stu-id="544ac-124">To move any top tool to the bottom, hover on a tab, open the contextual menu \(right-click\), and choose **Move to bottom**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         <span data-ttu-id="544ac-126">Mover para o fim</span><span class="sxs-lookup"><span data-stu-id="544ac-126">Move to bottom</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="544ac-127">Para mover qualquer ferramenta de cima para baixo, passe o mouse sobre uma guia, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **mover para o início**.</span><span class="sxs-lookup"><span data-stu-id="544ac-127">To move any bottom tool to the top, hover on a tab, open the contextual menu \(right-click\), and choose **Move to top**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/move-to-top.msft.png":::
         <span data-ttu-id="544ac-129">Mover para o início</span><span class="sxs-lookup"><span data-stu-id="544ac-129">Move to top</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <span data-ttu-id="544ac-130">Salvar e exportar usando o console de rede</span><span class="sxs-lookup"><span data-stu-id="544ac-130">Save and export using the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos":::
   <span data-ttu-id="544ac-132">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="544ac-132">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="544ac-133">A ferramenta de **console de rede** agora aumentou a compatibilidade com os esquemas do [postmaster v 2.1][PostmanSchemaJsonCollectionv210Index] e do [openapi v2][SwaggerSpecificationV2] .</span><span class="sxs-lookup"><span data-stu-id="544ac-133">The **Network Console** tool now has improved compatibility with the [Postman v2.1][PostmanSchemaJsonCollectionv210Index] and [OpenAPI v2][SwaggerSpecificationV2] schemas.</span></span>  <span data-ttu-id="544ac-134">Para habilitar o experimento, navegue até [ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **habilitar console de rede**.</span><span class="sxs-lookup"><span data-stu-id="544ac-134">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Network Console**.</span></span>  <span data-ttu-id="544ac-135">Para obter mais informações sobre o **console de rede**, navegue até habilitar o [recurso experimental do console de rede][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span><span class="sxs-lookup"><span data-stu-id="544ac-135">For more information about the **Network Console**, navigate to [Enable Network Console Experimental feature][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span></span>  <span data-ttu-id="544ac-136">Este experimento agora dá suporte às ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="544ac-136">This experiment now supports the following actions.</span></span>  

*   <span data-ttu-id="544ac-137">Salvar e exportar coletas e ambientes.</span><span class="sxs-lookup"><span data-stu-id="544ac-137">Save and export Collections and Environments.</span></span>  
*   <span data-ttu-id="544ac-138">Editar e exportar conjuntos de variáveis de ambiente dentro da ferramenta **console de rede** .</span><span class="sxs-lookup"><span data-stu-id="544ac-138">Edit and export sets of environment variables within the **Network Console** tool.</span></span>  
    
<span data-ttu-id="544ac-139">Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#1093687][CR1093687].</span><span class="sxs-lookup"><span data-stu-id="544ac-139">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1093687][CR1093687].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         <span data-ttu-id="544ac-141">Digite o nome do novo ambiente</span><span class="sxs-lookup"><span data-stu-id="544ac-141">Enter name for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         <span data-ttu-id="544ac-143">Escolher formato para o novo ambiente</span><span class="sxs-lookup"><span data-stu-id="544ac-143">Choose format for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="544ac-144">Ferramentas de grade CSS aprimoradas</span><span class="sxs-lookup"><span data-stu-id="544ac-144">Improved CSS Grid tooling</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos":::
   <span data-ttu-id="544ac-146">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="544ac-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="544ac-147">O Microsoft Edge DevTools agora oferece suporte aos recursos a seguir para inspecionar, exibir e depurar suas grades CSS.</span><span class="sxs-lookup"><span data-stu-id="544ac-147">The Microsoft Edge DevTools now support the following features for inspecting, viewing, and debugging your CSS grids.</span></span>  

*   <span data-ttu-id="544ac-148">Exiba uma sobreposição de grade simplificada usando a ferramenta **inspecionar** ou obter informações mais detalhadas com sobreposições persistentes.</span><span class="sxs-lookup"><span data-stu-id="544ac-148">Display a simplified grid overlay using the **Inspect** tool, or get more detailed information with persistent overlays.</span></span>  
*   <span data-ttu-id="544ac-149">Para habilitar sobreposições de grade persistente, escolha o ícone de grade ao lado de um elemento de contêiner de grade na ferramenta **elementos** ou escolha a grade na ferramenta de **layout** .</span><span class="sxs-lookup"><span data-stu-id="544ac-149">To enable persistent grid overlays, choose the grid icon next to a grid container element in the **Elements** tool or choose the grid in the **Layout** tool.</span></span>  
*   <span data-ttu-id="544ac-150">Você pode habilitar sobreposições persistentes para várias grades.</span><span class="sxs-lookup"><span data-stu-id="544ac-150">You may enable persistent overlays for multiple grids.</span></span>  
*   <span data-ttu-id="544ac-151">A nova ferramenta de **layout** permite que você alterne facilmente sobreposições de grade e configure a aparência e o conteúdo de cada um.</span><span class="sxs-lookup"><span data-stu-id="544ac-151">The new **Layout** tool allows you to easily toggle grid overlays and configure the appearance and the content for each.</span></span>  
    
<span data-ttu-id="544ac-152">Os recursos estão ativados por padrão.</span><span class="sxs-lookup"><span data-stu-id="544ac-152">The features are turned on by default.</span></span>  <span data-ttu-id="544ac-153">Para obter mais informações sobre os recursos, navegue até [grades CSS][DevtoolsCssGrid].</span><span class="sxs-lookup"><span data-stu-id="544ac-153">For more information about the features, navigate to [CSS grids][DevtoolsCssGrid].</span></span>  <span data-ttu-id="544ac-154">Para revisar o histórico desse recurso no projeto de fonte aberta do Chromium, navegue até Issue [#1047356][CR1047356].</span><span class="sxs-lookup"><span data-stu-id="544ac-154">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1047356][CR1047356].</span></span>  <span data-ttu-id="544ac-155">Além disso, a equipe do Microsoft Edge DevTools está colaborando com a equipe do Chrome DevTools e com a Comunidade da Chromium para adicionar novos recursos de ferramenta de flexbox ao DevTools.</span><span class="sxs-lookup"><span data-stu-id="544ac-155">Additionally, the Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new flexbox tooling features to DevTools.</span></span>  <span data-ttu-id="544ac-156">Para obter atualizações sobre a ferramenta flexbox no projeto de fonte aberta do Chromium, navegue até o Issue [#1136394][CR1136394].</span><span class="sxs-lookup"><span data-stu-id="544ac-156">For updates on flexbox tooling in the Chromium open-source project, navigate to Issue [#1136394][CR1136394].</span></span>  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   <span data-ttu-id="544ac-158">Ferramenta de **layout** com grades</span><span class="sxs-lookup"><span data-stu-id="544ac-158">**Layout** tool with grids</span></span>  
:::image-end:::  

## <span data-ttu-id="544ac-159">Personalizar atalhos de teclado em configurações</span><span class="sxs-lookup"><span data-stu-id="544ac-159">Customize keyboard shortcuts in Settings</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos":::
   <span data-ttu-id="544ac-161">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="544ac-161">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="544ac-162">Agora você pode personalizar o atalho de teclado para qualquer ação no DevTools.</span><span class="sxs-lookup"><span data-stu-id="544ac-162">You are now able to customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="544ac-163">Desde a versão 84 do Microsoft Edge, você pode escolher entre o **código do Visual Studio** e predefinições **devtools (padrão)** para [atalhos de teclado][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="544ac-163">Since Microsoft Edge version 84, you are able to choose between **Visual Studio Code** and **DevTools (default)** presets for [keyboard shortcuts][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="544ac-164">A partir da versão 87 do Microsoft Edge, você pode ativar o **Editor de atalhos de teclado** de teste para personalizar ainda mais os atalhos de [teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="544ac-164">Starting in Microsoft Edge version 87, you may turn on the **Enable keyboard shortcut editor** experiment to further [customize keyboard shortcuts][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="544ac-165">Para habilitar o experimento, navegue até [ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] e escolha a caixa de seleção ao lado de **habilitar o editor de atalhos de teclado**.</span><span class="sxs-lookup"><span data-stu-id="544ac-165">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="544ac-166">Para obter mais informações sobre como personalizar e editar atalhos, acesse o [recurso experimental do editor de atalhos de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="544ac-166">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  <span data-ttu-id="544ac-167">Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="544ac-167">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   <span data-ttu-id="544ac-169">Atalho personalizado para pausar um script</span><span class="sxs-lookup"><span data-stu-id="544ac-169">Custom shortcut for pausing a script</span></span>  
:::image-end:::  

## <span data-ttu-id="544ac-170">Apresentando a extensão de código do Microsoft Edge Tools para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="544ac-170">Introducing the Microsoft Edge Tools for Visual Studio Code extension</span></span>  

<span data-ttu-id="544ac-171">Os **elementos de código** e rede do Visual Studio **para extensões de código do Visual Studio** agora são mesclados nas novas [ferramentas de desenvolvedor do Microsoft Edge para extensão de código do Visual Studio][VisualStudioCodeMarketplaceMsEdgedevtools] .</span><span class="sxs-lookup"><span data-stu-id="544ac-171">The **Elements for Visual Studio Code** and **Network for Visual Studio Code** extensions are now merged into the new [Microsoft Edge Developer Tools for Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] extension.</span></span>  <span data-ttu-id="544ac-172">Use o Microsoft Edge DevTools para as seguintes atividades sem sair do código do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="544ac-172">Use the Microsoft Edge DevTools for the following activities without leaving Visual Studio Code.</span></span>  

*   <span data-ttu-id="544ac-173">Depurar o DOM</span><span class="sxs-lookup"><span data-stu-id="544ac-173">Debug the DOM</span></span>  
*   <span data-ttu-id="544ac-174">Editar CSS</span><span class="sxs-lookup"><span data-stu-id="544ac-174">Edit CSS</span></span>  
*   <span data-ttu-id="544ac-175">Inspecionar o tráfego de rede</span><span class="sxs-lookup"><span data-stu-id="544ac-175">Inspect network traffic</span></span>  

<span data-ttu-id="544ac-176">Com a extensão, inicie o Microsoft Edge, conecte-se a uma instância existente do navegador ou use um navegador sem cabeça diretamente do seu editor.</span><span class="sxs-lookup"><span data-stu-id="544ac-176">With the extension, launch Microsoft Edge, connect to an existing instance of the browser, or use a headless browser directly from your editor.</span></span>  <span data-ttu-id="544ac-177">Para começar a colaborar e arquivar problemas com seus comentários sobre essa extensão, navegue até as [ferramentas de desenvolvedor do Microsoft Edge para repositório de código do Visual Studio][GithubMicrosoftVscodeEdgeDevtools] no github.</span><span class="sxs-lookup"><span data-stu-id="544ac-177">To start contributing and filing issues with your feedback about this extension, navigate to the [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repo on GitHub.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         <span data-ttu-id="544ac-179">Usar a extensão na captura de tela do modo de navegador completo</span><span class="sxs-lookup"><span data-stu-id="544ac-179">Using the extension in full browser mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         <span data-ttu-id="544ac-181">Usar a extensão na captura de tela de modo sem periféricos</span><span class="sxs-lookup"><span data-stu-id="544ac-181">Using the extension in headless mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="544ac-182">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="544ac-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="544ac-183">Nova ferramenta webauthn</span><span class="sxs-lookup"><span data-stu-id="544ac-183">New WebAuthn tool</span></span>  

<span data-ttu-id="544ac-184">Em versões anteriores do Microsoft Edge, não havia nenhum suporte nativo à depuração webauthn.</span><span class="sxs-lookup"><span data-stu-id="544ac-184">In earlier versions of Microsoft Edge, there was no native WebAuthn debugging support.</span></span>  <span data-ttu-id="544ac-185">Você precisou de autenticadores físicos para testar seu aplicativo Web com a [API de autenticação da Web][GithubW3cWebauthn].</span><span class="sxs-lookup"><span data-stu-id="544ac-185">You needed physical authenticators to test your web application with the [Web Authentication API][GithubW3cWebauthn].</span></span>  <span data-ttu-id="544ac-186">Com a nova ferramenta **Webauthn** , você poderá executar as seguintes ações sem o uso de autenticadores físicos.</span><span class="sxs-lookup"><span data-stu-id="544ac-186">With the new **WebAuthn** tool, you are able to do the following actions without the use of any physical authenticators.</span></span>

*   <span data-ttu-id="544ac-187">Emular autenticadores</span><span class="sxs-lookup"><span data-stu-id="544ac-187">Emulate authenticators</span></span>
*   <span data-ttu-id="544ac-188">Personalizar atributos de autenticadores</span><span class="sxs-lookup"><span data-stu-id="544ac-188">Customize attributes of authenticators</span></span>
*   <span data-ttu-id="544ac-189">Inspecionar Estados de autenticadores</span><span class="sxs-lookup"><span data-stu-id="544ac-189">Inspect states of authenticators</span></span>
    
<span data-ttu-id="544ac-190">Para obter mais informações sobre o recurso **Webauthn** , navegue para [emular autenticadores e depurar webauthn no Microsoft Edge devtools][DevtoolsWebauthnIndex].</span><span class="sxs-lookup"><span data-stu-id="544ac-190">For more information about the **WebAuthn** feature, navigate to [Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span></span>  

<span data-ttu-id="544ac-191">Você pode emular autenticadores e depurar a API de [autenticação da Web][GithubW3cWebauthn] com a nova ferramenta [webauthn][DevtoolsWebauthnIndex] .</span><span class="sxs-lookup"><span data-stu-id="544ac-191">You are able to emulate authenticators and debug the [Web Authentication API][GithubW3cWebauthn] with the new [WebAuthn][DevtoolsWebauthnIndex] tool.</span></span>  <span data-ttu-id="544ac-192">Para abrir a ferramenta **webauthn** , escolha **o ícone Personalizar e controlar devtools** \ ( `...` \) > **mais ferramentas**  >  **webauthn**.</span><span class="sxs-lookup"><span data-stu-id="544ac-192">To open the **WebAuthn** tool, choose **the Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  <span data-ttu-id="544ac-193">Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#1034663][CR1034663].</span><span class="sxs-lookup"><span data-stu-id="544ac-193">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1034663][CR1034663].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         <span data-ttu-id="544ac-195">Abrir a ferramenta **Webauthn**</span><span class="sxs-lookup"><span data-stu-id="544ac-195">Open the **WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         <span data-ttu-id="544ac-197">Ferramenta **Webauthn**</span><span class="sxs-lookup"><span data-stu-id="544ac-197">**WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="544ac-198">Atualizações da ferramenta de elementos</span><span class="sxs-lookup"><span data-stu-id="544ac-198">Elements tool updates</span></span>  

#### <span data-ttu-id="544ac-199">Exibir o painel da barra lateral calculada no painel estilos</span><span class="sxs-lookup"><span data-stu-id="544ac-199">View the Computed sidebar pane in the Styles pane</span></span>  

<span data-ttu-id="544ac-200">Alternar o painel **calculado** no painel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="544ac-200">Toggle the **Computed** pane in the **Styles** pane.</span></span>  <span data-ttu-id="544ac-201">O painel **calculado** no painel **estilos** é recolhido por padrão.</span><span class="sxs-lookup"><span data-stu-id="544ac-201">The **Computed** pane in the **Styles** pane is collapsed by default.</span></span>  <span data-ttu-id="544ac-202">Para ativá-la, escolha o botão.</span><span class="sxs-lookup"><span data-stu-id="544ac-202">To toggle it, choose the button.</span></span>  <span data-ttu-id="544ac-203">Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#1073899][CR1073899].</span><span class="sxs-lookup"><span data-stu-id="544ac-203">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1073899][CR1073899].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         <span data-ttu-id="544ac-205">Abrir o painel da **barra lateral calculada**</span><span class="sxs-lookup"><span data-stu-id="544ac-205">Open the **Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         <span data-ttu-id="544ac-207">Painel da **barra lateral calculada**</span><span class="sxs-lookup"><span data-stu-id="544ac-207">**Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="544ac-208">Agrupando Propriedades CSS no painel calculado</span><span class="sxs-lookup"><span data-stu-id="544ac-208">Grouping CSS properties in the Computed panel</span></span>  

<span data-ttu-id="544ac-209">Para exibir a CSS aplicada com menos rolagem, agrupe as propriedades CSS por categorias no painel **calculado** .</span><span class="sxs-lookup"><span data-stu-id="544ac-209">To view your applied CSS with less scrolling, group the CSS properties by categories in the **Computed** pane.</span></span>  <span data-ttu-id="544ac-210">Você também pode se concentrar seletivamente em um conjunto de propriedades relacionadas enquanto inspeciona seu CSS.</span><span class="sxs-lookup"><span data-stu-id="544ac-210">You may also selectively focus on a set of related properties while you inspect your CSS.</span></span>  <span data-ttu-id="544ac-211">Na ferramenta **elementos** , escolha um elemento.</span><span class="sxs-lookup"><span data-stu-id="544ac-211">From the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="544ac-212">Para agrupar \ (ou desagrupar \) as propriedades CSS, alterne a caixa de seleção do **grupo** .</span><span class="sxs-lookup"><span data-stu-id="544ac-212">To group \(or ungroup\) the CSS properties, toggle the **Group** checkbox.</span></span>  <span data-ttu-id="544ac-213">Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até problemas [#1096230][CR1096230], [#1084673][CR1084673]e [#1106251][CR1106251].</span><span class="sxs-lookup"><span data-stu-id="544ac-213">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1096230][CR1096230], [#1084673][CR1084673], and [#1106251][CR1106251].</span></span>  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   <span data-ttu-id="544ac-215">Agrupando Propriedades CSS</span><span class="sxs-lookup"><span data-stu-id="544ac-215">Grouping CSS properties</span></span>  
:::image-end:::  

### <span data-ttu-id="544ac-216">Lighthouse 6,4 na ferramenta Lighthouse</span><span class="sxs-lookup"><span data-stu-id="544ac-216">Lighthouse 6.4 in the Lighthouse tool</span></span>  

<span data-ttu-id="544ac-217">A ferramenta **Lighthouse** agora está em execução Lighthouse 6,4.</span><span class="sxs-lookup"><span data-stu-id="544ac-217">The **Lighthouse** tool is now running Lighthouse 6.4.</span></span>  <span data-ttu-id="544ac-218">Para obter uma lista completa de alterações, acesse as [notas de versão do Lighthouse][GithubGoogleChromeLighthouseReleasesV641].</span><span class="sxs-lookup"><span data-stu-id="544ac-218">For a full list of changes, navigate to the [Lighthouse release notes][GithubGoogleChromeLighthouseReleasesV641].</span></span>  <span data-ttu-id="544ac-219">Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#772558][CR772558].</span><span class="sxs-lookup"><span data-stu-id="544ac-219">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#772558][CR772558].</span></span>  

### <span data-ttu-id="544ac-220">eventos performance. Mark () na seção timings</span><span class="sxs-lookup"><span data-stu-id="544ac-220">performance.mark() events in the Timings section</span></span>  

<span data-ttu-id="544ac-221">A **seção intervalos** de uma gravação na ferramenta [desempenho][DevtoolsGuideChromiumEvaluatePerformanceReference] agora marca os `performance.mark()` eventos.</span><span class="sxs-lookup"><span data-stu-id="544ac-221">The **Timings section** of a recording in the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool now marks `performance.mark()` events.</span></span>  <span data-ttu-id="544ac-222">Para experimentar esse recurso e medir o desempenho do seu código JavaScript, adicione `performance.mark()` eventos ao seu código.</span><span class="sxs-lookup"><span data-stu-id="544ac-222">To try this feature and measure the performance of your JavaScript code, add `performance.mark()` events to your code.</span></span>  <span data-ttu-id="544ac-223">Por exemplo, o trecho de código a seguir adiciona marcadores antes e depois de um `for` loop que itera de 0 a 1000 usando incrementos de 7.</span><span class="sxs-lookup"><span data-stu-id="544ac-223">For example, the following code snippet adds markers before and after a `for` loop that iterates from 0 to 1000 using increments of 7.</span></span>  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

<span data-ttu-id="544ac-224">Em seguida, abra a ferramenta [desempenho][DevtoolsGuideChromiumEvaluatePerformanceReference] e navegue até a **seção intervalos** para gravar o código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="544ac-224">Then, open the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool and navigate to the **Timings section** to record your JavaScript code.</span></span>  <span data-ttu-id="544ac-225">Os `performance.mark()` eventos que você adicionou são agora exibidos na gravação.</span><span class="sxs-lookup"><span data-stu-id="544ac-225">The `performance.mark()` events you added are now displayed in the recording.</span></span>  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` <span data-ttu-id="544ac-227">MouseUp</span><span class="sxs-lookup"><span data-stu-id="544ac-227">events</span></span>  
:::image-end:::  

### <span data-ttu-id="544ac-228">Novos filtros de tipo de recurso e URL na ferramenta rede</span><span class="sxs-lookup"><span data-stu-id="544ac-228">New resource-type and url filters in the Network tool</span></span>  

<span data-ttu-id="544ac-229">Use as `resource-type` `url` palavras-chave novo e na ferramenta **rede** para filtrar solicitações de rede.</span><span class="sxs-lookup"><span data-stu-id="544ac-229">Use the new `resource-type` and `url` keywords in the **Network** tool to filter network requests.</span></span>  <span data-ttu-id="544ac-230">Por exemplo, use `resource-type:image` para se concentrar nas solicitações de rede que são imagens.</span><span class="sxs-lookup"><span data-stu-id="544ac-230">For example, use `resource-type:image` to focus on the network requests that are images.</span></span>  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   <span data-ttu-id="544ac-232">filtro do tipo recurso</span><span class="sxs-lookup"><span data-stu-id="544ac-232">resource-type filter</span></span>  
:::image-end:::  

<span data-ttu-id="544ac-233">Para descobrir mais palavras-chave especiais, como `resource-type` e `url` , navegue até [Filtrar solicitações por Propriedades][DevtoolsNetworkReferenceFilterRequestsProperties].</span><span class="sxs-lookup"><span data-stu-id="544ac-233">To discover more special keywords such as `resource-type` and `url`, navigate to [filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties].</span></span>  <span data-ttu-id="544ac-234">Para revisar as atualizações em tempo real sobre esse recurso no projeto de fonte aberta do Chromium, navegue até problemas [#1121141][CR1121141] e [#1104188][CR1104188].</span><span class="sxs-lookup"><span data-stu-id="544ac-234">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1121141][CR1121141] and [#1104188][CR1104188].</span></span>  

### <span data-ttu-id="544ac-235">Atualizações da exibição de detalhes do quadro</span><span class="sxs-lookup"><span data-stu-id="544ac-235">Frame details view updates</span></span>  

#### <span data-ttu-id="544ac-236">Exibir relatórios do COEP e COOP para o ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="544ac-236">Display COEP and COOP reporting to endpoint</span></span>  

<span data-ttu-id="544ac-237">Veja o ponto de extremidade da política incorporada de várias origens \ (COEP \) e interoriginal Opener Policy \ (COOP \) `reporting to` na seção **isolamento de segurança &** .</span><span class="sxs-lookup"><span data-stu-id="544ac-237">View the Cross-Origin Embedder Policy \(COEP\) and Cross-Origin Opener Policy \(COOP\) `reporting to` endpoint under the **Security & Isolation** section.</span></span>  <span data-ttu-id="544ac-238">A [API de relatório][MdnReportingApi] define `Report-To` um novo cabeçalho HTTP, que oferece uma maneira de especificar os pontos de extremidade do servidor para que o navegador envie avisos e erros.</span><span class="sxs-lookup"><span data-stu-id="544ac-238">The [Reporting API][MdnReportingApi] defines `Report-To`, a new HTTP header, that gives you a way to specify the server endpoints for the browser to send warnings and errors.</span></span>  <span data-ttu-id="544ac-239">Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="544ac-239">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   <span data-ttu-id="544ac-241">O `reporting to` ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="544ac-241">The `reporting to` endpoint</span></span>  
:::image-end:::  

#### <span data-ttu-id="544ac-242">Exibir COEP e COOP modo somente de relatório</span><span class="sxs-lookup"><span data-stu-id="544ac-242">Display COEP and COOP report-only mode</span></span>  

<span data-ttu-id="544ac-243">O DevTools agora exibe o `report-only` rótulo para COEP e Coop que estão definidos como `report-only` Mode.</span><span class="sxs-lookup"><span data-stu-id="544ac-243">DevTools now display the `report-only` label for COEP and COOP that are set to `report-only` mode.</span></span>  <span data-ttu-id="544ac-244">Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="544ac-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   <span data-ttu-id="544ac-246">O `report-only` rótulo Mode</span><span class="sxs-lookup"><span data-stu-id="544ac-246">The `report-only` mode label</span></span>  
:::image-end:::  

### <span data-ttu-id="544ac-247">Exibir e corrigir problemas de contraste de cor na ferramenta de visão geral CSS</span><span class="sxs-lookup"><span data-stu-id="544ac-247">View and fix color contrast issues in the CSS Overview tool</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos":::
   <span data-ttu-id="544ac-249">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="544ac-249">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="544ac-250">A ferramenta de **visão geral CSS** agora exibe uma lista de elementos em sua página com problemas de contraste de cor.</span><span class="sxs-lookup"><span data-stu-id="544ac-250">The **CSS Overview** tool now displays a list of elements on your page that have color contrast issues.</span></span>  <span data-ttu-id="544ac-251">A seguinte página de demonstração tem um exemplo de um problema de contraste de cor.</span><span class="sxs-lookup"><span data-stu-id="544ac-251">The following demo page has an example of a color contrast issue.</span></span>  

[<span data-ttu-id="544ac-252">Visão geral da CSS demonstração de cores acessíveis</span><span class="sxs-lookup"><span data-stu-id="544ac-252">CSS Overview Accessible Colors Demo</span></span>][GlitchCssOverviewAccessibleColorsDemo]  

<span data-ttu-id="544ac-253">Para habilitar esse experimento, em **configurações**  >  **experimentos**, escolha a caixa de seleção **visão geral da CSS** .</span><span class="sxs-lookup"><span data-stu-id="544ac-253">To enable this experiment, under **Settings** > **Experiments**, choose the **CSS Overview** checkbox.</span></span>  <span data-ttu-id="544ac-254">Para exibir uma lista de elementos que têm um problema de contraste de cor, em **problemas de contraste**, escolha **texto**.</span><span class="sxs-lookup"><span data-stu-id="544ac-254">To view a list of elements that have a color contrast issue, on **Contrast issues**, choose **Text**.</span></span>  <span data-ttu-id="544ac-255">Para abrir o elemento na ferramenta **elementos** , escolha um elemento na lista.</span><span class="sxs-lookup"><span data-stu-id="544ac-255">To open the element in the **Elements** tool, choose an element in the list.</span></span>  <span data-ttu-id="544ac-256">Para ajudar a corrigir problemas de contraste, o Microsoft Edge DevTools [fornecer sugestões de cores automaticamente][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span><span class="sxs-lookup"><span data-stu-id="544ac-256">To help fix contrast issues, the Microsoft Edge DevTools [automatically provide color suggestions][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span></span>  <span data-ttu-id="544ac-257">Para revisar as atualizações em tempo real deste recurso no projeto de fonte aberta do Chromium, navegue até o Issue [#1120316][CR1120316].</span><span class="sxs-lookup"><span data-stu-id="544ac-257">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1120316][CR1120316].</span></span>  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Ferramenta de rede com filtros não traduzidos" lightbox="../../media/2020/10/css-overview.msft.png":::
   <span data-ttu-id="544ac-259">Problemas de contraste de cor baixo</span><span class="sxs-lookup"><span data-stu-id="544ac-259">Low color contrast issues</span></span>  
:::image-end:::  

## <span data-ttu-id="544ac-260">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="544ac-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="544ac-261">Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="544ac-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="544ac-262">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="544ac-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="544ac-263">Como entrar em contato com o Microsoft Edge DevTools equipe</span><span class="sxs-lookup"><span data-stu-id="544ac-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Substituição do painel Propriedades na ferramenta elementos – novidades do DevTools (Microsoft Edge 84) | Documentos da Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Recursos de depuração de grade CSS-novidades do DevTools (Microsoft Edge 85) | Documentos da Microsoft"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Sugestão de cor acessível no painel estilos – novidades do DevTools (Microsoft Edge 86) | Documentos da Microsoft"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móveis no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Elemento JavaScript ou elemento JavaScript selecionado recentemente-referência de API de utilitários de console | Documentos da Microsoft"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalizar atalhos de teclado no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Referência de análise de desempenho | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Emulação: suporta o modo de tela dupla-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Habilitar APIs experimentais-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Habilitar o editor de atalhos de teclado-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulação: suporta o modo de tela dupla-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Habilitar o console de rede-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Habilitar o Visualizador de ordem de origem-recursos experimentais | Documentos da Microsoft"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Testes em dispositivos dobrável e de tela dupla-recursos experimentais | Documentos da Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Ativar recursos experimentais-recursos experimentais | Documentos da Microsoft"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "tabela-referência da API do console | Documentos da Microsoft"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Localizar código JavaScript e CSS não usados com a guia cobertura no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Inspecionar grade CSS | Documentos da Microsoft"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Gaveta-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analisar o desempenho de renderização com a guia renderização-referência de análise de desempenho | Documentos da Microsoft"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Exibir e depurar informações do media players | Documentos da Microsoft"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Filtrar solicitações por Propriedades-referência de análise de rede | Documentos da Microsoft"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Emular autenticadores e depurar webauthn no Microsoft Edge DevTools | Documentos da Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de visualização do Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Código do Visual Studio"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Ferramentas do Microsoft Edge para o código do Visual Studio | Código do Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros de Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: permite personalizar atalhos de teclado/associações de teclas | Erros de Chromium"
[CR772558]: https://crbug.com/772558 "DevTools: Atualize para a versão mais recente do Lighthouse | Erros de Chromium"  
[CR1034663]: https://crbug.com/1034663 "Crie um front-end para a API de teste webauthn | Erros de Chromium"  
[CR1047356]: https://crbug.com/1047356 "Ferramentas de grade/flexbox/tabela CSS | Erros de Chromium"  
[CR1051466]: https://crbug.com/1051466 "Suporta a depuração COOP/COEP no DevTools | Erros de Chromium"  
[CR1073899]: https://crbug.com/1073899 "Guia estilo calculado desaparece no modo responsivo | Erros de Chromium"  
[CR1075732]: https://crbug.com/1075732 "Personalização DevTools-guias móveis | Erros de Chromium"  
[CR1084673]: https://crbug.com/1084673 "DevTools: aprimore a maneira como apresentamos as propriedades personalizadas CSS (também conhecidos). Variáveis CSS) e seus valores | Erros de Chromium"  
[CR1093687]: https://crbug.com/1093687 "Crie uma ferramenta para criar e reproduzir solicitações de rede sintéticas | Erros de Chromium"  
[CR1096230]: https://crbug.com/1096230 "Agrupar Propriedades CSS por categorias no painel estilos calculados | Erros de Chromium"  
[CR1104188]: https://crbug.com/1104188 "A pesquisa da ferramenta de rede não localiza resultados ao procurar por URL completa | Erros de Chromium"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: a guia melhorar estilos calculados | Erros de Chromium"  
[CR1120316]: https://crbug.com/1120316 "Realçar contraste incorreto na visão geral da CSS > cores | Erros de Chromium"  
[CR1121141]: https://crbug.com/1121141 "Permitir filtragem por tipo de recurso no log de rede | Erros de Chromium"  
[CR1121312]: https://crbug.com/1121312 "As configurações devem ser removidas do menu mais ferramentas | Erros de Chromium"  
[CR1136394]: https://crbug.com/1136394 "Ferramenta de flexbox | Erros de Chromium"  
[CR1136655]: https://crbug.com/1136655 "Devtools: localização v2 | Erros de Chromium"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "API de relatórios | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v 6.4.1-GoogleChrome/Lighthouse | GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticação da Web | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Olá! | Problema"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Formato da coleção do postmaster v 2.1.0 | Postmaster"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "Especificação do OpenAPI | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> <span data-ttu-id="544ac-316">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="544ac-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="544ac-317">A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/10/devtools/index) e é criada por [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="544ac-317">The original page is found [here](https://developers.google.com/web/updates/2020/10/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="544ac-319">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="544ac-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
