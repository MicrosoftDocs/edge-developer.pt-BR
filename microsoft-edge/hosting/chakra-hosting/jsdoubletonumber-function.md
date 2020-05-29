---
description: Cria um valor de número de um valor duplo.
title: Função JsDoubleToNumber | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDoubleToNumber
helpviewer_keywords:
- JsDoubleToNumber function
ms.assetid: 43eb2ee1-2789-4302-954e-c4087e1ee786
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c33adbe217f27f77e348fc56e87c4587c6a6ec4c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562204"
---
# <span data-ttu-id="81bf0-103">Função JsDoubleToNumber</span><span class="sxs-lookup"><span data-stu-id="81bf0-103">JsDoubleToNumber Function</span></span>
<span data-ttu-id="81bf0-104">Cria um valor numérico a partir de um `double` valor.</span><span class="sxs-lookup"><span data-stu-id="81bf0-104">Creates a number value from a `double` value.</span></span>  
  
## <span data-ttu-id="81bf0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81bf0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDoubleToNumber(  
   _In_ double doubleValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="81bf0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81bf0-106">Parameters</span></span>  
 `doubleValue`  
 <span data-ttu-id="81bf0-107">A `double` para converter para um valor numérico.</span><span class="sxs-lookup"><span data-stu-id="81bf0-107">The `double` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="81bf0-108">O novo valor numérico.</span><span class="sxs-lookup"><span data-stu-id="81bf0-108">The new number value.</span></span>  
  
## <span data-ttu-id="81bf0-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="81bf0-109">Return Value</span></span>  
 <span data-ttu-id="81bf0-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="81bf0-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="81bf0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="81bf0-111">Remarks</span></span>  
 <span data-ttu-id="81bf0-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="81bf0-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="81bf0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81bf0-113">Requirements</span></span>  
 <span data-ttu-id="81bf0-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="81bf0-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="81bf0-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="81bf0-115">See Also</span></span>  
 [<span data-ttu-id="81bf0-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="81bf0-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)