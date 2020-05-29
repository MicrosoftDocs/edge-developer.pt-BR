---
description: Referência para o domínio do depurador. O domínio do depurador expõe recursos de depuração JavaScript. Ele permite definir e remover pontos de interrupção, percorrer a execução, explorar rastreamentos de pilha, etc.
title: Domínio do depurador – versão do protocolo DevTools versão 0,2
author: pelavall
ms.author: pelavall
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: de967b0e067bf43ea07f8975eac7ee7c5a4dfd83
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561343"
---
# <span data-ttu-id="2eaf5-105">Depurador</span><span class="sxs-lookup"><span data-stu-id="2eaf5-105">Debugger</span></span>
<span data-ttu-id="2eaf5-106">O domínio do depurador expõe recursos de depuração JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-106">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="2eaf5-107">Ele permite definir e remover pontos de interrupção, percorrer a execução, explorar rastreamentos de pilha, etc.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="2eaf5-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="2eaf5-108">Methods</span></span>**](#methods) | <span data-ttu-id="2eaf5-109">[habilitar](#enable), [desabilitar](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [SetBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [StepOut](#stepout), [Pause](#pause), [resume](#resume), [getscriptname](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setvariablevalue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="2eaf5-109">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |
| [**<span data-ttu-id="2eaf5-110">Eventos</span><span class="sxs-lookup"><span data-stu-id="2eaf5-110">Events</span></span>**](#events) | <span data-ttu-id="2eaf5-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [pausado](#paused), [retomado](#resumed)</span><span class="sxs-lookup"><span data-stu-id="2eaf5-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |
| [**<span data-ttu-id="2eaf5-112">Tipos</span><span class="sxs-lookup"><span data-stu-id="2eaf5-112">Types</span></span>**](#types) | <span data-ttu-id="2eaf5-113">[Breakpointid](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span><span class="sxs-lookup"><span data-stu-id="2eaf5-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |
| [**<span data-ttu-id="2eaf5-114">Dependências</span><span class="sxs-lookup"><span data-stu-id="2eaf5-114">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="2eaf5-115">Classpath</span><span class="sxs-lookup"><span data-stu-id="2eaf5-115">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="2eaf5-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="2eaf5-116">Methods</span></span>

### <span data-ttu-id="2eaf5-117">Habilitar</span><span class="sxs-lookup"><span data-stu-id="2eaf5-117">enable</span></span>
<span data-ttu-id="2eaf5-118">Habilita o depurador para a página especificada.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-118">Enables debugger for the given page.</span></span> <span data-ttu-id="2eaf5-119">Os clientes não devem presumir que a depuração foi habilitada até que o resultado desse comando seja recebido.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-119">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>

</p>

---

### <span data-ttu-id="2eaf5-120">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="2eaf5-120">disable</span></span>
<span data-ttu-id="2eaf5-121">Desabilita o depurador para determinada página.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-121">Disables debugger for given page.</span></span>

</p>

---

### <span data-ttu-id="2eaf5-122">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="2eaf5-122">getPossibleBreakpoints</span></span>
<span data-ttu-id="2eaf5-123">Retorna possíveis locais para o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-123">Returns possible locations for breakpoint.</span></span> <span data-ttu-id="2eaf5-124">os scripts em locais de intervalo de início e término devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-124">scriptId in start and end range locations should be the same.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eaf5-125">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-126">start</span><span class="sxs-lookup"><span data-stu-id="2eaf5-126">start</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="2eaf5-127">Início do intervalo para pesquisar possíveis locais de ponto de interrupção em.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-127">Start of range to search possible breakpoint locations in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-128">encerrar</span><span class="sxs-lookup"><span data-stu-id="2eaf5-128">end</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="2eaf5-129">Fim do intervalo para pesquisar possíveis locais de ponto de interrupção (excluindo).</span><span class="sxs-lookup"><span data-stu-id="2eaf5-129">End of range to search possible breakpoint locations in (excluding).</span></span> <span data-ttu-id="2eaf5-130">Quando não especificado, o final dos scripts é usado como final do intervalo.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-130">When not specified, end of scripts is used as end of range.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-131">Devolver</span><span class="sxs-lookup"><span data-stu-id="2eaf5-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-132">localiza</span><span class="sxs-lookup"><span data-stu-id="2eaf5-132">locations</span></span></td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td><span data-ttu-id="2eaf5-133">Lista de possíveis locais de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-133">List of the possible breakpoint locations.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2eaf5-134">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="2eaf5-134">setBreakpointsActive</span></span>
<span data-ttu-id="2eaf5-135">Ativa/desativa todos os pontos de interrupção na página.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-135">Activates / deactivates all breakpoints on the page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-136">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eaf5-136">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-137">active</span><span class="sxs-lookup"><span data-stu-id="2eaf5-137">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="2eaf5-138">Novo valor para o estado ativo dos pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-138">New value for breakpoints active state.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2eaf5-139">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="2eaf5-139">setBreakpointByUrl</span></span>
<span data-ttu-id="2eaf5-140">Define o ponto de interrupção JavaScript em um determinado local especificado por URL ou Regex de URL.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-140">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span> <span data-ttu-id="2eaf5-141">Depois que esse comando for emitido, todos os scripts analisados existentes terão pontos de interrupção resolvidos e retornados na <code>locations</code> propriedade.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-141">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in <code>locations</code> property.</span></span> <span data-ttu-id="2eaf5-142">A análise de script correspondente resultará em eventos subsequentes <code>breakpointResolved</code> emitidos.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-142">Further matching script parsing will result in subsequent <code>breakpointResolved</code> events issued.</span></span> <span data-ttu-id="2eaf5-143">Esse ponto de interrupção lógico permanecerá recarregamentos de página.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-143">This logical breakpoint will survive page reloads.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-144">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eaf5-144">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-145">lineNumber</span><span class="sxs-lookup"><span data-stu-id="2eaf5-145">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2eaf5-146">Número da linha para definir o ponto de interrupção em.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-146">Line number to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-147">url</span><span class="sxs-lookup"><span data-stu-id="2eaf5-147">url</span></span> <br/> <i><span data-ttu-id="2eaf5-148">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-148">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2eaf5-149">URL dos recursos para definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-149">URL of the resources to set breakpoint on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-150">urlRegex</span><span class="sxs-lookup"><span data-stu-id="2eaf5-150">urlRegex</span></span> <br/> <i><span data-ttu-id="2eaf5-151">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-151">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2eaf5-152">Padrão Regex para as URLs dos recursos para definir os pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-152">Regex pattern for the URLs of the resources to set breakpoints on.</span></span> <span data-ttu-id="2eaf5-153"><code>url</code>Ou <code>urlRegex</code> deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-153">Either <code>url</code> or <code>urlRegex</code> must be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-154">columnNumber</span><span class="sxs-lookup"><span data-stu-id="2eaf5-154">columnNumber</span></span> <br/> <i><span data-ttu-id="2eaf5-155">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-155">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2eaf5-156">Offset na linha para definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-156">Offset in the line to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-157">problema</span><span class="sxs-lookup"><span data-stu-id="2eaf5-157">condition</span></span> <br/> <i><span data-ttu-id="2eaf5-158">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-158">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2eaf5-159">Expressão a ser usada como uma condição de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-159">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="2eaf5-160">Quando especificado, o depurador só será interrompido no ponto de interrupção se essa expressão for avaliada como true.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-160">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-161">Devolver</span><span class="sxs-lookup"><span data-stu-id="2eaf5-161">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-162">breakpointid</span><span class="sxs-lookup"><span data-stu-id="2eaf5-162">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="2eaf5-163">ID do ponto de interrupção criado para referência adicional.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-163">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-164">localiza</span><span class="sxs-lookup"><span data-stu-id="2eaf5-164">locations</span></span></td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td><span data-ttu-id="2eaf5-165">Lista de locais para os quais esse ponto de interrupção foi resolvido após adição.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-165">List of the locations this breakpoint resolved into upon addition.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2eaf5-166">SetBreakpoint</span><span class="sxs-lookup"><span data-stu-id="2eaf5-166">setBreakpoint</span></span>
<span data-ttu-id="2eaf5-167">Define o ponto de interrupção JavaScript em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-167">Sets JavaScript breakpoint at a given location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-168">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eaf5-168">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-169">ponto</span><span class="sxs-lookup"><span data-stu-id="2eaf5-169">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="2eaf5-170">Local para definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-170">Location to set breakpoint in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-171">problema</span><span class="sxs-lookup"><span data-stu-id="2eaf5-171">condition</span></span> <br/> <i><span data-ttu-id="2eaf5-172">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-172">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2eaf5-173">Expressão a ser usada como uma condição de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-173">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="2eaf5-174">Quando especificado, o depurador só será interrompido no ponto de interrupção se essa expressão for avaliada como true.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-174">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-175">Devolver</span><span class="sxs-lookup"><span data-stu-id="2eaf5-175">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-176">breakpointid</span><span class="sxs-lookup"><span data-stu-id="2eaf5-176">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="2eaf5-177">ID do ponto de interrupção criado para referência adicional.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-177">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-178">actualLocation</span><span class="sxs-lookup"><span data-stu-id="2eaf5-178">actualLocation</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="2eaf5-179">Local em que este ponto de interrupção foi resolvido.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-179">Location this breakpoint resolved into.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2eaf5-180">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="2eaf5-180">removeBreakpoint</span></span>
<span data-ttu-id="2eaf5-181">Remove o ponto de interrupção JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-181">Removes JavaScript breakpoint.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-182">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eaf5-182">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-183">breakpointid</span><span class="sxs-lookup"><span data-stu-id="2eaf5-183">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2eaf5-184">stepOver</span><span class="sxs-lookup"><span data-stu-id="2eaf5-184">stepOver</span></span>
<span data-ttu-id="2eaf5-185">Etapas sobre a instrução.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-185">Steps over the statement.</span></span>

</p>

---

### <span data-ttu-id="2eaf5-186">stepInto</span><span class="sxs-lookup"><span data-stu-id="2eaf5-186">stepInto</span></span>
<span data-ttu-id="2eaf5-187">Etapas para a chamada de função.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-187">Steps into the function call.</span></span>

</p>

---

### <span data-ttu-id="2eaf5-188">passo a passo</span><span class="sxs-lookup"><span data-stu-id="2eaf5-188">stepOut</span></span>
<span data-ttu-id="2eaf5-189">Etapas para sair da chamada de função.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-189">Steps out of the function call.</span></span>

</p>

---

### <span data-ttu-id="2eaf5-190">pause</span><span class="sxs-lookup"><span data-stu-id="2eaf5-190">pause</span></span>
<span data-ttu-id="2eaf5-191">Para a próxima instrução JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-191">Stops on the next JavaScript statement.</span></span>

</p>

---

### <span data-ttu-id="2eaf5-192">resume</span><span class="sxs-lookup"><span data-stu-id="2eaf5-192">resume</span></span>
<span data-ttu-id="2eaf5-193">Retoma a execução do JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-193">Resumes JavaScript execution.</span></span>

</p>

---

### <span data-ttu-id="2eaf5-194">getscriptname</span><span class="sxs-lookup"><span data-stu-id="2eaf5-194">getScriptSource</span></span>
<span data-ttu-id="2eaf5-195">Retorna a origem do script com ID especificado.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-195">Returns source for the script with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-196">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eaf5-196">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-197">scriptid</span><span class="sxs-lookup"><span data-stu-id="2eaf5-197">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="2eaf5-198">ID do script para o qual obter a fonte.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-198">Id of the script to get source for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-199">Devolver</span><span class="sxs-lookup"><span data-stu-id="2eaf5-199">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-200">scriptização</span><span class="sxs-lookup"><span data-stu-id="2eaf5-200">scriptSource</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2eaf5-201">Fonte de script.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-201">Script source.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2eaf5-202">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="2eaf5-202">setPauseOnExceptions</span></span>
<span data-ttu-id="2eaf5-203">Define o estado pausar exceções.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-203">Defines pause on exceptions state.</span></span> <span data-ttu-id="2eaf5-204">Pode ser definido para interromper todas as exceções, exceções não capturadas ou nenhuma exceção.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-204">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span> <span data-ttu-id="2eaf5-205">O estado de pausa inicial em exceções é <code>none</code> .</span><span class="sxs-lookup"><span data-stu-id="2eaf5-205">Initial pause on exceptions state is <code>none</code>.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-206">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eaf5-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-207">Estado</span><span class="sxs-lookup"><span data-stu-id="2eaf5-207">state</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="2eaf5-208">Valores permitidos: None, unpercebeud, All</span><span class="sxs-lookup"><span data-stu-id="2eaf5-208">Allowed values: none, uncaught, all</span></span></i></td>
            <td><span data-ttu-id="2eaf5-209">Pausar no modo de exceções.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-209">Pause on exceptions mode.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2eaf5-210">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="2eaf5-210">evaluateOnCallFrame</span></span>
<span data-ttu-id="2eaf5-211">Avalia a expressão em um determinado quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-211">Evaluates expression on a given call frame.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-212">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eaf5-212">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-213">callFrameId</span><span class="sxs-lookup"><span data-stu-id="2eaf5-213">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="2eaf5-214">Identificador de quadro de chamada para avaliação.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-214">Call frame identifier to evaluate on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-215">Express</span><span class="sxs-lookup"><span data-stu-id="2eaf5-215">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2eaf5-216">Expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-216">Expression to evaluate.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-217">Devolver</span><span class="sxs-lookup"><span data-stu-id="2eaf5-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-218">levar</span><span class="sxs-lookup"><span data-stu-id="2eaf5-218">result</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="2eaf5-219">Wrapper do objeto para o resultado da avaliação.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-219">Object wrapper for the evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2eaf5-220">setvariablevalue</span><span class="sxs-lookup"><span data-stu-id="2eaf5-220">setVariableValue</span></span>
<span data-ttu-id="2eaf5-221">Altera o valor da variável em um callframe.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-221">Changes value of variable in a callframe.</span></span> <span data-ttu-id="2eaf5-222">Escopos baseados em objeto não são compatíveis e devem ser modificados manualmente.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-222">Object-based scopes are not supported and must be mutated manually.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-223">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eaf5-223">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-224">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="2eaf5-224">scopeNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2eaf5-225">número baseado em 0 do escopo como foi listado na cadeia de escopos.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-225">0-based number of scope as was listed in scope chain.</span></span> <span data-ttu-id="2eaf5-226">Somente os tipos de escopo ' local ', ' fechamento ' e ' Catch ' são permitidos.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-226">Only 'local', 'closure' and 'catch' scope types are allowed.</span></span> <span data-ttu-id="2eaf5-227">Outros escopos podem ser manipulados manualmente.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-227">Other scopes could be manipulated manually.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-228">VariableName</span><span class="sxs-lookup"><span data-stu-id="2eaf5-228">variableName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2eaf5-229">Nome da variável.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-229">Variable name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-230">newValue</span><span class="sxs-lookup"><span data-stu-id="2eaf5-230">newValue</span></span></td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td><span data-ttu-id="2eaf5-231">Novo valor de variável.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-231">New variable value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-232">callFrameId</span><span class="sxs-lookup"><span data-stu-id="2eaf5-232">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="2eaf5-233">ID de callframe que mantém a variável.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-233">Id of callframe that holds variable.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2eaf5-234">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="2eaf5-234">setBlackboxPatterns</span></span>
<span><b><span data-ttu-id="2eaf5-235">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-235">Experimental.</span></span> </b></span><span data-ttu-id="2eaf5-236">Substituir os padrões de Blackbox anteriores pelos aprovados.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-236">Replace previous blackbox patterns with passed ones.</span></span> <span data-ttu-id="2eaf5-237">Força o back-end a ignorar a depuração/pausa em scripts com URL correspondente a um dos padrões.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-237">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span> <span data-ttu-id="2eaf5-238">O depurador tentará deixar o script do blackboxed executando ' Step in ' várias vezes, finalmente reclassificando para "Step Out" se não tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-238">The debugger will try to leave blackboxed script by performing 'step in' several times, finally resorting to 'step out' if unsuccessful.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-239">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eaf5-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-240">padrões</span><span class="sxs-lookup"><span data-stu-id="2eaf5-240">patterns</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="2eaf5-241">Matriz de regexps que será usada para verificar a URL do script para o estado Blackbox.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-241">Array of regexps that will be used to check script url for blackbox state.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2eaf5-242">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="2eaf5-242">msSetDebuggerPropertyValue</span></span>
<span><b><span data-ttu-id="2eaf5-243">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-243">Experimental.</span></span> </b></span><span data-ttu-id="2eaf5-244">Microsoft: define a Propriedade Debugger especificada para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-244">Microsoft: Sets the specified debugger property to the specified value.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-245">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eaf5-245">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-246">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="2eaf5-246">debuggerPropertyId</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2eaf5-247">Microsoft: a identificação da propriedade (por exemplo, msDebuggerPropertyId) a ser definida.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-247">Microsoft: The property id (i.e. msDebuggerPropertyId) to set.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-248">newValue</span><span class="sxs-lookup"><span data-stu-id="2eaf5-248">newValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="2eaf5-249">Eventos</span><span class="sxs-lookup"><span data-stu-id="2eaf5-249">Events</span></span>

### <span data-ttu-id="2eaf5-250">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="2eaf5-250">scriptParsed</span></span>
<span data-ttu-id="2eaf5-251">Acionado quando o script é analisado.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-251">Fired when the script is parsed.</span></span> <span data-ttu-id="2eaf5-252">Esse evento também é disparado para todos os scripts conhecidos e não coletados, quando o depurador é ativado.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-252">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-253">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eaf5-253">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-254">scriptid</span><span class="sxs-lookup"><span data-stu-id="2eaf5-254">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="2eaf5-255">Identificador do script analisado.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-255">Identifier of the script parsed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-256">url</span><span class="sxs-lookup"><span data-stu-id="2eaf5-256">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2eaf5-257">URL ou nome do script analisado (se houver).</span><span class="sxs-lookup"><span data-stu-id="2eaf5-257">URL or name of the script parsed (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-258">início</span><span class="sxs-lookup"><span data-stu-id="2eaf5-258">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2eaf5-259">Deslocamento de linha do script dentro do recurso com a URL fornecida (para marcas de script).</span><span class="sxs-lookup"><span data-stu-id="2eaf5-259">Line offset of the script within the resource with given URL (for script tags).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-260">startColumn</span><span class="sxs-lookup"><span data-stu-id="2eaf5-260">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2eaf5-261">O deslocamento da coluna do script dentro do recurso com a URL fornecida.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-261">Column offset of the script within the resource with given URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-262">Line</span><span class="sxs-lookup"><span data-stu-id="2eaf5-262">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2eaf5-263">Última linha do script.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-263">Last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-264">Coluna de EndColumn</span><span class="sxs-lookup"><span data-stu-id="2eaf5-264">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2eaf5-265">Comprimento da última linha do script.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-265">Length of the last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-266">executionContextid</span><span class="sxs-lookup"><span data-stu-id="2eaf5-266">executionContextId</span></span></td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td><span data-ttu-id="2eaf5-267">Especifica o contexto de criação de script.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-267">Specifies script creation context.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-268">sourceMapURL</span><span class="sxs-lookup"><span data-stu-id="2eaf5-268">sourceMapURL</span></span> <br/> <i><span data-ttu-id="2eaf5-269">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-269">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2eaf5-270">URL do mapa de origem associado ao script (se houver).</span><span class="sxs-lookup"><span data-stu-id="2eaf5-270">URL of source map associated with script (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-271">das</span><span class="sxs-lookup"><span data-stu-id="2eaf5-271">length</span></span> <br/> <i><span data-ttu-id="2eaf5-272">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-272">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="2eaf5-273">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-273">Experimental.</span></span> </b></span><span data-ttu-id="2eaf5-274">Esse tamanho do script.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-274">This script length.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-275">msParentId</span><span class="sxs-lookup"><span data-stu-id="2eaf5-275">msParentId</span></span> <br/> <i><span data-ttu-id="2eaf5-276">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-276">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="2eaf5-277">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-277">Experimental.</span></span> </b></span><span data-ttu-id="2eaf5-278">Esta é a ID do documento pai.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-278">This is the parent document ID.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-279">msMimeType</span><span class="sxs-lookup"><span data-stu-id="2eaf5-279">msMimeType</span></span> <br/> <i><span data-ttu-id="2eaf5-280">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-280">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="2eaf5-281">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-281">Experimental.</span></span> </b></span><span data-ttu-id="2eaf5-282">Esse é o tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-282">This is the mime type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-283">msIsDynamicCode</span><span class="sxs-lookup"><span data-stu-id="2eaf5-283">msIsDynamicCode</span></span> <br/> <i><span data-ttu-id="2eaf5-284">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-284">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="2eaf5-285">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-285">Experimental.</span></span> </b></span><span data-ttu-id="2eaf5-286">Isso indica se é um código dinâmico.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-286">This indicates whether it is dynamic code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-287">msLongDocumentId</span><span class="sxs-lookup"><span data-stu-id="2eaf5-287">msLongDocumentId</span></span> <br/> <i><span data-ttu-id="2eaf5-288">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-288">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="2eaf5-289">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-289">Experimental.</span></span> </b></span><span data-ttu-id="2eaf5-290">Esta é a ID do documento longo.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-290">This is the long document ID.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2eaf5-291">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="2eaf5-291">breakpointResolved</span></span>
<span data-ttu-id="2eaf5-292">Disparado quando o ponto de interrupção é resolvido para um script e local reais.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-292">Fired when breakpoint is resolved to an actual script and location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-293">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eaf5-293">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-294">breakpointid</span><span class="sxs-lookup"><span data-stu-id="2eaf5-294">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="2eaf5-295">Identificador exclusivo de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-295">Breakpoint unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-296">ponto</span><span class="sxs-lookup"><span data-stu-id="2eaf5-296">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="2eaf5-297">Local do ponto de interrupção real.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-297">Actual breakpoint location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-298">msLength</span><span class="sxs-lookup"><span data-stu-id="2eaf5-298">msLength</span></span> <br/> <i><span data-ttu-id="2eaf5-299">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-299">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="2eaf5-300">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-300">Experimental.</span></span> </b></span><span data-ttu-id="2eaf5-301">Microsoft: comprimento do código (ou seja, número de caracteres) no local do ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-301">Microsoft: Length of code (i.e. number of characters) at the breakpoint location.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2eaf5-302">pausado</span><span class="sxs-lookup"><span data-stu-id="2eaf5-302">paused</span></span>
<span data-ttu-id="2eaf5-303">Acionado quando os depuradores violam um ponto de interrupção ou uma exceção.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-303">Fired when the debuggers breaks for a breakpoint or exception.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-304">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eaf5-304">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-305">callFrames</span><span class="sxs-lookup"><span data-stu-id="2eaf5-305">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="2eaf5-306">Pilha de chamadas no depurador interrompido.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-306">Call stack the debugger stopped on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-307">motivo</span><span class="sxs-lookup"><span data-stu-id="2eaf5-307">reason</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="2eaf5-308">Valores permitidos: Breakpoint, Step, Exception, Other, EventListener</span><span class="sxs-lookup"><span data-stu-id="2eaf5-308">Allowed values: breakpoint, step, exception, other, EventListener</span></span></i></td>
            <td><span data-ttu-id="2eaf5-309">Motivo da pausa.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-309">Pause reason.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-310">data</span><span class="sxs-lookup"><span data-stu-id="2eaf5-310">data</span></span> <br/> <i><span data-ttu-id="2eaf5-311">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-311">optional</span></span></i></td>
            <td><code class="flyout">object</code></td>
            <td><span data-ttu-id="2eaf5-312">Objeto que contém propriedades auxiliares de quebra específicas.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-312">Object containing break-specific auxiliary properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-313">hitBreakpoints</span><span class="sxs-lookup"><span data-stu-id="2eaf5-313">hitBreakpoints</span></span> <br/> <i><span data-ttu-id="2eaf5-314">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-314">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="2eaf5-315">IDs de pontos de interrupção de acesso</span><span class="sxs-lookup"><span data-stu-id="2eaf5-315">Hit breakpoints IDs</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-316">asyncStackTrace</span><span class="sxs-lookup"><span data-stu-id="2eaf5-316">asyncStackTrace</span></span> <br/> <i><span data-ttu-id="2eaf5-317">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-317">optional</span></span></i></td>
            <td><!--  <a href="#stacktrace">  --><code class="flyout">StackTrace</code><!--  </a>  --></td>
            <td><span data-ttu-id="2eaf5-318">Rastreamento de pilha assíncrono JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-318">JavaScript async stack trace.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="2eaf5-319">retomado</span><span class="sxs-lookup"><span data-stu-id="2eaf5-319">resumed</span></span>
<span data-ttu-id="2eaf5-320">Acionado quando o depurador retomar a execução.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-320">Fired when the debugger resumes execution.</span></span>

</p>

---

## <span data-ttu-id="2eaf5-321">Tipos</span><span class="sxs-lookup"><span data-stu-id="2eaf5-321">Types</span></span>

### <a name="breakpointid"></a> <span data-ttu-id="2eaf5-322">Breakpointid</span><span class="sxs-lookup"><span data-stu-id="2eaf5-322">BreakpointId</span></span> `string`

<span data-ttu-id="2eaf5-323">Identificador de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-323">Breakpoint identifier.</span></span>

</p>

---

### <a name="callframeid"></a> <span data-ttu-id="2eaf5-324">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="2eaf5-324">CallFrameId</span></span> `string`

<span data-ttu-id="2eaf5-325">Identificador de quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-325">Call frame identifier.</span></span>

</p>

---

### <a name="location"></a> <span data-ttu-id="2eaf5-326">Location</span><span class="sxs-lookup"><span data-stu-id="2eaf5-326">Location</span></span> `object`

<span data-ttu-id="2eaf5-327">Local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-327">Location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-328">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2eaf5-328">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-329">scriptid</span><span class="sxs-lookup"><span data-stu-id="2eaf5-329">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="2eaf5-330">Identificador de script reportado no <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="2eaf5-330">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-331">lineNumber</span><span class="sxs-lookup"><span data-stu-id="2eaf5-331">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2eaf5-332">Número da linha no script (baseado em 0).</span><span class="sxs-lookup"><span data-stu-id="2eaf5-332">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-333">columnNumber</span><span class="sxs-lookup"><span data-stu-id="2eaf5-333">columnNumber</span></span> <br/> <i><span data-ttu-id="2eaf5-334">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-334">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2eaf5-335">Número da coluna no script (baseado em 0).</span><span class="sxs-lookup"><span data-stu-id="2eaf5-335">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-336">msLength</span><span class="sxs-lookup"><span data-stu-id="2eaf5-336">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2eaf5-337">Microsoft: comprimento do código (ou seja, número de caracteres) nesse quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-337">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="breaklocation"></a> <span data-ttu-id="2eaf5-338">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="2eaf5-338">BreakLocation</span></span> `object`

<span data-ttu-id="2eaf5-339">Interrompa o local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-339">Break location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-340">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2eaf5-340">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-341">scriptid</span><span class="sxs-lookup"><span data-stu-id="2eaf5-341">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="2eaf5-342">Identificador de script reportado no <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="2eaf5-342">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-343">lineNumber</span><span class="sxs-lookup"><span data-stu-id="2eaf5-343">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2eaf5-344">Número da linha no script (baseado em 0).</span><span class="sxs-lookup"><span data-stu-id="2eaf5-344">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-345">columnNumber</span><span class="sxs-lookup"><span data-stu-id="2eaf5-345">columnNumber</span></span> <br/> <i><span data-ttu-id="2eaf5-346">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-346">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2eaf5-347">Número da coluna no script (baseado em 0).</span><span class="sxs-lookup"><span data-stu-id="2eaf5-347">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-348">msLength</span><span class="sxs-lookup"><span data-stu-id="2eaf5-348">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="2eaf5-349">Microsoft: comprimento do código (ou seja, número de caracteres) nesse quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-349">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-350">tipo</span><span class="sxs-lookup"><span data-stu-id="2eaf5-350">type</span></span> <br/> <i><span data-ttu-id="2eaf5-351">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-351">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2eaf5-352">Valores permitidos: debuggerStatement, Call, Return.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-352">Allowed values: debuggerStatement, call, return.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callframe"></a> <span data-ttu-id="2eaf5-353">CallFrame</span><span class="sxs-lookup"><span data-stu-id="2eaf5-353">CallFrame</span></span> `object`

<span data-ttu-id="2eaf5-354">Quadro de chamada JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-354">JavaScript call frame.</span></span> <span data-ttu-id="2eaf5-355">Matriz de quadros de chamadas formam a pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-355">Array of call frames form the call stack.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-356">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2eaf5-356">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-357">callFrameId</span><span class="sxs-lookup"><span data-stu-id="2eaf5-357">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="2eaf5-358">Identificador de quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-358">Call frame identifier.</span></span> <span data-ttu-id="2eaf5-359">Esse identificador só é válido enquanto o depurador está pausado.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-359">This identifier is only valid while the debugger is paused.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-360">função FunctionName</span><span class="sxs-lookup"><span data-stu-id="2eaf5-360">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2eaf5-361">Nome da função JavaScript chamada neste quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-361">Name of the JavaScript function called on this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-362">functionLocation</span><span class="sxs-lookup"><span data-stu-id="2eaf5-362">functionLocation</span></span> <br/> <i><span data-ttu-id="2eaf5-363">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-363">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b><span data-ttu-id="2eaf5-364">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-364">Experimental.</span></span> </b></span><span data-ttu-id="2eaf5-365">Local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-365">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-366">ponto</span><span class="sxs-lookup"><span data-stu-id="2eaf5-366">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="2eaf5-367">Local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-367">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-368">url</span><span class="sxs-lookup"><span data-stu-id="2eaf5-368">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="2eaf5-369">Nome ou URL do script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-369">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-370">scopeChain</span><span class="sxs-lookup"><span data-stu-id="2eaf5-370">scopeChain</span></span></td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td><span data-ttu-id="2eaf5-371">Cadeia de escopos para este quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-371">Scope chain for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-372">deste</span><span class="sxs-lookup"><span data-stu-id="2eaf5-372">this</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> <span data-ttu-id="2eaf5-373">objeto para este quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-373">object for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-374">returnValue</span><span class="sxs-lookup"><span data-stu-id="2eaf5-374">returnValue</span></span> <br/> <i><span data-ttu-id="2eaf5-375">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-375">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="2eaf5-376">O valor que está sendo retornado, se a função estiver em um ponto de retorno.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-376">The value being returned, if the function is at return point.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="scope"></a> <span data-ttu-id="2eaf5-377">Escopo</span><span class="sxs-lookup"><span data-stu-id="2eaf5-377">Scope</span></span> `object`

<span data-ttu-id="2eaf5-378">Descrição do escopo.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-378">Scope description.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="2eaf5-379">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2eaf5-379">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="2eaf5-380">tipo</span><span class="sxs-lookup"><span data-stu-id="2eaf5-380">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="2eaf5-381">Valores permitidos: global, local, com, fechamento, catch, Block, script, eval, Module, Return</span><span class="sxs-lookup"><span data-stu-id="2eaf5-381">Allowed values: global, local, with, closure, catch, block, script, eval, module, return</span></span></i></td>
            <td><span data-ttu-id="2eaf5-382">Tipo de escopo.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-382">Scope type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-383">object</span><span class="sxs-lookup"><span data-stu-id="2eaf5-383">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="2eaf5-384">Objeto que representa o escopo.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-384">Object representing the scope.</span></span> <span data-ttu-id="2eaf5-385">Para <code>global</code> e <code>with</code> escopos, ele representa o objeto real; para o restante dos escopos, é um objeto transitório artificial enumerando variáveis de escopo como suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2eaf5-385">For <code>global</code> and <code>with</code> scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-386">name</span><span class="sxs-lookup"><span data-stu-id="2eaf5-386">name</span></span> <br/> <i><span data-ttu-id="2eaf5-387">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-387">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-388">startLocation</span><span class="sxs-lookup"><span data-stu-id="2eaf5-388">startLocation</span></span> <br/> <i><span data-ttu-id="2eaf5-389">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-389">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="2eaf5-390">Local no código-fonte onde o escopo é iniciado</span><span class="sxs-lookup"><span data-stu-id="2eaf5-390">Location in the source code where scope starts</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="2eaf5-391">EndLocation</span><span class="sxs-lookup"><span data-stu-id="2eaf5-391">endLocation</span></span> <br/> <i><span data-ttu-id="2eaf5-392">opcional</span><span class="sxs-lookup"><span data-stu-id="2eaf5-392">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="2eaf5-393">Local no código-fonte em que termina o escopo</span><span class="sxs-lookup"><span data-stu-id="2eaf5-393">Location in the source code where scope ends</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="2eaf5-394">Dependências</span><span class="sxs-lookup"><span data-stu-id="2eaf5-394">Dependencies</span></span>

[<span data-ttu-id="2eaf5-395">Classpath</span><span class="sxs-lookup"><span data-stu-id="2eaf5-395">Runtime</span></span>](runtime.md)
