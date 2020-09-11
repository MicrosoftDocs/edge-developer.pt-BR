---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: 8bf2cf37ef76256987a52fd5491e5c995244dd65
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011297"
---
# <span data-ttu-id="180d3-104">0.9.579-ICoreWebView2NavigationStartingEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="180d3-104">0.9.579 - interface ICoreWebView2NavigationStartingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="180d3-105">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="180d3-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="180d3-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="180d3-106">Summary</span></span>

 <span data-ttu-id="180d3-107">Parte</span><span class="sxs-lookup"><span data-stu-id="180d3-107">Members</span></span>                        | <span data-ttu-id="180d3-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="180d3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="180d3-109">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="180d3-109">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="180d3-110">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="180d3-110">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="180d3-111">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="180d3-111">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="180d3-112">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="180d3-112">True when the navigation is redirected.</span></span>
[<span data-ttu-id="180d3-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="180d3-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="180d3-114">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="180d3-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="180d3-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="180d3-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="180d3-116">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="180d3-116">The ID of the navigation.</span></span>
[<span data-ttu-id="180d3-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="180d3-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="180d3-118">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="180d3-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="180d3-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="180d3-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="180d3-120">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="180d3-120">The uri of the requested navigation.</span></span>
[<span data-ttu-id="180d3-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="180d3-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="180d3-122">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="180d3-122">Set the Cancel property.</span></span>

## <span data-ttu-id="180d3-123">Parte</span><span class="sxs-lookup"><span data-stu-id="180d3-123">Members</span></span>

#### <span data-ttu-id="180d3-124">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="180d3-124">get_Cancel</span></span> 

<span data-ttu-id="180d3-125">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="180d3-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="180d3-126">público HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="180d3-126">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="180d3-127">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="180d3-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="180d3-128">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="180d3-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="180d3-129">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="180d3-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="180d3-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="180d3-130">get_IsRedirected</span></span> 

<span data-ttu-id="180d3-131">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="180d3-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="180d3-132">[get_IsRedirected](#get_isredirected)público HRESULT (bool \* isredirected)</span><span class="sxs-lookup"><span data-stu-id="180d3-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="180d3-133">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="180d3-133">get_IsUserInitiated</span></span> 

<span data-ttu-id="180d3-134">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="180d3-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="180d3-135">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="180d3-135">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="180d3-136">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="180d3-136">get_NavigationId</span></span> 

<span data-ttu-id="180d3-137">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="180d3-137">The ID of the navigation.</span></span>

> <span data-ttu-id="180d3-138">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="180d3-138">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="180d3-139">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="180d3-139">get_RequestHeaders</span></span> 

<span data-ttu-id="180d3-140">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="180d3-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="180d3-141">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="180d3-141">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="180d3-142">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="180d3-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="180d3-143">get_Uri</span><span class="sxs-lookup"><span data-stu-id="180d3-143">get_Uri</span></span> 

<span data-ttu-id="180d3-144">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="180d3-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="180d3-145">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="180d3-145">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="180d3-146">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="180d3-146">put_Cancel</span></span> 

<span data-ttu-id="180d3-147">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="180d3-147">Set the Cancel property.</span></span>

> <span data-ttu-id="180d3-148">público HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="180d3-148">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

