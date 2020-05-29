---
description: Referência para o domínio de tempo de execução. O domínio do tempo de execução expõe o tempo de execução JavaScript por meio de objetos de avaliação e espelho remotos. Os resultados da avaliação são retornados como um objeto espelho que expõe o tipo de objeto, representação de cadeia de caracteres e identificador exclusivo que podem ser usados para referência de objeto posterior. Os objetos originais são mantidos na memória, a menos que eles sejam explicitamente liberados.
title: Domínio de tempo de execução – versão 0,2 do protocolo DevTools
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 504f944f7a8389450685b40cdd010b54c3a7ba4e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561328"
---
# <span data-ttu-id="5074d-106">Classpath</span><span class="sxs-lookup"><span data-stu-id="5074d-106">Runtime</span></span>
<span data-ttu-id="5074d-107">O domínio do tempo de execução expõe o tempo de execução JavaScript por meio de objetos de avaliação e espelho remotos.</span><span class="sxs-lookup"><span data-stu-id="5074d-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="5074d-108">Os resultados da avaliação são retornados como um objeto espelho que expõe o tipo de objeto, representação de cadeia de caracteres e identificador exclusivo que podem ser usados para referência de objeto posterior.</span><span class="sxs-lookup"><span data-stu-id="5074d-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="5074d-109">Os objetos originais são mantidos na memória, a menos que eles sejam explicitamente liberados.</span><span class="sxs-lookup"><span data-stu-id="5074d-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="5074d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="5074d-110">Methods</span></span>**](#methods) | <span data-ttu-id="5074d-111">[habilitar](#enable), [desabilitar](#disable), [avaliar](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [GetProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseobject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span><span class="sxs-lookup"><span data-stu-id="5074d-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span></span> |
| [**<span data-ttu-id="5074d-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="5074d-112">Events</span></span>**](#events) | <span data-ttu-id="5074d-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span><span class="sxs-lookup"><span data-stu-id="5074d-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span></span> |
| [**<span data-ttu-id="5074d-114">Tipos</span><span class="sxs-lookup"><span data-stu-id="5074d-114">Types</span></span>**](#types) | <span data-ttu-id="5074d-115">[Scriptid](#scriptid), [RemoteObjectId](#remoteobjectid), [unserializablevalue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [executioncontextid](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="5074d-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="5074d-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="5074d-116">Methods</span></span>

### <span data-ttu-id="5074d-117">Habilitar</span><span class="sxs-lookup"><span data-stu-id="5074d-117">enable</span></span>
<span data-ttu-id="5074d-118">Habilita o relatório dos <code>executionContextCreated</code> <code>executionContextDestroyed</code> eventos e <code>executionContextsCleared</code> .</span><span class="sxs-lookup"><span data-stu-id="5074d-118">Enables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span> <span data-ttu-id="5074d-119">Quando o relatório é ativado <code>executionContextCreated</code> , o evento será enviado imediatamente para cada contexto de execução existente.</span><span class="sxs-lookup"><span data-stu-id="5074d-119">When the reporting gets enabled the <code>executionContextCreated</code> event will be sent immediately for each existing execution context.</span></span>

</p>

---

### <span data-ttu-id="5074d-120">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="5074d-120">disable</span></span>
<span data-ttu-id="5074d-121">Desabilita o relatório dos <code>executionContextCreated</code> <code>executionContextDestroyed</code> <code>executionContextsCleared</code> eventos e.</span><span class="sxs-lookup"><span data-stu-id="5074d-121">Disables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span>

</p>

---

### <span data-ttu-id="5074d-122">retornará</span><span class="sxs-lookup"><span data-stu-id="5074d-122">evaluate</span></span>
<span data-ttu-id="5074d-123">Avalia a expressão no objeto global.</span><span class="sxs-lookup"><span data-stu-id="5074d-123">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5074d-124">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-125">Express</span><span class="sxs-lookup"><span data-stu-id="5074d-125">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5074d-126">Expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="5074d-126">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-127">includeCommandLineAPI</span><span class="sxs-lookup"><span data-stu-id="5074d-127">includeCommandLineAPI</span></span> <br/> <i><span data-ttu-id="5074d-128">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-128">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="5074d-129">Determina se a API de linha de comando deve estar disponível durante a avaliação.</span><span class="sxs-lookup"><span data-stu-id="5074d-129">Determines whether Command Line API should be available during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-130">objeto de objeto</span><span class="sxs-lookup"><span data-stu-id="5074d-130">objectGroup</span></span> <br/> <i><span data-ttu-id="5074d-131">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-131">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5074d-132">Nome do grupo simbólico que pode ser usado para liberar vários objetos.</span><span class="sxs-lookup"><span data-stu-id="5074d-132">Symbolic group name that can be used to release multiple objects.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-133">silent</span><span class="sxs-lookup"><span data-stu-id="5074d-133">silent</span></span> <br/> <i><span data-ttu-id="5074d-134">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-134">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="5074d-135">As exceções do modo silencioso lançadas durante a avaliação não são relatadas e não pausam a execução.</span><span class="sxs-lookup"><span data-stu-id="5074d-135">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="5074d-136">Substitui o <code>setPauseOnException</code> estado.</span><span class="sxs-lookup"><span data-stu-id="5074d-136">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-137">ContextId</span><span class="sxs-lookup"><span data-stu-id="5074d-137">contextId</span></span> <br/> <i><span data-ttu-id="5074d-138">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-138">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="5074d-139">Especifica em qual contexto de execução executar avaliação.</span><span class="sxs-lookup"><span data-stu-id="5074d-139">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="5074d-140">Se o parâmetro for omitido, a avaliação será executada no contexto da página inspecionada.</span><span class="sxs-lookup"><span data-stu-id="5074d-140">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-141">returnByValue</span><span class="sxs-lookup"><span data-stu-id="5074d-141">returnByValue</span></span> <br/> <i><span data-ttu-id="5074d-142">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-142">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="5074d-143">Se é esperado que o resultado seja um objeto JSON que deve ser enviado por valor.</span><span class="sxs-lookup"><span data-stu-id="5074d-143">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-144">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="5074d-144">awaitPromise</span></span> <br/> <i><span data-ttu-id="5074d-145">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-145">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="5074d-146">Se a execução deve <code>await</code> ser um valor resultante e retorna uma vez que a promessa esperada seja resolvida.</span><span class="sxs-lookup"><span data-stu-id="5074d-146">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-147">Devolver</span><span class="sxs-lookup"><span data-stu-id="5074d-147">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-148">levar</span><span class="sxs-lookup"><span data-stu-id="5074d-148">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="5074d-149">Resultado da avaliação.</span><span class="sxs-lookup"><span data-stu-id="5074d-149">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="5074d-150">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="5074d-150">callFunctionOn</span></span>
<span data-ttu-id="5074d-151">Função calls com declaração fornecida no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="5074d-151">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="5074d-152">O grupo de objetos do resultado é herdado do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="5074d-152">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-153">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5074d-153">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-154">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="5074d-154">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5074d-155">Declaração da função a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="5074d-155">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-156">objectId</span><span class="sxs-lookup"><span data-stu-id="5074d-156">objectId</span></span> <br/> <i><span data-ttu-id="5074d-157">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-157">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="5074d-158">Identificador do objeto no qual a função deve ser chamada.</span><span class="sxs-lookup"><span data-stu-id="5074d-158">Identifier of the object to call function on.</span></span> <span data-ttu-id="5074d-159">O objectId ou o executionContextid deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="5074d-159">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="5074d-160">objectId deve ser da função Runtime. Evaluate ().</span><span class="sxs-lookup"><span data-stu-id="5074d-160">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-161">arguments</span><span class="sxs-lookup"><span data-stu-id="5074d-161">arguments</span></span> <br/> <i><span data-ttu-id="5074d-162">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-162">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="5074d-163">Argumentos de chamada.</span><span class="sxs-lookup"><span data-stu-id="5074d-163">Call arguments.</span></span> <span data-ttu-id="5074d-164">Todos os argumentos de chamada devem pertencer ao mesmo mundo JavaScript que o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="5074d-164">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-165">silent</span><span class="sxs-lookup"><span data-stu-id="5074d-165">silent</span></span> <br/> <i><span data-ttu-id="5074d-166">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="5074d-167">As exceções do modo silencioso lançadas durante a avaliação não são relatadas e não pausam a execução.</span><span class="sxs-lookup"><span data-stu-id="5074d-167">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="5074d-168">Substitui o <code>setPauseOnException</code> estado.</span><span class="sxs-lookup"><span data-stu-id="5074d-168">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-169">returnByValue</span><span class="sxs-lookup"><span data-stu-id="5074d-169">returnByValue</span></span> <br/> <i><span data-ttu-id="5074d-170">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-170">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="5074d-171">Se é esperado que o resultado seja um objeto JSON que deve ser enviado por valor.</span><span class="sxs-lookup"><span data-stu-id="5074d-171">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-172">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="5074d-172">awaitPromise</span></span> <br/> <i><span data-ttu-id="5074d-173">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-173">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="5074d-174">Se a execução deve <code>await</code> ser um valor resultante e retorna uma vez que a promessa esperada seja resolvida.</span><span class="sxs-lookup"><span data-stu-id="5074d-174">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-175">executionContextid</span><span class="sxs-lookup"><span data-stu-id="5074d-175">executionContextId</span></span> <br/> <i><span data-ttu-id="5074d-176">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-176">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="5074d-177">Especifica o contexto de execução em que o objeto global será usado para chamar a função.</span><span class="sxs-lookup"><span data-stu-id="5074d-177">Specifies execution context which global object will be used to call function on.</span></span> <span data-ttu-id="5074d-178">O executionContextid ou o objectId deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="5074d-178">Either executionContextId or objectId should be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-179">objeto de objeto</span><span class="sxs-lookup"><span data-stu-id="5074d-179">objectGroup</span></span> <br/> <i><span data-ttu-id="5074d-180">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-180">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5074d-181">Nome do grupo simbólico que pode ser usado para liberar vários objetos.</span><span class="sxs-lookup"><span data-stu-id="5074d-181">Symbolic group name that can be used to release multiple objects.</span></span> <span data-ttu-id="5074d-182">Se o objeto de objeto não for especificado e objectId for, o objeto de objeto será herdado do objeto.</span><span class="sxs-lookup"><span data-stu-id="5074d-182">If objectGroup is not specified and objectId is, objectGroup will be inherited from object.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-183">Devolver</span><span class="sxs-lookup"><span data-stu-id="5074d-183">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-184">levar</span><span class="sxs-lookup"><span data-stu-id="5074d-184">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="5074d-185">Resultado da chamada.</span><span class="sxs-lookup"><span data-stu-id="5074d-185">Call result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="5074d-186">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="5074d-186">awaitPromise</span></span>
<span data-ttu-id="5074d-187">Adicione o manipulador a promessa com a ID de objeto Promise fornecida.</span><span class="sxs-lookup"><span data-stu-id="5074d-187">Add handler to promise with given promise object id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-188">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5074d-188">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-189">promiseObjectId</span><span class="sxs-lookup"><span data-stu-id="5074d-189">promiseObjectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="5074d-190">Identificador da promessa.</span><span class="sxs-lookup"><span data-stu-id="5074d-190">Identifier of the promise.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-191">returnByValue</span><span class="sxs-lookup"><span data-stu-id="5074d-191">returnByValue</span></span> <br/> <i><span data-ttu-id="5074d-192">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-192">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="5074d-193">Se é esperado que o resultado seja um objeto JSON que deve ser enviado por valor.</span><span class="sxs-lookup"><span data-stu-id="5074d-193">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-194">Devolver</span><span class="sxs-lookup"><span data-stu-id="5074d-194">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-195">levar</span><span class="sxs-lookup"><span data-stu-id="5074d-195">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="5074d-196">Resultado da promessa.</span><span class="sxs-lookup"><span data-stu-id="5074d-196">Promise result.</span></span>  <span data-ttu-id="5074d-197">Conterá o valor rejeitado se a promessa foi rejeitada.</span><span class="sxs-lookup"><span data-stu-id="5074d-197">Will contain rejected value if promise was rejected.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="5074d-198">GetProperties</span><span class="sxs-lookup"><span data-stu-id="5074d-198">getProperties</span></span>
<span data-ttu-id="5074d-199">Retorna as propriedades de um determinado objeto.</span><span class="sxs-lookup"><span data-stu-id="5074d-199">Returns properties of a given object.</span></span> <span data-ttu-id="5074d-200">O grupo de objetos do resultado é herdado do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="5074d-200">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-201">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5074d-201">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-202">objectId</span><span class="sxs-lookup"><span data-stu-id="5074d-202">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="5074d-203">Identificador do objeto para o qual as propriedades são retornadas.</span><span class="sxs-lookup"><span data-stu-id="5074d-203">Identifier of the object to return properties for.</span></span> <span data-ttu-id="5074d-204">objectId deve ser da função Debugger. evaluateOnCallFrame ().</span><span class="sxs-lookup"><span data-stu-id="5074d-204">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-205">ownProperties</span><span class="sxs-lookup"><span data-stu-id="5074d-205">ownProperties</span></span> <br/> <i><span data-ttu-id="5074d-206">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-206">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="5074d-207">Se verdadeiro, retorna propriedades pertencentes somente ao elemento em si, não à sua cadeia de protótipos.</span><span class="sxs-lookup"><span data-stu-id="5074d-207">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-208">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="5074d-208">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="5074d-209">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-209">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="5074d-210">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="5074d-210">Experimental.</span></span> </b></span><span data-ttu-id="5074d-211">Se verdadeiro, retorna propriedades de assessor (somente com getter/setter); as propriedades internas também não são retornadas.</span><span class="sxs-lookup"><span data-stu-id="5074d-211">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-212">Devolver</span><span class="sxs-lookup"><span data-stu-id="5074d-212">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-213">levar</span><span class="sxs-lookup"><span data-stu-id="5074d-213">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="5074d-214">Propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="5074d-214">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="5074d-215">globalLexicalScopeNames</span><span class="sxs-lookup"><span data-stu-id="5074d-215">globalLexicalScopeNames</span></span>
<span data-ttu-id="5074d-216">Retorna todas as variáveis Let, const e Class do escopo global do console.</span><span class="sxs-lookup"><span data-stu-id="5074d-216">Returns all let, const, and class variables from the console global scope.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-217">Devolver</span><span class="sxs-lookup"><span data-stu-id="5074d-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-218">os</span><span class="sxs-lookup"><span data-stu-id="5074d-218">names</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="5074d-219">releaseobject</span><span class="sxs-lookup"><span data-stu-id="5074d-219">releaseObject</span></span>
<span data-ttu-id="5074d-220">Libera o objeto remoto com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="5074d-220">Releases remote object with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-221">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5074d-221">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-222">objectId</span><span class="sxs-lookup"><span data-stu-id="5074d-222">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="5074d-223">Identificador do objeto a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="5074d-223">Identifier of the object to release.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="5074d-224">releaseObjectGroup</span><span class="sxs-lookup"><span data-stu-id="5074d-224">releaseObjectGroup</span></span>
<span data-ttu-id="5074d-225">Libera todos os objetos remotos que pertencem a um determinado grupo.</span><span class="sxs-lookup"><span data-stu-id="5074d-225">Releases all remote objects that belong to a given group.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-226">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5074d-226">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-227">objeto de objeto</span><span class="sxs-lookup"><span data-stu-id="5074d-227">objectGroup</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5074d-228">Nome do grupo de objetos simbólico.</span><span class="sxs-lookup"><span data-stu-id="5074d-228">Symbolic object group name.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="5074d-229">discardConsoleEntries</span><span class="sxs-lookup"><span data-stu-id="5074d-229">discardConsoleEntries</span></span>
<span data-ttu-id="5074d-230">Descarta exceções coletadas e chamadas de API do console.</span><span class="sxs-lookup"><span data-stu-id="5074d-230">Discards collected exceptions and console API calls.</span></span>

</p>

---

## <span data-ttu-id="5074d-231">Eventos</span><span class="sxs-lookup"><span data-stu-id="5074d-231">Events</span></span>

### <span data-ttu-id="5074d-232">executionContextCreated</span><span class="sxs-lookup"><span data-stu-id="5074d-232">executionContextCreated</span></span>
<span data-ttu-id="5074d-233">Emitido quando um novo contexto de execução é criado.</span><span class="sxs-lookup"><span data-stu-id="5074d-233">Issued when new execution context is created.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-234">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5074d-234">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-235">atalho</span><span class="sxs-lookup"><span data-stu-id="5074d-235">context</span></span></td>
            <td><a href="#executioncontextdescription"><code class="flyout">ExecutionContextDescription</code></a></td>
            <td><span data-ttu-id="5074d-236">Um contexto de execução recém criado.</span><span class="sxs-lookup"><span data-stu-id="5074d-236">A newly created execution context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="5074d-237">executionContextDestroyed</span><span class="sxs-lookup"><span data-stu-id="5074d-237">executionContextDestroyed</span></span>
<span data-ttu-id="5074d-238">Emitido quando o contexto de execução é destruído.</span><span class="sxs-lookup"><span data-stu-id="5074d-238">Issued when execution context is destroyed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-239">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5074d-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-240">executionContextid</span><span class="sxs-lookup"><span data-stu-id="5074d-240">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="5074d-241">ID do contexto destruído</span><span class="sxs-lookup"><span data-stu-id="5074d-241">Id of the destroyed context</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="5074d-242">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="5074d-242">executionContextsCleared</span></span>
<span data-ttu-id="5074d-243">Emitido quando todos os executionContext foram limpos no navegador</span><span class="sxs-lookup"><span data-stu-id="5074d-243">Issued when all executionContexts were cleared in browser</span></span>

</p>

---

### <span data-ttu-id="5074d-244">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="5074d-244">exceptionThrown</span></span>
<span data-ttu-id="5074d-245">Emitido quando a exceção foi gerada e não tratada.</span><span class="sxs-lookup"><span data-stu-id="5074d-245">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-246">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5074d-246">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-247">carimbo</span><span class="sxs-lookup"><span data-stu-id="5074d-247">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="5074d-248">Carimbo de data/hora da exceção.</span><span class="sxs-lookup"><span data-stu-id="5074d-248">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-249">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="5074d-249">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="5074d-250">consoleAPICalled</span><span class="sxs-lookup"><span data-stu-id="5074d-250">consoleAPICalled</span></span>


<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-251">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5074d-251">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-252">tipo</span><span class="sxs-lookup"><span data-stu-id="5074d-252">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="5074d-253">Valores permitidos: log, info, aviso, erro, depuração, Assert, Table, Trace, dir, DirXML, Clear, Select, Count, countReset, timeEnd, timeStamp, Start, startGroupCollapsed, ENDGROUP</span><span class="sxs-lookup"><span data-stu-id="5074d-253">Allowed values: log, info, warning, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</span></span></i></td>
            <td><span data-ttu-id="5074d-254">Tipo de chamada.</span><span class="sxs-lookup"><span data-stu-id="5074d-254">Type of the call.</span></span> <span data-ttu-id="5074d-255">Isso inclui log, informações, Warn, erro, depuração, Assert, Table, Trace, dir, DirXML, Clear, Select, Count, countReset, timeEnd, Exception, timeStamp, Group, groupCollapsed, groupEnd.</span><span class="sxs-lookup"><span data-stu-id="5074d-255">This includes log, info, warn, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, exception, timeStamp, group, groupCollapsed, groupEnd.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-256">args</span><span class="sxs-lookup"><span data-stu-id="5074d-256">args</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject[]</code></a></td>
            <td><span data-ttu-id="5074d-257">Argumentos de chamada.</span><span class="sxs-lookup"><span data-stu-id="5074d-257">Call arguments.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-258">executionContextid</span><span class="sxs-lookup"><span data-stu-id="5074d-258">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="5074d-259">Identificador do contexto em que foi feita a chamada do console</span><span class="sxs-lookup"><span data-stu-id="5074d-259">Identifier of the context where console call was made</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-260">carimbo</span><span class="sxs-lookup"><span data-stu-id="5074d-260">timestamp</span></span> <br/> <i><span data-ttu-id="5074d-261">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-261">optional</span></span></i></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="5074d-262">Carimbo de data/hora da chamada.</span><span class="sxs-lookup"><span data-stu-id="5074d-262">Call timestamp.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-263">Pilha</span><span class="sxs-lookup"><span data-stu-id="5074d-263">stackTrace</span></span> <br/> <i><span data-ttu-id="5074d-264">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-264">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="5074d-265">Rastreamento de pilha capturado se disponível</span><span class="sxs-lookup"><span data-stu-id="5074d-265">Stack trace captured if available</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="5074d-266">Tipos</span><span class="sxs-lookup"><span data-stu-id="5074d-266">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="5074d-267">Scriptid</span><span class="sxs-lookup"><span data-stu-id="5074d-267">ScriptId</span></span> `string`

<span data-ttu-id="5074d-268">Identificador de script exclusivo.</span><span class="sxs-lookup"><span data-stu-id="5074d-268">Unique script identifier.</span></span>

</p>

---

### <a name="remoteobjectid"></a> <span data-ttu-id="5074d-269">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="5074d-269">RemoteObjectId</span></span> `string`

<span data-ttu-id="5074d-270">Identificador de objeto exclusivo.</span><span class="sxs-lookup"><span data-stu-id="5074d-270">Unique object identifier.</span></span>

</p>

---

### <a name="unserializablevalue"></a> <span data-ttu-id="5074d-271">Unserializablevalue</span><span class="sxs-lookup"><span data-stu-id="5074d-271">UnserializableValue</span></span> `string`

<span data-ttu-id="5074d-272">Valor primitivo que não pode ser JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="5074d-272">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="5074d-273">Valores permitidos</span><span class="sxs-lookup"><span data-stu-id="5074d-273">Allowed Values</span></span>
<span data-ttu-id="5074d-274">Infinito, NaN,-Infinity,-0</span><span class="sxs-lookup"><span data-stu-id="5074d-274">Infinity, NaN, -Infinity, -0</span></span>
</p>

---

### <a name="remoteobject"></a> <span data-ttu-id="5074d-275">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="5074d-275">RemoteObject</span></span> `object`

<span data-ttu-id="5074d-276">Objeto espelho que faz referência ao objeto JavaScript original.</span><span class="sxs-lookup"><span data-stu-id="5074d-276">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-277">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5074d-277">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-278">tipo</span><span class="sxs-lookup"><span data-stu-id="5074d-278">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="5074d-279">Valores permitidos: Object, Function, undefined, String, Number, booliano, símbolo</span><span class="sxs-lookup"><span data-stu-id="5074d-279">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="5074d-280">Tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="5074d-280">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-281">subtipo</span><span class="sxs-lookup"><span data-stu-id="5074d-281">subtype</span></span> <br/> <i><span data-ttu-id="5074d-282">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-282">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="5074d-283">Valores permitidos: NULL, Error, Promise, Node</span><span class="sxs-lookup"><span data-stu-id="5074d-283">Allowed values: null, error, promise, node</span></span></i></td>
            <td><span data-ttu-id="5074d-284">Dica de subtipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="5074d-284">Object subtype hint.</span></span> <span data-ttu-id="5074d-285">Especificado <code>object</code> apenas para valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="5074d-285">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-286">Classe</span><span class="sxs-lookup"><span data-stu-id="5074d-286">className</span></span> <br/> <i><span data-ttu-id="5074d-287">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-287">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5074d-288">Nome do Construtor (classe objeto).</span><span class="sxs-lookup"><span data-stu-id="5074d-288">Object class (constructor) name.</span></span> <span data-ttu-id="5074d-289">Especificado <code>object</code> apenas para valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="5074d-289">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-290">value</span><span class="sxs-lookup"><span data-stu-id="5074d-290">value</span></span> <br/> <i><span data-ttu-id="5074d-291">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-291">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="5074d-292">Valor do objeto remoto em caso de valores primitivos ou valores JSON (se for solicitado).</span><span class="sxs-lookup"><span data-stu-id="5074d-292">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-293">unserializablevalue</span><span class="sxs-lookup"><span data-stu-id="5074d-293">unserializableValue</span></span> <br/> <i><span data-ttu-id="5074d-294">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-294">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="5074d-295">Um valor primitivo que não pode ser JSON-stringified não tem</span><span class="sxs-lookup"><span data-stu-id="5074d-295">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="5074d-296">, mas obtém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="5074d-296">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-297">description</span><span class="sxs-lookup"><span data-stu-id="5074d-297">description</span></span> <br/> <i><span data-ttu-id="5074d-298">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-298">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5074d-299">Representação de cadeia de caracteres do objeto.</span><span class="sxs-lookup"><span data-stu-id="5074d-299">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-300">objectId</span><span class="sxs-lookup"><span data-stu-id="5074d-300">objectId</span></span> <br/> <i><span data-ttu-id="5074d-301">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-301">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="5074d-302">Identificador de objeto exclusivo (para valores não primitivos).</span><span class="sxs-lookup"><span data-stu-id="5074d-302">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-303">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="5074d-303">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="5074d-304">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-304">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="5074d-305">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="5074d-305">Experimental.</span></span> </b></span><span data-ttu-id="5074d-306">Microsoft: a ID de Propriedade do depurador associado a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="5074d-306">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="5074d-307">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="5074d-307">PropertyDescriptor</span></span> `object`

<span data-ttu-id="5074d-308">Descritor de propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="5074d-308">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-309">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5074d-309">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-310">name</span><span class="sxs-lookup"><span data-stu-id="5074d-310">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5074d-311">Nome da propriedade ou descrição do símbolo.</span><span class="sxs-lookup"><span data-stu-id="5074d-311">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-312">value</span><span class="sxs-lookup"><span data-stu-id="5074d-312">value</span></span> <br/> <i><span data-ttu-id="5074d-313">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-313">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="5074d-314">O valor associado à propriedade.</span><span class="sxs-lookup"><span data-stu-id="5074d-314">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-315">gravável</span><span class="sxs-lookup"><span data-stu-id="5074d-315">writable</span></span> <br/> <i><span data-ttu-id="5074d-316">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-316">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="5074d-317">Verdadeiro se o valor associado à propriedade pode ser alterado (somente descritores de dados).</span><span class="sxs-lookup"><span data-stu-id="5074d-317">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-318">obter</span><span class="sxs-lookup"><span data-stu-id="5074d-318">get</span></span> <br/> <i><span data-ttu-id="5074d-319">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-319">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="5074d-320">Uma função que serve como um getter para a propriedade, ou <code>undefined</code> se não houver nenhum getter (somente descritores de acessador).</span><span class="sxs-lookup"><span data-stu-id="5074d-320">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-321">set</span><span class="sxs-lookup"><span data-stu-id="5074d-321">set</span></span> <br/> <i><span data-ttu-id="5074d-322">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-322">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="5074d-323">Uma função que serve como um setter para a propriedade ou <code>undefined</code> se não houver nenhum setter (somente descritores de acesso).</span><span class="sxs-lookup"><span data-stu-id="5074d-323">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-324">configurável</span><span class="sxs-lookup"><span data-stu-id="5074d-324">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="5074d-325">True se o tipo desse descritor de propriedades pode ser alterado e se a propriedade pode ser excluída do objeto correspondente.</span><span class="sxs-lookup"><span data-stu-id="5074d-325">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-326">enumer</span><span class="sxs-lookup"><span data-stu-id="5074d-326">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="5074d-327">Verdadeiro se essa propriedade aparecer durante a enumeração das propriedades no objeto correspondente.</span><span class="sxs-lookup"><span data-stu-id="5074d-327">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-328">wasThrown</span><span class="sxs-lookup"><span data-stu-id="5074d-328">wasThrown</span></span> <br/> <i><span data-ttu-id="5074d-329">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-329">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="5074d-330">Verdadeiro se o resultado foi lançado durante a avaliação.</span><span class="sxs-lookup"><span data-stu-id="5074d-330">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-331">isOwn</span><span class="sxs-lookup"><span data-stu-id="5074d-331">isOwn</span></span> <br/> <i><span data-ttu-id="5074d-332">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-332">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="5074d-333">Verdadeiro se a propriedade for proprietária para o objeto.</span><span class="sxs-lookup"><span data-stu-id="5074d-333">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-334">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="5074d-334">msReturnValue</span></span> <br/> <i><span data-ttu-id="5074d-335">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-335">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="5074d-336">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="5074d-336">Experimental.</span></span> </b></span><span data-ttu-id="5074d-337">Microsoft: true se a propriedade for um valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="5074d-337">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-338">symbol</span><span class="sxs-lookup"><span data-stu-id="5074d-338">symbol</span></span> <br/> <i><span data-ttu-id="5074d-339">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-339">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="5074d-340">Objeto de símbolo de propriedade, se a propriedade for do `symbol` tipo.</span><span class="sxs-lookup"><span data-stu-id="5074d-340">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callargument"></a> <span data-ttu-id="5074d-341">CallArgument</span><span class="sxs-lookup"><span data-stu-id="5074d-341">CallArgument</span></span> `object`

<span data-ttu-id="5074d-342">Representa o argumento de chamada de função.</span><span class="sxs-lookup"><span data-stu-id="5074d-342">Represents function call argument.</span></span> <span data-ttu-id="5074d-343">A ID de objeto remoto <code>objectId</code> , primitiva <code>value</code> , valor primitivo não serializável ou nenhum dos (para Undefined) eles devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="5074d-343">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-344">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5074d-344">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-345">value</span><span class="sxs-lookup"><span data-stu-id="5074d-345">value</span></span> <br/> <i><span data-ttu-id="5074d-346">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-346">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="5074d-347">Valor primitivo ou objeto JavaScript serializável.</span><span class="sxs-lookup"><span data-stu-id="5074d-347">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-348">unserializablevalue</span><span class="sxs-lookup"><span data-stu-id="5074d-348">unserializableValue</span></span> <br/> <i><span data-ttu-id="5074d-349">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-349">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="5074d-350">Valor primitivo que não pode ser JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="5074d-350">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-351">objectId</span><span class="sxs-lookup"><span data-stu-id="5074d-351">objectId</span></span> <br/> <i><span data-ttu-id="5074d-352">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-352">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="5074d-353">Identificador de objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="5074d-353">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="executioncontextid"></a> <span data-ttu-id="5074d-354">ExecutionContextid</span><span class="sxs-lookup"><span data-stu-id="5074d-354">ExecutionContextId</span></span> `integer`

<span data-ttu-id="5074d-355">ID de um contexto de execução.</span><span class="sxs-lookup"><span data-stu-id="5074d-355">Id of an execution context.</span></span>

</p>

---

### <a name="executioncontextdescription"></a> <span data-ttu-id="5074d-356">ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="5074d-356">ExecutionContextDescription</span></span> `object`

<span data-ttu-id="5074d-357">Descrição de um mundo isolado.</span><span class="sxs-lookup"><span data-stu-id="5074d-357">Description of an isolated world.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-358">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5074d-358">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-359">id</span><span class="sxs-lookup"><span data-stu-id="5074d-359">id</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="5074d-360">ID exclusiva do contexto de execução.</span><span class="sxs-lookup"><span data-stu-id="5074d-360">Unique id of the execution context.</span></span> <span data-ttu-id="5074d-361">Ele pode ser usado para especificar em qual execução a avaliação de script de contexto deve ser realizada.</span><span class="sxs-lookup"><span data-stu-id="5074d-361">It can be used to specify in which execution context script evaluation should be performed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-362">Origin</span><span class="sxs-lookup"><span data-stu-id="5074d-362">origin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5074d-363">Origem do contexto de execução.</span><span class="sxs-lookup"><span data-stu-id="5074d-363">Execution context origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-364">name</span><span class="sxs-lookup"><span data-stu-id="5074d-364">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5074d-365">Nome legível pelo homem descrevendo o contexto determinado.</span><span class="sxs-lookup"><span data-stu-id="5074d-365">Human readable name describing given context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="exceptiondetails"></a> <span data-ttu-id="5074d-366">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="5074d-366">ExceptionDetails</span></span> `object`

<span data-ttu-id="5074d-367">Informações detalhadas sobre exceção (ou erro) que foi lançada durante a compilação ou execução de scripts.</span><span class="sxs-lookup"><span data-stu-id="5074d-367">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-368">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5074d-368">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-369">exceptionid</span><span class="sxs-lookup"><span data-stu-id="5074d-369">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5074d-370">ID da exceção.</span><span class="sxs-lookup"><span data-stu-id="5074d-370">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-371">texto</span><span class="sxs-lookup"><span data-stu-id="5074d-371">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5074d-372">Texto de exceção, que deve ser usado em conjunto com o objeto de exceção quando disponível.</span><span class="sxs-lookup"><span data-stu-id="5074d-372">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-373">lineNumber</span><span class="sxs-lookup"><span data-stu-id="5074d-373">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5074d-374">Número da linha do local da exceção (com base em 0).</span><span class="sxs-lookup"><span data-stu-id="5074d-374">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-375">columnNumber</span><span class="sxs-lookup"><span data-stu-id="5074d-375">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5074d-376">Número da coluna do local da exceção (com base em 0).</span><span class="sxs-lookup"><span data-stu-id="5074d-376">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-377">scriptid</span><span class="sxs-lookup"><span data-stu-id="5074d-377">scriptId</span></span> <br/> <i><span data-ttu-id="5074d-378">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-378">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="5074d-379">ID do script do local da exceção.</span><span class="sxs-lookup"><span data-stu-id="5074d-379">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-380">url</span><span class="sxs-lookup"><span data-stu-id="5074d-380">url</span></span> <br/> <i><span data-ttu-id="5074d-381">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-381">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5074d-382">URL do local da exceção, a ser usado quando o script não foi reportado.</span><span class="sxs-lookup"><span data-stu-id="5074d-382">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-383">Pilha</span><span class="sxs-lookup"><span data-stu-id="5074d-383">stackTrace</span></span> <br/> <i><span data-ttu-id="5074d-384">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-384">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="5074d-385">Rastreamento de pilha JavaScript, se disponível.</span><span class="sxs-lookup"><span data-stu-id="5074d-385">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-386">extremamente</span><span class="sxs-lookup"><span data-stu-id="5074d-386">exception</span></span> <br/> <i><span data-ttu-id="5074d-387">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-387">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="5074d-388">Objeto de exceção, se disponível.</span><span class="sxs-lookup"><span data-stu-id="5074d-388">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-389">executionContextid</span><span class="sxs-lookup"><span data-stu-id="5074d-389">executionContextId</span></span> <br/> <i><span data-ttu-id="5074d-390">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-390">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="5074d-391">Identificador do contexto em que ocorreu a exceção.</span><span class="sxs-lookup"><span data-stu-id="5074d-391">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="timestamp"></a> <span data-ttu-id="5074d-392">Carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="5074d-392">Timestamp</span></span> `integer`

<span data-ttu-id="5074d-393">Número de milissegundos desde a época.</span><span class="sxs-lookup"><span data-stu-id="5074d-393">Number of milliseconds since epoch.</span></span>

</p>

---

### <a name="callframe"></a> <span data-ttu-id="5074d-394">CallFrame</span><span class="sxs-lookup"><span data-stu-id="5074d-394">CallFrame</span></span> `object`

<span data-ttu-id="5074d-395">Entrada de pilha para erros e asserções de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="5074d-395">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-396">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5074d-396">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-397">função FunctionName</span><span class="sxs-lookup"><span data-stu-id="5074d-397">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5074d-398">Nome da função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5074d-398">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-399">scriptid</span><span class="sxs-lookup"><span data-stu-id="5074d-399">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="5074d-400">Identificação do script JavaScript. O scriptid estará vazio se o depurador não estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="5074d-400">JavaScript script id. ScriptId will be empty if debugger is not enabled.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-401">url</span><span class="sxs-lookup"><span data-stu-id="5074d-401">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5074d-402">Nome ou URL do script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5074d-402">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-403">lineNumber</span><span class="sxs-lookup"><span data-stu-id="5074d-403">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5074d-404">Número da linha de script JavaScript (com base em 0).</span><span class="sxs-lookup"><span data-stu-id="5074d-404">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-405">columnNumber</span><span class="sxs-lookup"><span data-stu-id="5074d-405">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="5074d-406">Número da coluna de script JavaScript (baseado em 0).</span><span class="sxs-lookup"><span data-stu-id="5074d-406">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="stacktrace"></a> <span data-ttu-id="5074d-407">Pilha</span><span class="sxs-lookup"><span data-stu-id="5074d-407">StackTrace</span></span> `object`

<span data-ttu-id="5074d-408">Quadros de chamadas para asserções ou mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="5074d-408">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="5074d-409">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5074d-409">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="5074d-410">description</span><span class="sxs-lookup"><span data-stu-id="5074d-410">description</span></span> <br/> <i><span data-ttu-id="5074d-411">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-411">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="5074d-412">Rótulo de cadeia de caracteres deste rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="5074d-412">String label of this stack trace.</span></span> <span data-ttu-id="5074d-413">Para rastreamentos assíncronos, pode ser um nome da função que iniciou a chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="5074d-413">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-414">callFrames</span><span class="sxs-lookup"><span data-stu-id="5074d-414">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="5074d-415">Nome da função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5074d-415">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="5074d-416">mãe</span><span class="sxs-lookup"><span data-stu-id="5074d-416">parent</span></span> <br/> <i><span data-ttu-id="5074d-417">opcional</span><span class="sxs-lookup"><span data-stu-id="5074d-417">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="5074d-418">Rastreamento de pilha JavaScript assíncrono que precede esta pilha, se disponível.</span><span class="sxs-lookup"><span data-stu-id="5074d-418">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
