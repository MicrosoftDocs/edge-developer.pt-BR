---
description: Obtém o tipo de JavaScript de um JsValueRef.
title: Função JsGetValueType | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetValueType
helpviewer_keywords:
- JsGetValueType function
ms.assetid: f403cf7c-c8c0-4a17-bfa9-0302d00e760e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b2e9937ca13bf2a680a4a33c07020d06c53efdf3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231290"
---
# <span data-ttu-id="fffd3-103">Função JsGetValueType</span><span class="sxs-lookup"><span data-stu-id="fffd3-103">JsGetValueType Function</span></span>

<span data-ttu-id="fffd3-104">Obtém o tipo de JavaScript de um JsValueRef.</span><span class="sxs-lookup"><span data-stu-id="fffd3-104">Gets the JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="fffd3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fffd3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetValueType(  
   _In_ JsValueRef value,  
   _Out_ JsValueType *type  
);  
```  
  
#### <span data-ttu-id="fffd3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fffd3-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="fffd3-107">O valor cujo tipo deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="fffd3-107">The value whose type is to be returned.</span></span>  
  
 `type`  
 <span data-ttu-id="fffd3-108">O tipo do valor.</span><span class="sxs-lookup"><span data-stu-id="fffd3-108">The type of the value.</span></span>  
  
## <span data-ttu-id="fffd3-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fffd3-109">Return Value</span></span>  
 <span data-ttu-id="fffd3-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="fffd3-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fffd3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fffd3-111">Remarks</span></span>  
 <span data-ttu-id="fffd3-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="fffd3-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="fffd3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fffd3-113">Requirements</span></span>  
 <span data-ttu-id="fffd3-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fffd3-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fffd3-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fffd3-115">See Also</span></span>  
 [<span data-ttu-id="fffd3-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fffd3-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
