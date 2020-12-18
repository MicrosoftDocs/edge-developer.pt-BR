---
description: Obtém o uso de memória atual para um tempo de execução.
title: Função JsGetRuntimeMemoryUsage | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryUsage
helpviewer_keywords:
- JsGetRuntimeMemoryUsage function
ms.assetid: b9bd4146-bfbc-4cb1-a0e9-a0ded7fb09bd
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a9c8d59e8cf73ad178f539f2f9f0ed191ceb47fd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231995"
---
# <span data-ttu-id="bbc14-103">Função JsGetRuntimeMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="bbc14-103">JsGetRuntimeMemoryUsage Function</span></span>

<span data-ttu-id="bbc14-104">Obtém o uso de memória atual para um tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="bbc14-104">Gets the current memory usage for a runtime.</span></span>  
  
## <span data-ttu-id="bbc14-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbc14-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryUsage(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryUsage  
);  
```  
  
#### <span data-ttu-id="bbc14-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbc14-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="bbc14-107">O tempo de execução cujo uso da memória deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="bbc14-107">The runtime whose memory usage is to be retrieved.</span></span>  
  
 `memoryUsage`  
 <span data-ttu-id="bbc14-108">O uso atual da memória do tempo de execução, em bytes.</span><span class="sxs-lookup"><span data-stu-id="bbc14-108">The runtime's current memory usage, in bytes.</span></span>  
  
## <span data-ttu-id="bbc14-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bbc14-109">Return Value</span></span>  
 <span data-ttu-id="bbc14-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="bbc14-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bbc14-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbc14-111">Remarks</span></span>  
 <span data-ttu-id="bbc14-112">O uso da memória pode sempre ser recuperado, independentemente do tempo de execução estar ativo ou não em outro thread.</span><span class="sxs-lookup"><span data-stu-id="bbc14-112">Memory usage can be always be retrieved, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="bbc14-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbc14-113">Requirements</span></span>  
 <span data-ttu-id="bbc14-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bbc14-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bbc14-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bbc14-115">See Also</span></span>  
 [<span data-ttu-id="bbc14-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bbc14-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
