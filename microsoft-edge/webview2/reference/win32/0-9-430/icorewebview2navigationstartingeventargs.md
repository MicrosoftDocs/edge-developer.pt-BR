---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: bd9d10d5f281b2e8f0a5d0687235560c44edc170
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886434"
---
# <span data-ttu-id="ef5a5-104">0.9.430-ICoreWebView2NavigationStartingEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="ef5a5-104">0.9.430 - interface ICoreWebView2NavigationStartingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="ef5a5-105">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="ef5a5-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="ef5a5-106">Summary</span></span>

 <span data-ttu-id="ef5a5-107">Parte</span><span class="sxs-lookup"><span data-stu-id="ef5a5-107">Members</span></span>                        | <span data-ttu-id="ef5a5-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="ef5a5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ef5a5-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ef5a5-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="ef5a5-110">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-110">The uri of the requested navigation.</span></span>
[<span data-ttu-id="ef5a5-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ef5a5-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="ef5a5-112">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-112">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="ef5a5-113">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="ef5a5-113">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="ef5a5-114">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="ef5a5-115">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="ef5a5-115">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="ef5a5-116">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-116">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="ef5a5-117">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="ef5a5-117">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="ef5a5-118">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-118">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="ef5a5-119">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="ef5a5-119">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="ef5a5-120">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-120">Set the Cancel property.</span></span>
[<span data-ttu-id="ef5a5-121">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="ef5a5-121">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="ef5a5-122">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-122">The ID of the navigation.</span></span>

## <span data-ttu-id="ef5a5-123">Parte</span><span class="sxs-lookup"><span data-stu-id="ef5a5-123">Members</span></span>

#### <span data-ttu-id="ef5a5-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ef5a5-124">get_Uri</span></span> 

<span data-ttu-id="ef5a5-125">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-125">The uri of the requested navigation.</span></span>

> <span data-ttu-id="ef5a5-126">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="ef5a5-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="ef5a5-127">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ef5a5-127">get_IsUserInitiated</span></span> 

<span data-ttu-id="ef5a5-128">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-128">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="ef5a5-129">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="ef5a5-129">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="ef5a5-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="ef5a5-130">get_IsRedirected</span></span> 

<span data-ttu-id="ef5a5-131">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="ef5a5-132">[get_IsRedirected](#get_isredirected)público HRESULT (bool \* isredirected)</span><span class="sxs-lookup"><span data-stu-id="ef5a5-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="ef5a5-133">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="ef5a5-133">get_RequestHeaders</span></span> 

<span data-ttu-id="ef5a5-134">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-134">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="ef5a5-135">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="ef5a5-135">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="ef5a5-136">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-136">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="ef5a5-137">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="ef5a5-137">get_Cancel</span></span> 

<span data-ttu-id="ef5a5-138">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-138">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="ef5a5-139">público HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="ef5a5-139">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="ef5a5-140">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-140">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="ef5a5-141">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-141">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="ef5a5-142">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-142">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="ef5a5-143">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="ef5a5-143">put_Cancel</span></span> 

<span data-ttu-id="ef5a5-144">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-144">Set the Cancel property.</span></span>

> <span data-ttu-id="ef5a5-145">público HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="ef5a5-145">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

#### <span data-ttu-id="ef5a5-146">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="ef5a5-146">get_NavigationId</span></span> 

<span data-ttu-id="ef5a5-147">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="ef5a5-147">The ID of the navigation.</span></span>

> <span data-ttu-id="ef5a5-148">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="ef5a5-148">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

