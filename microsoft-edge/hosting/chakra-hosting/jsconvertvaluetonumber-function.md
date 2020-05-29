---
description: Converte o valor em núm usando a semântica JavaScript padrão.
title: Função JsConvertValueToNumber | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToNumber
helpviewer_keywords:
- JsConvertValueToNumber function
ms.assetid: c47b8653-0591-4863-b8b5-33187b315816
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 3b3f450a58aaf1c434e1d34cd51577e3a5a9ee31
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561116"
---
# <span data-ttu-id="b96a1-103">Função JsConvertValueToNumber</span><span class="sxs-lookup"><span data-stu-id="b96a1-103">JsConvertValueToNumber Function</span></span>
<span data-ttu-id="b96a1-104">Converte o valor em núm usando a semântica JavaScript padrão.</span><span class="sxs-lookup"><span data-stu-id="b96a1-104">Converts the value to number using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="b96a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b96a1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToNumber(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *numberValue  
);  
```  
  
#### <span data-ttu-id="b96a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b96a1-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="b96a1-107">O valor a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="b96a1-107">The value to be converted.</span></span>  
  
 `numberValue`  
 <span data-ttu-id="b96a1-108">O valor convertido.</span><span class="sxs-lookup"><span data-stu-id="b96a1-108">The converted value.</span></span>  
  
## <span data-ttu-id="b96a1-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b96a1-109">Return Value</span></span>  
 <span data-ttu-id="b96a1-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="b96a1-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b96a1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b96a1-111">Remarks</span></span>  
 <span data-ttu-id="b96a1-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="b96a1-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b96a1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b96a1-113">Requirements</span></span>  
 <span data-ttu-id="b96a1-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b96a1-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b96a1-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b96a1-115">See Also</span></span>  
 [<span data-ttu-id="b96a1-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b96a1-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)