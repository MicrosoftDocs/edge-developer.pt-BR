---
description: Executa uma coleta de lixo completa.
title: Função JsCollectGarbage | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCollectGarbage
helpviewer_keywords:
- JsCollectGarbage function
ms.assetid: 995c79a5-6e18-45be-81ff-2a5d3348edb8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1702ad960a0a2f366e97b8a994abd0700cec50e7
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561125"
---
# <span data-ttu-id="12e41-103">Função JsCollectGarbage</span><span class="sxs-lookup"><span data-stu-id="12e41-103">JsCollectGarbage Function</span></span>
<span data-ttu-id="12e41-104">Executa uma coleta de lixo completa.</span><span class="sxs-lookup"><span data-stu-id="12e41-104">Performs a full garbage collection.</span></span>  
  
## <span data-ttu-id="12e41-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12e41-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCollectGarbage(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="12e41-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12e41-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="12e41-107">O tempo de execução no qual a coleta de lixo será realizada.</span><span class="sxs-lookup"><span data-stu-id="12e41-107">The runtime in which the garbage collection will be performed.</span></span>  
  
## <span data-ttu-id="12e41-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="12e41-108">Return Value</span></span>  
 <span data-ttu-id="12e41-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="12e41-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="12e41-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12e41-110">Requirements</span></span>  
 <span data-ttu-id="12e41-111">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="12e41-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="12e41-112">Consulte também</span><span class="sxs-lookup"><span data-stu-id="12e41-112">See Also</span></span>  
 [<span data-ttu-id="12e41-113">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="12e41-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)