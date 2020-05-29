---
description: Cria um novo objeto de erro ReferenceError JavaScript.
title: Função JsCreateReferenceError | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateReferenceError
helpviewer_keywords:
- JsCreateReferenceError function
ms.assetid: 1d0b2339-4bea-4dd0-a46a-4dcbf0be3bd8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 958af7111a233077aa7a2c2391b26666f55c634b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561090"
---
# <span data-ttu-id="56327-103">Função JsCreateReferenceError</span><span class="sxs-lookup"><span data-stu-id="56327-103">JsCreateReferenceError Function</span></span>
<span data-ttu-id="56327-104">Cria um novo objeto de erro ReferenceError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="56327-104">Creates a new JavaScript ReferenceError error object.</span></span>
  
## <span data-ttu-id="56327-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56327-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateReferenceError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="56327-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56327-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="56327-107">Mensagem do objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="56327-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="56327-108">O novo objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="56327-108">The new error object.</span></span>  
  
## <span data-ttu-id="56327-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="56327-109">Return Value</span></span>  
 <span data-ttu-id="56327-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="56327-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="56327-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="56327-111">Remarks</span></span>  
 <span data-ttu-id="56327-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="56327-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="56327-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56327-113">Requirements</span></span>  
 <span data-ttu-id="56327-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="56327-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="56327-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="56327-115">See Also</span></span>  
 [<span data-ttu-id="56327-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="56327-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)