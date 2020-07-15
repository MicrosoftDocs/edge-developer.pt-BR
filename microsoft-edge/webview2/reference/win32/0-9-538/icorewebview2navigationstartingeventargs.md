---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: 8f4f366d02280163141c9591d04d72c5f5d9d082
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879755"
---
# <span data-ttu-id="7c0a6-104">interface ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="7c0a6-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="7c0a6-105">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="7c0a6-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="7c0a6-106">Summary</span></span>

 <span data-ttu-id="7c0a6-107">Parte</span><span class="sxs-lookup"><span data-stu-id="7c0a6-107">Members</span></span>                        | <span data-ttu-id="7c0a6-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="7c0a6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7c0a6-109">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="7c0a6-109">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="7c0a6-110">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-110">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="7c0a6-111">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="7c0a6-111">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="7c0a6-112">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-112">True when the navigation is redirected.</span></span>
[<span data-ttu-id="7c0a6-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="7c0a6-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="7c0a6-114">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="7c0a6-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="7c0a6-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="7c0a6-116">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-116">The ID of the navigation.</span></span>
[<span data-ttu-id="7c0a6-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="7c0a6-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="7c0a6-118">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="7c0a6-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="7c0a6-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="7c0a6-120">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-120">The uri of the requested navigation.</span></span>
[<span data-ttu-id="7c0a6-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="7c0a6-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="7c0a6-122">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-122">Set the Cancel property.</span></span>

## <span data-ttu-id="7c0a6-123">Parte</span><span class="sxs-lookup"><span data-stu-id="7c0a6-123">Members</span></span>

#### <span data-ttu-id="7c0a6-124">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="7c0a6-124">get_Cancel</span></span> 

<span data-ttu-id="7c0a6-125">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="7c0a6-126">público HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="7c0a6-126">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="7c0a6-127">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="7c0a6-128">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="7c0a6-129">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="7c0a6-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="7c0a6-130">get_IsRedirected</span></span> 

<span data-ttu-id="7c0a6-131">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="7c0a6-132">[get_IsRedirected](#get_isredirected)público HRESULT (bool \* isredirected)</span><span class="sxs-lookup"><span data-stu-id="7c0a6-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="7c0a6-133">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="7c0a6-133">get_IsUserInitiated</span></span> 

<span data-ttu-id="7c0a6-134">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="7c0a6-135">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="7c0a6-135">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="7c0a6-136">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="7c0a6-136">get_NavigationId</span></span> 

<span data-ttu-id="7c0a6-137">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-137">The ID of the navigation.</span></span>

> <span data-ttu-id="7c0a6-138">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="7c0a6-138">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="7c0a6-139">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="7c0a6-139">get_RequestHeaders</span></span> 

<span data-ttu-id="7c0a6-140">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="7c0a6-141">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="7c0a6-141">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="7c0a6-142">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="7c0a6-143">get_Uri</span><span class="sxs-lookup"><span data-stu-id="7c0a6-143">get_Uri</span></span> 

<span data-ttu-id="7c0a6-144">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="7c0a6-145">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="7c0a6-145">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="7c0a6-146">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="7c0a6-146">put_Cancel</span></span> 

<span data-ttu-id="7c0a6-147">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-147">Set the Cancel property.</span></span>

> <span data-ttu-id="7c0a6-148">público HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="7c0a6-148">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

