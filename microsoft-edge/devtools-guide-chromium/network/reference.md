---
description: Uma referência abrangente dos recursos do painel do Microsoft Edge DevTools Network.
title: Referência de Análise de Rede
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: e8e2259e0f95499519c954e2199e191382998649
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398375"
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

# <a name="network-analysis-reference"></a><span data-ttu-id="2ecaa-104">Referência de Análise de Rede</span><span class="sxs-lookup"><span data-stu-id="2ecaa-104">Network Analysis reference</span></span>  

<span data-ttu-id="2ecaa-105">Descubra novas maneiras de analisar como sua página é carregada nesta referência abrangente dos recursos de análise de rede do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

## <a name="record-network-requests"></a><span data-ttu-id="2ecaa-106">Registrar solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="2ecaa-106">Record network requests</span></span>  

<span data-ttu-id="2ecaa-107">Por padrão, o DevTools registra todas as solicitações de rede na ferramenta **Rede,** desde que o DevTools seja aberto.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-107">By default, DevTools record all network requests in the **Network** tool, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="O painel Rede" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="2ecaa-109">A **ferramenta Rede**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-109">The **Network** tool</span></span>  
:::image-end:::  

### <a name="stop-recording-network-requests"></a><span data-ttu-id="2ecaa-110">Interromper a gravação de solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="2ecaa-110">Stop recording network requests</span></span>  

<span data-ttu-id="2ecaa-111">Para interromper a gravação de solicitações, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="2ecaa-112">Na ferramenta **Rede,** escolha **Parar de gravar log de rede** \( Pare de gravar log de rede ![ ][ImageRecordOnIcon] \).</span><span class="sxs-lookup"><span data-stu-id="2ecaa-112">On the **Network** tool, choose **Stop recording network log** \(![Stop recording network log][ImageRecordOnIcon]\).</span></span>  <span data-ttu-id="2ecaa-113">Fica cinza para indicar que o DevTools não está mais gravando solicitações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="2ecaa-114">Selecione `Control` + `E` \(Windows, Linux\) ou `Command` + `E` \(macOS\) enquanto **a ferramenta Rede** está em foco.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-114">Select `Control`+`E` \(Windows, Linux\) or `Command`+`E` \(macOS\) while the **Network** tool is in focus.</span></span>  

### <a name="clear-requests"></a><span data-ttu-id="2ecaa-115">Limpar solicitações</span><span class="sxs-lookup"><span data-stu-id="2ecaa-115">Clear requests</span></span>  

<span data-ttu-id="2ecaa-116">Escolha **Limpar** \( ![ Limpar ][ImageClearIcon] \) na ferramenta **Rede** para limpar todas as solicitações da tabela Solicitações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-116">Choose **Clear** \(![Clear][ImageClearIcon]\) on the **Network** tool to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="O botão Limpar" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="2ecaa-118">O **botão Limpar**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-118">The **Clear** button</span></span>  
:::image-end:::  

### <a name="save-requests-across-page-loads"></a><span data-ttu-id="2ecaa-119">Salvar solicitações em cargas de página</span><span class="sxs-lookup"><span data-stu-id="2ecaa-119">Save requests across page loads</span></span>  

<span data-ttu-id="2ecaa-120">Para salvar solicitações em cargas de página, na **ferramenta Rede,** a caixa de seleção **Preservar log.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-120">To save requests across page loads, on the **Network** tool, turn on the **Preserve log** checkbox.</span></span>  <span data-ttu-id="2ecaa-121">O DevTools salva todas as solicitações até desabilitar **o log preserve.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="A caixa de seleção Preservar Log" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="2ecaa-123">A **caixa de seleção Preservar Log**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-123">The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <a name="capture-screenshots-during-page-load"></a><span data-ttu-id="2ecaa-124">Capturar capturas de tela durante o carregamento da página</span><span class="sxs-lookup"><span data-stu-id="2ecaa-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="2ecaa-125">Capture capturas de tela para analisar o que é exibido para os usuários enquanto aguarda a sua página ser carregada.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span></span>  

<span data-ttu-id="2ecaa-126">Para habilitar capturas de tela, escolha **Configurações de**rede e, na ferramenta **Rede,** ative a caixa de seleção **Captura capturas de** tela.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-126">To enable screenshots, choose **Network settings**, and on the **Network** tool, turn on the **Capture screenshots** checkbox.</span></span>  

<span data-ttu-id="2ecaa-127">Atualize a página enquanto **a ferramenta Rede** está em foco para capturar capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-127">Refresh the page while the **Network** tool is in focus to capture screenshots.</span></span>  

<span data-ttu-id="2ecaa-128">Depois de capturar uma captura de tela, você interage com ela das seguintes maneiras.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="2ecaa-129">Passe o mouse em uma captura de tela para exibir o ponto no qual essa captura de tela foi capturada.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-129">Hover on a screenshot to display the point at which that screenshot was captured.</span></span>  <span data-ttu-id="2ecaa-130">Uma linha amarela é exibida no painel **Visão** geral.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-130">A yellow line is displayed on the **Overview** pane.</span></span>  
*   <span data-ttu-id="2ecaa-131">Escolha a miniatura de uma tela para filtrar todas as solicitações que ocorreram após a captura de tela ter sido capturada.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-131">Choose the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="2ecaa-132">Clique duas vezes em uma miniatura para ampliá-la.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Passar o mouse em uma captura de tela" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="2ecaa-134">Passar o mouse em uma captura de tela</span><span class="sxs-lookup"><span data-stu-id="2ecaa-134">Hover on a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## <a name="change-loading-behavior"></a><span data-ttu-id="2ecaa-135">Alterar o comportamento de carregamento</span><span class="sxs-lookup"><span data-stu-id="2ecaa-135">Change loading behavior</span></span>  

### <a name="emulate-a-first-time-visitor-by-disabling-the-browser-cache"></a><span data-ttu-id="2ecaa-136">Emular um visitante pela primeira vez desabilitando o cache do navegador</span><span class="sxs-lookup"><span data-stu-id="2ecaa-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="2ecaa-137">Para emular como um usuário de primeira vez experimenta seu site, a caixa de seleção **Desabilitar cache.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-137">To emulate how a first-time user experiences your site, turn on the **Disable cache** checkbox.</span></span>  <span data-ttu-id="2ecaa-138">O DevTools desabilita o cache do navegador.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="2ecaa-139">Esse recurso emula com mais precisão a experiência de um usuário pela primeira vez, pois as solicitações são atendidas do cache do navegador em visitas repetidas.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="A caixa de seleção Desabilitar Cache" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="2ecaa-141">A **caixa de seleção Desabilitar Cache**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-141">The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <a name="disable-the-browser-cache-from-the-network-conditions-drawer"></a><span data-ttu-id="2ecaa-142">Desabilitar o cache do navegador na gaveta Condições de Rede</span><span class="sxs-lookup"><span data-stu-id="2ecaa-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="2ecaa-143">Se você quiser desabilitar o cache enquanto estiver trabalhando em outros painéis do DevTools, use a gaveta Condições de Rede.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="2ecaa-144">Abra a **gaveta Condições de** Rede.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="2ecaa-145">Ativar \(ou desativar\) a caixa **de seleção Desabilitar cache.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-145">Turn on \(or off\) the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-the-browser-cache"></a><span data-ttu-id="2ecaa-146">Limpar manualmente o cache do navegador</span><span class="sxs-lookup"><span data-stu-id="2ecaa-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="2ecaa-147">Para limpar manualmente o cache do navegador a qualquer momento, abra o menu contextual \(clique com o botão direito do mouse\) em qualquer lugar na tabela Solicitações e escolha Limpar Cache **do Navegador**.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and choose **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Escolha Limpar Cache do Navegador" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="2ecaa-149">Escolha **Limpar Cache do Navegador**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-149">Choose **Clear Browser Cache**</span></span>  
:::image-end:::  

### <a name="emulate-offline"></a><span data-ttu-id="2ecaa-150">Emular offline</span><span class="sxs-lookup"><span data-stu-id="2ecaa-150">Emulate offline</span></span>  

<span data-ttu-id="2ecaa-151">Uma nova classe de aplicativos Web, denominada [Progressive Web Apps,][DevtoolsProgressiveWebApps]funciona offline com a ajuda de funcionários **do serviço.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="2ecaa-152">Você pode achar útil simular rapidamente um dispositivo que não tenha conexão de dados ao criar esse tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="2ecaa-153">Escolha o **menu suspenso Online,** pesquise em **Predefinições**e escolha **Offline** para simular uma experiência de rede offline.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-153">Choose the **Online** dropdown menu, search under **Presets**, and choose **Offline** to simulate an offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="O menu suspenso Offline" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="2ecaa-155">O **menu** suspenso Offline</span><span class="sxs-lookup"><span data-stu-id="2ecaa-155">The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <a name="emulate-slow-network-connections"></a><span data-ttu-id="2ecaa-156">Emular conexões de rede lentas</span><span class="sxs-lookup"><span data-stu-id="2ecaa-156">Emulate slow network connections</span></span>  

<span data-ttu-id="2ecaa-157">Emular slow 3G, Fast 3G e outras velocidades de conexão do menu suspenso **Online.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="O menu suspenso Throttling" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="2ecaa-159">O **menu suspenso Throttling**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-159">The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="2ecaa-160">Você pode escolher entre predefinições diferentes, como Slow 3G ou Fast 3G.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-160">You may choose from different presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="2ecaa-161">Para adicionar suas próprias predefinições personalizadas, abra o menu Throttling e escolha **Adicionar**  >  **Personalizado**.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-161">To add your own custom presets, open the Throttling menu, and choose **Custom** > **Add**.</span></span>  

<span data-ttu-id="2ecaa-162">O DevTools exibe um ícone de aviso ao lado da **ferramenta Rede** para lembrá-lo de que a habilitação está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-162">DevTools displays a warning icon next to the **Network** tool to remind you that throttling is enabled.</span></span>  

#### <a name="emulate-slow-network-connections-from-the-network-conditions-drawer"></a><span data-ttu-id="2ecaa-163">Emular conexões de rede lentas da gaveta Condições de Rede</span><span class="sxs-lookup"><span data-stu-id="2ecaa-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="2ecaa-164">Se você quiser acelerar a conexão de rede enquanto estiver trabalhando em outros painéis de DevTools, use a gaveta Condições de Rede.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="2ecaa-165">Abra a **gaveta Condições de** Rede.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="2ecaa-166">Escolha a velocidade da conexão no menu **Throttling.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-166">Choose your connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-browser-cookies"></a><span data-ttu-id="2ecaa-167">Limpar manualmente cookies do navegador</span><span class="sxs-lookup"><span data-stu-id="2ecaa-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="2ecaa-168">Para limpar manualmente cookies do navegador a qualquer momento, passe o mouse em qualquer lugar na tabela Solicitações, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Limpar Cookies do Navegador**.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-168">To manually clear browser cookies at any time, hover anywhere in the Requests table, open the contextual menu \(right-click\), and choose **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Escolha Limpar Cookies do Navegador" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="2ecaa-170">Escolha **Limpar Cookies do Navegador**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-170">Choose **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <a name="override-the-user-agent"></a><span data-ttu-id="2ecaa-171">Substituir o agente do usuário</span><span class="sxs-lookup"><span data-stu-id="2ecaa-171">Override the user agent</span></span>  

<span data-ttu-id="2ecaa-172">Para substituir manualmente o agente do usuário, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-172">To manually override the user agent, use the following steps.</span></span>  

1.  <span data-ttu-id="2ecaa-173">Abra a **gaveta Condições de** Rede.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="2ecaa-174">Desativar a caixa **de seleção Selecionar** automaticamente.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-174">Turn off the **Select automatically** checkbox.</span></span>  
1.  <span data-ttu-id="2ecaa-175">Escolha uma opção de agente de usuário no menu ou insira uma personalizada na caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <a name="filter-requests"></a><span data-ttu-id="2ecaa-176">Solicitações de filtro</span><span class="sxs-lookup"><span data-stu-id="2ecaa-176">Filter requests</span></span>  

### <a name="filter-requests-by-properties"></a><span data-ttu-id="2ecaa-177">Filtrar solicitações por propriedades</span><span class="sxs-lookup"><span data-stu-id="2ecaa-177">Filter requests by properties</span></span>  

<span data-ttu-id="2ecaa-178">Use a **caixa de** texto Filtrar para filtrar solicitações por propriedades, como o domínio ou o tamanho da solicitação.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="2ecaa-179">Se a caixa de texto não for exibida, o painel **Filtros** provavelmente será oculto.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span></span>  
<span data-ttu-id="2ecaa-180">Para obter mais informações, navegue até [Ocultar o painel Filtros.](#hide-the-filters-pane)</span><span class="sxs-lookup"><span data-stu-id="2ecaa-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="A caixa de texto Filtrar" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="2ecaa-182">A **caixa de texto** Filtrar</span><span class="sxs-lookup"><span data-stu-id="2ecaa-182">The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="2ecaa-183">Você pode usar várias propriedades simultaneamente separando cada propriedade com um espaço.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="2ecaa-184">Por exemplo, `mime-type:image/png larger-than:1K` exibe todos os PNGs maiores que 1 quilobyte.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span></span>  <span data-ttu-id="2ecaa-185">Os filtros de várias propriedades são equivalentes às `AND` operações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-185">The multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="2ecaa-186">no momento, não há suporte para operações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-186">operations are currently not supported.</span></span>  

<span data-ttu-id="2ecaa-187">A lista completa de propriedades com suporte.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="2ecaa-188">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2ecaa-188">Property</span></span> | <span data-ttu-id="2ecaa-189">Detalhes</span><span class="sxs-lookup"><span data-stu-id="2ecaa-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="2ecaa-190">Exibe apenas recursos do domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="2ecaa-191">Você pode usar um caractere curinga \( `*` \) para incluir vários domínios.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="2ecaa-192">Por exemplo, `*.com` exibe recursos de todos os nomes de domínio que terminam em `.com` .</span><span class="sxs-lookup"><span data-stu-id="2ecaa-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="2ecaa-193">O DevTools preenche o menu suspenso preenchimento automático com todos os domínios encontrados.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span></span> |  
| `has-response-header` | <span data-ttu-id="2ecaa-194">Exibe os recursos que contêm o cabeçalho de resposta HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-194">Displays the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="2ecaa-195">O DevTools preenche o menu suspenso de preenchimento automático com todos os headers de resposta encontrados.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span></span> |  
| `is` | <span data-ttu-id="2ecaa-196">Use `is:running` para encontrar `WebSocket` recursos.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="2ecaa-197">Exibe recursos maiores do que o tamanho especificado, em bytes.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-197">Displays resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="2ecaa-198">Definir um valor de `1000` é equivalente à definição de um valor de `1k` .</span><span class="sxs-lookup"><span data-stu-id="2ecaa-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="2ecaa-199">Exibe recursos que foram recuperados em um tipo de método HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-199">Displays resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="2ecaa-200">DevTools preenche o menu suspenso com todos os métodos HTTP encontrados.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span></span> |  
| `mime-type` | <span data-ttu-id="2ecaa-201">Exibe recursos de um tipo MIME especificado.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-201">Displays resources of a specified MIME type.</span></span>  <span data-ttu-id="2ecaa-202">DevTools preenche o menu suspenso com todos os tipos MIME encontrados.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-202">DevTools populate the dropdown with all MIME types  that are found.</span></span> |  
| `mixed-content` | <span data-ttu-id="2ecaa-203">Mostrar todos os recursos de conteúdo misto \( \) ou apenas os que estão atualmente `mixed-content:all` exibidos \( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="2ecaa-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="2ecaa-204">Exibe recursos recuperados sobre HTTP \( `scheme:http` \) ou HTTPS protegido \( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="2ecaa-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="2ecaa-205">Exibe recursos que têm `Set-Cookie` um header com um `Domain` atributo que corresponde ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="2ecaa-206">DevTools preenche o preenchimento automático com todos os domínios de cookie encontrados.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="2ecaa-207">Exibe recursos que têm `Set-Cookie` um header com um nome que corresponde ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="2ecaa-208">DevTools preenche o preenchimento automático com todos os nomes de cookie encontrados.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-208">DevTools populate the autocomplete with all of the cookie names that are found.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="2ecaa-209">Exibe recursos que têm `Set-Cookie` um header com um valor que corresponde ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="2ecaa-210">DevTools preenche o preenchimento automático com todos os valores de cookie encontrados.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-210">DevTools populate the autocomplete with all of the cookie values that are found.</span></span> |  
| `status-code` | <span data-ttu-id="2ecaa-211">Exibe recursos que corresponderem ao código de status HTTP específico.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-211">Displays resources that match the specific HTTP status code.</span></span>  <span data-ttu-id="2ecaa-212">O DevTools preenche o menu suspenso preenchimento automático com todos os códigos de status encontrados.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span></span> |  

### <a name="filter-requests-by-type"></a><span data-ttu-id="2ecaa-213">Filtrar solicitações por tipo</span><span class="sxs-lookup"><span data-stu-id="2ecaa-213">Filter requests by type</span></span>  

<span data-ttu-id="2ecaa-214">Para filtrar solicitações por tipo de solicitação, escolha um dos seguintes botões na **ferramenta Rede.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-214">To filter requests by request type, choose the one of the following buttons on the **Network** tool.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-215">XHR</span><span class="sxs-lookup"><span data-stu-id="2ecaa-215">XHR</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-216">JS</span><span class="sxs-lookup"><span data-stu-id="2ecaa-216">JS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-217">CSS</span><span class="sxs-lookup"><span data-stu-id="2ecaa-217">CSS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-218">Img</span><span class="sxs-lookup"><span data-stu-id="2ecaa-218">Img</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-219">Media</span><span class="sxs-lookup"><span data-stu-id="2ecaa-219">Media</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-220">Fonte</span><span class="sxs-lookup"><span data-stu-id="2ecaa-220">Font</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-221">Doc</span><span class="sxs-lookup"><span data-stu-id="2ecaa-221">Doc</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-222">WS</span><span class="sxs-lookup"><span data-stu-id="2ecaa-222">WS</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-223">WebSocket.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-223">WebSocket.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-224">Manifesto</span><span class="sxs-lookup"><span data-stu-id="2ecaa-224">Manifest</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-225">Other</span><span class="sxs-lookup"><span data-stu-id="2ecaa-225">Other</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-226">Qualquer outro tipo não listado.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-226">Any other type not listed.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="2ecaa-227">Se os botões não são exibidos, o painel **Filtros** pode estar oculto.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-227">If the buttons do not display, the **Filters** pane may be hidden.</span></span>  
<span data-ttu-id="2ecaa-228">Para obter mais informações, navegue até [Ocultar o painel Filtros.](#hide-the-filters-pane)</span><span class="sxs-lookup"><span data-stu-id="2ecaa-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="2ecaa-229">Para habilitar vários filtros de tipo simultaneamente, segure `Control` \(Windows, Linux\) `Command` ou \(macOS\) e escolha.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-229">To enable multiple type filters simultaneously, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Use os filtros Type para exibir recursos JS, CSS e Document" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="2ecaa-231">Use os filtros Type para exibir recursos JS, CSS e Document</span><span class="sxs-lookup"><span data-stu-id="2ecaa-231">Use the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <a name="filter-requests-by-time"></a><span data-ttu-id="2ecaa-232">Filtrar solicitações por tempo</span><span class="sxs-lookup"><span data-stu-id="2ecaa-232">Filter requests by time</span></span>  

<span data-ttu-id="2ecaa-233">Escolha e arraste para a esquerda ou para a direita no painel **Visão** geral para exibir somente solicitações que estavam ativas durante esse período.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-233">Choose and drag left or right on the **Overview** pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="2ecaa-234">O filtro é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-234">The filter is inclusive.</span></span>  <span data-ttu-id="2ecaa-235">Qualquer solicitação que estava ativa durante o horário realçado é mostrada.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-235">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Filtrar todas as solicitações inativas em torno de 300 ms" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="2ecaa-237">Filtrar todas as solicitações inativas em torno de 300 ms</span><span class="sxs-lookup"><span data-stu-id="2ecaa-237">Filter out any requests that were inactive around 300 ms</span></span>  
:::image-end:::  

### <a name="hide-data-urls"></a><span data-ttu-id="2ecaa-238">Ocultar URLs de dados</span><span class="sxs-lookup"><span data-stu-id="2ecaa-238">Hide data URLs</span></span>  

<span data-ttu-id="2ecaa-239">[URLs de dados][MDNHTTPDataURIs] são arquivos pequenos incorporados a outros documentos.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="2ecaa-240">Qualquer solicitação exibida na tabela Solicitações que começa com `data:` é uma URL de dados.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="2ecaa-241">Para ocultar as solicitações, desligue a caixa de seleção **Ocultar URLs de** dados.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-241">To hide the requests, turn off the **Hide data URLs** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Caixa de seleção Ocultar URLs de Dados" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="2ecaa-243">Caixa **de seleção Ocultar URLs de** Dados</span><span class="sxs-lookup"><span data-stu-id="2ecaa-243">The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <a name="sort-requests"></a><span data-ttu-id="2ecaa-244">Classificar solicitações</span><span class="sxs-lookup"><span data-stu-id="2ecaa-244">Sort requests</span></span>  

<span data-ttu-id="2ecaa-245">Por padrão, as solicitações na tabela Solicitações são ordenadas por hora de início, mas você pode classificar a tabela usando outros critérios.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <a name="sort-by-column"></a><span data-ttu-id="2ecaa-246">Classificar por coluna</span><span class="sxs-lookup"><span data-stu-id="2ecaa-246">Sort by column</span></span>  

<span data-ttu-id="2ecaa-247">Escolha o header de qualquer coluna na solicitação para classificar solicitações por essa coluna.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-247">Choose the header of any column in the Requests to sort requests by that column.</span></span>  

### <a name="sort-by-activity-phase"></a><span data-ttu-id="2ecaa-248">Classificar por fase de atividade</span><span class="sxs-lookup"><span data-stu-id="2ecaa-248">Sort by activity phase</span></span>  

<span data-ttu-id="2ecaa-249">Para alterar como o Cascata classifica solicitações, passe o mouse no header da tabela Solicitações, abra o menu contextual \(clique com o botão direito do mouse\), passe o mouse em **Cascata**e escolha uma das seguintes opções.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover on **Waterfall**, and choose one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-250">Hora de início</span><span class="sxs-lookup"><span data-stu-id="2ecaa-250">Start Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-251">A primeira solicitação iniciada está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-251">The first request that was initiated is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-252">Tempo de Resposta</span><span class="sxs-lookup"><span data-stu-id="2ecaa-252">Response Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-253">A primeira solicitação que começou a baixar está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-253">The first request that started downloading is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-254">Hora de Término</span><span class="sxs-lookup"><span data-stu-id="2ecaa-254">End Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-255">A primeira solicitação concluída está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-255">The first request that finished is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-256">Duração Total</span><span class="sxs-lookup"><span data-stu-id="2ecaa-256">Total Duration</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-257">A solicitação com as configurações de conexão mais curtas e solicitação ou resposta está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-257">The request with the shortest connection settings and request or response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-258">Latência</span><span class="sxs-lookup"><span data-stu-id="2ecaa-258">Latency</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-259">A solicitação que esperou o menor tempo para uma resposta está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-259">The request that waited the shortest time for a response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="2ecaa-260">Essas descrições pressuem que cada opção respectiva é classificada da menor para a mais longa.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="2ecaa-261">Escolha o header da coluna **Cascata** para reverter a ordem.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-261">Choose the header of the **Waterfall** column to reverse the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Classificar a Cascata por duração total" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="2ecaa-263">Classificar a Cascata por duração total \(A parte mais leve de cada barra é o tempo gasto esperando e a parte mais escura é o tempo gasto baixando bytes\)</span><span class="sxs-lookup"><span data-stu-id="2ecaa-263">Sort the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <a name="analyze-requests"></a><span data-ttu-id="2ecaa-264">Analisar solicitações</span><span class="sxs-lookup"><span data-stu-id="2ecaa-264">Analyze requests</span></span>  

<span data-ttu-id="2ecaa-265">Desde que o DevTools seja aberto, ele registra todas as solicitações na **ferramenta Rede.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-265">So long as DevTools are open, it logs all requests in the **Network** tool.</span></span>  
<span data-ttu-id="2ecaa-266">Use o painel Rede para analisar solicitações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-266">Use the Network panel to analyze requests.</span></span>  

### <a name="display-a-log-of-requests"></a><span data-ttu-id="2ecaa-267">Exibir um log de solicitações</span><span class="sxs-lookup"><span data-stu-id="2ecaa-267">Display a log of requests</span></span>  

<span data-ttu-id="2ecaa-268">Use a tabela Solicitações para exibir um log de todas as solicitações feitas enquanto o DevTools estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-268">Use the Requests table to display a log of all requests made while DevTools have been open.</span></span>  <span data-ttu-id="2ecaa-269">Para revelar mais informações sobre cada item, escolha ou passe o mouse sobre solicitações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-269">To reveals more information about each item, choose or hover on requests.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="A tabela Solicitações" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="2ecaa-271">A tabela Solicitações</span><span class="sxs-lookup"><span data-stu-id="2ecaa-271">The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="2ecaa-272">A tabela Solicitações exibe as seguintes colunas por padrão.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-272">The Requests table displays the following columns by default.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-273">Nome</span><span class="sxs-lookup"><span data-stu-id="2ecaa-273">Name</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-274">O nome do arquivo ou um identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-274">The filename of, or an identifier for, the resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-275">Status</span><span class="sxs-lookup"><span data-stu-id="2ecaa-275">Status</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-276">O código de status HTTP.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-276">The HTTP status code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-277">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ecaa-277">Type</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-278">O tipo MIME do recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-278">The MIME type of the requested resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-279">Iniciador</span><span class="sxs-lookup"><span data-stu-id="2ecaa-279">Initiator</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-280">Os seguintes objetos ou processos iniciam solicitações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-280">The following objects or processes initiate requests.</span></span>  
      
      *   <span data-ttu-id="2ecaa-281">**Analisador**  O analisador HTML do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-281">**Parser**  The HTML parser for Microsoft Edge.</span></span>  
      *   <span data-ttu-id="2ecaa-282">**Redirecionamento**  Um redirecionamento HTTP.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-282">**Redirect**  An HTTP redirect.</span></span>  
      *   <span data-ttu-id="2ecaa-283">**Script**  Uma função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-283">**Script**  A JavaScript function.</span></span>  
      *   <span data-ttu-id="2ecaa-284">**Outros**  Algum outro processo ou ação, como navegar até uma página usando um link ou inserir uma URL na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-285">Size</span><span class="sxs-lookup"><span data-stu-id="2ecaa-285">Size</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-286">O tamanho combinado dos headers de resposta mais o corpo da resposta, conforme fornecido pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-286">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-287">Hora</span><span class="sxs-lookup"><span data-stu-id="2ecaa-287">Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-288">A duração total, desde o início da solicitação até o recebimento do byte final na resposta.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="2ecaa-289">Cascata</span><span class="sxs-lookup"><span data-stu-id="2ecaa-289">Waterfall</span></span>](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-290">Uma divisão visual da atividade para cada solicitação.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-290">A visual breakdown of the activity for each request.</span></span>  
   :::column-end:::
:::row-end:::  

#### <a name="add-or-remove-columns"></a><span data-ttu-id="2ecaa-291">Adicionar ou remover colunas</span><span class="sxs-lookup"><span data-stu-id="2ecaa-291">Add or remove columns</span></span>  

<span data-ttu-id="2ecaa-292">Passe o mouse no header da tabela Solicitações, abra o menu contextual \(clique com o botão direito do mouse\) e escolha uma opção para ocultar ou mostrar.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and choose an option to hide or show it.</span></span>  <span data-ttu-id="2ecaa-293">As opções exibidas no momento têm marcas de seleção ao lado de cada item.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-293">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Adicionar uma coluna à tabela Solicitações" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="2ecaa-295">Adicionar uma coluna à tabela Solicitações</span><span class="sxs-lookup"><span data-stu-id="2ecaa-295">Add a column to the Requests table</span></span>  
:::image-end:::  

#### <a name="add-custom-columns"></a><span data-ttu-id="2ecaa-296">Adicionar colunas personalizadas</span><span class="sxs-lookup"><span data-stu-id="2ecaa-296">Add custom columns</span></span>  

<span data-ttu-id="2ecaa-297">Para adicionar uma coluna personalizada à tabela Solicitações, passe o mouse no header da tabela Solicitações, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Headers**de Resposta Gerenciar Colunas de  >  **Header**.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and choose **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Adicionar uma coluna personalizada à tabela Solicitações" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="2ecaa-299">Adicionar uma coluna personalizada à tabela Solicitações</span><span class="sxs-lookup"><span data-stu-id="2ecaa-299">Add a custom column to the Requests table</span></span>  
:::image-end:::  

### <a name="display-the-timing-relationship-of-requests"></a><span data-ttu-id="2ecaa-300">Exibir a relação de tempo das solicitações</span><span class="sxs-lookup"><span data-stu-id="2ecaa-300">Display the timing relationship of requests</span></span>  

<span data-ttu-id="2ecaa-301">Use o Cascata para exibir as relações de tempo das solicitações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-301">Use the Waterfall to display the timing relationships of requests.</span></span>  
<span data-ttu-id="2ecaa-302">A organização padrão do Waterfall usa a hora de início das solicitações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-302">The default organization of the Waterfall uses the start time of the requests.</span></span>  
<span data-ttu-id="2ecaa-303">Portanto, solicitações mais distantes à esquerda iniciadas anteriormente às solicitações mais distantes à direita.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span></span>  

<span data-ttu-id="2ecaa-304">Para revisar as diferentes maneiras de classificar o Cascata, navegue até [Classificar por fase de atividade.](#sort-by-activity-phase)</span><span class="sxs-lookup"><span data-stu-id="2ecaa-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="A coluna Cascata do painel Solicitações" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="2ecaa-306">A coluna Cascata do painel **Solicitações**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-306">The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To review the frames of a WebSocket connection, use the following steps.  

1.  Choose the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Choose the **Frames** panel.  The table shows the last 100 frames.  

To refresh the table, re-choose the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames panel" lightbox="../media/network-frames.msft.png":::
   The **Frames** panel  
:::image-end:::  
-->

<!--The table contains the following three columns.  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to each type.  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <a name="display-a-preview-of-a-response-body"></a><span data-ttu-id="2ecaa-307">Exibir uma visualização de um corpo de resposta</span><span class="sxs-lookup"><span data-stu-id="2ecaa-307">Display a preview of a response body</span></span>  

<span data-ttu-id="2ecaa-308">Para exibir uma visualização de um corpo de resposta, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-308">To display a preview of a response body, use the following steps.</span></span>  

1.  <span data-ttu-id="2ecaa-309">Escolha a URL da solicitação, na coluna **Nome** da tabela Solicitações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-309">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="2ecaa-310">Escolha o **painel Visualização.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-310">Choose the **Preview** panel.</span></span>  

<span data-ttu-id="2ecaa-311">A guia Visualização é mais útil para exibir imagens.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-311">The Preview tab is mostly useful to display images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="O painel Visualização" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="2ecaa-313">O **painel Visualização**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-313">The **Preview** panel</span></span>  
:::image-end:::  

### <a name="display-a-response-body"></a><span data-ttu-id="2ecaa-314">Exibir um corpo de resposta</span><span class="sxs-lookup"><span data-stu-id="2ecaa-314">Display a response body</span></span>  

<span data-ttu-id="2ecaa-315">Para exibir o corpo da resposta a uma solicitação, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-315">To display the response body to a request, use the following steps.</span></span>  

1.  <span data-ttu-id="2ecaa-316">Escolha a URL da solicitação, na coluna **Nome** da tabela Solicitações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-316">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="2ecaa-317">Escolha o **painel Resposta.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-317">Choose the **Response** panel.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="O painel Resposta" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="2ecaa-319">O **painel Resposta**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-319">The **Response** panel</span></span>  
:::image-end:::  

### <a name="display-http-headers"></a><span data-ttu-id="2ecaa-320">Exibir cabeçalhos HTTP</span><span class="sxs-lookup"><span data-stu-id="2ecaa-320">Display HTTP headers</span></span>  

<span data-ttu-id="2ecaa-321">Para exibir dados de cabeçalho HTTP sobre uma solicitação, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-321">To display HTTP header data about a request, use the following steps.</span></span>  

1.  <span data-ttu-id="2ecaa-322">Escolha a URL da solicitação, na coluna **Nome** da tabela Solicitações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-322">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="2ecaa-323">Escolha **o psanel de headers.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-323">Choose the **Headers** psanel.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="O painel Headers" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="2ecaa-325">O **painel Headers**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-325">The **Headers** panel</span></span>  
:::image-end:::  

#### <a name="display-http-header-source"></a><span data-ttu-id="2ecaa-326">Exibir a origem do cabeçalho HTTP</span><span class="sxs-lookup"><span data-stu-id="2ecaa-326">Display HTTP header source</span></span>  

<span data-ttu-id="2ecaa-327">Por padrão, o **painel Headers** mostra nomes de header em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-327">By default, the **Headers** panel shows header names alphabetically.</span></span>  <span data-ttu-id="2ecaa-328">Para dsiplay os nomes de cabeçalho HTTP na ordem recebida, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-328">To dsiplay the HTTP header names in the order received, use the following steps.</span></span>  

1.  <span data-ttu-id="2ecaa-329">Abra o **painel Headers** para a solicitação que lhe interessa.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-329">Open the **Headers** panel for the request that interests you.</span></span>  <span data-ttu-id="2ecaa-330">Para obter mais informações, navegue até [Exibir cabeçalhos HTTP.](#display-http-headers)</span><span class="sxs-lookup"><span data-stu-id="2ecaa-330">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="2ecaa-331">Escolha **a origem**do exibição , ao lado da seção **Header de Solicitação** **ou Dec. de** Resposta.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-331">Choose **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <a name="display-query-string-parameters"></a><span data-ttu-id="2ecaa-332">Exibir parâmetros de cadeia de caracteres de consulta</span><span class="sxs-lookup"><span data-stu-id="2ecaa-332">Display query string parameters</span></span>  

<span data-ttu-id="2ecaa-333">Para exibir os parâmetros de cadeia de caracteres de consulta de uma URL em um formato acessível por humanos, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-333">To display the query string parameters of a URL in a human-readable format, use the following steps.</span></span>  

1.  <span data-ttu-id="2ecaa-334">Abra o **painel Headers** para a solicitação que lhe interessa.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-334">Open the **Headers** panel for the request that interests you.</span></span>  <span data-ttu-id="2ecaa-335">Para obter mais informações, navegue até [Exibir cabeçalhos HTTP.](#display-http-headers)</span><span class="sxs-lookup"><span data-stu-id="2ecaa-335">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="2ecaa-336">Navegue até **a seção Parâmetros da Cadeia de Caracteres de** Consulta.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-336">Navigate to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="A seção Parâmetros da Cadeia de Caracteres de Consulta" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="2ecaa-338">A **seção Parâmetros da Cadeia de Caracteres de** Consulta</span><span class="sxs-lookup"><span data-stu-id="2ecaa-338">The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <a name="display-query-string-parameters-source"></a><span data-ttu-id="2ecaa-339">Exibir a origem dos parâmetros da cadeia de caracteres de consulta</span><span class="sxs-lookup"><span data-stu-id="2ecaa-339">Display query string parameters source</span></span>  

<span data-ttu-id="2ecaa-340">Para exibir a fonte do parâmetro de cadeia de caracteres de consulta de uma solicitação, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-340">To display the query string parameter source of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="2ecaa-341">Navegue até a seção Parâmetros da Cadeia de Caracteres de Consulta.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-341">Navigate to the Query String Parameters section.</span></span>  <span data-ttu-id="2ecaa-342">Para obter mais informações, navegue até [Exibir parâmetros de cadeia de caracteres de consulta](#display-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="2ecaa-342">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="2ecaa-343">Escolha **a fonte de exibição**.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-343">Choose **view source**.</span></span>  

#### <a name="display-url-encoded-query-string-parameters"></a><span data-ttu-id="2ecaa-344">Exibir parâmetros de cadeia de caracteres de consulta codificada por URL</span><span class="sxs-lookup"><span data-stu-id="2ecaa-344">Display URL-encoded query string parameters</span></span>  

<span data-ttu-id="2ecaa-345">Para exibir parâmetros de cadeia de caracteres de consulta em um formato aceitável para humanos, mas com codificações preservadas, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-345">To display query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span></span>  

1.  <span data-ttu-id="2ecaa-346">Navegue até a seção Parâmetros da Cadeia de Caracteres de Consulta.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-346">Navigate to the Query String Parameters section.</span></span>  <span data-ttu-id="2ecaa-347">Para obter mais informações, navegue até [Exibir parâmetros de cadeia de caracteres de consulta](#display-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="2ecaa-347">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="2ecaa-348">Escolha **exibir URL codificada**.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-348">Choose **view URL encoded**.</span></span>  

### <a name="display-cookies"></a><span data-ttu-id="2ecaa-349">Exibir cookies</span><span class="sxs-lookup"><span data-stu-id="2ecaa-349">Display cookies</span></span>  

<span data-ttu-id="2ecaa-350">Para exibir os cookies enviados no cabeçalho HTTP de uma solicitação, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-350">To display the cookies sent in the HTTP header of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="2ecaa-351">Escolha a URL da solicitação, na coluna **Nome** da tabela Solicitações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-351">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="2ecaa-352">Escolha o **painel Cookies.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-352">Choose the **Cookies** panel.</span></span>  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="O painel Cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="2ecaa-354">O painel Cookies</span><span class="sxs-lookup"><span data-stu-id="2ecaa-354">The Cookies panel</span></span>  
:::image-end:::  

### <a name="display-the-timing-breakdown-of-a-request"></a><span data-ttu-id="2ecaa-355">Exibir a divisão de tempo de uma solicitação</span><span class="sxs-lookup"><span data-stu-id="2ecaa-355">Display the timing breakdown of a request</span></span>  

<span data-ttu-id="2ecaa-356">Para exibir a divisão de tempo de uma solicitação, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-356">To display the timing breakdown of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="2ecaa-357">Escolha a URL da solicitação, na coluna **Nome** da tabela Solicitações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-357">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="2ecaa-358">Escolha o **painel Timing.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-358">Choose the **Timing** panel.</span></span>  

<span data-ttu-id="2ecaa-359">Para uma maneira mais rápida de acessar os dados, navegue até [Visualizar uma divisão de tempo.](#preview-a-timing-breakdown)</span><span class="sxs-lookup"><span data-stu-id="2ecaa-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span></span>  

<span data-ttu-id="2ecaa-360">Para obter mais informações sobre cada uma das \*\*\*\* fases que podem ser exibidas no painel Timing, navegue até Fases de divisão [de tempo explicadas](#timing-breakdown-phases-explained).</span><span class="sxs-lookup"><span data-stu-id="2ecaa-360">For more information about each of the phases that may be displayed in the **Timing** panel, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="O painel Timing" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="2ecaa-362">O **painel Timing**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-362">The **Timing** panel</span></span>  
:::image-end:::  

<span data-ttu-id="2ecaa-363">Mais informações sobre cada uma das fases.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-363">More information about each of the phases.</span></span>  

<span data-ttu-id="2ecaa-364">Para obter mais informações sobre como acessar a exibição, navegue até [Exibir divisão de tempo](#display-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="2ecaa-364">For more information about accessing the display, navigate to [Display timing breakdown](#display-the-timing-breakdown-of-a-request).</span></span>  

#### <a name="preview-a-timing-breakdown"></a><span data-ttu-id="2ecaa-365">Visualizar uma divisão de tempo</span><span class="sxs-lookup"><span data-stu-id="2ecaa-365">Preview a timing breakdown</span></span>  

<span data-ttu-id="2ecaa-366">Para exibir uma visualização da divisão de tempo de uma solicitação, na coluna **Cascata** da tabela Solicitações, passe o mouse na entrada da solicitação.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-366">To display a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span></span>  

<span data-ttu-id="2ecaa-367">Para obter mais informações sobre como acessar os dados sem passar o mouse, navegue até Exibir a [divisão de tempo de uma solicitação](#display-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="2ecaa-367">For more information about how to access the data without hovering, navigate to [Display the timing breakdown of a request](#display-the-timing-breakdown-of-a-request).</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> Visualizar a divisão de tempo de uma solicitação" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="2ecaa-369">Visualizar a divisão de tempo de uma solicitação</span><span class="sxs-lookup"><span data-stu-id="2ecaa-369">Preview the timing breakdown of a request</span></span>  
:::image-end:::  

#### <a name="timing-breakdown-phases-explained"></a><span data-ttu-id="2ecaa-370">Fases de divisão de tempo explicadas</span><span class="sxs-lookup"><span data-stu-id="2ecaa-370">Timing breakdown phases explained</span></span>  

<span data-ttu-id="2ecaa-371">Mais informações sobre cada uma das fases que podem ser exibidas no painel **Timing.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-371">More information about each of the phases that may display in the **Timing** panel.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-372">Filas</span><span class="sxs-lookup"><span data-stu-id="2ecaa-372">Queueing</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-373">O navegador faz filas de solicitações quando qualquer um dos seguintes são verdadeiros.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-373">The browser queues requests when any of the following are true.</span></span>  
      
      *   <span data-ttu-id="2ecaa-374">Solicitações de prioridade mais alta existem.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-374">Higher priority requests exist.</span></span>  
      *   <span data-ttu-id="2ecaa-375">Seis conexões TCP estão abertas para a mesma origem, que é o limite.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-375">Six TCP connections are open for the same origin, which is the limit.</span></span>  <span data-ttu-id="2ecaa-376">Aplica-se somente a HTTP/1.0 e HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
      *   <span data-ttu-id="2ecaa-377">O navegador está alocando espaço brevemente no cache de disco.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-377">The browser is briefly allocating space in the disk cache.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-378">Parado</span><span class="sxs-lookup"><span data-stu-id="2ecaa-378">Stalled</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-379">A solicitação está paralisada por qualquer um dos motivos descritos em **Queueing**.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-379">The request is stalled for any of the reasons described in **Queueing**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-380">DNS Lookup</span><span class="sxs-lookup"><span data-stu-id="2ecaa-380">DNS Lookup</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-381">O navegador está resolvendo o endereço IP da solicitação.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-381">The browser is resolving the IP address for the request.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-382">Conexão inicial</span><span class="sxs-lookup"><span data-stu-id="2ecaa-382">Initial connection</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-383">O navegador estabelece uma conexão, incluindo handshakes TCP, recuperações TCP e negocia uma Camada de Soquete Seguro.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-384">Negociação de proxy</span><span class="sxs-lookup"><span data-stu-id="2ecaa-384">Proxy negotiation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-385">O navegador está negociando a solicitação com um [servidor proxy][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="2ecaa-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-386">Solicitação enviada</span><span class="sxs-lookup"><span data-stu-id="2ecaa-386">Request sent</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-387">A solicitação está sendo enviada.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-387">The request is being sent.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-388">Preparação do ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="2ecaa-388">ServiceWorker Preparation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-389">O navegador está iniciando o trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-389">The browser is starting the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-390">Solicitar ao ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="2ecaa-390">Request to ServiceWorker</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-391">A solicitação está sendo enviada para o trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-391">The request is being sent to the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-392">Aguardando \(TTFB\)</span><span class="sxs-lookup"><span data-stu-id="2ecaa-392">Waiting \(TTFB\)</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-393">O navegador está aguardando o primeiro byte de uma resposta.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-393">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="2ecaa-394">TTFB significa Time To First Byte.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-394">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="2ecaa-395">Esse tempo inclui uma viagem de ida e volta de latência e o tempo que o servidor levou para preparar a resposta.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-396">Download de conteúdo</span><span class="sxs-lookup"><span data-stu-id="2ecaa-396">Content Download</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-397">O navegador está recebendo a resposta.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-397">The browser is receiving the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-398">Receber Push</span><span class="sxs-lookup"><span data-stu-id="2ecaa-398">Receiving Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-399">O navegador está recebendo dados para essa resposta por meio do HTTP/2 Server Push.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-399">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="2ecaa-400">Push de leitura</span><span class="sxs-lookup"><span data-stu-id="2ecaa-400">Reading Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2ecaa-401">O navegador está lendo os dados locais recebidos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-401">The browser is reading the local data previously received.</span></span>  
   :::column-end:::
:::row-end:::  

### <a name="display-initiators-and-dependencies"></a><span data-ttu-id="2ecaa-402">Exibir iniciadores e dependências</span><span class="sxs-lookup"><span data-stu-id="2ecaa-402">Display initiators and dependencies</span></span>  

<span data-ttu-id="2ecaa-403">Para exibir os iniciadores e dependências de uma solicitação, segure e passe o mouse sobre a `Shift` solicitação na tabela Solicitações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-403">To display the initiators and dependencies of a request, hold `Shift`and hover on the request in the Requests table.</span></span>  <span data-ttu-id="2ecaa-404">Cores do DevTools: os iniciadores são mostrados em verde e as dependências são mostradas em vermelho.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Exibir os iniciadores e dependências de uma solicitação" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="2ecaa-406">Exibir os iniciadores e dependências de uma solicitação</span><span class="sxs-lookup"><span data-stu-id="2ecaa-406">Display the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="2ecaa-407">Quando a tabela Solicitações é ordenada cronologicamente, se você passar o mouse em uma linha, a linha anterior a ela exibirá uma solicitação verde.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span></span>  <span data-ttu-id="2ecaa-408">A solicitação verde é o iniciador da dependência.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-408">The green request is the initiator of the dependency.</span></span>  <span data-ttu-id="2ecaa-409">Se outra solicitação verde for exibida na linha antes disso, essa solicitação maior será o iniciador do iniciador.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="2ecaa-410">E assim em diante.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-410">And so on.</span></span>  

### <a name="display-load-events"></a><span data-ttu-id="2ecaa-411">Exibir eventos de carga</span><span class="sxs-lookup"><span data-stu-id="2ecaa-411">Display load events</span></span>  

<span data-ttu-id="2ecaa-412">O DevTools exibe o tempo dos eventos e em `DOMContentLoaded` vários locais na ferramenta `load` **Rede.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the **Network** tool.</span></span>  <span data-ttu-id="2ecaa-413">O `DOMContentLoaded` evento é colorido em azul e o evento é `load` vermelho.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Os locais dos eventos DOMContentLoaded e load no painel Rede" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="2ecaa-415">Os locais dos `DOMContentLoaded` eventos e na ferramenta `load` **Rede**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-415">The locations of the `DOMContentLoaded` and `load` events on the **Network** tool</span></span>  
:::image-end:::  

### <a name="display-the-total-number-of-requests"></a><span data-ttu-id="2ecaa-416">Exibir o número total de solicitações</span><span class="sxs-lookup"><span data-stu-id="2ecaa-416">Display the total number of requests</span></span>  

<span data-ttu-id="2ecaa-417">O número total de solicitações está listado no painel **Resumo,** na parte inferior da **ferramenta Rede.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-417">The total number of requests is listed in the **Summary** pane, at the bottom of the **Network** tool.</span></span>  

> [!CAUTION]
> <span data-ttu-id="2ecaa-418">Esse número só rastreia solicitações registradas desde que o DevTools foi aberto.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-418">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="2ecaa-419">Se outras solicitações ocorreram antes da abertura do DevTools, essas solicitações não são contadas.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-419">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="O número total de solicitações desde que o DevTools foi aberto" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="2ecaa-421">O número total de solicitações desde que o DevTools foi aberto</span><span class="sxs-lookup"><span data-stu-id="2ecaa-421">The total number of requests since DevTools were opened</span></span>  
:::image-end:::  

### <a name="display-the-total-download-size"></a><span data-ttu-id="2ecaa-422">Exibir o tamanho total do download</span><span class="sxs-lookup"><span data-stu-id="2ecaa-422">Display the total download size</span></span>  

<span data-ttu-id="2ecaa-423">O tamanho total de download de solicitações está listado no painel **Resumo,** na parte inferior da **ferramenta Rede.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-423">The total download size of requests is listed in the **Summary** pane, at the bottom of the **Network** tool.</span></span>  

> [!CAUTION]
> <span data-ttu-id="2ecaa-424">Esse número só rastreia solicitações registradas desde que o DevTools foi aberto.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-424">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="2ecaa-425">Se outras solicitações ocorreram antes da abertura do DevTools, as solicitações anteriores não são contadas.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="O tamanho total de download de solicitações" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="2ecaa-427">O tamanho total de download de solicitações</span><span class="sxs-lookup"><span data-stu-id="2ecaa-427">The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="2ecaa-428">Para verificar a dimensão dos recursos após o navegador descompactar cada item, navegue para exibir o tamanho não [compactado de um recurso](#display-the-uncompressed-size-of-a-resource).</span><span class="sxs-lookup"><span data-stu-id="2ecaa-428">To verify how large resources are after the browser uncompresses each item, navigate to [display the uncompressed size of a resource](#display-the-uncompressed-size-of-a-resource).</span></span>  

### <a name="display-the-stack-trace-that-caused-a-request"></a><span data-ttu-id="2ecaa-429">Exibir o rastreamento de pilha que causou uma solicitação</span><span class="sxs-lookup"><span data-stu-id="2ecaa-429">Display the stack trace that caused a request</span></span>  

<span data-ttu-id="2ecaa-430">Depois que uma instrução JavaScript solicitar um recurso, passe o mouse na coluna **Iniciador** para exibir o rastreamento de pilha que antecede a solicitação.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-430">After a JavaScript statement requests a resource, hover on the **Initiator** column to display the stack trace leading up to the request.</span></span>  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="O rastreamento de pilha que antecede uma solicitação de recurso" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="2ecaa-432">O rastreamento de pilha que antecede uma solicitação de recurso</span><span class="sxs-lookup"><span data-stu-id="2ecaa-432">The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <a name="display-the-uncompressed-size-of-a-resource"></a><span data-ttu-id="2ecaa-433">Exibir o tamanho não compactado de um recurso</span><span class="sxs-lookup"><span data-stu-id="2ecaa-433">Display the uncompressed size of a resource</span></span>  

<span data-ttu-id="2ecaa-434">A tela de seleção **Usar linhas de solicitação grandes** e, em seguida, revise o valor inferior da coluna **Tamanho.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-434">Turn on the **Use large request rows** checkbox and then review the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Um exemplo de recursos não compactados" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="2ecaa-436">Um exemplo de recursos não compactados \(O tamanho compactado do arquivo enviado pela rede foi , enquanto o tamanho não `jquery-3.3.1.min.js` `29.9 KB` compactado foi `84.9 KB` \)</span><span class="sxs-lookup"><span data-stu-id="2ecaa-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <a name="export-requests-data"></a><span data-ttu-id="2ecaa-437">Exportar dados de solicitações</span><span class="sxs-lookup"><span data-stu-id="2ecaa-437">Export requests data</span></span>  

### <a name="save-all-network-requests-to-a-har-file"></a><span data-ttu-id="2ecaa-438">Salvar todas as solicitações de rede em um arquivo HAR</span><span class="sxs-lookup"><span data-stu-id="2ecaa-438">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="2ecaa-439">Para salvar todas as solicitações de rede em um arquivo HAR, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-439">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="2ecaa-440">Passe o mouse em qualquer solicitação na tabela Solicitações e abra o menu contextual \(clique com o botão direito do mouse\).</span><span class="sxs-lookup"><span data-stu-id="2ecaa-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="2ecaa-441">Escolha **Salvar como HAR com Conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-441">Choose **Save as HAR with Content**.</span></span>  <span data-ttu-id="2ecaa-442">O DevTools salva todas as solicitações que ocorreram desde que você abriu o DevTools para o arquivo HAR.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="2ecaa-443">Não é possível filtrar solicitações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-443">You are not able to filter requests.</span></span>  <span data-ttu-id="2ecaa-444">Você também não é capaz de salvar uma única solicitação.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-444">You are also not able to save a single request.</span></span>  

<span data-ttu-id="2ecaa-445">Depois de salvar um arquivo HAR, você pode importá-lo de volta para o DevTools para análise.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="2ecaa-446">Basta arrastar e soltar o arquivo HAR na tabela Solicitações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-446">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Escolha Salvar como HAR com conteúdo" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="2ecaa-448">Escolha **Salvar como HAR com conteúdo**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-448">Choose **Save as HAR with Content**</span></span>  
:::image-end:::  

### <a name="copy-one-or-more-requests-to-the-clipboard"></a><span data-ttu-id="2ecaa-449">Copiar uma ou mais solicitações para a área de transferência</span><span class="sxs-lookup"><span data-stu-id="2ecaa-449">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="2ecaa-450">Na coluna **Nome** da tabela Solicitações, passe o mouse em uma solicitação, abra o menu contextual \(clique com o botão direito do mouse\), passe o mouse em **Copiar**e escolha uma das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover on **Copy**, and choose one of the following options.</span></span>  

| <span data-ttu-id="2ecaa-451">Nome</span><span class="sxs-lookup"><span data-stu-id="2ecaa-451">Name</span></span> | <span data-ttu-id="2ecaa-452">Detalhes</span><span class="sxs-lookup"><span data-stu-id="2ecaa-452">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="2ecaa-453">Copiar Endereço de Link</span><span class="sxs-lookup"><span data-stu-id="2ecaa-453">Copy Link Address</span></span>** | <span data-ttu-id="2ecaa-454">Copie a URL da solicitação para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-454">Copy the URL of the request to the clipboard.</span></span> |  
| **<span data-ttu-id="2ecaa-455">Copiar Resposta</span><span class="sxs-lookup"><span data-stu-id="2ecaa-455">Copy Response</span></span>** | <span data-ttu-id="2ecaa-456">Copie o corpo da resposta para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-456">Copy the response body to the clipboard.</span></span> |  
| **<span data-ttu-id="2ecaa-457">Copiar como Buscar</span><span class="sxs-lookup"><span data-stu-id="2ecaa-457">Copy as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="2ecaa-458">Copiar como cURL</span><span class="sxs-lookup"><span data-stu-id="2ecaa-458">Copy as cURL</span></span>** | <span data-ttu-id="2ecaa-459">Copie a solicitação como um comando cURL.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-459">Copy the request as a cURL command.</span></span> |  
| **<span data-ttu-id="2ecaa-460">Copiar Tudo como Busca</span><span class="sxs-lookup"><span data-stu-id="2ecaa-460">Copy All as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="2ecaa-461">Copiar Tudo como cURL</span><span class="sxs-lookup"><span data-stu-id="2ecaa-461">Copy All as cURL</span></span>** | <span data-ttu-id="2ecaa-462">Copie todas as solicitações como uma cadeia de comandos cURL.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-462">Copy all requests as a chain of cURL commands.</span></span> |  
| **<span data-ttu-id="2ecaa-463">Copiar Tudo como HAR</span><span class="sxs-lookup"><span data-stu-id="2ecaa-463">Copy All as HAR</span></span>** | <span data-ttu-id="2ecaa-464">Copie todas as solicitações como dados HAR.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-464">Copy all requests as HAR data.</span></span> |  

<!--
:::row:::
   :::column span="1":::
      **Copy Link Address**  
   :::column-end:::
   :::column span="2":::
      Copy the URL of the request to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy Response**  
   :::column-end:::
   :::column span="2":::
      Copy the response body to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy the request as a cURL command.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as a chain of cURL commands.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as HAR**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as HAR data.  
   :::column-end:::
:::row-end:::  
-->  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Escolha Copiar Resposta" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="2ecaa-466">Escolha **Copiar Resposta**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-466">Choose **Copy Response**</span></span>  
:::image-end:::  

### <a name="copy-formatted-response-json-to-the-clipboard"></a><span data-ttu-id="2ecaa-467">Copiar json de resposta formatada para a área de transferência</span><span class="sxs-lookup"><span data-stu-id="2ecaa-467">Copy formatted response JSON to the clipboard</span></span>  

<span data-ttu-id="2ecaa-468">Escolha uma solicitação de rede e navegue até o painel **Headers.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-468">Choose a network request and navigate to the **Headers** pane.</span></span>  <span data-ttu-id="2ecaa-469">Para copiar o valor JSON de uma resposta, navegue até **Solicitar**carga , passe o mouse no conteúdo de resposta JSON, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Copiar Valor**.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-469">To copy the JSON value of a response, navigate to **Request payload**, hover on the JSON response content, open the contextual menu \(right-click\), and choose **Copy Value**.</span></span>  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Copiar Valor no menu contextual" lightbox="../media/network-header-copy-property-value.msft.png":::
          <span data-ttu-id="2ecaa-471">**Copiar Valor** no menu contextual</span><span class="sxs-lookup"><span data-stu-id="2ecaa-471">**Copy Value** in contextual menu</span></span>  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Microsoft Visual Studio Código com resposta formatada JSON" lightbox="../media/network-header-paste-property-value.msft.png":::
          <span data-ttu-id="2ecaa-473">Colar json de resposta formatada no Microsoft Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="2ecaa-473">Pasting formatted response JSON in Microsoft Visual Studio Code</span></span>  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="copy-property-values-from-network-requests-to-your-clipboard"></a><span data-ttu-id="2ecaa-474">Copiar valores de propriedade de solicitações de rede para sua área de transferência</span><span class="sxs-lookup"><span data-stu-id="2ecaa-474">Copy property values from network requests to your clipboard</span></span>  

<span data-ttu-id="2ecaa-475">Para copiar valores de propriedade de solicitações de rede para sua área de transferência, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-475">To copy property values from network requests to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="2ecaa-476">Abra o **painel Headers.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-476">Open the **Headers** pane.</span></span>  
1.  <span data-ttu-id="2ecaa-477">Abra uma das seções de header a seguir.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-477">Open one of the following header sections.</span></span>  
    *   <span data-ttu-id="2ecaa-478">Solicitar carga \(JSON\)</span><span class="sxs-lookup"><span data-stu-id="2ecaa-478">Request payload \(JSON\)</span></span>  
    *   <span data-ttu-id="2ecaa-479">Dados do formulário</span><span class="sxs-lookup"><span data-stu-id="2ecaa-479">Form Data</span></span>  
    *   <span data-ttu-id="2ecaa-480">Parâmetros da cadeia de caracteres de consulta</span><span class="sxs-lookup"><span data-stu-id="2ecaa-480">Query String Parameters</span></span>  
    *   <span data-ttu-id="2ecaa-481">Headers de solicitação</span><span class="sxs-lookup"><span data-stu-id="2ecaa-481">Request Headers</span></span>  
    *   <span data-ttu-id="2ecaa-482">Headers de resposta</span><span class="sxs-lookup"><span data-stu-id="2ecaa-482">Response Headers</span></span>  
1.  <span data-ttu-id="2ecaa-483">Abra o menu contextual \(clique com o botão direito do mouse\) > **valor copiar**.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-483">Open the contextual menu \(right-click\) > **Copy value**.</span></span>  <span data-ttu-id="2ecaa-484">Agora você pode colar o valor em qualquer editor para revisá-lo.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-484">You may now paste the value into any editor to review it.</span></span>  
    
## <a name="change-the-layout-of-the-network-panel"></a><span data-ttu-id="2ecaa-485">Alterar o layout do painel Rede</span><span class="sxs-lookup"><span data-stu-id="2ecaa-485">Change the layout of the Network panel</span></span>  

<span data-ttu-id="2ecaa-486">Você pode expandir ou fechar \*\*\*\* seções da interface do usuário da ferramenta de rede para focalizar informações importantes.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-486">You may expand or collapse sections of the **Network** tool UI to focus important information.</span></span>  

### <a name="hide-the-filters-pane"></a><span data-ttu-id="2ecaa-487">Ocultar o painel Filtros</span><span class="sxs-lookup"><span data-stu-id="2ecaa-487">Hide the Filters pane</span></span>  

<span data-ttu-id="2ecaa-488">Por padrão, DevTools mostra o painel **Filtros.**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-488">By default, DevTools show the **Filters** pane.</span></span>  
<span data-ttu-id="2ecaa-489">Escolha **Filtrar** \( ![ ][ImageFilterIcon] Filtrar \) para o ocultar.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-489">Choose **Filter** \(![Filter][ImageFilterIcon]\) to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="O botão Ocultar Filtros" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="2ecaa-491">O botão Ocultar Filtros</span><span class="sxs-lookup"><span data-stu-id="2ecaa-491">The Hide Filters button</span></span>  
:::image-end:::  

### <a name="use-large-request-rows"></a><span data-ttu-id="2ecaa-492">Usar linhas de solicitação grandes</span><span class="sxs-lookup"><span data-stu-id="2ecaa-492">Use large request rows</span></span>  

<span data-ttu-id="2ecaa-493">Use linhas grandes quando quiser mais espaço em branco na tabela de solicitações de rede.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-493">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="2ecaa-494">Algumas colunas também fornecem um pouco mais de informações ao usar linhas grandes.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-494">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="2ecaa-495">Por exemplo, o valor inferior da coluna **Tamanho** é o tamanho não compactado de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-495">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Um exemplo de linhas de solicitação grandes no painel Solicitações" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="2ecaa-497">Um exemplo de linhas de solicitação grandes no painel **Solicitações**</span><span class="sxs-lookup"><span data-stu-id="2ecaa-497">An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="2ecaa-498">Para habilitar linhas grandes, ative a caixa de seleção **Usar linhas de solicitação** grandes.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-498">To enable large rows, turn on the **Use large request rows** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Caixa de seleção Usar linhas de solicitação grandes" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="2ecaa-500">Caixa **de seleção Usar linhas de solicitação** grandes</span><span class="sxs-lookup"><span data-stu-id="2ecaa-500">The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <a name="hide-the-overview-pane"></a><span data-ttu-id="2ecaa-501">Ocultar o painel Visão Geral</span><span class="sxs-lookup"><span data-stu-id="2ecaa-501">Hide the Overview pane</span></span>  

<span data-ttu-id="2ecaa-502">Por padrão, o DevTools exibe o painel **Visão** geral.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-502">By default, DevTools displays the **Overview** pane.</span></span>  <span data-ttu-id="2ecaa-503">Para o ocultar, desligue a caixa de seleção **Mostrar Visão** Geral.</span><span class="sxs-lookup"><span data-stu-id="2ecaa-503">To hide it, turn off the **Show Overview** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="A caixa de seleção Mostrar Visão Geral" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="2ecaa-505">A **caixa de seleção Mostrar Visão** Geral</span><span class="sxs-lookup"><span data-stu-id="2ecaa-505">The **Show Overview** checkbox</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2ecaa-506">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2ecaa-506">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Depurar aplicativos Web progressivos | Microsoft Docs"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URLs de dados | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Servidor proxy - Wikipédia"  

> [!NOTE]
> <span data-ttu-id="2ecaa-510">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2ecaa-510">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2ecaa-511">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/network/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="2ecaa-511">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2ecaa-513">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2ecaa-513">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
