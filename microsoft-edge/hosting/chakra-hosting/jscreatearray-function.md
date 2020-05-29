---
description: Cria um objeto de matriz JavaScript.
title: Função JsCreateArray | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateArray
helpviewer_keywords:
- JsCreateArray function
ms.assetid: a119949a-e427-4349-9d00-5ec20fb9319c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: fb6a65df1484eb308224a42bb5a65443855c6215
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561111"
---
# <span data-ttu-id="a462c-103">Função JsCreateArray</span><span class="sxs-lookup"><span data-stu-id="a462c-103">JsCreateArray Function</span></span>
<span data-ttu-id="a462c-104">Cria um objeto de matriz JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a462c-104">Creates a Javascript array object.</span></span>  
  
## <span data-ttu-id="a462c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a462c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArray(  
   _In_ unsigned int length,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="a462c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a462c-106">Parameters</span></span>  
 `length`  
 <span data-ttu-id="a462c-107">O comprimento inicial da matriz.</span><span class="sxs-lookup"><span data-stu-id="a462c-107">The initial length of the array.</span></span>  
  
 `result`  
 <span data-ttu-id="a462c-108">O novo objeto de matriz.</span><span class="sxs-lookup"><span data-stu-id="a462c-108">The new array object.</span></span>  
  
## <span data-ttu-id="a462c-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a462c-109">Return Value</span></span>  
 <span data-ttu-id="a462c-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="a462c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a462c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a462c-111">Remarks</span></span>  
 <span data-ttu-id="a462c-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="a462c-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a462c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a462c-113">Requirements</span></span>  
 <span data-ttu-id="a462c-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a462c-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a462c-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a462c-115">See Also</span></span>  
 [<span data-ttu-id="a462c-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a462c-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)