---
description: Invoca uma função como um construtor.
title: Função JsConstructObject | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConstructObject
helpviewer_keywords:
- JsConstructObject function
ms.assetid: b07d2440-db55-4a6a-8376-56b40a8039a1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8dbb757456412e50efaf3a026d169e6b3612b6b1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231437"
---
# <span data-ttu-id="3a8d5-103">Função JsConstructObject</span><span class="sxs-lookup"><span data-stu-id="3a8d5-103">JsConstructObject Function</span></span>

<span data-ttu-id="3a8d5-104">Invoca uma função como um construtor.</span><span class="sxs-lookup"><span data-stu-id="3a8d5-104">Invokes a function as a constructor.</span></span>  
  
## <span data-ttu-id="3a8d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a8d5-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConstructObject(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="3a8d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a8d5-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="3a8d5-107">A função a ser invocada como um construtor.</span><span class="sxs-lookup"><span data-stu-id="3a8d5-107">The function to invoke as a constructor.</span></span>  
  
 `arguments`  
 <span data-ttu-id="3a8d5-108">Os argumentos para a chamada.</span><span class="sxs-lookup"><span data-stu-id="3a8d5-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="3a8d5-109">O número de argumentos sendo passados para a função.</span><span class="sxs-lookup"><span data-stu-id="3a8d5-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="3a8d5-110">O valor retornado da invocação da função.</span><span class="sxs-lookup"><span data-stu-id="3a8d5-110">The value returned from the function invocation.</span></span>  
  
## <span data-ttu-id="3a8d5-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3a8d5-111">Return Value</span></span>  
 <span data-ttu-id="3a8d5-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="3a8d5-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3a8d5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a8d5-113">Remarks</span></span>  
 <span data-ttu-id="3a8d5-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="3a8d5-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="3a8d5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a8d5-115">Requirements</span></span>  
 <span data-ttu-id="3a8d5-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3a8d5-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3a8d5-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3a8d5-117">See Also</span></span>  
 [<span data-ttu-id="3a8d5-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3a8d5-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
