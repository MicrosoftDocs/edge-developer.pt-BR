---
description: Referência para o domínio do esquema. Fornece informações sobre o esquema de protocolo.
title: Schema Domain-DevTools Protocol versão 0,2
author: pelavall
ms.author: pelavall
ms.date: 8/17/2018
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: df86e6669956c14b7c905514fc44376f71eaa993
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561326"
---
# <span data-ttu-id="7298c-104">Esquema</span><span class="sxs-lookup"><span data-stu-id="7298c-104">Schema</span></span>
<span data-ttu-id="7298c-105">Fornece informações sobre o esquema de protocolo.</span><span class="sxs-lookup"><span data-stu-id="7298c-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="7298c-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="7298c-106">Methods</span></span>**](#methods) | [<span data-ttu-id="7298c-107">getdomains</span><span class="sxs-lookup"><span data-stu-id="7298c-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="7298c-108">Tipos</span><span class="sxs-lookup"><span data-stu-id="7298c-108">Types</span></span>**](#types) | [<span data-ttu-id="7298c-109">Domínio</span><span class="sxs-lookup"><span data-stu-id="7298c-109">Domain</span></span>](#domain) |
## <span data-ttu-id="7298c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="7298c-110">Methods</span></span>

### <span data-ttu-id="7298c-111">getdomains</span><span class="sxs-lookup"><span data-stu-id="7298c-111">getDomains</span></span>
<span data-ttu-id="7298c-112">Retorna domínios com suporte.</span><span class="sxs-lookup"><span data-stu-id="7298c-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7298c-113">Devolver</span><span class="sxs-lookup"><span data-stu-id="7298c-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7298c-114">domínio</span><span class="sxs-lookup"><span data-stu-id="7298c-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="7298c-115">Lista de domínios com suporte.</span><span class="sxs-lookup"><span data-stu-id="7298c-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="7298c-116">Tipos</span><span class="sxs-lookup"><span data-stu-id="7298c-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="7298c-117">Domínio</span><span class="sxs-lookup"><span data-stu-id="7298c-117">Domain</span></span> `object`

<span data-ttu-id="7298c-118">Descrição do domínio do protocolo.</span><span class="sxs-lookup"><span data-stu-id="7298c-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7298c-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7298c-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7298c-120">name</span><span class="sxs-lookup"><span data-stu-id="7298c-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7298c-121">Nome do domínio.</span><span class="sxs-lookup"><span data-stu-id="7298c-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7298c-122">version</span><span class="sxs-lookup"><span data-stu-id="7298c-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7298c-123">Versão do domínio.</span><span class="sxs-lookup"><span data-stu-id="7298c-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
