---
description: Define uma função de retorno de chamada de continuação Promise que é chamada pelo contexto quando uma tarefa precisa ser colocada em fila para execução futura.
title: Função JsSetPromiseContinuationCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6ef0faf4-1500-4bd9-aeca-c208492af8ea
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da928431f05831c95d5bc116dbd129de9cb5f3b4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231660"
---
# <span data-ttu-id="e6aa2-103">Função JsSetPromiseContinuationCallback</span><span class="sxs-lookup"><span data-stu-id="e6aa2-103">JsSetPromiseContinuationCallback Function</span></span>

<span data-ttu-id="e6aa2-104">Define uma função de retorno de chamada de continuação Promise que é chamada pelo contexto quando uma tarefa precisa ser colocada em fila para execução futura.</span><span class="sxs-lookup"><span data-stu-id="e6aa2-104">Sets a promise continuation callback function that is called by the context when a task needs to be queued for future execution.</span></span>  
  
## <span data-ttu-id="e6aa2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6aa2-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPromiseContinuationCallback(  
   _In_ JsPromiseContinuationCallback promiseContinuationCallback,  
   _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="e6aa2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6aa2-106">Parameters</span></span>  
 `promiseContinuationCallback`  
 <span data-ttu-id="e6aa2-107">A função de retorno de chamada sendo definida.</span><span class="sxs-lookup"><span data-stu-id="e6aa2-107">The callback function being set.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="e6aa2-108">Estado fornecido pelo usuário que será devolvido ao retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e6aa2-108">User provided state that will be passed back to the callback.</span></span>  
  
## <span data-ttu-id="e6aa2-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e6aa2-109">Return Value</span></span>  
 <span data-ttu-id="e6aa2-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="e6aa2-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e6aa2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6aa2-111">Remarks</span></span>  
 <span data-ttu-id="e6aa2-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="e6aa2-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="e6aa2-113">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="e6aa2-113">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="e6aa2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6aa2-114">Requirements</span></span>  
 <span data-ttu-id="e6aa2-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e6aa2-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e6aa2-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e6aa2-116">See Also</span></span>  
 [<span data-ttu-id="e6aa2-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e6aa2-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
