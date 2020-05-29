---
description: Comparar dois valores JavaScript para igualdade estrita.
title: Função JsStrictEquals | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStrictEquals
helpviewer_keywords:
- JsStrictEquals function
ms.assetid: b35bc655-7ff8-496a-b678-8950bb976047
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b7f2b7a66c32428100f0c0d0f9db6150559ed7a2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562099"
---
# <span data-ttu-id="be725-103">Função JsStrictEquals</span><span class="sxs-lookup"><span data-stu-id="be725-103">JsStrictEquals Function</span></span>
<span data-ttu-id="be725-104">Comparar dois valores JavaScript para igualdade estrita.</span><span class="sxs-lookup"><span data-stu-id="be725-104">Compare two JavaScript values for strict equality.</span></span>  
  
## <span data-ttu-id="be725-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be725-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStrictEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="be725-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be725-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="be725-107">O primeiro objeto a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="be725-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="be725-108">O segundo objeto a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="be725-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="be725-109">Se os valores são estritamente iguais.</span><span class="sxs-lookup"><span data-stu-id="be725-109">Whether the values are strictly equal.</span></span>  
  
## <span data-ttu-id="be725-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="be725-110">Return Value</span></span>  
 <span data-ttu-id="be725-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="be725-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="be725-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="be725-112">Remarks</span></span>  
 <span data-ttu-id="be725-113">Esta função é equivalente à `===` operadora em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="be725-113">This function is equivalent to the `===` operator in Javascript.</span></span>  
  
 <span data-ttu-id="be725-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="be725-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="be725-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be725-115">Requirements</span></span>  
 <span data-ttu-id="be725-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="be725-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="be725-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="be725-117">See Also</span></span>  
 [<span data-ttu-id="be725-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="be725-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)