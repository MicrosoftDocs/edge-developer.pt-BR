---
description: 'Permite a execução de scripts em um tempo de execução. '
title: Função JsEnableRuntimeExecution | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsEnableRuntimeExecution
helpviewer_keywords:
- JsEnableRuntimeExecution function
ms.assetid: daa2036b-aef6-497d-a8ce-5a006b6ed13f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: dd8071fd3c120d1c2029a3c7a3d9c39e68c4cfd2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562206"
---
# <span data-ttu-id="720c3-103">Função JsEnableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="720c3-103">JsEnableRuntimeExecution Function</span></span>
<span data-ttu-id="720c3-104">Permite a execução de scripts em um tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="720c3-104">Enables script execution in a runtime.</span></span>  
  
## <span data-ttu-id="720c3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="720c3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="720c3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="720c3-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="720c3-107">O tempo de execução a ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="720c3-107">The runtime to be enabled.</span></span>  
  
## <span data-ttu-id="720c3-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="720c3-108">Return Value</span></span>  
 <span data-ttu-id="720c3-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="720c3-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="720c3-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="720c3-110">Remarks</span></span>  
 <span data-ttu-id="720c3-111">Habilitar a execução de script em um tempo de execução que já tem a execução de script habilitada não é op.</span><span class="sxs-lookup"><span data-stu-id="720c3-111">Enabling script execution in a runtime that already has script execution enabled is a no-op.</span></span>  
  
## <span data-ttu-id="720c3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="720c3-112">Requirements</span></span>  
 <span data-ttu-id="720c3-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="720c3-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="720c3-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="720c3-114">See Also</span></span>  
 [<span data-ttu-id="720c3-115">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="720c3-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)