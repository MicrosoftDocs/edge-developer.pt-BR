---
description: Determina se um objeto tem uma propriedade.
title: Função JsHasProperty | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasProperty
helpviewer_keywords:
- JsHasProperty function
ms.assetid: 26c94c3d-aae6-4257-8644-df63c7e714fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e45ecfaafb06c49a6a3773eb798ee93a19fd6d6e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231633"
---
# <span data-ttu-id="7e9ce-103">Função JsHasProperty</span><span class="sxs-lookup"><span data-stu-id="7e9ce-103">JsHasProperty Function</span></span>

<span data-ttu-id="7e9ce-104">Determina se um objeto tem uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="7e9ce-104">Determines whether an object has a property.</span></span>  
  
## <span data-ttu-id="7e9ce-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e9ce-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ bool *hasProperty  
);  
```  
  
#### <span data-ttu-id="7e9ce-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e9ce-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="7e9ce-107">O objeto que pode conter a propriedade.</span><span class="sxs-lookup"><span data-stu-id="7e9ce-107">The object that may contain the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="7e9ce-108">A ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="7e9ce-108">The ID of the property.</span></span>  
  
 `hasProperty`  
 <span data-ttu-id="7e9ce-109">Se o objeto (ou um protótipo) tem a propriedade.</span><span class="sxs-lookup"><span data-stu-id="7e9ce-109">Whether the object (or a prototype) has the property.</span></span>  
  
## <span data-ttu-id="7e9ce-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7e9ce-110">Return Value</span></span>  
 <span data-ttu-id="7e9ce-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="7e9ce-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7e9ce-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e9ce-112">Remarks</span></span>  
 <span data-ttu-id="7e9ce-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="7e9ce-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="7e9ce-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e9ce-114">Requirements</span></span>  
 <span data-ttu-id="7e9ce-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7e9ce-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7e9ce-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7e9ce-116">See Also</span></span>  
 [<span data-ttu-id="7e9ce-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7e9ce-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
