---
description: Determina se um objeto tem uma propriedade.
title: Função JsHasProperty | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasProperty
helpviewer_keywords:
- JsHasProperty function
ms.assetid: 26c94c3d-aae6-4257-8644-df63c7e714fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c6cc195ae02c28500f0a018256d24278ad4b47d8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562159"
---
# <span data-ttu-id="4e89b-103">Função JsHasProperty</span><span class="sxs-lookup"><span data-stu-id="4e89b-103">JsHasProperty Function</span></span>
<span data-ttu-id="4e89b-104">Determina se um objeto tem uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="4e89b-104">Determines whether an object has a property.</span></span>  
  
## <span data-ttu-id="4e89b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e89b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ bool *hasProperty  
);  
```  
  
#### <span data-ttu-id="4e89b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e89b-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="4e89b-107">O objeto que pode conter a propriedade.</span><span class="sxs-lookup"><span data-stu-id="4e89b-107">The object that may contain the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="4e89b-108">A ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="4e89b-108">The ID of the property.</span></span>  
  
 `hasProperty`  
 <span data-ttu-id="4e89b-109">Se o objeto (ou um protótipo) tem a propriedade.</span><span class="sxs-lookup"><span data-stu-id="4e89b-109">Whether the object (or a prototype) has the property.</span></span>  
  
## <span data-ttu-id="4e89b-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4e89b-110">Return Value</span></span>  
 <span data-ttu-id="4e89b-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="4e89b-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4e89b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e89b-112">Remarks</span></span>  
 <span data-ttu-id="4e89b-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="4e89b-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4e89b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e89b-114">Requirements</span></span>  
 <span data-ttu-id="4e89b-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4e89b-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4e89b-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4e89b-116">See Also</span></span>  
 [<span data-ttu-id="4e89b-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4e89b-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)