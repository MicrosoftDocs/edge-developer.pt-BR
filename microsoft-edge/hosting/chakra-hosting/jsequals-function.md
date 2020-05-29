---
description: Comparar dois valores JavaScript para igualdade.
title: Função JsEquals | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsEquals
helpviewer_keywords:
- JsEquals function
ms.assetid: 8377a7b6-12ff-43e4-8cc8-5a5a198a168b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 84416584a048512ab20754a3b59eb8ec255901c4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562200"
---
# <span data-ttu-id="52748-103">Função JsEquals</span><span class="sxs-lookup"><span data-stu-id="52748-103">JsEquals Function</span></span>
<span data-ttu-id="52748-104">Comparar dois valores JavaScript para igualdade.</span><span class="sxs-lookup"><span data-stu-id="52748-104">Compare two JavaScript values for equality.</span></span>  
  
## <span data-ttu-id="52748-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52748-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="52748-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52748-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="52748-107">O primeiro objeto a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="52748-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="52748-108">O segundo objeto a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="52748-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="52748-109">Se os valores são iguais.</span><span class="sxs-lookup"><span data-stu-id="52748-109">Whether the values are equal.</span></span>  
  
## <span data-ttu-id="52748-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="52748-110">Return Value</span></span>  
 <span data-ttu-id="52748-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="52748-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="52748-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="52748-112">Remarks</span></span>  
 <span data-ttu-id="52748-113">Esta função é equivalente à `==` operadora em JavaScript.</span><span class="sxs-lookup"><span data-stu-id="52748-113">This function is equivalent to the `==` operator in Javascript.</span></span>  
  
 <span data-ttu-id="52748-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="52748-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="52748-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52748-115">Requirements</span></span>  
 <span data-ttu-id="52748-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="52748-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="52748-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="52748-117">See Also</span></span>  
 [<span data-ttu-id="52748-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="52748-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)