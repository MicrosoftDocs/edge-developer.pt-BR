---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: aa5206be13790fd7a783f2afb4471de90fc8f2ae
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885713"
---
# <span data-ttu-id="cd5a7-104">0.8.355-IWebView2WebResourceRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="cd5a7-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="cd5a7-105">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="cd5a7-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="cd5a7-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="cd5a7-106">Summary</span></span>

 <span data-ttu-id="cd5a7-107">Parte</span><span class="sxs-lookup"><span data-stu-id="cd5a7-107">Members</span></span>                        | <span data-ttu-id="cd5a7-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="cd5a7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cd5a7-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="cd5a7-109">get_Request</span></span>](#get_request) | <span data-ttu-id="cd5a7-110">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="cd5a7-110">The HTTP request.</span></span>
[<span data-ttu-id="cd5a7-111">get_Response</span><span class="sxs-lookup"><span data-stu-id="cd5a7-111">get_Response</span></span>](#get_response) | <span data-ttu-id="cd5a7-112">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="cd5a7-112">The HTTP response.</span></span>
[<span data-ttu-id="cd5a7-113">put_Response</span><span class="sxs-lookup"><span data-stu-id="cd5a7-113">put_Response</span></span>](#put_response) | <span data-ttu-id="cd5a7-114">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="cd5a7-114">Set the Response property.</span></span>
[<span data-ttu-id="cd5a7-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="cd5a7-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="cd5a7-116">Obtenha um objeto [IWebView2Deferral](IWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="cd5a7-116">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

## <span data-ttu-id="cd5a7-117">Parte</span><span class="sxs-lookup"><span data-stu-id="cd5a7-117">Members</span></span>

#### <span data-ttu-id="cd5a7-118">get_Request</span><span class="sxs-lookup"><span data-stu-id="cd5a7-118">get_Request</span></span> 

<span data-ttu-id="cd5a7-119">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="cd5a7-119">The HTTP request.</span></span>

> <span data-ttu-id="cd5a7-120">Public HRESULT [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="cd5a7-120">public HRESULT [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="cd5a7-121">get_Response</span><span class="sxs-lookup"><span data-stu-id="cd5a7-121">get_Response</span></span> 

<span data-ttu-id="cd5a7-122">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="cd5a7-122">The HTTP response.</span></span>

> <span data-ttu-id="cd5a7-123">público HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \* resposta)</span><span class="sxs-lookup"><span data-stu-id="cd5a7-123">public HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="cd5a7-124">put_Response</span><span class="sxs-lookup"><span data-stu-id="cd5a7-124">put_Response</span></span> 

<span data-ttu-id="cd5a7-125">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="cd5a7-125">Set the Response property.</span></span>

> <span data-ttu-id="cd5a7-126">público HRESULT [put_Response](#put_response)(resposta[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="cd5a7-126">public HRESULT [put_Response](#put_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="cd5a7-127">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="cd5a7-127">GetDeferral</span></span> 

<span data-ttu-id="cd5a7-128">Obtenha um objeto [IWebView2Deferral](IWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="cd5a7-128">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="cd5a7-129">público HRESULT [getadiamento](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="cd5a7-129">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="cd5a7-130">Você pode usar o objeto [IWebView2Deferral](IWebView2Deferral.md) para concluir a solicitação de rede em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="cd5a7-130">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the network request at a later time.</span></span>

