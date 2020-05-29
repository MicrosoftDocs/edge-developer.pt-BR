---
description: Recupera os dados de um objeto externo.
title: Função JsGetExternalData | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetExternalData
helpviewer_keywords:
- JsGetExternalData function
ms.assetid: 1919e1da-3ea7-4269-a5fb-a3be06bd029b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 469d28d47f89b06897e4b72d081baad34eb92a6c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561058"
---
# <span data-ttu-id="b8ffa-103">Função JsGetExternalData</span><span class="sxs-lookup"><span data-stu-id="b8ffa-103">JsGetExternalData Function</span></span>
<span data-ttu-id="b8ffa-104">Recupera os dados de um objeto externo.</span><span class="sxs-lookup"><span data-stu-id="b8ffa-104">Retrieves the data from an external object.</span></span>  
  
## <span data-ttu-id="b8ffa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8ffa-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExternalData(  
   _In_ JsValueRef object,  
   _Out_ void **externalData  
);  
```  
  
#### <span data-ttu-id="b8ffa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8ffa-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="b8ffa-107">O objeto externo.</span><span class="sxs-lookup"><span data-stu-id="b8ffa-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="b8ffa-108">Os dados externos armazenados no objeto.</span><span class="sxs-lookup"><span data-stu-id="b8ffa-108">The external data stored in the object.</span></span> <span data-ttu-id="b8ffa-109">Pode ser NULL se não houver dados externos armazenados no objeto.</span><span class="sxs-lookup"><span data-stu-id="b8ffa-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="b8ffa-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b8ffa-110">Return Value</span></span>  
 <span data-ttu-id="b8ffa-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="b8ffa-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b8ffa-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8ffa-112">Remarks</span></span>  
 <span data-ttu-id="b8ffa-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="b8ffa-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b8ffa-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8ffa-114">Requirements</span></span>  
 <span data-ttu-id="b8ffa-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b8ffa-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b8ffa-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b8ffa-116">See Also</span></span>  
 [<span data-ttu-id="b8ffa-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b8ffa-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)