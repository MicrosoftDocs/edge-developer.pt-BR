---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 5996f0eff4db17530750eb39c7693ea0f8496a4d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885882"
---
# <span data-ttu-id="5825d-104">0.8.355-IWebView2NavigationStartingEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="5825d-104">0.8.355 - interface IWebView2NavigationStartingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="5825d-105">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="5825d-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="5825d-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="5825d-106">Summary</span></span>

 <span data-ttu-id="5825d-107">Parte</span><span class="sxs-lookup"><span data-stu-id="5825d-107">Members</span></span>                        | <span data-ttu-id="5825d-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="5825d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5825d-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="5825d-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="5825d-110">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="5825d-110">The uri of the requested navigation.</span></span>
[<span data-ttu-id="5825d-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="5825d-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="5825d-112">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="5825d-112">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="5825d-113">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="5825d-113">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="5825d-114">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="5825d-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="5825d-115">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="5825d-115">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="5825d-116">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="5825d-116">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="5825d-117">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="5825d-117">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="5825d-118">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="5825d-118">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="5825d-119">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="5825d-119">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="5825d-120">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="5825d-120">Set the Cancel property.</span></span>

## <span data-ttu-id="5825d-121">Parte</span><span class="sxs-lookup"><span data-stu-id="5825d-121">Members</span></span>

#### <span data-ttu-id="5825d-122">get_Uri</span><span class="sxs-lookup"><span data-stu-id="5825d-122">get_Uri</span></span> 

<span data-ttu-id="5825d-123">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="5825d-123">The uri of the requested navigation.</span></span>

> <span data-ttu-id="5825d-124">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="5825d-124">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="5825d-125">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="5825d-125">get_IsUserInitiated</span></span> 

<span data-ttu-id="5825d-126">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="5825d-126">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="5825d-127">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="5825d-127">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="5825d-128">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="5825d-128">get_IsRedirected</span></span> 

<span data-ttu-id="5825d-129">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="5825d-129">True when the navigation is redirected.</span></span>

> <span data-ttu-id="5825d-130">[get_IsRedirected](#get_isredirected)público HRESULT (bool \* isredirected)</span><span class="sxs-lookup"><span data-stu-id="5825d-130">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="5825d-131">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="5825d-131">get_RequestHeaders</span></span> 

<span data-ttu-id="5825d-132">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="5825d-132">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="5825d-133">Public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="5825d-133">public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="5825d-134">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="5825d-134">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="5825d-135">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="5825d-135">get_Cancel</span></span> 

<span data-ttu-id="5825d-136">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="5825d-136">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="5825d-137">público HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="5825d-137">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="5825d-138">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="5825d-138">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="5825d-139">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="5825d-139">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="5825d-140">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="5825d-140">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="5825d-141">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="5825d-141">put_Cancel</span></span> 

<span data-ttu-id="5825d-142">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="5825d-142">Set the Cancel property.</span></span>

> <span data-ttu-id="5825d-143">público HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="5825d-143">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

