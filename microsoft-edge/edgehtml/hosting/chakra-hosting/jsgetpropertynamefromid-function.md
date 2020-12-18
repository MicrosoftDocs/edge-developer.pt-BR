---
description: Obtém o nome associado à ID da propriedade.
title: Função JsGetPropertyNameFromId | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyNameFromId
helpviewer_keywords:
- JsGetPropertyNameFromId function
ms.assetid: b4ca442c-573d-4bc3-adf7-1b8d48480b3a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 42061ab54a70fed571740961a909a6da17fb0733
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231636"
---
# <span data-ttu-id="2ace6-103">Função JsGetPropertyNameFromId</span><span class="sxs-lookup"><span data-stu-id="2ace6-103">JsGetPropertyNameFromId Function</span></span>

<span data-ttu-id="2ace6-104">Obtém o nome associado à ID da propriedade.</span><span class="sxs-lookup"><span data-stu-id="2ace6-104">Gets the name associated with the property ID.</span></span>  
  
## <span data-ttu-id="2ace6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ace6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyNameFromId(  
   _In_ JsPropertyIdRef propertyId,  
   _Outptr_result_z_ const wchar_t **name  
);  
```  
  
#### <span data-ttu-id="2ace6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ace6-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="2ace6-107">A ID da propriedade para obter o nome.</span><span class="sxs-lookup"><span data-stu-id="2ace6-107">The property ID to get the name of.</span></span>  
  
 `name`  
 <span data-ttu-id="2ace6-108">O nome associado à identificação da propriedade.</span><span class="sxs-lookup"><span data-stu-id="2ace6-108">The name associated with the property ID.</span></span>  
  
## <span data-ttu-id="2ace6-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2ace6-109">Return Value</span></span>  
 <span data-ttu-id="2ace6-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="2ace6-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2ace6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ace6-111">Remarks</span></span>  
 <span data-ttu-id="2ace6-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="2ace6-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="2ace6-113">O buffer retornado é válido desde que o tempo de execução esteja ativo e não pode ser usado após a alienação do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="2ace6-113">The returned buffer is valid as long as the runtime is alive and cannot be used once the runtime has been disposed.</span></span>  
  
## <span data-ttu-id="2ace6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ace6-114">Requirements</span></span>  
 <span data-ttu-id="2ace6-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2ace6-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2ace6-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2ace6-116">See Also</span></span>  
 [<span data-ttu-id="2ace6-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2ace6-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
