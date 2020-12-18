---
description: Cria um novo objeto de erro RangeError JavaScript.
title: Função JsCreateRangeError | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRangeError
helpviewer_keywords:
- JsCreateRangeError function
ms.assetid: 0ab05de7-57af-4cfd-9aa5-0a69a893cc97
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 72cf882d5f9517f0f05d9e3367283f5f531dbdb3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231588"
---
# <span data-ttu-id="e1bd6-103">Função JsCreateRangeError</span><span class="sxs-lookup"><span data-stu-id="e1bd6-103">JsCreateRangeError Function</span></span>

<span data-ttu-id="e1bd6-104">Cria um novo objeto de erro RangeError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e1bd6-104">Creates a new JavaScript RangeError error object.</span></span>
  
## <span data-ttu-id="e1bd6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1bd6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateRangeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="e1bd6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1bd6-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="e1bd6-107">Mensagem do objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="e1bd6-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="e1bd6-108">O novo objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="e1bd6-108">The new error object.</span></span>  
  
## <span data-ttu-id="e1bd6-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e1bd6-109">Return Value</span></span>  
 <span data-ttu-id="e1bd6-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="e1bd6-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e1bd6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1bd6-111">Remarks</span></span>  
 <span data-ttu-id="e1bd6-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="e1bd6-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e1bd6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1bd6-113">Requirements</span></span>  
 <span data-ttu-id="e1bd6-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e1bd6-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e1bd6-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e1bd6-115">See Also</span></span>  
 [<span data-ttu-id="e1bd6-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e1bd6-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
