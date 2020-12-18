---
description: Uma referência a um contexto de script.
title: Typedef JsContextRef | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c8a8fcbd67afb150d682cfc19321f0f13acfe3a6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231443"
---
# <span data-ttu-id="1ad5d-103">Typedef JsContextRef</span><span class="sxs-lookup"><span data-stu-id="1ad5d-103">JsContextRef Typedef</span></span>

<span data-ttu-id="1ad5d-104">Uma referência a um contexto de script.</span><span class="sxs-lookup"><span data-stu-id="1ad5d-104">A reference to a script context.</span></span>  
  
## <span data-ttu-id="1ad5d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ad5d-105">Syntax</span></span>  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## <span data-ttu-id="1ad5d-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ad5d-106">Remarks</span></span>  
 <span data-ttu-id="1ad5d-107">Cada contexto de script contém seu próprio objeto global, distinto do objeto global em outros contextos de script.</span><span class="sxs-lookup"><span data-stu-id="1ad5d-107">Each script context contains its own global object, distinct from the global object in other script contexts.</span></span>  
  
 <span data-ttu-id="1ad5d-108">Muitas APIs de hospedagem Chakra exigem um contexto de script "ativo", que pode ser definido usando `JsSetCurrentContext` .</span><span class="sxs-lookup"><span data-stu-id="1ad5d-108">Many Chakra hosting APIs require an "active" script context, which can be set using `JsSetCurrentContext`.</span></span> <span data-ttu-id="1ad5d-109">Chakra Hospedagem de APIs que exijam que um contexto atual seja definido notará que, explicitamente, em sua documentação.</span><span class="sxs-lookup"><span data-stu-id="1ad5d-109">Chakra hosting APIs that require a current context to be set will note that explicitly in their documentation.</span></span>  
  
## <span data-ttu-id="1ad5d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ad5d-110">Requirements</span></span>  
 <span data-ttu-id="1ad5d-111">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1ad5d-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1ad5d-112">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1ad5d-112">See Also</span></span>  
 [<span data-ttu-id="1ad5d-113">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1ad5d-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
