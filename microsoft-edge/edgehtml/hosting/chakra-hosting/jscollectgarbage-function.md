---
description: Executa uma coleta de lixo completa.
title: Função JsCollectGarbage | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCollectGarbage
helpviewer_keywords:
- JsCollectGarbage function
ms.assetid: 995c79a5-6e18-45be-81ff-2a5d3348edb8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c551ddf119ec0aa349fcd756f6001d92dbbb0faa
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231440"
---
# <span data-ttu-id="0f012-103">Função JsCollectGarbage</span><span class="sxs-lookup"><span data-stu-id="0f012-103">JsCollectGarbage Function</span></span>

<span data-ttu-id="0f012-104">Executa uma coleta de lixo completa.</span><span class="sxs-lookup"><span data-stu-id="0f012-104">Performs a full garbage collection.</span></span>  
  
## <span data-ttu-id="0f012-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f012-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCollectGarbage(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="0f012-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f012-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="0f012-107">O tempo de execução no qual a coleta de lixo será realizada.</span><span class="sxs-lookup"><span data-stu-id="0f012-107">The runtime in which the garbage collection will be performed.</span></span>  
  
## <span data-ttu-id="0f012-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0f012-108">Return Value</span></span>  
 <span data-ttu-id="0f012-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="0f012-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0f012-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f012-110">Requirements</span></span>  
 <span data-ttu-id="0f012-111">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0f012-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0f012-112">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0f012-112">See Also</span></span>  
 [<span data-ttu-id="0f012-113">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0f012-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
