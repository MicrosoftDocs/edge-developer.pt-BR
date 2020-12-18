---
description: Cria uma nova função JavaScript com Name.
title: Função JsCreateNamedFunction | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 72f40d06-ab82-4fed-a632-68af6b4126c2
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b54add359422a9312a0ded641051fd04585f3d7e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231562"
---
# <span data-ttu-id="f7d21-103">Função JsCreateNamedFunction</span><span class="sxs-lookup"><span data-stu-id="f7d21-103">JsCreateNamedFunction Function</span></span>

<span data-ttu-id="f7d21-104">Cria uma nova função JavaScript com Name.</span><span class="sxs-lookup"><span data-stu-id="f7d21-104">Creates a new JavaScript function with name.</span></span>
  
## <span data-ttu-id="f7d21-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7d21-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateNamedFunction(  
   _In_ JsValueRef name,  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="f7d21-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7d21-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="f7d21-107">O nome desta função que será usado para diagnóstico e propósitos de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f7d21-107">The name of this function that will be used for diagnostics and stringification purposes.</span></span>  
  
 `nativeFunction`  
 <span data-ttu-id="f7d21-108">O método a ser chamado quando a função é invocada.</span><span class="sxs-lookup"><span data-stu-id="f7d21-108">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="f7d21-109">Estado fornecido pelo usuário que será devolvido ao retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="f7d21-109">User provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="f7d21-110">O novo objeto function.</span><span class="sxs-lookup"><span data-stu-id="f7d21-110">The new function object.</span></span>  
  
## <span data-ttu-id="f7d21-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f7d21-111">Return Value</span></span>  
  
## <span data-ttu-id="f7d21-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7d21-112">Remarks</span></span>  
 <span data-ttu-id="f7d21-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="f7d21-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="f7d21-114">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f7d21-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="f7d21-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7d21-115">Requirements</span></span>  
 <span data-ttu-id="f7d21-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f7d21-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f7d21-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f7d21-117">See Also</span></span>  
 [<span data-ttu-id="f7d21-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f7d21-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
