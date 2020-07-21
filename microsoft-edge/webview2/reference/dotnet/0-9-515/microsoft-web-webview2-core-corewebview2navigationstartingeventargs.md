---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 2f129f36502ccc404da74904c73c4bdab1d9f472
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886371"
---
# <span data-ttu-id="97292-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="97292-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="97292-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="97292-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="97292-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="97292-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="97292-107">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="97292-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="97292-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="97292-108">Summary</span></span>

 <span data-ttu-id="97292-109">Parte</span><span class="sxs-lookup"><span data-stu-id="97292-109">Members</span></span>                        | <span data-ttu-id="97292-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="97292-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="97292-111">Cancelar</span><span class="sxs-lookup"><span data-stu-id="97292-111">Cancel</span></span>](#cancel) | <span data-ttu-id="97292-112">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="97292-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="97292-113">Redirecionado</span><span class="sxs-lookup"><span data-stu-id="97292-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="97292-114">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="97292-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="97292-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="97292-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="97292-116">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="97292-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="97292-117">Navigationid</span><span class="sxs-lookup"><span data-stu-id="97292-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="97292-118">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="97292-118">The ID of the navigation.</span></span>
[<span data-ttu-id="97292-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="97292-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="97292-120">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="97292-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="97292-121">Uri</span><span class="sxs-lookup"><span data-stu-id="97292-121">Uri</span></span>](#uri) | <span data-ttu-id="97292-122">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="97292-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="97292-123">Parte</span><span class="sxs-lookup"><span data-stu-id="97292-123">Members</span></span>

#### <span data-ttu-id="97292-124">Cancelar</span><span class="sxs-lookup"><span data-stu-id="97292-124">Cancel</span></span> 

<span data-ttu-id="97292-125">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="97292-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="97292-126">[cancelamento](#cancel) de booleano público</span><span class="sxs-lookup"><span data-stu-id="97292-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="97292-127">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="97292-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="97292-128">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="97292-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="97292-129">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="97292-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="97292-130">Redirecionado</span><span class="sxs-lookup"><span data-stu-id="97292-130">IsRedirected</span></span> 

<span data-ttu-id="97292-131">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="97292-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="97292-132">Public bool [Isredirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="97292-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="97292-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="97292-133">IsUserInitiated</span></span> 

<span data-ttu-id="97292-134">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="97292-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="97292-135">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="97292-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="97292-136">Navigationid</span><span class="sxs-lookup"><span data-stu-id="97292-136">NavigationId</span></span> 

<span data-ttu-id="97292-137">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="97292-137">The ID of the navigation.</span></span>

> <span data-ttu-id="97292-138">[navegação](#navigationid) de ULong do ULONG público</span><span class="sxs-lookup"><span data-stu-id="97292-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="97292-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="97292-139">RequestHeaders</span></span> 

<span data-ttu-id="97292-140">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="97292-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="97292-141">HttpRequestHeaders público [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="97292-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="97292-142">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="97292-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="97292-143">Uri</span><span class="sxs-lookup"><span data-stu-id="97292-143">Uri</span></span> 

<span data-ttu-id="97292-144">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="97292-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="97292-145">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="97292-145">public string [Uri](#uri)</span></span>

