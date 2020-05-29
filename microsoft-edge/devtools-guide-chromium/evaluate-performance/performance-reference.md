---
title: Referência do evento Timeline
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: e5f0807204877ce034fd52ea4535795ea80ba394
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611717"
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





# <span data-ttu-id="8e243-103">Referência do evento Timeline</span><span class="sxs-lookup"><span data-stu-id="8e243-103">Timeline Event Reference</span></span>   




<span data-ttu-id="8e243-104">O modo de eventos de linha do tempo exibe todos os eventos disparados ao criar uma gravação.</span><span class="sxs-lookup"><span data-stu-id="8e243-104">The timeline events mode displays all events triggered while making a recording.</span></span>  <span data-ttu-id="8e243-105">Use a referência de evento Timeline para saber mais sobre cada tipo de evento de linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="8e243-105">Use the timeline event reference to learn more about each timeline event type.</span></span>  

## <span data-ttu-id="8e243-106">Propriedades de eventos comuns da linha do tempo</span><span class="sxs-lookup"><span data-stu-id="8e243-106">Common timeline event properties</span></span>  

<span data-ttu-id="8e243-107">Alguns detalhes estão presentes em eventos de todos os tipos, enquanto alguns só se aplicam a determinados tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="8e243-107">Certain details are present in events of all types, while some only apply to certain event types.</span></span>  <span data-ttu-id="8e243-108">Esta seção lista as propriedades comuns a diferentes tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="8e243-108">This section lists properties common to different event types.</span></span>  <span data-ttu-id="8e243-109">As propriedades específicas para determinados tipos de eventos são listadas nas referências para os tipos de eventos que se seguem.</span><span class="sxs-lookup"><span data-stu-id="8e243-109">Properties specific to certain event types are listed in the references for those event types that follow.</span></span>  

| <span data-ttu-id="8e243-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8e243-110">Property</span></span> | <span data-ttu-id="8e243-111">Quando é exibido</span><span class="sxs-lookup"><span data-stu-id="8e243-111">When is it shown</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e243-112">Tempo agregado</span><span class="sxs-lookup"><span data-stu-id="8e243-112">Aggregated time</span></span> | <span data-ttu-id="8e243-113">Para eventos com **eventos aninhados**, o tempo usado por cada categoria de eventos.</span><span class="sxs-lookup"><span data-stu-id="8e243-113">For events with **nested events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="8e243-114">Pilha de chamadas</span><span class="sxs-lookup"><span data-stu-id="8e243-114">Call Stack</span></span> | <span data-ttu-id="8e243-115">Para eventos com **eventos filho**, o tempo usado por cada categoria de eventos.</span><span class="sxs-lookup"><span data-stu-id="8e243-115">For events with **child events**, the time taken by each category of events.</span></span> |  
| <span data-ttu-id="8e243-116">Tempo de CPU</span><span class="sxs-lookup"><span data-stu-id="8e243-116">CPU time</span></span> | <span data-ttu-id="8e243-117">Quanto tempo da CPU o evento registrado levou.</span><span class="sxs-lookup"><span data-stu-id="8e243-117">How much CPU time the recorded event took.</span></span> |  
| <span data-ttu-id="8e243-118">Detalhes</span><span class="sxs-lookup"><span data-stu-id="8e243-118">Details</span></span> | <span data-ttu-id="8e243-119">Outros detalhes sobre o evento.</span><span class="sxs-lookup"><span data-stu-id="8e243-119">Other details about the event.</span></span> |  
| <span data-ttu-id="8e243-120">Duration \ (no carimbo de data/hora \)</span><span class="sxs-lookup"><span data-stu-id="8e243-120">Duration \(at time-stamp\)</span></span> | <span data-ttu-id="8e243-121">Quanto tempo levava o evento com todos os seus filhos a concluir; carimbo de data/hora é o horário em que o evento ocorreu em relação ao início da gravação.</span><span class="sxs-lookup"><span data-stu-id="8e243-121">How long it took the event with all of its children to complete; timestamp is the time at which the event occurred, relative to when the recording started.</span></span> |  
| <span data-ttu-id="8e243-122">Tempo de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="8e243-122">Self time</span></span> | <span data-ttu-id="8e243-123">Por quanto tempo o evento demorou sem qualquer um de seus filhos.</span><span class="sxs-lookup"><span data-stu-id="8e243-123">How long the event took without any of its children.</span></span> |  
| <span data-ttu-id="8e243-124">Tamanho de heap usado</span><span class="sxs-lookup"><span data-stu-id="8e243-124">Used Heap Size</span></span> | <span data-ttu-id="8e243-125">A quantidade de memória que está sendo usada pelo aplicativo quando o evento foi gravado, e a alteração de \ (+/-\) do Delta é usada em tamanho de heap usado desde a última amostragem.</span><span class="sxs-lookup"><span data-stu-id="8e243-125">Amount of memory being used by the application when the event was recorded, and the delta \(+/-\) change in used heap size since the last sampling.</span></span> |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <span data-ttu-id="8e243-126">Carregando eventos</span><span class="sxs-lookup"><span data-stu-id="8e243-126">Loading events</span></span>  

<span data-ttu-id="8e243-127">Esta seção lista os eventos que pertencem à categoria de carregamento e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8e243-127">This section lists events that belong to Loading category and their properties.</span></span>  

| <span data-ttu-id="8e243-128">Evento</span><span class="sxs-lookup"><span data-stu-id="8e243-128">Event</span></span> | <span data-ttu-id="8e243-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e243-129">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e243-130">Analisar HTML</span><span class="sxs-lookup"><span data-stu-id="8e243-130">Parse HTML</span></span> |  <span data-ttu-id="8e243-131">O Microsoft Edge executou o algoritmo de análise HTML.</span><span class="sxs-lookup"><span data-stu-id="8e243-131">Microsoft Edge ran the HTML parsing algorithm.</span></span> |  
| <span data-ttu-id="8e243-132">Concluir o carregamento</span><span class="sxs-lookup"><span data-stu-id="8e243-132">Finish Loading</span></span> |  <span data-ttu-id="8e243-133">Uma solicitação de rede foi concluída.</span><span class="sxs-lookup"><span data-stu-id="8e243-133">A network request completed.</span></span> |  
| <span data-ttu-id="8e243-134">Receber dados</span><span class="sxs-lookup"><span data-stu-id="8e243-134">Receive Data</span></span> |  <span data-ttu-id="8e243-135">Os dados de uma solicitação foram recebidos.</span><span class="sxs-lookup"><span data-stu-id="8e243-135">Data for a request was received.</span></span>  <span data-ttu-id="8e243-136">Há um ou mais eventos de recebimento de dados.</span><span class="sxs-lookup"><span data-stu-id="8e243-136">There are one or more Receive Data events.</span></span> |  
| <span data-ttu-id="8e243-137">Receber resposta</span><span class="sxs-lookup"><span data-stu-id="8e243-137">Receive Response</span></span> |  <span data-ttu-id="8e243-138">A resposta HTTP inicial de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="8e243-138">The initial HTTP response from a request.</span></span> |  
| <span data-ttu-id="8e243-139">Enviar solicitação</span><span class="sxs-lookup"><span data-stu-id="8e243-139">Send Request</span></span> |  <span data-ttu-id="8e243-140">Uma solicitação de rede foi enviada.</span><span class="sxs-lookup"><span data-stu-id="8e243-140">A network request has been sent.</span></span> |  

### <span data-ttu-id="8e243-141">Carregando Propriedades do evento</span><span class="sxs-lookup"><span data-stu-id="8e243-141">Loading event properties</span></span>  

| <span data-ttu-id="8e243-142">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8e243-142">Property</span></span> | <span data-ttu-id="8e243-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e243-143">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e243-144">Recurso</span><span class="sxs-lookup"><span data-stu-id="8e243-144">Resource</span></span> | <span data-ttu-id="8e243-145">A URL do recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="8e243-145">The URL of the requested resource.</span></span> |  
| <span data-ttu-id="8e243-146">Visualização</span><span class="sxs-lookup"><span data-stu-id="8e243-146">Preview</span></span> | <span data-ttu-id="8e243-147">Visualização do recurso solicitado \ (apenas imagens \).</span><span class="sxs-lookup"><span data-stu-id="8e243-147">Preview of the requested resource \(images only\).</span></span> |  
| <span data-ttu-id="8e243-148">Método de solicitação</span><span class="sxs-lookup"><span data-stu-id="8e243-148">Request Method</span></span> | <span data-ttu-id="8e243-149">Método HTTP usado para a solicitação \ ( `GET` ou `POST` , por exemplo, \).</span><span class="sxs-lookup"><span data-stu-id="8e243-149">HTTP method used for the request \(`GET` or `POST`, for example\).</span></span> |  
| <span data-ttu-id="8e243-150">Código de status</span><span class="sxs-lookup"><span data-stu-id="8e243-150">Status Code</span></span> | <span data-ttu-id="8e243-151">Código de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="8e243-151">HTTP response code.</span></span> |  
| <span data-ttu-id="8e243-152">Tipo MIME</span><span class="sxs-lookup"><span data-stu-id="8e243-152">MIME Type</span></span> | <span data-ttu-id="8e243-153">Tipo MIME do recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="8e243-153">MIME type of the requested resource.</span></span> |  
| <span data-ttu-id="8e243-154">Comprimento de dados codificados</span><span class="sxs-lookup"><span data-stu-id="8e243-154">Encoded Data Length</span></span> | <span data-ttu-id="8e243-155">Comprimento do recurso solicitado em bytes.</span><span class="sxs-lookup"><span data-stu-id="8e243-155">Length of requested resource in bytes.</span></span> |  

## <span data-ttu-id="8e243-156">Eventos de script</span><span class="sxs-lookup"><span data-stu-id="8e243-156">Scripting events</span></span>  

<span data-ttu-id="8e243-157">Esta seção lista os eventos que pertencem à categoria de script e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8e243-157">This section lists events that belong to the Scripting category and their properties.</span></span>  

| <span data-ttu-id="8e243-158">Evento</span><span class="sxs-lookup"><span data-stu-id="8e243-158">Event</span></span> | <span data-ttu-id="8e243-159">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e243-159">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e243-160">Quadro de animação acionado</span><span class="sxs-lookup"><span data-stu-id="8e243-160">Animation Frame Fired</span></span> | <span data-ttu-id="8e243-161">Um quadro de animação programado foi acionado, e seu manipulador de retorno de chamada foi invocado.</span><span class="sxs-lookup"><span data-stu-id="8e243-161">A scheduled animation frame fired, and its callback handler invoked.</span></span> |  
| <span data-ttu-id="8e243-162">Cancelar quadro de animação</span><span class="sxs-lookup"><span data-stu-id="8e243-162">Cancel Animation Frame</span></span> |  <span data-ttu-id="8e243-163">Um quadro de animação agendado foi cancelado.</span><span class="sxs-lookup"><span data-stu-id="8e243-163">A scheduled animation frame was canceled.</span></span> |  
| <span data-ttu-id="8e243-164">Evento GC</span><span class="sxs-lookup"><span data-stu-id="8e243-164">GC Event</span></span> |  <span data-ttu-id="8e243-165">Ocorreu uma coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="8e243-165">Garbage collection occurred.</span></span> |  
| <span data-ttu-id="8e243-166">DOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="8e243-166">DOMContentLoaded</span></span> |  <span data-ttu-id="8e243-167">O [evento DOMContentLoaded][MDNWindowDOMContentLoadedEvent] foi acionado pelo navegador.</span><span class="sxs-lookup"><span data-stu-id="8e243-167">The [DOMContentLoaded event][MDNWindowDOMContentLoadedEvent] was fired by the browser.</span></span>  <span data-ttu-id="8e243-168">Esse evento é acionado quando todo o conteúdo DOM da página é carregado e analisado.</span><span class="sxs-lookup"><span data-stu-id="8e243-168">This event is fired when all of the page's DOM content has been loaded and parsed.</span></span> |  
| <span data-ttu-id="8e243-169">Avaliar o script</span><span class="sxs-lookup"><span data-stu-id="8e243-169">Evaluate Script</span></span> | <span data-ttu-id="8e243-170">Um script foi avaliado.</span><span class="sxs-lookup"><span data-stu-id="8e243-170">A script was evaluated.</span></span> |  
| <span data-ttu-id="8e243-171">Evento</span><span class="sxs-lookup"><span data-stu-id="8e243-171">Event</span></span> | <span data-ttu-id="8e243-172">Um evento JavaScript \ (por exemplo, `mousedown` , ou `key` \).</span><span class="sxs-lookup"><span data-stu-id="8e243-172">A JavaScript event \(for example, `mousedown`, or `key`\).</span></span> |  
| <span data-ttu-id="8e243-173">Chamada de função</span><span class="sxs-lookup"><span data-stu-id="8e243-173">Function Call</span></span> | <span data-ttu-id="8e243-174">Uma chamada de função JavaScript de nível superior foi feita \ (só aparece quando o navegador entra no mecanismo JavaScript \).</span><span class="sxs-lookup"><span data-stu-id="8e243-174">A top-level JavaScript function call was made \(only appears when browser enters JavaScript engine\).</span></span> |  
| <span data-ttu-id="8e243-175">Temporizador de instalação</span><span class="sxs-lookup"><span data-stu-id="8e243-175">Install Timer</span></span> | <span data-ttu-id="8e243-176">Um temporizador foi criado com [setInterval ()][MDNWindowOrWorkerGlobalScopeSetInterval] ou [setTimeout ()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span><span class="sxs-lookup"><span data-stu-id="8e243-176">A timer was created with [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] or [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout].</span></span> |  
| <span data-ttu-id="8e243-177">Quadro de animação de solicitação</span><span class="sxs-lookup"><span data-stu-id="8e243-177">Request Animation Frame</span></span> | <span data-ttu-id="8e243-178">Uma `requestAnimationFrame()` chamada agendou um novo quadro.</span><span class="sxs-lookup"><span data-stu-id="8e243-178">A `requestAnimationFrame()` call scheduled a new frame.</span></span> |  
| <span data-ttu-id="8e243-179">Remover temporizador</span><span class="sxs-lookup"><span data-stu-id="8e243-179">Remove Timer</span></span> | <span data-ttu-id="8e243-180">Um temporizador criado anteriormente foi limpo.</span><span class="sxs-lookup"><span data-stu-id="8e243-180">A previously created timer was cleared.</span></span> |  
| <span data-ttu-id="8e243-181">Hora</span><span class="sxs-lookup"><span data-stu-id="8e243-181">Time</span></span> |  <span data-ttu-id="8e243-182">Um script chamado [console. time ()][ConsoleApiTime].</span><span class="sxs-lookup"><span data-stu-id="8e243-182">A script called [console.time()][ConsoleApiTime].</span></span> |  
| <span data-ttu-id="8e243-183">Término do tempo</span><span class="sxs-lookup"><span data-stu-id="8e243-183">Time End</span></span> | <span data-ttu-id="8e243-184">Um script chamado [console. timeEnd ()][ConsoleApiTimeEnd].</span><span class="sxs-lookup"><span data-stu-id="8e243-184">A script called [console.timeEnd()][ConsoleApiTimeEnd].</span></span> |  
| <span data-ttu-id="8e243-185">Temporizador acionado</span><span class="sxs-lookup"><span data-stu-id="8e243-185">Timer Fired</span></span> | <span data-ttu-id="8e243-186">Um temporizador foi acionado que foi agendado com `setInterval()` ou `setTimeout()` .</span><span class="sxs-lookup"><span data-stu-id="8e243-186">A timer fired that was scheduled with `setInterval()` or `setTimeout()`.</span></span> |  
| <span data-ttu-id="8e243-187">Alteração de estado pronto para XHR</span><span class="sxs-lookup"><span data-stu-id="8e243-187">XHR Ready State Change</span></span> | <span data-ttu-id="8e243-188">O estado pronto de um XMLHttpRequest alterado.</span><span class="sxs-lookup"><span data-stu-id="8e243-188">The ready state of an XMLHTTPRequest changed.</span></span> |  
| <span data-ttu-id="8e243-189">Carga XHR</span><span class="sxs-lookup"><span data-stu-id="8e243-189">XHR Load</span></span> | <span data-ttu-id="8e243-190">`XMLHTTPRequest`Conclusão do carregamento.</span><span class="sxs-lookup"><span data-stu-id="8e243-190">An `XMLHTTPRequest` finished loading.</span></span> |  

### <span data-ttu-id="8e243-191">Propriedades de evento de script</span><span class="sxs-lookup"><span data-stu-id="8e243-191">Scripting event properties</span></span>  

| <span data-ttu-id="8e243-192">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8e243-192">Property</span></span> | <span data-ttu-id="8e243-193">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e243-193">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e243-194">ID do temporizador</span><span class="sxs-lookup"><span data-stu-id="8e243-194">Timer ID</span></span> | <span data-ttu-id="8e243-195">A ID do temporizador.</span><span class="sxs-lookup"><span data-stu-id="8e243-195">The timer ID.</span></span> |  
| <span data-ttu-id="8e243-196">Tempo limite</span><span class="sxs-lookup"><span data-stu-id="8e243-196">Timeout</span></span> | <span data-ttu-id="8e243-197">O tempo limite especificado pelo temporizador.</span><span class="sxs-lookup"><span data-stu-id="8e243-197">The timeout specified by the timer.</span></span> |  
| <span data-ttu-id="8e243-198">Repete</span><span class="sxs-lookup"><span data-stu-id="8e243-198">Repeats</span></span> | <span data-ttu-id="8e243-199">Booliano que especifica se o cronômetro se repete.</span><span class="sxs-lookup"><span data-stu-id="8e243-199">Boolean that specifies if the timer repeats.</span></span> |  
| <span data-ttu-id="8e243-200">Chamada de função</span><span class="sxs-lookup"><span data-stu-id="8e243-200">Function Call</span></span> | <span data-ttu-id="8e243-201">Uma função que foi invocada.</span><span class="sxs-lookup"><span data-stu-id="8e243-201">A function that was invoked.</span></span> |  

## <span data-ttu-id="8e243-202">Eventos de renderização</span><span class="sxs-lookup"><span data-stu-id="8e243-202">Rendering events</span></span>  

<span data-ttu-id="8e243-203">Esta seção lista os eventos que pertencem à categoria de renderização e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8e243-203">This section lists events that belong to Rendering category and their properties.</span></span>  

| <span data-ttu-id="8e243-204">Evento</span><span class="sxs-lookup"><span data-stu-id="8e243-204">Event</span></span> | <span data-ttu-id="8e243-205">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e243-205">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e243-206">Layout Invalidate</span><span class="sxs-lookup"><span data-stu-id="8e243-206">Invalidate layout</span></span> | <span data-ttu-id="8e243-207">O layout da página foi invalidado por uma alteração DOM.</span><span class="sxs-lookup"><span data-stu-id="8e243-207">The page layout was invalidated by a DOM change.</span></span> |  
| <span data-ttu-id="8e243-208">Layout</span><span class="sxs-lookup"><span data-stu-id="8e243-208">Layout</span></span> | <span data-ttu-id="8e243-209">Um layout de página foi concluído.</span><span class="sxs-lookup"><span data-stu-id="8e243-209">A page layout was completed.</span></span> |  
| <span data-ttu-id="8e243-210">Recalcular estilo</span><span class="sxs-lookup"><span data-stu-id="8e243-210">Recalculate style</span></span> | <span data-ttu-id="8e243-211">Estilos de elemento recalculados do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8e243-211">Microsoft Edge recalculated element styles.</span></span> |  
| <span data-ttu-id="8e243-212">Rolagem</span><span class="sxs-lookup"><span data-stu-id="8e243-212">Scroll</span></span> | <span data-ttu-id="8e243-213">O conteúdo do modo de exibição aninhado foi rolado.</span><span class="sxs-lookup"><span data-stu-id="8e243-213">The content of nested view was scrolled.</span></span> |  

### <span data-ttu-id="8e243-214">Renderizando Propriedades de eventos</span><span class="sxs-lookup"><span data-stu-id="8e243-214">Rendering event properties</span></span>  

| <span data-ttu-id="8e243-215">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8e243-215">Property</span></span> | <span data-ttu-id="8e243-216">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e243-216">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e243-217">Layout invalidado</span><span class="sxs-lookup"><span data-stu-id="8e243-217">Layout invalidated</span></span> | <span data-ttu-id="8e243-218">Para registros de layout, o rastreamento de pilha do código que fez com que o layout fosse invalidado.</span><span class="sxs-lookup"><span data-stu-id="8e243-218">For Layout records, the stack trace of the code that caused the layout to be invalidated.</span></span> |  
| <span data-ttu-id="8e243-219">Nós que precisam de layout</span><span class="sxs-lookup"><span data-stu-id="8e243-219">Nodes that need layout</span></span> | <span data-ttu-id="8e243-220">Para registros de layout, o número de nós que foram marcados como necessidade de layout antes do reinício do layout.</span><span class="sxs-lookup"><span data-stu-id="8e243-220">For Layout records, the number of nodes that were marked as needing layout before the relayout started.</span></span>  <span data-ttu-id="8e243-221">Esses nós normalmente são aqueles que foram invalidados pelo código do desenvolvedor, mais o caminho para a vertical para refazer o layout da raiz.</span><span class="sxs-lookup"><span data-stu-id="8e243-221">These are normally those nodes that were invalidated by developer code, plus a path upward to relayout root.</span></span> |  
| <span data-ttu-id="8e243-222">Tamanho da árvore de layout</span><span class="sxs-lookup"><span data-stu-id="8e243-222">Layout tree size</span></span> | <span data-ttu-id="8e243-223">Para registros de layout, o número total de nós sob a raiz do relayout \ (o nó que o Microsoft Edge inicia o relayout \).</span><span class="sxs-lookup"><span data-stu-id="8e243-223">For Layout records, the total number of nodes under the relayout root \(the node that Microsoft Edge starts the relayout\).</span></span> |  
| <span data-ttu-id="8e243-224">Escopo de layout</span><span class="sxs-lookup"><span data-stu-id="8e243-224">Layout scope</span></span> | <span data-ttu-id="8e243-225">Os valores possíveis são `Partial` \ (o limite de novo layout é uma parte do dom \) ou `Whole document` .</span><span class="sxs-lookup"><span data-stu-id="8e243-225">Possible values are `Partial` \(the re-layout boundary is a portion of the DOM\) or `Whole document`.</span></span> |  
| <span data-ttu-id="8e243-226">Elementos afetados</span><span class="sxs-lookup"><span data-stu-id="8e243-226">Elements affected</span></span> | <span data-ttu-id="8e243-227">Para recalcular registros de estilo, o número de elementos afetados por um recálculo de estilo.</span><span class="sxs-lookup"><span data-stu-id="8e243-227">For Recalculate style records, the number of elements affected by a style recalculation.</span></span> |  
| <span data-ttu-id="8e243-228">Estilos invalidados</span><span class="sxs-lookup"><span data-stu-id="8e243-228">Styles invalidated</span></span> | <span data-ttu-id="8e243-229">Para recalcular registros de estilo, fornece o rastreamento de pilha do código que causou a invalidação de estilo.</span><span class="sxs-lookup"><span data-stu-id="8e243-229">For Recalculate style records, provides the stack trace of the code that caused the style invalidation.</span></span> |  

## <span data-ttu-id="8e243-230">Eventos de pintura</span><span class="sxs-lookup"><span data-stu-id="8e243-230">Painting events</span></span>  

<span data-ttu-id="8e243-231">Esta seção lista os eventos que pertencem à categoria de pintura e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8e243-231">This section lists events that belong to Painting category and their properties.</span></span>  

| <span data-ttu-id="8e243-232">Evento</span><span class="sxs-lookup"><span data-stu-id="8e243-232">Event</span></span> | <span data-ttu-id="8e243-233">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e243-233">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e243-234">Camadas compostas</span><span class="sxs-lookup"><span data-stu-id="8e243-234">Composite Layers</span></span> | <span data-ttu-id="8e243-235">As camadas da imagem compostas para o mecanismo de renderização do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8e243-235">The composited image layers for the Microsoft Edge rendering engine.</span></span> |  
| <span data-ttu-id="8e243-236">Decodificação de imagem</span><span class="sxs-lookup"><span data-stu-id="8e243-236">Image Decode</span></span> | <span data-ttu-id="8e243-237">Um recurso de imagem foi decodificado.</span><span class="sxs-lookup"><span data-stu-id="8e243-237">An image resource was decoded.</span></span> |  
| <span data-ttu-id="8e243-238">Redimensionamento de imagens</span><span class="sxs-lookup"><span data-stu-id="8e243-238">Image Resize</span></span> | <span data-ttu-id="8e243-239">Uma imagem foi redimensionada a partir de suas dimensões nativas.</span><span class="sxs-lookup"><span data-stu-id="8e243-239">An image was resized from its native dimensions.</span></span> |  
| <span data-ttu-id="8e243-240">Paint</span><span class="sxs-lookup"><span data-stu-id="8e243-240">Paint</span></span> | <span data-ttu-id="8e243-241">Camadas compostas foram pintadas para uma região da exibição.</span><span class="sxs-lookup"><span data-stu-id="8e243-241">Composited layers were painted to a region of the display.</span></span>  <span data-ttu-id="8e243-242">Passar o mouse sobre um registro de pintura realça a região do vídeo que foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="8e243-242">Hovering over a Paint record highlights the region of the display that was updated.</span></span> |  

### <span data-ttu-id="8e243-243">Propriedades de evento de pintura</span><span class="sxs-lookup"><span data-stu-id="8e243-243">Painting event properties</span></span>  

| <span data-ttu-id="8e243-244">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8e243-244">Property</span></span> | <span data-ttu-id="8e243-245">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e243-245">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8e243-246">Location</span><span class="sxs-lookup"><span data-stu-id="8e243-246">Location</span></span> | <span data-ttu-id="8e243-247">Para eventos de pintura, as coordenadas x e y do retângulo de pintura.</span><span class="sxs-lookup"><span data-stu-id="8e243-247">For Paint events, the x and y coordinates of the paint rectangle.</span></span> |  
| <span data-ttu-id="8e243-248">Dimension</span><span class="sxs-lookup"><span data-stu-id="8e243-248">Dimensions</span></span> | <span data-ttu-id="8e243-249">Para eventos de pintura, a altura e a largura da região pintada.</span><span class="sxs-lookup"><span data-stu-id="8e243-249">For Paint events, the height and width of the painted region.</span></span> |  

 



<!-- image links -->  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "tempo-referência da API do console"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd-referência de API do console"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Janela: evento DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope. setInterval () | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope. setTimeout () | MDN"  

> [!NOTE]
> <span data-ttu-id="8e243-255">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="8e243-255">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8e243-256">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) e é criada por [Meggin Kearney][MegginKearney] \ (Tech Writer \) e o [Flavio][FlavioCopes] se encontra \ (desenvolvedor de pilha completa \).</span><span class="sxs-lookup"><span data-stu-id="8e243-256">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Flavio Copes][FlavioCopes] \(Full Stack Developer\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8e243-258">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8e243-258">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
