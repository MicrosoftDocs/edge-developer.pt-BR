---
description: Desenvolva um objeto JavaScript para um `IInspectable` ponteiro.
title: Função JsObjectToInspectable | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 1d15b0b8-516f-4fc6-95aa-2ddd65f8ab75
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0d818f798805e2afad4dc87b308258464d31bf92
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231753"
---
# <span data-ttu-id="87761-103">Função JsObjectToInspectable</span><span class="sxs-lookup"><span data-stu-id="87761-103">JsObjectToInspectable Function</span></span>

<span data-ttu-id="87761-104">Desenvolva um objeto JavaScript para um `IInspectable` ponteiro.</span><span class="sxs-lookup"><span data-stu-id="87761-104">Unwraps a JavaScript object to an `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="87761-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87761-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsObjectToInspectable(  
   _In_ JsValueRef value,  
   _Out_ IInspectable  **inspectable  
);  
```  
  
#### <span data-ttu-id="87761-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87761-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="87761-107">Um valor de JavaScript que deve ser projetado `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="87761-107">A JavaScript value that should be projected to `IInspectable`.</span></span>  
  
 `inspectable`  
 <span data-ttu-id="87761-108">Um `IInspectable` valor do objeto.</span><span class="sxs-lookup"><span data-stu-id="87761-108">An `IInspectable` value of the object.</span></span>  
  
## <span data-ttu-id="87761-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="87761-109">Return Value</span></span>  
 <span data-ttu-id="87761-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="87761-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="87761-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="87761-111">Remarks</span></span>  
 <span data-ttu-id="87761-112">Os hosts são responsáveis por impor regras de Threading COM.</span><span class="sxs-lookup"><span data-stu-id="87761-112">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="87761-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="87761-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="87761-114">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="87761-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="87761-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87761-115">Requirements</span></span>  
 <span data-ttu-id="87761-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="87761-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="87761-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="87761-117">See Also</span></span>  
 [<span data-ttu-id="87761-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="87761-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
