---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: ca7063ff1cd527032e9548d22a0346f8d1590480
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885699"
---
# <span data-ttu-id="48719-104">0.9.430-ICoreWebView2WebResourceRequest de interface</span><span class="sxs-lookup"><span data-stu-id="48719-104">0.9.430 - interface ICoreWebView2WebResourceRequest</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="48719-105">Uma solicitação HTTP usada com o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="48719-105">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="48719-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="48719-106">Summary</span></span>

 <span data-ttu-id="48719-107">Parte</span><span class="sxs-lookup"><span data-stu-id="48719-107">Members</span></span>                        | <span data-ttu-id="48719-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="48719-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="48719-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="48719-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="48719-110">O URI da solicitação.</span><span class="sxs-lookup"><span data-stu-id="48719-110">The request URI.</span></span>
[<span data-ttu-id="48719-111">put_Uri</span><span class="sxs-lookup"><span data-stu-id="48719-111">put_Uri</span></span>](#put_uri) | <span data-ttu-id="48719-112">Defina a propriedade URI.</span><span class="sxs-lookup"><span data-stu-id="48719-112">Set the Uri property.</span></span>
[<span data-ttu-id="48719-113">get_Method</span><span class="sxs-lookup"><span data-stu-id="48719-113">get_Method</span></span>](#get_method) | <span data-ttu-id="48719-114">O método de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="48719-114">The HTTP request method.</span></span>
[<span data-ttu-id="48719-115">put_Method</span><span class="sxs-lookup"><span data-stu-id="48719-115">put_Method</span></span>](#put_method) | <span data-ttu-id="48719-116">Defina a Propriedade Method.</span><span class="sxs-lookup"><span data-stu-id="48719-116">Set the Method property.</span></span>
[<span data-ttu-id="48719-117">get_Content</span><span class="sxs-lookup"><span data-stu-id="48719-117">get_Content</span></span>](#get_content) | <span data-ttu-id="48719-118">O corpo da mensagem de solicitação HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="48719-118">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="48719-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="48719-119">put_Content</span></span>](#put_content) | <span data-ttu-id="48719-120">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="48719-120">Set the Content property.</span></span>
[<span data-ttu-id="48719-121">get_Headers</span><span class="sxs-lookup"><span data-stu-id="48719-121">get_Headers</span></span>](#get_headers) | <span data-ttu-id="48719-122">Os cabeçalhos de solicitação HTTP mutável.</span><span class="sxs-lookup"><span data-stu-id="48719-122">The mutable HTTP request headers.</span></span>

## <span data-ttu-id="48719-123">Parte</span><span class="sxs-lookup"><span data-stu-id="48719-123">Members</span></span>

#### <span data-ttu-id="48719-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="48719-124">get_Uri</span></span> 

<span data-ttu-id="48719-125">O URI da solicitação.</span><span class="sxs-lookup"><span data-stu-id="48719-125">The request URI.</span></span>

> <span data-ttu-id="48719-126">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="48719-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="48719-127">put_Uri</span><span class="sxs-lookup"><span data-stu-id="48719-127">put_Uri</span></span> 

<span data-ttu-id="48719-128">Defina a propriedade URI.</span><span class="sxs-lookup"><span data-stu-id="48719-128">Set the Uri property.</span></span>

> <span data-ttu-id="48719-129">[put_Uri](#put_uri)público HRESULT (URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="48719-129">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

#### <span data-ttu-id="48719-130">get_Method</span><span class="sxs-lookup"><span data-stu-id="48719-130">get_Method</span></span> 

<span data-ttu-id="48719-131">O método de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="48719-131">The HTTP request method.</span></span>

> <span data-ttu-id="48719-132">[get_Method](#get_method)público HRESULT (método LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="48719-132">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="48719-133">put_Method</span><span class="sxs-lookup"><span data-stu-id="48719-133">put_Method</span></span> 

<span data-ttu-id="48719-134">Defina a Propriedade Method.</span><span class="sxs-lookup"><span data-stu-id="48719-134">Set the Method property.</span></span>

> <span data-ttu-id="48719-135">[put_Method](#put_method)público HRESULT (método LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="48719-135">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="48719-136">get_Content</span><span class="sxs-lookup"><span data-stu-id="48719-136">get_Content</span></span> 

<span data-ttu-id="48719-137">O corpo da mensagem de solicitação HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="48719-137">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="48719-138">[get_Content](#get_content)público HRESULT (conteúdo IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="48719-138">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="48719-139">PUBLICAR dados seria aqui.</span><span class="sxs-lookup"><span data-stu-id="48719-139">POST data would be here.</span></span> <span data-ttu-id="48719-140">Se um fluxo for definido, o que substituirá o corpo da mensagem, o fluxo deverá ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested desta resposta estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="48719-140">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="48719-141">Stream deve ser ágil ou ser criado a partir de um STA em segundo plano para evitar o impacto no desempenho do thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="48719-141">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="48719-142">NULL significa sem dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="48719-142">Null means no content data.</span></span> <span data-ttu-id="48719-143">Semântica de IStream se aplica (retornar S_OK para ler chamadas até que todos os dados tenham esgotado)</span><span class="sxs-lookup"><span data-stu-id="48719-143">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="48719-144">put_Content</span><span class="sxs-lookup"><span data-stu-id="48719-144">put_Content</span></span> 

<span data-ttu-id="48719-145">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="48719-145">Set the Content property.</span></span>

> <span data-ttu-id="48719-146">[put_Content](#put_content)público HRESULT (conteúdo IStream \*)</span><span class="sxs-lookup"><span data-stu-id="48719-146">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="48719-147">get_Headers</span><span class="sxs-lookup"><span data-stu-id="48719-147">get_Headers</span></span> 

<span data-ttu-id="48719-148">Os cabeçalhos de solicitação HTTP mutável.</span><span class="sxs-lookup"><span data-stu-id="48719-148">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="48719-149">público HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \* cabeçalhos)</span><span class="sxs-lookup"><span data-stu-id="48719-149">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* headers)</span></span>

