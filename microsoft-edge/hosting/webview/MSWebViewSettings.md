---
description: Define propriedades que habilitam ou desabilitam recursos do WebView
title: Objeto MSWebViewSettings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 0e164e7eb44edc636201f283ec4bbe866a122b8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560966"
---
# Objeto MSWebViewSettings

Define propriedades que habilitam ou desabilitam os recursos do [WebView](../webview.md) .

## Propriedades

### isIndexedDBEnabled

Obtém ou define um valor que indica se o uso de IndexedDB é permitido no [WebView](../webview.md).

```js
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```

#### Valor da propriedade
Tipo: **booliano**

**True** se IndexedDB for permitido no **WebView**; caso contrário, **false**. 

### isJavaScriptEnabled

Obtém ou define um valor que indica se o uso de JavaScript é permitido no [WebView](../webview.md).

```js
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```

#### Valor da propriedade
Tipo: **booliano**

**Verdadeiro** O JavaScript é permitido no [WebView](../webview.md); caso contrário, **false**. 

### isScriptNotifyAllowed

Obtém ou define um valor que indica se o uso de [ScriptNotifyEvent](ScriptNotifyEvent.md) é permitido no [WebView](../webview.md).

```js
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```

#### Valor da propriedade
Tipo: **booliano**

**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) é permitido no [WebView](../webview.md); caso contrário, **false**. 
