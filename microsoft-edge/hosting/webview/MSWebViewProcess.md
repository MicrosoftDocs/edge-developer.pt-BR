---
description: Representa um processo WebView.
title: Objeto MSWebViewProcess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 7581f6da3a23295180c50f6d41cc282ce998b64e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560968"
---
# Objeto MSWebViewProcess

Representa um processo [WebView](../webview.md) .

```js
var wvprocess = new MSWebViewProcess();
```

## Propriedades

### enterpriseid

A ID da empresa do processo.

```js
var enterpriseId = wvprocess.enterpriseId;
```

Essa propriedade é somente leitura.

#### Valor da propriedade
Tipo: **DOMString**

### isPrivateNetworkClientServerCapabilityEnabled

Obtém um valor que indica se o processo [WebView](../webview.md) tem a [declaração de funcionalidade do aplicativo](/windows/uwp/packaging/app-capability-declarations) universal do Windows de *redes privadas (cliente & servidor)* habilitada no manifesto do aplicativo.

```js
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```

Essa propriedade é somente leitura.

#### Valor da propriedade
Tipo: **booliano**

## Métodos

### CreateWebViewAsync

Cria uma [WebView](../webview.md) em um processo específico.

```js
wvprocess.createWebviewAsync();
```

#### Valor de retorno

Digite**`Promise<MSHTMLWebViewElement>`**

### Webviews

Retorna uma sequência de objetos **MSWebViewProcess** hospedados no processo.

#### Valor de retorno

Digite**`sequence<MSHTMLWebViewElement>`**

### Inesperada

Finaliza o processo.

```js
wvprocess.terminate();
```

#### Valor de retorno

Esse método não retorna um valor.
