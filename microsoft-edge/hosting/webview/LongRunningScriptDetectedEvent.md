---
description: ''
title: Objeto LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 6cf7af656531eea5046f7af44d4d43ff224d0f08
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560975"
---
# Objeto LongRunningScriptDetectedEvent

Fornece informações para [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).

## Propriedades

### ExecutionTime

Obtém o número de milissegundos durante os quais o elemento [WebView](../webview.md) está executando um script de longa execução.

```js
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```

#### Valor da propriedade
Tipo: **longo**

### stopPageScriptExecution
Interrompe um script de execução longa em execução no elemento [WebView](../webview.md) .

```js
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```

#### Valor da propriedade
Tipo: **booliano**