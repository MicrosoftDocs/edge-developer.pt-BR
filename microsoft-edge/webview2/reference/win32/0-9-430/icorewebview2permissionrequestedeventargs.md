---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: e29765a4b8a3e620b8c627c7b05b9f0b4ff63f95
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886408"
---
# <span data-ttu-id="666e0-104">0.9.430-ICoreWebView2PermissionRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="666e0-104">0.9.430 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="666e0-105">Args de evento para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="666e0-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="666e0-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="666e0-106">Summary</span></span>

 <span data-ttu-id="666e0-107">Parte</span><span class="sxs-lookup"><span data-stu-id="666e0-107">Members</span></span>                        | <span data-ttu-id="666e0-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="666e0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="666e0-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="666e0-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="666e0-110">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="666e0-110">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="666e0-111">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="666e0-111">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="666e0-112">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="666e0-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="666e0-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="666e0-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="666e0-114">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="666e0-114">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="666e0-115">get_State</span><span class="sxs-lookup"><span data-stu-id="666e0-115">get_State</span></span>](#get_state) | <span data-ttu-id="666e0-116">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="666e0-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="666e0-117">put_State</span><span class="sxs-lookup"><span data-stu-id="666e0-117">put_State</span></span>](#put_state) | <span data-ttu-id="666e0-118">Defina a propriedade State.</span><span class="sxs-lookup"><span data-stu-id="666e0-118">Set the State property.</span></span>
[<span data-ttu-id="666e0-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="666e0-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="666e0-120">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="666e0-120">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="666e0-121">Parte</span><span class="sxs-lookup"><span data-stu-id="666e0-121">Members</span></span>

#### <span data-ttu-id="666e0-122">get_Uri</span><span class="sxs-lookup"><span data-stu-id="666e0-122">get_Uri</span></span> 

<span data-ttu-id="666e0-123">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="666e0-123">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="666e0-124">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="666e0-124">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="666e0-125">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="666e0-125">get_PermissionKind</span></span> 

<span data-ttu-id="666e0-126">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="666e0-126">The type of the permission that is requested.</span></span>

> <span data-ttu-id="666e0-127">[get_PermissionKind](#get_permissionkind)público HRESULT (CORE_WEBVIEW2_PERMISSION_KIND \* valor)</span><span class="sxs-lookup"><span data-stu-id="666e0-127">public HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="666e0-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="666e0-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="666e0-129">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="666e0-129">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="666e0-130">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="666e0-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="666e0-131">Observe que a inicialização por meio de um gesto do usuário não significa que o usuário pretendia acessar o recurso associado.</span><span class="sxs-lookup"><span data-stu-id="666e0-131">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="666e0-132">get_State</span><span class="sxs-lookup"><span data-stu-id="666e0-132">get_State</span></span> 

<span data-ttu-id="666e0-133">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="666e0-133">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="666e0-134">[get_State](#get_state)público HRESULT (CORE_WEBVIEW2_PERMISSION_STATE \* valor)</span><span class="sxs-lookup"><span data-stu-id="666e0-134">public HRESULT [get_State](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="666e0-135">se a solicitação é concedida.</span><span class="sxs-lookup"><span data-stu-id="666e0-135">whether the request is granted.</span></span> <span data-ttu-id="666e0-136">O valor padrão é CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="666e0-136">Default value is CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="666e0-137">put_State</span><span class="sxs-lookup"><span data-stu-id="666e0-137">put_State</span></span> 

<span data-ttu-id="666e0-138">Defina a propriedade State.</span><span class="sxs-lookup"><span data-stu-id="666e0-138">Set the State property.</span></span>

> <span data-ttu-id="666e0-139">público HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE valor)</span><span class="sxs-lookup"><span data-stu-id="666e0-139">public HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="666e0-140">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="666e0-140">GetDeferral</span></span> 

<span data-ttu-id="666e0-141">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="666e0-141">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="666e0-142">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="666e0-142">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="666e0-143">O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="666e0-143">Developer can use the deferral object to make the permission decision at a later time.</span></span>

