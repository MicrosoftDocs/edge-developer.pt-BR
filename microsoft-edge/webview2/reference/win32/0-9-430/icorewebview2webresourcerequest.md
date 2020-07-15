---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: a2ac747a9981b3d44e8dbddd390bbb9b72690105
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880133"
---
# <span data-ttu-id="49636-104">0.9.430-ICoreWebView2WebResourceRequest de interface</span><span class="sxs-lookup"><span data-stu-id="49636-104">0.9.430 - interface ICoreWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="49636-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="49636-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="49636-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="49636-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="49636-107">Uma solicitação HTTP usada com o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="49636-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="49636-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="49636-108">Summary</span></span>

 <span data-ttu-id="49636-109">Parte</span><span class="sxs-lookup"><span data-stu-id="49636-109">Members</span></span>                        | <span data-ttu-id="49636-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="49636-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="49636-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="49636-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="49636-112">O URI da solicitação.</span><span class="sxs-lookup"><span data-stu-id="49636-112">The request URI.</span></span>
[<span data-ttu-id="49636-113">put_Uri</span><span class="sxs-lookup"><span data-stu-id="49636-113">put_Uri</span></span>](#put_uri) | <span data-ttu-id="49636-114">Defina a propriedade URI.</span><span class="sxs-lookup"><span data-stu-id="49636-114">Set the Uri property.</span></span>
[<span data-ttu-id="49636-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="49636-115">get_Method</span></span>](#get_method) | <span data-ttu-id="49636-116">O método de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="49636-116">The HTTP request method.</span></span>
[<span data-ttu-id="49636-117">put_Method</span><span class="sxs-lookup"><span data-stu-id="49636-117">put_Method</span></span>](#put_method) | <span data-ttu-id="49636-118">Defina a Propriedade Method.</span><span class="sxs-lookup"><span data-stu-id="49636-118">Set the Method property.</span></span>
[<span data-ttu-id="49636-119">get_Content</span><span class="sxs-lookup"><span data-stu-id="49636-119">get_Content</span></span>](#get_content) | <span data-ttu-id="49636-120">O corpo da mensagem de solicitação HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="49636-120">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="49636-121">put_Content</span><span class="sxs-lookup"><span data-stu-id="49636-121">put_Content</span></span>](#put_content) | <span data-ttu-id="49636-122">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="49636-122">Set the Content property.</span></span>
[<span data-ttu-id="49636-123">get_Headers</span><span class="sxs-lookup"><span data-stu-id="49636-123">get_Headers</span></span>](#get_headers) | <span data-ttu-id="49636-124">Os cabeçalhos de solicitação HTTP mutável.</span><span class="sxs-lookup"><span data-stu-id="49636-124">The mutable HTTP request headers.</span></span>

## <span data-ttu-id="49636-125">Parte</span><span class="sxs-lookup"><span data-stu-id="49636-125">Members</span></span>

#### <span data-ttu-id="49636-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="49636-126">get_Uri</span></span> 

<span data-ttu-id="49636-127">O URI da solicitação.</span><span class="sxs-lookup"><span data-stu-id="49636-127">The request URI.</span></span>

> <span data-ttu-id="49636-128">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="49636-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="49636-129">put_Uri</span><span class="sxs-lookup"><span data-stu-id="49636-129">put_Uri</span></span> 

<span data-ttu-id="49636-130">Defina a propriedade URI.</span><span class="sxs-lookup"><span data-stu-id="49636-130">Set the Uri property.</span></span>

> <span data-ttu-id="49636-131">[put_Uri](#put_uri)público HRESULT (URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="49636-131">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

#### <span data-ttu-id="49636-132">get_Method</span><span class="sxs-lookup"><span data-stu-id="49636-132">get_Method</span></span> 

<span data-ttu-id="49636-133">O método de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="49636-133">The HTTP request method.</span></span>

> <span data-ttu-id="49636-134">[get_Method](#get_method)público HRESULT (método LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="49636-134">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="49636-135">put_Method</span><span class="sxs-lookup"><span data-stu-id="49636-135">put_Method</span></span> 

<span data-ttu-id="49636-136">Defina a Propriedade Method.</span><span class="sxs-lookup"><span data-stu-id="49636-136">Set the Method property.</span></span>

> <span data-ttu-id="49636-137">[put_Method](#put_method)público HRESULT (método LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="49636-137">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="49636-138">get_Content</span><span class="sxs-lookup"><span data-stu-id="49636-138">get_Content</span></span> 

<span data-ttu-id="49636-139">O corpo da mensagem de solicitação HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="49636-139">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="49636-140">[get_Content](#get_content)público HRESULT (conteúdo IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="49636-140">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="49636-141">PUBLICAR dados seria aqui.</span><span class="sxs-lookup"><span data-stu-id="49636-141">POST data would be here.</span></span> <span data-ttu-id="49636-142">Se um fluxo for definido, o que substituirá o corpo da mensagem, o fluxo deverá ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested desta resposta estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="49636-142">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="49636-143">Stream deve ser ágil ou ser criado a partir de um STA em segundo plano para evitar o impacto no desempenho do thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="49636-143">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="49636-144">NULL significa sem dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="49636-144">Null means no content data.</span></span> <span data-ttu-id="49636-145">Semântica de IStream se aplica (retornar S_OK para ler chamadas até que todos os dados tenham esgotado)</span><span class="sxs-lookup"><span data-stu-id="49636-145">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="49636-146">put_Content</span><span class="sxs-lookup"><span data-stu-id="49636-146">put_Content</span></span> 

<span data-ttu-id="49636-147">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="49636-147">Set the Content property.</span></span>

> <span data-ttu-id="49636-148">[put_Content](#put_content)público HRESULT (conteúdo IStream \*)</span><span class="sxs-lookup"><span data-stu-id="49636-148">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="49636-149">get_Headers</span><span class="sxs-lookup"><span data-stu-id="49636-149">get_Headers</span></span> 

<span data-ttu-id="49636-150">Os cabeçalhos de solicitação HTTP mutável.</span><span class="sxs-lookup"><span data-stu-id="49636-150">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="49636-151">público HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \* cabeçalhos)</span><span class="sxs-lookup"><span data-stu-id="49636-151">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* headers)</span></span>

