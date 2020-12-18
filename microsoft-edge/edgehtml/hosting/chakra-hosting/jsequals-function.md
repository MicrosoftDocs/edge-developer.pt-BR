---
description: Comparar dois valores JavaScript para igualdade.
title: Função JsEquals | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEquals
helpviewer_keywords:
- JsEquals function
ms.assetid: 8377a7b6-12ff-43e4-8cc8-5a5a198a168b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 88f906419e73ed0de6ddde0a872becbd18908997
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231998"
---
# <span data-ttu-id="c44f0-103">Função JsEquals</span><span class="sxs-lookup"><span data-stu-id="c44f0-103">JsEquals Function</span></span>

<span data-ttu-id="c44f0-104">Comparar dois valores JavaScript para igualdade.</span><span class="sxs-lookup"><span data-stu-id="c44f0-104">Compare two JavaScript values for equality.</span></span>  
  
## <span data-ttu-id="c44f0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c44f0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="c44f0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c44f0-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="c44f0-107">O primeiro objeto a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="c44f0-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="c44f0-108">O segundo objeto a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="c44f0-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="c44f0-109">Se os valores são iguais.</span><span class="sxs-lookup"><span data-stu-id="c44f0-109">Whether the values are equal.</span></span>  
  
## <span data-ttu-id="c44f0-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c44f0-110">Return Value</span></span>  
 <span data-ttu-id="c44f0-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="c44f0-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c44f0-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c44f0-112">Remarks</span></span>  
 <span data-ttu-id="c44f0-113">Esta função é equivalente à `==` operadora em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c44f0-113">This function is equivalent to the `==` operator in Javascript.</span></span>  
  
 <span data-ttu-id="c44f0-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="c44f0-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c44f0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c44f0-115">Requirements</span></span>  
 <span data-ttu-id="c44f0-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c44f0-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c44f0-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c44f0-117">See Also</span></span>  
 [<span data-ttu-id="c44f0-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c44f0-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
