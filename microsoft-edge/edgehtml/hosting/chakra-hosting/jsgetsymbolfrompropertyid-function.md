---
description: Obtém o símbolo associado à ID da propriedade.
title: Função JsGetSymbolFromPropertyId | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0e822cb4-ba9e-44df-bf3a-fae97c354daa
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 472253aea228ca0374c42d99710a7a7ab528184c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231991"
---
# <span data-ttu-id="76d91-103">Função JsGetSymbolFromPropertyId</span><span class="sxs-lookup"><span data-stu-id="76d91-103">JsGetSymbolFromPropertyId Function</span></span>

<span data-ttu-id="76d91-104">Obtém o símbolo associado à ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="76d91-104">Gets the symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="76d91-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76d91-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetSymbolFromPropertyId(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *symbol  
);  
```  
  
#### <span data-ttu-id="76d91-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76d91-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="76d91-107">A ID da propriedade para obter o símbolo de.</span><span class="sxs-lookup"><span data-stu-id="76d91-107">The property ID to get the symbol of.</span></span>  
  
 `symbol`  
 <span data-ttu-id="76d91-108">O símbolo associado à identificação da propriedade.</span><span class="sxs-lookup"><span data-stu-id="76d91-108">The symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="76d91-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="76d91-109">Return Value</span></span>  
 <span data-ttu-id="76d91-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="76d91-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="76d91-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="76d91-111">Remarks</span></span>  
 <span data-ttu-id="76d91-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="76d91-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="76d91-113">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76d91-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="76d91-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76d91-114">Requirements</span></span>  
 <span data-ttu-id="76d91-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="76d91-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="76d91-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="76d91-116">See Also</span></span>  
 [<span data-ttu-id="76d91-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="76d91-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
