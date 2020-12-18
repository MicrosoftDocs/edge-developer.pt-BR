---
description: DevTools Protocol Version 0,1 (EdgeHTML) Reference para o domínio do esquema. Fornece informações sobre o esquema de protocolo.
title: Schema Domain-DevTools Protocol versão 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7b4ec71b7799ae099c673bd81fa5b15a8ddd5d27
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231690"
---
# <span data-ttu-id="7ee01-104">Schema Domain-DevTools Protocol versão 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="7ee01-104">Schema Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="7ee01-105">Fornece informações sobre o esquema de protocolo.</span><span class="sxs-lookup"><span data-stu-id="7ee01-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="7ee01-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="7ee01-106">Methods</span></span>**](#methods) | [<span data-ttu-id="7ee01-107">getdomains</span><span class="sxs-lookup"><span data-stu-id="7ee01-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="7ee01-108">Tipos</span><span class="sxs-lookup"><span data-stu-id="7ee01-108">Types</span></span>**](#types) | [<span data-ttu-id="7ee01-109">Domínio</span><span class="sxs-lookup"><span data-stu-id="7ee01-109">Domain</span></span>](#domain) |
## <span data-ttu-id="7ee01-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="7ee01-110">Methods</span></span>

### <span data-ttu-id="7ee01-111">getdomains</span><span class="sxs-lookup"><span data-stu-id="7ee01-111">getDomains</span></span>
<span data-ttu-id="7ee01-112">Retorna domínios com suporte.</span><span class="sxs-lookup"><span data-stu-id="7ee01-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7ee01-113">Devolver</span><span class="sxs-lookup"><span data-stu-id="7ee01-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7ee01-114">domínio</span><span class="sxs-lookup"><span data-stu-id="7ee01-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="7ee01-115">Lista de domínios com suporte.</span><span class="sxs-lookup"><span data-stu-id="7ee01-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="7ee01-116">Tipos</span><span class="sxs-lookup"><span data-stu-id="7ee01-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="7ee01-117">Domínio</span><span class="sxs-lookup"><span data-stu-id="7ee01-117">Domain</span></span> `object`

<span data-ttu-id="7ee01-118">Descrição do domínio do protocolo.</span><span class="sxs-lookup"><span data-stu-id="7ee01-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7ee01-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7ee01-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7ee01-120">name</span><span class="sxs-lookup"><span data-stu-id="7ee01-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7ee01-121">Nome do domínio.</span><span class="sxs-lookup"><span data-stu-id="7ee01-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7ee01-122">version</span><span class="sxs-lookup"><span data-stu-id="7ee01-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7ee01-123">Versão do domínio.</span><span class="sxs-lookup"><span data-stu-id="7ee01-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>

---
