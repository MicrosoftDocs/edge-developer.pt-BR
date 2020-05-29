---
description: Retorna um valor que indica se a execução do script está desabilitada no tempo de execução.
title: Função JsIsRuntimeExecutionDisabled | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6968a31c9acab70589fe58c86cc566e631778c3c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561022"
---
# <span data-ttu-id="4e00f-103">Função JsIsRuntimeExecutionDisabled</span><span class="sxs-lookup"><span data-stu-id="4e00f-103">JsIsRuntimeExecutionDisabled Function</span></span>
<span data-ttu-id="4e00f-104">Retorna um valor que indica se a execução do script está desabilitada no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="4e00f-104">Returns a value that indicates whether script execution is disabled in the runtime.</span></span>  
  
## <span data-ttu-id="4e00f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e00f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsRuntimeExecutionDisabled(    _In_ JsRuntimeHandle runtime,    _Out_ bool *isDisabled);  
```  
  
#### <span data-ttu-id="4e00f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e00f-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="4e00f-107">Especifica o tempo de execução para verificar se a execução está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="4e00f-107">Specifies the runtime to check if execution is disabled.</span></span>  
  
 `isDisabled`  
 `true` <span data-ttu-id="4e00f-108">se a execução estiver desabilitada, `false` caso contrário.</span><span class="sxs-lookup"><span data-stu-id="4e00f-108">if execution is disabled, `false` otherwise.</span></span>  
  
## <span data-ttu-id="4e00f-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4e00f-109">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="4e00f-110">se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="4e00f-110">if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4e00f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e00f-111">Requirements</span></span>  
 <span data-ttu-id="4e00f-112">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4e00f-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4e00f-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4e00f-113">See Also</span></span>  
 [<span data-ttu-id="4e00f-114">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4e00f-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)