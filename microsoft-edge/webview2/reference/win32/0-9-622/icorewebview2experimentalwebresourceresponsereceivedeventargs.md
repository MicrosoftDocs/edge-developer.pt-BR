---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
ms.openlocfilehash: 552421aa003be2ea52493f16ad94ed2b08e8c3a9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011539"
---
# <span data-ttu-id="4aa8b-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="4aa8b-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="4aa8b-105">Args de evento para o evento WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="4aa8b-105">Event args for the WebResourceResponseReceived event.</span></span>

## <span data-ttu-id="4aa8b-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="4aa8b-106">Summary</span></span>

 <span data-ttu-id="4aa8b-107">Parte</span><span class="sxs-lookup"><span data-stu-id="4aa8b-107">Members</span></span>                        | <span data-ttu-id="4aa8b-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="4aa8b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4aa8b-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="4aa8b-109">get_Request</span></span>](#get_request) | <span data-ttu-id="4aa8b-110">Objeto de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="4aa8b-110">Web resource request object.</span></span> <span data-ttu-id="4aa8b-111">Todas as modificações feitas neste objeto serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="4aa8b-111">Any modifications to this object will be ignored.</span></span>
[<span data-ttu-id="4aa8b-112">get_Response</span><span class="sxs-lookup"><span data-stu-id="4aa8b-112">get_Response</span></span>](#get_response) | <span data-ttu-id="4aa8b-113">Objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="4aa8b-113">Web resource response object.</span></span>
[<span data-ttu-id="4aa8b-114">PopulateResponseContent</span><span class="sxs-lookup"><span data-stu-id="4aa8b-114">PopulateResponseContent</span></span>](#populateresponsecontent) | <span data-ttu-id="4aa8b-115">Método Async para solicitar o fluxo de conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="4aa8b-115">Async method to request the Content stream of the response.</span></span>

<span data-ttu-id="4aa8b-116">Conterá a solicitação como foi enviada e a resposta como ela foi recebida.</span><span class="sxs-lookup"><span data-stu-id="4aa8b-116">Will contain the request as it was sent and the response as it was received.</span></span> <span data-ttu-id="4aa8b-117">Observação: para obter o fluxo de conteúdo da resposta, primeiro chame PopulateResponseContent e aguarde a chamada assíncrona ser concluída; caso contrário, o objeto de fluxo de conteúdo retornado será NULL.</span><span class="sxs-lookup"><span data-stu-id="4aa8b-117">Note: To get the response content stream, first call PopulateResponseContent and wait for the async call to complete, otherwise the content stream object returned will be null.</span></span>

## <span data-ttu-id="4aa8b-118">Parte</span><span class="sxs-lookup"><span data-stu-id="4aa8b-118">Members</span></span>

#### <span data-ttu-id="4aa8b-119">get_Request</span><span class="sxs-lookup"><span data-stu-id="4aa8b-119">get_Request</span></span> 

<span data-ttu-id="4aa8b-120">Objeto de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="4aa8b-120">Web resource request object.</span></span> <span data-ttu-id="4aa8b-121">Todas as modificações feitas neste objeto serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="4aa8b-121">Any modifications to this object will be ignored.</span></span>

> <span data-ttu-id="4aa8b-122">Public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="4aa8b-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="4aa8b-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="4aa8b-123">get_Response</span></span> 

<span data-ttu-id="4aa8b-124">Objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="4aa8b-124">Web resource response object.</span></span>

> <span data-ttu-id="4aa8b-125">público HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* resposta)</span><span class="sxs-lookup"><span data-stu-id="4aa8b-125">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

<span data-ttu-id="4aa8b-126">Todas as modificações feitas neste objeto serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="4aa8b-126">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="4aa8b-127">PopulateResponseContent</span><span class="sxs-lookup"><span data-stu-id="4aa8b-127">PopulateResponseContent</span></span> 

<span data-ttu-id="4aa8b-128">Método Async para solicitar o fluxo de conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="4aa8b-128">Async method to request the Content stream of the response.</span></span>

> <span data-ttu-id="4aa8b-129">Public HRESULT [PopulateResponseContent](#populateresponsecontent)(manipulador[ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="4aa8b-129">public HRESULT [PopulateResponseContent](#populateresponsecontent)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) \* handler)</span></span>

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

