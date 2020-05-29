---
description: Converte o valor em booliano usando a semântica JavaScript padrão.
title: Função JsConvertValueToBoolean | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToBoolean
helpviewer_keywords:
- JsConvertValueToBoolean function
ms.assetid: 7298ec72-a388-4334-b81b-1691ab4cecf0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 861871a030d5a47621ccaf40b6cd332f42a06583
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561118"
---
# <span data-ttu-id="089b4-103">Função JsConvertValueToBoolean</span><span class="sxs-lookup"><span data-stu-id="089b4-103">JsConvertValueToBoolean Function</span></span>
<span data-ttu-id="089b4-104">Converte o valor em booliano usando a semântica JavaScript padrão.</span><span class="sxs-lookup"><span data-stu-id="089b4-104">Converts the value to Boolean using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="089b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="089b4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToBoolean(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="089b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="089b4-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="089b4-107">O valor a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="089b4-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="089b4-108">O valor convertido.</span><span class="sxs-lookup"><span data-stu-id="089b4-108">The converted value.</span></span>  
  
## <span data-ttu-id="089b4-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="089b4-109">Return Value</span></span>  
 <span data-ttu-id="089b4-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="089b4-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="089b4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="089b4-111">Remarks</span></span>  
 <span data-ttu-id="089b4-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="089b4-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="089b4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="089b4-113">Requirements</span></span>  
 <span data-ttu-id="089b4-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="089b4-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="089b4-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="089b4-115">See Also</span></span>  
 [<span data-ttu-id="089b4-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="089b4-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)