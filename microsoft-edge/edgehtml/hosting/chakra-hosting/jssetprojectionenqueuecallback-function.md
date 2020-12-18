---
description: Define o retorno de chamada a ser usado para invocar uma conclusão de projeção para o thread dos chamadores obrigatórios.
title: Função JsSetProjectionEnqueueCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7dfedfeb1df5a97159a211795a2dd072d239bb35
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231405"
---
# <span data-ttu-id="7c8e1-103">Função JsSetProjectionEnqueueCallback</span><span class="sxs-lookup"><span data-stu-id="7c8e1-103">JsSetProjectionEnqueueCallback Function</span></span>

<span data-ttu-id="7c8e1-104">Define o retorno de chamada a ser usado para invocar uma conclusão de projeção para o thread dos chamadores obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="7c8e1-104">Sets the callback to be used in order to invoke a projection completion back to the callers required thread.</span></span>  
  
## <span data-ttu-id="7c8e1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c8e1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProjectionEnqueueCallback(  
   _In_ JsProjectionEnqueueCallback projectionEnqueueCallback,  
   _In_opt_ void *projectionEnqueueContext);  
  
```  
  
#### <span data-ttu-id="7c8e1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c8e1-106">Parameters</span></span>  
 `projectionEnqueueContext`  
 <span data-ttu-id="7c8e1-107">O retorno de chamada que será invocado sempre que uma conclusão de projeção ocorrer em um thread em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7c8e1-107">The callback that will be invoked any time a projection completion occurs on a background thread.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="7c8e1-108">O contexto do aplicativo fornecido para `projectionEnqueueContext` .</span><span class="sxs-lookup"><span data-stu-id="7c8e1-108">The application context provided to `projectionEnqueueContext`.</span></span>  
  
## <span data-ttu-id="7c8e1-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7c8e1-109">Return Value</span></span>  
 <span data-ttu-id="7c8e1-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="7c8e1-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7c8e1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c8e1-111">Remarks</span></span>  
 <span data-ttu-id="7c8e1-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="7c8e1-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="7c8e1-113">A chamada deve ser proveniente de um outro apartment COM ou de um thread diferente no mesmo MTA.</span><span class="sxs-lookup"><span data-stu-id="7c8e1-113">The call should be coming from a different COM apartment or from a different thread in the same MTA.</span></span>  
  
 <span data-ttu-id="7c8e1-114">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="7c8e1-114">This API is supported only in EdgeHTML mode.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="7c8e1-115">No momento, não há suporte para PInvoke para essa API.</span><span class="sxs-lookup"><span data-stu-id="7c8e1-115">PInvoke is not currently supported for this API.</span></span>  
  
## <span data-ttu-id="7c8e1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c8e1-116">Requirements</span></span>  
 <span data-ttu-id="7c8e1-117">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7c8e1-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7c8e1-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7c8e1-118">See Also</span></span>  
 [<span data-ttu-id="7c8e1-119">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7c8e1-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
