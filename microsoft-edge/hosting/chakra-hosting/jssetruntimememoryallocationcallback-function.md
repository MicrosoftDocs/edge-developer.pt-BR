---
description: Define um retorno de chamada de alocação de memória para o tempo de execução especificado.
title: Função JsSetRuntimeMemoryAllocationCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryAllocationCallback
helpviewer_keywords:
- JsSetRuntimeMemoryAllocationCallback function
ms.assetid: 6aa7d58d-6456-4df1-815f-1ba36fb4ae14
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5c648761473023f00e894fbf75c794cfcc9422c5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562007"
---
# <span data-ttu-id="0186b-103">Função JsSetRuntimeMemoryAllocationCallback</span><span class="sxs-lookup"><span data-stu-id="0186b-103">JsSetRuntimeMemoryAllocationCallback Function</span></span>
<span data-ttu-id="0186b-104">Define um retorno de chamada de alocação de memória para o tempo de execução especificado.</span><span class="sxs-lookup"><span data-stu-id="0186b-104">Sets a memory allocation callback for specified runtime.</span></span>  
  
## <span data-ttu-id="0186b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0186b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryAllocationCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryAllocationCallback allocationCallback  
);  
```  
  
#### <span data-ttu-id="0186b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0186b-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="0186b-107">O tempo de execução para o qual registrar o retorno de chamada de alocação.</span><span class="sxs-lookup"><span data-stu-id="0186b-107">The runtime for which to register the allocation callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="0186b-108">Estado fornecido pelo usuário que será devolvido ao retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="0186b-108">User provided state that will be passed back to the callback.</span></span>  
  
 `allocationCallback`  
 <span data-ttu-id="0186b-109">Retorno de chamada de alocação de memória a ser chamado para eventos de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="0186b-109">Memory allocation callback to be called for memory allocation events.</span></span>  
  
## <span data-ttu-id="0186b-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0186b-110">Return Value</span></span>  
 <span data-ttu-id="0186b-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="0186b-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0186b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="0186b-112">Remarks</span></span>  
 <span data-ttu-id="0186b-113">O registro de um retorno de chamada de alocação de memória fará com que o Runtime chame de volta para o host sempre que ele adquirir memória de ou liberar memória para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0186b-113">Registering a memory allocation callback will cause the runtime to call back to the host whenever it acquires memory from, or releases memory to, the OS.</span></span> <span data-ttu-id="0186b-114">A rotina de retorno de chamada é chamada antes do Gerenciador de memória de tempo de execução aloca um bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="0186b-114">The callback routine is called before the runtime memory manager allocates a block of memory.</span></span> <span data-ttu-id="0186b-115">A alocação será rejeitada se o retorno de chamada retornar false.</span><span class="sxs-lookup"><span data-stu-id="0186b-115">The allocation will be rejected if the callback returns false.</span></span> <span data-ttu-id="0186b-116">O Gerenciador de memória de tempo de execução também invocará a rotina de retorno de chamada após a liberação de um bloco de memória, bem como após a falha de alocação.</span><span class="sxs-lookup"><span data-stu-id="0186b-116">The runtime memory manager will also invoke the callback routine after freeing a block of memory, as well as after allocation failures.</span></span>  
  
 <span data-ttu-id="0186b-117">O retorno de chamada é invocado no thread de execução do tempo de execução atual, portanto a execução é bloqueada até que o retorno de chamada seja concluído.</span><span class="sxs-lookup"><span data-stu-id="0186b-117">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="0186b-118">O valor de retorno do retorno de chamada não é armazenado; as atribuições rejeitadas anteriormente não impedirão que o tempo de execução chame o retorno de chamada novamente mais tarde para novas atribuições de memória.</span><span class="sxs-lookup"><span data-stu-id="0186b-118">The return value of the callback is not stored; previously rejected allocations will not prevent the runtime from invoking the callback again later for new memory allocations.</span></span>  
  
## <span data-ttu-id="0186b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0186b-119">Requirements</span></span>  
 <span data-ttu-id="0186b-120">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0186b-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0186b-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0186b-121">See Also</span></span>  
 [<span data-ttu-id="0186b-122">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0186b-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)