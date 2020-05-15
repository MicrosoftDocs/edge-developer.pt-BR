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
ms.openlocfilehash: 4b9ad48d9b09343bad04d4acbe7c49750e76427d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652709"
---
# interface IWebView2HttpHeadersCollectionIterator 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

Iterador para uma coleção de cabeçalhos HTTP.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[GetCurrentHeader](#getcurrentheader) | Obter o nome e o valor do cabeçalho HTTP atual do iterador.
[MoveNext](#movenext) | Mover o iterador para o próximo cabeçalho HTTP na coleção.

Consulte [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) e [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).

## Parte

#### GetCurrentHeader 

Obter o nome e o valor do cabeçalho HTTP atual do iterador.

> Public HRESULT [GetCurrentHeader](#getcurrentheader)(nome LPWSTR * Name, LPWStr * Value)

Esse método irá falhar se a última chamada para MoveNext definir has_next como FALSE.

#### MoveNext 

Mover o iterador para o próximo cabeçalho HTTP na coleção.

> público HRESULT [MoveNext](#movenext)(BOOL * has_next)

O parâmetro has_next será definido como FALSE se não houver mais cabeçalhos HTTP. Após isso ocorrer, o método GetCurrentHeader falhará se chamado.

