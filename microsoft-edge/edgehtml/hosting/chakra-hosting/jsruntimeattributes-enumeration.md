---
description: 'Atributos de um tempo de execução. '
title: Enumeração JsRuntimeAttributes | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRuntimeAttributes
helpviewer_keywords:
- JsRuntimeAttributes enumeration
ms.assetid: f76d82e9-a695-4d6a-96c1-b3a4d27fed68
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bbc5341c3214d9796278d334507e284989ff45dd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231546"
---
# <span data-ttu-id="f5a63-103">Enumeração JsRuntimeAttributes</span><span class="sxs-lookup"><span data-stu-id="f5a63-103">JsRuntimeAttributes Enumeration</span></span>

<span data-ttu-id="f5a63-104">Atributos de um tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f5a63-104">Attributes of a runtime.</span></span>  
  
## <span data-ttu-id="f5a63-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5a63-105">Syntax</span></span>  
  
```cpp  
enum JsRuntimeAttributes;  
```  
  
## <span data-ttu-id="f5a63-106">Parte</span><span class="sxs-lookup"><span data-stu-id="f5a63-106">Members</span></span>  
  
### <span data-ttu-id="f5a63-107">Valores</span><span class="sxs-lookup"><span data-stu-id="f5a63-107">Values</span></span>  
  
|<span data-ttu-id="f5a63-108">Nome</span><span class="sxs-lookup"><span data-stu-id="f5a63-108">Name</span></span>|<span data-ttu-id="f5a63-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5a63-109">Description</span></span>|  
|----------|-----------------|  
|`JsRuntimeAttributeAllowScriptInterrupt`|<span data-ttu-id="f5a63-110">O tempo de execução deve dar suporte à interrupção de script confiável.</span><span class="sxs-lookup"><span data-stu-id="f5a63-110">The runtime should support reliable script interruption.</span></span> <span data-ttu-id="f5a63-111">Isso aumenta o número de locais em que o tempo de execução verifica se há solicitações de interrupção de script ao custo de uma pequena quantidade de desempenho de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f5a63-111">This increases the number of places where the runtime will check for a script interrupt request at the cost of a small amount of runtime performance.</span></span>|  
|`JsRuntimeAttributeDisableBackgroundWork`|<span data-ttu-id="f5a63-112">O tempo de execução não fará qualquer trabalho (como a coleta de lixo) em threads em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="f5a63-112">The runtime will not do any work (such as garbage collection) on background threads.</span></span>|  
|`JsRuntimeAttributeDisableEval`|<span data-ttu-id="f5a63-113">O uso do `eval` `function` Construtor ou gerará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="f5a63-113">Using `eval` or `function` constructor will throw an exception.</span></span>|  
|`JsRuntimeAttributeDisableNativeCodeGeneration`|<span data-ttu-id="f5a63-114">O tempo de execução não irá gerar código nativo.</span><span class="sxs-lookup"><span data-stu-id="f5a63-114">Runtime will not generate native code.</span></span>|  
|`JsRuntimeAttributeEnableExperimentalFeatures`|<span data-ttu-id="f5a63-115">O tempo de execução habilitará todos os recursos experimentais.</span><span class="sxs-lookup"><span data-stu-id="f5a63-115">Runtime will enable all experimental features.</span></span>|  
|`JsRuntimeAttributeEnableIdleProcessing`|<span data-ttu-id="f5a63-116">O host chamará `JsIdle` , portanto, habilitar o processamento de ociosidade.</span><span class="sxs-lookup"><span data-stu-id="f5a63-116">Host will call `JsIdle`, so enable idle processing.</span></span> <span data-ttu-id="f5a63-117">Caso contrário, o tempo de execução gerenciará a memória de forma ligeiramente mais agressiva.</span><span class="sxs-lookup"><span data-stu-id="f5a63-117">Otherwise, the runtime will manage memory slightly more aggressively.</span></span>|  
|`JsRuntimeAttributeDispatchSetExceptionsToDebugger`|<span data-ttu-id="f5a63-118">A chamada `JsSetException` também enviará a exceção para o depurador de script (se houver) dando ao depurador uma chance de interromper a exceção.</span><span class="sxs-lookup"><span data-stu-id="f5a63-118">Calling `JsSetException` will also dispatch the exception to the script debugger (if any) giving the debugger a chance to break on the exception.</span></span>|  
|`JsRuntimeAttributeNone`|<span data-ttu-id="f5a63-119">Nenhum atributo especial.</span><span class="sxs-lookup"><span data-stu-id="f5a63-119">No special attributes.</span></span>|  
  
## <span data-ttu-id="f5a63-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5a63-120">Requirements</span></span>  
 <span data-ttu-id="f5a63-121">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f5a63-121">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f5a63-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f5a63-122">See Also</span></span>  
 [<span data-ttu-id="f5a63-123">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f5a63-123">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)