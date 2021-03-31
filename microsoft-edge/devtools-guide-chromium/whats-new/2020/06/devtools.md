---
description: Recursos de depuração de grade CSS, solicitações de Edição e Repetição com o Console de Rede e muito mais.
title: Novidades no DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 9031f817a6079f64352c261a70eb9581213bf8c7
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408315"
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
# <a name="whats-new-in-devtools-microsoft-edge-85"></a><span data-ttu-id="48433-104">Novidades no DevTools (Microsoft Edge 85)</span><span class="sxs-lookup"><span data-stu-id="48433-104">What's New In DevTools (Microsoft Edge 85)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="48433-105">Comunicados da equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="48433-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="48433-106">As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="48433-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="48433-107">Confira os comunicados para experimentar novos recursos no DevTools, no Microsoft Visual Studio Code e muito mais.</span><span class="sxs-lookup"><span data-stu-id="48433-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="48433-108">Para ficar atualizado sobre todos os recursos mais recentes e maiores em suas ferramentas de desenvolvedor, baixe os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] e siga a equipe do Microsoft [Edge DevTools no Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="48433-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow the Microsoft Edge DevTools team on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="css-grid-debugging-features"></a><span data-ttu-id="48433-109">Recursos de depuração de grade CSS</span><span class="sxs-lookup"><span data-stu-id="48433-109">CSS grid debugging features</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="48433-111">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="48433-111">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="48433-112">A equipe do Microsoft Edge DevTools está colaborando com a equipe do Chrome DevTools e com a comunidade do Chromium para adicionar novos recursos de depuração de grade CSS ao DevTools.</span><span class="sxs-lookup"><span data-stu-id="48433-112">The Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new CSS grid debugging features to DevTools.</span></span>  <span data-ttu-id="48433-113">Agora você pode exibir números de linha de grade, lacunas de grade e linhas de grade estendidas como uma sobreposição na página.</span><span class="sxs-lookup"><span data-stu-id="48433-113">You are now able to display grid line numbers, grid gaps, and extended grid lines as an on-page overlay.</span></span>  <span data-ttu-id="48433-114">Além disso, mais melhorias nas ferramentas de grade estão chegando em breve.</span><span class="sxs-lookup"><span data-stu-id="48433-114">Plus, more improvements to the grid tools are coming soon.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Recursos de depuração de grade CSS" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   <span data-ttu-id="48433-116">Recursos de depuração de grade CSS</span><span class="sxs-lookup"><span data-stu-id="48433-116">CSS grid debugging features</span></span>
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="48433-117">Para habilitar o experimento, navegue até Ativar recursos [experimentais][DevtoolsExperimentalFeaturesTurnOn] e selecione a caixa de seleção ao lado de Habilitar novos recursos **de depuração de GRADE CSS.**</span><span class="sxs-lookup"><span data-stu-id="48433-117">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable new CSS Grid debugging features**.</span></span>  
> 
> <span data-ttu-id="48433-118">Para experimentar o experimento com um exemplo, navegue até [CSS Grid planner example][CodepenRachelweilYzwBzKM].</span><span class="sxs-lookup"><span data-stu-id="48433-118">To try out the experiment with a sample, navigate to [CSS Grid planner example][CodepenRachelweilYzwBzKM].</span></span>  

<span data-ttu-id="48433-119">Problema do Chromium [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="48433-119">Chromium issue [#1047356][CR1047356]</span></span>  

### <a name="edit-and-replay-requests-with-the-network-console"></a><span data-ttu-id="48433-120">Editar e repetir solicitações com o Console de Rede</span><span class="sxs-lookup"><span data-stu-id="48433-120">Edit and Replay requests with the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="48433-122">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="48433-122">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="48433-123">Agora você pode usar **Editar e Repetir** solicitações no Log de [Rede][DevtoolsNetworkIndexLogActivity] usando o Console **de Rede.**</span><span class="sxs-lookup"><span data-stu-id="48433-123">You are now able to use **Edit and Replay** on requests in the [Network Log][DevtoolsNetworkIndexLogActivity] using the **Network Console**.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Editar e repetir uma solicitação no NetworkLog com o Console de Rede" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   <span data-ttu-id="48433-125">Editar e repetir uma solicitação no [NetworkLog][DevtoolsNetworkIndexLogActivity] com o **Console de Rede**</span><span class="sxs-lookup"><span data-stu-id="48433-125">Edit and Replay a request in the [NetworkLog][DevtoolsNetworkIndexLogActivity] with the **Network Console**</span></span>  
:::image-end:::  

<span data-ttu-id="48433-126">Um novo painel, o **Console de Rede** é aberto na Gaveta de [DevTools][DevtoolsCustomizeIndexDrawer] e preenche automaticamente com informações para a solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="48433-126">A new panel, the **Network Console** opens in the [DevTools Drawer][DevtoolsCustomizeIndexDrawer] and automatically populates with information for the HTTP request.</span></span>  <span data-ttu-id="48433-127">Para exibir a resposta retornada do servidor, edite a solicitação \(se necessário\) e selecione **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="48433-127">To display the response returned from the server, edit the request \(if needed\) and select **Send**.</span></span>  

<span data-ttu-id="48433-128">Você também pode usar o **Console de Rede** para criar e enviar solicitações HTTP diretamente do DevTools.</span><span class="sxs-lookup"><span data-stu-id="48433-128">You may also use the **Network Console** to create and send HTTP requests directly from the DevTools.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="O painel Console de Rede" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   <span data-ttu-id="48433-130">O **painel Console de** Rede</span><span class="sxs-lookup"><span data-stu-id="48433-130">The **Network Console** panel</span></span>  
:::image-end:::  

> [!TIP]
> <span data-ttu-id="48433-131">Para exibir **o Console de Rede** no painel principal \(top\) em vez da Gaveta de [DevTools,][DevtoolsCustomizeIndexDrawer]navegue até mover ferramentas [entre painéis](#move-tools-between-panels).</span><span class="sxs-lookup"><span data-stu-id="48433-131">To display **Network Console** in the main \(top\) panel instead of the [DevTools Drawer][DevtoolsCustomizeIndexDrawer], navigate to [moving tools between panels](#move-tools-between-panels).</span></span>  

> [!NOTE]
> <span data-ttu-id="48433-132">Para habilitar o experimento, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOn] e escolha a caixa de seleção ao lado de **Habilitar Console de Rede**.</span><span class="sxs-lookup"><span data-stu-id="48433-132">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable Network Console**.</span></span>  
> 
> <span data-ttu-id="48433-133">Abra o [Log de Rede,][DevtoolsNetworkIndexLogActivity]abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Editar e Repetir**.</span><span class="sxs-lookup"><span data-stu-id="48433-133">Open the [Network Log][DevtoolsNetworkIndexLogActivity], open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  

<span data-ttu-id="48433-134">Problema do Chromium [#1093687][CR1093687]</span><span class="sxs-lookup"><span data-stu-id="48433-134">Chromium issue [#1093687][CR1093687]</span></span>  

### <a name="service-worker-respondwith-events-in-the-timing-tab"></a><span data-ttu-id="48433-135">O trabalhador do serviço respondeCom eventos na guia Timing</span><span class="sxs-lookup"><span data-stu-id="48433-135">Service worker respondWith events in the Timing tab</span></span>  

<span data-ttu-id="48433-136">A **guia** Timing da **ferramenta Rede** agora inclui eventos de trabalho de `respondWith` serviço.</span><span class="sxs-lookup"><span data-stu-id="48433-136">The **Timing** tab of the **Network** tool now includes `respondWith` service worker events.</span></span>  <span data-ttu-id="48433-137">O evento do trabalhador do serviço mostra a duração do tempo imediatamente antes do manipulador de eventos do trabalhador do serviço começar a ser executado até o momento em que a promessa do `respondWith` `fetch` manipulador é `respondWith` `fetch` resolvida.</span><span class="sxs-lookup"><span data-stu-id="48433-137">The `respondWith` service worker event shows the duration from the time immediately before the service worker `fetch` event handler starts running to the time when the `respondWith` promise of the `fetch` handler is settled.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="O evento respondWith service worker na guia Timing do painel Rede" lightbox="../../media/2020/06/timing-tab.msft.png":::
   <span data-ttu-id="48433-139">O `respondWith` evento do trabalhador do serviço na guia **Timing** da **ferramenta Rede**</span><span class="sxs-lookup"><span data-stu-id="48433-139">The `respondWith` service worker event in the **Timing** tab of the **Network** tool</span></span>  
:::image-end:::  

<span data-ttu-id="48433-140">Expanda **Resposta recebida** para exibir informações adicionais `fetch` da `CacheStorageCacheName` resposta, como , e `serviceWorkerResponseSource` `ResponseTime` .</span><span class="sxs-lookup"><span data-stu-id="48433-140">Expand **Response received** to display additional information from the `fetch` response like `CacheStorageCacheName`, `serviceWorkerResponseSource`, and `ResponseTime`.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Expanda Resposta recebida para exibir informações adicionais da resposta de busca" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   <span data-ttu-id="48433-142">Expanda **Resposta recebida** para exibir informações adicionais da `fetch` resposta</span><span class="sxs-lookup"><span data-stu-id="48433-142">Expand **Response received** to display additional information from the `fetch` response</span></span>  
:::image-end:::  

<span data-ttu-id="48433-143">Problema do Chromium [#1066579][CR1066579]</span><span class="sxs-lookup"><span data-stu-id="48433-143">Chromium issue [#1066579][CR1066579]</span></span>  

### <a name="webhint-feedback-in-the-issues-panel"></a><span data-ttu-id="48433-144">comentários webhint no painel Problemas</span><span class="sxs-lookup"><span data-stu-id="48433-144">webhint feedback in the Issues panel</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="48433-146">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="48433-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="48433-147">[webhint][WebhintMain] é uma ferramenta de código aberto que fornece comentários em tempo real sobre acessibilidade, compatibilidade entre navegadores, segurança, desempenho, PWAs e outros problemas comuns de desenvolvimento da Web de sites.</span><span class="sxs-lookup"><span data-stu-id="48433-147">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="48433-148">Para revisar os comentários da webhint no painel [Problemas.][DevtoolsIssues]</span><span class="sxs-lookup"><span data-stu-id="48433-148">To review webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="comentários webhint no painel Problemas" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   <span data-ttu-id="48433-150">comentários webhint no painel Problemas</span><span class="sxs-lookup"><span data-stu-id="48433-150">webhint feedback in the Issues panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="48433-151">Para habilitar o experimento, navegue até [Ativar recursos experimentais][DevtoolsExperimentalFeaturesTurnOn] e escolha a caixa de seleção ao lado de **Habilitar webhint**.</span><span class="sxs-lookup"><span data-stu-id="48433-151">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable webhint**.</span></span>  
> 
> <span data-ttu-id="48433-152">Abra o [painel Problemas][DevtoolsIssues] para exibir comentários da webhint.</span><span class="sxs-lookup"><span data-stu-id="48433-152">Open the [Issues][DevtoolsIssues] panel to display feedback from webhint.</span></span>  

<span data-ttu-id="48433-153">Problema do Chromium [#1070378][CR1070378]</span><span class="sxs-lookup"><span data-stu-id="48433-153">Chromium issue [#1070378][CR1070378]</span></span>  

### <a name="move-tools-between-panels"></a><span data-ttu-id="48433-154">Mover ferramentas entre painéis</span><span class="sxs-lookup"><span data-stu-id="48433-154">Move tools between panels</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Recurso experimental":::
   <span data-ttu-id="48433-156">Recurso experimental</span><span class="sxs-lookup"><span data-stu-id="48433-156">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="48433-157">Normalmente, ferramentas como **Elementos** e **Rede** só podem ser abertas no painel principal \(top\) do DevTools.</span><span class="sxs-lookup"><span data-stu-id="48433-157">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="48433-158">Da mesma forma, ferramentas como Exibição **3D** e **Problemas** só podem ser abertas no painel de gaveta \(bottom\) do DevTools.</span><span class="sxs-lookup"><span data-stu-id="48433-158">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="48433-159">Agora você pode personalizar o layout do DevTools movendo ferramentas entre os painéis superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="48433-159">You are now able to customize your DevTools layout by moving tools between the top and bottom panels.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Mover ferramentas entre painéis" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   <span data-ttu-id="48433-161">Mover ferramentas entre painéis</span><span class="sxs-lookup"><span data-stu-id="48433-161">Move tools between panels</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="48433-162">Para habilitar o experimento, navegue até Ativar recursos [experimentais][DevtoolsExperimentalFeaturesTurnOn] e escolha a caixa de seleção ao lado de Habilitar suporte para mover **guias entre painéis**.</span><span class="sxs-lookup"><span data-stu-id="48433-162">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable support to move tabs between panels**.</span></span>  

<span data-ttu-id="48433-163">Problema do Chromium [#897944][CR897944]</span><span class="sxs-lookup"><span data-stu-id="48433-163">Chromium issue [#897944][CR897944]</span></span>  

### <a name="improved-initiator-tooltip-in-the-network-panel"></a><span data-ttu-id="48433-164">Dica de ferramenta iniciador aprimorada no painel Rede</span><span class="sxs-lookup"><span data-stu-id="48433-164">Improved Initiator tooltip in the Network panel</span></span>  

<span data-ttu-id="48433-165">No Microsoft Edge 83 e 84, dicas de ferramenta para a coluna Iniciador, que mostra a causa da solicitação de recurso, no [Log][DevtoolsNetworkIndexLogActivity] de Rede exibido com uma barra de rolagem horizontal.</span><span class="sxs-lookup"><span data-stu-id="48433-165">In Microsoft Edge 83 and 84, tooltips for the Initiator column, which shows the cause of the resource request, in the [Network Log][DevtoolsNetworkIndexLogActivity] displayed with a horizontal scrollbar.</span></span>  <span data-ttu-id="48433-166">Você só foi capaz de exibir a pilha de chamada que iniciou a solicitação rolando horizontalmente na dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="48433-166">You were only able to display the call stack that initiated the request by scrolling horizontally in the tooltip.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="A dica de ferramenta Iniciador no Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   <span data-ttu-id="48433-168">A dica de ferramenta Iniciador no Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="48433-168">The Initiator tooltip in Microsoft Edge 84</span></span>  
:::image-end:::  

<span data-ttu-id="48433-169">A partir do Microsoft Edge 85, agora você pode exibir a pilha de chamada iniciador na dica de ferramenta sem rolar horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="48433-169">Starting with Microsoft Edge 85, you are now able to display the Initiator call stack in the tooltip without scrolling horizontally.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="A dica de ferramenta Iniciador no Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   <span data-ttu-id="48433-171">A dica de ferramenta Iniciador no Microsoft Edge 85</span><span class="sxs-lookup"><span data-stu-id="48433-171">The Initiator tooltip in Microsoft Edge 85</span></span>
:::image-end:::  

<span data-ttu-id="48433-172">Problema do Chromium [#1069404][CR1069404]</span><span class="sxs-lookup"><span data-stu-id="48433-172">Chromium issue [#1069404][CR1069404]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="48433-173">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="48433-173">Announcements from the Chromium project</span></span>  

<span data-ttu-id="48433-174">As seções a seguir anunciam recursos adicionais disponíveis no Microsoft Edge 85 que contribuíram para o projeto Chromium de código aberto.</span><span class="sxs-lookup"><span data-stu-id="48433-174">The following sections announce additional features available in Microsoft Edge 85 that were contributed to the open source Chromium project.</span></span>  

### <a name="style-editing-for-css-in-js-frameworks"></a><span data-ttu-id="48433-175">Edição de estilo para estruturas CSS-in-JS</span><span class="sxs-lookup"><span data-stu-id="48433-175">Style editing for CSS-in-JS frameworks</span></span>  

<span data-ttu-id="48433-176">O **painel Estilos** agora tem melhor suporte para edição de estilos que foram criados com as APIs CSS Object Model [(CSSOM).][CsswgDraftsCssom]</span><span class="sxs-lookup"><span data-stu-id="48433-176">The **Styles** pane now has better support for editing styles that were created with the [CSS Object Model (CSSOM)][CsswgDraftsCssom] APIs.</span></span>  <span data-ttu-id="48433-177">Muitas estruturas e bibliotecas CSS-in-JS usam as APIs CSSOM sob o hood para construir estilos.</span><span class="sxs-lookup"><span data-stu-id="48433-177">Many CSS-in-JS frameworks and libraries use the CSSOM APIs under the hood to construct styles.</span></span>  

<span data-ttu-id="48433-178">Agora você pode editar estilos adicionados em JavaScript usando [Folhas de Estilo Construíveis.][WicgConstructStylesheet]</span><span class="sxs-lookup"><span data-stu-id="48433-178">You are now able to edit styles added in JavaScript using [Constructable Stylesheets][WicgConstructStylesheet].</span></span>  <span data-ttu-id="48433-179">Folhas de estilo construíveis são uma nova maneira de criar e distribuir estilos reutilizáveis ao usar [o Shadow DOM.][MdnShadowDom]</span><span class="sxs-lookup"><span data-stu-id="48433-179">Constructable Stylesheets are a new way to create and distribute reusable styles when using [Shadow DOM][MdnShadowDom].</span></span>  

<span data-ttu-id="48433-180">Por exemplo, os `h1` estilos adicionados `CSSStyleSheet` com \(APIs CSSOM\) não eram editáveis anteriormente.</span><span class="sxs-lookup"><span data-stu-id="48433-180">For example, the `h1` styles added with `CSSStyleSheet` \(CSSOM APIs\) were not editable previously.</span></span>  <span data-ttu-id="48433-181">Os estilos agora podem ser editáveis no **painel Estilos.**</span><span class="sxs-lookup"><span data-stu-id="48433-181">The styles are editable now in the **Styles** panel.</span></span>  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Alterar a propriedade em segundo plano dos estilos h1 adicionados com CSSStyleSheet do rosa para o lightblue" lightbox="../../media/2020/06/css-in-js.msft.png":::
   <span data-ttu-id="48433-183">Alterar a `background` propriedade dos `h1` estilos adicionados de para `CSSStyleSheet` `pink` `lightblue` .</span><span class="sxs-lookup"><span data-stu-id="48433-183">Changing the `background` property of the `h1` styles added with `CSSStyleSheet` from `pink` to `lightblue`.</span></span>
:::image-end:::  

<span data-ttu-id="48433-184">Experimente esse recurso com um [exemplo que usa CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span><span class="sxs-lookup"><span data-stu-id="48433-184">Give this feature a try with a [sample that uses CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span></span>

<span data-ttu-id="48433-185">Problema do Chromium [#946975][CR946975]</span><span class="sxs-lookup"><span data-stu-id="48433-185">Chromium issue [#946975][CR946975]</span></span>  

### <a name="lighthouse-6-in-the-lighthouse-panel"></a><span data-ttu-id="48433-186">Farol 6 no painel do Farol</span><span class="sxs-lookup"><span data-stu-id="48433-186">Lighthouse 6 in the Lighthouse panel</span></span>  

<span data-ttu-id="48433-187">O **painel do Farol** agora está executando o Farol 6.</span><span class="sxs-lookup"><span data-stu-id="48433-187">The **Lighthouse** panel is now running Lighthouse 6.</span></span>  <span data-ttu-id="48433-188">Para uma lista completa de todas as alterações, navegue até [v6.0.0 notas de versão][GithubGoogleChromeLighthouse600].</span><span class="sxs-lookup"><span data-stu-id="48433-188">For a full list of all changes, navigate to [v6.0.0 release notes][GithubGoogleChromeLighthouse600].</span></span>  

<span data-ttu-id="48433-189">O Farol 6.0 apresenta três novas métricas ao relatório: Maior Tinta Contentful \(LCP\), Turno cumulativo de layout \(CLS\) e Tempo total de bloqueio \(TBT\).</span><span class="sxs-lookup"><span data-stu-id="48433-189">Lighthouse 6.0 introduces three new metrics to the report:  Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\), and Total Blocking Time \(TBT\).</span></span>  

<span data-ttu-id="48433-190">A fórmula de pontuação de desempenho também foi repesada para refletir melhor a experiência de carregamento do usuário.</span><span class="sxs-lookup"><span data-stu-id="48433-190">The performance score formula has also been reweighted to better reflect the loading experience of the user.</span></span>  

<span data-ttu-id="48433-191">Problema do Chromium [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="48433-191">Chromium issue [#772558][CR772558]</span></span>  

#### <a name="first-meaningful-paint-deprecation"></a><span data-ttu-id="48433-192">Primeira preteração de Tinta Significativa</span><span class="sxs-lookup"><span data-stu-id="48433-192">First Meaningful Paint deprecation</span></span>  

<span data-ttu-id="48433-193">First Meaningful Paint \(FMP\) é preterido no Lighthouse 6.0.</span><span class="sxs-lookup"><span data-stu-id="48433-193">First Meaningful Paint \(FMP\) is deprecated in Lighthouse 6.0.</span></span>  <span data-ttu-id="48433-194">O FMP também foi removido do painel **Desempenho.**</span><span class="sxs-lookup"><span data-stu-id="48433-194">FMP has also been removed from the **Performance** panel.</span></span>  <span data-ttu-id="48433-195">**Maior Tinta Contentful** é a substituição recomendada para FMP.</span><span class="sxs-lookup"><span data-stu-id="48433-195">**Largest Contentful Paint** is the recommended replacement for FMP.</span></span>  <!--For an explanation of why it was deprecated, navigate to [First Meaningful Paint][WebDevFirstMeaningfulPaint].  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

<span data-ttu-id="48433-196">Problema do Chromium [#1096008][CR1096008]</span><span class="sxs-lookup"><span data-stu-id="48433-196">Chromium issue [#1096008][CR1096008]</span></span>  

### <a name="support-for-new-javascript-features"></a><span data-ttu-id="48433-197">Suporte para novos recursos JavaScript</span><span class="sxs-lookup"><span data-stu-id="48433-197">Support for new JavaScript features</span></span>  

<span data-ttu-id="48433-198">O DevTools agora tem melhor suporte para alguns dos recursos de idioma JavaScript mais recentes.</span><span class="sxs-lookup"><span data-stu-id="48433-198">DevTools now has better support for some of the latest JavaScript language features.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="48433-199">[Autocompleção de][V8DevOptionalChaining] sintaxe de encadeamento opcional</span><span class="sxs-lookup"><span data-stu-id="48433-199">[Optional chaining][V8DevOptionalChaining] syntax autocompletion</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="48433-200">A conclusão automática da propriedade no **Console** agora dá suporte à sintaxe de encadeamento opcional, por exemplo, agora funciona  `name?.` além de e `name.` `name[` .</span><span class="sxs-lookup"><span data-stu-id="48433-200">Property auto-completion in the **Console** now supports optional chaining syntax, for example,  `name?.` now works in addition to `name.` and `name[`.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="48433-201">Realce de sintaxe para [campos privados][V8DevClassFieldsPrivate]</span><span class="sxs-lookup"><span data-stu-id="48433-201">Syntax highlighting for [private fields][V8DevClassFieldsPrivate]</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="48433-202">os campos de classe privada agora estão com realce de sintaxe corretamente e muito impressos no **painel Fontes.**</span><span class="sxs-lookup"><span data-stu-id="48433-202">private class fields are now properly syntax-highlighted and pretty-printed in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="48433-203">Realce de sintaxe para [operador de coalescing nullish][V8DevNullishCoalescing]</span><span class="sxs-lookup"><span data-stu-id="48433-203">Syntax highlighting for [Nullish coalescing operator][V8DevNullishCoalescing]</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="48433-204">O DevTools agora imprime corretamente o operador de coalescing nulo no **painel Fontes.**</span><span class="sxs-lookup"><span data-stu-id="48433-204">DevTools now properly pretty-prints the nullish coalescing operator in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="48433-205">Problemas de cromo [#1073903,][CR1073903] [#1083214,][CR1083214] [#1083797][CR1083797]</span><span class="sxs-lookup"><span data-stu-id="48433-205">Chromium issues [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span></span>  

### <a name="new-app-shortcut-warnings-in-the-manifest-pane"></a><span data-ttu-id="48433-206">Novos avisos de atalho de aplicativo no painel Manifesto</span><span class="sxs-lookup"><span data-stu-id="48433-206">New app shortcut warnings in the Manifest pane</span></span>  

<span data-ttu-id="48433-207">**Atalhos de aplicativo ajudam** os usuários a iniciar rapidamente tarefas comuns ou recomendadas em um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="48433-207">**App shortcuts** help users quickly start common or recommended tasks within a web app.</span></span>  

<!--todo: add App shortcuts when section is live  -->  

<span data-ttu-id="48433-208">O **painel** Manifesto agora mostra avisos para as seguintes condições.</span><span class="sxs-lookup"><span data-stu-id="48433-208">The **Manifest** pane now shows warnings for the following conditions.</span></span>  

* <span data-ttu-id="48433-209">Os ícones de atalho do aplicativo são menores que 96 x 96 pixels</span><span class="sxs-lookup"><span data-stu-id="48433-209">The app shortcut icons are smaller than 96x96 pixels</span></span>  
* <span data-ttu-id="48433-210">Os ícones de atalho do aplicativo e os ícones de manifesto não são quadrados \(já que os ícones são ignorados\)</span><span class="sxs-lookup"><span data-stu-id="48433-210">The app shortcut icons and manifest icons are not square \(since the icons are ignored\)</span></span>  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Avisos de atalho de aplicativo" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   <span data-ttu-id="48433-212">Avisos de atalho de aplicativo</span><span class="sxs-lookup"><span data-stu-id="48433-212">App shortcut warnings</span></span>  
:::image-end:::  

<span data-ttu-id="48433-213">Problema do Chromium [#955497][CR955497]</span><span class="sxs-lookup"><span data-stu-id="48433-213">Chromium issue [#955497][CR955497]</span></span>  

### <a name="consistent-display-of-the-computed-pane"></a><span data-ttu-id="48433-214">Exibição consistente do painel Computed</span><span class="sxs-lookup"><span data-stu-id="48433-214">Consistent display of the Computed pane</span></span>  

<span data-ttu-id="48433-215">O **painel computado** na ferramenta **Elementos** agora é exibido consistentemente como um painel em todos os tamanhos do visor.</span><span class="sxs-lookup"><span data-stu-id="48433-215">The **Computed** pane in the **Elements** tool now displays consistently as a pane across all viewport sizes.</span></span>  <span data-ttu-id="48433-216">**Anteriormente, o** painel computado mesclava dentro do painel **Estilos** quando a largura do viewport DevTools era estreita.</span><span class="sxs-lookup"><span data-stu-id="48433-216">Previously the **Computed** pane merged inside the **Styles** pane when the width of the DevTools viewport was narrow.</span></span>  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="O painel computado é exibido consistentemente como um painel separado, mesmo quando o DevTools é estreito" lightbox="../../media/2020/06/computed-pane.msft.png":::
   <span data-ttu-id="48433-218">O **painel computado** é exibido consistentemente como um painel separado, mesmo quando o DevTools é estreito.</span><span class="sxs-lookup"><span data-stu-id="48433-218">The **Computed** pane consistently displays as a separate pane even when the DevTools are narrow.</span></span>
:::image-end:::  

<span data-ttu-id="48433-219">Problema do Chromium [#1073899][CR1073899]</span><span class="sxs-lookup"><span data-stu-id="48433-219">Chromium issue [#1073899][CR1073899]</span></span>  

### <a name="bytecode-offsets-for-webassembly-files"></a><span data-ttu-id="48433-220">Deslocamentos de bytecode para arquivos WebAssembly</span><span class="sxs-lookup"><span data-stu-id="48433-220">Bytecode offsets for WebAssembly files</span></span>  

<span data-ttu-id="48433-221">O DevTools agora usa deslocamentos de bytecode para exibir números de linha de desmontagem de Wasm.</span><span class="sxs-lookup"><span data-stu-id="48433-221">DevTools now uses bytecode offsets for displaying line numbers of Wasm disassembly.</span></span>  
<span data-ttu-id="48433-222">Os números de linha fazem com que seja mais claro que você está olhando para dados binários e é mais consistente com a forma como os locais de referência do tempo de execução wasm.</span><span class="sxs-lookup"><span data-stu-id="48433-222">The line numbers make it clearer that you are looking at binary data, and is more consistent with how the Wasm runtime references locations.</span></span>  

<span data-ttu-id="48433-223">Problema do Chromium [#1071432][CR1071432]</span><span class="sxs-lookup"><span data-stu-id="48433-223">Chromium issue [#1071432][CR1071432]</span></span>  

### <a name="line-wise-copy-and-cut-in-sources-panel"></a><span data-ttu-id="48433-224">Cópia e corte em linha no Painel de Fontes</span><span class="sxs-lookup"><span data-stu-id="48433-224">Line-wise copy and cut in Sources Panel</span></span>  

<span data-ttu-id="48433-225">Ao executar a cópia ou o corte sem seleção no [editor][DevtoolsSourcesEditCssJavascript]do painel Fontes, o DevTools copia ou corta a linha atual de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="48433-225">When performing copy or cut with no selection in the [Sources panel editor][DevtoolsSourcesEditCssJavascript], DevTools copies or cuts the current line of content.</span></span>  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Com o cursor no final da Linha 5, copiando toda a linha do pen.js no DevTools e colar no Visual Studio Code" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   <span data-ttu-id="48433-227">Com o cursor no final da Linha 5, copiando toda  a  linha dopen.jsno DevTools e colar no [código Visual Studio][VisualStudioCode].</span><span class="sxs-lookup"><span data-stu-id="48433-227">With the cursor at the end of Line 5, copying the whole line from **pen.js** in the DevTools and pasting in [Visual Studio Code][VisualStudioCode].</span></span>
:::image-end:::  

<span data-ttu-id="48433-228">Problema do Chromium [#800028][CR800028]</span><span class="sxs-lookup"><span data-stu-id="48433-228">Chromium issue [#800028][CR800028]</span></span>

### <a name="console-settings-updates"></a><span data-ttu-id="48433-229">Atualizações de Configurações de Console</span><span class="sxs-lookup"><span data-stu-id="48433-229">Console Settings updates</span></span>  

#### <a name="ungroup-same-console-messages"></a><span data-ttu-id="48433-230">Desagrupar as mesmas mensagens de console</span><span class="sxs-lookup"><span data-stu-id="48433-230">Ungroup same console messages</span></span>  

<span data-ttu-id="48433-231">A **alternância de** grupo semelhante em Configurações de Console agora se aplica a mensagens duplicadas.</span><span class="sxs-lookup"><span data-stu-id="48433-231">The **Group similar** toggle in Console Settings now applies to duplicate messages.</span></span>  <span data-ttu-id="48433-232">Anteriormente, ele só se aplicava a mensagens semelhantes.</span><span class="sxs-lookup"><span data-stu-id="48433-232">Previously it just applied to similar messages.</span></span>  

<span data-ttu-id="48433-233">Por exemplo, anteriormente, o DevTools não desagrupou as `hello` mensagens, mesmo que **Group similar** seja desmarcado.</span><span class="sxs-lookup"><span data-stu-id="48433-233">For example, previously, DevTools did not ungroup the `hello` messages even though **Group similar** is unchecked.</span></span>  <span data-ttu-id="48433-234">Agora, as `hello` mensagens estão desagrupadas.</span><span class="sxs-lookup"><span data-stu-id="48433-234">Now, the `hello` messages are ungrouped.</span></span>  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Quando Group similar é desmarcado, as mensagens hello são desagrupadas" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   <span data-ttu-id="48433-236">Quando **Group similar** é desmarcado, as mensagens são `hello` desagrupadas</span><span class="sxs-lookup"><span data-stu-id="48433-236">When **Group similar** is unchecked, the `hello` messages are ungrouped</span></span>
:::image-end:::  

<span data-ttu-id="48433-237">Experimente esse recurso com um exemplo [que envia mensagens duplicadas para o Console][CodepenZoherghadyaliZyrjgdJ].</span><span class="sxs-lookup"><span data-stu-id="48433-237">Give this feature a try with a [sample that sends duplicate messages to the Console][CodepenZoherghadyaliZyrjgdJ].</span></span>  

<span data-ttu-id="48433-238">Problema do Chromium [#1082963][CR1082963]</span><span class="sxs-lookup"><span data-stu-id="48433-238">Chromium issue [#1082963][CR1082963]</span></span>  

### <a name="persisting-selected-context-only-settings"></a><span data-ttu-id="48433-239">Persistindo apenas configurações de contexto selecionado</span><span class="sxs-lookup"><span data-stu-id="48433-239">Persisting Selected context only settings</span></span>  

<span data-ttu-id="48433-240">As **configurações de contexto selecionadas** somente nas Configurações do Console agora são persistentes.</span><span class="sxs-lookup"><span data-stu-id="48433-240">The **Selected context only** settings in Console Settings is now persisted.</span></span>  <span data-ttu-id="48433-241">Anteriormente, as configurações eram redefinidas sempre que você fechava e reabria o DevTools.</span><span class="sxs-lookup"><span data-stu-id="48433-241">Previously the settings were reset every time you closed and reopened DevTools.</span></span>  <span data-ttu-id="48433-242">A alteração torna o comportamento de configuração consistente com outras opções de Configurações do Console.</span><span class="sxs-lookup"><span data-stu-id="48433-242">The change makes the setting behavior consistent with other Console Settings options.</span></span>  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Configuração somente de contexto selecionado" lightbox="../../media/2020/06/selected-context.msft.png":::
   <span data-ttu-id="48433-244">**Configuração somente de contexto** selecionado</span><span class="sxs-lookup"><span data-stu-id="48433-244">**Selected context only** setting</span></span>  
:::image-end:::  

<span data-ttu-id="48433-245">Problema do Chromium [#1055875][CR1055875]</span><span class="sxs-lookup"><span data-stu-id="48433-245">Chromium issue [#1055875][CR1055875]</span></span>  

### <a name="performance-panel-updates"></a><span data-ttu-id="48433-246">Atualizações do painel de desempenho</span><span class="sxs-lookup"><span data-stu-id="48433-246">Performance panel updates</span></span>  

#### <a name="javascript-compilation-cache-information-in-performance-tool"></a><span data-ttu-id="48433-247">Informações de cache de compilação JavaScript na **ferramenta Performance**</span><span class="sxs-lookup"><span data-stu-id="48433-247">JavaScript compilation cache information in **Performance** tool</span></span>  

<span data-ttu-id="48433-248">[As informações de cache de compilação javaScript][V8DevCodeCaching] agora são sempre exibidas no painel **Resumo** da **ferramenta Performance.**</span><span class="sxs-lookup"><span data-stu-id="48433-248">[JavaScript compilation cache information][V8DevCodeCaching] is now always displayed in the **Summary** panel of the **Performance** tool.</span></span>  <span data-ttu-id="48433-249">Anteriormente, o DevTools não mostrava nada relacionado ao cache de código se o cache de código não tivesse acontecido.</span><span class="sxs-lookup"><span data-stu-id="48433-249">Previously, DevTools did not show anything related to code caching if code caching did not happen.</span></span>  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Informações de cache de compilação javaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   <span data-ttu-id="48433-251">Informações de cache de compilação javaScript</span><span class="sxs-lookup"><span data-stu-id="48433-251">JavaScript compilation cache information</span></span>  
:::image-end:::  

<span data-ttu-id="48433-252">Problema do Chromium [#912581][CR912581]</span><span class="sxs-lookup"><span data-stu-id="48433-252">Chromium issue [#912581][CR912581]</span></span>  

#### <a name="navigation-timing-alignment-in-the-performance-panel"></a><span data-ttu-id="48433-253">Alinhamento do tempo de navegação no painel Desempenho</span><span class="sxs-lookup"><span data-stu-id="48433-253">Navigation timing alignment in the Performance panel</span></span>  

<span data-ttu-id="48433-254">O **painel** Desempenho usado para mostrar horários nas réguas com base em quando a gravação foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="48433-254">The **Performance** panel used to show times in the rulers based on when the recording started.</span></span>  <span data-ttu-id="48433-255">O tempo agora foi alterado para gravações em que o usuário navega, onde o DevTools agora mostra tempos de régua em relação à navegação.</span><span class="sxs-lookup"><span data-stu-id="48433-255">The timing has now changed for recordings where the user navigates, where DevTools now shows ruler times relative to the navigation instead.</span></span>  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Alinhar o tempo de navegação na ferramenta Performance" lightbox="../../media/2020/06/nav-timing.msft.png":::
   <span data-ttu-id="48433-257">Alinhar o tempo de navegação na **ferramenta Performance**</span><span class="sxs-lookup"><span data-stu-id="48433-257">Align navigation timing in **Performance** tool</span></span>  
:::image-end:::  

<span data-ttu-id="48433-258">Os tempos `DOMContentLoaded` para , First Paint, First Contentful Paint e Largest Contentful Paint eventos são atualizados para serem relativos ao início da navegação, o que significa que o tempo corresponde aos horários relatados por `PerformanceObserver` .</span><span class="sxs-lookup"><span data-stu-id="48433-258">The times for `DOMContentLoaded`, First Paint, First Contentful Paint, and Largest Contentful Paint events are updated to be relative to the start of the navigation, which means the timing matches the timings reported by `PerformanceObserver`.</span></span>  

<span data-ttu-id="48433-259">Problema do Chromium [#974550][CR974550]</span><span class="sxs-lookup"><span data-stu-id="48433-259">Chromium issue [#974550][CR974550]</span></span>  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a><span data-ttu-id="48433-260">Novos ícones para pontos de interrupção, pontos de interrupção condicional e logpoints</span><span class="sxs-lookup"><span data-stu-id="48433-260">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="48433-261">O **painel Fontes** tem novos designs para pontos de interrupção, pontos de interrupção condicionais e pontos de log.</span><span class="sxs-lookup"><span data-stu-id="48433-261">The **Sources** panel has new designs for breakpoints, conditional breakpoints, and logpoints.</span></span>  <span data-ttu-id="48433-262">Os pontos de interrupção são representados por um círculo vermelho, assim [como Visual Studio Código][VisualStudioCode] e [Visual Studio][VisualStudio].</span><span class="sxs-lookup"><span data-stu-id="48433-262">Breakpoints are represented by a red circle, just like [Visual Studio Code][VisualStudioCode] and [Visual Studio][VisualStudio].</span></span>  <span data-ttu-id="48433-263">Os ícones são adicionados para diferenciar pontos de interrupção condicionais e logpoints.</span><span class="sxs-lookup"><span data-stu-id="48433-263">Icons are added to differentiate conditional breakpoints and logpoints.</span></span>  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Pontos de interrupção" lightbox="../../media/2020/06/breakpoints.msft.png":::
   <span data-ttu-id="48433-265">Pontos de interrupção</span><span class="sxs-lookup"><span data-stu-id="48433-265">Breakpoints</span></span>  
:::image-end:::  

<span data-ttu-id="48433-266">Problema do Chromium [#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="48433-266">Chromium issue [#1041830][CR1041830]</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="48433-267">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="48433-267">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="48433-268">Se você estiver no Windows ou macOS, considere usar os canais de visualização do [Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="48433-268">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="48433-269">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="48433-269">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="48433-270">Como entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="48433-270">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Executar comandos com o menu de comando Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Gaveta - Personalizar o Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Ativar recursos experimentais - Recursos experimentais | Microsoft Docs"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Localizar e corrigir problemas com a ferramenta Issues do DevTools do Microsoft Edge | Microsoft Docs"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Editar CSS e JavaScript - Visão geral do painel de fontes | Microsoft Docs"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Atividade de rede de log - Inspecionar atividade de rede no Microsoft Edge DevTools | Microsoft Docs"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Edição de estilo para estruturas CSS-in-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Enviar mensagens duplicadas para o console | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Exemplo de planejador de grade CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Erros do Chromium"  

[CR772558]: https://crbug.com/772558 "DevTools: atualizar para a versão mais recente do | Bugs do Chromium"  
[CR800028]: https://crbug.com/800028 "Atalho de linha duplicado no editor de Ferramentas de Desenvolvedor não funcionando após a atualização do Chrome | Bugs do Chromium"  
[CR912581]: https://crbug.com/912581 "Expor quais scripts foram armazenados em cache pelo V8 no DevTools/about:tracing | Bugs do Chromium"  
[CR946975]: https://crbug.com/946975 "Barra lateral estilos de DevTools não funciona com folhas de estilo construídas | Bugs do Chromium"  
[CR955497]: https://crbug.com/955497 "Menu Atalho de ícone de aplicativo para PWAs | Bugs do Chromium"  
[CR974550]: https://crbug.com/974550 "Incompatibilidade métrica entre o painel Perf e performanceObserver | Bugs do Chromium"  
[CR1041830]: https://crbug.com/1041830 "Melhorar as cores para pontos de interrupção | Bugs do Chromium"  
[CR1055875]: https://crbug.com/1055875 "O valor da configuração de console somente de contexto selecionado não persiste após o fechamento e a reabertura das Ferramentas de Desenvolvedor | Bugs do Chromium"  
[CR1066579]: https://crbug.com/1066579 "DevTools: Mostrar Linha do Tempo de Busca do ServiceWorkers por solicitação no painel DevTools | Bugs do Chromium"  
[CR1071432]: https://crbug.com/1071432 "Experiência de Desenvolvedor Do Wasm Basic | Bugs do Chromium"  
[CR1073899]: https://crbug.com/1073899 "A guia Estilo Calculado desaparece no modo responsivo | Bugs do Chromium"  
[CR1073903]: https://crbug.com/1073903 "DevTools: Realce de sintaxe não funciona com campos privados | Bugs do Chromium"  
[CR1082963]: https://crbug.com/1082963 "Não é possível desabilitar o comportamento de mensagens semelhantes do grupo do console | Bugs do Chromium"  
[CR1083214]: https://crbug.com/1083214 "Acorn não dá suporte a encadeamento opcional | Bugs do Chromium"  
[CR1083797]: https://crbug.com/1083797 "Impressão bastante interrompida para a | Bugs do Chromium"  
[CR1096008]: https://crbug.com/1096008 "Remover O FMP | Bugs do Chromium"  
[CR1047356]: https://crbug.com/1047356 "Css Grid/Flexbox/Table tooling | Bugs do Chromium"  
[CR1093687]: https://crbug.com/1093687 "Criar ferramenta para criar e repetir solicitações de rede sintéticas | Bugs do Chromium"  
[CR1070378]: https://crbug.com/1070378 "Integrar webhint ao DevTools | Bugs do Chromium"  
[CR1069404]: https://crbug.com/1069404 "Os pop-ups de widget [Ferramentas de Dev] são muito estreitos | Bugs do Chromium"  
[CR897944]: https://crbug.com/897944 "Painéis de devtool arrastáveis | Bugs do Chromium"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v6.0.0 - GoogleChrome/| GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Novo problema - MicrosoftDocs/desenvolvedor de borda"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Usando o DOM de sombra | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Canais de visualização do Microsoft Edge"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"
[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio Code"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Modelo de Objeto CSS (CSSOM) | Rascunhos do Editor do Grupo de Trabalho CSS do W3C"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Postar um Tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools conta do Twitter"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Campos de classe privada - Campos de classe pública e privada | V8. Dev"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Cache de código para desenvolvedores JavaScript | V8. Dev"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Coalescing nullish | V8. Dev"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Encadeamento opcional | V8. Dev"  

[WebhintMain]: https://webhint.io "webhint"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Objetos Stylesheet construíveis | Web Incubator CG"

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
> <span data-ttu-id="48433-319">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="48433-319">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="48433-320">A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/06/devtools/index) e é de autoria de [Jecelyn Yeen][JecelynYeen] \(defensora do desenvolvedor, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="48433-320">The original page is found [here](https://developers.google.com/web/updates/2020/06/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="48433-322">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="48433-322">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
