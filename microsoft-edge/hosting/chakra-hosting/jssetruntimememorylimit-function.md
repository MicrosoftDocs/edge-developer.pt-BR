---
description: Define o limite de memória atual para um tempo de execução.
title: Função JsSetRuntimeMemoryLimit | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryLimit
helpviewer_keywords:
- JsSetRuntimeMemoryLimit function
ms.assetid: 74feb31f-19f6-43e3-b117-0694c59ac593
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ec8d098c528ac813926797280541aa2c9c4fee79
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562006"
---
# <span data-ttu-id="6096c-103">Função JsSetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="6096c-103">JsSetRuntimeMemoryLimit Function</span></span>
<span data-ttu-id="6096c-104">Define o limite de memória atual para um tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="6096c-104">Sets the current memory limit for a runtime.</span></span>  
  
## <span data-ttu-id="6096c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6096c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _In_ size_t memoryLimit  
);  
```  
  
#### <span data-ttu-id="6096c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6096c-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="6096c-107">O tempo de execução cujo limite de memória deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="6096c-107">The runtime whose memory limit is to be set.</span></span>  
  
 `memoryLimit`  
 <span data-ttu-id="6096c-108">O novo limite de memória em tempo de execução, em bytes ou-1 para nenhum limite de memória.</span><span class="sxs-lookup"><span data-stu-id="6096c-108">The new runtime memory limit, in bytes, or -1 for no memory limit.</span></span>  
  
## <span data-ttu-id="6096c-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6096c-109">Return Value</span></span>  
 <span data-ttu-id="6096c-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="6096c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6096c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6096c-111">Remarks</span></span>  
 <span data-ttu-id="6096c-112">Um limite de memória causará qualquer operação que exceda o limite de falha com um erro de "memória insuficiente".</span><span class="sxs-lookup"><span data-stu-id="6096c-112">A memory limit will cause any operation which exceeds the limit to fail with an "out of memory" error.</span></span> <span data-ttu-id="6096c-113">Definir o limite de memória do tempo de execução para-1 significa que o tempo de execução não tem limite de memória.</span><span class="sxs-lookup"><span data-stu-id="6096c-113">Setting a runtime's memory limit to -1 means that the runtime has no memory limit.</span></span> <span data-ttu-id="6096c-114">Novos tempos de execução padrão para não ter limite de memória.</span><span class="sxs-lookup"><span data-stu-id="6096c-114">New runtimes default to having no memory limit.</span></span> <span data-ttu-id="6096c-115">Se o novo limite de memória exceder o uso atual, a chamada será bem-sucedida e todas as atribuições futuras nesse tempo de execução falharão até que o uso da memória do tempo de execução fique abaixo do limite.</span><span class="sxs-lookup"><span data-stu-id="6096c-115">If the new memory limit exceeds current usage, the call will succeed and any future allocations in this runtime will fail until the runtime's memory usage drops below the limit.</span></span>  
  
 <span data-ttu-id="6096c-116">O limite de memória do tempo de execução pode ser sempre definido, independentemente do tempo de execução estar ativo ou não em outro thread.</span><span class="sxs-lookup"><span data-stu-id="6096c-116">A runtime's memory limit can be always be set, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="6096c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6096c-117">Requirements</span></span>  
 <span data-ttu-id="6096c-118">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6096c-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6096c-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6096c-119">See Also</span></span>  
 [<span data-ttu-id="6096c-120">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6096c-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)