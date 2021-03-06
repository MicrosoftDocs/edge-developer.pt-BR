---
description: Referência do Protocolo DevTools Versão 0.1 (EdgeHTML) para o Domínio de Esquema. Fornece informações sobre o esquema de protocolo.
title: Domínio do Esquema - DevTools Protocol Versão 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e89f4269b4984ee49e83a23fcab9679485c49040
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398858"
---
# <a name="schema-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="081ba-104">Domínio do Esquema - DevTools Protocol Versão 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="081ba-104">Schema Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="081ba-105">Fornece informações sobre o esquema de protocolo.</span><span class="sxs-lookup"><span data-stu-id="081ba-105">Provides information about the protocol schema.</span></span>  

| <span data-ttu-id="081ba-106">Classificação</span><span class="sxs-lookup"><span data-stu-id="081ba-106">Classification</span></span> | <span data-ttu-id="081ba-107">Membros</span><span class="sxs-lookup"><span data-stu-id="081ba-107">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="081ba-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="081ba-108">Methods</span></span>](#methods) | [<span data-ttu-id="081ba-109">getDomains</span><span class="sxs-lookup"><span data-stu-id="081ba-109">getDomains</span></span>](#getdomains) |  
| [<span data-ttu-id="081ba-110">Tipos</span><span class="sxs-lookup"><span data-stu-id="081ba-110">Types</span></span>](#types) | [<span data-ttu-id="081ba-111">Domínio</span><span class="sxs-lookup"><span data-stu-id="081ba-111">Domain</span></span>](#domain) |  

## <a name="methods"></a><span data-ttu-id="081ba-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="081ba-112">Methods</span></span>  

### <a name="getdomains"></a><span data-ttu-id="081ba-113">getDomains</span><span class="sxs-lookup"><span data-stu-id="081ba-113">getDomains</span></span>  

<span data-ttu-id="081ba-114">Retorna domínios com suporte.</span><span class="sxs-lookup"><span data-stu-id="081ba-114">Returns supported domains.</span></span>  

| <span data-ttu-id="081ba-115">Retorna</span><span class="sxs-lookup"><span data-stu-id="081ba-115">Returns</span></span> | <span data-ttu-id="081ba-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="081ba-116">Type</span></span> | <span data-ttu-id="081ba-117">Detalhes</span><span class="sxs-lookup"><span data-stu-id="081ba-117">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="081ba-118">domínios</span><span class="sxs-lookup"><span data-stu-id="081ba-118">domains</span></span> | [<span data-ttu-id="081ba-119">Domínio[]</span><span class="sxs-lookup"><span data-stu-id="081ba-119">Domain[]</span></span>](#domain) | <span data-ttu-id="081ba-120">Lista de domínios com suporte.</span><span class="sxs-lookup"><span data-stu-id="081ba-120">List of supported domains.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="081ba-121">Tipos</span><span class="sxs-lookup"><span data-stu-id="081ba-121">Types</span></span>  

### <a name="domain-object"></a><span data-ttu-id="081ba-122">Objeto Domain</span><span class="sxs-lookup"><span data-stu-id="081ba-122">Domain object</span></span>  

<a name="domain"></a>  

<span data-ttu-id="081ba-123">Descrição do domínio do protocolo.</span><span class="sxs-lookup"><span data-stu-id="081ba-123">Description of the protocol domain.</span></span>  

| <span data-ttu-id="081ba-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="081ba-124">Properties</span></span> | <span data-ttu-id="081ba-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="081ba-125">Type</span></span> | <span data-ttu-id="081ba-126">Detalhes</span><span class="sxs-lookup"><span data-stu-id="081ba-126">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="081ba-127">name</span><span class="sxs-lookup"><span data-stu-id="081ba-127">name</span></span> | `string` | <span data-ttu-id="081ba-128">Nome do domínio.</span><span class="sxs-lookup"><span data-stu-id="081ba-128">Domain name.</span></span> |  
| <span data-ttu-id="081ba-129">version</span><span class="sxs-lookup"><span data-stu-id="081ba-129">version</span></span> | `string` | <span data-ttu-id="081ba-130">Versão de domínio.</span><span class="sxs-lookup"><span data-stu-id="081ba-130">Domain version.</span></span> |  

---  
