---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2DevToolsProtocolEventReceivedEventHandler
ms.openlocfilehash: 163ab3f16b6d835fc64aef4ea0fdff2883084faa
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010261"
---
# 0.9.579-ICoreWebView2DevToolsProtocolEventReceivedEventHandler de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

O chamador implementa essa interface para receber eventos do DevToolsProtocolEventReceived da WebView.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Invocar](#invoke) | Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

## Parte

#### Invocar 

Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

> Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) * Sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) * args)

