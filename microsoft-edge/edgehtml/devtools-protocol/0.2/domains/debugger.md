---
description: DevTools Protocol Version 0,2 (EdgeHTML) Reference para o domínio do depurador. O domínio do depurador expõe recursos de depuração JavaScript. Ele permite definir e remover pontos de interrupção, percorrer a execução, explorar rastreamentos de pilha, etc.
title: Debugger Domain-DevTools Protocol versão 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 24571b3a32acf085dd9ccbd641b1e5b06b3b9504
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231310"
---
# <span data-ttu-id="e4e06-105">Debugger Domain-DevTools Protocol versão 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="e4e06-105">Debugger Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="e4e06-106">O domínio do depurador expõe recursos de depuração JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e4e06-106">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="e4e06-107">Ele permite definir e remover pontos de interrupção, percorrer a execução, explorar rastreamentos de pilha, etc.</span><span class="sxs-lookup"><span data-stu-id="e4e06-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="e4e06-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="e4e06-108">Methods</span></span>**](#methods) | <span data-ttu-id="e4e06-109">[habilitar](#enable), [desabilitar](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [SetBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [StepOut](#stepout), [Pause](#pause), [resume](#resume), [getscriptname](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setvariablevalue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="e4e06-109">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |
| [**<span data-ttu-id="e4e06-110">Eventos</span><span class="sxs-lookup"><span data-stu-id="e4e06-110">Events</span></span>**](#events) | <span data-ttu-id="e4e06-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [pausado](#paused), [retomado](#resumed)</span><span class="sxs-lookup"><span data-stu-id="e4e06-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |
| [**<span data-ttu-id="e4e06-112">Tipos</span><span class="sxs-lookup"><span data-stu-id="e4e06-112">Types</span></span>**](#types) | <span data-ttu-id="e4e06-113">[Breakpointid](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span><span class="sxs-lookup"><span data-stu-id="e4e06-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |
| [**<span data-ttu-id="e4e06-114">Dependências</span><span class="sxs-lookup"><span data-stu-id="e4e06-114">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="e4e06-115">Tempo de Execução</span><span class="sxs-lookup"><span data-stu-id="e4e06-115">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="e4e06-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="e4e06-116">Methods</span></span>

### <span data-ttu-id="e4e06-117">Habilitar</span><span class="sxs-lookup"><span data-stu-id="e4e06-117">enable</span></span>
<span data-ttu-id="e4e06-118">Habilita o depurador para a página especificada.</span><span class="sxs-lookup"><span data-stu-id="e4e06-118">Enables debugger for the given page.</span></span> <span data-ttu-id="e4e06-119">Os clientes não devem presumir que a depuração foi habilitada até que o resultado desse comando seja recebido.</span><span class="sxs-lookup"><span data-stu-id="e4e06-119">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>

</p>

---

### <span data-ttu-id="e4e06-120">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="e4e06-120">disable</span></span>
<span data-ttu-id="e4e06-121">Desabilita o depurador para determinada página.</span><span class="sxs-lookup"><span data-stu-id="e4e06-121">Disables debugger for given page.</span></span>

</p>

---

### <span data-ttu-id="e4e06-122">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="e4e06-122">getPossibleBreakpoints</span></span>
<span data-ttu-id="e4e06-123">Retorna possíveis locais para o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="e4e06-123">Returns possible locations for breakpoint.</span></span> <span data-ttu-id="e4e06-124">os scripts em locais de intervalo de início e término devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="e4e06-124">scriptId in start and end range locations should be the same.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e06-125">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-126">start</span><span class="sxs-lookup"><span data-stu-id="e4e06-126">start</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="e4e06-127">Início do intervalo para pesquisar possíveis locais de ponto de interrupção em.</span><span class="sxs-lookup"><span data-stu-id="e4e06-127">Start of range to search possible breakpoint locations in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-128">encerrar</span><span class="sxs-lookup"><span data-stu-id="e4e06-128">end</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="e4e06-129">Fim do intervalo para pesquisar possíveis locais de ponto de interrupção (excluindo).</span><span class="sxs-lookup"><span data-stu-id="e4e06-129">End of range to search possible breakpoint locations in (excluding).</span></span> <span data-ttu-id="e4e06-130">Quando não especificado, o final dos scripts é usado como final do intervalo.</span><span class="sxs-lookup"><span data-stu-id="e4e06-130">When not specified, end of scripts is used as end of range.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-131">Devolver</span><span class="sxs-lookup"><span data-stu-id="e4e06-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-132">localiza</span><span class="sxs-lookup"><span data-stu-id="e4e06-132">locations</span></span></td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td><span data-ttu-id="e4e06-133">Lista de possíveis locais de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="e4e06-133">List of the possible breakpoint locations.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e4e06-134">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="e4e06-134">setBreakpointsActive</span></span>
<span data-ttu-id="e4e06-135">Ativa/desativa todos os pontos de interrupção na página.</span><span class="sxs-lookup"><span data-stu-id="e4e06-135">Activates / deactivates all breakpoints on the page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-136">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e06-136">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-137">active</span><span class="sxs-lookup"><span data-stu-id="e4e06-137">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="e4e06-138">Novo valor para o estado ativo dos pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="e4e06-138">New value for breakpoints active state.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e4e06-139">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="e4e06-139">setBreakpointByUrl</span></span>
<span data-ttu-id="e4e06-140">Define o ponto de interrupção JavaScript em um determinado local especificado por URL ou Regex de URL.</span><span class="sxs-lookup"><span data-stu-id="e4e06-140">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span> <span data-ttu-id="e4e06-141">Depois que esse comando for emitido, todos os scripts analisados existentes terão pontos de interrupção resolvidos e retornados na <code>locations</code> propriedade.</span><span class="sxs-lookup"><span data-stu-id="e4e06-141">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in <code>locations</code> property.</span></span> <span data-ttu-id="e4e06-142">A análise de script correspondente resultará em eventos subsequentes <code>breakpointResolved</code> emitidos.</span><span class="sxs-lookup"><span data-stu-id="e4e06-142">Further matching script parsing will result in subsequent <code>breakpointResolved</code> events issued.</span></span> <span data-ttu-id="e4e06-143">Esse ponto de interrupção lógico permanecerá recarregamentos de página.</span><span class="sxs-lookup"><span data-stu-id="e4e06-143">This logical breakpoint will survive page reloads.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-144">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e06-144">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-145">lineNumber</span><span class="sxs-lookup"><span data-stu-id="e4e06-145">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e4e06-146">Número da linha para definir o ponto de interrupção em.</span><span class="sxs-lookup"><span data-stu-id="e4e06-146">Line number to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-147">url</span><span class="sxs-lookup"><span data-stu-id="e4e06-147">url</span></span> <br/> <i><span data-ttu-id="e4e06-148">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-148">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e4e06-149">URL dos recursos para definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="e4e06-149">URL of the resources to set breakpoint on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-150">urlRegex</span><span class="sxs-lookup"><span data-stu-id="e4e06-150">urlRegex</span></span> <br/> <i><span data-ttu-id="e4e06-151">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-151">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e4e06-152">Padrão Regex para as URLs dos recursos para definir os pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="e4e06-152">Regex pattern for the URLs of the resources to set breakpoints on.</span></span> <span data-ttu-id="e4e06-153"><code>url</code>Ou <code>urlRegex</code> deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="e4e06-153">Either <code>url</code> or <code>urlRegex</code> must be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-154">columnNumber</span><span class="sxs-lookup"><span data-stu-id="e4e06-154">columnNumber</span></span> <br/> <i><span data-ttu-id="e4e06-155">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-155">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e4e06-156">Offset na linha para definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="e4e06-156">Offset in the line to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-157">problema</span><span class="sxs-lookup"><span data-stu-id="e4e06-157">condition</span></span> <br/> <i><span data-ttu-id="e4e06-158">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-158">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e4e06-159">Expressão a ser usada como uma condição de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="e4e06-159">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="e4e06-160">Quando especificado, o depurador só será interrompido no ponto de interrupção se essa expressão for avaliada como true.</span><span class="sxs-lookup"><span data-stu-id="e4e06-160">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-161">Devolver</span><span class="sxs-lookup"><span data-stu-id="e4e06-161">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-162">breakpointid</span><span class="sxs-lookup"><span data-stu-id="e4e06-162">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="e4e06-163">ID do ponto de interrupção criado para referência adicional.</span><span class="sxs-lookup"><span data-stu-id="e4e06-163">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-164">localiza</span><span class="sxs-lookup"><span data-stu-id="e4e06-164">locations</span></span></td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td><span data-ttu-id="e4e06-165">Lista de locais para os quais esse ponto de interrupção foi resolvido após adição.</span><span class="sxs-lookup"><span data-stu-id="e4e06-165">List of the locations this breakpoint resolved into upon addition.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e4e06-166">SetBreakpoint</span><span class="sxs-lookup"><span data-stu-id="e4e06-166">setBreakpoint</span></span>
<span data-ttu-id="e4e06-167">Define o ponto de interrupção JavaScript em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="e4e06-167">Sets JavaScript breakpoint at a given location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-168">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e06-168">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-169">ponto</span><span class="sxs-lookup"><span data-stu-id="e4e06-169">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="e4e06-170">Local para definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="e4e06-170">Location to set breakpoint in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-171">problema</span><span class="sxs-lookup"><span data-stu-id="e4e06-171">condition</span></span> <br/> <i><span data-ttu-id="e4e06-172">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-172">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e4e06-173">Expressão a ser usada como uma condição de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="e4e06-173">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="e4e06-174">Quando especificado, o depurador só será interrompido no ponto de interrupção se essa expressão for avaliada como true.</span><span class="sxs-lookup"><span data-stu-id="e4e06-174">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-175">Devolver</span><span class="sxs-lookup"><span data-stu-id="e4e06-175">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-176">breakpointid</span><span class="sxs-lookup"><span data-stu-id="e4e06-176">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="e4e06-177">ID do ponto de interrupção criado para referência adicional.</span><span class="sxs-lookup"><span data-stu-id="e4e06-177">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-178">actualLocation</span><span class="sxs-lookup"><span data-stu-id="e4e06-178">actualLocation</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="e4e06-179">Local em que este ponto de interrupção foi resolvido.</span><span class="sxs-lookup"><span data-stu-id="e4e06-179">Location this breakpoint resolved into.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e4e06-180">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="e4e06-180">removeBreakpoint</span></span>
<span data-ttu-id="e4e06-181">Remove o ponto de interrupção JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e4e06-181">Removes JavaScript breakpoint.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-182">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e06-182">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-183">breakpointid</span><span class="sxs-lookup"><span data-stu-id="e4e06-183">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e4e06-184">stepOver</span><span class="sxs-lookup"><span data-stu-id="e4e06-184">stepOver</span></span>
<span data-ttu-id="e4e06-185">Etapas sobre a instrução.</span><span class="sxs-lookup"><span data-stu-id="e4e06-185">Steps over the statement.</span></span>

</p>

---

### <span data-ttu-id="e4e06-186">stepInto</span><span class="sxs-lookup"><span data-stu-id="e4e06-186">stepInto</span></span>
<span data-ttu-id="e4e06-187">Etapas para a chamada de função.</span><span class="sxs-lookup"><span data-stu-id="e4e06-187">Steps into the function call.</span></span>

</p>

---

### <span data-ttu-id="e4e06-188">passo a passo</span><span class="sxs-lookup"><span data-stu-id="e4e06-188">stepOut</span></span>
<span data-ttu-id="e4e06-189">Etapas para sair da chamada de função.</span><span class="sxs-lookup"><span data-stu-id="e4e06-189">Steps out of the function call.</span></span>

</p>

---

### <span data-ttu-id="e4e06-190">pause</span><span class="sxs-lookup"><span data-stu-id="e4e06-190">pause</span></span>
<span data-ttu-id="e4e06-191">Para a próxima instrução JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e4e06-191">Stops on the next JavaScript statement.</span></span>

</p>

---

### <span data-ttu-id="e4e06-192">resume</span><span class="sxs-lookup"><span data-stu-id="e4e06-192">resume</span></span>
<span data-ttu-id="e4e06-193">Retoma a execução do JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e4e06-193">Resumes JavaScript execution.</span></span>

</p>

---

### <span data-ttu-id="e4e06-194">getscriptname</span><span class="sxs-lookup"><span data-stu-id="e4e06-194">getScriptSource</span></span>
<span data-ttu-id="e4e06-195">Retorna a origem do script com ID especificado.</span><span class="sxs-lookup"><span data-stu-id="e4e06-195">Returns source for the script with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-196">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e06-196">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-197">scriptid</span><span class="sxs-lookup"><span data-stu-id="e4e06-197">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="e4e06-198">ID do script para o qual obter a fonte.</span><span class="sxs-lookup"><span data-stu-id="e4e06-198">Id of the script to get source for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-199">Devolver</span><span class="sxs-lookup"><span data-stu-id="e4e06-199">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-200">scriptização</span><span class="sxs-lookup"><span data-stu-id="e4e06-200">scriptSource</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e4e06-201">Fonte de script.</span><span class="sxs-lookup"><span data-stu-id="e4e06-201">Script source.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e4e06-202">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="e4e06-202">setPauseOnExceptions</span></span>
<span data-ttu-id="e4e06-203">Define o estado pausar exceções.</span><span class="sxs-lookup"><span data-stu-id="e4e06-203">Defines pause on exceptions state.</span></span> <span data-ttu-id="e4e06-204">Pode ser definido para interromper todas as exceções, exceções não capturadas ou nenhuma exceção.</span><span class="sxs-lookup"><span data-stu-id="e4e06-204">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span> <span data-ttu-id="e4e06-205">O estado de pausa inicial em exceções é <code>none</code> .</span><span class="sxs-lookup"><span data-stu-id="e4e06-205">Initial pause on exceptions state is <code>none</code>.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-206">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e06-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-207">Estado</span><span class="sxs-lookup"><span data-stu-id="e4e06-207">state</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="e4e06-208">Valores permitidos: None, unpercebeud, All</span><span class="sxs-lookup"><span data-stu-id="e4e06-208">Allowed values: none, uncaught, all</span></span></i></td>
            <td><span data-ttu-id="e4e06-209">Pausar no modo de exceções.</span><span class="sxs-lookup"><span data-stu-id="e4e06-209">Pause on exceptions mode.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e4e06-210">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="e4e06-210">evaluateOnCallFrame</span></span>
<span data-ttu-id="e4e06-211">Avalia a expressão em um determinado quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="e4e06-211">Evaluates expression on a given call frame.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-212">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e06-212">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-213">callFrameId</span><span class="sxs-lookup"><span data-stu-id="e4e06-213">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="e4e06-214">Identificador de quadro de chamada para avaliação.</span><span class="sxs-lookup"><span data-stu-id="e4e06-214">Call frame identifier to evaluate on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-215">Express</span><span class="sxs-lookup"><span data-stu-id="e4e06-215">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e4e06-216">Expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="e4e06-216">Expression to evaluate.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-217">Devolver</span><span class="sxs-lookup"><span data-stu-id="e4e06-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-218">levar</span><span class="sxs-lookup"><span data-stu-id="e4e06-218">result</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="e4e06-219">Wrapper do objeto para o resultado da avaliação.</span><span class="sxs-lookup"><span data-stu-id="e4e06-219">Object wrapper for the evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e4e06-220">setvariablevalue</span><span class="sxs-lookup"><span data-stu-id="e4e06-220">setVariableValue</span></span>
<span data-ttu-id="e4e06-221">Altera o valor da variável em um callframe.</span><span class="sxs-lookup"><span data-stu-id="e4e06-221">Changes value of variable in a callframe.</span></span> <span data-ttu-id="e4e06-222">Escopos baseados em objeto não são compatíveis e devem ser modificados manualmente.</span><span class="sxs-lookup"><span data-stu-id="e4e06-222">Object-based scopes are not supported and must be mutated manually.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-223">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e06-223">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-224">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="e4e06-224">scopeNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e4e06-225">número baseado em 0 do escopo como foi listado na cadeia de escopos.</span><span class="sxs-lookup"><span data-stu-id="e4e06-225">0-based number of scope as was listed in scope chain.</span></span> <span data-ttu-id="e4e06-226">Somente os tipos de escopo ' local ', ' fechamento ' e ' Catch ' são permitidos.</span><span class="sxs-lookup"><span data-stu-id="e4e06-226">Only 'local', 'closure' and 'catch' scope types are allowed.</span></span> <span data-ttu-id="e4e06-227">Outros escopos podem ser manipulados manualmente.</span><span class="sxs-lookup"><span data-stu-id="e4e06-227">Other scopes could be manipulated manually.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-228">VariableName</span><span class="sxs-lookup"><span data-stu-id="e4e06-228">variableName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e4e06-229">Nome da variável.</span><span class="sxs-lookup"><span data-stu-id="e4e06-229">Variable name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-230">newValue</span><span class="sxs-lookup"><span data-stu-id="e4e06-230">newValue</span></span></td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td><span data-ttu-id="e4e06-231">Novo valor de variável.</span><span class="sxs-lookup"><span data-stu-id="e4e06-231">New variable value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-232">callFrameId</span><span class="sxs-lookup"><span data-stu-id="e4e06-232">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="e4e06-233">ID de callframe que mantém a variável.</span><span class="sxs-lookup"><span data-stu-id="e4e06-233">Id of callframe that holds variable.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e4e06-234">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="e4e06-234">setBlackboxPatterns</span></span>
<span><b><span data-ttu-id="e4e06-235">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="e4e06-235">Experimental.</span></span> </b></span><span data-ttu-id="e4e06-236">Substituir os padrões de Blackbox anteriores pelos aprovados.</span><span class="sxs-lookup"><span data-stu-id="e4e06-236">Replace previous blackbox patterns with passed ones.</span></span> <span data-ttu-id="e4e06-237">Força o back-end a ignorar a depuração/pausa em scripts com URL correspondente a um dos padrões.</span><span class="sxs-lookup"><span data-stu-id="e4e06-237">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span> <span data-ttu-id="e4e06-238">O depurador tentará deixar o script do blackboxed executando ' Step in ' várias vezes, finalmente reclassificando para "Step Out" se não tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="e4e06-238">The debugger will try to leave blackboxed script by performing 'step in' several times, finally resorting to 'step out' if unsuccessful.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-239">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e06-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-240">padrões</span><span class="sxs-lookup"><span data-stu-id="e4e06-240">patterns</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="e4e06-241">Matriz de regexps que será usada para verificar a URL do script para o estado Blackbox.</span><span class="sxs-lookup"><span data-stu-id="e4e06-241">Array of regexps that will be used to check script url for blackbox state.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e4e06-242">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="e4e06-242">msSetDebuggerPropertyValue</span></span>
<span><b><span data-ttu-id="e4e06-243">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="e4e06-243">Experimental.</span></span> </b></span><span data-ttu-id="e4e06-244">Microsoft: define a Propriedade Debugger especificada para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="e4e06-244">Microsoft: Sets the specified debugger property to the specified value.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-245">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e06-245">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-246">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="e4e06-246">debuggerPropertyId</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e4e06-247">Microsoft: a identificação da propriedade (por exemplo, msDebuggerPropertyId) a ser definida.</span><span class="sxs-lookup"><span data-stu-id="e4e06-247">Microsoft: The property id (i.e. msDebuggerPropertyId) to set.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-248">newValue</span><span class="sxs-lookup"><span data-stu-id="e4e06-248">newValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="e4e06-249">Eventos</span><span class="sxs-lookup"><span data-stu-id="e4e06-249">Events</span></span>

### <span data-ttu-id="e4e06-250">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="e4e06-250">scriptParsed</span></span>
<span data-ttu-id="e4e06-251">Acionado quando o script é analisado.</span><span class="sxs-lookup"><span data-stu-id="e4e06-251">Fired when the script is parsed.</span></span> <span data-ttu-id="e4e06-252">Esse evento também é disparado para todos os scripts conhecidos e não coletados, quando o depurador é ativado.</span><span class="sxs-lookup"><span data-stu-id="e4e06-252">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-253">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e06-253">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-254">scriptid</span><span class="sxs-lookup"><span data-stu-id="e4e06-254">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="e4e06-255">Identificador do script analisado.</span><span class="sxs-lookup"><span data-stu-id="e4e06-255">Identifier of the script parsed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-256">url</span><span class="sxs-lookup"><span data-stu-id="e4e06-256">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e4e06-257">URL ou nome do script analisado (se houver).</span><span class="sxs-lookup"><span data-stu-id="e4e06-257">URL or name of the script parsed (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-258">início</span><span class="sxs-lookup"><span data-stu-id="e4e06-258">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e4e06-259">Deslocamento de linha do script dentro do recurso com a URL fornecida (para marcas de script).</span><span class="sxs-lookup"><span data-stu-id="e4e06-259">Line offset of the script within the resource with given URL (for script tags).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-260">startColumn</span><span class="sxs-lookup"><span data-stu-id="e4e06-260">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e4e06-261">O deslocamento da coluna do script dentro do recurso com a URL fornecida.</span><span class="sxs-lookup"><span data-stu-id="e4e06-261">Column offset of the script within the resource with given URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-262">Line</span><span class="sxs-lookup"><span data-stu-id="e4e06-262">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e4e06-263">Última linha do script.</span><span class="sxs-lookup"><span data-stu-id="e4e06-263">Last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-264">Coluna de EndColumn</span><span class="sxs-lookup"><span data-stu-id="e4e06-264">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e4e06-265">Comprimento da última linha do script.</span><span class="sxs-lookup"><span data-stu-id="e4e06-265">Length of the last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-266">executionContextid</span><span class="sxs-lookup"><span data-stu-id="e4e06-266">executionContextId</span></span></td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td><span data-ttu-id="e4e06-267">Especifica o contexto de criação de script.</span><span class="sxs-lookup"><span data-stu-id="e4e06-267">Specifies script creation context.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-268">sourceMapURL</span><span class="sxs-lookup"><span data-stu-id="e4e06-268">sourceMapURL</span></span> <br/> <i><span data-ttu-id="e4e06-269">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-269">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e4e06-270">URL do mapa de origem associado ao script (se houver).</span><span class="sxs-lookup"><span data-stu-id="e4e06-270">URL of source map associated with script (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-271">das</span><span class="sxs-lookup"><span data-stu-id="e4e06-271">length</span></span> <br/> <i><span data-ttu-id="e4e06-272">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-272">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="e4e06-273">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="e4e06-273">Experimental.</span></span> </b></span><span data-ttu-id="e4e06-274">Esse tamanho do script.</span><span class="sxs-lookup"><span data-stu-id="e4e06-274">This script length.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-275">msParentId</span><span class="sxs-lookup"><span data-stu-id="e4e06-275">msParentId</span></span> <br/> <i><span data-ttu-id="e4e06-276">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-276">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="e4e06-277">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="e4e06-277">Experimental.</span></span> </b></span><span data-ttu-id="e4e06-278">Esta é a ID do documento pai.</span><span class="sxs-lookup"><span data-stu-id="e4e06-278">This is the parent document ID.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-279">msMimeType</span><span class="sxs-lookup"><span data-stu-id="e4e06-279">msMimeType</span></span> <br/> <i><span data-ttu-id="e4e06-280">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-280">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="e4e06-281">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="e4e06-281">Experimental.</span></span> </b></span><span data-ttu-id="e4e06-282">Esse é o tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="e4e06-282">This is the mime type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-283">msIsDynamicCode</span><span class="sxs-lookup"><span data-stu-id="e4e06-283">msIsDynamicCode</span></span> <br/> <i><span data-ttu-id="e4e06-284">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-284">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="e4e06-285">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="e4e06-285">Experimental.</span></span> </b></span><span data-ttu-id="e4e06-286">Isso indica se é um código dinâmico.</span><span class="sxs-lookup"><span data-stu-id="e4e06-286">This indicates whether it is dynamic code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-287">msLongDocumentId</span><span class="sxs-lookup"><span data-stu-id="e4e06-287">msLongDocumentId</span></span> <br/> <i><span data-ttu-id="e4e06-288">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-288">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="e4e06-289">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="e4e06-289">Experimental.</span></span> </b></span><span data-ttu-id="e4e06-290">Esta é a ID do documento longo.</span><span class="sxs-lookup"><span data-stu-id="e4e06-290">This is the long document ID.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e4e06-291">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="e4e06-291">breakpointResolved</span></span>
<span data-ttu-id="e4e06-292">Disparado quando o ponto de interrupção é resolvido para um script e local reais.</span><span class="sxs-lookup"><span data-stu-id="e4e06-292">Fired when breakpoint is resolved to an actual script and location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-293">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e06-293">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-294">breakpointid</span><span class="sxs-lookup"><span data-stu-id="e4e06-294">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="e4e06-295">Identificador exclusivo de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="e4e06-295">Breakpoint unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-296">ponto</span><span class="sxs-lookup"><span data-stu-id="e4e06-296">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="e4e06-297">Local do ponto de interrupção real.</span><span class="sxs-lookup"><span data-stu-id="e4e06-297">Actual breakpoint location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-298">msLength</span><span class="sxs-lookup"><span data-stu-id="e4e06-298">msLength</span></span> <br/> <i><span data-ttu-id="e4e06-299">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-299">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="e4e06-300">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="e4e06-300">Experimental.</span></span> </b></span><span data-ttu-id="e4e06-301">Microsoft: comprimento do código (ou seja, número de caracteres) no local do ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="e4e06-301">Microsoft: Length of code (i.e. number of characters) at the breakpoint location.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e4e06-302">pausado</span><span class="sxs-lookup"><span data-stu-id="e4e06-302">paused</span></span>
<span data-ttu-id="e4e06-303">Acionado quando os depuradores violam um ponto de interrupção ou uma exceção.</span><span class="sxs-lookup"><span data-stu-id="e4e06-303">Fired when the debuggers breaks for a breakpoint or exception.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-304">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e06-304">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-305">callFrames</span><span class="sxs-lookup"><span data-stu-id="e4e06-305">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="e4e06-306">Pilha de chamadas no depurador interrompido.</span><span class="sxs-lookup"><span data-stu-id="e4e06-306">Call stack the debugger stopped on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-307">motivo</span><span class="sxs-lookup"><span data-stu-id="e4e06-307">reason</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="e4e06-308">Valores permitidos: Breakpoint, Step, Exception, Other, EventListener</span><span class="sxs-lookup"><span data-stu-id="e4e06-308">Allowed values: breakpoint, step, exception, other, EventListener</span></span></i></td>
            <td><span data-ttu-id="e4e06-309">Motivo da pausa.</span><span class="sxs-lookup"><span data-stu-id="e4e06-309">Pause reason.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-310">data</span><span class="sxs-lookup"><span data-stu-id="e4e06-310">data</span></span> <br/> <i><span data-ttu-id="e4e06-311">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-311">optional</span></span></i></td>
            <td><code class="flyout">object</code></td>
            <td><span data-ttu-id="e4e06-312">Objeto que contém propriedades auxiliares de quebra específicas.</span><span class="sxs-lookup"><span data-stu-id="e4e06-312">Object containing break-specific auxiliary properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-313">hitBreakpoints</span><span class="sxs-lookup"><span data-stu-id="e4e06-313">hitBreakpoints</span></span> <br/> <i><span data-ttu-id="e4e06-314">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-314">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="e4e06-315">IDs de pontos de interrupção de acesso</span><span class="sxs-lookup"><span data-stu-id="e4e06-315">Hit breakpoints IDs</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-316">asyncStackTrace</span><span class="sxs-lookup"><span data-stu-id="e4e06-316">asyncStackTrace</span></span> <br/> <i><span data-ttu-id="e4e06-317">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-317">optional</span></span></i></td>
            <td><!--  <a href="#stacktrace">  --><code class="flyout">StackTrace</code><!--  </a>  --></td>
            <td><span data-ttu-id="e4e06-318">Rastreamento de pilha assíncrono JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e4e06-318">JavaScript async stack trace.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="e4e06-319">retomado</span><span class="sxs-lookup"><span data-stu-id="e4e06-319">resumed</span></span>
<span data-ttu-id="e4e06-320">Acionado quando o depurador retomar a execução.</span><span class="sxs-lookup"><span data-stu-id="e4e06-320">Fired when the debugger resumes execution.</span></span>

</p>

---

## <span data-ttu-id="e4e06-321">Tipos</span><span class="sxs-lookup"><span data-stu-id="e4e06-321">Types</span></span>

### <a name="breakpointid"></a> <span data-ttu-id="e4e06-322">Breakpointid</span><span class="sxs-lookup"><span data-stu-id="e4e06-322">BreakpointId</span></span> `string`

<span data-ttu-id="e4e06-323">Identificador de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="e4e06-323">Breakpoint identifier.</span></span>

</p>

---

### <a name="callframeid"></a> <span data-ttu-id="e4e06-324">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="e4e06-324">CallFrameId</span></span> `string`

<span data-ttu-id="e4e06-325">Identificador de quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="e4e06-325">Call frame identifier.</span></span>

</p>

---

### <a name="location"></a> <span data-ttu-id="e4e06-326">Localização</span><span class="sxs-lookup"><span data-stu-id="e4e06-326">Location</span></span> `object`

<span data-ttu-id="e4e06-327">Local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="e4e06-327">Location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-328">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e4e06-328">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-329">scriptid</span><span class="sxs-lookup"><span data-stu-id="e4e06-329">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="e4e06-330">Identificador de script reportado no <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="e4e06-330">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-331">lineNumber</span><span class="sxs-lookup"><span data-stu-id="e4e06-331">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e4e06-332">Número da linha no script (baseado em 0).</span><span class="sxs-lookup"><span data-stu-id="e4e06-332">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-333">columnNumber</span><span class="sxs-lookup"><span data-stu-id="e4e06-333">columnNumber</span></span> <br/> <i><span data-ttu-id="e4e06-334">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-334">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e4e06-335">Número da coluna no script (baseado em 0).</span><span class="sxs-lookup"><span data-stu-id="e4e06-335">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-336">msLength</span><span class="sxs-lookup"><span data-stu-id="e4e06-336">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e4e06-337">Microsoft: comprimento do código (ou seja, número de caracteres) nesse quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="e4e06-337">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="breaklocation"></a> <span data-ttu-id="e4e06-338">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="e4e06-338">BreakLocation</span></span> `object`

<span data-ttu-id="e4e06-339">Interrompa o local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="e4e06-339">Break location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-340">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e4e06-340">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-341">scriptid</span><span class="sxs-lookup"><span data-stu-id="e4e06-341">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="e4e06-342">Identificador de script reportado no <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="e4e06-342">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-343">lineNumber</span><span class="sxs-lookup"><span data-stu-id="e4e06-343">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e4e06-344">Número da linha no script (baseado em 0).</span><span class="sxs-lookup"><span data-stu-id="e4e06-344">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-345">columnNumber</span><span class="sxs-lookup"><span data-stu-id="e4e06-345">columnNumber</span></span> <br/> <i><span data-ttu-id="e4e06-346">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-346">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e4e06-347">Número da coluna no script (baseado em 0).</span><span class="sxs-lookup"><span data-stu-id="e4e06-347">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-348">msLength</span><span class="sxs-lookup"><span data-stu-id="e4e06-348">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="e4e06-349">Microsoft: comprimento do código (ou seja, número de caracteres) nesse quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="e4e06-349">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-350">tipo</span><span class="sxs-lookup"><span data-stu-id="e4e06-350">type</span></span> <br/> <i><span data-ttu-id="e4e06-351">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-351">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e4e06-352">Valores permitidos: debuggerStatement, Call, Return.</span><span class="sxs-lookup"><span data-stu-id="e4e06-352">Allowed values: debuggerStatement, call, return.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callframe"></a> <span data-ttu-id="e4e06-353">CallFrame</span><span class="sxs-lookup"><span data-stu-id="e4e06-353">CallFrame</span></span> `object`

<span data-ttu-id="e4e06-354">Quadro de chamada JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e4e06-354">JavaScript call frame.</span></span> <span data-ttu-id="e4e06-355">Matriz de quadros de chamadas formam a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="e4e06-355">Array of call frames form the call stack.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-356">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e4e06-356">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-357">callFrameId</span><span class="sxs-lookup"><span data-stu-id="e4e06-357">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="e4e06-358">Identificador de quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="e4e06-358">Call frame identifier.</span></span> <span data-ttu-id="e4e06-359">Esse identificador só é válido enquanto o depurador está pausado.</span><span class="sxs-lookup"><span data-stu-id="e4e06-359">This identifier is only valid while the debugger is paused.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-360">função FunctionName</span><span class="sxs-lookup"><span data-stu-id="e4e06-360">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e4e06-361">Nome da função JavaScript chamada neste quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="e4e06-361">Name of the JavaScript function called on this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-362">functionLocation</span><span class="sxs-lookup"><span data-stu-id="e4e06-362">functionLocation</span></span> <br/> <i><span data-ttu-id="e4e06-363">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-363">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b><span data-ttu-id="e4e06-364">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="e4e06-364">Experimental.</span></span> </b></span><span data-ttu-id="e4e06-365">Local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="e4e06-365">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-366">ponto</span><span class="sxs-lookup"><span data-stu-id="e4e06-366">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="e4e06-367">Local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="e4e06-367">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-368">url</span><span class="sxs-lookup"><span data-stu-id="e4e06-368">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e4e06-369">Nome ou URL do script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e4e06-369">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-370">scopeChain</span><span class="sxs-lookup"><span data-stu-id="e4e06-370">scopeChain</span></span></td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td><span data-ttu-id="e4e06-371">Cadeia de escopos para este quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="e4e06-371">Scope chain for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-372">deste</span><span class="sxs-lookup"><span data-stu-id="e4e06-372">this</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> <span data-ttu-id="e4e06-373">objeto para este quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="e4e06-373">object for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-374">returnValue</span><span class="sxs-lookup"><span data-stu-id="e4e06-374">returnValue</span></span> <br/> <i><span data-ttu-id="e4e06-375">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-375">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="e4e06-376">O valor que está sendo retornado, se a função estiver em um ponto de retorno.</span><span class="sxs-lookup"><span data-stu-id="e4e06-376">The value being returned, if the function is at return point.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="scope"></a> <span data-ttu-id="e4e06-377">Escopo</span><span class="sxs-lookup"><span data-stu-id="e4e06-377">Scope</span></span> `object`

<span data-ttu-id="e4e06-378">Descrição do escopo.</span><span class="sxs-lookup"><span data-stu-id="e4e06-378">Scope description.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e4e06-379">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e4e06-379">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e4e06-380">tipo</span><span class="sxs-lookup"><span data-stu-id="e4e06-380">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="e4e06-381">Valores permitidos: global, local, com, fechamento, catch, Block, script, eval, Module, Return</span><span class="sxs-lookup"><span data-stu-id="e4e06-381">Allowed values: global, local, with, closure, catch, block, script, eval, module, return</span></span></i></td>
            <td><span data-ttu-id="e4e06-382">Tipo de escopo.</span><span class="sxs-lookup"><span data-stu-id="e4e06-382">Scope type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-383">object</span><span class="sxs-lookup"><span data-stu-id="e4e06-383">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="e4e06-384">Objeto que representa o escopo.</span><span class="sxs-lookup"><span data-stu-id="e4e06-384">Object representing the scope.</span></span> <span data-ttu-id="e4e06-385">Para <code>global</code> e <code>with</code> escopos, ele representa o objeto real; para o restante dos escopos, é um objeto transitório artificial enumerando variáveis de escopo como suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e4e06-385">For <code>global</code> and <code>with</code> scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-386">name</span><span class="sxs-lookup"><span data-stu-id="e4e06-386">name</span></span> <br/> <i><span data-ttu-id="e4e06-387">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-387">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-388">startLocation</span><span class="sxs-lookup"><span data-stu-id="e4e06-388">startLocation</span></span> <br/> <i><span data-ttu-id="e4e06-389">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-389">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="e4e06-390">Local no código-fonte onde o escopo é iniciado</span><span class="sxs-lookup"><span data-stu-id="e4e06-390">Location in the source code where scope starts</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e4e06-391">EndLocation</span><span class="sxs-lookup"><span data-stu-id="e4e06-391">endLocation</span></span> <br/> <i><span data-ttu-id="e4e06-392">opcional</span><span class="sxs-lookup"><span data-stu-id="e4e06-392">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="e4e06-393">Local no código-fonte em que termina o escopo</span><span class="sxs-lookup"><span data-stu-id="e4e06-393">Location in the source code where scope ends</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="e4e06-394">Dependências</span><span class="sxs-lookup"><span data-stu-id="e4e06-394">Dependencies</span></span>

[<span data-ttu-id="e4e06-395">Tempo de Execução</span><span class="sxs-lookup"><span data-stu-id="e4e06-395">Runtime</span></span>](runtime.md)
