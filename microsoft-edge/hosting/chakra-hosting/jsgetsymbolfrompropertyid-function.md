---
description: Obtém o símbolo associado à ID da propriedade.
title: Função JsGetSymbolFromPropertyId | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 0e822cb4-ba9e-44df-bf3a-fae97c354daa
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6902384772f29f80751660ce2d4a295d2ea620ab
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561037"
---
# <span data-ttu-id="c615a-103">Função JsGetSymbolFromPropertyId</span><span class="sxs-lookup"><span data-stu-id="c615a-103">JsGetSymbolFromPropertyId Function</span></span>
<span data-ttu-id="c615a-104">Obtém o símbolo associado à ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c615a-104">Gets the symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="c615a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c615a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetSymbolFromPropertyId(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *symbol  
);  
```  
  
#### <span data-ttu-id="c615a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c615a-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="c615a-107">A ID da propriedade para obter o símbolo de.</span><span class="sxs-lookup"><span data-stu-id="c615a-107">The property ID to get the symbol of.</span></span>  
  
 `symbol`  
 <span data-ttu-id="c615a-108">O símbolo associado à identificação da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c615a-108">The symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="c615a-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c615a-109">Return Value</span></span>  
 <span data-ttu-id="c615a-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="c615a-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c615a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c615a-111">Remarks</span></span>  
 <span data-ttu-id="c615a-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="c615a-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="c615a-113">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c615a-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="c615a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c615a-114">Requirements</span></span>  
 <span data-ttu-id="c615a-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c615a-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c615a-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c615a-116">See Also</span></span>  
 [<span data-ttu-id="c615a-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c615a-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)