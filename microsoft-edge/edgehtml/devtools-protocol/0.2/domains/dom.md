---
description: Referência para o domínio DOM. Esse domínio apresenta operações DOM de leitura/gravação. Cada nó DOM é representado com seu objeto espelho que tem um `id` . Isso `id` pode ser usado para obter informações adicionais sobre o nó, solucioná-lo para o invólucro do objeto JavaScript, etc. É importante que o cliente receba eventos DOM somente para os nós conhecidos do cliente. O back-end mantém o controle dos nós que foram enviados para o cliente e nunca envia o mesmo nó duas vezes. É responsabilidade do cliente coletar informações sobre os nós que foram enviados ao cliente.<p>Observe que `iframe` os elementos Owner retornarão elementos de documento correspondentes como seus nós filho.</p>
title: DOM Domain – protocolo DevTools versão 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7d9861a2395f7b24142a41efea9ac599907dec27
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231686"
---
# <span data-ttu-id="ce882-109">DOM</span><span class="sxs-lookup"><span data-stu-id="ce882-109">DOM</span></span>

<span data-ttu-id="ce882-110">Esse domínio apresenta operações DOM de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ce882-110">This domain exposes DOM read/write operations.</span></span> <span data-ttu-id="ce882-111">Cada nó DOM é representado com seu objeto espelho que tem um `id` .</span><span class="sxs-lookup"><span data-stu-id="ce882-111">Each DOM Node is represented with its mirror object that has an `id`.</span></span> <span data-ttu-id="ce882-112">Isso `id` pode ser usado para obter informações adicionais sobre o nó, solucioná-lo para o invólucro do objeto JavaScript, etc. É importante que o cliente receba eventos DOM somente para os nós conhecidos do cliente.</span><span class="sxs-lookup"><span data-stu-id="ce882-112">This `id` can be used to get additional information on the Node, resolve it into the JavaScript object wrapper, etc. It is important that client receives DOM events only for the nodes that are known to the client.</span></span> <span data-ttu-id="ce882-113">O back-end mantém o controle dos nós que foram enviados para o cliente e nunca envia o mesmo nó duas vezes.</span><span class="sxs-lookup"><span data-stu-id="ce882-113">Backend keeps track of the nodes that were sent to the client and never sends the same node twice.</span></span> <span data-ttu-id="ce882-114">É responsabilidade do cliente coletar informações sobre os nós que foram enviados ao cliente.</span><span class="sxs-lookup"><span data-stu-id="ce882-114">It is client's responsibility to collect information about the nodes that were sent to the client.</span></span><p><span data-ttu-id="ce882-115">Observe que `iframe` os elementos Owner retornarão elementos de documento correspondentes como seus nós filho.</span><span class="sxs-lookup"><span data-stu-id="ce882-115">Note that `iframe` owner elements will return corresponding document elements as their child nodes.</span></span></p>

| | |
|-|-|
| [**<span data-ttu-id="ce882-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce882-116">Methods</span></span>**](#methods) | <span data-ttu-id="ce882-117">[habilitar](#enable), [desabilitar](#disable), [GetDocument](#getdocument), [HighlightNode](#highlightnode), [hideHighlight](#hidehighlight), [requestChildNodes](#requestchildnodes), [GetAttributes](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector), [querySelectorAll](#queryselectorall), [requestNode](#requestnode), [resolveNode](#resolvenode), [setInspectedNode](#setinspectednode)</span><span class="sxs-lookup"><span data-stu-id="ce882-117">[enable](#enable), [disable](#disable), [getDocument](#getdocument), [highlightNode](#highlightnode), [hideHighlight](#hidehighlight), [requestChildNodes](#requestchildnodes), [getAttributes](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector), [querySelectorAll](#queryselectorall), [requestNode](#requestnode), [resolveNode](#resolvenode), [setInspectedNode](#setinspectednode)</span></span> |
| [**<span data-ttu-id="ce882-118">Eventos</span><span class="sxs-lookup"><span data-stu-id="ce882-118">Events</span></span>**](#events) | <span data-ttu-id="ce882-119">[setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated)</span><span class="sxs-lookup"><span data-stu-id="ce882-119">[setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated)</span></span> |
| [**<span data-ttu-id="ce882-120">Tipos</span><span class="sxs-lookup"><span data-stu-id="ce882-120">Types</span></span>**](#types) | <span data-ttu-id="ce882-121">[RGBA](#rgba), [HighlightConfig](#highlightconfig), [NodeId](#nodeid), [node](#node), [BackendNodeId](#backendnodeid), [pseudotype](#pseudotype)</span><span class="sxs-lookup"><span data-stu-id="ce882-121">[RGBA](#rgba), [HighlightConfig](#highlightconfig), [NodeId](#nodeid), [Node](#node), [BackendNodeId](#backendnodeid), [PseudoType](#pseudotype)</span></span> |
| [**<span data-ttu-id="ce882-122">Dependências</span><span class="sxs-lookup"><span data-stu-id="ce882-122">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="ce882-123">Tempo de Execução</span><span class="sxs-lookup"><span data-stu-id="ce882-123">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="ce882-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce882-124">Methods</span></span>

### <span data-ttu-id="ce882-125">Habilitar</span><span class="sxs-lookup"><span data-stu-id="ce882-125">enable</span></span>
<span data-ttu-id="ce882-126">Habilita o agente DOM para a página especificada.</span><span class="sxs-lookup"><span data-stu-id="ce882-126">Enables DOM agent for the given page.</span></span>

</p>

---

### <span data-ttu-id="ce882-127">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="ce882-127">disable</span></span>
<span data-ttu-id="ce882-128">Desabilita o agente DOM para a página especificada.</span><span class="sxs-lookup"><span data-stu-id="ce882-128">Disables DOM agent for the given page.</span></span> <span data-ttu-id="ce882-129">Desabilitar o DOM invalidará qualquer nodeIds válido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ce882-129">Disabling the DOM will invalidate any previously valid nodeIds.</span></span>

</p>

---

### <span data-ttu-id="ce882-130">GetDocument</span><span class="sxs-lookup"><span data-stu-id="ce882-130">getDocument</span></span>
<span data-ttu-id="ce882-131">Retorna o nó DOM raiz (e, opcionalmente, a subárvore) para o chamador.</span><span class="sxs-lookup"><span data-stu-id="ce882-131">Returns the root DOM node (and optionally the subtree) to the caller.</span></span> <span data-ttu-id="ce882-132">A chamada `getDocument` invalidará qualquer nodeIds válido anteriormente</span><span class="sxs-lookup"><span data-stu-id="ce882-132">Calling `getDocument` will invalidate any previously valid nodeIds</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-133">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-133">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-134">profundo</span><span class="sxs-lookup"><span data-stu-id="ce882-134">depth</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ce882-135">A profundidade máxima na qual os filhos devem ser recuperados, o padrão é 2.</span><span class="sxs-lookup"><span data-stu-id="ce882-135">The maximum depth at which children should be retrieved, defaults to 2.</span></span> <span data-ttu-id="ce882-136">Use-1 para subárvore inteira.</span><span class="sxs-lookup"><span data-stu-id="ce882-136">Use -1 for entire subtree.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-137">Pierce</span><span class="sxs-lookup"><span data-stu-id="ce882-137">pierce</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="ce882-138">Se os iframes devem ou não ser percorridos ao retornar a subárvore (o padrão é falso).</span><span class="sxs-lookup"><span data-stu-id="ce882-138">Whether or not iframes should be traversed when returning the subtree (default is false).</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-139">Devolver</span><span class="sxs-lookup"><span data-stu-id="ce882-139">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-140">raiz</span><span class="sxs-lookup"><span data-stu-id="ce882-140">root</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="ce882-141">Nó resultante.</span><span class="sxs-lookup"><span data-stu-id="ce882-141">Resulting Node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ce882-142">highlightNode</span><span class="sxs-lookup"><span data-stu-id="ce882-142">highlightNode</span></span>
<span data-ttu-id="ce882-143">Nó DOM higlights com ID ou wrapper de objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="ce882-143">Higlights DOM node with given id or object wrapper.</span></span> <span data-ttu-id="ce882-144">NodeId, backendNodeId ou objectId deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="ce882-144">nodeId, backendNodeId, or objectId must be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-145">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-145">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-146">NodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-146">nodeId</span></span> <br/> <i><span data-ttu-id="ce882-147">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-147">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-148">Identificador do nó a ser realçado.</span><span class="sxs-lookup"><span data-stu-id="ce882-148">Identifier of the node to highlight.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-149">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-149">backendNodeId</span></span> <br/> <i><span data-ttu-id="ce882-150">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-150">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="ce882-151">Identificador do nó back-end a ser realçado.</span><span class="sxs-lookup"><span data-stu-id="ce882-151">Identifier of the backend node to highlight.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-152">objectId</span><span class="sxs-lookup"><span data-stu-id="ce882-152">objectId</span></span> <br/> <i><span data-ttu-id="ce882-153">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-153">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="ce882-154">ID do objeto JavaScript do nó a ser realçado.</span><span class="sxs-lookup"><span data-stu-id="ce882-154">JavaScript object id of the node to be highlighted.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-155">higlightConfig</span><span class="sxs-lookup"><span data-stu-id="ce882-155">higlightConfig</span></span></td>
            <td><a href="#highlightconfig"><code class="flyout">HighlightConfig</code></a></td>
            <td><span data-ttu-id="ce882-156">Descritor da aparência do realce.</span><span class="sxs-lookup"><span data-stu-id="ce882-156">Descriptor of the highlight appearance.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-157">Devolver</span><span class="sxs-lookup"><span data-stu-id="ce882-157">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-158">raiz</span><span class="sxs-lookup"><span data-stu-id="ce882-158">root</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="ce882-159">Nó resultante.</span><span class="sxs-lookup"><span data-stu-id="ce882-159">Resulting Node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ce882-160">hideHighlight</span><span class="sxs-lookup"><span data-stu-id="ce882-160">hideHighlight</span></span>
<span data-ttu-id="ce882-161">Oculta qualquer realce do nó DOM atual.</span><span class="sxs-lookup"><span data-stu-id="ce882-161">Hides any current DOM node highlight.</span></span>

</p>

---

### <span data-ttu-id="ce882-162">requestChildNodes</span><span class="sxs-lookup"><span data-stu-id="ce882-162">requestChildNodes</span></span>
<span data-ttu-id="ce882-163">Solicitações que os filhos do nó com ID fornecida são retornadas para o chamador Ghe na forma de `setChildNodes` eventos.</span><span class="sxs-lookup"><span data-stu-id="ce882-163">Requests that children of the node with given id are returned to ghe caller in the form of `setChildNodes` events.</span></span> `setChildNodes` <span data-ttu-id="ce882-164">será disparado para cada nó que não tenha sido retornado anteriormente, a partir do nó solicitado até a profundidade especificada.</span><span class="sxs-lookup"><span data-stu-id="ce882-164">will be fired for each node that has not previously returned it's children, starting from the requested node down to the specified depth.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-165">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-165">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-166">NodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-166">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-167">ID do nó do qual obter filhos.</span><span class="sxs-lookup"><span data-stu-id="ce882-167">Id of the node to get children from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-168">profundo</span><span class="sxs-lookup"><span data-stu-id="ce882-168">depth</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ce882-169">A profundidade máxima na qual os filhos devem ser recuperados, o padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="ce882-169">The maximum depth at which children should be retrieved, defaults to 1.</span></span> <span data-ttu-id="ce882-170">Use-1 para subárvore inteira.</span><span class="sxs-lookup"><span data-stu-id="ce882-170">Use -1 for entire subtree.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-171">Pierce</span><span class="sxs-lookup"><span data-stu-id="ce882-171">pierce</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="ce882-172">Se os iframes devem ou não ser percorridos ao retornar a subárvore (o padrão é falso).</span><span class="sxs-lookup"><span data-stu-id="ce882-172">Whether or not iframes should be traversed when returning the subtree (default is false).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ce882-173">GetAttributes</span><span class="sxs-lookup"><span data-stu-id="ce882-173">getAttributes</span></span>
<span data-ttu-id="ce882-174">Retorna atributos para o nó especificado.</span><span class="sxs-lookup"><span data-stu-id="ce882-174">Returns attributes for the specified node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-175">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-175">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-176">NodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-176">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-177">ID do nó para o qual recuperar o attibutes.</span><span class="sxs-lookup"><span data-stu-id="ce882-177">Id of the node to retrieve attibutes for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-178">Devolver</span><span class="sxs-lookup"><span data-stu-id="ce882-178">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-179">Attribute</span><span class="sxs-lookup"><span data-stu-id="ce882-179">attributes</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="ce882-180">Uma matriz entrelaçada de nomes e valores de atributo de nó.</span><span class="sxs-lookup"><span data-stu-id="ce882-180">An interleaved array of node attribute names and values.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ce882-181">getOuterHTML</span><span class="sxs-lookup"><span data-stu-id="ce882-181">getOuterHTML</span></span>
<span data-ttu-id="ce882-182">Retorna a marcação HTML do nó.</span><span class="sxs-lookup"><span data-stu-id="ce882-182">Returns node's HTML markup.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-183">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-183">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-184">NodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-184">nodeId</span></span> <br/> <i><span data-ttu-id="ce882-185">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-185">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-186">Identificador do nó.</span><span class="sxs-lookup"><span data-stu-id="ce882-186">Identifier of the node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-187">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-187">backendNodeId</span></span> <br/> <i><span data-ttu-id="ce882-188">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-188">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="ce882-189">Identificador do nó back-end.</span><span class="sxs-lookup"><span data-stu-id="ce882-189">Identifier of the backend node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-190">objectId</span><span class="sxs-lookup"><span data-stu-id="ce882-190">objectId</span></span> <br/> <i><span data-ttu-id="ce882-191">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-191">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="ce882-192">ID de objeto JavaScript do invólucro de nó.</span><span class="sxs-lookup"><span data-stu-id="ce882-192">JavaScript object id of the node wrapper.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-193">Devolver</span><span class="sxs-lookup"><span data-stu-id="ce882-193">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-194">outerHTML</span><span class="sxs-lookup"><span data-stu-id="ce882-194">outerHTML</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ce882-195">Marcação HTML externa.</span><span class="sxs-lookup"><span data-stu-id="ce882-195">Outer HTML markup.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ce882-196">pushNodesByBackendIdsToFrontend</span><span class="sxs-lookup"><span data-stu-id="ce882-196">pushNodesByBackendIdsToFrontend</span></span>
<span data-ttu-id="ce882-197">Procura IDs de nó e resolve todos os pais para as IDs de nó de back-end especificadas</span><span class="sxs-lookup"><span data-stu-id="ce882-197">Looks up Node Ids and resolves all parents for the specified Backend Node Ids</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-198">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-198">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-199">backendNodeIds</span><span class="sxs-lookup"><span data-stu-id="ce882-199">backendNodeIds</span></span></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId[]</code></a></td>
            <td><span data-ttu-id="ce882-200">IDs de nó de back-end dos nós a serem resolvidos</span><span class="sxs-lookup"><span data-stu-id="ce882-200">Backend Node IDs of the nodes to resolve</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-201">Devolver</span><span class="sxs-lookup"><span data-stu-id="ce882-201">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-202">nodeIds</span><span class="sxs-lookup"><span data-stu-id="ce882-202">nodeIds</span></span></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td><span data-ttu-id="ce882-203">IDs de nó dos nós resolvidos</span><span class="sxs-lookup"><span data-stu-id="ce882-203">Node Ids of the resolved nodes</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ce882-204">querySelector</span><span class="sxs-lookup"><span data-stu-id="ce882-204">querySelector</span></span>
<span data-ttu-id="ce882-205">Executa `querySelector` em um determinado nó.</span><span class="sxs-lookup"><span data-stu-id="ce882-205">Executes `querySelector` on a given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-206">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-207">NodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-207">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-208">ID do nó para consulta.</span><span class="sxs-lookup"><span data-stu-id="ce882-208">Id of the node to query upon.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-209">seletor</span><span class="sxs-lookup"><span data-stu-id="ce882-209">selector</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ce882-210">A cadeia de caracteres do seletor.</span><span class="sxs-lookup"><span data-stu-id="ce882-210">The selector string.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-211">Devolver</span><span class="sxs-lookup"><span data-stu-id="ce882-211">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-212">NodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-212">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-213">Resultado do seletor de consulta.</span><span class="sxs-lookup"><span data-stu-id="ce882-213">Query selector result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ce882-214">querySelectorAll</span><span class="sxs-lookup"><span data-stu-id="ce882-214">querySelectorAll</span></span>
<span data-ttu-id="ce882-215">Executa `querySelectorAll` em um determinado nó.</span><span class="sxs-lookup"><span data-stu-id="ce882-215">Executes `querySelectorAll` on a given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-216">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-216">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-217">NodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-217">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-218">ID do nó para consulta.</span><span class="sxs-lookup"><span data-stu-id="ce882-218">Id of the node to query upon.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-219">seletor</span><span class="sxs-lookup"><span data-stu-id="ce882-219">selector</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ce882-220">A cadeia de caracteres do seletor.</span><span class="sxs-lookup"><span data-stu-id="ce882-220">The selector string.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-221">Devolver</span><span class="sxs-lookup"><span data-stu-id="ce882-221">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-222">nodeIds</span><span class="sxs-lookup"><span data-stu-id="ce882-222">nodeIds</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td><span data-ttu-id="ce882-223">Resultados do seletor de consulta.</span><span class="sxs-lookup"><span data-stu-id="ce882-223">Query selector results.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ce882-224">requestNode</span><span class="sxs-lookup"><span data-stu-id="ce882-224">requestNode</span></span>
<span data-ttu-id="ce882-225">Solicita que o nó com a ID de objeto remoto fornecido seja enviado ao chamador.</span><span class="sxs-lookup"><span data-stu-id="ce882-225">Requests that the node with given remote object Id is sent to caller.</span></span> <span data-ttu-id="ce882-226">Todos os nós que formam o caminho do nó para a raiz também são enviados ao cliente como uma série de `setChildNodes` notificações.</span><span class="sxs-lookup"><span data-stu-id="ce882-226">All nodes that form the path from the node to the root are also sent to the client as a series of `setChildNodes` notifications.</span></span> <span data-ttu-id="ce882-227">Retorna 0 se o documento que contém o nó solicitado não tiver sido solicitado anteriormente pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="ce882-227">returns 0 if the document containing the requested node has not previously been requested by the client.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-228">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-228">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-229">objectId</span><span class="sxs-lookup"><span data-stu-id="ce882-229">objectId</span></span></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td><span data-ttu-id="ce882-230">ID do objeto JavaScript para converter em nó.</span><span class="sxs-lookup"><span data-stu-id="ce882-230">JavaScript object Id to convert into node.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-231">Devolver</span><span class="sxs-lookup"><span data-stu-id="ce882-231">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-232">NodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-232">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-233">ID do nó para determinado objeto.</span><span class="sxs-lookup"><span data-stu-id="ce882-233">Node Id for given object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ce882-234">resolveNode</span><span class="sxs-lookup"><span data-stu-id="ce882-234">resolveNode</span></span>
<span data-ttu-id="ce882-235">Resolve o objeto de nó JavaScript para um determinado NodeId ou BackendNodeId.</span><span class="sxs-lookup"><span data-stu-id="ce882-235">Resolves the JavaScript node object for a given NodeId or BackendNodeId.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-236">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-236">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-237">NodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-237">nodeId</span></span> <br/> <i><span data-ttu-id="ce882-238">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-238">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-239">ID do nó a ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="ce882-239">Id of the node to resolve.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-240">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-240">backendNodeId</span></span> <br/> <i><span data-ttu-id="ce882-241">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-241">optional</span></span></i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td><span data-ttu-id="ce882-242">ID do nó back-end do nó a ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="ce882-242">Backend Node Id of the node to resolve.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-243">objeto de objeto</span><span class="sxs-lookup"><span data-stu-id="ce882-243">objectGroup</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ce882-244">Nome do grupo simbólico que pode ser usado para liberar vários objetos.</span><span class="sxs-lookup"><span data-stu-id="ce882-244">Symbolic group name that can be used to release multiple objects.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-245">Devolver</span><span class="sxs-lookup"><span data-stu-id="ce882-245">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-246">object</span><span class="sxs-lookup"><span data-stu-id="ce882-246">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="ce882-247">Wrapper do objeto JavaScript para o nó fornecido.</span><span class="sxs-lookup"><span data-stu-id="ce882-247">JavaScript object wrapper for given node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ce882-248">setInspectedNode</span><span class="sxs-lookup"><span data-stu-id="ce882-248">setInspectedNode</span></span>
<span><b><span data-ttu-id="ce882-249">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="ce882-249">Experimental.</span></span> </b></span><span data-ttu-id="ce882-250">Permite que o console se refira ao nó inspecionado anterior com uma determinada ID via $0-$ 4.</span><span class="sxs-lookup"><span data-stu-id="ce882-250">Enables console to refer to the previous inspected node with given id via $0-$4.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-251">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-251">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-252">NodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-252">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-253">ID do nó DOM para ser acessível por meio de $0-$ 4 na API da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="ce882-253">DOM node id to be accessible by means of $0-$4 in command line API.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="ce882-254">Eventos</span><span class="sxs-lookup"><span data-stu-id="ce882-254">Events</span></span>

### <span data-ttu-id="ce882-255">setChildNodes</span><span class="sxs-lookup"><span data-stu-id="ce882-255">setChildNodes</span></span>
<span data-ttu-id="ce882-256">Disparado quando o back-end deseja fornecer ao cliente a estrutura DOM ausente.</span><span class="sxs-lookup"><span data-stu-id="ce882-256">Fired when the backend wishes to provide client with missing DOM structure.</span></span> <span data-ttu-id="ce882-257">Isso acontece na maioria das chamadas solicitando nodeIds</span><span class="sxs-lookup"><span data-stu-id="ce882-257">This happens upon most calls requesting nodeIds</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-258">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-258">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-259">parentId</span><span class="sxs-lookup"><span data-stu-id="ce882-259">parentId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-260">Nó pai para poplate com filhos.</span><span class="sxs-lookup"><span data-stu-id="ce882-260">Parent node to poplate with children.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-261">Nós</span><span class="sxs-lookup"><span data-stu-id="ce882-261">nodes</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td><span data-ttu-id="ce882-262">Matriz de nós filho.</span><span class="sxs-lookup"><span data-stu-id="ce882-262">Child nodes array.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ce882-263">attributeModified</span><span class="sxs-lookup"><span data-stu-id="ce882-263">attributeModified</span></span>
<span data-ttu-id="ce882-264">Disparado quando o `Element` atributo for modificado.</span><span class="sxs-lookup"><span data-stu-id="ce882-264">Fired when `Element`'s attribute is modified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-265">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-265">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-266">NodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-266">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-267">ID do nó que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ce882-267">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-268">name</span><span class="sxs-lookup"><span data-stu-id="ce882-268">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ce882-269">Nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="ce882-269">Attribute name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-270">value</span><span class="sxs-lookup"><span data-stu-id="ce882-270">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ce882-271">Valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="ce882-271">Attribute value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ce882-272">attributeRemoved</span><span class="sxs-lookup"><span data-stu-id="ce882-272">attributeRemoved</span></span>
<span data-ttu-id="ce882-273">Disparado quando o `Element` atributo for removido.</span><span class="sxs-lookup"><span data-stu-id="ce882-273">Fired when `Element`'s attribute is removed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-274">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-274">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-275">NodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-275">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-276">ID do nó que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ce882-276">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-277">name</span><span class="sxs-lookup"><span data-stu-id="ce882-277">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ce882-278">Nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="ce882-278">Attribute name.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ce882-279">characterDataModified</span><span class="sxs-lookup"><span data-stu-id="ce882-279">characterDataModified</span></span>
<span data-ttu-id="ce882-280">Evento de espelhos `DOMCharacterDataModified` .</span><span class="sxs-lookup"><span data-stu-id="ce882-280">Mirrors `DOMCharacterDataModified` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-281">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-281">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-282">NodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-282">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-283">ID do nó que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ce882-283">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-284">charcterData</span><span class="sxs-lookup"><span data-stu-id="ce882-284">charcterData</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ce882-285">Novo valor de texto.</span><span class="sxs-lookup"><span data-stu-id="ce882-285">New text value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ce882-286">childNodeInserted</span><span class="sxs-lookup"><span data-stu-id="ce882-286">childNodeInserted</span></span>
<span data-ttu-id="ce882-287">Evento de espelhos `DOMNodeInserted` .</span><span class="sxs-lookup"><span data-stu-id="ce882-287">Mirrors `DOMNodeInserted` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-288">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-288">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-289">parentNodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-289">parentNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-290">ID do nó que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ce882-290">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-291">previousNodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-291">previousNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-292">ID do irmão anterior do nó inserido.</span><span class="sxs-lookup"><span data-stu-id="ce882-292">Id of the inserted node's previous sibling.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-293">nó</span><span class="sxs-lookup"><span data-stu-id="ce882-293">node</span></span></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="ce882-294">Dados de nó inseridos.</span><span class="sxs-lookup"><span data-stu-id="ce882-294">Inserted node data.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ce882-295">childNodeRemoved</span><span class="sxs-lookup"><span data-stu-id="ce882-295">childNodeRemoved</span></span>
<span data-ttu-id="ce882-296">Evento de espelhos `DOMNodeRemoved` .</span><span class="sxs-lookup"><span data-stu-id="ce882-296">Mirrors `DOMNodeRemoved` event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-297">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce882-297">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-298">parentNodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-298">parentNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-299">ID do nó que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ce882-299">Id of the node that has changed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-300">NodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-300">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-301">ID do nó que foi removido.</span><span class="sxs-lookup"><span data-stu-id="ce882-301">Id of the node that has been removed.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="ce882-302">documentUpdated</span><span class="sxs-lookup"><span data-stu-id="ce882-302">documentUpdated</span></span>
<span data-ttu-id="ce882-303">Acionado quando foi `Document` totalmente atualizado.</span><span class="sxs-lookup"><span data-stu-id="ce882-303">Fired when `Document` has been totally updated.</span></span> <span data-ttu-id="ce882-304">As IDs de nó não são mais válidas.</span><span class="sxs-lookup"><span data-stu-id="ce882-304">Node ids are no longer valid.</span></span>

</p>

---

## <span data-ttu-id="ce882-305">Tipos</span><span class="sxs-lookup"><span data-stu-id="ce882-305">Types</span></span>

### <a name="rgba"></a> <span data-ttu-id="ce882-306">RGBA</span><span class="sxs-lookup"><span data-stu-id="ce882-306">RGBA</span></span> `object`

<span data-ttu-id="ce882-307">Uma estrutura que contém uma cor RGBA.</span><span class="sxs-lookup"><span data-stu-id="ce882-307">A Structure holding an RGBA color.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-308">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ce882-308">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-309">r</span><span class="sxs-lookup"><span data-stu-id="ce882-309">r</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ce882-310">O componente vermelho, no intervalo [0-255].</span><span class="sxs-lookup"><span data-stu-id="ce882-310">The red component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-311">p</span><span class="sxs-lookup"><span data-stu-id="ce882-311">g</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ce882-312">O componente verde, no intervalo [0-255].</span><span class="sxs-lookup"><span data-stu-id="ce882-312">The green component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-313">b</span><span class="sxs-lookup"><span data-stu-id="ce882-313">b</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ce882-314">O componente azul, no intervalo [0-255].</span><span class="sxs-lookup"><span data-stu-id="ce882-314">The blue component, in the [0-255] range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-315">a</span><span class="sxs-lookup"><span data-stu-id="ce882-315">a</span></span> <br/> <i><span data-ttu-id="ce882-316">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-316">optional</span></span></i></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="ce882-317">O componente alfa, no intervalo [0-1].</span><span class="sxs-lookup"><span data-stu-id="ce882-317">The alpha component, in the [0-1] range.</span></span> <span data-ttu-id="ce882-318">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="ce882-318">Default is 1.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="highlightconfig"></a> <span data-ttu-id="ce882-319">HighlightConfig</span><span class="sxs-lookup"><span data-stu-id="ce882-319">HighlightConfig</span></span> `object`

<span data-ttu-id="ce882-320">Dados de configuração para realce de elementos de página.</span><span class="sxs-lookup"><span data-stu-id="ce882-320">Configuration data for highlighting of page elements.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-321">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ce882-321">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-322">contentColor</span><span class="sxs-lookup"><span data-stu-id="ce882-322">contentColor</span></span> <br/> <i><span data-ttu-id="ce882-323">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-323">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="ce882-324">A caixa de conteúdo realçar cor de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="ce882-324">The content box highlight fill color.</span></span> <span data-ttu-id="ce882-325">O padrão é transparente.</span><span class="sxs-lookup"><span data-stu-id="ce882-325">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-326">paddingColor</span><span class="sxs-lookup"><span data-stu-id="ce882-326">paddingColor</span></span> <br/> <i><span data-ttu-id="ce882-327">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-327">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="ce882-328">A cor de preenchimento da realce de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="ce882-328">The padding highlight fill color.</span></span> <span data-ttu-id="ce882-329">O padrão é transparente.</span><span class="sxs-lookup"><span data-stu-id="ce882-329">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-330">CorDaBorda</span><span class="sxs-lookup"><span data-stu-id="ce882-330">borderColor</span></span> <br/> <i><span data-ttu-id="ce882-331">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-331">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="ce882-332">A borda realce cor de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="ce882-332">The border highlight fill color.</span></span> <span data-ttu-id="ce882-333">O padrão é transparente.</span><span class="sxs-lookup"><span data-stu-id="ce882-333">Default is transparent.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-334">marginColor</span><span class="sxs-lookup"><span data-stu-id="ce882-334">marginColor</span></span> <br/> <i><span data-ttu-id="ce882-335">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-335">optional</span></span></i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td><span data-ttu-id="ce882-336">A cor de preenchimento da margem de realce.</span><span class="sxs-lookup"><span data-stu-id="ce882-336">The margin highlight fill color.</span></span> <span data-ttu-id="ce882-337">O padrão é transparente.</span><span class="sxs-lookup"><span data-stu-id="ce882-337">Default is transparent.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="nodeid"></a> <span data-ttu-id="ce882-338">NodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-338">NodeId</span></span> `integer`

<span data-ttu-id="ce882-339">Identificador de nó DOM exclusivo</span><span class="sxs-lookup"><span data-stu-id="ce882-339">Unique DOM node identifier</span></span>

</p>

---

### <a name="node"></a> <span data-ttu-id="ce882-340">Nó</span><span class="sxs-lookup"><span data-stu-id="ce882-340">Node</span></span> `object`

<span data-ttu-id="ce882-341">Objeto espelho que representa os nós DOM reais.</span><span class="sxs-lookup"><span data-stu-id="ce882-341">Mirror object that represents the actual DOM nodes.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="ce882-342">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ce882-342">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="ce882-343">NodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-343">nodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-344">Identificador de nó usado para fazer referência a esse nó.</span><span class="sxs-lookup"><span data-stu-id="ce882-344">Node Identifier used to reference this node.</span></span> <span data-ttu-id="ce882-345">O backend irá disparar eventos DOM para nós que têm um NodeId conhecido para o cliente</span><span class="sxs-lookup"><span data-stu-id="ce882-345">Backend will fire DOM events for nodes that have a nodeId that is known to the client</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-346">parentId</span><span class="sxs-lookup"><span data-stu-id="ce882-346">parentId</span></span> <br/> <i><span data-ttu-id="ce882-347">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-347">optional</span></span></i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-348">Identificador de nó do nó pai, se houver.</span><span class="sxs-lookup"><span data-stu-id="ce882-348">Node Identifier of the parent Node, if any.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-349">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-349">backendNodeId</span></span></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td><span data-ttu-id="ce882-350">Identificador de nó de back-end do nó.</span><span class="sxs-lookup"><span data-stu-id="ce882-350">Backend Node identifier of the node.</span></span> <span data-ttu-id="ce882-351">BackendNodeIds nós de referência que podem ser conhecidos pelo cliente, mas não enviem eventos DOM sobre esse nó.</span><span class="sxs-lookup"><span data-stu-id="ce882-351">BackendNodeIds reference Nodes that can be known to the client, but do not push DOM events about this node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-352">nodeType</span><span class="sxs-lookup"><span data-stu-id="ce882-352">nodeType</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td>`Node`<span data-ttu-id="ce882-353">nodeType do.</span><span class="sxs-lookup"><span data-stu-id="ce882-353">'s nodeType.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-354">Node</span><span class="sxs-lookup"><span data-stu-id="ce882-354">nodeName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="ce882-355">NodeName.</span><span class="sxs-lookup"><span data-stu-id="ce882-355">'s nodeName.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-356">localName</span><span class="sxs-lookup"><span data-stu-id="ce882-356">localName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="ce882-357">localName do</span><span class="sxs-lookup"><span data-stu-id="ce882-357">'s localName</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-358">NodeValue</span><span class="sxs-lookup"><span data-stu-id="ce882-358">nodeValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td>`Node`<span data-ttu-id="ce882-359">NodeValue</span><span class="sxs-lookup"><span data-stu-id="ce882-359">'s nodeValue</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-360">childNodeCount</span><span class="sxs-lookup"><span data-stu-id="ce882-360">childNodeCount</span></span> <br/> <i><span data-ttu-id="ce882-361">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-361">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="ce882-362">Contagem filho para `Container` nós.</span><span class="sxs-lookup"><span data-stu-id="ce882-362">Child count for `Container` nodes.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-363">menores de idade</span><span class="sxs-lookup"><span data-stu-id="ce882-363">children</span></span> <br/> <i><span data-ttu-id="ce882-364">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-364">optional</span></span></i></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td><span data-ttu-id="ce882-365">Nós filho deste nó quando solicitado com filhos.</span><span class="sxs-lookup"><span data-stu-id="ce882-365">Child nodes of this node when requested with children.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-366">Attribute</span><span class="sxs-lookup"><span data-stu-id="ce882-366">attributes</span></span> <br/> <i><span data-ttu-id="ce882-367">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-367">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="ce882-368">Atributos de `Element` nós na forma de uma matriz plana ' [Nome1, valor1, Nome2, valor2]</span><span class="sxs-lookup"><span data-stu-id="ce882-368">Attributes of `Element` nodes in the form of a flat array \`[name1, value1, name2, value2]</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-369">documentURL</span><span class="sxs-lookup"><span data-stu-id="ce882-369">documentURL</span></span> <br/> <i><span data-ttu-id="ce882-370">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-370">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ce882-371">URL do documento para o qual os `Document` nós apontam.</span><span class="sxs-lookup"><span data-stu-id="ce882-371">Document URL that `Document` nodes point to.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-372">baseURL</span><span class="sxs-lookup"><span data-stu-id="ce882-372">baseURL</span></span> <br/> <i><span data-ttu-id="ce882-373">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-373">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="ce882-374">URL do documento `Document` usada pelos nós para completar a URL.</span><span class="sxs-lookup"><span data-stu-id="ce882-374">Document URL that `Document` nodes use for URL completion.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-375">PublicId</span><span class="sxs-lookup"><span data-stu-id="ce882-375">publicId</span></span> <br/> <i><span data-ttu-id="ce882-376">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-376">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="ce882-377">PublicId do nó.</span><span class="sxs-lookup"><span data-stu-id="ce882-377">Node's publicId.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-378">SystemId</span><span class="sxs-lookup"><span data-stu-id="ce882-378">systemId</span></span> <br/> <i><span data-ttu-id="ce882-379">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-379">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="ce882-380">SystemId do nó.</span><span class="sxs-lookup"><span data-stu-id="ce882-380">Node's systemId.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-381">internalSubset</span><span class="sxs-lookup"><span data-stu-id="ce882-381">internalSubset</span></span> <br/> <i><span data-ttu-id="ce882-382">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-382">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` <span data-ttu-id="ce882-383">InternalSubset do nó.</span><span class="sxs-lookup"><span data-stu-id="ce882-383">Node's internalSubset.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-384">xmlversão</span><span class="sxs-lookup"><span data-stu-id="ce882-384">xmlVersion</span></span> <br/> <i><span data-ttu-id="ce882-385">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-385">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Document` <span data-ttu-id="ce882-386">A versão do nó XML no caso de documentos XML.</span><span class="sxs-lookup"><span data-stu-id="ce882-386">Node's xml version in the case of XML documents.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-387">name</span><span class="sxs-lookup"><span data-stu-id="ce882-387">name</span></span> <br/> <i><span data-ttu-id="ce882-388">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-388">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` <span data-ttu-id="ce882-389">Nome do nó.</span><span class="sxs-lookup"><span data-stu-id="ce882-389">Node's name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-390">value</span><span class="sxs-lookup"><span data-stu-id="ce882-390">value</span></span> <br/> <i><span data-ttu-id="ce882-391">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-391">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` <span data-ttu-id="ce882-392">Valor do nó.</span><span class="sxs-lookup"><span data-stu-id="ce882-392">Node's value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-393">frameid</span><span class="sxs-lookup"><span data-stu-id="ce882-393">frameId</span></span> <br/> <i><span data-ttu-id="ce882-394">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-394">optional</span></span></i></td>
            <td><a href="page.md#frameid"><code class="flyout">Page.FrameId</code></a></td>
            <td><span data-ttu-id="ce882-395">ID do quadro para elementos de proprietário do quadro.</span><span class="sxs-lookup"><span data-stu-id="ce882-395">Frame ID for frame owner elements.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-396">contentDocument</span><span class="sxs-lookup"><span data-stu-id="ce882-396">contentDocument</span></span> <br/> <i><span data-ttu-id="ce882-397">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-397">optional</span></span></i></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td><span data-ttu-id="ce882-398">Documento de conteúdo para elementos de proprietário do quadro.</span><span class="sxs-lookup"><span data-stu-id="ce882-398">Content document for frame owner elements.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="ce882-399">isSVG</span><span class="sxs-lookup"><span data-stu-id="ce882-399">isSVG</span></span> <br/> <i><span data-ttu-id="ce882-400">opcional</span><span class="sxs-lookup"><span data-stu-id="ce882-400">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="ce882-401">Verdadeiro se o nó for SVG.</span><span class="sxs-lookup"><span data-stu-id="ce882-401">True if the node is SVG.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="backendnodeid"></a> <span data-ttu-id="ce882-402">BackendNodeId</span><span class="sxs-lookup"><span data-stu-id="ce882-402">BackendNodeId</span></span> `integer`

<span data-ttu-id="ce882-403">Identificador de nó DOM exclusivo usado para fazer referência a um nó que pode não ter sido enviado para o front-end.</span><span class="sxs-lookup"><span data-stu-id="ce882-403">Unique DOM node identifier used to reference a node that may not have been pushed to the front-end.</span></span>

</p>

---

### <a name="pseudotype"></a> <span data-ttu-id="ce882-404">Pseudotype</span><span class="sxs-lookup"><span data-stu-id="ce882-404">PseudoType</span></span> `string`

<span data-ttu-id="ce882-405">Pseudo-tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="ce882-405">Pseudo element type.</span></span>

##### <span data-ttu-id="ce882-406">Valores permitidos</span><span class="sxs-lookup"><span data-stu-id="ce882-406">Allowed Values</span></span>
<span data-ttu-id="ce882-407">primeira linha, primeira letra, antes, depois, seleção</span><span class="sxs-lookup"><span data-stu-id="ce882-407">first-line, first-letter, before, after, selection</span></span>
</p>

---

## <span data-ttu-id="ce882-408">Dependências</span><span class="sxs-lookup"><span data-stu-id="ce882-408">Dependencies</span></span>

[<span data-ttu-id="ce882-409">Tempo de Execução</span><span class="sxs-lookup"><span data-stu-id="ce882-409">Runtime</span></span>](runtime.md)