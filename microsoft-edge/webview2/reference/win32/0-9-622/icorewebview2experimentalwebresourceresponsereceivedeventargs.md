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
# interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
  : public IUnknown
```

Args de evento para o evento WebResourceResponseReceived.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Request](#get_request) | Objeto de solicitação de recurso da Web. Todas as modificações feitas neste objeto serão ignoradas.
[get_Response](#get_response) | Objeto de resposta de recurso da Web.
[PopulateResponseContent](#populateresponsecontent) | Método Async para solicitar o fluxo de conteúdo da resposta.

Conterá a solicitação como foi enviada e a resposta como ela foi recebida. Observação: para obter o fluxo de conteúdo da resposta, primeiro chame PopulateResponseContent e aguarde a chamada assíncrona ser concluída; caso contrário, o objeto de fluxo de conteúdo retornado será NULL.

## Parte

#### get_Request 

Objeto de solicitação de recurso da Web. Todas as modificações feitas neste objeto serão ignoradas.

> Public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) * * Request)

#### get_Response 

Objeto de resposta de recurso da Web.

> público HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) * * resposta)

Todas as modificações feitas neste objeto serão ignoradas.

#### PopulateResponseContent 

Método Async para solicitar o fluxo de conteúdo da resposta.

> Public HRESULT [PopulateResponseContent](#populateresponsecontent)(manipulador[ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) *)

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

