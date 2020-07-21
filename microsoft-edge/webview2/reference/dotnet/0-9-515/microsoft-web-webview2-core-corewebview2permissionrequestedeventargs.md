---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 2bfa4559824c9bb397648249ead8fa8cb60c281c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884628"
---
# <span data-ttu-id="d91a9-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d91a9-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="d91a9-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="d91a9-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="d91a9-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="d91a9-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="d91a9-107">Args de evento para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="d91a9-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="d91a9-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="d91a9-108">Summary</span></span>

 <span data-ttu-id="d91a9-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d91a9-109">Members</span></span>                        | <span data-ttu-id="d91a9-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="d91a9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d91a9-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="d91a9-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="d91a9-112">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="d91a9-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="d91a9-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="d91a9-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="d91a9-114">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="d91a9-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="d91a9-115">Estado</span><span class="sxs-lookup"><span data-stu-id="d91a9-115">State</span></span>](#state) | <span data-ttu-id="d91a9-116">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="d91a9-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="d91a9-117">Uri</span><span class="sxs-lookup"><span data-stu-id="d91a9-117">Uri</span></span>](#uri) | <span data-ttu-id="d91a9-118">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="d91a9-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="d91a9-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d91a9-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="d91a9-120">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="d91a9-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="d91a9-121">Parte</span><span class="sxs-lookup"><span data-stu-id="d91a9-121">Members</span></span>

#### <span data-ttu-id="d91a9-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="d91a9-122">IsUserInitiated</span></span> 

<span data-ttu-id="d91a9-123">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="d91a9-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="d91a9-124">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="d91a9-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="d91a9-125">Observe que a inicialização por meio de um gesto do usuário não significa que o usuário pretendia acessar o recurso associado.</span><span class="sxs-lookup"><span data-stu-id="d91a9-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="d91a9-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="d91a9-126">PermissionKind</span></span> 

<span data-ttu-id="d91a9-127">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="d91a9-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="d91a9-128">CoreWebView2PermissionKind público [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="d91a9-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="d91a9-129">Estado</span><span class="sxs-lookup"><span data-stu-id="d91a9-129">State</span></span> 

<span data-ttu-id="d91a9-130">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="d91a9-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="d91a9-131">[estado](#state) CoreWebView2PermissionState público</span><span class="sxs-lookup"><span data-stu-id="d91a9-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="d91a9-132">se a solicitação é concedida.</span><span class="sxs-lookup"><span data-stu-id="d91a9-132">whether the request is granted.</span></span>

<span data-ttu-id="d91a9-133">O valor padrão é CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="d91a9-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="d91a9-134">Uri</span><span class="sxs-lookup"><span data-stu-id="d91a9-134">Uri</span></span> 

<span data-ttu-id="d91a9-135">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="d91a9-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="d91a9-136">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="d91a9-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="d91a9-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d91a9-137">GetDeferral</span></span> 

<span data-ttu-id="d91a9-138">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="d91a9-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="d91a9-139">Public CoreWebView2Deferral [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="d91a9-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="d91a9-140">O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="d91a9-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

