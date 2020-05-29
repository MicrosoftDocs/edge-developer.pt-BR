---
description: Testa se um objeto tem um valor no índice especificado.
title: Função JsHasIndexedProperty | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasIndexedProperty
helpviewer_keywords:
- JsHasIndexedProperty function
ms.assetid: 30436a3d-fda0-407e-aba2-142be2310372
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 85d9fa12c44bd1d961ec2a7ba494484873635586
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562160"
---
# <span data-ttu-id="53263-103">Função JsHasIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="53263-103">JsHasIndexedProperty Function</span></span>
<span data-ttu-id="53263-104">Testa se um objeto tem um valor no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="53263-104">Tests whether an object has a value at the specified index.</span></span>  
  
## <span data-ttu-id="53263-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53263-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="53263-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53263-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="53263-107">O objeto no qual operar.</span><span class="sxs-lookup"><span data-stu-id="53263-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="53263-108">O índice a ser testado.</span><span class="sxs-lookup"><span data-stu-id="53263-108">The index to test.</span></span>  
  
 `result`  
 <span data-ttu-id="53263-109">Se o objeto tem um valor no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="53263-109">Whether the object has an value at the specified index.</span></span>  
  
## <span data-ttu-id="53263-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="53263-110">Return Value</span></span>  
 <span data-ttu-id="53263-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="53263-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="53263-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="53263-112">Remarks</span></span>  
 <span data-ttu-id="53263-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="53263-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="53263-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53263-114">Requirements</span></span>  
 <span data-ttu-id="53263-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="53263-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="53263-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="53263-116">See Also</span></span>  
 [<span data-ttu-id="53263-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="53263-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)