---
description: Um retorno de chamada de serviço de thread.
title: Typedef JsThreadServiceCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5f1fe416e158e9524bdd1caab847977a5dd21b8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231576"
---
# <span data-ttu-id="fbc10-103">Typedef JsThreadServiceCallback</span><span class="sxs-lookup"><span data-stu-id="fbc10-103">JsThreadServiceCallback Typedef</span></span>

<span data-ttu-id="fbc10-104">Um retorno de chamada de serviço de thread.</span><span class="sxs-lookup"><span data-stu-id="fbc10-104">A thread service callback.</span></span>  
  
## <span data-ttu-id="fbc10-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbc10-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK *JsThreadServiceCallback)(  
   _In_ JsBackgroundWorkItemCallback callback,  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="fbc10-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbc10-106">Parameters</span></span>  
 <span data-ttu-id="fbc10-107">retorno</span><span class="sxs-lookup"><span data-stu-id="fbc10-107">callback</span></span>  
 <span data-ttu-id="fbc10-108">O retorno de chamada do item de trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="fbc10-108">The callback for the background work item.</span></span>  
  
 <span data-ttu-id="fbc10-109">callbackData</span><span class="sxs-lookup"><span data-stu-id="fbc10-109">callbackData</span></span>  
 <span data-ttu-id="fbc10-110">O argumento de dados a ser passado para o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="fbc10-110">The data argument to be passed to the callback.</span></span>  
  
## <span data-ttu-id="fbc10-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbc10-111">Remarks</span></span>  
 <span data-ttu-id="fbc10-112">O host pode especificar um serviço de thread de segundo plano ao chamar JsCreateRuntime.</span><span class="sxs-lookup"><span data-stu-id="fbc10-112">The host can specify a background thread service when calling JsCreateRuntime.</span></span> <span data-ttu-id="fbc10-113">Se especificado, os itens de trabalho em segundo plano serão passados para o host usando esse retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="fbc10-113">If specified, then background work items will be passed to the host using this callback.</span></span> <span data-ttu-id="fbc10-114">O host é esperado para começar a executar o item de trabalho em segundo plano imediatamente e retornar true ou retornar false e o tempo de execução manipulará o item de trabalho no-thread.</span><span class="sxs-lookup"><span data-stu-id="fbc10-114">The host is expected to either begin executing the background work item immediately and return true or return false and the runtime will handle the work item in-thread.</span></span>  
  
## <span data-ttu-id="fbc10-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbc10-115">Requirements</span></span>  
 <span data-ttu-id="fbc10-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fbc10-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fbc10-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fbc10-117">See Also</span></span>  
 [<span data-ttu-id="fbc10-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fbc10-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
