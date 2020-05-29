---
description: Coloca a propriedade de um objeto.
title: Função JsSetProperty | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetProperty
helpviewer_keywords:
- JsSetProperty function
ms.assetid: 2c36bebf-ec86-425c-8131-2dd75fd30f40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 2aba03a73f35284f79355a7d93161d9a9518012c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562100"
---
# <span data-ttu-id="a1203-103">Função JsSetProperty</span><span class="sxs-lookup"><span data-stu-id="a1203-103">JsSetProperty Function</span></span>
<span data-ttu-id="a1203-104">Coloca a propriedade de um objeto.</span><span class="sxs-lookup"><span data-stu-id="a1203-104">Puts an object's property.</span></span>  
  
## <span data-ttu-id="a1203-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1203-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef value,  
   _In_ bool useStrictRules  
);  
```  
  
#### <span data-ttu-id="a1203-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1203-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="a1203-107">O objeto que contém a propriedade.</span><span class="sxs-lookup"><span data-stu-id="a1203-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="a1203-108">A ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="a1203-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="a1203-109">O novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="a1203-109">The new value of the property.</span></span>  
  
 `useStrictRules`  
 <span data-ttu-id="a1203-110">O conjunto de propriedades deve seguir as regras do modo estrito.</span><span class="sxs-lookup"><span data-stu-id="a1203-110">The property set should follow strict mode rules.</span></span>  
  
## <span data-ttu-id="a1203-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a1203-111">Return Value</span></span>  
 <span data-ttu-id="a1203-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="a1203-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a1203-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1203-113">Remarks</span></span>  
 <span data-ttu-id="a1203-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="a1203-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a1203-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1203-115">Requirements</span></span>  
 <span data-ttu-id="a1203-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a1203-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a1203-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a1203-117">See Also</span></span>  
 [<span data-ttu-id="a1203-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a1203-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)