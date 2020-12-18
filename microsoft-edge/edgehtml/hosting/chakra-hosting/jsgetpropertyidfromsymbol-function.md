---
description: Obtém a ID da propriedade associada ao símbolo.
title: Função JsGetPropertyIdFromSymbol | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 190fe4b9-352e-4b10-9d0e-6c6bbd6363e8
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d97f1fb517164d692cdd010f899dc40d2e3596ed
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231808"
---
# <span data-ttu-id="57092-103">Função JsGetPropertyIdFromSymbol</span><span class="sxs-lookup"><span data-stu-id="57092-103">JsGetPropertyIdFromSymbol Function</span></span>

<span data-ttu-id="57092-104">Obtém a ID da propriedade associada ao símbolo.</span><span class="sxs-lookup"><span data-stu-id="57092-104">Gets the property ID associated with the symbol.</span></span>  
  
## <span data-ttu-id="57092-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57092-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromSymbol(  
   _In_ JsValueRef symbol,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="57092-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57092-106">Parameters</span></span>  
 `symbol`  
 <span data-ttu-id="57092-107">O símbolo cuja ID de propriedade está sendo recuperada.</span><span class="sxs-lookup"><span data-stu-id="57092-107">The symbol whose property ID is being retrieved.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="57092-108">A ID da propriedade para o símbolo fornecido.</span><span class="sxs-lookup"><span data-stu-id="57092-108">The property ID for the given symbol.</span></span>  
  
## <span data-ttu-id="57092-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="57092-109">Return Value</span></span>  
 <span data-ttu-id="57092-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="57092-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="57092-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="57092-111">Remarks</span></span>  
 <span data-ttu-id="57092-112">As IDs de propriedade são específicas de um contexto e não podem ser usadas em contextos.</span><span class="sxs-lookup"><span data-stu-id="57092-112">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="57092-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="57092-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="57092-114">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="57092-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="57092-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57092-115">Requirements</span></span>  
 <span data-ttu-id="57092-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="57092-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="57092-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="57092-117">See Also</span></span>  
 [<span data-ttu-id="57092-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="57092-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
