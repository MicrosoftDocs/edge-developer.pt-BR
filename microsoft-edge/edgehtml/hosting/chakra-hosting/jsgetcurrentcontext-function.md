---
description: Obtém o contexto do script atual no thread.
title: Função JsGetCurrentContext | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetCurrentContext
helpviewer_keywords:
- JsGetCurrentContext function
ms.assetid: dd5fe0fa-d1e5-4af6-809e-e655a27519b5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a43b9a6d4413ef1dc1b66321d6078aef84a0645f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231674"
---
# <span data-ttu-id="b5717-103">Função JsGetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="b5717-103">JsGetCurrentContext Function</span></span>

<span data-ttu-id="b5717-104">Obtém o contexto do script atual no thread.</span><span class="sxs-lookup"><span data-stu-id="b5717-104">Gets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="b5717-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5717-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetCurrentContext(  
   _Out_ JsContextRef *currentContext  
);  
```  
  
#### <span data-ttu-id="b5717-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5717-106">Parameters</span></span>  
 `currentContext`  
 <span data-ttu-id="b5717-107">O contexto de script atual no thread; nulo se não houver contexto de script atual.</span><span class="sxs-lookup"><span data-stu-id="b5717-107">The current script context on the thread, null if there is no current script context.</span></span>  
  
## <span data-ttu-id="b5717-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b5717-108">Return Value</span></span>  
 <span data-ttu-id="b5717-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="b5717-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b5717-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5717-110">Requirements</span></span>  
 <span data-ttu-id="b5717-111">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b5717-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b5717-112">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b5717-112">See Also</span></span>  
 [<span data-ttu-id="b5717-113">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b5717-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
