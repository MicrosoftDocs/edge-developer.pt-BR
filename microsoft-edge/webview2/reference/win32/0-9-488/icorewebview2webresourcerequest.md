---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: d91b7aeeebc8fd82587ac6c01fddd14e693c2559
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697060"
---
# interface ICoreWebView2WebResourceRequest 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

Uma solicitação HTTP usada com o evento WebResourceRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Content](#get_content) | O corpo da mensagem de solicitação HTTP como Stream.
[get_Headers](#get_headers) | Os cabeçalhos de solicitação HTTP mutável.
[get_Method](#get_method) | O método de solicitação HTTP.
[get_Uri](#get_uri) | O URI da solicitação.
[put_Content](#put_content) | Defina a propriedade Content.
[put_Method](#put_method) | Defina a Propriedade Method.
[put_Uri](#put_uri) | Defina a propriedade URI.

## Parte

#### get_Content 

O corpo da mensagem de solicitação HTTP como Stream.

> [get_Content](#get_content)público HRESULT (conteúdo IStream * *)

PUBLICAR dados seria aqui. Se um fluxo for definido, o que substituirá o corpo da mensagem, o fluxo deverá ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested desta resposta estiver concluído. Stream deve ser ágil ou ser criado a partir de um STA em segundo plano para evitar o impacto no desempenho do thread da interface do usuário. NULL significa sem dados de conteúdo. Semântica de IStream se aplica (retornar S_OK para ler chamadas até que todos os dados tenham esgotado)

#### get_Headers 

Os cabeçalhos de solicitação HTTP mutável.

> público HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) * * cabeçalhos)

#### get_Method 

O método de solicitação HTTP.

> [get_Method](#get_method)público HRESULT (método LPWSTR *)

#### get_Uri 

O URI da solicitação.

> [get_Uri](#get_uri)público HRESULT (URI LPWSTR *)

#### put_Content 

Defina a propriedade Content.

> [put_Content](#put_content)público HRESULT (conteúdo IStream *)

#### put_Method 

Defina a Propriedade Method.

> [put_Method](#put_method)público HRESULT (método LPCWSTR)

#### put_Uri 

Defina a propriedade URI.

> [put_Uri](#put_uri)público HRESULT (URI LPCWSTR)

