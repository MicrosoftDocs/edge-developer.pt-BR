---
description: O modo de eventos de linha do tempo exibe todos os eventos disparados ao criar uma gravação.  Use a referência de evento Timeline para saber mais sobre cada tipo de evento de linha do tempo.
title: Referência de Evento de Linha do Tempo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 989d4d84345fedc1c5aef2cb8d893db3c0e1634b
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124898"
---
<!-- Copyright Meggin Kearney and Flavio Copes

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <span data-ttu-id="2b0e1-105">Referência de Evento de Linha do Tempo</span><span class="sxs-lookup"><span data-stu-id="2b0e1-105">Timeline Event Reference</span></span>  

<span data-ttu-id="2b0e1-106">O modo de eventos de linha do tempo exibe todos os eventos disparados ao criar uma gravação.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-106">The timeline events mode displays all events triggered while making a recording.</span></span>  <span data-ttu-id="2b0e1-107">Use a referência de evento Timeline para saber mais sobre cada tipo de evento de linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-107">Use the timeline event reference to learn more about each timeline event type.</span></span>  

## <span data-ttu-id="2b0e1-108">Propriedades de eventos comuns da linha do tempo</span><span class="sxs-lookup"><span data-stu-id="2b0e1-108">Common timeline event properties</span></span>  

<span data-ttu-id="2b0e1-109">Alguns detalhes estão presentes em eventos de todos os tipos, enquanto alguns só se aplicam a determinados tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-109">Certain details are present in events of all types, while some only apply to certain event types.</span></span>  <span data-ttu-id="2b0e1-110">Esta seção lista as propriedades comuns a diferentes tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-110">This section lists properties common to different event types.</span></span>  <span data-ttu-id="2b0e1-111">As propriedades específicas para determinados tipos de eventos são listadas nas referências para os tipos de eventos que se seguem.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-111">Properties specific to certain event types are listed in the references for those event types that follow.</span></span>  

| <span data-ttu-id="2b0e1-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2b0e1-112">Property</span></span> | <span data-ttu-id="2b0e1-113">Quando é exibido</span><span class="sxs-lookup"><span data-stu-id="2b0e1-113">When is it shown</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="2b0e1-114">Tempo agregado</span><span class="sxs-lookup"><span data-stu-id="2b0e1-114">Aggregated time</span></span> | <span data-ttu-id="2b0e1-115">Para eventos com **eventos aninhados**, o tempo usado por cada categoria de eventos.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-115">For events with **nested events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="2b0e1-116">Pilha de chamadas</span><span class="sxs-lookup"><span data-stu-id="2b0e1-116">Call Stack</span></span> | <span data-ttu-id="2b0e1-117">Para eventos com **eventos filho**, o tempo usado por cada categoria de eventos.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-117">For events with **child events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="2b0e1-118">Tempo de CPU</span><span class="sxs-lookup"><span data-stu-id="2b0e1-118">CPU time</span></span> | <span data-ttu-id="2b0e1-119">Quanto tempo da CPU o evento registrado levou.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-119">How much CPU time the recorded event took.</span></span> |  
| <span data-ttu-id="2b0e1-120">Detalhes</span><span class="sxs-lookup"><span data-stu-id="2b0e1-120">Details</span></span> | <span data-ttu-id="2b0e1-121">Outros detalhes sobre o evento.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-121">Other details about the event.</span></span> |  
| <span data-ttu-id="2b0e1-122">Duration \ (no carimbo de data/hora \)</span><span class="sxs-lookup"><span data-stu-id="2b0e1-122">Duration \(at time-stamp\)</span></span> | <span data-ttu-id="2b0e1-123">Quanto tempo levava o evento com todos os seus filhos a concluir; carimbo de data/hora é o horário em que o evento ocorreu em relação ao início da gravação.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-123">How long it took the event with all of its children to complete; timestamp is the time at which the event occurred, relative to when the recording started.</span></span> |  
| <span data-ttu-id="2b0e1-124">Tempo de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="2b0e1-124">Self time</span></span> | <span data-ttu-id="2b0e1-125">Por quanto tempo o evento demorou sem qualquer um de seus filhos.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-125">How long the event took without any of its children.</span></span> |  
| <span data-ttu-id="2b0e1-126">Tamanho de heap usado</span><span class="sxs-lookup"><span data-stu-id="2b0e1-126">Used Heap Size</span></span> | <span data-ttu-id="2b0e1-127">A quantidade de memória que está sendo usada pelo aplicativo quando o evento foi gravado, e a alteração de \ (+/-\) do Delta é usada em tamanho de heap usado desde a última amostragem.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-127">Amount of memory being used by the application when the event was recorded, and the delta \(+/-\) change in used heap size since the last sampling.</span></span> |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <span data-ttu-id="2b0e1-128">Carregando eventos</span><span class="sxs-lookup"><span data-stu-id="2b0e1-128">Loading events</span></span>  

<span data-ttu-id="2b0e1-129">Esta seção lista os eventos que pertencem à categoria de carregamento e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-129">This section lists events that belong to Loading category and their properties.</span></span>  

| <span data-ttu-id="2b0e1-130">Evento</span><span class="sxs-lookup"><span data-stu-id="2b0e1-130">Event</span></span> | <span data-ttu-id="2b0e1-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b0e1-131">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="2b0e1-132">Analisar HTML</span><span class="sxs-lookup"><span data-stu-id="2b0e1-132">Parse HTML</span></span> |  <span data-ttu-id="2b0e1-133">O Microsoft Edge executou o algoritmo de análise HTML.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-133">Microsoft Edge ran the HTML parsing algorithm.</span></span> |  
| <span data-ttu-id="2b0e1-134">Concluir o carregamento</span><span class="sxs-lookup"><span data-stu-id="2b0e1-134">Finish Loading</span></span> |  <span data-ttu-id="2b0e1-135">Uma solicitação de rede foi concluída.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-135">A network request completed.</span></span> |  
| <span data-ttu-id="2b0e1-136">Receber dados</span><span class="sxs-lookup"><span data-stu-id="2b0e1-136">Receive Data</span></span> |  <span data-ttu-id="2b0e1-137">Os dados de uma solicitação foram recebidos.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-137">Data for a request was received.</span></span>  <span data-ttu-id="2b0e1-138">Há um ou mais eventos de recebimento de dados.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-138">There are one or more Receive Data events.</span></span> |  
| <span data-ttu-id="2b0e1-139">Receber resposta</span><span class="sxs-lookup"><span data-stu-id="2b0e1-139">Receive Response</span></span> |  <span data-ttu-id="2b0e1-140">A resposta HTTP inicial de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-140">The initial HTTP response from a request.</span></span> |  
| <span data-ttu-id="2b0e1-141">Enviar solicitação</span><span class="sxs-lookup"><span data-stu-id="2b0e1-141">Send Request</span></span> |  <span data-ttu-id="2b0e1-142">Uma solicitação de rede foi enviada.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-142">A network request has been sent.</span></span> |  

### <span data-ttu-id="2b0e1-143">Carregando Propriedades do evento</span><span class="sxs-lookup"><span data-stu-id="2b0e1-143">Loading event properties</span></span>  

| <span data-ttu-id="2b0e1-144">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2b0e1-144">Property</span></span> | <span data-ttu-id="2b0e1-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b0e1-145">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="2b0e1-146">Recurso</span><span class="sxs-lookup"><span data-stu-id="2b0e1-146">Resource</span></span> | <span data-ttu-id="2b0e1-147">A URL do recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-147">The URL of the requested resource.</span></span> |  
| <span data-ttu-id="2b0e1-148">Visualização</span><span class="sxs-lookup"><span data-stu-id="2b0e1-148">Preview</span></span> | <span data-ttu-id="2b0e1-149">Visualização do recurso solicitado \ (apenas imagens \).</span><span class="sxs-lookup"><span data-stu-id="2b0e1-149">Preview of the requested resource \(images only\).</span></span> |  
| <span data-ttu-id="2b0e1-150">Método de solicitação</span><span class="sxs-lookup"><span data-stu-id="2b0e1-150">Request Method</span></span> | <span data-ttu-id="2b0e1-151">Método HTTP usado para a solicitação \ ( `GET` ou `POST` , por exemplo, \).</span><span class="sxs-lookup"><span data-stu-id="2b0e1-151">HTTP method used for the request \(`GET` or `POST`, for example\).</span></span> |  
| <span data-ttu-id="2b0e1-152">Código de status</span><span class="sxs-lookup"><span data-stu-id="2b0e1-152">Status Code</span></span> | <span data-ttu-id="2b0e1-153">Código de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-153">HTTP response code.</span></span> |  
| <span data-ttu-id="2b0e1-154">Tipo MIME</span><span class="sxs-lookup"><span data-stu-id="2b0e1-154">MIME Type</span></span> | <span data-ttu-id="2b0e1-155">Tipo MIME do recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-155">MIME type of the requested resource.</span></span> |  
| <span data-ttu-id="2b0e1-156">Comprimento de dados codificados</span><span class="sxs-lookup"><span data-stu-id="2b0e1-156">Encoded Data Length</span></span> | <span data-ttu-id="2b0e1-157">Comprimento do recurso solicitado em bytes.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-157">Length of requested resource in bytes.</span></span> |  

## <span data-ttu-id="2b0e1-158">Eventos de script</span><span class="sxs-lookup"><span data-stu-id="2b0e1-158">Scripting events</span></span>  

<span data-ttu-id="2b0e1-159">Esta seção lista os eventos que pertencem à categoria de script e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-159">This section lists events that belong to the Scripting category and their properties.</span></span>  

| <span data-ttu-id="2b0e1-160">Evento</span><span class="sxs-lookup"><span data-stu-id="2b0e1-160">Event</span></span> | <span data-ttu-id="2b0e1-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b0e1-161">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="2b0e1-162">Quadro de animação acionado</span><span class="sxs-lookup"><span data-stu-id="2b0e1-162">Animation Frame Fired</span></span> | <span data-ttu-id="2b0e1-163">Um quadro de animação programado foi acionado, e seu manipulador de retorno de chamada foi invocado.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-163">A scheduled animation frame fired, and its callback handler invoked.</span></span> |  
| <span data-ttu-id="2b0e1-164">Cancelar quadro de animação</span><span class="sxs-lookup"><span data-stu-id="2b0e1-164">Cancel Animation Frame</span></span> |  <span data-ttu-id="2b0e1-165">Um quadro de animação agendado foi cancelado.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-165">A scheduled animation frame was canceled.</span></span> |  
| <span data-ttu-id="2b0e1-166">Evento GC</span><span class="sxs-lookup"><span data-stu-id="2b0e1-166">GC Event</span></span> |  <span data-ttu-id="2b0e1-167">Ocorreu uma coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-167">Garbage collection occurred.</span></span> |  
| <span data-ttu-id="2b0e1-168">DOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="2b0e1-168">DOMContentLoaded</span></span> |  <span data-ttu-id="2b0e1-169">O [evento DOMContentLoaded][MDNWindowDOMContentLoadedEvent] foi acionado pelo navegador.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-169">The [DOMContentLoaded event][MDNWindowDOMContentLoadedEvent] was fired by the browser.</span></span>  <span data-ttu-id="2b0e1-170">Esse evento é acionado quando todo o conteúdo DOM da página é carregado e analisado.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-170">This event is fired when all of the page's DOM content has been loaded and parsed.</span></span> |  
| <span data-ttu-id="2b0e1-171">Avaliar o script</span><span class="sxs-lookup"><span data-stu-id="2b0e1-171">Evaluate Script</span></span> | <span data-ttu-id="2b0e1-172">Um script foi avaliado.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-172">A script was evaluated.</span></span> |  
| <span data-ttu-id="2b0e1-173">Evento</span><span class="sxs-lookup"><span data-stu-id="2b0e1-173">Event</span></span> | <span data-ttu-id="2b0e1-174">Um evento JavaScript \ (por exemplo, `mousedown` , ou `key` \).</span><span class="sxs-lookup"><span data-stu-id="2b0e1-174">A JavaScript event \(for example, `mousedown`, or `key`\).</span></span> |  
| <span data-ttu-id="2b0e1-175">Chamada de função</span><span class="sxs-lookup"><span data-stu-id="2b0e1-175">Function Call</span></span> | <span data-ttu-id="2b0e1-176">Uma chamada de função JavaScript de nível superior foi feita \ (só aparece quando o navegador entra no mecanismo JavaScript \).</span><span class="sxs-lookup"><span data-stu-id="2b0e1-176">A top-level JavaScript function call was made \(only appears when browser enters JavaScript engine\).</span></span> |  
| <span data-ttu-id="2b0e1-177">Temporizador de instalação</span><span class="sxs-lookup"><span data-stu-id="2b0e1-177">Install Timer</span></span> | <span data-ttu-id="2b0e1-178">Um temporizador foi criado com [setInterval ()][MDNWindowOrWorkerGlobalScopeSetInterval] ou [setTimeout ()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span><span class="sxs-lookup"><span data-stu-id="2b0e1-178">A timer was created with [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] or [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span></span> |  
| <span data-ttu-id="2b0e1-179">Quadro de animação de solicitação</span><span class="sxs-lookup"><span data-stu-id="2b0e1-179">Request Animation Frame</span></span> | <span data-ttu-id="2b0e1-180">Uma `requestAnimationFrame()` chamada agendou um novo quadro.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-180">A `requestAnimationFrame()` call scheduled a new frame.</span></span> |  
| <span data-ttu-id="2b0e1-181">Remover temporizador</span><span class="sxs-lookup"><span data-stu-id="2b0e1-181">Remove Timer</span></span> | <span data-ttu-id="2b0e1-182">Um temporizador criado anteriormente foi limpo.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-182">A previously created timer was cleared.</span></span> |  
| <span data-ttu-id="2b0e1-183">Hora</span><span class="sxs-lookup"><span data-stu-id="2b0e1-183">Time</span></span> |  <span data-ttu-id="2b0e1-184">Um script chamado [console. time ()][ConsoleApiTime].</span><span class="sxs-lookup"><span data-stu-id="2b0e1-184">A script called [console.time()][ConsoleApiTime].</span></span> |  
| <span data-ttu-id="2b0e1-185">Término do tempo</span><span class="sxs-lookup"><span data-stu-id="2b0e1-185">Time End</span></span> | <span data-ttu-id="2b0e1-186">Um script chamado [console. timeEnd ()][ConsoleApiTimeEnd].</span><span class="sxs-lookup"><span data-stu-id="2b0e1-186">A script called [console.timeEnd()][ConsoleApiTimeEnd].</span></span> |  
| <span data-ttu-id="2b0e1-187">Temporizador acionado</span><span class="sxs-lookup"><span data-stu-id="2b0e1-187">Timer Fired</span></span> | <span data-ttu-id="2b0e1-188">Um temporizador foi acionado que foi agendado com `setInterval()` ou `setTimeout()` .</span><span class="sxs-lookup"><span data-stu-id="2b0e1-188">A timer fired that was scheduled with `setInterval()` or `setTimeout()`.</span></span> |  
| <span data-ttu-id="2b0e1-189">Alteração de estado pronto para XHR</span><span class="sxs-lookup"><span data-stu-id="2b0e1-189">XHR Ready State Change</span></span> | <span data-ttu-id="2b0e1-190">O estado pronto de um XMLHttpRequest alterado.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-190">The ready state of an XMLHTTPRequest changed.</span></span> |  
| <span data-ttu-id="2b0e1-191">Carga XHR</span><span class="sxs-lookup"><span data-stu-id="2b0e1-191">XHR Load</span></span> | <span data-ttu-id="2b0e1-192">`XMLHTTPRequest`Conclusão do carregamento.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-192">An `XMLHTTPRequest` finished loading.</span></span> |  

### <span data-ttu-id="2b0e1-193">Propriedades de evento de script</span><span class="sxs-lookup"><span data-stu-id="2b0e1-193">Scripting event properties</span></span>  

| <span data-ttu-id="2b0e1-194">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2b0e1-194">Property</span></span> | <span data-ttu-id="2b0e1-195">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b0e1-195">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="2b0e1-196">ID do temporizador</span><span class="sxs-lookup"><span data-stu-id="2b0e1-196">Timer ID</span></span> | <span data-ttu-id="2b0e1-197">A ID do temporizador.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-197">The timer ID.</span></span> |  
| <span data-ttu-id="2b0e1-198">Tempo limite</span><span class="sxs-lookup"><span data-stu-id="2b0e1-198">Timeout</span></span> | <span data-ttu-id="2b0e1-199">O tempo limite especificado pelo temporizador.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-199">The timeout specified by the timer.</span></span> |  
| <span data-ttu-id="2b0e1-200">Repete</span><span class="sxs-lookup"><span data-stu-id="2b0e1-200">Repeats</span></span> | <span data-ttu-id="2b0e1-201">Booliano que especifica se o cronômetro se repete.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-201">Boolean that specifies if the timer repeats.</span></span> |  
| <span data-ttu-id="2b0e1-202">Chamada de função</span><span class="sxs-lookup"><span data-stu-id="2b0e1-202">Function Call</span></span> | <span data-ttu-id="2b0e1-203">Uma função que foi invocada.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-203">A function that was invoked.</span></span> |  

## <span data-ttu-id="2b0e1-204">Eventos de renderização</span><span class="sxs-lookup"><span data-stu-id="2b0e1-204">Rendering events</span></span>  

<span data-ttu-id="2b0e1-205">Esta seção lista os eventos que pertencem à categoria de renderização e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-205">This section lists events that belong to Rendering category and their properties.</span></span>  

| <span data-ttu-id="2b0e1-206">Evento</span><span class="sxs-lookup"><span data-stu-id="2b0e1-206">Event</span></span> | <span data-ttu-id="2b0e1-207">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b0e1-207">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="2b0e1-208">Layout Invalidate</span><span class="sxs-lookup"><span data-stu-id="2b0e1-208">Invalidate layout</span></span> | <span data-ttu-id="2b0e1-209">O layout da página foi invalidado por uma alteração DOM.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-209">The page layout was invalidated by a DOM change.</span></span> |  
| <span data-ttu-id="2b0e1-210">Layout</span><span class="sxs-lookup"><span data-stu-id="2b0e1-210">Layout</span></span> | <span data-ttu-id="2b0e1-211">Um layout de página foi concluído.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-211">A page layout was completed.</span></span> |  
| <span data-ttu-id="2b0e1-212">Recalcular estilo</span><span class="sxs-lookup"><span data-stu-id="2b0e1-212">Recalculate style</span></span> | <span data-ttu-id="2b0e1-213">Estilos de elemento recalculados do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-213">Microsoft Edge recalculated element styles.</span></span> |  
| <span data-ttu-id="2b0e1-214">Rolagem</span><span class="sxs-lookup"><span data-stu-id="2b0e1-214">Scroll</span></span> | <span data-ttu-id="2b0e1-215">O conteúdo do modo de exibição aninhado foi rolado.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-215">The content of nested view was scrolled.</span></span> |  

### <span data-ttu-id="2b0e1-216">Renderizando Propriedades de eventos</span><span class="sxs-lookup"><span data-stu-id="2b0e1-216">Rendering event properties</span></span>  

| <span data-ttu-id="2b0e1-217">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2b0e1-217">Property</span></span> | <span data-ttu-id="2b0e1-218">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b0e1-218">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="2b0e1-219">Layout invalidado</span><span class="sxs-lookup"><span data-stu-id="2b0e1-219">Layout invalidated</span></span> | <span data-ttu-id="2b0e1-220">Para registros de layout, o rastreamento de pilha do código que fez com que o layout fosse invalidado.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-220">For Layout records, the stack trace of the code that caused the layout to be invalidated.</span></span> |  
| <span data-ttu-id="2b0e1-221">Nós que precisam de layout</span><span class="sxs-lookup"><span data-stu-id="2b0e1-221">Nodes that need layout</span></span> | <span data-ttu-id="2b0e1-222">Para registros de layout, o número de nós que foram marcados como necessidade de layout antes do reinício do layout.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-222">For Layout records, the number of nodes that were marked as needing layout before the relayout started.</span></span>  <span data-ttu-id="2b0e1-223">Esses nós normalmente são aqueles que foram invalidados pelo código do desenvolvedor, mais o caminho para a vertical para refazer o layout da raiz.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-223">These are normally those nodes that were invalidated by developer code, plus a path upward to relayout root.</span></span> |  
| <span data-ttu-id="2b0e1-224">Tamanho da árvore de layout</span><span class="sxs-lookup"><span data-stu-id="2b0e1-224">Layout tree size</span></span> | <span data-ttu-id="2b0e1-225">Para registros de layout, o número total de nós sob a raiz do relayout \ (o nó que o Microsoft Edge inicia o relayout \).</span><span class="sxs-lookup"><span data-stu-id="2b0e1-225">For Layout records, the total number of nodes under the relayout root \(the node that Microsoft Edge starts the relayout\).</span></span> |  
| <span data-ttu-id="2b0e1-226">Escopo de layout</span><span class="sxs-lookup"><span data-stu-id="2b0e1-226">Layout scope</span></span> | <span data-ttu-id="2b0e1-227">Os valores possíveis são `Partial` \ (o limite de novo layout é uma parte do dom \) ou `Whole document` .</span><span class="sxs-lookup"><span data-stu-id="2b0e1-227">Possible values are `Partial` \(the re-layout boundary is a portion of the DOM\) or `Whole document`.</span></span> |  
| <span data-ttu-id="2b0e1-228">Elementos afetados</span><span class="sxs-lookup"><span data-stu-id="2b0e1-228">Elements affected</span></span> | <span data-ttu-id="2b0e1-229">Para recalcular registros de estilo, o número de elementos afetados por um recálculo de estilo.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-229">For Recalculate style records, the number of elements affected by a style recalculation.</span></span> |  
| <span data-ttu-id="2b0e1-230">Estilos invalidados</span><span class="sxs-lookup"><span data-stu-id="2b0e1-230">Styles invalidated</span></span> | <span data-ttu-id="2b0e1-231">Para recalcular registros de estilo, fornece o rastreamento de pilha do código que causou a invalidação de estilo.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-231">For Recalculate style records, provides the stack trace of the code that caused the style invalidation.</span></span> |  

## <span data-ttu-id="2b0e1-232">Eventos de pintura</span><span class="sxs-lookup"><span data-stu-id="2b0e1-232">Painting events</span></span>  

<span data-ttu-id="2b0e1-233">Esta seção lista os eventos que pertencem à categoria de pintura e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-233">This section lists events that belong to Painting category and their properties.</span></span>  

| <span data-ttu-id="2b0e1-234">Evento</span><span class="sxs-lookup"><span data-stu-id="2b0e1-234">Event</span></span> | <span data-ttu-id="2b0e1-235">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b0e1-235">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="2b0e1-236">Camadas compostas</span><span class="sxs-lookup"><span data-stu-id="2b0e1-236">Composite Layers</span></span> | <span data-ttu-id="2b0e1-237">As camadas da imagem compostas para o mecanismo de renderização do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-237">The composited image layers for the Microsoft Edge rendering engine.</span></span> |  
| <span data-ttu-id="2b0e1-238">Decodificação de imagem</span><span class="sxs-lookup"><span data-stu-id="2b0e1-238">Image Decode</span></span> | <span data-ttu-id="2b0e1-239">Um recurso de imagem foi decodificado.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-239">An image resource was decoded.</span></span> |  
| <span data-ttu-id="2b0e1-240">Redimensionamento de imagens</span><span class="sxs-lookup"><span data-stu-id="2b0e1-240">Image Resize</span></span> | <span data-ttu-id="2b0e1-241">Uma imagem foi redimensionada a partir de suas dimensões nativas.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-241">An image was resized from its native dimensions.</span></span> |  
| <span data-ttu-id="2b0e1-242">Paint</span><span class="sxs-lookup"><span data-stu-id="2b0e1-242">Paint</span></span> | <span data-ttu-id="2b0e1-243">Camadas compostas foram pintadas para uma região da exibição.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-243">Composited layers were painted to a region of the display.</span></span>  <span data-ttu-id="2b0e1-244">Passar o mouse sobre um registro de pintura realça a região do vídeo que foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-244">Hovering over a Paint record highlights the region of the display that was updated.</span></span> |  

### <span data-ttu-id="2b0e1-245">Propriedades de evento de pintura</span><span class="sxs-lookup"><span data-stu-id="2b0e1-245">Painting event properties</span></span>  

| <span data-ttu-id="2b0e1-246">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2b0e1-246">Property</span></span> | <span data-ttu-id="2b0e1-247">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b0e1-247">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="2b0e1-248">Location</span><span class="sxs-lookup"><span data-stu-id="2b0e1-248">Location</span></span> | <span data-ttu-id="2b0e1-249">Para eventos de pintura, as coordenadas x e y do retângulo de pintura.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-249">For Paint events, the x and y coordinates of the paint rectangle.</span></span> |  
| <span data-ttu-id="2b0e1-250">Dimension</span><span class="sxs-lookup"><span data-stu-id="2b0e1-250">Dimensions</span></span> | <span data-ttu-id="2b0e1-251">Para eventos de pintura, a altura e a largura da região pintada.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-251">For Paint events, the height and width of the painted region.</span></span> |  

## <span data-ttu-id="2b0e1-252">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2b0e1-252">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "tempo-referência da API do console"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd-referência de API do console"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Janela: evento DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope. setInterval () | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope. setTimeout () | MDN"  

> [!NOTE]
> <span data-ttu-id="2b0e1-258">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="2b0e1-258">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2b0e1-259">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) e é criada por [Meggin Kearney][MegginKearney] \ (Tech Writer \) e o [Flavio][FlavioCopes] se encontra \ (desenvolvedor de pilha completa \).</span><span class="sxs-lookup"><span data-stu-id="2b0e1-259">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2b0e1-261">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2b0e1-261">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
