---
description: Obtém o tipo de propriedade.
title: Função JsGetPropertyIdType | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2b6e85ad-c630-4a07-a759-3b344d06faaa
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 93ee11bf74014361c89aa93bbb58361b426f573f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231807"
---
# <span data-ttu-id="22a89-103">Função JsGetPropertyIdType</span><span class="sxs-lookup"><span data-stu-id="22a89-103">JsGetPropertyIdType Function</span></span>

<span data-ttu-id="22a89-104">Obtém o tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="22a89-104">Gets the type of property.</span></span>  
  
## <span data-ttu-id="22a89-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22a89-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdType(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsPropertyIdType* propertyIdType  
);  
```  
  
#### <span data-ttu-id="22a89-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22a89-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="22a89-107">A ID da propriedade para obter o tipo.</span><span class="sxs-lookup"><span data-stu-id="22a89-107">The property ID to get the type of.</span></span>  
  
 `propertyIdType`  
 <span data-ttu-id="22a89-108">A `JsPropertyIdType` ID da propriedade fornecida.</span><span class="sxs-lookup"><span data-stu-id="22a89-108">The `JsPropertyIdType` of the given property ID.</span></span>  
  
## <span data-ttu-id="22a89-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="22a89-109">Return Value</span></span>  
 <span data-ttu-id="22a89-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="22a89-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="22a89-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="22a89-111">Remarks</span></span>  
 <span data-ttu-id="22a89-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="22a89-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="22a89-113">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="22a89-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="22a89-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22a89-114">Requirements</span></span>  
 <span data-ttu-id="22a89-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="22a89-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="22a89-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="22a89-116">See Also</span></span>  
 [<span data-ttu-id="22a89-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="22a89-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
