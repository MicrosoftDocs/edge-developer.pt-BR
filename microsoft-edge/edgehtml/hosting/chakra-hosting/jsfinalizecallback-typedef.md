---
description: Um retorno de chamada de finalizador.
title: Typedef JsFinalizeCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: aa7a0269-b9d4-4717-97ac-8da7eb6ced15
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 794edbb3a61c8c213c0908740ed0a867488a2c6d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231555"
---
# <span data-ttu-id="5c947-103">Typedef JsFinalizeCallback</span><span class="sxs-lookup"><span data-stu-id="5c947-103">JsFinalizeCallback Typedef</span></span>

<span data-ttu-id="5c947-104">Um retorno de chamada de finalizador.</span><span class="sxs-lookup"><span data-stu-id="5c947-104">A finalizer callback.</span></span>  
  
## <span data-ttu-id="5c947-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c947-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsFinalizeCallback)(  
   _In_opt_ void *data  
);  
```  
  
#### <span data-ttu-id="5c947-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c947-106">Parameters</span></span>  
 <span data-ttu-id="5c947-107">data</span><span class="sxs-lookup"><span data-stu-id="5c947-107">data</span></span>  
 <span data-ttu-id="5c947-108">Os dados externos que foram passados durante a criação do objeto sendo finalizado.</span><span class="sxs-lookup"><span data-stu-id="5c947-108">The external data that was passed in when creating the object being finalized.</span></span>  
  
## <span data-ttu-id="5c947-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c947-109">Requirements</span></span>  
 <span data-ttu-id="5c947-110">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5c947-110">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5c947-111">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5c947-111">See Also</span></span>  
 [<span data-ttu-id="5c947-112">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5c947-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
