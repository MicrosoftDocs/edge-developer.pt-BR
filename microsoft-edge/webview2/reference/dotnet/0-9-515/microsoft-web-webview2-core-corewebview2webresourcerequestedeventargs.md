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
ms.openlocfilehash: 072ce10e7ac1f34238278366c3e8799a3268cb0b
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697529"
---
# <span data-ttu-id="e3381-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e3381-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="e3381-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="e3381-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="e3381-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="e3381-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="e3381-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="e3381-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="e3381-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="e3381-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="e3381-109">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="e3381-109">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="e3381-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="e3381-110">Summary</span></span>

 <span data-ttu-id="e3381-111">Parte</span><span class="sxs-lookup"><span data-stu-id="e3381-111">Members</span></span>                        | <span data-ttu-id="e3381-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="e3381-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e3381-113">Solicitação</span><span class="sxs-lookup"><span data-stu-id="e3381-113">Request</span></span>](#request) | <span data-ttu-id="e3381-114">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="e3381-114">The HTTP request.</span></span>
[<span data-ttu-id="e3381-115">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="e3381-115">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="e3381-116">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="e3381-116">The web resource request contexts.</span></span>
[<span data-ttu-id="e3381-117">Resposta</span><span class="sxs-lookup"><span data-stu-id="e3381-117">Response</span></span>](#response) | <span data-ttu-id="e3381-118">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="e3381-118">The HTTP response.</span></span>
[<span data-ttu-id="e3381-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e3381-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="e3381-120">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="e3381-120">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="e3381-121">Parte</span><span class="sxs-lookup"><span data-stu-id="e3381-121">Members</span></span>

#### <span data-ttu-id="e3381-122">Solicitação</span><span class="sxs-lookup"><span data-stu-id="e3381-122">Request</span></span> 

<span data-ttu-id="e3381-123">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="e3381-123">The HTTP request.</span></span>

> <span data-ttu-id="e3381-124">[solicitação](#request) de HttpRequestMessage pública</span><span class="sxs-lookup"><span data-stu-id="e3381-124">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="e3381-125">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="e3381-125">ResourceContext</span></span> 

<span data-ttu-id="e3381-126">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="e3381-126">The web resource request contexts.</span></span>

> <span data-ttu-id="e3381-127">[CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) público [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="e3381-127">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="e3381-128">Resposta</span><span class="sxs-lookup"><span data-stu-id="e3381-128">Response</span></span> 

<span data-ttu-id="e3381-129">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="e3381-129">The HTTP response.</span></span>

> <span data-ttu-id="e3381-130">[resposta](#response) HttpResponseMessage pública</span><span class="sxs-lookup"><span data-stu-id="e3381-130">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="e3381-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e3381-131">GetDeferral</span></span> 

<span data-ttu-id="e3381-132">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="e3381-132">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="e3381-133">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="e3381-133">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="e3381-134">Você pode usar o objeto CoreWebView2Deferral para concluir a solicitação de rede em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="e3381-134">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

