---
description: Obtém a ID da propriedade associada ao nome.
title: Função JsGetPropertyIdFromName | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyIdFromName
helpviewer_keywords:
- JsGetPropertyIdFromName function
ms.assetid: 1674906f-746a-4c62-99cd-023276683a86
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: adc8de4d55fa0c74ad191b4621ceb3a54026d02d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231774"
---
# <span data-ttu-id="4e5d0-103">Função JsGetPropertyIdFromName</span><span class="sxs-lookup"><span data-stu-id="4e5d0-103">JsGetPropertyIdFromName Function</span></span>

<span data-ttu-id="4e5d0-104">Obtém a ID da propriedade associada ao nome.</span><span class="sxs-lookup"><span data-stu-id="4e5d0-104">Gets the property ID associated with the name.</span></span>  
  
## <span data-ttu-id="4e5d0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e5d0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromName(  
   _In_z_ const wchar_t *name,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="4e5d0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e5d0-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="4e5d0-107">O nome da identificação da propriedade a ser obtida ou criada.</span><span class="sxs-lookup"><span data-stu-id="4e5d0-107">The name of the property ID to get or create.</span></span> <span data-ttu-id="4e5d0-108">O nome pode consistir somente em dígitos.</span><span class="sxs-lookup"><span data-stu-id="4e5d0-108">The name may consist of only digits.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="4e5d0-109">A ID da propriedade nesse tempo de execução para o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="4e5d0-109">The property ID in this runtime for the given name.</span></span>  
  
## <span data-ttu-id="4e5d0-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4e5d0-110">Return Value</span></span>  
 <span data-ttu-id="4e5d0-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="4e5d0-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4e5d0-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e5d0-112">Remarks</span></span>  
 <span data-ttu-id="4e5d0-113">As IDs de propriedade são específicas de um contexto e não podem ser usadas em contextos.</span><span class="sxs-lookup"><span data-stu-id="4e5d0-113">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="4e5d0-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="4e5d0-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4e5d0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e5d0-115">Requirements</span></span>  
 <span data-ttu-id="4e5d0-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4e5d0-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4e5d0-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4e5d0-117">See Also</span></span>  
 [<span data-ttu-id="4e5d0-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4e5d0-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
