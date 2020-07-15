---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: d70162803cfb2f9d1f0cfbf7e7397ee1cdbeec0e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878187"
---
# 0.8.355-IWebView2WebMessageReceivedEventArgs de interface 

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

