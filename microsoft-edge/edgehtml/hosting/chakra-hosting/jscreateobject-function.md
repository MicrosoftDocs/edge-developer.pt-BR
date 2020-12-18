---
description: Cria um novo objeto.
title: Função JsCreateObject | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateObject
helpviewer_keywords:
- JsCreateObject function
ms.assetid: 6c1d01a4-9254-443e-b974-6f0b0c861ca2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d5effe7ade1679392fcad7f2bb5cea880712ef7f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231563"
---
# <span data-ttu-id="dedfc-103">Função JsCreateObject</span><span class="sxs-lookup"><span data-stu-id="dedfc-103">JsCreateObject Function</span></span>

<span data-ttu-id="dedfc-104">Cria um novo objeto.</span><span class="sxs-lookup"><span data-stu-id="dedfc-104">Creates a new object.</span></span>
  
## <span data-ttu-id="dedfc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dedfc-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateObject(  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="dedfc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dedfc-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="dedfc-107">O novo objeto.</span><span class="sxs-lookup"><span data-stu-id="dedfc-107">The new object.</span></span>  
  
## <span data-ttu-id="dedfc-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dedfc-108">Return Value</span></span>  
 <span data-ttu-id="dedfc-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="dedfc-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dedfc-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="dedfc-110">Remarks</span></span>  
 <span data-ttu-id="dedfc-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="dedfc-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="dedfc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dedfc-112">Requirements</span></span>  
 <span data-ttu-id="dedfc-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dedfc-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dedfc-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="dedfc-114">See Also</span></span>  
 [<span data-ttu-id="dedfc-115">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dedfc-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
