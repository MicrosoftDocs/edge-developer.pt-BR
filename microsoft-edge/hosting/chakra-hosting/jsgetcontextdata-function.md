---
description: Obtém o conjunto de dados internos no JsrtContext.
title: Função JsGetContextData | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: f5d7e446-267a-4a80-a427-6e1b95a3391b
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bd85ccbc4008897643ec3840e8cdeca3611a50c8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561067"
---
# <span data-ttu-id="a6b7e-103">Função JsGetContextData</span><span class="sxs-lookup"><span data-stu-id="a6b7e-103">JsGetContextData Function</span></span>
<span data-ttu-id="a6b7e-104">Obtém o conjunto de dados internos no JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="a6b7e-104">Gets the internal data set on JsrtContext.</span></span>  
  
## <span data-ttu-id="a6b7e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6b7e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextData(  
  _In_ JsContextRef context,  
  _Out_ void **data  
);  
```  
  
#### <span data-ttu-id="a6b7e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6b7e-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="a6b7e-107">O contexto do qual obter os dados.</span><span class="sxs-lookup"><span data-stu-id="a6b7e-107">The context to get the data from.</span></span>  
  
 `data`  
 <span data-ttu-id="a6b7e-108">O ponteiro para os dados em que os dados serão retornados.</span><span class="sxs-lookup"><span data-stu-id="a6b7e-108">The pointer to the data where data will be returned.</span></span>  
  
## <span data-ttu-id="a6b7e-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a6b7e-109">Return Value</span></span>  
 <span data-ttu-id="a6b7e-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="a6b7e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a6b7e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6b7e-111">Remarks</span></span>  
 <span data-ttu-id="a6b7e-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="a6b7e-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a6b7e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6b7e-113">Requirements</span></span>  
 <span data-ttu-id="a6b7e-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a6b7e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a6b7e-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a6b7e-115">See Also</span></span>  
 [<span data-ttu-id="a6b7e-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a6b7e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)