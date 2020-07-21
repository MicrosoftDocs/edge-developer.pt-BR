---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 61f731a948dee970731ba3dbe83426cbb40eb831
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883998"
---
# <span data-ttu-id="b643a-104">0.9.430-ICoreWebView2WebResourceResponse de interface</span><span class="sxs-lookup"><span data-stu-id="b643a-104">0.9.430 - interface ICoreWebView2WebResourceResponse</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="b643a-105">Uma resposta HTTP usada com o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="b643a-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="b643a-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="b643a-106">Summary</span></span>

 <span data-ttu-id="b643a-107">Parte</span><span class="sxs-lookup"><span data-stu-id="b643a-107">Members</span></span>                        | <span data-ttu-id="b643a-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="b643a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b643a-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="b643a-109">get_Content</span></span>](#get_content) | <span data-ttu-id="b643a-110">Conteúdo da resposta HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="b643a-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="b643a-111">put_Content</span><span class="sxs-lookup"><span data-stu-id="b643a-111">put_Content</span></span>](#put_content) | <span data-ttu-id="b643a-112">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="b643a-112">Set the Content property.</span></span>
[<span data-ttu-id="b643a-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="b643a-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="b643a-114">Cabeçalhos de resposta HTTP substituídos.</span><span class="sxs-lookup"><span data-stu-id="b643a-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="b643a-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="b643a-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="b643a-116">O código de status de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="b643a-116">The HTTP response status code.</span></span>
[<span data-ttu-id="b643a-117">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="b643a-117">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="b643a-118">Defina a propriedade StatusCode.</span><span class="sxs-lookup"><span data-stu-id="b643a-118">Set the StatusCode property.</span></span>
[<span data-ttu-id="b643a-119">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="b643a-119">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="b643a-120">A frase de motivo da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="b643a-120">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="b643a-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="b643a-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="b643a-122">Defina a propriedade ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="b643a-122">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="b643a-123">Parte</span><span class="sxs-lookup"><span data-stu-id="b643a-123">Members</span></span>

#### <span data-ttu-id="b643a-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="b643a-124">get_Content</span></span> 

<span data-ttu-id="b643a-125">Conteúdo da resposta HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="b643a-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="b643a-126">[get_Content](#get_content)público HRESULT (conteúdo IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="b643a-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="b643a-127">Stream deve ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested da resposta é concluído.</span><span class="sxs-lookup"><span data-stu-id="b643a-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="b643a-128">Stream deve ser ágil ou ser criado a partir de um thread de segundo plano para evitar o impacto de desempenho no thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b643a-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="b643a-129">NULL significa sem dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b643a-129">Null means no content data.</span></span> <span data-ttu-id="b643a-130">Semântica de IStream se aplica (retornar S_OK para ler chamadas até que todos os dados tenham esgotado)</span><span class="sxs-lookup"><span data-stu-id="b643a-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="b643a-131">put_Content</span><span class="sxs-lookup"><span data-stu-id="b643a-131">put_Content</span></span> 

<span data-ttu-id="b643a-132">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="b643a-132">Set the Content property.</span></span>

> <span data-ttu-id="b643a-133">[put_Content](#put_content)público HRESULT (conteúdo IStream \*)</span><span class="sxs-lookup"><span data-stu-id="b643a-133">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="b643a-134">get_Headers</span><span class="sxs-lookup"><span data-stu-id="b643a-134">get_Headers</span></span> 

<span data-ttu-id="b643a-135">Cabeçalhos de resposta HTTP substituídos.</span><span class="sxs-lookup"><span data-stu-id="b643a-135">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="b643a-136">público HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \* \* cabeçalhos)</span><span class="sxs-lookup"><span data-stu-id="b643a-136">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="b643a-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="b643a-137">get_StatusCode</span></span> 

<span data-ttu-id="b643a-138">O código de status de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="b643a-138">The HTTP response status code.</span></span>

> <span data-ttu-id="b643a-139">[get_StatusCode](#get_statuscode)público HRESULT (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="b643a-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="b643a-140">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="b643a-140">put_StatusCode</span></span> 

<span data-ttu-id="b643a-141">Defina a propriedade StatusCode.</span><span class="sxs-lookup"><span data-stu-id="b643a-141">Set the StatusCode property.</span></span>

> <span data-ttu-id="b643a-142">[put_StatusCode](#put_statuscode)público HRESULT (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="b643a-142">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="b643a-143">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="b643a-143">get_ReasonPhrase</span></span> 

<span data-ttu-id="b643a-144">A frase de motivo da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="b643a-144">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="b643a-145">público HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="b643a-145">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="b643a-146">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="b643a-146">put_ReasonPhrase</span></span> 

<span data-ttu-id="b643a-147">Defina a propriedade ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="b643a-147">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="b643a-148">Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="b643a-148">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

