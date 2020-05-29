---
description: Obtém o uso de memória atual para um tempo de execução.
title: Função JsGetRuntimeMemoryUsage | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryUsage
helpviewer_keywords:
- JsGetRuntimeMemoryUsage function
ms.assetid: b9bd4146-bfbc-4cb1-a0e9-a0ded7fb09bd
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9ec8472132b4c50b279ee95f36995bf46c0e29e5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561038"
---
# <span data-ttu-id="95c68-103">Função JsGetRuntimeMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="95c68-103">JsGetRuntimeMemoryUsage Function</span></span>
<span data-ttu-id="95c68-104">Obtém o uso de memória atual para um tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="95c68-104">Gets the current memory usage for a runtime.</span></span>  
  
## <span data-ttu-id="95c68-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95c68-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryUsage(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryUsage  
);  
```  
  
#### <span data-ttu-id="95c68-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95c68-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="95c68-107">O tempo de execução cujo uso da memória deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="95c68-107">The runtime whose memory usage is to be retrieved.</span></span>  
  
 `memoryUsage`  
 <span data-ttu-id="95c68-108">O uso atual da memória do tempo de execução, em bytes.</span><span class="sxs-lookup"><span data-stu-id="95c68-108">The runtime's current memory usage, in bytes.</span></span>  
  
## <span data-ttu-id="95c68-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="95c68-109">Return Value</span></span>  
 <span data-ttu-id="95c68-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="95c68-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="95c68-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="95c68-111">Remarks</span></span>  
 <span data-ttu-id="95c68-112">O uso da memória pode sempre ser recuperado, independentemente do tempo de execução estar ativo ou não em outro thread.</span><span class="sxs-lookup"><span data-stu-id="95c68-112">Memory usage can be always be retrieved, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="95c68-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95c68-113">Requirements</span></span>  
 <span data-ttu-id="95c68-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="95c68-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="95c68-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="95c68-115">See Also</span></span>  
 [<span data-ttu-id="95c68-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="95c68-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)