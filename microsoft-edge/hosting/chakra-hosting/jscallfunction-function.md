---
description: Invoca uma função.
title: Função JsCallFunction | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCallFunction
helpviewer_keywords:
- JsCallFunction function
ms.assetid: 8a1dca72-d720-4a28-a86e-6809465006fe
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f242ccef71d8a2b361dbe2d1a299728f5551f5d3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561128"
---
# <span data-ttu-id="1b177-103">Função JsCallFunction</span><span class="sxs-lookup"><span data-stu-id="1b177-103">JsCallFunction Function</span></span>
<span data-ttu-id="1b177-104">Invoca uma função.</span><span class="sxs-lookup"><span data-stu-id="1b177-104">Invokes a function.</span></span>  
  
## <span data-ttu-id="1b177-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b177-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCallFunction(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="1b177-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b177-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="1b177-107">A função a ser invocada.</span><span class="sxs-lookup"><span data-stu-id="1b177-107">The function to invoke.</span></span>  
  
 `arguments`  
 <span data-ttu-id="1b177-108">Os argumentos para a chamada.</span><span class="sxs-lookup"><span data-stu-id="1b177-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="1b177-109">O número de argumentos sendo passados para a função.</span><span class="sxs-lookup"><span data-stu-id="1b177-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="1b177-110">O valor retornado da invocação da função, se houver.</span><span class="sxs-lookup"><span data-stu-id="1b177-110">The value returned from the function invocation, if any.</span></span>  
  
## <span data-ttu-id="1b177-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1b177-111">Return Value</span></span>  
 <span data-ttu-id="1b177-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="1b177-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1b177-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b177-113">Remarks</span></span>  
 <span data-ttu-id="1b177-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="1b177-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="1b177-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b177-115">Requirements</span></span>  
 <span data-ttu-id="1b177-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1b177-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1b177-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1b177-117">See Also</span></span>  
 [<span data-ttu-id="1b177-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1b177-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)