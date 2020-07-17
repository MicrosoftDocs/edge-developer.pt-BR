---
description: Referência para o domínio de tempo de execução. O domínio do tempo de execução expõe o tempo de execução JavaScript por meio de objetos de avaliação e espelho remotos. Os resultados da avaliação são retornados como um objeto espelho que expõe o tipo de objeto, representação de cadeia de caracteres e identificador exclusivo que podem ser usados para referência de objeto posterior. Os objetos originais são mantidos na memória, a menos que eles sejam explicitamente liberados.
title: Domínio de tempo de execução-DevTools protocolo versão 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 710b3b3e0383f1f6feb7947e0468730d2e0b0e66
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882848"
---
# <span data-ttu-id="c506f-106">Domínio de tempo de execução-DevTools protocolo versão 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="c506f-106">Runtime Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="c506f-107">O domínio do tempo de execução expõe o tempo de execução JavaScript por meio de objetos de avaliação e espelho remotos.</span><span class="sxs-lookup"><span data-stu-id="c506f-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="c506f-108">Os resultados da avaliação são retornados como um objeto espelho que expõe o tipo de objeto, representação de cadeia de caracteres e identificador exclusivo que podem ser usados para referência de objeto posterior.</span><span class="sxs-lookup"><span data-stu-id="c506f-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="c506f-109">Os objetos originais são mantidos na memória, a menos que eles sejam explicitamente liberados.</span><span class="sxs-lookup"><span data-stu-id="c506f-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="c506f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="c506f-110">Methods</span></span>**](#methods) | <span data-ttu-id="c506f-111">[habilitar](#enable), [desabilitar](#disable), [avaliar](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [GetProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseobject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span><span class="sxs-lookup"><span data-stu-id="c506f-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span></span> |
| [**<span data-ttu-id="c506f-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="c506f-112">Events</span></span>**](#events) | <span data-ttu-id="c506f-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span><span class="sxs-lookup"><span data-stu-id="c506f-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span></span> |
| [**<span data-ttu-id="c506f-114">Tipos</span><span class="sxs-lookup"><span data-stu-id="c506f-114">Types</span></span>**](#types) | <span data-ttu-id="c506f-115">[Scriptid](#scriptid), [RemoteObjectId](#remoteobjectid), [unserializablevalue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [executioncontextid](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="c506f-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="c506f-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="c506f-116">Methods</span></span>

### <span data-ttu-id="c506f-117">Habilitar</span><span class="sxs-lookup"><span data-stu-id="c506f-117">enable</span></span>
<span data-ttu-id="c506f-118">Habilita o relatório dos <code>executionContextCreated</code> <code>executionContextDestroyed</code> eventos e <code>executionContextsCleared</code> .</span><span class="sxs-lookup"><span data-stu-id="c506f-118">Enables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span> <span data-ttu-id="c506f-119">Quando o relatório é ativado <code>executionContextCreated</code> , o evento será enviado imediatamente para cada contexto de execução existente.</span><span class="sxs-lookup"><span data-stu-id="c506f-119">When the reporting gets enabled the <code>executionContextCreated</code> event will be sent immediately for each existing execution context.</span></span>

</p>

---

### <span data-ttu-id="c506f-120">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="c506f-120">disable</span></span>
<span data-ttu-id="c506f-121">Desabilita o relatório dos <code>executionContextCreated</code> <code>executionContextDestroyed</code> <code>executionContextsCleared</code> eventos e.</span><span class="sxs-lookup"><span data-stu-id="c506f-121">Disables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span>

</p>

---

### <span data-ttu-id="c506f-122">retornará</span><span class="sxs-lookup"><span data-stu-id="c506f-122">evaluate</span></span>
<span data-ttu-id="c506f-123">Avalia a expressão no objeto global.</span><span class="sxs-lookup"><span data-stu-id="c506f-123">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c506f-124">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-125">Express</span><span class="sxs-lookup"><span data-stu-id="c506f-125">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c506f-126">Expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="c506f-126">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-127">includeCommandLineAPI</span><span class="sxs-lookup"><span data-stu-id="c506f-127">includeCommandLineAPI</span></span> <br/> <i><span data-ttu-id="c506f-128">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-128">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c506f-129">Determina se a API de linha de comando deve estar disponível durante a avaliação.</span><span class="sxs-lookup"><span data-stu-id="c506f-129">Determines whether Command Line API should be available during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-130">objeto de objeto</span><span class="sxs-lookup"><span data-stu-id="c506f-130">objectGroup</span></span> <br/> <i><span data-ttu-id="c506f-131">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-131">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c506f-132">Nome do grupo simbólico que pode ser usado para liberar vários objetos.</span><span class="sxs-lookup"><span data-stu-id="c506f-132">Symbolic group name that can be used to release multiple objects.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-133">silent</span><span class="sxs-lookup"><span data-stu-id="c506f-133">silent</span></span> <br/> <i><span data-ttu-id="c506f-134">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-134">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c506f-135">As exceções do modo silencioso lançadas durante a avaliação não são relatadas e não pausam a execução.</span><span class="sxs-lookup"><span data-stu-id="c506f-135">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="c506f-136">Substitui o <code>setPauseOnException</code> estado.</span><span class="sxs-lookup"><span data-stu-id="c506f-136">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-137">ContextId</span><span class="sxs-lookup"><span data-stu-id="c506f-137">contextId</span></span> <br/> <i><span data-ttu-id="c506f-138">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-138">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="c506f-139">Especifica em qual contexto de execução executar avaliação.</span><span class="sxs-lookup"><span data-stu-id="c506f-139">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="c506f-140">Se o parâmetro for omitido, a avaliação será executada no contexto da página inspecionada.</span><span class="sxs-lookup"><span data-stu-id="c506f-140">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-141">returnByValue</span><span class="sxs-lookup"><span data-stu-id="c506f-141">returnByValue</span></span> <br/> <i><span data-ttu-id="c506f-142">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-142">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c506f-143">Se é esperado que o resultado seja um objeto JSON que deve ser enviado por valor.</span><span class="sxs-lookup"><span data-stu-id="c506f-143">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-144">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="c506f-144">awaitPromise</span></span> <br/> <i><span data-ttu-id="c506f-145">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-145">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c506f-146">Se a execução deve <code>await</code> ser um valor resultante e retorna uma vez que a promessa esperada seja resolvida.</span><span class="sxs-lookup"><span data-stu-id="c506f-146">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-147">Devolver</span><span class="sxs-lookup"><span data-stu-id="c506f-147">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-148">levar</span><span class="sxs-lookup"><span data-stu-id="c506f-148">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="c506f-149">Resultado da avaliação.</span><span class="sxs-lookup"><span data-stu-id="c506f-149">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="c506f-150">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="c506f-150">callFunctionOn</span></span>
<span data-ttu-id="c506f-151">Função calls com declaração fornecida no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="c506f-151">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="c506f-152">O grupo de objetos do resultado é herdado do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="c506f-152">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-153">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c506f-153">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-154">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="c506f-154">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c506f-155">Declaração da função a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="c506f-155">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-156">objectId</span><span class="sxs-lookup"><span data-stu-id="c506f-156">objectId</span></span> <br/> <i><span data-ttu-id="c506f-157">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-157">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="c506f-158">Identificador do objeto no qual a função deve ser chamada.</span><span class="sxs-lookup"><span data-stu-id="c506f-158">Identifier of the object to call function on.</span></span> <span data-ttu-id="c506f-159">O objectId ou o executionContextid deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="c506f-159">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="c506f-160">objectId deve ser da função Runtime. Evaluate ().</span><span class="sxs-lookup"><span data-stu-id="c506f-160">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-161">arguments</span><span class="sxs-lookup"><span data-stu-id="c506f-161">arguments</span></span> <br/> <i><span data-ttu-id="c506f-162">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-162">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="c506f-163">Argumentos de chamada.</span><span class="sxs-lookup"><span data-stu-id="c506f-163">Call arguments.</span></span> <span data-ttu-id="c506f-164">Todos os argumentos de chamada devem pertencer ao mesmo mundo JavaScript que o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="c506f-164">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-165">silent</span><span class="sxs-lookup"><span data-stu-id="c506f-165">silent</span></span> <br/> <i><span data-ttu-id="c506f-166">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c506f-167">As exceções do modo silencioso lançadas durante a avaliação não são relatadas e não pausam a execução.</span><span class="sxs-lookup"><span data-stu-id="c506f-167">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="c506f-168">Substitui o <code>setPauseOnException</code> estado.</span><span class="sxs-lookup"><span data-stu-id="c506f-168">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-169">returnByValue</span><span class="sxs-lookup"><span data-stu-id="c506f-169">returnByValue</span></span> <br/> <i><span data-ttu-id="c506f-170">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-170">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c506f-171">Se é esperado que o resultado seja um objeto JSON que deve ser enviado por valor.</span><span class="sxs-lookup"><span data-stu-id="c506f-171">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-172">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="c506f-172">awaitPromise</span></span> <br/> <i><span data-ttu-id="c506f-173">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-173">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c506f-174">Se a execução deve <code>await</code> ser um valor resultante e retorna uma vez que a promessa esperada seja resolvida.</span><span class="sxs-lookup"><span data-stu-id="c506f-174">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-175">executionContextid</span><span class="sxs-lookup"><span data-stu-id="c506f-175">executionContextId</span></span> <br/> <i><span data-ttu-id="c506f-176">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-176">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="c506f-177">Especifica o contexto de execução em que o objeto global será usado para chamar a função.</span><span class="sxs-lookup"><span data-stu-id="c506f-177">Specifies execution context which global object will be used to call function on.</span></span> <span data-ttu-id="c506f-178">O executionContextid ou o objectId deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="c506f-178">Either executionContextId or objectId should be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-179">objeto de objeto</span><span class="sxs-lookup"><span data-stu-id="c506f-179">objectGroup</span></span> <br/> <i><span data-ttu-id="c506f-180">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-180">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c506f-181">Nome do grupo simbólico que pode ser usado para liberar vários objetos.</span><span class="sxs-lookup"><span data-stu-id="c506f-181">Symbolic group name that can be used to release multiple objects.</span></span> <span data-ttu-id="c506f-182">Se o objeto de objeto não for especificado e objectId for, o objeto de objeto será herdado do objeto.</span><span class="sxs-lookup"><span data-stu-id="c506f-182">If objectGroup is not specified and objectId is, objectGroup will be inherited from object.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-183">Devolver</span><span class="sxs-lookup"><span data-stu-id="c506f-183">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-184">levar</span><span class="sxs-lookup"><span data-stu-id="c506f-184">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="c506f-185">Resultado da chamada.</span><span class="sxs-lookup"><span data-stu-id="c506f-185">Call result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="c506f-186">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="c506f-186">awaitPromise</span></span>
<span data-ttu-id="c506f-187">Adicione o manipulador a promessa com a ID de objeto Promise fornecida.</span><span class="sxs-lookup"><span data-stu-id="c506f-187">Add handler to promise with given promise object id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-188">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c506f-188">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-189">promiseObjectId</span><span class="sxs-lookup"><span data-stu-id="c506f-189">promiseObjectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="c506f-190">Identificador da promessa.</span><span class="sxs-lookup"><span data-stu-id="c506f-190">Identifier of the promise.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-191">returnByValue</span><span class="sxs-lookup"><span data-stu-id="c506f-191">returnByValue</span></span> <br/> <i><span data-ttu-id="c506f-192">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-192">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c506f-193">Se é esperado que o resultado seja um objeto JSON que deve ser enviado por valor.</span><span class="sxs-lookup"><span data-stu-id="c506f-193">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-194">Devolver</span><span class="sxs-lookup"><span data-stu-id="c506f-194">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-195">levar</span><span class="sxs-lookup"><span data-stu-id="c506f-195">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="c506f-196">Resultado da promessa.</span><span class="sxs-lookup"><span data-stu-id="c506f-196">Promise result.</span></span>  <span data-ttu-id="c506f-197">Conterá o valor rejeitado se a promessa foi rejeitada.</span><span class="sxs-lookup"><span data-stu-id="c506f-197">Will contain rejected value if promise was rejected.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="c506f-198">GetProperties</span><span class="sxs-lookup"><span data-stu-id="c506f-198">getProperties</span></span>
<span data-ttu-id="c506f-199">Retorna as propriedades de um determinado objeto.</span><span class="sxs-lookup"><span data-stu-id="c506f-199">Returns properties of a given object.</span></span> <span data-ttu-id="c506f-200">O grupo de objetos do resultado é herdado do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="c506f-200">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-201">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c506f-201">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-202">objectId</span><span class="sxs-lookup"><span data-stu-id="c506f-202">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="c506f-203">Identificador do objeto para o qual as propriedades são retornadas.</span><span class="sxs-lookup"><span data-stu-id="c506f-203">Identifier of the object to return properties for.</span></span> <span data-ttu-id="c506f-204">objectId deve ser da função Debugger. evaluateOnCallFrame ().</span><span class="sxs-lookup"><span data-stu-id="c506f-204">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-205">ownProperties</span><span class="sxs-lookup"><span data-stu-id="c506f-205">ownProperties</span></span> <br/> <i><span data-ttu-id="c506f-206">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-206">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c506f-207">Se verdadeiro, retorna propriedades pertencentes somente ao elemento em si, não à sua cadeia de protótipos.</span><span class="sxs-lookup"><span data-stu-id="c506f-207">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-208">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="c506f-208">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="c506f-209">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-209">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="c506f-210">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="c506f-210">Experimental.</span></span> </b></span><span data-ttu-id="c506f-211">Se verdadeiro, retorna propriedades de assessor (somente com getter/setter); as propriedades internas também não são retornadas.</span><span class="sxs-lookup"><span data-stu-id="c506f-211">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-212">Devolver</span><span class="sxs-lookup"><span data-stu-id="c506f-212">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-213">levar</span><span class="sxs-lookup"><span data-stu-id="c506f-213">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="c506f-214">Propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="c506f-214">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="c506f-215">globalLexicalScopeNames</span><span class="sxs-lookup"><span data-stu-id="c506f-215">globalLexicalScopeNames</span></span>
<span data-ttu-id="c506f-216">Retorna todas as variáveis Let, const e Class do escopo global do console.</span><span class="sxs-lookup"><span data-stu-id="c506f-216">Returns all let, const, and class variables from the console global scope.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-217">Devolver</span><span class="sxs-lookup"><span data-stu-id="c506f-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-218">os</span><span class="sxs-lookup"><span data-stu-id="c506f-218">names</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="c506f-219">releaseobject</span><span class="sxs-lookup"><span data-stu-id="c506f-219">releaseObject</span></span>
<span data-ttu-id="c506f-220">Libera o objeto remoto com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="c506f-220">Releases remote object with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-221">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c506f-221">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-222">objectId</span><span class="sxs-lookup"><span data-stu-id="c506f-222">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="c506f-223">Identificador do objeto a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="c506f-223">Identifier of the object to release.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="c506f-224">releaseObjectGroup</span><span class="sxs-lookup"><span data-stu-id="c506f-224">releaseObjectGroup</span></span>
<span data-ttu-id="c506f-225">Libera todos os objetos remotos que pertencem a um determinado grupo.</span><span class="sxs-lookup"><span data-stu-id="c506f-225">Releases all remote objects that belong to a given group.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-226">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c506f-226">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-227">objeto de objeto</span><span class="sxs-lookup"><span data-stu-id="c506f-227">objectGroup</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c506f-228">Nome do grupo de objetos simbólico.</span><span class="sxs-lookup"><span data-stu-id="c506f-228">Symbolic object group name.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="c506f-229">discardConsoleEntries</span><span class="sxs-lookup"><span data-stu-id="c506f-229">discardConsoleEntries</span></span>
<span data-ttu-id="c506f-230">Descarta exceções coletadas e chamadas de API do console.</span><span class="sxs-lookup"><span data-stu-id="c506f-230">Discards collected exceptions and console API calls.</span></span>

</p>

---

## <span data-ttu-id="c506f-231">Eventos</span><span class="sxs-lookup"><span data-stu-id="c506f-231">Events</span></span>

### <span data-ttu-id="c506f-232">executionContextCreated</span><span class="sxs-lookup"><span data-stu-id="c506f-232">executionContextCreated</span></span>
<span data-ttu-id="c506f-233">Emitido quando um novo contexto de execução é criado.</span><span class="sxs-lookup"><span data-stu-id="c506f-233">Issued when new execution context is created.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-234">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c506f-234">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-235">atalho</span><span class="sxs-lookup"><span data-stu-id="c506f-235">context</span></span></td>
            <td><a href="#executioncontextdescription"><code class="flyout">ExecutionContextDescription</code></a></td>
            <td><span data-ttu-id="c506f-236">Um contexto de execução recém criado.</span><span class="sxs-lookup"><span data-stu-id="c506f-236">A newly created execution context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="c506f-237">executionContextDestroyed</span><span class="sxs-lookup"><span data-stu-id="c506f-237">executionContextDestroyed</span></span>
<span data-ttu-id="c506f-238">Emitido quando o contexto de execução é destruído.</span><span class="sxs-lookup"><span data-stu-id="c506f-238">Issued when execution context is destroyed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-239">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c506f-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-240">executionContextid</span><span class="sxs-lookup"><span data-stu-id="c506f-240">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="c506f-241">ID do contexto destruído</span><span class="sxs-lookup"><span data-stu-id="c506f-241">Id of the destroyed context</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="c506f-242">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="c506f-242">executionContextsCleared</span></span>
<span data-ttu-id="c506f-243">Emitido quando todos os executionContext foram limpos no navegador</span><span class="sxs-lookup"><span data-stu-id="c506f-243">Issued when all executionContexts were cleared in browser</span></span>

</p>

---

### <span data-ttu-id="c506f-244">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="c506f-244">exceptionThrown</span></span>
<span data-ttu-id="c506f-245">Emitido quando a exceção foi gerada e não tratada.</span><span class="sxs-lookup"><span data-stu-id="c506f-245">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-246">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c506f-246">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-247">carimbo</span><span class="sxs-lookup"><span data-stu-id="c506f-247">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="c506f-248">Carimbo de data/hora da exceção.</span><span class="sxs-lookup"><span data-stu-id="c506f-248">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-249">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="c506f-249">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="c506f-250">consoleAPICalled</span><span class="sxs-lookup"><span data-stu-id="c506f-250">consoleAPICalled</span></span>


<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-251">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c506f-251">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-252">tipo</span><span class="sxs-lookup"><span data-stu-id="c506f-252">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="c506f-253">Valores permitidos: log, info, aviso, erro, depuração, Assert, Table, Trace, dir, DirXML, Clear, Select, Count, countReset, timeEnd, timeStamp, Start, startGroupCollapsed, ENDGROUP</span><span class="sxs-lookup"><span data-stu-id="c506f-253">Allowed values: log, info, warning, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</span></span></i></td>
            <td><span data-ttu-id="c506f-254">Tipo de chamada.</span><span class="sxs-lookup"><span data-stu-id="c506f-254">Type of the call.</span></span> <span data-ttu-id="c506f-255">Isso inclui log, informações, Warn, erro, depuração, Assert, Table, Trace, dir, DirXML, Clear, Select, Count, countReset, timeEnd, Exception, timeStamp, Group, groupCollapsed, groupEnd.</span><span class="sxs-lookup"><span data-stu-id="c506f-255">This includes log, info, warn, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, exception, timeStamp, group, groupCollapsed, groupEnd.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-256">args</span><span class="sxs-lookup"><span data-stu-id="c506f-256">args</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject[]</code></a></td>
            <td><span data-ttu-id="c506f-257">Argumentos de chamada.</span><span class="sxs-lookup"><span data-stu-id="c506f-257">Call arguments.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-258">executionContextid</span><span class="sxs-lookup"><span data-stu-id="c506f-258">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="c506f-259">Identificador do contexto em que foi feita a chamada do console</span><span class="sxs-lookup"><span data-stu-id="c506f-259">Identifier of the context where console call was made</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-260">carimbo</span><span class="sxs-lookup"><span data-stu-id="c506f-260">timestamp</span></span> <br/> <i><span data-ttu-id="c506f-261">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-261">optional</span></span></i></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="c506f-262">Carimbo de data/hora da chamada.</span><span class="sxs-lookup"><span data-stu-id="c506f-262">Call timestamp.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-263">Pilha</span><span class="sxs-lookup"><span data-stu-id="c506f-263">stackTrace</span></span> <br/> <i><span data-ttu-id="c506f-264">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-264">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="c506f-265">Rastreamento de pilha capturado se disponível</span><span class="sxs-lookup"><span data-stu-id="c506f-265">Stack trace captured if available</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="c506f-266">Tipos</span><span class="sxs-lookup"><span data-stu-id="c506f-266">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="c506f-267">Scriptid</span><span class="sxs-lookup"><span data-stu-id="c506f-267">ScriptId</span></span> `string`

<span data-ttu-id="c506f-268">Identificador de script exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c506f-268">Unique script identifier.</span></span>

</p>

---

### <a name="remoteobjectid"></a> <span data-ttu-id="c506f-269">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="c506f-269">RemoteObjectId</span></span> `string`

<span data-ttu-id="c506f-270">Identificador de objeto exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c506f-270">Unique object identifier.</span></span>

</p>

---

### <a name="unserializablevalue"></a> <span data-ttu-id="c506f-271">Unserializablevalue</span><span class="sxs-lookup"><span data-stu-id="c506f-271">UnserializableValue</span></span> `string`

<span data-ttu-id="c506f-272">Valor primitivo que não pode ser JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="c506f-272">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="c506f-273">Valores permitidos</span><span class="sxs-lookup"><span data-stu-id="c506f-273">Allowed Values</span></span>
<span data-ttu-id="c506f-274">Infinito, NaN,-Infinity,-0</span><span class="sxs-lookup"><span data-stu-id="c506f-274">Infinity, NaN, -Infinity, -0</span></span>
</p>

---

### <a name="remoteobject"></a> <span data-ttu-id="c506f-275">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="c506f-275">RemoteObject</span></span> `object`

<span data-ttu-id="c506f-276">Objeto espelho que faz referência ao objeto JavaScript original.</span><span class="sxs-lookup"><span data-stu-id="c506f-276">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-277">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c506f-277">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-278">tipo</span><span class="sxs-lookup"><span data-stu-id="c506f-278">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="c506f-279">Valores permitidos: Object, Function, undefined, String, Number, booliano, símbolo</span><span class="sxs-lookup"><span data-stu-id="c506f-279">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="c506f-280">Tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="c506f-280">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-281">subtipo</span><span class="sxs-lookup"><span data-stu-id="c506f-281">subtype</span></span> <br/> <i><span data-ttu-id="c506f-282">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-282">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="c506f-283">Valores permitidos: NULL, Error, Promise, Node</span><span class="sxs-lookup"><span data-stu-id="c506f-283">Allowed values: null, error, promise, node</span></span></i></td>
            <td><span data-ttu-id="c506f-284">Dica de subtipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="c506f-284">Object subtype hint.</span></span> <span data-ttu-id="c506f-285">Especificado <code>object</code> apenas para valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="c506f-285">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-286">Classe</span><span class="sxs-lookup"><span data-stu-id="c506f-286">className</span></span> <br/> <i><span data-ttu-id="c506f-287">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-287">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c506f-288">Nome do Construtor (classe objeto).</span><span class="sxs-lookup"><span data-stu-id="c506f-288">Object class (constructor) name.</span></span> <span data-ttu-id="c506f-289">Especificado <code>object</code> apenas para valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="c506f-289">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-290">value</span><span class="sxs-lookup"><span data-stu-id="c506f-290">value</span></span> <br/> <i><span data-ttu-id="c506f-291">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-291">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="c506f-292">Valor do objeto remoto em caso de valores primitivos ou valores JSON (se for solicitado).</span><span class="sxs-lookup"><span data-stu-id="c506f-292">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-293">unserializablevalue</span><span class="sxs-lookup"><span data-stu-id="c506f-293">unserializableValue</span></span> <br/> <i><span data-ttu-id="c506f-294">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-294">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="c506f-295">Um valor primitivo que não pode ser JSON-stringified não tem</span><span class="sxs-lookup"><span data-stu-id="c506f-295">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="c506f-296">, mas obtém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c506f-296">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-297">description</span><span class="sxs-lookup"><span data-stu-id="c506f-297">description</span></span> <br/> <i><span data-ttu-id="c506f-298">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-298">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c506f-299">Representação de cadeia de caracteres do objeto.</span><span class="sxs-lookup"><span data-stu-id="c506f-299">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-300">objectId</span><span class="sxs-lookup"><span data-stu-id="c506f-300">objectId</span></span> <br/> <i><span data-ttu-id="c506f-301">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-301">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="c506f-302">Identificador de objeto exclusivo (para valores não primitivos).</span><span class="sxs-lookup"><span data-stu-id="c506f-302">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-303">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="c506f-303">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="c506f-304">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-304">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="c506f-305">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="c506f-305">Experimental.</span></span> </b></span><span data-ttu-id="c506f-306">Microsoft: a ID de Propriedade do depurador associado a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="c506f-306">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="c506f-307">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="c506f-307">PropertyDescriptor</span></span> `object`

<span data-ttu-id="c506f-308">Descritor de propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="c506f-308">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-309">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c506f-309">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-310">name</span><span class="sxs-lookup"><span data-stu-id="c506f-310">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c506f-311">Nome da propriedade ou descrição do símbolo.</span><span class="sxs-lookup"><span data-stu-id="c506f-311">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-312">value</span><span class="sxs-lookup"><span data-stu-id="c506f-312">value</span></span> <br/> <i><span data-ttu-id="c506f-313">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-313">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="c506f-314">O valor associado à propriedade.</span><span class="sxs-lookup"><span data-stu-id="c506f-314">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-315">gravável</span><span class="sxs-lookup"><span data-stu-id="c506f-315">writable</span></span> <br/> <i><span data-ttu-id="c506f-316">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-316">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c506f-317">Verdadeiro se o valor associado à propriedade pode ser alterado (somente descritores de dados).</span><span class="sxs-lookup"><span data-stu-id="c506f-317">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-318">obter</span><span class="sxs-lookup"><span data-stu-id="c506f-318">get</span></span> <br/> <i><span data-ttu-id="c506f-319">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-319">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="c506f-320">Uma função que serve como um getter para a propriedade, ou <code>undefined</code> se não houver nenhum getter (somente descritores de acessador).</span><span class="sxs-lookup"><span data-stu-id="c506f-320">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-321">set</span><span class="sxs-lookup"><span data-stu-id="c506f-321">set</span></span> <br/> <i><span data-ttu-id="c506f-322">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-322">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="c506f-323">Uma função que serve como um setter para a propriedade ou <code>undefined</code> se não houver nenhum setter (somente descritores de acesso).</span><span class="sxs-lookup"><span data-stu-id="c506f-323">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-324">configurável</span><span class="sxs-lookup"><span data-stu-id="c506f-324">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c506f-325">True se o tipo desse descritor de propriedades pode ser alterado e se a propriedade pode ser excluída do objeto correspondente.</span><span class="sxs-lookup"><span data-stu-id="c506f-325">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-326">enumer</span><span class="sxs-lookup"><span data-stu-id="c506f-326">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c506f-327">Verdadeiro se essa propriedade aparecer durante a enumeração das propriedades no objeto correspondente.</span><span class="sxs-lookup"><span data-stu-id="c506f-327">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-328">wasThrown</span><span class="sxs-lookup"><span data-stu-id="c506f-328">wasThrown</span></span> <br/> <i><span data-ttu-id="c506f-329">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-329">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c506f-330">Verdadeiro se o resultado foi lançado durante a avaliação.</span><span class="sxs-lookup"><span data-stu-id="c506f-330">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-331">isOwn</span><span class="sxs-lookup"><span data-stu-id="c506f-331">isOwn</span></span> <br/> <i><span data-ttu-id="c506f-332">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-332">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c506f-333">Verdadeiro se a propriedade for proprietária para o objeto.</span><span class="sxs-lookup"><span data-stu-id="c506f-333">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-334">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="c506f-334">msReturnValue</span></span> <br/> <i><span data-ttu-id="c506f-335">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-335">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="c506f-336">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="c506f-336">Experimental.</span></span> </b></span><span data-ttu-id="c506f-337">Microsoft: true se a propriedade for um valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="c506f-337">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-338">symbol</span><span class="sxs-lookup"><span data-stu-id="c506f-338">symbol</span></span> <br/> <i><span data-ttu-id="c506f-339">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-339">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="c506f-340">Objeto de símbolo de propriedade, se a propriedade for do `symbol` tipo.</span><span class="sxs-lookup"><span data-stu-id="c506f-340">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callargument"></a> <span data-ttu-id="c506f-341">CallArgument</span><span class="sxs-lookup"><span data-stu-id="c506f-341">CallArgument</span></span> `object`

<span data-ttu-id="c506f-342">Representa o argumento de chamada de função.</span><span class="sxs-lookup"><span data-stu-id="c506f-342">Represents function call argument.</span></span> <span data-ttu-id="c506f-343">A ID de objeto remoto <code>objectId</code> , primitiva <code>value</code> , valor primitivo não serializável ou nenhum dos (para Undefined) eles devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="c506f-343">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-344">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c506f-344">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-345">value</span><span class="sxs-lookup"><span data-stu-id="c506f-345">value</span></span> <br/> <i><span data-ttu-id="c506f-346">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-346">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="c506f-347">Valor primitivo ou objeto JavaScript serializável.</span><span class="sxs-lookup"><span data-stu-id="c506f-347">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-348">unserializablevalue</span><span class="sxs-lookup"><span data-stu-id="c506f-348">unserializableValue</span></span> <br/> <i><span data-ttu-id="c506f-349">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-349">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="c506f-350">Valor primitivo que não pode ser JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="c506f-350">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-351">objectId</span><span class="sxs-lookup"><span data-stu-id="c506f-351">objectId</span></span> <br/> <i><span data-ttu-id="c506f-352">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-352">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="c506f-353">Identificador de objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="c506f-353">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="executioncontextid"></a> <span data-ttu-id="c506f-354">ExecutionContextid</span><span class="sxs-lookup"><span data-stu-id="c506f-354">ExecutionContextId</span></span> `integer`

<span data-ttu-id="c506f-355">ID de um contexto de execução.</span><span class="sxs-lookup"><span data-stu-id="c506f-355">Id of an execution context.</span></span>

</p>

---

### <a name="executioncontextdescription"></a> <span data-ttu-id="c506f-356">ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="c506f-356">ExecutionContextDescription</span></span> `object`

<span data-ttu-id="c506f-357">Descrição de um mundo isolado.</span><span class="sxs-lookup"><span data-stu-id="c506f-357">Description of an isolated world.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-358">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c506f-358">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-359">id</span><span class="sxs-lookup"><span data-stu-id="c506f-359">id</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="c506f-360">ID exclusiva do contexto de execução.</span><span class="sxs-lookup"><span data-stu-id="c506f-360">Unique id of the execution context.</span></span> <span data-ttu-id="c506f-361">Ele pode ser usado para especificar em qual execução a avaliação de script de contexto deve ser realizada.</span><span class="sxs-lookup"><span data-stu-id="c506f-361">It can be used to specify in which execution context script evaluation should be performed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-362">Origin</span><span class="sxs-lookup"><span data-stu-id="c506f-362">origin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c506f-363">Origem do contexto de execução.</span><span class="sxs-lookup"><span data-stu-id="c506f-363">Execution context origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-364">name</span><span class="sxs-lookup"><span data-stu-id="c506f-364">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c506f-365">Nome legível pelo homem descrevendo o contexto determinado.</span><span class="sxs-lookup"><span data-stu-id="c506f-365">Human readable name describing given context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="exceptiondetails"></a> <span data-ttu-id="c506f-366">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="c506f-366">ExceptionDetails</span></span> `object`

<span data-ttu-id="c506f-367">Informações detalhadas sobre exceção (ou erro) que foi lançada durante a compilação ou execução de scripts.</span><span class="sxs-lookup"><span data-stu-id="c506f-367">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-368">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c506f-368">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-369">exceptionid</span><span class="sxs-lookup"><span data-stu-id="c506f-369">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="c506f-370">ID da exceção.</span><span class="sxs-lookup"><span data-stu-id="c506f-370">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-371">texto</span><span class="sxs-lookup"><span data-stu-id="c506f-371">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c506f-372">Texto de exceção, que deve ser usado em conjunto com o objeto de exceção quando disponível.</span><span class="sxs-lookup"><span data-stu-id="c506f-372">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-373">lineNumber</span><span class="sxs-lookup"><span data-stu-id="c506f-373">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="c506f-374">Número da linha do local da exceção (com base em 0).</span><span class="sxs-lookup"><span data-stu-id="c506f-374">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-375">columnNumber</span><span class="sxs-lookup"><span data-stu-id="c506f-375">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="c506f-376">Número da coluna do local da exceção (com base em 0).</span><span class="sxs-lookup"><span data-stu-id="c506f-376">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-377">scriptid</span><span class="sxs-lookup"><span data-stu-id="c506f-377">scriptId</span></span> <br/> <i><span data-ttu-id="c506f-378">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-378">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="c506f-379">ID do script do local da exceção.</span><span class="sxs-lookup"><span data-stu-id="c506f-379">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-380">url</span><span class="sxs-lookup"><span data-stu-id="c506f-380">url</span></span> <br/> <i><span data-ttu-id="c506f-381">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-381">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c506f-382">URL do local da exceção, a ser usado quando o script não foi reportado.</span><span class="sxs-lookup"><span data-stu-id="c506f-382">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-383">Pilha</span><span class="sxs-lookup"><span data-stu-id="c506f-383">stackTrace</span></span> <br/> <i><span data-ttu-id="c506f-384">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-384">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="c506f-385">Rastreamento de pilha JavaScript, se disponível.</span><span class="sxs-lookup"><span data-stu-id="c506f-385">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-386">extremamente</span><span class="sxs-lookup"><span data-stu-id="c506f-386">exception</span></span> <br/> <i><span data-ttu-id="c506f-387">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-387">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="c506f-388">Objeto de exceção, se disponível.</span><span class="sxs-lookup"><span data-stu-id="c506f-388">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-389">executionContextid</span><span class="sxs-lookup"><span data-stu-id="c506f-389">executionContextId</span></span> <br/> <i><span data-ttu-id="c506f-390">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-390">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="c506f-391">Identificador do contexto em que ocorreu a exceção.</span><span class="sxs-lookup"><span data-stu-id="c506f-391">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="timestamp"></a> <span data-ttu-id="c506f-392">Carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="c506f-392">Timestamp</span></span> `integer`

<span data-ttu-id="c506f-393">Número de milissegundos desde a época.</span><span class="sxs-lookup"><span data-stu-id="c506f-393">Number of milliseconds since epoch.</span></span>

</p>

---

### <a name="callframe"></a> <span data-ttu-id="c506f-394">CallFrame</span><span class="sxs-lookup"><span data-stu-id="c506f-394">CallFrame</span></span> `object`

<span data-ttu-id="c506f-395">Entrada de pilha para erros e asserções de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="c506f-395">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-396">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c506f-396">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-397">função FunctionName</span><span class="sxs-lookup"><span data-stu-id="c506f-397">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c506f-398">Nome da função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c506f-398">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-399">scriptid</span><span class="sxs-lookup"><span data-stu-id="c506f-399">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="c506f-400">Identificação do script JavaScript. O scriptid estará vazio se o depurador não estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="c506f-400">JavaScript script id. ScriptId will be empty if debugger is not enabled.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-401">url</span><span class="sxs-lookup"><span data-stu-id="c506f-401">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c506f-402">Nome ou URL do script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c506f-402">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-403">lineNumber</span><span class="sxs-lookup"><span data-stu-id="c506f-403">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="c506f-404">Número da linha de script JavaScript (com base em 0).</span><span class="sxs-lookup"><span data-stu-id="c506f-404">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-405">columnNumber</span><span class="sxs-lookup"><span data-stu-id="c506f-405">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="c506f-406">Número da coluna de script JavaScript (baseado em 0).</span><span class="sxs-lookup"><span data-stu-id="c506f-406">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="stacktrace"></a> <span data-ttu-id="c506f-407">Pilha</span><span class="sxs-lookup"><span data-stu-id="c506f-407">StackTrace</span></span> `object`

<span data-ttu-id="c506f-408">Quadros de chamadas para asserções ou mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="c506f-408">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c506f-409">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c506f-409">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c506f-410">description</span><span class="sxs-lookup"><span data-stu-id="c506f-410">description</span></span> <br/> <i><span data-ttu-id="c506f-411">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-411">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c506f-412">Rótulo de cadeia de caracteres deste rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="c506f-412">String label of this stack trace.</span></span> <span data-ttu-id="c506f-413">Para rastreamentos assíncronos, pode ser um nome da função que iniciou a chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="c506f-413">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-414">callFrames</span><span class="sxs-lookup"><span data-stu-id="c506f-414">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="c506f-415">Nome da função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c506f-415">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c506f-416">mãe</span><span class="sxs-lookup"><span data-stu-id="c506f-416">parent</span></span> <br/> <i><span data-ttu-id="c506f-417">opcional</span><span class="sxs-lookup"><span data-stu-id="c506f-417">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="c506f-418">Rastreamento de pilha JavaScript assíncrono que precede esta pilha, se disponível.</span><span class="sxs-lookup"><span data-stu-id="c506f-418">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
