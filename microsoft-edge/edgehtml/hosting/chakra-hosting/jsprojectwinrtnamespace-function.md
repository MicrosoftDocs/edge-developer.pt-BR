---
description: Projetar um namespace WinRT.
title: Função JsProjectWinRTNamespace | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8a23c154-df4b-4ce3-9fef-f41f90acdb87
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f781cf90aaec68b2bd305bf34c453fc663ad0187
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231989"
---
# <span data-ttu-id="abdcb-103">Função JsProjectWinRTNamespace</span><span class="sxs-lookup"><span data-stu-id="abdcb-103">JsProjectWinRTNamespace Function</span></span>

<span data-ttu-id="abdcb-104">Projetar um namespace WinRT.</span><span class="sxs-lookup"><span data-stu-id="abdcb-104">Project a WinRT namespace.</span></span>  
  
## <span data-ttu-id="abdcb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abdcb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode)  
   JsProjectWinRTNamespace(  
   _In_z_ const wchar_t *namespaceName  
);  
```  
  
#### <span data-ttu-id="abdcb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abdcb-106">Parameters</span></span>  
 `namespaceName`  
 <span data-ttu-id="abdcb-107">O namespace WinRT seja projetado.</span><span class="sxs-lookup"><span data-stu-id="abdcb-107">The WinRT namespace to be projected.</span></span>  
  
## <span data-ttu-id="abdcb-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="abdcb-108">Return Value</span></span>  
 <span data-ttu-id="abdcb-109">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="abdcb-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="abdcb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="abdcb-110">Remarks</span></span>  
 <span data-ttu-id="abdcb-111">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="abdcb-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="abdcb-112">Essa API só tem suporte no modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="abdcb-112">This API is supported only in EdgeHTML mode.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="abdcb-113">O WinRT foi o nome da plataforma antes da plataforma universal do Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="abdcb-113">WinRT was the platform name before Universal Windows Platform (UWP).</span></span>  
  
## <span data-ttu-id="abdcb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abdcb-114">Requirements</span></span>  
 <span data-ttu-id="abdcb-115">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="abdcb-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="abdcb-116">Consulte também</span><span class="sxs-lookup"><span data-stu-id="abdcb-116">See Also</span></span>  
 [<span data-ttu-id="abdcb-117">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="abdcb-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
