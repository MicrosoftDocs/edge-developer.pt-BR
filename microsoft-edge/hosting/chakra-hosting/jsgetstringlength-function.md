---
description: Obtém o comprimento de um valor de cadeia de caracteres.
title: Função JsGetStringLength | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetStringLength
helpviewer_keywords:
- JsGetStringLength function
ms.assetid: e9f9f28c-e644-439c-aee5-7ce362f71347
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6b562b2dc58341523910db41fb8b748453b2a836
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561041"
---
# <span data-ttu-id="b0ed9-103">Função JsGetStringLength</span><span class="sxs-lookup"><span data-stu-id="b0ed9-103">JsGetStringLength Function</span></span>
<span data-ttu-id="b0ed9-104">Obtém o comprimento de um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b0ed9-104">Gets the length of a string value.</span></span>  
  
## <span data-ttu-id="b0ed9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0ed9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetStringLength(  
   _In_ JsValueRef stringValue,  
   _Out_ int *length  
);  
```  
  
#### <span data-ttu-id="b0ed9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0ed9-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="b0ed9-107">O valor da cadeia de caracteres para obter o comprimento.</span><span class="sxs-lookup"><span data-stu-id="b0ed9-107">The string value to get the length of.</span></span>  
  
 `length`  
 <span data-ttu-id="b0ed9-108">O comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b0ed9-108">The length of the string.</span></span>  
  
## <span data-ttu-id="b0ed9-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0ed9-109">Return Value</span></span>  
 <span data-ttu-id="b0ed9-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="b0ed9-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b0ed9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0ed9-111">Remarks</span></span>  
 <span data-ttu-id="b0ed9-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="b0ed9-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b0ed9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0ed9-113">Requirements</span></span>  
 <span data-ttu-id="b0ed9-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b0ed9-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b0ed9-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b0ed9-115">See Also</span></span>  
 [<span data-ttu-id="b0ed9-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b0ed9-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)