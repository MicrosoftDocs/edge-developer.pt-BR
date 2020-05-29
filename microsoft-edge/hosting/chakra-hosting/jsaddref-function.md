---
description: Adiciona uma referência a um objeto de lixo coletado.
title: Função JsAddRef | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsAddRef
helpviewer_keywords:
- JsAddRef function
ms.assetid: a7f3ed49-6a86-489a-abdf-c99428e79cae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bd02dded6dc2877228f22b4d2800e41a78163467
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561136"
---
# <span data-ttu-id="5395d-103">Função JsAddRef</span><span class="sxs-lookup"><span data-stu-id="5395d-103">JsAddRef Function</span></span>
<span data-ttu-id="5395d-104">Adiciona uma referência a um objeto de lixo coletado.</span><span class="sxs-lookup"><span data-stu-id="5395d-104">Adds a reference to a garbage collected object.</span></span>  
  
## <span data-ttu-id="5395d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5395d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsAddRef(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### <span data-ttu-id="5395d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5395d-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="5395d-107">O objeto ao qual adicionar uma referência.</span><span class="sxs-lookup"><span data-stu-id="5395d-107">The object to add a reference to.</span></span>  
  
 `count`  
 <span data-ttu-id="5395d-108">A nova contagem de referência do objeto (pode passar nulo).</span><span class="sxs-lookup"><span data-stu-id="5395d-108">The object's new reference count (can pass in null).</span></span>  
  
## <span data-ttu-id="5395d-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5395d-109">Return Value</span></span>  
 <span data-ttu-id="5395d-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="5395d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5395d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5395d-111">Remarks</span></span>  
 <span data-ttu-id="5395d-112">Isso só precisa ser chamado nas `JsRef` alças que não serão armazenadas em algum lugar na pilha.</span><span class="sxs-lookup"><span data-stu-id="5395d-112">This only needs to be called on `JsRef` handles that are not going to be stored somewhere on the stack.</span></span> <span data-ttu-id="5395d-113">A chamada `JsAddRef` assegura que o objeto ao qual a `JsRef` referência não será liberado até `JsRelease` ser chamado.</span><span class="sxs-lookup"><span data-stu-id="5395d-113">Calling `JsAddRef` ensures that the object the `JsRef` refers to will not be freed until `JsRelease` is called.</span></span>  
  
## <span data-ttu-id="5395d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5395d-114">Requirements</span></span>  
 <span data-ttu-id="5395d-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5395d-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5395d-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5395d-116">See Also</span></span>  
 [<span data-ttu-id="5395d-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5395d-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)