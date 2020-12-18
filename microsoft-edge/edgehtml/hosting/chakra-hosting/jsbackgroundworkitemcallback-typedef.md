---
description: Um retorno de chamada de item de trabalho em segundo plano.
title: Typedef JsBackgroundWorkItemCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d69306b334c2e0c9b27b96a5a417739ffdcd7dd7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231454"
---
# <span data-ttu-id="48d1b-103">Typedef JsBackgroundWorkItemCallback </span><span class="sxs-lookup"><span data-stu-id="48d1b-103">JsBackgroundWorkItemCallback Typedef</span></span>

<span data-ttu-id="48d1b-104">Um retorno de chamada de item de trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="48d1b-104">A background work item callback.</span></span>  
  
## <span data-ttu-id="48d1b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48d1b-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBackgroundWorkItemCallback)(  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="48d1b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48d1b-106">Parameters</span></span>  
 <span data-ttu-id="48d1b-107">callbackData</span><span class="sxs-lookup"><span data-stu-id="48d1b-107">callbackData</span></span>  
 <span data-ttu-id="48d1b-108">Argumento de dados passado para o serviço de thread.</span><span class="sxs-lookup"><span data-stu-id="48d1b-108">Data argument passed to the thread service.</span></span>  
  
## <span data-ttu-id="48d1b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="48d1b-109">Remarks</span></span>  
 <span data-ttu-id="48d1b-110">Isso é passado para o serviço de thread do host (se for fornecido) para permitir que o host invoque o retorno de chamada de item de trabalho no thread de segundo plano de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="48d1b-110">This is passed to the host's thread service (if provided) to allow the host to invoke the work item callback on the background thread of its choice.</span></span>  
  
## <span data-ttu-id="48d1b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48d1b-111">Requirements</span></span>  
 <span data-ttu-id="48d1b-112">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="48d1b-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="48d1b-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="48d1b-113">See Also</span></span>  
 [<span data-ttu-id="48d1b-114">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="48d1b-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
