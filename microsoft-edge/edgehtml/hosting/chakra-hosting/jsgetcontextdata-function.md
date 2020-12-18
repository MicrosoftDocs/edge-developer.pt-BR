---
description: Obtém o conjunto de dados internos no JsrtContext.
title: Função JsGetContextData | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: f5d7e446-267a-4a80-a427-6e1b95a3391b
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8f5f70a9c36fea355792050c1a2a810bca2d07b3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231547"
---
# <span data-ttu-id="33477-103">Função JsGetContextData</span><span class="sxs-lookup"><span data-stu-id="33477-103">JsGetContextData Function</span></span>

<span data-ttu-id="33477-104">Obtém o conjunto de dados internos no JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="33477-104">Gets the internal data set on JsrtContext.</span></span>  
  
## <span data-ttu-id="33477-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33477-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextData(  
  _In_ JsContextRef context,  
  _Out_ void **data  
);  
```  
  
#### <span data-ttu-id="33477-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33477-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="33477-107">O contexto do qual obter os dados.</span><span class="sxs-lookup"><span data-stu-id="33477-107">The context to get the data from.</span></span>  
  
 `data`  
 <span data-ttu-id="33477-108">O ponteiro para os dados em que os dados serão retornados.</span><span class="sxs-lookup"><span data-stu-id="33477-108">The pointer to the data where data will be returned.</span></span>  
  
## <span data-ttu-id="33477-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="33477-109">Return Value</span></span>  
 <span data-ttu-id="33477-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="33477-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="33477-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="33477-111">Remarks</span></span>  
 <span data-ttu-id="33477-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="33477-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="33477-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33477-113">Requirements</span></span>  
 <span data-ttu-id="33477-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="33477-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="33477-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="33477-115">See Also</span></span>  
 [<span data-ttu-id="33477-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="33477-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
