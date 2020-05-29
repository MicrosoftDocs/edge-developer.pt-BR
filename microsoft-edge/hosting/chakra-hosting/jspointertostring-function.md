---
description: Cria um valor de cadeia de caracteres de um ponteiro de cadeia de caracteres.
title: Função JsPointerToString | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsPointerToString
helpviewer_keywords:
- JsPointerToString function
ms.assetid: c71ce07e-4359-450c-afbf-a6ab7d48dddf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b3c5b2d6439244bc9584e15c361412c8a1e87557
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562147"
---
# <span data-ttu-id="d8846-103">Função JsPointerToString</span><span class="sxs-lookup"><span data-stu-id="d8846-103">JsPointerToString Function</span></span>
<span data-ttu-id="d8846-104">Cria um valor de cadeia de caracteres de um ponteiro de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d8846-104">Creates a string value from a string pointer.</span></span>  
  
## <span data-ttu-id="d8846-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8846-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPointerToString(  
   _In_reads_(stringLength) const wchar_t *stringValue,  
   _In_ size_t stringLength,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="d8846-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8846-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="d8846-107">O ponteiro da cadeia de caracteres a ser convertido em um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d8846-107">The string pointer to convert to a string value.</span></span>  
  
 `stringLength`  
 <span data-ttu-id="d8846-108">O comprimento da cadeia de caracteres a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="d8846-108">The length of the string to convert.</span></span>  
  
 `value`  
 <span data-ttu-id="d8846-109">O novo valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d8846-109">The new string value.</span></span>  
  
## <span data-ttu-id="d8846-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d8846-110">Return Value</span></span>  
 <span data-ttu-id="d8846-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="d8846-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d8846-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8846-112">Remarks</span></span>  
 <span data-ttu-id="d8846-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="d8846-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d8846-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8846-114">Requirements</span></span>  
 <span data-ttu-id="d8846-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d8846-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d8846-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d8846-116">See Also</span></span>  
 [<span data-ttu-id="d8846-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d8846-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)