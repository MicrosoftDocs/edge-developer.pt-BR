---
description: Obtém o valor do `false` contexto do script atual.
title: Função JsGetFalseValue | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetFalseValue
helpviewer_keywords:
- JsGetFalseValue function
ms.assetid: 621a584c-4ca8-4ba0-b19a-6cb50cf830b6
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 52e54ad7eb34877c3cb83b06f5aba70edf285bca
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561055"
---
# <span data-ttu-id="429f0-103">Função JsGetFalseValue</span><span class="sxs-lookup"><span data-stu-id="429f0-103">JsGetFalseValue Function</span></span>
<span data-ttu-id="429f0-104">Obtém o valor do `false` contexto do script atual.</span><span class="sxs-lookup"><span data-stu-id="429f0-104">Gets the value of `false` in the current script context.</span></span>  
  
## <span data-ttu-id="429f0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="429f0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetFalseValue(  
   _Out_ JsValueRef *falseValue  
);  
```  
  
#### <span data-ttu-id="429f0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="429f0-106">Parameters</span></span>  
 `falseValue`  
 <span data-ttu-id="429f0-107">O `false` valor.</span><span class="sxs-lookup"><span data-stu-id="429f0-107">The `false` value.</span></span>  
  
## <span data-ttu-id="429f0-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="429f0-108">Return Value</span></span>  
 <span data-ttu-id="429f0-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="429f0-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="429f0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="429f0-110">Remarks</span></span>  
 <span data-ttu-id="429f0-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="429f0-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="429f0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="429f0-112">Requirements</span></span>  
 <span data-ttu-id="429f0-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="429f0-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="429f0-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="429f0-114">See Also</span></span>  
 [<span data-ttu-id="429f0-115">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="429f0-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)