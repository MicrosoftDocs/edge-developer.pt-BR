---
description: Converte o valor em Object usando a semântica JavaScript padrão.
title: Função JsConvertValueToObject | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToObject
helpviewer_keywords:
- JsConvertValueToObject function
ms.assetid: 6528b28a-1d2b-417f-bf78-bf05547c52e1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6f3676b512585b0750c994bcfcdf9d2e6e4e1cc3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231427"
---
# <span data-ttu-id="a4f2d-103">Função JsConvertValueToObject</span><span class="sxs-lookup"><span data-stu-id="a4f2d-103">JsConvertValueToObject Function</span></span>

<span data-ttu-id="a4f2d-104">Converte o valor em Object usando a semântica JavaScript padrão.</span><span class="sxs-lookup"><span data-stu-id="a4f2d-104">Converts the value to object using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="a4f2d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4f2d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToObject(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="a4f2d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4f2d-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="a4f2d-107">O valor a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="a4f2d-107">The value to be converted.</span></span>  
  
 `object`  
 <span data-ttu-id="a4f2d-108">O valor convertido.</span><span class="sxs-lookup"><span data-stu-id="a4f2d-108">The converted value.</span></span>  
  
## <span data-ttu-id="a4f2d-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a4f2d-109">Return Value</span></span>  
 <span data-ttu-id="a4f2d-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="a4f2d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a4f2d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4f2d-111">Remarks</span></span>  
 <span data-ttu-id="a4f2d-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="a4f2d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a4f2d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4f2d-113">Requirements</span></span>  
 <span data-ttu-id="a4f2d-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a4f2d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a4f2d-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a4f2d-115">See Also</span></span>  
 [<span data-ttu-id="a4f2d-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a4f2d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
