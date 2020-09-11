---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2DevToolsProtocolEventReceivedEventArgs
ms.openlocfilehash: 79af7b28b8b8ab7e2e2b6612f121208b8d917725
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010265"
---
# 0.9.579-ICoreWebView2DevToolsProtocolEventReceivedEventArgs de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

