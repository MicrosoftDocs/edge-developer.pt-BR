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
ms.openlocfilehash: d91b7aeeebc8fd82587ac6c01fddd14e693c2559
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697060"
---
# <span data-ttu-id="28f41-104">interface ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="28f41-104">interface ICoreWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="28f41-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="28f41-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="28f41-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="28f41-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="28f41-107">Uma solicitação HTTP usada com o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="28f41-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="28f41-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="28f41-108">Summary</span></span>

 <span data-ttu-id="28f41-109">Parte</span><span class="sxs-lookup"><span data-stu-id="28f41-109">Members</span></span>                        | <span data-ttu-id="28f41-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="28f41-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="28f41-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="28f41-111">get_Content</span></span>](#get_content) | <span data-ttu-id="28f41-112">O corpo da mensagem de solicitação HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="28f41-112">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="28f41-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="28f41-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="28f41-114">Os cabeçalhos de solicitação HTTP mutável.</span><span class="sxs-lookup"><span data-stu-id="28f41-114">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="28f41-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="28f41-115">get_Method</span></span>](#get_method) | <span data-ttu-id="28f41-116">O método de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="28f41-116">The HTTP request method.</span></span>
[<span data-ttu-id="28f41-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="28f41-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="28f41-118">O URI da solicitação.</span><span class="sxs-lookup"><span data-stu-id="28f41-118">The request URI.</span></span>
[<span data-ttu-id="28f41-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="28f41-119">put_Content</span></span>](#put_content) | <span data-ttu-id="28f41-120">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="28f41-120">Set the Content property.</span></span>
[<span data-ttu-id="28f41-121">put_Method</span><span class="sxs-lookup"><span data-stu-id="28f41-121">put_Method</span></span>](#put_method) | <span data-ttu-id="28f41-122">Defina a Propriedade Method.</span><span class="sxs-lookup"><span data-stu-id="28f41-122">Set the Method property.</span></span>
[<span data-ttu-id="28f41-123">put_Uri</span><span class="sxs-lookup"><span data-stu-id="28f41-123">put_Uri</span></span>](#put_uri) | <span data-ttu-id="28f41-124">Defina a propriedade URI.</span><span class="sxs-lookup"><span data-stu-id="28f41-124">Set the Uri property.</span></span>

## <span data-ttu-id="28f41-125">Parte</span><span class="sxs-lookup"><span data-stu-id="28f41-125">Members</span></span>

#### <span data-ttu-id="28f41-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="28f41-126">get_Content</span></span> 

<span data-ttu-id="28f41-127">O corpo da mensagem de solicitação HTTP como Stream.</span><span class="sxs-lookup"><span data-stu-id="28f41-127">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="28f41-128">[get_Content](#get_content)público HRESULT (conteúdo IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="28f41-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="28f41-129">PUBLICAR dados seria aqui.</span><span class="sxs-lookup"><span data-stu-id="28f41-129">POST data would be here.</span></span> <span data-ttu-id="28f41-130">Se um fluxo for definido, o que substituirá o corpo da mensagem, o fluxo deverá ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested desta resposta estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="28f41-130">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="28f41-131">Stream deve ser ágil ou ser criado a partir de um STA em segundo plano para evitar o impacto no desempenho do thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="28f41-131">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="28f41-132">NULL significa sem dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="28f41-132">Null means no content data.</span></span> <span data-ttu-id="28f41-133">Semântica de IStream se aplica (retornar S_OK para ler chamadas até que todos os dados tenham esgotado)</span><span class="sxs-lookup"><span data-stu-id="28f41-133">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="28f41-134">get_Headers</span><span class="sxs-lookup"><span data-stu-id="28f41-134">get_Headers</span></span> 

<span data-ttu-id="28f41-135">Os cabeçalhos de solicitação HTTP mutável.</span><span class="sxs-lookup"><span data-stu-id="28f41-135">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="28f41-136">público HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* cabeçalhos)</span><span class="sxs-lookup"><span data-stu-id="28f41-136">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="28f41-137">get_Method</span><span class="sxs-lookup"><span data-stu-id="28f41-137">get_Method</span></span> 

<span data-ttu-id="28f41-138">O método de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="28f41-138">The HTTP request method.</span></span>

> <span data-ttu-id="28f41-139">[get_Method](#get_method)público HRESULT (método LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="28f41-139">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="28f41-140">get_Uri</span><span class="sxs-lookup"><span data-stu-id="28f41-140">get_Uri</span></span> 

<span data-ttu-id="28f41-141">O URI da solicitação.</span><span class="sxs-lookup"><span data-stu-id="28f41-141">The request URI.</span></span>

> <span data-ttu-id="28f41-142">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="28f41-142">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="28f41-143">put_Content</span><span class="sxs-lookup"><span data-stu-id="28f41-143">put_Content</span></span> 

<span data-ttu-id="28f41-144">Defina a propriedade Content.</span><span class="sxs-lookup"><span data-stu-id="28f41-144">Set the Content property.</span></span>

> <span data-ttu-id="28f41-145">[put_Content](#put_content)público HRESULT (conteúdo IStream \*)</span><span class="sxs-lookup"><span data-stu-id="28f41-145">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="28f41-146">put_Method</span><span class="sxs-lookup"><span data-stu-id="28f41-146">put_Method</span></span> 

<span data-ttu-id="28f41-147">Defina a Propriedade Method.</span><span class="sxs-lookup"><span data-stu-id="28f41-147">Set the Method property.</span></span>

> <span data-ttu-id="28f41-148">[put_Method](#put_method)público HRESULT (método LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="28f41-148">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="28f41-149">put_Uri</span><span class="sxs-lookup"><span data-stu-id="28f41-149">put_Uri</span></span> 

<span data-ttu-id="28f41-150">Defina a propriedade URI.</span><span class="sxs-lookup"><span data-stu-id="28f41-150">Set the Uri property.</span></span>

> <span data-ttu-id="28f41-151">[put_Uri](#put_uri)público HRESULT (URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="28f41-151">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

