---
description: Retorna um valor que indica se a execução do script está desabilitada no tempo de execução.
title: Função JsIsRuntimeExecutionDisabled | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0ce59c77525abdb2dd6cac71dde1378264395e79
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231246"
---
# <span data-ttu-id="247bc-103">Função JsIsRuntimeExecutionDisabled</span><span class="sxs-lookup"><span data-stu-id="247bc-103">JsIsRuntimeExecutionDisabled Function</span></span>

<span data-ttu-id="247bc-104">Retorna um valor que indica se a execução do script está desabilitada no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="247bc-104">Returns a value that indicates whether script execution is disabled in the runtime.</span></span>  
  
## <span data-ttu-id="247bc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="247bc-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsRuntimeExecutionDisabled(    _In_ JsRuntimeHandle runtime,    _Out_ bool *isDisabled);  
```  
  
#### <span data-ttu-id="247bc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="247bc-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="247bc-107">Especifica o tempo de execução para verificar se a execução está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="247bc-107">Specifies the runtime to check if execution is disabled.</span></span>  
  
 `isDisabled`  
 `true` <span data-ttu-id="247bc-108">se a execução estiver desabilitada, `false` caso contrário.</span><span class="sxs-lookup"><span data-stu-id="247bc-108">if execution is disabled, `false` otherwise.</span></span>  
  
## <span data-ttu-id="247bc-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="247bc-109">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="247bc-110">se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="247bc-110">if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="247bc-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="247bc-111">Requirements</span></span>  
 <span data-ttu-id="247bc-112">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="247bc-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="247bc-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="247bc-113">See Also</span></span>  
 [<span data-ttu-id="247bc-114">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="247bc-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
