---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 2282b36d3b7dfcca83f84ed50a976d4e6622ce07
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010121"
---
# <span data-ttu-id="f31c9-104">classe 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f31c9-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="f31c9-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f31c9-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f31c9-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="f31c9-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f31c9-107">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="f31c9-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="f31c9-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="f31c9-108">Summary</span></span>

 <span data-ttu-id="f31c9-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f31c9-109">Members</span></span>                        | <span data-ttu-id="f31c9-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="f31c9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f31c9-111">Solicitação</span><span class="sxs-lookup"><span data-stu-id="f31c9-111">Request</span></span>](#request) | <span data-ttu-id="f31c9-112">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="f31c9-112">The HTTP request.</span></span>
[<span data-ttu-id="f31c9-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="f31c9-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="f31c9-114">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="f31c9-114">The web resource request contexts.</span></span>
[<span data-ttu-id="f31c9-115">Resposta</span><span class="sxs-lookup"><span data-stu-id="f31c9-115">Response</span></span>](#response) | <span data-ttu-id="f31c9-116">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f31c9-116">The HTTP response.</span></span>
[<span data-ttu-id="f31c9-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f31c9-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="f31c9-118">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="f31c9-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="f31c9-119">Parte</span><span class="sxs-lookup"><span data-stu-id="f31c9-119">Members</span></span>

#### <span data-ttu-id="f31c9-120">Solicitação</span><span class="sxs-lookup"><span data-stu-id="f31c9-120">Request</span></span> 

<span data-ttu-id="f31c9-121">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="f31c9-121">The HTTP request.</span></span>

> <span data-ttu-id="f31c9-122">[solicitação](#request) de HttpRequestMessage pública</span><span class="sxs-lookup"><span data-stu-id="f31c9-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="f31c9-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="f31c9-123">ResourceContext</span></span> 

<span data-ttu-id="f31c9-124">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="f31c9-124">The web resource request contexts.</span></span>

> <span data-ttu-id="f31c9-125">[CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) público [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="f31c9-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="f31c9-126">Resposta</span><span class="sxs-lookup"><span data-stu-id="f31c9-126">Response</span></span> 

<span data-ttu-id="f31c9-127">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f31c9-127">The HTTP response.</span></span>

> <span data-ttu-id="f31c9-128">[resposta](#response) HttpResponseMessage pública</span><span class="sxs-lookup"><span data-stu-id="f31c9-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="f31c9-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f31c9-129">GetDeferral</span></span> 

<span data-ttu-id="f31c9-130">Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="f31c9-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="f31c9-131">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="f31c9-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="f31c9-132">Você pode usar o objeto CoreWebView2Deferral para concluir a solicitação de rede em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="f31c9-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

