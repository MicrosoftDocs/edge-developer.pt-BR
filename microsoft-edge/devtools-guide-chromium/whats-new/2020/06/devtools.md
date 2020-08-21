---
title: O que há de novo no DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f569414a95336278c93b1bbafd57153ca902df12
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942196"
---
# <span data-ttu-id="1a4d2-103">O que há de novo no DevTools (Microsoft Edge 85)</span><span class="sxs-lookup"><span data-stu-id="1a4d2-103">What's New In DevTools (Microsoft Edge 85)</span></span>  

## <span data-ttu-id="1a4d2-104">Anúncios da equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1a4d2-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="1a4d2-105">As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="1a4d2-106">Veja os comunicados para experimentar novos recursos no DevTools, extensões de código VS e muito mais.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-106">See the announcements to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="1a4d2-107">Para ficar atualizado sobre todos os recursos mais recentes e mais recentes em suas ferramentas de desenvolvedor, baixe os [canais de visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga a equipe do Microsoft Edge devtools no Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="1a4d2-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow the Microsoft Edge DevTools team on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="1a4d2-108">Recursos de depuração de grade CSS</span><span class="sxs-lookup"><span data-stu-id="1a4d2-108">CSS grid debugging features</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="1a4d2-110">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="1a4d2-110">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="1a4d2-111">A equipe do Microsoft Edge DevTools está colaborando com o Chrome DevTools Team e na Comunidade Chromium para adicionar novos recursos de depuração de grade CSS ao DevTools.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-111">The Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new CSS grid debugging features to DevTools.</span></span>  <span data-ttu-id="1a4d2-112">Agora você pode exibir números de linha de grade, lacunas de grade e linhas de grade estendidas como uma sobreposição na página.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-112">You are now able to display grid line numbers, grid gaps, and extended grid lines as an on-page overlay.</span></span>  <span data-ttu-id="1a4d2-113">Além disso, mais melhorias nas ferramentas de grade serão disponibilizadas em breve.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-113">Plus, more improvements to the grid tools are coming soon.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Recursos de depuração de grade CSS" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   <span data-ttu-id="1a4d2-115">Recursos de depuração de grade CSS</span><span class="sxs-lookup"><span data-stu-id="1a4d2-115">CSS grid debugging features</span></span>
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="1a4d2-116">Para habilitar o experimento, consulte [ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOn] e marque a caixa de seleção ao lado de **habilitar novos recursos de depuração de grade CSS**.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-116">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable new CSS Grid debugging features**.</span></span>  
> 
> <span data-ttu-id="1a4d2-117">Para experimentar o experimento com um exemplo, consulte [exemplo de planejador de grade CSS][CodepenRachelweilYzwBzKM].</span><span class="sxs-lookup"><span data-stu-id="1a4d2-117">To try out the experiment with a sample, see [CSS Grid planner example][CodepenRachelweilYzwBzKM].</span></span>  

<span data-ttu-id="1a4d2-118">Chromium problema [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-118">Chromium issue [#1047356][CR1047356]</span></span>  

### <span data-ttu-id="1a4d2-119">Editar e reproduzir solicitações com o console de rede</span><span class="sxs-lookup"><span data-stu-id="1a4d2-119">Edit and Replay requests with the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="1a4d2-121">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="1a4d2-121">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="1a4d2-122">Agora você pode usar **Editar e reproduzir** em solicitações no [log de rede][DevtoolsNetworkIndexLogActivity] usando o **console de rede**.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-122">You are now able to use **Edit and Replay** on requests in the [Network Log][DevtoolsNetworkIndexLogActivity] using the **Network Console**.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Editar e reproduzir uma solicitação no NetworkLog com o console de rede" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   <span data-ttu-id="1a4d2-124">Editar e reproduzir uma solicitação no [NetworkLog][DevtoolsNetworkIndexLogActivity] com o console de **rede**</span><span class="sxs-lookup"><span data-stu-id="1a4d2-124">Edit and Replay a request in the [NetworkLog][DevtoolsNetworkIndexLogActivity] with the **Network Console**</span></span>  
:::image-end:::  

<span data-ttu-id="1a4d2-125">Um novo painel, o **console de rede** abre na [gaveta devtools][DevtoolsCustomizeIndexDrawer] e preenche automaticamente com as informações da solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-125">A new panel, the **Network Console** opens in the [DevTools Drawer][DevtoolsCustomizeIndexDrawer] and automatically populates with information for the HTTP request.</span></span>  <span data-ttu-id="1a4d2-126">Para ver a resposta retornada do servidor, edite a solicitação \ (se necessário \) e selecione **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-126">To see the response returned from the server, edit the request \(if needed\) and select **Send**.</span></span>  

<span data-ttu-id="1a4d2-127">Você também pode usar o **console de rede** para criar e enviar solicitações HTTP diretamente do devtools.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-127">You may also use the **Network Console** to create and send HTTP requests directly from the DevTools.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Painel do console de rede" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   <span data-ttu-id="1a4d2-129">Painel do **console de rede**</span><span class="sxs-lookup"><span data-stu-id="1a4d2-129">The **Network Console** panel</span></span>  
:::image-end:::  

> [!TIP]
> <span data-ttu-id="1a4d2-130">Para ver o **console de rede** no painel main \ (superior \) em vez da [gaveta devtools][DevtoolsCustomizeIndexDrawer], consulte [movendo ferramentas entre painéis](#move-tools-between-panels).</span><span class="sxs-lookup"><span data-stu-id="1a4d2-130">To see **Network Console** in the main \(top\) panel instead of the [DevTools Drawer][DevtoolsCustomizeIndexDrawer], see [moving tools between panels](#move-tools-between-panels).</span></span>  

> [!NOTE]
> <span data-ttu-id="1a4d2-131">Para habilitar o experimento, consulte [ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOn] e marque a caixa de seleção ao lado de **habilitar console de rede**.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-131">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable Network Console**.</span></span>  
> 
> <span data-ttu-id="1a4d2-132">Abra o [log de rede][DevtoolsNetworkIndexLogActivity], abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **Editar e reproduzir**.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-132">Open the [Network Log][DevtoolsNetworkIndexLogActivity], open the contextual menu \(right-click\), and select **Edit and Replay**.</span></span>  

<span data-ttu-id="1a4d2-133">Chromium problema [#1093687][CR1093687]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-133">Chromium issue [#1093687][CR1093687]</span></span>  

### <span data-ttu-id="1a4d2-134">Eventos do trabalho do respondWith eventos na guia intervalo</span><span class="sxs-lookup"><span data-stu-id="1a4d2-134">Service worker respondWith events in the Timing tab</span></span>  

<span data-ttu-id="1a4d2-135">A guia **intervalo** do painel **rede** agora inclui `respondWith` eventos de trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-135">The **Timing** tab of the **Network** panel now includes `respondWith` service worker events.</span></span>  <span data-ttu-id="1a4d2-136">O `respondWith` evento de trabalho do serviço mostra a duração do tempo imediatamente antes de o manipulador de eventos do trabalho do serviço `fetch` começar a ser executado até o momento em que a `respondWith` promessa do `fetch` manipulador é liquidada.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-136">The `respondWith` service worker event shows the duration from the time immediately before the service worker `fetch` event handler starts running to the time when the `respondWith` promise of the `fetch` handler is settled.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="O evento de trabalho do serviço respondWith na guia intervalo do painel de rede" lightbox="../../media/2020/06/timing-tab.msft.png":::
   <span data-ttu-id="1a4d2-138">O `respondWith` evento de trabalho do serviço na guia **intervalo** do painel de **rede**</span><span class="sxs-lookup"><span data-stu-id="1a4d2-138">The `respondWith` service worker event in the **Timing** tab of the **Network** panel</span></span>  
:::image-end:::  

<span data-ttu-id="1a4d2-139">Expanda a **resposta recebida** para ver informações adicionais da `fetch` resposta como `CacheStorageCacheName` , `serviceWorkerResponseSource` e `ResponseTime` .</span><span class="sxs-lookup"><span data-stu-id="1a4d2-139">Expand **Response received** to see additional information from the `fetch` response like `CacheStorageCacheName`, `serviceWorkerResponseSource`, and `ResponseTime`.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Expandir a resposta recebida para ver informações adicionais da resposta de busca" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   <span data-ttu-id="1a4d2-141">Expandir a **resposta recebida** para ver informações adicionais da `fetch` resposta</span><span class="sxs-lookup"><span data-stu-id="1a4d2-141">Expand **Response received** to see additional information from the `fetch` response</span></span>  
:::image-end:::  

<span data-ttu-id="1a4d2-142">Chromium problema [#1066579][CR1066579]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-142">Chromium issue [#1066579][CR1066579]</span></span>  

### <span data-ttu-id="1a4d2-143">Comentários da webhint no painel problemas</span><span class="sxs-lookup"><span data-stu-id="1a4d2-143">webhint feedback in the Issues panel</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="1a4d2-145">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="1a4d2-145">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="1a4d2-146">[webhint][WebhintMain] é uma ferramenta de código-fonte aberto que fornece comentários em tempo real sobre a acessibilidade, a compatibilidade entre navegadores, a segurança, o desempenho, a PWAs e outras questões de desenvolvimento da Web comuns dos sites.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-146">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="1a4d2-147">Agora você pode ver comentários da webhint no painel [problemas][DevtoolsIssues] .</span><span class="sxs-lookup"><span data-stu-id="1a4d2-147">You are now able to see webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="Comentários da webhint no painel problemas" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   <span data-ttu-id="1a4d2-149">Comentários da webhint no painel problemas</span><span class="sxs-lookup"><span data-stu-id="1a4d2-149">webhint feedback in the Issues panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="1a4d2-150">Para habilitar o experimento, consulte [ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOn] e marque a caixa de seleção ao lado de **habilitar webhint**.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-150">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable webhint**.</span></span>  
> 
> <span data-ttu-id="1a4d2-151">Abra o painel [problemas][DevtoolsIssues] para ver os comentários da webhint.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-151">Open the [Issues][DevtoolsIssues] panel to see feedback from webhint.</span></span>  

<span data-ttu-id="1a4d2-152">Chromium problema [#1070378][CR1070378]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-152">Chromium issue [#1070378][CR1070378]</span></span>  

### <span data-ttu-id="1a4d2-153">Ferramentas de movimentação entre painéis</span><span class="sxs-lookup"><span data-stu-id="1a4d2-153">Move tools between panels</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="1a4d2-155">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="1a4d2-155">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="1a4d2-156">Normalmente, ferramentas como **elementos** e **rede** só podem ser abertas no painel main \ (Top \) do devtools.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-156">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="1a4d2-157">Da mesma forma, ferramentas como **modo de exibição 3D** e **problemas** só podem ser abertos no painel gaveta \ (inferior \) do devtools.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-157">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="1a4d2-158">Agora você pode personalizar o layout do DevTools movendo ferramentas entre os painéis superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-158">You are now able to customize your DevTools layout by moving tools between the top and bottom panels.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Mover guias entre painéis" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   <span data-ttu-id="1a4d2-160">Mover guias entre painéis</span><span class="sxs-lookup"><span data-stu-id="1a4d2-160">Moving tabs between panels</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="1a4d2-161">Para habilitar o experimento, consulte [ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOn] e marque a caixa de seleção ao lado de **habilitar o suporte para mover as guias entre painéis**.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-161">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable support to move tabs between panels**.</span></span>  

<span data-ttu-id="1a4d2-162">Chromium problema [#897944][CR897944]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-162">Chromium issue [#897944][CR897944]</span></span>  

### <span data-ttu-id="1a4d2-163">Dica de ferramenta do iniciador aprimorada no painel rede</span><span class="sxs-lookup"><span data-stu-id="1a4d2-163">Improved Initiator tooltip in the Network panel</span></span>  

<span data-ttu-id="1a4d2-164">No Microsoft Edge 83 e no 84, as dicas de ferramenta para a coluna do iniciador, que mostra a causa da solicitação do recurso, no [log de rede][DevtoolsNetworkIndexLogActivity] exibido com uma barra de rolagem horizontal.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-164">In Microsoft Edge 83 and 84, tooltips for the Initiator column, which shows the cause of the resource request, in the [Network Log][DevtoolsNetworkIndexLogActivity] displayed with a horizontal scrollbar.</span></span>  <span data-ttu-id="1a4d2-165">Você só pôde ver a pilha de chamadas que iniciou a solicitação rolando horizontalmente na dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-165">You were only able to see the call stack that initiated the request by scrolling horizontally in the tooltip.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="A dica de ferramenta do iniciador no Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   <span data-ttu-id="1a4d2-167">A dica de ferramenta do iniciador no Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="1a4d2-167">The Initiator tooltip in Microsoft Edge 84</span></span>  
:::image-end:::  

<span data-ttu-id="1a4d2-168">Começando com o Microsoft Edge 85, agora você pode ver a pilha de chamadas do iniciador na dica de ferramenta sem rolar horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-168">Starting with Microsoft Edge 85, you are now able to see the Initiator call stack in the tooltip without scrolling horizontally.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="A dica de ferramenta do iniciador no Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   <span data-ttu-id="1a4d2-170">A dica de ferramenta do iniciador no Microsoft Edge 85</span><span class="sxs-lookup"><span data-stu-id="1a4d2-170">The Initiator tooltip in Microsoft Edge 85</span></span>
:::image-end:::  

<span data-ttu-id="1a4d2-171">Chromium problema [#1069404][CR1069404]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-171">Chromium issue [#1069404][CR1069404]</span></span>  

## <span data-ttu-id="1a4d2-172">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="1a4d2-172">Announcements from the Chromium project</span></span>  

<span data-ttu-id="1a4d2-173">As seções a seguir anunciarão recursos adicionais disponíveis no Microsoft Edge 85 que contribuíram para o projeto de código-fonte aberto Chromium.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-173">The following sections announce additional features available in Microsoft Edge 85 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="1a4d2-174">Edição de estilo para estruturas CSS-in-JS</span><span class="sxs-lookup"><span data-stu-id="1a4d2-174">Style editing for CSS-in-JS frameworks</span></span>  

<span data-ttu-id="1a4d2-175">Agora, o painel **estilos** tem melhor suporte para edição de estilos que foram criados com as APIs do [modelo de objeto CSS (CSSOM)][CsswgDraftsCssom] .</span><span class="sxs-lookup"><span data-stu-id="1a4d2-175">The **Styles** pane now has better support for editing styles that were created with the [CSS Object Model (CSSOM)][CsswgDraftsCssom] APIs.</span></span>  <span data-ttu-id="1a4d2-176">Muitas estruturas e bibliotecas CSS-in-JS usam as APIs CSSOM nos bastidores para construir estilos.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-176">Many CSS-in-JS frameworks and libraries use the CSSOM APIs under the hood to construct styles.</span></span>  

<span data-ttu-id="1a4d2-177">Agora você pode editar estilos adicionados em JavaScript usando folhas de [estilo construíveis][WicgConstructStylesheet].</span><span class="sxs-lookup"><span data-stu-id="1a4d2-177">You are now able to edit styles added in JavaScript using [Constructable Stylesheets][WicgConstructStylesheet].</span></span>  <span data-ttu-id="1a4d2-178">As folhas de estilo construíveis são uma nova maneira de criar e distribuir estilos reutilizáveis ao usar o [dom de sombra][MdnShadowDom].</span><span class="sxs-lookup"><span data-stu-id="1a4d2-178">Constructable Stylesheets are a new way to create and distribute reusable styles when using [Shadow DOM][MdnShadowDom].</span></span>  

<span data-ttu-id="1a4d2-179">Por exemplo, os `h1` estilos adicionados com `CSSStyleSheet` \ (APIs CSSOM \) não eram editáveis anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-179">For example, the `h1` styles added with `CSSStyleSheet` \(CSSOM APIs\) were not editable previously.</span></span>  <span data-ttu-id="1a4d2-180">Os estilos são editáveis agora no painel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="1a4d2-180">The styles are editable now in the **Styles** pane.</span></span>  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Alterar a propriedade Background dos estilos H1 adicionados com CSSStyleSheet de rosa a LightBlue" lightbox="../../media/2020/06/css-in-js.msft.png":::
   <span data-ttu-id="1a4d2-182">Alterar a `background` propriedade dos `h1` estilos adicionados com `CSSStyleSheet` from `pink` to `lightblue` .</span><span class="sxs-lookup"><span data-stu-id="1a4d2-182">Changing the `background` property of the `h1` styles added with `CSSStyleSheet` from `pink` to `lightblue`.</span></span>
:::image-end:::  

<span data-ttu-id="1a4d2-183">Dê a esse recurso uma tentativa com um [exemplo que usa CSS-in-js][CodepenZoherghadyaliAbdgrpz].</span><span class="sxs-lookup"><span data-stu-id="1a4d2-183">Give this feature a try with a [sample that uses CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span></span>

<span data-ttu-id="1a4d2-184">Chromium problema [#946975][CR946975]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-184">Chromium issue [#946975][CR946975]</span></span>  

### <span data-ttu-id="1a4d2-185">Lighthouse 6 no painel Lighthouse</span><span class="sxs-lookup"><span data-stu-id="1a4d2-185">Lighthouse 6 in the Lighthouse panel</span></span>  

<span data-ttu-id="1a4d2-186">O painel **Lighthouse** agora está em execução Lighthouse 6.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-186">The **Lighthouse** panel is now running Lighthouse 6.</span></span>  <span data-ttu-id="1a4d2-187">Para obter uma lista completa de todas as alterações, consulte [notas de versão do v 6.0.0][GithubGoogleChromeLighthouse600].</span><span class="sxs-lookup"><span data-stu-id="1a4d2-187">For a full list of all changes, see [v6.0.0 release notes][GithubGoogleChromeLighthouse600].</span></span>  

<span data-ttu-id="1a4d2-188">O Lighthouse 6,0 introduz três novas métricas para o relatório: maior pintura de conteúdo \ (LCP \), deslocamento de layout cumulativo \ (CLS \) e tempo de bloqueio total \ (TBT \).</span><span class="sxs-lookup"><span data-stu-id="1a4d2-188">Lighthouse 6.0 introduces three new metrics to the report:  Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\), and Total Blocking Time \(TBT\).</span></span>  

<span data-ttu-id="1a4d2-189">A fórmula de Pontuação de desempenho também foi reponderada para refletir melhor a experiência de carregamento do usuário.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-189">The performance score formula has also been reweighted to better reflect the loading experience of the user.</span></span>  

<span data-ttu-id="1a4d2-190">Chromium problema [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-190">Chromium issue [#772558][CR772558]</span></span>  

#### <span data-ttu-id="1a4d2-191">Primeira substituição de pintura significativa</span><span class="sxs-lookup"><span data-stu-id="1a4d2-191">First Meaningful Paint deprecation</span></span>  

<span data-ttu-id="1a4d2-192">O primeiro pintura FMP \ (\) está obsoleto no Lighthouse 6,0.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-192">First Meaningful Paint \(FMP\) is deprecated in Lighthouse 6.0.</span></span>  <span data-ttu-id="1a4d2-193">O FMP também foi removido do painel **desempenho** .</span><span class="sxs-lookup"><span data-stu-id="1a4d2-193">FMP has also been removed from the **Performance** panel.</span></span>  <span data-ttu-id="1a4d2-194">**Maior pintura com conteúdo** é o substituto recomendado para FMP.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-194">**Largest Contentful Paint** is the recommended replacement for FMP.</span></span>  <!--See [First Meaningful Paint][WebDevFirstMeaningfulPaint] for an explanation of why it was deprecated.  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

<span data-ttu-id="1a4d2-195">Chromium problema [#1096008][CR1096008]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-195">Chromium issue [#1096008][CR1096008]</span></span>  

### <span data-ttu-id="1a4d2-196">Suporte para novos recursos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="1a4d2-196">Support for new JavaScript features</span></span>  

<span data-ttu-id="1a4d2-197">O DevTools agora tem melhor suporte para alguns dos recursos de linguagem JavaScript mais recentes.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-197">DevTools now has better support for some of the latest JavaScript language features.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="1a4d2-198">Conclusão automática da sintaxe de [encadeamento opcional][V8DevOptionalChaining]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-198">[Optional chaining][V8DevOptionalChaining] syntax autocompletion</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="1a4d2-199">A conclusão automática de propriedades no **console** agora oferece suporte à sintaxe de encadeamento opcional, por exemplo,  `name?.` agora funciona além de `name.` e `name[` .</span><span class="sxs-lookup"><span data-stu-id="1a4d2-199">Property auto-completion in the **Console** now supports optional chaining syntax, for example,  `name?.` now works in addition to `name.` and `name[`.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="1a4d2-200">Realce de sintaxe para [campos particulares][V8DevClassFieldsPrivate]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-200">Syntax highlighting for [private fields][V8DevClassFieldsPrivate]</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="1a4d2-201">os campos de classe particular agora têm a sintaxe corretamente realçada e bem impressas no painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="1a4d2-201">private class fields are now properly syntax-highlighted and pretty-printed in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="1a4d2-202">Realce de sintaxe para [operadora de União NULL][V8DevNullishCoalescing] esficado</span><span class="sxs-lookup"><span data-stu-id="1a4d2-202">Syntax highlighting for [Nullish coalescing operator][V8DevNullishCoalescing]</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="1a4d2-203">Agora, o DevTools agora realmente imprime o operador de União NULL esficado no painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="1a4d2-203">DevTools now properly pretty-prints the nullish coalescing operator in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="1a4d2-204">Problemas com o Chromium [#1073903][CR1073903], [#1083214][CR1083214] [#1083797][CR1083797]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-204">Chromium issues [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span></span>  

### <span data-ttu-id="1a4d2-205">Novos avisos de atalho do aplicativo no painel manifesto</span><span class="sxs-lookup"><span data-stu-id="1a4d2-205">New app shortcut warnings in the Manifest pane</span></span>  

<span data-ttu-id="1a4d2-206">Os **atalhos do aplicativo** ajudam os usuários a iniciar rapidamente tarefas comuns ou recomendadas em um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-206">**App shortcuts** help users quickly start common or recommended tasks within a web app.</span></span>  

<!--todo: add App shortcuts when section is live  -->  

<span data-ttu-id="1a4d2-207">O painel **manifestar** agora mostra avisos para as seguintes condições.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-207">The **Manifest** pane now shows warnings for the following conditions.</span></span>  

* <span data-ttu-id="1a4d2-208">Os ícones de atalho do aplicativo são menores do que 96x96 pixels</span><span class="sxs-lookup"><span data-stu-id="1a4d2-208">The app shortcut icons are smaller than 96x96 pixels</span></span>  
* <span data-ttu-id="1a4d2-209">Os ícones de atalho e os ícones de manifesto do aplicativo não são quadrados \ (já que os ícones são ignorados \)</span><span class="sxs-lookup"><span data-stu-id="1a4d2-209">The app shortcut icons and manifest icons are not square \(since the icons are ignored\)</span></span>  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Avisos de atalho do aplicativo" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   <span data-ttu-id="1a4d2-211">Avisos de atalho do aplicativo</span><span class="sxs-lookup"><span data-stu-id="1a4d2-211">App shortcut warnings</span></span>  
:::image-end:::  

<span data-ttu-id="1a4d2-212">Chromium problema [#955497][CR955497]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-212">Chromium issue [#955497][CR955497]</span></span>  

### <span data-ttu-id="1a4d2-213">Exibição consistente do painel calculado</span><span class="sxs-lookup"><span data-stu-id="1a4d2-213">Consistent display of the Computed pane</span></span>  

<span data-ttu-id="1a4d2-214">O painel **calculado** no painel de **elementos** agora é exibido consistentemente em um painel em todos os tamanhos do visor.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-214">The **Computed** pane in the **Elements** panel now displays consistently as a pane across all viewport sizes.</span></span>  <span data-ttu-id="1a4d2-215">Anteriormente, o painel **calculado** foi mesclado dentro do painel **estilos** quando a largura do visor devtools era estreita.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-215">Previously the **Computed** pane merged inside the **Styles** pane when the width of the DevTools viewport was narrow.</span></span>  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="O painel calculado é exibido consistentemente como um painel separado, mesmo quando o DevTools é estreito" lightbox="../../media/2020/06/computed-pane.msft.png":::
   <span data-ttu-id="1a4d2-217">O painel **calculado** é exibido consistentemente como um painel separado, mesmo quando os devtools são estreitos.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-217">The **Computed** pane consistently displays as a separate pane even when the DevTools are narrow.</span></span>
:::image-end:::  

<span data-ttu-id="1a4d2-218">Chromium problema [#1073899][CR1073899]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-218">Chromium issue [#1073899][CR1073899]</span></span>  

### <span data-ttu-id="1a4d2-219">Deslocamentos de código de bytes para arquivos Webassembly</span><span class="sxs-lookup"><span data-stu-id="1a4d2-219">Bytecode offsets for WebAssembly files</span></span>  

<span data-ttu-id="1a4d2-220">O DevTools agora usa deslocamentos de código de bytes para exibir números de linha de desmontagem de WASM.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-220">DevTools now uses bytecode offsets for displaying line numbers of Wasm disassembly.</span></span>  
<span data-ttu-id="1a4d2-221">Os números de linha tornam mais claro que você está olhando para dados binários e é mais consistente com a maneira como o tempo de execução do WASM faz referência a locais.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-221">The line numbers make it clearer that you are looking at binary data, and is more consistent with how the Wasm runtime references locations.</span></span>  

<span data-ttu-id="1a4d2-222">Chromium problema [#1071432][CR1071432]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-222">Chromium issue [#1071432][CR1071432]</span></span>  

### <span data-ttu-id="1a4d2-223">Painel copiar e recortar linhas em fontes</span><span class="sxs-lookup"><span data-stu-id="1a4d2-223">Line-wise copy and cut in Sources Panel</span></span>  

<span data-ttu-id="1a4d2-224">Ao fazer a cópia ou recortar sem seleção no [Editor de painel fontes][DevtoolsSourcesEditCssJavascript], o devtools copia ou recorta a linha atual do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-224">When performing copy or cut with no selection in the [Sources panel editor][DevtoolsSourcesEditCssJavascript], DevTools copies or cuts the current line of content.</span></span>  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Com o cursor no final da linha 5, copiar a linha inteira de pen.js no DevTools e colar em um código VS" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   <span data-ttu-id="1a4d2-226">Com o cursor no final da linha 5, copiar a linha inteira de **pen.js** no devtools e colar no [vs Code][VSCode].</span><span class="sxs-lookup"><span data-stu-id="1a4d2-226">With the cursor at the end of Line 5, copying the whole line from **pen.js** in the DevTools and pasting in [VS Code][VSCode].</span></span>
:::image-end:::  

<span data-ttu-id="1a4d2-227">Chromium problema [#800028][CR800028]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-227">Chromium issue [#800028][CR800028]</span></span>

### <span data-ttu-id="1a4d2-228">Atualizações de configurações do console</span><span class="sxs-lookup"><span data-stu-id="1a4d2-228">Console Settings updates</span></span>  

#### <span data-ttu-id="1a4d2-229">Desagrupar as mesmas mensagens do console</span><span class="sxs-lookup"><span data-stu-id="1a4d2-229">Ungroup same console messages</span></span>  

<span data-ttu-id="1a4d2-230">A opção de alternância **semelhante em grupo** nas configurações do console agora se aplica a mensagens duplicadas.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-230">The **Group similar** toggle in Console Settings now applies to duplicate messages.</span></span>  <span data-ttu-id="1a4d2-231">Anteriormente, ele era aplicado apenas a mensagens semelhantes.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-231">Previously it just applied to similar messages.</span></span>  

<span data-ttu-id="1a4d2-232">Por exemplo, anteriormente, o DevTools não desagrupau as `hello` mensagens, apesar de o **grupo semelhante** não estar desmarcado.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-232">For example, previously, DevTools did not ungroup the `hello` messages even though **Group similar** is unchecked.</span></span>  <span data-ttu-id="1a4d2-233">Agora, as `hello` mensagens são desagrupadas.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-233">Now, the `hello` messages are ungrouped.</span></span>  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Quando o grupo semelhante está desmarcado, as mensagens de saudação são desagrupadas" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   <span data-ttu-id="1a4d2-235">Quando o **grupo semelhante** está desmarcado, as `hello` mensagens são desagrupadas.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-235">When **Group similar** is unchecked, the `hello` messages are ungrouped.</span></span>
:::image-end:::  

<span data-ttu-id="1a4d2-236">Dê esse recurso uma tentativa com um [exemplo que envia mensagens duplicadas ao console][CodepenZoherghadyaliZyrjgdJ].</span><span class="sxs-lookup"><span data-stu-id="1a4d2-236">Give this feature a try with a [sample that sends duplicate messages to the Console][CodepenZoherghadyaliZyrjgdJ].</span></span>  

<span data-ttu-id="1a4d2-237">Chromium problema [#1082963][CR1082963]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-237">Chromium issue [#1082963][CR1082963]</span></span>  

### <span data-ttu-id="1a4d2-238">Mantendo somente as configurações de contexto selecionado</span><span class="sxs-lookup"><span data-stu-id="1a4d2-238">Persisting Selected context only settings</span></span>  

<span data-ttu-id="1a4d2-239">As configurações de **contexto selecionado somente** em configurações do console agora são mantidas.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-239">The **Selected context only** settings in Console Settings is now persisted.</span></span>  <span data-ttu-id="1a4d2-240">Anteriormente, as configurações foram redefinidas toda vez que você fechou e reabriu o DevTools.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-240">Previously the settings were reset every time you closed and reopened DevTools.</span></span>  <span data-ttu-id="1a4d2-241">A alteração torna o comportamento de configuração consistente com outras opções de configurações do console.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-241">The change makes the setting behavior consistent with other Console Settings options.</span></span>  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Configuração somente contexto selecionada" lightbox="../../media/2020/06/selected-context.msft.png":::
   <span data-ttu-id="1a4d2-243">Configuração **somente contexto selecionada**</span><span class="sxs-lookup"><span data-stu-id="1a4d2-243">**Selected context only** setting</span></span>  
:::image-end:::  

<span data-ttu-id="1a4d2-244">Chromium problema [#1055875][CR1055875]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-244">Chromium issue [#1055875][CR1055875]</span></span>  

### <span data-ttu-id="1a4d2-245">Atualizações do painel de desempenho</span><span class="sxs-lookup"><span data-stu-id="1a4d2-245">Performance panel updates</span></span>  

#### <span data-ttu-id="1a4d2-246">Informações de cache de compilação JavaScript no painel desempenho</span><span class="sxs-lookup"><span data-stu-id="1a4d2-246">JavaScript compilation cache information in Performance panel</span></span>  

<span data-ttu-id="1a4d2-247">[As informações do cache de compilação do JavaScript][V8DevCodeCaching] agora são sempre exibidas na guia Resumo do painel desempenho.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-247">[JavaScript compilation cache information][V8DevCodeCaching] is now always displayed in the Summary tab of the Performance panel.</span></span>  <span data-ttu-id="1a4d2-248">Anteriormente, o DevTools não mostraria nada relacionado ao cache de código se o cache de código não existisse.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-248">Previously, DevTools did not show anything related to code caching if code caching did not happen.</span></span>  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Informações do cache de compilação JavaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   <span data-ttu-id="1a4d2-250">Informações do cache de compilação JavaScript</span><span class="sxs-lookup"><span data-stu-id="1a4d2-250">JavaScript compilation cache information</span></span>  
:::image-end:::  

<span data-ttu-id="1a4d2-251">Chromium problema [#912581][CR912581]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-251">Chromium issue [#912581][CR912581]</span></span>  

#### <span data-ttu-id="1a4d2-252">Alinhamento do tempo de navegação no painel desempenho</span><span class="sxs-lookup"><span data-stu-id="1a4d2-252">Navigation timing alignment in the Performance panel</span></span>  

<span data-ttu-id="1a4d2-253">O painel de **desempenho** usado para mostrar horas nas réguas com base na hora de início da gravação.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-253">The **Performance** panel used to show times in the rulers based on when the recording started.</span></span>  <span data-ttu-id="1a4d2-254">O intervalo foi alterado para gravações nas quais o usuário navega, onde DevTools agora mostra as horas da régua em relação à navegação em vez disso.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-254">The timing has now changed for recordings where the user navigates, where DevTools now shows ruler times relative to the navigation instead.</span></span>  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Alinhar o intervalo de navegação no painel de desempenho" lightbox="../../media/2020/06/nav-timing.msft.png":::
   <span data-ttu-id="1a4d2-256">Alinhar o intervalo de navegação no painel de **desempenho**</span><span class="sxs-lookup"><span data-stu-id="1a4d2-256">Align navigation timing in **Performance** panel</span></span>  
:::image-end:::  

<span data-ttu-id="1a4d2-257">As horas para `DOMContentLoaded` , primeiro pintura, primeira pintura com conteúdo e maiores eventos de pintura com conteúdo são atualizadas para serem relativas ao início da navegação, o que significa que o intervalo corresponde aos intervalos relatados por `PerformanceObserver` .</span><span class="sxs-lookup"><span data-stu-id="1a4d2-257">The times for `DOMContentLoaded`, First Paint, First Contentful Paint, and Largest Contentful Paint events are updated to be relative to the start of the navigation, which means the timing matches the timings reported by `PerformanceObserver`.</span></span>  

<span data-ttu-id="1a4d2-258">Chromium problema [#974550][CR974550]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-258">Chromium issue [#974550][CR974550]</span></span>  

### <span data-ttu-id="1a4d2-259">Novos ícones para pontos de interrupção, pontos de interrupção condicionais e logpoints</span><span class="sxs-lookup"><span data-stu-id="1a4d2-259">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="1a4d2-260">O painel **fontes** tem novos designs para pontos de interrupção, pontos de interrupção condicionais e logpoints.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-260">The **Sources** panel has new designs for breakpoints, conditional breakpoints, and logpoints.</span></span>  <span data-ttu-id="1a4d2-261">Os pontos de interrupção são representados por um círculo vermelho, da mesma forma que o [código vs][VSCode] e o [Visual Studio][VS].</span><span class="sxs-lookup"><span data-stu-id="1a4d2-261">Breakpoints are represented by a red circle, just like [VS Code][VSCode] and [Visual Studio][VS].</span></span>  <span data-ttu-id="1a4d2-262">Ícones são adicionados para diferenciar pontos de interrupção condicionais e logpoints.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-262">Icons are added to differentiate conditional breakpoints and logpoints.</span></span>  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Pontos de interrupção" lightbox="../../media/2020/06/breakpoints.msft.png":::
   <span data-ttu-id="1a4d2-264">Pontos de interrupção</span><span class="sxs-lookup"><span data-stu-id="1a4d2-264">Breakpoints</span></span>  
:::image-end:::  

<span data-ttu-id="1a4d2-265">Chromium problema [#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="1a4d2-265">Chromium issue [#1041830][CR1041830]</span></span>  

## <span data-ttu-id="1a4d2-266">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a4d2-266">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="1a4d2-267">Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-267">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="1a4d2-268">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-268">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="1a4d2-269">Como entrar em contato com o Microsoft Edge DevTools equipe</span><span class="sxs-lookup"><span data-stu-id="1a4d2-269">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Gaveta-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Ativar recursos experimentais-recursos experimentais | Documentos da Microsoft"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Localizar e corrigir problemas com a ferramenta problemas do DevTools Microsoft Edge | Documentos da Microsoft"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Visão geral do painel Editar CSS e JavaScript-fontes | Documentos da Microsoft"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Registrar atividades de rede-Inspecione a atividade de rede no Microsoft Edge DevTools | Documentos da Microsoft"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Edição de estilo para estruturas CSS-in-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Enviar mensagens duplicadas para o console | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Exemplo de Planner de grade CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros de Chromium"  

[CR772558]: https://crbug.com/772558 "DevTools: Atualize para a versão mais recente do Lighthouse | Erros de Chromium"  
[CR800028]: https://crbug.com/800028 "O atalho de linha duplicada no editor de ferramentas de desenvolvedor não está funcionando após a atualização do Chrome | Erros de Chromium"  
[CR912581]: https://crbug.com/912581 "Expor quais scripts foram armazenados em cache por V8 no DevTools/about: Tracing | Erros de Chromium"  
[CR946975]: https://crbug.com/946975 "A barra lateral estilos DevTools não funciona com folhas de estilos construídas | Erros de Chromium"  
[CR955497]: https://crbug.com/955497 "Menu de atalho do ícone do aplicativo para PWAs | Erros de Chromium"  
[CR974550]: https://crbug.com/974550 "Diferença de métrica entre o painel perf e performanceObserver | Erros de Chromium"  
[CR1041830]: https://crbug.com/1041830 "Melhorar as cores dos pontos de interrupção | Erros de Chromium"  
[CR1055875]: https://crbug.com/1055875 "O valor da configuração do console somente contexto selecionado não persiste após fechar e reabrir as ferramentas de desenvolvedor | Erros de Chromium"  
[CR1066579]: https://crbug.com/1066579 "DevTools: show inworkrs busca a linha do tempo por solicitação no painel de rede | Erros de Chromium"  
[CR1071432]: https://crbug.com/1071432 "WASM experiência básica para desenvolvedores | Erros de Chromium"  
[CR1073899]: https://crbug.com/1073899 "Guia estilo calculado desaparece no modo responsivo | Erros de Chromium"  
[CR1073903]: https://crbug.com/1073903 "DevTools: o realce de sintaxe não funciona com campos particulares | Erros de Chromium"  
[CR1082963]: https://crbug.com/1082963 "Não é possível desativar o comportamento de mensagens semelhantes em grupo do console | Erros de Chromium"  
[CR1083214]: https://crbug.com/1083214 "o Acorn não dá suporte a encadeamento opcional | Erros de Chromium"  
[CR1083797]: https://crbug.com/1083797 "Impressão bonita interrompida para União nula esficarada | Erros de Chromium"  
[CR1096008]: https://crbug.com/1096008 "Remover FMP | Erros de Chromium"  
[CR1047356]: https://crbug.com/1047356 "Ferramentas de grade/flexbox/tabela CSS | Erros de Chromium"  
[CR1093687]: https://crbug.com/1093687 "Crie uma ferramenta para criar e reproduzir solicitações de rede sintéticas | Erros de Chromium"  
[CR1070378]: https://crbug.com/1070378 "Integrar dica WebA DevTools | Erros de Chromium"  
[CR1069404]: https://crbug.com/1069404 "[Ferramentas de desenvolvimento] os pop-ups do widget são muito estreitas | Erros de Chromium"  
[CR897944]: https://crbug.com/897944 "Painéis devtool arrastáveis | Erros de Chromium"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v 6.0.0-GoogleChrome/Lighthouse | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Novo problema-MicrosoftDocs/Edge-Developer"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Usando o DOM de sombra | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Canais de visualização do Microsoft Edge"  

[VS]: https://visualstudio.microsoft.com/ "Visual Studio"
[VSCode]: https://code.visualstudio.com/ "Código do Visual Studio"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Modelo de objeto CSS (CSSOM) | Rascunhos do editor de grupo de trabalho W3C CSS"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Postar um tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools conta do Twitter"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Campos de classe particular-campos de classe pública e particular | V8. Dispositivos"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Cache de código para desenvolvedores de JavaScript | V8. Dispositivos"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "União esnulada nula | V8. Dispositivos"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Encadeamento opcional | V8. Dispositivos"  

[WebhintMain]: https://webhint.io "webhint"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Objetos de folha de estilos construíveis | Web Incubator CG"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "A Web que queremos"  

> [!NOTE]
> <span data-ttu-id="1a4d2-318">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="1a4d2-318">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1a4d2-319">A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/06/devtools/index) e é criada por [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="1a4d2-319">The original page is found [here](https://developers.google.com/web/updates/2020/06/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1a4d2-321">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1a4d2-321">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
