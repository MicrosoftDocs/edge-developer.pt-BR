---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 53cc31bc714417ab902fa8fdef9fd83f80871f10
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879664"
---
# <span data-ttu-id="e67e5-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e67e5-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

<span data-ttu-id="e67e5-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="e67e5-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="e67e5-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="e67e5-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="e67e5-107">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="e67e5-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="e67e5-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="e67e5-108">Summary</span></span>

 <span data-ttu-id="e67e5-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e67e5-109">Members</span></span>                        | <span data-ttu-id="e67e5-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="e67e5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e67e5-111">Solicitação</span><span class="sxs-lookup"><span data-stu-id="e67e5-111">Request</span></span>](#request) | <span data-ttu-id="e67e5-112">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="e67e5-112">The HTTP request.</span></span>
[<span data-ttu-id="e67e5-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="e67e5-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="e67e5-114">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="e67e5-114">The web resource request contexts.</span></span>
[<span data-ttu-id="e67e5-115">Resposta</span><span class="sxs-lookup"><span data-stu-id="e67e5-115">Response</span></span>](#response) | <span data-ttu-id="e67e5-116">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="e67e5-116">The HTTP response.</span></span>
[<span data-ttu-id="e67e5-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e67e5-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="e67e5-118">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="e67e5-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="e67e5-119">Parte</span><span class="sxs-lookup"><span data-stu-id="e67e5-119">Members</span></span>

#### <span data-ttu-id="e67e5-120">Solicitação</span><span class="sxs-lookup"><span data-stu-id="e67e5-120">Request</span></span> 

<span data-ttu-id="e67e5-121">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="e67e5-121">The HTTP request.</span></span>

> <span data-ttu-id="e67e5-122">[solicitação](#request) de HttpRequestMessage pública</span><span class="sxs-lookup"><span data-stu-id="e67e5-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="e67e5-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="e67e5-123">ResourceContext</span></span> 

<span data-ttu-id="e67e5-124">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="e67e5-124">The web resource request contexts.</span></span>

> <span data-ttu-id="e67e5-125">[CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) público [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="e67e5-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="e67e5-126">Resposta</span><span class="sxs-lookup"><span data-stu-id="e67e5-126">Response</span></span> 

<span data-ttu-id="e67e5-127">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="e67e5-127">The HTTP response.</span></span>

> <span data-ttu-id="e67e5-128">[resposta](#response) HttpResponseMessage pública</span><span class="sxs-lookup"><span data-stu-id="e67e5-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="e67e5-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e67e5-129">GetDeferral</span></span> 

<span data-ttu-id="e67e5-130">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="e67e5-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="e67e5-131">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="e67e5-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="e67e5-132">Você pode usar o objeto CoreWebView2Deferral para concluir a solicitação de rede em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="e67e5-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

