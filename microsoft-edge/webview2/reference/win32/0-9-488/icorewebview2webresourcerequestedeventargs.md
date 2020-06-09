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
ms.openlocfilehash: 85954a3f866ed9fd778af93fc27872af2d20eb2e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697942"
---
# <span data-ttu-id="a55d9-104">interface ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a55d9-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="a55d9-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="a55d9-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="a55d9-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="a55d9-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="a55d9-107">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="a55d9-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="a55d9-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="a55d9-108">Summary</span></span>

 <span data-ttu-id="a55d9-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a55d9-109">Members</span></span>                        | <span data-ttu-id="a55d9-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="a55d9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a55d9-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="a55d9-111">get_Request</span></span>](#get_request) | <span data-ttu-id="a55d9-112">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="a55d9-112">The HTTP request.</span></span>
[<span data-ttu-id="a55d9-113">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="a55d9-113">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="a55d9-114">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="a55d9-114">The web resource request contexts.</span></span>
[<span data-ttu-id="a55d9-115">get_Response</span><span class="sxs-lookup"><span data-stu-id="a55d9-115">get_Response</span></span>](#get_response) | <span data-ttu-id="a55d9-116">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="a55d9-116">The HTTP response.</span></span>
[<span data-ttu-id="a55d9-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="a55d9-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="a55d9-118">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="a55d9-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="a55d9-119">put_Response</span><span class="sxs-lookup"><span data-stu-id="a55d9-119">put_Response</span></span>](#put_response) | <span data-ttu-id="a55d9-120">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="a55d9-120">Set the Response property.</span></span>

## <span data-ttu-id="a55d9-121">Parte</span><span class="sxs-lookup"><span data-stu-id="a55d9-121">Members</span></span>

#### <span data-ttu-id="a55d9-122">get_Request</span><span class="sxs-lookup"><span data-stu-id="a55d9-122">get_Request</span></span> 

<span data-ttu-id="a55d9-123">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="a55d9-123">The HTTP request.</span></span>

> <span data-ttu-id="a55d9-124">Public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="a55d9-124">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="a55d9-125">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="a55d9-125">get_ResourceContext</span></span> 

<span data-ttu-id="a55d9-126">Os contextos de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="a55d9-126">The web resource request contexts.</span></span>

> <span data-ttu-id="a55d9-127">[get_ResourceContext](#get_resourcecontext)público HRESULT (COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* contexto)</span><span class="sxs-lookup"><span data-stu-id="a55d9-127">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="a55d9-128">get_Response</span><span class="sxs-lookup"><span data-stu-id="a55d9-128">get_Response</span></span> 

<span data-ttu-id="a55d9-129">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="a55d9-129">The HTTP response.</span></span>

> <span data-ttu-id="a55d9-130">público HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* resposta)</span><span class="sxs-lookup"><span data-stu-id="a55d9-130">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

#### <span data-ttu-id="a55d9-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="a55d9-131">GetDeferral</span></span> 

<span data-ttu-id="a55d9-132">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="a55d9-132">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="a55d9-133">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="a55d9-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="a55d9-134">Você pode usar o objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para concluir a solicitação de rede em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="a55d9-134">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="a55d9-135">put_Response</span><span class="sxs-lookup"><span data-stu-id="a55d9-135">put_Response</span></span> 

<span data-ttu-id="a55d9-136">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="a55d9-136">Set the Response property.</span></span>

> <span data-ttu-id="a55d9-137">público HRESULT [put_Response](#put_response)(resposta[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="a55d9-137">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>

