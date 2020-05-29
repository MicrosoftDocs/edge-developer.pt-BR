---
description: O contexto passado para o retorno de chamada do aplicativo, JsProjectionEnqueueCallback, de JsRT e, em seguida, passado de volta para JsRT no retorno de chamada fornecido, `JsProjectionCallback` pelo aplicativo na thread correta.
title: Typedef JsProjectionCallbackContext | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 58d4c74da13ae0dd269f3c101bbf3d2b95e77732
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561011"
---
# <span data-ttu-id="d0939-103">Typedef JsProjectionCallbackContext</span><span class="sxs-lookup"><span data-stu-id="d0939-103">JsProjectionCallbackContext Typedef</span></span>
<span data-ttu-id="d0939-104">O contexto passado para o retorno de chamada do aplicativo, JsProjectionEnqueueCallback, de JsRT e, em seguida, passado de volta para JsRT no retorno de chamada fornecido, `JsProjectionCallback` pelo aplicativo na thread correta.</span><span class="sxs-lookup"><span data-stu-id="d0939-104">The context passed into application callback, JsProjectionEnqueueCallback, from JsRT and then passed back to JsRT in the provided callback, `JsProjectionCallback`, by the application on the correct thread.</span></span>  
  
## <span data-ttu-id="d0939-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0939-105">Syntax</span></span>  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## <span data-ttu-id="d0939-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0939-106">Remarks</span></span>  
 <span data-ttu-id="d0939-107">Requer chamadas `JsSetProjectionEnqueueCallback` para receber chamadas de retorno.</span><span class="sxs-lookup"><span data-stu-id="d0939-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
 <span data-ttu-id="d0939-108">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="d0939-108">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="d0939-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0939-109">Requirements</span></span>  
 <span data-ttu-id="d0939-110">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d0939-110">jsrt.h</span></span>  
  
## <span data-ttu-id="d0939-111">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d0939-111">See Also</span></span>  
 [<span data-ttu-id="d0939-112">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d0939-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)