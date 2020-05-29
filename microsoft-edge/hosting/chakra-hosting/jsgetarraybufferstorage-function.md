---
description: Obtém o armazenamento de memória subjacente usado por um ArrayBuffer.
title: Função JsGetArrayBufferStorage | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 712ae298-36a9-47ef-b089-e51835c056bc
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e8d265f3e81015ba9f5d0547b6b1c7246c23ce5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562196"
---
# <span data-ttu-id="02b78-103">Função JsGetArrayBufferStorage</span><span class="sxs-lookup"><span data-stu-id="02b78-103">JsGetArrayBufferStorage Function</span></span>
<span data-ttu-id="02b78-104">Obtém o armazenamento de memória subjacente usado por um `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="02b78-104">Obtains the underlying memory storage used by an `ArrayBuffer`.</span></span>  
  
## <span data-ttu-id="02b78-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02b78-105">Syntax</span></span>  
  
```cpp  
JsErrorCode STDAPI_ JsGetArrayBufferStorage(  
   _In_ JsValueRef arrayBuffer,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="02b78-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02b78-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="02b78-107">A instância ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="02b78-107">The ArrayBuffer instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="02b78-108">O buffer do ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="02b78-108">The ArrayBuffer's buffer.</span></span> <span data-ttu-id="02b78-109">O tempo de vida do buffer retornado é o mesmo que o tempo de vida do `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="02b78-109">The lifetime of the buffer returned is the same as the lifetime of the `ArrayBuffer`.</span></span> <span data-ttu-id="02b78-110">O ponteiro de buffer não conta como uma referência para a `ArrayBuffer` finalidade da coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="02b78-110">The buffer pointer does not count as a reference to the `ArrayBuffer` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="02b78-111">O número de bytes no buffer.</span><span class="sxs-lookup"><span data-stu-id="02b78-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="02b78-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="02b78-112">Return Value</span></span>  
 <span data-ttu-id="02b78-113">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="02b78-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="02b78-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="02b78-114">Remarks</span></span>  
 <span data-ttu-id="02b78-115">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="02b78-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="02b78-116">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="02b78-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="02b78-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02b78-117">Requirements</span></span>  
 <span data-ttu-id="02b78-118">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="02b78-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="02b78-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="02b78-119">See Also</span></span>  
 [<span data-ttu-id="02b78-120">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="02b78-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)