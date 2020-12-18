---
description: Suspende a execução do script e encerra todos os scripts em execução em um tempo de execução.
title: Função JsDisableRuntimeExecution | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6a08e6a7f89c724f8cf1a73afd97d2cb23c0334e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231625"
---
# <span data-ttu-id="0162c-103">Função JsDisableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="0162c-103">JsDisableRuntimeExecution Function</span></span>

<span data-ttu-id="0162c-104">Suspende a execução do script e encerra todos os scripts em execução em um tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="0162c-104">Suspends script execution and terminates any running scripts in a runtime.</span></span>  
  
## <span data-ttu-id="0162c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0162c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDisableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="0162c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0162c-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="0162c-107">O tempo de execução a ser suspenso.</span><span class="sxs-lookup"><span data-stu-id="0162c-107">The runtime to be suspended.</span></span>  
  
## <span data-ttu-id="0162c-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0162c-108">Return Value</span></span>  
 <span data-ttu-id="0162c-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="0162c-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0162c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="0162c-110">Remarks</span></span>  
 <span data-ttu-id="0162c-111">As chamadas para um tempo de execução suspenso falharão até `JsEnableRuntimeExecution` serem chamadas.</span><span class="sxs-lookup"><span data-stu-id="0162c-111">Calls to a suspended runtime will fail until `JsEnableRuntimeExecution` is called.</span></span>  
  
 <span data-ttu-id="0162c-112">Essa API não precisa ser chamada no thread em que o tempo de execução está ativado.</span><span class="sxs-lookup"><span data-stu-id="0162c-112">This API does not have to be called on the thread the runtime is active on.</span></span> <span data-ttu-id="0162c-113">Embora o tempo de execução seja definido em um estado suspenso, um script em execução pode não ser suspenso imediatamente; um script em execução será encerrado com uma exceção uncatchável o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="0162c-113">Although the runtime will be set into a suspended state, an executing script may not be suspended immediately; a running script will be terminated with an uncatchable exception as soon as possible.</span></span>  
  
 <span data-ttu-id="0162c-114">Suspender a execução em um tempo de execução que já está suspenso não é op.</span><span class="sxs-lookup"><span data-stu-id="0162c-114">Suspending execution in a runtime that is already suspended is a no-op.</span></span>  
  
## <span data-ttu-id="0162c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0162c-115">Requirements</span></span>  
 <span data-ttu-id="0162c-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0162c-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0162c-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0162c-117">See Also</span></span>  
 [<span data-ttu-id="0162c-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0162c-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
