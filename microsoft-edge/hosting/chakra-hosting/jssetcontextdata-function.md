---
description: Define os dados internos do JsrtContext.
title: Função JsSetContextData | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e874f500ca82328dddeaaa03a0b78a188b8fd241
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751930"
---
# <span data-ttu-id="0167c-103">Função JsSetContextData</span><span class="sxs-lookup"><span data-stu-id="0167c-103">JsSetContextData Function</span></span>
<span data-ttu-id="0167c-104">Define os dados internos do JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="0167c-104">Sets the internal data of JsrtContext.</span></span>  
  
## <span data-ttu-id="0167c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0167c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### <span data-ttu-id="0167c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0167c-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="0167c-107">O contexto para o qual definir os dados.</span><span class="sxs-lookup"><span data-stu-id="0167c-107">The context to set the data to.</span></span>  
  
 `data`  
 <span data-ttu-id="0167c-108">O ponteiro para os dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="0167c-108">The pointer to the data to be set.</span></span>  
  
## <span data-ttu-id="0167c-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0167c-109">Return Value</span></span>  
 <span data-ttu-id="0167c-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="0167c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0167c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0167c-111">Remarks</span></span>  
 <span data-ttu-id="0167c-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="0167c-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0167c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0167c-113">Requirements</span></span>  
 <span data-ttu-id="0167c-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0167c-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0167c-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0167c-115">See Also</span></span>  
 [<span data-ttu-id="0167c-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0167c-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)