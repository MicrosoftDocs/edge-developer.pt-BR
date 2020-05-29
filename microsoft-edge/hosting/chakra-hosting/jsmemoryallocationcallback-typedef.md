---
description: Rotina de retorno de chamada implementada pelo usuário para eventos de alocação de memória.
title: Typedef JsMemoryAllocationCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b11b3d076c01dbfcae190fd665528323d6f8b987
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561021"
---
# <span data-ttu-id="9bb4a-103">Typedef JsMemoryAllocationCallback</span><span class="sxs-lookup"><span data-stu-id="9bb4a-103">JsMemoryAllocationCallback Typedef</span></span>
<span data-ttu-id="9bb4a-104">Rotina de retorno de chamada implementada pelo usuário para eventos de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="9bb4a-104">User implemented callback routine for memory allocation events.</span></span>  
  
## <span data-ttu-id="9bb4a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bb4a-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsMemoryAllocationCallback)(  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryEventType allocationEvent,  
   _In_ size_t allocationSize  
);  
```  
  
#### <span data-ttu-id="9bb4a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bb4a-106">Parameters</span></span>  
 <span data-ttu-id="9bb4a-107">callbackstate</span><span class="sxs-lookup"><span data-stu-id="9bb4a-107">callbackState</span></span>  
 <span data-ttu-id="9bb4a-108">O estado passado para JsSetRuntimeMemoryAllocationCallback.</span><span class="sxs-lookup"><span data-stu-id="9bb4a-108">The state passed to JsSetRuntimeMemoryAllocationCallback.</span></span>  
  
 <span data-ttu-id="9bb4a-109">allocationEvent</span><span class="sxs-lookup"><span data-stu-id="9bb4a-109">allocationEvent</span></span>  
 <span data-ttu-id="9bb4a-110">O tipo de evento de alocação de tipo.</span><span class="sxs-lookup"><span data-stu-id="9bb4a-110">The type of type allocation event.</span></span>  
  
 <span data-ttu-id="9bb4a-111">inlocatione</span><span class="sxs-lookup"><span data-stu-id="9bb4a-111">allocationSize</span></span>  
 <span data-ttu-id="9bb4a-112">O tamanho da alocação.</span><span class="sxs-lookup"><span data-stu-id="9bb4a-112">The size of the allocation.</span></span>  
  
## <span data-ttu-id="9bb4a-113">Valor da propriedade/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9bb4a-113">Property Value/Return Value</span></span>  
 <span data-ttu-id="9bb4a-114">Para o evento JsMemoryAllocate, retornar true permite que o tempo de execução continue com a alocação.</span><span class="sxs-lookup"><span data-stu-id="9bb4a-114">For the JsMemoryAllocate event, returning true allows the runtime to continue with allocation.</span></span> <span data-ttu-id="9bb4a-115">Retornar false indica que a solicitação de alocação foi rejeitada.</span><span class="sxs-lookup"><span data-stu-id="9bb4a-115">Returning false indicates the allocation request is rejected.</span></span> <span data-ttu-id="9bb4a-116">O valor de retorno é ignorado para outros eventos de alocação.</span><span class="sxs-lookup"><span data-stu-id="9bb4a-116">The return value is ignored for other allocation events.</span></span>  
  
## <span data-ttu-id="9bb4a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="9bb4a-117">Remarks</span></span>  
 <span data-ttu-id="9bb4a-118">Use JsSetRuntimeMemoryAllocationCallback para registrar esse retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="9bb4a-118">Use JsSetRuntimeMemoryAllocationCallback to register this callback.</span></span>  
  
## <span data-ttu-id="9bb4a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bb4a-119">Requirements</span></span>  
 <span data-ttu-id="9bb4a-120">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9bb4a-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9bb4a-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9bb4a-121">See Also</span></span>  
 [<span data-ttu-id="9bb4a-122">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9bb4a-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)