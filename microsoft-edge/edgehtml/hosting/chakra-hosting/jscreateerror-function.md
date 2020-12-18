---
description: Cria um novo objeto de erro JavaScript.
title: Função JsCreateError | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateError
helpviewer_keywords:
- JsCreateError function
ms.assetid: dadbcac8-c56f-4f30-ba00-2d284daee191
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cd2fd0172902cc6dc8a4dd169eef5947d0b25256
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231423"
---
# <span data-ttu-id="7416d-103">Função JsCreateError</span><span class="sxs-lookup"><span data-stu-id="7416d-103">JsCreateError Function</span></span>

<span data-ttu-id="7416d-104">Cria um novo objeto de erro JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7416d-104">Creates a new JavaScript error object.</span></span>  
  
## <span data-ttu-id="7416d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7416d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="7416d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7416d-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="7416d-107">Mensagem do objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="7416d-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="7416d-108">O novo objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="7416d-108">The new error object.</span></span>  
  
## <span data-ttu-id="7416d-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7416d-109">Return Value</span></span>  
 <span data-ttu-id="7416d-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="7416d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7416d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7416d-111">Remarks</span></span>  
 <span data-ttu-id="7416d-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="7416d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="7416d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7416d-113">Requirements</span></span>  
 <span data-ttu-id="7416d-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7416d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7416d-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7416d-115">See Also</span></span>  
 [<span data-ttu-id="7416d-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7416d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
