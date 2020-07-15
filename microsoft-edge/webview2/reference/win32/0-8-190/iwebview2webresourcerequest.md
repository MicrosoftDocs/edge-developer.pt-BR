---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 3c9736c8b5a3cfb0de994285f3a1f90d62666fd0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878145"
---
# <span data-ttu-id="a8c27-104">0.8.355-IWebView2WebResourceRequest de interface</span><span class="sxs-lookup"><span data-stu-id="a8c27-104">0.8.355 - interface IWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="a8c27-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="a8c27-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="a8c27-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="a8c27-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="a8c27-107">Uma solicitação HTTP usada com o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="a8c27-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="a8c27-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="a8c27-108">Summary</span></span>

 <span data-ttu-id="a8c27-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a8c27-109">Members</span></span>                        | <span data-ttu-id="a8c27-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="a8c27-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a8c27-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="a8c27-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="a8c27-112">O URI da solicitação.</span><span class="sxs-lookup"><span data-stu-id="a8c27-112">The request URI.</span></span>
[<span data-ttu-id="a8c27-113">put_Uri</span><span class="sxs-lookup"><span data-stu-id="a8c27-113">put_Uri</span></span>](#put_uri) | <span data-ttu-id="a8c27-114">Defina a propriedade URI.</span><span class="sxs-lookup"><span data-stu-id="a8c27-114">Set the Uri property.</span></span>
[<span data-ttu-id="a8c27-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="a8c27-115">get_Method</span></span>](#get_method) | <span data-ttu-id="a8c27-116">O método de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="a8c27-116">The HTTP request method.</span></span>
[<span data-ttu-id="a8c27-117">put_Method</span><span class="sxs-lookup"><span data-stu-id="a8c27-117">put_Method</span></span>](#put_method) | <span data-ttu-id="a8c27-118">Defina a Propriedade Method.</span><span class="sxs-lookup"><span data-stu-id="a8c27-118">Set the Method property.</span></span>
[<span data-ttu-id="a8c27-119">get_Content</span><span class="sxs-lookup"><span data-stu-id="a8c27-119">get_Content</span></span>](#get_content) | <span data-ttu-id="a8c27-120">O corpo da mensagem de solicitação HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="a8c27-120">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="a8c27-121">put_Content</span><span class="sxs-lookup"><span data-stu-id="a8c27-121">put_Content</span></span>](#put_content) | <span data-ttu-id="a8c27-122">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="a8c27-122">Set the Content property.</span></span>
[<span data-ttu-id="a8c27-123">get_Headers</span><span class="sxs-lookup"><span data-stu-id="a8c27-123">get_Headers</span></span>](#get_headers) | <span data-ttu-id="a8c27-124">Os cabeçalhos de solicitação HTTP mutável.</span><span class="sxs-lookup"><span data-stu-id="a8c27-124">The mutable HTTP request headers.</span></span>

## <span data-ttu-id="a8c27-125">Parte</span><span class="sxs-lookup"><span data-stu-id="a8c27-125">Members</span></span>

#### <span data-ttu-id="a8c27-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="a8c27-126">get_Uri</span></span> 

<span data-ttu-id="a8c27-127">O URI da solicitação.</span><span class="sxs-lookup"><span data-stu-id="a8c27-127">The request URI.</span></span>

> <span data-ttu-id="a8c27-128">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="a8c27-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="a8c27-129">put_Uri</span><span class="sxs-lookup"><span data-stu-id="a8c27-129">put_Uri</span></span> 

<span data-ttu-id="a8c27-130">Defina a propriedade URI.</span><span class="sxs-lookup"><span data-stu-id="a8c27-130">Set the Uri property.</span></span>

> <span data-ttu-id="a8c27-131">[put_Uri](#put_uri)público HRESULT (URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="a8c27-131">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

#### <span data-ttu-id="a8c27-132">get_Method</span><span class="sxs-lookup"><span data-stu-id="a8c27-132">get_Method</span></span> 

<span data-ttu-id="a8c27-133">O método de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="a8c27-133">The HTTP request method.</span></span>

> <span data-ttu-id="a8c27-134">[get_Method](#get_method)público HRESULT (método LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="a8c27-134">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="a8c27-135">put_Method</span><span class="sxs-lookup"><span data-stu-id="a8c27-135">put_Method</span></span> 

<span data-ttu-id="a8c27-136">Defina a Propriedade Method.</span><span class="sxs-lookup"><span data-stu-id="a8c27-136">Set the Method property.</span></span>

> <span data-ttu-id="a8c27-137">[put_Method](#put_method)público HRESULT (método LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="a8c27-137">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="a8c27-138">get_Content</span><span class="sxs-lookup"><span data-stu-id="a8c27-138">get_Content</span></span> 

<span data-ttu-id="a8c27-139">O corpo da mensagem de solicitação HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="a8c27-139">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="a8c27-140">[get_Content](#get_content)público HRESULT (conteúdo IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="a8c27-140">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="a8c27-141">PUBLICAR dados seria aqui.</span><span class="sxs-lookup"><span data-stu-id="a8c27-141">POST data would be here.</span></span> <span data-ttu-id="a8c27-142">Se um fluxo for definido, o que substituirá o corpo da mensagem, o fluxo deverá ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested desta resposta estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="a8c27-142">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="a8c27-143">Stream deve ser ágil ou ser criado a partir de um STA em segundo plano para evitar o impacto no desempenho do thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a8c27-143">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="a8c27-144">NULL significa sem dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a8c27-144">Null means no content data.</span></span> <span data-ttu-id="a8c27-145">Semântica de IStream se aplica (retornar S_OK para ler chamadas até que todos os dados tenham esgotado)</span><span class="sxs-lookup"><span data-stu-id="a8c27-145">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="a8c27-146">put_Content</span><span class="sxs-lookup"><span data-stu-id="a8c27-146">put_Content</span></span> 

<span data-ttu-id="a8c27-147">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="a8c27-147">Set the Content property.</span></span>

> <span data-ttu-id="a8c27-148">[put_Content](#put_content)público HRESULT (conteúdo IStream \*)</span><span class="sxs-lookup"><span data-stu-id="a8c27-148">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="a8c27-149">get_Headers</span><span class="sxs-lookup"><span data-stu-id="a8c27-149">get_Headers</span></span> 

<span data-ttu-id="a8c27-150">Os cabeçalhos de solicitação HTTP mutável.</span><span class="sxs-lookup"><span data-stu-id="a8c27-150">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="a8c27-151">público HRESULT [get_Headers](#get_headers)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \* cabeçalhos)</span><span class="sxs-lookup"><span data-stu-id="a8c27-151">public HRESULT [get_Headers](#get_headers)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* headers)</span></span>

