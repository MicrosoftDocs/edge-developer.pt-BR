---
description: Obtém a lista de todas as propriedades do objeto.
title: Função JsGetOwnPropertyNames | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyNames
helpviewer_keywords:
- JsGetOwnPropertyNames function
ms.assetid: 0c17ea06-b17f-4ea3-ad04-1259a4d1b6de
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4d00788b6ef581b923413e5c71a63bb27398a326
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231229"
---
# <span data-ttu-id="3e06f-103">Função JsGetOwnPropertyNames</span><span class="sxs-lookup"><span data-stu-id="3e06f-103">JsGetOwnPropertyNames Function</span></span>

<span data-ttu-id="3e06f-104">Obtém a lista de todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="3e06f-104">Gets the list of all properties on the object.</span></span>  
  
## <span data-ttu-id="3e06f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e06f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyNames(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertyNames  
);  
```  
  
#### <span data-ttu-id="3e06f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e06f-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="3e06f-107">O objeto do qual obter os nomes das propriedades.</span><span class="sxs-lookup"><span data-stu-id="3e06f-107">The object from which to get the property names.</span></span>  
  
 `propertyNames`  
 <span data-ttu-id="3e06f-108">Uma matriz de nomes de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3e06f-108">An array of property names.</span></span>  
  
## <span data-ttu-id="3e06f-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3e06f-109">Return Value</span></span>  
 <span data-ttu-id="3e06f-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="3e06f-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3e06f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e06f-111">Remarks</span></span>  
 <span data-ttu-id="3e06f-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="3e06f-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="3e06f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e06f-113">Requirements</span></span>  
 <span data-ttu-id="3e06f-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3e06f-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3e06f-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3e06f-115">See Also</span></span>  
 [<span data-ttu-id="3e06f-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3e06f-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
