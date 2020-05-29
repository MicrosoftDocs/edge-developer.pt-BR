---
description: Um retorno de chamada de item de trabalho em segundo plano.
title: Typedef JsBackgroundWorkItemCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9bc1e5687d92d7286e1e6d4387bd6b69d95ceb68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561135"
---
# <span data-ttu-id="9eb20-103">Typedef JsBackgroundWorkItemCallback</span><span class="sxs-lookup"><span data-stu-id="9eb20-103">JsBackgroundWorkItemCallback Typedef</span></span>
<span data-ttu-id="9eb20-104">Um retorno de chamada de item de trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="9eb20-104">A background work item callback.</span></span>  
  
## <span data-ttu-id="9eb20-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9eb20-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBackgroundWorkItemCallback)(  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="9eb20-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9eb20-106">Parameters</span></span>  
 <span data-ttu-id="9eb20-107">callbackData</span><span class="sxs-lookup"><span data-stu-id="9eb20-107">callbackData</span></span>  
 <span data-ttu-id="9eb20-108">Argumento de dados passado para o serviço de thread.</span><span class="sxs-lookup"><span data-stu-id="9eb20-108">Data argument passed to the thread service.</span></span>  
  
## <span data-ttu-id="9eb20-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="9eb20-109">Remarks</span></span>  
 <span data-ttu-id="9eb20-110">Isso é passado para o serviço de thread do host (se for fornecido) para permitir que o host invoque o retorno de chamada de item de trabalho no thread de segundo plano de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="9eb20-110">This is passed to the host's thread service (if provided) to allow the host to invoke the work item callback on the background thread of its choice.</span></span>  
  
## <span data-ttu-id="9eb20-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9eb20-111">Requirements</span></span>  
 <span data-ttu-id="9eb20-112">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9eb20-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9eb20-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9eb20-113">See Also</span></span>  
 [<span data-ttu-id="9eb20-114">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9eb20-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)