---
description: Rotina de retorno de chamada implementada pelo usuário para eventos de alocação de memória.
title: Typedef JsMemoryAllocationCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 22b5cc0fe5a2c8b49f71c91d28f95ba29af37849
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231422"
---
# <span data-ttu-id="bf0aa-103">Typedef JsMemoryAllocationCallback</span><span class="sxs-lookup"><span data-stu-id="bf0aa-103">JsMemoryAllocationCallback Typedef</span></span>

<span data-ttu-id="bf0aa-104">Rotina de retorno de chamada implementada pelo usuário para eventos de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="bf0aa-104">User implemented callback routine for memory allocation events.</span></span>  
  
## <span data-ttu-id="bf0aa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf0aa-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsMemoryAllocationCallback)(  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryEventType allocationEvent,  
   _In_ size_t allocationSize  
);  
```  
  
#### <span data-ttu-id="bf0aa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf0aa-106">Parameters</span></span>  
 <span data-ttu-id="bf0aa-107">callbackstate</span><span class="sxs-lookup"><span data-stu-id="bf0aa-107">callbackState</span></span>  
 <span data-ttu-id="bf0aa-108">O estado passado para JsSetRuntimeMemoryAllocationCallback.</span><span class="sxs-lookup"><span data-stu-id="bf0aa-108">The state passed to JsSetRuntimeMemoryAllocationCallback.</span></span>  
  
 <span data-ttu-id="bf0aa-109">allocationEvent</span><span class="sxs-lookup"><span data-stu-id="bf0aa-109">allocationEvent</span></span>  
 <span data-ttu-id="bf0aa-110">O tipo de evento de alocação de tipo.</span><span class="sxs-lookup"><span data-stu-id="bf0aa-110">The type of type allocation event.</span></span>  
  
 <span data-ttu-id="bf0aa-111">inlocatione</span><span class="sxs-lookup"><span data-stu-id="bf0aa-111">allocationSize</span></span>  
 <span data-ttu-id="bf0aa-112">O tamanho da alocação.</span><span class="sxs-lookup"><span data-stu-id="bf0aa-112">The size of the allocation.</span></span>  
  
## <span data-ttu-id="bf0aa-113">Valor da propriedade/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bf0aa-113">Property Value/Return Value</span></span>  
 <span data-ttu-id="bf0aa-114">Para o evento JsMemoryAllocate, retornar true permite que o tempo de execução continue com a alocação.</span><span class="sxs-lookup"><span data-stu-id="bf0aa-114">For the JsMemoryAllocate event, returning true allows the runtime to continue with allocation.</span></span> <span data-ttu-id="bf0aa-115">Retornar false indica que a solicitação de alocação foi rejeitada.</span><span class="sxs-lookup"><span data-stu-id="bf0aa-115">Returning false indicates the allocation request is rejected.</span></span> <span data-ttu-id="bf0aa-116">O valor de retorno é ignorado para outros eventos de alocação.</span><span class="sxs-lookup"><span data-stu-id="bf0aa-116">The return value is ignored for other allocation events.</span></span>  
  
## <span data-ttu-id="bf0aa-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf0aa-117">Remarks</span></span>  
 <span data-ttu-id="bf0aa-118">Use JsSetRuntimeMemoryAllocationCallback para registrar esse retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="bf0aa-118">Use JsSetRuntimeMemoryAllocationCallback to register this callback.</span></span>  
  
## <span data-ttu-id="bf0aa-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf0aa-119">Requirements</span></span>  
 <span data-ttu-id="bf0aa-120">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bf0aa-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bf0aa-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bf0aa-121">See Also</span></span>  
 [<span data-ttu-id="bf0aa-122">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bf0aa-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
