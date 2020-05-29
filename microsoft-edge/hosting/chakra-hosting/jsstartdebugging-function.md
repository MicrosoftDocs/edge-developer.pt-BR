---
description: Inicia a depuração no contexto atual.
title: Função JsStartDebugging | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStartDebugging
helpviewer_keywords:
- JsStartDebugging function
ms.assetid: c48ba02d-6d47-466f-a970-02f087d525f3
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 2c94a6f36ad72bfb9354c85d98ae0b5b4e9c77fb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562005"
---
# <span data-ttu-id="d61fc-103">Função JsStartDebugging</span><span class="sxs-lookup"><span data-stu-id="d61fc-103">JsStartDebugging Function</span></span>
<span data-ttu-id="d61fc-104">Inicia a depuração no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="d61fc-104">Starts debugging in the current context.</span></span>  
  
## <span data-ttu-id="d61fc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d61fc-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsStartDebugging();  
  
// Legacy mode signature  
STDAPI_(JsErrorCode)  JsStartDebugging(  
   _In_ IDebugApplication *debugApplication  
);  
```  
  
#### <span data-ttu-id="d61fc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d61fc-106">Parameters</span></span>  
 `debugApplication`  
 <span data-ttu-id="d61fc-107">O aplicativo de depuração a ser usado para depuração.</span><span class="sxs-lookup"><span data-stu-id="d61fc-107">The debug application to use for debugging.</span></span>  
  
## <span data-ttu-id="d61fc-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d61fc-108">Return Value</span></span>  
 <span data-ttu-id="d61fc-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="d61fc-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d61fc-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d61fc-110">Remarks</span></span>  
 <span data-ttu-id="d61fc-111">O host deve ter certeza de que `CoInitializeEx` é chamado com `COINIT_MULTITHREADED` ou `COINIT_APARTMENTTHREADED` pelo menos uma vez antes de usar essa API</span><span class="sxs-lookup"><span data-stu-id="d61fc-111">The host should make sure that `CoInitializeEx` is called with `COINIT_MULTITHREADED` or `COINIT_APARTMENTTHREADED` at least once before using this API</span></span>  
  
 <span data-ttu-id="d61fc-112">`debugApplication`Não há suporte para o parâmetro no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d61fc-112">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="d61fc-113">Para obter mais informações sobre o uso dessa API no modo Microsoft Edge, consulte [direcionamento de mecanismos do Microsoft Edge versus herdados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="d61fc-113">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="d61fc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d61fc-114">Requirements</span></span>  
 <span data-ttu-id="d61fc-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d61fc-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d61fc-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d61fc-116">See Also</span></span>  
 [<span data-ttu-id="d61fc-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d61fc-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)