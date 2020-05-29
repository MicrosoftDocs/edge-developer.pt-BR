---
description: Obtém a propriedade de um objeto.
title: Função JsGetProperty | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetProperty
helpviewer_keywords:
- JsGetProperty function
ms.assetid: 606bc14f-e849-4f88-a148-6660e923c07b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ea0e5a3bad9363800d2b4a3a18ab932ecc384486
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562180"
---
# <span data-ttu-id="f2e84-103">Função JsGetProperty</span><span class="sxs-lookup"><span data-stu-id="f2e84-103">JsGetProperty Function</span></span>
<span data-ttu-id="f2e84-104">Obtém a propriedade de um objeto.</span><span class="sxs-lookup"><span data-stu-id="f2e84-104">Gets an object's property.</span></span>  
  
## <span data-ttu-id="f2e84-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2e84-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="f2e84-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2e84-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="f2e84-107">O objeto que contém a propriedade.</span><span class="sxs-lookup"><span data-stu-id="f2e84-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="f2e84-108">A ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="f2e84-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="f2e84-109">O valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="f2e84-109">The value of the property.</span></span>  
  
## <span data-ttu-id="f2e84-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f2e84-110">Return Value</span></span>  
 <span data-ttu-id="f2e84-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="f2e84-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f2e84-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2e84-112">Remarks</span></span>  
 <span data-ttu-id="f2e84-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="f2e84-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f2e84-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2e84-114">Requirements</span></span>  
 <span data-ttu-id="f2e84-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f2e84-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f2e84-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f2e84-116">See Also</span></span>  
 [<span data-ttu-id="f2e84-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f2e84-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)