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
ms.openlocfilehash: ad3f4e5e95b0309628644f17e5d647ab6d4af658
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652404"
---
# interface IWebView2WebResourceResponse 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2WebResourceResponse
  : public IUnknown
```

Uma resposta HTTP usada com o evento WebResourceRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Content](#get_content) | Conteúdo da resposta HTTP como Stream.
[put_Content](#put_content) | Defina a propriedade Content.
[get_Headers](#get_headers) | Cabeçalhos de resposta HTTP substituídos.
[get_StatusCode](#get_statuscode) | O código de status de resposta HTTP.
[put_StatusCode](#put_statuscode) | Defina a propriedade StatusCode.
[get_ReasonPhrase](#get_reasonphrase) | A frase de motivo da resposta HTTP.
[put_ReasonPhrase](#put_reasonphrase) | Defina a propriedade ReasonPhrase.

## Parte

#### get_Content 

Conteúdo da resposta HTTP como Stream.

> [get_Content](#get_content)público HRESULT (conteúdo IStream * *)

Stream deve ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested da resposta é concluído. Stream deve ser ágil ou ser criado a partir de um thread de segundo plano para evitar o impacto de desempenho no thread da interface do usuário. NULL significa sem dados de conteúdo. Semântica de IStream se aplica (retornar S_OK para ler chamadas até que todos os dados tenham esgotado)

#### put_Content 

Defina a propriedade Content.

> [put_Content](#put_content)público HRESULT (conteúdo IStream *)

#### get_Headers 

Cabeçalhos de resposta HTTP substituídos.

> público HRESULT [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) * * cabeçalhos)

#### get_StatusCode 

O código de status de resposta HTTP.

> [get_StatusCode](#get_statuscode)público HRESULT (int * StatusCode)

#### put_StatusCode 

Defina a propriedade StatusCode.

> [put_StatusCode](#put_statuscode)público HRESULT (int StatusCode)

#### get_ReasonPhrase 

A frase de motivo da resposta HTTP.

> público HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR * ReasonPhrase)

#### put_ReasonPhrase 

Defina a propriedade ReasonPhrase.

> Public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)

