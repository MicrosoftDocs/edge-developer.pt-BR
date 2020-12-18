---
description: Descarta um tempo de execução.
title: Função JsDisposeRuntime | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisposeRuntime
helpviewer_keywords:
- JsDisposeRuntime function
ms.assetid: 0aefde3f-7250-48be-afc5-53ea85c12f30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8cff4578415cdf1aaa01b7203ce734cef9115301
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231626"
---
# <span data-ttu-id="b1670-103">Função JsDisposeRuntime</span><span class="sxs-lookup"><span data-stu-id="b1670-103">JsDisposeRuntime Function</span></span>

<span data-ttu-id="b1670-104">Descarta um tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="b1670-104">Disposes a runtime.</span></span>  
  
## <span data-ttu-id="b1670-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1670-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDisposeRuntime(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="b1670-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1670-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="b1670-107">O tempo de execução a ser Descartado.</span><span class="sxs-lookup"><span data-stu-id="b1670-107">The runtime to dispose.</span></span>  
  
## <span data-ttu-id="b1670-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b1670-108">Return Value</span></span>  
 <span data-ttu-id="b1670-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="b1670-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b1670-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1670-110">Remarks</span></span>  
 <span data-ttu-id="b1670-111">Depois que um tempo de execução é Descartado, todos os recursos pertencentes a ele são inválidos e não podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="b1670-111">Once a runtime has been disposed, all resources owned by it are invalid and cannot be used.</span></span> <span data-ttu-id="b1670-112">Se o tempo de execução estiver ativo (ou seja, estiver definido como atual em um determinado thread), ele não poderá ser Descartado.</span><span class="sxs-lookup"><span data-stu-id="b1670-112">If the runtime is active (i.e. it is set to be current on a particular thread), it cannot be disposed.</span></span>  
  
## <span data-ttu-id="b1670-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1670-113">Requirements</span></span>  
 <span data-ttu-id="b1670-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b1670-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b1670-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b1670-115">See Also</span></span>  
 [<span data-ttu-id="b1670-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b1670-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
