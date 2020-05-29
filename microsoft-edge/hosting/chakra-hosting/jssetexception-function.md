---
description: Define o tempo de execução do contexto atual como um estado de exceção.
title: Função JsSetException | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 75d2895a725c622a0b46887d10154c3a0c56c7e9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562114"
---
# <span data-ttu-id="9aea3-103">Função JsSetException</span><span class="sxs-lookup"><span data-stu-id="9aea3-103">JsSetException Function</span></span>
<span data-ttu-id="9aea3-104">Define o tempo de execução do contexto atual como um estado de exceção.</span><span class="sxs-lookup"><span data-stu-id="9aea3-104">Sets the runtime of the current context to an exception state.</span></span>  
  
## <span data-ttu-id="9aea3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9aea3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetException(  
   _In_ JsValueRef exception  
);  
```  
  
#### <span data-ttu-id="9aea3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9aea3-106">Parameters</span></span>  
 `exception`  
 <span data-ttu-id="9aea3-107">A exceção JavaScript a ser definida para o tempo de execução do contexto atual.</span><span class="sxs-lookup"><span data-stu-id="9aea3-107">The JavaScript exception to set for the runtime of the current context.</span></span>  
  
## <span data-ttu-id="9aea3-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9aea3-108">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="9aea3-109">Se o mecanismo tiver sido definido como um estado de exceção, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="9aea3-109">if the engine was set into an exception state, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9aea3-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="9aea3-110">Remarks</span></span>  
 <span data-ttu-id="9aea3-111">Se o tempo de execução do contexto atual já estiver em um estado de exceção, essa API retornará `JsErrorInExceptionState` .</span><span class="sxs-lookup"><span data-stu-id="9aea3-111">If the runtime of the current context is already in an exception state, this API will return `JsErrorInExceptionState`.</span></span>  
  
 <span data-ttu-id="9aea3-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="9aea3-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9aea3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aea3-113">Requirements</span></span>  
 <span data-ttu-id="9aea3-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9aea3-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9aea3-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9aea3-115">See Also</span></span>  
 [<span data-ttu-id="9aea3-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9aea3-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)