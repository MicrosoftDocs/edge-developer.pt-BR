---
description: Cria um valor de número de um `int` valor.
title: Função JsIntToNumber | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 1393c4ac-7189-4e9c-8e54-b0e041c22112
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: dd8f51638292346ec3058f9537d72b8fd21bebc6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561029"
---
# <span data-ttu-id="2771c-103">Função JsIntToNumber</span><span class="sxs-lookup"><span data-stu-id="2771c-103">JsIntToNumber Function</span></span>
<span data-ttu-id="2771c-104">Cria um valor de número de um `int` valor.</span><span class="sxs-lookup"><span data-stu-id="2771c-104">Creates a number value from an `int` value.</span></span>  
  
## <span data-ttu-id="2771c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2771c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIntToNumber(  
   _In_ int intValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="2771c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2771c-106">Parameters</span></span>  
 `intValue`  
 <span data-ttu-id="2771c-107">A `int` para converter para um valor numérico.</span><span class="sxs-lookup"><span data-stu-id="2771c-107">The `int` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="2771c-108">O novo valor numérico.</span><span class="sxs-lookup"><span data-stu-id="2771c-108">The new number value.</span></span>  
  
## <span data-ttu-id="2771c-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2771c-109">Return Value</span></span>  
 <span data-ttu-id="2771c-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="2771c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2771c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2771c-111">Remarks</span></span>  
 <span data-ttu-id="2771c-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="2771c-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="2771c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2771c-113">Requirements</span></span>  
 <span data-ttu-id="2771c-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2771c-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2771c-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2771c-115">See Also</span></span>  
 [<span data-ttu-id="2771c-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2771c-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)