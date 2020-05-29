---
description: Cria um valor JavaScript que é uma projeção do ponteiro passado `IInspectable` .
title: Função JsInspectableToObject | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 26ce17eb3abcefcf9a1f0cc773e9fe4c3aaf05cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561032"
---
# <span data-ttu-id="8247e-103">Função JsInspectableToObject</span><span class="sxs-lookup"><span data-stu-id="8247e-103">JsInspectableToObject Function</span></span>
<span data-ttu-id="8247e-104">Cria um valor JavaScript que é uma projeção do ponteiro passado `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="8247e-104">Creates a JavaScript value that is a projection of the passed in `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="8247e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8247e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsInspectableToObject(  
        _In_ IInspectable  *inspectable,  
        _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="8247e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8247e-106">Parameters</span></span>  
 `inspectable`  
 <span data-ttu-id="8247e-107">A `IInspectable` a a ser projetada.</span><span class="sxs-lookup"><span data-stu-id="8247e-107">A `IInspectable` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="8247e-108">Um valor JavaScript que é uma projeção de `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="8247e-108">A JavaScript value that is a projection of the `IInspectable`.</span></span>  
  
## <span data-ttu-id="8247e-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8247e-109">Return Value</span></span>  
 <span data-ttu-id="8247e-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="8247e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8247e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8247e-111">Remarks</span></span>  
 <span data-ttu-id="8247e-112">O valor projetado pode ser usado pelo script para chamar um objeto WinRT.</span><span class="sxs-lookup"><span data-stu-id="8247e-112">The projected value can be used by script to call a WinRT object.</span></span> <span data-ttu-id="8247e-113">Os hosts são responsáveis por impor regras de Threading COM.</span><span class="sxs-lookup"><span data-stu-id="8247e-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="8247e-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="8247e-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="8247e-115">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="8247e-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="8247e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8247e-116">Requirements</span></span>  
 <span data-ttu-id="8247e-117">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8247e-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8247e-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8247e-118">See Also</span></span>  
 [<span data-ttu-id="8247e-119">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8247e-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)