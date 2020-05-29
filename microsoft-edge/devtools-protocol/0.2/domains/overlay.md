---
description: Referência para o domínio de sobreposição. Domínio sobreposto expõe a interação visual adorners e seleção de nós
title: Sobreposição de protocolo de domínio-DevTools versão 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: a7657e2abc99e45894f19f6557f12f78f8ee9c75
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561331"
---
# <span data-ttu-id="d5c6b-104">Sobreposição</span><span class="sxs-lookup"><span data-stu-id="d5c6b-104">Overlay</span></span>
<span data-ttu-id="d5c6b-105">Domínio sobreposto expõe a interação visual adorners e seleção de nós</span><span class="sxs-lookup"><span data-stu-id="d5c6b-105">Overlay domain exposes visual adornments and node selection interaction</span></span>

| | |
|-|-|
| [**<span data-ttu-id="d5c6b-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="d5c6b-106">Methods</span></span>**](#methods) | <span data-ttu-id="d5c6b-107">[habilitar](#enable), [desabilitar](#disable)e [setinspecionámode](#setinspectmode)</span><span class="sxs-lookup"><span data-stu-id="d5c6b-107">[enable](#enable), [disable](#disable), [setInspectMode](#setinspectmode)</span></span> |
| [**<span data-ttu-id="d5c6b-108">Eventos</span><span class="sxs-lookup"><span data-stu-id="d5c6b-108">Events</span></span>**](#events) | <span data-ttu-id="d5c6b-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span><span class="sxs-lookup"><span data-stu-id="d5c6b-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span></span> |
| [**<span data-ttu-id="d5c6b-110">Dependências</span><span class="sxs-lookup"><span data-stu-id="d5c6b-110">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="d5c6b-111">DOM</span><span class="sxs-lookup"><span data-stu-id="d5c6b-111">DOM</span></span>](dom.md) |
## <span data-ttu-id="d5c6b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d5c6b-112">Methods</span></span>

### <span data-ttu-id="d5c6b-113">Habilitar</span><span class="sxs-lookup"><span data-stu-id="d5c6b-113">enable</span></span>
<span data-ttu-id="d5c6b-114">Permite a emissão de relatórios <code>nodeHighlightRequested</code> e <code>inspectElementRequested</code> eventos</span><span class="sxs-lookup"><span data-stu-id="d5c6b-114">Enables reporting of <code>nodeHighlightRequested</code> and <code>inspectElementRequested</code> events</span></span>

</p>

---

### <span data-ttu-id="d5c6b-115">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="d5c6b-115">disable</span></span>
<span data-ttu-id="d5c6b-116">Desabilita o relatório de eventos de domínio sobrepostos</span><span class="sxs-lookup"><span data-stu-id="d5c6b-116">Disables reporting of Overlay domain events</span></span>

</p>

---

### <span data-ttu-id="d5c6b-117">setinspecionámode</span><span class="sxs-lookup"><span data-stu-id="d5c6b-117">setInspectMode</span></span>
<span data-ttu-id="d5c6b-118">Define o modo de seleção de elementos do cliente</span><span class="sxs-lookup"><span data-stu-id="d5c6b-118">Sets the element selection mode for the client</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d5c6b-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5c6b-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d5c6b-120">modo</span><span class="sxs-lookup"><span data-stu-id="d5c6b-120">mode</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d5c6b-121">O modo de inspeção.</span><span class="sxs-lookup"><span data-stu-id="d5c6b-121">The inspection mode.</span></span>  <span data-ttu-id="d5c6b-122">Os valores válidos são ' searchForNode ' e ' nenhum '.</span><span class="sxs-lookup"><span data-stu-id="d5c6b-122">Valid values are 'searchForNode' and 'none'.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="d5c6b-123">highlightConfig</span><span class="sxs-lookup"><span data-stu-id="d5c6b-123">highlightConfig</span></span> <br/> <i><span data-ttu-id="d5c6b-124">opcional</span><span class="sxs-lookup"><span data-stu-id="d5c6b-124">optional</span></span></i></td>
            <td><a href="dom.md#highlightconfig"><code class="flyout">DOM.HighlightConfig</code></a></td>
            <td><span data-ttu-id="d5c6b-125">A configuração de destaque a ser usada ao inspecionar</span><span class="sxs-lookup"><span data-stu-id="d5c6b-125">The highlight configuration to use while inspecting</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="d5c6b-126">Eventos</span><span class="sxs-lookup"><span data-stu-id="d5c6b-126">Events</span></span>

### <span data-ttu-id="d5c6b-127">inspectNodeRequested</span><span class="sxs-lookup"><span data-stu-id="d5c6b-127">inspectNodeRequested</span></span>
<span data-ttu-id="d5c6b-128">Notifica o cliente que o usuário pediu para inspecionar um nó específico</span><span class="sxs-lookup"><span data-stu-id="d5c6b-128">Notifies the client that the user has asked to inspect a particular node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d5c6b-129">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5c6b-129">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d5c6b-130">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="d5c6b-130">backendNodeId</span></span></td>
            <td><a href="dom.md#backendnodeid"><code class="flyout">DOM.BackendNodeId</code></a></td>
            <td><span data-ttu-id="d5c6b-131">A ID do nó back-end do nó solicitado</span><span class="sxs-lookup"><span data-stu-id="d5c6b-131">The backend node ID of node requested</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d5c6b-132">nodeHighlightRequested</span><span class="sxs-lookup"><span data-stu-id="d5c6b-132">nodeHighlightRequested</span></span>
<span data-ttu-id="d5c6b-133">Indica que o usuário passou o mouse sobre o nó e pode inspecionar o nó</span><span class="sxs-lookup"><span data-stu-id="d5c6b-133">Indicates that the user has hovered over the node and may inspect the node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d5c6b-134">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5c6b-134">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d5c6b-135">NodeId</span><span class="sxs-lookup"><span data-stu-id="d5c6b-135">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td><span data-ttu-id="d5c6b-136">A ID do nó que está sendo considerado</span><span class="sxs-lookup"><span data-stu-id="d5c6b-136">The node ID of the node being considered</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="d5c6b-137">Dependências</span><span class="sxs-lookup"><span data-stu-id="d5c6b-137">Dependencies</span></span>

[<span data-ttu-id="d5c6b-138">DOM</span><span class="sxs-lookup"><span data-stu-id="d5c6b-138">DOM</span></span>](dom.md)