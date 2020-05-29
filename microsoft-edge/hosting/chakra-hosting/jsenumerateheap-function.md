---
description: Enumera o heap do contexto atual.
title: Função JsEnumerateHeap | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsEnumerateHeap
helpviewer_keywords:
- JsEnumerateHeap function
ms.assetid: 3e518e0b-b959-4686-899c-83e6b1946c9d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f1c2590388fcc09b641e3908d45eef7271bcb1ad
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562205"
---
# <span data-ttu-id="3ebd2-103">Função JsEnumerateHeap</span><span class="sxs-lookup"><span data-stu-id="3ebd2-103">JsEnumerateHeap Function</span></span>
<span data-ttu-id="3ebd2-104">Enumera o heap do contexto atual.</span><span class="sxs-lookup"><span data-stu-id="3ebd2-104">Enumerates the heap of the current context.</span></span>  
  
## <span data-ttu-id="3ebd2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ebd2-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnumerateHeap(  
   _Out_ IActiveScriptProfilerHeapEnum **enumerator  
);  
```  
  
#### <span data-ttu-id="3ebd2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ebd2-106">Parameters</span></span>  
 `enumerator`  
 <span data-ttu-id="3ebd2-107">O enumerador de heap.</span><span class="sxs-lookup"><span data-stu-id="3ebd2-107">The heap enumerator.</span></span>  
  
## <span data-ttu-id="3ebd2-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3ebd2-108">Return Value</span></span>  
 <span data-ttu-id="3ebd2-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="3ebd2-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3ebd2-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ebd2-110">Remarks</span></span>  
 <span data-ttu-id="3ebd2-111">Enquanto a heap está sendo enumerada, o contexto atual não pode ser removido, e todas as chamadas para modificar o estado do contexto falharão até que o enumerador de heap seja liberado.</span><span class="sxs-lookup"><span data-stu-id="3ebd2-111">While the heap is being enumerated, the current context cannot be removed, and all calls to modify the state of the context will fail until the heap enumerator is released.</span></span>  
  
 <span data-ttu-id="3ebd2-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="3ebd2-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="3ebd2-113">Essa API tem suporte em aplicativos de área de trabalho, mas não é compatível com aplicativos da loja.</span><span class="sxs-lookup"><span data-stu-id="3ebd2-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="3ebd2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ebd2-114">Requirements</span></span>  
 <span data-ttu-id="3ebd2-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3ebd2-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3ebd2-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3ebd2-116">See Also</span></span>  
 [<span data-ttu-id="3ebd2-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3ebd2-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)