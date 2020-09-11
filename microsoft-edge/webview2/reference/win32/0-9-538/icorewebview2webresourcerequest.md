---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2WebResourceRequest
ms.openlocfilehash: 4d339d6a066404b51bd8b362ad2c455fa8f26e1f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010198"
---
# 0.9.579-ICoreWebView2WebResourceRequest de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

