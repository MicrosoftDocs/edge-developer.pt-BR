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
ms.openlocfilehash: a90e7d3479f93d58d72db5c69cca53669a6d4501
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698273"
---
# interface ICoreWebView2MoveFocusRequestedEventHandler 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

O chamador implementa esse método para receber o evento MoveFocusRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Invocar](#invoke) | Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

## Parte

#### Invocar 

Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

> Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) * Sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) * args)

