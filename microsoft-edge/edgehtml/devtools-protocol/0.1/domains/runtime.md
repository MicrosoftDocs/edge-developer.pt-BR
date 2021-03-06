---
description: Referência do Protocolo DevTools Versão 0.1 (EdgeHTML) para o Domínio do Tempo de Execução.  O domínio de tempo de execução expõe o tempo de execução do JavaScript por meio de objetos de avaliação remota e espelho.  Os resultados da avaliação são retornados como objeto espelho que expõe o tipo de objeto, a representação de cadeia de caracteres e o identificador exclusivo que pode ser usado para referência de objeto posterior.  Os objetos originais são mantidos na memória, a menos que sejam lançados explicitamente.
title: Domínio do tempo de execução - DevTools Protocol Versão 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9aa87c1c289452844ef3442811f84881fc752b4
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397689"
---
# <a name="runtime-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="ffc09-106">Domínio do tempo de execução - DevTools Protocol Versão 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="ffc09-106">Runtime Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="ffc09-107">O domínio de tempo de execução expõe o tempo de execução do JavaScript por meio de objetos de avaliação remota e espelho.</span><span class="sxs-lookup"><span data-stu-id="ffc09-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span>  <span data-ttu-id="ffc09-108">Os resultados da avaliação são retornados como objeto espelho que expõe o tipo de objeto, a representação de cadeia de caracteres e o identificador exclusivo que pode ser usado para referência de objeto posterior.</span><span class="sxs-lookup"><span data-stu-id="ffc09-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span>  <span data-ttu-id="ffc09-109">Os objetos originais são mantidos na memória, a menos que sejam lançados explicitamente.</span><span class="sxs-lookup"><span data-stu-id="ffc09-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>  

| <span data-ttu-id="ffc09-110">Classificação</span><span class="sxs-lookup"><span data-stu-id="ffc09-110">Classification</span></span> | <span data-ttu-id="ffc09-111">Membros</span><span class="sxs-lookup"><span data-stu-id="ffc09-111">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="ffc09-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ffc09-112">Methods</span></span>](#methods) | <span data-ttu-id="ffc09-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span><span class="sxs-lookup"><span data-stu-id="ffc09-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span></span> |  
| [<span data-ttu-id="ffc09-114">Eventos</span><span class="sxs-lookup"><span data-stu-id="ffc09-114">Events</span></span>](#events) | <span data-ttu-id="ffc09-115">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span><span class="sxs-lookup"><span data-stu-id="ffc09-115">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span></span> |  
| [<span data-ttu-id="ffc09-116">Tipos</span><span class="sxs-lookup"><span data-stu-id="ffc09-116">Types</span></span>](#types) | <span data-ttu-id="ffc09-117">[ScriptId,](#scriptid) [RemoteObjectId,](#remoteobjectid) [UnserializableValue,](#unserializablevalue) [RemoteObject,](#remoteobject) [PropertyDescriptor,](#propertydescriptor) [CallArgument,](#callargument) [ExecutionContextId,](#executioncontextid) [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="ffc09-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |  

## <a name="methods"></a><span data-ttu-id="ffc09-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="ffc09-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="ffc09-119">Habilitar</span><span class="sxs-lookup"><span data-stu-id="ffc09-119">enable</span></span>  

<span data-ttu-id="ffc09-120">Habilita o relatório do `executionContextsCleared` evento.</span><span class="sxs-lookup"><span data-stu-id="ffc09-120">Enables reporting of the `executionContextsCleared` event.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="ffc09-121">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="ffc09-121">disable</span></span>  

<span data-ttu-id="ffc09-122">Desabilita o relatório do `executionContextsCleared` evento.</span><span class="sxs-lookup"><span data-stu-id="ffc09-122">Disables reporting of the `executionContextsCleared` event.</span></span>  

&nbsp;  

---  

### <a name="evaluate"></a><span data-ttu-id="ffc09-123">evaluate</span><span class="sxs-lookup"><span data-stu-id="ffc09-123">evaluate</span></span>  

<span data-ttu-id="ffc09-124">Avalia a expressão no objeto global.</span><span class="sxs-lookup"><span data-stu-id="ffc09-124">Evaluates expression on global object.</span></span>  

| <span data-ttu-id="ffc09-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ffc09-125">Parameters</span></span> | <span data-ttu-id="ffc09-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffc09-126">Type</span></span> | <span data-ttu-id="ffc09-127">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ffc09-127">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ffc09-128">expressão</span><span class="sxs-lookup"><span data-stu-id="ffc09-128">expression</span></span> | `string` | <span data-ttu-id="ffc09-129">Expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="ffc09-129">Expression to evaluate.</span></span> |  
| <span data-ttu-id="ffc09-130">silent \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-130">silent \(optional\)</span></span> | `boolean` | <span data-ttu-id="ffc09-131">No modo silencioso, as exceções lançadas durante a avaliação não são relatadas e não pausam a execução.</span><span class="sxs-lookup"><span data-stu-id="ffc09-131">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span>  <span data-ttu-id="ffc09-132">Substitui o `setPauseOnException` estado.</span><span class="sxs-lookup"><span data-stu-id="ffc09-132">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="ffc09-133">contextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-133">contextId \(optional\)</span></span> | [<span data-ttu-id="ffc09-134">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="ffc09-134">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="ffc09-135">Especifica em qual contexto de execução executar a avaliação.</span><span class="sxs-lookup"><span data-stu-id="ffc09-135">Specifies in which execution context to perform evaluation.</span></span>  <span data-ttu-id="ffc09-136">Se o parâmetro for omitido, a avaliação será executada no contexto da página inspecionada.</span><span class="sxs-lookup"><span data-stu-id="ffc09-136">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span> |  
| <span data-ttu-id="ffc09-137">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-137">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="ffc09-138">Se o resultado é esperado para ser um objeto JSON que deve ser enviado por valor.</span><span class="sxs-lookup"><span data-stu-id="ffc09-138">Whether the result is expected to be a JSON object that should be sent by value.</span></span> |  
| <span data-ttu-id="ffc09-139">awaitPromise \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-139">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="ffc09-140">Se a execução `await` deve para o valor resultante e retornar uma vez que a promessa esperada for resolvida.</span><span class="sxs-lookup"><span data-stu-id="ffc09-140">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  

| <span data-ttu-id="ffc09-141">Retorna</span><span class="sxs-lookup"><span data-stu-id="ffc09-141">Returns</span></span> | <span data-ttu-id="ffc09-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffc09-142">Type</span></span> | <span data-ttu-id="ffc09-143">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ffc09-143">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ffc09-144">result</span><span class="sxs-lookup"><span data-stu-id="ffc09-144">result</span></span> | [<span data-ttu-id="ffc09-145">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="ffc09-145">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="ffc09-146">Resultado da avaliação.</span><span class="sxs-lookup"><span data-stu-id="ffc09-146">Evaluation result.</span></span> |  

---  

### <a name="callfunctionon"></a><span data-ttu-id="ffc09-147">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="ffc09-147">callFunctionOn</span></span>  

<span data-ttu-id="ffc09-148">Função Calls com determinada declaração no objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="ffc09-148">Calls function with given declaration on the given object.</span></span>  <span data-ttu-id="ffc09-149">O grupo de objetos do resultado é herdado do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="ffc09-149">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="ffc09-150">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ffc09-150">Parameters</span></span> | <span data-ttu-id="ffc09-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffc09-151">Type</span></span> | <span data-ttu-id="ffc09-152">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ffc09-152">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ffc09-153">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="ffc09-153">functionDeclaration</span></span> | `string` | <span data-ttu-id="ffc09-154">Declaração da função a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="ffc09-154">Declaration of the function to call.</span></span> |  
| <span data-ttu-id="ffc09-155">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-155">objectId \(optional\)</span></span> | [<span data-ttu-id="ffc09-156">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="ffc09-156">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="ffc09-157">Identificador da função de chamada do objeto.</span><span class="sxs-lookup"><span data-stu-id="ffc09-157">Identifier of the object to call function on.</span></span>  <span data-ttu-id="ffc09-158">Ou `objectId` `executionContextId` deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="ffc09-158">Either `objectId` or `executionContextId` should be specified.</span></span>  <span data-ttu-id="ffc09-159">objectId deve ser da função Runtime.evaluate().</span><span class="sxs-lookup"><span data-stu-id="ffc09-159">objectId must be from the Runtime.evaluate() function.</span></span> |  
| <span data-ttu-id="ffc09-160">argumentos \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-160">arguments \(optional\)</span></span> | [<span data-ttu-id="ffc09-161">CallArgument[]</span><span class="sxs-lookup"><span data-stu-id="ffc09-161">CallArgument[]</span></span>](#callargument) | <span data-ttu-id="ffc09-162">Argumentos de chamada.</span><span class="sxs-lookup"><span data-stu-id="ffc09-162">Call arguments.</span></span>  <span data-ttu-id="ffc09-163">Todos os argumentos de chamada devem pertencer ao mesmo mundo JavaScript que o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="ffc09-163">All call arguments must belong to the same JavaScript world as the target object.</span></span> |  
| <span data-ttu-id="ffc09-164">silent \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-164">silent \(optional\)</span></span> | `boolean` | <span data-ttu-id="ffc09-165">No modo silencioso, as exceções lançadas durante a avaliação não são relatadas e não pausam a execução.</span><span class="sxs-lookup"><span data-stu-id="ffc09-165">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span>  <span data-ttu-id="ffc09-166">Substitui o `setPauseOnException` estado.</span><span class="sxs-lookup"><span data-stu-id="ffc09-166">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="ffc09-167">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-167">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="ffc09-168">Se o resultado é esperado para ser um objeto JSON que deve ser enviado por valor.</span><span class="sxs-lookup"><span data-stu-id="ffc09-168">Whether the result is expected to be a JSON object which should be sent by value.</span></span> |  
| <span data-ttu-id="ffc09-169">awaitPromise \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-169">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="ffc09-170">Se a execução `await` deve para o valor resultante e retornar uma vez que a promessa esperada for resolvida.</span><span class="sxs-lookup"><span data-stu-id="ffc09-170">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  

| <span data-ttu-id="ffc09-171">Retorna</span><span class="sxs-lookup"><span data-stu-id="ffc09-171">Returns</span></span> | <span data-ttu-id="ffc09-172">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffc09-172">Type</span></span> | <span data-ttu-id="ffc09-173">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ffc09-173">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ffc09-174">result</span><span class="sxs-lookup"><span data-stu-id="ffc09-174">result</span></span> | [<span data-ttu-id="ffc09-175">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="ffc09-175">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="ffc09-176">Resultado da chamada.</span><span class="sxs-lookup"><span data-stu-id="ffc09-176">Call result.</span></span> |  

---  

### <a name="getproperties"></a><span data-ttu-id="ffc09-177">getProperties</span><span class="sxs-lookup"><span data-stu-id="ffc09-177">getProperties</span></span>  

<span data-ttu-id="ffc09-178">Retorna propriedades de um determinado objeto.</span><span class="sxs-lookup"><span data-stu-id="ffc09-178">Returns properties of a given object.</span></span>  <span data-ttu-id="ffc09-179">O grupo de objetos do resultado é herdado do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="ffc09-179">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="ffc09-180">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ffc09-180">Parameters</span></span> | <span data-ttu-id="ffc09-181">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffc09-181">Type</span></span> | <span data-ttu-id="ffc09-182">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ffc09-182">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ffc09-183">objectId</span><span class="sxs-lookup"><span data-stu-id="ffc09-183">objectId</span></span> | [<span data-ttu-id="ffc09-184">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="ffc09-184">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="ffc09-185">Identificador do objeto para o que retornar propriedades.</span><span class="sxs-lookup"><span data-stu-id="ffc09-185">Identifier of the object to return properties for.</span></span>  `objectId` <span data-ttu-id="ffc09-186">deve ser da `Debugger.evaluateOnCallFrame()` função.</span><span class="sxs-lookup"><span data-stu-id="ffc09-186">must be from the `Debugger.evaluateOnCallFrame()` function.</span></span> |  
| <span data-ttu-id="ffc09-187">ownProperties \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-187">ownProperties \(optional\)</span></span> | `boolean` | <span data-ttu-id="ffc09-188">Se `true` , retorna propriedades pertencentes apenas ao elemento em si, não à cadeia de protótipos.</span><span class="sxs-lookup"><span data-stu-id="ffc09-188">If `true`, returns properties belonging only to the element itself, not to its prototype chain.</span></span> |  
| <span data-ttu-id="ffc09-189">accessorPropertiesOnly \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-189">accessorPropertiesOnly \(optional\)</span></span> | `boolean` | <span data-ttu-id="ffc09-190">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="ffc09-190">**Experimental**.</span></span>  <span data-ttu-id="ffc09-191">Se `true` , retorna propriedades do acessador \(somente com getter/setter\) ; as propriedades internas também não são retornadas.</span><span class="sxs-lookup"><span data-stu-id="ffc09-191">If `true`, returns accessor properties \(with getter/setter\) only; internal properties are not returned either.</span></span> |  

| <span data-ttu-id="ffc09-192">Retorna</span><span class="sxs-lookup"><span data-stu-id="ffc09-192">Returns</span></span> | <span data-ttu-id="ffc09-193">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffc09-193">Type</span></span> | <span data-ttu-id="ffc09-194">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ffc09-194">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ffc09-195">result</span><span class="sxs-lookup"><span data-stu-id="ffc09-195">result</span></span> | [<span data-ttu-id="ffc09-196">PropertyDescriptor[]</span><span class="sxs-lookup"><span data-stu-id="ffc09-196">PropertyDescriptor[]</span></span>](#propertydescriptor) | <span data-ttu-id="ffc09-197">Propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="ffc09-197">Object properties.</span></span> |  

---  

## <a name="events"></a><span data-ttu-id="ffc09-198">Eventos</span><span class="sxs-lookup"><span data-stu-id="ffc09-198">Events</span></span>  

### <a name="executioncontextscleared"></a><span data-ttu-id="ffc09-199">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="ffc09-199">executionContextsCleared</span></span>  

<span data-ttu-id="ffc09-200">Emitido quando todos os executionContexts foram limpos no navegador.</span><span class="sxs-lookup"><span data-stu-id="ffc09-200">Issued when all executionContexts were cleared in browser.</span></span>  

&nbsp;  

---  

### <a name="exceptionthrown"></a><span data-ttu-id="ffc09-201">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="ffc09-201">exceptionThrown</span></span>  

<span data-ttu-id="ffc09-202">Emitido quando a exceção foi lançada e não foi acionada.</span><span class="sxs-lookup"><span data-stu-id="ffc09-202">Issued when exception was thrown and unhandled.</span></span>  

| <span data-ttu-id="ffc09-203">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ffc09-203">Parameters</span></span> | <span data-ttu-id="ffc09-204">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffc09-204">Type</span></span> | <span data-ttu-id="ffc09-205">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ffc09-205">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ffc09-206">timestamp</span><span class="sxs-lookup"><span data-stu-id="ffc09-206">timestamp</span></span> | [<span data-ttu-id="ffc09-207">Carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="ffc09-207">Timestamp</span></span>](#timestamp) | <span data-ttu-id="ffc09-208">Timestamp da exceção.</span><span class="sxs-lookup"><span data-stu-id="ffc09-208">Timestamp of the exception.</span></span> |  
| <span data-ttu-id="ffc09-209">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="ffc09-209">exceptionDetails</span></span> | [<span data-ttu-id="ffc09-210">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="ffc09-210">ExceptionDetails</span></span>](#exceptiondetails) | &nbsp; |  

---  

## <a name="types"></a><span data-ttu-id="ffc09-211">Tipos</span><span class="sxs-lookup"><span data-stu-id="ffc09-211">Types</span></span>  

### <a name="scriptid-string"></a><span data-ttu-id="ffc09-212">Cadeia de caracteres ScriptId</span><span class="sxs-lookup"><span data-stu-id="ffc09-212">ScriptId string</span></span>  

<a name="scriptid"></a>  

<span data-ttu-id="ffc09-213">Identificador de script exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ffc09-213">Unique script identifier.</span></span>  

&nbsp;  

---  

### <a name="remoteobjectid-string"></a><span data-ttu-id="ffc09-214">Cadeia de caracteres RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="ffc09-214">RemoteObjectId string</span></span>  

<a name="remoteobjectid"></a>  

<span data-ttu-id="ffc09-215">Identificador de objeto exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ffc09-215">Unique object identifier.</span></span>  

&nbsp;  

---  

### <a name="unserializablevalue-string"></a><span data-ttu-id="ffc09-216">Cadeia de caracteres UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="ffc09-216">UnserializableValue string</span></span>  

<a name="unserializablevalue"></a>  

<span data-ttu-id="ffc09-217">Valor primitivo que não pode ser stringified JSON.</span><span class="sxs-lookup"><span data-stu-id="ffc09-217">Primitive value which cannot be JSON-stringified.</span></span>  

##### <a name="allowed-values"></a><span data-ttu-id="ffc09-218">Valores permitidos</span><span class="sxs-lookup"><span data-stu-id="ffc09-218">Allowed Values</span></span>  

`Infinity`<span data-ttu-id="ffc09-219">, `NaN`, `-Infinity`,</span><span class="sxs-lookup"><span data-stu-id="ffc09-219">, `NaN`, `-Infinity`,</span></span> `-0`  

---  

### <a name="remoteobject-object"></a><span data-ttu-id="ffc09-220">Objeto RemoteObject</span><span class="sxs-lookup"><span data-stu-id="ffc09-220">RemoteObject object</span></span>  

<a name="remoteobject"></a>  

<span data-ttu-id="ffc09-221">Objeto Mirror fazendo referência ao objeto JavaScript original.</span><span class="sxs-lookup"><span data-stu-id="ffc09-221">Mirror object referencing original JavaScript object.</span></span>  

| <span data-ttu-id="ffc09-222">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ffc09-222">Properties</span></span> | <span data-ttu-id="ffc09-223">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffc09-223">Type</span></span> | <span data-ttu-id="ffc09-224">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ffc09-224">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ffc09-225">tipo</span><span class="sxs-lookup"><span data-stu-id="ffc09-225">type</span></span> | `string` | <span data-ttu-id="ffc09-226">Tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="ffc09-226">Object type.</span></span>  <span data-ttu-id="ffc09-227">Valores permitidos:  `object` , , , , , `function` `undefined` `string` `number` `boolean` e</span><span class="sxs-lookup"><span data-stu-id="ffc09-227">Allowed values:  `object`, `function`, `undefined`, `string`, `number`, `boolean`, and</span></span> `symbol` |  
| <span data-ttu-id="ffc09-228">subtipo \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-228">subtype \(optional\)</span></span> | `string` | <span data-ttu-id="ffc09-229">Dica de subtipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="ffc09-229">Object subtype hint.</span></span>  <span data-ttu-id="ffc09-230">Especificado apenas para `object` valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="ffc09-230">Specified for `object` type values only.</span></span>  <span data-ttu-id="ffc09-231">Valores permitidos:  `null` `error` , e</span><span class="sxs-lookup"><span data-stu-id="ffc09-231">Allowed values:  `null`, `error`, and</span></span> `promise` |  
| <span data-ttu-id="ffc09-232">className \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-232">className \(optional\)</span></span> | `string` | <span data-ttu-id="ffc09-233">Nome da classe de objeto \(construtor\).</span><span class="sxs-lookup"><span data-stu-id="ffc09-233">Object class \(constructor\) name.</span></span>  <span data-ttu-id="ffc09-234">Especificado apenas para `object` valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="ffc09-234">Specified for `object` type values only.</span></span> |  
| <span data-ttu-id="ffc09-235">valor \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-235">value \(optional\)</span></span> | `any` | <span data-ttu-id="ffc09-236">Valor do objeto remoto em caso de valores primitivos ou valores JSON \(se foi solicitado\).</span><span class="sxs-lookup"><span data-stu-id="ffc09-236">Remote object value in case of primitive values or JSON values \(if it was requested\).</span></span> |  
| <span data-ttu-id="ffc09-237">unserializableValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-237">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="ffc09-238">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="ffc09-238">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="ffc09-239">O valor primitivo que não pode ser stringified JSON não tem `value` , mas obtém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="ffc09-239">Primitive value which can not be JSON-stringified does not have `value`, but gets this property.</span></span> |  
| <span data-ttu-id="ffc09-240">description \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-240">description \(optional\)</span></span> | `string` | <span data-ttu-id="ffc09-241">Representação de cadeia de caracteres do objeto.</span><span class="sxs-lookup"><span data-stu-id="ffc09-241">String representation of the object.</span></span> |  
| <span data-ttu-id="ffc09-242">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-242">objectId \(optional\)</span></span> | [<span data-ttu-id="ffc09-243">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="ffc09-243">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="ffc09-244">Identificador de objeto exclusivo \(para valores não primitivos\).</span><span class="sxs-lookup"><span data-stu-id="ffc09-244">Unique object identifier \(for non-primitive values\).</span></span> |  
| <span data-ttu-id="ffc09-245">msDebuggerPropertyId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-245">msDebuggerPropertyId \(optional\)</span></span> | `string` | <span data-ttu-id="ffc09-246">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="ffc09-246">**Experimental**.</span></span>  <span data-ttu-id="ffc09-247">Microsoft: A ID da propriedade depurador associada para este objeto.</span><span class="sxs-lookup"><span data-stu-id="ffc09-247">Microsoft:  The associated debugger property ID for this object.</span></span> |  

---  

### <a name="propertydescriptor-object"></a><span data-ttu-id="ffc09-248">Objeto PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="ffc09-248">PropertyDescriptor object</span></span>  

<a name="propertydescriptor"></a>  

<span data-ttu-id="ffc09-249">Descritor da propriedade Object.</span><span class="sxs-lookup"><span data-stu-id="ffc09-249">Object property descriptor.</span></span>  

| <span data-ttu-id="ffc09-250">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ffc09-250">Properties</span></span> | <span data-ttu-id="ffc09-251">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffc09-251">Type</span></span> | <span data-ttu-id="ffc09-252">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ffc09-252">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ffc09-253">name</span><span class="sxs-lookup"><span data-stu-id="ffc09-253">name</span></span> | `string` | <span data-ttu-id="ffc09-254">Nome da propriedade ou descrição de símbolo.</span><span class="sxs-lookup"><span data-stu-id="ffc09-254">Property name or symbol description.</span></span> |  
| <span data-ttu-id="ffc09-255">valor \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-255">value \(optional\)</span></span> | [<span data-ttu-id="ffc09-256">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="ffc09-256">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="ffc09-257">O valor associado à propriedade.</span><span class="sxs-lookup"><span data-stu-id="ffc09-257">The value associated with the property.</span></span> |  
| <span data-ttu-id="ffc09-258">writable \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-258">writable \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="ffc09-259">se o valor associado à propriedade pode ser alterado \(descritores de dados somente\).</span><span class="sxs-lookup"><span data-stu-id="ffc09-259">if the value associated with the property may be changed \(data descriptors only\).</span></span> |  
| <span data-ttu-id="ffc09-260">get \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-260">get \(optional\)</span></span> | [<span data-ttu-id="ffc09-261">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="ffc09-261">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="ffc09-262">Uma função que serve como um getter para a propriedade ou se não houver getter \(descritores do acessador `undefined` somente\).</span><span class="sxs-lookup"><span data-stu-id="ffc09-262">A function which serves as a getter for the property, or `undefined` if there is no getter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="ffc09-263">set \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-263">set \(optional\)</span></span> | [<span data-ttu-id="ffc09-264">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="ffc09-264">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="ffc09-265">Uma função que serve como um setter para a propriedade ou se não houver setter \(descritores do acessador `undefined` somente\).</span><span class="sxs-lookup"><span data-stu-id="ffc09-265">A function which serves as a setter for the property, or `undefined` if there is no setter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="ffc09-266">configurável</span><span class="sxs-lookup"><span data-stu-id="ffc09-266">configurable</span></span> | `boolean` | `True` <span data-ttu-id="ffc09-267">se o tipo desse descritor de propriedade pode ser alterado e se a propriedade pode ser excluída do objeto correspondente.</span><span class="sxs-lookup"><span data-stu-id="ffc09-267">if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span> |  
| <span data-ttu-id="ffc09-268">enumerable</span><span class="sxs-lookup"><span data-stu-id="ffc09-268">enumerable</span></span> | `boolean` | `True` <span data-ttu-id="ffc09-269">se essa propriedade aparecer durante a enumeração das propriedades no objeto correspondente.</span><span class="sxs-lookup"><span data-stu-id="ffc09-269">if this property shows up during enumeration of the properties on the corresponding object.</span></span> |  
| <span data-ttu-id="ffc09-270">wasThrown \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-270">wasThrown \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="ffc09-271">se o resultado foi lançado durante a avaliação.</span><span class="sxs-lookup"><span data-stu-id="ffc09-271">if the result was thrown during the evaluation.</span></span> |  
| <span data-ttu-id="ffc09-272">isOwn \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-272">isOwn \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="ffc09-273">se a propriedade pertence ao objeto.</span><span class="sxs-lookup"><span data-stu-id="ffc09-273">if the property is owned for the object.</span></span> |  
| <span data-ttu-id="ffc09-274">msReturnValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-274">msReturnValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="ffc09-275">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="ffc09-275">**Experimental**.</span></span>  <span data-ttu-id="ffc09-276">Microsoft:  `True` se a propriedade for um valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="ffc09-276">Microsoft:  `True` if the property is a return value.</span></span> |  
| <span data-ttu-id="ffc09-277">símbolo \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-277">symbol \(optional\)</span></span> | [<span data-ttu-id="ffc09-278">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="ffc09-278">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="ffc09-279">Objeto símbolo de propriedade, se a propriedade for do `symbol` tipo.</span><span class="sxs-lookup"><span data-stu-id="ffc09-279">Property symbol object, if the property is of the `symbol` type.</span></span> |  

---  

### <a name="callargument-object"></a><span data-ttu-id="ffc09-280">Objeto CallArgument</span><span class="sxs-lookup"><span data-stu-id="ffc09-280">CallArgument object</span></span>  

<a name="callargument"></a>  

<span data-ttu-id="ffc09-281">Representa o argumento de chamada de função.</span><span class="sxs-lookup"><span data-stu-id="ffc09-281">Represents function call argument.</span></span>  <span data-ttu-id="ffc09-282">A ID do objeto remoto , o valor primitivo `value` inserializável ou nenhum dos \(for undefined\) deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="ffc09-282">Either remote object ID `value`, unserializable primitive value or neither of \(for undefined\) them should be specified.</span></span>  

| <span data-ttu-id="ffc09-283">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ffc09-283">Properties</span></span> | <span data-ttu-id="ffc09-284">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffc09-284">Type</span></span> | <span data-ttu-id="ffc09-285">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ffc09-285">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ffc09-286">valor \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-286">value \(optional\)</span></span> | `any` | <span data-ttu-id="ffc09-287">Valor primitivo ou objeto javascript serializable.</span><span class="sxs-lookup"><span data-stu-id="ffc09-287">Primitive value or serializable javascript object.</span></span> |  
| <span data-ttu-id="ffc09-288">unserializableValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-288">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="ffc09-289">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="ffc09-289">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="ffc09-290">Valor primitivo que não pode ser stringified JSON.</span><span class="sxs-lookup"><span data-stu-id="ffc09-290">Primitive value which can not be JSON-stringified.</span></span> |  
| <span data-ttu-id="ffc09-291">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-291">objectId \(optional\)</span></span> | [<span data-ttu-id="ffc09-292">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="ffc09-292">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="ffc09-293">Identificador de objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="ffc09-293">Remote object handle.</span></span> |  

---  

### <a name="executioncontextid-integer"></a><span data-ttu-id="ffc09-294">ExecutionContextId integer</span><span class="sxs-lookup"><span data-stu-id="ffc09-294">ExecutionContextId integer</span></span>  

<a name="executioncontextid"></a>  

<span data-ttu-id="ffc09-295">ID de um contexto de execução.</span><span class="sxs-lookup"><span data-stu-id="ffc09-295">ID of an execution context.</span></span>  

&nbsp;  

---  

### <a name="exceptiondetails-object"></a><span data-ttu-id="ffc09-296">Objeto ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="ffc09-296">ExceptionDetails object</span></span>  

<a name="exceptiondetails"></a>  

<span data-ttu-id="ffc09-297">Informações detalhadas sobre exceção \(ou error\) que foram lançadas durante a compilação ou execução do script.</span><span class="sxs-lookup"><span data-stu-id="ffc09-297">Detailed information about exception \(or error\) that was thrown during script compilation or execution.</span></span>  

| <span data-ttu-id="ffc09-298">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ffc09-298">Properties</span></span> | <span data-ttu-id="ffc09-299">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffc09-299">Type</span></span> | <span data-ttu-id="ffc09-300">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ffc09-300">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ffc09-301">exceptionId</span><span class="sxs-lookup"><span data-stu-id="ffc09-301">exceptionId</span></span> | `integer` | <span data-ttu-id="ffc09-302">ID de exceção.</span><span class="sxs-lookup"><span data-stu-id="ffc09-302">Exception ID.</span></span> |  
| <span data-ttu-id="ffc09-303">texto</span><span class="sxs-lookup"><span data-stu-id="ffc09-303">text</span></span> | `string` | <span data-ttu-id="ffc09-304">Texto de exceção, que deve ser usado junto com o objeto exception quando disponível.</span><span class="sxs-lookup"><span data-stu-id="ffc09-304">Exception text, which should be used together with exception object when available.</span></span> |  
| <span data-ttu-id="ffc09-305">lineNumber</span><span class="sxs-lookup"><span data-stu-id="ffc09-305">lineNumber</span></span> | `integer` | <span data-ttu-id="ffc09-306">Número de linha do local de exceção \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="ffc09-306">Line number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="ffc09-307">columnNumber</span><span class="sxs-lookup"><span data-stu-id="ffc09-307">columnNumber</span></span> | `integer` | <span data-ttu-id="ffc09-308">Número da coluna do local de exceção \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="ffc09-308">Column number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="ffc09-309">scriptId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-309">scriptId \(optional\)</span></span> | [<span data-ttu-id="ffc09-310">ScriptId</span><span class="sxs-lookup"><span data-stu-id="ffc09-310">ScriptId</span></span>](#scriptid) | <span data-ttu-id="ffc09-311">ID do script do local de exceção.</span><span class="sxs-lookup"><span data-stu-id="ffc09-311">Script ID of the exception location.</span></span> |  
| <span data-ttu-id="ffc09-312">url \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-312">url \(optional\)</span></span> | `string` | <span data-ttu-id="ffc09-313">URL do local de exceção, a ser usada quando o script não foi relatado.</span><span class="sxs-lookup"><span data-stu-id="ffc09-313">URL of the exception location, to be used when the script was not reported.</span></span> |  
| <span data-ttu-id="ffc09-314">stackTrace \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-314">stackTrace \(optional\)</span></span> | [<span data-ttu-id="ffc09-315">StackTrace</span><span class="sxs-lookup"><span data-stu-id="ffc09-315">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="ffc09-316">Rastreamento de pilha JavaScript, se disponível.</span><span class="sxs-lookup"><span data-stu-id="ffc09-316">JavaScript stack trace if available.</span></span> |  
| <span data-ttu-id="ffc09-317">exception \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-317">exception \(optional\)</span></span> | [<span data-ttu-id="ffc09-318">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="ffc09-318">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="ffc09-319">Objeto Exception, se disponível.</span><span class="sxs-lookup"><span data-stu-id="ffc09-319">Exception object if available.</span></span> |  
| <span data-ttu-id="ffc09-320">executionContextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-320">executionContextId \(optional\)</span></span> | [<span data-ttu-id="ffc09-321">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="ffc09-321">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="ffc09-322">Identificador do contexto em que a exceção aconteceu.</span><span class="sxs-lookup"><span data-stu-id="ffc09-322">Identifier of the context where exception happened.</span></span> |  

---  

### <a name="timestamp-integer"></a><span data-ttu-id="ffc09-323">Número inteiro do timestamp</span><span class="sxs-lookup"><span data-stu-id="ffc09-323">Timestamp integer</span></span>  

<a name="timestamp"></a>  

<span data-ttu-id="ffc09-324">Número de milissegundos desde a época.</span><span class="sxs-lookup"><span data-stu-id="ffc09-324">Number of milliseconds since epoch.</span></span>  

&nbsp;  

---  

### <a name="callframe-object"></a><span data-ttu-id="ffc09-325">Objeto CallFrame</span><span class="sxs-lookup"><span data-stu-id="ffc09-325">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="ffc09-326">Entrada de pilha para erros e declarações de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="ffc09-326">Stack entry for runtime errors and assertions.</span></span>  

| <span data-ttu-id="ffc09-327">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ffc09-327">Properties</span></span> | <span data-ttu-id="ffc09-328">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffc09-328">Type</span></span> | <span data-ttu-id="ffc09-329">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ffc09-329">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ffc09-330">functionName</span><span class="sxs-lookup"><span data-stu-id="ffc09-330">functionName</span></span> | `string` | <span data-ttu-id="ffc09-331">Nome da função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ffc09-331">JavaScript function name.</span></span> |  
| <span data-ttu-id="ffc09-332">scriptId</span><span class="sxs-lookup"><span data-stu-id="ffc09-332">scriptId</span></span> | [<span data-ttu-id="ffc09-333">ScriptId</span><span class="sxs-lookup"><span data-stu-id="ffc09-333">ScriptId</span></span>](#scriptid) | <span data-ttu-id="ffc09-334">ID de script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ffc09-334">JavaScript script ID.</span></span> |  
| <span data-ttu-id="ffc09-335">url</span><span class="sxs-lookup"><span data-stu-id="ffc09-335">url</span></span> | `string` | <span data-ttu-id="ffc09-336">Nome ou url do script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ffc09-336">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="ffc09-337">lineNumber</span><span class="sxs-lookup"><span data-stu-id="ffc09-337">lineNumber</span></span> | `integer` | <span data-ttu-id="ffc09-338">Número da linha de script JavaScript \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="ffc09-338">JavaScript script line number \(0-based\).</span></span> |  
| <span data-ttu-id="ffc09-339">columnNumber</span><span class="sxs-lookup"><span data-stu-id="ffc09-339">columnNumber</span></span> | `integer` | <span data-ttu-id="ffc09-340">Número da coluna de script JavaScript \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="ffc09-340">JavaScript script column number \(0-based\).</span></span> |  

---  

### <a name="stacktrace-object"></a><span data-ttu-id="ffc09-341">Objeto StackTrace</span><span class="sxs-lookup"><span data-stu-id="ffc09-341">StackTrace object</span></span>  

<a name="stacktrace"></a>  

<span data-ttu-id="ffc09-342">Quadros de chamada para declarações ou mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="ffc09-342">Call frames for assertions or error messages.</span></span>  

| <span data-ttu-id="ffc09-343">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ffc09-343">Properties</span></span> | <span data-ttu-id="ffc09-344">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffc09-344">Type</span></span> | <span data-ttu-id="ffc09-345">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ffc09-345">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="ffc09-346">description \(optional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-346">description \(optional\)</span></span> | `string` | <span data-ttu-id="ffc09-347">Rótulo de cadeia de caracteres desse rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="ffc09-347">String label of this stack trace.</span></span>  <span data-ttu-id="ffc09-348">Para rastreamentos assíncrono, pode ser um nome da função que iniciou a chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="ffc09-348">For async traces this may be a name of the function that initiated the async call.</span></span> |  
| <span data-ttu-id="ffc09-349">callFrames</span><span class="sxs-lookup"><span data-stu-id="ffc09-349">callFrames</span></span> | [<span data-ttu-id="ffc09-350">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="ffc09-350">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="ffc09-351">Nome da função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ffc09-351">JavaScript function name.</span></span> |  
| <span data-ttu-id="ffc09-352">pai \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="ffc09-352">parent \(optional\)</span></span> | [<span data-ttu-id="ffc09-353">StackTrace</span><span class="sxs-lookup"><span data-stu-id="ffc09-353">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="ffc09-354">Rastreamento de pilha JavaScript assíncrono que precedeu essa pilha, se disponível.</span><span class="sxs-lookup"><span data-stu-id="ffc09-354">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span> |  

---  
