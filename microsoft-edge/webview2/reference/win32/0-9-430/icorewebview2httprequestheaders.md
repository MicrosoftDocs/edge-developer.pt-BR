---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: a67c5c267178ea873cd12d8a22dea7409b260d52
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880994"
---
# 0.9.430-ICoreWebView2HttpRequestHeaders de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

Cabeçalhos de solicitação HTTP.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[GetHeader](#getheader) | Obtém o valor do cabeçalho que corresponde ao nome.
[Getheaders](#getheaders) | Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.
[Contém](#contains) | Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.
[SetHeader](#setheader) | Adiciona ou atualiza o cabeçalho que corresponde ao nome.
[RemoveHeader](#removeheader) | Remove o cabeçalho que corresponde ao nome.
[GetIterator](#getiterator) | Obtém um iterador sobre a coleção de cabeçalhos de solicitação.

Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting. Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.

## Parte

#### GetHeader 

Obtém o valor do cabeçalho que corresponde ao nome.

> público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR *)

#### Getheaders 

Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.

> público HRESULT [Getheaders](#getheaders)(LPCWSTR Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) * * Iteration)

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

> público HRESULT [Getiteration](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) * * iterador)

