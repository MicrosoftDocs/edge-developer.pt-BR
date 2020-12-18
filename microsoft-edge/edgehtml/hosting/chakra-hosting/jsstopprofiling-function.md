---
description: Interrompe a criação de perfil no contexto atual.
title: Função JsStopProfiling | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 02c42afda7e61d71b90a9a1a71aa71cc53584ff8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231615"
---
# <span data-ttu-id="1336c-103">Função JsStopProfiling</span><span class="sxs-lookup"><span data-stu-id="1336c-103">JsStopProfiling Function</span></span>

<span data-ttu-id="1336c-104">Interrompe a criação de perfil no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="1336c-104">Stops profiling in the current context.</span></span>  
  
## <span data-ttu-id="1336c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1336c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStopProfiling(  
   _In_ HRESULT reason  
);  
```  
  
#### <span data-ttu-id="1336c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1336c-106">Parameters</span></span>  
 `reason`  
 <span data-ttu-id="1336c-107">O motivo para interromper a criação de perfil para passar para o retorno de chamada do gerador de perfil.</span><span class="sxs-lookup"><span data-stu-id="1336c-107">The reason for stopping profiling to pass to the profiler callback.</span></span>  
  
## <span data-ttu-id="1336c-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1336c-108">Return Value</span></span>  
 <span data-ttu-id="1336c-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="1336c-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1336c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1336c-110">Remarks</span></span>  
 <span data-ttu-id="1336c-111">Não retornará um erro se o profiling não tiver começado.</span><span class="sxs-lookup"><span data-stu-id="1336c-111">Will not return an error if profiling has not started.</span></span>  
  
 <span data-ttu-id="1336c-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="1336c-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="1336c-113">Essa API tem suporte em aplicativos de área de trabalho, mas não é compatível com aplicativos da loja.</span><span class="sxs-lookup"><span data-stu-id="1336c-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="1336c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1336c-114">Requirements</span></span>  
 <span data-ttu-id="1336c-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1336c-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1336c-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1336c-116">See Also</span></span>  
 [<span data-ttu-id="1336c-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1336c-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
