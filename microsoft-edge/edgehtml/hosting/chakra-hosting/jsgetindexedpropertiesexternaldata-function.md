---
description: Recupera as propriedades de dados externos de propriedades indexadas de um objeto.
title: Função JsGetIndexedPropertiesExternalData | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2c313163-3462-42fd-8dee-3dfb3ac7f43f
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 627aaef48def2e042927467e1cbb6d6b7c06a525
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231254"
---
# <span data-ttu-id="a7368-103">Função JsGetIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="a7368-103">JsGetIndexedPropertiesExternalData Function</span></span>

<span data-ttu-id="a7368-104">Recupera as propriedades de dados externos de propriedades indexadas de um objeto.</span><span class="sxs-lookup"><span data-stu-id="a7368-104">Retrieves an object's indexed properties external data information.</span></span>  
  
## <span data-ttu-id="a7368-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7368-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ void** data,  
   _Out_ JsTypedArrayType* arrayType,  
   _Out_ unsigned int* elementLength  
);  
```  
  
#### <span data-ttu-id="a7368-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7368-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="a7368-107">O objeto.</span><span class="sxs-lookup"><span data-stu-id="a7368-107">The object.</span></span>  
  
 `data`  
 <span data-ttu-id="a7368-108">O repositório de retorno de dados externos das propriedades indexadas do objeto.</span><span class="sxs-lookup"><span data-stu-id="a7368-108">The external data back store for the object's indexed properties.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="a7368-109">O tipo de elemento array em dados externos.</span><span class="sxs-lookup"><span data-stu-id="a7368-109">The array element type in external data.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="a7368-110">O número de elementos de matriz em dados externos.</span><span class="sxs-lookup"><span data-stu-id="a7368-110">The number of array elements in external data.</span></span>  
  
## <span data-ttu-id="a7368-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a7368-111">Return Value</span></span>  
 <span data-ttu-id="a7368-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="a7368-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a7368-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7368-113">Remarks</span></span>  
 <span data-ttu-id="a7368-114">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a7368-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="a7368-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7368-115">Requirements</span></span>  
 <span data-ttu-id="a7368-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a7368-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a7368-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a7368-117">See Also</span></span>  
 [<span data-ttu-id="a7368-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a7368-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
