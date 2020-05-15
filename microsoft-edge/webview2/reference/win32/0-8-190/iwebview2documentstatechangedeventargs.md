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
ms.openlocfilehash: 342716da2cded9c903f1edd13fb3400c779a9b39
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652592"
---
# interface IWebView2DocumentStateChangedEventArgs 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

Args de evento para o evento DocumentStateChanged.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_IsNewDocument](#get_isnewdocument) | True se a página à qual está sendo acessada for um novo documento.
[get_IsErrorPage](#get_iserrorpage) | Verdadeiro se o conteúdo carregado for uma página de erro.

## Parte

#### get_IsNewDocument 

True se a página à qual está sendo acessada for um novo documento.

> [get_IsNewDocument](#get_isnewdocument)público HRESULT (bool * IsNewDocument)

#### get_IsErrorPage 

Verdadeiro se o conteúdo carregado for uma página de erro.

> [get_IsErrorPage](#get_iserrorpage)público HRESULT (bool * IsErrorPage)

