---
description: Um retorno de chamada chamado antes de coletar um objeto.
title: Typedef JsObjectBeforeCollectCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: f21a064a-579f-44cb-9d21-76b62e8c18f5
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 27bbd1aed72cc751397ac4e6734f107612653b66
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561013"
---
# <span data-ttu-id="08f5d-103">Typedef JsObjectBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="08f5d-103">JsObjectBeforeCollectCallback Typedef</span></span>
<span data-ttu-id="08f5d-104">Um retorno de chamada chamado antes de coletar um objeto.</span><span class="sxs-lookup"><span data-stu-id="08f5d-104">A callback called before collecting an object.</span></span>  
  
## <span data-ttu-id="08f5d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08f5d-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsObjectBeforeCollectCallback)(  
  _In_ JsRef ref,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="08f5d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08f5d-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="08f5d-107">O objeto a ser coletado.</span><span class="sxs-lookup"><span data-stu-id="08f5d-107">The object to be collected.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="08f5d-108">O estado passado para `JsSetObjectBeforeCollectCallback` .</span><span class="sxs-lookup"><span data-stu-id="08f5d-108">The state passed to `JsSetObjectBeforeCollectCallback`.</span></span>  
  
## <span data-ttu-id="08f5d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="08f5d-109">Remarks</span></span>  
 <span data-ttu-id="08f5d-110">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="08f5d-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="08f5d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08f5d-111">Requirements</span></span>  
 <span data-ttu-id="08f5d-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="08f5d-112">jsrt.h</span></span>  
  
## <span data-ttu-id="08f5d-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="08f5d-113">See Also</span></span>  
 [<span data-ttu-id="08f5d-114">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="08f5d-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)