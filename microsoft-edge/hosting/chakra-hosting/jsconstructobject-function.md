---
description: Invoca uma função como um construtor.
title: Função JsConstructObject | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConstructObject
helpviewer_keywords:
- JsConstructObject function
ms.assetid: b07d2440-db55-4a6a-8376-56b40a8039a1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6fb9654b5c7321d6c6b0b255ec897fb30a114041
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561123"
---
# <span data-ttu-id="844ba-103">Função JsConstructObject</span><span class="sxs-lookup"><span data-stu-id="844ba-103">JsConstructObject Function</span></span>
<span data-ttu-id="844ba-104">Invoca uma função como um construtor.</span><span class="sxs-lookup"><span data-stu-id="844ba-104">Invokes a function as a constructor.</span></span>  
  
## <span data-ttu-id="844ba-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="844ba-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConstructObject(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="844ba-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="844ba-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="844ba-107">A função a ser invocada como um construtor.</span><span class="sxs-lookup"><span data-stu-id="844ba-107">The function to invoke as a constructor.</span></span>  
  
 `arguments`  
 <span data-ttu-id="844ba-108">Os argumentos para a chamada.</span><span class="sxs-lookup"><span data-stu-id="844ba-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="844ba-109">O número de argumentos sendo passados para a função.</span><span class="sxs-lookup"><span data-stu-id="844ba-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="844ba-110">O valor retornado da invocação da função.</span><span class="sxs-lookup"><span data-stu-id="844ba-110">The value returned from the function invocation.</span></span>  
  
## <span data-ttu-id="844ba-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="844ba-111">Return Value</span></span>  
 <span data-ttu-id="844ba-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="844ba-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="844ba-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="844ba-113">Remarks</span></span>  
 <span data-ttu-id="844ba-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="844ba-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="844ba-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="844ba-115">Requirements</span></span>  
 <span data-ttu-id="844ba-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="844ba-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="844ba-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="844ba-117">See Also</span></span>  
 [<span data-ttu-id="844ba-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="844ba-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)