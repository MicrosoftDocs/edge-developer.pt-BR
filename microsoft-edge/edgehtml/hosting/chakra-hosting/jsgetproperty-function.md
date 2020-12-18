---
description: Obtém a propriedade de um objeto.
title: Função JsGetProperty | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetProperty
helpviewer_keywords:
- JsGetProperty function
ms.assetid: 606bc14f-e849-4f88-a148-6660e923c07b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e5731fa3f889fc1b182f88e37ae90c96d3825402
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231228"
---
# <span data-ttu-id="821cf-103">Função JsGetProperty</span><span class="sxs-lookup"><span data-stu-id="821cf-103">JsGetProperty Function</span></span>

<span data-ttu-id="821cf-104">Obtém a propriedade de um objeto.</span><span class="sxs-lookup"><span data-stu-id="821cf-104">Gets an object's property.</span></span>  
  
## <span data-ttu-id="821cf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="821cf-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="821cf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="821cf-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="821cf-107">O objeto que contém a propriedade.</span><span class="sxs-lookup"><span data-stu-id="821cf-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="821cf-108">A ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="821cf-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="821cf-109">O valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="821cf-109">The value of the property.</span></span>  
  
## <span data-ttu-id="821cf-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="821cf-110">Return Value</span></span>  
 <span data-ttu-id="821cf-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="821cf-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="821cf-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="821cf-112">Remarks</span></span>  
 <span data-ttu-id="821cf-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="821cf-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="821cf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="821cf-114">Requirements</span></span>  
 <span data-ttu-id="821cf-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="821cf-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="821cf-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="821cf-116">See Also</span></span>  
 [<span data-ttu-id="821cf-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="821cf-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
