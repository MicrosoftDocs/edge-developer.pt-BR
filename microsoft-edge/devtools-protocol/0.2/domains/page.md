---
description: Referência para o domínio da página. Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.
title: Page Domain-DevTools Protocol Version 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 864515eefbcb809e280f2ab1d81015018272c398
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882839"
---
# <span data-ttu-id="304fb-104">Page Domain-DevTools Protocol Version 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="304fb-104">Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="304fb-105">Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.</span><span class="sxs-lookup"><span data-stu-id="304fb-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="304fb-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="304fb-106">Methods</span></span>**](#methods) | <span data-ttu-id="304fb-107">[habilitar](#enable), [desabilitar](#disable), [navegar](#navigate), [getFrameTree](#getframetree)</span><span class="sxs-lookup"><span data-stu-id="304fb-107">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span></span> |
| [**<span data-ttu-id="304fb-108">Eventos</span><span class="sxs-lookup"><span data-stu-id="304fb-108">Events</span></span>**](#events) | <span data-ttu-id="304fb-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span><span class="sxs-lookup"><span data-stu-id="304fb-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span></span> |
| [**<span data-ttu-id="304fb-110">Tipos</span><span class="sxs-lookup"><span data-stu-id="304fb-110">Types</span></span>**](#types) | <span data-ttu-id="304fb-111">[Frameid](#frameid), [frame](#frame), [FrameTree](#frametree)</span><span class="sxs-lookup"><span data-stu-id="304fb-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span></span> |
## <span data-ttu-id="304fb-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="304fb-112">Methods</span></span>

### <span data-ttu-id="304fb-113">Habilitar</span><span class="sxs-lookup"><span data-stu-id="304fb-113">enable</span></span>
<span data-ttu-id="304fb-114">Habilita as notificações de domínio da página.</span><span class="sxs-lookup"><span data-stu-id="304fb-114">Enables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="304fb-115">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="304fb-115">disable</span></span>
<span data-ttu-id="304fb-116">Desativa as notificações de domínio da página.</span><span class="sxs-lookup"><span data-stu-id="304fb-116">Disables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="304fb-117">navegar</span><span class="sxs-lookup"><span data-stu-id="304fb-117">navigate</span></span>
<span data-ttu-id="304fb-118">Navega a página atual para a URL fornecida.</span><span class="sxs-lookup"><span data-stu-id="304fb-118">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="304fb-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="304fb-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="304fb-120">url</span><span class="sxs-lookup"><span data-stu-id="304fb-120">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="304fb-121">URL para navegar na página.</span><span class="sxs-lookup"><span data-stu-id="304fb-121">URL to navigate the page to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="304fb-122">frameid</span><span class="sxs-lookup"><span data-stu-id="304fb-122">frameId</span></span> <br/> <i><span data-ttu-id="304fb-123">opcional</span><span class="sxs-lookup"><span data-stu-id="304fb-123">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="304fb-124">ID do quadro para navegar.</span><span class="sxs-lookup"><span data-stu-id="304fb-124">Frame id to navigate.</span></span> <span data-ttu-id="304fb-125">Se não for especificado, navegará na página superior.</span><span class="sxs-lookup"><span data-stu-id="304fb-125">If not specified, will navigate the top page.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="304fb-126">Devolver</span><span class="sxs-lookup"><span data-stu-id="304fb-126">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="304fb-127">frameid</span><span class="sxs-lookup"><span data-stu-id="304fb-127">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="304fb-128">ID do quadro que será navegada.</span><span class="sxs-lookup"><span data-stu-id="304fb-128">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="304fb-129">getFrameTree</span><span class="sxs-lookup"><span data-stu-id="304fb-129">getFrameTree</span></span>
<span data-ttu-id="304fb-130">Retorna a estrutura da árvore de quadros atual.</span><span class="sxs-lookup"><span data-stu-id="304fb-130">Returns present frame tree structure.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="304fb-131">Devolver</span><span class="sxs-lookup"><span data-stu-id="304fb-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="304fb-132">frameTree</span><span class="sxs-lookup"><span data-stu-id="304fb-132">frameTree</span></span></td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td><span data-ttu-id="304fb-133">Apresentar estrutura de árvore de quadros.</span><span class="sxs-lookup"><span data-stu-id="304fb-133">Present frame tree structure.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="304fb-134">Eventos</span><span class="sxs-lookup"><span data-stu-id="304fb-134">Events</span></span>

### <span data-ttu-id="304fb-135">frameAttached</span><span class="sxs-lookup"><span data-stu-id="304fb-135">frameAttached</span></span>
<span data-ttu-id="304fb-136">Disparado quando o quadro é anexado ao seu pai.</span><span class="sxs-lookup"><span data-stu-id="304fb-136">Fired when frame has been attached to its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="304fb-137">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="304fb-137">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="304fb-138">frameid</span><span class="sxs-lookup"><span data-stu-id="304fb-138">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="304fb-139">ID do quadro que foi anexado.</span><span class="sxs-lookup"><span data-stu-id="304fb-139">Id of the frame that has been attached.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="304fb-140">parentFrameId</span><span class="sxs-lookup"><span data-stu-id="304fb-140">parentFrameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="304fb-141">Identificador de quadro pai.</span><span class="sxs-lookup"><span data-stu-id="304fb-141">Parent frame identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="304fb-142">empilh</span><span class="sxs-lookup"><span data-stu-id="304fb-142">stack</span></span> <br/> <i><span data-ttu-id="304fb-143">opcional</span><span class="sxs-lookup"><span data-stu-id="304fb-143">optional</span></span></i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td><span data-ttu-id="304fb-144">Rastreamento de pilha JavaScript de quando o quadro foi anexado, somente defina se o quadro foi iniciado a partir do script.</span><span class="sxs-lookup"><span data-stu-id="304fb-144">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="304fb-145">frameDetached</span><span class="sxs-lookup"><span data-stu-id="304fb-145">frameDetached</span></span>
<span data-ttu-id="304fb-146">Disparado quando o quadro é separado de seu pai.</span><span class="sxs-lookup"><span data-stu-id="304fb-146">Fired when frame has been detached from its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="304fb-147">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="304fb-147">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="304fb-148">frameid</span><span class="sxs-lookup"><span data-stu-id="304fb-148">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="304fb-149">ID do quadro que foi desconectado.</span><span class="sxs-lookup"><span data-stu-id="304fb-149">Id of the frame that has been detached.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="304fb-150">frameNavigated</span><span class="sxs-lookup"><span data-stu-id="304fb-150">frameNavigated</span></span>
<span data-ttu-id="304fb-151">Disparado após a conclusão da navegação do quadro.</span><span class="sxs-lookup"><span data-stu-id="304fb-151">Fired once navigation of the frame has completed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="304fb-152">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="304fb-152">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="304fb-153">tempo</span><span class="sxs-lookup"><span data-stu-id="304fb-153">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="304fb-154">Objeto frame.</span><span class="sxs-lookup"><span data-stu-id="304fb-154">Frame object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="304fb-155">loadEventFired</span><span class="sxs-lookup"><span data-stu-id="304fb-155">loadEventFired</span></span>
<span data-ttu-id="304fb-156">Corresponde ao evento Window. OnLoad.</span><span class="sxs-lookup"><span data-stu-id="304fb-156">Corresponds to the window.onload event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="304fb-157">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="304fb-157">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="304fb-158">carimbo</span><span class="sxs-lookup"><span data-stu-id="304fb-158">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="304fb-159">Número de milissegundos desde a época.</span><span class="sxs-lookup"><span data-stu-id="304fb-159">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="304fb-160">domContentEventFired</span><span class="sxs-lookup"><span data-stu-id="304fb-160">domContentEventFired</span></span>
<span data-ttu-id="304fb-161">Corresponde ao evento Document. onDOMContentLoaded.</span><span class="sxs-lookup"><span data-stu-id="304fb-161">Corresponds to the document.onDOMContentLoaded event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="304fb-162">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="304fb-162">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="304fb-163">carimbo</span><span class="sxs-lookup"><span data-stu-id="304fb-163">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="304fb-164">Número de milissegundos desde a época.</span><span class="sxs-lookup"><span data-stu-id="304fb-164">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="304fb-165">Tipos</span><span class="sxs-lookup"><span data-stu-id="304fb-165">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="304fb-166">Frameid</span><span class="sxs-lookup"><span data-stu-id="304fb-166">FrameId</span></span> `string`

<span data-ttu-id="304fb-167">Identificador de quadro exclusivo.</span><span class="sxs-lookup"><span data-stu-id="304fb-167">Unique frame identifier.</span></span>

</p>

---

### <a name="frame"></a> <span data-ttu-id="304fb-168">Quadro</span><span class="sxs-lookup"><span data-stu-id="304fb-168">Frame</span></span> `object`

<span data-ttu-id="304fb-169">Informações sobre o quadro na página.</span><span class="sxs-lookup"><span data-stu-id="304fb-169">Information about the Frame on the Page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="304fb-170">Propriedades</span><span class="sxs-lookup"><span data-stu-id="304fb-170">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="304fb-171">id</span><span class="sxs-lookup"><span data-stu-id="304fb-171">id</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="304fb-172">Identificador exclusivo do quadro.</span><span class="sxs-lookup"><span data-stu-id="304fb-172">Frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="304fb-173">parentId</span><span class="sxs-lookup"><span data-stu-id="304fb-173">parentId</span></span> <br/> <i><span data-ttu-id="304fb-174">opcional</span><span class="sxs-lookup"><span data-stu-id="304fb-174">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="304fb-175">Identificador exclusivo do quadro pai.</span><span class="sxs-lookup"><span data-stu-id="304fb-175">Parent frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="304fb-176">name</span><span class="sxs-lookup"><span data-stu-id="304fb-176">name</span></span> <br/> <i><span data-ttu-id="304fb-177">opcional</span><span class="sxs-lookup"><span data-stu-id="304fb-177">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="304fb-178">Nome do quadro, conforme especificado na marca.</span><span class="sxs-lookup"><span data-stu-id="304fb-178">Frame's name as specified in the tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="304fb-179">url</span><span class="sxs-lookup"><span data-stu-id="304fb-179">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="304fb-180">URL do documento de quadro.</span><span class="sxs-lookup"><span data-stu-id="304fb-180">Frame document's URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="304fb-181">securityOrigin</span><span class="sxs-lookup"><span data-stu-id="304fb-181">securityOrigin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="304fb-182">Origem de segurança do documento de quadro.</span><span class="sxs-lookup"><span data-stu-id="304fb-182">Frame document's security origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="304fb-183">MIME</span><span class="sxs-lookup"><span data-stu-id="304fb-183">mimeType</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="304fb-184">MimeType do documento de quadro conforme determinado pelo navegador.</span><span class="sxs-lookup"><span data-stu-id="304fb-184">Frame document's mimeType as determined by the browser.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> <span data-ttu-id="304fb-185">FrameTree</span><span class="sxs-lookup"><span data-stu-id="304fb-185">FrameTree</span></span> `object`

<span data-ttu-id="304fb-186">Informações sobre a hierarquia de quadros.</span><span class="sxs-lookup"><span data-stu-id="304fb-186">Information about the Frame hierarchy.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="304fb-187">Propriedades</span><span class="sxs-lookup"><span data-stu-id="304fb-187">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="304fb-188">tempo</span><span class="sxs-lookup"><span data-stu-id="304fb-188">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="304fb-189">Informações de quadro para este item de árvore.</span><span class="sxs-lookup"><span data-stu-id="304fb-189">Frame information for this tree item.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="304fb-190">childFrames</span><span class="sxs-lookup"><span data-stu-id="304fb-190">childFrames</span></span> <br/> <i><span data-ttu-id="304fb-191">opcional</span><span class="sxs-lookup"><span data-stu-id="304fb-191">optional</span></span></i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td><span data-ttu-id="304fb-192">Quadros filho.</span><span class="sxs-lookup"><span data-stu-id="304fb-192">Child frames.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
