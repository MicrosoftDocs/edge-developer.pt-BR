---
description: Obtém um descritor de propriedades para a propriedade do próprio objeto.
title: Função JsGetOwnPropertyDescriptor | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyDescriptor
helpviewer_keywords:
- JsGetOwnPropertyDescriptor function
ms.assetid: 44c417ce-ab63-44eb-a0ab-19838e3ab34f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 05c7a58fa12d7ca8013c512f40031963ebc8ac18
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231619"
---
# <span data-ttu-id="01989-103">Função JsGetOwnPropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="01989-103">JsGetOwnPropertyDescriptor Function</span></span>

<span data-ttu-id="01989-104">Obtém um descritor de propriedades para a propriedade do próprio objeto.</span><span class="sxs-lookup"><span data-stu-id="01989-104">Gets a property descriptor for an object's own property.</span></span>  
  
## <span data-ttu-id="01989-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01989-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyDescriptor(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *propertyDescriptor  
);  
```  
  
#### <span data-ttu-id="01989-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01989-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="01989-107">O objeto que tem a propriedade.</span><span class="sxs-lookup"><span data-stu-id="01989-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="01989-108">A ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="01989-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="01989-109">O descritor de propriedades.</span><span class="sxs-lookup"><span data-stu-id="01989-109">The property descriptor.</span></span>  
  
## <span data-ttu-id="01989-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="01989-110">Return Value</span></span>  
 <span data-ttu-id="01989-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="01989-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="01989-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="01989-112">Remarks</span></span>  
 <span data-ttu-id="01989-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="01989-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="01989-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01989-114">Requirements</span></span>  
 <span data-ttu-id="01989-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="01989-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="01989-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="01989-116">See Also</span></span>  
 [<span data-ttu-id="01989-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="01989-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
