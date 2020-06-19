---
description: Contém informações sobre a navegação da WebView completada
title: Objeto NavigationCompletedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: eb5727ab59dbaf056f05ab4b19450c70f85d595f
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752133"
---
# Objeto NavigationCompletedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Um objeto que representa um evento disparado quando o [WebView](../webview.md) concluiu o carregamento do conteúdo atual ou se houve falha na navegação.  

## Propriedades  

### uri  

O URI (Uniform Resource Identifier) da navegação.  

Essa propriedade é somente leitura.  

```javascript
var uri = NavigationCompletedEvent.uri;
```  

#### Valor da propriedade  

Tipo: **DOMString**  

### IsSuccess  

Obtém um valor que indica se a navegação foi concluída com sucesso.  

Essa propriedade é somente leitura.  

```javascript
var isSuccess = NavigationCompletedEvent.isSuccess;
```  

#### Valor da propriedade  

Tipo: **booliano**  

### webErrorStatus  

Se a navegação não tiver sido bem-sucedida, obtém um valor que indica o motivo.  

Essa propriedade é somente leitura.  

```javascript
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```  

#### Valor da propriedade  

Tipo: **unsigned long**  
