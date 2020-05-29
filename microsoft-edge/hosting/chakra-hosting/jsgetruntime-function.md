---
description: Obtém o tempo de execução ao qual o contexto pertence.
title: Função JsGetRuntime | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntime
helpviewer_keywords:
- JsGetRuntime function
ms.assetid: 5b62e940-a885-405a-9fdd-0495fb391b95
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6eeb132dd35fcb5104828bef8e8f27334a5f34e4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561045"
---
# <span data-ttu-id="bbbab-103">Função JsGetRuntime</span><span class="sxs-lookup"><span data-stu-id="bbbab-103">JsGetRuntime Function</span></span>
<span data-ttu-id="bbbab-104">Obtém o tempo de execução ao qual o contexto pertence.</span><span class="sxs-lookup"><span data-stu-id="bbbab-104">Gets the runtime that the context belongs to.</span></span>  
  
## <span data-ttu-id="bbbab-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbbab-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntime(  
   _In_ JsContextRef context,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### <span data-ttu-id="bbbab-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbbab-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="bbbab-107">O contexto do qual obter o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="bbbab-107">The context to get the runtime from.</span></span>  
  
 `runtime`  
 <span data-ttu-id="bbbab-108">O tempo de execução ao qual o contexto pertence.</span><span class="sxs-lookup"><span data-stu-id="bbbab-108">The runtime the context belongs to.</span></span>  
  
## <span data-ttu-id="bbbab-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bbbab-109">Return Value</span></span>  
 <span data-ttu-id="bbbab-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="bbbab-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bbbab-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbbab-111">Requirements</span></span>  
 <span data-ttu-id="bbbab-112">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bbbab-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bbbab-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bbbab-113">See Also</span></span>  
 [<span data-ttu-id="bbbab-114">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bbbab-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)