---
description: Os recursos experimentais mais recentes no Microsoft Edge DevTools
title: Recursos experimentais
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, experimento
ms.openlocfilehash: 612b3b83aee1ee9035982e58e008395ec3645b2b
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408301"
---
# <a name="experimental-features"></a><span data-ttu-id="0afc7-104">Recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="0afc7-104">Experimental features</span></span>  

<span data-ttu-id="0afc7-105">O Microsoft Edge DevTools fornece acesso a recursos experimentais que ainda estão em desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="0afc7-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="0afc7-106">Você pode testar e [fornecer comentários antes](#providing-feedback-on-experimental-features) de cada recurso ser lançado.</span><span class="sxs-lookup"><span data-stu-id="0afc7-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="0afc7-107">Embora os recursos experimentais estão disponíveis em todos os canais do Microsoft Edge, você pode obter os recursos experimentais mais recentes usando o canal Canary do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0afc7-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="0afc7-108">Ativar recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="0afc7-108">Turn on experimental features</span></span>  

<span data-ttu-id="0afc7-109">Para ativar \(ou desativar\) recursos experimentais no Microsoft Edge, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0afc7-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="0afc7-110">[Abra DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="0afc7-110">[Open DevTools][DevtoolsOpenIndex].</span></span>  
    *   <span data-ttu-id="0afc7-111">Selecione `Control` + `Shift` + `I` \(Windows, Linux\) `Command` + `Option` + `I` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="0afc7-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="0afc7-112">Para obter mais informações, navegue até Atalhos de teclado [do Microsoft Edge DevTools.][DevtoolsShortcutsIndex]</span><span class="sxs-lookup"><span data-stu-id="0afc7-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="0afc7-113">Abra o [painel Configurações.][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="0afc7-113">Open the [Settings][DevToolsCustomizeIndexSettings] pane.</span></span>  
    *   <span data-ttu-id="0afc7-114">Selecione `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="0afc7-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="0afc7-115">Para obter mais informações, navegue até Atalhos de teclado [do Microsoft Edge DevTools.][DevtoolsShortcutsIndex]</span><span class="sxs-lookup"><span data-stu-id="0afc7-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="0afc7-116">No lado esquerdo do painel **Configurações,** escolha a **seção Experimentos.**</span><span class="sxs-lookup"><span data-stu-id="0afc7-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="A página Experimentos em Configurações" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="0afc7-118">A **página Experimentos** **em Configurações**</span><span class="sxs-lookup"><span data-stu-id="0afc7-118">The **Experiments** page in **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0afc7-119">Na página **Experimentos,** role a lista de todos os recursos experimentais disponíveis e escolha a caixa de seleção ao lado de cada recurso que você deseja testar.</span><span class="sxs-lookup"><span data-stu-id="0afc7-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="0afc7-120">Feche e reabra o Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="0afc7-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="0afc7-121">Os recursos experimentais estão sendo atualizados constantemente e podem causar problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="0afc7-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="0afc7-122">Para desativar um recurso experimental, abra a página **Experimentos** e limpe a caixa de seleção do recurso experimental que você deseja desativar.</span><span class="sxs-lookup"><span data-stu-id="0afc7-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <a name="highlighted-experimental-features"></a><span data-ttu-id="0afc7-123">Recursos experimentais realçados</span><span class="sxs-lookup"><span data-stu-id="0afc7-123">Highlighted experimental features</span></span>  

<span data-ttu-id="0afc7-124">As seções a seguir descrevem os novos recursos experimentais disponíveis no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0afc7-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="0afc7-125">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="0afc7-125">Experimental feature</span></span> | <span data-ttu-id="0afc7-126">Versão do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0afc7-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="0afc7-127">Habilitar webhint</span><span class="sxs-lookup"><span data-stu-id="0afc7-127">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="0afc7-128">85 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0afc7-128">85 or later</span></span> |  
| [<span data-ttu-id="0afc7-129">Habilitar o Console de Rede</span><span class="sxs-lookup"><span data-stu-id="0afc7-129">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="0afc7-130">85 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0afc7-130">85 or later</span></span> |  
| [<span data-ttu-id="0afc7-131">Visualizador de Ordem de Origem</span><span class="sxs-lookup"><span data-stu-id="0afc7-131">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="0afc7-132">86 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0afc7-132">86 or later</span></span> |  
| [<span data-ttu-id="0afc7-133">Habilitar camadas compostas no modo de exibição 3D</span><span class="sxs-lookup"><span data-stu-id="0afc7-133">Enable Composited Layers in 3D View</span></span>](#enable-composited-layers-in-3d-view) | <span data-ttu-id="0afc7-134">87 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0afc7-134">87 or later</span></span> |  
| [<span data-ttu-id="0afc7-135">Habilitar a nova ferramenta Editor de Fontes no painel Estilos</span><span class="sxs-lookup"><span data-stu-id="0afc7-135">Enable new Font Editor tool within the Styles pane</span></span>](#enable-new-font-editor-tool-within-the-styles-pane) | <span data-ttu-id="0afc7-136">89 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0afc7-136">89 or later</span></span> |  
| [<span data-ttu-id="0afc7-137">Habilitar novos recursos de depuração do CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="0afc7-137">Enable new CSS Flexbox debugging features</span></span>](#enable-new-css-flexbox-debugging-features) | <span data-ttu-id="0afc7-138">89 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0afc7-138">89 or later</span></span> |  
| [<span data-ttu-id="0afc7-139">Habilitar + menus de guia de botão para abrir mais ferramentas</span><span class="sxs-lookup"><span data-stu-id="0afc7-139">Enable + button tab menus to open more tools</span></span>](#enable--button-tab-menus-to-open-more-tools) | <span data-ttu-id="0afc7-140">89 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0afc7-140">89 or later</span></span> |  
| [<span data-ttu-id="0afc7-141">Habilitar a guia Bem-vindo</span><span class="sxs-lookup"><span data-stu-id="0afc7-141">Enable Welcome tab</span></span>](#enable-welcome-tool) | <span data-ttu-id="0afc7-142">89 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0afc7-142">89 or later</span></span> |  

### <a name="enable-webhint"></a><span data-ttu-id="0afc7-143">Habilitar webhint</span><span class="sxs-lookup"><span data-stu-id="0afc7-143">Enable webhint</span></span>  

<span data-ttu-id="0afc7-144">[webhint][WebhintMain] é uma ferramenta de código aberto que fornece comentários em tempo real para sites e páginas da Web locais.</span><span class="sxs-lookup"><span data-stu-id="0afc7-144">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="0afc7-145">O tipo de comentários fornecido pela [webhint][WebhintMain].</span><span class="sxs-lookup"><span data-stu-id="0afc7-145">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="0afc7-146">acessibilidade</span><span class="sxs-lookup"><span data-stu-id="0afc7-146">accessibility</span></span>  
*   <span data-ttu-id="0afc7-147">Compatibilidade entre navegadores</span><span class="sxs-lookup"><span data-stu-id="0afc7-147">cross-browser compatibility</span></span>  
*   <span data-ttu-id="0afc7-148">segurança</span><span class="sxs-lookup"><span data-stu-id="0afc7-148">security</span></span>  
*   <span data-ttu-id="0afc7-149">performance</span><span class="sxs-lookup"><span data-stu-id="0afc7-149">performance</span></span>  
*   <span data-ttu-id="0afc7-150">Aplicativos Web Progressivos (PWAs)</span><span class="sxs-lookup"><span data-stu-id="0afc7-150">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="0afc7-151">outros problemas comuns de desenvolvimento da Web</span><span class="sxs-lookup"><span data-stu-id="0afc7-151">other common web development issues</span></span>  
    
<span data-ttu-id="0afc7-152">O [experimento webhint][WebhintMain] exibe os comentários webhint no painel [Problemas.][DevtoolsIssuesIndex]</span><span class="sxs-lookup"><span data-stu-id="0afc7-152">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssuesIndex] panel.</span></span>  <span data-ttu-id="0afc7-153">Escolha um problema para exibir a documentação da solução e uma lista dos recursos afetados em seu site.</span><span class="sxs-lookup"><span data-stu-id="0afc7-153">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="0afc7-154">Escolha um link de recurso para abrir o painel **Rede,** **Fontes**ou **Elementos** relevantes no DevTools.</span><span class="sxs-lookup"><span data-stu-id="0afc7-154">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="comentários webhint no painel Problemas" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="0afc7-156">comentários webhint no painel **Problemas**</span><span class="sxs-lookup"><span data-stu-id="0afc7-156">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-network-console"></a><span data-ttu-id="0afc7-157">Habilitar o Console de Rede</span><span class="sxs-lookup"><span data-stu-id="0afc7-157">Enable Network Console</span></span>  

<span data-ttu-id="0afc7-158">**Console de** Rede é o título de trabalho de um experimento para fazer solicitações de rede sintéticas por HTTP.</span><span class="sxs-lookup"><span data-stu-id="0afc7-158">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="0afc7-159">Você pode usar o experimento **de Console de Rede** para enviar solicitações de API da Web.</span><span class="sxs-lookup"><span data-stu-id="0afc7-159">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="0afc7-160">Depois de ativar o experimento, reinicie o DevTools.</span><span class="sxs-lookup"><span data-stu-id="0afc7-160">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="0afc7-161">Para usar o **Console de Rede,** conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0afc7-161">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="0afc7-162">Abra o **painel** Rede.</span><span class="sxs-lookup"><span data-stu-id="0afc7-162">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="0afc7-163">Encontre a solicitação de rede que você deseja alterar e reendá-la.</span><span class="sxs-lookup"><span data-stu-id="0afc7-163">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="0afc7-164">Abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Editar e Repetir**.</span><span class="sxs-lookup"><span data-stu-id="0afc7-164">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="0afc7-165">Quando o **Console de Rede** for aberto, edite as informações de solicitação de rede.</span><span class="sxs-lookup"><span data-stu-id="0afc7-165">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="0afc7-166">Escolha **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="0afc7-166">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Console de rede na gaveta console" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="0afc7-168">**Console de rede** na gaveta **console**</span><span class="sxs-lookup"><span data-stu-id="0afc7-168">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="source-order-viewer"></a><span data-ttu-id="0afc7-169">Visualizador de Ordem de Origem</span><span class="sxs-lookup"><span data-stu-id="0afc7-169">Source Order Viewer</span></span>  

<span data-ttu-id="0afc7-170">**O Visualizador de Ordem de** Origem é um experimento que exibe a ordem dos elementos na origem da página da Web.</span><span class="sxs-lookup"><span data-stu-id="0afc7-170">**Source Order Viewer** is an experiment that displays the order of elements in the webpage source.</span></span>  <span data-ttu-id="0afc7-171">A ordem de exibição na tela pode ser diferente da ordem da origem, o que confundiu usuários de leitor de tela e teclado.</span><span class="sxs-lookup"><span data-stu-id="0afc7-171">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="0afc7-172">Use o **experimento Visualizador de Ordem** de Origem para encontrar as diferenças entre a ordem de exibição na tela e a ordem da fonte.</span><span class="sxs-lookup"><span data-stu-id="0afc7-172">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="0afc7-173">Depois de ativar o experimento, reinicie o DevTools.</span><span class="sxs-lookup"><span data-stu-id="0afc7-173">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="0afc7-174">Para usar **o Visualizador de Ordem de**Origem, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0afc7-174">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="0afc7-175">Abra a **ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="0afc7-175">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="0afc7-176">Abra o **painel Acessibilidade** no painel de gaveta \(bottom\)</span><span class="sxs-lookup"><span data-stu-id="0afc7-176">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="0afc7-177">Na seção **Visualizador de Ordem de** Origem, escolha a caixa de seleção **Mostrar Ordem** de Origem.</span><span class="sxs-lookup"><span data-stu-id="0afc7-177">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="0afc7-178">Realça qualquer elemento HTML para exibir uma sobreposição que a ordem na origem da página da Web.</span><span class="sxs-lookup"><span data-stu-id="0afc7-178">Highlight any HTML element to display an overlay that the order in the webpage source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Visualizador de Ordem de Origem no painel Acessibilidade" lightbox="../media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="0afc7-180">**Visualizador de Ordem de** Origem no painel **Acessibilidade**</span><span class="sxs-lookup"><span data-stu-id="0afc7-180">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <a name="enable-composited-layers-in-3d-view"></a><span data-ttu-id="0afc7-181">Habilitar camadas compostas no modo de exibição 3D</span><span class="sxs-lookup"><span data-stu-id="0afc7-181">Enable Composited Layers in 3D View</span></span>  

<span data-ttu-id="0afc7-182">Agora você pode visualizar Layers juntamente com índices z e o Modelo de Objeto de Documento \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="0afc7-182">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="0afc7-183">Esse recurso ajuda você a depurar sem alternar contextos com a mesma frequência.</span><span class="sxs-lookup"><span data-stu-id="0afc7-183">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="0afc7-184">Você identificou que a redução da alternção de contexto era um grande ponto de dor.</span><span class="sxs-lookup"><span data-stu-id="0afc7-184">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="0afc7-185">Nem sempre é claro como o código que você escreve afeta seu aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="0afc7-185">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="0afc7-186">Para uma experiência de depuração visual abrangente, o Modo de exibição 3D e as camadas compostas agora são combinados.</span><span class="sxs-lookup"><span data-stu-id="0afc7-186">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  

<span data-ttu-id="0afc7-187">Depois de ativar o experimento, reinicie o DevTools.</span><span class="sxs-lookup"><span data-stu-id="0afc7-187">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="0afc7-188">Para usar **Camadas Compostas,** conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0afc7-188">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="0afc7-189">Na gaveta, escolha a ferramenta De exibição **3D.**</span><span class="sxs-lookup"><span data-stu-id="0afc7-189">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="0afc7-190">Abra o **painel Camadas Compostas.**</span><span class="sxs-lookup"><span data-stu-id="0afc7-190">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="0afc7-191">Todas as camadas pintadas do aplicativo são exibidas.</span><span class="sxs-lookup"><span data-stu-id="0afc7-191">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="0afc7-192">Experimente esse recurso com seus próprios aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="0afc7-192">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Painel de Camadas compostas" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="0afc7-194">Painel de **Camadas Compostas**</span><span class="sxs-lookup"><span data-stu-id="0afc7-194">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-new-font-editor-tool-within-the-styles-pane"></a><span data-ttu-id="0afc7-195">Habilitar a nova ferramenta Editor de Fontes no painel Estilos</span><span class="sxs-lookup"><span data-stu-id="0afc7-195">Enable new Font Editor tool within the Styles pane</span></span>  

<span data-ttu-id="0afc7-196">Agora você pode usar o novo Editor de [Fonte visual][DevtoolsInspectStylesEditFonts] para editar fontes.</span><span class="sxs-lookup"><span data-stu-id="0afc7-196">You may now use the new visual [Font Editor][DevtoolsInspectStylesEditFonts] to edit fonts.</span></span>  <span data-ttu-id="0afc7-197">Use-o para definir fontes e características de fonte.</span><span class="sxs-lookup"><span data-stu-id="0afc7-197">Use it define fonts and font characteristics.</span></span>  <span data-ttu-id="0afc7-198">O Editor **de Fonte visual** ajuda você a concluir as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="0afc7-198">The visual **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="0afc7-199">Alternar entre unidades para propriedades de fonte diferentes</span><span class="sxs-lookup"><span data-stu-id="0afc7-199">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="0afc7-200">Alternar entre palavras-chave para propriedades de fonte diferentes</span><span class="sxs-lookup"><span data-stu-id="0afc7-200">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="0afc7-201">Converter unidades</span><span class="sxs-lookup"><span data-stu-id="0afc7-201">Convert units</span></span>  
*   <span data-ttu-id="0afc7-202">Gerar código CSS preciso</span><span class="sxs-lookup"><span data-stu-id="0afc7-202">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="0afc7-203">Depois de ativar o experimento, reinicie o DevTools.</span><span class="sxs-lookup"><span data-stu-id="0afc7-203">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="0afc7-204">Para usar o novo Editor de **Fonte visual,** conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0afc7-204">To use the new visual **Font Editor**, complete the following steps.</span></span>  

1.  <span data-ttu-id="0afc7-205">Abra a **ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="0afc7-205">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="0afc7-206">Abra o **painel Estilos.**</span><span class="sxs-lookup"><span data-stu-id="0afc7-206">Open the **Styles** pane.</span></span>  
1.  <span data-ttu-id="0afc7-207">Escolha o **ícone editor de** fontes.</span><span class="sxs-lookup"><span data-stu-id="0afc7-207">Choose the **Font Editor** icon.</span></span>  
    
<span data-ttu-id="0afc7-208">Para obter mais informações sobre o novo Editor de **Fontes visuais,** navegue até Editar estilos de fonte CSS e configurações no [painel Estilos em DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="0afc7-208">For more information about the new visual **Font Editor**, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="O painel editor de fontes visual é realçado" lightbox="../media/font-editor-open.msft.png":::
   <span data-ttu-id="0afc7-210">O painel **editor de fontes** visual é realçado</span><span class="sxs-lookup"><span data-stu-id="0afc7-210">The visual **Font Editor** pane is highlighted</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-new-css-flexbox-debugging-features"></a><span data-ttu-id="0afc7-211">Habilitar novos recursos de depuração do CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="0afc7-211">Enable new CSS Flexbox debugging features</span></span>  

<span data-ttu-id="0afc7-212">Esse recurso experimental fornece muitas novas visualizações para ajudá-lo a depurar layouts do CSS Flexbox.</span><span class="sxs-lookup"><span data-stu-id="0afc7-212">This experimental feature provides many new visualizations to help you debug CSS Flexbox layouts.</span></span>  <span data-ttu-id="0afc7-213">Para visualizar os recursos experimentais mais recentes, [a ligue este experimento](#turn-on-experimental-features) e recarregue o DevTools.</span><span class="sxs-lookup"><span data-stu-id="0afc7-213">To preview the latest experimental features, [turn on this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a><span data-ttu-id="0afc7-214">Exibir sobreposições persistentes em layouts do Flexbox com a ferramenta Inspecionar</span><span class="sxs-lookup"><span data-stu-id="0afc7-214">Display persistent overlays on Flexbox layouts with the Inspect tool</span></span>  

<span data-ttu-id="0afc7-215">A **ferramenta Inspect** fornece uma maneira rápida de identificar e visualizar layouts do CSS Flexbox em um site, pairando sobre eles com o mouse.</span><span class="sxs-lookup"><span data-stu-id="0afc7-215">The **Inspect** tool provides a quick way to identify and visualize CSS Flexbox layouts in a website by hovering on them with the mouse.</span></span>  <span data-ttu-id="0afc7-216">Escolha o **ícone Inspecionar** \( ![ Inspecionar ](../media/inspect-icon.msft.png) \) no canto superior esquerdo do DevTools.</span><span class="sxs-lookup"><span data-stu-id="0afc7-216">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="0afc7-217">Em seguida, durante a depuração do site, passe o mouse em um contêiner flexível para exibir contornos ao redor do contêiner flexível.</span><span class="sxs-lookup"><span data-stu-id="0afc7-217">Then, while debugging the website, hover on a flex container to display outlines around the flex container.</span></span>  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Exibir contêineres do Flexbox com a ferramenta Inspecionar" lightbox="../media/flexbox-hover.msft.png":::
   <span data-ttu-id="0afc7-219">Exibir contêineres do Flexbox com a **ferramenta Inspecionar**</span><span class="sxs-lookup"><span data-stu-id="0afc7-219">Display Flexbox containers with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a><span data-ttu-id="0afc7-220">Exibir sobreposições persistentes em layouts do Flexbox</span><span class="sxs-lookup"><span data-stu-id="0afc7-220">Display persistent overlays on Flexbox layouts</span></span>  

<span data-ttu-id="0afc7-221">No Microsoft Edge versão 89 ou posterior, o recurso experimental CSS Flexbox também oferece a opção de ativar sobreposições persistentes em layouts do Flexbox.</span><span class="sxs-lookup"><span data-stu-id="0afc7-221">In Microsoft Edge version 89 or later, the experimental CSS Flexbox feature also offers the option to turn on persistent overlays on Flexbox layouts.</span></span>  <span data-ttu-id="0afc7-222">Sobreposições persistentes fornecem os seguintes benefícios.</span><span class="sxs-lookup"><span data-stu-id="0afc7-222">Persistent overlays provide the following benefits.</span></span>  

*   <span data-ttu-id="0afc7-223">As sobreposições persistentes permanecem visíveis na página da Web à medida que você rola, move o mouse e usa outros recursos do DevTools.</span><span class="sxs-lookup"><span data-stu-id="0afc7-223">Persistent overlays remain visible on the webpage as you scroll, move your mouse, and use other features of the DevTools.</span></span>
*   <span data-ttu-id="0afc7-224">Várias sobreposições persistentes podem ser usadas ao mesmo tempo, para permitir que você revise vários layouts do Flexbox ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="0afc7-224">Multiple persistent overlays may be used at the same time, to allow you to review several Flexbox layouts at once.</span></span>  
*   <span data-ttu-id="0afc7-225">Sobreposições persistentes oferecem opções de configuração de cores.</span><span class="sxs-lookup"><span data-stu-id="0afc7-225">Persistent overlays offer color configuration options.</span></span>  
    
<span data-ttu-id="0afc7-226">Para alternar sobreposições persistentes no layout do Flexbox, use uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="0afc7-226">To toggle persistent overlays on Flexbox layout, use one of following actions.</span></span>  

*   <span data-ttu-id="0afc7-227">Escolha o ícone de oval **Flexbox** ao lado de qualquer contêiner Flexbox exibido na árvore DOM da **ferramenta Elements.**</span><span class="sxs-lookup"><span data-stu-id="0afc7-227">Choose the **Flexbox** oval icon next to any Flexbox container displayed in the DOM tree of the **Elements** tool.</span></span>  
*   <span data-ttu-id="0afc7-228">Abra o novo **painel layout** localizado na ferramenta **Elementos** e escolha a caixa de seleção ao lado de cada contêiner do Flexbox que você deseja realçar.</span><span class="sxs-lookup"><span data-stu-id="0afc7-228">Open the new **Layout** panel located in the **Elements** tool, and choose the checkbox next to each Flexbox container you want to highlight.</span></span>  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Ícones flexíveis e painel layout no DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   <span data-ttu-id="0afc7-230">Ícones flexíveis **e painel layout** no DevTools</span><span class="sxs-lookup"><span data-stu-id="0afc7-230">Flex icons and **Layout** panel in DevTools</span></span>  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a><span data-ttu-id="0afc7-231">Configurar sobreposições persistentes</span><span class="sxs-lookup"><span data-stu-id="0afc7-231">Configure persistent overlays</span></span>  

<span data-ttu-id="0afc7-232">Para configurar opções para sobreposições persistentes para grades CSS ou layouts do Flexbox, use o **painel Layout.**</span><span class="sxs-lookup"><span data-stu-id="0afc7-232">To configure options for persistent overlays for CSS grids or Flexbox layouts, use the **Layout** pane.</span></span>  <span data-ttu-id="0afc7-233">O **painel Layout** está localizado na ferramenta **Elements** ao lado dos painéis **Estilos** **e** Calculados.</span><span class="sxs-lookup"><span data-stu-id="0afc7-233">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span></span>  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Painel de layout" lightbox="../media/flexbox-layout.msft.png":::
   <span data-ttu-id="0afc7-235">Painel de layout</span><span class="sxs-lookup"><span data-stu-id="0afc7-235">Layout panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable--button-tab-menus-to-open-more-tools"></a><span data-ttu-id="0afc7-236">Habilitar + menus de guia de botão para abrir mais ferramentas</span><span class="sxs-lookup"><span data-stu-id="0afc7-236">Enable + button tab menus to open more tools</span></span>  

<span data-ttu-id="0afc7-237">Agora você pode abrir mais ferramentas usando o novo ícone **Mais Ferramentas** \( `+` \)</span><span class="sxs-lookup"><span data-stu-id="0afc7-237">You may now open more tools using the new **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="0afc7-238">Depois de ativar os **menus** de guia Habilitar + botão para abrir mais ferramentas experimento e recarregar DevTools, um sinal de a mais \( \) é exibido à direita do grupo de guias na parte superior `+` do DevTools.</span><span class="sxs-lookup"><span data-stu-id="0afc7-238">After you turn on the **Enable + button tab menus to open more tools** experiment and reload DevTools, a plus sign \(`+`\) displays to the right of the tab group at the top of the DevTools.</span></span>  <span data-ttu-id="0afc7-239">Para exibir uma lista de outras ferramentas que você pode adicionar à barra de guias, escolha o novo ícone **Mais Ferramentas** \( `+` \).</span><span class="sxs-lookup"><span data-stu-id="0afc7-239">To display a list of other tools that you may add to the tab bar, choose the new **More Tools** \(`+`\) icon.</span></span>  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Mais Ferramentas no painel superior" lightbox="../media/experiments-more-tools-button.msft.png":::
   <span data-ttu-id="0afc7-241">**Mais Ferramentas** no painel superior</span><span class="sxs-lookup"><span data-stu-id="0afc7-241">**More Tools** in the top pane</span></span>
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-welcome-tool"></a><span data-ttu-id="0afc7-242">Habilitar a ferramenta Bem-vindo</span><span class="sxs-lookup"><span data-stu-id="0afc7-242">Enable Welcome tool</span></span>

<span data-ttu-id="0afc7-243">Este experimento substitui a **ferramenta Novidades** pela nova ferramenta **de Boas-vindas.**</span><span class="sxs-lookup"><span data-stu-id="0afc7-243">This experiment replaces the **What's New** tool with the new **Welcome** tool.</span></span>  <span data-ttu-id="0afc7-244">Ele exibe um design atualizado para o conteúdo a seguir.</span><span class="sxs-lookup"><span data-stu-id="0afc7-244">It displays a refreshed design for the following content.</span></span>  

*   <span data-ttu-id="0afc7-245">Links para documentos de desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="0afc7-245">Links to developer docs</span></span>  
*   <span data-ttu-id="0afc7-246">os recursos mais recentes</span><span class="sxs-lookup"><span data-stu-id="0afc7-246">the latest features</span></span>  
*   <span data-ttu-id="0afc7-247">notas de versão</span><span class="sxs-lookup"><span data-stu-id="0afc7-247">release notes</span></span>  
*   <span data-ttu-id="0afc7-248">Opção para entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0afc7-248">Option to contact the Microsoft Edge DevTools team</span></span>  
    
<span data-ttu-id="0afc7-249">A **ferramenta Bem-vindo** é aberta automaticamente após cada atualização para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0afc7-249">The **Welcome** tool opens automatically after each update to Microsoft Edge.</span></span>  <span data-ttu-id="0afc7-250">Para impedir a exibição da ferramenta **De** boas-vindas após cada atualização, deslocar a caixa de seleção ao lado da guia **Abrir** após cada atualização sob o **título** da ferramenta de boas-vindas.</span><span class="sxs-lookup"><span data-stu-id="0afc7-250">To prevent the display of the **Welcome** tool after each update, clear the checkbox next to **Open tab after each update** under the **Welcome** tool title.</span></span>  

<span data-ttu-id="0afc7-251">Se você preferir a ferramenta **Original Novidades,** navegue até [Configurações Experimentos][DevtoolsCustomizeIndexSettings]e remova a caixa de seleção ao lado da guia  >  \*\*\*\* Habilitar **Boas-vindas.**</span><span class="sxs-lookup"><span data-stu-id="0afc7-251">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Ferramenta de boas-vindas" lightbox="../media/experiments-welcome.msft.png":::
   <span data-ttu-id="0afc7-253">**Ferramenta de boas-vindas**</span><span class="sxs-lookup"><span data-stu-id="0afc7-253">**Welcome** tool</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a><span data-ttu-id="0afc7-254">Recursos experimentais anteriores</span><span class="sxs-lookup"><span data-stu-id="0afc7-254">Previous experimental features</span></span>  

*   <span data-ttu-id="0afc7-255">[O Modo de Exibição 3D][Devtools3dViewIndex] agora está disponível e ligado por padrão no Microsoft Edge versão 83 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0afc7-255">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="0afc7-256">[Ativar o suporte para mover guias][DevtoolsCustomizeIndex] entre painéis agora está disponível e ligado por padrão no Microsoft Edge versão 85 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0afc7-256">[Turn on support to move tabs between panels][DevtoolsCustomizeIndex] is now available and turned on by default in Microsoft Edge version 85 or later.</span></span>  
*   <span data-ttu-id="0afc7-257">[Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] is now available and turned on by default in Microsoft Edge version 86 or later.</span><span class="sxs-lookup"><span data-stu-id="0afc7-257">[Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  
*   <span data-ttu-id="0afc7-258">Editar atalhos de teclado para qualquer ação no [DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] agora está disponível e ativado por padrão no Microsoft Edge versão 89 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0afc7-258">[Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="0afc7-259">[Ativar novos recursos de depuração][DevtoolsCssGrid] de grade CSS agora está disponível e ligado por padrão no Microsoft Edge versão 89 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0afc7-259">[Turn on new CSS grid debugging features][DevtoolsCssGrid] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="0afc7-260">[Emulação: o modo de tela dupla][DevtoolsDeviceModeDualScreenAndFoldables] de suporte agora está disponível e ligado por padrão no Microsoft Edge versão 90 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0afc7-260">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] is now available and turned on by default in Microsoft Edge version 90 or later.</span></span>  

    
## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="0afc7-261">Fornecendo comentários sobre recursos experimentais</span><span class="sxs-lookup"><span data-stu-id="0afc7-261">Providing feedback on experimental features</span></span>  

<span data-ttu-id="0afc7-262">Para fornecer comentários sobre experimentos do Microsoft Edge DevTools ou qualquer outra coisa relacionada ao DevTools.</span><span class="sxs-lookup"><span data-stu-id="0afc7-262">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="0afc7-263">Enviar seus comentários usando o **ícone Enviar Comentários** no DevTools</span><span class="sxs-lookup"><span data-stu-id="0afc7-263">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="0afc7-264">Tweet no [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="0afc7-264">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="O ícone Enviar Comentários no Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="0afc7-266">O **ícone Enviar Comentários** no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0afc7-266">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Modo de exibição 3D | Microsoft Docs"  
[DevtoolsCssGrid]: ../css/grid.md "Inspecionar Grade CSS no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndex]: ../customize/index.md "Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Configurações - Personalizar o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Editar atalhos de teclado para qualquer ação no devTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]: ../customize/shortcuts.md#match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code "Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Editar estilos de fonte CSS e configurações no painel Estilos no DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../issues/index.md "Localizar e corrigir problemas com a ferramenta Issues do DevTools do Microsoft Edge | Microsoft Docs"  
[DevtoolsOpenIndex]: ../open/index.md "Abra o Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Atalhos de teclado do Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emular dispositivos de tela dupla e dobráveis no Microsoft Edge DevTools | Microsoft Docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
