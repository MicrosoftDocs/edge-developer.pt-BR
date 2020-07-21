---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 82c94869a84165de4c3b8d09937d6ea5d1f79256
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885685"
---
# <span data-ttu-id="5fda4-104">0.8.355-IWebView2WebResourceResponse de interface</span><span class="sxs-lookup"><span data-stu-id="5fda4-104">0.8.355 - interface IWebView2WebResourceResponse</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="5fda4-105">Uma resposta HTTP usada com o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="5fda4-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="5fda4-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="5fda4-106">Summary</span></span>

 <span data-ttu-id="5fda4-107">Parte</span><span class="sxs-lookup"><span data-stu-id="5fda4-107">Members</span></span>                        | <span data-ttu-id="5fda4-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="5fda4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5fda4-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="5fda4-109">get_Content</span></span>](#get_content) | <span data-ttu-id="5fda4-110">Conteúdo da resposta HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="5fda4-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="5fda4-111">put_Content</span><span class="sxs-lookup"><span data-stu-id="5fda4-111">put_Content</span></span>](#put_content) | <span data-ttu-id="5fda4-112">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="5fda4-112">Set the Content property.</span></span>
[<span data-ttu-id="5fda4-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="5fda4-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="5fda4-114">Cabeçalhos de resposta HTTP substituídos.</span><span class="sxs-lookup"><span data-stu-id="5fda4-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="5fda4-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="5fda4-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="5fda4-116">O código de status de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="5fda4-116">The HTTP response status code.</span></span>
[<span data-ttu-id="5fda4-117">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="5fda4-117">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="5fda4-118">Defina a propriedade StatusCode.</span><span class="sxs-lookup"><span data-stu-id="5fda4-118">Set the StatusCode property.</span></span>
[<span data-ttu-id="5fda4-119">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="5fda4-119">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="5fda4-120">A frase de motivo da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="5fda4-120">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="5fda4-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="5fda4-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="5fda4-122">Defina a propriedade ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="5fda4-122">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="5fda4-123">Parte</span><span class="sxs-lookup"><span data-stu-id="5fda4-123">Members</span></span>

#### <span data-ttu-id="5fda4-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="5fda4-124">get_Content</span></span> 

<span data-ttu-id="5fda4-125">Conteúdo da resposta HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="5fda4-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="5fda4-126">[get_Content](#get_content)público HRESULT (conteúdo IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="5fda4-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="5fda4-127">Stream deve ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested da resposta é concluído.</span><span class="sxs-lookup"><span data-stu-id="5fda4-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="5fda4-128">Stream deve ser ágil ou ser criado a partir de um thread de segundo plano para evitar o impacto de desempenho no thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="5fda4-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="5fda4-129">NULL significa sem dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5fda4-129">Null means no content data.</span></span> <span data-ttu-id="5fda4-130">Semântica de IStream se aplica (retornar S_OK para ler chamadas até que todos os dados tenham esgotado)</span><span class="sxs-lookup"><span data-stu-id="5fda4-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="5fda4-131">put_Content</span><span class="sxs-lookup"><span data-stu-id="5fda4-131">put_Content</span></span> 

<span data-ttu-id="5fda4-132">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="5fda4-132">Set the Content property.</span></span>

> <span data-ttu-id="5fda4-133">[put_Content](#put_content)público HRESULT (conteúdo IStream \*)</span><span class="sxs-lookup"><span data-stu-id="5fda4-133">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="5fda4-134">get_Headers</span><span class="sxs-lookup"><span data-stu-id="5fda4-134">get_Headers</span></span> 

<span data-ttu-id="5fda4-135">Cabeçalhos de resposta HTTP substituídos.</span><span class="sxs-lookup"><span data-stu-id="5fda4-135">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="5fda4-136">público HRESULT [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \* \* cabeçalhos)</span><span class="sxs-lookup"><span data-stu-id="5fda4-136">public HRESULT [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="5fda4-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="5fda4-137">get_StatusCode</span></span> 

<span data-ttu-id="5fda4-138">O código de status de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="5fda4-138">The HTTP response status code.</span></span>

> <span data-ttu-id="5fda4-139">[get_StatusCode](#get_statuscode)público HRESULT (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="5fda4-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="5fda4-140">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="5fda4-140">put_StatusCode</span></span> 

<span data-ttu-id="5fda4-141">Defina a propriedade StatusCode.</span><span class="sxs-lookup"><span data-stu-id="5fda4-141">Set the StatusCode property.</span></span>

> <span data-ttu-id="5fda4-142">[put_StatusCode](#put_statuscode)público HRESULT (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="5fda4-142">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="5fda4-143">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="5fda4-143">get_ReasonPhrase</span></span> 

<span data-ttu-id="5fda4-144">A frase de motivo da resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="5fda4-144">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="5fda4-145">público HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="5fda4-145">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="5fda4-146">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="5fda4-146">put_ReasonPhrase</span></span> 

<span data-ttu-id="5fda4-147">Defina a propriedade ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="5fda4-147">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="5fda4-148">Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="5fda4-148">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

