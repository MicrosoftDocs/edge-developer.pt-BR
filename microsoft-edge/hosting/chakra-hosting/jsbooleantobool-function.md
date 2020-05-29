---
description: Recupera o `bool` valor de um valor booliano.
title: Função JsBooleanToBool | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsBooleanToBool
helpviewer_keywords:
- JsBooleanToBool function
ms.assetid: ab16ac71-fe47-475d-a7ee-46e4643dee60
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 55b0ef1278cbc73652fc8427e004cab002d76e5b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561133"
---
# <span data-ttu-id="f8021-103">Função JsBooleanToBool</span><span class="sxs-lookup"><span data-stu-id="f8021-103">JsBooleanToBool Function</span></span>
<span data-ttu-id="f8021-104">Recupera o `bool` valor de um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="f8021-104">Retrieves the `bool` value of a Boolean value.</span></span>  
  
## <span data-ttu-id="f8021-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8021-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsBooleanToBool(  
   _In_ JsValueRef value,  
   _Out_ bool *boolValue  
);  
```  
  
#### <span data-ttu-id="f8021-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8021-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="f8021-107">O valor a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="f8021-107">The value to be converted.</span></span>  
  
 `boolValue`  
 <span data-ttu-id="f8021-108">O valor convertido.</span><span class="sxs-lookup"><span data-stu-id="f8021-108">The converted value.</span></span>  
  
## <span data-ttu-id="f8021-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f8021-109">Return Value</span></span>  
 <span data-ttu-id="f8021-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="f8021-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f8021-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8021-111">Remarks</span></span>  
 <span data-ttu-id="f8021-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="f8021-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f8021-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8021-113">Requirements</span></span>  
 <span data-ttu-id="f8021-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f8021-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f8021-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f8021-115">See Also</span></span>  
 [<span data-ttu-id="f8021-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f8021-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)