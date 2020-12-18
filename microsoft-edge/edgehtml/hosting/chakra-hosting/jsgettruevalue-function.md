---
description: Obtém o valor do `true` contexto do script atual.
title: Função JsGetTrueValue | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetTrueValue
helpviewer_keywords:
- JsGetTrueValue function
ms.assetid: c2a56d48-344b-492b-90b8-f570710f8310
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 58798e1e8aab57d626be0c8c878f9be39d0af942
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231987"
---
# <span data-ttu-id="6c101-103">Função JsGetTrueValue</span><span class="sxs-lookup"><span data-stu-id="6c101-103">JsGetTrueValue Function</span></span>

<span data-ttu-id="6c101-104">Obtém o valor do `true` contexto do script atual.</span><span class="sxs-lookup"><span data-stu-id="6c101-104">Gets the value of `true` in the current script context.</span></span>  
  
## <span data-ttu-id="6c101-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c101-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTrueValue(  
   _Out_ JsValueRef *trueValue  
);  
```  
  
#### <span data-ttu-id="6c101-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c101-106">Parameters</span></span>  
 `trueValue`  
 <span data-ttu-id="6c101-107">O `true` valor.</span><span class="sxs-lookup"><span data-stu-id="6c101-107">The `true` value.</span></span>  
  
## <span data-ttu-id="6c101-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6c101-108">Return Value</span></span>  
 <span data-ttu-id="6c101-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="6c101-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6c101-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c101-110">Remarks</span></span>  
 <span data-ttu-id="6c101-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="6c101-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="6c101-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c101-112">Requirements</span></span>  
 <span data-ttu-id="6c101-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6c101-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6c101-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6c101-114">See Also</span></span>  
 [<span data-ttu-id="6c101-115">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6c101-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
