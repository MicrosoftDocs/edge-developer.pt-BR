---
description: Exclui a propriedade de um objeto.
title: Função JsDeleteProperty | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteProperty
helpviewer_keywords:
- JsDeleteProperty function
ms.assetid: 0f6ac6a7-3576-42f5-98d0-1c06542c8149
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55089bd4cff7ef4d58bcce1d7531d4ca1c7381ae
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231255"
---
# <span data-ttu-id="ede2f-103">Função JsDeleteProperty</span><span class="sxs-lookup"><span data-stu-id="ede2f-103">JsDeleteProperty Function</span></span>

<span data-ttu-id="ede2f-104">Exclui a propriedade de um objeto.</span><span class="sxs-lookup"><span data-stu-id="ede2f-104">Deletes an object's property.</span></span>  
  
## <span data-ttu-id="ede2f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ede2f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ bool useStrictRules,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="ede2f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ede2f-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="ede2f-107">O objeto que contém a propriedade.</span><span class="sxs-lookup"><span data-stu-id="ede2f-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="ede2f-108">A ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="ede2f-108">The ID of the property.</span></span>  
  
 `useStrictRules`  
 <span data-ttu-id="ede2f-109">O conjunto de propriedades deve seguir as regras do modo estrito.</span><span class="sxs-lookup"><span data-stu-id="ede2f-109">The property set should follow strict mode rules.</span></span>  
  
 `result`  
 <span data-ttu-id="ede2f-110">Se a propriedade foi excluída.</span><span class="sxs-lookup"><span data-stu-id="ede2f-110">Whether the property was deleted.</span></span>  
  
## <span data-ttu-id="ede2f-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ede2f-111">Return Value</span></span>  
 <span data-ttu-id="ede2f-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="ede2f-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ede2f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ede2f-113">Remarks</span></span>  
 <span data-ttu-id="ede2f-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="ede2f-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ede2f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ede2f-115">Requirements</span></span>  
 <span data-ttu-id="ede2f-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ede2f-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ede2f-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ede2f-117">See Also</span></span>  
 [<span data-ttu-id="ede2f-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ede2f-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
