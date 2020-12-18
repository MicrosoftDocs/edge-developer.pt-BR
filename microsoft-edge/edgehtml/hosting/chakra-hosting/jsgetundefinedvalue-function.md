---
description: Obtém o valor do `undefined` contexto do script atual.
title: Função JsGetUndefinedValue | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetUndefinedValue
helpviewer_keywords:
- JsGetUndefinedValue function
ms.assetid: e118eaf6-452c-42f2-86b8-e63c7d987cba
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 34bfaec4548ee2b77d6d98749c3049bb8f679134
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231285"
---
# <span data-ttu-id="d9867-103">Função JsGetUndefinedValue</span><span class="sxs-lookup"><span data-stu-id="d9867-103">JsGetUndefinedValue Function</span></span>

<span data-ttu-id="d9867-104">Obtém o valor do `undefined` contexto do script atual.</span><span class="sxs-lookup"><span data-stu-id="d9867-104">Gets the value of `undefined` in the current script context.</span></span>  
  
## <span data-ttu-id="d9867-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9867-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetUndefinedValue(  
   _Out_ JsValueRef *undefinedValue  
);  
```  
  
#### <span data-ttu-id="d9867-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9867-106">Parameters</span></span>  
 `undefinedValue`  
 <span data-ttu-id="d9867-107">O `undefined` valor.</span><span class="sxs-lookup"><span data-stu-id="d9867-107">The `undefined` value.</span></span>  
  
## <span data-ttu-id="d9867-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d9867-108">Return Value</span></span>  
 <span data-ttu-id="d9867-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="d9867-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d9867-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9867-110">Remarks</span></span>  
 <span data-ttu-id="d9867-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="d9867-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d9867-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9867-112">Requirements</span></span>  
 <span data-ttu-id="d9867-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d9867-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d9867-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d9867-114">See Also</span></span>  
 [<span data-ttu-id="d9867-115">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d9867-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
