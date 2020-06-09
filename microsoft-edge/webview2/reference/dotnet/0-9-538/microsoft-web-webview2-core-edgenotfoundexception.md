---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: b7d738628d6627232780e003f126b45c0421d6f0
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698232"
---
# Classe Microsoft. Web. WebView2. Core. EdgeNotFoundException 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

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

