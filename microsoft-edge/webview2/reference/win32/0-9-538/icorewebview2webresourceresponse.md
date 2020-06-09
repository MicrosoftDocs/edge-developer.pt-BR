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
ms.openlocfilehash: 7072a25636efb638fcb42c593aa6cc77e990965a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698319"
---
# <span data-ttu-id="6877e-104">interface ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="6877e-104">interface ICoreWebView2WebResourceResponse</span></span> 

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="6877e-105">Uma resposta HTTP usada com o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="6877e-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="6877e-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="6877e-106">Summary</span></span>

 <span data-ttu-id="6877e-107">Parte</span><span class="sxs-lookup"><span data-stu-id="6877e-107">Members</span></span>                        | <span data-ttu-id="6877e-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="6877e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6877e-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="6877e-109">get_Content</span></span>](#get_content) | <span data-ttu-id="6877e-110">Conteúdo da resposta HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="6877e-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="6877e-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="6877e-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="6877e-112">Cabeçalhos de resposta HTTP substituídos.</span><span class="sxs-lookup"><span data-stu-id="6877e-112">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="6877e-113">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="6877e-113">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="6877e-114">A frase de motivo da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="6877e-114">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="6877e-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="6877e-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="6877e-116">O código de status de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="6877e-116">The HTTP response status code.</span></span>
[<span data-ttu-id="6877e-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="6877e-117">put_Content</span></span>](#put_content) | <span data-ttu-id="6877e-118">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="6877e-118">Set the Content property.</span></span>
[<span data-ttu-id="6877e-119">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="6877e-119">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="6877e-120">Defina a propriedade ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="6877e-120">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="6877e-121">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="6877e-121">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="6877e-122">Defina a propriedade StatusCode.</span><span class="sxs-lookup"><span data-stu-id="6877e-122">Set the StatusCode property.</span></span>

## <span data-ttu-id="6877e-123">Parte</span><span class="sxs-lookup"><span data-stu-id="6877e-123">Members</span></span>

#### <span data-ttu-id="6877e-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="6877e-124">get_Content</span></span> 

<span data-ttu-id="6877e-125">Conteúdo da resposta HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="6877e-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="6877e-126">[get_Content](#get_content)público HRESULT (conteúdo IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="6877e-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="6877e-127">Stream deve ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested da resposta é concluído.</span><span class="sxs-lookup"><span data-stu-id="6877e-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="6877e-128">Stream deve ser ágil ou ser criado a partir de um thread de segundo plano para evitar o impacto de desempenho no thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6877e-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="6877e-129">NULL significa sem dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6877e-129">Null means no content data.</span></span> <span data-ttu-id="6877e-130">Semântica de IStream se aplica (retornar S_OK para ler chamadas até que todos os dados tenham esgotado)</span><span class="sxs-lookup"><span data-stu-id="6877e-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="6877e-131">get_Headers</span><span class="sxs-lookup"><span data-stu-id="6877e-131">get_Headers</span></span> 

<span data-ttu-id="6877e-132">Cabeçalhos de resposta HTTP substituídos.</span><span class="sxs-lookup"><span data-stu-id="6877e-132">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="6877e-133">público HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \* cabeçalhos)</span><span class="sxs-lookup"><span data-stu-id="6877e-133">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="6877e-134">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="6877e-134">get_ReasonPhrase</span></span> 

<span data-ttu-id="6877e-135">A frase de motivo da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="6877e-135">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="6877e-136">público HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="6877e-136">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="6877e-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="6877e-137">get_StatusCode</span></span> 

<span data-ttu-id="6877e-138">O código de status de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="6877e-138">The HTTP response status code.</span></span>

> <span data-ttu-id="6877e-139">[get_StatusCode](#get_statuscode)público HRESULT (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="6877e-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="6877e-140">put_Content</span><span class="sxs-lookup"><span data-stu-id="6877e-140">put_Content</span></span> 

<span data-ttu-id="6877e-141">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="6877e-141">Set the Content property.</span></span>

> <span data-ttu-id="6877e-142">[put_Content](#put_content)público HRESULT (conteúdo IStream \*)</span><span class="sxs-lookup"><span data-stu-id="6877e-142">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="6877e-143">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="6877e-143">put_ReasonPhrase</span></span> 

<span data-ttu-id="6877e-144">Defina a propriedade ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="6877e-144">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="6877e-145">Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="6877e-145">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="6877e-146">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="6877e-146">put_StatusCode</span></span> 

<span data-ttu-id="6877e-147">Defina a propriedade StatusCode.</span><span class="sxs-lookup"><span data-stu-id="6877e-147">Set the StatusCode property.</span></span>

> <span data-ttu-id="6877e-148">[put_StatusCode](#put_statuscode)público HRESULT (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="6877e-148">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

