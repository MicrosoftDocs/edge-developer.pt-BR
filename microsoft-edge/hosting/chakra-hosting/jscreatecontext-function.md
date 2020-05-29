---
description: Cria um contexto de script para executar scripts.
title: Função JsCreateContext | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateContext
helpviewer_keywords:
- JsCreateContext function
ms.assetid: aceca043-2c73-4029-a06c-8ad6695109cf
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 06bd4c4780a8c7610ebc95cfc0da058306ce5b78
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561108"
---
# <span data-ttu-id="660c8-103">Função JsCreateContext</span><span class="sxs-lookup"><span data-stu-id="660c8-103">JsCreateContext Function</span></span>
<span data-ttu-id="660c8-104">Cria um contexto de script para executar scripts.</span><span class="sxs-lookup"><span data-stu-id="660c8-104">Creates a script context for running scripts.</span></span>  
  
## <span data-ttu-id="660c8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="660c8-105">Syntax</span></span>  
  
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
  
#### <span data-ttu-id="660c8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="660c8-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="660c8-107">O tempo de execução em que o contexto do script está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="660c8-107">The runtime the script context is being created in.</span></span>  
  
 `debugApplication`  
 <span data-ttu-id="660c8-108">O aplicativo de depuração a ser usado para depuração.</span><span class="sxs-lookup"><span data-stu-id="660c8-108">The debug application to use for debugging.</span></span> <span data-ttu-id="660c8-109">Esse parâmetro pode ser nulo e, nesse caso, a depuração não está habilitada para o contexto.</span><span class="sxs-lookup"><span data-stu-id="660c8-109">This parameter can be null, in which case debugging is not enabled for the context.</span></span>  
  
 `newContext`  
 <span data-ttu-id="660c8-110">O contexto de script criado.</span><span class="sxs-lookup"><span data-stu-id="660c8-110">The created script context.</span></span>  
  
## <span data-ttu-id="660c8-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="660c8-111">Return Value</span></span>  
 <span data-ttu-id="660c8-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="660c8-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="660c8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="660c8-113">Remarks</span></span>  
 <span data-ttu-id="660c8-114">Cada contexto de script tem seu próprio objeto global que é isolado de todos os outros contextos de script.</span><span class="sxs-lookup"><span data-stu-id="660c8-114">Each script context has its own global object that is isolated from all other script contexts.</span></span>  
  
 <span data-ttu-id="660c8-115">`debugApplication`Não há suporte para o parâmetro no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="660c8-115">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="660c8-116">Para obter mais informações sobre o uso dessa API no modo Microsoft Edge, consulte [direcionamento de mecanismos do Microsoft Edge versus herdados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="660c8-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="660c8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="660c8-117">Requirements</span></span>  
 <span data-ttu-id="660c8-118">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="660c8-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="660c8-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="660c8-119">See Also</span></span>  
 [<span data-ttu-id="660c8-120">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="660c8-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)