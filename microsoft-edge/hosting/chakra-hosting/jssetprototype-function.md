---
description: Define o protótipo de um objeto.
title: Função JsSetPrototype | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 88e1e421-4ae5-4e3b-b377-19256cc80e9f
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 625269c5f9f459a5c7eecb6cfc31cb85fc24214b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562020"
---
# <span data-ttu-id="0900e-103">Função JsSetPrototype</span><span class="sxs-lookup"><span data-stu-id="0900e-103">JsSetPrototype Function</span></span>
<span data-ttu-id="0900e-104">Define o protótipo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="0900e-104">Sets the prototype of an object.</span></span>  
  
## <span data-ttu-id="0900e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0900e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPrototype(  
   _In_ JsValueRef object,  
   _In_ JsValueRef prototypeObject  
);  
```  
  
#### <span data-ttu-id="0900e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0900e-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="0900e-107">O objeto cujo protótipo deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="0900e-107">The object whose prototype is to be changed.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="0900e-108">O novo protótipo do objeto.</span><span class="sxs-lookup"><span data-stu-id="0900e-108">The object's new prototype.</span></span>  
  
## <span data-ttu-id="0900e-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0900e-109">Return Value</span></span>  
 <span data-ttu-id="0900e-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="0900e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0900e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0900e-111">Remarks</span></span>  
 <span data-ttu-id="0900e-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="0900e-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0900e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0900e-113">Requirements</span></span>  
 <span data-ttu-id="0900e-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0900e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0900e-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0900e-115">See Also</span></span>  
 [<span data-ttu-id="0900e-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0900e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)