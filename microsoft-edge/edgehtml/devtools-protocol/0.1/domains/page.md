---
description: Referência do protocolo DevTools versão 0,1 (EdgeHTML) para o domínio da página. Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.
title: Page Domain-DevTools Protocol Version 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55575e54b9125d7ff544c23c81da4b15d3b56fb1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231697"
---
# <span data-ttu-id="54fb3-104">Page Domain-DevTools Protocol Version 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="54fb3-104">Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="54fb3-105">Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.</span><span class="sxs-lookup"><span data-stu-id="54fb3-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="54fb3-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="54fb3-106">Methods</span></span>**](#methods) | <span data-ttu-id="54fb3-107">[habilitar](#enable), [desabilitar](#disable), [navegar](#navigate)</span><span class="sxs-lookup"><span data-stu-id="54fb3-107">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |
| [**<span data-ttu-id="54fb3-108">Tipos</span><span class="sxs-lookup"><span data-stu-id="54fb3-108">Types</span></span>**](#types) | [<span data-ttu-id="54fb3-109">Frameid</span><span class="sxs-lookup"><span data-stu-id="54fb3-109">FrameId</span></span>](#frameid) |
## <span data-ttu-id="54fb3-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="54fb3-110">Methods</span></span>

### <span data-ttu-id="54fb3-111">Habilitar</span><span class="sxs-lookup"><span data-stu-id="54fb3-111">enable</span></span>
<span data-ttu-id="54fb3-112">Habilita as notificações de domínio da página.</span><span class="sxs-lookup"><span data-stu-id="54fb3-112">Enables page domain notifications.</span></span>


---

### <span data-ttu-id="54fb3-113">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="54fb3-113">disable</span></span>
<span data-ttu-id="54fb3-114">Desativa as notificações de domínio da página.</span><span class="sxs-lookup"><span data-stu-id="54fb3-114">Disables page domain notifications.</span></span>


---

### <span data-ttu-id="54fb3-115">navegar</span><span class="sxs-lookup"><span data-stu-id="54fb3-115">navigate</span></span>
<span data-ttu-id="54fb3-116">Navega a página atual para a URL fornecida.</span><span class="sxs-lookup"><span data-stu-id="54fb3-116">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="54fb3-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54fb3-117">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="54fb3-118">url</span><span class="sxs-lookup"><span data-stu-id="54fb3-118">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="54fb3-119">URL para navegar na página.</span><span class="sxs-lookup"><span data-stu-id="54fb3-119">URL to navigate the page to.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="54fb3-120">Devolver</span><span class="sxs-lookup"><span data-stu-id="54fb3-120">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="54fb3-121">frameid</span><span class="sxs-lookup"><span data-stu-id="54fb3-121">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b><span data-ttu-id="54fb3-122">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="54fb3-122">Experimental.</span></span> </b></span><span data-ttu-id="54fb3-123">ID do quadro que será navegada.</span><span class="sxs-lookup"><span data-stu-id="54fb3-123">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="54fb3-124">Tipos</span><span class="sxs-lookup"><span data-stu-id="54fb3-124">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="54fb3-125">Frameid</span><span class="sxs-lookup"><span data-stu-id="54fb3-125">FrameId</span></span> `string`

<span data-ttu-id="54fb3-126">Identificador de quadro exclusivo.</span><span class="sxs-lookup"><span data-stu-id="54fb3-126">Unique frame identifier.</span></span>


---
