---
description: Executa o `instanceof` teste de operador JavaScript.
title: Função JsInstanceOf | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 94399a62-b996-4fd2-82ce-1c26e7a4da08
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d8aec1d4512fe937d1fd48aa6f3e88294bf9850c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231804"
---
# <span data-ttu-id="8c435-103">Função JsInstanceOf</span><span class="sxs-lookup"><span data-stu-id="8c435-103">JsInstanceOf Function</span></span>

<span data-ttu-id="8c435-104">Executa o `instanceof` teste de operador JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8c435-104">Performs JavaScript `instanceof` operator test.</span></span>  
  
## <span data-ttu-id="8c435-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c435-105">Syntax</span></span>  
  
```cpp  
JsInstanceOf(   
  _In_ JsValueRef object,  
  _In_ JsValueRef constructor,  
  _Out_ bool *result  
);  
  
```  
  
#### <span data-ttu-id="8c435-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c435-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="8c435-107">O objeto a ser testado.</span><span class="sxs-lookup"><span data-stu-id="8c435-107">The object to test.</span></span>  
  
 `constructor`  
 <span data-ttu-id="8c435-108">A função do Construtor a ser testada.</span><span class="sxs-lookup"><span data-stu-id="8c435-108">The constructor function to test against.</span></span>  
  
 `result`  
 <span data-ttu-id="8c435-109">Se o "Construtor do objeto instanceof" é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="8c435-109">Whether the "object instanceof constructor" is true.</span></span>  
  
## <span data-ttu-id="8c435-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8c435-110">Return Value</span></span>  
 <span data-ttu-id="8c435-111">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="8c435-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8c435-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c435-112">Remarks</span></span>  
 <span data-ttu-id="8c435-113">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="8c435-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="8c435-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c435-114">Requirements</span></span>  
 <span data-ttu-id="8c435-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8c435-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8c435-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8c435-116">See Also</span></span>  
 [<span data-ttu-id="8c435-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8c435-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
