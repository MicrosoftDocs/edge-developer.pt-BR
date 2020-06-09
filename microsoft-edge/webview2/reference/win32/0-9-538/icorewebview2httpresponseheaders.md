---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 508ecacc867330c73132ae7e446b7483ea002f83
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698361"
---
# interface ICoreWebView2HttpResponseHeaders 

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

