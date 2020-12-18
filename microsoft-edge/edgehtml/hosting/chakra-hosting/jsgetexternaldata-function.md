---
description: Recupera os dados de um objeto externo.
title: Função JsGetExternalData | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetExternalData
helpviewer_keywords:
- JsGetExternalData function
ms.assetid: 1919e1da-3ea7-4269-a5fb-a3be06bd029b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d046b5c515b1a688cd527fdc0eb9cd173eb47570
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231668"
---
# <span data-ttu-id="db8b6-103">Função JsGetExternalData</span><span class="sxs-lookup"><span data-stu-id="db8b6-103">JsGetExternalData Function</span></span>

<span data-ttu-id="db8b6-104">Recupera os dados de um objeto externo.</span><span class="sxs-lookup"><span data-stu-id="db8b6-104">Retrieves the data from an external object.</span></span>  
  
## <span data-ttu-id="db8b6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db8b6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExternalData(  
   _In_ JsValueRef object,  
   _Out_ void **externalData  
);  
```  
  
#### <span data-ttu-id="db8b6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db8b6-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="db8b6-107">O objeto externo.</span><span class="sxs-lookup"><span data-stu-id="db8b6-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="db8b6-108">Os dados externos armazenados no objeto.</span><span class="sxs-lookup"><span data-stu-id="db8b6-108">The external data stored in the object.</span></span> <span data-ttu-id="db8b6-109">Pode ser NULL se não houver dados externos armazenados no objeto.</span><span class="sxs-lookup"><span data-stu-id="db8b6-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="db8b6-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="db8b6-110">Return Value</span></span>  
 <span data-ttu-id="db8b6-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="db8b6-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="db8b6-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="db8b6-112">Remarks</span></span>  
 <span data-ttu-id="db8b6-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="db8b6-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="db8b6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db8b6-114">Requirements</span></span>  
 <span data-ttu-id="db8b6-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="db8b6-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="db8b6-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="db8b6-116">See Also</span></span>  
 [<span data-ttu-id="db8b6-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="db8b6-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
