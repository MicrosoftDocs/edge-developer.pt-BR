---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest
ms.openlocfilehash: 5c8d164b24995cc31070232dd9b1a2d88fc16cec
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011463"
---
# <span data-ttu-id="25082-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="25082-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest class</span></span> 

<span data-ttu-id="25082-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="25082-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="25082-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="25082-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="25082-107">Uma solicitação HTTP usada com o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="25082-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="25082-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="25082-108">Summary</span></span>

 <span data-ttu-id="25082-109">Parte</span><span class="sxs-lookup"><span data-stu-id="25082-109">Members</span></span>                        | <span data-ttu-id="25082-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="25082-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="25082-111">Conteúdo</span><span class="sxs-lookup"><span data-stu-id="25082-111">Content</span></span>](#content) | <span data-ttu-id="25082-112">O corpo da mensagem de solicitação HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="25082-112">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="25082-113">Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="25082-113">Headers</span></span>](#headers) | <span data-ttu-id="25082-114">Os cabeçalhos de solicitação HTTP mutável.</span><span class="sxs-lookup"><span data-stu-id="25082-114">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="25082-115">Método</span><span class="sxs-lookup"><span data-stu-id="25082-115">Method</span></span>](#method) | <span data-ttu-id="25082-116">O método de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="25082-116">The HTTP request method.</span></span>
[<span data-ttu-id="25082-117">Uri</span><span class="sxs-lookup"><span data-stu-id="25082-117">Uri</span></span>](#uri) | <span data-ttu-id="25082-118">O URI da solicitação.</span><span class="sxs-lookup"><span data-stu-id="25082-118">The request URI.</span></span>

## <span data-ttu-id="25082-119">Parte</span><span class="sxs-lookup"><span data-stu-id="25082-119">Members</span></span>

#### <span data-ttu-id="25082-120">Conteúdo</span><span class="sxs-lookup"><span data-stu-id="25082-120">Content</span></span> 

<span data-ttu-id="25082-121">O corpo da mensagem de solicitação HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="25082-121">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="25082-122">[conteúdo](#content) do fluxo público</span><span class="sxs-lookup"><span data-stu-id="25082-122">public Stream [Content](#content)</span></span>

<span data-ttu-id="25082-123">PUBLICAR dados seria aqui.</span><span class="sxs-lookup"><span data-stu-id="25082-123">POST data would be here.</span></span> <span data-ttu-id="25082-124">Se um fluxo for definido, o que substituirá o corpo da mensagem, o fluxo deverá ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested desta resposta estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="25082-124">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="25082-125">Stream deve ser ágil ou ser criado a partir de um STA em segundo plano para evitar o impacto no desempenho do thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="25082-125">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="25082-126">NULL significa sem dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="25082-126">Null means no content data.</span></span> <span data-ttu-id="25082-127">Semântica de IStream se aplica (retorna S_OK para ler chamadas até que todos os dados sejam esgotados).</span><span class="sxs-lookup"><span data-stu-id="25082-127">IStream semantics apply (return S_OK to Read calls until all data is exhausted).</span></span>

#### <span data-ttu-id="25082-128">Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="25082-128">Headers</span></span> 

<span data-ttu-id="25082-129">Os cabeçalhos de solicitação HTTP mutável.</span><span class="sxs-lookup"><span data-stu-id="25082-129">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="25082-130">cabeçalhos [CoreWebView2HttpRequestHeaders](microsoft-web-webview2-core-corewebview2httprequestheaders.md) [Headers](#headers) públicos</span><span class="sxs-lookup"><span data-stu-id="25082-130">public [CoreWebView2HttpRequestHeaders](microsoft-web-webview2-core-corewebview2httprequestheaders.md) [Headers](#headers)</span></span>

#### <span data-ttu-id="25082-131">Método</span><span class="sxs-lookup"><span data-stu-id="25082-131">Method</span></span> 

<span data-ttu-id="25082-132">O método de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="25082-132">The HTTP request method.</span></span>

> <span data-ttu-id="25082-133">[método](#method) de cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="25082-133">public string [Method](#method)</span></span>

#### <span data-ttu-id="25082-134">Uri</span><span class="sxs-lookup"><span data-stu-id="25082-134">Uri</span></span> 

<span data-ttu-id="25082-135">O URI da solicitação.</span><span class="sxs-lookup"><span data-stu-id="25082-135">The request URI.</span></span>

> <span data-ttu-id="25082-136">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="25082-136">public string [Uri](#uri)</span></span>

