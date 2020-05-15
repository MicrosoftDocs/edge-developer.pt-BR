---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: b0b868b99d3f77679b3684a20e7744d7a22fd715
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652538"
---
# <span data-ttu-id="ebe59-104">interface ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="ebe59-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="ebe59-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="ebe59-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="ebe59-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="ebe59-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="ebe59-107">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="ebe59-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="ebe59-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="ebe59-108">Summary</span></span>

 <span data-ttu-id="ebe59-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ebe59-109">Members</span></span>                        | <span data-ttu-id="ebe59-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="ebe59-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ebe59-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ebe59-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="ebe59-112">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="ebe59-112">The uri of the requested navigation.</span></span>
[<span data-ttu-id="ebe59-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ebe59-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="ebe59-114">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="ebe59-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="ebe59-115">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="ebe59-115">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="ebe59-116">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="ebe59-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="ebe59-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="ebe59-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="ebe59-118">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="ebe59-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="ebe59-119">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="ebe59-119">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="ebe59-120">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="ebe59-120">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="ebe59-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="ebe59-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="ebe59-122">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="ebe59-122">Set the Cancel property.</span></span>
[<span data-ttu-id="ebe59-123">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="ebe59-123">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="ebe59-124">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="ebe59-124">The ID of the navigation.</span></span>

## <span data-ttu-id="ebe59-125">Parte</span><span class="sxs-lookup"><span data-stu-id="ebe59-125">Members</span></span>

#### <span data-ttu-id="ebe59-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ebe59-126">get_Uri</span></span> 

<span data-ttu-id="ebe59-127">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="ebe59-127">The uri of the requested navigation.</span></span>

> <span data-ttu-id="ebe59-128">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="ebe59-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="ebe59-129">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ebe59-129">get_IsUserInitiated</span></span> 

<span data-ttu-id="ebe59-130">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="ebe59-130">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="ebe59-131">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="ebe59-131">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="ebe59-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="ebe59-132">get_IsRedirected</span></span> 

<span data-ttu-id="ebe59-133">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="ebe59-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="ebe59-134">[get_IsRedirected](#get_isredirected)público HRESULT (bool \* isredirected)</span><span class="sxs-lookup"><span data-stu-id="ebe59-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="ebe59-135">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="ebe59-135">get_RequestHeaders</span></span> 

<span data-ttu-id="ebe59-136">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="ebe59-136">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="ebe59-137">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="ebe59-137">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="ebe59-138">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="ebe59-138">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="ebe59-139">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="ebe59-139">get_Cancel</span></span> 

<span data-ttu-id="ebe59-140">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="ebe59-140">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="ebe59-141">público HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="ebe59-141">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="ebe59-142">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="ebe59-142">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="ebe59-143">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="ebe59-143">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="ebe59-144">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="ebe59-144">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="ebe59-145">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="ebe59-145">put_Cancel</span></span> 

<span data-ttu-id="ebe59-146">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="ebe59-146">Set the Cancel property.</span></span>

> <span data-ttu-id="ebe59-147">público HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="ebe59-147">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

#### <span data-ttu-id="ebe59-148">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="ebe59-148">get_NavigationId</span></span> 

<span data-ttu-id="ebe59-149">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="ebe59-149">The ID of the navigation.</span></span>

> <span data-ttu-id="ebe59-150">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="ebe59-150">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

