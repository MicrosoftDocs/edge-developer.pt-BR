---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 98e242ace5eb0ae5958ddb1eb6cd380d194294be
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697627"
---
# <span data-ttu-id="3cfd0-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="3cfd0-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="3cfd0-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="3cfd0-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="3cfd0-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="3cfd0-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="3cfd0-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="3cfd0-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="3cfd0-109">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-109">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="3cfd0-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="3cfd0-110">Summary</span></span>

 <span data-ttu-id="3cfd0-111">Parte</span><span class="sxs-lookup"><span data-stu-id="3cfd0-111">Members</span></span>                        | <span data-ttu-id="3cfd0-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="3cfd0-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3cfd0-113">Cancelar</span><span class="sxs-lookup"><span data-stu-id="3cfd0-113">Cancel</span></span>](#cancel) | <span data-ttu-id="3cfd0-114">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-114">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="3cfd0-115">Redirecionado</span><span class="sxs-lookup"><span data-stu-id="3cfd0-115">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="3cfd0-116">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="3cfd0-117">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="3cfd0-117">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="3cfd0-118">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-118">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="3cfd0-119">Navigationid</span><span class="sxs-lookup"><span data-stu-id="3cfd0-119">NavigationId</span></span>](#navigationid) | <span data-ttu-id="3cfd0-120">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-120">The ID of the navigation.</span></span>
[<span data-ttu-id="3cfd0-121">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="3cfd0-121">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="3cfd0-122">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-122">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="3cfd0-123">Uri</span><span class="sxs-lookup"><span data-stu-id="3cfd0-123">Uri</span></span>](#uri) | <span data-ttu-id="3cfd0-124">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-124">The uri of the requested navigation.</span></span>

## <span data-ttu-id="3cfd0-125">Parte</span><span class="sxs-lookup"><span data-stu-id="3cfd0-125">Members</span></span>

#### <span data-ttu-id="3cfd0-126">Cancelar</span><span class="sxs-lookup"><span data-stu-id="3cfd0-126">Cancel</span></span> 

<span data-ttu-id="3cfd0-127">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="3cfd0-128">[cancelamento](#cancel) de booleano público</span><span class="sxs-lookup"><span data-stu-id="3cfd0-128">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="3cfd0-129">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="3cfd0-130">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="3cfd0-131">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="3cfd0-132">Redirecionado</span><span class="sxs-lookup"><span data-stu-id="3cfd0-132">IsRedirected</span></span> 

<span data-ttu-id="3cfd0-133">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="3cfd0-134">Public bool [Isredirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="3cfd0-134">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="3cfd0-135">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="3cfd0-135">IsUserInitiated</span></span> 

<span data-ttu-id="3cfd0-136">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="3cfd0-137">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="3cfd0-137">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="3cfd0-138">Navigationid</span><span class="sxs-lookup"><span data-stu-id="3cfd0-138">NavigationId</span></span> 

<span data-ttu-id="3cfd0-139">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-139">The ID of the navigation.</span></span>

> <span data-ttu-id="3cfd0-140">[navegação](#navigationid) de ULong do ULONG público</span><span class="sxs-lookup"><span data-stu-id="3cfd0-140">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="3cfd0-141">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="3cfd0-141">RequestHeaders</span></span> 

<span data-ttu-id="3cfd0-142">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="3cfd0-143">HttpRequestHeaders público [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="3cfd0-143">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="3cfd0-144">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="3cfd0-145">Uri</span><span class="sxs-lookup"><span data-stu-id="3cfd0-145">Uri</span></span> 

<span data-ttu-id="3cfd0-146">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="3cfd0-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="3cfd0-147">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="3cfd0-147">public string [Uri](#uri)</span></span>

