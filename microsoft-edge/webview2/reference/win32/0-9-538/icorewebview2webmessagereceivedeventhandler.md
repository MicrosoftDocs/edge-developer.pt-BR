---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2WebMessageReceivedEventHandler
ms.openlocfilehash: 77af4fc8c3e05e46883e6d2428d9fa9015815f8b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010366"
---
# 0.9.579-ICoreWebView2WebMessageReceivedEventHandler de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

O chamador implementa essa interface para receber o evento WebMessageReceived.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Invocar](#invoke) | Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

## Parte

#### Invocar 

Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

> Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) * Sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) * args)

