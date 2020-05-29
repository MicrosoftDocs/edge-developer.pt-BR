---
description: Retorna o protótipo de um objeto.
title: Função JsGetPrototype | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetPrototype
helpviewer_keywords:
- JsGetPrototype function
ms.assetid: 05d743fc-103e-4a92-86f2-a063f39a2a6f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 12708634fea9e8f9fd1205514845b1cb9760ee9e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561048"
---
# <span data-ttu-id="10830-103">Função JsGetPrototype</span><span class="sxs-lookup"><span data-stu-id="10830-103">JsGetPrototype Function</span></span>
<span data-ttu-id="10830-104">Retorna o protótipo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="10830-104">Returns the prototype of an object.</span></span>  
  
## <span data-ttu-id="10830-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10830-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPrototype(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *prototypeObject  
);  
```  
  
#### <span data-ttu-id="10830-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10830-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="10830-107">O objeto cujo protótipo deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="10830-107">The object whose prototype is to be returned.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="10830-108">O protótipo do objeto.</span><span class="sxs-lookup"><span data-stu-id="10830-108">The object's prototype.</span></span>  
  
## <span data-ttu-id="10830-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="10830-109">Return Value</span></span>  
 <span data-ttu-id="10830-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="10830-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="10830-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="10830-111">Remarks</span></span>  
 <span data-ttu-id="10830-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="10830-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="10830-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10830-113">Requirements</span></span>  
 <span data-ttu-id="10830-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="10830-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="10830-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="10830-115">See Also</span></span>  
 [<span data-ttu-id="10830-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="10830-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)