---
description: Define o valor no índice especificado de um objeto.
title: Função JsSetIndexedProperty | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetIndexedProperty
helpviewer_keywords:
- JsSetIndexedProperty function
ms.assetid: ccbc5bf4-d99b-485c-ab25-d2bd1ed2142e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 893849c42d9cbf0de160846d3397fcd5d7c77b7b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562107"
---
# <span data-ttu-id="33349-103">Função JsSetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="33349-103">JsSetIndexedProperty Function</span></span>
<span data-ttu-id="33349-104">Define o valor no índice especificado de um objeto.</span><span class="sxs-lookup"><span data-stu-id="33349-104">Set the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="33349-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33349-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _In_ JsValueRef value  
);  
```  
  
#### <span data-ttu-id="33349-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33349-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="33349-107">O objeto no qual operar.</span><span class="sxs-lookup"><span data-stu-id="33349-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="33349-108">O índice a ser definido.</span><span class="sxs-lookup"><span data-stu-id="33349-108">The index to set.</span></span>  
  
 `value`  
 <span data-ttu-id="33349-109">O valor a ser definido.</span><span class="sxs-lookup"><span data-stu-id="33349-109">The value to set.</span></span>  
  
## <span data-ttu-id="33349-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="33349-110">Return Value</span></span>  
 <span data-ttu-id="33349-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="33349-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="33349-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="33349-112">Remarks</span></span>  
 <span data-ttu-id="33349-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="33349-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="33349-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33349-114">Requirements</span></span>  
 <span data-ttu-id="33349-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="33349-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="33349-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="33349-116">See Also</span></span>  
 [<span data-ttu-id="33349-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="33349-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)