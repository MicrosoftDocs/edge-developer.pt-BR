---
description: Uma referência a um contexto de script.
title: Typedef JsContextRef | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 80e4b5034079f4f0d26da070bd209aa41bf3475f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561122"
---
# <span data-ttu-id="17cc7-103">Typedef JsContextRef</span><span class="sxs-lookup"><span data-stu-id="17cc7-103">JsContextRef Typedef</span></span>
<span data-ttu-id="17cc7-104">Uma referência a um contexto de script.</span><span class="sxs-lookup"><span data-stu-id="17cc7-104">A reference to a script context.</span></span>  
  
## <span data-ttu-id="17cc7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17cc7-105">Syntax</span></span>  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## <span data-ttu-id="17cc7-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="17cc7-106">Remarks</span></span>  
 <span data-ttu-id="17cc7-107">Cada contexto de script contém seu próprio objeto global, distinto do objeto global em outros contextos de script.</span><span class="sxs-lookup"><span data-stu-id="17cc7-107">Each script context contains its own global object, distinct from the global object in other script contexts.</span></span>  
  
 <span data-ttu-id="17cc7-108">Muitas APIs de hospedagem Chakra exigem um contexto de script "ativo", que pode ser definido usando `JsSetCurrentContext` .</span><span class="sxs-lookup"><span data-stu-id="17cc7-108">Many Chakra hosting APIs require an "active" script context, which can be set using `JsSetCurrentContext`.</span></span> <span data-ttu-id="17cc7-109">Chakra Hospedagem de APIs que exijam que um contexto atual seja definido notará que, explicitamente, em sua documentação.</span><span class="sxs-lookup"><span data-stu-id="17cc7-109">Chakra hosting APIs that require a current context to be set will note that explicitly in their documentation.</span></span>  
  
## <span data-ttu-id="17cc7-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17cc7-110">Requirements</span></span>  
 <span data-ttu-id="17cc7-111">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="17cc7-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="17cc7-112">Consulte também</span><span class="sxs-lookup"><span data-stu-id="17cc7-112">See Also</span></span>  
 [<span data-ttu-id="17cc7-113">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="17cc7-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)