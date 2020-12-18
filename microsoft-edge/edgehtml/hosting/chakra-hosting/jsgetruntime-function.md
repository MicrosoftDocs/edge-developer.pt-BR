---
description: Obtém o tempo de execução ao qual o contexto pertence.
title: Função JsGetRuntime | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntime
helpviewer_keywords:
- JsGetRuntime function
ms.assetid: 5b62e940-a885-405a-9fdd-0495fb391b95
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 49739f0cf3675a44b9fc328e3eaa7d49c6282e53
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231637"
---
# <span data-ttu-id="9af57-103">Função JsGetRuntime</span><span class="sxs-lookup"><span data-stu-id="9af57-103">JsGetRuntime Function</span></span>

<span data-ttu-id="9af57-104">Obtém o tempo de execução ao qual o contexto pertence.</span><span class="sxs-lookup"><span data-stu-id="9af57-104">Gets the runtime that the context belongs to.</span></span>  
  
## <span data-ttu-id="9af57-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9af57-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntime(  
   _In_ JsContextRef context,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### <span data-ttu-id="9af57-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9af57-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="9af57-107">O contexto do qual obter o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="9af57-107">The context to get the runtime from.</span></span>  
  
 `runtime`  
 <span data-ttu-id="9af57-108">O tempo de execução ao qual o contexto pertence.</span><span class="sxs-lookup"><span data-stu-id="9af57-108">The runtime the context belongs to.</span></span>  
  
## <span data-ttu-id="9af57-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9af57-109">Return Value</span></span>  
 <span data-ttu-id="9af57-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="9af57-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9af57-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9af57-111">Requirements</span></span>  
 <span data-ttu-id="9af57-112">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9af57-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9af57-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9af57-113">See Also</span></span>  
 [<span data-ttu-id="9af57-114">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9af57-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
