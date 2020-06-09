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
ms.openlocfilehash: 743cd0fc6a1a9b21605dfa427273a7a457f806d7
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697606"
---
# <span data-ttu-id="d920d-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d920d-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="d920d-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="d920d-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="d920d-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="d920d-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="d920d-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="d920d-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="d920d-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="d920d-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="d920d-109">Args de evento para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="d920d-109">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="d920d-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="d920d-110">Summary</span></span>

 <span data-ttu-id="d920d-111">Parte</span><span class="sxs-lookup"><span data-stu-id="d920d-111">Members</span></span>                        | <span data-ttu-id="d920d-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="d920d-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d920d-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="d920d-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="d920d-114">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="d920d-114">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="d920d-115">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="d920d-115">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="d920d-116">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="d920d-116">The type of the permission that is requested.</span></span>
[<span data-ttu-id="d920d-117">Estado</span><span class="sxs-lookup"><span data-stu-id="d920d-117">State</span></span>](#state) | <span data-ttu-id="d920d-118">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="d920d-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="d920d-119">Uri</span><span class="sxs-lookup"><span data-stu-id="d920d-119">Uri</span></span>](#uri) | <span data-ttu-id="d920d-120">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="d920d-120">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="d920d-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d920d-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="d920d-122">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="d920d-122">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="d920d-123">Parte</span><span class="sxs-lookup"><span data-stu-id="d920d-123">Members</span></span>

#### <span data-ttu-id="d920d-124">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="d920d-124">IsUserInitiated</span></span> 

<span data-ttu-id="d920d-125">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="d920d-125">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="d920d-126">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="d920d-126">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="d920d-127">Observe que a inicialização por meio de um gesto do usuário não significa que o usuário pretendia acessar o recurso associado.</span><span class="sxs-lookup"><span data-stu-id="d920d-127">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="d920d-128">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="d920d-128">PermissionKind</span></span> 

<span data-ttu-id="d920d-129">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="d920d-129">The type of the permission that is requested.</span></span>

> <span data-ttu-id="d920d-130">CoreWebView2PermissionKind público [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="d920d-130">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="d920d-131">Estado</span><span class="sxs-lookup"><span data-stu-id="d920d-131">State</span></span> 

<span data-ttu-id="d920d-132">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="d920d-132">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="d920d-133">[estado](#state) CoreWebView2PermissionState público</span><span class="sxs-lookup"><span data-stu-id="d920d-133">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="d920d-134">se a solicitação é concedida.</span><span class="sxs-lookup"><span data-stu-id="d920d-134">whether the request is granted.</span></span>

<span data-ttu-id="d920d-135">O valor padrão é CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="d920d-135">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="d920d-136">Uri</span><span class="sxs-lookup"><span data-stu-id="d920d-136">Uri</span></span> 

<span data-ttu-id="d920d-137">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="d920d-137">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="d920d-138">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="d920d-138">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="d920d-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d920d-139">GetDeferral</span></span> 

<span data-ttu-id="d920d-140">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="d920d-140">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="d920d-141">Public CoreWebView2Deferral [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="d920d-141">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="d920d-142">O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="d920d-142">Developer can use the deferral object to make the permission decision at a later time.</span></span>

