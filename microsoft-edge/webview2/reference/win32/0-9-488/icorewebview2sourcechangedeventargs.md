---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 9ea8f860d637c5d9e49e68917d167380c0418b87
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877368"
---
# 0.9.515-ICoreWebView2SourceChangedEventArgs de interface 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

Argumentos de evento para o evento SourceChanged.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_IsNewDocument](#get_isnewdocument) | True se a página à qual está sendo acessada for um novo documento.

## Parte

#### get_IsNewDocument 

True se a página à qual está sendo acessada for um novo documento.

> [get_IsNewDocument](#get_isnewdocument)público HRESULT (bool * IsNewDocument)

