---
description: Um retorno de chamada de função.
title: Typedef JsNativeFunction | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 891fe55f776e8519a5d3c187104b2bc326336482
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231245"
---
# <span data-ttu-id="6f7bc-103">Typedef JsNativeFunction </span><span class="sxs-lookup"><span data-stu-id="6f7bc-103">JsNativeFunction Typedef</span></span>

<span data-ttu-id="6f7bc-104">Um retorno de chamada de função.</span><span class="sxs-lookup"><span data-stu-id="6f7bc-104">A function callback.</span></span>  
  
## <span data-ttu-id="6f7bc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f7bc-105">Syntax</span></span>  
  
```cpp  
typedef _Ret_maybenull_ JsValueRef (CALLBACK * JsNativeFunction)(  
   _In_ JsValueRef callee,  
   _In_ bool isConstructCall,  
   _In_ JsValueRef *arguments,  
   _In_ unsigned short argumentCount  
);  
```  
  
#### <span data-ttu-id="6f7bc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f7bc-106">Parameters</span></span>  
 <span data-ttu-id="6f7bc-107">destinatário</span><span class="sxs-lookup"><span data-stu-id="6f7bc-107">callee</span></span>  
 <span data-ttu-id="6f7bc-108">Um `Function` objeto que representa a função que está sendo invocada.</span><span class="sxs-lookup"><span data-stu-id="6f7bc-108">A `Function` object that represents the function being invoked.</span></span>  
  
 <span data-ttu-id="6f7bc-109">isConstructCall</span><span class="sxs-lookup"><span data-stu-id="6f7bc-109">isConstructCall</span></span>  
 <span data-ttu-id="6f7bc-110">Indica se esta é uma chamada regular ou ' nova '.</span><span class="sxs-lookup"><span data-stu-id="6f7bc-110">Indicates whether this is a regular call or a 'new' call.</span></span>  
  
 <span data-ttu-id="6f7bc-111">arguments</span><span class="sxs-lookup"><span data-stu-id="6f7bc-111">arguments</span></span>  
 <span data-ttu-id="6f7bc-112">Os argumentos para a chamada.</span><span class="sxs-lookup"><span data-stu-id="6f7bc-112">The arguments to the call.</span></span>  
  
 <span data-ttu-id="6f7bc-113">argumentCount</span><span class="sxs-lookup"><span data-stu-id="6f7bc-113">argumentCount</span></span>  
 <span data-ttu-id="6f7bc-114">O número de argumentos.</span><span class="sxs-lookup"><span data-stu-id="6f7bc-114">The number of arguments.</span></span>  
  
## <span data-ttu-id="6f7bc-115">Valor da propriedade/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6f7bc-115">Property Value/Return Value</span></span>  
 <span data-ttu-id="6f7bc-116">O resultado da chamada, se houver.</span><span class="sxs-lookup"><span data-stu-id="6f7bc-116">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="6f7bc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f7bc-117">Requirements</span></span>  
 <span data-ttu-id="6f7bc-118">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6f7bc-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6f7bc-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6f7bc-119">See Also</span></span>  
 [<span data-ttu-id="6f7bc-120">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6f7bc-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
