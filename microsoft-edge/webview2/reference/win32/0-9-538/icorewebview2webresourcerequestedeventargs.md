---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 3613ed9b2ef562e8760de1a88322ef028ddf4ca9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879216"
---
# <span data-ttu-id="4d18f-104">interface ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="4d18f-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="4d18f-105">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="4d18f-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="4d18f-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="4d18f-106">Summary</span></span>

 <span data-ttu-id="4d18f-107">Parte</span><span class="sxs-lookup"><span data-stu-id="4d18f-107">Members</span></span>                        | <span data-ttu-id="4d18f-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="4d18f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4d18f-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="4d18f-109">get_Request</span></span>](#get_request) | <span data-ttu-id="4d18f-110">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="4d18f-110">The HTTP request.</span></span>
[<span data-ttu-id="4d18f-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="4d18f-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="4d18f-112">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="4d18f-112">The web resource request contexts.</span></span>
[<span data-ttu-id="4d18f-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="4d18f-113">get_Response</span></span>](#get_response) | <span data-ttu-id="4d18f-114">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="4d18f-114">The HTTP response.</span></span>
[<span data-ttu-id="4d18f-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4d18f-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="4d18f-116">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="4d18f-116">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="4d18f-117">put_Response</span><span class="sxs-lookup"><span data-stu-id="4d18f-117">put_Response</span></span>](#put_response) | <span data-ttu-id="4d18f-118">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="4d18f-118">Set the Response property.</span></span>

## <span data-ttu-id="4d18f-119">Parte</span><span class="sxs-lookup"><span data-stu-id="4d18f-119">Members</span></span>

#### <span data-ttu-id="4d18f-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="4d18f-120">get_Request</span></span> 

<span data-ttu-id="4d18f-121">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="4d18f-121">The HTTP request.</span></span>

> <span data-ttu-id="4d18f-122">Public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="4d18f-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="4d18f-123">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="4d18f-123">get_ResourceContext</span></span> 

<span data-ttu-id="4d18f-124">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="4d18f-124">The web resource request contexts.</span></span>

> <span data-ttu-id="4d18f-125">[get_ResourceContext](#get_resourcecontext)público HRESULT (COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* contexto)</span><span class="sxs-lookup"><span data-stu-id="4d18f-125">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="4d18f-126">get_Response</span><span class="sxs-lookup"><span data-stu-id="4d18f-126">get_Response</span></span> 

<span data-ttu-id="4d18f-127">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="4d18f-127">The HTTP response.</span></span>

> <span data-ttu-id="4d18f-128">público HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* resposta)</span><span class="sxs-lookup"><span data-stu-id="4d18f-128">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

#### <span data-ttu-id="4d18f-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4d18f-129">GetDeferral</span></span> 

<span data-ttu-id="4d18f-130">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="4d18f-130">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="4d18f-131">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="4d18f-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="4d18f-132">Você pode usar o objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para concluir a solicitação de rede em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="4d18f-132">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="4d18f-133">put_Response</span><span class="sxs-lookup"><span data-stu-id="4d18f-133">put_Response</span></span> 

<span data-ttu-id="4d18f-134">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="4d18f-134">Set the Response property.</span></span>

> <span data-ttu-id="4d18f-135">público HRESULT [put_Response](#put_response)(resposta[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="4d18f-135">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>

