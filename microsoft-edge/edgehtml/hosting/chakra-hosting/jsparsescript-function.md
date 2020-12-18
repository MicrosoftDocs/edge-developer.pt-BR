---
description: Analisa um script e retorna uma função que representa o script.
title: Função JsParseScript | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsParseScript
helpviewer_keywords:
- JsParseScript function
ms.assetid: e9d0e363-7cbe-43eb-9dc0-1f47e586c9ab
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 656d9a992868a3cb892808775f160092b8eaf069
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231757"
---
# <span data-ttu-id="15770-103">Função JsParseScript</span><span class="sxs-lookup"><span data-stu-id="15770-103">JsParseScript Function</span></span>

<span data-ttu-id="15770-104">Analisa um script e retorna uma função que representa o script.</span><span class="sxs-lookup"><span data-stu-id="15770-104">Parses a script and returns a function representing the script.</span></span>  
  
## <span data-ttu-id="15770-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15770-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="15770-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15770-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="15770-107">O script a ser analisado.</span><span class="sxs-lookup"><span data-stu-id="15770-107">The script to parse.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="15770-108">Um cookie identificando o script que pode ser usado por contextos de script debuggable.</span><span class="sxs-lookup"><span data-stu-id="15770-108">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="15770-109">O local de onde o script veio.</span><span class="sxs-lookup"><span data-stu-id="15770-109">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="15770-110">Uma função que representa o código de script.</span><span class="sxs-lookup"><span data-stu-id="15770-110">A function representing the script code.</span></span>  
  
## <span data-ttu-id="15770-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="15770-111">Return Value</span></span>  
 <span data-ttu-id="15770-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="15770-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="15770-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="15770-113">Remarks</span></span>  
 <span data-ttu-id="15770-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="15770-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="15770-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15770-115">Requirements</span></span>  
 <span data-ttu-id="15770-116">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="15770-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="15770-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="15770-117">See Also</span></span>  
 [<span data-ttu-id="15770-118">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="15770-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
