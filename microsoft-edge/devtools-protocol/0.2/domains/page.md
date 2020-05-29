---
description: Referência para o domínio da página. Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.
title: Página Domain-DevTools protocolo versão 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 688cc1fcfce0b81c5eed0c858a4a60b4754c49a4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561333"
---
# <span data-ttu-id="18edc-104">Página</span><span class="sxs-lookup"><span data-stu-id="18edc-104">Page</span></span>
<span data-ttu-id="18edc-105">Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.</span><span class="sxs-lookup"><span data-stu-id="18edc-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="18edc-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="18edc-106">Methods</span></span>**](#methods) | <span data-ttu-id="18edc-107">[habilitar](#enable), [desabilitar](#disable), [navegar](#navigate), [getFrameTree](#getframetree)</span><span class="sxs-lookup"><span data-stu-id="18edc-107">[enable](#enable), [disable](#disable), [navigate](#navigate), [getFrameTree](#getframetree)</span></span> |
| [**<span data-ttu-id="18edc-108">Eventos</span><span class="sxs-lookup"><span data-stu-id="18edc-108">Events</span></span>**](#events) | <span data-ttu-id="18edc-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span><span class="sxs-lookup"><span data-stu-id="18edc-109">[frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired)</span></span> |
| [**<span data-ttu-id="18edc-110">Tipos</span><span class="sxs-lookup"><span data-stu-id="18edc-110">Types</span></span>**](#types) | <span data-ttu-id="18edc-111">[Frameid](#frameid), [frame](#frame), [FrameTree](#frametree)</span><span class="sxs-lookup"><span data-stu-id="18edc-111">[FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree)</span></span> |
## <span data-ttu-id="18edc-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="18edc-112">Methods</span></span>

### <span data-ttu-id="18edc-113">Habilitar</span><span class="sxs-lookup"><span data-stu-id="18edc-113">enable</span></span>
<span data-ttu-id="18edc-114">Habilita as notificações de domínio da página.</span><span class="sxs-lookup"><span data-stu-id="18edc-114">Enables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="18edc-115">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="18edc-115">disable</span></span>
<span data-ttu-id="18edc-116">Desativa as notificações de domínio da página.</span><span class="sxs-lookup"><span data-stu-id="18edc-116">Disables page domain notifications.</span></span>

</p>

---

### <span data-ttu-id="18edc-117">navegar</span><span class="sxs-lookup"><span data-stu-id="18edc-117">navigate</span></span>
<span data-ttu-id="18edc-118">Navega a página atual para a URL fornecida.</span><span class="sxs-lookup"><span data-stu-id="18edc-118">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="18edc-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18edc-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="18edc-120">url</span><span class="sxs-lookup"><span data-stu-id="18edc-120">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="18edc-121">URL para navegar na página.</span><span class="sxs-lookup"><span data-stu-id="18edc-121">URL to navigate the page to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="18edc-122">frameid</span><span class="sxs-lookup"><span data-stu-id="18edc-122">frameId</span></span> <br/> <i><span data-ttu-id="18edc-123">opcional</span><span class="sxs-lookup"><span data-stu-id="18edc-123">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="18edc-124">ID do quadro para navegar.</span><span class="sxs-lookup"><span data-stu-id="18edc-124">Frame id to navigate.</span></span> <span data-ttu-id="18edc-125">Se não for especificado, navegará na página superior.</span><span class="sxs-lookup"><span data-stu-id="18edc-125">If not specified, will navigate the top page.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="18edc-126">Devolver</span><span class="sxs-lookup"><span data-stu-id="18edc-126">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="18edc-127">frameid</span><span class="sxs-lookup"><span data-stu-id="18edc-127">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="18edc-128">ID do quadro que será navegada.</span><span class="sxs-lookup"><span data-stu-id="18edc-128">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="18edc-129">getFrameTree</span><span class="sxs-lookup"><span data-stu-id="18edc-129">getFrameTree</span></span>
<span data-ttu-id="18edc-130">Retorna a estrutura da árvore de quadros atual.</span><span class="sxs-lookup"><span data-stu-id="18edc-130">Returns present frame tree structure.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="18edc-131">Devolver</span><span class="sxs-lookup"><span data-stu-id="18edc-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="18edc-132">frameTree</span><span class="sxs-lookup"><span data-stu-id="18edc-132">frameTree</span></span></td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td><span data-ttu-id="18edc-133">Apresentar estrutura de árvore de quadros.</span><span class="sxs-lookup"><span data-stu-id="18edc-133">Present frame tree structure.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="18edc-134">Eventos</span><span class="sxs-lookup"><span data-stu-id="18edc-134">Events</span></span>

### <span data-ttu-id="18edc-135">frameAttached</span><span class="sxs-lookup"><span data-stu-id="18edc-135">frameAttached</span></span>
<span data-ttu-id="18edc-136">Disparado quando o quadro é anexado ao seu pai.</span><span class="sxs-lookup"><span data-stu-id="18edc-136">Fired when frame has been attached to its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="18edc-137">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18edc-137">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="18edc-138">frameid</span><span class="sxs-lookup"><span data-stu-id="18edc-138">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="18edc-139">ID do quadro que foi anexado.</span><span class="sxs-lookup"><span data-stu-id="18edc-139">Id of the frame that has been attached.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="18edc-140">parentFrameId</span><span class="sxs-lookup"><span data-stu-id="18edc-140">parentFrameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="18edc-141">Identificador de quadro pai.</span><span class="sxs-lookup"><span data-stu-id="18edc-141">Parent frame identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="18edc-142">empilh</span><span class="sxs-lookup"><span data-stu-id="18edc-142">stack</span></span> <br/> <i><span data-ttu-id="18edc-143">opcional</span><span class="sxs-lookup"><span data-stu-id="18edc-143">optional</span></span></i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td><span data-ttu-id="18edc-144">Rastreamento de pilha JavaScript de quando o quadro foi anexado, somente defina se o quadro foi iniciado a partir do script.</span><span class="sxs-lookup"><span data-stu-id="18edc-144">JavaScript stack trace of when frame was attached, only set if frame initiated from script.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="18edc-145">frameDetached</span><span class="sxs-lookup"><span data-stu-id="18edc-145">frameDetached</span></span>
<span data-ttu-id="18edc-146">Disparado quando o quadro é separado de seu pai.</span><span class="sxs-lookup"><span data-stu-id="18edc-146">Fired when frame has been detached from its parent.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="18edc-147">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18edc-147">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="18edc-148">frameid</span><span class="sxs-lookup"><span data-stu-id="18edc-148">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="18edc-149">ID do quadro que foi desconectado.</span><span class="sxs-lookup"><span data-stu-id="18edc-149">Id of the frame that has been detached.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="18edc-150">frameNavigated</span><span class="sxs-lookup"><span data-stu-id="18edc-150">frameNavigated</span></span>
<span data-ttu-id="18edc-151">Disparado após a conclusão da navegação do quadro.</span><span class="sxs-lookup"><span data-stu-id="18edc-151">Fired once navigation of the frame has completed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="18edc-152">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18edc-152">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="18edc-153">tempo</span><span class="sxs-lookup"><span data-stu-id="18edc-153">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="18edc-154">Objeto frame.</span><span class="sxs-lookup"><span data-stu-id="18edc-154">Frame object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="18edc-155">loadEventFired</span><span class="sxs-lookup"><span data-stu-id="18edc-155">loadEventFired</span></span>
<span data-ttu-id="18edc-156">Corresponde ao evento Window. OnLoad.</span><span class="sxs-lookup"><span data-stu-id="18edc-156">Corresponds to the window.onload event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="18edc-157">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18edc-157">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="18edc-158">carimbo</span><span class="sxs-lookup"><span data-stu-id="18edc-158">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="18edc-159">Número de milissegundos desde a época.</span><span class="sxs-lookup"><span data-stu-id="18edc-159">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="18edc-160">domContentEventFired</span><span class="sxs-lookup"><span data-stu-id="18edc-160">domContentEventFired</span></span>
<span data-ttu-id="18edc-161">Corresponde ao evento Document. onDOMContentLoaded.</span><span class="sxs-lookup"><span data-stu-id="18edc-161">Corresponds to the document.onDOMContentLoaded event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="18edc-162">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18edc-162">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="18edc-163">carimbo</span><span class="sxs-lookup"><span data-stu-id="18edc-163">timestamp</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="18edc-164">Número de milissegundos desde a época.</span><span class="sxs-lookup"><span data-stu-id="18edc-164">Number of milliseconds since epoch.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="18edc-165">Tipos</span><span class="sxs-lookup"><span data-stu-id="18edc-165">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="18edc-166">Frameid</span><span class="sxs-lookup"><span data-stu-id="18edc-166">FrameId</span></span> `string`

<span data-ttu-id="18edc-167">Identificador de quadro exclusivo.</span><span class="sxs-lookup"><span data-stu-id="18edc-167">Unique frame identifier.</span></span>

</p>

---

### <a name="frame"></a> <span data-ttu-id="18edc-168">Quadro</span><span class="sxs-lookup"><span data-stu-id="18edc-168">Frame</span></span> `object`

<span data-ttu-id="18edc-169">Informações sobre o quadro na página.</span><span class="sxs-lookup"><span data-stu-id="18edc-169">Information about the Frame on the Page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="18edc-170">Propriedades</span><span class="sxs-lookup"><span data-stu-id="18edc-170">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="18edc-171">id</span><span class="sxs-lookup"><span data-stu-id="18edc-171">id</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="18edc-172">Identificador exclusivo do quadro.</span><span class="sxs-lookup"><span data-stu-id="18edc-172">Frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="18edc-173">parentId</span><span class="sxs-lookup"><span data-stu-id="18edc-173">parentId</span></span> <br/> <i><span data-ttu-id="18edc-174">opcional</span><span class="sxs-lookup"><span data-stu-id="18edc-174">optional</span></span></i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span data-ttu-id="18edc-175">Identificador exclusivo do quadro pai.</span><span class="sxs-lookup"><span data-stu-id="18edc-175">Parent frame unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="18edc-176">name</span><span class="sxs-lookup"><span data-stu-id="18edc-176">name</span></span> <br/> <i><span data-ttu-id="18edc-177">opcional</span><span class="sxs-lookup"><span data-stu-id="18edc-177">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="18edc-178">Nome do quadro, conforme especificado na marca.</span><span class="sxs-lookup"><span data-stu-id="18edc-178">Frame's name as specified in the tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="18edc-179">url</span><span class="sxs-lookup"><span data-stu-id="18edc-179">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="18edc-180">URL do documento de quadro.</span><span class="sxs-lookup"><span data-stu-id="18edc-180">Frame document's URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="18edc-181">securityOrigin</span><span class="sxs-lookup"><span data-stu-id="18edc-181">securityOrigin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="18edc-182">Origem de segurança do documento de quadro.</span><span class="sxs-lookup"><span data-stu-id="18edc-182">Frame document's security origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="18edc-183">MIME</span><span class="sxs-lookup"><span data-stu-id="18edc-183">mimeType</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="18edc-184">MimeType do documento de quadro conforme determinado pelo navegador.</span><span class="sxs-lookup"><span data-stu-id="18edc-184">Frame document's mimeType as determined by the browser.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> <span data-ttu-id="18edc-185">FrameTree</span><span class="sxs-lookup"><span data-stu-id="18edc-185">FrameTree</span></span> `object`

<span data-ttu-id="18edc-186">Informações sobre a hierarquia de quadros.</span><span class="sxs-lookup"><span data-stu-id="18edc-186">Information about the Frame hierarchy.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="18edc-187">Propriedades</span><span class="sxs-lookup"><span data-stu-id="18edc-187">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="18edc-188">tempo</span><span class="sxs-lookup"><span data-stu-id="18edc-188">frame</span></span></td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td><span data-ttu-id="18edc-189">Informações de quadro para este item de árvore.</span><span class="sxs-lookup"><span data-stu-id="18edc-189">Frame information for this tree item.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="18edc-190">childFrames</span><span class="sxs-lookup"><span data-stu-id="18edc-190">childFrames</span></span> <br/> <i><span data-ttu-id="18edc-191">opcional</span><span class="sxs-lookup"><span data-stu-id="18edc-191">optional</span></span></i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td><span data-ttu-id="18edc-192">Quadros filho.</span><span class="sxs-lookup"><span data-stu-id="18edc-192">Child frames.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
