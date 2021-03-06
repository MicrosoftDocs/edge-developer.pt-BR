---
description: Referência do Protocolo DevTools Versão 0.1 (EdgeHTML) para o Domínio da Página. Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.
title: Domínio da Página - DevTools Protocol Versão 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b04b0685a6b465d40e999a2a48d370573a3058d8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399145"
---
# <a name="page-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="7de67-104">Domínio da Página - DevTools Protocol Versão 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="7de67-104">Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="7de67-105">Ações e eventos relacionados à página inspecionada pertencem ao domínio da página.</span><span class="sxs-lookup"><span data-stu-id="7de67-105">Actions and events related to the inspected page belong to the page domain.</span></span>  

| <span data-ttu-id="7de67-106">Classificação</span><span class="sxs-lookup"><span data-stu-id="7de67-106">Classification</span></span> | <span data-ttu-id="7de67-107">Membros</span><span class="sxs-lookup"><span data-stu-id="7de67-107">Members</span></span> |  
|:--- |:--- |  
| [**<span data-ttu-id="7de67-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="7de67-108">Methods</span></span>**](#methods) | <span data-ttu-id="7de67-109">[habilitar](#enable), [desabilitar,](#disable) [navegar](#navigate)</span><span class="sxs-lookup"><span data-stu-id="7de67-109">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |  
| [**<span data-ttu-id="7de67-110">Tipos</span><span class="sxs-lookup"><span data-stu-id="7de67-110">Types</span></span>**](#types) | [<span data-ttu-id="7de67-111">FrameId</span><span class="sxs-lookup"><span data-stu-id="7de67-111">FrameId</span></span>](#frameid) |  

## <a name="methods"></a><span data-ttu-id="7de67-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="7de67-112">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="7de67-113">Habilitar</span><span class="sxs-lookup"><span data-stu-id="7de67-113">enable</span></span>  

<span data-ttu-id="7de67-114">Habilita notificações de domínio de página.</span><span class="sxs-lookup"><span data-stu-id="7de67-114">Enables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="7de67-115">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="7de67-115">disable</span></span>  

<span data-ttu-id="7de67-116">Desabilita notificações de domínio de página.</span><span class="sxs-lookup"><span data-stu-id="7de67-116">Disables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="navigate"></a><span data-ttu-id="7de67-117">navegar</span><span class="sxs-lookup"><span data-stu-id="7de67-117">navigate</span></span>  

<span data-ttu-id="7de67-118">Navega a página atual para a URL determinada.</span><span class="sxs-lookup"><span data-stu-id="7de67-118">Navigates current page to the given URL.</span></span>  

| <span data-ttu-id="7de67-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7de67-119">Parameters</span></span> | <span data-ttu-id="7de67-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="7de67-120">Type</span></span> | <span data-ttu-id="7de67-121">Detalhes</span><span class="sxs-lookup"><span data-stu-id="7de67-121">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="7de67-122">url</span><span class="sxs-lookup"><span data-stu-id="7de67-122">url</span></span> | `string` | <span data-ttu-id="7de67-123">URL para navegar na página.</span><span class="sxs-lookup"><span data-stu-id="7de67-123">URL to navigate the page to.</span></span> |  

| <span data-ttu-id="7de67-124">Retorna</span><span class="sxs-lookup"><span data-stu-id="7de67-124">Returns</span></span> | <span data-ttu-id="7de67-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="7de67-125">Type</span></span> | <span data-ttu-id="7de67-126">Detalhes</span><span class="sxs-lookup"><span data-stu-id="7de67-126">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="7de67-127">frameId</span><span class="sxs-lookup"><span data-stu-id="7de67-127">frameId</span></span> | [<span data-ttu-id="7de67-128">FrameId</span><span class="sxs-lookup"><span data-stu-id="7de67-128">FrameId</span></span>](#frameid) | <span data-ttu-id="7de67-129">**Experimental**.</span><span class="sxs-lookup"><span data-stu-id="7de67-129">**Experimental**.</span></span>  <span data-ttu-id="7de67-130">ID do quadro que será navegada.</span><span class="sxs-lookup"><span data-stu-id="7de67-130">Frame ID that will be navigated.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="7de67-131">Tipos</span><span class="sxs-lookup"><span data-stu-id="7de67-131">Types</span></span>  

### <a name="frameid-string"></a><span data-ttu-id="7de67-132">Cadeia de caracteres FrameId</span><span class="sxs-lookup"><span data-stu-id="7de67-132">FrameId string</span></span>  

<a name="frameid"></a>  

<span data-ttu-id="7de67-133">Identificador de quadro exclusivo.</span><span class="sxs-lookup"><span data-stu-id="7de67-133">Unique frame identifier.</span></span>  

&nbsp;  

---  
