---
description: Obtém o objeto global no contexto do script atual.
title: Função JsGetGlobalObject | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetGlobalObject
helpviewer_keywords:
- JsGetGlobalObject function
ms.assetid: d3e91e64-1ca3-4d2b-aada-725ded0fd0b1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cda960710180c135b99abd359d0cc76776ff0225
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231666"
---
# <span data-ttu-id="12013-103">Função JsGetGlobalObject</span><span class="sxs-lookup"><span data-stu-id="12013-103">JsGetGlobalObject Function</span></span>

<span data-ttu-id="12013-104">Obtém o objeto global no contexto do script atual.</span><span class="sxs-lookup"><span data-stu-id="12013-104">Gets the global object in the current script context.</span></span>  
  
## <span data-ttu-id="12013-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12013-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetGlobalObject(  
   _Out_ JsValueRef *globalObject  
);  
```  
  
#### <span data-ttu-id="12013-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12013-106">Parameters</span></span>  
 `globalObject`  
 <span data-ttu-id="12013-107">O objeto global.</span><span class="sxs-lookup"><span data-stu-id="12013-107">The global object.</span></span>  
  
## <span data-ttu-id="12013-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="12013-108">Return Value</span></span>  
 <span data-ttu-id="12013-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="12013-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="12013-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="12013-110">Remarks</span></span>  
 <span data-ttu-id="12013-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="12013-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="12013-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12013-112">Requirements</span></span>  
 <span data-ttu-id="12013-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="12013-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="12013-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="12013-114">See Also</span></span>  
 [<span data-ttu-id="12013-115">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="12013-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
