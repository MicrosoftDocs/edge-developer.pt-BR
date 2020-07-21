---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 9f56ba33534c76cb1bd60c01a88eedfced45f1fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884858"
---
# 0.9.430-ICoreWebView2NewBrowserVersionAvailableEventArgs de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

