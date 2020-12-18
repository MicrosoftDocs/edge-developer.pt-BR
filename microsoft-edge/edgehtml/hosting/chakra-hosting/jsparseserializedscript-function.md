---
description: Analisa um script serializado e retorna uma função que representa o script.
title: Função JsParseSerializedScript | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsParseSerializedScript
helpviewer_keywords:
- JsParseSerializedScript function
ms.assetid: 40d0c7c4-fd5b-46ed-9e65-38c2db2fc859
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 66ecabb9d96c3f339625f93858444f55d25fd4d7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231756"
---
# <span data-ttu-id="735c8-103">Função JsParseSerializedScript</span><span class="sxs-lookup"><span data-stu-id="735c8-103">JsParseSerializedScript Function</span></span>

<span data-ttu-id="735c8-104">Analisa um script serializado e retorna uma função que representa o script.</span><span class="sxs-lookup"><span data-stu-id="735c8-104">Parses a serialized script and returns a function representing the script.</span></span>  
  
## <span data-ttu-id="735c8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="735c8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="735c8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="735c8-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="735c8-107">O script a ser analisado.</span><span class="sxs-lookup"><span data-stu-id="735c8-107">The script to parse.</span></span>  
  
 `buffer`  
 <span data-ttu-id="735c8-108">O script serializado.</span><span class="sxs-lookup"><span data-stu-id="735c8-108">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="735c8-109">Um cookie identificando o script que pode ser usado por contextos de script debuggable.</span><span class="sxs-lookup"><span data-stu-id="735c8-109">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="735c8-110">O local de onde o script veio.</span><span class="sxs-lookup"><span data-stu-id="735c8-110">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="735c8-111">Uma função que representa o código de script.</span><span class="sxs-lookup"><span data-stu-id="735c8-111">A function representing the script code.</span></span>  
  
## <span data-ttu-id="735c8-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="735c8-112">Return Value</span></span>  
 <span data-ttu-id="735c8-113">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="735c8-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="735c8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="735c8-114">Remarks</span></span>  
 <span data-ttu-id="735c8-115">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="735c8-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="735c8-116">O buffer não é mantido na memória pelo mecanismo de script, portanto, o código deve mantê-lo ativo pelo tempo que pode ser usado para executar scripts.</span><span class="sxs-lookup"><span data-stu-id="735c8-116">The buffer is not persisted in memory by the scripting engine, so your code must keep it alive for as long as it might be used to execute scripts.</span></span>  
  
## <span data-ttu-id="735c8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="735c8-117">Requirements</span></span>  
 <span data-ttu-id="735c8-118">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="735c8-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="735c8-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="735c8-119">See Also</span></span>  
 [<span data-ttu-id="735c8-120">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="735c8-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
