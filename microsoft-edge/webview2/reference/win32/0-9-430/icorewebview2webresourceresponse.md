---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 6d28a5e0b08406cdf83b7e0a60428463e9647d45
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652543"
---
# <span data-ttu-id="3d6b1-104">interface ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="3d6b1-104">interface ICoreWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="3d6b1-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="3d6b1-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="3d6b1-107">Uma resposta HTTP usada com o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="3d6b1-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="3d6b1-108">Summary</span></span>

 <span data-ttu-id="3d6b1-109">Parte</span><span class="sxs-lookup"><span data-stu-id="3d6b1-109">Members</span></span>                        | <span data-ttu-id="3d6b1-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="3d6b1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3d6b1-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="3d6b1-111">get_Content</span></span>](#get_content) | <span data-ttu-id="3d6b1-112">Conteúdo da resposta HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="3d6b1-113">put_Content</span><span class="sxs-lookup"><span data-stu-id="3d6b1-113">put_Content</span></span>](#put_content) | <span data-ttu-id="3d6b1-114">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-114">Set the Content property.</span></span>
[<span data-ttu-id="3d6b1-115">get_Headers</span><span class="sxs-lookup"><span data-stu-id="3d6b1-115">get_Headers</span></span>](#get_headers) | <span data-ttu-id="3d6b1-116">Cabeçalhos de resposta HTTP substituídos.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-116">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="3d6b1-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="3d6b1-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="3d6b1-118">O código de status de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-118">The HTTP response status code.</span></span>
[<span data-ttu-id="3d6b1-119">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="3d6b1-119">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="3d6b1-120">Defina a propriedade StatusCode.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-120">Set the StatusCode property.</span></span>
[<span data-ttu-id="3d6b1-121">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="3d6b1-121">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="3d6b1-122">A frase de motivo da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-122">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="3d6b1-123">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="3d6b1-123">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="3d6b1-124">Defina a propriedade ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-124">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="3d6b1-125">Parte</span><span class="sxs-lookup"><span data-stu-id="3d6b1-125">Members</span></span>

#### <span data-ttu-id="3d6b1-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="3d6b1-126">get_Content</span></span> 

<span data-ttu-id="3d6b1-127">Conteúdo da resposta HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="3d6b1-128">[get_Content](#get_content)público HRESULT (conteúdo IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="3d6b1-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="3d6b1-129">Stream deve ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested da resposta é concluído.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="3d6b1-130">Stream deve ser ágil ou ser criado a partir de um thread de segundo plano para evitar o impacto de desempenho no thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="3d6b1-131">NULL significa sem dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-131">Null means no content data.</span></span> <span data-ttu-id="3d6b1-132">Semântica de IStream se aplica (retornar S_OK para ler chamadas até que todos os dados tenham esgotado)</span><span class="sxs-lookup"><span data-stu-id="3d6b1-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="3d6b1-133">put_Content</span><span class="sxs-lookup"><span data-stu-id="3d6b1-133">put_Content</span></span> 

<span data-ttu-id="3d6b1-134">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-134">Set the Content property.</span></span>

> <span data-ttu-id="3d6b1-135">[put_Content](#put_content)público HRESULT (conteúdo IStream \*)</span><span class="sxs-lookup"><span data-stu-id="3d6b1-135">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="3d6b1-136">get_Headers</span><span class="sxs-lookup"><span data-stu-id="3d6b1-136">get_Headers</span></span> 

<span data-ttu-id="3d6b1-137">Cabeçalhos de resposta HTTP substituídos.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-137">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="3d6b1-138">público HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \* \* cabeçalhos)</span><span class="sxs-lookup"><span data-stu-id="3d6b1-138">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="3d6b1-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="3d6b1-139">get_StatusCode</span></span> 

<span data-ttu-id="3d6b1-140">O código de status de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-140">The HTTP response status code.</span></span>

> <span data-ttu-id="3d6b1-141">[get_StatusCode](#get_statuscode)público HRESULT (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="3d6b1-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="3d6b1-142">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="3d6b1-142">put_StatusCode</span></span> 

<span data-ttu-id="3d6b1-143">Defina a propriedade StatusCode.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-143">Set the StatusCode property.</span></span>

> <span data-ttu-id="3d6b1-144">[put_StatusCode](#put_statuscode)público HRESULT (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="3d6b1-144">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="3d6b1-145">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="3d6b1-145">get_ReasonPhrase</span></span> 

<span data-ttu-id="3d6b1-146">A frase de motivo da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-146">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="3d6b1-147">público HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="3d6b1-147">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="3d6b1-148">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="3d6b1-148">put_ReasonPhrase</span></span> 

<span data-ttu-id="3d6b1-149">Defina a propriedade ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="3d6b1-149">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="3d6b1-150">Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="3d6b1-150">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

