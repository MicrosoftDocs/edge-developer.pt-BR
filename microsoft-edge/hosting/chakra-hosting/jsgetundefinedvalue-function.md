---
description: Obtém o valor do `undefined` contexto do script atual.
title: Função JsGetUndefinedValue | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetUndefinedValue
helpviewer_keywords:
- JsGetUndefinedValue function
ms.assetid: e118eaf6-452c-42f2-86b8-e63c7d987cba
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5edd536a29f5003591de476cb5d21ddb64f48c0b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562169"
---
# <span data-ttu-id="3aa71-103">Função JsGetUndefinedValue</span><span class="sxs-lookup"><span data-stu-id="3aa71-103">JsGetUndefinedValue Function</span></span>
<span data-ttu-id="3aa71-104">Obtém o valor do `undefined` contexto do script atual.</span><span class="sxs-lookup"><span data-stu-id="3aa71-104">Gets the value of `undefined` in the current script context.</span></span>  
  
## <span data-ttu-id="3aa71-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3aa71-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetUndefinedValue(  
   _Out_ JsValueRef *undefinedValue  
);  
```  
  
#### <span data-ttu-id="3aa71-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3aa71-106">Parameters</span></span>  
 `undefinedValue`  
 <span data-ttu-id="3aa71-107">O `undefined` valor.</span><span class="sxs-lookup"><span data-stu-id="3aa71-107">The `undefined` value.</span></span>  
  
## <span data-ttu-id="3aa71-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3aa71-108">Return Value</span></span>  
 <span data-ttu-id="3aa71-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="3aa71-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3aa71-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3aa71-110">Remarks</span></span>  
 <span data-ttu-id="3aa71-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="3aa71-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="3aa71-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aa71-112">Requirements</span></span>  
 <span data-ttu-id="3aa71-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3aa71-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3aa71-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3aa71-114">See Also</span></span>  
 [<span data-ttu-id="3aa71-115">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3aa71-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)