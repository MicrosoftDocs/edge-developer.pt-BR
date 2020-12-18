---
description: 'Define uma função de retorno de chamada que é chamada pelo tempo de execução antes da coleta de lixo. '
title: Função JsSetRuntimeBeforeCollectCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeBeforeCollectCallback
helpviewer_keywords:
- JsSetRuntimeBeforeCollectCallback function
ms.assetid: 7b2fb911-6007-4ed9-a307-66cefe590ea4
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 94ad29fcfb778fc630d70664f917c6b5c2637dde
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231410"
---
# <span data-ttu-id="7e6b9-103">Função JsSetRuntimeBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="7e6b9-103">JsSetRuntimeBeforeCollectCallback Function</span></span>

<span data-ttu-id="7e6b9-104">Define uma função de retorno de chamada que é chamada pelo tempo de execução antes da coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="7e6b9-104">Sets a callback function that is called by the runtime before garbage collection.</span></span>  
  
## <span data-ttu-id="7e6b9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e6b9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeBeforeCollectCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsBeforeCollectCallback beforeCollectCallback  
);  
```  
  
#### <span data-ttu-id="7e6b9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e6b9-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="7e6b9-107">O tempo de execução para o qual registrar o retorno de chamada de alocação.</span><span class="sxs-lookup"><span data-stu-id="7e6b9-107">The runtime for which to register the allocation callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="7e6b9-108">Estado fornecido pelo usuário que será devolvido ao retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="7e6b9-108">User provided state that will be passed back to the callback.</span></span>  
  
 `beforeCollectCallback`  
 <span data-ttu-id="7e6b9-109">A função de retorno de chamada sendo definida.</span><span class="sxs-lookup"><span data-stu-id="7e6b9-109">The callback function being set.</span></span>  
  
## <span data-ttu-id="7e6b9-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7e6b9-110">Return Value</span></span>  
 <span data-ttu-id="7e6b9-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="7e6b9-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7e6b9-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e6b9-112">Remarks</span></span>  
 <span data-ttu-id="7e6b9-113">O retorno de chamada é invocado no thread de execução do tempo de execução atual, portanto a execução é bloqueada até que o retorno de chamada seja concluído.</span><span class="sxs-lookup"><span data-stu-id="7e6b9-113">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="7e6b9-114">O retorno de chamada pode ser usado pelos hosts para se preparar para a coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="7e6b9-114">The callback can be used by hosts to prepare for garbage collection.</span></span> <span data-ttu-id="7e6b9-115">Por exemplo, ao liberar referências desnecessárias em objetos Chakra.</span><span class="sxs-lookup"><span data-stu-id="7e6b9-115">For example, by releasing unnecessary references on Chakra objects.</span></span>  
  
## <span data-ttu-id="7e6b9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e6b9-116">Requirements</span></span>  
 <span data-ttu-id="7e6b9-117">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7e6b9-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7e6b9-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7e6b9-118">See Also</span></span>  
 [<span data-ttu-id="7e6b9-119">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7e6b9-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
