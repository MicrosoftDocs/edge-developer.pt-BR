---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 59557ca86e8b044fb937fe93b3060c0879abb6f1
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652679"
---
# interface ICoreWebView2WebResourceRequestedEventArgs 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Args de evento para o evento WebResourceRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Request](#get_request) | A solicitação HTTP.
[get_Response](#get_response) | A resposta HTTP.
[put_Response](#put_response) | Defina a propriedade Response.
[GetDeferral](#getdeferral) | Obtenha um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) e coloque o evento em um estado adiado.
[get_ResourceContext](#get_resourcecontext) | Os contextos de solicitação de recurso da Web.

## Parte

#### get_Request 

A solicitação HTTP.

> Public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) * * Request)

#### get_Response 

A resposta HTTP.

> público HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) * * resposta)

#### put_Response 

Defina a propriedade Response.

> público HRESULT [put_Response](#put_response)(resposta[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) *)

#### GetDeferral 

Obtenha um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) e coloque o evento em um estado adiado.

> público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) * * adiamento)

Você pode usar o objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) para concluir a solicitação de rede em um momento posterior.

#### get_ResourceContext 

Os contextos de solicitação de recurso da Web.

> [get_ResourceContext](#get_resourcecontext)público HRESULT (CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT * contexto)

