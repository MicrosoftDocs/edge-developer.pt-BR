---
description: Recupera o `double` valor de um valor numérico.
title: Função JsNumberToDouble | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsNumberToDouble
helpviewer_keywords:
- JsNumberToDouble function
ms.assetid: 5f52e8b6-2b70-49a3-879a-bd83ebf2ac33
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: fc99e02aa0376bb100b4e1302c29532a57bd539f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561015"
---
# <span data-ttu-id="dafc4-103">Função JsNumberToDouble</span><span class="sxs-lookup"><span data-stu-id="dafc4-103">JsNumberToDouble Function</span></span>
<span data-ttu-id="dafc4-104">Recupera o `double` valor de um valor numérico.</span><span class="sxs-lookup"><span data-stu-id="dafc4-104">Retrieves the `double` value of a number value.</span></span>  
  
## <span data-ttu-id="dafc4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dafc4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToDouble(  
   _In_ JsValueRef value,  
   _Out_ double *doubleValue  
);  
```  
  
#### <span data-ttu-id="dafc4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dafc4-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="dafc4-107">O valor numérico a ser convertido em um `double` valor.</span><span class="sxs-lookup"><span data-stu-id="dafc4-107">The number value to convert to a `double` value.</span></span>  
  
 `doubleValue`  
 <span data-ttu-id="dafc4-108">O `double` valor.</span><span class="sxs-lookup"><span data-stu-id="dafc4-108">The `double` value.</span></span>  
  
## <span data-ttu-id="dafc4-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dafc4-109">Return Value</span></span>  
 <span data-ttu-id="dafc4-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="dafc4-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dafc4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="dafc4-111">Remarks</span></span>  
 <span data-ttu-id="dafc4-112">Esta função recupera o valor de um valor numérico.</span><span class="sxs-lookup"><span data-stu-id="dafc4-112">This function retrieves the value of a number value.</span></span> <span data-ttu-id="dafc4-113">Ocorrerá uma falha `JsErrorInvalidArgument` se o tipo do valor não for número.</span><span class="sxs-lookup"><span data-stu-id="dafc4-113">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="dafc4-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="dafc4-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="dafc4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dafc4-115">Requirements</span></span>  
 <span data-ttu-id="dafc4-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dafc4-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dafc4-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="dafc4-117">See Also</span></span>  
 [<span data-ttu-id="dafc4-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dafc4-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)