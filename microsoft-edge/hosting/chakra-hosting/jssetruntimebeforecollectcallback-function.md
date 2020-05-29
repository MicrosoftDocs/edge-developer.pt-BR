---
description: 'Define uma função de retorno de chamada que é chamada pelo tempo de execução antes da coleta de lixo. '
title: Função JsSetRuntimeBeforeCollectCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeBeforeCollectCallback
helpviewer_keywords:
- JsSetRuntimeBeforeCollectCallback function
ms.assetid: 7b2fb911-6007-4ed9-a307-66cefe590ea4
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 31aefd28698c14a6fe17421a990a7c8b120876bf
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562008"
---
# <span data-ttu-id="14075-103">Função JsSetRuntimeBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="14075-103">JsSetRuntimeBeforeCollectCallback Function</span></span>
<span data-ttu-id="14075-104">Define uma função de retorno de chamada que é chamada pelo tempo de execução antes da coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="14075-104">Sets a callback function that is called by the runtime before garbage collection.</span></span>  
  
## <span data-ttu-id="14075-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14075-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeBeforeCollectCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsBeforeCollectCallback beforeCollectCallback  
);  
```  
  
#### <span data-ttu-id="14075-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14075-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="14075-107">O tempo de execução para o qual registrar o retorno de chamada de alocação.</span><span class="sxs-lookup"><span data-stu-id="14075-107">The runtime for which to register the allocation callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="14075-108">Estado fornecido pelo usuário que será devolvido ao retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="14075-108">User provided state that will be passed back to the callback.</span></span>  
  
 `beforeCollectCallback`  
 <span data-ttu-id="14075-109">A função de retorno de chamada sendo definida.</span><span class="sxs-lookup"><span data-stu-id="14075-109">The callback function being set.</span></span>  
  
## <span data-ttu-id="14075-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="14075-110">Return Value</span></span>  
 <span data-ttu-id="14075-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="14075-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="14075-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="14075-112">Remarks</span></span>  
 <span data-ttu-id="14075-113">O retorno de chamada é invocado no thread de execução do tempo de execução atual, portanto a execução é bloqueada até que o retorno de chamada seja concluído.</span><span class="sxs-lookup"><span data-stu-id="14075-113">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="14075-114">O retorno de chamada pode ser usado pelos hosts para se preparar para a coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="14075-114">The callback can be used by hosts to prepare for garbage collection.</span></span> <span data-ttu-id="14075-115">Por exemplo, ao liberar referências desnecessárias em objetos Chakra.</span><span class="sxs-lookup"><span data-stu-id="14075-115">For example, by releasing unnecessary references on Chakra objects.</span></span>  
  
## <span data-ttu-id="14075-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14075-116">Requirements</span></span>  
 <span data-ttu-id="14075-117">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="14075-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="14075-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="14075-118">See Also</span></span>  
 [<span data-ttu-id="14075-119">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="14075-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)