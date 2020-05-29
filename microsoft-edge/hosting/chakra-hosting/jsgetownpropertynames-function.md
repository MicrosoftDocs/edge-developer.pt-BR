---
description: Obtém a lista de todas as propriedades do objeto.
title: Função JsGetOwnPropertyNames | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyNames
helpviewer_keywords:
- JsGetOwnPropertyNames function
ms.assetid: 0c17ea06-b17f-4ea3-ad04-1259a4d1b6de
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5355caab864724d72fdb2c7abb3dc70e39662b55
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562182"
---
# <span data-ttu-id="80200-103">Função JsGetOwnPropertyNames</span><span class="sxs-lookup"><span data-stu-id="80200-103">JsGetOwnPropertyNames Function</span></span>
<span data-ttu-id="80200-104">Obtém a lista de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="80200-104">Gets the list of all properties on the object.</span></span>  
  
## <span data-ttu-id="80200-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80200-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyNames(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertyNames  
);  
```  
  
#### <span data-ttu-id="80200-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80200-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="80200-107">O objeto do qual obter os nomes das propriedades.</span><span class="sxs-lookup"><span data-stu-id="80200-107">The object from which to get the property names.</span></span>  
  
 `propertyNames`  
 <span data-ttu-id="80200-108">Uma matriz de nomes de propriedades.</span><span class="sxs-lookup"><span data-stu-id="80200-108">An array of property names.</span></span>  
  
## <span data-ttu-id="80200-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="80200-109">Return Value</span></span>  
 <span data-ttu-id="80200-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="80200-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="80200-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="80200-111">Remarks</span></span>  
 <span data-ttu-id="80200-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="80200-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="80200-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80200-113">Requirements</span></span>  
 <span data-ttu-id="80200-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="80200-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="80200-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="80200-115">See Also</span></span>  
 [<span data-ttu-id="80200-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="80200-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)