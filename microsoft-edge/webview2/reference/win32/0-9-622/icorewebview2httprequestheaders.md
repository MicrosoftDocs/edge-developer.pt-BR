---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2HttpRequestHeaders
ms.openlocfilehash: 8455db6adccf2d3d10e9934fee940d00bba7377c
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011497"
---
# interface ICoreWebView2HttpRequestHeaders 

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

