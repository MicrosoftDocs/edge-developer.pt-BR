---
description: O modo de eventos de linha do tempo exibe todos os eventos disparados durante a gravação.  Use a referência de evento da linha do tempo para saber mais sobre cada tipo de evento de linha do tempo.
title: Referência do evento Timeline
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 2a166c9eebc980682fa872e5ee8d213f2058b384
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398662"
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

# <a name="timeline-event-reference"></a><span data-ttu-id="c3e23-105">Referência do evento Timeline</span><span class="sxs-lookup"><span data-stu-id="c3e23-105">Timeline Event reference</span></span>  

<span data-ttu-id="c3e23-106">O modo de eventos de linha do tempo exibe todos os eventos disparados durante a gravação.</span><span class="sxs-lookup"><span data-stu-id="c3e23-106">The timeline events mode displays all events triggered while making a recording.</span></span>  <span data-ttu-id="c3e23-107">Use a referência de evento da linha do tempo para saber mais sobre cada tipo de evento de linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="c3e23-107">Use the timeline event reference to learn more about each timeline event type.</span></span>  

## <a name="common-timeline-event-properties"></a><span data-ttu-id="c3e23-108">Propriedades comuns de eventos de linha do tempo</span><span class="sxs-lookup"><span data-stu-id="c3e23-108">Common timeline event properties</span></span>  

<span data-ttu-id="c3e23-109">Certos detalhes estão presentes em eventos de todos os tipos, enquanto alguns se aplicam apenas a determinados tipos de evento.</span><span class="sxs-lookup"><span data-stu-id="c3e23-109">Certain details are present in events of all types, while some only apply to certain event types.</span></span>  <span data-ttu-id="c3e23-110">Esta seção lista propriedades comuns a tipos de eventos diferentes.</span><span class="sxs-lookup"><span data-stu-id="c3e23-110">This section lists properties common to different event types.</span></span>  <span data-ttu-id="c3e23-111">Propriedades específicas de determinados tipos de evento são listadas nas referências para os tipos de evento a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3e23-111">Properties specific to certain event types are listed in the references for those event types that follow.</span></span>  

| <span data-ttu-id="c3e23-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c3e23-112">Property</span></span> | <span data-ttu-id="c3e23-113">Quando é mostrado</span><span class="sxs-lookup"><span data-stu-id="c3e23-113">When is it shown</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c3e23-114">Tempo agregado</span><span class="sxs-lookup"><span data-stu-id="c3e23-114">Aggregated time</span></span> | <span data-ttu-id="c3e23-115">Para eventos com **eventos aninhados**, o tempo de cada categoria de eventos.</span><span class="sxs-lookup"><span data-stu-id="c3e23-115">For events with **nested events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="c3e23-116">Pilha de chamada</span><span class="sxs-lookup"><span data-stu-id="c3e23-116">Call Stack</span></span> | <span data-ttu-id="c3e23-117">Para eventos com **eventos filho**, o tempo de cada categoria de eventos.</span><span class="sxs-lookup"><span data-stu-id="c3e23-117">For events with **child events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="c3e23-118">Hora da CPU</span><span class="sxs-lookup"><span data-stu-id="c3e23-118">CPU time</span></span> | <span data-ttu-id="c3e23-119">Quanto tempo de CPU o evento gravado levou.</span><span class="sxs-lookup"><span data-stu-id="c3e23-119">How much CPU time the recorded event took.</span></span> |  
| <span data-ttu-id="c3e23-120">Detalhes</span><span class="sxs-lookup"><span data-stu-id="c3e23-120">Details</span></span> | <span data-ttu-id="c3e23-121">Outros detalhes sobre o evento.</span><span class="sxs-lookup"><span data-stu-id="c3e23-121">Other details about the event.</span></span> |  
| <span data-ttu-id="c3e23-122">Duração \(at time-stamp\)</span><span class="sxs-lookup"><span data-stu-id="c3e23-122">Duration \(at time-stamp\)</span></span> | <span data-ttu-id="c3e23-123">Quanto tempo levou para concluir o evento com todos os seus filhos; timestamp é o momento em que o evento ocorreu, em relação ao início da gravação.</span><span class="sxs-lookup"><span data-stu-id="c3e23-123">How long it took the event with all of its children to complete; timestamp is the time at which the event occurred, relative to when the recording started.</span></span> |  
| <span data-ttu-id="c3e23-124">Auto-tempo</span><span class="sxs-lookup"><span data-stu-id="c3e23-124">Self time</span></span> | <span data-ttu-id="c3e23-125">Quanto tempo o evento demorou sem nenhum de seus filhos.</span><span class="sxs-lookup"><span data-stu-id="c3e23-125">How long the event took without any of its children.</span></span> |  
| <span data-ttu-id="c3e23-126">Tamanho da pilha usado</span><span class="sxs-lookup"><span data-stu-id="c3e23-126">Used Heap Size</span></span> | <span data-ttu-id="c3e23-127">Quantidade de memória sendo usada pelo aplicativo quando o evento foi gravado e a alteração delta \(+/-\) no tamanho de pilha usado desde a última amostragem.</span><span class="sxs-lookup"><span data-stu-id="c3e23-127">Amount of memory being used by the application when the event was recorded, and the delta \(+/-\) change in used heap size since the last sampling.</span></span> |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <a name="loading-events"></a><span data-ttu-id="c3e23-128">Carregando eventos</span><span class="sxs-lookup"><span data-stu-id="c3e23-128">Loading events</span></span>  

<span data-ttu-id="c3e23-129">Esta seção lista eventos que pertencem à categoria Loading e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c3e23-129">This section lists events that belong to Loading category and their properties.</span></span>  

| <span data-ttu-id="c3e23-130">Evento</span><span class="sxs-lookup"><span data-stu-id="c3e23-130">Event</span></span> | <span data-ttu-id="c3e23-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3e23-131">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c3e23-132">HTML de análise</span><span class="sxs-lookup"><span data-stu-id="c3e23-132">Parse HTML</span></span> |  <span data-ttu-id="c3e23-133">O Microsoft Edge correu o algoritmo de análise HTML.</span><span class="sxs-lookup"><span data-stu-id="c3e23-133">Microsoft Edge ran the HTML parsing algorithm.</span></span> |  
| <span data-ttu-id="c3e23-134">Concluir o carregamento</span><span class="sxs-lookup"><span data-stu-id="c3e23-134">Finish Loading</span></span> |  <span data-ttu-id="c3e23-135">Uma solicitação de rede concluída.</span><span class="sxs-lookup"><span data-stu-id="c3e23-135">A network request completed.</span></span> |  
| <span data-ttu-id="c3e23-136">Receber Dados</span><span class="sxs-lookup"><span data-stu-id="c3e23-136">Receive Data</span></span> |  <span data-ttu-id="c3e23-137">Os dados de uma solicitação foram recebidos.</span><span class="sxs-lookup"><span data-stu-id="c3e23-137">Data for a request was received.</span></span>  <span data-ttu-id="c3e23-138">Há um ou mais eventos De recebimento de dados.</span><span class="sxs-lookup"><span data-stu-id="c3e23-138">There are one or more Receive Data events.</span></span> |  
| <span data-ttu-id="c3e23-139">Receber Resposta</span><span class="sxs-lookup"><span data-stu-id="c3e23-139">Receive Response</span></span> |  <span data-ttu-id="c3e23-140">A resposta HTTP inicial de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="c3e23-140">The initial HTTP response from a request.</span></span> |  
| <span data-ttu-id="c3e23-141">Enviar Solicitação</span><span class="sxs-lookup"><span data-stu-id="c3e23-141">Send Request</span></span> |  <span data-ttu-id="c3e23-142">Uma solicitação de rede foi enviada.</span><span class="sxs-lookup"><span data-stu-id="c3e23-142">A network request has been sent.</span></span> |  

### <a name="loading-event-properties"></a><span data-ttu-id="c3e23-143">Carregando propriedades de evento</span><span class="sxs-lookup"><span data-stu-id="c3e23-143">Loading event properties</span></span>  

| <span data-ttu-id="c3e23-144">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c3e23-144">Property</span></span> | <span data-ttu-id="c3e23-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3e23-145">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c3e23-146">Recurso</span><span class="sxs-lookup"><span data-stu-id="c3e23-146">Resource</span></span> | <span data-ttu-id="c3e23-147">A URL do recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="c3e23-147">The URL of the requested resource.</span></span> |  
| <span data-ttu-id="c3e23-148">Visualização</span><span class="sxs-lookup"><span data-stu-id="c3e23-148">Preview</span></span> | <span data-ttu-id="c3e23-149">Visualização do recurso solicitado \(somente imagens\).</span><span class="sxs-lookup"><span data-stu-id="c3e23-149">Preview of the requested resource \(images only\).</span></span> |  
| <span data-ttu-id="c3e23-150">Método Request</span><span class="sxs-lookup"><span data-stu-id="c3e23-150">Request Method</span></span> | <span data-ttu-id="c3e23-151">Método HTTP usado para a solicitação \( `GET` ou `POST` , por exemplo\).</span><span class="sxs-lookup"><span data-stu-id="c3e23-151">HTTP method used for the request \(`GET` or `POST`, for example\).</span></span> |  
| <span data-ttu-id="c3e23-152">Código de Status</span><span class="sxs-lookup"><span data-stu-id="c3e23-152">Status Code</span></span> | <span data-ttu-id="c3e23-153">Código de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="c3e23-153">HTTP response code.</span></span> |  
| <span data-ttu-id="c3e23-154">Tipo MIME</span><span class="sxs-lookup"><span data-stu-id="c3e23-154">MIME Type</span></span> | <span data-ttu-id="c3e23-155">Tipo MIME do recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="c3e23-155">MIME type of the requested resource.</span></span> |  
| <span data-ttu-id="c3e23-156">Comprimento de dados codificados</span><span class="sxs-lookup"><span data-stu-id="c3e23-156">Encoded Data Length</span></span> | <span data-ttu-id="c3e23-157">Comprimento do recurso solicitado em bytes.</span><span class="sxs-lookup"><span data-stu-id="c3e23-157">Length of requested resource in bytes.</span></span> |  

## <a name="scripting-events"></a><span data-ttu-id="c3e23-158">Eventos de script</span><span class="sxs-lookup"><span data-stu-id="c3e23-158">Scripting events</span></span>  

<span data-ttu-id="c3e23-159">Esta seção lista eventos que pertencem à categoria Scripting e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c3e23-159">This section lists events that belong to the Scripting category and their properties.</span></span>  

| <span data-ttu-id="c3e23-160">Evento</span><span class="sxs-lookup"><span data-stu-id="c3e23-160">Event</span></span> | <span data-ttu-id="c3e23-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3e23-161">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c3e23-162">Quadro de animação disparado</span><span class="sxs-lookup"><span data-stu-id="c3e23-162">Animation Frame Fired</span></span> | <span data-ttu-id="c3e23-163">Um quadro de animação agendado disparado e seu manipulador de retorno de chamada invocado.</span><span class="sxs-lookup"><span data-stu-id="c3e23-163">A scheduled animation frame fired, and its callback handler invoked.</span></span> |  
| <span data-ttu-id="c3e23-164">Cancelar Quadro de Animação</span><span class="sxs-lookup"><span data-stu-id="c3e23-164">Cancel Animation Frame</span></span> |  <span data-ttu-id="c3e23-165">Um quadro de animação agendado foi cancelado.</span><span class="sxs-lookup"><span data-stu-id="c3e23-165">A scheduled animation frame was canceled.</span></span> |  
| <span data-ttu-id="c3e23-166">Evento GC</span><span class="sxs-lookup"><span data-stu-id="c3e23-166">GC Event</span></span> |  <span data-ttu-id="c3e23-167">Coleta de lixo ocorreu.</span><span class="sxs-lookup"><span data-stu-id="c3e23-167">Garbage collection occurred.</span></span> |  
| <span data-ttu-id="c3e23-168">DOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="c3e23-168">DOMContentLoaded</span></span> |  <span data-ttu-id="c3e23-169">O [evento DOMContentLoaded][MDNWindowDOMContentLoadedEvent] foi disparado pelo navegador.</span><span class="sxs-lookup"><span data-stu-id="c3e23-169">The [DOMContentLoaded event][MDNWindowDOMContentLoadedEvent] was fired by the browser.</span></span>  <span data-ttu-id="c3e23-170">Esse evento é acionado quando todo o conteúdo DOM da página é carregado e analisado.</span><span class="sxs-lookup"><span data-stu-id="c3e23-170">This event is fired when all of the DOM content of the page is loaded and parsed.</span></span> |  
| <span data-ttu-id="c3e23-171">Avaliar Script</span><span class="sxs-lookup"><span data-stu-id="c3e23-171">Evaluate Script</span></span> | <span data-ttu-id="c3e23-172">Um script foi avaliado.</span><span class="sxs-lookup"><span data-stu-id="c3e23-172">A script was evaluated.</span></span> |  
| <span data-ttu-id="c3e23-173">Evento</span><span class="sxs-lookup"><span data-stu-id="c3e23-173">Event</span></span> | <span data-ttu-id="c3e23-174">Um evento JavaScript \(por exemplo, `mousedown` , ou `key` \).</span><span class="sxs-lookup"><span data-stu-id="c3e23-174">A JavaScript event \(for example, `mousedown`, or `key`\).</span></span> |  
| <span data-ttu-id="c3e23-175">Chamada de função</span><span class="sxs-lookup"><span data-stu-id="c3e23-175">Function Call</span></span> | <span data-ttu-id="c3e23-176">Uma chamada de função JavaScript de nível superior foi feita \(somente aparece quando o navegador entra no mecanismo JavaScript\).</span><span class="sxs-lookup"><span data-stu-id="c3e23-176">A top-level JavaScript function call was made \(only appears when browser enters JavaScript engine\).</span></span> |  
| <span data-ttu-id="c3e23-177">Instalar Timer</span><span class="sxs-lookup"><span data-stu-id="c3e23-177">Install Timer</span></span> | <span data-ttu-id="c3e23-178">Um timer foi criado com [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] ou [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span><span class="sxs-lookup"><span data-stu-id="c3e23-178">A timer was created with [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] or [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span></span> |  
| <span data-ttu-id="c3e23-179">Quadro de animação de solicitação</span><span class="sxs-lookup"><span data-stu-id="c3e23-179">Request Animation Frame</span></span> | <span data-ttu-id="c3e23-180">Uma `requestAnimationFrame()` chamada agendou um novo quadro.</span><span class="sxs-lookup"><span data-stu-id="c3e23-180">A `requestAnimationFrame()` call scheduled a new frame.</span></span> |  
| <span data-ttu-id="c3e23-181">Remover Timer</span><span class="sxs-lookup"><span data-stu-id="c3e23-181">Remove Timer</span></span> | <span data-ttu-id="c3e23-182">Um temporizador criado anteriormente foi limpo.</span><span class="sxs-lookup"><span data-stu-id="c3e23-182">A previously created timer was cleared.</span></span> |  
| <span data-ttu-id="c3e23-183">Hora</span><span class="sxs-lookup"><span data-stu-id="c3e23-183">Time</span></span> |  <span data-ttu-id="c3e23-184">Um script chamado [console.time()][ConsoleApiTime].</span><span class="sxs-lookup"><span data-stu-id="c3e23-184">A script called [console.time()][ConsoleApiTime].</span></span> |  
| <span data-ttu-id="c3e23-185">Fim do Tempo</span><span class="sxs-lookup"><span data-stu-id="c3e23-185">Time End</span></span> | <span data-ttu-id="c3e23-186">Um script chamado [console.timeEnd()][ConsoleApiTimeEnd].</span><span class="sxs-lookup"><span data-stu-id="c3e23-186">A script called [console.timeEnd()][ConsoleApiTimeEnd].</span></span> |  
| <span data-ttu-id="c3e23-187">Timer acionado</span><span class="sxs-lookup"><span data-stu-id="c3e23-187">Timer Fired</span></span> | <span data-ttu-id="c3e23-188">Um timer disparado que foi agendado `setInterval()` com ou `setTimeout()` .</span><span class="sxs-lookup"><span data-stu-id="c3e23-188">A timer fired that was scheduled with `setInterval()` or `setTimeout()`.</span></span> |  
| <span data-ttu-id="c3e23-189">Alteração de estado pronto XHR</span><span class="sxs-lookup"><span data-stu-id="c3e23-189">XHR Ready State Change</span></span> | <span data-ttu-id="c3e23-190">O estado pronto de um XMLHTTPRequest foi alterado.</span><span class="sxs-lookup"><span data-stu-id="c3e23-190">The ready state of an XMLHTTPRequest changed.</span></span> |  
| <span data-ttu-id="c3e23-191">Carga XHR</span><span class="sxs-lookup"><span data-stu-id="c3e23-191">XHR Load</span></span> | <span data-ttu-id="c3e23-192">Um `XMLHTTPRequest` carregamento concluído.</span><span class="sxs-lookup"><span data-stu-id="c3e23-192">An `XMLHTTPRequest` finished loading.</span></span> |  

### <a name="scripting-event-properties"></a><span data-ttu-id="c3e23-193">Propriedades do evento Scripting</span><span class="sxs-lookup"><span data-stu-id="c3e23-193">Scripting event properties</span></span>  

| <span data-ttu-id="c3e23-194">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c3e23-194">Property</span></span> | <span data-ttu-id="c3e23-195">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3e23-195">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c3e23-196">Timer ID</span><span class="sxs-lookup"><span data-stu-id="c3e23-196">Timer ID</span></span> | <span data-ttu-id="c3e23-197">A ID do timer.</span><span class="sxs-lookup"><span data-stu-id="c3e23-197">The timer ID.</span></span> |  
| <span data-ttu-id="c3e23-198">Tempo limite</span><span class="sxs-lookup"><span data-stu-id="c3e23-198">Timeout</span></span> | <span data-ttu-id="c3e23-199">O tempo de tempo especificado pelo temporizador.</span><span class="sxs-lookup"><span data-stu-id="c3e23-199">The timeout specified by the timer.</span></span> |  
| <span data-ttu-id="c3e23-200">Repetições</span><span class="sxs-lookup"><span data-stu-id="c3e23-200">Repeats</span></span> | <span data-ttu-id="c3e23-201">Boolean que especifica se o temporizador se repete.</span><span class="sxs-lookup"><span data-stu-id="c3e23-201">Boolean that specifies if the timer repeats.</span></span> |  
| <span data-ttu-id="c3e23-202">Chamada de função</span><span class="sxs-lookup"><span data-stu-id="c3e23-202">Function Call</span></span> | <span data-ttu-id="c3e23-203">Uma função que foi invocada.</span><span class="sxs-lookup"><span data-stu-id="c3e23-203">A function that was invoked.</span></span> |  

## <a name="rendering-events"></a><span data-ttu-id="c3e23-204">Eventos de renderização</span><span class="sxs-lookup"><span data-stu-id="c3e23-204">Rendering events</span></span>  

<span data-ttu-id="c3e23-205">Esta seção lista eventos que pertencem à categoria Rendering e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c3e23-205">This section lists events that belong to Rendering category and their properties.</span></span>  

| <span data-ttu-id="c3e23-206">Evento</span><span class="sxs-lookup"><span data-stu-id="c3e23-206">Event</span></span> | <span data-ttu-id="c3e23-207">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3e23-207">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c3e23-208">Layout inválido</span><span class="sxs-lookup"><span data-stu-id="c3e23-208">Invalidate layout</span></span> | <span data-ttu-id="c3e23-209">O layout da página foi invalidado por uma alteração dom.</span><span class="sxs-lookup"><span data-stu-id="c3e23-209">The page layout was invalidated by a DOM change.</span></span> |  
| <span data-ttu-id="c3e23-210">Layout</span><span class="sxs-lookup"><span data-stu-id="c3e23-210">Layout</span></span> | <span data-ttu-id="c3e23-211">Um layout de página foi concluído.</span><span class="sxs-lookup"><span data-stu-id="c3e23-211">A page layout was completed.</span></span> |  
| <span data-ttu-id="c3e23-212">Estilo recalcular</span><span class="sxs-lookup"><span data-stu-id="c3e23-212">Recalculate style</span></span> | <span data-ttu-id="c3e23-213">Estilos de elemento recalculados do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c3e23-213">Microsoft Edge recalculated element styles.</span></span> |  
| <span data-ttu-id="c3e23-214">Rolagem</span><span class="sxs-lookup"><span data-stu-id="c3e23-214">Scroll</span></span> | <span data-ttu-id="c3e23-215">O conteúdo do exibição aninhado foi rolado.</span><span class="sxs-lookup"><span data-stu-id="c3e23-215">The content of nested view was scrolled.</span></span> |  

### <a name="rendering-event-properties"></a><span data-ttu-id="c3e23-216">Propriedades de evento de renderização</span><span class="sxs-lookup"><span data-stu-id="c3e23-216">Rendering event properties</span></span>  

| <span data-ttu-id="c3e23-217">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c3e23-217">Property</span></span> | <span data-ttu-id="c3e23-218">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3e23-218">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c3e23-219">Layout invalidado</span><span class="sxs-lookup"><span data-stu-id="c3e23-219">Layout invalidated</span></span> | <span data-ttu-id="c3e23-220">Para registros de Layout, o rastreamento de pilha do código que fez com que o layout fosse invalidado.</span><span class="sxs-lookup"><span data-stu-id="c3e23-220">For Layout records, the stack trace of the code that caused the layout to be invalidated.</span></span> |  
| <span data-ttu-id="c3e23-221">Nós que precisam de layout</span><span class="sxs-lookup"><span data-stu-id="c3e23-221">Nodes that need layout</span></span> | <span data-ttu-id="c3e23-222">Para registros de Layout, o número de nós que foram marcados como layout necessário antes do retransmissão ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="c3e23-222">For Layout records, the number of nodes that were marked as needing layout before the relayout started.</span></span>  <span data-ttu-id="c3e23-223">Esses são normalmente os nós que foram invalidados pelo código do desenvolvedor, além de um caminho para cima para raiz de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="c3e23-223">These are normally those nodes that were invalidated by developer code, plus a path upward to relayout root.</span></span> |  
| <span data-ttu-id="c3e23-224">Tamanho da árvore de layout</span><span class="sxs-lookup"><span data-stu-id="c3e23-224">Layout tree size</span></span> | <span data-ttu-id="c3e23-225">Para registros de Layout, o número total de nós sob a raiz de retransmissão \(o nó que o Microsoft Edge inicia o retransmissão\).</span><span class="sxs-lookup"><span data-stu-id="c3e23-225">For Layout records, the total number of nodes under the relayout root \(the node that Microsoft Edge starts the relayout\).</span></span> |  
| <span data-ttu-id="c3e23-226">Escopo de layout</span><span class="sxs-lookup"><span data-stu-id="c3e23-226">Layout scope</span></span> | <span data-ttu-id="c3e23-227">Os valores `Partial` possíveis são \(o limite de layout de novo é uma parte do DOM\) ou `Whole document` .</span><span class="sxs-lookup"><span data-stu-id="c3e23-227">Possible values are `Partial` \(the re-layout boundary is a portion of the DOM\) or `Whole document`.</span></span> |  
| <span data-ttu-id="c3e23-228">Elementos afetados</span><span class="sxs-lookup"><span data-stu-id="c3e23-228">Elements affected</span></span> | <span data-ttu-id="c3e23-229">Para registros de estilo recalculado, o número de elementos afetados por um recálculo de estilo.</span><span class="sxs-lookup"><span data-stu-id="c3e23-229">For Recalculate style records, the number of elements affected by a style recalculation.</span></span> |  
| <span data-ttu-id="c3e23-230">Estilos invalidados</span><span class="sxs-lookup"><span data-stu-id="c3e23-230">Styles invalidated</span></span> | <span data-ttu-id="c3e23-231">Para registros de estilo recalculado, fornece o rastreamento de pilha do código que causou a invalidação do estilo.</span><span class="sxs-lookup"><span data-stu-id="c3e23-231">For Recalculate style records, provides the stack trace of the code that caused the style invalidation.</span></span> |  

## <a name="painting-events"></a><span data-ttu-id="c3e23-232">Eventos de pintura</span><span class="sxs-lookup"><span data-stu-id="c3e23-232">Painting events</span></span>  

<span data-ttu-id="c3e23-233">Esta seção lista eventos que pertencem à categoria Painting e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c3e23-233">This section lists events that belong to Painting category and their properties.</span></span>  

| <span data-ttu-id="c3e23-234">Evento</span><span class="sxs-lookup"><span data-stu-id="c3e23-234">Event</span></span> | <span data-ttu-id="c3e23-235">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3e23-235">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c3e23-236">Camadas compostas</span><span class="sxs-lookup"><span data-stu-id="c3e23-236">Composite Layers</span></span> | <span data-ttu-id="c3e23-237">As camadas de imagem compostas para o mecanismo de renderização do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c3e23-237">The composited image layers for the Microsoft Edge rendering engine.</span></span> |  
| <span data-ttu-id="c3e23-238">Decodificar imagem</span><span class="sxs-lookup"><span data-stu-id="c3e23-238">Image Decode</span></span> | <span data-ttu-id="c3e23-239">Um recurso de imagem foi decodificado.</span><span class="sxs-lookup"><span data-stu-id="c3e23-239">An image resource was decoded.</span></span> |  
| <span data-ttu-id="c3e23-240">Resize de imagem</span><span class="sxs-lookup"><span data-stu-id="c3e23-240">Image Resize</span></span> | <span data-ttu-id="c3e23-241">Uma imagem foi resized de suas dimensões nativas.</span><span class="sxs-lookup"><span data-stu-id="c3e23-241">An image was resized from its native dimensions.</span></span> |  
| <span data-ttu-id="c3e23-242">Paint</span><span class="sxs-lookup"><span data-stu-id="c3e23-242">Paint</span></span> | <span data-ttu-id="c3e23-243">Camadas compostas foram pintadas para uma região da exibição.</span><span class="sxs-lookup"><span data-stu-id="c3e23-243">Composited layers were painted to a region of the display.</span></span>  <span data-ttu-id="c3e23-244">Passar o mouse sobre um registro Paint realça a região da exibição que foi atualizada.</span><span class="sxs-lookup"><span data-stu-id="c3e23-244">Hovering over a Paint record highlights the region of the display that was updated.</span></span> |  

### <a name="painting-event-properties"></a><span data-ttu-id="c3e23-245">Propriedades do evento Painting</span><span class="sxs-lookup"><span data-stu-id="c3e23-245">Painting event properties</span></span>  

| <span data-ttu-id="c3e23-246">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c3e23-246">Property</span></span> | <span data-ttu-id="c3e23-247">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3e23-247">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="c3e23-248">Location</span><span class="sxs-lookup"><span data-stu-id="c3e23-248">Location</span></span> | <span data-ttu-id="c3e23-249">Para eventos Paint, as coordenadas x e y do retângulo de tinta.</span><span class="sxs-lookup"><span data-stu-id="c3e23-249">For Paint events, the x and y coordinates of the paint rectangle.</span></span> |  
| <span data-ttu-id="c3e23-250">Dimensões</span><span class="sxs-lookup"><span data-stu-id="c3e23-250">Dimensions</span></span> | <span data-ttu-id="c3e23-251">Para eventos Paint, a altura e a largura da região pintada.</span><span class="sxs-lookup"><span data-stu-id="c3e23-251">For Paint events, the height and width of the painted region.</span></span> |  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c3e23-252">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c3e23-252">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "time - Referência da API de Console"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd - Referência da API de Console"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Janela: evento DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope.setInterval() | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope.setTimeout() | MDN"  

> [!NOTE]
> <span data-ttu-id="c3e23-258">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c3e23-258">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c3e23-259">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) e é de autoria de [Meggin Kearney][MegginKearney] \(Tech Writer\) e [Flávio Copes][FlavioCopes] \(Desenvolvedor de Pilha Completa\).</span><span class="sxs-lookup"><span data-stu-id="c3e23-259">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c3e23-261">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c3e23-261">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
