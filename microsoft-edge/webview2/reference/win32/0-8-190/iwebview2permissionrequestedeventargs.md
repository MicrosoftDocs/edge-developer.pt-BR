---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 9d16f1c72a3921b220bd0046e78ed0c6b32a718a
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652571"
---
# <span data-ttu-id="19e52-104">interface IWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="19e52-104">interface IWebView2PermissionRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="19e52-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="19e52-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="19e52-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="19e52-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="19e52-107">Args de evento para o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="19e52-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="19e52-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="19e52-108">Summary</span></span>

 <span data-ttu-id="19e52-109">Parte</span><span class="sxs-lookup"><span data-stu-id="19e52-109">Members</span></span>                        | <span data-ttu-id="19e52-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="19e52-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="19e52-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="19e52-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="19e52-112">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="19e52-112">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="19e52-113">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="19e52-113">get_PermissionType</span></span>](#get_permissiontype) | <span data-ttu-id="19e52-114">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="19e52-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="19e52-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="19e52-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="19e52-116">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="19e52-116">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="19e52-117">get_State</span><span class="sxs-lookup"><span data-stu-id="19e52-117">get_State</span></span>](#get_state) | <span data-ttu-id="19e52-118">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="19e52-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="19e52-119">put_State</span><span class="sxs-lookup"><span data-stu-id="19e52-119">put_State</span></span>](#put_state) | <span data-ttu-id="19e52-120">Defina a propriedade State.</span><span class="sxs-lookup"><span data-stu-id="19e52-120">Set the State property.</span></span>
[<span data-ttu-id="19e52-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="19e52-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="19e52-122">Getadiamento pode ser chamado para retornar um objeto [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="19e52-122">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="19e52-123">Parte</span><span class="sxs-lookup"><span data-stu-id="19e52-123">Members</span></span>

#### <span data-ttu-id="19e52-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="19e52-124">get_Uri</span></span> 

<span data-ttu-id="19e52-125">A origem do conteúdo da Web que solicita a permissão.</span><span class="sxs-lookup"><span data-stu-id="19e52-125">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="19e52-126">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="19e52-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="19e52-127">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="19e52-127">get_PermissionType</span></span> 

<span data-ttu-id="19e52-128">O tipo da permissão que é solicitada.</span><span class="sxs-lookup"><span data-stu-id="19e52-128">The type of the permission that is requested.</span></span>

> <span data-ttu-id="19e52-129">[get_PermissionType](#get_permissiontype)público HRESULT (WEBVIEW2_PERMISSION_TYPE \* valor)</span><span class="sxs-lookup"><span data-stu-id="19e52-129">public HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE \* value)</span></span>

#### <span data-ttu-id="19e52-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="19e52-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="19e52-131">Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.</span><span class="sxs-lookup"><span data-stu-id="19e52-131">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="19e52-132">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="19e52-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="19e52-133">Observe que a inicialização por meio de um gesto do usuário não significa que o usuário pretendia acessar o recurso associado.</span><span class="sxs-lookup"><span data-stu-id="19e52-133">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="19e52-134">get_State</span><span class="sxs-lookup"><span data-stu-id="19e52-134">get_State</span></span> 

<span data-ttu-id="19e52-135">O status de uma solicitação de permissão, ou seja,</span><span class="sxs-lookup"><span data-stu-id="19e52-135">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="19e52-136">[get_State](#get_state)público HRESULT (WEBVIEW2_PERMISSION_STATE \* valor)</span><span class="sxs-lookup"><span data-stu-id="19e52-136">public HRESULT [get_State](#get_state)(WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="19e52-137">se a solicitação é concedida.</span><span class="sxs-lookup"><span data-stu-id="19e52-137">whether the request is granted.</span></span> <span data-ttu-id="19e52-138">O valor padrão é WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="19e52-138">Default value is WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="19e52-139">put_State</span><span class="sxs-lookup"><span data-stu-id="19e52-139">put_State</span></span> 

<span data-ttu-id="19e52-140">Defina a propriedade State.</span><span class="sxs-lookup"><span data-stu-id="19e52-140">Set the State property.</span></span>

> <span data-ttu-id="19e52-141">público HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE valor)</span><span class="sxs-lookup"><span data-stu-id="19e52-141">public HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="19e52-142">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="19e52-142">GetDeferral</span></span> 

<span data-ttu-id="19e52-143">Getadiamento pode ser chamado para retornar um objeto [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="19e52-143">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="19e52-144">público HRESULT [getadiamento](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="19e52-144">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="19e52-145">O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="19e52-145">Developer can use the deferral object to make the permission decision at a later time.</span></span>

