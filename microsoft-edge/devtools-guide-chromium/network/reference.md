---
description: Uma referência abrangente dos recursos do painel de rede do Microsoft Edge DevTools.
title: Referência de análise de rede
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 8123fbebadf1d43fd1460ecebf91190cac793e19
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125367"
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

# <span data-ttu-id="5b0d6-104">Referência de análise de rede</span><span class="sxs-lookup"><span data-stu-id="5b0d6-104">Network Analysis reference</span></span>  

<span data-ttu-id="5b0d6-105">Descubra novas maneiras de analisar como a sua página é carregada nesta referência abrangente dos recursos de análise de rede do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  To verify which version of Microsoft Edge you are running, navigate to `edge://help`.  
-->

## <span data-ttu-id="5b0d6-106">Gravar solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="5b0d6-106">Record network requests</span></span>  

<span data-ttu-id="5b0d6-107">Por padrão, o DevTools registra todas as solicitações de rede no painel de rede, desde que DevTools esteja aberto.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-107">By default, DevTools record all network requests in the Network panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="5b0d6-109">Painel de **rede**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-109">The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-110">Parar a gravação de solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="5b0d6-110">Stop recording network requests</span></span>  

<span data-ttu-id="5b0d6-111">Para parar de gravar solicitações, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="5b0d6-112">Escolha **parar gravação do log** ![ de rede parar de gravar ][ImageRecordOnIcon] o log de rede no painel de **rede** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-112">Choose **Stop recording network log** ![Stop recording network log][ImageRecordOnIcon] on the **Network** panel.</span></span>  <span data-ttu-id="5b0d6-113">Ele fica cinza para indicar que o DevTools não está mais gravando solicitações.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="5b0d6-114">Selecione `Control` + `E` \ (Windows, Linux \) ou `Command` + `E` \ (MacOS \) enquanto o painel de **rede** estiver em foco.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-114">Select `Control`+`E` \(Windows, Linux\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="5b0d6-115">Solicitações de limpeza</span><span class="sxs-lookup"><span data-stu-id="5b0d6-115">Clear requests</span></span>  

<span data-ttu-id="5b0d6-116">Escolha **limpar** \ ( ![ limpar ][ImageClearIcon] \) no painel rede para limpar todas as solicitações da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-116">Choose **Clear** \(![Clear][ImageClearIcon]\) on the Network panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="5b0d6-118">O botão **limpar**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-118">The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-119">Salvar solicitações nas cargas de página</span><span class="sxs-lookup"><span data-stu-id="5b0d6-119">Save requests across page loads</span></span>  

<span data-ttu-id="5b0d6-120">Para salvar as solicitações nas cargas da página, marque a caixa de seleção **preservar registro** no painel rede.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-120">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="5b0d6-121">O DevTools salva todas as solicitações até você desabilitar o **preserve log**.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="5b0d6-123">A caixa de seleção **preservar registro**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-123">The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-124">Capturar capturas de tela durante o carregamento da página</span><span class="sxs-lookup"><span data-stu-id="5b0d6-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="5b0d6-125">Capture capturas de tela para analisar o que é exibido para os usuários enquanto aguarda a sua página ser carregada.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span></span>  

<span data-ttu-id="5b0d6-126">Para habilitar capturas de tela, escolha **configurações de rede** e escolha **capturar capturas de tela** no painel **rede** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-126">To enable screenshots, choose **Network settings** and choose **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="5b0d6-127">Atualize a página enquanto o painel de **rede** estiver em foco para capturar capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-127">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="5b0d6-128">Após a captura de uma captura de tela, você interage com ela das seguintes maneiras.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="5b0d6-129">Passe o mouse sobre uma captura de tela para ver o ponto em que a captura de tela foi capturada.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-129">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="5b0d6-130">Uma linha amarela é exibida no painel **visão geral** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-130">A yellow line is displayed on the **Overview** pane.</span></span>  
*   <span data-ttu-id="5b0d6-131">Selecione a miniatura de uma tela para filtrar todas as solicitações ocorridas após a captura da captura de tela.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-131">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="5b0d6-132">Clique duas vezes em uma miniatura para ampliá-la.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="5b0d6-134">Passar o mouse sobre uma captura de tela</span><span class="sxs-lookup"><span data-stu-id="5b0d6-134">Hovering over a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Painel de rede" lightbox="../media/network-replay-xhr.msft.png":::
   Selecting Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="5b0d6-135">Alterar comportamento de carregamento</span><span class="sxs-lookup"><span data-stu-id="5b0d6-135">Change loading behavior</span></span>  

### <span data-ttu-id="5b0d6-136">Emular um visitante da primeira vez desabilitando o cache do navegador</span><span class="sxs-lookup"><span data-stu-id="5b0d6-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="5b0d6-137">Para emular como um usuário da primeira vez experimenta o seu site, marque a caixa de seleção **desabilitar cache** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-137">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="5b0d6-138">DevTools desabilita o cache do navegador.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="5b0d6-139">Esse recurso emula de forma mais precisa uma experiência do usuário pela primeira vez, pois as solicitações são servidas do cache do navegador em visitas repetitivas.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="5b0d6-141">A caixa de seleção **desabilitar cache**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-141">The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="5b0d6-142">Desabilitar o cache do navegador da gaveta de condições da rede</span><span class="sxs-lookup"><span data-stu-id="5b0d6-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="5b0d6-143">Se você quiser desabilitar o cache enquanto trabalha em outros painéis do DevTools, use a gaveta de condições de rede.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="5b0d6-144">Abra a gaveta de **condições de rede** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="5b0d6-145">Marque ou desmarque a caixa de seleção **desativar cache** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-145">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="5b0d6-146">Limpar manualmente o cache do navegador</span><span class="sxs-lookup"><span data-stu-id="5b0d6-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="5b0d6-147">Para limpar manualmente o cache do navegador a qualquer momento, abra o menu contextual \ (clique com o botão direito do mouse \) em qualquer lugar na tabela solicitações e escolha **Limpar cache do navegador**.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and choose **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="5b0d6-149">Selecionando **Limpar cache do navegador**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-149">Selecting **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-150">Emular offline</span><span class="sxs-lookup"><span data-stu-id="5b0d6-150">Emulate offline</span></span>  

<span data-ttu-id="5b0d6-151">Uma nova classe de aplicativos Web, chamada [Web Apps progressivos][DevtoolsProgressiveWebApps], funciona offline com a ajuda do **serviço de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="5b0d6-152">Pode ser útil simular rapidamente um dispositivo que não tem conexão de dados quando você está criando esse tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="5b0d6-153">Selecione o menu suspenso **online** , procure em **predefinições**e escolha **offline** para simular uma experiência de rede offline.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-153">Select the **Online** dropdown menu, search under **Presets**, and choose **Offline** to simulate an offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="5b0d6-155">O menu suspenso **offline**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-155">The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-156">Emular conexões de rede lentas</span><span class="sxs-lookup"><span data-stu-id="5b0d6-156">Emulate slow network connections</span></span>  

<span data-ttu-id="5b0d6-157">Emular a conexão 3G, rápida 3G e outras velocidades de conexão a partir do menu suspenso **online** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="5b0d6-159">O menu suspenso **limitação**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-159">The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="5b0d6-160">Você pode selecionar em predefinições diferentes, como 3G ou Fast 3G.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-160">You may select from different presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="5b0d6-161">Você também pode adicionar suas próprias predefinições personalizadas abrindo o menu de limitação e selecionando **Custom**  >  **Adicionar**personalizado.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-161">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="5b0d6-162">O DevTools exibe um ícone de aviso ao lado da guia **rede** para lembrá-lo de que a limitação está habilitada.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-162">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="5b0d6-163">Emular conexões de rede lentas da gaveta de condições da rede</span><span class="sxs-lookup"><span data-stu-id="5b0d6-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="5b0d6-164">Se você quiser controlar a conexão de rede enquanto trabalha em outros painéis do DevTools, use a gaveta de condições de rede.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="5b0d6-165">Abra a gaveta de **condições de rede** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="5b0d6-166">Selecione a velocidade da conexão no menu **limitação** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-166">Select your connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="5b0d6-167">Limpar manualmente os cookies do navegador</span><span class="sxs-lookup"><span data-stu-id="5b0d6-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="5b0d6-168">Para limpar manualmente os cookies do navegador a qualquer momento, abra o menu contextual \ (clique com o botão direito do mouse \) em qualquer lugar na tabela solicitações e escolha **Limpar cookies do navegador**.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-168">To manually clear browser cookies at any time, open the contextual menu \(right-click\) anywhere in the Requests table and choose **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="5b0d6-170">Selecionando **Limpar cookies do navegador**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-170">Selecting **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-171">Substituir o agente do usuário</span><span class="sxs-lookup"><span data-stu-id="5b0d6-171">Override the user agent</span></span>  

<span data-ttu-id="5b0d6-172">Para substituir manualmente o agente de usuário, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-172">To manually override the user agent, use the following steps.</span></span>  

1.  <span data-ttu-id="5b0d6-173">Abra a gaveta de **condições de rede** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="5b0d6-174">Desmarque **selecionar automaticamente**.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-174">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="5b0d6-175">Escolha uma opção de agente do usuário no menu ou insira uma opção personalizada na caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="5b0d6-176">Filtrar solicitações</span><span class="sxs-lookup"><span data-stu-id="5b0d6-176">Filter requests</span></span>  

### <span data-ttu-id="5b0d6-177">Filtrar solicitações por propriedades</span><span class="sxs-lookup"><span data-stu-id="5b0d6-177">Filter requests by properties</span></span>  

<span data-ttu-id="5b0d6-178">Use a caixa de texto **Filtrar** para filtrar solicitações por propriedades, como o domínio ou o tamanho da solicitação.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="5b0d6-179">Se a caixa de texto não for exibida, o painel **filtros** provavelmente ficará oculto.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span></span>  
<span data-ttu-id="5b0d6-180">Para obter mais informações, navegue para [ocultar o painel filtros](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="5b0d6-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="5b0d6-182">A caixa de texto **filtro**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-182">The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="5b0d6-183">Você pode usar várias propriedades simultaneamente, separando cada propriedade com um espaço.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="5b0d6-184">Por exemplo, `mime-type:image/png larger-than:1K` exibe todas as PNGs maiores do que 1 kilobyte.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span></span>  <span data-ttu-id="5b0d6-185">Os filtros de várias propriedades são equivalentes às `AND` operações.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-185">The multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="5b0d6-186">Não há suporte para operações no momento.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-186">operations are currently not supported.</span></span>  

<span data-ttu-id="5b0d6-187">A lista completa de propriedades com suporte.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="5b0d6-188">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5b0d6-188">Property</span></span> | <span data-ttu-id="5b0d6-189">Detalhes</span><span class="sxs-lookup"><span data-stu-id="5b0d6-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="5b0d6-190">Exiba somente os recursos do domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="5b0d6-191">Você pode usar um caractere curinga \ ( `*` \) para incluir vários domínios.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="5b0d6-192">Por exemplo, `*.com` exibe os recursos de todos os nomes de domínio terminam em `.com` .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="5b0d6-193">DevTools popular o menu suspenso de preenchimento automático com todos os domínios encontrados.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span></span> |  
| `has-response-header` | <span data-ttu-id="5b0d6-194">Exibe os recursos que contêm o cabeçalho de resposta HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-194">Displays the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="5b0d6-195">DevTools popular a lista suspensa preenchimento automático com todos os cabeçalhos de resposta encontrados.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span></span> |  
| `is` | <span data-ttu-id="5b0d6-196">Use `is:running` para localizar `WebSocket` recursos.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="5b0d6-197">Exibe os recursos maiores do que o tamanho especificado, em bytes.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-197">Displays resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="5b0d6-198">Definir um valor `1000` é equivalente a definir um valor de `1k` .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="5b0d6-199">Exibe os recursos que foram recuperados em um tipo de método HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-199">Displays resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="5b0d6-200">DevTools popular a lista suspensa com todos os métodos HTTP que são encontrados.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span></span> |  
| `mime-type` | <span data-ttu-id="5b0d6-201">Exibe os recursos de um tipo MIME especificado.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-201">Displays resources of a specified MIME type.</span></span>  <span data-ttu-id="5b0d6-202">DevTools popular a lista suspensa com todos os tipos de MIME que são encontrados.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-202">DevTools populate the dropdown with all MIME types  that are found.</span></span> |  
| `mixed-content` | <span data-ttu-id="5b0d6-203">Mostrar todos os recursos de conteúdo mistos \ ( `mixed-content:all` \) ou apenas aqueles que são exibidos no momento \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="5b0d6-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="5b0d6-204">Exibe os recursos recuperados por HTTP \ ( `scheme:http` \) ou HTTPS protegido \ ( `scheme:https` \) protegido.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="5b0d6-205">Exibe os recursos que têm um `Set-Cookie` cabeçalho com um `Domain` atributo que corresponde ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="5b0d6-206">DevTools popular o preenchimento automático com todos os domínios de cookies encontrados.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="5b0d6-207">Exibe os recursos que têm um `Set-Cookie` cabeçalho com um nome que corresponde ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="5b0d6-208">DevTools popular o preenchimento automático com todos os nomes de cookies encontrados.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-208">DevTools populate the autocomplete with all of the cookie names that are found.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="5b0d6-209">Exibe os recursos que têm um `Set-Cookie` cabeçalho com um valor que corresponde ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="5b0d6-210">DevTools popular o preenchimento automático com todos os valores de cookies que são encontrados.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-210">DevTools populate the autocomplete with all of the cookie values that are found.</span></span> |  
| `status-code` | <span data-ttu-id="5b0d6-211">Exibe os recursos que correspondem ao código de status HTTP específico.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-211">Displays resources that match the specific HTTP status code.</span></span>  <span data-ttu-id="5b0d6-212">DevTools preenche o menu suspenso preenchimento automático com todos os códigos de status encontrados.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span></span> |  

### <span data-ttu-id="5b0d6-213">Filtrar solicitações por tipo</span><span class="sxs-lookup"><span data-stu-id="5b0d6-213">Filter requests by type</span></span>  

<span data-ttu-id="5b0d6-214">Para filtrar solicitações por tipo de solicitação, selecione um dos botões a seguir no painel **rede** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-214">To filter requests by request type, select the one of the following buttons on the **Network** panel.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-215">XHR</span><span class="sxs-lookup"><span data-stu-id="5b0d6-215">XHR</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-216">JS</span><span class="sxs-lookup"><span data-stu-id="5b0d6-216">JS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-217">CSS</span><span class="sxs-lookup"><span data-stu-id="5b0d6-217">CSS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-218">Img</span><span class="sxs-lookup"><span data-stu-id="5b0d6-218">Img</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-219">Media</span><span class="sxs-lookup"><span data-stu-id="5b0d6-219">Media</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-220">Fonte</span><span class="sxs-lookup"><span data-stu-id="5b0d6-220">Font</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-221">Documentação</span><span class="sxs-lookup"><span data-stu-id="5b0d6-221">Doc</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-222">WS</span><span class="sxs-lookup"><span data-stu-id="5b0d6-222">WS</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-223">WebSocket.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-223">WebSocket.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-224">Manifesto</span><span class="sxs-lookup"><span data-stu-id="5b0d6-224">Manifest</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-225">Other</span><span class="sxs-lookup"><span data-stu-id="5b0d6-225">Other</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-226">Qualquer outro tipo não listado.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-226">Any other type not listed.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="5b0d6-227">Se os botões não forem exibidos, o painel **filtros** poderá estar oculto.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-227">If the buttons do not display, the **Filters** pane may be hidden.</span></span>  
<span data-ttu-id="5b0d6-228">Para obter mais informações, navegue para [ocultar o painel filtros](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="5b0d6-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="5b0d6-229">Para habilitar vários filtros de tipo simultaneamente, segure `Control` \ (Windows, Linux \) ou `Command` \ (MacOS \) e, em seguida, selecione.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-229">To enable multiple type filters simultaneously, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then select.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="5b0d6-231">Usar os filtros de tipo para exibir os recursos de documento, CSS e JS</span><span class="sxs-lookup"><span data-stu-id="5b0d6-231">Using the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-232">Filtrar solicitações por tempo</span><span class="sxs-lookup"><span data-stu-id="5b0d6-232">Filter requests by time</span></span>  

<span data-ttu-id="5b0d6-233">Selecione e arraste para a esquerda ou direita no painel Visão geral para exibir apenas as solicitações que estavam ativas durante esse período de tempo.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-233">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="5b0d6-234">O filtro é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-234">The filter is inclusive.</span></span>  <span data-ttu-id="5b0d6-235">Todas as solicitações ativas durante o tempo realçado são mostradas.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-235">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="5b0d6-237">Filtragem de todas as solicitações que estavam inativas em torno de 300 MS</span><span class="sxs-lookup"><span data-stu-id="5b0d6-237">Filtering out any requests that were inactive around 300 ms</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-238">Ocultar URLs de dados</span><span class="sxs-lookup"><span data-stu-id="5b0d6-238">Hide data URLs</span></span>  

<span data-ttu-id="5b0d6-239">As [URLs de dados][MDNHTTPDataURIs] são pequenos arquivos incorporados a outros documentos.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="5b0d6-240">Qualquer solicitação que é exibida na tabela solicitações que começa com `data:` é uma URL de dados.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="5b0d6-241">Marque a caixa de seleção **ocultar URLs de dados** para ocultar as solicitações.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-241">Check the **Hide data URLs** checkbox to hide the requests.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="5b0d6-243">A caixa de seleção **ocultar URLs de dados**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-243">The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="5b0d6-244">Solicitações de classificação</span><span class="sxs-lookup"><span data-stu-id="5b0d6-244">Sort requests</span></span>  

<span data-ttu-id="5b0d6-245">Por padrão, as solicitações na tabela solicitações são classificadas por hora de início, mas você pode classificar a tabela usando outros critérios.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="5b0d6-246">Classificar por coluna</span><span class="sxs-lookup"><span data-stu-id="5b0d6-246">Sort by column</span></span>  

<span data-ttu-id="5b0d6-247">Selecione o cabeçalho de qualquer coluna nas solicitações para classificar solicitações por essa coluna.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-247">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="5b0d6-248">Fase classificar por atividade</span><span class="sxs-lookup"><span data-stu-id="5b0d6-248">Sort by activity phase</span></span>  

<span data-ttu-id="5b0d6-249">Para alterar a forma como a cascata classifica solicitações, passe o cursor do mouse sobre o cabeçalho da tabela solicitações, abra o menu contextual \ (clique com o botão direito do mouse \), passe o mouse sobre a **cascata**e selecione uma das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover over **Waterfall**, and select one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-250">Hora de início</span><span class="sxs-lookup"><span data-stu-id="5b0d6-250">Start Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-251">A primeira solicitação iniciada está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-251">The first request that was initiated is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-252">Tempo de resposta</span><span class="sxs-lookup"><span data-stu-id="5b0d6-252">Response Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-253">A primeira solicitação iniciada para download está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-253">The first request that started downloading is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-254">Hora de término</span><span class="sxs-lookup"><span data-stu-id="5b0d6-254">End Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-255">A primeira solicitação que terminou está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-255">The first request that finished is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-256">Duração total</span><span class="sxs-lookup"><span data-stu-id="5b0d6-256">Total Duration</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-257">A solicitação com as configurações de conexão mais curtas e solicitação ou resposta está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-257">The request with the shortest connection settings and request or response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-258">Latência</span><span class="sxs-lookup"><span data-stu-id="5b0d6-258">Latency</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-259">A solicitação que aguardou o tempo mais curto para uma resposta está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-259">The request that waited the shortest time for a response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="5b0d6-260">Essas descrições pressupõem que cada opção respectiva seja classificada da mais curta para a mais longa.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="5b0d6-261">A seleção do cabeçalho da coluna em **cascata** inverte a ordem.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-261">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="5b0d6-263">Classificar a cascata com duração total \ (a parte mais clara de cada barra é o tempo gasto aguardando e a parte mais escura é o tempo gasto para baixar bytes \)</span><span class="sxs-lookup"><span data-stu-id="5b0d6-263">Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="5b0d6-264">Analisar solicitações</span><span class="sxs-lookup"><span data-stu-id="5b0d6-264">Analyze requests</span></span>  

<span data-ttu-id="5b0d6-265">Desde que o DevTools esteja aberto, ele registra todas as solicitações no painel de rede.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-265">So long as DevTools are open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="5b0d6-266">Use o painel rede para analisar solicitações.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-266">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="5b0d6-267">Exibir um log de solicitações</span><span class="sxs-lookup"><span data-stu-id="5b0d6-267">View a log of requests</span></span>  

<span data-ttu-id="5b0d6-268">Use a tabela requests para exibir um log de todas as solicitações feitas enquanto o DevTools está aberto.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-268">Use the Requests table to view a log of all requests made while DevTools have been open.</span></span>  <span data-ttu-id="5b0d6-269">Selecionar ou passar o mouse nas solicitações revela mais informações sobre cada item.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-269">Selecting or hovering over requests reveals more information about each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="5b0d6-271">A tabela solicitações</span><span class="sxs-lookup"><span data-stu-id="5b0d6-271">The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="5b0d6-272">A tabela solicitações exibe as seguintes colunas por padrão.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-272">The Requests table displays the following columns by default.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-273">Nome</span><span class="sxs-lookup"><span data-stu-id="5b0d6-273">Name</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-274">O nome do recurso ou um identificador para o recurso.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-274">The filename of, or an identifier for, the resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-275">Status</span><span class="sxs-lookup"><span data-stu-id="5b0d6-275">Status</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-276">O código de status HTTP.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-276">The HTTP status code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-277">Tipo</span><span class="sxs-lookup"><span data-stu-id="5b0d6-277">Type</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-278">O tipo MIME do recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-278">The MIME type of the requested resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-279">Inicia</span><span class="sxs-lookup"><span data-stu-id="5b0d6-279">Initiator</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-280">Os seguintes objetos ou processos iniciam solicitações.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-280">The following objects or processes initiate requests.</span></span>  
      
      *   <span data-ttu-id="5b0d6-281">**Analisador**  O analisador HTML para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-281">**Parser**  The HTML parser for Microsoft Edge.</span></span>  
      *   <span data-ttu-id="5b0d6-282">**Redirecionar**  Um redirecionamento HTTP.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-282">**Redirect**  An HTTP redirect.</span></span>  
      *   <span data-ttu-id="5b0d6-283">**Script**  Uma função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-283">**Script**  A JavaScript function.</span></span>  
      *   <span data-ttu-id="5b0d6-284">**Outros**  Algum outro processo ou ação, como navegar para uma página usando um link ou inserir uma URL na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-285">Size</span><span class="sxs-lookup"><span data-stu-id="5b0d6-285">Size</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-286">O tamanho combinado dos cabeçalhos de resposta mais o corpo da resposta, conforme entregue pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-286">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-287">Hora</span><span class="sxs-lookup"><span data-stu-id="5b0d6-287">Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-288">A duração total, desde o início da solicitação até o recebimento do byte final na resposta.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="5b0d6-289">Água</span><span class="sxs-lookup"><span data-stu-id="5b0d6-289">Waterfall</span></span>](#view-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-290">Uma divisão Visual da atividade para cada solicitação.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-290">A visual breakdown of the activity for each request.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="5b0d6-291">Adicionar ou remover colunas</span><span class="sxs-lookup"><span data-stu-id="5b0d6-291">Add or remove columns</span></span>  

<span data-ttu-id="5b0d6-292">Passe o mouse sobre o cabeçalho da tabela solicitações, abra o menu contextual \ (clique com o botão direito do mouse \) e selecione uma opção para ocultá-la ou mostrá-la.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and select an option to hide or show it.</span></span>  <span data-ttu-id="5b0d6-293">As opções atualmente exibidas têm marcas de opção ao lado de cada item.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-293">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="5b0d6-295">Adicionar uma coluna à tabela solicitações</span><span class="sxs-lookup"><span data-stu-id="5b0d6-295">Adding a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="5b0d6-296">Adicionar colunas personalizadas</span><span class="sxs-lookup"><span data-stu-id="5b0d6-296">Add custom columns</span></span>  

<span data-ttu-id="5b0d6-297">Para adicionar uma coluna personalizada à tabela solicitações, passe o mouse sobre o cabeçalho da tabela solicitações, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **cabeçalhos de resposta**  >  **gerenciar colunas de cabeçalho**.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and choose **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="5b0d6-299">Adicionando uma coluna personalizada à tabela solicitações</span><span class="sxs-lookup"><span data-stu-id="5b0d6-299">Adding a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-300">Exibir a relação de tempo de solicitações</span><span class="sxs-lookup"><span data-stu-id="5b0d6-300">View the timing relationship of requests</span></span>  

<span data-ttu-id="5b0d6-301">Use a cascata para ver as relações de tempo das solicitações.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-301">Use the Waterfall to view the timing relationships of requests.</span></span>  
<span data-ttu-id="5b0d6-302">A organização padrão da cascata usa a hora de início das solicitações.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-302">The default organization of the Waterfall uses the start time of the requests.</span></span>  
<span data-ttu-id="5b0d6-303">Portanto, as solicitações mais distantes do lado esquerdo são mais antigas do que as solicitações mais distantes da direita.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span></span>  

<span data-ttu-id="5b0d6-304">Para revisar as diferentes maneiras pelas quais você pode classificar a cascata, navegue até a [fase classificar por atividade](#sort-by-activity-phase).</span><span class="sxs-lookup"><span data-stu-id="5b0d6-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="5b0d6-306">A coluna de cascata do painel **solicitações**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-306">The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To view the frames of a WebSocket connection, use the following steps.  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-select the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="Painel de rede" lightbox="../media/network-frames.msft.png":::
   The **Frames** tab  
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

### <span data-ttu-id="5b0d6-307">Exibir uma visualização de um corpo de resposta</span><span class="sxs-lookup"><span data-stu-id="5b0d6-307">View a preview of a response body</span></span>  

<span data-ttu-id="5b0d6-308">Para exibir uma visualização de um corpo de resposta, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-308">To view a preview of a response body, use the following steps.</span></span>  

1.  <span data-ttu-id="5b0d6-309">Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-309">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="5b0d6-310">Selecione a guia **Visualizar** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-310">Select the **Preview** tab.</span></span>  

<span data-ttu-id="5b0d6-311">Esta guia é principalmente útil para exibir imagens.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-311">This tab is mostly useful for viewing images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="5b0d6-313">A guia **Visualização**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-313">The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-314">Exibir um corpo de resposta</span><span class="sxs-lookup"><span data-stu-id="5b0d6-314">View a response body</span></span>  

<span data-ttu-id="5b0d6-315">Para exibir o corpo da resposta a uma solicitação, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-315">To view the response body to a request, use the following steps.</span></span>  

1.  <span data-ttu-id="5b0d6-316">Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-316">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="5b0d6-317">Selecione a guia **resposta** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-317">Select the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="5b0d6-319">A guia **resposta**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-319">The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-320">Exibir cabeçalhos HTTP</span><span class="sxs-lookup"><span data-stu-id="5b0d6-320">View HTTP headers</span></span>  

<span data-ttu-id="5b0d6-321">Para exibir dados de cabeçalho HTTP sobre uma solicitação, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-321">To view HTTP header data about a request, use the following steps.</span></span>  

1.  <span data-ttu-id="5b0d6-322">Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-322">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="5b0d6-323">Selecione a guia **cabeçalhos** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-323">Select the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Painel de rede" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="5b0d6-325">A guia **cabeçalhos**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-325">The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="5b0d6-326">Exibir fonte de cabeçalho HTTP</span><span class="sxs-lookup"><span data-stu-id="5b0d6-326">View HTTP header source</span></span>  

<span data-ttu-id="5b0d6-327">Por padrão, a guia cabeçalhos mostra os nomes dos cabeçalhos em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-327">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="5b0d6-328">Para exibir os nomes dos cabeçalhos HTTP na ordem recebida, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-328">To view the HTTP header names in the order received, use the following steps.</span></span>  

1.  <span data-ttu-id="5b0d6-329">Abra a guia **cabeçalhos** para a solicitação que lhe interessa.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-329">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="5b0d6-330">Para obter mais informações, navegue para [Ver os cabeçalhos HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="5b0d6-330">For more information, navigate to [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="5b0d6-331">Escolha **Exibir fonte**, ao lado da seção cabeçalho da **solicitação** ou **cabeçalho de resposta** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-331">Choose **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="5b0d6-332">Exibir parâmetros da cadeia de caracteres de consulta</span><span class="sxs-lookup"><span data-stu-id="5b0d6-332">View query string parameters</span></span>  

<span data-ttu-id="5b0d6-333">Para exibir os parâmetros da cadeia de caracteres de consulta de uma URL em um formato legível pelo homem, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-333">To view the query string parameters of a URL in a human-readable format, use the following steps.</span></span>  

1.  <span data-ttu-id="5b0d6-334">Abra a guia **cabeçalhos** para a solicitação que lhe interessa.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-334">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="5b0d6-335">Para obter mais informações, navegue para [Ver os cabeçalhos HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="5b0d6-335">For more information, navigate to [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="5b0d6-336">Vá para a seção **parâmetros da cadeia de caracteres de consulta** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-336">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="5b0d6-338">A seção **parâmetros da cadeia de consulta**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-338">The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="5b0d6-339">Exibir origem dos parâmetros da cadeia de consulta</span><span class="sxs-lookup"><span data-stu-id="5b0d6-339">View query string parameters source</span></span>  

<span data-ttu-id="5b0d6-340">Para exibir a origem do parâmetro da cadeia de caracteres de consulta de uma solicitação, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-340">To view the query string parameter source of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="5b0d6-341">Vá para a seção parâmetros da cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-341">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="5b0d6-342">Para obter mais informações, navegue para [exibir os parâmetros da cadeia de consulta](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="5b0d6-342">For more information, navigate to [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="5b0d6-343">Escolha **Exibir fonte**.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-343">Choose **view source**.</span></span>  

#### <span data-ttu-id="5b0d6-344">Exibir parâmetros da cadeia de consulta codificada por URL</span><span class="sxs-lookup"><span data-stu-id="5b0d6-344">View URL-encoded query string parameters</span></span>  

<span data-ttu-id="5b0d6-345">Para exibir os parâmetros da cadeia de caracteres de consulta em um formato legível pelo homem, mas com codificações preservadas, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-345">To view query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span></span>  

1.  <span data-ttu-id="5b0d6-346">Vá para a seção parâmetros da cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-346">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="5b0d6-347">Para obter mais informações, navegue para [exibir os parâmetros da cadeia de consulta](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="5b0d6-347">For more information, navigate to [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="5b0d6-348">Escolha **exibir URL codificado**.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-348">Choose **view URL encoded**.</span></span>  

### <span data-ttu-id="5b0d6-349">Exibir cookies</span><span class="sxs-lookup"><span data-stu-id="5b0d6-349">View cookies</span></span>  

<span data-ttu-id="5b0d6-350">Para exibir os cookies enviados no cabeçalho HTTP de uma solicitação, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-350">To view the cookies sent in the HTTP header of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="5b0d6-351">Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-351">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="5b0d6-352">Selecione a guia **cookies** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-352">Select the **Cookies** tab.</span></span>  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="5b0d6-354">A guia cookies</span><span class="sxs-lookup"><span data-stu-id="5b0d6-354">The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-355">Exibir a divisão de tempo de uma solicitação</span><span class="sxs-lookup"><span data-stu-id="5b0d6-355">View the timing breakdown of a request</span></span>  

<span data-ttu-id="5b0d6-356">Para exibir a divisão de tempo de uma solicitação, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-356">To view the timing breakdown of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="5b0d6-357">Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-357">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="5b0d6-358">Selecione a guia **intervalo** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-358">Select the **Timing** tab.</span></span>  

<span data-ttu-id="5b0d6-359">Para obter uma maneira mais rápida de acessar os dados, navegue até [Visualizar uma divisão de intervalo](#preview-a-timing-breakdown).</span><span class="sxs-lookup"><span data-stu-id="5b0d6-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span></span>  

<span data-ttu-id="5b0d6-360">Para obter mais informações sobre cada uma das fases que podem ser exibidas na guia **intervalo** , navegue até [fases da divisão de tempo explicadas](#timing-breakdown-phases-explained).</span><span class="sxs-lookup"><span data-stu-id="5b0d6-360">For more information about each of the phases that may be displayed in the **Timing** tab, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="5b0d6-362">A guia **intervalo**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-362">The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="5b0d6-363">Mais informações sobre cada uma das fases.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-363">More information about each of the phases.</span></span>  

<span data-ttu-id="5b0d6-364">Para obter mais informações sobre como acessar o modo de exibição, navegue para [exibir a divisão de tempo](#view-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="5b0d6-364">For more information about accessing the view, navigate to [View timing breakdown](#view-the-timing-breakdown-of-a-request).</span></span>  

#### <span data-ttu-id="5b0d6-365">Visualizar uma divisão de intervalo</span><span class="sxs-lookup"><span data-stu-id="5b0d6-365">Preview a timing breakdown</span></span>  

<span data-ttu-id="5b0d6-366">Para exibir uma visualização da divisão de tempo de uma solicitação, na coluna **cascata** da tabela solicitações, passe o mouse sobre a entrada da solicitação.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-366">To view a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span></span>  

<span data-ttu-id="5b0d6-367">Para obter mais informações sobre como acessar os dados sem passar o mouse, navegue para [exibir a divisão de tempo de uma solicitação](#view-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="5b0d6-367">For more information about how to access the data without hovering, navigate to [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request).</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="5b0d6-369">Visualizando a divisão de tempo de uma solicitação</span><span class="sxs-lookup"><span data-stu-id="5b0d6-369">Previewing the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="5b0d6-370">Fases da divisão de tempo explicadas</span><span class="sxs-lookup"><span data-stu-id="5b0d6-370">Timing breakdown phases explained</span></span>  

<span data-ttu-id="5b0d6-371">Mais informações sobre cada uma das fases que podem ser exibidas na guia **intervalo** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-371">More information about each of the phases that may display in the **Timing** tab.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-372">Enfileiramento</span><span class="sxs-lookup"><span data-stu-id="5b0d6-372">Queueing</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-373">O navegador enfileira solicitações quando qualquer uma das seguintes opções é verdadeira.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-373">The browser queues requests when any of the following are true.</span></span>  
      *   <span data-ttu-id="5b0d6-374">Há solicitações de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-374">Higher priority requests exist.</span></span>  
      *   <span data-ttu-id="5b0d6-375">Seis conexões TCP estão abertas para a mesma origem, que é o limite.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-375">Six TCP connections are open for the same origin, which is the limit.</span></span>  <span data-ttu-id="5b0d6-376">Aplica-se somente a HTTP/1.0 e HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
      *   <span data-ttu-id="5b0d6-377">O navegador está alocando um espaço brevemente no cache de disco.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-377">The browser is briefly allocating space in the disk cache.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-378">Paralisação</span><span class="sxs-lookup"><span data-stu-id="5b0d6-378">Stalled</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-379">A solicitação é interrompida por qualquer um dos motivos descritos no **enfileiramento**.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-379">The request is stalled for any of the reasons described in **Queueing**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-380">Pesquisa de DNS</span><span class="sxs-lookup"><span data-stu-id="5b0d6-380">DNS Lookup</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-381">O navegador está resolvendo o endereço IP da solicitação.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-381">The browser is resolving the IP address for the request.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-382">Conexão inicial</span><span class="sxs-lookup"><span data-stu-id="5b0d6-382">Initial connection</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-383">O navegador estabelece uma conexão, incluindo Handshakes TCP, tentativas de TCP e negocia uma camada de soquete segura.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-384">Negociação de proxy</span><span class="sxs-lookup"><span data-stu-id="5b0d6-384">Proxy negotiation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-385">O navegador está negociando a solicitação com um [servidor proxy][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="5b0d6-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-386">Solicitação enviada</span><span class="sxs-lookup"><span data-stu-id="5b0d6-386">Request sent</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-387">A solicitação está sendo enviada.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-387">The request is being sent.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-388">Preparação do trabalho</span><span class="sxs-lookup"><span data-stu-id="5b0d6-388">ServiceWorker Preparation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-389">O navegador está iniciando o trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-389">The browser is starting the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-390">Solicitação para o serviço de serviço</span><span class="sxs-lookup"><span data-stu-id="5b0d6-390">Request to ServiceWorker</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-391">A solicitação está sendo enviada para o trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-391">The request is being sent to the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-392">Aguardando \ (TTFB \)</span><span class="sxs-lookup"><span data-stu-id="5b0d6-392">Waiting \(TTFB\)</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-393">O navegador está aguardando o primeiro byte de uma resposta.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-393">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="5b0d6-394">TTFB significa tempo até o primeiro byte.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-394">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="5b0d6-395">Esse intervalo inclui uma viagem de ida e volta da latência e o tempo gasto pelo servidor para preparar a resposta.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-396">Download de conteúdo</span><span class="sxs-lookup"><span data-stu-id="5b0d6-396">Content Download</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-397">O navegador está recebendo a resposta.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-397">The browser is receiving the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-398">Recebimento de envio</span><span class="sxs-lookup"><span data-stu-id="5b0d6-398">Receiving Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-399">O navegador está recebendo dados para esta resposta via Push HTTP/2 Server Push.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-399">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-400">Envio de leitura</span><span class="sxs-lookup"><span data-stu-id="5b0d6-400">Reading Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-401">O navegador está lendo os dados locais anteriormente recebidos.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-401">The browser is reading the local data previously received.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="5b0d6-402">Exibir iniciadores e dependências</span><span class="sxs-lookup"><span data-stu-id="5b0d6-402">View initiators and dependencies</span></span>  

<span data-ttu-id="5b0d6-403">Para ver os iniciadores e as dependências de uma solicitação, mantenha o `Shift` cursor sobre a solicitação na tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-403">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="5b0d6-404">Cores DevTools: os iniciadores são exibidos em verde e as dependências são mostradas em vermelho.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="5b0d6-406">Exibindo os iniciadores e as dependências de uma solicitação</span><span class="sxs-lookup"><span data-stu-id="5b0d6-406">Viewing the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="5b0d6-407">Quando a tabela de solicitações for ordenada cronologicamente, se você passar o mouse em uma linha, a linha anterior será exibida uma solicitação verde.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span></span>  <span data-ttu-id="5b0d6-408">A solicitação verde é o iniciador da dependência.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-408">The green request is the initiator of the dependency.</span></span>  <span data-ttu-id="5b0d6-409">Se outra solicitação verde for exibida na linha antes disso, essa solicitação mais alta será o iniciador do iniciador.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="5b0d6-410">E assim em diante.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-410">And so on.</span></span>  

### <span data-ttu-id="5b0d6-411">Exibir eventos de carga</span><span class="sxs-lookup"><span data-stu-id="5b0d6-411">View load events</span></span>  

<span data-ttu-id="5b0d6-412">DevTools exibe a temporização dos `DOMContentLoaded` eventos e de `load` vários locais no painel de rede.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="5b0d6-413">O `DOMContentLoaded` evento está em azul colorido e o `load` evento está em vermelho.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="5b0d6-415">Os locais dos `DOMContentLoaded` eventos e do `load` painel de rede</span><span class="sxs-lookup"><span data-stu-id="5b0d6-415">The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-416">Ver o número total de solicitações</span><span class="sxs-lookup"><span data-stu-id="5b0d6-416">View the total number of requests</span></span>  

<span data-ttu-id="5b0d6-417">O número total de solicitações está listado no painel Resumo, na parte inferior do painel de rede.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-417">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="5b0d6-418">Esse número controla apenas as solicitações que foram registradas desde que o DevTools foi aberto.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-418">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="5b0d6-419">Se ocorrerem outras solicitações antes da abertura do DevTools, essas solicitações não serão contadas.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-419">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="5b0d6-421">O número total de solicitações desde que o DevTools foi aberto</span><span class="sxs-lookup"><span data-stu-id="5b0d6-421">The total number of requests since DevTools were opened</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-422">Ver o tamanho total do download</span><span class="sxs-lookup"><span data-stu-id="5b0d6-422">View the total download size</span></span>  

<span data-ttu-id="5b0d6-423">O tamanho total do download de solicitações é listado no painel Resumo, na parte inferior do painel de rede.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-423">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="5b0d6-424">Esse número controla apenas as solicitações que foram registradas desde que o DevTools foi aberto.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-424">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="5b0d6-425">Se ocorrerem outras solicitações antes da abertura do DevTools, as solicitações anteriores não serão contadas.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="5b0d6-427">O tamanho total do download de solicitações</span><span class="sxs-lookup"><span data-stu-id="5b0d6-427">The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="5b0d6-428">Para verificar a quantidade de recursos grandes após o navegador descompactar cada item, navegue para [Exibir o tamanho descompactado de um recurso](#view-the-uncompressed-size-of-a-resource).</span><span class="sxs-lookup"><span data-stu-id="5b0d6-428">To verify how large resources are after the browser uncompresses each item, navigate to [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource).</span></span>  

### <span data-ttu-id="5b0d6-429">Exibir o rastreamento de pilha que causou uma solicitação</span><span class="sxs-lookup"><span data-stu-id="5b0d6-429">View the stack trace that caused a request</span></span>  

<span data-ttu-id="5b0d6-430">Depois que uma instrução JavaScript solicita um recurso, passe o mouse sobre a coluna do **iniciador** para exibir o rastreamento de pilha que leva à solicitação.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-430">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="5b0d6-432">O rastreamento de pilha que leva a uma solicitação de recurso</span><span class="sxs-lookup"><span data-stu-id="5b0d6-432">The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-433">Exibir o tamanho descompactado de um recurso</span><span class="sxs-lookup"><span data-stu-id="5b0d6-433">View the uncompressed size of a resource</span></span>  

<span data-ttu-id="5b0d6-434">Marque a caixa de seleção **usar linhas de solicitação grandes** e examine o valor inferior da coluna **tamanho** .</span><span class="sxs-lookup"><span data-stu-id="5b0d6-434">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="5b0d6-436">Um exemplo de recursos não compactados \ (o tamanho compactado do `jquery-3.3.1.min.js` arquivo que foi enviado pela rede foi `29.9 KB` , enquanto o tamanho não compactado era `84.9 KB` \)</span><span class="sxs-lookup"><span data-stu-id="5b0d6-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="5b0d6-437">Exportar dados de solicitações</span><span class="sxs-lookup"><span data-stu-id="5b0d6-437">Export requests data</span></span>  

### <span data-ttu-id="5b0d6-438">Salvar todas as solicitações de rede em um arquivo HAR</span><span class="sxs-lookup"><span data-stu-id="5b0d6-438">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="5b0d6-439">Para salvar todas as solicitações de rede em um arquivo HAR, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-439">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="5b0d6-440">Passe o mouse sobre qualquer solicitação na tabela solicitações e abra o menu contextual \ (clique com o botão direito do mouse \).</span><span class="sxs-lookup"><span data-stu-id="5b0d6-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="5b0d6-441">Escolha **salvar como Har com conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-441">Choose **Save as HAR with Content**.</span></span>  <span data-ttu-id="5b0d6-442">DevTools salva todas as solicitações ocorridas desde que você abriu o DevTools para o arquivo HAR.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="5b0d6-443">Você não pode filtrar solicitações.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-443">You are not able to filter requests.</span></span>  <span data-ttu-id="5b0d6-444">Você também não pode salvar uma única solicitação.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-444">You are also not able to save a single request.</span></span>  

<span data-ttu-id="5b0d6-445">Depois de salvar um arquivo HAR, você poderá importá-lo novamente no DevTools para análise.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="5b0d6-446">Basta arrastar e soltar o arquivo HAR na tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-446">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="5b0d6-448">Selecionando **salvar como Har com conteúdo**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-448">Selecting **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-449">Copiar uma ou mais solicitações para a área de transferência</span><span class="sxs-lookup"><span data-stu-id="5b0d6-449">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="5b0d6-450">Na coluna **nome** da tabela solicitações, passe o mouse sobre uma solicitação, abra o menu contextual \ (clique com o botão direito do mouse \), passe o mouse sobre a **cópia**e selecione uma das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover over **Copy**, and select one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-451">Copiar endereço do link</span><span class="sxs-lookup"><span data-stu-id="5b0d6-451">Copy Link Address</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-452">Copie a URL da solicitação para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-452">Copy the URL of the request to the clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-453">Copiar resposta</span><span class="sxs-lookup"><span data-stu-id="5b0d6-453">Copy Response</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-454">Copie o corpo da resposta para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-454">Copy the response body to the clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-455">Copiar como busca</span><span class="sxs-lookup"><span data-stu-id="5b0d6-455">Copy as Fetch</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-456">Copiar como ondulação</span><span class="sxs-lookup"><span data-stu-id="5b0d6-456">Copy as cURL</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-457">Copie a solicitação como um comando de rotação.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-457">Copy the request as a cURL command.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-458">Copiar tudo como busca</span><span class="sxs-lookup"><span data-stu-id="5b0d6-458">Copy All as Fetch</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-459">Copiar tudo como ondulação</span><span class="sxs-lookup"><span data-stu-id="5b0d6-459">Copy All as cURL</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-460">Copie todas as solicitações como uma cadeia de comandos de ondulação.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-460">Copy all requests as a chain of cURL commands.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="5b0d6-461">Copiar tudo como HAR</span><span class="sxs-lookup"><span data-stu-id="5b0d6-461">Copy All as HAR</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5b0d6-462">Copie todas as solicitações como dados de HAR.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-462">Copy all requests as HAR data.</span></span>  
   :::column-end:::
:::row-end:::  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="5b0d6-464">Selecionando a **resposta de cópia**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-464">Selecting **Copy Response**</span></span>  
:::image-end:::  

## <span data-ttu-id="5b0d6-465">Alterar o layout do painel de rede</span><span class="sxs-lookup"><span data-stu-id="5b0d6-465">Change the layout of the Network panel</span></span>  

<span data-ttu-id="5b0d6-466">Você pode expandir ou recolher seções da interface do usuário do painel de rede para concentrar informações importantes.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-466">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="5b0d6-467">Ocultar o painel filtros</span><span class="sxs-lookup"><span data-stu-id="5b0d6-467">Hide the Filters pane</span></span>  

<span data-ttu-id="5b0d6-468">Por padrão, o DevTools mostra o **painel filtros**.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-468">By default, DevTools show the **Filters pane**.</span></span>  
<span data-ttu-id="5b0d6-469">Escolha **filtro** \ ( ![ filtro ][ImageFilterIcon] \) para ocultá-lo.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-469">Choose **Filter** \(![Filter][ImageFilterIcon]\) to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="5b0d6-471">O botão Ocultar filtros</span><span class="sxs-lookup"><span data-stu-id="5b0d6-471">The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-472">Usar linhas de solicitação grandes</span><span class="sxs-lookup"><span data-stu-id="5b0d6-472">Use large request rows</span></span>  

<span data-ttu-id="5b0d6-473">Use linhas grandes quando quiser mais espaço em branco na tabela solicitações de rede.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-473">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="5b0d6-474">Algumas colunas também fornecem um pouco mais de informações ao usar linhas grandes.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-474">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="5b0d6-475">Por exemplo, o valor inferior da coluna **tamanho** é o tamanho descompactado de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-475">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="5b0d6-477">Um exemplo de linhas de solicitação grandes no painel **solicitações**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-477">An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="5b0d6-478">Marque a caixa de seleção **usar linhas de solicitação grandes** para habilitar linhas grandes.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-478">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="5b0d6-480">A caixa de seleção **usar linhas de solicitação grandes**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-480">The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="5b0d6-481">Ocultar o painel Visão geral</span><span class="sxs-lookup"><span data-stu-id="5b0d6-481">Hide the Overview pane</span></span>  

<span data-ttu-id="5b0d6-482">Por padrão, o DevTools mostra o **painel Visão geral**.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-482">By default, DevTools show the **Overview pane**.</span></span>  <span data-ttu-id="5b0d6-483">Desmarque a caixa de seleção **Mostrar visão geral** para ocultá-la.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-483">Deselect the **Show Overview** checkbox to hide it.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Painel de rede" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="5b0d6-485">A caixa de seleção **Mostrar visão geral**</span><span class="sxs-lookup"><span data-stu-id="5b0d6-485">The **Show Overview** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="5b0d6-486">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5b0d6-486">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps.md "Depurar aplicativos Web progressivos | Documentos da Microsoft"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URLs de dados | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Servidor proxy-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="5b0d6-490">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="5b0d6-490">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5b0d6-491">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/network/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5b0d6-491">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5b0d6-493">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5b0d6-493">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
