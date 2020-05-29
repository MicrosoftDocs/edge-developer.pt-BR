---
description: Informa o tempo de execução para fazer qualquer processamento de ociosidade necessário.
title: Função JsIdle | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4da7148bf7daa3db983ab8f5bba622bfe0b19466
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562157"
---
# <span data-ttu-id="f61cb-103">Função JsIdle</span><span class="sxs-lookup"><span data-stu-id="f61cb-103">JsIdle Function</span></span>
<span data-ttu-id="f61cb-104">Informa o tempo de execução para fazer qualquer processamento de ociosidade necessário.</span><span class="sxs-lookup"><span data-stu-id="f61cb-104">Tells the runtime to do any idle processing it need to do.</span></span>  
  
## <span data-ttu-id="f61cb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f61cb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIdle(  
   _Out_opt_ unsigned int *nextIdleTick  
);  
```  
  
#### <span data-ttu-id="f61cb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f61cb-106">Parameters</span></span>  
 `nextIdleTick`  
 <span data-ttu-id="f61cb-107">O próximo tique do sistema quando houver mais trabalho ocioso a fazer.</span><span class="sxs-lookup"><span data-stu-id="f61cb-107">The next system tick when there will be more idle work to do.</span></span> <span data-ttu-id="f61cb-108">Pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="f61cb-108">Can be null.</span></span> <span data-ttu-id="f61cb-109">Retorna o número máximo de tiques se não houver nenhum trabalho ocioso futuro.</span><span class="sxs-lookup"><span data-stu-id="f61cb-109">Returns the maximum number of ticks if there no upcoming idle work to do.</span></span>  
  
## <span data-ttu-id="f61cb-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f61cb-110">Return Value</span></span>  
 <span data-ttu-id="f61cb-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="f61cb-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f61cb-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f61cb-112">Remarks</span></span>  
 <span data-ttu-id="f61cb-113">Se o processamento de ociosidade tiver sido habilitado para o tempo de execução atual, a chamada `JsIdle` informará o tempo de execução atual que o host está ocioso e que o tempo de execução pode executar tarefas de limpeza de memória.</span><span class="sxs-lookup"><span data-stu-id="f61cb-113">If idle processing has been enabled for the current runtime, calling `JsIdle` will inform the current runtime that the host is idle and that the runtime can perform memory cleanup tasks.</span></span>  
  
 `JsIdle` <span data-ttu-id="f61cb-114">também pode retornar o número de tiques do sistema até que haja mais trabalho ocioso para o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f61cb-114">can also return the number of system ticks until there will be more idle work for the runtime to do.</span></span> <span data-ttu-id="f61cb-115">Chamar `JsIdle` antes deste número de tiques aprovados não funcionará.</span><span class="sxs-lookup"><span data-stu-id="f61cb-115">Calling `JsIdle` before this number of ticks has passed will do no work.</span></span>  
  
 <span data-ttu-id="f61cb-116">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="f61cb-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f61cb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f61cb-117">Requirements</span></span>  
 <span data-ttu-id="f61cb-118">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f61cb-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f61cb-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f61cb-119">See Also</span></span>  
 [<span data-ttu-id="f61cb-120">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f61cb-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)