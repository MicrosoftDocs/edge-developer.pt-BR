---
description: Retorna a exceção que causou o tempo de execução do contexto atual para estar no estado de exceção e redefine o estado de exceção desse tempo de execução.
title: Função JsGetAndClearException | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetAndClearException
helpviewer_keywords:
- JsGetAndClearException function
ms.assetid: 6aec8a88-41ee-47f6-b5f4-32f3cae6bb7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb296ea351d0466a856d5ac020550ebacc254ac9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231548"
---
# <span data-ttu-id="ec98e-103">Função JsGetAndClearException</span><span class="sxs-lookup"><span data-stu-id="ec98e-103">JsGetAndClearException Function</span></span>

<span data-ttu-id="ec98e-104">Retorna a exceção que causou o tempo de execução do contexto atual para estar no estado de exceção e redefine o estado de exceção desse tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="ec98e-104">Returns the exception that caused the runtime of the current context to be in the exception state and resets the exception state for that runtime.</span></span>  
  
## <span data-ttu-id="ec98e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec98e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetAndClearException(  
   _Out_ JsValueRef *exception  
);  
```  
  
#### <span data-ttu-id="ec98e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec98e-106">Parameters</span></span>  
 `exception`  
 <span data-ttu-id="ec98e-107">A exceção para o tempo de execução do contexto atual.</span><span class="sxs-lookup"><span data-stu-id="ec98e-107">The exception for the runtime of the current context.</span></span>  
  
## <span data-ttu-id="ec98e-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ec98e-108">Return Value</span></span>  
 <span data-ttu-id="ec98e-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="ec98e-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ec98e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec98e-110">Remarks</span></span>  
 <span data-ttu-id="ec98e-111">Se o tempo de execução do contexto atual não estiver em um estado de exceção, essa API retornará `JsErrorInvalidArgument` .</span><span class="sxs-lookup"><span data-stu-id="ec98e-111">If the runtime of the current context is not in an exception state, this API will return `JsErrorInvalidArgument`.</span></span> <span data-ttu-id="ec98e-112">Se o tempo de execução estiver desabilitado, isso retornará uma exceção indicando que o script foi encerrado, mas não limpará a exceção (a exceção será desmarcada se o tempo de execução for habilitado novamente usando `JsEnableRuntimeExecution` ).</span><span class="sxs-lookup"><span data-stu-id="ec98e-112">If the runtime is disabled, this will return an exception indicating that the script was terminated, but it will not clear the exception (the exception will be cleared if the runtime is re-enabled using `JsEnableRuntimeExecution`).</span></span>  
  
 <span data-ttu-id="ec98e-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="ec98e-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ec98e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec98e-114">Requirements</span></span>  
 <span data-ttu-id="ec98e-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ec98e-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ec98e-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ec98e-116">See Also</span></span>  
 [<span data-ttu-id="ec98e-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ec98e-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
