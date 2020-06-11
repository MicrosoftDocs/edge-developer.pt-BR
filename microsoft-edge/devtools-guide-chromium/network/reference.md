---
title: Referência de análise de rede
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 7e7ac287e116e28773a42456c21ec4ba07647f04
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "10709140"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="0a0ac-103">Referência de análise de rede</span><span class="sxs-lookup"><span data-stu-id="0a0ac-103">Network Analysis Reference</span></span>  

<span data-ttu-id="0a0ac-104">Descubra novas maneiras de analisar como a sua página é carregada nesta referência abrangente dos recursos de análise de rede do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-104">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## <span data-ttu-id="0a0ac-105">Gravar solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="0a0ac-105">Record network requests</span></span>  

<span data-ttu-id="0a0ac-106">Por padrão, o DevTools registra todas as solicitações de rede no painel de rede, desde que DevTools esteja aberto.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-106">By default, DevTools records all network requests in the Network panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="0a0ac-108">Figura 1: painel de **rede**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-108">Figure 1:  The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-109">Parar a gravação de solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="0a0ac-109">Stop recording network requests</span></span>  

<span data-ttu-id="0a0ac-110">Para parar de gravar solicitações, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-110">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="0a0ac-111">Selecione **parar gravação de log de rede** ![ parar de gravar ][ImageRecordOnIcon] o log de rede no painel de **rede** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-111">Select **Stop recording network log** ![Stop recording network log][ImageRecordOnIcon] on the **Network** panel.</span></span>  <span data-ttu-id="0a0ac-112">Ele fica cinza para indicar que o DevTools não está mais gravando solicitações.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-112">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="0a0ac-113">Pressione `Control` + `E` \ (Windows \) ou `Command` + `E` \ (MacOS \) enquanto o painel de **rede** estiver em foco.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-113">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="0a0ac-114">Solicitações de limpeza</span><span class="sxs-lookup"><span data-stu-id="0a0ac-114">Clear requests</span></span>  

<span data-ttu-id="0a0ac-115">Selecione **limpar** ![ limpar ][ImageClearIcon] no painel rede para limpar todas as solicitações da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-115">Select **Clear** ![Clear][ImageClearIcon] on the Network panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="O botão limpar" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="0a0ac-117">Figura 2: o botão **limpar**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-117">Figure 2:  The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-118">Salvar solicitações nas cargas de página</span><span class="sxs-lookup"><span data-stu-id="0a0ac-118">Save requests across page loads</span></span>  

<span data-ttu-id="0a0ac-119">Para salvar as solicitações nas cargas da página, marque a caixa de seleção **preservar registro** no painel rede.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-119">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="0a0ac-120">O DevTools salva todas as solicitações até você desabilitar o **preserve log**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-120">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="A caixa de seleção preservar registro" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="0a0ac-122">Figura 3: caixa de seleção **preservar registro**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-122">Figure 3:  The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-123">Capturar capturas de tela durante o carregamento da página</span><span class="sxs-lookup"><span data-stu-id="0a0ac-123">Capture screenshots during page load</span></span>  

<span data-ttu-id="0a0ac-124">Capture capturas de tela para analisar o que os usuários vêem enquanto esperam pela página para carregar.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-124">Capture screenshots to analyze what users see as they wait for your page to load.</span></span>  

<span data-ttu-id="0a0ac-125">Para habilitar capturas de tela, selecione **configurações de rede** e escolha **capturar capturas de tela** no painel **rede** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-125">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="0a0ac-126">Recarregue a página enquanto o painel de **rede** estiver em foco para capturar capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-126">Reload the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="0a0ac-127">Após a captura de uma captura de tela, você interage com ela das seguintes maneiras.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-127">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="0a0ac-128">Passe o mouse sobre uma captura de tela para ver o ponto em que a captura de tela foi capturada.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-128">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="0a0ac-129">Uma linha amarela é exibida no painel **visão geral** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-129">A yellow line appears on the **Overview** pane.</span></span>  
*   <span data-ttu-id="0a0ac-130">Selecione a miniatura de uma tela para filtrar todas as solicitações ocorridas após a captura da captura de tela.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-130">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="0a0ac-131">Clique duas vezes em uma miniatura para ampliá-la.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-131">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Passar o mouse sobre uma captura de tela" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="0a0ac-133">Figura 4: passando o mouse sobre uma captura de tela</span><span class="sxs-lookup"><span data-stu-id="0a0ac-133">Figure 4:  Hovering over a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and select **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Selecting Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Old Figure 5:  Selecting Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="0a0ac-134">Alterar comportamento de carregamento</span><span class="sxs-lookup"><span data-stu-id="0a0ac-134">Change loading behavior</span></span>  

### <span data-ttu-id="0a0ac-135">Emular um visitante da primeira vez desabilitando o cache do navegador</span><span class="sxs-lookup"><span data-stu-id="0a0ac-135">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="0a0ac-136">Para emular como um usuário da primeira vez experimenta o seu site, marque a caixa de seleção **desabilitar cache** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-136">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="0a0ac-137">DevTools desabilita o cache do navegador.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-137">DevTools disables the browser cache.</span></span>  <span data-ttu-id="0a0ac-138">Isso emula com mais precisão uma experiência do usuário pela primeira vez, pois as solicitações são servidas do cache do navegador em visitas repetidas.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-138">This more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="A caixa de seleção desabilitar cache" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="0a0ac-140">Figura 5: caixa de seleção **desabilitar cache**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-140">Figure 5:  The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="0a0ac-141">Desabilitar o cache do navegador da gaveta de condições da rede</span><span class="sxs-lookup"><span data-stu-id="0a0ac-141">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="0a0ac-142">Se você quiser desabilitar o cache enquanto trabalha em outros painéis do DevTools, use a gaveta de condições de rede.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-142">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="0a0ac-143">Abra a gaveta de **condições de rede** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-143">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="0a0ac-144">Marque ou desmarque a caixa de seleção **desativar cache** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-144">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="0a0ac-145">Limpar manualmente o cache do navegador</span><span class="sxs-lookup"><span data-stu-id="0a0ac-145">Manually clear the browser cache</span></span>  

<span data-ttu-id="0a0ac-146">Para limpar manualmente o cache do navegador a qualquer momento, abra o menu contextual \ (clique com o botão direito do mouse \) em qualquer lugar na tabela solicitações e selecione **Limpar cache do navegador**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-146">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Selecionando limpar cache do navegador" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="0a0ac-148">Figura 6: selecionando **Limpar cache do navegador**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-148">Figure 6:  Selecting **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-149">Emular offline</span><span class="sxs-lookup"><span data-stu-id="0a0ac-149">Emulate offline</span></span>  

<span data-ttu-id="0a0ac-150">Uma nova classe de aplicativos Web, chamada [Web Apps progressivos][DevtoolsProgressiveWebApps], funciona offline com a ajuda do **serviço de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-150">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="0a0ac-151">Pode ser útil simular rapidamente um dispositivo que não tem conexão de dados quando você está criando esse tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-151">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="0a0ac-152">Selecione o menu suspenso **online** , procure em **predefinições**e selecione **offline** para simular uma experiência de rede completamente offline.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-152">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate a completely offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="O menu suspenso offline" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="0a0ac-154">Figura 7: menu suspenso **offline**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-154">Figure 7:  The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-155">Emular conexões de rede lentas</span><span class="sxs-lookup"><span data-stu-id="0a0ac-155">Emulate slow network connections</span></span>  

<span data-ttu-id="0a0ac-156">Emular a conexão 3G, rápida 3G e outras velocidades de conexão a partir do menu suspenso **online** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-156">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="O menu suspenso limitação" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="0a0ac-158">Figura 8: menu suspenso **regulagem**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-158">Figure 8:  The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="0a0ac-159">Você pode escolher entre uma variedade de predefinições, como 3G ou Fast 3G lento.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-159">You may select from a variety of presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="0a0ac-160">Você também pode adicionar suas próprias predefinições personalizadas abrindo o menu de limitação e selecionando **Custom**  >  **Adicionar**personalizado.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-160">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="0a0ac-161">O DevTools exibe um ícone de aviso ao lado da guia **rede** para lembrá-lo de que a limitação está habilitada.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-161">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="0a0ac-162">Emular conexões de rede lentas da gaveta de condições da rede</span><span class="sxs-lookup"><span data-stu-id="0a0ac-162">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="0a0ac-163">Se você quiser controlar a conexão de rede enquanto trabalha em outros painéis do DevTools, use a gaveta de condições de rede.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-163">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="0a0ac-164">Abra a gaveta de **condições de rede** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-164">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="0a0ac-165">Selecione a velocidade de conexão desejada no menu **limitação** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-165">Select your desired connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="0a0ac-166">Limpar manualmente os cookies do navegador</span><span class="sxs-lookup"><span data-stu-id="0a0ac-166">Manually clear browser cookies</span></span>  

<span data-ttu-id="0a0ac-167">Para limpar manualmente os cookies do navegador a qualquer momento, abra o menu contextual \ (clique com o botão direito do mouse \) em qualquer lugar na tabela solicitações e selecione **Limpar cookies do navegador**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-167">To manually clear browser cookies at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Selecionando limpar cookies do navegador" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="0a0ac-169">Figura 9: selecionando **Limpar cookies do navegador**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-169">Figure 9:  Selecting **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-170">Substituir o agente do usuário</span><span class="sxs-lookup"><span data-stu-id="0a0ac-170">Override the user agent</span></span>  

<span data-ttu-id="0a0ac-171">Para substituir manualmente o agente do usuário:</span><span class="sxs-lookup"><span data-stu-id="0a0ac-171">To manually override the user agent:</span></span>  

1.  <span data-ttu-id="0a0ac-172">Abra a gaveta de **condições de rede** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-172">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="0a0ac-173">Desmarque **selecionar automaticamente**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-173">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="0a0ac-174">Escolha uma opção de agente do usuário no menu ou insira uma opção personalizada na caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-174">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="0a0ac-175">Filtrar solicitações</span><span class="sxs-lookup"><span data-stu-id="0a0ac-175">Filter requests</span></span>  

### <span data-ttu-id="0a0ac-176">Filtrar solicitações por propriedades</span><span class="sxs-lookup"><span data-stu-id="0a0ac-176">Filter requests by properties</span></span>  

<span data-ttu-id="0a0ac-177">Use a caixa de texto **Filtrar** para filtrar solicitações por propriedades, como o domínio ou o tamanho da solicitação.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-177">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="0a0ac-178">Se você não vir a caixa de texto, o painel filtros provavelmente está oculto.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-178">If you do not see the text box, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="0a0ac-179">Consulte [ocultar o painel filtros](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="0a0ac-179">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="A caixa de texto filtro" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="0a0ac-181">Figura 10: caixa de texto do **filtro**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-181">Figure 10:  The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="0a0ac-182">Você pode usar várias propriedades simultaneamente, separando cada propriedade com um espaço.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-182">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="0a0ac-183">Por exemplo, `mime-type:image/png larger-than:1K` exibe todas as PNGs maiores do que um kilobyte.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-183">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than one kilobyte.</span></span>  <span data-ttu-id="0a0ac-184">Esses filtros de várias propriedades são equivalentes às `AND` operações.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-184">These multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="0a0ac-185">Não há suporte para operações no momento.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-185">operations are currently not supported.</span></span>  

<span data-ttu-id="0a0ac-186">A lista completa de propriedades com suporte.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-186">The complete list of supported properties.</span></span>  

| <span data-ttu-id="0a0ac-187">Propriedade</span><span class="sxs-lookup"><span data-stu-id="0a0ac-187">Property</span></span> | <span data-ttu-id="0a0ac-188">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0a0ac-188">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="0a0ac-189">Exiba somente os recursos do domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-189">Only display resources from the specified domain.</span></span>  <span data-ttu-id="0a0ac-190">Você pode usar um caractere curinga \ ( `*` \) para incluir vários domínios.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-190">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="0a0ac-191">Por exemplo, `*.com` exibe os recursos de todos os nomes de domínio terminam em `.com` .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-191">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="0a0ac-192">DevTools preenche o menu suspenso de preenchimento automático com todos os domínios encontrados.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-192">DevTools populates the autocomplete dropdown menu with all of the domains it has encountered.</span></span> |  
| `has-response-header` | <span data-ttu-id="0a0ac-193">Mostrar os recursos que contêm o cabeçalho de resposta HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-193">Show the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="0a0ac-194">DevTools preenche a lista suspensa preenchimento automático com todos os cabeçalhos de resposta detectados.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-194">DevTools populates the autocomplete dropdown with all of the response headers that it has encountered.</span></span> |  
| `is` | <span data-ttu-id="0a0ac-195">Use `is:running` para localizar `WebSocket` recursos.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-195">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="0a0ac-196">Mostrar recursos maiores do que o tamanho especificado, em bytes.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-196">Show resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="0a0ac-197">Definir um valor `1000` é equivalente a definir um valor de `1k` .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-197">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="0a0ac-198">Mostrar recursos que foram recuperados em um tipo de método HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-198">Show resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="0a0ac-199">DevTools preenche a lista suspensa com todos os métodos HTTP que ele encontrou.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-199">DevTools populates the dropdown with all of the HTTP methods it has encountered.</span></span> |  
| `mime-type` | <span data-ttu-id="0a0ac-200">Mostrar recursos de um tipo MIME especificado.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-200">Show resources of a specified MIME type.</span></span>  <span data-ttu-id="0a0ac-201">DevTools preenche a lista suspensa com todos os tipos de MIME encontrados.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-201">DevTools populates the dropdown with all MIME types it has encountered.</span></span> |  
| `mixed-content` | <span data-ttu-id="0a0ac-202">Mostrar todos os recursos de conteúdo mistos \ ( `mixed-content:all` \) ou apenas aqueles que são exibidos no momento \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="0a0ac-202">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="0a0ac-203">Mostrar recursos recuperados por HTTP \ ( `scheme:http` \) ou HTTPS protegido \ ( `scheme:https` \) protegido.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-203">Show resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="0a0ac-204">Mostrar os recursos que têm um `Set-Cookie` cabeçalho com um `Domain` atributo que corresponde ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-204">Show the resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="0a0ac-205">DevTools preenche o preenchimento automático com todos os domínios de cookies que ele encontrou.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-205">DevTools populates the autocomplete with all of the cookie domains that it has encountered.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="0a0ac-206">Mostrar os recursos que têm um `Set-Cookie` cabeçalho com um nome que corresponde ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-206">Show the resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="0a0ac-207">DevTools preenche o preenchimento automático com todos os nomes de cookies que ele encontrou.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-207">DevTools populates the autocomplete with all of the cookie names that it has encountered.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="0a0ac-208">Mostrar os recursos que têm um `Set-Cookie` cabeçalho com um valor que corresponde ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-208">Show the resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="0a0ac-209">DevTools preenche o preenchimento automático com todos os valores de cookies que ele encontrou.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-209">DevTools populates the autocomplete with all of the cookie values that it has encountered.</span></span> |  
| `status-code` | <span data-ttu-id="0a0ac-210">Mostre apenas os recursos para os quais o código de status HTTP corresponde ao código especificado.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-210">Show only the resources for which the HTTP status code matches the specified code.</span></span>  <span data-ttu-id="0a0ac-211">DevTools preenche o menu suspenso preenchimento automático com todos os códigos de status encontrados.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-211">DevTools populates the autocomplete dropdown menu with all of the status codes it has encountered.</span></span> |  

### <span data-ttu-id="0a0ac-212">Filtrar solicitações por tipo</span><span class="sxs-lookup"><span data-stu-id="0a0ac-212">Filter requests by type</span></span>  

<span data-ttu-id="0a0ac-213">Para filtrar solicitações por tipo de solicitação, selecione o **XHR**, **js**, **CSS**, **img**, **mídia**, **fonte**, **Doc**, **WS** \ (WebSocket \), **manifesto**ou **outros** \ (qualquer outro tipo não listado aqui \) botões no painel de rede.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-213">To filter requests by request type, select the **XHR**, **JS**, **CSS**, **Img**, **Media**, **Font**, **Doc**, **WS** \(WebSocket\), **Manifest**, or **Other** \(any other type not listed here\) buttons on the Network panel.</span></span>  

<span data-ttu-id="0a0ac-214">Se você não vir esses botões, o painel filtros provavelmente ficará oculto.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-214">If you do not see these buttons, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="0a0ac-215">Consulte [ocultar o painel filtros](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="0a0ac-215">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="0a0ac-216">Para habilitar vários filtros de tipo simultaneamente, segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e, em seguida, selecione.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-216">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Usar os filtros de tipo para exibir os recursos de documento, CSS e JS" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="0a0ac-218">Figura 11: usar os filtros de tipo para exibir os recursos de um JS, CSS e documento</span><span class="sxs-lookup"><span data-stu-id="0a0ac-218">Figure 11:  Using the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-219">Filtrar solicitações por tempo</span><span class="sxs-lookup"><span data-stu-id="0a0ac-219">Filter requests by time</span></span>  

<span data-ttu-id="0a0ac-220">Selecione e arraste para a esquerda ou direita no painel Visão geral para exibir apenas as solicitações que estavam ativas durante esse período de tempo.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-220">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="0a0ac-221">O filtro é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-221">The filter is inclusive.</span></span>  <span data-ttu-id="0a0ac-222">Todas as solicitações ativas durante o tempo realçado são mostradas.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-222">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Filtragem de todas as solicitações que estavam inativas em torno de 300ms" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="0a0ac-224">Figura 12: filtragem de todas as solicitações que estavam inativas em torno de 300ms</span><span class="sxs-lookup"><span data-stu-id="0a0ac-224">Figure 12:  Filtering out any requests that were inactive around 300ms</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-225">Ocultar URLs de dados</span><span class="sxs-lookup"><span data-stu-id="0a0ac-225">Hide data URLs</span></span>  

<span data-ttu-id="0a0ac-226">As [URLs de dados][MDNHTTPDataURIs] são pequenos arquivos incorporados a outros documentos.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-226">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="0a0ac-227">Qualquer solicitação que você vê na tabela solicitações que começa com `data:` é uma URL de dados.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-227">Any request that you see in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="0a0ac-228">Marque a caixa de seleção **ocultar URLs de dados** para ocultar as solicitações.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-228">Check the **Hide data URLs** checkbox to hide the requests.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="A caixa de seleção Ocultar URLs de dados" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="0a0ac-230">Figura 13: caixa de seleção **ocultar URLs de dados**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-230">Figure 13:  The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="0a0ac-231">Solicitações de classificação</span><span class="sxs-lookup"><span data-stu-id="0a0ac-231">Sort requests</span></span>  

<span data-ttu-id="0a0ac-232">Por padrão, as solicitações na tabela solicitações são classificadas por hora de início, mas você pode classificar a tabela usando outros critérios.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-232">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="0a0ac-233">Classificar por coluna</span><span class="sxs-lookup"><span data-stu-id="0a0ac-233">Sort by column</span></span>  

<span data-ttu-id="0a0ac-234">Selecione o cabeçalho de qualquer coluna nas solicitações para classificar solicitações por essa coluna.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-234">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="0a0ac-235">Fase classificar por atividade</span><span class="sxs-lookup"><span data-stu-id="0a0ac-235">Sort by activity phase</span></span>  

<span data-ttu-id="0a0ac-236">Para alterar a forma como a cascata classifica solicitações, passe o cursor do mouse sobre o cabeçalho da tabela solicitações, abra o menu contextual \ (clique com o botão direito do mouse \), passe o mouse sobre a **cascata**e selecione uma das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-236">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover over **Waterfall**, and select one of the following options.</span></span>  

*   <span data-ttu-id="0a0ac-237">**Hora de início**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-237">**Start Time**.</span></span>  <span data-ttu-id="0a0ac-238">A primeira solicitação iniciada está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-238">The first request that was initiated is at the top.</span></span>  
*   <span data-ttu-id="0a0ac-239">**Tempo de resposta**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-239">**Response Time**.</span></span>  <span data-ttu-id="0a0ac-240">A primeira solicitação iniciada para download está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-240">The first request that started downloading is at the top.</span></span>  
*   <span data-ttu-id="0a0ac-241">**Hora de término**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-241">**End Time**.</span></span>  <span data-ttu-id="0a0ac-242">A primeira solicitação que terminou está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-242">The first request that finished is at the top.</span></span>  
*   <span data-ttu-id="0a0ac-243">**Duração total**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-243">**Total Duration**.</span></span>  <span data-ttu-id="0a0ac-244">A solicitação com a configuração de conexão mais curta e solicitação/resposta está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-244">The request with the shortest connection setup and request / response is at the top.</span></span>  
*   <span data-ttu-id="0a0ac-245">**Latência**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-245">**Latency**.</span></span>  <span data-ttu-id="0a0ac-246">A solicitação que aguardou o tempo mais curto para uma resposta está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-246">The request that waited the shortest time for a response is at the top.</span></span>  

<span data-ttu-id="0a0ac-247">Essas descrições pressupõem que cada opção respectiva seja classificada da mais curta para a mais longa.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-247">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="0a0ac-248">A seleção do cabeçalho da coluna em **cascata** inverte a ordem.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-248">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Classificando a cascata com duração total" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="0a0ac-250">Figura 14: classificando a cascata com duração total \ (a parte mais clara de cada barra é o tempo gasto esperando e a parte mais escura é o tempo gasto para baixar bytes \)</span><span class="sxs-lookup"><span data-stu-id="0a0ac-250">Figure 14:  Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="0a0ac-251">Analisar solicitações</span><span class="sxs-lookup"><span data-stu-id="0a0ac-251">Analyze requests</span></span>  

<span data-ttu-id="0a0ac-252">Desde que o DevTools esteja aberto, ele registra todas as solicitações no painel de rede.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-252">So long as DevTools is open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="0a0ac-253">Use o painel rede para analisar solicitações.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-253">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="0a0ac-254">Exibir um log de solicitações</span><span class="sxs-lookup"><span data-stu-id="0a0ac-254">View a log of requests</span></span>  

<span data-ttu-id="0a0ac-255">Use a tabela requests para exibir um log de todas as solicitações feitas enquanto o DevTools está aberto.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-255">Use the Requests table to view a log of all requests made while DevTools has been open.</span></span>  <span data-ttu-id="0a0ac-256">Selecionar ou passar o mouse nas solicitações revela mais informações sobre cada item.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-256">Selecting or hovering over requests reveals more information about each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="A tabela solicitações" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="0a0ac-258">Figura 15: a tabela de solicitações</span><span class="sxs-lookup"><span data-stu-id="0a0ac-258">Figure 15:  The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="0a0ac-259">A tabela solicitações exibe as seguintes colunas por padrão.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-259">The Requests table displays the following columns by default.</span></span>  

*   <span data-ttu-id="0a0ac-260">**Nome**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-260">**Name**.</span></span>  <span data-ttu-id="0a0ac-261">O nome do recurso ou um identificador para o recurso.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-261">The filename of, or an identifier for, the resource.</span></span>  
*   <span data-ttu-id="0a0ac-262">**Status**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-262">**Status**.</span></span>  <span data-ttu-id="0a0ac-263">O código de status HTTP.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-263">The HTTP status code.</span></span>  
*   <span data-ttu-id="0a0ac-264">**Tipo**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-264">**Type**.</span></span>  <span data-ttu-id="0a0ac-265">O tipo MIME do recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-265">The MIME type of the requested resource.</span></span>  
*   <span data-ttu-id="0a0ac-266">**Iniciador**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-266">**Initiator**.</span></span>  <span data-ttu-id="0a0ac-267">Os seguintes objetos ou processos iniciam solicitações:</span><span class="sxs-lookup"><span data-stu-id="0a0ac-267">The following objects or processes initiate requests:</span></span>  
    *   <span data-ttu-id="0a0ac-268">**Analisador**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-268">**Parser**.</span></span>  <span data-ttu-id="0a0ac-269">O analisador HTML para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-269">The HTML parser for Microsoft Edge.</span></span>  
    *   <span data-ttu-id="0a0ac-270">**Redirecionar**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-270">**Redirect**.</span></span>  <span data-ttu-id="0a0ac-271">Um redirecionamento HTTP.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-271">An HTTP redirect.</span></span>  
    *   <span data-ttu-id="0a0ac-272">**Script**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-272">**Script**.</span></span>  <span data-ttu-id="0a0ac-273">Uma função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-273">A JavaScript function.</span></span>  
    *   <span data-ttu-id="0a0ac-274">**Outros**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-274">**Other**.</span></span>  <span data-ttu-id="0a0ac-275">Algum outro processo ou ação, como navegar para uma página por meio de um link ou inserir uma URL na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-275">Some other process or action, such as navigating to a page via a link or entering a URL in the address bar.</span></span>  
*   <span data-ttu-id="0a0ac-276">**Tamanho**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-276">**Size**.</span></span>  <span data-ttu-id="0a0ac-277">O tamanho combinado dos cabeçalhos de resposta mais o corpo da resposta, conforme entregue pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-277">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
*   <span data-ttu-id="0a0ac-278">**Tempo**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-278">**Time**.</span></span>  <span data-ttu-id="0a0ac-279">A duração total, desde o início da solicitação até o recebimento do byte final na resposta.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-279">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
*   <span data-ttu-id="0a0ac-280">[**Cascata**](#view-the-timing-of-requests-in-relation-to-one-another).</span><span class="sxs-lookup"><span data-stu-id="0a0ac-280">[**Waterfall**](#view-the-timing-of-requests-in-relation-to-one-another).</span></span>  <span data-ttu-id="0a0ac-281">Uma divisão Visual da atividade para cada solicitação.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-281">A visual breakdown of the activity for each request.</span></span>  

#### <span data-ttu-id="0a0ac-282">Adicionar ou remover colunas</span><span class="sxs-lookup"><span data-stu-id="0a0ac-282">Add or remove columns</span></span>  

<span data-ttu-id="0a0ac-283">Passe o mouse sobre o cabeçalho da tabela solicitações, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione uma opção para ocultá-la ou mostrá-la.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-283">Hover on the header of the Requests table, open the contextual menu \(right-click\), and select an option to hide or show it.</span></span>  <span data-ttu-id="0a0ac-284">As opções atualmente exibidas têm marcas de opção ao lado de cada item.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-284">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Adicionar uma coluna à tabela solicitações" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="0a0ac-286">Figura 16: adicionando uma coluna à tabela solicitações</span><span class="sxs-lookup"><span data-stu-id="0a0ac-286">Figure 16:  Adding a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="0a0ac-287">Adicionar colunas personalizadas</span><span class="sxs-lookup"><span data-stu-id="0a0ac-287">Add custom columns</span></span>  

<span data-ttu-id="0a0ac-288">Para adicionar uma coluna personalizada à tabela solicitações, passe o mouse sobre o cabeçalho da tabela solicitações, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione **cabeçalhos de resposta**  >  **gerenciar colunas de cabeçalho**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-288">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and select **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Adicionando uma coluna personalizada à tabela solicitações" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="0a0ac-290">Figura 17: adicionando uma coluna personalizada à tabela solicitações</span><span class="sxs-lookup"><span data-stu-id="0a0ac-290">Figure 17:  Adding a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-291">Exibir o intervalo de solicitações em relação umas as outras</span><span class="sxs-lookup"><span data-stu-id="0a0ac-291">View the timing of requests in relation to one another</span></span>  

<span data-ttu-id="0a0ac-292">Use a cascata para ver o intervalo de solicitações em relação umas as outras.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-292">Use the Waterfall to view the timing of requests in relation to one another.</span></span>  
<span data-ttu-id="0a0ac-293">Por padrão, a cascata é organizada pela hora de início das solicitações.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-293">By default, the Waterfall is organized by the start time of the requests.</span></span>  
<span data-ttu-id="0a0ac-294">Portanto, as solicitações mais distantes do lado esquerdo são mais antigas do que aquelas mais distantes do lado direito.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-294">So, requests that are farther to the left started earlier than those that are farther to the right.</span></span>  

<span data-ttu-id="0a0ac-295">Consulte a [fase classificar por atividade](#sort-by-activity-phase) para ver as diferentes maneiras de classificar a cascata.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-295">See [Sort by activity phase](#sort-by-activity-phase) to see the different ways that you may sort the Waterfall.</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="A coluna de cascata do painel solicitações" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="0a0ac-297">Figura 18: a coluna de cascata do painel **solicitações**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-297">Figure 18:  The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To view the frames of a WebSocket connection:  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-select the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames tab" lightbox="../media/network-frames.msft.png":::
   Old Figure 20:  The **Frames** tab  
:::image-end:::  
-->

<!--The table contains three columns:  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to their type:  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <span data-ttu-id="0a0ac-298">Exibir uma visualização de um corpo de resposta</span><span class="sxs-lookup"><span data-stu-id="0a0ac-298">View a preview of a response body</span></span>  

<span data-ttu-id="0a0ac-299">Para exibir uma visualização do corpo de uma resposta:</span><span class="sxs-lookup"><span data-stu-id="0a0ac-299">To view a preview of a response body:</span></span>  

1.  <span data-ttu-id="0a0ac-300">Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-300">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="0a0ac-301">Selecione a guia **Visualizar** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-301">Select the **Preview** tab.</span></span>  

<span data-ttu-id="0a0ac-302">Esta guia é principalmente útil para exibir imagens.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-302">This tab is mostly useful for viewing images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="A guia Visualização" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="0a0ac-304">Figura 19: a guia **Visualizar**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-304">Figure 19:  The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-305">Exibir um corpo de resposta</span><span class="sxs-lookup"><span data-stu-id="0a0ac-305">View a response body</span></span>  

<span data-ttu-id="0a0ac-306">Para exibir o corpo da resposta a uma solicitação:</span><span class="sxs-lookup"><span data-stu-id="0a0ac-306">To view the response body to a request:</span></span>  

1.  <span data-ttu-id="0a0ac-307">Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-307">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="0a0ac-308">Selecione a guia **resposta** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-308">Select the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="A guia resposta" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="0a0ac-310">Figura 20: a guia **resposta**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-310">Figure 20:  The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-311">Exibir cabeçalhos HTTP</span><span class="sxs-lookup"><span data-stu-id="0a0ac-311">View HTTP headers</span></span>  

<span data-ttu-id="0a0ac-312">Para ver os dados do cabeçalho HTTP sobre uma solicitação:</span><span class="sxs-lookup"><span data-stu-id="0a0ac-312">To view HTTP header data about a request:</span></span>  

1.  <span data-ttu-id="0a0ac-313">Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-313">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="0a0ac-314">Selecione a guia **cabeçalhos** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-314">Select the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="A guia cabeçalhos" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="0a0ac-316">Figura 21: a guia **cabeçalhos**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-316">Figure 21:  The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="0a0ac-317">Exibir fonte de cabeçalho HTTP</span><span class="sxs-lookup"><span data-stu-id="0a0ac-317">View HTTP header source</span></span>  

<span data-ttu-id="0a0ac-318">Por padrão, a guia cabeçalhos mostra os nomes dos cabeçalhos em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-318">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="0a0ac-319">Para exibir os nomes dos cabeçalhos HTTP na ordem em que foram recebidos:</span><span class="sxs-lookup"><span data-stu-id="0a0ac-319">To view the HTTP header names in the order they were received:</span></span>  

1.  <span data-ttu-id="0a0ac-320">Abra a guia **cabeçalhos** para a solicitação que lhe interessa.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-320">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="0a0ac-321">Consulte [exibir cabeçalhos HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="0a0ac-321">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="0a0ac-322">Selecione **Exibir fonte**, ao lado da seção cabeçalho da **solicitação** ou **cabeçalho de resposta** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-322">Select **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="0a0ac-323">Exibir parâmetros da cadeia de caracteres de consulta</span><span class="sxs-lookup"><span data-stu-id="0a0ac-323">View query string parameters</span></span>  

<span data-ttu-id="0a0ac-324">Para exibir os parâmetros da cadeia de caracteres de consulta de uma URL em um formato legível por pessoas:</span><span class="sxs-lookup"><span data-stu-id="0a0ac-324">To view the query string parameters of a URL in a human-readable format:</span></span>  

1.  <span data-ttu-id="0a0ac-325">Abra a guia **cabeçalhos** para a solicitação que lhe interessa.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-325">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="0a0ac-326">Consulte [exibir cabeçalhos HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="0a0ac-326">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="0a0ac-327">Vá para a seção **parâmetros da cadeia de caracteres de consulta** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-327">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="A seção parâmetros da cadeia de consulta" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="0a0ac-329">Figura 22: seção **parâmetros da cadeia de consulta**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-329">Figure 22:  The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="0a0ac-330">Exibir origem dos parâmetros da cadeia de consulta</span><span class="sxs-lookup"><span data-stu-id="0a0ac-330">View query string parameters source</span></span>  

<span data-ttu-id="0a0ac-331">Para exibir a origem do parâmetro da cadeia de caracteres de consulta de uma solicitação:</span><span class="sxs-lookup"><span data-stu-id="0a0ac-331">To view the query string parameter source of a request:</span></span>  

1.  <span data-ttu-id="0a0ac-332">Vá para a seção parâmetros da cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-332">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="0a0ac-333">Consulte [Exibir parâmetros da cadeia de consulta](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="0a0ac-333">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="0a0ac-334">Selecione **Exibir código-fonte**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-334">Select **view source**.</span></span>  

#### <span data-ttu-id="0a0ac-335">Exibir parâmetros da cadeia de consulta codificada por URL</span><span class="sxs-lookup"><span data-stu-id="0a0ac-335">View URL-encoded query string parameters</span></span>  

<span data-ttu-id="0a0ac-336">Para exibir os parâmetros da cadeia de caracteres de consulta em um formato legível pelo homem, mas com codificações preservadas:</span><span class="sxs-lookup"><span data-stu-id="0a0ac-336">To view query string parameters in a human-readable format, but with encodings preserved:</span></span>  

1.  <span data-ttu-id="0a0ac-337">Vá para a seção parâmetros da cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-337">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="0a0ac-338">Consulte [Exibir parâmetros da cadeia de consulta](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="0a0ac-338">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="0a0ac-339">Selecione **exibir URL codificada**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-339">Select **view URL encoded**.</span></span>  

### <span data-ttu-id="0a0ac-340">Exibir cookies</span><span class="sxs-lookup"><span data-stu-id="0a0ac-340">View cookies</span></span>  

<span data-ttu-id="0a0ac-341">Para exibir os cookies enviados no cabeçalho HTTP de uma solicitação:</span><span class="sxs-lookup"><span data-stu-id="0a0ac-341">To view the cookies sent in the HTTP header of a request:</span></span>  

1.  <span data-ttu-id="0a0ac-342">Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-342">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="0a0ac-343">Selecione a guia **cookies** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-343">Select the **Cookies** tab.</span></span>  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="A guia cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="0a0ac-345">Figura 23: a guia cookies</span><span class="sxs-lookup"><span data-stu-id="0a0ac-345">Figure 23:  The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-346">Exibir a divisão de tempo de uma solicitação</span><span class="sxs-lookup"><span data-stu-id="0a0ac-346">View the timing breakdown of a request</span></span>  

<span data-ttu-id="0a0ac-347">Para exibir a divisão de tempo de uma solicitação:</span><span class="sxs-lookup"><span data-stu-id="0a0ac-347">To view the timing breakdown of a request:</span></span>  

1.  <span data-ttu-id="0a0ac-348">Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-348">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="0a0ac-349">Selecione a guia **intervalo** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-349">Select the **Timing** tab.</span></span>  

<span data-ttu-id="0a0ac-350">Consulte [Visualizar um detalhamento de intervalos](#preview-a-timing-breakdown) para obter uma maneira mais rápida de acessar esses dados.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-350">See [Preview a timing breakdown](#preview-a-timing-breakdown) for a faster way to access this data.</span></span>  

<span data-ttu-id="0a0ac-351">Veja as [fases da divisão de intervalo explicadas](#timing-breakdown-phases-explained) para obter mais informações sobre cada uma das fases que você pode ver na guia intervalo.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-351">See [Timing breakdown phases explained](#timing-breakdown-phases-explained) for more information about each of the phases that you may see in the Timing tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="A guia intervalo" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="0a0ac-353">Figura 24: a guia **intervalo**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-353">Figure 24:  The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="0a0ac-354">Mais informações sobre cada uma das fases.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-354">More information about each of the phases.</span></span>  

<span data-ttu-id="0a0ac-355">Consulte [Exibir detalhamento de intervalo](#view-the-timing-breakdown-of-a-request) para obter outra maneira de acessar este modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-355">See [View timing breakdown](#view-the-timing-breakdown-of-a-request) for another way to access this view.</span></span>  

#### <span data-ttu-id="0a0ac-356">Visualizar uma divisão de intervalo</span><span class="sxs-lookup"><span data-stu-id="0a0ac-356">Preview a timing breakdown</span></span>  

<span data-ttu-id="0a0ac-357">Para exibir uma visualização da divisão de tempo de uma solicitação, passe o mouse sobre a entrada da solicitação na coluna **cascata** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-357">To view a preview of the timing breakdown of a request, hover over the entry for the request in the **Waterfall** column of the Requests table.</span></span>  

<span data-ttu-id="0a0ac-358">Consulte [Exibir o detalhamento de intervalos de uma solicitação](#view-the-timing-breakdown-of-a-request) para acessar esses dados que não exigem o foco.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-358">See [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request) for a way to access this data that does not require hovering.</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> Visualizar a divisão de tempo de uma solicitação" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="0a0ac-360">Figura 25: visualização da divisão de tempo de uma solicitação</span><span class="sxs-lookup"><span data-stu-id="0a0ac-360">Figure 25:  Previewing the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="0a0ac-361">Fases da divisão de tempo explicadas</span><span class="sxs-lookup"><span data-stu-id="0a0ac-361">Timing breakdown phases explained</span></span>  

<span data-ttu-id="0a0ac-362">Mais informações sobre cada uma das fases que você pode ver na guia **intervalo** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-362">More information about each of the phases you may see in the **Timing** tab.</span></span>  

*   <span data-ttu-id="0a0ac-363">Em **fila**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-363">**Queueing**.</span></span>  <span data-ttu-id="0a0ac-364">O navegador solicita uma fila quando:</span><span class="sxs-lookup"><span data-stu-id="0a0ac-364">The browser queues requests when:</span></span>  
    *   <span data-ttu-id="0a0ac-365">Há solicitações de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-365">There are higher priority requests.</span></span>  
    *   <span data-ttu-id="0a0ac-366">Já existem seis conexões TCP abertas para essa origem, que é o limite.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-366">There are already six TCP connections open for this origin, which is the limit.</span></span>  <span data-ttu-id="0a0ac-367">Aplica-se somente a HTTP/1.0 e HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-367">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
    *   <span data-ttu-id="0a0ac-368">O navegador está alocando um espaço brevemente no cache de disco.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-368">The browser is briefly allocating space in the disk cache.</span></span>  
*   <span data-ttu-id="0a0ac-369">**Parado**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-369">**Stalled**.</span></span>  <span data-ttu-id="0a0ac-370">A solicitação pode estar parada para qualquer um dos motivos descritos no **enfileiramento**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-370">The request could be stalled for any of the reasons described in **Queueing**.</span></span>  
*   <span data-ttu-id="0a0ac-371">**Pesquisa de DNS**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-371">**DNS Lookup**.</span></span>  <span data-ttu-id="0a0ac-372">O navegador está resolvendo o endereço IP da solicitação.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-372">The browser is resolving the IP address for the request.</span></span>  
*   <span data-ttu-id="0a0ac-373">**Conexão inicial**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-373">**Initial connection**.</span></span>  <span data-ttu-id="0a0ac-374">O navegador está estabelecendo uma conexão, incluindo Handshakes TCP, novas tentativas de TCP e negociando um SSL.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-374">The browser is establishing a connection including TCP handshakes, TCP retries, and negotiating an SSL.</span></span>
*   <span data-ttu-id="0a0ac-375">**Negociação de proxy**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-375">**Proxy negotiation**.</span></span>  <span data-ttu-id="0a0ac-376">O navegador está negociando a solicitação com um [servidor proxy][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="0a0ac-376">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
*   <span data-ttu-id="0a0ac-377">**Solicitação enviada**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-377">**Request sent**.</span></span>  <span data-ttu-id="0a0ac-378">A solicitação está sendo enviada.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-378">The request is being sent.</span></span>  
*   <span data-ttu-id="0a0ac-379">**Preparação do serviço**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-379">**ServiceWorker Preparation**.</span></span>  <span data-ttu-id="0a0ac-380">O navegador está iniciando o trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-380">The browser is starting up the service worker.</span></span>  
*   <span data-ttu-id="0a0ac-381">**Solicitação ao serviço de serviço**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-381">**Request to ServiceWorker**.</span></span>  <span data-ttu-id="0a0ac-382">A solicitação está sendo enviada para o trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-382">The request is being sent to the service worker.</span></span>  
*   <span data-ttu-id="0a0ac-383">**Aguardando \ (TTFB \)**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-383">**Waiting \(TTFB\)**.</span></span>  <span data-ttu-id="0a0ac-384">O navegador está aguardando o primeiro byte de uma resposta.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-384">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="0a0ac-385">TTFB significa tempo até o primeiro byte.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-385">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="0a0ac-386">Esse tempo inclui 1 viagem de ida e volta da latência e o tempo que o servidor levou para preparar a resposta.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-386">This timing includes 1 round trip of latency and the time the server took to prepare the response.</span></span>  
*   <span data-ttu-id="0a0ac-387">**Download de conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-387">**Content Download**.</span></span>  <span data-ttu-id="0a0ac-388">O navegador está recebendo a resposta.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-388">The browser is receiving the response.</span></span>  
*   <span data-ttu-id="0a0ac-389">**Recebendo Push**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-389">**Receiving Push**.</span></span>  <span data-ttu-id="0a0ac-390">O navegador está recebendo dados para esta resposta via Push HTTP/2 Server Push.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-390">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
*   <span data-ttu-id="0a0ac-391">**Leitura por push**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-391">**Reading Push**.</span></span>  <span data-ttu-id="0a0ac-392">O navegador está lendo os dados locais anteriormente recebidos.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-392">The browser is reading the local data previously received.</span></span>  

### <span data-ttu-id="0a0ac-393">Exibir iniciadores e dependências</span><span class="sxs-lookup"><span data-stu-id="0a0ac-393">View initiators and dependencies</span></span>  

<span data-ttu-id="0a0ac-394">Para ver os iniciadores e as dependências de uma solicitação, mantenha o `Shift` cursor sobre a solicitação na tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-394">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="0a0ac-395">Cores DevTools: os iniciadores são exibidos em verde e as dependências são mostradas em vermelho.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-395">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Exibindo os iniciadores e as dependências de uma solicitação" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="0a0ac-397">Figura 26: exibindo os iniciadores e as dependências de uma solicitação</span><span class="sxs-lookup"><span data-stu-id="0a0ac-397">Figure 26:  Viewing the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="0a0ac-398">Quando a tabela de solicitações é ordenada cronologicamente, a primeira solicitação verde acima da que você está passando é o iniciador da dependência.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-398">When the Requests table is ordered chronologically, the first green request above the one you are hovering is the initiator of the dependency.</span></span>  <span data-ttu-id="0a0ac-399">Se outra solicitação verde aparecer acima disso, essa solicitação mais alta será o iniciador do iniciador.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-399">If another green request appears above that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="0a0ac-400">E assim em diante.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-400">And so on.</span></span>  

### <span data-ttu-id="0a0ac-401">Exibir eventos de carga</span><span class="sxs-lookup"><span data-stu-id="0a0ac-401">View load events</span></span>  

<span data-ttu-id="0a0ac-402">DevTools exibe a temporização dos `DOMContentLoaded` eventos e de `load` vários locais no painel de rede.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-402">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="0a0ac-403">O `DOMContentLoaded` evento está em azul colorido e o `load` evento está em vermelho.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-403">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Os locais dos eventos DOMContentLoaded e Load no painel de rede" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="0a0ac-405">Figura 27: localizações dos `DOMContentLoaded` eventos e dos `load` eventos no painel de rede</span><span class="sxs-lookup"><span data-stu-id="0a0ac-405">Figure 27:  The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-406">Ver o número total de solicitações</span><span class="sxs-lookup"><span data-stu-id="0a0ac-406">View the total number of requests</span></span>  

<span data-ttu-id="0a0ac-407">O número total de solicitações está listado no painel Resumo, na parte inferior do painel de rede.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-407">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="0a0ac-408">Esse número controla apenas as solicitações que foram registradas desde que o DevTools foi aberto.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-408">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="0a0ac-409">Se ocorrerem outras solicitações antes da abertura do DevTools, essas solicitações não serão contadas.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-409">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="O número total de solicitações desde que o DevTools foi aberto" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="0a0ac-411">Figura 28: o número total de solicitações desde que o DevTools foi aberto</span><span class="sxs-lookup"><span data-stu-id="0a0ac-411">Figure 28:  The total number of requests since DevTools was opened</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-412">Ver o tamanho total do download</span><span class="sxs-lookup"><span data-stu-id="0a0ac-412">View the total download size</span></span>  

<span data-ttu-id="0a0ac-413">O tamanho total do download de solicitações é listado no painel Resumo, na parte inferior do painel de rede.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-413">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="0a0ac-414">Esse número controla apenas as solicitações que foram registradas desde que o DevTools foi aberto.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-414">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="0a0ac-415">Se ocorrerem outras solicitações antes da abertura do DevTools, as solicitações anteriores não serão contadas.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-415">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="O tamanho total do download de solicitações" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="0a0ac-417">Figura 29: o tamanho total do download de solicitações</span><span class="sxs-lookup"><span data-stu-id="0a0ac-417">Figure 29:  The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="0a0ac-418">Consulte [Exibir o tamanho descompactado de um recurso](#view-the-uncompressed-size-of-a-resource) para ver a quantidade de recursos grandes após o navegador descompactar cada item.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-418">See [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource) to see how large resources are after the browser uncompresses each item.</span></span>  

### <span data-ttu-id="0a0ac-419">Exibir o rastreamento de pilha que causou uma solicitação</span><span class="sxs-lookup"><span data-stu-id="0a0ac-419">View the stack trace that caused a request</span></span>  

<span data-ttu-id="0a0ac-420">Depois que uma instrução JavaScript solicita um recurso, passe o mouse sobre a coluna do **iniciador** para exibir o rastreamento de pilha que leva à solicitação.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-420">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

<!-- [codepen.io/contoso/pen/yLBrOWa?editors=0010#0](https://codepen.io/contoso/pen/yLBrOWa?editors=0010#0) -->  

<!--
```javascript
function init() {
  getData();
}

function getData() {
  fetch('https:/httpbin.org/get?message=hi');
}

init();
```  
-->  

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="O rastreamento de pilha que leva a uma solicitação de recurso" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="0a0ac-422">Figura 30: o rastreamento de pilha que leva a uma solicitação de recurso</span><span class="sxs-lookup"><span data-stu-id="0a0ac-422">Figure 30:  The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-423">Exibir o tamanho descompactado de um recurso</span><span class="sxs-lookup"><span data-stu-id="0a0ac-423">View the uncompressed size of a resource</span></span>  

<span data-ttu-id="0a0ac-424">Marque a caixa de seleção **usar linhas de solicitação grandes** e examine o valor inferior da coluna **tamanho** .</span><span class="sxs-lookup"><span data-stu-id="0a0ac-424">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Um exemplo de recursos não compactados" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="0a0ac-426">Figura 31: um exemplo de recursos não compactados \ (o tamanho compactado do `jquery-3.3.1.min.js` arquivo que foi enviado pela rede foi `29.9 KB` , enquanto o tamanho não compactado era `84.9 KB` \)</span><span class="sxs-lookup"><span data-stu-id="0a0ac-426">Figure 31:  An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="0a0ac-427">Exportar dados de solicitações</span><span class="sxs-lookup"><span data-stu-id="0a0ac-427">Export requests data</span></span>  

### <span data-ttu-id="0a0ac-428">Salvar todas as solicitações de rede em um arquivo HAR</span><span class="sxs-lookup"><span data-stu-id="0a0ac-428">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="0a0ac-429">Para salvar todas as solicitações de rede em um arquivo HAR, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-429">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="0a0ac-430">Passe o mouse sobre qualquer solicitação na tabela solicitações e abra o menu contextual \ (clique com o botão direito do mouse \).</span><span class="sxs-lookup"><span data-stu-id="0a0ac-430">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="0a0ac-431">Selecione **salvar como Har com conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-431">Select **Save as HAR with Content**.</span></span>  <span data-ttu-id="0a0ac-432">DevTools salva todas as solicitações ocorridas desde que você abriu o DevTools para o arquivo HAR.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-432">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="0a0ac-433">Não há nenhuma maneira de filtrar solicitações ou salvar uma única solicitação.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-433">There is no way to filter requests, or to save just a single request.</span></span>  

<span data-ttu-id="0a0ac-434">Depois de salvar um arquivo HAR, você poderá importá-lo novamente no DevTools para análise.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-434">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="0a0ac-435">Basta arrastar e soltar o arquivo HAR na tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-435">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Selecionando salvar como HAR com conteúdo" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="0a0ac-437">Figura 32: selecionando **salvar como Har com conteúdo**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-437">Figure 32:  Selecting **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-438">Copiar uma ou mais solicitações para a área de transferência</span><span class="sxs-lookup"><span data-stu-id="0a0ac-438">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="0a0ac-439">Na coluna **nome** da tabela solicitações, passe o mouse sobre uma solicitação, abra o menu contextual \ (clique com o botão direito do mouse \), passe o mouse sobre a **cópia**e selecione uma das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-439">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover over **Copy**, and select one of the following options.</span></span>  

*   <span data-ttu-id="0a0ac-440">**Copie o endereço do link**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-440">**Copy Link Address**.</span></span>  <span data-ttu-id="0a0ac-441">Copie a URL da solicitação para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-441">Copy the URL of the request to the clipboard.</span></span>  
*   <span data-ttu-id="0a0ac-442">**Copiar resposta**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-442">**Copy Response**.</span></span>  <span data-ttu-id="0a0ac-443">Copie o corpo da resposta para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-443">Copy the response body to the clipboard.</span></span>  
*   <span data-ttu-id="0a0ac-444">**Copiar como busca**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-444">**Copy as Fetch**.</span></span>  
*   <span data-ttu-id="0a0ac-445">**Copiar como ondulação**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-445">**Copy as cURL**.</span></span>  <span data-ttu-id="0a0ac-446">Copie a solicitação como um comando de rotação.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-446">Copy the request as a cURL command.</span></span>  
*   <span data-ttu-id="0a0ac-447">**Copiar tudo como busca**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-447">**Copy All as Fetch**.</span></span>  
*   <span data-ttu-id="0a0ac-448">**Copiar tudo como ondulado**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-448">**Copy All as cURL**.</span></span>  <span data-ttu-id="0a0ac-449">Copie todas as solicitações como uma cadeia de comandos de ondulação.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-449">Copy all requests as a chain of cURL commands.</span></span>  
*   <span data-ttu-id="0a0ac-450">**Copiar tudo como Har**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-450">**Copy All as HAR**.</span></span>  <span data-ttu-id="0a0ac-451">Copie todas as solicitações como dados de HAR.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-451">Copy all requests as HAR data.</span></span>  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Selecionando a resposta de cópia" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="0a0ac-453">Figura 33: selecionando a **resposta de cópia**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-453">Figure 33:  Selecting **Copy Response**</span></span>  
:::image-end:::  

## <span data-ttu-id="0a0ac-454">Alterar o layout do painel de rede</span><span class="sxs-lookup"><span data-stu-id="0a0ac-454">Change the layout of the Network panel</span></span>  

<span data-ttu-id="0a0ac-455">Você pode expandir ou recolher seções da interface do usuário do painel de rede para concentrar informações importantes.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-455">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="0a0ac-456">Ocultar o painel filtros</span><span class="sxs-lookup"><span data-stu-id="0a0ac-456">Hide the Filters pane</span></span>  

<span data-ttu-id="0a0ac-457">Por padrão, o DevTools mostra o **painel filtros**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-457">By default, DevTools shows the **Filters pane**.</span></span>  
<span data-ttu-id="0a0ac-458">Selecione **Filter** ![ filtro ][ImageFilterIcon] de filtro para ocultá-lo.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-458">Select **Filter** ![Filter][ImageFilterIcon] to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="O botão Ocultar filtros" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="0a0ac-460">Figura 34: o botão Ocultar filtros</span><span class="sxs-lookup"><span data-stu-id="0a0ac-460">Figure 34:  The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-461">Usar linhas de solicitação grandes</span><span class="sxs-lookup"><span data-stu-id="0a0ac-461">Use large request rows</span></span>  

<span data-ttu-id="0a0ac-462">Use linhas grandes quando quiser mais espaço em branco na tabela solicitações de rede.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-462">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="0a0ac-463">Algumas colunas também fornecem um pouco mais de informações ao usar linhas grandes.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-463">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="0a0ac-464">Por exemplo, o valor inferior da coluna **tamanho** é o tamanho descompactado de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-464">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Um exemplo de linhas de solicitação grandes no painel solicitações" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="0a0ac-466">Figura 35: um exemplo de linhas de solicitação grandes no painel **solicitações**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-466">Figure 35:  An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="0a0ac-467">Marque a caixa de seleção **usar linhas de solicitação grandes** para habilitar linhas grandes.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-467">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="A caixa de seleção usar linhas de solicitação grandes" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="0a0ac-469">Figura 36: caixa de seleção **usar linhas de solicitação grandes**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-469">Figure 36:  The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="0a0ac-470">Ocultar o painel Visão geral</span><span class="sxs-lookup"><span data-stu-id="0a0ac-470">Hide the Overview pane</span></span>  

<span data-ttu-id="0a0ac-471">Por padrão, o DevTools mostra o **painel Visão geral**.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-471">By default, DevTools shows the **Overview pane**.</span></span>  <span data-ttu-id="0a0ac-472">Desmarque a caixa de seleção **Mostrar visão geral** para ocultá-la.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-472">Deselect the **Show Overview** checkbox to hide it.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="A caixa de seleção Mostrar visão geral" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="0a0ac-474">Figura 37: a caixa de seleção **Mostrar visão geral**</span><span class="sxs-lookup"><span data-stu-id="0a0ac-474">Figure 37:  The **Show Overview** checkbox</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: /microsoft-edge/devtools-guide-chromium/network/progressive-web-apps "Depurar aplicativos Web progressivos"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URLs de dados | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Servidor proxy-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="0a0ac-478">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="0a0ac-478">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0a0ac-479">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/network/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="0a0ac-479">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0a0ac-481">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0a0ac-481">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
