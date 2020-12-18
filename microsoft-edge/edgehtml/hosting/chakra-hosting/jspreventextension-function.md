---
description: Torna um objeto não extensível.
title: Função JsPreventExtension | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsPreventExtension
helpviewer_keywords:
- JsPreventExtension function
ms.assetid: 8da07e20-d076-4ae4-9fb0-3f3c141518c2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1904756a932bd581e05ec474004af7107da3f64b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231752"
---
# <span data-ttu-id="470ff-103">Função JsPreventExtension</span><span class="sxs-lookup"><span data-stu-id="470ff-103">JsPreventExtension Function</span></span>

<span data-ttu-id="470ff-104">Torna um objeto não extensível.</span><span class="sxs-lookup"><span data-stu-id="470ff-104">Makes an object non-extensible.</span></span>  
  
## <span data-ttu-id="470ff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="470ff-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPreventExtension(  
   _In_ JsValueRef object  
);  
```  
  
#### <span data-ttu-id="470ff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="470ff-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="470ff-107">O objeto para torná-lo não extensível.</span><span class="sxs-lookup"><span data-stu-id="470ff-107">The object to make non-extensible.</span></span>  
  
## <span data-ttu-id="470ff-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="470ff-108">Return Value</span></span>  
 <span data-ttu-id="470ff-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="470ff-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="470ff-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="470ff-110">Remarks</span></span>  
 <span data-ttu-id="470ff-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="470ff-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="470ff-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="470ff-112">Requirements</span></span>  
 <span data-ttu-id="470ff-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="470ff-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="470ff-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="470ff-114">See Also</span></span>  
 [<span data-ttu-id="470ff-115">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="470ff-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
