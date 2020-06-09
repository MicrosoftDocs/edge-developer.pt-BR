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
ms.openlocfilehash: effceb6fafb062b1747f39876b8d2a5e02721aa8
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697270"
---
# interface ICoreWebView2HttpRequestHeaders 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

Cabeçalhos de solicitação HTTP.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Contém](#contains) | Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.
[GetHeader](#getheader) | Obtém o valor do cabeçalho que corresponde ao nome.
[Getheaders](#getheaders) | Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.
[GetIterator](#getiterator) | Obtém um iterador sobre a coleção de cabeçalhos de solicitação.
[RemoveHeader](#removeheader) | Remove o cabeçalho que corresponde ao nome.
[SetHeader](#setheader) | Adiciona ou atualiza o cabeçalho que corresponde ao nome.

Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting. Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.

## Parte

#### Contém 

Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.

> a Public HRESULT [contém](#contains)(LPCWSTR Name, bool * Contains)

#### GetHeader 

Obtém o valor do cabeçalho que corresponde ao nome.

> público HRESULT [GetHeader](#getheader)(nome do LPCWSTR, o valor LPWSTR *)

#### Getheaders 

Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.

> público HRESULT [Getheaders](#getheaders)(LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * * Iteration)

#### GetIterator 

Obtém um iterador sobre a coleção de cabeçalhos de solicitação.

> público HRESULT [Getiteration](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * * iterador)

#### RemoveHeader 

Remove o cabeçalho que corresponde ao nome.

> Public HRESULT [RemoveHeader](#removeheader)(nome LPCWSTR)

#### SetHeader 

Adiciona ou atualiza o cabeçalho que corresponde ao nome.

> Public HRESULT [SetHeader](#setheader)(nome LPCWSTR, valor LPCWSTR)

