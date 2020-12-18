---
description: Obtém o armazenamento de memória subjacente usado por uma matriz digitada.
title: Função JsGetTypedArrayStorage | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 52e4ac5f-cc71-456d-95de-a48f7327503d
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 442727228433368de14bac528ea416fcc2a95fa8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231286"
---
# <span data-ttu-id="44efe-103">Função JsGetTypedArrayStorage</span><span class="sxs-lookup"><span data-stu-id="44efe-103">JsGetTypedArrayStorage Function</span></span>

<span data-ttu-id="44efe-104">Obtém o armazenamento de memória subjacente usado por uma matriz digitada.</span><span class="sxs-lookup"><span data-stu-id="44efe-104">Obtains the underlying memory storage used by a typed array.</span></span>  
  
## <span data-ttu-id="44efe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44efe-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayStorage(  
   _In_ JsValueRef typedArray,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength,  
   _Out_opt_ JsTypedArrayType *arrayType,  
   _Out_opt_ int *elementSize  
);  
```  
  
#### <span data-ttu-id="44efe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44efe-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="44efe-107">A instância de matriz tipada.</span><span class="sxs-lookup"><span data-stu-id="44efe-107">The typed array instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="44efe-108">O buffer da matriz.</span><span class="sxs-lookup"><span data-stu-id="44efe-108">The array's buffer.</span></span> <span data-ttu-id="44efe-109">O tempo de vida do buffer retornado é o mesmo que o tempo de vida da matriz.</span><span class="sxs-lookup"><span data-stu-id="44efe-109">The lifetime of the buffer returned is the same as the lifetime of the array.</span></span> <span data-ttu-id="44efe-110">O ponteiro de buffer não conta como uma referência à matriz para a finalidade da coleta de lixo.</span><span class="sxs-lookup"><span data-stu-id="44efe-110">The buffer pointer does not count as a reference to the array for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="44efe-111">O número de bytes no buffer.</span><span class="sxs-lookup"><span data-stu-id="44efe-111">The number of bytes in the buffer.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="44efe-112">O tipo da matriz.</span><span class="sxs-lookup"><span data-stu-id="44efe-112">The type of the array.</span></span>  
  
 `elementSize`  
 <span data-ttu-id="44efe-113">O tamanho de um elemento da matriz.</span><span class="sxs-lookup"><span data-stu-id="44efe-113">The size of an element of the array.</span></span>  
  
## <span data-ttu-id="44efe-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="44efe-114">Return Value</span></span>  
 <span data-ttu-id="44efe-115">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="44efe-115">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="44efe-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="44efe-116">Remarks</span></span>  
 <span data-ttu-id="44efe-117">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="44efe-117">Requires an active script context.</span></span>  
  
 <span data-ttu-id="44efe-118">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="44efe-118">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="44efe-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44efe-119">Requirements</span></span>  
 <span data-ttu-id="44efe-120">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="44efe-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="44efe-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="44efe-121">See Also</span></span>  
 [<span data-ttu-id="44efe-122">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="44efe-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
