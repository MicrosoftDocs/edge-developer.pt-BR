---
description: Obtém o valor do `false` contexto do script atual.
title: Função JsGetFalseValue | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetFalseValue
helpviewer_keywords:
- JsGetFalseValue function
ms.assetid: 621a584c-4ca8-4ba0-b19a-6cb50cf830b6
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c87ad969fc7547f4d650148005327fb93dce805d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231667"
---
# <span data-ttu-id="1f62a-103">Função JsGetFalseValue</span><span class="sxs-lookup"><span data-stu-id="1f62a-103">JsGetFalseValue Function</span></span>

<span data-ttu-id="1f62a-104">Obtém o valor do `false` contexto do script atual.</span><span class="sxs-lookup"><span data-stu-id="1f62a-104">Gets the value of `false` in the current script context.</span></span>  
  
## <span data-ttu-id="1f62a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f62a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetFalseValue(  
   _Out_ JsValueRef *falseValue  
);  
```  
  
#### <span data-ttu-id="1f62a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f62a-106">Parameters</span></span>  
 `falseValue`  
 <span data-ttu-id="1f62a-107">O `false` valor.</span><span class="sxs-lookup"><span data-stu-id="1f62a-107">The `false` value.</span></span>  
  
## <span data-ttu-id="1f62a-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1f62a-108">Return Value</span></span>  
 <span data-ttu-id="1f62a-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="1f62a-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1f62a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f62a-110">Remarks</span></span>  
 <span data-ttu-id="1f62a-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="1f62a-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="1f62a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f62a-112">Requirements</span></span>  
 <span data-ttu-id="1f62a-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1f62a-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1f62a-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1f62a-114">See Also</span></span>  
 [<span data-ttu-id="1f62a-115">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1f62a-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
