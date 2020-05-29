---
description: Determina se o tempo de execução do contexto atual está em um estado de exceção.
title: Função JsHasException | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 25ddb8f9cc407dd414a6cd2210c315eb4dd7b141
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562163"
---
# <span data-ttu-id="444c0-103">Função JsHasException</span><span class="sxs-lookup"><span data-stu-id="444c0-103">JsHasException Function</span></span>
<span data-ttu-id="444c0-104">Determina se o tempo de execução do contexto atual está em um estado de exceção.</span><span class="sxs-lookup"><span data-stu-id="444c0-104">Determines whether the runtime of the current context is in an exception state.</span></span>  
  
## <span data-ttu-id="444c0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="444c0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasException(  
   _Out_ bool *hasException  
);  
```  
  
#### <span data-ttu-id="444c0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="444c0-106">Parameters</span></span>  
 `hasException`  
 <span data-ttu-id="444c0-107">Se o tempo de execução do contexto atual está no estado de exceção.</span><span class="sxs-lookup"><span data-stu-id="444c0-107">Whether the runtime of the current context is in the exception state.</span></span>  
  
## <span data-ttu-id="444c0-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="444c0-108">Return Value</span></span>  
 <span data-ttu-id="444c0-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="444c0-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="444c0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="444c0-110">Remarks</span></span>  
 <span data-ttu-id="444c0-111">Se uma chamada no tempo de execução resulta em uma exceção (como resultado da execução de um script ou devido a uma falha de conversão), o tempo de execução é colocado em um "estado de exceção".</span><span class="sxs-lookup"><span data-stu-id="444c0-111">If a call into the runtime results in an exception (either as the result of running a script or due to something like a conversion failure), the runtime is placed into an "exception state."</span></span> <span data-ttu-id="444c0-112">Todas as chamadas em qualquer contexto criado pelo tempo de execução (exceto para APIs de exceção) falharão `JsErrorInExceptionState` até que a exceção seja desmarcada.</span><span class="sxs-lookup"><span data-stu-id="444c0-112">All calls into any context created by the runtime (except for the exception APIs) will fail with `JsErrorInExceptionState` until the exception is cleared.</span></span>  
  
 <span data-ttu-id="444c0-113">Se o tempo de execução do contexto atual estiver no estado de exceção quando um retorno de chamada retornar ao mecanismo, o mecanismo relançará automaticamente a exceção.</span><span class="sxs-lookup"><span data-stu-id="444c0-113">If the runtime of the current context is in the exception state when a callback returns into the engine, the engine will automatically rethrow the exception.</span></span>  
  
 <span data-ttu-id="444c0-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="444c0-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="444c0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="444c0-115">Requirements</span></span>  
 <span data-ttu-id="444c0-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="444c0-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="444c0-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="444c0-117">See Also</span></span>  
 [<span data-ttu-id="444c0-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="444c0-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)