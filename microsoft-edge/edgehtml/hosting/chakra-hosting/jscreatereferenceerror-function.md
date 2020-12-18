---
description: Cria um novo objeto de erro ReferenceError JavaScript.
title: Função JsCreateReferenceError | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateReferenceError
helpviewer_keywords:
- JsCreateReferenceError function
ms.assetid: 1d0b2339-4bea-4dd0-a46a-4dcbf0be3bd8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fc8f10c443d6ca019c1460c84344bf04513e44b9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231644"
---
# <span data-ttu-id="1d89a-103">Função JsCreateReferenceError</span><span class="sxs-lookup"><span data-stu-id="1d89a-103">JsCreateReferenceError Function</span></span>

<span data-ttu-id="1d89a-104">Cria um novo objeto de erro ReferenceError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1d89a-104">Creates a new JavaScript ReferenceError error object.</span></span>
  
## <span data-ttu-id="1d89a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d89a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateReferenceError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="1d89a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d89a-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="1d89a-107">Mensagem do objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="1d89a-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="1d89a-108">O novo objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="1d89a-108">The new error object.</span></span>  
  
## <span data-ttu-id="1d89a-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1d89a-109">Return Value</span></span>  
 <span data-ttu-id="1d89a-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="1d89a-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1d89a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d89a-111">Remarks</span></span>  
 <span data-ttu-id="1d89a-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="1d89a-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="1d89a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d89a-113">Requirements</span></span>  
 <span data-ttu-id="1d89a-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1d89a-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1d89a-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1d89a-115">See Also</span></span>  
 [<span data-ttu-id="1d89a-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1d89a-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
