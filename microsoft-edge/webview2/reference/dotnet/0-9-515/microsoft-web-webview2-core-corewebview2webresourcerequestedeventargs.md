---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 656510998879e77c2e7797c700dacc5966299210
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884649"
---
# <span data-ttu-id="06026-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="06026-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="06026-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="06026-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="06026-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="06026-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="06026-107">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="06026-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="06026-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="06026-108">Summary</span></span>

 <span data-ttu-id="06026-109">Parte</span><span class="sxs-lookup"><span data-stu-id="06026-109">Members</span></span>                        | <span data-ttu-id="06026-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="06026-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="06026-111">Solicitação</span><span class="sxs-lookup"><span data-stu-id="06026-111">Request</span></span>](#request) | <span data-ttu-id="06026-112">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="06026-112">The HTTP request.</span></span>
[<span data-ttu-id="06026-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="06026-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="06026-114">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="06026-114">The web resource request contexts.</span></span>
[<span data-ttu-id="06026-115">Resposta</span><span class="sxs-lookup"><span data-stu-id="06026-115">Response</span></span>](#response) | <span data-ttu-id="06026-116">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="06026-116">The HTTP response.</span></span>
[<span data-ttu-id="06026-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="06026-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="06026-118">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="06026-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="06026-119">Parte</span><span class="sxs-lookup"><span data-stu-id="06026-119">Members</span></span>

#### <span data-ttu-id="06026-120">Solicitação</span><span class="sxs-lookup"><span data-stu-id="06026-120">Request</span></span> 

<span data-ttu-id="06026-121">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="06026-121">The HTTP request.</span></span>

> <span data-ttu-id="06026-122">[solicitação](#request) de HttpRequestMessage pública</span><span class="sxs-lookup"><span data-stu-id="06026-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="06026-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="06026-123">ResourceContext</span></span> 

<span data-ttu-id="06026-124">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="06026-124">The web resource request contexts.</span></span>

> <span data-ttu-id="06026-125">[CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) público [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="06026-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="06026-126">Resposta</span><span class="sxs-lookup"><span data-stu-id="06026-126">Response</span></span> 

<span data-ttu-id="06026-127">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="06026-127">The HTTP response.</span></span>

> <span data-ttu-id="06026-128">[resposta](#response) HttpResponseMessage pública</span><span class="sxs-lookup"><span data-stu-id="06026-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="06026-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="06026-129">GetDeferral</span></span> 

<span data-ttu-id="06026-130">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="06026-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="06026-131">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="06026-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="06026-132">Você pode usar o objeto CoreWebView2Deferral para concluir a solicitação de rede em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="06026-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

