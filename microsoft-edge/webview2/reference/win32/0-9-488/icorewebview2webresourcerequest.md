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
ms.openlocfilehash: 4b76cf998f8e2fd8982f7e51f1d9167e3862ec02
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652401"
---
# <span data-ttu-id="aff82-104">interface ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="aff82-104">interface ICoreWebView2WebResourceRequest</span></span> 

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="aff82-105">Uma solicitação HTTP usada com o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="aff82-105">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="aff82-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="aff82-106">Summary</span></span>

 <span data-ttu-id="aff82-107">Parte</span><span class="sxs-lookup"><span data-stu-id="aff82-107">Members</span></span>                        | <span data-ttu-id="aff82-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="aff82-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aff82-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="aff82-109">get_Content</span></span>](#get_content) | <span data-ttu-id="aff82-110">O corpo da mensagem de solicitação HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="aff82-110">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="aff82-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="aff82-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="aff82-112">Os cabeçalhos de solicitação HTTP mutável.</span><span class="sxs-lookup"><span data-stu-id="aff82-112">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="aff82-113">get_Method</span><span class="sxs-lookup"><span data-stu-id="aff82-113">get_Method</span></span>](#get_method) | <span data-ttu-id="aff82-114">O método de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="aff82-114">The HTTP request method.</span></span>
[<span data-ttu-id="aff82-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="aff82-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="aff82-116">O URI da solicitação.</span><span class="sxs-lookup"><span data-stu-id="aff82-116">The request URI.</span></span>
[<span data-ttu-id="aff82-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="aff82-117">put_Content</span></span>](#put_content) | <span data-ttu-id="aff82-118">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="aff82-118">Set the Content property.</span></span>
[<span data-ttu-id="aff82-119">put_Method</span><span class="sxs-lookup"><span data-stu-id="aff82-119">put_Method</span></span>](#put_method) | <span data-ttu-id="aff82-120">Defina a Propriedade Method.</span><span class="sxs-lookup"><span data-stu-id="aff82-120">Set the Method property.</span></span>
[<span data-ttu-id="aff82-121">put_Uri</span><span class="sxs-lookup"><span data-stu-id="aff82-121">put_Uri</span></span>](#put_uri) | <span data-ttu-id="aff82-122">Defina a propriedade URI.</span><span class="sxs-lookup"><span data-stu-id="aff82-122">Set the Uri property.</span></span>

## <span data-ttu-id="aff82-123">Parte</span><span class="sxs-lookup"><span data-stu-id="aff82-123">Members</span></span>

#### <span data-ttu-id="aff82-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="aff82-124">get_Content</span></span> 

<span data-ttu-id="aff82-125">O corpo da mensagem de solicitação HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="aff82-125">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="aff82-126">[get_Content](#get_content)público HRESULT (conteúdo IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="aff82-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="aff82-127">PUBLICAR dados seria aqui.</span><span class="sxs-lookup"><span data-stu-id="aff82-127">POST data would be here.</span></span> <span data-ttu-id="aff82-128">Se um fluxo for definido, o que substituirá o corpo da mensagem, o fluxo deverá ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested desta resposta estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="aff82-128">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="aff82-129">Stream deve ser ágil ou ser criado a partir de um STA em segundo plano para evitar o impacto no desempenho do thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="aff82-129">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="aff82-130">NULL significa sem dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="aff82-130">Null means no content data.</span></span> <span data-ttu-id="aff82-131">Semântica de IStream se aplica (retornar S_OK para ler chamadas até que todos os dados tenham esgotado)</span><span class="sxs-lookup"><span data-stu-id="aff82-131">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="aff82-132">get_Headers</span><span class="sxs-lookup"><span data-stu-id="aff82-132">get_Headers</span></span> 

<span data-ttu-id="aff82-133">Os cabeçalhos de solicitação HTTP mutável.</span><span class="sxs-lookup"><span data-stu-id="aff82-133">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="aff82-134">público HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* cabeçalhos)</span><span class="sxs-lookup"><span data-stu-id="aff82-134">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="aff82-135">get_Method</span><span class="sxs-lookup"><span data-stu-id="aff82-135">get_Method</span></span> 

<span data-ttu-id="aff82-136">O método de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="aff82-136">The HTTP request method.</span></span>

> <span data-ttu-id="aff82-137">[get_Method](#get_method)público HRESULT (método LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="aff82-137">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="aff82-138">get_Uri</span><span class="sxs-lookup"><span data-stu-id="aff82-138">get_Uri</span></span> 

<span data-ttu-id="aff82-139">O URI da solicitação.</span><span class="sxs-lookup"><span data-stu-id="aff82-139">The request URI.</span></span>

> <span data-ttu-id="aff82-140">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="aff82-140">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="aff82-141">put_Content</span><span class="sxs-lookup"><span data-stu-id="aff82-141">put_Content</span></span> 

<span data-ttu-id="aff82-142">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="aff82-142">Set the Content property.</span></span>

> <span data-ttu-id="aff82-143">[put_Content](#put_content)público HRESULT (conteúdo IStream \*)</span><span class="sxs-lookup"><span data-stu-id="aff82-143">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="aff82-144">put_Method</span><span class="sxs-lookup"><span data-stu-id="aff82-144">put_Method</span></span> 

<span data-ttu-id="aff82-145">Defina a Propriedade Method.</span><span class="sxs-lookup"><span data-stu-id="aff82-145">Set the Method property.</span></span>

> <span data-ttu-id="aff82-146">[put_Method](#put_method)público HRESULT (método LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="aff82-146">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="aff82-147">put_Uri</span><span class="sxs-lookup"><span data-stu-id="aff82-147">put_Uri</span></span> 

<span data-ttu-id="aff82-148">Defina a propriedade URI.</span><span class="sxs-lookup"><span data-stu-id="aff82-148">Set the Uri property.</span></span>

> <span data-ttu-id="aff82-149">[put_Uri](#put_uri)público HRESULT (URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="aff82-149">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

