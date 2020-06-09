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
ms.openlocfilehash: 2429c519858aa9c55e52d47bea64fc182b6beb73
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698294"
---
# interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
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

