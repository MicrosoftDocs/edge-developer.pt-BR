---
description: Recuperar o valor no índice especificado de um objeto.
title: Função JsGetIndexedProperty | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetIndexedProperty
helpviewer_keywords:
- JsGetIndexedProperty function
ms.assetid: f61ea388-0ae6-4a19-b3b5-75ed49a3f32d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 7bb048b841462e27604ab169c69e4c051209a67d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562185"
---
# <span data-ttu-id="9f329-103">Função JsGetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="9f329-103">JsGetIndexedProperty Function</span></span>
<span data-ttu-id="9f329-104">Recuperar o valor no índice especificado de um objeto.</span><span class="sxs-lookup"><span data-stu-id="9f329-104">Retrieve the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="9f329-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f329-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="9f329-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f329-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="9f329-107">O objeto no qual operar.</span><span class="sxs-lookup"><span data-stu-id="9f329-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="9f329-108">O índice a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="9f329-108">The index to retrieve.</span></span>  
  
 `result`  
 <span data-ttu-id="9f329-109">O valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="9f329-109">The retrieved value.</span></span>  
  
## <span data-ttu-id="9f329-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9f329-110">Return Value</span></span>  
 <span data-ttu-id="9f329-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="9f329-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9f329-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f329-112">Remarks</span></span>  
 <span data-ttu-id="9f329-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="9f329-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9f329-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f329-114">Requirements</span></span>  
 <span data-ttu-id="9f329-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9f329-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9f329-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9f329-116">See Also</span></span>  
 [<span data-ttu-id="9f329-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9f329-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)