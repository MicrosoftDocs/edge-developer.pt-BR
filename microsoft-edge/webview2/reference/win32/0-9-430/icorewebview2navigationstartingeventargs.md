---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: c2ac2e499e6bbd49f411a001e061af72fda524b5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877879"
---
# <span data-ttu-id="6cc0a-104">0.9.430-ICoreWebView2NavigationStartingEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="6cc0a-104">0.9.430 - interface ICoreWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="6cc0a-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="6cc0a-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="6cc0a-107">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="6cc0a-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="6cc0a-108">Summary</span></span>

 <span data-ttu-id="6cc0a-109">Parte</span><span class="sxs-lookup"><span data-stu-id="6cc0a-109">Members</span></span>                        | <span data-ttu-id="6cc0a-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="6cc0a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6cc0a-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="6cc0a-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="6cc0a-112">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-112">The uri of the requested navigation.</span></span>
[<span data-ttu-id="6cc0a-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6cc0a-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="6cc0a-114">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="6cc0a-115">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="6cc0a-115">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="6cc0a-116">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="6cc0a-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="6cc0a-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="6cc0a-118">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="6cc0a-119">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="6cc0a-119">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="6cc0a-120">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-120">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="6cc0a-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="6cc0a-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="6cc0a-122">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-122">Set the Cancel property.</span></span>
[<span data-ttu-id="6cc0a-123">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="6cc0a-123">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="6cc0a-124">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-124">The ID of the navigation.</span></span>

## <span data-ttu-id="6cc0a-125">Parte</span><span class="sxs-lookup"><span data-stu-id="6cc0a-125">Members</span></span>

#### <span data-ttu-id="6cc0a-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="6cc0a-126">get_Uri</span></span> 

<span data-ttu-id="6cc0a-127">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-127">The uri of the requested navigation.</span></span>

> <span data-ttu-id="6cc0a-128">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="6cc0a-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="6cc0a-129">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6cc0a-129">get_IsUserInitiated</span></span> 

<span data-ttu-id="6cc0a-130">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-130">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="6cc0a-131">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="6cc0a-131">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="6cc0a-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="6cc0a-132">get_IsRedirected</span></span> 

<span data-ttu-id="6cc0a-133">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="6cc0a-134">[get_IsRedirected](#get_isredirected)público HRESULT (bool \* isredirected)</span><span class="sxs-lookup"><span data-stu-id="6cc0a-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="6cc0a-135">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="6cc0a-135">get_RequestHeaders</span></span> 

<span data-ttu-id="6cc0a-136">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-136">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="6cc0a-137">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="6cc0a-137">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="6cc0a-138">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-138">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="6cc0a-139">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="6cc0a-139">get_Cancel</span></span> 

<span data-ttu-id="6cc0a-140">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-140">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="6cc0a-141">público HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="6cc0a-141">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="6cc0a-142">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-142">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="6cc0a-143">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-143">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="6cc0a-144">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-144">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="6cc0a-145">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="6cc0a-145">put_Cancel</span></span> 

<span data-ttu-id="6cc0a-146">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-146">Set the Cancel property.</span></span>

> <span data-ttu-id="6cc0a-147">público HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="6cc0a-147">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

#### <span data-ttu-id="6cc0a-148">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="6cc0a-148">get_NavigationId</span></span> 

<span data-ttu-id="6cc0a-149">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="6cc0a-149">The ID of the navigation.</span></span>

> <span data-ttu-id="6cc0a-150">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="6cc0a-150">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

