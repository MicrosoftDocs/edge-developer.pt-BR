---
description: Obtém a ID da propriedade associada ao nome.
title: Função JsGetPropertyIdFromName | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyIdFromName
helpviewer_keywords:
- JsGetPropertyIdFromName function
ms.assetid: 1674906f-746a-4c62-99cd-023276683a86
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e1954b86937056523a30c15dbf350ac02fd63dde
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562178"
---
# <span data-ttu-id="8f139-103">Função JsGetPropertyIdFromName</span><span class="sxs-lookup"><span data-stu-id="8f139-103">JsGetPropertyIdFromName Function</span></span>
<span data-ttu-id="8f139-104">Obtém a ID da propriedade associada ao nome.</span><span class="sxs-lookup"><span data-stu-id="8f139-104">Gets the property ID associated with the name.</span></span>  
  
## <span data-ttu-id="8f139-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f139-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromName(  
   _In_z_ const wchar_t *name,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="8f139-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f139-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="8f139-107">O nome da identificação da propriedade a ser obtida ou criada.</span><span class="sxs-lookup"><span data-stu-id="8f139-107">The name of the property ID to get or create.</span></span> <span data-ttu-id="8f139-108">O nome pode consistir somente em dígitos.</span><span class="sxs-lookup"><span data-stu-id="8f139-108">The name may consist of only digits.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="8f139-109">A ID da propriedade nesse tempo de execução para o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="8f139-109">The property ID in this runtime for the given name.</span></span>  
  
## <span data-ttu-id="8f139-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8f139-110">Return Value</span></span>  
 <span data-ttu-id="8f139-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="8f139-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8f139-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f139-112">Remarks</span></span>  
 <span data-ttu-id="8f139-113">As IDs de propriedade são específicas de um contexto e não podem ser usadas em contextos.</span><span class="sxs-lookup"><span data-stu-id="8f139-113">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="8f139-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="8f139-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="8f139-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f139-115">Requirements</span></span>  
 <span data-ttu-id="8f139-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8f139-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8f139-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8f139-117">See Also</span></span>  
 [<span data-ttu-id="8f139-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8f139-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)