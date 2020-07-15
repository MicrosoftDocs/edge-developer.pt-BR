---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 2f9fb899746922206ff3f6cbfd129d69389fd60e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879307"
---
# <span data-ttu-id="be74c-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="be74c-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="be74c-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="be74c-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="be74c-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="be74c-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="be74c-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="be74c-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="be74c-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="be74c-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="be74c-109">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="be74c-109">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="be74c-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="be74c-110">Summary</span></span>

 <span data-ttu-id="be74c-111">Parte</span><span class="sxs-lookup"><span data-stu-id="be74c-111">Members</span></span>                        | <span data-ttu-id="be74c-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="be74c-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="be74c-113">Solicitação</span><span class="sxs-lookup"><span data-stu-id="be74c-113">Request</span></span>](#request) | <span data-ttu-id="be74c-114">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="be74c-114">The HTTP request.</span></span>
[<span data-ttu-id="be74c-115">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="be74c-115">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="be74c-116">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="be74c-116">The web resource request contexts.</span></span>
[<span data-ttu-id="be74c-117">Resposta</span><span class="sxs-lookup"><span data-stu-id="be74c-117">Response</span></span>](#response) | <span data-ttu-id="be74c-118">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="be74c-118">The HTTP response.</span></span>
[<span data-ttu-id="be74c-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="be74c-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="be74c-120">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="be74c-120">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="be74c-121">Parte</span><span class="sxs-lookup"><span data-stu-id="be74c-121">Members</span></span>

#### <span data-ttu-id="be74c-122">Solicitação</span><span class="sxs-lookup"><span data-stu-id="be74c-122">Request</span></span> 

<span data-ttu-id="be74c-123">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="be74c-123">The HTTP request.</span></span>

> <span data-ttu-id="be74c-124">[solicitação](#request) de HttpRequestMessage pública</span><span class="sxs-lookup"><span data-stu-id="be74c-124">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="be74c-125">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="be74c-125">ResourceContext</span></span> 

<span data-ttu-id="be74c-126">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="be74c-126">The web resource request contexts.</span></span>

> <span data-ttu-id="be74c-127">[CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) público [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="be74c-127">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="be74c-128">Resposta</span><span class="sxs-lookup"><span data-stu-id="be74c-128">Response</span></span> 

<span data-ttu-id="be74c-129">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="be74c-129">The HTTP response.</span></span>

> <span data-ttu-id="be74c-130">[resposta](#response) HttpResponseMessage pública</span><span class="sxs-lookup"><span data-stu-id="be74c-130">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="be74c-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="be74c-131">GetDeferral</span></span> 

<span data-ttu-id="be74c-132">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="be74c-132">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="be74c-133">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="be74c-133">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="be74c-134">Você pode usar o objeto CoreWebView2Deferral para concluir a solicitação de rede em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="be74c-134">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

