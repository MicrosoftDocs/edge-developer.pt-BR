---
description: Referência para o domínio DOMDebugger. A depuração de DOM permite definir pontos de interrupção em determinadas operações e eventos do DOM. A execução do JavaScript será interrompida nessas operações como se houvesse um ponto de interrupção regular definido.
title: DOMDebugger Domain-DevTools Protocol versão 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d97a9a8f2d0e49166f5f081e8bb0c0d5d3cdd93f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231308"
---
# <span data-ttu-id="9eb10-105">DOMDebugger</span><span class="sxs-lookup"><span data-stu-id="9eb10-105">DOMDebugger</span></span>

<span data-ttu-id="9eb10-106">A depuração de DOM permite definir pontos de interrupção em determinadas operações e eventos do DOM.</span><span class="sxs-lookup"><span data-stu-id="9eb10-106">DOM debugging allows setting breakpoints on particular DOM operations and events.</span></span> <span data-ttu-id="9eb10-107">A execução do JavaScript será interrompida nessas operações como se houvesse um ponto de interrupção regular definido.</span><span class="sxs-lookup"><span data-stu-id="9eb10-107">JavaScript execution will stop on these operations as if there was a regular breakpoint set.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="9eb10-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="9eb10-108">Methods</span></span>**](#methods) | <span data-ttu-id="9eb10-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span><span class="sxs-lookup"><span data-stu-id="9eb10-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span></span> |
## <span data-ttu-id="9eb10-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9eb10-110">Methods</span></span>

### <span data-ttu-id="9eb10-111">setInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="9eb10-111">setInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="9eb10-112">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="9eb10-112">Experimental.</span></span> </b></span><span data-ttu-id="9eb10-113">Define um ponto de interrupção em um evento nativo específico.</span><span class="sxs-lookup"><span data-stu-id="9eb10-113">Sets a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="9eb10-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9eb10-114">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="9eb10-115">EventName</span><span class="sxs-lookup"><span data-stu-id="9eb10-115">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="9eb10-116">Nome da instrumentação para parar.</span><span class="sxs-lookup"><span data-stu-id="9eb10-116">Instrumentation name to stop on.</span></span> <span data-ttu-id="9eb10-117">Valores válidos: "scriptFirstStatement".</span><span class="sxs-lookup"><span data-stu-id="9eb10-117">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="9eb10-118">removeInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="9eb10-118">removeInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="9eb10-119">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="9eb10-119">Experimental.</span></span> </b></span><span data-ttu-id="9eb10-120">Remove um ponto de interrupção em um evento nativo específico.</span><span class="sxs-lookup"><span data-stu-id="9eb10-120">Removes a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="9eb10-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9eb10-121">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="9eb10-122">EventName</span><span class="sxs-lookup"><span data-stu-id="9eb10-122">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="9eb10-123">Nome da instrumentação para parar.</span><span class="sxs-lookup"><span data-stu-id="9eb10-123">Instrumentation name to stop on.</span></span> <span data-ttu-id="9eb10-124">Valores válidos: "scriptFirstStatement".</span><span class="sxs-lookup"><span data-stu-id="9eb10-124">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
