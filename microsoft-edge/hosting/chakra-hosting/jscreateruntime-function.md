---
description: Cria um novo tempo de execução.
title: Função JsCreateRuntime | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRuntime
helpviewer_keywords:
- JsCreateRuntime function
ms.assetid: 92d09b89-6593-4d73-a562-88f9fec10228
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d25c1b46354be1fda0ce906dc68c3643989fe2c6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561088"
---
# <span data-ttu-id="e507d-103">Função JsCreateRuntime</span><span class="sxs-lookup"><span data-stu-id="e507d-103">JsCreateRuntime Function</span></span>
<span data-ttu-id="e507d-104">Cria um novo tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="e507d-104">Creates a new runtime.</span></span>
  
## <span data-ttu-id="e507d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e507d-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_ JsRuntimeVersion version,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### <span data-ttu-id="e507d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e507d-106">Parameters</span></span>  
 `attributes`  
 <span data-ttu-id="e507d-107">Os atributos do tempo de execução a ser criado.</span><span class="sxs-lookup"><span data-stu-id="e507d-107">The attributes of the runtime to be created.</span></span>  
  
 `version`  
 <span data-ttu-id="e507d-108">A versão do tempo de execução a ser criada.</span><span class="sxs-lookup"><span data-stu-id="e507d-108">The version of the runtime to be created.</span></span>  
  
 `threadService`  
 <span data-ttu-id="e507d-109">O serviço de thread para o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="e507d-109">The thread service for the runtime.</span></span> <span data-ttu-id="e507d-110">Pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="e507d-110">Can be null.</span></span>  
  
 `runtime`  
 <span data-ttu-id="e507d-111">O tempo de execução criado.</span><span class="sxs-lookup"><span data-stu-id="e507d-111">The runtime created.</span></span>  
  
## <span data-ttu-id="e507d-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e507d-112">Return Value</span></span>  
 <span data-ttu-id="e507d-113">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="e507d-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e507d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e507d-114">Remarks</span></span>  
 <span data-ttu-id="e507d-115">`version`Não há suporte para o parâmetro no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e507d-115">The `version` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="e507d-116">Para obter mais informações sobre o uso dessa API no modo Microsoft Edge, consulte [direcionamento de mecanismos do Microsoft Edge versus herdados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="e507d-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="e507d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e507d-117">Requirements</span></span>  
 <span data-ttu-id="e507d-118">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e507d-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e507d-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e507d-119">See Also</span></span>  
 [<span data-ttu-id="e507d-120">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e507d-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)