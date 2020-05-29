---
description: Inicializa o passado `VARIANT` como uma projeção de um valor JavaScript.
title: Função JsValueToVariant | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d8748fddcc149cf09fbd46ad3ad489cd66200b71
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560994"
---
# <span data-ttu-id="bb386-103">Função JsValueToVariant</span><span class="sxs-lookup"><span data-stu-id="bb386-103">JsValueToVariant Function</span></span>
<span data-ttu-id="bb386-104">Inicializa o passado `VARIANT` como uma projeção de um valor JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bb386-104">Initializes the passed in `VARIANT` as a projection of a JavaScript value.</span></span>  
  
## <span data-ttu-id="bb386-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb386-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsValueToVariant(  
   _In_ JsValueRef object,  
   _Out_ VARIANT *variant  
);  
```  
  
#### <span data-ttu-id="bb386-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb386-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="bb386-107">Um valor JavaScript para projetar como `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="bb386-107">A JavaScript value to project as a `VARIANT`.</span></span>  
  
 `variant`  
 <span data-ttu-id="bb386-108">Um ponteiro para uma `VARIANT` estrutura que será inicializada como uma projeção.</span><span class="sxs-lookup"><span data-stu-id="bb386-108">A pointer to a `VARIANT` struct that will be initialized as a projection.</span></span>  
  
## <span data-ttu-id="bb386-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bb386-109">Return Value</span></span>  
  
## <span data-ttu-id="bb386-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb386-110">Remarks</span></span>  
 <span data-ttu-id="bb386-111">A projeção `VARIANT` pode ser usada por clientes de automação com para chamar o objeto JavaScript projetado.</span><span class="sxs-lookup"><span data-stu-id="bb386-111">The projection `VARIANT` can be used by COM automation clients to call into the projected JavaScript object.</span></span>  
  
 <span data-ttu-id="bb386-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="bb386-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bb386-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb386-113">Requirements</span></span>  
 <span data-ttu-id="bb386-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bb386-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bb386-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bb386-115">See Also</span></span>  
 [<span data-ttu-id="bb386-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bb386-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)