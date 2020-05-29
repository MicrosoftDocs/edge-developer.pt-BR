---
description: Cria um valor JavaScript que é uma projeção da passada `VARIANT` .
title: Função JsVariantToValue | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsVariantToValue
helpviewer_keywords:
- JsVariantToValue function
ms.assetid: e8f9eb8b-55b3-4b65-927e-cad5b482edee
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 01796bc38548cf56b500731d899541ef214ec4e3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560990"
---
# <span data-ttu-id="7c327-103">Função JsVariantToValue</span><span class="sxs-lookup"><span data-stu-id="7c327-103">JsVariantToValue Function</span></span>
<span data-ttu-id="7c327-104">Cria um valor JavaScript que é uma projeção da passada `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="7c327-104">Creates a JavaScript value that is a projection of the passed in `VARIANT`.</span></span>  
  
## <span data-ttu-id="7c327-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c327-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsVariantToValue(  
   _In_ VARIANT *variant,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="7c327-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c327-106">Parameters</span></span>  
 `variant`  
 <span data-ttu-id="7c327-107">A `VARIANT` a a ser projetada.</span><span class="sxs-lookup"><span data-stu-id="7c327-107">A `VARIANT` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="7c327-108">Um valor JavaScript que é uma projeção de `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="7c327-108">A JavaScript value that is a projection of the `VARIANT`.</span></span>  
  
## <span data-ttu-id="7c327-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7c327-109">Return Value</span></span>  
 <span data-ttu-id="7c327-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="7c327-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7c327-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c327-111">Remarks</span></span>  
 <span data-ttu-id="7c327-112">O valor projetado pode ser usado pelo script para chamar um objeto de automação COM do script.</span><span class="sxs-lookup"><span data-stu-id="7c327-112">The projected value can be used by script to call a COM automation object from script.</span></span> <span data-ttu-id="7c327-113">Os hosts são responsáveis por impor regras de Threading COM.</span><span class="sxs-lookup"><span data-stu-id="7c327-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="7c327-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="7c327-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="7c327-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c327-115">Requirements</span></span>  
 <span data-ttu-id="7c327-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7c327-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7c327-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7c327-117">See Also</span></span>  
 [<span data-ttu-id="7c327-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7c327-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)