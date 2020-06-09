---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 3d85b1116a3f75058bda59f1c374700555b42a5e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698368"
---
# <span data-ttu-id="ccbdb-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ccbdb-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

<span data-ttu-id="ccbdb-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="ccbdb-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="ccbdb-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="ccbdb-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="ccbdb-107">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="ccbdb-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="ccbdb-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="ccbdb-108">Summary</span></span>

 <span data-ttu-id="ccbdb-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ccbdb-109">Members</span></span>                        | <span data-ttu-id="ccbdb-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="ccbdb-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ccbdb-111">Solicitação</span><span class="sxs-lookup"><span data-stu-id="ccbdb-111">Request</span></span>](#request) | <span data-ttu-id="ccbdb-112">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="ccbdb-112">The HTTP request.</span></span>
[<span data-ttu-id="ccbdb-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="ccbdb-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="ccbdb-114">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="ccbdb-114">The web resource request contexts.</span></span>
[<span data-ttu-id="ccbdb-115">Resposta</span><span class="sxs-lookup"><span data-stu-id="ccbdb-115">Response</span></span>](#response) | <span data-ttu-id="ccbdb-116">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="ccbdb-116">The HTTP response.</span></span>
[<span data-ttu-id="ccbdb-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ccbdb-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="ccbdb-118">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="ccbdb-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="ccbdb-119">Parte</span><span class="sxs-lookup"><span data-stu-id="ccbdb-119">Members</span></span>

#### <span data-ttu-id="ccbdb-120">Solicitação</span><span class="sxs-lookup"><span data-stu-id="ccbdb-120">Request</span></span> 

<span data-ttu-id="ccbdb-121">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="ccbdb-121">The HTTP request.</span></span>

> <span data-ttu-id="ccbdb-122">[solicitação](#request) de HttpRequestMessage pública</span><span class="sxs-lookup"><span data-stu-id="ccbdb-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="ccbdb-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="ccbdb-123">ResourceContext</span></span> 

<span data-ttu-id="ccbdb-124">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="ccbdb-124">The web resource request contexts.</span></span>

> <span data-ttu-id="ccbdb-125">[CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) público [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="ccbdb-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="ccbdb-126">Resposta</span><span class="sxs-lookup"><span data-stu-id="ccbdb-126">Response</span></span> 

<span data-ttu-id="ccbdb-127">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="ccbdb-127">The HTTP response.</span></span>

> <span data-ttu-id="ccbdb-128">[resposta](#response) HttpResponseMessage pública</span><span class="sxs-lookup"><span data-stu-id="ccbdb-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="ccbdb-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ccbdb-129">GetDeferral</span></span> 

<span data-ttu-id="ccbdb-130">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="ccbdb-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="ccbdb-131">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="ccbdb-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="ccbdb-132">Você pode usar o objeto CoreWebView2Deferral para concluir a solicitação de rede em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="ccbdb-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

