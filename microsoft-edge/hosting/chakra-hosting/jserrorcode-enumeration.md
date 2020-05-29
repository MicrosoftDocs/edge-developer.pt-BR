---
description: Um código de erro retornado de uma API de hospedagem Chakra.
title: Enumeração JsErrorCode | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsErrorCode
helpviewer_keywords:
- JsErrorCode enumeration
ms.assetid: 4902f3f3-47a5-4e74-9c29-f96eeecbcda9
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e3d1a319872ac69b2acaf19997f3c38f9c04597b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562199"
---
# <span data-ttu-id="5ab2a-103">Enumeração JsErrorCode</span><span class="sxs-lookup"><span data-stu-id="5ab2a-103">JsErrorCode Enumeration</span></span>
<span data-ttu-id="5ab2a-104">Um código de erro retornado de uma API de hospedagem Chakra.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-104">An error code returned from a Chakra hosting API.</span></span>  
  
## <span data-ttu-id="5ab2a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ab2a-105">Syntax</span></span>  
  
```cpp  
enum JsErrorCode : unsigned int;  
```  
  
## <span data-ttu-id="5ab2a-106">Parte</span><span class="sxs-lookup"><span data-stu-id="5ab2a-106">Members</span></span>  
  
### <span data-ttu-id="5ab2a-107">Valores</span><span class="sxs-lookup"><span data-stu-id="5ab2a-107">Values</span></span>  
  
|<span data-ttu-id="5ab2a-108">Nome</span><span class="sxs-lookup"><span data-stu-id="5ab2a-108">Name</span></span>|<span data-ttu-id="5ab2a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ab2a-109">Description</span></span>|  
|----------|-----------------|  
|`JsErrorAlreadyDebuggingContext`|<span data-ttu-id="5ab2a-110">O contexto não pode ser colocado em um estado de depuração porque já está em um estado de depuração.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-110">The context cannot be put into a debug state because it is already in a debug state.</span></span>|  
|`JsErrorAlreadyProfilingContext`|<span data-ttu-id="5ab2a-111">O contexto não pode iniciar a criação de perfil porque já está criando o perfil.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-111">The context cannot start profiling because it is already profiling.</span></span>|  
|`JsErrorArgumentNotObject`|<span data-ttu-id="5ab2a-112">Uma API de hospedagem que opera em valores de objeto foi chamada com um valor não objeto.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-112">A hosting API that operates on object values was called with a non-object value.</span></span>|  
|`JsErrorBadSerializedScript`|<span data-ttu-id="5ab2a-113">Um script serializado incorreto foi usado ou o script serializado foi serializado por uma versão diferente do mecanismo Chakra.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-113">A bad serialized script was used, or the serialized script was serialized by a different version of the Chakra engine.</span></span>|  
|`JsErrorCannotDisableExecution`|<span data-ttu-id="5ab2a-114">O tempo de execução não dá suporte à interrupção de script confiável.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-114">Runtime does not support reliable script interruption.</span></span>|  
|`JsErrorCannotSerializeDebugScript`|<span data-ttu-id="5ab2a-115">Scripts não podem ser serializados em contextos de depuração.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-115">Scripts cannot be serialized in debug contexts.</span></span>|  
|`JsErrorCategoryEngine`|<span data-ttu-id="5ab2a-116">Categoria de erros relacionados a erros que ocorrem dentro do próprio mecanismo.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-116">Category of errors that relates to errors occurring within the engine itself.</span></span>|  
|`JsErrorCategoryFatal`|<span data-ttu-id="5ab2a-117">Categoria de erros que são fatais e significam falha do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-117">Category of errors that are fatal and signify failure of the engine.</span></span>|  
|`JsErrorCategoryScript`|<span data-ttu-id="5ab2a-118">Categoria de erros relacionados a erros em um script.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-118">Category of errors that relates to errors in a script.</span></span>|  
|`JsErrorCategoryUsage`|<span data-ttu-id="5ab2a-119">Categoria de erros relacionados ao uso incorreto da própria API.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-119">Category of errors that relates to incorrect usage of the API itself.</span></span>|  
|`JsErrorFatal`|<span data-ttu-id="5ab2a-120">Ocorreu um erro fatal no mecanismo.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-120">A fatal error in the engine has occurred.</span></span>|  
|`JsErrorHeapEnumInProgress`|<span data-ttu-id="5ab2a-121">No momento, uma enumeração de heap está em andamento no contexto do script.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-121">A heap enumeration is currently underway in the script context.</span></span>|  
|`JsErrorIdleNotEnabled`|<span data-ttu-id="5ab2a-122">Notificação ociosa fornecida quando o host não habilitou o processamento de ociosidade.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-122">Idle notification given when the host did not enable idle processing.</span></span>|  
|`JsErrorInDisabledState`|<span data-ttu-id="5ab2a-123">O tempo de execução está em um estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-123">The runtime is in a disabled state.</span></span>|  
|`JsErrorInExceptionState`|<span data-ttu-id="5ab2a-124">O mecanismo está em um estado de exceção e nenhuma API pode ser chamada até que a exceção seja desmarcada.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-124">The engine is in an exception state and no APIs can be called until the exception is cleared.</span></span>|  
|`JsErrorInObjectBeforeCollectCallback`|<span data-ttu-id="5ab2a-125">Não há suporte para a operação em um objeto antes da coleta de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-125">The operation is not supported in an object before collect callback.</span></span><br /><br /> <span data-ttu-id="5ab2a-126">Esse valor de enumeração só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-126">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorInProfileCallback`|<span data-ttu-id="5ab2a-127">Um contexto de script está no meio de um retorno de chamada de perfil.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-127">A script context is in the middle of a profile callback.</span></span>|  
|`JsErrorInThreadServiceCallback`|<span data-ttu-id="5ab2a-128">No momento, um retorno de chamada de serviço de thread está em andamento.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-128">A thread service callback is currently underway.</span></span>|  
|`JsErrorInvalidArgument`|<span data-ttu-id="5ab2a-129">Um argumento para uma API de hospedagem era inválido.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-129">An argument to a hosting API was invalid.</span></span>|  
|`JsErrorNoCurrentContext`|<span data-ttu-id="5ab2a-130">A API de hospedagem requer que um contexto seja atual, mas não há contexto atual.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-130">The hosting API requires that a context be current, but there is no current context.</span></span>|  
|`JsErrorNotImplemented`|<span data-ttu-id="5ab2a-131">Uma API de hospedagem ainda não foi implementada.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-131">A hosting API is not yet implemented.</span></span>|  
|`JsErrorNullArgument`|<span data-ttu-id="5ab2a-132">Um argumento para uma API de hospedagem era nulo em um contexto em que NULL não é permitido.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-132">An argument to a hosting API was null in a context where null is not allowed.</span></span>|  
|`JsErrorObjectNotInspectable`|<span data-ttu-id="5ab2a-133">O objeto não pode ser quebrado para `IInspectable` ponteiro.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-133">Object cannot be unwrapped to `IInspectable` pointer.</span></span><br /><br /> <span data-ttu-id="5ab2a-134">Esse valor de enumeração só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-134">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorOutOfMemory`|<span data-ttu-id="5ab2a-135">O mecanismo Chakra não tem memória suficiente.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-135">The Chakra engine has run out of memory.</span></span>|  
|`JsErrorPropertyNotSymbol`|<span data-ttu-id="5ab2a-136">Uma API de hospedagem que opera em IDs de propriedade de símbolo, mas foi chamada com uma ID de propriedade sem símbolo. O código de erro é retornado `JsGetSymbolFromPropertyId` se a função for chamada com a ID de propriedade sem símbolo.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-136">A hosting API that operates on symbol property ids but was called with a non-symbol property id. The error code is returned by `JsGetSymbolFromPropertyId` if the function is called with non-symbol property id.</span></span><br /><br /> <span data-ttu-id="5ab2a-137">Esse valor de enumeração só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-137">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorPropertyNotString`|<span data-ttu-id="5ab2a-138">Uma API de hospedagem que opera em IDs de propriedades de cadeias de caracteres, mas foi chamada com uma ID de propriedade não cadeia de caracteres. O código de erro é retornado por existente `JsGetPropertyNamefromId` se a função for chamada com a ID de propriedade não cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-138">A hosting API that operates on string property ids but was called with a non-string property id. The error code is returned by existing `JsGetPropertyNamefromId` if the function is called with non-string property id.</span></span><br /><br /> <span data-ttu-id="5ab2a-139">Esse valor de enumeração só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-139">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorRuntimeInUse`|<span data-ttu-id="5ab2a-140">Não é possível descartar um tempo de execução que ainda está em uso.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-140">A runtime that is still in use cannot be disposed.</span></span>|  
|`JsErrorScriptCompile`|<span data-ttu-id="5ab2a-141">Falha na compilação do JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-141">JavaScript failed to compile.</span></span>|  
|`JsErrorScriptEvalDisabled`|<span data-ttu-id="5ab2a-142">Um script foi encerrado porque tentou usar `eval` ou `function` eval foi desabilitada.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-142">A script was terminated because it tried to use `eval` or `function` and eval was disabled.</span></span>|  
|`JsErrorScriptException`|<span data-ttu-id="5ab2a-143">Ocorreu uma exceção JavaScript ao executar um script.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-143">A JavaScript exception occurred while running a script.</span></span>|  
|`JsErrorScriptTerminated`|<span data-ttu-id="5ab2a-144">Um script foi encerrado devido a uma solicitação para suspender um tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-144">A script was terminated due to a request to suspend a runtime.</span></span>|  
|`JsErrorWrongRuntime`|<span data-ttu-id="5ab2a-145">Uma API de hospedagem era chamada com objeto criado em um tempo de execução JavaScript diferente.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-145">A hosting API was called with object created on different JavaScript runtime.</span></span>|  
|`JsErrorWrongThread`|<span data-ttu-id="5ab2a-146">Uma API de hospedagem foi chamada no thread errado.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-146">A hosting API was called on the wrong thread.</span></span>|  
|`JsNoError`|<span data-ttu-id="5ab2a-147">Código de erro de sucesso.</span><span class="sxs-lookup"><span data-stu-id="5ab2a-147">Success error code.</span></span>|  
  
## <span data-ttu-id="5ab2a-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ab2a-148">Requirements</span></span>  
 <span data-ttu-id="5ab2a-149">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5ab2a-149">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5ab2a-150">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5ab2a-150">See Also</span></span>  
 [<span data-ttu-id="5ab2a-151">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5ab2a-151">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)