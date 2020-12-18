---
description: Inicializa o passado `VARIANT` como uma projeção de um valor JavaScript.
title: Função JsValueToVariant | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f383f2d8bc3aab70b4a361b370698cd71cb714d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231574"
---
# <span data-ttu-id="6fa0f-103">Função JsValueToVariant</span><span class="sxs-lookup"><span data-stu-id="6fa0f-103">JsValueToVariant Function</span></span>

<span data-ttu-id="6fa0f-104">Inicializa o passado `VARIANT` como uma projeção de um valor JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6fa0f-104">Initializes the passed in `VARIANT` as a projection of a JavaScript value.</span></span>  
  
## <span data-ttu-id="6fa0f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fa0f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsValueToVariant(  
   _In_ JsValueRef object,  
   _Out_ VARIANT *variant  
);  
```  
  
#### <span data-ttu-id="6fa0f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fa0f-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="6fa0f-107">Um valor JavaScript para projetar como `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="6fa0f-107">A JavaScript value to project as a `VARIANT`.</span></span>  
  
 `variant`  
 <span data-ttu-id="6fa0f-108">Um ponteiro para uma `VARIANT` estrutura que será inicializada como uma projeção.</span><span class="sxs-lookup"><span data-stu-id="6fa0f-108">A pointer to a `VARIANT` struct that will be initialized as a projection.</span></span>  
  
## <span data-ttu-id="6fa0f-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6fa0f-109">Return Value</span></span>  
  
## <span data-ttu-id="6fa0f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fa0f-110">Remarks</span></span>  
 <span data-ttu-id="6fa0f-111">A projeção `VARIANT` pode ser usada por clientes de automação com para chamar o objeto JavaScript projetado.</span><span class="sxs-lookup"><span data-stu-id="6fa0f-111">The projection `VARIANT` can be used by COM automation clients to call into the projected JavaScript object.</span></span>  
  
 <span data-ttu-id="6fa0f-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="6fa0f-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="6fa0f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fa0f-113">Requirements</span></span>  
 <span data-ttu-id="6fa0f-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6fa0f-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6fa0f-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6fa0f-115">See Also</span></span>  
 [<span data-ttu-id="6fa0f-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6fa0f-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
