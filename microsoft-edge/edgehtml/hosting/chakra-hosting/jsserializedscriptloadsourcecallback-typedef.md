---
description: Chamado pelo tempo de execução para carregar o código-fonte do script serializado. O chamador deve manter o buffer do script válido até que o `JsSerializedScriptUnloadCallback` .
title: Typedef JsSerializedScriptLoadSourceCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2bb30befc61003d20cdeaa293fd1fdfdc95b36f7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231983"
---
# <span data-ttu-id="72415-104">Typedef JsSerializedScriptLoadSourceCallback</span><span class="sxs-lookup"><span data-stu-id="72415-104">JsSerializedScriptLoadSourceCallback Typedef</span></span>

<span data-ttu-id="72415-105">Chamado pelo tempo de execução para carregar o código-fonte do script serializado.</span><span class="sxs-lookup"><span data-stu-id="72415-105">Called by the runtime to load the source code of the serialized script.</span></span> <span data-ttu-id="72415-106">O chamador deve manter o buffer do script válido até que o `JsSerializedScriptUnloadCallback` .</span><span class="sxs-lookup"><span data-stu-id="72415-106">The caller must keep the script buffer valid until the `JsSerializedScriptUnloadCallback`.</span></span>  
  
## <span data-ttu-id="72415-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72415-107">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### <span data-ttu-id="72415-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72415-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="72415-109">O contexto passado para `JsParseSerializedScriptWithCallback` ou `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="72415-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
 `scriptBuffer`  
 <span data-ttu-id="72415-110">O script retornou.</span><span class="sxs-lookup"><span data-stu-id="72415-110">The script returned.</span></span>  
  
## <span data-ttu-id="72415-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="72415-111">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="72415-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72415-112">Requirements</span></span>  
 <span data-ttu-id="72415-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="72415-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="72415-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="72415-114">See Also</span></span>  
 [<span data-ttu-id="72415-115">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="72415-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
