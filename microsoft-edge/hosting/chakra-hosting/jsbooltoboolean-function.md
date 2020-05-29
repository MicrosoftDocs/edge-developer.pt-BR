---
description: Cria um valor booliano a partir de um `bool` valor.
title: Função JsBoolToBoolean | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsBoolToBoolean
helpviewer_keywords:
- JsBoolToBoolean function
ms.assetid: 24322ea3-0638-40a3-9b4c-fc912ebed3ff
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f795bdd02a2a21dc4a0c8948a76ef817d6e0fac6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561131"
---
# <span data-ttu-id="52306-103">Função JsBoolToBoolean</span><span class="sxs-lookup"><span data-stu-id="52306-103">JsBoolToBoolean Function</span></span>
<span data-ttu-id="52306-104">Cria um valor booliano a partir de um `bool` valor.</span><span class="sxs-lookup"><span data-stu-id="52306-104">Creates a Boolean value from a `bool` value.</span></span>  
  
## <span data-ttu-id="52306-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52306-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode JsBoolToBoolean(  
   _In_ bool value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="52306-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52306-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="52306-107">O valor a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="52306-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="52306-108">O valor convertido.</span><span class="sxs-lookup"><span data-stu-id="52306-108">The converted value.</span></span>  
  
## <span data-ttu-id="52306-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="52306-109">Return Value</span></span>  
 <span data-ttu-id="52306-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="52306-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="52306-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="52306-111">Remarks</span></span>  
 <span data-ttu-id="52306-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="52306-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="52306-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52306-113">Requirements</span></span>  
 <span data-ttu-id="52306-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="52306-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="52306-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="52306-115">See Also</span></span>  
 [<span data-ttu-id="52306-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="52306-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)