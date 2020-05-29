---
description: Determina se um objeto é um objeto externo.
title: Função JsHasExternalData | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasExternalData
helpviewer_keywords:
- JsHasExternalData function
ms.assetid: a077e3ac-4f6f-4d94-8398-f1b5cc4c18e0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 0ca86df09264eb82dac2e928874ca15edd2c8c8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562166"
---
# <span data-ttu-id="48238-103">Função JsHasExternalData</span><span class="sxs-lookup"><span data-stu-id="48238-103">JsHasExternalData Function</span></span>
<span data-ttu-id="48238-104">Determina se um objeto é um objeto externo.</span><span class="sxs-lookup"><span data-stu-id="48238-104">Determines whether an object is an external object.</span></span>  
  
## <span data-ttu-id="48238-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48238-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="48238-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48238-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="48238-107">O objeto.</span><span class="sxs-lookup"><span data-stu-id="48238-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="48238-108">Se o objeto é um objeto externo.</span><span class="sxs-lookup"><span data-stu-id="48238-108">Whether the object is an external object.</span></span>  
  
## <span data-ttu-id="48238-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="48238-109">Return Value</span></span>  
 <span data-ttu-id="48238-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="48238-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="48238-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="48238-111">Remarks</span></span>  
 <span data-ttu-id="48238-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="48238-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="48238-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48238-113">Requirements</span></span>  
 <span data-ttu-id="48238-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="48238-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="48238-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="48238-115">See Also</span></span>  
 [<span data-ttu-id="48238-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="48238-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)