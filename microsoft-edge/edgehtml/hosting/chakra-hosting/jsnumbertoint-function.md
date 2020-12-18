---
description: Recupera o `int` valor de um valor numérico.
title: Função JsNumberToInt | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 928be9a7cc5cd3e26e8b8df99af1e08a6c50209c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231763"
---
# <span data-ttu-id="3a182-103">Função JsNumberToInt</span><span class="sxs-lookup"><span data-stu-id="3a182-103">JsNumberToInt Function</span></span>

<span data-ttu-id="3a182-104">Recupera o `int` valor de um valor numérico.</span><span class="sxs-lookup"><span data-stu-id="3a182-104">Retrieves the `int` value of a number value.</span></span>  
  
## <span data-ttu-id="3a182-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a182-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToInt(  
      _In_ JsValueRef value,  
      _Out_ int *intValue  
);  
```  
  
#### <span data-ttu-id="3a182-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a182-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="3a182-107">O valor numérico a ser convertido em um `int` valor.</span><span class="sxs-lookup"><span data-stu-id="3a182-107">The number value to convert to an `int` value.</span></span>  
  
 `intValue`  
 <span data-ttu-id="3a182-108">O `int` valor.</span><span class="sxs-lookup"><span data-stu-id="3a182-108">The `int` value.</span></span>  
  
## <span data-ttu-id="3a182-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3a182-109">Return Value</span></span>  
  
## <span data-ttu-id="3a182-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a182-110">Remarks</span></span>  
 <span data-ttu-id="3a182-111">Essa função recupera o valor de um valor numérico e converte para um `int` valor.</span><span class="sxs-lookup"><span data-stu-id="3a182-111">This function retrieves the value of a number value and converts to an `int` value.</span></span> <span data-ttu-id="3a182-112">Ocorrerá uma falha `JsErrorInvalidArgument` se o tipo do valor não for número.</span><span class="sxs-lookup"><span data-stu-id="3a182-112">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="3a182-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="3a182-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="3a182-114">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="3a182-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="3a182-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a182-115">Requirements</span></span>  
 <span data-ttu-id="3a182-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3a182-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3a182-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3a182-117">See Also</span></span>  
 [<span data-ttu-id="3a182-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3a182-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
