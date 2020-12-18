---
description: Obtém o valor do `null` contexto do script atual.
title: Função JsGetNullValue | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetNullValue
helpviewer_keywords:
- JsGetNullValue function
ms.assetid: 132a1496-8dfe-4d3c-a8f8-389f5b0b50d2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 31e1ba19f9f27e75f0166238d98390e2c4a26c24
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231251"
---
# <span data-ttu-id="63860-103">Função JsGetNullValue</span><span class="sxs-lookup"><span data-stu-id="63860-103">JsGetNullValue Function</span></span>

<span data-ttu-id="63860-104">Obtém o valor do `null` contexto do script atual.</span><span class="sxs-lookup"><span data-stu-id="63860-104">Gets the value of `null` in the current script context.</span></span>  
  
## <span data-ttu-id="63860-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63860-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetNullValue(  
   _Out_ JsValueRef *nullValue  
);  
```  
  
#### <span data-ttu-id="63860-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63860-106">Parameters</span></span>  
 `nullValue`  
 <span data-ttu-id="63860-107">O `null` valor.</span><span class="sxs-lookup"><span data-stu-id="63860-107">The `null` value.</span></span>  
  
## <span data-ttu-id="63860-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="63860-108">Return Value</span></span>  
 <span data-ttu-id="63860-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="63860-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="63860-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="63860-110">Remarks</span></span>  
 <span data-ttu-id="63860-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="63860-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="63860-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63860-112">Requirements</span></span>  
 <span data-ttu-id="63860-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="63860-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="63860-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="63860-114">See Also</span></span>  
 [<span data-ttu-id="63860-115">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="63860-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
