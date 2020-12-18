---
description: Cria um `ArrayBuffer` objeto JavaScript.
title: Função JsCreateArrayBuffer | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c9e74184-7dd9-41a7-a1fe-9575e1701392
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3bee44d77f78bd35705211c598db78ab09000c71
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231421"
---
# <span data-ttu-id="2e466-103">Função JsCreateArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="2e466-103">JsCreateArrayBuffer Function</span></span>

<span data-ttu-id="2e466-104">Cria um `ArrayBuffer` objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2e466-104">Creates a JavaScript `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="2e466-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e466-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArrayBuffer(  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="2e466-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e466-106">Parameters</span></span>  
 `byteLength`  
 <span data-ttu-id="2e466-107">O número de bytes no ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="2e466-107">The number of bytes in the ArrayBuffer.</span></span>  
  
 `result`  
 <span data-ttu-id="2e466-108">O novo objeto ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="2e466-108">The new ArrayBuffer object.</span></span>  
  
## <span data-ttu-id="2e466-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2e466-109">Return Value</span></span>  
 <span data-ttu-id="2e466-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="2e466-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2e466-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e466-111">Remarks</span></span>  
 <span data-ttu-id="2e466-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="2e466-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="2e466-113">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2e466-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="2e466-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e466-114">Requirements</span></span>  
 <span data-ttu-id="2e466-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2e466-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2e466-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2e466-116">See Also</span></span>  
 [<span data-ttu-id="2e466-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2e466-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
