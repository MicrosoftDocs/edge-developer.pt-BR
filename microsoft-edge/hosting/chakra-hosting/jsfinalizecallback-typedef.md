---
description: Um retorno de chamada de finalizador.
title: Typedef JsFinalizeCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: aa7a0269-b9d4-4717-97ac-8da7eb6ced15
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d2ee2c2c11e85094010cd15be59aa7ac587b614f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562198"
---
# <span data-ttu-id="860c4-103">Typedef JsFinalizeCallback</span><span class="sxs-lookup"><span data-stu-id="860c4-103">JsFinalizeCallback Typedef</span></span>
<span data-ttu-id="860c4-104">Um retorno de chamada de finalizador.</span><span class="sxs-lookup"><span data-stu-id="860c4-104">A finalizer callback.</span></span>  
  
## <span data-ttu-id="860c4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="860c4-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsFinalizeCallback)(  
   _In_opt_ void *data  
);  
```  
  
#### <span data-ttu-id="860c4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="860c4-106">Parameters</span></span>  
 <span data-ttu-id="860c4-107">data</span><span class="sxs-lookup"><span data-stu-id="860c4-107">data</span></span>  
 <span data-ttu-id="860c4-108">Os dados externos que foram passados durante a criação do objeto sendo finalizado.</span><span class="sxs-lookup"><span data-stu-id="860c4-108">The external data that was passed in when creating the object being finalized.</span></span>  
  
## <span data-ttu-id="860c4-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="860c4-109">Requirements</span></span>  
 <span data-ttu-id="860c4-110">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="860c4-110">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="860c4-111">Consulte também</span><span class="sxs-lookup"><span data-stu-id="860c4-111">See Also</span></span>  
 [<span data-ttu-id="860c4-112">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="860c4-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)