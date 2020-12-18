---
description: Retorna o protótipo de um objeto.
title: Função JsGetPrototype | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPrototype
helpviewer_keywords:
- JsGetPrototype function
ms.assetid: 05d743fc-103e-4a92-86f2-a063f39a2a6f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d64e8b090753e5d0627f0d40ee8745eeadd65227
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231921"
---
# <span data-ttu-id="2f1eb-103">Função JsGetPrototype</span><span class="sxs-lookup"><span data-stu-id="2f1eb-103">JsGetPrototype Function</span></span>

<span data-ttu-id="2f1eb-104">Retorna o protótipo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-104">Returns the prototype of an object.</span></span>  
  
## <span data-ttu-id="2f1eb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f1eb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPrototype(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *prototypeObject  
);  
```  
  
#### <span data-ttu-id="2f1eb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f1eb-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="2f1eb-107">O objeto cujo protótipo deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-107">The object whose prototype is to be returned.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="2f1eb-108">O protótipo do objeto.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-108">The object's prototype.</span></span>  
  
## <span data-ttu-id="2f1eb-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2f1eb-109">Return Value</span></span>  
 <span data-ttu-id="2f1eb-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2f1eb-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f1eb-111">Remarks</span></span>  
 <span data-ttu-id="2f1eb-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="2f1eb-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="2f1eb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f1eb-113">Requirements</span></span>  
 <span data-ttu-id="2f1eb-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2f1eb-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2f1eb-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2f1eb-115">See Also</span></span>  
 [<span data-ttu-id="2f1eb-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2f1eb-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
