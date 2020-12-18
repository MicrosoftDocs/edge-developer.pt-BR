---
description: Retorna um valor que indica se a heap do contexto atual está sendo enumerado.
title: Função JsIsEnumeratingHeap | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIsEnumeratingHeap
helpviewer_keywords:
- JsIsEnumeratingHeap function
ms.assetid: 5d14518e-3153-43f2-9a9c-068580cbd54f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5b66fc70ea79d78029f6bc0c900ade1aae38e604
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231797"
---
# <span data-ttu-id="24953-103">Função JsIsEnumeratingHeap</span><span class="sxs-lookup"><span data-stu-id="24953-103">JsIsEnumeratingHeap Function</span></span>

<span data-ttu-id="24953-104">Retorna um valor que indica se a heap do contexto atual está sendo enumerado.</span><span class="sxs-lookup"><span data-stu-id="24953-104">Returns a value that indicates whether the heap of the current context is being enumerated.</span></span>  
  
## <span data-ttu-id="24953-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24953-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsEnumeratingHeap(  
   _Out_ bool *isEnumeratingHeap  
);  
```  
  
#### <span data-ttu-id="24953-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24953-106">Parameters</span></span>  
 `isEnumeratingHeap`  
 <span data-ttu-id="24953-107">Se o heap está sendo enumerado.</span><span class="sxs-lookup"><span data-stu-id="24953-107">Whether the heap is being enumerated.</span></span>  
  
## <span data-ttu-id="24953-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="24953-108">Return Value</span></span>  
 <span data-ttu-id="24953-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="24953-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="24953-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="24953-110">Remarks</span></span>  
 <span data-ttu-id="24953-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="24953-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="24953-112">Essa API tem suporte em aplicativos de área de trabalho, mas não é compatível com aplicativos da loja.</span><span class="sxs-lookup"><span data-stu-id="24953-112">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="24953-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24953-113">Requirements</span></span>  
 <span data-ttu-id="24953-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="24953-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="24953-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="24953-115">See Also</span></span>  
 [<span data-ttu-id="24953-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="24953-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
