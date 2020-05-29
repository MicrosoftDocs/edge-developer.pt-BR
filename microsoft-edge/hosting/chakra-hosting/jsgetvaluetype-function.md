---
description: Obtém o tipo de JavaScript de um JsValueRef.
title: Função JsGetValueType | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetValueType
helpviewer_keywords:
- JsGetValueType function
ms.assetid: f403cf7c-c8c0-4a17-bfa9-0302d00e760e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 85dc6644e26017c6085ab64d914a86196cca8080
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562164"
---
# <span data-ttu-id="ad35b-103">Função JsGetValueType</span><span class="sxs-lookup"><span data-stu-id="ad35b-103">JsGetValueType Function</span></span>
<span data-ttu-id="ad35b-104">Obtém o tipo de JavaScript de um JsValueRef.</span><span class="sxs-lookup"><span data-stu-id="ad35b-104">Gets the JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="ad35b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad35b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetValueType(  
   _In_ JsValueRef value,  
   _Out_ JsValueType *type  
);  
```  
  
#### <span data-ttu-id="ad35b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad35b-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="ad35b-107">O valor cujo tipo deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="ad35b-107">The value whose type is to be returned.</span></span>  
  
 `type`  
 <span data-ttu-id="ad35b-108">O tipo do valor.</span><span class="sxs-lookup"><span data-stu-id="ad35b-108">The type of the value.</span></span>  
  
## <span data-ttu-id="ad35b-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ad35b-109">Return Value</span></span>  
 <span data-ttu-id="ad35b-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="ad35b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ad35b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad35b-111">Remarks</span></span>  
 <span data-ttu-id="ad35b-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="ad35b-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ad35b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad35b-113">Requirements</span></span>  
 <span data-ttu-id="ad35b-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ad35b-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ad35b-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ad35b-115">See Also</span></span>  
 [<span data-ttu-id="ad35b-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ad35b-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)