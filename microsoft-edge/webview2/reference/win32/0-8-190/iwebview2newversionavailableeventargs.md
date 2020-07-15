---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: e8965ebe2e0434d83b4d6e8eabe74466adb7cec6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878341"
---
# 0.8.355-IWebView2NewVersionAvailableEventArgs de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

Args de evento para o evento NewVersionAvailable.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_NewVersion](#get_newversion) | As informações de versão do navegador do [IWebView2Environment](IWebView2Environment.md)atual.

## Parte

#### get_NewVersion 

As informações de versão do navegador do [IWebView2Environment](IWebView2Environment.md)atual.

> [get_NewVersion](#get_newversion)público HRESULT (LPWSTR * NewVersion)

