---
description: Define os dados internos do JsrtContext.
title: Função JsSetContextData | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cac404b9e79bafb5a8eafb47e893dbdf38a02405
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231743"
---
# <span data-ttu-id="2b45b-103">Função JsSetContextData</span><span class="sxs-lookup"><span data-stu-id="2b45b-103">JsSetContextData Function</span></span>

<span data-ttu-id="2b45b-104">Define os dados internos do JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="2b45b-104">Sets the internal data of JsrtContext.</span></span>  
  
## <span data-ttu-id="2b45b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b45b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### <span data-ttu-id="2b45b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b45b-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="2b45b-107">O contexto para o qual definir os dados.</span><span class="sxs-lookup"><span data-stu-id="2b45b-107">The context to set the data to.</span></span>  
  
 `data`  
 <span data-ttu-id="2b45b-108">O ponteiro para os dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="2b45b-108">The pointer to the data to be set.</span></span>  
  
## <span data-ttu-id="2b45b-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2b45b-109">Return Value</span></span>  
 <span data-ttu-id="2b45b-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="2b45b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2b45b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b45b-111">Remarks</span></span>  
 <span data-ttu-id="2b45b-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="2b45b-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="2b45b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b45b-113">Requirements</span></span>  
 <span data-ttu-id="2b45b-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2b45b-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2b45b-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2b45b-115">See Also</span></span>  
 [<span data-ttu-id="2b45b-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2b45b-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
