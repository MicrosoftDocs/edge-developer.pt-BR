---
description: Obtém um descritor de propriedades para a propriedade do próprio objeto.
title: Função JsGetOwnPropertyDescriptor | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyDescriptor
helpviewer_keywords:
- JsGetOwnPropertyDescriptor function
ms.assetid: 44c417ce-ab63-44eb-a0ab-19838e3ab34f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6f500aec8b892cb2ad437bd7159ab14165a8bfb4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562189"
---
# <span data-ttu-id="bc1b5-103">Função JsGetOwnPropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="bc1b5-103">JsGetOwnPropertyDescriptor Function</span></span>
<span data-ttu-id="bc1b5-104">Obtém um descritor de propriedades para a propriedade do próprio objeto.</span><span class="sxs-lookup"><span data-stu-id="bc1b5-104">Gets a property descriptor for an object's own property.</span></span>  
  
## <span data-ttu-id="bc1b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc1b5-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyDescriptor(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *propertyDescriptor  
);  
```  
  
#### <span data-ttu-id="bc1b5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc1b5-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="bc1b5-107">O objeto que tem a propriedade.</span><span class="sxs-lookup"><span data-stu-id="bc1b5-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="bc1b5-108">A ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="bc1b5-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="bc1b5-109">O descritor de propriedades.</span><span class="sxs-lookup"><span data-stu-id="bc1b5-109">The property descriptor.</span></span>  
  
## <span data-ttu-id="bc1b5-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bc1b5-110">Return Value</span></span>  
 <span data-ttu-id="bc1b5-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="bc1b5-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bc1b5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc1b5-112">Remarks</span></span>  
 <span data-ttu-id="bc1b5-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="bc1b5-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bc1b5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc1b5-114">Requirements</span></span>  
 <span data-ttu-id="bc1b5-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bc1b5-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bc1b5-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bc1b5-116">See Also</span></span>  
 [<span data-ttu-id="bc1b5-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bc1b5-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)