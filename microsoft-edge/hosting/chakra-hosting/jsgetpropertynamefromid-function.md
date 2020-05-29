---
description: Obtém o nome associado à ID da propriedade.
title: Função JsGetPropertyNameFromId | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyNameFromId
helpviewer_keywords:
- JsGetPropertyNameFromId function
ms.assetid: b4ca442c-573d-4bc3-adf7-1b8d48480b3a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e76c69c1d746302bb95cd7229872845c4fbcc88
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561049"
---
# <span data-ttu-id="2d008-103">Função JsGetPropertyNameFromId</span><span class="sxs-lookup"><span data-stu-id="2d008-103">JsGetPropertyNameFromId Function</span></span>
<span data-ttu-id="2d008-104">Obtém o nome associado à ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="2d008-104">Gets the name associated with the property ID.</span></span>  
  
## <span data-ttu-id="2d008-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d008-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyNameFromId(  
   _In_ JsPropertyIdRef propertyId,  
   _Outptr_result_z_ const wchar_t **name  
);  
```  
  
#### <span data-ttu-id="2d008-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d008-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="2d008-107">A ID da propriedade para obter o nome.</span><span class="sxs-lookup"><span data-stu-id="2d008-107">The property ID to get the name of.</span></span>  
  
 `name`  
 <span data-ttu-id="2d008-108">O nome associado à identificação da propriedade.</span><span class="sxs-lookup"><span data-stu-id="2d008-108">The name associated with the property ID.</span></span>  
  
## <span data-ttu-id="2d008-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2d008-109">Return Value</span></span>  
 <span data-ttu-id="2d008-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="2d008-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2d008-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d008-111">Remarks</span></span>  
 <span data-ttu-id="2d008-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="2d008-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="2d008-113">O buffer retornado é válido desde que o tempo de execução esteja ativo e não pode ser usado após a alienação do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="2d008-113">The returned buffer is valid as long as the runtime is alive and cannot be used once the runtime has been disposed.</span></span>  
  
## <span data-ttu-id="2d008-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d008-114">Requirements</span></span>  
 <span data-ttu-id="2d008-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2d008-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2d008-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2d008-116">See Also</span></span>  
 [<span data-ttu-id="2d008-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2d008-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)