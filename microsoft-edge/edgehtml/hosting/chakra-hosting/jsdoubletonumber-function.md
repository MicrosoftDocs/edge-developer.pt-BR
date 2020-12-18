---
description: Cria um valor de número de um valor duplo.
title: Função JsDoubleToNumber | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDoubleToNumber
helpviewer_keywords:
- JsDoubleToNumber function
ms.assetid: 43eb2ee1-2789-4302-954e-c4087e1ee786
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d3385633f41c2e20c43ca865eaeec763b6ff7f43
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231624"
---
# <span data-ttu-id="4cf53-103">Função JsDoubleToNumber</span><span class="sxs-lookup"><span data-stu-id="4cf53-103">JsDoubleToNumber Function</span></span>

<span data-ttu-id="4cf53-104">Cria um valor numérico a partir de um `double` valor.</span><span class="sxs-lookup"><span data-stu-id="4cf53-104">Creates a number value from a `double` value.</span></span>  
  
## <span data-ttu-id="4cf53-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4cf53-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDoubleToNumber(  
   _In_ double doubleValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="4cf53-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4cf53-106">Parameters</span></span>  
 `doubleValue`  
 <span data-ttu-id="4cf53-107">A `double` para converter para um valor numérico.</span><span class="sxs-lookup"><span data-stu-id="4cf53-107">The `double` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="4cf53-108">O novo valor numérico.</span><span class="sxs-lookup"><span data-stu-id="4cf53-108">The new number value.</span></span>  
  
## <span data-ttu-id="4cf53-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4cf53-109">Return Value</span></span>  
 <span data-ttu-id="4cf53-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="4cf53-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4cf53-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4cf53-111">Remarks</span></span>  
 <span data-ttu-id="4cf53-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="4cf53-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4cf53-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cf53-113">Requirements</span></span>  
 <span data-ttu-id="4cf53-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4cf53-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4cf53-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4cf53-115">See Also</span></span>  
 [<span data-ttu-id="4cf53-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4cf53-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
