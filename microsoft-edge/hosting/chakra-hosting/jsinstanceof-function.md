---
description: Executa o `instanceof` teste de operador JavaScript.
title: Função JsInstanceOf | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 94399a62-b996-4fd2-82ce-1c26e7a4da08
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4d9bf2e4c3da9f83fdf7c0ef4e2c31df04670420
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751972"
---
# <span data-ttu-id="c53a0-103">Função JsInstanceOf</span><span class="sxs-lookup"><span data-stu-id="c53a0-103">JsInstanceOf Function</span></span>
<span data-ttu-id="c53a0-104">Executa o `instanceof` teste de operador JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c53a0-104">Performs JavaScript `instanceof` operator test.</span></span>  
  
## <span data-ttu-id="c53a0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c53a0-105">Syntax</span></span>  
  
```cpp  
JsInstanceOf(   
  _In_ JsValueRef object,  
  _In_ JsValueRef constructor,  
  _Out_ bool *result  
);  
  
```  
  
#### <span data-ttu-id="c53a0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c53a0-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="c53a0-107">O objeto a ser testado.</span><span class="sxs-lookup"><span data-stu-id="c53a0-107">The object to test.</span></span>  
  
 `constructor`  
 <span data-ttu-id="c53a0-108">A função do Construtor a ser testada.</span><span class="sxs-lookup"><span data-stu-id="c53a0-108">The constructor function to test against.</span></span>  
  
 `result`  
 <span data-ttu-id="c53a0-109">Se o "Construtor do objeto instanceof" é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="c53a0-109">Whether the "object instanceof constructor" is true.</span></span>  
  
## <span data-ttu-id="c53a0-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c53a0-110">Return Value</span></span>  
 <span data-ttu-id="c53a0-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="c53a0-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c53a0-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c53a0-112">Remarks</span></span>  
 <span data-ttu-id="c53a0-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="c53a0-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c53a0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c53a0-114">Requirements</span></span>  
 <span data-ttu-id="c53a0-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c53a0-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c53a0-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c53a0-116">See Also</span></span>  
 [<span data-ttu-id="c53a0-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c53a0-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)