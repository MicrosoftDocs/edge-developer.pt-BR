---
description: Cria um valor JavaScript que é uma projeção da passada `VARIANT` .
title: Função JsVariantToValue | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsVariantToValue
helpviewer_keywords:
- JsVariantToValue function
ms.assetid: e8f9eb8b-55b3-4b65-927e-cad5b482edee
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 58c928b519b5a9a678b6cd6ad367e1db2332f021
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231571"
---
# <span data-ttu-id="f6b93-103">Função JsVariantToValue</span><span class="sxs-lookup"><span data-stu-id="f6b93-103">JsVariantToValue Function</span></span>

<span data-ttu-id="f6b93-104">Cria um valor JavaScript que é uma projeção da passada `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="f6b93-104">Creates a JavaScript value that is a projection of the passed in `VARIANT`.</span></span>  
  
## <span data-ttu-id="f6b93-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6b93-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsVariantToValue(  
   _In_ VARIANT *variant,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="f6b93-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6b93-106">Parameters</span></span>  
 `variant`  
 <span data-ttu-id="f6b93-107">A `VARIANT` a a ser projetada.</span><span class="sxs-lookup"><span data-stu-id="f6b93-107">A `VARIANT` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="f6b93-108">Um valor JavaScript que é uma projeção de `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="f6b93-108">A JavaScript value that is a projection of the `VARIANT`.</span></span>  
  
## <span data-ttu-id="f6b93-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f6b93-109">Return Value</span></span>  
 <span data-ttu-id="f6b93-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="f6b93-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f6b93-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6b93-111">Remarks</span></span>  
 <span data-ttu-id="f6b93-112">O valor projetado pode ser usado pelo script para chamar um objeto de automação COM do script.</span><span class="sxs-lookup"><span data-stu-id="f6b93-112">The projected value can be used by script to call a COM automation object from script.</span></span> <span data-ttu-id="f6b93-113">Os hosts são responsáveis por impor regras de Threading COM.</span><span class="sxs-lookup"><span data-stu-id="f6b93-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="f6b93-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="f6b93-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f6b93-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6b93-115">Requirements</span></span>  
 <span data-ttu-id="f6b93-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f6b93-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f6b93-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f6b93-117">See Also</span></span>  
 [<span data-ttu-id="f6b93-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f6b93-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
