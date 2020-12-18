---
description: Cria um valor de número de um `int` valor.
title: Função JsIntToNumber | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 1393c4ac-7189-4e9c-8e54-b0e041c22112
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 24e861d1535ae79843fb35de8a047031a479fe16
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231805"
---
# <span data-ttu-id="76652-103">Função JsIntToNumber</span><span class="sxs-lookup"><span data-stu-id="76652-103">JsIntToNumber Function</span></span>

<span data-ttu-id="76652-104">Cria um valor de número de um `int` valor.</span><span class="sxs-lookup"><span data-stu-id="76652-104">Creates a number value from an `int` value.</span></span>  
  
## <span data-ttu-id="76652-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76652-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIntToNumber(  
   _In_ int intValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="76652-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76652-106">Parameters</span></span>  
 `intValue`  
 <span data-ttu-id="76652-107">A `int` para converter para um valor numérico.</span><span class="sxs-lookup"><span data-stu-id="76652-107">The `int` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="76652-108">O novo valor numérico.</span><span class="sxs-lookup"><span data-stu-id="76652-108">The new number value.</span></span>  
  
## <span data-ttu-id="76652-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="76652-109">Return Value</span></span>  
 <span data-ttu-id="76652-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="76652-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="76652-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="76652-111">Remarks</span></span>  
 <span data-ttu-id="76652-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="76652-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="76652-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76652-113">Requirements</span></span>  
 <span data-ttu-id="76652-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="76652-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="76652-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="76652-115">See Also</span></span>  
 [<span data-ttu-id="76652-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="76652-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
