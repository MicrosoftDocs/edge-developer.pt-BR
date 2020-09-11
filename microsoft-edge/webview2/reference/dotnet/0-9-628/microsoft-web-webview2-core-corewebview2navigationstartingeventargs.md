---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: 1b80b42bc26316d1fcc8ac74656f24cb0db75bae
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011480"
---
# <span data-ttu-id="85f9d-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="85f9d-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

<span data-ttu-id="85f9d-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="85f9d-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="85f9d-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="85f9d-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="85f9d-107">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="85f9d-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="85f9d-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="85f9d-108">Summary</span></span>

 <span data-ttu-id="85f9d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="85f9d-109">Members</span></span>                        | <span data-ttu-id="85f9d-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="85f9d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="85f9d-111">Cancelar</span><span class="sxs-lookup"><span data-stu-id="85f9d-111">Cancel</span></span>](#cancel) | <span data-ttu-id="85f9d-112">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="85f9d-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="85f9d-113">Redirecionado</span><span class="sxs-lookup"><span data-stu-id="85f9d-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="85f9d-114">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="85f9d-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="85f9d-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="85f9d-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="85f9d-116">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="85f9d-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="85f9d-117">Navigationid</span><span class="sxs-lookup"><span data-stu-id="85f9d-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="85f9d-118">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="85f9d-118">The ID of the navigation.</span></span>
[<span data-ttu-id="85f9d-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="85f9d-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="85f9d-120">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="85f9d-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="85f9d-121">Uri</span><span class="sxs-lookup"><span data-stu-id="85f9d-121">Uri</span></span>](#uri) | <span data-ttu-id="85f9d-122">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="85f9d-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="85f9d-123">Parte</span><span class="sxs-lookup"><span data-stu-id="85f9d-123">Members</span></span>

#### <span data-ttu-id="85f9d-124">Cancelar</span><span class="sxs-lookup"><span data-stu-id="85f9d-124">Cancel</span></span> 

<span data-ttu-id="85f9d-125">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="85f9d-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="85f9d-126">[cancelamento](#cancel) de booleano público</span><span class="sxs-lookup"><span data-stu-id="85f9d-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="85f9d-127">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="85f9d-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="85f9d-128">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="85f9d-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="85f9d-129">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="85f9d-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="85f9d-130">Redirecionado</span><span class="sxs-lookup"><span data-stu-id="85f9d-130">IsRedirected</span></span> 

<span data-ttu-id="85f9d-131">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="85f9d-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="85f9d-132">Public bool [Isredirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="85f9d-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="85f9d-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="85f9d-133">IsUserInitiated</span></span> 

<span data-ttu-id="85f9d-134">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="85f9d-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="85f9d-135">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="85f9d-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="85f9d-136">Navigationid</span><span class="sxs-lookup"><span data-stu-id="85f9d-136">NavigationId</span></span> 

<span data-ttu-id="85f9d-137">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="85f9d-137">The ID of the navigation.</span></span>

> <span data-ttu-id="85f9d-138">[navegação](#navigationid) de ULong do ULONG público</span><span class="sxs-lookup"><span data-stu-id="85f9d-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="85f9d-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="85f9d-139">RequestHeaders</span></span> 

<span data-ttu-id="85f9d-140">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="85f9d-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="85f9d-141">CoreWebView2HttpRequestHeaders público [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="85f9d-141">public CoreWebView2HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="85f9d-142">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="85f9d-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="85f9d-143">Uri</span><span class="sxs-lookup"><span data-stu-id="85f9d-143">Uri</span></span> 

<span data-ttu-id="85f9d-144">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="85f9d-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="85f9d-145">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="85f9d-145">public string [Uri](#uri)</span></span>

