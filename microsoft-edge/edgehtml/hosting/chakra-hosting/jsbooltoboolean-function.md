---
description: Cria um valor booliano a partir de um `bool` valor.
title: Função JsBoolToBoolean | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsBoolToBoolean
helpviewer_keywords:
- JsBoolToBoolean function
ms.assetid: 24322ea3-0638-40a3-9b4c-fc912ebed3ff
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3d6ec9f85d53e0d78c6bbe1c7d3282971831717b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231442"
---
# <span data-ttu-id="f33ea-103">Função JsBoolToBoolean</span><span class="sxs-lookup"><span data-stu-id="f33ea-103">JsBoolToBoolean Function</span></span>

<span data-ttu-id="f33ea-104">Cria um valor booliano a partir de um `bool` valor.</span><span class="sxs-lookup"><span data-stu-id="f33ea-104">Creates a Boolean value from a `bool` value.</span></span>  
  
## <span data-ttu-id="f33ea-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f33ea-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode JsBoolToBoolean(  
   _In_ bool value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="f33ea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f33ea-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="f33ea-107">O valor a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="f33ea-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="f33ea-108">O valor convertido.</span><span class="sxs-lookup"><span data-stu-id="f33ea-108">The converted value.</span></span>  
  
## <span data-ttu-id="f33ea-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f33ea-109">Return Value</span></span>  
 <span data-ttu-id="f33ea-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="f33ea-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f33ea-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f33ea-111">Remarks</span></span>  
 <span data-ttu-id="f33ea-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="f33ea-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f33ea-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f33ea-113">Requirements</span></span>  
 <span data-ttu-id="f33ea-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f33ea-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f33ea-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f33ea-115">See Also</span></span>  
 [<span data-ttu-id="f33ea-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f33ea-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
