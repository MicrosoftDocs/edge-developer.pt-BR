---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: fc65d857f11a77a1d3629d40266f0453acadaa7b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886308"
---
# classe 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

