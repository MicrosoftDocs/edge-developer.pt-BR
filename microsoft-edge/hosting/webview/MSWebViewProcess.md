---
description: Representa um processo WebView.
title: Objeto MSWebViewProcess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: bb70b0e8eb12c7a7c23d71f01ea24e9084caa156
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752149"
---
# Objeto MSWebViewProcess  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Representa um processo [WebView](../webview.md) .  

```javascript
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

```javascript
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```  

Essa propriedade é somente leitura.  

#### Valor da propriedade  

Tipo: **booliano**  

## Métodos  

### CreateWebViewAsync  

Cria uma [WebView](../webview.md) em um processo específico.  

```javascript
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

```javascript
wvprocess.terminate();
```  

#### Valor de retorno  

Esse método não retorna um valor.  
