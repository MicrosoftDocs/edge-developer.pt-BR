---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: e83078b6ac45fbc0b479c5d6b0fde3263a8f34fd
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698321"
---
# interface ICoreWebView2WebResourceRequestedEventArgs 

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Args de evento para o evento WebResourceRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Request](#get_request) | A solicitação HTTP.
[get_ResourceContext](#get_resourcecontext) | Os contextos de solicitação de recurso da Web.
[get_Response](#get_response) | A resposta HTTP.
[GetDeferral](#getdeferral) | Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.
[put_Response](#put_response) | Defina a propriedade Response.

## Parte

#### get_Request 

A solicitação HTTP.

> Public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) * * Request)

#### get_ResourceContext 

Os contextos de solicitação de recurso da Web.

> [get_ResourceContext](#get_resourcecontext)público HRESULT (COREWEBVIEW2_WEB_RESOURCE_CONTEXT * contexto)

#### get_Response 

A resposta HTTP.

> público HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) * * resposta)

#### GetDeferral 

Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.

> público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * adiamento)

Você pode usar o objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para concluir a solicitação de rede em um momento posterior.

#### put_Response 

Defina a propriedade Response.

> público HRESULT [put_Response](#put_response)(resposta[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) *)
