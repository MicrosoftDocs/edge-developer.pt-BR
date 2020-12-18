---
description: Obtém propriedades usadas com frequência de uma matriz digitada.
title: Função JsGetTypedArrayInfo | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fdc9a05a2aebdabfd0c8e95c848d3bd5f97e580a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231789"
---
# <span data-ttu-id="8dc4e-103">Função JsGetTypedArrayInfo</span><span class="sxs-lookup"><span data-stu-id="8dc4e-103">JsGetTypedArrayInfo Function</span></span>

<span data-ttu-id="8dc4e-104">Obtém propriedades usadas com frequência de uma matriz digitada.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-104">Obtains frequently used properties of a typed array.</span></span>  
  
## <span data-ttu-id="8dc4e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8dc4e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### <span data-ttu-id="8dc4e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8dc4e-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="8dc4e-107">A instância de matriz tipada.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-107">The typed array instance.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="8dc4e-108">O tipo da matriz.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-108">The type of the array.</span></span>  
  
 `arrayBuffer`  
 <span data-ttu-id="8dc4e-109">A `ArrayBuffer` BACKSTORE da matriz.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-109">The `ArrayBuffer` backstore of the array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="8dc4e-110">O offset em bytes do início de arrayBuffer referenciado pela matriz.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-110">The offset in bytes from the start of arrayBuffer referenced by the array.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="8dc4e-111">O número de bytes na matriz.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-111">The number of bytes in the array.</span></span>  
  
## <span data-ttu-id="8dc4e-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8dc4e-112">Return Value</span></span>  
 <span data-ttu-id="8dc4e-113">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8dc4e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8dc4e-114">Remarks</span></span>  
 <span data-ttu-id="8dc4e-115">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="8dc4e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8dc4e-116">Requirements</span></span>  
 <span data-ttu-id="8dc4e-117">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8dc4e-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8dc4e-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8dc4e-118">See Also</span></span>  
 [<span data-ttu-id="8dc4e-119">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8dc4e-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
