---
description: Converte o valor em núm usando a semântica JavaScript padrão.
title: Função JsConvertValueToNumber | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToNumber
helpviewer_keywords:
- JsConvertValueToNumber function
ms.assetid: c47b8653-0591-4863-b8b5-33187b315816
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8d00950ef3835c6d75f8f55ffe5002b32c6ee160
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231444"
---
# <span data-ttu-id="453b3-103">Função JsConvertValueToNumber</span><span class="sxs-lookup"><span data-stu-id="453b3-103">JsConvertValueToNumber Function</span></span>

<span data-ttu-id="453b3-104">Converte o valor em núm usando a semântica JavaScript padrão.</span><span class="sxs-lookup"><span data-stu-id="453b3-104">Converts the value to number using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="453b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="453b3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToNumber(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *numberValue  
);  
```  
  
#### <span data-ttu-id="453b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="453b3-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="453b3-107">O valor a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="453b3-107">The value to be converted.</span></span>  
  
 `numberValue`  
 <span data-ttu-id="453b3-108">O valor convertido.</span><span class="sxs-lookup"><span data-stu-id="453b3-108">The converted value.</span></span>  
  
## <span data-ttu-id="453b3-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="453b3-109">Return Value</span></span>  
 <span data-ttu-id="453b3-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="453b3-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="453b3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="453b3-111">Remarks</span></span>  
 <span data-ttu-id="453b3-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="453b3-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="453b3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="453b3-113">Requirements</span></span>  
 <span data-ttu-id="453b3-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="453b3-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="453b3-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="453b3-115">See Also</span></span>  
 [<span data-ttu-id="453b3-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="453b3-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
