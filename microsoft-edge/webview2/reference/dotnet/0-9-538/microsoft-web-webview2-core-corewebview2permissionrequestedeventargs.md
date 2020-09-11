---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: 2ad85879ccf69ccecef355ea07d311cc5a23de11
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010926"
---
# <span data-ttu-id="0bfda-104">classe 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="0bfda-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="0bfda-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="0bfda-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="0bfda-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="0bfda-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="0bfda-107">Args de evento para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="0bfda-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="0bfda-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="0bfda-108">Summary</span></span>

 <span data-ttu-id="0bfda-109">Parte</span><span class="sxs-lookup"><span data-stu-id="0bfda-109">Members</span></span>                        | <span data-ttu-id="0bfda-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="0bfda-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0bfda-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="0bfda-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="0bfda-112">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="0bfda-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="0bfda-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="0bfda-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="0bfda-114">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="0bfda-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="0bfda-115">Estado</span><span class="sxs-lookup"><span data-stu-id="0bfda-115">State</span></span>](#state) | <span data-ttu-id="0bfda-116">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="0bfda-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="0bfda-117">Uri</span><span class="sxs-lookup"><span data-stu-id="0bfda-117">Uri</span></span>](#uri) | <span data-ttu-id="0bfda-118">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="0bfda-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="0bfda-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="0bfda-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="0bfda-120">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="0bfda-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="0bfda-121">Parte</span><span class="sxs-lookup"><span data-stu-id="0bfda-121">Members</span></span>

#### <span data-ttu-id="0bfda-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="0bfda-122">IsUserInitiated</span></span> 

<span data-ttu-id="0bfda-123">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="0bfda-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="0bfda-124">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="0bfda-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="0bfda-125">Observe que a inicialização por meio de um gesto do usuário não significa que o usuário pretendia acessar o recurso associado.</span><span class="sxs-lookup"><span data-stu-id="0bfda-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="0bfda-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="0bfda-126">PermissionKind</span></span> 

<span data-ttu-id="0bfda-127">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="0bfda-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="0bfda-128">CoreWebView2PermissionKind público [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="0bfda-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="0bfda-129">Estado</span><span class="sxs-lookup"><span data-stu-id="0bfda-129">State</span></span> 

<span data-ttu-id="0bfda-130">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="0bfda-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="0bfda-131">[estado](#state) CoreWebView2PermissionState público</span><span class="sxs-lookup"><span data-stu-id="0bfda-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="0bfda-132">se a solicitação é concedida.</span><span class="sxs-lookup"><span data-stu-id="0bfda-132">whether the request is granted.</span></span>

<span data-ttu-id="0bfda-133">O valor padrão é CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="0bfda-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="0bfda-134">Uri</span><span class="sxs-lookup"><span data-stu-id="0bfda-134">Uri</span></span> 

<span data-ttu-id="0bfda-135">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="0bfda-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="0bfda-136">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="0bfda-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="0bfda-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="0bfda-137">GetDeferral</span></span> 

<span data-ttu-id="0bfda-138">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="0bfda-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="0bfda-139">Public CoreWebView2Deferral [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="0bfda-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="0bfda-140">O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="0bfda-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

