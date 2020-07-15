---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 52218ddcbecdaf3bdb736af877493c85d4460c10
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878040"
---
# 0.8.355-IWebView2WebView2 de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2WebView2
  : public IUnknown
```

Funcionalidades adicionais implementadas pelo objeto WebView primário.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Parar](#stop) | Interrompa todas as navegações e buscas de recursos pendentes.

Você pode QueryInterface para essa interface do objeto que implementa [IWebView2WebView](IWebView2WebView.md). Consulte a interface [IWebView2WebView](IWebView2WebView.md) para obter mais detalhes.

## Parte

#### Parar 

Interrompa todas as navegações e buscas de recursos pendentes.

> público- [limite](#stop)HRESULT ()

