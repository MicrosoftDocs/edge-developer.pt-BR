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
ms.openlocfilehash: 8b7ac3ab27cf5a2d9e80a77eabc488599820a02f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652776"
---
# <span data-ttu-id="9ceb6-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="9ceb6-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

<span data-ttu-id="9ceb6-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="9ceb6-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="9ceb6-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="9ceb6-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="9ceb6-107">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="9ceb6-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="9ceb6-108">Summary</span></span>

 <span data-ttu-id="9ceb6-109">Parte</span><span class="sxs-lookup"><span data-stu-id="9ceb6-109">Members</span></span>                        | <span data-ttu-id="9ceb6-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="9ceb6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9ceb6-111">Cancelar</span><span class="sxs-lookup"><span data-stu-id="9ceb6-111">Cancel</span></span>](#cancel) | <span data-ttu-id="9ceb6-112">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="9ceb6-113">Redirecionado</span><span class="sxs-lookup"><span data-stu-id="9ceb6-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="9ceb6-114">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="9ceb6-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="9ceb6-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="9ceb6-116">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="9ceb6-117">Navigationid</span><span class="sxs-lookup"><span data-stu-id="9ceb6-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="9ceb6-118">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-118">The ID of the navigation.</span></span>
[<span data-ttu-id="9ceb6-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="9ceb6-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="9ceb6-120">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="9ceb6-121">Uri</span><span class="sxs-lookup"><span data-stu-id="9ceb6-121">Uri</span></span>](#uri) | <span data-ttu-id="9ceb6-122">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="9ceb6-123">Parte</span><span class="sxs-lookup"><span data-stu-id="9ceb6-123">Members</span></span>

#### <span data-ttu-id="9ceb6-124">Cancelar</span><span class="sxs-lookup"><span data-stu-id="9ceb6-124">Cancel</span></span> 

<span data-ttu-id="9ceb6-125">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="9ceb6-126">[cancelamento](#cancel) de booleano público</span><span class="sxs-lookup"><span data-stu-id="9ceb6-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="9ceb6-127">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="9ceb6-128">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="9ceb6-129">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="9ceb6-130">Redirecionado</span><span class="sxs-lookup"><span data-stu-id="9ceb6-130">IsRedirected</span></span> 

<span data-ttu-id="9ceb6-131">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="9ceb6-132">Public bool [Isredirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="9ceb6-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="9ceb6-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="9ceb6-133">IsUserInitiated</span></span> 

<span data-ttu-id="9ceb6-134">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="9ceb6-135">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="9ceb6-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="9ceb6-136">Navigationid</span><span class="sxs-lookup"><span data-stu-id="9ceb6-136">NavigationId</span></span> 

<span data-ttu-id="9ceb6-137">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-137">The ID of the navigation.</span></span>

> <span data-ttu-id="9ceb6-138">[navegação](#navigationid) de ULong do ULONG público</span><span class="sxs-lookup"><span data-stu-id="9ceb6-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="9ceb6-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="9ceb6-139">RequestHeaders</span></span> 

<span data-ttu-id="9ceb6-140">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="9ceb6-141">HttpRequestHeaders público [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="9ceb6-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="9ceb6-142">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="9ceb6-143">Uri</span><span class="sxs-lookup"><span data-stu-id="9ceb6-143">Uri</span></span> 

<span data-ttu-id="9ceb6-144">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="9ceb6-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="9ceb6-145">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="9ceb6-145">public string [Uri](#uri)</span></span>

