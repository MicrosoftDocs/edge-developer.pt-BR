---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 3d88d4ee0a89b4690b47f67ee90756ebecdd1c78
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698187"
---
# <span data-ttu-id="b1785-104">interface ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b1785-104">interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="b1785-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="b1785-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="b1785-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="b1785-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="b1785-107">Args de evento para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="b1785-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="b1785-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="b1785-108">Summary</span></span>

 <span data-ttu-id="b1785-109">Parte</span><span class="sxs-lookup"><span data-stu-id="b1785-109">Members</span></span>                        | <span data-ttu-id="b1785-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="b1785-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b1785-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="b1785-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="b1785-112">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="b1785-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="b1785-113">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="b1785-113">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="b1785-114">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="b1785-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="b1785-115">get_State</span><span class="sxs-lookup"><span data-stu-id="b1785-115">get_State</span></span>](#get_state) | <span data-ttu-id="b1785-116">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="b1785-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="b1785-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b1785-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="b1785-118">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="b1785-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="b1785-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b1785-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="b1785-120">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="b1785-120">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="b1785-121">put_State</span><span class="sxs-lookup"><span data-stu-id="b1785-121">put_State</span></span>](#put_state) | <span data-ttu-id="b1785-122">Defina a propriedade State.</span><span class="sxs-lookup"><span data-stu-id="b1785-122">Set the State property.</span></span>

## <span data-ttu-id="b1785-123">Parte</span><span class="sxs-lookup"><span data-stu-id="b1785-123">Members</span></span>

#### <span data-ttu-id="b1785-124">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="b1785-124">get_IsUserInitiated</span></span> 

<span data-ttu-id="b1785-125">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="b1785-125">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="b1785-126">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="b1785-126">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="b1785-127">Observe que a inicialização por meio de um gesto do usuário não significa que o usuário pretendia acessar o recurso associado.</span><span class="sxs-lookup"><span data-stu-id="b1785-127">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="b1785-128">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="b1785-128">get_PermissionKind</span></span> 

<span data-ttu-id="b1785-129">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="b1785-129">The type of the permission that is requested.</span></span>

> <span data-ttu-id="b1785-130">[get_PermissionKind](#get_permissionkind)público HRESULT (COREWEBVIEW2_PERMISSION_KIND \* valor)</span><span class="sxs-lookup"><span data-stu-id="b1785-130">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="b1785-131">get_State</span><span class="sxs-lookup"><span data-stu-id="b1785-131">get_State</span></span> 

<span data-ttu-id="b1785-132">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="b1785-132">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="b1785-133">[get_State](#get_state)público HRESULT (COREWEBVIEW2_PERMISSION_STATE \* valor)</span><span class="sxs-lookup"><span data-stu-id="b1785-133">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="b1785-134">se a solicitação é concedida.</span><span class="sxs-lookup"><span data-stu-id="b1785-134">whether the request is granted.</span></span> <span data-ttu-id="b1785-135">O valor padrão é COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="b1785-135">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="b1785-136">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b1785-136">get_Uri</span></span> 

<span data-ttu-id="b1785-137">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="b1785-137">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="b1785-138">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="b1785-138">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="b1785-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b1785-139">GetDeferral</span></span> 

<span data-ttu-id="b1785-140">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="b1785-140">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="b1785-141">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="b1785-141">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="b1785-142">O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="b1785-142">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="b1785-143">put_State</span><span class="sxs-lookup"><span data-stu-id="b1785-143">put_State</span></span> 

<span data-ttu-id="b1785-144">Defina a propriedade State.</span><span class="sxs-lookup"><span data-stu-id="b1785-144">Set the State property.</span></span>

> <span data-ttu-id="b1785-145">público HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE valor)</span><span class="sxs-lookup"><span data-stu-id="b1785-145">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE value)</span></span>

