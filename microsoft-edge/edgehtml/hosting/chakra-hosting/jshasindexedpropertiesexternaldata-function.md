---
description: Determina se um objeto tem suas propriedades indexadas em dados externos.
title: Função JsHasIndexedPropertiesExternalData | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c676db20-3ef1-4f84-8b26-3e06fe0ab2bf
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e6395bacb15904bc3f2e74d22959844e8e0af373
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231922"
---
# <span data-ttu-id="feabf-103">Função JsHasIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="feabf-103">JsHasIndexedPropertiesExternalData Function</span></span>

<span data-ttu-id="feabf-104">Determina se um objeto tem suas propriedades indexadas em dados externos.</span><span class="sxs-lookup"><span data-stu-id="feabf-104">Determines whether an object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="feabf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="feabf-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool* value  
);  
```  
  
#### <span data-ttu-id="feabf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="feabf-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="feabf-107">O objeto.</span><span class="sxs-lookup"><span data-stu-id="feabf-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="feabf-108">Se o objeto tem suas propriedades indexadas em dados externos.</span><span class="sxs-lookup"><span data-stu-id="feabf-108">Whether the object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="feabf-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="feabf-109">Return Value</span></span>  
 <span data-ttu-id="feabf-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="feabf-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="feabf-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="feabf-111">Remarks</span></span>  
 <span data-ttu-id="feabf-112">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="feabf-112">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="feabf-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="feabf-113">Requirements</span></span>  
 <span data-ttu-id="feabf-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="feabf-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="feabf-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="feabf-115">See Also</span></span>  
 [<span data-ttu-id="feabf-116">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="feabf-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
