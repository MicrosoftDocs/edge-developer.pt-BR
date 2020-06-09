---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 705289c386a174bf6ac3929fabf9ede92e0987ae
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698230"
---
# <span data-ttu-id="158ff-104">interface ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="158ff-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="158ff-105">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="158ff-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="158ff-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="158ff-106">Summary</span></span>

 <span data-ttu-id="158ff-107">Parte</span><span class="sxs-lookup"><span data-stu-id="158ff-107">Members</span></span>                        | <span data-ttu-id="158ff-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="158ff-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="158ff-109">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="158ff-109">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="158ff-110">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="158ff-110">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="158ff-111">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="158ff-111">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="158ff-112">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="158ff-112">True when the navigation is redirected.</span></span>
[<span data-ttu-id="158ff-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="158ff-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="158ff-114">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="158ff-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="158ff-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="158ff-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="158ff-116">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="158ff-116">The ID of the navigation.</span></span>
[<span data-ttu-id="158ff-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="158ff-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="158ff-118">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="158ff-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="158ff-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="158ff-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="158ff-120">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="158ff-120">The uri of the requested navigation.</span></span>
[<span data-ttu-id="158ff-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="158ff-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="158ff-122">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="158ff-122">Set the Cancel property.</span></span>

## <span data-ttu-id="158ff-123">Parte</span><span class="sxs-lookup"><span data-stu-id="158ff-123">Members</span></span>

#### <span data-ttu-id="158ff-124">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="158ff-124">get_Cancel</span></span> 

<span data-ttu-id="158ff-125">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="158ff-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="158ff-126">público HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="158ff-126">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="158ff-127">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="158ff-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="158ff-128">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="158ff-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="158ff-129">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="158ff-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="158ff-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="158ff-130">get_IsRedirected</span></span> 

<span data-ttu-id="158ff-131">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="158ff-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="158ff-132">[get_IsRedirected](#get_isredirected)público HRESULT (bool \* isredirected)</span><span class="sxs-lookup"><span data-stu-id="158ff-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="158ff-133">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="158ff-133">get_IsUserInitiated</span></span> 

<span data-ttu-id="158ff-134">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="158ff-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="158ff-135">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="158ff-135">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="158ff-136">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="158ff-136">get_NavigationId</span></span> 

<span data-ttu-id="158ff-137">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="158ff-137">The ID of the navigation.</span></span>

> <span data-ttu-id="158ff-138">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="158ff-138">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="158ff-139">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="158ff-139">get_RequestHeaders</span></span> 

<span data-ttu-id="158ff-140">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="158ff-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="158ff-141">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="158ff-141">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="158ff-142">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="158ff-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="158ff-143">get_Uri</span><span class="sxs-lookup"><span data-stu-id="158ff-143">get_Uri</span></span> 

<span data-ttu-id="158ff-144">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="158ff-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="158ff-145">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="158ff-145">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="158ff-146">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="158ff-146">put_Cancel</span></span> 

<span data-ttu-id="158ff-147">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="158ff-147">Set the Cancel property.</span></span>

> <span data-ttu-id="158ff-148">público HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="158ff-148">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

