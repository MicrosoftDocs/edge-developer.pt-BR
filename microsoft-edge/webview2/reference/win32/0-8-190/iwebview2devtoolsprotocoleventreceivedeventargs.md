---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 0df2ea043a95c8cca24c0b9bbe3091c490b4ea3d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878600"
---
# 0.8.355-IWebView2DevToolsProtocolEventReceivedEventArgs de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

Args de evento para o evento DevToolsProtocolEventReceived.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_ParameterObjectAsJson](#get_parameterobjectasjson) | O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.

## Parte

#### get_ParameterObjectAsJson 

O objeto de parâmetro do evento DevToolsProtocol correspondente representado como uma cadeia de caracteres JSON.

> público HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR * ParameterObjectAsJson)

