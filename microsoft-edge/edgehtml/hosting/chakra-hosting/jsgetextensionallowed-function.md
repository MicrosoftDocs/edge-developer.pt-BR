---
description: Retorna um valor que indica se um objeto é extensível ou não.
title: Função JsGetExtensionAllowed | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetExtensionAllowed
helpviewer_keywords:
- JsGetExtensionAllowed function
ms.assetid: 839054a1-d643-47d9-89db-6a015bba0d91
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7bc9e3265b48a27d0da4bc4646b2b5e3b1765b86
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231669"
---
# <span data-ttu-id="cad05-103">Função JsGetExtensionAllowed</span><span class="sxs-lookup"><span data-stu-id="cad05-103">JsGetExtensionAllowed Function</span></span>

<span data-ttu-id="cad05-104">Retorna um valor que indica se um objeto é extensível ou não.</span><span class="sxs-lookup"><span data-stu-id="cad05-104">Returns a value that indicates whether an object is extensible or not.</span></span>  
  
## <span data-ttu-id="cad05-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cad05-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExtensionAllowed(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="cad05-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cad05-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="cad05-107">O objeto a ser testado.</span><span class="sxs-lookup"><span data-stu-id="cad05-107">The object to test.</span></span>  
  
 `value`  
 <span data-ttu-id="cad05-108">Se o objeto é extensível ou não.</span><span class="sxs-lookup"><span data-stu-id="cad05-108">Whether the object is extensible or not.</span></span>  
  
## <span data-ttu-id="cad05-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cad05-109">Return Value</span></span>  
 <span data-ttu-id="cad05-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="cad05-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="cad05-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cad05-111">Remarks</span></span>  
 <span data-ttu-id="cad05-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="cad05-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="cad05-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cad05-113">Requirements</span></span>  
 <span data-ttu-id="cad05-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cad05-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cad05-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cad05-115">See Also</span></span>  
 [<span data-ttu-id="cad05-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="cad05-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
