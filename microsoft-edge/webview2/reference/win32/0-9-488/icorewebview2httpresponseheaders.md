---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 356f8bfc235e522ef5e976baf61f8c9017766a3d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880532"
---
# 0.9.515-ICoreWebView2HttpResponseHeaders de interface 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

Cabeçalhos de resposta HTTP.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[AppendHeader](#appendheader) | Acrescenta uma linha de cabeçalho com nome e valor.
[Contém](#contains) | Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.
[GetHeader](#getheader) | Obtém o primeiro valor de cabeçalho na coleção que corresponde ao nome.
[Getheaders](#getheaders) | Obtém os valores de cabeçalho correspondentes ao nome.
[GetIterator](#getiterator) | Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.

Usado para construir um WebResourceResponse para o evento WebResourceRequested.

## Parte

#### AppendHeader 

Acrescenta uma linha de cabeçalho com nome e valor.

> Public HRESULT [AppendHeader](#appendheader)(nome LPCWSTR, valor LPCWSTR)

#### Contém 

Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.

> a Public HRESULT [contém](#contains)(LPCWSTR Name, bool * Contains)

#### GetHeader 

Obtém o primeiro valor de cabeçalho na coleção que corresponde ao nome.

> público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR *)

#### Getheaders 

Obtém os valores de cabeçalho correspondentes ao nome.

> público HRESULT [Getheaders](#getheaders)(LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * * Iteration)

#### GetIterator 

Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.

> público HRESULT [Getiteration](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * * iterador)

