---
description: 'Permite a execução de scripts em um tempo de execução. '
title: Função JsEnableRuntimeExecution | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEnableRuntimeExecution
helpviewer_keywords:
- JsEnableRuntimeExecution function
ms.assetid: daa2036b-aef6-497d-a8ce-5a006b6ed13f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e87191197f70898b2f69d138026edd4e75cd5114
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231622"
---
# <span data-ttu-id="cd28e-103">Função JsEnableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="cd28e-103">JsEnableRuntimeExecution Function</span></span>

<span data-ttu-id="cd28e-104">Permite a execução de scripts em um tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="cd28e-104">Enables script execution in a runtime.</span></span>  
  
## <span data-ttu-id="cd28e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd28e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="cd28e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd28e-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="cd28e-107">O tempo de execução a ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="cd28e-107">The runtime to be enabled.</span></span>  
  
## <span data-ttu-id="cd28e-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cd28e-108">Return Value</span></span>  
 <span data-ttu-id="cd28e-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="cd28e-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="cd28e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd28e-110">Remarks</span></span>  
 <span data-ttu-id="cd28e-111">Habilitar a execução de script em um tempo de execução que já tem a execução de script habilitada não é op.</span><span class="sxs-lookup"><span data-stu-id="cd28e-111">Enabling script execution in a runtime that already has script execution enabled is a no-op.</span></span>  
  
## <span data-ttu-id="cd28e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd28e-112">Requirements</span></span>  
 <span data-ttu-id="cd28e-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cd28e-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cd28e-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cd28e-114">See Also</span></span>  
 [<span data-ttu-id="cd28e-115">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="cd28e-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
