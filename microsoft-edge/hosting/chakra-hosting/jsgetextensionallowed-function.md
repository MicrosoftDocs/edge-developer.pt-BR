---
description: Retorna um valor que indica se um objeto é extensível ou não.
title: Função JsGetExtensionAllowed | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetExtensionAllowed
helpviewer_keywords:
- JsGetExtensionAllowed function
ms.assetid: 839054a1-d643-47d9-89db-6a015bba0d91
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e3baa6449294f7b055251d861a32095deb1bdfe9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561057"
---
# <span data-ttu-id="13cf1-103">Função JsGetExtensionAllowed</span><span class="sxs-lookup"><span data-stu-id="13cf1-103">JsGetExtensionAllowed Function</span></span>
<span data-ttu-id="13cf1-104">Retorna um valor que indica se um objeto é extensível ou não.</span><span class="sxs-lookup"><span data-stu-id="13cf1-104">Returns a value that indicates whether an object is extensible or not.</span></span>  
  
## <span data-ttu-id="13cf1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13cf1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExtensionAllowed(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="13cf1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13cf1-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="13cf1-107">O objeto a ser testado.</span><span class="sxs-lookup"><span data-stu-id="13cf1-107">The object to test.</span></span>  
  
 `value`  
 <span data-ttu-id="13cf1-108">Se o objeto é extensível ou não.</span><span class="sxs-lookup"><span data-stu-id="13cf1-108">Whether the object is extensible or not.</span></span>  
  
## <span data-ttu-id="13cf1-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13cf1-109">Return Value</span></span>  
 <span data-ttu-id="13cf1-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="13cf1-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="13cf1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="13cf1-111">Remarks</span></span>  
 <span data-ttu-id="13cf1-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="13cf1-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="13cf1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13cf1-113">Requirements</span></span>  
 <span data-ttu-id="13cf1-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="13cf1-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="13cf1-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="13cf1-115">See Also</span></span>  
 [<span data-ttu-id="13cf1-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="13cf1-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)