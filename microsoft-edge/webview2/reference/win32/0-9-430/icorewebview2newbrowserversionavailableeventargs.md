---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 3ac37f7d90fc03214381b991c8becae602bac738
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652587"
---
# interface ICoreWebView2NewBrowserVersionAvailableEventArgs 

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

