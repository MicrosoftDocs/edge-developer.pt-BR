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
ms.openlocfilehash: 3b348d64bb09fcdc693ffbdfa5481fe6d7520cae
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652419"
---
# <span data-ttu-id="06ff8-104">interface ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="06ff8-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="06ff8-105">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="06ff8-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="06ff8-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="06ff8-106">Summary</span></span>

 <span data-ttu-id="06ff8-107">Parte</span><span class="sxs-lookup"><span data-stu-id="06ff8-107">Members</span></span>                        | <span data-ttu-id="06ff8-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="06ff8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="06ff8-109">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="06ff8-109">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="06ff8-110">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="06ff8-110">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="06ff8-111">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="06ff8-111">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="06ff8-112">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="06ff8-112">True when the navigation is redirected.</span></span>
[<span data-ttu-id="06ff8-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="06ff8-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="06ff8-114">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="06ff8-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="06ff8-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="06ff8-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="06ff8-116">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="06ff8-116">The ID of the navigation.</span></span>
[<span data-ttu-id="06ff8-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="06ff8-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="06ff8-118">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="06ff8-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="06ff8-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="06ff8-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="06ff8-120">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="06ff8-120">The uri of the requested navigation.</span></span>
[<span data-ttu-id="06ff8-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="06ff8-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="06ff8-122">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="06ff8-122">Set the Cancel property.</span></span>

## <span data-ttu-id="06ff8-123">Parte</span><span class="sxs-lookup"><span data-stu-id="06ff8-123">Members</span></span>

#### <span data-ttu-id="06ff8-124">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="06ff8-124">get_Cancel</span></span> 

<span data-ttu-id="06ff8-125">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="06ff8-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="06ff8-126">público HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="06ff8-126">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="06ff8-127">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="06ff8-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="06ff8-128">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="06ff8-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="06ff8-129">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="06ff8-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="06ff8-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="06ff8-130">get_IsRedirected</span></span> 

<span data-ttu-id="06ff8-131">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="06ff8-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="06ff8-132">[get_IsRedirected](#get_isredirected)público HRESULT (bool \* isredirected)</span><span class="sxs-lookup"><span data-stu-id="06ff8-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="06ff8-133">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="06ff8-133">get_IsUserInitiated</span></span> 

<span data-ttu-id="06ff8-134">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="06ff8-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="06ff8-135">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="06ff8-135">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="06ff8-136">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="06ff8-136">get_NavigationId</span></span> 

<span data-ttu-id="06ff8-137">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="06ff8-137">The ID of the navigation.</span></span>

> <span data-ttu-id="06ff8-138">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="06ff8-138">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="06ff8-139">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="06ff8-139">get_RequestHeaders</span></span> 

<span data-ttu-id="06ff8-140">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="06ff8-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="06ff8-141">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="06ff8-141">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="06ff8-142">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="06ff8-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="06ff8-143">get_Uri</span><span class="sxs-lookup"><span data-stu-id="06ff8-143">get_Uri</span></span> 

<span data-ttu-id="06ff8-144">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="06ff8-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="06ff8-145">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="06ff8-145">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="06ff8-146">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="06ff8-146">put_Cancel</span></span> 

<span data-ttu-id="06ff8-147">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="06ff8-147">Set the Cancel property.</span></span>

> <span data-ttu-id="06ff8-148">público HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="06ff8-148">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

