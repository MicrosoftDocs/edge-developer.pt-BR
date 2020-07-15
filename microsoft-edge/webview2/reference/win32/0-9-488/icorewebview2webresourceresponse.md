---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 7a649944686df4d425141d5d22c03c5874572d1a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877340"
---
# <span data-ttu-id="66eb1-104">0.9.515-ICoreWebView2WebResourceResponse de interface</span><span class="sxs-lookup"><span data-stu-id="66eb1-104">0.9.515 - interface ICoreWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="66eb1-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="66eb1-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="66eb1-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="66eb1-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="66eb1-107">Uma resposta HTTP usada com o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="66eb1-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="66eb1-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="66eb1-108">Summary</span></span>

 <span data-ttu-id="66eb1-109">Parte</span><span class="sxs-lookup"><span data-stu-id="66eb1-109">Members</span></span>                        | <span data-ttu-id="66eb1-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="66eb1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="66eb1-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="66eb1-111">get_Content</span></span>](#get_content) | <span data-ttu-id="66eb1-112">Conteúdo da resposta HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="66eb1-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="66eb1-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="66eb1-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="66eb1-114">Cabeçalhos de resposta HTTP substituídos.</span><span class="sxs-lookup"><span data-stu-id="66eb1-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="66eb1-115">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="66eb1-115">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="66eb1-116">A frase de motivo da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="66eb1-116">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="66eb1-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="66eb1-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="66eb1-118">O código de status de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="66eb1-118">The HTTP response status code.</span></span>
[<span data-ttu-id="66eb1-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="66eb1-119">put_Content</span></span>](#put_content) | <span data-ttu-id="66eb1-120">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="66eb1-120">Set the Content property.</span></span>
[<span data-ttu-id="66eb1-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="66eb1-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="66eb1-122">Defina a propriedade ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="66eb1-122">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="66eb1-123">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="66eb1-123">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="66eb1-124">Defina a propriedade StatusCode.</span><span class="sxs-lookup"><span data-stu-id="66eb1-124">Set the StatusCode property.</span></span>

## <span data-ttu-id="66eb1-125">Parte</span><span class="sxs-lookup"><span data-stu-id="66eb1-125">Members</span></span>

#### <span data-ttu-id="66eb1-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="66eb1-126">get_Content</span></span> 

<span data-ttu-id="66eb1-127">Conteúdo da resposta HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="66eb1-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="66eb1-128">[get_Content](#get_content)público HRESULT (conteúdo IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="66eb1-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="66eb1-129">Stream deve ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested da resposta é concluído.</span><span class="sxs-lookup"><span data-stu-id="66eb1-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="66eb1-130">Stream deve ser ágil ou ser criado a partir de um thread de segundo plano para evitar o impacto de desempenho no thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="66eb1-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="66eb1-131">NULL significa sem dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="66eb1-131">Null means no content data.</span></span> <span data-ttu-id="66eb1-132">Semântica de IStream se aplica (retornar S_OK para ler chamadas até que todos os dados tenham esgotado)</span><span class="sxs-lookup"><span data-stu-id="66eb1-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="66eb1-133">get_Headers</span><span class="sxs-lookup"><span data-stu-id="66eb1-133">get_Headers</span></span> 

<span data-ttu-id="66eb1-134">Cabeçalhos de resposta HTTP substituídos.</span><span class="sxs-lookup"><span data-stu-id="66eb1-134">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="66eb1-135">público HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \* cabeçalhos)</span><span class="sxs-lookup"><span data-stu-id="66eb1-135">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="66eb1-136">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="66eb1-136">get_ReasonPhrase</span></span> 

<span data-ttu-id="66eb1-137">A frase de motivo da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="66eb1-137">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="66eb1-138">público HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="66eb1-138">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="66eb1-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="66eb1-139">get_StatusCode</span></span> 

<span data-ttu-id="66eb1-140">O código de status de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="66eb1-140">The HTTP response status code.</span></span>

> <span data-ttu-id="66eb1-141">[get_StatusCode](#get_statuscode)público HRESULT (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="66eb1-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="66eb1-142">put_Content</span><span class="sxs-lookup"><span data-stu-id="66eb1-142">put_Content</span></span> 

<span data-ttu-id="66eb1-143">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="66eb1-143">Set the Content property.</span></span>

> <span data-ttu-id="66eb1-144">[put_Content](#put_content)público HRESULT (conteúdo IStream \*)</span><span class="sxs-lookup"><span data-stu-id="66eb1-144">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="66eb1-145">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="66eb1-145">put_ReasonPhrase</span></span> 

<span data-ttu-id="66eb1-146">Defina a propriedade ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="66eb1-146">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="66eb1-147">Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="66eb1-147">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="66eb1-148">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="66eb1-148">put_StatusCode</span></span> 

<span data-ttu-id="66eb1-149">Defina a propriedade StatusCode.</span><span class="sxs-lookup"><span data-stu-id="66eb1-149">Set the StatusCode property.</span></span>

> <span data-ttu-id="66eb1-150">[put_StatusCode](#put_statuscode)público HRESULT (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="66eb1-150">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

