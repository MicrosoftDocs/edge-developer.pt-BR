---
description: Recupera o `double` valor de um valor numérico.
title: Função JsNumberToDouble | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsNumberToDouble
helpviewer_keywords:
- JsNumberToDouble function
ms.assetid: 5f52e8b6-2b70-49a3-879a-bd83ebf2ac33
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e4ae744f091045116a639aff619c475c7c7025f3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231765"
---
# <span data-ttu-id="f1248-103">Função JsNumberToDouble</span><span class="sxs-lookup"><span data-stu-id="f1248-103">JsNumberToDouble Function</span></span>

<span data-ttu-id="f1248-104">Recupera o `double` valor de um valor numérico.</span><span class="sxs-lookup"><span data-stu-id="f1248-104">Retrieves the `double` value of a number value.</span></span>  
  
## <span data-ttu-id="f1248-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1248-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToDouble(  
   _In_ JsValueRef value,  
   _Out_ double *doubleValue  
);  
```  
  
#### <span data-ttu-id="f1248-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1248-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="f1248-107">O valor numérico a ser convertido em um `double` valor.</span><span class="sxs-lookup"><span data-stu-id="f1248-107">The number value to convert to a `double` value.</span></span>  
  
 `doubleValue`  
 <span data-ttu-id="f1248-108">O `double` valor.</span><span class="sxs-lookup"><span data-stu-id="f1248-108">The `double` value.</span></span>  
  
## <span data-ttu-id="f1248-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f1248-109">Return Value</span></span>  
 <span data-ttu-id="f1248-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="f1248-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f1248-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1248-111">Remarks</span></span>  
 <span data-ttu-id="f1248-112">Esta função recupera o valor de um valor numérico.</span><span class="sxs-lookup"><span data-stu-id="f1248-112">This function retrieves the value of a number value.</span></span> <span data-ttu-id="f1248-113">Ocorrerá uma falha `JsErrorInvalidArgument` se o tipo do valor não for número.</span><span class="sxs-lookup"><span data-stu-id="f1248-113">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="f1248-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="f1248-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f1248-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1248-115">Requirements</span></span>  
 <span data-ttu-id="f1248-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f1248-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f1248-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f1248-117">See Also</span></span>  
 [<span data-ttu-id="f1248-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f1248-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
