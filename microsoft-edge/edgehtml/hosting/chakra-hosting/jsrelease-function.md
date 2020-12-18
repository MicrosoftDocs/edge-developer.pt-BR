---
description: Libera uma referência a um objeto coletado pelo Garbage Collector.
title: Função JsRelease | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRelease
helpviewer_keywords:
- JsRelease function
ms.assetid: 8714fd0b-5b66-48e0-927e-7b93af6cde7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 46552a03dc56a10b1d258d8c33da1c533f38464a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231404"
---
# <span data-ttu-id="05270-103">Função JsRelease</span><span class="sxs-lookup"><span data-stu-id="05270-103">JsRelease Function</span></span>

<span data-ttu-id="05270-104">Libera uma referência a um objeto coletado pelo Garbage Collector.</span><span class="sxs-lookup"><span data-stu-id="05270-104">Releases a reference to a garbage collected object.</span></span>  
  
## <span data-ttu-id="05270-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05270-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRelease(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### <span data-ttu-id="05270-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05270-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="05270-107">O objeto ao qual adicionar uma referência.</span><span class="sxs-lookup"><span data-stu-id="05270-107">The object to add a reference to.</span></span>  
  
 `count`  
 <span data-ttu-id="05270-108">A nova contagem de referência do objeto (pode passar nulo).</span><span class="sxs-lookup"><span data-stu-id="05270-108">The object's new reference count (can pass in null).</span></span>  
  
## <span data-ttu-id="05270-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="05270-109">Return Value</span></span>  
 <span data-ttu-id="05270-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="05270-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="05270-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="05270-111">Remarks</span></span>  
 <span data-ttu-id="05270-112">Remove uma referência a um `JsRef` identificador criado por `JsAddRef` .</span><span class="sxs-lookup"><span data-stu-id="05270-112">Removes a reference to a `JsRef` handle that was created by `JsAddRef`.</span></span>  
  
## <span data-ttu-id="05270-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05270-113">Requirements</span></span>  
 <span data-ttu-id="05270-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="05270-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="05270-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="05270-115">See Also</span></span>  
 [<span data-ttu-id="05270-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="05270-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
