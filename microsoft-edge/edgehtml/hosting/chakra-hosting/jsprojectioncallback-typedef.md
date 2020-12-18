---
description: O retorno de chamada JsRT que deve ser chamado com o contexto passado para `JsProjectionEnqueueCallback` o thread correto.
title: Typedef JsProjectionCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 211325b536dc84340974b02973f1de9d5749a60a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231751"
---
# <span data-ttu-id="e1dcd-103">Typedef JsProjectionCallback</span><span class="sxs-lookup"><span data-stu-id="e1dcd-103">JsProjectionCallback Typedef</span></span>

<span data-ttu-id="e1dcd-104">O retorno de chamada JsRT que deve ser chamado com o contexto passado para `JsProjectionEnqueueCallback` o thread correto.</span><span class="sxs-lookup"><span data-stu-id="e1dcd-104">The JsRT callback which should be called with the context passed to `JsProjectionEnqueueCallback` on the correct thread.</span></span>  
  
## <span data-ttu-id="e1dcd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1dcd-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionCallback)(  
  _In_ JsProjectionCallbackContext jsContext  
);  
```  
  
#### <span data-ttu-id="e1dcd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1dcd-106">Parameters</span></span>  
 `jsContext`  
 <span data-ttu-id="e1dcd-107">Requer chamadas `JsSetProjectionEnqueueCallback` para receber chamadas de retorno.</span><span class="sxs-lookup"><span data-stu-id="e1dcd-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
## <span data-ttu-id="e1dcd-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1dcd-108">Remarks</span></span>  
 <span data-ttu-id="e1dcd-109">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="e1dcd-109">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="e1dcd-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1dcd-110">Requirements</span></span>  
 <span data-ttu-id="e1dcd-111">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e1dcd-111">jsrt.h</span></span>  
  
## <span data-ttu-id="e1dcd-112">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e1dcd-112">See Also</span></span>  
 [<span data-ttu-id="e1dcd-113">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e1dcd-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
