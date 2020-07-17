---
description: Referência para o domínio da página. Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.
title: Page Domain-DevTools Protocol Version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 1602673eae1c04f60046a898dbadeab1b59f9ce5
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882937"
---
# <span data-ttu-id="78c3d-104">Page Domain-DevTools Protocol Version 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="78c3d-104">Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="78c3d-105">Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.</span><span class="sxs-lookup"><span data-stu-id="78c3d-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="78c3d-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="78c3d-106">Methods</span></span>**](#methods) | <span data-ttu-id="78c3d-107">[habilitar](#enable), [desabilitar](#disable), [navegar](#navigate)</span><span class="sxs-lookup"><span data-stu-id="78c3d-107">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |
| [**<span data-ttu-id="78c3d-108">Tipos</span><span class="sxs-lookup"><span data-stu-id="78c3d-108">Types</span></span>**](#types) | [<span data-ttu-id="78c3d-109">Frameid</span><span class="sxs-lookup"><span data-stu-id="78c3d-109">FrameId</span></span>](#frameid) |
## <span data-ttu-id="78c3d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="78c3d-110">Methods</span></span>

### <span data-ttu-id="78c3d-111">Habilitar</span><span class="sxs-lookup"><span data-stu-id="78c3d-111">enable</span></span>
<span data-ttu-id="78c3d-112">Habilita as notificações de domínio da página.</span><span class="sxs-lookup"><span data-stu-id="78c3d-112">Enables page domain notifications.</span></span>


---

### <span data-ttu-id="78c3d-113">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="78c3d-113">disable</span></span>
<span data-ttu-id="78c3d-114">Desativa as notificações de domínio da página.</span><span class="sxs-lookup"><span data-stu-id="78c3d-114">Disables page domain notifications.</span></span>


---

### <span data-ttu-id="78c3d-115">navegar</span><span class="sxs-lookup"><span data-stu-id="78c3d-115">navigate</span></span>
<span data-ttu-id="78c3d-116">Navega a página atual para a URL fornecida.</span><span class="sxs-lookup"><span data-stu-id="78c3d-116">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="78c3d-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78c3d-117">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="78c3d-118">url</span><span class="sxs-lookup"><span data-stu-id="78c3d-118">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="78c3d-119">URL para navegar na página.</span><span class="sxs-lookup"><span data-stu-id="78c3d-119">URL to navigate the page to.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="78c3d-120">Devolver</span><span class="sxs-lookup"><span data-stu-id="78c3d-120">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="78c3d-121">frameid</span><span class="sxs-lookup"><span data-stu-id="78c3d-121">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b><span data-ttu-id="78c3d-122">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="78c3d-122">Experimental.</span></span> </b></span><span data-ttu-id="78c3d-123">ID do quadro que será navegada.</span><span class="sxs-lookup"><span data-stu-id="78c3d-123">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="78c3d-124">Tipos</span><span class="sxs-lookup"><span data-stu-id="78c3d-124">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="78c3d-125">Frameid</span><span class="sxs-lookup"><span data-stu-id="78c3d-125">FrameId</span></span> `string`

<span data-ttu-id="78c3d-126">Identificador de quadro exclusivo.</span><span class="sxs-lookup"><span data-stu-id="78c3d-126">Unique frame identifier.</span></span>


---
