---
description: Um retorno de chamada chamado antes da coleta.
title: Typedef JsBeforeCollectCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 58bece47-4e6d-49e7-a93d-b6a8f9928b41
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 23ed386a6a28d356aa80cf85650a981d4836a6b6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231445"
---
# <span data-ttu-id="d3475-103">Typedef JsBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="d3475-103">JsBeforeCollectCallback Typedef</span></span>

<span data-ttu-id="d3475-104">Um retorno de chamada chamado antes da coleta.</span><span class="sxs-lookup"><span data-stu-id="d3475-104">A callback called before collection.</span></span>  
  
## <span data-ttu-id="d3475-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3475-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBeforeCollectCallback)(  
_In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="d3475-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3475-106">Parameters</span></span>  
 <span data-ttu-id="d3475-107">callbackstate</span><span class="sxs-lookup"><span data-stu-id="d3475-107">callbackState</span></span>  
 <span data-ttu-id="d3475-108">O estado passado para JsSetBeforeCollectCallback.</span><span class="sxs-lookup"><span data-stu-id="d3475-108">The state passed to JsSetBeforeCollectCallback.</span></span>  
  
## <span data-ttu-id="d3475-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3475-109">Remarks</span></span>  
 <span data-ttu-id="d3475-110">Use JsSetBeforeCollectCallback para registrar esse retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="d3475-110">Use JsSetBeforeCollectCallback to register this callback.</span></span>  
  
## <span data-ttu-id="d3475-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3475-111">Requirements</span></span>  
 <span data-ttu-id="d3475-112">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d3475-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d3475-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d3475-113">See Also</span></span>  
 [<span data-ttu-id="d3475-114">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d3475-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
