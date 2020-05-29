---
description: Analisa um script e retorna uma função que representa o script.
title: Função JsParseScript | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsParseScript
helpviewer_keywords:
- JsParseScript function
ms.assetid: e9d0e363-7cbe-43eb-9dc0-1f47e586c9ab
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: dd224ef0e800f05e6e07580f545bc4af218b3498
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562150"
---
# <span data-ttu-id="bd5c4-103">Função JsParseScript</span><span class="sxs-lookup"><span data-stu-id="bd5c4-103">JsParseScript Function</span></span>
<span data-ttu-id="bd5c4-104">Analisa um script e retorna uma função que representa o script.</span><span class="sxs-lookup"><span data-stu-id="bd5c4-104">Parses a script and returns a function representing the script.</span></span>  
  
## <span data-ttu-id="bd5c4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd5c4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="bd5c4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd5c4-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="bd5c4-107">O script a ser analisado.</span><span class="sxs-lookup"><span data-stu-id="bd5c4-107">The script to parse.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="bd5c4-108">Um cookie identificando o script que pode ser usado por contextos de script debuggable.</span><span class="sxs-lookup"><span data-stu-id="bd5c4-108">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="bd5c4-109">O local de onde o script veio.</span><span class="sxs-lookup"><span data-stu-id="bd5c4-109">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="bd5c4-110">Uma função que representa o código de script.</span><span class="sxs-lookup"><span data-stu-id="bd5c4-110">A function representing the script code.</span></span>  
  
## <span data-ttu-id="bd5c4-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bd5c4-111">Return Value</span></span>  
 <span data-ttu-id="bd5c4-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="bd5c4-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bd5c4-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd5c4-113">Remarks</span></span>  
 <span data-ttu-id="bd5c4-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="bd5c4-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bd5c4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd5c4-115">Requirements</span></span>  
 <span data-ttu-id="bd5c4-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bd5c4-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bd5c4-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bd5c4-117">See Also</span></span>  
 [<span data-ttu-id="bd5c4-118">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bd5c4-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)