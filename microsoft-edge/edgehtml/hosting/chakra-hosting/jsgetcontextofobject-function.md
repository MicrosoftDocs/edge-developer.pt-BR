---
description: Obtém o contexto de script ao qual o objeto pertence.
title: Função JsGetContextOfObject | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: cea6cdcd-790f-455c-af04-026af8ae2eb7
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9085f9156e4e0ca9e952fe51447185239082f975
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231679"
---
# <span data-ttu-id="25f9e-103">Função JsGetContextOfObject</span><span class="sxs-lookup"><span data-stu-id="25f9e-103">JsGetContextOfObject Function</span></span>

<span data-ttu-id="25f9e-104">Obtém o contexto de script ao qual o objeto pertence.</span><span class="sxs-lookup"><span data-stu-id="25f9e-104">Gets the script context that the object belongs to.</span></span>  
  
## <span data-ttu-id="25f9e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25f9e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextOfObject(  
  _In_ JsValueRef object,  
  _Out_ JsContextRef *context  
);  
```  
  
#### <span data-ttu-id="25f9e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25f9e-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="25f9e-107">O objeto do qual o contexto será obtido.</span><span class="sxs-lookup"><span data-stu-id="25f9e-107">The object to get the context from.</span></span>  
  
 `context`  
 <span data-ttu-id="25f9e-108">O contexto ao qual o objeto pertence.</span><span class="sxs-lookup"><span data-stu-id="25f9e-108">The context the object belongs to.</span></span>  
  
## <span data-ttu-id="25f9e-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="25f9e-109">Return Value</span></span>  
 <span data-ttu-id="25f9e-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="25f9e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="25f9e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="25f9e-111">Remarks</span></span>  
 <span data-ttu-id="25f9e-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="25f9e-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="25f9e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25f9e-113">Requirements</span></span>  
 <span data-ttu-id="25f9e-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="25f9e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="25f9e-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="25f9e-115">See Also</span></span>  
 [<span data-ttu-id="25f9e-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="25f9e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
