---
description: Exclua o valor no índice especificado de um objeto.
title: Função JsDeleteIndexedProperty | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteIndexedProperty
helpviewer_keywords:
- JsDeleteIndexedProperty function
ms.assetid: cc876839-2ecd-41a8-82d0-c19b3de944e3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1340b0204d3845d4a9bd3f18a58ec125a82d2bc0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231769"
---
# <span data-ttu-id="971b4-103">Função JsDeleteIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="971b4-103">JsDeleteIndexedProperty Function</span></span>

<span data-ttu-id="971b4-104">Exclua o valor no índice especificado de um objeto.</span><span class="sxs-lookup"><span data-stu-id="971b4-104">Delete the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="971b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="971b4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index  
);  
```  
  
#### <span data-ttu-id="971b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="971b4-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="971b4-107">O objeto no qual operar.</span><span class="sxs-lookup"><span data-stu-id="971b4-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="971b4-108">O índice a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="971b4-108">The index to delete.</span></span>  
  
## <span data-ttu-id="971b4-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="971b4-109">Return Value</span></span>  
 <span data-ttu-id="971b4-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="971b4-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="971b4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="971b4-111">Remarks</span></span>  
 <span data-ttu-id="971b4-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="971b4-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="971b4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="971b4-113">Requirements</span></span>  
 <span data-ttu-id="971b4-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="971b4-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="971b4-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="971b4-115">See Also</span></span>  
 [<span data-ttu-id="971b4-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="971b4-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
