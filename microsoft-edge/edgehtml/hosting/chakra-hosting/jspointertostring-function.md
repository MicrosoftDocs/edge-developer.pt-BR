---
description: Cria um valor de cadeia de caracteres de um ponteiro de cadeia de caracteres.
title: Função JsPointerToString | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsPointerToString
helpviewer_keywords:
- JsPointerToString function
ms.assetid: c71ce07e-4359-450c-afbf-a6ab7d48dddf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c00a060098f0b021afca27b300f3e0578e992cb9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231754"
---
# <span data-ttu-id="f7c8c-103">Função JsPointerToString</span><span class="sxs-lookup"><span data-stu-id="f7c8c-103">JsPointerToString Function</span></span>

<span data-ttu-id="f7c8c-104">Cria um valor de cadeia de caracteres de um ponteiro de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f7c8c-104">Creates a string value from a string pointer.</span></span>  
  
## <span data-ttu-id="f7c8c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7c8c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPointerToString(  
   _In_reads_(stringLength) const wchar_t *stringValue,  
   _In_ size_t stringLength,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="f7c8c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7c8c-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="f7c8c-107">O ponteiro da cadeia de caracteres a ser convertido em um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f7c8c-107">The string pointer to convert to a string value.</span></span>  
  
 `stringLength`  
 <span data-ttu-id="f7c8c-108">O comprimento da cadeia de caracteres a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="f7c8c-108">The length of the string to convert.</span></span>  
  
 `value`  
 <span data-ttu-id="f7c8c-109">O novo valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f7c8c-109">The new string value.</span></span>  
  
## <span data-ttu-id="f7c8c-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f7c8c-110">Return Value</span></span>  
 <span data-ttu-id="f7c8c-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="f7c8c-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f7c8c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7c8c-112">Remarks</span></span>  
 <span data-ttu-id="f7c8c-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="f7c8c-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f7c8c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7c8c-114">Requirements</span></span>  
 <span data-ttu-id="f7c8c-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f7c8c-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f7c8c-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f7c8c-116">See Also</span></span>  
 [<span data-ttu-id="f7c8c-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f7c8c-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
