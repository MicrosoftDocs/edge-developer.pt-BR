---
description: Obtém o valor do `null` contexto do script atual.
title: Função JsGetNullValue | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetNullValue
helpviewer_keywords:
- JsGetNullValue function
ms.assetid: 132a1496-8dfe-4d3c-a8f8-389f5b0b50d2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 84164aa9ce5d522b0933d928d85b26c652be066f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562188"
---
# <span data-ttu-id="29c66-103">Função JsGetNullValue</span><span class="sxs-lookup"><span data-stu-id="29c66-103">JsGetNullValue Function</span></span>
<span data-ttu-id="29c66-104">Obtém o valor do `null` contexto do script atual.</span><span class="sxs-lookup"><span data-stu-id="29c66-104">Gets the value of `null` in the current script context.</span></span>  
  
## <span data-ttu-id="29c66-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29c66-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetNullValue(  
   _Out_ JsValueRef *nullValue  
);  
```  
  
#### <span data-ttu-id="29c66-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29c66-106">Parameters</span></span>  
 `nullValue`  
 <span data-ttu-id="29c66-107">O `null` valor.</span><span class="sxs-lookup"><span data-stu-id="29c66-107">The `null` value.</span></span>  
  
## <span data-ttu-id="29c66-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="29c66-108">Return Value</span></span>  
 <span data-ttu-id="29c66-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="29c66-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="29c66-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="29c66-110">Remarks</span></span>  
 <span data-ttu-id="29c66-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="29c66-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="29c66-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29c66-112">Requirements</span></span>  
 <span data-ttu-id="29c66-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="29c66-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="29c66-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="29c66-114">See Also</span></span>  
 [<span data-ttu-id="29c66-115">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="29c66-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)