---
description: Cria um novo objeto de erro JavaScript.
title: Função JsCreateError | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateError
helpviewer_keywords:
- JsCreateError function
ms.assetid: dadbcac8-c56f-4f30-ba00-2d284daee191
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 33d70e3f077b085ccb4ab541d3246d777ea68978
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561103"
---
# <span data-ttu-id="24015-103">Função JsCreateError</span><span class="sxs-lookup"><span data-stu-id="24015-103">JsCreateError Function</span></span>
<span data-ttu-id="24015-104">Cria um novo objeto de erro JavaScript.</span><span class="sxs-lookup"><span data-stu-id="24015-104">Creates a new JavaScript error object.</span></span>  
  
## <span data-ttu-id="24015-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24015-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="24015-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24015-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="24015-107">Mensagem do objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="24015-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="24015-108">O novo objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="24015-108">The new error object.</span></span>  
  
## <span data-ttu-id="24015-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="24015-109">Return Value</span></span>  
 <span data-ttu-id="24015-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="24015-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="24015-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="24015-111">Remarks</span></span>  
 <span data-ttu-id="24015-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="24015-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="24015-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24015-113">Requirements</span></span>  
 <span data-ttu-id="24015-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="24015-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="24015-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="24015-115">See Also</span></span>  
 [<span data-ttu-id="24015-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="24015-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)