---
description: Cria um novo objeto.
title: Função JsCreateObject | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateObject
helpviewer_keywords:
- JsCreateObject function
ms.assetid: 6c1d01a4-9254-443e-b974-6f0b0c861ca2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9ed988aae0921978819d379562d4a966e4a082a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561093"
---
# <span data-ttu-id="56f3d-103">Função JsCreateObject</span><span class="sxs-lookup"><span data-stu-id="56f3d-103">JsCreateObject Function</span></span>
<span data-ttu-id="56f3d-104">Cria um novo objeto.</span><span class="sxs-lookup"><span data-stu-id="56f3d-104">Creates a new object.</span></span>
  
## <span data-ttu-id="56f3d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56f3d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateObject(  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="56f3d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56f3d-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="56f3d-107">O novo objeto.</span><span class="sxs-lookup"><span data-stu-id="56f3d-107">The new object.</span></span>  
  
## <span data-ttu-id="56f3d-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="56f3d-108">Return Value</span></span>  
 <span data-ttu-id="56f3d-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="56f3d-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="56f3d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="56f3d-110">Remarks</span></span>  
 <span data-ttu-id="56f3d-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="56f3d-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="56f3d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56f3d-112">Requirements</span></span>  
 <span data-ttu-id="56f3d-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="56f3d-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="56f3d-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="56f3d-114">See Also</span></span>  
 [<span data-ttu-id="56f3d-115">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="56f3d-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)