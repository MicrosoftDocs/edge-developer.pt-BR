---
description: Referência do Protocolo DevTools Versão 0.2 (EdgeHTML) para o Domínio de Depurador. O domínio depurador expõe os recursos de depuração do JavaScript. Ele permite definir e remover pontos de interrupção, passar pela execução, explorar rastreamentos de pilha, etc.
title: Domínio de depurador - DevTools Protocol Versão 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 00c410812edd4d11e9904a489955e7fd218a7e5d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398172"
---
# <a name="debugger-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="faf81-105">Domínio de depurador - DevTools Protocol Versão 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="faf81-105">Debugger Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="faf81-106">O domínio depurador expõe os recursos de depuração do JavaScript.</span><span class="sxs-lookup"><span data-stu-id="faf81-106">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="faf81-107">Ele permite definir e remover pontos de interrupção, passar pela execução, explorar rastreamentos de pilha, etc.</span><span class="sxs-lookup"><span data-stu-id="faf81-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| <span data-ttu-id="faf81-108">Classificação</span><span class="sxs-lookup"><span data-stu-id="faf81-108">Classification</span></span> | <span data-ttu-id="faf81-109">Membros</span><span class="sxs-lookup"><span data-stu-id="faf81-109">Members</span></span> |  
|:--- |:--- |  
| [**<span data-ttu-id="faf81-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="faf81-110">Methods</span></span>**](#methods) | <span data-ttu-id="faf81-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="faf81-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |  
| [**<span data-ttu-id="faf81-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="faf81-112">Events</span></span>**](#events) | <span data-ttu-id="faf81-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span><span class="sxs-lookup"><span data-stu-id="faf81-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |  
| [**<span data-ttu-id="faf81-114">Tipos</span><span class="sxs-lookup"><span data-stu-id="faf81-114">Types</span></span>**](#types) | <span data-ttu-id="faf81-115">[BreakpointId,](#breakpointid) [CallFrameId,](#callframeid) [Location,](#location) [BreakLocation,](#breaklocation) [CallFrame,](#callframe) [Scope](#scope)</span><span class="sxs-lookup"><span data-stu-id="faf81-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |  
| [**<span data-ttu-id="faf81-116">Dependências</span><span class="sxs-lookup"><span data-stu-id="faf81-116">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="faf81-117">Tempo de Execução</span><span class="sxs-lookup"><span data-stu-id="faf81-117">Runtime</span></span>](./runtime.md) |  

## <a name="methods"></a><span data-ttu-id="faf81-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="faf81-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="faf81-119">Habilitar</span><span class="sxs-lookup"><span data-stu-id="faf81-119">enable</span></span>  

<span data-ttu-id="faf81-120">Habilita o depurador para a página determinada.</span><span class="sxs-lookup"><span data-stu-id="faf81-120">Enables debugger for the given page.</span></span> <span data-ttu-id="faf81-121">Os clientes não devem presumir que a depuração foi habilitada até que o resultado desse comando seja recebido.</span><span class="sxs-lookup"><span data-stu-id="faf81-121">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="faf81-122">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="faf81-122">disable</span></span>  

<span data-ttu-id="faf81-123">Desabilita o depurador para determinada página.</span><span class="sxs-lookup"><span data-stu-id="faf81-123">Disables debugger for given page.</span></span>  

&nbsp;  

---  

### <a name="getpossiblebreakpoints"></a><span data-ttu-id="faf81-124">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="faf81-124">getPossibleBreakpoints</span></span>  

<span data-ttu-id="faf81-125">Retorna possíveis locais para ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="faf81-125">Returns possible locations for breakpoint.</span></span> <span data-ttu-id="faf81-126">scriptId em locais de intervalo inicial e final deve ser o mesmo.</span><span class="sxs-lookup"><span data-stu-id="faf81-126">scriptId in start and end range locations should be the same.</span></span>  

| <span data-ttu-id="faf81-127">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf81-127">Parameters</span></span> | <span data-ttu-id="faf81-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-128">Type</span></span> | <span data-ttu-id="faf81-129">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-129">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-130">start</span><span class="sxs-lookup"><span data-stu-id="faf81-130">start</span></span> | [<span data-ttu-id="faf81-131">Location</span><span class="sxs-lookup"><span data-stu-id="faf81-131">Location</span></span>](#location) | <span data-ttu-id="faf81-132">Início do intervalo para pesquisar possíveis locais de ponto de interrupção em.</span><span class="sxs-lookup"><span data-stu-id="faf81-132">Start of range to search possible breakpoint locations in.</span></span> |  
| <span data-ttu-id="faf81-133">encerrar</span><span class="sxs-lookup"><span data-stu-id="faf81-133">end</span></span> | [<span data-ttu-id="faf81-134">Location</span><span class="sxs-lookup"><span data-stu-id="faf81-134">Location</span></span>](#location) | <span data-ttu-id="faf81-135">Fim do intervalo para pesquisar possíveis locais de ponto de interrupção em \(excludendo\).</span><span class="sxs-lookup"><span data-stu-id="faf81-135">End of range to search possible breakpoint locations in \(excluding\).</span></span>  <span data-ttu-id="faf81-136">Quando não especificado, o fim dos scripts é usado como fim do intervalo.</span><span class="sxs-lookup"><span data-stu-id="faf81-136">When not specified, end of scripts is used as end of range.</span></span> |  

| <span data-ttu-id="faf81-137">Retorna</span><span class="sxs-lookup"><span data-stu-id="faf81-137">Returns</span></span> | <span data-ttu-id="faf81-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-138">Type</span></span> | <span data-ttu-id="faf81-139">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-139">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-140">locations</span><span class="sxs-lookup"><span data-stu-id="faf81-140">locations</span></span> | [<span data-ttu-id="faf81-141">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="faf81-141">BreakLocation</span></span>](#breaklocation) | <span data-ttu-id="faf81-142">Lista dos possíveis locais de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="faf81-142">List of the possible breakpoint locations.</span></span> |  

---  

### <a name="setbreakpointsactive"></a><span data-ttu-id="faf81-143">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="faf81-143">setBreakpointsActive</span></span>  

<span data-ttu-id="faf81-144">Ativa/desativa todos os pontos de interrupção na página.</span><span class="sxs-lookup"><span data-stu-id="faf81-144">Activates / deactivates all breakpoints on the page.</span></span>  

| <span data-ttu-id="faf81-145">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf81-145">Parameters</span></span> | <span data-ttu-id="faf81-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-146">Type</span></span> | <span data-ttu-id="faf81-147">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-147">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-148">active</span><span class="sxs-lookup"><span data-stu-id="faf81-148">active</span></span> | `boolean` | <span data-ttu-id="faf81-149">Novo valor para o estado ativo de pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="faf81-149">New value for breakpoints active state.</span></span> | 

---  

### <a name="setbreakpointbyurl"></a><span data-ttu-id="faf81-150">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="faf81-150">setBreakpointByUrl</span></span>  

<span data-ttu-id="faf81-151">Define o ponto de interrupção JavaScript em determinado local especificado por URL ou URL regex.</span><span class="sxs-lookup"><span data-stu-id="faf81-151">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span>  <span data-ttu-id="faf81-152">Depois que esse comando for emitido, todos os scripts analisados existentes terão pontos de interrupção resolvidos e retornados na `locations` propriedade.</span><span class="sxs-lookup"><span data-stu-id="faf81-152">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in `locations` property.</span></span>  <span data-ttu-id="faf81-153">A análise de scripts correspondentes posteriores resultará em eventos `breakpointResolved` subsequentes emitidos.</span><span class="sxs-lookup"><span data-stu-id="faf81-153">Further matching script parsing will result in subsequent `breakpointResolved` events issued.</span></span>  <span data-ttu-id="faf81-154">Esse ponto de interrupção lógico sobreviverá a recarregações de página.</span><span class="sxs-lookup"><span data-stu-id="faf81-154">This logical breakpoint will survive page reloads.</span></span>  

| <span data-ttu-id="faf81-155">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf81-155">Parameters</span></span> | <span data-ttu-id="faf81-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-156">Type</span></span> | <span data-ttu-id="faf81-157">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-157">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-158">lineNumber</span><span class="sxs-lookup"><span data-stu-id="faf81-158">lineNumber</span></span> | `integer` | <span data-ttu-id="faf81-159">Número da linha para definir ponto de interrupção em.</span><span class="sxs-lookup"><span data-stu-id="faf81-159">Line number to set breakpoint at.</span></span> | 
| <span data-ttu-id="faf81-160">url \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-160">url \(optional\)</span></span> | `string` | <span data-ttu-id="faf81-161">URL dos recursos para definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="faf81-161">URL of the resources to set breakpoint on.</span></span> |  
| <span data-ttu-id="faf81-162">urlRegex \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-162">urlRegex \(optional\)</span></span> | `string` | <span data-ttu-id="faf81-163">Padrão regex para as URLs dos recursos para definir pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="faf81-163">Regex pattern for the URLs of the resources to set breakpoints on.</span></span>  <span data-ttu-id="faf81-164">Ou `url` `urlRegex` deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="faf81-164">Either `url` or `urlRegex` must be specified.</span></span> |  
| <span data-ttu-id="faf81-165">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-165">columnNumber \(optional\)</span></span> | `integer` | <span data-ttu-id="faf81-166">Deslocamento na linha para definir ponto de interrupção em.</span><span class="sxs-lookup"><span data-stu-id="faf81-166">Offset in the line to set breakpoint at.</span></span> |  
| <span data-ttu-id="faf81-167">condição \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-167">condition \(optional\)</span></span> | `string` | <span data-ttu-id="faf81-168">Expressão a ser usada como uma condição de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="faf81-168">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="faf81-169">Quando especificado, o depurador só será parar no ponto de interrupção se essa expressão for avaliada como true.</span><span class="sxs-lookup"><span data-stu-id="faf81-169">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="faf81-170">Retorna</span><span class="sxs-lookup"><span data-stu-id="faf81-170">Returns</span></span> | <span data-ttu-id="faf81-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-171">Type</span></span> | <span data-ttu-id="faf81-172">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-172">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-173">breakpointId</span><span class="sxs-lookup"><span data-stu-id="faf81-173">breakpointId</span></span> | [<span data-ttu-id="faf81-174">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="faf81-174">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="faf81-175">ID do ponto de interrupção criado para referência posterior.</span><span class="sxs-lookup"><span data-stu-id="faf81-175">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="faf81-176">locations</span><span class="sxs-lookup"><span data-stu-id="faf81-176">locations</span></span> | [<span data-ttu-id="faf81-177">Local[]</span><span class="sxs-lookup"><span data-stu-id="faf81-177">Location[]</span></span>](#location) | <span data-ttu-id="faf81-178">Lista dos locais em que esse ponto de interrupção foi resolvido após a adição.</span><span class="sxs-lookup"><span data-stu-id="faf81-178">List of the locations this breakpoint resolved into upon addition.</span></span> |  

---  

### <a name="setbreakpoint"></a><span data-ttu-id="faf81-179">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="faf81-179">setBreakpoint</span></span>  

<span data-ttu-id="faf81-180">Define o ponto de interrupção JavaScript em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="faf81-180">Sets JavaScript breakpoint at a given location.</span></span>  

| <span data-ttu-id="faf81-181">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf81-181">Parameters</span></span> | <span data-ttu-id="faf81-182">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-182">Type</span></span> | <span data-ttu-id="faf81-183">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-183">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-184">location</span><span class="sxs-lookup"><span data-stu-id="faf81-184">location</span></span> | [<span data-ttu-id="faf81-185">Location</span><span class="sxs-lookup"><span data-stu-id="faf81-185">Location</span></span>](#location) | <span data-ttu-id="faf81-186">Local para definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="faf81-186">Location to set breakpoint in.</span></span> |  
| <span data-ttu-id="faf81-187">condição \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-187">condition \(optional\)</span></span> | `string` | <span data-ttu-id="faf81-188">Expressão a ser usada como uma condição de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="faf81-188">Expression to use as a breakpoint condition.</span></span>  <span data-ttu-id="faf81-189">Quando especificado, o depurador só será parar no ponto de interrupção se essa expressão for avaliada como true.</span><span class="sxs-lookup"><span data-stu-id="faf81-189">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="faf81-190">Retorna</span><span class="sxs-lookup"><span data-stu-id="faf81-190">Returns</span></span> | <span data-ttu-id="faf81-191">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-191">Type</span></span> | <span data-ttu-id="faf81-192">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-192">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-193">breakpointId</span><span class="sxs-lookup"><span data-stu-id="faf81-193">breakpointId</span></span> | [<span data-ttu-id="faf81-194">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="faf81-194">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="faf81-195">ID do ponto de interrupção criado para referência posterior.</span><span class="sxs-lookup"><span data-stu-id="faf81-195">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="faf81-196">actualLocation</span><span class="sxs-lookup"><span data-stu-id="faf81-196">actualLocation</span></span> | [<span data-ttu-id="faf81-197">Location</span><span class="sxs-lookup"><span data-stu-id="faf81-197">Location</span></span>](#location) | <span data-ttu-id="faf81-198">Local em que o ponto de interrupção foi resolvido.</span><span class="sxs-lookup"><span data-stu-id="faf81-198">Location this breakpoint resolved into.</span></span> |  

---  

### <a name="removebreakpoint"></a><span data-ttu-id="faf81-199">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="faf81-199">removeBreakpoint</span></span>  

<span data-ttu-id="faf81-200">Remove o ponto de interrupção JavaScript.</span><span class="sxs-lookup"><span data-stu-id="faf81-200">Removes JavaScript breakpoint.</span></span>  

| <span data-ttu-id="faf81-201">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf81-201">Parameters</span></span> | <span data-ttu-id="faf81-202">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-202">Type</span></span> | <span data-ttu-id="faf81-203">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-203">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-204">breakpointId</span><span class="sxs-lookup"><span data-stu-id="faf81-204">breakpointId</span></span> | [<span data-ttu-id="faf81-205">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="faf81-205">BreakpointId</span></span>](#breakpointid) | &nbsp; |  

---  

### <a name="stepover"></a><span data-ttu-id="faf81-206">stepOver</span><span class="sxs-lookup"><span data-stu-id="faf81-206">stepOver</span></span>  

<span data-ttu-id="faf81-207">Etapas sobre a instrução.</span><span class="sxs-lookup"><span data-stu-id="faf81-207">Steps over the statement.</span></span>  

&nbsp;  

---  

### <a name="stepinto"></a><span data-ttu-id="faf81-208">stepInto</span><span class="sxs-lookup"><span data-stu-id="faf81-208">stepInto</span></span>  

<span data-ttu-id="faf81-209">Etapas na chamada de função.</span><span class="sxs-lookup"><span data-stu-id="faf81-209">Steps into the function call.</span></span>  

&nbsp;  

---  

### <a name="stepout"></a><span data-ttu-id="faf81-210">stepOut</span><span class="sxs-lookup"><span data-stu-id="faf81-210">stepOut</span></span>  

<span data-ttu-id="faf81-211">Sai da chamada de função.</span><span class="sxs-lookup"><span data-stu-id="faf81-211">Steps out of the function call.</span></span>  

&nbsp;  

---  

### <a name="pause"></a><span data-ttu-id="faf81-212">pause</span><span class="sxs-lookup"><span data-stu-id="faf81-212">pause</span></span>  

<span data-ttu-id="faf81-213">Para na próxima instrução JavaScript.</span><span class="sxs-lookup"><span data-stu-id="faf81-213">Stops on the next JavaScript statement.</span></span>  

&nbsp;  

---  

### <a name="resume"></a><span data-ttu-id="faf81-214">resume</span><span class="sxs-lookup"><span data-stu-id="faf81-214">resume</span></span>  

<span data-ttu-id="faf81-215">Retoma a execução do JavaScript.</span><span class="sxs-lookup"><span data-stu-id="faf81-215">Resumes JavaScript execution.</span></span>  

&nbsp;  

---  

### <a name="getscriptsource"></a><span data-ttu-id="faf81-216">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="faf81-216">getScriptSource</span></span>  

<span data-ttu-id="faf81-217">Retorna a origem do script com a ID determinada.</span><span class="sxs-lookup"><span data-stu-id="faf81-217">Returns source for the script with given id.</span></span>  

| <span data-ttu-id="faf81-218">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf81-218">Parameters</span></span> | <span data-ttu-id="faf81-219">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-219">Type</span></span> | <span data-ttu-id="faf81-220">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-220">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-221">scriptId</span><span class="sxs-lookup"><span data-stu-id="faf81-221">scriptId</span></span> | [<span data-ttu-id="faf81-222">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="faf81-222">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="faf81-223">ID do script para o que obter a origem.</span><span class="sxs-lookup"><span data-stu-id="faf81-223">ID of the script to get source for.</span></span> |  

| <span data-ttu-id="faf81-224">Retorna</span><span class="sxs-lookup"><span data-stu-id="faf81-224">Returns</span></span> | <span data-ttu-id="faf81-225">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-225">Type</span></span> | <span data-ttu-id="faf81-226">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-226">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-227">scriptSource</span><span class="sxs-lookup"><span data-stu-id="faf81-227">scriptSource</span></span> | `string` | <span data-ttu-id="faf81-228">Origem do script.</span><span class="sxs-lookup"><span data-stu-id="faf81-228">Script source.</span></span> | 

---  

### <a name="setpauseonexceptions"></a><span data-ttu-id="faf81-229">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="faf81-229">setPauseOnExceptions</span></span>  

<span data-ttu-id="faf81-230">Define pausa no estado de exceções.</span><span class="sxs-lookup"><span data-stu-id="faf81-230">Defines pause on exceptions state.</span></span>  <span data-ttu-id="faf81-231">Pode ser definido para parar em todas as exceções, exceções não ativas ou nenhuma exceção.</span><span class="sxs-lookup"><span data-stu-id="faf81-231">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span>  <span data-ttu-id="faf81-232">A pausa inicial no estado de exceções é `none` .</span><span class="sxs-lookup"><span data-stu-id="faf81-232">Initial pause on exceptions state is `none`.</span></span>  

| <span data-ttu-id="faf81-233">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf81-233">Parameters</span></span> | <span data-ttu-id="faf81-234">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-234">Type</span></span> | <span data-ttu-id="faf81-235">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-235">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-236">state</span><span class="sxs-lookup"><span data-stu-id="faf81-236">state</span></span> | `string` | <span data-ttu-id="faf81-237">Pause no modo de exceções.</span><span class="sxs-lookup"><span data-stu-id="faf81-237">Pause on exceptions mode.</span></span>  <span data-ttu-id="faf81-238">Valores permitidos:  `none` , `uncaught` ,</span><span class="sxs-lookup"><span data-stu-id="faf81-238">Allowed values:  `none`, `uncaught`,</span></span> `all` |  

---  

### <a name="evaluateoncallframe"></a><span data-ttu-id="faf81-239">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="faf81-239">evaluateOnCallFrame</span></span>  

<span data-ttu-id="faf81-240">Avalia a expressão em um determinado quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="faf81-240">Evaluates expression on a given call frame.</span></span>  

| <span data-ttu-id="faf81-241">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf81-241">Parameters</span></span> | <span data-ttu-id="faf81-242">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-242">Type</span></span> | <span data-ttu-id="faf81-243">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-243">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-244">callFrameId</span><span class="sxs-lookup"><span data-stu-id="faf81-244">callFrameId</span></span> | [<span data-ttu-id="faf81-245">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="faf81-245">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="faf81-246">Identificador de quadro de chamada a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="faf81-246">Call frame identifier to evaluate on.</span></span> |  
| <span data-ttu-id="faf81-247">expressão</span><span class="sxs-lookup"><span data-stu-id="faf81-247">expression</span></span> | `string` | <span data-ttu-id="faf81-248">Expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="faf81-248">Expression to evaluate.</span></span> | 

| <span data-ttu-id="faf81-249">Retorna</span><span class="sxs-lookup"><span data-stu-id="faf81-249">Returns</span></span> | <span data-ttu-id="faf81-250">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-250">Type</span></span> | <span data-ttu-id="faf81-251">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-251">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-252">result</span><span class="sxs-lookup"><span data-stu-id="faf81-252">result</span></span> | [<span data-ttu-id="faf81-253">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="faf81-253">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="faf81-254">Wrapper do objeto para o resultado da avaliação.</span><span class="sxs-lookup"><span data-stu-id="faf81-254">Object wrapper for the evaluation result.</span></span> |  

---  

### <a name="setvariablevalue"></a><span data-ttu-id="faf81-255">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="faf81-255">setVariableValue</span></span>  

<span data-ttu-id="faf81-256">Altera o valor da variável em um callframe.</span><span class="sxs-lookup"><span data-stu-id="faf81-256">Changes value of variable in a callframe.</span></span>  <span data-ttu-id="faf81-257">Os escopos baseados em objeto não têm suporte e devem ser transformados manualmente.</span><span class="sxs-lookup"><span data-stu-id="faf81-257">Object-based scopes are not supported and must be mutated manually.</span></span>  

| <span data-ttu-id="faf81-258">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf81-258">Parameters</span></span> | <span data-ttu-id="faf81-259">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-259">Type</span></span> | <span data-ttu-id="faf81-260">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-260">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-261">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="faf81-261">scopeNumber</span></span> | `integer` | <span data-ttu-id="faf81-262">Número baseado em 0 do escopo conforme listado na cadeia de escopo.</span><span class="sxs-lookup"><span data-stu-id="faf81-262">0-based number of scope as was listed in scope chain.</span></span>  <span data-ttu-id="faf81-263">Somente `local` , e os tipos de escopo são `closure` `catch` permitidos.</span><span class="sxs-lookup"><span data-stu-id="faf81-263">Only `local`, `closure`, and `catch` scope types are allowed.</span></span>  <span data-ttu-id="faf81-264">Outros escopos podem ser manipulados manualmente.</span><span class="sxs-lookup"><span data-stu-id="faf81-264">Other scopes could be manipulated manually.</span></span> | 
| <span data-ttu-id="faf81-265">variableName</span><span class="sxs-lookup"><span data-stu-id="faf81-265">variableName</span></span> | `string` | <span data-ttu-id="faf81-266">Nome da variável.</span><span class="sxs-lookup"><span data-stu-id="faf81-266">Variable name.</span></span> | 
| <span data-ttu-id="faf81-267">newValue</span><span class="sxs-lookup"><span data-stu-id="faf81-267">newValue</span></span> | [<span data-ttu-id="faf81-268">Runtime.CallArgument</span><span class="sxs-lookup"><span data-stu-id="faf81-268">Runtime.CallArgument</span></span>](./runtime.md#callargument) | <span data-ttu-id="faf81-269">Novo valor variável.</span><span class="sxs-lookup"><span data-stu-id="faf81-269">New variable value.</span></span> |  
| <span data-ttu-id="faf81-270">callFrameId</span><span class="sxs-lookup"><span data-stu-id="faf81-270">callFrameId</span></span> | [<span data-ttu-id="faf81-271">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="faf81-271">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="faf81-272">ID do callframe que contém variável.</span><span class="sxs-lookup"><span data-stu-id="faf81-272">ID of callframe that holds variable.</span></span> |  

---  

### <a name="setblackboxpatterns"></a><span data-ttu-id="faf81-273">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="faf81-273">setBlackboxPatterns</span></span>  

<span data-ttu-id="faf81-274">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="faf81-274">**Experimental**.</span></span>  <span data-ttu-id="faf81-275">Substitua padrões de caixa preta anteriores por aqueles passados.</span><span class="sxs-lookup"><span data-stu-id="faf81-275">Replace previous blackbox patterns with passed ones.</span></span>  <span data-ttu-id="faf81-276">Força o back-end a ignorar a revisão/pausa em scripts com a URL correspondente a um dos padrões.</span><span class="sxs-lookup"><span data-stu-id="faf81-276">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span>  <span data-ttu-id="faf81-277">O depurador tentará deixar o script em blackbox executando 'step in' várias vezes, finalmente recorrendo a "sair" se não tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="faf81-277">The debugger will try to leave blackboxed script by performing 'step in' several times, finally resorting to 'step out' if unsuccessful.</span></span>  


| <span data-ttu-id="faf81-278">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf81-278">Parameters</span></span> | <span data-ttu-id="faf81-279">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-279">Type</span></span> | <span data-ttu-id="faf81-280">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-280">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-281">patterns</span><span class="sxs-lookup"><span data-stu-id="faf81-281">patterns</span></span> | `string[]` | <span data-ttu-id="faf81-282">Matriz de regexps que será usada para verificar a URL do script para o estado de blackbox.</span><span class="sxs-lookup"><span data-stu-id="faf81-282">Array of regexps that will be used to check script url for blackbox state.</span></span> | 

---  

### <a name="mssetdebuggerpropertyvalue"></a><span data-ttu-id="faf81-283">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="faf81-283">msSetDebuggerPropertyValue</span></span>  

<span data-ttu-id="faf81-284">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="faf81-284">**Experimental**.</span></span>  <span data-ttu-id="faf81-285">Microsoft: define a propriedade depurador especificada como o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="faf81-285">Microsoft: Sets the specified debugger property to the specified value.</span></span>  

| <span data-ttu-id="faf81-286">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf81-286">Parameters</span></span> | <span data-ttu-id="faf81-287">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-287">Type</span></span> | <span data-ttu-id="faf81-288">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-288">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-289">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="faf81-289">debuggerPropertyId</span></span> | <span data-ttu-id="faf81-290">string</span><span class="sxs-lookup"><span data-stu-id="faf81-290">string</span></span> | <span data-ttu-id="faf81-291">Microsoft: a id da propriedade \(ou `msDebuggerPropertyId` seja, \) a ser definida.</span><span class="sxs-lookup"><span data-stu-id="faf81-291">Microsoft:  The property id \(i.e. `msDebuggerPropertyId`\) to set.</span></span> | 
| <span data-ttu-id="faf81-292">newValue</span><span class="sxs-lookup"><span data-stu-id="faf81-292">newValue</span></span> | `string` | &nbsp; |  

---  

## <a name="events"></a><span data-ttu-id="faf81-293">Eventos</span><span class="sxs-lookup"><span data-stu-id="faf81-293">Events</span></span>  

### <a name="scriptparsed"></a><span data-ttu-id="faf81-294">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="faf81-294">scriptParsed</span></span>  

<span data-ttu-id="faf81-295">Disparado quando o script é analisado.</span><span class="sxs-lookup"><span data-stu-id="faf81-295">Fired when the script is parsed.</span></span> <span data-ttu-id="faf81-296">Esse evento também é acionado para todos os scripts conhecidos e não recolhidos ao habilitar o depurador.</span><span class="sxs-lookup"><span data-stu-id="faf81-296">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>  

| <span data-ttu-id="faf81-297">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf81-297">Parameters</span></span> | <span data-ttu-id="faf81-298">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-298">Type</span></span> | <span data-ttu-id="faf81-299">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-299">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-300">scriptId</span><span class="sxs-lookup"><span data-stu-id="faf81-300">scriptId</span></span> | [<span data-ttu-id="faf81-301">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="faf81-301">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="faf81-302">Identificador do script analisado.</span><span class="sxs-lookup"><span data-stu-id="faf81-302">Identifier of the script parsed.</span></span> |  
| <span data-ttu-id="faf81-303">url</span><span class="sxs-lookup"><span data-stu-id="faf81-303">url</span></span> | `string` | <span data-ttu-id="faf81-304">URL ou nome do script analisado \(se tiver\).</span><span class="sxs-lookup"><span data-stu-id="faf81-304">URL or name of the script parsed \(if any\).</span></span> | 
| <span data-ttu-id="faf81-305">startLine</span><span class="sxs-lookup"><span data-stu-id="faf81-305">startLine</span></span> | `integer` | <span data-ttu-id="faf81-306">Deslocamento de linha do script dentro do recurso com a URL determinada \(para marcas de script\).</span><span class="sxs-lookup"><span data-stu-id="faf81-306">Line offset of the script within the resource with given URL \(for script tags\).</span></span> | 
| <span data-ttu-id="faf81-307">startColumn</span><span class="sxs-lookup"><span data-stu-id="faf81-307">startColumn</span></span> | `integer` | <span data-ttu-id="faf81-308">Deslocamento de coluna do script dentro do recurso com a URL determinada.</span><span class="sxs-lookup"><span data-stu-id="faf81-308">Column offset of the script within the resource with given URL.</span></span> | 
| <span data-ttu-id="faf81-309">endLine</span><span class="sxs-lookup"><span data-stu-id="faf81-309">endLine</span></span> | `integer` | <span data-ttu-id="faf81-310">Última linha do script.</span><span class="sxs-lookup"><span data-stu-id="faf81-310">Last line of the script.</span></span> | 
| <span data-ttu-id="faf81-311">endColumn</span><span class="sxs-lookup"><span data-stu-id="faf81-311">endColumn</span></span> | `integer` | <span data-ttu-id="faf81-312">Comprimento da última linha do script.</span><span class="sxs-lookup"><span data-stu-id="faf81-312">Length of the last line of the script.</span></span> | 
| <span data-ttu-id="faf81-313">executionContextId</span><span class="sxs-lookup"><span data-stu-id="faf81-313">executionContextId</span></span> | [<span data-ttu-id="faf81-314">Runtime.ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="faf81-314">Runtime.ExecutionContextId</span></span>](./runtime.md#executioncontextid) | <span data-ttu-id="faf81-315">Especifica o contexto de criação de script.</span><span class="sxs-lookup"><span data-stu-id="faf81-315">Specifies script creation context.</span></span> |  
| <span data-ttu-id="faf81-316">sourceMapURL \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-316">sourceMapURL \(optional\)</span></span> | `string` | <span data-ttu-id="faf81-317">URL do mapa de origem associado ao script (se for o caso).</span><span class="sxs-lookup"><span data-stu-id="faf81-317">URL of source map associated with script (if any).</span></span> |  
| <span data-ttu-id="faf81-318">comprimento \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-318">length \(optional\)</span></span> | `integer` | <span data-ttu-id="faf81-319">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="faf81-319">**Experimental**.</span></span>  <span data-ttu-id="faf81-320">Este comprimento do script.</span><span class="sxs-lookup"><span data-stu-id="faf81-320">This script length.</span></span> |  
| <span data-ttu-id="faf81-321">msParentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-321">msParentId \(optional\)</span></span> | `string` | <span data-ttu-id="faf81-322">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="faf81-322">**Experimental**.</span></span>  <span data-ttu-id="faf81-323">Esta é a ID do documento pai.</span><span class="sxs-lookup"><span data-stu-id="faf81-323">This is the parent document ID.</span></span> |  
| <span data-ttu-id="faf81-324">msMimeType \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-324">msMimeType \(optional\)</span></span> | `string` | <span data-ttu-id="faf81-325">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="faf81-325">**Experimental**.</span></span>  <span data-ttu-id="faf81-326">Esse é o tipo de mime.</span><span class="sxs-lookup"><span data-stu-id="faf81-326">This is the mime type.</span></span> |  
| <span data-ttu-id="faf81-327">msIsDynamicCode \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-327">msIsDynamicCode \(optional\)</span></span> | `boolean` | <span data-ttu-id="faf81-328">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="faf81-328">**Experimental**.</span></span>  <span data-ttu-id="faf81-329">Isso indica se é um código dinâmico.</span><span class="sxs-lookup"><span data-stu-id="faf81-329">This indicates whether it is dynamic code.</span></span> |  
| <span data-ttu-id="faf81-330">msLongDocumentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-330">msLongDocumentId \(optional\)</span></span> | `integer` | <span data-ttu-id="faf81-331">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="faf81-331">**Experimental**.</span></span>  <span data-ttu-id="faf81-332">Esta é a ID do documento longa.</span><span class="sxs-lookup"><span data-stu-id="faf81-332">This is the long document ID.</span></span> |  

---  

### <a name="breakpointresolved"></a><span data-ttu-id="faf81-333">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="faf81-333">breakpointResolved</span></span>  

<span data-ttu-id="faf81-334">Acionado quando o ponto de interrupção é resolvido para um script e local reais.</span><span class="sxs-lookup"><span data-stu-id="faf81-334">Fired when breakpoint is resolved to an actual script and location.</span></span>  

| <span data-ttu-id="faf81-335">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf81-335">Parameters</span></span> | <span data-ttu-id="faf81-336">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-336">Type</span></span> | <span data-ttu-id="faf81-337">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-337">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-338">breakpointId</span><span class="sxs-lookup"><span data-stu-id="faf81-338">breakpointId</span></span> | [<span data-ttu-id="faf81-339">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="faf81-339">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="faf81-340">Identificador exclusivo do ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="faf81-340">Breakpoint unique identifier.</span></span> |  
| <span data-ttu-id="faf81-341">location</span><span class="sxs-lookup"><span data-stu-id="faf81-341">location</span></span> | [<span data-ttu-id="faf81-342">Location</span><span class="sxs-lookup"><span data-stu-id="faf81-342">Location</span></span>](#location) | <span data-ttu-id="faf81-343">Local real do ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="faf81-343">Actual breakpoint location.</span></span> |  
| <span data-ttu-id="faf81-344">msLength \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-344">msLength \(optional\)</span></span> | `integer` | <span data-ttu-id="faf81-345">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="faf81-345">**Experimental**.</span></span>  <span data-ttu-id="faf81-346">Microsoft: Comprimento do código \(ou seja, número de caracteres\) no local do ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="faf81-346">Microsoft:  Length of code \(i.e. number of characters\) at the breakpoint location.</span></span> |  

---  

### <a name="paused"></a><span data-ttu-id="faf81-347">pausado</span><span class="sxs-lookup"><span data-stu-id="faf81-347">paused</span></span>  

<span data-ttu-id="faf81-348">Acionado quando os depurador quebram para um ponto de interrupção ou exceção.</span><span class="sxs-lookup"><span data-stu-id="faf81-348">Fired when the debuggers breaks for a breakpoint or exception.</span></span>  

| <span data-ttu-id="faf81-349">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf81-349">Parameters</span></span> | <span data-ttu-id="faf81-350">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-350">Type</span></span> | <span data-ttu-id="faf81-351">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-351">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-352">callFrames</span><span class="sxs-lookup"><span data-stu-id="faf81-352">callFrames</span></span> | [<span data-ttu-id="faf81-353">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="faf81-353">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="faf81-354">Pilha de chamada em que o depurador parou.</span><span class="sxs-lookup"><span data-stu-id="faf81-354">Call stack the debugger stopped on.</span></span> |  
| <span data-ttu-id="faf81-355">reason</span><span class="sxs-lookup"><span data-stu-id="faf81-355">reason</span></span> | `string` |  <span data-ttu-id="faf81-356">Pause reason.</span><span class="sxs-lookup"><span data-stu-id="faf81-356">Pause reason.</span></span>  <span data-ttu-id="faf81-357">Valores permitidos:  `breakpoint` `step` , , , `exception` `other` e</span><span class="sxs-lookup"><span data-stu-id="faf81-357">Allowed values:  `breakpoint`, `step`, `exception`, `other`, and</span></span> `EventListener` |  
| <span data-ttu-id="faf81-358">data \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-358">data \(optional\)</span></span> | `object` | <span data-ttu-id="faf81-359">Objeto que contém propriedades auxiliares específicas de quebra.</span><span class="sxs-lookup"><span data-stu-id="faf81-359">Object containing break-specific auxiliary properties.</span></span> |  
| <span data-ttu-id="faf81-360">hitBreakpoints \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-360">hitBreakpoints \(optional\)</span></span> | `string[]` | <span data-ttu-id="faf81-361">Hit breakpoints IDs</span><span class="sxs-lookup"><span data-stu-id="faf81-361">Hit breakpoints IDs</span></span> |  
| <span data-ttu-id="faf81-362">asyncStackTrace \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-362">asyncStackTrace \(optional\)</span></span> | `StackTrace` | <span data-ttu-id="faf81-363">Rastreamento de pilha assíncrona javaScript.</span><span class="sxs-lookup"><span data-stu-id="faf81-363">JavaScript async stack trace.</span></span> |  

---  

### <a name="resumed"></a><span data-ttu-id="faf81-364">retomada</span><span class="sxs-lookup"><span data-stu-id="faf81-364">resumed</span></span>  

<span data-ttu-id="faf81-365">Acionado quando o depurador retoma a execução.</span><span class="sxs-lookup"><span data-stu-id="faf81-365">Fired when the debugger resumes execution.</span></span>  

&nbsp;  

---  

## <a name="types"></a><span data-ttu-id="faf81-366">Tipos</span><span class="sxs-lookup"><span data-stu-id="faf81-366">Types</span></span>  

### <a name="breakpointid-string"></a><span data-ttu-id="faf81-367">Cadeia de caracteres BreakpointId</span><span class="sxs-lookup"><span data-stu-id="faf81-367">BreakpointId string</span></span>  

<a name="breakpointid"></a>  

<span data-ttu-id="faf81-368">Identificador de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="faf81-368">Breakpoint identifier.</span></span>  

&nbsp;  

---  

### <a name="callframeid-string"></a><span data-ttu-id="faf81-369">Cadeia de caracteres CallFrameId</span><span class="sxs-lookup"><span data-stu-id="faf81-369">CallFrameId string</span></span>  

<a name="callframeid"></a>  

<span data-ttu-id="faf81-370">Identificador de quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="faf81-370">Call frame identifier.</span></span>  

&nbsp;  

---  

### <a name="location-object"></a><span data-ttu-id="faf81-371">Objeto Location</span><span class="sxs-lookup"><span data-stu-id="faf81-371">Location object</span></span>  

<a name="location"></a>  

<span data-ttu-id="faf81-372">Local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="faf81-372">Location in the source code.</span></span>  

| <span data-ttu-id="faf81-373">Propriedades</span><span class="sxs-lookup"><span data-stu-id="faf81-373">Properties</span></span> | <span data-ttu-id="faf81-374">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-374">Type</span></span> | <span data-ttu-id="faf81-375">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-375">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-376">scriptId</span><span class="sxs-lookup"><span data-stu-id="faf81-376">scriptId</span></span> | [<span data-ttu-id="faf81-377">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="faf81-377">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="faf81-378">Identificador de script conforme relatado no `Debugger.scriptParsed` .</span><span class="sxs-lookup"><span data-stu-id="faf81-378">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="faf81-379">lineNumber</span><span class="sxs-lookup"><span data-stu-id="faf81-379">lineNumber</span></span> | `integer` | <span data-ttu-id="faf81-380">Número da linha no script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="faf81-380">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="faf81-381">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-381">columnNumber \(optional\)</span></span> | `integer` | <span data-ttu-id="faf81-382">Número da coluna no script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="faf81-382">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="faf81-383">msLength</span><span class="sxs-lookup"><span data-stu-id="faf81-383">msLength</span></span> | `integer` | <span data-ttu-id="faf81-384">Microsoft: Comprimento do código \(ou seja, número de caracteres\) neste quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="faf81-384">Microsoft:  Length of code \(i.e. number of characters\) at this call frame.</span></span> |  

---  

### <a name="breaklocation-object"></a><span data-ttu-id="faf81-385">Objeto BreakLocation</span><span class="sxs-lookup"><span data-stu-id="faf81-385">BreakLocation object</span></span>  

<a name="breaklocation"></a>  

<span data-ttu-id="faf81-386">Local de quebra no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="faf81-386">Break location in the source code.</span></span>  

| <span data-ttu-id="faf81-387">Propriedades</span><span class="sxs-lookup"><span data-stu-id="faf81-387">Properties</span></span> | <span data-ttu-id="faf81-388">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-388">Type</span></span> | <span data-ttu-id="faf81-389">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-389">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-390">scriptId</span><span class="sxs-lookup"><span data-stu-id="faf81-390">scriptId</span></span> | [<span data-ttu-id="faf81-391">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="faf81-391">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="faf81-392">Identificador de script conforme relatado no `Debugger.scriptParsed` .</span><span class="sxs-lookup"><span data-stu-id="faf81-392">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="faf81-393">lineNumber</span><span class="sxs-lookup"><span data-stu-id="faf81-393">lineNumber</span></span> | `integer` | <span data-ttu-id="faf81-394">Número da linha no script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="faf81-394">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="faf81-395">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-395">columnNumber \(optional\)</span></span> | `integer` | <span data-ttu-id="faf81-396">Número da coluna no script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="faf81-396">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="faf81-397">msLength</span><span class="sxs-lookup"><span data-stu-id="faf81-397">msLength</span></span> | `integer` | <span data-ttu-id="faf81-398">Microsoft: Comprimento do código \(ou seja, número de caracteres\) neste quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="faf81-398">Microsoft:  Length of code \(i.e. number of characters\) at this call frame.</span></span> |  
| <span data-ttu-id="faf81-399">tipo \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-399">type \(optional\)</span></span> | `string` | <span data-ttu-id="faf81-400">Valores permitidos: depuradorStatement, chamada, retorno.</span><span class="sxs-lookup"><span data-stu-id="faf81-400">Allowed values: debuggerStatement, call, return.</span></span> |  

---  

### <a name="callframe-object"></a><span data-ttu-id="faf81-401">Objeto CallFrame</span><span class="sxs-lookup"><span data-stu-id="faf81-401">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="faf81-402">Quadro de chamada JavaScript.</span><span class="sxs-lookup"><span data-stu-id="faf81-402">JavaScript call frame.</span></span> <span data-ttu-id="faf81-403">Matriz de quadros de chamada forma a pilha de chamada.</span><span class="sxs-lookup"><span data-stu-id="faf81-403">Array of call frames form the call stack.</span></span>  

| <span data-ttu-id="faf81-404">Propriedades</span><span class="sxs-lookup"><span data-stu-id="faf81-404">Properties</span></span> | <span data-ttu-id="faf81-405">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-405">Type</span></span> | <span data-ttu-id="faf81-406">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-406">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-407">callFrameId</span><span class="sxs-lookup"><span data-stu-id="faf81-407">callFrameId</span></span> | [<span data-ttu-id="faf81-408">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="faf81-408">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="faf81-409">Identificador de quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="faf81-409">Call frame identifier.</span></span>  <span data-ttu-id="faf81-410">Esse identificador só é válido enquanto o depurador é pausado.</span><span class="sxs-lookup"><span data-stu-id="faf81-410">This identifier is only valid while the debugger is paused.</span></span> |  
| <span data-ttu-id="faf81-411">functionName</span><span class="sxs-lookup"><span data-stu-id="faf81-411">functionName</span></span> | `string` | <span data-ttu-id="faf81-412">Nome da função JavaScript chamada neste quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="faf81-412">Name of the JavaScript function called on this call frame.</span></span> |  
| <span data-ttu-id="faf81-413">functionLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-413">functionLocation \(optional\)</span></span> | [<span data-ttu-id="faf81-414">Location</span><span class="sxs-lookup"><span data-stu-id="faf81-414">Location</span></span>](#location) | <span data-ttu-id="faf81-415">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="faf81-415">**Experimental**.</span></span>  <span data-ttu-id="faf81-416">Local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="faf81-416">Location in the source code.</span></span> |  
| <span data-ttu-id="faf81-417">location</span><span class="sxs-lookup"><span data-stu-id="faf81-417">location</span></span> | [<span data-ttu-id="faf81-418">Location</span><span class="sxs-lookup"><span data-stu-id="faf81-418">Location</span></span>](#location) | <span data-ttu-id="faf81-419">Local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="faf81-419">Location in the source code.</span></span> |  
| <span data-ttu-id="faf81-420">url</span><span class="sxs-lookup"><span data-stu-id="faf81-420">url</span></span> | `string` | <span data-ttu-id="faf81-421">Nome ou url do script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="faf81-421">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="faf81-422">scopeChain</span><span class="sxs-lookup"><span data-stu-id="faf81-422">scopeChain</span></span> | [<span data-ttu-id="faf81-423">Scope[]</span><span class="sxs-lookup"><span data-stu-id="faf81-423">Scope[]</span></span>](#scope) | <span data-ttu-id="faf81-424">Cadeia de escopo para esse quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="faf81-424">Scope chain for this call frame.</span></span> |  
| <span data-ttu-id="faf81-425">this</span><span class="sxs-lookup"><span data-stu-id="faf81-425">this</span></span> | [<span data-ttu-id="faf81-426">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="faf81-426">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | `this` <span data-ttu-id="faf81-427">para esse quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="faf81-427">object for this call frame.</span></span> |  
| <span data-ttu-id="faf81-428">returnValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-428">returnValue \(optional\)</span></span> | [<span data-ttu-id="faf81-429">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="faf81-429">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="faf81-430">O valor que está sendo retornado, se a função estiver no ponto de retorno.</span><span class="sxs-lookup"><span data-stu-id="faf81-430">The value being returned, if the function is at return point.</span></span> |  

---  

### <a name="scope-object"></a><span data-ttu-id="faf81-431">Objeto Scope</span><span class="sxs-lookup"><span data-stu-id="faf81-431">Scope object</span></span>  

<a name="scope"></a>  

<span data-ttu-id="faf81-432">Descrição do escopo.</span><span class="sxs-lookup"><span data-stu-id="faf81-432">Scope description.</span></span>  

| <span data-ttu-id="faf81-433">Propriedades</span><span class="sxs-lookup"><span data-stu-id="faf81-433">Properties</span></span> | <span data-ttu-id="faf81-434">Tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-434">Type</span></span> | <span data-ttu-id="faf81-435">Detalhes</span><span class="sxs-lookup"><span data-stu-id="faf81-435">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="faf81-436">tipo</span><span class="sxs-lookup"><span data-stu-id="faf81-436">type</span></span> | `string` | <span data-ttu-id="faf81-437">Tipo de escopo.</span><span class="sxs-lookup"><span data-stu-id="faf81-437">Scope type.</span></span>  <span data-ttu-id="faf81-438">Valores permitidos:  `global` , , , , , , , , , `local` , `with` `closure` `catch` `block` `script` `eval` `module` e</span><span class="sxs-lookup"><span data-stu-id="faf81-438">Allowed values:  `global`, `local`, `with`, `closure`, `catch`, `block`, `script`, `eval`, `module`, and</span></span> `return` |  
| <span data-ttu-id="faf81-439">object</span><span class="sxs-lookup"><span data-stu-id="faf81-439">object</span></span> | [<span data-ttu-id="faf81-440">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="faf81-440">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="faf81-441">Objeto que representa o escopo.</span><span class="sxs-lookup"><span data-stu-id="faf81-441">Object representing the scope.</span></span>  <span data-ttu-id="faf81-442">Para e escopos ele representa o objeto real; para o restante dos escopos, ele é `global` objeto transitório artificial enumerando variáveis de escopo `with` como suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="faf81-442">For `global` and `with` scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span> |  
| <span data-ttu-id="faf81-443">nome \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-443">name \(optional\)</span></span> | `string` | &nbsp; |  
| <span data-ttu-id="faf81-444">startLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-444">startLocation \(optional\)</span></span> | [<span data-ttu-id="faf81-445">Location</span><span class="sxs-lookup"><span data-stu-id="faf81-445">Location</span></span>](#location) | <span data-ttu-id="faf81-446">Local no código-fonte onde o escopo é iniciado.</span><span class="sxs-lookup"><span data-stu-id="faf81-446">Location in the source code where scope starts.</span></span> |  
| <span data-ttu-id="faf81-447">endLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="faf81-447">endLocation \(optional\)</span></span> | [<span data-ttu-id="faf81-448">Location</span><span class="sxs-lookup"><span data-stu-id="faf81-448">Location</span></span>](#location) | <span data-ttu-id="faf81-449">Local no código-fonte onde o escopo termina.</span><span class="sxs-lookup"><span data-stu-id="faf81-449">Location in the source code where scope ends.</span></span> |  

---  

## <a name="dependencies"></a><span data-ttu-id="faf81-450">Dependências</span><span class="sxs-lookup"><span data-stu-id="faf81-450">Dependencies</span></span>  

[<span data-ttu-id="faf81-451">Tempo de Execução</span><span class="sxs-lookup"><span data-stu-id="faf81-451">Runtime</span></span>](./runtime.md)  
