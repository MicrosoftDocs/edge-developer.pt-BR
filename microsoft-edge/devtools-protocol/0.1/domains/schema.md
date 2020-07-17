---
description: Referência para o domínio do esquema. Fornece informações sobre o esquema de protocolo.
title: Schema Domain-DevTools Protocol versão 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a2f679f6f4bf8e82dc7298d96f798507b1338062
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882923"
---
# <span data-ttu-id="e6067-104">Schema Domain-DevTools Protocol versão 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="e6067-104">Schema Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="e6067-105">Fornece informações sobre o esquema de protocolo.</span><span class="sxs-lookup"><span data-stu-id="e6067-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="e6067-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6067-106">Methods</span></span>**](#methods) | [<span data-ttu-id="e6067-107">getdomains</span><span class="sxs-lookup"><span data-stu-id="e6067-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="e6067-108">Tipos</span><span class="sxs-lookup"><span data-stu-id="e6067-108">Types</span></span>**](#types) | [<span data-ttu-id="e6067-109">Domínio</span><span class="sxs-lookup"><span data-stu-id="e6067-109">Domain</span></span>](#domain) |
## <span data-ttu-id="e6067-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6067-110">Methods</span></span>

### <span data-ttu-id="e6067-111">getdomains</span><span class="sxs-lookup"><span data-stu-id="e6067-111">getDomains</span></span>
<span data-ttu-id="e6067-112">Retorna domínios com suporte.</span><span class="sxs-lookup"><span data-stu-id="e6067-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e6067-113">Devolver</span><span class="sxs-lookup"><span data-stu-id="e6067-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e6067-114">domínio</span><span class="sxs-lookup"><span data-stu-id="e6067-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="e6067-115">Lista de domínios com suporte.</span><span class="sxs-lookup"><span data-stu-id="e6067-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="e6067-116">Tipos</span><span class="sxs-lookup"><span data-stu-id="e6067-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="e6067-117">Domínio</span><span class="sxs-lookup"><span data-stu-id="e6067-117">Domain</span></span> `object`

<span data-ttu-id="e6067-118">Descrição do domínio do protocolo.</span><span class="sxs-lookup"><span data-stu-id="e6067-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e6067-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e6067-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="e6067-120">name</span><span class="sxs-lookup"><span data-stu-id="e6067-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e6067-121">Nome do domínio.</span><span class="sxs-lookup"><span data-stu-id="e6067-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="e6067-122">version</span><span class="sxs-lookup"><span data-stu-id="e6067-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="e6067-123">Versão do domínio.</span><span class="sxs-lookup"><span data-stu-id="e6067-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>

---
