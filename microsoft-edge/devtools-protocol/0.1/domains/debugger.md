---
description: Referência para o domínio do depurador. O domínio do depurador expõe recursos de depuração JavaScript. Ele permite definir e remover pontos de interrupção, percorrer a execução, explorar rastreamentos de pilha, etc.
title: Domínio do depurador – versão do protocolo DevTools versão 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 6c5d668f943a731e5ba86ed5aa2294007a432ce6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561360"
---
# <span data-ttu-id="11e89-105">Depurador</span><span class="sxs-lookup"><span data-stu-id="11e89-105">Debugger</span></span>
<span data-ttu-id="11e89-106">O domínio do depurador expõe recursos de depuração JavaScript.</span><span class="sxs-lookup"><span data-stu-id="11e89-106">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="11e89-107">Ele permite definir e remover pontos de interrupção, percorrer a execução, explorar rastreamentos de pilha, etc.</span><span class="sxs-lookup"><span data-stu-id="11e89-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="11e89-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="11e89-108">Methods</span></span>**](#methods) | <span data-ttu-id="11e89-109">[habilitar](#enable), [desabilitar](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [SetBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [StepOut](#stepout), [Pause](#pause), [resume](#resume), [getscriptname](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setvariablevalue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="11e89-109">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |
| [**<span data-ttu-id="11e89-110">Eventos</span><span class="sxs-lookup"><span data-stu-id="11e89-110">Events</span></span>**](#events) | <span data-ttu-id="11e89-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [pausado](#paused), [retomado](#resumed)</span><span class="sxs-lookup"><span data-stu-id="11e89-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |
| [**<span data-ttu-id="11e89-112">Tipos</span><span class="sxs-lookup"><span data-stu-id="11e89-112">Types</span></span>**](#types) | <span data-ttu-id="11e89-113">[Breakpointid](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span><span class="sxs-lookup"><span data-stu-id="11e89-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |
| [**<span data-ttu-id="11e89-114">Dependências</span><span class="sxs-lookup"><span data-stu-id="11e89-114">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="11e89-115">Classpath</span><span class="sxs-lookup"><span data-stu-id="11e89-115">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="11e89-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="11e89-116">Methods</span></span>

### <span data-ttu-id="11e89-117">Habilitar</span><span class="sxs-lookup"><span data-stu-id="11e89-117">enable</span></span>
<span data-ttu-id="11e89-118">Habilita o depurador para a página especificada.</span><span class="sxs-lookup"><span data-stu-id="11e89-118">Enables debugger for the given page.</span></span> <span data-ttu-id="11e89-119">Os clientes não devem presumir que a depuração foi habilitada até que o resultado desse comando seja recebido.</span><span class="sxs-lookup"><span data-stu-id="11e89-119">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>


---

### <span data-ttu-id="11e89-120">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="11e89-120">disable</span></span>
<span data-ttu-id="11e89-121">Desabilita o depurador para determinada página.</span><span class="sxs-lookup"><span data-stu-id="11e89-121">Disables debugger for given page.</span></span>


---

### <span data-ttu-id="11e89-122">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="11e89-122">getPossibleBreakpoints</span></span>
<span data-ttu-id="11e89-123">Retorna possíveis locais para o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="11e89-123">Returns possible locations for breakpoint.</span></span> <span data-ttu-id="11e89-124">os scripts em locais de intervalo de início e término devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="11e89-124">scriptId in start and end range locations should be the same.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e89-125">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-126">start</span><span class="sxs-lookup"><span data-stu-id="11e89-126">start</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="11e89-127">Início do intervalo para pesquisar possíveis locais de ponto de interrupção em.</span><span class="sxs-lookup"><span data-stu-id="11e89-127">Start of range to search possible breakpoint locations in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-128">encerrar</span><span class="sxs-lookup"><span data-stu-id="11e89-128">end</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="11e89-129">Fim do intervalo para pesquisar possíveis locais de ponto de interrupção (excluindo).</span><span class="sxs-lookup"><span data-stu-id="11e89-129">End of range to search possible breakpoint locations in (excluding).</span></span> <span data-ttu-id="11e89-130">Quando não especificado, o final dos scripts é usado como final do intervalo.</span><span class="sxs-lookup"><span data-stu-id="11e89-130">When not specified, end of scripts is used as end of range.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-131">Devolver</span><span class="sxs-lookup"><span data-stu-id="11e89-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-132">localiza</span><span class="sxs-lookup"><span data-stu-id="11e89-132">locations</span></span></td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td><span data-ttu-id="11e89-133">Lista de possíveis locais de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="11e89-133">List of the possible breakpoint locations.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="11e89-134">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="11e89-134">setBreakpointsActive</span></span>
<span data-ttu-id="11e89-135">Ativa/desativa todos os pontos de interrupção na página.</span><span class="sxs-lookup"><span data-stu-id="11e89-135">Activates / deactivates all breakpoints on the page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-136">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e89-136">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-137">active</span><span class="sxs-lookup"><span data-stu-id="11e89-137">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="11e89-138">Novo valor para o estado ativo dos pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="11e89-138">New value for breakpoints active state.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="11e89-139">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="11e89-139">setBreakpointByUrl</span></span>
<span data-ttu-id="11e89-140">Define o ponto de interrupção JavaScript em um determinado local especificado por URL ou Regex de URL.</span><span class="sxs-lookup"><span data-stu-id="11e89-140">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span> <span data-ttu-id="11e89-141">Depois que esse comando for emitido, todos os scripts analisados existentes terão pontos de interrupção resolvidos e retornados na <code>locations</code> propriedade.</span><span class="sxs-lookup"><span data-stu-id="11e89-141">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in <code>locations</code> property.</span></span> <span data-ttu-id="11e89-142">A análise de script correspondente resultará em eventos subsequentes <code>breakpointResolved</code> emitidos.</span><span class="sxs-lookup"><span data-stu-id="11e89-142">Further matching script parsing will result in subsequent <code>breakpointResolved</code> events issued.</span></span> <span data-ttu-id="11e89-143">Esse ponto de interrupção lógico permanecerá recarregamentos de página.</span><span class="sxs-lookup"><span data-stu-id="11e89-143">This logical breakpoint will survive page reloads.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-144">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e89-144">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-145">lineNumber</span><span class="sxs-lookup"><span data-stu-id="11e89-145">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="11e89-146">Número da linha para definir o ponto de interrupção em.</span><span class="sxs-lookup"><span data-stu-id="11e89-146">Line number to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-147">url</span><span class="sxs-lookup"><span data-stu-id="11e89-147">url</span></span> <br/> <i><span data-ttu-id="11e89-148">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-148">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="11e89-149">URL dos recursos para definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="11e89-149">URL of the resources to set breakpoint on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-150">urlRegex</span><span class="sxs-lookup"><span data-stu-id="11e89-150">urlRegex</span></span> <br/> <i><span data-ttu-id="11e89-151">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-151">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="11e89-152">Padrão Regex para as URLs dos recursos para definir os pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="11e89-152">Regex pattern for the URLs of the resources to set breakpoints on.</span></span> <span data-ttu-id="11e89-153"><code>url</code>Ou <code>urlRegex</code> deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="11e89-153">Either <code>url</code> or <code>urlRegex</code> must be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-154">columnNumber</span><span class="sxs-lookup"><span data-stu-id="11e89-154">columnNumber</span></span> <br/> <i><span data-ttu-id="11e89-155">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-155">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="11e89-156">Offset na linha para definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="11e89-156">Offset in the line to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-157">problema</span><span class="sxs-lookup"><span data-stu-id="11e89-157">condition</span></span> <br/> <i><span data-ttu-id="11e89-158">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-158">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="11e89-159">Expressão a ser usada como uma condição de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="11e89-159">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="11e89-160">Quando especificado, o depurador só será interrompido no ponto de interrupção se essa expressão for avaliada como true.</span><span class="sxs-lookup"><span data-stu-id="11e89-160">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-161">Devolver</span><span class="sxs-lookup"><span data-stu-id="11e89-161">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-162">breakpointid</span><span class="sxs-lookup"><span data-stu-id="11e89-162">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="11e89-163">ID do ponto de interrupção criado para referência adicional.</span><span class="sxs-lookup"><span data-stu-id="11e89-163">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-164">localiza</span><span class="sxs-lookup"><span data-stu-id="11e89-164">locations</span></span></td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td><span data-ttu-id="11e89-165">Lista de locais para os quais esse ponto de interrupção foi resolvido após adição.</span><span class="sxs-lookup"><span data-stu-id="11e89-165">List of the locations this breakpoint resolved into upon addition.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="11e89-166">SetBreakpoint</span><span class="sxs-lookup"><span data-stu-id="11e89-166">setBreakpoint</span></span>
<span data-ttu-id="11e89-167">Define o ponto de interrupção JavaScript em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="11e89-167">Sets JavaScript breakpoint at a given location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-168">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e89-168">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-169">ponto</span><span class="sxs-lookup"><span data-stu-id="11e89-169">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="11e89-170">Local para definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="11e89-170">Location to set breakpoint in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-171">problema</span><span class="sxs-lookup"><span data-stu-id="11e89-171">condition</span></span> <br/> <i><span data-ttu-id="11e89-172">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-172">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="11e89-173">Expressão a ser usada como uma condição de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="11e89-173">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="11e89-174">Quando especificado, o depurador só será interrompido no ponto de interrupção se essa expressão for avaliada como true.</span><span class="sxs-lookup"><span data-stu-id="11e89-174">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-175">Devolver</span><span class="sxs-lookup"><span data-stu-id="11e89-175">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-176">breakpointid</span><span class="sxs-lookup"><span data-stu-id="11e89-176">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="11e89-177">ID do ponto de interrupção criado para referência adicional.</span><span class="sxs-lookup"><span data-stu-id="11e89-177">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-178">actualLocation</span><span class="sxs-lookup"><span data-stu-id="11e89-178">actualLocation</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="11e89-179">Local em que este ponto de interrupção foi resolvido.</span><span class="sxs-lookup"><span data-stu-id="11e89-179">Location this breakpoint resolved into.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="11e89-180">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="11e89-180">removeBreakpoint</span></span>
<span data-ttu-id="11e89-181">Remove o ponto de interrupção JavaScript.</span><span class="sxs-lookup"><span data-stu-id="11e89-181">Removes JavaScript breakpoint.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-182">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e89-182">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-183">breakpointid</span><span class="sxs-lookup"><span data-stu-id="11e89-183">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="11e89-184">stepOver</span><span class="sxs-lookup"><span data-stu-id="11e89-184">stepOver</span></span>
<span data-ttu-id="11e89-185">Etapas sobre a instrução.</span><span class="sxs-lookup"><span data-stu-id="11e89-185">Steps over the statement.</span></span>


---

### <span data-ttu-id="11e89-186">stepInto</span><span class="sxs-lookup"><span data-stu-id="11e89-186">stepInto</span></span>
<span data-ttu-id="11e89-187">Etapas para a chamada de função.</span><span class="sxs-lookup"><span data-stu-id="11e89-187">Steps into the function call.</span></span>


---

### <span data-ttu-id="11e89-188">passo a passo</span><span class="sxs-lookup"><span data-stu-id="11e89-188">stepOut</span></span>
<span data-ttu-id="11e89-189">Etapas para sair da chamada de função.</span><span class="sxs-lookup"><span data-stu-id="11e89-189">Steps out of the function call.</span></span>


---

### <span data-ttu-id="11e89-190">pause</span><span class="sxs-lookup"><span data-stu-id="11e89-190">pause</span></span>
<span data-ttu-id="11e89-191">Para a próxima instrução JavaScript.</span><span class="sxs-lookup"><span data-stu-id="11e89-191">Stops on the next JavaScript statement.</span></span>


---

### <span data-ttu-id="11e89-192">resume</span><span class="sxs-lookup"><span data-stu-id="11e89-192">resume</span></span>
<span data-ttu-id="11e89-193">Retoma a execução do JavaScript.</span><span class="sxs-lookup"><span data-stu-id="11e89-193">Resumes JavaScript execution.</span></span>


---

### <span data-ttu-id="11e89-194">getscriptname</span><span class="sxs-lookup"><span data-stu-id="11e89-194">getScriptSource</span></span>
<span data-ttu-id="11e89-195">Retorna a origem do script com ID especificado.</span><span class="sxs-lookup"><span data-stu-id="11e89-195">Returns source for the script with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-196">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e89-196">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-197">scriptid</span><span class="sxs-lookup"><span data-stu-id="11e89-197">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="11e89-198">ID do script para o qual obter a fonte.</span><span class="sxs-lookup"><span data-stu-id="11e89-198">Id of the script to get source for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-199">Devolver</span><span class="sxs-lookup"><span data-stu-id="11e89-199">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-200">scriptização</span><span class="sxs-lookup"><span data-stu-id="11e89-200">scriptSource</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="11e89-201">Fonte de script.</span><span class="sxs-lookup"><span data-stu-id="11e89-201">Script source.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="11e89-202">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="11e89-202">setPauseOnExceptions</span></span>
<span data-ttu-id="11e89-203">Define o estado pausar exceções.</span><span class="sxs-lookup"><span data-stu-id="11e89-203">Defines pause on exceptions state.</span></span> <span data-ttu-id="11e89-204">Pode ser definido para interromper todas as exceções, exceções não capturadas ou nenhuma exceção.</span><span class="sxs-lookup"><span data-stu-id="11e89-204">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span> <span data-ttu-id="11e89-205">O estado de pausa inicial em exceções é <code>none</code> .</span><span class="sxs-lookup"><span data-stu-id="11e89-205">Initial pause on exceptions state is <code>none</code>.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-206">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e89-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-207">Estado</span><span class="sxs-lookup"><span data-stu-id="11e89-207">state</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="11e89-208">Valores permitidos: None, unpercebeud, All</span><span class="sxs-lookup"><span data-stu-id="11e89-208">Allowed values: none, uncaught, all</span></span></i></td>
            <td><span data-ttu-id="11e89-209">Pausar no modo de exceções.</span><span class="sxs-lookup"><span data-stu-id="11e89-209">Pause on exceptions mode.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="11e89-210">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="11e89-210">evaluateOnCallFrame</span></span>
<span data-ttu-id="11e89-211">Avalia a expressão em um determinado quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="11e89-211">Evaluates expression on a given call frame.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-212">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e89-212">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-213">callFrameId</span><span class="sxs-lookup"><span data-stu-id="11e89-213">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="11e89-214">Identificador de quadro de chamada para avaliação.</span><span class="sxs-lookup"><span data-stu-id="11e89-214">Call frame identifier to evaluate on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-215">Express</span><span class="sxs-lookup"><span data-stu-id="11e89-215">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="11e89-216">Expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="11e89-216">Expression to evaluate.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-217">Devolver</span><span class="sxs-lookup"><span data-stu-id="11e89-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-218">levar</span><span class="sxs-lookup"><span data-stu-id="11e89-218">result</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="11e89-219">Wrapper do objeto para o resultado da avaliação.</span><span class="sxs-lookup"><span data-stu-id="11e89-219">Object wrapper for the evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="11e89-220">setvariablevalue</span><span class="sxs-lookup"><span data-stu-id="11e89-220">setVariableValue</span></span>
<span data-ttu-id="11e89-221">Altera o valor da variável em um callframe.</span><span class="sxs-lookup"><span data-stu-id="11e89-221">Changes value of variable in a callframe.</span></span> <span data-ttu-id="11e89-222">Escopos baseados em objeto não são compatíveis e devem ser modificados manualmente.</span><span class="sxs-lookup"><span data-stu-id="11e89-222">Object-based scopes are not supported and must be mutated manually.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-223">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e89-223">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-224">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="11e89-224">scopeNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="11e89-225">número baseado em 0 do escopo como foi listado na cadeia de escopos.</span><span class="sxs-lookup"><span data-stu-id="11e89-225">0-based number of scope as was listed in scope chain.</span></span> <span data-ttu-id="11e89-226">Somente os tipos de escopo ' local ', ' fechamento ' e ' Catch ' são permitidos.</span><span class="sxs-lookup"><span data-stu-id="11e89-226">Only 'local', 'closure' and 'catch' scope types are allowed.</span></span> <span data-ttu-id="11e89-227">Outros escopos podem ser manipulados manualmente.</span><span class="sxs-lookup"><span data-stu-id="11e89-227">Other scopes could be manipulated manually.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-228">VariableName</span><span class="sxs-lookup"><span data-stu-id="11e89-228">variableName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="11e89-229">Nome da variável.</span><span class="sxs-lookup"><span data-stu-id="11e89-229">Variable name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-230">newValue</span><span class="sxs-lookup"><span data-stu-id="11e89-230">newValue</span></span></td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td><span data-ttu-id="11e89-231">Novo valor de variável.</span><span class="sxs-lookup"><span data-stu-id="11e89-231">New variable value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-232">callFrameId</span><span class="sxs-lookup"><span data-stu-id="11e89-232">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="11e89-233">ID de callframe que mantém a variável.</span><span class="sxs-lookup"><span data-stu-id="11e89-233">Id of callframe that holds variable.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="11e89-234">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="11e89-234">setBlackboxPatterns</span></span>
<span><b><span data-ttu-id="11e89-235">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="11e89-235">Experimental.</span></span> </b></span><span data-ttu-id="11e89-236">Substituir os padrões de Blackbox anteriores pelos aprovados.</span><span class="sxs-lookup"><span data-stu-id="11e89-236">Replace previous blackbox patterns with passed ones.</span></span> <span data-ttu-id="11e89-237">Força o back-end a ignorar a depuração/pausa em scripts com URL correspondente a um dos padrões.</span><span class="sxs-lookup"><span data-stu-id="11e89-237">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span> <span data-ttu-id="11e89-238">O depurador tentará deixar o script do blackboxed executando ' Step in ' várias vezes, finalmente reclassificando para "Step Out" se não tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="11e89-238">The debugger will try to leave blackboxed script by performing 'step in' several times, finally resorting to 'step out' if unsuccessful.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-239">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e89-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-240">padrões</span><span class="sxs-lookup"><span data-stu-id="11e89-240">patterns</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="11e89-241">Matriz de regexps que será usada para verificar a URL do script para o estado Blackbox.</span><span class="sxs-lookup"><span data-stu-id="11e89-241">Array of regexps that will be used to check script url for blackbox state.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="11e89-242">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="11e89-242">msSetDebuggerPropertyValue</span></span>
<span><b><span data-ttu-id="11e89-243">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="11e89-243">Experimental.</span></span> </b></span><span data-ttu-id="11e89-244">Microsoft: define a Propriedade Debugger especificada para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="11e89-244">Microsoft: Sets the specified debugger property to the specified value.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-245">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e89-245">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-246">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="11e89-246">debuggerPropertyId</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="11e89-247">Microsoft: a identificação da propriedade (por exemplo, msDebuggerPropertyId) a ser definida.</span><span class="sxs-lookup"><span data-stu-id="11e89-247">Microsoft: The property id (i.e. msDebuggerPropertyId) to set.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-248">newValue</span><span class="sxs-lookup"><span data-stu-id="11e89-248">newValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="11e89-249">Eventos</span><span class="sxs-lookup"><span data-stu-id="11e89-249">Events</span></span>

### <span data-ttu-id="11e89-250">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="11e89-250">scriptParsed</span></span>
<span data-ttu-id="11e89-251">Acionado quando o script é analisado.</span><span class="sxs-lookup"><span data-stu-id="11e89-251">Fired when the script is parsed.</span></span> <span data-ttu-id="11e89-252">Esse evento também é disparado para todos os scripts conhecidos e não coletados, quando o depurador é ativado.</span><span class="sxs-lookup"><span data-stu-id="11e89-252">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-253">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e89-253">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-254">scriptid</span><span class="sxs-lookup"><span data-stu-id="11e89-254">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="11e89-255">Identificador do script analisado.</span><span class="sxs-lookup"><span data-stu-id="11e89-255">Identifier of the script parsed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-256">url</span><span class="sxs-lookup"><span data-stu-id="11e89-256">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="11e89-257">URL ou nome do script analisado (se houver).</span><span class="sxs-lookup"><span data-stu-id="11e89-257">URL or name of the script parsed (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-258">início</span><span class="sxs-lookup"><span data-stu-id="11e89-258">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="11e89-259">Deslocamento de linha do script dentro do recurso com a URL fornecida (para marcas de script).</span><span class="sxs-lookup"><span data-stu-id="11e89-259">Line offset of the script within the resource with given URL (for script tags).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-260">startColumn</span><span class="sxs-lookup"><span data-stu-id="11e89-260">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="11e89-261">O deslocamento da coluna do script dentro do recurso com a URL fornecida.</span><span class="sxs-lookup"><span data-stu-id="11e89-261">Column offset of the script within the resource with given URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-262">Line</span><span class="sxs-lookup"><span data-stu-id="11e89-262">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="11e89-263">Última linha do script.</span><span class="sxs-lookup"><span data-stu-id="11e89-263">Last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-264">Coluna de EndColumn</span><span class="sxs-lookup"><span data-stu-id="11e89-264">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="11e89-265">Comprimento da última linha do script.</span><span class="sxs-lookup"><span data-stu-id="11e89-265">Length of the last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-266">executionContextid</span><span class="sxs-lookup"><span data-stu-id="11e89-266">executionContextId</span></span></td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td><span data-ttu-id="11e89-267">Especifica o contexto de criação de script.</span><span class="sxs-lookup"><span data-stu-id="11e89-267">Specifies script creation context.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-268">sourceMapURL</span><span class="sxs-lookup"><span data-stu-id="11e89-268">sourceMapURL</span></span> <br/> <i><span data-ttu-id="11e89-269">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-269">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="11e89-270">URL do mapa de origem associado ao script (se houver).</span><span class="sxs-lookup"><span data-stu-id="11e89-270">URL of source map associated with script (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-271">das</span><span class="sxs-lookup"><span data-stu-id="11e89-271">length</span></span> <br/> <i><span data-ttu-id="11e89-272">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-272">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="11e89-273">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="11e89-273">Experimental.</span></span> </b></span><span data-ttu-id="11e89-274">Esse tamanho do script.</span><span class="sxs-lookup"><span data-stu-id="11e89-274">This script length.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-275">msParentId</span><span class="sxs-lookup"><span data-stu-id="11e89-275">msParentId</span></span> <br/> <i><span data-ttu-id="11e89-276">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-276">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="11e89-277">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="11e89-277">Experimental.</span></span> </b></span><span data-ttu-id="11e89-278">Esta é a ID do documento pai.</span><span class="sxs-lookup"><span data-stu-id="11e89-278">This is the parent document ID.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-279">msMimeType</span><span class="sxs-lookup"><span data-stu-id="11e89-279">msMimeType</span></span> <br/> <i><span data-ttu-id="11e89-280">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-280">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="11e89-281">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="11e89-281">Experimental.</span></span> </b></span><span data-ttu-id="11e89-282">Esse é o tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="11e89-282">This is the mime type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-283">msIsDynamicCode</span><span class="sxs-lookup"><span data-stu-id="11e89-283">msIsDynamicCode</span></span> <br/> <i><span data-ttu-id="11e89-284">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-284">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="11e89-285">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="11e89-285">Experimental.</span></span> </b></span><span data-ttu-id="11e89-286">Isso indica se é um código dinâmico.</span><span class="sxs-lookup"><span data-stu-id="11e89-286">This indicates whether it is dynamic code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-287">msLongDocumentId</span><span class="sxs-lookup"><span data-stu-id="11e89-287">msLongDocumentId</span></span> <br/> <i><span data-ttu-id="11e89-288">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-288">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="11e89-289">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="11e89-289">Experimental.</span></span> </b></span><span data-ttu-id="11e89-290">Esta é a ID do documento longo.</span><span class="sxs-lookup"><span data-stu-id="11e89-290">This is the long document ID.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="11e89-291">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="11e89-291">breakpointResolved</span></span>
<span data-ttu-id="11e89-292">Disparado quando o ponto de interrupção é resolvido para um script e local reais.</span><span class="sxs-lookup"><span data-stu-id="11e89-292">Fired when breakpoint is resolved to an actual script and location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-293">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e89-293">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-294">breakpointid</span><span class="sxs-lookup"><span data-stu-id="11e89-294">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="11e89-295">Identificador exclusivo de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="11e89-295">Breakpoint unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-296">ponto</span><span class="sxs-lookup"><span data-stu-id="11e89-296">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="11e89-297">Local do ponto de interrupção real.</span><span class="sxs-lookup"><span data-stu-id="11e89-297">Actual breakpoint location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-298">msLength</span><span class="sxs-lookup"><span data-stu-id="11e89-298">msLength</span></span> <br/> <i><span data-ttu-id="11e89-299">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-299">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="11e89-300">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="11e89-300">Experimental.</span></span> </b></span><span data-ttu-id="11e89-301">Microsoft: comprimento do código (ou seja, número de caracteres) no local do ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="11e89-301">Microsoft: Length of code (i.e. number of characters) at the breakpoint location.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="11e89-302">pausado</span><span class="sxs-lookup"><span data-stu-id="11e89-302">paused</span></span>
<span data-ttu-id="11e89-303">Acionado quando os depuradores violam um ponto de interrupção ou uma exceção.</span><span class="sxs-lookup"><span data-stu-id="11e89-303">Fired when the debuggers breaks for a breakpoint or exception.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-304">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e89-304">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-305">callFrames</span><span class="sxs-lookup"><span data-stu-id="11e89-305">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="11e89-306">Pilha de chamadas no depurador interrompido.</span><span class="sxs-lookup"><span data-stu-id="11e89-306">Call stack the debugger stopped on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-307">motivo</span><span class="sxs-lookup"><span data-stu-id="11e89-307">reason</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="11e89-308">Valores permitidos: Breakpoint, Step, Exception, Other</span><span class="sxs-lookup"><span data-stu-id="11e89-308">Allowed values: breakpoint, step, exception, other</span></span></i></td>
            <td><span data-ttu-id="11e89-309">Motivo da pausa.</span><span class="sxs-lookup"><span data-stu-id="11e89-309">Pause reason.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-310">data</span><span class="sxs-lookup"><span data-stu-id="11e89-310">data</span></span> <br/> <i><span data-ttu-id="11e89-311">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-311">optional</span></span></i></td>
            <td><code class="flyout">object</code></td>
            <td><span data-ttu-id="11e89-312">Objeto que contém propriedades auxiliares de quebra específicas.</span><span class="sxs-lookup"><span data-stu-id="11e89-312">Object containing break-specific auxiliary properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-313">hitBreakpoints</span><span class="sxs-lookup"><span data-stu-id="11e89-313">hitBreakpoints</span></span> <br/> <i><span data-ttu-id="11e89-314">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-314">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="11e89-315">IDs de pontos de interrupção de acesso</span><span class="sxs-lookup"><span data-stu-id="11e89-315">Hit breakpoints IDs</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="11e89-316">retomado</span><span class="sxs-lookup"><span data-stu-id="11e89-316">resumed</span></span>
<span data-ttu-id="11e89-317">Acionado quando o depurador retomar a execução.</span><span class="sxs-lookup"><span data-stu-id="11e89-317">Fired when the debugger resumes execution.</span></span>


---

## <span data-ttu-id="11e89-318">Tipos</span><span class="sxs-lookup"><span data-stu-id="11e89-318">Types</span></span>

### <a name="breakpointid"></a> <span data-ttu-id="11e89-319">Breakpointid</span><span class="sxs-lookup"><span data-stu-id="11e89-319">BreakpointId</span></span> `string`

<span data-ttu-id="11e89-320">Identificador de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="11e89-320">Breakpoint identifier.</span></span>


---

### <a name="callframeid"></a> <span data-ttu-id="11e89-321">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="11e89-321">CallFrameId</span></span> `string`

<span data-ttu-id="11e89-322">Identificador de quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="11e89-322">Call frame identifier.</span></span>


---

### <a name="location"></a> <span data-ttu-id="11e89-323">Location</span><span class="sxs-lookup"><span data-stu-id="11e89-323">Location</span></span> `object`

<span data-ttu-id="11e89-324">Local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="11e89-324">Location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-325">Propriedades</span><span class="sxs-lookup"><span data-stu-id="11e89-325">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-326">scriptid</span><span class="sxs-lookup"><span data-stu-id="11e89-326">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="11e89-327">Identificador de script reportado no <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="11e89-327">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-328">lineNumber</span><span class="sxs-lookup"><span data-stu-id="11e89-328">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="11e89-329">Número da linha no script (baseado em 0).</span><span class="sxs-lookup"><span data-stu-id="11e89-329">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-330">columnNumber</span><span class="sxs-lookup"><span data-stu-id="11e89-330">columnNumber</span></span> <br/> <i><span data-ttu-id="11e89-331">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-331">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="11e89-332">Número da coluna no script (baseado em 0).</span><span class="sxs-lookup"><span data-stu-id="11e89-332">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-333">msLength</span><span class="sxs-lookup"><span data-stu-id="11e89-333">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="11e89-334">Microsoft: comprimento do código (ou seja, número de caracteres) nesse quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="11e89-334">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="breaklocation"></a> <span data-ttu-id="11e89-335">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="11e89-335">BreakLocation</span></span> `object`

<span data-ttu-id="11e89-336">Interrompa o local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="11e89-336">Break location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-337">Propriedades</span><span class="sxs-lookup"><span data-stu-id="11e89-337">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-338">scriptid</span><span class="sxs-lookup"><span data-stu-id="11e89-338">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="11e89-339">Identificador de script reportado no <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="11e89-339">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-340">lineNumber</span><span class="sxs-lookup"><span data-stu-id="11e89-340">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="11e89-341">Número da linha no script (baseado em 0).</span><span class="sxs-lookup"><span data-stu-id="11e89-341">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-342">columnNumber</span><span class="sxs-lookup"><span data-stu-id="11e89-342">columnNumber</span></span> <br/> <i><span data-ttu-id="11e89-343">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-343">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="11e89-344">Número da coluna no script (baseado em 0).</span><span class="sxs-lookup"><span data-stu-id="11e89-344">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-345">msLength</span><span class="sxs-lookup"><span data-stu-id="11e89-345">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="11e89-346">Microsoft: comprimento do código (ou seja, número de caracteres) nesse quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="11e89-346">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-347">tipo</span><span class="sxs-lookup"><span data-stu-id="11e89-347">type</span></span> <br/> <i><span data-ttu-id="11e89-348">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-348">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="11e89-349">Valores permitidos: debuggerStatement, Call, Return.</span><span class="sxs-lookup"><span data-stu-id="11e89-349">Allowed values: debuggerStatement, call, return.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="callframe"></a> <span data-ttu-id="11e89-350">CallFrame</span><span class="sxs-lookup"><span data-stu-id="11e89-350">CallFrame</span></span> `object`

<span data-ttu-id="11e89-351">Quadro de chamada JavaScript.</span><span class="sxs-lookup"><span data-stu-id="11e89-351">JavaScript call frame.</span></span> <span data-ttu-id="11e89-352">Matriz de quadros de chamadas formam a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="11e89-352">Array of call frames form the call stack.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-353">Propriedades</span><span class="sxs-lookup"><span data-stu-id="11e89-353">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-354">callFrameId</span><span class="sxs-lookup"><span data-stu-id="11e89-354">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="11e89-355">Identificador de quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="11e89-355">Call frame identifier.</span></span> <span data-ttu-id="11e89-356">Esse identificador só é válido enquanto o depurador está pausado.</span><span class="sxs-lookup"><span data-stu-id="11e89-356">This identifier is only valid while the debugger is paused.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-357">função FunctionName</span><span class="sxs-lookup"><span data-stu-id="11e89-357">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="11e89-358">Nome da função JavaScript chamada neste quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="11e89-358">Name of the JavaScript function called on this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-359">functionLocation</span><span class="sxs-lookup"><span data-stu-id="11e89-359">functionLocation</span></span> <br/> <i><span data-ttu-id="11e89-360">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-360">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b><span data-ttu-id="11e89-361">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="11e89-361">Experimental.</span></span> </b></span><span data-ttu-id="11e89-362">Local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="11e89-362">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-363">ponto</span><span class="sxs-lookup"><span data-stu-id="11e89-363">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="11e89-364">Local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="11e89-364">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-365">url</span><span class="sxs-lookup"><span data-stu-id="11e89-365">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="11e89-366">Nome ou URL do script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="11e89-366">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-367">scopeChain</span><span class="sxs-lookup"><span data-stu-id="11e89-367">scopeChain</span></span></td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td><span data-ttu-id="11e89-368">Cadeia de escopos para este quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="11e89-368">Scope chain for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-369">deste</span><span class="sxs-lookup"><span data-stu-id="11e89-369">this</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> <span data-ttu-id="11e89-370">objeto para este quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="11e89-370">object for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-371">returnValue</span><span class="sxs-lookup"><span data-stu-id="11e89-371">returnValue</span></span> <br/> <i><span data-ttu-id="11e89-372">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-372">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="11e89-373">O valor que está sendo retornado, se a função estiver em um ponto de retorno.</span><span class="sxs-lookup"><span data-stu-id="11e89-373">The value being returned, if the function is at return point.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="scope"></a> <span data-ttu-id="11e89-374">Escopo</span><span class="sxs-lookup"><span data-stu-id="11e89-374">Scope</span></span> `object`

<span data-ttu-id="11e89-375">Descrição do escopo.</span><span class="sxs-lookup"><span data-stu-id="11e89-375">Scope description.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="11e89-376">Propriedades</span><span class="sxs-lookup"><span data-stu-id="11e89-376">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="11e89-377">tipo</span><span class="sxs-lookup"><span data-stu-id="11e89-377">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="11e89-378">Valores permitidos: global, local, com, fechamento, catch, Block, script, eval, módulo</span><span class="sxs-lookup"><span data-stu-id="11e89-378">Allowed values: global, local, with, closure, catch, block, script, eval, module</span></span></i></td>
            <td><span data-ttu-id="11e89-379">Tipo de escopo.</span><span class="sxs-lookup"><span data-stu-id="11e89-379">Scope type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-380">object</span><span class="sxs-lookup"><span data-stu-id="11e89-380">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="11e89-381">Objeto que representa o escopo.</span><span class="sxs-lookup"><span data-stu-id="11e89-381">Object representing the scope.</span></span> <span data-ttu-id="11e89-382">Para <code>global</code> e <code>with</code> escopos, ele representa o objeto real; para o restante dos escopos, é um objeto transitório artificial enumerando variáveis de escopo como suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="11e89-382">For <code>global</code> and <code>with</code> scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-383">name</span><span class="sxs-lookup"><span data-stu-id="11e89-383">name</span></span> <br/> <i><span data-ttu-id="11e89-384">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-384">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-385">startLocation</span><span class="sxs-lookup"><span data-stu-id="11e89-385">startLocation</span></span> <br/> <i><span data-ttu-id="11e89-386">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-386">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="11e89-387">Local no código-fonte onde o escopo é iniciado</span><span class="sxs-lookup"><span data-stu-id="11e89-387">Location in the source code where scope starts</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="11e89-388">EndLocation</span><span class="sxs-lookup"><span data-stu-id="11e89-388">endLocation</span></span> <br/> <i><span data-ttu-id="11e89-389">opcional</span><span class="sxs-lookup"><span data-stu-id="11e89-389">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="11e89-390">Local no código-fonte em que termina o escopo</span><span class="sxs-lookup"><span data-stu-id="11e89-390">Location in the source code where scope ends</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="11e89-391">Dependências</span><span class="sxs-lookup"><span data-stu-id="11e89-391">Dependencies</span></span>

[<span data-ttu-id="11e89-392">Classpath</span><span class="sxs-lookup"><span data-stu-id="11e89-392">Runtime</span></span>](runtime.md)