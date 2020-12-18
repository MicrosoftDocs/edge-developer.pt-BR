---
description: O contexto passado para o retorno de chamada do aplicativo, JsProjectionEnqueueCallback, de JsRT e, em seguida, passado de volta para JsRT no retorno de chamada fornecido, `JsProjectionCallback` pelo aplicativo na thread correta.
title: Typedef JsProjectionCallbackContext | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7742b0186a49e99f2738b81357b9e55cfe00042b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231747"
---
# <span data-ttu-id="24d72-103">Typedef JsProjectionCallbackContext</span><span class="sxs-lookup"><span data-stu-id="24d72-103">JsProjectionCallbackContext Typedef</span></span>

<span data-ttu-id="24d72-104">O contexto passado para o retorno de chamada do aplicativo, JsProjectionEnqueueCallback, de JsRT e, em seguida, passado de volta para JsRT no retorno de chamada fornecido, `JsProjectionCallback` pelo aplicativo na thread correta.</span><span class="sxs-lookup"><span data-stu-id="24d72-104">The context passed into application callback, JsProjectionEnqueueCallback, from JsRT and then passed back to JsRT in the provided callback, `JsProjectionCallback`, by the application on the correct thread.</span></span>  
  
## <span data-ttu-id="24d72-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24d72-105">Syntax</span></span>  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## <span data-ttu-id="24d72-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="24d72-106">Remarks</span></span>  
 <span data-ttu-id="24d72-107">Requer chamadas `JsSetProjectionEnqueueCallback` para receber chamadas de retorno.</span><span class="sxs-lookup"><span data-stu-id="24d72-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
 <span data-ttu-id="24d72-108">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="24d72-108">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="24d72-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24d72-109">Requirements</span></span>  
 <span data-ttu-id="24d72-110">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="24d72-110">jsrt.h</span></span>  
  
## <span data-ttu-id="24d72-111">Consulte também</span><span class="sxs-lookup"><span data-stu-id="24d72-111">See Also</span></span>  
 [<span data-ttu-id="24d72-112">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="24d72-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
