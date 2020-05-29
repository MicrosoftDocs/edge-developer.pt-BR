---
description: Um identificador para um tempo de execução do Chakra.
title: Typedef JsRuntimeHandle | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4ccdcf39ec6062db47e1b9de249d75c8804de405
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562122"
---
# <span data-ttu-id="f0b4e-103">Typedef JsRuntimeHandle</span><span class="sxs-lookup"><span data-stu-id="f0b4e-103">JsRuntimeHandle Typedef</span></span>
<span data-ttu-id="f0b4e-104">Um identificador para um tempo de execução do Chakra.</span><span class="sxs-lookup"><span data-stu-id="f0b4e-104">A handle to a Chakra runtime.</span></span>  
  
## <span data-ttu-id="f0b4e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0b4e-105">Syntax</span></span>  
  
```cpp  
typedef void *JsRuntimeHandle;  
```  
  
## <span data-ttu-id="f0b4e-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0b4e-106">Remarks</span></span>  
 <span data-ttu-id="f0b4e-107">Cada tempo de execução do Chakra tem seu próprio mecanismo de execução independente, compilador JIT e heap de lixo coletado.</span><span class="sxs-lookup"><span data-stu-id="f0b4e-107">Each Chakra runtime has its own independent execution engine, JIT compiler, and garbage collected heap.</span></span> <span data-ttu-id="f0b4e-108">Dessa forma, cada tempo de execução é completamente isolado de outros tempos de execução.</span><span class="sxs-lookup"><span data-stu-id="f0b4e-108">As such, each runtime is completely isolated from other runtimes.</span></span>  
  
 <span data-ttu-id="f0b4e-109">Os tempos de execução podem ser usados em qualquer thread, mas somente um thread pode chamar em um tempo de execução a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="f0b4e-109">Runtimes can be used on any thread, but only one thread can call into a runtime at any time.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="f0b4e-110">Um JsRuntimeHandle, diferentemente de outras referências a objetos na API de hospedagem do Chakra, não é coletado como lixo, já que contém o próprio heap coletado pelo Garbage Collector.</span><span class="sxs-lookup"><span data-stu-id="f0b4e-110">A JsRuntimeHandle, unlike other object references in the Chakra hosting API, is not garbage collected since it contains the garbage collected heap itself.</span></span> <span data-ttu-id="f0b4e-111">Um tempo de execução continuará a existir até que o JsDisposeRuntime seja chamado.</span><span class="sxs-lookup"><span data-stu-id="f0b4e-111">A runtime will continue to exist until JsDisposeRuntime is called.</span></span>  
  
## <span data-ttu-id="f0b4e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0b4e-112">Requirements</span></span>  
 <span data-ttu-id="f0b4e-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f0b4e-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f0b4e-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f0b4e-114">See Also</span></span>  
 [<span data-ttu-id="f0b4e-115">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f0b4e-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)