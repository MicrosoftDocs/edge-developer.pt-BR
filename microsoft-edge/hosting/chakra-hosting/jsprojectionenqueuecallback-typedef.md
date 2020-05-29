---
description: O retorno de chamada do aplicativo que é chamado por JsRT quando uma API de projeção é concluída em um thread diferente do original.
title: Typedef JsProjectionEnqueueCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 064a7d1077ae5222e44ab08ebe0592bb97b1f2af
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561009"
---
# <span data-ttu-id="bf0c6-103">Typedef JsProjectionEnqueueCallback</span><span class="sxs-lookup"><span data-stu-id="bf0c6-103">JsProjectionEnqueueCallback Typedef</span></span>
<span data-ttu-id="bf0c6-104">O retorno de chamada do aplicativo que é chamado por JsRT quando uma API de projeção é concluída em um thread diferente do original.</span><span class="sxs-lookup"><span data-stu-id="bf0c6-104">The application callback which is called by JsRT when a projection API is completed on a different thread than the original.</span></span>  
  
## <span data-ttu-id="bf0c6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf0c6-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionEnqueueCallback)(  
  _In_ JsProjectionCallback jsCallback,  
  _In_ JsProjectionCallbackContext jsContext,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="bf0c6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf0c6-106">Parameters</span></span>  
 `jsCallback`  
 <span data-ttu-id="bf0c6-107">O retorno de chamada a ser invocado no thread original.</span><span class="sxs-lookup"><span data-stu-id="bf0c6-107">The callback to be invoked on the original thread.</span></span>  
  
 `jsContext`  
 <span data-ttu-id="bf0c6-108">O contexto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bf0c6-108">The applications context.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="bf0c6-109">O contexto JsRT que deve ser passado `jsCallback` .</span><span class="sxs-lookup"><span data-stu-id="bf0c6-109">The JsRT context that must be passed into `jsCallback`.</span></span>  
  
## <span data-ttu-id="bf0c6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf0c6-110">Remarks</span></span>  
 <span data-ttu-id="bf0c6-111">Requer chamadas JsSetProjectionEnqueueCallback para receber retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="bf0c6-111">Requires calling JsSetProjectionEnqueueCallback to receive callbacks.</span></span>  
  
 <span data-ttu-id="bf0c6-112">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="bf0c6-112">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="bf0c6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf0c6-113">Requirements</span></span>  
 <span data-ttu-id="bf0c6-114">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bf0c6-114">jsrt.h</span></span>  
  
## <span data-ttu-id="bf0c6-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bf0c6-115">See Also</span></span>  
 [<span data-ttu-id="bf0c6-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bf0c6-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)