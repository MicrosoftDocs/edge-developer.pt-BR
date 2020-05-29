---
description: Chamado pelo tempo de execução para carregar o código-fonte do script serializado. O chamador deve manter o buffer do script válido até que o `JsSerializedScriptUnloadCallback` .
title: Typedef JsSerializedScriptLoadSourceCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bc1264bdc77da10cadb44a570ae37e7f3cd9ce6b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562121"
---
# <span data-ttu-id="fce53-104">Typedef JsSerializedScriptLoadSourceCallback</span><span class="sxs-lookup"><span data-stu-id="fce53-104">JsSerializedScriptLoadSourceCallback Typedef</span></span>
<span data-ttu-id="fce53-105">Chamado pelo tempo de execução para carregar o código-fonte do script serializado.</span><span class="sxs-lookup"><span data-stu-id="fce53-105">Called by the runtime to load the source code of the serialized script.</span></span> <span data-ttu-id="fce53-106">O chamador deve manter o buffer do script válido até que o `JsSerializedScriptUnloadCallback` .</span><span class="sxs-lookup"><span data-stu-id="fce53-106">The caller must keep the script buffer valid until the `JsSerializedScriptUnloadCallback`.</span></span>  
  
## <span data-ttu-id="fce53-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fce53-107">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### <span data-ttu-id="fce53-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fce53-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="fce53-109">O contexto passado para `JsParseSerializedScriptWithCallback` ou `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="fce53-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
 `scriptBuffer`  
 <span data-ttu-id="fce53-110">O script retornou.</span><span class="sxs-lookup"><span data-stu-id="fce53-110">The script returned.</span></span>  
  
## <span data-ttu-id="fce53-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fce53-111">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="fce53-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fce53-112">Requirements</span></span>  
 <span data-ttu-id="fce53-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fce53-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fce53-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fce53-114">See Also</span></span>  
 [<span data-ttu-id="fce53-115">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fce53-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)