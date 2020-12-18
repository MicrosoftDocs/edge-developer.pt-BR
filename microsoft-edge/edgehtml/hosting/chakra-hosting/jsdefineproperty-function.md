---
description: Define a propriedade do novo objeto de um descritor de propriedades.
title: Função JsDefineProperty | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDefineProperty
helpviewer_keywords:
- JsDefineProperty function
ms.assetid: b2cf48d6-eb40-457c-aa8b-b16a50dc5d6a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a35dd6214190fa558c50cbb743b0f2b92b5e00b3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231772"
---
# <span data-ttu-id="3f2a1-103">Função JsDefineProperty</span><span class="sxs-lookup"><span data-stu-id="3f2a1-103">JsDefineProperty Function</span></span>

<span data-ttu-id="3f2a1-104">Define a propriedade do novo objeto de um descritor de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-104">Defines a new object's own property from a property descriptor.</span></span>  
  
## <span data-ttu-id="3f2a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f2a1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDefineProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef propertyDescriptor,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="3f2a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f2a1-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="3f2a1-107">O objeto que tem a propriedade.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="3f2a1-108">A ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="3f2a1-109">O descritor de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-109">The property descriptor.</span></span>  
  
 `result`  
 <span data-ttu-id="3f2a1-110">Se a propriedade foi definida.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-110">Whether the property was defined.</span></span>  
  
## <span data-ttu-id="3f2a1-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3f2a1-111">Return Value</span></span>  
 <span data-ttu-id="3f2a1-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3f2a1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f2a1-113">Remarks</span></span>  
 <span data-ttu-id="3f2a1-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="3f2a1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f2a1-115">Requirements</span></span>  
 <span data-ttu-id="3f2a1-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3f2a1-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3f2a1-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3f2a1-117">See Also</span></span>  
 [<span data-ttu-id="3f2a1-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3f2a1-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
