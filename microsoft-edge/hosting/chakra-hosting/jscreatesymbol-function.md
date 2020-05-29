---
description: Cria um símbolo JavaScript.
title: Função JsCreateSymbol | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2fccc5d9-f857-46cd-9aeb-f0a2e7cdee6b
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a4e634e6f0726ca32ad1056129186ce941edb77b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561084"
---
# <span data-ttu-id="65630-103">Função JsCreateSymbol</span><span class="sxs-lookup"><span data-stu-id="65630-103">JsCreateSymbol Function</span></span>
<span data-ttu-id="65630-104">Cria um símbolo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="65630-104">Creates a JavaScript symbol.</span></span>
  
## <span data-ttu-id="65630-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65630-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSymbol(  
   _In_ JsValueRef description,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="65630-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65630-106">Parameters</span></span>  
 `description`  
 <span data-ttu-id="65630-107">A descrição da cadeia de caracteres do símbolo.</span><span class="sxs-lookup"><span data-stu-id="65630-107">The string description of the symbol.</span></span> <span data-ttu-id="65630-108">Pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="65630-108">Can be null.</span></span>  
  
 `result`  
 <span data-ttu-id="65630-109">O novo símbolo.</span><span class="sxs-lookup"><span data-stu-id="65630-109">The new symbol.</span></span>  
  
## <span data-ttu-id="65630-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="65630-110">Return Value</span></span>  
 <span data-ttu-id="65630-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="65630-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="65630-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="65630-112">Remarks</span></span>  
 <span data-ttu-id="65630-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="65630-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="65630-114">Essa API só tem suporte no modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="65630-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="65630-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65630-115">Requirements</span></span>  
 <span data-ttu-id="65630-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="65630-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="65630-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="65630-117">See Also</span></span>  
 [<span data-ttu-id="65630-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="65630-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)