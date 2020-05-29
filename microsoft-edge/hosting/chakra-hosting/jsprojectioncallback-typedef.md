---
description: O retorno de chamada JsRT que deve ser chamado com o contexto passado para `JsProjectionEnqueueCallback` o thread correto.
title: Typedef JsProjectionCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b30f9a7dc4671896eeacecbf58ef88f0383e9e7e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561010"
---
# <span data-ttu-id="d8e1c-103">Typedef JsProjectionCallback</span><span class="sxs-lookup"><span data-stu-id="d8e1c-103">JsProjectionCallback Typedef</span></span>
<span data-ttu-id="d8e1c-104">O retorno de chamada JsRT que deve ser chamado com o contexto passado para `JsProjectionEnqueueCallback` o thread correto.</span><span class="sxs-lookup"><span data-stu-id="d8e1c-104">The JsRT callback which should be called with the context passed to `JsProjectionEnqueueCallback` on the correct thread.</span></span>  
  
## <span data-ttu-id="d8e1c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8e1c-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionCallback)(  
  _In_ JsProjectionCallbackContext jsContext  
);  
```  
  
#### <span data-ttu-id="d8e1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8e1c-106">Parameters</span></span>  
 `jsContext`  
 <span data-ttu-id="d8e1c-107">Requer chamadas `JsSetProjectionEnqueueCallback` para receber chamadas de retorno.</span><span class="sxs-lookup"><span data-stu-id="d8e1c-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
## <span data-ttu-id="d8e1c-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8e1c-108">Remarks</span></span>  
 <span data-ttu-id="d8e1c-109">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="d8e1c-109">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="d8e1c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8e1c-110">Requirements</span></span>  
 <span data-ttu-id="d8e1c-111">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d8e1c-111">jsrt.h</span></span>  
  
## <span data-ttu-id="d8e1c-112">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d8e1c-112">See Also</span></span>  
 [<span data-ttu-id="d8e1c-113">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d8e1c-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)