---
description: Referência para o domínio de tempo de execução. O domínio do tempo de execução expõe o tempo de execução JavaScript por meio de objetos de avaliação e espelho remotos. Os resultados da avaliação são retornados como um objeto espelho que expõe o tipo de objeto, representação de cadeia de caracteres e identificador exclusivo que podem ser usados para referência de objeto posterior. Os objetos originais são mantidos na memória, a menos que eles sejam explicitamente liberados.
title: Domínio de tempo de execução – versão 0,1 do protocolo DevTools
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 33bc98b272aaa8831e908207b97ea7d3d0842976
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561354"
---
# <span data-ttu-id="0a341-106">Classpath</span><span class="sxs-lookup"><span data-stu-id="0a341-106">Runtime</span></span>
<span data-ttu-id="0a341-107">O domínio do tempo de execução expõe o tempo de execução JavaScript por meio de objetos de avaliação e espelho remotos.</span><span class="sxs-lookup"><span data-stu-id="0a341-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="0a341-108">Os resultados da avaliação são retornados como um objeto espelho que expõe o tipo de objeto, representação de cadeia de caracteres e identificador exclusivo que podem ser usados para referência de objeto posterior.</span><span class="sxs-lookup"><span data-stu-id="0a341-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="0a341-109">Os objetos originais são mantidos na memória, a menos que eles sejam explicitamente liberados.</span><span class="sxs-lookup"><span data-stu-id="0a341-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="0a341-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="0a341-110">Methods</span></span>**](#methods) | <span data-ttu-id="0a341-111">[habilitar](#enable), [desabilitar](#disable), [avaliar](#evaluate), [callFunctionOn](#callfunctionon), [GetProperties](#getproperties)</span><span class="sxs-lookup"><span data-stu-id="0a341-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span></span> |
| [**<span data-ttu-id="0a341-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="0a341-112">Events</span></span>**](#events) | <span data-ttu-id="0a341-113">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span><span class="sxs-lookup"><span data-stu-id="0a341-113">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span></span> |
| [**<span data-ttu-id="0a341-114">Tipos</span><span class="sxs-lookup"><span data-stu-id="0a341-114">Types</span></span>**](#types) | <span data-ttu-id="0a341-115">[Scriptid](#scriptid), [RemoteObjectId](#remoteobjectid), [unserializablevalue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [executioncontextid](#executioncontextid), [ExceptionDetails](#exceptiondetails), [timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="0a341-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="0a341-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="0a341-116">Methods</span></span>

### <span data-ttu-id="0a341-117">Habilitar</span><span class="sxs-lookup"><span data-stu-id="0a341-117">enable</span></span>
<span data-ttu-id="0a341-118">Habilita o relatório do <code>executionContextsCleared</code> evento.</span><span class="sxs-lookup"><span data-stu-id="0a341-118">Enables reporting of the <code>executionContextsCleared</code> event.</span></span>


---

### <span data-ttu-id="0a341-119">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="0a341-119">disable</span></span>
<span data-ttu-id="0a341-120">Desabilita o relatório do <code>executionContextsCleared</code> evento.</span><span class="sxs-lookup"><span data-stu-id="0a341-120">Disables reporting of the <code>executionContextsCleared</code> event.</span></span>


---

### <span data-ttu-id="0a341-121">retornará</span><span class="sxs-lookup"><span data-stu-id="0a341-121">evaluate</span></span>
<span data-ttu-id="0a341-122">Avalia a expressão no objeto global.</span><span class="sxs-lookup"><span data-stu-id="0a341-122">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0a341-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a341-123">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0a341-124">Express</span><span class="sxs-lookup"><span data-stu-id="0a341-124">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0a341-125">Expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="0a341-125">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-126">silent</span><span class="sxs-lookup"><span data-stu-id="0a341-126">silent</span></span> <br/> <i><span data-ttu-id="0a341-127">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-127">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0a341-128">As exceções do modo silencioso lançadas durante a avaliação não são relatadas e não pausam a execução.</span><span class="sxs-lookup"><span data-stu-id="0a341-128">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="0a341-129">Substitui o <code>setPauseOnException</code> estado.</span><span class="sxs-lookup"><span data-stu-id="0a341-129">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-130">ContextId</span><span class="sxs-lookup"><span data-stu-id="0a341-130">contextId</span></span> <br/> <i><span data-ttu-id="0a341-131">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-131">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="0a341-132">Especifica em qual contexto de execução executar avaliação.</span><span class="sxs-lookup"><span data-stu-id="0a341-132">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="0a341-133">Se o parâmetro for omitido, a avaliação será executada no contexto da página inspecionada.</span><span class="sxs-lookup"><span data-stu-id="0a341-133">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-134">returnByValue</span><span class="sxs-lookup"><span data-stu-id="0a341-134">returnByValue</span></span> <br/> <i><span data-ttu-id="0a341-135">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-135">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0a341-136">Se é esperado que o resultado seja um objeto JSON que deve ser enviado por valor.</span><span class="sxs-lookup"><span data-stu-id="0a341-136">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-137">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="0a341-137">awaitPromise</span></span> <br/> <i><span data-ttu-id="0a341-138">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-138">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0a341-139">Se a execução deve <code>await</code> ser um valor resultante e retorna uma vez que a promessa esperada seja resolvida.</span><span class="sxs-lookup"><span data-stu-id="0a341-139">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0a341-140">Devolver</span><span class="sxs-lookup"><span data-stu-id="0a341-140">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0a341-141">levar</span><span class="sxs-lookup"><span data-stu-id="0a341-141">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="0a341-142">Resultado da avaliação.</span><span class="sxs-lookup"><span data-stu-id="0a341-142">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="0a341-143">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="0a341-143">callFunctionOn</span></span>
<span data-ttu-id="0a341-144">Função calls com declaração fornecida no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="0a341-144">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="0a341-145">O grupo de objetos do resultado é herdado do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="0a341-145">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0a341-146">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a341-146">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0a341-147">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="0a341-147">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0a341-148">Declaração da função a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="0a341-148">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-149">objectId</span><span class="sxs-lookup"><span data-stu-id="0a341-149">objectId</span></span> <br/> <i><span data-ttu-id="0a341-150">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-150">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="0a341-151">Identificador do objeto no qual a função deve ser chamada.</span><span class="sxs-lookup"><span data-stu-id="0a341-151">Identifier of the object to call function on.</span></span> <span data-ttu-id="0a341-152">O objectId ou o executionContextid deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="0a341-152">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="0a341-153">objectId deve ser da função Runtime. Evaluate ().</span><span class="sxs-lookup"><span data-stu-id="0a341-153">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-154">arguments</span><span class="sxs-lookup"><span data-stu-id="0a341-154">arguments</span></span> <br/> <i><span data-ttu-id="0a341-155">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-155">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="0a341-156">Argumentos de chamada.</span><span class="sxs-lookup"><span data-stu-id="0a341-156">Call arguments.</span></span> <span data-ttu-id="0a341-157">Todos os argumentos de chamada devem pertencer ao mesmo mundo JavaScript que o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="0a341-157">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-158">silent</span><span class="sxs-lookup"><span data-stu-id="0a341-158">silent</span></span> <br/> <i><span data-ttu-id="0a341-159">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-159">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0a341-160">As exceções do modo silencioso lançadas durante a avaliação não são relatadas e não pausam a execução.</span><span class="sxs-lookup"><span data-stu-id="0a341-160">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="0a341-161">Substitui o <code>setPauseOnException</code> estado.</span><span class="sxs-lookup"><span data-stu-id="0a341-161">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-162">returnByValue</span><span class="sxs-lookup"><span data-stu-id="0a341-162">returnByValue</span></span> <br/> <i><span data-ttu-id="0a341-163">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-163">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0a341-164">Se é esperado que o resultado seja um objeto JSON que deve ser enviado por valor.</span><span class="sxs-lookup"><span data-stu-id="0a341-164">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-165">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="0a341-165">awaitPromise</span></span> <br/> <i><span data-ttu-id="0a341-166">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0a341-167">Se a execução deve <code>await</code> ser um valor resultante e retorna uma vez que a promessa esperada seja resolvida.</span><span class="sxs-lookup"><span data-stu-id="0a341-167">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0a341-168">Devolver</span><span class="sxs-lookup"><span data-stu-id="0a341-168">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0a341-169">levar</span><span class="sxs-lookup"><span data-stu-id="0a341-169">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="0a341-170">Resultado da chamada.</span><span class="sxs-lookup"><span data-stu-id="0a341-170">Call result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="0a341-171">GetProperties</span><span class="sxs-lookup"><span data-stu-id="0a341-171">getProperties</span></span>
<span data-ttu-id="0a341-172">Retorna as propriedades de um determinado objeto.</span><span class="sxs-lookup"><span data-stu-id="0a341-172">Returns properties of a given object.</span></span> <span data-ttu-id="0a341-173">O grupo de objetos do resultado é herdado do objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="0a341-173">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0a341-174">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a341-174">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0a341-175">objectId</span><span class="sxs-lookup"><span data-stu-id="0a341-175">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="0a341-176">Identificador do objeto para o qual as propriedades são retornadas.</span><span class="sxs-lookup"><span data-stu-id="0a341-176">Identifier of the object to return properties for.</span></span>  <span data-ttu-id="0a341-177">objectId deve ser da função Debugger. evaluateOnCallFrame ().</span><span class="sxs-lookup"><span data-stu-id="0a341-177">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-178">ownProperties</span><span class="sxs-lookup"><span data-stu-id="0a341-178">ownProperties</span></span> <br/> <i><span data-ttu-id="0a341-179">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-179">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0a341-180">Se verdadeiro, retorna propriedades pertencentes somente ao elemento em si, não à sua cadeia de protótipos.</span><span class="sxs-lookup"><span data-stu-id="0a341-180">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-181">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="0a341-181">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="0a341-182">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-182">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="0a341-183">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="0a341-183">Experimental.</span></span> </b></span><span data-ttu-id="0a341-184">Se verdadeiro, retorna propriedades de assessor (somente com getter/setter); as propriedades internas também não são retornadas.</span><span class="sxs-lookup"><span data-stu-id="0a341-184">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0a341-185">Devolver</span><span class="sxs-lookup"><span data-stu-id="0a341-185">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0a341-186">levar</span><span class="sxs-lookup"><span data-stu-id="0a341-186">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="0a341-187">Propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="0a341-187">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="0a341-188">Eventos</span><span class="sxs-lookup"><span data-stu-id="0a341-188">Events</span></span>

### <span data-ttu-id="0a341-189">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="0a341-189">executionContextsCleared</span></span>
<span data-ttu-id="0a341-190">Emitido quando todos os executionContext foram limpos no navegador</span><span class="sxs-lookup"><span data-stu-id="0a341-190">Issued when all executionContexts were cleared in browser</span></span>


---

### <span data-ttu-id="0a341-191">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="0a341-191">exceptionThrown</span></span>
<span data-ttu-id="0a341-192">Emitido quando a exceção foi gerada e não tratada.</span><span class="sxs-lookup"><span data-stu-id="0a341-192">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0a341-193">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a341-193">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0a341-194">carimbo</span><span class="sxs-lookup"><span data-stu-id="0a341-194">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="0a341-195">Carimbo de data/hora da exceção.</span><span class="sxs-lookup"><span data-stu-id="0a341-195">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-196">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="0a341-196">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="0a341-197">Tipos</span><span class="sxs-lookup"><span data-stu-id="0a341-197">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="0a341-198">Scriptid</span><span class="sxs-lookup"><span data-stu-id="0a341-198">ScriptId</span></span> `string`

<span data-ttu-id="0a341-199">Identificador de script exclusivo.</span><span class="sxs-lookup"><span data-stu-id="0a341-199">Unique script identifier.</span></span>


---

### <a name="remoteobjectid"></a> <span data-ttu-id="0a341-200">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="0a341-200">RemoteObjectId</span></span> `string`

<span data-ttu-id="0a341-201">Identificador de objeto exclusivo.</span><span class="sxs-lookup"><span data-stu-id="0a341-201">Unique object identifier.</span></span>


---

### <a name="unserializablevalue"></a> <span data-ttu-id="0a341-202">Unserializablevalue</span><span class="sxs-lookup"><span data-stu-id="0a341-202">UnserializableValue</span></span> `string`

<span data-ttu-id="0a341-203">Valor primitivo que não pode ser JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="0a341-203">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="0a341-204">Valores permitidos</span><span class="sxs-lookup"><span data-stu-id="0a341-204">Allowed Values</span></span>
<span data-ttu-id="0a341-205">Infinito, NaN,-Infinity,-0</span><span class="sxs-lookup"><span data-stu-id="0a341-205">Infinity, NaN, -Infinity, -0</span></span>

---

### <a name="remoteobject"></a> <span data-ttu-id="0a341-206">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0a341-206">RemoteObject</span></span> `object`

<span data-ttu-id="0a341-207">Objeto espelho que faz referência ao objeto JavaScript original.</span><span class="sxs-lookup"><span data-stu-id="0a341-207">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0a341-208">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0a341-208">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0a341-209">tipo</span><span class="sxs-lookup"><span data-stu-id="0a341-209">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="0a341-210">Valores permitidos: Object, Function, undefined, String, Number, booliano, símbolo</span><span class="sxs-lookup"><span data-stu-id="0a341-210">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="0a341-211">Tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="0a341-211">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-212">subtipo</span><span class="sxs-lookup"><span data-stu-id="0a341-212">subtype</span></span> <br/> <i><span data-ttu-id="0a341-213">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-213">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="0a341-214">Valores permitidos: NULL, Error, Promise</span><span class="sxs-lookup"><span data-stu-id="0a341-214">Allowed values: null, error, promise</span></span></i></td>
            <td><span data-ttu-id="0a341-215">Dica de subtipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="0a341-215">Object subtype hint.</span></span> <span data-ttu-id="0a341-216">Especificado <code>object</code> apenas para valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="0a341-216">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-217">Classe</span><span class="sxs-lookup"><span data-stu-id="0a341-217">className</span></span> <br/> <i><span data-ttu-id="0a341-218">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-218">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0a341-219">Nome do Construtor (classe objeto).</span><span class="sxs-lookup"><span data-stu-id="0a341-219">Object class (constructor) name.</span></span> <span data-ttu-id="0a341-220">Especificado <code>object</code> apenas para valores de tipo.</span><span class="sxs-lookup"><span data-stu-id="0a341-220">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-221">value</span><span class="sxs-lookup"><span data-stu-id="0a341-221">value</span></span> <br/> <i><span data-ttu-id="0a341-222">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-222">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="0a341-223">Valor do objeto remoto em caso de valores primitivos ou valores JSON (se for solicitado).</span><span class="sxs-lookup"><span data-stu-id="0a341-223">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-224">unserializablevalue</span><span class="sxs-lookup"><span data-stu-id="0a341-224">unserializableValue</span></span> <br/> <i><span data-ttu-id="0a341-225">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-225">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="0a341-226">Um valor primitivo que não pode ser JSON-stringified não tem</span><span class="sxs-lookup"><span data-stu-id="0a341-226">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="0a341-227">, mas obtém essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="0a341-227">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-228">description</span><span class="sxs-lookup"><span data-stu-id="0a341-228">description</span></span> <br/> <i><span data-ttu-id="0a341-229">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-229">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0a341-230">Representação de cadeia de caracteres do objeto.</span><span class="sxs-lookup"><span data-stu-id="0a341-230">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-231">objectId</span><span class="sxs-lookup"><span data-stu-id="0a341-231">objectId</span></span> <br/> <i><span data-ttu-id="0a341-232">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-232">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="0a341-233">Identificador de objeto exclusivo (para valores não primitivos).</span><span class="sxs-lookup"><span data-stu-id="0a341-233">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-234">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="0a341-234">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="0a341-235">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-235">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="0a341-236">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="0a341-236">Experimental.</span></span> </b></span><span data-ttu-id="0a341-237">Microsoft: a ID de Propriedade do depurador associado a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="0a341-237">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="0a341-238">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="0a341-238">PropertyDescriptor</span></span> `object`

<span data-ttu-id="0a341-239">Descritor de propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="0a341-239">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0a341-240">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0a341-240">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0a341-241">name</span><span class="sxs-lookup"><span data-stu-id="0a341-241">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0a341-242">Nome da propriedade ou descrição do símbolo.</span><span class="sxs-lookup"><span data-stu-id="0a341-242">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-243">value</span><span class="sxs-lookup"><span data-stu-id="0a341-243">value</span></span> <br/> <i><span data-ttu-id="0a341-244">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-244">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="0a341-245">O valor associado à propriedade.</span><span class="sxs-lookup"><span data-stu-id="0a341-245">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-246">gravável</span><span class="sxs-lookup"><span data-stu-id="0a341-246">writable</span></span> <br/> <i><span data-ttu-id="0a341-247">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-247">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0a341-248">Verdadeiro se o valor associado à propriedade pode ser alterado (somente descritores de dados).</span><span class="sxs-lookup"><span data-stu-id="0a341-248">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-249">obter</span><span class="sxs-lookup"><span data-stu-id="0a341-249">get</span></span> <br/> <i><span data-ttu-id="0a341-250">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-250">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="0a341-251">Uma função que serve como um getter para a propriedade, ou <code>undefined</code> se não houver nenhum getter (somente descritores de acessador).</span><span class="sxs-lookup"><span data-stu-id="0a341-251">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-252">set</span><span class="sxs-lookup"><span data-stu-id="0a341-252">set</span></span> <br/> <i><span data-ttu-id="0a341-253">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-253">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="0a341-254">Uma função que serve como um setter para a propriedade ou <code>undefined</code> se não houver nenhum setter (somente descritores de acesso).</span><span class="sxs-lookup"><span data-stu-id="0a341-254">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-255">configurável</span><span class="sxs-lookup"><span data-stu-id="0a341-255">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0a341-256">True se o tipo desse descritor de propriedades pode ser alterado e se a propriedade pode ser excluída do objeto correspondente.</span><span class="sxs-lookup"><span data-stu-id="0a341-256">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-257">enumer</span><span class="sxs-lookup"><span data-stu-id="0a341-257">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0a341-258">Verdadeiro se essa propriedade aparecer durante a enumeração das propriedades no objeto correspondente.</span><span class="sxs-lookup"><span data-stu-id="0a341-258">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-259">wasThrown</span><span class="sxs-lookup"><span data-stu-id="0a341-259">wasThrown</span></span> <br/> <i><span data-ttu-id="0a341-260">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-260">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0a341-261">Verdadeiro se o resultado foi lançado durante a avaliação.</span><span class="sxs-lookup"><span data-stu-id="0a341-261">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-262">isOwn</span><span class="sxs-lookup"><span data-stu-id="0a341-262">isOwn</span></span> <br/> <i><span data-ttu-id="0a341-263">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-263">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="0a341-264">Verdadeiro se a propriedade for proprietária para o objeto.</span><span class="sxs-lookup"><span data-stu-id="0a341-264">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-265">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="0a341-265">msReturnValue</span></span> <br/> <i><span data-ttu-id="0a341-266">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-266">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="0a341-267">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="0a341-267">Experimental.</span></span> </b></span><span data-ttu-id="0a341-268">Microsoft: true se a propriedade for um valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="0a341-268">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-269">symbol</span><span class="sxs-lookup"><span data-stu-id="0a341-269">symbol</span></span> <br/> <i><span data-ttu-id="0a341-270">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-270">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="0a341-271">Objeto de símbolo de propriedade, se a propriedade for do `symbol` tipo.</span><span class="sxs-lookup"><span data-stu-id="0a341-271">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>

---

### <a name="callargument"></a> <span data-ttu-id="0a341-272">CallArgument</span><span class="sxs-lookup"><span data-stu-id="0a341-272">CallArgument</span></span> `object`

<span data-ttu-id="0a341-273">Representa o argumento de chamada de função.</span><span class="sxs-lookup"><span data-stu-id="0a341-273">Represents function call argument.</span></span> <span data-ttu-id="0a341-274">A ID de objeto remoto <code>objectId</code> , primitiva <code>value</code> , valor primitivo não serializável ou nenhum dos (para Undefined) eles devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="0a341-274">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0a341-275">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0a341-275">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0a341-276">value</span><span class="sxs-lookup"><span data-stu-id="0a341-276">value</span></span> <br/> <i><span data-ttu-id="0a341-277">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-277">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="0a341-278">Valor primitivo ou objeto JavaScript serializável.</span><span class="sxs-lookup"><span data-stu-id="0a341-278">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-279">unserializablevalue</span><span class="sxs-lookup"><span data-stu-id="0a341-279">unserializableValue</span></span> <br/> <i><span data-ttu-id="0a341-280">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-280">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="0a341-281">Valor primitivo que não pode ser JSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="0a341-281">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-282">objectId</span><span class="sxs-lookup"><span data-stu-id="0a341-282">objectId</span></span> <br/> <i><span data-ttu-id="0a341-283">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-283">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="0a341-284">Identificador de objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="0a341-284">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="executioncontextid"></a> <span data-ttu-id="0a341-285">ExecutionContextid</span><span class="sxs-lookup"><span data-stu-id="0a341-285">ExecutionContextId</span></span> `integer`

<span data-ttu-id="0a341-286">ID de um contexto de execução.</span><span class="sxs-lookup"><span data-stu-id="0a341-286">Id of an execution context.</span></span>


---

### <a name="exceptiondetails"></a> <span data-ttu-id="0a341-287">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="0a341-287">ExceptionDetails</span></span> `object`

<span data-ttu-id="0a341-288">Informações detalhadas sobre exceção (ou erro) que foi lançada durante a compilação ou execução de scripts.</span><span class="sxs-lookup"><span data-stu-id="0a341-288">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0a341-289">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0a341-289">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0a341-290">exceptionid</span><span class="sxs-lookup"><span data-stu-id="0a341-290">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="0a341-291">ID da exceção.</span><span class="sxs-lookup"><span data-stu-id="0a341-291">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-292">texto</span><span class="sxs-lookup"><span data-stu-id="0a341-292">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0a341-293">Texto de exceção, que deve ser usado em conjunto com o objeto de exceção quando disponível.</span><span class="sxs-lookup"><span data-stu-id="0a341-293">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-294">lineNumber</span><span class="sxs-lookup"><span data-stu-id="0a341-294">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="0a341-295">Número da linha do local da exceção (com base em 0).</span><span class="sxs-lookup"><span data-stu-id="0a341-295">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-296">columnNumber</span><span class="sxs-lookup"><span data-stu-id="0a341-296">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="0a341-297">Número da coluna do local da exceção (com base em 0).</span><span class="sxs-lookup"><span data-stu-id="0a341-297">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-298">scriptid</span><span class="sxs-lookup"><span data-stu-id="0a341-298">scriptId</span></span> <br/> <i><span data-ttu-id="0a341-299">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-299">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="0a341-300">ID do script do local da exceção.</span><span class="sxs-lookup"><span data-stu-id="0a341-300">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-301">url</span><span class="sxs-lookup"><span data-stu-id="0a341-301">url</span></span> <br/> <i><span data-ttu-id="0a341-302">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-302">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0a341-303">URL do local da exceção, a ser usado quando o script não foi reportado.</span><span class="sxs-lookup"><span data-stu-id="0a341-303">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-304">Pilha</span><span class="sxs-lookup"><span data-stu-id="0a341-304">stackTrace</span></span> <br/> <i><span data-ttu-id="0a341-305">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-305">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="0a341-306">Rastreamento de pilha JavaScript, se disponível.</span><span class="sxs-lookup"><span data-stu-id="0a341-306">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-307">extremamente</span><span class="sxs-lookup"><span data-stu-id="0a341-307">exception</span></span> <br/> <i><span data-ttu-id="0a341-308">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-308">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="0a341-309">Objeto de exceção, se disponível.</span><span class="sxs-lookup"><span data-stu-id="0a341-309">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-310">executionContextid</span><span class="sxs-lookup"><span data-stu-id="0a341-310">executionContextId</span></span> <br/> <i><span data-ttu-id="0a341-311">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-311">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="0a341-312">Identificador do contexto em que ocorreu a exceção.</span><span class="sxs-lookup"><span data-stu-id="0a341-312">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="timestamp"></a> <span data-ttu-id="0a341-313">Carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="0a341-313">Timestamp</span></span> `integer`

<span data-ttu-id="0a341-314">Número de milissegundos desde a época.</span><span class="sxs-lookup"><span data-stu-id="0a341-314">Number of milliseconds since epoch.</span></span>


---

### <a name="callframe"></a> <span data-ttu-id="0a341-315">CallFrame</span><span class="sxs-lookup"><span data-stu-id="0a341-315">CallFrame</span></span> `object`

<span data-ttu-id="0a341-316">Entrada de pilha para erros e asserções de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="0a341-316">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0a341-317">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0a341-317">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0a341-318">função FunctionName</span><span class="sxs-lookup"><span data-stu-id="0a341-318">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0a341-319">Nome da função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0a341-319">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-320">scriptid</span><span class="sxs-lookup"><span data-stu-id="0a341-320">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="0a341-321">Identificação do script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0a341-321">JavaScript script id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-322">url</span><span class="sxs-lookup"><span data-stu-id="0a341-322">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0a341-323">Nome ou URL do script JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0a341-323">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-324">lineNumber</span><span class="sxs-lookup"><span data-stu-id="0a341-324">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="0a341-325">Número da linha de script JavaScript (com base em 0).</span><span class="sxs-lookup"><span data-stu-id="0a341-325">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-326">columnNumber</span><span class="sxs-lookup"><span data-stu-id="0a341-326">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="0a341-327">Número da coluna de script JavaScript (baseado em 0).</span><span class="sxs-lookup"><span data-stu-id="0a341-327">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="stacktrace"></a> <span data-ttu-id="0a341-328">Pilha</span><span class="sxs-lookup"><span data-stu-id="0a341-328">StackTrace</span></span> `object`

<span data-ttu-id="0a341-329">Quadros de chamadas para asserções ou mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="0a341-329">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="0a341-330">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0a341-330">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="0a341-331">description</span><span class="sxs-lookup"><span data-stu-id="0a341-331">description</span></span> <br/> <i><span data-ttu-id="0a341-332">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-332">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="0a341-333">Rótulo de cadeia de caracteres deste rastreamento de pilha.</span><span class="sxs-lookup"><span data-stu-id="0a341-333">String label of this stack trace.</span></span> <span data-ttu-id="0a341-334">Para rastreamentos assíncronos, pode ser um nome da função que iniciou a chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="0a341-334">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-335">callFrames</span><span class="sxs-lookup"><span data-stu-id="0a341-335">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="0a341-336">Nome da função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0a341-336">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="0a341-337">mãe</span><span class="sxs-lookup"><span data-stu-id="0a341-337">parent</span></span> <br/> <i><span data-ttu-id="0a341-338">opcional</span><span class="sxs-lookup"><span data-stu-id="0a341-338">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="0a341-339">Rastreamento de pilha JavaScript assíncrono que precede esta pilha, se disponível.</span><span class="sxs-lookup"><span data-stu-id="0a341-339">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>

---
