---
description: Cria um valor JavaScript que é uma projeção do ponteiro passado `IInspectable` .
title: Função JsInspectableToObject | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5d3d91b38c9db5de2eb8fb02526f6072f0f5147
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231806"
---
# <span data-ttu-id="0585a-103">Função JsInspectableToObject</span><span class="sxs-lookup"><span data-stu-id="0585a-103">JsInspectableToObject Function</span></span>

<span data-ttu-id="0585a-104">Cria um valor JavaScript que é uma projeção do ponteiro passado `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="0585a-104">Creates a JavaScript value that is a projection of the passed in `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="0585a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0585a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsInspectableToObject(  
        _In_ IInspectable  *inspectable,  
        _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="0585a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0585a-106">Parameters</span></span>  
 `inspectable`  
 <span data-ttu-id="0585a-107">A `IInspectable` a a ser projetada.</span><span class="sxs-lookup"><span data-stu-id="0585a-107">A `IInspectable` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="0585a-108">Um valor JavaScript que é uma projeção de `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="0585a-108">A JavaScript value that is a projection of the `IInspectable`.</span></span>  
  
## <span data-ttu-id="0585a-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0585a-109">Return Value</span></span>  
 <span data-ttu-id="0585a-110">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="0585a-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0585a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0585a-111">Remarks</span></span>  
 <span data-ttu-id="0585a-112">O valor projetado pode ser usado pelo script para chamar um objeto WinRT.</span><span class="sxs-lookup"><span data-stu-id="0585a-112">The projected value can be used by script to call a WinRT object.</span></span> <span data-ttu-id="0585a-113">Os hosts são responsáveis por impor regras de Threading COM.</span><span class="sxs-lookup"><span data-stu-id="0585a-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="0585a-114">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="0585a-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="0585a-115">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="0585a-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="0585a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0585a-116">Requirements</span></span>  
 <span data-ttu-id="0585a-117">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0585a-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0585a-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0585a-118">See Also</span></span>  
 [<span data-ttu-id="0585a-119">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0585a-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
