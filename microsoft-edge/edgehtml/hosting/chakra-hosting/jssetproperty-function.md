---
description: Coloca a propriedade de um objeto.
title: Função JsSetProperty | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetProperty
helpviewer_keywords:
- JsSetProperty function
ms.assetid: 2c36bebf-ec86-425c-8131-2dd75fd30f40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 29c3e04fc240bd63fc755c6727752d053b94484d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231634"
---
# <span data-ttu-id="e78c8-103">Função JsSetProperty</span><span class="sxs-lookup"><span data-stu-id="e78c8-103">JsSetProperty Function</span></span>

<span data-ttu-id="e78c8-104">Coloca a propriedade de um objeto.</span><span class="sxs-lookup"><span data-stu-id="e78c8-104">Puts an object's property.</span></span>  
  
## <span data-ttu-id="e78c8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e78c8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef value,  
   _In_ bool useStrictRules  
);  
```  
  
#### <span data-ttu-id="e78c8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e78c8-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="e78c8-107">O objeto que contém a propriedade.</span><span class="sxs-lookup"><span data-stu-id="e78c8-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="e78c8-108">A ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="e78c8-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="e78c8-109">O novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="e78c8-109">The new value of the property.</span></span>  
  
 `useStrictRules`  
 <span data-ttu-id="e78c8-110">O conjunto de propriedades deve seguir as regras do modo estrito.</span><span class="sxs-lookup"><span data-stu-id="e78c8-110">The property set should follow strict mode rules.</span></span>  
  
## <span data-ttu-id="e78c8-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e78c8-111">Return Value</span></span>  
 <span data-ttu-id="e78c8-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="e78c8-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e78c8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e78c8-113">Remarks</span></span>  
 <span data-ttu-id="e78c8-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="e78c8-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e78c8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e78c8-115">Requirements</span></span>  
 <span data-ttu-id="e78c8-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e78c8-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e78c8-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e78c8-117">See Also</span></span>  
 [<span data-ttu-id="e78c8-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e78c8-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
