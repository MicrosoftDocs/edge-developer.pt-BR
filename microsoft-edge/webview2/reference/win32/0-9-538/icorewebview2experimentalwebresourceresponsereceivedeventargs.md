---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
ms.openlocfilehash: 056667b4ee1995763fee81c8d7a9be31496f7f3e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886499"
---
# <span data-ttu-id="dd2e0-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="dd2e0-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="dd2e0-105">Args de evento para o evento WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="dd2e0-105">Event args for the WebResourceResponseReceived event.</span></span>

## <span data-ttu-id="dd2e0-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="dd2e0-106">Summary</span></span>

 <span data-ttu-id="dd2e0-107">Parte</span><span class="sxs-lookup"><span data-stu-id="dd2e0-107">Members</span></span>                        | <span data-ttu-id="dd2e0-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="dd2e0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dd2e0-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="dd2e0-109">get_Request</span></span>](#get_request) | <span data-ttu-id="dd2e0-110">Objeto de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="dd2e0-110">Web resource request object.</span></span> <span data-ttu-id="dd2e0-111">Todas as modificações feitas neste objeto serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="dd2e0-111">Any modifications to this object will be ignored.</span></span>
[<span data-ttu-id="dd2e0-112">get_Response</span><span class="sxs-lookup"><span data-stu-id="dd2e0-112">get_Response</span></span>](#get_response) | <span data-ttu-id="dd2e0-113">Objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="dd2e0-113">Web resource response object.</span></span>
[<span data-ttu-id="dd2e0-114">PopulateResponseContent</span><span class="sxs-lookup"><span data-stu-id="dd2e0-114">PopulateResponseContent</span></span>](#populateresponsecontent) | <span data-ttu-id="dd2e0-115">Método Async para solicitar o fluxo de conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="dd2e0-115">Async method to request the Content stream of the response.</span></span>

<span data-ttu-id="dd2e0-116">Conterá a solicitação como foi enviada e a resposta como ela foi recebida.</span><span class="sxs-lookup"><span data-stu-id="dd2e0-116">Will contain the request as it was sent and the response as it was received.</span></span> <span data-ttu-id="dd2e0-117">Observação: para obter o fluxo de conteúdo da resposta, primeiro chame PopulateResponseContent e aguarde a chamada assíncrona ser concluída; caso contrário, o objeto de fluxo de conteúdo retornado será NULL.</span><span class="sxs-lookup"><span data-stu-id="dd2e0-117">Note: To get the response content stream, first call PopulateResponseContent and wait for the async call to complete, otherwise the content stream object returned will be null.</span></span>

## <span data-ttu-id="dd2e0-118">Parte</span><span class="sxs-lookup"><span data-stu-id="dd2e0-118">Members</span></span>

#### <span data-ttu-id="dd2e0-119">get_Request</span><span class="sxs-lookup"><span data-stu-id="dd2e0-119">get_Request</span></span> 

<span data-ttu-id="dd2e0-120">Objeto de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="dd2e0-120">Web resource request object.</span></span> <span data-ttu-id="dd2e0-121">Todas as modificações feitas neste objeto serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="dd2e0-121">Any modifications to this object will be ignored.</span></span>

> <span data-ttu-id="dd2e0-122">Public HRESULT [get_Request](#get_request)(ICoreWebView2WebResourceRequest \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="dd2e0-122">public HRESULT [get_Request](#get_request)(ICoreWebView2WebResourceRequest \*\* request)</span></span>

#### <span data-ttu-id="dd2e0-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="dd2e0-123">get_Response</span></span> 

<span data-ttu-id="dd2e0-124">Objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="dd2e0-124">Web resource response object.</span></span>

> <span data-ttu-id="dd2e0-125">público HRESULT [get_Response](#get_response)(ICoreWebView2WebResourceResponse \* \* resposta)</span><span class="sxs-lookup"><span data-stu-id="dd2e0-125">public HRESULT [get_Response](#get_response)(ICoreWebView2WebResourceResponse \*\* response)</span></span>

<span data-ttu-id="dd2e0-126">Todas as modificações feitas neste objeto serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="dd2e0-126">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="dd2e0-127">PopulateResponseContent</span><span class="sxs-lookup"><span data-stu-id="dd2e0-127">PopulateResponseContent</span></span> 

<span data-ttu-id="dd2e0-128">Método Async para solicitar o fluxo de conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="dd2e0-128">Async method to request the Content stream of the response.</span></span>

> <span data-ttu-id="dd2e0-129">Public HRESULT [PopulateResponseContent](#populateresponsecontent)(manipulador[ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="dd2e0-129">public HRESULT [PopulateResponseContent](#populateresponsecontent)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) \* handler)</span></span>

```cpp
                    args->PopulateResponseContent(
                        Callback<
                            ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler>(
                            [this, webResourceRequest, webResourceResponse](HRESULT result) {
                                std::wstring message =
                                    L"{ \"kind\": \"event\", \"name\": "
                                    L"\"WebResourceResponseReceived\", \"args\": {"
                                    L"\"request\": " +
                                    RequestToJsonString(webResourceRequest.get()) +
                                    L", "
                                    L"\"response\": " +
                                    ResponseToJsonString(webResourceResponse.get()) + L"}";

                                message +=
                                    WebViewPropertiesToJsonString(m_webviewEventSource.get());
                                message += L"}";
                                PostEventMessage(message);
                                return S_OK;
                            })
                            .Get());
```

