---
description: Referência para o domínio da página. Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.
title: Página Domain-DevTools protocolo versão 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a1cd094baef4571240881a86ecccfdb319fef61b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561357"
---
# <span data-ttu-id="a54b9-104">Página</span><span class="sxs-lookup"><span data-stu-id="a54b9-104">Page</span></span>
<span data-ttu-id="a54b9-105">Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.</span><span class="sxs-lookup"><span data-stu-id="a54b9-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="a54b9-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="a54b9-106">Methods</span></span>**](#methods) | <span data-ttu-id="a54b9-107">[habilitar](#enable), [desabilitar](#disable), [navegar](#navigate)</span><span class="sxs-lookup"><span data-stu-id="a54b9-107">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |
| [**<span data-ttu-id="a54b9-108">Tipos</span><span class="sxs-lookup"><span data-stu-id="a54b9-108">Types</span></span>**](#types) | [<span data-ttu-id="a54b9-109">Frameid</span><span class="sxs-lookup"><span data-stu-id="a54b9-109">FrameId</span></span>](#frameid) |
## <span data-ttu-id="a54b9-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a54b9-110">Methods</span></span>

### <span data-ttu-id="a54b9-111">Habilitar</span><span class="sxs-lookup"><span data-stu-id="a54b9-111">enable</span></span>
<span data-ttu-id="a54b9-112">Habilita as notificações de domínio da página.</span><span class="sxs-lookup"><span data-stu-id="a54b9-112">Enables page domain notifications.</span></span>


---

### <span data-ttu-id="a54b9-113">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="a54b9-113">disable</span></span>
<span data-ttu-id="a54b9-114">Desativa as notificações de domínio da página.</span><span class="sxs-lookup"><span data-stu-id="a54b9-114">Disables page domain notifications.</span></span>


---

### <span data-ttu-id="a54b9-115">navegar</span><span class="sxs-lookup"><span data-stu-id="a54b9-115">navigate</span></span>
<span data-ttu-id="a54b9-116">Navega a página atual para a URL fornecida.</span><span class="sxs-lookup"><span data-stu-id="a54b9-116">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a54b9-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a54b9-117">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a54b9-118">url</span><span class="sxs-lookup"><span data-stu-id="a54b9-118">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a54b9-119">URL para navegar na página.</span><span class="sxs-lookup"><span data-stu-id="a54b9-119">URL to navigate the page to.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a54b9-120">Devolver</span><span class="sxs-lookup"><span data-stu-id="a54b9-120">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a54b9-121">frameid</span><span class="sxs-lookup"><span data-stu-id="a54b9-121">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b><span data-ttu-id="a54b9-122">Experimentais.</span><span class="sxs-lookup"><span data-stu-id="a54b9-122">Experimental.</span></span> </b></span><span data-ttu-id="a54b9-123">ID do quadro que será navegada.</span><span class="sxs-lookup"><span data-stu-id="a54b9-123">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="a54b9-124">Tipos</span><span class="sxs-lookup"><span data-stu-id="a54b9-124">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="a54b9-125">Frameid</span><span class="sxs-lookup"><span data-stu-id="a54b9-125">FrameId</span></span> `string`

<span data-ttu-id="a54b9-126">Identificador de quadro exclusivo.</span><span class="sxs-lookup"><span data-stu-id="a54b9-126">Unique frame identifier.</span></span>


---
