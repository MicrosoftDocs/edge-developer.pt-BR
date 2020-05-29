---
description: Usar o painel rede para monitorar e criar o perfil de solicitações de recursos de página
title: DevTools-rede
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, rede, tempo de carregamento, http, HTTPS, cache do navegador, HAR
ms.custom: seodec18
ms.openlocfilehash: 0b190f5163f9b7a9f9920877a94577177053e4f6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561396"
---
# <span data-ttu-id="a44b5-104">Rede</span><span class="sxs-lookup"><span data-stu-id="a44b5-104">Network</span></span>

<span data-ttu-id="a44b5-105">Use o painel **rede** para monitorar, inspecionar e criar perfil das solicitações e respostas enviadas pela transmissão.</span><span class="sxs-lookup"><span data-stu-id="a44b5-105">Use the **Network** panel to monitor, inspect and profile the requests and responses sent over the wire.</span></span> <span data-ttu-id="a44b5-106">Com ele, você pode:</span><span class="sxs-lookup"><span data-stu-id="a44b5-106">With it, you can:</span></span>

 - <span data-ttu-id="a44b5-107">[Procurar um registro de todas as solicitações de recursos](#network-summary) feitas pela página</span><span class="sxs-lookup"><span data-stu-id="a44b5-107">[Browse a record of all the resource requests](#network-summary) made by the page</span></span>
 - <span data-ttu-id="a44b5-108">[Meça o tempo de carregamento do seu site](#summary-bar) para novos e devolver usuários</span><span class="sxs-lookup"><span data-stu-id="a44b5-108">[Measure the load time of your site](#summary-bar) for new and returning users</span></span> 
 - <span data-ttu-id="a44b5-109">[Inspecione os cabeçalhos, corpos de mensagens, parâmetros e cookies](#request-details) trocados entre a sua página e a rede</span><span class="sxs-lookup"><span data-stu-id="a44b5-109">[Inspect the headers, message bodies, parameters, and cookies](#request-details) exchanged between your page and the network</span></span>
 - <span data-ttu-id="a44b5-110">[Identifique os eventos de rede que causam afunilamentos](#timings) no tempo de carregamento do seu site</span><span class="sxs-lookup"><span data-stu-id="a44b5-110">[Identify the network events causing bottlenecks](#timings) in the load time of your site</span></span>

![O painel de rede do Microsoft Edge DevTools](./media/network.png)

## <span data-ttu-id="a44b5-112">Resumo da rede</span><span class="sxs-lookup"><span data-stu-id="a44b5-112">Network summary</span></span>

<span data-ttu-id="a44b5-113">Quando você abre o DevTools, a criação de perfil de rede é ativada por padrão.</span><span class="sxs-lookup"><span data-stu-id="a44b5-113">When you open  DevTools, network profiling is turned on by default.</span></span> <span data-ttu-id="a44b5-114">Todo o tráfego de rede da guia ativa do navegador é gravado na lista Resumo da rede, mesmo quando você está trabalhando em um painel DevTools diferente da *rede*.</span><span class="sxs-lookup"><span data-stu-id="a44b5-114">All the network traffic from your active browser tab is recorded in the network summary list, even while you are working in a different  DevTools panel than *Network*.</span></span>

![Indicador de perfil de rede em andamento](./media/network_profile_indicator.png)

### <span data-ttu-id="a44b5-116">Barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="a44b5-116">Toolbar</span></span>

<span data-ttu-id="a44b5-117">A barra de ferramentas fornece controles para perfilar e filtrar a atividade de rede de sua página.</span><span class="sxs-lookup"><span data-stu-id="a44b5-117">The toolbar provides controls for profiling and filtering the network activity of your page.</span></span> 

![Barra de ferramentas perfil de rede](./media/network_toolbar.png)

1. <span data-ttu-id="a44b5-119">**Iniciar/parar sessão de criação de perfil**: por padrão, o profiling de rede está ativado, e o tráfego de rede será registrado na lista do [**perfil de rede**](#network-request-list) .</span><span class="sxs-lookup"><span data-stu-id="a44b5-119">**Start / Stop profiling session**: By default, network profiling is turned on, and network traffic will be logged in the [**Network profiler**](#network-request-list) list.</span></span> <span data-ttu-id="a44b5-120">Você pode desativar a captura de rede com o botão **parar** ( `Ctrl+E` ).</span><span class="sxs-lookup"><span data-stu-id="a44b5-120">You can turn off network capture with the **Stop** (`Ctrl+E`) button.</span></span>

2. <span data-ttu-id="a44b5-121">**Exportar como Har**: você pode salvar a sessão atual de criação de perfil de rede ( `Ctrl+S` ) como um arquivo de arquivo http formatado para JSON [(Har)](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/HAR/Overview.html) .</span><span class="sxs-lookup"><span data-stu-id="a44b5-121">**Export as HAR**: You can save the current network profiling session (`Ctrl+S`) as a JSON-formatted [HTTP Archive (HAR)](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/HAR/Overview.html) file.</span></span> 

3. <span data-ttu-id="a44b5-122">**Filtro de tipo de conteúdo**: filtrar a lista de solicitações de rede por solicitações de conteúdo específicas (*documentos, folhas de estilos, imagens, scripts, mídia, fontes, XHR, outros*).</span><span class="sxs-lookup"><span data-stu-id="a44b5-122">**Content type filter**: Filter the network request list by specific content requests (*Documents, Style sheets, Images, Scripts, Media, Fonts, XHR, Other*).</span></span> <span data-ttu-id="a44b5-123">Por padrão, todos os tipos de conteúdo são mostrados.</span><span class="sxs-lookup"><span data-stu-id="a44b5-123">By default all content types are shown.</span></span>

4. <span data-ttu-id="a44b5-124">**Find**: Filter ( `Ctrl+F` ) a lista de solicitação de rede por nomes de entrada (caminhos de recursos) contendo uma cadeia de pesquisa especificada.</span><span class="sxs-lookup"><span data-stu-id="a44b5-124">**Find**: Filter (`Ctrl+F`) the network request list by entry names (resource paths) containing a specified search string.</span></span>

5. <span data-ttu-id="a44b5-125">**Sempre atualizar do servidor**: a desativação desse botão forçará os recursos da página a carregar da rede, em vez do cache do navegador.</span><span class="sxs-lookup"><span data-stu-id="a44b5-125">**Always refresh from server**: Depressing this button will force page resources to load from the network rather than the browser cache.</span></span> <span data-ttu-id="a44b5-126">Você pode atualizar a página da rede de uma única vez pressionando `Ctrl+F5` .</span><span class="sxs-lookup"><span data-stu-id="a44b5-126">You can refresh the page from  network a single time by pressing `Ctrl+F5`.</span></span>

6. <span data-ttu-id="a44b5-127">**Ignorar o trabalho de serviço para todas as solicitações de rede**: Desabilite seus trabalhadores de serviço cadastrados como proxies de rede.</span><span class="sxs-lookup"><span data-stu-id="a44b5-127">**Bypass Service Worker for all network requests**: Disable your registered service workers as network proxies.</span></span> 

7. <span data-ttu-id="a44b5-128">Botões limpar</span><span class="sxs-lookup"><span data-stu-id="a44b5-128">Clear buttons</span></span>

   - <span data-ttu-id="a44b5-129">**Limpar cache**: Remove todos os recursos armazenados no cache do navegador (e emula uma experiência de primeira hora carregando a página).</span><span class="sxs-lookup"><span data-stu-id="a44b5-129">**Clear cache**: Removes all resources stored in the browser cache (and emulates a first-time experience loading the page).</span></span>
   - <span data-ttu-id="a44b5-130">**Limpar cookies**: Remove todos os cookies para o domínio especificado (e emula uma experiência de primeira vez do site).</span><span class="sxs-lookup"><span data-stu-id="a44b5-130">**Clear cookies**: Removes all cookies for the given domain (and emulates a first-time experience of the site).</span></span>
   - <span data-ttu-id="a44b5-131">**Limpar entradas ao navegar**: o tráfego gravado é limpo na navegação da página.</span><span class="sxs-lookup"><span data-stu-id="a44b5-131">**Clear entries on navigate**: Recorded traffic is cleared upon page navigation.</span></span> <span data-ttu-id="a44b5-132">Isso é ativado por padrão.</span><span class="sxs-lookup"><span data-stu-id="a44b5-132">This is turned on by default.</span></span>
   - <span data-ttu-id="a44b5-133">**Limpar sessão**: limpa todas as entradas de solicitação de rede na lista **Resumo da rede** .</span><span class="sxs-lookup"><span data-stu-id="a44b5-133">**Clear session**: Clears all network request entries from the **Network summary** list.</span></span>

### <span data-ttu-id="a44b5-134">Lista de solicitações de rede</span><span class="sxs-lookup"><span data-stu-id="a44b5-134">Network request list</span></span>

<span data-ttu-id="a44b5-135">Todo o tráfego de rede é gravado em uma lista (até ser limpo após a navegação, desmarcada manualmente ou DevTools são fechadas).</span><span class="sxs-lookup"><span data-stu-id="a44b5-135">All network traffic is recorded to a list (until cleared upon navigation, manually cleared, or  DevTools are closed).</span></span> <span data-ttu-id="a44b5-136">Clicar em qualquer entrada abrirá uma [visão mais detalhada da solicitação](#request-details).</span><span class="sxs-lookup"><span data-stu-id="a44b5-136">Clicking on any entry will open a more [detailed view of the request](#request-details).</span></span>

![Lista de solicitações de rede](./media/network_request_list.png)

<span data-ttu-id="a44b5-138">A lista de solicitações de rede inclui as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="a44b5-138">The network request list includes the following info:</span></span> 

<span data-ttu-id="a44b5-139">Coluna</span><span class="sxs-lookup"><span data-stu-id="a44b5-139">Column</span></span> | <span data-ttu-id="a44b5-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="a44b5-140">Description</span></span> 
:------------ | :------------- 
**<span data-ttu-id="a44b5-141">Name</span><span class="sxs-lookup"><span data-stu-id="a44b5-141">Name</span></span>** | <span data-ttu-id="a44b5-142">Nome e caminho da URL da solicitação</span><span class="sxs-lookup"><span data-stu-id="a44b5-142">Name and URL path of the request</span></span>
**<span data-ttu-id="a44b5-143">Protocolo</span><span class="sxs-lookup"><span data-stu-id="a44b5-143">Protocol</span></span>** |  <span data-ttu-id="a44b5-144">Tipo de protocolo para a solicitação (por exemplo *, HTTPS, http/2*)</span><span class="sxs-lookup"><span data-stu-id="a44b5-144">Type of protocol for the request (such as *HTTPS, HTTP/2*)</span></span>
**<span data-ttu-id="a44b5-145">Método</span><span class="sxs-lookup"><span data-stu-id="a44b5-145">Method</span></span>** |    <span data-ttu-id="a44b5-146">[Método http](https://developer.mozilla.org/docs/Web/HTTP/Methods) usado para a solicitação</span><span class="sxs-lookup"><span data-stu-id="a44b5-146">[HTTP method](https://developer.mozilla.org/docs/Web/HTTP/Methods) used for the request</span></span>
**<span data-ttu-id="a44b5-147">Resultado</span><span class="sxs-lookup"><span data-stu-id="a44b5-147">Result</span></span>** |    <span data-ttu-id="a44b5-148">Código de [status de resposta http](https://developer.mozilla.org/docs/Web/HTTP/Status)</span><span class="sxs-lookup"><span data-stu-id="a44b5-148">[HTTP response status](https://developer.mozilla.org/docs/Web/HTTP/Status)  code</span></span>
**<span data-ttu-id="a44b5-149">Tipo de conteúdo</span><span class="sxs-lookup"><span data-stu-id="a44b5-149">Content type</span></span>** |  <span data-ttu-id="a44b5-150">Tipo de mídia solicitada ([tipo MIME](https://en.wikipedia.org/wiki/Media_type))</span><span class="sxs-lookup"><span data-stu-id="a44b5-150">Type of media requested ([MIME type](https://en.wikipedia.org/wiki/Media_type))</span></span>
**<span data-ttu-id="a44b5-151">Recebido</span><span class="sxs-lookup"><span data-stu-id="a44b5-151">Received</span></span>** | <span data-ttu-id="a44b5-152">Tamanho da resposta conforme entregue pelo servidor (não calculado para respostas em cache)</span><span class="sxs-lookup"><span data-stu-id="a44b5-152">Size of the response as delivered by the server (not calculated for cached responses)</span></span>
**<span data-ttu-id="a44b5-153">Hora</span><span class="sxs-lookup"><span data-stu-id="a44b5-153">Time</span></span>** |  <span data-ttu-id="a44b5-154">Tempo para carregar a resposta do servidor (não calculadas para respostas em cache)</span><span class="sxs-lookup"><span data-stu-id="a44b5-154">Time to load the server response (not calculated for cached responses)</span></span>
**<span data-ttu-id="a44b5-155">Inicia</span><span class="sxs-lookup"><span data-stu-id="a44b5-155">Initiator</span></span>** | <span data-ttu-id="a44b5-156">Subsistema responsável por iniciar a solicitação (como *Parser, redirecionar, script, outros*)</span><span class="sxs-lookup"><span data-stu-id="a44b5-156">Subsystem responsible for initiating the request (such as *Parser, Redirect, Script, Other*)</span></span>
**<span data-ttu-id="a44b5-157">Linha do Tempo</span><span class="sxs-lookup"><span data-stu-id="a44b5-157">Timeline</span></span>** | <span data-ttu-id="a44b5-158">Linha do tempo visual dos eventos de rede da solicitação (por exemplo *, interrupções, resolução (DNS), conexão (TCP), SSL, envio, espera (TTFB), baixando*).</span><span class="sxs-lookup"><span data-stu-id="a44b5-158">Visual timeline for the network events of the request (such as *Stalled, Resolving(DNS), Connecting(TCP), SSL, Sending, Waiting(TTFB), Downloading*).</span></span> <span data-ttu-id="a44b5-159">Passar o mouse sobre o gráfico fornece a divisão mais granular dos [intervalos de rede](#timings)de rede).</span><span class="sxs-lookup"><span data-stu-id="a44b5-159">Hovering over the chart provides the more granular breakdown of network [network timings](#timings)).</span></span>

### <span data-ttu-id="a44b5-160">Barra de resumo</span><span class="sxs-lookup"><span data-stu-id="a44b5-160">Summary bar</span></span>

<span data-ttu-id="a44b5-161">A barra na parte inferior do painel de **rede** resumirá o número total de erros de rede http, solicitações, dados transferidos e tempos de carregamento durante a sessão de criação de perfil de rede (ou seja, como o devtools foi aberto e gravando o tráfego de rede).</span><span class="sxs-lookup"><span data-stu-id="a44b5-161">The bar at the bottom of **Network** panel summarizes the total number of HTTP network errors, requests, data transfered, and load times during the network profiling session (i.e., since  DevTools were opened and recording network traffic).</span></span>

![Barra de resumo da rede](./media/network_summary_bar.png)

<span data-ttu-id="a44b5-163">**Tempo decorrido** significa o tempo entre o início da sessão de criação de perfil e quando o último recurso foi baixado da rede.</span><span class="sxs-lookup"><span data-stu-id="a44b5-163">**Elapsed time** means the time between the start of the profiling session and when the last resource was downloaded from the network.</span></span> <span data-ttu-id="a44b5-164">Os recursos buscados no cache do navegador não acumulam tempo para este número.</span><span class="sxs-lookup"><span data-stu-id="a44b5-164">Resources fetched from the browser cache do not accrue time to this number.</span></span> 

<span data-ttu-id="a44b5-165">**Tempo de carregamento do dom** significa o tempo entre o início da sessão de criação de perfil e quando o evento [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded) foi disparado para indicar que a estrutura do documento de página foi carregada e analisada (mas não necessariamente qualquer folha de estilos, imagem ou subquadros).</span><span class="sxs-lookup"><span data-stu-id="a44b5-165">**DOM load time** means the time between the start of the profiling session and when the [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded) event was fired to indicate that the structure of the page document has been loaded and parsed (though not necessarily any stylesheets, images or subframes).</span></span>

<span data-ttu-id="a44b5-166">Tempo de **carregamento de página** significa o tempo entre o início da sessão de criação de perfil e quando o evento [Load](https://developer.mozilla.org/docs/Web/Events/load) foi disparado para indicar que o documento da página (e todos os seus recursos) foi totalmente carregado.</span><span class="sxs-lookup"><span data-stu-id="a44b5-166">**Page load time** time means the time between the start of the profiling session and when the [load](https://developer.mozilla.org/docs/Web/Events/load) event was fired to indicate that the page document (and all its resources) has been fully loaded.</span></span>

## <span data-ttu-id="a44b5-167">Detalhes da solicitação</span><span class="sxs-lookup"><span data-stu-id="a44b5-167">Request details</span></span>

<span data-ttu-id="a44b5-168">Clicar em qualquer entrada na lista [**Resumo da rede**](#network-summary) abrirá o painel [**detalhes da solicitação**](#request-details) com informações adicionais em cada uma das guias a seguir.</span><span class="sxs-lookup"><span data-stu-id="a44b5-168">Clicking on any entry in the [**Network summary**](#network-summary) list will open the [**Request details**](#request-details) pane with further information in each of the following tabs.</span></span>

![Painel detalhes da solicitação de rede](./media/network_request_details.png)

### <span data-ttu-id="a44b5-170">Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="a44b5-170">Headers</span></span>
<span data-ttu-id="a44b5-171">Exibe os [cabeçalhos HTTP](https://developer.mozilla.org/docs/Web/HTTP/Headers) enviados para e recebidos do servidor.</span><span class="sxs-lookup"><span data-stu-id="a44b5-171">Displays the [HTTP headers](https://developer.mozilla.org/docs/Web/HTTP/Headers) sent to and received from the server.</span></span> <span data-ttu-id="a44b5-172">Clique com o botão direito do mouse em qualquer entrada de cabeçalho para copiá-lo ( `Ctrl+C` ) para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="a44b5-172">Right-click on any header entry to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="a44b5-173">Você também pode selecionar várias entradas mantendo pressionada a `Shift` tecla ou selecionando ALL ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="a44b5-173">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

### <span data-ttu-id="a44b5-174">Body</span><span class="sxs-lookup"><span data-stu-id="a44b5-174">Body</span></span>
<span data-ttu-id="a44b5-175">Exibe os dados do corpo (se disponíveis) das cargas de solicitação e resposta.</span><span class="sxs-lookup"><span data-stu-id="a44b5-175">Displays the body data (if available) of the request and response payloads.</span></span>

<span data-ttu-id="a44b5-176">Conteúdo da imagem é exibido com dimensões e dados de tamanho.</span><span class="sxs-lookup"><span data-stu-id="a44b5-176">Image content is displayed with dimensions and size data.</span></span>

<span data-ttu-id="a44b5-177">O conteúdo de texto é exibido em um editor (somente leitura) com opções para formatar o conteúdo do minified com uma **superimposição de impressão** e/ou **quebra automática de texto** para facilitar a leitura.</span><span class="sxs-lookup"><span data-stu-id="a44b5-177">Text content appears in a (read-only) editor with options to format minified content with **Pretty print** and/or **Word wrap** for easier readability.</span></span>

![Guia corpo do painel detalhes da solicitação](./media/network_details_body.png)

### <span data-ttu-id="a44b5-179">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a44b5-179">Parameters</span></span>
<span data-ttu-id="a44b5-180">Exibe parâmetros da cadeia de caracteres de consulta para solicitações GET.</span><span class="sxs-lookup"><span data-stu-id="a44b5-180">Displays query string parameters for GET requests.</span></span> <span data-ttu-id="a44b5-181">Enquanto os parâmetros de solicitações POST são enviados nos cabeçalhos, as solicitações GET são incluídas na URL.</span><span class="sxs-lookup"><span data-stu-id="a44b5-181">While the parameters of POST requests are sent in the headers, GET requests include them in the URL.</span></span> <span data-ttu-id="a44b5-182">Elas são desmembradas aqui para facilitar a leitura.</span><span class="sxs-lookup"><span data-stu-id="a44b5-182">They're broken out here for easier reading.</span></span>

<span data-ttu-id="a44b5-183">Clique com o botão direito do mouse em qualquer linha para copiá-la ( `Ctrl+C` ) para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="a44b5-183">Right-click on any row to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="a44b5-184">Você também pode selecionar várias entradas mantendo pressionada a `Shift` tecla ou selecionando ALL ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="a44b5-184">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

### <span data-ttu-id="a44b5-185">Cookies</span><span class="sxs-lookup"><span data-stu-id="a44b5-185">Cookies</span></span>
<span data-ttu-id="a44b5-186">Exibe cookies que são enviados ou recebidos como pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="a44b5-186">Displays cookies that are sent or received as key/value pairs.</span></span>

<span data-ttu-id="a44b5-187">Clique com o botão direito do mouse em qualquer linha para copiá-la ( `Ctrl+C` ) para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="a44b5-187">Right-click on any row to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="a44b5-188">Você também pode selecionar várias entradas mantendo pressionada a `Shift` tecla ou selecionando ALL ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="a44b5-188">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

<span data-ttu-id="a44b5-189">Você pode limpar os cookies armazenados para o domínio especificado na [barra de ferramentas](#network-summary) (botão**Limpar cookies** ).</span><span class="sxs-lookup"><span data-stu-id="a44b5-189">You can clear the stored cookies for the given domain from the [Toolbar](#network-summary) (**Clear cookies** button).</span></span> 

### <span data-ttu-id="a44b5-190">Intervalos</span><span class="sxs-lookup"><span data-stu-id="a44b5-190">Timings</span></span>

<span data-ttu-id="a44b5-191">A guia **intervalos** fornece uma linha do tempo de eventos de rede envolvidos no carregamento do recurso selecionado.</span><span class="sxs-lookup"><span data-stu-id="a44b5-191">The **Timings** tab provides a timeline of network events involved in the loading of the selected resource.</span></span> <span data-ttu-id="a44b5-192">Isso é semelhante às informações encontradas na coluna *linha do tempo* da lista de [solicitação de rede](#network-request-list), mas também inclui os eventos que levaram à solicitação que está sendo enviada pela conexão, como o tempo gasto aguardando (*parado*) na fila de solicitações, a resolução DNS e o estabelecimento da conexão TCP.</span><span class="sxs-lookup"><span data-stu-id="a44b5-192">This is similar to the information found in the *Timeline* column of the [Network request list](#network-request-list), but also includes the events leading up to the request being sent over the wire, such as time spent waiting (*Stalled*) in the request queue, DNS resolution, and establishing the TCP connection.</span></span> 

![Guia intervalos do painel detalhes da solicitação](./media/network_details_timings.png)

<span data-ttu-id="a44b5-194">Os redirecionamentos de/para outros recursos são observados e clicar no link definirá o foco para esse recurso no painel de [detalhes da solicitação](#request details) de rede.</span><span class="sxs-lookup"><span data-stu-id="a44b5-194">Redirections to/from other resources are noted, and clicking on the link will set focus to that resource in the network [request details](#request details) pane.</span></span>

<span data-ttu-id="a44b5-195">Os redirecionamentos carregados do cache não são afetados pela latência da rede, portanto, nenhum gráfico de *tempo* de rede será exibido.</span><span class="sxs-lookup"><span data-stu-id="a44b5-195">Resouces loaded from the cache are not affected by network latency, so no network *Timings* chart will display.</span></span>

![Recurso Redirecionado carregado do cache](./media/network_details_timings_cache_redirect.png)

<span data-ttu-id="a44b5-197">Aqui estão os diferentes eventos de rede que podem ser exibidos para um determinado recurso, em ordem cronológica:</span><span class="sxs-lookup"><span data-stu-id="a44b5-197">Here are the different network events you might see for a given resource, in chronological order:</span></span>

#### <span data-ttu-id="a44b5-198">Paralisação</span><span class="sxs-lookup"><span data-stu-id="a44b5-198">Stalled</span></span>

<span data-ttu-id="a44b5-199">Tempo gasto aguardando uma conexão de rede disponível na fila de solicitações.</span><span class="sxs-lookup"><span data-stu-id="a44b5-199">Time spent waiting for an available network connection in the request queue.</span></span> <span data-ttu-id="a44b5-200">Para HTTP 1.0/1.1, o Microsoft Edge permite um máximo de seis (6) conexões TCP simultâneas por nome de host.</span><span class="sxs-lookup"><span data-stu-id="a44b5-200">For HTTP 1.0/1.1, Microsoft Edge allows a maximum of six (6) simultaneous TCP connections per hostname.</span></span> 

#### <span data-ttu-id="a44b5-201">Resolvendo (DNS)</span><span class="sxs-lookup"><span data-stu-id="a44b5-201">Resolving (DNS)</span></span>

<span data-ttu-id="a44b5-202">Tempo gasto procurando o endereço IP do nome do host do recurso no DNS (sistema de[nome de domínio](https://en.wikipedia.org/wiki/Domain_Name_System)).</span><span class="sxs-lookup"><span data-stu-id="a44b5-202">Time spent looking up the IP address for the hostname of the resource in the DNS ([Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System)).</span></span>

#### <span data-ttu-id="a44b5-203">Conectando (TCP)</span><span class="sxs-lookup"><span data-stu-id="a44b5-203">Connecting (TCP)</span></span>

<span data-ttu-id="a44b5-204">Tempo gasto para estabelecer a conexão TCP ([Transmission Control Protocol](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)).</span><span class="sxs-lookup"><span data-stu-id="a44b5-204">Time spent establishing the TCP ([Transmission Control Protocol](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)) connection.</span></span>

#### <span data-ttu-id="a44b5-205">SSL</span><span class="sxs-lookup"><span data-stu-id="a44b5-205">SSL</span></span>

<span data-ttu-id="a44b5-206">Tempo gasto na negociação de uma conexão SSL ([Secure Sockets](https://en.wikipedia.org/wiki/Transport_Layer_Security)Layer) com o [servidor proxy](https://en.wikipedia.org/wiki/Proxy_server) para o host.</span><span class="sxs-lookup"><span data-stu-id="a44b5-206">Time spent negotiating a SSL ([Secure Sockets Layer](https://en.wikipedia.org/wiki/Transport_Layer_Security))  connection with the [proxy server](https://en.wikipedia.org/wiki/Proxy_server) for the host.</span></span>

#### <span data-ttu-id="a44b5-207">Envie</span><span class="sxs-lookup"><span data-stu-id="a44b5-207">Sending</span></span>

<span data-ttu-id="a44b5-208">Tempo gasto para enviar a solicitação de recurso.</span><span class="sxs-lookup"><span data-stu-id="a44b5-208">Time spent sending the resource request.</span></span>

#### <span data-ttu-id="a44b5-209">Aguardando (TTFB)</span><span class="sxs-lookup"><span data-stu-id="a44b5-209">Waiting (TTFB)</span></span>

<span data-ttu-id="a44b5-210">Tempo gasto aguardando o primeiro byte da resposta do servidor host ("tempo até o primeiro byte" ou *TTFB*).</span><span class="sxs-lookup"><span data-stu-id="a44b5-210">Time spent waiting for the first byte of the response from the host server ("time to first byte", or *TTFB*).</span></span>

#### <span data-ttu-id="a44b5-211">Baixá</span><span class="sxs-lookup"><span data-stu-id="a44b5-211">Downloading</span></span>

<span data-ttu-id="a44b5-212">Tempo gasto na leitura da resposta do servidor.</span><span class="sxs-lookup"><span data-stu-id="a44b5-212">Time spent reading the response from the server.</span></span>

## <span data-ttu-id="a44b5-213">Teclado</span><span class="sxs-lookup"><span data-stu-id="a44b5-213">Shortcuts</span></span>

| <span data-ttu-id="a44b5-214">Ação</span><span class="sxs-lookup"><span data-stu-id="a44b5-214">Action</span></span>                         | <span data-ttu-id="a44b5-215">Atalho</span><span class="sxs-lookup"><span data-stu-id="a44b5-215">Shortcut</span></span>     |
|:-------------------------------|:-------------|
| <span data-ttu-id="a44b5-216">Iniciar/parar sessão de criação de perfil</span><span class="sxs-lookup"><span data-stu-id="a44b5-216">Start / Stop profiling session</span></span> | `Ctrl` + `E` |
| <span data-ttu-id="a44b5-217">Exportar como HAR</span><span class="sxs-lookup"><span data-stu-id="a44b5-217">Export as HAR</span></span>                  | `Ctrl` + `S` |
| <span data-ttu-id="a44b5-218">Localizar</span><span class="sxs-lookup"><span data-stu-id="a44b5-218">Find</span></span>                           | `Ctrl` + `F` |
| <span data-ttu-id="a44b5-219">Copiar</span><span class="sxs-lookup"><span data-stu-id="a44b5-219">Copy</span></span>                           | `Ctrl` + `C` |

## <span data-ttu-id="a44b5-220">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="a44b5-220">Known Issues</span></span>

### <span data-ttu-id="a44b5-221">Falha ao iniciar o agente de coleta de rede.</span><span class="sxs-lookup"><span data-stu-id="a44b5-221">The network collection agent failed to start.</span></span>

<span data-ttu-id="a44b5-222">Se você vir esta mensagem de erro: **o agente de coleta de rede falhou ao iniciar** na ferramenta de rede, siga estas etapas para solucionar o problema.</span><span class="sxs-lookup"><span data-stu-id="a44b5-222">If you see this error message: **The network collection agent failed to start** in the Network tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="a44b5-223">Pressione `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="a44b5-223">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="a44b5-224">Na caixa de diálogo Executar, digite **Services. msc**.</span><span class="sxs-lookup"><span data-stu-id="a44b5-224">In the Run dialog, enter **services.msc**.</span></span>
![conhecidos-problemas-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="a44b5-226">Localize o **serviço coletor padrão do hub de diagnóstico da Microsoft (R)** e clique nele com o botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="a44b5-226">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![conhecidos-problemas-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="a44b5-228">Reinicie o **serviço coletor padrão do hub de diagnóstico do Microsoft (R)**.</span><span class="sxs-lookup"><span data-stu-id="a44b5-228">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![conhecidos-problemas-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="a44b5-230">Feche as ferramentas de desenvolvedor do Microsoft Edge e a guia. Abra uma nova guia, navegue até a página e pressione `F12` .</span><span class="sxs-lookup"><span data-stu-id="a44b5-230">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="a44b5-231">Agora você deve ver um emblema de reprodução ao lado de **rede** e solicitações de rede para a sua página da Web.</span><span class="sxs-lookup"><span data-stu-id="a44b5-231">You should now see a Play badge next to **Network** and the network requests for your webpage.</span></span>
![conhecidos-problemas-4](./media/known_issues_4-network.PNG)

<span data-ttu-id="a44b5-233">Ainda está com problemas?</span><span class="sxs-lookup"><span data-stu-id="a44b5-233">Still running into problems?</span></span> <span data-ttu-id="a44b5-234">Envie-nos seus comentários usando o ícone **enviar comentários** !</span><span class="sxs-lookup"><span data-stu-id="a44b5-234">Please send us your feedback using the **Send feedback** icon!</span></span> 

![conhecidos-problemas-5](./media/known_issues_5.PNG)

### <span data-ttu-id="a44b5-236">Falha ao parar o agente de coleta de rede.</span><span class="sxs-lookup"><span data-stu-id="a44b5-236">The network collection agent failed to stop.</span></span>

<span data-ttu-id="a44b5-237">Se você vir esta mensagem de erro: **o agente de coleta de rede não parou** na ferramenta de rede, siga estas etapas para solucionar o problema.</span><span class="sxs-lookup"><span data-stu-id="a44b5-237">If you see this error message: **The network collection agent failed to stop** in the Network tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="a44b5-238">Pressione `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="a44b5-238">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="a44b5-239">Na caixa de diálogo Executar, digite **Services. msc**.</span><span class="sxs-lookup"><span data-stu-id="a44b5-239">In the Run dialog, enter **services.msc**.</span></span>
![conhecidos-problemas-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="a44b5-241">Localize o **serviço coletor padrão do hub de diagnóstico da Microsoft (R)** e clique nele com o botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="a44b5-241">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![conhecidos-problemas-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="a44b5-243">Reinicie o **serviço coletor padrão do hub de diagnóstico do Microsoft (R)**.</span><span class="sxs-lookup"><span data-stu-id="a44b5-243">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![conhecidos-problemas-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="a44b5-245">Feche as ferramentas de desenvolvedor do Microsoft Edge e a guia. Abra uma nova guia, navegue até a página e pressione `F12` .</span><span class="sxs-lookup"><span data-stu-id="a44b5-245">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="a44b5-246">Agora você deve ver um emblema de reprodução ao lado de **rede** e solicitações de rede para a sua página da Web.</span><span class="sxs-lookup"><span data-stu-id="a44b5-246">You should now see a Play badge next to **Network** and the network requests for your webpage.</span></span>
![conhecidos-problemas-4](./media/known_issues_4-network.PNG)

<span data-ttu-id="a44b5-248">Ainda está com problemas?</span><span class="sxs-lookup"><span data-stu-id="a44b5-248">Still running into problems?</span></span> <span data-ttu-id="a44b5-249">Envie-nos seus comentários usando o ícone **enviar comentários** !</span><span class="sxs-lookup"><span data-stu-id="a44b5-249">Please send us your feedback using the **Send feedback** icon!</span></span> 

![conhecidos-problemas-5](./media/known_issues_5.PNG)
