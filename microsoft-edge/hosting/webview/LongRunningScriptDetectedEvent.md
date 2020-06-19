---
description: ''
title: Objeto LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 5fe90495b83ab8f95ee594d3400c8c1a26f0547e
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752147"
---
# Objeto LongRunningScriptDetectedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Fornece informações para [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).  

## Propriedades  

### ExecutionTime  

Obtém o número de milissegundos durante os quais o elemento [WebView](../webview.md) está executando um script de longa execução.  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### Valor da propriedade  

Tipo: **longo**  

### stopPageScriptExecution  

Interrompe um script de execução longa em execução no elemento [WebView](../webview.md) .  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### Valor da propriedade  

Tipo: **booliano**  
