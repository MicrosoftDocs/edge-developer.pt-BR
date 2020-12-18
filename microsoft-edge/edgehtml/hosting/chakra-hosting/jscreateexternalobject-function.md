---
description: Cria um novo objeto que armazena alguns dados externos.
title: Função JsCreateExternalObject | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateExternalObject
helpviewer_keywords:
- JsCreateExternalObject function
ms.assetid: 6bcef506-93fb-429b-b06a-a971ff0b71f3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4d402c3d379a16186daaba601c7f830c53a9a953
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231936"
---
# <span data-ttu-id="ba0a5-103">Função JsCreateExternalObject</span><span class="sxs-lookup"><span data-stu-id="ba0a5-103">JsCreateExternalObject Function</span></span>

<span data-ttu-id="ba0a5-104">Cria um novo objeto que armazena alguns dados externos.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-104">Creates a new object that stores some external data.</span></span>
  
## <span data-ttu-id="ba0a5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba0a5-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalObject(  
   _In_opt_ void *data,  
   _In_opt_ JsFinalizeCallback finalizeCallback,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="ba0a5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba0a5-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="ba0a5-107">Dados externos a serem representados pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-107">External data that the object will represent.</span></span> <span data-ttu-id="ba0a5-108">Pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-108">May be null.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="ba0a5-109">Um retorno de chamada para quando o objeto for finalizado.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="ba0a5-110">Pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-110">May be null.</span></span>  
  
 `object`  
 <span data-ttu-id="ba0a5-111">O novo objeto.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-111">The new object.</span></span>  
  
## <span data-ttu-id="ba0a5-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ba0a5-112">Return Value</span></span>  
 <span data-ttu-id="ba0a5-113">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ba0a5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba0a5-114">Remarks</span></span>  
 <span data-ttu-id="ba0a5-115">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="ba0a5-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ba0a5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba0a5-116">Requirements</span></span>  
 <span data-ttu-id="ba0a5-117">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ba0a5-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ba0a5-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ba0a5-118">See Also</span></span>  
 [<span data-ttu-id="ba0a5-119">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ba0a5-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
