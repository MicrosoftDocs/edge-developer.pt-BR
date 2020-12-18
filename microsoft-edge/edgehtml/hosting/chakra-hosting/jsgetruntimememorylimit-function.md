---
description: Obtém o limite de memória atual para um tempo de execução.
title: Função JsGetRuntimeMemoryLimit | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryLimit
helpviewer_keywords:
- JsGetRuntimeMemoryLimit function
ms.assetid: ed81ca60-99fd-46b0-89ae-f6ac07926904
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ed04a0fb921d22eea17eaf86ef7a0152fbf2a1d0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231934"
---
# <span data-ttu-id="6ab67-103">Função JsGetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="6ab67-103">JsGetRuntimeMemoryLimit Function</span></span>

<span data-ttu-id="6ab67-104">Obtém o limite de memória atual para um tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="6ab67-104">Gets the current memory limit for a runtime.</span></span>  
  
## <span data-ttu-id="6ab67-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ab67-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryLimit  
);  
```  
  
#### <span data-ttu-id="6ab67-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ab67-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="6ab67-107">O tempo de execução cujo limite de memória deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="6ab67-107">The runtime whose memory limit is to be retrieved.</span></span>  
  
 `memoryLimit`  
 <span data-ttu-id="6ab67-108">O limite de memória atual do tempo de execução, em bytes ou-1, se nenhum limite tiver sido definido.</span><span class="sxs-lookup"><span data-stu-id="6ab67-108">The runtime's current memory limit, in bytes, or -1 if no limit has been set.</span></span>  
  
## <span data-ttu-id="6ab67-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6ab67-109">Return Value</span></span>  
 <span data-ttu-id="6ab67-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="6ab67-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6ab67-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ab67-111">Remarks</span></span>  
 <span data-ttu-id="6ab67-112">O limite de memória de um tempo de execução pode ser sempre recuperado, independentemente do tempo de execução estar ativo ou não em outro thread.</span><span class="sxs-lookup"><span data-stu-id="6ab67-112">The memory limit of a runtime can be always be retrieved, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="6ab67-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ab67-113">Requirements</span></span>  
 <span data-ttu-id="6ab67-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6ab67-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6ab67-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6ab67-115">See Also</span></span>  
 [<span data-ttu-id="6ab67-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6ab67-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
