---
description: Referência do Protocolo DevTools Versão 0.2 (EdgeHTML) para o Domínio do Tempo de Execução. O domínio de tempo de execução expõe o tempo de execução do JavaScript por meio de objetos de avaliação remota e espelho. Os resultados da avaliação são retornados como objeto espelho que expõe o tipo de objeto, a representação de cadeia de caracteres e o identificador exclusivo que pode ser usado para referência de objeto posterior. Os objetos originais são mantidos na memória, a menos que sejam lançados explicitamente.
title: Domínio do tempo de execução - DevTools Protocol Versão 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: afc79a17c5002f60806872a9add57f518ff6cb45
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398137"
---
# <a name="runtime-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="0ad71-106">Domínio do tempo de execução - DevTools Protocol Versão 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="0ad71-106">Runtime Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="0ad71-107">O domínio de tempo de execução expõe o tempo de execução do JavaScript por meio de objetos de avaliação remota e espelho.</span><span class="sxs-lookup"><span data-stu-id="0ad71-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="0ad71-108">Os resultados da avaliação são retornados como objeto espelho que expõe o tipo de objeto, a representação de cadeia de caracteres e o identificador exclusivo que pode ser usado para referência de objeto posterior.</span><span class="sxs-lookup"><span data-stu-id="0ad71-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="0ad71-109">Os objetos originais são mantidos na memória, a menos que sejam lançados explicitamente.</span><span class="sxs-lookup"><span data-stu-id="0ad71-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>  

| <span data-ttu-id="0ad71-110">Classificação</span><span class="sxs-lookup"><span data-stu-id="0ad71-110">Classification</span></span> | <span data-ttu-id="0ad71-111">Membros</span><span class="sxs-lookup"><span data-stu-id="0ad71-111">Members</span></span> |  
|:--- |:--- |  
| [**<span data-ttu-id="0ad71-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="0ad71-112">Methods</span></span>**](#methods) | <span data-ttu-id="0ad71-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span><span class="sxs-lookup"><span data-stu-id="0ad71-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span></span> |  
| [**<span data-ttu-id="0ad71-114">Eventos</span><span class="sxs-lookup"><span data-stu-id="0ad71-114">Events</span></span>**](#events) | <span data-ttu-id="0ad71-115">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span><span class="sxs-lookup"><span data-stu-id="0ad71-115">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span></span> |  
| [**<span data-ttu-id="0ad71-116">Tipos</span><span class="sxs-lookup"><span data-stu-id="0ad71-116">Types</span></span>**](#types) | <span data-ttu-id="0ad71-117">[ScriptId,](#scriptid) [RemoteObjectId,](#remoteobjectid) [UnserializableValue,](#unserializablevalue) [RemoteObject,](#remoteobject) [PropertyDescriptor,](#propertydescriptor) [CallArgument,](#callargument) [ExecutionContextId,](#executioncontextid) [ExecutionContextDescription,](#executioncontextdescription) [ExceptionDetails](#exceptiondetails), [Timestamp,](#timestamp) [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="0ad71-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |  

## <a name="methods"></a><span data-ttu-id="0ad71-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="0ad71-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="0ad71-119">Habilitar</span><span class="sxs-lookup"><span data-stu-id="0ad71-119">enable</span></span>  

<span data-ttu-id="0ad71-120">Habilita o relatório `executionContextCreated` de `executionContextDestroyed` , e `executionContextsCleared` eventos.</span><span class="sxs-lookup"><span data-stu-id="0ad71-120">Enables reporting of the `executionContextCreated`, `executionContextDestroyed`, and `executionContextsCleared` events.</span></span>  <span data-ttu-id="0ad71-121">Quando o relatório for habilitado, `executionContextCreated` o evento será enviado imediatamente para cada contexto de execução existente.</span><span class="sxs-lookup"><span data-stu-id="0ad71-121">When the reporting gets enabled the `executionContextCreated` event will be sent immediately for each existing execution context.</span></span>  

---  

### <a name="disable"></a><span data-ttu-id="0ad71-122">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="0ad71-122">disable</span></span>  

<span data-ttu-id="0ad71-123">Desabilita o relatório `executionContextCreated` de `executionContextDestroyed` , e `executionContextsCleared` eventos.</span><span class="sxs-lookup"><span data-stu-id="0ad71-123">Disables reporting of the `executionContextCreated`, `executionContextDestroyed`, and `executionContextsCleared` events.</span></span>  

---  

### <a name="evaluate"></a><span data-ttu-id="0ad71-124">evaluate</span><span class="sxs-lookup"><span data-stu-id="0ad71-124">evaluate</span></span>  

<span data-ttu-id="0ad71-125">Avalia a expressão no objeto global.</span><span class="sxs-lookup"><span data-stu-id="0ad71-125">Evaluates expression on global object.</span></span>  

| <span data-ttu-id="0ad71-126">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ad71-126">Parameters</span></span> | <span data-ttu-id="0ad71-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-127">Type</span></span> | <span data-ttu-id="0ad71-128">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-128">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-129">expressão</span><span class="sxs-lookup"><span data-stu-id="0ad71-129">expression</span></span> | `string` | <span data-ttu-id="0ad71-130">Expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="0ad71-130">Expression to evaluate.</span></span> |  
| <span data-ttu-id="0ad71-131">includeCommandLineAPI \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-131">includeCommandLineAPI \(optional\)</span></span> | `boolean` | <span data-ttu-id="0ad71-132">Determina se a API de Linha de Comando deve estar disponível durante a avaliação.</span><span class="sxs-lookup"><span data-stu-id="0ad71-132">Determines whether Command Line API should be available during the evaluation.</span></span> |  
| <span data-ttu-id="0ad71-133">objectGroup \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-133">objectGroup \(optional\)</span></span> | `string` | <span data-ttu-id="0ad71-134">Nome de grupo simbólico que pode ser usado para liberar vários objetos.</span><span class="sxs-lookup"><span data-stu-id="0ad71-134">Symbolic group name that can be used to release multiple objects.</span></span> |  
| <span data-ttu-id="0ad71-135">silent \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-135">silent \(optional\)</span></span> | `boolean` | <span data-ttu-id="0ad71-136">No modo silencioso, as exceções lançadas durante a avaliação não são relatadas e não pausam a execução.</span><span class="sxs-lookup"><span data-stu-id="0ad71-136">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span>  <span data-ttu-id="0ad71-137">Substitui o `setPauseOnException` estado.</span><span class="sxs-lookup"><span data-stu-id="0ad71-137">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="0ad71-138">contextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-138">contextId \(optional\)</span></span> | [<span data-ttu-id="0ad71-139">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="0ad71-139">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="0ad71-140">Especifica em qual contexto de execução executar a avaliação.</span><span class="sxs-lookup"><span data-stu-id="0ad71-140">Specifies in which execution context to perform evaluation.</span></span>  <span data-ttu-id="0ad71-141">Se o parâmetro for omitido, a avaliação será executada no contexto da página inspecionada.</span><span class="sxs-lookup"><span data-stu-id="0ad71-141">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span> |  
| <span data-ttu-id="0ad71-142">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-142">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="0ad71-143">Se o resultado é esperado para ser um objeto JSON que deve ser enviado por valor.</span><span class="sxs-lookup"><span data-stu-id="0ad71-143">Whether the result is expected to be a JSON object that should be sent by value.</span></span> |  
| <span data-ttu-id="0ad71-144">awaitPromise \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-144">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="0ad71-145">Se a execução `await` deve para o valor resultante e retornar uma vez que a promessa esperada for resolvida.</span><span class="sxs-lookup"><span data-stu-id="0ad71-145">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  

| <span data-ttu-id="0ad71-146">Retorna</span><span class="sxs-lookup"><span data-stu-id="0ad71-146">Returns</span></span> | <span data-ttu-id="0ad71-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-147">Type</span></span> | <span data-ttu-id="0ad71-148">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-148">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-149">result</span><span class="sxs-lookup"><span data-stu-id="0ad71-149">result</span></span> | [<span data-ttu-id="0ad71-150">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0ad71-150">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="0ad71-151">Resultado da avaliação.</span><span class="sxs-lookup"><span data-stu-id="0ad71-151">Evaluation result.</span></span> |  

---  

### <a name="callfunctionon"></a><span data-ttu-id="0ad71-152">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="0ad71-152">callFunctionOn</span></span>  

<span data-ttu-id="0ad71-153">Função Calls com determinada declaração no objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="0ad71-153">Calls function with given declaration on the given object.</span></span>  <span data-ttu-id="0ad71-154">O grupo de objetos do resultado é herdado do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="0ad71-154">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="0ad71-155">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ad71-155">Parameters</span></span> | <span data-ttu-id="0ad71-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-156">Type</span></span> | <span data-ttu-id="0ad71-157">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-157">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-158">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="0ad71-158">functionDeclaration</span></span> | `string` | <span data-ttu-id="0ad71-159">Declaração da função a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="0ad71-159">Declaration of the function to call.</span></span> |  
| <span data-ttu-id="0ad71-160">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-160">objectId \(optional\)</span></span> | [<span data-ttu-id="0ad71-161">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="0ad71-161">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="0ad71-162">Identificador da função de chamada do objeto.</span><span class="sxs-lookup"><span data-stu-id="0ad71-162">Identifier of the object to call function on.</span></span>  <span data-ttu-id="0ad71-163">Ou `objectId` `executionContextId` deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="0ad71-163">Either `objectId` or `executionContextId` should be specified.</span></span>  `objectId` <span data-ttu-id="0ad71-164">deve ser da `Runtime.evaluate()` função.</span><span class="sxs-lookup"><span data-stu-id="0ad71-164">must be from the `Runtime.evaluate()` function.</span></span> |  
| <span data-ttu-id="0ad71-165">argumentos \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-165">arguments \(optional\)</span></span> | [<span data-ttu-id="0ad71-166">CallArgument[]</span><span class="sxs-lookup"><span data-stu-id="0ad71-166">CallArgument[]</span></span>](#callargument) | <span data-ttu-id="0ad71-167">Argumentos de chamada.</span><span class="sxs-lookup"><span data-stu-id="0ad71-167">Call arguments.</span></span>  <span data-ttu-id="0ad71-168">Todos os argumentos de chamada devem pertencer ao mesmo mundo JavaScript que o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="0ad71-168">All call arguments must belong to the same JavaScript world as the target object.</span></span> |  
| <span data-ttu-id="0ad71-169">booleano \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-169">boolean \(optional\)</span></span> | `boolean` | <span data-ttu-id="0ad71-170">No modo silencioso, as exceções lançadas durante a avaliação não são relatadas e não pausam a execução.</span><span class="sxs-lookup"><span data-stu-id="0ad71-170">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="0ad71-171">Substitui o `setPauseOnException` estado.</span><span class="sxs-lookup"><span data-stu-id="0ad71-171">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="0ad71-172">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-172">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="0ad71-173">Se o resultado é esperado para ser um objeto JSON que deve ser enviado por valor.</span><span class="sxs-lookup"><span data-stu-id="0ad71-173">Whether the result is expected to be a JSON object which should be sent by value.</span></span> |  
| <span data-ttu-id="0ad71-174">awaitPromise \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-174">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="0ad71-175">Se a execução `await` deve para o valor resultante e retornar uma vez que a promessa esperada for resolvida.</span><span class="sxs-lookup"><span data-stu-id="0ad71-175">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  
| <span data-ttu-id="0ad71-176">executionContextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-176">executionContextId \(optional\)</span></span> | [<span data-ttu-id="0ad71-177">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="0ad71-177">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="0ad71-178">Especifica o contexto de execução em que objeto global será usado para chamar a função.</span><span class="sxs-lookup"><span data-stu-id="0ad71-178">Specifies execution context which global object will be used to call function on.</span></span>  <span data-ttu-id="0ad71-179">Qualquer um dos dois</span><span class="sxs-lookup"><span data-stu-id="0ad71-179">Either</span></span>
`executionContextId` <span data-ttu-id="0ad71-180">ou `objectId` deve ser especificado</span><span class="sxs-lookup"><span data-stu-id="0ad71-180">or `objectId` should be specified</span></span> |  
| <span data-ttu-id="0ad71-181">objectGroup \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-181">objectGroup \(optional\)</span></span> | `string` | <span data-ttu-id="0ad71-182">Nome de grupo simbólico que pode ser usado para liberar vários objetos.</span><span class="sxs-lookup"><span data-stu-id="0ad71-182">Symbolic group name that can be used to release multiple objects.</span></span>  <span data-ttu-id="0ad71-183">Se `objectGroup` não for especificado e `objectId` for, será `objectGroup` herdado do objeto.</span><span class="sxs-lookup"><span data-stu-id="0ad71-183">If `objectGroup` is not specified and `objectId` is, `objectGroup` will be inherited from object.</span></span> |  

| <span data-ttu-id="0ad71-184">Retorna</span><span class="sxs-lookup"><span data-stu-id="0ad71-184">Returns</span></span> | <span data-ttu-id="0ad71-185">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-185">Type</span></span> | <span data-ttu-id="0ad71-186">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-186">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-187">result</span><span class="sxs-lookup"><span data-stu-id="0ad71-187">result</span></span> | [<span data-ttu-id="0ad71-188">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0ad71-188">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="0ad71-189">Resultado da chamada.</span><span class="sxs-lookup"><span data-stu-id="0ad71-189">Call result.</span></span> |  

---  

### <a name="awaitpromise"></a><span data-ttu-id="0ad71-190">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="0ad71-190">awaitPromise</span></span>  

<span data-ttu-id="0ad71-191">Adicione manipulador para promessa com uma ID de objeto promise determinada.</span><span class="sxs-lookup"><span data-stu-id="0ad71-191">Add handler to promise with given promise object id.</span></span>  

| <span data-ttu-id="0ad71-192">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ad71-192">Parameters</span></span> | <span data-ttu-id="0ad71-193">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-193">Type</span></span> | <span data-ttu-id="0ad71-194">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-194">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-195">promiseObjectId</span><span class="sxs-lookup"><span data-stu-id="0ad71-195">promiseObjectId</span></span> | [<span data-ttu-id="0ad71-196">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="0ad71-196">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="0ad71-197">Identificador da promessa.</span><span class="sxs-lookup"><span data-stu-id="0ad71-197">Identifier of the promise.</span></span> |  
| <span data-ttu-id="0ad71-198">returnByValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-198">returnByValue \(optional\)</span></span> | <span data-ttu-id="0ad71-199">boolean</span><span class="sxs-lookup"><span data-stu-id="0ad71-199">boolean</span></span> | <span data-ttu-id="0ad71-200">Se o resultado é esperado para ser um objeto JSON que deve ser enviado por valor.</span><span class="sxs-lookup"><span data-stu-id="0ad71-200">Whether the result is expected to be a JSON object that should be sent by value.</span></span> |  

| <span data-ttu-id="0ad71-201">Retorna</span><span class="sxs-lookup"><span data-stu-id="0ad71-201">Returns</span></span> | <span data-ttu-id="0ad71-202">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-202">Type</span></span> | <span data-ttu-id="0ad71-203">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-203">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-204">result</span><span class="sxs-lookup"><span data-stu-id="0ad71-204">result</span></span> | [<span data-ttu-id="0ad71-205">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0ad71-205">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="0ad71-206">Resultado da promessa.</span><span class="sxs-lookup"><span data-stu-id="0ad71-206">Promise result.</span></span>  <span data-ttu-id="0ad71-207">Conterá valor rejeitado se a promessa for rejeitada.</span><span class="sxs-lookup"><span data-stu-id="0ad71-207">Will contain rejected value if promise was rejected.</span></span> |  

---  

### <a name="getproperties"></a><span data-ttu-id="0ad71-208">getProperties</span><span class="sxs-lookup"><span data-stu-id="0ad71-208">getProperties</span></span>  

<span data-ttu-id="0ad71-209">Retorna propriedades de um determinado objeto.</span><span class="sxs-lookup"><span data-stu-id="0ad71-209">Returns properties of a given object.</span></span> <span data-ttu-id="0ad71-210">O grupo de objetos do resultado é herdado do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="0ad71-210">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="0ad71-211">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ad71-211">Parameters</span></span> | <span data-ttu-id="0ad71-212">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-212">Type</span></span> | <span data-ttu-id="0ad71-213">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-213">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-214">objectId</span><span class="sxs-lookup"><span data-stu-id="0ad71-214">objectId</span></span> | [<span data-ttu-id="0ad71-215">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="0ad71-215">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="0ad71-216">Identificador do objeto para o que retornar propriedades.</span><span class="sxs-lookup"><span data-stu-id="0ad71-216">Identifier of the object to return properties for.</span></span>  `objectId` <span data-ttu-id="0ad71-217">deve ser da `Debugger.evaluateOnCallFrame()` função.</span><span class="sxs-lookup"><span data-stu-id="0ad71-217">must be from the `Debugger.evaluateOnCallFrame()` function.</span></span> |  
| <span data-ttu-id="0ad71-218">ownProperties \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-218">ownProperties \(optional\)</span></span> | `boolean` | <span data-ttu-id="0ad71-219">Se `true` , retorna propriedades pertencentes apenas ao elemento em si, não à cadeia de protótipos.</span><span class="sxs-lookup"><span data-stu-id="0ad71-219">If `true`, returns properties belonging only to the element itself, not to its prototype chain.</span></span> |  
| <span data-ttu-id="0ad71-220">accessorPropertiesOnly \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-220">accessorPropertiesOnly \(optional\)</span></span> | `boolean` | <span data-ttu-id="0ad71-221">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="0ad71-221">**Experimental**.</span></span>  <span data-ttu-id="0ad71-222">Se `true` , retorna propriedades do acessador \(somente com getter/setter\) ; as propriedades internas também não são retornadas.</span><span class="sxs-lookup"><span data-stu-id="0ad71-222">If `true`, returns accessor properties \(with getter/setter\) only; internal properties are not returned either.</span></span> |  

| <span data-ttu-id="0ad71-223">Retorna</span><span class="sxs-lookup"><span data-stu-id="0ad71-223">Returns</span></span> | <span data-ttu-id="0ad71-224">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-224">Type</span></span> | <span data-ttu-id="0ad71-225">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-225">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-226">result</span><span class="sxs-lookup"><span data-stu-id="0ad71-226">result</span></span> | [<span data-ttu-id="0ad71-227">PropertyDescriptor[]</span><span class="sxs-lookup"><span data-stu-id="0ad71-227">PropertyDescriptor[]</span></span>](#propertydescriptor) | <span data-ttu-id="0ad71-228">Propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="0ad71-228">Object properties.</span></span> |  

---  

### <a name="globallexicalscopenames"></a><span data-ttu-id="0ad71-229">globalLexicalScopeNames</span><span class="sxs-lookup"><span data-stu-id="0ad71-229">globalLexicalScopeNames</span></span>  

<span data-ttu-id="0ad71-230">Retorna todas as variáveis let, const e class do escopo global do console.</span><span class="sxs-lookup"><span data-stu-id="0ad71-230">Returns all let, const, and class variables from the console global scope.</span></span>  

| <span data-ttu-id="0ad71-231">Retorna</span><span class="sxs-lookup"><span data-stu-id="0ad71-231">Returns</span></span> | <span data-ttu-id="0ad71-232">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-232">Type</span></span> | <span data-ttu-id="0ad71-233">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-233">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-234">names</span><span class="sxs-lookup"><span data-stu-id="0ad71-234">names</span></span> | `string[]` | &nbsp; |  

---  

### <a name="releaseobject"></a><span data-ttu-id="0ad71-235">releaseObject</span><span class="sxs-lookup"><span data-stu-id="0ad71-235">releaseObject</span></span>  

<span data-ttu-id="0ad71-236">Libera o objeto remoto com uma ID determinada.</span><span class="sxs-lookup"><span data-stu-id="0ad71-236">Releases remote object with given ID.</span></span>  

| <span data-ttu-id="0ad71-237">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ad71-237">Parameters</span></span> | <span data-ttu-id="0ad71-238">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-238">Type</span></span> | <span data-ttu-id="0ad71-239">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-239">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-240">objectId</span><span class="sxs-lookup"><span data-stu-id="0ad71-240">objectId</span></span> | [<span data-ttu-id="0ad71-241">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="0ad71-241">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="0ad71-242">Identificador do objeto a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="0ad71-242">Identifier of the object to release.</span></span> |  

---  

### <a name="releaseobjectgroup"></a><span data-ttu-id="0ad71-243">releaseObjectGroup</span><span class="sxs-lookup"><span data-stu-id="0ad71-243">releaseObjectGroup</span></span>  

<span data-ttu-id="0ad71-244">Libera todos os objetos remotos que pertencem a um determinado grupo.</span><span class="sxs-lookup"><span data-stu-id="0ad71-244">Releases all remote objects that belong to a given group.</span></span>  

| <span data-ttu-id="0ad71-245">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ad71-245">Parameters</span></span> | <span data-ttu-id="0ad71-246">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-246">Type</span></span> | <span data-ttu-id="0ad71-247">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-247">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-248">objectGroup</span><span class="sxs-lookup"><span data-stu-id="0ad71-248">objectGroup</span></span> | `string` | <span data-ttu-id="0ad71-249">Nome do grupo de objetos simbólicos.</span><span class="sxs-lookup"><span data-stu-id="0ad71-249">Symbolic object group name.</span></span> |  

---  

### <a name="discardconsoleentries"></a><span data-ttu-id="0ad71-250">discardConsoleEntries</span><span class="sxs-lookup"><span data-stu-id="0ad71-250">discardConsoleEntries</span></span>  

<span data-ttu-id="0ad71-251">Descarta exceções coletadas e chamadas de API de console.</span><span class="sxs-lookup"><span data-stu-id="0ad71-251">Discards collected exceptions and console API calls.</span></span>  

---  

## <a name="events"></a><span data-ttu-id="0ad71-252">Eventos</span><span class="sxs-lookup"><span data-stu-id="0ad71-252">Events</span></span>  

### <a name="executioncontextcreated"></a><span data-ttu-id="0ad71-253">executionContextCreated</span><span class="sxs-lookup"><span data-stu-id="0ad71-253">executionContextCreated</span></span>  

<span data-ttu-id="0ad71-254">Emitido quando o novo contexto de execução é criado.</span><span class="sxs-lookup"><span data-stu-id="0ad71-254">Issued when new execution context is created.</span></span>  

| <span data-ttu-id="0ad71-255">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ad71-255">Parameters</span></span> | <span data-ttu-id="0ad71-256">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-256">Type</span></span> | <span data-ttu-id="0ad71-257">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-257">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-258">context</span><span class="sxs-lookup"><span data-stu-id="0ad71-258">context</span></span> | [<span data-ttu-id="0ad71-259">ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="0ad71-259">ExecutionContextDescription</span></span>](#executioncontextdescription) | <span data-ttu-id="0ad71-260">Um contexto de execução recém-criado.</span><span class="sxs-lookup"><span data-stu-id="0ad71-260">A newly created execution context.</span></span> |  

---  

### <a name="executioncontextdestroyed"></a><span data-ttu-id="0ad71-261">executionContextDestroyed</span><span class="sxs-lookup"><span data-stu-id="0ad71-261">executionContextDestroyed</span></span>  

<span data-ttu-id="0ad71-262">Emitido quando o contexto de execução é destruído.</span><span class="sxs-lookup"><span data-stu-id="0ad71-262">Issued when execution context is destroyed.</span></span>  

| <span data-ttu-id="0ad71-263">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ad71-263">Parameters</span></span> | <span data-ttu-id="0ad71-264">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-264">Type</span></span> | <span data-ttu-id="0ad71-265">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-265">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-266">executionContextId</span><span class="sxs-lookup"><span data-stu-id="0ad71-266">executionContextId</span></span> | [<span data-ttu-id="0ad71-267">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="0ad71-267">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="0ad71-268">ID do contexto destruído.</span><span class="sxs-lookup"><span data-stu-id="0ad71-268">ID of the destroyed context.</span></span> |  

---  

### <a name="executioncontextscleared"></a><span data-ttu-id="0ad71-269">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="0ad71-269">executionContextsCleared</span></span>  

<span data-ttu-id="0ad71-270">Emitido quando todos os executionContexts foram limpos no navegador.</span><span class="sxs-lookup"><span data-stu-id="0ad71-270">Issued when all executionContexts were cleared in browser.</span></span>  

&nbsp;  

---  

### <a name="exceptionthrown"></a><span data-ttu-id="0ad71-271">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="0ad71-271">exceptionThrown</span></span>  

<span data-ttu-id="0ad71-272">Emitido quando a exceção foi lançada e não foi acionada.</span><span class="sxs-lookup"><span data-stu-id="0ad71-272">Issued when exception was thrown and unhandled.</span></span>  

| <span data-ttu-id="0ad71-273">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ad71-273">Parameters</span></span> | <span data-ttu-id="0ad71-274">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-274">Type</span></span> | <span data-ttu-id="0ad71-275">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-275">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-276">timestamp</span><span class="sxs-lookup"><span data-stu-id="0ad71-276">timestamp</span></span> | [<span data-ttu-id="0ad71-277">Carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="0ad71-277">Timestamp</span></span>](#timestamp) | <span data-ttu-id="0ad71-278">Timestamp da exceção.</span><span class="sxs-lookup"><span data-stu-id="0ad71-278">Timestamp of the exception.</span></span> |  
| <span data-ttu-id="0ad71-279">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="0ad71-279">exceptionDetails</span></span> | [<span data-ttu-id="0ad71-280">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="0ad71-280">ExceptionDetails</span></span>](#exceptiondetails) | &nbsp; |  

---  

### <a name="consoleapicalled"></a><span data-ttu-id="0ad71-281">consoleAPICalled</span><span class="sxs-lookup"><span data-stu-id="0ad71-281">consoleAPICalled</span></span>  

| <span data-ttu-id="0ad71-282">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ad71-282">Parameters</span></span> | <span data-ttu-id="0ad71-283">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-283">Type</span></span> | <span data-ttu-id="0ad71-284">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-284">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-285">tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-285">type</span></span> | `string` | <span data-ttu-id="0ad71-286">Tipo da chamada.</span><span class="sxs-lookup"><span data-stu-id="0ad71-286">Type of the call.</span></span>  <span data-ttu-id="0ad71-287">Valores permitidos: `log` , , , , , , , , `info` , , `warning` , , , , `error` , , `debug` `assert` `table` , `trace` `dir` `dirxml` `clear` `select` `count` `countReset` `timeEnd` `timeStamp` `startGroup` , `startGroupCollapsed`</span><span class="sxs-lookup"><span data-stu-id="0ad71-287">Allowed values:  `log`, `info`, `warning`, `error`, `debug`, `assert`, `table`, `trace`, `dir`, `dirxml`, `clear`, `select`, `count`, `countReset`, `timeEnd`, `timeStamp`, `startGroup`, `startGroupCollapsed`, and</span></span> `endGroup` |  
| <span data-ttu-id="0ad71-288">args</span><span class="sxs-lookup"><span data-stu-id="0ad71-288">args</span></span> | <span data-ttu-id="0ad71-289">[RemoteObject[]] (#remoteobject</span><span class="sxs-lookup"><span data-stu-id="0ad71-289">[RemoteObject[]](#remoteobject</span></span> | <span data-ttu-id="0ad71-290">Argumentos de chamada.</span><span class="sxs-lookup"><span data-stu-id="0ad71-290">Call arguments.</span></span> |  
| <span data-ttu-id="0ad71-291">executionContextId</span><span class="sxs-lookup"><span data-stu-id="0ad71-291">executionContextId</span></span> | [<span data-ttu-id="0ad71-292">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="0ad71-292">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="0ad71-293">Identificador do contexto em que a chamada do console foi feita.</span><span class="sxs-lookup"><span data-stu-id="0ad71-293">Identifier of the context where console call was made.</span></span> |  
| <span data-ttu-id="0ad71-294">timestamp \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-294">timestamp \(optional\)</span></span> | [<span data-ttu-id="0ad71-295">Carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="0ad71-295">Timestamp</span></span>](#timestamp) | <span data-ttu-id="0ad71-296">Timestamp de chamada.</span><span class="sxs-lookup"><span data-stu-id="0ad71-296">Call timestamp.</span></span> |  
| <span data-ttu-id="0ad71-297">stackTrace \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-297">stackTrace \(optional\)</span></span> | [<span data-ttu-id="0ad71-298">StackTrace</span><span class="sxs-lookup"><span data-stu-id="0ad71-298">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="0ad71-299">Rastreamento de pilha capturado se disponível.</span><span class="sxs-lookup"><span data-stu-id="0ad71-299">Stack trace captured if available.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="0ad71-300">Tipos</span><span class="sxs-lookup"><span data-stu-id="0ad71-300">Types</span></span>  

### <a name="scriptid-string"></a><span data-ttu-id="0ad71-301">Cadeia de caracteres ScriptId</span><span class="sxs-lookup"><span data-stu-id="0ad71-301">ScriptId string</span></span>  

<a name="scriptid"></a>

<span data-ttu-id="0ad71-302">Identificador de script exclusivo.</span><span class="sxs-lookup"><span data-stu-id="0ad71-302">Unique script identifier.</span></span>  

&nbsp;  

---  

### <a name="remoteobjectid-string"></a><span data-ttu-id="0ad71-303">Cadeia de caracteres RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="0ad71-303">RemoteObjectId string</span></span>  

<a name="remoteobjectid"></a>

<span data-ttu-id="0ad71-304">Identificador de objeto exclusivo.</span><span class="sxs-lookup"><span data-stu-id="0ad71-304">Unique object identifier.</span></span>  

&nbsp;  

---  

### <a name="unserializablevalue-string"></a><span data-ttu-id="0ad71-305">Cadeia de caracteres UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="0ad71-305">UnserializableValue string</span></span>  

<a name="unserializablevalue"></a>  

<span data-ttu-id="0ad71-306">Valor primitivo que não pode ser stringified JSON.</span><span class="sxs-lookup"><span data-stu-id="0ad71-306">Primitive value which cannot be JSON-stringified.</span></span>  

##### <a name="allowed-values"></a><span data-ttu-id="0ad71-307">Valores permitidos</span><span class="sxs-lookup"><span data-stu-id="0ad71-307">Allowed Values</span></span>  

`Infinity`<span data-ttu-id="0ad71-308">, `NaN`, `-Infinity`,</span><span class="sxs-lookup"><span data-stu-id="0ad71-308">, `NaN`, `-Infinity`,</span></span> `-0`  

---  

### <a name="remoteobject-object"></a><span data-ttu-id="0ad71-309">Objeto RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0ad71-309">RemoteObject object</span></span>  

<a name="remoteobject"></a>  

<span data-ttu-id="0ad71-310">Objeto Mirror fazendo referência ao objeto JavaScript original.</span><span class="sxs-lookup"><span data-stu-id="0ad71-310">Mirror object referencing original JavaScript object.</span></span>  

| <span data-ttu-id="0ad71-311">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0ad71-311">Properties</span></span> | <span data-ttu-id="0ad71-312">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-312">Type</span></span> | <span data-ttu-id="0ad71-313">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-313">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-314">tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-314">type</span></span> | `string` | <span data-ttu-id="0ad71-315">Tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="0ad71-315">Object type.</span></span>  <span data-ttu-id="0ad71-316">Valores permitidos:  `object` , , , , , `function` `undefined` `string` `number` `boolean` e</span><span class="sxs-lookup"><span data-stu-id="0ad71-316">Allowed values:  `object`, `function`, `undefined`, `string`, `number`, `boolean`, and</span></span> `symbol` |  
| <span data-ttu-id="0ad71-317">subtipo \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-317">subtype \(optional\)</span></span> | `string` | <span data-ttu-id="0ad71-318">Dica de subtipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="0ad71-318">Object subtype hint.</span></span>  <span data-ttu-id="0ad71-319">Especificado apenas para `object` valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="0ad71-319">Specified for `object` type values only.</span></span>  <span data-ttu-id="0ad71-320">Valores permitidos:  `null` `error` , , `promise` e</span><span class="sxs-lookup"><span data-stu-id="0ad71-320">Allowed values:  `null`, `error`, `promise`, and</span></span> `node` |  
| <span data-ttu-id="0ad71-321">className \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-321">className \(optional\)</span></span> | `string` | <span data-ttu-id="0ad71-322">Nome da classe de objeto \(construtor\).</span><span class="sxs-lookup"><span data-stu-id="0ad71-322">Object class \(constructor\) name.</span></span>  <span data-ttu-id="0ad71-323">Especificado apenas para `object` valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="0ad71-323">Specified for `object` type values only.</span></span> |  
| <span data-ttu-id="0ad71-324">valor \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-324">value \(optional\)</span></span> | `any` | <span data-ttu-id="0ad71-325">Valor do objeto remoto em caso de valores primitivos ou valores JSON \(se foi solicitado\).</span><span class="sxs-lookup"><span data-stu-id="0ad71-325">Remote object value in case of primitive values or JSON values \(if it was requested\).</span></span> |  
| <span data-ttu-id="0ad71-326">unserializableValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-326">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="0ad71-327">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="0ad71-327">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="0ad71-328">O valor primitivo que não pode ser stringified JSON não tem `value` , mas obtém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="0ad71-328">Primitive value which can not be JSON-stringified does not have `value`, but gets this property.</span></span> |  
| <span data-ttu-id="0ad71-329">description \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-329">description \(optional\)</span></span> | `string` | <span data-ttu-id="0ad71-330">Representação de cadeia de caracteres do objeto.</span><span class="sxs-lookup"><span data-stu-id="0ad71-330">String representation of the object.</span></span> |  
| <span data-ttu-id="0ad71-331">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-331">objectId \(optional\)</span></span> | [<span data-ttu-id="0ad71-332">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="0ad71-332">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="0ad71-333">Identificador de objeto exclusivo \(para valores não primitivos\).</span><span class="sxs-lookup"><span data-stu-id="0ad71-333">Unique object identifier \(for non-primitive values\).</span></span> |  
| <span data-ttu-id="0ad71-334">msDebuggerPropertyId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-334">msDebuggerPropertyId \(optional\)</span></span> | `string` | <span data-ttu-id="0ad71-335">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="0ad71-335">**Experimental**.</span></span>  <span data-ttu-id="0ad71-336">Microsoft: A ID da propriedade depurador associada para este objeto.</span><span class="sxs-lookup"><span data-stu-id="0ad71-336">Microsoft:  The associated debugger property ID for this object.</span></span> |  

---  

### <a name="propertydescriptor-object"></a><span data-ttu-id="0ad71-337">Objeto PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="0ad71-337">PropertyDescriptor object</span></span>  

<a name="propertydescriptor"></a>  

<span data-ttu-id="0ad71-338">Descritor da propriedade Object.</span><span class="sxs-lookup"><span data-stu-id="0ad71-338">Object property descriptor.</span></span>  

| <span data-ttu-id="0ad71-339">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0ad71-339">Properties</span></span> | <span data-ttu-id="0ad71-340">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-340">Type</span></span> | <span data-ttu-id="0ad71-341">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-341">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-342">name</span><span class="sxs-lookup"><span data-stu-id="0ad71-342">name</span></span> | `string` | <span data-ttu-id="0ad71-343">Nome da propriedade ou descrição de símbolo.</span><span class="sxs-lookup"><span data-stu-id="0ad71-343">Property name or symbol description.</span></span> |  
| <span data-ttu-id="0ad71-344">valor \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-344">value \(optional\)</span></span> | [<span data-ttu-id="0ad71-345">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0ad71-345">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="0ad71-346">O valor associado à propriedade.</span><span class="sxs-lookup"><span data-stu-id="0ad71-346">The value associated with the property.</span></span> |  
| <span data-ttu-id="0ad71-347">writable \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-347">writable \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="0ad71-348">se o valor associado à propriedade pode ser alterado \(descritores de dados somente\).</span><span class="sxs-lookup"><span data-stu-id="0ad71-348">if the value associated with the property may be changed \(data descriptors only\).</span></span> |  
| <span data-ttu-id="0ad71-349">get \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-349">get \(optional\)</span></span> | [<span data-ttu-id="0ad71-350">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0ad71-350">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="0ad71-351">Uma função que serve como um getter para a propriedade ou se não houver getter \(descritores do acessador `undefined` somente\).</span><span class="sxs-lookup"><span data-stu-id="0ad71-351">A function which serves as a getter for the property, or `undefined` if there is no getter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="0ad71-352">set \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-352">set \(optional\)</span></span> | [<span data-ttu-id="0ad71-353">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0ad71-353">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="0ad71-354">Uma função que serve como um setter para a propriedade ou se não houver setter \(descritores do acessador `undefined` somente\).</span><span class="sxs-lookup"><span data-stu-id="0ad71-354">A function which serves as a setter for the property, or `undefined` if there is no setter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="0ad71-355">configurável</span><span class="sxs-lookup"><span data-stu-id="0ad71-355">configurable</span></span> | `boolean` | `True` <span data-ttu-id="0ad71-356">se o tipo desse descritor de propriedade pode ser alterado e se a propriedade pode ser excluída do objeto correspondente.</span><span class="sxs-lookup"><span data-stu-id="0ad71-356">if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span> |  
| <span data-ttu-id="0ad71-357">enumerable</span><span class="sxs-lookup"><span data-stu-id="0ad71-357">enumerable</span></span> | `boolean` | `True` <span data-ttu-id="0ad71-358">se essa propriedade aparecer durante a enumeração das propriedades no objeto correspondente.</span><span class="sxs-lookup"><span data-stu-id="0ad71-358">if this property shows up during enumeration of the properties on the corresponding object.</span></span> |  
| <span data-ttu-id="0ad71-359">wasThrown \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-359">wasThrown \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="0ad71-360">se o resultado foi lançado durante a avaliação.</span><span class="sxs-lookup"><span data-stu-id="0ad71-360">if the result was thrown during the evaluation.</span></span> |  
| <span data-ttu-id="0ad71-361">isOwn \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-361">isOwn \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="0ad71-362">se a propriedade pertence ao objeto.</span><span class="sxs-lookup"><span data-stu-id="0ad71-362">if the property is owned for the object.</span></span> |  
| <span data-ttu-id="0ad71-363">msReturnValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-363">msReturnValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="0ad71-364">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="0ad71-364">**Experimental**.</span></span>  <span data-ttu-id="0ad71-365">Microsoft:  `True` se a propriedade for um valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="0ad71-365">Microsoft:  `True` if the property is a return value.</span></span> |  
| <span data-ttu-id="0ad71-366">símbolo \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-366">symbol \(optional\)</span></span> | [<span data-ttu-id="0ad71-367">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0ad71-367">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="0ad71-368">Objeto símbolo de propriedade, se a propriedade for do `symbol` tipo.</span><span class="sxs-lookup"><span data-stu-id="0ad71-368">Property symbol object, if the property is of the `symbol` type.</span></span> |  

---  

### <a name="callargument-object"></a><span data-ttu-id="0ad71-369">Objeto CallArgument</span><span class="sxs-lookup"><span data-stu-id="0ad71-369">CallArgument object</span></span>  

<a name="callargument"></a>  

<span data-ttu-id="0ad71-370">Representa o argumento de chamada de função.</span><span class="sxs-lookup"><span data-stu-id="0ad71-370">Represents function call argument.</span></span>  <span data-ttu-id="0ad71-371">A ID do objeto remoto, o valor primitivo, o valor primitivo `objectId` `value` inserializável ou nenhum dos \(for undefined\) deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="0ad71-371">Either remote object ID `objectId`, primitive `value`, unserializable primitive value, or neither of \(for undefined\) them should be specified.</span></span>  

| <span data-ttu-id="0ad71-372">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0ad71-372">Properties</span></span> | <span data-ttu-id="0ad71-373">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-373">Type</span></span> | <span data-ttu-id="0ad71-374">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-374">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-375">valor \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-375">value \(optional\)</span></span> | `any` | <span data-ttu-id="0ad71-376">Valor primitivo ou objeto javascript serializable.</span><span class="sxs-lookup"><span data-stu-id="0ad71-376">Primitive value or serializable javascript object.</span></span> |  
| <span data-ttu-id="0ad71-377">unserializableValue \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-377">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="0ad71-378">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="0ad71-378">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="0ad71-379">Valor primitivo que não pode ser stringified JSON.</span><span class="sxs-lookup"><span data-stu-id="0ad71-379">Primitive value which can not be JSON-stringified.</span></span> |  
| <span data-ttu-id="0ad71-380">objectId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-380">objectId \(optional\)</span></span> | <span data-ttu-id="0ad71-381">[RemoteObjectId](#remoteobjectid)]</span><span class="sxs-lookup"><span data-stu-id="0ad71-381">[RemoteObjectId](#remoteobjectid)]</span></span> | <span data-ttu-id="0ad71-382">Identificador de objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="0ad71-382">Remote object handle.</span></span> |  

---  

### <a name="executioncontextid-integer"></a><span data-ttu-id="0ad71-383">ExecutionContextId integer</span><span class="sxs-lookup"><span data-stu-id="0ad71-383">ExecutionContextId integer</span></span>  

<a name="executioncontextid"></a>  

<span data-ttu-id="0ad71-384">ID de um contexto de execução.</span><span class="sxs-lookup"><span data-stu-id="0ad71-384">ID of an execution context.</span></span>  

&nbsp;  

---  

### <a name="executioncontextdescription-object"></a><span data-ttu-id="0ad71-385">Objeto ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="0ad71-385">ExecutionContextDescription object</span></span>  

<a name="executioncontextdescription"></a>  

<span data-ttu-id="0ad71-386">Descrição de um mundo isolado.</span><span class="sxs-lookup"><span data-stu-id="0ad71-386">Description of an isolated world.</span></span>  

| <span data-ttu-id="0ad71-387">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0ad71-387">Properties</span></span> | <span data-ttu-id="0ad71-388">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-388">Type</span></span> | <span data-ttu-id="0ad71-389">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-389">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-390">id</span><span class="sxs-lookup"><span data-stu-id="0ad71-390">id</span></span> | [<span data-ttu-id="0ad71-391">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="0ad71-391">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="0ad71-392">ID exclusiva do contexto de execução.</span><span class="sxs-lookup"><span data-stu-id="0ad71-392">Unique ID of the execution context.</span></span>  <span data-ttu-id="0ad71-393">Ele pode ser usado para especificar em qual contexto de execução</span><span class="sxs-lookup"><span data-stu-id="0ad71-393">It can be used to specify in which execution context</span></span>
<span data-ttu-id="0ad71-394">a avaliação de script deve ser realizada.</span><span class="sxs-lookup"><span data-stu-id="0ad71-394">script evaluation should be performed.</span></span> |  
| <span data-ttu-id="0ad71-395">origin</span><span class="sxs-lookup"><span data-stu-id="0ad71-395">origin</span></span> | `string` | <span data-ttu-id="0ad71-396">Origem do contexto de execução.</span><span class="sxs-lookup"><span data-stu-id="0ad71-396">Execution context origin.</span></span> |  
| <span data-ttu-id="0ad71-397">name</span><span class="sxs-lookup"><span data-stu-id="0ad71-397">name</span></span> | `string` | <span data-ttu-id="0ad71-398">Nome acessível humano que descreve determinado contexto.</span><span class="sxs-lookup"><span data-stu-id="0ad71-398">Human readable name describing given context.</span></span> |  

---  

### <a name="exceptiondetails-object"></a><span data-ttu-id="0ad71-399">Objeto ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="0ad71-399">ExceptionDetails object</span></span>  

<a name="exceptiondetails"></a>  

<span data-ttu-id="0ad71-400">Informações detalhadas sobre exceção (ou erro) que foram lançadas durante a compilação ou execução do script.</span><span class="sxs-lookup"><span data-stu-id="0ad71-400">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>  

| <span data-ttu-id="0ad71-401">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0ad71-401">Properties</span></span> | <span data-ttu-id="0ad71-402">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-402">Type</span></span> | <span data-ttu-id="0ad71-403">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-403">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-404">exceptionId</span><span class="sxs-lookup"><span data-stu-id="0ad71-404">exceptionId</span></span> | `integer` | <span data-ttu-id="0ad71-405">ID de exceção.</span><span class="sxs-lookup"><span data-stu-id="0ad71-405">Exception ID.</span></span> |  
| <span data-ttu-id="0ad71-406">texto</span><span class="sxs-lookup"><span data-stu-id="0ad71-406">text</span></span> | `string` | <span data-ttu-id="0ad71-407">Texto de exceção, que deve ser usado junto com o objeto exception quando disponível.</span><span class="sxs-lookup"><span data-stu-id="0ad71-407">Exception text, which should be used together with exception object when available.</span></span> |  
| <span data-ttu-id="0ad71-408">lineNumber</span><span class="sxs-lookup"><span data-stu-id="0ad71-408">lineNumber</span></span> | `integer` | <span data-ttu-id="0ad71-409">Número de linha do local de exceção \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="0ad71-409">Line number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="0ad71-410">columnNumber</span><span class="sxs-lookup"><span data-stu-id="0ad71-410">columnNumber</span></span> | `integer` | <span data-ttu-id="0ad71-411">Número da coluna do local de exceção \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="0ad71-411">Column number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="0ad71-412">scriptId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-412">scriptId \(optional\)</span></span> | [<span data-ttu-id="0ad71-413">ScriptId</span><span class="sxs-lookup"><span data-stu-id="0ad71-413">ScriptId</span></span>](#scriptid) | <span data-ttu-id="0ad71-414">ID do script do local de exceção.</span><span class="sxs-lookup"><span data-stu-id="0ad71-414">Script ID of the exception location.</span></span> |  
| <span data-ttu-id="0ad71-415">url \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-415">url \(optional\)</span></span> | `string` | <span data-ttu-id="0ad71-416">URL do local de exceção, a ser usada quando o script não foi relatado.</span><span class="sxs-lookup"><span data-stu-id="0ad71-416">URL of the exception location, to be used when the script was not reported.</span></span> |  
| <span data-ttu-id="0ad71-417">stackTrace \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-417">stackTrace \(optional\)</span></span> | [<span data-ttu-id="0ad71-418">StackTrace</span><span class="sxs-lookup"><span data-stu-id="0ad71-418">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="0ad71-419">Rastreamento de pilha JavaScript, se disponível.</span><span class="sxs-lookup"><span data-stu-id="0ad71-419">JavaScript stack trace if available.</span></span> |  
| <span data-ttu-id="0ad71-420">exception \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-420">exception \(optional\)</span></span> | [<span data-ttu-id="0ad71-421">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0ad71-421">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="0ad71-422">Objeto Exception, se disponível.</span><span class="sxs-lookup"><span data-stu-id="0ad71-422">Exception object if available.</span></span> |  
| <span data-ttu-id="0ad71-423">executionContextId \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-423">executionContextId \(optional\)</span></span> | [<span data-ttu-id="0ad71-424">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="0ad71-424">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="0ad71-425">Identificador do contexto em que a exceção aconteceu.</span><span class="sxs-lookup"><span data-stu-id="0ad71-425">Identifier of the context where exception happened.</span></span> |  

---  

### <a name="timestamp-integer"></a><span data-ttu-id="0ad71-426">Número inteiro do timestamp</span><span class="sxs-lookup"><span data-stu-id="0ad71-426">Timestamp integer</span></span>  

<a name="timestamp"></a>  

<span data-ttu-id="0ad71-427">Número de milissegundos desde a época.</span><span class="sxs-lookup"><span data-stu-id="0ad71-427">Number of milliseconds since epoch.</span></span>  

&nbsp;  

---  

### <a name="callframe-object"></a><span data-ttu-id="0ad71-428">Objeto CallFrame</span><span class="sxs-lookup"><span data-stu-id="0ad71-428">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="0ad71-429">Entrada de pilha para erros e declarações de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="0ad71-429">Stack entry for runtime errors and assertions.</span></span>  

| <span data-ttu-id="0ad71-430">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0ad71-430">Properties</span></span> | <span data-ttu-id="0ad71-431">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-431">Type</span></span> | <span data-ttu-id="0ad71-432">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-432">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-433">functionName</span><span class="sxs-lookup"><span data-stu-id="0ad71-433">functionName</span></span> | `string` | <span data-ttu-id="0ad71-434">Nome da função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0ad71-434">JavaScript function name.</span></span> |  
| <span data-ttu-id="0ad71-435">scriptId</span><span class="sxs-lookup"><span data-stu-id="0ad71-435">scriptId</span></span> | [<span data-ttu-id="0ad71-436">ScriptId</span><span class="sxs-lookup"><span data-stu-id="0ad71-436">ScriptId</span></span>](#scriptid) | <span data-ttu-id="0ad71-437">ID de script JavaScript. ScriptId estará vazio se o depurador não estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="0ad71-437">JavaScript script id. ScriptId will be empty if debugger is not enabled.</span></span> |  
| <span data-ttu-id="0ad71-438">url</span><span class="sxs-lookup"><span data-stu-id="0ad71-438">url</span></span> | `string` | <span data-ttu-id="0ad71-439">Nome ou url do script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0ad71-439">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="0ad71-440">lineNumber</span><span class="sxs-lookup"><span data-stu-id="0ad71-440">lineNumber</span></span> | `integer` | <span data-ttu-id="0ad71-441">Número da linha de script JavaScript \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="0ad71-441">JavaScript script line number \(0-based\).</span></span> |  
| <span data-ttu-id="0ad71-442">columnNumber</span><span class="sxs-lookup"><span data-stu-id="0ad71-442">columnNumber</span></span> | <span data-ttu-id="0ad71-443">número inteiro</span><span class="sxs-lookup"><span data-stu-id="0ad71-443">integer</span></span> | <span data-ttu-id="0ad71-444">Número da coluna de script JavaScript \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="0ad71-444">JavaScript script column number \(0-based\).</span></span> |  

---  

### <a name="stacktrace-object"></a><span data-ttu-id="0ad71-445">Objeto StackTrace</span><span class="sxs-lookup"><span data-stu-id="0ad71-445">StackTrace object</span></span>  

<a name="stacktrace"></a>  

<span data-ttu-id="0ad71-446">Quadros de chamada para declarações ou mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="0ad71-446">Call frames for assertions or error messages.</span></span>  

| <span data-ttu-id="0ad71-447">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0ad71-447">Properties</span></span> | <span data-ttu-id="0ad71-448">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad71-448">Type</span></span> | <span data-ttu-id="0ad71-449">Detalhes</span><span class="sxs-lookup"><span data-stu-id="0ad71-449">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0ad71-450">description \(optional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-450">description \(optional\)</span></span> | `string` | <span data-ttu-id="0ad71-451">Rótulo de cadeia de caracteres desse rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="0ad71-451">String label of this stack trace.</span></span>  <span data-ttu-id="0ad71-452">Para rastreamentos assíncrono, pode ser um nome da função que iniciou a chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="0ad71-452">For async traces this may be a name of the function that initiated the async call.</span></span> |  
| <span data-ttu-id="0ad71-453">callFrames</span><span class="sxs-lookup"><span data-stu-id="0ad71-453">callFrames</span></span> | [<span data-ttu-id="0ad71-454">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="0ad71-454">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="0ad71-455">Nome da função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0ad71-455">JavaScript function name.</span></span> |  
| <span data-ttu-id="0ad71-456">pai \(opcional\)</span><span class="sxs-lookup"><span data-stu-id="0ad71-456">parent \(optional\)</span></span> | [<span data-ttu-id="0ad71-457">StackTrace</span><span class="sxs-lookup"><span data-stu-id="0ad71-457">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="0ad71-458">Rastreamento de pilha JavaScript assíncrono que precedeu essa pilha, se disponível.</span><span class="sxs-lookup"><span data-stu-id="0ad71-458">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span> |  

---  
