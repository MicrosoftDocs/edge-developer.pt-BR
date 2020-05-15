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
ms.openlocfilehash: 69bf9eeae4b6736ac6df6ddaa9594b7438cbf58c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652416"
---
# interface IWebView2WebResourceRequest 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2WebResourceRequest
  : public IUnknown
```

Uma solicitação HTTP usada com o evento WebResourceRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | O URI da solicitação.
[put_Uri](#put_uri) | Defina a propriedade URI.
[get_Method](#get_method) | O método de solicitação HTTP.
[put_Method](#put_method) | Defina a Propriedade Method.
[get_Content](#get_content) | O corpo da mensagem de solicitação HTTP como Stream.
[put_Content](#put_content) | Defina a propriedade Content.
[get_Headers](#get_headers) | Os cabeçalhos de solicitação HTTP mutável.

## Parte

#### get_Uri 

O URI da solicitação.

> [get_Uri](#get_uri)público HRESULT (URI LPWSTR *)

#### put_Uri 

Defina a propriedade URI.

> [put_Uri](#put_uri)público HRESULT (URI LPCWSTR)

#### get_Method 

O método de solicitação HTTP.

> [get_Method](#get_method)público HRESULT (método LPWSTR *)

#### put_Method 

Defina a Propriedade Method.

> [put_Method](#put_method)público HRESULT (método LPCWSTR)

#### get_Content 

O corpo da mensagem de solicitação HTTP como Stream.

> [get_Content](#get_content)público HRESULT (conteúdo IStream * *)

PUBLICAR dados seria aqui. Se um fluxo for definido, o que substituirá o corpo da mensagem, o fluxo deverá ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested desta resposta estiver concluído. Stream deve ser ágil ou ser criado a partir de um STA em segundo plano para evitar o impacto no desempenho do thread da interface do usuário. NULL significa sem dados de conteúdo. Semântica de IStream se aplica (retornar S_OK para ler chamadas até que todos os dados tenham esgotado)

#### put_Content 

Defina a propriedade Content.

> [put_Content](#put_content)público HRESULT (conteúdo IStream *)

#### get_Headers 

Os cabeçalhos de solicitação HTTP mutável.

> público HRESULT [get_Headers](#get_headers)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) * * cabeçalhos)

