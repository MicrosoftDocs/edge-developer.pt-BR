---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 0314c796865d3d745b831d050498f59868e38e8f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652686"
---
# interface IWebView2NewVersionAvailableEventArgs 

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

