---
description: Converte o valor em booliano usando a semântica JavaScript padrão.
title: Função JsConvertValueToBoolean | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToBoolean
helpviewer_keywords:
- JsConvertValueToBoolean function
ms.assetid: 7298ec72-a388-4334-b81b-1691ab4cecf0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d2e109690fc8a7a98a1ecb84d6f5abf6a646162b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231441"
---
# <span data-ttu-id="86c60-103">Função JsConvertValueToBoolean</span><span class="sxs-lookup"><span data-stu-id="86c60-103">JsConvertValueToBoolean Function</span></span>

<span data-ttu-id="86c60-104">Converte o valor em booliano usando a semântica JavaScript padrão.</span><span class="sxs-lookup"><span data-stu-id="86c60-104">Converts the value to Boolean using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="86c60-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86c60-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToBoolean(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="86c60-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86c60-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="86c60-107">O valor a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="86c60-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="86c60-108">O valor convertido.</span><span class="sxs-lookup"><span data-stu-id="86c60-108">The converted value.</span></span>  
  
## <span data-ttu-id="86c60-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="86c60-109">Return Value</span></span>  
 <span data-ttu-id="86c60-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="86c60-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="86c60-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="86c60-111">Remarks</span></span>  
 <span data-ttu-id="86c60-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="86c60-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="86c60-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86c60-113">Requirements</span></span>  
 <span data-ttu-id="86c60-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="86c60-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="86c60-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="86c60-115">See Also</span></span>  
 [<span data-ttu-id="86c60-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="86c60-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
