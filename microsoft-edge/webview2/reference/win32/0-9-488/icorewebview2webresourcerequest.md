---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: cdea3b4d4643e6f14e546eb9edd27bf1534beadd
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877347"
---
# <span data-ttu-id="9d439-104">0.9.515-ICoreWebView2WebResourceRequest de interface</span><span class="sxs-lookup"><span data-stu-id="9d439-104">0.9.515 - interface ICoreWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="9d439-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="9d439-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="9d439-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="9d439-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="9d439-107">Uma solicitação HTTP usada com o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9d439-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="9d439-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="9d439-108">Summary</span></span>

 <span data-ttu-id="9d439-109">Parte</span><span class="sxs-lookup"><span data-stu-id="9d439-109">Members</span></span>                        | <span data-ttu-id="9d439-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="9d439-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9d439-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="9d439-111">get_Content</span></span>](#get_content) | <span data-ttu-id="9d439-112">O corpo da mensagem de solicitação HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="9d439-112">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="9d439-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="9d439-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="9d439-114">Os cabeçalhos de solicitação HTTP mutável.</span><span class="sxs-lookup"><span data-stu-id="9d439-114">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="9d439-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="9d439-115">get_Method</span></span>](#get_method) | <span data-ttu-id="9d439-116">O método de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="9d439-116">The HTTP request method.</span></span>
[<span data-ttu-id="9d439-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="9d439-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="9d439-118">O URI da solicitação.</span><span class="sxs-lookup"><span data-stu-id="9d439-118">The request URI.</span></span>
[<span data-ttu-id="9d439-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="9d439-119">put_Content</span></span>](#put_content) | <span data-ttu-id="9d439-120">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="9d439-120">Set the Content property.</span></span>
[<span data-ttu-id="9d439-121">put_Method</span><span class="sxs-lookup"><span data-stu-id="9d439-121">put_Method</span></span>](#put_method) | <span data-ttu-id="9d439-122">Defina a Propriedade Method.</span><span class="sxs-lookup"><span data-stu-id="9d439-122">Set the Method property.</span></span>
[<span data-ttu-id="9d439-123">put_Uri</span><span class="sxs-lookup"><span data-stu-id="9d439-123">put_Uri</span></span>](#put_uri) | <span data-ttu-id="9d439-124">Defina a propriedade URI.</span><span class="sxs-lookup"><span data-stu-id="9d439-124">Set the Uri property.</span></span>

## <span data-ttu-id="9d439-125">Parte</span><span class="sxs-lookup"><span data-stu-id="9d439-125">Members</span></span>

#### <span data-ttu-id="9d439-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="9d439-126">get_Content</span></span> 

<span data-ttu-id="9d439-127">O corpo da mensagem de solicitação HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="9d439-127">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="9d439-128">[get_Content](#get_content)público HRESULT (conteúdo IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="9d439-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="9d439-129">PUBLICAR dados seria aqui.</span><span class="sxs-lookup"><span data-stu-id="9d439-129">POST data would be here.</span></span> <span data-ttu-id="9d439-130">Se um fluxo for definido, o que substituirá o corpo da mensagem, o fluxo deverá ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested desta resposta estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="9d439-130">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="9d439-131">Stream deve ser ágil ou ser criado a partir de um STA em segundo plano para evitar o impacto no desempenho do thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="9d439-131">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="9d439-132">NULL significa sem dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="9d439-132">Null means no content data.</span></span> <span data-ttu-id="9d439-133">Semântica de IStream se aplica (retornar S_OK para ler chamadas até que todos os dados tenham esgotado)</span><span class="sxs-lookup"><span data-stu-id="9d439-133">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="9d439-134">get_Headers</span><span class="sxs-lookup"><span data-stu-id="9d439-134">get_Headers</span></span> 

<span data-ttu-id="9d439-135">Os cabeçalhos de solicitação HTTP mutável.</span><span class="sxs-lookup"><span data-stu-id="9d439-135">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="9d439-136">público HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* cabeçalhos)</span><span class="sxs-lookup"><span data-stu-id="9d439-136">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="9d439-137">get_Method</span><span class="sxs-lookup"><span data-stu-id="9d439-137">get_Method</span></span> 

<span data-ttu-id="9d439-138">O método de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="9d439-138">The HTTP request method.</span></span>

> <span data-ttu-id="9d439-139">[get_Method](#get_method)público HRESULT (método LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="9d439-139">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="9d439-140">get_Uri</span><span class="sxs-lookup"><span data-stu-id="9d439-140">get_Uri</span></span> 

<span data-ttu-id="9d439-141">O URI da solicitação.</span><span class="sxs-lookup"><span data-stu-id="9d439-141">The request URI.</span></span>

> <span data-ttu-id="9d439-142">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="9d439-142">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="9d439-143">put_Content</span><span class="sxs-lookup"><span data-stu-id="9d439-143">put_Content</span></span> 

<span data-ttu-id="9d439-144">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="9d439-144">Set the Content property.</span></span>

> <span data-ttu-id="9d439-145">[put_Content](#put_content)público HRESULT (conteúdo IStream \*)</span><span class="sxs-lookup"><span data-stu-id="9d439-145">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="9d439-146">put_Method</span><span class="sxs-lookup"><span data-stu-id="9d439-146">put_Method</span></span> 

<span data-ttu-id="9d439-147">Defina a Propriedade Method.</span><span class="sxs-lookup"><span data-stu-id="9d439-147">Set the Method property.</span></span>

> <span data-ttu-id="9d439-148">[put_Method](#put_method)público HRESULT (método LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="9d439-148">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="9d439-149">put_Uri</span><span class="sxs-lookup"><span data-stu-id="9d439-149">put_Uri</span></span> 

<span data-ttu-id="9d439-150">Defina a propriedade URI.</span><span class="sxs-lookup"><span data-stu-id="9d439-150">Set the Uri property.</span></span>

> <span data-ttu-id="9d439-151">[put_Uri](#put_uri)público HRESULT (URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="9d439-151">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

