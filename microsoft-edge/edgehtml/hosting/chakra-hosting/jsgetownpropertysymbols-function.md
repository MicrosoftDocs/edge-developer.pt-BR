---
description: Obtém a lista de todas as propriedades de símbolo no objeto.
title: Função JsGetOwnPropertySymbols | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 57c431e3-de0b-4ed0-b750-87a86448daff
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d44da140f61a17d4cdc3a959c8fa7d017cbab1cc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231790"
---
# <span data-ttu-id="df1e3-103">Função JsGetOwnPropertySymbols</span><span class="sxs-lookup"><span data-stu-id="df1e3-103">JsGetOwnPropertySymbols Function</span></span>

<span data-ttu-id="df1e3-104">Obtém a lista de todas as propriedades de símbolo no objeto.</span><span class="sxs-lookup"><span data-stu-id="df1e3-104">Gets the list of all symbol properties on the object.</span></span>  
  
## <span data-ttu-id="df1e3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df1e3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertySymbols(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertySymbols  
);  
```  
  
#### <span data-ttu-id="df1e3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df1e3-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="df1e3-107">O objeto do qual obter os símbolos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="df1e3-107">The object from which to get the property symbols.</span></span>  
  
 `propertySymbols`  
 <span data-ttu-id="df1e3-108">Uma matriz de símbolos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="df1e3-108">An array of property symbols.</span></span>  
  
## <span data-ttu-id="df1e3-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="df1e3-109">Return Value</span></span>  
 <span data-ttu-id="df1e3-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="df1e3-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="df1e3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="df1e3-111">Remarks</span></span>  
 <span data-ttu-id="df1e3-112">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="df1e3-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="df1e3-113">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="df1e3-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="df1e3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df1e3-114">Requirements</span></span>  
 <span data-ttu-id="df1e3-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="df1e3-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="df1e3-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="df1e3-116">See Also</span></span>  
 [<span data-ttu-id="df1e3-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="df1e3-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
