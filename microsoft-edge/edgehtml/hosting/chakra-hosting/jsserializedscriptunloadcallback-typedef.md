---
description: Chamado pelo tempo de execução quando ele é concluído com todos os recursos relacionados à execução do script. O chamador deve liberar a origem, se carregada, o código de byte e o contexto no momento.
title: Typedef JsSerializedScriptUnloadCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5c63f2ff3faf21a19e31f2f6fd1692e21d59fc0b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231933"
---
# <span data-ttu-id="ac549-104">Typedef JsSerializedScriptUnloadCallback</span><span class="sxs-lookup"><span data-stu-id="ac549-104">JsSerializedScriptUnloadCallback typedef</span></span>

<span data-ttu-id="ac549-105">Chamado pelo tempo de execução quando ele é concluído com todos os recursos relacionados à execução do script.</span><span class="sxs-lookup"><span data-stu-id="ac549-105">Called by the runtime when it is finished with all resources related to the script execution.</span></span> <span data-ttu-id="ac549-106">O chamador deve liberar a origem, se carregada, o código de byte e o contexto no momento.</span><span class="sxs-lookup"><span data-stu-id="ac549-106">The caller should free the source if loaded, the byte code, and the context at this time.</span></span>  
  
## <span data-ttu-id="ac549-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac549-107">Syntax</span></span>  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### <span data-ttu-id="ac549-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac549-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="ac549-109">O contexto passado para `JsParseSerializedScriptWithCallback` ou `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="ac549-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
## <span data-ttu-id="ac549-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac549-110">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="ac549-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac549-111">Requirements</span></span>  
 <span data-ttu-id="ac549-112">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ac549-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ac549-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ac549-113">See Also</span></span>  
 [<span data-ttu-id="ac549-114">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ac549-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
