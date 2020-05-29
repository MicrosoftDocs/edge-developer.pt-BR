---
description: Obtém a lista de todas as propriedades de símbolo no objeto.
title: Função JsGetOwnPropertySymbols | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 57c431e3-de0b-4ed0-b750-87a86448daff
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7a7f4e88986a45fbccfae0c53e92ff2e5313991
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562183"
---
# <span data-ttu-id="49c9c-103">Função JsGetOwnPropertySymbols</span><span class="sxs-lookup"><span data-stu-id="49c9c-103">JsGetOwnPropertySymbols Function</span></span>
<span data-ttu-id="49c9c-104">Obtém a lista de todas as propriedades de símbolo no objeto.</span><span class="sxs-lookup"><span data-stu-id="49c9c-104">Gets the list of all symbol properties on the object.</span></span>  
  
## <span data-ttu-id="49c9c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49c9c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertySymbols(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertySymbols  
);  
```  
  
#### <span data-ttu-id="49c9c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49c9c-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="49c9c-107">O objeto do qual obter os símbolos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="49c9c-107">The object from which to get the property symbols.</span></span>  
  
 `propertySymbols`  
 <span data-ttu-id="49c9c-108">Uma matriz de símbolos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="49c9c-108">An array of property symbols.</span></span>  
  
## <span data-ttu-id="49c9c-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="49c9c-109">Return Value</span></span>  
 <span data-ttu-id="49c9c-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="49c9c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="49c9c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="49c9c-111">Remarks</span></span>  
 <span data-ttu-id="49c9c-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="49c9c-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="49c9c-113">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="49c9c-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="49c9c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49c9c-114">Requirements</span></span>  
 <span data-ttu-id="49c9c-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="49c9c-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="49c9c-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="49c9c-116">See Also</span></span>  
 [<span data-ttu-id="49c9c-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="49c9c-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)