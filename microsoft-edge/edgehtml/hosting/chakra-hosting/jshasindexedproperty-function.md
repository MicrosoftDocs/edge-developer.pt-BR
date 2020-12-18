---
description: Testa se um objeto tem um valor no índice especificado.
title: Função JsHasIndexedProperty | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasIndexedProperty
helpviewer_keywords:
- JsHasIndexedProperty function
ms.assetid: 30436a3d-fda0-407e-aba2-142be2310372
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9eb1794c465b4b116978a2150285e2fed3ae1d9b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231635"
---
# <span data-ttu-id="8e973-103">Função JsHasIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="8e973-103">JsHasIndexedProperty Function</span></span>

<span data-ttu-id="8e973-104">Testa se um objeto tem um valor no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="8e973-104">Tests whether an object has a value at the specified index.</span></span>  
  
## <span data-ttu-id="8e973-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e973-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="8e973-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e973-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="8e973-107">O objeto no qual operar.</span><span class="sxs-lookup"><span data-stu-id="8e973-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="8e973-108">O índice a ser testado.</span><span class="sxs-lookup"><span data-stu-id="8e973-108">The index to test.</span></span>  
  
 `result`  
 <span data-ttu-id="8e973-109">Se o objeto tem um valor no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="8e973-109">Whether the object has an value at the specified index.</span></span>  
  
## <span data-ttu-id="8e973-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8e973-110">Return Value</span></span>  
 <span data-ttu-id="8e973-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="8e973-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8e973-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e973-112">Remarks</span></span>  
 <span data-ttu-id="8e973-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="8e973-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="8e973-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e973-114">Requirements</span></span>  
 <span data-ttu-id="8e973-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8e973-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8e973-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8e973-116">See Also</span></span>  
 [<span data-ttu-id="8e973-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8e973-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
