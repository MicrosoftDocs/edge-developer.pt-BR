---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: bacd1cff4406caffd4d7c3e1ca4c3e320c051443
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878320"
---
# 0.8.355-IWebView2NewWindowRequestedEventHandler de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

O chamador implementa essa interface para receber eventos NewWindowRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Invocar](#invoke) | Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

## Parte

#### Invocar 

Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

> Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) * WebView,[IWebView2NewWindowRequestedEventArgs](IWebView2NewWindowRequestedEventArgs.md) * args)

