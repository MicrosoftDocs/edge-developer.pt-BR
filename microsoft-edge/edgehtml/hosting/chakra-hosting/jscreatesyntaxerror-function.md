---
description: Cria um novo objeto de erro SyntaxError JavaScript.
title: Função JsCreateSyntaxError | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateSyntaxError
helpviewer_keywords:
- JsCreateSyntaxError function
ms.assetid: 839845fc-60c4-4ffc-bfcc-fd7a8f06126f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7d6534bfa2b59cb2f6ab68c231d7a97c84876d62
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231777"
---
# <span data-ttu-id="b3071-103">Função JsCreateSyntaxError</span><span class="sxs-lookup"><span data-stu-id="b3071-103">JsCreateSyntaxError Function</span></span>

<span data-ttu-id="b3071-104">Cria um novo objeto de erro SyntaxError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b3071-104">Creates a new JavaScript SyntaxError error object.</span></span>  
  
## <span data-ttu-id="b3071-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3071-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSyntaxError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="b3071-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3071-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="b3071-107">Mensagem do objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="b3071-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="b3071-108">O novo objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="b3071-108">The new error object.</span></span>  
  
## <span data-ttu-id="b3071-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b3071-109">Return Value</span></span>  
 <span data-ttu-id="b3071-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="b3071-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b3071-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3071-111">Remarks</span></span>  
 <span data-ttu-id="b3071-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="b3071-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b3071-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3071-113">Requirements</span></span>  
 <span data-ttu-id="b3071-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b3071-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b3071-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b3071-115">See Also</span></span>  
 [<span data-ttu-id="b3071-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b3071-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
