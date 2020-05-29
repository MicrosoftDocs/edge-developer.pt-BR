---
description: Referência para o domínio DOMDebugger. A depuração de DOM permite definir pontos de interrupção em determinadas operações e eventos do DOM. A execução do JavaScript será interrompida nessas operações como se houvesse um ponto de interrupção regular definido.
title: DOMDebugger Domain-DevTools Protocol versão 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 437a88ff93bda36d85a8f5632c1a02aa205d049b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561332"
---
# <span data-ttu-id="d9451-105">DOMDebugger</span><span class="sxs-lookup"><span data-stu-id="d9451-105">DOMDebugger</span></span>
<span data-ttu-id="d9451-106">A depuração de DOM permite definir pontos de interrupção em determinadas operações e eventos do DOM.</span><span class="sxs-lookup"><span data-stu-id="d9451-106">DOM debugging allows setting breakpoints on particular DOM operations and events.</span></span> <span data-ttu-id="d9451-107">A execução do JavaScript será interrompida nessas operações como se houvesse um ponto de interrupção regular definido.</span><span class="sxs-lookup"><span data-stu-id="d9451-107">JavaScript execution will stop on these operations as if there was a regular breakpoint set.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="d9451-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="d9451-108">Methods</span></span>**](#methods) | <span data-ttu-id="d9451-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span><span class="sxs-lookup"><span data-stu-id="d9451-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span></span> |
## <span data-ttu-id="d9451-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d9451-110">Methods</span></span>

### <span data-ttu-id="d9451-111">setInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="d9451-111">setInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="d9451-112">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="d9451-112">Experimental.</span></span> </b></span><span data-ttu-id="d9451-113">Define um ponto de interrupção em um evento nativo específico.</span><span class="sxs-lookup"><span data-stu-id="d9451-113">Sets a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9451-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9451-114">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9451-115">EventName</span><span class="sxs-lookup"><span data-stu-id="d9451-115">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9451-116">Nome da instrumentação para parar.</span><span class="sxs-lookup"><span data-stu-id="d9451-116">Instrumentation name to stop on.</span></span> <span data-ttu-id="d9451-117">Valores válidos: "scriptFirstStatement".</span><span class="sxs-lookup"><span data-stu-id="d9451-117">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="d9451-118">removeInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="d9451-118">removeInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="d9451-119">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="d9451-119">Experimental.</span></span> </b></span><span data-ttu-id="d9451-120">Remove um ponto de interrupção em um evento nativo específico.</span><span class="sxs-lookup"><span data-stu-id="d9451-120">Removes a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="d9451-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9451-121">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="d9451-122">EventName</span><span class="sxs-lookup"><span data-stu-id="d9451-122">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="d9451-123">Nome da instrumentação para parar.</span><span class="sxs-lookup"><span data-stu-id="d9451-123">Instrumentation name to stop on.</span></span> <span data-ttu-id="d9451-124">Valores válidos: "scriptFirstStatement".</span><span class="sxs-lookup"><span data-stu-id="d9451-124">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
