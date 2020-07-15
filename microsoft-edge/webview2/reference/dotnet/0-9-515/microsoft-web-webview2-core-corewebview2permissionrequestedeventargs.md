---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 22fc8ec74c8da0a0ff072cacf91a792b9246900f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879797"
---
# <span data-ttu-id="c381c-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c381c-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="c381c-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="c381c-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="c381c-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="c381c-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="c381c-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="c381c-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="c381c-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="c381c-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="c381c-109">Args de evento para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="c381c-109">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="c381c-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="c381c-110">Summary</span></span>

 <span data-ttu-id="c381c-111">Parte</span><span class="sxs-lookup"><span data-stu-id="c381c-111">Members</span></span>                        | <span data-ttu-id="c381c-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="c381c-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c381c-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c381c-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="c381c-114">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="c381c-114">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="c381c-115">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="c381c-115">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="c381c-116">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="c381c-116">The type of the permission that is requested.</span></span>
[<span data-ttu-id="c381c-117">Estado</span><span class="sxs-lookup"><span data-stu-id="c381c-117">State</span></span>](#state) | <span data-ttu-id="c381c-118">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="c381c-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="c381c-119">Uri</span><span class="sxs-lookup"><span data-stu-id="c381c-119">Uri</span></span>](#uri) | <span data-ttu-id="c381c-120">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="c381c-120">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="c381c-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c381c-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="c381c-122">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="c381c-122">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="c381c-123">Parte</span><span class="sxs-lookup"><span data-stu-id="c381c-123">Members</span></span>

#### <span data-ttu-id="c381c-124">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c381c-124">IsUserInitiated</span></span> 

<span data-ttu-id="c381c-125">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="c381c-125">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="c381c-126">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="c381c-126">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="c381c-127">Observe que a inicialização por meio de um gesto do usuário não significa que o usuário pretendia acessar o recurso associado.</span><span class="sxs-lookup"><span data-stu-id="c381c-127">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="c381c-128">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="c381c-128">PermissionKind</span></span> 

<span data-ttu-id="c381c-129">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="c381c-129">The type of the permission that is requested.</span></span>

> <span data-ttu-id="c381c-130">CoreWebView2PermissionKind público [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="c381c-130">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="c381c-131">Estado</span><span class="sxs-lookup"><span data-stu-id="c381c-131">State</span></span> 

<span data-ttu-id="c381c-132">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="c381c-132">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="c381c-133">[estado](#state) CoreWebView2PermissionState público</span><span class="sxs-lookup"><span data-stu-id="c381c-133">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="c381c-134">se a solicitação é concedida.</span><span class="sxs-lookup"><span data-stu-id="c381c-134">whether the request is granted.</span></span>

<span data-ttu-id="c381c-135">O valor padrão é CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="c381c-135">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="c381c-136">Uri</span><span class="sxs-lookup"><span data-stu-id="c381c-136">Uri</span></span> 

<span data-ttu-id="c381c-137">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="c381c-137">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="c381c-138">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="c381c-138">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="c381c-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c381c-139">GetDeferral</span></span> 

<span data-ttu-id="c381c-140">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="c381c-140">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="c381c-141">Public CoreWebView2Deferral [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="c381c-141">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="c381c-142">O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="c381c-142">Developer can use the deferral object to make the permission decision at a later time.</span></span>

