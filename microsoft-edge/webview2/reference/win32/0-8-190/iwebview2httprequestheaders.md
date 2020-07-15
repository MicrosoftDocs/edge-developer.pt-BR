---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 162d6dde904868ad6a4864b81c0ca76d50638c06
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878453"
---
# 0.8.355-IWebView2HttpRequestHeaders de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2HttpRequestHeaders
  : public IUnknown
```

Cabeçalhos de solicitação HTTP.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[GetHeader](#getheader) | Obtém o valor do cabeçalho que corresponde ao nome.
[Contém](#contains) | Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.
[SetHeader](#setheader) | Adiciona ou atualiza o cabeçalho que corresponde ao nome.
[RemoveHeader](#removeheader) | Remove o cabeçalho que corresponde ao nome.
[GetIterator](#getiterator) | Obtém um iterador sobre a coleção de cabeçalhos de solicitação.

Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting. Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.

## Parte

#### GetHeader 

Obtém o valor do cabeçalho que corresponde ao nome.

> público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR *)

#### Contém 

Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.

> a Public HRESULT [contém](#contains)(LPCWSTR Name, bool * Contains)

#### SetHeader 

Adiciona ou atualiza o cabeçalho que corresponde ao nome.

> Public HRESULT [SetHeader](#setheader)(nome LPCWSTR, valor LPCWSTR)

#### RemoveHeader 

Remove o cabeçalho que corresponde ao nome.

> Public HRESULT [RemoveHeader](#removeheader)(nome LPCWSTR)

#### GetIterator 

Obtém um iterador sobre a coleção de cabeçalhos de solicitação.

> público HRESULT [Getiteration](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) * * iterador)

