---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 826cdf960a20e32b8e0fa6b5a8ddad720ac137a6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877578"
---
# <span data-ttu-id="c8e8c-104">0.9.430-ICoreWebView2WebResourceRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="c8e8c-104">0.9.430 - interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="c8e8c-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="c8e8c-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="c8e8c-107">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="c8e8c-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="c8e8c-108">Summary</span></span>

 <span data-ttu-id="c8e8c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c8e8c-109">Members</span></span>                        | <span data-ttu-id="c8e8c-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="c8e8c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c8e8c-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="c8e8c-111">get_Request</span></span>](#get_request) | <span data-ttu-id="c8e8c-112">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-112">The HTTP request.</span></span>
[<span data-ttu-id="c8e8c-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="c8e8c-113">get_Response</span></span>](#get_response) | <span data-ttu-id="c8e8c-114">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-114">The HTTP response.</span></span>
[<span data-ttu-id="c8e8c-115">put_Response</span><span class="sxs-lookup"><span data-stu-id="c8e8c-115">put_Response</span></span>](#put_response) | <span data-ttu-id="c8e8c-116">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-116">Set the Response property.</span></span>
[<span data-ttu-id="c8e8c-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c8e8c-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="c8e8c-118">Obtenha um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-118">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="c8e8c-119">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="c8e8c-119">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="c8e8c-120">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-120">The web resource request contexts.</span></span>

## <span data-ttu-id="c8e8c-121">Parte</span><span class="sxs-lookup"><span data-stu-id="c8e8c-121">Members</span></span>

#### <span data-ttu-id="c8e8c-122">get_Request</span><span class="sxs-lookup"><span data-stu-id="c8e8c-122">get_Request</span></span> 

<span data-ttu-id="c8e8c-123">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-123">The HTTP request.</span></span>

> <span data-ttu-id="c8e8c-124">Public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="c8e8c-124">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="c8e8c-125">get_Response</span><span class="sxs-lookup"><span data-stu-id="c8e8c-125">get_Response</span></span> 

<span data-ttu-id="c8e8c-126">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-126">The HTTP response.</span></span>

> <span data-ttu-id="c8e8c-127">público HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* \* resposta)</span><span class="sxs-lookup"><span data-stu-id="c8e8c-127">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="c8e8c-128">put_Response</span><span class="sxs-lookup"><span data-stu-id="c8e8c-128">put_Response</span></span> 

<span data-ttu-id="c8e8c-129">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-129">Set the Response property.</span></span>

> <span data-ttu-id="c8e8c-130">público HRESULT [put_Response](#put_response)(resposta[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="c8e8c-130">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="c8e8c-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c8e8c-131">GetDeferral</span></span> 

<span data-ttu-id="c8e8c-132">Obtenha um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-132">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="c8e8c-133">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="c8e8c-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="c8e8c-134">Você pode usar o objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) para concluir a solicitação de rede em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-134">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="c8e8c-135">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="c8e8c-135">get_ResourceContext</span></span> 

<span data-ttu-id="c8e8c-136">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="c8e8c-136">The web resource request contexts.</span></span>

> <span data-ttu-id="c8e8c-137">[get_ResourceContext](#get_resourcecontext)público HRESULT (CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* contexto)</span><span class="sxs-lookup"><span data-stu-id="c8e8c-137">public HRESULT [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

