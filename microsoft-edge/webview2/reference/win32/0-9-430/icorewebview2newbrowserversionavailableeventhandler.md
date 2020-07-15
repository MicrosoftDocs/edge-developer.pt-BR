---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 42f63855c97363dab1a19cc784cf654afc40de74
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877844"
---
# 0.9.430-ICoreWebView2NewBrowserVersionAvailableEventHandler de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

O chamador implementa essa interface para receber eventos NewBrowserVersionAvailable.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Invocar](#invoke) | Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

Use o método get_NewVersion de [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) para obter o novo número de versão.

## Parte

#### Invocar 

Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

> [chamada](#invoke)a Public HRESULT ([ICoreWebView2Environment](ICoreWebView2Environment.md) * webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) * args)

