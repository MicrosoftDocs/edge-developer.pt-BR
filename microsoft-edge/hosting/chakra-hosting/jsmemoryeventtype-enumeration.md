---
description: Tipo de evento de retorno de chamada de atribuição.
title: Enumeração JsMemoryEventType | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsMemoryEventType
helpviewer_keywords:
- JsMemoryEventType enumeration
ms.assetid: b4b176b6-b536-472e-8999-95b681a1df55
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e9833777ed8fe5a19fd2a1487715296279f7351
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561018"
---
# <span data-ttu-id="5208f-103">Enumeração JsMemoryEventType</span><span class="sxs-lookup"><span data-stu-id="5208f-103">JsMemoryEventType Enumeration</span></span>
<span data-ttu-id="5208f-104">Tipo de evento de retorno de chamada de atribuição.</span><span class="sxs-lookup"><span data-stu-id="5208f-104">Allocation callback event type.</span></span>  
  
## <span data-ttu-id="5208f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5208f-105">Syntax</span></span>  
  
```cpp  
enum JsMemoryEventType;  
```  
  
## <span data-ttu-id="5208f-106">Parte</span><span class="sxs-lookup"><span data-stu-id="5208f-106">Members</span></span>  
  
### <span data-ttu-id="5208f-107">Valores</span><span class="sxs-lookup"><span data-stu-id="5208f-107">Values</span></span>  
  
|<span data-ttu-id="5208f-108">Nome</span><span class="sxs-lookup"><span data-stu-id="5208f-108">Name</span></span>|<span data-ttu-id="5208f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5208f-109">Description</span></span>|  
|----------|-----------------|  
|`JsMemoryAllocate`|<span data-ttu-id="5208f-110">Indica uma solicitação de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="5208f-110">Indicates a request for memory allocation.</span></span>|  
|`JsMemoryFailure`|<span data-ttu-id="5208f-111">Indica um evento de alocação com falha.</span><span class="sxs-lookup"><span data-stu-id="5208f-111">Indicates a failed allocation event.</span></span>|  
|`JsMemoryFree`|<span data-ttu-id="5208f-112">Indica um evento de liberação de memória.</span><span class="sxs-lookup"><span data-stu-id="5208f-112">Indicates a memory freeing event.</span></span>|  
  
## <span data-ttu-id="5208f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5208f-113">Requirements</span></span>  
 <span data-ttu-id="5208f-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5208f-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5208f-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5208f-115">See Also</span></span>  
 [<span data-ttu-id="5208f-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5208f-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)