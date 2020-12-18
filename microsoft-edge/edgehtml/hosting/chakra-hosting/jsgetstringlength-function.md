---
description: Obtém o comprimento de um valor de cadeia de caracteres.
title: Função JsGetStringLength | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetStringLength
helpviewer_keywords:
- JsGetStringLength function
ms.assetid: e9f9f28c-e644-439c-aee5-7ce362f71347
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 10fd6be4bb839ccb9eb64c99931cdb474e3aa7a2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231992"
---
# <span data-ttu-id="9a078-103">Função JsGetStringLength</span><span class="sxs-lookup"><span data-stu-id="9a078-103">JsGetStringLength Function</span></span>

<span data-ttu-id="9a078-104">Obtém o comprimento de um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9a078-104">Gets the length of a string value.</span></span>  
  
## <span data-ttu-id="9a078-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a078-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetStringLength(  
   _In_ JsValueRef stringValue,  
   _Out_ int *length  
);  
```  
  
#### <span data-ttu-id="9a078-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a078-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="9a078-107">O valor da cadeia de caracteres para obter o comprimento.</span><span class="sxs-lookup"><span data-stu-id="9a078-107">The string value to get the length of.</span></span>  
  
 `length`  
 <span data-ttu-id="9a078-108">O comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9a078-108">The length of the string.</span></span>  
  
## <span data-ttu-id="9a078-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9a078-109">Return Value</span></span>  
 <span data-ttu-id="9a078-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="9a078-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9a078-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a078-111">Remarks</span></span>  
 <span data-ttu-id="9a078-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="9a078-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9a078-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a078-113">Requirements</span></span>  
 <span data-ttu-id="9a078-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9a078-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9a078-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9a078-115">See Also</span></span>  
 [<span data-ttu-id="9a078-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9a078-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
