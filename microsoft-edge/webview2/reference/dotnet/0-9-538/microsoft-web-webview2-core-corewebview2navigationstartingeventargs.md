---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: 5f63cd8a9dc16ee82d77fe4b5a0b705eb79e7c6f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010931"
---
# <span data-ttu-id="0b8e8-104">classe 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="0b8e8-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="0b8e8-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="0b8e8-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="0b8e8-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="0b8e8-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="0b8e8-107">Args de evento para o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="0b8e8-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="0b8e8-108">Summary</span></span>

 <span data-ttu-id="0b8e8-109">Parte</span><span class="sxs-lookup"><span data-stu-id="0b8e8-109">Members</span></span>                        | <span data-ttu-id="0b8e8-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="0b8e8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0b8e8-111">Cancelar</span><span class="sxs-lookup"><span data-stu-id="0b8e8-111">Cancel</span></span>](#cancel) | <span data-ttu-id="0b8e8-112">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="0b8e8-113">Redirecionado</span><span class="sxs-lookup"><span data-stu-id="0b8e8-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="0b8e8-114">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="0b8e8-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="0b8e8-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="0b8e8-116">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="0b8e8-117">Navigationid</span><span class="sxs-lookup"><span data-stu-id="0b8e8-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="0b8e8-118">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-118">The ID of the navigation.</span></span>
[<span data-ttu-id="0b8e8-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="0b8e8-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="0b8e8-120">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="0b8e8-121">Uri</span><span class="sxs-lookup"><span data-stu-id="0b8e8-121">Uri</span></span>](#uri) | <span data-ttu-id="0b8e8-122">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="0b8e8-123">Parte</span><span class="sxs-lookup"><span data-stu-id="0b8e8-123">Members</span></span>

#### <span data-ttu-id="0b8e8-124">Cancelar</span><span class="sxs-lookup"><span data-stu-id="0b8e8-124">Cancel</span></span> 

<span data-ttu-id="0b8e8-125">O host pode definir esse sinalizador para cancelar a navegação.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="0b8e8-126">[cancelamento](#cancel) de booleano público</span><span class="sxs-lookup"><span data-stu-id="0b8e8-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="0b8e8-127">Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="0b8e8-128">Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="0b8e8-129">Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="0b8e8-130">Redirecionado</span><span class="sxs-lookup"><span data-stu-id="0b8e8-130">IsRedirected</span></span> 

<span data-ttu-id="0b8e8-131">Verdadeiro quando a navegação é redirecionada.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="0b8e8-132">Public bool [Isredirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="0b8e8-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="0b8e8-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="0b8e8-133">IsUserInitiated</span></span> 

<span data-ttu-id="0b8e8-134">Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="0b8e8-135">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="0b8e8-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="0b8e8-136">Navigationid</span><span class="sxs-lookup"><span data-stu-id="0b8e8-136">NavigationId</span></span> 

<span data-ttu-id="0b8e8-137">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-137">The ID of the navigation.</span></span>

> <span data-ttu-id="0b8e8-138">[navegação](#navigationid) de ULong do ULONG público</span><span class="sxs-lookup"><span data-stu-id="0b8e8-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="0b8e8-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="0b8e8-139">RequestHeaders</span></span> 

<span data-ttu-id="0b8e8-140">Os cabeçalhos da solicitação HTTP para a navegação.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="0b8e8-141">HttpRequestHeaders público [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="0b8e8-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="0b8e8-142">Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="0b8e8-143">Uri</span><span class="sxs-lookup"><span data-stu-id="0b8e8-143">Uri</span></span> 

<span data-ttu-id="0b8e8-144">O URI da navegação solicitada.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="0b8e8-145">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="0b8e8-145">public string [Uri](#uri)</span></span>

