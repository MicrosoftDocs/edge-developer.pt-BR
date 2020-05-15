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
ms.openlocfilehash: 8cdedd8051f52b7f6ad187ec948eabef96c6670b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652399"
---
# <span data-ttu-id="5b16d-104">interface ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="5b16d-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="5b16d-105">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="5b16d-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="5b16d-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="5b16d-106">Summary</span></span>

 <span data-ttu-id="5b16d-107">Parte</span><span class="sxs-lookup"><span data-stu-id="5b16d-107">Members</span></span>                        | <span data-ttu-id="5b16d-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="5b16d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5b16d-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="5b16d-109">get_Request</span></span>](#get_request) | <span data-ttu-id="5b16d-110">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="5b16d-110">The HTTP request.</span></span>
[<span data-ttu-id="5b16d-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="5b16d-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="5b16d-112">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="5b16d-112">The web resource request contexts.</span></span>
[<span data-ttu-id="5b16d-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="5b16d-113">get_Response</span></span>](#get_response) | <span data-ttu-id="5b16d-114">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="5b16d-114">The HTTP response.</span></span>
[<span data-ttu-id="5b16d-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="5b16d-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="5b16d-116">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="5b16d-116">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="5b16d-117">put_Response</span><span class="sxs-lookup"><span data-stu-id="5b16d-117">put_Response</span></span>](#put_response) | <span data-ttu-id="5b16d-118">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="5b16d-118">Set the Response property.</span></span>

## <span data-ttu-id="5b16d-119">Parte</span><span class="sxs-lookup"><span data-stu-id="5b16d-119">Members</span></span>

#### <span data-ttu-id="5b16d-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="5b16d-120">get_Request</span></span> 

<span data-ttu-id="5b16d-121">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="5b16d-121">The HTTP request.</span></span>

> <span data-ttu-id="5b16d-122">Public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="5b16d-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="5b16d-123">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="5b16d-123">get_ResourceContext</span></span> 

<span data-ttu-id="5b16d-124">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="5b16d-124">The web resource request contexts.</span></span>

> <span data-ttu-id="5b16d-125">[get_ResourceContext](#get_resourcecontext)público HRESULT (COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* contexto)</span><span class="sxs-lookup"><span data-stu-id="5b16d-125">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="5b16d-126">get_Response</span><span class="sxs-lookup"><span data-stu-id="5b16d-126">get_Response</span></span> 

<span data-ttu-id="5b16d-127">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="5b16d-127">The HTTP response.</span></span>

> <span data-ttu-id="5b16d-128">público HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* resposta)</span><span class="sxs-lookup"><span data-stu-id="5b16d-128">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

#### <span data-ttu-id="5b16d-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="5b16d-129">GetDeferral</span></span> 

<span data-ttu-id="5b16d-130">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="5b16d-130">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="5b16d-131">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="5b16d-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="5b16d-132">Você pode usar o objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para concluir a solicitação de rede em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="5b16d-132">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="5b16d-133">put_Response</span><span class="sxs-lookup"><span data-stu-id="5b16d-133">put_Response</span></span> 

<span data-ttu-id="5b16d-134">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="5b16d-134">Set the Response property.</span></span>

> <span data-ttu-id="5b16d-135">público HRESULT [put_Response](#put_response)(resposta[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="5b16d-135">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>

