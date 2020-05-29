---
title: Referência de análise de rede
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 460ad05983e7615e8739953ce3cb7d559492bc90
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611837"
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







# <span data-ttu-id="7f823-103">Referência de análise de rede</span><span class="sxs-lookup"><span data-stu-id="7f823-103">Network Analysis Reference</span></span>   



<span data-ttu-id="7f823-104">Descubra novas maneiras de analisar como a sua página é carregada nesta referência abrangente dos recursos de análise de rede do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="7f823-104">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## <span data-ttu-id="7f823-105">Gravar solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="7f823-105">Record network requests</span></span>   

<span data-ttu-id="7f823-106">Por padrão, o DevTools registra todas as solicitações de rede no painel de rede, desde que DevTools esteja aberto.</span><span class="sxs-lookup"><span data-stu-id="7f823-106">By default, DevTools records all network requests in the Network panel, so long as DevTools is open.</span></span>  

> ##### <span data-ttu-id="7f823-107">Figura 1</span><span class="sxs-lookup"><span data-stu-id="7f823-107">Figure 1</span></span>  
> <span data-ttu-id="7f823-108">Painel de rede</span><span class="sxs-lookup"><span data-stu-id="7f823-108">The Network panel</span></span>  
> ![Painel de rede][ImageNetworkPanel]  

### <span data-ttu-id="7f823-110">Parar a gravação de solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="7f823-110">Stop recording network requests</span></span>   

<span data-ttu-id="7f823-111">Para parar de gravar solicitações:</span><span class="sxs-lookup"><span data-stu-id="7f823-111">To stop recording requests:</span></span>  

*   <span data-ttu-id="7f823-112">Selecione **parar gravação de log de rede** ![ parar de gravar ][ImageRecordOnIcon] o log de rede no painel de **rede** .</span><span class="sxs-lookup"><span data-stu-id="7f823-112">Select **Stop recording network log** ![Stop recording network log][ImageRecordOnIcon] on the **Network** panel.</span></span>  <span data-ttu-id="7f823-113">Ele fica cinza para indicar que o DevTools não está mais gravando solicitações.</span><span class="sxs-lookup"><span data-stu-id="7f823-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
*   <span data-ttu-id="7f823-114">Pressione `Control` + `E` \ (Windows \) ou `Command` + `E` \ (MacOS \) enquanto o painel de **rede** estiver em foco.</span><span class="sxs-lookup"><span data-stu-id="7f823-114">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="7f823-115">Solicitações de limpeza</span><span class="sxs-lookup"><span data-stu-id="7f823-115">Clear requests</span></span>   

<span data-ttu-id="7f823-116">Selecione **limpar** ![ limpar ][ImageClearIcon] no painel rede para limpar todas as solicitações da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="7f823-116">Select **Clear** ![Clear][ImageClearIcon] on the Network panel to clear all requests from the Requests table.</span></span>  

> ##### <span data-ttu-id="7f823-117">Figura 2</span><span class="sxs-lookup"><span data-stu-id="7f823-117">Figure 2</span></span>  
> <span data-ttu-id="7f823-118">O botão limpar</span><span class="sxs-lookup"><span data-stu-id="7f823-118">The Clear button</span></span>  
> ![O botão limpar][ImageClearButton]  

### <span data-ttu-id="7f823-120">Salvar solicitações nas cargas de página</span><span class="sxs-lookup"><span data-stu-id="7f823-120">Save requests across page loads</span></span>   

<span data-ttu-id="7f823-121">Para salvar as solicitações nas cargas da página, marque a caixa de seleção **preservar registro** no painel rede.</span><span class="sxs-lookup"><span data-stu-id="7f823-121">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="7f823-122">O DevTools salva todas as solicitações até você desabilitar o **preserve log**.</span><span class="sxs-lookup"><span data-stu-id="7f823-122">DevTools saves all requests until you disable **Preserve log**.</span></span>  

> ##### <span data-ttu-id="7f823-123">Figura 3</span><span class="sxs-lookup"><span data-stu-id="7f823-123">Figure 3</span></span>  
> <span data-ttu-id="7f823-124">A caixa de seleção preservar registro</span><span class="sxs-lookup"><span data-stu-id="7f823-124">The Preserve Log checkbox</span></span>  
> ![A caixa de seleção preservar registro][ImagePreserveLogCheckBox]  

### <span data-ttu-id="7f823-126">Capturar capturas de tela durante o carregamento da página</span><span class="sxs-lookup"><span data-stu-id="7f823-126">Capture screenshots during page load</span></span>   

<span data-ttu-id="7f823-127">Capture capturas de tela para analisar o que os usuários vêem enquanto esperam pela página para carregar.</span><span class="sxs-lookup"><span data-stu-id="7f823-127">Capture screenshots to analyze what users see as they wait for your page to load.</span></span>  

<span data-ttu-id="7f823-128">Para habilitar capturas de tela, selecione **configurações de rede** e escolha **capturar capturas de tela** no painel **rede** .</span><span class="sxs-lookup"><span data-stu-id="7f823-128">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="7f823-129">Recarregue a página enquanto o painel de **rede** estiver em foco para capturar capturas de tela.</span><span class="sxs-lookup"><span data-stu-id="7f823-129">Reload the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="7f823-130">Após a captura de uma captura de tela, você interage com ela das seguintes maneiras.</span><span class="sxs-lookup"><span data-stu-id="7f823-130">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="7f823-131">Passe o mouse sobre uma captura de tela para ver o ponto em que a captura de tela foi capturada.</span><span class="sxs-lookup"><span data-stu-id="7f823-131">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="7f823-132">Uma linha amarela é exibida no painel **visão geral** .</span><span class="sxs-lookup"><span data-stu-id="7f823-132">A yellow line appears on the **Overview** pane.</span></span>  
*   <span data-ttu-id="7f823-133">Selecione a miniatura de uma tela para filtrar todas as solicitações ocorridas após a captura da captura de tela.</span><span class="sxs-lookup"><span data-stu-id="7f823-133">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="7f823-134">Clique duas vezes em uma miniatura para ampliá-la.</span><span class="sxs-lookup"><span data-stu-id="7f823-134">Double-click a thumbnail to zoom in on it.</span></span>  

> ##### <span data-ttu-id="7f823-135">Figura 4</span><span class="sxs-lookup"><span data-stu-id="7f823-135">Figure 4</span></span>  
> <span data-ttu-id="7f823-136">Passar o mouse sobre uma captura de tela</span><span class="sxs-lookup"><span data-stu-id="7f823-136">Hovering over a screenshot</span></span>  
> ![Passar o mouse sobre uma captura de tela][ImageScreenshotHover]  

<!--  ### Replay XHR request   -->

<!--  To replay an XHR request, right-click the request in the Requests table and select **Replay XHR**.  -->

<!--  
> ##### Old Figure 5  
> Selecting Replay XHR  
> ![Selecting Replay XHR][ImageReplayXHR]  
-->  

## <span data-ttu-id="7f823-138">Alterar comportamento de carregamento</span><span class="sxs-lookup"><span data-stu-id="7f823-138">Change loading behavior</span></span>  

### <span data-ttu-id="7f823-139">Emular um visitante da primeira vez desabilitando o cache do navegador</span><span class="sxs-lookup"><span data-stu-id="7f823-139">Emulate a first-time visitor by disabling the browser cache</span></span>   

<span data-ttu-id="7f823-140">Para emular como um usuário da primeira vez experimenta o seu site, marque a caixa de seleção **desabilitar cache** .</span><span class="sxs-lookup"><span data-stu-id="7f823-140">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="7f823-141">DevTools desabilita o cache do navegador.</span><span class="sxs-lookup"><span data-stu-id="7f823-141">DevTools disables the browser cache.</span></span>  <span data-ttu-id="7f823-142">Isso emula com mais precisão uma experiência do usuário pela primeira vez, pois as solicitações são servidas do cache do navegador em visitas repetidas.</span><span class="sxs-lookup"><span data-stu-id="7f823-142">This more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

> ##### <span data-ttu-id="7f823-143">Figura 5</span><span class="sxs-lookup"><span data-stu-id="7f823-143">Figure 5</span></span>  
> <span data-ttu-id="7f823-144">A caixa de seleção desabilitar cache</span><span class="sxs-lookup"><span data-stu-id="7f823-144">The Disable Cache checkbox</span></span>  
> <span data-ttu-id="7f823-145">! [A caixa de seleção desativar cache] [ImageDisableCacheCheckBox]</span><span class="sxs-lookup"><span data-stu-id="7f823-145">![The Disable Cache checkbox][ImageDisableCacheCheckBox]</span></span>  

#### <span data-ttu-id="7f823-146">Desabilitar o cache do navegador da gaveta de condições da rede</span><span class="sxs-lookup"><span data-stu-id="7f823-146">Disable the browser cache from the Network Conditions drawer</span></span>   

<span data-ttu-id="7f823-147">Se você quiser desabilitar o cache enquanto trabalha em outros painéis do DevTools, use a gaveta de condições de rede.</span><span class="sxs-lookup"><span data-stu-id="7f823-147">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="7f823-148">Abra a gaveta de **condições de rede** .</span><span class="sxs-lookup"><span data-stu-id="7f823-148">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="7f823-149">Marque ou desmarque a caixa de seleção **desativar cache** .</span><span class="sxs-lookup"><span data-stu-id="7f823-149">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="7f823-150">Limpar manualmente o cache do navegador</span><span class="sxs-lookup"><span data-stu-id="7f823-150">Manually clear the browser cache</span></span>   

<span data-ttu-id="7f823-151">Para limpar manualmente o cache do navegador a qualquer momento, clique com o botão direito do mouse em qualquer lugar na tabela solicitações e selecione **Limpar cache do navegador**.</span><span class="sxs-lookup"><span data-stu-id="7f823-151">To manually clear the browser cache at any time, right-click anywhere in the Requests table and select **Clear Browser Cache**.</span></span>  

> ##### <span data-ttu-id="7f823-152">Figura 6</span><span class="sxs-lookup"><span data-stu-id="7f823-152">Figure 6</span></span>  
> <span data-ttu-id="7f823-153">Selecionando limpar cache do navegador</span><span class="sxs-lookup"><span data-stu-id="7f823-153">Selecting Clear Browser Cache</span></span>  
> <span data-ttu-id="7f823-154">! [Selecionando limpar cache do navegador] [ImageClearBrowserCache]</span><span class="sxs-lookup"><span data-stu-id="7f823-154">![Selecting Clear Browser Cache][ImageClearBrowserCache]</span></span>  

### <span data-ttu-id="7f823-155">Emular offline</span><span class="sxs-lookup"><span data-stu-id="7f823-155">Emulate offline</span></span>   

<span data-ttu-id="7f823-156">Uma nova classe de aplicativos Web, chamada [Web Apps progressivos][DevtoolsProgressiveWebApps], funciona offline com a ajuda do **serviço de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="7f823-156">A new class of web apps, called [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="7f823-157">Pode ser útil simular rapidamente um dispositivo que não tem conexão de dados quando você está criando esse tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7f823-157">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="7f823-158">Selecione o menu suspenso **online** , procure em **predefinições**e selecione **offline** para simular uma experiência de rede completamente offline.</span><span class="sxs-lookup"><span data-stu-id="7f823-158">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate a completely offline network experience.</span></span>  

> ##### <span data-ttu-id="7f823-159">Figura 7</span><span class="sxs-lookup"><span data-stu-id="7f823-159">Figure 7</span></span>  
> <span data-ttu-id="7f823-160">O menu suspenso offline</span><span class="sxs-lookup"><span data-stu-id="7f823-160">The Offline dropdown menu</span></span>  
> <span data-ttu-id="7f823-161">! [Menu suspenso offline] [ImageOfflineDropdown]</span><span class="sxs-lookup"><span data-stu-id="7f823-161">![The Offline dropdown menu][ImageOfflineDropdown]</span></span>  

### <span data-ttu-id="7f823-162">Emular conexões de rede lentas</span><span class="sxs-lookup"><span data-stu-id="7f823-162">Emulate slow network connections</span></span>   

<span data-ttu-id="7f823-163">Emular a conexão 3G, rápida 3G e outras velocidades de conexão a partir do menu suspenso **online** .</span><span class="sxs-lookup"><span data-stu-id="7f823-163">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

> ##### <span data-ttu-id="7f823-164">Figura 8</span><span class="sxs-lookup"><span data-stu-id="7f823-164">Figure 8</span></span>  
> <span data-ttu-id="7f823-165">O menu suspenso limitação</span><span class="sxs-lookup"><span data-stu-id="7f823-165">The Throttling dropdown menu</span></span>  
> <span data-ttu-id="7f823-166">! [O menu suspenso limitação] [ImageNetworkThrottlingMenu]</span><span class="sxs-lookup"><span data-stu-id="7f823-166">![The Throttling dropdown menu][ImageNetworkThrottlingMenu]</span></span>  

<span data-ttu-id="7f823-167">Você pode escolher entre uma variedade de predefinições, como 3G ou Fast 3G lento.</span><span class="sxs-lookup"><span data-stu-id="7f823-167">You may select from a variety of presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="7f823-168">Você também pode adicionar suas próprias predefinições personalizadas abrindo o menu de limitação e selecionando **Custom**  >  **Adicionar**personalizado.</span><span class="sxs-lookup"><span data-stu-id="7f823-168">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="7f823-169">O DevTools exibe um ícone de aviso ao lado da guia **rede** para lembrá-lo de que a limitação está habilitada.</span><span class="sxs-lookup"><span data-stu-id="7f823-169">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="7f823-170">Emular conexões de rede lentas da gaveta de condições da rede</span><span class="sxs-lookup"><span data-stu-id="7f823-170">Emulate slow network connections from the Network Conditions drawer</span></span>   

<span data-ttu-id="7f823-171">Se você quiser controlar a conexão de rede enquanto trabalha em outros painéis do DevTools, use a gaveta de condições de rede.</span><span class="sxs-lookup"><span data-stu-id="7f823-171">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="7f823-172">Abra a gaveta de **condições de rede** .</span><span class="sxs-lookup"><span data-stu-id="7f823-172">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="7f823-173">Selecione a velocidade de conexão desejada no menu **limitação** .</span><span class="sxs-lookup"><span data-stu-id="7f823-173">Select your desired connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="7f823-174">Limpar manualmente os cookies do navegador</span><span class="sxs-lookup"><span data-stu-id="7f823-174">Manually clear browser cookies</span></span>   

<span data-ttu-id="7f823-175">Para limpar manualmente os cookies do navegador a qualquer momento, clique com o botão direito do mouse em qualquer lugar na tabela solicitações e selecione **Limpar cookies do navegador**.</span><span class="sxs-lookup"><span data-stu-id="7f823-175">To manually clear browser cookies at any time, right-click anywhere in the Requests table and select **Clear Browser Cookies**.</span></span>  

> ##### <span data-ttu-id="7f823-176">Figura 9</span><span class="sxs-lookup"><span data-stu-id="7f823-176">Figure 9</span></span>  
> <span data-ttu-id="7f823-177">Selecionando limpar cookies do navegador</span><span class="sxs-lookup"><span data-stu-id="7f823-177">Selecting Clear Browser Cookies</span></span>  
> <span data-ttu-id="7f823-178">! [Selecionando limpar cookies do navegador] [ImageClearBrowserCookies]</span><span class="sxs-lookup"><span data-stu-id="7f823-178">![Selecting Clear Browser Cookies][ImageClearBrowserCookies]</span></span>  

### <span data-ttu-id="7f823-179">Substituir o agente do usuário</span><span class="sxs-lookup"><span data-stu-id="7f823-179">Override the user agent</span></span>   

<span data-ttu-id="7f823-180">Para substituir manualmente o agente do usuário:</span><span class="sxs-lookup"><span data-stu-id="7f823-180">To manually override the user agent:</span></span>  

1.  <span data-ttu-id="7f823-181">Abra a gaveta de **condições de rede** .</span><span class="sxs-lookup"><span data-stu-id="7f823-181">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="7f823-182">Desmarque **selecionar automaticamente**.</span><span class="sxs-lookup"><span data-stu-id="7f823-182">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="7f823-183">Escolha uma opção de agente do usuário no menu ou insira uma opção personalizada na caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="7f823-183">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="7f823-184">Filtrar solicitações</span><span class="sxs-lookup"><span data-stu-id="7f823-184">Filter requests</span></span>   

### <span data-ttu-id="7f823-185">Filtrar solicitações por propriedades</span><span class="sxs-lookup"><span data-stu-id="7f823-185">Filter requests by properties</span></span>   

<span data-ttu-id="7f823-186">Use a caixa de texto **Filtrar** para filtrar solicitações por propriedades, como o domínio ou o tamanho da solicitação.</span><span class="sxs-lookup"><span data-stu-id="7f823-186">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="7f823-187">Se você não vir a caixa de texto, o painel filtros provavelmente está oculto.</span><span class="sxs-lookup"><span data-stu-id="7f823-187">If you do not see the text box, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="7f823-188">Consulte [ocultar o painel filtros](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="7f823-188">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

> ##### <span data-ttu-id="7f823-189">Figura 10</span><span class="sxs-lookup"><span data-stu-id="7f823-189">Figure 10</span></span>  
> <span data-ttu-id="7f823-190">A caixa de texto filtros</span><span class="sxs-lookup"><span data-stu-id="7f823-190">The Filters text box</span></span>  
> <span data-ttu-id="7f823-191">! [A caixa de texto filtros] [ImageFilterTextBox]</span><span class="sxs-lookup"><span data-stu-id="7f823-191">![The Filters text box][ImageFilterTextBox]</span></span>  

<span data-ttu-id="7f823-192">Você pode usar várias propriedades simultaneamente, separando cada propriedade com um espaço.</span><span class="sxs-lookup"><span data-stu-id="7f823-192">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="7f823-193">Por exemplo, `mime-type:image/png larger-than:1K` exibe todas as PNGs maiores do que um kilobyte.</span><span class="sxs-lookup"><span data-stu-id="7f823-193">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than one kilobyte.</span></span>  <span data-ttu-id="7f823-194">Esses filtros de várias propriedades são equivalentes às `AND` operações.</span><span class="sxs-lookup"><span data-stu-id="7f823-194">These multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="7f823-195">Não há suporte para operações no momento.</span><span class="sxs-lookup"><span data-stu-id="7f823-195">operations are currently not supported.</span></span>  

<span data-ttu-id="7f823-196">A lista completa de propriedades com suporte.</span><span class="sxs-lookup"><span data-stu-id="7f823-196">The complete list of supported properties.</span></span>  

| <span data-ttu-id="7f823-197">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7f823-197">Property</span></span> | <span data-ttu-id="7f823-198">Detalhes</span><span class="sxs-lookup"><span data-stu-id="7f823-198">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="7f823-199">Exiba somente os recursos do domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="7f823-199">Only display resources from the specified domain.</span></span>  <span data-ttu-id="7f823-200">Você pode usar um caractere curinga \ ( `*` \) para incluir vários domínios.</span><span class="sxs-lookup"><span data-stu-id="7f823-200">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="7f823-201">Por exemplo, `*.com` exibe os recursos de todos os nomes de domínio terminam em `.com` .</span><span class="sxs-lookup"><span data-stu-id="7f823-201">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="7f823-202">DevTools preenche o menu suspenso de preenchimento automático com todos os domínios encontrados.</span><span class="sxs-lookup"><span data-stu-id="7f823-202">DevTools populates the autocomplete dropdown menu with all of the domains it has encountered.</span></span> |  
| `has-response-header` | <span data-ttu-id="7f823-203">Mostrar os recursos que contêm o cabeçalho de resposta HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="7f823-203">Show the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="7f823-204">DevTools preenche a lista suspensa preenchimento automático com todos os cabeçalhos de resposta detectados.</span><span class="sxs-lookup"><span data-stu-id="7f823-204">DevTools populates the autocomplete dropdown with all of the response headers that it has encountered.</span></span> |  
| `is` | <span data-ttu-id="7f823-205">Use `is:running` para localizar `WebSocket` recursos.</span><span class="sxs-lookup"><span data-stu-id="7f823-205">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="7f823-206">Mostrar recursos maiores do que o tamanho especificado, em bytes.</span><span class="sxs-lookup"><span data-stu-id="7f823-206">Show resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="7f823-207">Definir um valor `1000` é equivalente a definir um valor de `1k` .</span><span class="sxs-lookup"><span data-stu-id="7f823-207">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="7f823-208">Mostrar recursos que foram recuperados em um tipo de método HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="7f823-208">Show resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="7f823-209">DevTools preenche a lista suspensa com todos os métodos HTTP que ele encontrou.</span><span class="sxs-lookup"><span data-stu-id="7f823-209">DevTools populates the dropdown with all of the HTTP methods it has encountered.</span></span> |  
| `mime-type` | <span data-ttu-id="7f823-210">Mostrar recursos de um tipo MIME especificado.</span><span class="sxs-lookup"><span data-stu-id="7f823-210">Show resources of a specified MIME type.</span></span>  <span data-ttu-id="7f823-211">DevTools preenche a lista suspensa com todos os tipos de MIME encontrados.</span><span class="sxs-lookup"><span data-stu-id="7f823-211">DevTools populates the dropdown with all MIME types it has encountered.</span></span> |  
| `mixed-content` | <span data-ttu-id="7f823-212">Mostrar todos os recursos de conteúdo mistos \ ( `mixed-content:all` \) ou apenas aqueles que são exibidos no momento \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="7f823-212">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="7f823-213">Mostrar recursos recuperados por HTTP \ ( `scheme:http` \) ou HTTPS protegido \ ( `scheme:https` \) protegido.</span><span class="sxs-lookup"><span data-stu-id="7f823-213">Show resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="7f823-214">Mostrar os recursos que têm um `Set-Cookie` cabeçalho com um `Domain` atributo que corresponde ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="7f823-214">Show the resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="7f823-215">DevTools preenche o preenchimento automático com todos os domínios de cookies que ele encontrou.</span><span class="sxs-lookup"><span data-stu-id="7f823-215">DevTools populates the autocomplete with all of the cookie domains that it has encountered.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="7f823-216">Mostrar os recursos que têm um `Set-Cookie` cabeçalho com um nome que corresponde ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="7f823-216">Show the resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="7f823-217">DevTools preenche o preenchimento automático com todos os nomes de cookies que ele encontrou.</span><span class="sxs-lookup"><span data-stu-id="7f823-217">DevTools populates the autocomplete with all of the cookie names that it has encountered.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="7f823-218">Mostrar os recursos que têm um `Set-Cookie` cabeçalho com um valor que corresponde ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="7f823-218">Show the resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="7f823-219">DevTools preenche o preenchimento automático com todos os valores de cookies que ele encontrou.</span><span class="sxs-lookup"><span data-stu-id="7f823-219">DevTools populates the autocomplete with all of the cookie values that it has encountered.</span></span> |  
| `status-code` | <span data-ttu-id="7f823-220">Mostre apenas os recursos para os quais o código de status HTTP corresponde ao código especificado.</span><span class="sxs-lookup"><span data-stu-id="7f823-220">Show only the resources for which the HTTP status code matches the specified code.</span></span>  <span data-ttu-id="7f823-221">DevTools preenche o menu suspenso preenchimento automático com todos os códigos de status encontrados.</span><span class="sxs-lookup"><span data-stu-id="7f823-221">DevTools populates the autocomplete dropdown menu with all of the status codes it has encountered.</span></span> |  

### <span data-ttu-id="7f823-222">Filtrar solicitações por tipo</span><span class="sxs-lookup"><span data-stu-id="7f823-222">Filter requests by type</span></span>   

<span data-ttu-id="7f823-223">Para filtrar solicitações por tipo de solicitação, selecione o **XHR**, **js**, **CSS**, **img**, **mídia**, **fonte**, **Doc**, **WS** \ (WebSocket \), **manifesto**ou **outros** \ (qualquer outro tipo não listado aqui \) botões no painel de rede.</span><span class="sxs-lookup"><span data-stu-id="7f823-223">To filter requests by request type, select the **XHR**, **JS**, **CSS**, **Img**, **Media**, **Font**, **Doc**, **WS** \(WebSocket\), **Manifest**, or **Other** \(any other type not listed here\) buttons on the Network panel.</span></span>  

<span data-ttu-id="7f823-224">Se você não vir esses botões, o painel filtros provavelmente ficará oculto.</span><span class="sxs-lookup"><span data-stu-id="7f823-224">If you do not see these buttons, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="7f823-225">Consulte [ocultar o painel filtros](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="7f823-225">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="7f823-226">Para habilitar vários filtros de tipo simultaneamente, segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e, em seguida, selecione.</span><span class="sxs-lookup"><span data-stu-id="7f823-226">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span></span>  

> ##### <span data-ttu-id="7f823-227">Figura 11</span><span class="sxs-lookup"><span data-stu-id="7f823-227">Figure 11</span></span>  
> <span data-ttu-id="7f823-228">Usar os filtros de tipo para exibir os recursos de documento, CSS e JS</span><span class="sxs-lookup"><span data-stu-id="7f823-228">Using the Type filters to display JS, CSS, and Document resources</span></span>  
> <span data-ttu-id="7f823-229">! [Usando os filtros de tipo para exibir os recursos JS, CSS e de documento] [ImageMultiTypeFilter]</span><span class="sxs-lookup"><span data-stu-id="7f823-229">![Using the Type filters to display JS, CSS, and Document resources][ImageMultiTypeFilter]</span></span>  

### <span data-ttu-id="7f823-230">Filtrar solicitações por tempo</span><span class="sxs-lookup"><span data-stu-id="7f823-230">Filter requests by time</span></span>   

<span data-ttu-id="7f823-231">Selecione e arraste para a esquerda ou direita no painel Visão geral para exibir apenas as solicitações que estavam ativas durante esse período de tempo.</span><span class="sxs-lookup"><span data-stu-id="7f823-231">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="7f823-232">O filtro é inclusivo.</span><span class="sxs-lookup"><span data-stu-id="7f823-232">The filter is inclusive.</span></span>  <span data-ttu-id="7f823-233">Todas as solicitações ativas durante o tempo realçado são mostradas.</span><span class="sxs-lookup"><span data-stu-id="7f823-233">Any request that was active during the highlighted time is shown.</span></span>  

> ##### <span data-ttu-id="7f823-234">Figura 12</span><span class="sxs-lookup"><span data-stu-id="7f823-234">Figure 12</span></span>  
> <span data-ttu-id="7f823-235">Filtragem de todas as solicitações que estavam inativas em torno de 300ms</span><span class="sxs-lookup"><span data-stu-id="7f823-235">Filtering out any requests that were inactive around 300ms</span></span>  
> <span data-ttu-id="7f823-236">! [Filtragem de todas as solicitações que estavam inativas em torno de 300ms] [ImageOverviewFilter]</span><span class="sxs-lookup"><span data-stu-id="7f823-236">![Filtering out any requests that were inactive around 300ms][ImageOverviewFilter]</span></span>  

### <span data-ttu-id="7f823-237">Ocultar URLs de dados</span><span class="sxs-lookup"><span data-stu-id="7f823-237">Hide data URLs</span></span>  

<span data-ttu-id="7f823-238">As [URLs de dados][MDNHTTPDataURIs] são pequenos arquivos incorporados a outros documentos.</span><span class="sxs-lookup"><span data-stu-id="7f823-238">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="7f823-239">Qualquer solicitação que você vê na tabela solicitações que começa com `data:` é uma URL de dados.</span><span class="sxs-lookup"><span data-stu-id="7f823-239">Any request that you see in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="7f823-240">Marque a caixa de seleção **ocultar URLs de dados** para ocultar essas solicitações.</span><span class="sxs-lookup"><span data-stu-id="7f823-240">Check the **Hide data URLs** checkbox to hide these requests.</span></span>  

> ##### <span data-ttu-id="7f823-241">Figura 13</span><span class="sxs-lookup"><span data-stu-id="7f823-241">Figure 13</span></span>  
> <span data-ttu-id="7f823-242">A caixa de seleção Ocultar URLs de dados</span><span class="sxs-lookup"><span data-stu-id="7f823-242">The Hide Data URLs checkbox</span></span>  
> <span data-ttu-id="7f823-243">! [A caixa de seleção Ocultar URLs de dados] [ImageHideDataURLsCheckBox]</span><span class="sxs-lookup"><span data-stu-id="7f823-243">![The Hide Data URLs checkbox][ImageHideDataURLsCheckBox]</span></span>  

## <span data-ttu-id="7f823-244">Solicitações de classificação</span><span class="sxs-lookup"><span data-stu-id="7f823-244">Sort requests</span></span>  

<span data-ttu-id="7f823-245">Por padrão, as solicitações na tabela solicitações são classificadas por hora de início, mas você pode classificar a tabela usando outros critérios.</span><span class="sxs-lookup"><span data-stu-id="7f823-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="7f823-246">Classificar por coluna</span><span class="sxs-lookup"><span data-stu-id="7f823-246">Sort by column</span></span>   

<span data-ttu-id="7f823-247">Selecione o cabeçalho de qualquer coluna nas solicitações para classificar solicitações por essa coluna.</span><span class="sxs-lookup"><span data-stu-id="7f823-247">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="7f823-248">Fase classificar por atividade</span><span class="sxs-lookup"><span data-stu-id="7f823-248">Sort by activity phase</span></span>   

<span data-ttu-id="7f823-249">Para alterar a forma como a cascata classifica solicitações, clique com o botão direito do mouse no cabeçalho da tabela solicitações, passe o mouse sobre a **cascata**e selecione uma das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="7f823-249">To change how the Waterfall sorts requests, right-click the header of the Requests table, hover over **Waterfall**, and select one of the following options.</span></span>  

*   <span data-ttu-id="7f823-250">**Hora de início**.</span><span class="sxs-lookup"><span data-stu-id="7f823-250">**Start Time**.</span></span>  <span data-ttu-id="7f823-251">A primeira solicitação iniciada está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="7f823-251">The first request that was initiated is at the top.</span></span>  
*   <span data-ttu-id="7f823-252">**Tempo de resposta**.</span><span class="sxs-lookup"><span data-stu-id="7f823-252">**Response Time**.</span></span>  <span data-ttu-id="7f823-253">A primeira solicitação iniciada para download está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="7f823-253">The first request that started downloading is at the top.</span></span>  
*   <span data-ttu-id="7f823-254">**Hora de término**.</span><span class="sxs-lookup"><span data-stu-id="7f823-254">**End Time**.</span></span>  <span data-ttu-id="7f823-255">A primeira solicitação que terminou está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="7f823-255">The first request that finished is at the top.</span></span>  
*   <span data-ttu-id="7f823-256">**Duração total**.</span><span class="sxs-lookup"><span data-stu-id="7f823-256">**Total Duration**.</span></span>  <span data-ttu-id="7f823-257">A solicitação com a configuração de conexão mais curta e solicitação/resposta está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="7f823-257">The request with the shortest connection setup and request / response is at the top.</span></span>  
*   <span data-ttu-id="7f823-258">**Latência**.</span><span class="sxs-lookup"><span data-stu-id="7f823-258">**Latency**.</span></span>  <span data-ttu-id="7f823-259">A solicitação que aguardou o tempo mais curto para uma resposta está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="7f823-259">The request that waited the shortest time for a response is at the top.</span></span>  

<span data-ttu-id="7f823-260">Essas descrições pressupõem que cada opção respectiva seja classificada da mais curta para a mais longa.</span><span class="sxs-lookup"><span data-stu-id="7f823-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="7f823-261">A seleção do cabeçalho da coluna em **cascata** inverte a ordem.</span><span class="sxs-lookup"><span data-stu-id="7f823-261">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

> ##### <span data-ttu-id="7f823-262">Figura 14</span><span class="sxs-lookup"><span data-stu-id="7f823-262">Figure 14</span></span>  
> <span data-ttu-id="7f823-263">Classificar a cascata com duração total \ (a parte mais clara de cada barra é o tempo gasto aguardando e a parte mais escura é o tempo gasto para baixar bytes \)</span><span class="sxs-lookup"><span data-stu-id="7f823-263">Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
> <span data-ttu-id="7f823-264">! [Classificar a cascata por duração total] [ImageWaterfallTotalDuration]</span><span class="sxs-lookup"><span data-stu-id="7f823-264">![Sorting the Waterfall by total duration][ImageWaterfallTotalDuration]</span></span>  

## <span data-ttu-id="7f823-265">Analisar solicitações</span><span class="sxs-lookup"><span data-stu-id="7f823-265">Analyze requests</span></span>   

<span data-ttu-id="7f823-266">Desde que o DevTools esteja aberto, ele registra todas as solicitações no painel de rede.</span><span class="sxs-lookup"><span data-stu-id="7f823-266">So long as DevTools is open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="7f823-267">Use o painel rede para analisar solicitações.</span><span class="sxs-lookup"><span data-stu-id="7f823-267">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="7f823-268">Exibir um log de solicitações</span><span class="sxs-lookup"><span data-stu-id="7f823-268">View a log of requests</span></span>   

<span data-ttu-id="7f823-269">Use a tabela requests para exibir um log de todas as solicitações feitas enquanto o DevTools está aberto.</span><span class="sxs-lookup"><span data-stu-id="7f823-269">Use the Requests table to view a log of all requests made while DevTools has been open.</span></span>  <span data-ttu-id="7f823-270">Selecionar ou passar o mouse nas solicitações revela mais informações sobre cada item.</span><span class="sxs-lookup"><span data-stu-id="7f823-270">Selecting or hovering over requests reveals more information about each item.</span></span>  

> ##### <span data-ttu-id="7f823-271">Figura 15</span><span class="sxs-lookup"><span data-stu-id="7f823-271">Figure 15</span></span>  
> <span data-ttu-id="7f823-272">A tabela solicitações</span><span class="sxs-lookup"><span data-stu-id="7f823-272">The Requests table</span></span>  
> <span data-ttu-id="7f823-273">! [A tabela de solicitações] [ImageRequestsTable]</span><span class="sxs-lookup"><span data-stu-id="7f823-273">![The Requests table][ImageRequestsTable]</span></span>  

<span data-ttu-id="7f823-274">A tabela solicitações exibe as seguintes colunas por padrão:</span><span class="sxs-lookup"><span data-stu-id="7f823-274">The Requests table displays the following columns by default:</span></span>  

*   <span data-ttu-id="7f823-275">**Nome**.</span><span class="sxs-lookup"><span data-stu-id="7f823-275">**Name**.</span></span>  <span data-ttu-id="7f823-276">O nome do recurso ou um identificador para o recurso.</span><span class="sxs-lookup"><span data-stu-id="7f823-276">The filename of, or an identifier for, the resource.</span></span>  
*   <span data-ttu-id="7f823-277">**Status**.</span><span class="sxs-lookup"><span data-stu-id="7f823-277">**Status**.</span></span>  <span data-ttu-id="7f823-278">O código de status HTTP.</span><span class="sxs-lookup"><span data-stu-id="7f823-278">The HTTP status code.</span></span>  
*   <span data-ttu-id="7f823-279">**Tipo**.</span><span class="sxs-lookup"><span data-stu-id="7f823-279">**Type**.</span></span>  <span data-ttu-id="7f823-280">O tipo MIME do recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="7f823-280">The MIME type of the requested resource.</span></span>  
*   <span data-ttu-id="7f823-281">**Iniciador**.</span><span class="sxs-lookup"><span data-stu-id="7f823-281">**Initiator**.</span></span>  <span data-ttu-id="7f823-282">Os seguintes objetos ou processos iniciam solicitações:</span><span class="sxs-lookup"><span data-stu-id="7f823-282">The following objects or processes initiate requests:</span></span>  
    *   <span data-ttu-id="7f823-283">**Analisador**.</span><span class="sxs-lookup"><span data-stu-id="7f823-283">**Parser**.</span></span>  <span data-ttu-id="7f823-284">O analisador HTML para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7f823-284">The HTML parser for Microsoft Edge.</span></span>  
    *   <span data-ttu-id="7f823-285">**Redirecionar**.</span><span class="sxs-lookup"><span data-stu-id="7f823-285">**Redirect**.</span></span>  <span data-ttu-id="7f823-286">Um redirecionamento HTTP.</span><span class="sxs-lookup"><span data-stu-id="7f823-286">An HTTP redirect.</span></span>  
    *   <span data-ttu-id="7f823-287">**Script**.</span><span class="sxs-lookup"><span data-stu-id="7f823-287">**Script**.</span></span>  <span data-ttu-id="7f823-288">Uma função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7f823-288">A JavaScript function.</span></span>  
    *   <span data-ttu-id="7f823-289">**Outros**.</span><span class="sxs-lookup"><span data-stu-id="7f823-289">**Other**.</span></span>  <span data-ttu-id="7f823-290">Algum outro processo ou ação, como navegar para uma página por meio de um link ou inserir uma URL na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="7f823-290">Some other process or action, such as navigating to a page via a link or entering a URL in the address bar.</span></span>  
*   <span data-ttu-id="7f823-291">**Tamanho**.</span><span class="sxs-lookup"><span data-stu-id="7f823-291">**Size**.</span></span>  <span data-ttu-id="7f823-292">O tamanho combinado dos cabeçalhos de resposta mais o corpo da resposta, conforme entregue pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="7f823-292">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
*   <span data-ttu-id="7f823-293">**Tempo**.</span><span class="sxs-lookup"><span data-stu-id="7f823-293">**Time**.</span></span>  <span data-ttu-id="7f823-294">A duração total, desde o início da solicitação até o recebimento do byte final na resposta.</span><span class="sxs-lookup"><span data-stu-id="7f823-294">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
*   <span data-ttu-id="7f823-295">[**Cascata**](#view-the-timing-of-requests-in-relation-to-one-another).</span><span class="sxs-lookup"><span data-stu-id="7f823-295">[**Waterfall**](#view-the-timing-of-requests-in-relation-to-one-another).</span></span>  <span data-ttu-id="7f823-296">Uma divisão Visual da atividade para cada solicitação.</span><span class="sxs-lookup"><span data-stu-id="7f823-296">A visual breakdown of the activity for each request.</span></span>  

#### <span data-ttu-id="7f823-297">Adicionar ou remover colunas</span><span class="sxs-lookup"><span data-stu-id="7f823-297">Add or remove columns</span></span>   

<span data-ttu-id="7f823-298">Clique com o botão direito do mouse no cabeçalho da tabela solicitações e selecione uma opção para ocultá-la ou mostrá-la.</span><span class="sxs-lookup"><span data-stu-id="7f823-298">Right-click the header of the Requests table and select an option to hide or show it.</span></span>  <span data-ttu-id="7f823-299">As opções atualmente exibidas têm marcas de opção ao lado de cada item.</span><span class="sxs-lookup"><span data-stu-id="7f823-299">Currently displayed options have checkmarks next to each item.</span></span>  

> ##### <span data-ttu-id="7f823-300">Figura 16</span><span class="sxs-lookup"><span data-stu-id="7f823-300">Figure 16</span></span>  
> <span data-ttu-id="7f823-301">Adicionar uma coluna à tabela solicitações</span><span class="sxs-lookup"><span data-stu-id="7f823-301">Adding a column to the Requests table</span></span>  
> <span data-ttu-id="7f823-302">! [Adicionando uma coluna à tabela solicitações] [ImageRequestsTableAddColumn]</span><span class="sxs-lookup"><span data-stu-id="7f823-302">![Adding a column to the Requests table][ImageRequestsTableAddColumn]</span></span>  

#### <span data-ttu-id="7f823-303">Adicionar colunas personalizadas</span><span class="sxs-lookup"><span data-stu-id="7f823-303">Add custom columns</span></span>   

<span data-ttu-id="7f823-304">Para adicionar uma coluna personalizada à tabela solicitações, clique com o botão direito do mouse no cabeçalho da tabela solicitações e selecione **cabeçalhos de resposta**  >  **gerenciar colunas de cabeçalho**.</span><span class="sxs-lookup"><span data-stu-id="7f823-304">To add a custom column to the Requests table, right-click the header of the Requests table and select **Response Headers** > **Manage Header Columns**.</span></span>  

> ##### <span data-ttu-id="7f823-305">Figura 17</span><span class="sxs-lookup"><span data-stu-id="7f823-305">Figure 17</span></span>  
> <span data-ttu-id="7f823-306">Adicionando uma coluna personalizada à tabela solicitações</span><span class="sxs-lookup"><span data-stu-id="7f823-306">Adding a custom column to the Requests table</span></span>  
> <span data-ttu-id="7f823-307">! [Adicionando uma coluna personalizada à tabela de solicitações] [ImageRequestsTableCustomColumn]</span><span class="sxs-lookup"><span data-stu-id="7f823-307">![Adding a custom column to the Requests table][ImageRequestsTableCustomColumn]</span></span>  

### <span data-ttu-id="7f823-308">Exibir o intervalo de solicitações em relação umas as outras</span><span class="sxs-lookup"><span data-stu-id="7f823-308">View the timing of requests in relation to one another</span></span>   

<span data-ttu-id="7f823-309">Use a cascata para ver o intervalo de solicitações em relação umas as outras.</span><span class="sxs-lookup"><span data-stu-id="7f823-309">Use the Waterfall to view the timing of requests in relation to one another.</span></span>  
<span data-ttu-id="7f823-310">Por padrão, a cascata é organizada pela hora de início das solicitações.</span><span class="sxs-lookup"><span data-stu-id="7f823-310">By default, the Waterfall is organized by the start time of the requests.</span></span>  
<span data-ttu-id="7f823-311">Portanto, as solicitações mais distantes do lado esquerdo são mais antigas do que aquelas mais distantes do lado direito.</span><span class="sxs-lookup"><span data-stu-id="7f823-311">So, requests that are farther to the left started earlier than those that are farther to the right.</span></span>  

<span data-ttu-id="7f823-312">Consulte a [fase classificar por atividade](#sort-by-activity-phase) para ver as diferentes maneiras de classificar a cascata.</span><span class="sxs-lookup"><span data-stu-id="7f823-312">See [Sort by activity phase](#sort-by-activity-phase) to see the different ways that you may sort the Waterfall.</span></span>  

> ##### <span data-ttu-id="7f823-313">Figura 18</span><span class="sxs-lookup"><span data-stu-id="7f823-313">Figure 18</span></span>  
> <span data-ttu-id="7f823-314">A coluna de cascata do painel solicitações</span><span class="sxs-lookup"><span data-stu-id="7f823-314">The Waterfall column of the Requests pane</span></span>  
> <span data-ttu-id="7f823-315">! [A coluna em cascata do painel solicitações] [ImageRequestsTableWaterfallColumn]</span><span class="sxs-lookup"><span data-stu-id="7f823-315">![The Waterfall column of the Requests pane][ImageRequestsTableWaterfallColumn]</span></span>  

<!-- ### Analyze the frames of a WebSocket Connection   -->

<!--To view the frames of a WebSocket connection:  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-click the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
> ##### Old Figure 20  
> The Frames tab  
> ![The Frames tab][ImageFrames]  
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

### <span data-ttu-id="7f823-316">Exibir uma visualização de um corpo de resposta</span><span class="sxs-lookup"><span data-stu-id="7f823-316">View a preview of a response body</span></span>   

<span data-ttu-id="7f823-317">Para exibir uma visualização do corpo de uma resposta:</span><span class="sxs-lookup"><span data-stu-id="7f823-317">To view a preview of a response body:</span></span>  

1.  <span data-ttu-id="7f823-318">Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="7f823-318">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="7f823-319">Selecione a guia **Visualizar** .</span><span class="sxs-lookup"><span data-stu-id="7f823-319">Select the **Preview** tab.</span></span>  

<span data-ttu-id="7f823-320">Esta guia é principalmente útil para exibir imagens.</span><span class="sxs-lookup"><span data-stu-id="7f823-320">This tab is mostly useful for viewing images.</span></span>  

> ##### <span data-ttu-id="7f823-321">Figura 19</span><span class="sxs-lookup"><span data-stu-id="7f823-321">Figure 19</span></span>  
> <span data-ttu-id="7f823-322">A guia Visualização</span><span class="sxs-lookup"><span data-stu-id="7f823-322">The Preview tab</span></span>  
> <span data-ttu-id="7f823-323">! [A guia Visualização] [ImagePreview]</span><span class="sxs-lookup"><span data-stu-id="7f823-323">![The Preview tab][ImagePreview]</span></span>  

### <span data-ttu-id="7f823-324">Exibir um corpo de resposta</span><span class="sxs-lookup"><span data-stu-id="7f823-324">View a response body</span></span>   

<span data-ttu-id="7f823-325">Para exibir o corpo da resposta a uma solicitação:</span><span class="sxs-lookup"><span data-stu-id="7f823-325">To view the response body to a request:</span></span>  

1.  <span data-ttu-id="7f823-326">Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="7f823-326">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="7f823-327">Selecione a guia **resposta** .</span><span class="sxs-lookup"><span data-stu-id="7f823-327">Select the **Response** tab.</span></span>  

> ##### <span data-ttu-id="7f823-328">Figura 20</span><span class="sxs-lookup"><span data-stu-id="7f823-328">Figure 20</span></span>  
> <span data-ttu-id="7f823-329">A guia resposta</span><span class="sxs-lookup"><span data-stu-id="7f823-329">The Response tab</span></span>  
> <span data-ttu-id="7f823-330">! [A guia resposta] [ImageResponse]</span><span class="sxs-lookup"><span data-stu-id="7f823-330">![The Response tab][ImageResponse]</span></span>  

### <span data-ttu-id="7f823-331">Exibir cabeçalhos HTTP</span><span class="sxs-lookup"><span data-stu-id="7f823-331">View HTTP headers</span></span>   

<span data-ttu-id="7f823-332">Para ver os dados do cabeçalho HTTP sobre uma solicitação:</span><span class="sxs-lookup"><span data-stu-id="7f823-332">To view HTTP header data about a request:</span></span>  

1.  <span data-ttu-id="7f823-333">Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="7f823-333">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="7f823-334">Selecione a guia **cabeçalhos** .</span><span class="sxs-lookup"><span data-stu-id="7f823-334">Select the **Headers** tab.</span></span>  

> ##### <span data-ttu-id="7f823-335">Figura 21</span><span class="sxs-lookup"><span data-stu-id="7f823-335">Figure 21</span></span>  
> <span data-ttu-id="7f823-336">A guia cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="7f823-336">The Headers tab</span></span>  
> <span data-ttu-id="7f823-337">! [A guia cabeçalhos] [ImageHeaders]</span><span class="sxs-lookup"><span data-stu-id="7f823-337">![The Headers tab][ImageHeaders]</span></span>  

#### <span data-ttu-id="7f823-338">Exibir fonte de cabeçalho HTTP</span><span class="sxs-lookup"><span data-stu-id="7f823-338">View HTTP header source</span></span>   

<span data-ttu-id="7f823-339">Por padrão, a guia cabeçalhos mostra os nomes dos cabeçalhos em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="7f823-339">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="7f823-340">Para exibir os nomes dos cabeçalhos HTTP na ordem em que foram recebidos:</span><span class="sxs-lookup"><span data-stu-id="7f823-340">To view the HTTP header names in the order they were received:</span></span>  

1.  <span data-ttu-id="7f823-341">Abra a guia **cabeçalhos** para a solicitação que lhe interessa.</span><span class="sxs-lookup"><span data-stu-id="7f823-341">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="7f823-342">Consulte [exibir cabeçalhos HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="7f823-342">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="7f823-343">Selecione **Exibir fonte**, ao lado da seção cabeçalho da **solicitação** ou **cabeçalho de resposta** .</span><span class="sxs-lookup"><span data-stu-id="7f823-343">Select **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="7f823-344">Exibir parâmetros da cadeia de caracteres de consulta</span><span class="sxs-lookup"><span data-stu-id="7f823-344">View query string parameters</span></span>   

<span data-ttu-id="7f823-345">Para exibir os parâmetros da cadeia de caracteres de consulta de uma URL em um formato legível por pessoas:</span><span class="sxs-lookup"><span data-stu-id="7f823-345">To view the query string parameters of a URL in a human-readable format:</span></span>  

1.  <span data-ttu-id="7f823-346">Abra a guia **cabeçalhos** para a solicitação que lhe interessa.</span><span class="sxs-lookup"><span data-stu-id="7f823-346">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="7f823-347">Consulte [exibir cabeçalhos HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="7f823-347">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="7f823-348">Vá para a seção **parâmetros da cadeia de caracteres de consulta** .</span><span class="sxs-lookup"><span data-stu-id="7f823-348">Go to the **Query String Parameters** section.</span></span>  

> ##### <span data-ttu-id="7f823-349">Figura 22</span><span class="sxs-lookup"><span data-stu-id="7f823-349">Figure 22</span></span>  
> <span data-ttu-id="7f823-350">A seção parâmetros da cadeia de consulta</span><span class="sxs-lookup"><span data-stu-id="7f823-350">The Query String Parameters section</span></span>  
> <span data-ttu-id="7f823-351">! [Seção parâmetros da cadeia de consulta] [ImageQueryStringParameters]</span><span class="sxs-lookup"><span data-stu-id="7f823-351">![The Query String Parameters section][ImageQueryStringParameters]</span></span>  

#### <span data-ttu-id="7f823-352">Exibir origem dos parâmetros da cadeia de consulta</span><span class="sxs-lookup"><span data-stu-id="7f823-352">View query string parameters source</span></span>   

<span data-ttu-id="7f823-353">Para exibir a origem do parâmetro da cadeia de caracteres de consulta de uma solicitação:</span><span class="sxs-lookup"><span data-stu-id="7f823-353">To view the query string parameter source of a request:</span></span>  

1.  <span data-ttu-id="7f823-354">Vá para a seção parâmetros da cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="7f823-354">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="7f823-355">Consulte [Exibir parâmetros da cadeia de consulta](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="7f823-355">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="7f823-356">Selecione **Exibir código-fonte**.</span><span class="sxs-lookup"><span data-stu-id="7f823-356">Select **view source**.</span></span>  

#### <span data-ttu-id="7f823-357">Exibir parâmetros da cadeia de consulta codificada por URL</span><span class="sxs-lookup"><span data-stu-id="7f823-357">View URL-encoded query string parameters</span></span>   

<span data-ttu-id="7f823-358">Para exibir os parâmetros da cadeia de caracteres de consulta em um formato legível pelo homem, mas com codificações preservadas:</span><span class="sxs-lookup"><span data-stu-id="7f823-358">To view query string parameters in a human-readable format, but with encodings preserved:</span></span>  

1.  <span data-ttu-id="7f823-359">Vá para a seção parâmetros da cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="7f823-359">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="7f823-360">Consulte [Exibir parâmetros da cadeia de consulta](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="7f823-360">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="7f823-361">Selecione **exibir URL codificada**.</span><span class="sxs-lookup"><span data-stu-id="7f823-361">Select **view URL encoded**.</span></span>  

### <span data-ttu-id="7f823-362">Exibir cookies</span><span class="sxs-lookup"><span data-stu-id="7f823-362">View cookies</span></span>   

<span data-ttu-id="7f823-363">Para exibir os cookies enviados no cabeçalho HTTP de uma solicitação:</span><span class="sxs-lookup"><span data-stu-id="7f823-363">To view the cookies sent in the HTTP header of a request:</span></span>  

1.  <span data-ttu-id="7f823-364">Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="7f823-364">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="7f823-365">Selecione a guia **cookies** .</span><span class="sxs-lookup"><span data-stu-id="7f823-365">Select the **Cookies** tab.</span></span>  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

> ##### <span data-ttu-id="7f823-366">Figura 23</span><span class="sxs-lookup"><span data-stu-id="7f823-366">Figure 23</span></span>  
> <span data-ttu-id="7f823-367">A guia cookies</span><span class="sxs-lookup"><span data-stu-id="7f823-367">The Cookies tab</span></span>  
> <span data-ttu-id="7f823-368">! [A guia cookies] [ImageCookies]</span><span class="sxs-lookup"><span data-stu-id="7f823-368">![The Cookies tab][ImageCookies]</span></span>  

### <span data-ttu-id="7f823-369">Exibir a divisão de tempo de uma solicitação</span><span class="sxs-lookup"><span data-stu-id="7f823-369">View the timing breakdown of a request</span></span>   

<span data-ttu-id="7f823-370">Para exibir a divisão de tempo de uma solicitação:</span><span class="sxs-lookup"><span data-stu-id="7f823-370">To view the timing breakdown of a request:</span></span>  

1.  <span data-ttu-id="7f823-371">Selecione a URL da solicitação, na coluna **nome** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="7f823-371">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="7f823-372">Selecione a guia **intervalo** .</span><span class="sxs-lookup"><span data-stu-id="7f823-372">Select the **Timing** tab.</span></span>  

<span data-ttu-id="7f823-373">Consulte [Visualizar um detalhamento de intervalos](#preview-a-timing-breakdown) para obter uma maneira mais rápida de acessar esses dados.</span><span class="sxs-lookup"><span data-stu-id="7f823-373">See [Preview a timing breakdown](#preview-a-timing-breakdown) for a faster way to access this data.</span></span>  

<span data-ttu-id="7f823-374">Veja as [fases da divisão de intervalo explicadas](#timing-breakdown-phases-explained) para obter mais informações sobre cada uma das fases que você pode ver na guia intervalo.</span><span class="sxs-lookup"><span data-stu-id="7f823-374">See [Timing breakdown phases explained](#timing-breakdown-phases-explained) for more information about each of the phases that you may see in the Timing tab.</span></span>  

> ##### <span data-ttu-id="7f823-375">Figura 24</span><span class="sxs-lookup"><span data-stu-id="7f823-375">Figure 24</span></span>  
> <span data-ttu-id="7f823-376">A guia intervalo</span><span class="sxs-lookup"><span data-stu-id="7f823-376">The Timing tab</span></span>  
> <span data-ttu-id="7f823-377">! [A guia intervalo] [ImageTiming]</span><span class="sxs-lookup"><span data-stu-id="7f823-377">![The Timing tab][ImageTiming]</span></span>  

<span data-ttu-id="7f823-378">Mais informações sobre cada uma das fases.</span><span class="sxs-lookup"><span data-stu-id="7f823-378">More information about each of the phases.</span></span>  

<span data-ttu-id="7f823-379">Consulte [Exibir detalhamento de intervalo](#view-the-timing-breakdown-of-a-request) para obter outra maneira de acessar este modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="7f823-379">See [View timing breakdown](#view-the-timing-breakdown-of-a-request) for another way to access this view.</span></span>  

#### <span data-ttu-id="7f823-380">Visualizar uma divisão de intervalo</span><span class="sxs-lookup"><span data-stu-id="7f823-380">Preview a timing breakdown</span></span>   

<span data-ttu-id="7f823-381">Para exibir uma visualização da divisão de tempo de uma solicitação, passe o mouse sobre a entrada da solicitação na coluna **cascata** da tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="7f823-381">To view a preview of the timing breakdown of a request, hover over the entry for the request in the **Waterfall** column of the Requests table.</span></span>  

<span data-ttu-id="7f823-382">Consulte [Exibir o detalhamento de intervalos de uma solicitação](#view-the-timing-breakdown-of-a-request) para acessar esses dados que não exigem o foco.</span><span class="sxs-lookup"><span data-stu-id="7f823-382">See [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request) for a way to access this data that does not require hovering.</span></span>  

> ##### <span data-ttu-id="7f823-383">Figura 25</span><span class="sxs-lookup"><span data-stu-id="7f823-383">Figure 25</span></span>  
> <span data-ttu-id="7f823-384">Visualizando a divisão de tempo de uma solicitação</span><span class="sxs-lookup"><span data-stu-id="7f823-384">Previewing the timing breakdown of a request</span></span>  
> <span data-ttu-id="7f823-385">! [Visualização da divisão de tempo de uma solicitação] [ImageWaterfallHover]</span><span class="sxs-lookup"><span data-stu-id="7f823-385">![Previewing the timing breakdown of a request][ImageWaterfallHover]</span></span>  

#### <span data-ttu-id="7f823-386">Fases da divisão de tempo explicadas</span><span class="sxs-lookup"><span data-stu-id="7f823-386">Timing breakdown phases explained</span></span>   

<span data-ttu-id="7f823-387">Mais informações sobre cada uma das fases que você pode ver na guia intervalo:</span><span class="sxs-lookup"><span data-stu-id="7f823-387">More information about each of the phases you may see in the Timing tab:</span></span>  

*   <span data-ttu-id="7f823-388">Em **fila**.</span><span class="sxs-lookup"><span data-stu-id="7f823-388">**Queueing**.</span></span>  <span data-ttu-id="7f823-389">O navegador solicita uma fila quando:</span><span class="sxs-lookup"><span data-stu-id="7f823-389">The browser queues requests when:</span></span>  
    *   <span data-ttu-id="7f823-390">Há solicitações de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="7f823-390">There are higher priority requests.</span></span>  
    *   <span data-ttu-id="7f823-391">Já existem seis conexões TCP abertas para essa origem, que é o limite.</span><span class="sxs-lookup"><span data-stu-id="7f823-391">There are already six TCP connections open for this origin, which is the limit.</span></span>  <span data-ttu-id="7f823-392">Aplica-se somente a HTTP/1.0 e HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="7f823-392">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
    *   <span data-ttu-id="7f823-393">O navegador está alocando um espaço brevemente no cache de disco.</span><span class="sxs-lookup"><span data-stu-id="7f823-393">The browser is briefly allocating space in the disk cache.</span></span>  
*   <span data-ttu-id="7f823-394">**Parado**.</span><span class="sxs-lookup"><span data-stu-id="7f823-394">**Stalled**.</span></span>  <span data-ttu-id="7f823-395">A solicitação pode estar parada para qualquer um dos motivos descritos no **enfileiramento**.</span><span class="sxs-lookup"><span data-stu-id="7f823-395">The request could be stalled for any of the reasons described in **Queueing**.</span></span>  
*   <span data-ttu-id="7f823-396">**Pesquisa de DNS**.</span><span class="sxs-lookup"><span data-stu-id="7f823-396">**DNS Lookup**.</span></span>  <span data-ttu-id="7f823-397">O navegador está resolvendo o endereço IP da solicitação.</span><span class="sxs-lookup"><span data-stu-id="7f823-397">The browser is resolving the IP address for the request.</span></span>  
*   <span data-ttu-id="7f823-398">**Negociação de proxy**.</span><span class="sxs-lookup"><span data-stu-id="7f823-398">**Proxy negotiation**.</span></span>  <span data-ttu-id="7f823-399">O navegador está negociando a solicitação com um [servidor proxy][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="7f823-399">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
*   <span data-ttu-id="7f823-400">**Solicitação enviada**.</span><span class="sxs-lookup"><span data-stu-id="7f823-400">**Request sent**.</span></span>  <span data-ttu-id="7f823-401">A solicitação está sendo enviada.</span><span class="sxs-lookup"><span data-stu-id="7f823-401">The request is being sent.</span></span>  
*   <span data-ttu-id="7f823-402">**Preparação do serviço**.</span><span class="sxs-lookup"><span data-stu-id="7f823-402">**ServiceWorker Preparation**.</span></span>  <span data-ttu-id="7f823-403">O navegador está iniciando o trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="7f823-403">The browser is starting up the service worker.</span></span>  
*   <span data-ttu-id="7f823-404">**Solicitação ao serviço de serviço**.</span><span class="sxs-lookup"><span data-stu-id="7f823-404">**Request to ServiceWorker**.</span></span>  <span data-ttu-id="7f823-405">A solicitação está sendo enviada para o trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="7f823-405">The request is being sent to the service worker.</span></span>  
*   <span data-ttu-id="7f823-406">**Aguardando \ (TTFB \)**.</span><span class="sxs-lookup"><span data-stu-id="7f823-406">**Waiting \(TTFB\)**.</span></span>  <span data-ttu-id="7f823-407">O navegador está aguardando o primeiro byte de uma resposta.</span><span class="sxs-lookup"><span data-stu-id="7f823-407">The browser is waiting for the first byte of a response.</span></span>  
  <span data-ttu-id="7f823-408">TTFB significa tempo até o primeiro byte.</span><span class="sxs-lookup"><span data-stu-id="7f823-408">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="7f823-409">Esse tempo inclui 1 viagem de ida e volta da latência e o tempo que o servidor levou para preparar a resposta.</span><span class="sxs-lookup"><span data-stu-id="7f823-409">This timing includes 1 round trip of latency and the time the server took to prepare the response.</span></span>  
*   <span data-ttu-id="7f823-410">**Download de conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="7f823-410">**Content Download**.</span></span>  <span data-ttu-id="7f823-411">O navegador está recebendo a resposta.</span><span class="sxs-lookup"><span data-stu-id="7f823-411">The browser is receiving the response.</span></span>  
*   <span data-ttu-id="7f823-412">**Recebendo Push**.</span><span class="sxs-lookup"><span data-stu-id="7f823-412">**Receiving Push**.</span></span>  <span data-ttu-id="7f823-413">O navegador está recebendo dados para esta resposta via Push HTTP/2 Server Push.</span><span class="sxs-lookup"><span data-stu-id="7f823-413">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
*   <span data-ttu-id="7f823-414">**Leitura por push**.</span><span class="sxs-lookup"><span data-stu-id="7f823-414">**Reading Push**.</span></span>  <span data-ttu-id="7f823-415">O navegador está lendo os dados locais anteriormente recebidos.</span><span class="sxs-lookup"><span data-stu-id="7f823-415">The browser is reading the local data previously received.</span></span>  

### <span data-ttu-id="7f823-416">Exibir iniciadores e dependências</span><span class="sxs-lookup"><span data-stu-id="7f823-416">View initiators and dependencies</span></span>   

<span data-ttu-id="7f823-417">Para ver os iniciadores e as dependências de uma solicitação, mantenha o `Shift` cursor sobre a solicitação na tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="7f823-417">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="7f823-418">Cores DevTools: os iniciadores são exibidos em verde e as dependências são mostradas em vermelho.</span><span class="sxs-lookup"><span data-stu-id="7f823-418">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

> ##### <span data-ttu-id="7f823-419">Figura 26</span><span class="sxs-lookup"><span data-stu-id="7f823-419">Figure 26</span></span>  
> <span data-ttu-id="7f823-420">Exibindo os iniciadores e as dependências de uma solicitação</span><span class="sxs-lookup"><span data-stu-id="7f823-420">Viewing the initiators and dependencies of a request</span></span>  
> <span data-ttu-id="7f823-421">! [Exibindo os iniciadores e as dependências de uma solicitação] [ImageRequestInitiatorsDependencies]</span><span class="sxs-lookup"><span data-stu-id="7f823-421">![Viewing the initiators and dependencies of a request][ImageRequestInitiatorsDependencies]</span></span>  

<span data-ttu-id="7f823-422">Quando a tabela de solicitações é ordenada cronologicamente, a primeira solicitação verde acima da que você está passando é o iniciador da dependência.</span><span class="sxs-lookup"><span data-stu-id="7f823-422">When the Requests table is ordered chronologically, the first green request above the one you are hovering is the initiator of the dependency.</span></span>  <span data-ttu-id="7f823-423">Se outra solicitação verde aparecer acima disso, essa solicitação mais alta será o iniciador do iniciador.</span><span class="sxs-lookup"><span data-stu-id="7f823-423">If another green request appears above that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="7f823-424">E assim em diante.</span><span class="sxs-lookup"><span data-stu-id="7f823-424">And so on.</span></span>  

### <span data-ttu-id="7f823-425">Exibir eventos de carga</span><span class="sxs-lookup"><span data-stu-id="7f823-425">View load events</span></span>   

<span data-ttu-id="7f823-426">DevTools exibe a temporização dos `DOMContentLoaded` eventos e de `load` vários locais no painel de rede.</span><span class="sxs-lookup"><span data-stu-id="7f823-426">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="7f823-427">O `DOMContentLoaded` evento está em azul colorido e o `load` evento está em vermelho.</span><span class="sxs-lookup"><span data-stu-id="7f823-427">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

> ##### <span data-ttu-id="7f823-428">Figura 27</span><span class="sxs-lookup"><span data-stu-id="7f823-428">Figure 27</span></span>  
> <span data-ttu-id="7f823-429">Os locais dos `DOMContentLoaded` eventos e do `load` painel de rede</span><span class="sxs-lookup"><span data-stu-id="7f823-429">The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
> <span data-ttu-id="7f823-430">! [Os locais dos eventos DOMContentLoaded e Load no painel de rede] [ImageNetworkPanelDOMContentLoadedLoadEvents]</span><span class="sxs-lookup"><span data-stu-id="7f823-430">![The locations of the DOMContentLoaded and load events on the Network panel][ImageNetworkPanelDOMContentLoadedLoadEvents]</span></span>  

### <span data-ttu-id="7f823-431">Ver o número total de solicitações</span><span class="sxs-lookup"><span data-stu-id="7f823-431">View the total number of requests</span></span>   

<span data-ttu-id="7f823-432">O número total de solicitações está listado no painel Resumo, na parte inferior do painel de rede.</span><span class="sxs-lookup"><span data-stu-id="7f823-432">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="7f823-433">Esse número controla apenas as solicitações que foram registradas desde que o DevTools foi aberto.</span><span class="sxs-lookup"><span data-stu-id="7f823-433">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="7f823-434">Se ocorrerem outras solicitações antes da abertura do DevTools, essas solicitações não serão contadas.</span><span class="sxs-lookup"><span data-stu-id="7f823-434">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

> ##### <span data-ttu-id="7f823-435">Figura 28</span><span class="sxs-lookup"><span data-stu-id="7f823-435">Figure 28</span></span>  
> <span data-ttu-id="7f823-436">O número total de solicitações desde que o DevTools foi aberto</span><span class="sxs-lookup"><span data-stu-id="7f823-436">The total number of requests since DevTools was opened</span></span>  
> <span data-ttu-id="7f823-437">! [O número total de solicitações desde que o DevTools foi aberto] [ImageTotalRequests]</span><span class="sxs-lookup"><span data-stu-id="7f823-437">![The total number of requests since DevTools was opened][ImageTotalRequests]</span></span>  

### <span data-ttu-id="7f823-438">Ver o tamanho total do download</span><span class="sxs-lookup"><span data-stu-id="7f823-438">View the total download size</span></span>   

<span data-ttu-id="7f823-439">O tamanho total do download de solicitações é listado no painel Resumo, na parte inferior do painel de rede.</span><span class="sxs-lookup"><span data-stu-id="7f823-439">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="7f823-440">Esse número controla apenas as solicitações que foram registradas desde que o DevTools foi aberto.</span><span class="sxs-lookup"><span data-stu-id="7f823-440">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="7f823-441">Se ocorrerem outras solicitações antes da abertura do DevTools, essas solicitações não serão contadas.</span><span class="sxs-lookup"><span data-stu-id="7f823-441">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

> ##### <span data-ttu-id="7f823-442">Figura 29</span><span class="sxs-lookup"><span data-stu-id="7f823-442">Figure 29</span></span>  
> <span data-ttu-id="7f823-443">O tamanho total do download de solicitações</span><span class="sxs-lookup"><span data-stu-id="7f823-443">The total download size of requests</span></span>  
> <span data-ttu-id="7f823-444">! [O tamanho total do download de solicitações] [ImageTotalSize]</span><span class="sxs-lookup"><span data-stu-id="7f823-444">![The total download size of requests][ImageTotalSize]</span></span>  

<span data-ttu-id="7f823-445">Consulte [Exibir o tamanho descompactado de um recurso](#view-the-uncompressed-size-of-a-resource) para ver a quantidade de recursos grandes após o navegador descompactar cada item.</span><span class="sxs-lookup"><span data-stu-id="7f823-445">See [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource) to see how large resources are after the browser uncompresses each item.</span></span>  

### <span data-ttu-id="7f823-446">Exibir o rastreamento de pilha que causou uma solicitação</span><span class="sxs-lookup"><span data-stu-id="7f823-446">View the stack trace that caused a request</span></span>   

<span data-ttu-id="7f823-447">Depois que uma instrução JavaScript solicita um recurso, passe o mouse sobre a coluna do **iniciador** para exibir o rastreamento de pilha que leva à solicitação.</span><span class="sxs-lookup"><span data-stu-id="7f823-447">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

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

> ##### <span data-ttu-id="7f823-448">Figura 30</span><span class="sxs-lookup"><span data-stu-id="7f823-448">Figure 30</span></span>  
> <span data-ttu-id="7f823-449">O rastreamento de pilha que leva a uma solicitação de recurso</span><span class="sxs-lookup"><span data-stu-id="7f823-449">The stack trace leading up to a resource request</span></span>  
> <span data-ttu-id="7f823-450">! [O rastreamento de pilha que leva à solicitação de recurso] [ImageInitiatorStack]</span><span class="sxs-lookup"><span data-stu-id="7f823-450">![The stack trace leading up to a resource request][ImageInitiatorStack]</span></span>  

### <span data-ttu-id="7f823-451">Exibir o tamanho descompactado de um recurso</span><span class="sxs-lookup"><span data-stu-id="7f823-451">View the uncompressed size of a resource</span></span>   

<span data-ttu-id="7f823-452">Marque a caixa de seleção **usar linhas de solicitação grandes** e examine o valor inferior da coluna **tamanho** .</span><span class="sxs-lookup"><span data-stu-id="7f823-452">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

> ##### <span data-ttu-id="7f823-453">Figura 31</span><span class="sxs-lookup"><span data-stu-id="7f823-453">Figure 31</span></span>  
> <span data-ttu-id="7f823-454">Um exemplo de recursos não compactados \ (o tamanho compactado do `jquery-3.3.1.min.js` arquivo que foi enviado pela rede foi `29.9 KB` , enquanto o tamanho não compactado era `84.9 KB` \)</span><span class="sxs-lookup"><span data-stu-id="7f823-454">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
> <span data-ttu-id="7f823-455">! [Um exemplo de recursos não compactados] [ImageUncompressedResources]</span><span class="sxs-lookup"><span data-stu-id="7f823-455">![An example of uncompressed resources][ImageUncompressedResources]</span></span>  

## <span data-ttu-id="7f823-456">Exportar dados de solicitações</span><span class="sxs-lookup"><span data-stu-id="7f823-456">Export requests data</span></span>   

### <span data-ttu-id="7f823-457">Salvar todas as solicitações de rede em um arquivo HAR</span><span class="sxs-lookup"><span data-stu-id="7f823-457">Save all network requests to a HAR file</span></span>   

<span data-ttu-id="7f823-458">Para salvar todas as solicitações de rede em um arquivo HAR:</span><span class="sxs-lookup"><span data-stu-id="7f823-458">To save all network requests to a HAR file:</span></span>  

1.  <span data-ttu-id="7f823-459">Clique com o botão direito do mouse em qualquer solicitação na tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="7f823-459">Right-click any request in the Requests table.</span></span>  
1.  <span data-ttu-id="7f823-460">Selecione **salvar como Har com conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="7f823-460">Select **Save as HAR with Content**.</span></span>  <span data-ttu-id="7f823-461">DevTools salva todas as solicitações ocorridas desde que você abriu o DevTools para o arquivo HAR.</span><span class="sxs-lookup"><span data-stu-id="7f823-461">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="7f823-462">Não há nenhuma maneira de filtrar solicitações ou salvar uma única solicitação.</span><span class="sxs-lookup"><span data-stu-id="7f823-462">There is no way to filter requests, or to save just a single request.</span></span>  

<span data-ttu-id="7f823-463">Depois de salvar um arquivo HAR, você poderá importá-lo novamente no DevTools para análise.</span><span class="sxs-lookup"><span data-stu-id="7f823-463">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="7f823-464">Basta arrastar e soltar o arquivo HAR na tabela solicitações.</span><span class="sxs-lookup"><span data-stu-id="7f823-464">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

> ##### <span data-ttu-id="7f823-465">Figura 32</span><span class="sxs-lookup"><span data-stu-id="7f823-465">Figure 32</span></span>  
> <span data-ttu-id="7f823-466">Selecionando salvar como HAR com conteúdo</span><span class="sxs-lookup"><span data-stu-id="7f823-466">Selecting Save as HAR with Content</span></span>  
> <span data-ttu-id="7f823-467">! [Selecionando salvar como HAR com conteúdo] [ImageSaveAsHAR]</span><span class="sxs-lookup"><span data-stu-id="7f823-467">![Selecting Save as HAR with Content][ImageSaveAsHAR]</span></span>  

### <span data-ttu-id="7f823-468">Copiar uma ou mais solicitações para a área de transferência</span><span class="sxs-lookup"><span data-stu-id="7f823-468">Copy one or more requests to the clipboard</span></span>   

<span data-ttu-id="7f823-469">Na coluna **nome** da tabela solicitações, clique com o botão direito do mouse em uma solicitação, passe o mouse sobre a **cópia**e selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="7f823-469">Under the **Name** column of the Requests table, right-click a request, hover over **Copy**, and select one of the following options:</span></span>  

*   <span data-ttu-id="7f823-470">**Copie o endereço do link**.</span><span class="sxs-lookup"><span data-stu-id="7f823-470">**Copy Link Address**.</span></span>  <span data-ttu-id="7f823-471">Copie a URL da solicitação para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="7f823-471">Copy the URL of the request to the clipboard.</span></span>  
*   <span data-ttu-id="7f823-472">**Copiar resposta**.</span><span class="sxs-lookup"><span data-stu-id="7f823-472">**Copy Response**.</span></span>  <span data-ttu-id="7f823-473">Copie o corpo da resposta para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="7f823-473">Copy the response body to the clipboard.</span></span>  
*   <span data-ttu-id="7f823-474">**Copiar como busca**.</span><span class="sxs-lookup"><span data-stu-id="7f823-474">**Copy as Fetch**.</span></span>  
*   <span data-ttu-id="7f823-475">**Copiar como ondulação**.</span><span class="sxs-lookup"><span data-stu-id="7f823-475">**Copy as cURL**.</span></span>  <span data-ttu-id="7f823-476">Copie a solicitação como um comando de rotação.</span><span class="sxs-lookup"><span data-stu-id="7f823-476">Copy the request as a cURL command.</span></span>  
*   <span data-ttu-id="7f823-477">**Copiar tudo como busca**.</span><span class="sxs-lookup"><span data-stu-id="7f823-477">**Copy All as Fetch**.</span></span>  
*   <span data-ttu-id="7f823-478">**Copiar tudo como ondulado**.</span><span class="sxs-lookup"><span data-stu-id="7f823-478">**Copy All as cURL**.</span></span>  <span data-ttu-id="7f823-479">Copie todas as solicitações como uma cadeia de comandos de ondulação.</span><span class="sxs-lookup"><span data-stu-id="7f823-479">Copy all requests as a chain of cURL commands.</span></span>  
*   <span data-ttu-id="7f823-480">**Copiar tudo como Har**.</span><span class="sxs-lookup"><span data-stu-id="7f823-480">**Copy All as HAR**.</span></span>  <span data-ttu-id="7f823-481">Copie todas as solicitações como dados de HAR.</span><span class="sxs-lookup"><span data-stu-id="7f823-481">Copy all requests as HAR data.</span></span>  

> ##### <span data-ttu-id="7f823-482">Figura 33</span><span class="sxs-lookup"><span data-stu-id="7f823-482">Figure 33</span></span>  
> <span data-ttu-id="7f823-483">Selecionando a resposta de cópia</span><span class="sxs-lookup"><span data-stu-id="7f823-483">Selecting Copy Response</span></span>  
> <span data-ttu-id="7f823-484">! [Selecionando resposta de cópia] [ImageCopyResponse]</span><span class="sxs-lookup"><span data-stu-id="7f823-484">![Selecting Copy Response][ImageCopyResponse]</span></span>  

## <span data-ttu-id="7f823-485">Alterar o layout do painel de rede</span><span class="sxs-lookup"><span data-stu-id="7f823-485">Change the layout of the Network panel</span></span>  

<span data-ttu-id="7f823-486">Você pode expandir ou recolher seções da interface do usuário do painel de rede para concentrar informações importantes.</span><span class="sxs-lookup"><span data-stu-id="7f823-486">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="7f823-487">Ocultar o painel filtros</span><span class="sxs-lookup"><span data-stu-id="7f823-487">Hide the Filters pane</span></span>   

<span data-ttu-id="7f823-488">Por padrão, o DevTools mostra o **painel filtros**.</span><span class="sxs-lookup"><span data-stu-id="7f823-488">By default, DevTools shows the **Filters pane**.</span></span>  
<span data-ttu-id="7f823-489">Selecione **Filter** ![ filtro ][ImageFilterIcon] de filtro para ocultá-lo.</span><span class="sxs-lookup"><span data-stu-id="7f823-489">Select **Filter** ![Filter][ImageFilterIcon]  to hide it.</span></span>  

> ##### <span data-ttu-id="7f823-490">Figura 34</span><span class="sxs-lookup"><span data-stu-id="7f823-490">Figure 34</span></span>  
> <span data-ttu-id="7f823-491">O botão Ocultar filtros</span><span class="sxs-lookup"><span data-stu-id="7f823-491">The Hide Filters button</span></span>  
> <span data-ttu-id="7f823-492">! [O botão Ocultar filtros] [ImageHideFiltersButton]</span><span class="sxs-lookup"><span data-stu-id="7f823-492">![The Hide Filters button][ImageHideFiltersButton]</span></span>  

### <span data-ttu-id="7f823-493">Usar linhas de solicitação grandes</span><span class="sxs-lookup"><span data-stu-id="7f823-493">Use large request rows</span></span>   

<span data-ttu-id="7f823-494">Use linhas grandes quando quiser mais espaço em branco na tabela solicitações de rede.</span><span class="sxs-lookup"><span data-stu-id="7f823-494">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="7f823-495">Algumas colunas também fornecem um pouco mais de informações ao usar linhas grandes.</span><span class="sxs-lookup"><span data-stu-id="7f823-495">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="7f823-496">Por exemplo, o valor inferior da coluna **tamanho** é o tamanho descompactado de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="7f823-496">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

> ##### <span data-ttu-id="7f823-497">Figura 35</span><span class="sxs-lookup"><span data-stu-id="7f823-497">Figure 35</span></span>  
> <span data-ttu-id="7f823-498">Um exemplo de linhas de solicitação grandes no painel solicitações</span><span class="sxs-lookup"><span data-stu-id="7f823-498">An example of large request rows in the Requests pane</span></span>  
> <span data-ttu-id="7f823-499">! [Um exemplo de linhas de solicitação grandes no painel solicitações] [ImageLargeRequestRows]</span><span class="sxs-lookup"><span data-stu-id="7f823-499">![An example of large request rows in the Requests pane][ImageLargeRequestRows]</span></span>  

<span data-ttu-id="7f823-500">Marque a caixa de seleção **usar linhas de solicitação grandes** para habilitar linhas grandes.</span><span class="sxs-lookup"><span data-stu-id="7f823-500">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

> ##### <span data-ttu-id="7f823-501">Figura 36</span><span class="sxs-lookup"><span data-stu-id="7f823-501">Figure 36</span></span>  
> <span data-ttu-id="7f823-502">A caixa de seleção de linhas de solicitação grandes</span><span class="sxs-lookup"><span data-stu-id="7f823-502">The Large Request Rows checkbox</span></span>  
> <span data-ttu-id="7f823-503">! [A caixa de seleção solicitar linhas grandes] [ImageLargeRequestRowsCheckbox]</span><span class="sxs-lookup"><span data-stu-id="7f823-503">![The Large Request Rows checkbox][ImageLargeRequestRowsCheckbox]</span></span>  

### <span data-ttu-id="7f823-504">Ocultar o painel Visão geral</span><span class="sxs-lookup"><span data-stu-id="7f823-504">Hide the Overview pane</span></span>   

<span data-ttu-id="7f823-505">Por padrão, o DevTools mostra o **painel Visão geral**.</span><span class="sxs-lookup"><span data-stu-id="7f823-505">By default, DevTools shows the **Overview pane**.</span></span>  
<span data-ttu-id="7f823-506">Desmarque a caixa de seleção **Mostrar visão geral** para ocultá-la.</span><span class="sxs-lookup"><span data-stu-id="7f823-506">Deselect the **Show Overview** checkbox to hide it.</span></span>  

> ##### <span data-ttu-id="7f823-507">Figura 37</span><span class="sxs-lookup"><span data-stu-id="7f823-507">Figure 37</span></span>  
> <span data-ttu-id="7f823-508">A caixa de seleção Mostrar visão geral</span><span class="sxs-lookup"><span data-stu-id="7f823-508">The Show Overview checkbox</span></span>  
> <span data-ttu-id="7f823-509">! [A caixa de seleção Mostrar visão geral] [ImageHideOverviewCheckbox]</span><span class="sxs-lookup"><span data-stu-id="7f823-509">![The Show Overview checkbox][ImageHideOverviewCheckbox]</span></span>  

<!-->   -->  

  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-requests-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageHideIcon]: /microsoft-edge/devtools-guide-chromium/media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: /microsoft-edge/devtools-guide-chromium/media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: /microsoft-edge/devtools-guide-chromium/media/record-on-icon.msft.png  

[ImageNetworkPanel]: /microsoft-edge/devtools-guide-chromium/media/network-network-panel.msft.png "Figura 1: painel de rede"  
[ImageClearButton]: /microsoft-edge/devtools-guide-chromium/media/network-network-clear-button.msft.png "Figura 2: o botão limpar"  
[ImagePreserveLogCheckBox]: /microsoft-edge/devtools-guide-chromium/media/network-network-preserve-log.msft.png "Figura 3: caixa de seleção preservar registro"  
[ImageScreenshotHover]: /microsoft-edge/devtools-guide-chromium/media/network-network-screenshot-hover.msft.png "Figura 4: passando o mouse sobre uma captura de tela"  
<!--[ImageReplayXHR]: /microsoft-edge/devtools-guide-chromium/media/network-replay-xhr.msft.png "Old Figure 5: Selecting Replay XHR"  -->  
[ImageDisableCacheCheckBox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Disable-cache-CheckBox.msft.png "Figura 5: a caixa de seleção desativar cache"  
[ImageClearBrowserCache]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Clear-browser-cache.msft.png "Figura 6: selecionando limpar cache do navegador"  
[ImageOfflineDropdown]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-offline-DropDown.msft.png "Figura 7: o menu suspenso offline"  
[ImageNetworkThrottlingMenu]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-throttling-menu.msft.png "Figura 8: o menu de limitação de rede"  
[ImageClearBrowserCookies]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Clear-browser-cookies.msft.png "Figura 9: selecionando limpar cookies do navegador"  
[ImageFilterTextBox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Filters-TextBox.msft.png "Figura 10: a caixa de texto filtros"  
[ImageMultiTypeFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Type-Filters.msft.png "Figura 11: usar os filtros de tipo para exibir os recursos de JS, CSS e documentos"  
[ImageOverviewFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Overview-Filter.msft.png "Figura 12: filtrar todas as solicitações que estavam inativas em torno de 300ms"  
[ImageHideDataURLsCheckBox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Hide-data-URLs.msft.png "Figura 13: caixa de seleção Ocultar URLs de dados"  
[ImageWaterfallTotalDuration]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Waterfall-total-duration.msft.png "Figura 14: classificando a cascata por duração total"  
[ImageRequestsTable]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Table.msft.png "Figura 15: a tabela de solicitações"  
[ImageRequestsTableAddColumn]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Add-Column.msft.png "Figura 16: adicionando uma coluna à tabela de solicitações"  
[ImageRequestsTableCustomColumn]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Add-Custom.msft.png "figura 17: adicionando uma coluna personalizada à tabela de solicitações"  
[ImageRequestsTableWaterfallColumn]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Waterfall.msft.png "Figura 18: a coluna de cascata do painel solicitações"  
[ImagePreview]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Preview.msft.png "Figura 19: a guia Visualizar"  
<!--[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/network-frames.msft.png "Old Figure 20: The Frames tab"  -->  
[ImageResponse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Response.msft.png "Figura 20: a guia resposta"  
[ImageHeaders]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Resources-Headers.msft.png "figura 21: a guia cabeçalhos"  
[ImageQueryStringParameters]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Headers-Query-String-Parameters.msft.png "Figura 22: seção de parâmetros da cadeia de consulta"  
[ImageCookies]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-cookies.msft.png "Figura 23: a guia cookies"  
[ImageTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-timing.msft.png "Figura 24: a guia intervalo"  
[ImageWaterfallHover]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Waterfall-hover.msft.png "figura 25: visualizando a divisão de tempo de uma solicitação"  
[ImageRequestInitiatorsDependencies]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-initiators-Dependencies.msft.png "Figura 26: exibindo os iniciadores e as dependências de uma solicitação"  
[ImageNetworkPanelDOMContentLoadedLoadEvents]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Load-Events.msft.png "Figura 27: os locais dos eventos DOMContentLoaded e Load no painel de rede"  
[ImageTotalRequests]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-total-requests.msft.png "Figura 28: o número total de solicitações desde que o DevTools foi aberto"  
[ImageTotalSize]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-total-download-size.msft.png "figura 29: o tamanho total do download de solicitações"  
[ImageInitiatorStack]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Initiator-Stack.msft.png "figura 30: o rastreamento de pilha que leva até uma solicitação de recurso"  
[ImageUncompressedResources]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-uncompressed-Compare.msft.png "figura 31: um exemplo de recursos não compactados"  
[ImageSaveAsHAR]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Save-Har-Content.msft.png "Figura 32: selecionando salvar como HAR com conteúdo"  
[ImageCopyResponse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Copy-Response.msft.png "figura 33: selecionando cópia de resposta"  
[ImageHideFiltersButton]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-Resources-Hide-Filters-Button.msft.png "Figura 34: o botão Ocultar filtros"  
[ImageLargeRequestRows]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-Large-Request-Rows.msft.png "Figura 35: um exemplo de linhas de solicitação grandes no painel solicitações"  
[ImageLargeRequestRowsCheckbox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-use-Large-Request-Rows-on.msft.png "Figura 36: a caixa de seleção de linhas de solicitação grandes"  
[ImageHideOverviewCheckbox]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-Network-requests-show-Overview-off.msft.png "figura 37: a caixa de seleção Ocultar visão geral"  

<!-- links -->  

[DevtoolsProgressiveWebApps]: /microsoft-edge/devtools-guide-chromium/network/progressive-web-apps "Depurar aplicativos Web progressivos"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URLs de dados | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Servidor proxy-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="7f823-550">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="7f823-550">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7f823-551">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/network/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="7f823-551">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7f823-553">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7f823-553">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
