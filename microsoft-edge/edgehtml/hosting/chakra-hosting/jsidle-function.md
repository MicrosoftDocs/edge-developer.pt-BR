---
description: Informa o tempo de execução para fazer qualquer processamento de ociosidade necessário.
title: Função JsIdle | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ecba0aafb6b4dcccb4485c2956cae5ce4045355f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231935"
---
# <span data-ttu-id="9175d-103">Função JsIdle</span><span class="sxs-lookup"><span data-stu-id="9175d-103">JsIdle Function</span></span>

<span data-ttu-id="9175d-104">Informa o tempo de execução para fazer qualquer processamento de ociosidade necessário.</span><span class="sxs-lookup"><span data-stu-id="9175d-104">Tells the runtime to do any idle processing it need to do.</span></span>  
  
## <span data-ttu-id="9175d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9175d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIdle(  
   _Out_opt_ unsigned int *nextIdleTick  
);  
```  
  
#### <span data-ttu-id="9175d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9175d-106">Parameters</span></span>  
 `nextIdleTick`  
 <span data-ttu-id="9175d-107">O próximo tique do sistema quando houver mais trabalho ocioso a fazer.</span><span class="sxs-lookup"><span data-stu-id="9175d-107">The next system tick when there will be more idle work to do.</span></span> <span data-ttu-id="9175d-108">Pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="9175d-108">Can be null.</span></span> <span data-ttu-id="9175d-109">Retorna o número máximo de tiques se não houver nenhum trabalho ocioso futuro.</span><span class="sxs-lookup"><span data-stu-id="9175d-109">Returns the maximum number of ticks if there no upcoming idle work to do.</span></span>  
  
## <span data-ttu-id="9175d-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9175d-110">Return Value</span></span>  
 <span data-ttu-id="9175d-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="9175d-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9175d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9175d-112">Remarks</span></span>  
 <span data-ttu-id="9175d-113">Se o processamento de ociosidade tiver sido habilitado para o tempo de execução atual, a chamada `JsIdle` informará o tempo de execução atual que o host está ocioso e que o tempo de execução pode executar tarefas de limpeza de memória.</span><span class="sxs-lookup"><span data-stu-id="9175d-113">If idle processing has been enabled for the current runtime, calling `JsIdle` will inform the current runtime that the host is idle and that the runtime can perform memory cleanup tasks.</span></span>  
  
 `JsIdle` <span data-ttu-id="9175d-114">também pode retornar o número de tiques do sistema até que haja mais trabalho ocioso para o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="9175d-114">can also return the number of system ticks until there will be more idle work for the runtime to do.</span></span> <span data-ttu-id="9175d-115">Chamar `JsIdle` antes deste número de tiques aprovados não funcionará.</span><span class="sxs-lookup"><span data-stu-id="9175d-115">Calling `JsIdle` before this number of ticks has passed will do no work.</span></span>  
  
 <span data-ttu-id="9175d-116">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="9175d-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9175d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9175d-117">Requirements</span></span>  
 <span data-ttu-id="9175d-118">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9175d-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9175d-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9175d-119">See Also</span></span>  
 [<span data-ttu-id="9175d-120">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9175d-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
