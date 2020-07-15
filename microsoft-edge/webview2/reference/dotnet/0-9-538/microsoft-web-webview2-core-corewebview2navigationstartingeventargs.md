---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: cd692de6aaa3dc694fb2fe149411e5fd64de1ee2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878866"
---
# <span data-ttu-id="87835-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="87835-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

<span data-ttu-id="87835-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="87835-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="87835-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="87835-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="87835-107">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="87835-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="87835-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="87835-108">Summary</span></span>

 <span data-ttu-id="87835-109">Parte</span><span class="sxs-lookup"><span data-stu-id="87835-109">Members</span></span>                        | <span data-ttu-id="87835-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="87835-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="87835-111">Cancelar</span><span class="sxs-lookup"><span data-stu-id="87835-111">Cancel</span></span>](#cancel) | <span data-ttu-id="87835-112">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="87835-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="87835-113">Redirecionado</span><span class="sxs-lookup"><span data-stu-id="87835-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="87835-114">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="87835-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="87835-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="87835-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="87835-116">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="87835-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="87835-117">Navigationid</span><span class="sxs-lookup"><span data-stu-id="87835-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="87835-118">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="87835-118">The ID of the navigation.</span></span>
[<span data-ttu-id="87835-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="87835-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="87835-120">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="87835-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="87835-121">Uri</span><span class="sxs-lookup"><span data-stu-id="87835-121">Uri</span></span>](#uri) | <span data-ttu-id="87835-122">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="87835-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="87835-123">Parte</span><span class="sxs-lookup"><span data-stu-id="87835-123">Members</span></span>

#### <span data-ttu-id="87835-124">Cancelar</span><span class="sxs-lookup"><span data-stu-id="87835-124">Cancel</span></span> 

<span data-ttu-id="87835-125">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="87835-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="87835-126">[cancelamento](#cancel) de booleano público</span><span class="sxs-lookup"><span data-stu-id="87835-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="87835-127">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="87835-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="87835-128">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="87835-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="87835-129">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="87835-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="87835-130">Redirecionado</span><span class="sxs-lookup"><span data-stu-id="87835-130">IsRedirected</span></span> 

<span data-ttu-id="87835-131">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="87835-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="87835-132">Public bool [Isredirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="87835-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="87835-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="87835-133">IsUserInitiated</span></span> 

<span data-ttu-id="87835-134">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="87835-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="87835-135">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="87835-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="87835-136">Navigationid</span><span class="sxs-lookup"><span data-stu-id="87835-136">NavigationId</span></span> 

<span data-ttu-id="87835-137">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="87835-137">The ID of the navigation.</span></span>

> <span data-ttu-id="87835-138">[navegação](#navigationid) de ULong do ULONG público</span><span class="sxs-lookup"><span data-stu-id="87835-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="87835-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="87835-139">RequestHeaders</span></span> 

<span data-ttu-id="87835-140">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="87835-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="87835-141">HttpRequestHeaders público [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="87835-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="87835-142">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="87835-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="87835-143">Uri</span><span class="sxs-lookup"><span data-stu-id="87835-143">Uri</span></span> 

<span data-ttu-id="87835-144">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="87835-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="87835-145">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="87835-145">public string [Uri](#uri)</span></span>

