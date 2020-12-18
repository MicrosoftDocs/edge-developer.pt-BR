---
description: Executa um script serializado.
title: Função JsRunSerializedScript | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRunSerializedScript
helpviewer_keywords:
- JsRunSerializedScript function
ms.assetid: 3fd3f6f1-eb3e-4751-92a5-c93b1035f3b2
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 46f293d76bf0944c1cdedae917735c505798f4ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231919"
---
# <span data-ttu-id="2d6bf-103">Função JsRunSerializedScript</span><span class="sxs-lookup"><span data-stu-id="2d6bf-103">JsRunSerializedScript Function</span></span>

<span data-ttu-id="2d6bf-104">Executa um script serializado.</span><span class="sxs-lookup"><span data-stu-id="2d6bf-104">Runs a serialized script.</span></span>  
  
## <span data-ttu-id="2d6bf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d6bf-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="2d6bf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d6bf-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="2d6bf-107">O código-fonte do script serializado.</span><span class="sxs-lookup"><span data-stu-id="2d6bf-107">The source code of the serialized script.</span></span>  
  
 `buffer`  
 <span data-ttu-id="2d6bf-108">O script serializado.</span><span class="sxs-lookup"><span data-stu-id="2d6bf-108">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="2d6bf-109">Um cookie identificando o script que pode ser usado por contextos de script debuggable.</span><span class="sxs-lookup"><span data-stu-id="2d6bf-109">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="2d6bf-110">O local de onde o script veio.</span><span class="sxs-lookup"><span data-stu-id="2d6bf-110">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="2d6bf-111">O resultado da execução do script, se houver.</span><span class="sxs-lookup"><span data-stu-id="2d6bf-111">The result of running the script, if any.</span></span> <span data-ttu-id="2d6bf-112">Esse parâmetro pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="2d6bf-112">This parameter can be null.</span></span>  
  
## <span data-ttu-id="2d6bf-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2d6bf-113">Return Value</span></span>  
 <span data-ttu-id="2d6bf-114">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="2d6bf-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2d6bf-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d6bf-115">Remarks</span></span>  
 <span data-ttu-id="2d6bf-116">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="2d6bf-116">Requires an active script context.</span></span>  
  
 <span data-ttu-id="2d6bf-117">O buffer não é mantido na memória pelo mecanismo de script, portanto, o código deve mantê-lo ativo pelo tempo que pode ser usado para executar scripts.</span><span class="sxs-lookup"><span data-stu-id="2d6bf-117">The buffer is not persisted in memory by the scripting engine, so your code must keep it alive for as long as it might be used to execute scripts.</span></span>  
  
## <span data-ttu-id="2d6bf-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d6bf-118">Requirements</span></span>  
 <span data-ttu-id="2d6bf-119">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2d6bf-119">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2d6bf-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2d6bf-120">See Also</span></span>  
 [<span data-ttu-id="2d6bf-121">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2d6bf-121">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
