---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: 87993559d4d70daef84cbd86a2305f09cc017aa9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011477"
---
# <span data-ttu-id="1f2a8-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1f2a8-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

<span data-ttu-id="1f2a8-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="1f2a8-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="1f2a8-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="1f2a8-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="1f2a8-107">Args de evento para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="1f2a8-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="1f2a8-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="1f2a8-108">Summary</span></span>

 <span data-ttu-id="1f2a8-109">Parte</span><span class="sxs-lookup"><span data-stu-id="1f2a8-109">Members</span></span>                        | <span data-ttu-id="1f2a8-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="1f2a8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1f2a8-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="1f2a8-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="1f2a8-112">Verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, como clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="1f2a8-112">True when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="1f2a8-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="1f2a8-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="1f2a8-114">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="1f2a8-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="1f2a8-115">Estado</span><span class="sxs-lookup"><span data-stu-id="1f2a8-115">State</span></span>](#state) | <span data-ttu-id="1f2a8-116">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="1f2a8-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="1f2a8-117">Uri</span><span class="sxs-lookup"><span data-stu-id="1f2a8-117">Uri</span></span>](#uri) | <span data-ttu-id="1f2a8-118">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="1f2a8-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="1f2a8-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="1f2a8-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="1f2a8-120">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="1f2a8-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="1f2a8-121">Parte</span><span class="sxs-lookup"><span data-stu-id="1f2a8-121">Members</span></span>

#### <span data-ttu-id="1f2a8-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="1f2a8-122">IsUserInitiated</span></span> 

<span data-ttu-id="1f2a8-123">Verdadeiro quando a nova solicitação de janela foi iniciada por meio de um gesto do usuário, como clicar em uma marca de âncora com destino.</span><span class="sxs-lookup"><span data-stu-id="1f2a8-123">True when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="1f2a8-124">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="1f2a8-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="1f2a8-125">O bloqueador de borda pop-up está desabilitado para WebView para que o aplicativo possa usar esse sinalizador para bloquear pop-ups que não sejam iniciados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="1f2a8-125">The Edge popup blocker is disabled for WebView so the app can use this flag to block non-user initiated popups.</span></span>

#### <span data-ttu-id="1f2a8-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="1f2a8-126">PermissionKind</span></span> 

<span data-ttu-id="1f2a8-127">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="1f2a8-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="1f2a8-128">CoreWebView2PermissionKind público [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="1f2a8-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="1f2a8-129">Estado</span><span class="sxs-lookup"><span data-stu-id="1f2a8-129">State</span></span> 

<span data-ttu-id="1f2a8-130">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="1f2a8-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="1f2a8-131">[estado](#state) CoreWebView2PermissionState público</span><span class="sxs-lookup"><span data-stu-id="1f2a8-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="1f2a8-132">se a solicitação é concedida.</span><span class="sxs-lookup"><span data-stu-id="1f2a8-132">whether the request is granted.</span></span>

<span data-ttu-id="1f2a8-133">O valor padrão é CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="1f2a8-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="1f2a8-134">Uri</span><span class="sxs-lookup"><span data-stu-id="1f2a8-134">Uri</span></span> 

<span data-ttu-id="1f2a8-135">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="1f2a8-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="1f2a8-136">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="1f2a8-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="1f2a8-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="1f2a8-137">GetDeferral</span></span> 

<span data-ttu-id="1f2a8-138">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="1f2a8-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="1f2a8-139">Public CoreWebView2Deferral [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="1f2a8-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="1f2a8-140">O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="1f2a8-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

