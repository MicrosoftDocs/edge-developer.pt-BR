---
description: Referência do Protocolo DevTools Versão 0.1 (EdgeHTML) para o Domínio de Depurador.  O domínio depurador expõe os recursos de depuração do JavaScript.  Ele permite definir e remover pontos de interrupção, passar pela execução, explorar rastreamentos de pilha, etc.
title: Domínio de depurador - DevTools Protocol Versão 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d63408e23fd8912cf617bfefae2b991387b45a38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397675"
---
# <a name="debugger-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="dc9b6-105">Domínio de depurador - DevTools Protocol Versão 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-105">Debugger Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  
  
<span data-ttu-id="dc9b6-106">O domínio depurador expõe os recursos de depuração do JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-106">Debugger domain exposes JavaScript debugging capabilities.</span></span>  <span data-ttu-id="dc9b6-107">Ele permite definir e remover pontos de interrupção, passar pela execução, explorar rastreamentos de pilha, etc.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| <span data-ttu-id="dc9b6-108">Classificação</span><span class="sxs-lookup"><span data-stu-id="dc9b6-108">Classification</span></span> | <span data-ttu-id="dc9b6-109">Membros</span><span class="sxs-lookup"><span data-stu-id="dc9b6-109">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="dc9b6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc9b6-110">Methods</span></span>](#methods) | <span data-ttu-id="dc9b6-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |  
| [<span data-ttu-id="dc9b6-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="dc9b6-112">Events</span></span>](#events) | <span data-ttu-id="dc9b6-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |  
| [<span data-ttu-id="dc9b6-114">Tipos</span><span class="sxs-lookup"><span data-stu-id="dc9b6-114">Types</span></span>](#types) | <span data-ttu-id="dc9b6-115">[BreakpointId,](#breakpointid) [CallFrameId,](#callframeid) [Location,](#location) [BreakLocation,](#breaklocation) [CallFrame,](#callframe) [Scope](#scope)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |  
| [<span data-ttu-id="dc9b6-116">Dependências</span><span class="sxs-lookup"><span data-stu-id="dc9b6-116">Dependencies</span></span>](#dependencies) | [<span data-ttu-id="dc9b6-117">Tempo de Execução</span><span class="sxs-lookup"><span data-stu-id="dc9b6-117">Runtime</span></span>](./runtime.md) |  

## <a name="methods"></a><span data-ttu-id="dc9b6-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc9b6-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="dc9b6-119">Habilitar</span><span class="sxs-lookup"><span data-stu-id="dc9b6-119">enable</span></span>  

<span data-ttu-id="dc9b6-120">Habilita o depurador para a página determinada.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-120">Enables debugger for the given page.</span></span>  <span data-ttu-id="dc9b6-121">Os clientes não devem presumir que a depuração foi habilitada até que o resultado desse comando seja recebido.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-121">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="dc9b6-122">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="dc9b6-122">disable</span></span>  

<span data-ttu-id="dc9b6-123">Desabilita o depurador para determinada página.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-123">Disables debugger for given page.</span></span>  

&nbsp;  

---  

### <a name="getpossiblebreakpoints"></a><span data-ttu-id="dc9b6-124">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="dc9b6-124">getPossibleBreakpoints</span></span>  

<span data-ttu-id="dc9b6-125">Retorna possíveis locais para ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-125">Returns possible locations for breakpoint.</span></span>  <span data-ttu-id="dc9b6-126">scriptId em locais de intervalo inicial e final deve ser o mesmo.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-126">scriptId in start and end range locations should be the same.</span></span>  

| <span data-ttu-id="dc9b6-127">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc9b6-127">Parameters</span></span> | <span data-ttu-id="dc9b6-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-128">Type</span></span> | <span data-ttu-id="dc9b6-129">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-129">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-130">start</span><span class="sxs-lookup"><span data-stu-id="dc9b6-130">start</span></span> | [<span data-ttu-id="dc9b6-131">Location</span><span class="sxs-lookup"><span data-stu-id="dc9b6-131">Location</span></span>](#location) | <span data-ttu-id="dc9b6-132">Início do intervalo para pesquisar possíveis locais de ponto de interrupção em.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-132">Start of range to search possible breakpoint locations in.</span></span> |  
| <span data-ttu-id="dc9b6-133">encerrar</span><span class="sxs-lookup"><span data-stu-id="dc9b6-133">end</span></span> | [<span data-ttu-id="dc9b6-134">Location</span><span class="sxs-lookup"><span data-stu-id="dc9b6-134">Location</span></span>](#location) | <span data-ttu-id="dc9b6-135">Fim do intervalo para pesquisar possíveis locais de ponto de interrupção em \(excludendo\).</span><span class="sxs-lookup"><span data-stu-id="dc9b6-135">End of range to search possible breakpoint locations in \(excluding\).</span></span>  <span data-ttu-id="dc9b6-136">Quando não especificado, o fim dos scripts é usado como fim do intervalo.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-136">When not specified, end of scripts is used as end of range.</span></span> |  

| <span data-ttu-id="dc9b6-137">Retorna</span><span class="sxs-lookup"><span data-stu-id="dc9b6-137">Returns</span></span> | <span data-ttu-id="dc9b6-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-138">Type</span></span> | <span data-ttu-id="dc9b6-139">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-139">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-140">locations</span><span class="sxs-lookup"><span data-stu-id="dc9b6-140">locations</span></span> | [<span data-ttu-id="dc9b6-141">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="dc9b6-141">BreakLocation</span></span>](#breaklocation) | <span data-ttu-id="dc9b6-142">Lista dos possíveis locais de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-142">List of the possible breakpoint locations.</span></span> |  

---  

### <a name="setbreakpointsactive"></a><span data-ttu-id="dc9b6-143">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="dc9b6-143">setBreakpointsActive</span></span>  

<span data-ttu-id="dc9b6-144">Ativa/desativa todos os pontos de interrupção na página.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-144">Activates / deactivates all breakpoints on the page.</span></span>  

| <span data-ttu-id="dc9b6-145">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc9b6-145">Parameters</span></span> | <span data-ttu-id="dc9b6-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-146">Type</span></span> | <span data-ttu-id="dc9b6-147">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-147">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-148">active</span><span class="sxs-lookup"><span data-stu-id="dc9b6-148">active</span></span> | `boolean` | <span data-ttu-id="dc9b6-149">Novo valor para o estado ativo de pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-149">New value for breakpoints active state.</span></span> |  

---  

### <a name="setbreakpointbyurl"></a><span data-ttu-id="dc9b6-150">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="dc9b6-150">setBreakpointByUrl</span></span>  

<span data-ttu-id="dc9b6-151">Define o ponto de interrupção JavaScript em determinado local especificado por URL ou URL regex.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-151">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span>  <span data-ttu-id="dc9b6-152">Depois que esse comando for emitido, todos os scripts analisados existentes terão pontos de interrupção resolvidos e retornados na `locations` propriedade.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-152">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in `locations` property.</span></span>  <span data-ttu-id="dc9b6-153">A análise de scripts correspondentes posteriores resultará em eventos `breakpointResolved` subsequentes emitidos.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-153">Further matching script parsing will result in subsequent `breakpointResolved` events issued.</span></span>  <span data-ttu-id="dc9b6-154">Esse ponto de interrupção lógico sobreviverá a recarregações de página.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-154">This logical breakpoint will survive page reloads.</span></span>  

| <span data-ttu-id="dc9b6-155">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc9b6-155">Parameters</span></span> | <span data-ttu-id="dc9b6-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-156">Type</span></span> | <span data-ttu-id="dc9b6-157">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-157">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-158">lineNumber</span><span class="sxs-lookup"><span data-stu-id="dc9b6-158">lineNumber</span></span> | `integer` | <span data-ttu-id="dc9b6-159">Número da linha para definir ponto de interrupção em.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-159">Line number to set breakpoint at.</span></span> |  
| <span data-ttu-id="dc9b6-160">url \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-160">url  \(optional\)</span></span> | `string` | <span data-ttu-id="dc9b6-161">URL dos recursos para definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-161">URL of the resources to set breakpoint on.</span></span> |  
| <span data-ttu-id="dc9b6-162">urlRegex \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-162">urlRegex  \(optional\)</span></span> | `string` | <span data-ttu-id="dc9b6-163">Padrão regex para as URLs dos recursos para definir pontos de interrupção.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-163">Regex pattern for the URLs of the resources to set breakpoints on.</span></span>  <span data-ttu-id="dc9b6-164">Ou `url` `urlRegex` deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-164">Either `url` or `urlRegex` must be specified.</span></span> |  
| <span data-ttu-id="dc9b6-165">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-165">columnNumber  \(optional\)</span></span> | `integer` | <span data-ttu-id="dc9b6-166">Deslocamento na linha para definir ponto de interrupção em.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-166">Offset in the line to set breakpoint at.</span></span> |  
| <span data-ttu-id="dc9b6-167">condição \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-167">condition  \(optional\)</span></span> | `string` | <span data-ttu-id="dc9b6-168">Expressão a ser usada como uma condição de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-168">Expression to use as a breakpoint condition.</span></span>  <span data-ttu-id="dc9b6-169">Quando especificado, o depurador só será parar no ponto de interrupção se essa expressão for avaliada como true.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-169">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="dc9b6-170">Retorna</span><span class="sxs-lookup"><span data-stu-id="dc9b6-170">Returns</span></span> | <span data-ttu-id="dc9b6-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-171">Type</span></span> | <span data-ttu-id="dc9b6-172">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-172">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-173">breakpointId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-173">breakpointId</span></span> | [<span data-ttu-id="dc9b6-174">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-174">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="dc9b6-175">ID do ponto de interrupção criado para referência posterior.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-175">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="dc9b6-176">locations</span><span class="sxs-lookup"><span data-stu-id="dc9b6-176">locations</span></span> | [<span data-ttu-id="dc9b6-177">Local[]</span><span class="sxs-lookup"><span data-stu-id="dc9b6-177">Location[]</span></span>](#location) | <span data-ttu-id="dc9b6-178">Lista dos locais em que esse ponto de interrupção foi resolvido após a adição.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-178">List of the locations this breakpoint resolved into upon addition.</span></span> |  

---  

### <a name="setbreakpoint"></a><span data-ttu-id="dc9b6-179">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="dc9b6-179">setBreakpoint</span></span>  

<span data-ttu-id="dc9b6-180">Define o ponto de interrupção JavaScript em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-180">Sets JavaScript breakpoint at a given location.</span></span>  

| <span data-ttu-id="dc9b6-181">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc9b6-181">Parameters</span></span> | <span data-ttu-id="dc9b6-182">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-182">Type</span></span> | <span data-ttu-id="dc9b6-183">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-183">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-184">location</span><span class="sxs-lookup"><span data-stu-id="dc9b6-184">location</span></span> | [<span data-ttu-id="dc9b6-185">Location</span><span class="sxs-lookup"><span data-stu-id="dc9b6-185">Location</span></span>](#location) | <span data-ttu-id="dc9b6-186">Local para definir o ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-186">Location to set breakpoint in.</span></span> |  
| <span data-ttu-id="dc9b6-187">condição \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-187">condition  \(optional\)</span></span> | `string` | <span data-ttu-id="dc9b6-188">Expressão a ser usada como uma condição de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-188">Expression to use as a breakpoint condition.</span></span>  <span data-ttu-id="dc9b6-189">Quando especificado, o depurador só será parar no ponto de interrupção se essa expressão for avaliada como true.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-189">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="dc9b6-190">Retorna</span><span class="sxs-lookup"><span data-stu-id="dc9b6-190">Returns</span></span> | <span data-ttu-id="dc9b6-191">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-191">Type</span></span> | <span data-ttu-id="dc9b6-192">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-192">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-193">breakpointId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-193">breakpointId</span></span> | [<span data-ttu-id="dc9b6-194">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-194">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="dc9b6-195">ID do ponto de interrupção criado para referência posterior.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-195">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="dc9b6-196">actualLocation</span><span class="sxs-lookup"><span data-stu-id="dc9b6-196">actualLocation</span></span> | [<span data-ttu-id="dc9b6-197">Location</span><span class="sxs-lookup"><span data-stu-id="dc9b6-197">Location</span></span>](#location) | <span data-ttu-id="dc9b6-198">Local em que o ponto de interrupção foi resolvido.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-198">Location this breakpoint resolved into.</span></span> |  

---  

### <a name="removebreakpoint"></a><span data-ttu-id="dc9b6-199">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="dc9b6-199">removeBreakpoint</span></span>  

<span data-ttu-id="dc9b6-200">Remove o ponto de interrupção JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-200">Removes JavaScript breakpoint.</span></span>  

| <span data-ttu-id="dc9b6-201">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc9b6-201">Parameters</span></span> | <span data-ttu-id="dc9b6-202">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-202">Type</span></span> | <span data-ttu-id="dc9b6-203">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-203">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-204">breakpointId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-204">breakpointId</span></span> | [<span data-ttu-id="dc9b6-205">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-205">BreakpointId</span></span>](#breakpointid) | &nbsp; |  

---  

### <a name="stepover"></a><span data-ttu-id="dc9b6-206">stepOver</span><span class="sxs-lookup"><span data-stu-id="dc9b6-206">stepOver</span></span>  

<span data-ttu-id="dc9b6-207">Etapas sobre a instrução.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-207">Steps over the statement.</span></span>  

&nbsp;  

---  

### <a name="stepinto"></a><span data-ttu-id="dc9b6-208">stepInto</span><span class="sxs-lookup"><span data-stu-id="dc9b6-208">stepInto</span></span>  

<span data-ttu-id="dc9b6-209">Etapas na chamada de função.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-209">Steps into the function call.</span></span>  

&nbsp;  

---  

### <a name="stepout"></a><span data-ttu-id="dc9b6-210">stepOut</span><span class="sxs-lookup"><span data-stu-id="dc9b6-210">stepOut</span></span>  

<span data-ttu-id="dc9b6-211">Sai da chamada de função.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-211">Steps out of the function call.</span></span>  

&nbsp;  

---  

### <a name="pause"></a><span data-ttu-id="dc9b6-212">pause</span><span class="sxs-lookup"><span data-stu-id="dc9b6-212">pause</span></span>  

<span data-ttu-id="dc9b6-213">Para na próxima instrução JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-213">Stops on the next JavaScript statement.</span></span>  

&nbsp;  

---  

### <a name="resume"></a><span data-ttu-id="dc9b6-214">resume</span><span class="sxs-lookup"><span data-stu-id="dc9b6-214">resume</span></span>  

<span data-ttu-id="dc9b6-215">Retoma a execução do JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-215">Resumes JavaScript execution.</span></span>  

&nbsp;  

---  

### <a name="getscriptsource"></a><span data-ttu-id="dc9b6-216">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="dc9b6-216">getScriptSource</span></span>  

<span data-ttu-id="dc9b6-217">Retorna a origem do script com a ID determinada.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-217">Returns source for the script with given ID.</span></span>  

| <span data-ttu-id="dc9b6-218">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc9b6-218">Parameters</span></span> | <span data-ttu-id="dc9b6-219">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-219">Type</span></span> | <span data-ttu-id="dc9b6-220">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-220">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-221">scriptId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-221">scriptId</span></span> | [<span data-ttu-id="dc9b6-222">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-222">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="dc9b6-223">ID do script para o que obter a origem.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-223">ID of the script to get source for.</span></span> |  
| <span data-ttu-id="dc9b6-224">Retorna</span><span class="sxs-lookup"><span data-stu-id="dc9b6-224">Returns</span></span> | <span data-ttu-id="dc9b6-225">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-225">Type</span></span> | <span data-ttu-id="dc9b6-226">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-226">Details</span></span> |  
|<span data-ttu-id="dc9b6-227">:---</span><span class="sxs-lookup"><span data-stu-id="dc9b6-227">:---</span></span> |<span data-ttu-id="dc9b6-228">:---</span><span class="sxs-lookup"><span data-stu-id="dc9b6-228">:---</span></span> |<span data-ttu-id="dc9b6-229">:---</span><span class="sxs-lookup"><span data-stu-id="dc9b6-229">:---</span></span> |  
| <span data-ttu-id="dc9b6-230">scriptSource</span><span class="sxs-lookup"><span data-stu-id="dc9b6-230">scriptSource</span></span> | `string` | <span data-ttu-id="dc9b6-231">Origem do script.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-231">Script source.</span></span> |  

---  

### <a name="setpauseonexceptions"></a><span data-ttu-id="dc9b6-232">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="dc9b6-232">setPauseOnExceptions</span></span>  

<span data-ttu-id="dc9b6-233">Define pausa no estado de exceções.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-233">Defines pause on exceptions state.</span></span>  <span data-ttu-id="dc9b6-234">Pode ser definido para parar em todas as exceções, exceções não ativas ou nenhuma exceção.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-234">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span>  <span data-ttu-id="dc9b6-235">A pausa inicial no estado de exceções é `none` .</span><span class="sxs-lookup"><span data-stu-id="dc9b6-235">Initial pause on exceptions state is `none`.</span></span>  

| <span data-ttu-id="dc9b6-236">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc9b6-236">Parameters</span></span> | <span data-ttu-id="dc9b6-237">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-237">Type</span></span> | <span data-ttu-id="dc9b6-238">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-238">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-239">state</span><span class="sxs-lookup"><span data-stu-id="dc9b6-239">state</span></span> | `string` | <span data-ttu-id="dc9b6-240">Pause no modo de exceções.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-240">Pause on exceptions mode.</span></span>  <span data-ttu-id="dc9b6-241">Valores permitidos:  `none` `uncaught` , e</span><span class="sxs-lookup"><span data-stu-id="dc9b6-241">Allowed values:  `none`, `uncaught`, and</span></span> `all` |  

---  

### <a name="evaluateoncallframe"></a><span data-ttu-id="dc9b6-242">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="dc9b6-242">evaluateOnCallFrame</span></span>  

<span data-ttu-id="dc9b6-243">Avalia a expressão em um determinado quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-243">Evaluates expression on a given call frame.</span></span>  

| <span data-ttu-id="dc9b6-244">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc9b6-244">Parameters</span></span> | <span data-ttu-id="dc9b6-245">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-245">Type</span></span> | <span data-ttu-id="dc9b6-246">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-246">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-247">callFrameId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-247">callFrameId</span></span> | [<span data-ttu-id="dc9b6-248">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-248">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="dc9b6-249">Identificador de quadro de chamada a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-249">Call frame identifier to evaluate on.</span></span> |  
| <span data-ttu-id="dc9b6-250">expressão</span><span class="sxs-lookup"><span data-stu-id="dc9b6-250">expression</span></span> | `string` | <span data-ttu-id="dc9b6-251">Expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-251">Expression to evaluate.</span></span> |  
| <span data-ttu-id="dc9b6-252">Retorna</span><span class="sxs-lookup"><span data-stu-id="dc9b6-252">Returns</span></span> | <span data-ttu-id="dc9b6-253">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-253">Type</span></span> | <span data-ttu-id="dc9b6-254">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-254">Details</span></span> |  
|<span data-ttu-id="dc9b6-255">:---</span><span class="sxs-lookup"><span data-stu-id="dc9b6-255">:---</span></span> |<span data-ttu-id="dc9b6-256">:---</span><span class="sxs-lookup"><span data-stu-id="dc9b6-256">:---</span></span> |<span data-ttu-id="dc9b6-257">:---</span><span class="sxs-lookup"><span data-stu-id="dc9b6-257">:---</span></span> |  
| <span data-ttu-id="dc9b6-258">result</span><span class="sxs-lookup"><span data-stu-id="dc9b6-258">result</span></span> | [<span data-ttu-id="dc9b6-259">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="dc9b6-259">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="dc9b6-260">Wrapper do objeto para o resultado da avaliação.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-260">Object wrapper for the evaluation result.</span></span> |  

---  

### <a name="setvariablevalue"></a><span data-ttu-id="dc9b6-261">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="dc9b6-261">setVariableValue</span></span>  

<span data-ttu-id="dc9b6-262">Altera o valor da variável em um callframe.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-262">Changes value of variable in a callframe.</span></span>  <span data-ttu-id="dc9b6-263">Os escopos baseados em objeto não têm suporte e devem ser transformados manualmente.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-263">Object-based scopes are not supported and must be mutated manually.</span></span>  

| <span data-ttu-id="dc9b6-264">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc9b6-264">Parameters</span></span> | <span data-ttu-id="dc9b6-265">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-265">Type</span></span> | <span data-ttu-id="dc9b6-266">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-266">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-267">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="dc9b6-267">scopeNumber</span></span> | `integer` | <span data-ttu-id="dc9b6-268">Número baseado em 0 do escopo conforme listado na cadeia de escopo.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-268">0-based number of scope as was listed in scope chain.</span></span>  <span data-ttu-id="dc9b6-269">Somente `local` , e os tipos de escopo são `closure` `catch` permitidos.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-269">Only `local`, `closure`, and `catch` scope types are allowed.</span></span>  <span data-ttu-id="dc9b6-270">Outros escopos podem ser manipulados manualmente.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-270">Other scopes could be manipulated manually.</span></span> |  
| <span data-ttu-id="dc9b6-271">variableName</span><span class="sxs-lookup"><span data-stu-id="dc9b6-271">variableName</span></span> | `string` | <span data-ttu-id="dc9b6-272">Nome da variável.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-272">Variable name.</span></span> |  
| <span data-ttu-id="dc9b6-273">newValue</span><span class="sxs-lookup"><span data-stu-id="dc9b6-273">newValue</span></span> | [<span data-ttu-id="dc9b6-274">Runtime.CallArgument</span><span class="sxs-lookup"><span data-stu-id="dc9b6-274">Runtime.CallArgument</span></span>](./runtime.md#callargument) | <span data-ttu-id="dc9b6-275">Novo valor variável.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-275">New variable value.</span></span> |  
| <span data-ttu-id="dc9b6-276">callFrameId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-276">callFrameId</span></span> | [<span data-ttu-id="dc9b6-277">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-277">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="dc9b6-278">ID do callframe que contém variável.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-278">ID of callframe that holds variable.</span></span> |  

---  

### <a name="setblackboxpatterns"></a><span data-ttu-id="dc9b6-279">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="dc9b6-279">setBlackboxPatterns</span></span>  

<span data-ttu-id="dc9b6-280">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-280">**Experimental**.</span></span>  <span data-ttu-id="dc9b6-281">Substitua padrões de caixa preta anteriores por aqueles passados.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-281">Replace previous blackbox patterns with passed ones.</span></span>  <span data-ttu-id="dc9b6-282">Força o back-end a ignorar a revisão/pausa em scripts com a URL correspondente a um dos padrões.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-282">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span>  <span data-ttu-id="dc9b6-283">O depurador tentará deixar o script em caixa preta executando várias vezes, finalmente `step in` recorrendo `step out` se não tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-283">The debugger will try to leave blackboxed script by performing `step in` several times, finally resorting to `step out` if unsuccessful.</span></span>  

| <span data-ttu-id="dc9b6-284">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc9b6-284">Parameters</span></span> | <span data-ttu-id="dc9b6-285">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-285">Type</span></span> | <span data-ttu-id="dc9b6-286">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-286">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-287">patterns</span><span class="sxs-lookup"><span data-stu-id="dc9b6-287">patterns</span></span> | `string[]` | <span data-ttu-id="dc9b6-288">Matriz de regexps que será usada para verificar a URL do script para o estado de blackbox.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-288">Array of regexps that will be used to check script url for blackbox state.</span></span> |  

---  

### <a name="mssetdebuggerpropertyvalue"></a><span data-ttu-id="dc9b6-289">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="dc9b6-289">msSetDebuggerPropertyValue</span></span>  

<span data-ttu-id="dc9b6-290">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-290">**Experimental**.</span></span>  <span data-ttu-id="dc9b6-291">Microsoft: define a propriedade depurador especificada como o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-291">Microsoft:  Sets the specified debugger property to the specified value.</span></span>  

| <span data-ttu-id="dc9b6-292">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc9b6-292">Parameters</span></span> | <span data-ttu-id="dc9b6-293">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-293">Type</span></span> | <span data-ttu-id="dc9b6-294">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-294">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-295">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-295">debuggerPropertyId</span></span> | `string` | <span data-ttu-id="dc9b6-296">Microsoft: A ID da propriedade \(ou seja, msDebuggerPropertyId\) a ser definida.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-296">Microsoft: The property ID \(i.e. msDebuggerPropertyId\) to set.</span></span> |  
| <span data-ttu-id="dc9b6-297">newValue</span><span class="sxs-lookup"><span data-stu-id="dc9b6-297">newValue</span></span> | `string` | &nbsp; |  

---  

## <a name="events"></a><span data-ttu-id="dc9b6-298">Eventos</span><span class="sxs-lookup"><span data-stu-id="dc9b6-298">Events</span></span>  

### <a name="scriptparsed"></a><span data-ttu-id="dc9b6-299">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="dc9b6-299">scriptParsed</span></span>  

<span data-ttu-id="dc9b6-300">Disparado quando o script é analisado.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-300">Fired when the script is parsed.</span></span>  <span data-ttu-id="dc9b6-301">Esse evento também é acionado para todos os scripts conhecidos e não recolhidos ao habilitar o depurador.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-301">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>  

| <span data-ttu-id="dc9b6-302">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc9b6-302">Parameters</span></span> | <span data-ttu-id="dc9b6-303">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-303">Type</span></span> | <span data-ttu-id="dc9b6-304">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-304">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-305">scriptId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-305">scriptId</span></span> | [<span data-ttu-id="dc9b6-306">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-306">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="dc9b6-307">Identificador do script analisado.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-307">Identifier of the script parsed.</span></span> |  
| <span data-ttu-id="dc9b6-308">url</span><span class="sxs-lookup"><span data-stu-id="dc9b6-308">url</span></span> | `string` | <span data-ttu-id="dc9b6-309">URL ou nome do script analisado \(se tiver\).</span><span class="sxs-lookup"><span data-stu-id="dc9b6-309">URL or name of the script parsed \(if any\).</span></span> |  
| <span data-ttu-id="dc9b6-310">startLine</span><span class="sxs-lookup"><span data-stu-id="dc9b6-310">startLine</span></span> | `integer` | <span data-ttu-id="dc9b6-311">Deslocamento de linha do script dentro do recurso com a URL determinada \(para marcas de script\).</span><span class="sxs-lookup"><span data-stu-id="dc9b6-311">Line offset of the script within the resource with given URL \(for script tags\).</span></span> |  
| <span data-ttu-id="dc9b6-312">startColumn</span><span class="sxs-lookup"><span data-stu-id="dc9b6-312">startColumn</span></span> | `integer` | <span data-ttu-id="dc9b6-313">Deslocamento de coluna do script dentro do recurso com a URL determinada.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-313">Column offset of the script within the resource with given URL.</span></span> |  
| <span data-ttu-id="dc9b6-314">endLine</span><span class="sxs-lookup"><span data-stu-id="dc9b6-314">endLine</span></span> | `integer` | <span data-ttu-id="dc9b6-315">Última linha do script.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-315">Last line of the script.</span></span> |  
| <span data-ttu-id="dc9b6-316">endColumn</span><span class="sxs-lookup"><span data-stu-id="dc9b6-316">endColumn</span></span> | `integer` | <span data-ttu-id="dc9b6-317">Comprimento da última linha do script.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-317">Length of the last line of the script.</span></span> |  
| <span data-ttu-id="dc9b6-318">executionContextId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-318">executionContextId</span></span> | [<span data-ttu-id="dc9b6-319">Runtime.ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-319">Runtime.ExecutionContextId</span></span>](./runtime.md#executioncontextid) | <span data-ttu-id="dc9b6-320">Especifica o contexto de criação de script.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-320">Specifies script creation context.</span></span> |  
| <span data-ttu-id="dc9b6-321">sourceMapURL \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-321">sourceMapURL  \(optional\)</span></span> | `string` | <span data-ttu-id="dc9b6-322">URL do mapa de origem associado ao script (se for o caso).</span><span class="sxs-lookup"><span data-stu-id="dc9b6-322">URL of source map associated with script (if any).</span></span> |  
| <span data-ttu-id="dc9b6-323">comprimento \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-323">length  \(optional\)</span></span> | `integer` | <span data-ttu-id="dc9b6-324">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-324">**Experimental**.</span></span>  <span data-ttu-id="dc9b6-325">Este comprimento do script.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-325">This script length.</span></span> |  
| <span data-ttu-id="dc9b6-326">msParentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-326">msParentId  \(optional\)</span></span> | `string` | <span data-ttu-id="dc9b6-327">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-327">**Experimental**.</span></span>  <span data-ttu-id="dc9b6-328">Esta é a ID do documento pai.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-328">This is the parent document ID.</span></span> |  
| <span data-ttu-id="dc9b6-329">msMimeType \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-329">msMimeType  \(optional\)</span></span> | `string` | <span data-ttu-id="dc9b6-330">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-330">**Experimental**.</span></span>  <span data-ttu-id="dc9b6-331">Esse é o tipo de mime.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-331">This is the mime type.</span></span> |  
| <span data-ttu-id="dc9b6-332">msIsDynamicCode \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-332">msIsDynamicCode  \(optional\)</span></span> | `boolean` | <span data-ttu-id="dc9b6-333">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-333">**Experimental**.</span></span>  <span data-ttu-id="dc9b6-334">Isso indica se é um código dinâmico.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-334">This indicates whether it is dynamic code.</span></span> |  
| <span data-ttu-id="dc9b6-335">msLongDocumentId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-335">msLongDocumentId  \(optional\)</span></span> | `integer` | <span data-ttu-id="dc9b6-336">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-336">**Experimental**.</span></span>  <span data-ttu-id="dc9b6-337">Esta é a ID do documento longa.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-337">This is the long document ID.</span></span> |  

---  

### <a name="breakpointresolved"></a><span data-ttu-id="dc9b6-338">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="dc9b6-338">breakpointResolved</span></span>  

<span data-ttu-id="dc9b6-339">Acionado quando o ponto de interrupção é resolvido para um script e local reais.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-339">Fired when breakpoint is resolved to an actual script and location.</span></span>  

| <span data-ttu-id="dc9b6-340">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc9b6-340">Parameters</span></span> | <span data-ttu-id="dc9b6-341">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-341">Type</span></span> | <span data-ttu-id="dc9b6-342">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-342">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-343">breakpointId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-343">breakpointId</span></span> | [<span data-ttu-id="dc9b6-344">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-344">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="dc9b6-345">Identificador exclusivo do ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-345">Breakpoint unique identifier.</span></span> |  
| <span data-ttu-id="dc9b6-346">location</span><span class="sxs-lookup"><span data-stu-id="dc9b6-346">location</span></span> | [<span data-ttu-id="dc9b6-347">Location</span><span class="sxs-lookup"><span data-stu-id="dc9b6-347">Location</span></span>](#location) | <span data-ttu-id="dc9b6-348">Local real do ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-348">Actual breakpoint location.</span></span> |  
| <span data-ttu-id="dc9b6-349">msLength \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-349">msLength  \(optional\)</span></span> | `integer` | <span data-ttu-id="dc9b6-350">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-350">**Experimental**.</span></span>  <span data-ttu-id="dc9b6-351">Microsoft: Comprimento do código \(ou seja, número de caracteres\) no local do ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-351">Microsoft:  Length of code \(i.e. number of characters\) at the breakpoint location.</span></span> |  

---  

### <a name="paused"></a><span data-ttu-id="dc9b6-352">pausado</span><span class="sxs-lookup"><span data-stu-id="dc9b6-352">paused</span></span>  

<span data-ttu-id="dc9b6-353">Acionado quando os depurador quebram para um ponto de interrupção ou exceção.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-353">Fired when the debuggers breaks for a breakpoint or exception.</span></span>  

| <span data-ttu-id="dc9b6-354">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc9b6-354">Parameters</span></span> | <span data-ttu-id="dc9b6-355">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-355">Type</span></span> | <span data-ttu-id="dc9b6-356">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-356">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-357">callFrames</span><span class="sxs-lookup"><span data-stu-id="dc9b6-357">callFrames</span></span> | [<span data-ttu-id="dc9b6-358">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="dc9b6-358">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="dc9b6-359">Pilha de chamada em que o depurador parou.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-359">Call stack the debugger stopped on.</span></span> |  
| <span data-ttu-id="dc9b6-360">reason</span><span class="sxs-lookup"><span data-stu-id="dc9b6-360">reason</span></span> | `string` | <span data-ttu-id="dc9b6-361">Pause reason.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-361">Pause reason.</span></span>  <span data-ttu-id="dc9b6-362">Valores permitidos:  `breakpoint` `step` , , `exception` e</span><span class="sxs-lookup"><span data-stu-id="dc9b6-362">Allowed values:  `breakpoint`, `step`, `exception`, and</span></span> `other` |  
| <span data-ttu-id="dc9b6-363">data \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-363">data  \(optional\)</span></span> | `object` | <span data-ttu-id="dc9b6-364">Objeto que contém propriedades auxiliares específicas de quebra.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-364">Object containing break-specific auxiliary properties.</span></span> |  
| <span data-ttu-id="dc9b6-365">hitBreakpoints \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-365">hitBreakpoints  \(optional\)</span></span> | `string[]` | <span data-ttu-id="dc9b6-366">Hit breakpoints IDs</span><span class="sxs-lookup"><span data-stu-id="dc9b6-366">Hit breakpoints IDs</span></span> |  

---  

### <a name="resumed"></a><span data-ttu-id="dc9b6-367">retomada</span><span class="sxs-lookup"><span data-stu-id="dc9b6-367">resumed</span></span>  

<span data-ttu-id="dc9b6-368">Acionado quando o depurador retoma a execução.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-368">Fired when the debugger resumes execution.</span></span>  

&nbsp;  

---  

## <a name="types"></a><span data-ttu-id="dc9b6-369">Tipos</span><span class="sxs-lookup"><span data-stu-id="dc9b6-369">Types</span></span>  

### <a name="breakpointid-string"></a><span data-ttu-id="dc9b6-370">Cadeia de caracteres BreakpointId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-370">BreakpointId string</span></span>  

<a name="breakpointid"></a>  

<span data-ttu-id="dc9b6-371">Identificador de ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-371">Breakpoint identifier.</span></span>  

&nbsp;  

---  

### <a name="callframeid-string"></a><span data-ttu-id="dc9b6-372">Cadeia de caracteres CallFrameId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-372">CallFrameId string</span></span>  

<a name="callframeid"></a>  

<span data-ttu-id="dc9b6-373">Identificador de quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-373">Call frame identifier.</span></span>  

&nbsp;  

---  

### <a name="location-object"></a><span data-ttu-id="dc9b6-374">Objeto Location</span><span class="sxs-lookup"><span data-stu-id="dc9b6-374">Location object</span></span>  

<a name="location"></a>  

<span data-ttu-id="dc9b6-375">Local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-375">Location in the source code.</span></span>  

| <span data-ttu-id="dc9b6-376">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dc9b6-376">Properties</span></span> | <span data-ttu-id="dc9b6-377">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-377">Type</span></span> | <span data-ttu-id="dc9b6-378">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-378">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-379">scriptId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-379">scriptId</span></span> | [<span data-ttu-id="dc9b6-380">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-380">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="dc9b6-381">Identificador de script conforme relatado no `Debugger.scriptParsed` .</span><span class="sxs-lookup"><span data-stu-id="dc9b6-381">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="dc9b6-382">lineNumber</span><span class="sxs-lookup"><span data-stu-id="dc9b6-382">lineNumber</span></span> | `integer` | <span data-ttu-id="dc9b6-383">Número da linha no script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="dc9b6-383">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="dc9b6-384">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-384">columnNumber  \(optional\)</span></span> | `integer` | <span data-ttu-id="dc9b6-385">Número da coluna no script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="dc9b6-385">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="dc9b6-386">msLength</span><span class="sxs-lookup"><span data-stu-id="dc9b6-386">msLength</span></span> | `integer` | <span data-ttu-id="dc9b6-387">Microsoft: Comprimento do código \(ou seja, número de caracteres\) neste quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-387">Microsoft: Length of code \(i.e. number of characters\) at this call frame.</span></span> |  

---  

### <a name="breaklocation-object"></a><span data-ttu-id="dc9b6-388">Objeto BreakLocation</span><span class="sxs-lookup"><span data-stu-id="dc9b6-388">BreakLocation object</span></span>  

<a name="breaklocation"></a>  

<span data-ttu-id="dc9b6-389">Local de quebra no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-389">Break location in the source code.</span></span>  

| <span data-ttu-id="dc9b6-390">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dc9b6-390">Properties</span></span> | <span data-ttu-id="dc9b6-391">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-391">Type</span></span> | <span data-ttu-id="dc9b6-392">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-392">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-393">scriptId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-393">scriptId</span></span> | [<span data-ttu-id="dc9b6-394">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-394">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="dc9b6-395">Identificador de script conforme relatado no `Debugger.scriptParsed` .</span><span class="sxs-lookup"><span data-stu-id="dc9b6-395">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="dc9b6-396">lineNumber</span><span class="sxs-lookup"><span data-stu-id="dc9b6-396">lineNumber</span></span> | `integer` | <span data-ttu-id="dc9b6-397">Número da linha no script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="dc9b6-397">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="dc9b6-398">columnNumber \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-398">columnNumber  \(optional\)</span></span> | `integer` | <span data-ttu-id="dc9b6-399">Número da coluna no script \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="dc9b6-399">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="dc9b6-400">msLength</span><span class="sxs-lookup"><span data-stu-id="dc9b6-400">msLength</span></span> | `integer` | <span data-ttu-id="dc9b6-401">Microsoft: Comprimento do código \(ou seja, número de caracteres\) neste quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-401">Microsoft:  Length of code \(i.e. number of characters\) at this call frame.</span></span> |  
| <span data-ttu-id="dc9b6-402">tipo \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-402">type  \(optional\)</span></span> | `string` | <span data-ttu-id="dc9b6-403">Valores permitidos:  `debuggerStatement` `call` , e</span><span class="sxs-lookup"><span data-stu-id="dc9b6-403">Allowed values:  `debuggerStatement`, `call`, and</span></span> `return` |  

---  

### <a name="callframe-object"></a><span data-ttu-id="dc9b6-404">Objeto CallFrame</span><span class="sxs-lookup"><span data-stu-id="dc9b6-404">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="dc9b6-405">Quadro de chamada JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-405">JavaScript call frame.</span></span>  <span data-ttu-id="dc9b6-406">Matriz de quadros de chamada forma a pilha de chamada.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-406">Array of call frames form the call stack.</span></span>  

| <span data-ttu-id="dc9b6-407">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dc9b6-407">Properties</span></span> | <span data-ttu-id="dc9b6-408">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-408">Type</span></span> | <span data-ttu-id="dc9b6-409">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-409">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-410">callFrameId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-410">callFrameId</span></span> | [<span data-ttu-id="dc9b6-411">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="dc9b6-411">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="dc9b6-412">Identificador de quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-412">Call frame identifier.</span></span>  <span data-ttu-id="dc9b6-413">Esse identificador só é válido enquanto o depurador é pausado.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-413">This identifier is only valid while the debugger is paused.</span></span> |  
| <span data-ttu-id="dc9b6-414">functionName</span><span class="sxs-lookup"><span data-stu-id="dc9b6-414">functionName</span></span> | `string` | <span data-ttu-id="dc9b6-415">Nome da função JavaScript chamada neste quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-415">Name of the JavaScript function called on this call frame.</span></span> |  
| <span data-ttu-id="dc9b6-416">functionLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-416">functionLocation  \(optional\)</span></span> | [<span data-ttu-id="dc9b6-417">Location</span><span class="sxs-lookup"><span data-stu-id="dc9b6-417">Location</span></span>](#location) | <span data-ttu-id="dc9b6-418">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-418">**Experimental**.</span></span>  <span data-ttu-id="dc9b6-419">Local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-419">Location in the source code.</span></span> |  
| <span data-ttu-id="dc9b6-420">location</span><span class="sxs-lookup"><span data-stu-id="dc9b6-420">location</span></span> | [<span data-ttu-id="dc9b6-421">Location</span><span class="sxs-lookup"><span data-stu-id="dc9b6-421">Location</span></span>](#location) | <span data-ttu-id="dc9b6-422">Local no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-422">Location in the source code.</span></span> |  
| <span data-ttu-id="dc9b6-423">url</span><span class="sxs-lookup"><span data-stu-id="dc9b6-423">url</span></span> | `string` | <span data-ttu-id="dc9b6-424">Nome ou url do script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-424">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="dc9b6-425">scopeChain</span><span class="sxs-lookup"><span data-stu-id="dc9b6-425">scopeChain</span></span> | [<span data-ttu-id="dc9b6-426">Scope[]</span><span class="sxs-lookup"><span data-stu-id="dc9b6-426">Scope[]</span></span>](#scope) | <span data-ttu-id="dc9b6-427">Cadeia de escopo para esse quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-427">Scope chain for this call frame.</span></span> |  
| <span data-ttu-id="dc9b6-428">this</span><span class="sxs-lookup"><span data-stu-id="dc9b6-428">this</span></span> | [<span data-ttu-id="dc9b6-429">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="dc9b6-429">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | `this` <span data-ttu-id="dc9b6-430">para esse quadro de chamada.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-430">object for this call frame.</span></span> |  
| <span data-ttu-id="dc9b6-431">returnValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-431">returnValue  \(optional\)</span></span> | [<span data-ttu-id="dc9b6-432">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="dc9b6-432">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="dc9b6-433">O valor que está sendo retornado, se a função estiver no ponto de retorno.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-433">The value being returned, if the function is at return point.</span></span> |  

---  

### <a name="scope-object"></a><span data-ttu-id="dc9b6-434">Objeto Scope</span><span class="sxs-lookup"><span data-stu-id="dc9b6-434">Scope object</span></span>  

<a name="scope"></a>  

<span data-ttu-id="dc9b6-435">Descrição do escopo.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-435">Scope description.</span></span>  

| <span data-ttu-id="dc9b6-436">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dc9b6-436">Properties</span></span> | <span data-ttu-id="dc9b6-437">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-437">Type</span></span> | <span data-ttu-id="dc9b6-438">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dc9b6-438">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="dc9b6-439">tipo</span><span class="sxs-lookup"><span data-stu-id="dc9b6-439">type</span></span> | `string` | <span data-ttu-id="dc9b6-440">Tipo de escopo.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-440">Scope type.</span></span>  <span data-ttu-id="dc9b6-441">Valores permitidos:  `global` , , , , , , , `local` , `with` `closure` `catch` `block` `script` `eval` e</span><span class="sxs-lookup"><span data-stu-id="dc9b6-441">Allowed values:  `global`, `local`, `with`, `closure`, `catch`, `block`, `script`, `eval`, and</span></span> `module` |  
| <span data-ttu-id="dc9b6-442">object</span><span class="sxs-lookup"><span data-stu-id="dc9b6-442">object</span></span> | [<span data-ttu-id="dc9b6-443">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="dc9b6-443">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="dc9b6-444">Objeto que representa o escopo.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-444">Object representing the scope.</span></span>  <span data-ttu-id="dc9b6-445">Para e escopos ele representa o objeto real; para o restante dos escopos, ele é `global` objeto transitório artificial enumerando variáveis de escopo `with` como suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-445">For `global` and `with` scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span> |  
| <span data-ttu-id="dc9b6-446">nome \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-446">name  \(optional\)</span></span> | `string` | &nbsp; |  
| <span data-ttu-id="dc9b6-447">startLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-447">startLocation  \(optional\)</span></span> | [<span data-ttu-id="dc9b6-448">Location</span><span class="sxs-lookup"><span data-stu-id="dc9b6-448">Location</span></span>](#location) | <span data-ttu-id="dc9b6-449">Local no código-fonte onde o escopo é iniciado.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-449">Location in the source code where scope starts.</span></span> |  
| <span data-ttu-id="dc9b6-450">endLocation \(optional\)</span><span class="sxs-lookup"><span data-stu-id="dc9b6-450">endLocation  \(optional\)</span></span> | [<span data-ttu-id="dc9b6-451">Location</span><span class="sxs-lookup"><span data-stu-id="dc9b6-451">Location</span></span>](#location) | <span data-ttu-id="dc9b6-452">Local no código-fonte onde o escopo termina.</span><span class="sxs-lookup"><span data-stu-id="dc9b6-452">Location in the source code where scope ends.</span></span> |  

---  

## <a name="dependencies"></a><span data-ttu-id="dc9b6-453">Dependências</span><span class="sxs-lookup"><span data-stu-id="dc9b6-453">Dependencies</span></span>  

[<span data-ttu-id="dc9b6-454">Tempo de Execução</span><span class="sxs-lookup"><span data-stu-id="dc9b6-454">Runtime</span></span>](./runtime.md)  
