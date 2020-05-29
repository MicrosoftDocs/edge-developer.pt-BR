---
description: Cria um novo objeto de erro SyntaxError JavaScript.
title: Função JsCreateSyntaxError | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateSyntaxError
helpviewer_keywords:
- JsCreateSyntaxError function
ms.assetid: 839845fc-60c4-4ffc-bfcc-fd7a8f06126f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 8f7459e8300df56aa8ccfaa78ef97ce2b6ec6fa0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561081"
---
# <span data-ttu-id="be237-103">Função JsCreateSyntaxError</span><span class="sxs-lookup"><span data-stu-id="be237-103">JsCreateSyntaxError Function</span></span>
<span data-ttu-id="be237-104">Cria um novo objeto de erro SyntaxError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="be237-104">Creates a new JavaScript SyntaxError error object.</span></span>  
  
## <span data-ttu-id="be237-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be237-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSyntaxError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="be237-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be237-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="be237-107">Mensagem do objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="be237-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="be237-108">O novo objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="be237-108">The new error object.</span></span>  
  
## <span data-ttu-id="be237-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="be237-109">Return Value</span></span>  
 <span data-ttu-id="be237-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="be237-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="be237-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="be237-111">Remarks</span></span>  
 <span data-ttu-id="be237-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="be237-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="be237-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be237-113">Requirements</span></span>  
 <span data-ttu-id="be237-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="be237-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="be237-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="be237-115">See Also</span></span>  
 [<span data-ttu-id="be237-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="be237-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)