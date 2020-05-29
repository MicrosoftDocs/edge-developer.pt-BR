---
description: Obtém o objeto global no contexto do script atual.
title: Função JsGetGlobalObject | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetGlobalObject
helpviewer_keywords:
- JsGetGlobalObject function
ms.assetid: d3e91e64-1ca3-4d2b-aada-725ded0fd0b1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9f8b540485e75ef80d42ba66f031b3e827b475fa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561053"
---
# <span data-ttu-id="fac7f-103">Função JsGetGlobalObject</span><span class="sxs-lookup"><span data-stu-id="fac7f-103">JsGetGlobalObject Function</span></span>
<span data-ttu-id="fac7f-104">Obtém o objeto global no contexto do script atual.</span><span class="sxs-lookup"><span data-stu-id="fac7f-104">Gets the global object in the current script context.</span></span>  
  
## <span data-ttu-id="fac7f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fac7f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetGlobalObject(  
   _Out_ JsValueRef *globalObject  
);  
```  
  
#### <span data-ttu-id="fac7f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fac7f-106">Parameters</span></span>  
 `globalObject`  
 <span data-ttu-id="fac7f-107">O objeto global.</span><span class="sxs-lookup"><span data-stu-id="fac7f-107">The global object.</span></span>  
  
## <span data-ttu-id="fac7f-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fac7f-108">Return Value</span></span>  
 <span data-ttu-id="fac7f-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="fac7f-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fac7f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fac7f-110">Remarks</span></span>  
 <span data-ttu-id="fac7f-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="fac7f-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="fac7f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fac7f-112">Requirements</span></span>  
 <span data-ttu-id="fac7f-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fac7f-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fac7f-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fac7f-114">See Also</span></span>  
 [<span data-ttu-id="fac7f-115">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fac7f-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)