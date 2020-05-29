---
description: Converte o valor em Object usando a semântica JavaScript padrão.
title: Função JsConvertValueToObject | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToObject
helpviewer_keywords:
- JsConvertValueToObject function
ms.assetid: 6528b28a-1d2b-417f-bf78-bf05547c52e1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6a8b1a8933cdcaaf250a2e28ed8fc758ea66cc0e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561115"
---
# <span data-ttu-id="85572-103">Função JsConvertValueToObject</span><span class="sxs-lookup"><span data-stu-id="85572-103">JsConvertValueToObject Function</span></span>
<span data-ttu-id="85572-104">Converte o valor em Object usando a semântica JavaScript padrão.</span><span class="sxs-lookup"><span data-stu-id="85572-104">Converts the value to object using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="85572-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85572-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToObject(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="85572-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85572-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="85572-107">O valor a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="85572-107">The value to be converted.</span></span>  
  
 `object`  
 <span data-ttu-id="85572-108">O valor convertido.</span><span class="sxs-lookup"><span data-stu-id="85572-108">The converted value.</span></span>  
  
## <span data-ttu-id="85572-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="85572-109">Return Value</span></span>  
 <span data-ttu-id="85572-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="85572-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="85572-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="85572-111">Remarks</span></span>  
 <span data-ttu-id="85572-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="85572-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="85572-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85572-113">Requirements</span></span>  
 <span data-ttu-id="85572-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="85572-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="85572-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="85572-115">See Also</span></span>  
 [<span data-ttu-id="85572-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="85572-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)