---
description: Define os dados externos em um objeto externo.
title: Função JsSetExternalData | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetExternalData
helpviewer_keywords:
- JsSetExternalData function
ms.assetid: 94e0ad34-67d7-4f7f-88a3-3b057ef5e4b9
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f2ebdce4448a14f145ce5aafe6ba412f7db26c17
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231738"
---
# <span data-ttu-id="7ef72-103">Função JsSetExternalData</span><span class="sxs-lookup"><span data-stu-id="7ef72-103">JsSetExternalData Function</span></span>

<span data-ttu-id="7ef72-104">Define os dados externos em um objeto externo.</span><span class="sxs-lookup"><span data-stu-id="7ef72-104">Sets the external data on an external object.</span></span>  
  
## <span data-ttu-id="7ef72-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ef72-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetExternalData(  
   _In_ JsValueRef object,  
   _In_opt_ void *externalData  
);  
```  
  
#### <span data-ttu-id="7ef72-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ef72-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="7ef72-107">O objeto externo.</span><span class="sxs-lookup"><span data-stu-id="7ef72-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="7ef72-108">Os dados externos armazenados no objeto.</span><span class="sxs-lookup"><span data-stu-id="7ef72-108">The external data stored in the object.</span></span> <span data-ttu-id="7ef72-109">Pode ser NULL se não houver dados externos armazenados no objeto.</span><span class="sxs-lookup"><span data-stu-id="7ef72-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="7ef72-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7ef72-110">Return Value</span></span>  
 <span data-ttu-id="7ef72-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="7ef72-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7ef72-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ef72-112">Remarks</span></span>  
 <span data-ttu-id="7ef72-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="7ef72-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="7ef72-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ef72-114">Requirements</span></span>  
 <span data-ttu-id="7ef72-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7ef72-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7ef72-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7ef72-116">See Also</span></span>  
 [<span data-ttu-id="7ef72-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7ef72-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
