---
description: Cria um contexto de script para executar scripts.
title: Função JsCreateContext | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateContext
helpviewer_keywords:
- JsCreateContext function
ms.assetid: aceca043-2c73-4029-a06c-8ad6695109cf
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5d6c8149b8a5e5fee7cbc8dac821713b1d9649ee
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231424"
---
# <span data-ttu-id="a927e-103">Função JsCreateContext</span><span class="sxs-lookup"><span data-stu-id="a927e-103">JsCreateContext Function</span></span>

<span data-ttu-id="a927e-104">Cria um contexto de script para executar scripts.</span><span class="sxs-lookup"><span data-stu-id="a927e-104">Creates a script context for running scripts.</span></span>  
  
## <span data-ttu-id="a927e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a927e-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ JsContextRef *newContext);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _In_ IDebugApplication *debugApplication,  
   _Out_ JsContextRef *newContext  
);  
```  
  
#### <span data-ttu-id="a927e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a927e-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="a927e-107">O tempo de execução em que o contexto do script está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="a927e-107">The runtime the script context is being created in.</span></span>  
  
 `debugApplication`  
 <span data-ttu-id="a927e-108">O aplicativo de depuração a ser usado para depuração.</span><span class="sxs-lookup"><span data-stu-id="a927e-108">The debug application to use for debugging.</span></span> <span data-ttu-id="a927e-109">Esse parâmetro pode ser nulo e, nesse caso, a depuração não está habilitada para o contexto.</span><span class="sxs-lookup"><span data-stu-id="a927e-109">This parameter can be null, in which case debugging is not enabled for the context.</span></span>  
  
 `newContext`  
 <span data-ttu-id="a927e-110">O contexto de script criado.</span><span class="sxs-lookup"><span data-stu-id="a927e-110">The created script context.</span></span>  
  
## <span data-ttu-id="a927e-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a927e-111">Return Value</span></span>  
 <span data-ttu-id="a927e-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="a927e-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a927e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a927e-113">Remarks</span></span>  
 <span data-ttu-id="a927e-114">Cada contexto de script tem seu próprio objeto global que é isolado de todos os outros contextos de script.</span><span class="sxs-lookup"><span data-stu-id="a927e-114">Each script context has its own global object that is isolated from all other script contexts.</span></span>  
  
 <span data-ttu-id="a927e-115">`debugApplication`Não há suporte para o parâmetro no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a927e-115">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="a927e-116">Para obter mais informações sobre o uso dessa API no modo Microsoft Edge, consulte [direcionamento de mecanismos do Microsoft Edge versus herdados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="a927e-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="a927e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a927e-117">Requirements</span></span>  
 <span data-ttu-id="a927e-118">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a927e-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a927e-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a927e-119">See Also</span></span>  
 [<span data-ttu-id="a927e-120">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a927e-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
