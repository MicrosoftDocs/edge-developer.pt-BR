---
description: Desenvolva um objeto JavaScript para um `IInspectable` ponteiro.
title: Função JsObjectToInspectable | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 1d15b0b8-516f-4fc6-95aa-2ddd65f8ab75
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7127e1cf1372020e0df00b81ed172739379426f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562154"
---
# <span data-ttu-id="07c53-103">Função JsObjectToInspectable</span><span class="sxs-lookup"><span data-stu-id="07c53-103">JsObjectToInspectable Function</span></span>
<span data-ttu-id="07c53-104">Desenvolva um objeto JavaScript para um `IInspectable` ponteiro.</span><span class="sxs-lookup"><span data-stu-id="07c53-104">Unwraps a JavaScript object to an `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="07c53-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07c53-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsObjectToInspectable(  
   _In_ JsValueRef value,  
   _Out_ IInspectable  **inspectable  
);  
```  
  
#### <span data-ttu-id="07c53-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07c53-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="07c53-107">Um valor de JavaScript que deve ser projetado `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="07c53-107">A JavaScript value that should be projected to `IInspectable`.</span></span>  
  
 `inspectable`  
 <span data-ttu-id="07c53-108">Um `IInspectable` valor do objeto.</span><span class="sxs-lookup"><span data-stu-id="07c53-108">An `IInspectable` value of the object.</span></span>  
  
## <span data-ttu-id="07c53-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="07c53-109">Return Value</span></span>  
 <span data-ttu-id="07c53-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="07c53-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="07c53-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="07c53-111">Remarks</span></span>  
 <span data-ttu-id="07c53-112">Os hosts são responsáveis por impor regras de Threading COM.</span><span class="sxs-lookup"><span data-stu-id="07c53-112">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="07c53-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="07c53-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="07c53-114">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="07c53-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="07c53-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07c53-115">Requirements</span></span>  
 <span data-ttu-id="07c53-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="07c53-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="07c53-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="07c53-117">See Also</span></span>  
 [<span data-ttu-id="07c53-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="07c53-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)