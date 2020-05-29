---
description: Torna um objeto não extensível.
title: Função JsPreventExtension | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsPreventExtension
helpviewer_keywords:
- JsPreventExtension function
ms.assetid: 8da07e20-d076-4ae4-9fb0-3f3c141518c2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: baa001b2fd26133ef3a20c88213ac6aaf34a2e0d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562141"
---
# <span data-ttu-id="ca818-103">Função JsPreventExtension</span><span class="sxs-lookup"><span data-stu-id="ca818-103">JsPreventExtension Function</span></span>
<span data-ttu-id="ca818-104">Torna um objeto não extensível.</span><span class="sxs-lookup"><span data-stu-id="ca818-104">Makes an object non-extensible.</span></span>  
  
## <span data-ttu-id="ca818-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca818-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPreventExtension(  
   _In_ JsValueRef object  
);  
```  
  
#### <span data-ttu-id="ca818-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca818-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="ca818-107">O objeto para torná-lo não extensível.</span><span class="sxs-lookup"><span data-stu-id="ca818-107">The object to make non-extensible.</span></span>  
  
## <span data-ttu-id="ca818-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ca818-108">Return Value</span></span>  
 <span data-ttu-id="ca818-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="ca818-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ca818-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca818-110">Remarks</span></span>  
 <span data-ttu-id="ca818-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="ca818-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ca818-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca818-112">Requirements</span></span>  
 <span data-ttu-id="ca818-113">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ca818-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ca818-114">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ca818-114">See Also</span></span>  
 [<span data-ttu-id="ca818-115">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ca818-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)