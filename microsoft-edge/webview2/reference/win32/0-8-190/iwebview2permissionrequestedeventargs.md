---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: e2a9486011d5ef3ef480271ed32a7c8b586cf9bd
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885825"
---
# <span data-ttu-id="dc91e-104">0.8.355-IWebView2PermissionRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="dc91e-104">0.8.355 - interface IWebView2PermissionRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="dc91e-105">Args de evento para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="dc91e-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="dc91e-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="dc91e-106">Summary</span></span>

 <span data-ttu-id="dc91e-107">Parte</span><span class="sxs-lookup"><span data-stu-id="dc91e-107">Members</span></span>                        | <span data-ttu-id="dc91e-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="dc91e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dc91e-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="dc91e-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="dc91e-110">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="dc91e-110">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="dc91e-111">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="dc91e-111">get_PermissionType</span></span>](#get_permissiontype) | <span data-ttu-id="dc91e-112">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="dc91e-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="dc91e-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="dc91e-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="dc91e-114">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc91e-114">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="dc91e-115">get_State</span><span class="sxs-lookup"><span data-stu-id="dc91e-115">get_State</span></span>](#get_state) | <span data-ttu-id="dc91e-116">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="dc91e-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="dc91e-117">put_State</span><span class="sxs-lookup"><span data-stu-id="dc91e-117">put_State</span></span>](#put_state) | <span data-ttu-id="dc91e-118">Defina a propriedade State.</span><span class="sxs-lookup"><span data-stu-id="dc91e-118">Set the State property.</span></span>
[<span data-ttu-id="dc91e-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="dc91e-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="dc91e-120">Getadiamento pode ser chamado para retornar um objeto [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="dc91e-120">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="dc91e-121">Parte</span><span class="sxs-lookup"><span data-stu-id="dc91e-121">Members</span></span>

#### <span data-ttu-id="dc91e-122">get_Uri</span><span class="sxs-lookup"><span data-stu-id="dc91e-122">get_Uri</span></span> 

<span data-ttu-id="dc91e-123">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="dc91e-123">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="dc91e-124">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="dc91e-124">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="dc91e-125">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="dc91e-125">get_PermissionType</span></span> 

<span data-ttu-id="dc91e-126">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="dc91e-126">The type of the permission that is requested.</span></span>

> <span data-ttu-id="dc91e-127">[get_PermissionType](#get_permissiontype)público HRESULT (WEBVIEW2_PERMISSION_TYPE \* valor)</span><span class="sxs-lookup"><span data-stu-id="dc91e-127">public HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE \* value)</span></span>

#### <span data-ttu-id="dc91e-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="dc91e-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="dc91e-129">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc91e-129">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="dc91e-130">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="dc91e-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="dc91e-131">Observe que a inicialização por meio de um gesto do usuário não significa que o usuário pretendia acessar o recurso associado.</span><span class="sxs-lookup"><span data-stu-id="dc91e-131">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="dc91e-132">get_State</span><span class="sxs-lookup"><span data-stu-id="dc91e-132">get_State</span></span> 

<span data-ttu-id="dc91e-133">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="dc91e-133">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="dc91e-134">[get_State](#get_state)público HRESULT (WEBVIEW2_PERMISSION_STATE \* valor)</span><span class="sxs-lookup"><span data-stu-id="dc91e-134">public HRESULT [get_State](#get_state)(WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="dc91e-135">se a solicitação é concedida.</span><span class="sxs-lookup"><span data-stu-id="dc91e-135">whether the request is granted.</span></span> <span data-ttu-id="dc91e-136">O valor padrão é WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="dc91e-136">Default value is WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="dc91e-137">put_State</span><span class="sxs-lookup"><span data-stu-id="dc91e-137">put_State</span></span> 

<span data-ttu-id="dc91e-138">Defina a propriedade State.</span><span class="sxs-lookup"><span data-stu-id="dc91e-138">Set the State property.</span></span>

> <span data-ttu-id="dc91e-139">público HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE valor)</span><span class="sxs-lookup"><span data-stu-id="dc91e-139">public HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="dc91e-140">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="dc91e-140">GetDeferral</span></span> 

<span data-ttu-id="dc91e-141">Getadiamento pode ser chamado para retornar um objeto [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="dc91e-141">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="dc91e-142">público HRESULT [getadiamento](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="dc91e-142">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="dc91e-143">O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="dc91e-143">Developer can use the deferral object to make the permission decision at a later time.</span></span>

