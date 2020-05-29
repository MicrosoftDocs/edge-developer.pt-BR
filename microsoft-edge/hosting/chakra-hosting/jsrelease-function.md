---
description: Libera uma referência a um objeto coletado pelo Garbage Collector.
title: Função JsRelease | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRelease
helpviewer_keywords:
- JsRelease function
ms.assetid: 8714fd0b-5b66-48e0-927e-7b93af6cde7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 134ba16509b6c2f0c232214d7efba4d8c8915d43
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562138"
---
# <span data-ttu-id="99c73-103">Função JsRelease</span><span class="sxs-lookup"><span data-stu-id="99c73-103">JsRelease Function</span></span>
<span data-ttu-id="99c73-104">Libera uma referência a um objeto coletado pelo Garbage Collector.</span><span class="sxs-lookup"><span data-stu-id="99c73-104">Releases a reference to a garbage collected object.</span></span>  
  
## <span data-ttu-id="99c73-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99c73-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRelease(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### <span data-ttu-id="99c73-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99c73-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="99c73-107">O objeto ao qual adicionar uma referência.</span><span class="sxs-lookup"><span data-stu-id="99c73-107">The object to add a reference to.</span></span>  
  
 `count`  
 <span data-ttu-id="99c73-108">A nova contagem de referência do objeto (pode passar nulo).</span><span class="sxs-lookup"><span data-stu-id="99c73-108">The object's new reference count (can pass in null).</span></span>  
  
## <span data-ttu-id="99c73-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="99c73-109">Return Value</span></span>  
 <span data-ttu-id="99c73-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="99c73-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="99c73-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="99c73-111">Remarks</span></span>  
 <span data-ttu-id="99c73-112">Remove uma referência a um `JsRef` identificador criado por `JsAddRef` .</span><span class="sxs-lookup"><span data-stu-id="99c73-112">Removes a reference to a `JsRef` handle that was created by `JsAddRef`.</span></span>  
  
## <span data-ttu-id="99c73-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99c73-113">Requirements</span></span>  
 <span data-ttu-id="99c73-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="99c73-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="99c73-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="99c73-115">See Also</span></span>  
 [<span data-ttu-id="99c73-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="99c73-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)