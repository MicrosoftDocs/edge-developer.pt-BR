---
description: Referência do Protocolo DevTools Versão 0.2 (EdgeHTML) para o Domínio da Página. Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.
title: Domínio da Página - DevTools Protocol Versão 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d969dd100164ace61445a4618174cfa943dcfd2b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398844"
---
# <a name="page-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="77f76-104">Domínio da Página - DevTools Protocol Versão 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="77f76-104">Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="77f76-105">Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.</span><span class="sxs-lookup"><span data-stu-id="77f76-105">Actions and events related to the inspected page belong to the page domain.</span></span>  

| <span data-ttu-id="77f76-106">Classificação</span><span class="sxs-lookup"><span data-stu-id="77f76-106">Classification</span></span> | <span data-ttu-id="77f76-107">Membros</span><span class="sxs-lookup"><span data-stu-id="77f76-107">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="77f76-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="77f76-108">Methods</span></span>](#methods) | <span data-ttu-id="77f76-109">[habilitar](#enable), [desabilitar, navegar](#navigate), [getFrameTree](#getframetree) [](#disable)</span><span class="sxs-lookup"><span data-stu-id="77f76-109">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span></span> |  
| [<span data-ttu-id="77f76-110">Eventos</span><span class="sxs-lookup"><span data-stu-id="77f76-110">Events</span></span>](#events) | <span data-ttu-id="77f76-111">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired,](#loadeventfired) [domContentEventFired](#domcontenteventfired)</span><span class="sxs-lookup"><span data-stu-id="77f76-111">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span></span> |  
| [<span data-ttu-id="77f76-112">Tipos</span><span class="sxs-lookup"><span data-stu-id="77f76-112">Types</span></span>](#types) | <span data-ttu-id="77f76-113">[FrameId,](#frameid) [Frame](#frame), [FrameTree](#frametree)</span><span class="sxs-lookup"><span data-stu-id="77f76-113">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span></span> |  

## <a name="methods"></a><span data-ttu-id="77f76-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="77f76-114">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="77f76-115">Habilitar</span><span class="sxs-lookup"><span data-stu-id="77f76-115">enable</span></span>  

<span data-ttu-id="77f76-116">Habilita notificações de domínio de página.</span><span class="sxs-lookup"><span data-stu-id="77f76-116">Enables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="77f76-117">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="77f76-117">disable</span></span>  

<span data-ttu-id="77f76-118">Desabilita notificações de domínio de página.</span><span class="sxs-lookup"><span data-stu-id="77f76-118">Disables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="navigate"></a><span data-ttu-id="77f76-119">navegar</span><span class="sxs-lookup"><span data-stu-id="77f76-119">navigate</span></span>  

<span data-ttu-id="77f76-120">Navega a página atual para a URL determinada.</span><span class="sxs-lookup"><span data-stu-id="77f76-120">Navigates current page to the given URL.</span></span>  

| <span data-ttu-id="77f76-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77f76-121">Parameters</span></span> | <span data-ttu-id="77f76-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="77f76-122">Type</span></span> | <span data-ttu-id="77f76-123">Detalhes</span><span class="sxs-lookup"><span data-stu-id="77f76-123">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="77f76-124">url</span><span class="sxs-lookup"><span data-stu-id="77f76-124">url</span></span> | `string` | <span data-ttu-id="77f76-125">URL para navegar na página.</span><span class="sxs-lookup"><span data-stu-id="77f76-125">URL to navigate the page to.</span></span> |  
| <span data-ttu-id="77f76-126">frameId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="77f76-126">frameId \(optional\)</span></span> | [<span data-ttu-id="77f76-127">FrameId</span><span class="sxs-lookup"><span data-stu-id="77f76-127">FrameId</span></span>](#frameid) | <span data-ttu-id="77f76-128">ID do quadro para navegar.</span><span class="sxs-lookup"><span data-stu-id="77f76-128">Frame id to navigate.</span></span>  <span data-ttu-id="77f76-129">Se não for especificado, navegará pela página superior.</span><span class="sxs-lookup"><span data-stu-id="77f76-129">If not specified, will navigate the top page.</span></span> |  

| <span data-ttu-id="77f76-130">Retorna</span><span class="sxs-lookup"><span data-stu-id="77f76-130">Returns</span></span> | <span data-ttu-id="77f76-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="77f76-131">Type</span></span> | <span data-ttu-id="77f76-132">Detalhes</span><span class="sxs-lookup"><span data-stu-id="77f76-132">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="77f76-133">frameId</span><span class="sxs-lookup"><span data-stu-id="77f76-133">frameId</span></span> | [<span data-ttu-id="77f76-134">FrameId</span><span class="sxs-lookup"><span data-stu-id="77f76-134">FrameId</span></span>](#frameid) | <span data-ttu-id="77f76-135">ID do quadro que será navegada.</span><span class="sxs-lookup"><span data-stu-id="77f76-135">Frame id that will be navigated.</span></span> |  

---  

### <a name="getframetree"></a><span data-ttu-id="77f76-136">getFrameTree</span><span class="sxs-lookup"><span data-stu-id="77f76-136">getFrameTree</span></span>  

<span data-ttu-id="77f76-137">Retorna a estrutura da árvore de quadros atual.</span><span class="sxs-lookup"><span data-stu-id="77f76-137">Returns present frame tree structure.</span></span>  

| <span data-ttu-id="77f76-138">Retorna</span><span class="sxs-lookup"><span data-stu-id="77f76-138">Returns</span></span> | <span data-ttu-id="77f76-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="77f76-139">Type</span></span> | <span data-ttu-id="77f76-140">Detalhes</span><span class="sxs-lookup"><span data-stu-id="77f76-140">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="77f76-141">frameTree</span><span class="sxs-lookup"><span data-stu-id="77f76-141">frameTree</span></span> | [<span data-ttu-id="77f76-142">FrameTree</span><span class="sxs-lookup"><span data-stu-id="77f76-142">FrameTree</span></span>](#frametree) | <span data-ttu-id="77f76-143">Estrutura da árvore de quadros presente.</span><span class="sxs-lookup"><span data-stu-id="77f76-143">Present frame tree structure.</span></span> |  

---  

## <a name="events"></a><span data-ttu-id="77f76-144">Eventos</span><span class="sxs-lookup"><span data-stu-id="77f76-144">Events</span></span>  

### <a name="frameattached"></a><span data-ttu-id="77f76-145">frameAttached</span><span class="sxs-lookup"><span data-stu-id="77f76-145">frameAttached</span></span>  

<span data-ttu-id="77f76-146">Acionado quando o quadro foi anexado ao pai.</span><span class="sxs-lookup"><span data-stu-id="77f76-146">Fired when frame has been attached to its parent.</span></span>  

| <span data-ttu-id="77f76-147">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77f76-147">Parameters</span></span> | <span data-ttu-id="77f76-148">Tipo</span><span class="sxs-lookup"><span data-stu-id="77f76-148">Type</span></span> | <span data-ttu-id="77f76-149">Detalhes</span><span class="sxs-lookup"><span data-stu-id="77f76-149">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="77f76-150">frameId</span><span class="sxs-lookup"><span data-stu-id="77f76-150">frameId</span></span> | [<span data-ttu-id="77f76-151">FrameId</span><span class="sxs-lookup"><span data-stu-id="77f76-151">FrameId</span></span>](#frameid) | <span data-ttu-id="77f76-152">ID do quadro anexado.</span><span class="sxs-lookup"><span data-stu-id="77f76-152">Id of the frame that has been attached.</span></span> |  
| <span data-ttu-id="77f76-153">parentFrameId</span><span class="sxs-lookup"><span data-stu-id="77f76-153">parentFrameId</span></span> | [<span data-ttu-id="77f76-154">FrameId</span><span class="sxs-lookup"><span data-stu-id="77f76-154">FrameId</span></span>](#frameid) | <span data-ttu-id="77f76-155">Identificador de quadro pai.</span><span class="sxs-lookup"><span data-stu-id="77f76-155">Parent frame identifier.</span></span> |  
| <span data-ttu-id="77f76-156">stack \(optional\)</span><span class="sxs-lookup"><span data-stu-id="77f76-156">stack \(optional\)</span></span> | [<span data-ttu-id="77f76-157">Runtime.StackTrace</span><span class="sxs-lookup"><span data-stu-id="77f76-157">Runtime.StackTrace</span></span>](./runtime.md#stacktrace) | <span data-ttu-id="77f76-158">Rastreamento de pilha JavaScript de quando o quadro foi anexado, somente definido se o quadro tiver sido iniciado a partir do script.</span><span class="sxs-lookup"><span data-stu-id="77f76-158">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span></span> |  

---  

### <a name="framedetached"></a><span data-ttu-id="77f76-159">frameDetached</span><span class="sxs-lookup"><span data-stu-id="77f76-159">frameDetached</span></span>  

<span data-ttu-id="77f76-160">Acionado quando o quadro foi desvinculado de seu pai.</span><span class="sxs-lookup"><span data-stu-id="77f76-160">Fired when frame has been detached from its parent.</span></span>  

| <span data-ttu-id="77f76-161">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77f76-161">Parameters</span></span> | <span data-ttu-id="77f76-162">Tipo</span><span class="sxs-lookup"><span data-stu-id="77f76-162">Type</span></span> | <span data-ttu-id="77f76-163">Detalhes</span><span class="sxs-lookup"><span data-stu-id="77f76-163">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="77f76-164">frameId</span><span class="sxs-lookup"><span data-stu-id="77f76-164">frameId</span></span> | [<span data-ttu-id="77f76-165">FrameId</span><span class="sxs-lookup"><span data-stu-id="77f76-165">FrameId</span></span>](#frameid) | <span data-ttu-id="77f76-166">ID do quadro que foi desvinculado.</span><span class="sxs-lookup"><span data-stu-id="77f76-166">ID of the frame that has been detached.</span></span> |  

---  

### <a name="framenavigated"></a><span data-ttu-id="77f76-167">frameNavigated</span><span class="sxs-lookup"><span data-stu-id="77f76-167">frameNavigated</span></span>  

<span data-ttu-id="77f76-168">Acionado depois que a navegação do quadro tiver sido concluída.</span><span class="sxs-lookup"><span data-stu-id="77f76-168">Fired once navigation of the frame has completed.</span></span>  

| <span data-ttu-id="77f76-169">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77f76-169">Parameters</span></span> | <span data-ttu-id="77f76-170">Tipo</span><span class="sxs-lookup"><span data-stu-id="77f76-170">Type</span></span> | <span data-ttu-id="77f76-171">Detalhes</span><span class="sxs-lookup"><span data-stu-id="77f76-171">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="77f76-172">frame</span><span class="sxs-lookup"><span data-stu-id="77f76-172">frame</span></span> | [<span data-ttu-id="77f76-173">Quadro</span><span class="sxs-lookup"><span data-stu-id="77f76-173">Frame</span></span>](#frame) | <span data-ttu-id="77f76-174">Objeto Frame.</span><span class="sxs-lookup"><span data-stu-id="77f76-174">Frame object.</span></span> |  

---  

### <a name="loadeventfired"></a><span data-ttu-id="77f76-175">loadEventFired</span><span class="sxs-lookup"><span data-stu-id="77f76-175">loadEventFired</span></span>  

<span data-ttu-id="77f76-176">Corresponde ao `window.onload` evento.</span><span class="sxs-lookup"><span data-stu-id="77f76-176">Corresponds to the `window.onload` event.</span></span>  

| <span data-ttu-id="77f76-177">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77f76-177">Parameters</span></span> | <span data-ttu-id="77f76-178">Tipo</span><span class="sxs-lookup"><span data-stu-id="77f76-178">Type</span></span> | <span data-ttu-id="77f76-179">Detalhes</span><span class="sxs-lookup"><span data-stu-id="77f76-179">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="77f76-180">timestamp</span><span class="sxs-lookup"><span data-stu-id="77f76-180">timestamp</span></span> | `number` | <span data-ttu-id="77f76-181">Número de milissegundos desde a época.</span><span class="sxs-lookup"><span data-stu-id="77f76-181">Number of milliseconds since epoch.</span></span> |  

---  

### <a name="domcontenteventfired"></a><span data-ttu-id="77f76-182">domContentEventFired</span><span class="sxs-lookup"><span data-stu-id="77f76-182">domContentEventFired</span></span>  

<span data-ttu-id="77f76-183">Corresponde ao `document.onDOMContentLoaded` evento.</span><span class="sxs-lookup"><span data-stu-id="77f76-183">Corresponds to the `document.onDOMContentLoaded` event.</span></span>  

| <span data-ttu-id="77f76-184">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77f76-184">Parameters</span></span> | <span data-ttu-id="77f76-185">Tipo</span><span class="sxs-lookup"><span data-stu-id="77f76-185">Type</span></span> | <span data-ttu-id="77f76-186">Detalhes</span><span class="sxs-lookup"><span data-stu-id="77f76-186">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="77f76-187">timestamp</span><span class="sxs-lookup"><span data-stu-id="77f76-187">timestamp</span></span> | `number` | <span data-ttu-id="77f76-188">Número de milissegundos desde a época.</span><span class="sxs-lookup"><span data-stu-id="77f76-188">Number of milliseconds since epoch.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="77f76-189">Tipos</span><span class="sxs-lookup"><span data-stu-id="77f76-189">Types</span></span>  

### <a name="frameid-string"></a><span data-ttu-id="77f76-190">Cadeia de caracteres FrameId</span><span class="sxs-lookup"><span data-stu-id="77f76-190">FrameId string</span></span>  

<a name="frameid"></a>  

<span data-ttu-id="77f76-191">Identificador de quadro exclusivo.</span><span class="sxs-lookup"><span data-stu-id="77f76-191">Unique frame identifier.</span></span>  

&nbsp;  

---  

### <a name="frame-object"></a><span data-ttu-id="77f76-192">Objeto Frame</span><span class="sxs-lookup"><span data-stu-id="77f76-192">Frame object</span></span>  

<a name="frame"></a>  

<span data-ttu-id="77f76-193">Informações sobre o Quadro na Página.</span><span class="sxs-lookup"><span data-stu-id="77f76-193">Information about the Frame on the Page.</span></span>  

| <span data-ttu-id="77f76-194">Propriedades</span><span class="sxs-lookup"><span data-stu-id="77f76-194">Properties</span></span> | <span data-ttu-id="77f76-195">Tipo</span><span class="sxs-lookup"><span data-stu-id="77f76-195">Type</span></span> | <span data-ttu-id="77f76-196">Detalhes</span><span class="sxs-lookup"><span data-stu-id="77f76-196">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="77f76-197">id</span><span class="sxs-lookup"><span data-stu-id="77f76-197">id</span></span> | [<span data-ttu-id="77f76-198">FrameId</span><span class="sxs-lookup"><span data-stu-id="77f76-198">FrameId</span></span>](#frameid) | <span data-ttu-id="77f76-199">Identificador exclusivo do quadro.</span><span class="sxs-lookup"><span data-stu-id="77f76-199">Frame unique identifier.</span></span> |  
| <span data-ttu-id="77f76-200">parentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="77f76-200">parentId \(optional\)</span></span> | [<span data-ttu-id="77f76-201">FrameId</span><span class="sxs-lookup"><span data-stu-id="77f76-201">FrameId</span></span>](#frameid) | <span data-ttu-id="77f76-202">Identificador exclusivo do quadro pai.</span><span class="sxs-lookup"><span data-stu-id="77f76-202">Parent frame unique identifier.</span></span> |  
| <span data-ttu-id="77f76-203">nome \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="77f76-203">name \(optional\)</span></span> | `string` | <span data-ttu-id="77f76-204">O nome do quadro conforme especificado na marca.</span><span class="sxs-lookup"><span data-stu-id="77f76-204">Frame's name as specified in the tag.</span></span> |  
| <span data-ttu-id="77f76-205">url</span><span class="sxs-lookup"><span data-stu-id="77f76-205">url</span></span> | `string` | <span data-ttu-id="77f76-206">URL do documento do quadro.</span><span class="sxs-lookup"><span data-stu-id="77f76-206">Frame document's URL.</span></span> |  
| <span data-ttu-id="77f76-207">securityOrigin</span><span class="sxs-lookup"><span data-stu-id="77f76-207">securityOrigin</span></span> | `string` | <span data-ttu-id="77f76-208">Origem da segurança do documento do quadro.</span><span class="sxs-lookup"><span data-stu-id="77f76-208">Frame document's security origin.</span></span> |  
| <span data-ttu-id="77f76-209">mimeType</span><span class="sxs-lookup"><span data-stu-id="77f76-209">mimeType</span></span> | `string` | <span data-ttu-id="77f76-210">MimeType do documento de quadro conforme determinado pelo navegador.</span><span class="sxs-lookup"><span data-stu-id="77f76-210">Frame document's mimeType as determined by the browser.</span></span> |  

---  

### <a name="frametree-object"></a><span data-ttu-id="77f76-211">Objeto FrameTree</span><span class="sxs-lookup"><span data-stu-id="77f76-211">FrameTree object</span></span>  

<a name="frametree"></a>  

<span data-ttu-id="77f76-212">Informações sobre a hierarquia frame.</span><span class="sxs-lookup"><span data-stu-id="77f76-212">Information about the Frame hierarchy.</span></span>  

| <span data-ttu-id="77f76-213">Propriedades</span><span class="sxs-lookup"><span data-stu-id="77f76-213">Properties</span></span> | <span data-ttu-id="77f76-214">Tipo</span><span class="sxs-lookup"><span data-stu-id="77f76-214">Type</span></span> | <span data-ttu-id="77f76-215">Detalhes</span><span class="sxs-lookup"><span data-stu-id="77f76-215">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="77f76-216">frame</span><span class="sxs-lookup"><span data-stu-id="77f76-216">frame</span></span> | [<span data-ttu-id="77f76-217">Quadro</span><span class="sxs-lookup"><span data-stu-id="77f76-217">Frame</span></span>](#frame) | <span data-ttu-id="77f76-218">Informações de quadro para este item de árvore.</span><span class="sxs-lookup"><span data-stu-id="77f76-218">Frame information for this tree item.</span></span> |  
| <span data-ttu-id="77f76-219">childFrames \(optional\)</span><span class="sxs-lookup"><span data-stu-id="77f76-219">childFrames \(optional\)</span></span> | [<span data-ttu-id="77f76-220">FrameTree[]</span><span class="sxs-lookup"><span data-stu-id="77f76-220">FrameTree[]</span></span>](#frametree) | <span data-ttu-id="77f76-221">Quadros filho.</span><span class="sxs-lookup"><span data-stu-id="77f76-221">Child frames.</span></span> |  

---  
