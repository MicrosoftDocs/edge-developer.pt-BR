---
description: Obtém o armazenamento de memória subjacente usado por um DataView.
title: Função JsGetDataViewStorage | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55f357e4a94b1edbc417ebb14ab99db11083dff4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231670"
---
# <span data-ttu-id="0d37b-103">Função JsGetDataViewStorage</span><span class="sxs-lookup"><span data-stu-id="0d37b-103">JsGetDataViewStorage Function</span></span>

<span data-ttu-id="0d37b-104">Obtém o armazenamento de memória subjacente usado por a `DataView` .</span><span class="sxs-lookup"><span data-stu-id="0d37b-104">Obtains the underlying memory storage used by a `DataView`.</span></span>  
  
## <span data-ttu-id="0d37b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d37b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetDataViewStorage(  
   _In_ JsValueRef dataView,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="0d37b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d37b-106">Parameters</span></span>  
 `dataView`  
 <span data-ttu-id="0d37b-107">A instância DataView.</span><span class="sxs-lookup"><span data-stu-id="0d37b-107">The DataView instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="0d37b-108">O buffer do DataView.</span><span class="sxs-lookup"><span data-stu-id="0d37b-108">The DataView's buffer.</span></span> <span data-ttu-id="0d37b-109">O tempo de vida do buffer retornado é o mesmo que o tempo de vida do `DataView` .</span><span class="sxs-lookup"><span data-stu-id="0d37b-109">The lifetime of the buffer returned is the same as the lifetime of the `DataView`.</span></span> <span data-ttu-id="0d37b-110">O ponteiro de buffer não conta como uma referência para a `DataView` finalidade da coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="0d37b-110">The buffer pointer does not count as a reference to the `DataView` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="0d37b-111">O número de bytes no buffer.</span><span class="sxs-lookup"><span data-stu-id="0d37b-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="0d37b-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0d37b-112">Return Value</span></span>  
 <span data-ttu-id="0d37b-113">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="0d37b-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0d37b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d37b-114">Remarks</span></span>  
 <span data-ttu-id="0d37b-115">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="0d37b-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="0d37b-116">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0d37b-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="0d37b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d37b-117">Requirements</span></span>  
 <span data-ttu-id="0d37b-118">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0d37b-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0d37b-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0d37b-119">See Also</span></span>  
 [<span data-ttu-id="0d37b-120">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0d37b-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)