---
description: Um retorno de chamada chamado antes da coleta.
title: Typedef JsBeforeCollectCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 58bece47-4e6d-49e7-a93d-b6a8f9928b41
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 17f279c2d2ffcc8d02819994dddebfc22baa4cab
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561132"
---
# <span data-ttu-id="df5f7-103">Typedef JsBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="df5f7-103">JsBeforeCollectCallback Typedef</span></span>
<span data-ttu-id="df5f7-104">Um retorno de chamada chamado antes da coleta.</span><span class="sxs-lookup"><span data-stu-id="df5f7-104">A callback called before collection.</span></span>  
  
## <span data-ttu-id="df5f7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df5f7-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBeforeCollectCallback)(  
_In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="df5f7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df5f7-106">Parameters</span></span>  
 <span data-ttu-id="df5f7-107">callbackstate</span><span class="sxs-lookup"><span data-stu-id="df5f7-107">callbackState</span></span>  
 <span data-ttu-id="df5f7-108">O estado passado para JsSetBeforeCollectCallback.</span><span class="sxs-lookup"><span data-stu-id="df5f7-108">The state passed to JsSetBeforeCollectCallback.</span></span>  
  
## <span data-ttu-id="df5f7-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="df5f7-109">Remarks</span></span>  
 <span data-ttu-id="df5f7-110">Use JsSetBeforeCollectCallback para registrar esse retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="df5f7-110">Use JsSetBeforeCollectCallback to register this callback.</span></span>  
  
## <span data-ttu-id="df5f7-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df5f7-111">Requirements</span></span>  
 <span data-ttu-id="df5f7-112">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="df5f7-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="df5f7-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="df5f7-113">See Also</span></span>  
 [<span data-ttu-id="df5f7-114">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="df5f7-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)