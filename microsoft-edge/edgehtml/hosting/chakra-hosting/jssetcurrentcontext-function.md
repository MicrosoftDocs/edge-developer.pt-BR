---
description: Define o contexto do script atual no thread.
title: Função JsSetCurrentContext | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetCurrentContext
helpviewer_keywords:
- JsSetCurrentContext function
ms.assetid: 603cc94c-6585-411b-89f9-c6f144e2aa30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 60ec1760c582f1f6771a5af64f59c4a77b1a43f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231582"
---
# <span data-ttu-id="4c1bd-103">Função JsSetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="4c1bd-103">JsSetCurrentContext Function</span></span>

<span data-ttu-id="4c1bd-104">Define o contexto do script atual no thread.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-104">Sets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="4c1bd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c1bd-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetCurrentContext(  
   _In_ JsContextRef context  
);  
```  
  
#### <span data-ttu-id="4c1bd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c1bd-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="4c1bd-107">O contexto do script para torná-lo atual.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-107">The script context to make current.</span></span>  
  
## <span data-ttu-id="4c1bd-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4c1bd-108">Return Value</span></span>  
 <span data-ttu-id="4c1bd-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="4c1bd-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  

## <span data-ttu-id="4c1bd-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4c1bd-110">Example</span></span>

```cpp
JsRuntimeHandle runtime;
JsContextRef context;

// Create a runtime.
JsCreateRuntime(JsRuntimeAttributeNone, nullptr, &runtime);

// Create an execution context.
JsCreateContext(runtime, &context);

// Now set the current execution context.
JsSetCurrentContext(context);
```

## <span data-ttu-id="4c1bd-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c1bd-111">Requirements</span></span>  
 <span data-ttu-id="4c1bd-112">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4c1bd-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4c1bd-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4c1bd-113">See Also</span></span>  
 [<span data-ttu-id="4c1bd-114">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4c1bd-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
