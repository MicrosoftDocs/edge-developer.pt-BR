---
description: Invoca uma função.
title: Função JsCallFunction | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCallFunction
helpviewer_keywords:
- JsCallFunction function
ms.assetid: 8a1dca72-d720-4a28-a86e-6809465006fe
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: dc26f66cb7deae0857ce34cbd4d83ee26046b3c8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231439"
---
# <span data-ttu-id="dfb77-103">Função JsCallFunction</span><span class="sxs-lookup"><span data-stu-id="dfb77-103">JsCallFunction Function</span></span>

<span data-ttu-id="dfb77-104">Invoca uma função.</span><span class="sxs-lookup"><span data-stu-id="dfb77-104">Invokes a function.</span></span>  
  
## <span data-ttu-id="dfb77-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfb77-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCallFunction(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="dfb77-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfb77-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="dfb77-107">A função a ser invocada.</span><span class="sxs-lookup"><span data-stu-id="dfb77-107">The function to invoke.</span></span>  
  
 `arguments`  
 <span data-ttu-id="dfb77-108">Os argumentos para a chamada.</span><span class="sxs-lookup"><span data-stu-id="dfb77-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="dfb77-109">O número de argumentos sendo passados para a função.</span><span class="sxs-lookup"><span data-stu-id="dfb77-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="dfb77-110">O valor retornado da invocação da função, se houver.</span><span class="sxs-lookup"><span data-stu-id="dfb77-110">The value returned from the function invocation, if any.</span></span>  
  
## <span data-ttu-id="dfb77-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dfb77-111">Return Value</span></span>  
 <span data-ttu-id="dfb77-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="dfb77-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dfb77-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfb77-113">Remarks</span></span>  
 <span data-ttu-id="dfb77-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="dfb77-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="dfb77-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfb77-115">Requirements</span></span>  
 <span data-ttu-id="dfb77-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dfb77-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dfb77-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="dfb77-117">See Also</span></span>  
 [<span data-ttu-id="dfb77-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dfb77-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
