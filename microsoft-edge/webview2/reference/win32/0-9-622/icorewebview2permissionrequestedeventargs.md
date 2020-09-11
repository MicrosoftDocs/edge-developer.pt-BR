---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: 18048222a9d6bf4d3ad80346a41e4ef5950ca0e6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011586"
---
# <span data-ttu-id="bddab-104">interface ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="bddab-104">interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="bddab-105">Args de evento para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="bddab-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="bddab-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="bddab-106">Summary</span></span>

 <span data-ttu-id="bddab-107">Parte</span><span class="sxs-lookup"><span data-stu-id="bddab-107">Members</span></span>                        | <span data-ttu-id="bddab-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="bddab-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bddab-109">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="bddab-109">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="bddab-110">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="bddab-110">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="bddab-111">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="bddab-111">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="bddab-112">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="bddab-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="bddab-113">get_State</span><span class="sxs-lookup"><span data-stu-id="bddab-113">get_State</span></span>](#get_state) | <span data-ttu-id="bddab-114">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="bddab-114">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="bddab-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="bddab-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="bddab-116">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="bddab-116">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="bddab-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="bddab-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="bddab-118">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="bddab-118">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="bddab-119">put_State</span><span class="sxs-lookup"><span data-stu-id="bddab-119">put_State</span></span>](#put_state) | <span data-ttu-id="bddab-120">Defina a propriedade State.</span><span class="sxs-lookup"><span data-stu-id="bddab-120">Set the State property.</span></span>

## <span data-ttu-id="bddab-121">Parte</span><span class="sxs-lookup"><span data-stu-id="bddab-121">Members</span></span>

#### <span data-ttu-id="bddab-122">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="bddab-122">get_IsUserInitiated</span></span> 

<span data-ttu-id="bddab-123">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="bddab-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="bddab-124">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="bddab-124">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="bddab-125">Observe que a inicialização por meio de um gesto do usuário não significa que o usuário pretendia acessar o recurso associado.</span><span class="sxs-lookup"><span data-stu-id="bddab-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="bddab-126">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="bddab-126">get_PermissionKind</span></span> 

<span data-ttu-id="bddab-127">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="bddab-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="bddab-128">público HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* PermissionKind)</span><span class="sxs-lookup"><span data-stu-id="bddab-128">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* permissionKind)</span></span>

#### <span data-ttu-id="bddab-129">get_State</span><span class="sxs-lookup"><span data-stu-id="bddab-129">get_State</span></span> 

<span data-ttu-id="bddab-130">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="bddab-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="bddab-131">público HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* estado)</span><span class="sxs-lookup"><span data-stu-id="bddab-131">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* state)</span></span>

<span data-ttu-id="bddab-132">se a solicitação é concedida.</span><span class="sxs-lookup"><span data-stu-id="bddab-132">whether the request is granted.</span></span> <span data-ttu-id="bddab-133">O valor padrão é COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="bddab-133">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="bddab-134">get_Uri</span><span class="sxs-lookup"><span data-stu-id="bddab-134">get_Uri</span></span> 

<span data-ttu-id="bddab-135">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="bddab-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="bddab-136">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="bddab-136">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="bddab-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="bddab-137">GetDeferral</span></span> 

<span data-ttu-id="bddab-138">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="bddab-138">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="bddab-139">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="bddab-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="bddab-140">O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="bddab-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="bddab-141">put_State</span><span class="sxs-lookup"><span data-stu-id="bddab-141">put_State</span></span> 

<span data-ttu-id="bddab-142">Defina a propriedade State.</span><span class="sxs-lookup"><span data-stu-id="bddab-142">Set the State property.</span></span>

> <span data-ttu-id="bddab-143">[put_State](#put_state)público HRESULT (COREWEBVIEW2_PERMISSION_STATE estado)</span><span class="sxs-lookup"><span data-stu-id="bddab-143">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE state)</span></span>

