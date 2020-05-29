---
description: Define os dados externos em um objeto externo.
title: Função JsSetExternalData | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetExternalData
helpviewer_keywords:
- JsSetExternalData function
ms.assetid: 94e0ad34-67d7-4f7f-88a3-3b057ef5e4b9
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: cc638905786a1baa0a3d5f79bfa3792a764f358f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562111"
---
# <span data-ttu-id="84959-103">Função JsSetExternalData</span><span class="sxs-lookup"><span data-stu-id="84959-103">JsSetExternalData Function</span></span>
<span data-ttu-id="84959-104">Define os dados externos em um objeto externo.</span><span class="sxs-lookup"><span data-stu-id="84959-104">Sets the external data on an external object.</span></span>  
  
## <span data-ttu-id="84959-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84959-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetExternalData(  
   _In_ JsValueRef object,  
   _In_opt_ void *externalData  
);  
```  
  
#### <span data-ttu-id="84959-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84959-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="84959-107">O objeto externo.</span><span class="sxs-lookup"><span data-stu-id="84959-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="84959-108">Os dados externos armazenados no objeto.</span><span class="sxs-lookup"><span data-stu-id="84959-108">The external data stored in the object.</span></span> <span data-ttu-id="84959-109">Pode ser NULL se não houver dados externos armazenados no objeto.</span><span class="sxs-lookup"><span data-stu-id="84959-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="84959-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="84959-110">Return Value</span></span>  
 <span data-ttu-id="84959-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="84959-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="84959-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="84959-112">Remarks</span></span>  
 <span data-ttu-id="84959-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="84959-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="84959-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84959-114">Requirements</span></span>  
 <span data-ttu-id="84959-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="84959-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="84959-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="84959-116">See Also</span></span>  
 [<span data-ttu-id="84959-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="84959-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)