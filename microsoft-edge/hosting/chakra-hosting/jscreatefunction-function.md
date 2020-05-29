---
description: Cria uma nova função JavaScript.
title: Função JsCreateFunction | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateFunction
helpviewer_keywords:
- JsCreateFunction function
ms.assetid: b298a96a-5ef7-4203-a8c8-55f9bfc6d2bb
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 22585afcb379c281eda621c3b233ccf4bc278ad1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561097"
---
# <span data-ttu-id="bb946-103">Função JsCreateFunction</span><span class="sxs-lookup"><span data-stu-id="bb946-103">JsCreateFunction Function</span></span>
<span data-ttu-id="bb946-104">Cria uma nova função JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bb946-104">Creates a new JavaScript function.</span></span>
  
## <span data-ttu-id="bb946-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb946-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateFunction(  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="bb946-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb946-106">Parameters</span></span>  
 `nativeFunction`  
 <span data-ttu-id="bb946-107">O método a ser chamado quando a função é invocada.</span><span class="sxs-lookup"><span data-stu-id="bb946-107">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="bb946-108">Estado fornecido pelo usuário que será devolvido ao retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="bb946-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="bb946-109">O novo objeto function.</span><span class="sxs-lookup"><span data-stu-id="bb946-109">The new function object.</span></span>  
  
## <span data-ttu-id="bb946-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bb946-110">Return Value</span></span>  
 <span data-ttu-id="bb946-111">O resultado da chamada, se houver.</span><span class="sxs-lookup"><span data-stu-id="bb946-111">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="bb946-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb946-112">Remarks</span></span>  
 <span data-ttu-id="bb946-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="bb946-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bb946-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb946-114">Requirements</span></span>  
 <span data-ttu-id="bb946-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bb946-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bb946-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bb946-116">See Also</span></span>  
 [<span data-ttu-id="bb946-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bb946-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)