---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: ebfb4aaf3f0c2b5531aaab3783572cf550bebf83
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011567"
---
# <span data-ttu-id="a8589-104">interface ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="a8589-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="a8589-105">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="a8589-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="a8589-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="a8589-106">Summary</span></span>

 <span data-ttu-id="a8589-107">Parte</span><span class="sxs-lookup"><span data-stu-id="a8589-107">Members</span></span>                        | <span data-ttu-id="a8589-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="a8589-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a8589-109">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="a8589-109">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="a8589-110">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="a8589-110">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="a8589-111">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="a8589-111">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="a8589-112">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="a8589-112">True when the navigation is redirected.</span></span>
[<span data-ttu-id="a8589-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a8589-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="a8589-114">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="a8589-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="a8589-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="a8589-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="a8589-116">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="a8589-116">The ID of the navigation.</span></span>
[<span data-ttu-id="a8589-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="a8589-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="a8589-118">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="a8589-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="a8589-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="a8589-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="a8589-120">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="a8589-120">The uri of the requested navigation.</span></span>
[<span data-ttu-id="a8589-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="a8589-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="a8589-122">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="a8589-122">Set the Cancel property.</span></span>

## <span data-ttu-id="a8589-123">Parte</span><span class="sxs-lookup"><span data-stu-id="a8589-123">Members</span></span>

#### <span data-ttu-id="a8589-124">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="a8589-124">get_Cancel</span></span> 

<span data-ttu-id="a8589-125">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="a8589-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="a8589-126">público HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="a8589-126">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="a8589-127">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="a8589-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="a8589-128">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="a8589-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="a8589-129">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="a8589-129">This means cookies can be set and used part of a request for the navigation.</span></span> <span data-ttu-id="a8589-130">Cancelamento de navegação para a navegação: não há suporte para a navegação de quadro ou em branco para srcdoc.</span><span class="sxs-lookup"><span data-stu-id="a8589-130">Cancellation for navigation to about:blank or frame navigation to srcdoc is not supported.</span></span> <span data-ttu-id="a8589-131">Tais tentativas serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="a8589-131">Such attempts will be ignored.</span></span>

#### <span data-ttu-id="a8589-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="a8589-132">get_IsRedirected</span></span> 

<span data-ttu-id="a8589-133">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="a8589-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="a8589-134">[get_IsRedirected](#get_isredirected)público HRESULT (bool \* isredirected)</span><span class="sxs-lookup"><span data-stu-id="a8589-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="a8589-135">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a8589-135">get_IsUserInitiated</span></span> 

<span data-ttu-id="a8589-136">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="a8589-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="a8589-137">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="a8589-137">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="a8589-138">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="a8589-138">get_NavigationId</span></span> 

<span data-ttu-id="a8589-139">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="a8589-139">The ID of the navigation.</span></span>

> <span data-ttu-id="a8589-140">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigationid)</span><span class="sxs-lookup"><span data-stu-id="a8589-140">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigationId)</span></span>

#### <span data-ttu-id="a8589-141">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="a8589-141">get_RequestHeaders</span></span> 

<span data-ttu-id="a8589-142">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="a8589-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="a8589-143">Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="a8589-143">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="a8589-144">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="a8589-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="a8589-145">get_Uri</span><span class="sxs-lookup"><span data-stu-id="a8589-145">get_Uri</span></span> 

<span data-ttu-id="a8589-146">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="a8589-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="a8589-147">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="a8589-147">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="a8589-148">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="a8589-148">put_Cancel</span></span> 

<span data-ttu-id="a8589-149">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="a8589-149">Set the Cancel property.</span></span>

> <span data-ttu-id="a8589-150">público HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="a8589-150">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

