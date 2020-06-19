---
description: Define propriedades que habilitam ou desabilitam recursos do WebView
title: Objeto MSWebViewSettings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 147f852f8fbcb2a748c00b472814e9cc45b9c9da
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752175"
---
# Objeto MSWebViewSettings  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Define propriedades que habilitam ou desabilitam os recursos do [WebView](../webview.md) .  

## Propriedades  

### isIndexedDBEnabled  

Obtém ou define um valor que indica se o uso de IndexedDB é permitido no [WebView](../webview.md).  

```javascript
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```  

#### Valor da propriedade  

Tipo: **booliano**  

**True** se IndexedDB for permitido no **WebView**; caso contrário, **false**.  

### isJavaScriptEnabled  

Obtém ou define um valor que indica se o uso de JavaScript é permitido no [WebView](../webview.md).  

```javascript
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```  

#### Valor da propriedade  

Tipo: **booliano**  

**Verdadeiro** O JavaScript é permitido no [WebView](../webview.md); caso contrário, **false**.  

### isScriptNotifyAllowed  

Obtém ou define um valor que indica se o uso de [ScriptNotifyEvent](ScriptNotifyEvent.md) é permitido no [WebView](../webview.md).  

```javascript
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```  

#### Valor da propriedade  

Tipo: **booliano**  

**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) é permitido no [WebView](../webview.md); caso contrário, **false**.  
