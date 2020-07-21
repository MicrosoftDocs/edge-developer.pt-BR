---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: dec8bfb2927e823c85f472bd2cab0800ff5f00c7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883746"
---
# <span data-ttu-id="1af18-104">0.9.515-ICoreWebView2WebResourceRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="1af18-104">0.9.515 - interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="1af18-105">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="1af18-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="1af18-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="1af18-106">Summary</span></span>

 <span data-ttu-id="1af18-107">Parte</span><span class="sxs-lookup"><span data-stu-id="1af18-107">Members</span></span>                        | <span data-ttu-id="1af18-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="1af18-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1af18-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="1af18-109">get_Request</span></span>](#get_request) | <span data-ttu-id="1af18-110">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="1af18-110">The HTTP request.</span></span>
[<span data-ttu-id="1af18-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="1af18-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="1af18-112">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="1af18-112">The web resource request contexts.</span></span>
[<span data-ttu-id="1af18-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="1af18-113">get_Response</span></span>](#get_response) | <span data-ttu-id="1af18-114">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="1af18-114">The HTTP response.</span></span>
[<span data-ttu-id="1af18-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="1af18-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="1af18-116">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="1af18-116">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="1af18-117">put_Response</span><span class="sxs-lookup"><span data-stu-id="1af18-117">put_Response</span></span>](#put_response) | <span data-ttu-id="1af18-118">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="1af18-118">Set the Response property.</span></span>

## <span data-ttu-id="1af18-119">Parte</span><span class="sxs-lookup"><span data-stu-id="1af18-119">Members</span></span>

#### <span data-ttu-id="1af18-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="1af18-120">get_Request</span></span> 

<span data-ttu-id="1af18-121">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="1af18-121">The HTTP request.</span></span>

> <span data-ttu-id="1af18-122">Public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="1af18-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="1af18-123">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="1af18-123">get_ResourceContext</span></span> 

<span data-ttu-id="1af18-124">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="1af18-124">The web resource request contexts.</span></span>

> <span data-ttu-id="1af18-125">[get_ResourceContext](#get_resourcecontext)público HRESULT (COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* contexto)</span><span class="sxs-lookup"><span data-stu-id="1af18-125">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="1af18-126">get_Response</span><span class="sxs-lookup"><span data-stu-id="1af18-126">get_Response</span></span> 

<span data-ttu-id="1af18-127">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="1af18-127">The HTTP response.</span></span>

> <span data-ttu-id="1af18-128">público HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* resposta)</span><span class="sxs-lookup"><span data-stu-id="1af18-128">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

#### <span data-ttu-id="1af18-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="1af18-129">GetDeferral</span></span> 

<span data-ttu-id="1af18-130">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="1af18-130">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="1af18-131">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="1af18-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="1af18-132">Você pode usar o objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para concluir a solicitação de rede em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="1af18-132">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="1af18-133">put_Response</span><span class="sxs-lookup"><span data-stu-id="1af18-133">put_Response</span></span> 

<span data-ttu-id="1af18-134">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="1af18-134">Set the Response property.</span></span>

> <span data-ttu-id="1af18-135">público HRESULT [put_Response](#put_response)(resposta[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="1af18-135">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>

