---
description: Representa uma cadeia de caracteres de notificação passada do conteúdo WebView para o aplicativo
title: Objeto ScriptNotifyEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 22313f2d96ca2c5d4d3554ca40589b9a583c89cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560492"
---
# Objeto ScriptNotifyEvent

Um objeto que representa um evento disparado quando o conteúdo contido no [WebView](../webview.md) passa uma cadeia de caracteres para o aplicativo usando JavaScript.

## Propriedades
    
### callingUri

Obtém o URI (Uniform Resource Identifier) da página que contém o script que disparou o **ScriptNotifyEvent**.

Essa propriedade é somente leitura.

```js
var callingUri = ScriptNotifyEvent.callingUri;
```

#### Valor da propriedade
Tipo: **DOMString**

### value

O nome do método como passado para o aplicativo.

Essa propriedade é somente leitura.

```js
var value = ScriptNotifyEvent.value;
```

#### Valor da propriedade
Tipo: **DOMString**