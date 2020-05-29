---
description: Um retorno de chamada de função.
title: Typedef JsNativeFunction | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c0b73a11d3a0b2ed0867ef001f3c29c5643132a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561019"
---
# <span data-ttu-id="d593c-103">Typedef JsNativeFunction</span><span class="sxs-lookup"><span data-stu-id="d593c-103">JsNativeFunction Typedef</span></span>
<span data-ttu-id="d593c-104">Um retorno de chamada de função.</span><span class="sxs-lookup"><span data-stu-id="d593c-104">A function callback.</span></span>  
  
## <span data-ttu-id="d593c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d593c-105">Syntax</span></span>  
  
```cpp  
typedef _Ret_maybenull_ JsValueRef (CALLBACK * JsNativeFunction)(  
   _In_ JsValueRef callee,  
   _In_ bool isConstructCall,  
   _In_ JsValueRef *arguments,  
   _In_ unsigned short argumentCount  
);  
```  
  
#### <span data-ttu-id="d593c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d593c-106">Parameters</span></span>  
 <span data-ttu-id="d593c-107">destinatário</span><span class="sxs-lookup"><span data-stu-id="d593c-107">callee</span></span>  
 <span data-ttu-id="d593c-108">Um `Function` objeto que representa a função que está sendo invocada.</span><span class="sxs-lookup"><span data-stu-id="d593c-108">A `Function` object that represents the function being invoked.</span></span>  
  
 <span data-ttu-id="d593c-109">isConstructCall</span><span class="sxs-lookup"><span data-stu-id="d593c-109">isConstructCall</span></span>  
 <span data-ttu-id="d593c-110">Indica se esta é uma chamada regular ou ' nova '.</span><span class="sxs-lookup"><span data-stu-id="d593c-110">Indicates whether this is a regular call or a 'new' call.</span></span>  
  
 <span data-ttu-id="d593c-111">arguments</span><span class="sxs-lookup"><span data-stu-id="d593c-111">arguments</span></span>  
 <span data-ttu-id="d593c-112">Os argumentos para a chamada.</span><span class="sxs-lookup"><span data-stu-id="d593c-112">The arguments to the call.</span></span>  
  
 <span data-ttu-id="d593c-113">argumentCount</span><span class="sxs-lookup"><span data-stu-id="d593c-113">argumentCount</span></span>  
 <span data-ttu-id="d593c-114">O número de argumentos.</span><span class="sxs-lookup"><span data-stu-id="d593c-114">The number of arguments.</span></span>  
  
## <span data-ttu-id="d593c-115">Valor da propriedade/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d593c-115">Property Value/Return Value</span></span>  
 <span data-ttu-id="d593c-116">O resultado da chamada, se houver.</span><span class="sxs-lookup"><span data-stu-id="d593c-116">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="d593c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d593c-117">Requirements</span></span>  
 <span data-ttu-id="d593c-118">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d593c-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d593c-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d593c-119">See Also</span></span>  
 [<span data-ttu-id="d593c-120">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d593c-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)