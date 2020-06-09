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
ms.openlocfilehash: 0f14f8d281d4729d797eb5271a19cff67becafab
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698331"
---
# interface ICoreWebView2HistoryChangedEventHandler 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

O chamador implementa essa interface para receber o evento Historychanged.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Invocar](#invoke) | Não há argumentos de evento e o parâmetro args será nulo.

## Parte

#### Invocar 

Não há argumentos de evento e o parâmetro args será nulo.

> [chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) * WebView, IUnknown * args)

