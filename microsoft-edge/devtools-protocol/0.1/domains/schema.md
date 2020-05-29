---
description: Referência para o domínio do esquema. Fornece informações sobre o esquema de protocolo.
title: Schema Domain-DevTools Protocol versão 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 83d7019d18ccce1c81b67aafdcafe1a8566694ea
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561351"
---
# <span data-ttu-id="1b3ac-104">Esquema</span><span class="sxs-lookup"><span data-stu-id="1b3ac-104">Schema</span></span>
<span data-ttu-id="1b3ac-105">Fornece informações sobre o esquema de protocolo.</span><span class="sxs-lookup"><span data-stu-id="1b3ac-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="1b3ac-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="1b3ac-106">Methods</span></span>**](#methods) | [<span data-ttu-id="1b3ac-107">getdomains</span><span class="sxs-lookup"><span data-stu-id="1b3ac-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="1b3ac-108">Tipos</span><span class="sxs-lookup"><span data-stu-id="1b3ac-108">Types</span></span>**](#types) | [<span data-ttu-id="1b3ac-109">Domínio</span><span class="sxs-lookup"><span data-stu-id="1b3ac-109">Domain</span></span>](#domain) |
## <span data-ttu-id="1b3ac-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="1b3ac-110">Methods</span></span>

### <span data-ttu-id="1b3ac-111">getdomains</span><span class="sxs-lookup"><span data-stu-id="1b3ac-111">getDomains</span></span>
<span data-ttu-id="1b3ac-112">Retorna domínios com suporte.</span><span class="sxs-lookup"><span data-stu-id="1b3ac-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="1b3ac-113">Devolver</span><span class="sxs-lookup"><span data-stu-id="1b3ac-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="1b3ac-114">domínio</span><span class="sxs-lookup"><span data-stu-id="1b3ac-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="1b3ac-115">Lista de domínios com suporte.</span><span class="sxs-lookup"><span data-stu-id="1b3ac-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="1b3ac-116">Tipos</span><span class="sxs-lookup"><span data-stu-id="1b3ac-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="1b3ac-117">Domínio</span><span class="sxs-lookup"><span data-stu-id="1b3ac-117">Domain</span></span> `object`

<span data-ttu-id="1b3ac-118">Descrição do domínio do protocolo.</span><span class="sxs-lookup"><span data-stu-id="1b3ac-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="1b3ac-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1b3ac-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="1b3ac-120">name</span><span class="sxs-lookup"><span data-stu-id="1b3ac-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="1b3ac-121">Nome do domínio.</span><span class="sxs-lookup"><span data-stu-id="1b3ac-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="1b3ac-122">version</span><span class="sxs-lookup"><span data-stu-id="1b3ac-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="1b3ac-123">Versão do domínio.</span><span class="sxs-lookup"><span data-stu-id="1b3ac-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>

---
