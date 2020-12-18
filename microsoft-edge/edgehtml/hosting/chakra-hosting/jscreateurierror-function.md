---
description: Cria um novo objeto de erro URIError JavaScript.
title: Função JsCreateURIError | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateURIError
helpviewer_keywords:
- JsCreateURIError function
ms.assetid: 711fd237-12a2-4ff0-b58a-ad74c91e79fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 88e6c1fc04607b3be088e297d1fa86f9374bcb03
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231561"
---
# <span data-ttu-id="f2732-103">Função JsCreateURIError</span><span class="sxs-lookup"><span data-stu-id="f2732-103">JsCreateURIError Function</span></span>

<span data-ttu-id="f2732-104">Cria um novo objeto de erro URIError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f2732-104">Creates a new JavaScript URIError error object.</span></span>  
  
## <span data-ttu-id="f2732-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2732-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateURIError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="f2732-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2732-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="f2732-107">Mensagem do objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="f2732-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="f2732-108">O novo objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="f2732-108">The new error object.</span></span>  
  
## <span data-ttu-id="f2732-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f2732-109">Return Value</span></span>  
 <span data-ttu-id="f2732-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="f2732-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f2732-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2732-111">Remarks</span></span>  
 <span data-ttu-id="f2732-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="f2732-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f2732-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2732-113">Requirements</span></span>  
 <span data-ttu-id="f2732-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f2732-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f2732-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f2732-115">See Also</span></span>  
 [<span data-ttu-id="f2732-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f2732-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
