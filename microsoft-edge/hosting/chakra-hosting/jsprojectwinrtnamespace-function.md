---
description: Projetar um namespace WinRT.
title: Função JsProjectWinRTNamespace | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8a23c154-df4b-4ce3-9fef-f41f90acdb87
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c4d63727b3d25bbb346fee7179ae0d942ae37008
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561005"
---
# <span data-ttu-id="d2055-103">Função JsProjectWinRTNamespace</span><span class="sxs-lookup"><span data-stu-id="d2055-103">JsProjectWinRTNamespace Function</span></span>
<span data-ttu-id="d2055-104">Projetar um namespace WinRT.</span><span class="sxs-lookup"><span data-stu-id="d2055-104">Project a WinRT namespace.</span></span>  
  
## <span data-ttu-id="d2055-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2055-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode)  
   JsProjectWinRTNamespace(  
   _In_z_ const wchar_t *namespaceName  
);  
```  
  
#### <span data-ttu-id="d2055-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2055-106">Parameters</span></span>  
 `namespaceName`  
 <span data-ttu-id="d2055-107">O namespace WinRT seja projetado.</span><span class="sxs-lookup"><span data-stu-id="d2055-107">The WinRT namespace to be projected.</span></span>  
  
## <span data-ttu-id="d2055-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d2055-108">Return Value</span></span>  
 <span data-ttu-id="d2055-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="d2055-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d2055-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2055-110">Remarks</span></span>  
 <span data-ttu-id="d2055-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="d2055-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="d2055-112">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="d2055-112">This API is supported only in EdgeHTML mode.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d2055-113">O WinRT foi o nome da plataforma antes da plataforma universal do Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="d2055-113">WinRT was the platform name before Universal Windows Platform (UWP).</span></span>  
  
## <span data-ttu-id="d2055-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2055-114">Requirements</span></span>  
 <span data-ttu-id="d2055-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d2055-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d2055-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d2055-116">See Also</span></span>  
 [<span data-ttu-id="d2055-117">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d2055-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)