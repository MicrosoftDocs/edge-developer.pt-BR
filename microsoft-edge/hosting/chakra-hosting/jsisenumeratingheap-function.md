---
description: Retorna um valor que indica se a heap do contexto atual está sendo enumerado.
title: Função JsIsEnumeratingHeap | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIsEnumeratingHeap
helpviewer_keywords:
- JsIsEnumeratingHeap function
ms.assetid: 5d14518e-3153-43f2-9a9c-068580cbd54f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 79f263547ef5812d905103d09ede7499d56c5dfb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561025"
---
# <span data-ttu-id="f812f-103">Função JsIsEnumeratingHeap</span><span class="sxs-lookup"><span data-stu-id="f812f-103">JsIsEnumeratingHeap Function</span></span>
<span data-ttu-id="f812f-104">Retorna um valor que indica se a heap do contexto atual está sendo enumerado.</span><span class="sxs-lookup"><span data-stu-id="f812f-104">Returns a value that indicates whether the heap of the current context is being enumerated.</span></span>  
  
## <span data-ttu-id="f812f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f812f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsEnumeratingHeap(  
   _Out_ bool *isEnumeratingHeap  
);  
```  
  
#### <span data-ttu-id="f812f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f812f-106">Parameters</span></span>  
 `isEnumeratingHeap`  
 <span data-ttu-id="f812f-107">Se o heap está sendo enumerado.</span><span class="sxs-lookup"><span data-stu-id="f812f-107">Whether the heap is being enumerated.</span></span>  
  
## <span data-ttu-id="f812f-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f812f-108">Return Value</span></span>  
 <span data-ttu-id="f812f-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="f812f-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f812f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f812f-110">Remarks</span></span>  
 <span data-ttu-id="f812f-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="f812f-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="f812f-112">Essa API tem suporte em aplicativos de área de trabalho, mas não é compatível com aplicativos da loja.</span><span class="sxs-lookup"><span data-stu-id="f812f-112">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="f812f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f812f-113">Requirements</span></span>  
 <span data-ttu-id="f812f-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f812f-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f812f-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f812f-115">See Also</span></span>  
 [<span data-ttu-id="f812f-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f812f-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)