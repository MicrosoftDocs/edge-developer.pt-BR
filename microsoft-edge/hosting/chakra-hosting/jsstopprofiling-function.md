---
description: Interrompe a criação de perfil no contexto atual.
title: Função JsStopProfiling | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9d021c7c9849d20283a39d6ecffc89c5b2ea0db0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562001"
---
# <span data-ttu-id="19173-103">Função JsStopProfiling</span><span class="sxs-lookup"><span data-stu-id="19173-103">JsStopProfiling Function</span></span>
<span data-ttu-id="19173-104">Interrompe a criação de perfil no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="19173-104">Stops profiling in the current context.</span></span>  
  
## <span data-ttu-id="19173-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19173-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStopProfiling(  
   _In_ HRESULT reason  
);  
```  
  
#### <span data-ttu-id="19173-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19173-106">Parameters</span></span>  
 `reason`  
 <span data-ttu-id="19173-107">O motivo para interromper a criação de perfil para passar para o retorno de chamada do gerador de perfil.</span><span class="sxs-lookup"><span data-stu-id="19173-107">The reason for stopping profiling to pass to the profiler callback.</span></span>  
  
## <span data-ttu-id="19173-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="19173-108">Return Value</span></span>  
 <span data-ttu-id="19173-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="19173-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="19173-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="19173-110">Remarks</span></span>  
 <span data-ttu-id="19173-111">Não retornará um erro se o profiling não tiver começado.</span><span class="sxs-lookup"><span data-stu-id="19173-111">Will not return an error if profiling has not started.</span></span>  
  
 <span data-ttu-id="19173-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="19173-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="19173-113">Essa API tem suporte em aplicativos de área de trabalho, mas não é compatível com aplicativos da loja.</span><span class="sxs-lookup"><span data-stu-id="19173-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="19173-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19173-114">Requirements</span></span>  
 <span data-ttu-id="19173-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="19173-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="19173-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="19173-116">See Also</span></span>  
 [<span data-ttu-id="19173-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="19173-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)