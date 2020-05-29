---
description: Cria uma nova função JavaScript com Name.
title: Função JsCreateNamedFunction | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 72f40d06-ab82-4fed-a632-68af6b4126c2
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d963fe196b8e56394e22501ed3898a0d887a3d3b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561095"
---
# <span data-ttu-id="ce08f-103">Função JsCreateNamedFunction</span><span class="sxs-lookup"><span data-stu-id="ce08f-103">JsCreateNamedFunction Function</span></span>
<span data-ttu-id="ce08f-104">Cria uma nova função JavaScript com Name.</span><span class="sxs-lookup"><span data-stu-id="ce08f-104">Creates a new JavaScript function with name.</span></span>
  
## <span data-ttu-id="ce08f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce08f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateNamedFunction(  
   _In_ JsValueRef name,  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="ce08f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce08f-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="ce08f-107">O nome desta função que será usado para diagnóstico e propósitos de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ce08f-107">The name of this function that will be used for diagnostics and stringification purposes.</span></span>  
  
 `nativeFunction`  
 <span data-ttu-id="ce08f-108">O método a ser chamado quando a função é invocada.</span><span class="sxs-lookup"><span data-stu-id="ce08f-108">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="ce08f-109">Estado fornecido pelo usuário que será devolvido ao retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="ce08f-109">User provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="ce08f-110">O novo objeto function.</span><span class="sxs-lookup"><span data-stu-id="ce08f-110">The new function object.</span></span>  
  
## <span data-ttu-id="ce08f-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ce08f-111">Return Value</span></span>  
  
## <span data-ttu-id="ce08f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce08f-112">Remarks</span></span>  
 <span data-ttu-id="ce08f-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="ce08f-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="ce08f-114">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ce08f-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="ce08f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce08f-115">Requirements</span></span>  
 <span data-ttu-id="ce08f-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ce08f-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ce08f-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ce08f-117">See Also</span></span>  
 [<span data-ttu-id="ce08f-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ce08f-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)