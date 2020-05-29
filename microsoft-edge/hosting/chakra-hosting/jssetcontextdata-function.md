---
description: Define os dados internos do JsrtContext.
title: Função JsSetContextData | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 00521bafdaf6125dd15746de8a1d403eaf03b4a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562117"
---
# <span data-ttu-id="60b95-103">Função JsSetContextData</span><span class="sxs-lookup"><span data-stu-id="60b95-103">JsSetContextData Function</span></span>
<span data-ttu-id="60b95-104">Define os dados internos do JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="60b95-104">Sets the internal data of JsrtContext.</span></span>  
  
## <span data-ttu-id="60b95-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60b95-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### <span data-ttu-id="60b95-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60b95-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="60b95-107">O contexto para o qual definir os dados.</span><span class="sxs-lookup"><span data-stu-id="60b95-107">The context to set the data to.</span></span>  
  
 `data`  
 <span data-ttu-id="60b95-108">O ponteiro para os dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="60b95-108">The pointer to the data to be set.</span></span>  
  
## <span data-ttu-id="60b95-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="60b95-109">Return Value</span></span>  
 <span data-ttu-id="60b95-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="60b95-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="60b95-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="60b95-111">Remarks</span></span>  
 <span data-ttu-id="60b95-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="60b95-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="60b95-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60b95-113">Requirements</span></span>  
 <span data-ttu-id="60b95-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="60b95-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="60b95-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="60b95-115">See Also</span></span>  
 [<span data-ttu-id="60b95-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="60b95-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)