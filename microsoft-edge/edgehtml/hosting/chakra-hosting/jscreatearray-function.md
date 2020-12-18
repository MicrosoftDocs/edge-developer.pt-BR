---
description: Cria um objeto de matriz JavaScript.
title: Função JsCreateArray | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateArray
helpviewer_keywords:
- JsCreateArray function
ms.assetid: a119949a-e427-4349-9d00-5ec20fb9319c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 34ce07055fa3d4d24188d7edbcedc3f08973e233
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231425"
---
# <span data-ttu-id="d099e-103">Função JsCreateArray</span><span class="sxs-lookup"><span data-stu-id="d099e-103">JsCreateArray Function</span></span>

<span data-ttu-id="d099e-104">Cria um objeto de matriz JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d099e-104">Creates a Javascript array object.</span></span>  
  
## <span data-ttu-id="d099e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d099e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArray(  
   _In_ unsigned int length,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="d099e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d099e-106">Parameters</span></span>  
 `length`  
 <span data-ttu-id="d099e-107">O comprimento inicial da matriz.</span><span class="sxs-lookup"><span data-stu-id="d099e-107">The initial length of the array.</span></span>  
  
 `result`  
 <span data-ttu-id="d099e-108">O novo objeto de matriz.</span><span class="sxs-lookup"><span data-stu-id="d099e-108">The new array object.</span></span>  
  
## <span data-ttu-id="d099e-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d099e-109">Return Value</span></span>  
 <span data-ttu-id="d099e-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="d099e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d099e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d099e-111">Remarks</span></span>  
 <span data-ttu-id="d099e-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="d099e-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d099e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d099e-113">Requirements</span></span>  
 <span data-ttu-id="d099e-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d099e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d099e-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d099e-115">See Also</span></span>  
 [<span data-ttu-id="d099e-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d099e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
