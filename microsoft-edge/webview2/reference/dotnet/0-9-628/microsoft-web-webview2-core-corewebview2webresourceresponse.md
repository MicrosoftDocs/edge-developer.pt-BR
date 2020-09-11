---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
ms.openlocfilehash: 5359634d83717ce844d2c1604a2645ceffc477cc
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011459"
---
# <span data-ttu-id="6660f-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="6660f-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse class</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="6660f-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="6660f-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="6660f-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="6660f-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="6660f-107">Uma resposta HTTP usada com o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="6660f-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="6660f-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="6660f-108">Summary</span></span>

 <span data-ttu-id="6660f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="6660f-109">Members</span></span>                        | <span data-ttu-id="6660f-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="6660f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6660f-111">Conteúdo</span><span class="sxs-lookup"><span data-stu-id="6660f-111">Content</span></span>](#content) | <span data-ttu-id="6660f-112">Conteúdo da resposta HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="6660f-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="6660f-113">Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="6660f-113">Headers</span></span>](#headers) | <span data-ttu-id="6660f-114">Cabeçalhos de resposta HTTP substituídos.</span><span class="sxs-lookup"><span data-stu-id="6660f-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="6660f-115">ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="6660f-115">ReasonPhrase</span></span>](#reasonphrase) | <span data-ttu-id="6660f-116">A frase de motivo da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="6660f-116">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="6660f-117">StatusCode</span><span class="sxs-lookup"><span data-stu-id="6660f-117">StatusCode</span></span>](#statuscode) | <span data-ttu-id="6660f-118">O código de status de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="6660f-118">The HTTP response status code.</span></span>

## <span data-ttu-id="6660f-119">Parte</span><span class="sxs-lookup"><span data-stu-id="6660f-119">Members</span></span>

#### <span data-ttu-id="6660f-120">Conteúdo</span><span class="sxs-lookup"><span data-stu-id="6660f-120">Content</span></span> 

<span data-ttu-id="6660f-121">Conteúdo da resposta HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="6660f-121">HTTP response content as stream.</span></span>

> <span data-ttu-id="6660f-122">[conteúdo](#content) do fluxo público</span><span class="sxs-lookup"><span data-stu-id="6660f-122">public Stream [Content](#content)</span></span>

<span data-ttu-id="6660f-123">Stream deve ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested da resposta é concluído.</span><span class="sxs-lookup"><span data-stu-id="6660f-123">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="6660f-124">Stream deve ser ágil ou ser criado a partir de um thread de segundo plano para evitar o impacto de desempenho no thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6660f-124">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="6660f-125">NULL significa sem dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6660f-125">Null means no content data.</span></span> <span data-ttu-id="6660f-126">Semântica de IStream se aplica (retorna S_OK para ler chamadas até que todos os dados sejam esgotados).</span><span class="sxs-lookup"><span data-stu-id="6660f-126">IStream semantics apply (return S_OK to Read calls until all data is exhausted).</span></span>

#### <span data-ttu-id="6660f-127">Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="6660f-127">Headers</span></span> 

<span data-ttu-id="6660f-128">Cabeçalhos de resposta HTTP substituídos.</span><span class="sxs-lookup"><span data-stu-id="6660f-128">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="6660f-129">cabeçalhos [CoreWebView2HttpResponseHeaders](microsoft-web-webview2-core-corewebview2httpresponseheaders.md) [Headers](#headers) públicos</span><span class="sxs-lookup"><span data-stu-id="6660f-129">public [CoreWebView2HttpResponseHeaders](microsoft-web-webview2-core-corewebview2httpresponseheaders.md) [Headers](#headers)</span></span>

#### <span data-ttu-id="6660f-130">ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="6660f-130">ReasonPhrase</span></span> 

<span data-ttu-id="6660f-131">A frase de motivo da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="6660f-131">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="6660f-132">Cadeia de caracteres pública [ReasonPhrase](#reasonphrase)</span><span class="sxs-lookup"><span data-stu-id="6660f-132">public string [ReasonPhrase](#reasonphrase)</span></span>

#### <span data-ttu-id="6660f-133">StatusCode</span><span class="sxs-lookup"><span data-stu-id="6660f-133">StatusCode</span></span> 

<span data-ttu-id="6660f-134">O código de status de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="6660f-134">The HTTP response status code.</span></span>

> <span data-ttu-id="6660f-135">[StatusCode](#statuscode) público público</span><span class="sxs-lookup"><span data-stu-id="6660f-135">public int [StatusCode](#statuscode)</span></span>

