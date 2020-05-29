---
description: Obtém propriedades usadas com frequência de uma matriz digitada.
title: Função JsGetTypedArrayInfo | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b33b0c515733864c1849a08aa2f8dc6e884c22ad
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561033"
---
# <span data-ttu-id="3bc10-103">Função JsGetTypedArrayInfo</span><span class="sxs-lookup"><span data-stu-id="3bc10-103">JsGetTypedArrayInfo Function</span></span>
<span data-ttu-id="3bc10-104">Obtém propriedades usadas com frequência de uma matriz digitada.</span><span class="sxs-lookup"><span data-stu-id="3bc10-104">Obtains frequently used properties of a typed array.</span></span>  
  
## <span data-ttu-id="3bc10-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bc10-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### <span data-ttu-id="3bc10-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bc10-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="3bc10-107">A instância de matriz tipada.</span><span class="sxs-lookup"><span data-stu-id="3bc10-107">The typed array instance.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="3bc10-108">O tipo da matriz.</span><span class="sxs-lookup"><span data-stu-id="3bc10-108">The type of the array.</span></span>  
  
 `arrayBuffer`  
 <span data-ttu-id="3bc10-109">A `ArrayBuffer` BACKSTORE da matriz.</span><span class="sxs-lookup"><span data-stu-id="3bc10-109">The `ArrayBuffer` backstore of the array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="3bc10-110">O offset em bytes do início de arrayBuffer referenciado pela matriz.</span><span class="sxs-lookup"><span data-stu-id="3bc10-110">The offset in bytes from the start of arrayBuffer referenced by the array.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="3bc10-111">O número de bytes na matriz.</span><span class="sxs-lookup"><span data-stu-id="3bc10-111">The number of bytes in the array.</span></span>  
  
## <span data-ttu-id="3bc10-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3bc10-112">Return Value</span></span>  
 <span data-ttu-id="3bc10-113">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="3bc10-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3bc10-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3bc10-114">Remarks</span></span>  
 <span data-ttu-id="3bc10-115">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="3bc10-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="3bc10-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bc10-116">Requirements</span></span>  
 <span data-ttu-id="3bc10-117">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3bc10-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3bc10-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3bc10-118">See Also</span></span>  
 [<span data-ttu-id="3bc10-119">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3bc10-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)