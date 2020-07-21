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

> Public HRESULT [get_Request](#get_request)(ICoreWebView2WebResourceRequest * * Request)

#### get_Response 

Objeto de resposta de recurso da Web.

> público HRESULT [get_Response](#get_response)(ICoreWebView2WebResourceResponse * * resposta)

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

