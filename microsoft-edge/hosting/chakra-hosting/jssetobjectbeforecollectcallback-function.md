---
description: Define uma função de retorno de chamada que é chamada pelo tempo de execução antes da coleta de lixo de um objeto.
title: Função JsSetObjectBeforeCollectCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: ea2cbd94-d8b0-4fa9-a4a1-c75a4e338eaf
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 77a59c6ace96809c0b232c96aa9639555e7badcd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562105"
---
# <span data-ttu-id="e3adc-103">Função JsSetObjectBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="e3adc-103">JsSetObjectBeforeCollectCallback Function</span></span>
<span data-ttu-id="e3adc-104">Define uma função de retorno de chamada que é chamada pelo tempo de execução antes da coleta de lixo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="e3adc-104">Sets a callback function that is called by the runtime before garbage collection of an object.</span></span>  
  
## <span data-ttu-id="e3adc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3adc-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetObjectBeforeCollectCallback(  
   _In_ JsRef ref,  
   _In_opt_ void *callbackState,  
   _In_ JsObjectBeforeCollectCallback objectBeforeCollectCallback  
);  
```  
  
#### <span data-ttu-id="e3adc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3adc-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="e3adc-107">O objeto para o qual registrar o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e3adc-107">The object for which to register the callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="e3adc-108">Estado fornecido pelo usuário que será devolvido ao retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e3adc-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `objectBeforeCollectCallback`  
 <span data-ttu-id="e3adc-109">A função de retorno de chamada sendo definida.</span><span class="sxs-lookup"><span data-stu-id="e3adc-109">The callback function being set.</span></span> <span data-ttu-id="e3adc-110">Use NULL para limpar o retorno de chamada registrado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e3adc-110">Use null to clear previously registered callback.</span></span>  
  
## <span data-ttu-id="e3adc-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e3adc-111">Return Value</span></span>  
 <span data-ttu-id="e3adc-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="e3adc-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e3adc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3adc-113">Remarks</span></span>  
 <span data-ttu-id="e3adc-114">O retorno de chamada é invocado no thread de execução do tempo de execução atual, portanto a execução é bloqueada até que o retorno de chamada seja concluído.</span><span class="sxs-lookup"><span data-stu-id="e3adc-114">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="e3adc-115">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="e3adc-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="e3adc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3adc-116">Requirements</span></span>  
 <span data-ttu-id="e3adc-117">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e3adc-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e3adc-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e3adc-118">See Also</span></span>  
 [<span data-ttu-id="e3adc-119">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e3adc-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)