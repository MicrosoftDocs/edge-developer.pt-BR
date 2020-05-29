---
description: Converte o valor em cadeia de caracteres usando semântica JavaScript padrão.
title: Função JsConvertValueToString | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToString
helpviewer_keywords:
- JsConvertValueToString function
ms.assetid: a97aca04-b2ce-446a-acf4-49cd6777a85c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 21c77ca3050773c07572665c6d58e0ebc05d8ee9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561113"
---
# <span data-ttu-id="0f6d9-103">Função JsConvertValueToString</span><span class="sxs-lookup"><span data-stu-id="0f6d9-103">JsConvertValueToString Function</span></span>
<span data-ttu-id="0f6d9-104">Converte o valor em cadeia de caracteres usando semântica JavaScript padrão.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-104">Converts the value to string using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="0f6d9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f6d9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToString(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *stringValue  
);  
```  
  
#### <span data-ttu-id="0f6d9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f6d9-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="0f6d9-107">O valor a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-107">The value to be converted.</span></span>  
  
 `stringValue`  
 <span data-ttu-id="0f6d9-108">O valor convertido.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-108">The converted value.</span></span>  
  
## <span data-ttu-id="0f6d9-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0f6d9-109">Return Value</span></span>  
 <span data-ttu-id="0f6d9-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0f6d9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f6d9-111">Remarks</span></span>  
 <span data-ttu-id="0f6d9-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0f6d9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f6d9-113">Requirements</span></span>  
 <span data-ttu-id="0f6d9-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0f6d9-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0f6d9-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0f6d9-115">See Also</span></span>  
 [<span data-ttu-id="0f6d9-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0f6d9-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)