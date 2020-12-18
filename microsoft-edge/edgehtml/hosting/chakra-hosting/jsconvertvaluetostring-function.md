---
description: Converte o valor em cadeia de caracteres usando semântica JavaScript padrão.
title: Função JsConvertValueToString | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToString
helpviewer_keywords:
- JsConvertValueToString function
ms.assetid: a97aca04-b2ce-446a-acf4-49cd6777a85c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 499f9555f6385b8458524fb4e14b92339c0aa478
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231426"
---
# <span data-ttu-id="9705e-103">Função JsConvertValueToString</span><span class="sxs-lookup"><span data-stu-id="9705e-103">JsConvertValueToString Function</span></span>

<span data-ttu-id="9705e-104">Converte o valor em cadeia de caracteres usando semântica JavaScript padrão.</span><span class="sxs-lookup"><span data-stu-id="9705e-104">Converts the value to string using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="9705e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9705e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToString(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *stringValue  
);  
```  
  
#### <span data-ttu-id="9705e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9705e-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="9705e-107">O valor a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="9705e-107">The value to be converted.</span></span>  
  
 `stringValue`  
 <span data-ttu-id="9705e-108">O valor convertido.</span><span class="sxs-lookup"><span data-stu-id="9705e-108">The converted value.</span></span>  
  
## <span data-ttu-id="9705e-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9705e-109">Return Value</span></span>  
 <span data-ttu-id="9705e-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="9705e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9705e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9705e-111">Remarks</span></span>  
 <span data-ttu-id="9705e-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="9705e-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9705e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9705e-113">Requirements</span></span>  
 <span data-ttu-id="9705e-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9705e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9705e-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9705e-115">See Also</span></span>  
 [<span data-ttu-id="9705e-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9705e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
