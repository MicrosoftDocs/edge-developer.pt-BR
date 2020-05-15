---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 899a6f50db1d77f3f24524c5ccec139dcbdbcaf9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652415"
---
# <span data-ttu-id="3dfd5-104">interface IWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="3dfd5-104">interface IWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="3dfd5-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="3dfd5-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="3dfd5-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="3dfd5-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="3dfd5-107">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="3dfd5-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="3dfd5-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="3dfd5-108">Summary</span></span>

 <span data-ttu-id="3dfd5-109">Parte</span><span class="sxs-lookup"><span data-stu-id="3dfd5-109">Members</span></span>                        | <span data-ttu-id="3dfd5-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="3dfd5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3dfd5-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="3dfd5-111">get_Request</span></span>](#get_request) | <span data-ttu-id="3dfd5-112">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="3dfd5-112">The HTTP request.</span></span>
[<span data-ttu-id="3dfd5-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="3dfd5-113">get_Response</span></span>](#get_response) | <span data-ttu-id="3dfd5-114">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="3dfd5-114">The HTTP response.</span></span>
[<span data-ttu-id="3dfd5-115">put_Response</span><span class="sxs-lookup"><span data-stu-id="3dfd5-115">put_Response</span></span>](#put_response) | <span data-ttu-id="3dfd5-116">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="3dfd5-116">Set the Response property.</span></span>
[<span data-ttu-id="3dfd5-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="3dfd5-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="3dfd5-118">Obtenha um objeto [IWebView2Deferral](IWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="3dfd5-118">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

## <span data-ttu-id="3dfd5-119">Parte</span><span class="sxs-lookup"><span data-stu-id="3dfd5-119">Members</span></span>

#### <span data-ttu-id="3dfd5-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="3dfd5-120">get_Request</span></span> 

<span data-ttu-id="3dfd5-121">A solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="3dfd5-121">The HTTP request.</span></span>

> <span data-ttu-id="3dfd5-122">Public HRESULT [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="3dfd5-122">public HRESULT [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="3dfd5-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="3dfd5-123">get_Response</span></span> 

<span data-ttu-id="3dfd5-124">A resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="3dfd5-124">The HTTP response.</span></span>

> <span data-ttu-id="3dfd5-125">público HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \* resposta)</span><span class="sxs-lookup"><span data-stu-id="3dfd5-125">public HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="3dfd5-126">put_Response</span><span class="sxs-lookup"><span data-stu-id="3dfd5-126">put_Response</span></span> 

<span data-ttu-id="3dfd5-127">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="3dfd5-127">Set the Response property.</span></span>

> <span data-ttu-id="3dfd5-128">público HRESULT [put_Response](#put_response)(resposta[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="3dfd5-128">public HRESULT [put_Response](#put_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="3dfd5-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="3dfd5-129">GetDeferral</span></span> 

<span data-ttu-id="3dfd5-130">Obtenha um objeto [IWebView2Deferral](IWebView2Deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="3dfd5-130">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="3dfd5-131">público HRESULT [getadiamento](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="3dfd5-131">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="3dfd5-132">Você pode usar o objeto [IWebView2Deferral](IWebView2Deferral.md) para concluir a solicitação de rede em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="3dfd5-132">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the network request at a later time.</span></span>

