---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 59557ca86e8b044fb937fe93b3060c0879abb6f1
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652679"
---
# <span data-ttu-id="f433d-104">interface ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f433d-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="f433d-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="f433d-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="f433d-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="f433d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="f433d-107">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="f433d-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="f433d-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="f433d-108">Summary</span></span>

 <span data-ttu-id="f433d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f433d-109">Members</span></span>                        | <span data-ttu-id="f433d-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="f433d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f433d-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="f433d-111">get_Request</span></span>](#get_request) | <span data-ttu-id="f433d-112">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="f433d-112">The HTTP request.</span></span>
[<span data-ttu-id="f433d-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="f433d-113">get_Response</span></span>](#get_response) | <span data-ttu-id="f433d-114">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f433d-114">The HTTP response.</span></span>
[<span data-ttu-id="f433d-115">put_Response</span><span class="sxs-lookup"><span data-stu-id="f433d-115">put_Response</span></span>](#put_response) | <span data-ttu-id="f433d-116">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="f433d-116">Set the Response property.</span></span>
[<span data-ttu-id="f433d-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f433d-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="f433d-118">Obtenha um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="f433d-118">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="f433d-119">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="f433d-119">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="f433d-120">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="f433d-120">The web resource request contexts.</span></span>

## <span data-ttu-id="f433d-121">Parte</span><span class="sxs-lookup"><span data-stu-id="f433d-121">Members</span></span>

#### <span data-ttu-id="f433d-122">get_Request</span><span class="sxs-lookup"><span data-stu-id="f433d-122">get_Request</span></span> 

<span data-ttu-id="f433d-123">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="f433d-123">The HTTP request.</span></span>

> <span data-ttu-id="f433d-124">Public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="f433d-124">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="f433d-125">get_Response</span><span class="sxs-lookup"><span data-stu-id="f433d-125">get_Response</span></span> 

<span data-ttu-id="f433d-126">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f433d-126">The HTTP response.</span></span>

> <span data-ttu-id="f433d-127">público HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* \* resposta)</span><span class="sxs-lookup"><span data-stu-id="f433d-127">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="f433d-128">put_Response</span><span class="sxs-lookup"><span data-stu-id="f433d-128">put_Response</span></span> 

<span data-ttu-id="f433d-129">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="f433d-129">Set the Response property.</span></span>

> <span data-ttu-id="f433d-130">público HRESULT [put_Response](#put_response)(resposta[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="f433d-130">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="f433d-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f433d-131">GetDeferral</span></span> 

<span data-ttu-id="f433d-132">Obtenha um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="f433d-132">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="f433d-133">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="f433d-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="f433d-134">Você pode usar o objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) para concluir a solicitação de rede em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="f433d-134">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="f433d-135">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="f433d-135">get_ResourceContext</span></span> 

<span data-ttu-id="f433d-136">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="f433d-136">The web resource request contexts.</span></span>

> <span data-ttu-id="f433d-137">[get_ResourceContext](#get_resourcecontext)público HRESULT (CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* contexto)</span><span class="sxs-lookup"><span data-stu-id="f433d-137">public HRESULT [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

