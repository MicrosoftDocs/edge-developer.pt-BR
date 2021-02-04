---
description: Define as propriedades indexadas de um objeto para dados externos. Os dados externos serão usados como loja de volta para as propriedades indexadas do objeto e acessados como uma matriz digitada.
title: Função JsSetIndexedPropertiesToExternalData | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: cee2d86d-ed42-4acb-86ef-95a67e63d0d6
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fa0eba3659c20066913cd42a0a18dd5ffe5f857f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231408"
---
# <span data-ttu-id="f0c7c-104">Função JsSetIndexedPropertiesToExternalData</span><span class="sxs-lookup"><span data-stu-id="f0c7c-104">JsSetIndexedPropertiesToExternalData Function</span></span>

<span data-ttu-id="f0c7c-105">Define as propriedades indexadas de um objeto para dados externos.</span><span class="sxs-lookup"><span data-stu-id="f0c7c-105">Sets an object's indexed properties to external data.</span></span> <span data-ttu-id="f0c7c-106">Os dados externos serão usados como loja de volta para as propriedades indexadas do objeto e acessados como uma matriz digitada.</span><span class="sxs-lookup"><span data-stu-id="f0c7c-106">The external data will be used as back store for the object's indexed properties and accessed like a typed array.</span></span>  
  
## <span data-ttu-id="f0c7c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0c7c-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedPropertiesToExternalData(  
   _In_ JsValueRef object,  
   _In_ void* data,  
   _In_ JsTypedArrayType arrayType,  
   _In_ unsigned int elementLength  
);  
```  
  
#### <span data-ttu-id="f0c7c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0c7c-108">Parameters</span></span>  
 `object`  
 <span data-ttu-id="f0c7c-109">O objeto no qual operar.</span><span class="sxs-lookup"><span data-stu-id="f0c7c-109">The object to operate on.</span></span>  
  
 `data`  
 <span data-ttu-id="f0c7c-110">Os dados externos a serem usados como loja de volta para as propriedades indexadas do objeto.</span><span class="sxs-lookup"><span data-stu-id="f0c7c-110">The external data to be used as back store for the object's indexed properties.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="f0c7c-111">O tipo de elemento array em dados externos.</span><span class="sxs-lookup"><span data-stu-id="f0c7c-111">The array element type in external data.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="f0c7c-112">O número de elementos de matriz em dados externos.</span><span class="sxs-lookup"><span data-stu-id="f0c7c-112">The number of array elements in external data.</span></span>  
  
## <span data-ttu-id="f0c7c-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f0c7c-113">Return Value</span></span>  
 <span data-ttu-id="f0c7c-114">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="f0c7c-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f0c7c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0c7c-115">Remarks</span></span>  
 <span data-ttu-id="f0c7c-116">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="f0c7c-116">Requires an active script context.</span></span>  
  
 <span data-ttu-id="f0c7c-117">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="f0c7c-117">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="f0c7c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0c7c-118">Requirements</span></span>  
 <span data-ttu-id="f0c7c-119">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f0c7c-119">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f0c7c-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f0c7c-120">See Also</span></span>  
 [<span data-ttu-id="f0c7c-121">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f0c7c-121">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)