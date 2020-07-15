---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: f59b5acac510b66eae0e1ada51e28b6dd9363ca8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877851"
---
# 0.9.430-ICoreWebView2NewBrowserVersionAvailableEventArgs de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

Args de evento para o evento NewBrowserVersionAvailable.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_NewVersion](#get_newversion) | As informações de versão do navegador do [ICoreWebView2Environment](ICoreWebView2Environment.md)atual.

## Parte

#### get_NewVersion 

As informações de versão do navegador do [ICoreWebView2Environment](ICoreWebView2Environment.md)atual.

> [get_NewVersion](#get_newversion)público HRESULT (LPWSTR * NewVersion)

