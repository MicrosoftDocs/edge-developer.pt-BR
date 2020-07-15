---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: ea3936ac1267fa085f62db843f5cac3fad2635b5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879783"
---
# <span data-ttu-id="a0286-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0286-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="a0286-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="a0286-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="a0286-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="a0286-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="a0286-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="a0286-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="a0286-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="a0286-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="a0286-109">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="a0286-109">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="a0286-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="a0286-110">Summary</span></span>

 <span data-ttu-id="a0286-111">Parte</span><span class="sxs-lookup"><span data-stu-id="a0286-111">Members</span></span>                        | <span data-ttu-id="a0286-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="a0286-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a0286-113">Cancelar</span><span class="sxs-lookup"><span data-stu-id="a0286-113">Cancel</span></span>](#cancel) | <span data-ttu-id="a0286-114">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="a0286-114">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="a0286-115">Redirecionado</span><span class="sxs-lookup"><span data-stu-id="a0286-115">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="a0286-116">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="a0286-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="a0286-117">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a0286-117">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="a0286-118">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="a0286-118">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="a0286-119">Navigationid</span><span class="sxs-lookup"><span data-stu-id="a0286-119">NavigationId</span></span>](#navigationid) | <span data-ttu-id="a0286-120">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="a0286-120">The ID of the navigation.</span></span>
[<span data-ttu-id="a0286-121">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="a0286-121">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="a0286-122">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="a0286-122">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="a0286-123">Uri</span><span class="sxs-lookup"><span data-stu-id="a0286-123">Uri</span></span>](#uri) | <span data-ttu-id="a0286-124">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="a0286-124">The uri of the requested navigation.</span></span>

## <span data-ttu-id="a0286-125">Parte</span><span class="sxs-lookup"><span data-stu-id="a0286-125">Members</span></span>

#### <span data-ttu-id="a0286-126">Cancelar</span><span class="sxs-lookup"><span data-stu-id="a0286-126">Cancel</span></span> 

<span data-ttu-id="a0286-127">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="a0286-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="a0286-128">[cancelamento](#cancel) de booleano público</span><span class="sxs-lookup"><span data-stu-id="a0286-128">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="a0286-129">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="a0286-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="a0286-130">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="a0286-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="a0286-131">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="a0286-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="a0286-132">Redirecionado</span><span class="sxs-lookup"><span data-stu-id="a0286-132">IsRedirected</span></span> 

<span data-ttu-id="a0286-133">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="a0286-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="a0286-134">Public bool [Isredirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="a0286-134">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="a0286-135">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a0286-135">IsUserInitiated</span></span> 

<span data-ttu-id="a0286-136">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="a0286-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="a0286-137">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="a0286-137">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="a0286-138">Navigationid</span><span class="sxs-lookup"><span data-stu-id="a0286-138">NavigationId</span></span> 

<span data-ttu-id="a0286-139">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="a0286-139">The ID of the navigation.</span></span>

> <span data-ttu-id="a0286-140">[navegação](#navigationid) de ULong do ULONG público</span><span class="sxs-lookup"><span data-stu-id="a0286-140">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="a0286-141">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="a0286-141">RequestHeaders</span></span> 

<span data-ttu-id="a0286-142">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="a0286-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="a0286-143">HttpRequestHeaders público [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="a0286-143">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="a0286-144">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="a0286-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="a0286-145">Uri</span><span class="sxs-lookup"><span data-stu-id="a0286-145">Uri</span></span> 

<span data-ttu-id="a0286-146">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="a0286-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="a0286-147">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="a0286-147">public string [Uri](#uri)</span></span>

