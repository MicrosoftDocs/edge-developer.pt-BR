---
description: Enumera o heap do contexto atual.
title: Função JsEnumerateHeap | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEnumerateHeap
helpviewer_keywords:
- JsEnumerateHeap function
ms.assetid: 3e518e0b-b959-4686-899c-83e6b1946c9d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bb76b28f24b769f71827e59be691188e34e9e1a3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231771"
---
# <span data-ttu-id="eecb4-103">Função JsEnumerateHeap</span><span class="sxs-lookup"><span data-stu-id="eecb4-103">JsEnumerateHeap Function</span></span>

<span data-ttu-id="eecb4-104">Enumera o heap do contexto atual.</span><span class="sxs-lookup"><span data-stu-id="eecb4-104">Enumerates the heap of the current context.</span></span>  
  
## <span data-ttu-id="eecb4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eecb4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnumerateHeap(  
   _Out_ IActiveScriptProfilerHeapEnum **enumerator  
);  
```  
  
#### <span data-ttu-id="eecb4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eecb4-106">Parameters</span></span>  
 `enumerator`  
 <span data-ttu-id="eecb4-107">O enumerador de heap.</span><span class="sxs-lookup"><span data-stu-id="eecb4-107">The heap enumerator.</span></span>  
  
## <span data-ttu-id="eecb4-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="eecb4-108">Return Value</span></span>  
 <span data-ttu-id="eecb4-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="eecb4-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="eecb4-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="eecb4-110">Remarks</span></span>  
 <span data-ttu-id="eecb4-111">Enquanto a heap está sendo enumerada, o contexto atual não pode ser removido, e todas as chamadas para modificar o estado do contexto falharão até que o enumerador de heap seja liberado.</span><span class="sxs-lookup"><span data-stu-id="eecb4-111">While the heap is being enumerated, the current context cannot be removed, and all calls to modify the state of the context will fail until the heap enumerator is released.</span></span>  
  
 <span data-ttu-id="eecb4-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="eecb4-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="eecb4-113">Essa API tem suporte em aplicativos de área de trabalho, mas não é compatível com aplicativos da loja.</span><span class="sxs-lookup"><span data-stu-id="eecb4-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="eecb4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eecb4-114">Requirements</span></span>  
 <span data-ttu-id="eecb4-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="eecb4-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="eecb4-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="eecb4-116">See Also</span></span>  
 [<span data-ttu-id="eecb4-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="eecb4-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
