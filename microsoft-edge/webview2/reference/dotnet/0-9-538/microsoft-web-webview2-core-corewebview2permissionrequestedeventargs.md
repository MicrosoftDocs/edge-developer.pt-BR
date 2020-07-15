---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: ede6cef20a1a0f5fcd0780376b5ddec07bf05d26
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878796"
---
# <span data-ttu-id="70283-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="70283-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

<span data-ttu-id="70283-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="70283-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="70283-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="70283-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="70283-107">Args de evento para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="70283-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="70283-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="70283-108">Summary</span></span>

 <span data-ttu-id="70283-109">Parte</span><span class="sxs-lookup"><span data-stu-id="70283-109">Members</span></span>                        | <span data-ttu-id="70283-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="70283-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="70283-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="70283-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="70283-112">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="70283-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="70283-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="70283-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="70283-114">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="70283-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="70283-115">Estado</span><span class="sxs-lookup"><span data-stu-id="70283-115">State</span></span>](#state) | <span data-ttu-id="70283-116">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="70283-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="70283-117">Uri</span><span class="sxs-lookup"><span data-stu-id="70283-117">Uri</span></span>](#uri) | <span data-ttu-id="70283-118">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="70283-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="70283-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="70283-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="70283-120">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="70283-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="70283-121">Parte</span><span class="sxs-lookup"><span data-stu-id="70283-121">Members</span></span>

#### <span data-ttu-id="70283-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="70283-122">IsUserInitiated</span></span> 

<span data-ttu-id="70283-123">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="70283-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="70283-124">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="70283-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="70283-125">Observe que a inicialização por meio de um gesto do usuário não significa que o usuário pretendia acessar o recurso associado.</span><span class="sxs-lookup"><span data-stu-id="70283-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="70283-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="70283-126">PermissionKind</span></span> 

<span data-ttu-id="70283-127">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="70283-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="70283-128">CoreWebView2PermissionKind público [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="70283-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="70283-129">Estado</span><span class="sxs-lookup"><span data-stu-id="70283-129">State</span></span> 

<span data-ttu-id="70283-130">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="70283-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="70283-131">[estado](#state) CoreWebView2PermissionState público</span><span class="sxs-lookup"><span data-stu-id="70283-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="70283-132">se a solicitação é concedida.</span><span class="sxs-lookup"><span data-stu-id="70283-132">whether the request is granted.</span></span>

<span data-ttu-id="70283-133">O valor padrão é CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="70283-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="70283-134">Uri</span><span class="sxs-lookup"><span data-stu-id="70283-134">Uri</span></span> 

<span data-ttu-id="70283-135">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="70283-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="70283-136">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="70283-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="70283-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="70283-137">GetDeferral</span></span> 

<span data-ttu-id="70283-138">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="70283-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="70283-139">Public CoreWebView2Deferral [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="70283-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="70283-140">O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="70283-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

