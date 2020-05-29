---
description: Obtém a ID da propriedade associada ao símbolo.
title: Função JsGetPropertyIdFromSymbol | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 190fe4b9-352e-4b10-9d0e-6c6bbd6363e8
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 0d11dbaf25b85e2bcd85a0cf2bac1b499fd4fa3e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562179"
---
# <span data-ttu-id="cf3cc-103">Função JsGetPropertyIdFromSymbol</span><span class="sxs-lookup"><span data-stu-id="cf3cc-103">JsGetPropertyIdFromSymbol Function</span></span>
<span data-ttu-id="cf3cc-104">Obtém a ID da propriedade associada ao símbolo.</span><span class="sxs-lookup"><span data-stu-id="cf3cc-104">Gets the property ID associated with the symbol.</span></span>  
  
## <span data-ttu-id="cf3cc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf3cc-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromSymbol(  
   _In_ JsValueRef symbol,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="cf3cc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf3cc-106">Parameters</span></span>  
 `symbol`  
 <span data-ttu-id="cf3cc-107">O símbolo cuja ID de propriedade está sendo recuperada.</span><span class="sxs-lookup"><span data-stu-id="cf3cc-107">The symbol whose property ID is being retrieved.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="cf3cc-108">A ID da propriedade para o símbolo fornecido.</span><span class="sxs-lookup"><span data-stu-id="cf3cc-108">The property ID for the given symbol.</span></span>  
  
## <span data-ttu-id="cf3cc-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cf3cc-109">Return Value</span></span>  
 <span data-ttu-id="cf3cc-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="cf3cc-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="cf3cc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf3cc-111">Remarks</span></span>  
 <span data-ttu-id="cf3cc-112">As IDs de propriedade são específicas de um contexto e não podem ser usadas em contextos.</span><span class="sxs-lookup"><span data-stu-id="cf3cc-112">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="cf3cc-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="cf3cc-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="cf3cc-114">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cf3cc-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="cf3cc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf3cc-115">Requirements</span></span>  
 <span data-ttu-id="cf3cc-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cf3cc-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cf3cc-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cf3cc-117">See Also</span></span>  
 [<span data-ttu-id="cf3cc-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="cf3cc-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)