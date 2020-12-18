---
description: Cria um `DataView` objeto JavaScript.
title: Função JsCreateDataView | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1d6d170d53f3bfaf885713b6f3abca0b066f8c1d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231420"
---
# <span data-ttu-id="5092b-103">Função JsCreateDataView</span><span class="sxs-lookup"><span data-stu-id="5092b-103">JsCreateDataView Function</span></span>

<span data-ttu-id="5092b-104">Cria um `DataView` objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5092b-104">Creates a Javascript `DataView` object.</span></span>  
  
## <span data-ttu-id="5092b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5092b-105">Syntax</span></span>  
  
```cpp  
JsErrorCode  JsCreateDataView(  
   _In_ JsValueRef arrayBuffer,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="5092b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5092b-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="5092b-107">Um `ArrayBuffer` objeto existente a ser usado como armazenamento para o objeto de resultado `DataView` .</span><span class="sxs-lookup"><span data-stu-id="5092b-107">An existing `ArrayBuffer` object to use as the storage for the result `DataView` object.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="5092b-108">O offset em bytes do início do `arrayBuffer` para o resultado `DataView` para referência.</span><span class="sxs-lookup"><span data-stu-id="5092b-108">The offset in bytes from the start of `arrayBuffer` for result `DataView` to reference.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="5092b-109">O número de bytes em ArrayBuffer para o DataView do resultado fazer referência.</span><span class="sxs-lookup"><span data-stu-id="5092b-109">The number of bytes in the ArrayBuffer for result DataView to reference.</span></span>  
  
 `result`  
 <span data-ttu-id="5092b-110">O novo objeto DataView.</span><span class="sxs-lookup"><span data-stu-id="5092b-110">The new DataView object.</span></span>  
  
## <span data-ttu-id="5092b-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5092b-111">Return Value</span></span>  
 <span data-ttu-id="5092b-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="5092b-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5092b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5092b-113">Remarks</span></span>  
 <span data-ttu-id="5092b-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="5092b-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="5092b-115">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5092b-115">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="5092b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5092b-116">Requirements</span></span>  
 <span data-ttu-id="5092b-117">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5092b-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5092b-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5092b-118">See Also</span></span>  
 [<span data-ttu-id="5092b-119">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5092b-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
