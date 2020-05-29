---
description: Cria um `DataView` objeto JavaScript.
title: Função JsCreateDataView | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1bf237458e8561b7070e4f3f0d4a14050f028375
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561105"
---
# <span data-ttu-id="a63ff-103">Função JsCreateDataView</span><span class="sxs-lookup"><span data-stu-id="a63ff-103">JsCreateDataView Function</span></span>
<span data-ttu-id="a63ff-104">Cria um `DataView` objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a63ff-104">Creates a Javascript `DataView` object.</span></span>  
  
## <span data-ttu-id="a63ff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a63ff-105">Syntax</span></span>  
  
```cpp  
JsErrorCode  JsCreateDataView(  
   _In_ JsValueRef arrayBuffer,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="a63ff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a63ff-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="a63ff-107">Um `ArrayBuffer` objeto existente a ser usado como armazenamento para o objeto de resultado `DataView` .</span><span class="sxs-lookup"><span data-stu-id="a63ff-107">An existing `ArrayBuffer` object to use as the storage for the result `DataView` object.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="a63ff-108">O offset em bytes do início do `arrayBuffer` para o resultado `DataView` para referência.</span><span class="sxs-lookup"><span data-stu-id="a63ff-108">The offset in bytes from the start of `arrayBuffer` for result `DataView` to reference.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="a63ff-109">O número de bytes em ArrayBuffer para o DataView do resultado fazer referência.</span><span class="sxs-lookup"><span data-stu-id="a63ff-109">The number of bytes in the ArrayBuffer for result DataView to reference.</span></span>  
  
 `result`  
 <span data-ttu-id="a63ff-110">O novo objeto DataView.</span><span class="sxs-lookup"><span data-stu-id="a63ff-110">The new DataView object.</span></span>  
  
## <span data-ttu-id="a63ff-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a63ff-111">Return Value</span></span>  
 <span data-ttu-id="a63ff-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="a63ff-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a63ff-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a63ff-113">Remarks</span></span>  
 <span data-ttu-id="a63ff-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="a63ff-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="a63ff-115">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a63ff-115">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="a63ff-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a63ff-116">Requirements</span></span>  
 <span data-ttu-id="a63ff-117">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a63ff-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a63ff-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a63ff-118">See Also</span></span>  
 [<span data-ttu-id="a63ff-119">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a63ff-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)