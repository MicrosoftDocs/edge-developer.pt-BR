---
description: Cria um novo objeto de erro TypeError JavaScript.
title: Função JsCreateTypeError | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateTypeError
helpviewer_keywords:
- JsCreateTypeError function
ms.assetid: 8ef7bb77-2c98-482a-bccb-1f0fe2b826f5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 627dfdc6f01f0708366720a957b3784fc7bb59a4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231773"
---
# <span data-ttu-id="ff128-103">Função JsCreateTypeError</span><span class="sxs-lookup"><span data-stu-id="ff128-103">JsCreateTypeError Function</span></span>

<span data-ttu-id="ff128-104">Cria um novo objeto de erro TypeError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ff128-104">Creates a new JavaScript TypeError error object.</span></span>  
  
## <span data-ttu-id="ff128-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff128-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="ff128-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff128-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="ff128-107">Mensagem do objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="ff128-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="ff128-108">O novo objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="ff128-108">The new error object.</span></span>  
  
## <span data-ttu-id="ff128-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ff128-109">Return Value</span></span>  
 <span data-ttu-id="ff128-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="ff128-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ff128-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff128-111">Remarks</span></span>  
 <span data-ttu-id="ff128-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="ff128-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ff128-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff128-113">Requirements</span></span>  
 <span data-ttu-id="ff128-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ff128-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ff128-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ff128-115">See Also</span></span>  
 [<span data-ttu-id="ff128-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ff128-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
