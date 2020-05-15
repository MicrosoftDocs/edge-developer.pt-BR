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
ms.openlocfilehash: 9210a4b70d0e2edf30cbaad906f57b360688dfe8
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652433"
---
# <span data-ttu-id="077ed-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="077ed-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

<span data-ttu-id="077ed-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="077ed-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="077ed-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="077ed-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="077ed-107">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="077ed-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="077ed-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="077ed-108">Summary</span></span>

 <span data-ttu-id="077ed-109">Parte</span><span class="sxs-lookup"><span data-stu-id="077ed-109">Members</span></span>                        | <span data-ttu-id="077ed-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="077ed-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="077ed-111">Solicitação</span><span class="sxs-lookup"><span data-stu-id="077ed-111">Request</span></span>](#request) | <span data-ttu-id="077ed-112">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="077ed-112">The HTTP request.</span></span>
[<span data-ttu-id="077ed-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="077ed-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="077ed-114">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="077ed-114">The web resource request contexts.</span></span>
[<span data-ttu-id="077ed-115">Resposta</span><span class="sxs-lookup"><span data-stu-id="077ed-115">Response</span></span>](#response) | <span data-ttu-id="077ed-116">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="077ed-116">The HTTP response.</span></span>
[<span data-ttu-id="077ed-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="077ed-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="077ed-118">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="077ed-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="077ed-119">Parte</span><span class="sxs-lookup"><span data-stu-id="077ed-119">Members</span></span>

#### <span data-ttu-id="077ed-120">Solicitação</span><span class="sxs-lookup"><span data-stu-id="077ed-120">Request</span></span> 

<span data-ttu-id="077ed-121">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="077ed-121">The HTTP request.</span></span>

> <span data-ttu-id="077ed-122">[solicitação](#request) de HttpRequestMessage pública</span><span class="sxs-lookup"><span data-stu-id="077ed-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="077ed-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="077ed-123">ResourceContext</span></span> 

<span data-ttu-id="077ed-124">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="077ed-124">The web resource request contexts.</span></span>

> <span data-ttu-id="077ed-125">[CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) público [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="077ed-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="077ed-126">Resposta</span><span class="sxs-lookup"><span data-stu-id="077ed-126">Response</span></span> 

<span data-ttu-id="077ed-127">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="077ed-127">The HTTP response.</span></span>

> <span data-ttu-id="077ed-128">[resposta](#response) HttpResponseMessage pública</span><span class="sxs-lookup"><span data-stu-id="077ed-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="077ed-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="077ed-129">GetDeferral</span></span> 

<span data-ttu-id="077ed-130">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="077ed-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="077ed-131">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="077ed-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="077ed-132">Você pode usar o objeto CoreWebView2Deferral para concluir a solicitação de rede em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="077ed-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

