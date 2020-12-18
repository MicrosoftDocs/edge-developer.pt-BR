---
description: Determina se um objeto é um objeto externo.
title: Função JsHasExternalData | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasExternalData
helpviewer_keywords:
- JsHasExternalData function
ms.assetid: a077e3ac-4f6f-4d94-8398-f1b5cc4c18e0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d73333215a33fc409190a0e33fa616b6350fb2a3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231284"
---
# <span data-ttu-id="1911a-103">Função JsHasExternalData</span><span class="sxs-lookup"><span data-stu-id="1911a-103">JsHasExternalData Function</span></span>

<span data-ttu-id="1911a-104">Determina se um objeto é um objeto externo.</span><span class="sxs-lookup"><span data-stu-id="1911a-104">Determines whether an object is an external object.</span></span>  
  
## <span data-ttu-id="1911a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1911a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="1911a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1911a-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="1911a-107">O objeto.</span><span class="sxs-lookup"><span data-stu-id="1911a-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="1911a-108">Se o objeto é um objeto externo.</span><span class="sxs-lookup"><span data-stu-id="1911a-108">Whether the object is an external object.</span></span>  
  
## <span data-ttu-id="1911a-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1911a-109">Return Value</span></span>  
 <span data-ttu-id="1911a-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="1911a-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1911a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1911a-111">Remarks</span></span>  
 <span data-ttu-id="1911a-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="1911a-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="1911a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1911a-113">Requirements</span></span>  
 <span data-ttu-id="1911a-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1911a-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1911a-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1911a-115">See Also</span></span>  
 [<span data-ttu-id="1911a-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1911a-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
