---
description: Cria uma nova função JavaScript.
title: Função JsCreateFunction | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateFunction
helpviewer_keywords:
- JsCreateFunction function
ms.assetid: b298a96a-5ef7-4203-a8c8-55f9bfc6d2bb
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f7e67e86e6d8055664bfb1b58e6d5653f6d75d1b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231781"
---
# <span data-ttu-id="93c53-103">Função JsCreateFunction</span><span class="sxs-lookup"><span data-stu-id="93c53-103">JsCreateFunction Function</span></span>

<span data-ttu-id="93c53-104">Cria uma nova função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="93c53-104">Creates a new JavaScript function.</span></span>
  
## <span data-ttu-id="93c53-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93c53-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateFunction(  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="93c53-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93c53-106">Parameters</span></span>  
 `nativeFunction`  
 <span data-ttu-id="93c53-107">O método a ser chamado quando a função é invocada.</span><span class="sxs-lookup"><span data-stu-id="93c53-107">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="93c53-108">Estado fornecido pelo usuário que será devolvido ao retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="93c53-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="93c53-109">O novo objeto function.</span><span class="sxs-lookup"><span data-stu-id="93c53-109">The new function object.</span></span>  
  
## <span data-ttu-id="93c53-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="93c53-110">Return Value</span></span>  
 <span data-ttu-id="93c53-111">O resultado da chamada, se houver.</span><span class="sxs-lookup"><span data-stu-id="93c53-111">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="93c53-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="93c53-112">Remarks</span></span>  
 <span data-ttu-id="93c53-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="93c53-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="93c53-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93c53-114">Requirements</span></span>  
 <span data-ttu-id="93c53-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="93c53-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="93c53-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="93c53-116">See Also</span></span>  
 [<span data-ttu-id="93c53-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="93c53-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
