---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 75f88a08f5a94df85a471658704fcd77a5926417
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877783"
---
# <span data-ttu-id="091e3-104">0.9.430-ICoreWebView2PermissionRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="091e3-104">0.9.430 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="091e3-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="091e3-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="091e3-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="091e3-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="091e3-107">Args de evento para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="091e3-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="091e3-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="091e3-108">Summary</span></span>

 <span data-ttu-id="091e3-109">Parte</span><span class="sxs-lookup"><span data-stu-id="091e3-109">Members</span></span>                        | <span data-ttu-id="091e3-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="091e3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="091e3-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="091e3-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="091e3-112">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="091e3-112">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="091e3-113">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="091e3-113">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="091e3-114">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="091e3-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="091e3-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="091e3-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="091e3-116">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="091e3-116">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="091e3-117">get_State</span><span class="sxs-lookup"><span data-stu-id="091e3-117">get_State</span></span>](#get_state) | <span data-ttu-id="091e3-118">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="091e3-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="091e3-119">put_State</span><span class="sxs-lookup"><span data-stu-id="091e3-119">put_State</span></span>](#put_state) | <span data-ttu-id="091e3-120">Defina a propriedade State.</span><span class="sxs-lookup"><span data-stu-id="091e3-120">Set the State property.</span></span>
[<span data-ttu-id="091e3-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="091e3-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="091e3-122">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="091e3-122">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="091e3-123">Parte</span><span class="sxs-lookup"><span data-stu-id="091e3-123">Members</span></span>

#### <span data-ttu-id="091e3-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="091e3-124">get_Uri</span></span> 

<span data-ttu-id="091e3-125">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="091e3-125">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="091e3-126">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="091e3-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="091e3-127">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="091e3-127">get_PermissionKind</span></span> 

<span data-ttu-id="091e3-128">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="091e3-128">The type of the permission that is requested.</span></span>

> <span data-ttu-id="091e3-129">[get_PermissionKind](#get_permissionkind)público HRESULT (CORE_WEBVIEW2_PERMISSION_KIND \* valor)</span><span class="sxs-lookup"><span data-stu-id="091e3-129">public HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="091e3-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="091e3-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="091e3-131">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="091e3-131">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="091e3-132">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="091e3-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="091e3-133">Observe que a inicialização por meio de um gesto do usuário não significa que o usuário pretendia acessar o recurso associado.</span><span class="sxs-lookup"><span data-stu-id="091e3-133">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="091e3-134">get_State</span><span class="sxs-lookup"><span data-stu-id="091e3-134">get_State</span></span> 

<span data-ttu-id="091e3-135">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="091e3-135">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="091e3-136">[get_State](#get_state)público HRESULT (CORE_WEBVIEW2_PERMISSION_STATE \* valor)</span><span class="sxs-lookup"><span data-stu-id="091e3-136">public HRESULT [get_State](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="091e3-137">se a solicitação é concedida.</span><span class="sxs-lookup"><span data-stu-id="091e3-137">whether the request is granted.</span></span> <span data-ttu-id="091e3-138">O valor padrão é CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="091e3-138">Default value is CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="091e3-139">put_State</span><span class="sxs-lookup"><span data-stu-id="091e3-139">put_State</span></span> 

<span data-ttu-id="091e3-140">Defina a propriedade State.</span><span class="sxs-lookup"><span data-stu-id="091e3-140">Set the State property.</span></span>

> <span data-ttu-id="091e3-141">público HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE valor)</span><span class="sxs-lookup"><span data-stu-id="091e3-141">public HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="091e3-142">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="091e3-142">GetDeferral</span></span> 

<span data-ttu-id="091e3-143">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="091e3-143">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="091e3-144">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="091e3-144">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="091e3-145">O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="091e3-145">Developer can use the deferral object to make the permission decision at a later time.</span></span>

