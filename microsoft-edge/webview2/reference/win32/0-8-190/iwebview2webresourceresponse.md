---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 95c0a881a8a201d21ca9cb2662c282b36efa2ed3
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878103"
---
# <span data-ttu-id="bebac-104">0.8.355-IWebView2WebResourceResponse de interface</span><span class="sxs-lookup"><span data-stu-id="bebac-104">0.8.355 - interface IWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="bebac-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="bebac-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="bebac-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="bebac-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="bebac-107">Uma resposta HTTP usada com o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="bebac-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="bebac-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="bebac-108">Summary</span></span>

 <span data-ttu-id="bebac-109">Parte</span><span class="sxs-lookup"><span data-stu-id="bebac-109">Members</span></span>                        | <span data-ttu-id="bebac-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="bebac-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bebac-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="bebac-111">get_Content</span></span>](#get_content) | <span data-ttu-id="bebac-112">Conteúdo da resposta HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="bebac-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="bebac-113">put_Content</span><span class="sxs-lookup"><span data-stu-id="bebac-113">put_Content</span></span>](#put_content) | <span data-ttu-id="bebac-114">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="bebac-114">Set the Content property.</span></span>
[<span data-ttu-id="bebac-115">get_Headers</span><span class="sxs-lookup"><span data-stu-id="bebac-115">get_Headers</span></span>](#get_headers) | <span data-ttu-id="bebac-116">Cabeçalhos de resposta HTTP substituídos.</span><span class="sxs-lookup"><span data-stu-id="bebac-116">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="bebac-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="bebac-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="bebac-118">O código de status de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="bebac-118">The HTTP response status code.</span></span>
[<span data-ttu-id="bebac-119">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="bebac-119">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="bebac-120">Defina a propriedade StatusCode.</span><span class="sxs-lookup"><span data-stu-id="bebac-120">Set the StatusCode property.</span></span>
[<span data-ttu-id="bebac-121">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="bebac-121">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="bebac-122">A frase de motivo da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="bebac-122">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="bebac-123">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="bebac-123">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="bebac-124">Defina a propriedade ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="bebac-124">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="bebac-125">Parte</span><span class="sxs-lookup"><span data-stu-id="bebac-125">Members</span></span>

#### <span data-ttu-id="bebac-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="bebac-126">get_Content</span></span> 

<span data-ttu-id="bebac-127">Conteúdo da resposta HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="bebac-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="bebac-128">[get_Content](#get_content)público HRESULT (conteúdo IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="bebac-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="bebac-129">Stream deve ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested da resposta é concluído.</span><span class="sxs-lookup"><span data-stu-id="bebac-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="bebac-130">Stream deve ser ágil ou ser criado a partir de um thread de segundo plano para evitar o impacto de desempenho no thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="bebac-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="bebac-131">NULL significa sem dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="bebac-131">Null means no content data.</span></span> <span data-ttu-id="bebac-132">Semântica de IStream se aplica (retornar S_OK para ler chamadas até que todos os dados tenham esgotado)</span><span class="sxs-lookup"><span data-stu-id="bebac-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="bebac-133">put_Content</span><span class="sxs-lookup"><span data-stu-id="bebac-133">put_Content</span></span> 

<span data-ttu-id="bebac-134">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="bebac-134">Set the Content property.</span></span>

> <span data-ttu-id="bebac-135">[put_Content](#put_content)público HRESULT (conteúdo IStream \*)</span><span class="sxs-lookup"><span data-stu-id="bebac-135">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="bebac-136">get_Headers</span><span class="sxs-lookup"><span data-stu-id="bebac-136">get_Headers</span></span> 

<span data-ttu-id="bebac-137">Cabeçalhos de resposta HTTP substituídos.</span><span class="sxs-lookup"><span data-stu-id="bebac-137">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="bebac-138">público HRESULT [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \* \* cabeçalhos)</span><span class="sxs-lookup"><span data-stu-id="bebac-138">public HRESULT [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="bebac-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="bebac-139">get_StatusCode</span></span> 

<span data-ttu-id="bebac-140">O código de status de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="bebac-140">The HTTP response status code.</span></span>

> <span data-ttu-id="bebac-141">[get_StatusCode](#get_statuscode)público HRESULT (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="bebac-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="bebac-142">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="bebac-142">put_StatusCode</span></span> 

<span data-ttu-id="bebac-143">Defina a propriedade StatusCode.</span><span class="sxs-lookup"><span data-stu-id="bebac-143">Set the StatusCode property.</span></span>

> <span data-ttu-id="bebac-144">[put_StatusCode](#put_statuscode)público HRESULT (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="bebac-144">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="bebac-145">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="bebac-145">get_ReasonPhrase</span></span> 

<span data-ttu-id="bebac-146">A frase de motivo da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="bebac-146">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="bebac-147">público HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="bebac-147">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="bebac-148">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="bebac-148">put_ReasonPhrase</span></span> 

<span data-ttu-id="bebac-149">Defina a propriedade ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="bebac-149">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="bebac-150">Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="bebac-150">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

