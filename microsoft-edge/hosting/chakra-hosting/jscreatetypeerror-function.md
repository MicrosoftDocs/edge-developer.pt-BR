---
description: Cria um novo objeto de erro TypeError JavaScript.
title: Função JsCreateTypeError | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateTypeError
helpviewer_keywords:
- JsCreateTypeError function
ms.assetid: 8ef7bb77-2c98-482a-bccb-1f0fe2b826f5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 302bf75af3668dfdd0b40336e940e3eef3a74bce
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561078"
---
# <span data-ttu-id="d8ea5-103">Função JsCreateTypeError</span><span class="sxs-lookup"><span data-stu-id="d8ea5-103">JsCreateTypeError Function</span></span>
<span data-ttu-id="d8ea5-104">Cria um novo objeto de erro TypeError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d8ea5-104">Creates a new JavaScript TypeError error object.</span></span>  
  
## <span data-ttu-id="d8ea5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8ea5-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="d8ea5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8ea5-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="d8ea5-107">Mensagem do objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="d8ea5-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="d8ea5-108">O novo objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="d8ea5-108">The new error object.</span></span>  
  
## <span data-ttu-id="d8ea5-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d8ea5-109">Return Value</span></span>  
 <span data-ttu-id="d8ea5-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="d8ea5-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d8ea5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8ea5-111">Remarks</span></span>  
 <span data-ttu-id="d8ea5-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="d8ea5-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d8ea5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8ea5-113">Requirements</span></span>  
 <span data-ttu-id="d8ea5-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d8ea5-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d8ea5-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d8ea5-115">See Also</span></span>  
 [<span data-ttu-id="d8ea5-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d8ea5-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)