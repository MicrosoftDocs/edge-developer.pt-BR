---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 5b80691f0e42be4cdea7c99b165bfe9cebf632dd
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697928"
---
# <span data-ttu-id="aa516-104">interface ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="aa516-104">interface ICoreWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="aa516-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="aa516-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="aa516-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="aa516-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="aa516-107">Uma resposta HTTP usada com o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="aa516-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="aa516-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="aa516-108">Summary</span></span>

 <span data-ttu-id="aa516-109">Parte</span><span class="sxs-lookup"><span data-stu-id="aa516-109">Members</span></span>                        | <span data-ttu-id="aa516-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="aa516-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aa516-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="aa516-111">get_Content</span></span>](#get_content) | <span data-ttu-id="aa516-112">Conteúdo da resposta HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="aa516-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="aa516-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="aa516-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="aa516-114">Cabeçalhos de resposta HTTP substituídos.</span><span class="sxs-lookup"><span data-stu-id="aa516-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="aa516-115">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="aa516-115">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="aa516-116">A frase de motivo da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="aa516-116">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="aa516-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="aa516-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="aa516-118">O código de status de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="aa516-118">The HTTP response status code.</span></span>
[<span data-ttu-id="aa516-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="aa516-119">put_Content</span></span>](#put_content) | <span data-ttu-id="aa516-120">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="aa516-120">Set the Content property.</span></span>
[<span data-ttu-id="aa516-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="aa516-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="aa516-122">Defina a propriedade ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="aa516-122">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="aa516-123">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="aa516-123">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="aa516-124">Defina a propriedade StatusCode.</span><span class="sxs-lookup"><span data-stu-id="aa516-124">Set the StatusCode property.</span></span>

## <span data-ttu-id="aa516-125">Parte</span><span class="sxs-lookup"><span data-stu-id="aa516-125">Members</span></span>

#### <span data-ttu-id="aa516-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="aa516-126">get_Content</span></span> 

<span data-ttu-id="aa516-127">Conteúdo da resposta HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="aa516-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="aa516-128">[get_Content](#get_content)público HRESULT (conteúdo IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="aa516-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="aa516-129">Stream deve ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested da resposta é concluído.</span><span class="sxs-lookup"><span data-stu-id="aa516-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="aa516-130">Stream deve ser ágil ou ser criado a partir de um thread de segundo plano para evitar o impacto de desempenho no thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="aa516-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="aa516-131">NULL significa sem dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="aa516-131">Null means no content data.</span></span> <span data-ttu-id="aa516-132">Semântica de IStream se aplica (retornar S_OK para ler chamadas até que todos os dados tenham esgotado)</span><span class="sxs-lookup"><span data-stu-id="aa516-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="aa516-133">get_Headers</span><span class="sxs-lookup"><span data-stu-id="aa516-133">get_Headers</span></span> 

<span data-ttu-id="aa516-134">Cabeçalhos de resposta HTTP substituídos.</span><span class="sxs-lookup"><span data-stu-id="aa516-134">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="aa516-135">público HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \* cabeçalhos)</span><span class="sxs-lookup"><span data-stu-id="aa516-135">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="aa516-136">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="aa516-136">get_ReasonPhrase</span></span> 

<span data-ttu-id="aa516-137">A frase de motivo da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="aa516-137">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="aa516-138">público HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="aa516-138">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="aa516-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="aa516-139">get_StatusCode</span></span> 

<span data-ttu-id="aa516-140">O código de status de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="aa516-140">The HTTP response status code.</span></span>

> <span data-ttu-id="aa516-141">[get_StatusCode](#get_statuscode)público HRESULT (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="aa516-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="aa516-142">put_Content</span><span class="sxs-lookup"><span data-stu-id="aa516-142">put_Content</span></span> 

<span data-ttu-id="aa516-143">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="aa516-143">Set the Content property.</span></span>

> <span data-ttu-id="aa516-144">[put_Content](#put_content)público HRESULT (conteúdo IStream \*)</span><span class="sxs-lookup"><span data-stu-id="aa516-144">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="aa516-145">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="aa516-145">put_ReasonPhrase</span></span> 

<span data-ttu-id="aa516-146">Defina a propriedade ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="aa516-146">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="aa516-147">Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="aa516-147">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="aa516-148">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="aa516-148">put_StatusCode</span></span> 

<span data-ttu-id="aa516-149">Defina a propriedade StatusCode.</span><span class="sxs-lookup"><span data-stu-id="aa516-149">Set the StatusCode property.</span></span>

> <span data-ttu-id="aa516-150">[put_StatusCode](#put_statuscode)público HRESULT (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="aa516-150">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

