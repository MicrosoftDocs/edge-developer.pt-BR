---
description: Define o contexto do script atual no thread.
title: Função JsSetCurrentContext | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetCurrentContext
helpviewer_keywords:
- JsSetCurrentContext function
ms.assetid: 603cc94c-6585-411b-89f9-c6f144e2aa30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 57620ad0e986034791ec07765d7cc115b958d661
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562116"
---
# <span data-ttu-id="ec80d-103">Função JsSetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="ec80d-103">JsSetCurrentContext Function</span></span>
<span data-ttu-id="ec80d-104">Define o contexto do script atual no thread.</span><span class="sxs-lookup"><span data-stu-id="ec80d-104">Sets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="ec80d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec80d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetCurrentContext(  
   _In_ JsContextRef context  
);  
```  
  
#### <span data-ttu-id="ec80d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec80d-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="ec80d-107">O contexto do script para torná-lo atual.</span><span class="sxs-lookup"><span data-stu-id="ec80d-107">The script context to make current.</span></span>  
  
## <span data-ttu-id="ec80d-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ec80d-108">Return Value</span></span>  
 <span data-ttu-id="ec80d-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="ec80d-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  

## <span data-ttu-id="ec80d-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ec80d-110">Example</span></span>

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

## <span data-ttu-id="ec80d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec80d-111">Requirements</span></span>  
 <span data-ttu-id="ec80d-112">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ec80d-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ec80d-113">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ec80d-113">See Also</span></span>  
 [<span data-ttu-id="ec80d-114">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ec80d-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)