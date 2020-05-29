---
description: Define uma função de retorno de chamada de continuação Promise que é chamada pelo contexto quando uma tarefa precisa ser colocada em fila para execução futura.
title: Função JsSetPromiseContinuationCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 6ef0faf4-1500-4bd9-aeca-c208492af8ea
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9438bf05d879b0c2014c0a4d49d374d26eff3fb4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562102"
---
# <span data-ttu-id="bd97a-103">Função JsSetPromiseContinuationCallback</span><span class="sxs-lookup"><span data-stu-id="bd97a-103">JsSetPromiseContinuationCallback Function</span></span>
<span data-ttu-id="bd97a-104">Define uma função de retorno de chamada de continuação Promise que é chamada pelo contexto quando uma tarefa precisa ser colocada em fila para execução futura.</span><span class="sxs-lookup"><span data-stu-id="bd97a-104">Sets a promise continuation callback function that is called by the context when a task needs to be queued for future execution.</span></span>  
  
## <span data-ttu-id="bd97a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd97a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPromiseContinuationCallback(  
   _In_ JsPromiseContinuationCallback promiseContinuationCallback,  
   _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="bd97a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd97a-106">Parameters</span></span>  
 `promiseContinuationCallback`  
 <span data-ttu-id="bd97a-107">A função de retorno de chamada sendo definida.</span><span class="sxs-lookup"><span data-stu-id="bd97a-107">The callback function being set.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="bd97a-108">Estado fornecido pelo usuário que será devolvido ao retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="bd97a-108">User provided state that will be passed back to the callback.</span></span>  
  
## <span data-ttu-id="bd97a-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bd97a-109">Return Value</span></span>  
 <span data-ttu-id="bd97a-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="bd97a-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bd97a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd97a-111">Remarks</span></span>  
 <span data-ttu-id="bd97a-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="bd97a-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="bd97a-113">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="bd97a-113">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="bd97a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd97a-114">Requirements</span></span>  
 <span data-ttu-id="bd97a-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bd97a-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bd97a-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bd97a-116">See Also</span></span>  
 [<span data-ttu-id="bd97a-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bd97a-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)