---
description: O retorno de chamada do aplicativo que é chamado por JsRT quando uma API de projeção é concluída em um thread diferente do original.
title: Typedef JsProjectionEnqueueCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 47527d5e32076e40a82ab5452c2e0f624e8a2818
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231986"
---
# <span data-ttu-id="065aa-103">Typedef JsProjectionEnqueueCallback</span><span class="sxs-lookup"><span data-stu-id="065aa-103">JsProjectionEnqueueCallback Typedef</span></span>

<span data-ttu-id="065aa-104">O retorno de chamada do aplicativo que é chamado por JsRT quando uma API de projeção é concluída em um thread diferente do original.</span><span class="sxs-lookup"><span data-stu-id="065aa-104">The application callback which is called by JsRT when a projection API is completed on a different thread than the original.</span></span>  
  
## <span data-ttu-id="065aa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="065aa-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionEnqueueCallback)(  
  _In_ JsProjectionCallback jsCallback,  
  _In_ JsProjectionCallbackContext jsContext,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="065aa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="065aa-106">Parameters</span></span>  
 `jsCallback`  
 <span data-ttu-id="065aa-107">O retorno de chamada a ser invocado no thread original.</span><span class="sxs-lookup"><span data-stu-id="065aa-107">The callback to be invoked on the original thread.</span></span>  
  
 `jsContext`  
 <span data-ttu-id="065aa-108">O contexto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="065aa-108">The applications context.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="065aa-109">O contexto JsRT que deve ser passado `jsCallback` .</span><span class="sxs-lookup"><span data-stu-id="065aa-109">The JsRT context that must be passed into `jsCallback`.</span></span>  
  
## <span data-ttu-id="065aa-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="065aa-110">Remarks</span></span>  
 <span data-ttu-id="065aa-111">Requer chamadas JsSetProjectionEnqueueCallback para receber retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="065aa-111">Requires calling JsSetProjectionEnqueueCallback to receive callbacks.</span></span>  
  
 <span data-ttu-id="065aa-112">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="065aa-112">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="065aa-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="065aa-113">Requirements</span></span>  
 <span data-ttu-id="065aa-114">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="065aa-114">jsrt.h</span></span>  
  
## <span data-ttu-id="065aa-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="065aa-115">See Also</span></span>  
 [<span data-ttu-id="065aa-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="065aa-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
