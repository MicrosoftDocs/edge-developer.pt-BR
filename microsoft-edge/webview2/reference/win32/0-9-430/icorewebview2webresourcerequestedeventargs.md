---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 00aaddcc732076e4f7aa808b04132641fe7fe969
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886441"
---
# <span data-ttu-id="6a47e-104">0.9.430-ICoreWebView2WebResourceRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="6a47e-104">0.9.430 - interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="6a47e-105">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="6a47e-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="6a47e-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="6a47e-106">Summary</span></span>

 <span data-ttu-id="6a47e-107">Parte</span><span class="sxs-lookup"><span data-stu-id="6a47e-107">Members</span></span>                        | <span data-ttu-id="6a47e-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="6a47e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6a47e-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="6a47e-109">get_Request</span></span>](#get_request) | <span data-ttu-id="6a47e-110">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="6a47e-110">The HTTP request.</span></span>
[<span data-ttu-id="6a47e-111">get_Response</span><span class="sxs-lookup"><span data-stu-id="6a47e-111">get_Response</span></span>](#get_response) | <span data-ttu-id="6a47e-112">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="6a47e-112">The HTTP response.</span></span>
[<span data-ttu-id="6a47e-113">put_Response</span><span class="sxs-lookup"><span data-stu-id="6a47e-113">put_Response</span></span>](#put_response) | <span data-ttu-id="6a47e-114">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="6a47e-114">Set the Response property.</span></span>
[<span data-ttu-id="6a47e-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="6a47e-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="6a47e-116">Obtenha um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="6a47e-116">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="6a47e-117">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="6a47e-117">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="6a47e-118">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="6a47e-118">The web resource request contexts.</span></span>

## <span data-ttu-id="6a47e-119">Parte</span><span class="sxs-lookup"><span data-stu-id="6a47e-119">Members</span></span>

#### <span data-ttu-id="6a47e-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="6a47e-120">get_Request</span></span> 

<span data-ttu-id="6a47e-121">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="6a47e-121">The HTTP request.</span></span>

> <span data-ttu-id="6a47e-122">Public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="6a47e-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="6a47e-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="6a47e-123">get_Response</span></span> 

<span data-ttu-id="6a47e-124">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="6a47e-124">The HTTP response.</span></span>

> <span data-ttu-id="6a47e-125">público HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* \* resposta)</span><span class="sxs-lookup"><span data-stu-id="6a47e-125">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="6a47e-126">put_Response</span><span class="sxs-lookup"><span data-stu-id="6a47e-126">put_Response</span></span> 

<span data-ttu-id="6a47e-127">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="6a47e-127">Set the Response property.</span></span>

> <span data-ttu-id="6a47e-128">público HRESULT [put_Response](#put_response)(resposta[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="6a47e-128">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="6a47e-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="6a47e-129">GetDeferral</span></span> 

<span data-ttu-id="6a47e-130">Obtenha um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="6a47e-130">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="6a47e-131">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="6a47e-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="6a47e-132">Você pode usar o objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) para concluir a solicitação de rede em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="6a47e-132">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="6a47e-133">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="6a47e-133">get_ResourceContext</span></span> 

<span data-ttu-id="6a47e-134">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="6a47e-134">The web resource request contexts.</span></span>

> <span data-ttu-id="6a47e-135">[get_ResourceContext](#get_resourcecontext)público HRESULT (CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* contexto)</span><span class="sxs-lookup"><span data-stu-id="6a47e-135">public HRESULT [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

