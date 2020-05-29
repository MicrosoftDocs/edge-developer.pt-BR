---
description: Um retorno de chamada de serviço de thread.
title: Typedef JsThreadServiceCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5eb9f2986c79db024f01f4d22050f79c9689400c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561001"
---
# <span data-ttu-id="cb542-103">Typedef JsThreadServiceCallback</span><span class="sxs-lookup"><span data-stu-id="cb542-103">JsThreadServiceCallback Typedef</span></span>
<span data-ttu-id="cb542-104">Um retorno de chamada de serviço de thread.</span><span class="sxs-lookup"><span data-stu-id="cb542-104">A thread service callback.</span></span>  
  
## <span data-ttu-id="cb542-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb542-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK *JsThreadServiceCallback)(  
   _In_ JsBackgroundWorkItemCallback callback,  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="cb542-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb542-106">Parameters</span></span>  
 <span data-ttu-id="cb542-107">retorno</span><span class="sxs-lookup"><span data-stu-id="cb542-107">callback</span></span>  
 <span data-ttu-id="cb542-108">O retorno de chamada do item de trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="cb542-108">The callback for the background work item.</span></span>  
  
 <span data-ttu-id="cb542-109">callbackData</span><span class="sxs-lookup"><span data-stu-id="cb542-109">callbackData</span></span>  
 <span data-ttu-id="cb542-110">O argumento de dados a ser passado para o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="cb542-110">The data argument to be passed to the callback.</span></span>  
  
## <span data-ttu-id="cb542-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb542-111">Remarks</span></span>  
 <span data-ttu-id="cb542-112">O host pode especificar um serviço de thread de segundo plano ao chamar JsCreateRuntime.</span><span class="sxs-lookup"><span data-stu-id="cb542-112">The host can specify a background thread service when calling JsCreateRuntime.</span></span> <span data-ttu-id="cb542-113">Se especificado, os itens de trabalho em segundo plano serão passados para o host usando esse retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="cb542-113">If specified, then background work items will be passed to the host using this callback.</span></span> <span data-ttu-id="cb542-114">O host é esperado para começar a executar o item de trabalho em segundo plano imediatamente e retornar true ou retornar false e o tempo de execução manipulará o item de trabalho no-thread.</span><span class="sxs-lookup"><span data-stu-id="cb542-114">The host is expected to either begin executing the background work item immediately and return true or return false and the runtime will handle the work item in-thread.</span></span>  
  
## <span data-ttu-id="cb542-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb542-115">Requirements</span></span>  
 <span data-ttu-id="cb542-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cb542-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cb542-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cb542-117">See Also</span></span>  
 [<span data-ttu-id="cb542-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="cb542-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)