---
description: Define a propriedade do novo objeto de um descritor de propriedades.
title: Função JsDefineProperty | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDefineProperty
helpviewer_keywords:
- JsDefineProperty function
ms.assetid: b2cf48d6-eb40-457c-aa8b-b16a50dc5d6a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b3c9641b4d00540670b44d1718a6aa2aca3b02de
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561075"
---
# <span data-ttu-id="fda17-103">Função JsDefineProperty</span><span class="sxs-lookup"><span data-stu-id="fda17-103">JsDefineProperty Function</span></span>
<span data-ttu-id="fda17-104">Define a propriedade do novo objeto de um descritor de propriedades.</span><span class="sxs-lookup"><span data-stu-id="fda17-104">Defines a new object's own property from a property descriptor.</span></span>  
  
## <span data-ttu-id="fda17-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fda17-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDefineProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef propertyDescriptor,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="fda17-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fda17-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="fda17-107">O objeto que tem a propriedade.</span><span class="sxs-lookup"><span data-stu-id="fda17-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="fda17-108">A ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="fda17-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="fda17-109">O descritor de propriedades.</span><span class="sxs-lookup"><span data-stu-id="fda17-109">The property descriptor.</span></span>  
  
 `result`  
 <span data-ttu-id="fda17-110">Se a propriedade foi definida.</span><span class="sxs-lookup"><span data-stu-id="fda17-110">Whether the property was defined.</span></span>  
  
## <span data-ttu-id="fda17-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fda17-111">Return Value</span></span>  
 <span data-ttu-id="fda17-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="fda17-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fda17-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fda17-113">Remarks</span></span>  
 <span data-ttu-id="fda17-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="fda17-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="fda17-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fda17-115">Requirements</span></span>  
 <span data-ttu-id="fda17-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fda17-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fda17-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fda17-117">See Also</span></span>  
 [<span data-ttu-id="fda17-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fda17-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)