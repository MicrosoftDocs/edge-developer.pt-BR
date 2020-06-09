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
ms.openlocfilehash: d56f40a9780313c79f421559eaf54750828542a5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697186"
---
# <span data-ttu-id="01a91-104">interface ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="01a91-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="01a91-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="01a91-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="01a91-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="01a91-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="01a91-107">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="01a91-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="01a91-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="01a91-108">Summary</span></span>

 <span data-ttu-id="01a91-109">Parte</span><span class="sxs-lookup"><span data-stu-id="01a91-109">Members</span></span>                        | <span data-ttu-id="01a91-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="01a91-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="01a91-111">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="01a91-111">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="01a91-112">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="01a91-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="01a91-113">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="01a91-113">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="01a91-114">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="01a91-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="01a91-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="01a91-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="01a91-116">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="01a91-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="01a91-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="01a91-117">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="01a91-118">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="01a91-118">The ID of the navigation.</span></span>
[<span data-ttu-id="01a91-119">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="01a91-119">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="01a91-120">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="01a91-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="01a91-121">get_Uri</span><span class="sxs-lookup"><span data-stu-id="01a91-121">get_Uri</span></span>](#get_uri) | <span data-ttu-id="01a91-122">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="01a91-122">The uri of the requested navigation.</span></span>
[<span data-ttu-id="01a91-123">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="01a91-123">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="01a91-124">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="01a91-124">Set the Cancel property.</span></span>

## <span data-ttu-id="01a91-125">Parte</span><span class="sxs-lookup"><span data-stu-id="01a91-125">Members</span></span>

#### <span data-ttu-id="01a91-126">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="01a91-126">get_Cancel</span></span> 

<span data-ttu-id="01a91-127">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="01a91-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="01a91-128">público HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="01a91-128">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="01a91-129">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="01a91-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="01a91-130">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="01a91-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="01a91-131">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="01a91-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="01a91-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="01a91-132">get_IsRedirected</span></span> 

<span data-ttu-id="01a91-133">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="01a91-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="01a91-134">[get_IsRedirected](#get_isredirected)público HRESULT (bool \* isredirected)</span><span class="sxs-lookup"><span data-stu-id="01a91-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="01a91-135">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="01a91-135">get_IsUserInitiated</span></span> 

<span data-ttu-id="01a91-136">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="01a91-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="01a91-137">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="01a91-137">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="01a91-138">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="01a91-138">get_NavigationId</span></span> 

<span data-ttu-id="01a91-139">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="01a91-139">The ID of the navigation.</span></span>

> <span data-ttu-id="01a91-140">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="01a91-140">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="01a91-141">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="01a91-141">get_RequestHeaders</span></span> 

<span data-ttu-id="01a91-142">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="01a91-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="01a91-143">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="01a91-143">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="01a91-144">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="01a91-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="01a91-145">get_Uri</span><span class="sxs-lookup"><span data-stu-id="01a91-145">get_Uri</span></span> 

<span data-ttu-id="01a91-146">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="01a91-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="01a91-147">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="01a91-147">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="01a91-148">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="01a91-148">put_Cancel</span></span> 

<span data-ttu-id="01a91-149">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="01a91-149">Set the Cancel property.</span></span>

> <span data-ttu-id="01a91-150">público HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="01a91-150">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

