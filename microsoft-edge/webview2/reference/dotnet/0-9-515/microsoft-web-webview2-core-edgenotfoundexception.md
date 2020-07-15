---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: db4a903ca430541fa9edec9d953bf28531f7c0a4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879601"
---
# classe 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

```
class Microsoft.Web.WebView2.Core.EdgeNotFoundException
  : public Exception
```

A exceção que é lançada quando uma instalação de borda está ausente.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[EdgeNotFoundException](#edgenotfoundexception) | Inicializa uma nova instância da classe EdgeNotFoundException.
[EdgeNotFoundException](#edgenotfoundexception) | Inicializa uma nova instância da classe EdgeNotFoundException com uma referência à exceção interna que é a causa dessa exceção.
[EdgeNotFoundException](#edgenotfoundexception) | Inicializa uma nova instância da classe EdgeNotFoundException com uma mensagem de erro especificada.
[EdgeNotFoundException](#edgenotfoundexception) | Inicializa uma nova instância da classe EdgeNotFoundException com uma mensagem de erro especificada e uma referência à exceção interna que é a causa dessa exceção.

## Parte

#### EdgeNotFoundException 

Inicializa uma nova instância da classe EdgeNotFoundException.

> [EdgeNotFoundException](#edgenotfoundexception)público ()

#### EdgeNotFoundException 

Inicializa uma nova instância da classe EdgeNotFoundException com uma referência à exceção interna que é a causa dessa exceção.

> [EdgeNotFoundException](#edgenotfoundexception)público (exceção interna)

##### Parâmetros
* `inner` A exceção que é a causa da exceção atual.

#### EdgeNotFoundException 

Inicializa uma nova instância da classe EdgeNotFoundException com uma mensagem de erro especificada.

> Public [EdgeNotFoundException](#edgenotfoundexception)(mensagem de cadeia de caracteres)

##### Parâmetros
* `message` A mensagem de erro que explica o motivo da exceção.

#### EdgeNotFoundException 

Inicializa uma nova instância da classe EdgeNotFoundException com uma mensagem de erro especificada e uma referência à exceção interna que é a causa dessa exceção.

> Public [EdgeNotFoundException](#edgenotfoundexception)(mensagem de cadeia de caracteres, exceção interna)

##### Parâmetros
* `message` A mensagem de erro que explica o motivo da exceção. 

* `inner` A exceção que é a causa da exceção atual.

