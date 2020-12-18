---
description: Comparar dois valores JavaScript para igualdade estrita.
title: Função JsStrictEquals | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStrictEquals
helpviewer_keywords:
- JsStrictEquals function
ms.assetid: b35bc655-7ff8-496a-b678-8950bb976047
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 98af1629129986cc21cafe5660d3155e031919dc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231581"
---
# <span data-ttu-id="137c4-103">Função JsStrictEquals</span><span class="sxs-lookup"><span data-stu-id="137c4-103">JsStrictEquals Function</span></span>

<span data-ttu-id="137c4-104">Comparar dois valores JavaScript para igualdade estrita.</span><span class="sxs-lookup"><span data-stu-id="137c4-104">Compare two JavaScript values for strict equality.</span></span>  
  
## <span data-ttu-id="137c4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="137c4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStrictEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="137c4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="137c4-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="137c4-107">O primeiro objeto a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="137c4-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="137c4-108">O segundo objeto a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="137c4-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="137c4-109">Se os valores são estritamente iguais.</span><span class="sxs-lookup"><span data-stu-id="137c4-109">Whether the values are strictly equal.</span></span>  
  
## <span data-ttu-id="137c4-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="137c4-110">Return Value</span></span>  
 <span data-ttu-id="137c4-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="137c4-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="137c4-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="137c4-112">Remarks</span></span>  
 <span data-ttu-id="137c4-113">Esta função é equivalente à `===` operadora em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="137c4-113">This function is equivalent to the `===` operator in Javascript.</span></span>  
  
 <span data-ttu-id="137c4-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="137c4-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="137c4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="137c4-115">Requirements</span></span>  
 <span data-ttu-id="137c4-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="137c4-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="137c4-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="137c4-117">See Also</span></span>  
 [<span data-ttu-id="137c4-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="137c4-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
