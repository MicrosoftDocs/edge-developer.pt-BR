---
description: Exclua o valor no índice especificado de um objeto.
title: Função JsDeleteIndexedProperty | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteIndexedProperty
helpviewer_keywords:
- JsDeleteIndexedProperty function
ms.assetid: cc876839-2ecd-41a8-82d0-c19b3de944e3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6148a9c59105749a78ece73578d4b840501c6ecc
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561072"
---
# <span data-ttu-id="9507c-103">Função JsDeleteIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="9507c-103">JsDeleteIndexedProperty Function</span></span>
<span data-ttu-id="9507c-104">Exclua o valor no índice especificado de um objeto.</span><span class="sxs-lookup"><span data-stu-id="9507c-104">Delete the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="9507c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9507c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index  
);  
```  
  
#### <span data-ttu-id="9507c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9507c-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="9507c-107">O objeto no qual operar.</span><span class="sxs-lookup"><span data-stu-id="9507c-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="9507c-108">O índice a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="9507c-108">The index to delete.</span></span>  
  
## <span data-ttu-id="9507c-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9507c-109">Return Value</span></span>  
 <span data-ttu-id="9507c-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="9507c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9507c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9507c-111">Remarks</span></span>  
 <span data-ttu-id="9507c-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="9507c-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9507c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9507c-113">Requirements</span></span>  
 <span data-ttu-id="9507c-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9507c-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9507c-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9507c-115">See Also</span></span>  
 [<span data-ttu-id="9507c-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9507c-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)