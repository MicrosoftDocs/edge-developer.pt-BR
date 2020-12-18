---
description: Referência do protocolo DevTools versão 0,2 (EdgeHTML) para o domínio da página. Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.
title: Page Domain-DevTools Protocol Version 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2f1849a2e2aa2f53cef9dff5d03ac991d368a6f3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231307"
---
# <span data-ttu-id="f3d9b-104">Page Domain-DevTools Protocol Version 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="f3d9b-104">Page Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="f3d9b-105">Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="f3d9b-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="f3d9b-106">Methods</span></span>**](#methods) | <span data-ttu-id="f3d9b-107">[habilitar](#enable), [desabilitar](#disable), [navegar](#navigate), [getFrameTree](#getframetree)</span><span class="sxs-lookup"><span data-stu-id="f3d9b-107">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span></span> |
| [**<span data-ttu-id="f3d9b-108">Eventos</span><span class="sxs-lookup"><span data-stu-id="f3d9b-108">Events</span></span>**](#events) | <span data-ttu-id="f3d9b-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span><span class="sxs-lookup"><span data-stu-id="f3d9b-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span></span> |
| [**<span data-ttu-id="f3d9b-110">Tipos</span><span class="sxs-lookup"><span data-stu-id="f3d9b-110">Types</span></span>**](#types) | <span data-ttu-id="f3d9b-111">[Frameid](#frameid), [frame](#frame), [FrameTree](#frametree)</span><span class="sxs-lookup"><span data-stu-id="f3d9b-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span></span> |
## <span data-ttu-id="f3d9b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="f3d9b-112">Methods</span></span>

### <span data-ttu-id="f3d9b-113">Habilitar</span><span class="sxs-lookup"><span data-stu-id="f3d9b-113">enable</span></span>
<span data-ttu-id="f3d9b-114">Habilita as notificações de domínio da página.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-114">Enables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="f3d9b-115">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="f3d9b-115">disable</span></span>
<span data-ttu-id="f3d9b-116">Desativa as notificações de domínio da página.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-116">Disables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="f3d9b-117">navegar</span><span class="sxs-lookup"><span data-stu-id="f3d9b-117">navigate</span></span>
<span data-ttu-id="f3d9b-118">Navega a página atual para a URL fornecida.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-118">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f3d9b-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3d9b-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f3d9b-120">url</span><span class="sxs-lookup"><span data-stu-id="f3d9b-120">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f3d9b-121">URL para navegar na página.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-121">URL to navigate the page to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f3d9b-122">frameid</span><span class="sxs-lookup"><span data-stu-id="f3d9b-122">frameId</span></span> <br/> <i><span data-ttu-id="f3d9b-123">opcional</span><span class="sxs-lookup"><span data-stu-id="f3d9b-123">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="f3d9b-124">ID do quadro para navegar.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-124">Frame id to navigate.</span></span> <span data-ttu-id="f3d9b-125">Se não for especificado, navegará na página superior.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-125">If not specified, will navigate the top page.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f3d9b-126">Devolver</span><span class="sxs-lookup"><span data-stu-id="f3d9b-126">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f3d9b-127">frameid</span><span class="sxs-lookup"><span data-stu-id="f3d9b-127">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="f3d9b-128">ID do quadro que será navegada.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-128">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f3d9b-129">getFrameTree</span><span class="sxs-lookup"><span data-stu-id="f3d9b-129">getFrameTree</span></span>
<span data-ttu-id="f3d9b-130">Retorna a estrutura da árvore de quadros atual.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-130">Returns present frame tree structure.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f3d9b-131">Devolver</span><span class="sxs-lookup"><span data-stu-id="f3d9b-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f3d9b-132">frameTree</span><span class="sxs-lookup"><span data-stu-id="f3d9b-132">frameTree</span></span></td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td><span data-ttu-id="f3d9b-133">Apresentar estrutura de árvore de quadros.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-133">Present frame tree structure.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="f3d9b-134">Eventos</span><span class="sxs-lookup"><span data-stu-id="f3d9b-134">Events</span></span>

### <span data-ttu-id="f3d9b-135">frameAttached</span><span class="sxs-lookup"><span data-stu-id="f3d9b-135">frameAttached</span></span>
<span data-ttu-id="f3d9b-136">Disparado quando o quadro é anexado ao seu pai.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-136">Fired when frame has been attached to its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f3d9b-137">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3d9b-137">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f3d9b-138">frameid</span><span class="sxs-lookup"><span data-stu-id="f3d9b-138">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="f3d9b-139">ID do quadro que foi anexado.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-139">Id of the frame that has been attached.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f3d9b-140">parentFrameId</span><span class="sxs-lookup"><span data-stu-id="f3d9b-140">parentFrameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="f3d9b-141">Identificador de quadro pai.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-141">Parent frame identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f3d9b-142">empilh</span><span class="sxs-lookup"><span data-stu-id="f3d9b-142">stack</span></span> <br/> <i><span data-ttu-id="f3d9b-143">opcional</span><span class="sxs-lookup"><span data-stu-id="f3d9b-143">optional</span></span></i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td><span data-ttu-id="f3d9b-144">Rastreamento de pilha JavaScript de quando o quadro foi anexado, somente defina se o quadro foi iniciado a partir do script.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-144">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f3d9b-145">frameDetached</span><span class="sxs-lookup"><span data-stu-id="f3d9b-145">frameDetached</span></span>
<span data-ttu-id="f3d9b-146">Disparado quando o quadro é separado de seu pai.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-146">Fired when frame has been detached from its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f3d9b-147">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3d9b-147">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f3d9b-148">frameid</span><span class="sxs-lookup"><span data-stu-id="f3d9b-148">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="f3d9b-149">ID do quadro que foi desconectado.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-149">Id of the frame that has been detached.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f3d9b-150">frameNavigated</span><span class="sxs-lookup"><span data-stu-id="f3d9b-150">frameNavigated</span></span>
<span data-ttu-id="f3d9b-151">Disparado após a conclusão da navegação do quadro.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-151">Fired once navigation of the frame has completed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f3d9b-152">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3d9b-152">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f3d9b-153">tempo</span><span class="sxs-lookup"><span data-stu-id="f3d9b-153">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="f3d9b-154">Objeto frame.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-154">Frame object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f3d9b-155">loadEventFired</span><span class="sxs-lookup"><span data-stu-id="f3d9b-155">loadEventFired</span></span>
<span data-ttu-id="f3d9b-156">Corresponde ao evento Window. OnLoad.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-156">Corresponds to the window.onload event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f3d9b-157">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3d9b-157">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f3d9b-158">carimbo</span><span class="sxs-lookup"><span data-stu-id="f3d9b-158">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="f3d9b-159">Número de milissegundos desde a época.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-159">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="f3d9b-160">domContentEventFired</span><span class="sxs-lookup"><span data-stu-id="f3d9b-160">domContentEventFired</span></span>
<span data-ttu-id="f3d9b-161">Corresponde ao evento Document. onDOMContentLoaded.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-161">Corresponds to the document.onDOMContentLoaded event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f3d9b-162">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3d9b-162">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f3d9b-163">carimbo</span><span class="sxs-lookup"><span data-stu-id="f3d9b-163">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="f3d9b-164">Número de milissegundos desde a época.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-164">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="f3d9b-165">Tipos</span><span class="sxs-lookup"><span data-stu-id="f3d9b-165">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="f3d9b-166">Frameid</span><span class="sxs-lookup"><span data-stu-id="f3d9b-166">FrameId</span></span> `string`

<span data-ttu-id="f3d9b-167">Identificador de quadro exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-167">Unique frame identifier.</span></span>

</p>

---

### <a name="frame"></a> <span data-ttu-id="f3d9b-168">Quadro</span><span class="sxs-lookup"><span data-stu-id="f3d9b-168">Frame</span></span> `object`

<span data-ttu-id="f3d9b-169">Informações sobre o quadro na página.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-169">Information about the Frame on the Page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f3d9b-170">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f3d9b-170">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f3d9b-171">id</span><span class="sxs-lookup"><span data-stu-id="f3d9b-171">id</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="f3d9b-172">Identificador exclusivo do quadro.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-172">Frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f3d9b-173">parentId</span><span class="sxs-lookup"><span data-stu-id="f3d9b-173">parentId</span></span> <br/> <i><span data-ttu-id="f3d9b-174">opcional</span><span class="sxs-lookup"><span data-stu-id="f3d9b-174">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="f3d9b-175">Identificador exclusivo do quadro pai.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-175">Parent frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f3d9b-176">name</span><span class="sxs-lookup"><span data-stu-id="f3d9b-176">name</span></span> <br/> <i><span data-ttu-id="f3d9b-177">opcional</span><span class="sxs-lookup"><span data-stu-id="f3d9b-177">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f3d9b-178">Nome do quadro, conforme especificado na marca.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-178">Frame's name as specified in the tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f3d9b-179">url</span><span class="sxs-lookup"><span data-stu-id="f3d9b-179">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f3d9b-180">URL do documento de quadro.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-180">Frame document's URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f3d9b-181">securityOrigin</span><span class="sxs-lookup"><span data-stu-id="f3d9b-181">securityOrigin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f3d9b-182">Origem de segurança do documento de quadro.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-182">Frame document's security origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f3d9b-183">MIME</span><span class="sxs-lookup"><span data-stu-id="f3d9b-183">mimeType</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="f3d9b-184">MimeType do documento de quadro conforme determinado pelo navegador.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-184">Frame document's mimeType as determined by the browser.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> <span data-ttu-id="f3d9b-185">FrameTree</span><span class="sxs-lookup"><span data-stu-id="f3d9b-185">FrameTree</span></span> `object`

<span data-ttu-id="f3d9b-186">Informações sobre a hierarquia de quadros.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-186">Information about the Frame hierarchy.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="f3d9b-187">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f3d9b-187">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="f3d9b-188">tempo</span><span class="sxs-lookup"><span data-stu-id="f3d9b-188">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="f3d9b-189">Informações de quadro para este item de árvore.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-189">Frame information for this tree item.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="f3d9b-190">childFrames</span><span class="sxs-lookup"><span data-stu-id="f3d9b-190">childFrames</span></span> <br/> <i><span data-ttu-id="f3d9b-191">opcional</span><span class="sxs-lookup"><span data-stu-id="f3d9b-191">optional</span></span></i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td><span data-ttu-id="f3d9b-192">Quadros filho.</span><span class="sxs-lookup"><span data-stu-id="f3d9b-192">Child frames.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
