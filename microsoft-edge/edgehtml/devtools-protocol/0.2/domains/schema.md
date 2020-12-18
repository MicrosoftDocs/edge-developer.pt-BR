---
description: DevTools Protocol Version 0,2 (EdgeHTML) Reference para o domínio do esquema. Fornece informações sobre o esquema de protocolo.
title: Schema Domain-DevTools Protocol versão 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/16/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 53038a02844fafc9550a6ac26303620a1a0183f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231302"
---
# <span data-ttu-id="b9366-104">Schema Domain-DevTools Protocol versão 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="b9366-104">Schema Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="b9366-105">Fornece informações sobre o esquema de protocolo.</span><span class="sxs-lookup"><span data-stu-id="b9366-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="b9366-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="b9366-106">Methods</span></span>**](#methods) | [<span data-ttu-id="b9366-107">getdomains</span><span class="sxs-lookup"><span data-stu-id="b9366-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="b9366-108">Tipos</span><span class="sxs-lookup"><span data-stu-id="b9366-108">Types</span></span>**](#types) | [<span data-ttu-id="b9366-109">Domínio</span><span class="sxs-lookup"><span data-stu-id="b9366-109">Domain</span></span>](#domain) |
## <span data-ttu-id="b9366-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b9366-110">Methods</span></span>

### <span data-ttu-id="b9366-111">getdomains</span><span class="sxs-lookup"><span data-stu-id="b9366-111">getDomains</span></span>
<span data-ttu-id="b9366-112">Retorna domínios com suporte.</span><span class="sxs-lookup"><span data-stu-id="b9366-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b9366-113">Devolver</span><span class="sxs-lookup"><span data-stu-id="b9366-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b9366-114">domínio</span><span class="sxs-lookup"><span data-stu-id="b9366-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="b9366-115">Lista de domínios com suporte.</span><span class="sxs-lookup"><span data-stu-id="b9366-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="b9366-116">Tipos</span><span class="sxs-lookup"><span data-stu-id="b9366-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="b9366-117">Domínio</span><span class="sxs-lookup"><span data-stu-id="b9366-117">Domain</span></span> `object`

<span data-ttu-id="b9366-118">Descrição do domínio do protocolo.</span><span class="sxs-lookup"><span data-stu-id="b9366-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="b9366-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b9366-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="b9366-120">name</span><span class="sxs-lookup"><span data-stu-id="b9366-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b9366-121">Nome do domínio.</span><span class="sxs-lookup"><span data-stu-id="b9366-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="b9366-122">version</span><span class="sxs-lookup"><span data-stu-id="b9366-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="b9366-123">Versão do domínio.</span><span class="sxs-lookup"><span data-stu-id="b9366-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
