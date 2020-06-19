---
description: Chamado pelo tempo de execução para carregar o código-fonte do script serializado. O chamador deve manter o buffer do script válido até que o `JsSerializedScriptUnloadCallback` .
title: Typedef JsSerializedScriptLoadSourceCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 571314145cc19513f04174a9a1c93822a5795b29
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752196"
---
# <span data-ttu-id="562f9-104">Typedef JsSerializedScriptLoadSourceCallback</span><span class="sxs-lookup"><span data-stu-id="562f9-104">JsSerializedScriptLoadSourceCallback Typedef</span></span>
<span data-ttu-id="562f9-105">Chamado pelo tempo de execução para carregar o código-fonte do script serializado.</span><span class="sxs-lookup"><span data-stu-id="562f9-105">Called by the runtime to load the source code of the serialized script.</span></span> <span data-ttu-id="562f9-106">O chamador deve manter o buffer do script válido até que o `JsSerializedScriptUnloadCallback` .</span><span class="sxs-lookup"><span data-stu-id="562f9-106">The caller must keep the script buffer valid until the `JsSerializedScriptUnloadCallback`.</span></span>  
  
## <span data-ttu-id="562f9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="562f9-107">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### <span data-ttu-id="562f9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="562f9-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="562f9-109">O contexto passado para `JsParseSerializedScriptWithCallback` ou `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="562f9-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
 `scriptBuffer`  
 <span data-ttu-id="562f9-110">O script retornou.</span><span class="sxs-lookup"><span data-stu-id="562f9-110">The script returned.</span></span>  
  
## <span data-ttu-id="562f9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="562f9-111">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="562f9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="562f9-112">Requirements</span></span>  
 <span data-ttu-id="562f9-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="562f9-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="562f9-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="562f9-114">See Also</span></span>  
 [<span data-ttu-id="562f9-115">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="562f9-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)