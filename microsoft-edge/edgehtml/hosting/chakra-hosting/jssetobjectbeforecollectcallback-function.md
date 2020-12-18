---
description: Define uma função de retorno de chamada que é chamada pelo tempo de execução antes da coleta de lixo de um objeto.
title: Função JsSetObjectBeforeCollectCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: ea2cbd94-d8b0-4fa9-a4a1-c75a4e338eaf
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4689184dccaf6bc9f98eeacda5f5a4b91a927d40
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231409"
---
# <span data-ttu-id="50b08-103">Função JsSetObjectBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="50b08-103">JsSetObjectBeforeCollectCallback Function</span></span>

<span data-ttu-id="50b08-104">Define uma função de retorno de chamada que é chamada pelo tempo de execução antes da coleta de lixo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="50b08-104">Sets a callback function that is called by the runtime before garbage collection of an object.</span></span>  
  
## <span data-ttu-id="50b08-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50b08-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetObjectBeforeCollectCallback(  
   _In_ JsRef ref,  
   _In_opt_ void *callbackState,  
   _In_ JsObjectBeforeCollectCallback objectBeforeCollectCallback  
);  
```  
  
#### <span data-ttu-id="50b08-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50b08-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="50b08-107">O objeto para o qual registrar o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="50b08-107">The object for which to register the callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="50b08-108">Estado fornecido pelo usuário que será devolvido ao retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="50b08-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `objectBeforeCollectCallback`  
 <span data-ttu-id="50b08-109">A função de retorno de chamada sendo definida.</span><span class="sxs-lookup"><span data-stu-id="50b08-109">The callback function being set.</span></span> <span data-ttu-id="50b08-110">Use NULL para limpar o retorno de chamada registrado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="50b08-110">Use null to clear previously registered callback.</span></span>  
  
## <span data-ttu-id="50b08-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="50b08-111">Return Value</span></span>  
 <span data-ttu-id="50b08-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="50b08-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="50b08-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="50b08-113">Remarks</span></span>  
 <span data-ttu-id="50b08-114">O retorno de chamada é invocado no thread de execução do tempo de execução atual, portanto a execução é bloqueada até que o retorno de chamada seja concluído.</span><span class="sxs-lookup"><span data-stu-id="50b08-114">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="50b08-115">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="50b08-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="50b08-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50b08-116">Requirements</span></span>  
 <span data-ttu-id="50b08-117">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="50b08-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="50b08-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="50b08-118">See Also</span></span>  
 [<span data-ttu-id="50b08-119">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="50b08-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
