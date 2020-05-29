---
description: Cria um novo objeto de erro RangeError JavaScript.
title: Função JsCreateRangeError | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRangeError
helpviewer_keywords:
- JsCreateRangeError function
ms.assetid: 0ab05de7-57af-4cfd-9aa5-0a69a893cc97
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 3759f1c04a2eb13488f756ae2c135373d9db1f74
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561092"
---
# <span data-ttu-id="4ae3f-103">Função JsCreateRangeError</span><span class="sxs-lookup"><span data-stu-id="4ae3f-103">JsCreateRangeError Function</span></span>
<span data-ttu-id="4ae3f-104">Cria um novo objeto de erro RangeError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4ae3f-104">Creates a new JavaScript RangeError error object.</span></span>
  
## <span data-ttu-id="4ae3f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ae3f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateRangeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="4ae3f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ae3f-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="4ae3f-107">Mensagem do objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="4ae3f-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="4ae3f-108">O novo objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="4ae3f-108">The new error object.</span></span>  
  
## <span data-ttu-id="4ae3f-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4ae3f-109">Return Value</span></span>  
 <span data-ttu-id="4ae3f-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="4ae3f-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4ae3f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ae3f-111">Remarks</span></span>  
 <span data-ttu-id="4ae3f-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="4ae3f-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4ae3f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ae3f-113">Requirements</span></span>  
 <span data-ttu-id="4ae3f-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4ae3f-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4ae3f-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4ae3f-115">See Also</span></span>  
 [<span data-ttu-id="4ae3f-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4ae3f-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)