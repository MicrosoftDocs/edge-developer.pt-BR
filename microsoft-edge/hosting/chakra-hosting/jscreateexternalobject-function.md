---
description: Cria um novo objeto que armazena alguns dados externos.
title: Função JsCreateExternalObject | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateExternalObject
helpviewer_keywords:
- JsCreateExternalObject function
ms.assetid: 6bcef506-93fb-429b-b06a-a971ff0b71f3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9a68f4befea7dc7c3369bcade475e29d53342730
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561098"
---
# <span data-ttu-id="bf29c-103">Função JsCreateExternalObject</span><span class="sxs-lookup"><span data-stu-id="bf29c-103">JsCreateExternalObject Function</span></span>
<span data-ttu-id="bf29c-104">Cria um novo objeto que armazena alguns dados externos.</span><span class="sxs-lookup"><span data-stu-id="bf29c-104">Creates a new object that stores some external data.</span></span>
  
## <span data-ttu-id="bf29c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf29c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalObject(  
   _In_opt_ void *data,  
   _In_opt_ JsFinalizeCallback finalizeCallback,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="bf29c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf29c-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="bf29c-107">Dados externos a serem representados pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="bf29c-107">External data that the object will represent.</span></span> <span data-ttu-id="bf29c-108">Pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="bf29c-108">May be null.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="bf29c-109">Um retorno de chamada para quando o objeto for finalizado.</span><span class="sxs-lookup"><span data-stu-id="bf29c-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="bf29c-110">Pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="bf29c-110">May be null.</span></span>  
  
 `object`  
 <span data-ttu-id="bf29c-111">O novo objeto.</span><span class="sxs-lookup"><span data-stu-id="bf29c-111">The new object.</span></span>  
  
## <span data-ttu-id="bf29c-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bf29c-112">Return Value</span></span>  
 <span data-ttu-id="bf29c-113">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="bf29c-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bf29c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf29c-114">Remarks</span></span>  
 <span data-ttu-id="bf29c-115">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="bf29c-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bf29c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf29c-116">Requirements</span></span>  
 <span data-ttu-id="bf29c-117">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bf29c-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bf29c-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bf29c-118">See Also</span></span>  
 [<span data-ttu-id="bf29c-119">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bf29c-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)