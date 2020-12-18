---
description: Define o valor no índice especificado de um objeto.
title: Função JsSetIndexedProperty | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetIndexedProperty
helpviewer_keywords:
- JsSetIndexedProperty function
ms.assetid: ccbc5bf4-d99b-485c-ab25-d2bd1ed2142e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1fa961750fa5db262e1512d8d26572280d5e726c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231403"
---
# <span data-ttu-id="cbe2d-103">Função JsSetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="cbe2d-103">JsSetIndexedProperty Function</span></span>

<span data-ttu-id="cbe2d-104">Define o valor no índice especificado de um objeto.</span><span class="sxs-lookup"><span data-stu-id="cbe2d-104">Set the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="cbe2d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbe2d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _In_ JsValueRef value  
);  
```  
  
#### <span data-ttu-id="cbe2d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbe2d-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="cbe2d-107">O objeto no qual operar.</span><span class="sxs-lookup"><span data-stu-id="cbe2d-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="cbe2d-108">O índice a ser definido.</span><span class="sxs-lookup"><span data-stu-id="cbe2d-108">The index to set.</span></span>  
  
 `value`  
 <span data-ttu-id="cbe2d-109">O valor a ser definido.</span><span class="sxs-lookup"><span data-stu-id="cbe2d-109">The value to set.</span></span>  
  
## <span data-ttu-id="cbe2d-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cbe2d-110">Return Value</span></span>  
 <span data-ttu-id="cbe2d-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="cbe2d-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="cbe2d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbe2d-112">Remarks</span></span>  
 <span data-ttu-id="cbe2d-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="cbe2d-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="cbe2d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbe2d-114">Requirements</span></span>  
 <span data-ttu-id="cbe2d-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cbe2d-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cbe2d-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cbe2d-116">See Also</span></span>  
 [<span data-ttu-id="cbe2d-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="cbe2d-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
