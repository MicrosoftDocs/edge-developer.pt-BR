---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: ee6886e32b32f4da4bbdc04fe6e866210a76488b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652788"
---
# <span data-ttu-id="643b5-104">interface IWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="643b5-104">interface IWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="643b5-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="643b5-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="643b5-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="643b5-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="643b5-107">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="643b5-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="643b5-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="643b5-108">Summary</span></span>

 <span data-ttu-id="643b5-109">Parte</span><span class="sxs-lookup"><span data-stu-id="643b5-109">Members</span></span>                        | <span data-ttu-id="643b5-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="643b5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="643b5-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="643b5-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="643b5-112">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="643b5-112">The uri of the requested navigation.</span></span>
[<span data-ttu-id="643b5-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="643b5-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="643b5-114">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="643b5-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="643b5-115">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="643b5-115">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="643b5-116">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="643b5-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="643b5-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="643b5-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="643b5-118">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="643b5-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="643b5-119">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="643b5-119">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="643b5-120">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="643b5-120">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="643b5-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="643b5-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="643b5-122">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="643b5-122">Set the Cancel property.</span></span>

## <span data-ttu-id="643b5-123">Parte</span><span class="sxs-lookup"><span data-stu-id="643b5-123">Members</span></span>

#### <span data-ttu-id="643b5-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="643b5-124">get_Uri</span></span> 

<span data-ttu-id="643b5-125">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="643b5-125">The uri of the requested navigation.</span></span>

> <span data-ttu-id="643b5-126">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="643b5-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="643b5-127">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="643b5-127">get_IsUserInitiated</span></span> 

<span data-ttu-id="643b5-128">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="643b5-128">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="643b5-129">[get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="643b5-129">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="643b5-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="643b5-130">get_IsRedirected</span></span> 

<span data-ttu-id="643b5-131">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="643b5-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="643b5-132">[get_IsRedirected](#get_isredirected)público HRESULT (bool \* isredirected)</span><span class="sxs-lookup"><span data-stu-id="643b5-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="643b5-133">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="643b5-133">get_RequestHeaders</span></span> 

<span data-ttu-id="643b5-134">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="643b5-134">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="643b5-135">Public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="643b5-135">public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="643b5-136">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="643b5-136">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="643b5-137">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="643b5-137">get_Cancel</span></span> 

<span data-ttu-id="643b5-138">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="643b5-138">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="643b5-139">público HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="643b5-139">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="643b5-140">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="643b5-140">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="643b5-141">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="643b5-141">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="643b5-142">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="643b5-142">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="643b5-143">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="643b5-143">put_Cancel</span></span> 

<span data-ttu-id="643b5-144">Defina a propriedade cancelamento.</span><span class="sxs-lookup"><span data-stu-id="643b5-144">Set the Cancel property.</span></span>

> <span data-ttu-id="643b5-145">público HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="643b5-145">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

