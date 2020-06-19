---
description: Representa uma cadeia de caracteres de notificação passada do conteúdo WebView para o aplicativo
title: Objeto ScriptNotifyEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 164bfa7228b1f4ccf9817e4b7231361d090f1394
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752007"
---
# Objeto ScriptNotifyEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Um objeto que representa um evento disparado quando o conteúdo contido no [WebView](../webview.md) passa uma cadeia de caracteres para o aplicativo usando JavaScript.  

## Propriedades  

### callingUri  

Obtém o URI (Uniform Resource Identifier) da página que contém o script que disparou o **ScriptNotifyEvent**.  

Essa propriedade é somente leitura.  

```javascript
var callingUri = ScriptNotifyEvent.callingUri;
```  

#### Valor da propriedade  

Tipo: **DOMString**  

### value  

O nome do método como passado para o aplicativo.  

Essa propriedade é somente leitura.  

```javascript
var value = ScriptNotifyEvent.value;
```  

#### Valor da propriedade  

Tipo: **DOMString**  
