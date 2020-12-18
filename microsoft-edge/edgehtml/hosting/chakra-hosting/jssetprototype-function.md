---
description: Define o protótipo de um objeto.
title: Função JsSetPrototype | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 88e1e421-4ae5-4e3b-b377-19256cc80e9f
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 860a7b8d85e043c87d554e09de50d0cb642b273a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231406"
---
# <span data-ttu-id="8f275-103">Função JsSetPrototype</span><span class="sxs-lookup"><span data-stu-id="8f275-103">JsSetPrototype Function</span></span>

<span data-ttu-id="8f275-104">Define o protótipo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="8f275-104">Sets the prototype of an object.</span></span>  
  
## <span data-ttu-id="8f275-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f275-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPrototype(  
   _In_ JsValueRef object,  
   _In_ JsValueRef prototypeObject  
);  
```  
  
#### <span data-ttu-id="8f275-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f275-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="8f275-107">O objeto cujo protótipo deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="8f275-107">The object whose prototype is to be changed.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="8f275-108">O novo protótipo do objeto.</span><span class="sxs-lookup"><span data-stu-id="8f275-108">The object's new prototype.</span></span>  
  
## <span data-ttu-id="8f275-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8f275-109">Return Value</span></span>  
 <span data-ttu-id="8f275-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="8f275-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8f275-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f275-111">Remarks</span></span>  
 <span data-ttu-id="8f275-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="8f275-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="8f275-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f275-113">Requirements</span></span>  
 <span data-ttu-id="8f275-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8f275-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8f275-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8f275-115">See Also</span></span>  
 [<span data-ttu-id="8f275-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8f275-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
