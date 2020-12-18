---
description: Recupera o `bool` valor de um valor booliano.
title: Função JsBooleanToBool | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsBooleanToBool
helpviewer_keywords:
- JsBooleanToBool function
ms.assetid: ab16ac71-fe47-475d-a7ee-46e4643dee60
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 36bf2dc32b94466d8cdea37886e86a42c4ec01d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231438"
---
# <span data-ttu-id="28199-103">Função JsBooleanToBool</span><span class="sxs-lookup"><span data-stu-id="28199-103">JsBooleanToBool Function</span></span>

<span data-ttu-id="28199-104">Recupera o `bool` valor de um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="28199-104">Retrieves the `bool` value of a Boolean value.</span></span>  
  
## <span data-ttu-id="28199-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28199-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsBooleanToBool(  
   _In_ JsValueRef value,  
   _Out_ bool *boolValue  
);  
```  
  
#### <span data-ttu-id="28199-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28199-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="28199-107">O valor a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="28199-107">The value to be converted.</span></span>  
  
 `boolValue`  
 <span data-ttu-id="28199-108">O valor convertido.</span><span class="sxs-lookup"><span data-stu-id="28199-108">The converted value.</span></span>  
  
## <span data-ttu-id="28199-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="28199-109">Return Value</span></span>  
 <span data-ttu-id="28199-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="28199-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="28199-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="28199-111">Remarks</span></span>  
 <span data-ttu-id="28199-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="28199-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="28199-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28199-113">Requirements</span></span>  
 <span data-ttu-id="28199-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="28199-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="28199-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="28199-115">See Also</span></span>  
 [<span data-ttu-id="28199-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="28199-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
