---
description: Cria um novo tempo de execução.
title: Função JsCreateRuntime | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRuntime
helpviewer_keywords:
- JsCreateRuntime function
ms.assetid: 92d09b89-6593-4d73-a562-88f9fec10228
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3b893bd75725d6d9da56417ba83adfce18d77bac
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231643"
---
# <span data-ttu-id="0b6a0-103">Função JsCreateRuntime</span><span class="sxs-lookup"><span data-stu-id="0b6a0-103">JsCreateRuntime Function</span></span>

<span data-ttu-id="0b6a0-104">Cria um novo tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="0b6a0-104">Creates a new runtime.</span></span>
  
## <span data-ttu-id="0b6a0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b6a0-105">Syntax</span></span>  
  
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
  
#### <span data-ttu-id="0b6a0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b6a0-106">Parameters</span></span>  
 `attributes`  
 <span data-ttu-id="0b6a0-107">Os atributos do tempo de execução a ser criado.</span><span class="sxs-lookup"><span data-stu-id="0b6a0-107">The attributes of the runtime to be created.</span></span>  
  
 `version`  
 <span data-ttu-id="0b6a0-108">A versão do tempo de execução a ser criada.</span><span class="sxs-lookup"><span data-stu-id="0b6a0-108">The version of the runtime to be created.</span></span>  
  
 `threadService`  
 <span data-ttu-id="0b6a0-109">O serviço de thread para o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="0b6a0-109">The thread service for the runtime.</span></span> <span data-ttu-id="0b6a0-110">Pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="0b6a0-110">Can be null.</span></span>  
  
 `runtime`  
 <span data-ttu-id="0b6a0-111">O tempo de execução criado.</span><span class="sxs-lookup"><span data-stu-id="0b6a0-111">The runtime created.</span></span>  
  
## <span data-ttu-id="0b6a0-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0b6a0-112">Return Value</span></span>  
 <span data-ttu-id="0b6a0-113">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="0b6a0-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0b6a0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b6a0-114">Remarks</span></span>  
 <span data-ttu-id="0b6a0-115">`version`Não há suporte para o parâmetro no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0b6a0-115">The `version` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="0b6a0-116">Para obter mais informações sobre o uso dessa API no modo Microsoft Edge, consulte [direcionamento de mecanismos do Microsoft Edge versus herdados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="0b6a0-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="0b6a0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b6a0-117">Requirements</span></span>  
 <span data-ttu-id="0b6a0-118">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0b6a0-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0b6a0-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0b6a0-119">See Also</span></span>  
 [<span data-ttu-id="0b6a0-120">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0b6a0-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
