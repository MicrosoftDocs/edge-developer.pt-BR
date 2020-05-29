---
description: Cria um objeto matriz tipada JavaScript.
title: Função JsCreateTypedArray | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 937a2a91-6f5f-4aaa-a018-d3089702bf36
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 57c5d15d76bf8b3ff29d10f7500fe41b3e959f68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561080"
---
# <span data-ttu-id="81f0a-103">Função JsCreateTypedArray</span><span class="sxs-lookup"><span data-stu-id="81f0a-103">JsCreateTypedArray Function</span></span>
<span data-ttu-id="81f0a-104">Cria um objeto matriz tipada JavaScript.</span><span class="sxs-lookup"><span data-stu-id="81f0a-104">Creates a JavaScript typed array object.</span></span>  
  
## <span data-ttu-id="81f0a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81f0a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypedArray(  
   _In_ JsTypedArrayType arrayType,  
   _In_ JsValueRef baseArray,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int elementLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="81f0a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81f0a-106">Parameters</span></span>  
 `arrayType`  
 <span data-ttu-id="81f0a-107">O tipo da matriz a ser criada.</span><span class="sxs-lookup"><span data-stu-id="81f0a-107">The type of the array to create.</span></span>  
  
 `baseArray`  
 <span data-ttu-id="81f0a-108">A matriz base da nova matriz.</span><span class="sxs-lookup"><span data-stu-id="81f0a-108">The base array of the new array.</span></span> <span data-ttu-id="81f0a-109">Use `JS_INVALID_REFERENCE` se não houver matriz base.</span><span class="sxs-lookup"><span data-stu-id="81f0a-109">Use `JS_INVALID_REFERENCE` if no base array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="81f0a-110">O offset em bytes do início de `baseArray` ( `ArrayBuffer` ) para a matriz de resultado digitada para fazer referência.</span><span class="sxs-lookup"><span data-stu-id="81f0a-110">The offset in bytes from the start of `baseArray` (`ArrayBuffer`) for result typed array to reference.</span></span> <span data-ttu-id="81f0a-111">Aplicável somente quando `baseArray` é um `ArrayBuffer` objeto.</span><span class="sxs-lookup"><span data-stu-id="81f0a-111">Only applicable when `baseArray` is an `ArrayBuffer` object.</span></span> <span data-ttu-id="81f0a-112">Caso contrário, deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="81f0a-112">Must be 0 otherwise.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="81f0a-113">O número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="81f0a-113">The number of elements in the array.</span></span> <span data-ttu-id="81f0a-114">Só se aplica ao criar uma nova matriz tipada sem `baseArray` ( `baseArray` is `JS_INVALID_REFERENCE` ) ou quando `baseArray` é um `ArrayBuffer` objeto.</span><span class="sxs-lookup"><span data-stu-id="81f0a-114">Only applicable when creating a new typed array without `baseArray` (`baseArray` is `JS_INVALID_REFERENCE`) or when `baseArray` is an `ArrayBuffer` object.</span></span> <span data-ttu-id="81f0a-115">Caso contrário, deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="81f0a-115">Must be 0 otherwise.</span></span>  
  
 `result`  
 <span data-ttu-id="81f0a-116">O novo objeto de matriz tipada.</span><span class="sxs-lookup"><span data-stu-id="81f0a-116">The new typed array object.</span></span>  
  
## <span data-ttu-id="81f0a-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="81f0a-117">Return Value</span></span>  
 <span data-ttu-id="81f0a-118">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="81f0a-118">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="81f0a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="81f0a-119">Remarks</span></span>  
 <span data-ttu-id="81f0a-120">`baseArray`Pode ser uma `ArrayBuffer` , outra matriz tipada ou JavaScript `Array` .</span><span class="sxs-lookup"><span data-stu-id="81f0a-120">The `baseArray` can be an `ArrayBuffer`, another typed array, or a JavaScript `Array`.</span></span> <span data-ttu-id="81f0a-121">A matriz tipada retornada usará o `baseArray` se for um `ArrayBuffer` ou, caso contrário, criará e usará uma cópia da matriz de origem subjacente.</span><span class="sxs-lookup"><span data-stu-id="81f0a-121">The returned typed array will use the `baseArray` if it is an `ArrayBuffer`, or otherwise create and use a copy of the underlying source array.</span></span>  
  
 <span data-ttu-id="81f0a-122">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="81f0a-122">Requires an active script context.</span></span>  
  
 <span data-ttu-id="81f0a-123">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="81f0a-123">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="81f0a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81f0a-124">Requirements</span></span>  
 <span data-ttu-id="81f0a-125">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="81f0a-125">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="81f0a-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="81f0a-126">See Also</span></span>  
 [<span data-ttu-id="81f0a-127">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="81f0a-127">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)