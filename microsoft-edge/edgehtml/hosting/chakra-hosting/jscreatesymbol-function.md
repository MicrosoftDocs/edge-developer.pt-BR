---
description: Cria um símbolo JavaScript.
title: Função JsCreateSymbol | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2fccc5d9-f857-46cd-9aeb-f0a2e7cdee6b
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6a2f77f477aeebac150635d93cbd0cd043357256
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231639"
---
# <span data-ttu-id="49bdf-103">Função JsCreateSymbol</span><span class="sxs-lookup"><span data-stu-id="49bdf-103">JsCreateSymbol Function</span></span>

<span data-ttu-id="49bdf-104">Cria um símbolo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="49bdf-104">Creates a JavaScript symbol.</span></span>
  
## <span data-ttu-id="49bdf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49bdf-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSymbol(  
   _In_ JsValueRef description,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="49bdf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49bdf-106">Parameters</span></span>  
 `description`  
 <span data-ttu-id="49bdf-107">A descrição da cadeia de caracteres do símbolo.</span><span class="sxs-lookup"><span data-stu-id="49bdf-107">The string description of the symbol.</span></span> <span data-ttu-id="49bdf-108">Pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="49bdf-108">Can be null.</span></span>  
  
 `result`  
 <span data-ttu-id="49bdf-109">O novo símbolo.</span><span class="sxs-lookup"><span data-stu-id="49bdf-109">The new symbol.</span></span>  
  
## <span data-ttu-id="49bdf-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="49bdf-110">Return Value</span></span>  
 <span data-ttu-id="49bdf-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="49bdf-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="49bdf-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="49bdf-112">Remarks</span></span>  
 <span data-ttu-id="49bdf-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="49bdf-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="49bdf-114">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="49bdf-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="49bdf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49bdf-115">Requirements</span></span>  
 <span data-ttu-id="49bdf-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="49bdf-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="49bdf-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="49bdf-117">See Also</span></span>  
 [<span data-ttu-id="49bdf-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="49bdf-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
