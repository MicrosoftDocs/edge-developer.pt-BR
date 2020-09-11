---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 501483894a2abca58c5a1856ab587b93be904c8b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011462"
---
# <span data-ttu-id="d5bbd-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d5bbd-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

<span data-ttu-id="d5bbd-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="d5bbd-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="d5bbd-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="d5bbd-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="d5bbd-107">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d5bbd-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="d5bbd-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="d5bbd-108">Summary</span></span>

 <span data-ttu-id="d5bbd-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d5bbd-109">Members</span></span>                        | <span data-ttu-id="d5bbd-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="d5bbd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d5bbd-111">Solicitação</span><span class="sxs-lookup"><span data-stu-id="d5bbd-111">Request</span></span>](#request) | <span data-ttu-id="d5bbd-112">Solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="d5bbd-112">The Web resource request.</span></span>
[<span data-ttu-id="d5bbd-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="d5bbd-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="d5bbd-114">O contexto de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="d5bbd-114">The web resource request context.</span></span>
[<span data-ttu-id="d5bbd-115">Resposta</span><span class="sxs-lookup"><span data-stu-id="d5bbd-115">Response</span></span>](#response) | <span data-ttu-id="d5bbd-116">Um espaço reservado para o objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="d5bbd-116">A placeholder for the web resource response object.</span></span>
[<span data-ttu-id="d5bbd-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d5bbd-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="d5bbd-118">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="d5bbd-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="d5bbd-119">Parte</span><span class="sxs-lookup"><span data-stu-id="d5bbd-119">Members</span></span>

#### <span data-ttu-id="d5bbd-120">Solicitação</span><span class="sxs-lookup"><span data-stu-id="d5bbd-120">Request</span></span> 

<span data-ttu-id="d5bbd-121">Solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="d5bbd-121">The Web resource request.</span></span>

> <span data-ttu-id="d5bbd-122">[solicitação](#request) de [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md) pública</span><span class="sxs-lookup"><span data-stu-id="d5bbd-122">public [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md) [Request](#request)</span></span>

<span data-ttu-id="d5bbd-123">O objeto de solicitação pode não ter alguns cabeçalhos que são adicionados pela pilha de rede mais tarde.</span><span class="sxs-lookup"><span data-stu-id="d5bbd-123">The request object may be missing some headers that are added by network stack later on.</span></span>

#### <span data-ttu-id="d5bbd-124">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="d5bbd-124">ResourceContext</span></span> 

<span data-ttu-id="d5bbd-125">O contexto de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="d5bbd-125">The web resource request context.</span></span>

> <span data-ttu-id="d5bbd-126">[CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) público [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="d5bbd-126">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="d5bbd-127">Resposta</span><span class="sxs-lookup"><span data-stu-id="d5bbd-127">Response</span></span> 

<span data-ttu-id="d5bbd-128">Um espaço reservado para o objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="d5bbd-128">A placeholder for the web resource response object.</span></span>

> <span data-ttu-id="d5bbd-129">resposta [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [Response](#response) pública</span><span class="sxs-lookup"><span data-stu-id="d5bbd-129">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [Response](#response)</span></span>

<span data-ttu-id="d5bbd-130">Se esse objeto estiver definido, a solicitação de recurso da Web será concluída com essa resposta.</span><span class="sxs-lookup"><span data-stu-id="d5bbd-130">If this object is set, the web resource request will be completed with this response.</span></span> <span data-ttu-id="d5bbd-131">Um objeto de resposta de recurso da Web vazio pode ser criado com CreateWebResourceResponse e, em seguida, modificado para construir a resposta.</span><span class="sxs-lookup"><span data-stu-id="d5bbd-131">An empty Web resource response object can be created with CreateWebResourceResponse and then modified to construct the response.</span></span>

#### <span data-ttu-id="d5bbd-132">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d5bbd-132">GetDeferral</span></span> 

<span data-ttu-id="d5bbd-133">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="d5bbd-133">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="d5bbd-134">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="d5bbd-134">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="d5bbd-135">Você pode usar o objeto CoreWebView2Deferral para concluir a solicitação em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="d5bbd-135">You can use the CoreWebView2Deferral object to complete the request at a later time.</span></span>

