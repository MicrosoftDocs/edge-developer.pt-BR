---
description: Um retorno de chamada de continuação da Promise.
title: Typedef JsPromiseContinuationCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da121d186cd9d0ab1a9770be08c9a92b52cf3366
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231984"
---
# <span data-ttu-id="d2916-103">Typedef JsPromiseContinuationCallback</span><span class="sxs-lookup"><span data-stu-id="d2916-103">JsPromiseContinuationCallback Typedef</span></span>

<span data-ttu-id="d2916-104">Um retorno de chamada de continuação da Promise.</span><span class="sxs-lookup"><span data-stu-id="d2916-104">A promise continuation callback.</span></span>  
  
## <span data-ttu-id="d2916-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2916-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsPromiseContinuationCallback)(  
  _In_ JsValueRef task,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="d2916-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2916-106">Parameters</span></span>  
 `task`  
  `callbackState`  
  
## <span data-ttu-id="d2916-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2916-107">Remarks</span></span>  
 <span data-ttu-id="d2916-108">O host pode especificar um retorno de chamada de continuação Promise em `JsSetPromiseContinuationCallback` .</span><span class="sxs-lookup"><span data-stu-id="d2916-108">The host can specify a promise continuation callback in `JsSetPromiseContinuationCallback`.</span></span> <span data-ttu-id="d2916-109">Se um script criar uma tarefa para ser executada mais tarde, o retorno de chamada de continuação Promise será chamado com a tarefa e a tarefa deverá ser inserida em uma fila FIFO para ser executada quando o script atual for executado.</span><span class="sxs-lookup"><span data-stu-id="d2916-109">If a script creates a task to be run later, then the promise continuation callback will be called with the task and the task should be put in a FIFO queue, to be run when the current script is done executing.</span></span>  
  
 <span data-ttu-id="d2916-110">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="d2916-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="d2916-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2916-111">Requirements</span></span>  
 <span data-ttu-id="d2916-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d2916-112">jsrt.h</span></span>  
  
## <span data-ttu-id="d2916-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d2916-113">See Also</span></span>  
 [<span data-ttu-id="d2916-114">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d2916-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
