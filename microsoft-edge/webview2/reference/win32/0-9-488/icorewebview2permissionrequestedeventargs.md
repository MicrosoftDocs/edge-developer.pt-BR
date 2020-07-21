---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 85cba958c5c918bb99f14cb7202c7645b0ae6c52
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885202"
---
# <span data-ttu-id="bfb95-104">0.9.515-ICoreWebView2PermissionRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="bfb95-104">0.9.515 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="bfb95-105">Args de evento para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="bfb95-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="bfb95-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="bfb95-106">Summary</span></span>

 <span data-ttu-id="bfb95-107">Parte</span><span class="sxs-lookup"><span data-stu-id="bfb95-107">Members</span></span>                        | <span data-ttu-id="bfb95-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="bfb95-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bfb95-109">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="bfb95-109">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="bfb95-110">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="bfb95-110">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="bfb95-111">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="bfb95-111">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="bfb95-112">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="bfb95-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="bfb95-113">get_State</span><span class="sxs-lookup"><span data-stu-id="bfb95-113">get_State</span></span>](#get_state) | <span data-ttu-id="bfb95-114">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="bfb95-114">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="bfb95-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="bfb95-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="bfb95-116">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="bfb95-116">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="bfb95-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="bfb95-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="bfb95-118">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="bfb95-118">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="bfb95-119">put_State</span><span class="sxs-lookup"><span data-stu-id="bfb95-119">put_State</span></span>](#put_state) | <span data-ttu-id="bfb95-120">Defina a propriedade State.</span><span class="sxs-lookup"><span data-stu-id="bfb95-120">Set the State property.</span></span>

## <span data-ttu-id="bfb95-121">Parte</span><span class="sxs-lookup"><span data-stu-id="bfb95-121">Members</span></span>

#### <span data-ttu-id="bfb95-122">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="bfb95-122">get_IsUserInitiated</span></span> 

<span data-ttu-id="bfb95-123">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="bfb95-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="bfb95-124">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="bfb95-124">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="bfb95-125">Observe que a inicialização por meio de um gesto do usuário não significa que o usuário pretendia acessar o recurso associado.</span><span class="sxs-lookup"><span data-stu-id="bfb95-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="bfb95-126">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="bfb95-126">get_PermissionKind</span></span> 

<span data-ttu-id="bfb95-127">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="bfb95-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="bfb95-128">[get_PermissionKind](#get_permissionkind)público HRESULT (COREWEBVIEW2_PERMISSION_KIND \* valor)</span><span class="sxs-lookup"><span data-stu-id="bfb95-128">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="bfb95-129">get_State</span><span class="sxs-lookup"><span data-stu-id="bfb95-129">get_State</span></span> 

<span data-ttu-id="bfb95-130">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="bfb95-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="bfb95-131">[get_State](#get_state)público HRESULT (COREWEBVIEW2_PERMISSION_STATE \* valor)</span><span class="sxs-lookup"><span data-stu-id="bfb95-131">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="bfb95-132">se a solicitação é concedida.</span><span class="sxs-lookup"><span data-stu-id="bfb95-132">whether the request is granted.</span></span> <span data-ttu-id="bfb95-133">O valor padrão é COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="bfb95-133">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="bfb95-134">get_Uri</span><span class="sxs-lookup"><span data-stu-id="bfb95-134">get_Uri</span></span> 

<span data-ttu-id="bfb95-135">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="bfb95-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="bfb95-136">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="bfb95-136">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="bfb95-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="bfb95-137">GetDeferral</span></span> 

<span data-ttu-id="bfb95-138">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="bfb95-138">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="bfb95-139">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="bfb95-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="bfb95-140">O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="bfb95-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="bfb95-141">put_State</span><span class="sxs-lookup"><span data-stu-id="bfb95-141">put_State</span></span> 

<span data-ttu-id="bfb95-142">Defina a propriedade State.</span><span class="sxs-lookup"><span data-stu-id="bfb95-142">Set the State property.</span></span>

> <span data-ttu-id="bfb95-143">público HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE valor)</span><span class="sxs-lookup"><span data-stu-id="bfb95-143">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE value)</span></span>

