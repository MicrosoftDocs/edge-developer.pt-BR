---
description: Define o tempo de execução do contexto atual como um estado de exceção.
title: Função JsSetException | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2c2e3840d2a831db23a525c5d8854b9b2fcfb8c9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231621"
---
# <span data-ttu-id="d0146-103">Função JsSetException</span><span class="sxs-lookup"><span data-stu-id="d0146-103">JsSetException Function</span></span>

<span data-ttu-id="d0146-104">Define o tempo de execução do contexto atual como um estado de exceção.</span><span class="sxs-lookup"><span data-stu-id="d0146-104">Sets the runtime of the current context to an exception state.</span></span>  
  
## <span data-ttu-id="d0146-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0146-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetException(  
   _In_ JsValueRef exception  
);  
```  
  
#### <span data-ttu-id="d0146-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0146-106">Parameters</span></span>  
 `exception`  
 <span data-ttu-id="d0146-107">A exceção JavaScript a ser definida para o tempo de execução do contexto atual.</span><span class="sxs-lookup"><span data-stu-id="d0146-107">The JavaScript exception to set for the runtime of the current context.</span></span>  
  
## <span data-ttu-id="d0146-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d0146-108">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="d0146-109">Se o mecanismo tiver sido definido como um estado de exceção, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="d0146-109">if the engine was set into an exception state, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d0146-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0146-110">Remarks</span></span>  
 <span data-ttu-id="d0146-111">Se o tempo de execução do contexto atual já estiver em um estado de exceção, essa API retornará `JsErrorInExceptionState` .</span><span class="sxs-lookup"><span data-stu-id="d0146-111">If the runtime of the current context is already in an exception state, this API will return `JsErrorInExceptionState`.</span></span>  
  
 <span data-ttu-id="d0146-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="d0146-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d0146-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0146-113">Requirements</span></span>  
 <span data-ttu-id="d0146-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d0146-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d0146-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d0146-115">See Also</span></span>  
 [<span data-ttu-id="d0146-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d0146-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
