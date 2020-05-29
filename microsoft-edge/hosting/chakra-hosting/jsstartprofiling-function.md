---
description: Inicia a criação de perfil no contexto atual.
title: Função JsStartProfiling | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStartProfiling
helpviewer_keywords:
- JsStartProfiling function
ms.assetid: 638da395-42dd-4fc5-b581-819e647e887d
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 891c39305e08d214a8f06b680c7022683a9d6fe4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562002"
---
# <span data-ttu-id="b7524-103">Função JsStartProfiling</span><span class="sxs-lookup"><span data-stu-id="b7524-103">JsStartProfiling Function</span></span>
<span data-ttu-id="b7524-104">Inicia a criação de perfil no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="b7524-104">Starts profiling in the current context.</span></span>  
  
## <span data-ttu-id="b7524-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7524-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStartProfiling(  
   _In_ IActiveScriptProfilerCallback *callback,  
   _In_ PROFILER_EVENT_MASK eventMask,  
   _In_ unsigned long context  
);  
```  
  
#### <span data-ttu-id="b7524-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7524-106">Parameters</span></span>  
 `callback`  
 <span data-ttu-id="b7524-107">O retorno de chamada de perfil a ser usado.</span><span class="sxs-lookup"><span data-stu-id="b7524-107">The profiling callback to use.</span></span>  
  
 `eventMask`  
 <span data-ttu-id="b7524-108">A criação de perfil dos eventos para retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b7524-108">The profiling events to callback with.</span></span>  
  
 `context`  
 <span data-ttu-id="b7524-109">Um contexto para passar para o retorno de chamada de perfil.</span><span class="sxs-lookup"><span data-stu-id="b7524-109">A context to pass to the profiling callback.</span></span>  
  
## <span data-ttu-id="b7524-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b7524-110">Return Value</span></span>  
 <span data-ttu-id="b7524-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="b7524-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b7524-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7524-112">Remarks</span></span>  
 <span data-ttu-id="b7524-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="b7524-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="b7524-114">Essa API tem suporte em aplicativos de área de trabalho, mas não é compatível com aplicativos da loja.</span><span class="sxs-lookup"><span data-stu-id="b7524-114">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="b7524-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7524-115">Requirements</span></span>  
 <span data-ttu-id="b7524-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b7524-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b7524-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b7524-117">See Also</span></span>  
 [<span data-ttu-id="b7524-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b7524-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)