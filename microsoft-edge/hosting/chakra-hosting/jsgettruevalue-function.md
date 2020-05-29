---
description: Obtém o valor do `true` contexto do script atual.
title: Função JsGetTrueValue | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetTrueValue
helpviewer_keywords:
- JsGetTrueValue function
ms.assetid: c2a56d48-344b-492b-90b8-f570710f8310
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 620ed775947db9d7156d61df1cfdf974a46baec2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561035"
---
# <span data-ttu-id="30d61-103">Função JsGetTrueValue</span><span class="sxs-lookup"><span data-stu-id="30d61-103">JsGetTrueValue Function</span></span>
<span data-ttu-id="30d61-104">Obtém o valor do `true` contexto do script atual.</span><span class="sxs-lookup"><span data-stu-id="30d61-104">Gets the value of `true` in the current script context.</span></span>  
  
## <span data-ttu-id="30d61-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30d61-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTrueValue(  
   _Out_ JsValueRef *trueValue  
);  
```  
  
#### <span data-ttu-id="30d61-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30d61-106">Parameters</span></span>  
 `trueValue`  
 <span data-ttu-id="30d61-107">O `true` valor.</span><span class="sxs-lookup"><span data-stu-id="30d61-107">The `true` value.</span></span>  
  
## <span data-ttu-id="30d61-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="30d61-108">Return Value</span></span>  
 <span data-ttu-id="30d61-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="30d61-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="30d61-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="30d61-110">Remarks</span></span>  
 <span data-ttu-id="30d61-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="30d61-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="30d61-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30d61-112">Requirements</span></span>  
 <span data-ttu-id="30d61-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="30d61-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="30d61-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="30d61-114">See Also</span></span>  
 [<span data-ttu-id="30d61-115">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="30d61-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)