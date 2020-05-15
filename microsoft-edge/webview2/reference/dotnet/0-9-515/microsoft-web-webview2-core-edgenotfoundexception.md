---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 55ada31485ef061bb3649fb5e2a2811358913dd7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652432"
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
