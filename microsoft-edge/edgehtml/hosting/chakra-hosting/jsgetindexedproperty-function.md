---
description: Recuperar o valor no índice especificado de um objeto.
title: Função JsGetIndexedProperty | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetIndexedProperty
helpviewer_keywords:
- JsGetIndexedProperty function
ms.assetid: f61ea388-0ae6-4a19-b3b5-75ed49a3f32d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bd0246464d00884ca71fd8d3564ce775415f6267
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231252"
---
# <span data-ttu-id="b75cf-103">Função JsGetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="b75cf-103">JsGetIndexedProperty Function</span></span>

<span data-ttu-id="b75cf-104">Recuperar o valor no índice especificado de um objeto.</span><span class="sxs-lookup"><span data-stu-id="b75cf-104">Retrieve the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="b75cf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b75cf-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="b75cf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b75cf-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="b75cf-107">O objeto no qual operar.</span><span class="sxs-lookup"><span data-stu-id="b75cf-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="b75cf-108">O índice a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="b75cf-108">The index to retrieve.</span></span>  
  
 `result`  
 <span data-ttu-id="b75cf-109">O valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="b75cf-109">The retrieved value.</span></span>  
  
## <span data-ttu-id="b75cf-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b75cf-110">Return Value</span></span>  
 <span data-ttu-id="b75cf-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="b75cf-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b75cf-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b75cf-112">Remarks</span></span>  
 <span data-ttu-id="b75cf-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="b75cf-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b75cf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b75cf-114">Requirements</span></span>  
 <span data-ttu-id="b75cf-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b75cf-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b75cf-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b75cf-116">See Also</span></span>  
 [<span data-ttu-id="b75cf-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b75cf-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
