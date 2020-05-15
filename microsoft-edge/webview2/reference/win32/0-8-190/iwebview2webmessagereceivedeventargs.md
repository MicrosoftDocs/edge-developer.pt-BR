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
ms.openlocfilehash: 053e186aec3871b47e2eb5c6684bc00c934c3a77
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652469"
---
# interface IWebView2WebMessageReceivedEventArgs 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

Args de evento para o evento WebMessageReceived.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Source](#get_source) | O URI do documento que enviou esta mensagem da Web.
[get_WebMessageAsJson](#get_webmessageasjson) | A mensagem postada do conteúdo da WebView para o host convertido em uma cadeia de caracteres JSON.
[get_WebMessageAsString](#get_webmessageasstring) | Se a mensagem postada do conteúdo WebView para o host for um tipo de cadeia de caracteres, esse método retornará o valor dessa cadeia de caracteres.

## Parte

#### get_Source 

O URI do documento que enviou esta mensagem da Web.

> [get_Source](#get_source)público HRESULT (fonte LPWSTR *)

#### get_WebMessageAsJson 

A mensagem postada do conteúdo da WebView para o host convertido em uma cadeia de caracteres JSON.

> público HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR * WebMessageAsJson)

Use isso para se comunicar por objetos JavaScript.

Por exemplo, as seguintes chamadas de mensagens de mensagens resultam nos seguintes valores de WebMessageAsJson:

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### get_WebMessageAsString 

Se a mensagem postada do conteúdo WebView para o host for um tipo de cadeia de caracteres, esse método retornará o valor dessa cadeia de caracteres.

> público HRESULT [get_WebMessageAsString](#get_webmessageasstring)(LPWSTR * WebMessageAsString)

Se a mensagem publicada for outro tipo de tipo JavaScript, esse método falhará com E_INVALIDARG. Use isso para se comunicar por meio de cadeias de caracteres simples.

Por exemplo, as seguintes chamadas de mensagens de mensagens resultam nos seguintes valores de WebMessageAsString:

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

