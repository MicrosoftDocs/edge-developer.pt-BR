---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 40474d6b1169467022e5bb47e82eba3883edc2aa
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878096"
---
# 0.8.355-IWebView2WebResourceRequestedEventArgs de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Args de evento para o evento WebResourceRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Request](#get_request) | A solicitação HTTP.
[get_Response](#get_response) | A resposta HTTP.
[put_Response](#put_response) | Defina a propriedade Response.
[GetDeferral](#getdeferral) | Obtenha um objeto [IWebView2Deferral](IWebView2Deferral.md) e coloque o evento em um estado adiado.

## Parte

#### get_Request 

A solicitação HTTP.

> Public HRESULT [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) * * Request)

#### get_Response 

A resposta HTTP.

> público HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) * * resposta)

#### put_Response 

Defina a propriedade Response.

> público HRESULT [put_Response](#put_response)(resposta[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) *)

#### GetDeferral 

Obtenha um objeto [IWebView2Deferral](IWebView2Deferral.md) e coloque o evento em um estado adiado.

> público HRESULT [getadiamento](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) * * adiamento)

Você pode usar o objeto [IWebView2Deferral](IWebView2Deferral.md) para concluir a solicitação de rede em um momento posterior.

