---
description: Referência para o domínio de sobreposição. Domínio sobreposto expõe a interação visual adorners e seleção de nós
title: Sobreposição de protocolo de domínio-DevTools versão 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: dcf5feff9983aa2e9e61ac0569938988812165f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231306"
---
# <span data-ttu-id="da315-104">Sobreposição</span><span class="sxs-lookup"><span data-stu-id="da315-104">Overlay</span></span>

<span data-ttu-id="da315-105">Domínio sobreposto expõe a interação visual adorners e seleção de nós</span><span class="sxs-lookup"><span data-stu-id="da315-105">Overlay domain exposes visual adornments and node selection interaction</span></span>

| | |
|-|-|
| [**<span data-ttu-id="da315-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="da315-106">Methods</span></span>**](#methods) | <span data-ttu-id="da315-107">[habilitar](#enable), [desabilitar](#disable)e [setinspecionámode](#setinspectmode)</span><span class="sxs-lookup"><span data-stu-id="da315-107">[enable](#enable), [disable](#disable), [setInspectMode](#setinspectmode)</span></span> |
| [**<span data-ttu-id="da315-108">Eventos</span><span class="sxs-lookup"><span data-stu-id="da315-108">Events</span></span>**](#events) | <span data-ttu-id="da315-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span><span class="sxs-lookup"><span data-stu-id="da315-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span></span> |
| [**<span data-ttu-id="da315-110">Dependências</span><span class="sxs-lookup"><span data-stu-id="da315-110">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="da315-111">DOM</span><span class="sxs-lookup"><span data-stu-id="da315-111">DOM</span></span>](dom.md) |
## <span data-ttu-id="da315-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="da315-112">Methods</span></span>

### <span data-ttu-id="da315-113">Habilitar</span><span class="sxs-lookup"><span data-stu-id="da315-113">enable</span></span>
<span data-ttu-id="da315-114">Permite a emissão de relatórios <code>nodeHighlightRequested</code> e <code>inspectElementRequested</code> eventos</span><span class="sxs-lookup"><span data-stu-id="da315-114">Enables reporting of <code>nodeHighlightRequested</code> and <code>inspectElementRequested</code> events</span></span>

</p>

---

### <span data-ttu-id="da315-115">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="da315-115">disable</span></span>
<span data-ttu-id="da315-116">Desabilita o relatório de eventos de domínio sobrepostos</span><span class="sxs-lookup"><span data-stu-id="da315-116">Disables reporting of Overlay domain events</span></span>

</p>

---

### <span data-ttu-id="da315-117">setinspecionámode</span><span class="sxs-lookup"><span data-stu-id="da315-117">setInspectMode</span></span>
<span data-ttu-id="da315-118">Define o modo de seleção de elementos do cliente</span><span class="sxs-lookup"><span data-stu-id="da315-118">Sets the element selection mode for the client</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="da315-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da315-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="da315-120">modo</span><span class="sxs-lookup"><span data-stu-id="da315-120">mode</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="da315-121">O modo de inspeção.</span><span class="sxs-lookup"><span data-stu-id="da315-121">The inspection mode.</span></span>  <span data-ttu-id="da315-122">Os valores válidos são ' searchForNode ' e ' nenhum '.</span><span class="sxs-lookup"><span data-stu-id="da315-122">Valid values are 'searchForNode' and 'none'.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="da315-123">highlightConfig</span><span class="sxs-lookup"><span data-stu-id="da315-123">highlightConfig</span></span> <br/> <i><span data-ttu-id="da315-124">opcional</span><span class="sxs-lookup"><span data-stu-id="da315-124">optional</span></span></i></td>
            <td><a href="dom.md#highlightconfig"><code class="flyout">DOM.HighlightConfig</code></a></td>
            <td><span data-ttu-id="da315-125">A configuração de destaque a ser usada ao inspecionar</span><span class="sxs-lookup"><span data-stu-id="da315-125">The highlight configuration to use while inspecting</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="da315-126">Eventos</span><span class="sxs-lookup"><span data-stu-id="da315-126">Events</span></span>

### <span data-ttu-id="da315-127">inspectNodeRequested</span><span class="sxs-lookup"><span data-stu-id="da315-127">inspectNodeRequested</span></span>
<span data-ttu-id="da315-128">Notifica o cliente que o usuário pediu para inspecionar um nó específico</span><span class="sxs-lookup"><span data-stu-id="da315-128">Notifies the client that the user has asked to inspect a particular node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="da315-129">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da315-129">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="da315-130">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="da315-130">backendNodeId</span></span></td>
            <td><a href="dom.md#backendnodeid"><code class="flyout">DOM.BackendNodeId</code></a></td>
            <td><span data-ttu-id="da315-131">A ID do nó back-end do nó solicitado</span><span class="sxs-lookup"><span data-stu-id="da315-131">The backend node ID of node requested</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="da315-132">nodeHighlightRequested</span><span class="sxs-lookup"><span data-stu-id="da315-132">nodeHighlightRequested</span></span>
<span data-ttu-id="da315-133">Indica que o usuário passou o mouse sobre o nó e pode inspecionar o nó</span><span class="sxs-lookup"><span data-stu-id="da315-133">Indicates that the user has hovered over the node and may inspect the node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="da315-134">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da315-134">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="da315-135">NodeId</span><span class="sxs-lookup"><span data-stu-id="da315-135">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td><span data-ttu-id="da315-136">A ID do nó que está sendo considerado</span><span class="sxs-lookup"><span data-stu-id="da315-136">The node ID of the node being considered</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="da315-137">Dependências</span><span class="sxs-lookup"><span data-stu-id="da315-137">Dependencies</span></span>

[<span data-ttu-id="da315-138">DOM</span><span class="sxs-lookup"><span data-stu-id="da315-138">DOM</span></span>](dom.md)
