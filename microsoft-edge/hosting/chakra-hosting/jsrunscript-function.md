---
description: Executa um script.
title: Função JsRunScript | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRunScript
helpviewer_keywords:
- JsRunScript function
ms.assetid: 8d6b8c9a-af3a-4e21-a330-5a6b535423a3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 49a06e4e6ad0c04e124b76f31d38b2e362e03f99
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562136"
---
# <span data-ttu-id="fb8ad-103">Função JsRunScript</span><span class="sxs-lookup"><span data-stu-id="fb8ad-103">JsRunScript Function</span></span>
<span data-ttu-id="fb8ad-104">Executa um script.</span><span class="sxs-lookup"><span data-stu-id="fb8ad-104">Executes a script.</span></span>  
  
## <span data-ttu-id="fb8ad-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb8ad-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="fb8ad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb8ad-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="fb8ad-107">O script a ser executado.</span><span class="sxs-lookup"><span data-stu-id="fb8ad-107">The script to run.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="fb8ad-108">Um cookie identificando o script que pode ser usado por contextos de script debuggable.</span><span class="sxs-lookup"><span data-stu-id="fb8ad-108">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="fb8ad-109">O local de onde o script veio.</span><span class="sxs-lookup"><span data-stu-id="fb8ad-109">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="fb8ad-110">O resultado do script, se houver.</span><span class="sxs-lookup"><span data-stu-id="fb8ad-110">The result of the script, if any.</span></span> <span data-ttu-id="fb8ad-111">Esse parâmetro pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="fb8ad-111">This parameter can be null.</span></span>  
  
## <span data-ttu-id="fb8ad-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fb8ad-112">Return Value</span></span>  
 <span data-ttu-id="fb8ad-113">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="fb8ad-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fb8ad-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb8ad-114">Remarks</span></span>  
 <span data-ttu-id="fb8ad-115">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="fb8ad-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="fb8ad-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb8ad-116">Requirements</span></span>  
 <span data-ttu-id="fb8ad-117">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fb8ad-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fb8ad-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fb8ad-118">See Also</span></span>  
 [<span data-ttu-id="fb8ad-119">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fb8ad-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)