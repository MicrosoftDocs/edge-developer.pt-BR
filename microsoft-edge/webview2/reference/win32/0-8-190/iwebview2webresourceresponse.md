---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 82c94869a84165de4c3b8d09937d6ea5d1f79256
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885685"
---
# 0.8.355-IWebView2WebResourceResponse de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

