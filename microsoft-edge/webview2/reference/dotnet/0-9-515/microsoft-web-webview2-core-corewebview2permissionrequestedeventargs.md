---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 5aeeebfc3d8434c096e6946e5161437809f207d3
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652371"
---
# <span data-ttu-id="4d13d-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="4d13d-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

<span data-ttu-id="4d13d-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="4d13d-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="4d13d-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="4d13d-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="4d13d-107">Args de evento para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="4d13d-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="4d13d-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="4d13d-108">Summary</span></span>

 <span data-ttu-id="4d13d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="4d13d-109">Members</span></span>                        | <span data-ttu-id="4d13d-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="4d13d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4d13d-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="4d13d-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="4d13d-112">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="4d13d-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="4d13d-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="4d13d-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="4d13d-114">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="4d13d-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="4d13d-115">Estado</span><span class="sxs-lookup"><span data-stu-id="4d13d-115">State</span></span>](#state) | <span data-ttu-id="4d13d-116">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="4d13d-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="4d13d-117">Uri</span><span class="sxs-lookup"><span data-stu-id="4d13d-117">Uri</span></span>](#uri) | <span data-ttu-id="4d13d-118">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="4d13d-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="4d13d-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4d13d-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="4d13d-120">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="4d13d-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="4d13d-121">Parte</span><span class="sxs-lookup"><span data-stu-id="4d13d-121">Members</span></span>

#### <span data-ttu-id="4d13d-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="4d13d-122">IsUserInitiated</span></span> 

<span data-ttu-id="4d13d-123">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="4d13d-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="4d13d-124">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="4d13d-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="4d13d-125">Observe que a inicialização por meio de um gesto do usuário não significa que o usuário pretendia acessar o recurso associado.</span><span class="sxs-lookup"><span data-stu-id="4d13d-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="4d13d-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="4d13d-126">PermissionKind</span></span> 

<span data-ttu-id="4d13d-127">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="4d13d-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="4d13d-128">CoreWebView2PermissionKind público [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="4d13d-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="4d13d-129">Estado</span><span class="sxs-lookup"><span data-stu-id="4d13d-129">State</span></span> 

<span data-ttu-id="4d13d-130">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="4d13d-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="4d13d-131">[estado](#state) CoreWebView2PermissionState público</span><span class="sxs-lookup"><span data-stu-id="4d13d-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="4d13d-132">se a solicitação é concedida.</span><span class="sxs-lookup"><span data-stu-id="4d13d-132">whether the request is granted.</span></span>

<span data-ttu-id="4d13d-133">O valor padrão é CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="4d13d-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="4d13d-134">Uri</span><span class="sxs-lookup"><span data-stu-id="4d13d-134">Uri</span></span> 

<span data-ttu-id="4d13d-135">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="4d13d-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="4d13d-136">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="4d13d-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="4d13d-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4d13d-137">GetDeferral</span></span> 

<span data-ttu-id="4d13d-138">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="4d13d-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="4d13d-139">Public CoreWebView2Deferral [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="4d13d-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="4d13d-140">O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="4d13d-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

