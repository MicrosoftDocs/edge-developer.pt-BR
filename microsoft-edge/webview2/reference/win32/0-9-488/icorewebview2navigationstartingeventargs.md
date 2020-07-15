---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 9aa44483fc824f8a26af6293f031c58d681de624
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880469"
---
# <span data-ttu-id="997fe-104">0.9.515-ICoreWebView2NavigationStartingEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="997fe-104">0.9.515 - interface ICoreWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="997fe-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="997fe-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="997fe-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="997fe-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="997fe-107">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="997fe-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="997fe-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="997fe-108">Summary</span></span>

 <span data-ttu-id="997fe-109">Parte</span><span class="sxs-lookup"><span data-stu-id="997fe-109">Members</span></span>                        | <span data-ttu-id="997fe-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="997fe-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="997fe-111">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="997fe-111">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="997fe-112">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="997fe-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="997fe-113">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="997fe-113">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="997fe-114">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="997fe-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="997fe-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="997fe-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="997fe-116">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="997fe-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="997fe-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="997fe-117">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="997fe-118">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="997fe-118">The ID of the navigation.</span></span>
[<span data-ttu-id="997fe-119">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="997fe-119">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="997fe-120">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="997fe-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="997fe-121">get_Uri</span><span class="sxs-lookup"><span data-stu-id="997fe-121">get_Uri</span></span>](#get_uri) | <span data-ttu-id="997fe-122">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="997fe-122">The uri of the requested navigation.</span></span>
[<span data-ttu-id="997fe-123">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="997fe-123">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="997fe-124">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="997fe-124">Set the Cancel property.</span></span>

## <span data-ttu-id="997fe-125">Parte</span><span class="sxs-lookup"><span data-stu-id="997fe-125">Members</span></span>

#### <span data-ttu-id="997fe-126">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="997fe-126">get_Cancel</span></span> 

<span data-ttu-id="997fe-127">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="997fe-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="997fe-128">público HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="997fe-128">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="997fe-129">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="997fe-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="997fe-130">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="997fe-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="997fe-131">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="997fe-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="997fe-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="997fe-132">get_IsRedirected</span></span> 

<span data-ttu-id="997fe-133">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="997fe-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="997fe-134">[get_IsRedirected](#get_isredirected)público HRESULT (bool \* isredirected)</span><span class="sxs-lookup"><span data-stu-id="997fe-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="997fe-135">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="997fe-135">get_IsUserInitiated</span></span> 

<span data-ttu-id="997fe-136">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="997fe-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="997fe-137">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="997fe-137">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="997fe-138">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="997fe-138">get_NavigationId</span></span> 

<span data-ttu-id="997fe-139">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="997fe-139">The ID of the navigation.</span></span>

> <span data-ttu-id="997fe-140">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="997fe-140">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="997fe-141">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="997fe-141">get_RequestHeaders</span></span> 

<span data-ttu-id="997fe-142">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="997fe-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="997fe-143">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="997fe-143">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="997fe-144">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="997fe-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="997fe-145">get_Uri</span><span class="sxs-lookup"><span data-stu-id="997fe-145">get_Uri</span></span> 

<span data-ttu-id="997fe-146">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="997fe-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="997fe-147">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="997fe-147">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="997fe-148">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="997fe-148">put_Cancel</span></span> 

<span data-ttu-id="997fe-149">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="997fe-149">Set the Cancel property.</span></span>

> <span data-ttu-id="997fe-150">público HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="997fe-150">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

