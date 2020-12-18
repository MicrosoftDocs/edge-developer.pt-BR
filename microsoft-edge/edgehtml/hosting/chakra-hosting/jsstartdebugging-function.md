---
description: Inicia a depuração no contexto atual.
title: Função JsStartDebugging | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStartDebugging
helpviewer_keywords:
- JsStartDebugging function
ms.assetid: c48ba02d-6d47-466f-a970-02f087d525f3
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9685779911db8e3045986682b66d13e38c70fe8d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231917"
---
# <span data-ttu-id="81542-103">Função JsStartDebugging</span><span class="sxs-lookup"><span data-stu-id="81542-103">JsStartDebugging Function</span></span>

<span data-ttu-id="81542-104">Inicia a depuração no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="81542-104">Starts debugging in the current context.</span></span>  
  
## <span data-ttu-id="81542-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81542-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsStartDebugging();  
  
// Legacy mode signature  
STDAPI_(JsErrorCode)  JsStartDebugging(  
   _In_ IDebugApplication *debugApplication  
);  
```  
  
#### <span data-ttu-id="81542-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81542-106">Parameters</span></span>  
 `debugApplication`  
 <span data-ttu-id="81542-107">O aplicativo de depuração a ser usado para depuração.</span><span class="sxs-lookup"><span data-stu-id="81542-107">The debug application to use for debugging.</span></span>  
  
## <span data-ttu-id="81542-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="81542-108">Return Value</span></span>  
 <span data-ttu-id="81542-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="81542-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="81542-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="81542-110">Remarks</span></span>  
 <span data-ttu-id="81542-111">O host deve ter certeza de que `CoInitializeEx` é chamado com `COINIT_MULTITHREADED` ou `COINIT_APARTMENTTHREADED` pelo menos uma vez antes de usar essa API</span><span class="sxs-lookup"><span data-stu-id="81542-111">The host should make sure that `CoInitializeEx` is called with `COINIT_MULTITHREADED` or `COINIT_APARTMENTTHREADED` at least once before using this API</span></span>  
  
 <span data-ttu-id="81542-112">`debugApplication`Não há suporte para o parâmetro no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="81542-112">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="81542-113">Para obter mais informações sobre o uso dessa API no modo Microsoft Edge, consulte [direcionamento de mecanismos do Microsoft Edge versus herdados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="81542-113">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="81542-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81542-114">Requirements</span></span>  
 <span data-ttu-id="81542-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="81542-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="81542-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="81542-116">See Also</span></span>  
 [<span data-ttu-id="81542-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="81542-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
