---
description: Tipo de evento de retorno de chamada de atribuição.
title: Enumeração JsMemoryEventType | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsMemoryEventType
helpviewer_keywords:
- JsMemoryEventType enumeration
ms.assetid: b4b176b6-b536-472e-8999-95b681a1df55
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a28010f908285098cf652b497b6d6c272bc763fc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231231"
---
# <span data-ttu-id="acdef-103">Enumeração JsMemoryEventType</span><span class="sxs-lookup"><span data-stu-id="acdef-103">JsMemoryEventType Enumeration</span></span>

<span data-ttu-id="acdef-104">Tipo de evento de retorno de chamada de atribuição.</span><span class="sxs-lookup"><span data-stu-id="acdef-104">Allocation callback event type.</span></span>  
  
## <span data-ttu-id="acdef-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="acdef-105">Syntax</span></span>  
  
```cpp  
enum JsMemoryEventType;  
```  
  
## <span data-ttu-id="acdef-106">Parte</span><span class="sxs-lookup"><span data-stu-id="acdef-106">Members</span></span>  
  
### <span data-ttu-id="acdef-107">Valores</span><span class="sxs-lookup"><span data-stu-id="acdef-107">Values</span></span>  
  
|<span data-ttu-id="acdef-108">Nome</span><span class="sxs-lookup"><span data-stu-id="acdef-108">Name</span></span>|<span data-ttu-id="acdef-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="acdef-109">Description</span></span>|  
|----------|-----------------|  
|`JsMemoryAllocate`|<span data-ttu-id="acdef-110">Indica uma solicitação de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="acdef-110">Indicates a request for memory allocation.</span></span>|  
|`JsMemoryFailure`|<span data-ttu-id="acdef-111">Indica um evento de alocação com falha.</span><span class="sxs-lookup"><span data-stu-id="acdef-111">Indicates a failed allocation event.</span></span>|  
|`JsMemoryFree`|<span data-ttu-id="acdef-112">Indica um evento de liberação de memória.</span><span class="sxs-lookup"><span data-stu-id="acdef-112">Indicates a memory freeing event.</span></span>|  
  
## <span data-ttu-id="acdef-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acdef-113">Requirements</span></span>  
 <span data-ttu-id="acdef-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="acdef-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="acdef-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="acdef-115">See Also</span></span>  
 [<span data-ttu-id="acdef-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="acdef-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
