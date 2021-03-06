---
description: Objeto LongRunningScriptDetectedEvent
title: Objeto LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: webview, aplicativos do Windows 10, uwp, borda
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5f5eb3230e46ee2cd7926b21f6526e512a7a0322
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397935"
---
# <a name="longrunningscriptdetectedevent-object"></a>Objeto LongRunningScriptDetectedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Fornece informações para [MSWebViewLongRunningScriptDetected](../webview/index.md#mswebviewlongrunningscriptdetected).  

## <a name="properties"></a>Propriedades  

### <a name="executiontime"></a>executionTime  

Obtém o número de milissegundos que o [elemento Webview](../webview/index.md) está executando um script de longa execução.  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### <a name="property-value"></a>Valor da propriedade  

Tipo: **longo**  

### <a name="stoppagescriptexecution"></a>stopPageScriptExecution  

Interrompe a execução de um script de longa duração no [elemento webview.](../webview/index.md)  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### <a name="property-value"></a>Valor da propriedade  

Tipo: **Boolean**  
