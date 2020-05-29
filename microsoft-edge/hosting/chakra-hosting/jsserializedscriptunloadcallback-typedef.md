---
description: Chamado pelo tempo de execução quando ele é concluído com todos os recursos relacionados à execução do script. O chamador deve liberar a origem, se carregada, o código de byte e o contexto no momento.
title: Typedef JsSerializedScriptUnloadCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9555b3fd8c14c9629d17c13592e3c78a78be150e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562120"
---
# <span data-ttu-id="e8856-104">Typedef JsSerializedScriptUnloadCallback</span><span class="sxs-lookup"><span data-stu-id="e8856-104">JsSerializedScriptUnloadCallback typedef</span></span>
<span data-ttu-id="e8856-105">Chamado pelo tempo de execução quando ele é concluído com todos os recursos relacionados à execução do script.</span><span class="sxs-lookup"><span data-stu-id="e8856-105">Called by the runtime when it is finished with all resources related to the script execution.</span></span> <span data-ttu-id="e8856-106">O chamador deve liberar a origem, se carregada, o código de byte e o contexto no momento.</span><span class="sxs-lookup"><span data-stu-id="e8856-106">The caller should free the source if loaded, the byte code, and the context at this time.</span></span>  
  
## <span data-ttu-id="e8856-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8856-107">Syntax</span></span>  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### <span data-ttu-id="e8856-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8856-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="e8856-109">O contexto passado para `JsParseSerializedScriptWithCallback` ou `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="e8856-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
## <span data-ttu-id="e8856-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8856-110">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="e8856-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8856-111">Requirements</span></span>  
 <span data-ttu-id="e8856-112">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e8856-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e8856-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e8856-113">See Also</span></span>  
 [<span data-ttu-id="e8856-114">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e8856-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)