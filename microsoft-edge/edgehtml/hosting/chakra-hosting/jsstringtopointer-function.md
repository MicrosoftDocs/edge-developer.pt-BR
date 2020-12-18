---
description: Recupera o ponteiro da cadeia de caracteres de um valor de cadeia de caracteres.
title: Função JsStringToPointer | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStringToPointer
helpviewer_keywords:
- JsStringToPointer function
ms.assetid: c7aa7a09-489d-4435-8f8a-aeb62f8875ae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 77b8e16be41d8b5541129b50fa200b947f566342
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231578"
---
# <span data-ttu-id="efb0a-103">Função JsStringToPointer</span><span class="sxs-lookup"><span data-stu-id="efb0a-103">JsStringToPointer Function</span></span>

<span data-ttu-id="efb0a-104">Recupera o ponteiro da cadeia de caracteres de um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="efb0a-104">Retrieves the string pointer of a string value.</span></span>  
  
## <span data-ttu-id="efb0a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efb0a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStringToPointer(  
   _In_ JsValueRef value,  
   _Outptr_result_buffer_(*stringLength) const wchar_t **stringValue,  
   _Out_ size_t *stringLength  
);  
```  
  
#### <span data-ttu-id="efb0a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efb0a-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="efb0a-107">O valor da cadeia de caracteres a ser convertido em um ponteiro de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="efb0a-107">The string value to convert to a string pointer.</span></span>  
  
 `stringValue`  
 <span data-ttu-id="efb0a-108">O ponteiro da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="efb0a-108">The string pointer.</span></span>  
  
 `stringLength`  
 <span data-ttu-id="efb0a-109">O comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="efb0a-109">The length of the string.</span></span>  
  
## <span data-ttu-id="efb0a-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="efb0a-110">Return Value</span></span>  
 <span data-ttu-id="efb0a-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="efb0a-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="efb0a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="efb0a-112">Remarks</span></span>  
 <span data-ttu-id="efb0a-113">Esta função recupera o ponteiro da cadeia de caracteres de um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="efb0a-113">This function retrieves the string pointer of a string value.</span></span> <span data-ttu-id="efb0a-114">Ele falhará `JsErrorInvalidArgument` se o tipo do valor não for cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="efb0a-114">It will fail with `JsErrorInvalidArgument` if the type of the value is not string.</span></span> <span data-ttu-id="efb0a-115">O tempo de vida da cadeia de caracteres retornado será o mesmo do tempo de vida do valor que veio, mas o ponteiro da cadeia de caracteres não será considerado uma referência para o valor (e, portanto, não o deixará de ser coletado).</span><span class="sxs-lookup"><span data-stu-id="efb0a-115">The lifetime of the string returned will be the same as the lifetime of the value it came from, however the string pointer is not considered a reference to the value (and so will not keep it from being collected).</span></span>  
  
 <span data-ttu-id="efb0a-116">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="efb0a-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="efb0a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efb0a-117">Requirements</span></span>  
 <span data-ttu-id="efb0a-118">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="efb0a-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="efb0a-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="efb0a-119">See Also</span></span>  
 [<span data-ttu-id="efb0a-120">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="efb0a-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
