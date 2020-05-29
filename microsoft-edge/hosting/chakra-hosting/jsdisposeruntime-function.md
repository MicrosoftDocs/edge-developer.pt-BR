---
description: Descarta um tempo de execução.
title: Função JsDisposeRuntime | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDisposeRuntime
helpviewer_keywords:
- JsDisposeRuntime function
ms.assetid: 0aefde3f-7250-48be-afc5-53ea85c12f30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 89166249616c265ce75ebc43a01c838d607bdd08
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562207"
---
# <span data-ttu-id="7e1d9-103">Função JsDisposeRuntime</span><span class="sxs-lookup"><span data-stu-id="7e1d9-103">JsDisposeRuntime Function</span></span>
<span data-ttu-id="7e1d9-104">Descarta um tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-104">Disposes a runtime.</span></span>  
  
## <span data-ttu-id="7e1d9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e1d9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDisposeRuntime(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="7e1d9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e1d9-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="7e1d9-107">O tempo de execução a ser Descartado.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-107">The runtime to dispose.</span></span>  
  
## <span data-ttu-id="7e1d9-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7e1d9-108">Return Value</span></span>  
 <span data-ttu-id="7e1d9-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7e1d9-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e1d9-110">Remarks</span></span>  
 <span data-ttu-id="7e1d9-111">Depois que um tempo de execução é Descartado, todos os recursos pertencentes a ele são inválidos e não podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-111">Once a runtime has been disposed, all resources owned by it are invalid and cannot be used.</span></span> <span data-ttu-id="7e1d9-112">Se o tempo de execução estiver ativo (ou seja, estiver definido como atual em um determinado thread), ele não poderá ser Descartado.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-112">If the runtime is active (i.e. it is set to be current on a particular thread), it cannot be disposed.</span></span>  
  
## <span data-ttu-id="7e1d9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e1d9-113">Requirements</span></span>  
 <span data-ttu-id="7e1d9-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7e1d9-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7e1d9-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7e1d9-115">See Also</span></span>  
 [<span data-ttu-id="7e1d9-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7e1d9-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)