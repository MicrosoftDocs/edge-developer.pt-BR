---
description: Um retorno de chamada chamado antes de coletar um objeto.
title: Typedef JsObjectBeforeCollectCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: f21a064a-579f-44cb-9d21-76b62e8c18f5
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4c24385ec5e15919719ffb0ae71c8adf39c1724c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231761"
---
# <span data-ttu-id="e643b-103">Typedef JsObjectBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="e643b-103">JsObjectBeforeCollectCallback Typedef</span></span>

<span data-ttu-id="e643b-104">Um retorno de chamada chamado antes de coletar um objeto.</span><span class="sxs-lookup"><span data-stu-id="e643b-104">A callback called before collecting an object.</span></span>  
  
## <span data-ttu-id="e643b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e643b-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsObjectBeforeCollectCallback)(  
  _In_ JsRef ref,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="e643b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e643b-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="e643b-107">O objeto a ser coletado.</span><span class="sxs-lookup"><span data-stu-id="e643b-107">The object to be collected.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="e643b-108">O estado passado para `JsSetObjectBeforeCollectCallback` .</span><span class="sxs-lookup"><span data-stu-id="e643b-108">The state passed to `JsSetObjectBeforeCollectCallback`.</span></span>  
  
## <span data-ttu-id="e643b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="e643b-109">Remarks</span></span>  
 <span data-ttu-id="e643b-110">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="e643b-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="e643b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e643b-111">Requirements</span></span>  
 <span data-ttu-id="e643b-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e643b-112">jsrt.h</span></span>  
  
## <span data-ttu-id="e643b-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e643b-113">See Also</span></span>  
 [<span data-ttu-id="e643b-114">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e643b-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
