---
description: Cria um novo objeto de erro URIError JavaScript.
title: Função JsCreateURIError | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateURIError
helpviewer_keywords:
- JsCreateURIError function
ms.assetid: 711fd237-12a2-4ff0-b58a-ad74c91e79fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5188827cd0b89b1dd6b54af005f6e118c4ae4c94
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561077"
---
# <span data-ttu-id="aaa22-103">Função JsCreateURIError</span><span class="sxs-lookup"><span data-stu-id="aaa22-103">JsCreateURIError Function</span></span>
<span data-ttu-id="aaa22-104">Cria um novo objeto de erro URIError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aaa22-104">Creates a new JavaScript URIError error object.</span></span>  
  
## <span data-ttu-id="aaa22-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aaa22-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateURIError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="aaa22-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aaa22-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="aaa22-107">Mensagem do objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="aaa22-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="aaa22-108">O novo objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="aaa22-108">The new error object.</span></span>  
  
## <span data-ttu-id="aaa22-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="aaa22-109">Return Value</span></span>  
 <span data-ttu-id="aaa22-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="aaa22-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="aaa22-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="aaa22-111">Remarks</span></span>  
 <span data-ttu-id="aaa22-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="aaa22-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="aaa22-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aaa22-113">Requirements</span></span>  
 <span data-ttu-id="aaa22-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="aaa22-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="aaa22-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="aaa22-115">See Also</span></span>  
 [<span data-ttu-id="aaa22-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="aaa22-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)