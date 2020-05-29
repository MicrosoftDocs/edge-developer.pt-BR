---
description: Recupera o `int` valor de um valor numérico.
title: Função JsNumberToInt | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: cf4c8cb42c737cfb9efee5422fe6bb3c1389cbfd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562155"
---
# <span data-ttu-id="e7aa4-103">Função JsNumberToInt</span><span class="sxs-lookup"><span data-stu-id="e7aa4-103">JsNumberToInt Function</span></span>
<span data-ttu-id="e7aa4-104">Recupera o `int` valor de um valor numérico.</span><span class="sxs-lookup"><span data-stu-id="e7aa4-104">Retrieves the `int` value of a number value.</span></span>  
  
## <span data-ttu-id="e7aa4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7aa4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToInt(  
      _In_ JsValueRef value,  
      _Out_ int *intValue  
);  
```  
  
#### <span data-ttu-id="e7aa4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7aa4-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="e7aa4-107">O valor numérico a ser convertido em um `int` valor.</span><span class="sxs-lookup"><span data-stu-id="e7aa4-107">The number value to convert to an `int` value.</span></span>  
  
 `intValue`  
 <span data-ttu-id="e7aa4-108">O `int` valor.</span><span class="sxs-lookup"><span data-stu-id="e7aa4-108">The `int` value.</span></span>  
  
## <span data-ttu-id="e7aa4-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e7aa4-109">Return Value</span></span>  
  
## <span data-ttu-id="e7aa4-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7aa4-110">Remarks</span></span>  
 <span data-ttu-id="e7aa4-111">Essa função recupera o valor de um valor numérico e converte para um `int` valor.</span><span class="sxs-lookup"><span data-stu-id="e7aa4-111">This function retrieves the value of a number value and converts to an `int` value.</span></span> <span data-ttu-id="e7aa4-112">Ocorrerá uma falha `JsErrorInvalidArgument` se o tipo do valor não for número.</span><span class="sxs-lookup"><span data-stu-id="e7aa4-112">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="e7aa4-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="e7aa4-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="e7aa4-114">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="e7aa4-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="e7aa4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7aa4-115">Requirements</span></span>  
 <span data-ttu-id="e7aa4-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e7aa4-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e7aa4-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e7aa4-117">See Also</span></span>  
 [<span data-ttu-id="e7aa4-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e7aa4-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)