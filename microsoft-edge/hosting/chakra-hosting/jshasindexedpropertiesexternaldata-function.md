---
description: Determina se um objeto tem suas propriedades indexadas em dados externos.
title: Função JsHasIndexedPropertiesExternalData | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: c676db20-3ef1-4f84-8b26-3e06fe0ab2bf
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7f9f87b19016b3d837b637219eec936a11211e9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562165"
---
# <span data-ttu-id="20bd8-103">Função JsHasIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="20bd8-103">JsHasIndexedPropertiesExternalData Function</span></span>
<span data-ttu-id="20bd8-104">Determina se um objeto tem suas propriedades indexadas em dados externos.</span><span class="sxs-lookup"><span data-stu-id="20bd8-104">Determines whether an object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="20bd8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20bd8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool* value  
);  
```  
  
#### <span data-ttu-id="20bd8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20bd8-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="20bd8-107">O objeto.</span><span class="sxs-lookup"><span data-stu-id="20bd8-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="20bd8-108">Se o objeto tem suas propriedades indexadas em dados externos.</span><span class="sxs-lookup"><span data-stu-id="20bd8-108">Whether the object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="20bd8-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="20bd8-109">Return Value</span></span>  
 <span data-ttu-id="20bd8-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="20bd8-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="20bd8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="20bd8-111">Remarks</span></span>  
 <span data-ttu-id="20bd8-112">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="20bd8-112">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="20bd8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20bd8-113">Requirements</span></span>  
 <span data-ttu-id="20bd8-114">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="20bd8-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="20bd8-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="20bd8-115">See Also</span></span>  
 [<span data-ttu-id="20bd8-116">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="20bd8-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)